---
title: Bangos vykdymo pranešimai
description: Šioje temoje aprašyti bangos vykdymo pranešimai ir paaiškinta, kaip juos nustatyti.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2022-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: fee112d3211f619b2146dd21c4f8a52ad33667d6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019159"
---
# <a name="wave-execution-notifications"></a><span data-ttu-id="73c38-103">Bangos vykdymo pranešimai</span><span class="sxs-lookup"><span data-stu-id="73c38-103">Wave execution notifications</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="73c38-104">Funkcija *Bangos vykdymo pranešimai* naudoja verslo įvykius ir veiksmų centrą pateikti pranešimams, susijusiems su bangos vykdymu.</span><span class="sxs-lookup"><span data-stu-id="73c38-104">The *Wave execution notifications* feature uses business events and the Action center to deliver notifications that are related to wave execution.</span></span> <span data-ttu-id="73c38-105">Tai leidžia jums nurodyti įvykius, kurie generuoja pranešimus, sandėliuos, kurie juos generuoja ir vartotojus, kurie juos gauna.</span><span class="sxs-lookup"><span data-stu-id="73c38-105">It lets you specify the types of events that generate notifications, the warehouses that generate them, and the users who receive them.</span></span>

<span data-ttu-id="73c38-106">Mygtukas **Rodyti pranešimus** (skambučio simbolis), esantis dešinėje naršymo meniu pusėje, nurodo, kada veiksmų centro pranešimas bus pasiekiamas dabartiniam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="73c38-106">The **Show messages** button (bell symbol) on the right side of the navigation bar indicates when an Action center message is available for the current user.</span></span> <span data-ttu-id="73c38-107">Vartotojas gali pasirinkti mygtuką **Rodyti pranešimus** veiksmų centrui atidaryti ir pranešimams peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="73c38-107">The user can select the **Show messages** button to open the Action center and review the messages.</span></span>

