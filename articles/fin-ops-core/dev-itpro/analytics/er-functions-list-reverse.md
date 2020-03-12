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
ms.openlocfilehash: a6134ae7eb1a8044cf906f2a8d02eb153522a6cf
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041934"
---
# <span data-ttu-id="359d9-103"><a name="REVERSE">ER REVERSE funkcija</a></span><span class="sxs-lookup"><span data-stu-id="359d9-103"><a name="REVERSE">REVERSE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="359d9-104">`REVERSE` funkcija nurodytą sąrašą pateikia kaip tipo *Įrašų sąrašas* reikšmę, surikiuotą atvirkštine tvarka.</span><span class="sxs-lookup"><span data-stu-id="359d9-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="359d9-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="359d9-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="359d9-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="359d9-106">Arguments</span></span>

<span data-ttu-id="359d9-107">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="359d9-107">`list`: *Record list*</span></span>

<span data-ttu-id="359d9-108">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="359d9-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="359d9-109">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="359d9-109">Return values</span></span>

<span data-ttu-id="359d9-110">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="359d9-110">*Record list*</span></span>

<span data-ttu-id="359d9-111">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="359d9-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="359d9-112">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="359d9-112">Example 1</span></span>

<span data-ttu-id="359d9-113">Jei įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("C|B|A", "|")`, reiškinys `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` pateikia teksto reikšmę **„C“**.</span><span class="sxs-lookup"><span data-stu-id="359d9-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="359d9-114">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="359d9-114">Example 2</span></span>

<span data-ttu-id="359d9-115">Jei **Tiekėjas** sukonfigūruotas kaip modulio Elektroninės ataskaitos (ER) duomenų šaltinis, nurodantis lentelę VendTable, reiškinys `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` pateikia tiekėjų sąrašą, surikiuotą pagal pavadinimą mažėjančia tvarka.</span><span class="sxs-lookup"><span data-stu-id="359d9-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="359d9-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="359d9-116">Additional resources</span></span>

[<span data-ttu-id="359d9-117">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="359d9-117">List functions</span></span>](er-functions-category-list.md)
