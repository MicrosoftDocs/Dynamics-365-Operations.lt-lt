---
title: Teikti ir tvirtinti projekto biudžetą
description: Šioje procedūroje nurodoma, kaip sukurti ir pateikti projekto biudžetą.
author: mkirknel
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14683554c45db72061ecbbf4a528656df3132692
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207457"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="a0619-103">Teikti ir tvirtinti projekto biudžetą</span><span class="sxs-lookup"><span data-stu-id="a0619-103">Submit and approve project budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0619-104">Šioje procedūroje nurodoma, kaip sukurti ir pateikti projekto biudžetą.</span><span class="sxs-lookup"><span data-stu-id="a0619-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="a0619-105">Kai kuriate projekto biudžetą, galite įvesti įvertintas projekto įplaukas ir išlaidas, o tada naudoti jas faktinėms projekto operacijoms valdyti.</span><span class="sxs-lookup"><span data-stu-id="a0619-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="a0619-106">Sudarant projekto biudžetą visi pradiniai biudžetai ir tikslinimai turi būti siunčiami į projekto darbo eigą patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="a0619-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="a0619-107">Darbo eiga suteikia didesnę proceso kontrolę ir sukuria keitimų istorijos įrašą.</span><span class="sxs-lookup"><span data-stu-id="a0619-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="a0619-108">Ši užduotis buvo sukurta naudojant USSI duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="a0619-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="a0619-109">**Naršymo srityje** eikite į **Moduliai > Projekto valdymas ir apskaita > Projektai > Visi projektai**.</span><span class="sxs-lookup"><span data-stu-id="a0619-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="a0619-110">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a0619-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a0619-111">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a0619-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a0619-112">Parinktyje **Veiksmų sritis** spustelėkite **Planas**.</span><span class="sxs-lookup"><span data-stu-id="a0619-112">On the **Action Pane**, click **Plan**.</span></span>
5. <span data-ttu-id="a0619-113">Spustelėkite **Projekto biudžetas**.</span><span class="sxs-lookup"><span data-stu-id="a0619-113">Click **Project budget**.</span></span>
6. <span data-ttu-id="a0619-114">Lauke **Aprašo laukas**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a0619-114">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="a0619-115">Išplėskite „fastTab“ **Išlaidos**.</span><span class="sxs-lookup"><span data-stu-id="a0619-115">Expand the **Cost** fastTab.</span></span>
8. <span data-ttu-id="a0619-116">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a0619-116">Click **New**.</span></span>
9. <span data-ttu-id="a0619-117">Lauke **Operacijos tipas** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="a0619-117">In the **Transaction type** field, select an option.</span></span>
10. <span data-ttu-id="a0619-118">Lauke **Kategorija** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a0619-118">In the **Category** field, enter or select a value.</span></span>
11. <span data-ttu-id="a0619-119">Lauke **Pradinis biudžetas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a0619-119">In the **Original budget** field, enter a number.</span></span>
12. <span data-ttu-id="a0619-120">Išplėskite „fastTab“ **Įplaukos**.</span><span class="sxs-lookup"><span data-stu-id="a0619-120">Expand the **Revenues** fastTab.</span></span>
13. <span data-ttu-id="a0619-121">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a0619-121">Click **New**.</span></span>
14. <span data-ttu-id="a0619-122">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a0619-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="a0619-123">Lauke **Operacijos tipas** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="a0619-123">In the **Transaction type** field, select an option.</span></span>
16. <span data-ttu-id="a0619-124">Lauke **Kategorija** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a0619-124">In the **Category** field, enter or select a value.</span></span>
17. <span data-ttu-id="a0619-125">Lauke **Pradinis biudžetas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a0619-125">In the **Original budget** field, enter a number.</span></span>
18. <span data-ttu-id="a0619-126">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a0619-126">Click **Save**.</span></span>
19. <span data-ttu-id="a0619-127">Spustelėkite **Darbo eiga**.</span><span class="sxs-lookup"><span data-stu-id="a0619-127">Click **Workflow**.</span></span>
20. <span data-ttu-id="a0619-128">Spustelėkite **Pateikti**.</span><span class="sxs-lookup"><span data-stu-id="a0619-128">Click **Submit**.</span></span>
21. <span data-ttu-id="a0619-129">Lauke **Komentaras** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a0619-129">In the **Comment** field, type a value.</span></span>
22. <span data-ttu-id="a0619-130">Spustelėkite **Pateikti**.</span><span class="sxs-lookup"><span data-stu-id="a0619-130">Click **Submit**.</span></span>

