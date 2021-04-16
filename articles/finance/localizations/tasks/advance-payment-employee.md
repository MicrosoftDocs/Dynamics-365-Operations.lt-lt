---
title: 'EEU-00047: išankstinis mokėjimas darbuotojui'
description: Šioje procedūroje parodoma, kaip nustatyti ir registruoti išankstinio savininko operacijas.
author: v-oloski
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RCashTable, LedgerJournalSetup, HcmWorkerGroup_RU, EmplPosting_RU, VendParameters, RCashPosting, BankParameters, PaymTerm, HcmWorker, HcmWorkerNewWorker, HcmWorkerAdvHolderTableListPage_RU, HcmWorkerAdvHolderTable_RU, PurchTable, PurchCreateOrder, HcmAdvHolderLookup_RU, InventItemIdLookupPurchase, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, EmplTrans_RU, EmplBalance_RU
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cfdbdf30c9900b792c57a26e4a4d4f4a8830cebc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832541"
---
# <a name="eeu-00047-advance-payment-to-employee"></a><span data-ttu-id="b049c-103">EEU-00047: išankstinis mokėjimas darbuotojui</span><span class="sxs-lookup"><span data-stu-id="b049c-103">EEU-00047 Advance payment to employee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b049c-104">Šioje procedūroje parodoma, kaip nustatyti ir registruoti išankstinio savininko operacijas.</span><span class="sxs-lookup"><span data-stu-id="b049c-104">This procedure demonstrates how to set up and register transactions for an advance holder.</span></span> <span data-ttu-id="b049c-105">Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kurios pirminis adresas yra Lietuvoje.</span><span class="sxs-lookup"><span data-stu-id="b049c-105">This procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="b049c-106">Šią užduotį gali atlikti tik su juridiniais subjektais, kurių pagrindinis adresas yra Lenkijoje, Lietuvoje, Latvijoje, Estijoje, Čekijoje arba Vengrijoje.</span><span class="sxs-lookup"><span data-stu-id="b049c-106">This task only works for legal entities with a primary address in Poland, Lithuania, Latvia, Estonia, Czech Republic, or Hungary.</span></span> <span data-ttu-id="b049c-107">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="b049c-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-cash-account"></a><span data-ttu-id="b049c-108">Naujo kasos kodo kūrimas</span><span class="sxs-lookup"><span data-stu-id="b049c-108">Create a new cash account</span></span>
1. <span data-ttu-id="b049c-109">Pasirinkite Grynųjų pinigų ir banko valdymas > Banko kodai > Kasos kodai.</span><span class="sxs-lookup"><span data-stu-id="b049c-109">Go to Cash and bank management > Bank accounts > Cash accounts.</span></span>
2. <span data-ttu-id="b049c-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b049c-110">Click New.</span></span>
3. <span data-ttu-id="b049c-111">Lauke Grynieji pinigai įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-111">In the Cash field, type a value.</span></span>
4. <span data-ttu-id="b049c-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="b049c-113">Lauke Numeracijos grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="b049c-113">In the Number sequence group field, enter or select a value.</span></span>
6. <span data-ttu-id="b049c-114">Išplėskite skyrių Tikrinimas.</span><span class="sxs-lookup"><span data-stu-id="b049c-114">Expand the Validation section.</span></span>
7. <span data-ttu-id="b049c-115">Lauke Valiuta įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="b049c-115">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="b049c-116">Lauke Neigiami grynieji pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="b049c-116">Select Yes in the Negative cash field.</span></span>
9. <span data-ttu-id="b049c-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b049c-117">Click Save.</span></span>

## <a name="create-a-new-journal"></a><span data-ttu-id="b049c-118">Naujo žurnalo kūrimas</span><span class="sxs-lookup"><span data-stu-id="b049c-118">Create a new journal</span></span>
1. <span data-ttu-id="b049c-119">Pasirinkite Didžioji knyga > Žurnalo nustatymas > Žurnalo pavadinimai.</span><span class="sxs-lookup"><span data-stu-id="b049c-119">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="b049c-120">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b049c-120">Click New.</span></span>
3. <span data-ttu-id="b049c-121">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-121">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b049c-122">Lauke Kvitų serijos įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-122">In the Voucher series field, enter or select a value.</span></span>
5. <span data-ttu-id="b049c-123">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b049c-123">Click Save.</span></span>
6. <span data-ttu-id="b049c-124">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b049c-124">Click New.</span></span>
7. <span data-ttu-id="b049c-125">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-125">In the Name field, type a value.</span></span>
8. <span data-ttu-id="b049c-126">Lauke „Žurnalo tipas“ pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="b049c-126">In the Journal type field, select an option.</span></span>
9. <span data-ttu-id="b049c-127">Lauke Kvitų serijos įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-127">In the Voucher series field, enter or select a value.</span></span>
10. <span data-ttu-id="b049c-128">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b049c-128">Click Save.</span></span>

