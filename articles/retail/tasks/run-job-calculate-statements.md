--- 
title: " Konfigūruoti ir vykdyti išrašų skaičiavimo užduotį"
description: "Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančias paketines užduotis, norint kurti ir apskaičiuoti pasirinktos parduotuvės arba parduotuvių grupės išrašus."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6d98adc919d50957b92a879b69517e0a826ea45f
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="configure-and-run-a-job-to-calculate-statements"></a><span data-ttu-id="fb110-103"> Konfigūruoti ir vykdyti išrašų skaičiavimo užduotį</span><span class="sxs-lookup"><span data-stu-id="fb110-103">Configure and run a job to calculate statements</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="fb110-104">Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančias paketines užduotis, norint kurti ir apskaičiuoti pasirinktos parduotuvės arba parduotuvių grupės išrašus.</span><span class="sxs-lookup"><span data-stu-id="fb110-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="fb110-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="fb110-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="fb110-106">Eikite į Visos darbo sritys > Mažmeninės prekybos parduotuvės finansai.</span><span class="sxs-lookup"><span data-stu-id="fb110-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="fb110-107">Spustelėkite Skaičiuoti išrašus.</span><span class="sxs-lookup"><span data-stu-id="fb110-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="fb110-108">Pasirinkite konkrečią parduotuvę arba mazgą, jei norite kurti parduotuvių grupės paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="fb110-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="fb110-109">Spustelėkite rodyklę ir įtraukite savo pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="fb110-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="fb110-110">Spustelėkite skirtuką Vykdyti fone.</span><span class="sxs-lookup"><span data-stu-id="fb110-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="fb110-111">Šalia dalis Paketinis vykdymas pasirinkite „Taip“.</span><span class="sxs-lookup"><span data-stu-id="fb110-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="fb110-112">Spustelėkite Pasikartojimas.</span><span class="sxs-lookup"><span data-stu-id="fb110-112">Click Recurrence.</span></span>
6. <span data-ttu-id="fb110-113">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="fb110-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="fb110-114">Lauke Pradžios laikas įveskite laiką.</span><span class="sxs-lookup"><span data-stu-id="fb110-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="fb110-115">Pasirinkite parinktį Nėra pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="fb110-115">Select the No end date option.</span></span>
9. <span data-ttu-id="fb110-116">Lauke „PatternUnit“ įveskite „Dienos“.</span><span class="sxs-lookup"><span data-stu-id="fb110-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="fb110-117">Lauke Per įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="fb110-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="fb110-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="fb110-118">Click OK.</span></span>
12. <span data-ttu-id="fb110-119">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="fb110-119">Click OK.</span></span>


