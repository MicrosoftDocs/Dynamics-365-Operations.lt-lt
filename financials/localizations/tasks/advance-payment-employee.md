--- 
title: "Išankstinis mokėjimas darbuotojui (Rytų Europa)"
description: "Šioje procedūroje parodoma, kaip nustatyti ir registruoti išankstinio savininko operacijas."
author: v-oloski
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4cc3ba589204f87b844ab4302e03105d2aa1de8d
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="advance-payment-to-an-employee-eastern-europe"></a><span data-ttu-id="084a7-103">Išankstinis mokėjimas darbuotojui (Rytų Europa)</span><span class="sxs-lookup"><span data-stu-id="084a7-103">Advance payment to an employee (Eastern Europe)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="084a7-104">Šioje procedūroje parodoma, kaip nustatyti ir registruoti išankstinio savininko operacijas.</span><span class="sxs-lookup"><span data-stu-id="084a7-104">This procedure demonstrates how to set up and register transactions for an advance holder.</span></span> <span data-ttu-id="084a7-105">Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kurios pirminis adresas yra Lietuvoje.</span><span class="sxs-lookup"><span data-stu-id="084a7-105">This procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="084a7-106">Šią užduotį gali atlikti tik su juridiniais subjektais, kurių pagrindinis adresas yra Lenkijoje, Lietuvoje, Latvijoje, Estijoje, Čekijoje arba Vengrijoje.</span><span class="sxs-lookup"><span data-stu-id="084a7-106">This task only works for legal entities with a primary address in Poland, Lithuania, Latvia, Estonia, Czech Republic, or Hungary.</span></span> <span data-ttu-id="084a7-107">Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="084a7-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-cash-account"></a><span data-ttu-id="084a7-108">Naujo kasos kodo kūrimas</span><span class="sxs-lookup"><span data-stu-id="084a7-108">Create a new cash account</span></span>
1. <span data-ttu-id="084a7-109">Pasirinkite Grynųjų pinigų ir banko valdymas > Banko kodai > Kasos kodai.</span><span class="sxs-lookup"><span data-stu-id="084a7-109">Go to Cash and bank management > Bank accounts > Cash accounts.</span></span>
2. <span data-ttu-id="084a7-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="084a7-110">Click New.</span></span>
3. <span data-ttu-id="084a7-111">Lauke Grynieji pinigai įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-111">In the Cash field, type a value.</span></span>
4. <span data-ttu-id="084a7-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="084a7-113">Lauke Numeracijos grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="084a7-113">In the Number sequence group field, enter or select a value.</span></span>
6. <span data-ttu-id="084a7-114">Išplėskite skyrių Tikrinimas.</span><span class="sxs-lookup"><span data-stu-id="084a7-114">Expand the Validation section.</span></span>
7. <span data-ttu-id="084a7-115">Lauke Valiuta įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="084a7-115">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="084a7-116">Lauke Neigiami grynieji pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="084a7-116">Select Yes in the Negative cash field.</span></span>
9. <span data-ttu-id="084a7-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="084a7-117">Click Save.</span></span>

## <a name="create-a-new-journal"></a><span data-ttu-id="084a7-118">Naujo žurnalo kūrimas</span><span class="sxs-lookup"><span data-stu-id="084a7-118">Create a new journal</span></span>
1. <span data-ttu-id="084a7-119">Pasirinkite Didžioji knyga > Žurnalo nustatymas > Žurnalo pavadinimai.</span><span class="sxs-lookup"><span data-stu-id="084a7-119">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="084a7-120">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="084a7-120">Click New.</span></span>
3. <span data-ttu-id="084a7-121">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-121">In the Name field, type a value.</span></span>
4. <span data-ttu-id="084a7-122">Lauke Kvitų serijos įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-122">In the Voucher series field, enter or select a value.</span></span>
5. <span data-ttu-id="084a7-123">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="084a7-123">Click Save.</span></span>
6. <span data-ttu-id="084a7-124">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="084a7-124">Click New.</span></span>
7. <span data-ttu-id="084a7-125">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-125">In the Name field, type a value.</span></span>
8. <span data-ttu-id="084a7-126">Lauke „Žurnalo tipas“ pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="084a7-126">In the Journal type field, select an option.</span></span>
9. <span data-ttu-id="084a7-127">Lauke Kvitų serijos įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-127">In the Voucher series field, enter or select a value.</span></span>
10. <span data-ttu-id="084a7-128">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="084a7-128">Click Save.</span></span>

