---
title: WHERE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama WHERE elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 392cf7acebd7ad95bcc0f5d4b7a67500a412a795
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041840"
---
# <span data-ttu-id="14a83-103"><a name="WHERE">WHERE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="14a83-103"><a name="WHERE">WHERE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14a83-104">`WHERE` funkcija grąžina nurodytą sąrašą kaip *Įrašų sąrašo* reikšmę, baigus ją filtruoti pagal nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="14a83-104">The `WHERE` function returns the specified list as a *Record list* value after it has been filtered according to the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="14a83-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="14a83-105">Syntax</span></span>

```vb
WHERE (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="14a83-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="14a83-106">Arguments</span></span>

<span data-ttu-id="14a83-107">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="14a83-107">`list`: *Record list*</span></span>

<span data-ttu-id="14a83-108">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="14a83-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="14a83-109">`condition`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="14a83-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="14a83-110">Tinkama sąlyginė išraiška, naudojama nurodyto sąrašo įrašams filtruoti.</span><span class="sxs-lookup"><span data-stu-id="14a83-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="14a83-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="14a83-111">Return values</span></span>

<span data-ttu-id="14a83-112">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="14a83-112">*Record list*</span></span>

<span data-ttu-id="14a83-113">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="14a83-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="14a83-114">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="14a83-114">Usage notes</span></span>

<span data-ttu-id="14a83-115">Ši funkcija skiriasi nuo funkcijos [FILTER](er-functions-list-filter.md), nes nurodyta sąlyga taikoma bet kuriam elektroninių ataskaitų (ER) duomenų šaltiniui, kurio tipas – *Įrašų sąrašas*.</span><span class="sxs-lookup"><span data-stu-id="14a83-115">This function differs from the [FILTER](er-functions-list-filter.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="14a83-116">Jei argumentais, kurie sukonfigūruoti šiai funkcijai (`list` ir `condition`), galima siųsti užklausą paversti į tiesioginį SQL skambutį, kuriant rodomas įspėjamasis pranešimas.</span><span class="sxs-lookup"><span data-stu-id="14a83-116">If the arguments that are configured for this function (`list` and `condition`) allow this request to be translated to the direct SQL call, a warning message is thrown at design time.</span></span> <span data-ttu-id="14a83-117">Šis pranešimas informuoja vartotoją, kad našumas gali būti pagerintas, jei funkcija [FILTER](er-functions-list-filter.md) naudojama vietoj funkcijos `WHERE`.</span><span class="sxs-lookup"><span data-stu-id="14a83-117">This message informs the user that performance might be improved if the [FILTER](er-functions-list-filter.md) function is used instead of `WHERE`.</span></span>

## <a name="example-1"></a><span data-ttu-id="14a83-118">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="14a83-118">Example 1</span></span>

<span data-ttu-id="14a83-119">Jei **Tiekėjas** sukonfigūruotas kaip ER duomenų šaltinis, nurodantis lentelę „VendTable“, išraiška `WHERE (Vendors, Vendors.VendGroup = "40")` grąžina tik tų tiekėjų, kurie priklauso 40 tiekėjų grupei, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="14a83-119">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `WHERE (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="14a83-120">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="14a83-120">Example 2</span></span>

<span data-ttu-id="14a83-121">Jei įvedate duomenų šaltinį **DS**, kurio tipas – *Apskaičiuotasis laukas*, ir jame yra išraiška `SPLIT ("A|B|C", "|")`, `WHERE( DS, DS.Value = "B")`išraiška grąžina tik vieno įrašo sąrašą, kuriame yra tekstas **„B“** lauke **Reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="14a83-121">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `WHERE( DS, DS.Value = "B")` returns a list of only one record that contains the text **"B"** in the **Value** field.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14a83-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="14a83-122">Additional resources</span></span>

[<span data-ttu-id="14a83-123">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="14a83-123">List functions</span></span>](er-functions-category-list.md)
