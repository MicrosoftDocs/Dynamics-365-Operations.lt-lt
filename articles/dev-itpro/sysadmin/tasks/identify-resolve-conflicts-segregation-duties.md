---
title: Pareigų atskyrimo nesuderinamumų nustatymas ir pašalinimas
description: Šioje temoje paaiškinama, kaip nustatyti ir pašalinti pareigų atskyrimo nesuderinamumus.
author: maertenm
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c89d27eb8b587e8936258aae3ec1fee4574ccfb
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851340"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Pareigų atskyrimo nesuderinamumų nustatymas ir pašalinimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje temoje paaiškinama, kaip nustatyti ir pašalinti pareigų atskyrimo nesuderinamumus. Galite nustatyti taisykles, kad atskirtumėte užduotis, kurias turi atlikti skirtingi vartotojai. Ši koncepcija vadinama pareigų atskyrimu. Kai saugos vaidmens apibrėžimas arba vartotojo vaidmens priskyrimai pažeidžia taisykles, registruojamas neatitikimas. Visus neatitikimus turi išspręsti administratorius. Norėdami identifikuoti ir išspręsti neatitikimus, atlikite šią procedūrą. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Patikrinti, ar vartotojo vaidmens priskyrimai atitinka naujas pareigų atskyrimo taisykles
1. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Pareigų atskyrimas > Tikrinti vartotojo vaidmenų priskyrimo atitikimą**.
2. Pasirinkite **Gerai**. Pranešime rodomi tikrinimo rezultatai. Jei yra neatitikimas, galite atidaryti puslapį **Vartotojai** ir pakeisti vartotojo vaidmens priskyrimus. Neatitikimai taip pat registruojami puslapyje **Segregation of duties conflicts**. Norėdami tikrinimo procesą paleisti kaip paketinę užduotį, pasirinkite **Batch processing** ir nustatykite kitus paketo parametrus. Paleidę paketinę užduotį, puslapyje **Pareigų atskyrimo nesuderinamumai** galėsite peržiūrėti neatitikimus.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Peržiūrėti ir išspręsti nesuderinamus vartotojo vaidmenų priskyrimus
1. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Pareigų atskyrimas > Pareigų atskyrimo nesuderinamumai.** Pasirinkite konfliktą, tada pasirinkite vieną iš šių mygtukų: **Deny assignment – Deny the assignment of the user to the additional security role**. Jei atmesite automatinį vaidmens priskyrimą, vartotojas pažymimas kaip pašalintas iš vaidmens. Pašalintam vartotojui nesuteikiama su vaidmeniu susieta prieiga ir šio vartotojo negalima priskirti vaidmeniui tol, kol administratorius nepanaikins pašalinimo. Leisti priskirti – **nepaisyti** neatitikimo ir leisti vartotoją priskirti abiems saugos vaidmenims. Jei nepaisote neatitikimo, lauke **Reason for override** turite įvesti priežastį.  
2. Uždarykite puslapį.
3. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Pareigų atskyrimas > Neišspręsti pareigų atskyrimo nesuderinamumai.** Pasirinkite konfliktą, tada pasirinkite vieną iš šių mygtukų: **Deny assignment – Deny the assignment of the user to the additional security role**. Jei atmesite automatinį vaidmens priskyrimą, vartotojas pažymimas kaip pašalintas iš vaidmens. Pašalintam vartotojui nesuteikiama su vaidmeniu susieta prieiga ir šio vartotojo negalima priskirti vaidmeniui tol, kol administratorius nepanaikins pašalinimo. Leisti priskirti – **nepaisyti** neatitikimo ir leisti vartotoją priskirti abiems saugos vaidmenims. Jei nepaisote neatitikimo, **Reason for override field** turite įvesti priežastį.    
4. Uždarykite puslapį.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Patikrinti, ar esami vaidmenys atitinka naujas pareigų atskyrimo taisykles
1. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Pareigų atskyrimas > Pareigų atskyrimo taisyklės**. Pasirinkite taisyklę.  
2. Pasirinkite **Tikrinti pareigas ir vaidmenis**. Jei esami vaidmenys pažeidžia pasirinktą taisyklę, rodomas pranešimas, kuriame pateikiamas vaidmens pavadinimas ir nesuderinamų pareigų pavadinimai. Administratorius turi nurodyti saugos rizikos mažinimą arba modifikuoti vaidmenį, kad jis nepažeistų pareigų atskyrimo taisyklių. Jei nėra vaidmenų, kurie pažeistų pasirinktą taisyklę, pranešime rodoma, kad visi vaidmenys atitinka.  

