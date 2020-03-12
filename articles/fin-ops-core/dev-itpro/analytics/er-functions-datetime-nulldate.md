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
ms.openlocfilehash: 24a295a6ad8aca7718e60dd351248c9fbfdafee8
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042325"
---
# <span data-ttu-id="a8d85-103"><a name="NULLDATE">ER NULLDATE funkcija</a></span><span class="sxs-lookup"><span data-stu-id="a8d85-103"><a name="NULLDATE">NULLDATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8d85-104">`NULLDATE` funkcija pateikia tipo *Data* reikšmę, kuri nurodo **neapibrėžtą** datą (1900 m. sausio 1 d.).</span><span class="sxs-lookup"><span data-stu-id="a8d85-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="a8d85-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="a8d85-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="a8d85-106">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="a8d85-106">Return values</span></span>

<span data-ttu-id="a8d85-107">*Data*</span><span class="sxs-lookup"><span data-stu-id="a8d85-107">*Date*</span></span>

<span data-ttu-id="a8d85-108">Gauta datos reikšmė.</span><span class="sxs-lookup"><span data-stu-id="a8d85-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="a8d85-109">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="a8d85-109">Example 1</span></span>

<span data-ttu-id="a8d85-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` **neapibrėžtą** datą – 1900 m. sausio 1 d. – pagal nurodytą pasirinktinį formatą pateikia kaip **„1900-01-01“**.</span><span class="sxs-lookup"><span data-stu-id="a8d85-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="a8d85-111">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="a8d85-111">Example 2</span></span>

<span data-ttu-id="a8d85-112">Kai lauko **DocumentDate** reikšmė sutampa su **neapibrėžta** data, reiškinys `IF( Invoice.DocumentDate = NULLDATE(), true, false)` pateikia **True**.</span><span class="sxs-lookup"><span data-stu-id="a8d85-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="a8d85-113">Šiame pavyzdyje **Sąskaita faktūra** yra tipo **Finance/Table records** modulio Elektroninės ataskaitos (ER) duomenų šaltinis, nurodantis lentelę CustInvoiceJour.</span><span class="sxs-lookup"><span data-stu-id="a8d85-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a8d85-114">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="a8d85-114">Additional resources</span></span>

[<span data-ttu-id="a8d85-115">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="a8d85-115">Date and time functions</span></span>](er-functions-category-datetime.md)
