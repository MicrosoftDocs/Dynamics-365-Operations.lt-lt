---
title: CONVERTCURRENCY ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CONVERTCURRENCY elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: bf972c6c2cc798811a9fb3bd3a355ac6ffca5a60
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915952"
---
# <span data-ttu-id="1b202-103"><a name="CONVERTCURRENCY">CONVERTCURRENCY ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="1b202-103"><a name="CONVERTCURRENCY">CONVERTCURRENCY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b202-104">`CONVERTCURRENCY` funkcija grąžina *realiojo skaičiaus* reikšmę, nurodančią gautą rezultatą konvertuojant nurodytą piniginę sumą iš nurodytos pirminės valiutos į nurodytą norimą valiutą naudojant nurodytos įmonės parametrus nurodytą dieną.</span><span class="sxs-lookup"><span data-stu-id="1b202-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b202-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="1b202-105">Syntax</span></span>

```
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="1b202-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="1b202-106">Arguments</span></span>

<span data-ttu-id="1b202-107">`amount`: *Sveikasis* arba *Realusis*</span><span class="sxs-lookup"><span data-stu-id="1b202-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="1b202-108">Skaitinė reikšmė, nurodanti piniginę sumą, kurią reikia konvertuoti.</span><span class="sxs-lookup"><span data-stu-id="1b202-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="1b202-109">`source currency`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="1b202-109">`source currency`: *String*</span></span>

<span data-ttu-id="1b202-110">Pirminės valiutos kodas.</span><span class="sxs-lookup"><span data-stu-id="1b202-110">The code of the source currency.</span></span>

<span data-ttu-id="1b202-111">`target currency`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="1b202-111">`target currency`: *String*</span></span>

<span data-ttu-id="1b202-112">Antrinės valiutos kodas.</span><span class="sxs-lookup"><span data-stu-id="1b202-112">The code of the target currency.</span></span>

<span data-ttu-id="1b202-113">`date`: *Data*</span><span class="sxs-lookup"><span data-stu-id="1b202-113">`date`: *Date*</span></span>

<span data-ttu-id="1b202-114">*Datos* reikšmė, kuri nurodo datą, naudojamą konvertavimo valiutos kurso datai nustatyti.</span><span class="sxs-lookup"><span data-stu-id="1b202-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="1b202-115">`company`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="1b202-115">`company`: *String*</span></span>

<span data-ttu-id="1b202-116">*Eilutės* reikšmė, kuri nurodo įmonės, teikiančios parametrus, naudojamus konvertuojant, kodą.</span><span class="sxs-lookup"><span data-stu-id="1b202-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="1b202-117">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="1b202-117">Return values</span></span>

<span data-ttu-id="1b202-118">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="1b202-118">*Real*</span></span>

<span data-ttu-id="1b202-119">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="1b202-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="1b202-120">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="1b202-120">Example</span></span>

<span data-ttu-id="1b202-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` grąžina vieno euro atitikmenį JAV doleriais dabartinio seanso dieną, atsižvelgiant į **DEMF** įmonės parametrus.</span><span class="sxs-lookup"><span data-stu-id="1b202-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b202-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1b202-122">Additional resources</span></span>

[<span data-ttu-id="1b202-123">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="1b202-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
