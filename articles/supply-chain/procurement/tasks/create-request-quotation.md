--- 
title: "Kurti pasiūlymo patvirtinimą"
description: "Šia procedūra parodoma, kaip kurti pasiūlymo patvirtinimą."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 331f516f3483acd79be4ef7b95b53adcfbef1ae2
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-request-for-quotation"></a><span data-ttu-id="60b9e-103">Kurti pasiūlymo patvirtinimą</span><span class="sxs-lookup"><span data-stu-id="60b9e-103">Create a request for quotation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60b9e-104">Šia procedūra parodoma, kaip kurti pasiūlymo patvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="60b9e-104">This procedure shows you how to create a request for quotation.</span></span> <span data-ttu-id="60b9e-105">Paprastai tai atlieka pirkimo agentas.</span><span class="sxs-lookup"><span data-stu-id="60b9e-105">This would typically be done by a purchasing agent.</span></span> <span data-ttu-id="60b9e-106">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="60b9e-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="60b9e-107">Prieš pradėdami turite nustatyti siūlymų tipus.</span><span class="sxs-lookup"><span data-stu-id="60b9e-107">You need to have set up solicitation types before you start.</span></span> <span data-ttu-id="60b9e-108">Atlikę šią užduotį ir sukūrę bei išsiuntę RFQ, galite įvesti atsakymus pagal tiekėją, juos palyginti ir pasirinkti sutartį.</span><span class="sxs-lookup"><span data-stu-id="60b9e-108">Once you’ve completed this task and you’ve created and sent an RFQ you can then enter the replies per vendor, compare them, and award the contract.</span></span>


## <a name="prepare-a-new-rfq"></a><span data-ttu-id="60b9e-109">Naujo RFQ parengimas</span><span class="sxs-lookup"><span data-stu-id="60b9e-109">Prepare a new RFQ</span></span>
1. <span data-ttu-id="60b9e-110">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pasiūlymų patvirtinimai > Visi pasiūlymų patvirtinimai.</span><span class="sxs-lookup"><span data-stu-id="60b9e-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="60b9e-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="60b9e-111">Click New.</span></span>
    * <span data-ttu-id="60b9e-112">Galimi tolesni pirkimo tipai. Pirkimo užsakymas (numatytasis tipas): dokumentas, kuriuo patvirtinamas siūlymas pirkti produktų arba priimamas siūlymas parduoti produktų už užmokestį.</span><span class="sxs-lookup"><span data-stu-id="60b9e-112">The following purchase types are available: Purchase order (this is the default): a document that confirms the offer to buy products, or the acceptance of an offer to sell products in exchange for payment.</span></span> <span data-ttu-id="60b9e-113">Pirkimo paraiška: šis tipas pasirenkamas automatiškai, jei RFQ kuriate tiesiai iš pirkimo paraiškos.</span><span class="sxs-lookup"><span data-stu-id="60b9e-113">Purchase requisition: this type is automatically selected if you create an RFQ directly from a purchase requisition.</span></span> <span data-ttu-id="60b9e-114">Jei šią parinktį pasirinksite rankiniu būdu, gausite klaidą.</span><span class="sxs-lookup"><span data-stu-id="60b9e-114">If you manually select this option, you’ll get an error.</span></span> <span data-ttu-id="60b9e-115">Pirkimo sutartis: susitarimas per tam tikrą laikotarpį nupirkti tam tikrą produktų kiekį arba tam tikros vertės produktų.</span><span class="sxs-lookup"><span data-stu-id="60b9e-115">Purchase agreement: an agreement to purchase a specific quantity or value of product over time.</span></span> <span data-ttu-id="60b9e-116">Jei pasirenkate šią parinktį, turite pasirinkti datų intervalą, taikomą pirkimo sutarčiai.</span><span class="sxs-lookup"><span data-stu-id="60b9e-116">If you select this option, you must select the date range that applies to the purchase agreement.</span></span>  
