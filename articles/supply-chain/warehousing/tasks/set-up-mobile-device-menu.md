---
title: Nustatyti mobiliojo įrenginio meniu elementą Pirkimo užsakymo tipo darbui atlikti
description: Šioje procedūroje nurodoma, kaip nustatyti mobiliojo įrenginio meniu elementą.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 707fc9c798da8eac30cc9f56c158be3d96b271d6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847116"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a><span data-ttu-id="aeb50-103">Nustatyti mobiliojo įrenginio meniu elementą Pirkimo užsakymo tipo darbui atlikti</span><span class="sxs-lookup"><span data-stu-id="aeb50-103">Set up a mobile device menu item for completing work of type Purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aeb50-104">Šioje procedūroje nurodoma, kaip nustatyti mobiliojo įrenginio meniu elementą.</span><span class="sxs-lookup"><span data-stu-id="aeb50-104">This procedure shows how to set up a Mobile device menu item.</span></span> <span data-ttu-id="aeb50-105">Šiame pavyzdyje meniu elementas naudojamas atliekant tipo Pirkimo užsakymas darbą.</span><span class="sxs-lookup"><span data-stu-id="aeb50-105">In this example, the menu item is used for performing work of type Purchase order.</span></span> <span data-ttu-id="aeb50-106">Galiojantis darbas nustatomas pagal darbo klasę, kuri susieta su meniu elementu.</span><span class="sxs-lookup"><span data-stu-id="aeb50-106">The work class that’s associated with the menu item determines which work is valid.</span></span> <span data-ttu-id="aeb50-107">Šį vadovą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="aeb50-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="aeb50-108">Šią procedūrą paprastai atlieka sandėlio vadovas.</span><span class="sxs-lookup"><span data-stu-id="aeb50-108">This procedure is typically carried out by a warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="aeb50-109">Mobiliojo įrenginio meniu elemento kūrimas</span><span class="sxs-lookup"><span data-stu-id="aeb50-109">Create a mobile device menu item</span></span>
1. <span data-ttu-id="aeb50-110">Eikite į Mobiliojo įrenginio meniu elementai.</span><span class="sxs-lookup"><span data-stu-id="aeb50-110">Go to Mobile device menu items.</span></span>
2. <span data-ttu-id="aeb50-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="aeb50-111">Click New.</span></span>
3. <span data-ttu-id="aeb50-112">Lauke Meniu elemento pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aeb50-112">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="aeb50-113">Įveskite unikalią reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aeb50-113">Enter a unique value.</span></span> <span data-ttu-id="aeb50-114">Pavyzdžiui, galite įvesti „POMove“.</span><span class="sxs-lookup"><span data-stu-id="aeb50-114">For example, you could type POMove.</span></span> <span data-ttu-id="aeb50-115">Įsiminkite reikšmę, nes jos reikės vėliau.</span><span class="sxs-lookup"><span data-stu-id="aeb50-115">Remember the value, you'll need it later.</span></span>  
4. <span data-ttu-id="aeb50-116">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aeb50-116">In the Title field, type a value.</span></span>
    * <span data-ttu-id="aeb50-117">Tai yra pavadinimas, kuris bus rodomas mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="aeb50-117">This is the title which will be displayed on the mobile device.</span></span> <span data-ttu-id="aeb50-118">Pavyzdžiui, galite įvesti „PO Move“.</span><span class="sxs-lookup"><span data-stu-id="aeb50-118">For example, you could type PO Move.</span></span>  
5. <span data-ttu-id="aeb50-119">Lauke Režimas pasirinkite „Darbas“.</span><span class="sxs-lookup"><span data-stu-id="aeb50-119">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="aeb50-120">Lauke Naudoti esamą darbą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="aeb50-120">Select Yes in the Use existing work field.</span></span>
    * <span data-ttu-id="aeb50-121">Šis mobiliojo įrenginio meniu elementas yra naudojamas esamam darbui atlikti.</span><span class="sxs-lookup"><span data-stu-id="aeb50-121">This mobile device menu item is used to perform existing work.</span></span> <span data-ttu-id="aeb50-122">Todėl turite šią reikšmę nustatyti į parinktį Taip.</span><span class="sxs-lookup"><span data-stu-id="aeb50-122">Therefore you must set this value to Yes.</span></span>  
    * <span data-ttu-id="aeb50-123">Laukas Rodyti atsargų būseną nustato, ar turimų atsargų būsena bus rodoma sandėlio darbuotojo mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="aeb50-123">The Display inventory status field determines whether the inventory status of the on-hand inventory will be displayed to the warehouse worker on the mobile device.</span></span>  
7. <span data-ttu-id="aeb50-124">Lauke Nukreipė pasirinkite 'Sistemos grupavimas'.</span><span class="sxs-lookup"><span data-stu-id="aeb50-124">In the Directed by field, select 'System grouping'.</span></span>
    * <span data-ttu-id="aeb50-125">Kai ką nors pasirenkate lauke Nukreipė, šio puslapio dalyje Bendra rodomi papildomi laukai.</span><span class="sxs-lookup"><span data-stu-id="aeb50-125">When you select something in the Directed by field, additional fields appear in the General section on this page.</span></span> <span data-ttu-id="aeb50-126">Rodomi laukai priklauso nuo to, ką pasirinkote.</span><span class="sxs-lookup"><span data-stu-id="aeb50-126">The fields that appear depend on what you selected.</span></span> <span data-ttu-id="aeb50-127">Pasirinkus Sistemos grupavimas, įtraukiami du nauji laukai.</span><span class="sxs-lookup"><span data-stu-id="aeb50-127">When you select System grouping, two new fields are added.</span></span> <span data-ttu-id="aeb50-128">Jie yra paaiškinti toliau.</span><span class="sxs-lookup"><span data-stu-id="aeb50-128">These are explained below.</span></span>  
8. <span data-ttu-id="aeb50-129">Lauke Sistemos grupavimas pasirinkite WorkPoolId.</span><span class="sxs-lookup"><span data-stu-id="aeb50-129">In the System grouping field, select 'WorkPoolId'.</span></span>
    * <span data-ttu-id="aeb50-130">Sandėlio darbuotojams atidarius šią meniu elementą, jie bus prašyti nuskaityti darbo telkinio ID.</span><span class="sxs-lookup"><span data-stu-id="aeb50-130">When warehouse workers open this menu item, they’ll be asked to scan a Work pool ID.</span></span> <span data-ttu-id="aeb50-131">Visi darbo užsakymai su šiuo darbo telkinio ID ir į šį meniu elementą įtrauktų darbo klasių atviros darbo užsakymo eilutės bus perkelti darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="aeb50-131">All work orders with this Work pool ID and open work order lines with one of the work classes added to this menu item will be pushed to the user.</span></span>  
9. <span data-ttu-id="aeb50-132">Lauke Sistemos grupavimo žyma įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="aeb50-132">In the System grouping label field, type a value.</span></span>
    * <span data-ttu-id="aeb50-133">Šis tekstas rodomas vartotojui mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="aeb50-133">This is the text displayed to the user on the mobile device.</span></span> <span data-ttu-id="aeb50-134">Pavyzdžiui, galite įvesti Darbo telkinys.</span><span class="sxs-lookup"><span data-stu-id="aeb50-134">For example, you could type Work pool.</span></span>  
10. <span data-ttu-id="aeb50-135">Pildydami lauke Nepaisyti numerio lentelės pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="aeb50-135">Select Yes in the Override license plate during put field.</span></span>
    * <span data-ttu-id="aeb50-136">Ši parinktis leidžia sandėlio darbuotojams perrašyti tikslinę numerio lentelę, kai prekės padedamos vietoje, kuri kontroliuojama pagal numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="aeb50-136">This option allows warehouse workers to override the target license plate when items are put down on a license plate controlled location.</span></span>  
11. <span data-ttu-id="aeb50-137">Lauke Grupinis atidėjimas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="aeb50-137">Select Yes in the Group put away field.</span></span>
    * <span data-ttu-id="aeb50-138">Jei visose darbo užsakymo padėjimo eilutėse bendrai naudojama ta pati vieta, vartotojui bus pateikta viena bendra visų eilučių padėjimo instrukcija.</span><span class="sxs-lookup"><span data-stu-id="aeb50-138">If all the Put lines on the work order share the same location, the user will receive one combined Put instruction for all lines.</span></span>  
    * <span data-ttu-id="aeb50-139">Audito šablono ID: darbo audito šablonas leidžia nurodyti, kad meniu elemento darbo procesas turi būti nutrauktas, kad būtų galima atlikti kitą operaciją.</span><span class="sxs-lookup"><span data-stu-id="aeb50-139">Audit template ID: A work audit template allows you to specify that the work process for a menu item should be interrupted so that another operation can be performed.</span></span> <span data-ttu-id="aeb50-140">Pavyzdžiui, jei šis meniu elementas skirtas gaunamam darbui, audito šablone gali būti reikalaujama, kad darbuotojas tikrintų temperatūrą.</span><span class="sxs-lookup"><span data-stu-id="aeb50-140">For example, if this menu item is for inbound work, the audit template might require that the worker checks the temperature.</span></span> <span data-ttu-id="aeb50-141">Proceso pertraukimo taškas nurodomas audito šablone, tai gali būti, pavyzdžiui, darbo pradžios ar pabaigos arba jo būsenos pakeitimo taškas.</span><span class="sxs-lookup"><span data-stu-id="aeb50-141">The point at which the process is interrupted is specified on the audit template and can be, for example, when work is started or completed, or when its status changes.</span></span>  
