---
title: IoT analizės stebėjimas ir valdymas
description: Šioje temoje aiškinama, kaip stebėti ir valdyti IoT analizę.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7082f9e7640e8ef1b2873a954327b61a440e8ad0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000011"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="35233-103">IoT analizės stebėjimas ir valdymas</span><span class="sxs-lookup"><span data-stu-id="35233-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="35233-104">Šioje temoje aiškinama, kaip stebėti ir valdyti IoT analizę.</span><span class="sxs-lookup"><span data-stu-id="35233-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="35233-105">Scenarijų stebėjimas programoje „Microsoft Dynamics 365 Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="35233-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="35233-106">IoT analizės apdorojimą galite stebėti keliose vietose.</span><span class="sxs-lookup"><span data-stu-id="35233-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="35233-107">**Moduliai \> Gamybos kontrolė \> Užklausos ir ataskaitos \> IoT analizė \> Pranešimai** – peržiūrėkite neišspręstų pranešimų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="35233-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="35233-108">**Moduliai \> Gamybos kontrolė \> Užklausos ir ataskaitos \> IoT analizė \> Uždaryti pranešimai** – peržiūrėkite išspręstų arba atmestų pranešimų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="35233-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="35233-109">**Moduliai \> Gamybos kontrolė \> Užklausos ir ataskaitos \> IoT analizė \> Metrikos raktai** – peržiūrėkite laiko sekų diagramų **Išteklių būsena** metrikos raktus.</span><span class="sxs-lookup"><span data-stu-id="35233-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="35233-110">**Moduliai \> Gamybos kontrolė \> Gamybos vykdymas \> Išteklių būsena** – sekite specifinę metriką naudodami dialogo langą **Konfigūruoti**.</span><span class="sxs-lookup"><span data-stu-id="35233-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="35233-111">Jei scenarijus aptinka išimtį, pranešime pateikiama išsami išimties informacija.</span><span class="sxs-lookup"><span data-stu-id="35233-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="35233-112">**Darbo sritys \> Gamybos vietos valdymas \> Pranešimai** – peržiūrėite neišspręstų pranešimų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="35233-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="35233-113">Vykdomo IoT analizės scenarijaus modifikavimas</span><span class="sxs-lookup"><span data-stu-id="35233-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="35233-114">Kai scenarijus vykdomas, galite atlikti toliau nurodytus keitimus.</span><span class="sxs-lookup"><span data-stu-id="35233-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="35233-115">Įtraukti naujų jutiklio schemos apibrėžimų.</span><span class="sxs-lookup"><span data-stu-id="35233-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="35233-116">Pasirinkti naujas signalų duomenų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="35233-116">Select new signal data values.</span></span>
+ <span data-ttu-id="35233-117">Atšaukti esamų signalo duomenų reikšmių pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="35233-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="35233-118">Įtraukti ir susieti naujas signalo duomenų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="35233-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="35233-119">Atnaujinti ribines reikšmes.</span><span class="sxs-lookup"><span data-stu-id="35233-119">Update threshold values.</span></span>

<span data-ttu-id="35233-120">Kai scenarijus vykdomas, toliau nurodyti keitimai yra draudžiami.</span><span class="sxs-lookup"><span data-stu-id="35233-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="35233-121">Schemos apibrėžimų, kuriuos einamuoju metu naudoja įgalintas scenarijus, naikinimas arba modifikavimas.</span><span class="sxs-lookup"><span data-stu-id="35233-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="35233-122">Įgalinto scenarijaus schemos kelių keitimas.</span><span class="sxs-lookup"><span data-stu-id="35233-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="35233-123">Modeliavimo parinktys</span><span class="sxs-lookup"><span data-stu-id="35233-123">Simulation options</span></span>

<span data-ttu-id="35233-124">Galite modeliuoti gamyklos įrenginių signalus.</span><span class="sxs-lookup"><span data-stu-id="35233-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="35233-125">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="35233-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="35233-126">IoT kūrimo rinkinio AZ3166 prijungimas prie „Azure IoT Hub“</span><span class="sxs-lookup"><span data-stu-id="35233-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="35233-127">„Raspberry Pi“ internetinio simuliatoriaus prijungimas prie „Azure IoT Hub“ (Node.js)</span><span class="sxs-lookup"><span data-stu-id="35233-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="35233-128">Įrenginių modeliavimo sprendimų spartintuvo apžvalga</span><span class="sxs-lookup"><span data-stu-id="35233-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)
