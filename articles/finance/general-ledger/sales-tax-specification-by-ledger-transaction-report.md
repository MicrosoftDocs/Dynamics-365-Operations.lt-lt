---
title: PVM specifikacija pagal DK operacijų ataskaitą
description: Šioje temoje paaiškinama, kaip naudoti ataskaitą PVM specifikacija pagal DK operaciją, kad būtų galima peržiūrėti ir atsispausdinti informaciją apie DK operacijas, kurių PVM yra skaičiuojamas.
author: ericwang
manager: Ann Beebe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 438a640124e778b839c660f5e161efa22c319af0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445844"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a><span data-ttu-id="cda51-103">PVM specifikacija pagal DK operacijų ataskaitą</span><span class="sxs-lookup"><span data-stu-id="cda51-103">Sales tax specification by ledger transaction report</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="cda51-104">Šioje temoje paaiškinama, kaip naudoti ataskaitą **PVM specifikacija pagal DK operaciją**, kad būtų galima peržiūrėti ir atsispausdinti informaciją apie DK operacijas, kurių PVM yra skaičiuojamas.</span><span class="sxs-lookup"><span data-stu-id="cda51-104">This topic explains how to use the **Sales tax specification by ledger transaction** report to view and print information about ledger transactions that sales tax is calculated for.</span></span>

## <a name="tax-accounts-vs-non-tax-accounts"></a><span data-ttu-id="cda51-105">Mokesčių sąskaitos, lyginant su ne mokesčių sąskaitomis</span><span class="sxs-lookup"><span data-stu-id="cda51-105">Tax accounts vs. non-tax accounts</span></span>

<span data-ttu-id="cda51-106">Ataskaitoje **PVM specifikacija pagal DK operaciją** rodomos mokesčių sąskaitų ir ne mokesčių sąskaitų mokesčių operacijos.</span><span class="sxs-lookup"><span data-stu-id="cda51-106">The **Sales tax specification by ledger transaction** report shows tax transactions for both tax accounts and non-tax accounts.</span></span> <span data-ttu-id="cda51-107">Šios ataskaitos skirstomos į kategorijas toliau nurodytais būdais.</span><span class="sxs-lookup"><span data-stu-id="cda51-107">These accounts are categorized in the following way:</span></span>

- <span data-ttu-id="cda51-108">**Mokesčių sąskaita** – sąskaita yra laikoma mokesčių sąskaita, kai užregistruojama mokesčių operacija, o pagrindinė sąskaita žurnalo eilutėje **PVM** yra mokesčių sąskaita, pvz., mokėtino PVM sąskaita arba gautino PVM sąskaita.</span><span class="sxs-lookup"><span data-stu-id="cda51-108">**Tax account** – An account is considered a tax account when a tax transaction is posted, and the main account on the **Sales Tax** journal line is a tax account, such as a sales tax payable account or a sales tax receivable account.</span></span>
- <span data-ttu-id="cda51-109">**Ne mokesčių sąskaita** – sąskaita yra laikoma ne mokesčių sąskaita, kai užregistruojama mokesčių operacija, o pradinės operacijos pagrindinė sąskaita yra ne mokesčių sąskaita, pvz., įplaukų sąskaita arba išlaidų sąskaita.</span><span class="sxs-lookup"><span data-stu-id="cda51-109">**Non-tax account** – An account is considered a non-tax account when a tax transaction is posted, and the main account on the original transaction is a non-tax account, such as a revenue account or an expense account.</span></span>

<span data-ttu-id="cda51-110">Ataskaitose mokesčių sąskaitų stulpeliuose **Kilmė**, **Gautinas PVM** ir **Mokėtinas PVM** rodomas **0** (nulis).</span><span class="sxs-lookup"><span data-stu-id="cda51-110">For tax accounts, the **Origin**, **Sales tax receivable**, and **Sales tax payable** columns on the report show **0** (zero).</span></span> <span data-ttu-id="cda51-111">Ne mokesčių sąskaitose šiuose stulpeliuose rodomos sumos.</span><span class="sxs-lookup"><span data-stu-id="cda51-111">For non-tax accounts, those columns show amounts.</span></span>

## <a name="filtering-the-data-on-the-report"></a><span data-ttu-id="cda51-112">Ataskaitoje pateikiamų duomenų filtravimas</span><span class="sxs-lookup"><span data-stu-id="cda51-112">Filtering the data on the report</span></span>

