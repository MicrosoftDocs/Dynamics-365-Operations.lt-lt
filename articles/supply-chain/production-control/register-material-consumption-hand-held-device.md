---
title: Medžiagų vartojimo registravimas naudojant mobilųjį įrenginį
description: Šioje temoje aprašoma darbo eiga, kurią naudojant galima kišeniniu įrenginiu registruoti žaliavų sunaudojimą gamybos metu.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a4afc4b0c8d9a7109201326169311e85798d532
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209399"
---
# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="6152f-103">Medžiagų vartojimo registravimas naudojant mobilųjį įrenginį</span><span class="sxs-lookup"><span data-stu-id="6152f-103">Register material consumption using a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6152f-104">Šioje temoje aprašoma darbo eiga, kurią naudojant galima kišeniniu įrenginiu registruoti žaliavų sunaudojimą gamybos metu.</span><span class="sxs-lookup"><span data-stu-id="6152f-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="6152f-105">Įžanga</span><span class="sxs-lookup"><span data-stu-id="6152f-105">Introduction</span></span>
------------

<span data-ttu-id="6152f-106">Ši darbo eiga aktuali, jei yra griežtas medžiagų atsekamumo reikalavimas.</span><span class="sxs-lookup"><span data-stu-id="6152f-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="6152f-107">Tokiais atvejais norint užtikrinti medžiagų atsekamumą reikia nurodyti tikslų sunaudojimo laiką ir kiekį.</span><span class="sxs-lookup"><span data-stu-id="6152f-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="6152f-108">Šį procesą galima laikyti priešingu išankstinio ar atgalinio sunaudojimo operacijoms, kai nesutampa registracijos laikas ir laikas, kada medžiagos faktiškai naudojamos.</span><span class="sxs-lookup"><span data-stu-id="6152f-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="6152f-109">Tai paaiškina, kodėl automatinio sunaudojimo strategijos negalima naudoti su kai kuriomis medžiagomis, kurias reikalaujama atsekti.</span><span class="sxs-lookup"><span data-stu-id="6152f-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="6152f-110">Pažvelkime į paprastą scenarijų, kuris paaiškina, kaip nustatyti darbo eigą, kad kišeniniu įrenginiu būtų galima registruoti žaliavų sunaudojimą gamybos metu.</span><span class="sxs-lookup"><span data-stu-id="6152f-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> <span data-ttu-id="6152f-111">[![darbo eigą, kad kišeniniu įrenginiu būtų galima registruoti žaliavų sunaudojimą, nustatymas](./media/scenario3.png)](./media/scenario3.png)</span><span class="sxs-lookup"><span data-stu-id="6152f-111">[![set up a workflow to enable registration of raw material consumption by using a handheld device](./media/scenario3.png)](./media/scenario3.png)</span></span>

### <a name="scenario-details"></a><span data-ttu-id="6152f-112">Išsami scenarijaus informacija</span><span class="sxs-lookup"><span data-stu-id="6152f-112">Scenario details</span></span>

