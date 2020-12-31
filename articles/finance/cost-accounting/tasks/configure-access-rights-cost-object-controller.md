---
title: Konfigūruoti savikainos objekto valdiklio prieigos teises
description: Pasinaudokite šia procedūra, norėdami konfigūruoti prieigos teises savikainos objekto kontrolieriui.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4b50782c7a1b69b6953c65d6df155f003028333
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446142"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="c1844-103">Konfigūruoti savikainos objekto valdiklio prieigos teises</span><span class="sxs-lookup"><span data-stu-id="c1844-103">Configure access rights for a cost object controller</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1844-104">Pasinaudokite šia procedūra, norėdami konfigūruoti prieigos teises savikainos objekto kontrolieriui.</span><span class="sxs-lookup"><span data-stu-id="c1844-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="c1844-105">Šiame įraše naudojama demonstracinių duomenų įmonė USP2.</span><span class="sxs-lookup"><span data-stu-id="c1844-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="c1844-106">Priskirti išlaidų objekto kontrolieriaus vaidmenį</span><span class="sxs-lookup"><span data-stu-id="c1844-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="c1844-107">Pasirinkite Sistemos administravimas > Vartotojai > Vartotojai.</span><span class="sxs-lookup"><span data-stu-id="c1844-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="c1844-108">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="c1844-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c1844-109">Pavyzdžiui, filtruokite lauką Vartotojo vardas, naudodami reikšmę „alicia‟.</span><span class="sxs-lookup"><span data-stu-id="c1844-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="c1844-110">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c1844-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c1844-111">Spustelėkite „Priskirti vaidmenis“.</span><span class="sxs-lookup"><span data-stu-id="c1844-111">Click Assign roles.</span></span>
5. <span data-ttu-id="c1844-112">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="c1844-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="c1844-113">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c1844-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="c1844-114">Įgalinti prieigos sąrašo saugą</span><span class="sxs-lookup"><span data-stu-id="c1844-114">Enable access list security</span></span>
1. <span data-ttu-id="c1844-115">Eikite į Išlaidų apskaita > Dimensijos > Dimensijų hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="c1844-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="c1844-116">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="c1844-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c1844-117">Pasirinkti organizaciją</span><span class="sxs-lookup"><span data-stu-id="c1844-117">Select Organization.</span></span>  
3. <span data-ttu-id="c1844-118">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="c1844-118">Click Edit.</span></span>
4. <span data-ttu-id="c1844-119">Pasirinkite Taip lauke Prieigos sąrašo hierarchija.</span><span class="sxs-lookup"><span data-stu-id="c1844-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="c1844-120">Spustelėkite Peržiūrėti hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="c1844-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="c1844-121">Priskirti prieigos teises vartotojui</span><span class="sxs-lookup"><span data-stu-id="c1844-121">Assign access rights to user</span></span>
1. <span data-ttu-id="c1844-122">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c1844-122">Click New.</span></span>
2. <span data-ttu-id="c1844-123">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="c1844-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="c1844-124">Lauke Vartotojo ID įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="c1844-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="c1844-125">Pasirinkite Admin.</span><span class="sxs-lookup"><span data-stu-id="c1844-125">Select Admin.</span></span>  
4. <span data-ttu-id="c1844-126">Medyje pasirinkite „Organization\CEO\CFO\FIM“.</span><span class="sxs-lookup"><span data-stu-id="c1844-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="c1844-127">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c1844-127">Click New.</span></span>
6. <span data-ttu-id="c1844-128">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="c1844-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="c1844-129">Lauke Vartotojo ID įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="c1844-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="c1844-130">Pasirinkite Alicia.</span><span class="sxs-lookup"><span data-stu-id="c1844-130">Select Alicia.</span></span>  
8. <span data-ttu-id="c1844-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c1844-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="c1844-132">Įgalinti išlaidų apskaitos prieigos teises</span><span class="sxs-lookup"><span data-stu-id="c1844-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="c1844-133">Eikite į Savikainos apskaita > Sąranka > Parametrai.</span><span class="sxs-lookup"><span data-stu-id="c1844-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="c1844-134">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="c1844-134">Click the General tab.</span></span>
3. <span data-ttu-id="c1844-135">Pasirinkite Taip lauke Įgalinti savikainos objekto dimensijos narių peržiūros prieigą.</span><span class="sxs-lookup"><span data-stu-id="c1844-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="c1844-136">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c1844-136">Click Save.</span></span>
5. <span data-ttu-id="c1844-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c1844-137">Close the page.</span></span>
6. <span data-ttu-id="c1844-138">Eikite į Savikainos apskaita > Sąranka > Savikainos kontrolės darbo srities konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="c1844-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="c1844-139">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="c1844-139">Click Edit.</span></span>
8. <span data-ttu-id="c1844-140">Lauke Paskelbta pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="c1844-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="c1844-141">Jei pasirenkate Taip, vartotojas, kuriam priskirtas vienas iš tolesnių keturių vaidmenų, gali matyti ataskaitas savikainos kontrolės darbo srityje: savikainos apskaitos vadovas, savikainos apskaitininkas, savikainos apskaitininko klerkas ir išlaidų objekto kontrolierius.</span><span class="sxs-lookup"><span data-stu-id="c1844-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="c1844-142">Jei pasirenkate Ne, vartotojas, kuriam priskirtas vienas iš tolesnių vaidmenų, gali matyti ataskaitas: savikainos apskaitos vadovas, savikainos apskaitininkas ir savikainos apskaitininko klerkas.</span><span class="sxs-lookup"><span data-stu-id="c1844-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="c1844-143">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c1844-143">Click Save.</span></span>

