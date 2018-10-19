--- 
title: "Konfigūruoti ir vykdyti išrašų registravimo užduotį"
description: "Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančią paketinę užduotį, norint registruoti pasirinktos parduotuvės arba parduotuvių grupės išrašus."
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 676216d90c50c0d3fa1a839cab7a734e624708ba
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="653ca-103">Konfigūruoti ir vykdyti išrašų registravimo užduotį</span><span class="sxs-lookup"><span data-stu-id="653ca-103">Configure and run job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="653ca-104">Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančią paketinę užduotį, norint registruoti pasirinktos parduotuvės arba parduotuvių grupės išrašus.</span><span class="sxs-lookup"><span data-stu-id="653ca-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="653ca-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="653ca-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="653ca-106">Eikite į Visos darbo sritys > ..</span><span class="sxs-lookup"><span data-stu-id="653ca-106">Go to All workspaces > ..</span></span> <span data-ttu-id="653ca-107">> Mažmeninės prekybos parduotuvės finansai.</span><span class="sxs-lookup"><span data-stu-id="653ca-107">> Retail store financials.</span></span>
2. <span data-ttu-id="653ca-108">Spustelėkite Registruoti išrašus.</span><span class="sxs-lookup"><span data-stu-id="653ca-108">Click Post statements.</span></span>
    * <span data-ttu-id="653ca-109">Pasirinkite organizacijos hierarchiją ir organizacijos mazgų medį, pasirinkite atskirą parduotuvę arba mazgą.</span><span class="sxs-lookup"><span data-stu-id="653ca-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="653ca-110">Pasirinkite mazgą, jei norite kurti parduotuvių grupės paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="653ca-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="653ca-111">Spustelėkite rodyklę ir įtraukite savo pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="653ca-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="653ca-112">Spustelėkite skirtuką Vykdyti fone.</span><span class="sxs-lookup"><span data-stu-id="653ca-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="653ca-113">Pažymėkite arba atžymėkite žymės langelį Paketinis vykdymas.</span><span class="sxs-lookup"><span data-stu-id="653ca-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="653ca-114">Spustelėkite Pasikartojimas.</span><span class="sxs-lookup"><span data-stu-id="653ca-114">Click Recurrence.</span></span>
6. <span data-ttu-id="653ca-115">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="653ca-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="653ca-116">Lauke Pradžios laikas įveskite laiką.</span><span class="sxs-lookup"><span data-stu-id="653ca-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="653ca-117">Pasirinkite, jei norite baigti pasikartojimą po konkretaus vykdymų skaičiaus, tam tikrą datą arba niekada.</span><span class="sxs-lookup"><span data-stu-id="653ca-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="653ca-118">Tada pasirinkite įvairias parinktis, norėdami nurodyti, kaip dažnai norite paleisti užduotį.</span><span class="sxs-lookup"><span data-stu-id="653ca-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="653ca-119">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="653ca-119">Click OK.</span></span>
9. <span data-ttu-id="653ca-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="653ca-120">Click OK.</span></span>


