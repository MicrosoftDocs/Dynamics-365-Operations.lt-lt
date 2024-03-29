---
title: Standartinių savikainų įkainojimo versijų apribojimai
description: Šiame straipsnyje aprašomi apribojimai, taikomi standartinių išlaidų įkainojimo versijai.
author: JennySong-SH
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c5c00ae8952e2c80d97d039271a6f5c63e9a72f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867991"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Standartinių savikainų įkainojimo versijų apribojimai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomi apribojimai, taikomi standartinių išlaidų įkainojimo versijai. 

Tolesni apribojimai padeda užtikrinti griežtą standartinių įkainojimo principų laikymąsi.

-  Išlaidos turi būti įtrauktos į prekės savikainą. Pagamintos prekės išlaidos nurodo komplektavimo specifikacijos (KS) ir maršruto informacijos amortizuotas pastovias išlaidas. Todėl išlaidos turi būti įtrauktos į vieneto savikainą. Nupirktos prekės išlaidos taip pat įtrauktos į prekės vieneto savikainą.

-  Pagamintų prekių standartinių išlaidų skaičiavimas turi būti pagrįstas standartinių išlaidų įkainojimo versijos išlaidų įrašais. Alternatyvūs išlaidų duomenų šaltiniai gali būti naudojami tik su planuojamų išlaidų įkainojimo versija, pvz., nupirktų prekių pirkimo kainų prekybos sutartimis. Alternatyvius išlaidų duomenų šaltinius nustato KS skaičiavimo grupė.

-  KS skaičiavimai turi būti atliekami vieno lygio išskleidimo režimu.

Prekės standartinių išlaidų duomenys gali būti kopijuojami į kitą įkainojimo versiją, į kurią įtrauktos standartinės išlaidos arba planuojamos išlaidos. Tačiau prekės planuojamų išlaidų duomenys negali būti kopijuojami į išlaidų versiją, kurioje yra standartinės išlaidos, nes anksčiau šiame straipsnyje išvardyti apribojimai netaikomi planuojams išlaidoms.

## <a name="related-articles"></a>Susiję straipsniai

[Įkainojimo versijų apžvalga](costing-versions.md)

[Ne gamybos aplinkos standartinių išlaidų naujinimas](update-standard-costs-non-manufacturing-environment.md)

[Pagamintų prekių standartinių savikainų paruošimas priežiūrai](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]