3. <span data-ttu-id="60b9e-117">Lauke Dokumento pavadinimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="60b9e-117">In the Document title field, type a value.</span></span>
4. <span data-ttu-id="60b9e-118">Lauke Siūlymo tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="60b9e-118">In the Solicitation type field, enter or select a value.</span></span>
    * <span data-ttu-id="60b9e-119">Jei vertinimo būdas susietas su siūlymo tipu, jis bus numatytasis jūsų kuriamo RFQ vertinimo būdas.</span><span class="sxs-lookup"><span data-stu-id="60b9e-119">If a scoring method is associated with the solicitation type, this will be the default scoring method for the RFQ that you’re creating.</span></span> <span data-ttu-id="60b9e-120">Vertinimo būdą vėliau galima pakeisti.</span><span class="sxs-lookup"><span data-stu-id="60b9e-120">It is possible to change the scoring method later.</span></span>  
    * <span data-ttu-id="60b9e-121">Lauke Pristatymo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="60b9e-121">In the Delivery date field, enter a date.</span></span>  
    * <span data-ttu-id="60b9e-122">Pasirinkite datą, iki kurios norite gauti prekes.</span><span class="sxs-lookup"><span data-stu-id="60b9e-122">Select the date by which you want to receive the items.</span></span>  
    * <span data-ttu-id="60b9e-123">Lauke Galiojimo data ir laikas įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="60b9e-123">In the Expiration date and time field, enter a date and time.</span></span>  
    * <span data-ttu-id="60b9e-124">Nurodykite datą ir laiką, iki kurių tiekėjai turi atsakyti į RFQ.</span><span class="sxs-lookup"><span data-stu-id="60b9e-124">Specify the date and time by which vendors must respond to the RFQ.</span></span>  
5. <span data-ttu-id="60b9e-125">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="60b9e-125">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="60b9e-126">Numatytasis pristatymo adresas bus sandėlio adresas.</span><span class="sxs-lookup"><span data-stu-id="60b9e-126">The delivery address will default to the warehouse address.</span></span>  
6. <span data-ttu-id="60b9e-127">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="60b9e-127">Click OK.</span></span>

## <a name="add-lines"></a><span data-ttu-id="60b9e-128">Pridėti eilutes</span><span class="sxs-lookup"><span data-stu-id="60b9e-128">Add lines</span></span>
    * <span data-ttu-id="60b9e-129">Nurodę pagrindinę informaciją apie RFQ, galite nurodyti prekes arba paslaugas, kurių kainos pasiūlymus turi teikti tiekėjai.</span><span class="sxs-lookup"><span data-stu-id="60b9e-129">After you’ve specified the basic information about your RFQ, you specify the goods or services that you want vendors to bid on.</span></span> <span data-ttu-id="60b9e-130">Numatytasis eilutės tipas yra Prekė.</span><span class="sxs-lookup"><span data-stu-id="60b9e-130">Item is the default line type.</span></span>   
1. <span data-ttu-id="60b9e-131">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="60b9e-131">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="60b9e-132">Jei naudojate USMF, galite pasirinkti T0020.</span><span class="sxs-lookup"><span data-stu-id="60b9e-132">If you're using USMF, you can select T0020.</span></span>  
2. <span data-ttu-id="60b9e-133">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="60b9e-133">In the Quantity field, enter a number.</span></span>
3. <span data-ttu-id="60b9e-134">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="60b9e-134">Click Add line.</span></span>
4. <span data-ttu-id="60b9e-135">Lauke Eilutės tipas pasirinkite Kategorija.</span><span class="sxs-lookup"><span data-stu-id="60b9e-135">In the Line type field, select 'Category'.</span></span>
    * <span data-ttu-id="60b9e-136">Naudodami tipą Kategorijos eilutė, galite kurti ne atsargų prekių ar paslaugų RFQ.</span><span class="sxs-lookup"><span data-stu-id="60b9e-136">You can use the Category line type to create RFQs for non-inventory goods or services.</span></span> <span data-ttu-id="60b9e-137">Tada iš įsigijimo kategorijų hierarchijos turite pasirinkti prekių ar paslaugų tipą.</span><span class="sxs-lookup"><span data-stu-id="60b9e-137">You then need to select the type of goods or services from a hierarchy of procurement categories.</span></span>  