<span data-ttu-id="cda51-113">Kai generuojate ataskaitą, galimi šie numatytieji laukai.</span><span class="sxs-lookup"><span data-stu-id="cda51-113">When you generate the report, the following default fields are available.</span></span> <span data-ttu-id="cda51-114">Šiuos laukus galite naudoti norėdami filtruoti duomenis, kurie rodomi ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="cda51-114">You can use these fields to filter the data that is shown on the report.</span></span>

| <span data-ttu-id="cda51-115">Laukas</span><span class="sxs-lookup"><span data-stu-id="cda51-115">Field</span></span>                      | <span data-ttu-id="cda51-116">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="cda51-116">Description</span></span> |
|----------------------------|-------------|
| <span data-ttu-id="cda51-117">Data</span><span class="sxs-lookup"><span data-stu-id="cda51-117">Date</span></span>                       | <span data-ttu-id="cda51-118">Norėdami nustatyti mokesčių operacijų datų intervalą, naudokite laukus dalyse **Nuo** ir **Iki**.</span><span class="sxs-lookup"><span data-stu-id="cda51-118">Use the fields in the **From** and **To** sections to define a date range for the tax transactions.</span></span> |
| <span data-ttu-id="cda51-119">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="cda51-119">Main account</span></span>               | <span data-ttu-id="cda51-120">Norėdami nustatyti pagrindinių sąskaitų intervalą, naudokite laukus dalyse **Nuo** ir **Iki**.</span><span class="sxs-lookup"><span data-stu-id="cda51-120">Use the fields in the **From** and **To** sections to define a range of main accounts.</span></span> |
| <span data-ttu-id="cda51-121">PVM kodas</span><span class="sxs-lookup"><span data-stu-id="cda51-121">Sales tax code</span></span>             | <span data-ttu-id="cda51-122">Norėdami nustatyti PVM kodų intervalą, naudokite laukus dalyse **Nuo** ir **Iki**.</span><span class="sxs-lookup"><span data-stu-id="cda51-122">Use the fields in the **From** and **To** sections to define a range of sales tax codes.</span></span> |
| <span data-ttu-id="cda51-123">Grupavimas</span><span class="sxs-lookup"><span data-stu-id="cda51-123">Grouping</span></span>                   | <span data-ttu-id="cda51-124">Pasirinkite, ar ataskaita turi būti grupuojama pagal DK sąskaitą, ar pagal PVM kodą.</span><span class="sxs-lookup"><span data-stu-id="cda51-124">Select whether the report should be grouped by ledger account or sales tax code.</span></span> |
| <span data-ttu-id="cda51-125">Tarpinė suma pagal PVM kodą</span><span class="sxs-lookup"><span data-stu-id="cda51-125">Subtotal by sales tax code</span></span> | <span data-ttu-id="cda51-126">Šioje parinktyje nustatykite **Taip**, kad būtų rodomos tarpinės sumos pagal PVM kodą.</span><span class="sxs-lookup"><span data-stu-id="cda51-126">Set this option to **Yes** to show subtotals by sales tax code.</span></span> |
| <span data-ttu-id="cda51-127">Tik bendrosios sumos</span><span class="sxs-lookup"><span data-stu-id="cda51-127">Totals only</span></span>                | <span data-ttu-id="cda51-128">Šioje parinktyje nustatykite **Taip**, kad būtų rodomos tik bendrosios sumos.</span><span class="sxs-lookup"><span data-stu-id="cda51-128">Set this option to **Yes** to show only totals.</span></span> |
| <span data-ttu-id="cda51-129">Tik pagrindinės sąskaitos</span><span class="sxs-lookup"><span data-stu-id="cda51-129">Main accounts only</span></span>         | <span data-ttu-id="cda51-130">Šioje parinktyje nustatykite **Taip**, kad į ataskaitą būtų įtrauktos tik pagrindinės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="cda51-130">Set this option to **Yes** to include only main accounts on the report.</span></span> |

## <a name="showing-only-non-tax-accounts-on-the-report"></a><span data-ttu-id="cda51-131">Tik ne mokesčių sąskaitų rodymas ataskaitoje</span><span class="sxs-lookup"><span data-stu-id="cda51-131">Showing only non-tax accounts on the report</span></span>

<span data-ttu-id="cda51-132">Norėdami, kad ataskaitoje būtų rodomos tik ne mokesčių ataskaitos, nustatykite filtro sąlygą, pvz., žvaigždutę (\*), kaip parodyta toliau pateiktoje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="cda51-132">To show only non-tax accounts on the report, set up a filter condition, such as an asterisk (\*), as shown in the following illustration.</span></span>

![Ataskaita, kurioje rodomos ne mokesčių ataskaitos](media/taxspecperledgertrans.png)
