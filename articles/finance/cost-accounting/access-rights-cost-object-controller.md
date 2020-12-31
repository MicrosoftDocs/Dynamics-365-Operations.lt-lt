---
title: Savikainos objekto valdiklių prieigos teisės
description: Šioje temoje pateikiama informacija apie savikainos objekto valdiklių prieigos teises.
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fd1ed875e5c6e3f8ada3b13ea8cc05f98526691d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446026"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="71bef-103">Savikainos objekto valdiklių prieigos teisės</span><span class="sxs-lookup"><span data-stu-id="71bef-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71bef-104">Darbo sritis **Savikainos kontrolė** yra centrinis taškas, kuriame vadybininkai gali peržiūrėti savo savikainos objektų našumą.</span><span class="sxs-lookup"><span data-stu-id="71bef-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="71bef-105">Naudodamiesi šia sritimi vadybininkai gali naudoti kaštų apskaitos duomenis net jei jie nėra išlaidų buhalterijai.</span><span class="sxs-lookup"><span data-stu-id="71bef-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="71bef-106">Saugumo sumetimais vadybininkams turi būti leidžiama matyti tik tuos kaštų apskaitos duomenis, kurie yra susiję su konkrečiais savikainos objektais, už kuriuos jie atsakingi.</span><span class="sxs-lookup"><span data-stu-id="71bef-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="71bef-107">Yra keturi unikalūs kaštų apskaitos vaidmenys.</span><span class="sxs-lookup"><span data-stu-id="71bef-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="71bef-108">Vaidmens pavadinimas</span><span class="sxs-lookup"><span data-stu-id="71bef-108">Role name</span></span>               | <span data-ttu-id="71bef-109">Licencija</span><span class="sxs-lookup"><span data-stu-id="71bef-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="71bef-110">Savikainos apskaitos vadovas</span><span class="sxs-lookup"><span data-stu-id="71bef-110">Cost accounting manager</span></span> | <span data-ttu-id="71bef-111">Veikla</span><span class="sxs-lookup"><span data-stu-id="71bef-111">Activity</span></span>     |
| <span data-ttu-id="71bef-112">Išlaidų buhalteris</span><span class="sxs-lookup"><span data-stu-id="71bef-112">Cost accountant</span></span>         | <span data-ttu-id="71bef-113">„Operations‟</span><span class="sxs-lookup"><span data-stu-id="71bef-113">Operations</span></span>   |
| <span data-ttu-id="71bef-114">Išlaidų buhalteris</span><span class="sxs-lookup"><span data-stu-id="71bef-114">Cost accountant clerk</span></span>   | <span data-ttu-id="71bef-115">„Operations‟</span><span class="sxs-lookup"><span data-stu-id="71bef-115">Operations</span></span>   |
| <span data-ttu-id="71bef-116">Savikainos objekto valdiklis</span><span class="sxs-lookup"><span data-stu-id="71bef-116">Cost object controller</span></span>  | <span data-ttu-id="71bef-117">Komandos nariai</span><span class="sxs-lookup"><span data-stu-id="71bef-117">Team members</span></span> |

<span data-ttu-id="71bef-118">Šioje temoje paaiškinama, kaip vadybininkui priskirti vaidmenį **Savikainos objekto valdiklis**.</span><span class="sxs-lookup"><span data-stu-id="71bef-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="71bef-119">Kai vaidmuo **Savikainos objekto valdiklis** priskirtas vadybininkui, vadybininkas gali atlikti šias užduotis:</span><span class="sxs-lookup"><span data-stu-id="71bef-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="71bef-120">Įjunkite darbo sritį **Savikainos kontrolė** (kliente).</span><span class="sxs-lookup"><span data-stu-id="71bef-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="71bef-121">Detalizuokite ir peržiūrėkite prieigą prie puslapių, palaikančių detalizavimo patirtį.</span><span class="sxs-lookup"><span data-stu-id="71bef-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="71bef-122">Įjunkite darbo sritį **Savikainos kontrolė** (mobiliojoje programoje).</span><span class="sxs-lookup"><span data-stu-id="71bef-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="71bef-123">Vaidmuo **Savikainos objekto valdiklis** nekontroliuoja, kuriuos savikainos objektus gali įjungti vartotojas ir kurių duomenis jis gali peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="71bef-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="71bef-124">Eilutės lygio sauga teikiama per dimensijų hierarchijas ir prieigos sąrašo hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="71bef-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="71bef-125">Suteikti prieigos teises</span><span class="sxs-lookup"><span data-stu-id="71bef-125">Grant access rights</span></span>
<span data-ttu-id="71bef-126">Toliau pateiktame pavyzdyje parodyta, kaip gali atrodyti dimensijų hierarchija.</span><span class="sxs-lookup"><span data-stu-id="71bef-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="71bef-127">**Dimensijų hierarchijos informacija**</span><span class="sxs-lookup"><span data-stu-id="71bef-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="71bef-128">Dimensijų hierarchijos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="71bef-128">Dimension hierarchy name</span></span> | <span data-ttu-id="71bef-129">Dimensija</span><span class="sxs-lookup"><span data-stu-id="71bef-129">Dimension</span></span>    | <span data-ttu-id="71bef-130">Dimensijų hierarchijos tipo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="71bef-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="71bef-131">Prieigos sąrašo hierarchija</span><span class="sxs-lookup"><span data-stu-id="71bef-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="71bef-132">Organizacija</span><span class="sxs-lookup"><span data-stu-id="71bef-132">Organization</span></span>             | <span data-ttu-id="71bef-133">Išlaidų centrai</span><span class="sxs-lookup"><span data-stu-id="71bef-133">Cost centers</span></span> | <span data-ttu-id="71bef-134">Dimensijų klasifikavimo hierarchija</span><span class="sxs-lookup"><span data-stu-id="71bef-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="71bef-135">**Taip**</span><span class="sxs-lookup"><span data-stu-id="71bef-135">**Yes**</span></span>               |

