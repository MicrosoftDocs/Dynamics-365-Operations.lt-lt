---
title: CN_GBT_ADDITIONALDIMENSIONID ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CN_GBT_ADDITIONALDIMENSIONID elektroninių ataskaitų (ER) funkcija.
author: NickSelin
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
ms.openlocfilehash: ac0b54476265171b3826e43600f99097701231e1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744396"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="c3324-103">CN_GBT_ADDITIONALDIMENSIONID ER funkcija</span><span class="sxs-lookup"><span data-stu-id="c3324-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3324-104">`CN_GBT_ADDITIONALDIMENSIONID` funkcija grąžina *Eilutės* reikšmę, nurodančią vieną finansinės dimensijos ID, paimtą iš nurodytos eilutės.</span><span class="sxs-lookup"><span data-stu-id="c3324-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="c3324-105">Nurodytoje eilutėje visos dimensijos pateikiamos kaip kableliais atskirtų ID sąrašas.</span><span class="sxs-lookup"><span data-stu-id="c3324-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3324-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="c3324-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="c3324-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="c3324-107">Arguments</span></span>

<span data-ttu-id="c3324-108">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="c3324-108">`text`: *String*</span></span>

<span data-ttu-id="c3324-109">*Eilutės* reikšmė, kuri pateikia visus matmenis kaip kableliais atskirtų ID sąrašą.</span><span class="sxs-lookup"><span data-stu-id="c3324-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="c3324-110">`number`: Sveikasis</span><span class="sxs-lookup"><span data-stu-id="c3324-110">`number`: Integer</span></span>

<span data-ttu-id="c3324-111">*Sveikojo skaičiaus* reikšmė nurodo pageidaujamos dimensijos sekos kodą nurodytoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c3324-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="c3324-112">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="c3324-112">Return values</span></span>

<span data-ttu-id="c3324-113">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="c3324-113">*String*</span></span>

<span data-ttu-id="c3324-114">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="c3324-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c3324-115">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="c3324-115">Example</span></span>

<span data-ttu-id="c3324-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` grąžina **„CC“**.</span><span class="sxs-lookup"><span data-stu-id="c3324-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3324-117">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c3324-117">Additional resources</span></span>

[<span data-ttu-id="c3324-118">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="c3324-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]