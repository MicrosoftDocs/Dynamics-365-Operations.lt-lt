---
title: Papildymo strategijos
description: Šiame skyriuje aprašyta informacija apie papildymo strategijas ir paaiškinta, kaip galite naudoti papildymo strategijos laukelį bangos paklausos papildymo šablono eilutės siekiant pasirinkti, kaip atliekamas papildymas.
author: mirzaab
manager: tfehr
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-29
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: a66d48c6636f9f2012c92945868728d8430c1cbe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256044"
---
# <a name="replenishment-strategies"></a><span data-ttu-id="2c9e1-103">Papildymo strategijos</span><span class="sxs-lookup"><span data-stu-id="2c9e1-103">Replenishment strategies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c9e1-104">Šablonai, kurie nustatyti **Papildymo šablonuose** puslapyje apima bangos paklausos papildymo šablono eilutes, leidžiančias jums pasirinkti, kaip papildymas atliekamas.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-104">The templates that are defined on the **Replenishment templates** page include wave demand replenishment template lines that let you select how replenishment is done.</span></span> <span data-ttu-id="2c9e1-105">Kiekviena eilutė apima **Papildymo strategijos** laukelį.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-105">Each line now includes a **Replenishment strategy** field.</span></span>

<span data-ttu-id="2c9e1-106">Strategija *Bangos paklausos kokybė* yra nustatytoji.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-106">The *Wave demand quantity* strategy is the default strategy.</span></span> <span data-ttu-id="2c9e1-107">Tai papildymo strategija naudojama anksčiau įžanogs **Papildymo strategijos** laukelyje.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-107">It's the replenishment strategy that was used before the introduction of the **Replenishment strategy** field.</span></span> <span data-ttu-id="2c9e1-108">Ji naudoja papildymo vietos kryptis, kad rastų papildytinas vietas.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-108">It uses the replenishment location directives to find locations that can be replenished.</span></span> <span data-ttu-id="2c9e1-109">Ji tada pildo tas vietas, kol paklausa bus padengta.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-109">It then replenishes those locations until the demand is covered.</span></span>

<span data-ttu-id="2c9e1-110">Strategija *Maksimali vietos talpa* pristato keletą naujų funkcijų.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-110">The *Maximum location capacity* strategy introduces some new functionality.</span></span> <span data-ttu-id="2c9e1-111">Kaip *Bangos paklausos kokybės* strategija ji naudoja papildymo vietos kryptis, kad rastų papildytinas vietas ir tada pildo jas iki kol padengs paklausą.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-111">Like the *Wave demand quantity* strategy, this strategy uses the replenishment location directives to find locations that can be replenished, and then it replenishes those locations until the demand is covered.</span></span> <span data-ttu-id="2c9e1-112">Jis skiriasi nuo *Bangos paklausos kiekio* strategijos, kurioje visos papildymo vietos yra pildomos iki jų maksimalios talpos kaip nustatyta vietos talpos apribojimuose.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-112">It differs from the *Wave demand quantity* strategy in that all the replenished locations are replenished to their maximum capacity, as defined by the location stocking limits.</span></span> <span data-ttu-id="2c9e1-113">Strategija *Maksimali vietos talpa* stengiasi sukurti darbą tam, kad paimtų šį būtiną kiekį, kartu su papildomu kiekiu ir užpildytų pildomas vietas.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-113">The *Maximum location capacity* strategy tries to create work to bring in the requested quantity, plus some extra quantity, to fill the locations that are being replenished.</span></span> <span data-ttu-id="2c9e1-114">Nepaisant to, kai kuriais atvejais tai nepavyksta.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-114">However, in some cases, that attempt might fail.</span></span> <span data-ttu-id="2c9e1-115">Pavyzdžiui, palaidos vietos gali neturėti pakankamai inventoriaus, kad padengtų papildomą kiekį.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-115">For example, the bulk locations might not have enough inventory to cover the extra quantity.</span></span> <span data-ttu-id="2c9e1-116">Tais atvejais, sistema aptinka problemą ir bando atkurti.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-116">In these cases, the system detects the failure and tries to recover.</span></span>

