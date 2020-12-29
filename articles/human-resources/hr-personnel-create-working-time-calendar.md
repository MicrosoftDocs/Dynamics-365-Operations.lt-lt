---
title: Kalendorių kūrimas ir darbo laikų generavimas
description: Kalendoriuje apibūdinamas operacijos išteklius ir pajėgumas ir darbo laikas. Šis straipsnis padės jums nustatyti darbo kalendorių pagal darbo laiko šabloną.
author: andreabichsel
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate, HcmPersonnelManagementWorkspace, WrkCtrGroupDateCalendar, WrkCtrDateCalendar
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f5c630297a8962d1bb383110881b2acdc872b9cd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419645"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="ca16c-104">Kalendorių kūrimas ir darbo laikų generavimas</span><span class="sxs-lookup"><span data-stu-id="ca16c-104">Create calendars and generate working times</span></span>



<span data-ttu-id="ca16c-105">Kalendoriuje apibūdinamas operacijos išteklius ir pajėgumas ir darbo laikas.</span><span class="sxs-lookup"><span data-stu-id="ca16c-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="ca16c-106">Šis straipsnis padės jums nustatyti darbo kalendorių pagal darbo laiko šabloną.</span><span class="sxs-lookup"><span data-stu-id="ca16c-106">This article explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="ca16c-107">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="ca16c-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="ca16c-108">Pagrindiniame puslapyje pasirinkite **Išteklių ciklo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="ca16c-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="ca16c-109">Pasirinkti **Kalendoriai**.</span><span class="sxs-lookup"><span data-stu-id="ca16c-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="ca16c-110">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ca16c-110">Select **New**.</span></span>
4. <span data-ttu-id="ca16c-111">Lauke **Kalendorius** priskirkite kalendorių.</span><span class="sxs-lookup"><span data-stu-id="ca16c-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="ca16c-112">Tai ID kalendorius, kuris naudojamas kaip nuoroda priskiriant kalendorius, pvz., operacijų išteklius arba išteklių grupę.</span><span class="sxs-lookup"><span data-stu-id="ca16c-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="ca16c-113">Tada lauke **Pavadinimas** įveskite savo kalendorių.</span><span class="sxs-lookup"><span data-stu-id="ca16c-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="ca16c-114">Lauke **Standartinė darbo diena valandomis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="ca16c-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="ca16c-115">Įsitikinkite, kad eilutė pažymėta, tada veiksmų srityje pasirinkite **Darbo laikai**.</span><span class="sxs-lookup"><span data-stu-id="ca16c-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="ca16c-116">Pasirinkite **Kurti darbo laikus**.</span><span class="sxs-lookup"><span data-stu-id="ca16c-116">Select **Compose working times**.</span></span> <span data-ttu-id="ca16c-117">Generuokite kiekvienos dienos darbo valandas per laikotarpį, kai norite planuoti darbą.</span><span class="sxs-lookup"><span data-stu-id="ca16c-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="ca16c-118">Laikui bėgant, galite kurti papildomų laikotarpių darbo laikus.</span><span class="sxs-lookup"><span data-stu-id="ca16c-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="ca16c-119">Lauke **Pradžios data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="ca16c-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="ca16c-120">Tai pirma diena, kai šis kalendorius turi būti atidarytas.</span><span class="sxs-lookup"><span data-stu-id="ca16c-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="ca16c-121">Lauke **Pabaigos data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="ca16c-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="ca16c-122">Tai paskutinė diena, kai šis kalendorius yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="ca16c-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="ca16c-123">Lauke **Darbo laiko šablonas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ca16c-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="ca16c-124">Darbo laiko šablonas nurodo kiekvienos savaitės dienos darbo valandas.</span><span class="sxs-lookup"><span data-stu-id="ca16c-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="ca16c-125">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ca16c-125">Select **OK**.</span></span>
13. <span data-ttu-id="ca16c-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ca16c-126">Close the page.</span></span>

