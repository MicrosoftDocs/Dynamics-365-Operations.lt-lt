---
title: ENDSWITH ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip „ENDSWITH” elektroninė ataskaita (ER) funkcija yra naudojama.
author: NickSelin
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
ms.openlocfilehash: bdd2f364e2d0b80d3df20592ec827dcabf99a06c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745406"
---
# <a name="endswith-er-function"></a><span data-ttu-id="05a61-103">ENDSWITH ER funkcija</span><span class="sxs-lookup"><span data-stu-id="05a61-103">ENDSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05a61-104">`ENDSWITH` funkcija nustato, ar nurodyta įvestis baigiasi nurodytu tekstu.</span><span class="sxs-lookup"><span data-stu-id="05a61-104">The `ENDSWITH` function determines whether the specified input ends with the specified text.</span></span> <span data-ttu-id="05a61-105">Gražinama *Loginė reikšmė* **TRUE** vertės, jeigu nurodyta įvestis baigiasi nurodytu tekstu.</span><span class="sxs-lookup"><span data-stu-id="05a61-105">It returns a *Boolean* value of **TRUE** if the specified input ends with the specified text.</span></span> <span data-ttu-id="05a61-106">Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="05a61-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="05a61-107">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="05a61-107">Syntax</span></span>

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a><span data-ttu-id="05a61-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="05a61-108">Arguments</span></span>

<span data-ttu-id="05a61-109">`input`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="05a61-109">`input`: *String*</span></span>

<span data-ttu-id="05a61-110">Tinkamas *Eilutė* tipo arba eilutės konstantos duomenų šaltinio elemento maršrutas, kurio vertė gali baigtis antru argumentu.</span><span class="sxs-lookup"><span data-stu-id="05a61-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might end with the second argument.</span></span>

<span data-ttu-id="05a61-111">`start text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="05a61-111">`start text`: *String*</span></span>

<span data-ttu-id="05a61-112">Tinkamas *Eilutė* duomenų tipo arba eilutės konstantos duomenų šaltinio elemento maršrutas, kurio vertė gali baigtis pirmo argumento pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="05a61-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the end of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="05a61-113">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="05a61-113">Return values</span></span>

<span data-ttu-id="05a61-114">*Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="05a61-114">*Boolean*</span></span>

<span data-ttu-id="05a61-115">Gaunama *Bulio logikos* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="05a61-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="05a61-116">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="05a61-116">Usage notes</span></span>

<span data-ttu-id="05a61-117">Šią funkciją galima naudoti nurodant [FILTER](er-functions-list-filter.md) funkcijos sąlygos išraišką, kai aktualus susiejimas sukonfigūruotas [„Regulatory Configuration Services”](../../../finance/localizations/rcs-globalization-feature.md), kad pasiektumėte [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="05a61-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="05a61-118">Priešingu atveju dizaino metu pateikiama išimtis.</span><span class="sxs-lookup"><span data-stu-id="05a61-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="05a61-119">Gautame pranešime rekomenduojama naudoti [WHERE](er-functions-list-where.md) funkciją vietoje `FILTER` funkcijos.</span><span class="sxs-lookup"><span data-stu-id="05a61-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="05a61-120">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="05a61-120">Example 1</span></span>

<span data-ttu-id="05a61-121">Išraiška `ENDSWITH ("abc", "d")` grąžina **FALSE**, o išraiška `ENDSWITH ("abc", "C")` grąžina **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="05a61-121">The expression `ENDSWITH ("abc", "d")` returns **FALSE**, whereas the expression `ENDSWITH ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="05a61-122">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="05a61-122">Example 2</span></span>

<span data-ttu-id="05a61-123">Išraiška `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` grąžina **TRUE**, jei vertė **Adresas** lauke **modelis** duomenų šaltinio baigiasi eilute **JAV**.</span><span class="sxs-lookup"><span data-stu-id="05a61-123">The expression `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` returns **TRUE** if the value of the **Address** field of the **model** data source ends with the string **USA**.</span></span> <span data-ttu-id="05a61-124">Kitu atveju ji grąžina **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="05a61-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="05a61-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="05a61-125">Additional resources</span></span>

[<span data-ttu-id="05a61-126">Loginės funkcijos</span><span class="sxs-lookup"><span data-stu-id="05a61-126">Logical functions</span></span>](er-functions-category-logical.md)
