---
title: Neautomatiniu būdu sukurti darbo užsakymai
description: Šioje temoje paaiškinta, kaip kurti darbo užsakymą rankiniu būdu skiltyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875797"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="a1e8f-103">Neautomatiniu būdu sukurti darbo užsakymai</span><span class="sxs-lookup"><span data-stu-id="a1e8f-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="a1e8f-104">Galite kurti darbo užsakymus rankiniu būdu dviem būdais:</span><span class="sxs-lookup"><span data-stu-id="a1e8f-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="a1e8f-105">Skiltyje **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**</span><span class="sxs-lookup"><span data-stu-id="a1e8f-105">in **All work orders** or **Active work orders**</span></span>  
- <span data-ttu-id="a1e8f-106">Skiltyje **Visos priežiūros užklausos** arba **Aktyviosios priežiūros užklausos**, arba **Mano funkcinės vietos priežiūros užklausos**</span><span class="sxs-lookup"><span data-stu-id="a1e8f-106">in **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests**</span></span>  

## <a name="create-work-order"></a><span data-ttu-id="a1e8f-107">Kurti darbo užsakymą</span><span class="sxs-lookup"><span data-stu-id="a1e8f-107">Create work order</span></span>

1. <span data-ttu-id="a1e8f-108">Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="a1e8f-109">Spustelėkite mygtuką **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-109">Click the **New** button.</span></span>

3. <span data-ttu-id="a1e8f-110">Išplečiamajame meniu **Sukurti darbo užsakymą** pasirinkite darbo užsakymo tipą.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-110">In the **Create work order** drop-down, select a work order type.</span></span>

4. <span data-ttu-id="a1e8f-111">Jei reikia, pasirinkite aprašą.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-111">If required, select a description.</span></span>

5. <span data-ttu-id="a1e8f-112">Pasirinkite darbo užsakymo turtą bei priežiūros užduoties tipą.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-112">Select the asset for the work order as well as a maintenance job type.</span></span>

>[!NOTE]
><span data-ttu-id="a1e8f-113">Pasirinkus turtą galimi trys skirtukai: skirtuke **Mano turtas** nurodomas turtas, susijęs su funkcine vieta, į kurią jūs (prisijungęs į sistemą darbuotojas) galite būti paskirtas (sąranka aprašoma [Priežiūros darbuotojai ir darbo grupės](../setup-for-objects/workers-and-worker-groups.md)).</span><span class="sxs-lookup"><span data-stu-id="a1e8f-113">When you select an asset, three tabs may be available: The **My assets** tab contains assets related to the functional locations to which you (the worker who is logged on the system) may be allocated (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)).</span></span> <span data-ttu-id="a1e8f-114">Jei darbuotojui nėra nurodyta funkcinė vieta skiltyje [Priežiūros darbuotojai ir darbo grupės](../setup-for-objects/workers-and-worker-groups.md), skirtukas **Mano turtas** nebus rodomas.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-114">If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab will not be visible.</span></span> <span data-ttu-id="a1e8f-115">Skirtuke **Aktyvus turtas** yra viso turto, kurio turto ciklo būsena „Aktyvi“, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-115">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="a1e8f-116">Skirtuke **Turto rodinys** rodomas funkcinių vietų ir tose vietose įdiegto turto medžio rodinys.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-116">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="a1e8f-117">Jei reikia, pasirinkite **Priežiūros užduoties tipo variantas** ir **Prekybos šaka**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-117">If required, select **Maintenance job type variant** and **Trade**.</span></span>

7. <span data-ttu-id="a1e8f-118">Jei reikia, galite keisti darbo užsakymo aptarnavimo lygį lauke **Aptarnavimo lygis**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-118">If required, you can change the work order service level in the **Service level** field.</span></span>

8. <span data-ttu-id="a1e8f-119">Susijusiuose laukuose pasirinkite numatomas pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-119">Select expected start and end dates in the related fields.</span></span>

9. <span data-ttu-id="a1e8f-120">Spustelėkite **Gerai**, kad sukurtumėte naują darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-120">Click **OK** to create a new work order.</span></span>

