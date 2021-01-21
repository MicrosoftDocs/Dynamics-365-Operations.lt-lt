---
title: IoT analizės papildinio diegimas LCS
description: Šioje temoje aiškinama, kaip portale „Microsoft Dynamics Lifecycle Services“ (LCS) įdiegti IoT analizės papildinį.
author: robinarh
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ad8b33633646f27bc368dc4bbedc1eb64c150a9f
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4014940"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="d5d11-103">IoT analizės papildinio diegimas LCS</span><span class="sxs-lookup"><span data-stu-id="d5d11-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d5d11-104">Šioje temoje aiškinama, kaip portale „Microsoft Dynamics Lifecycle Services“ (LCS) įdiegti IoT analizės papildinį.</span><span class="sxs-lookup"><span data-stu-id="d5d11-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="d5d11-105">Atkreipkite dėmesį, kad priedai negali būti įdiegti demo ar bandyminėje aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="d5d11-105">Note that add-ins cannot be installed on a demo/trial environment.</span></span> <span data-ttu-id="d5d11-106">Kad galėtumėte įdiegti papildinį, turite [sukurti „Azure“ išteklius ](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="d5d11-106">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="d5d11-107">LCS aplinkos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="d5d11-107">Set up the LCS environment</span></span>

1. <span data-ttu-id="d5d11-108">Atidarykite LCS ir eikite į savo „Microsoft Dynamics 365 Supply Chain Management“ aplinką.</span><span class="sxs-lookup"><span data-stu-id="d5d11-108">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="d5d11-109">Slinkite iki dalies **Aplinkos papildiniai**.</span><span class="sxs-lookup"><span data-stu-id="d5d11-109">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="d5d11-110">Pasirinkite **Diegti naują papildinį** , kad būtų rodomas aplinkoje įgalintų papildinių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="d5d11-110">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="d5d11-111">Dialogo lange **Diegiamo papildinio pasirinkimas** pasirinkite **IoT analizė**.</span><span class="sxs-lookup"><span data-stu-id="d5d11-111">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="d5d11-112">Dialogo lange **Papildinio sąranka** pateikite savo „IoT Hub“ ir „Redis“ talpyklos informaciją.</span><span class="sxs-lookup"><span data-stu-id="d5d11-112">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="d5d11-113">Reikiamas reikšmes galite rasti raktų saugykloje, kurią sukūrėte dalyje [„Azure“ išteklių kūrimas](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="d5d11-113">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="d5d11-114">**Nuomotojo ID** – „Azure“ portale eikite į raktų saugyklą, tada kairiojoje naršymo srityje pasirinkite **Apžvalga** ir nukopijuokite **Katalogo ID** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d5d11-114">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview** , and copy the **Directory ID** value.</span></span> <span data-ttu-id="d5d11-115">Įklijuokite šią reikšmę dialogo lange **Papildinio sąranka**.</span><span class="sxs-lookup"><span data-stu-id="d5d11-115">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="d5d11-116">**Su „IoT Event Hub“ suderinamo galinio punkto raktų saugyklos URI** – eikite į raktų saugyklą, tada kairiojoje naršymo srityje pasirinkite **Apžvalga** ir nukopijuokite **DNS pavadinimas** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d5d11-116">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview** , and copy the **DNS name** value.</span></span> <span data-ttu-id="d5d11-117">Įklijuokite šią reikšmę dialogo lange **Papildinio sąranka**.</span><span class="sxs-lookup"><span data-stu-id="d5d11-117">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="d5d11-118">**Su „IoT Event Hub“ suderinamo galinio punkto slaptasis pavadinimas** – eikite į raktų saugyklą, tada kairiojoje naršymo srityje pasirinkite **Slaptieji raktai** ir nukopijuokite slaptojo rakto, kur saugoma „IoT Event Hub“ ryšio eilutė, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="d5d11-118">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets** , and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="d5d11-119">Įklijuokite šią reikšmę dialogo lange **Papildinio sąranka**.</span><span class="sxs-lookup"><span data-stu-id="d5d11-119">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="d5d11-120">**„Redis“ talpyklos raktų saugyklos URI** – eikite į raktų saugyklą, tada kairiojoje naršymo srityje pasirinkite **Apžvalga** ir nukopijuokite **DNS pavadinimas** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d5d11-120">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview** , and copy the **DNS name** value.</span></span> <span data-ttu-id="d5d11-121">Įklijuokite šią reikšmę dialogo lange **Papildinio sąranka**.</span><span class="sxs-lookup"><span data-stu-id="d5d11-121">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="d5d11-122">**„Redis“ talpyklos galinio punkto slaptasis pavadinimas** – eikite į raktų saugyklą, tada kairiojoje naršymo srityje pasirinkite **Slaptieji raktai** ir nukopijuokite slaptojo rakto, kur saugoma „Redis“ talpyklos ryšio eilutė, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="d5d11-122">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets** , and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="d5d11-123">Įklijuokite šią reikšmę dialogo lange **Papildinio sąranka**.</span><span class="sxs-lookup"><span data-stu-id="d5d11-123">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="d5d11-124">Pažymėkite žymės langelį, kad sutiktumėte su sąlygomis.</span><span class="sxs-lookup"><span data-stu-id="d5d11-124">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="d5d11-125">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="d5d11-125">Select **Install**.</span></span>
8. <span data-ttu-id="d5d11-126">Atidaromas pranešimo langas, kuriame nurodoma, kad „Papildinys sėkmingai pradėtas diegti“.</span><span class="sxs-lookup"><span data-stu-id="d5d11-126">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="d5d11-127">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d5d11-127">Select **OK**.</span></span>

<span data-ttu-id="d5d11-128">LCS sąranka dabar baigta.</span><span class="sxs-lookup"><span data-stu-id="d5d11-128">LCS setup is now completed.</span></span> <span data-ttu-id="d5d11-129">Kitas veiksmas – [nustatyti scenarijus](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="d5d11-129">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="d5d11-130">Papildinio šalinimas</span><span class="sxs-lookup"><span data-stu-id="d5d11-130">Uninstall the add-in</span></span>

1. <span data-ttu-id="d5d11-131">Programoje „Supply Chain Management“ [išjunkite scenarijus](iot-scenario-setup.md#disable-a-scenario).</span><span class="sxs-lookup"><span data-stu-id="d5d11-131">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#disable-a-scenario).</span></span>
2. <span data-ttu-id="d5d11-132">LCS eikite į „Supply Chain Management” aplinkos informaciją.</span><span class="sxs-lookup"><span data-stu-id="d5d11-132">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="d5d11-133">Slinkite iki dalies **Aplinkos papildiniai**.</span><span class="sxs-lookup"><span data-stu-id="d5d11-133">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="d5d11-134">Prie IoT analizės papildinio pasirinkite **Šalinti**.</span><span class="sxs-lookup"><span data-stu-id="d5d11-134">Select **Uninstall** for the IoT Intelligence add-in.</span></span>