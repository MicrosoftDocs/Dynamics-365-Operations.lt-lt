---
title: EUR-00011, ES pardavimo sąrašo ataskaitų nustatymas
description: Ši užduotis skirta jums padėti peržiūrėti būtinąsias sąlygas, kurių reikia laikytis norint teikti ES pardavimo sąrašo ataskaitas.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, SysQueryForm, SysQueryFieldLookUp,  TaxTable, TaxGroup, TaxItemGroup, TaxCountryRegionParameters, TaxVATNumTable, IntrastatParameters, CustTable, DirPartyQuickCreateForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c312e14247c42acd5e0de5df02833275d9e3a4f1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408210"
---
# <a name="eur-00011-set-up-eu-sales-list-reporting"></a><span data-ttu-id="19fb1-103">EUR-00011, ES pardavimo sąrašo ataskaitų nustatymas</span><span class="sxs-lookup"><span data-stu-id="19fb1-103">EUR-00011 Set up EU sales list reporting</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="19fb1-104">Ši užduotis skirta jums padėti peržiūrėti būtinąsias sąlygas, kurių reikia laikytis norint teikti ES pardavimo sąrašo ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="19fb1-104">This task walks you through an overview of the prerequisites required for EU sales list reporting.</span></span> <span data-ttu-id="19fb1-105">Daugiau informacijos apie ES pardavimo sąrašų ataskaitas, įskaitant būtinąsias sąlygas, žr. žinyne.</span><span class="sxs-lookup"><span data-stu-id="19fb1-105">For more information about EU Sales list reporting, including required prerequisites, refer to Help.</span></span>

<span data-ttu-id="19fb1-106">ES pardavimo sąrašo ataskaitų „wiki‟ puslapį.</span><span class="sxs-lookup"><span data-stu-id="19fb1-106">This task applies to all European countries/regions.</span></span> <span data-ttu-id="19fb1-107">Vadovas buvo sukurtas naudojant demonstracinių duomenų įmonės DEMF paslaugas ir dėl to kaip šalies / regiono pavyzdį naudojant Vokietiją.</span><span class="sxs-lookup"><span data-stu-id="19fb1-107">The guide was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="19fb1-108">Vadovas taip pat kaip ES šalies / regiono pavyzdį naudoja Portugaliją.</span><span class="sxs-lookup"><span data-stu-id="19fb1-108">The guide also uses Portugal as an exemplar EU country/region.</span></span>

