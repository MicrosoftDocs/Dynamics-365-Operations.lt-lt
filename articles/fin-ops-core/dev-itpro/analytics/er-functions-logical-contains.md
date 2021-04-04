---
title: „CONTAINS” ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip „CONTAINS” elektroninė ataskaita (ER) funkcija yra naudojama.
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
ms.openlocfilehash: 81964681688cebf870bc9b6c59aff0b7fdd82449
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557539"
---
# <a name="contains-er-function"></a><span data-ttu-id="b7f4e-103">„CONTAINS” ER funkcija</span><span class="sxs-lookup"><span data-stu-id="b7f4e-103">CONTAINS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7f4e-104">`CONTAINS` funkcija nustato, ar nurodytoje įvestyje yra nurodytas tekstas.</span><span class="sxs-lookup"><span data-stu-id="b7f4e-104">The `CONTAINS` function determines whether the specified input contains the specified text.</span></span> <span data-ttu-id="b7f4e-105">Gražinama *Loginė reikšmė* **TRUE** vertės, jeigu nurodytoje įvestyje yra nurodytas tekstas.</span><span class="sxs-lookup"><span data-stu-id="b7f4e-105">It returns a *Boolean* value of **TRUE** if the specified input contains the specified text.</span></span> <span data-ttu-id="b7f4e-106">Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="b7f4e-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7f4e-107">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="b7f4e-107">Syntax</span></span>

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a><span data-ttu-id="b7f4e-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="b7f4e-108">Arguments</span></span>

<span data-ttu-id="b7f4e-109">`input`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="b7f4e-109">`input`: *String*</span></span>

<span data-ttu-id="b7f4e-110">Tinkamas *Eilutė* tipo arba eilutės konstantos duomenų šaltinio elemento maršrutas, kurio vertė gali talpinti antrą argumentą.</span><span class="sxs-lookup"><span data-stu-id="b7f4e-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might contain the second argument.</span></span>

<span data-ttu-id="b7f4e-111">`search text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="b7f4e-111">`search text`: *String*</span></span>

<span data-ttu-id="b7f4e-112">Tinkamas *Eilutė* duomenų tipo arba eilutės konstantos duomenų šaltinio elemento maršrutas, kurio vertė gali būti talpinama pirmame argumente.</span><span class="sxs-lookup"><span data-stu-id="b7f4e-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be contained in the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="b7f4e-113">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="b7f4e-113">Return values</span></span>

<span data-ttu-id="b7f4e-114">*Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="b7f4e-114">*Boolean*</span></span>

<span data-ttu-id="b7f4e-115">Gaunama *Bulio logikos* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="b7f4e-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b7f4e-116">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="b7f4e-116">Usage notes</span></span>

<span data-ttu-id="b7f4e-117">Šią funkciją galima naudoti nurodant [FILTER](er-functions-list-filter.md) funkcijos sąlygos išraišką, kai aktualus susiejimas sukonfigūruotas [„Regulatory Configuration Services”](../../../finance/localizations/rcs-globalization-feature.md), kad pasiektumėte [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="b7f4e-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="b7f4e-118">Priešingu atveju dizaino metu pateikiama išimtis.</span><span class="sxs-lookup"><span data-stu-id="b7f4e-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="b7f4e-119">Gautame pranešime rekomenduojama naudoti [WHERE](er-functions-list-where.md) funkciją vietoje `FILTER` funkcijos.</span><span class="sxs-lookup"><span data-stu-id="b7f4e-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="b7f4e-120">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="b7f4e-120">Example 1</span></span>

<span data-ttu-id="b7f4e-121">Išraiška `CONTAINS ("abc", "d")` grąžina **FALSE**, o išraiška `CONTAINS ("abc", "C")` grąžina **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="b7f4e-121">The expression `CONTAINS ("abc", "d")` returns **FALSE**, whereas the expression `CONTAINS ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b7f4e-122">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="b7f4e-122">Example 2</span></span>

<span data-ttu-id="b7f4e-123">Išraiška `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` grąžina **TRUE**, jei vertė **Adresas** lauke **modelis** duomenų šaltinio yra eilutė **DEU**.</span><span class="sxs-lookup"><span data-stu-id="b7f4e-123">The expression `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` returns **TRUE** if the value of the **Address** field of the **model** data source contains the string **DEU**.</span></span> <span data-ttu-id="b7f4e-124">Kitu atveju ji grąžina **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="b7f4e-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b7f4e-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b7f4e-125">Additional resources</span></span>

[<span data-ttu-id="b7f4e-126">Loginės funkcijos</span><span class="sxs-lookup"><span data-stu-id="b7f4e-126">Logical functions</span></span>](er-functions-category-logical.md)
