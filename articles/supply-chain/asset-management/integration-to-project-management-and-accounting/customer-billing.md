---
title: Kliento turto priežiūros sąskaitos pateikimas
description: Šioje temoje paaiškinama, kaip kurti, apdoroti ir išrašyti priežiūros darbo, atliekamam su jūsų klientų turtu, sąskaitą.
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 643e59f082949ed51ab61d79648a98b83a7f0b03
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131846"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a><span data-ttu-id="f178f-103">Kliento turto priežiūros sąskaitos pateikimas</span><span class="sxs-lookup"><span data-stu-id="f178f-103">Bill for maintenance on customer-owned assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f178f-104">Funkcija *Darbo užsakymo sąskaitos pateikimas* leidžia kurti, apdoroti ir pateikti priežiūros darbo, atliekamam su jūsų klientų turtu, sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="f178f-104">The *Work order billing* feature lets you create, process, and bill maintenance work that is done on assets that your customers own.</span></span> <span data-ttu-id="f178f-105">Ši funkcija jums leidžia atlikti tolesnes užduotis:</span><span class="sxs-lookup"><span data-stu-id="f178f-105">This feature lets you perform the following tasks:</span></span>

- <span data-ttu-id="f178f-106">Susieti klientus su jų turimu turtu.</span><span class="sxs-lookup"><span data-stu-id="f178f-106">Connect customers to the assets that they own.</span></span>
- <span data-ttu-id="f178f-107">Pasirinkti klientą ir peržiūrėti jam priklausantį turtą, kai kuriate darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="f178f-107">Select a customer and view the assets that customer owns when you create a work order.</span></span>
- <span data-ttu-id="f178f-108">Nustatyti pirminį projektą kiekvienam klientui.</span><span class="sxs-lookup"><span data-stu-id="f178f-108">Set up a parent project for each customer.</span></span>
- <span data-ttu-id="f178f-109">Registruoti valandas, prekes, išlaidas ir mokesčius pagal darbo užsakymą ir tada vėliau sukurti sąskaitos faktūros pasiūlymą klientui.</span><span class="sxs-lookup"><span data-stu-id="f178f-109">Register hours, items, expenses, and fees against the work order, and then create an invoice proposal for the customer later.</span></span>

<span data-ttu-id="f178f-110">Papildomai funkcija suteikia šias funkcijas:</span><span class="sxs-lookup"><span data-stu-id="f178f-110">In addition, the feature provides the following functionality:</span></span>

- <span data-ttu-id="f178f-111">Projekto sutartis automatiškai kopijuojama iš kliento pirminio projekto į atitinkamą darbo užsakymo projektą.</span><span class="sxs-lookup"><span data-stu-id="f178f-111">The project contract from a customer's parent project is automatically copied to the relevant work order project.</span></span>
- <span data-ttu-id="f178f-112">Turto valdymas dabar gali naudoti projekto operacijos tipą *mokestis* tiek darbo užsakymo prognozėse, tiek darbo užsakymų žurnaluose.</span><span class="sxs-lookup"><span data-stu-id="f178f-112">Asset management can now use the *fee* project transaction type on both work order forecasts and work order journals.</span></span>

## <a name="turn-on-the-customer-billing-feature"></a><span data-ttu-id="f178f-113">Funkcijos Kliento sąskaitos pateikimas įjungimas</span><span class="sxs-lookup"><span data-stu-id="f178f-113">Turn on the customer billing feature</span></span>

