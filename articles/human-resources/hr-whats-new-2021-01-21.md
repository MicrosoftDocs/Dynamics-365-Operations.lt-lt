---
title: Kas naujo ar pasikeitusio „Dynamics 365 Human Resources“ 2021 m. sausio 21 d.
description: Šioje temoje aprašomos funkcijos, kurios yra naujos ar pasikeitusios „Microsoft Dynamics 365 Human Resources“ 2021 m. sausio 21 d.
author: marcelbf
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 02f0b0664dcb78d20c2719b4377dcc6047f2bf3392225f1cf9c166a1073ecd59
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772621"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-21-2021"></a>Kas naujo ar pasikeitusio „Dynamics 365 Human Resources“ 2021 m. sausio 21 d.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomos naujos, pasikeitusios ar netrukus pasirodysiančios „Dynamics 365 Human Resources“ funkcijos.

Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2020 m. 2-os leidimo bangos apžvalga](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.3866 komponavimo versijai.

### <a name="new-features"></a>Naujos funkcijos

Šiame leidime bendrai prieinamos toliau pateiktos funkcijos.

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Platformos naujinimas 10.0.16 (40) | -- | [Platformos naujinimai versijai 10.0.16 „Finance and Operations“ programoms (vasario 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-16.md) |
| Patobulintos darbo eigos užklausos ir patvirtinimai | [Organizacijos ir personalo valdymo darbo eigos patobulinimai](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigūracijos parinktis, skirta sąrašui Man priskirti darbo elementai perkelti](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Leistinas priežiūros aktas (ACA) atitikties naujinimai nuo 1095-C, 1095-B ir elektroninės ataskaitos ankstesnėms išlaidoms | -- | -- | 
| Išlaidų valdymas dabar palaiko ACA atitiktį ataskaitoms JAV paremtuose juridiniuose asmenyse | -- | [Kurti ACA ataskaitas išmokų valdyme](hr-benefits-management-aca-reports.md) |
| Išmokų valdymas dabar turi išmokų reitingo pakopas ir išmokų reitingo rodomus dvigubų pakopų įrašus  | -- | -- |

### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šią temą, kad būtų įtraukti klaidų ištaisymai, įtraukti į komponavimo versiją publikavus šią temą.

| Problemos numeris | Išdavimas |  aprašymas |
| --- | --- | --- |
| 533079 | Naršymo klaida „Forma buvo netinkamai pavadinta“, kai bandome ieškoti atskaitymų. | Ištaisyta klaida ieškant išmokų atskaitymų su rodiniu **Pagal datą**. |
| 543641 | ZIP kodas nėra užpildomas elektroninės ataskaitos metu.  | Ištaisyta vidaus klaida ZIP kode nepasirodo ACa elektroninės ataskaitose išmokų valdyme, kai aprėpties kodas yra nuo M iki Q. |
| 542815 | Asmens kontakto ekranas darbuotojo savitarnos paslaugose leidžia darbuotojams matyti kitus asmenų kontaktus. | Ištaisyta klaida, kai **Redaguoti** forma darbuotojo savitarnos paslaugų asmens kontaktuose neapriboja jos užklausos pakankamai, kad užtikrintų, jog vienas asmenines kontaktas yra gaunamas leidžiant vartotojui naudoti klaviatūros trumpinius siekiant peržiūrėti kitų asmenų kontaktus. |
| 536157 | Negalima atverti **„Microsoft Dataverse“ integravimo** puslapio sistemos administravime dėl pavadinimo IsVirtualEntityPackageInstalled(). | Klaida apsaugo **„Microsoft Dataverse“ integravimo** puslapį nuo paleidimo „Human Resources“. |
| 533079 | Naršymo klaida „Forma buvo netinkamai pavadinta“, kai bandome ieškoti atskaitymų. | Ištaisyta klaida, kai **Atskaitymai** vyksta iš išmokų valdymo rodant **Pagal datą**. |
| 537264 | **Asmeninės informacija** greitas skirtukas nerodomas kandidato įraše. | Asmeninė informacija kandidatui dabar prieinama kandidato įraše. |
| 537267 | **Profesinė patirtis** nerodoma vidiniuose kandidato įrašuose. | **Profesinė patirtis** greitas skirtukas dabar rodomas vidaus kandidato įrašuose. Anksčiau, jei kandidatas buvo viduje, **Profesinė patirtis** buvo pakeista **Įdarbinimo istorija**, kuri yra kandidato įdarbinimo istorija organizacijoje. Abu yra taikomi ir turi būti rodomi vidaus kandidatams. |
| 537067 | **Leidžiama kontaktuoti darbdavį** nerodoma. | Valdiklis **Leidžiama kontaktuoti darbdavį** buvo įtrauktas į **Redaguoti asmeninę patirtį** juostą kandidato įrašui. |
| 525957 | **Kandidato būsena** nenaujinama vidaus kandidatams, kai perkėlimas užbaigtas. | Kai perkėlimas užbaigiamas (**Keisti pareigas** ar **Tęsti** mygtukas pasirenkamas **Perkelti darbuotoją į naujų pareigų paskyrimą** puslapį), **Būsena** kandidato įraše turi pasikeisti į **Pasamdytas**. |
| 537051 | Šiuo metu simboliai Indijos rupiais ir Turkijos lyra nesinchronizuojami teisingai „Dataverse“ | Simboliai Indijos rupiais ir Turkijos lyra dabar sinchronizuojami teisingai „Dataverse“. |
| 534846 | Samdymo lentelės turi būti įjungtos duomenų valdymui. | Naujos lentelės sukuriamos samdymo užklausoms ir kandidatai dabar įjungti duomenų valdymui. Tai leidžia keisti sekimą, kad jis būtų įjungtas lentelėms, įjungiant „OData“ keitimą sekimo „Dataverse“ virtualiose lentelėse. |
| 533474 | Pataisyta trūkstama nuoroda į Microsoft.SqlServer.XEvent.dll. | Rinkinio užkrovimo išlygos Microsoft.SqlServer.XEvent.dll buvo užblokuotos „Dataverse“ virtualioms lentelėms nuo nustatymo kai kuriose aplinkose. |
| 481122 | **Asmenys** darbo sritis rodo pensininkų pareigas. | Nurašytos pareigos rodomos kaip atviros **Asmenų** darbo srityje. Nurašytos pareigos neberodomos. | 
| 541978 | Įtraukite priminį el. pašto adresą į pagrindinio darbuotojo įrašą. | Toks keitimas įtraukiamas į darbuotojo pirminį el. pašto adresą į HcmWorkerBaseEntity. |

## <a name="in-preview"></a>Peržiūros režimu

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie funkcijų įjungimą ir išjungimą žr. [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| „Human Resources“ programa, esanti „Microsoft Teams” | [Darbuotojo atostogos ir neatvykimai „Microsoft Teams”](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [„Human Resources“ programa „Teams“](./hr-admin-teams-leave-app.md)<br>[Atostogų prašymų valdymas „Teams“](hr-teams-leave-app.md) |
| Integravimas su „LinkedIn Talent Hub“ | [Integravimas su „LinkedIn Talent Hub“](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integravimas su „LinkedIn Talent Hub“](./hr-admin-integration-linkedin.md) |
| Kryžminės įmonės rodinys atostogų vadovams | [Kryžminės įmonės rodinys darbuotojų atostogų vadovams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Atostogų ir neatvykimų parametrų konfigūravimas](./hr-leave-and-absence-parameters.md) |
|Pateikite papildomas įžvalgas apie atostogų balansus| [Pateikite papildomas įžvalgas apie atostogų balansus](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Darbuotojų atostogų valdymas](./hr-leave-and-absence-manage-employee-leave.md) |
| Vadovai gali pateikti įdarbinimo užklausas darbo vietoms | [Vadovai gali pateikti įdarbinimo užklausą atvirai darbo vietai](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Įtraukti įdarbinimo užklausą](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Papildytas kandidato profilis personalo valdyme | [Papildytas kandidato profilis personalo valdyme](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Įtraukite ar redaguokite kandidato profilį](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Įjunkite supaprastintas integracijas su įdarbinimo tiekėjais | [Įjunkite supaprastintas integracijas su įdarbinimo tiekėjais](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Kandidatų į darbo vietas įdarbinimas](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>Jau greitai
| Funkcija | Išsamiai |
| --- | --- |
| El. pašto tvirtinimai išmokų paskyrimui | Ši funkcija pateiks parinktį, kuri siųs patvirtinimo el. laišką darbuotojams, kai jie išsiregistruoja iš išmokų paskyrimo patirčių darbuotojo savitarnos paslaugose. Dėl daugiau informacijos, žr. [Konfigūruoti išmokų valdymo parametrus bendrovei](hr-benefits-setup-parameters-per-company.md). |
| Vadovo įvesti įgūdžiai savo darbuotojams gali būti automatiškai patvirtinami darbo eigos | Greitai bus išleista. |

Norėdami gauti visą planuojamų funkcijų ir jų suplanuotų leidimų sąrašą, žr. [„Dynamics 365 Human Resources” 2020 m. 2-os leidimo bangos apžvalga](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Terminologijos naujinimai „Microsoft Dataverse“

Įsigalioja nuo lapkričio mėn. 2020, „Common Data Service“ buvo pervardytas į [„Microsoft Dataverse“](/powerapps/maker/data-platform/data-platform-intro). Žr. [oficialų skelbimą](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) „Power Apps“ tinklaraštyje, kad sužinotumėte daugiau. Kartu su pavadinimu, kai kurie terminai „Dataverse“ buvo atnaujinti. Pavyzdžiui, nuo šiol *objektas* yra *lentelė* ir *laukas* yra *stulpelis*. Daugiau informacijos rasite skyriuje [Terminijos naujinimai](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Šiame leidime terminai susiję su „Dynamics 365 Human Resources“ integravimu su „Dataverse“ buvo atnaujinti per programą, kad atspindėtų šiuos pakeitimus. Pavyzdžiui, **„Common Data Service“ integravimas** forma dabar yra **„Microsoft Dataverse“ integravimas**.

Tam, kad sužinotumėte daugiau apie „Dynamics 365 Human Resources“ integravimą su „Microsoft Dataverse“, žr. [Konfigūruoti „Microsoft Dataverse“ integravimą](./hr-admin-integration-common-data-service.md) ir [Konfigūruoti „Microsoft Dataverse“ virtualias lenteles](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2020 m. leidimo 2 bangos apžvalga](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]