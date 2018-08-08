---
title: "Nustatyti valdymo būtinąsias sąlygas"
description: "Naudokite šią procedūrą, kad įgalintumėte neatitikčių valdymo procesus."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 084b1dc840f147371bb9156376d4819f0f810915
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-prerequisites-for-management"></a><span data-ttu-id="56043-103">Nustatyti valdymo būtinąsias sąlygas</span><span class="sxs-lookup"><span data-stu-id="56043-103">Set up prerequisites for management</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="56043-104">Naudokite šią procedūrą, kad įgalintumėte neatitikčių valdymo procesus.</span><span class="sxs-lookup"><span data-stu-id="56043-104">Use this procedure to enable nonconformance management processes.</span></span> <span data-ttu-id="56043-105">Neatitiktyje apibūdinama procedūra arba prekė, kuri turi kokybės problemų, aprašomojoje informacijoje pateiktas problemos šaltinis ir tipas.</span><span class="sxs-lookup"><span data-stu-id="56043-105">A nonconformance describes a procedure or item that has a quality problem, where the descriptive information includes the source and type of problem.</span></span> <span data-ttu-id="56043-106">Šioje procedūroje naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="56043-106">This procedure uses the USMF demo data company.</span></span> <span data-ttu-id="56043-107">Šią procedūrą paprastai atlieka kokybės vadovas.</span><span class="sxs-lookup"><span data-stu-id="56043-107">This procedure is typically performed by a quality manager.</span></span>


## <a name="enable-quality-management-processes-within-the-company"></a><span data-ttu-id="56043-108">Kokybės valdymo procesų įmonėje įgalinimas</span><span class="sxs-lookup"><span data-stu-id="56043-108">Enable quality management processes within the company</span></span>
1. <span data-ttu-id="56043-109">Pasirinkite Atsargų valdymas > Nustatymas > Atsargų ir sandėlio valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="56043-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="56043-110">Spustelėkite skirtuką Kokybės valdymas.</span><span class="sxs-lookup"><span data-stu-id="56043-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="56043-111">Lauke Naudoti kokybės valdymą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="56043-111">Select Yes in the Use quality management field.</span></span>
    * <span data-ttu-id="56043-112">Pasirinkite šį parametrą, kad įgalintumėte įmonės kokybės valdymo procesus.</span><span class="sxs-lookup"><span data-stu-id="56043-112">Select this parameter to enable quality management processes for the company.</span></span>  
4. <span data-ttu-id="56043-113">Lauke Valandinis tarifas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="56043-113">In the Hourly rate field, enter a number.</span></span>
    * <span data-ttu-id="56043-114">Naudokite lauką Valandinis tarifas, kad įvestumėte valandinį darbo tarifą vietine valiuta.</span><span class="sxs-lookup"><span data-stu-id="56043-114">Use the Hourly rate field to enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="56043-115">Valandinis tarifas naudojamas apskaičiuojant su neatitikimu susijusias operacijų išlaidas.</span><span class="sxs-lookup"><span data-stu-id="56043-115">The hourly rate is used for calculating costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="56043-116">Valandinis tarifas ir apskaičiuotos išlaidos suteikia nuorodos informacijos apie neatitiktį ir nesąveikauja su kitomis funkcijomis.</span><span class="sxs-lookup"><span data-stu-id="56043-116">The hourly rate and calculated costs provide reference information for a nonconformance, and they do not interact with other functionality.</span></span>  
5. <span data-ttu-id="56043-117">Spustelėkite Ataskaitų sąranka.</span><span class="sxs-lookup"><span data-stu-id="56043-117">Click Report setup.</span></span>
    * <span data-ttu-id="56043-118">Šiame puslapyje galima apibrėžti kokybės ataskaitų pastabų tipus, kurie bus naudojami įvairių rūšių kokybės valdymo ataskaitose.</span><span class="sxs-lookup"><span data-stu-id="56043-118">This page allows you to define the quality report note types that will be used on different kinds of quality management reports.</span></span>  
6. <span data-ttu-id="56043-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="56043-119">Close the page.</span></span>
7. <span data-ttu-id="56043-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="56043-120">Close the page.</span></span>