10. <span data-ttu-id="a1e8f-121">Redaguokite, jei reikia, darbo užsakymą, pasirinkę **Visi darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-121">Edit the work order in **All work orders**, if required.</span></span>

- <span data-ttu-id="a1e8f-122">Pasirinkę **Visi darbo užsakymai** galite pridėti prie darbo užsakymo kelis turtus Išsamios informacijos rodinyje įterpdami eilutes į „FastTab“ **Darbo užsakymų priežiūros užduotys**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-122">In **All work orders**, You can add several assets to a work order in Details view by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="a1e8f-123">Turtui galite pasirinkti tik tuos priežiūros užduoties tipus, kurie yra nurodyti turto tipe konkrečiam turtui.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-123">On an asset, you can only select the maintenance job types that are defined on the asset type selected for the asset.</span></span>  
- <span data-ttu-id="a1e8f-124">Jei pakeitėte turto aptarnavimo lygį arba turto kritiškumą, po to, kai panaudojote jį darbo užsakyme (žr. [Turto aptarnavimo lygiai](../setup-for-objects/object-priorities.md) ir [Turto kritiškumas](../setup-for-objects/object-criticalities.md)), darbo užsakymo aptarnavimo lygis arba kritiškumas atitinkamai nėra naujinami.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-124">If you have changed an asset service level or an asset criticality after you have used them on a work order (refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md)), the service level or criticality on the work order is not updated accordingly.</span></span>
- <span data-ttu-id="a1e8f-125">Darbo užsakymo kritiškumas yra perskaičiuojamas kiekvienąkart, kai darbo užsakymo eilutė yra įterpiama arba pašalinama tame darbo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-125">Criticality on a work order is re-calculated each time a work order line is added or deleted on the work order.</span></span>
- <span data-ttu-id="a1e8f-126">Išsamios informacijos rodinyje **Visi darbo užsakymai** > rodinyje **Antraštė** > „FastTab“ **Grafikas** galite pasirinkti atsakingą priežiūros darbo grupę arba atsakingą priežiūros darbuotoją laukuose **Atsakinga grupė** arba **Atsakingas**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-126">In **All work orders** Details view > **Header** view > **Schedule** FastTab, you can select a responsible maintenance worker group or a responsible maintenance worker in the **Responsible group** or **Responsible** fields.</span></span> <span data-ttu-id="a1e8f-127">Šie parametrai gali būti keičiami tol, kol darbo užsakymas yra aktyvus, pavyzdžiui, kai darbo užsakymo ciklo būsena pakinta.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-127">These settings can be changed as long as the work order is active, for example, when the work order lifecycle state changes.</span></span> <span data-ttu-id="a1e8f-128">Automatinė atranka, vykdoma kuriant darbo užsakymą, yra grindžiama sąranka, esančia **Atsakingi priežiūros darbuotojai**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-128">The automatic selection made during work order creation is based on the setup in **Responsible maintenance workers**.</span></span> <span data-ttu-id="a1e8f-129">Jei pridėsite arba pašalinsite darbo užsakymo užduotis po to, kai sukūrėte darbo užsakymą, o atnaujinus darbo užsakymą laukai **Atsakinga grupė** ir **Atsakingas**, Turto valdyme bus ieškomos galimos atitiktys sąrankos formoje, skirtoje nurodyti atsakingą priežiūros darbo grupę arba atsakingą priežiūros darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-129">If you add or remove work order jobs after you have created a work order, and the **Responsible group** field and the **Responsible** field are blank when you update the work order, Asset Management searches for a possible match in the setup form for a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="a1e8f-130">Jei atnaujinus darbo užsakymą laukas **Atsakinga grupė** arba laukas **Atsakingas** jau yra užpildyti, pakeitimai nėra vykdomi.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-130">If the **Responsible group** field or the **Responsible** field is already filled out when you update the work order, no changes are made.</span></span> 

