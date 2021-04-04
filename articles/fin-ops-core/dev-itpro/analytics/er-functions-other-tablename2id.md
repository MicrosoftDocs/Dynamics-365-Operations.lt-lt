---
title: TABLENAME2ID ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama TABLENAME2ID elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 49370af4ebb7552dd3aff4512890fd93fa67c72d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563275"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="2f6d3-103">TABLENAME2ID ER funkcija</span><span class="sxs-lookup"><span data-stu-id="2f6d3-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f6d3-104">`TABLENAME2ID` funkcija grąžina nurodyto lentelės pavadinimo lentelės ID skaitinį vaizdavimą kaip *sveikojo skaičiaus* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2f6d3-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f6d3-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="2f6d3-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="2f6d3-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="2f6d3-106">Arguments</span></span>

<span data-ttu-id="2f6d3-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="2f6d3-107">`text`: *String*</span></span>

<span data-ttu-id="2f6d3-108">Tekstinė reikšmė, nurodanti tinkamą lentelės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="2f6d3-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="2f6d3-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="2f6d3-109">Return values</span></span>

<span data-ttu-id="2f6d3-110">*Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="2f6d3-110">*Integer*</span></span>

<span data-ttu-id="2f6d3-111">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="2f6d3-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2f6d3-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="2f6d3-112">Usage notes</span></span>

<span data-ttu-id="2f6d3-113">Šios funkcijos atlikimas gali lemti skirtingus rezultatus skirtinguose „Microsoft Dynamics 365 Finance“ egzemplioriuose, net jei naudojamas tos pačios įmonės pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="2f6d3-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="2f6d3-114">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="2f6d3-114">Example</span></span>

<span data-ttu-id="2f6d3-115">`TABLENAME2ID ("Intrastat")` grąžina **1510**.</span><span class="sxs-lookup"><span data-stu-id="2f6d3-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f6d3-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="2f6d3-116">Additional resources</span></span>

[<span data-ttu-id="2f6d3-117">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="2f6d3-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]