---
title: Prekių gavimo įrašymas pirkimo užsakyme
description: Šioje temoje aprašoma, kaip įrašyti prekių gavimą tiesiogiai pirkimo užsakyme.
author: kamaybac
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a030de902915d25d1b309e53a2af5d8b7ec32125
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811971"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Prekių gavimo įrašymas pirkimo užsakyme

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip įrašyti prekių gavimą tiesiogiai pirkimo užsakyme. Taip pat produktų gavimą galima registruoti sandėlyje ir vėliau tai įrašyti pirkimo užsakyme. Šią užduotį paprastai atlieka pirkimo agentas arba mokėtinų sumų koordinatorius. Šiame vedlyje pateikiamą pavyzdį galima naudoti demonstracinių duomenų įmonėje USMF. Pavyzdys apima veiksmus, skirtus paprastam pirkimo užsakymui kurti, kad procedūrą būtų galima paleisti kaip užduočių vedlį. Jei atlikdami procedūrą naudojote savo duomenis, pradėkite nuo antrinės užduoties **Įrašyti prekių gavimą**.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Naujo prekių gavimo pirkimo užsakymo ruošimas
1. Pasirinkite **Naršymo sritis > Moduliai > Įsigijimas ir šaltinio pasirinkimas > Pirkimo užsakymai > Visi pirkimo užsakymai**.
2. Pasirinkite **Naujas**.
3. Lauke **„Tiekėjo paskyra“** įveskite „`US-101`“.
4. Pasirinkite **Gerai**.
5. Lauke **„Prekės numeris“** įveskite „`M0001`“.
6. Lauke **„Kiekis“** įveskite „`5`“.
7. Veiksmų srityje pasirinkite **Pirkimas**.
8. Pasirinkite **„Patvirtinti“**.

## <a name="record-receipt-of-goods"></a>Įrašyti prekių gavimą
1. Veiksmų srityje pasirinkite **„Gauti“**.
2. Pasirinkite **„Produkto gavimo kvitas“**. Lauke **Kiekis** galima pasirinkti skirtingas kiekio, kurį norite gauti, parinktis. Pavyzdžiui, jei kiekis buvo anksčiau užregistruotas sandėlyje, galite pasirinkti **Užregistruotas kiekis**. Pavyzdžiui, naudokite reikšmę **Užsakytas kiekis**.
3. Išplėskite **Peržiūra** skyrių.
4. Lauke **Produkto gavimo kvitas** įveskite bet kurią reikšmę. Šiame lauke įvedama nuoroda, kuri naudojama kaip produktų gavimo žurnalo kvitas.  
5. Išplėskite skyrių **Eilutės**.
6. Nustatykite **Kiekis** lauke „4“. Čia galite patys nurodyti kiekvienos užsakymo eilutės gaunamą kiekį.  
7. Pasirinkite **Gerai**. Dabar pirkimo užsakyme prekės užregistruotos kaip gautos, o tai atsispindi sukurtame produktų gavimo kvitų žurnale. Galite naudoti veiksmą Produkto gavimo kvitas, norėdami peržiūrėti žurnalus, sukurtus su pirkimo užsakymu, ir sužinoti, kas ir kada buvo gauta.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]