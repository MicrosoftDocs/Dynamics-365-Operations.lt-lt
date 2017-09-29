---
title: "Operacijų planavimo parinktys"
description: "Šioje temoje aprašomos operacijų planavimo parinktys. Galite naudoti operacijų planavimą, norėdami bendrai įvertinti gamybos procesą per tam tikrą laikotarpį."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 198123
ms.assetid: d680d7be-da64-4132-89fe-ad2fa59afb77
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5a64445b58c3d6b523b766b4e864aeea9f93de2b
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="operations-scheduling-options"></a><span data-ttu-id="ceb1f-104">Operacijų planavimo parinktys</span><span class="sxs-lookup"><span data-stu-id="ceb1f-104">Operations scheduling options</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ceb1f-105">Šioje temoje aprašomos operacijų planavimo parinktys.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-105">This topic describes the options for operations scheduling.</span></span> <span data-ttu-id="ceb1f-106">Galite naudoti operacijų planavimą, norėdami bendrai įvertinti gamybos procesą per tam tikrą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-106">You can use operations scheduling to provide a general estimate of the production process over time.</span></span>

<span data-ttu-id="ceb1f-107">Operacijų planavimo metu apskaičiuojama toliau nurodyta gamybos užsakymo informacija.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-107">Operations scheduling calculates the following information for a production order:</span></span>

-   <span data-ttu-id="ceb1f-108">Nustatomos gamybos užsakymo ir kiekvienos operacijos pradžios ir pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-108">Start and end dates are set for the production order and each operation.</span></span>
-   <span data-ttu-id="ceb1f-109">Ištekliai priskiriami operacijoms.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-109">Resources are assigned to operations.</span></span>

<span data-ttu-id="ceb1f-110">Keli parametrai nustato, kaip skaičiuojamas gamybos planavimas.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-110">Several settings determine how production schedules are calculated.</span></span> <span data-ttu-id="ceb1f-111">Šiuos parametrus galite nustatyti puslapyje **Operacijų planavimas**.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-111">You define these settings on the **Operations scheduling** page.</span></span> <span data-ttu-id="ceb1f-112">Toliau apibūdinamos planavimo pasirinktys.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-112">The following information describes the scheduling options.</span></span>

## <a name="operations-scheduling"></a><span data-ttu-id="ceb1f-113">Operacijų planavimas</span><span class="sxs-lookup"><span data-stu-id="ceb1f-113">Operations scheduling</span></span>
### <a name="scheduling-direction"></a><span data-ttu-id="ceb1f-114">Planavimo kryptis</span><span class="sxs-lookup"><span data-stu-id="ceb1f-114">Scheduling direction</span></span>

<span data-ttu-id="ceb1f-115">Planavimo kryptis yra esminė planavimo proceso dalis.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-115">The scheduling direction is fundamental to the scheduling process.</span></span> <span data-ttu-id="ceb1f-116">Gamybą galima planuoti pirmyn arba atgal nuo bet kurios datos, atsižvelgiant į laiko ir planavimo poreikius.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-116">A production can be scheduled forward or backward from any date, depending on timing and scheduling requirements.</span></span>

-   <span data-ttu-id="ceb1f-117">**Planavimas į priekį** – galite planuoti, kad gamyba būtų pradedama kaip įmanoma anksčiau.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-117">**Forward scheduling** – You can schedule a production to start as early as possible.</span></span> <span data-ttu-id="ceb1f-118">Gamybą galima pradėti šiandien, rytoj ar nuo bet kurios kitos konkrečios datos ateityje.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-118">The production can be started today, tomorrow, or on any specific date in the future.</span></span> <span data-ttu-id="ceb1f-119">Gamyba suplanuojama taip, kad būtų pradėta anksčiausią įmanomą datą ir būtų baigta anksčiausią įmanomą datą.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-119">The production is scheduled to start on the earliest possible date and is planned forward in time to the earliest possible end date.</span></span>
-   <span data-ttu-id="ceb1f-120">**Atgalinis planavimas** – galite planuoti, kad gamyba būtų pradedama kaip įmanoma vėliau.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-120">**Backward scheduling** – You can schedule a production to start as late as possible.</span></span> <span data-ttu-id="ceb1f-121">Grafikas paremtas data, kada gamyba turi būti užbaigta, ir skaičiuoja atgal iki vėliausios galimos datos, nuo kurios galima pradėti gamybą, nepraleidžiant jos tikslinio termino.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-121">The schedule is based on the date when the production must be completed and counts backward to the latest possible date that the production can be started without missing its target deadline.</span></span>

