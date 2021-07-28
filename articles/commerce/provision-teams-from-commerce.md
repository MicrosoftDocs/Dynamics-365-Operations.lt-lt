---
title: „Microsoft Teams” parengimas iš „Dynamics 365 Commerce”
description: Šioje temoje aprašoma, kaip parengti „Microsoft Teams” naudojant organizacinius duomenis iš „Dynamics 365 Commerce”.
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
ms.openlocfilehash: 39dabeb8bacc4ebc3376f53f15c7fb292c8d301c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352113"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a>„Microsoft Teams” parengimas iš „Dynamics 365 Commerce”

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip parengti „Microsoft Teams” naudojant organizacinius duomenis iš „Dynamics 365 Commerce”.

„Dynamics 365 Commerce” leidžia lengvai parengti „Teams”, jeigu ten dar nenustatėte komandų savo mažmeninės prekybos parduotuvėms. Pasinaudodami gerai apibrėžtą informacija iš „Commerce”, kurią norite naudoti „Teams”, galite padėti savo parduotuvės darbuotojams pradėti naudotis „Teams” platforma. Ši informacija apima organizacijos hierarchiją, parduotuvių pavadinimus, darbuotojų informaciją ir „Azure Active Directory” (Azure AD) abonementus. 

„Teams” parengimo procesas susideda iš dviejų pagrindinių žingsnių:

1. „Teams” platformoje sukurkite komandą kiekvienai mažmeninės prekybos parduotuvei ir kaip atitinkamos komandos narius įtraukite parduotuvės darbuotojus. Jeigu darbuotojas yra susietas su daugiau nei viena mažmeninės prekybos parduotuve, komandos narystė atspindės šį faktą. Užduočių publikavimui iš „Teams” palengvinimui bus sukurta komunikacijos komanda, kurios nariai bus regioniniai vadovai.
1. Įkelkite savo organizacijos hierarchiją iš „Commerce” į „Teams”.

## <a name="provision-teams-in-commerce-headquarters"></a>„Teams” parengimas „Commerce” būstinėje

Prieš parengdami „Microsoft Teams”, atlikite šias užduotis:

- Patvirtinkite, kad visi regiono vadovai yra komunikacijos vadovai.
- Patvirtinkite, kad kiekvieno parduotuvės vadovo ir darbininko „Azure” abonementas yra susietas su to vadovo arba darbininko darbuotojo įrašu „Commerce” būstinėje.

Norėdami parengti „Teams” platformą „Commerce“ būstinėje, atlikite nurodytus veiksmus.

1. Eikite į **Mažmeninė prekyba ir komercija \> Kanalų sąranka \> „Microsoft Teams” integravimo konfigūravimas**.
1. Veiksmų srityje pasirinkite **Komandų parengimas**. Sukuriama paketinė užduotis pavadinimu **Komandų parengimas**.
1. Eikite į **Sistemos administravimas \> Užklausos \> Paketinės užduotys** ir suraskite naujausią užduotį, kurios aprašymas yra **Komandų parengimas**. Palaukite tol, kol ši užduotis bus baigta.

> [!TIP]
> Jei nė vienas iš jūsų regiono vadovų, parduotuvių vadovų ir parduotuvės darbuotojų nėra susietas su „Teams” licencija, jūs galite gauti šį klaidos pranešimą: „Nepavyko nuskaityti vartotojui taikytinų Sku kategorijų.” Norėdami išspręsti šią problemą, veiksmų srityje pasirinkite **Sinchronizuoti komandas ir narius**.

