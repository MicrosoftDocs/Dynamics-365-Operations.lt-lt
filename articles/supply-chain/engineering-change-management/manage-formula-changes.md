---
title: Formulių ir jų ingredientų pakeitimų valdymas
description: Šioje temoje aprašoma, kaip atlikti formulės valdymą ir valdyti gamybos proceso bendrųjų duomenų pakeitimus.
author: t-benebo
ms.date: 05/19/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: c65f929120d2501fa3873880179a9b53ab79c60c73fd4d597fb6151b1c5bb2b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720401"
---
# <a name="manage-changes-in-formulas-and-their-ingredients"></a>Formulių ir jų ingredientų pakeitimų valdymas

[!include [banner](../includes/banner.md)]

Jei naudojate „Microsoft Dynamics 365 Supply Chain Management” proceso gamybos galimybės, taip pat galite naudoti susijusias formulių valdymo galimybes toliau pateiktiems pokyčiams valdyti:

- **Formulė ir suplanuotos prekės:** Valdykite formulėse nurodytų ingredientų ir jų sudėtinių bei šalutinių produktų pakeitimus.
- **Sudėtiniai ir šalutiniai produktai:** Redaguokite formulėje nurodytų sudėtinių ir šalutinių produktų kiekius ir kitą informaciją.
- **Esamo svorio prekės:** Valdykite esamo svorio prekių pakeitimus.

## <a name="turn-on-this-feature-in-your-system"></a>Funkcijos įjungimas jūsų sistemoje

Norėdami naudotis šia galimybe turite atlikti tolesnes užduotis.

1. Įgalinkite *Inžinerinių keitimų valdymo* funkciją ir jos konfigūracijos raktą, kaip aprašyta skyriuje [Inžinerinių keitimų valdymo apžvalga](product-engineering-overview.md). Kaip nurodyta toje temoje, įsitikinkite, kad taip pat įgalinote **Gamybos procesų pakeitimų valdymo** licencijos raktą, kuris yra įdėtas po pagrindiniu **Inžinerinių keitimų valdymo** licencijos raktu.
1. Įjunkite *Formulių ir jų ingredientų keitimų valdymo* funkciją [Funkcijų valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="feature-naming-conventions"></a>Funkcijų pavadinimų suteikimo konvencijos

„Supply Chain Management” vartotojo sąsajoje (UI) ir dokumentacijoje keitimų valdymo funkcijos įprastai yra vadinamos *inžinerinių pakeitimų valdymu*, o valdomi produktai įprastai vadinami *inžinerijos produktais*. Nors ši terminologija įprastai nesiejama su gamybos procesų formulių valdymu, inžinerinių pakeitimų valdymą turėtumėte laikyti tiesiog pakeitimų valdymu, o apie inžinerijos produktus turėtumėte galvoti kaip apie produktų versijas.

## <a name="work-with-formula-change-management-features"></a>Darbas su formulės keitimų valdymo funkcijomis

Šiame sąraše apibendrinama, kaip inžinerinių pakeitimų valdymo funkcijos yra taikomos formulės valdymui. Jame taip pat pateikiamos nuorodos į išsamesnę informaciją. Kadangi formulių pakeitimų valdymas išnaudoja inžinerinių pakeitimų valdymo funkcijas, turėtumėte sužinoti apie bendrus inžinerinių pakeitimų valdymo veikimo principus, kad galėtumėte jį naudoti savo formulių ir jų ingredientų valdymui.

- **Centralizuotas produkto duomenų valdymas** – Nustatykite organizaciją, kuri per valdomą išleidimo procesą užtikrina, kad įmonės vartotojams būtų pasiekiami tikslūs ir aktualūs produkto duomenis. Dėl daugiau informacijos, žr. [Inžinerijos bendrovės ir duomenų turėjimo taisyklės](engineering-org-data-ownership-rules.md).
- **Produkto versijos kūrimas** – Sekite produktų pakeitimus per produkto versijas ir valdykite produktą visuose tiekimo grandinės etapuose. Tokiu būdu galite sekti savo formuluočių pakeitimus. Dėl daugiau informacijos apie inžinerijos duomenis, žr. [Inžinerijos versijos ir inžinerijos produkto kategorijos](engineering-versions-product-category.md).
- **Produkto ciklo valdymas** – Valdykite produkto duomenų matomumą organizacijoje ir taip pat valdykite produkto versijų pasiekiamumą kiekviename tiekimo grandinės etape. Turite išsamią kontrolę, kada produkto versiją galima naudoti konkretiems verslo procesams, ir galite sukurti savo ciklo būsenas, atitinkančias jūsų verslo poreikius. Dėl daugiau informacijos, žr. [Produkto gyvavimo ciklo būsenos ir perlaidos](product-lifecycle-state-transactions.md).
- **Formulės keitimų valdymas** – Jūsų organizacijos vartotojai gali reikalauti formulių pakeitimų. Naudokite pakeitimo užsakymus, kad įvertintumėte ir dokumentuotumėte siūlomų pakeitimų poveikį. Įtraukite darbo eigas, kad valdytumėte pakeitimų procesą ir naujų produkto bei jo formulės versijų išleidimą. Dėl daugiau informacijos, žr. [Valdyti keitimus inžinerijos produktams](engineering-change-management.md).
- **Pasirengimo valdymas** – Naudokite sistemos patikrinimus ir vartotojo nurodymus (klausimynus ir kontrolinius sąrašus), kad užtikrintumėte, jog visi reikalingi produkto duomenys bus visiškai įvesti prieš išleidžiant produktą. Dėl daugiau informacijos, žr. [Produkto parengimas](product-readiness.md).
- **Patobulintos produkto išleidimo funkcijos** – Išleiskite visiškai apibrėžtas produkto ir jo formulės versijas iš organizacijos (juridinio subjekto) į kitus juridinius subjektus. Jūs galite netgi nuspręsti, ar prieš išleidžiant produktą, jo informaciją reikia peržiūrėti ar redaguoti. Dėl daugiau informacijos, žr. [Leidžiamo produkto struktūros](release-product-structure.md).

Atkreipkite dėmesį, kad daugelyje temų, susietų su ankstesniu sąrašu, pateikiami pavyzdžiai, pagrįsti komplektavimo specifikacijomis (KS). Tačiau formulės veikia panašiai. Toliau pateiktos kelios papildomos sąvokos, naudingos žinoti, kai naudojate pakeitimų valdymą (arba tik formulių keitimų valdymą) formulėms ir KS valdyti:

- Kiekvienai [produkto inžinerinei kategorijai](engineering-versions-product-category.md) galite nurodyti gamybos tipą (KS, formulė arba suplanuota prekė). Taip pat galite nurodyti, ar esamo svorio palaikymas yra reikalingas produktams, naudojantiems tą kategoriją.
- Sudėtiniai ir šalutiniai produktai nėra inžinerijos produktai. Todėl nėra jų versijų. Jeigu turite juos pakeisti, tiesiog sukurkite naują produktą. Toks principas palengvina priežiūrą.
- Galite valdyti gatavas prekes, kurios yra KS ir kurios turi antrinių sudėtinių prekių. Funkcijos veiks bet kuriam KS deriniui, kuriame yra formulių ir (arba) formulių, kuriose yra KS.
