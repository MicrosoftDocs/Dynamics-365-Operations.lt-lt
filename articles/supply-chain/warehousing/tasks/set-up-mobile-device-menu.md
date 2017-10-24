--- 
title: "Nustatyti mobiliojo įrenginio meniu elementą pirkimo užsakymo darbui atlikti"
description: "Šioje procedūroje nurodoma, kaip nustatyti mobiliojo įrenginio meniu elementą."
author: BibiSp
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b80c258d6a779a8fc5bb6c846abd3af7e69d5e06
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-in-a-purchase-order"></a><span data-ttu-id="21984-103">Nustatyti mobiliojo įrenginio meniu elementą pirkimo užsakymo darbui atlikti</span><span class="sxs-lookup"><span data-stu-id="21984-103">Set up a mobile device menu item for completing work in a purchase order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="21984-104">Šioje procedūroje nurodoma, kaip nustatyti mobiliojo įrenginio meniu elementą.</span><span class="sxs-lookup"><span data-stu-id="21984-104">This procedure shows how to set up a Mobile device menu item.</span></span> <span data-ttu-id="21984-105">Šiame pavyzdyje meniu elementas naudojamas atliekant tipo Pirkimo užsakymas darbą.</span><span class="sxs-lookup"><span data-stu-id="21984-105">In this example, the menu item is used for performing work of type Purchase order.</span></span> <span data-ttu-id="21984-106">Galiojantis darbas nustatomas pagal darbo klasę, kuri susieta su meniu elementu.</span><span class="sxs-lookup"><span data-stu-id="21984-106">The work class that’s associated with the menu item determines which work is valid.</span></span> <span data-ttu-id="21984-107">Šį vadovą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="21984-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="21984-108">Šią procedūrą paprastai atlieka sandėlio vadovas.</span><span class="sxs-lookup"><span data-stu-id="21984-108">This procedure is typically carried out by a warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="21984-109">Mobiliojo įrenginio meniu elemento kūrimas</span><span class="sxs-lookup"><span data-stu-id="21984-109">Create a mobile device menu item</span></span>
1. <span data-ttu-id="21984-110">Eikite į Mobiliojo įrenginio meniu elementai.</span><span class="sxs-lookup"><span data-stu-id="21984-110">Go to Mobile device menu items.</span></span>
2. <span data-ttu-id="21984-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="21984-111">Click New.</span></span>
3. <span data-ttu-id="21984-112">Lauke Meniu elemento pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="21984-112">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="21984-113">Įveskite unikalią reikšmę.</span><span class="sxs-lookup"><span data-stu-id="21984-113">Enter a unique value.</span></span> <span data-ttu-id="21984-114">Pavyzdžiui, galite įvesti „POMove“.</span><span class="sxs-lookup"><span data-stu-id="21984-114">For example, you could type POMove.</span></span> <span data-ttu-id="21984-115">Įsiminkite reikšmę, nes jos reikės vėliau.</span><span class="sxs-lookup"><span data-stu-id="21984-115">Remember the value, you'll need it later.</span></span>  
4. <span data-ttu-id="21984-116">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="21984-116">In the Title field, type a value.</span></span>
    * <span data-ttu-id="21984-117">Tai yra pavadinimas, kuris bus rodomas mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="21984-117">This is the title which will be displayed on the mobile device.</span></span> <span data-ttu-id="21984-118">Pavyzdžiui, galite įvesti „PO Move“.</span><span class="sxs-lookup"><span data-stu-id="21984-118">For example, you could type PO Move.</span></span>  
5. <span data-ttu-id="21984-119">Lauke Režimas pasirinkite „Darbas“.</span><span class="sxs-lookup"><span data-stu-id="21984-119">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="21984-120">Lauke Naudoti esamą darbą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="21984-120">Select Yes in the Use existing work field.</span></span>
    * <span data-ttu-id="21984-121">Šis mobiliojo įrenginio meniu elementas yra naudojamas esamam darbui atlikti.</span><span class="sxs-lookup"><span data-stu-id="21984-121">This mobile device menu item is used to perform existing work.</span></span> <span data-ttu-id="21984-122">Todėl turite šią reikšmę nustatyti į parinktį Taip.</span><span class="sxs-lookup"><span data-stu-id="21984-122">Therefore you must set this value to Yes.</span></span>  
    * <span data-ttu-id="21984-123">Laukas Rodyti atsargų būseną nustato, ar turimų atsargų būsena bus rodoma sandėlio darbuotojo mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="21984-123">The Display inventory status field determines whether the inventory status of the on-hand inventory will be displayed to the warehouse worker on the mobile device.</span></span>  
