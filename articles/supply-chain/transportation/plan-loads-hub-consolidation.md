---
title: "Krovinių planavimas naudojant tranzito punktų konsolidaciją"
description: "Šiame straipsnyje aprašomas siuntų konsolidavimas tranzito punkte, kai tam pačiam klientui pristatomos prekės iš skirtingų sandėlių arba kai prekės į tą patį sandėlį pristatomos iš kelių tiekėjų."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 3145febe40108e50b263514de1ca541dd914b7c5
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="plan-loads-using-hub-consolidation"></a><span data-ttu-id="dba7f-103">Krovinių planavimas naudojant tranzito punktų konsolidaciją</span><span class="sxs-lookup"><span data-stu-id="dba7f-103">Plan loads using hub consolidation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="dba7f-104">Šiame straipsnyje aprašomas siuntų konsolidavimas tranzito punkte, kai tam pačiam klientui pristatomos prekės iš skirtingų sandėlių arba kai prekės į tą patį sandėlį pristatomos iš kelių tiekėjų.</span><span class="sxs-lookup"><span data-stu-id="dba7f-104">This article describes the feature for consolidating shipments in a hub when you deliver goods from different warehouses to the same customer, or when you receive goods from multiple vendors in the same warehouse.</span></span>

<span data-ttu-id="dba7f-105">Gali būti naudinga konsoliduoti siuntas tranzito punkte, kai tam pačiam klientui pristatote prekes iš skirtingų sandėlių arba kai prekės į tą patį sandėlį pristatomos iš kelių tiekėjų.</span><span class="sxs-lookup"><span data-stu-id="dba7f-105">It can be useful to consolidate shipments in a hub when you deliver goods from different warehouses to the same customer, or when goods are delivered from multiple vendors to the same warehouse.</span></span>