- <span data-ttu-id="a1e8f-131">Skiltyje **Priežiūros būsena** galite vykdyti skaičiavimus, kuriuos atlikus bus suformuojama darbo krūvio, susijusio su gaunamais ir baigtais darbo užsakymais, apžvalga.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-131">In **Maintenance status**, you can make a calculation to get an overview of workload regarding incoming and completed work orders.</span></span>  

- <span data-ttu-id="a1e8f-132">„FastTab“ **Eilutės išsami informacija** naudokite laukus **Platuma** ir **Ilguma** įterpti geografines koordinates turtui, pasirinktam darbo užsakymo užduočiai.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-132">On the **Line details** FastTab, use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset selected on the work order job.</span></span>  

## <a name="create-related-work-order"></a><span data-ttu-id="a1e8f-133">Kurti susijusį darbo užsakymą</span><span class="sxs-lookup"><span data-stu-id="a1e8f-133">Create related work order</span></span>

<span data-ttu-id="a1e8f-134">Galite sukurti susijusį darbo užsakymą esamam darbo užsakymui, pavyzdžiui, jei norite dirbti su pagrindiniais ir antriniais darbo užsakymais.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-134">You can create a related work order to an existing work order if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="a1e8f-135">Naujas darbo užsakymas yra kuriamas pagal darbo užsakymo užduotį iš esamo darbo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-135">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="a1e8f-136">Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-136">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="a1e8f-137">Pažymėkite darbo užsakymą, kuriam norite sukurti susijusį darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-137">Select the work order for which you want to make a related work order.</span></span>

3. <span data-ttu-id="a1e8f-138">Spustelėkite **Susijęs darbo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-138">Click **Related work order**.</span></span>

4. <span data-ttu-id="a1e8f-139">Išplečiamajame dialogo lange **Sukurti susijusį darbo užsakymą** pasirinkite darbo užsakymo užduotį, kuriai norite sukurti susijusį darbo užsakymą lauke **Darbo užsakymo užduotis**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-139">In the **Create related work order** drop-down dialog, select the work order job for which you want to create a related work order in the **Work order job** field.</span></span>

5. <span data-ttu-id="a1e8f-140">Pasirinkite priežiūros užduoties tipą lauke **Priežiūros užduoties tipas** ir, jei reikia, susijusį priežiūros užduoties tipo variantą ir prekybos šaką laukuose **Priežiūros užduoties tipo variantas** ir **Prekybos šaka**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-140">Select a maintenance job type in the **Maintenance job type** field and, if required, a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields.</span></span>

6. <span data-ttu-id="a1e8f-141">Jei tai pirmas susijęs darbo užsakymas, kurį kursite, spustelėkite išrinkimo mygtuką **Naujas darbo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-141">If this is the first related work order you make, click the **New work order** radio button.</span></span>

7. <span data-ttu-id="a1e8f-142">Susijusiuose laukuose pasirinkite **Darbo užsakymo tipas** ir **Aprašas**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-142">Select a **Work order type** and a **Description** in the related fields.</span></span>

8. <span data-ttu-id="a1e8f-143">Prireikus keiskite darbo užsakymo aptarnavimo lygį lauke **Aptarnavimo lygis**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-143">If required, change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="a1e8f-144">Įterpkite numatomas pradžios ir pabaigos datas susijusiuose laukuose.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-144">Insert expected start and end dates in the related fields.</span></span>

10. <span data-ttu-id="a1e8f-145">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-145">Click **OK**.</span></span> <span data-ttu-id="a1e8f-146">Naujai sukurtas susijęs darbo užsakymas bus rodomas sąraše **Visi darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-146">The new related work order is shown in the **All work orders** list.</span></span>

