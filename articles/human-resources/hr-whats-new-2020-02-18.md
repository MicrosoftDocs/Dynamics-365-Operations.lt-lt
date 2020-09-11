---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. vasario 18 d.)
description: Šiame straipsnyje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. vasario 18 d.
author: Darinkramer
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5e9e1f05de682b4fe29ec23f06099b2968ebe3df
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/20/2020
ms.locfileid: "3711993"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. vasario 18 d.)

Šiame straipsnyje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources“ funkcijos. Pakeitimai taikomi 8.1.2903 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo LCS palaikymo numerius informaciniais tikslais.

## <a name="platform-update-32"></a>Platformos „update 32“ 

Dabar pasiekiamas 32-asis platformos naujinimas. Norėdami gauti daugiau informacijos, žr. [Kas nauja arba pakeista „Finance and Operations“ 32-ajame platformos naujinime (2020 m. vasario mėn.)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a>Keičiant rodinio parinktis supaprastintoje darbuotojo formoje, įsimenamos ieškos reikšmės (383833)

Naujoji forma **Darbininkas** dabar įsimena ieškos reikšmes, kai keičiate rodinio parinktis ir taikote keitimus.

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a>Naudojant peržiūros funkciją kompensavimo valdymo suvestinės plytelės peradresuoja į klaidingą formą (401861)

Naujojoje formoje **Darbininkas** esančiose pastoviosios ir kintamosios kompensacijos valdymo plytelėse dabar rodomi teisingi įrašai. Taikoma tik supaprastintos darbuotojo formos peržiūros funkcijai. Šią peržiūros funkciją galite įjungti srityje **Funkcijų valdymas**. Norėdami gauti daugiau informacijos, žr. [Funkcijų valdymas](hr-admin-manage-features.md).

## <a name="empty-status-field-for-some-leave-request-records-in-common-data-service-414915"></a>Tuščias kai kurių „Common Data Service“ prašymo išeiti atostogų įrašų laukas Būsena (414915)

Šiuo keitimu ištaisoma „Common Data Service“ problema, kai prašymo išeiti atostogų laukas **Būsena** nustatomas kaip **Peržiūra**. „Common Data Service“ dabar būsena rodoma.

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a>Įgūdžių trūkumo analizė galima tik priskirtai užduočiai (411390)

Dabar įgūdžių trūkumų analizę galite atlikti bet kuriai užduočiai, nustatytai sprendime „Human Resources“.

## <a name="system-currency-doesnt-sync-from-common-data-service-to-human-resources-in-new-environments-418011"></a>Naujose aplinkose sistemos valiuta nesinchronizuojama iš „Common Data Service“ su „Human Resources“ (418011)

„Common Data Service“ sistemos valiuta dabar gali būti sinchronizuojama su „Human Resources“.

## <a name="in-preview"></a>Peržiūros režimu

- [Atostogų ir neatvykimų peržiūros funkcijos](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [Išmokų valdymo peržiūros funkcijos](hr-benefits-management-overview.md)

## <a name="coming-soon"></a>Jau greitai

### <a name="updated-common-data-service-solution"></a>Atnaujintas „Common Data Service“ sprendimas

Nauju „Common Data Service” sprendimu greitai galėsite naudotis atlikdami šiuos keitimus:

| Aprašymas | Keitimas |
| ----------------------------------------- | --- |
| Objekto **Užduotis / pareigos** keitimai | Pridėta **Kompensacijos sritis**</br>Pridėta **Finansinės dimensijos** |
| Objekto **Darbininkas** keitimai | Pridėta **Pavadinimų seka**</br>Pridėta **Dirba iš namų**</br>Pridėta **Kalba**</br>Pridėta **Paaukštinimo data**</br>Pridėta **Jubiliejaus data**</br>Pridėta **Pradinio įdarbinimo data** |
| Objekto **Įdarbinimas** keitimai | Pridėta **Finansinės dimensijos**</br>Pridėta **Atleidimo priežastis**</br>**Perėjimo data** pervardyta į **Atleidimo data**</br>Pridėta **Bandomojo laikotarpio data** |
| Objekto **Darbininko adresas** keitimai | Pridėta **Gatvė**</br>**1 adreso eilutė**, **2 adreso eilutė**ir **3 adreso eilutė** pažymėtos kaip nebenaudojamos |
| Nauji kintamosios atlyginimo dalies sąrankos objektai | **Kompensacijų kitimo plano tipas**</br>**Kompensacijų kitimo planas**</br>**Kintamosios atlyginimo dalies paskirstymo taisyklės**</br>**Kompensacijų kitimo plano lygis** |
| Naujas objektas **Darbuotojo įdarbinimo kalendorius** | Pridėta **Darbo kalendoriaus objektas** |
| Naujas objektas **Algalapio pareigų informacija** | Pridėta **Algalapio pareigų informacija** |
| Naujas subjektas **Pavadinimas** | Pridėtas **Pavadinimas**. Į „Human Resources“ ir „Common Data Service“ sinchronizavimo procesą bus įtrauktas naujas objektas **Pavadinimas**. Jis iš pradžių nebus nurodomas iš objektų **Pareigos** ar **Darbas**. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)