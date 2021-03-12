---
title: Plano su apribojimais kūrimas
description: Šioje temoje aiškinama, kaip sukurti planą, kuriame būtų atsižvelgta į medžiagos ir pajėgumo apribojimus.
author: ShylaThompson
manager: tfehr
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d4af946a8dd4e5311bcb90386c88d5e7f205c4eb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999861"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="a8803-103">Plano su apribojimais kūrimas</span><span class="sxs-lookup"><span data-stu-id="a8803-103">Generate a constrained plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a8803-104">Šioje temoje aiškinama, kaip sukurti planą, kuriame būtų atsižvelgta į medžiagos ir pajėgumo apribojimus.</span><span class="sxs-lookup"><span data-stu-id="a8803-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="a8803-105">Planas užtikrina, kad gamyba neprasidėtų tol, kol bus turima medžiagų ir nebus perpildyti ištekliai.</span><span class="sxs-lookup"><span data-stu-id="a8803-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="a8803-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="a8803-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a8803-107">Ši procedūra yra skirta gamybos planuotojui.</span><span class="sxs-lookup"><span data-stu-id="a8803-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="a8803-108">Nustatyti planą su apribojimais</span><span class="sxs-lookup"><span data-stu-id="a8803-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="a8803-109">Pagrindiniame puslapyje pažymėkite darbo sritį **Pagrindinis planavimas**.</span><span class="sxs-lookup"><span data-stu-id="a8803-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="a8803-110">Darbo srities dešinėje pusėje saitų sąraše pažymėkite **Pagrindiniai planai**.</span><span class="sxs-lookup"><span data-stu-id="a8803-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="a8803-111">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a8803-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="a8803-112">Pavyzdys: **StaticPlan**</span><span class="sxs-lookup"><span data-stu-id="a8803-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="a8803-113">Pasirinkite **Taip** lauke **Ribotas pajėgumas**.</span><span class="sxs-lookup"><span data-stu-id="a8803-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="a8803-114">Lauke **Riboto pajėgumo laiko riba** įveskite `30`.</span><span class="sxs-lookup"><span data-stu-id="a8803-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="a8803-115">Išplėskite skyrių **Laiko riba dienomis**.</span><span class="sxs-lookup"><span data-stu-id="a8803-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="a8803-116">Pasirinkite **Taip** lauke **Pajėgumas**.</span><span class="sxs-lookup"><span data-stu-id="a8803-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="a8803-117">Lauke **Pajėgumo planavimo laiko riba (dienomis)** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a8803-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="a8803-118">Pavyzdys: `60`</span><span class="sxs-lookup"><span data-stu-id="a8803-118">Example: `60`</span></span>  
9. <span data-ttu-id="a8803-119">Pasirinkite **Taip** lauke **Apskaičiuotos delsos**.</span><span class="sxs-lookup"><span data-stu-id="a8803-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="a8803-120">Lauke **Apskaičiuotų delsų laiko riba (dienomis)** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a8803-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="a8803-121">Pavyzdys: `60`</span><span class="sxs-lookup"><span data-stu-id="a8803-121">Example: `60`</span></span> 
11. <span data-ttu-id="a8803-122">Išplėskite skyrių **Apskaičiuotos delsos**.</span><span class="sxs-lookup"><span data-stu-id="a8803-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="a8803-123">Visuose laukuose **Įtraukti apskaičiuotą delsą į reikalavimo datą** pažymėkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="a8803-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="a8803-124">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a8803-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="a8803-125">Kurti planą su apribojimais</span><span class="sxs-lookup"><span data-stu-id="a8803-125">Create a constrained plan</span></span>
1. <span data-ttu-id="a8803-126">Pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="a8803-126">Select **Run**.</span></span>
2. <span data-ttu-id="a8803-127">Lauke **Pagrindinis planas** įveskite arba pasirinkite planą, kuriam nustatėte apribojimus.</span><span class="sxs-lookup"><span data-stu-id="a8803-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="a8803-128">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a8803-128">Select **OK**.</span></span>
4. <span data-ttu-id="a8803-129">Pažymėkite **Suplanuoti užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="a8803-129">Select **Planned orders**.</span></span>

