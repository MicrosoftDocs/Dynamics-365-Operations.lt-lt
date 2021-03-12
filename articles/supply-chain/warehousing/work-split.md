---
title: Darbo skaidymas
description: Šiame temoje paaiškinama informacija apie darbo atskyrimo funkciją. Ši funkcija leidžia jums atskirti didelius darbo užsakymus į keletą mažesnių darbo užsakymų, kuriuos galite tuomet priskirti keliems sandėlio darbuotojų. Tokiu būdu tas pats darbas gali būti paimamas vienu metu kelių sandėlio darbuotojų.
author: mirzaab
manager: tfehr
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8a530f3887c3c66295177d480a8c486dd0984153
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965532"
---
# <a name="work-split"></a><span data-ttu-id="3f3d8-105">Darbo skaidymas</span><span class="sxs-lookup"><span data-stu-id="3f3d8-105">Work split</span></span>

<span data-ttu-id="3f3d8-106">Darbo atskyrimo funkcija leidžia jums atskirti didelio darbo ID (tai reiškia, darbo užsakymus su keliomis linijomis) į keletą mažesnių darbo ID ir tuomet priskirti juos keliems sandėlio darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-106">Work split functionality lets you split large work IDs (that is, work orders that have several lines) into several smaller work IDs that you can then assign to multiple warehouse workers.</span></span> <span data-ttu-id="3f3d8-107">Tokiu būdu tas pats darbas sukūrimo numeris gali būti paimamas vienu metu kelių sandėlio darbuotojų.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-107">In this way, the same work creation number can be picked simultaneously by several warehouse workers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3f3d8-108">Galite išskirti keletą darbo užsakymų, kurie turi būseną *Atviras* ar *Vykdomas*.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-108">You can split only work orders that have a status of *Open* or *In-progress*.</span></span>

## <a name="turn-on-the-work-split-functionality"></a><span data-ttu-id="3f3d8-109">Įjunkite darbo atskyrimo funkciją</span><span class="sxs-lookup"><span data-stu-id="3f3d8-109">Turn on the work split functionality</span></span>

<span data-ttu-id="3f3d8-110">Prieš tai, kai galėsite naudoti darbo atskyrimo funkciją, turite įjungti funkciją ir būtinųjų sąlygių funkcijų savo sistemoje.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-110">Before you can use the work split functionality, you must turn on the feature and its prerequisite feature in your system.</span></span> <span data-ttu-id="3f3d8-111">Administratoriai gali naudoti [funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) nustatymus tam, kad patikrintų funkcijų būseną ir jas įjungtų kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-111">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on as required.</span></span>

<span data-ttu-id="3f3d8-112">Pirmiausia įjunkite būtinąsias sąlygas *Organizacijos sklaidos darbo blokavimo* funkciją, jei ji dar nėra įjungta.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-112">First, turn on the prerequisite *Organization-wide work blocking* feature if it isn't already turned on.</span></span> <span data-ttu-id="3f3d8-113">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-113">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="3f3d8-114">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="3f3d8-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="3f3d8-115">**Funkcijos pavadinimas:** *Organizacijos sklaidos darbo blokavimas*</span><span class="sxs-lookup"><span data-stu-id="3f3d8-115">**Feature name:** *Organization-wide work blocking*</span></span>

> [!NOTE]
> <span data-ttu-id="3f3d8-116">Įjungus šią funkciją, duomenų pagerinamas yra automatiškai taikomos įjungus funkciją visuose juridiniuose asmenyse.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-116">When this feature is activated, a data upgrade is automatically applied after the feature is turned on across all legal entities.</span></span>

<span data-ttu-id="3f3d8-117">Toliau, įjunkite *Darbo atskyrimo* funkciją, kuri yra įrašyta tolesne tvarka:</span><span class="sxs-lookup"><span data-stu-id="3f3d8-117">Next, turn on the *Work split* feature, which is listed in the following way:</span></span>

