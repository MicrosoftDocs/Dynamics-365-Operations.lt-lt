---
title: CN_GBT_ADDITIONALDIMENSIONID ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CN_GBT_ADDITIONALDIMENSIONID elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: df693d745d1fe74b4500dd3fda0cc0c4be21142d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917033"
---
# <span data-ttu-id="c3897-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="c3897-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3897-104">`CN_GBT_ADDITIONALDIMENSIONID` funkcija grąžina *Eilutės* reikšmę, nurodančią vieną finansinės dimensijos ID, paimtą iš nurodytos eilutės.</span><span class="sxs-lookup"><span data-stu-id="c3897-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="c3897-105">Nurodytoje eilutėje visos dimensijos pateikiamos kaip kableliais atskirtų ID sąrašas.</span><span class="sxs-lookup"><span data-stu-id="c3897-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3897-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="c3897-106">Syntax</span></span>

```
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="c3897-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="c3897-107">Arguments</span></span>

<span data-ttu-id="c3897-108">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="c3897-108">`text`: *String*</span></span>

<span data-ttu-id="c3897-109">*Eilutės* reikšmė, kuri pateikia visus matmenis kaip kableliais atskirtų ID sąrašą.</span><span class="sxs-lookup"><span data-stu-id="c3897-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="c3897-110">`number`: Sveikasis</span><span class="sxs-lookup"><span data-stu-id="c3897-110">`number`: Integer</span></span>

<span data-ttu-id="c3897-111">*Sveikojo skaičiaus* reikšmė nurodo pageidaujamos dimensijos sekos kodą nurodytoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c3897-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="c3897-112">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="c3897-112">Return values</span></span>

<span data-ttu-id="c3897-113">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="c3897-113">*String*</span></span>

<span data-ttu-id="c3897-114">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="c3897-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c3897-115">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="c3897-115">Example</span></span>

<span data-ttu-id="c3897-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` grąžina **„CC“**.</span><span class="sxs-lookup"><span data-stu-id="c3897-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3897-117">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c3897-117">Additional resources</span></span>

[<span data-ttu-id="c3897-118">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="c3897-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
