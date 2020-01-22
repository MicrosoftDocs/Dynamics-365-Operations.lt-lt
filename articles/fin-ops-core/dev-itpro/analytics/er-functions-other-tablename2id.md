---
title: TABLENAME2ID ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama TABLENAME2ID elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 77d889f75f38b3c07855a96bf65f1456ac2f42e2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915814"
---
# <span data-ttu-id="bd664-103"><a name="TABLENAME2ID">TABLENAME2ID ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="bd664-103"><a name="TABLENAME2ID">TABLENAME2ID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd664-104">`TABLENAME2ID` funkcija grąžina nurodyto lentelės pavadinimo lentelės ID skaitinį vaizdavimą kaip *sveikojo skaičiaus*reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bd664-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd664-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="bd664-105">Syntax</span></span>

```
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="bd664-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="bd664-106">Arguments</span></span>

<span data-ttu-id="bd664-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="bd664-107">`text`: *String*</span></span>

<span data-ttu-id="bd664-108">Tekstinė reikšmė, nurodanti tinkamą lentelės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="bd664-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="bd664-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="bd664-109">Return values</span></span>

<span data-ttu-id="bd664-110">*Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="bd664-110">*Integer*</span></span>

<span data-ttu-id="bd664-111">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="bd664-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bd664-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="bd664-112">Usage notes</span></span>

<span data-ttu-id="bd664-113">Šios funkcijos atlikimas gali lemti skirtingus rezultatus skirtinguose „Microsoft Dynamics 365 Finance“ egzemplioriuose, net jei naudojamas tos pačios įmonės pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="bd664-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="bd664-114">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="bd664-114">Example</span></span>

<span data-ttu-id="bd664-115">`TABLENAME2ID ("Intrastat")` grąžina **1510**.</span><span class="sxs-lookup"><span data-stu-id="bd664-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bd664-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="bd664-116">Additional resources</span></span>

[<span data-ttu-id="bd664-117">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="bd664-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