12. <span data-ttu-id="aeb50-142">Išplėskite skyrių Darbo klasės.</span><span class="sxs-lookup"><span data-stu-id="aeb50-142">Expand the Work classes section.</span></span>
13. <span data-ttu-id="aeb50-143">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="aeb50-143">Click New.</span></span>
14. <span data-ttu-id="aeb50-144">Lauke Darbo klasės ID įveskite Pirkimas.</span><span class="sxs-lookup"><span data-stu-id="aeb50-144">In the Work class ID field, type 'Purchase'.</span></span>
    * <span data-ttu-id="aeb50-145">Darbo telkinys riboja darbą, kuriam galima naudoti meniu elementą.</span><span class="sxs-lookup"><span data-stu-id="aeb50-145">The work pool restricts the work that the menu item can be used for.</span></span> <span data-ttu-id="aeb50-146">Šiuo atveju jis bus naudojamas atviroms darbo užsakymo eilutėms, turinčioms pirkimo darbo klasės ID.</span><span class="sxs-lookup"><span data-stu-id="aeb50-146">In this case it will be used for open work order lines that have the Purchase work class ID.</span></span>  
15. <span data-ttu-id="aeb50-147">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="aeb50-147">Click Save.</span></span>

## <a name="set-up-work-confirmation"></a><span data-ttu-id="aeb50-148">Nustatykite darbo patvirtinimą</span><span class="sxs-lookup"><span data-stu-id="aeb50-148">Set up work confirmation</span></span>
1. <span data-ttu-id="aeb50-149">Spustelėkite Darbo patvirtinimo nustatymas.</span><span class="sxs-lookup"><span data-stu-id="aeb50-149">Click Work confirmation setup.</span></span>
2. <span data-ttu-id="aeb50-150">Lauke Darbo tipas pasirinkite 'Paimti'.</span><span class="sxs-lookup"><span data-stu-id="aeb50-150">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="aeb50-151">Pažymėkite žymės langelį Automatinis patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="aeb50-151">Select the Auto confirm check box.</span></span>
    * <span data-ttu-id="aeb50-152">Darbo instrukcija, kurios darbo tipas yra Paėmimas, bus patvirtinta automatiškai.</span><span class="sxs-lookup"><span data-stu-id="aeb50-152">The work instruction with work type Pick will be auto-confirmed.</span></span> <span data-ttu-id="aeb50-153">Ši instrukcija nebus pateikta vartotojui.</span><span class="sxs-lookup"><span data-stu-id="aeb50-153">This instruction will not be presented to the user.</span></span>  
4. <span data-ttu-id="aeb50-154">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="aeb50-154">Click New.</span></span>
5. <span data-ttu-id="aeb50-155">Lauke Darbo tipas pasirinkite „Padėjimas“.</span><span class="sxs-lookup"><span data-stu-id="aeb50-155">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="aeb50-156">Pažymėkite žymės langelį Vietos patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="aeb50-156">Select the Location confirmation check box.</span></span>
    * <span data-ttu-id="aeb50-157">Sandėlio darbuotojas bus paprašytas atlikti patvirtinamąjį vietos nuskaitymą, kai prekė bus padėta.</span><span class="sxs-lookup"><span data-stu-id="aeb50-157">The warehouse worker will be asked to perform a confirmation scan of the location, when the item is put down.</span></span>  
7. <span data-ttu-id="aeb50-158">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="aeb50-158">Click Save.</span></span>
8. <span data-ttu-id="aeb50-159">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="aeb50-159">Close the page.</span></span>
9. <span data-ttu-id="aeb50-160">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="aeb50-160">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="aeb50-161">Meniu elemento įtraukimas į mobiliojo įrenginio meniu</span><span class="sxs-lookup"><span data-stu-id="aeb50-161">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="aeb50-162">Eikite į Mobiliojo įrenginio meniu.</span><span class="sxs-lookup"><span data-stu-id="aeb50-162">Go to Mobile device menu.</span></span>
2. <span data-ttu-id="aeb50-163">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="aeb50-163">Click Edit.</span></span>
3. <span data-ttu-id="aeb50-164">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="aeb50-164">Use the Quick Filter to find records.</span></span> <span data-ttu-id="aeb50-165">Pvz., filtruokite lauką Pavadinimas verte 'gaunama'.</span><span class="sxs-lookup"><span data-stu-id="aeb50-165">For example, filter on the Name field with a value of 'inbound'.</span></span>
    * <span data-ttu-id="aeb50-166">Norite rasti meniu, kurį galite naudoti gavimo meniu elementams.</span><span class="sxs-lookup"><span data-stu-id="aeb50-166">You want to find the menu you use for inbound menu items.</span></span> <span data-ttu-id="aeb50-167">USMF tai vadinama Gaunama.</span><span class="sxs-lookup"><span data-stu-id="aeb50-167">In USMF this is called Inbound.</span></span>  
4. <span data-ttu-id="aeb50-168">Medyje pasirinkite 'vertė'.</span><span class="sxs-lookup"><span data-stu-id="aeb50-168">In the tree, select 'a value'.</span></span>
5. <span data-ttu-id="aeb50-169">Spustelėkite į dešinę pusę rodančią rodyklę.</span><span class="sxs-lookup"><span data-stu-id="aeb50-169">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="aeb50-170">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="aeb50-170">Click Save.</span></span>
7. <span data-ttu-id="aeb50-171">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="aeb50-171">Close the page.</span></span>

