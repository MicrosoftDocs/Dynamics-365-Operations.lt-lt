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
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b7356706ea80c97fdf5b73faf32134a4aebacbb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179038"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="24041-103">Konfigūruoti savikainos objekto valdiklio prieigos teises</span><span class="sxs-lookup"><span data-stu-id="24041-103">Configure access rights for a cost object controller</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="24041-104">Pasinaudokite šia procedūra, norėdami konfigūruoti prieigos teises savikainos objekto kontrolieriui.</span><span class="sxs-lookup"><span data-stu-id="24041-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="24041-105">Šiame įraše naudojama demonstracinių duomenų įmonė USP2.</span><span class="sxs-lookup"><span data-stu-id="24041-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="24041-106">Priskirti išlaidų objekto kontrolieriaus vaidmenį</span><span class="sxs-lookup"><span data-stu-id="24041-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="24041-107">Pasirinkite Sistemos administravimas > Vartotojai > Vartotojai.</span><span class="sxs-lookup"><span data-stu-id="24041-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="24041-108">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="24041-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="24041-109">Pavyzdžiui, filtruokite lauką Vartotojo vardas, naudodami reikšmę „alicia‟.</span><span class="sxs-lookup"><span data-stu-id="24041-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="24041-110">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="24041-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="24041-111">Spustelėkite „Priskirti vaidmenis“.</span><span class="sxs-lookup"><span data-stu-id="24041-111">Click Assign roles.</span></span>
5. <span data-ttu-id="24041-112">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="24041-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="24041-113">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="24041-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="24041-114">Įgalinti prieigos sąrašo saugą</span><span class="sxs-lookup"><span data-stu-id="24041-114">Enable access list security</span></span>
1. <span data-ttu-id="24041-115">Eikite į Išlaidų apskaita > Dimensijos > Dimensijų hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="24041-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="24041-116">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="24041-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="24041-117">Pasirinkti organizaciją</span><span class="sxs-lookup"><span data-stu-id="24041-117">Select Organization.</span></span>  
3. <span data-ttu-id="24041-118">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="24041-118">Click Edit.</span></span>
4. <span data-ttu-id="24041-119">Pasirinkite Taip lauke Prieigos sąrašo hierarchija.</span><span class="sxs-lookup"><span data-stu-id="24041-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="24041-120">Spustelėkite Peržiūrėti hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="24041-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="24041-121">Priskirti prieigos teises vartotojui</span><span class="sxs-lookup"><span data-stu-id="24041-121">Assign access rights to user</span></span>
1. <span data-ttu-id="24041-122">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="24041-122">Click New.</span></span>
2. <span data-ttu-id="24041-123">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="24041-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="24041-124">Lauke Vartotojo ID įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="24041-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="24041-125">Pasirinkite Admin.</span><span class="sxs-lookup"><span data-stu-id="24041-125">Select Admin.</span></span>  
4. <span data-ttu-id="24041-126">Medyje pasirinkite „Organization\CEO\CFO\FIM“.</span><span class="sxs-lookup"><span data-stu-id="24041-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="24041-127">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="24041-127">Click New.</span></span>
6. <span data-ttu-id="24041-128">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="24041-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="24041-129">Lauke Vartotojo ID įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="24041-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="24041-130">Pasirinkite Alicia.</span><span class="sxs-lookup"><span data-stu-id="24041-130">Select Alicia.</span></span>  
8. <span data-ttu-id="24041-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="24041-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="24041-132">Įgalinti išlaidų apskaitos prieigos teises</span><span class="sxs-lookup"><span data-stu-id="24041-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="24041-133">Eikite į Savikainos apskaita > Sąranka > Parametrai.</span><span class="sxs-lookup"><span data-stu-id="24041-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="24041-134">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="24041-134">Click the General tab.</span></span>
3. <span data-ttu-id="24041-135">Pasirinkite Taip lauke Įgalinti savikainos objekto dimensijos narių peržiūros prieigą.</span><span class="sxs-lookup"><span data-stu-id="24041-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="24041-136">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="24041-136">Click Save.</span></span>
5. <span data-ttu-id="24041-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="24041-137">Close the page.</span></span>
6. <span data-ttu-id="24041-138">Eikite į Savikainos apskaita > Sąranka > Savikainos kontrolės darbo srities konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="24041-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="24041-139">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="24041-139">Click Edit.</span></span>
8. <span data-ttu-id="24041-140">Lauke Paskelbta pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="24041-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="24041-141">Jei pasirenkate Taip, vartotojas, kuriam priskirtas vienas iš tolesnių keturių vaidmenų, gali matyti ataskaitas savikainos kontrolės darbo srityje: savikainos apskaitos vadovas, savikainos apskaitininkas, savikainos apskaitininko klerkas ir išlaidų objekto kontrolierius.</span><span class="sxs-lookup"><span data-stu-id="24041-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="24041-142">Jei pasirenkate Ne, vartotojas, kuriam priskirtas vienas iš tolesnių vaidmenų, gali matyti ataskaitas: savikainos apskaitos vadovas, savikainos apskaitininkas ir savikainos apskaitininko klerkas.</span><span class="sxs-lookup"><span data-stu-id="24041-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="24041-143">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="24041-143">Click Save.</span></span>

