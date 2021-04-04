---
title: ISOCREDREF ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama ISOCREDREF elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: a9378028a4b308aae7796b861b37a5f89ddfe49c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563418"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="078c1-103">ISOCREDREF ER funkcija</span><span class="sxs-lookup"><span data-stu-id="078c1-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="078c1-104">`ISOCREDREF` funkcija grąžina *Eilutės* reikšmę, kuri nurodo Tarptautinės standartizacijos organizacijos (ISO) kreditoriaus nuorodą pagal nurodyto SF numerio skaitmenis ir raidinius simbolius.</span><span class="sxs-lookup"><span data-stu-id="078c1-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="078c1-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="078c1-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="078c1-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="078c1-106">Arguments</span></span>

<span data-ttu-id="078c1-107">`invoice number digits`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="078c1-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="078c1-108">Tekstinė reikšmė, nurodanti sąskaitos faktūros numerio skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="078c1-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="078c1-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="078c1-109">Return values</span></span>

<span data-ttu-id="078c1-110">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="078c1-110">*String*</span></span>

<span data-ttu-id="078c1-111">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="078c1-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="078c1-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="078c1-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="078c1-113">Norint iš abėcėlės pašalinti simbolius, kurie nėra suderinami su ISO, `invoice number digits` argumentas turi būti išverstas prieš jį perduodant į šią funkciją.</span><span class="sxs-lookup"><span data-stu-id="078c1-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="078c1-114">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="078c1-114">Example</span></span>

<span data-ttu-id="078c1-115">`ISOCredRef ("VEND-200002")` grąžina **„RF23VEND-200002“**.</span><span class="sxs-lookup"><span data-stu-id="078c1-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="078c1-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="078c1-116">Additional resources</span></span>

[<span data-ttu-id="078c1-117">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="078c1-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]