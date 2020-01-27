---
title: ISOCREDREF ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama ISOCREDREF elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: ea72d824d3a98d7685a965e981d057991f012a0e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916964"
---
# <a name="ISOCREDREF">ISOCREDREF ER funkcija</a>

[!include [banner](../includes/banner.md)]

`ISOCREDREF` funkcija grąžina *Eilutės* reikšmę, kuri nurodo Tarptautinės standartizacijos organizacijos (ISO) kreditoriaus nuorodą pagal nurodyto SF numerio skaitmenis ir raidinius simbolius.

## <a name="syntax"></a>Sintaksė

```
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a>Argumentai

`invoice number digits`: *Eilutė*

Tekstinė reikšmė, nurodanti sąskaitos faktūros numerio skaitmenis.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

> [!NOTE] 
> Norint iš abėcėlės pašalinti simbolius, kurie nėra suderinami su ISO, `invoice number digits` argumentas turi būti išverstas prieš jį perduodant į šią funkciją.

## <a name="example"></a>Pavyzdys

`ISOCredRef ("VEND-200002")` grąžina **„RF23VEND-200002“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kitos (konkrečios verslo srities) funkcijos](er-functions-category-other.md)
