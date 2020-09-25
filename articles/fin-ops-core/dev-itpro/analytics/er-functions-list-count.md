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
ms.openlocfilehash: c48483a6677aaeb36eac57a57cec71bf54c7991d
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745350"
---
# <a name="count-er-function"></a><span data-ttu-id="bd141-103">ER COUNT funkcija</span><span class="sxs-lookup"><span data-stu-id="bd141-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd141-104">`COUNT` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią konkretaus sąrašo įrašų skaičių (jei sąrašas nėra tuščias).</span><span class="sxs-lookup"><span data-stu-id="bd141-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="bd141-105">Jei sąrašas tuščias, ši funkcija pateikia **0** (nulį).</span><span class="sxs-lookup"><span data-stu-id="bd141-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="bd141-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="bd141-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="bd141-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="bd141-107">Arguments</span></span>

<span data-ttu-id="bd141-108">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="bd141-108">`list`: *Record list*</span></span>

<span data-ttu-id="bd141-109">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="bd141-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="bd141-110">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="bd141-110">Return values</span></span>

<span data-ttu-id="bd141-111">*Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="bd141-111">*Integer*</span></span>

<span data-ttu-id="bd141-112">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="bd141-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="bd141-113">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="bd141-113">Example</span></span>

<span data-ttu-id="bd141-114">`COUNT (SPLIT("abcd" , 3))` pateikia **2**, nes šiame pavyzdyje naudojama `SPLIT` funkcija sukuria sąrašą, sudarytą iš dviejų įrašų.</span><span class="sxs-lookup"><span data-stu-id="bd141-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bd141-115">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="bd141-115">Additional resources</span></span>

[<span data-ttu-id="bd141-116">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="bd141-116">List functions</span></span>](er-functions-category-list.md)
