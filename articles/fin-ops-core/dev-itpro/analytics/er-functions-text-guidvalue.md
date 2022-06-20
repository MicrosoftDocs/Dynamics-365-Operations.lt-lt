---
title: GUIDVALUE ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama GUIDVALUE elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f3899d983f7c790ff2e3dc74dd91c44fc54e44d3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898746"
---
# <a name="guidvalue-er-function"></a>GUIDVALUE ER funkcija

[!include [banner](../includes/banner.md)]

`GUIDVALUE` funkcija konvertuoja nurodytą *Eilutės* tipo įvestį į duomenų elementą, kurio duomenų tipas *GUID*.

## <a name="syntax"></a>Sintaksė

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a>Argumentai

`input`: *Eilutė*

Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas.

## <a name="return-values"></a>Grįžties vertės

*GUID*

Gaunama globaliai unikalaus identifikatoriaus (GUID) reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Norėdami atlikti konvertavimą priešinga kryptimi (t. y. nurodytą duomenų tipo *GUID* įvestį konvertuoti į duomenų tipo *Eilutė* duomenų elementą), galite naudotis funkcija [TEXT()](er-functions-text-text.md).

## <a name="example"></a>Pavyzdys

Apibrėžkite šiuos modelio susiejimo duomenų šaltinius:

- Duomenų šaltinis **myID**, kuris priklauso tipui *Apskaičiuojamas laukas* ir turi išraišką `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`
- Duomenų šaltinis **Vartotojai**, kuris priklauso tipui *Lentelės įrašai* ir susijęs su lentele „UserInfo“

Tada galite naudoti išraišką, pvz. `FILTER (Users, Users.objectId = myID)`, filtruoti lentelę „UserInfo“ pagal lauką **objectId**, priklausantį duomenų tipui *GUID*.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]