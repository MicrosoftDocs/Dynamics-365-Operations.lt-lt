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
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: af6ddc86bb6313387aa9c6ccc347d2a1c5fac50a
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154487"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="d2c5e-103">Savikainos objekto valdiklių prieigos teisės</span><span class="sxs-lookup"><span data-stu-id="d2c5e-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2c5e-104">Darbo sritis **Savikainos kontrolė** yra centrinis taškas, kuriame vadybininkai gali peržiūrėti savo savikainos objektų našumą.</span><span class="sxs-lookup"><span data-stu-id="d2c5e-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="d2c5e-105">Naudodamiesi šia sritimi vadybininkai gali naudoti kaštų apskaitos duomenis net jei jie nėra išlaidų buhalterijai.</span><span class="sxs-lookup"><span data-stu-id="d2c5e-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="d2c5e-106">Saugumo sumetimais vadybininkams turi būti leidžiama matyti tik tuos kaštų apskaitos duomenis, kurie yra susiję su konkrečiais savikainos objektais, už kuriuos jie atsakingi.</span><span class="sxs-lookup"><span data-stu-id="d2c5e-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="d2c5e-107">Yra keturi unikalūs kaštų apskaitos vaidmenys.</span><span class="sxs-lookup"><span data-stu-id="d2c5e-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="d2c5e-108">Vaidmens pavadinimas</span><span class="sxs-lookup"><span data-stu-id="d2c5e-108">Role name</span></span>               | <span data-ttu-id="d2c5e-109">Licencija</span><span class="sxs-lookup"><span data-stu-id="d2c5e-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="d2c5e-110">Savikainos apskaitos vadovas</span><span class="sxs-lookup"><span data-stu-id="d2c5e-110">Cost accounting manager</span></span> | <span data-ttu-id="d2c5e-111">Veikla</span><span class="sxs-lookup"><span data-stu-id="d2c5e-111">Activity</span></span>     |
| <span data-ttu-id="d2c5e-112">Išlaidų buhalteris</span><span class="sxs-lookup"><span data-stu-id="d2c5e-112">Cost accountant</span></span>         | <span data-ttu-id="d2c5e-113">„Operations‟</span><span class="sxs-lookup"><span data-stu-id="d2c5e-113">Operations</span></span>   |
| <span data-ttu-id="d2c5e-114">Išlaidų buhalteris</span><span class="sxs-lookup"><span data-stu-id="d2c5e-114">Cost accountant clerk</span></span>   | <span data-ttu-id="d2c5e-115">„Operations‟</span><span class="sxs-lookup"><span data-stu-id="d2c5e-115">Operations</span></span>   |
| <span data-ttu-id="d2c5e-116">Savikainos objekto valdiklis</span><span class="sxs-lookup"><span data-stu-id="d2c5e-116">Cost object controller</span></span>  | <span data-ttu-id="d2c5e-117">Komandos nariai</span><span class="sxs-lookup"><span data-stu-id="d2c5e-117">Team members</span></span> |

<span data-ttu-id="d2c5e-118">Šioje temoje paaiškinama, kaip vadybininkui priskirti vaidmenį **Savikainos objekto valdiklis**.</span><span class="sxs-lookup"><span data-stu-id="d2c5e-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="d2c5e-119">Kai vaidmuo **Savikainos objekto valdiklis** priskirtas vadybininkui, vadybininkas gali atlikti šias užduotis:</span><span class="sxs-lookup"><span data-stu-id="d2c5e-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="d2c5e-120">Įjunkite darbo sritį **Savikainos kontrolė** (kliente).</span><span class="sxs-lookup"><span data-stu-id="d2c5e-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="d2c5e-121">Detalizuokite ir peržiūrėkite prieigą prie puslapių, palaikančių detalizavimo patirtį.</span><span class="sxs-lookup"><span data-stu-id="d2c5e-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="d2c5e-122">Įjunkite darbo sritį **Savikainos kontrolė** (mobiliojoje programoje).</span><span class="sxs-lookup"><span data-stu-id="d2c5e-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="d2c5e-123">Vaidmuo **Savikainos objekto valdiklis** nekontroliuoja, kuriuos savikainos objektus gali įjungti vartotojas ir kurių duomenis jis gali peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="d2c5e-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="d2c5e-124">Eilutės lygio sauga teikiama per dimensijų hierarchijas ir prieigos sąrašo hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="d2c5e-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="d2c5e-125">Suteikti prieigos teises</span><span class="sxs-lookup"><span data-stu-id="d2c5e-125">Grant access rights</span></span>
<span data-ttu-id="d2c5e-126">Toliau pateiktame pavyzdyje parodyta, kaip gali atrodyti dimensijų hierarchija.</span><span class="sxs-lookup"><span data-stu-id="d2c5e-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="d2c5e-127">**Dimensijų hierarchijos informacija**</span><span class="sxs-lookup"><span data-stu-id="d2c5e-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="d2c5e-128">Dimensijų hierarchijos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="d2c5e-128">Dimension hierarchy name</span></span> | <span data-ttu-id="d2c5e-129">Dimensija</span><span class="sxs-lookup"><span data-stu-id="d2c5e-129">Dimension</span></span>    | <span data-ttu-id="d2c5e-130">Dimensijų hierarchijos tipo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="d2c5e-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="d2c5e-131">Prieigos sąrašo hierarchija</span><span class="sxs-lookup"><span data-stu-id="d2c5e-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="d2c5e-132">Organizacija</span><span class="sxs-lookup"><span data-stu-id="d2c5e-132">Organization</span></span>             | <span data-ttu-id="d2c5e-133">Išlaidų centrai</span><span class="sxs-lookup"><span data-stu-id="d2c5e-133">Cost centers</span></span> | <span data-ttu-id="d2c5e-134">Dimensijų klasifikavimo hierarchija</span><span class="sxs-lookup"><span data-stu-id="d2c5e-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="d2c5e-135">**Taip**</span><span class="sxs-lookup"><span data-stu-id="d2c5e-135">**Yes**</span></span>               |

