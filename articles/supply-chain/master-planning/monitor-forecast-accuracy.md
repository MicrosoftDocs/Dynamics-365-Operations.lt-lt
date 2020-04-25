---
title: Prognozės tikslumo stebėjimas
description: Šioje temoje aprašomi prognozės tikslumo, kurį apskaičiuoja „Dynamics 365 Supply Chain Management“, tipai, ir paaiškinama, kaip galima peržiūrėti tikslumo reikšmes.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab74ba88ba9eb683107ef82bc105f5a3ed8fac08
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209817"
---
# <a name="monitor-forecast-accuracy"></a>Prognozės tikslumo stebėjimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomi prognozės tikslumo, kurį apskaičiuoja „Microsoft Dynamics 365 Supply Chain Management“, tipai, ir paaiškinama, kaip galima peržiūrėti tikslumo reikšmes.

„Supply Chain Management“ apskaičiuoja toliau nurodytų tipų prognozės tikslumą.

-   Praeities prognozės tikslumas, bendrajame planavime naudojamą praeities prognozę palyginant su praeities poreikiu. Norėdami peržiūrėti praeities prognozės tikslumo reikšmes (absoliučiąsias ir procentines), puslapyje **Poreikio prognozės informacija** spustelėkite **Rodyti tikslumą**.
-   Įvertintas prognozės modelio, naudojamo prognozėms generuoti, tikslumas. Tikslumo procentą galite peržiūrėti puslapio **Poreikio prognozės informacija** dalyje **Modelio informacija – MAPE**. 

> [!NOTE]
> Jei naudojate poreikio prognozės „Microsoft Azure“ mašininį mokymą, vidaus modelio tikslumo skaičiavimas yra pagrįstas bandymo duomenų rinkiniu. Norėdami nurodyti bandymo duomenų rinkinio dydį, puslapyje **Poreikio prognozės parametrai** nustatykite parametrą **TEST\_SET\_SIZE\_PERCENT**. Pavyzdžiui, jei nustatysite reikšmę **20**, vidaus modelio tikslumui apskaičiuoti bus naudojami paskutiniai 20 procentų praeities duomenų.


<a name="additional-resources"></a>Papildomi ištekliai
--------

[Pakoreguotos prognozės įgaliojimas](authorize-adjusted-forecast.md)

[Pašalinių reikšmių šalinimas iš praeities operacijų duomenų skaičiuojant poreikio prognozę](remove-historical-outliers-calculating-demand-forecast.md)



