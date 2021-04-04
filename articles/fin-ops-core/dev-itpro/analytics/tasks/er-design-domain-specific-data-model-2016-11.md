---
title: ER konkretaus domeno duomenų modelio kūrimas
description: Šioje temoje aprašoma, kaip sukurti naują elektroninių ataskaitų (ER) konfigūraciją, kurioje būtų elektroninių mokėjimo dokumentų duomenų modelis.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 284fad8b6646c35217789cc9936cbe9fe75a03d0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567814"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="6fd0e-103">ER konkretaus domeno duomenų modelio kūrimas</span><span class="sxs-lookup"><span data-stu-id="6fd0e-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6fd0e-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti naują elektroninių ataskaitų (ER) konfigūraciją, apimančią elektroninio mokėjimo dokumentų duomenų modelį.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="6fd0e-105">Šis duomenų modelis vėliau bus naudojamas kaip duomenų šaltinis, kai kursite mokėjimo dokumentų formatą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="6fd0e-106">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijas visos įmonės naudoja bendrai.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="6fd0e-107">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="6fd0e-108">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="6fd0e-109">Pasirinkite pavyzdinės įmonės „Litware, Inc.‟ konfigūracijų teikėją</span><span class="sxs-lookup"><span data-stu-id="6fd0e-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="6fd0e-110">Jei nematote šio konfigūracijos teikėjo, pirmiausia turite atlikti procedūros „Konfigūracijos teikėjo sukūrimas ir pažymėjimas aktyviu” veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="6fd0e-111">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="6fd0e-112">Sukursite konfigūraciją, apimančią elektroninio mokėjimo dokumentų duomenų modelį.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="6fd0e-113">Šis duomenų modelis bus vėliau naudojamas kaip duomenų šaltinis, kai kursite mokėjimo dokumentų formatą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="6fd0e-114">Sukurti naują duomenų modelio konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="6fd0e-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="6fd0e-115">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="6fd0e-116">Lauke „Pavadinimas“ įveskite „Mokėjimai (supaprastas modelis)“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="6fd0e-117">Lauke „Aprašas“ įveskite „Mokėjimo modelio konfigūracija“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="6fd0e-118">Čia automatiškai įvedamas aktyvios konfigūracijos teikėjas.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="6fd0e-119">Šis teikėjas galės prižiūrėti šią konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="6fd0e-120">Kiti teikėjai šią konfigūraciją galės naudoti, bet negalės jos prižiūrėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="6fd0e-121">Spustelėkite mygtuką „Kurti konfigūraciją“, kad užbaigtumėte konfigūracijos kūrimo užduotį</span><span class="sxs-lookup"><span data-stu-id="6fd0e-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="6fd0e-122">Sukurti duomenų modelį</span><span class="sxs-lookup"><span data-stu-id="6fd0e-122">Create a data model</span></span>
<span data-ttu-id="6fd0e-123">Kuriate naują pasirinktos konfigūracijos duomenų modelį.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="6fd0e-124">Šios konfigūracijos versijos būsena bus „Juodraštis“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="6fd0e-125">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="6fd0e-126">Nurodyti mokėjimo procese dalyvaujančios šalies struktūrą</span><span class="sxs-lookup"><span data-stu-id="6fd0e-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="6fd0e-127">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="6fd0e-128">Lauke „Pavadinimas” įveskite „Šalis”.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="6fd0e-129">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-129">Click Add.</span></span>
4. <span data-ttu-id="6fd0e-130">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="6fd0e-131">Lauke „Pavadinimas“ įveskite „Agentas“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="6fd0e-132">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="6fd0e-133">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-133">Click Add.</span></span>
8. <span data-ttu-id="6fd0e-134">Lauke „Rasti” įveskite „Šalis”.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="6fd0e-135">Spustelėkite Rasti ankstesnį.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="6fd0e-136">Nurodyti šio modelio banko struktūrą</span><span class="sxs-lookup"><span data-stu-id="6fd0e-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="6fd0e-137">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="6fd0e-138">Lauke „Pavadinimas“ įveskite „Agentas“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="6fd0e-139">Lauke „Prekės tipas“ pasirinkite „Įrašas“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="6fd0e-140">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-140">Click Add.</span></span>
5. <span data-ttu-id="6fd0e-141">Lauke „Aprašas“ įveskite „Šalies (skolininko / kreditoriaus) sąskaitą prižiūrinti finansų įstaiga (pvz., bankas)“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="6fd0e-142">Šalies (skolininko / kreditoriaus) sąskaitą prižiūrinti finansų įstaiga (pvz., bankas).</span><span class="sxs-lookup"><span data-stu-id="6fd0e-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="6fd0e-143">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="6fd0e-144">Lauke „Pavadinimas“ įveskite „Agentas“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="6fd0e-145">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="6fd0e-146">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-146">Click Add.</span></span>
10. <span data-ttu-id="6fd0e-147">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="6fd0e-148">Lauke „Pavadinimas“ įveskite „SWIFT“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="6fd0e-149">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-149">Click Add.</span></span>
13. <span data-ttu-id="6fd0e-150">Lauke „Aprašas” įveskite „Banko identifikavimo kodas”.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="6fd0e-151">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="6fd0e-152">Lauke „Pavadinimas“ įveskite „RoutingNumber“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="6fd0e-153">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-153">Click Add.</span></span>
17. <span data-ttu-id="6fd0e-154">Lauke „Aprašas” įveskite „Banko kodas”.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="6fd0e-155">Spustelėkite Rasti ankstesnį.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="6fd0e-156">Nurodyti šio modelio banko sąskaitos struktūrą</span><span class="sxs-lookup"><span data-stu-id="6fd0e-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="6fd0e-157">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="6fd0e-158">Lauke „Pavadinimas“ įveskite „Sąskaita“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="6fd0e-159">Lauke „Prekės tipas“ pasirinkite „Įrašas“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="6fd0e-160">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-160">Click Add.</span></span>
5. <span data-ttu-id="6fd0e-161">Lauke „Aprašas” įveskite „Šalies sąskaitos finansų įstaigoje (pvz., banke) identifikavimas”.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="6fd0e-162">Šalies sąskaitos finansų įstaigoje (pvz., banke) identifikavimas.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="6fd0e-163">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="6fd0e-164">Lauke „Pavadinimas“ suveskite „Valiuta“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="6fd0e-165">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="6fd0e-166">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-166">Click Add.</span></span>
10. <span data-ttu-id="6fd0e-167">Lauke „Aprašas” įveskite „Valiutos kodas”.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="6fd0e-168">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="6fd0e-169">Lauke „Pavadinimas“ įveskite „Numeris“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="6fd0e-170">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-170">Click Add.</span></span>
14. <span data-ttu-id="6fd0e-171">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="6fd0e-172">Lauke „Pavadinimas“, įveskite „IBAN“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="6fd0e-173">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-173">Click Add.</span></span>
17. <span data-ttu-id="6fd0e-174">Lauke „Aprašas” įveskite „Tarptautinės banko sąskaitos numeris”.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="6fd0e-175">Nurodyti kredito pervedimo mokėjimo tipo pranešimo struktūrą</span><span class="sxs-lookup"><span data-stu-id="6fd0e-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="6fd0e-176">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="6fd0e-177">Lauke „Naujas mazgas kaip” įveskite „Modelio šaknis”.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="6fd0e-178">Lauke „Pavadinimas“, įveskite „CustomerCreditTransferInitiation“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="6fd0e-179">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-179">Click Add.</span></span>
5. <span data-ttu-id="6fd0e-180">Lauke „Rasti“, įveskite „CustomerCreditTransferInitiation“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="6fd0e-181">Spustelėkite Rasti ankstesnį.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-181">Click Find previous.</span></span>
7. <span data-ttu-id="6fd0e-182">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="6fd0e-183">Lauke „Pavadinimas“, įveskite „MessageIdentification“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="6fd0e-184">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-184">Click Add.</span></span>
10. <span data-ttu-id="6fd0e-185">Lauke „Aprašas“ įveskite „Tiesioginė nuoroda, kurią priskyrė nurodančioji šalis (ir išsiuntė kitai šaliai), kad būtų galima identifikuoti pranešimą“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="6fd0e-186">Tiesioginė nuoroda, kurią priskyrė nurodančioji šalis (ir išsiuntė kitai šaliai), kad būtų galima identifikuoti pranešimą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="6fd0e-187">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="6fd0e-188">Lauke „Pavadinimas“, įveskite „ProcessingDateTime“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="6fd0e-189">Lauke „Prekės tipas“ pasirinkite „DateTime“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="6fd0e-190">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-190">Click Add.</span></span>
15. <span data-ttu-id="6fd0e-191">Lauke „Aprašas“ įveskite „Mokėjimo pranešimo sukūrimo data ir laikas“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="6fd0e-192">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="6fd0e-193">Nurodyti šio modelio mokėjimo operacijos struktūrą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="6fd0e-194">Lauke „Pavadinimas“, įveskite „Mokėjimai“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="6fd0e-195">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="6fd0e-196">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-196">Click Add.</span></span>
20. <span data-ttu-id="6fd0e-197">Lauke „Aprašas“ įveskite „Dabartinio pranešimo mokėjimo eilutės“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="6fd0e-198">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="6fd0e-199">Lauke „Pavadinimas“, įveskite „Kreditorius“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="6fd0e-200">Lauke „Prekės tipas“ pasirinkite „Įrašas“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="6fd0e-201">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-201">Click Add.</span></span>
25. <span data-ttu-id="6fd0e-202">Lauke „Aprašas“ įveskite „Šalis, kuriai reikia sumokėti tam tikrą pinigų sumą“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="6fd0e-203">Spustelėkite Perjungti elemento nuorodą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="6fd0e-204">Lauke „Rasti” įveskite „Šalis”.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="6fd0e-205">Spustelėkite Rasti kitą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-205">Click Find next.</span></span>
29. <span data-ttu-id="6fd0e-206">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-206">Click OK.</span></span>
30. <span data-ttu-id="6fd0e-207">Lauke „Rasti“ įveskite „Mokėjimai“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="6fd0e-208">Spustelėkite Rasti kitą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-208">Click Find next.</span></span>
32. <span data-ttu-id="6fd0e-209">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="6fd0e-210">Lauke „Pavadinimas“, įveskite „Skolininkas“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="6fd0e-211">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-211">Click Add.</span></span>
35. <span data-ttu-id="6fd0e-212">Lauke „Aprašas“ įveskite „Šalis, kuri (galutiniam) kreditoriui skolinga tam tikrą pinigų sumą“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="6fd0e-213">Spustelėkite Perjungti elemento nuorodą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="6fd0e-214">Lauke „Rasti” įveskite „Šalis”.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="6fd0e-215">Spustelėkite Rasti kitą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-215">Click Find next.</span></span>
39. <span data-ttu-id="6fd0e-216">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-216">Click OK.</span></span>
40. <span data-ttu-id="6fd0e-217">Spustelėkite Rasti kitą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-217">Click Find next.</span></span>
41. <span data-ttu-id="6fd0e-218">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="6fd0e-219">Lauke „Pavadinimas“, įveskite „Aprašas“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="6fd0e-220">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="6fd0e-221">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-221">Click Add.</span></span>
45. <span data-ttu-id="6fd0e-222">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="6fd0e-223">Lauke „Pavadinimas“ suveskite „Valiuta“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="6fd0e-224">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-224">Click Add.</span></span>
48. <span data-ttu-id="6fd0e-225">Lauke „Aprašas” įveskite „Valiutos kodas”.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="6fd0e-226">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="6fd0e-227">Lauke „Pavadinimas“, įveskite „TransactionDate“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="6fd0e-228">Lauke „Prekės tipas“ pasirinkite „Data“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="6fd0e-229">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-229">Click Add.</span></span>
53. <span data-ttu-id="6fd0e-230">Lauke „Aprašas” įveskite „Operacijos data”.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="6fd0e-231">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="6fd0e-232">Lauke „Pavadinimas“, įveskite „InstructedAmount“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="6fd0e-233">Lauke „Prekės tipas“ pasirinkite „Realusis skaičius“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="6fd0e-234">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-234">Click Add.</span></span>
58. <span data-ttu-id="6fd0e-235">Lauke „Aprašas“ įveskite „Pinigų suma, kurią, prieš atskaitant mokesčius, skolininkas turi perduoti kreditoriui”.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="6fd0e-236">Suma turėtų būti išreikšta inicijuojančios šalies nurodyta valiuta“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="6fd0e-237">Pinigų suma, kurią, prieš atskaitant mokesčius, skolininkas turi perduoti kreditoriui.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="6fd0e-238">Suma turėtų būti išreikšta inicijuojančios šalies nurodyta valiuta.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="6fd0e-239">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="6fd0e-240">Lauke „Pavadinimas“, įveskite „End2EndID“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="6fd0e-241">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="6fd0e-242">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-242">Click Add.</span></span>
63. <span data-ttu-id="6fd0e-243">Lauke „Aprašas“ įveskite „Unikali inicijuojančios šalies priskirta identifikacija”.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="6fd0e-244">Ši identifikacija perduodama per visą tiesioginę grandinę ir lieka nepakeista“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="6fd0e-245">Lauke „Pavadinimas“ įveskite „PaymentModel“.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="6fd0e-246">Pavadinimas „PaymentModel“ sutampa su iš anksto nustatytomis mokėjimo formų sąsajomis.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="6fd0e-247">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-247">Click Save.</span></span>
66. <span data-ttu-id="6fd0e-248">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-248">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]