<span data-ttu-id="2c9e1-117">Piko seansas yra vienas pavyzdys, kai *Maksimali vietos talpos* strategija yra svarbesnė nei *Bangos paklausos kiekio* strategija.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-117">Peak season is one example of a situation where the *Maximum location capacity* strategy is preferable to the *Wave demand quantity* strategy.</span></span> <span data-ttu-id="2c9e1-118">Piko sezono metu, kai kurios prekės gali būti parduodamos dideliais kiekiais.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-118">During peak season, some items might be selling at high volume.</span></span> <span data-ttu-id="2c9e1-119">Dėl to, jums gali reikėti aktyviai pildyti atitinkamas paėmimo vietas kaip įmanoma labiau siekiant sumažinti darbo skaičiaus ID sukuriamą papildymo metu.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-119">Therefore, you might want to proactively replenish the relevant picking locations as much as possible, to reduce the number of work IDs that are created for replenishment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c9e1-120">Norėdami pasinaudoti visa *Maksimalios vietos talpos* strategija, turite nustatyti iš naujo talpos apribojimus atitinkamoms vietoms.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-120">To take full advantage of the *Maximum location capacity* strategy, you must redefine the stocking limits for the relevant locations.</span></span> <span data-ttu-id="2c9e1-121">Kitu atveju, ši strategija veiks kaip *Bangos paklausos kokybė* strategija.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-121">Otherwise, this strategy works just like the *Wave demand quantity* strategy.</span></span>

## <a name="turn-on-the-replenish-to-max-based-on-stocking-limits-feature"></a><span data-ttu-id="2c9e1-122">Įjunkite papildymą iki maksimalaus pagal talpos apribojimų funkciją</span><span class="sxs-lookup"><span data-stu-id="2c9e1-122">Turn on the Replenish to max based on stocking limits feature</span></span>

<span data-ttu-id="2c9e1-123">Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-123">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="2c9e1-124">Adminsitratoriai gali naudoti [Funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo erdvę tam, kad patikrintų funkcijos būseną ir ją įjungtų, jei jos reikia.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-124">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of this feature and turn it on if it's required.</span></span> <span data-ttu-id="2c9e1-125">Ten ši funkcija pateikiama taip:</span><span class="sxs-lookup"><span data-stu-id="2c9e1-125">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="2c9e1-126">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="2c9e1-126">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="2c9e1-127">**Funkcijos pavadinimas:** *Pildymas iki maksimalaus pagal talpos apribojimus*</span><span class="sxs-lookup"><span data-stu-id="2c9e1-127">**Feature name:** *Replenish to max based on stocking limits*</span></span>

## <a name="set-up-replenishment-strategies"></a><span data-ttu-id="2c9e1-128">Papildymo strategijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="2c9e1-128">Set up replenishment strategies</span></span>

<span data-ttu-id="2c9e1-129">Norėdami prieiti prie šablonų, eikite į **Sandėlio valdymas \> Nustatymai \> Pildymas \> Pildymo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-129">To access the templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span> <span data-ttu-id="2c9e1-130">Skyriuje **Peržiūra** pasirinkite ar sukurkite bangos paklausos papildymo šabloną, kuriame **Papildymo tipo** laukelis nustatytas į *Bangos paklausa*.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-130">In the **Overview** section, select or create a wave demand replenishment template where the **Replenishment type** field is set to *Wave demand*.</span></span> <span data-ttu-id="2c9e1-131">Tuomet nustatykite papildymo šablono eilutes **Papildymo šablono išsami informacija** skyriuje.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-131">Then set up the replenishment template lines in the **Replenishment template details** section.</span></span> <span data-ttu-id="2c9e1-132">Kiekvienai eilutei **Papildymo strategijos** laukelyje pasirinkite papildymo strategiją, kurią norite naudoti.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-132">For each line, in the **Replenishment strategy** field, select the replenishment strategy that you want to use.</span></span>

<span data-ttu-id="2c9e1-133">![Papildymo šablonų puslapis](media/ReplenTempWaveDmdMaxLocCap.png "Papildymo šablonų puslapis")</span><span class="sxs-lookup"><span data-stu-id="2c9e1-133">![Replenishment templates page](media/ReplenTempWaveDmdMaxLocCap.png "Replenishment templates page")</span></span>

