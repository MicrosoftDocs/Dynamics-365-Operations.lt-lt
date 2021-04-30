---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ 2021 m. kovo 8 d.
description: Šioje temoje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2021 m. kovo 8 d.
author: marcelbf
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 890d7a2e671d6365cd1f6e23e399166541c04496
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890632"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-08-2021"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ 2021 m. kovo 8 d.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomos naujos, pasikeitusios ar netrukus pasirodysiančios „Dynamics 365 Human Resources“ funkcijos.

Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2021 m. 1-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.4017 komponavimo versijai.

### <a name="new-features"></a>Naujos funkcijos

Šiame leidime bendrai prieinamos toliau pateiktos funkcijos.

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Kryžminės įmonės rodinys atostogų vadovams | [Kryžminės įmonės rodinys darbuotojų atostogų vadovams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Atostogų ir neatvykimų parametrų konfigūravimas](./hr-leave-and-absence-parameters.md) |

### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šią temą, kad būtų įtraukti klaidų ištaisymai, įtraukti į komponavimo versiją publikavus šią temą.

| Problemos numeris | Išdavimas |  aprašymas |
| --- | --- | --- |
| 486611 | Atostogų laikas rodomas atostogų kalendoriuje, kai įjungta funkcija **Išjungti atostogas visuose kalendoriuose** | Jei įjungta funkcija **Išjungti atostogas visuose kalendoriuose**, informacija apie atostogas neberodoma įjungus atostogų ir neatvykimų kalendoriaus patobulinimų funkciją.|
| 508972 | Atostogų ir neatvykimų banko operacijos objektui trūksta registracijos patikrinimo | Naudojant atostogų ir neatvykimo banko operacijos objektą, į planą netrauktų darbuotojų importuoti nebegalima. |
| 554854 | Atnaujinamas kalendorius įdarbinimo subjekto klaidose, jei numatytasis juridinis subjektas naudotojo parinktyse skiriasi | Jei norite atnaujinti darbuotojo kalendorių, naudodami įdarbinimo subjektą daugiau nieko nedarysite, jei numatytasis naudotojo parinkčių juridinis subjektas skiriasi. |
| 558347 | Įkeliant pradžios puslapį rodomas pranešimas „(Formos konfigūracijose FormRunConfiguration) negalima sukurti įrašo“. | Dėl suasmeninimų įkeliant pradžios puslapį rodomas klaidos pranešimas „(Formos konfigūracijose FormRunConfiguration) negalima sukurti įrašo“. |
| 557327 | Išmokų valdymo darbo sritis: virš tinklelio atsiranda tarpas. | Pataisyta naudotojo patirties problema, susijusi su nenumatytomis spragomis, rodomomis lentelės tinklelio ribose išmokų darbo srityje. |
| 557334 | Išmokų valdymo darbo sritis: parinkties **Laikotarpis** išskleidžiamasis langelis turėtų būti rodomas tik skirtuke **Suvestinė** | Parinkties **Laikotarpis** išskleidžiamasis laukelis dabar rodomas tik tada, kai išmokų darbo srityje aktyvus skirtukas **Suvestinė**, o ne skyriuose **Proceso rezultatai** ir **Nuorodos**. |
| 557336 | Išmokų valdymo darbo sritis: plytelių rodinyje tekstas **Atidaryti registraciją su patikrintais planais** yra sutrumpintas | Tekstas plytelių rodinyje pakeistas į **Patikrinti planai... atvira registracija**, siekiant išvengti būtino konteksto sutrumpinimo. |

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