## <a name="create-an-advance-holder-group"></a><span data-ttu-id="b049c-129">Išankstinių savininkų grupės kūrimas</span><span class="sxs-lookup"><span data-stu-id="b049c-129">Create an advance holder group</span></span>
1. <span data-ttu-id="b049c-130">Pasirinkite Mokėtinos sumos > Nustatymas > Išankstiniai savininkai > Išankstinių savininkų grupės.</span><span class="sxs-lookup"><span data-stu-id="b049c-130">Go to Accounts payable > Setup > Advance holders > Advance holder groups.</span></span>
2. <span data-ttu-id="b049c-131">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b049c-131">Click New.</span></span>
3. <span data-ttu-id="b049c-132">Lauke Grupė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-132">In the Group field, type a value.</span></span>
4. <span data-ttu-id="b049c-133">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b049c-134">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b049c-134">Click Save.</span></span>

## <a name="create-an-employee-posting-profile"></a><span data-ttu-id="b049c-135">Darbuotojų registravimo šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="b049c-135">Create an employee posting profile</span></span>
1. <span data-ttu-id="b049c-136">Pasirinkite Mokėtinos sumos > Nustatymas > Išankstiniai savininkai > Darbuotojų registravimo šablonai.</span><span class="sxs-lookup"><span data-stu-id="b049c-136">Go to Accounts payable > Setup > Advance holders > Employee posting profiles.</span></span>
2. <span data-ttu-id="b049c-137">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b049c-137">Click New.</span></span>
3. <span data-ttu-id="b049c-138">Lauke Registravimo šablonas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-138">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="b049c-139">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-139">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b049c-140">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b049c-140">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="b049c-141">Lauke Galioja pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="b049c-141">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="b049c-142">Lauke Suminė sąskaita nurodykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="b049c-142">In the Summary account field, specify the desired values.</span></span>
8. <span data-ttu-id="b049c-143">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b049c-143">Click Save.</span></span>

## <a name="set-up-advance-holder-parameters"></a><span data-ttu-id="b049c-144">Išankstinio savininko parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="b049c-144">Set up advance holder parameters</span></span>
1. <span data-ttu-id="b049c-145">Pasirinkite Mokėtinos sumos > Sąranka > Mokėtinų sumų parametrai.</span><span class="sxs-lookup"><span data-stu-id="b049c-145">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="b049c-146">Spustelėkite skirtuką Išankstiniai savininkai.</span><span class="sxs-lookup"><span data-stu-id="b049c-146">Click the Advance holders tab.</span></span>
3. <span data-ttu-id="b049c-147">Lauke Registravimo šablonas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-147">In the Posting profile field, enter or select a value.</span></span>
4. <span data-ttu-id="b049c-148">Lauke Pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-148">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="b049c-149">Lauke Grynieji pinigai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-149">In the Cash field, enter or select a value.</span></span>
6. <span data-ttu-id="b049c-150">Lauke Pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-150">In the Name field, enter or select a value.</span></span>
7. <span data-ttu-id="b049c-151">Lauke Sąskaitos tipas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="b049c-151">In the Account type field, select an option.</span></span>
8. <span data-ttu-id="b049c-152">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="b049c-152">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="b049c-153">Spustelėkite skirtuką Numeracijos.</span><span class="sxs-lookup"><span data-stu-id="b049c-153">Click the Number sequences tab.</span></span>
10. <span data-ttu-id="b049c-154">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b049c-154">Click Save.</span></span>

## <a name="set-up-a-cash-posting-profile"></a><span data-ttu-id="b049c-155">Grynųjų registravimo šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="b049c-155">Set up a cash posting profile</span></span>
1. <span data-ttu-id="b049c-156">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų registravimo šablonai.</span><span class="sxs-lookup"><span data-stu-id="b049c-156">Go to Cash and bank management > Setup > Cash posting profiles.</span></span>
2. <span data-ttu-id="b049c-157">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b049c-157">Click New.</span></span>
3. <span data-ttu-id="b049c-158">Lauke Grynųjų registravimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-158">In the Cash posting field, type a value.</span></span>
4. <span data-ttu-id="b049c-159">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b049c-160">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b049c-160">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="b049c-161">Lauke Galioja pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="b049c-161">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="b049c-162">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="b049c-162">In the Main account field, specify the desired values.</span></span>
8. <span data-ttu-id="b049c-163">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b049c-163">Click Save.</span></span>