<span data-ttu-id="2c9e1-134">Jei **Papildymo strategijos** stulpelis nepasirodo tinklelyje **Papildymo šablono išsamios informacijos** skyriuje, įsitikinkite, kad funkcija buvo įjungta ir kad pasirinktas papildymo šablonas turi papildymo tipą *Bangos paklausa*.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-134">If the **Replenishment strategy** column doesn't appear in the grid in the **Replenishment template details** section, make sure that the feature has been turned on, and that the selected replenishment template has a replenishment type of *Wave demand*.</span></span>

> [!NOTE]
> <span data-ttu-id="2c9e1-135">Strategija *Bangos paklausos kokybė* yra nustatytoji.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-135">The *Wave demand quantity* strategy is the default strategy.</span></span> <span data-ttu-id="2c9e1-136">Dėl to, turite tik naujinti papildymo šablono eilutes, kuriose norite naudoti *Maksimalio vietos talpos* strategiją vietoje kitos.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-136">Therefore, you just have to update the replenishment template lines where you want to use the *Maximum location capacity* strategy instead.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="2c9e1-137">Scenarijų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="2c9e1-137">Example scenarios</span></span>

### <a name="example-1"></a><span data-ttu-id="2c9e1-138">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="2c9e1-138">Example 1</span></span>

<span data-ttu-id="2c9e1-139">Šiame pavyzdyje yrar tik vienas papildymo šablonas, kuris turi vieną šablono eilutę.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-139">For this example, there is only one replenishment template that has only one replenishment template line.</span></span>

<span data-ttu-id="2c9e1-140">Sukuriate prekybos užsakymą 130 vienetams (vnt) prekei A0001.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-140">You create a sales order for 130 pieces (pcs) of item A0001.</span></span> <span data-ttu-id="2c9e1-141">Prieš jums išleidžiant užsakymą į sandėlį, jis nustatytas tokiu būdu:</span><span class="sxs-lookup"><span data-stu-id="2c9e1-141">Before you release the order to the warehouse, the warehouse is set up in the following way:</span></span>

- <span data-ttu-id="2c9e1-142">Yra tik viena bendra vieta ir joje yra 500 vnt esančio turimo inventoriaus.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-142">There is only one bulk location, and it has 500 pcs of available on-hand inventory.</span></span>
- <span data-ttu-id="2c9e1-143">Yra trys paėmimo vietos, kurių kiekvienoje kiekis yra 100 vnt.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-143">There are three pick locations, each of which has a stocking limit of 100 pcs.</span></span> <span data-ttu-id="2c9e1-144">(Atminkite, kad talpos apribojimų reikia *Maksimalios vietos talpos* strategijai.)</span><span class="sxs-lookup"><span data-stu-id="2c9e1-144">(Remember that stocking limits are required for the *Maximum location capacity* strategy.)</span></span>
- <span data-ttu-id="2c9e1-145">Papildymo padėjimo vietos yra tokios pačios kaip paėmimo.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-145">The replenishment put locations are the same as the sales pick locations.</span></span>
- <span data-ttu-id="2c9e1-146">Papildymo vienetas yra dėžė (1 dėžė = 20 vnt).</span><span class="sxs-lookup"><span data-stu-id="2c9e1-146">The replenishment unit is a box (1 box = 20 pcs).</span></span>

<span data-ttu-id="2c9e1-147">Užsakymo metu, tolesnis inventorius turimas prekybos paėimimo vietoje:</span><span class="sxs-lookup"><span data-stu-id="2c9e1-147">At the time of the order, the following inventory is on hand at the sales pick locations:</span></span>

- <span data-ttu-id="2c9e1-148">**Pick-001:** 20 vnt (1 dėžė)</span><span class="sxs-lookup"><span data-stu-id="2c9e1-148">**Pick-001:** 20 pcs (1 box)</span></span>
- <span data-ttu-id="2c9e1-149">**Pick-002:** 0 vnt</span><span class="sxs-lookup"><span data-stu-id="2c9e1-149">**Pick-002:** 0 pcs</span></span>
- <span data-ttu-id="2c9e1-150">**Pick-003:** 0 vnt</span><span class="sxs-lookup"><span data-stu-id="2c9e1-150">**Pick-003:** 0 pcs</span></span>

