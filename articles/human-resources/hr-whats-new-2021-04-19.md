---
title: Kas nauja arba pasikeitė 2021 m. balandžio 19 d. „Dynamics 365 Human Resources”
description: Šiame straipsnyje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2021 m. balandžio 19 d.
author: marcelbf
ms.date: 04/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e46c5721853ebfe3b9d5955ca5f4e7a4ead570c1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846306"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-19-2021"></a>Kas nauja arba pasikeitė 2021 m. balandžio 19 d. „Dynamics 365 Human Resources”

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomos priemonės, kurios yra naujos, pakeistos arba tuoj pat Dynamics 365 Human Resources.

Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2021 m. 1-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.4113 komponavimo versijai.

### <a name="new-features"></a>Naujos funkcijos

Šiame leidime bendrai prieinamos toliau pateiktos funkcijos.

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Platformos atnaujinimas 10.0.17 (41) | -- | [Finansų ir operacijų programėlių 10.0.17 versijos platformos naujinimai (2021 m. balandžio mėn.)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md) |
| Pasirinktinių laukų palaikymas išmokų valdymo formose | [Pasirinktinių laukų palaikymas išmokų valdyme](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management)| [Išmokų valdymo apžvalga](hr-benefits-management-overview.md)|

### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šį straipsnį, kad būtų įtrauktos pataisos, kurios buvo sukurtas po to, kai buvo publikuotas šis straipsnis.

| Problemos numeris | Problema |  Aprašymas |
| --- | --- | --- |
| 552164 | **Įrašytas** darbuotojų **savitarnos paslaugos rodinys >** Atviri kursai ne darbo su darbotvarke | Jei atidarytuose kursuose (ESS) naudojamas įrašytas rodinys ir prie vieno iš kursų pridėta darbotvarkė, rodinyje daugiau nebus parodytos kelios to kurso eilutės |
| 560614 | **Išmokos > Gyvenimo įvykio pasirinktys** rodo nesutapimų patarimo dokumentuose ir kodo elgsenoje. | Atnaujinti patarimai dėl naudojimo laiko **įvykio parinkčių, kad** būtų rodomas teisingas veikimo būdas. |
| 560616 | **Išmokos > Gyvenimo įvykio** parinktys yra redaguojamos darbuotojų išmokų plane, tačiau pakeitimai nėra paveikiami. | Atnaujintas gyvenimo įvykio parinkties raktų veikimas, siekiant įgalinti arba uždrausti, remiantis priklausomų pasirinkčių, patarimo dokumentacijoje. |
| 565054 | Nepavyksta peržiūrėti darbuotojų **be įdarbinimo sąrašo** turinio, kai yra išplėstinė **prieiga**. | Šiame leidime ištaisoma problema, kuri, kai buvo įjungta išplėstinė prieiga, tik sistemos administratoriai gali peržiūrėti **darbuotojų turinį be** įdarbinimo **sąrašo**. Kadangi šis taisymas yra saugos pakeitimas, turėsite pasirinkti jį funkcijų valdymo srityje. Kai priemonė yra, tie vaidmenys, kurie turi prieigą prie formos, matys turinį, nors ir yra išplėstinė prieiga. Daugiau informacijos rasite [Darbuotojai be įdarbinimo](hr-personnel-workers-without-employment.md). |
| 570586 | Atostogų užklausų patikrinimas nesėkmingas, kai darbas baigiasi anksčiau nei paskutinė to darbuotojo operacija visuose atostogų planuose. | Kai darbas baigiasi, atostogų užklausos tikrinimas neateis dėl darbuotojo atostogų operacijų.|
| 570783 | Įgalinus ir užjungus visų įmonių atostogas personalo bendrinamuose parametruose, pasikeičia tai, kurie darbuotojai, įdarbinti vienoje įmonėje, mato atostogų užklausas. | Vienoje įmonėje įdarbinti darbuotojai nematote jokių pasirašančiųjų laiko pakeitimų, jei parametras įgalintas ar išjungtas. |
| 572343 | Būtinas priežasties kodas nerodomas, kai įgalinta kelių įmonių atostogų rodinio priemonė. | Kai būtinas priežasties kodas nerodomas, priežasties kodas rodomas kaip tikėtasi. |
| 573676 | Negalima įtraukti laikotarpio **į** Išmokų valdymas **> Saitai > Išmokų** planai. | Fiksuotos klaidos, **kurių** laikotarpio nepavyko įtraukti arba atnaujinti esamoje išmokų **plano** formoje. |

## <a name="in-preview"></a>Peržiūros režimu

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie funkcijų įjungimą ir išjungimą žr. [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Išmokų valdymo darbo sritis | [Išmokų valdymo darbo sritis (peržiūra)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Išmokų valdymo darbo sritis](hr-benefits-management-workspace.md) |
| Atostogų ir neatvykimų darbo eigos patirties patobulinimai | [Atostogų ir neatvykimų darbo eigos patirties patobulinimai](https://go.microsoft.com/fwlink/?linkid=2147528) | [Prašyti išleisti iš darbo](hr-employee-self-service-request-time-off.md)|
| Įgalinti supaprastintą algalapio integravimą (algalapio integravimo API) | [Įjunkite supaprastintas integraciją su mokėjimo tiekėjais](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Algalapių integravimo API](hr-admin-integration-payroll-api-introduction.md)|

## <a name="coming-soon"></a>Jau greitai

| Funkcija | Informacija |
| --- | --- |
| Vadovo įvesti įgūdžiai savo darbuotojams gali būti automatiškai patvirtinami darbo eigos | Greitai bus išleista. |
| Platformos atnaujinimas 10.0.18 (42) | Platformos atnaujinimas 10.0.18 yra suplanuotas pasirodyti su nauju leidimu 2021 m. gegužės 17 d. Daugiau informacijos rasite finansų ir [operacijų programėlių 10.0.18 versijos platformos atnaujinimų (2021 m. gegužės mėn.)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Pasirinktinių laukų palaikymas išmokų valdyme pagal atitinkamas taisykles  | [Pasirinktinio lauko palaikymas tinkamumo apdorojimui](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Norėdami gauti visą planuojamų funkcijų ir jų suplanuotų leidimų sąrašą, žr. [„Dynamics 365 Human Resources” 2021 m. 1-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2021 m. leidimo 1 bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
