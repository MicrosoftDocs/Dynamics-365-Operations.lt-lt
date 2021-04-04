---
title: Teisės į išmoką apdorojimas
description: Šioje procedūroje rodomas išmokų tinkamumo proceso darbas.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 3720adf26d2cb942bc5d9f6988641bf5e504a852
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465131"
---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="57505-103">Teisės į išmoką apdorojimas</span><span class="sxs-lookup"><span data-stu-id="57505-103">Benefit eligibility process</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="57505-104">Šioje procedūroje rodomas išmokų tinkamumo proceso darbas.</span><span class="sxs-lookup"><span data-stu-id="57505-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="57505-105">Kai procesas baigtas, galite peržiūrėti rezultatus.</span><span class="sxs-lookup"><span data-stu-id="57505-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="57505-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="57505-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="57505-107">Pasirinkite Personalas > Išmokos > Išmokos.</span><span class="sxs-lookup"><span data-stu-id="57505-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="57505-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="57505-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="57505-109">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="57505-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="57505-110">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="57505-110">Click Edit.</span></span>
5. <span data-ttu-id="57505-111">Lauke Tinkamumas pasirinkite 'Pagal taisyklę'.</span><span class="sxs-lookup"><span data-stu-id="57505-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="57505-112">Lauke Taisyklės tipas, pasirinkite išmokos strategijos taisyklę, norimą taikyti išmokai.</span><span class="sxs-lookup"><span data-stu-id="57505-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="57505-113">Veiksmų srityje spustelėkite „Išmoka“.</span><span class="sxs-lookup"><span data-stu-id="57505-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="57505-114">Spustelėję Kurti tinkamumo įvykį, atidarysite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="57505-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="57505-115">Lauke Įvykis įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="57505-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="57505-116">Lauke Aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="57505-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="57505-117">Lauke Įvykio tipas pasirinkite 'Atidaryti registraciją'.</span><span class="sxs-lookup"><span data-stu-id="57505-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="57505-118">Lauke Padengimo pradžios data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="57505-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="57505-119">Lauke Registracijos laikotarpio pradžios data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="57505-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="57505-120">Lauke Registracijos dienos įveskite numerį.</span><span class="sxs-lookup"><span data-stu-id="57505-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="57505-121">Spustelėkite Kurti įvykį.</span><span class="sxs-lookup"><span data-stu-id="57505-121">Click Create event.</span></span>
16. <span data-ttu-id="57505-122">Darbuotojų "FastTab" spustelėkite Įtraukti.</span><span class="sxs-lookup"><span data-stu-id="57505-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="57505-123">Lauke Rodyti pagal tipą pasirinkite 'Darbuotojai'.</span><span class="sxs-lookup"><span data-stu-id="57505-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="57505-124">Lauke Rodyti pagal juridinį subjektą pasirinkite 'Dabartinis juridinis subjektas'.</span><span class="sxs-lookup"><span data-stu-id="57505-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="57505-125">Pažymėkite arba atžymėkite visas sąrašo eilutes.</span><span class="sxs-lookup"><span data-stu-id="57505-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="57505-126">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="57505-126">Click OK.</span></span>
21. <span data-ttu-id="57505-127">Spustelėkite „Apdoroti“.</span><span class="sxs-lookup"><span data-stu-id="57505-127">Click Process.</span></span>
22. <span data-ttu-id="57505-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="57505-128">Click OK.</span></span>
23. <span data-ttu-id="57505-129">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="57505-129">Refresh the page.</span></span>
24. <span data-ttu-id="57505-130">Spustelėkite Rodyti rezultatus.</span><span class="sxs-lookup"><span data-stu-id="57505-130">Click Show results.</span></span>
25. <span data-ttu-id="57505-131">Atidarykite Būsenos stulpelio filtrą.</span><span class="sxs-lookup"><span data-stu-id="57505-131">Open Status column filter.</span></span>
26. <span data-ttu-id="57505-132">Rikiuoti nuo A iki Z</span><span class="sxs-lookup"><span data-stu-id="57505-132">Sort A to Z</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]