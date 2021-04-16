---
title: Pagrindinio planavimo trikčių šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite dirbdami su pagrindiniu planavimu.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8e78634c0efb1c401297559ce40b2ca30519f3bf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809475"
---
# <a name="troubleshoot-master-planning"></a><span data-ttu-id="e36d1-103">Pagrindinio planavimo trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="e36d1-103">Troubleshoot master planning</span></span>

<span data-ttu-id="e36d1-104">Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite dirbdami su pagrindiniu planavimu.</span><span class="sxs-lookup"><span data-stu-id="e36d1-104">This topic describes how to fix issues that you might encounter while you work with master planning.</span></span>

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a><span data-ttu-id="e36d1-105">Medžiagų važtaraščio sprogimas elgiasi kitaip patvirtintiems gamybos užsakymams ir apskaičiuotiems gamybos užsakymams, kai darbai sukuriami rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="e36d1-105">Bill of materials explosion behaves differently for firmed production orders and for estimated production orders for manually created work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e36d1-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="e36d1-106">Issue description</span></span>

<span data-ttu-id="e36d1-107">Patvirtinus gamybos užsakymą, prekės nėra sprogdinamos, kai sprogdinate medžiagų aprašą (BOM).</span><span class="sxs-lookup"><span data-stu-id="e36d1-107">When a production order is firmed, the items aren't exploded when you explode the bill of materials (BOM).</span></span> <span data-ttu-id="e36d1-108">Nepaisant to, jums rankiniu būdu sukuriant darbo užsakymą ir tada apskaičiuojant gamybos užsakymą, prekės yra sprogdinamos.</span><span class="sxs-lookup"><span data-stu-id="e36d1-108">However, when you manually create a work order and then estimate the production order, the items are exploded.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e36d1-109">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="e36d1-109">Issue resolution</span></span>

<span data-ttu-id="e36d1-110">Sistema dirba kaip tikėtasi.</span><span class="sxs-lookup"><span data-stu-id="e36d1-110">The system is working as expected.</span></span> <span data-ttu-id="e36d1-111">Sprogimas, įvykstantis kai gamybos užsakymas yra patvirtinamas, rodys į suplanuotą užsakymą, bet bus nerodoma, jog suplanuotas užsakymas šiuo metu ir šiuo atveju yra patvirtintas.</span><span class="sxs-lookup"><span data-stu-id="e36d1-111">The explosion that occurs when the production order is firmed will point to the planned order, but it doesn't appear that the planned order is currently firmed in this case.</span></span> <span data-ttu-id="e36d1-112">Nepaisant to, ar gamybos užsakymas buvo apskaičiuotas, sprogimas yra paskatinamas iš išleisto gamybos užsakymo, kai nėra jokio suplanuoto užsakymo.</span><span class="sxs-lookup"><span data-stu-id="e36d1-112">However, if the production order has been estimated, the explosion is triggered from the released production order where no planned order exists.</span></span>

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a><span data-ttu-id="e36d1-113">Vėlinimo vertė nėra naujinama, kai iš naujo suplanuoju suplanuotą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="e36d1-113">The Delay value isn't updated when I reschedule a planned order.</span></span>

<span data-ttu-id="e36d1-114">Norėdami naujinti suplanuotų užsakymų pavėlinimą, atverkite **Naujo suplanavimo** teksto laukelį suplanuotam užsakymui.</span><span class="sxs-lookup"><span data-stu-id="e36d1-114">To update the delay for planned orders, open the **Rescheduling** dialog box for the planned order.</span></span> <span data-ttu-id="e36d1-115">„FastTab“ **Sprogimas** įsitikinkite, kad **Atlikti sprogimą po pakartotinio suplanavimo** parinktis yra nustatyta į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="e36d1-115">On the **Explosion** FastTab, make sure that the **Perform explosion after rescheduling** option is set to *Yes*.</span></span>

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a><span data-ttu-id="e36d1-116">Gamybos naujas suplanavimas neapima saugos maržų, kurios yra nustatytos prekės apimtyje fiksuotam tiekimui.</span><span class="sxs-lookup"><span data-stu-id="e36d1-116">Production scheduling doesn't consider the safety margins that are set on the item coverage for pegged supply.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e36d1-117">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="e36d1-117">Issue description</span></span>

<span data-ttu-id="e36d1-118">Pagrindinis planavimas apima saugos maržas.</span><span class="sxs-lookup"><span data-stu-id="e36d1-118">Master planning considers the safety margins.</span></span> <span data-ttu-id="e36d1-119">Nepaisant to, saugos maržos ignoruojamos planuojant prekybos užsakymus, kai jie yra suplanuojami iš anksto.</span><span class="sxs-lookup"><span data-stu-id="e36d1-119">However, the safety margins are ignored when planned production orders are scheduled.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e36d1-120">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="e36d1-120">Issue resolution</span></span>

