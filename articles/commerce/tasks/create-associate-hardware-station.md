---
title: Aparatūros stoties kūrimas ir susiejimas
description: Šioje procedūroje nurodyta, kaip kurti naują aparatūros stotį.
author: jashanno
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4402e8d1179499512034e7deb8b3eb78f12096f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798590"
---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="54a77-103">Aparatūros stoties kūrimas ir susiejimas</span><span class="sxs-lookup"><span data-stu-id="54a77-103">Create and associate a hardware station</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54a77-104">Šioje procedūroje nurodyta, kaip kurti naują aparatūros stotį.</span><span class="sxs-lookup"><span data-stu-id="54a77-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="54a77-105">Naujos aparatūros šablonas bus sukurtas ir naudojamas naujoms aparatūros stotims į iš anksto nustatytą parduotuvę (kanalą) įtraukti.</span><span class="sxs-lookup"><span data-stu-id="54a77-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="54a77-106">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="54a77-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="54a77-107">Eikite į Prekybos pagrindai > Kanalai >..</span><span class="sxs-lookup"><span data-stu-id="54a77-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="54a77-108">> ..</span><span class="sxs-lookup"><span data-stu-id="54a77-108">> ..</span></span> <span data-ttu-id="54a77-109">> ..</span><span class="sxs-lookup"><span data-stu-id="54a77-109">> ..</span></span> <span data-ttu-id="54a77-110">> Aparatūros stoties profiliai.</span><span class="sxs-lookup"><span data-stu-id="54a77-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="54a77-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="54a77-111">Click New.</span></span>
3. <span data-ttu-id="54a77-112">Lauke Aparatūros stoties ID įveskite „TestHWProfile“.</span><span class="sxs-lookup"><span data-stu-id="54a77-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="54a77-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54a77-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="54a77-114">Lauke Prievado numeris įveskite numerį.</span><span class="sxs-lookup"><span data-stu-id="54a77-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="54a77-115">Lauke Aparatūros profilis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="54a77-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="54a77-116">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="54a77-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="54a77-117">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="54a77-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="54a77-118">Lauke Paketo pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="54a77-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="54a77-119">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="54a77-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="54a77-120">Tai yra standartinis paketas, teikiamas su nauja aplinka.</span><span class="sxs-lookup"><span data-stu-id="54a77-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="54a77-121">Versijos numeris gali skirtis.</span><span class="sxs-lookup"><span data-stu-id="54a77-121">The version number may vary.</span></span>  
11. <span data-ttu-id="54a77-122">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="54a77-122">Click Save.</span></span>
12. <span data-ttu-id="54a77-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="54a77-123">Close the page.</span></span>
13. <span data-ttu-id="54a77-124">Eikite į Mažmeninė prekyba ir prekyba > Kanalai > Visos parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="54a77-124">Go to Retail and Commerce > Channels > All stores.</span></span>
14. <span data-ttu-id="54a77-125">Sąraše pasirinkite 17 eilutę.</span><span class="sxs-lookup"><span data-stu-id="54a77-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="54a77-126">Jei naudojate demonstracinių duomenų įmonę USRT, tai yra „Houston“ parduotuvė.</span><span class="sxs-lookup"><span data-stu-id="54a77-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="54a77-127">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="54a77-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="54a77-128">Perjunkite sekcijos Aparatūros stotys išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="54a77-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="54a77-129">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="54a77-129">Click Add.</span></span>
18. <span data-ttu-id="54a77-130">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="54a77-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="54a77-131">Lauke Šablono ID spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="54a77-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="54a77-132">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="54a77-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="54a77-133">Tai turi būti naujas aparatūros stoties šablonas, sukurtas atliekant ankstesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="54a77-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="54a77-134">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="54a77-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="54a77-135">Lauke Pagrindinio kompiuterio vardas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54a77-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="54a77-136">Lauke EFT terminalo ID įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54a77-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="54a77-137">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="54a77-137">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]