<span data-ttu-id="f178f-114">Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="f178f-114">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="f178f-115">Administratoriai gali naudoti [funkcijos valdymas](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją.</span><span class="sxs-lookup"><span data-stu-id="f178f-115">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="f178f-116">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="f178f-116">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f178f-117">**Modulis:** *Projektų valdymas ir apskaita*</span><span class="sxs-lookup"><span data-stu-id="f178f-117">**Module:** *Project management and accounting*</span></span>
- <span data-ttu-id="f178f-118">**Funkcijos pavadinimas:** *Darbo užsakymo sąskaitos pateikimas*</span><span class="sxs-lookup"><span data-stu-id="f178f-118">**Feature name:** *Work order billing*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="f178f-119">Pavyzdinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="f178f-119">Example scenario</span></span>

<span data-ttu-id="f178f-120">Norėdami sužinoti, kaip veikia ši funkcija, dirbkite naudodami šį pavyzdinį scenarijų.</span><span class="sxs-lookup"><span data-stu-id="f178f-120">To learn how this feature works, work through the following example scenario.</span></span>

<span data-ttu-id="f178f-121">Norėdami dirbti pagal šį scenarijų, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) turi būti įdiegti Jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="f178f-121">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="f178f-122">Prieš pradėdami turite pasirinkti **„USMF”** juridinį subjektą.</span><span class="sxs-lookup"><span data-stu-id="f178f-122">You must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="f178f-123">Taip pat galite naudoti šią scenarijų kaip vedlį, kaip naudotis funkcija dirbant gamybos sistemoje.</span><span class="sxs-lookup"><span data-stu-id="f178f-123">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="f178f-124">Tačiau tokiu atveju, Jūs turėsite keisti vertes ir galite neturėti kai kurių tipų būtinų įrašų, kuriuos suteikia standartiniai demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="f178f-124">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a><span data-ttu-id="f178f-125">1 žingsnis: Sukurkite naują projekto sutartį klientui</span><span class="sxs-lookup"><span data-stu-id="f178f-125">Step 1: Create a new project contract for the customer</span></span>

1. <span data-ttu-id="f178f-126">Eikite į **Projektų valdymas ir apskaita \> Projektai \> Projekto sutartys**.</span><span class="sxs-lookup"><span data-stu-id="f178f-126">Go to **Project management and accounting \> Projects \> Project contracts**.</span></span>
1. <span data-ttu-id="f178f-127">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f178f-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f178f-128">Dialogo lange **Nauja projekto sutartis** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="f178f-128">In the **New project contract** dialog box, set the following values:</span></span>

    - <span data-ttu-id="f178f-129">**Pavadinimas:** *„Pelican” didmeninė prekyba*</span><span class="sxs-lookup"><span data-stu-id="f178f-129">**Name:** *Pelican Wholesales*</span></span>
    - <span data-ttu-id="f178f-130">**Lėšų skyrimo tipas:** *Klientas*</span><span class="sxs-lookup"><span data-stu-id="f178f-130">**Funding type:** *Customer*</span></span>
    - <span data-ttu-id="f178f-131">**Lėšų skyrimo šaltinis:** *„US-013”* (*„Pelican” didmeninė prekyba)*</span><span class="sxs-lookup"><span data-stu-id="f178f-131">**Funding source:** *US-013* (*Pelican Wholesales*)</span></span>

1. <span data-ttu-id="f178f-132">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f178f-132">Select **OK**.</span></span>

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a><span data-ttu-id="f178f-133">2 žingsnis: Sukurkite pirminį projektą klientui</span><span class="sxs-lookup"><span data-stu-id="f178f-133">Step 2: Create a new parent project for the customer</span></span>

<span data-ttu-id="f178f-134">Čia sukurtas pirminis projektas bus naudojamas kuriant darbo užsakymus klientui.</span><span class="sxs-lookup"><span data-stu-id="f178f-134">The parent project that you create here will be used when work orders for the customer are created.</span></span>

1. <span data-ttu-id="f178f-135">Eikite į **Projektų valdymas ir apskaita \> Projektai \> Visi projektai**.</span><span class="sxs-lookup"><span data-stu-id="f178f-135">Go to **Project management and accounting \> Projects \> All projects**.</span></span>
1. <span data-ttu-id="f178f-136">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f178f-136">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f178f-137">Dialogo lange **Naujas projektas** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="f178f-137">In the **New project** dialog box, set the following values:</span></span>

    - <span data-ttu-id="f178f-138">**Projekto tipas:** *Laikas ir medžiaga*</span><span class="sxs-lookup"><span data-stu-id="f178f-138">**Project type:** *Time and material*</span></span>
    - <span data-ttu-id="f178f-139">**Projekto pavadinimas:** *„Pelican” didmeninės prekybos darbo užsakymai*</span><span class="sxs-lookup"><span data-stu-id="f178f-139">**Project name:** *Pelican Wholesales work orders*</span></span>
    - <span data-ttu-id="f178f-140">**Projekto grupė:** *„TM”*</span><span class="sxs-lookup"><span data-stu-id="f178f-140">**Project group:** *TM*</span></span>
    - <span data-ttu-id="f178f-141">**Projekto sutarties ID:** *„Pelican” didmeninė prekyba* (anksčiau sukurta sutartis)</span><span class="sxs-lookup"><span data-stu-id="f178f-141">**Project contract ID:** *Pelican Wholesales* (the contract that you created earlier)</span></span>
    - <span data-ttu-id="f178f-142">**Pradžios data:** Pasirinkite šiandienos datą.</span><span class="sxs-lookup"><span data-stu-id="f178f-142">**Start date:** Select today's date.</span></span>

