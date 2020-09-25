---
title: ER ALLITEMSQUERY funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) ALLITEMSQUERY funkcija.
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
ms.openlocfilehash: 37546fccf804a4522638147d39206997e8c0c24c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745374"
---
# <a name="allitemsquery-er-function"></a><span data-ttu-id="6bd47-103">ER ALLITEMSQUERY funkcija</span><span class="sxs-lookup"><span data-stu-id="6bd47-103">ALLITEMSQUERY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6bd47-104">`ALLITEMSQUERY` funkcija veikia kaip sujungta SQL užklausa.</span><span class="sxs-lookup"><span data-stu-id="6bd47-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="6bd47-105">Ji pateikia naują plokščia padarytą tipo *Įrašų sąrašas* reikšmę, sudarytą iš įrašų sąrašo, kuriame nurodomi visi elementai, atitinkantys nurodytą kelią.</span><span class="sxs-lookup"><span data-stu-id="6bd47-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bd47-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="6bd47-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="6bd47-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="6bd47-107">Arguments</span></span>

<span data-ttu-id="6bd47-108">`path`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="6bd47-108">`path`: *Record list*</span></span>

<span data-ttu-id="6bd47-109">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="6bd47-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="6bd47-110">Jame turi būti bent vienas ryšys.</span><span class="sxs-lookup"><span data-stu-id="6bd47-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="6bd47-111">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="6bd47-111">Return values</span></span>

<span data-ttu-id="6bd47-112">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="6bd47-112">*Record list*</span></span>

<span data-ttu-id="6bd47-113">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="6bd47-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6bd47-114">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="6bd47-114">Usage notes</span></span>

<span data-ttu-id="6bd47-115">Nurodytas kelias turi būti apibrėžtas kaip tinkamas duomenų tipo *Įrašų sąrašas* duomenų šaltinio elemento kelias.</span><span class="sxs-lookup"><span data-stu-id="6bd47-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="6bd47-116">Jame taip pat turi būti bent vienas ryšys.</span><span class="sxs-lookup"><span data-stu-id="6bd47-116">It must also contain at least one relation.</span></span> <span data-ttu-id="6bd47-117">Duomenų elementai, pvz., kelio *Eilutė* ir *Data*, kūrimo metu modulio Elektroninės ataskaitos (ER) reiškinių daryklėje turėtų pateikti klaidą.</span><span class="sxs-lookup"><span data-stu-id="6bd47-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="6bd47-118">Kai ši funkcija taikoma duomenų tipo *Įrašų sąrašas* duomenų šaltiniams, nurodantiems programos objektą, kurį galima tiesiogiai iškviesti naudojant SQL (pvz., lentelę, objektą ar užklausą), ji veikia kaip sujungta SQL užklausa.</span><span class="sxs-lookup"><span data-stu-id="6bd47-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="6bd47-119">Priešingu atveju ji veikia atmintyje kaip funkcija [ALLITEMS](er-functions-list-allitems.md).</span><span class="sxs-lookup"><span data-stu-id="6bd47-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="6bd47-120">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="6bd47-120">Example</span></span>

<span data-ttu-id="6bd47-121">Apibrėžkite šiuos modelio susiejimo duomenų šaltinius:</span><span class="sxs-lookup"><span data-stu-id="6bd47-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="6bd47-122">Duomenų šaltinis **CustInv**, kuris priklauso tipui *Lentelės įrašai* ir susijęs su lentele CustInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="6bd47-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="6bd47-123">Duomenų šaltinis **FilteredInv**, kuris priklauso tipui *Apskaičiuotasis laukas* ir turi reiškinį `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span><span class="sxs-lookup"><span data-stu-id="6bd47-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="6bd47-124">**JourLines**, kuris priklauso tipui *Apskaičiuotasis laukas* ir turi reiškinį `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span><span class="sxs-lookup"><span data-stu-id="6bd47-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="6bd47-125">Kai vykdote modelio susiejimą norėdami iškviesti duomenų šaltinį **JourLines**, vykdomas tolesnis SQL sakinys.</span><span class="sxs-lookup"><span data-stu-id="6bd47-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="6bd47-126">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="6bd47-126">Additional resources</span></span>

[<span data-ttu-id="6bd47-127">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="6bd47-127">List functions</span></span>](er-functions-category-list.md)
