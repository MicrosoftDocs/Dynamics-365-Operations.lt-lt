---
title: Prekių gavimo įrašymas pirkimo užsakyme
description: Šiame straipsnyje paaiškinama, kaip registruoti prekių gavimą tiesiogiai į pirkimo užsakymą.
author: GalynaFedorova
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22baf6d0f6db04b3c6ce3c09ee8cb286e9a1e590
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882466"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Prekių gavimo įrašymas pirkimo užsakyme

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip registruoti prekių gavimą tiesiogiai į pirkimo užsakymą. Taip pat produktų gavimą galima registruoti sandėlyje ir vėliau tai įrašyti pirkimo užsakyme. Šią užduotį paprastai atlieka pirkimo agentas arba mokėtinų sumų koordinatorius. Šiame vedlyje pateikiamą pavyzdį galima naudoti demonstracinių duomenų įmonėje USMF. Pavyzdys apima veiksmus, skirtus paprastam pirkimo užsakymui kurti, kad procedūrą būtų galima paleisti kaip užduočių vedlį. Jei atlikdami procedūrą naudojote savo duomenis, pradėkite nuo antrinės užduoties **Įrašyti prekių gavimą**.


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