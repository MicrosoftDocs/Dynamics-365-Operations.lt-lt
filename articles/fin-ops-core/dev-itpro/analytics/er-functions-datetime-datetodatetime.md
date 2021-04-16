---
title: ER DATETODATETIME funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DATETODATETIME funkcija.
author: NickSelin
ms.date: 12/04/2019
ms.topic: article
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
ms.openlocfilehash: bb90c58544eeba804cd39542cc70fab3b840af80
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746968"
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