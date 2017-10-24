---
title: "Kurti ir tvarkyti atsargų blokavimą"
description: "Ši procedūra nurodo, kaip neleisti kitiems siunčiamiems šaltinio dokumentams rezervuoti faktiškai turimų atsargų naudojant atsargų blokavimą."
author: perlynne
manager: AnnBe
ms.date: 12/02/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7272349cf16b9459823a752b8d3df915f42606ef
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-maintain-inventory-blocking"></a><span data-ttu-id="cf277-103">Kurti ir tvarkyti atsargų blokavimą</span><span class="sxs-lookup"><span data-stu-id="cf277-103">Create and maintain inventory blocking</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cf277-104">Ši procedūra nurodo, kaip neleisti kitiems siunčiamiems šaltinio dokumentams rezervuoti faktiškai turimų atsargų naudojant atsargų blokavimą.</span><span class="sxs-lookup"><span data-stu-id="cf277-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="cf277-105">Galite vykdyti šią procedūrą demonstracinių duomenų įmonėje USMF naudodami rodomas pavyzdines reikšmes.</span><span class="sxs-lookup"><span data-stu-id="cf277-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="cf277-106">Prieš pradedant šią procedūrą jums reikės turėti prekę su faktiškai turimomis atsargomis.</span><span class="sxs-lookup"><span data-stu-id="cf277-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="cf277-107">Sukurti atsargų blokavimą</span><span class="sxs-lookup"><span data-stu-id="cf277-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="cf277-108">Pasirinkite Atsargų valdymas > Periodinės užduotys > Atsargų blokavimas.</span><span class="sxs-lookup"><span data-stu-id="cf277-108">Go to Inventory management > Periodic tasks > Inventory blocking.</span></span>
2. <span data-ttu-id="cf277-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="cf277-109">Click New.</span></span>
3. <span data-ttu-id="cf277-110">Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="cf277-110">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="cf277-111">Sąraše pasirinkite norimą prekę.</span><span class="sxs-lookup"><span data-stu-id="cf277-111">In the list, select the item you want to choose.</span></span>
    * <span data-ttu-id="cf277-112">Pasirinkite prekės numerį su faktiškai turimomis atsargomis, kurias norite blokuoti.</span><span class="sxs-lookup"><span data-stu-id="cf277-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="cf277-113">Jei naudojate USMF, galite pasirinkti prekę M9201.</span><span class="sxs-lookup"><span data-stu-id="cf277-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="cf277-114">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="cf277-114">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="cf277-115">Jei naudojate prekę M9201, turite pasirinkti mažiau nei 200.</span><span class="sxs-lookup"><span data-stu-id="cf277-115">If you’re using item M9201, you need to select less than 200.</span></span>  
6. <span data-ttu-id="cf277-116">Perjunkite skyriaus „Atsargų matmenys“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="cf277-116">Toggle the expansion of the Inventory dimensions section.</span></span>
7. <span data-ttu-id="cf277-117">Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="cf277-117">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="cf277-118">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="cf277-118">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cf277-119">Jei naudojate prekę M9201, galite pasirinkti sandėlį 51.</span><span class="sxs-lookup"><span data-stu-id="cf277-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="cf277-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="cf277-120">Click Save.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="cf277-121">Atnaujinti atsargų blokavimo sąlygas</span><span class="sxs-lookup"><span data-stu-id="cf277-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="cf277-122">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="cf277-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="cf277-123">Atnaujinkite atsargų kiekio lauką, kad atitiktų norimą blokuoti kiekį.</span><span class="sxs-lookup"><span data-stu-id="cf277-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="cf277-124">Lauke „Numatoma data“ įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="cf277-124">In the Expected date field, enter a date.</span></span>
    * <span data-ttu-id="cf277-125">Galite nurodyti, kada turėtų būti galima rezervuoti užblokuotas atsargas, priskirdami numatomą datą.</span><span class="sxs-lookup"><span data-stu-id="cf277-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="cf277-126">Jei atsargų blokavimui parenkama parinktis „Numatomi gavimai“, kuri būna parenkama pagal numatytuosius nustatymus, kai blokavimą kuriate rankiniu būdu, ši data bus rodoma numatomoje operacijoje.</span><span class="sxs-lookup"><span data-stu-id="cf277-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="cf277-127">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="cf277-127">Click Save.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="cf277-128">Pašalinti atsargų blokavimą</span><span class="sxs-lookup"><span data-stu-id="cf277-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="cf277-129">Spustelėkite Naikinti.</span><span class="sxs-lookup"><span data-stu-id="cf277-129">Click Delete.</span></span>
2. <span data-ttu-id="cf277-130">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="cf277-130">Click Yes.</span></span>
3. <span data-ttu-id="cf277-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="cf277-131">Close the page.</span></span>

