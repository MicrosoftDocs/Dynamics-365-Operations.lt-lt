---
title: "Savikainos objekto valdiklių prieigos teisių apibrėžimas"
description: "Šioje temoje pateikiama informacija apie savikainos objekto valdiklių prieigos teises."
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 89497e49b85eecec5da31e76786ab950db088746
ms.contentlocale: lt-lt
ms.lasthandoff: 01/19/2018

---

# <a name="access-rights-of-a-cost-object-controller"></a><span data-ttu-id="f273c-103">Savikainos objekto valdiklio prieigos teisės</span><span class="sxs-lookup"><span data-stu-id="f273c-103">Access rights of a cost object controller</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f273c-104">Darbo sritis **Savikainos kontrolė** yra centrinis taškas, kuriame vadybininkai gali peržiūrėti savo savikainos objektų našumą.</span><span class="sxs-lookup"><span data-stu-id="f273c-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="f273c-105">Naudodamiesi šia sritimi vadybininkai gali naudoti kaštų apskaitos duomenis net jei jie nėra išlaidų buhalterijai.</span><span class="sxs-lookup"><span data-stu-id="f273c-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="f273c-106">Saugumo sumetimais vadybininkams turi būti leidžiama matyti tik tuos kaštų apskaitos duomenis, kurie yra susiję su konkrečiais savikainos objektais, už kuriuos jie atsakingi.</span><span class="sxs-lookup"><span data-stu-id="f273c-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="f273c-107">Yra keturi unikalūs kaštų apskaitos vaidmenys.</span><span class="sxs-lookup"><span data-stu-id="f273c-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="f273c-108">Vaidmens pavadinimas</span><span class="sxs-lookup"><span data-stu-id="f273c-108">Role name</span></span>               | <span data-ttu-id="f273c-109">Licencija</span><span class="sxs-lookup"><span data-stu-id="f273c-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="f273c-110">Savikainos apskaitos vadovas</span><span class="sxs-lookup"><span data-stu-id="f273c-110">Cost accounting manager</span></span> | <span data-ttu-id="f273c-111">Veikla</span><span class="sxs-lookup"><span data-stu-id="f273c-111">Activity</span></span>     |
| <span data-ttu-id="f273c-112">Išlaidų buhalteris</span><span class="sxs-lookup"><span data-stu-id="f273c-112">Cost accountant</span></span>         | <span data-ttu-id="f273c-113">„Operations‟</span><span class="sxs-lookup"><span data-stu-id="f273c-113">Operations</span></span>   |
| <span data-ttu-id="f273c-114">Išlaidų buhalteris</span><span class="sxs-lookup"><span data-stu-id="f273c-114">Cost accountant clerk</span></span>   | <span data-ttu-id="f273c-115">„Operations‟</span><span class="sxs-lookup"><span data-stu-id="f273c-115">Operations</span></span>   |
| <span data-ttu-id="f273c-116">Savikainos objekto valdiklis</span><span class="sxs-lookup"><span data-stu-id="f273c-116">Cost object controller</span></span>  | <span data-ttu-id="f273c-117">Komandos nariai</span><span class="sxs-lookup"><span data-stu-id="f273c-117">Team members</span></span> |

<span data-ttu-id="f273c-118">Šioje temoje paaiškinama, kaip vadybininkui priskirti vaidmenį **Savikainos objekto valdiklis**.</span><span class="sxs-lookup"><span data-stu-id="f273c-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="f273c-119">Kai vaidmuo **Savikainos objekto valdiklis** priskirtas vadybininkui, vadybininkas gali atlikti šias užduotis:</span><span class="sxs-lookup"><span data-stu-id="f273c-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="f273c-120">Įjunkite darbo sritį **Savikainos kontrolė** (kliente).</span><span class="sxs-lookup"><span data-stu-id="f273c-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="f273c-121">Detalizuokite ir peržiūrėkite prieigą prie puslapių, palaikančių detalizavimo patirtį.</span><span class="sxs-lookup"><span data-stu-id="f273c-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="f273c-122">Įjunkite darbo sritį **Savikainos kontrolė** (mobiliojoje programoje).</span><span class="sxs-lookup"><span data-stu-id="f273c-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="f273c-123">Vaidmuo **Savikainos objekto valdiklis** nekontroliuoja, kuriuos savikainos objektus gali įjungti vartotojas ir kurių duomenis jis gali peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="f273c-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="f273c-124">Eilutės lygio sauga teikiama per dimensijų hierarchijas ir prieigos sąrašo hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="f273c-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="f273c-125">Suteikti prieigos teises</span><span class="sxs-lookup"><span data-stu-id="f273c-125">Grant access rights</span></span>
<span data-ttu-id="f273c-126">Toliau pateiktame pavyzdyje parodyta, kaip gali atrodyti dimensijų hierarchija.</span><span class="sxs-lookup"><span data-stu-id="f273c-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="f273c-127">**Dimensijų hierarchijos informacija**</span><span class="sxs-lookup"><span data-stu-id="f273c-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="f273c-128">Dimensijų hierarchijos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="f273c-128">Dimension hierarchy name</span></span> | <span data-ttu-id="f273c-129">Dimensija</span><span class="sxs-lookup"><span data-stu-id="f273c-129">Dimension</span></span>    | <span data-ttu-id="f273c-130">Dimensijų hierarchijos tipo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="f273c-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="f273c-131">Prieigos sąrašo hierarchija</span><span class="sxs-lookup"><span data-stu-id="f273c-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="f273c-132">Organizacija</span><span class="sxs-lookup"><span data-stu-id="f273c-132">Organization</span></span>             | <span data-ttu-id="f273c-133">Išlaidų centrai</span><span class="sxs-lookup"><span data-stu-id="f273c-133">Cost centers</span></span> | <span data-ttu-id="f273c-134">Dimensijų klasifikavimo hierarchija</span><span class="sxs-lookup"><span data-stu-id="f273c-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="f273c-135">**Taip**</span><span class="sxs-lookup"><span data-stu-id="f273c-135">**Yes**</span></span>               |