- <span data-ttu-id="3f3d8-118">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="3f3d8-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="3f3d8-119">**Funkcijos pavadinimas:** *Darbo atskyrimas*</span><span class="sxs-lookup"><span data-stu-id="3f3d8-119">**Feature name:** *Work split*</span></span>

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a><span data-ttu-id="3f3d8-120">Darbo išsamios informacijos pagerinimas ir Visi darbo puslapiai</span><span class="sxs-lookup"><span data-stu-id="3f3d8-120">Enhancements to the Work details and All work pages</span></span>

<span data-ttu-id="3f3d8-121">*Darbo atskyrimo* funkcija įtraukia tolesnius du mygtukus į **Darbo** skirtuką veiksmų juostoje **Darbo išsamioje informacijoje** ir **Visų darbų** puslapyse:</span><span class="sxs-lookup"><span data-stu-id="3f3d8-121">The *Work split* feature adds the following two buttons to the **Work** tab on the Action Pane of the **Work details** and **All work** pages:</span></span>

- <span data-ttu-id="3f3d8-122">**Atskyrimo darbas** – Atskirkite esamo darbo ID į keletą mažesnių darbų ID, kurie gali būti tvarkomi atskirų darbuotojų.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-122">**Split work** – Split the current work ID into multiple smaller work IDs that can be processed by separate workers.</span></span>
- <span data-ttu-id="3f3d8-123">**Atšaukite darbo atskyrimo seansą** – Atšaukite darbo atskyrimo seansą ir padarykite darbą prieinamą tvarkymui.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-123">**Cancel work split session** – Cancel the work split session, and make the work available for processing.</span></span>

<span data-ttu-id="3f3d8-124">![Atskyrimo darbas ir Atšaukimo darbo atskyrimo seanso mygtukai](media/Work_split_buttons.png "Atskyrimo darbas ir Atšaukimo darbo atskyrimo seanso mygtukai")</span><span class="sxs-lookup"><span data-stu-id="3f3d8-124">![Split work and Cancel work split session buttons](media/Work_split_buttons.png "Split work and Cancel work split session buttons")</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3f3d8-125">**Atskyrimo darbo** mygtukas nebus prieinamas, jei nebus patenkintos tolesnės sąlygos:</span><span class="sxs-lookup"><span data-stu-id="3f3d8-125">The **Split work** button won't be available if any of the following conditions are met:</span></span>
>
> - <span data-ttu-id="3f3d8-126">Darbo būsena yra kas kita, o ne *Atvira* ar *Vykdoma*.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-126">The work status is something other than *Open* or *In progress*.</span></span>
> - <span data-ttu-id="3f3d8-127">Talpyklos ID yra susietas su darbo ID.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-127">A container ID is associated with the work ID.</span></span> <span data-ttu-id="3f3d8-128">(Talpykla negali būti sistemiškai atskiriama, nes jai reikia fizinių veiksmų.)</span><span class="sxs-lookup"><span data-stu-id="3f3d8-128">(A container can't be systematically split, because it requires physical actions.)</span></span>
> - <span data-ttu-id="3f3d8-129">Darbas yra susietas su klasteriu.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-129">The work is associated with a cluster.</span></span>
> - <span data-ttu-id="3f3d8-130">Darbo užsakymo tipas yra kas kita, o ne vienas iš tolesnių tipų:</span><span class="sxs-lookup"><span data-stu-id="3f3d8-130">The work order type is something other than one of the following types:</span></span>
>
>    - <span data-ttu-id="3f3d8-131">Pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="3f3d8-131">Sales orders</span></span>
>    - <span data-ttu-id="3f3d8-132">Žaliavų paėmimas</span><span class="sxs-lookup"><span data-stu-id="3f3d8-132">Raw material picking</span></span>
>    - <span data-ttu-id="3f3d8-133">Perkėlimo išdavimas</span><span class="sxs-lookup"><span data-stu-id="3f3d8-133">Transfer issue</span></span>
>
> - <span data-ttu-id="3f3d8-134">Darbą šiuo metu atskiria kitas vartotojas.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-134">The work is currently being split by another user.</span></span> <span data-ttu-id="3f3d8-135">Jei bandote atverti atskyrimo langą darbui, kurį jau atskiria kitas vartotojas, gausite šį klaidos pranešimą: „Darbas su ID \#\#\#\# šiuo metu atskiriamas.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-135">If you try to open the splitting page for work that is already being split by another user, you receive the following error message: "The work with ID \#\#\#\# is currently being split.</span></span> <span data-ttu-id="3f3d8-136">Bandykite po kelių minučių.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-136">Retry in a few minutes.</span></span> <span data-ttu-id="3f3d8-137">Jei ir toliau gaunate šį pranešimą, susisiekite su vadovu."</span><span class="sxs-lookup"><span data-stu-id="3f3d8-137">If you continue to receive this message, contact a supervisor."</span></span>

<span data-ttu-id="3f3d8-138">Nauja darbo blokavimo priežastis, *Atskirti darbą*, rodomas, kai darbo ID yra atskyrimo procese.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-138">A new work blocking reason, *Split work*, indicates when the work ID is in the process of being split.</span></span> <span data-ttu-id="3f3d8-139">Jis rodomas tiek **Atskirti darbą** puslapyje ir sandėlio programoje, jei vartotojas bando vykdyti darbą.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-139">It's shown both on the **Split work** page and in the warehouse app if a user tries to run the work.</span></span> <span data-ttu-id="3f3d8-140">Kai blokavimo priežastys yra naudojamos, **Blokuota bangos** laukelio pavadinimas iš darbo ID yra pakeistas į **Blokuotas**.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-140">When blocking reasons are used, the name of the **Blocked wave** field from the work ID is changed to **Blocked**.</span></span>

## <a name="initiate-a-work-split"></a><span data-ttu-id="3f3d8-141">Pradėkite darbo atskyrimą</span><span class="sxs-lookup"><span data-stu-id="3f3d8-141">Initiate a work split</span></span>

<span data-ttu-id="3f3d8-142">Funkcija įtraukia naują **Atskyrimo darbo** puslapį, kuris leidžia vartotojams atskirti darbų linijas nuo darbo ID.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-142">The feature adds a new **Split work** page that lets users split work lines from the work ID.</span></span> <span data-ttu-id="3f3d8-143">Kai puslapis pirmą kartą atveriamas, jis rodo eilutes, kurios turi darbo būseną *Atvira* ir jei jos parengtos atskyrimui.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-143">When the page is first opened, it shows lines that have a work status of *Open* and that are available to be split.</span></span> <span data-ttu-id="3f3d8-144">Veiksmų juostoje pasirinkite **Atskirti darbą** tam, kad apdorotumėte pasirinktą darbą.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-144">On the Action Pane, select **Split work** to process the selected work.</span></span>

<span data-ttu-id="3f3d8-145">Norėdami atskirti darbą atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-145">To split work, follow these steps.</span></span>

1. <span data-ttu-id="3f3d8-146">Atverkite vieną iš tolesnių darbo langų:</span><span class="sxs-lookup"><span data-stu-id="3f3d8-146">Open one of the following work pages:</span></span>

    - <span data-ttu-id="3f3d8-147">**Darbo išsami informacija** (**Sandėlio valdymas \> Darbas \> Išsami darbo informacija**)</span><span class="sxs-lookup"><span data-stu-id="3f3d8-147">**Work details** (**Warehouse management \> Work \> Work details**)</span></span>
    - <span data-ttu-id="3f3d8-148">**Visi darbai** (**Sandėlio valdymas \> Darbas \> Visi darbai**)</span><span class="sxs-lookup"><span data-stu-id="3f3d8-148">**All work** (**Warehouse management \> Work \> All work**)</span></span>

1. <span data-ttu-id="3f3d8-149">Tinklelyje pasirinkite darbo ID atskyrimui.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-149">In the grid, select a work ID to split.</span></span> <span data-ttu-id="3f3d8-150">**Darbo užsakymo tipas** laukelis turi būti nustatytas viena iš tolesnių verčių:</span><span class="sxs-lookup"><span data-stu-id="3f3d8-150">The **Work order type** field must be set to one of the following values:</span></span>

    - <span data-ttu-id="3f3d8-151">Pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="3f3d8-151">Sales orders</span></span>
    - <span data-ttu-id="3f3d8-152">Žaliavų paėmimas</span><span class="sxs-lookup"><span data-stu-id="3f3d8-152">Raw material picking</span></span>
    - <span data-ttu-id="3f3d8-153">Perkėlimo išdavimas</span><span class="sxs-lookup"><span data-stu-id="3f3d8-153">Transfer issue</span></span>

1. <span data-ttu-id="3f3d8-154">Veiksmų juostoje pasirinkite **Darbo** skirtuką **Darbo** grupėje, pasirinkite **Atskirti darbą**.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-154">On the Action Pane, on the **Work** tab, in the **Work** group, select **Split work**.</span></span>

    <span data-ttu-id="3f3d8-155">**Atskirti darbą** puslapis pasirodo ir rodo darbo eilutes, kurios yra atvertos ir gali būti atskirtos.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-155">The **Split work** page appears and shows the work lines that are open and available to be split.</span></span> <span data-ttu-id="3f3d8-156">Pagal nutylėjimą, tik prieinamos darbo eilutės yra rodomos.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-156">By default, only available work lines are shown.</span></span> <span data-ttu-id="3f3d8-157">Norėdami peržiūrėti visas eilutes darbo ID (pavyzdžiui, eilutes, kurių darbo tipas yra *Padėti*), pasirinkite **Rodyti visas eilutes** žymimą laukelį virš tinklelio.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-157">To view all lines for the work ID (for example, lines that have a work type of *Put*), select the **Show all lines** check box above the grid.</span></span>

    <span data-ttu-id="3f3d8-158">Rodomas tolesnis pranešimas:„Vartotojai negali apdoroti darbo eilučių, kol nepabaigėte atskyrimo ir neuždarėte šio puslapio."</span><span class="sxs-lookup"><span data-stu-id="3f3d8-158">The following message is shown: "Users can't process lines of the work until you finish splitting and close this page."</span></span>

    <span data-ttu-id="3f3d8-159">**Darbo blokavimo priežastis** laukelis esamam darbui bus nustatytas į *Atskirti darbą* ir darbas bus užblokuotas.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-159">The **Work blocking reason** field for the current work will be set to *Split work*, and the work will be blocked.</span></span>

    <span data-ttu-id="3f3d8-160">![Blokavimo priežastis](media/Blocking_reason.png "Blokavimo priežastis")</span><span class="sxs-lookup"><span data-stu-id="3f3d8-160">![Blocking reason](media/Blocking_reason.png "Blocking reason")</span></span>

1. <span data-ttu-id="3f3d8-161">Pasirinkite eilutes, kad pašalintumėte iš esamo darbo ID ir įtrauktumėte naują darbo ID.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-161">Select the lines to remove from the current work ID and add to a new work ID.</span></span> <span data-ttu-id="3f3d8-162">Atistinka šis įvykis:</span><span class="sxs-lookup"><span data-stu-id="3f3d8-162">The following events occur:</span></span>

    - <span data-ttu-id="3f3d8-163">Jums atskyrus darbą, pasirinkta eilutė ar eilutės iš originalaus darbo ID yra atšaukiamos ir tuomet nukopijuojamos į naują darbo ID.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-163">When you split the work, the selected line or lines from the original work ID are canceled and then copied to a new work ID.</span></span>
    - <span data-ttu-id="3f3d8-164">Esanti darbo šablono struktūra ir padėjimo vieta (taip pat ateities padėjimo/paėmimo poros) yra užrezervuojamos iš anksto.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-164">The existing work template structure and the location of the put (and also future pick/put pairs) are preserved.</span></span> <span data-ttu-id="3f3d8-165">Tolesnio darbo ID laukelių vertės yra nukopijuojamos iš originalaus darbo į naują:</span><span class="sxs-lookup"><span data-stu-id="3f3d8-165">Values for the following work ID fields are copied from the original work to the new work:</span></span>

        - <span data-ttu-id="3f3d8-166">Krovinio ID</span><span class="sxs-lookup"><span data-stu-id="3f3d8-166">Load ID</span></span>
        - <span data-ttu-id="3f3d8-167">Siuntos ID</span><span class="sxs-lookup"><span data-stu-id="3f3d8-167">Shipment ID</span></span>
        - <span data-ttu-id="3f3d8-168">Darbo užsakymo tipas</span><span class="sxs-lookup"><span data-stu-id="3f3d8-168">Work order type</span></span>
        - <span data-ttu-id="3f3d8-169">Užsakymo numeris</span><span class="sxs-lookup"><span data-stu-id="3f3d8-169">Order number</span></span>
        - <span data-ttu-id="3f3d8-170">Vieta</span><span class="sxs-lookup"><span data-stu-id="3f3d8-170">Site</span></span>
        - <span data-ttu-id="3f3d8-171">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="3f3d8-171">Warehouse</span></span>
        - <span data-ttu-id="3f3d8-172">Darbo prioritetas</span><span class="sxs-lookup"><span data-stu-id="3f3d8-172">Work priority</span></span>
        - <span data-ttu-id="3f3d8-173">Darbo telkinio ID</span><span class="sxs-lookup"><span data-stu-id="3f3d8-173">Work pool ID</span></span>
        - <span data-ttu-id="3f3d8-174">Bangos ID</span><span class="sxs-lookup"><span data-stu-id="3f3d8-174">Wave ID</span></span>
        - <span data-ttu-id="3f3d8-175">Darbo sukūrimo numeris</span><span class="sxs-lookup"><span data-stu-id="3f3d8-175">Work creation number</span></span>

    - <span data-ttu-id="3f3d8-176">Tolesni laukeliai nenukopijuojami į naują darbo ID:</span><span class="sxs-lookup"><span data-stu-id="3f3d8-176">The following fields aren't copied to the new work ID:</span></span>

        - <span data-ttu-id="3f3d8-177">**Darbo ID** – Naujas darbo ID yra sukuriamas pagal atitinkamą skaičių seką.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-177">**Work ID** – A new work ID is generated from the appropriate number sequence.</span></span>
        - <span data-ttu-id="3f3d8-178">**Darbo būsena** – Šis laukelis nustatytas į *Atviras*.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-178">**Work status** – This field is set to *Open*.</span></span>
        - <span data-ttu-id="3f3d8-179">**Užrakino** – Šis laukelis pagal nutylėjimą nustatytas tuščias.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-179">**Locked by** – This field is initially set to blank.</span></span>
        - <span data-ttu-id="3f3d8-180">**Tikslinės licencijos lentelės ID** – Šis laukelis paliekamas tuščias.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-180">**Target license plate ID** – This field is left blank.</span></span>
        - <span data-ttu-id="3f3d8-181">**Sukūrimo data ir valanda** – Šis laukelis nustatytas esamai datai ir laikui rodyti.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-181">**Created date and time** – This field is set to the current date and time.</span></span>
        - <span data-ttu-id="3f3d8-182">**Užblokuota/užšaldyta banga** – Šis laukelis yra iš naujo suprojektuojamas originaliam darbo ID ir naujam darbo ID.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-182">**Blocked wave/frozen** – This field is recomputed for the original work ID and the new work ID.</span></span>

1. <span data-ttu-id="3f3d8-183">Veiksmų juosoje rinkitės **Atskirti darbą**.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-183">On the Action Pane, select **Split work**.</span></span>

<span data-ttu-id="3f3d8-184">Darbo atskyrimo metu, rodomas tolesnis pranešimas: „Apdorojimo operacija - Atskirti darbą“.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-184">While the work is being split, the following message is shown: "Processing operation - Split work".</span></span> <span data-ttu-id="3f3d8-185">Kai šis pranešimas matomas, galite atšaukti operaciją pasirinkę **Atšaukti** pranešimo laukelyje.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-185">While this message is visible, you can cancel the operation by selecting **Cancel** in the message box.</span></span>

