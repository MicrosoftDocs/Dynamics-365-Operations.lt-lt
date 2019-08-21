---
title: Teikti ir tvirtinti projekto biudžetą
description: Šioje procedūroje nurodoma, kaip sukurti ir pateikti projekto biudžetą.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ffa7b4f23e63196947fef1b2180145702531e0a6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843918"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="15de1-103">Teikti ir tvirtinti projekto biudžetą</span><span class="sxs-lookup"><span data-stu-id="15de1-103">Submit and approve project budget</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="15de1-104">Šioje procedūroje nurodoma, kaip sukurti ir pateikti projekto biudžetą.</span><span class="sxs-lookup"><span data-stu-id="15de1-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="15de1-105">Kai kuriate projekto biudžetą, galite įvesti įvertintas projekto įplaukas ir išlaidas, o tada naudoti jas faktinėms projekto operacijoms valdyti.</span><span class="sxs-lookup"><span data-stu-id="15de1-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="15de1-106">Sudarant projekto biudžetą visi pradiniai biudžetai ir tikslinimai turi būti siunčiami į projekto darbo eigą patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="15de1-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="15de1-107">Darbo eiga suteikia didesnę proceso kontrolę ir sukuria keitimų istorijos įrašą.</span><span class="sxs-lookup"><span data-stu-id="15de1-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="15de1-108">Ši užduotis buvo sukurta naudojant USSI duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="15de1-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="15de1-109">Eikite į Projektų valdymas ir apskaita > Projektai > Visi projektai.</span><span class="sxs-lookup"><span data-stu-id="15de1-109">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="15de1-110">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="15de1-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="15de1-111">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="15de1-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="15de1-112">Veiksmų srityje spustelėkite Planas.</span><span class="sxs-lookup"><span data-stu-id="15de1-112">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="15de1-113">Spustelėkite Projekto biudžetas.</span><span class="sxs-lookup"><span data-stu-id="15de1-113">Click Project budget.</span></span>
6. <span data-ttu-id="15de1-114">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="15de1-114">In the Description field, type a value.</span></span>
7. <span data-ttu-id="15de1-115">Išplėskite dalį Išlaidos</span><span class="sxs-lookup"><span data-stu-id="15de1-115">Expand the Cost section</span></span>
8. <span data-ttu-id="15de1-116">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="15de1-116">Click New.</span></span>
9. <span data-ttu-id="15de1-117">Lauke Operacijos tipas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="15de1-117">In the Transaction type field, select an option.</span></span>
10. <span data-ttu-id="15de1-118">Lauke Kategorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="15de1-118">In the Category field, enter or select a value.</span></span>
11. <span data-ttu-id="15de1-119">Lauke Pradinis biudžetas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="15de1-119">In the Original budget field, enter a number.</span></span>
12. <span data-ttu-id="15de1-120">Išplėskite dalį Įplaukos.</span><span class="sxs-lookup"><span data-stu-id="15de1-120">Expand the Revenues section.</span></span>
13. <span data-ttu-id="15de1-121">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="15de1-121">Click New.</span></span>
14. <span data-ttu-id="15de1-122">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="15de1-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="15de1-123">Lauke Operacijos tipas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="15de1-123">In the Transaction type field, select an option.</span></span>
16. <span data-ttu-id="15de1-124">Lauke Kategorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="15de1-124">In the Category field, enter or select a value.</span></span>
17. <span data-ttu-id="15de1-125">Lauke Pradinis biudžetas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="15de1-125">In the Original budget field, enter a number.</span></span>
18. <span data-ttu-id="15de1-126">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="15de1-126">Click Save.</span></span>
19. <span data-ttu-id="15de1-127">Spustelėkite Darbo eiga.</span><span class="sxs-lookup"><span data-stu-id="15de1-127">Click Workflow.</span></span>
20. <span data-ttu-id="15de1-128">Spustelėkite Pateikti.</span><span class="sxs-lookup"><span data-stu-id="15de1-128">Click Submit.</span></span>
21. <span data-ttu-id="15de1-129">Lauke Komentaras įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="15de1-129">In the Comment field, type a value.</span></span>
22. <span data-ttu-id="15de1-130">Spustelėkite Pateikti.</span><span class="sxs-lookup"><span data-stu-id="15de1-130">Click Submit.</span></span>

