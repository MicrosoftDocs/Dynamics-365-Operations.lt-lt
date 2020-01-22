---
title: ER NULLDATE funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) NULLDATE funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 7761342c6759c11591e06fc7c32f0ddd8bef407a
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916320"
---
# <a name="NULLDATE">ER NULLDATE funkcija</a>

[!include [banner](../includes/banner.md)]

`NULLDATE` funkcija pateikia tipo *Data* reikšmę, kuri nurodo **neapibrėžtą** datą (1900 m. sausio 1 d.).

## <a name="syntax"></a>Sintaksė

```
NULLDATE () as 
```

## <a name="return-values"></a>Pateikiamos reikšmės

*Data*

Gauta datos reikšmė.

## <a name="example-1"></a>1 pavyzdys

`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` **neapibrėžtą** datą – 1900 m. sausio 1 d. – pagal nurodytą pasirinktinį formatą pateikia kaip **„1900-01-01“**.

## <a name="example-2"></a>2 pavyzdys

Kai lauko **DocumentDate** reikšmė sutampa su **neapibrėžta** data, reiškinys `IF( Invoice.DocumentDate = NULLDATE(), true, false)` pateikia **True**. Šiame pavyzdyje **Sąskaita faktūra** yra tipo **Finance/Table records** modulio Elektroninės ataskaitos (ER) duomenų šaltinis, nurodantis lentelę CustInvoiceJour.

## <a name="additional-resources"></a>Papildomi ištekliai

[Datos ir laiko funkcijos](er-functions-category-datetime.md)
