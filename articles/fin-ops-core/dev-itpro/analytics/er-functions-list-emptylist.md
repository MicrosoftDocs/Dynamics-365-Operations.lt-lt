---
title: ER EMPTYLIST funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) EMPTYLIST funkcija.
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
ms.openlocfilehash: 747b661d0dee4e9c27741e167c89f9ef7eefa470
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745326"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="67889-103">ER EMPTYLIST funkcija</span><span class="sxs-lookup"><span data-stu-id="67889-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67889-104">`EMPTYLIST` funkcija pateikia tuščią tipo *Įrašų sąrašas* reikšmę, kaip sąrašo struktūros šaltinį naudodama nurodytą sąrašą.</span><span class="sxs-lookup"><span data-stu-id="67889-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="67889-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="67889-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="67889-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="67889-106">Arguments</span></span>

<span data-ttu-id="67889-107">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="67889-107">`list`: *Record list*</span></span>

<span data-ttu-id="67889-108">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="67889-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="67889-109">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="67889-109">Return values</span></span>

<span data-ttu-id="67889-110">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="67889-110">*Record list*</span></span>

<span data-ttu-id="67889-111">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="67889-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="67889-112">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="67889-112">Example</span></span>

<span data-ttu-id="67889-113">`EMPTYLIST (SPLIT ("abc", 1))` pateikia naują tuščią sąrašą, kuris yra tokios pačios struktūros, kaip ir sąrašas, kurį pateikia naudojama `SPLIT` funkcija.</span><span class="sxs-lookup"><span data-stu-id="67889-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67889-114">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="67889-114">Additional resources</span></span>

[<span data-ttu-id="67889-115">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="67889-115">List functions</span></span>](er-functions-category-list.md)
