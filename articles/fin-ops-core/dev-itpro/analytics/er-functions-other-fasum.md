---
title: FA_SUM ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama FA_SUM elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c31722537e2a6bae502800953939ca01da4527b9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567573"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="7f25f-103">FA_SUM ER funkcija</span><span class="sxs-lookup"><span data-stu-id="7f25f-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f25f-104">`FA_SUM` funkcija grąžina *konteinerio (įrašo)* reikšmę, kurią sudaro nurodyto ilgalaikio turto elemento, vertinimo modelio kodo ir datų laikotarpio ilgalaikio turto sumų duomenys.</span><span class="sxs-lookup"><span data-stu-id="7f25f-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f25f-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="7f25f-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="7f25f-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="7f25f-106">Arguments</span></span>

<span data-ttu-id="7f25f-107">`fixed asset code`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="7f25f-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="7f25f-108">*Eilutės* vertė, reiškianti ilgalaikio turto elemento, kurio balansas skaičiuojamas, kodą.</span><span class="sxs-lookup"><span data-stu-id="7f25f-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="7f25f-109">`value model code`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="7f25f-109">`value model code`: *String*</span></span>

<span data-ttu-id="7f25f-110">*Eilutės* vertė, reiškianti reikšmės modelio, kurio balansas skaičiuojamas, kodą.</span><span class="sxs-lookup"><span data-stu-id="7f25f-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="7f25f-111">`start date`: *Data*</span><span class="sxs-lookup"><span data-stu-id="7f25f-111">`start date`: *Date*</span></span>

<span data-ttu-id="7f25f-112">*Datos* reikšmė, reiškianti laikotarpio, kuriam apskaičiuojamos ilgalaikio turto sumos, pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="7f25f-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="7f25f-113">`end date`: *Data*</span><span class="sxs-lookup"><span data-stu-id="7f25f-113">`end date`: *Date*</span></span>

<span data-ttu-id="7f25f-114">*Datos* reikšmė, reiškianti laikotarpio, kuriam apskaičiuojamos ilgalaikio turto sumos, pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="7f25f-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="7f25f-115">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="7f25f-115">Return values</span></span>

<span data-ttu-id="7f25f-116">*Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="7f25f-116">*Container (record)*</span></span>

<span data-ttu-id="7f25f-117">Gauta įrašo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="7f25f-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="7f25f-118">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="7f25f-118">Example</span></span>

<span data-ttu-id="7f25f-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` grąžina ilgalaikio turto **COMP-000001**, paruošto **dabartiniam** reikšmės modeliui ir laikotarpiui nuo **Data1** iki **Data2**, duomenų konteinerį.</span><span class="sxs-lookup"><span data-stu-id="7f25f-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f25f-120">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7f25f-120">Additional resources</span></span>

[<span data-ttu-id="7f25f-121">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="7f25f-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]