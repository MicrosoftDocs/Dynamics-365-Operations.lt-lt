---
title: Duomenų integravimo trikčių šalinimo vadovas
description: Šioje temoje pateikiama trikčių šalinimo informacija apie duomenų integravimą tarp „Microsoft Dynamics 365 for Finance and Operations“ ir „Common Data Service“.
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
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797280"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="8cef5-103">Duomenų integravimo trikčių šalinimo vadovas</span><span class="sxs-lookup"><span data-stu-id="8cef5-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a><span data-ttu-id="8cef5-104">Įjunkite priedo sekimą programoje „Common Data Service“ ir patikrinkite dvigubo rašymo priedo klaidos informaciją.</span><span class="sxs-lookup"><span data-stu-id="8cef5-104">Enable Plugin Trace in Common Data Service and check the dual-write Plugin error details</span></span>

<span data-ttu-id="8cef5-105">Jei susiduriate su problema ar klaida atlikdami dvigubo rašymo sinchronizavimą, galite patikrinti klaidas sekimo žurnale:</span><span class="sxs-lookup"><span data-stu-id="8cef5-105">If you are facing an issue or error with dual-write synchronization, you can inspect the errors in the trace log:</span></span>

1. <span data-ttu-id="8cef5-106">Prieš galėdami patikrinti klaidas, turite įjungti priedo sekimą naudodamiesi instrukcijomis, pateiktomis dalyje [Register plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs), kad įjungtumėte priedo sekimą.</span><span class="sxs-lookup"><span data-stu-id="8cef5-106">Before you can inspect the errors, you must enable Plugin trace using the instructions in [Register plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) to enable Plugin trace.</span></span> <span data-ttu-id="8cef5-107">Dabar galite patikrinti klaidas.</span><span class="sxs-lookup"><span data-stu-id="8cef5-107">Now you can inspect the errors.</span></span>
2. <span data-ttu-id="8cef5-108">Prisijungti prie „Dynamics 365 for Sales‟</span><span class="sxs-lookup"><span data-stu-id="8cef5-108">Login to Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="8cef5-109">Spustelėkite nustatymų piktogramą (pavara) ir pasirinkite **„Išplėstiniai parametrai“**.</span><span class="sxs-lookup"><span data-stu-id="8cef5-109">Click on the Settings icon (a gear), and select **Advanced Settings**.</span></span>
4. <span data-ttu-id="8cef5-110">Meniu **„Parametrai“** pasirinkite **„Tinkinimas“ > „Priedo sekimo žurnalas“**</span><span class="sxs-lookup"><span data-stu-id="8cef5-110">In the **Settings** menu, choose **Customization > Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="8cef5-111">Spustelėkite tipo pavadinimą **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**, kad būtų rodoma išsami klaidos informacija.</span><span class="sxs-lookup"><span data-stu-id="8cef5-111">Click the type name **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** to display the error details.</span></span>

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="8cef5-112">Patikrinkite „Finance and Operations“ dvigubo rašymo sinchronizavimo klaidas</span><span class="sxs-lookup"><span data-stu-id="8cef5-112">Check dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="8cef5-113">Atlikdami toliau nurodytus veiksmus galite patikrinti klaidas per testavimą:</span><span class="sxs-lookup"><span data-stu-id="8cef5-113">You can check the errors during testing by following these steps:</span></span>

