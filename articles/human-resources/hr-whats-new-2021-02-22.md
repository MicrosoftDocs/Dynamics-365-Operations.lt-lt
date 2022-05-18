---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2021 m. vasario 22 d.)
description: Šioje temoje aprašomos funkcijos, kurios yra naujos ar pasikeitusios „Microsoft Dynamics 365 Human Resources“ 2021 m. vasario 22 d.
author: marcelbf
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c0f854908f4c4bb76604665701c97724351b0120
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686889"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-22-2021"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2021 m. vasario 22 d.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomos naujos, pasikeitusios ar netrukus pasirodysiančios „Dynamics 365 Human Resources“ funkcijos.

Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2021 m. 1-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.3988 komponavimo versijai.

### <a name="new-features"></a>Naujos funkcijos

Šiame leidime bendrai prieinamos toliau pateiktos funkcijos.

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| „Dynamics 365 Human Resources“ programa, skirta „Microsoft Teams“ | [Darbuotojo atostogos ir neatvykimai „Microsoft Teams”](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [„Human Resources“ programa „Teams“](./hr-admin-teams-leave-app.md)<br>[Atostogų prašymų valdymas „Teams“](hr-teams-leave-app.md) |

### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šią temą, kad būtų įtraukti klaidų ištaisymai, įtraukti į komponavimo versiją publikavus šią temą.

| Problemos numeris | Išdavimas |  aprašymas |
| --- | --- | --- |
| 529994 | Modifikuojant laukelį **Žinoma kaip** formoje **Darbuotojas** neįjungiamas „Dataverse“ naujinimas | Ištaisyta klaida, kai „Dataverse“ neatsinaujino, kai laukelis **Žinoma kaip** nebuvo atnaujintas formoje **Darbuotojas**. |
| 532651 | Kompensavimo analizės PBI ataskaita nenaudoja valiutos konvertavimo, skaičiuojant visos įmonės metriką | Ištaisyta klaida, dėl kurios kompensavimo analizės PBI ataskaita neteisingai atliko valiutos konvertavimą. |
| 552226 | Gyvenimo įvykio apdorojimas uždaro ir iš naujo atidaro planus kelis kartus vienkartiniam gyvenimo įvykiui  | Sutvarkyta problema, kai darbuotojas yra keliuose juridiniuose subjektuose ir įvyksta gyvenimo įvykis, o gyvenimo įvykio įrašas generuojamas kiekvienam juridiniam subjektui, kuriame yra darbuotojas. Kai apdorojami galiojimo įvykiai, būtina pasirinkti juridinį subjektą, kuris bus apdorojamas. Tačiau apdorojimo logika neturi apribojimo šiam juridiniam subjektui. Vietoje to jis apdoroja visus juridinius subjektus ir uždaro bei iš naujo atidaro pasirinkto juridinio subjekto planus. Šis veiksmas yra gyvenimo įvykis, kurį reikia kelis kartus apdoroti tame pačiame juridiniame subjekte; dėl to kelis kartus kiekvienas gyvenimo įvykio paveiktas planas uždaromas ir iš naujo atidaromas. |
| 518064 | Tinkamuose planuose pasirinktas tik vienas priklausomasis, kai daugiau nei vienas yra pažymėtas kaip numatytasis gavėjas | Ištaisyta problema, kai keli numatytieji gavėjai automatiškai nepasirenkami tinkamuose planuose. Dabar kontaktiniam asmeniui taip pat galite paskirti pirminį gavėją. Pirminis gavėjas, kai yra keli gavėjai, tinkamuose planuose yra nurodytas kaip 100 %. |
| 552365 | Atnaujinus programos 40 „Platform“ naujinimą nepavyko perkelti savo duomenų bazės (BYOD) eksportavimo užduočių | Ištaisyta problema, kai BYOD nepavyko eksportuoti po to, kai 40 „Platform“ atnaujinimas buvo pritaikytas aplinkoje. |
| 547123 | Užduočių, kurioms užklausa buvo siųsta ataskaitų srities užduočių sąraše, skaičiaus ribojimas | Užduočių sąraše rodomų užduočių skaičius yra ribojamas iki 15, kad išspręstų efektyvumo problemą, kurią lemia bandomų įkelti užduočių skaičiaus perviršį. |

## <a name="in-preview"></a>Peržiūros režimu

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie funkcijų įjungimą ir išjungimą žr. [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Kryžminės įmonės rodinys atostogų vadovams | [Kryžminės įmonės rodinys darbuotojų atostogų vadovams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Atostogų ir neatvykimų parametrų konfigūravimas](./hr-leave-and-absence-parameters.md) |
| Išmokų valdymo darbo sritis | [Išmokų valdymo darbo sritis (peržiūra)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Išmokų valdymo darbo sritis](hr-benefits-management-workspace.md) |
| Apribokite darbuotojų galimybes redaguoti įmonės kontaktinius duomenis | [Darbuotojų galimybių redaguoti įmonės kontaktinius duomenis ribojimas](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Asmeninės informacijos redagavimo apribojimas](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Jau greitai

| Funkcija | Išsamiai |
| --- | --- |
| Vadovo įvesti įgūdžiai savo darbuotojams gali būti automatiškai patvirtinami darbo eigos | Greitai bus išleista. |

Norėdami gauti visą planuojamų funkcijų ir jų suplanuotų leidimų sąrašą, žr. [„Dynamics 365 Human Resources” 2021 m. 1-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Terminologijos naujinimai „Microsoft Dataverse“

Įsigalioja nuo lapkričio mėn. 2020, „Common Data Service“ buvo pervardytas į [„Microsoft Dataverse“](/powerapps/maker/data-platform/data-platform-intro). Žr. [oficialų skelbimą](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) „Power Apps“ tinklaraštyje, kad sužinotumėte daugiau. Pakeitus šį pavadinimą, kai kurie terminai „Dataverse“ buvo atnaujinti. Pavyzdžiui, nuo šiol *objektas* yra *lentelė* ir *laukas* yra *stulpelis*. Daugiau informacijos rasite skyriuje [Terminijos naujinimai](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Šiame leidime terminai susiję su „Dynamics 365 Human Resources“ integravimu su „Dataverse“ buvo atnaujinti per programą, kad atspindėtų šiuos pakeitimus. Pavyzdžiui, **„Common Data Service“ integravimas** forma dabar yra **„Microsoft Dataverse“ integravimas**.

Tam, kad sužinotumėte daugiau apie „Dynamics 365 Human Resources“ integravimą su „Microsoft Dataverse“, žr. [Konfigūruoti „Microsoft Dataverse“ integravimą](./hr-admin-integration-common-data-service.md) ir [Konfigūruoti „Microsoft Dataverse“ virtualias lenteles](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="updates-to-service-deployment"></a>Tarnybos diegimo naujinimai

Nuo 2021 m. vasario 22 d. leidimo koreguojame savo regiono tarnybos naujinimo diegimą. Atlikus koregavimus bus keičiama tvarka, kuria visuotiniai regionai gaus personalo paslaugos naujinimus ir modifikacijas laukimo tarp naujinimo etapų laikotarpiu. Šie pokyčiai atitinka saugaus diegimo praktiką (SDP), siekiant pagerinti aptarnavimo stabilumą, kokybę ir palaikymo galimybes.

Toliau seksime dviejų savaičių diegimo intervalą. Tačiau klientai gali pastebėti, kad naujinimai dažniausiai taikomi jų personalo aplinkai kitą dviejų savaičių ciklo dieną, nei ankstesniuose leidimuose.

Daugiau informacijos apie paslaugos atnaujinimo procesą žr. skyriuje [Atnaujinimo procesas](./hr-admin-setup-update-process.md).

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2021 m. leidimo 1 bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]