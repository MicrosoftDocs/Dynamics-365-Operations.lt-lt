---
title: Standartinių savikainų įkainojimo versijų apribojimai
description: Šioje temoje aprašomi apribojimai, taikomi standartinių savikainų įkainojimo versijai.
author: AndersGirke
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
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2028cdabde3d01de16050b38893ec9e42353ae542be7a0cd7362cf62e9315170
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748792"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Standartinių savikainų įkainojimo versijų apribojimai

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomi apribojimai, taikomi standartinių savikainų įkainojimo versijai. 

Tolesni apribojimai padeda užtikrinti griežtą standartinių įkainojimo principų laikymąsi.

-  Išlaidos turi būti įtrauktos į prekės savikainą. Pagamintos prekės išlaidos nurodo komplektavimo specifikacijos (KS) ir maršruto informacijos amortizuotas pastovias išlaidas. Todėl išlaidos turi būti įtrauktos į vieneto savikainą. Nupirktos prekės išlaidos taip pat įtrauktos į prekės vieneto savikainą.

-  Pagamintų prekių standartinių išlaidų skaičiavimas turi būti pagrįstas standartinių išlaidų įkainojimo versijos išlaidų įrašais. Alternatyvūs išlaidų duomenų šaltiniai gali būti naudojami tik su planuojamų išlaidų įkainojimo versija, pvz., nupirktų prekių pirkimo kainų prekybos sutartimis. Alternatyvius išlaidų duomenų šaltinius nustato KS skaičiavimo grupė.

-  KS skaičiavimai turi būti atliekami vieno lygio išskleidimo režimu.

Prekės standartinių išlaidų duomenys gali būti kopijuojami į kitą įkainojimo versiją, į kurią įtrauktos standartinės išlaidos arba planuojamos išlaidos. Tačiau prekės planuojamų išlaidų duomenys negali būti kopijuojami į išlaidų versiją, į kurią įtrauktos standartinės savikainos, nes anksčiau šioje temoje išvardyti apribojimai netaikomi planuojamoms išlaidoms.

## <a name="related-topics"></a>Susijusios temos

[Įkainojimo versijų apžvalga](costing-versions.md)

[Ne gamybos aplinkos standartinių išlaidų naujinimas](update-standard-costs-non-manufacturing-environment.md)

[Pagamintų prekių standartinių savikainų paruošimas priežiūrai](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]