1. <span data-ttu-id="f178f-143">Pasirinkite **Kurti projektą**.</span><span class="sxs-lookup"><span data-stu-id="f178f-143">Select **Create project**.</span></span>
1. <span data-ttu-id="f178f-144">Atidaromas naujas projektas.</span><span class="sxs-lookup"><span data-stu-id="f178f-144">The new project is opened.</span></span> <span data-ttu-id="f178f-145">Pasižymėkite **Projekto ID** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f178f-145">Make a note of the **Project ID** value.</span></span> <span data-ttu-id="f178f-146">Turėsite ją įvesti vėliau.</span><span class="sxs-lookup"><span data-stu-id="f178f-146">You will have to enter it later.</span></span>

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a><span data-ttu-id="f178f-147">3 žingsnis: Naujo darbo užsakymo tipo kūrimas turto valdyme</span><span class="sxs-lookup"><span data-stu-id="f178f-147">Step 3: Create a new work order type in Asset management</span></span>

1. <span data-ttu-id="f178f-148">Eikite į **Turto valdymas \> Sąranka \> Darbo užsakymas \> Darbo užsakymų tipai**.</span><span class="sxs-lookup"><span data-stu-id="f178f-148">Go to **Asset management \> Setup \> Work order \> Work order types**.</span></span>
1. <span data-ttu-id="f178f-149">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f178f-149">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f178f-150">Naujas įrašas įtraukiamas į sąrašą.</span><span class="sxs-lookup"><span data-stu-id="f178f-150">A new record is added to the list.</span></span> <span data-ttu-id="f178f-151">Nustatykite tokias šio įrašo reikšmes:</span><span class="sxs-lookup"><span data-stu-id="f178f-151">Set the following values for it:</span></span>

    - <span data-ttu-id="f178f-152">**Darbo užsakymo tipas:** *Paslauga*</span><span class="sxs-lookup"><span data-stu-id="f178f-152">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="f178f-153">**Pavadinimas:** *Paslaugos darbo užsakymai*</span><span class="sxs-lookup"><span data-stu-id="f178f-153">**Name:** *Service work orders*</span></span>
    - <span data-ttu-id="f178f-154">**Darbo užsakymo ciklo būsena:** *Standartinė*</span><span class="sxs-lookup"><span data-stu-id="f178f-154">**Work order lifecycle state:** *Standard*</span></span>

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a><span data-ttu-id="f178f-155">4 žingsnis: Susiekite kliento paskyrą su pirminiu projektu</span><span class="sxs-lookup"><span data-stu-id="f178f-155">Step 4: Link the customer account to the parent project</span></span>

<span data-ttu-id="f178f-156">Dabar turite susieti kliento paskyrą su pirminiu projektu Turto valdymo projektų sąrankoje.</span><span class="sxs-lookup"><span data-stu-id="f178f-156">You must now link the customer account to the parent project in the project setup in Asset management.</span></span>

1. <span data-ttu-id="f178f-157">Eikite į **Turto valdymas \> Sąranka \> Darbo užsakymai \> Projekto sąranka**.</span><span class="sxs-lookup"><span data-stu-id="f178f-157">Go to **Asset management \> Setup \> Work orders \> Project setup**.</span></span>
1. <span data-ttu-id="f178f-158">Skirtuke **Pirminis projektas** pasirinkite **Pridėti** naujai eilutei pridėti.</span><span class="sxs-lookup"><span data-stu-id="f178f-158">On the **Parent project** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="f178f-159">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="f178f-159">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f178f-160">**Kliento paskyra:** *„US-013”* (*„Pelican” didmeninė prekyba*)</span><span class="sxs-lookup"><span data-stu-id="f178f-160">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="f178f-161">**Projekto ID:** Įveskite anksčiau pasižymėtą projekto ID.</span><span class="sxs-lookup"><span data-stu-id="f178f-161">**Project ID:** Enter the project ID that you made a note of earlier.</span></span>

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a><span data-ttu-id="f178f-162">5 žingsnis: Susiekite projektų grupę ir tipą su darbo užsakymo projektu</span><span class="sxs-lookup"><span data-stu-id="f178f-162">Step 5: Link the project group and type to the work order project</span></span>

