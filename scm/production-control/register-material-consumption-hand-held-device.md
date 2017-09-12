---
title: "Medžiagų vartojimo registravimas naudojant mobilųjį įrenginį"
description: "Šioje temoje aprašoma darbo eiga, kurią naudojant galima kišeniniu įrenginiu registruoti žaliavų sunaudojimą gamybos metu."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 97d374230cc6e833b9f585de000e1252f2a78b9d
ms.openlocfilehash: 83703d962d6099ba8ac107548a569c8d1f34882f
ms.contentlocale: lt-lt
ms.lasthandoff: 08/30/2017

---

# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="d91f2-103">Medžiagų vartojimo registravimas naudojant mobilųjį įrenginį</span><span class="sxs-lookup"><span data-stu-id="d91f2-103">Register material consumption using a mobile device</span></span>
<span data-ttu-id="d91f2-104">Šioje temoje aprašoma darbo eiga, kurią naudojant galima kišeniniu įrenginiu registruoti žaliavų sunaudojimą gamybos metu.</span><span class="sxs-lookup"><span data-stu-id="d91f2-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="d91f2-105">Įžanga</span><span class="sxs-lookup"><span data-stu-id="d91f2-105">Introduction</span></span>
------------

<span data-ttu-id="d91f2-106">Ši darbo eiga aktuali, jei griežtai reikalaujama atsekti medžiagas.</span><span class="sxs-lookup"><span data-stu-id="d91f2-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="d91f2-107">Tokiais atvejais norint užtikrinti medžiagų atsekamumą reikia nurodyti tikslų sunaudojimo laiką ir kiekį.</span><span class="sxs-lookup"><span data-stu-id="d91f2-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="d91f2-108">Šį procesą galima laikyti priešingu išankstinio ar atgalinio sunaudojimo operacijoms, kai nesutampa registracijos laikas ir laikas, kada medžiagos faktiškai naudojamos.</span><span class="sxs-lookup"><span data-stu-id="d91f2-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="d91f2-109">Tai paaiškina, kodėl automatinio sunaudojimo strategijos negalima naudoti su kai kuriomis medžiagomis, kurias reikalaujama atsekti.</span><span class="sxs-lookup"><span data-stu-id="d91f2-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="d91f2-110">Pažvelkime į paprastą scenarijų, paaiškinantį, kaip nustatyti darbo eigą, kad kišeniniu įrenginiu būtų galima registruoti žaliavų sunaudojimą gamybos metu.</span><span class="sxs-lookup"><span data-stu-id="d91f2-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> [![](./media/scenario3.png)](./media/scenario3.png)

### <a name="scenario-details"></a><span data-ttu-id="d91f2-111">Išsami scenarijaus informacija</span><span class="sxs-lookup"><span data-stu-id="d91f2-111">Scenario details</span></span>

