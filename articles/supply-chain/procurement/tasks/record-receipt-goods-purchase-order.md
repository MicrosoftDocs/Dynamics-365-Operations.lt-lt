---
title: Prekių gavimo įrašymas pirkimo užsakyme
description: Šioje temoje aprašoma, kaip įrašyti prekių gavimą tiesiogiai pirkimo užsakyme.
author: FrankDahl
manager: AnnBe
ms.date: 07/09/19
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e81bb3fe95326636c28885d4decad69f841e3db
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844014"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Prekių gavimo įrašymas pirkimo užsakyme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje temoje aprašoma, kaip įrašyti prekių gavimą tiesiogiai pirkimo užsakyme. Taip pat produktų gavimą galima registruoti sandėlyje ir vėliau tai įrašyti pirkimo užsakyme. Šią užduotį paprastai atlieka pirkimo agentas arba mokėtinų sumų koordinatorius. Šiame vedlyje pateikiamą pavyzdį galima naudoti demonstracinių duomenų įmonėje USMF. Pavyzdys apima veiksmus, skirtus paprastam pirkimo užsakymui kurti, kad procedūrą būtų galima paleisti kaip užduočių vedlį. Jei atlikdami procedūrą naudojote savo duomenis, pradėkite nuo antrinės užduoties **Record receipt of goods**.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Naujo prekių gavimo pirkimo užsakymo ruošimas
1. Pasirinkite**Navigation pane > Modules > Procurement and sourcing > Purchase orders > All purchase orders**.
2. Pasirinkite **Naujas**.
3. Lauke **„Tiekėjo paskyra“** įveskite „`US-101`“.
4. Pasirinkite **Gerai**.
5. Lauke **„Prekės numeris“** įveskite „`M0001`“.
6. Lauke **„Kiekis“** įveskite „`5`“.
7. Veiksmų srityje pasirinkite **Pirkimas**.
8. Pasirinkite **„Patvirtinti“**.

## <a name="record-receipt-of-goods"></a>Įrašyti prekių gavimą
1. Veiksmų srityje pasirinkite **„Gauti“**.
2. Pasirinkite **„Produkto gavimo kvitas“**. Lauke **Quantity** galima pasirinkti skirtingas kiekio, kurį norite gauti, parinktis. Pavyzdžiui, jei kiekis buvo anksčiau užregistruotas sandėlyje, galite pasirinkti **Registered quantity**. Pavyzdžiui, naudokite reikšmę **Ordered quantity**.
3. Išplėskite **Overview** skyrių.
4. Lauke **Produkto gavimo kvitas** įveskite bet kurią reikšmę. Šiame lauke įvedama nuoroda, kuri naudojama kaip produktų gavimo žurnalo kvitas.  
5. Išplėskite skyrių **Lines**.
6. Nustatykite **Quantity** lauke „4“. Čia galite patys nurodyti kiekvienos užsakymo eilutės gaunamą kiekį.  
7. Pasirinkite **Gerai**. Dabar pirkimo užsakyme prekės užregistruotos kaip gautos, o tai atsispindi sukurtame produktų gavimo kvitų žurnale. Galite naudoti veiksmą Produkto gavimo kvitas, norėdami peržiūrėti žurnalus, sukurtus su pirkimo užsakymu, ir sužinoti, kas ir kada buvo gauta.  