<span data-ttu-id="ceb1f-122">Galimos toliau nurodytos pasirinktys:</span><span class="sxs-lookup"><span data-stu-id="ceb1f-122">The following options are available:</span></span>

-   <span data-ttu-id="ceb1f-123">**Pirmyn nuo šiandien** – planavimas pirmyn nuo esamos datos.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-123">**Forward from today** – Schedule forward from the current date.</span></span> <span data-ttu-id="ceb1f-124">(Dabartinė data yra sistemos data.)</span><span class="sxs-lookup"><span data-stu-id="ceb1f-124">(The current date is the system date.)</span></span>
-   <span data-ttu-id="ceb1f-125">**Pirmyn nuo suplanuotos pradžios** – planavimas pirmyn nuo ankstesnės pradžios datos.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-125">**Forward from planned start** – Schedule forward from an earlier start date.</span></span> <span data-ttu-id="ceb1f-126">Jei anksčiau planuota nebuvo, planavimo kryptis yra pirmyn nuo esamos datos.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-126">If there is no previous scheduling, the scheduling direction is forward from the current date.</span></span>
-   <span data-ttu-id="ceb1f-127">**Pirmyn nuo planavimo datos** – planavimas pirmyn nuo datos, nurodytos lauke **Planavimo data**.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-127">**Forward from scheduling date** – Schedule forward from the date that is specified in the **Scheduling date** field.</span></span> <span data-ttu-id="ceb1f-128">Jei nenurodote planavimo datos, planavimo kryptis yra pirmyn nuo esamos datos.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-128">If you don't specify a scheduling date, the scheduling direction is forward from the current date.</span></span>
-   <span data-ttu-id="ceb1f-129">**Atgal nuo pristatymo datos** – planavimas atgal nuo pristatymo datos, nurodytos gamybos užsakyme.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-129">**Backward from delivery date** – Schedule backward from the delivery date that is specified for the production order.</span></span> <span data-ttu-id="ceb1f-130">Jei pasirinksite šią parinktį, o pristatymo data nebus nurodyta, esama data bus pristatymo data.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-130">If you select this option, but no delivery date is specified, the delivery date is the current date.</span></span>
-   <span data-ttu-id="ceb1f-131">**Atgal nuo suplanuotos pabaigos** – planavimas atgal nuo anksčiau apskaičiuotos pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-131">**Backward from planned end** – Schedule backward from a previously calculated end date.</span></span> <span data-ttu-id="ceb1f-132">Jei nėra jokio ankstesnio planavimo, dabartinė data yra pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-132">If there is no previous scheduling, the end date is the current date.</span></span>
-   <span data-ttu-id="ceb1f-133">**Atgal nuo planavimo datos** – planavimas atgal nuo datos, nurodytos lauke **Planavimo data**.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-133">**Backward from scheduling date** – Schedule backward from the date that is specified in the **Scheduling date** field.</span></span> <span data-ttu-id="ceb1f-134">Jei nenurodote planavimo datos, naudojama esama data.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-134">If you don't specify a scheduling date, the current date is used.</span></span> <span data-ttu-id="ceb1f-135">Lauko Atgal nuo planavimo datos reikšmė apskaičiuojama pagal paskutinį kartą skaičiuotą gamybos užsakymo poreikį.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-135">Backward from scheduling date is calculated for the production order the last time that a requirement was calculated.</span></span> <span data-ttu-id="ceb1f-136">Jei nenurodyta jokia gamybos užsakymo data, naudojama esama sistemos data.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-136">If no date is specified for the production order, the current system date is used.</span></span>
-   <span data-ttu-id="ceb1f-137">**Atgal nuo ateities datos** – planavimas atgal nuo ateities datos, apskaičiuotos pagal paskutinį kartą skaičiuotą gamybos užsakymo poreikį.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-137">**Backward from futures date** – Schedule backward from the futures date that was calculated for the production order the last time that a requirement was calculated.</span></span> <span data-ttu-id="ceb1f-138">Jei nenurodyta jokia gamybos užsakymo ateities data, naudojama esama sistemos data.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-138">If no futures date is specified for the production order, the current system date is used.</span></span>
-   <span data-ttu-id="ceb1f-139">**Kaip per paskutinį planavimą** – įrašant operacijas ir užduočių planavimą kartu įrašoma pasirinkta planavimo kryptis ir data.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-139">**As last scheduling** – For operations scheduling and job scheduling, the selected scheduling direction and date are saved.</span></span> <span data-ttu-id="ceb1f-140">Todėl šią pasirinktį galite taikyti būsimiems planavimams.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-140">Therefore, you can select this option for subsequent scheduling.</span></span> <span data-ttu-id="ceb1f-141">Jei anksčiau nevykdytas gamybos užsakymo planavimas, planavimas vykdomas atgal nuo esamos sistemos datos.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-141">If there is no previous scheduling of the production order, scheduling is backward from the current system date.</span></span>
-   <span data-ttu-id="ceb1f-142">**Pradedant nuo rytojaus** – planavimas pradedant nuo esamos datos + viena diena.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-142">**Forward from tomorrow** – Schedule forward from the current date plus one day.</span></span>
-   <span data-ttu-id="ceb1f-143">**Pirmyn nuo ankstesnės užduoties** – ši funkcija tinkama tik užduotims planuoti.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-143">**Forward from previous job** – This option is relevant only in job scheduling.</span></span> <span data-ttu-id="ceb1f-144">Jei operacijoms planuoti pasirenkate šią planavimo kryptį, gamybos užsakymas bus planuojamas pirmyn nuo esamos datos.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-144">If you select this scheduling direction for operations scheduling, the production order is scheduled forward from the current date.</span></span> <span data-ttu-id="ceb1f-145">Planuojant užduotis nustatomas vienos užduoties planavimas, o visos kitos gamybos užduotys planuojamos pagal tą užduotį.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-145">In job scheduling, scheduling is established for one job, and all other jobs for the production are scheduled based on that job.</span></span>
-   <span data-ttu-id="ceb1f-146">**Atgal nuo ankstesnės užduoties** – ši parinktis tinkama tik užduotims planuoti.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-146">**Backward from previous job** – This option is relevant only in job scheduling.</span></span> <span data-ttu-id="ceb1f-147">Jei pasirinksite šią operacijų planavimo kryptį, suplanuoti užsakymai bus planuojami atgal nuo esamos datos.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-147">If you select this scheduling direction for operations scheduling, planned orders are scheduled backward from the current date.</span></span> <span data-ttu-id="ceb1f-148">Planuojant užduotis nustatomas vienos užduoties planavimas, o visos kitos gamybos užduotys planuojamos pagal tą užduotį.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-148">In job scheduling, scheduling is established for one job, and all other jobs for the production are scheduled based on that job.</span></span>