<span data-ttu-id="71bef-136">Naudodami „FastTab“ skirtuką **Vartotojai** hierarchijos dizaino įrankyje kiekviename mazge galite įterpti vieną ar kelis vartotojų ID.</span><span class="sxs-lookup"><span data-stu-id="71bef-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="71bef-137">Vartotojai</span><span class="sxs-lookup"><span data-stu-id="71bef-137">Users</span></span>            | <span data-ttu-id="71bef-138">Dimensijos narių intervalai</span><span class="sxs-lookup"><span data-stu-id="71bef-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="71bef-139">**Mazgai**</span><span class="sxs-lookup"><span data-stu-id="71bef-139">**Nodes**</span></span>                         | <span data-ttu-id="71bef-140">**Vartotojo ID**</span><span class="sxs-lookup"><span data-stu-id="71bef-140">**User ID**</span></span>      | <span data-ttu-id="71bef-141">**Iš dimensijos nario**</span><span class="sxs-lookup"><span data-stu-id="71bef-141">**From dimension member**</span></span> | <span data-ttu-id="71bef-142">**Į dimensijos narį**</span><span class="sxs-lookup"><span data-stu-id="71bef-142">**To dimension member**</span></span> |
| <span data-ttu-id="71bef-143">Organizacija</span><span class="sxs-lookup"><span data-stu-id="71bef-143">Organization</span></span>                      | <span data-ttu-id="71bef-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="71bef-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="71bef-145">&nbsp;&nbsp;Administratorius</span><span class="sxs-lookup"><span data-stu-id="71bef-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="71bef-146">Balandžio</span><span class="sxs-lookup"><span data-stu-id="71bef-146">April</span></span>            |                           |                         |
| <span data-ttu-id="71bef-147">&nbsp;&nbsp;&nbsp;&nbsp;Finansai</span><span class="sxs-lookup"><span data-stu-id="71bef-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="71bef-148">Alicia</span><span class="sxs-lookup"><span data-stu-id="71bef-148">Alicia</span></span>           | <span data-ttu-id="71bef-149">CC002</span><span class="sxs-lookup"><span data-stu-id="71bef-149">CC002</span></span>                     | <span data-ttu-id="71bef-150">CC003</span><span class="sxs-lookup"><span data-stu-id="71bef-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="71bef-151">CC007</span><span class="sxs-lookup"><span data-stu-id="71bef-151">CC007</span></span>                     | <span data-ttu-id="71bef-152">CC007</span><span class="sxs-lookup"><span data-stu-id="71bef-152">CC007</span></span>                   |
| <span data-ttu-id="71bef-153">&nbsp;&nbsp;&nbsp;&nbsp;Personalas</span><span class="sxs-lookup"><span data-stu-id="71bef-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="71bef-154">Arnie</span><span class="sxs-lookup"><span data-stu-id="71bef-154">Arnie</span></span>            | <span data-ttu-id="71bef-155">CC001</span><span class="sxs-lookup"><span data-stu-id="71bef-155">CC001</span></span>                     | <span data-ttu-id="71bef-156">CC001</span><span class="sxs-lookup"><span data-stu-id="71bef-156">CC001</span></span>                   |
| <span data-ttu-id="71bef-157">&nbsp;&nbsp;Gamyba</span><span class="sxs-lookup"><span data-stu-id="71bef-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="71bef-158">David</span><span class="sxs-lookup"><span data-stu-id="71bef-158">David</span></span>            |                           |                         |
| <span data-ttu-id="71bef-159">&nbsp;&nbsp;&nbsp;&nbsp;Pakuotės</span><span class="sxs-lookup"><span data-stu-id="71bef-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="71bef-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="71bef-160">Ellen</span></span>            | <span data-ttu-id="71bef-161">CC005</span><span class="sxs-lookup"><span data-stu-id="71bef-161">CC005</span></span>                     | <span data-ttu-id="71bef-162">CC005</span><span class="sxs-lookup"><span data-stu-id="71bef-162">CC005</span></span>                   |
| <span data-ttu-id="71bef-163">&nbsp;&nbsp;&nbsp;&nbsp;Surinkimas</span><span class="sxs-lookup"><span data-stu-id="71bef-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="71bef-164">Chris</span><span class="sxs-lookup"><span data-stu-id="71bef-164">Chris</span></span>            | <span data-ttu-id="71bef-165">CC006</span><span class="sxs-lookup"><span data-stu-id="71bef-165">CC006</span></span>                     | <span data-ttu-id="71bef-166">CC006</span><span class="sxs-lookup"><span data-stu-id="71bef-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="71bef-167">Išlaidų buhalteriai turi būti priskirti aukščiausiam hierarchijos lygiui, kad galėtų matyti visus kaštų apskaitos įrašus.</span><span class="sxs-lookup"><span data-stu-id="71bef-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="71bef-168">Prieš taikant prieigos sąrašo hierarchiją ir jos saugos parametrus, puslapio **Savikainos apskaitos parametrai** (**Kaštų apskaita** > **Sąranka** > **Parametrai**) skirtuke **Bendra** turi būti nustatyta funkcijos **Įgalinti savikainos objekto dimensijos narių peržiūros prieigą** parinktis **Taip**.</span><span class="sxs-lookup"><span data-stu-id="71bef-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="71bef-169">Prieigos sąrašo hierarchijos parametrai naudojami norint valdyti toliau nurodytose srityse rodomus duomenis.</span><span class="sxs-lookup"><span data-stu-id="71bef-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="71bef-170">**Savikainos kontrolės** darbo sritis (kliente):</span><span class="sxs-lookup"><span data-stu-id="71bef-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="71bef-171">Detalizavimui naudojamų puslapių duomenys</span><span class="sxs-lookup"><span data-stu-id="71bef-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="71bef-172">**Savikainos kontrolės** darbo sritis (mobiliojoje programoje):</span><span class="sxs-lookup"><span data-stu-id="71bef-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="71bef-173">Likučiai kortelėse</span><span class="sxs-lookup"><span data-stu-id="71bef-173">Balances in cards</span></span>