<span data-ttu-id="d91f2-112">Nepertraukiamo gamybos proceso (5) metu sunaudojama paketiniu būdu kontroliuojama žaliava RM-100.</span><span class="sxs-lookup"><span data-stu-id="d91f2-112">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="d91f2-113">Medžiaga turima vietoje Bulk-001 (1) (numerio lentelė – PL-1), kurioje yra du paketai (B1 ir B2), kuriuose yra po 100 svarų medžiagos kiekio.</span><span class="sxs-lookup"><span data-stu-id="d91f2-113">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="d91f2-114">Pateikiamas ir apdorojamas RM-100 sandėlio darbas (2), o medžiaga iš Bulk-001 paimama į gamybos įvesties vietą PIL-01 (3), kuri apibrėžta kaip kontroliuojama ne pagal numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="d91f2-114">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="d91f2-115">Mašinos operatorius pasveria medžiagą iš gamybos įvesties vietos (3) ir svorį bei paketo numerį užregistruoja kaip sunaudotus (4).</span><span class="sxs-lookup"><span data-stu-id="d91f2-115">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="d91f2-116">Dalis medžiagos apibrėžtais laiko intervalais rankiniu būdu iš gamybos įvesties vietos dedama į gamybos procesą.</span><span class="sxs-lookup"><span data-stu-id="d91f2-116">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="d91f2-117">Mašinos operatoriui dedant medžiagą, ji pasveriama ant svarstyklių ir užregistruojamas paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="d91f2-117">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="d91f2-118">Darbo eigos nustatymas, kad sunaudojimą būtų galima registruoti kišeniniu įrenginiu</span><span class="sxs-lookup"><span data-stu-id="d91f2-118">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="d91f2-119">Sukurkite baigtos prekės produktą FG-100 su komplektavimo specifikacija, kurioje yra paketiniu būdu kontroliuojama žaliava RM-100.</span><span class="sxs-lookup"><span data-stu-id="d91f2-119">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="d91f2-120">Į vietą Bulk-001 (numerio lentelė – PL-1) įtraukite du RM-100 paketus (B1 ir B2), kurių kiekis – 100.</span><span class="sxs-lookup"><span data-stu-id="d91f2-120">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="d91f2-121">Komplektavimo specifikacijos RM-100 eilutėje sunaudojimo principas nustatomas kaip **Rankinis**.</span><span class="sxs-lookup"><span data-stu-id="d91f2-121">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="d91f2-122">Gamybos įvesties vietą nustatykite kaip PIL-01.</span><span class="sxs-lookup"><span data-stu-id="d91f2-122">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="d91f2-123">Tai padaryti galite šią vietą pasirinkdami kaip numatytąją 51 sandėlio gamybos įvesties vietą.</span><span class="sxs-lookup"><span data-stu-id="d91f2-123">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="d91f2-124">Sukurkite naują mobiliojo įrenginio meniu elementą:</span><span class="sxs-lookup"><span data-stu-id="d91f2-124">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="d91f2-125">**Meniu elemento pavadinimas** – Registruoti medžiagų sunaudojimą.</span><span class="sxs-lookup"><span data-stu-id="d91f2-125">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="d91f2-126">**Pavadinimas** – Registruoti medžiagų sunaudojimą.</span><span class="sxs-lookup"><span data-stu-id="d91f2-126">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="d91f2-127">**Režimas** – Netiesioginis.</span><span class="sxs-lookup"><span data-stu-id="d91f2-127">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="d91f2-128">**Veiklos kodas** – Registruoti medžiagų sunaudojimą.</span><span class="sxs-lookup"><span data-stu-id="d91f2-128">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="d91f2-129">Meniu elementą įtraukite į mobiliojo įrenginio meniu **Gamyba**.</span><span class="sxs-lookup"><span data-stu-id="d91f2-129">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="d91f2-130">Sukurkite baigto produkto gamybos užsakymą:</span><span class="sxs-lookup"><span data-stu-id="d91f2-130">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="d91f2-131">**Prekės numeris** – FG-100</span><span class="sxs-lookup"><span data-stu-id="d91f2-131">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="d91f2-132">**Teritorija** – 5</span><span class="sxs-lookup"><span data-stu-id="d91f2-132">**Site** - 5</span></span> 
-    <span data-ttu-id="d91f2-133">**Sandėlis** – 51</span><span class="sxs-lookup"><span data-stu-id="d91f2-133">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="d91f2-134">**Kiekis** – 150</span><span class="sxs-lookup"><span data-stu-id="d91f2-134">**Quantity** - 150</span></span>