## <a name="create-an-advance-holder-group"></a><span data-ttu-id="084a7-129">Išankstinių savininkų grupės kūrimas</span><span class="sxs-lookup"><span data-stu-id="084a7-129">Create an advance holder group</span></span>
1. <span data-ttu-id="084a7-130">Pasirinkite Mokėtinos sumos > Nustatymas > Išankstiniai savininkai > Išankstinių savininkų grupės.</span><span class="sxs-lookup"><span data-stu-id="084a7-130">Go to Accounts payable > Setup > Advance holders > Advance holder groups.</span></span>
2. <span data-ttu-id="084a7-131">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="084a7-131">Click New.</span></span>
3. <span data-ttu-id="084a7-132">Lauke Grupė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-132">In the Group field, type a value.</span></span>
4. <span data-ttu-id="084a7-133">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="084a7-134">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="084a7-134">Click Save.</span></span>

## <a name="create-an-employee-posting-profile"></a><span data-ttu-id="084a7-135">Darbuotojų registravimo šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="084a7-135">Create an employee posting profile</span></span>
1. <span data-ttu-id="084a7-136">Pasirinkite Mokėtinos sumos > Nustatymas > Išankstiniai savininkai > Darbuotojų registravimo šablonai.</span><span class="sxs-lookup"><span data-stu-id="084a7-136">Go to Accounts payable > Setup > Advance holders > Employee posting profiles.</span></span>
2. <span data-ttu-id="084a7-137">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="084a7-137">Click New.</span></span>
3. <span data-ttu-id="084a7-138">Lauke Registravimo šablonas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-138">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="084a7-139">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-139">In the Description field, type a value.</span></span>
5. <span data-ttu-id="084a7-140">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="084a7-140">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="084a7-141">Lauke Galioja pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="084a7-141">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="084a7-142">Lauke Suminė sąskaita nurodykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="084a7-142">In the Summary account field, specify the desired values.</span></span>
8. <span data-ttu-id="084a7-143">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="084a7-143">Click Save.</span></span>

## <a name="set-up-advance-holder-parameters"></a><span data-ttu-id="084a7-144">Išankstinio savininko parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="084a7-144">Set up advance holder parameters</span></span>
1. <span data-ttu-id="084a7-145">Pasirinkite Mokėtinos sumos > Sąranka > Mokėtinų sumų parametrai.</span><span class="sxs-lookup"><span data-stu-id="084a7-145">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="084a7-146">Spustelėkite skirtuką Išankstiniai savininkai.</span><span class="sxs-lookup"><span data-stu-id="084a7-146">Click the Advance holders tab.</span></span>
3. <span data-ttu-id="084a7-147">Lauke Registravimo šablonas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-147">In the Posting profile field, enter or select a value.</span></span>
4. <span data-ttu-id="084a7-148">Lauke Pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-148">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="084a7-149">Lauke Grynieji pinigai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-149">In the Cash field, enter or select a value.</span></span>
6. <span data-ttu-id="084a7-150">Lauke Pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-150">In the Name field, enter or select a value.</span></span>
7. <span data-ttu-id="084a7-151">Lauke Sąskaitos tipas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="084a7-151">In the Account type field, select an option.</span></span>
8. <span data-ttu-id="084a7-152">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="084a7-152">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="084a7-153">Spustelėkite skirtuką Numeracijos.</span><span class="sxs-lookup"><span data-stu-id="084a7-153">Click the Number sequences tab.</span></span>
10. <span data-ttu-id="084a7-154">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="084a7-154">Click Save.</span></span>

## <a name="set-up-a-cash-posting-profile"></a><span data-ttu-id="084a7-155">Grynųjų registravimo šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="084a7-155">Set up a cash posting profile</span></span>
1. <span data-ttu-id="084a7-156">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų registravimo šablonai.</span><span class="sxs-lookup"><span data-stu-id="084a7-156">Go to Cash and bank management > Setup > Cash posting profiles.</span></span>
2. <span data-ttu-id="084a7-157">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="084a7-157">Click New.</span></span>
3. <span data-ttu-id="084a7-158">Lauke Grynųjų registravimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-158">In the Cash posting field, type a value.</span></span>
4. <span data-ttu-id="084a7-159">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="084a7-160">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="084a7-160">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="084a7-161">Lauke Galioja pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="084a7-161">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="084a7-162">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="084a7-162">In the Main account field, specify the desired values.</span></span>
8. <span data-ttu-id="084a7-163">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="084a7-163">Click Save.</span></span>