<span data-ttu-id="f178f-163">Jūs turite likti **Projekto sąrankos** puslapyje (**Turto valdymas \> Sąranka \> Darbo užsakymai \> Projekto sąranka**).</span><span class="sxs-lookup"><span data-stu-id="f178f-163">You should still be on the **Project setup** page (**Asset management \> Setup \> Work orders \> Project setup**).</span></span>

1. <span data-ttu-id="f178f-164">Skirtuke **Projekto grupė** pasirinkite **Pridėti** naujai eilutei pridėti.</span><span class="sxs-lookup"><span data-stu-id="f178f-164">On the **Project group** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="f178f-165">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="f178f-165">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f178f-166">**Darbo užsakymo tipas:** *Paslauga* (anksčiau sukurtas darbo užsakymo tipas)</span><span class="sxs-lookup"><span data-stu-id="f178f-166">**Work order type:** *Service* (the work order type that you created earlier)</span></span>
    - <span data-ttu-id="f178f-167">**Projekto grupė:** *„TM”*</span><span class="sxs-lookup"><span data-stu-id="f178f-167">**Project group:** *TM*</span></span>

> [!NOTE]
> <span data-ttu-id="f178f-168">Projekto sutartis darbo užsakymo projekte yra visada perimama iš pirminio projekto.</span><span class="sxs-lookup"><span data-stu-id="f178f-168">The project contract on the work order project is always inherited from the parent project.</span></span>

### <a name="step-6-link-an-asset-to-the-customer-id"></a><span data-ttu-id="f178f-169">6 žingsnis: Susiekite turtą su kliento ID</span><span class="sxs-lookup"><span data-stu-id="f178f-169">Step 6: Link an asset to the customer ID</span></span>

1. <span data-ttu-id="f178f-170">Eikite į **Turto valdymas \> Turtas \> Aktyvus turtas**.</span><span class="sxs-lookup"><span data-stu-id="f178f-170">Go to **Asset management \> Assets \> Active assets**.</span></span>
1. <span data-ttu-id="f178f-171">Lauke **Filtruoti** įveskite *„VE-102”* ir pasirinkite filtruoti pagal **Turtą**.</span><span class="sxs-lookup"><span data-stu-id="f178f-171">In the **Filter** field, enter *VE-102*, and select to filter by **Asset**.</span></span>
1. <span data-ttu-id="f178f-172">Pasirinkite turtą jo parametrams atidaryti.</span><span class="sxs-lookup"><span data-stu-id="f178f-172">Select the asset to open its settings.</span></span>
1. <span data-ttu-id="f178f-173">„FastTab” skirtuke **Klientas** nustatykite lauką **Kliento paskyra** į *„US-013”* (*„Pelican”didmeninė prekyba*).</span><span class="sxs-lookup"><span data-stu-id="f178f-173">On the **Customer** FastTab, set the **Customer account** field to *US-013* (*Pelican Wholesales*).</span></span>

    <span data-ttu-id="f178f-174">Laukas **Pavadinimas** automatiškai atnaujinamas į *„Pelican” didmeninė prekyba*.</span><span class="sxs-lookup"><span data-stu-id="f178f-174">The **Name** field is automatically updated to *Pelican Wholesales*.</span></span>

### <a name="step-7-create-a-new-work-order-on-the-asset"></a><span data-ttu-id="f178f-175">7 žingsnis: Sukurkite naują turto darbo užsakymą</span><span class="sxs-lookup"><span data-stu-id="f178f-175">Step 7: Create a new work order on the asset</span></span>

