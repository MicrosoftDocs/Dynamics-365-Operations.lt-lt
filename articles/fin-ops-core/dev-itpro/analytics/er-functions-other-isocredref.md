---
title: ISOCREDREF ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama ISOCREDREF elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: dd692720872314d533274f392f84e5ac7d36c7c1
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041382"
---
# <span data-ttu-id="061e9-103"><a name="ISOCREDREF">ISOCREDREF ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="061e9-103"><a name="ISOCREDREF">ISOCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="061e9-104">`ISOCREDREF` funkcija grąžina *Eilutės* reikšmę, kuri nurodo Tarptautinės standartizacijos organizacijos (ISO) kreditoriaus nuorodą pagal nurodyto SF numerio skaitmenis ir raidinius simbolius.</span><span class="sxs-lookup"><span data-stu-id="061e9-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="061e9-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="061e9-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="061e9-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="061e9-106">Arguments</span></span>

<span data-ttu-id="061e9-107">`invoice number digits`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="061e9-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="061e9-108">Tekstinė reikšmė, nurodanti sąskaitos faktūros numerio skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="061e9-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="061e9-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="061e9-109">Return values</span></span>

<span data-ttu-id="061e9-110">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="061e9-110">*String*</span></span>

<span data-ttu-id="061e9-111">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="061e9-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="061e9-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="061e9-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="061e9-113">Norint iš abėcėlės pašalinti simbolius, kurie nėra suderinami su ISO, `invoice number digits` argumentas turi būti išverstas prieš jį perduodant į šią funkciją.</span><span class="sxs-lookup"><span data-stu-id="061e9-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="061e9-114">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="061e9-114">Example</span></span>

<span data-ttu-id="061e9-115">`ISOCredRef ("VEND-200002")` grąžina **„RF23VEND-200002“**.</span><span class="sxs-lookup"><span data-stu-id="061e9-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="061e9-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="061e9-116">Additional resources</span></span>

[<span data-ttu-id="061e9-117">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="061e9-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
