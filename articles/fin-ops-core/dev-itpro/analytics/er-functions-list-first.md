---
title: ER FIRST funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) FIRST funkcija.
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
ms.openlocfilehash: 4d10abcf15b93961bd2ba4aec22914825d9ac38c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042095"
---
# <span data-ttu-id="15c4e-103"><a name="FIRST">ER FIRST funkcija</a></span><span class="sxs-lookup"><span data-stu-id="15c4e-103"><a name="FIRST">FIRST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15c4e-104">`FIRST` funkcija pirmąjį nurodyto sąrašo įrašą pateikia kaip tipo *Konteineris (įrašas)* reikšmę (jei tas sąrašas nėra tuščias).</span><span class="sxs-lookup"><span data-stu-id="15c4e-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="15c4e-105">Jei sąrašas tuščias, ši funkcija pateikia išimtį.</span><span class="sxs-lookup"><span data-stu-id="15c4e-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="15c4e-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="15c4e-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="15c4e-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="15c4e-107">Arguments</span></span>

<span data-ttu-id="15c4e-108">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="15c4e-108">`list`: *Record list*</span></span>

<span data-ttu-id="15c4e-109">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="15c4e-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="15c4e-110">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="15c4e-110">Return values</span></span>

<span data-ttu-id="15c4e-111">*Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="15c4e-111">*Container (record)*</span></span>

<span data-ttu-id="15c4e-112">Gauta įrašo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="15c4e-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="15c4e-113">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="15c4e-113">Example 1</span></span>

<span data-ttu-id="15c4e-114">Reiškinys `FIRST(SPLIT("ABC",1)).Value` pateikia teksto reikšmę **„A“**.</span><span class="sxs-lookup"><span data-stu-id="15c4e-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="15c4e-115">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="15c4e-115">Example 2</span></span>

<span data-ttu-id="15c4e-116">Vykdomas reiškinys `FIRST(SPLIT("",1)).Value` pateikia išimtį.</span><span class="sxs-lookup"><span data-stu-id="15c4e-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15c4e-117">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="15c4e-117">Additional resources</span></span>

[<span data-ttu-id="15c4e-118">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="15c4e-118">List functions</span></span>](er-functions-category-list.md)
