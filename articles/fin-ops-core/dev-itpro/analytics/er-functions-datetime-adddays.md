---
title: ER ADDDAYS funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) ADDDAYS funkcija.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 998cf2c0dac67040814d4a32e433b465ec51f88c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743380"
---
# <a name="adddays-er-function"></a>ER ADDDAYS funkcija

[!include [banner](../includes/banner.md)]

`ADDDAYS` funkcija apskaičiuoja *DateTime* reikšmę, kuri yra nurodytas dienų skaičius prieš nurodytą pradžios datą arba po jos.

## <a name="syntax"></a>Sintaksė

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>Argumentai

`datetime`: *DateTime*

Datos / laiko reikšmė, nurodanti pradžios datą.

`days`: *Sveikasis skaičius*

Dienų prieš `datetime` arba po jos skaičius.

## <a name="return-values"></a>Pateikiamos reikšmės

*Data ir laikas*

Gauta datos / laiko reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Teigiama `days` reikšmė pateikia būsimą datą. Neigiama reikšmė pateikia praeities datą.

## <a name="example-1"></a>1 pavyzdys

`ADDDAYS (NOW(), 7)` nukelia datą ir laiką septyniomis dienomis į ateitį.

## <a name="example-2"></a>2 pavyzdys

`ADDDAYS (NOW(), -3)` nukelia datą ir laiką trimis dienomis į praeitį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Datos ir laiko funkcijos](er-functions-category-datetime.md)
