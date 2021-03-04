---
title: MID ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama MID elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 1d8a7d2e9beb0fc8724d26de0acaf1d61e3834c6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680295"
---
# <a name="mid-er-function"></a>MID ER funkcija

[!include [banner](../includes/banner.md)]

`MID` funkcija grąžina *Eilutės* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius iš nurodytos eilutės, pradėdama nuo nurodytos vietos.

## <a name="syntax"></a>Sintaksė

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

*Eilutės* reikšmė, nurodanti tekstą, iš kurio grąžinami simboliai.

`starting position`: *Sveikasis*

*Sveikojo skaičiaus* reikšmė, nurodanti pirmojo simbolio, kuris turi būti grąžinamas iš nurodyto teksto, vietą.

`number of characters`: *Sveikasis*

*Sveikojo skaičiaus* reikšmė, nurodanti simbolių, kurie turi būti grąžinami pradedant nuo nurodytos pradžios vietos, skaičių.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Jei argumento `starting position` reikšmė yra mažesnė už 0 (nulį), grąžinami simboliai skaičiuojami nuo pirmosios nurodytos eilutės vietos.

Jei argumento `starting position` reikšmė viršija nurodytos eilutės ilgį, grąžinama tuščia eilutė.

## <a name="example"></a>Pavyzdys

`MID ("Sample", 2, 3)`grąžina **„amp“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]