<span data-ttu-id="d91f2-135">Gamybos užsakymas **įvertinamas** bei **pateikiamas** ir sukuriamas sandėlio darbas.</span><span class="sxs-lookup"><span data-stu-id="d91f2-135">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="d91f2-136">Atlikite darbą naudodami kišeniniam įrenginiui skirtą žaliavų paėmimo darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="d91f2-136">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="d91f2-137">Taip medžiaga iš buferinės vietos bus perkelta į gamybos įvesties vietą PIL-01.</span><span class="sxs-lookup"><span data-stu-id="d91f2-137">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="d91f2-138">Baigus darbą medžiagos būsena yra **Paimta gamybos įvesties vietoje**.</span><span class="sxs-lookup"><span data-stu-id="d91f2-138">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="d91f2-139">Apdorojus darbą būsena gali būti **Paimta** arba **Rezervuota faktiškai**.</span><span class="sxs-lookup"><span data-stu-id="d91f2-139">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="d91f2-140">Tai konfigūruojama naudojant parametrą **išdavimo būsena pateikus sandėlio formoje**.</span><span class="sxs-lookup"><span data-stu-id="d91f2-140">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="d91f2-141">Kliente arba kišeniniame įrenginyje naudodami meniu elementą **Gamybos pradžia** pradėkite gamybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="d91f2-141">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="d91f2-142">Kai gamybos užsakymas pradėtas, naudodami kišeniniam įrenginiui skirtą darbo eigą galite registruoti medžiagų sunaudojimą.</span><span class="sxs-lookup"><span data-stu-id="d91f2-142">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="d91f2-143">Pradėkime registruodami paketo B1 25 svarų sunaudojimą.</span><span class="sxs-lookup"><span data-stu-id="d91f2-143">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="d91f2-144">Kišeninio įrenginio meniu pasirinkite elementą **Registruoti medžiagų** **sunaudojimą** ir įveskite tolesnę informaciją.</span><span class="sxs-lookup"><span data-stu-id="d91f2-144">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="d91f2-145">Gamybos užsakymo numeris.</span><span class="sxs-lookup"><span data-stu-id="d91f2-145">The production order number.</span></span> 
-    <span data-ttu-id="d91f2-146">Vietą, kurioje medžiaga bus sunaudota, šiuo atveju – PIL-01.</span><span class="sxs-lookup"><span data-stu-id="d91f2-146">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="d91f2-147">Prekės numerį RM-100.</span><span class="sxs-lookup"><span data-stu-id="d91f2-147">Item number RM-100.</span></span> 
-    <span data-ttu-id="d91f2-148">Paketo numerį B1.</span><span class="sxs-lookup"><span data-stu-id="d91f2-148">Batch number B1.</span></span> 
-    <span data-ttu-id="d91f2-149">Kiekį – 25.</span><span class="sxs-lookup"><span data-stu-id="d91f2-149">A quantity of 25.</span></span>

7.  <span data-ttu-id="d91f2-150">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d91f2-150">Select **OK**.</span></span>

<span data-ttu-id="d91f2-151">Atkreipkite dėmesį, kad ekrane atsiranda pranešimas „Sukurta žurnalo eilutė‟.</span><span class="sxs-lookup"><span data-stu-id="d91f2-151">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="d91f2-152">Gamybos užsakyme yra atviras tipo **Gamybos išrinkimo dokumentas** žurnalas, kurio prekės numeris – RM-100, o paketo numeris – B1.</span><span class="sxs-lookup"><span data-stu-id="d91f2-152">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="d91f2-153">Dabar galite pasirinkti tęsti registraciją, pavyzdžiui, paketo nr. B2, ir kiekvieną kartą pasirinkus **Gerai** į atvirą žurnalą įtraukiama nauja žurnalo eilutė.</span><span class="sxs-lookup"><span data-stu-id="d91f2-153">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="d91f2-154">Baigę registraciją pasirinkite **Atlikta** – žurnalas užregistruojamas, o darbo eiga baigiama.</span><span class="sxs-lookup"><span data-stu-id="d91f2-154">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="d91f2-155">Papildomi komentarai</span><span class="sxs-lookup"><span data-stu-id="d91f2-155">Additional comments</span></span> 

-   <span data-ttu-id="d91f2-156">Jei vartotojas atšaukia darbo eigą, kai sukurta žurnalo eilutė, žurnalas yra neužregistruotos būsenos, tačiau, jei vartotojas vėliau šią darbo eigą naudos su tuo pačiu gamybos užsakymu, eilutės bus įtrauktos į atvirą, o ne į naują žurnalą.</span><span class="sxs-lookup"><span data-stu-id="d91f2-156">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="d91f2-157">Naujoje darbo eigoje taip pat galima registruoti serijos numerius.</span><span class="sxs-lookup"><span data-stu-id="d91f2-157">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="d91f2-158">Galima registruoti tik pasirinkto gamybos užsakymo arba paketinio užsakymo komplektavimo specifikacijoje ar formulėje nustatytą prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="d91f2-158">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="d91f2-159">Medžiagos galima sunaudoti daugiau nei numatyta.</span><span class="sxs-lookup"><span data-stu-id="d91f2-159">Material can be overconsumed.</span></span> <span data-ttu-id="d91f2-160">Pavyzdžiui, jei numatoma sunaudoti 100 svarų medžiagos, jos galima sunaudoti daugiau, pavyzdžiui, 105 svarus.</span><span class="sxs-lookup"><span data-stu-id="d91f2-160">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>