### <a name="scheduling-date"></a><span data-ttu-id="ceb1f-149">Planavimo data</span><span class="sxs-lookup"><span data-stu-id="ceb1f-149">Scheduling date</span></span>

<span data-ttu-id="ceb1f-150">Ši data naudojama planavimo kryptyse **Pirmyn nuo planavimo datos** ir **Atgal nuo planavimo datos**.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-150">This date is used for the **Forward from scheduling date** and **Backward from scheduling date** scheduling directions.</span></span> <span data-ttu-id="ceb1f-151">Planuojama atgal arba pirmyn nuo šios datos.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-151">Scheduling is backward or forward from this date.</span></span> <span data-ttu-id="ceb1f-152">Daugiau informacijos žr. ankstesniame skyriuje „Planavimo kryptis“.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-152">For more information, see the previous section, "Scheduling direction."</span></span>

### <a name="recalculate-bom-levels"></a><span data-ttu-id="ceb1f-153">Perskaičiuoti KS lygius</span><span class="sxs-lookup"><span data-stu-id="ceb1f-153">Recalculate BOM levels</span></span>

<span data-ttu-id="ceb1f-154">Kai pasirenkate **Perskaičiuoti KS lygius**, bus perskaičiuoti pasirinktos komplektavimo specifikacijos (KS) lygiai, kad būtų užtikrinta teisinga planavimo tvarka.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-154">When you select **Recalculate BOM levels**, the selected bill of materials (BOM) levels will be recalculated to help guarantee the correct scheduling order.</span></span>

