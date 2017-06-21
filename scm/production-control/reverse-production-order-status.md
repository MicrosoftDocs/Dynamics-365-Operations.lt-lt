---
title: "Atšaukti gamybos užsakymo būseną"
description: "Šioje temoje aprašoma, kaip atšaukti gamybos užsakymo būseną."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmStatusDecrease
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: cfeb5a6d980318871c74baa58d5d48bf11a6bb58
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="reverse-the-production-order-status"></a>Atšaukti gamybos užsakymo būseną

[!include[banner](../includes/banner.md)]


Šioje temoje aprašoma, kaip atšaukti gamybos užsakymo būseną. 

Atšaukus gamybos užsakymo būseną, užsakymas ir visos operacijos, susijusios su maršrutais, grįš į ankstesnį gamybos ciklo etapą. Pavyzdžiui, jei gamybos užsakymo būsena yra **Suplanuota**, o jūs pakeičiate ją atgal į **Sukurta**. Šiuo atveju sistema pirmiausia turi pakeisti būseną į **Įvertinta**, kuri eina prieš būseną **Suplanuota**. Tada būseną galima pakeisti į tą, kurios norite, pvz., **Sukurta**. **Pastaba.** Jei jūsų užsakymas pasiekė būseną **Paskelbti baigtu** vis tiek galite gražinti jį į ankstesnę būseną. Tačiau norėdami atnaujinti užsakymo informaciją turite iš naujo paleisti įvertinimą ir operacijų planavimą, užduočių planavimą arba abiejų tipų planavimą. Taip yra todėl, kad bet koks likusios prekės rezervavimo ir operacijų išteklių suvartojimas taip pat turi būti atnaujinti. Toliau šiame straipsnyje aprašoma, kas rodoma, kai atšaukiate gamybos užsakymo būseną šiais būdais.

-   Iš **Įvertinta** į **Sukurta**
-   Iš **Suplanuota** į **Įvertinta**
-   Iš **Išleista** į **Suplanuota**
-   Iš **Pradėta** į **Išleista**

## <a name="from-estimated-to-created"></a>Iš Įvertinta į Sukurta
Grąžinus gamybos užsakymo būseną iš **Įvertinta** į **Sukurta**, į komplektavimo specifikaciją (KS) įtrauktų apskaičiuoto prekių suvartojimo duomenys bus pašalinti. Atsargų operacijos gamybos eilutėje naikinamos ir gamybos KS eilučių laukas **Likučio būsena** nustatomas kaip **Baigta**. Pasirinkus parinktis **Išvestiniai pirkimai** ir **Išvestinė gamyba**, visi esami pirkimo arba gamybos užsakymai panaikinami. Jei įvertinote gamybos užsakymo išlaidas arba rankiniu būdu rezervavote prekes, kad jas būtų galima naudoti gamyboje, šios operacijos bus pašalintos.

## <a name="from-scheduled-to-estimated"></a>Iš Suplanuota į Įvertinta
Grąžinus gamybos užsakymo būseną iš **Suplanuota** į **Įvertinta**, suplanuotos pradžios ir pabaigos datos ir laikai bus pašalinti. Planavimo metu įvykdytas pajėgumo rezervavimas yra pašalinamas, o užduotys, sukurtos užduočių planavimo metu, yra naikinamos. Visa informacija apie operacijų planavimą ir užduočių planavimą, įrašoma puslapyje **Gamybos užsakymo informacija**, bus atnaujinta.

## <a name="from-released-to-scheduled"></a>Iš Išleista į Suplanuota
Grąžinus gamybos užsakymo būseną iš **Išleista** į **Suplanuota**, pasikeis tik būsenos lauke rodoma būsena.

## <a name="from-started-to-released"></a>Iš Pradėta į Išleista
Grąžinus gamybos užsakymo būseną iš **Pradėta** į **Išleista**, visos prekės, kurios buvo paskelbtos baigtomis, bus grąžintos. Jei medžiagos buvo surinktos arba jei gautos ir siunčiamos siuntos buvo gaminamos, šie parametrai atšaukiami. Gamybos užsakymo KS eilučių lauko **Likučio būsena** vertė pasikeičia iš **Baigta** į **Medžiagų suvartojimas**. Jei buvo užregistruotas laikas arba gamybos maršruto operacijai nustatytas kiekis buvo paskelbtas baigtu, šie parametrai bus atšaukti. Gamybos maršruto lauke **Likučio būsena** pasikeičia iš **Baigta** į **Maršruto suvartojimas**. Atšaukiami visų prekių, kurios užregistruotos kaip apdorojamos arba kurių gamyba nebaigta, parametrai. **Gamybos užsakymo informacijos** puslapio laukai, kuriuose nurodomas pradėtas gaminti arba paskelbtas baigtu kiekis, nustatomi iš naujo. Šių operacijų datos taip pat nustatomos iš naujo.




