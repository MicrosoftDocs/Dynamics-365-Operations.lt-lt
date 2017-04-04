---
title: "Stebėjimo prognozės tikslumas"
description: "Šiame straipsnyje aprašoma rūšių prognozių tikslumą, kad Microsoft Dynamics 365 operacijoms skaičiuoja, ir paaiškinama, kaip galite peržiūrėti tikslumo reikšmėmis."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d3f88a4fa54217cea909c54955de05e2175db0cd
ms.lasthandoff: 03/29/2017


---

# <a name="monitor-forecast-accuracy"></a>Stebėjimo prognozės tikslumas

Šiame straipsnyje aprašoma rūšių prognozių tikslumą, kad Microsoft Dynamics 365 operacijoms skaičiuoja, ir paaiškinama, kaip galite peržiūrėti tikslumo reikšmėmis.

Dinamika 365 operacijoms apskaičiuoja šių rūšių prognozių tikslumas:

-   Praeities prognozės tikslumas, bendrajame planavime naudojamą praeities prognozę palyginant su praeities poreikiu. Norėdami peržiūrėti praeities prognozės tikslumo reikšmes (absoliučiąsias ir procentines), puslapyje **Poreikio prognozės informacija** spustelėkite **Rodyti tikslumą**.
-   Įvertintas prognozės modelio, naudojamo prognozėms generuoti, tikslumas. Tikslumo procentą galite peržiūrėti puslapio **Poreikio prognozės informacija** dalyje **Modelio informacija – MAPE**. 

**Pastaba:** jei naudojate Dynamics 365 operacijų paklausos prognozavimo Microsoft Azure mašinos mokymosi tarnyba, vidaus modelio tikslumas skaičiuojama remiantis bandymo duomenų rinkinys. Nurodyti, kokio dydžio bandymo duomenų rinkinį, nustatytas į **išbandyti\_nustatyti\_dydis\_procentų** parametras su **paklausos prognozavimo parametrai** puslapis. Pavyzdžiui, jei nustatysite reikšmę **20**, vidaus modelio tikslumui apskaičiuoti bus naudojami paskutiniai 20 procentų praeities duomenų.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