<span data-ttu-id="19fb1-109">Šios užduotys yra skirtos sistemų administratoriams.</span><span class="sxs-lookup"><span data-stu-id="19fb1-109">These tasks are intended for system administrators.</span></span>


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a><span data-ttu-id="19fb1-110">Elektroninių ataskaitų konfigūracijų, skirtų ES pardavimų sąrašo ataskaitoms, importavimas</span><span class="sxs-lookup"><span data-stu-id="19fb1-110">Import electronic reporting configurations for EU sales list reporting</span></span>
1. <span data-ttu-id="19fb1-111">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="19fb1-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="19fb1-112">Spustelėkite Nustatyti kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="19fb1-112">Click Set active.</span></span>
3. <span data-ttu-id="19fb1-113">Spustelėkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="19fb1-113">Click Repositories.</span></span>
4. <span data-ttu-id="19fb1-114">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="19fb1-114">Click Open.</span></span>
5. <span data-ttu-id="19fb1-115">Veiksmų srityje spustelėkite Parinktys.</span><span class="sxs-lookup"><span data-stu-id="19fb1-115">On the Action Pane, click Options.</span></span>
6. <span data-ttu-id="19fb1-116">Spustelėkite Išplėstinis filtras / rūšiavimas.</span><span class="sxs-lookup"><span data-stu-id="19fb1-116">Click Advanced Filter/Sort.</span></span>
7. <span data-ttu-id="19fb1-117">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="19fb1-117">Click Add.</span></span>
8. <span data-ttu-id="19fb1-118">Lauke Laukas pasirinkite „Konfigūracijos pavadinimas“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-118">In the Field field, select 'Configuration name'.</span></span>
9. <span data-ttu-id="19fb1-119">Lauke Kriterijai įveskite „ES pardavimų sąrašas (DE)“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-119">In the Criteria field, type 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="19fb1-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="19fb1-120">Click OK.</span></span>
11. <span data-ttu-id="19fb1-121">Spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="19fb1-121">Click Import.</span></span>
12. <span data-ttu-id="19fb1-122">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="19fb1-122">Click Yes.</span></span>
13. <span data-ttu-id="19fb1-123">Veiksmų srityje spustelėkite Parinktys.</span><span class="sxs-lookup"><span data-stu-id="19fb1-123">On the Action Pane, click Options.</span></span>
14. <span data-ttu-id="19fb1-124">Spustelėkite Išplėstinis filtras / rūšiavimas.</span><span class="sxs-lookup"><span data-stu-id="19fb1-124">Click Advanced Filter/Sort.</span></span>
15. <span data-ttu-id="19fb1-125">Spustelėkite Nustatyti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="19fb1-125">Click Reset.</span></span>
16. <span data-ttu-id="19fb1-126">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="19fb1-126">Click Add.</span></span>
17. <span data-ttu-id="19fb1-127">Lauke Laukas pasirinkite „Konfigūracijos pavadinimas“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-127">In the Field field, select 'Configuration name'.</span></span>
18. <span data-ttu-id="19fb1-128">Lauke Kriterijai įveskite „ES pardavimų sąrašas pagal eilučių ataskaitą“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-128">In the Criteria field, type 'EU Sales list by rows report'.</span></span>
19. <span data-ttu-id="19fb1-129">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="19fb1-129">Click OK.</span></span>
20. <span data-ttu-id="19fb1-130">Spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="19fb1-130">Click Import.</span></span>
21. <span data-ttu-id="19fb1-131">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="19fb1-131">Click Yes.</span></span>

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a><span data-ttu-id="19fb1-132">ES pardavimų sąrašo ataskaitų PVM kodų nustatymas</span><span class="sxs-lookup"><span data-stu-id="19fb1-132">Set up sales tax codes for EU sales list reporting</span></span>
1. <span data-ttu-id="19fb1-133">Pasirinkite Mokestis > Netiesioginiai mokesčiai > PVM > PVM kodai.</span><span class="sxs-lookup"><span data-stu-id="19fb1-133">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="19fb1-134">Naudodami spartųjį filtrą atfiltruokite lauką PVM kodas pagal reikšmę „PVM19“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-134">Use the Quick Filter to filter on the Sales tax code field with a value of 'VAT19'.</span></span>
3. <span data-ttu-id="19fb1-135">Išplėskite skyrių Ataskaitų nustatymai.</span><span class="sxs-lookup"><span data-stu-id="19fb1-135">Expand the Report setup section.</span></span>
    * <span data-ttu-id="19fb1-136">Patikrinkite, ar pasirinkties Neįtraukta nustatymas yra Nr.</span><span class="sxs-lookup"><span data-stu-id="19fb1-136">Verify that the Excluded selection is set to No.</span></span>  
    * <span data-ttu-id="19fb1-137">Norint pakeisti šį parametrą, jums gali reikėti atrakinti užduoties vadovą.</span><span class="sxs-lookup"><span data-stu-id="19fb1-137">You may need to unlock the task guide to change this setting.</span></span>  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="19fb1-138">ES pardavimų sąrašo ataskaitų PVM grupių nustatymas</span><span class="sxs-lookup"><span data-stu-id="19fb1-138">Set up sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="19fb1-139">Eikite į Mokestis > Netiesioginiai mokesčiai > PVM > PVM grupės.</span><span class="sxs-lookup"><span data-stu-id="19fb1-139">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="19fb1-140">Naudodami spartųjį filtrą atfiltruokite lauką PVM grupė pagal reikšmę „AR-DOM“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-140">Use the Quick Filter to filter on the Sales tax group field with a value of 'AR-DOM'.</span></span>
3. <span data-ttu-id="19fb1-141">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="19fb1-141">Click Edit.</span></span>
4. <span data-ttu-id="19fb1-142">Išplėskite skyrių Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="19fb1-142">Expand the Setup section.</span></span>
5. <span data-ttu-id="19fb1-143">Sąraše pasirinkite pirmą eilutę.</span><span class="sxs-lookup"><span data-stu-id="19fb1-143">In the list, select the first row.</span></span>
6. <span data-ttu-id="19fb1-144">Pažymėkite žymės langelį Neapmokestinama.</span><span class="sxs-lookup"><span data-stu-id="19fb1-144">Select the Exempt check box.</span></span>
7. <span data-ttu-id="19fb1-145">Sąraše pasirinkite antrą eilutę.</span><span class="sxs-lookup"><span data-stu-id="19fb1-145">In the list, select the second row.</span></span>
8. <span data-ttu-id="19fb1-146">Pažymėkite žymės langelį Neapmokestinama.</span><span class="sxs-lookup"><span data-stu-id="19fb1-146">Select the Exempt check box.</span></span>
9. <span data-ttu-id="19fb1-147">Sąraše pasirinkite trečią eilutę.</span><span class="sxs-lookup"><span data-stu-id="19fb1-147">In the list, select the third row.</span></span>
10. <span data-ttu-id="19fb1-148">Pažymėkite žymės langelį Neapmokestinama.</span><span class="sxs-lookup"><span data-stu-id="19fb1-148">Select the Exempt check box.</span></span>

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="19fb1-149">ES pardavimų sąrašo ataskaitų prekių PVM grupių nustatymas</span><span class="sxs-lookup"><span data-stu-id="19fb1-149">Set up item sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="19fb1-150">Eikite į Mokestis > Netiesioginiai mokesčiai > PVM > Prekės PVM grupės.</span><span class="sxs-lookup"><span data-stu-id="19fb1-150">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
2. <span data-ttu-id="19fb1-151">Naudodami spartųjį filtrą atfiltruokite lauką Prekės PVM grupė pagal reikšmę „VISAS “.</span><span class="sxs-lookup"><span data-stu-id="19fb1-151">Use the Quick Filter to filter on the Item sales tax group field with a value of 'FULL '.</span></span>
    * <span data-ttu-id="19fb1-152">Patikrinkite, ar pasirinkties Ataskaitos tipas nustatymas yra „Prekė“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-152">Verify that the Reporting type selection is set to 'Item'.</span></span>  
    * <span data-ttu-id="19fb1-153">Norint pakeisti šio lauko reikšmę, jums gali reikėti atrakinti užduoties vadovą.</span><span class="sxs-lookup"><span data-stu-id="19fb1-153">You may need to unlock the task guide to change the value in this field.</span></span>  
