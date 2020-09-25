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
ms.openlocfilehash: ae6e0069c6e9227d4cf1045eeebbb825a2f943c3
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744316"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="8f108-103">CONVERTCURRENCY ER funkcija</span><span class="sxs-lookup"><span data-stu-id="8f108-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f108-104">`CONVERTCURRENCY` funkcija grąžina *realiojo skaičiaus* reikšmę, nurodančią gautą rezultatą konvertuojant nurodytą piniginę sumą iš nurodytos pirminės valiutos į nurodytą norimą valiutą naudojant nurodytos įmonės parametrus nurodytą dieną.</span><span class="sxs-lookup"><span data-stu-id="8f108-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f108-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="8f108-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="8f108-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="8f108-106">Arguments</span></span>

<span data-ttu-id="8f108-107">`amount`: *Sveikasis* arba *Realusis*</span><span class="sxs-lookup"><span data-stu-id="8f108-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="8f108-108">Skaitinė reikšmė, nurodanti piniginę sumą, kurią reikia konvertuoti.</span><span class="sxs-lookup"><span data-stu-id="8f108-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="8f108-109">`source currency`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="8f108-109">`source currency`: *String*</span></span>

<span data-ttu-id="8f108-110">Pirminės valiutos kodas.</span><span class="sxs-lookup"><span data-stu-id="8f108-110">The code of the source currency.</span></span>

<span data-ttu-id="8f108-111">`target currency`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="8f108-111">`target currency`: *String*</span></span>

<span data-ttu-id="8f108-112">Antrinės valiutos kodas.</span><span class="sxs-lookup"><span data-stu-id="8f108-112">The code of the target currency.</span></span>

<span data-ttu-id="8f108-113">`date`: *Data*</span><span class="sxs-lookup"><span data-stu-id="8f108-113">`date`: *Date*</span></span>

<span data-ttu-id="8f108-114">*Datos* reikšmė, kuri nurodo datą, naudojamą konvertavimo valiutos kurso datai nustatyti.</span><span class="sxs-lookup"><span data-stu-id="8f108-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="8f108-115">`company`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="8f108-115">`company`: *String*</span></span>

<span data-ttu-id="8f108-116">*Eilutės* reikšmė, kuri nurodo įmonės, teikiančios parametrus, naudojamus konvertuojant, kodą.</span><span class="sxs-lookup"><span data-stu-id="8f108-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="8f108-117">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="8f108-117">Return values</span></span>

<span data-ttu-id="8f108-118">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="8f108-118">*Real*</span></span>

<span data-ttu-id="8f108-119">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="8f108-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="8f108-120">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="8f108-120">Example</span></span>

<span data-ttu-id="8f108-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` grąžina vieno euro atitikmenį JAV doleriais dabartinio seanso dieną, atsižvelgiant į **DEMF** įmonės parametrus.</span><span class="sxs-lookup"><span data-stu-id="8f108-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8f108-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="8f108-122">Additional resources</span></span>

[<span data-ttu-id="8f108-123">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="8f108-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
