---
title: TRIM ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama TRIM elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 02/28/2022
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
ms.openlocfilehash: 95b8d2989d705c4998da0af8e683adf567edfe92
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273105"
---
# <a name="trim-er-function"></a>TRIM ER funkcija

[!include [banner](../includes/banner.md)]

Funkcija `TRIM` grąžina *nurodytą* teksto eilutę kaip eilutės vertę po skirtuko, grąžinimas, eilučių tiektuvas ir formos tiektuvo simboliai buvo pakeisti vienu tarpo simboliu, po to, kai sutrumpinti priekiniai ir galiiniai tarpai ir po kelių tarpų.

## <a name="syntax"></a>Sintaksė

```vb
TRIM (text)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas.

## <a name="return-values"></a>Grįžimo vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Kai kuriais atvejais galite norėti sutrumpinti priekinius ir gali būti mažiau tarpus, bet labiau norite toliau formatuoti nurodytą tekstą. Pavyzdžiui, kai šis tekstas nurodo adresą, kurį galima įvesti į kelių eilučių teksto lauką, ir jame gali būti eilutės tiektuvo ir eilutės grąžinimo grąžos formatavimas. Šiuo atveju naudokite šią išraišką: `REPLACE(text,"^[ \t]+|[ \t]+$","", true)` čia yra `text` argumentas, nurodantis nurodytą teksto eilutę.

## <a name="example-1"></a>1 pavyzdys

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` grąžina **„Teksto pavyzdys“**.

## <a name="example-2"></a>2 pavyzdys

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` pateikia **"Pavyzdžio tekstas"**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)

[REPLACE ER funkcija](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