<span data-ttu-id="2c9e1-151">Iš pradžių, papildymo strategija nustatyta į *Bangos paklausos kokybė*.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-151">Initially, the replenishment strategy is set to *Wave demand quantity*.</span></span>

<span data-ttu-id="2c9e1-152">Po prekybos užsakymo išleidimo į sandėlį ir bangos tvarkymo vykdymo bangai, gaunate šį papildymo darbą:</span><span class="sxs-lookup"><span data-stu-id="2c9e1-152">After you release the sales order to the warehouse, and wave processing runs for the wave, you get the following replenishment work:</span></span>

- <span data-ttu-id="2c9e1-153">**Papildymo darbas 1:** Imkite 4 dėžes iš bendros vietos ir padėkite jas į vietą pick-001.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-153">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
- <span data-ttu-id="2c9e1-154">**Papildymo darbas 2:** Imkite 2 dėžes iš bendros vietos ir padėkite jas į vietą pick-002.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-154">**Replenishment work 2:** Pick 2 boxes from the bulk location, and put them in location pick-002.</span></span>

<span data-ttu-id="2c9e1-155">Gaunate du papildymo darbo ID, nes privalote papildyti dvi vietas ir keli padėjimai nepalaikomi.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-155">You get two replenishment work IDs because you must replenish two locations, and multi-puts aren't supported.</span></span>

<span data-ttu-id="2c9e1-156">Jei nustatote papildymo strategiją į *Maksimali vietos talpa* gaunate šį papildymo darbą:</span><span class="sxs-lookup"><span data-stu-id="2c9e1-156">If you set the replenishment strategy to *Maximum location capacity* instead, you get the following replenishment work:</span></span>

- <span data-ttu-id="2c9e1-157">**Papildymo darbas 1:** Imkite 4 dėžes iš bendros vietos ir padėkite jas į vietą pick-001.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-157">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
- <span data-ttu-id="2c9e1-158">**Papildymo darbas 2:** Imkite 5 dėžes iš bendros vietos ir padėkite jas į vietą pick-002.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-158">**Replenishment work 2:** Pick 5 boxes from the bulk location, and put them in location pick-002.</span></span>

<span data-ttu-id="2c9e1-159">[![1 pavyzdys](media/ReplenTemp_example_1.png "1 pavyzdys")](media/ReplenTemp_example_1_large.png)</span><span class="sxs-lookup"><span data-stu-id="2c9e1-159">[![Example 1](media/ReplenTemp_example_1.png "Example 1")](media/ReplenTemp_example_1_large.png)</span></span>

### <a name="example-2"></a><span data-ttu-id="2c9e1-160">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="2c9e1-160">Example 2</span></span>

<span data-ttu-id="2c9e1-161">Šis pavyzdys rodo, kas atsitinka, kai bendra vieta neturi pakankamai inventoriaus, kad jis padengtų papildomą kiekį.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-161">This example shows what happens when the bulk location doesn't have enough inventory to cover the extra quantity.</span></span> <span data-ttu-id="2c9e1-162">Jis naudoja tą patį scenarijų kaip pavyzdyje 1, bet bendra vieta turi 160 vnt. (8 dėžes).</span><span class="sxs-lookup"><span data-stu-id="2c9e1-162">It uses the same scenario as example 1, but the bulk location has 160 pcs (8 boxes).</span></span>

<span data-ttu-id="2c9e1-163">Strategija *Bangos paklausos kiekis* sukuria tą patį darbą, kaip ir padarė pavyzdyje 1.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-163">The *Wave demand quantity* strategy creates the same work that it did in example 1.</span></span>

<span data-ttu-id="2c9e1-164">Nepaisant to, kadangi *Maksimali vietos talpos* strategija bando sukurti darbo ID kaip padarė pavyzdyje e 1, ji gali nepavykti.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-164">However, because the *Maximum location capacity* strategy tries to create the work IDs as it did in example 1, it might fail.</span></span> <span data-ttu-id="2c9e1-165">Tuo metu, sistema bando atkurti.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-165">At that point, the system tries to recover.</span></span>