<span data-ttu-id="d2c5e-136">Naudodami „FastTab“ skirtuką **Vartotojai** hierarchijos dizaino įrankyje kiekviename mazge galite įterpti vieną ar kelis vartotojų ID.</span><span class="sxs-lookup"><span data-stu-id="d2c5e-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="d2c5e-137">Vartotojai</span><span class="sxs-lookup"><span data-stu-id="d2c5e-137">Users</span></span>            | <span data-ttu-id="d2c5e-138">Dimensijos narių intervalai</span><span class="sxs-lookup"><span data-stu-id="d2c5e-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="d2c5e-139">**Mazgai**</span><span class="sxs-lookup"><span data-stu-id="d2c5e-139">**Nodes**</span></span>                         | <span data-ttu-id="d2c5e-140">**Vartotojo ID**</span><span class="sxs-lookup"><span data-stu-id="d2c5e-140">**User ID**</span></span>      | <span data-ttu-id="d2c5e-141">**Iš dimensijos nario**</span><span class="sxs-lookup"><span data-stu-id="d2c5e-141">**From dimension member**</span></span> | <span data-ttu-id="d2c5e-142">**Į dimensijos narį**</span><span class="sxs-lookup"><span data-stu-id="d2c5e-142">**To dimension member**</span></span> |
| <span data-ttu-id="d2c5e-143">Organizacija</span><span class="sxs-lookup"><span data-stu-id="d2c5e-143">Organization</span></span>                      | <span data-ttu-id="d2c5e-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="d2c5e-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="d2c5e-145">&nbsp;&nbsp;Administratorius</span><span class="sxs-lookup"><span data-stu-id="d2c5e-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="d2c5e-146">Balandžio</span><span class="sxs-lookup"><span data-stu-id="d2c5e-146">April</span></span>            |                           |                         |
| <span data-ttu-id="d2c5e-147">&nbsp;&nbsp;&nbsp;&nbsp;Finansai</span><span class="sxs-lookup"><span data-stu-id="d2c5e-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="d2c5e-148">Alicia</span><span class="sxs-lookup"><span data-stu-id="d2c5e-148">Alicia</span></span>           | <span data-ttu-id="d2c5e-149">CC002</span><span class="sxs-lookup"><span data-stu-id="d2c5e-149">CC002</span></span>                     | <span data-ttu-id="d2c5e-150">CC003</span><span class="sxs-lookup"><span data-stu-id="d2c5e-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="d2c5e-151">CC007</span><span class="sxs-lookup"><span data-stu-id="d2c5e-151">CC007</span></span>                     | <span data-ttu-id="d2c5e-152">CC007</span><span class="sxs-lookup"><span data-stu-id="d2c5e-152">CC007</span></span>                   |
| <span data-ttu-id="d2c5e-153">&nbsp;&nbsp;&nbsp;&nbsp;Personalas</span><span class="sxs-lookup"><span data-stu-id="d2c5e-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="d2c5e-154">Arnie</span><span class="sxs-lookup"><span data-stu-id="d2c5e-154">Arnie</span></span>            | <span data-ttu-id="d2c5e-155">CC001</span><span class="sxs-lookup"><span data-stu-id="d2c5e-155">CC001</span></span>                     | <span data-ttu-id="d2c5e-156">CC001</span><span class="sxs-lookup"><span data-stu-id="d2c5e-156">CC001</span></span>                   |
| <span data-ttu-id="d2c5e-157">&nbsp;&nbsp;Gamyba</span><span class="sxs-lookup"><span data-stu-id="d2c5e-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="d2c5e-158">David</span><span class="sxs-lookup"><span data-stu-id="d2c5e-158">David</span></span>            |                           |                         |
| <span data-ttu-id="d2c5e-159">&nbsp;&nbsp;&nbsp;&nbsp;Pakuotės</span><span class="sxs-lookup"><span data-stu-id="d2c5e-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="d2c5e-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="d2c5e-160">Ellen</span></span>            | <span data-ttu-id="d2c5e-161">CC005</span><span class="sxs-lookup"><span data-stu-id="d2c5e-161">CC005</span></span>                     | <span data-ttu-id="d2c5e-162">CC005</span><span class="sxs-lookup"><span data-stu-id="d2c5e-162">CC005</span></span>                   |
| <span data-ttu-id="d2c5e-163">&nbsp;&nbsp;&nbsp;&nbsp;Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d2c5e-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="d2c5e-164">Chris</span><span class="sxs-lookup"><span data-stu-id="d2c5e-164">Chris</span></span>            | <span data-ttu-id="d2c5e-165">CC006</span><span class="sxs-lookup"><span data-stu-id="d2c5e-165">CC006</span></span>                     | <span data-ttu-id="d2c5e-166">CC006</span><span class="sxs-lookup"><span data-stu-id="d2c5e-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="d2c5e-167">Išlaidų buhalteriai turi būti priskirti aukščiausiam hierarchijos lygiui, kad galėtų matyti visus kaštų apskaitos įrašus.</span><span class="sxs-lookup"><span data-stu-id="d2c5e-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="d2c5e-168">Prieš taikant prieigos sąrašo hierarchiją ir jos saugos parametrus, puslapio **Savikainos apskaitos parametrai** (**Kaštų apskaita** > **Sąranka** > **Parametrai**) skirtuke **Bendra** turi būti nustatyta funkcijos **Įgalinti savikainos objekto dimensijos narių peržiūros prieigą** parinktis **Taip**.</span><span class="sxs-lookup"><span data-stu-id="d2c5e-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="d2c5e-169">Prieigos sąrašo hierarchijos parametrai naudojami norint valdyti toliau nurodytose srityse rodomus duomenis.</span><span class="sxs-lookup"><span data-stu-id="d2c5e-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="d2c5e-170">**Savikainos kontrolės** darbo sritis (kliente):</span><span class="sxs-lookup"><span data-stu-id="d2c5e-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="d2c5e-171">Detalizavimui naudojamų puslapių duomenys</span><span class="sxs-lookup"><span data-stu-id="d2c5e-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="d2c5e-172">**Savikainos kontrolės** darbo sritis (mobiliojoje programoje):</span><span class="sxs-lookup"><span data-stu-id="d2c5e-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="d2c5e-173">Likučiai kortelėse</span><span class="sxs-lookup"><span data-stu-id="d2c5e-173">Balances in cards</span></span>