## <a name="limitations"></a><span data-ttu-id="ceb1f-155">Apribojimai</span><span class="sxs-lookup"><span data-stu-id="ceb1f-155">Limitations</span></span>
### <a name="finite-capacity"></a><span data-ttu-id="ceb1f-156">Ribotas pajėgumas</span><span class="sxs-lookup"><span data-stu-id="ceb1f-156">Finite capacity</span></span>

<span data-ttu-id="ceb1f-157">Planavimas priklauso nuo išteklių centrų, reikalingų gamybai užbaigti, prieinamumo.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-157">Scheduling depends on the availability of the resources that are required in order to complete production.</span></span> <span data-ttu-id="ceb1f-158">Jei nėra pakankamai pajėgumų, gamybos užsakymus galima atidėti arba net sustabdyti.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-158">If there isn't enough capacity, production orders can be delayed or even stopped.</span></span> <span data-ttu-id="ceb1f-159">Jei operacijų planavime taikomas ribotas pajėgumas, naudojami esami išteklių pajėgumų rezervavimai ir tas pajėgumas rodomas kaip negalimas.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-159">If finite capacity is applied to operations scheduling, existing capacity reservations that are made on the resources are considered, and that capacity is seen as unavailable.</span></span> <span data-ttu-id="ceb1f-160">Gamybos užsakymas planuojamas pagal reikalingų išteklių pajėgumo prieinamumą.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-160">The production order is scheduled based on the availability of capacity on the resources that are required.</span></span> <span data-ttu-id="ceb1f-161">Operacijų planavime naudojama nurodyta operacijų seka, kad būtų nustatyta gamybos maršruto operacijų tvarka.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-161">Operations scheduling uses the specified sequence of operations to determine the order of operations in the production route.</span></span> <span data-ttu-id="ceb1f-162">Operacijų planavimas rezervuoja pajėgumą išteklių grupėse pagal operacijų laiką, nurodytą gamybos maršruto.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-162">Operations scheduling reserves capacity on the resource groups, based on the operation times that are defined on the production route.</span></span> <span data-ttu-id="ceb1f-163">Išteklių grupių pajėgumas yra visų išteklių grupių išteklių galimų pajėgumų suma.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-163">The capacity of the resource groups is the sum of available capacity on all the resources in the resource groups.</span></span>

### <a name="finite-material"></a><span data-ttu-id="ceb1f-164">Ribotos medžiagos</span><span class="sxs-lookup"><span data-stu-id="ceb1f-164">Finite material</span></span>