## <a name="set-up-cash-and-bank-parameters"></a><span data-ttu-id="084a7-164">Grynųjų pinigų ir banko parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="084a7-164">Set up cash and bank parameters</span></span>
1. <span data-ttu-id="084a7-165">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų ir banko valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="084a7-165">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="084a7-166">Spustelėkite skirtuką Grynieji pinigai.</span><span class="sxs-lookup"><span data-stu-id="084a7-166">Click the Cash tab.</span></span>
3. <span data-ttu-id="084a7-167">Lauke Grynieji pinigai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-167">In the Cash field, enter or select a value.</span></span>
4. <span data-ttu-id="084a7-168">Lauke Grynųjų registravimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-168">In the Cash posting field, enter or select a value.</span></span>
5. <span data-ttu-id="084a7-169">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="084a7-169">Click Save.</span></span>
6. <span data-ttu-id="084a7-170">Spustelėkite skirtuką Numeracijos.</span><span class="sxs-lookup"><span data-stu-id="084a7-170">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="084a7-171">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="084a7-171">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="084a7-172">Lauke Numeracijos kodas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="084a7-172">In the Number sequence code field, enter or select a value.</span></span>
9. <span data-ttu-id="084a7-173">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="084a7-173">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="084a7-174">Lauke Numeracijos kodas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="084a7-174">In the Number sequence code field, enter or select a value.</span></span>
11. <span data-ttu-id="084a7-175">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="084a7-175">Click Save.</span></span>

## <a name="set-up-terms-of-payment"></a><span data-ttu-id="084a7-176">Nustatyti mokėjimo sąlygas</span><span class="sxs-lookup"><span data-stu-id="084a7-176">Set up terms of payment</span></span>
1. <span data-ttu-id="084a7-177">Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo sąlygos.</span><span class="sxs-lookup"><span data-stu-id="084a7-177">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="084a7-178">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="084a7-178">Click Edit.</span></span>
3. <span data-ttu-id="084a7-179">Lauke Iš išankstinio savininko pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="084a7-179">Select Yes in the From advance holder field.</span></span>
4. <span data-ttu-id="084a7-180">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="084a7-180">Click Save.</span></span>

## <a name="create-a-new-worker"></a><span data-ttu-id="084a7-181">Naujo darbuotojo kūrimas</span><span class="sxs-lookup"><span data-stu-id="084a7-181">Create a new worker</span></span>
1. <span data-ttu-id="084a7-182">Pasirinkite Personalas > Darbuotojai > Darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="084a7-182">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="084a7-183">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="084a7-183">Click New.</span></span>
3. <span data-ttu-id="084a7-184">Lauke Vardas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-184">In the First name field, type a value.</span></span>
4. <span data-ttu-id="084a7-185">Lauke Pavardė surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-185">In the Last name field, type a value.</span></span>
5. <span data-ttu-id="084a7-186">Lauke Darbuotojo ID įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-186">In the Worker ID field, type a value.</span></span>
6. <span data-ttu-id="084a7-187">Spustelėkite Samdyti naują darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="084a7-187">Click Hire new worker.</span></span>
7. <span data-ttu-id="084a7-188">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="084a7-188">Click Save.</span></span>

## <a name="set-up-a-worker-as-an-advance-holder"></a><span data-ttu-id="084a7-189">Darbuotojo kaip išankstinio savininko nustatymas</span><span class="sxs-lookup"><span data-stu-id="084a7-189">Set up a worker as an advance holder</span></span>
1. <span data-ttu-id="084a7-190">Pasirinkite Mokėtinos sumos > Nustatymas > Išankstiniai savininkai.</span><span class="sxs-lookup"><span data-stu-id="084a7-190">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="084a7-191">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="084a7-191">Click Edit.</span></span>
3. <span data-ttu-id="084a7-192">Lauke Grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-192">In the Group field, enter or select a value.</span></span>
4. <span data-ttu-id="084a7-193">Lauke Išankstinis savininkas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="084a7-193">Select Yes in the Advance holder field.</span></span>
5. <span data-ttu-id="084a7-194">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="084a7-194">Click Save.</span></span>