## <a name="set-up-cash-and-bank-parameters"></a><span data-ttu-id="b049c-164">Grynųjų pinigų ir banko parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="b049c-164">Set up cash and bank parameters</span></span>
1. <span data-ttu-id="b049c-165">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų ir banko valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="b049c-165">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="b049c-166">Spustelėkite skirtuką Grynieji pinigai.</span><span class="sxs-lookup"><span data-stu-id="b049c-166">Click the Cash tab.</span></span>
3. <span data-ttu-id="b049c-167">Lauke Grynieji pinigai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-167">In the Cash field, enter or select a value.</span></span>
4. <span data-ttu-id="b049c-168">Lauke Grynųjų registravimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-168">In the Cash posting field, enter or select a value.</span></span>
5. <span data-ttu-id="b049c-169">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b049c-169">Click Save.</span></span>
6. <span data-ttu-id="b049c-170">Spustelėkite skirtuką Numeracijos.</span><span class="sxs-lookup"><span data-stu-id="b049c-170">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="b049c-171">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b049c-171">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="b049c-172">Lauke Numeracijos kodas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="b049c-172">In the Number sequence code field, enter or select a value.</span></span>
9. <span data-ttu-id="b049c-173">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b049c-173">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="b049c-174">Lauke Numeracijos kodas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="b049c-174">In the Number sequence code field, enter or select a value.</span></span>
11. <span data-ttu-id="b049c-175">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b049c-175">Click Save.</span></span>

## <a name="set-up-terms-of-payment"></a><span data-ttu-id="b049c-176">Nustatyti mokėjimo sąlygas</span><span class="sxs-lookup"><span data-stu-id="b049c-176">Set up terms of payment</span></span>
1. <span data-ttu-id="b049c-177">Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo sąlygos.</span><span class="sxs-lookup"><span data-stu-id="b049c-177">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="b049c-178">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="b049c-178">Click Edit.</span></span>
3. <span data-ttu-id="b049c-179">Lauke Iš išankstinio savininko pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="b049c-179">Select Yes in the From advance holder field.</span></span>
4. <span data-ttu-id="b049c-180">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b049c-180">Click Save.</span></span>

## <a name="create-a-new-worker"></a><span data-ttu-id="b049c-181">Naujo darbuotojo kūrimas</span><span class="sxs-lookup"><span data-stu-id="b049c-181">Create a new worker</span></span>
1. <span data-ttu-id="b049c-182">Pasirinkite Personalas > Darbuotojai > Darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="b049c-182">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="b049c-183">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b049c-183">Click New.</span></span>
3. <span data-ttu-id="b049c-184">Lauke Vardas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-184">In the First name field, type a value.</span></span>
4. <span data-ttu-id="b049c-185">Lauke Pavardė surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-185">In the Last name field, type a value.</span></span>
5. <span data-ttu-id="b049c-186">Lauke Darbuotojo ID įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-186">In the Worker ID field, type a value.</span></span>
6. <span data-ttu-id="b049c-187">Spustelėkite Samdyti naują darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="b049c-187">Click Hire new worker.</span></span>
7. <span data-ttu-id="b049c-188">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b049c-188">Click Save.</span></span>

## <a name="set-up-a-worker-as-an-advance-holder"></a><span data-ttu-id="b049c-189">Darbuotojo kaip išankstinio savininko nustatymas</span><span class="sxs-lookup"><span data-stu-id="b049c-189">Set up a worker as an advance holder</span></span>
1. <span data-ttu-id="b049c-190">Pasirinkite Mokėtinos sumos > Nustatymas > Išankstiniai savininkai.</span><span class="sxs-lookup"><span data-stu-id="b049c-190">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="b049c-191">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="b049c-191">Click Edit.</span></span>
3. <span data-ttu-id="b049c-192">Lauke Grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-192">In the Group field, enter or select a value.</span></span>
4. <span data-ttu-id="b049c-193">Lauke Išankstinis savininkas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="b049c-193">Select Yes in the Advance holder field.</span></span>
5. <span data-ttu-id="b049c-194">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b049c-194">Click Save.</span></span>

