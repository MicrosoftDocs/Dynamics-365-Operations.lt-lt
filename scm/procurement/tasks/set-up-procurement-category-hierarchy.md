--- 
title: "Nustatyti įsigijimo kategorijų hierarchiją"
description: "Ši procedūra nurodo, kaip sukurti naujų mazgų įsigijimo kategorijų hierarchijoje ir kaip konfigūruoti įsigijimo kategoriją, kuri bus naudojama įsigijimo procese."
author: mkirknel
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b9897b1184e8159b20a45d4cedbba56baef31a3c
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="a9a61-103">Nustatyti įsigijimo kategorijų hierarchiją</span><span class="sxs-lookup"><span data-stu-id="a9a61-103">Set up a procurement category hierarchy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a9a61-104">Ši procedūra nurodo, kaip sukurti naujų mazgų įsigijimo kategorijų hierarchijoje ir kaip konfigūruoti įsigijimo kategoriją, kuri bus naudojama įsigijimo procese.</span><span class="sxs-lookup"><span data-stu-id="a9a61-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="a9a61-105">Šias užduotis paprastai atlieka pirkimo vadybininkas.</span><span class="sxs-lookup"><span data-stu-id="a9a61-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="a9a61-106">Šią procedūrą galėsite pradėti tik esant įsigijimo tipo kategorijų hierarchijai.</span><span class="sxs-lookup"><span data-stu-id="a9a61-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="a9a61-107">Jei naudojate demonstracinių duomenų įmonę, šią procedūrą galite vykdyti su USMF įmonėje.</span><span class="sxs-lookup"><span data-stu-id="a9a61-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="a9a61-108">Įtraukiti naują įsigijimo kategoriją</span><span class="sxs-lookup"><span data-stu-id="a9a61-108">Add a new procurement category</span></span>
1. <span data-ttu-id="a9a61-109">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > ..</span><span class="sxs-lookup"><span data-stu-id="a9a61-109">Go to Procurement and sourcing > ..</span></span> <span data-ttu-id="a9a61-110">> Įsigijimo kategorijos.</span><span class="sxs-lookup"><span data-stu-id="a9a61-110">> Procurement categories.</span></span>
2. <span data-ttu-id="a9a61-111">Spustelėkite „Redaguoti kategorijų hierarchiją“.</span><span class="sxs-lookup"><span data-stu-id="a9a61-111">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="a9a61-112">Kairiojoje puslapio pusėje rodoma dabartinė įsigijimo kategorijų hierarchija.</span><span class="sxs-lookup"><span data-stu-id="a9a61-112">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="a9a61-113">Ketinate pakeisti hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="a9a61-113">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="a9a61-114">Spustelėkite „Naujas kategorijos mazgas“.</span><span class="sxs-lookup"><span data-stu-id="a9a61-114">Click New category node.</span></span>
    * <span data-ttu-id="a9a61-115">Sistema pasirenka viršutinį mazgą pagal numatytuosius nustatymus.</span><span class="sxs-lookup"><span data-stu-id="a9a61-115">The system selects the top node by default.</span></span> <span data-ttu-id="a9a61-116">Jei vykdote šią procedūrą kaip užduoties vadovą, galite spustelėti mygtuką „Atrakinti“ ir pasirinkti kitą pirminį mazgą, į kurį galėsite įterpti savo naująjį mazgą.</span><span class="sxs-lookup"><span data-stu-id="a9a61-116">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="a9a61-117">Tai atlikę, vėl užrakinkite užduoties vadovą, o tada spustelėkite „Nauja kategorijos mazgas“.</span><span class="sxs-lookup"><span data-stu-id="a9a61-117">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="a9a61-118">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9a61-118">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a9a61-119">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9a61-119">In the Description field, type a value.</span></span>