3. <span data-ttu-id="19fb1-154">Naudodami spartųjį filtrą atfiltruokite lauką Prekės PVM grupė pagal reikšmę „RAUDONAS “.</span><span class="sxs-lookup"><span data-stu-id="19fb1-154">Use the Quick Filter to filter on the Item sales tax group field with a value of 'RED '.</span></span>
    * <span data-ttu-id="19fb1-155">Patikrinkite, ar pasirinkties Ataskaitos tipas nustatymas yra „Paslauga“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-155">Verify that the Reporting type selection is set to 'Service'.</span></span>  
    * <span data-ttu-id="19fb1-156">Norint pakeisti šio lauko reikšmę, jums gali reikėti atrakinti užduoties vadovą.</span><span class="sxs-lookup"><span data-stu-id="19fb1-156">You may need to unlock the task guide to change the value in this field.</span></span>  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a><span data-ttu-id="19fb1-157">ES pardavimų sąrašo ataskaitų šalies / regiono parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="19fb1-157">Set up country/region parameters for EU sales list reporting</span></span>
1. <span data-ttu-id="19fb1-158">Eikite į Mokestis > Nustatymas > PVM > Šalies / regiono parametrai.</span><span class="sxs-lookup"><span data-stu-id="19fb1-158">Go to Tax > Setup > Sales tax > Country/region parameters.</span></span>
2. <span data-ttu-id="19fb1-159">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="19fb1-159">Click New.</span></span>
3. <span data-ttu-id="19fb1-160">Lauke Šalis / regionas įveskite „PRT“</span><span class="sxs-lookup"><span data-stu-id="19fb1-160">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="19fb1-161">Lauke PVM įveskite „PT“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-161">In the Sales tax field, type 'PT'.</span></span>

## <a name="create-tax-exempt-numbers"></a><span data-ttu-id="19fb1-162">PVM mokėtojo kodų kūrimas</span><span class="sxs-lookup"><span data-stu-id="19fb1-162">Create tax exempt numbers</span></span>
1. <span data-ttu-id="19fb1-163">Eikite į Mokestis > Nustatymas > PVM > PVM mokėtojo kodai.</span><span class="sxs-lookup"><span data-stu-id="19fb1-163">Go to Tax > Setup > Sales tax > Tax exempt numbers.</span></span>
2. <span data-ttu-id="19fb1-164">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="19fb1-164">Click New.</span></span>
3. <span data-ttu-id="19fb1-165">Lauke Šalis / regionas įveskite „PRT“</span><span class="sxs-lookup"><span data-stu-id="19fb1-165">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="19fb1-166">Lauke PVM mokėtojo kodas įveskite „PT12345“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-166">In the Tax exempt number field, type 'PT12345'.</span></span>

