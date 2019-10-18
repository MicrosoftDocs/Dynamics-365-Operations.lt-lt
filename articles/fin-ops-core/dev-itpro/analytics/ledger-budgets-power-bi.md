---
title: „Power BI“ turinys Faktinis palyginti su biudžeto
description: Šioje temoje aprašomas „Power BI“ turinys Faktinis palyginti su biudžeto. Joje paaiškinama, kaip pasiekti į turinį įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudotus turiniui kurti.
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a577ab24aaf86c1f7a22953e03f397a2e8213c78
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184398"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="db6be-104">„Power BI“ turinys Faktinis palyginti su biudžeto</span><span class="sxs-lookup"><span data-stu-id="db6be-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db6be-105">Šioje temoje aprašomas „Microsoft Power BI“ turinys **Faktinis palyginti su biudžeto**.</span><span class="sxs-lookup"><span data-stu-id="db6be-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="db6be-106">Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.</span><span class="sxs-lookup"><span data-stu-id="db6be-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="db6be-107">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="db6be-107">Overview</span></span>

<span data-ttu-id="db6be-108">„Power BI“ turinys **Faktinis palyginti su biudžeto** buvo sukurtas asmenims, kurie organizacijoje yra atsakingi už faktinio našumo stebėjimą palyginti su biudžeto.</span><span class="sxs-lookup"><span data-stu-id="db6be-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="db6be-109">„Power BI“ turinys **Faktinis palyginti su biudžeto** leidžia matyti biudžeto nuokrypius.</span><span class="sxs-lookup"><span data-stu-id="db6be-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="db6be-110">Norėdami geriau suprasti nuokrypių priežastį, galite analizuoti einamųjų metų biudžetą pagal sąskaitos kategoriją, biudžeto kodą, pagrindinę sąskaitą, pagrindinės sąskaitos aprašymus arba ataskaitinį laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="db6be-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="db6be-111">Prieiga prie „Power BI“ turinio</span><span class="sxs-lookup"><span data-stu-id="db6be-111">Accessing the Power BI content</span></span>
<span data-ttu-id="db6be-112">„Power BI“ turinio **Faktinis palyginti su biudžeto** ataskaitos rodomos darbo srityse **Didžiosios knygos biudžetas ir prognozės** ir **CFO**.</span><span class="sxs-lookup"><span data-stu-id="db6be-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="db6be-113">Į „Power BI“ turinį įtrauktos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="db6be-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="db6be-114">Tolesnėje lentelėje pateikiama informacija apie metrikas, pateikiamas kiekviename „Power BI“ turinio **Faktinis palyginti su biudžeto** ataskaitų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="db6be-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="db6be-115">Ataskaita</span><span class="sxs-lookup"><span data-stu-id="db6be-115">Report</span></span>                      | <span data-ttu-id="db6be-116">Metrika</span><span class="sxs-lookup"><span data-stu-id="db6be-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="db6be-117">Išlaidos - faktinės ir biudžeto</span><span class="sxs-lookup"><span data-stu-id="db6be-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="db6be-118">Visos išlaidos šiais metais</span><span class="sxs-lookup"><span data-stu-id="db6be-118">Total expenses this year</span></span></li><li><span data-ttu-id="db6be-119">Visos biudžeto išlaidos šiais metais</span><span class="sxs-lookup"><span data-stu-id="db6be-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="db6be-120">Įplaukos - faktinės ir biudžeto</span><span class="sxs-lookup"><span data-stu-id="db6be-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="db6be-121">Visos įplaukos šiais metais</span><span class="sxs-lookup"><span data-stu-id="db6be-121">Total revenue this year</span></span></li><li><span data-ttu-id="db6be-122">Visos biudžeto įplaukos šiais metais</span><span class="sxs-lookup"><span data-stu-id="db6be-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="db6be-123">Išlaidos</span><span class="sxs-lookup"><span data-stu-id="db6be-123">Expense</span></span>                     | <ul><li><span data-ttu-id="db6be-124">Visos išlaidos šiais metais</span><span class="sxs-lookup"><span data-stu-id="db6be-124">Total expenses this year</span></span></li><li><span data-ttu-id="db6be-125">Išlaidų tikslas pagal biudžetą</span><span class="sxs-lookup"><span data-stu-id="db6be-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="db6be-126">Įplaukos</span><span class="sxs-lookup"><span data-stu-id="db6be-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="db6be-127">Visos įplaukos šiais metais</span><span class="sxs-lookup"><span data-stu-id="db6be-127">Total revenue this year</span></span></li><li><span data-ttu-id="db6be-128">Įplaukų tikslas pagal biudžetą</span><span class="sxs-lookup"><span data-stu-id="db6be-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="db6be-129">Grynosios pajamos</span><span class="sxs-lookup"><span data-stu-id="db6be-129">Net income</span></span>                  | <ul><li><span data-ttu-id="db6be-130">Grynosios pajamos šiais metais</span><span class="sxs-lookup"><span data-stu-id="db6be-130">Net income this year</span></span></li><li><span data-ttu-id="db6be-131">Grynųjų pajamų tikslas pagal biudžetą</span><span class="sxs-lookup"><span data-stu-id="db6be-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="db6be-132">Duomenų modelio ir objektų supratimas</span><span class="sxs-lookup"><span data-stu-id="db6be-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="db6be-133">Objektas</span><span class="sxs-lookup"><span data-stu-id="db6be-133">Entity</span></span>                    | <span data-ttu-id="db6be-134">Turinys</span><span class="sxs-lookup"><span data-stu-id="db6be-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="db6be-135">Didžiosios knygos veikla</span><span class="sxs-lookup"><span data-stu-id="db6be-135">General Ledger Activities</span></span> | <span data-ttu-id="db6be-136">Didžiosios knygos operacijų sumos</span><span class="sxs-lookup"><span data-stu-id="db6be-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="db6be-137">Biudžeto veikla</span><span class="sxs-lookup"><span data-stu-id="db6be-137">Budget Activities</span></span>         | <span data-ttu-id="db6be-138">Biudžeto registro operacijų sumos</span><span class="sxs-lookup"><span data-stu-id="db6be-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="db6be-139">Pagrindinės sąskaitos</span><span class="sxs-lookup"><span data-stu-id="db6be-139">Main Accounts</span></span>             | <span data-ttu-id="db6be-140">Pagrindinės sąskaitos, pagal kurias filtruojamos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="db6be-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="db6be-141">Finansiniai kalendoriai</span><span class="sxs-lookup"><span data-stu-id="db6be-141">Fiscal Calendars</span></span>          | <span data-ttu-id="db6be-142">Finansiniai metai, pagal kuriuos filtruojamos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="db6be-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="db6be-143">Didžiosios knygos</span><span class="sxs-lookup"><span data-stu-id="db6be-143">Ledgers</span></span>                   | <span data-ttu-id="db6be-144">Didžiosios knygos, kurias galima naudoti norint filtruoti dabartinės didžiosios knygos ataskaitą</span><span class="sxs-lookup"><span data-stu-id="db6be-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="db6be-145">Biudžeto kodai</span><span class="sxs-lookup"><span data-stu-id="db6be-145">Budget Codes</span></span>              | <span data-ttu-id="db6be-146">Biudžeto kodai, pagal kuriuos filtruojamos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="db6be-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="db6be-147">Juridiniai subjektai</span><span class="sxs-lookup"><span data-stu-id="db6be-147">Legal Entities</span></span>            | <span data-ttu-id="db6be-148">Juridiniai subjektai, kurias galima naudoti norint filtruoti dabartinio juridinio subjekto ataskaitą</span><span class="sxs-lookup"><span data-stu-id="db6be-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |
