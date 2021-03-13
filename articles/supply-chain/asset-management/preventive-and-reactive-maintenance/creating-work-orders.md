---
title: Darbo užsakymų kūrimas
description: Šioje temoje aiškinama, kaip sukurti darbo užsakymus turto valdyme.
author: johanhoffmann
manager: tfehr
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 876aef9f3f470490bb385e1861c837dcfa82db69
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131798"
---
# <a name="creating-work-orders"></a><span data-ttu-id="c2fc0-103">Darbo užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="c2fc0-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c2fc0-104">Suplanavus prevencines priežiūros užduotis, kitas žingsnis yra sukurti jų darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="c2fc0-105">Šį veiksmą atlikti galite naudodami vieną iš priežiūros grafikų.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="c2fc0-106">Suplanuotos užduotys priežiūros grafike gali turėti skirtingus nuorodos numerius, kaip apibūdinta šioje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="c2fc0-107">Nuorodos tipas</span><span class="sxs-lookup"><span data-stu-id="c2fc0-107">Reference type</span></span> | <span data-ttu-id="c2fc0-108">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="c2fc0-108">Description</span></span> |
|---|---|
| <span data-ttu-id="c2fc0-109">Priežiūros planai</span><span class="sxs-lookup"><span data-stu-id="c2fc0-109">Maintenance plans</span></span> | <span data-ttu-id="c2fc0-110">Prevencinės priežiūros užduotys, pagrįstos *Laikas* arba *Skaitiklis* priežiūros plano tipu.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="c2fc0-111">Priežiūros ciklai</span><span class="sxs-lookup"><span data-stu-id="c2fc0-111">Maintenance rounds</span></span> | <span data-ttu-id="c2fc0-112">Prevencinės priežiūros užduotys, turinčios kelis turtus, kuriems reikia atlikti panašaus tipo priežiūrą.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="c2fc0-113">Priežiūros užklausa</span><span class="sxs-lookup"><span data-stu-id="c2fc0-113">Maintenance request</span></span> | <span data-ttu-id="c2fc0-114">Rankiniu būdu sukurta turto priežiūros ar atkūrimo užklausa.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="c2fc0-115">Šią užklausą galima konvertuoti į darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="c2fc0-116">Darbo užsakymų, remiantis jūsų priežiūros grafiku, kūrimas</span><span class="sxs-lookup"><span data-stu-id="c2fc0-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="c2fc0-117">Norėdami sukurti darbo užsakymus pagal jūsų priežiūros grafiką, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="c2fc0-118">Atidarykite vieną iš šių puslapių, atsižvelgiant į tai, kaip norite pasirinkti jūsų darbo užsakymų grafiko elementus:</span><span class="sxs-lookup"><span data-stu-id="c2fc0-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="c2fc0-119">Visi priežiūros grafikai (**Turto valdymas \> Valdymo grafikas \> Visi priežiūros grafikai**)</span><span class="sxs-lookup"><span data-stu-id="c2fc0-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="c2fc0-120">Atviros priežiūros grafiko eilutės (**Turto valdymas \> Valdymo grafikas \> Atviros priežiūros grafiko eilutės**)</span><span class="sxs-lookup"><span data-stu-id="c2fc0-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="c2fc0-121">Atviri priežiūros grafiko telkiniai (**Turto valdymas \> Valdymo grafikas \> Atviri priežiūros grafiko telkiniai**)</span><span class="sxs-lookup"><span data-stu-id="c2fc0-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="c2fc0-122">Tinklelyje pažymėkite žymės langelį kiekvienai suplanuotai priežiūros užduočiai, kuriai norite sukurti darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="c2fc0-123">Tada veiksmų srityje pasirinkite **Darbo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="c2fc0-124">Atsiranda **Kurti darbo užsakymus** dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="c2fc0-125">Lauke **Priežiūros prognozės valandos** rodomas bendras prognozuojamų valandų skaičius pasirinktoms eilutėms.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![Dialogo langas Kurti darbo užsakymus](media/18-preventive-maintenance.png)

1. <span data-ttu-id="c2fc0-127">Skyriuje **Parametrai** nurodykite skaičių darbo užsakymų, kurie turi būti sukurti.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="c2fc0-128">Pasirinkite vieną iš toliau pateiktų pasirinkčių:</span><span class="sxs-lookup"><span data-stu-id="c2fc0-128">Select one of the following options:</span></span>

    - <span data-ttu-id="c2fc0-129">**Vienas darbo užsakymas vienai eilutei** – Kurkite vieną darbo užsakymą vienai priežiūros grafiko eilutei.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="c2fc0-130">**Vienas darbo užsakymas pagal** – Kurkite darbo užsakymus, sugrupuotus pagal kitų parinkčių, kurios tampa galimos pasirinkus šią parinktį, nustatymus.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="c2fc0-131">Lauke **Darbo užsakymo tipas** pasirinkite darbo užsakymo tipą, kuris bus naudojamas visiems jūsų kuriamiems darbo užsakymams.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="c2fc0-132">Pasirinkite **Gerai** darbo užsakymų kūrimui pagal savo parametrus.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="c2fc0-133">Darbo užsakymo eilučių, sukuriamų automatiškai priežiūros plano vykdymo metu, grupavimas</span><span class="sxs-lookup"><span data-stu-id="c2fc0-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2fc0-134">Šiame skyriuje aprašytos funkcijos yra galimos kaip peržiūros versijos leidimo dalis.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-134">The functionality that is described in this section is available as part of a preview release.</span></span> <span data-ttu-id="c2fc0-135">Turinys ir funkcijos gali būti keičiami.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-135">The content and the functionality are subject to change.</span></span> <span data-ttu-id="c2fc0-136">Norėdami apie peržiūros leidimus gauti daugiau informacijos, žr. [DUK apie vienos versijos paslaugų naujinimus](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).</span><span class="sxs-lookup"><span data-stu-id="c2fc0-136">For more information about preview releases, see [One version service updates FAQ](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).</span></span>

