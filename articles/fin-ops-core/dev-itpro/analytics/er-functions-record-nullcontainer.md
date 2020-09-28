---
title: NULLCONTAINER ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama NULLCONTAINER elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: dac6283ec35d3d03f586ca157048bd3ecc4bfa8a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743932"
---
# <a name="nullcontainer-er-function"></a>NULLCONTAINER ER funkcija

[!include [banner](../includes/banner.md)]

`NULLCONTAINER` funkcija grąžina nulinę *konteinerio (įrašo)* reikšmę, kurios struktūra yra tokia pati kaip nurodyto įrašų sąrašo arba įrašo.

## <a name="syntax"></a>Sintaksė

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas* arba *Konteineris (įrašas)*

Tinkamas *Įrašų sąrašo* arba *Konteinerio (įrašo)* tipo duomenų šaltinio maršrutas.

## <a name="return-values"></a>Grįžties vertės

*Konteineris (įrašas)*

Gauta įrašo reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

> [!NOTE] 
> Ši funkcija nebenaudojama. Naudokite `EMPTYRECORD` funkciją kaip pakaitą. Daugiau informacijos žr. [EMPTYRECORD](er-functions-record-emptyrecord.md).

## <a name="example"></a>Pavyzdys

`NULLCONTAINER (SPLIT ("abc", 1))` grąžina naują tuščią įrašą, kuris yra tokios pačios struktūros kaip ir sąrašas, kurį grąžina `SPLIT` funkcija. Daugiau informacijos žr. [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Įrašo funkcijos](er-functions-category-record.md)
