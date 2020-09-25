---
title: ER FILTER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) FILTER funkcija.
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
ms.openlocfilehash: d281fe710381b0ecb075a0d9281d46bd6edf987d
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745302"
---
# <a name="filter-er-function"></a><span data-ttu-id="9539a-103">ER FILTER funkcija</span><span class="sxs-lookup"><span data-stu-id="9539a-103">FILTER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9539a-104">`FILTER` funkcija pateikia nurodytą sąrašą kaip tipo *Įrašų sąrašas* reikšmę, užklausą pakeitus taip, kad ji taikytų nurodytos sąlygos filtrą.</span><span class="sxs-lookup"><span data-stu-id="9539a-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="9539a-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="9539a-105">Syntax</span></span>

```vb
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="9539a-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="9539a-106">Arguments</span></span>

<span data-ttu-id="9539a-107">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="9539a-107">`list`: *Record list*</span></span>

<span data-ttu-id="9539a-108">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="9539a-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="9539a-109">`condition`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="9539a-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="9539a-110">Tinkama sąlyginė išraiška, naudojama nurodyto sąrašo įrašams filtruoti.</span><span class="sxs-lookup"><span data-stu-id="9539a-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="9539a-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="9539a-111">Return values</span></span>

<span data-ttu-id="9539a-112">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="9539a-112">*Record list*</span></span>

<span data-ttu-id="9539a-113">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="9539a-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9539a-114">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="9539a-114">Usage notes</span></span>

<span data-ttu-id="9539a-115">Ši funkcija skiriasi nuo funkcijos [WHERE](er-functions-list-where.md), nes nurodyta sąlyga duomenų bazės lygiu taikoma bet kuriam modulio Elektroninės ataskaitos (ER) duomenų šaltiniui, kurio tipas – *Lentelės įrašai*.</span><span class="sxs-lookup"><span data-stu-id="9539a-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="9539a-116">Sąrašą ir sąlygas galima nustatyti naudojant lenteles ir ryšius.</span><span class="sxs-lookup"><span data-stu-id="9539a-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="9539a-117">Jei vienu ar abiem argumentais, kurie sukonfigūruoti šiai funkcijai (`list` ir `condition`), negalima siųsti šios užklausos paversti į tiesioginę SQL iškvietą, kuriant pateikiama išimtis.</span><span class="sxs-lookup"><span data-stu-id="9539a-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="9539a-118">Ši išimtis vartotoją informuoja, kad arba `list`, arba `condition` negalima naudoti norint teikti duomenų bazės užklausą.</span><span class="sxs-lookup"><span data-stu-id="9539a-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="9539a-119">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9539a-119">Example 1</span></span>

<span data-ttu-id="9539a-120">Jei **Tiekėjas** sukonfigūruotas kaip ER duomenų šaltinis, nurodantis lentelę VendTable, reiškinys `FILTER (Vendors, Vendors.VendGroup = "40")` pateikia tik tų tiekėjų, kurie priklauso 40 tiekėjų grupei, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="9539a-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="9539a-121">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9539a-121">Example 2</span></span>

<span data-ttu-id="9539a-122">Jei **Tiekėjas** sukonfigūruotas kaip ER duomenų šaltinis, nurodantis lentelę VendTable, o **parmVendorBankGroup** sukonfigūruotas kaip ER duomenų šaltinis, pateikiantis duomenų tipo *Eilutė* reikšmę, reiškinys `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` pateikia tik tų tiekėjų, kurie priklauso konkrečiai banko grupei, sąskaitų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="9539a-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="9539a-123">3 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9539a-123">Example 3</span></span>

<span data-ttu-id="9539a-124">Įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("A,B,C", ",")`.</span><span class="sxs-lookup"><span data-stu-id="9539a-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="9539a-125">Tada įvedate kitą reiškinį `FILTER( DS, DS.Value = "B")`.</span><span class="sxs-lookup"><span data-stu-id="9539a-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="9539a-126">Šį reiškinį bandant įrašyti ER formulių kūrimo įrankyje, pateikiama tokia išimtis: „Tikrinimo klaida: FILTER funkcijos sąrašo reiškinio užklausų teikti negalima.“</span><span class="sxs-lookup"><span data-stu-id="9539a-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9539a-127">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9539a-127">Additional resources</span></span>

[<span data-ttu-id="9539a-128">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="9539a-128">List functions</span></span>](er-functions-category-list.md)
