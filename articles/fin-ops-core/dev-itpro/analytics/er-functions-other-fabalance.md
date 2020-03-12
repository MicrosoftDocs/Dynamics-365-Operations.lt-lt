---
title: FA_BALANCE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama FA_BALANCE elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 76a087157ae53e2c571654ade7383d7bd7a005c3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041451"
---
# <span data-ttu-id="2b53d-103"><a name="FA_BALANCE">FA_BALANCE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="2b53d-103"><a name="FA_BALANCE">FA_BALANCE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b53d-104">`FA_BALANCE` funkcija grąžina *konteinerio (įrašo)* reikšmę, kurią sudaro nurodyto ilgalaikio turto elemento, vertinimo modelio kodo, ataskaitinių metų ir ataskaitos datos ilgalaikio turto balanso duomenys.</span><span class="sxs-lookup"><span data-stu-id="2b53d-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b53d-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="2b53d-105">Syntax</span></span>

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="2b53d-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="2b53d-106">Arguments</span></span>

<span data-ttu-id="2b53d-107">`fixed asset code`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="2b53d-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="2b53d-108">*Eilutės* vertė, reiškianti ilgalaikio turto elemento, kurio balansas skaičiuojamas, kodą.</span><span class="sxs-lookup"><span data-stu-id="2b53d-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="2b53d-109">`value model code`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="2b53d-109">`value model code`: *String*</span></span>

<span data-ttu-id="2b53d-110">*Eilutės* vertė, reiškianti reikšmės modelio, kurio balansas skaičiuojamas, kodą.</span><span class="sxs-lookup"><span data-stu-id="2b53d-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="2b53d-111">`reporting year`: *Išvardijimo vertė*</span><span class="sxs-lookup"><span data-stu-id="2b53d-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="2b53d-112">Programos išvardijimo**Assetyear**, apibrėžiančio balanso skaičiavimo laikotarpį, išvardijimo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="2b53d-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="2b53d-113">`reporting date`: *Data*</span><span class="sxs-lookup"><span data-stu-id="2b53d-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="2b53d-114">*Datos* reikšmė, nurodanti balanso skaičiavimo datą.</span><span class="sxs-lookup"><span data-stu-id="2b53d-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="2b53d-115">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="2b53d-115">Return values</span></span>

<span data-ttu-id="2b53d-116">*Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="2b53d-116">*Container (record)*</span></span>

<span data-ttu-id="2b53d-117">Gauta įrašo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="2b53d-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="2b53d-118">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="2b53d-118">Example</span></span>

<span data-ttu-id="2b53d-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` grąžina ilgalaikio turto **COMP-000001**, dabartinio programos seanso datą paruošto reikšmės modeliui **Dabartinis**, balansų duomenų konteinerį.</span><span class="sxs-lookup"><span data-stu-id="2b53d-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2b53d-120">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="2b53d-120">Additional resources</span></span>

[<span data-ttu-id="2b53d-121">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="2b53d-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
