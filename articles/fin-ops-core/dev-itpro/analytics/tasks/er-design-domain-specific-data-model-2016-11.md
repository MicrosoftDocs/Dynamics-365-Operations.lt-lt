---
title: ER konkretaus domeno duomenų modelio kūrimas
description: Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti naują elektroninių ataskaitų (ER) konfigūraciją, apimančią elektroninio mokėjimo dokumentų duomenų modelį.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d66cc69da08478ceb931fab594da51bafcacc38
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185088"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="ae78d-103">ER konkretaus domeno duomenų modelio kūrimas</span><span class="sxs-lookup"><span data-stu-id="ae78d-103">ER Design domain specific data model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ae78d-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti naują elektroninių ataskaitų (ER) konfigūraciją, apimančią elektroninio mokėjimo dokumentų duomenų modelį.</span><span class="sxs-lookup"><span data-stu-id="ae78d-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="ae78d-105">Šis duomenų modelis vėliau bus naudojamas kaip duomenų šaltinis, kai kursite mokėjimo dokumentų formatą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="ae78d-106">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijas visos įmonės naudoja bendrai.</span><span class="sxs-lookup"><span data-stu-id="ae78d-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="ae78d-107">Norėdami atlikti šiuos veiksmus, pirmiausia turite juos užbaigti procedūroje „Sukurti konfigūracijos teikėją ir pažymėti jį kaip aktyvų“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="ae78d-108">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="ae78d-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="ae78d-109">Pasirinkite pavyzdinės įmonės „Litware, Inc.‟ konfigūracijų teikėją.</span><span class="sxs-lookup"><span data-stu-id="ae78d-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="ae78d-110">Jei nematote šio konfigūracijų teikėjo, pirmiausia turite atlikti procedūros „Konfigūracijų teikėjo sukūrimas ir jo pažymėjimas kaip aktyvaus" veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ae78d-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="ae78d-111">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="ae78d-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="ae78d-112">Sukursite konfigūraciją, apimančią elektroninio mokėjimo dokumentų duomenų modelį.</span><span class="sxs-lookup"><span data-stu-id="ae78d-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="ae78d-113">Šis duomenų modelis bus vėliau naudojamas kaip duomenų šaltinis, kai kursite mokėjimo dokumentų formatą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="ae78d-114">Sukurti naują duomenų modelio konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="ae78d-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="ae78d-115">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="ae78d-116">Lauke „Pavadinimas“ įveskite „Mokėjimai (supaprastas modelis)“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="ae78d-117">Mokėjimai (supaprastintas modelis)</span><span class="sxs-lookup"><span data-stu-id="ae78d-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="ae78d-118">Lauke „Aprašas“ įveskite „Mokėjimo modelio konfigūracija“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="ae78d-119">Mokėjimo modelio konfigūracija</span><span class="sxs-lookup"><span data-stu-id="ae78d-119">Payment model configuration</span></span>  
    * <span data-ttu-id="ae78d-120">Čia automatiškai įvedamas aktyvios konfigūracijos teikėjas.</span><span class="sxs-lookup"><span data-stu-id="ae78d-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="ae78d-121">Šis teikėjas galės prižiūrėti šią konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="ae78d-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="ae78d-122">Kiti teikėjai šią konfigūraciją galės naudoti, bet negalės jos prižiūrėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="ae78d-123">Spustelėkite mygtuką „Kurti konfigūraciją“, kad užbaigtumėte konfigūracijos kūrimo užduotį</span><span class="sxs-lookup"><span data-stu-id="ae78d-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="ae78d-124">Sukurti duomenų modelį</span><span class="sxs-lookup"><span data-stu-id="ae78d-124">Create a data model</span></span>
    * <span data-ttu-id="ae78d-125">Kuriate naują pasirinktos konfigūracijos duomenų modelį.</span><span class="sxs-lookup"><span data-stu-id="ae78d-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="ae78d-126">Šios konfigūracijos versijos būsena bus „Juodraštis“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="ae78d-127">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="ae78d-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="ae78d-128">Nurodyti mokėjimo procese dalyvaujančios šalies struktūrą</span><span class="sxs-lookup"><span data-stu-id="ae78d-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="ae78d-129">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="ae78d-130">Lauke „Pavadinimas” įveskite „Šalis”.</span><span class="sxs-lookup"><span data-stu-id="ae78d-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="ae78d-131">Įrašas</span><span class="sxs-lookup"><span data-stu-id="ae78d-131">Party</span></span>  
