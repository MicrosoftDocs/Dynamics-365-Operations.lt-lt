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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3cd4c152d4e220a2f6315265ed5e44d148134279
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042267"
---
# <a name="NULLDATETIME">ER NULLDATETIME funkcija</a>

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
