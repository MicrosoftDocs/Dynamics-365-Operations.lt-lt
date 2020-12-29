---
title: Sukurti pirkimo leidimo užsakymą iš pirkimo sutarties
description: Ši procedūra nurodo, kaip naudoti pirkimo sutartį, kai kuriate pirkimo užsakymą.
author: mkirknel
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee0c40dfc3c820343c7054238cc2da47e8203d59
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433534"
---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a><span data-ttu-id="11972-103">Sukurti pirkimo leidimo užsakymą iš pirkimo sutarties</span><span class="sxs-lookup"><span data-stu-id="11972-103">Create a purchase release order from a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11972-104">Ši procedūra nurodo, kaip naudoti pirkimo sutartį, kai kuriate pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="11972-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="11972-105">Pirkimo sutartis turi būti taikoma, kai kuriate pirkimo užsakymą, nes yra bendrų sąlygų, kurios turi būti nukopijuotos į pirkimo užsakymo antraštę.</span><span class="sxs-lookup"><span data-stu-id="11972-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="11972-106">Šią užduotį paprastai atlieka pirkimo agentas.</span><span class="sxs-lookup"><span data-stu-id="11972-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="11972-107">Būtina šio vadovo sąlyga – privalote turėti galiojančią pirkimo sutartį su tiėkėjo įsipareigojimu dėl produkto kiekio ir prekių.</span><span class="sxs-lookup"><span data-stu-id="11972-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="11972-108">Saugojimo dimensijų grupė nustato, kurios saugojimo dimensijos bus naudojamos produktų operacijoms.</span><span class="sxs-lookup"><span data-stu-id="11972-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="11972-109">Šį vadovą galite vykdyti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="11972-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="11972-110">Jei naudojate USMF, galite pirmiausia paleisti vadovą „Kurti pirkimo sutartį“, kad įvykdytumėte būtinas išankstines šio vadovo sąlygas.</span><span class="sxs-lookup"><span data-stu-id="11972-110">If you're using USMF, you can run the "Create a purchase agreement" guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="11972-111">Pirkimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="11972-111">Create a purchase order</span></span>
1. <span data-ttu-id="11972-112">**Naršymo sritis** eikite į **Darbo sritys > Pirkimo užsakymo paruošimas**.</span><span class="sxs-lookup"><span data-stu-id="11972-112">In the **Navigation pane**, go to **Workspaces > Purchase order preparation**.</span></span> 
2. <span data-ttu-id="11972-113">Spustelėkite **Naujas pirkimo užsakymas**. </span><span class="sxs-lookup"><span data-stu-id="11972-113">Click **New purchase order**.</span></span>
3. <span data-ttu-id="11972-114">Lauke **Tiekėjo sąskaita** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="11972-114">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="11972-115">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="11972-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="11972-116">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="11972-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="11972-117">Išplėskite „fastTab“ **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="11972-117">Expand the **General** fastTab.</span></span>
7. <span data-ttu-id="11972-118">Lauke **Pirkimo sutartis** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="11972-118">In the **Purchase agreement** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="11972-119">Čia išvardytos visos esamos sutartys su tiekėjais.</span><span class="sxs-lookup"><span data-stu-id="11972-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="11972-120">Raskite galiojančią sutartį, kurią norite naudoti.</span><span class="sxs-lookup"><span data-stu-id="11972-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="11972-121">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="11972-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="11972-122">Spustelėkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="11972-122">Click **Yes**.</span></span>
10. <span data-ttu-id="11972-123">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="11972-123">Click **OK**.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="11972-124">Įtraukti eilutę</span><span class="sxs-lookup"><span data-stu-id="11972-124">Add a line</span></span>
1. <span data-ttu-id="11972-125">Lauke **Prekės numeris** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="11972-125">In the **Item number** field, type a value.</span></span> <span data-ttu-id="11972-126">Jei įsipareigojimas nurodo konkrečias atsargų arba vietos dimensijas, turite įvesti tas pačias reikšmes ir pirkimo užsakymo eilutėje, kad galėtumėte naudotis sutartimi.</span><span class="sxs-lookup"><span data-stu-id="11972-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="11972-127">Lauke **Vieta** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="11972-127">In the **Site** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="11972-128">Svetainėje jau gali būti įvesta numatytoji reikšmė iš užsakymo arba iš tiekėjo.</span><span class="sxs-lookup"><span data-stu-id="11972-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="11972-129">Tokiu atveju praleiskite šį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="11972-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="11972-130">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="11972-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="11972-131">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="11972-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="11972-132">Lauke **Kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="11972-132">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="11972-133">Patikrinkite, ar kaina nukopijuota iš įsipareigojimo.</span><span class="sxs-lookup"><span data-stu-id="11972-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="11972-134">Ieškoti įsipareigojimo</span><span class="sxs-lookup"><span data-stu-id="11972-134">Look up the commitment</span></span>
1. <span data-ttu-id="11972-135">Spustelėkite **Naujinti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="11972-135">Click **Update line**.</span></span>
2. <span data-ttu-id="11972-136">Spustelėkite **Pridėta**.</span><span class="sxs-lookup"><span data-stu-id="11972-136">Click **Attached**.</span></span> <span data-ttu-id="11972-137">Čia galite gauti informaciją apie pirkimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="11972-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="11972-138">Pvz., galite matyti kainą ir ar kaina bei nuolaida yra fiksuotos – tai reiškia, kad pakeitus kainos ar nuolaidos reikšmę pirkimo užsakyme į kitą nei nurodyta įsipareigojime, sistema pašalins saitą, todėl pirkimo užsakymo eilutė neatitiks įsipareigojimo.</span><span class="sxs-lookup"><span data-stu-id="11972-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="11972-139">Taip pat galite matyti, ar pasirinkta parinktis „Maksimaliai vykdoma“ – tai reiškia, kad negalima viršyti įsipareigojime nurodyto kiekio sudedant visus pirkimus, kurie atitinka įsipareigojimą.</span><span class="sxs-lookup"><span data-stu-id="11972-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="11972-140">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="11972-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="11972-141">Ieškoti pirkimo sutarties</span><span class="sxs-lookup"><span data-stu-id="11972-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="11972-142">**Veiksmų sritis** spustelėkite **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="11972-142">On the **Action Pane**, click **General**.</span></span>
2. <span data-ttu-id="11972-143">Spustelėkite **Pirkimo sutartis**. </span><span class="sxs-lookup"><span data-stu-id="11972-143">Click **Purchase agreement**.</span></span>
3. <span data-ttu-id="11972-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="11972-144">Close the page.</span></span>
4. <span data-ttu-id="11972-145">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="11972-145">Close the page.</span></span>