<span data-ttu-id="3f3d8-186">Jei **Rodyti visas eilutes** žymimas laukelis yra atžymimas, atskirta ir atšaukta eilutės nebebus rodoma tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-186">If the **Show all lines** check box is cleared, the line that was split off and canceled will no longer appear in the grid.</span></span> <span data-ttu-id="3f3d8-187">Jei žymimas laukelis yra pasirinktas, turėtumėte matyti **Darbo būsenos** laukelio vertę tai eilutei, kuri buvo pakeista į *Atšaukta*.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-187">If the check box is selected, you should see that the value of the **Work status** field for that line has changed to *Canceled*.</span></span>

<span data-ttu-id="3f3d8-188">Tolesnis pranešimas yra rodomas siekiant parodyti, kad naujas darbo ID buvo sukurtas: „Darbas \#\#\#\# buvo sukurtas atskiriant nuo originalaus darbo \#\#\#\#."</span><span class="sxs-lookup"><span data-stu-id="3f3d8-188">The following notification is shown to indicate that the new work ID has been created: "Work \#\#\#\# has been created by splitting off from original work \#\#\#\#."</span></span>

<span data-ttu-id="3f3d8-189">Kitos darbo eilutės nuo originalaus darbo ID (toks kaip *Padėti* eilutės) buvo pataisytos kaip būtina tam, kad atsipindėtų atšauktas darbo eilutes.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-189">Other work lines from the original work ID (such as *Put* lines) will be adjusted as required to reflect the lines of work that have been canceled.</span></span> <span data-ttu-id="3f3d8-190">Pavyzdžiui, jei originalaus darbo ID *Padėti* eilutė 15 kiekiui ir *Paėmimo* eilutės, kurių bendras kiekis yra 10 buvo atšauktos, naujas *Padėjimo* kiekis originalaus darbo ID dabar bus 5.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-190">For example, if the original work ID had a *Put* line for a quantity of 15, and *Pick* lines that have a total quantity of 10 were canceled, the new *Put* quantity on the original work ID will now be 5.</span></span>

<span data-ttu-id="3f3d8-191">Naujas darbas nebus nedelsiant priskirtas bet kuriam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-191">The new work won't immediately be assigned to any user.</span></span> <span data-ttu-id="3f3d8-192">Nepaisant to, galite priskirti jį dabar vartotojui kaip reikia naudodami standartinę funkciją **Darbo išsamios informacijos** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-192">However, you can assign it to a user now, as required, by using the standard functionality of the **Work details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3f3d8-193">Galite atskirti tik darbo ID, kurie turi du ar daugiau esamų darbo eilučių.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-193">You can split only work IDs that contain two or more available work lines.</span></span> <span data-ttu-id="3f3d8-194">Jei pasirenkate **Atskirti darbą** kai yra tik viena darbo eilutė, gausite tolesnį klaidos pranešimą: „Mažiausiai viena darbo eilutė turi likti pradiniame darbe."</span><span class="sxs-lookup"><span data-stu-id="3f3d8-194">If you select **Split work** when there is only one work line, you will receive the following error message: "At least one work line must remain on initial work."</span></span> <span data-ttu-id="3f3d8-195">Tokiu atveju, atskyrimas neįvyks.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-195">In this case, no splitting will occur.</span></span>

## <a name="finish-a-work-split"></a><span data-ttu-id="3f3d8-196">Pabaikite darbo atskyrimą</span><span class="sxs-lookup"><span data-stu-id="3f3d8-196">Finish a work split</span></span>

<span data-ttu-id="3f3d8-197">Norėdami pabaigti darbo atskyrimą, *Atskirti darbą* blokavimo priežastis turi būti pašalinta.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-197">To finish splitting work, the *Split work* blocking reason must be removed.</span></span> <span data-ttu-id="3f3d8-198">Yra du būdai atlikti šį žingsnį:</span><span class="sxs-lookup"><span data-stu-id="3f3d8-198">There are two ways to complete this step:</span></span>

