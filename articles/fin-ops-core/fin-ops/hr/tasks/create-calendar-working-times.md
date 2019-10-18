---
title: Kalendorių kūrimas ir darbo laikų generavimas
description: Kalendoriuje apibūdinamas operacijos išteklius ir pajėgumas ir darbo laikas. Ši procedūra padės jums nustatyti darbo kalendorių pagal darbo laiko šabloną.
author: andreabichsel
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 50b81ae228d9aee4111ce8d161508d5ed1af4f27
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190677"
---
# <a name="create-calendar-and-generate-working-times"></a><span data-ttu-id="809d8-104">Kurti kalendorių ir generuoti darbo laikus</span><span class="sxs-lookup"><span data-stu-id="809d8-104">Create calendar and generate working times</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="809d8-105">Kalendoriuje apibūdinamas operacijos išteklius ir pajėgumas ir darbo laikas.</span><span class="sxs-lookup"><span data-stu-id="809d8-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="809d8-106">Ši procedūra padės jums nustatyti darbo kalendorių pagal darbo laiko šabloną.</span><span class="sxs-lookup"><span data-stu-id="809d8-106">This topic explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="809d8-107">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="809d8-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="809d8-108">Pagrindiniame puslapyje pasirinkite **Išteklių ciklo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="809d8-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="809d8-109">Pasirinkti **Kalendoriai**.</span><span class="sxs-lookup"><span data-stu-id="809d8-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="809d8-110">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="809d8-110">Select **New**.</span></span>
4. <span data-ttu-id="809d8-111">Lauke **Kalendorius** priskirkite kalendorių.</span><span class="sxs-lookup"><span data-stu-id="809d8-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="809d8-112">Tai ID kalendorius, kuris naudojamas kaip nuoroda priskiriant kalendorius, pvz., operacijų išteklius arba išteklių grupę.</span><span class="sxs-lookup"><span data-stu-id="809d8-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="809d8-113">Tada lauke **Pavadinimas** įveskite savo kalendorių.</span><span class="sxs-lookup"><span data-stu-id="809d8-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="809d8-114">Lauke **Standartinė darbo diena valandomis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="809d8-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="809d8-115">Įsitikinkite, kad eilutė pažymėta, tada veiksmų srityje pasirinkite **Darbo laikai**.</span><span class="sxs-lookup"><span data-stu-id="809d8-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="809d8-116">Pasirinkite **Kurti darbo laikus**.</span><span class="sxs-lookup"><span data-stu-id="809d8-116">Select **Compose working times**.</span></span> <span data-ttu-id="809d8-117">Generuokite kiekvienos dienos darbo valandas per laikotarpį, kai norite planuoti darbą.</span><span class="sxs-lookup"><span data-stu-id="809d8-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="809d8-118">Laikui bėgant, galite kurti papildomų laikotarpių darbo laikus.</span><span class="sxs-lookup"><span data-stu-id="809d8-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="809d8-119">Lauke **Pradžios data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="809d8-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="809d8-120">Tai pirma diena, kai šis kalendorius turi būti atidarytas.</span><span class="sxs-lookup"><span data-stu-id="809d8-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="809d8-121">Lauke **Pabaigos data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="809d8-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="809d8-122">Tai paskutinė diena, kai šis kalendorius yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="809d8-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="809d8-123">Lauke **Darbo laiko šablonas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="809d8-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="809d8-124">Darbo laiko šablonas nurodo kiekvienos savaitės dienos darbo valandas.</span><span class="sxs-lookup"><span data-stu-id="809d8-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="809d8-125">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="809d8-125">Select **OK**.</span></span>
13. <span data-ttu-id="809d8-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="809d8-126">Close the page.</span></span>

