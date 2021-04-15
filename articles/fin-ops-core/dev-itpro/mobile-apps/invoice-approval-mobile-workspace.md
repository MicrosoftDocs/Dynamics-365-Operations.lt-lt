---
title: Mobilioji darbo sritis Sąskaitos faktūros tvirtinimas
description: Šioje temoje pateikiama informacija apie mobiliąją darbo sritį Sąskaitos faktūros tvirtinimas
author: abruer
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: c3414d6ef5f2df62f37f1ef2e7e2ff43ce040e5e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752255"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="ce05d-103">Mobilioji darbo sritis Sąskaitos faktūros tvirtinimas</span><span class="sxs-lookup"><span data-stu-id="ce05d-103">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce05d-104">Šioje temoje pateikiama informacija apie mobiliąją darbo sritį **Sąskaitos faktūros tvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="ce05d-104">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="ce05d-105">Šioje darbo srityje pateikiamas sąskaitų faktūrų, kurios buvo jums priskirtos tiekėjo SF antraštės darbo eigos procese, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="ce05d-105">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="ce05d-106">Ši mobili darbo sritis skirta naudoti kartu su mobiliųjų įrenginių programėle „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="ce05d-106">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="ce05d-107">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="ce05d-107">Overview</span></span>

<span data-ttu-id="ce05d-108">Mobilioji darbo sritis **Sąskaitos faktūros tvirtinimas** leidžia mokėtinų sumų tarnautojams ir vadovams peržiūrėti sąskaitas faktūras, jiems priskirtas vykdant tiekėjo SF antraštės darbo eigos procesą.</span><span class="sxs-lookup"><span data-stu-id="ce05d-108">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="ce05d-109">Galite peržiūrėti sąskaitos faktūros informaciją, ir netgi eilutės bei paskirstymo informaciją, kad galėtumėte priimti pagrįstus sprendimus dėl patvirtinimo.</span><span class="sxs-lookup"><span data-stu-id="ce05d-109">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="ce05d-110">Darbo srityje galite atlikti veiksmus ir perkelti sąskaitą faktūrą darbo eigos procese.</span><span class="sxs-lookup"><span data-stu-id="ce05d-110">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="ce05d-111">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="ce05d-111">Prerequisites</span></span>

<span data-ttu-id="ce05d-112">Tam, kad galėtumėte naudoti šią mobiliąją darbo sritį, turi būti laikomasi toliau nurodytų būtinųjų sąlygų.</span><span class="sxs-lookup"><span data-stu-id="ce05d-112">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ce05d-113">Būtinoji sąlyga</span><span class="sxs-lookup"><span data-stu-id="ce05d-113">Prerequisite</span></span></th>
<th><span data-ttu-id="ce05d-114">Vaidmuo</span><span class="sxs-lookup"><span data-stu-id="ce05d-114">Role</span></span></th>
<th><span data-ttu-id="ce05d-115">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="ce05d-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce05d-116">Jūsų organizacijoje turi būti visuotinai įdiegta „Microsoft Dynamics 365 Finance“.</span><span class="sxs-lookup"><span data-stu-id="ce05d-116">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="ce05d-117">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="ce05d-117">System administrator</span></span></td>
<td><span data-ttu-id="ce05d-118">Žr. <a href="../deployment/deploy-demo-environment.md">Demonstracinės aplinkos diegimas</a>.</span><span class="sxs-lookup"><span data-stu-id="ce05d-118">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce05d-119">Mobilioji darbo sritis <strong>Sąskaitos faktūros tvirtinimas</strong> turi būti paskelbta.</span><span class="sxs-lookup"><span data-stu-id="ce05d-119">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="ce05d-120">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="ce05d-120">System administrator</span></span></td>
<td><span data-ttu-id="ce05d-121">Žr. <a href="publish-mobile-workspace.md">Mobiliosios darbo srities publikavimas</a>.</span><span class="sxs-lookup"><span data-stu-id="ce05d-121">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="ce05d-122">Mobiliosios programos atsisiuntimas ir diegimas</span><span class="sxs-lookup"><span data-stu-id="ce05d-122">Download and install the mobile app</span></span>

