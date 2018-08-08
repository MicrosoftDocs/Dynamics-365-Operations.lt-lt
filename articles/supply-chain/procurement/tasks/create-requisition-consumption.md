--- 
title: "Kurti vartojimo paraišką"
description: "Ši procedūra žingsnis po žingsnio supažindins su paraiškos kūrimo procesu."
author: mkirknel
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e81ca3966cf7dae88468ccf107b52b8c3d7b323d
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-requisition-for-consumption"></a><span data-ttu-id="625dc-103">Kurti vartojimo paraišką</span><span class="sxs-lookup"><span data-stu-id="625dc-103">Create a requisition for consumption</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="625dc-104">Ši procedūra žingsnis po žingsnio supažindins su paraiškos kūrimo procesu.</span><span class="sxs-lookup"><span data-stu-id="625dc-104">This procedure walks you through the process of creating a requisition.</span></span> <span data-ttu-id="625dc-105">Ji parodo skirtingus produktų paiekos įsigijimo kataloge būdus ir kaip įtraukti produktą, kurio nėra kataloge.</span><span class="sxs-lookup"><span data-stu-id="625dc-105">It shows you different ways to search for products in your procurement catalog and how to add a product that isn’t in your catalog.</span></span> <span data-ttu-id="625dc-106">Prieš pradėdami šią procedūrą, pirkimo strategiją numatytuoju paraiškos tipu turite nustatyti suvartojimą.</span><span class="sxs-lookup"><span data-stu-id="625dc-106">Before you start this procedure, you must have a purchasing policy set up with Consumption as the default type of requisition.</span></span> <span data-ttu-id="625dc-107">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="625dc-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="625dc-108">Procedūrą galima atlikti tik iš vartotojo profilio, kuris nustatytas kaip darbuotojo.</span><span class="sxs-lookup"><span data-stu-id="625dc-108">The procedure can only be carried out by a user profile that is set up as worker.</span></span>  <span data-ttu-id="625dc-109">Šiią užduotį paprastai atlieka darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="625dc-109">This task would normally be carried out by an employee.</span></span> <span data-ttu-id="625dc-110">Užduotis galėsite atlikti per darbuotojo saugos vaidmenį arba, jei naudojate USMF, galite prisijungti kaip Alicia.</span><span class="sxs-lookup"><span data-stu-id="625dc-110">The Employee employ security role will allow you to carry out the tasks, or if you’re using USMF, you can log in as Alicia.</span></span>


## <a name="create-a-new-requisition"></a><span data-ttu-id="625dc-111">Kurti naują paraišką</span><span class="sxs-lookup"><span data-stu-id="625dc-111">Create a new requisition</span></span>
1. <span data-ttu-id="625dc-112">Pasirinkite Pirkimai ir tiekėjų parinkimas > Pirkimo paraiškos > Mano parengtos pirkimo paraiškos.</span><span class="sxs-lookup"><span data-stu-id="625dc-112">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="625dc-113">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="625dc-113">Click New.</span></span>
3. <span data-ttu-id="625dc-114">Lauke „Pavadiniams“ suteikite paraiškai pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="625dc-114">In the Name field, give the requisition a name.</span></span>
4. <span data-ttu-id="625dc-115">Lauke „Pageidaujama data“ įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="625dc-115">In the Requested date field, enter a date.</span></span>
    * <span data-ttu-id="625dc-116">Pagal numatytuosius nustatymus, pageidaujama data ir apskaitos data nukopijuojamos į pirkimo paraiškos eilutes.</span><span class="sxs-lookup"><span data-stu-id="625dc-116">By default, the requested date and accounting date are copied to the purchase requisition lines.</span></span> <span data-ttu-id="625dc-117">Jas galima keisti eilučių lygmeniu.</span><span class="sxs-lookup"><span data-stu-id="625dc-117">They can be changed at the line level.</span></span> <span data-ttu-id="625dc-118">Pareikalauta data – tai pageidaujama pristatymo data.</span><span class="sxs-lookup"><span data-stu-id="625dc-118">The requested date is the requested delivery date.</span></span>  
5. <span data-ttu-id="625dc-119">Lauke „Apskaitos data“ įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="625dc-119">In the Accounting date field, enter a date.</span></span>
    * <span data-ttu-id="625dc-120">Apskaitos data naudojama įrašant apskaitos įrašą didžiojoje knygoje bei tikrinant, ar yra biudžeto lėšų.</span><span class="sxs-lookup"><span data-stu-id="625dc-120">The accounting date is used to record the accounting entry in the general ledger, and to validate whether budget funds are available.</span></span>  
