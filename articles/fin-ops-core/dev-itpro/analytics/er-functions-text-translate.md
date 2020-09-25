---
title: TRANSLATE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama TRANSLATE elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 51b9a2e25a9f1dfc08e9e0f7fc3ad84b359a6d1b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744244"
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
