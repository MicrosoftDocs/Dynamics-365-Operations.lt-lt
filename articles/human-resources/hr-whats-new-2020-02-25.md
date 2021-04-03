---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. vasario 25 d.)
description: Šiame straipsnyje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. vasario 25 d.
author: andreabichsel
manager: tfehr
ms.date: 02/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5048c94543d0ee35bbc0f210a86a5d58ae901510
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463771"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. vasario 25 d.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šiame straipsnyje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources“ funkcijos. Pakeitimai taikomi 8.1.2927 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo LCS palaikymo numerius informaciniais tikslais.

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a>Atvejų valdymo naršymo ir duomenų valdymo sistemos (DMF) objekto (414754) įjungimas

Ši peržiūros funkcija įjungia papildomas atvejų valdymo naršymo galimybes. Šią peržiūros funkciją galite įjungti darbo srityje **Funkcijų valdymas**. Šie meniu elementai rodomi programos Dynamics 365 Human Resources darbo srityje **Atitiktis**. Atlikus šį pakeitimą, „Human Resources“ gali pasiekti:

- Visi atvejai
- Mano atvejai
- Mano atviri atvejai
- Mano vėluojantys atvejai
- Per darbo sritį man priskirti atvejai

Kartu su šiomis naujomis atvejų peržiūros galimybėmis taip pat galimas DMF objektas **Išsami informacija apie objektą**.

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a>Ryšių apibrėžimo įjungimas visuotinėje adresų knygelėje (414762)

Visuotinėje adresų knygelėje ryšiai dabar yra įjungti. Iki šios savaitės versijos pasirodymo informaciniame skydelyje **Ryšys** buvo rodomi bet kokie sistemos nustatyti ryšiai. Dabar galite apibrėžti šiuos ryšius visuotinės adresų knygelės puslapyje.

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a>Pareigas galima pašalinti, kai egzistuoja tų pareigų aktyvūs kompensacijos įrašai (414568)

Atlikus šį pakeitimą, nuo šiol, kai bandysite pašalinti pareigas ir darbuotojas turės aktyvų tos pačios kompensacijos įrašą, pasirodys įspėjimas. Taip nutikus, turite atnaujinti darbuotojo pastoviosios atlyginimo dalies įrašą, prieš pašalindami pareigas.

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a>Našumo peržiūros darbo eiga retkarčiais įtraukia išsiregistravimus tų žmonių, kurie nėra proceso dalis (414171)

Šis pakeitimas pataiso problemą, kai prie našumo peržiūros pridedami papildomi išsiregistravimo dalyviai.

## <a name="worker-position-assignment-not-created-in-dataverse-when-selected-on-the-new-worker-dialog-413479"></a>Darbuotojo pareigų priskyrimas Dataverse nėra sukuriamas, kai pasirinktas naujo darbuotojo dialogo lange (413479)

Šis pakeitimas pataiso problemą, kai darbuotojas įdarbinamas ir į naujas pareigas paskiriamas per dialogo langą **Naujas darbuotojas**. Dabar pareigų priskyrimas atsispindi Dataverse.

## <a name="coming-soon"></a>Jau greitai

### <a name="updated-dataverse-solution"></a>Atnaujintas „Dataverse“ sprendimas

Nauju „Dataverse” sprendimu greitai galėsite naudotis atlikdami šiuos keitimus:

| Aprašymas | Keitimas |
| ----------------------------------------- | --- |
| Objekto **Užduotis / pareigos** keitimai | Pridėta **Kompensacijos sritis**</br>Pridėta **Finansinės dimensijos** |
| Objekto **Darbininkas** keitimai | Pridėta **Pavadinimų seka**</br>Pridėta **Dirba iš namų**</br>Pridėta **Kalba**</br>Pridėta **Paaukštinimo data**</br>Pridėta **Jubiliejaus data**</br>Pridėta **Pradinio įdarbinimo data** |
| Objekto **Įdarbinimas** keitimai | Pridėta **Finansinės dimensijos**</br>Pridėta **Atleidimo priežastis**</br>**Perėjimo data** pervardyta į **Atleidimo data**</br>Pridėta **Bandomojo laikotarpio data** |
| Objekto **Darbininko adresas** keitimai | Pridėta **Gatvė**</br>**1 adreso eilutė**, **2 adreso eilutė** ir **3 adreso eilutė** pažymėtos kaip nebenaudojamos |
| Nauji kintamosios atlyginimo dalies sąrankos objektai | **Kompensacijų kitimo plano tipas**</br>**Kompensacijų kitimo planas**</br>**Kintamosios atlyginimo dalies paskirstymo taisyklės**</br>**Kompensacijų kitimo plano lygis** |
| Naujas objektas **Darbuotojo įdarbinimo kalendorius** | Pridėta **Darbo kalendoriaus objektas** |
| Naujas objektas **Algalapio pareigų informacija** | Pridėta **Algalapio pareigų informacija** |
| Naujas subjektas **Pavadinimas** | Pridėtas **Pavadinimas**. Į „Human Resources“ ir „Dataverse“ sinchronizavimo procesą bus įtrauktas naujas objektas **Pavadinimas**. Jis iš pradžių nebus nurodomas iš objektų **Pareigos** ar **Darbas**. |

Per artimiausias kelias savaites šie objektų pakeitimai bus galimi visose aplinkose. Norėdami rankiniu būdu įdiegti naujausią Dataverse sprendimą, skirtą „Human Resources“:

1.  Eikite į [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).

2.  Pasirinkite **Aplinkos**.

3.  Raskite aplinką, kurią norite atnaujinti. Ji turėtų atitikti „Human Resources“ formoje **Apie** esančios sekcijos **Common Data Service informacija** reikšmę **Aplinkos pavadinimas**.

4.  Pasirinkite aplinką, kad peržiūrėtumėte detalią aplinkos informaciją.

5.  Veiksmo juostos viršuje pasirinkite **Valdyti sprendimus**. Atsidarys naujas naršyklės langas ir pereisite į **„Dynamics 365“ administravimo centrą** savo aplinkos kontekste.

6.  Sąraše **Sprendimas** pasirinkite **Dynamics 365 Human Resources fiksavimas**.

7.  Pasirinkite **Atnaujinti**, kad pritaikytumėte naujausią sprendimą.

## <a name="in-preview"></a>Peržiūros režimu

Šios peržiūros funkcijos tapo pasiekiamos nuo 2020 m. vasario 3 d.:

- **Atostogų ir neatvykimų peržiūros funkcijos** – daugiau informacijos žr. skyrių [Atostogų ir neatvykimų peržiūros funkcijos](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Išmokų valdymo peržiūros funkcija** – norėdami gauti daugiau informacijos, įskaitant žinomas problemas, žr. skyrių [Išmokų valdymo peržiūra](hr-benefits-management-overview.md).

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]