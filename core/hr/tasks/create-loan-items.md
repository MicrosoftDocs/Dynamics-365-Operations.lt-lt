--- 
title: Kurti panaudos objektus
description: "Skolinamos prekės yra įrašai, kurie padeda sekti fizines prekes, pvz., telefonus arba kompiuterius, kurias jūsų įmonė skolina darbuotojams."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 65655283c70c99b5d64289b319ecc69f6e414221
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="create-loan-items"></a><span data-ttu-id="8017d-103">Kurti panaudos objektus</span><span class="sxs-lookup"><span data-stu-id="8017d-103">Create loan items</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8017d-104">Skolinamos prekės yra įrašai, kurie padeda sekti fizines prekes, pvz., telefonus arba kompiuterius, kurias jūsų įmonė skolina darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="8017d-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="8017d-105">Kiekviena fizinė prekė turi turėti atitinkamą skolinamą prekę.</span><span class="sxs-lookup"><span data-stu-id="8017d-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="8017d-106">Kiekviename skolinamos prekės įraše turi būti aprašyta, kas skolinama, kas atsakingas už paskolą ir kiek dienų prekę galima skolinti.</span><span class="sxs-lookup"><span data-stu-id="8017d-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="8017d-107">Vienu kartu galite sukurti keletą skolinamų prekių, pvz., raktų, įėjimo kortelių ar uniformų.</span><span class="sxs-lookup"><span data-stu-id="8017d-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="8017d-108">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="8017d-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="8017d-109">Kurti paskolų tipus</span><span class="sxs-lookup"><span data-stu-id="8017d-109">Create Loan types</span></span>
1. <span data-ttu-id="8017d-110">Eikite į Žmogiškieji ištekliai > Darbuotojai > Skolinamos prekės > Paskolų tipai.</span><span class="sxs-lookup"><span data-stu-id="8017d-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="8017d-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="8017d-111">Click New.</span></span>
3. <span data-ttu-id="8017d-112">Lauke „Paskolos tipas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8017d-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="8017d-113">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8017d-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8017d-114">Įveskite dienų, kurias šiam paskolos tipui priskirtų prekių grąžinimas gali vėluoti, skaičių.</span><span class="sxs-lookup"><span data-stu-id="8017d-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="8017d-115">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="8017d-115">Click Save.</span></span>
7. <span data-ttu-id="8017d-116">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8017d-116">Close the page.</span></span>
8. <span data-ttu-id="8017d-117">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8017d-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="8017d-118">Kurti panaudos objektus</span><span class="sxs-lookup"><span data-stu-id="8017d-118">Create Loan items</span></span>
1. <span data-ttu-id="8017d-119">Eikite į Žmogiškieji ištekliai > Darbuotojai > Skolinamos prekės > Skolinamos prekės.</span><span class="sxs-lookup"><span data-stu-id="8017d-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="8017d-120">Spustelėkite „Sukurti skolinamas prekes“.</span><span class="sxs-lookup"><span data-stu-id="8017d-120">Click Create loan items.</span></span>
3. <span data-ttu-id="8017d-121">Kiekyje.</span><span class="sxs-lookup"><span data-stu-id="8017d-121">In the Qty.</span></span> <span data-ttu-id="8017d-122">įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="8017d-122">field, enter a number.</span></span>
4. <span data-ttu-id="8017d-123">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8017d-123">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8017d-124">Lauke „Paskolos tipas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="8017d-124">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="8017d-125">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="8017d-125">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="8017d-126">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="8017d-126">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="8017d-127">Įveskite skaičių dienų, kurias prekė gali būti paskolinta.</span><span class="sxs-lookup"><span data-stu-id="8017d-127">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="8017d-128">Puslapyje „Paskolinta įranga“ esančio lauko „Planuojamas grąžinimas“ numatytoji vertė apskaičiuojama prie dabartinės datos pridedant šį skaičių.</span><span class="sxs-lookup"><span data-stu-id="8017d-128">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="8017d-129">Lauke „Vadovaujantysis asmuo“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="8017d-129">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="8017d-130">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="8017d-130">Click Select.</span></span>
11. <span data-ttu-id="8017d-131">Lauke „Pradinė reikšmė“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="8017d-131">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="8017d-132">Lauke „Intervalas“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="8017d-132">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="8017d-133">Lauke „Formatas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8017d-133">In the Format field, type a value.</span></span>
    * <span data-ttu-id="8017d-134">Pvz., jei skolinamos prekės pradžios numeris yra 10, lauke „Formatas“ įveskite du numerio simbolius.</span><span class="sxs-lookup"><span data-stu-id="8017d-134">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="8017d-135">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="8017d-135">Click OK.</span></span>
15. <span data-ttu-id="8017d-136">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8017d-136">Refresh the page.</span></span>


