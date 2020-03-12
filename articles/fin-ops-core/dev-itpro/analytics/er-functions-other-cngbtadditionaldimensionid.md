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
ms.openlocfilehash: 2395a1932e543e35ced28a2a6e56ab44835de19a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041543"
---
# <span data-ttu-id="cc32f-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="cc32f-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc32f-104">`CN_GBT_ADDITIONALDIMENSIONID` funkcija grąžina *Eilutės* reikšmę, nurodančią vieną finansinės dimensijos ID, paimtą iš nurodytos eilutės.</span><span class="sxs-lookup"><span data-stu-id="cc32f-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="cc32f-105">Nurodytoje eilutėje visos dimensijos pateikiamos kaip kableliais atskirtų ID sąrašas.</span><span class="sxs-lookup"><span data-stu-id="cc32f-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc32f-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="cc32f-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="cc32f-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="cc32f-107">Arguments</span></span>

<span data-ttu-id="cc32f-108">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="cc32f-108">`text`: *String*</span></span>

<span data-ttu-id="cc32f-109">*Eilutės* reikšmė, kuri pateikia visus matmenis kaip kableliais atskirtų ID sąrašą.</span><span class="sxs-lookup"><span data-stu-id="cc32f-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="cc32f-110">`number`: Sveikasis</span><span class="sxs-lookup"><span data-stu-id="cc32f-110">`number`: Integer</span></span>

<span data-ttu-id="cc32f-111">*Sveikojo skaičiaus* reikšmė nurodo pageidaujamos dimensijos sekos kodą nurodytoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="cc32f-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="cc32f-112">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="cc32f-112">Return values</span></span>

<span data-ttu-id="cc32f-113">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="cc32f-113">*String*</span></span>

<span data-ttu-id="cc32f-114">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="cc32f-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="cc32f-115">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="cc32f-115">Example</span></span>

<span data-ttu-id="cc32f-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` grąžina **„CC“**.</span><span class="sxs-lookup"><span data-stu-id="cc32f-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc32f-117">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="cc32f-117">Additional resources</span></span>

[<span data-ttu-id="cc32f-118">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="cc32f-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
