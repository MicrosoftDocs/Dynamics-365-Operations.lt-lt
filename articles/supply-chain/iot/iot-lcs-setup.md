---
title: IoT analizės papildinio diegimas LCS
description: Šioje temoje aiškinama, kaip portale „Microsoft Dynamics Lifecycle Services“ (LCS) įdiegti IoT analizės papildinį.
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 04333b3659f090b15cc0d0ee216f14dabc588883
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386541"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="18062-103">IoT analizės papildinio diegimas LCS</span><span class="sxs-lookup"><span data-stu-id="18062-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="18062-104">Šioje temoje aiškinama, kaip portale „Microsoft Dynamics Lifecycle Services“ (LCS) įdiegti IoT analizės papildinį.</span><span class="sxs-lookup"><span data-stu-id="18062-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="18062-105">Kad galėtumėte įdiegti papildinį, turite [sukurti „Azure“ išteklius ](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="18062-105">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="18062-106">LCS aplinkos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="18062-106">Set up the LCS environment</span></span>

1. <span data-ttu-id="18062-107">Atidarykite LCS ir eikite į savo „Microsoft Dynamics 365 Supply Chain Management“ aplinką.</span><span class="sxs-lookup"><span data-stu-id="18062-107">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="18062-108">Slinkite iki dalies **Aplinkos papildiniai**.</span><span class="sxs-lookup"><span data-stu-id="18062-108">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="18062-109">Pasirinkite **Diegti naują papildinį**, kad būtų rodomas aplinkoje įgalintų papildinių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="18062-109">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="18062-110">Dialogo lange **Diegiamo papildinio pasirinkimas** pasirinkite **IoT analizė**.</span><span class="sxs-lookup"><span data-stu-id="18062-110">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="18062-111">Dialogo lange **Papildinio sąranka** pateikite savo „IoT Hub“ ir „Redis“ talpyklos informaciją.</span><span class="sxs-lookup"><span data-stu-id="18062-111">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="18062-112">Reikiamas reikšmes galite rasti raktų saugykloje, kurią sukūrėte dalyje [„Azure“ išteklių kūrimas](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="18062-112">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="18062-113">**Nuomotojo ID** – „Azure“ portale eikite į raktų saugyklą, tada kairiojoje naršymo srityje pasirinkite **Apžvalga** ir nukopijuokite **Katalogo ID** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="18062-113">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="18062-114">Įklijuokite šią reikšmę dialogo lange **Papildinio sąranka**.</span><span class="sxs-lookup"><span data-stu-id="18062-114">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="18062-115">**Su „IoT Event Hub“ suderinamo galinio punkto raktų saugyklos URI** – eikite į raktų saugyklą, tada kairiojoje naršymo srityje pasirinkite **Apžvalga** ir nukopijuokite **DNS pavadinimas** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="18062-115">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="18062-116">Įklijuokite šią reikšmę dialogo lange **Papildinio sąranka**.</span><span class="sxs-lookup"><span data-stu-id="18062-116">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="18062-117">**Su „IoT Event Hub“ suderinamo galinio punkto slaptasis pavadinimas** – eikite į raktų saugyklą, tada kairiojoje naršymo srityje pasirinkite **Slaptieji raktai** ir nukopijuokite slaptojo rakto, kur saugoma „IoT Event Hub“ ryšio eilutė, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="18062-117">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="18062-118">Įklijuokite šią reikšmę dialogo lange **Papildinio sąranka**.</span><span class="sxs-lookup"><span data-stu-id="18062-118">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="18062-119">**„Redis“ talpyklos raktų saugyklos URI** – eikite į raktų saugyklą, tada kairiojoje naršymo srityje pasirinkite **Apžvalga** ir nukopijuokite **DNS pavadinimas** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="18062-119">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="18062-120">Įklijuokite šią reikšmę dialogo lange **Papildinio sąranka**.</span><span class="sxs-lookup"><span data-stu-id="18062-120">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="18062-121">**„Redis“ talpyklos galinio punkto slaptasis pavadinimas** – eikite į raktų saugyklą, tada kairiojoje naršymo srityje pasirinkite **Slaptieji raktai** ir nukopijuokite slaptojo rakto, kur saugoma „Redis“ talpyklos ryšio eilutė, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="18062-121">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="18062-122">Įklijuokite šią reikšmę dialogo lange **Papildinio sąranka**.</span><span class="sxs-lookup"><span data-stu-id="18062-122">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="18062-123">Pažymėkite žymės langelį, kad sutiktumėte su sąlygomis.</span><span class="sxs-lookup"><span data-stu-id="18062-123">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="18062-124">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="18062-124">Select **Install**.</span></span>
8. <span data-ttu-id="18062-125">Atidaromas pranešimo langas, kuriame nurodoma, kad „Papildinys sėkmingai pradėtas diegti“.</span><span class="sxs-lookup"><span data-stu-id="18062-125">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="18062-126">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="18062-126">Select **OK**.</span></span>

<span data-ttu-id="18062-127">LCS sąranka dabar baigta.</span><span class="sxs-lookup"><span data-stu-id="18062-127">LCS setup is now completed.</span></span> <span data-ttu-id="18062-128">Kitas veiksmas – [nustatyti scenarijus](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="18062-128">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="18062-129">Papildinio šalinimas</span><span class="sxs-lookup"><span data-stu-id="18062-129">Uninstall the add-in</span></span>

1. <span data-ttu-id="18062-130">Programoje „Supply Chain Management“ [išjunkite scenarijus](iot-scenario-setup.md#how-to-disable-a-scenario).</span><span class="sxs-lookup"><span data-stu-id="18062-130">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#how-to-disable-a-scenario).</span></span>
2. <span data-ttu-id="18062-131">LCS eikite į „Supply Chain Management” aplinkos informaciją.</span><span class="sxs-lookup"><span data-stu-id="18062-131">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="18062-132">Slinkite iki dalies **Aplinkos papildiniai**.</span><span class="sxs-lookup"><span data-stu-id="18062-132">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="18062-133">Prie IoT analizės papildinio pasirinkite **Šalinti**.</span><span class="sxs-lookup"><span data-stu-id="18062-133">Select **Uninstall** for the IoT Intelligence add-in.</span></span>
