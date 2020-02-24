---
title: Pristatyti darbuotojų išmokų programą
description: Šiame straipsnyje sužinosite, kaip kurti išmokų elementus, kurie bus naudojami kuriant naują išmoką.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: b8631e4f8cb2947ec7e09de86a7ceb075a83a453
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010006"
---
# <a name="deliver-employee-benefits-program"></a><span data-ttu-id="77ca9-103">Pristatyti darbuotojų išmokų programą</span><span class="sxs-lookup"><span data-stu-id="77ca9-103">Deliver employee benefits program</span></span>

<span data-ttu-id="77ca9-104">Šiame straipsnyje sužinosite, kaip kurti išmokų elementus, kurie bus naudojami kuriant naują išmoką.</span><span class="sxs-lookup"><span data-stu-id="77ca9-104">This article shows you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="77ca9-105">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="77ca9-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="77ca9-106">Ši užduotis yra skirta kompensacijų ir išmokų vadovui.</span><span class="sxs-lookup"><span data-stu-id="77ca9-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="77ca9-107">Kurti išmokų elementus</span><span class="sxs-lookup"><span data-stu-id="77ca9-107">Create benefit elements</span></span>
1. <span data-ttu-id="77ca9-108">Ši užduotis prasideda puslapyje Išmokų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="77ca9-108">This task starts from the Benefits list page.</span></span> <span data-ttu-id="77ca9-109">Pradėkite užduotį atidarydami puslapį Išmokų sąrašas arba jo ieškodami.</span><span class="sxs-lookup"><span data-stu-id="77ca9-109">Start the task by opening that page or searching the Benefits list page.</span></span>
2. <span data-ttu-id="77ca9-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="77ca9-110">Click New.</span></span>
3. <span data-ttu-id="77ca9-111">Lauke Tipas įveskite kuriamo išmokų tipo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="77ca9-111">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="77ca9-112">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="77ca9-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="77ca9-113">Lauke Registravimas tuo pačiu metu pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="77ca9-113">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="77ca9-114">Norėdami apriboti darbuotojų galimybę registruotis keliems medicinos planams, pasirinkite Viena vieno tipo registracija.</span><span class="sxs-lookup"><span data-stu-id="77ca9-114">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="77ca9-115">Lauke Algalapių kategorija pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="77ca9-115">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="77ca9-116">Spustelėkite skirtuką Planai.</span><span class="sxs-lookup"><span data-stu-id="77ca9-116">Click the Plans tab.</span></span>
8. <span data-ttu-id="77ca9-117">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="77ca9-117">Click New.</span></span>
9. <span data-ttu-id="77ca9-118">Lauke Planas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="77ca9-118">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="77ca9-119">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="77ca9-119">In the Description field, type a value.</span></span>
11. <span data-ttu-id="77ca9-120">Lauke Tipas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="77ca9-120">In the Type field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="77ca9-121">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="77ca9-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="77ca9-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="77ca9-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="77ca9-123">Lauke Poveikis algalapiui pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="77ca9-123">In the Payroll impact field, select an option.</span></span>
15. <span data-ttu-id="77ca9-124">Spustelėkite skirtuką Parinktys.</span><span class="sxs-lookup"><span data-stu-id="77ca9-124">Click the Options tab.</span></span>
16. <span data-ttu-id="77ca9-125">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="77ca9-125">Click New.</span></span>
17. <span data-ttu-id="77ca9-126">Lauke Parinktis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="77ca9-126">In the Option field, type a value.</span></span>
18. <span data-ttu-id="77ca9-127">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="77ca9-127">In the Description field, type a value.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="77ca9-128">Išmokos kūrimas</span><span class="sxs-lookup"><span data-stu-id="77ca9-128">Create a benefit</span></span>
1. <span data-ttu-id="77ca9-129">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="77ca9-129">Close the page.</span></span>
2. <span data-ttu-id="77ca9-130">Pasirinkite Personalas > Išmokos > Išmokos.</span><span class="sxs-lookup"><span data-stu-id="77ca9-130">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="77ca9-131">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="77ca9-131">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="77ca9-132">Lauke Planas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="77ca9-132">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="77ca9-133">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="77ca9-133">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="77ca9-134">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="77ca9-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="77ca9-135">Lauke Parinktis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="77ca9-135">In the Option field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="77ca9-136">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="77ca9-136">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="77ca9-137">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="77ca9-137">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="77ca9-138">Lauke Įsigalioja įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="77ca9-138">In the Effective field, enter a date and time.</span></span>
11. <span data-ttu-id="77ca9-139">Spustelėkite Kurti išmoką.</span><span class="sxs-lookup"><span data-stu-id="77ca9-139">Click Create benefit.</span></span>
12. <span data-ttu-id="77ca9-140">Perjunkite dalies Algalapio informacija išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="77ca9-140">Toggle the expansion of the Payroll details section.</span></span>
13. <span data-ttu-id="77ca9-141">Lauke Dažnis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="77ca9-141">In the Frequency field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="77ca9-142">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="77ca9-142">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="77ca9-143">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="77ca9-143">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="77ca9-144">Lauke Pagrindas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="77ca9-144">In the Basis field, select an option.</span></span>
17. <span data-ttu-id="77ca9-145">Lauke Suma arba koeficientas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="77ca9-145">In the Amount or rate field, enter a number.</span></span>

