--- 
title: "Valdyti darbuotojų apgyvendinimą"
description: "Ši procedūra padeda žingsnis po žingsnio atlikti darbo aplinkos patogumų tipų (pvz., ergonominės kėdės arba periodinės pertraukos) nustatymo veiksmus."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a05fec7b79003d5b98470d85644d70bd1dbac285
ms.openlocfilehash: 83c2495eb7602282d7bb97515e655f3dbd33cb4a
ms.contentlocale: lt-lt
ms.lasthandoff: 02/06/2018

---
# <a name="manage-worker-accommodations"></a><span data-ttu-id="e6dcf-103">Valdyti darbuotojų apgyvendinimą</span><span class="sxs-lookup"><span data-stu-id="e6dcf-103">Manage worker accommodations</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="e6dcf-104">Ši procedūra padeda žingsnis po žingsnio atlikti darbo aplinkos patogumų tipų (pvz., ergonominės kėdės arba periodinės pertraukos) nustatymo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-104">This procedure walks through the steps for setting up work environment accommodation types, such as ergonomic chairs or periodic breaks.</span></span> <span data-ttu-id="e6dcf-105">Ji taip pat nurodo, kaip šiuos patogumų tipus priskirti darbuotojui ir patvirtinti arba atmesti patogumo tipą.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-105">It also shows how to assign these accommodation types to a worker, and either approve or deny the accommodation type.</span></span> <span data-ttu-id="e6dcf-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="setup-accommodations"></a><span data-ttu-id="e6dcf-107">Nustatyti patogumus</span><span class="sxs-lookup"><span data-stu-id="e6dcf-107">Setup accommodations</span></span>
1. <span data-ttu-id="e6dcf-108">Pasirinkite Personalas > Nustatymas > Patogumų tipai.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-108">Go to Human resources > Setup > Accommodation types.</span></span>
2. <span data-ttu-id="e6dcf-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-109">Click New.</span></span>
3. <span data-ttu-id="e6dcf-110">Lauke „Patogumo tipas“ įveskite patogumo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-110">In the Accommodation type field, enter a name for the accommodation.</span></span> <span data-ttu-id="e6dcf-111">Pavyzdys: klaviatūra.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-111">Example: Keyboard.</span></span>
4. <span data-ttu-id="e6dcf-112">Lauke „Aprašas“ įveskite patogumo aprašą.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-112">In the Description field, enter a description for the accommodation.</span></span> <span data-ttu-id="e6dcf-113">Pavyzdys: ergonomiška klaviatūra.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-113">Example: Ergonomic Keyboard.</span></span>
5. <span data-ttu-id="e6dcf-114">Lauke „Pastaba“ įveskite bet kokią informaciją, kuri padeda paaiškinti patogumą.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-114">In the Note field, enter any information that helps to clarify the accommodation.</span></span>
6. <span data-ttu-id="e6dcf-115">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-115">Click Save.</span></span>
7. <span data-ttu-id="e6dcf-116">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-116">Close the page.</span></span>

## <a name="assign-accommodations"></a><span data-ttu-id="e6dcf-117">Priskirti patogumus</span><span class="sxs-lookup"><span data-stu-id="e6dcf-117">Assign accommodations</span></span>
1. <span data-ttu-id="e6dcf-118">Pasirinkite Personalas > Darbuotojai > Darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-118">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="e6dcf-119">Iš sąrašo pasirinkite darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-119">From the list, select an employee.</span></span>
3. <span data-ttu-id="e6dcf-120">Spustelėkite darbuotojo vardą norėdami peržiūrėti informaciją apie darbuotoją, kuris prašo suteikti patogumą.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-120">Click the employee's name to view details about the employee who is requesting the accommodation.</span></span>
4. <span data-ttu-id="e6dcf-121">Išplėskite „FastTab“ asmeninę informaciją.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-121">Expand the Personal information FastTab.</span></span>
5. <span data-ttu-id="e6dcf-122">Spustelėkite „Patogumai“.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-122">Click Accommodations.</span></span>
6. <span data-ttu-id="e6dcf-123">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-123">Click New.</span></span>
7. <span data-ttu-id="e6dcf-124">Lauke „Patogumo tipas“ pasirinkite atitinkamą patogumą.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-124">In the Accommodation type field, select the appropriate accommodation.</span></span> <span data-ttu-id="e6dcf-125">Pavyzdys: klaviatūra</span><span class="sxs-lookup"><span data-stu-id="e6dcf-125">Example: Keyboard</span></span>
8. <span data-ttu-id="e6dcf-126">Lauke „Darbo užduotis“ įveskite darbo užduotį, kuriai reikia patogumo.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-126">In the Job task field, enter the work task that requires the accommodation.</span></span>
9. <span data-ttu-id="e6dcf-127">Lauke „Būsena“ įveskite atitinkamą būseną.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-127">In the Status field, enter the appropriate status.</span></span> <span data-ttu-id="e6dcf-128">Pavyzdys: pagrįsta</span><span class="sxs-lookup"><span data-stu-id="e6dcf-128">Example: Reasonable</span></span>
    * <span data-ttu-id="e6dcf-129">Galimos šios būsenos.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-129">The following statuses are available.</span></span> <span data-ttu-id="e6dcf-130">„Pageidaujama“ nurodo, kad patogumas sukurtas, bet dar neperžiūrėtas.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-130">Requested indicates that the accommodation has been created but not yet reviewed.</span></span> <span data-ttu-id="e6dcf-131">„Pagrįstas“ nurodo, kad patogumas yra pagrįstas ir bus patenkintas.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-131">Reasonable indicates that the accommodation is reasonable and will be granted.</span></span> <span data-ttu-id="e6dcf-132">„Netikėti sunkumai“ nurodo, kad toks patogumas darbdaviui užkrautų nepagrįstą naštą, todėl buvo atmestas.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-132">Undue hardship indicates that the accommodation will place an unreasonable burden on the employer, and has been denied.</span></span> <span data-ttu-id="e6dcf-133">Šiame pavyzdyje prašymas buvo patvirtintas iš karto, nes patogumų prašymas buvo minimalus.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-133">In this example, the request was approved immediately because the accommodation request was minimal.</span></span>  
10. <span data-ttu-id="e6dcf-134">Lauke „Priimta“ pasirinkite asmenį, kuris priėmė patogumo užklausą.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-134">In the Accepted field, select the person who accepted the accommodation request.</span></span>
11. <span data-ttu-id="e6dcf-135">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-135">Click Select.</span></span>
12. <span data-ttu-id="e6dcf-136">Lauke „Priėmimo data“ įveskite datą ir laiką, kada buvo priimta patogumo užklausa.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-136">In the Accepted date field, enter the date and time when the accommodation request was accepted.</span></span>
13. <span data-ttu-id="e6dcf-137">Išplėskite skyrių „Pastaba“.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-137">Expand the Note section.</span></span>
14. <span data-ttu-id="e6dcf-138">Lauke „Finansinė informacija“ įveskite bet kokią informaciją arba išteklių išlaidas, kurios padeda paaiškinti patogumų poveikį.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-138">In the Financial field, enter any information or resource costs that helps to clarify the impact of the accommodation.</span></span>
    * <span data-ttu-id="e6dcf-139">Jei patogumas buvo atmestas, lauke „Atsakyti“ galima nurodyti, kodėl prašymas buvo atmestas.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-139">If the accommodation has been denied, the Reply field can be used to indicate why a request was denied.</span></span>  
15. <span data-ttu-id="e6dcf-140">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-140">Click Save.</span></span>


