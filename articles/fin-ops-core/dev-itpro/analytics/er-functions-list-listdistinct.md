---
title: LISTDISTINCT ER funkcija
description: Šioje temoje pateikta informacija apie tai, kaip yra naudojama LISTDISTINCT elektroninės ataskaitos funkcija.
author: NickSelin
manager: kfend
ms.date: 7/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 791038981e88d0f52026bfb17d2d1fa381f28c46
ms.sourcegitcommit: 41e165482b9bff4175c0e3b224dbeead13461956
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2020
ms.locfileid: "3688012"
---
# <a name="listdistinct-er-function"></a><span data-ttu-id="d5021-103">LISTDISTINCT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="d5021-103">LISTDISTINCT ER Function</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="d5021-104">`LISTDISTINCT` funkcija apskaičiuota nurodytą išraišką, kaip selektorių kiekvienam nurodyto sąrašo įrašui.</span><span class="sxs-lookup"><span data-stu-id="d5021-104">The `LISTDISTINCT` function calculates the specified expression as a selector for every record of the specified list.</span></span> <span data-ttu-id="d5021-105">Jis grįžta į naują *Įrašo sąrašo* vertę, kuri turi vieną įrašą kiekvienai atskirai selektoriaus vertei.</span><span class="sxs-lookup"><span data-stu-id="d5021-105">It returns a new *Record list* value that contains a single record for each unique selector value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5021-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="d5021-106">Syntax</span></span>

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a><span data-ttu-id="d5021-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="d5021-107">Arguments</span></span>

<span data-ttu-id="d5021-108">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="d5021-108">`list`: *Record list*</span></span>

<span data-ttu-id="d5021-109">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="d5021-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="d5021-110">`selector`: *Pirminių duomenų tipas*</span><span class="sxs-lookup"><span data-stu-id="d5021-110">`selector`: *Primitive data type*</span></span>

<span data-ttu-id="d5021-111">Galiojanti išraiška yra naudojama selektoriaus vertės apskaičiavimui kiekvienam sąraše nurodytam įrašui.</span><span class="sxs-lookup"><span data-stu-id="d5021-111">A valid expression that is used to calculate a selector value for every record in the specified list.</span></span>

<span data-ttu-id="d5021-112">Toliau pateikti duomenys yra palaikomi šiam parametrui:</span><span class="sxs-lookup"><span data-stu-id="d5021-112">The following data types are supported for this parameter:</span></span>

- <span data-ttu-id="d5021-113">Bulio logika</span><span class="sxs-lookup"><span data-stu-id="d5021-113">Boolean</span></span>
- <span data-ttu-id="d5021-114">Data</span><span class="sxs-lookup"><span data-stu-id="d5021-114">Date</span></span>
- <span data-ttu-id="d5021-115">DateTime</span><span class="sxs-lookup"><span data-stu-id="d5021-115">DateTime</span></span>
- <span data-ttu-id="d5021-116">Guid</span><span class="sxs-lookup"><span data-stu-id="d5021-116">GUID</span></span>
- <span data-ttu-id="d5021-117">Sveikasis skaičius</span><span class="sxs-lookup"><span data-stu-id="d5021-117">Integer</span></span>
- <span data-ttu-id="d5021-118">Int64</span><span class="sxs-lookup"><span data-stu-id="d5021-118">Int64</span></span>
- <span data-ttu-id="d5021-119">Tikrasis</span><span class="sxs-lookup"><span data-stu-id="d5021-119">Real</span></span>
- <span data-ttu-id="d5021-120">Eilutė</span><span class="sxs-lookup"><span data-stu-id="d5021-120">String</span></span>

## <a name="return-values"></a><span data-ttu-id="d5021-121">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="d5021-121">Return values</span></span>

<span data-ttu-id="d5021-122">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="d5021-122">*Record list*</span></span>

<span data-ttu-id="d5021-123">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="d5021-123">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d5021-124">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="d5021-124">Usage notes</span></span>

<span data-ttu-id="d5021-125">Sąrašo struktūra yra sukuriama tiap, kad atitiktų sąraše nurodytą struktūrą.</span><span class="sxs-lookup"><span data-stu-id="d5021-125">The structure of the list that is created matches the structure of the specified list.</span></span>

<span data-ttu-id="d5021-126">Ta pati selektoriaus vertė gali būti apskaičiuojama keliems įrašams nurodytame sąraše.</span><span class="sxs-lookup"><span data-stu-id="d5021-126">The same selector value might be calculated for multiple records in the specified list.</span></span> <span data-ttu-id="d5021-127">Tokiu atveju, įrašą atitinkančios sąraše sukurtos laukelio vertės atitinka pirmojo įrašo vertes nurodytas sąraše, kuriame yra apskaičiuota selektoriaus vertė.</span><span class="sxs-lookup"><span data-stu-id="d5021-127">In this case, field values of the corresponding record in the created list equal the values of the first record from the specified list that the selector value is calculated for.</span></span>