7. <span data-ttu-id="21984-124">Lauke Nukreipė pasirinkite 'Sistemos grupavimas'.</span><span class="sxs-lookup"><span data-stu-id="21984-124">In the Directed by field, select 'System grouping'.</span></span>
    * <span data-ttu-id="21984-125">Kai ką nors pasirenkate lauke Nukreipė, šio puslapio dalyje Bendra rodomi papildomi laukai.</span><span class="sxs-lookup"><span data-stu-id="21984-125">When you select something in the Directed by field, additional fields appear in the General section on this page.</span></span> <span data-ttu-id="21984-126">Rodomi laukai priklauso nuo to, ką pasirinkote.</span><span class="sxs-lookup"><span data-stu-id="21984-126">The fields that appear depend on what you selected.</span></span> <span data-ttu-id="21984-127">Pasirinkus Sistemos grupavimas, įtraukiami du nauji laukai.</span><span class="sxs-lookup"><span data-stu-id="21984-127">When you select System grouping, two new fields are added.</span></span> <span data-ttu-id="21984-128">Jie yra paaiškinti toliau.</span><span class="sxs-lookup"><span data-stu-id="21984-128">These are explained below.</span></span>  
8. <span data-ttu-id="21984-129">Lauke Sistemos grupavimas pasirinkite WorkPoolId.</span><span class="sxs-lookup"><span data-stu-id="21984-129">In the System grouping field, select 'WorkPoolId'.</span></span>
    * <span data-ttu-id="21984-130">Sandėlio darbuotojams atidarius šią meniu elementą, jie bus prašyti nuskaityti darbo telkinio ID.</span><span class="sxs-lookup"><span data-stu-id="21984-130">When warehouse workers open this menu item, they’ll be asked to scan a Work pool ID.</span></span> <span data-ttu-id="21984-131">Visi darbo užsakymai su šiuo darbo telkinio ID ir į šį meniu elementą įtrauktų darbo klasių atviros darbo užsakymo eilutės bus perkelti darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="21984-131">All work orders with this Work pool ID and open work order lines with one of the work classes added to this menu item will be pushed to the user.</span></span>  
9. <span data-ttu-id="21984-132">Lauke Sistemos grupavimo žyma įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="21984-132">In the System grouping label field, type a value.</span></span>
    * <span data-ttu-id="21984-133">Šis tekstas rodomas vartotojui mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="21984-133">This is the text displayed to the user on the mobile device.</span></span> <span data-ttu-id="21984-134">Pavyzdžiui, galite įvesti Darbo telkinys.</span><span class="sxs-lookup"><span data-stu-id="21984-134">For example, you could type Work pool.</span></span>  
10. <span data-ttu-id="21984-135">Pildydami lauke Nepaisyti numerio lentelės pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="21984-135">Select Yes in the Override license plate during put field.</span></span>
    * <span data-ttu-id="21984-136">Ši parinktis leidžia sandėlio darbuotojams perrašyti tikslinę numerio lentelę, kai prekės padedamos vietoje, kuri kontroliuojama pagal numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="21984-136">This option allows warehouse workers to override the target license plate when items are put down on a license plate controlled location.</span></span>  
11. <span data-ttu-id="21984-137">Lauke Grupinis atidėjimas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="21984-137">Select Yes in the Group put away field.</span></span>
    * <span data-ttu-id="21984-138">Jei visose darbo užsakymo padėjimo eilutėse bendrai naudojama ta pati vieta, vartotojui bus pateikta viena bendra visų eilučių padėjimo instrukcija.</span><span class="sxs-lookup"><span data-stu-id="21984-138">If all the Put lines on the work order share the same location, the user will receive one combined Put instruction for all lines.</span></span>  
    * <span data-ttu-id="21984-139">Audito šablono ID: darbo audito šablonas leidžia nurodyti, kad meniu elemento darbo procesas turi būti nutrauktas, kad būtų galima atlikti kitą operaciją.</span><span class="sxs-lookup"><span data-stu-id="21984-139">Audit template ID: A work audit template allows you to specify that the work process for a menu item should be interrupted so that another operation can be performed.</span></span> <span data-ttu-id="21984-140">Pavyzdžiui, jei šis meniu elementas skirtas gaunamam darbui, audito šablone gali būti reikalaujama, kad darbuotojas tikrintų temperatūrą.</span><span class="sxs-lookup"><span data-stu-id="21984-140">For example, if this menu item is for inbound work, the audit template might require that the worker checks the temperature.</span></span> <span data-ttu-id="21984-141">Proceso pertraukimo taškas nurodomas audito šablone, tai gali būti, pavyzdžiui, darbo pradžios ar pabaigos arba jo būsenos pakeitimo taškas.</span><span class="sxs-lookup"><span data-stu-id="21984-141">The point at which the process is interrupted is specified on the audit template and can be, for example, when work is started or completed, or when its status changes.</span></span>  
