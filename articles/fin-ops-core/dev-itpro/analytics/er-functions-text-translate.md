---
title: TRANSLATE ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama TRANSLATE elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 7a15a28f6efa5333b54aa34938d22a9d6e404cec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278448"
---
# <a name="translate-er-function"></a>TRANSLATE ER funkcija

[!include [banner](../includes/banner.md)]

`TRANSLATE` funkcija grąžina *Eilutės* reikšmę, kurioje pateikiamas kito pateikto rinkinio nurodyto teksto simbolių pakeitimas.

## <a name="syntax"></a>Sintaksė

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas.

`pattern`: *Eilutė*

Tekstas, kuris turi būti pakeistas.

`replacement`: *Eilutė*

Tekstas, kurį norite naudoti kaip pakaitą.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

`TRANSLATE` funkcija vienu metu pakeičia vieną simbolį. Funkcija pakeičia pirmą `text` argumento simbolį pirmu `pattern` argumento simboliu, tada pakeičia antrą simbolį ir naudoja tokią pačią gamybos eigą, kol užbaigia darbą. Kai `text` ir `pattern` argumentų simboliai sutampa, jie pakeičiami `replacement` argumento simboliu, kuris yra tokioje pačioje vietoje kaip ir `pattern` argumento simbolis. Jei `pattern` argumente simbolis rodomas kelis kartus, naudojamas `replacement` argumento susiejimas, atitinkantis pirmą šio simbolio atvejį.

## <a name="example-1"></a>1 pavyzdys

`TRANSLATE ("abcdef", "cd", "GH")` pakeičia nurodyto teksto **„abcdef”** simbolį **c** `replacement` teksto simboliu **G** dėl toliau pateiktų priežasčių.
-   Simbolis **c** pateikiamas pirmoje `pattern` teksto vietoje.
-   Pirmoje `replacement` teksto vietoje yra simbolis **G**.

## <a name="example-2"></a>2 pavyzdys

`TRANSLATE ("abcdef", "ccd", "GH")` grąžina **„abGdef“**.

## <a name="example-3"></a>3 pavyzdys

`TRANSLATE ("abccba", "abc", "123")` grąžina **„123321“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
