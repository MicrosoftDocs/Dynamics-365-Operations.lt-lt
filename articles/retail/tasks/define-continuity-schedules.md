--- 
title: " Nustatyti tęstinumo grafikus"
description: "Šioje temoje parodoma, kaip nustatyti tęstinumo programą (dar vadinamą pasikartojančiais užsakymais)."
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
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 5ac333989dd987fd3cb1d2b2769fbcdb93bdb4bd
ms.contentlocale: lt-lt
ms.lasthandoff: 02/07/2018

---
# <a name="define-continuity-schedules"></a><span data-ttu-id="6fe1a-103"> Nustatyti tęstinumo grafikus</span><span class="sxs-lookup"><span data-stu-id="6fe1a-103">Define continuity schedules</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="6fe1a-104">Šioje temoje parodoma, kaip nustatyti tęstinumo programą (dar vadinamą pasikartojančiais užsakymais).</span><span class="sxs-lookup"><span data-stu-id="6fe1a-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="6fe1a-105">Šioje temoje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="6fe1a-106">Tęstinumo programos kūrimas</span><span class="sxs-lookup"><span data-stu-id="6fe1a-106">Create continuity program</span></span>
1. <span data-ttu-id="6fe1a-107">Pasirinkite Mažmeninė prekyba ir prekyba > Tęstinumas > Tęstinumo programos.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-107">Go to Retail and commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="6fe1a-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-108">Click New.</span></span>
3. <span data-ttu-id="6fe1a-109">Lauke Grafiko ID įveskite tęstinumo grafiko ID.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="6fe1a-110">Lauke Užsakymo pradžia pasirinkite Pirmasis įvykis.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="6fe1a-111">Jei klientas pateikia naują užsakymą tęstinumo programai, yra dvi parinktys, kuris produktas bus siunčiamas: 1.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="6fe1a-112">Pirmas įvykis: bus siunčiamas pirmas tęstinumo programos produktas.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="6fe1a-113">2.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-113">2.</span></span> <span data-ttu-id="6fe1a-114">Dabartinis įvykis: bus siunčiamas pirmasis tęstinumo programos produktas.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="6fe1a-115">2) Dabartinis įvykis: bus siunčiamas dabartinis produktas.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-115">For example.</span></span> <span data-ttu-id="6fe1a-116">Pavyzdys: praėjus trims mėnesiams nuo programos pradžios, klientas gaus trečiąjį programos produktą.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="6fe1a-117">Pasirinkite Taip, norite paraginti nurodyti užsakymo pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="6fe1a-118">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-118">Click Add line.</span></span>
7. <span data-ttu-id="6fe1a-119">Lauke Prekės numeris įveskite pirmojo produkto (0013) prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="6fe1a-120">Įveskite CP.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-120">Type 'CP'.</span></span>
9. <span data-ttu-id="6fe1a-121">Įveskite datą, kada pirmąjį produktą bus galima užsisakyti.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="6fe1a-122">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-122">Click Add line.</span></span>
11. <span data-ttu-id="6fe1a-123">Lauke Prekės numeris įveskite „0014“.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="6fe1a-124">Išvalykite lauko Datų intervalo kodas reikšmę, kad jis būtų tuščias.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="6fe1a-125">Atlikdami šią procedūrą, išvalykite datų intervalą.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="6fe1a-126">Galite nustatyti, kad datos reikšmė didėtų skaičiuojant nuo pirmosios prekės pradžios datos.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="6fe1a-127">Čia galite įvesti intervalą, kuriuo siunčiami produktai.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="6fe1a-128">Įveskite 30.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-128">Type '30'.</span></span>
    * <span data-ttu-id="6fe1a-129">Jei programa trunka mėnesį, įveskite 30 dienų intervalą.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="6fe1a-130">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-130">Click Add line.</span></span>
15. <span data-ttu-id="6fe1a-131">Lauke Prekės numeris įveskite „0015“.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="6fe1a-132">Įveskite Baigti.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-132">Type 'End'.</span></span>
17. <span data-ttu-id="6fe1a-133">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="6fe1a-134">Tęstinumo prekės priskyrimas</span><span class="sxs-lookup"><span data-stu-id="6fe1a-134">Assign to continuity item</span></span>
1. <span data-ttu-id="6fe1a-135">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="6fe1a-136">Pasirinkite prekę 0016.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-136">Select item '0016'.</span></span>
    * <span data-ttu-id="6fe1a-137">Atlikdami šią procedūrą, pasirinkite prekės numerį 0016.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="6fe1a-138">Įprastai jūs sukursite patvirtintą produktą, kuriam taikoma papildoma tęstinumo verslo logika, kai jis pateikiamas skambučių centro pardavimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="6fe1a-139">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6fe1a-140">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-140">Click Edit.</span></span>
5. <span data-ttu-id="6fe1a-141">Išplėskite arba sutraukite skyrių Parduoti.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="6fe1a-142">Čia galite įvesti tęstinumo programą, kurią ši prekė nurodo.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="6fe1a-143">Įveskite tvarkaraščio ID, kurį sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="6fe1a-144">Kai ši prekė parduodama skambučių centre, taikoma papildoma verslo logika iš pasirinktos tęstinumo programos.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="6fe1a-145">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-145">Click Save.</span></span>