<span data-ttu-id="73c38-108">Verslo įvykiai įvyksta, kai paleidžiami verslo procesai.</span><span class="sxs-lookup"><span data-stu-id="73c38-108">Business events occur when business processes are run.</span></span> <span data-ttu-id="73c38-109">Verslo procesai susideda iš užduočių.</span><span class="sxs-lookup"><span data-stu-id="73c38-109">Business processes are made up of tasks.</span></span> <span data-ttu-id="73c38-110">Verslo proceso metu jame dalyvaujantys vartotojai atlieka verslo veiksmus toms užduotims atlikti.</span><span class="sxs-lookup"><span data-stu-id="73c38-110">During a business process, the users who participate in it perform business actions to complete those tasks.</span></span> <span data-ttu-id="73c38-111">Verslo įvykiai suteikia mechanizmą, kuris leidžia išorinėms sistemoms gauti pranešimus iš „Finance and Operations” programų.</span><span class="sxs-lookup"><span data-stu-id="73c38-111">Business events provide a mechanism that lets external systems receive notifications from Finance and Operations applications.</span></span> <span data-ttu-id="73c38-112">Tokiu būdu sistemos gali atlikti verslo veiksmus, kaip atsaką į verslo įvykius.</span><span class="sxs-lookup"><span data-stu-id="73c38-112">In this way, the systems can perform business actions in response to the business events.</span></span> <span data-ttu-id="73c38-113">Daugiau informacijos rasite [Verslo įvykių apžvalga](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span><span class="sxs-lookup"><span data-stu-id="73c38-113">For more information, see [Business events overview](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span></span>

## <a name="turn-on-the-wave-execution-notifications-feature"></a><span data-ttu-id="73c38-114">Bangos vykdymo pranešimų funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="73c38-114">Turn on the Wave execution notifications feature</span></span>

<span data-ttu-id="73c38-115">Norėdami naudoti *Bangos vykdymo pranešimų* funkciją, įjunkite ją savo sistemoje.</span><span class="sxs-lookup"><span data-stu-id="73c38-115">Before you can use the *Wave execution notifications* feature, it must be turned on in your system.</span></span> <span data-ttu-id="73c38-116">Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="73c38-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="73c38-117">Ten ši funkcija pateikiama taip:</span><span class="sxs-lookup"><span data-stu-id="73c38-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="73c38-118">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="73c38-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="73c38-119">**Funkcijos pavadinimas:** *Bangos vykdymo pranešimai*</span><span class="sxs-lookup"><span data-stu-id="73c38-119">**Feature name:** *Wave execution notifications*</span></span>

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a><span data-ttu-id="73c38-120">Scenarijus: bangos paketinio vykdymo pranešimų siuntimas į veiksmų centrą</span><span class="sxs-lookup"><span data-stu-id="73c38-120">Scenario: Send wave batch execution notifications to the Action center</span></span>

<span data-ttu-id="73c38-121">Šis scenarijus rodo tiesioginį srautą, skirtą pranešimų apie bangos paketinio vykdymo klaidas siuntimui į konkretų vaidmenį per veiksmų centrą.</span><span class="sxs-lookup"><span data-stu-id="73c38-121">This scenario shows the end-to-end flow for sending notifications about wave batch execution errors to a specific role via the Action center.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="73c38-122">Demonstracinių duomenų įgalinimas</span><span class="sxs-lookup"><span data-stu-id="73c38-122">Make demo data available</span></span>

<span data-ttu-id="73c38-123">Šio scenarijaus įgyvendinimui, privalote turėti įdiegtus demo duomenis ir pasirinkti **USMF** juridinį asmenį.</span><span class="sxs-lookup"><span data-stu-id="73c38-123">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a><span data-ttu-id="73c38-124">Užtikrinkite, kad bangos veikia paketiniu režimu</span><span class="sxs-lookup"><span data-stu-id="73c38-124">Make sure that waves are run in batch mode</span></span>

1. <span data-ttu-id="73c38-125">Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="73c38-125">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="73c38-126">„FastTab” **Bangų apdorojimas** nustatykite parinktį **Apdoroti bangas paketais** į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="73c38-126">On the **Wave processing** FastTab, set the **Process waves in batch** option to *Yes*.</span></span>

> [!NOTE]
> <span data-ttu-id="73c38-127">Jei norite išjungti bangos paketinio vykdymo pranešimus, nustatykite parinktį **Išjungti bangos paketinio apdorojimo pranešimus** į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="73c38-127">If you want to disable wave batch execution notifications, set the **Disable wave processing batch notifications** option to *Yes*.</span></span>

### <a name="configure-a-wave-notification-policy"></a><span data-ttu-id="73c38-128">Bangos pranešimų strategijos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="73c38-128">Configure a wave notification policy</span></span>

<span data-ttu-id="73c38-129">Bangos pranešimų strategijos nurodo vartotojams siunčiamų pranešimų tipus.</span><span class="sxs-lookup"><span data-stu-id="73c38-129">Wave notification policies define the types of notifications that are sent and the users who are notified.</span></span>

1. <span data-ttu-id="73c38-130">Eikite į **Sandėlio tvarkymas \> Sąranka \> Bangos \> Bangos pranešimų strategijos**.</span><span class="sxs-lookup"><span data-stu-id="73c38-130">Go to **Warehouse management \> Setup \> Waves \> Wave notification policies**.</span></span>
1. <span data-ttu-id="73c38-131">Sukurkite įrašą, kuris turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="73c38-131">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="73c38-132">**Bangos pranešimų strategija:** *24 Paketo klaida*</span><span class="sxs-lookup"><span data-stu-id="73c38-132">**Wave notification policy:** *24BatchError*</span></span>
    - <span data-ttu-id="73c38-133">**Aprašas:** *24 sandėlio bangų paketo klaida*</span><span class="sxs-lookup"><span data-stu-id="73c38-133">**Description:** *Warehouse 24 wave batch error*</span></span>
    - <span data-ttu-id="73c38-134">**Siųsti pranešimą:** *Tik klaidos*</span><span class="sxs-lookup"><span data-stu-id="73c38-134">**Send notification on:** *Error only*</span></span>
    - <span data-ttu-id="73c38-135">**Į vaidmenį:** *Sistemos administratorius*</span><span class="sxs-lookup"><span data-stu-id="73c38-135">**To role:** *System administrator*</span></span>

        > [!NOTE]
        > <span data-ttu-id="73c38-136">Kadangi šiame scenarijuje naudojami demonstraciniai duomenys, *Sistemos administratoriaus* vaidmuo buvo pasirinktas dėl paprastumo.</span><span class="sxs-lookup"><span data-stu-id="73c38-136">Because this scenario uses demo data, the *System administrator* role is selected for the sake of simplicity.</span></span> <span data-ttu-id="73c38-137">Todėl, kadangi esate prisijungęs kaip sistemos administratoriaus vartotojas, gausite pranešimus.</span><span class="sxs-lookup"><span data-stu-id="73c38-137">Therefore, because you're signed in as a system administrator user, you will receive the notifications.</span></span> <span data-ttu-id="73c38-138">Tačiau praktiškai, įprastai turėtumėte pasirinkti konkretesnį vaidmenį, kuriam pranešti apie bangos paketinio vykdymo klaidas, pavyzdžiui, *Sandėlio vadovą*.</span><span class="sxs-lookup"><span data-stu-id="73c38-138">However, in practice, you should usually select a more specific role to notify about wave batch execution errors, such as *Warehouse manager*.</span></span>

1. <span data-ttu-id="73c38-139">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="73c38-139">On the Action Pane, select **Save**.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="73c38-140">Bangos šablono konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="73c38-140">Configure a wave template</span></span>

<span data-ttu-id="73c38-141">Bangos šablonai leidžia jums susieti konkrečius bangų metodų atvejus su atitinkamais bangos žymos šablonais.</span><span class="sxs-lookup"><span data-stu-id="73c38-141">Wave templates let you link specific instances of wave methods to corresponding wave label templates.</span></span>

1. <span data-ttu-id="73c38-142">Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="73c38-142">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="73c38-143">Sąrašo srityje nustatykite lauką **Bangos šablono tipas** į *Siuntimas*, o tada pasirinkite *24 numatytojo siuntimo* bangos šabloną 24 sandėliui.</span><span class="sxs-lookup"><span data-stu-id="73c38-143">In the list pane, set the **Wave template type** field to *Shipping*, and then select the *24 Shipping Default* wave template for warehouse 24.</span></span>
1. <span data-ttu-id="73c38-144">„FastTab“ **Bendra** nustatykite **Bangos pranešimų strategija** lauką į *24 Paketinė klaida*.</span><span class="sxs-lookup"><span data-stu-id="73c38-144">On the **General** FastTab, set the **Wave notification policy** field to *24BatchError*.</span></span>

### <a name="configure-a-work-template"></a><span data-ttu-id="73c38-145">Bangos šablono konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="73c38-145">Configure a work template</span></span>

<span data-ttu-id="73c38-146">Darbo šablonai naudojami bangos vykdymo metu generuoti darbui.</span><span class="sxs-lookup"><span data-stu-id="73c38-146">Work templates are used during wave execution to generate work.</span></span> <span data-ttu-id="73c38-147">Šiame scenarijuje bangos vykdymas turi sukelti klaidą.</span><span class="sxs-lookup"><span data-stu-id="73c38-147">For this scenario, wave execution should trigger an error.</span></span> <span data-ttu-id="73c38-148">Nustatydami darbo šablono užklausą neegzistuojančio sandėlio naudojimui, užtikrinsite, kad bangos vykdymas nepavyks, tad atsiųs pranešimą.</span><span class="sxs-lookup"><span data-stu-id="73c38-148">By setting the work template query to use a nonexistent warehouse, you will ensure that wave execution fails and therefore sends a notification.</span></span>

1. <span data-ttu-id="73c38-149">Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="73c38-149">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="73c38-150">Sąrašo srityje nustatykite lauką **Darbo šablono tipas** į *Pardavimo užsakymai* ir tada pasirinkite *24 PU etapo* darbo šabloną 24 sandėliui.</span><span class="sxs-lookup"><span data-stu-id="73c38-150">In the list pane, set the **Work template type** field to *Sales orders* and then select the *24 SO Stage* work template for warehouse 24.</span></span>
1. <span data-ttu-id="73c38-151">Veiksmų srityje pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="73c38-151">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="73c38-152">Užklausos redaktoriaus dialogo lango skirtuke **Diapazonas** redaguokite šią eilutę (arba pridėkite ją, jeigu jos nėra):</span><span class="sxs-lookup"><span data-stu-id="73c38-152">In the query editor dialog box, on the **Range** tab, edit the following row (or add it if it doesn't exist):</span></span>

    - <span data-ttu-id="73c38-153">**Lentelė:** *Laikinos darbo operacijos*</span><span class="sxs-lookup"><span data-stu-id="73c38-153">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="73c38-154">**Išvestinė lentelė:** *Laikinos darbo operacijos*</span><span class="sxs-lookup"><span data-stu-id="73c38-154">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="73c38-155">**Laukas:** *Sandėlis*</span><span class="sxs-lookup"><span data-stu-id="73c38-155">**Field:** *Warehouse*</span></span>
    - <span data-ttu-id="73c38-156">**Kriterijai:** pakeiskite reikšmę *iš 24* į *Klaida*.</span><span class="sxs-lookup"><span data-stu-id="73c38-156">**Criteria:** Change the value from *24* to *Error*.</span></span>

1. <span data-ttu-id="73c38-157">Pasirinkite **Gerai** ir patvirtinkite keitimą.</span><span class="sxs-lookup"><span data-stu-id="73c38-157">Select **OK**, and confirm the change.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="73c38-158">Sukurkite prekybos užsakymą ir išleiskite jį į sandėlį</span><span class="sxs-lookup"><span data-stu-id="73c38-158">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="73c38-159">Eikite į **Prekyba ir komercija \> Prekybos užsakymas \> Visi prekybos užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="73c38-159">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="73c38-160">Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="73c38-160">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="73c38-161">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="73c38-161">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="73c38-162">**Sandėlis:** *24*</span><span class="sxs-lookup"><span data-stu-id="73c38-162">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="73c38-163">„FastTab” **Pardavimo užsakymo eilutės** įtraukite pardavimo užsakymo eilutę, turinčią šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="73c38-163">On the **Sales order lines** FastTab, add a sales order line that has the following settings:</span></span>

    - <span data-ttu-id="73c38-164">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="73c38-164">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="73c38-165">**Kiekis:** *10*</span><span class="sxs-lookup"><span data-stu-id="73c38-165">**Quantity:** *10*</span></span>

    > [!NOTE]
    > <span data-ttu-id="73c38-166">Šitos prekės ir kiekiai yra tik pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="73c38-166">These items and quantities are only examples.</span></span> <span data-ttu-id="73c38-167">Nurodytame sandėlyje turi būti pakankamai atsargų.</span><span class="sxs-lookup"><span data-stu-id="73c38-167">The specified warehouse must contain enough stock.</span></span>

1. <span data-ttu-id="73c38-168">Kai „FastTab” **Pardavimo užsakymo eilutės** vis dar renkatės naują liniją, įrankių juostoje pasirinkite **Atsargos \> Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="73c38-168">While the new line is still selected on the **Sales order lines** FastTab, select **Inventory \> Reservation** on the toolbar.</span></span>
1. <span data-ttu-id="73c38-169">**Rezervacija** puslapyje, esančiame Veiksmų srityje, pasirinkite **Rezervuoti partiją**.</span><span class="sxs-lookup"><span data-stu-id="73c38-169">On the **Reservation** page, on the Action Pane, select **Reserve lot**.</span></span> <span data-ttu-id="73c38-170">Tada uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="73c38-170">Then close the page.</span></span>
1. <span data-ttu-id="73c38-171">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="73c38-171">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

### <a name="notifications-from-wave-batch-job-execution"></a><span data-ttu-id="73c38-172">Pranešimai iš bangos paketo užduoties vykdymo</span><span class="sxs-lookup"><span data-stu-id="73c38-172">Notifications from wave batch job execution</span></span>

<span data-ttu-id="73c38-173">Atsižvelgiant į jūsų verslo įvykių nustatymą, galiausiai jūs gausite pranešimą apie bangos vykdymo nesėkmę.</span><span class="sxs-lookup"><span data-stu-id="73c38-173">Depending on the setup of your business events, you will eventually receive a notification about wave execution failure.</span></span> <span data-ttu-id="73c38-174">Veiksmų centro pranešimas bus panašus į toliau pateiktą pavyzdį ir įtrauks nuorodą į nepavykusią bangą.</span><span class="sxs-lookup"><span data-stu-id="73c38-174">The Action center message will resemble the following example and will include a link to the wave that failed.</span></span>

> <span data-ttu-id="73c38-175">**Klaida vykdant bangą**</span><span class="sxs-lookup"><span data-stu-id="73c38-175">**Error during wave execution**</span></span>  
> <span data-ttu-id="73c38-176">Vykdant bangą USMF-000000001 įvyko klaida.</span><span class="sxs-lookup"><span data-stu-id="73c38-176">An error occurred while executing wave USMF-000000001.</span></span>  
> <span data-ttu-id="73c38-177">Paskutiniai pranešimai: bangai USMF-000000001 nebuvo sukurta jokio darbo.</span><span class="sxs-lookup"><span data-stu-id="73c38-177">Last messages: No Work was created for Wave USMF-000000001.</span></span>
>
> <span data-ttu-id="73c38-178">**BŪSENA**</span><span class="sxs-lookup"><span data-stu-id="73c38-178">**STATUS**</span></span>  
> <span data-ttu-id="73c38-179">Aktyvi</span><span class="sxs-lookup"><span data-stu-id="73c38-179">Active</span></span>
>
> <span data-ttu-id="73c38-180">Atidaryti išsamią bangos informaciją</span><span class="sxs-lookup"><span data-stu-id="73c38-180">Open wave details</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