## <a name="enable-user-for-nonconformance-processing"></a><span data-ttu-id="56043-121">Leidimas vartotojui apdoroti neatitiktis</span><span class="sxs-lookup"><span data-stu-id="56043-121">Enable user for nonconformance processing</span></span>
1. <span data-ttu-id="56043-122">Pasirinkite Sistemos administravimas > Vartotojai > Vartotojai.</span><span class="sxs-lookup"><span data-stu-id="56043-122">Go to System administration > Users > Users.</span></span>
    * <span data-ttu-id="56043-123">Norint apdoroti neatitikties patvirtinimą, neatitiktis patvirtinusiam ar atmetusiam vartotojui puslapyje Vartotojai turi būti priskirta reikšmė Pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="56043-123">To process the approval of a nonconformance the user who  approves or rejects nonconformances must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="56043-124">Norint naudoti dokumento pastabas, vartotojui taip pat turi būti suaktyvinta vartotojo pasirinktis Dokumentų tvarkymas.</span><span class="sxs-lookup"><span data-stu-id="56043-124">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
2. <span data-ttu-id="56043-125">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="56043-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="56043-126">Pvz., filtruokite lauką Pavadinimas reikšme „Ricardo‟.</span><span class="sxs-lookup"><span data-stu-id="56043-126">For example, filter on the Name field with a value of 'Ricardo'.</span></span>
    * <span data-ttu-id="56043-127">Naudokite filtrą, kad rastumėte vartotoją, kuris tvirtins arba atmes neatitikimo įrašus.</span><span class="sxs-lookup"><span data-stu-id="56043-127">Use the filter to find the user who will be approving or rejecting the nonconformance records.</span></span>  
3. <span data-ttu-id="56043-128">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="56043-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="56043-129">Norėdami apdoroti neatitikties patvirtinimą, pasirūpinkite, kad neatitiktis patvirtinusiam ar atmetusiam vartotojui puslapyje Vartotojai būtų priskirta reikšmė Pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="56043-129">To process the approval of a nonconformance, make sure the user who approves or rejects nonconformances has a “Name” value assigned on the Users page.</span></span>  
4. <span data-ttu-id="56043-130">Spustelėkite Vartotojo parinktys.</span><span class="sxs-lookup"><span data-stu-id="56043-130">Click User options.</span></span>
5. <span data-ttu-id="56043-131">Spustelėkite skirtuką Nuostatos.</span><span class="sxs-lookup"><span data-stu-id="56043-131">Click the Preferences tab.</span></span>
6. <span data-ttu-id="56043-132">Lauke Įgalinti dokumentų tvarkymą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="56043-132">Select Yes in the Enable document handling field.</span></span>
    * <span data-ttu-id="56043-133">Norint naudoti dokumento pastabas, vartotojui taip pat turi būti suaktyvinta vartotojo pasirinktis Dokumentų tvarkymas.</span><span class="sxs-lookup"><span data-stu-id="56043-133">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
7. <span data-ttu-id="56043-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="56043-134">Close the page.</span></span>
8. <span data-ttu-id="56043-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="56043-135">Close the page.</span></span>
9. <span data-ttu-id="56043-136">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="56043-136">Close the page.</span></span>

## <a name="define-diagnostic-types-for-nonconformance-processing"></a><span data-ttu-id="56043-137">Neatitikčių apdorojimo diagnostikos tipų apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="56043-137">Define diagnostic types for nonconformance processing</span></span>
1. <span data-ttu-id="56043-138">Pasirinkite Atsargų valdymas > Nustatymas > Kokybės valdymas > Diagnostikos tipai.</span><span class="sxs-lookup"><span data-stu-id="56043-138">Go to Inventory management > Setup > Quality management > Diagnostic types.</span></span>
    * <span data-ttu-id="56043-139">Naudodami puslapį Diagnozės tipai nurodykite diagnostikos veiksmų klasifikaciją.</span><span class="sxs-lookup"><span data-stu-id="56043-139">Use the Diagnostic types page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="56043-140">Koregavimu identifikuojama, kurio diagnostinio veiksmo turi būti imtasi, atsiradus patvirtintai neatitikčiai, kas turėtų jį atlikti bei pageidaujamą ir planuojamą baigimo datą.</span><span class="sxs-lookup"><span data-stu-id="56043-140">A correction identifies what type of diagnostic action should be taken on an approved nonconformance, who should perform it, and the requested and planned completion date.</span></span>  