<span data-ttu-id="c2fc0-137">Ši funkcija leidžia jums nustatyti darbo užsakymo eilučių grupavimo pagal vieną darbo užsakymą taisykles, kai sistema yra nustatyta generuoti darbo užsakymus automatiškai, atsižvelgiant į priežiūros planą.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-137">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="c2fc0-138">Anksčiau automatiškai sugeneruotuose darbo užsakymuose galėjo būti tik viena eilutė.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-138">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="c2fc0-139">Tačiau dabar galite grupuoti darbo užsakymus pagal, pavyzdžiui, turtą, turto tipą ar funkcinę vietą.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-139">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="c2fc0-140">(Rankiniu būdu sugeneruotus darbo užsakymus tokiu būdų jau buvo galima grupuoti, kaip aprašyta ankstesniame šios temos skyriuje.)</span><span class="sxs-lookup"><span data-stu-id="c2fc0-140">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="c2fc0-141">Automatiškai sugeneruotų darbo užsakymų grupavimo įgalinimas</span><span class="sxs-lookup"><span data-stu-id="c2fc0-141">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="c2fc0-142">Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-142">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="c2fc0-143">Administratoriai gali naudoti [funkcijos valdymas](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-143">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="c2fc0-144">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-144">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c2fc0-145">**Modulis:** *Turto valdymas*</span><span class="sxs-lookup"><span data-stu-id="c2fc0-145">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="c2fc0-146">**Funkcijos pavadinimas:** *(Peržiūros versija) Taikyti darbo užsakymų grupavimo taisykles vykdant priežiūros planą*</span><span class="sxs-lookup"><span data-stu-id="c2fc0-146">**Feature name:** *(Preview) Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="c2fc0-147">Automatiškai sugeneruotų darbo užsakymų grupavimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="c2fc0-147">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="c2fc0-148">Norėdami nustatyti automatiškai sugeneruotų darbo užsakymų grupavimą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-148">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="c2fc0-149">Eikite į **Turto valdymas \> Sąranka \> Prevencinė priežiūra \> Priežiūros planai**.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-149">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="c2fc0-150">Kiekvienam planui, kuriame norite generuoti sugrupuotus darbo užsakymus, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="c2fc0-150">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="c2fc0-151">Pasirinkite planą iš sąrašo srities.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-151">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="c2fc0-152">„FastTab” **Eilutės** įsitikinkite, kad žymės langelis **Automatinis kūrimas** yra pažymėtas kiekvienoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-152">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="c2fc0-153">Eikite į **Turto valdymas \> Laikotarpio \> Prevencinė priežiūra \> Planuoti priežiūros planus**.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-153">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="c2fc0-154">Dialogo lango **Planuoti priežiūros planus** skyriuje **Laikotarpis** nurodykite plano laiko perspektyvas (kaip toli žvelgti į ateitį ieškant suplanuotų priežiūros užduočių, kurioms generuoti darbą).</span><span class="sxs-lookup"><span data-stu-id="c2fc0-154">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="c2fc0-155">Nustatykite parinktį **Automatiškai kurti darbo užsakymą iš grafiko** į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-155">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="c2fc0-156">Skyriuje **Darbo užsakymas** pasirinkite vieną iš šių parinkčių:</span><span class="sxs-lookup"><span data-stu-id="c2fc0-156">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="c2fc0-157">**Vienas darbo užsakymas vienai eilutei** – Kurkite vieną darbo užsakymą vienai priežiūros grafiko eilutei.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-157">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="c2fc0-158">(Ši parinktis suteikia tas pačias funkcijas, kurios galimos, kai išjungta *Taikyti darbo užsakymų grupavimo taisykles, kai vykdomas priežiūros planas* funkcija.)</span><span class="sxs-lookup"><span data-stu-id="c2fc0-158">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="c2fc0-159">**Vienas darbo užsakymas pagal** – Kurkite darbo užsakymus, sugrupuotus pagal kitų parinkčių, kurios tampa galimos pasirinkus šią parinktį, nustatymus.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-159">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="c2fc0-160">Jei norite, kad parinktys būtų taikomos vykdant tik kai kuriuos jūsų priežiūros planus, „FastTab” **Įtrauktini įrašai** pridėkite tiek filtrų, kiek jums reikia, kaip ir kitose „Microsoft Dynamics 365 Supply Chain Management” paketinėse užduotyse.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-160">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="c2fc0-161">„FastTab” **Vykdyti fone** nustatykite paketo ir planavimo parinktis taip, kaip jums reikia, kaip ir kitoms „Supply Chain Management” paketinėms užduotims.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-161">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="c2fc0-162">Pasirinkite **Gerai** tam, kad būtų vykdomi ir (arba) suplanuoti pasirinkti priežiūros planai.</span><span class="sxs-lookup"><span data-stu-id="c2fc0-162">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>
