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
ms.openlocfilehash: d6e5d025e7de15c27b19711ea5b597d75bdf3d41
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744100"
---
# <a name="isocredref-er-function"></a>ISOCREDREF ER funkcija

[!include [banner](../includes/banner.md)]

`ISOCREDREF` funkcija grąžina *Eilutės* reikšmę, kuri nurodo Tarptautinės standartizacijos organizacijos (ISO) kreditoriaus nuorodą pagal nurodyto SF numerio skaitmenis ir raidinius simbolius.

## <a name="syntax"></a>Sintaksė

```vb
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