<span data-ttu-id="ceb1f-165">Planavimas taip pat yra priklausomas nuo gamybai reikalingų medžiagų prieinamumo.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-165">Scheduling also depends on the availability of the materials that are required for production.</span></span> <span data-ttu-id="ceb1f-166">Nepakankamas komponentų prieinamumas taip pat gali būti gamybos atidėjimo priežastis.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-166">Insufficient component availability can also cause production delays.</span></span> <span data-ttu-id="ceb1f-167">Planavimas taip pat gali būti paremtas ir medžiagų naudojimu.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-167">Scheduling can also be based on the use of materials.</span></span> <span data-ttu-id="ceb1f-168">Tiesiog nurodykite gamybos medžiagas, kurios turi būti prieinamos, o ne medžiagas, kurios nėra svarbios.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-168">Just specify the materials that must be available for production instead of the materials that aren't critical.</span></span> <span data-ttu-id="ceb1f-169">Tokio tipo planavimas vadinamas planavimu turint ribą medžiagų kiekį.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-169">This type of scheduling is known as scheduling with finite material.</span></span> <span data-ttu-id="ceb1f-170">Kai nurodote ribotas medžiagas, gamyba planuojama pagal tai, ar medžiagos prieinamos.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-170">When you specify finite materials, production is scheduled based on whether materials are available.</span></span> <span data-ttu-id="ceb1f-171">**Pastaba.** Optimizuojant ir pajėgumą, ir medžiagas, gamyba apskaičiuojama taip, kad atitiktų abu apribojimus.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-171">**Note:** When you optimize on both capacity and materials, production is calculated to meet both restrictions.</span></span> <span data-ttu-id="ceb1f-172">Įvertinamas pajėgumo ir medžiagų prieinamumas ir negalima suplanuoti gamybos užsakymo operacijų vykdymo pradžios, jei tuo pačiu metu nėra reikiamo kiekio pajėgumo ir medžiagų.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-172">The availability of capacity and materials is considered, and the production order’s operations can't be scheduled to start until capacity and materials are available at the same time and in the required quantities.</span></span> <span data-ttu-id="ceb1f-173">Pažymėkite šį žymės langelį, jei planavimo metu medžiagas reikėtų laikyti ribotomis.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-173">Select this check box if materials should be considered limited during scheduling.</span></span> <span data-ttu-id="ceb1f-174">Jei medžiagos yra ribotos, bus atsižvelgiama į to laikotarpio medžiagų padengimą.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-174">If the materials are limited, the material's coverage for that time will be considered.</span></span> <span data-ttu-id="ceb1f-175">Kitaip tariant, planuojant atsižvelgiama į apskaičiuotas prekių ateities datas.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-175">In other words, scheduling considers the futures dates that are calculated for the items.</span></span> <span data-ttu-id="ceb1f-176">Planuojant rezervuojamos žaliavos ir išskleidžiama esama gamyba.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-176">Scheduling reserves raw materials and explodes the current production.</span></span> <span data-ttu-id="ceb1f-177">Jei planavimas vyksta keletą kartų, tik pirmojo planavimo metu vykdomas išskleidimas ir atliekami rezervavimai.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-177">If scheduling occurs several times, only the first scheduling runs an explosion and makes reservations.</span></span> <span data-ttu-id="ceb1f-178">Jei gamybos KS arba maršrute atliksite pakeitimų, išskleidžiama bus kito planavimo metu.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-178">If you make changes in the production BOM or route, the next scheduling runs an explosion.</span></span> <span data-ttu-id="ceb1f-179">Išskleidžiant bus manoma, kad medžiagos reikalingos tą pačią dieną.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-179">For the explosion, it's assumed that the materials are required on the same day.</span></span> <span data-ttu-id="ceb1f-180">Kadangi gamyba nesuplanuojama išskleidžiant bendrąjį planą, dabartinė data yra tinkamiausias įvertinimas, kada bus galima gauti prekes.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-180">Because the production isn't scheduled at the time of the master schedule explosion, the current date is the best estimate of when the items will be available.</span></span> <span data-ttu-id="ceb1f-181">Tada išskleidimo metu tikrinama, ar prekės galimos.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-181">The explosion then checks whether the items are available.</span></span> <span data-ttu-id="ceb1f-182">Jei prekės yra prieinamos, galima patenkinti gamybos poreikį.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-182">If the items are available, the production requirement can be fulfilled.</span></span> <span data-ttu-id="ceb1f-183">Jei šiuo metu prekės neprieinamos, sugeneruojamas suplanuotas užsakymas ir atliekamas korespondentinis suplanuoto užsakymo pasirinkimas.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-183">If the items aren't available by the current date, a planned order is generated, and an offset selection is made for the planned order.</span></span> <span data-ttu-id="ceb1f-184">Jei nustatytas automatinis suplanuoto užsakymo patvirtinimas, tada suplanuotas pirkimo ar gamybos užsakymas bus automatiškai patvirtintas.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-184">If automatic firming is set for the planned order, the planned order is firmed automatically for purchase or production.</span></span> <span data-ttu-id="ceb1f-185">Gamybos būsena automatiškai pasikeis į būseną, nurodytą dialogo lango **Padengimo grupės** lauke **Reikalaujama gamybos būsena**.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-185">The production status is automatically changed to the status that is specified in the **Requested production status** field in the **Coverage groups** dialog box.</span></span> <span data-ttu-id="ceb1f-186">Jei žymės langelis nepažymėtas, bus laikoma, kad medžiagų yra.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-186">If the check box is cleared, the materials are always considered available.</span></span> <span data-ttu-id="ceb1f-187">Dėl to planuojant neatsižvelgiama į tai, ar medžiagos yra pasiekiamos reikalavimo metu.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-187">Therefore, scheduling doesn't consider whether the materials are available at the time of requirement.</span></span>

### <a name="finite-property"></a><span data-ttu-id="ceb1f-188">Ribota ypatybė</span><span class="sxs-lookup"><span data-stu-id="ceb1f-188">Finite property</span></span>