## <a name="create-and-post-a-purchase-order-invoice"></a><span data-ttu-id="b049c-195">Pirkimo užsakymo SF kūrimas ir registravimas</span><span class="sxs-lookup"><span data-stu-id="b049c-195">Create and post a purchase order invoice</span></span>
1. <span data-ttu-id="b049c-196">Eikite į Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="b049c-196">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="b049c-197">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b049c-197">Click New.</span></span>
3. <span data-ttu-id="b049c-198">Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="b049c-198">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="b049c-199">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="b049c-199">Click OK.</span></span>
5. <span data-ttu-id="b049c-200">Lauke Eilutės arba antraštė pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="b049c-200">In the Lines or header field, select an option.</span></span>
6. <span data-ttu-id="b049c-201">Išplėskite skyrių Kaina ir nuolaida.</span><span class="sxs-lookup"><span data-stu-id="b049c-201">Expand the Price and discount section.</span></span>
7. <span data-ttu-id="b049c-202">Lauke Mokėjimo sąlygos įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-202">In the Terms of payment field, enter or select a value.</span></span>
8. <span data-ttu-id="b049c-203">Lauke Išankstinis savininkas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-203">In the Advance holder field, enter or select a value.</span></span>
9. <span data-ttu-id="b049c-204">Lauke Eilutės arba antraštė pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="b049c-204">In the Lines or header field, select an option.</span></span>
10. <span data-ttu-id="b049c-205">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b049c-205">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="b049c-206">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-206">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="b049c-207">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b049c-207">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="b049c-208">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b049c-208">In the Unit price field, enter a number.</span></span>
14. <span data-ttu-id="b049c-209">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b049c-209">Click Save.</span></span>
15. <span data-ttu-id="b049c-210">Veiksmų srityje spustelėkite Pirkti.</span><span class="sxs-lookup"><span data-stu-id="b049c-210">On the Action Pane, click Purchase.</span></span>
16. <span data-ttu-id="b049c-211">Spustelėkite Patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="b049c-211">Click Confirm.</span></span>
17. <span data-ttu-id="b049c-212">Veiksmų srityje spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="b049c-212">On the Action Pane, click Invoice.</span></span>
18. <span data-ttu-id="b049c-213">Spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="b049c-213">Click Invoice.</span></span>
19. <span data-ttu-id="b049c-214">Spustelėkite Numatyt. iš: gavimo dokumento kiekio, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="b049c-214">Click Default from: Product receipt quantity to open the drop dialog.</span></span>
20. <span data-ttu-id="b049c-215">Lauke Numatytasis eilučių kiekis pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="b049c-215">In the Default quantity for lines field, select an option.</span></span>
21. <span data-ttu-id="b049c-216">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="b049c-216">Click OK.</span></span>
22. <span data-ttu-id="b049c-217">Lauke Numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-217">In the Number field, type a value.</span></span>
23. <span data-ttu-id="b049c-218">Lauke Sąskaitos faktūros aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b049c-218">In the Invoice description field, type a value.</span></span>
24. <span data-ttu-id="b049c-219">Lauke SF data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="b049c-219">In the Invoice date field, enter a date.</span></span>
25. <span data-ttu-id="b049c-220">Lauke PVM registro data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="b049c-220">In the Date of VAT register field, enter a date.</span></span>
26. <span data-ttu-id="b049c-221">Lauke Gavimo dokumento data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="b049c-221">In the Receive document date field, enter a date.</span></span>
27. <span data-ttu-id="b049c-222">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="b049c-222">Click Post.</span></span>

## <a name="balance-and-close-advance-holders-transactions"></a><span data-ttu-id="b049c-223">Išankstinių savininkų operacijų balansavimas ir uždarymas</span><span class="sxs-lookup"><span data-stu-id="b049c-223">Balance and close advance holders transactions</span></span>
1. <span data-ttu-id="b049c-224">Pasirinkite Mokėtinos sumos > Nustatymas > Išankstiniai savininkai.</span><span class="sxs-lookup"><span data-stu-id="b049c-224">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="b049c-225">Spustelėkite Operacijos.</span><span class="sxs-lookup"><span data-stu-id="b049c-225">Click Transactions.</span></span>
3. <span data-ttu-id="b049c-226">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b049c-226">Close the page.</span></span>
4. <span data-ttu-id="b049c-227">Spustelėkite Balansas.</span><span class="sxs-lookup"><span data-stu-id="b049c-227">Click Balance.</span></span>
5. <span data-ttu-id="b049c-228">Spustelėkite Uždaryti per banką.</span><span class="sxs-lookup"><span data-stu-id="b049c-228">Click Close via bank.</span></span>
6. <span data-ttu-id="b049c-229">Lauke Automatinis pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="b049c-229">Select Yes in the Automatic field.</span></span>
7. <span data-ttu-id="b049c-230">Lauke Suma, skirta perkelti</span><span class="sxs-lookup"><span data-stu-id="b049c-230">In the Amount to be transferred.</span></span> <span data-ttu-id="b049c-231">įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b049c-231">field, enter a number.</span></span>
8. <span data-ttu-id="b049c-232">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b049c-232">Click OK.</span></span>
9. <span data-ttu-id="b049c-233">Spustelėkite Uždaryti per kasą.</span><span class="sxs-lookup"><span data-stu-id="b049c-233">Click Close via cash.</span></span>
10. <span data-ttu-id="b049c-234">Lauke Automatinis pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="b049c-234">Select Yes in the Automatic field.</span></span>
11. <span data-ttu-id="b049c-235">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b049c-235">Click OK.</span></span>
12. <span data-ttu-id="b049c-236">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b049c-236">Close the page.</span></span>
13. <span data-ttu-id="b049c-237">Spustelėkite Operacijos.</span><span class="sxs-lookup"><span data-stu-id="b049c-237">Click Transactions.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]