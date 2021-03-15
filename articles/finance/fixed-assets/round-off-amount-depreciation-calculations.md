---
title: Nusidėvėjimo skaičiavimų apvalinimo suma
description: Šiame straipsnyje aptariamas laukas Suapvalinti nusidėvėjimą, kurį galima rasti puslapyje Knygos nustatymas.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01c8662f0731abd089c9039c16bb77e39c1d3e51
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976021"
---
# <a name="round-off-amount-for-depreciation-calculations"></a>Nusidėvėjimo skaičiavimų apvalinimo suma

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aptariamas laukas Suapvalinti nusidėvėjimą, kurį galima rasti puslapyje Knygos nustatymas.

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