11. <span data-ttu-id="a1e8f-147">Jei kursite susijusį darbo užsakymą darbo užsakymui, kuris jau turi susijusių darbo užsakymų, galėsite įterpti darbo užsakymo užduotį jau esančiam susijusiam darbo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-147">If you create a related work order on a work order that already has related work orders, you can add the work order job to an already related work order.</span></span> <span data-ttu-id="a1e8f-148">Tai galite atlikti spustelėjus išrinkimo mygtuką **Pridėti prie darbo užsakymo** 6 etape.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-148">This is done by clicking the **Add to related work order** radio button in step 6.</span></span> <span data-ttu-id="a1e8f-149">Tada pažymėkite susijusį darbo užsakymą, kuriam norite pridėti naują darbo užsakymo užduotį.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-149">Then you select the related work order to which you want to add a new work order job.</span></span> <span data-ttu-id="a1e8f-150">Redaguokite kiek reikia laukus **Aptarnavimo lygis**, **Numatoma pradžia** ir **Numatoma pabaiga**, ir spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-150">Edit the **Service level**, **Expected start**, and **Expected end** fields, as required, and click **OK**.</span></span> <span data-ttu-id="a1e8f-151">Darbo užsakymo užduotis pridedama prie esamo susijusio darbo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-151">The work order job is added to the existing related work order.</span></span>


![1 pav.](media/03-work-orders.png)

<span data-ttu-id="a1e8f-153">**Pastaba.** Jei nustatėte susijusio darbo šabloną **Turto valdymo parametrai** > **Darbo užsakymai** nuorodoje > **Susijusio darbo užsakymo šablonas** lauke, darbo užsakymo ID bus sukuriami pagal šablono sąranką.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-153">**Note:** If you have set up a related work order mask in **Asset management parameters** > **Work orders** link > **Related work order mask** field, work order IDs will be created in accordance with the mask setup.</span></span> <span data-ttu-id="a1e8f-154">Jei nėra nurodytas joks susijusio darbo užsakymo šablonas, kitas pasiekiamas darbo užsakymo ID bus naudojamas susijusiems darbo užsakymams.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-154">If no related work order mask is set up, the next available work order ID will be used for related work orders.</span></span>

## <a name="copy-work-order"></a><span data-ttu-id="a1e8f-155">Kopijuoti darbo užsakymą</span><span class="sxs-lookup"><span data-stu-id="a1e8f-155">Copy work order</span></span>

<span data-ttu-id="a1e8f-156">Galima greitai sukurti naują darbo užsakymą iš esamo darbo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-156">It is possible to quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="a1e8f-157">Toks darbo užsakymų tvarkymas skiriasi nuo darbo užsakymų kūrimo pagal priežiūros planus.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-157">This way of working with work orders is different from creating work orders based on maintenance plans.</span></span> <span data-ttu-id="a1e8f-158">Tai naudinga, pavyzdžiui, jei turite darbo užsakymą, kuriame yra daug darbo užsakymo užduočių su skirtingomis užduotimis, skirtomis skirtingam turtui, ir jos turi būti atliktos reguliariais intervalais.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-158">It is useful if, for example, you have a work order containing many work order jobs with various jobs on different assets that should be completed at regular intervals.</span></span>

1. <span data-ttu-id="a1e8f-159">Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-159">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="a1e8f-160">Pasirinkite darbo užsakymą, iš kurio norite nukopijuoti turinį.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-160">Select the work order from which you want to copy content.</span></span>

3. <span data-ttu-id="a1e8f-161">Spustelėkite **Kopijuoti darbo užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-161">Click **Copy work order**.</span></span> <span data-ttu-id="a1e8f-162">Rodoma darbo užsakymo sąranka iš pasirinkto darbo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-162">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="a1e8f-163">Prireikus galite redaguoti kai kuriuos laukus.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-163">If required, you can edit some of the fields.</span></span>

4. <span data-ttu-id="a1e8f-164">Spustelėkite **Gerai**, kad sukurtumėte naują darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-164">Click **OK** to create the new work order.</span></span>

5. <span data-ttu-id="a1e8f-165">Redaguokite, jei reikia, darbo užsakymą, pasirinkę **Visi darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-165">Edit the work order in **All work orders**, if required.</span></span>

