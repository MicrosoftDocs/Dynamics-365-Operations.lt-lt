---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ 2021 m. kovo 8 d.
description: Šiame straipsnyje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2021 m. kovo 8 d.
author: marcelbf
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9280e85f9701573717c4115b4d752ed11be4862e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868074"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-08-2021"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ 2021 m. kovo 8 d.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomos priemonės, kurios yra naujos, pakeistos arba tuoj pat Dynamics 365 Human Resources.

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
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šį straipsnį, kad būtų įtrauktos pataisos, kurios buvo sukurtas po to, kai buvo publikuotas šis straipsnis.

| Problemos numeris | Problema |  Aprašymas |
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