2. <span data-ttu-id="56043-141">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="56043-141">Click New.</span></span>
3. <span data-ttu-id="56043-142">Lauke Diagnostikos įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="56043-142">In the Diagnostic field, type a value.</span></span>
4. <span data-ttu-id="56043-143">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="56043-143">In the Description field, type a value.</span></span>
5. <span data-ttu-id="56043-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="56043-144">Close the page.</span></span>

## <a name="define-quality-charges-for-nonconformance-processing"></a><span data-ttu-id="56043-145">Neatitikčių apdorojimo kokybės išlaidų apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="56043-145">Define quality charges for nonconformance processing</span></span>
1. <span data-ttu-id="56043-146">Pasirinkite Atsargų valdymas > Nustatymas > Kokybės valdymas > Kokybės išlaidos.</span><span class="sxs-lookup"><span data-stu-id="56043-146">Go to Inventory management > Setup > Quality management > Quality charges.</span></span>
    * <span data-ttu-id="56043-147">Naudokite puslapį Kokybės išlaidos, kad apibrėžtumėte išlaidų, kurios bus naudojamos su neatitiktimis susijusiose operacijose, klasifikaciją.</span><span class="sxs-lookup"><span data-stu-id="56043-147">Use the Quality charges page to define a classification of charges that will used in operations related to nonconformances.</span></span>  
2. <span data-ttu-id="56043-148">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="56043-148">Click New.</span></span>
3. <span data-ttu-id="56043-149">Lauke Išlaidų kodas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="56043-149">In the Charges code field, type a value.</span></span>
4. <span data-ttu-id="56043-150">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="56043-150">In the Description field, type a value.</span></span>
5. <span data-ttu-id="56043-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="56043-151">Close the page.</span></span>

## <a name="define-the-operations-for-nonconformance-processing"></a><span data-ttu-id="56043-152">Neatitikčių apdorojimo operacijų apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="56043-152">Define the operations for nonconformance processing</span></span>
1. <span data-ttu-id="56043-153">Pasirinkite Atsargų valdymas > Nustatymas > Kokybės valdymas > Operacijos.</span><span class="sxs-lookup"><span data-stu-id="56043-153">Go to Inventory management > Setup > Quality management > Operations.</span></span>
    * <span data-ttu-id="56043-154">Norėdami nurodyti darbų, kurie gali būti atlikti atsiradus patvirtintai neatitikčiai, klasifikaciją, naudokite puslapį Operacijos.</span><span class="sxs-lookup"><span data-stu-id="56043-154">Use the Operations page to define a classification of the work that may be performed for an approved nonconformance.</span></span> <span data-ttu-id="56043-155">Susiję operaciją su neatitiktimi galite nurodyti informaciją apie susijusią medžiagą, darbo valandas ir papildomas išlaidas, būtinas atliekant operaciją.</span><span class="sxs-lookup"><span data-stu-id="56043-155">When you relate an operation to a nonconformance, you can define information about the associated material, labor hours, and miscellaneous charges that are required to perform the operation.</span></span> <span data-ttu-id="56043-156">Šia informacija bus remiamasi skaičiuojant operacijos atlikimo numatytas išlaidas.</span><span class="sxs-lookup"><span data-stu-id="56043-156">This information provides the basis for calculating an estimated cost for performing the operation.</span></span>  
2. <span data-ttu-id="56043-157">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="56043-157">Click New.</span></span>
3. <span data-ttu-id="56043-158">Lauke Operacija įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="56043-158">In the Operation field, type a value.</span></span>
4. <span data-ttu-id="56043-159">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="56043-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="56043-160">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="56043-160">Close the page.</span></span>

