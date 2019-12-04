---
title: Duomenų integravimo trikčių šalinimo vadovas
description: Šioje temoje pateikiama duomenų integravimo tarp „Finance and Operations“ programų ir „Common Data Service” trikčių šalinimo informacija.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 35c0a1e6342008bc2ee6ff25a1663e199c8cb985
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771030"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="6e67c-103">Duomenų integravimo trikčių šalinimo vadovas</span><span class="sxs-lookup"><span data-stu-id="6e67c-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="6e67c-104">Įjunkite priedo sekimo žurnalus programoje „Common Data Service“ ir patikrinkite dvigubo rašymo priedo klaidų išsamią informaciją</span><span class="sxs-lookup"><span data-stu-id="6e67c-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e67c-105">Jei atlikdami dvigubo rašymo sinchronizavimą susiduriate su problema arba klaida, atlikite šiuos veiksmus, kad patikrintumėte klaidas sekimo žurnale.</span><span class="sxs-lookup"><span data-stu-id="6e67c-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="6e67c-106">Prieš tikrindami klaidas, turite įjungti priedo sekimo žurnalus.</span><span class="sxs-lookup"><span data-stu-id="6e67c-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="6e67c-107">Instrukcijas rasite vadovo [Mokymo priemonė: įrašykite ir užregistruokite priedą](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) skyriuje „Sekimo žurnalų peržiūrėjimas“.</span><span class="sxs-lookup"><span data-stu-id="6e67c-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="6e67c-108">Dabar galite tikrinti klaidas.</span><span class="sxs-lookup"><span data-stu-id="6e67c-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="6e67c-109">Prisijunkite prie „Microsoft Dynamics 365 Sales“.</span><span class="sxs-lookup"><span data-stu-id="6e67c-109">Sign in to Microsoft Dynamics 365 Sales.</span></span>
3. <span data-ttu-id="6e67c-110">Pasirinkite mygtuką **Parametrai** (krumpliaračio simbolis) ir pasirinkite **Išplėstiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="6e67c-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="6e67c-111">Meniu **Parametrai** pasirinkite **Tinkinimas\> Priedo sekimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="6e67c-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="6e67c-112">Pasirinkite **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** kaip tipo pavadinimą, kad būtų rodoma išsami klaidos informacija.</span><span class="sxs-lookup"><span data-stu-id="6e67c-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors"></a><span data-ttu-id="6e67c-113">Tikrinti dvigubo rašymo sinchronizavimo klaidas</span><span class="sxs-lookup"><span data-stu-id="6e67c-113">Inspect dual-write synchronization errors</span></span>

<span data-ttu-id="6e67c-114">Atlikite šiuos veiksmus, kad galėtumėte tikrinti klaidas per testavimą.</span><span class="sxs-lookup"><span data-stu-id="6e67c-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="6e67c-115">Prisijunkite prie „Microsoft Dynamics“ portale „Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="6e67c-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="6e67c-116">Atidarykite LCS projektą, kad atliktumėte dvigubo rašymo testavimą.</span><span class="sxs-lookup"><span data-stu-id="6e67c-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="6e67c-117">Pasirinkite **Aplinkos diegimo debesyje įrankis**.</span><span class="sxs-lookup"><span data-stu-id="6e67c-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="6e67c-118">Sukurkite nuotolinį darbalaukį, skirtą programos virtualiajai mašinai (VM), pasinaudoję LCS rodoma vietine paskyra.</span><span class="sxs-lookup"><span data-stu-id="6e67c-118">Make a Remote desktop connection to the application virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="6e67c-119">Atidarykite įvykių peržiūros programą.</span><span class="sxs-lookup"><span data-stu-id="6e67c-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="6e67c-120">Eikite į **Programų ir paslaugų žurnalai\> „Microsoft“\> „Dynamics“\> „AX-DualWriteSync“\> Veikia**</span><span class="sxs-lookup"><span data-stu-id="6e67c-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="6e67c-121">Rodomos klaidos ir išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="6e67c-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a><span data-ttu-id="6e67c-122">Atsiekite vieną „Common Data Service“ aplinką nuo programos ir susiekite kitą aplinką.</span><span class="sxs-lookup"><span data-stu-id="6e67c-122">Unlink one Common Data Service environment from the application and link another environment</span></span>

<span data-ttu-id="6e67c-123">Norėdami atnaujinti saitus atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6e67c-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="6e67c-124">Eikite į programos aplinką.</span><span class="sxs-lookup"><span data-stu-id="6e67c-124">Go to the application environment.</span></span>
2. <span data-ttu-id="6e67c-125">Atidarykite duomenų valdymą.</span><span class="sxs-lookup"><span data-stu-id="6e67c-125">Open Data Management.</span></span>
3. <span data-ttu-id="6e67c-126">Pasirinkite **Programėlių CDS saitas**.</span><span class="sxs-lookup"><span data-stu-id="6e67c-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="6e67c-127">Pasirinkite visus vykdomus susiejimus ir tada pasirinkite **Stabdyti**.</span><span class="sxs-lookup"><span data-stu-id="6e67c-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="6e67c-128">Pasirinkite visus susiejimus ir tada pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="6e67c-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6e67c-129">Parinktis **Naikinti** nepasiekiama, jei pasirinktas **„CustomerV3-Account“** šablonas.</span><span class="sxs-lookup"><span data-stu-id="6e67c-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="6e67c-130">Išvalykite šio šablono žymėjimą, kaip nurodyta.</span><span class="sxs-lookup"><span data-stu-id="6e67c-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="6e67c-131">**„CustomerV3-Account“** yra senesnis sukonfigūruotas šablonas ir veikia su potencialių grynųjų pinigų sprendimu.</span><span class="sxs-lookup"><span data-stu-id="6e67c-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="6e67c-132">Jis rodomas visuose šablonuose, nes buvo išleistas visose šalyse.</span><span class="sxs-lookup"><span data-stu-id="6e67c-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="6e67c-133">Pasirinkite **Atsieti aplinką**.</span><span class="sxs-lookup"><span data-stu-id="6e67c-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="6e67c-134">Kad patvirtintumėte operaciją, pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="6e67c-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="6e67c-135">Norėdami susieti naują aplinką, vykdykite [diegimo vadove](https://aka.ms/dualwrite-docs)nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6e67c-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
