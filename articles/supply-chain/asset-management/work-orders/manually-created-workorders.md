---
title: Neautomatiniu būdu sukurti darbo užsakymai
description: Šioje temoje paaiškinta, kaip kurti darbo užsakymą rankiniu būdu skiltyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8c787dbc9889139df76b9b102deb18fce567e382
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017873"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="aa4c8-103">Neautomatiniu būdu sukurti darbo užsakymai</span><span class="sxs-lookup"><span data-stu-id="aa4c8-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="aa4c8-104">Galite kurti darbo užsakymus rankiniu būdu dviem būdais:</span><span class="sxs-lookup"><span data-stu-id="aa4c8-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="aa4c8-105">Puslapyje **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**</span><span class="sxs-lookup"><span data-stu-id="aa4c8-105">On the **All work orders** or **Active work orders** page</span></span> 
- <span data-ttu-id="aa4c8-106">Puslapyje **Visos priežiūros užklausos** arba **Aktyviosios priežiūros užklausos**, arba **Mano funkcinės vietos priežiūros užklausos**</span><span class="sxs-lookup"><span data-stu-id="aa4c8-106">On the **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests** page</span></span> 

## <a name="create-work-order"></a><span data-ttu-id="aa4c8-107">Kurti darbo užsakymą</span><span class="sxs-lookup"><span data-stu-id="aa4c8-107">Create work order</span></span>

1. <span data-ttu-id="aa4c8-108">Pasirinkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-108">Selece **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="aa4c8-109">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-109">Select **New**.</span></span>

3. <span data-ttu-id="aa4c8-110">Dialogo lange **Kurti darbo užsakymą**, lauke **Darbo užsakymo tipas**, pasirinkite darbo užsakymo tipą.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-110">In the **Create work order** dialog, select a work order type in the **Work order type** field.</span></span>

4. <span data-ttu-id="aa4c8-111">Jei reikia, pasirinkite **aprašymą**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-111">If required, select a **Description**.</span></span>

5. <span data-ttu-id="aa4c8-112">Lauke **Turtas** pasirinkite turtą.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-112">In the **Asset** field, select the asset.</span></span>

>[!NOTE]
><span data-ttu-id="aa4c8-113">Pasirinkus turtą, išplečiamajame meniu **Turtas** gali būti galimi trys toliau pateikti skirtukai.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-113">When you select an asset, three tabs might be available in the **Asset** drop-down:</span></span> 

- <span data-ttu-id="aa4c8-114">**Aktyvus turtas**: šiame skirtuke yra viso turto, kurio turto ciklo būsena „Aktyvi“, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-114">**Active assets** - This tab contains a list of all assets that have an "Active" asset lifecycle state.</span></span> 
- <span data-ttu-id="aa4c8-115">**Turto rodinys**: šiame skirtuke rodomas funkcinių vietų ir jose įdiegto turto medžio rodinys.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-115">**Asset view** - This tab displays a tree view of functional locations and the assets installed on them.</span></span>
- <span data-ttu-id="aa4c8-116">**Mano turtas**: šiame skirtuke yra turtas, susijęs su funkcinėmis vietomis, į kurias jūs (darbuotojas, prisijungęs prie sistemos) galite būti priskirtas.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-116">**My assets** - This tab contains assets that are related to the functional locations that you (the worker who is signed in to the system) may be allocated to.</span></span> <span data-ttu-id="aa4c8-117">(Norėdami gauti informacijos apie nustatymą, žr. [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md).) Jei darbuotojui nėra priskirtų funkcinių vietų skiltyje [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md), skirtukas **Mano turtas** negalimas.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-117">(For information about the setup, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).) If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab isn't available.</span></span> 

6. <span data-ttu-id="aa4c8-118">Lauke **Priežiūros užduoties tipas** pasirinkite darbo užsakymo priežiūros užduoties tipą.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-118">In the **Maintenance job type** field, select a maintenance job type for the work order.</span></span>

7. <span data-ttu-id="aa4c8-119">Jei reikia, pasirinkite **Priežiūros užduoties tipo variantas** ir **Prekybos šaka**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-119">If required, select **Maintenance job type variant** and **Trade**.</span></span>

