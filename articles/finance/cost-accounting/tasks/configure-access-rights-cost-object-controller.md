---
title: Konfigūruoti savikainos objekto valdiklio prieigos teises
description: Pasinaudokite šia procedūra, norėdami konfigūruoti prieigos teises savikainos objekto kontrolieriui.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eef755dd9a44ce24d3bfb2953cf9a52e6a8ac849
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822884"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="00944-103">Konfigūruoti savikainos objekto valdiklio prieigos teises</span><span class="sxs-lookup"><span data-stu-id="00944-103">Configure access rights for a cost object controller</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="00944-104">Pasinaudokite šia procedūra, norėdami konfigūruoti prieigos teises savikainos objekto kontrolieriui.</span><span class="sxs-lookup"><span data-stu-id="00944-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="00944-105">Šiame įraše naudojama demonstracinių duomenų įmonė USP2.</span><span class="sxs-lookup"><span data-stu-id="00944-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="00944-106">Priskirti išlaidų objekto kontrolieriaus vaidmenį</span><span class="sxs-lookup"><span data-stu-id="00944-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="00944-107">Pasirinkite Sistemos administravimas > Vartotojai > Vartotojai.</span><span class="sxs-lookup"><span data-stu-id="00944-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="00944-108">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="00944-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="00944-109">Pavyzdžiui, filtruokite lauką Vartotojo vardas, naudodami reikšmę „alicia‟.</span><span class="sxs-lookup"><span data-stu-id="00944-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="00944-110">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="00944-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="00944-111">Spustelėkite „Priskirti vaidmenis“.</span><span class="sxs-lookup"><span data-stu-id="00944-111">Click Assign roles.</span></span>
5. <span data-ttu-id="00944-112">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="00944-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="00944-113">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="00944-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="00944-114">Įgalinti prieigos sąrašo saugą</span><span class="sxs-lookup"><span data-stu-id="00944-114">Enable access list security</span></span>
1. <span data-ttu-id="00944-115">Eikite į Išlaidų apskaita > Dimensijos > Dimensijų hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="00944-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="00944-116">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="00944-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="00944-117">Pasirinkti organizaciją</span><span class="sxs-lookup"><span data-stu-id="00944-117">Select Organization.</span></span>  
3. <span data-ttu-id="00944-118">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="00944-118">Click Edit.</span></span>
4. <span data-ttu-id="00944-119">Pasirinkite Taip lauke Prieigos sąrašo hierarchija.</span><span class="sxs-lookup"><span data-stu-id="00944-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="00944-120">Spustelėkite Peržiūrėti hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="00944-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="00944-121">Priskirti prieigos teises vartotojui</span><span class="sxs-lookup"><span data-stu-id="00944-121">Assign access rights to user</span></span>
1. <span data-ttu-id="00944-122">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="00944-122">Click New.</span></span>
2. <span data-ttu-id="00944-123">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="00944-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="00944-124">Lauke Vartotojo ID įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="00944-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="00944-125">Pasirinkite Admin.</span><span class="sxs-lookup"><span data-stu-id="00944-125">Select Admin.</span></span>  
4. <span data-ttu-id="00944-126">Medyje pasirinkite „Organization\CEO\CFO\FIM“.</span><span class="sxs-lookup"><span data-stu-id="00944-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="00944-127">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="00944-127">Click New.</span></span>
6. <span data-ttu-id="00944-128">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="00944-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="00944-129">Lauke Vartotojo ID įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="00944-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="00944-130">Pasirinkite Alicia.</span><span class="sxs-lookup"><span data-stu-id="00944-130">Select Alicia.</span></span>  
8. <span data-ttu-id="00944-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="00944-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="00944-132">Įgalinti išlaidų apskaitos prieigos teises</span><span class="sxs-lookup"><span data-stu-id="00944-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="00944-133">Eikite į Savikainos apskaita > Sąranka > Parametrai.</span><span class="sxs-lookup"><span data-stu-id="00944-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="00944-134">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="00944-134">Click the General tab.</span></span>
3. <span data-ttu-id="00944-135">Pasirinkite Taip lauke Įgalinti savikainos objekto dimensijos narių peržiūros prieigą.</span><span class="sxs-lookup"><span data-stu-id="00944-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="00944-136">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="00944-136">Click Save.</span></span>
5. <span data-ttu-id="00944-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="00944-137">Close the page.</span></span>
6. <span data-ttu-id="00944-138">Eikite į Savikainos apskaita > Sąranka > Savikainos kontrolės darbo srities konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="00944-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="00944-139">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="00944-139">Click Edit.</span></span>
8. <span data-ttu-id="00944-140">Lauke Paskelbta pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="00944-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="00944-141">Jei pasirenkate Taip, vartotojas, kuriam priskirtas vienas iš tolesnių keturių vaidmenų, gali matyti ataskaitas savikainos kontrolės darbo srityje: savikainos apskaitos vadovas, savikainos apskaitininkas, savikainos apskaitininko klerkas ir išlaidų objekto kontrolierius.</span><span class="sxs-lookup"><span data-stu-id="00944-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="00944-142">Jei pasirenkate Ne, vartotojas, kuriam priskirtas vienas iš tolesnių vaidmenų, gali matyti ataskaitas: savikainos apskaitos vadovas, savikainos apskaitininkas ir savikainos apskaitininko klerkas.</span><span class="sxs-lookup"><span data-stu-id="00944-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="00944-143">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="00944-143">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]