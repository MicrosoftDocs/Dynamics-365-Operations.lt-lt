---
title: Konfigūruoti ir vykdyti išrašų registravimo užduotį
description: Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančią paketinę užduotį, norint registruoti pasirinktos parduotuvės arba parduotuvių grupės išrašus.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a24014f7e1b925e0fdb20b91bcc9594feb8f4c5c
ms.sourcegitcommit: fc40279d0e56f8a43c601bca6265fdde4c8c4c7e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/29/2019
ms.locfileid: "1792253"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="6cf7e-103">Konfigūruoti ir vykdyti išrašų registravimo užduotį</span><span class="sxs-lookup"><span data-stu-id="6cf7e-103">Configure and run job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="6cf7e-104">Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančią paketinę užduotį, norint registruoti pasirinktos parduotuvės arba parduotuvių grupės išrašus.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="6cf7e-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="6cf7e-106">Eikite į Visos darbo sritys > ..</span><span class="sxs-lookup"><span data-stu-id="6cf7e-106">Go to All workspaces > ..</span></span> <span data-ttu-id="6cf7e-107">> Mažmeninės prekybos parduotuvės finansai.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-107">> Retail store financials.</span></span>
2. <span data-ttu-id="6cf7e-108">Registruoti išrašus pakete</span><span class="sxs-lookup"><span data-stu-id="6cf7e-108">Click Post statements in batch.</span></span>
    * <span data-ttu-id="6cf7e-109">Pasirinkite organizacijos hierarchiją ir organizacijos mazgų medį, pasirinkite atskirą parduotuvę arba mazgą.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="6cf7e-110">Pasirinkite mazgą, jei norite kurti parduotuvių grupės paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="6cf7e-111">Spustelėkite rodyklę ir įtraukite savo pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="6cf7e-112">Spustelėkite skirtuką Vykdyti fone. ![Vykdyti fone](../dev-itpro/media/runbackground.png "Vykdyti fone")</span><span class="sxs-lookup"><span data-stu-id="6cf7e-112">Click the Run in the background tab. ![Run in the background](../dev-itpro/media/runbackground.png "Run in the background")</span></span> 
4. <span data-ttu-id="6cf7e-113">Pažymėkite arba atžymėkite žymės langelį Paketinis vykdymas.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-113">Check or uncheck the Batch processing checkbox.</span></span>
<span data-ttu-id="6cf7e-114">![Paketinis vykdymas](../dev-itpro/media/batchprocessing.png "Paketinis vykdymas ir pasikartojimas")</span><span class="sxs-lookup"><span data-stu-id="6cf7e-114">![Batch Processing](../dev-itpro/media/batchprocessing.png "Batch Processing & Recurrance")</span></span> 
5. <span data-ttu-id="6cf7e-115">Spustelėkite Pasikartojimas.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-115">Click Recurrence.</span></span>
6. <span data-ttu-id="6cf7e-116">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-116">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="6cf7e-117">Lauke Pradžios laikas įveskite laiką.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-117">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="6cf7e-118">Pasirinkite, jei norite baigti pasikartojimą po konkretaus vykdymų skaičiaus, tam tikrą datą arba niekada.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-118">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="6cf7e-119">Tada pasirinkite įvairias parinktis, norėdami nurodyti, kaip dažnai norite paleisti užduotį.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-119">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="6cf7e-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-120">Click OK.</span></span>
9. <span data-ttu-id="6cf7e-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-121">Click OK.</span></span>