8. <span data-ttu-id="aa4c8-120">Jei reikia, galite keisti darbo užsakymo aptarnavimo lygį lauke **Aptarnavimo lygis**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-120">If required, you can change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="aa4c8-121">Susijusiuose laukuose pasirinkite **numatomas pradžios** ir **numatomas pabaigos** datas.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-121">Select **Expected start** and **Expected end** dates in the related fields.</span></span>

10. <span data-ttu-id="aa4c8-122">Spustelėkite **Gerai**, kad sukurtumėte darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-122">Click **OK** to create the work order.</span></span>

11. <span data-ttu-id="aa4c8-123">Sąrašo puslapyje **Visi darbo užsakymai** galite pagal poreikį redaguoti darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-123">On the **All work orders** list page, you can edit the work order as you require.</span></span>

<span data-ttu-id="aa4c8-124">Atkreipkite dėmesį į toliau nurodytus punktus.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-124">Note the following points:</span></span>

- <span data-ttu-id="aa4c8-125">Sąrašo puslapio **Visi darbo užsakymai** išsamios informacijos rodinyje galite pridėti kelis turtus prie darbo užsakymo įterpdami eilutes į „FastTab“ **Darbo užsakymų priežiūros užduotys**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-125">In the details view on the **All work orders** list page, you can add several assets to a work order by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="aa4c8-126">Turtui galite pasirinkti tik tuos priežiūros užduoties tipus, kurie yra nurodyti turto tipe konkrečiam turtui.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-126">On an asset, you can select only the maintenance job types that are defined on the asset type that is selected on the asset.</span></span>  

- <span data-ttu-id="aa4c8-127">Jei pakeisite turto aptarnavimo lygį ar turto kritiškumą po to, kai naudojote turtą darbo užsakyme, šio darbo užsakymo aptarnavimo lygis ar kritiškumas nebus atitinkamai atnaujintas.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-127">If you change an asset service level or an asset criticality after you've used the asset on a work order, the service level or criticality on the work order isn't updated accordingly.</span></span> <span data-ttu-id="aa4c8-128">Daugiau informacijos apie aptarnavimo lygius ir kritiškumus žr. [Turto aptarnavimo lygiai](../setup-for-objects/object-priorities.md) ir [Turto svarbos tipai](../setup-for-objects/object-criticalities.md).</span><span class="sxs-lookup"><span data-stu-id="aa4c8-128">For more information about service levels and criticalities, see [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticality types](../setup-for-objects/object-criticalities.md).</span></span>

- <span data-ttu-id="aa4c8-129">Darbo užsakymo kritiškumas iš naujo apskaičiuojamas kaskart, kai prie darbo užsakymo pridedama arba pašalinama darbo užsakymo užduotis.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-129">Criticality on a work order is recalculated every time a work order job is added to or deleted from the work order.</span></span>

