--- 
title: "Nustatyti ir pašalinti pareigų atskyrimo nesuderinamumus"
description: "Galite nustatyti taisykles, kad atskirtumėte užduotis, kurias turi atlikti skirtingi vartotojai."
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c3a366ea4b558ba4e4af7336992dbb091b0b1414
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Nustatyti ir pašalinti pareigų atskyrimo nesuderinamumus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Galite nustatyti taisykles, kad atskirtumėte užduotis, kurias turi atlikti skirtingi vartotojai. Ši koncepcija vadinama pareigų atskyrimu. Kai saugos vaidmens apibrėžimas arba vartotojo vaidmens priskyrimai pažeidžia taisykles, registruojamas neatitikimas. Visus neatitikimus turi išspręsti administratorius. Norėdami identifikuoti ir išspręsti neatitikimus, atlikite šią procedūrą. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Patikrinti, ar vartotojo vaidmens priskyrimai atitinka naujas pareigų atskyrimo taisykles
1. Eikite į Sistemos administravimas > Sauga > Pareigų atskyrimas > Tikrinti vartotojo vaidmenų priskyrimo atitikimą.
2. Spustelėkite GERAI.
    * Pranešime rodomi tikrinimo rezultatai.     Jei yra neatitikimas, galite atidaryti puslapį Vartotojai ir pakeisti vartotojo vaidmens priskyrimus. Neatitikimai taip pat registruojami puslapyje Pareigų atskyrimo nesuderinamumai.     Norėdami tikrinimo procesą paleisti kaip paketinę užduotį, pasirinkite Paketinis vykdymas ir nustatykite kitus paketo parametrus. Paleidę paketinę užduotį puslapyje Pareigų atskyrimo nesuderinamumai galėsite peržiūrėti neatitikimus.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Peržiūrėti ir išspręsti nesuderinamus vartotojo vaidmenų priskyrimus
1. Eikite į Sistemos administravimas > Sauga > Pareigų atskyrimas > Pareigų atskyrimo nesuderinamumus.
    * Pasirinkite neatitikimą, tada spustelėkite vieną iš šių mygtukų: Atmesti priskyrimą – atmesti vartotojo priskyrimą prie papildomo saugos vaidmens. Jei atmesite automatinį vaidmens priskyrimą, vartotojas pažymimas kaip pašalintas iš vaidmens. Pašalintam vartotojui nesuteikiama su vaidmeniu susieta prieiga ir šio vartotojo negalima priskirti vaidmeniui tol, kol administratorius nepanaikins pašalinimo.     Leisti priskirti – nepaisyti neatitikimo ir leisti vartotoją priskirti abiems saugos vaidmenims. Jei nepaisote neatitikimo, lauke Nepaisymo priežastis turite įvesti priežastį.  
2. Uždarykite puslapį.
3. Eikite į Sistemos administravimas > Sauga > Pareigų atskyrimas > Neišspręsti pareigų atskyrimo nesuderinamumai.
    * Pasirinkite neatitikimą, tada spustelėkite vieną iš šių mygtukų: Atmesti priskyrimą – atmesti vartotojo priskyrimą prie papildomo saugos vaidmens. Jei atmesite automatinį vaidmens priskyrimą, vartotojas pažymimas kaip pašalintas iš vaidmens. Pašalintam vartotojui nesuteikiama su vaidmeniu susieta prieiga ir šio vartotojo negalima priskirti vaidmeniui tol, kol administratorius nepanaikins pašalinimo.     Leisti priskirti – nepaisyti neatitikimo ir leisti vartotoją priskirti abiems saugos vaidmenims. Jei nepaisote neatitikimo, lauke Nepaisymo priežastis turite įvesti priežastį.    
4. Uždarykite puslapį.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Patikrinti, ar esami vaidmenys atitinka naujas pareigų atskyrimo taisykles
1. Eikite į Sistemos administravimas > Sauga > Pareigų atskyrimas > Pareigų atskyrimo taisyklės.
    * Pasirinkite taisyklę.  
2. Spustelėkite Tikrinti pareigas ir vaidmenis.
    * Jei esami vaidmenys pažeidžia pasirinktą taisyklę, rodomas pranešimas, kuriame pateikiamas vaidmens pavadinimas ir nesuderinamų pareigų pavadinimai. Administratorius turi nurodyti saugos rizikos mažinimą arba modifikuoti vaidmenį, kad jis nepažeistų pareigų atskyrimo taisyklių.     Jei nėra vaidmenų, kurie pažeistų pasirinktą taisyklę, pranešime rodoma, kad visi vaidmenys atitinka.  


