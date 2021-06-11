---
title: Dvigubo rašymo sąranka iš „Lifecycle Services“
description: Šioje temoje paaiškinama, kaip nustatyti dvigubo rašymo ryšį iš „Microsoft Dynamics Lifecycle Services” (LCS).
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103574"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="f3214-103">Dvigubo rašymo sąranka iš „Lifecycle Services“</span><span class="sxs-lookup"><span data-stu-id="f3214-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f3214-104">Šioje temoje paaiškinama, kaip įgalinti dvigubą rašymą iš „Microsoft Dynamics Lifecycle Services” (LCS).</span><span class="sxs-lookup"><span data-stu-id="f3214-104">This topic explains how to enable dual-write from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f3214-105">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="f3214-105">Prerequisites</span></span>

<span data-ttu-id="f3214-106">Turite užbaigti „Power Platform” integravimą, kaip aprašyta šiose temose:</span><span class="sxs-lookup"><span data-stu-id="f3214-106">You must complete the Power Platform integration as described in the following topics:</span></span>

+ [<span data-ttu-id="f3214-107">„Power Platform” Integravimas – Įgalinti aplinkos diegimo metu</span><span class="sxs-lookup"><span data-stu-id="f3214-107">Power Platform Integration - Enable during environment deployment</span></span>](../../power-platform/overview.md#enable-during-environment-deployment)
+ [<span data-ttu-id="f3214-108">„Power Platform” integravimas – Nustatyti po aplinkos diegimo</span><span class="sxs-lookup"><span data-stu-id="f3214-108">Power Platform integration - Set up after environment deployment</span></span>](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a><span data-ttu-id="f3214-109">Dvigubo rašymo nustatymas naujoms „Dataverse” aplinkoms</span><span class="sxs-lookup"><span data-stu-id="f3214-109">Set up dual-write for new Dataverse environments</span></span>

<span data-ttu-id="f3214-110">Norėdami nustatyti dvigubą rašymą iš LCS **Aplinkos informacijos** puslapio, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="f3214-110">Follow these steps to set up dual-write from LCS **Environment Details** page:</span></span>

1. <span data-ttu-id="f3214-111">Puslapyje **Aplinkos informacija** išplėskite skyrių **„Power Platform” Integravimas**.</span><span class="sxs-lookup"><span data-stu-id="f3214-111">On the **Environment Details** page, expand the **Power Platform Integration** section.</span></span>

2. <span data-ttu-id="f3214-112">Pasirinkite **Dvigubo rašymo programos** mygtuką.</span><span class="sxs-lookup"><span data-stu-id="f3214-112">Select the **Dual-write application** button.</span></span>

    ![„Power Platform“ integravimas](media/powerplat_integration_step2.png)

3. <span data-ttu-id="f3214-114">Peržiūrėkite sąlygas ir nuostatas, o tada pasirinkite **Konfigūruoti**.</span><span class="sxs-lookup"><span data-stu-id="f3214-114">Review the terms and conditions, and then select **Configure**.</span></span>

4. <span data-ttu-id="f3214-115">Norėdami tęsti pasirinkite **GERAI**.</span><span class="sxs-lookup"><span data-stu-id="f3214-115">Select **OK** to continue.</span></span>

5. <span data-ttu-id="f3214-116">Eigą galite stebėti periodiškai atnaujindami aplinkos informacijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="f3214-116">You can monitor the progress by periodically refreshing the environment details page.</span></span> <span data-ttu-id="f3214-117">Įprastai nustatymas trunka ne daugiau kaip 30 minučių.</span><span class="sxs-lookup"><span data-stu-id="f3214-117">Setup typically takes 30 minutes or less.</span></span>  

6. <span data-ttu-id="f3214-118">Užbaigę nustatymą, gausite pranešimą, ar procesas buvo sėkmingas.</span><span class="sxs-lookup"><span data-stu-id="f3214-118">When the setup is complete, a message will inform you if the process was successful or if there was a failure.</span></span> <span data-ttu-id="f3214-119">Jei nustatymas nepavyko, rodomas susijęs klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="f3214-119">If the setup failed, then a related error message is displayed.</span></span> <span data-ttu-id="f3214-120">Prieš pereidami prie kito veiksmo, turite ištaisyti klaidas, jei jų yra.</span><span class="sxs-lookup"><span data-stu-id="f3214-120">You must fix any errors before moving to the next step.</span></span>

7. <span data-ttu-id="f3214-121">Pasirinkite **Saitas į „Power Platform” aplinką**, kad sukurtumėte saitą tarp „Dataverse” ir dabartinės aplinkos duomenų bazių.</span><span class="sxs-lookup"><span data-stu-id="f3214-121">Select **Link to Power Platform environment** to create a link between Dataverse and the current environment's databases.</span></span> <span data-ttu-id="f3214-122">Įprastai tai trunka mažiau nei 5 minutes.</span><span class="sxs-lookup"><span data-stu-id="f3214-122">This typically takes less than 5 minutes.</span></span>

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Saitas į Power Platform aplinką":::

8. <span data-ttu-id="f3214-124">Užbaigus susiejimą, rodomas hipersaitas.</span><span class="sxs-lookup"><span data-stu-id="f3214-124">When the linking is complete, a hyperlink is displayed.</span></span> <span data-ttu-id="f3214-125">Naudokite saitą, kad prisiregistruotumėte prie dvigubo rašymo administravimo srities „Finance and Operations” aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="f3214-125">Use the link to sign in to the dual-write administration area in the Finance and Operations environment.</span></span> <span data-ttu-id="f3214-126">Iš ten galite nustatyti objektų susiejimus.</span><span class="sxs-lookup"><span data-stu-id="f3214-126">From there, you can set up entity mappings.</span></span>

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a><span data-ttu-id="f3214-127">Dvigubo rašymo nustatymas esamai „Dataverse” aplinkai</span><span class="sxs-lookup"><span data-stu-id="f3214-127">Set up dual-write for an existing Dataverse environment</span></span>

<span data-ttu-id="f3214-128">Norėdami nustatyti dvigubą rašymą esamai „Dataverse” aplinkai, turite sukurti „Microsoft” [palaikymo kvitą](../../lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="f3214-128">To set up dual-write for an existing Dataverse environment, you must create a Microsoft [support ticket](../../lifecycle-services/lcs-support.md).</span></span> <span data-ttu-id="f3214-129">Į kvitą turi būti įtraukta:</span><span class="sxs-lookup"><span data-stu-id="f3214-129">The ticket must include:</span></span>

+ <span data-ttu-id="f3214-130">Jūsų „Finance and Operations” aplinkos ID.</span><span class="sxs-lookup"><span data-stu-id="f3214-130">Your Finance and Operations environment ID.</span></span>
+ <span data-ttu-id="f3214-131">Jūsų aplinkos pavadinimas iš „Lifecycle Services”.</span><span class="sxs-lookup"><span data-stu-id="f3214-131">Your environment name from Lifecycle Services.</span></span>
+ <span data-ttu-id="f3214-132">„Dataverse” organizacijos ID arba „Power Platform” aplinkos ID iš „Power Platform” administravimo centro.</span><span class="sxs-lookup"><span data-stu-id="f3214-132">The Dataverse organization ID or Power Platform Environment ID from Power Platform Admin Center.</span></span> <span data-ttu-id="f3214-133">Savo kvite pateikite užklausą, kad ID būtų egzempliorius, naudotas „Power Platform” integravimui.</span><span class="sxs-lookup"><span data-stu-id="f3214-133">In your ticket, request that the ID be the instance used for Power Platform integration.</span></span>

> [!NOTE]
> <span data-ttu-id="f3214-134">Negalite atsieti aplinkos naudodami LCS.</span><span class="sxs-lookup"><span data-stu-id="f3214-134">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="f3214-135">Norėdami atsieti aplinką, aplinkoje Finance and Operations atidarykite darbo sritį **Duomenų integravimas** ir pasirinkite **Atsieti**.</span><span class="sxs-lookup"><span data-stu-id="f3214-135">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
