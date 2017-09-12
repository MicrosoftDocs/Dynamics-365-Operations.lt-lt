---
title: "Mobilioji darbo sritis Sąskaitos faktūros tvirtinimas"
description: "Šioje temoje pateikiama informacija apie mobiliąją darbo sritį Sąskaitos faktūros tvirtinimas Šioje darbo srityje pateikiamas sąskaitų faktūrų, kurios buvo jums priskirtos tiekėjo SF antraštės darbo eigos procese, sąrašas."
author: abruer
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 24818afbbdf328c8fd3eea691634db24e443b07b
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="d09c4-104">Mobilioji darbo sritis Sąskaitos faktūros tvirtinimas</span><span class="sxs-lookup"><span data-stu-id="d09c4-104">Invoice approvals mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d09c4-105">Šioje temoje pateikiama informacija apie mobiliąją darbo sritį **Sąskaitos faktūros tvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="d09c4-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="d09c4-106">Šioje darbo srityje pateikiamas sąskaitų faktūrų, kurios buvo jums priskirtos tiekėjo SF antraštės darbo eigos procese, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="d09c4-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="d09c4-107">Ši mobilioji darbo sritis skirta naudoti kartu su mobiliąja programa „Microsoft Dynamics 365 for Unified Operations“.</span><span class="sxs-lookup"><span data-stu-id="d09c4-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="d09c4-108">Apžvalga</span><span class="sxs-lookup"><span data-stu-id="d09c4-108">Overview</span></span>

<span data-ttu-id="d09c4-109">Mobilioji darbo sritis **Sąskaitos faktūros tvirtinimas** leidžia mokėtinų sumų tarnautojams ir vadovams peržiūrėti sąskaitas faktūras, jiems priskirtas vykdant tiekėjo SF antraštės darbo eigos procesą.</span><span class="sxs-lookup"><span data-stu-id="d09c4-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="d09c4-110">Galite peržiūrėti sąskaitos faktūros informaciją, ir netgi eilutės bei paskirstymo informaciją, kad galėtumėte priimti pagrįstus sprendimus dėl patvirtinimo.</span><span class="sxs-lookup"><span data-stu-id="d09c4-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="d09c4-111">Darbo srityje galite atlikti veiksmus ir perkelti sąskaitą faktūrą darbo eigos procese.</span><span class="sxs-lookup"><span data-stu-id="d09c4-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="d09c4-112">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="d09c4-112">Prerequisites</span></span>

<span data-ttu-id="d09c4-113">Tam, kad galėtumėte naudoti šią mobiliąją darbo sritį, turi būti laikomasi toliau nurodytų būtinųjų sąlygų.</span><span class="sxs-lookup"><span data-stu-id="d09c4-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d09c4-114">Būtinoji sąlyga</span><span class="sxs-lookup"><span data-stu-id="d09c4-114">Prerequisite</span></span></th>
<th><span data-ttu-id="d09c4-115">Vaidmuo</span><span class="sxs-lookup"><span data-stu-id="d09c4-115">Role</span></span></th>
<th><span data-ttu-id="d09c4-116">aprašymas</span><span class="sxs-lookup"><span data-stu-id="d09c4-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d09c4-117">Jūsų organizacijoje turi būti įdiegtas „Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition‟ 2017 m. liepos mėn. naujinimas.</span><span class="sxs-lookup"><span data-stu-id="d09c4-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="d09c4-118">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="d09c4-118">System administrator</span></span></td>
<td><span data-ttu-id="d09c4-119">Žr. <a href="../deployment/deploy-demo-environment.md">Demonstracinės aplinkos diegimas</a>.</span><span class="sxs-lookup"><span data-stu-id="d09c4-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="d09c4-120">Mobilioji darbo sritis <strong>Sąskaitos faktūros tvirtinimas</strong> turi būti paskelbta.</span><span class="sxs-lookup"><span data-stu-id="d09c4-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="d09c4-121">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="d09c4-121">System administrator</span></span></td>
<td><span data-ttu-id="d09c4-122">Žr. <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiliosios darbo srities publikavimas</a>.</span><span class="sxs-lookup"><span data-stu-id="d09c4-122">See <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="d09c4-123">Mobiliosios programos atsisiuntimas ir diegimas</span><span class="sxs-lookup"><span data-stu-id="d09c4-123">Download and install the mobile app</span></span>

