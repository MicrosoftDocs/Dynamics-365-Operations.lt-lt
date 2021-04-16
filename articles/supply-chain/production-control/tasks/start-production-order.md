---
title: Pradėti gamybos užsakymą
description: Šioje procedūroje nurodoma, kaip paleisti gamybos užsakymą ceche.
author: johanhoffmann
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationStartJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be1c389bc4193ef080dbeb1639b69acf466ef0de
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831871"
---
# <a name="start-a-production-order"></a><span data-ttu-id="9e94d-103">Pradėti gamybos užsakymą</span><span class="sxs-lookup"><span data-stu-id="9e94d-103">Start a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9e94d-104">Šioje procedūroje nurodoma, kaip paleisti gamybos užsakymą ceche.</span><span class="sxs-lookup"><span data-stu-id="9e94d-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="9e94d-105">Šiame procese skelbiamos laiko ir medžiagų sąnaudos.</span><span class="sxs-lookup"><span data-stu-id="9e94d-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="9e94d-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="9e94d-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9e94d-107">Tai yra penkta procedūra iš septynių, kurioje paaiškinamas gamybos užsakymo ciklas.</span><span class="sxs-lookup"><span data-stu-id="9e94d-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="9e94d-108">Pradėti gamybos užsakymą</span><span class="sxs-lookup"><span data-stu-id="9e94d-108">Start a production order</span></span>
1. <span data-ttu-id="9e94d-109">Pasirinkite Gamybos kontrolė > Gamybos užsakymai > Visi gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="9e94d-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="9e94d-110">Pasirinkite gamybos užsakymą, kurio būsena yra Išleistas.</span><span class="sxs-lookup"><span data-stu-id="9e94d-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="9e94d-111">Veiksmų srityje spustelėkite Gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="9e94d-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="9e94d-112">Spustelėkite Pradėti.</span><span class="sxs-lookup"><span data-stu-id="9e94d-112">Click Start.</span></span>
    * <span data-ttu-id="9e94d-113">Šiame puslapyje galite patvirtinti gamybos užsakymo pradžią.</span><span class="sxs-lookup"><span data-stu-id="9e94d-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="9e94d-114">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="9e94d-114">Click the General tab.</span></span>
5. <span data-ttu-id="9e94d-115">Lauke Šaltinio oper.</span><span class="sxs-lookup"><span data-stu-id="9e94d-115">In the From Oper.</span></span> <span data-ttu-id="9e94d-116">Nr.</span><span class="sxs-lookup"><span data-stu-id="9e94d-116">No.</span></span> <span data-ttu-id="9e94d-117">įveskite „10“.</span><span class="sxs-lookup"><span data-stu-id="9e94d-117">field, enter '10'.</span></span>
6. <span data-ttu-id="9e94d-118">Lauke Automatinis maršruto suvartojimas pasirinkite „Visada“.</span><span class="sxs-lookup"><span data-stu-id="9e94d-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="9e94d-119">Spustelėkite žymės langelį Registruoti technologinę kortelę dabar.</span><span class="sxs-lookup"><span data-stu-id="9e94d-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="9e94d-120">Lauke Automatinis KS suvartojimas pasirinkite „Visada“.</span><span class="sxs-lookup"><span data-stu-id="9e94d-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="9e94d-121">Spustelėkite žymės langelį Registruoti išrinkimo dokumentą dabar.</span><span class="sxs-lookup"><span data-stu-id="9e94d-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="9e94d-122">Spustelėkite žymės langelį Spausdinti išrinkimo dokumentą.</span><span class="sxs-lookup"><span data-stu-id="9e94d-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="9e94d-123">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9e94d-123">Click OK.</span></span>
    * <span data-ttu-id="9e94d-124">Tai yra atspausdintas išrinkimo dokumentas, kuriame nurodomos gamybos užsakymui naudojamos medžiagos.</span><span class="sxs-lookup"><span data-stu-id="9e94d-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="9e94d-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9e94d-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="9e94d-126">Išrinkimo dokumento tikrinimas</span><span class="sxs-lookup"><span data-stu-id="9e94d-126">Validate the picking list</span></span>
1. <span data-ttu-id="9e94d-127">Veiksmų srityje spustelėkite Peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="9e94d-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="9e94d-128">Spustelėkite Išrinkimo dokumentas.</span><span class="sxs-lookup"><span data-stu-id="9e94d-128">Click Picking list.</span></span>
3. <span data-ttu-id="9e94d-129">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="9e94d-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="9e94d-130">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="9e94d-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9e94d-131">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="9e94d-131">Click Edit.</span></span>
6. <span data-ttu-id="9e94d-132">Lauke Suvartojimas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9e94d-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="9e94d-133">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="9e94d-133">Click Post.</span></span>
8. <span data-ttu-id="9e94d-134">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9e94d-134">Click OK.</span></span>
    * <span data-ttu-id="9e94d-135">Išrinkimo dokumento žurnale užregistruojamos gamybos užsakymui suvartotos medžiagos.</span><span class="sxs-lookup"><span data-stu-id="9e94d-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="9e94d-136">Prieš užregistruodami žurnalą, jei yra skirtumas tarp įvertinto kiekio ir faktinio suvartoto kiekio, galite atlikti koregavimus.</span><span class="sxs-lookup"><span data-stu-id="9e94d-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="9e94d-137">Spustelėkite skirtuką GridPanel.</span><span class="sxs-lookup"><span data-stu-id="9e94d-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="9e94d-138">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9e94d-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="9e94d-139">Technologinės kortelės žurnalo tikrinimas</span><span class="sxs-lookup"><span data-stu-id="9e94d-139">Verify the route card journal</span></span>
1. <span data-ttu-id="9e94d-140">Veiksmų srityje spustelėkite Peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="9e94d-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="9e94d-141">Spustelėkite Technologinė kortelė.</span><span class="sxs-lookup"><span data-stu-id="9e94d-141">Click Route card.</span></span>
3. <span data-ttu-id="9e94d-142">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="9e94d-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="9e94d-143">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="9e94d-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9e94d-144">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="9e94d-144">Click Edit.</span></span>
6. <span data-ttu-id="9e94d-145">Lauke Valandos įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9e94d-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="9e94d-146">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="9e94d-146">Click Post.</span></span>
8. <span data-ttu-id="9e94d-147">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9e94d-147">Click OK.</span></span>
    * <span data-ttu-id="9e94d-148">Technologinės kortelės žurnale įrašomas atskiroms operacijoms skiriamas laikas.</span><span class="sxs-lookup"><span data-stu-id="9e94d-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="9e94d-149">Taip pat gali būti nurodytas prekių ir klaidų kiekis.</span><span class="sxs-lookup"><span data-stu-id="9e94d-149">Good and error quantity can also be reported.</span></span>  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]