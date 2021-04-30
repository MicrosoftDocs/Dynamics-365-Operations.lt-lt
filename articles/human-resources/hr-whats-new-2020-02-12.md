---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. vasario 12 d.)
description: Šiame straipsnyje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. vasario 12 d.
author: andreabichsel
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0d5991f23723056d7ee766c00ed0f4ee16ff0f85
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890939"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-12-2020"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. vasario 12 d.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šiame straipsnyje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources“ funkcijos. Pakeitimai taikomi 8.1.2867 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo palaikymo numerius „Microsoft Dynamics Lifecycle Services“ (LCS).

## <a name="existing-entities-compfixedempls-and-hcmpersonimage-should-be-accessible-from-odata-414178"></a>Esami objektai CompFixedEmpls ir HcmPersonImage turi būti pasiekiami naudojant „OData“ (414178)

Nuo šios savaitės leidimo objektai **CompFixedEmpls** ir **HcmPersonImage** dabar yra vieši ir pasiekiami naudojant „OData“.

## <a name="delete-employment-from-dataverse-doesnt-work-when-employment-details-arent-active-403193"></a>Kai įdarbinimo informacija nėra aktyvi, negalima panaikinti įdarbinimo iš „Dataverse“ (403193)

Atlikus šį pakeitimą, dabar galima panaikinti įdarbinimą naudojant „Dataverse“, kai įdarbinimo informacija nėra aktyvi.

## <a name="course-registration-workflow-changes-status-to-complete-and-errors-after-second-approval-409749"></a>Kursų registracijos darbo eigos būsena pasikeičia į baigtą ir po antro patvirtinimo pateikiamos klaidos (409749)

Kursų registracijos darbo eiga atnaujinta, kad būtų palaikomi keli tvirtintojai.

## <a name="in-preview"></a>Peržiūros režimu

Šios peržiūros funkcijos bus pasiekiamos nuo 2020 m. vasario 3 d.

- **Atostogų ir neatvykimų peržiūros funkcijos** – daugiau informacijos žr. skyrių [Atostogų ir neatvykimų peržiūros funkcijos](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Išmokų valdymo peržiūros funkcija** – norėdami gauti daugiau informacijos, įskaitant žinomas problemas, žr. skyrių [Išmokų valdymo peržiūra](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Jau greitai

### <a name="platform-update-32"></a>Platformos „update 32“ 

„Platform update 32“ bus pasiekiamas artimiausiu metu. [Čia rasite daugiau informacijos apie „Platform update 32“](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md).

### <a name="updated-dataverse-solution"></a>„Dataverse“ sprendimo naujinimas

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

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]