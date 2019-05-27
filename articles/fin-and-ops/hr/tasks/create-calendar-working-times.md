---
title: Kurti kalendorių ir generuoti darbo laikus
description: Kalendoriuje apibūdinamas operacijos išteklius ir pajėgumas ir darbo laikas.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: ba4bd51d2102b3036307f34ab46f94f83df4f461
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510133"
---
# <a name="create-calendar-and-generate-working-times"></a><span data-ttu-id="fb4d7-103">Kurti kalendorių ir generuoti darbo laikus</span><span class="sxs-lookup"><span data-stu-id="fb4d7-103">Create calendar and generate working times</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fb4d7-104">Kalendoriuje apibūdinamas operacijos išteklius ir pajėgumas ir darbo laikas.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="fb4d7-105">Ši procedūra padės jums nustatyti darbo kalendorių pagal darbo laiko šabloną.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="fb4d7-106">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="fb4d7-107">Pasirinkite Visos darbo sritys > Išteklių naudojimo ciklo valdymas.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="fb4d7-108">Spustelėkite Kalendoriai.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-108">Click Calendars.</span></span>
3. <span data-ttu-id="fb4d7-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-109">Click New.</span></span>
4. <span data-ttu-id="fb4d7-110">Lauke Kalendorius įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="fb4d7-111">Tai ID kalendorius, kuris naudojamas kaip nuoroda priskiriant kalendorius, pvz., operacijų išteklius arba išteklių grupę.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="fb4d7-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="fb4d7-113">Standartinės darbo dienos valandų lauke, įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="fb4d7-114">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="fb4d7-115">Spustelėkite Darbo laikai.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-115">Click Working times.</span></span>
9. <span data-ttu-id="fb4d7-116">Spustelėkite Kurti darbo laikus.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-116">Click Compose working times.</span></span>
    * <span data-ttu-id="fb4d7-117">Generuokite kiekvienos dienos darbo valandas per laikotarpį, kai norite planuoti darbą.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="fb4d7-118">Laikui bėgant, galite kurti papildomų laikotarpių darbo laikus.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="fb4d7-119">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="fb4d7-120">Tai pirma diena, kai šis kalendorius turi būti atidarytas.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="fb4d7-121">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="fb4d7-122">Tai paskutinė diena, kai šis kalendorius yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="fb4d7-123">Lauke Darbo laiko šablonas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="fb4d7-124">Darbo laiko šablonas nurodo kiekvienos savaitės dienos darbo valandas.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="fb4d7-125">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-125">Click OK.</span></span>
14. <span data-ttu-id="fb4d7-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fb4d7-126">Close the page.</span></span>

