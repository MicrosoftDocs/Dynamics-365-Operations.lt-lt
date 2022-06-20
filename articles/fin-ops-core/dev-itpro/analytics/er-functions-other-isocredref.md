---
title: ISOCREDREF ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama ISOCREDREF Electronic Reporting (ER) funkcija.
author: NickSelin
ms.date: 12/17/2019
ms.prod: ''
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
ms.openlocfilehash: dcbd53ec1939e6fb4bcd829bad01b353e823795a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896769"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]