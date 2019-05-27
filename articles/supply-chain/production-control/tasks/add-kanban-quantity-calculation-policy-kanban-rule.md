---
title: Į „kanban“ taisyklę įtraukti „kanban“ kiekio skaičiavimo strategiją
description: Šios procedūros tikslas yra sukurti „kanban“ kiekio skaičiavimo strategiją ir įtraukti ją į „kanban“ taisyklę, siekiant optimizuoti „kanban“ dydį ir kiekius.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fffd623104dc403e230128c9234521ad1e39c7bb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568333"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="a74a2-103">Į „kanban“ taisyklę įtraukti „kanban“ kiekio skaičiavimo strategiją</span><span class="sxs-lookup"><span data-stu-id="a74a2-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a74a2-104">Šios procedūros tikslas yra sukurti „kanban“ kiekio skaičiavimo strategiją ir įtraukti ją į „kanban“ taisyklę, siekiant optimizuoti „kanban“ dydį ir kiekius.</span><span class="sxs-lookup"><span data-stu-id="a74a2-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="a74a2-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="a74a2-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a74a2-106">Ši procedūra skirta vertės srauto vadybininkui.</span><span class="sxs-lookup"><span data-stu-id="a74a2-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="a74a2-107">Ši procedūra yra būtina norint sukurti procedūrą „Skaičiuoti „kanban“ kiekio pasiūlymus“.</span><span class="sxs-lookup"><span data-stu-id="a74a2-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="a74a2-108">Sukurti „kanban“ kiekio skaičiavimo strategiją</span><span class="sxs-lookup"><span data-stu-id="a74a2-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="a74a2-109">Pasirinkite Gamybos kontrolė > Periodinės užduotys > „Kanban“ kiekio skaičiavimas > „Kanban“ kiekio skaičiavimo strategijos.</span><span class="sxs-lookup"><span data-stu-id="a74a2-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="a74a2-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a74a2-110">Click New.</span></span>
3. <span data-ttu-id="a74a2-111">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a74a2-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a74a2-112">Pvz., įveskite „Speaker2016“.</span><span class="sxs-lookup"><span data-stu-id="a74a2-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="a74a2-113">Lauke „Bendrasis planas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a74a2-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a74a2-114">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a74a2-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a74a2-115">Pasirinkite „StaticPlan“ poreikiui apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="a74a2-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="a74a2-116">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a74a2-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="a74a2-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a74a2-117">Click Save.</span></span>
8. <span data-ttu-id="a74a2-118">Lauke „Žemiausias „kanban“ kiekis“ įveskite „1“.</span><span class="sxs-lookup"><span data-stu-id="a74a2-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="a74a2-119">Tai yra papildomas „kanban“ skaičius, įtrauktas į „kanban“ kiekio skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="a74a2-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="a74a2-120">Nustatykite pakankamumo koeficiento reikšmę „1“.</span><span class="sxs-lookup"><span data-stu-id="a74a2-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="a74a2-121">Tai yra koeficientas, naudojamas papildomam pakankamų atsargų kiekiui apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="a74a2-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="a74a2-122">Lauke „Dienų į priekį“ įveskite „30‟.</span><span class="sxs-lookup"><span data-stu-id="a74a2-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="a74a2-123">Tai yra dienų skaičius prieš „kanban“ kiekio skaičiavimo datą, įtrauktas į poreikio skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="a74a2-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="a74a2-124">Lauke „Dienų atgal“ įveskite „30‟.</span><span class="sxs-lookup"><span data-stu-id="a74a2-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="a74a2-125">Tai yra dienų skaičius nuo „kanban“ kiekio skaičiavimo datos, įtrauktas į poreikio skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="a74a2-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="a74a2-126">Skaičiavimui naudojama formulė rodoma su faktinėmis reikšmėmis.</span><span class="sxs-lookup"><span data-stu-id="a74a2-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="a74a2-127">Pvz., „kanban“ kiekis = ((vidutinis kasdienis poreikis x gamybos laikas x 2.00 / produkto kiekis sandėliavimo vienetui) + 1</span><span class="sxs-lookup"><span data-stu-id="a74a2-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="a74a2-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a74a2-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="a74a2-129">Į „kanban“ taisyklę įtraukti „kanban“ kiekio skaičiavimo strategiją</span><span class="sxs-lookup"><span data-stu-id="a74a2-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="a74a2-130">Pasirinkite Produkto informacijos valdymas > „Lean manufacturing“ > „Kanban“ taisyklės.</span><span class="sxs-lookup"><span data-stu-id="a74a2-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="a74a2-131">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a74a2-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a74a2-132">Šiai procedūrai pasirinkite „kanban“ taisyklę 000020.</span><span class="sxs-lookup"><span data-stu-id="a74a2-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="a74a2-133">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a74a2-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a74a2-134">Perjunkite skyriaus „Kanban“ kiekio skaičiavimo strategija“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="a74a2-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="a74a2-135">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="a74a2-135">Click Add.</span></span>
    * <span data-ttu-id="a74a2-136">Pridėkite „kanban“ kiekio skaičiavimo strategiją, kurią ką tik sukūrėte ankstesnėje papildomoje užduotyje.</span><span class="sxs-lookup"><span data-stu-id="a74a2-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="a74a2-137">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a74a2-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="a74a2-138">Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a74a2-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="a74a2-139">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a74a2-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a74a2-140">Pasirinkite „Speaker2016“ strategiją, kurią ką tik sukūrėte ankstesnėje papildomoje užduotyje.</span><span class="sxs-lookup"><span data-stu-id="a74a2-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  