- <span data-ttu-id="3f3d8-199">Darbą atskiriantis darbuotojas užveria **Atskirti darbą** puslapį pasirinkdamas **Užverti** mygtuką (**X**) viršutiniame dešiniame kampe.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-199">The user who is splitting the work closes the **Split work** page by selecting the **Close** button (**X**) in the upper-right corner.</span></span> <span data-ttu-id="3f3d8-200">Uždarius puslapį, *Atskirti darbą* blokavimo priežastis bus panaikinta.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-200">When the page is closed, the *Split Work* blocking reason will be removed.</span></span> <span data-ttu-id="3f3d8-201">*Blokavimo* būsena šiam darbui bus parengta iš naujo ir jei nebėra daugiau blokavimo priežasčių jam. darbas bus atblokuotas.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-201">The *Blocked* state of this work will be recomputed and, if there are no remaining blocking reasons for this work, the work will be unblocked.</span></span>
- <span data-ttu-id="3f3d8-202">Bet kuri vartotojas atidaro darbo ID ir pasirenka **Atšaukti darbo atskyrimo seansą** mygtuką veiksmų juostoje.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-202">Any user opens the work ID and selects the **Cancel work split session** button on the Action Pane.</span></span> <span data-ttu-id="3f3d8-203">Taigi *Atskirti darbą* vlokavimo priežastis bus panaikinta ir *Blokavimo* būsena šiam darbui bus parengta iš naujo, kai tik **Atskirti darbą** langas bus užvertas.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-203">The *Split work* blocking reason will be removed, and the *Blocked* state of this work will be recomputed, just as when the **Split work** page is closed.</span></span>

<span data-ttu-id="3f3d8-204">Po to, kai *Atskirti darbą* blokavimo priežastis yra panaikinta, darbas gali vykti mobiliame įrenginyje su sąlyga, kad **Blokuotas** būsena yra nustatyta į *Ne* darbo ID.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-204">After the *Split work* blocking reason is removed, the work can be run on the mobile device, provided that the **Blocked** state is set to *No* on the work ID.</span></span>

## <a name="user-blocking-on-the-warehouse-app"></a><span data-ttu-id="3f3d8-205">Vartotojo blokavimas sandėlio programoje</span><span class="sxs-lookup"><span data-stu-id="3f3d8-205">User blocking on the warehouse app</span></span>

<span data-ttu-id="3f3d8-206">Jei bandote naudoti sandėlio programą, kad vykdytumėte paėmimo darbą pagal atskiriamą darbo ID, gausite tolesnį klaidos pranešimą: „Darbas su ID  \#\#\#\# šiuo metu atskiriamas."</span><span class="sxs-lookup"><span data-stu-id="3f3d8-206">If you try to use the warehouse app to run picking work against a work ID that is being split, you will receive the following error message: "The work with ID \#\#\#\# is currently being split."</span></span> <span data-ttu-id="3f3d8-207">Jei gaunate šį pranešimą, pasirinkite **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-207">If you receive this message, select **Cancel**.</span></span> <span data-ttu-id="3f3d8-208">Tuomet galite tęsti šio darbo apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="3f3d8-208">You can then continue to process other work.</span></span>

## <a name="other-blocked-operations"></a><span data-ttu-id="3f3d8-209">Kitos užblokuotos operacijos</span><span class="sxs-lookup"><span data-stu-id="3f3d8-209">Other blocked operations</span></span>

<span data-ttu-id="3f3d8-210">Bet kurios operacijos, kurios keičia darbo eilutes, darbo inventoriaus perdavimus ar papildymo nuoradas, kurios susijusios su atskiriamu darbu neveiks ir bus rodomas tolesnis klaidos pranešimas : „Darbas su ID \#\#\#\# šiuo metu yra atskiriamas."</span><span class="sxs-lookup"><span data-stu-id="3f3d8-210">Any operations that modify work lines, work inventory transactions, or replenishment links that are related to work that is being split will fail, and the following error message will be shown: "The work with ID \#\#\#\# is currently being split."</span></span>