<span data-ttu-id="6152f-113">Nepertraukiamo gamybos proceso (5) metu naudojama paketiniu būdu kontroliuojama žaliava RM-100.</span><span class="sxs-lookup"><span data-stu-id="6152f-113">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="6152f-114">Medžiaga turima vietoje Bulk-001 (1) (numerio lentelė – PL-1), kurioje yra du paketai (B1 ir B2), kuriuose yra po 100 svarų medžiagos kiekio.</span><span class="sxs-lookup"><span data-stu-id="6152f-114">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="6152f-115">Pateikiamas ir apdorojamas RM-100 sandėlio darbas (2), o medžiaga iš Bulk-001 paimama į gamybos įvesties vietą PIL-01 (3), kuri apibrėžta kaip kontroliuojama ne pagal numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="6152f-115">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="6152f-116">Mašinos operatorius pasveria medžiagą iš gamybos įvesties vietos (3) ir svorį bei paketo numerį užregistruoja kaip sunaudotus (4).</span><span class="sxs-lookup"><span data-stu-id="6152f-116">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="6152f-117">Dalis medžiagos apibrėžtais laiko intervalais rankiniu būdu iš gamybos įvesties vietos dedama į gamybos procesą.</span><span class="sxs-lookup"><span data-stu-id="6152f-117">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="6152f-118">Mašinos operatoriui dedant medžiagą, ji pasveriama ant svarstyklių ir užregistruojamas paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="6152f-118">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="6152f-119">Darbo eigos nustatymas taip, kad sunaudojimą būtų galima registruoti kišeniniu įrenginiu</span><span class="sxs-lookup"><span data-stu-id="6152f-119">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="6152f-120">Sukurkite baigtos prekės produktą (FG-100) su komplektavimo specifikacija, kurioje yra paketiniu būdu kontroliuojama žaliava RM-100.</span><span class="sxs-lookup"><span data-stu-id="6152f-120">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="6152f-121">Įtraukite du RM-100 paketus (B1 ir B2), kurių kiekis – 100, į vietą: „Bulk-001” numerio lentelėje PL-1.</span><span class="sxs-lookup"><span data-stu-id="6152f-121">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="6152f-122">Komplektavimo specifikacijos RM-100 eilutėje sunaudojimo principas nustatomas kaip **Rankinis**.</span><span class="sxs-lookup"><span data-stu-id="6152f-122">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="6152f-123">Nustatykite gamybos įvesties vietą į PIL-01.</span><span class="sxs-lookup"><span data-stu-id="6152f-123">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="6152f-124">Tai padaryti galite šią vietą pasirinkdami kaip numatytąją 51 sandėlio gamybos įvesties vietą.</span><span class="sxs-lookup"><span data-stu-id="6152f-124">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="6152f-125">Sukurkite naują mobiliojo įrenginio meniu elementą:</span><span class="sxs-lookup"><span data-stu-id="6152f-125">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="6152f-126">**Meniu elemento pavadinimas** – Registruoja medžiagų sunaudojimą.</span><span class="sxs-lookup"><span data-stu-id="6152f-126">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="6152f-127">**Pavadinimas** – Registruoti medžiagų sunaudojimą.</span><span class="sxs-lookup"><span data-stu-id="6152f-127">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="6152f-128">**Režimas** – Netiesioginis.</span><span class="sxs-lookup"><span data-stu-id="6152f-128">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="6152f-129">**Veiklos kodas** – Registruoja medžiagų sunaudojimą.</span><span class="sxs-lookup"><span data-stu-id="6152f-129">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="6152f-130">Meniu elementą įtraukite į **Mobili gamyba** įrenginio meniu.</span><span class="sxs-lookup"><span data-stu-id="6152f-130">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="6152f-131">Sukurkite baigto produkto gamybos užsakymą:</span><span class="sxs-lookup"><span data-stu-id="6152f-131">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="6152f-132">**Prekės numeris** – „FG-100”</span><span class="sxs-lookup"><span data-stu-id="6152f-132">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="6152f-133">**Vieta** – 5</span><span class="sxs-lookup"><span data-stu-id="6152f-133">**Site** - 5</span></span> 
-    <span data-ttu-id="6152f-134">**Sandėlis** – „51”</span><span class="sxs-lookup"><span data-stu-id="6152f-134">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="6152f-135">**Kiekis** – 150</span><span class="sxs-lookup"><span data-stu-id="6152f-135">**Quantity** - 150</span></span>

