--- 
title: "Įrašyti prekių gavimą pirkimo užsakyme"
description: "Šioje procedūroje parodoma, kaip prekių gavimą registruoti tiesiogiai pirkimo užsakyme."
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9b2300a593c9e153ee598fa72e29907c82f2b79e
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Įrašyti prekių gavimą pirkimo užsakyme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip prekių gavimą registruoti tiesiogiai pirkimo užsakyme. Taip pat produktų gavimą galima registruoti sandėlyje ir vėliau tai įrašyti pirkimo užsakyme. Šią užduotį paprastai atlieka pirkimo agentas arba mokėtinų sumų koordinatorius. Šiame vedlyje pateikiamą pavyzdį galima naudoti demonstracinių duomenų įmonėje USMF. Pavyzdys apima veiksmus, skirtus paprastam pirkimo užsakymui kurti, kad procedūrą būtų galima paleisti kaip užduočių vedlį. Jei atlikdami procedūrą naudojote savo duomenis, pradėkite nuo antrinės užduoties Įrašyti prekių gavimą.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Naujo prekių gavimo pirkimo užsakymo ruošimas
1. Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pirkimo užsakymai > Visi pirkimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Tiekėjo kodas įveskite US-101.
4. Spustelėkite GERAI.
5. Lauke Prekės numeris įveskite M0001.
6. Lauke Kiekis įveskite 5.
7. Veiksmų srityje spustelėkite Pirkti.
8. Spustelėkite Patvirtinti.

## <a name="record-receipt-of-goods"></a>Įrašyti prekių gavimą
1. Veiksmų srityje spustelėkite Gauti.
2. Spustelėkite Produkto gavimo kvitas.
    * Lauke Kiekis galima pasirinkti skirtingas kiekio, kurį norite gauti, parinktis. Pavyzdžiui, jei kiekis buvo anksčiau užregistruotas sandėlyje, galite pasirinkti Užregistruotas kiekis.  Pavyzdžiui, naudokite reikšmę Užsakytas kiekis.   
3. Lauke Produkto gavimo kvitas įveskite bet kokią reikšmę.
    * Šiame lauke įvedama nuoroda, kuri naudojama kaip produktų gavimo žurnalo kvitas.  
4. Išplėskite dalį Eilutės.
5. Nustatykite kiekį – 4.
    * Čia galite patys nurodyti kiekvienos užsakymo eilutės gaunamą kiekį.  
6. Sutraukite sekciją Eilutės.
7. Spustelėkite GERAI.
    * Dabar pirkimo užsakyme prekės užregistruotos kaip gautos, o tai atsispindi sukurtame produktų gavimo kvitų žurnale. Galite naudoti veiksmą Produkto gavimo kvitas, norėdami peržiūrėti žurnalus, sukurtus su pirkimo užsakymu, ir sužinoti, kas ir kada buvo gauta.  