<span data-ttu-id="ceb1f-189">Pažymėti šį žymės langelį, jei norima leisti ypatybių reikalavimus planuojant užduotis.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-189">Select this check box if the job scheduling should include property requirements.</span></span>

### <a name="keep-production-unit"></a><span data-ttu-id="ceb1f-190">Išlaikyti gamybos vienetą</span><span class="sxs-lookup"><span data-stu-id="ceb1f-190">Keep production unit</span></span>

<span data-ttu-id="ceb1f-191">Pasirinkite, ar planavimo mechanizmas turėtų planuoti tik išteklius, kurie jau yra nurodyti gamybos vienete.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-191">Select whether the scheduling engine should schedule only resources that are already specified on the production unit.</span></span>

### <a name="keep-warehouse-from-resource"></a><span data-ttu-id="ceb1f-192">Išlaikyti sandėlį iš išteklių</span><span class="sxs-lookup"><span data-stu-id="ceb1f-192">Keep warehouse from resource</span></span>

<span data-ttu-id="ceb1f-193">Pasirinkite, ar planavimo mechanizmas turėtų planuoti tik išteklius, susietus su nurodytu ištekliaus tiekimo sandėliu.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-193">Select whether the scheduling engine should schedule only resources that are associated with the input warehouse that is specified on the resource.</span></span>

## <a name="references"></a><span data-ttu-id="ceb1f-194">Nuorodos</span><span class="sxs-lookup"><span data-stu-id="ceb1f-194">References</span></span>
### <a name="schedule-references"></a><span data-ttu-id="ceb1f-195">Grafiko nuorodos</span><span class="sxs-lookup"><span data-stu-id="ceb1f-195">Schedule references</span></span>

<span data-ttu-id="ceb1f-196">Kai nuorodos priklauso nuo gamybos užsakymų, jos taip pat vadinamos tarpinėmis gamybomis.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-196">When references depend on production orders, they are also known as subproductions.</span></span> <span data-ttu-id="ceb1f-197">Tarpines gamybas galima planuoti kaip gamybos užsakymo planavimo dalį.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-197">Subproductions can be scheduled as part of the scheduling of a production order.</span></span> <span data-ttu-id="ceb1f-198">Pažymėkite šį žymės langelį, jei tarpinių gamybų planavimas turi būti pagrįstas pagrindinės gamybos planavimu.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-198">Select this check box if the scheduling of subproductions should be based on the scheduling of the main production.</span></span> <span data-ttu-id="ceb1f-199">Siejant su pagrindine gamyba, aukščiau esanti gamyba planuojama į priekį, o žemiau esanti gamyba – atgal.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-199">In relation to the main production, overlying productions are scheduled forward, and underlying productions are scheduled backward.</span></span> <span data-ttu-id="ceb1f-200">Gamybos užsakymo nuorodas galima peržiūrėti puslapio **Gamybos užsakymai** lauke **Nuorodos lygis**.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-200">You can view production order references can be viewed in the **Reference level** field on the **Production orders** page.</span></span>

### <a name="synchronize-references"></a><span data-ttu-id="ceb1f-201">Sinchronizuoti nuorodas</span><span class="sxs-lookup"><span data-stu-id="ceb1f-201">Synchronize references</span></span>

<span data-ttu-id="ceb1f-202">Jūs taip pat galite nuorodas sinchronizuoti su gamybos užsakymu.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-202">You can synchronize references with the production order.</span></span> <span data-ttu-id="ceb1f-203">Jei pasirenkama ši parinktis, tarpinės gamybos datos perkeliamos sulygiuojamos, kai keičiamas gamybos užsakymo grafikas.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-203">If this option is selected, the dates of the subproductions are moved and aligned when changes are made to the production order’s schedule.</span></span> <span data-ttu-id="ceb1f-204">Jei produkto užsakymui priskirta viena ar daugiau tarpinių gamybų, galite tarpines gamybas planuoti kartu su pagrindine gamyba.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-204">If a production order has one or more subproductions, you might want to schedule the subproductions together with the main production.</span></span> <span data-ttu-id="ceb1f-205">Šiuo atveju pagrindinės gamybos negalima pradėti, kol susijusios tarpinės gamybos nebus baigtos.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-205">In this case, the main production can't be started until the related subproductions have been completed.</span></span> <span data-ttu-id="ceb1f-206">Todėl pažymėkite šį žymės langelį, jei tarpinių gamybų planavimas turi būti pagrįstas pasirinktos gamybos pradžios ir pabaigos laiku.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-206">Therefore, select this check box if the scheduling of subproductions should be based on the start and end times of the selected production.</span></span> <span data-ttu-id="ceb1f-207">Galite pažymėti šį žymės langelį tik jei žymės langelis **Grafiko nuorodos** yra taip pat pažymėtas.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-207">You can select this check box only if the **Schedule references** check box is also selected.</span></span>