<span data-ttu-id="f273c-136">Naudodami „FastTab“ skirtuką **Vartotojai** hierarchijos dizaino įrankyje kiekviename mazge galite įterpti vieną ar kelis vartotojų ID.</span><span class="sxs-lookup"><span data-stu-id="f273c-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="f273c-137">Vartotojai</span><span class="sxs-lookup"><span data-stu-id="f273c-137">Users</span></span>            | <span data-ttu-id="f273c-138">Dimensijos narių intervalai</span><span class="sxs-lookup"><span data-stu-id="f273c-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="f273c-139">**Mazgai**</span><span class="sxs-lookup"><span data-stu-id="f273c-139">**Nodes**</span></span>                         | <span data-ttu-id="f273c-140">**Vartotojo ID**</span><span class="sxs-lookup"><span data-stu-id="f273c-140">**User ID**</span></span>      | <span data-ttu-id="f273c-141">**Iš dimensijos nario**</span><span class="sxs-lookup"><span data-stu-id="f273c-141">**From dimension member**</span></span> | <span data-ttu-id="f273c-142">**Į dimensijos narį**</span><span class="sxs-lookup"><span data-stu-id="f273c-142">**To dimension member**</span></span> |
| <span data-ttu-id="f273c-143">Organizacija</span><span class="sxs-lookup"><span data-stu-id="f273c-143">Organization</span></span>                      | <span data-ttu-id="f273c-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="f273c-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="f273c-145">&nbsp;&nbsp;Administratorius</span><span class="sxs-lookup"><span data-stu-id="f273c-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="f273c-146">Balandžio</span><span class="sxs-lookup"><span data-stu-id="f273c-146">April</span></span>            |                           |                         |
| <span data-ttu-id="f273c-147">&nbsp;&nbsp;&nbsp;&nbsp;Finansai</span><span class="sxs-lookup"><span data-stu-id="f273c-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="f273c-148">Alicia</span><span class="sxs-lookup"><span data-stu-id="f273c-148">Alicia</span></span>           | <span data-ttu-id="f273c-149">CC002</span><span class="sxs-lookup"><span data-stu-id="f273c-149">CC002</span></span>                     | <span data-ttu-id="f273c-150">CC003</span><span class="sxs-lookup"><span data-stu-id="f273c-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="f273c-151">CC007</span><span class="sxs-lookup"><span data-stu-id="f273c-151">CC007</span></span>                     | <span data-ttu-id="f273c-152">CC007</span><span class="sxs-lookup"><span data-stu-id="f273c-152">CC007</span></span>                   |
| <span data-ttu-id="f273c-153">&nbsp;&nbsp;&nbsp;&nbsp;Personalas</span><span class="sxs-lookup"><span data-stu-id="f273c-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="f273c-154">Arnie</span><span class="sxs-lookup"><span data-stu-id="f273c-154">Arnie</span></span>            | <span data-ttu-id="f273c-155">CC001</span><span class="sxs-lookup"><span data-stu-id="f273c-155">CC001</span></span>                     | <span data-ttu-id="f273c-156">CC001</span><span class="sxs-lookup"><span data-stu-id="f273c-156">CC001</span></span>                   |
| <span data-ttu-id="f273c-157">&nbsp;&nbsp;Gamyba</span><span class="sxs-lookup"><span data-stu-id="f273c-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="f273c-158">David</span><span class="sxs-lookup"><span data-stu-id="f273c-158">David</span></span>            |                           |                         |
| <span data-ttu-id="f273c-159">&nbsp;&nbsp;&nbsp;&nbsp;Pakuotės</span><span class="sxs-lookup"><span data-stu-id="f273c-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="f273c-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="f273c-160">Ellen</span></span>            | <span data-ttu-id="f273c-161">CC005</span><span class="sxs-lookup"><span data-stu-id="f273c-161">CC005</span></span>                     | <span data-ttu-id="f273c-162">CC005</span><span class="sxs-lookup"><span data-stu-id="f273c-162">CC005</span></span>                   |
| <span data-ttu-id="f273c-163">&nbsp;&nbsp;&nbsp;&nbsp;Surinkimas</span><span class="sxs-lookup"><span data-stu-id="f273c-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="f273c-164">Chris</span><span class="sxs-lookup"><span data-stu-id="f273c-164">Chris</span></span>            | <span data-ttu-id="f273c-165">CC006</span><span class="sxs-lookup"><span data-stu-id="f273c-165">CC006</span></span>                     | <span data-ttu-id="f273c-166">CC006</span><span class="sxs-lookup"><span data-stu-id="f273c-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="f273c-167">Išlaidų buhalteriai turi būti priskirti aukščiausiam hierarchijos lygiui, kad galėtų matyti visus kaštų apskaitos įrašus.</span><span class="sxs-lookup"><span data-stu-id="f273c-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="f273c-168">Prieš taikant prieigos sąrašo hierarchiją ir jos saugos parametrus, puslapio **Savikainos apskaitos parametrai** (**Kaštų apskaita** > **Sąranka** > **Parametrai**) skirtuke **Bendra** turi būti nustatyta funkcijos **Įgalinti savikainos objekto dimensijos narių peržiūros prieigą** parinktis **Taip**.</span><span class="sxs-lookup"><span data-stu-id="f273c-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="f273c-169">Prieigos sąrašo hierarchijos parametrai naudojami norint valdyti toliau nurodytose srityse rodomus duomenis.</span><span class="sxs-lookup"><span data-stu-id="f273c-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="f273c-170">**Savikainos kontrolės** darbo sritis (kliente):</span><span class="sxs-lookup"><span data-stu-id="f273c-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="f273c-171">Detalizavimui naudojamų puslapių duomenys</span><span class="sxs-lookup"><span data-stu-id="f273c-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="f273c-172">**Savikainos kontrolės** darbo sritis (mobiliojoje programoje):</span><span class="sxs-lookup"><span data-stu-id="f273c-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="f273c-173">Likučiai kortelėse</span><span class="sxs-lookup"><span data-stu-id="f273c-173">Balances in cards</span></span>

