---
title: "„Power BI‟ turinys Faktinis palyginti su biudžeto"
description: "Šioje temoje aprašomas „Power BI‟ turinys Faktinis palyginti su biudžeto. Joje paaiškinama, kaip pasiekti į turinį įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudotus turiniui kurti."
author: ryansandness
manager: AnnBe
ms.date: 06/16/2017
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f09af96fb1c76d8737d2c535f1a46565a18deca0
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="eb108-104">„Power BI‟ turinys Faktinis palyginti su biudžeto</span><span class="sxs-lookup"><span data-stu-id="eb108-104">Actual vs budget Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="eb108-105">Šioje temoje aprašomas „Microsoft Power BI‟ turinys **Faktinis palyginti su biudžeto**.</span><span class="sxs-lookup"><span data-stu-id="eb108-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="eb108-106">Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.</span><span class="sxs-lookup"><span data-stu-id="eb108-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

# <a name="overview"></a><span data-ttu-id="eb108-107">Apžvalga</span><span class="sxs-lookup"><span data-stu-id="eb108-107">Overview</span></span>

<span data-ttu-id="eb108-108">„Power BI‟ turinys **Faktinis palyginti su biudžeto** buvo sukurtas asmenims, kurie organizacijoje yra atsakingi už faktinio našumo stebėjimą palyginti su biudžeto.</span><span class="sxs-lookup"><span data-stu-id="eb108-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="eb108-109">„Power BI‟ turinys **Faktinis palyginti su biudžeto** leidžia matyti biudžeto nuokrypius.</span><span class="sxs-lookup"><span data-stu-id="eb108-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="eb108-110">Norėdami geriau suprasti nuokrypių priežastį, galite analizuoti einamųjų metų biudžetą pagal sąskaitos kategoriją, biudžeto kodą, pagrindinę sąskaitą, pagrindinės sąskaitos aprašymus arba ataskaitinį laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="eb108-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

# <a name="accessing-the-power-bi-content"></a><span data-ttu-id="eb108-111">Prieiga prie „Power BI“ turinio</span><span class="sxs-lookup"><span data-stu-id="eb108-111">Accessing the Power BI content</span></span>
<span data-ttu-id="eb108-112">Jei naudojate „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ (2017 m. liepos mėn.), „Power BI“ turinio **Faktinis palyginti su biudžeto** ataskaitos rodomos darbo srityse **Didžiosios knygos biudžetas ir prognozės** ir **CFO**.</span><span class="sxs-lookup"><span data-stu-id="eb108-112">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