## <a name="cancellation"></a><span data-ttu-id="ceb1f-208">Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="ceb1f-208">Cancellation</span></span>
### <a name="cancel-queue-time"></a><span data-ttu-id="ceb1f-209">Atšaukti laukimo darbo grupėje laiką</span><span class="sxs-lookup"><span data-stu-id="ceb1f-209">Cancel queue time</span></span>

<span data-ttu-id="ceb1f-210">Pažymėkite šį žymės langelį norėdami laukimo eilėje laiko neįtraukti į planavimą.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-210">Select this check box to exclude queue time from the scheduling.</span></span>

### <a name="cancel-setup"></a><span data-ttu-id="ceb1f-211">Atšaukti nustatymus</span><span class="sxs-lookup"><span data-stu-id="ceb1f-211">Cancel setup</span></span>

<span data-ttu-id="ceb1f-212">Pažymėkite šį žymės langelį norėdami sąrankos laiko neįtraukti į planavimą.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-212">Select this check box to exclude setup time from the scheduling.</span></span>

### <a name="cancel-process"></a><span data-ttu-id="ceb1f-213">Atšaukti procesą</span><span class="sxs-lookup"><span data-stu-id="ceb1f-213">Cancel process</span></span>

<span data-ttu-id="ceb1f-214">Pažymėkite šį žymės langelį norėdami vykdymo laiko neįtraukti į planavimą.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-214">Select this check box to exclude run time from the scheduling.</span></span>

### <a name="cancel-overlap"></a><span data-ttu-id="ceb1f-215">Atšaukti persidengimą</span><span class="sxs-lookup"><span data-stu-id="ceb1f-215">Cancel overlap</span></span>

<span data-ttu-id="ceb1f-216">Pažymėkite šį žymės langelį norėdami persidengiančio laiko neįtraukti į planavimą.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-216">Select this check box to exclude overlap time from the scheduling.</span></span>

### <a name="cancel-transport"></a><span data-ttu-id="ceb1f-217">Atšaukti transportavimą</span><span class="sxs-lookup"><span data-stu-id="ceb1f-217">Cancel transport</span></span>

<span data-ttu-id="ceb1f-218">Pažymėkite šį žymės langelį norėdami tranzito laiko neįtraukti į planavimą.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-218">Select this check box to exclude transit time from the scheduling.</span></span>

## <a name="set-default"></a><span data-ttu-id="ceb1f-219">Nustatyti numatytąją</span><span class="sxs-lookup"><span data-stu-id="ceb1f-219">Set default</span></span>
<span data-ttu-id="ceb1f-220">Galite išsaugoti dabartines reikšmes kaip numatytąsias reikšmes.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-220">You can save the current values as default values.</span></span> <span data-ttu-id="ceb1f-221">Galima naudoti dvi parinktis.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-221">There are two options:</span></span>

-   <span data-ttu-id="ceb1f-222">Nustatyti kaip mano numatytąjį parametrą</span><span class="sxs-lookup"><span data-stu-id="ceb1f-222">Set as my default</span></span>
-   <span data-ttu-id="ceb1f-223">Nustatyti kaip visų numatytąjį parametrą</span><span class="sxs-lookup"><span data-stu-id="ceb1f-223">Set as default for everyone</span></span>


<a name="see-also"></a><span data-ttu-id="ceb1f-224">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="ceb1f-224">See also</span></span>
--------

[<span data-ttu-id="ceb1f-225">Operacijų planavimas</span><span class="sxs-lookup"><span data-stu-id="ceb1f-225">Operations scheduling</span></span>](operations-scheduling.md)



