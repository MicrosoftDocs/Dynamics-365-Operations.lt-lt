---
title: JSONVALUE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama JSONVALUE elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 75f20632074cb4dead98991fd6522ab9b20b9965
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041235"
---
# <a name="JSONVALUE">JSONVALUE ER funkcija</a>

[!include [banner](../includes/banner.md)]

`JSONVALUE` funkcija analizuojami duomenys „JavaScript Object Notation“ (JSON) formatu, kuris pasiekiamas nurodytu keliu bei norint išskleisti skaliarinę vertę, turinčią nurodytą ID. Tada grąžinama išskleista skaliarinė reikšmė kaip *Eilutės* reikšmė.

## <a name="syntax"></a>Sintaksė

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Argumentai

`input`: *Eilutė*

Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas, kuriame yra JSON duomenų.

`path`: *Eilutė*

Skaliarinės reikšmės JSON duomenų identifikatorius.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="example"></a>Pavyzdys

Duomenų šaltinyje **JsonField** yra toliau nurodyti duomenys JSON formatu: **{„BuildNumber“:„7.3.1234.1“, „KeyThumbprint“:„7366E“}**. Tokiu atveju išraiška `JSONVALUE (JsonField, "BuildNumber")` grąžina šią *Eilutės* duomenų tipo reikšmę: **„7.3.1234.1“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)
