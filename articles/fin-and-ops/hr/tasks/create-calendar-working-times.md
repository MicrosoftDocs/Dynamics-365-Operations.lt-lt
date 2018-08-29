--- 
title: "Kalendorių kūrimas ir darbo laikų generavimas"
description: "Kalendoriuje apibūdinamas operacijos išteklius ir pajėgumas ir darbo laikas."
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 9e0b574d83272acf9ccad49e29e80827810b783a
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="d7166-103">Kalendorių kūrimas ir darbo laikų generavimas</span><span class="sxs-lookup"><span data-stu-id="d7166-103">Create calendars and generate working times</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d7166-104">Kalendoriuje apibūdinamas operacijos išteklius ir pajėgumas ir darbo laikas.</span><span class="sxs-lookup"><span data-stu-id="d7166-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="d7166-105">Ši procedūra padės jums nustatyti darbo kalendorių pagal darbo laiko šabloną.</span><span class="sxs-lookup"><span data-stu-id="d7166-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="d7166-106">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="d7166-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="d7166-107">Pasirinkite Visos darbo sritys > Išteklių naudojimo ciklo valdymas.</span><span class="sxs-lookup"><span data-stu-id="d7166-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="d7166-108">Spustelėkite Kalendoriai.</span><span class="sxs-lookup"><span data-stu-id="d7166-108">Click Calendars.</span></span>
3. <span data-ttu-id="d7166-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="d7166-109">Click New.</span></span>
4. <span data-ttu-id="d7166-110">Lauke Kalendorius įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="d7166-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="d7166-111">Tai ID kalendorius, kuris naudojamas kaip nuoroda priskiriant kalendorius, pvz., operacijų išteklius arba išteklių grupę.</span><span class="sxs-lookup"><span data-stu-id="d7166-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="d7166-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d7166-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="d7166-113">Standartinės darbo dienos valandų lauke, įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d7166-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="d7166-114">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d7166-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="d7166-115">Spustelėkite Darbo laikai.</span><span class="sxs-lookup"><span data-stu-id="d7166-115">Click Working times.</span></span>
9. <span data-ttu-id="d7166-116">Spustelėkite Kurti darbo laikus.</span><span class="sxs-lookup"><span data-stu-id="d7166-116">Click Compose working times.</span></span>
    * <span data-ttu-id="d7166-117">Generuokite kiekvienos dienos darbo valandas per laikotarpį, kai norite planuoti darbą.</span><span class="sxs-lookup"><span data-stu-id="d7166-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="d7166-118">Laikui bėgant, galite kurti papildomų laikotarpių darbo laikus.</span><span class="sxs-lookup"><span data-stu-id="d7166-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="d7166-119">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="d7166-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="d7166-120">Tai pirma diena, kai šis kalendorius turi būti atidarytas.</span><span class="sxs-lookup"><span data-stu-id="d7166-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="d7166-121">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="d7166-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="d7166-122">Tai paskutinė diena, kai šis kalendorius yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="d7166-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="d7166-123">Lauke Darbo laiko šablonas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="d7166-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="d7166-124">Darbo laiko šablonas nurodo kiekvienos savaitės dienos darbo valandas.</span><span class="sxs-lookup"><span data-stu-id="d7166-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="d7166-125">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="d7166-125">Click OK.</span></span>
14. <span data-ttu-id="d7166-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d7166-126">Close the page.</span></span>


