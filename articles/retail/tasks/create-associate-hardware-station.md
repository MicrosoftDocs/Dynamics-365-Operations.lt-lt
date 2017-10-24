--- 
title: " Kurti ir susieti aparatūros stotį"
description: "Šioje procedūroje nurodyta, kaip kurti naują aparatūros stotį."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2705008908699bda9479eb54a4827c71f402b603
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="3d97b-103"> Kurti ir susieti aparatūros stotį</span><span class="sxs-lookup"><span data-stu-id="3d97b-103">Create and associate a hardware station</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="3d97b-104">Šioje procedūroje nurodyta, kaip kurti naują aparatūros stotį.</span><span class="sxs-lookup"><span data-stu-id="3d97b-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="3d97b-105">Naujos aparatūros šablonas bus sukurtas ir naudojamas naujoms aparatūros stotims į iš anksto nustatytą parduotuvę (kanalą) įtraukti.</span><span class="sxs-lookup"><span data-stu-id="3d97b-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="3d97b-106">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="3d97b-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="3d97b-107">Eikite į Prekybos pagrindai > Kanalai >...</span><span class="sxs-lookup"><span data-stu-id="3d97b-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="3d97b-108">> ..</span><span class="sxs-lookup"><span data-stu-id="3d97b-108">> ..</span></span> <span data-ttu-id="3d97b-109">> ..</span><span class="sxs-lookup"><span data-stu-id="3d97b-109">> ..</span></span> <span data-ttu-id="3d97b-110">> Aparatūros stoties profiliai.</span><span class="sxs-lookup"><span data-stu-id="3d97b-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="3d97b-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3d97b-111">Click New.</span></span>
3. <span data-ttu-id="3d97b-112">Lauke Aparatūros stoties ID įveskite „TestHWProfile“.</span><span class="sxs-lookup"><span data-stu-id="3d97b-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="3d97b-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3d97b-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="3d97b-114">Lauke Prievado numeris įveskite numerį.</span><span class="sxs-lookup"><span data-stu-id="3d97b-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="3d97b-115">Lauke Aparatūros profilis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3d97b-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="3d97b-116">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3d97b-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="3d97b-117">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3d97b-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="3d97b-118">Lauke Paketo pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3d97b-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="3d97b-119">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3d97b-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3d97b-120">Tai yra standartinis paketas, teikiamas su nauja aplinka.</span><span class="sxs-lookup"><span data-stu-id="3d97b-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="3d97b-121">Versijos numeris gali skirtis.</span><span class="sxs-lookup"><span data-stu-id="3d97b-121">The version number may vary.</span></span>  
11. <span data-ttu-id="3d97b-122">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3d97b-122">Click Save.</span></span>
12. <span data-ttu-id="3d97b-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3d97b-123">Close the page.</span></span>
13. <span data-ttu-id="3d97b-124">Pasirinkite Mažmeninė prekyba ir prekyba > Kanalai > Visos mažmeninės prekybos parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="3d97b-124">Go to Retail and commerce > Channels > All retail stores.</span></span>
14. <span data-ttu-id="3d97b-125">Sąraše pasirinkite 17 eilutę.</span><span class="sxs-lookup"><span data-stu-id="3d97b-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="3d97b-126">Jei naudojate demonstracinių duomenų įmonę USRT, tai yra „Houston“ parduotuvė.</span><span class="sxs-lookup"><span data-stu-id="3d97b-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="3d97b-127">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3d97b-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="3d97b-128">Perjunkite sekcijos Aparatūros stotys išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="3d97b-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="3d97b-129">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3d97b-129">Click Add.</span></span>
18. <span data-ttu-id="3d97b-130">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="3d97b-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="3d97b-131">Lauke Šablono ID spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3d97b-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="3d97b-132">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3d97b-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3d97b-133">Tai turi būti naujas aparatūros stoties šablonas, sukurtas atliekant ankstesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3d97b-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="3d97b-134">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3d97b-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="3d97b-135">Lauke Pagrindinio kompiuterio vardas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3d97b-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="3d97b-136">Lauke EFT terminalo ID įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3d97b-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="3d97b-137">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3d97b-137">Click Save.</span></span>