6. <span data-ttu-id="625dc-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="625dc-121">Click OK.</span></span>
7. <span data-ttu-id="625dc-122">Lauke „Priežastis“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="625dc-122">In the Reason field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="625dc-123">Pagal nustatytuosius parametrus, jūsų pasirinkta verslo pagrindimo priežastis rodoma pirkimo paraiškos eilutėse, bet galite ją pakeisti eilutės lygmeniu.</span><span class="sxs-lookup"><span data-stu-id="625dc-123">By default, the business justification reason that you select appears for the purchase requisition lines, but you can change it at the line level.</span></span>    
8. <span data-ttu-id="625dc-124">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="625dc-124">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="625dc-125">Pasirinkti priežastį</span><span class="sxs-lookup"><span data-stu-id="625dc-125">Select the reason</span></span>
10. <span data-ttu-id="625dc-126">Informacija lauke įveskite išsamesnį paraiškos pagrindimą</span><span class="sxs-lookup"><span data-stu-id="625dc-126">In the details field enter a more descriptive justification for the requisition</span></span>

## <a name="add-a-line-to-the-requisition"></a><span data-ttu-id="625dc-127">Įtraukti eilutę į paraišką</span><span class="sxs-lookup"><span data-stu-id="625dc-127">Add a line to the requisition</span></span>
1. <span data-ttu-id="625dc-128">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="625dc-128">Click Add line.</span></span>
    * <span data-ttu-id="625dc-129">Pridėti eilutes į pirkimo paraišką galima dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="625dc-129">There are two ways of adding lines to the purchase requisition.</span></span> <span data-ttu-id="625dc-130">Jei jau žinote produkto numerį arba jau žinote, kad jums reikalingo produkto kataloge nėra, galite pridėti eilutę tiesiogiai, paspaudę „Pridėti eilutę“.</span><span class="sxs-lookup"><span data-stu-id="625dc-130">If you already know the product number or you already  know that you are requesting a product that is not in the product catalog, then you can add the line directly with "Add line".</span></span> <span data-ttu-id="625dc-131">Kitas būdas yra paspausti „Pridėti produktus“, kur galite naudoti paiešką ir filtravimą, kad rastumėte prekes produktų kataloge.</span><span class="sxs-lookup"><span data-stu-id="625dc-131">The other way is to use "Add products" where you can use searching and filtering to find items in the product catalog.</span></span>    
2. <span data-ttu-id="625dc-132">Spustelėkite eilutę, kurią ką tik sukūrėte.</span><span class="sxs-lookup"><span data-stu-id="625dc-132">Click on the row you just created.</span></span>
    * <span data-ttu-id="625dc-133">Prašytojas yra darbuotojas, kuris paprašė leisti rengti paraišką.</span><span class="sxs-lookup"><span data-stu-id="625dc-133">The requester is the worker that has requested the requisition.</span></span>   
    * <span data-ttu-id="625dc-134">Pagal numatytuosius nustatymus, paraišką rengiantis asmuo yra to prašęs darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="625dc-134">By default the person preparing the requisition is the worker who has requested it.</span></span> <span data-ttu-id="625dc-135">Norėdami parengti paraiškos eilutę kito darbuotojo vardu turėsite gauti leidimą.</span><span class="sxs-lookup"><span data-stu-id="625dc-135">You have to be given permission to prepare a requisition line on behalf of another worker.</span></span> <span data-ttu-id="625dc-136">Jei tokius leidimus turite, tada šioje paieškoje bus rodomi kiti darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="625dc-136">If you have such permissions then the other workers will show up in this lookup.</span></span>  
3. <span data-ttu-id="625dc-137">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="625dc-137">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="625dc-138">Prekes, iš kurių galite rinktis, riboja kategorijos prieigos strategija ir perkančio juridinio subjekto įsigijimo katalogas.</span><span class="sxs-lookup"><span data-stu-id="625dc-138">The items that are available for you to choose are limited by the category access policy and the procurement catalog for the buying legal entity.</span></span>   
4. <span data-ttu-id="625dc-139">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="625dc-139">In the Quantity field, enter a number.</span></span>

## <a name="add-more-products-to-the-requisition"></a><span data-ttu-id="625dc-140">Įtraukti daugiau produktų į paraišką</span><span class="sxs-lookup"><span data-stu-id="625dc-140">Add more products to the requisition</span></span>
1. <span data-ttu-id="625dc-141">Spustelėkite „Įtraukti produktus“.</span><span class="sxs-lookup"><span data-stu-id="625dc-141">Click Add products.</span></span>
    * <span data-ttu-id="625dc-142">Ši parinktis leidžia ieškoti produktų kataloge.</span><span class="sxs-lookup"><span data-stu-id="625dc-142">This is the option where you can search for products in the product catalog.</span></span>    
