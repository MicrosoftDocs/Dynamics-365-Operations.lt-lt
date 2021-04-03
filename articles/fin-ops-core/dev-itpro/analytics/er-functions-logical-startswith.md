---
title: STARTSWITH ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip „STARTSWITH” elektroninė ataskaita (ER) funkcija yra naudojama.
author: NickSelin
manager: kfend
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 22e99d9e131410820abd12536b8d4f3e868c6863
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557540"
---
# <a name="startswith-er-function"></a><span data-ttu-id="195ca-103">STARTSWITH ER funkcija</span><span class="sxs-lookup"><span data-stu-id="195ca-103">STARTSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="195ca-104">`STARTSWITH` funkcija nustato, ar nurodyta įvestis prasideda nurodytu tekstu.</span><span class="sxs-lookup"><span data-stu-id="195ca-104">The `STARTSWITH` function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="195ca-105">Gražinama *Loginė reikšmė* **TRUE** vertės, jeigu nurodyta įvestis prasideda nurodytu tekstu.</span><span class="sxs-lookup"><span data-stu-id="195ca-105">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="195ca-106">Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="195ca-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="195ca-107">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="195ca-107">Syntax</span></span>

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a><span data-ttu-id="195ca-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="195ca-108">Arguments</span></span>

<span data-ttu-id="195ca-109">`input`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="195ca-109">`input`: *String*</span></span>

<span data-ttu-id="195ca-110">Tinkamas *Eilutė* tipo arba eilutės konstantos duomenų šaltinio elemento maršrutas, kurio vertė gali prasidėti antru argumentu.</span><span class="sxs-lookup"><span data-stu-id="195ca-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might start with the second argument.</span></span>

<span data-ttu-id="195ca-111">`start text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="195ca-111">`start text`: *String*</span></span>

<span data-ttu-id="195ca-112">Tinkamas *Eilutė* duomenų tipo arba eilutės konstantos duomenų šaltinio elemento maršrutas, kurio vertė gali prasidėti pirmo argumento pradžioje.</span><span class="sxs-lookup"><span data-stu-id="195ca-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the beginning of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="195ca-113">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="195ca-113">Return values</span></span>

<span data-ttu-id="195ca-114">*Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="195ca-114">*Boolean*</span></span>

<span data-ttu-id="195ca-115">Gaunama *Bulio logikos* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="195ca-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="195ca-116">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="195ca-116">Usage notes</span></span>

<span data-ttu-id="195ca-117">Šią funkciją galima naudoti nurodant [FILTER](er-functions-list-filter.md) funkcijos sąlygos išraišką, kai aktualus susiejimas sukonfigūruotas [„Regulatory Configuration Services”](../../../finance/localizations/rcs-globalization-feature.md), kad pasiektumėte [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="195ca-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="195ca-118">Priešingu atveju dizaino metu pateikiama išimtis.</span><span class="sxs-lookup"><span data-stu-id="195ca-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="195ca-119">Gautame pranešime rekomenduojama naudoti [WHERE](er-functions-list-where.md) funkciją vietoje `FILTER` funkcijos.</span><span class="sxs-lookup"><span data-stu-id="195ca-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="195ca-120">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="195ca-120">Example 1</span></span>

<span data-ttu-id="195ca-121">Išraiška `STARTSWITH ("abc", "d")` grąžina **FALSE**, o išraiška `STARTSWITH ("abc", "A")` grąžina **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="195ca-121">The expression `STARTSWITH ("abc", "d")` returns **FALSE**, whereas the expression `STARTSWITH ("abc", "A")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="195ca-122">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="195ca-122">Example 2</span></span>

<span data-ttu-id="195ca-123">Išraiška `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` grąžina **TRUE**, jei vertė **Adresas** lauke **modelis** duomenų šaltinio prasideda **123 Coffee Street**.</span><span class="sxs-lookup"><span data-stu-id="195ca-123">The expression `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returns **TRUE** if the value of the **Address** field of the **model** data source starts with the string **123 Coffee Street**.</span></span> <span data-ttu-id="195ca-124">Kitu atveju ji grąžina **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="195ca-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="195ca-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="195ca-125">Additional resources</span></span>

[<span data-ttu-id="195ca-126">Loginės funkcijos</span><span class="sxs-lookup"><span data-stu-id="195ca-126">Logical functions</span></span>](er-functions-category-logical.md)