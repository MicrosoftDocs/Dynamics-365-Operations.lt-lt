---
title: ER FIRSTORNULL funkcija
description: Šioje temoje paaiškinama, kaip naudojama modulio Elektroninės ataskaitos (ER) FIRSTORNULL funkcija
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 53284333507ef1264d3eb66b0c7141eb69f32392
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564630"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="b0229-103">ER FIRSTORNULL funkcija</span><span class="sxs-lookup"><span data-stu-id="b0229-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0229-104">`FIRSTORNULL` funkcija pirmąjį nurodyto sąrašo įrašą pateikia kaip tipo *Konteineris (įrašas)* reikšmę (jei tas įrašas nėra tuščias).</span><span class="sxs-lookup"><span data-stu-id="b0229-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="b0229-105">Jei įrašas tuščias, ši funkcija pateikia neapibrėžtą tipo *Konteineris (įrašas)* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b0229-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0229-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="b0229-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="b0229-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="b0229-107">Arguments</span></span>

<span data-ttu-id="b0229-108">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="b0229-108">`list`: *Record list*</span></span>

<span data-ttu-id="b0229-109">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="b0229-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="b0229-110">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="b0229-110">Return values</span></span>

<span data-ttu-id="b0229-111">*Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="b0229-111">*Container (record)*</span></span>

<span data-ttu-id="b0229-112">Gauta įrašo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="b0229-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="b0229-113">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="b0229-113">Example</span></span>

<span data-ttu-id="b0229-114">Reiškinys `FIRSTORNULL(SPLIT("",1)).Value` pateikia tuščią eilutę (**„“**).</span><span class="sxs-lookup"><span data-stu-id="b0229-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b0229-115">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b0229-115">Additional resources</span></span>

[<span data-ttu-id="b0229-116">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="b0229-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]