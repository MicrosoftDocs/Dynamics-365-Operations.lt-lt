---
title: ER ORDERBY funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) ORDERBY funkcija.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c39700fab90265ed1915b4815a6bb27af58d9516
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686469"
---
# <a name="orderby-er-function"></a><span data-ttu-id="40e96-103">ER ORDERBY funkcija</span><span class="sxs-lookup"><span data-stu-id="40e96-103">ORDERBY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40e96-104">`ORDERBY` funkcija nurodytą sąrašą pateikia kaip tipo *Įrašų sąrašas* reikšmę, jį surikiavus pagal nurodytus argumentus.</span><span class="sxs-lookup"><span data-stu-id="40e96-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="40e96-105">Šiuos argumentus galima apibrėžti kaip išraiškas.</span><span class="sxs-lookup"><span data-stu-id="40e96-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="40e96-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="40e96-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="40e96-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="40e96-107">Arguments</span></span>

<span data-ttu-id="40e96-108">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="40e96-108">`list`: *Record list*</span></span>

<span data-ttu-id="40e96-109">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="40e96-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="40e96-110">`expression 1`: *Laukas*</span><span class="sxs-lookup"><span data-stu-id="40e96-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="40e96-111">Tinkamas duomenų šaltinio lauko kelias, kurį nurodo iškviestos funkcijos `list` argumentas.</span><span class="sxs-lookup"><span data-stu-id="40e96-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="40e96-112">Nurodytas laukas turi būti primityviojo duomenų tipo.</span><span class="sxs-lookup"><span data-stu-id="40e96-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="40e96-113">Šis argumentas yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="40e96-113">This argument is required.</span></span>

<span data-ttu-id="40e96-114">`expression N`: *Laukas*</span><span class="sxs-lookup"><span data-stu-id="40e96-114">`expression N`: *Field*</span></span>

<span data-ttu-id="40e96-115">Tinkamas duomenų šaltinio lauko kelias, kurį nurodo iškviestos funkcijos `list` argumentas.</span><span class="sxs-lookup"><span data-stu-id="40e96-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="40e96-116">Nurodytas laukas turi būti primityviojo duomenų tipo.</span><span class="sxs-lookup"><span data-stu-id="40e96-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="40e96-117">Šie papildomi argumentai yra pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="40e96-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="40e96-118">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="40e96-118">Return values</span></span>

<span data-ttu-id="40e96-119">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="40e96-119">*Record list*</span></span>

<span data-ttu-id="40e96-120">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="40e96-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="40e96-121">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="40e96-121">Example 1</span></span>

<span data-ttu-id="40e96-122">Jei įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("C|B|A", "|")`, reiškinys `FIRST( ORDERBY( DS, DS. Value)).Value` pateikia teksto reikšmę **„A“**.</span><span class="sxs-lookup"><span data-stu-id="40e96-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="40e96-123">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="40e96-123">Example 2</span></span>

<span data-ttu-id="40e96-124">Jei **Tiekėjas** sukonfigūruotas kaip modulio Elektroninės ataskaitos (ER) duomenų šaltinis, nurodantis lentelę VendTable, reiškinys `ORDERBY (Vendors, Vendors.'name()')` pateikia tiekėjų sąrašą, surikiuotą pagal pavadinimą didėjančia tvarka.</span><span class="sxs-lookup"><span data-stu-id="40e96-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40e96-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="40e96-125">Additional resources</span></span>

[<span data-ttu-id="40e96-126">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="40e96-126">List functions</span></span>](er-functions-category-list.md)
