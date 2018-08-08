---
title: "Standartinių gamybos aplinkos išlaidų atnaujinimas"
description: "Šiame straipsnyje patariama, kaip atnaujinti standartines išlaidas gamybos aplinkoje."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b9ad13071c3e0c3a294e9d4413de160a58559640
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="update-standard-costs-in-a-manufacturing-environment"></a>Standartinių gamybos aplinkos išlaidų atnaujinimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje patariama, kaip atnaujinti standartines išlaidas gamybos aplinkoje. 

Atnaujinimai gali atspindėti naujas prekes, išlaidų kategorijas ar netiesioginių išlaidų skaičiavimo formules. Jie taip pat gali atspindėti taisymus ir išlaidų pokyčius. Atnaujinimo tipas lemia veiksmus, kuriuos turite atlikti norėdami atnaujinti standartines išlaidas, kaip parodyta šiuose pavyzdžiuose:

-   Įveskite numatomus nupirktų prekių standartinių išlaidų keitimus, tada atitinkama data pakeiskite prekės išlaidų įrašų būseną į **Aktyvi**. Tačiau neperskaičiuokite pagamintų prekių, naudojančių nupirktas prekes, išlaidų.
-   Įveskite naujai nupirktos prekės standartines išlaidas, bet neperskaičiuokite pagamintų prekių, turinčių komplektavimo specifikacijos (KS) versiją, kurios vienas iš komponentų yra naujai nupirkta prekė, išlaidų.
-   Pataisykite ir pakeiskite nupirktos prekės išlaidas arba pakeiskite nupirktai prekei priskirtą išlaidų grupę bei apskaičiuokite visų pagamintų prekių, turinčių KS versiją, kurios vienas iš komponentų yra nupirkta prekė, išlaidas.
-   Pakeiskite išlaidų kategorijos išlaidas ir apskaičiuokite visų pagamintų prekių, turinčių maršruto versiją, kurioje yra išlaidų kategoriją naudojančios maršruto planavimo operacijos, išlaidas.
-   Pakeiskite išlaidų kategorijas, priskirtas maršruto planavimo operacijoms arba išlaidų grupei, kuri priskirta išlaidų kategorijoms. Tada apskaičiuokite visų pagamintų prekių, turinčių maršruto versiją, kurioje yra išlaidų kategoriją naudojančios maršruto planavimo operacijos, išlaidas.
-   Pakeiskite netiesioginių išlaidų skaičiavimo formulę bei apskaičiuokite visų pagamintų prekių, kurias paveikė keitimas, išlaidas.
-   Pakeiskite arba pridėkite gamybos teritoriją pagamintai prekei ir apskaičiuokite pagamintos prekės išlaidas teritorijai.
-   Apskaičiuokite, arba perskaičiuokite, pagamintos prekės išlaidas ir perskaičiuokite visų pagamintų prekių, turinčių KS versiją, kurios vienas iš komponentų yra pagaminta prekė, išlaidas.
-   Apskaičiuokite naujai pagamintos prekės išlaidas, atsižvelgdami į nurodytą, patvirtintą ir aktyvią KS ir maršruto informaciją.

Kiekvienu atveju reikia kruopščiai įvertinti, kaip atnaujinti standartines išlaidas.