2. <span data-ttu-id="625dc-143">Lauke „Rasti įsigijimo kategorijos mazgą“ įveskite pirmąją jūsų ieškomos kategorijos pavadinimo dalį, tada paspauskite „Įvesti“.</span><span class="sxs-lookup"><span data-stu-id="625dc-143">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="625dc-144">Pvz., įveskite „kompiut“.</span><span class="sxs-lookup"><span data-stu-id="625dc-144">For example, type comput.</span></span>  
3. <span data-ttu-id="625dc-145">Naudokite InvokeDefaultButton sparčiuosius klavišus.</span><span class="sxs-lookup"><span data-stu-id="625dc-145">Use the InvokeDefaultButton shortcut.</span></span>
4. <span data-ttu-id="625dc-146">Naudokite filtrą pasirinktos kategorijos produktų sąrašui filtruoti.</span><span class="sxs-lookup"><span data-stu-id="625dc-146">Use the Filter to filter the list of products in the selected category.</span></span>
5. <span data-ttu-id="625dc-147">Pasirinkite produkto kortelę, kurią norite įtraukti į paraišką.</span><span class="sxs-lookup"><span data-stu-id="625dc-147">Select the product card that you want to add to the requisition.</span></span>
6. <span data-ttu-id="625dc-148">Spustelėkite „Įtraukti į eilutes“.</span><span class="sxs-lookup"><span data-stu-id="625dc-148">Click Add to lines.</span></span>
7. <span data-ttu-id="625dc-149">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="625dc-149">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="625dc-150">Lauke „Rasti įsigijimo kategorijos mazgą“ įveskite pirmąją jūsų ieškomos kategorijos pavadinimo dalį, tada paspauskite „Įvesti“.</span><span class="sxs-lookup"><span data-stu-id="625dc-150">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="625dc-151">Pvz., įveskite „žym“ (žymekliai).</span><span class="sxs-lookup"><span data-stu-id="625dc-151">For example, type High (highlighters).</span></span>  
9. <span data-ttu-id="625dc-152">Naudokite InvokeDefaultButton sparčiuosius klavišus.</span><span class="sxs-lookup"><span data-stu-id="625dc-152">Use the InvokeDefaultButton shortcut.</span></span>
10. <span data-ttu-id="625dc-153">Spustelėkite „Įtraukti į eilutes produktą ne iš sąrašo“, kad pridėtumėte produktą, kurio nėra įsigijimo kataloge.</span><span class="sxs-lookup"><span data-stu-id="625dc-153">Click Add unlisted product to lines to add a product that’s not listed in the procurement catalog.</span></span>
11. <span data-ttu-id="625dc-154">Lauke Produkto pavadinimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="625dc-154">In the Product name field, type a value.</span></span>
12. <span data-ttu-id="625dc-155">Lauke „Vienetas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="625dc-155">In the Unit field, type a value.</span></span>
13. <span data-ttu-id="625dc-156">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="625dc-156">Click OK.</span></span>
14. <span data-ttu-id="625dc-157">Lauke „Prekės aprašas“ pridėkite produkto aprašą.</span><span class="sxs-lookup"><span data-stu-id="625dc-157">In the Item description field, add a description of the product.</span></span>
15. <span data-ttu-id="625dc-158">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="625dc-158">In the Quantity field, enter a number.</span></span>
16. <span data-ttu-id="625dc-159">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="625dc-159">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="625dc-160">Jei žinote konkretaus tiekėjo kainą (kurią pasirenkate tiekėjo sąskaitos lauke), tada galite įvesti šią kainą</span><span class="sxs-lookup"><span data-stu-id="625dc-160">If you know the price for a particular vendor (that you select in the vendor account field) then that price can be entered</span></span>   
17. <span data-ttu-id="625dc-161">Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="625dc-161">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="625dc-162">Kokie tiekėjai bus šiame lauke priklauso nuo pirkimo strategijų ir tiekėjo būsenos esamoje įsigijimo kategorijoje.</span><span class="sxs-lookup"><span data-stu-id="625dc-162">The vendors that are available in this field depend on the purchasing policies and the status that the vendor has for the current procurement category.</span></span> <span data-ttu-id="625dc-163">Tiekėją galite pasirinkti ne tik čia – taip pat galite spustelėti mygtuką „Siūlyti tiekėją“.</span><span class="sxs-lookup"><span data-stu-id="625dc-163">As an alternative to selecting a vendor here, you can click the Suggest vendor button.</span></span>    
18. <span data-ttu-id="625dc-164">Sąrašo pasirinkite tiekėją, kurį norite naudoti.</span><span class="sxs-lookup"><span data-stu-id="625dc-164">In the list, select the vendor you want to use.</span></span>
19. <span data-ttu-id="625dc-165">Lauke „Išorinis prekės numeris“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="625dc-165">In the External item number field, type a value.</span></span>
    * <span data-ttu-id="625dc-166">Tai yra produkto nuorodos numeris, kurį žino tiekėjas.</span><span class="sxs-lookup"><span data-stu-id="625dc-166">This is a reference number for the product that is known by the vendor.</span></span> <span data-ttu-id="625dc-167">Pvz., tai gali būti prekės numeris tiekėjo produktų kataloge.</span><span class="sxs-lookup"><span data-stu-id="625dc-167">For example, this could be the item number of the product in the vendor's own catalog.</span></span>  
