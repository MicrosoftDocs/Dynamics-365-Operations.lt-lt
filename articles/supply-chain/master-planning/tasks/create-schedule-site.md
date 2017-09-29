--- 
title: "Vietos grafiko kūrimas"
description: "Šia procedūra rodoma, kaip planuoti dar nepradėtus vietos gamybos užsakymus."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 775428bf84a752c03c492e764fa9ed576ab64fb8
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="4ef0a-103">Vietos grafiko kūrimas</span><span class="sxs-lookup"><span data-stu-id="4ef0a-103">Create a schedule for a site</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4ef0a-104">Šia procedūra rodoma, kaip planuoti dar nepradėtus vietos gamybos užsakymus.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="4ef0a-105">Atlikti šiai procedūrai naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="4ef0a-106">Nepradėtų gamybos užsakymų identifikavimas</span><span class="sxs-lookup"><span data-stu-id="4ef0a-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="4ef0a-107">Pasirinkite Gamybos kontrolė > Gamybos užsakymai > Visi gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="4ef0a-108">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4ef0a-109">Pvz., filtruokite lauką Vieta reikšme „1“.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="4ef0a-110">1 – tai USMF vieta.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-110">1 represents a site in USMF.</span></span> <span data-ttu-id="4ef0a-111">Jei USMF nenaudojate, vietą pasirinkite iš savo įmonės.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="4ef0a-112">Atidarykite stulpelio filtrą Būsena.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="4ef0a-113">Laukui Būsena taikykite filtrą – reikšmę Suplanuota, naudodami filtro operatorių „yra tiksliai‟.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="4ef0a-114">Grafiko kūrimas</span><span class="sxs-lookup"><span data-stu-id="4ef0a-114">Create a schedule</span></span>
1. <span data-ttu-id="4ef0a-115">Pažymėkite arba atžymėkite visas sąrašo eilutes.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="4ef0a-116">Veiksmų srityje spustelėkite Grafikas.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="4ef0a-117">Spustelėkite Planuoti užduotis.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="4ef0a-118">Lauke Planavimo kryptis pasirinkite „Atgal nuo pristatymo datos‟.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="4ef0a-119">Lauke Ribotas pajėgumas pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="4ef0a-120">Lauke Ribotos medžiagos pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="4ef0a-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-121">Click OK.</span></span>
    * <span data-ttu-id="4ef0a-122">Tai gali užtrukti.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="4ef0a-123">Suplanuotų gamybos užsakymų rezultato peržiūra</span><span class="sxs-lookup"><span data-stu-id="4ef0a-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="4ef0a-124">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4ef0a-125">Galite pažymėti bet kurią eilutę.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-125">You can mark any row.</span></span>  
2. <span data-ttu-id="4ef0a-126">Veiksmų srityje spustelėkite Gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="4ef0a-127">Spustelėkite Visos užduotys.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-127">Click All jobs.</span></span>
    * <span data-ttu-id="4ef0a-128">Šiame puslapyje galite matyti užduočių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="4ef0a-129">Skirtuke Planavimas galite matyti užduoties pradžios datą ir pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="4ef0a-130">Spustelėkite Medžiagos.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-130">Click Materials.</span></span>
    * <span data-ttu-id="4ef0a-131">Šiame puslapyje galite matyti įvertintą medžiagų suvartojimą gamybos užsakymo operacijoms atlikti ir dabartines turimas atsargas.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  