<span data-ttu-id="e36d1-121">Į maržas atsižvelgiama tik pagrindinio planavimo metu, o ne rankiniu būdu planuojant.</span><span class="sxs-lookup"><span data-stu-id="e36d1-121">Margins are considered only during master planning, not during manual scheduling.</span></span> <span data-ttu-id="e36d1-122">Maržos skirtos veikti kaip buferis planavimo etapo metu tam, kad suteiktų šiokią tokią esamo proceso „maržą“.</span><span class="sxs-lookup"><span data-stu-id="e36d1-122">Margins are designed to act as a buffer during the planning phase, to give some "margin" for the actual process.</span></span>

<span data-ttu-id="e36d1-123">Norėdami gauti norimą rezultatą, galite pašalinti maržą.</span><span class="sxs-lookup"><span data-stu-id="e36d1-123">To get the desired result, you can remove the margin.</span></span> <span data-ttu-id="e36d1-124">Maršrutas turi būti tuomet atnaujintas taip, kad apimtų norimą laiką (pavyzdžiui, laukimo laiką).</span><span class="sxs-lookup"><span data-stu-id="e36d1-124">The route must then be updated so that it includes the desired time (for example, as queue time).</span></span> <span data-ttu-id="e36d1-125">Tiek pagrindinis, tiek ir rankinis planavimas turi tuomet duoti tą patį rezultatą.</span><span class="sxs-lookup"><span data-stu-id="e36d1-125">Both master planning and manual scheduling should then produce the same result.</span></span>

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a><span data-ttu-id="e36d1-126">Suplanuoti užsakymai sukuriami net jei turime prekes atsargoje ir prekybos užsakymai jiems jau egzistuoja.</span><span class="sxs-lookup"><span data-stu-id="e36d1-126">Planned orders are generated even though we have items in stock and production orders already exist for them.</span></span>

<span data-ttu-id="e36d1-127">Galite ištaisyti šią problemą didindami **Teigiamų dienų** vertę atitinkamoms grupėms **Apimties grupės** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="e36d1-127">You might be able to fix this issue by increasing the **Positive days** value for the relevant groups on the **Coverage group** page.</span></span> <span data-ttu-id="e36d1-128">Dėl šio pakeitimo sistema nustatys, ar turimas inventorius gali būti naudojamas paklausai.</span><span class="sxs-lookup"><span data-stu-id="e36d1-128">This change will cause the system to determine whether on-hand inventory can be used for the demand.</span></span> <span data-ttu-id="e36d1-129">Tuomet naujas suplanuotas užsakymas nebus sukuriamas atsargų prekėms.</span><span class="sxs-lookup"><span data-stu-id="e36d1-129">Then a new planned order won't be generated for the items that are in stock.</span></span>

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a><span data-ttu-id="e36d1-130">Pagrindinis planavimas nesilaiko pajėgumo apribojimų ir yra suplanuotas daugiau nei prieinamas pajėgumas.</span><span class="sxs-lookup"><span data-stu-id="e36d1-130">Master planning doesn't seem to respect capacity limitations and is scheduling more than the available capacity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e36d1-131">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="e36d1-131">Issue description</span></span>

<span data-ttu-id="e36d1-132">Jums naudojant operacijos planavimą, kai yra baigtinis pajėgumas ir kai maršrutas nurodo reikalavimų mišinį tiek išteklių grupei, tiek ir atskiriems resursams, yra nedidelė per didelio rezervavimo tikimybė dėl būdo, kuriuo algoritmas patvirtina pajėgumo konfliktus.</span><span class="sxs-lookup"><span data-stu-id="e36d1-132">When you use operation scheduling where there is finite capacity, and where the route specifies a mix of requirements for both a resource group and individual resources, there is a small chance of overbooking because of the way that the algorithm validates for capacity conflicts.</span></span> <span data-ttu-id="e36d1-133">Per didelis rezervavimas gali įvykti jums naudojant padedančius įrankius siekiant vykdyti pagrindinį planavimą.</span><span class="sxs-lookup"><span data-stu-id="e36d1-133">This overbooking can occur when you use helpers to run master planning.</span></span> <span data-ttu-id="e36d1-134">Labiausiai tikėtina, kad jis įvyks, jei yra per daug darbų turinčių atitinkamą trumpą vykdymo laiką.</span><span class="sxs-lookup"><span data-stu-id="e36d1-134">It's most likely to occur if there are many jobs that have a relatively short runtime.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e36d1-135">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="e36d1-135">Issue resolution</span></span>

