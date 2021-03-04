---
title: ER SESSIONTODAY funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) SESSIONTODAY funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 87e8d5498c82d7c9ca6ee0a855f139dde77d75ab
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683824"
---
# <a name="sessiontoday-er-function"></a>ER SESSIONTODAY funkcija

[!include [banner](../includes/banner.md)]

`SESSIONTODAY` funkcija pateikia tipo *Data* reikšmę, kuri nurodo dabartinę programos seanso datą.

## <a name="syntax"></a>Sintaksė

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a>Pateikiamos reikšmės

*Data*

Gauta datos reikšmė.

## <a name="example"></a>Pavyzdys

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` pagal pasirinktą Vokietijos kultūrą ir nurodytą formatą pateikia dabartinę programos seanso datą – 2015 m. gruodžio 24 d. – kaip eilutę **24-12-2015**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Datos ir laiko funkcijos](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]