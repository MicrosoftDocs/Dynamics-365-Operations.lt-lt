---
title: ER DATETODATETIME funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DATETODATETIME funkcija.
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
ms.openlocfilehash: eac09c9b410815ad9ae71dec53fc0416b020ca1e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744820"
---
# <a name="datetodatetime-er-function"></a><span data-ttu-id="e04d8-103">ER DATETODATETIME funkcija</span><span class="sxs-lookup"><span data-stu-id="e04d8-103">DATETODATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e04d8-104">`DATETODATETIME` funkcija pateikia *DateTime* reikšmę, kuri iš nurodytos datos reikšmės konvertuojama į datos / laiko reikšmę universaliojo laiko (Grinvičo laiko \[GMT\]) formatu.</span><span class="sxs-lookup"><span data-stu-id="e04d8-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="e04d8-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="e04d8-105">Syntax</span></span>

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="e04d8-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="e04d8-106">Arguments</span></span>

<span data-ttu-id="e04d8-107">`date`: *Data*</span><span class="sxs-lookup"><span data-stu-id="e04d8-107">`date`: *Date*</span></span>

<span data-ttu-id="e04d8-108">Datos reikšmė, nurodanti konvertavimo datą.</span><span class="sxs-lookup"><span data-stu-id="e04d8-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="e04d8-109">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="e04d8-109">Return values</span></span>

<span data-ttu-id="e04d8-110">*Data ir laikas*</span><span class="sxs-lookup"><span data-stu-id="e04d8-110">*DateTime*</span></span>

<span data-ttu-id="e04d8-111">Gauta datos / laiko reikšmė.</span><span class="sxs-lookup"><span data-stu-id="e04d8-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="e04d8-112">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e04d8-112">Example 1</span></span>

<span data-ttu-id="e04d8-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` dabartinio „Microsoft Dynamics 365 Finance“ seanso datą – 2015 m. gruodžio 24 d. – pateikia kaip **12/24/2015 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="e04d8-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="e04d8-114">Šiame pavyzdyje **CompInfo** yra tipo **„Finance and Operations” / Lentelė** modulio Elektroninės ataskaitos (ER) duomenų šaltinis, nurodantis lentelę CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="e04d8-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="e04d8-115">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e04d8-115">Example 2</span></span>

<span data-ttu-id="e04d8-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` pateikia datos / laiko reikšmę **11/12/2019 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="e04d8-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e04d8-117">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e04d8-117">Additional resources</span></span>

[<span data-ttu-id="e04d8-118">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="e04d8-118">Date and time functions</span></span>](er-functions-category-datetime.md)
