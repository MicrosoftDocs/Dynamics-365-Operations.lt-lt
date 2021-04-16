---
title: ER ISEMPTY funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) ISEMPTY funkcija.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 9c33e8b613bf5bf5bc17a42a7668d4cc4ee58e53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750441"
---
# <a name="isempty-er-function"></a><span data-ttu-id="2930f-103">ER ISEMPTY funkcija</span><span class="sxs-lookup"><span data-stu-id="2930f-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2930f-104">Jei nurodytame sąraše nėra įrašų, `ISEMPTY` funkcija pateikia *Bulio logikos* reikšmę **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="2930f-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="2930f-105">Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="2930f-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2930f-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="2930f-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="2930f-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="2930f-107">Arguments</span></span>

<span data-ttu-id="2930f-108">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="2930f-108">`list`: *Record list*</span></span>

<span data-ttu-id="2930f-109">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="2930f-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="2930f-110">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="2930f-110">Return values</span></span>

<span data-ttu-id="2930f-111">*Būlio logika*</span><span class="sxs-lookup"><span data-stu-id="2930f-111">*Boolean*</span></span>

<span data-ttu-id="2930f-112">Gaunama *Bulio logikos* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="2930f-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="2930f-113">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="2930f-113">Example 1</span></span>

<span data-ttu-id="2930f-114">Jei įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("A|B|C", "|")`, reiškinys `ISEMPTY(DS)` pateikia **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="2930f-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="2930f-115">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="2930f-115">Example 2</span></span>

<span data-ttu-id="2930f-116">Reiškinys `ISEMPTY (SPLIT ("",1))` pateikia **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="2930f-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2930f-117">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="2930f-117">Additional resources</span></span>

[<span data-ttu-id="2930f-118">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="2930f-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]