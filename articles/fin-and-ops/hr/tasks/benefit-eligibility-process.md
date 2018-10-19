--- 
title: "Teisės į išmoką apdorojimas"
description: "Šioje procedūroje rodomas išmokų tinkamumo proceso darbas."
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 965826f5fddc2f53f33157434929eb265979376e
ms.openlocfilehash: 859bf2ef369173ce4b6bc380820ea157ae86e13a
ms.contentlocale: lt-lt
ms.lasthandoff: 09/17/2018

---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="63d40-103">Teisės į išmoką apdorojimas</span><span class="sxs-lookup"><span data-stu-id="63d40-103">Benefit eligibility process</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="63d40-104">Šioje procedūroje rodomas išmokų tinkamumo proceso darbas.</span><span class="sxs-lookup"><span data-stu-id="63d40-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="63d40-105">Kai procesas baigtas, galite peržiūrėti rezultatus.</span><span class="sxs-lookup"><span data-stu-id="63d40-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="63d40-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="63d40-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="63d40-107">Pasirinkite Personalas > Išmokos > Išmokos.</span><span class="sxs-lookup"><span data-stu-id="63d40-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="63d40-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="63d40-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="63d40-109">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="63d40-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="63d40-110">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="63d40-110">Click Edit.</span></span>
5. <span data-ttu-id="63d40-111">Lauke Tinkamumas pasirinkite 'Pagal taisyklę'.</span><span class="sxs-lookup"><span data-stu-id="63d40-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="63d40-112">Lauke Taisyklės tipas, pasirinkite išmokos strategijos taisyklę, norimą taikyti išmokai.</span><span class="sxs-lookup"><span data-stu-id="63d40-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="63d40-113">Veiksmų srityje spustelėkite „Išmoka“.</span><span class="sxs-lookup"><span data-stu-id="63d40-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="63d40-114">Spustelėję Kurti tinkamumo įvykį, atidarysite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="63d40-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="63d40-115">Lauke Įvykis įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="63d40-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="63d40-116">Lauke Aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="63d40-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="63d40-117">Lauke Įvykio tipas pasirinkite 'Atidaryti registraciją'.</span><span class="sxs-lookup"><span data-stu-id="63d40-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="63d40-118">Lauke Padengimo pradžios data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="63d40-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="63d40-119">Lauke Registracijos laikotarpio pradžios data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="63d40-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="63d40-120">Lauke Registracijos dienos įveskite numerį.</span><span class="sxs-lookup"><span data-stu-id="63d40-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="63d40-121">Spustelėkite Kurti įvykį.</span><span class="sxs-lookup"><span data-stu-id="63d40-121">Click Create event.</span></span>
16. <span data-ttu-id="63d40-122">Darbuotojų "FastTab" spustelėkite Įtraukti.</span><span class="sxs-lookup"><span data-stu-id="63d40-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="63d40-123">Lauke Rodyti pagal tipą pasirinkite 'Darbuotojai'.</span><span class="sxs-lookup"><span data-stu-id="63d40-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="63d40-124">Lauke Rodyti pagal juridinį subjektą pasirinkite 'Dabartinis juridinis subjektas'.</span><span class="sxs-lookup"><span data-stu-id="63d40-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="63d40-125">Pažymėkite arba atžymėkite visas sąrašo eilutes.</span><span class="sxs-lookup"><span data-stu-id="63d40-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="63d40-126">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="63d40-126">Click OK.</span></span>
21. <span data-ttu-id="63d40-127">Spustelėkite „Apdoroti“.</span><span class="sxs-lookup"><span data-stu-id="63d40-127">Click Process.</span></span>
22. <span data-ttu-id="63d40-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="63d40-128">Click OK.</span></span>
23. <span data-ttu-id="63d40-129">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="63d40-129">Refresh the page.</span></span>
24. <span data-ttu-id="63d40-130">Spustelėkite Rodyti rezultatus.</span><span class="sxs-lookup"><span data-stu-id="63d40-130">Click Show results.</span></span>
25. <span data-ttu-id="63d40-131">Atidarykite Būsenos stulpelio filtrą.</span><span class="sxs-lookup"><span data-stu-id="63d40-131">Open Status column filter.</span></span>
26. <span data-ttu-id="63d40-132">Rikiuoti nuo A iki Z</span><span class="sxs-lookup"><span data-stu-id="63d40-132">Sort A to Z</span></span>


