---
title: Nusidėvėjimo skaičiavimų apvalinimo suma
description: Šiame straipsnyje aptariamas laukas Suapvalinti nusidėvėjimą, kurį galima rasti puslapyje Knygos nustatymas.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d3df48fc7bb092b0257c4652a8c67d1d740dbcfe
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674338"
---
# <a name="round-off-amount-for-depreciation-calculations"></a>Nusidėvėjimo skaičiavimų apvalinimo suma

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aptariamas **Nusidėvėjimo suapvalinimo** laukas, kurį galima rasti **Knygos nustatymas** puslapiuose.

Nusidėvėjimo sumų apvalinimas nustatomas kiekvienai knygai. Nusidėvėjimo sumų apvalinimas naudojamas ilgalaikio turto nusidėvėjimo profilyje, kuris rodo būsimą ilgalaikio turto nusidėvėjimą ir vertę, ir yra rodomas nusidėvėjimo pasiūlymuose. Įveskite žemiausią leidžiamą knygos nusidėvėjimo sumą. 

Neatsižvelgiant į nustatytą apvalinimą, paskutinio nusidėvėjimo laikotarpio nusidėvėjimo suma nėra suapvalinama. Paskutinio nusidėvėjimo laikotarpio pabaigoje, ilgalaikio turto vertė turi būti 0 (nulis) arba likvidacinė vertė, jei likvidacinė vertė naudojama.

### <a name="example"></a>Pavyzdys

Apskaičiuotas nusidėvėjimas be apvalinimo yra 2444,44. Kaip parodyta toliau pateikiamoje lentelėje, siūlomos sumos skiriasi, atsižvelgiant į tai, kaip apvalinimas nustatytas.

| Apvalinimo metodas | Nusidėvėjimo suma |
|-----------------|---------------------|
| Apvalinimas 0,1    | 2,444.40            |
| Apvalinimas 1,00   | 2,444.00            |
| Apvalinimas 10,00  | 2,440.00            |
| Apvalinimas 100,00 | 2,400.00            |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