- <span data-ttu-id="71bef-174">Microsoft Power BI</span><span class="sxs-lookup"><span data-stu-id="71bef-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="71bef-175">Atliekant „Power BI“ vizualizavimą rodomi duomenys</span><span class="sxs-lookup"><span data-stu-id="71bef-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="71bef-176">Į „Dynamics 365 Finance“ klientą įtrauktų duomenų „Power BI“ vizualizavimai</span><span class="sxs-lookup"><span data-stu-id="71bef-176">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="71bef-177">Tam, kad prieigos sąrašo hierarchija galėtų turėti įtakos „Power BI“, turi būti susieta prieigos sąrašo hierarchija ir „Power BI“ eilučių lygio sauga.</span><span class="sxs-lookup"><span data-stu-id="71bef-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="71bef-178">Daugiau informacijos rasite dalyje [Kaštų apskaitos turinio paketo saugos nustatymas](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="71bef-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="71bef-179">Šioje temoje rodomos prieš naudojantis darbo sritimi **Savikainos kontrolė** turimos įdiegti būtinosios sąlygos.</span><span class="sxs-lookup"><span data-stu-id="71bef-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="71bef-180">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="71bef-180">Additional resources</span></span>

- [<span data-ttu-id="71bef-181">Savikainos kontrolės darbo sritis</span><span class="sxs-lookup"><span data-stu-id="71bef-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="71bef-182">Dimensijų hierarchija</span><span class="sxs-lookup"><span data-stu-id="71bef-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="71bef-183">Kaštų apskaitos turinio paketo saugos nustatymas</span><span class="sxs-lookup"><span data-stu-id="71bef-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)