<span data-ttu-id="ce05d-123">Mobiliosios programos „Finance and Operations“ atsisiuntimas ir diegimas.</span><span class="sxs-lookup"><span data-stu-id="ce05d-123">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="ce05d-124">„Android“ telefonams</span><span class="sxs-lookup"><span data-stu-id="ce05d-124">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="ce05d-125">„iPhone“ telefonams</span><span class="sxs-lookup"><span data-stu-id="ce05d-125">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="ce05d-126">Prisijunkite prie mobiliosios programos</span><span class="sxs-lookup"><span data-stu-id="ce05d-126">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="ce05d-127">Paleiskite programą savo mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="ce05d-127">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="ce05d-128">Įveskite savo „Microsoft Dynamics 365“ URL.</span><span class="sxs-lookup"><span data-stu-id="ce05d-128">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="ce05d-129">Kai prisijungsite pirmą kartą, bus rodomas raginimas įvesti savo vartotojo vardą ir slaptažodį.</span><span class="sxs-lookup"><span data-stu-id="ce05d-129">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="ce05d-130">Įveskite savo kredencialus.</span><span class="sxs-lookup"><span data-stu-id="ce05d-130">Enter your credentials.</span></span>
4.  <span data-ttu-id="ce05d-131">Prisijungus rodomos galimos jūsų įmonės darbo sritys.</span><span class="sxs-lookup"><span data-stu-id="ce05d-131">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="ce05d-132">Atkreipkite dėmesį, kad sistemos administratoriui paskelbus naują darbo sritį vėliau turėsite atnaujinti mobiliųjų darbo sričių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="ce05d-132">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="ce05d-133">[![Patraukite norėdami atnaujinti](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="ce05d-133">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="ce05d-134">Sąskaitų faktūrų tvirtinimas naudojant mobiliąją darbo sritį Sąskaitos faktūros tvirtinimas</span><span class="sxs-lookup"><span data-stu-id="ce05d-134">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="ce05d-135">Savo mobiliajame įrenginyje pasirinkite darbo sritį **Sąskaitos faktūros tvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="ce05d-135">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="ce05d-136">Pasirinkite sąskaitą faktūrą, kuri jums buvo priskirta tiekėjo SF antraštės darbo eigos proceso.</span><span class="sxs-lookup"><span data-stu-id="ce05d-136">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="ce05d-137">Puslapyje **Sąskaitos faktūros informacija** peržiūrėkite sąskaitos faktūros antraštės informaciją, pvz., tiekėjo ir datos informaciją.</span><span class="sxs-lookup"><span data-stu-id="ce05d-137">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="ce05d-138">Pasirinkite sąskaitos faktūros eilutę, kad peržiūrėtumėte išsamią informaciją apie ją rodinyje **Sąskaitos faktūros eilutės informacija**.</span><span class="sxs-lookup"><span data-stu-id="ce05d-138">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="ce05d-139">Rodinyje **Sąskaitos faktūros eilutės informacija** pasirinkite **Paskirstymai**, kad būtų parodyti eilutės paskirstymai.</span><span class="sxs-lookup"><span data-stu-id="ce05d-139">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="ce05d-140">Čia galite peržiūrėti sąskaitos faktūros eilutės apskaitą.</span><span class="sxs-lookup"><span data-stu-id="ce05d-140">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="ce05d-141">Rodoma informacija apima finansinių dimensijų ir pagrindinės sąskaitos informaciją.</span><span class="sxs-lookup"><span data-stu-id="ce05d-141">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="ce05d-142">Puslapyje **Sąskaitos faktūros informacija** pasirinkite **Paskirstymai**, kad būtų parodyti visi paskirstymai.</span><span class="sxs-lookup"><span data-stu-id="ce05d-142">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="ce05d-143">Čia galite peržiūrėti visos sąskaitos faktūros apskaitą.</span><span class="sxs-lookup"><span data-stu-id="ce05d-143">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="ce05d-144">Rodoma informacija apima finansinių dimensijų ir pagrindinių sąskaitų informaciją.</span><span class="sxs-lookup"><span data-stu-id="ce05d-144">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="ce05d-145">Pasirinkite **Priedai**, kad peržiūrėtumėte prie sąskaitos faktūros pridėtas pastabas ar failus.</span><span class="sxs-lookup"><span data-stu-id="ce05d-145">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="ce05d-146">Puslapyje **Sąskaitos faktūros informacija** pasirinkite atitinkamą darbo eigos veiksmą, kad užbaigtumėte savo peržiūros procesą.</span><span class="sxs-lookup"><span data-stu-id="ce05d-146">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="ce05d-147">Pasirinkite **Atlikta**.</span><span class="sxs-lookup"><span data-stu-id="ce05d-147">Select **Done**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]