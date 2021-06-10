---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ 2021 m. kovo 22 d.
description: Šioje temoje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2021 m. kovo 22 d.
author: marcelbf
ms.date: 03/22/2021
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
ms.search.validFrom: 2021-03-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 383f4dcf315c46534cce93da469a8818f690c45c
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056497"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-22-2021"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ 2021 m. kovo 22 d.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomos naujos, pasikeitusios ar netrukus pasirodysiančios „Dynamics 365 Human Resources“ funkcijos.

Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2021 m. 1-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.4049 komponavimo versijai.

### <a name="new-features"></a>Naujos funkcijos

Šiame leidime bendrai prieinamos toliau pateiktos funkcijos.

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Parinktis, norint priversti atšaukimą ir iš naujo nustatyti įklijuotų paketinių užduočių (560976) | NA | [Iš naujo nustatyti įstrigusias paketines užduotis](./hr-admin-troubleshooting-batch-execution.md) |
| Smulkūs UX atnaujinimai, skirti naujam išmokų planui sukurti (419941) | NA | [Išmokų plano kūrimas](hr-benefits-plans-setup.md) |

### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šią temą, kad būtų įtraukti klaidų ištaisymai, įtraukti į komponavimo versiją publikavus šią temą.

| Problemos numeris | Išdavimas |  Aprašas |
| --- | --- | --- |
| 554239 | Objektų, susijusių su **lentele BusinessProcessTaskAssignment, našumo** patobulinimai | Pagerinti objektų, susijusių su lentele **BusinessProcessTaskAssignment, našumą, į lentelę** įtraukiant siūlomus indeksus. |
| 566061 | Pašalinti V2 objekto atsarginį kodą iš naktinės sinchronizavimo | Pašalinkite V2 atsarginį kodą, kad būtų galima sinchronizuoti „Dataverse“ naktį. Atsarginis sinchronizavimas nebereikalingas ir apsaugo filtruotus sinchronizavimus nuo darbo, kaip tikėtasi. Keitimas pagerina duomenų sinchronizavimo „Dataverse“ vientisumą. |
| 538024 | Darbuotojo išmokų planai > Pašalinti tikrinimo klaidą | Pastovi klaida šalinant išmokų plano išregistravimo parinktį darbuotojų išmokų formoje. |
| 557965 | **Išmokų** darbo sritis: **aktyvaus galiojimo įvykių** saitas visada turi būti matomas **skyriuje** Saitai | Fiksuota problema, kai aktyvių gyvenimo įvykių saitas buvo matomas saitų skyriuje, bet bandant naršyti įvyko klaida, jei nėra įgalintos **(peržiūros) išmokų valdymo darbo** **srities** **funkcijos**. Daugiau informacijos apie darbo srities įgalinimas žr. [Išmokų valdymo darbo srityje](hr-benefits-management-workspace.md). |
| 556672 | Nepavyko apdoroti atjungtų darbuotojų kaupimų, kai **supaprastinamas** darbuotojų įrašas funkcijų valdymas | Parinktis kaupti atostogas ir neatvykimo planus buvo įtraukta į Daugiau pasirinkčių darbuotojų darbo retrospektyvoje, kai supaprastinamas darbuotojo **įrašas** **funkcijų** **valdymas**. |
| 562656 | **SysRecordChangeLogValidTimeState meniu elementas turėtų būti įtrauktas į saugos teisę ir** **SystemExternalBasicMaintain saugos pareigos** plėtinį | Datų tvarkytuvo formose nebuvo **keitimų peržiūros mygtuko ne** sistemos administratoriaus vaidmenų. |
| 505989 | Gyvenimo įvykių apdorojimas: tinkamumo keitimas netinkamai apdorotas dėl naudojamos datos | Fiksuotas išdavimas, kai tinkamumo nustatymo pakeitimas buvo priklausomas nuo pareigų pradžios datos, o ne nuo dabartinių pareigų. |
| 562286 | Atleisti darbuotoją ir nebesiųsti kelių atnaujinimų „Dataverse“ | Kai darbuotojas atleistas, siunčiama daugiau nei viena atnaujinimo operacija, todėl yra du to „Dataverse“ paties pakeitimo atnaujinimo pranešimai. Tai gali sukelti keletą paleidiklių, „Power Automate“ jei eiga yra sukonfigūruota taip, kad paleis būtų suaktyvintas pagal veiksmą. |
| 527340 | „Unrepresentable DateTime" klaida rodoma atidarant atostogų ir neatvykimų registracijas | Renkantis atostogų ir neatvykimo registraciją, klaida neberodoma. |
| 561663 | Padidinti klasterio atidėjimo laukimo laiko intervalą | Pagerinti infrastruktūros stabilumą ir parengimą kartu su klasterio parengimo atnaujinimais. |
| 486129 | Negalima redaguoti pasirinktinių laukų **pareigose > Tvarkyti pakeitimus** | Išspręskite problemą, dėl kurios pasirinktinių laukų nepavyko redaguoti pareigų **skirtuke** Tvarkyti **keitimus**. |

## <a name="in-preview"></a>Peržiūros režimu

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie funkcijų įjungimą ir išjungimą žr. [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Išmokų valdymo darbo sritis | [Išmokų valdymo darbo sritis (peržiūra)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Išmokų valdymo darbo sritis](hr-benefits-management-workspace.md) |
| Apribokite darbuotojų galimybes redaguoti įmonės kontaktinius duomenis | [Darbuotojų galimybių redaguoti įmonės kontaktinius duomenis ribojimas](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Asmeninės informacijos redagavimo apribojimas](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Jau greitai

| Funkcija | Išsamiai |
| --- | --- |
| Vadovo įvesti įgūdžiai savo darbuotojams gali būti automatiškai patvirtinami darbo eigos | Greitai bus išleista. |

Norėdami gauti visą planuojamų funkcijų ir jų suplanuotų leidimų sąrašą, žr. [„Dynamics 365 Human Resources” 2021 m. 1-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2021 m. leidimo 1 bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]