- <span data-ttu-id="aa4c8-130">Išsamios informacijos rodinyje **Visi darbo užsakymai** > skirtuke **Antraštė** > „FastTab“ **Grafikas**, laukuose **Atsakinga grupė** arba **Atsakingas**, galite pasirinkti atsakingą priežiūros darbo grupę arba atsakingą priežiūros darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-130">In the **All work orders** details view > **Header** tab > **Schedule** FastTab, in the **Responsible group** or **Responsible** field, you can select a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="aa4c8-131">Šiuos parametrus galima keisti, kol darbo užsakymas yra aktyvus.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-131">These settings can be changed while the work order is active.</span></span> <span data-ttu-id="aa4c8-132">Pavyzdžiui, jas galima pakeisti, kai pasikeičia darbo užsakymo ciklo būsena.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-132">For example, they can be changed when the work order lifecycle state changes.</span></span> <span data-ttu-id="aa4c8-133">Automatinė atranka, vykdoma kuriant darbo užsakymą, yra grindžiama sąranka, esančia puslapyje **Atsakingi priežiūros darbuotojai**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-133">The automatic selection that is made during work order creation is based on the setup on the **Responsible maintenance workers** page.</span></span> <span data-ttu-id="aa4c8-134">Jei pridėsite arba pašalinsite darbo užsakymo užduotis po to, kai sukūrėte darbo užsakymą, o atnaujinus darbo užsakymą laukai **Atsakinga grupė** ir **Atsakingas** yra tušti, turto valdyme bus ieškomos galimos atitiktys sąrankos formoje, skirtoje nurodyti atsakingą priežiūros darbo grupę arba atsakingą priežiūros darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-134">If you add or remove work order jobs after you've created a work order, and if the **Responsible group** and **Responsible** fields are blank when you update the work order, Asset Management tries to find a responsible maintenance worker group or a responsible maintenance worker for a possible match on the setup page.</span></span> <span data-ttu-id="aa4c8-135">Jei atnaujinus darbo užsakymą laukai **Atsakinga grupė** arba **Atsakingas** jau yra nustatyti, pakeitimai nėra vykdomi.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-135">If the **Responsible group** or **Responsible** field is already set when you update the work order, no changes are made.</span></span> <span data-ttu-id="aa4c8-136">Daugiau informacijos apie už priežiūrą atsakingus darbuotojus ir darbuotojų grupes, rasite temoje [Atsakingi priežiūros darbuotojai](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="aa4c8-136">For more information about responsible maintenance workers and worker groups, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

- <span data-ttu-id="aa4c8-137">Puslapyje [Priežiūros būsena](../controlling-and-reporting/maintenance-status.md) galite vykdyti skaičiavimus, kuriuos atlikus bus suformuojama darbo krūvio, susijusio su gaunamais ir baigtais darbo užsakymais, apžvalga.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-137">From the [Maintenance status](../controlling-and-reporting/maintenance-status.md) page, you can do a calculation to get an overview of the workload for incoming and completed work orders.</span></span>  

- <span data-ttu-id="aa4c8-138">Puslapio **Visi darbo užsakymai** išsamios informacijos rodinyje, „FastTab” **Eilutės informacija**, galite naudoti laukus **Platuma** ir **Ilguma**, kad būtų galima pridėti darbo užsakymo užduoties pasirinkto turto geografines koordinates.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-138">In the details view of the **All work orders** page, on the **Line details** FastTab, you can use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset that is selected on the work order job.</span></span>  


## <a name="create-related-work-order"></a><span data-ttu-id="aa4c8-139">Kurti susijusį darbo užsakymą</span><span class="sxs-lookup"><span data-stu-id="aa4c8-139">Create related work order</span></span>

<span data-ttu-id="aa4c8-140">Galite sukurti darbo užsakymą, susijusį su esamu darbo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-140">You can create a work order that is related to an existing work order.</span></span> <span data-ttu-id="aa4c8-141">Ši galimybė naudinga jei, pavyzdžiui, norite dirbti su pirminiais ir antriniais darbo užsakymais.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-141">This capability is useful if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="aa4c8-142">Naujas darbo užsakymas yra kuriamas pagal darbo užsakymo užduotį iš esamo darbo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-142">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="aa4c8-143">Pasirinkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-143">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="aa4c8-144">Pasirinkite darbo užsakymą, kuriam kursite susijusį darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-144">Select the work order to create a related work order for.</span></span>

3. <span data-ttu-id="aa4c8-145">Veiksmų srities skirtuko **Darbo užsakymas** grupėje **Naujas** pasirinkite **Susijęs darbo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-145">On the Action Pane, on the **Work order** tab, in the **New** group, select **Related work order**.</span></span>

4. <span data-ttu-id="aa4c8-146">Dialogo lange **Kurti susijusį darbo užsakymą**, lauke **Darbo užsakymo užduotis**, pasirinkite darbo užsakymo užduotį, kuriai norite sukurti susijusį darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-146">In the **Create related work order** dialog, in the **Work order job** field, select the work order job to create a related work order for.</span></span>

5. <span data-ttu-id="aa4c8-147">Lauke **Priežiūros užduoties tipas** pasirinkite priežiūros užduoties tipą.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-147">Select a maintenance job type in the **Maintenance job type** field.</span></span>

6. <span data-ttu-id="aa4c8-148">Laukuose **Priežiūros užduoties tipo variantas** ir **Prekybos šaka** pasirinkite susijusios priežiūros užduoties tipo variantą ir prekybos šaką.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-148">Select a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields, as you require.</span></span>

7. <span data-ttu-id="aa4c8-149">Jei šis darbo užsakymas yra pirmas susijęs darbo užsakymas, sukurtas pasirinktam darbo užsakymui, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-149">If this work order is the first related work order that has been created for the selected work order, follow these steps:</span></span>
    1. <span data-ttu-id="aa4c8-150">Pasirinkite parinktį **Naujas darbo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-150">Select the **New work order** option.</span></span>
    2. <span data-ttu-id="aa4c8-151">Lauke **Darbo užsakymo tipas** pasirinkite darbo užsakymo tipą.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-151">In  the **Work order type** field, select a work order type.</span></span>
    3. <span data-ttu-id="aa4c8-152">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-152">In the **Description**, enter a description.</span></span>
    4. <span data-ttu-id="aa4c8-153">Pagal poreikį keiskite darbo užsakymo aptarnavimo lygį lauke **Aptarnavimo lygis**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-153">In the **Service level** field, change the work order service level as you require.</span></span>
    5. <span data-ttu-id="aa4c8-154">Laukuose **Numatoma pradžia** ir **Numatoma pabaiga** pasirinkite numatomas pradžios bei pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-154">In the **Expected start** and **Expected end** fields, select the expected start and end dates.</span></span>
    6. <span data-ttu-id="aa4c8-155">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-155">Select **OK**.</span></span> <span data-ttu-id="aa4c8-156">Naujai sukurtas susijęs darbo užsakymas bus rodomas sąrašo puslapyje **Visi darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-156">The new related work order is shown on the **All work orders** list page.</span></span>  

8. <span data-ttu-id="aa4c8-157">Jei darbo užsakymas, kuriam kuriate susijusį darbo užsakymą, jau turi susijusių darbo užsakymų, atlikite toliau pateiktus veiksmus, norėdami įtraukti naują darbo užsakymo užduotį į esamą susijusį darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-157">If the work order that you're creating this related work order for already has related work orders, follow these steps to add a new work order job to an existing related work order:</span></span>
    1. <span data-ttu-id="aa4c8-158">Pasirinkite parinktį **Įtraukti į susijusį darbo užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-158">Select the **Add to related work order** option.</span></span>
    2. <span data-ttu-id="aa4c8-159">Lauke **Darbo užsakymas** pažymėkite susijusį darbo užsakymą, kuriam norite pridėti naują darbo užsakymo užduotį.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-159">In the **Work order** field, select the related work order to add a new work order job to.</span></span>
    3. <span data-ttu-id="aa4c8-160">Pagal poreikį keiskite darbo užsakymo aptarnavimo lygį lauke **Aptarnavimo lygis**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-160">In the **Service level** field, change the work order service level as you require.</span></span>
    4. <span data-ttu-id="aa4c8-161">Laukuose **Numatoma pradžia** ir **Numatoma pabaiga** pagal poreikį pakeiskite numatomas pradžios bei pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-161">In the **Expected start** and **Expected end** fields, change the expected start and end dates as you require.</span></span>
    5. <span data-ttu-id="aa4c8-162">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-162">Select **OK**.</span></span> <span data-ttu-id="aa4c8-163">Darbo užsakymo užduotis pridedama prie esamo susijusio darbo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-163">The work order job is added to the existing related work order.</span></span>

<span data-ttu-id="aa4c8-164">Toliau pateiktame paveikslėlyje parodytas dialogo lango **Kurti susijusį darbo užsakymą** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-164">The illustration below shows an example of the **Create related work order** dialog.</span></span>

![1 pav.](media/03-work-orders.png)

>[!NOTE]
><span data-ttu-id="aa4c8-166">Jei nustatėte susijusio darbo šabloną **Turto valdymo parametrai** > skirtuke **Darbo užsakymai** > lauke **Susijusio darbo užsakymo šablonas**, darbo užsakymo ID bus sukuriami pagal šablono sąranką.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-166">If you've set up a related work order mask in **Asset management parameters** > **Work orders** tab > **Related work order mask** field, work order IDs are created according to the mask setup.</span></span> <span data-ttu-id="aa4c8-167">Jei nėra nurodytas joks susijusio darbo užsakymo šablonas, kitas pasiekiamas darbo užsakymo ID naudojamas susijusiems darbo užsakymams.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-167">If no related work order mask is set up, the next available work order ID is used for related work orders.</span></span>

## <a name="copy-a-work-order"></a><span data-ttu-id="aa4c8-168">Kopijuoti darbo užsakymą</span><span class="sxs-lookup"><span data-stu-id="aa4c8-168">Copy a work order</span></span>

<span data-ttu-id="aa4c8-169">Galite greitai sukurti naują darbo užsakymą iš esamo darbo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-169">You can quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="aa4c8-170">Toks darbo užsakymų tvarkymas skiriasi nuo darbo užsakymų kūrimo pagal [priežiūros planus](../preventive-and-reactive-maintenance/maintenance-plans.md).</span><span class="sxs-lookup"><span data-stu-id="aa4c8-170">This way of working with work orders differs from the creation of work orders based on [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md).</span></span> <span data-ttu-id="aa4c8-171">Tai naudinga, pavyzdžiui, jei darbo užsakyme yra daug darbo užsakymo užduočių ir skirtingos užduotys turi būti atliktos skirtingam turtui ir reguliariais intervalais.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-171">It's useful if, for example, a work order contains many work order jobs, and the various jobs should be completed on different assets at regular intervals.</span></span>

1. <span data-ttu-id="aa4c8-172">Pasirinkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-172">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="aa4c8-173">Pasirinkite darbo užsakymą, iš kurio norite nukopijuoti turinį.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-173">Select the work order to copy content from.</span></span>

3. <span data-ttu-id="aa4c8-174">Veiksmų srityje > skirtuke **Darbo užsakymas** > grupėje **Naujas**, pasirinkite **Kopijuoti darbo užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-174">On the Action Pane > **Work order** tab > **New** group, select **Copy work order**.</span></span>

4. <span data-ttu-id="aa4c8-175">Rodoma darbo užsakymo sąranka iš pasirinkto darbo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-175">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="aa4c8-176">Prireikus galite redaguoti kai kuriuos laukus.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-176">You can edit some of the fields as you require.</span></span>

5. <span data-ttu-id="aa4c8-177">Spustelėkite **Gerai**, kad sukurtumėte naują darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-177">Select **OK** to create the new work order.</span></span>

6. <span data-ttu-id="aa4c8-178">Sąrašo puslapyje **Visi darbo užsakymai** galite pagal poreikį redaguoti darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-178">On the **All work orders** list page, you can edit the work order as you require.</span></span>

>[!NOTE]
><span data-ttu-id="aa4c8-179">Kai sukuriamas naujas darbo užsakymas, dalis informacijos yra nukopijuojama tiesiai iš esamo darbo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-179">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="aa4c8-180">Informacija apie prognozes, įrankius, prižiūrimo turto kontrolinius sąrašus, funkcines vietas, adresus ir planavimą nėra kopijuojama.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-180">Information about forecasts, tools, maintenance checklists, functional location, addresses, and scheduling isn't copied.</span></span> <span data-ttu-id="aa4c8-181">Vietoje to, ji inicijuojama naudojant dabartinį nustatymą turto valdyme.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-181">Instead, it's initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="aa4c8-182">Todėl, jei ši informacija buvo pakeista nuo tada, kai buvo sukurtas pirmas darbo užsakymas, iki tada, kai buvo sukurta darbo užsakymo kopija, pakeitimai įtraukiami į naują darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-182">Therefore, if that information was changed between the time when the first work order was created and the time when you made a copy of the work order, the changes are included in the new work order.</span></span> <span data-ttu-id="aa4c8-183">Pavyzdžiai: prognozių pakeitimai ir prižiūrimo turto kontrolinių sąrašų naujinimai.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-183">Examples include changes to forecasts and updates to maintenance checklists.</span></span>

<span data-ttu-id="aa4c8-184">Toliau pateiktame paveikslėlyje parodytas dialogo lango **Kopijuoti darbo užsakymą** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-184">The illustration below shows an example of the **Copy work order** dialog.</span></span>

![2 pav.](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="aa4c8-186">Sukurkite darbo užsakymą pagal priežiūros užklausą</span><span class="sxs-lookup"><span data-stu-id="aa4c8-186">Create a work order based on a maintenance request</span></span>

1. <span data-ttu-id="aa4c8-187">Pasirinkite **Turto valdymas** > **Bendrieji dalykai** > **Priežiūros užklausos** > **Visos priežiūros užklausos** arba **Aktyviosios priežiūros užklausos**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-187">Select **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="aa4c8-188">Pasirinkite priežiūros užklausą, kuriai norite sukurti darbo užsakymą, ir spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-188">Select the maintenance request to create a work order for, and click **Edit**.</span></span>

3. <span data-ttu-id="aa4c8-189">Veiksmų srityje > skirtuke **Priežiūros užklausa** > grupėje **Naujas**, pasirinkite **Darbo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-189">On the Action Pane > **Maintenance request** tab > **New** group, select **Work order**.</span></span>

4. <span data-ttu-id="aa4c8-190">Dialogo lange **Darbo užsakymas** nustatykite laukus.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-190">In the **Work order** dialog, set the fields.</span></span> <span data-ttu-id="aa4c8-191">Jei priežiūros užduoties tipas buvo pasirinktas priežiūros užklausoje, jei pageidaujate, galite pasirinkti kitą priežiūros užduoties tipą, kai kuriate darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-191">If a maintenance job type has been selected in the maintenance request, you can select a different maintenance job type when you create the work order, as you require.</span></span>

5. <span data-ttu-id="aa4c8-192">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-192">Select **OK**.</span></span> <span data-ttu-id="aa4c8-193">Pranešimas informuoja, kad darbo užsakymas sukurtas.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-193">A message notifies you that the work order has been created.</span></span>

6. <span data-ttu-id="aa4c8-194">Jei norite peržiūrėti su priežiūros užklausa susietus darbo užsakymus, pasirinkite priežiūros užklausą sąrašo puslapiuose **Visos priežiūros užklausos** arba **Aktyvios priežiūros užklausos**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-194">To view the work orders that are connected to a maintenance request, on the **All maintenance requests** or **Active maintenance requests** list page, select the maintenance request.</span></span> <span data-ttu-id="aa4c8-195">Tada, veiksmų srityje, skirtuke **Priežiūros užklausa**, grupėje **Peržiūrėti**, pasirinkite **Darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-195">Then, on the Action Pane, on the **Maintenance request** tab, in the **View** group, select **Work orders**.</span></span>


<span data-ttu-id="aa4c8-196">Toliau pateiktame paveikslėlyje parodytas dialogo lango **Kurti darbo užsakymą** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-196">The illustration below shows an example of the **Create work order** dialog.</span></span>

![3 pav.](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="aa4c8-198">Jei norite, kad darbo užsakymai būtų sukurti automatiškai, tai galite padaryti planuojant priežiūros planų užduotis arba nustatant turtui „Kurti automatiškai“ [priežiūros planus](../preventive-and-reactive-maintenance/maintenance-plans.md) arba [priežiūros ciklus](../preventive-and-reactive-maintenance/maintenance-rounds.md).</span><span class="sxs-lookup"><span data-stu-id="aa4c8-198">If you want work orders to be created automatically, you can schedule maintenance plan jobs, or you can set up "Auto create" [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md) or [maintenance rounds](../preventive-and-reactive-maintenance/maintenance-rounds.md) on an asset.</span></span> <span data-ttu-id="aa4c8-199">Darbo užsakymų, sukurtų pagal priežiūros užklausas sąrašo puslapyje **Visas priežiūros grafikas**, priežiūros užduoties tipai pasirenkami priežiūros užklausose.</span><span class="sxs-lookup"><span data-stu-id="aa4c8-199">Work orders that are created from maintenance requests on the **All maintenance schedule** list page have the maintenance job types that are selected on the maintenance requests.</span></span>

