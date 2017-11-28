---
title: "Prognozės tikslumo stebėjimas"
description: "Šiame straipsnyje aprašomi prognozės tikslumo, kurį apskaičiuoja „Microsoft Dynamics 365 for Finance and Operations“, tipai ir paaiškinama, kaip galima peržiūrėti tikslumo reikšmes."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bd84dde353972d2d259706dd9f8f3621cef04472
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="monitor-forecast-accuracy"></a>Prognozės tikslumo stebėjimas

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašomi prognozės tikslumo, kurį apskaičiuoja „Microsoft Dynamics 365 for Finance and Operations“, tipai ir paaiškinama, kaip galima peržiūrėti tikslumo reikšmes.

„Finance and Operations“ apskaičiuoja toliau nurodytų tipų prognozės tikslumą.

-   Praeities prognozės tikslumas, bendrajame planavime naudojamą praeities prognozę palyginant su praeities poreikiu. Norėdami peržiūrėti praeities prognozės tikslumo reikšmes (absoliučiąsias ir procentines), puslapyje **Poreikio prognozės informacija** spustelėkite **Rodyti tikslumą**.
-   Įvertintas prognozės modelio, naudojamo prognozėms generuoti, tikslumas. Tikslumo procentą galite peržiūrėti puslapio **Poreikio prognozės informacija** dalyje **Modelio informacija – MAPE**. 

**Pastaba:** jei naudojate „Finance and Operations“ poreikio prognozės „Microsoft Azure“ mašininio mokymo tarnybą, vidaus modelio tikslumo skaičiavimas yra pagrįstas bandymo duomenų rinkiniu. Norėdami nurodyti bandymo duomenų rinkinio dydį, puslapyje **Poreikio prognozės parametrai** nustatykite parametrą **TEST\_SET\_SIZE\_PERCENT**. Pavyzdžiui, jei nustatysite reikšmę **20**, vidaus modelio tikslumui apskaičiuoti bus naudojami paskutiniai 20 procentų praeities duomenų.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Pakoreguotos poreikio prognozės įgaliojimas](authorize-adjusted-forecast.md)

[Skaičiuodami poreikio prognozę iš praeities operacijų duomenų pašalinkite pašalines reikšmes](remove-historical-outliers-calculating-demand-forecast.md)