<span data-ttu-id="6152f-136">Gamybos užsakymas **įvertinamas** bei **pateikiamas** ir sukuriamas sandėlio darbas.</span><span class="sxs-lookup"><span data-stu-id="6152f-136">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="6152f-137">Atlikite darbą naudodami kišeniniam įrenginiui skirtą žaliavų paėmimo darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="6152f-137">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="6152f-138">Taip medžiaga iš buferinės vietos bus perkelta į gamybos įvesties vietą PIL-01.</span><span class="sxs-lookup"><span data-stu-id="6152f-138">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="6152f-139">Baigus darbą medžiaga yra **Paimta gamybos įvesties vietoje** būsenoje.</span><span class="sxs-lookup"><span data-stu-id="6152f-139">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="6152f-140">Apdorojus darbą būsena gali būti **Paimta** arba **Rezervuota faktiškai**.</span><span class="sxs-lookup"><span data-stu-id="6152f-140">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="6152f-141">Tai konfigūruojama naudojant parametrą **išdavimo būsena pateikus sandėlio formoje**.</span><span class="sxs-lookup"><span data-stu-id="6152f-141">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="6152f-142">Kliente arba kišeniniame įrenginyje naudodami meniu elementą **Gamybos pradžia** pradėkite gamybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="6152f-142">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="6152f-143">Kai gamybos užsakymas pradėtas, naudodami kišeniniam įrenginiui skirtą darbo eigą galite registruoti medžiagų sunaudojimą.</span><span class="sxs-lookup"><span data-stu-id="6152f-143">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="6152f-144">Pradėkime užregistruodami paketo B1 25 svarų sunaudojimą.</span><span class="sxs-lookup"><span data-stu-id="6152f-144">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="6152f-145">Kišeninio įrenginio meniu pasirinkite elementus **Registruoti medžiagų** **sunaudojimą** ir įveskite tolesnę informaciją:</span><span class="sxs-lookup"><span data-stu-id="6152f-145">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="6152f-146">Gamybos užsakymo numeris.</span><span class="sxs-lookup"><span data-stu-id="6152f-146">The production order number.</span></span> 
-    <span data-ttu-id="6152f-147">Vietą, kurioje medžiaga bus sunaudota, šiuo atveju – PIL-01.</span><span class="sxs-lookup"><span data-stu-id="6152f-147">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="6152f-148">Prekės numerį RM-100.</span><span class="sxs-lookup"><span data-stu-id="6152f-148">Item number RM-100.</span></span> 
-    <span data-ttu-id="6152f-149">Paketo numerį B1.</span><span class="sxs-lookup"><span data-stu-id="6152f-149">Batch number B1.</span></span> 
-    <span data-ttu-id="6152f-150">Kiekį 25.</span><span class="sxs-lookup"><span data-stu-id="6152f-150">A quantity of 25.</span></span>

7.  <span data-ttu-id="6152f-151">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6152f-151">Select **OK**.</span></span>

<span data-ttu-id="6152f-152">Atkreipkite dėmesį, kad pranešimas „Sukurta žurnalo eilutė“ atsiranda ekrane.</span><span class="sxs-lookup"><span data-stu-id="6152f-152">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="6152f-153">Gamybos užsakyme yra atviras tipo **Gamybos išrinkimo dokumentas** žurnalas, kurio prekės numeris – RM-100, o paketo numeris – B1.</span><span class="sxs-lookup"><span data-stu-id="6152f-153">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="6152f-154">Dabar galite pasirinkti tęsti registraciją, pavyzdžiui, paketo nr. B2, ir kiekvieną kartą pasirinkus **Gerai** į atvirą žurnalą įtraukiama nauja žurnalo eilutė.</span><span class="sxs-lookup"><span data-stu-id="6152f-154">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="6152f-155">Baigę registraciją pasirinkite **Atlikta** tam, kad užregistruotumėte žurnalą ir baigtumėte darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="6152f-155">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="6152f-156">Papildomi komentarai</span><span class="sxs-lookup"><span data-stu-id="6152f-156">Additional comments</span></span> 

-   <span data-ttu-id="6152f-157">Jei vartotojas atšaukia darbo eigą, kai sukurta žurnalo eilutė, žurnalas yra neužregistruotos būsenos, tačiau, jeigu vartotojas vėliau šią darbo eigą naudos su tuo pačiu gamybos užsakymu, eilutės bus įtrauktos į atvirą, o ne į naują žurnalą.</span><span class="sxs-lookup"><span data-stu-id="6152f-157">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="6152f-158">Nauja darbo eiga taip pat palaiko serijos numerių registraciją.</span><span class="sxs-lookup"><span data-stu-id="6152f-158">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="6152f-159">Galima registruoti tik pasirinkto gamybos užsakymo arba paketinio užsakymo komplektavimo specifikacijoje ar formulėje nustatytą prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="6152f-159">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="6152f-160">Medžiagos galima sunaudoti daugiau nei numatyta.</span><span class="sxs-lookup"><span data-stu-id="6152f-160">Material can be overconsumed.</span></span> <span data-ttu-id="6152f-161">Pavyzdžiui, jei numatoma sunaudoti 100 svarų medžiagos, jos galima sunaudoti daugiau, pavyzdžiui, 105 svarus.</span><span class="sxs-lookup"><span data-stu-id="6152f-161">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]