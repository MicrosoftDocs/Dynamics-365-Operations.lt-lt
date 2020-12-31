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
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28f03e5e6af0f252a994f2e54b57a5ef654f4e67
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682248"
---
# <a name="listjoin-er-function"></a><span data-ttu-id="13548-103">LISTJOIN ER funkcija</span><span class="sxs-lookup"><span data-stu-id="13548-103">LISTJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13548-104">`LISTJOIN` funkcija pateikia tipo *Įrašų sąrašas* reikšmę, nurodančią naują jungtinį įrašų sąrašą, sukurtą iš nurodytų argumentų.</span><span class="sxs-lookup"><span data-stu-id="13548-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="13548-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="13548-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="13548-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="13548-106">Arguments</span></span>

<span data-ttu-id="13548-107">`list 1`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="13548-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="13548-108">Nuoroda į duomenų tipo *Įrašų sąrašas* duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="13548-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="13548-109">Šis argumentas yra privalomas.</span><span class="sxs-lookup"><span data-stu-id="13548-109">This argument is mandatory.</span></span>

<span data-ttu-id="13548-110">`list N`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="13548-110">`list N`: *Record list*</span></span>

<span data-ttu-id="13548-111">Nuoroda į duomenų tipo *Įrašų sąrašas* duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="13548-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="13548-112">Šie papildomi argumentai yra pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="13548-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="13548-113">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="13548-113">Return values</span></span>

<span data-ttu-id="13548-114">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="13548-114">*Record list*</span></span>

<span data-ttu-id="13548-115">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="13548-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="13548-116">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="13548-116">Usage notes</span></span>

<span data-ttu-id="13548-117">Sukurto sąrašo struktūroje yra tik tie laukai, kurie pateikiami kiekvieno argumentuose nurodyto įrašų sąrašo struktūroje.</span><span class="sxs-lookup"><span data-stu-id="13548-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="13548-118">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="13548-118">Example</span></span>

<span data-ttu-id="13548-119">Įvedate tipo `Container` duomenų šaltinį **1-asis įrašas**.</span><span class="sxs-lookup"><span data-stu-id="13548-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="13548-120">Šiame duomenų šaltinyje yra tolesni įdėtieji tipo `Calculated field` laukai.</span><span class="sxs-lookup"><span data-stu-id="13548-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="13548-121">**Kodas**. Šiame lauke yra reiškinys, pateikiantis tipo `String` reikšmę.</span><span class="sxs-lookup"><span data-stu-id="13548-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="13548-122">**Suma**. Šiame lauke yra reiškinys, pateikiantis tipo `Real` reikšmę.</span><span class="sxs-lookup"><span data-stu-id="13548-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="13548-123">Tada įvedate tipo `Container` duomenų šaltinį **2-asis įrašas**.</span><span class="sxs-lookup"><span data-stu-id="13548-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="13548-124">Šiame duomenų šaltinyje yra tolesni įdėtieji tipo `Calculated field` laukai.</span><span class="sxs-lookup"><span data-stu-id="13548-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="13548-125">**Suma**. Šiame lauke yra reiškinys, pateikiantis tipo `Real` reikšmę.</span><span class="sxs-lookup"><span data-stu-id="13548-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="13548-126">**IsValid**. Šiame lauke yra reiškinys, pateikiantis tipo `Boolean` reikšmę.</span><span class="sxs-lookup"><span data-stu-id="13548-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

![ER modelio susiejimo dizaino įrankio puslapis](./media/er-functions-list-listjoin-image1.gif)

<span data-ttu-id="13548-128">Šiuo atveju reiškinys `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` pateikia naują sąrašą, kuriame yra du įrašai.</span><span class="sxs-lookup"><span data-stu-id="13548-128">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span>

![ER modelio susiejimo dizaino įrankio puslapis su dviem įrašais](./media/er-functions-list-listjoin-image2.gif)

<span data-ttu-id="13548-130">Šio sąrašo struktūrą sudaro vienas tipo `Real` laukas **Suma**, nes šis laukas yra vienintelis laukas, pateikiamas kiekviename iškviestos funkcijos argumente.</span><span class="sxs-lookup"><span data-stu-id="13548-130">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

![ER modelio susiejimo dizaino įrankio puslapio sumos laukas](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a><span data-ttu-id="13548-132">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="13548-132">Additional resources</span></span>

[<span data-ttu-id="13548-133">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="13548-133">List functions</span></span>](er-functions-category-list.md)

[<span data-ttu-id="13548-134">Įvykdyto ER formato duomenų šaltinių derinimas duomenų srautams ir transformacijai analizuoti</span><span class="sxs-lookup"><span data-stu-id="13548-134">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>](er-debug-data-sources.md)