3. <span data-ttu-id="ae78d-132">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-132">Click Add.</span></span>
4. <span data-ttu-id="ae78d-133">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="ae78d-134">Lauke „Pavadinimas“ įveskite „Agentas“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="ae78d-135">Vardas</span><span class="sxs-lookup"><span data-stu-id="ae78d-135">Name</span></span>  
6. <span data-ttu-id="ae78d-136">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="ae78d-137">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-137">Click Add.</span></span>
8. <span data-ttu-id="ae78d-138">Lauke „Rasti” įveskite „Šalis”.</span><span class="sxs-lookup"><span data-stu-id="ae78d-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="ae78d-139">Įrašas</span><span class="sxs-lookup"><span data-stu-id="ae78d-139">Party</span></span>  
9. <span data-ttu-id="ae78d-140">Spustelėkite Rasti ankstesnį.</span><span class="sxs-lookup"><span data-stu-id="ae78d-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="ae78d-141">Nurodyti šio modelio banko struktūrą</span><span class="sxs-lookup"><span data-stu-id="ae78d-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="ae78d-142">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="ae78d-143">Lauke „Pavadinimas“ įveskite „Agentas“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="ae78d-144">Agentas</span><span class="sxs-lookup"><span data-stu-id="ae78d-144">Agent</span></span>  
3. <span data-ttu-id="ae78d-145">Lauke „Prekės tipas“ pasirinkite „Įrašas“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="ae78d-146">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-146">Click Add.</span></span>
5. <span data-ttu-id="ae78d-147">Lauke „Aprašas“ įveskite „Šalies (skolininko / kreditoriaus) sąskaitą prižiūrinti finansų įstaiga (pvz., bankas)“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="ae78d-148">Šalies (skolininko / kreditoriaus) sąskaitą prižiūrinti finansų įstaiga (pvz., bankas).</span><span class="sxs-lookup"><span data-stu-id="ae78d-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="ae78d-149">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="ae78d-150">Lauke „Pavadinimas“ įveskite „Agentas“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="ae78d-151">Vardas</span><span class="sxs-lookup"><span data-stu-id="ae78d-151">Name</span></span>  
8. <span data-ttu-id="ae78d-152">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="ae78d-153">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-153">Click Add.</span></span>
10. <span data-ttu-id="ae78d-154">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="ae78d-155">Lauke „Pavadinimas“ įveskite „SWIFT“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="ae78d-156">SWIFT</span><span class="sxs-lookup"><span data-stu-id="ae78d-156">SWIFT</span></span>  
12. <span data-ttu-id="ae78d-157">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-157">Click Add.</span></span>
13. <span data-ttu-id="ae78d-158">Lauke „Aprašas” įveskite „Banko identifikavimo kodas”.</span><span class="sxs-lookup"><span data-stu-id="ae78d-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="ae78d-159">Banko identifikavimo kodas</span><span class="sxs-lookup"><span data-stu-id="ae78d-159">Bank identification code</span></span>  
14. <span data-ttu-id="ae78d-160">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="ae78d-161">Lauke „Pavadinimas“ įveskite „RoutingNumber“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="ae78d-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="ae78d-162">RoutingNumber</span></span>  
16. <span data-ttu-id="ae78d-163">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-163">Click Add.</span></span>
17. <span data-ttu-id="ae78d-164">Lauke „Aprašas” įveskite „Banko kodas”.</span><span class="sxs-lookup"><span data-stu-id="ae78d-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="ae78d-165">Įmonės kodas</span><span class="sxs-lookup"><span data-stu-id="ae78d-165">Routing number</span></span>  
18. <span data-ttu-id="ae78d-166">Spustelėkite Rasti ankstesnį.</span><span class="sxs-lookup"><span data-stu-id="ae78d-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="ae78d-167">Nurodyti šio modelio banko sąskaitos struktūrą</span><span class="sxs-lookup"><span data-stu-id="ae78d-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="ae78d-168">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="ae78d-169">Lauke „Pavadinimas“ įveskite „Sąskaita“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="ae78d-170">Paskyra</span><span class="sxs-lookup"><span data-stu-id="ae78d-170">Account</span></span>  
3. <span data-ttu-id="ae78d-171">Lauke „Prekės tipas“ pasirinkite „Įrašas“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="ae78d-172">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-172">Click Add.</span></span>
5. <span data-ttu-id="ae78d-173">Lauke „Aprašas” įveskite „Šalies sąskaitos finansų įstaigoje (pvz., banke) identifikavimas”.</span><span class="sxs-lookup"><span data-stu-id="ae78d-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="ae78d-174">Šalies sąskaitos finansų įstaigoje (pvz., banke) identifikavimas.</span><span class="sxs-lookup"><span data-stu-id="ae78d-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="ae78d-175">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="ae78d-176">Lauke „Pavadinimas“ suveskite „Valiuta“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="ae78d-177">Valiuta</span><span class="sxs-lookup"><span data-stu-id="ae78d-177">Currency</span></span>  
8. <span data-ttu-id="ae78d-178">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="ae78d-179">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-179">Click Add.</span></span>
10. <span data-ttu-id="ae78d-180">Lauke „Aprašas” įveskite „Valiutos kodas”.</span><span class="sxs-lookup"><span data-stu-id="ae78d-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="ae78d-181">Valiutos kodas</span><span class="sxs-lookup"><span data-stu-id="ae78d-181">Currency code</span></span>  
11. <span data-ttu-id="ae78d-182">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="ae78d-183">Lauke „Pavadinimas“ įveskite „Numeris“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="ae78d-184">Skaičius</span><span class="sxs-lookup"><span data-stu-id="ae78d-184">Number</span></span>  
13. <span data-ttu-id="ae78d-185">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-185">Click Add.</span></span>
14. <span data-ttu-id="ae78d-186">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="ae78d-187">Lauke „Pavadinimas“, įveskite „IBAN“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="ae78d-188">IBAN</span><span class="sxs-lookup"><span data-stu-id="ae78d-188">IBAN</span></span>  
16. <span data-ttu-id="ae78d-189">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-189">Click Add.</span></span>
17. <span data-ttu-id="ae78d-190">Lauke „Aprašas” įveskite „Tarptautinės banko sąskaitos numeris”.</span><span class="sxs-lookup"><span data-stu-id="ae78d-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="ae78d-191">Tarptautinės banko sąskaitos numeris</span><span class="sxs-lookup"><span data-stu-id="ae78d-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="ae78d-192">Nurodyti kredito pervedimo mokėjimo tipo pranešimo struktūrą</span><span class="sxs-lookup"><span data-stu-id="ae78d-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="ae78d-193">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="ae78d-194">Lauke „Naujas mazgas kaip” įveskite „Modelio šaknis”.</span><span class="sxs-lookup"><span data-stu-id="ae78d-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="ae78d-195">Lauke „Pavadinimas“, įveskite „CustomerCreditTransferInitiation“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="ae78d-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="ae78d-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="ae78d-197">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-197">Click Add.</span></span>
5. <span data-ttu-id="ae78d-198">Lauke „Rasti“, įveskite „CustomerCreditTransferInitiation“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="ae78d-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="ae78d-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="ae78d-200">Spustelėkite Rasti ankstesnį.</span><span class="sxs-lookup"><span data-stu-id="ae78d-200">Click Find previous.</span></span>
7. <span data-ttu-id="ae78d-201">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="ae78d-202">Lauke „Pavadinimas“, įveskite „MessageIdentification“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="ae78d-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="ae78d-203">MessageIdentification</span></span>  
9. <span data-ttu-id="ae78d-204">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-204">Click Add.</span></span>
10. <span data-ttu-id="ae78d-205">Lauke „Aprašas“ įveskite „Tiesioginė nuoroda, kurią priskyrė nurodančioji šalis (ir išsiuntė kitai šaliai), kad būtų galima identifikuoti pranešimą“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="ae78d-206">Tiesioginė nuoroda, kurią priskyrė nurodančioji šalis (ir išsiuntė kitai šaliai), kad būtų galima identifikuoti pranešimą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="ae78d-207">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="ae78d-208">Lauke „Pavadinimas“, įveskite „ProcessingDateTime“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="ae78d-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="ae78d-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="ae78d-210">Lauke „Prekės tipas“ pasirinkite „DateTime“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="ae78d-211">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-211">Click Add.</span></span>
15. <span data-ttu-id="ae78d-212">Lauke „Aprašas“ įveskite „Mokėjimo pranešimo sukūrimo data ir laikas“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="ae78d-213">Mokėjimo pranešimo sukūrimo data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="ae78d-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="ae78d-214">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="ae78d-215">Nurodyti šio modelio mokėjimo operacijos struktūrą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="ae78d-216">Lauke „Pavadinimas“, įveskite „Mokėjimai“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="ae78d-217">Mokėjimai</span><span class="sxs-lookup"><span data-stu-id="ae78d-217">Payments</span></span>  
18. <span data-ttu-id="ae78d-218">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="ae78d-219">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-219">Click Add.</span></span>
20. <span data-ttu-id="ae78d-220">Lauke „Aprašas“ įveskite „Dabartinio pranešimo mokėjimo eilutės“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="ae78d-221">Dabartinio pranešimo mokėjimo eilutės</span><span class="sxs-lookup"><span data-stu-id="ae78d-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="ae78d-222">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="ae78d-223">Lauke „Pavadinimas“, įveskite „Kreditorius“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="ae78d-224">Gavėjas</span><span class="sxs-lookup"><span data-stu-id="ae78d-224">Creditor</span></span>  
23. <span data-ttu-id="ae78d-225">Lauke „Prekės tipas“ pasirinkite „Įrašas“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="ae78d-226">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-226">Click Add.</span></span>
25. <span data-ttu-id="ae78d-227">Lauke „Aprašas“ įveskite „Šalis, kuriai reikia sumokėti tam tikrą pinigų sumą“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="ae78d-228">Šalis, kuriai reikia sumokėti tam tikrą pinigų sumą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="ae78d-229">Spustelėkite Perjungti elemento nuorodą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="ae78d-230">Lauke „Rasti” įveskite „Šalis”.</span><span class="sxs-lookup"><span data-stu-id="ae78d-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="ae78d-231">Įrašas</span><span class="sxs-lookup"><span data-stu-id="ae78d-231">Party</span></span>  
28. <span data-ttu-id="ae78d-232">Spustelėkite Rasti kitą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-232">Click Find next.</span></span>
29. <span data-ttu-id="ae78d-233">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ae78d-233">Click OK.</span></span>
30. <span data-ttu-id="ae78d-234">Lauke „Rasti“ įveskite „Mokėjimai“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="ae78d-235">Mokėjimai</span><span class="sxs-lookup"><span data-stu-id="ae78d-235">Payments</span></span>  
31. <span data-ttu-id="ae78d-236">Spustelėkite Rasti kitą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-236">Click Find next.</span></span>
32. <span data-ttu-id="ae78d-237">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="ae78d-238">Lauke „Pavadinimas“, įveskite „Skolininkas“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="ae78d-239">Debitorius</span><span class="sxs-lookup"><span data-stu-id="ae78d-239">Debtor</span></span>  
34. <span data-ttu-id="ae78d-240">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-240">Click Add.</span></span>
35. <span data-ttu-id="ae78d-241">Lauke „Aprašas“ įveskite „Šalis, kuri (galutiniam) kreditoriui skolinga tam tikrą pinigų sumą“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="ae78d-242">Šalis, kuri (galutiniam) kreditoriui skolinga tam tikrą pinigų sumą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="ae78d-243">Spustelėkite Perjungti elemento nuorodą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="ae78d-244">Lauke „Rasti” įveskite „Šalis”.</span><span class="sxs-lookup"><span data-stu-id="ae78d-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="ae78d-245">Įrašas</span><span class="sxs-lookup"><span data-stu-id="ae78d-245">Party</span></span>  
38. <span data-ttu-id="ae78d-246">Spustelėkite Rasti kitą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-246">Click Find next.</span></span>
39. <span data-ttu-id="ae78d-247">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ae78d-247">Click OK.</span></span>
40. <span data-ttu-id="ae78d-248">Spustelėkite Rasti kitą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-248">Click Find next.</span></span>
41. <span data-ttu-id="ae78d-249">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="ae78d-250">Lauke „Pavadinimas“, įveskite „Aprašas“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="ae78d-251">aprašymas</span><span class="sxs-lookup"><span data-stu-id="ae78d-251">Description</span></span>  
43. <span data-ttu-id="ae78d-252">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="ae78d-253">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-253">Click Add.</span></span>
45. <span data-ttu-id="ae78d-254">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="ae78d-255">Lauke „Pavadinimas“ suveskite „Valiuta“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="ae78d-256">Valiuta</span><span class="sxs-lookup"><span data-stu-id="ae78d-256">Currency</span></span>  
47. <span data-ttu-id="ae78d-257">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-257">Click Add.</span></span>
48. <span data-ttu-id="ae78d-258">Lauke „Aprašas” įveskite „Valiutos kodas”.</span><span class="sxs-lookup"><span data-stu-id="ae78d-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="ae78d-259">Valiutos kodas</span><span class="sxs-lookup"><span data-stu-id="ae78d-259">Currency code</span></span>  
49. <span data-ttu-id="ae78d-260">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="ae78d-261">Lauke „Pavadinimas“, įveskite „TransactionDate“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="ae78d-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="ae78d-262">TransactionDate</span></span>  
51. <span data-ttu-id="ae78d-263">Lauke „Prekės tipas“ pasirinkite „Data“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="ae78d-264">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-264">Click Add.</span></span>
53. <span data-ttu-id="ae78d-265">Lauke „Aprašas” įveskite „Operacijos data”.</span><span class="sxs-lookup"><span data-stu-id="ae78d-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="ae78d-266">Operacijos data</span><span class="sxs-lookup"><span data-stu-id="ae78d-266">Transaction date</span></span>  
54. <span data-ttu-id="ae78d-267">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="ae78d-268">Lauke „Pavadinimas“, įveskite „InstructedAmount“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="ae78d-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="ae78d-269">InstructedAmount</span></span>  
56. <span data-ttu-id="ae78d-270">Lauke „Prekės tipas“ pasirinkite „Realusis skaičius“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="ae78d-271">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-271">Click Add.</span></span>
58. <span data-ttu-id="ae78d-272">Lauke „Aprašas“ įveskite „Pinigų suma, kurią, prieš atskaitant mokesčius, skolininkas turi perduoti kreditoriui”.</span><span class="sxs-lookup"><span data-stu-id="ae78d-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="ae78d-273">Suma turėtų būti išreikšta inicijuojančios šalies nurodyta valiuta“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="ae78d-274">Pinigų suma, kurią, prieš atskaitant mokesčius, skolininkas turi perduoti kreditoriui.</span><span class="sxs-lookup"><span data-stu-id="ae78d-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="ae78d-275">Suma turėtų būti išreikšta inicijuojančios šalies nurodyta valiuta.</span><span class="sxs-lookup"><span data-stu-id="ae78d-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="ae78d-276">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae78d-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="ae78d-277">Lauke „Pavadinimas“, įveskite „End2EndID“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="ae78d-278">„End2EndID“</span><span class="sxs-lookup"><span data-stu-id="ae78d-278">End2EndID</span></span>  
61. <span data-ttu-id="ae78d-279">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="ae78d-280">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-280">Click Add.</span></span>
63. <span data-ttu-id="ae78d-281">Lauke „Aprašas“ įveskite „Unikali inicijuojančios šalies priskirta identifikacija”.</span><span class="sxs-lookup"><span data-stu-id="ae78d-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="ae78d-282">Ši identifikacija perduodama per visą tiesioginę grandinę ir lieka nepakeista“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="ae78d-283">Unikali inicijuojančios šalies priskirta identifikacija.</span><span class="sxs-lookup"><span data-stu-id="ae78d-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="ae78d-284">Ši identifikacija perduodama per visą tiesioginę grandinę ir lieka nepakeista.</span><span class="sxs-lookup"><span data-stu-id="ae78d-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="ae78d-285">Lauke „Pavadinimas“ įveskite „PaymentModel“.</span><span class="sxs-lookup"><span data-stu-id="ae78d-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="ae78d-286">Pavadinimas „PaymentModel“ sutampa su iš anksto nustatytomis mokėjimo formų sąsajomis.</span><span class="sxs-lookup"><span data-stu-id="ae78d-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="ae78d-287">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ae78d-287">Click Save.</span></span>
66. <span data-ttu-id="ae78d-288">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ae78d-288">Close the page.</span></span>

