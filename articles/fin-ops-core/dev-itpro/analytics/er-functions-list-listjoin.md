---
title: LISTJOIN ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama LISTJOIN elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249040"
---
# <a name=""></a><span data-ttu-id="48380-103"><a name="LISTJOIN">LISTJOIN ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="48380-103"><a name="LISTJOIN">LISTJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48380-104">`LISTJOIN` funkcija pateikia tipo *Įrašų sąrašas* reikšmę, nurodančią naują jungtinį įrašų sąrašą, sukurtą iš nurodytų argumentų.</span><span class="sxs-lookup"><span data-stu-id="48380-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="48380-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="48380-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="48380-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="48380-106">Arguments</span></span>

<span data-ttu-id="48380-107">`list 1`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="48380-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="48380-108">Nuoroda į duomenų tipo *Įrašų sąrašas* duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="48380-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="48380-109">Šis argumentas yra privalomas.</span><span class="sxs-lookup"><span data-stu-id="48380-109">This argument is mandatory.</span></span>

<span data-ttu-id="48380-110">`list N`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="48380-110">`list N`: *Record list*</span></span>

<span data-ttu-id="48380-111">Nuoroda į duomenų tipo *Įrašų sąrašas* duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="48380-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="48380-112">Šie papildomi argumentai yra pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="48380-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="48380-113">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="48380-113">Return values</span></span>

<span data-ttu-id="48380-114">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="48380-114">*Record list*</span></span>

<span data-ttu-id="48380-115">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="48380-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="48380-116">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="48380-116">Usage notes</span></span>

<span data-ttu-id="48380-117">Sukurto sąrašo struktūroje yra tik tie laukai, kurie pateikiami kiekvieno argumentuose nurodyto įrašų sąrašo struktūroje.</span><span class="sxs-lookup"><span data-stu-id="48380-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="48380-118">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="48380-118">Example</span></span>

<span data-ttu-id="48380-119">Įvedate tipo `Container` duomenų šaltinį **1-asis įrašas**.</span><span class="sxs-lookup"><span data-stu-id="48380-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="48380-120">Šiame duomenų šaltinyje yra tolesni įdėtieji tipo `Calculated field` laukai.</span><span class="sxs-lookup"><span data-stu-id="48380-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="48380-121">**Kodas**. Šiame lauke yra reiškinys, pateikiantis tipo `String` reikšmę.</span><span class="sxs-lookup"><span data-stu-id="48380-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="48380-122">**Suma**. Šiame lauke yra reiškinys, pateikiantis tipo `Real` reikšmę.</span><span class="sxs-lookup"><span data-stu-id="48380-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="48380-123">Tada įvedate tipo `Container` duomenų šaltinį **2-asis įrašas**.</span><span class="sxs-lookup"><span data-stu-id="48380-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="48380-124">Šiame duomenų šaltinyje yra tolesni įdėtieji tipo `Calculated field` laukai.</span><span class="sxs-lookup"><span data-stu-id="48380-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="48380-125">**Suma**. Šiame lauke yra reiškinys, pateikiantis tipo `Real` reikšmę.</span><span class="sxs-lookup"><span data-stu-id="48380-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="48380-126">**IsValid**. Šiame lauke yra reiškinys, pateikiantis tipo `Boolean` reikšmę.</span><span class="sxs-lookup"><span data-stu-id="48380-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

<span data-ttu-id="48380-127">Šiuo atveju reiškinys `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` pateikia naują sąrašą, kuriame yra du įrašai.</span><span class="sxs-lookup"><span data-stu-id="48380-127">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span> <span data-ttu-id="48380-128">Šio sąrašo struktūrą sudaro vienas tipo `Real` laukas **Suma**, nes šis laukas yra vienintelis laukas, pateikiamas kiekviename iškviestos funkcijos argumente.</span><span class="sxs-lookup"><span data-stu-id="48380-128">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48380-129">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="48380-129">Additional resources</span></span>

[<span data-ttu-id="48380-130">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="48380-130">List functions</span></span>](er-functions-category-list.md)
