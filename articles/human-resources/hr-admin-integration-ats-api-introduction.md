---
title: Aplikanto sekimo sistemos integravimo API įžanga
description: Šiame straipsnyje aprašoma pretendento Dynamics 365 Human Resources sekimo sistemos (ATS) integravimo API.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6037d09fdc484753c7e90a896ce383bd71391356
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894707"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a>Aplikanto sekimo sistemos integravimo API įžanga


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašoma pretendento Dynamics 365 Human Resources sekimo sistemos (ATS) integravimo API. API paskirtis yra įjungti paleistą integravimą tarp „Dynamics 365 Human Resources“ ir partnerio ATS.

![ATS integravimo eiga.](media/hr-admin-integration-ats-api-introduction-flow.png)

Integruota patirtis prasideda žmogiškuosiuose ištekliuose, kai samdantis vadovas sukuria samdymo užklausą. Kai užklausa aktyvuota, ATS ištraukia išsamią informaciją užklausai siekiant sukurti samdymo projektą. Tuomet jis seka samdymo vamzdynu, kad pasirinktų ir samdytų pretendentą pareigoms. Galiausiai ATS užbaigia kelionę aplink integravimą nusiųsdama pasirinkto pretendento įrašą žmogiškiesiems ištekliams. Pretendento įrašas tada gali praeiti pro daugiau samdymo patvirtinimų ir darbo eigų, kad sukurtų darbuotojo įrašą.

Norėdami įjungti integravimą, žmogiškieji ištekliai įtraukė šiuos komponentus:

1.  Funkcijas siekiant sukurti samdymo užklausą.
2.  Išplėsto kandidato profilis ir susijusios darbo eigos.
3.  API integravimas atveriantis naujas funkcijas siekiant integruoti paraiškas.

Dėl daugiau informacijos apie samdymo užklausų ir pretendentų funkcijų nustatymą ir naudojimą žr. [Samdyti pretendentus darbui](hr-personnel-recruit.md).

## <a name="microsoft-dataverse"></a>„Microsoft Dataverse“

API yra sukurtos „Microsoft Dataverse“ (anksčiau „Common Data Service“). Visos RESTful sąveikos su šiuo API yra daromos per „Microsoft Dataverse“ žiniatinklio API, kurios naudoja OData. Šis API yra papildomas rinkinys „Dataverse“ žiniatinklio API. „Dataverse“ žiniatinklio API nustato savybes, tokias kaip autentifikavimas, SLA, rinkinys, konkurencijos kontrolė ir klaidų tvarkymas.

Dėl bendresnės informacijos apie „Microsoft Dataverse“ žiniatinklio API, žr.:

- [Kas yra „Microsoft Dataverse“?](/powerapps/maker/data-platform/data-platform-intro)
- [Naudokite „Microsoft Dataverse“ žiniatinklio API](/powerapps/developer/data-platform/webapi/overview)
- [„Microsoft Dataverse“ kūrėjo gairės](/powerapps/developer/data-platform)

Prieš tai buvusi dokumentacija apima išsamią informaciją ir kūrėjo gaires apie „Dataverse“ žiniatinklio API naudojimą, tokias kaip [autentifikavimo valdymas](/powerapps/developer/data-platform/webapi/authenticate-web-api), [operacijų atlikimas](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](/powerapps/developer/data-platform/webapi/use-postman-web-api) ir [sekimo keitimo naudojimas ir delta žymos](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) su API.

### <a name="option-sets"></a>Parinkties rinkiniai

Duomenų modelis ATS integravimui API aprašoma šiame dokumente apima parinkčių rinkinius, kurie pateikia numeravimo vertes susietas su objekto ypatybėmis. Dėl išsamaus darbo su parinkčių rinkiniais „Dataverse“ žiniatinklių API, žr. [Kurti ir naujinti parinkčių rinkinius su žiniatinklio API](/powerapps/developer/data-platform/webapi/create-update-optionsets). Parinkčių rinkiniai yra nustatyti kiekvienai „Dataverse“ aplinkai.

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Virtualios lentelės žmogiškiesiems ištekliams „Dataverse“

Galutiniai taškai ATS integravimui API naudoja virtualios lentelės platformos galimybes „Microsoft Dataverse“. Pagal nutylėjimą, virtualios lentelės ir jų susieti API galutiniai taškai nėra talpinami žmogiškųjų išteklių aplinkose, įjungiant organizacijas tam, kad jos nustatytų, kurie OData galutiniai taškai turi būti rodomi aplinkoje. Norėdami naudoti API, virtualios lentelės, skirtos žmogiškųjų išteklių objektams, turi būti sukurtos aplinkoje. 

