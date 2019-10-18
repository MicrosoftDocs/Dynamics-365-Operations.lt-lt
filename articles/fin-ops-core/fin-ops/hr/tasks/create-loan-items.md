---
title: Kurti panaudos objektus
description: Skolinamos prekės yra įrašai, kurie padeda sekti fizines prekes, pvz., telefonus arba kompiuterius, kurias jūsų įmonė skolina darbuotojams.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75b2f17eb41ead7422276f72429eb6ede2ef4759
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179142"
---
# <a name="create-loan-items"></a><span data-ttu-id="e6a0b-103">Kurti panaudos objektus</span><span class="sxs-lookup"><span data-stu-id="e6a0b-103">Create loan items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e6a0b-104">Skolinamos prekės yra įrašai, kurie padeda sekti fizines prekes, pvz., telefonus arba kompiuterius, kurias jūsų įmonė skolina darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="e6a0b-105">Kiekviena fizinė prekė turi turėti atitinkamą skolinamą prekę.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="e6a0b-106">Kiekviename skolinamos prekės įraše turi būti aprašyta, kas skolinama, kas atsakingas už paskolą ir kiek dienų prekę galima skolinti.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="e6a0b-107">Vienu kartu galite sukurti keletą skolinamų prekių, pvz., raktų, įėjimo kortelių ar uniformų.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="e6a0b-108">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="e6a0b-109">Kurti paskolų tipus</span><span class="sxs-lookup"><span data-stu-id="e6a0b-109">Create Loan types</span></span>
1. <span data-ttu-id="e6a0b-110">Eikite į Žmogiškieji ištekliai > Darbuotojai > Skolinamos prekės > Paskolų tipai.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="e6a0b-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-111">Click New.</span></span>
3. <span data-ttu-id="e6a0b-112">Lauke „Paskolos tipas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="e6a0b-113">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e6a0b-114">Įveskite dienų, kurias šiam paskolos tipui priskirtų prekių grąžinimas gali vėluoti, skaičių.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="e6a0b-115">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-115">Click Save.</span></span>
7. <span data-ttu-id="e6a0b-116">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-116">Close the page.</span></span>
8. <span data-ttu-id="e6a0b-117">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="e6a0b-118">Kurti panaudos objektus</span><span class="sxs-lookup"><span data-stu-id="e6a0b-118">Create Loan items</span></span>
1. <span data-ttu-id="e6a0b-119">Eikite į Žmogiškieji ištekliai > Darbuotojai > Skolinamos prekės > Skolinamos prekės.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="e6a0b-120">Spustelėkite „Sukurti skolinamas prekes“.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-120">Click Create loan items.</span></span>
3. <span data-ttu-id="e6a0b-121">Kiekio įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="e6a0b-122">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e6a0b-123">Lauke „Paskolos tipas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e6a0b-124">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e6a0b-125">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e6a0b-126">Įveskite skaičių dienų, kurias prekė gali būti paskolinta.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="e6a0b-127">Puslapyje „Paskolinta įranga“ esančio lauko „Planuojamas grąžinimas“ numatytoji vertė apskaičiuojama prie dabartinės datos pridedant šį skaičių.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="e6a0b-128">Lauke „Vadovaujantysis asmuo“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="e6a0b-129">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-129">Click Select.</span></span>
11. <span data-ttu-id="e6a0b-130">Lauke „Pradinė reikšmė“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="e6a0b-131">Lauke „Intervalas“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="e6a0b-132">Lauke „Formatas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="e6a0b-133">Pvz., jei skolinamos prekės pradžios numeris yra 10, lauke „Formatas“ įveskite du numerio simbolius.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-133">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="e6a0b-134">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-134">Click OK.</span></span>
15. <span data-ttu-id="e6a0b-135">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-135">Refresh the page.</span></span>

