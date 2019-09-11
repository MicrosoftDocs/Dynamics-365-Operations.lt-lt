---
title: Duomenų integravimo trikčių šalinimo vadovas
description: Šioje temoje pateikiama duomenų integravimo tarp „Microsoft Dynamics 365 for Finance and Operations“ ir “Common Data Service“ trikčių šalinimo informacija.
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
ms.openlocfilehash: 5e71729dafd2ad85a01b055363d1c7056b5558b2
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873110"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="4eaff-103">Duomenų integravimo trikčių šalinimo vadovas</span><span class="sxs-lookup"><span data-stu-id="4eaff-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="4eaff-104">Įjunkite priedo sekimo žurnalus programoje „Common Data Service“ ir patikrinkite dvigubo rašymo priedo klaidų išsamią informaciją</span><span class="sxs-lookup"><span data-stu-id="4eaff-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="4eaff-105">Jei atlikdami dvigubo rašymo sinchronizavimą susiduriate su problema arba klaida, atlikite šiuos veiksmus, kad patikrintumėte klaidas sekimo žurnale.</span><span class="sxs-lookup"><span data-stu-id="4eaff-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="4eaff-106">Prieš tikrindami klaidas, turite įjungti priedo sekimo žurnalus.</span><span class="sxs-lookup"><span data-stu-id="4eaff-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="4eaff-107">Instrukcijas rasite vadovo [Mokymo priemonė: įrašykite ir užregistruokite priedą](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) skyriuje „Sekimo žurnalų peržiūrėjimas“.</span><span class="sxs-lookup"><span data-stu-id="4eaff-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="4eaff-108">Dabar galite tikrinti klaidas.</span><span class="sxs-lookup"><span data-stu-id="4eaff-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="4eaff-109">Prisijunkite prie „Microsoft Dynamics 365 for Sales“.</span><span class="sxs-lookup"><span data-stu-id="4eaff-109">Sign in to Microsoft Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="4eaff-110">Pasirinkite mygtuką **Parametrai** (krumpliaračio simbolis) ir pasirinkite **Išplėstiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="4eaff-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="4eaff-111">Meniu **Parametrai** pasirinkite **Tinkinimas\> Priedo sekimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="4eaff-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="4eaff-112">Pasirinkite **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** kaip tipo pavadinimą, kad būtų rodoma išsami klaidos informacija.</span><span class="sxs-lookup"><span data-stu-id="4eaff-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="4eaff-113">Patikrinkite dvigubo rašymo sinchronizavimo klaidas programoje „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="4eaff-113">Inspect dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="4eaff-114">Atlikite šiuos veiksmus, kad galėtumėte tikrinti klaidas per testavimą.</span><span class="sxs-lookup"><span data-stu-id="4eaff-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="4eaff-115">Prisijunkite prie „Microsoft Dynamics“ portale „Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="4eaff-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="4eaff-116">Atidarykite LCS projektą, kad atliktumėte dvigubo rašymo testavimą.</span><span class="sxs-lookup"><span data-stu-id="4eaff-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="4eaff-117">Pasirinkite **Aplinkos diegimo debesyje įrankis**.</span><span class="sxs-lookup"><span data-stu-id="4eaff-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="4eaff-118">Sukurkite nuotolinį darbalaukį, skirtą „Dynamics 365 for Finance and Operations“ virtualiajai mašinai (VM), pasinaudoję LCS rodoma vietine paskyra.</span><span class="sxs-lookup"><span data-stu-id="4eaff-118">Make a Remote desktop connection to the Dynamics 365 for Finance and Operations virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="4eaff-119">Atidarykite įvykių peržiūros programą.</span><span class="sxs-lookup"><span data-stu-id="4eaff-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="4eaff-120">Eikite į **Programų ir paslaugų žurnalai\> „Microsoft“\> „Dynamics“\> „AX-DualWriteSync“\> Veikia**</span><span class="sxs-lookup"><span data-stu-id="4eaff-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="4eaff-121">Rodomos klaidos ir išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="4eaff-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-finance-and-operations-and-link-another-environment"></a><span data-ttu-id="4eaff-122">Atsiekite vieną „Common Data Service“ aplinką nuo „Finance and Operations“ ir susiekite kitą aplinką.</span><span class="sxs-lookup"><span data-stu-id="4eaff-122">Unlink one Common Data Service environment from Finance and Operations and link another environment</span></span>

<span data-ttu-id="4eaff-123">Norėdami atnaujinti saitus atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4eaff-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="4eaff-124">Eikite į „Finance and Operations“ aplinką.</span><span class="sxs-lookup"><span data-stu-id="4eaff-124">Go to the Finance and Operations environment.</span></span>
2. <span data-ttu-id="4eaff-125">Atidarykite duomenų valdymą.</span><span class="sxs-lookup"><span data-stu-id="4eaff-125">Open Data Management.</span></span>
3. <span data-ttu-id="4eaff-126">Pasirinkite **Programėlių CDS saitas**.</span><span class="sxs-lookup"><span data-stu-id="4eaff-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="4eaff-127">Pasirinkite visus vykdomus susiejimus ir tada pasirinkite **Stabdyti**.</span><span class="sxs-lookup"><span data-stu-id="4eaff-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="4eaff-128">Pasirinkite visus susiejimus ir tada pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="4eaff-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4eaff-129">Parinktis **Naikinti** nepasiekiama, jei pasirinktas **„CustomerV3-Account“** šablonas.</span><span class="sxs-lookup"><span data-stu-id="4eaff-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="4eaff-130">Išvalykite šio šablono žymėjimą, kaip nurodyta.</span><span class="sxs-lookup"><span data-stu-id="4eaff-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="4eaff-131">**„CustomerV3-Account“** yra senesnis sukonfigūruotas šablonas ir veikia su potencialių grynųjų pinigų sprendimu.</span><span class="sxs-lookup"><span data-stu-id="4eaff-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="4eaff-132">Jis rodomas visuose šablonuose, nes buvo išleistas visose šalyse.</span><span class="sxs-lookup"><span data-stu-id="4eaff-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="4eaff-133">Pasirinkite **Atsieti aplinką**.</span><span class="sxs-lookup"><span data-stu-id="4eaff-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="4eaff-134">Kad patvirtintumėte operaciją, pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="4eaff-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="4eaff-135">Norėdami susieti naują aplinką, vykdykite [diegimo vadove](https://aka.ms/dualwrite-docs)nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4eaff-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