## <a name="set-up-eu-sales-list-reporting-parameters"></a><span data-ttu-id="19fb1-167">ES pardavimų sąrašo ataskaitų parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="19fb1-167">Set up EU sales list reporting parameters</span></span>
1. <span data-ttu-id="19fb1-168">Eikite į Mokestis > Nustatymas > Užsienio prekyba > Užsienio prekybos parametrai.</span><span class="sxs-lookup"><span data-stu-id="19fb1-168">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="19fb1-169">Spustelėkite skirtuką ES pardavimų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="19fb1-169">Click the EU sales list tab.</span></span>
3. <span data-ttu-id="19fb1-170">Lauke Perkelti pirkinius pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="19fb1-170">Select Yes in the Transfer purchases field.</span></span>
4. <span data-ttu-id="19fb1-171">Išplėskite skyrių Apvalinimo taisyklės.</span><span class="sxs-lookup"><span data-stu-id="19fb1-171">Expand the Rounding rules section.</span></span>
5. <span data-ttu-id="19fb1-172">Nustatykite skyriaus Apvalinimo taisyklė parinktį „0.1“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-172">Set Rounding rule to '0.1'.</span></span>
6. <span data-ttu-id="19fb1-173">Lauke Naudoti minimalią reikšmę pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="19fb1-173">Select Yes in the Use minimum value field.</span></span>
7. <span data-ttu-id="19fb1-174">Lauke Dešimtainių dalių skaičius įveskite „2“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-174">In the Number of decimals field, enter '2'.</span></span>
8. <span data-ttu-id="19fb1-175">Išplėskite skyrių Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="19fb1-175">Expand the Electronic reporting section.</span></span>
9. <span data-ttu-id="19fb1-176">Lauke Failo formato susiejimas pasirinkite „ES pardavimų sąrašas (DE)“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-176">In the File format mapping field, select 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="19fb1-177">Lauke Ataskaitos formato susiejimas pasirinkite „ES pardavimų sąrašas pagal eilučių ataskaitą“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-177">In the Report format mapping field, select 'EU Sales list by rows report'.</span></span>
11. <span data-ttu-id="19fb1-178">Spustelėkite skirtuką Šalies / regiono ypatybės.</span><span class="sxs-lookup"><span data-stu-id="19fb1-178">Click the Country/region properties tab.</span></span>
    * <span data-ttu-id="19fb1-179">Patikrinkite, ar lauko Šalies / regiono tipas, skirto šalies / regiono DEU, nustatymas yra „Vietinis“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-179">Verify that the Country/region type field is set to 'Domestic' for Country/region DEU.</span></span>  
    * <span data-ttu-id="19fb1-180">Norint pakeisti šio lauko reikšmę, jums gali reikėti atrakinti užduoties vadovą.</span><span class="sxs-lookup"><span data-stu-id="19fb1-180">You may need to unlock the task guide to change the value in this field.</span></span>  
12. <span data-ttu-id="19fb1-181">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="19fb1-181">Click New.</span></span>
13. <span data-ttu-id="19fb1-182">Lauke Šalis / regionas įveskite „PRT“</span><span class="sxs-lookup"><span data-stu-id="19fb1-182">In the Country/region field, type 'PRT'.</span></span>
14. <span data-ttu-id="19fb1-183">Lauke „Intrastat“ kodas įveskite „PT“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-183">In the Intrastat code field, type 'PT'.</span></span>
15. <span data-ttu-id="19fb1-184">Lauke Šalies / regiono tipas pasirinkite „ES“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-184">In the Country/region type field, select 'EU'.</span></span>
16. <span data-ttu-id="19fb1-185">Spustelėkite skirtuką Numeracijos.</span><span class="sxs-lookup"><span data-stu-id="19fb1-185">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="19fb1-186">Patikrinkite, ar skaičių sekos kodas yra nurodytas priskiriant nuorodai „ES pardavimų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-186">Verify that a Number sequence code is specified for the Reference 'EU sales list'.</span></span>  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a><span data-ttu-id="19fb1-187">Kliento kūrimas ES pardavimų sąrašo ataskaitų demonstraciniams tikslams</span><span class="sxs-lookup"><span data-stu-id="19fb1-187">Create a customer for EU sales list reporting demo purposes</span></span>
1. <span data-ttu-id="19fb1-188">Pasirinkite Gautinos sumos > Klientai > Visi klientai.</span><span class="sxs-lookup"><span data-stu-id="19fb1-188">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="19fb1-189">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="19fb1-189">Click New.</span></span>
3. <span data-ttu-id="19fb1-190">Lauke Kliento sąskaita įveskite „PRT-001“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-190">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="19fb1-191">Lauke Pavadinimas įveskite „Klientas iš Portugalijos“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-191">In the Name field, type 'A customer from Portugal'.</span></span>
5. <span data-ttu-id="19fb1-192">Lauke Klientų grupė pasirinkite „10“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-192">In the Customer group field, select '10'.</span></span>
6. <span data-ttu-id="19fb1-193">Lauke PVM grupė pasirinkite „AR-DOM“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-193">In the Sales tax group field, select 'AR-DOM'.</span></span>
7. <span data-ttu-id="19fb1-194">Lauke PVM mokėtojo kodas pasirinkite „PT12345“.</span><span class="sxs-lookup"><span data-stu-id="19fb1-194">In the Tax exempt number field, select 'PT12345'.</span></span>
8. <span data-ttu-id="19fb1-195">Lauke Šalis / regionas įveskite „PRT“</span><span class="sxs-lookup"><span data-stu-id="19fb1-195">In the Country/region field, type 'PRT'.</span></span>
9. <span data-ttu-id="19fb1-196">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="19fb1-196">Click Save.</span></span>