5. <span data-ttu-id="60b9e-138">Lauke Įsigijimo kategorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="60b9e-138">In the Procurement category field, enter or select a value.</span></span>
6. <span data-ttu-id="60b9e-139">Lauke „Produkto pavadinimas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="60b9e-139">In the Product name field, type a value.</span></span>
7. <span data-ttu-id="60b9e-140">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="60b9e-140">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="60b9e-141">Lauke Vienetas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="60b9e-141">In the Unit field, enter or select a value.</span></span>

## <a name="add-vendors"></a><span data-ttu-id="60b9e-142">Įtraukti tiekėjų</span><span class="sxs-lookup"><span data-stu-id="60b9e-142">Add vendors</span></span>
1. <span data-ttu-id="60b9e-143">Spustelėdami antraštę, rodinį Eilutės pakeisite į rodinį Antraštė.</span><span class="sxs-lookup"><span data-stu-id="60b9e-143">Click Header to change from the Lines view to the Header view.</span></span> 
2. <span data-ttu-id="60b9e-144">Išplėskite sekciją Tiekėjas.</span><span class="sxs-lookup"><span data-stu-id="60b9e-144">Expand the Vendor section.</span></span>
3. <span data-ttu-id="60b9e-145">Spustelėkite Automatiškai įtraukti tiekėjų.</span><span class="sxs-lookup"><span data-stu-id="60b9e-145">Click Auto-add vendors.</span></span>
    * <span data-ttu-id="60b9e-146">Tiekėjų į RFQ galite įtraukti automatiškai pagal pageidaujamų prekių įsigijimo kategoriją.</span><span class="sxs-lookup"><span data-stu-id="60b9e-146">You can add vendors to the RFQ automatically, based on the procurement category of the items requested.</span></span> <span data-ttu-id="60b9e-147">Jei nėra patvirtintų eilutėse įtrauktų kategorijų tiekėjų, jų įtraukti galite rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="60b9e-147">If there are no vendors approved for the categories included in the lines you can add vendors manually.</span></span>  
4. <span data-ttu-id="60b9e-148">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="60b9e-148">Click Add.</span></span>
5. <span data-ttu-id="60b9e-149">Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="60b9e-149">In the Vendor account field, enter or select a value.</span></span>
6. <span data-ttu-id="60b9e-150">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="60b9e-150">Click Add.</span></span>
7. <span data-ttu-id="60b9e-151">Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="60b9e-151">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="60b9e-152">Kai pasirenkate tiekėją, būsena yra Sukurtas.</span><span class="sxs-lookup"><span data-stu-id="60b9e-152">Once you’ve selected a vendor, the status is Created.</span></span> <span data-ttu-id="60b9e-153">Tai reiškia, kad tiekėjo informacija buvo įrašyta į RFQ, tačiau RFQ nebuvo išsiųstas tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="60b9e-153">This means that the vendor information has been saved in the RFQ, but you have not sent the RFQ to the vendor.</span></span> <span data-ttu-id="60b9e-154">Galite pridėti tiekėją prie RFQ, nepriklausomai nuo jo statuso.</span><span class="sxs-lookup"><span data-stu-id="60b9e-154">You can add a vendor to an RFQ regardless of the vendor status.</span></span>  

## <a name="send-the-rfq-to-vendors"></a><span data-ttu-id="60b9e-155">Siųsti RFQ tiekėjams</span><span class="sxs-lookup"><span data-stu-id="60b9e-155">Send the RFQ to vendors</span></span>
1. <span data-ttu-id="60b9e-156">Spustelėkite Siųsti.</span><span class="sxs-lookup"><span data-stu-id="60b9e-156">Click Send.</span></span>
    * <span data-ttu-id="60b9e-157">Puslapyje Pasiūlymo patvirtinimo siuntimas patikrinkite, ar sąraše esantys tiekėjai yra tie, kurie turi gauti RFQ.</span><span class="sxs-lookup"><span data-stu-id="60b9e-157">In the Sending request for quotation page, check that the vendors in the list are the ones that you want to receive the RFQ.</span></span>  
