---
title: GETENUMVALUEBYNAME ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama GETENUMVALUEBYNAME elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 33ccf358dc5355cd00d5ff41ebd8148a334cba38
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743860"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="37160-103">GETENUMVALUEBYNAME ER funkcija</span><span class="sxs-lookup"><span data-stu-id="37160-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37160-104">`GETENUMVALUEBYNAME`funkcija ieško nurodytame išvardijimo duomenų šaltinyje konkrečios *Enum* reikšmės, naudodama išvardijimo pavadinimą, kuris nurodytas kaip *Eilutės* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="37160-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="37160-105">Jei *Enum* reikšmė randama, funkcija ją pateikia.</span><span class="sxs-lookup"><span data-stu-id="37160-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="37160-106">Priešingu atveju funkcija grąžina **null** išvardijimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="37160-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="37160-107">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="37160-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="37160-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="37160-108">Arguments</span></span>

<span data-ttu-id="37160-109">`enumeration data source path`: *Išvardijimas*</span><span class="sxs-lookup"><span data-stu-id="37160-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="37160-110">Tinkamas vieno iš tolesnių išvardijimo tipų duomenų šaltinio maršrutas:</span><span class="sxs-lookup"><span data-stu-id="37160-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="37160-111">Elektroninių ataskaitų (ER) modelių išvardijimas</span><span class="sxs-lookup"><span data-stu-id="37160-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="37160-112">ER formatų išvardijimas</span><span class="sxs-lookup"><span data-stu-id="37160-112">ER format enumeration</span></span>
- <span data-ttu-id="37160-113">„Microsoft Dynamics 365 Finance“ išvardijimas</span><span class="sxs-lookup"><span data-stu-id="37160-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="37160-114">`enumeration value text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="37160-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="37160-115">Eilutės reikšmė, nurodanti vienos išvardijimo reikšmės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="37160-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="37160-116">Grįžimo vertės</span><span class="sxs-lookup"><span data-stu-id="37160-116">Return values</span></span>

<span data-ttu-id="37160-117">*Išvard.* leidžiama reikšmė NULL</span><span class="sxs-lookup"><span data-stu-id="37160-117">Nullable *Enum*</span></span>

<span data-ttu-id="37160-118">Gaunama išvardijimo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="37160-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="37160-119">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="37160-119">Usage notes</span></span>

<span data-ttu-id="37160-120">Nėra pateikiama jokia išimtis, jei reikšmė *Enum* nerasta naudojant išvardijimo reikšmę, nurodytą kaip *Eilutės* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="37160-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example"></a><span data-ttu-id="37160-121">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="37160-121">Example</span></span>

<span data-ttu-id="37160-122">Tolesnėje iliustracijoje duomenų modelyje įvestas išvardijimas **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="37160-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="37160-123">Atkreipkite dėmesį, kad išvardijimo reikšmėms nurodytos žymos.</span><span class="sxs-lookup"><span data-stu-id="37160-123">Notice that labels are defined for the enumeration values.</span></span>

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="37160-124">Tolesnėje iliustracijoje parodyta tolesnė išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="37160-124">The following illustration shows these details:</span></span>

- <span data-ttu-id="37160-125">Duomenų šaltinis **$Direction** sukonfigūruotas ER ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="37160-125">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="37160-126">Šis duomenų šaltinis yra sukonfigūruotas pagal modelių išvardijimą **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="37160-126">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="37160-127">Išraiška `$IsArrivals` sukurta naudoti modelių išvardijime veikiantį duomenų šaltinį **$Direction** kaip šios funkcijos parametrą.</span><span class="sxs-lookup"><span data-stu-id="37160-127">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="37160-128">Šios lyginamosios išraiškos reikšmė yra **TEISINGA**.</span><span class="sxs-lookup"><span data-stu-id="37160-128">The value of this comparison expression is **TRUE**.</span></span>

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a><span data-ttu-id="37160-129">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="37160-129">Additional resources</span></span>

[<span data-ttu-id="37160-130">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="37160-130">Text functions</span></span>](er-functions-category-text.md)