1. <span data-ttu-id="f178f-176">Eikite į **Turto valdymas \> Darbo užsakymai \> Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="f178f-176">Go to **Asset management \> Work orders \> Active work orders**.</span></span>
1. <span data-ttu-id="f178f-177">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f178f-177">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f178f-178">Dialogo lange **Sukurti darbo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="f178f-178">In the **Create work order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="f178f-179">**Darbo užsakymo tipas:** *Paslauga*</span><span class="sxs-lookup"><span data-stu-id="f178f-179">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="f178f-180">**Aprašas:** *Remonto sunkvežimis*</span><span class="sxs-lookup"><span data-stu-id="f178f-180">**Description:** *Repair Truck*</span></span>
    - <span data-ttu-id="f178f-181">**Kliento paskyra:** *„US-013”* (*„Pelican” didmeninė prekyba*)</span><span class="sxs-lookup"><span data-stu-id="f178f-181">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="f178f-182">**Turtas:** *„VE-102”*</span><span class="sxs-lookup"><span data-stu-id="f178f-182">**Asset:** *VE-102*</span></span>

        > [!NOTE]
        > <span data-ttu-id="f178f-183">Peržvalgoje rodomas tik su pasirinkta kliento paskyra susietas turtas.</span><span class="sxs-lookup"><span data-stu-id="f178f-183">The lookup shows only assets that are linked to the selected customer account.</span></span>

    - <span data-ttu-id="f178f-184">**Priežiūros užduoties tipas:** *Remontas*</span><span class="sxs-lookup"><span data-stu-id="f178f-184">**Maintenance job type:** *Repair*</span></span>
    - <span data-ttu-id="f178f-185">**Prekyba:** *Mechanika*</span><span class="sxs-lookup"><span data-stu-id="f178f-185">**Trade:** *Mechanic*</span></span>
    - <span data-ttu-id="f178f-186">**Paslaugos lygis:** *4'*</span><span class="sxs-lookup"><span data-stu-id="f178f-186">**Service level:** *4*</span></span>

1. <span data-ttu-id="f178f-187">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f178f-187">Select **OK**.</span></span>

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a><span data-ttu-id="f178f-188">8 žingsnis: Peržiūrėkite darbo užsakymą ir pradėkite su juo dirbti</span><span class="sxs-lookup"><span data-stu-id="f178f-188">Step 8: Review the work order and start to work on it</span></span>

<span data-ttu-id="f178f-189">Šiame skyriuje dirbsite su ankstesniame skyriuje sukurtu darbo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="f178f-189">In this section, you will work on the work order that you created in the previous section.</span></span>

1. <span data-ttu-id="f178f-190">Norėdami patikrinti, ar pirminis projektas yra *„Pelican” didmeninės prekybos darbo užsakymo* projektas, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="f178f-190">Follow these steps to verify that the parent project is the *Pelican wholesales Work order* project:</span></span>

    1. <span data-ttu-id="f178f-191">Skyriuje **Darbo užsakymo priežiūros užduotys** pasirinkite eilutę.</span><span class="sxs-lookup"><span data-stu-id="f178f-191">In the **Work order maintenance jobs** section, select a line.</span></span>
    1. <span data-ttu-id="f178f-192">„FastTab” skirtuke **Eilutės informacija** patikrinkite **Projekto ID** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f178f-192">On the **Line details** FastTab, inspect the **Project ID** value.</span></span> <span data-ttu-id="f178f-193">Ji turėtų būti brūkšninis skaičius forma *\<Parent-Project-ID\>-\<Project-ID\>*.</span><span class="sxs-lookup"><span data-stu-id="f178f-193">It should be a hyphenated number in the form *\<Parent-Project-ID\>-\<Project-ID\>*.</span></span> <span data-ttu-id="f178f-194">Ši reikšmė yra saitas.</span><span class="sxs-lookup"><span data-stu-id="f178f-194">This value is a link.</span></span>
    1. <span data-ttu-id="f178f-195">Pasirinkite projekto ID saitą atidaryti puslapiui, kuriame galite peržiūrėti pirminio projekto ir projekto pavadinimus.</span><span class="sxs-lookup"><span data-stu-id="f178f-195">Select the project ID link to open a page where you can view the parent project and project names.</span></span>

