---
title: Užduočių valdymo sinchronizavimas tarp „Microsoft Teams” ir „Dynamics 365 Commerce” EKA
description: Šiame straipsnyje aprašoma, kaip sinchronizuoti užduočių valdymą tarp ir point Microsoft Teams Dynamics 365 Commerce sale (EKA).
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f339ae031f11ad850dab47f84bc9823cf6776e74
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746103"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>Užduočių valdymo sinchronizavimas tarp „Microsoft Teams” ir „Dynamics 365 Commerce” EKA

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip sinchronizuoti užduočių valdymą tarp ir point Microsoft Teams Dynamics 365 Commerce sale (EKA).

Vienas iš pagrindinių „Teams” integravimo tikslų yra užduočių sinchronizavimo tarp EKA programos ir „Teams” įgalinimas. Tokiu būdu parduotuvės darbuotojai užduotims valdyti gali naudoti tiek EKA programą, tiek „Teams”, ir jiems nereikia perjungti programų.

Kadangi planavimo priemonė yra naudojama kaip „Teams” užduočių saugykla, todėl turi būti saitas tarp „Teams” ir „Dynamics 365 Commerce”. Šis saitas nustatomas naudojant konkretų plano ID tam tikrai parduotuvės komandai.

Toliau pateiktose procedūrose rodoma, kaip nustatyti užduočių valdymo sinchronizavimą tarp EKA ir „Teams” programų.

## <a name="link-pos-and-teams-for-task-management"></a>EKA ir „Teams” susiejimas užduotims valdyti

Norėdami susieti EKA ir „Microsoft Teams” programas, skirtas užduočių valdymui „Commerce” būstinėje, atlikite šiuos veiksmus.

> [!NOTE]
> Prieš bandydami integruoti užduočių valdymą su komandomis, įsitikinkite, kad įgalinote ir integruojate [Dynamics 365 Commerce Microsoft Teams](enable-teams-integration.md). 

1. Eikite į **Mažmeninė prekyba ir komercija \> Užduočių valdymas \> Užduočių integravimas su „Microsoft Teams”**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Nustatykite parinktį **Įgalinti užduočių valdymo integravimą** į **Taip**.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Veiksmų srityje pasirinkite **Užduočių valdymo nustatymas**. Turėtumėte gauti pranešimą, nurodantį, kad kuriamos paketinės užduoties, pavadintos **Komandų** atidėjimas.
1. Eikite į **Sistemos administravimas \> Užklausos \> Paketinės užduotys** ir suraskite naujausią užduotį, kurios aprašymas yra **Komandų parengimas**. Palaukite, kol užduotis bus baigta.
1. Vykdykite **CDX užduotį 1070**, kad publikuotumėte plano ID ir parduotuvės nuorodas į „Retail Server”.

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

> [!NOTE]
> Sėkmingai publikuous užduočių sąrašą komandose, užduotys bus rodomos EKA. Tada EKA vadybininkai ir kasininkai turės įjungti EKA Azure AD prisijungimą. Norėdami gauti daugiau informacijos, žr. straipsnį [Įgalinti Azure Active Directory EKA prisijungimo autentifikavimą](aad-pos-logon.md). 

## <a name="additional-resources"></a>Papildomi ištekliai

[„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga](commerce-teams-integration.md)

[„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo įgalinimas](enable-teams-integration.md)

[„Microsoft Teams” parengimas iš „Dynamics 365 Commerce”](provision-teams-from-commerce.md)

[Vartotojų vaidmenų tvarkymas Microsoft Teams” platformoje](manage-user-roles-teams.md)

[Susiekite parduotuves ir komandas, jeigu yra išankstinių komandų „Microsoft Teams” platformoje](map-stores-existing-teams.md)

[„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo DUK](teams-integration-faq.md)