## <a name="building-loads"></a><span data-ttu-id="dba7f-106">Krovinių kūrimas</span><span class="sxs-lookup"><span data-stu-id="dba7f-106">Building loads</span></span>
<span data-ttu-id="dba7f-107">Norėdami naudoti tranzito punktų konsolidaciją, puslapyje **transporto valdymo parametrai** turite įjungti parinktį **Transportavimo valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="dba7f-107">Before you can use hub consolidation, you must enable the **In transit planning** option on the **Transportation management parameters** page.</span></span> <span data-ttu-id="dba7f-108">Taip pat turite sukurti tranzito punktus, kuriuose bus vykdoma konsolidacija.</span><span class="sxs-lookup"><span data-stu-id="dba7f-108">You must also create the hubs where consolidation will occur.</span></span> <span data-ttu-id="dba7f-109">Pateiktoje diagramoje parodytas tranzito punktų konsolidacijos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="dba7f-109">The following diagram shows an example of hub consolidation.</span></span> <span data-ttu-id="dba7f-110">Šiuo atveju pardavimo užsakymai iš skirtingų sandėlių vykdomi tam pačiam klientu.</span><span class="sxs-lookup"><span data-stu-id="dba7f-110">In this case, sales orders from different warehouses are going to the same customer.</span></span> <span data-ttu-id="dba7f-111">Pagrindiniai kroviniai kuriami pagal pardavimo užsakymus įprastu būdu, naudojant puslapį **Krovinio planavimo darbo sritis**.</span><span class="sxs-lookup"><span data-stu-id="dba7f-111">The basic loads are created based on sales orders in the usual way, by using the **Load planning workbench** page.</span></span> <span data-ttu-id="dba7f-112">Norėdami tranzito punkte konsoliduoti du krovinius prieš juos pristatydami klientui, puslapio **Krovinio planavimo darbo sritis** lauke **Transportavimas** pasirinkite **Tranzito punktų konsolidacija**.</span><span class="sxs-lookup"><span data-stu-id="dba7f-112">To consolidate the two loads in a hub before they are delivered to the customer, on the **Load planning workbench** page, in the **Transportation** field, select **Hub consolidation**.</span></span> <span data-ttu-id="dba7f-113">Kiekvienam kroviniui parinkus teisingą tranzito punktą, krovinių tranzito punktas bus nustatytas kaip „pridavimo“ paskirties vieta.</span><span class="sxs-lookup"><span data-stu-id="dba7f-113">When you select the correct hub for each load, the loads will have the hub as the “drop off” destination.</span></span> <span data-ttu-id="dba7f-114">Puslapio **Krovinio planavimo darbo sritis** dalyje **Tiekimas ir poreikis** taip pat bus pateiktos dvi transportavimo užklausos eilutės.</span><span class="sxs-lookup"><span data-stu-id="dba7f-114">You will also have two “transportation request lines” in the **Supply and Demand** section on the **Load planning workbench** page.</span></span> <span data-ttu-id="dba7f-115">Tada šias dvi eilutes galite įtraukti į naują krovinį.</span><span class="sxs-lookup"><span data-stu-id="dba7f-115">You can then add these two lines to a new load.</span></span> <span data-ttu-id="dba7f-116">Šiame naujame krovinyje bus abi pardavimo užsakymo eilutės, jo tranzito punktas bus nustatytas kaip „paėmimo“ adresas, o A klientas – kaip „pridavimo“ paskirties vieta.</span><span class="sxs-lookup"><span data-stu-id="dba7f-116">This new load will have both sales order lines, and will also have the hub as the “pick up” address and customer A as the “drop off” destination.</span></span> <span data-ttu-id="dba7f-117">Tada visų trijų krovinių tarifą ir maršrutą bus galima nustatyti kaip bet kurio kito krovinio tarifą ir maršrutą.</span><span class="sxs-lookup"><span data-stu-id="dba7f-117">The three loads are then ready to be rated and routed like any other load.</span></span> <span data-ttu-id="dba7f-118">Galite pasirinkti bet kokį kiekvieno krovinio vežėją, kurį pasiūlys sistema.</span><span class="sxs-lookup"><span data-stu-id="dba7f-118">You can select whatever shipping carrier the system suggests for each load.</span></span> <span data-ttu-id="dba7f-119">[![Tranzito punktų konsolidacija](./media/hubconsol.jpg)](./media/hubconsol.jpg) Taip pat tą patį metodą galite naudoti norėdami konsoliduoti kelių perkėlimo užsakymų krovinius.</span><span class="sxs-lookup"><span data-stu-id="dba7f-119">[![Hub consolidation](./media/hubconsol.jpg)](./media/hubconsol.jpg) You can also use the same method to consolidate loads for multiple transfer orders.</span></span> <span data-ttu-id="dba7f-120">Šiuo atveju ankstesnėje diagramoje A klientas yra sandėlis.</span><span class="sxs-lookup"><span data-stu-id="dba7f-120">In this case, customer A in the preceding diagram is a warehouse.</span></span> <span data-ttu-id="dba7f-121">Arba galite konsoliduoti kelių pirkimo užsakymų krovinius, kurie į tą patį sandėlį pristatomi iš įvairių tiekėjų.</span><span class="sxs-lookup"><span data-stu-id="dba7f-121">Alternatively, you can consolidate loads for multiple purchase orders, where the loads are delivered from different vendors to the same warehouse.</span></span> <span data-ttu-id="dba7f-122">Galite nustatyti daugiau nei vieną konsolidavimo tranzito punktą, ir papildomus krovinius, gabenamus iš įvairių sandėlių, galite konsoliduoti keliuose tranzito punktuose.</span><span class="sxs-lookup"><span data-stu-id="dba7f-122">You can have more than one consolidation hub, and can consolidate in multiple hubs for more loads that come from different warehouses.</span></span> <span data-ttu-id="dba7f-123">Kai sukuriate pagrindinius krovinius ir naudojate tranzito punktų konsolidavimo parinktį, naujus krovinius kurkite naudodami konsoliduoto transportavimo užklausos eilutes.</span><span class="sxs-lookup"><span data-stu-id="dba7f-123">After you build your basic loads and use the hub consolidation option, you build the new loads by using the consolidated transportation request lines.</span></span> <span data-ttu-id="dba7f-124">Tada galite nustatyti krovinių tarifą ir maršrutą.</span><span class="sxs-lookup"><span data-stu-id="dba7f-124">You then rate and route your loads.</span></span>




