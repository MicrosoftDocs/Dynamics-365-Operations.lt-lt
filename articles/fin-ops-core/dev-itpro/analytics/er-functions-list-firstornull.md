---
title: ER FIRSTORNULL funkcija
description: Šioje temoje paaiškinama, kaip naudojama modulio Elektroninės ataskaitos (ER) FIRSTORNULL funkcija
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: e360812c5b0dbfb8df4ab279bf3e0050acebbb25
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745205"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="195a2-103">ER FIRSTORNULL funkcija</span><span class="sxs-lookup"><span data-stu-id="195a2-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="195a2-104">`FIRSTORNULL` funkcija pirmąjį nurodyto sąrašo įrašą pateikia kaip tipo *Konteineris (įrašas)* reikšmę (jei tas įrašas nėra tuščias).</span><span class="sxs-lookup"><span data-stu-id="195a2-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="195a2-105">Jei įrašas tuščias, ši funkcija pateikia neapibrėžtą tipo *Konteineris (įrašas)* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="195a2-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="195a2-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="195a2-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="195a2-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="195a2-107">Arguments</span></span>

<span data-ttu-id="195a2-108">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="195a2-108">`list`: *Record list*</span></span>

<span data-ttu-id="195a2-109">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="195a2-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="195a2-110">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="195a2-110">Return values</span></span>

<span data-ttu-id="195a2-111">*Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="195a2-111">*Container (record)*</span></span>

<span data-ttu-id="195a2-112">Gauta įrašo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="195a2-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="195a2-113">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="195a2-113">Example</span></span>

<span data-ttu-id="195a2-114">Reiškinys `FIRSTORNULL(SPLIT("",1)).Value` pateikia tuščią eilutę (**„“**).</span><span class="sxs-lookup"><span data-stu-id="195a2-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="195a2-115">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="195a2-115">Additional resources</span></span>

[<span data-ttu-id="195a2-116">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="195a2-116">List functions</span></span>](er-functions-category-list.md)
