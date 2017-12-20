---
title: "„Power BI‟ turinys Faktinis palyginti su biudžeto"
description: "Šioje temoje aprašomas „Power BI‟ turinys Faktinis palyginti su biudžeto. Joje paaiškinama, kaip pasiekti į turinį įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudotus turiniui kurti."
author: ryansandness
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 2a0ad5af4e4d7da09690331dc9d1a51d2e97a664
ms.contentlocale: lt-lt
ms.lasthandoff: 12/01/2017

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="6b4bc-104">„Power BI‟ turinys Faktinis palyginti su biudžeto</span><span class="sxs-lookup"><span data-stu-id="6b4bc-104">Actual vs budget Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6b4bc-105">Šioje temoje aprašomas „Microsoft Power BI‟ turinys **Faktinis palyginti su biudžeto**.</span><span class="sxs-lookup"><span data-stu-id="6b4bc-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="6b4bc-106">Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.</span><span class="sxs-lookup"><span data-stu-id="6b4bc-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

# <a name="overview"></a><span data-ttu-id="6b4bc-107">Apžvalga</span><span class="sxs-lookup"><span data-stu-id="6b4bc-107">Overview</span></span>

<span data-ttu-id="6b4bc-108">„Power BI‟ turinys **Faktinis palyginti su biudžeto** buvo sukurtas asmenims, kurie organizacijoje yra atsakingi už faktinio našumo stebėjimą palyginti su biudžeto.</span><span class="sxs-lookup"><span data-stu-id="6b4bc-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="6b4bc-109">„Power BI‟ turinys **Faktinis palyginti su biudžeto** leidžia matyti biudžeto nuokrypius.</span><span class="sxs-lookup"><span data-stu-id="6b4bc-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="6b4bc-110">Norėdami geriau suprasti nuokrypių priežastį, galite analizuoti einamųjų metų biudžetą pagal sąskaitos kategoriją, biudžeto kodą, pagrindinę sąskaitą, pagrindinės sąskaitos aprašymus arba ataskaitinį laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="6b4bc-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

# <a name="accessing-the-power-bi-content"></a><span data-ttu-id="6b4bc-111">Prieiga prie „Power BI“ turinio</span><span class="sxs-lookup"><span data-stu-id="6b4bc-111">Accessing the Power BI content</span></span>
<span data-ttu-id="6b4bc-112">„Power BI“ turinio **Faktinis palyginti su biudžeto** ataskaitos rodomos darbo srityse **Didžiosios knygos biudžetas ir prognozės** ir **CFO**.</span><span class="sxs-lookup"><span data-stu-id="6b4bc-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

