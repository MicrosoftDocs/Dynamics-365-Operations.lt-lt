---
title: ER COUNT funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) COUNT funkcija.
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
ms.openlocfilehash: 72d2ea1b26c295c97575a3c7a479ee4e06762424
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042210"
---
# <a name="COUNT">ER COUNT funkcija</a>

[!include [banner](../includes/banner.md)]

`COUNT` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią konkretaus sąrašo įrašų skaičių (jei sąrašas nėra tuščias). Jei sąrašas tuščias, ši funkcija pateikia **0** (nulį).

## <a name="syntax"></a>Sintaksė

```vb
COUNT (list)
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

## <a name="return-values"></a>Pateikiamos reikšmės

*Sveikasis skaičius*

Gaunama skaitinė reikšmė.

## <a name="example"></a>Pavyzdys

`COUNT (SPLIT("abcd" , 3))` pateikia **2**, nes šiame pavyzdyje naudojama `SPLIT` funkcija sukuria sąrašą, sudarytą iš dviejų įrašų.

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)