## <a name="create-and-post-a-purchase-order-invoice"></a><span data-ttu-id="084a7-195">Pirkimo užsakymo SF kūrimas ir registravimas</span><span class="sxs-lookup"><span data-stu-id="084a7-195">Create and post a purchase order invoice</span></span>
1. <span data-ttu-id="084a7-196">Eikite į Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="084a7-196">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="084a7-197">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="084a7-197">Click New.</span></span>
3. <span data-ttu-id="084a7-198">Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="084a7-198">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="084a7-199">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="084a7-199">Click OK.</span></span>
5. <span data-ttu-id="084a7-200">Lauke Eilutės arba antraštė pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="084a7-200">In the Lines or header field, select an option.</span></span>
6. <span data-ttu-id="084a7-201">Išplėskite skyrių Kaina ir nuolaida.</span><span class="sxs-lookup"><span data-stu-id="084a7-201">Expand the Price and discount section.</span></span>
7. <span data-ttu-id="084a7-202">Lauke Mokėjimo sąlygos įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-202">In the Terms of payment field, enter or select a value.</span></span>
8. <span data-ttu-id="084a7-203">Lauke Išankstinis savininkas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-203">In the Advance holder field, enter or select a value.</span></span>
9. <span data-ttu-id="084a7-204">Lauke Eilutės arba antraštė pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="084a7-204">In the Lines or header field, select an option.</span></span>
10. <span data-ttu-id="084a7-205">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="084a7-205">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="084a7-206">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-206">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="084a7-207">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="084a7-207">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="084a7-208">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="084a7-208">In the Unit price field, enter a number.</span></span>
14. <span data-ttu-id="084a7-209">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="084a7-209">Click Save.</span></span>
15. <span data-ttu-id="084a7-210">Veiksmų srityje spustelėkite Pirkti.</span><span class="sxs-lookup"><span data-stu-id="084a7-210">On the Action Pane, click Purchase.</span></span>
16. <span data-ttu-id="084a7-211">Spustelėkite Patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="084a7-211">Click Confirm.</span></span>
17. <span data-ttu-id="084a7-212">Veiksmų srityje spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="084a7-212">On the Action Pane, click Invoice.</span></span>
18. <span data-ttu-id="084a7-213">Spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="084a7-213">Click Invoice.</span></span>
19. <span data-ttu-id="084a7-214">Spustelėkite Numatyt. iš: gavimo dokumento kiekio, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="084a7-214">Click Default from: Product receipt quantity to open the drop dialog.</span></span>
20. <span data-ttu-id="084a7-215">Lauke Numatytasis eilučių kiekis pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="084a7-215">In the Default quantity for lines field, select an option.</span></span>
21. <span data-ttu-id="084a7-216">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="084a7-216">Click OK.</span></span>
22. <span data-ttu-id="084a7-217">Lauke Numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-217">In the Number field, type a value.</span></span>
23. <span data-ttu-id="084a7-218">Lauke Sąskaitos faktūros aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="084a7-218">In the Invoice description field, type a value.</span></span>
24. <span data-ttu-id="084a7-219">Lauke SF data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="084a7-219">In the Invoice date field, enter a date.</span></span>
25. <span data-ttu-id="084a7-220">Lauke PVM registro data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="084a7-220">In the Date of VAT register field, enter a date.</span></span>
26. <span data-ttu-id="084a7-221">Lauke Gavimo dokumento data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="084a7-221">In the Receive document date field, enter a date.</span></span>
27. <span data-ttu-id="084a7-222">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="084a7-222">Click Post.</span></span>

## <a name="balance-and-close-advance-holders-transactions"></a><span data-ttu-id="084a7-223">Išankstinių savininkų operacijų balansavimas ir uždarymas</span><span class="sxs-lookup"><span data-stu-id="084a7-223">Balance and close advance holders transactions</span></span>
1. <span data-ttu-id="084a7-224">Pasirinkite Mokėtinos sumos > Nustatymas > Išankstiniai savininkai.</span><span class="sxs-lookup"><span data-stu-id="084a7-224">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="084a7-225">Spustelėkite Operacijos.</span><span class="sxs-lookup"><span data-stu-id="084a7-225">Click Transactions.</span></span>
3. <span data-ttu-id="084a7-226">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="084a7-226">Close the page.</span></span>
4. <span data-ttu-id="084a7-227">Spustelėkite Balansas.</span><span class="sxs-lookup"><span data-stu-id="084a7-227">Click Balance.</span></span>
5. <span data-ttu-id="084a7-228">Spustelėkite Uždaryti per banką.</span><span class="sxs-lookup"><span data-stu-id="084a7-228">Click Close via bank.</span></span>
6. <span data-ttu-id="084a7-229">Lauke Automatinis pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="084a7-229">Select Yes in the Automatic field.</span></span>
7. <span data-ttu-id="084a7-230">Lauke Suma, skirta perkelti</span><span class="sxs-lookup"><span data-stu-id="084a7-230">In the Amount to be transferred.</span></span> <span data-ttu-id="084a7-231">įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="084a7-231">field, enter a number.</span></span>
8. <span data-ttu-id="084a7-232">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="084a7-232">Click OK.</span></span>
9. <span data-ttu-id="084a7-233">Spustelėkite Uždaryti per kasą.</span><span class="sxs-lookup"><span data-stu-id="084a7-233">Click Close via cash.</span></span>
10. <span data-ttu-id="084a7-234">Lauke Automatinis pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="084a7-234">Select Yes in the Automatic field.</span></span>
11. <span data-ttu-id="084a7-235">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="084a7-235">Click OK.</span></span>
12. <span data-ttu-id="084a7-236">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="084a7-236">Close the page.</span></span>
13. <span data-ttu-id="084a7-237">Spustelėkite Operacijos.</span><span class="sxs-lookup"><span data-stu-id="084a7-237">Click Transactions.</span></span>