## <a name="define-problem-types-for-nonconformance-processing"></a><span data-ttu-id="56043-161">Neatitikčių apdorojimo problemų tipų apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="56043-161">Define problem types for nonconformance processing</span></span>
1. <span data-ttu-id="56043-162">Pasirinkite Atsargų valdymas > Nustatymas > Kokybės valdymas > Problemų tipai.</span><span class="sxs-lookup"><span data-stu-id="56043-162">Go to Inventory management > Setup > Quality management > Problem types.</span></span>
    * <span data-ttu-id="56043-163">Naudodami puslapį Problemų tipai apibrėžkite kokybės problemų, su kuriomis susiduriama įvairiuose neatitikimo tipuose, klasifikaciją.</span><span class="sxs-lookup"><span data-stu-id="56043-163">Use the Problem types page to define a classification of quality problems that are encountered in the various nonconformance types.</span></span> <span data-ttu-id="56043-164">Neatitikčių tipai – tai Vidinis, Kliento, Tiekėjo, Aptarnavimo užklausos, Gamybos ir Sudėtinio produkto gamybos.</span><span class="sxs-lookup"><span data-stu-id="56043-164">The nonconformance types include Internal, Customer, Vendor, Service request, Production, and Co-product production.</span></span> <span data-ttu-id="56043-165">Vieną problemos tipą galima susieti su keliais neatitikčių tipais.</span><span class="sxs-lookup"><span data-stu-id="56043-165">A single problem type can be associated with multiple nonconformance types.</span></span>  
2. <span data-ttu-id="56043-166">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="56043-166">Click New.</span></span>
3. <span data-ttu-id="56043-167">Lauke Problemos tipas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="56043-167">In the Problem type field, type a value.</span></span>
4. <span data-ttu-id="56043-168">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="56043-168">In the Description field, type a value.</span></span>
5. <span data-ttu-id="56043-169">Spustelėkite Neatitikčių tipai.</span><span class="sxs-lookup"><span data-stu-id="56043-169">Click Non conformance types.</span></span>
    * <span data-ttu-id="56043-170">Naudokite puslapį Neatitikčių tipai, kur galite leisti priskirti problemos tipą vienam ar keliems neatitikčių tipams.</span><span class="sxs-lookup"><span data-stu-id="56043-170">Use the Non conformance types page to authorize the use of a problem type for one or more of the nonconformance types.</span></span> <span data-ttu-id="56043-171">Pavyzdžiui, problemos, susijusios su defekto kodu, tipas gali būti taikomas visiems neatitikimų tipams, tuo tarpu problemos, susijusios su klientų skundais, tipas gali būti taikomas tik klientų ir aptarnavimo užklausų neatitikimų tipams.</span><span class="sxs-lookup"><span data-stu-id="56043-171">For example, a problem type regarding a defect code could apply to all nonconformance types, whereas a problem type about customer complaints may only apply to the customer and service request nonconformance types.</span></span>  
6. <span data-ttu-id="56043-172">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="56043-172">Click New.</span></span>
7. <span data-ttu-id="56043-173">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="56043-173">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="56043-174">Lauke Neatitikties tipas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="56043-174">In the Non conformance type field, select an option.</span></span>
9. <span data-ttu-id="56043-175">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="56043-175">Close the page.</span></span>
10. <span data-ttu-id="56043-176">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="56043-176">Close the page.</span></span>

## <a name="define-quarantine-zones-for-nonconformance-processing"></a><span data-ttu-id="56043-177">Neatitikčių apdorojimo sulaikymo zonų apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="56043-177">Define quarantine zones for nonconformance processing</span></span>
1. <span data-ttu-id="56043-178">Pasirinkite Atsargų valdymas > Nustatymas > Kokybės valdymas > Sulaikymo zonos.</span><span class="sxs-lookup"><span data-stu-id="56043-178">Go to Inventory management > Setup > Quality management > Quarantine zones.</span></span>
2. <span data-ttu-id="56043-179">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="56043-179">Click New.</span></span>
3. <span data-ttu-id="56043-180">Lauke Sulaikymo zona įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="56043-180">In the Quarantine zone field, type a value.</span></span>
4. <span data-ttu-id="56043-181">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="56043-181">In the Description field, type a value.</span></span>
5. <span data-ttu-id="56043-182">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="56043-182">Close the page.</span></span>

