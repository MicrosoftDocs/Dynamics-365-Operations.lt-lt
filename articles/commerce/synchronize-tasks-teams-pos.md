---
title: Užduočių valdymo sinchronizavimas tarp „Microsoft Teams” ir „Dynamics 365 Commerce” EKA
description: Šioje temoje aprašoma, kaip sinchronizuoti užduočių valdymą tarp „Microsoft Teams” ir „Dynamics 365 Commerce” elektroninio kasos aparato (EKA).
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 74d53a850113c83979fba6baa4ff3c3e5d9ca02d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020632"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>Užduočių valdymo sinchronizavimas tarp „Microsoft Teams” ir „Dynamics 365 Commerce” EKA

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip sinchronizuoti užduočių valdymą tarp „Microsoft Teams” ir „Dynamics 365 Commerce” elektroninio kasos aparato (EKA).

Vienas iš pagrindinių „Teams” integravimo tikslų yra užduočių sinchronizavimo tarp EKA programos ir „Teams” įgalinimas. Tokiu būdu parduotuvės darbuotojai užduotims valdyti gali naudoti tiek EKA programą, tiek „Teams”, ir jiems nereikia perjungti programų.

Kadangi planavimo priemonė yra naudojama kaip „Teams” užduočių saugykla, todėl turi būti saitas tarp „Teams” ir „Dynamics 365 Commerce”. Šis saitas nustatomas naudojant konkretų plano ID tam tikrai parduotuvės komandai.

Toliau pateiktose procedūrose rodoma, kaip nustatyti užduočių valdymo sinchronizavimą tarp EKA ir „Teams” programų.

## <a name="publish-a-test-task-list-in-teams"></a>Testavimo užduočių sąrašo publikavimas „Teams” platformoje

Toliau pateiktoje procedūroje laikoma, kad jūsų parduotuvių komandos naudoja „Microsoft Teams” užduočių valdymo integravimą su „Commerce” pirmą kartą.

Norėdami publikuoti testavimo užduočių sąrašą „Teams” platformoje, atlikite šiuos veiksmus.

1. Prisijunkite prie „Teams” kaip komunikacijos vadovas. Įprastai, komunikacijos vadovai yra vartotojai, turintys **Regiono vadovo** vaidmenį „Commerce” platformoje.
1. Kairiojoje naršymo srityje pasirinkite **Planavimo priemonės užduotys**.
1. Skirtuko **Publikuoti sąrašai** apatinėje kairėje dalyje pasirinkite **Naujas sąrašas** ir pavadinkite jį **Testavimo užduočių sąrašu**.
1. Pasirinkite **Kurti**. Naujas sąrašas rodomas dalyje **Juodraščiai**.
1. Prie **Užduoties pavadinimo** suteikite pirmajai užduočiai pavadinimą **„Teams” integravimo testavimas**. Tada pasirinkite **Įvesti**.
1. Sąraše **Juodraščiai** pasirinkite užduočių sąrašą. Tada viršutiniame dešiniajame kampe pasirinkite  **Publikuoti** .
1. Dialogo lange **Pasirinkti, kam publikuoti** pažymėkite komandas, kurios turėtų gauti testavimo užduočių sąrašą.
1. Pasirinkite **Pirmyn**, norėdami peržiūrėti savo publikavimo planą. Jei turite atlikti pakeitimus, pasirinkite  **Atgal**. 
1. Pasirinkite **Patvirtinti, kad tęsiate**, o tada pasirinkite **Publikuoti**.
1. Užbaigus publikavimą, skirtuko **Publikuoti sąrašai** viršuje esantis pranešimas nurodo, ar jūsų užduočių sąrašas buvo sėkmingai pristatytas.

Daugiau informacijos rasite [Užduočių sąrašų publikavimas jūsų organizacijos darbo kūrimui ir sekimui](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).

## <a name="link-pos-and-teams-for-task-management"></a>EKA ir „Teams” susiejimas užduotims valdyti

Norėdami susieti EKA ir „Microsoft Teams” programas, skirtas užduočių valdymui „Commerce” būstinėje, atlikite šiuos veiksmus.

1. Eikite į **Mažmeninė prekyba ir komercija \> Užduočių valdymas \> Užduočių integravimas su „Microsoft Teams”**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Nustatykite parinktį **Įgalinti užduočių valdymo integravimą** į **Taip**.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Veiksmų srityje pasirinkite **Užduočių valdymo nustatymas**. Turėtumėte gauti pranešimą, nurodantį, kad kuriama paketinė užduotis pavadinimu **„Teams” parengimas**.
1. Eikite į **Sistemos administravimas \> Užklausos \> Paketinės užduotys** ir suraskite naujausią užduotį, kurios aprašymas yra **Komandų parengimas**. Palaukite tol, kol ši užduotis bus baigta.
1. Vykdykite **CDX užduotį 1070**, kad publikuotumėte plano ID ir parduotuvės nuorodas į „Retail Server”.

## <a name="additional-resources"></a>Papildomi ištekliai

[„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga](commerce-teams-integration.md)

[„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo įgalinimas](enable-teams-integration.md)

[„Microsoft Teams” parengimas iš „Dynamics 365 Commerce”](provision-teams-from-commerce.md)

[Vartotojų vaidmenų tvarkymas Microsoft Teams” platformoje](manage-user-roles-teams.md)

[Susiekite parduotuves ir komandas, jeigu yra išankstinių komandų „Microsoft Teams” platformoje](map-stores-existing-teams.md)

[„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo DUK](teams-integration-faq.md)
