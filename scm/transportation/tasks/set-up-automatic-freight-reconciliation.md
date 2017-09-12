--- 
title: Automatinio transportavimo derinimo nustatymas
description: "Šioje procedūroje parodoma, kaip nustatyti automatinio transportavimo derinimo duomenis."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 97f0c4d8fe06ab2fc252b9543cb688306214c79f
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-automatic-freight-reconciliation"></a><span data-ttu-id="f78e9-103">Automatinio transportavimo derinimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="f78e9-103">Set up automatic freight reconciliation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f78e9-104">Šioje procedūroje parodoma, kaip nustatyti automatinio transportavimo derinimo duomenis.</span><span class="sxs-lookup"><span data-stu-id="f78e9-104">This procedure shows how to set up data for automatic freight reconciliation.</span></span> <span data-ttu-id="f78e9-105">Tai paprastai atlieka sandėlio vadovas.</span><span class="sxs-lookup"><span data-stu-id="f78e9-105">This is typically done by a warehouse manager.</span></span> <span data-ttu-id="f78e9-106">Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="f78e9-106">You can use this procedure in demo data company USMF.</span></span>


## <a name="set-up-the-freight-bill-type"></a><span data-ttu-id="f78e9-107">Transportavimo sąskaitos tipo nustatymas</span><span class="sxs-lookup"><span data-stu-id="f78e9-107">Set up the freight bill type</span></span>
1. <span data-ttu-id="f78e9-108">Eikite į Transportavimo valdymas > Sąranka > Transportavimo mokesčių derinimas > Transportavimo sąskaitos tipas.</span><span class="sxs-lookup"><span data-stu-id="f78e9-108">Go to Transportation management > Setup > Freight reconciliation > Freight bill type.</span></span>
    * <span data-ttu-id="f78e9-109">Transportavimo sąskaitos tipas apibrėžia, kaip transportavimo sąskaita ir vežėjo SF turi būti derinamos.</span><span class="sxs-lookup"><span data-stu-id="f78e9-109">The freight bill type defines how freight bills and carrier invoices  should be matched.</span></span>  
2. <span data-ttu-id="f78e9-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f78e9-110">Click New.</span></span>
3. <span data-ttu-id="f78e9-111">Lauke Transportavimo sąskaitos tipas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f78e9-111">In the Freight bill type field, type a value.</span></span>
4. <span data-ttu-id="f78e9-112">Lauke Mechanizmo rinkinys įveskite Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer.</span><span class="sxs-lookup"><span data-stu-id="f78e9-112">In the Engine assembly field, type 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span></span>
    * <span data-ttu-id="f78e9-113">Tai yra standartinė transportavimo valdymo gretinimo mechanizmo kodų biblioteka.</span><span class="sxs-lookup"><span data-stu-id="f78e9-113">This is the standard Transportation management matching engine code library.</span></span>  
5. <span data-ttu-id="f78e9-114">Lauke Mechanizmo klasė įveskite Microsoft.Dynamics.Ax.Tms.dll.</span><span class="sxs-lookup"><span data-stu-id="f78e9-114">In the Engine class field, type 'Microsoft.Dynamics.Ax.Tms.dll'.</span></span>
    * <span data-ttu-id="f78e9-115">Tai yra standartinė transportavimo valdymo gretinimo mechanizmo klasė.</span><span class="sxs-lookup"><span data-stu-id="f78e9-115">This is the standard Transportation management matching engine class.</span></span>  
6. <span data-ttu-id="f78e9-116">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f78e9-116">Click New.</span></span>
7. <span data-ttu-id="f78e9-117">Lauke Aprašas pasirinkite reikšmę, kuri turėtų atitikti transportavimo sąskaitos ir vežėjo SF reikšmes.</span><span class="sxs-lookup"><span data-stu-id="f78e9-117">In the Description field, choose the value that should match on the freight bill and the carrier invoice.</span></span>  
8. <span data-ttu-id="f78e9-118">Lauke Būtina gretinti pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="f78e9-118">In the Match required field, select 'Yes'.</span></span>
    * <span data-ttu-id="f78e9-119">Jei nustatote šio lauko reikšmę Taip, lauke Aprašas pasirinkta reikšmė turi sutapti tiek transportavimo sąskaitoje, tiek vežėjo SF.</span><span class="sxs-lookup"><span data-stu-id="f78e9-119">If you set this field to Yes this means that the value selected in the Description field needs to match on both the freight bill and the carrier invoice.</span></span> <span data-ttu-id="f78e9-120">Jei nustatysite parinktį Ne, vienoje iš šių sąskaitų laukas gali būti tuščias.</span><span class="sxs-lookup"><span data-stu-id="f78e9-120">If you set it to No, the field can be blank on one of these.</span></span>  
9. <span data-ttu-id="f78e9-121">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f78e9-121">Click Save.</span></span>

