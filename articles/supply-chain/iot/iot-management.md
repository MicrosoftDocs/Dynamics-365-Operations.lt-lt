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
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 15021281b9ec33cd0552bca16e3054d0d3cdd589
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433844"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="e5fdd-103">IoT analizės stebėjimas ir valdymas</span><span class="sxs-lookup"><span data-stu-id="e5fdd-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e5fdd-104">Šioje temoje aiškinama, kaip stebėti ir valdyti IoT analizę.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="e5fdd-105">Scenarijų stebėjimas programoje „Microsoft Dynamics 365 Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="e5fdd-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="e5fdd-106">IoT analizės apdorojimą galite stebėti keliose vietose.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="e5fdd-107">**Moduliai \> Gamybos kontrolė \> Užklausos ir ataskaitos \> IoT analizė \> Pranešimai** – peržiūrėkite neišspręstų pranešimų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="e5fdd-108">**Moduliai \> Gamybos kontrolė \> Užklausos ir ataskaitos \> IoT analizė \> Uždaryti pranešimai** – peržiūrėkite išspręstų arba atmestų pranešimų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="e5fdd-109">**Moduliai \> Gamybos kontrolė \> Užklausos ir ataskaitos \> IoT analizė \> Metrikos raktai** – peržiūrėkite laiko sekų diagramų **Išteklių būsena** metrikos raktus.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="e5fdd-110">**Moduliai \> Gamybos kontrolė \> Gamybos vykdymas \> Išteklių būsena** – sekite specifinę metriką naudodami dialogo langą **Konfigūruoti**.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="e5fdd-111">Jei scenarijus aptinka išimtį, pranešime pateikiama išsami išimties informacija.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="e5fdd-112">**Darbo sritys \> Gamybos vietos valdymas \> Pranešimai** – peržiūrėite neišspręstų pranešimų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="e5fdd-113">Vykdomo IoT analizės scenarijaus modifikavimas</span><span class="sxs-lookup"><span data-stu-id="e5fdd-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="e5fdd-114">Kai scenarijus vykdomas, galite atlikti toliau nurodytus keitimus.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="e5fdd-115">Įtraukti naujų jutiklio schemos apibrėžimų.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="e5fdd-116">Pasirinkti naujas signalų duomenų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-116">Select new signal data values.</span></span>
+ <span data-ttu-id="e5fdd-117">Atšaukti esamų signalo duomenų reikšmių pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="e5fdd-118">Įtraukti ir susieti naujas signalo duomenų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="e5fdd-119">Atnaujinti ribines reikšmes.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-119">Update threshold values.</span></span>

<span data-ttu-id="e5fdd-120">Kai scenarijus vykdomas, toliau nurodyti keitimai yra draudžiami.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="e5fdd-121">Schemos apibrėžimų, kuriuos einamuoju metu naudoja įgalintas scenarijus, naikinimas arba modifikavimas.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="e5fdd-122">Įgalinto scenarijaus schemos kelių keitimas.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="e5fdd-123">Modeliavimo parinktys</span><span class="sxs-lookup"><span data-stu-id="e5fdd-123">Simulation options</span></span>

<span data-ttu-id="e5fdd-124">Galite modeliuoti gamyklos įrenginių signalus.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="e5fdd-125">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="e5fdd-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="e5fdd-126">IoT kūrimo rinkinio AZ3166 prijungimas prie „Azure IoT Hub“</span><span class="sxs-lookup"><span data-stu-id="e5fdd-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="e5fdd-127">„Raspberry Pi“ internetinio simuliatoriaus prijungimas prie „Azure IoT Hub“ (Node.js)</span><span class="sxs-lookup"><span data-stu-id="e5fdd-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="e5fdd-128">Įrenginių modeliavimo sprendimų spartintuvo apžvalga</span><span class="sxs-lookup"><span data-stu-id="e5fdd-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)
