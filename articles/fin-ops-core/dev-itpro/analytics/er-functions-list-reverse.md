---
title: ER REVERSE funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) REVERSE funkcija.
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
ms.openlocfilehash: 3343ad788cef29a79f9b110bf29809cd5f0e5c63
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917240"
---
# <span data-ttu-id="f42e5-103"><a name="REVERSE">ER REVERSE funkcija</a></span><span class="sxs-lookup"><span data-stu-id="f42e5-103"><a name="REVERSE">REVERSE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f42e5-104">`REVERSE` funkcija nurodytą sąrašą pateikia kaip tipo *Įrašų sąrašas* reikšmę, surikiuotą atvirkštine tvarka.</span><span class="sxs-lookup"><span data-stu-id="f42e5-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f42e5-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="f42e5-105">Syntax</span></span>

```
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="f42e5-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="f42e5-106">Arguments</span></span>

<span data-ttu-id="f42e5-107">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="f42e5-107">`list`: *Record list*</span></span>

<span data-ttu-id="f42e5-108">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="f42e5-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f42e5-109">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="f42e5-109">Return values</span></span>

<span data-ttu-id="f42e5-110">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="f42e5-110">*Record list*</span></span>

<span data-ttu-id="f42e5-111">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="f42e5-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="f42e5-112">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="f42e5-112">Example 1</span></span>

<span data-ttu-id="f42e5-113">Jei įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("C|B|A", "|")`, reiškinys `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` pateikia teksto reikšmę **„C“**.</span><span class="sxs-lookup"><span data-stu-id="f42e5-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f42e5-114">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="f42e5-114">Example 2</span></span>

<span data-ttu-id="f42e5-115">Jei **Tiekėjas** sukonfigūruotas kaip modulio Elektroninės ataskaitos (ER) duomenų šaltinis, nurodantis lentelę VendTable, reiškinys `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` pateikia tiekėjų sąrašą, surikiuotą pagal pavadinimą mažėjančia tvarka.</span><span class="sxs-lookup"><span data-stu-id="f42e5-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f42e5-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f42e5-116">Additional resources</span></span>

[<span data-ttu-id="f42e5-117">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="f42e5-117">List functions</span></span>](er-functions-category-list.md)
