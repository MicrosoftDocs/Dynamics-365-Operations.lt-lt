---
title: CHAR ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CHAR elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 7813b0c6002e47aef6a8c119c72728a49584401b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041238"
---
# <a name="CHAR">CHAR ER funkcija</a>

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

Šios funkcijos grąžinta eilutė priklauso nuo kodavimo, kuris pasirinktas pirminiame formato **FAILAS** elemente. Norėdami matyti palaikomų kodavimų sąrašą, žr. [Kodavimo klasė](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).

## <a name="example"></a>Pavyzdys

`CHAR (255)` grąžina **„ÿ“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)
