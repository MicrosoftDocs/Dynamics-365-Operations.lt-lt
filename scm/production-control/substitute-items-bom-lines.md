---
title: "Medžiagų keitimas gamyboje"
description: "Šioje temoje aprašoma, kaip keisti medžiagas gamybos proceso metu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdBOM
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70171
ms.assetid: ce3b11ef-550e-49b7-8942-2607c2ec3c5c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 1d6f16cad4c985a5628e2589aece8e628c83ef22
ms.lasthandoff: 03/31/2017


---

# <a name="material-substitution-in-manufacturing"></a>Medžiagų keitimas gamyboje

[!include[banner](../includes/banner.md)]


Šioje temoje aprašoma, kaip keisti medžiagas gamybos proceso metu. 

Medžiagas keisti gamybos proceso metu galima trimis toliau nurodytais būdais.

-   Pagal datą, kai vienos medžiagos pakeičiamos kitomis po tam tikros datos
-   Vykdant bendrąjį planavimą, kai medžiagos formulėje pakeičiamos kitomis medžiagomis, nes jų atsargose nebėra
-   Gaminant, kai medžiagos netikėtai baigiasi ir yra pakeičiamos kitomis medžiagomis

## <a name="substituting-material-by-date"></a>Medžiagų keitimas pagal datą
Apsvarstykite šį scenarijų: įmonės gaminama mašina turi komponentą, kurio atsargos tiekėjo kataloge baigsis po dviejų mėnesių. Pasibaigus galiojimo datai tiekėjas pasiūlys naują komponentą, kuriuo būtų galima pakeisti seną komponentą. Nuo ir iki galiojimo datas galima nustatyti komplektavimo specifikacijos (KS) eilutėse. Pvz., seno komponento galiojimo datą galite nustatyti lauke **Pabaigos data** įvesdami galiojimo datą. Tada KS galite nustatyti naują komponento pakaitalą, kuris galios nuo tos dienos, kai baigs galioti senas komponentas. Norėdami tai padaryti, lauke **Pradžios data** įveskite pradžios datą.

## <a name="substituting-material-by-planning"></a>Medžiagų keitimas planuojant
Planuodami medžiagas galite keisti tik kai naudojate formules, o ne KS. Apsvarstykite šį scenarijų: maisto gamybos įmonė galima padažą pagal formulę, kurioje yra 20 ingredientų. Vieną formulės ingredientą galima pakeisti vienu arba dviem kitais ingredientais. Tačiau kadangi šie du ingredientai yra brangesni nei pageidaujamas ingredientas, ingrediento pakaitalai naudojami tik jei pageidaujamo ingrediento atsargos baigėsi. Medžiaga, kurią galima keisti, vadinama A, o du galimi tos medžiagos pakaitalai vadinami B ir C. Medžiagų keitimą planuojant valdo formulės eilučių laukai **Plano grupė** ir **Prioritetas**. Pagal šį pavyzdį galite sukurti trijų medžiagų formulės eilutes ir jas susieti su ta pačia plano grupe. Pagal nustatymus A medžiagos formulės eilutės prioritetas yra aukščiausias (mažiausias skaičius), C medžiagos formulės eilutės prioritetas yra žemiausias, o B medžiagos formulės eilutės prioritetas yra tarp kitų dviejų eilučių prioritetų. Jei nustatytas baigtos prekės poreikis, bendrojo planavimo metu pirmiausia nustatoma, ar galima patenkinti A medžiagos poreikį. Jei poreikio patenkinti negalima, bendrojo planavimo metu analizuojamos B ir C medžiagos, atsižvelgiant į jų prioritetą. Jei yra B medžiagos, ji bus naudojama, kai suplanuotas formulės paketinis užsakymas bus patvirtintas. Jei atsargose nėra jokių reikiamų medžiagų, bendrojo planavimo metu sukuriamas suplanuotas A medžiagų užsakymas. **Pastaba:** formulės eilutes nustatydami plano grupėje, turite nurodyti tik aukščiausio prioriteto medžiagos kiekį. Šis kiekis bus naudojamas visų plano medžiagų poreikiui apskaičiuoti, įskaitant net ir žemesnio prioriteto medžiagas. Skirtingų žemesnio prioriteto plano grupės prekių kiekių nurodyti negalima.

## <a name="substituting-material-during-production"></a>Medžiagų keitimas gamybos metu
Apsvarstykite šį scenarijų: atliekant suvirinimo operaciją reikalinga metalinės plokštės dalis. Operacijos metu sandėlio darbuotojas informuoja mašinų operatorių, kad plokščių atsargose nėra. Tačiau nuspręsta, kad plokštę galima pakeisti kita, šiek tiek storesne plokšte. Tokiu atveju operaciją galima baigti. Medžiagą galima įtraukti į atviro gamybos užsakymo KS. Jei gamybos užsakymo būsena yra **Pradėtas**, vartotojų paprašoma iš naujo įvertinti užsakymą, kai jie į gamybos KS įtraukia naują elementą. Įtraukus medžiagą galima sukurti naują naujos prekės išrinkimo dokumentą. Į gamybos KS naujos medžiagos įtraukti nereikia. Vietoj to, galite jas įtraukti tiesiai į gamybos išrinkimo dokumentą. Tada, užregistravus išrinkimo dokumentą, sistema medžiagą įtrauks į gamybos KS.




