---
title: CHAR ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CHAR elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: e422ccc406e919b2191f4bccb1ac8198bba84b09e9f01f6971876e2c6507d6d3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754371"
---
# <a name="char-er-function"></a>CHAR ER funkcija

[!include [banner](../includes/banner.md)]

`CHAR` funkcija grąžina *Eilutės* reikšmę, kuri pateikia vieną simbolį, kurį nurodo nurodytas „Unicode“ numeris.

## <a name="syntax"></a>Sintaksė

```vb
CHAR (number)
```

## <a name="arguments"></a>Argumentai

`number`: *Sveikasis*

Skaičius, atitinkantis numatomą vieną simbolį.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Šios funkcijos grąžinta eilutė priklauso nuo kodavimo, kuris pasirinktas pirminiame formato **FAILAS** elemente. Norėdami matyti palaikomų kodavimų sąrašą, žr. [Kodavimo klasė](/dotnet/api/system.text.encoding).

## <a name="example"></a>Pavyzdys

`CHAR (255)` grąžina **„ÿ“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]