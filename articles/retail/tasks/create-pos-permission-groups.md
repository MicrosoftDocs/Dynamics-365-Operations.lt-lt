--- 
title: " Kurti EKA teisių grupes"
description: "Ši procedūra padės kurti EKA teisių grupę."
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e924dc59c3e4cb9b6979014852512453dd3d70db
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="a1bff-103"> Kurti EKA teisių grupes</span><span class="sxs-lookup"><span data-stu-id="a1bff-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="a1bff-104">Ši procedūra padės kurti EKA teisių grupę.</span><span class="sxs-lookup"><span data-stu-id="a1bff-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="a1bff-105">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USRT.</span><span class="sxs-lookup"><span data-stu-id="a1bff-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="a1bff-106">Ši užduotis skirta mažmeninės prekybos operacijų vadovo vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="a1bff-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="a1bff-107">Pasirinkite Teisių grupės.</span><span class="sxs-lookup"><span data-stu-id="a1bff-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="a1bff-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a1bff-108">Click New.</span></span>
3. <span data-ttu-id="a1bff-109">Lauke EKA teisių grupės ID įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a1bff-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="a1bff-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a1bff-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a1bff-111">Lauke Peržiūrėti laikrodžio įrašus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="a1bff-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="a1bff-112">Dabar galite įjungti arba uždrausti įvairias savo EKA teisių grupės teises.</span><span class="sxs-lookup"><span data-stu-id="a1bff-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="a1bff-113">Galite nustatyti kai kurių teisių reikšmę, kuri bus naudojama siekiant įvertinti, ar EKA vartotojas gali atlikti veiksmą.</span><span class="sxs-lookup"><span data-stu-id="a1bff-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="a1bff-114">Šiame užduočių vadove įjungiamos kelios teisės, kurias galima suteikti kasininkui.</span><span class="sxs-lookup"><span data-stu-id="a1bff-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="a1bff-115">Lauke Leisti kurti užsakymą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="a1bff-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="a1bff-116">Lauke Leisti redaguoti užsakymą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="a1bff-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="a1bff-117">Lauke Leisti nuskaityti užsakymą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="a1bff-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="a1bff-118">Lauke Leisti keisti slaptažodį pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="a1bff-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="a1bff-119">Lauke Leisti anoniminį uždarymą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="a1bff-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="a1bff-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a1bff-120">Click Save.</span></span>
    * <span data-ttu-id="a1bff-121">Įrašius keitimus, reikia paleisti darbuotojų paskirstymo grafiką, kad keitimai būtų taikomi mažmeninės prekybos kanalams.</span><span class="sxs-lookup"><span data-stu-id="a1bff-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="a1bff-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a1bff-122">Close the page.</span></span>
13. <span data-ttu-id="a1bff-123">Pasirinkite Užduotys.</span><span class="sxs-lookup"><span data-stu-id="a1bff-123">Go to Jobs.</span></span>
    * <span data-ttu-id="a1bff-124">Dabar mes priskirsime EKA teisių grupę užduočiai.</span><span class="sxs-lookup"><span data-stu-id="a1bff-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="a1bff-125">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a1bff-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="a1bff-126">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a1bff-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="a1bff-127">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="a1bff-127">Click Edit.</span></span>
17. <span data-ttu-id="a1bff-128">Išplėskite sekciją Užduočių klasifikacija.</span><span class="sxs-lookup"><span data-stu-id="a1bff-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="a1bff-129">Lauke EKA teisių grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a1bff-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="a1bff-130">Visi darbuotojai su šios užduoties pareigomis naudos šios EKA teisių grupės parametrus, nebent darbuotojų EKA teisių nepaisoma pareigų lygyje.</span><span class="sxs-lookup"><span data-stu-id="a1bff-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="a1bff-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a1bff-131">Click Save.</span></span>
    * <span data-ttu-id="a1bff-132">Įrašius keitimus, reikia paleisti darbuotojų paskirstymo grafiką, kad keitimai būtų taikomi mažmeninės prekybos kanalams.</span><span class="sxs-lookup"><span data-stu-id="a1bff-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  