- <span data-ttu-id="d2c5e-174">Microsoft Power BI</span><span class="sxs-lookup"><span data-stu-id="d2c5e-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="d2c5e-175">Atliekant „Power BI“ vizualizavimą rodomi duomenys</span><span class="sxs-lookup"><span data-stu-id="d2c5e-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="d2c5e-176">Į „Dynamics 365 Finance“ klientą įtrauktų duomenų „Power BI“ vizualizavimai</span><span class="sxs-lookup"><span data-stu-id="d2c5e-176">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="d2c5e-177">Tam, kad prieigos sąrašo hierarchija galėtų turėti įtakos „Power BI“, turi būti susieta prieigos sąrašo hierarchija ir „Power BI“ eilučių lygio sauga.</span><span class="sxs-lookup"><span data-stu-id="d2c5e-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="d2c5e-178">Daugiau informacijos rasite dalyje [Kaštų apskaitos turinio paketo saugos nustatymas](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="d2c5e-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="d2c5e-179">Šioje temoje rodomos prieš naudojantis darbo sritimi **Savikainos kontrolė** turimos įdiegti būtinosios sąlygos.</span><span class="sxs-lookup"><span data-stu-id="d2c5e-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="d2c5e-180">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d2c5e-180">Additional resources</span></span>

- [<span data-ttu-id="d2c5e-181">Savikainos kontrolės darbo sritis</span><span class="sxs-lookup"><span data-stu-id="d2c5e-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="d2c5e-182">Dimensijų hierarchija</span><span class="sxs-lookup"><span data-stu-id="d2c5e-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="d2c5e-183">Kaštų apskaitos turinio paketo saugos nustatymas</span><span class="sxs-lookup"><span data-stu-id="d2c5e-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)
