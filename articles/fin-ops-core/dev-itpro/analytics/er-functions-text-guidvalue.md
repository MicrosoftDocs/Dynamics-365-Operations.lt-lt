---
title: GUIDVALUE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama GUIDVALUE elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be5e8e7625d0226c9eb59efd3217fce7b8eba086
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915699"
---
# <a name="GUIDVALUE">GUIDVALUE ER funkcija</a>

[!include [banner](../includes/banner.md)]

`GUIDVALUE` funkcija konvertuoja nurodytą *Eilutės* tipo įvestį į duomenų elementą, kurio duomenų tipas *GUID*.

## <a name="syntax"></a>Sintaksė

```
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