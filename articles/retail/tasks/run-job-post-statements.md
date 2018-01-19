--- 
title: " Konfigūruoti ir vykdyti užduotis įrašams registruoti"
description: "Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančią paketinę užduotį, norint registruoti pasirinktos parduotuvės arba parduotuvių grupės išrašus."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: d05e37790aa1068222f2e98ff71fc3fa5eedb0ed
ms.contentlocale: lt-lt
ms.lasthandoff: 01/19/2018

---
# <a name="configure-and-run-a-job-to-post-statements"></a><span data-ttu-id="39219-103"> Konfigūruoti ir vykdyti užduotis įrašams registruoti</span><span class="sxs-lookup"><span data-stu-id="39219-103">Configure and run a job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="39219-104">Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančią paketinę užduotį, norint registruoti pasirinktos parduotuvės arba parduotuvių grupės išrašus.</span><span class="sxs-lookup"><span data-stu-id="39219-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="39219-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="39219-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="39219-106">Eikite į Visos darbo sritys > ..</span><span class="sxs-lookup"><span data-stu-id="39219-106">Go to All workspaces > ..</span></span> <span data-ttu-id="39219-107">> Mažmeninės prekybos parduotuvės finansai.</span><span class="sxs-lookup"><span data-stu-id="39219-107">> Retail store financials.</span></span>
2. <span data-ttu-id="39219-108">Spustelėkite Registruoti išrašus.</span><span class="sxs-lookup"><span data-stu-id="39219-108">Click Post statements.</span></span>
    * <span data-ttu-id="39219-109">Pasirinkite organizacijos hierarchiją ir organizacijos mazgų medį, pasirinkite atskirą parduotuvę arba mazgą.</span><span class="sxs-lookup"><span data-stu-id="39219-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="39219-110">Pasirinkite mazgą, jei norite kurti parduotuvių grupės paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="39219-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="39219-111">Spustelėkite rodyklę ir įtraukite savo pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="39219-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="39219-112">Spustelėkite skirtuką Vykdyti fone.</span><span class="sxs-lookup"><span data-stu-id="39219-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="39219-113">Pažymėkite arba atžymėkite žymės langelį Paketinis vykdymas.</span><span class="sxs-lookup"><span data-stu-id="39219-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="39219-114">Spustelėkite Pasikartojimas.</span><span class="sxs-lookup"><span data-stu-id="39219-114">Click Recurrence.</span></span>
6. <span data-ttu-id="39219-115">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="39219-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="39219-116">Lauke Pradžios laikas įveskite laiką.</span><span class="sxs-lookup"><span data-stu-id="39219-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="39219-117">Pasirinkite, jei norite baigti pasikartojimą po konkretaus vykdymų skaičiaus, tam tikrą datą arba niekada.</span><span class="sxs-lookup"><span data-stu-id="39219-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="39219-118">Tada pasirinkite įvairias parinktis, norėdami nurodyti, kaip dažnai norite paleisti užduotį.</span><span class="sxs-lookup"><span data-stu-id="39219-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="39219-119">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="39219-119">Click OK.</span></span>
9. <span data-ttu-id="39219-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="39219-120">Click OK.</span></span>


