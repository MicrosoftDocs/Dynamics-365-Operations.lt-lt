---
title: REPLACE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama REPLACE elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: c9e64bd8e039b4eeca829c3c37299f002ba03592
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743740"
---
# <a name="replace-er-function"></a>REPLACE ER funkcija

[!include [banner](../includes/banner.md)]

`REPLACE` funkcija grąžina nurodytą teksto eilutę kaip *Eilutės* reikšmę po to, kai visa arba jos dalis buvo pakeista kita eilute.

## <a name="syntax"></a>Sintaksė

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas.

`pattern`: *Eilutė*

Jei `regular expression flag` argumentas yra **KLAIDINGAS**, šiame argumente yra tekstas, kurį reikia pakeisti.

Jei `regular expression flag` argumentas yra **TEISINGAS**, šiame argumente yra įprasta išraiška, apibrėžianti ieškos šabloną ir pakaitinį tekstą.

`replacement`: *Eilutė*

Jei `regular expression flag` argumentas yra **KLAIDINGAS**, šiame argumente yra tekstas, naudotinas kaip pakaitas.

Jei `regular expression flag` argumentas yra **TEISINGAS**, šis argumentas nenaudojamas.

`regular expression flag`: *Bulio logika*

*Bulio logikos* reikšmė, nurodanti, ar pakeitimui atlikti naudojama įprasta išraiška.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Jei `regular expression flag` argumentas yra **TEISINGAS**, ši funkcija grąžina nurodytą eilutę, po to, kai ji buvo pakeista pagal `pattern` argumentui nurodytą įprastą išraišką. Įprasta išraiška naudojama ieškant simbolių, kuriuos reikia pakeisti.

Jei `regular expression flag` argumentas yra **KLAIDINGAS**, ši funkcija grąžina nurodytą eilutę po to, kai simbolių, apibrėžtų `pattern` argumente, rinkinį pakeičia `replacement` argumento simboliai. 

## <a name="example-1"></a>1 pavyzdys

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` pritaiko įprastą išraišką, kuri pašalina visus neskaitinius simbolius ir grąžina **„19234564971“**. 

## <a name="example-2"></a>2 pavyzdys

`REPLACE ("abcdef", "cd", "GH", false)` pakeičia šabloną **„cd“** į eilutę **„GH“** ir grąžinama **„abGHef“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)
