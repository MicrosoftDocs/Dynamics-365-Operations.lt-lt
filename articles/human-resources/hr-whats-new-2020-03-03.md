---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. kovo 3 d.)
description: Šiame straipsnyje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. kovo 3 d.
author: Darinkramer
manager: AnnBe
ms.date: 03/03/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bf5b5ce9efbd2014164db213ff20d28d20ecf3e
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712309"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-3-2020"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. kovo 3 d.)

Šiame straipsnyje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources“ funkcijos. Pakeitimai taikomi 8.1.2955 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo LCS palaikymo numerius informaciniais tikslais.

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service sprendimas dabar galimas su šiais pakeitimais:

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

Per artimiausias kelias savaites šie objektų pakeitimai bus galimi visose aplinkose. Norėdami rankiniu būdu įdiegti naujausią Common Data Service sprendimą, skirtą „Human Resources“:

1.  Eikite į [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).

2.  Pasirinkite **Aplinkos**.

3.  Raskite aplinką, kurią norite atnaujinti. Aplinka turėtų atitikti „Human Resources“ formoje **Apie** esančios sekcijos **Common Data Service informacija** reikšmę **Aplinkos pavadinimas**.

4.  Pasirinkite aplinką, kad peržiūrėtumėte detalią aplinkos informaciją.

5.  Veiksmo juostos viršuje pasirinkite **Valdyti sprendimus**. Atsidarys naujas naršyklės langas ir pereisite į **„Dynamics 365“ administravimo centrą** savo aplinkos kontekste.

6.  Sąraše **Sprendimas** pasirinkite **Dynamics 365 Human Resources fiksavimas**.

7.  Pasirinkite **Atnaujinti**, kad pritaikytumėte naujausią sprendimą.

## <a name="import-issues-with-the-leave-enrollment-data-entity-406082"></a>Importavimo problemos, susijusios su atostogų registracijos duomenų objektu (406082)

Dabar darbuotoją galite užregistruoti naujame to paties tipo atostogų plane, jei tik registracijos data yra vėlesnė nei pasibaigusi ankstesnio plano registracijos data.

## <a name="issue-with-exporting-contribution-rates-in-the-401k-payrollworkerenrolledbenefitdetail-entity-in-dmf-420700"></a>Problema, kilusi dėl kontribucijos koeficientų objekte 401k payrollWorkerEnrolledBenefitDetail entity, esančiame DMF (420700)

Šis pakeitimas pakoreguoja eksportavimo funkcijas, skirtas objektui **payrollWorkerEnrolledBenefitDetail**, kad būtų atitiktos dabartinės darbuotojo kontribucijos vertės.

## <a name="searching-in-the-streamlined-worker-form-causes-message-saying-person-field-must-be-filled-in-402525"></a>Atliekant iešką supaprastintoje darbuotojo formoje, pasirodo pranešimas, nurodantis, kad reikia užpildyti laukelį „Asmuo“ (402525)

Kai ieškote darbuotojo, daugiau nebegausite gauti pranešimų apie tai, kad turite užpildyti laukelį **Asmuo**.

## <a name="note-field-value-doesnt-render-on-the-add-more-skills-form-380134"></a>Pastabos lauko reikšmė neperteikiama formoje „Įtraukti daugiau įgūdžių“ (380134)

Šis pakeitimas ištaiso problemą, kylančią individualizuojant darbuotojų savitarnos formą **Įtraukti daugiau įgūdžių**.

## <a name="multiple-fixed-compensation-plans-dont-expire-when-transferring-employees-389466"></a>Keli pastoviųjų atlyginimo dalių planai nenustoja galioti perkeliant darbuotojus (389466)

Atlikus šį pakeitimą, visi senųjų pareigų aktyvūs įrašai apie pastoviąją atlyginimo dalį nustos galioti atėjus perėjimo datai.

## <a name="in-preview"></a>Peržiūros režimu

Šios peržiūros funkcijos tapo pasiekiamos nuo 2020 m. vasario 3 d.:

- **Atostogų ir neatvykimų peržiūros funkcijos** – daugiau informacijos žr. skyrių [Atostogų ir neatvykimų peržiūros funkcijos](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Išmokų valdymo peržiūros funkcija** – norėdami gauti daugiau informacijos, įskaitant žinomas problemas, žr. skyrių [Išmokų valdymo peržiūra](hr-benefits-management-overview.md).

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)