- <span data-ttu-id="f273c-174">„Microsoft Power BI“:</span><span class="sxs-lookup"><span data-stu-id="f273c-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="f273c-175">Atliekant „Power BI‟ vizualizavimą rodomi duomenys</span><span class="sxs-lookup"><span data-stu-id="f273c-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="f273c-176">Į „Microsoft Dynamics 365 for Finance and Operations‟ leidimo „Enterprise‟ klientą įtrauktų duomenų „Power BI‟ vizualizavimai</span><span class="sxs-lookup"><span data-stu-id="f273c-176">Data Power BI visualizations that are embedded in the Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="f273c-177">Tam, kad prieigos sąrašo hierarchija galėtų turėti įtakos „Power BI‟, turi būti susieta prieigos sąrašo hierarchija ir „Power BI‟ eilučių lygio sauga.</span><span class="sxs-lookup"><span data-stu-id="f273c-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="f273c-178">Daugiau informacijos rasite dalyje [Kaštų apskaitos analizės „Power BI‟ turinio apsaugos nustatymas](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="f273c-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="f273c-179">Šioje temoje rodomos prieš naudojantis darbo sritimi **Savikainos kontrolė** turimos įdiegti būtinosios sąlygos.</span><span class="sxs-lookup"><span data-stu-id="f273c-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="f273c-180">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="f273c-180">See also</span></span>

- [<span data-ttu-id="f273c-181">Savikainos kontrolės darbo sritis</span><span class="sxs-lookup"><span data-stu-id="f273c-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="f273c-182">Dimensijų hierarchija</span><span class="sxs-lookup"><span data-stu-id="f273c-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="f273c-183">Kaštų apskaitos turinio paketo saugos nustatymas</span><span class="sxs-lookup"><span data-stu-id="f273c-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)