1. <span data-ttu-id="f178f-196">Veiksmų srities skirtuko **Darbo užsakymas** grupėje **Ciklo būsena** pasirinkite **Atnaujinti darbo užsakymo būseną**.</span><span class="sxs-lookup"><span data-stu-id="f178f-196">On the Action Pane, on the **Work order** tab, in the **Lifecycle state** group, select **Update work order state**.</span></span>
1. <span data-ttu-id="f178f-197">Dialogo lango **Atnaujinti darbo užsakymo būseną** stulpelyje **Pasirinkti** pasirinkite žymės langelį eilutei, kurioje laukas **Ciklo būsena** yra nustatytas į *Vykdoma*.</span><span class="sxs-lookup"><span data-stu-id="f178f-197">In the **Update work order state** dialog box, in the **Select** column, select the check box for the row where the **Lifecycle state** field is set to *In progress*.</span></span>
1. <span data-ttu-id="f178f-198">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f178f-198">Select **OK**.</span></span>
1. <span data-ttu-id="f178f-199">Dialogo lange **Ciklo būsena: Vykdoma** pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f178f-199">In the **Lifecycle state: InProgress** dialog box, select **OK**.</span></span>

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a><span data-ttu-id="f178f-200">9 žingsnis: Registruoti darbo užsakymo kūrimo valandas ir sukurti naują sąskaitos faktūros pasiūlymą</span><span class="sxs-lookup"><span data-stu-id="f178f-200">Step 9: Post the hours that were spent on the work order and create a new invoice proposal</span></span>

<span data-ttu-id="f178f-201">Šiame skyriuje ir toliau dirbsite su tuo darbo užsakymu, su kuriuo dirbote ankstesniame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="f178f-201">In this section, you will continue to work on the work order that you worked on in the previous section.</span></span>

1. <span data-ttu-id="f178f-202">Veiksmų srities skirtuko **Darbo užsakymas** grupėje **Projektas** pasirinkite **Žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="f178f-202">On the Action Pane, on the **Work order** tab, in the **Project** group, select **Journals**.</span></span>

    <span data-ttu-id="f178f-203">Rodomas **Darbo užsakymų žurnalai** puslapis.</span><span class="sxs-lookup"><span data-stu-id="f178f-203">The **Work order journals** page appears.</span></span> <span data-ttu-id="f178f-204">Čia galite registruoti laiką, kurį paskyrėte darbo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="f178f-204">Here, you can register the time that you spent on the work order.</span></span>

1. <span data-ttu-id="f178f-205">„FastTab“ **Valandos** pasirinkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="f178f-205">On the **Hours** FastTab, select **Add line**.</span></span>
1. <span data-ttu-id="f178f-206">Naujoje eilutėje nustatykite lauką **Valandos** į *4'*.</span><span class="sxs-lookup"><span data-stu-id="f178f-206">On the new, line, set the **Hours** field to *4*.</span></span>
1. <span data-ttu-id="f178f-207">Veiksmų srityje pasirinkite **Registruoti žurnalus**.</span><span class="sxs-lookup"><span data-stu-id="f178f-207">On the Action Pane, select **Post journals**.</span></span>
1. <span data-ttu-id="f178f-208">Uždarykite puslapį **Darbo užsakymų žurnalai** tam, kad sugrįžtumėte prie darbo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="f178f-208">Close the **Work order journals** page to return to the work order.</span></span>
1. <span data-ttu-id="f178f-209">Veiksmų srities skirtuke **Sąskaitų faktūrų išrašymas** pasirinkite **Naujas sąskaitos faktūros pasiūlymas**.</span><span class="sxs-lookup"><span data-stu-id="f178f-209">On the Action Pane, on the **Invoicing** tab, select **New invoice proposal**.</span></span>
1. <span data-ttu-id="f178f-210">Dialogo lango **Kurti sąskaitos faktūros pasiūlymą** skyriuje **Projekto operacijos** pasirinkite žymės langelį **Pasirinkti** kiekvienai eilutei, kuriai norite sukurti sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="f178f-210">In the **Create invoice proposal** dialog box, in the **Project transactions** section, select the **Select** check box for every line  that you want to invoice.</span></span>
1. <span data-ttu-id="f178f-211">Pasirinkite **Gerai** tam, kad uždarytumėte dialogo langą ir peržiūrėtumėte naują sąskaitos faktūros pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="f178f-211">Select **OK** to close the dialog box and view the new invoice proposal.</span></span>