20. <span data-ttu-id="625dc-168">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="625dc-168">Click OK.</span></span>

## <a name="distribute-amounts"></a><span data-ttu-id="625dc-169">Paskirstyti sumas</span><span class="sxs-lookup"><span data-stu-id="625dc-169">Distribute amounts</span></span>
1. <span data-ttu-id="625dc-170">Spustelėkite Finansai.</span><span class="sxs-lookup"><span data-stu-id="625dc-170">Click Financials.</span></span>
2. <span data-ttu-id="625dc-171">Spustelėkite „Paskirstyti sumas“.</span><span class="sxs-lookup"><span data-stu-id="625dc-171">Click Distribute amounts.</span></span>
    * <span data-ttu-id="625dc-172">Šis procesas nurodo, kaip paskirstyti pirmos eilutės išlaidas 2 sąskaitoms.</span><span class="sxs-lookup"><span data-stu-id="625dc-172">This process shows you how to distribute the cost for the first line between 2 accounts.</span></span> <span data-ttu-id="625dc-173">Tą taip pat galima atlikti vėliau, kai paraiška bus peržiūrima.</span><span class="sxs-lookup"><span data-stu-id="625dc-173">This can also be done later when the requisition is in review.</span></span>  
3. <span data-ttu-id="625dc-174">Spustelėkite „Skaidyti“, kad sukurtumėte naują paskirstymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="625dc-174">Click Split to create a new distribution line.</span></span>
4. <span data-ttu-id="625dc-175">Lauke „DK sąskaita“ pasirinkite pirmą išlaidų centrą, kuris turėtų prisiimti dalį išlaidų.</span><span class="sxs-lookup"><span data-stu-id="625dc-175">In the Ledger account field select the first cost center that should take part of the cost.</span></span>
5. <span data-ttu-id="625dc-176">Pasirinkite kitą paskirstymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="625dc-176">Select the other distribution line.</span></span>
6. <span data-ttu-id="625dc-177">Lauke „DK sąskaita“ nurodykite kitą išlaidų centrą.</span><span class="sxs-lookup"><span data-stu-id="625dc-177">In the Ledger account field specify the other cost center.</span></span>
7. <span data-ttu-id="625dc-178">Spustelėkite „Paskirstyti tolygiai“.</span><span class="sxs-lookup"><span data-stu-id="625dc-178">Click Distribute equally.</span></span>
8. <span data-ttu-id="625dc-179">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="625dc-179">Close the page.</span></span>

## <a name="view-line-details"></a><span data-ttu-id="625dc-180">Peržiūrėti eilutės informaciją</span><span class="sxs-lookup"><span data-stu-id="625dc-180">View line details</span></span>
1. <span data-ttu-id="625dc-181">Perjunkite dalies Išsami eilučių informacija išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="625dc-181">Toggle the expansion of the Line details section.</span></span>

## <a name="submit-the-requisition"></a><span data-ttu-id="625dc-182">Pateikti paraišką</span><span class="sxs-lookup"><span data-stu-id="625dc-182">Submit the requisition</span></span>
1. <span data-ttu-id="625dc-183">Spustelėkite „Darbo eiga“, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="625dc-183">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="625dc-184">Spustelėkite Pateikti.</span><span class="sxs-lookup"><span data-stu-id="625dc-184">Click Submit.</span></span>
3. <span data-ttu-id="625dc-185">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="625dc-185">Close the page.</span></span>
4. <span data-ttu-id="625dc-186">Lauke „Komentaras“ įveskite pastabą paraiškos tvirtintojui.</span><span class="sxs-lookup"><span data-stu-id="625dc-186">In the Comment field, type a note for the approver of the requisition.</span></span>
5. <span data-ttu-id="625dc-187">Spustelėkite Pateikti.</span><span class="sxs-lookup"><span data-stu-id="625dc-187">Click Submit.</span></span>
6. <span data-ttu-id="625dc-188">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="625dc-188">Close the page.</span></span>
7. <span data-ttu-id="625dc-189">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="625dc-189">Refresh the page.</span></span>