12. <span data-ttu-id="21984-142">Išplėskite skyrių Darbo klasės.</span><span class="sxs-lookup"><span data-stu-id="21984-142">Expand the Work classes section.</span></span>
13. <span data-ttu-id="21984-143">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="21984-143">Click New.</span></span>
14. <span data-ttu-id="21984-144">Lauke Darbo klasės ID įveskite Pirkimas.</span><span class="sxs-lookup"><span data-stu-id="21984-144">In the Work class ID field, type 'Purchase'.</span></span>
    * <span data-ttu-id="21984-145">Darbo telkinys riboja darbą, kuriam galima naudoti meniu elementą.</span><span class="sxs-lookup"><span data-stu-id="21984-145">The work pool restricts the work that the menu item can be used for.</span></span> <span data-ttu-id="21984-146">Šiuo atveju jis bus naudojamas atviroms darbo užsakymo eilutėms, turinčioms pirkimo darbo klasės ID.</span><span class="sxs-lookup"><span data-stu-id="21984-146">In this case it will be used for open work order lines that have the Purchase work class ID.</span></span>  
15. <span data-ttu-id="21984-147">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="21984-147">Click Save.</span></span>

## <a name="set-up-work-confirmation"></a><span data-ttu-id="21984-148">Nustatykite darbo patvirtinimą</span><span class="sxs-lookup"><span data-stu-id="21984-148">Set up work confirmation</span></span>
1. <span data-ttu-id="21984-149">Spustelėkite Darbo patvirtinimo nustatymas.</span><span class="sxs-lookup"><span data-stu-id="21984-149">Click Work confirmation setup.</span></span>
2. <span data-ttu-id="21984-150">Lauke Darbo tipas pasirinkite 'Paimti'.</span><span class="sxs-lookup"><span data-stu-id="21984-150">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="21984-151">Pažymėkite žymės langelį Automatinis patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="21984-151">Select the Auto confirm check box.</span></span>
    * <span data-ttu-id="21984-152">Darbo instrukcija, kurios darbo tipas yra Paėmimas, bus patvirtinta automatiškai.</span><span class="sxs-lookup"><span data-stu-id="21984-152">The work instruction with work type Pick will be auto-confirmed.</span></span> <span data-ttu-id="21984-153">Ši instrukcija nebus pateikta vartotojui.</span><span class="sxs-lookup"><span data-stu-id="21984-153">This instruction will not be presented to the user.</span></span>  
4. <span data-ttu-id="21984-154">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="21984-154">Click New.</span></span>
5. <span data-ttu-id="21984-155">Lauke Darbo tipas pasirinkite „Padėjimas“.</span><span class="sxs-lookup"><span data-stu-id="21984-155">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="21984-156">Pažymėkite žymės langelį Vietos patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="21984-156">Select the Location confirmation check box.</span></span>
    * <span data-ttu-id="21984-157">Sandėlio darbuotojas bus paprašytas atlikti patvirtinamąjį vietos nuskaitymą, kai prekė bus padėta.</span><span class="sxs-lookup"><span data-stu-id="21984-157">The warehouse worker will be asked to perform a confirmation scan of the location, when the item is put down.</span></span>  
7. <span data-ttu-id="21984-158">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="21984-158">Click Save.</span></span>
8. <span data-ttu-id="21984-159">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="21984-159">Close the page.</span></span>
9. <span data-ttu-id="21984-160">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="21984-160">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="21984-161">Meniu elemento įtraukimas į mobiliojo įrenginio meniu</span><span class="sxs-lookup"><span data-stu-id="21984-161">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="21984-162">Eikite į Mobiliojo įrenginio meniu.</span><span class="sxs-lookup"><span data-stu-id="21984-162">Go to Mobile device menu.</span></span>
2. <span data-ttu-id="21984-163">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="21984-163">Click Edit.</span></span>
3. <span data-ttu-id="21984-164">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="21984-164">Use the Quick Filter to find records.</span></span> <span data-ttu-id="21984-165">Pvz., filtruokite lauką Pavadinimas verte 'gaunama'.</span><span class="sxs-lookup"><span data-stu-id="21984-165">For example, filter on the Name field with a value of 'inbound'.</span></span>
    * <span data-ttu-id="21984-166">Norite rasti meniu, kurį galite naudoti gavimo meniu elementams.</span><span class="sxs-lookup"><span data-stu-id="21984-166">You want to find the menu you use for inbound menu items.</span></span> <span data-ttu-id="21984-167">USMF tai vadinama Gaunama.</span><span class="sxs-lookup"><span data-stu-id="21984-167">In USMF this is called Inbound.</span></span>  
4. <span data-ttu-id="21984-168">Medyje pasirinkite 'vertė'.</span><span class="sxs-lookup"><span data-stu-id="21984-168">In the tree, select 'a value'.</span></span>
5. <span data-ttu-id="21984-169">Spustelėkite į dešinę pusę rodančią rodyklę.</span><span class="sxs-lookup"><span data-stu-id="21984-169">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="21984-170">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="21984-170">Click Save.</span></span>
7. <span data-ttu-id="21984-171">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="21984-171">Close the page.</span></span>