# <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="6b4bc-113">Į „Power BI“ turinį įtrauktos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="6b4bc-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="6b4bc-114">Tolesnėje lentelėje pateikiama informacija apie metrikas, pateikiamas kiekviename „Power BI“ turinio **Faktinis palyginti su biudžeto** ataskaitų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="6b4bc-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="6b4bc-115">Ataskaita</span><span class="sxs-lookup"><span data-stu-id="6b4bc-115">Report</span></span>                      | <span data-ttu-id="6b4bc-116">Metrika</span><span class="sxs-lookup"><span data-stu-id="6b4bc-116">Metrics</span></span> |
|-----------------------------|---------|
| <span data-ttu-id="6b4bc-117">Išlaidos - faktinės ir biudžeto</span><span class="sxs-lookup"><span data-stu-id="6b4bc-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="6b4bc-118">Visos išlaidos šiais metais</span><span class="sxs-lookup"><span data-stu-id="6b4bc-118">Total expenses this year</span></span></li><li><span data-ttu-id="6b4bc-119">Visos biudžeto išlaidos šiais metais</span><span class="sxs-lookup"><span data-stu-id="6b4bc-119">Budget total expenses this year</span></span></li></ul> |
| <span data-ttu-id="6b4bc-120">Įplaukos - faktinės ir biudžeto</span><span class="sxs-lookup"><span data-stu-id="6b4bc-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="6b4bc-121">Visos įplaukos šiais metais</span><span class="sxs-lookup"><span data-stu-id="6b4bc-121">Total revenue this year</span></span></li><li><span data-ttu-id="6b4bc-122">Visos biudžeto įplaukos šiais metais</span><span class="sxs-lookup"><span data-stu-id="6b4bc-122">Budget total revenue this year</span></span></li><ul> |
| <span data-ttu-id="6b4bc-123">Išlaidos</span><span class="sxs-lookup"><span data-stu-id="6b4bc-123">Expense</span></span>                     | <ul><li><span data-ttu-id="6b4bc-124">Visos išlaidos šiais metais</span><span class="sxs-lookup"><span data-stu-id="6b4bc-124">Total expenses this year</span></span></li><li><span data-ttu-id="6b4bc-125">Išlaidų tikslas pagal biudžetą</span><span class="sxs-lookup"><span data-stu-id="6b4bc-125">Goal for expenses based on budget</span></span> </li><ul> |
| <span data-ttu-id="6b4bc-126">Įplaukos</span><span class="sxs-lookup"><span data-stu-id="6b4bc-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="6b4bc-127">Visos įplaukos šiais metais</span><span class="sxs-lookup"><span data-stu-id="6b4bc-127">Total revenue this year</span></span></li><li><span data-ttu-id="6b4bc-128">Įplaukų tikslas pagal biudžetą</span><span class="sxs-lookup"><span data-stu-id="6b4bc-128">Goal for revenue based on budget</span></span> </li><ul> |
| <span data-ttu-id="6b4bc-129">Grynosios pajamos</span><span class="sxs-lookup"><span data-stu-id="6b4bc-129">Net income</span></span>                  | <ul><li><span data-ttu-id="6b4bc-130">Grynosios pajamos šiais metais</span><span class="sxs-lookup"><span data-stu-id="6b4bc-130">Net income this year</span></span></li><li><span data-ttu-id="6b4bc-131">Grynųjų pajamų tikslas pagal biudžetą</span><span class="sxs-lookup"><span data-stu-id="6b4bc-131">Goal for net income based on budget</span></span> </li><ul> |

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="6b4bc-132">„Power BI“ turinio išplėtimas</span><span class="sxs-lookup"><span data-stu-id="6b4bc-132">Extending the Power BI content</span></span>
<span data-ttu-id="6b4bc-133">Naudodami turinio paketus, kurie pateikiami „Microsoft Dynamics Lifecycle Services“ (LCS), žmonėms, kurie neprisijungia prie „Microsoft Dynamics 365“ galite pateikti didžiąją analizę.</span><span class="sxs-lookup"><span data-stu-id="6b4bc-133">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="6b4bc-134">Galite keisti šiuos turinio paketus, kad į juos įtrauktumėte kitas ataskaitas arba vaizdinius, o po to paskelbti turinio paketus savo Power BI.com nuomotojui analizei.</span><span class="sxs-lookup"><span data-stu-id="6b4bc-134">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="6b4bc-135">„Power BI“ turinį **Faktinis palyginti su biudžeto** galite rasti LCS bibliotekoje Bendrai naudojamas turtas.</span><span class="sxs-lookup"><span data-stu-id="6b4bc-135">You can find the **Actual vs budget** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="6b4bc-136">Norėdami gauti daugiau informacijos apie tai, kaip atsisiųsti turinį ir įdiegti jį savo organizacijoje, žr. [„Power BI“ turinys LCS iš „Microsoft“ ir jūsų partnerių](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="6b4bc-136">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="6b4bc-137">Norėdami peržiūrėti demonstracinius duomenis, kuriuose parodoma, kaip diegti „Power BI“ turinį, žr. „Office Mix“ [„Power BI“ turinys iš „Microsoft“ ir partnerių „Dynamics Lifecycle Services“](https://mix.office.com/watch/9puyb1b2xs1w).</span><span class="sxs-lookup"><span data-stu-id="6b4bc-137">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

# <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="6b4bc-138">Duomenų modelio ir objektų supratimas</span><span class="sxs-lookup"><span data-stu-id="6b4bc-138">Understanding the data model and entities</span></span>

| <span data-ttu-id="6b4bc-139">Objektas</span><span class="sxs-lookup"><span data-stu-id="6b4bc-139">Entity</span></span>                    | <span data-ttu-id="6b4bc-140">Turinys</span><span class="sxs-lookup"><span data-stu-id="6b4bc-140">Contents</span></span> |
|---------------------------|----------|
| <span data-ttu-id="6b4bc-141">Didžiosios knygos veikla</span><span class="sxs-lookup"><span data-stu-id="6b4bc-141">General Ledger Activities</span></span> | <span data-ttu-id="6b4bc-142">Didžiosios knygos operacijų sumos</span><span class="sxs-lookup"><span data-stu-id="6b4bc-142">Transaction amounts for the general ledger</span></span> |
| <span data-ttu-id="6b4bc-143">Biudžeto veikla</span><span class="sxs-lookup"><span data-stu-id="6b4bc-143">Budget Activities</span></span>         | <span data-ttu-id="6b4bc-144">Biudžeto registro operacijų sumos</span><span class="sxs-lookup"><span data-stu-id="6b4bc-144">Transaction amounts for the budget register</span></span> |
| <span data-ttu-id="6b4bc-145">Pagrindinės sąskaitos</span><span class="sxs-lookup"><span data-stu-id="6b4bc-145">Main Accounts</span></span>             | <span data-ttu-id="6b4bc-146">Pagrindinės sąskaitos, pagal kurias filtruojamos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="6b4bc-146">Main accounts to filter reports by</span></span> |
| <span data-ttu-id="6b4bc-147">Finansiniai kalendoriai</span><span class="sxs-lookup"><span data-stu-id="6b4bc-147">Fiscal Calendars</span></span>          | <span data-ttu-id="6b4bc-148">Finansiniai metai, pagal kuriuos filtruojamos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="6b4bc-148">Fiscal calendars to filter reports by</span></span> |
| <span data-ttu-id="6b4bc-149">Didžiosios knygos</span><span class="sxs-lookup"><span data-stu-id="6b4bc-149">Ledgers</span></span>                   | <span data-ttu-id="6b4bc-150">Didžiosios knygos, kurias galima naudoti norint filtruoti dabartinės didžiosios knygos ataskaitą</span><span class="sxs-lookup"><span data-stu-id="6b4bc-150">Ledgers that can be used to filter the report to the current ledger</span></span> |
| <span data-ttu-id="6b4bc-151">Biudžeto kodai</span><span class="sxs-lookup"><span data-stu-id="6b4bc-151">Budget Codes</span></span>              | <span data-ttu-id="6b4bc-152">Biudžeto kodai, pagal kuriuos filtruojamos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="6b4bc-152">Budget codes to filter reports by</span></span> |
| <span data-ttu-id="6b4bc-153">Juridiniai subjektai</span><span class="sxs-lookup"><span data-stu-id="6b4bc-153">Legal Entities</span></span>            | <span data-ttu-id="6b4bc-154">Juridiniai subjektai, kurias galima naudoti norint filtruoti dabartinio juridinio subjekto ataskaitą</span><span class="sxs-lookup"><span data-stu-id="6b4bc-154">Legal entities that can be used to filter the report to the current legal entity</span></span> |

