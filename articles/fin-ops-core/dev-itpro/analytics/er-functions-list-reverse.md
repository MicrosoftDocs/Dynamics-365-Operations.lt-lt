---
title: ER REVERSE funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) REVERSE funkcija.
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
ms.openlocfilehash: 746a736c8797c1c1c5bd71d7d803be4212984595
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755209"
---
# <a name="reverse-er-function"></a><span data-ttu-id="97cf7-103">ER REVERSE funkcija</span><span class="sxs-lookup"><span data-stu-id="97cf7-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97cf7-104">`REVERSE` funkcija nurodytą sąrašą pateikia kaip tipo *Įrašų sąrašas* reikšmę, surikiuotą atvirkštine tvarka.</span><span class="sxs-lookup"><span data-stu-id="97cf7-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="97cf7-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="97cf7-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="97cf7-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="97cf7-106">Arguments</span></span>

<span data-ttu-id="97cf7-107">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="97cf7-107">`list`: *Record list*</span></span>

<span data-ttu-id="97cf7-108">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="97cf7-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="97cf7-109">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="97cf7-109">Return values</span></span>

<span data-ttu-id="97cf7-110">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="97cf7-110">*Record list*</span></span>

<span data-ttu-id="97cf7-111">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="97cf7-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="97cf7-112">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="97cf7-112">Example 1</span></span>

<span data-ttu-id="97cf7-113">Jei įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("C|B|A", "|")`, reiškinys `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` pateikia teksto reikšmę **„C“**.</span><span class="sxs-lookup"><span data-stu-id="97cf7-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="97cf7-114">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="97cf7-114">Example 2</span></span>

<span data-ttu-id="97cf7-115">Jei **Tiekėjas** sukonfigūruotas kaip modulio Elektroninės ataskaitos (ER) duomenų šaltinis, nurodantis lentelę VendTable, reiškinys `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` pateikia tiekėjų sąrašą, surikiuotą pagal pavadinimą mažėjančia tvarka.</span><span class="sxs-lookup"><span data-stu-id="97cf7-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97cf7-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="97cf7-116">Additional resources</span></span>

[<span data-ttu-id="97cf7-117">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="97cf7-117">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]