---
title: Kas naujo ar pasikeitusio „Dynamics 365 Human Resources“ 2021 m. sausio 28 d.
description: Šiame straipsnyje aprašomos priemonės, kurios yra naujos arba pakeistos "Microsoft Dynamics 365 Human Resources " 2021 m. sausio 28 d.
author: marcelbf
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 46bbda21c3eb2b32030b93afc2a40785c22b124e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909765"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-28-2021"></a>Kas naujo ar pasikeitusio „Dynamics 365 Human Resources“ 2021 m. sausio 28 d.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomos priemonės, kurios yra naujos, pakeistos arba tuoj pat Dynamics 365 Human Resources.

Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2021 m. 1-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.3906 komponavimo versijai.

### <a name="new-features"></a>Naujos funkcijos

Šiame leidime bendrai prieinamos toliau pateiktos funkcijos.

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Integruoti išmokų priežasties kodus į **Personalo valdymo** darbo sritį | -- | [Nustatyti priežasčių kodus](hr-benefits-setup-reason-codes.md) |

### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šį straipsnį, kad būtų įtrauktos pataisos, kurios buvo sukurtas po to, kai buvo publikuotas šis straipsnis.


| Problemos numeris | Problema |  Aprašymas |
| --- | --- | --- |
| 539456 | Kalendorius rodo atostogų tipus pasviru tekstu, kai **Rodyti tik nebuvimą be išsamios informacijos** parametras įjungtas. | Kai **Rodyti tik nebuvimą be išsamios informacijos** parinktis yra įjungta, užklausos data dabar rodoma pasviru tekstu. |
| 528907 | Prieigos suteikimas juridiniam asmeniui darbuotojo vaidmenio rezultatuose vadovams negali leisti matyti atostogų balanso veiklos darbuotojams **Mano komandos** srityje darbuotojo savitarnos paslaugose. |Nustatydami šią parinktį dabar vadovai gali ir toliau matyti atostogų balanso veiklą. |
| 526280 | Leidimų klaida HcmWorkerEntity, HcmEmployeeEntity ir HcmContractorEntity. | Vartotojai ne sistemos administratoriaus vaidmenyje negalėjo eksportuoti objektų įvardytų dėl leidimo klaidos NationalityCountryRegion laukelyje. Vartotojams ir toliau reikės tolesnių teisių, kad jie eksportuotų šią informaciją: HcmWorkerEntityMaintain, HcmWorkerEntityView, HcmEmployeeEntityMaintain, HcmEmployeeEntityMaintain, HcmEmployeeEntityView, HcmContractorEntityMaintain ir HCMContractorEntityView. |
| 542147 | **Banko sąskaitos numeris** ir **Maršruto numeris** laukeliai yra privalomi įtraukiant banko sąskaitą per darbuotojo savitarnos paslaugas. | Dabar ištaisėme klaidą, kai darbuotojai privalėjo įvesti **Banko sąskaitos numeris** ir **Maršruto numeris** laukelius įtraukdami banko sąskaitos išsamią informaciją. Šie laukeliai nebėrą privalomi įrašant naują banko sąskaitos informaciją. |
| 543641 | ZIP kodas nėra užpildomas elektroninės ataskaitos metu. | Ištaisyta klaida, kai ZIP kodas neužpildomas ACA ataskaitoje skirtoje apimti kodus nuo L iki Q. |
| 545402 | Įtraukti maršruto keitimą UserBranding.js faile siekiant pašalinti 404 klaidas. | Vartotojas nebematys 404 klaidų konsolėje. |

## <a name="in-preview"></a>Peržiūros režimu   

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie funkcijų įjungimą ir išjungimą žr. [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| „Human Resources“ programa, esanti „Microsoft Teams” | [Darbuotojo atostogos ir neatvykimai „Microsoft Teams”](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [„Human Resources“ programa „Teams“](./hr-admin-teams-leave-app.md)<br>[Atostogų prašymų valdymas „Teams“](hr-teams-leave-app.md) |
| Kryžminės įmonės rodinys atostogų vadovams | [Kryžminės įmonės rodinys darbuotojų atostogų vadovams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Atostogų ir neatvykimų parametrų konfigūravimas](./hr-leave-and-absence-parameters.md) |

## <a name="coming-soon"></a>Jau greitai

| Funkcija | Išsamiai |
| --- | --- |
| El. pašto tvirtinimai išmokų paskyrimui | Ši funkcija pateiks parinktį, kuri siųs patvirtinimo el. laišką darbuotojams, kai jie išsiregistruoja iš išmokų paskyrimo patirčių darbuotojo savitarnos paslaugose. Ši funkcija bus prieinama nuo vasario 1 d. Dėl daugiau informacijos, žr. [Konfigūruoti išmokų valdymo parametrus bendrovei](hr-benefits-setup-parameters-per-company.md). |
| Vadovo įvesti įgūdžiai savo darbuotojams gali būti automatiškai patvirtinami darbo eigos | Greitai bus išleista. |

Norėdami gauti visą planuojamų funkcijų ir jų suplanuotų leidimų sąrašą, žr. [„Dynamics 365 Human Resources” 2021 m. 1-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Terminologijos naujinimai „Microsoft Dataverse“

Įsigalioja nuo lapkričio mėn. 2020, „Common Data Service“ buvo pervardytas į [„Microsoft Dataverse“](/powerapps/maker/data-platform/data-platform-intro). Žr. [oficialų skelbimą](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) „Power Apps“ tinklaraštyje, kad sužinotumėte daugiau. Kartu su pavadinimu, kai kurie terminai „Dataverse“ buvo atnaujinti. Pavyzdžiui, nuo šiol *objektas* yra *lentelė* ir *laukas* yra *stulpelis*. Daugiau informacijos rasite skyriuje [Terminijos naujinimai](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Šiame leidime terminai susiję su „Dynamics 365 Human Resources“ integravimu su „Dataverse“ buvo atnaujinti per programą, kad atspindėtų šiuos pakeitimus. Pavyzdžiui, **„Common Data Service“ integravimas** forma dabar yra **„Microsoft Dataverse“ integravimas**.

Tam, kad sužinotumėte daugiau apie „Dynamics 365 Human Resources“ integravimą su „Microsoft Dataverse“, žr. [Konfigūruoti „Microsoft Dataverse“ integravimą](./hr-admin-integration-common-data-service.md) ir [Konfigūruoti „Microsoft Dataverse“ virtualias lenteles](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2021 m. leidimo 1 bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]