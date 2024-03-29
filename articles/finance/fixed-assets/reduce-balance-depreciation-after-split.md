---
title: Mažėjančios vertės nusidėvėjimas po skaidymo
description: Šiame straipsnyje aprašomas metodas, kuris naudojamas ilgalaikiam turtui skaičiuojant nusidėvėjimą po to, kai turtas padalintas naudojant balanso mažinimo metodą.
author: moaamer
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 539967a9a73da91f6b49c1bb89f404267ae0a804
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883306"
---
# <a name="reduce-balance-depreciation-after-a-split"></a>Mažėjančios vertės nusidėvėjimas po skaidymo

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomas metodas, kuris naudojamas ilgalaikiam turtui skaičiuojant nusidėvėjimą po to, kai turtas padalintas į kitą turtą, naudojant balanso mažinimo metodą. Turto knygoje sukonfigūruoti nusidėvėjimo metai yra finansiniai metai. Norėdami daugiau informacijos žr. [Balanso nusidėvėjimo mažinimas](reduce-balance-depreciation.md) ir [Ilgalaikio turto skaidymas](tasks/split-fixed-asset.md).

Jei jūs skaidote ilgalaikį turtą per ataskaitinį laikotarpį, kuris yra vėlesnis už turto įsigijimo laikotarpį, sumažintas balanso nusidėvėjimas bus skaičiuojamas pagal praėjusių metų turto balansinę vertę (NBV). Taip pat bus atsižvelgiama į įsigijimo ir nusidėvėjimo nustatymo operacijas, sugeneruotas iš operacijos, kuri skaido turtą. Taip daroma prielaida, kad turtas buvo įsigytas per vienerius finansinius metus ir padalintas į vėlesnius finansinius metus. Suma, kuri turi būti nusidėvėjama pradiniam turtui, kai skaidymas atitinka turto NBV prieš tai, kai turtas buvo suskaidytas, ir pirkimo ir nusidėvėjimo derinimo operacija, užregistruota išskaidyti.

Pavyzdžiui, šios sąlygos galioja.

- Ataskaitinis laikotarpis yra nuo birželio 30 d. iki liepos 1 d.
- Mažėjančios vertės procentas yra 18 proc., o turtas įsigytas 2019 m. birželį, kai įsigijimo kaina buvo 10 000 USD.
- Pirmųjų finansinių metų nusidėvėjimas lygus 18 000 USD, mėnesinis nusidėvėjimas yra lygus 150 USD, o turtas nusidėvimas iki 2019 m. lapkričio, suma – 738,75 USD.
- 2019 m. lapkritį 80 procentų turto išskaidoma į kitą ilgalaikį turtą.

[![Mažėjančios vertės nusidėvėjimas po skaidymo.](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)

Pradinio turto nusidėvėjimo suma yra 1822,25 USD. Ši suma yra lygi NBV prieš registruojant išskaidytą operaciją (9111,25 USD), pridėjus įsigijimo suderinimą, sugeneruotą registruojant skaidymo operaciją (–8000 USD), pridėjus nusidėvėjimo suderinimą, sugeneruotą per išskaidytą operaciją (711 USD). Todėl antraisiais metais nusidėvėjimas yra (1822,25 × 18 proc.) ÷ 12 = 27,33 USD.

Pirmaisiais metais naujo ilgalaikio turto nusidėvėjimo suma yra (8000 × 18 proc.) ÷ 12 = 120 USD.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
