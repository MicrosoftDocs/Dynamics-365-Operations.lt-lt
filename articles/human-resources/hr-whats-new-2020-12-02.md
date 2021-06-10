---
title: Kas naujo ar pasikeitusio „Dynamics 365 Human Resources“ 2020 m. gruodžio 2 d.
description: Ši tema aprašo funkcijas, kurios yra naujos arba pakeistos „Microsoft Dynamics 365 Human Resources“ nuo 2020 m. gruodžio 2 d.
author: marcelbf
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fa772691eebd177cae8cb8e470a48d27d1f33822
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054867"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>Kas naujo ar pasikeitusio „Dynamics 365 Human Resources“ 2020 m. gruodžio 2 d.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomos naujos, pasikeitusios ar netrukus pasirodysiančios „Dynamics 365 Human Resources“ funkcijos.

Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2020 m. 2-os leidimo bangos apžvalga](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.3788 komponavimo versijai.

### <a name="new-features"></a>Naujos funkcijos

Šiame leidime bendrai prieinamos toliau pateiktos funkcijos.

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Vadovai gali pateikti įdarbinimo užklausas darbo vietoms | [Vadovai gali pateikti įdarbinimo užklausą atvirai darbo vietai](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Įtraukti įdarbinimo užklausą](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Papildytas kandidato profilis personalo valdyme | [Papildytas kandidato profilis personalo valdyme](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Įtraukite ar redaguokite kandidato profilį](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Įjunkite supaprastintas integracijas su įdarbinimo tiekėjais | [Įjunkite supaprastintas integracijas su įdarbinimo tiekėjais](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Įdarbinti darbo kandidatai](./hr-personnel-recruit.md) |
| Pasirinktiniai saitai vadovų savitarnoje | [Pasirinktiniai saitai vadovų savitarnoje](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Pasirinktiniai saitai vadovų savitarnoje](./hr-employee-manager-self-service-custom-links.md) |


### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šią temą, kad būtų įtraukti klaidų ištaisymai, įtraukti į komponavimo versiją publikavus šią temą.

| Problemos numeris | Išdavimas | aprašymas |
| --- | --- | --- |
| 514087 | BenefitEligibilityProcessResult turi apimti datą ir laiką, kuris buvo naudojamas apdorojimo metu. | BenefitEligibility apdorojimo rezultatai dabar apima duomenų laiko antspaudą paskutiniam apdorojimui, kurio trūko anksčiau. |
| 526903 | Priedų įtraukimas nepavyksta planams su priklausiniais, kai **Automatinio pasirinkimo gavėjai** yra įjungti **Žmogiškųjų išteklių bendrinti parametrai**. | Fiksuota problema, kai naudos įtraukimas nepavyko priklausiniams, kai **Automatinio pasirinkimo gavėjų** parinktis buvo įjungta nustatytiesiems gavėjams. |
| 521922 | **Rodyti nebuvimą be išsamios informacijos** parametras rodo nebuvimo užklausų išsamią informaciją komandos nebuvimo kalendoriuje. | Atostogų tipas, atostogų tipo spalva ir dienų išsami informacija buvo rodoma komandos nebuvimo kalendoriuje, kai **Rodyti nebuvimą be išsamios informacijos** buvo nustatytas į **Taip** skyriuje **Atostogų ir nebuvimo parametrai**. Tai buvo pažymėta ir dabar atostogų tipas neberodomas ir nustatytoji atostogų tipo spalva (tamsiai mėlyna) yra naudojama visiems atostogų tipams komandos nebuvimo kalendoriuje. |
| 527316 | Pareigų keitimai darbui, pareigoms ir darbuotojo pranešimams nesinchronizuojami. | Pareigų ryšys anksčiau buvo įtrauktas į darbą, pareigas ir darbuotojo objektus. Sinchronizavimas su šiais susijusiais darbais sinchronizavimui žmogiškuosiuose ištekliuose į „Dataverse“, bet neveikia pranešimams iš „Dataverse“. Tai buvo pažymėta. |
| 512275 | Pašalinkite spalvos parinktis iš **Atostogų ir nebuvimo parametrai**. | Dabar spalvos yra nustatytos pagal atostogų tipą, spalvų parinktys nebėra reikalingos **Atostogų ir nebuvimo parametrams**, dėl to jos buvo panaikintos. |
| 437112 | Neteisingas klaidos pranešimo tekstas darbuotojo padėties priskyrime. | Naujintas klaidos pranešimas darbuotojo samdymo metu ir bandymas priskirti darbuotoją pareigoms neveikia. Naujintas pranešimas **Nurodyta padėtis nebeveikia kaip darbuotojo pradžios data. Prašome patikrinti šių pareigų trukmę.** |
| 527816 | Vykdymo triktys su **Nebuvimo** puslapiu. | Vykdymas buvo pagerintas pagal **Nebuvimą** puslapiu. |
| 523158 | BenefitPeriodMigrationUpgrade ir BenefitPlanMigrationUpgrade nevyksta. | Ištaisytos triktys su priedų perkėlimo darbais susijusiais su **Laikotarpiu** ir **Planavimo** tinkamai neveikia. |

## <a name="in-preview"></a>Peržiūros režimu

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie funkcijų įjungimą ir išjungimą žr. [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| „Human Resources“ programa, esanti „Microsoft Teams” | [Darbuotojo atostogos ir neatvykimai „Microsoft Teams”](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [„Human Resources“ programa „Teams“](./hr-admin-teams-leave-app.md)<br>[Atostogų prašymų valdymas „Teams“](hr-teams-leave-app.md) |
| Patobulintos darbo eigos užklausos ir patvirtinimai | [Organizacijos ir personalo valdymo darbo eigos patobulinimai](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigūracijos parinktis, skirta sąrašui Man priskirti darbo elementai perkelti](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Integravimas su „LinkedIn Talent Hub“ | [Integravimas su „LinkedIn Talent Hub“](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integravimas su „LinkedIn Talent Hub“](./hr-admin-integration-linkedin.md) |
|Kryžminės įmonės rodinys atostogų vadovams | [Kryžminės įmonės rodinys darbuotojų atostogų vadovams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Atostogų ir neatvykimų parametrų konfigūravimas](./hr-leave-and-absence-parameters.md) |
|Pateikite papildomas įžvalgas apie atostogų balansus| [Pateikite papildomas įžvalgas apie atostogų balansus](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Darbuotojų atostogų valdymas](./hr-leave-and-absence-manage-employee-leave.md) |
| Vadovai gali pateikti įdarbinimo užklausas darbo vietoms | [Vadovai gali pateikti įdarbinimo užklausą atvirai darbo vietai](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Įtraukti įdarbinimo užklausą](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Papildytas kandidato profilis personalo valdyme | [Papildytas kandidato profilis personalo valdyme](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Įtraukite ar redaguokite kandidato profilį](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Įjunkite supaprastintas integracijas su įdarbinimo tiekėjais | [Įjunkite supaprastintas integracijas su įdarbinimo tiekėjais](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Įdarbinti darbo kandidatai](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>Jau greitai

Norėdami gauti visą planuojamų funkcijų ir jų suplanuotų leidimų sąrašą, žr. [„Dynamics 365 Human Resources” 2020 m. 2-os leidimo bangos apžvalga](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2020 m. leidimo 2 bangos apžvalga](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]