6. <span data-ttu-id="a9a61-120">Lauke „Patogus pavadinimas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9a61-120">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="a9a61-121">Pasirinktinai galite įvesti patogų pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="a9a61-121">The friendly name is optional.</span></span> <span data-ttu-id="a9a61-122">Jis bus rodomas kategorijos peržvalgose kartu su kategorijos pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="a9a61-122">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="a9a61-123">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a9a61-123">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="a9a61-124">Įtraukti produktus į naują įsigijimo kategoriją</span><span class="sxs-lookup"><span data-stu-id="a9a61-124">Add products to your new procurement category</span></span>
1. <span data-ttu-id="a9a61-125">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > ..</span><span class="sxs-lookup"><span data-stu-id="a9a61-125">Go to Procurement and sourcing > ..</span></span> <span data-ttu-id="a9a61-126">> Įsigijimo kategorijos.</span><span class="sxs-lookup"><span data-stu-id="a9a61-126">> Procurement categories.</span></span>
    * <span data-ttu-id="a9a61-127">Pasirinkite mazgą, kurį ką tik pridėjote.</span><span class="sxs-lookup"><span data-stu-id="a9a61-127">Select the node you just added.</span></span> <span data-ttu-id="a9a61-128">Jei šią procedūrą vykdote kaip užduočių vadovą, jį gali reikėti atrakinti, kad galėtumėte pasirinkti mazgą,</span><span class="sxs-lookup"><span data-stu-id="a9a61-128">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="a9a61-129">Perjunkite skyriaus „Produktai“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="a9a61-129">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="a9a61-130">Spustelėkite „Įtraukti“, kad susietumėte produktus su įsigijimo kategorija.</span><span class="sxs-lookup"><span data-stu-id="a9a61-130">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="a9a61-131">Pasirinkite produktą, kurį norite įtraukti į įsigijimo kategoriją.</span><span class="sxs-lookup"><span data-stu-id="a9a61-131">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="a9a61-132">Spustelėkite rodyklę, kad pasirinktumėte produktą.</span><span class="sxs-lookup"><span data-stu-id="a9a61-132">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="a9a61-133">Pasirinkite kitą produktą, kurį norite įtraukti į įsigijimo kategoriją.</span><span class="sxs-lookup"><span data-stu-id="a9a61-133">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="a9a61-134">Spustelėkite rodyklę, kad pasirinktumėte produktą.</span><span class="sxs-lookup"><span data-stu-id="a9a61-134">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="a9a61-135">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a9a61-135">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="a9a61-136">Įtraukti patvirtintus ir pirmenybę turinčius tiekėjus</span><span class="sxs-lookup"><span data-stu-id="a9a61-136">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="a9a61-137">Perjunkite dalies Tiekėjai išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="a9a61-137">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="a9a61-138">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="a9a61-138">Click Add.</span></span>
    * <span data-ttu-id="a9a61-139">Galite įtraukti tiekėją į įsigijimo kategoriją ir nurodyti, ar tiekėjas toje kategorijoje yra turintis pirmenybę, ar jis joje tiesiog patvirtintas.</span><span class="sxs-lookup"><span data-stu-id="a9a61-139">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="a9a61-140">Kai panaikinate tiekėją iš kategorijos, istorinės operacijos su tiekėju kategorijoje nepanaikinamos.</span><span class="sxs-lookup"><span data-stu-id="a9a61-140">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="a9a61-141">Raskite tiekėją, kurį norite įtraukti į kategoriją.</span><span class="sxs-lookup"><span data-stu-id="a9a61-141">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="a9a61-142">Spustelėkite rodyklę, kad pasirinktumėte tiekėją.</span><span class="sxs-lookup"><span data-stu-id="a9a61-142">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="a9a61-143">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="a9a61-143">Click OK.</span></span>
6. <span data-ttu-id="a9a61-144">Pasirinkite tiekėjo eilutę, kurią norite modifikuoti.</span><span class="sxs-lookup"><span data-stu-id="a9a61-144">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="a9a61-145">Lauke „Tiekėjo būsena“ pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="a9a61-145">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="a9a61-146">Tiekėjo pasirinkimo nustatymas kategorijos strategijos taisyklėje reguliuoja, ar pirkimo paraiškose bus pateikiami pirmenybę turintys, patvirtinti ar visi tiekėjai.</span><span class="sxs-lookup"><span data-stu-id="a9a61-146">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="a9a61-147">Įtraukti papildomą informaciją į kategoriją</span><span class="sxs-lookup"><span data-stu-id="a9a61-147">Add additional information to the category</span></span>
1. <span data-ttu-id="a9a61-148">Perjunkite skyriaus „Tiekėjo vertinimo kriterijų grupės“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="a9a61-148">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="a9a61-149">Šiame skirtuke galima apibrėžti kriterijus, pagal kuriuos turi būti vertinami tiekėjai atitinkamoje įsigijimo kategorijoje.</span><span class="sxs-lookup"><span data-stu-id="a9a61-149">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="a9a61-150">Jei norite tai padaryti, spustelėkite „Pridėti“ ir pasirinkite tiekėjo vertinimo grupę, kurioje yra jūsų norimi kriterijai.</span><span class="sxs-lookup"><span data-stu-id="a9a61-150">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="a9a61-151">Perjunkite skyriaus „Klausimynai“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="a9a61-151">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="a9a61-152">Šiame skirtuke galima pridėti klausimynus, kurie bus rodomi paraiškoje tol, kol nustatytas veiklos tipas bus „Paraiška“.</span><span class="sxs-lookup"><span data-stu-id="a9a61-152">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="a9a61-153">Tada prašytojas turi užpildyti klausimyną, prieš pateikdamas paraišką dėl konkretaus produkto ar produktų toje įsigijimo kategorijoje.</span><span class="sxs-lookup"><span data-stu-id="a9a61-153">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="a9a61-154">Perjunkite skyriaus „Prekių PVM grupės“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="a9a61-154">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="a9a61-155">Lauke Prekių PVM grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a9a61-155">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a9a61-156">Pasirinkite PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="a9a61-156">Select a sales tax group.</span></span>
6. <span data-ttu-id="a9a61-157">Perjunkite skyriaus „Kategorijos puslapis“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="a9a61-157">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="a9a61-158">Kategorijos puslapius galima sukurti puslapyje „Kategorijų hierarchija“.</span><span class="sxs-lookup"><span data-stu-id="a9a61-158">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="a9a61-159">Juose yra informacija apie įsigijimo kategoriją, pvz., informacija apie kategorijos produktų tipus, kategorijos produktų vaizdai arba pranešimai, pvz., apie kategorijoje galimas nuolaidas.</span><span class="sxs-lookup"><span data-stu-id="a9a61-159">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="a9a61-160">Kategorijos puslapyje esanti informacija rodoma pirkimo paraiškose.</span><span class="sxs-lookup"><span data-stu-id="a9a61-160">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="a9a61-161">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a9a61-161">Close the page.</span></span>