>[!NOTE]
><span data-ttu-id="a1e8f-166">Kai sukuriamas naujas darbo užsakymas, dalis informacijos yra nukopijuojama tiesiai iš esamo darbo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-166">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="a1e8f-167">Tokia informacija kaip prognozės, įrankiai, priežiūros kontroliniai sąrašai, funkcinė vieta, adresai ir planavimas nėra kopijuojama, bet pradedama kurti iš esamos sąrankos Turto valdyme.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-167">Information regarding forecasts, tools, maintenance checklists, functional location, addresses, and scheduling is not copied, but initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="a1e8f-168">Tai reiškia, jog, jei buvo įvykdyti pakeitimai tuose duomenyse sukūrus pirmą darbo užsakymą ir, iki kol padarėte darbo užsakymo kopiją, tie pakeitimai išliks naujai sukurtame darbo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-168">This means that if changes were made in those data from the time of creation of the first work order until the time you made a copy of the work order, those changes are included in the new work order you have created.</span></span> <span data-ttu-id="a1e8f-169">Pavyzdžiai – prognozių arba atnaujintų prižiūrimo turto kontrolinių sąrašų pakeitimai.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-169">Examples are changes in forecasts or updated maintenance checklists.</span></span>


![2 paveikslėlis](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="a1e8f-171">Sukurkite darbo užsakymą pagal priežiūros užklausą</span><span class="sxs-lookup"><span data-stu-id="a1e8f-171">Create work order based on a maintenance request</span></span>

1. <span data-ttu-id="a1e8f-172">Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Priežiūros užklausos** > **Visos priežiūros užklausos** arba **Aktyviosios priežiūros užklausos**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-172">Click **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="a1e8f-173">Pasirinkite priežiūros užklausą, kuriai norite sukurti darbo užsakymą, ir spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-173">Select the maintenance request for which you want to create a work order, and click **Edit**.</span></span>

3. <span data-ttu-id="a1e8f-174">Skiltyje **Visos užklausos** spustelėkite **Darbo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-174">In **All requests**, click **Work order**.</span></span>

4. <span data-ttu-id="a1e8f-175">Užpildykite išplečiamąjį sąrašą **Darbo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-175">Fill out the **Work order** drop-down.</span></span> <span data-ttu-id="a1e8f-176">Jei priežiūros užduoties tipas buvo pasirinktas priežiūros užklausoje, jei pageidaujate, galite pasirinkti kitą priežiūros užduoties tipą, kai kuriate darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-176">If a maintenance job type has been selected in the maintenance request, you are able to select another maintenance job type, if required, when you create the work order.</span></span>

5. <span data-ttu-id="a1e8f-177">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-177">Click **OK**.</span></span> <span data-ttu-id="a1e8f-178">Bus rodomas pranešimas, kuriame informuojama apie sukurtą darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-178">You will see a message informing you that the work order has been created.</span></span>

6. <span data-ttu-id="a1e8f-179">Jei norite matyti, kurie darbo užsakymai yra susieti su priežiūros užklausa, pasirinkite priežiūros užklausą iš sąrašų **Visos priežiūros užklausos** arba**Aktyvios priežiūros užklausos** ir spustelėkite mygtuką **Darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-179">If you want to see which work orders are connected to a maintenance request, select the maintenance request in the **All maintenance requests** or **Active maintenance requests** lists, and click the **Work orders** button.</span></span>


![3 paveikslėlis](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="a1e8f-181">Darbo užsakymai gali būti sukurti automatiškai, planuojant priežiūros planų užduotis arba nustatant turtui „Kurti automatiškai“ priežiūros planus arba priežiūros ciklus.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-181">Work orders can also be created automatically by scheduling maintenance plan jobs, or by setting up "Auto create" maintenance plans or maintenance rounds on an asset.</span></span> <span data-ttu-id="a1e8f-182">Darbo užsakymai, sukurti pagal priežiūros užklausas ir nurodomi skiltyje**Priežiūros grafikas**, kuriami nurodant priežiūros užduoties tipus, pasirinktus priežiūros užklausose.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-182">Work orders created from maintenance requests in **Maintenance schedule** are created with the maintenance job types selected in the maintenance requests.</span></span>