<span data-ttu-id="2c9e1-166">Priklausomai nuo **Leisti atskyrimą** parinkties nustatymų vietos kryptyse papildymo paėmimui, galimos dvi išeitys:</span><span class="sxs-lookup"><span data-stu-id="2c9e1-166">Depending on the setting of the **Allow split** option on the location directives for replenishment picking, two outcomes are possible:</span></span>

- <span data-ttu-id="2c9e1-167">Jei **Leisti atskyrimą** parinktis nustatyta į *Taip*, sukuriamas tolesnis papildymo darbas:</span><span class="sxs-lookup"><span data-stu-id="2c9e1-167">If the **Allow split** option is set to *Yes*, the following replenishment work is created:</span></span>

    - <span data-ttu-id="2c9e1-168">**Papildymo darbas 1:** Imkite 4 dėžes iš bendros vietos ir padėkite jas į vietą pick-001.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-168">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
    - <span data-ttu-id="2c9e1-169">**Papildymo darbas 2:** Imkite 4 dėžes iš bendros vietos ir padėkite jas į vietą pick-002.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-169">**Replenishment work 2:** Pick 4 boxes from the bulk location, and put them in location pick-002.</span></span>

- <span data-ttu-id="2c9e1-170">Jei **Leisti atskyrimą** parinktis nustatyta į *Ne*, sukuriamas tolesnis papildymo darbas:</span><span class="sxs-lookup"><span data-stu-id="2c9e1-170">If the **Allow split** option is set to *No*, the following replenishment work is created:</span></span>

    - <span data-ttu-id="2c9e1-171">**Papildymo darbas 1:** Imkite 4 dėžes iš bendros vietos ir padėkite jas į vietą pick-001.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-171">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
    - <span data-ttu-id="2c9e1-172">**Papildymo darbas 2:** Imkite 2 dėžes iš bendros vietos ir padėkite jas į vietą pick-002.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-172">**Replenishment work 2:** Pick 2 boxes from the bulk location, and put them in location pick-002.</span></span>

<span data-ttu-id="2c9e1-173">Pasekmė skiriasi dėl informacijos, kuri prieinama jums sukūrus darbą.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-173">The outcomes differ because of the information that is available when you create the work.</span></span> <span data-ttu-id="2c9e1-174">Kai **Leisti atskyrimą** nustayta į *Taip* vieto kryptyse papildymo paėmimui, žinote, kad sugebėjote surasti 160 vnt.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-174">When the **Allow split** is set to *Yes* on the location directives for replenishment picking, you know that you managed to find 160 pcs.</span></span> <span data-ttu-id="2c9e1-175">Dėl to, galite sukurti darbą tam kiekiui.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-175">Therefore, you can create work for that quantity.</span></span> <span data-ttu-id="2c9e1-176">Nepaisant to, kai **Leisti atskyrimą** parinktis nustatyta į *Ne*, nežinote apie esančius 160 vnt.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-176">However, when the **Allow split** option is set to *No*, you don't know about the existence of the 160 pcs.</span></span> <span data-ttu-id="2c9e1-177">Kadangi papildomas kiekis, kurį nusprendėte papildyti buvo 3 dėžės, numetėte papildomą kiekį ir bandote ankstesnį kiekį dar kartą.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-177">Because the extra quantity that you decided to replenish was 3 boxes, you drop that extra quantity and try the original quantity again.</span></span>

<span data-ttu-id="2c9e1-178">[![2 pavyzdys](media/ReplenTemp_example_2.png "2 pavyzdys")](media/ReplenTemp_example_2_large.png)</span><span class="sxs-lookup"><span data-stu-id="2c9e1-178">[![Example 2](media/ReplenTemp_example_2.png "Example 2")](media/ReplenTemp_example_2_large.png)</span></span>

<span data-ttu-id="2c9e1-179">Dėl to, kad gautumėte maksimalų kiekį vietų papildymui, turite nustatyti **Leisti atskyrimą** parinktį į *Taip* vietos kryptyse papildymui.</span><span class="sxs-lookup"><span data-stu-id="2c9e1-179">Therefore, to get the maximum quantity to the replenished locations, you should set the **Allow split** option to *Yes* on the location directives for replenishment picking.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]