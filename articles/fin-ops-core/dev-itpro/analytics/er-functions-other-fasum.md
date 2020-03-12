---
title: FA_SUM ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama FA_SUM elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 03bed091350b39601edb22b5af6bda5a83af47eb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041359"
---
# <span data-ttu-id="05bcd-103"><a name="FA_SUM">FA_SUM ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="05bcd-103"><a name="FA_SUM">FA_SUM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05bcd-104">`FA_SUM` funkcija grąžina *konteinerio (įrašo)* reikšmę, kurią sudaro nurodyto ilgalaikio turto elemento, vertinimo modelio kodo ir datų laikotarpio ilgalaikio turto sumų duomenys.</span><span class="sxs-lookup"><span data-stu-id="05bcd-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="05bcd-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="05bcd-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="05bcd-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="05bcd-106">Arguments</span></span>

<span data-ttu-id="05bcd-107">`fixed asset code`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="05bcd-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="05bcd-108">*Eilutės* vertė, reiškianti ilgalaikio turto elemento, kurio balansas skaičiuojamas, kodą.</span><span class="sxs-lookup"><span data-stu-id="05bcd-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="05bcd-109">`value model code`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="05bcd-109">`value model code`: *String*</span></span>

<span data-ttu-id="05bcd-110">*Eilutės* vertė, reiškianti reikšmės modelio, kurio balansas skaičiuojamas, kodą.</span><span class="sxs-lookup"><span data-stu-id="05bcd-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="05bcd-111">`start date`: *Data*</span><span class="sxs-lookup"><span data-stu-id="05bcd-111">`start date`: *Date*</span></span>

<span data-ttu-id="05bcd-112">*Datos* reikšmė, reiškianti laikotarpio, kuriam apskaičiuojamos ilgalaikio turto sumos, pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="05bcd-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="05bcd-113">`end date`: *Data*</span><span class="sxs-lookup"><span data-stu-id="05bcd-113">`end date`: *Date*</span></span>

<span data-ttu-id="05bcd-114">*Datos* reikšmė, reiškianti laikotarpio, kuriam apskaičiuojamos ilgalaikio turto sumos, pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="05bcd-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="05bcd-115">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="05bcd-115">Return values</span></span>

<span data-ttu-id="05bcd-116">*Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="05bcd-116">*Container (record)*</span></span>

<span data-ttu-id="05bcd-117">Gauta įrašo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="05bcd-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="05bcd-118">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="05bcd-118">Example</span></span>

<span data-ttu-id="05bcd-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` grąžina ilgalaikio turto **COMP-000001**, paruošto **dabartiniam** reikšmės modeliui ir laikotarpiui nuo **Data1** iki **Data2**, duomenų konteinerį.</span><span class="sxs-lookup"><span data-stu-id="05bcd-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="05bcd-120">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="05bcd-120">Additional resources</span></span>

[<span data-ttu-id="05bcd-121">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="05bcd-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