<span data-ttu-id="d5021-128">Šios funkcijos vykdymas yra atliekamas bet kuriame [Elektroninių ataskaitų (ER)](general-electronic-reporting.md) duomenų *Įrašo sąrašo* tipo šaltinyje, kuris yra atmintyje.</span><span class="sxs-lookup"><span data-stu-id="d5021-128">The execution of this function is done on any [Electronic reporting (ER)](general-electronic-reporting.md) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="d5021-129">**GROUPBY** duomenų šaltinis gali būti taip pat naudojamas siekiant sukurti įrašų sąrašą, kuriam selektorius apskaičiuota atskiras vertes.</span><span class="sxs-lookup"><span data-stu-id="d5021-129">The **GROUPBY** data source can also be used to generate the list of records that the selector that has distinct values is calculated for.</span></span> <span data-ttu-id="d5021-130">Nepaisant to, iš vykdymo ir atminties vartojimo perspektyvos, geriau naudoti `LISTDISTINCT` funkciją nei **GROUPBY** duomenų šaltinį, nes ši funkcija yra vykdoma atmintyje.</span><span class="sxs-lookup"><span data-stu-id="d5021-130">However, from a performance and memory consumption perspective, it's better to use the `LISTDISTINCT` function than the **GROUPBY** data source, because the execution of the function is done in memory.</span></span>

## <a name="example"></a><span data-ttu-id="d5021-131">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="d5021-131">Example</span></span>

<span data-ttu-id="d5021-132">Toliau pateiktas pavyzdys rodo, kaip galite gauti unikalios kliento paskyros skaičių sąrašą, turintį mažiausiai vieną pardavimo sąskaitą ar projekto sąskaitą, išduotą per tam tikrą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="d5021-132">The following example shows how you can get the list of unique customer account numbers that at least one sales invoice or project invoice has been issued to during a specific period.</span></span>

1. <span data-ttu-id="d5021-133">Įveskite **Prekybossąskaita** `Record list` tipo duomenų šaltinį, kuris atitinka **Klientosąskaitosdiena** programos lentelę ir filtruoja prekybos sąskaitas per tam tikrą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="d5021-133">Enter the **SalesInvoice** data source of the `Record list` type that refers to the **CustInvoiceJour** application table and filters sales invoices for specific periods.</span></span>

    <span data-ttu-id="d5021-134">Šių duomenų šaltinio `InvoiceAccount` laukelis grąžina klientui išrašytus paskyros skaičius.</span><span class="sxs-lookup"><span data-stu-id="d5021-134">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

2. <span data-ttu-id="d5021-135">Įveskite **Projektosąskaitos** `Record list` tipo duomenų šaltinį, kuris atitinka **Projektosąskaitosdienos** programos lentelę ir filtruoja projekto sąskaitas per tam tikrą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="d5021-135">Enter the **ProjectInvoice** data source of the `Record list` type that refers to the **ProjInvoiceJour** application table and filters project invoices for specific periods.</span></span>

    <span data-ttu-id="d5021-136">Šių duomenų šaltinio `InvoiceAccount` laukelis grąžina klientui išrašytus paskyros skaičius.</span><span class="sxs-lookup"><span data-stu-id="d5021-136">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

3. <span data-ttu-id="d5021-137">Konfigūruokite **Visossąskaitos**`Calculated field` duomenų šaltinio tipą, kuriame yra išsireiškimas `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span><span class="sxs-lookup"><span data-stu-id="d5021-137">Configure the **AllInvoices** data source of the `Calculated field` type that contains the expression `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span></span>

    <span data-ttu-id="d5021-138">Šis duomenų šaltinis grąžina bendrą prekybos sąskaitų ir projekto sąskaitų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="d5021-138">This data source returns the joined list of sales invoices and project invoices.</span></span>

4. <span data-ttu-id="d5021-139">Konfigūruokite **Išrašytaklientui** `Record list` duomenų šaltinio tipą, kuriame yra išraiška `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span><span class="sxs-lookup"><span data-stu-id="d5021-139">Configure the **InvoicedCustomer** data source of the `Record list` type that contains the expression `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span></span>

    <span data-ttu-id="d5021-140">Šis duomenų šaltinis grąžina naują sąrašą, kuriame yra vienas įrašas kiekvienam atskiram klientui, gavusiam sąskaitą per nustatytą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="d5021-140">This data source returns a new list that contains a single record for every unique customer that has been invoiced during the defined period.</span></span> <span data-ttu-id="d5021-141">Šio sąrašo `InvoiceAccount` laukelyje yra kliento paskyros numeris.</span><span class="sxs-lookup"><span data-stu-id="d5021-141">The `InvoiceAccount` field of this list contains a customer account number.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d5021-142">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d5021-142">Additional resources</span></span>

[<span data-ttu-id="d5021-143">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="d5021-143">List functions</span></span>](er-functions-category-list.md)