+ <span data-ttu-id="8cef5-114">Prisijunkite prie „LifeCycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="8cef5-114">Login to LifeCycle Services (LCS).</span></span>
+ <span data-ttu-id="8cef5-115">Atidarykite LCS projektą, kurį pasirinkote dvigubo rašymo testavimui atlikti.</span><span class="sxs-lookup"><span data-stu-id="8cef5-115">Open the LCS project that you chose to perform dual-write testing.</span></span>
+ <span data-ttu-id="8cef5-116">Eikite į debesies nuomojamas aplinkas.</span><span class="sxs-lookup"><span data-stu-id="8cef5-116">Go to Cloud Hosted Environments.</span></span>
+ <span data-ttu-id="8cef5-117">Prisijunkite prie „Finance and Operations“ VM nuotolinio darbalaukio naudodami vietinį abonementą, kuris rodomas LCS.</span><span class="sxs-lookup"><span data-stu-id="8cef5-117">Remote desktop to Finance and Operations VM using local account that is displayed in LCS.</span></span>
+ <span data-ttu-id="8cef5-118">Atidarykite įvykio peržiūrą.</span><span class="sxs-lookup"><span data-stu-id="8cef5-118">Open the event viewer.</span></span> 
+ <span data-ttu-id="8cef5-119">Pereikite į **„Programų ir paslaugų žurnalai“ > „Microsoft“ > „Dynamics“ > „AX-DualWriteSync“ > „Operacinis“**.</span><span class="sxs-lookup"><span data-stu-id="8cef5-119">Navigate to **Applications and Services logs > Microsoft > Dynamics > AX-DualWriteSync > Operational**.</span></span> <span data-ttu-id="8cef5-120">Rodomos klaidos ir išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="8cef5-120">The errors and details are displayed.</span></span>

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a><span data-ttu-id="8cef5-121">Kaip atsieti ir susieti kitą „Common Data Service“ aplinką iš „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="8cef5-121">How to unlink and link another Common Data Service environment from Finance and Operations</span></span>

<span data-ttu-id="8cef5-122">Saitus galite naujinti atlikdami šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="8cef5-122">You can update links by following these steps:</span></span>

+ <span data-ttu-id="8cef5-123">Pereikite į „Finance and Operations“ aplinką.</span><span class="sxs-lookup"><span data-stu-id="8cef5-123">Navigate to the Finance and Operations environment.</span></span>
+ <span data-ttu-id="8cef5-124">Atidarykite duomenų valdymą.</span><span class="sxs-lookup"><span data-stu-id="8cef5-124">Open Data Management.</span></span>
+ <span data-ttu-id="8cef5-125">Paspauskite **„Susieti su CDS, skirtu programoms**.</span><span class="sxs-lookup"><span data-stu-id="8cef5-125">Click on **Link to CDS for apps**.</span></span>
+ <span data-ttu-id="8cef5-126">Pasirinkite visus veikiančius susiejimus ir spustelėkite **„Stabdyti“**.</span><span class="sxs-lookup"><span data-stu-id="8cef5-126">Select all the running mappings and click **Stop**.</span></span> 
+ <span data-ttu-id="8cef5-127">Pasirinkite visus susiejimus ir spustelėkite **„Naikinti“**.</span><span class="sxs-lookup"><span data-stu-id="8cef5-127">Select all the mappings and click **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8cef5-128">Parinktis **„Naikinti“** nebus rodoma, jei pasirinktas **„CustomerV3-Account“** šablonas.</span><span class="sxs-lookup"><span data-stu-id="8cef5-128">The **Delete** option will not appear if **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="8cef5-129">Jei reikia, atžymėkite.</span><span class="sxs-lookup"><span data-stu-id="8cef5-129">Unselect it if needed.</span></span> <span data-ttu-id="8cef5-130">**„CustomerV3-Account“** yra senesnis sukonfigūruotas šablonas ir veikia su potencialių grynųjų pinigų sprendimu.</span><span class="sxs-lookup"><span data-stu-id="8cef5-130">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="8cef5-131">Kadangi jis yra išleistasvisame pasaulyje, jis rodomas po visais šablonais.</span><span class="sxs-lookup"><span data-stu-id="8cef5-131">Because it is globally released, it shows up under all templates.</span></span>

+ <span data-ttu-id="8cef5-132">Spustelėkite **„Atsieti aplinką“**.</span><span class="sxs-lookup"><span data-stu-id="8cef5-132">Click **Unlink environment**.</span></span>
+ <span data-ttu-id="8cef5-133">Spustelėkite **Yes**, kad patvirtintumėte.</span><span class="sxs-lookup"><span data-stu-id="8cef5-133">Click **Yes** for confirmation.</span></span>
+ <span data-ttu-id="8cef5-134">Norėdami susieti naują aplinką, vykdykite [diegimo vadove](https://aka.ms/dualwrite-docs)nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8cef5-134">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>

