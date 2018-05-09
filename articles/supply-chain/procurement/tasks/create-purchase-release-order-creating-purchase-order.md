--- 
title: "Kurti pirkimo leidimą išduoti kuriant pirkimo užsakymą"
description: "Ši procedūra nurodo, kaip naudoti pirkimo sutartį, kai kuriate pirkimo užsakymą."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2a5fde13fac7f0523c098f750d897ca5da06473b
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a><span data-ttu-id="4bc06-103">Kurti pirkimo leidimą išduoti kuriant pirkimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="4bc06-103">Create a purchase release order when creating the purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4bc06-104">Ši procedūra nurodo, kaip naudoti pirkimo sutartį, kai kuriate pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="4bc06-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="4bc06-105">Pirkimo sutartis turi būti taikoma, kai kuriate pirkimo užsakymą, nes yra bendrų sąlygų, kurios turi būti nukopijuotos į pirkimo užsakymo antraštę.</span><span class="sxs-lookup"><span data-stu-id="4bc06-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="4bc06-106">Šią užduotį paprastai atlieka pirkimo agentas.</span><span class="sxs-lookup"><span data-stu-id="4bc06-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="4bc06-107">Būtina šio vadovo sąlyga – privalote turėti galiojančią pirkimo sutartį su tiėkėjo įsipareigojimu dėl produkto kiekio ir prekių.</span><span class="sxs-lookup"><span data-stu-id="4bc06-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="4bc06-108">Saugojimo dimensijų grupė nustato, kurios saugojimo dimensijos bus naudojamos produktų operacijoms.</span><span class="sxs-lookup"><span data-stu-id="4bc06-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="4bc06-109">Šį vadovą galite vykdyti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="4bc06-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="4bc06-110">Jei naudojate USMF, galite pirmiausia paleisti vadovą „Kurti pirkimo sutartį“, kad įvykdytumėte būtinas išankstines šio vadovo sąlygas.</span><span class="sxs-lookup"><span data-stu-id="4bc06-110">If you’re using USMF, you can run the “Create a purchase agreement” guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="4bc06-111">Pirkimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="4bc06-111">Create a purchase order</span></span>
1. <span data-ttu-id="4bc06-112">Atidarykite pirkimo užsakymo rengimo darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="4bc06-112">Open the purchase order preparation workspace.</span></span>
2. <span data-ttu-id="4bc06-113">Spustelėkite „Naujas pirkimo užsakymas“.</span><span class="sxs-lookup"><span data-stu-id="4bc06-113">Click New purchase order.</span></span>
3. <span data-ttu-id="4bc06-114">Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="4bc06-114">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4bc06-115">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="4bc06-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="4bc06-116">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="4bc06-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="4bc06-117">Perjunkite dalies Bendra išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="4bc06-117">Toggle the expansion of the General section.</span></span>
7. <span data-ttu-id="4bc06-118">Lauke „Pirkimo sutartis“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="4bc06-118">In the Purchase agreement field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4bc06-119">Čia išvardytos visos esamos sutartys su tiekėjais.</span><span class="sxs-lookup"><span data-stu-id="4bc06-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="4bc06-120">Raskite galiojančią sutartį, kurią norite naudoti.</span><span class="sxs-lookup"><span data-stu-id="4bc06-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="4bc06-121">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="4bc06-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="4bc06-122">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="4bc06-122">Click Yes.</span></span>
10. <span data-ttu-id="4bc06-123">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="4bc06-123">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="4bc06-124">Įtraukti eilutę</span><span class="sxs-lookup"><span data-stu-id="4bc06-124">Add a line</span></span>
1. <span data-ttu-id="4bc06-125">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4bc06-125">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="4bc06-126">Jei įsipareigojimas nurodo konkrečias atsargų arba vietos dimensijas, turite įvesti tas pačias reikšmes ir pirkimo užsakymo eilutėje, kad galėtumėte naudotis sutartimi.</span><span class="sxs-lookup"><span data-stu-id="4bc06-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="4bc06-127">Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="4bc06-127">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4bc06-128">Svetainėje jau gali būti įvesta numatytoji reikšmė iš užsakymo arba iš tiekėjo.</span><span class="sxs-lookup"><span data-stu-id="4bc06-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="4bc06-129">Tokiu atveju praleiskite šį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="4bc06-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="4bc06-130">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="4bc06-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="4bc06-131">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="4bc06-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4bc06-132">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="4bc06-132">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="4bc06-133">Patikrinkite, ar kaina nukopijuota iš įsipareigojimo.</span><span class="sxs-lookup"><span data-stu-id="4bc06-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="4bc06-134">Ieškoti įsipareigojimo</span><span class="sxs-lookup"><span data-stu-id="4bc06-134">Look up the commitment</span></span>
1. <span data-ttu-id="4bc06-135">Spustelėkite eilutę „Atnaujinti“.</span><span class="sxs-lookup"><span data-stu-id="4bc06-135">Click Update line.</span></span>
2. <span data-ttu-id="4bc06-136">Spustelėkite „Pridėta“.</span><span class="sxs-lookup"><span data-stu-id="4bc06-136">Click Attached.</span></span>
    * <span data-ttu-id="4bc06-137">Čia galite gauti informaciją apie pirkimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="4bc06-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="4bc06-138">Pvz., galite matyti kainą ir ar kaina bei nuolaida yra fiksuotos – tai reiškia, kad pakeitus kainos ar nuolaidos reikšmę pirkimo užsakyme į kitą nei nurodyta įsipareigojime, sistema pašalins saitą, todėl pirkimo užsakymo eilutė neatitiks įsipareigojimo.</span><span class="sxs-lookup"><span data-stu-id="4bc06-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="4bc06-139">Taip pat galite matyti, ar pasirinkta parinktis „Maksimaliai vykdoma“ – tai reiškia, kad negalima viršyti įsipareigojime nurodyto kiekio sudedant visus pirkimus, kurie atitinka įsipareigojimą.</span><span class="sxs-lookup"><span data-stu-id="4bc06-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="4bc06-140">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4bc06-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="4bc06-141">Ieškoti pirkimo sutarties</span><span class="sxs-lookup"><span data-stu-id="4bc06-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="4bc06-142">Veiksmų srityje spustelėkite Bendra.</span><span class="sxs-lookup"><span data-stu-id="4bc06-142">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="4bc06-143">Spustelėkite „Pirkimo sutartis“.</span><span class="sxs-lookup"><span data-stu-id="4bc06-143">Click Purchase agreement.</span></span>
3. <span data-ttu-id="4bc06-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4bc06-144">Close the page.</span></span>
4. <span data-ttu-id="4bc06-145">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4bc06-145">Close the page.</span></span>


