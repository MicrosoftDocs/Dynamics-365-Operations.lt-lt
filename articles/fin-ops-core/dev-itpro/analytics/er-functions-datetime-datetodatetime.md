---
title: ER DATETODATETIME funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DATETODATETIME funkcija.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 1e5fa64b776ed2702ac65a2f6416adcf657c748caa1156a71b4c3e99ee188880
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755012"
---
# <a name="datetodatetime-er-function"></a>ER DATETODATETIME funkcija

[!include [banner](../includes/banner.md)]

`DATETODATETIME` funkcija pateikia *DateTime* reikšmę, kuri iš nurodytos datos reikšmės konvertuojama į datos / laiko reikšmę universaliojo laiko (Grinvičo laiko \[GMT\]) formatu.

## <a name="syntax"></a>Sintaksė

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a>Argumentai

`date`: *Data*

Datos reikšmė, nurodanti konvertavimo datą.

## <a name="return-values"></a>Pateikiamos reikšmės

*Data ir laikas*

Gauta datos / laiko reikšmė.

## <a name="example-1"></a>1 pavyzdys

`DATETODATETIME (CompInfo. 'getCurrentDate()')` dabartinio „Microsoft Dynamics 365 Finance“ seanso datą – 2015 m. gruodžio 24 d. – pateikia kaip **12/24/2015 12:00:00 AM**. Šiame pavyzdyje **CompInfo** yra tipo **„Finance and Operations” / Lentelė** modulio Elektroninės ataskaitos (ER) duomenų šaltinis, nurodantis lentelę CompanyInfo.

## <a name="example-2"></a>2 pavyzdys

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` pateikia datos / laiko reikšmę **11/12/2019 12:00:00 AM**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Datos ir laiko funkcijos](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]