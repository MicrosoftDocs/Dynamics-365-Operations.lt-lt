---
title: ER NULLDATETIME funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) NULLDATETIME funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 65e9ef92dc30e46c297d93e262bad8878df47a0c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682298"
---
# <a name="nulldatetime-er-function"></a>ER NULLDATETIME funkcija

[!include [banner](../includes/banner.md)]

`NULLDATETIME` funkcija pateikia *DateTime* reikšmę, kuri nurodo **neapibrėžtą** datos / laiko reikšmę (1900 m. sausio 1 d.) universaliojo laiko (Grinvičo \[GMT\] laiko) formatu.

## <a name="syntax"></a>Sintaksė

```vb
NULLDATETIME ()
```

## <a name="return-values"></a>Pateikiamos reikšmės

*Data ir laikas*

Gauta datos / laiko reikšmė.

## <a name="example"></a>Pavyzdys

`DATETIMEFORMAT( NULLDATETIME(), "O")` pateikia eilutės reikšmę **1900-01-01T00:00:00.0000000+00:00**, kai ji iškviečiama vykdant procesą, kurį inicijavo programos vartotojas, skyriuje **Kalba ir šalies / regiono nuostatos** pasirinkęs laiko juostos reikšmę **(GMT) universalusis laikas**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Datos ir laiko funkcijos](er-functions-category-datetime.md)