2. <span data-ttu-id="60b9e-158">Spustelėkite Spausdinti.</span><span class="sxs-lookup"><span data-stu-id="60b9e-158">Click Print.</span></span>
    * <span data-ttu-id="60b9e-159">Naudodami šį dialogo langą galite spausdinti RFQ.</span><span class="sxs-lookup"><span data-stu-id="60b9e-159">This dialog allows you to print the RFQ.</span></span> <span data-ttu-id="60b9e-160">Jei pasirinksite spausdinti atsakymų lapą, jo turinys apibrėžtas įsigijimo ir šaltinio pasirinkimo parametruose.</span><span class="sxs-lookup"><span data-stu-id="60b9e-160">If you choose to print a reply sheet, the contents of this are defined in Procurement and Sourcing parameters.</span></span> <span data-ttu-id="60b9e-161">Norėdami pasirinkti, kaip spausdinti atsakymų lapus, atidarę dialogo langą Spausdinti, spustelėkite Papildomos spausdinimo parinktys.</span><span class="sxs-lookup"><span data-stu-id="60b9e-161">To choose how to print reply sheets, once you’ve opened the Print dialog, click Advanced printing options.</span></span> <span data-ttu-id="60b9e-162">Kiekvienam tiekėjui bus išspausdintas vienas RFQ su eilutėmis, kurių būsena – Sukurta arba Išsiųsta.</span><span class="sxs-lookup"><span data-stu-id="60b9e-162">One RFQ will be printed for each vendor containing the lines that have the status of Created or Sent.</span></span> <span data-ttu-id="60b9e-163">Atšauktos eilutės ir eilutės su registruotas atsakymais nebus išspausdintos.</span><span class="sxs-lookup"><span data-stu-id="60b9e-163">Canceled lines and lines with registered replies will not be printed.</span></span>   
3. <span data-ttu-id="60b9e-164">Spustelėkite Atšaukti.</span><span class="sxs-lookup"><span data-stu-id="60b9e-164">Click Cancel.</span></span>
4. <span data-ttu-id="60b9e-165">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="60b9e-165">Click OK.</span></span>
5. <span data-ttu-id="60b9e-166">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="60b9e-166">Close the page.</span></span>
6. <span data-ttu-id="60b9e-167">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="60b9e-167">Close the page.</span></span>

## <a name="view-the-rfq-journal"></a><span data-ttu-id="60b9e-168">RFQ žurnalo peržiūra</span><span class="sxs-lookup"><span data-stu-id="60b9e-168">View the RFQ journal</span></span>
1. <span data-ttu-id="60b9e-169">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pasiūlymų patvirtinimai > Pasiūlymo patvirtinimų sekimas > Pasiūlymo patvirtinimų žurnalai.</span><span class="sxs-lookup"><span data-stu-id="60b9e-169">Go to Procurement and sourcing > Requests for quotations > Request for quotations follow-up > Request for quotation journals.</span></span>
2. <span data-ttu-id="60b9e-170">Spustelėkite Peržiūrėti / spausdinti.</span><span class="sxs-lookup"><span data-stu-id="60b9e-170">Click Preview/Print.</span></span>
3. <span data-ttu-id="60b9e-171">Spustelėkite Originalo peržiūra.</span><span class="sxs-lookup"><span data-stu-id="60b9e-171">Click Original preview.</span></span>
4. <span data-ttu-id="60b9e-172">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="60b9e-172">Close the page.</span></span>
5. <span data-ttu-id="60b9e-173">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="60b9e-173">Close the page.</span></span>


