---
title: ER LIST funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama SĄRAŠO elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 7a5f27baa248ec84c75725cf32a1f482841424c2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277639"
---
# <a name="list-er-function"></a>ER LIST funkcija

[!include [banner](../includes/banner.md)]

`LIST` funkcija pateikia tipo *Įrašų sąrašas* reikšmę, sudarytą iš naujo įrašų sąrašo, sukurto iš nurodytų argumentų.

## <a name="syntax"></a>Sintaksė

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a>Argumentai

`record 1`: *Konteineris (įrašas)*

Nuoroda į duomenų tipo *Įrašas* duomenų šaltinį. Šis argumentas yra būtinas.

`record N`: *Konteineris (įrašas)*

Nuoroda į duomenų tipo *Įrašas* duomenų šaltinį. Šie papildomi argumentai yra pasirinktiniai.

## <a name="return-values"></a>Pateikiamos reikšmės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="usage-notes"></a>Naudojimo pastabos

Sukurto sąrašo struktūroje yra tik tie laukai, kurie pateikiami kiekvieno argumentuose paminėto įrašo struktūroje.

## <a name="example"></a>Pavyzdys

Įvedate tipo *Konteineris* duomenų šaltinį **1-asis įrašas**. Šiame duomenų šaltinyje yra tolesni įdėtieji tipo *Apskaičiuotasis laukas* laukai.

- **Kodas.** Šiame lauke yra reiškinys, pateikiantis tipo *Eilutė* reikšmę.
- **Suma.** Šiame lauke yra reiškinys, pateikiantis tipo *Realusis skaičius* reikšmę.

Tada įvedate tipo *Konteineris* duomenų šaltinį **2-asis įrašas**. Šiame duomenų šaltinyje yra tolesni įdėtieji tipo *Apskaičiuotasis laukas* laukai.

- **Suma.** Šiame lauke yra reiškinys, pateikiantis tipo *Realusis skaičius* reikšmę.
- **IsValid.** Šiame lauke yra reiškinys, pateikiantis tipo *Bulio logika* reikšmę.

Šiuo atveju reiškinys `LIST('Record 1', 'Record 2')` pateikia naują sąrašą, kuriame yra du įrašai. Šio sąrašo struktūrą sudaro vienas tipo *Realusis skaičius* laukas **Suma**, nes šis laukas yra vienintelis laukas, pateikiamas kiekviename iškviestos funkcijos argumente.

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