<span data-ttu-id="e36d1-136">Jei reikia, kad nebūtų per didelio rezervavimo veikimo planavimui, galite atlikti vienos linijos pagrindinio planavimo dalies naują planavimą įjungdami **Tikslus baigtas pajėgumas operacijos planavimui** parinktį puslapyje **Pagrindinio planavimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="e36d1-136">If it's essential that no overbooking occur for operation scheduling, you can make the scheduling part of master planning single-threaded by turning on the **Accurate finite capacity for Operation Scheduling** option on the **Master planning parameters** page.</span></span> <span data-ttu-id="e36d1-137">Ši parinktis nėra prieinama pagal nutylėjimą.</span><span class="sxs-lookup"><span data-stu-id="e36d1-137">This option isn't available by default.</span></span> <span data-ttu-id="e36d1-138">Privalote rankiniu būdu įtraukti ją į puslapį naudodami suasmenintas funkcijas.</span><span class="sxs-lookup"><span data-stu-id="e36d1-138">You must manually add it to the page by using personalization features.</span></span> <span data-ttu-id="e36d1-139">Jums naudojant šią parinktį, planavimas bus vykdomas lėčiau dėl paralelaus apdorojimo trūkumo.</span><span class="sxs-lookup"><span data-stu-id="e36d1-139">When you use this option, scheduling will run more slowly because of the lack of parallel processing.</span></span>

## <a name="planned-orders-take-a-long-time-to-update"></a><span data-ttu-id="e36d1-140">Suplanuoti užsakymai užtrunka ilgai, kai yra naujinami.</span><span class="sxs-lookup"><span data-stu-id="e36d1-140">Planned orders take a long time to update.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e36d1-141">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="e36d1-141">Issue description</span></span>

<span data-ttu-id="e36d1-142">Naujinant reikalavimo kiekį ir (arba) pristatymo datą suplanuotame užsakyme, dažniausiai užtrunka mažiausiai 30 sekundžių, kad vienas užsakymas įrašytų naujinimą.</span><span class="sxs-lookup"><span data-stu-id="e36d1-142">When updating the requirement quantity and/or delivery date on a planned order, it typically takes at least 30 seconds per order to save the update.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e36d1-143">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="e36d1-143">Issue resolution</span></span>

<span data-ttu-id="e36d1-144">Ši žinoma problema su įtaisytuoju pagrindinio planavimo varikliu.</span><span class="sxs-lookup"><span data-stu-id="e36d1-144">This is a known issue with the built-in master planning engine.</span></span> <span data-ttu-id="e36d1-145">Jį sukelia jį remiantis automatinis sprogimas per BOM struktūrą redagavimo metu.</span><span class="sxs-lookup"><span data-stu-id="e36d1-145">It is caused by the underlying auto explosion through the BOM structure during edits.</span></span> <span data-ttu-id="e36d1-146">Ši problema pažymėta „Planning Optimization“, kurioje planavimo įrankis gali būti naujinti ir tvirtinti atitinkamus užsakymus ir kai norima, paskatinti planavimo vykdymą siekiant atnaujinti suplanuotus užsakymus po ja esančiai BOM struktūrai.</span><span class="sxs-lookup"><span data-stu-id="e36d1-146">This issue is addressed in Planning Optimization, where a planner can update and approve the relevant orders and, when desired, trigger a planning run to update planned orders for the underlying BOM structure.</span></span>

<span data-ttu-id="e36d1-147">Vienas būdas skirtas pagerinti vykdymą su inkorporuotu pagrindinio planavimo varikliu yra tokia:</span><span class="sxs-lookup"><span data-stu-id="e36d1-147">One way to improve performance with the built-in master planning engine is to do the following:</span></span>

1. <span data-ttu-id="e36d1-148">Eikite į **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**.</span><span class="sxs-lookup"><span data-stu-id="e36d1-148">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="e36d1-149">Pasirinkite kelią.</span><span class="sxs-lookup"><span data-stu-id="e36d1-149">Select a plan.</span></span>
1. <span data-ttu-id="e36d1-150">Išplėskite **Laiko tvora dienomis** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="e36d1-150">Expand the **Time fence in days** FastTab.</span></span>
1. <span data-ttu-id="e36d1-151">Nustatykite **Sprogimą** į *Taip* ir nustatykite tolesnio laukelio nustatymą į 0 (taip).</span><span class="sxs-lookup"><span data-stu-id="e36d1-151">Set **Explosion** to *Yes*, and set the field below this setting to 0 (zero).</span></span>

> [!NOTE]
> <span data-ttu-id="e36d1-152">Toks bus ribojimas sprogimų laikotarpiui, kurie įvyko per šį pagrindinį planavimą ir vienos dienos metu.</span><span class="sxs-lookup"><span data-stu-id="e36d1-152">This will limit the period for explosions performed for this master plan to a single day.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]