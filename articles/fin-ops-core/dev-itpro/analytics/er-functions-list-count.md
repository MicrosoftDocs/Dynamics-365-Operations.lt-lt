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
ms.openlocfilehash: 2d29b82a8c3b108f7651e6d593cb17e7ec8ca872
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916251"
---
# <span data-ttu-id="d59dc-103"><a name="COUNT">ER COUNT funkcija</a></span><span class="sxs-lookup"><span data-stu-id="d59dc-103"><a name="COUNT">COUNT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d59dc-104">`COUNT` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią konkretaus sąrašo įrašų skaičių (jei sąrašas nėra tuščias).</span><span class="sxs-lookup"><span data-stu-id="d59dc-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="d59dc-105">Jei sąrašas tuščias, ši funkcija pateikia **0** (nulį).</span><span class="sxs-lookup"><span data-stu-id="d59dc-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="d59dc-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="d59dc-106">Syntax</span></span>

```
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="d59dc-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="d59dc-107">Arguments</span></span>

<span data-ttu-id="d59dc-108">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="d59dc-108">`list`: *Record list*</span></span>

<span data-ttu-id="d59dc-109">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="d59dc-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d59dc-110">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="d59dc-110">Return values</span></span>

<span data-ttu-id="d59dc-111">*Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="d59dc-111">*Integer*</span></span>

<span data-ttu-id="d59dc-112">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="d59dc-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="d59dc-113">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="d59dc-113">Example</span></span>

<span data-ttu-id="d59dc-114">`COUNT (SPLIT("abcd" , 3))` pateikia **2**, nes šiame pavyzdyje naudojama `SPLIT` funkcija sukuria sąrašą, sudarytą iš dviejų įrašų.</span><span class="sxs-lookup"><span data-stu-id="d59dc-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d59dc-115">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d59dc-115">Additional resources</span></span>

[<span data-ttu-id="d59dc-116">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="d59dc-116">List functions</span></span>](er-functions-category-list.md)
