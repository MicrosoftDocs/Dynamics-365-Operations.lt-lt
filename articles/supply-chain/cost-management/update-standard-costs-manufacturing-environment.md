---
title: Standartinių gamybos aplinkos išlaidų atnaujinimas
description: Šiame straipsnyje patariama, kaip atnaujinti standartines išlaidas gamybos aplinkoje.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8acbcb79fa45ea2f225775068e0d061a44cba1f7
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675241"
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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]