# <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="eb108-113">Į „Power BI“ turinį įtrauktos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="eb108-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="eb108-114">Tolesnėje lentelėje pateikiama informacija apie metrikas, pateikiamas kiekviename „Power BI“ turinio **Faktinis palyginti su biudžeto** ataskaitų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="eb108-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="eb108-115">Ataskaita</span><span class="sxs-lookup"><span data-stu-id="eb108-115">Report</span></span>                      | <span data-ttu-id="eb108-116">Metrika</span><span class="sxs-lookup"><span data-stu-id="eb108-116">Metrics</span></span> |
|-----------------------------|---------|
| <span data-ttu-id="eb108-117">Išlaidos - faktinės ir biudžeto</span><span class="sxs-lookup"><span data-stu-id="eb108-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="eb108-118">Visos išlaidos šiais metais</span><span class="sxs-lookup"><span data-stu-id="eb108-118">Total expenses this year</span></span></li><li><span data-ttu-id="eb108-119">Visos biudžeto išlaidos šiais metais</span><span class="sxs-lookup"><span data-stu-id="eb108-119">Budget total expenses this year</span></span></li></ul> |
| <span data-ttu-id="eb108-120">Įplaukos - faktinės ir biudžeto</span><span class="sxs-lookup"><span data-stu-id="eb108-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="eb108-121">Visos įplaukos šiais metais</span><span class="sxs-lookup"><span data-stu-id="eb108-121">Total revenue this year</span></span></li><li><span data-ttu-id="eb108-122">Visos biudžeto įplaukos šiais metais</span><span class="sxs-lookup"><span data-stu-id="eb108-122">Budget total revenue this year</span></span></li><ul> |
| <span data-ttu-id="eb108-123">Išlaidos</span><span class="sxs-lookup"><span data-stu-id="eb108-123">Expense</span></span>                     | <ul><li><span data-ttu-id="eb108-124">Visos išlaidos šiais metais</span><span class="sxs-lookup"><span data-stu-id="eb108-124">Total expenses this year</span></span></li><li><span data-ttu-id="eb108-125">Išlaidų tikslas pagal biudžetą</span><span class="sxs-lookup"><span data-stu-id="eb108-125">Goal for expenses based on budget</span></span> </li><ul> |
| <span data-ttu-id="eb108-126">Įplaukos</span><span class="sxs-lookup"><span data-stu-id="eb108-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="eb108-127">Visos įplaukos šiais metais</span><span class="sxs-lookup"><span data-stu-id="eb108-127">Total revenue this year</span></span></li><li><span data-ttu-id="eb108-128">Įplaukų tikslas pagal biudžetą</span><span class="sxs-lookup"><span data-stu-id="eb108-128">Goal for revenue based on budget</span></span> </li><ul> |
| <span data-ttu-id="eb108-129">Grynosios pajamos</span><span class="sxs-lookup"><span data-stu-id="eb108-129">Net income</span></span>                  | <ul><li><span data-ttu-id="eb108-130">Grynosios pajamos šiais metais</span><span class="sxs-lookup"><span data-stu-id="eb108-130">Net income this year</span></span></li><li><span data-ttu-id="eb108-131">Grynųjų pajamų tikslas pagal biudžetą</span><span class="sxs-lookup"><span data-stu-id="eb108-131">Goal for net income based on budget</span></span> </li><ul> |

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="eb108-132">„Power BI“ turinio išplėtimas</span><span class="sxs-lookup"><span data-stu-id="eb108-132">Extending the Power BI content</span></span>
<span data-ttu-id="eb108-133">Naudodami turinio paketus, kurie pateikiami „Microsoft Dynamics Lifecycle Services“ (LCS), žmonėms, kurie neprisijungia prie „Microsoft Dynamics 365“ galite pateikti didžiąją analizę.</span><span class="sxs-lookup"><span data-stu-id="eb108-133">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="eb108-134">Galite keisti šiuos turinio paketus, kad į juos įtrauktumėte kitas ataskaitas arba vaizdinius, o po to paskelbti turinio paketus savo Power BI.com nuomotojui analizei.</span><span class="sxs-lookup"><span data-stu-id="eb108-134">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="eb108-135">„Power BI“ turinį **Faktinis palyginti su biudžeto** galite rasti LCS bibliotekoje Bendrai naudojamas turtas.</span><span class="sxs-lookup"><span data-stu-id="eb108-135">You can find the **Actual vs budget** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="eb108-136">Norėdami gauti daugiau informacijos apie tai, kaip atsisiųsti turinį ir įdiegti jį savo organizacijoje, žr. [„Power BI“ turinys LCS iš „Microsoft“ ir jūsų partnerių](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="eb108-136">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="eb108-137">Norėdami peržiūrėti demonstracinius duomenis, kuriuose parodoma, kaip diegti „Power BI“ turinį, žr. „Office Mix“ [„Power BI“ turinys iš „Microsoft“ ir partnerių „Dynamics Lifecycle Services“](https://mix.office.com/watch/9puyb1b2xs1w).</span><span class="sxs-lookup"><span data-stu-id="eb108-137">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

# <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="eb108-138">Duomenų modelio ir objektų supratimas</span><span class="sxs-lookup"><span data-stu-id="eb108-138">Understanding the data model and entities</span></span>

| <span data-ttu-id="eb108-139">Objektas</span><span class="sxs-lookup"><span data-stu-id="eb108-139">Entity</span></span>                    | <span data-ttu-id="eb108-140">Turinys</span><span class="sxs-lookup"><span data-stu-id="eb108-140">Contents</span></span> |
|---------------------------|----------|
| <span data-ttu-id="eb108-141">Didžiosios knygos veikla</span><span class="sxs-lookup"><span data-stu-id="eb108-141">General Ledger Activities</span></span> | <span data-ttu-id="eb108-142">Didžiosios knygos operacijų sumos</span><span class="sxs-lookup"><span data-stu-id="eb108-142">Transaction amounts for the general ledger</span></span> |
| <span data-ttu-id="eb108-143">Biudžeto veikla</span><span class="sxs-lookup"><span data-stu-id="eb108-143">Budget Activities</span></span>         | <span data-ttu-id="eb108-144">Biudžeto registro operacijų sumos</span><span class="sxs-lookup"><span data-stu-id="eb108-144">Transaction amounts for the budget register</span></span> |
| <span data-ttu-id="eb108-145">Pagrindinės sąskaitos</span><span class="sxs-lookup"><span data-stu-id="eb108-145">Main Accounts</span></span>             | <span data-ttu-id="eb108-146">Pagrindinės sąskaitos, pagal kurias filtruojamos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="eb108-146">Main accounts to filter reports by</span></span> |
| <span data-ttu-id="eb108-147">Finansiniai kalendoriai</span><span class="sxs-lookup"><span data-stu-id="eb108-147">Fiscal Calendars</span></span>          | <span data-ttu-id="eb108-148">Finansiniai metai, pagal kuriuos filtruojamos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="eb108-148">Fiscal calendars to filter reports by</span></span> |
| <span data-ttu-id="eb108-149">Didžiosios knygos</span><span class="sxs-lookup"><span data-stu-id="eb108-149">Ledgers</span></span>                   | <span data-ttu-id="eb108-150">Didžiosios knygos, kurias galima naudoti norint filtruoti dabartinės didžiosios knygos ataskaitą</span><span class="sxs-lookup"><span data-stu-id="eb108-150">Ledgers that can be used to filter the report to the current ledger</span></span> |
| <span data-ttu-id="eb108-151">Biudžeto kodai</span><span class="sxs-lookup"><span data-stu-id="eb108-151">Budget Codes</span></span>              | <span data-ttu-id="eb108-152">Biudžeto kodai, pagal kuriuos filtruojamos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="eb108-152">Budget codes to filter reports by</span></span> |
| <span data-ttu-id="eb108-153">Juridiniai subjektai</span><span class="sxs-lookup"><span data-stu-id="eb108-153">Legal Entities</span></span>            | <span data-ttu-id="eb108-154">Juridiniai subjektai, kurias galima naudoti norint filtruoti dabartinio juridinio subjekto ataskaitą</span><span class="sxs-lookup"><span data-stu-id="eb108-154">Legal entities that can be used to filter the report to the current legal entity</span></span> |

