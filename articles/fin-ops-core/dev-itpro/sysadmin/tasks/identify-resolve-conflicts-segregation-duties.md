---
title: Pareigų atskyrimo nesuderinamumų nustatymas ir pašalinimas
description: Šioje temoje paaiškinama, kaip nustatyti ir pašalinti pareigų atskyrimo nesuderinamumus.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0638699c0e569bbe67024a87d6c55729642557cb085ee899aa98aa0022b12840
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748317"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Pareigų atskyrimo nesuderinamumų nustatymas ir pašalinimas

[!include [banner](../../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti ir pašalinti pareigų atskyrimo nesuderinamumus. Galite nustatyti taisykles, kad atskirtumėte pareigas, kurias turi atlikti skirtingi vartotojai. Ši koncepcija vadinama pareigų atskyrimu. Kai saugos vaidmens apibrėžimas arba vartotojo vaidmens priskyrimai pažeidžia taisykles, registruojamas neatitikimas. Visus neatitikimus turi išspręsti administratorius. Norėdami identifikuoti ir išspręsti neatitikimus, atlikite šią procedūrą.

Pridėję taisyklę patikrinkite, ar visi esami vaidmenys yra suderinami. 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a>Patikrinkite, ar esami vaidmenys ir pareigos atitinka naujas pareigų atskyrimo taisykles
1. Eikite į **Sistemos administravimas** > **Sauga** > **Pareigų atskyrimas** > **Pareigų atskyrimo taisyklės**.
3. Pasirinkite **Tikrinti pareigas ir vaidmenis**. Jei esami vaidmenys pažeidžia taisykles, parodomas pranešimas, kuriame pateikiamas taisyklės pavadinimas, vaidmuo ir nesuderinamų pareigų pavadinimai. Nesuderinamus vaidmenis būtina redaguoti naudojant **Saugos konfigūravimas** ir jie negali turėti nesuderinamų pareigų. Jei nėra vaidmenų, kurie pažeistų pasirinktą taisyklę, pranešime rodoma, kad visi vaidmenys suderinami.   

> [!NOTE]
> Patvirtinimas atliekamas tik pasirinktai taisyklei. Svarbu patikrinti kiekvienos taisyklės atitikimą.   

Kuriant arba modifikuojant vaidmenį, automatiškai taikomos pareigų atskyrimo taisyklės. Vaidmeniui negalima priskirti nesuderinamų pareigų.

Tada patikrinkite, ar visi esami vaidmenų priskyrimai yra suderinami.

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Patikrinimas, ar vartotojo vaidmens priskyrimai atitinka naujas pareigų atskyrimo taisykles
1. Eikite į **Sistemos administravimas > Sauga > Pareigų atskyrimas > Tikrinti vartotojo vaidmenų priskyrimo atitikimą**.
2. Pasirinkite **Gerai**. Pranešime rodomi tikrinimo rezultatai. Neatitikimai registruojami **Pareigų atskyrimo neišspręsti nesuderinamumai** puslapyje.   

Priskiriant vartotojus vaidmenims, automatiškai taikomos pareigų atskyrimo taisyklės. Jei bandysite priskirti vartotoją vaidmenims, kuriuose yra nesuderinamų pareigų, gausite klaidos pranešimą. Tada turite išspręsti nesuderinamumą leisdami arba neleisdami papildomą vaidmens priskyrimą. Leidus priskyrimą bus priskirtas papildomas vaidmuo. 

> [!NOTE]
> Šiuo metu nėra tikrinami vartotojų, kuriems priskirti vaidmenys pagal „Active Directory” domenų grupes, nesuderinamumai.

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Peržiūrėti ir išspręsti nesuderinamus vartotojo vaidmenų priskyrimus
1. Eikite į **Sistemos administravimas** > **Sauga** > **Pareigų atskyrimas** > **Neišspręsti pareigų atskyrimo nesuderinamumai**. 
2. Pasirinkite nesuderinamumą ir tada pasirinkite vieną iš tolesnių veiksmų: 

  - **Atmesti priskyrimą**: Tai atmes papildomą saugos vaidmens priskyrimą vartotojui. Jei atmesite automatinį vaidmens priskyrimą, vartotojas pažymimas kaip pašalintas iš vaidmens. Pašalintam vartotojui nesuteikiama su vaidmeniu susieta prieiga ir jo negalima priskirti vaidmeniui tol, kol administratorius nepanaikins pašalinimo. 
-  **Leisti priskyrimą**: Tai nepaisys neatitikimo ir leis vartotoją priskirti papildomam saugos vaidmeniui. Jei nepaisote neatitikimo, lauke **Nepaisymo priežastis** turite įvesti priežastį. Visus nepaisomus vaidmenų priskyrimus galima peržiūrėti **Pareigų atskyrimo nesuderinamumai** puslapyje.  

> [!NOTE]
> Jei keli nesuderinamumai išvardyti tam pačiam vartotojui, pasirinkite vartotojo įrašą ir įvertinkite priskirtus vaidmenis **Vartotojai** puslapyje. Norėdami išvengti šio nesuderinamumo, patvirtinkite kiekvieną taisyklę ją pridėjus arba modifikavus.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]