## <a name="set-up-the-freight-bill-type-assignment"></a><span data-ttu-id="f78e9-122">Transportavimo sąskaitos tipo priskyrimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="f78e9-122">Set up the freight bill type assignment</span></span>
1. <span data-ttu-id="f78e9-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f78e9-123">Close the page.</span></span>
2. <span data-ttu-id="f78e9-124">Eikite į Transportavimo valdymas > Sąranka > Transportavimo mokesčių derinimas > Transportavimo sąskaitos tipo priskyrimai.</span><span class="sxs-lookup"><span data-stu-id="f78e9-124">Go to Transportation management > Setup > Freight reconciliation > Freight bill type assignments.</span></span>
    * <span data-ttu-id="f78e9-125">Transportavimo sąskaitos tipo priskyrimas naudojamas norint nurodyti, kuris transportavimo sąskaitos tipas naudojamas konkrečiam vežėjui.</span><span class="sxs-lookup"><span data-stu-id="f78e9-125">The freight bill type assignment is used to specify which freight bill type is used for a particular carrier.</span></span>   
3. <span data-ttu-id="f78e9-126">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f78e9-126">Click New.</span></span>
4. <span data-ttu-id="f78e9-127">Lauke Režimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f78e9-127">In the Mode field, enter or select a value.</span></span>
5. <span data-ttu-id="f78e9-128">Lauke Siuntos vežėjas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f78e9-128">In the Shipping carrier field, enter or select a value.</span></span>
6. <span data-ttu-id="f78e9-129">Lauke Transportavimo sąskaitos tipas pasirinkite transportavimo sąskaitos tipą, kurį sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="f78e9-129">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
7. <span data-ttu-id="f78e9-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f78e9-130">Close the page.</span></span>

## <a name="set-up-the-audit-master"></a><span data-ttu-id="f78e9-131">Pagrindinio audito nustatymas</span><span class="sxs-lookup"><span data-stu-id="f78e9-131">Set up the audit master</span></span>
1. <span data-ttu-id="f78e9-132">Eikite į Transportavimo valdymas > Sąranka > Transportavimo mokesčių derinimas > Pagrindinis auditas.</span><span class="sxs-lookup"><span data-stu-id="f78e9-132">Go to Transportation management > Setup > Freight reconciliation > Audit master.</span></span>
    * <span data-ttu-id="f78e9-133">Pagrindinis auditas nurodo automatinio transportavimo derinimo nuokrypio ribas.</span><span class="sxs-lookup"><span data-stu-id="f78e9-133">The audit master defines the tolerance limits for automatic freight reconciliation.</span></span> <span data-ttu-id="f78e9-134">Jis nurodo sumą, kuria transportavimo sąskaitos ir vežėjo SF piniginės sumos gali skirtis, kad vis tiek būtų galima derinti.</span><span class="sxs-lookup"><span data-stu-id="f78e9-134">It specifies by how much the monetary amounts on the freight bill and the carrier invoice can differ and still allow reconciliation to occur.</span></span> <span data-ttu-id="f78e9-135">Jis taip pat apibrėžia, kaip tvarkyti nesutapimus.</span><span class="sxs-lookup"><span data-stu-id="f78e9-135">It also defines how to handle discrepancies.</span></span>  
2. <span data-ttu-id="f78e9-136">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f78e9-136">Click New.</span></span>
3. <span data-ttu-id="f78e9-137">Lauke Pagrindinio audito ID įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f78e9-137">In the Audit master ID field, type a value.</span></span>
4. <span data-ttu-id="f78e9-138">Lauke Siuntos vežėjas pasirinkite tą patį siuntos vežėją, kurį pasirinkote anksčiau.</span><span class="sxs-lookup"><span data-stu-id="f78e9-138">In the Shipping carrier  field, select the same shipping carrier as you did earlier.</span></span>
5. <span data-ttu-id="f78e9-139">Lauke Transportavimo sąskaitos tipas pasirinkite transportavimo sąskaitos tipą, kurį sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="f78e9-139">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
6. <span data-ttu-id="f78e9-140">Išplėskite Nuokrypis skyrių.</span><span class="sxs-lookup"><span data-stu-id="f78e9-140">Expand the Tolerance section.</span></span>
7. <span data-ttu-id="f78e9-141">Lauke Mažiausias leistinas nuokrypio lygis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="f78e9-141">In the Minimum tolerance level field, enter a number.</span></span>
8. <span data-ttu-id="f78e9-142">Lauke Didžiausias leistinas nuokrypio lygis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="f78e9-142">In the Maximum tolerance level field, enter a number.</span></span>
9. <span data-ttu-id="f78e9-143">Išplėskite skyrių Rezultatas.</span><span class="sxs-lookup"><span data-stu-id="f78e9-143">Expand the Result section.</span></span>
10. <span data-ttu-id="f78e9-144">Lauke Permokėjimo priežasties įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f78e9-144">In the Overpayment reason code field, enter or select a value.</span></span>
    * <span data-ttu-id="f78e9-145">Jei piniginė suma transportavimo sąskaitoje ir vežėjo SF skiriasi, permokėjimo ir neprimokėjimo priežasties kodai nurodo sąskaitas, kuriose skirtumas turi būti užregistruotas, jei skirtumas neviršija leistinų lygių.</span><span class="sxs-lookup"><span data-stu-id="f78e9-145">If the monetary amounts differ on the freight bill and the carrier invoice, the overpayment and underpayment reason codes specify the accounts that the difference should be registered on, as long as the difference is within the tolerance levels.</span></span>  
11. <span data-ttu-id="f78e9-146">Lauke Neprimokėjimo priežasties įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f78e9-146">In the Underpayment reason code field, enter or select a value.</span></span>
12. <span data-ttu-id="f78e9-147">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f78e9-147">Close the page.</span></span>


