---
title: "„Power BI‟ turinys Faktinis palyginti su biudžeto"
description: "Šioje temoje aprašomas „Power BI‟ turinys Faktinis palyginti su biudžeto. Joje paaiškinama, kaip pasiekti į turinį įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudotus turiniui kurti."
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: c801544e9e37a528203f5a1730aa8cb526d63dbf
ms.contentlocale: lt-lt
ms.lasthandoff: 08/13/2018

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="4248f-104">„Power BI‟ turinys Faktinis palyginti su biudžeto</span><span class="sxs-lookup"><span data-stu-id="4248f-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4248f-105">Šioje temoje aprašomas „Microsoft Power BI‟ turinys **Faktinis palyginti su biudžeto**.</span><span class="sxs-lookup"><span data-stu-id="4248f-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="4248f-106">Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.</span><span class="sxs-lookup"><span data-stu-id="4248f-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="4248f-107">Apžvalga</span><span class="sxs-lookup"><span data-stu-id="4248f-107">Overview</span></span>

<span data-ttu-id="4248f-108">„Power BI‟ turinys **Faktinis palyginti su biudžeto** buvo sukurtas asmenims, kurie organizacijoje yra atsakingi už faktinio našumo stebėjimą palyginti su biudžeto.</span><span class="sxs-lookup"><span data-stu-id="4248f-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="4248f-109">„Power BI‟ turinys **Faktinis palyginti su biudžeto** leidžia matyti biudžeto nuokrypius.</span><span class="sxs-lookup"><span data-stu-id="4248f-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="4248f-110">Norėdami geriau suprasti nuokrypių priežastį, galite analizuoti einamųjų metų biudžetą pagal sąskaitos kategoriją, biudžeto kodą, pagrindinę sąskaitą, pagrindinės sąskaitos aprašymus arba ataskaitinį laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="4248f-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="4248f-111">Prieiga prie „Power BI“ turinio</span><span class="sxs-lookup"><span data-stu-id="4248f-111">Accessing the Power BI content</span></span>
<span data-ttu-id="4248f-112">„Power BI“ turinio **Faktinis palyginti su biudžeto** ataskaitos rodomos darbo srityse **Didžiosios knygos biudžetas ir prognozės** ir **CFO**.</span><span class="sxs-lookup"><span data-stu-id="4248f-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="4248f-113">Į „Power BI“ turinį įtrauktos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="4248f-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="4248f-114">Tolesnėje lentelėje pateikiama informacija apie metrikas, pateikiamas kiekviename „Power BI“ turinio **Faktinis palyginti su biudžeto** ataskaitų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="4248f-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="4248f-115">Ataskaita</span><span class="sxs-lookup"><span data-stu-id="4248f-115">Report</span></span>                      | <span data-ttu-id="4248f-116">Metrika</span><span class="sxs-lookup"><span data-stu-id="4248f-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4248f-117">Išlaidos - faktinės ir biudžeto</span><span class="sxs-lookup"><span data-stu-id="4248f-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="4248f-118">Visos išlaidos šiais metais</span><span class="sxs-lookup"><span data-stu-id="4248f-118">Total expenses this year</span></span></li><li><span data-ttu-id="4248f-119">Visos biudžeto išlaidos šiais metais</span><span class="sxs-lookup"><span data-stu-id="4248f-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="4248f-120">Įplaukos - faktinės ir biudžeto</span><span class="sxs-lookup"><span data-stu-id="4248f-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="4248f-121">Visos įplaukos šiais metais</span><span class="sxs-lookup"><span data-stu-id="4248f-121">Total revenue this year</span></span></li><li><span data-ttu-id="4248f-122">Visos biudžeto įplaukos šiais metais</span><span class="sxs-lookup"><span data-stu-id="4248f-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="4248f-123">Išlaidos</span><span class="sxs-lookup"><span data-stu-id="4248f-123">Expense</span></span>                     | <ul><li><span data-ttu-id="4248f-124">Visos išlaidos šiais metais</span><span class="sxs-lookup"><span data-stu-id="4248f-124">Total expenses this year</span></span></li><li><span data-ttu-id="4248f-125">Išlaidų tikslas pagal biudžetą</span><span class="sxs-lookup"><span data-stu-id="4248f-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="4248f-126">Įplaukos</span><span class="sxs-lookup"><span data-stu-id="4248f-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="4248f-127">Visos įplaukos šiais metais</span><span class="sxs-lookup"><span data-stu-id="4248f-127">Total revenue this year</span></span></li><li><span data-ttu-id="4248f-128">Įplaukų tikslas pagal biudžetą</span><span class="sxs-lookup"><span data-stu-id="4248f-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="4248f-129">Grynosios pajamos</span><span class="sxs-lookup"><span data-stu-id="4248f-129">Net income</span></span>                  | <ul><li><span data-ttu-id="4248f-130">Grynosios pajamos šiais metais</span><span class="sxs-lookup"><span data-stu-id="4248f-130">Net income this year</span></span></li><li><span data-ttu-id="4248f-131">Grynųjų pajamų tikslas pagal biudžetą</span><span class="sxs-lookup"><span data-stu-id="4248f-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="4248f-132">Duomenų modelio ir objektų supratimas</span><span class="sxs-lookup"><span data-stu-id="4248f-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="4248f-133">Objektas</span><span class="sxs-lookup"><span data-stu-id="4248f-133">Entity</span></span>                    | <span data-ttu-id="4248f-134">Turinys</span><span class="sxs-lookup"><span data-stu-id="4248f-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4248f-135">Didžiosios knygos veikla</span><span class="sxs-lookup"><span data-stu-id="4248f-135">General Ledger Activities</span></span> | <span data-ttu-id="4248f-136">Didžiosios knygos operacijų sumos</span><span class="sxs-lookup"><span data-stu-id="4248f-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="4248f-137">Biudžeto veikla</span><span class="sxs-lookup"><span data-stu-id="4248f-137">Budget Activities</span></span>         | <span data-ttu-id="4248f-138">Biudžeto registro operacijų sumos</span><span class="sxs-lookup"><span data-stu-id="4248f-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="4248f-139">Pagrindinės sąskaitos</span><span class="sxs-lookup"><span data-stu-id="4248f-139">Main Accounts</span></span>             | <span data-ttu-id="4248f-140">Pagrindinės sąskaitos, pagal kurias filtruojamos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="4248f-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="4248f-141">Finansiniai kalendoriai</span><span class="sxs-lookup"><span data-stu-id="4248f-141">Fiscal Calendars</span></span>          | <span data-ttu-id="4248f-142">Finansiniai metai, pagal kuriuos filtruojamos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="4248f-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="4248f-143">Didžiosios knygos</span><span class="sxs-lookup"><span data-stu-id="4248f-143">Ledgers</span></span>                   | <span data-ttu-id="4248f-144">Didžiosios knygos, kurias galima naudoti norint filtruoti dabartinės didžiosios knygos ataskaitą</span><span class="sxs-lookup"><span data-stu-id="4248f-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="4248f-145">Biudžeto kodai</span><span class="sxs-lookup"><span data-stu-id="4248f-145">Budget Codes</span></span>              | <span data-ttu-id="4248f-146">Biudžeto kodai, pagal kuriuos filtruojamos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="4248f-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="4248f-147">Juridiniai subjektai</span><span class="sxs-lookup"><span data-stu-id="4248f-147">Legal Entities</span></span>            | <span data-ttu-id="4248f-148">Juridiniai subjektai, kurias galima naudoti norint filtruoti dabartinio juridinio subjekto ataskaitą</span><span class="sxs-lookup"><span data-stu-id="4248f-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |

