---
title: ER COUNT funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) COUNT funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: e36347d928148e85bc9295d529cbf2801946433a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567897"
---
# <a name="count-er-function"></a><span data-ttu-id="d3327-103">ER COUNT funkcija</span><span class="sxs-lookup"><span data-stu-id="d3327-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3327-104">`COUNT` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią konkretaus sąrašo įrašų skaičių (jei sąrašas nėra tuščias).</span><span class="sxs-lookup"><span data-stu-id="d3327-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="d3327-105">Jei sąrašas tuščias, ši funkcija pateikia **0** (nulį).</span><span class="sxs-lookup"><span data-stu-id="d3327-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3327-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="d3327-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="d3327-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="d3327-107">Arguments</span></span>

<span data-ttu-id="d3327-108">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="d3327-108">`list`: *Record list*</span></span>

<span data-ttu-id="d3327-109">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="d3327-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d3327-110">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="d3327-110">Return values</span></span>

<span data-ttu-id="d3327-111">*Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="d3327-111">*Integer*</span></span>

<span data-ttu-id="d3327-112">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="d3327-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="d3327-113">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="d3327-113">Example</span></span>

<span data-ttu-id="d3327-114">`COUNT (SPLIT("abcd" , 3))` pateikia **2**, nes šiame pavyzdyje naudojama `SPLIT` funkcija sukuria sąrašą, sudarytą iš dviejų įrašų.</span><span class="sxs-lookup"><span data-stu-id="d3327-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3327-115">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d3327-115">Additional resources</span></span>

[<span data-ttu-id="d3327-116">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="d3327-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]