---
title: ER VALUE funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip modulio Elektroninės ataskaitos (ER) VALUE funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: c90772ca1e93500ac45cc52ba92d4169c4d29bad
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042624"
---
# <a name="VALUE">ER VALUE funkcija</a>

[!include [banner](../includes/banner.md)]

`VALUE` funkcija pateikia tipo *Realusis skaičius* reikšmę, konvertuotą iš nurodytos eilutės.

## <a name="syntax"></a>Sintaksė

```vb
VALUE (text)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

Eilutės reikšmė, kurią reikia konvertuoti į skaitinę reikšmę.

## <a name="return-values"></a>Pateikiamos reikšmės

*Tikrasis*

Gaunama skaitinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Kableliai ir taško simboliai (.) laikomi dešimtainiais skyrikliais, o prieš skaičių rašomas brūkšnelis (-) naudojamas kaip neigiamas ženklas. Jei nurodytoje eilutėje yra kitų neskaitinių simbolių, vykdant pateikiama išimtis.

## <a name="example-1"></a>1 pavyzdys

`VALUE ("1 234,56")` pateikia išimtį.

## <a name="example-2"></a>2 pavyzdys

`VALUE ("1234,56")` pateikia **1234,56**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tipų konvertavimo funkcijos](er-functions-category-type-conversion.md)
