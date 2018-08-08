--- 
title: "Apibrėžti atskiros gamybos išteklių grupę"
description: "Išteklių grupė yra operacijų išteklių rinkinys, kurie paprastai atitinka fizinį darbo elementų išdėstymą, ant gamybos cecho grindų apibrėžtą geltonomis linijomis."
author: sorenva
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
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e1be950a7d1d7548aced041a189222b472d767cf
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="020be-103">Apibrėžti atskiros gamybos išteklių grupę</span><span class="sxs-lookup"><span data-stu-id="020be-103">Define discrete manufacturing resource group</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="020be-104">Išteklių grupė yra operacijų išteklių rinkinys, kurie paprastai atitinka fizinį darbo elementų išdėstymą, ant gamybos cecho grindų apibrėžtą geltonomis linijomis.</span><span class="sxs-lookup"><span data-stu-id="020be-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="020be-105">Ši procedūra parodo, kaip nustatyti išteklių grupę, skirtą naudoti atskiroje gamyboje.</span><span class="sxs-lookup"><span data-stu-id="020be-105">This procedure shows you how to define a resource group for use in discrete production.</span></span> <span data-ttu-id="020be-106">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="020be-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="020be-107">Eikite į Išteklių grupės.</span><span class="sxs-lookup"><span data-stu-id="020be-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="020be-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="020be-108">Click New.</span></span>
3. <span data-ttu-id="020be-109">Lauke Išteklių grupės surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="020be-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="020be-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="020be-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="020be-111">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="020be-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="020be-112">Lauke Gamybos vienetas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="020be-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="020be-113">Nustatyti numatytuosius veiklos parametrus</span><span class="sxs-lookup"><span data-stu-id="020be-113">Define default operational parameters</span></span>
1. <span data-ttu-id="020be-114">Išplėskite skyrių Operacija.</span><span class="sxs-lookup"><span data-stu-id="020be-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="020be-115">Lauke Atliekų procentinė dalis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="020be-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="020be-116">Lauke Nustatymų kategorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="020be-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="020be-117">Lauke Apdorojimo laiko kategorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="020be-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="020be-118">Lauke Operacijų planavimo procentas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="020be-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="020be-119">Nustatyti veikimo valandas</span><span class="sxs-lookup"><span data-stu-id="020be-119">Define operating hours</span></span>
1. <span data-ttu-id="020be-120">Išplėskite skyrių Kalendoriai.</span><span class="sxs-lookup"><span data-stu-id="020be-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="020be-121">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="020be-121">Click Add.</span></span>
3. <span data-ttu-id="020be-122">Lauke Kalendorius įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="020be-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="020be-123">Pridėti operacijų išteklių</span><span class="sxs-lookup"><span data-stu-id="020be-123">Add operations resources</span></span>
1. <span data-ttu-id="020be-124">Išplėskite skyrių Ištekliai.</span><span class="sxs-lookup"><span data-stu-id="020be-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="020be-125">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="020be-125">Click Add.</span></span>
3. <span data-ttu-id="020be-126">Lauke Išteklius įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="020be-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="020be-127">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="020be-127">Click Add.</span></span>
5. <span data-ttu-id="020be-128">Lauke Išteklius įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="020be-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="020be-129">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="020be-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="020be-130">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="020be-130">In the list, click the link in the selected row.</span></span>