<!-- ![Dynamics 365 Commerce - Teams integration configuration.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a>„Teams” parengimo patvirtinimas „Teams” administravimo centre

Norėdami patvirtinti „Microsoft Teams” parengimą „Microsoft Teams” administravimo centre, atlikite šiuos veiksmus.
    
1. Eikite į [„Teams” administravimo centrą](https://admin.teams.microsoft.com/) ir prisijunkite kaip jūsų el. prekybos nuomotojo administratorius.
1. Kairiojoje naršymo srityje pasirinkite **Komandos** jų išplėtimui ir tada pasirinkite **Tvarkyti komandas**.
1. Patvirtinkite, kad kiekvienai „Commerce” mažmeninės prekybos parduotuvei buvo sukurta viena komanda.
1. Pasirinkite komandą ir patvirtinkite, kad parduotuvės darbuotojai buvo įtraukti į ją kaip nariai.
1. Kairiojoje naršymo srityje pasirinkite **Vartotojai** ir patvirtinkite, kad visų parduotuvių visi darbuotojai buvo įtraukti kaip vartotojai.

Šioje iliustracijoje pateiktas „Teams” administravimo centro puslapio **Tvarkyti komandas** pavyzdys.

![„Teams” administravimo centro puslapio Tvarkyti komandas pavyzdys.](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a>Organizacijos hierarchijos įkėlimas iš „Commerce” į „Teams”
    
„Commerce” organizacijos hierarchija gali būti naudojama „Microsoft Teams” platformoje užduočių publikavimui visoms arba pasirinktoms parduotuvėms, naudojančioms tą pačią hierarchijos struktūrą.

Norėdami įkelti „Commerce“ organizacijos hierarchiją į „Teams”, atlikite tolesnius veiksmus.
    
1. „Commerce” būstinėje eikite į **Mažmeninė prekyba ir komercija \> Kanalo sąranka \> „Microsoft Teams” integravimo konfigūracija**.
1. Pasirinkite **Atsisiųsti tikslinę hierarchiją**, o tada pasirinkite **Mažmeninės prekybos parduotuvės pagal regioną** tam, kad atsisiųstumėte organizacijos hierarchijos kableliais atskirtų reikšmių (CSV) failą.
1. Įdiekite „Microsoft Teams PowerShell” modulį atlikdami skyriuje [„Microsoft Teams PowerShell” diegimas](/microsoftteams/teams-powershell-install) nurodytus veiksmus.
1. Kai gausite raginimą „Teams PowerShell” lange, prisijunkite naudodami savo nuomotojo „Azure AD” administratoriaus abonementą.
1. Atlikite skyriuje [Jūsų komandos tikslinės hierarchijos nustatymas](/microsoftteams/set-up-your-team-hierarchy) nurodytus veiksmus, kad įkeltumėte tikslinės hierarchijos CSV failą.

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a>Patikrinkite, ar organizacijos hierarchija buvo įkelta į „Teams”

Norėdami patikrinti, ar organizacijos hierarchija buvo įkelta į „Microsoft Teams”, atlikite šiuos veiksmus.

1. Prisijunkite prie „Teams” kaip komunikacijos vadovas.
1. Kairiojoje naršymo srityje pasirinkite **Planavimo priemonės užduotys**.
1. Skirtuke **Publikuoti sąrašai** sukurkite naują sąrašą, kuriame yra bandomųjų užduočių.
1. Pasirinkite **Publikuoti**. Organizacijos hierarchija turėtų atsirasti dialogo lange **Pasirinkti, kas turi publikuoti**, kaip parodyta toliau pateiktos iliustracijos pavyzdyje.

![Organizacijos hierarchijos pavyzdys dialogo lange „Pasirinkti, kam publikuoti”.](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga](commerce-teams-integration.md)

[„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo įgalinimas](enable-teams-integration.md)

[Užduočių valdymo sinchronizavimas tarp „Microsoft Teams” ir „Dynamics 365 Commerce” EKA](synchronize-tasks-teams-pos.md)

[Vartotojų vaidmenų tvarkymas Microsoft Teams” platformoje](manage-user-roles-teams.md)

[Susiekite parduotuves ir komandas, jeigu yra išankstinių komandų „Microsoft Teams” platformoje](map-stores-existing-teams.md)

[„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo DUK](teams-integration-faq.md)