<span data-ttu-id="d09c4-124">Atsisiųskite ir įdiekite mobiliąją programą „Dynamics 365 for Unified Operations“:</span><span class="sxs-lookup"><span data-stu-id="d09c4-124">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="d09c4-125">Telefonams „Android“</span><span class="sxs-lookup"><span data-stu-id="d09c4-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="d09c4-126">Telefonams „iPhone“</span><span class="sxs-lookup"><span data-stu-id="d09c4-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="d09c4-127">Prisijunkite prie mobiliosios programos</span><span class="sxs-lookup"><span data-stu-id="d09c4-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="d09c4-128">Paleiskite programą savo mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="d09c4-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="d09c4-129">Įveskite savo „Microsoft Dynamics 365“ URL.</span><span class="sxs-lookup"><span data-stu-id="d09c4-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="d09c4-130">Kai prisijungsite pirmą kartą, bus rodomas raginimas įvesti savo vartotojo vardą ir slaptažodį.</span><span class="sxs-lookup"><span data-stu-id="d09c4-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="d09c4-131">Įveskite savo kredencialus.</span><span class="sxs-lookup"><span data-stu-id="d09c4-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="d09c4-132">Prisijungus rodomos galimos jūsų įmonės darbo sritys.</span><span class="sxs-lookup"><span data-stu-id="d09c4-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="d09c4-133">Atkreipkite dėmesį, kad sistemos administratoriui paskelbus naują darbo sritį vėliau turėsite atnaujinti mobiliųjų darbo sričių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="d09c4-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="d09c4-134">[![Patraukite norėdami atnaujinti](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="d09c4-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="d09c4-135">Sąskaitų faktūrų tvirtinimas naudojant mobiliąją darbo sritį Sąskaitos faktūros tvirtinimas</span><span class="sxs-lookup"><span data-stu-id="d09c4-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="d09c4-136">Savo mobiliajame įrenginyje pasirinkite darbo sritį **Sąskaitos faktūros tvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="d09c4-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="d09c4-137">Pasirinkite sąskaitą faktūrą, kuri jums buvo priskirta tiekėjo SF antraštės darbo eigos proceso.</span><span class="sxs-lookup"><span data-stu-id="d09c4-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="d09c4-138">Puslapyje **Sąskaitos faktūros informacija** peržiūrėkite sąskaitos faktūros antraštės informaciją, pvz., tiekėjo ir datos informaciją.</span><span class="sxs-lookup"><span data-stu-id="d09c4-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="d09c4-139">Pasirinkite sąskaitos faktūros eilutę, kad peržiūrėtumėte išsamią informaciją apie ją rodinyje **Sąskaitos faktūros eilutės informacija**.</span><span class="sxs-lookup"><span data-stu-id="d09c4-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="d09c4-140">Rodinyje **Sąskaitos faktūros eilutės informacija** pasirinkite **Paskirstymai**, kad būtų parodyti eilutės paskirstymai.</span><span class="sxs-lookup"><span data-stu-id="d09c4-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="d09c4-141">Čia galite peržiūrėti sąskaitos faktūros eilutės apskaitą.</span><span class="sxs-lookup"><span data-stu-id="d09c4-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="d09c4-142">Rodoma informacija apima finansinių dimensijų ir pagrindinės sąskaitos informaciją.</span><span class="sxs-lookup"><span data-stu-id="d09c4-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="d09c4-143">Puslapyje **Sąskaitos faktūros informacija** pasirinkite **Paskirstymai**, kad būtų parodyti visi paskirstymai.</span><span class="sxs-lookup"><span data-stu-id="d09c4-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="d09c4-144">Čia galite peržiūrėti visos sąskaitos faktūros apskaitą.</span><span class="sxs-lookup"><span data-stu-id="d09c4-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="d09c4-145">Rodoma informacija apima finansinių dimensijų ir pagrindinių sąskaitų informaciją.</span><span class="sxs-lookup"><span data-stu-id="d09c4-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="d09c4-146">Pasirinkite **Priedai**, kad peržiūrėtumėte prie sąskaitos faktūros pridėtas pastabas ar failus.</span><span class="sxs-lookup"><span data-stu-id="d09c4-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="d09c4-147">Puslapyje **Sąskaitos faktūros informacija** pasirinkite atitinkamą darbo eigos veiksmą, kad užbaigtumėte savo peržiūros procesą.</span><span class="sxs-lookup"><span data-stu-id="d09c4-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="d09c4-148">Pasirinkite **Atlikta**.</span><span class="sxs-lookup"><span data-stu-id="d09c4-148">Select **Done**.</span></span>