Dėl informacijos apie virtualių lentelių kūrimą API, žr. [Konfigūruoti „Dataverse“ virtualias lenteles](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>Duomenų modelis

Duomenų modelis yra sukoncentruotas apie du pagrindinius objektus:

- **Samdymo užklausą** rodančią užklausą ATS siekiant pasamdyti asmenis į vieną ar daugiau atvirų pareigų. Dėl užklausos pavyzdžio, žr. [Pavyzdžio užklausa samdymo užklausai](hr-admin-integration-ats-api-recruiting-request-example-query.md).
- **Samdomas pretendentas** rodo pretendento išsamią informaciją, kuris priėmė pasiūlymą į pareigas. **Asmuo** rodo asmenį, kuris yra pretendentas. Asmuo gali turėti kelis vaidmenis įmonėje, tokius kaip pretendentas, darbuotojas, darbininkas ar rangovas. Dėl pavyzdžio užklausos, žr. [Pavyzdžio užklausa samdytinam pretendentui](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).

Tolesnėje diagramoje rodomi santykiai su API. Keli tipai turi užsienio raktus su kitais, iš anksto esantys objektai žmogiškuosiuose ištekliuose čia nerodomi. Dokumente pateikta informacija apie objektus, kurie yra būdingi samdymo integravimo scenarijams. Nepaisant to, esama daugelio kitų objektų „Dataverse“ žiniatinklio API skirtų „Dynamics 365 Human Resources“, kurie gali būti taip pat svarbūs jūsų integravimui. Pavyzdžiui, jums gali taip pat reikėti išsamios čia nenustatytos informacijos darbuotojams, darbams, pareigoms ar kitiems objektams. Daugelis šių objektų yra nukreipiami į užsienio raktų santykius ar naršymo ypatybes.

![ATS integravimo API duomenų modelis.](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a>Samdymo užklausa ir susiję objektai bei parinkčių rinkiniai

Pavyzdinė užklausa: 

- [Pavyzdinė užklausa Samdymo prašymui](hr-admin-integration-ats-api-recruiting-request-example-query.md)

Objektai:

- [Įdarbinimo užklausa](hr-admin-integration-ats-api-recruiting-request.md)
- [Įdarbinimo užklausų pareigos](hr-admin-integration-ats-api-recruiting-request-position.md)
- [Samdymo užklausos įgūdžiai](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [Samdymo užklausos išsilavinimas](hr-admin-integration-ats-api-recruiting-request-education.md)
- [Įdarbinimo užklausų vieta](hr-admin-integration-ats-api-recruiting-request-location.md)

Parinkties rinkiniai:

- [Atleidimo nuo darbo būsena](hr-admin-integration-ats-api-job-exempt-status.md)
- [Samdymo užklausos pareigų būsena](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [Samdymo užklausos būsena](hr-admin-integration-ats-api-recruiting-request-status.md)
- [Reguliavimo darbo kategorija](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a>Samdomas pretendentas ir susiję objektai ir parinkčių rinkiniai

Pavyzdinė užklausa:

- [Samdomo pretendento pavyzdžio užklausa](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

Objektai:

- [Samdytinas pretendentas](hr-admin-integration-ats-api-candidate-to-hire.md)
- [Asmuo](hr-admin-integration-ats-api-person.md)
- [Asmens išsilavinimas](hr-admin-integration-ats-api-person-education.md)
- [Asmens profesinė patirtis](hr-admin-integration-ats-api-person-professional-experience.md)
- [Asmens adresas](hr-admin-integration-ats-api-person-address.md)
- [Šalies kontaktai](hr-admin-integration-ats-api-party-contact.md)
- [Asmens įgūdžiai](hr-admin-integration-ats-api-person-skill.md)
- [Vertinimo lygis](hr-admin-integration-ats-api-rating-level.md)
- [Asmens sertifiktas](hr-admin-integration-ats-api-person-certificate.md)
- [Sertifikato tipas](hr-admin-integration-ats-api-certificate-type.md)
- [Asmens atranka](hr-admin-integration-ats-api-person-screening.md)
- [Atrankos tipai](hr-admin-integration-ats-api-screening-types.md)
- [Asmens tapatybės numeris](hr-admin-integration-ats-api-person-identification-number.md)

Parinkties rinkiniai:

- [Pretendento integravimo rezultatas](hr-admin-integration-ats-api-applicant-integration-result.md)
- [Tuščia Taip Ne](hr-admin-integration-ats-api-blank-yes-no.md)
- [Užbaigimo būsena](hr-admin-integration-ats-api-completion-status.md)
- [Kontakto tipas](hr-admin-integration-ats-api-contact-type.md)
- [Išsilavinimo kredito pagrindas](hr-admin-integration-ats-api-education-credit-basis.md)
- [Giminė](hr-admin-integration-ats-api-gender.md)
- [Šeiminė padėtis](hr-admin-integration-ats-api-marital-status.md)
- [Metų mėnesiai](hr-admin-integration-ats-api-months-of-year.md)
- [Ne Taip](hr-admin-integration-ats-api-no-yes.md)
- [Laikotarpio vienetas](hr-admin-integration-ats-api-period-unit.md)
- [Atrankos dažnumas](hr-admin-integration-ats-api-screening-frequency.md)
- [Atrankos dažnumas sukuriamas pagal](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [Įgūdžių lygio tipas](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a>Taip pat žiūrėkite

[Kandidatų į darbo vietas įdarbinimas](hr-personnel-recruit.md)<br>
[Kas yra „Microsoft Dataverse“?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Naudokite „Microsoft Dataverse“ žiniatinklio API](/powerapps/developer/data-platform/webapi/overview)<br>
[Kurti ir naujinti parinkčių rinkinius naudojant žiniatinklio API](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
