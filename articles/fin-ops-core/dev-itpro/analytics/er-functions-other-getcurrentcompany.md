---
title: GETCURRENTCOMPANY ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama GETCURRENTCOMPANY elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 7e3c164c6d54d8387eed5018219da5fd82c765c8
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744131"
---
# <a name="getcurrentcompany-er-function"></a>GETCURRENTCOMPANY ER funkcija 

[!include [banner](../includes/banner.md)]

`GETCURRENTCOMPANY` funkcija grąžina *Eilutės* reikšmę, nurodančią juridinio subjekto (įmonės), prie kurio šiuo metu prisijungęs vartotojas, kodą.

## <a name="syntax"></a>Sintaksė

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="example"></a>Pavyzdys

Vartotojui, prisijungusiam prie įmonės **„Contoso Entertainment System USA“**, `GETCURRENTCOMPANY ()` grąžina **USMF**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kitos (konkrečios verslo srities) funkcijos](er-functions-category-other.md)
