--- 
title: "Skaidyti ilgalaikį turtą"
description: "Šis užduočių vadovas išskaidys vienos turto knygos procentinę dalį naujai turto knygai."
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b4c1b39bcae1fa3830f3a217d1ad89e84cd72134
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="5328b-103">Skaidyti ilgalaikį turtą</span><span class="sxs-lookup"><span data-stu-id="5328b-103">Split a fixed asset</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5328b-104">Šis užduočių vadovas išskaidys vienos turto knygos procentinę dalį naujai turto knygai.</span><span class="sxs-lookup"><span data-stu-id="5328b-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="5328b-105">Jis naudoja vaidmenį Buhalteris ir USMF demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="5328b-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="5328b-106">Kurti naują ilgalaikį turtą</span><span class="sxs-lookup"><span data-stu-id="5328b-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="5328b-107">Eikite į dalį Ilgalaikis turtas > Ilgalaikis turtas > Ilgalaikis turtas.</span><span class="sxs-lookup"><span data-stu-id="5328b-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="5328b-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="5328b-108">Click New.</span></span>
3. <span data-ttu-id="5328b-109">Lauke Ilgalaikio turto grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5328b-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="5328b-110">Pasižymėkite ilgalaikio turto numerį, kuris bus vėliau naudojamas skaidymo procese.</span><span class="sxs-lookup"><span data-stu-id="5328b-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="5328b-111">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5328b-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="5328b-112">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="5328b-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="5328b-113">Skaidyti ilgalaikį turtą</span><span class="sxs-lookup"><span data-stu-id="5328b-113">Split a fixed asset</span></span>
1. <span data-ttu-id="5328b-114">Sąraše raskite ir pasirinkite skaidytiną ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="5328b-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="5328b-115">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="5328b-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="5328b-116">Spustelėkite Knygos.</span><span class="sxs-lookup"><span data-stu-id="5328b-116">Click Books.</span></span>
    * <span data-ttu-id="5328b-117">Pasirinkite, kurią knygą padalinti naujajam turtui.</span><span class="sxs-lookup"><span data-stu-id="5328b-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="5328b-118">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="5328b-118">Click Functions.</span></span>
5. <span data-ttu-id="5328b-119">Spustelėkite Skaidyti ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="5328b-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="5328b-120">Lauke Į ilgalaikį turtą įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5328b-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="5328b-121">Lauke Į knygą spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="5328b-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="5328b-122">Lauke Operacijos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="5328b-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="5328b-123">Lauke Procentas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="5328b-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="5328b-124">Lauke Žurnalo pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5328b-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="5328b-125">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="5328b-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="5328b-126">Registruoti žurnalo operaciją</span><span class="sxs-lookup"><span data-stu-id="5328b-126">Post the journal transaction</span></span>
1. <span data-ttu-id="5328b-127">Eikite į Ilgalaikis turtas > Žurnalo įrašai > Ilgalaikio turto žurnalas.</span><span class="sxs-lookup"><span data-stu-id="5328b-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="5328b-128">Sąraše pasirinkite žurnalą, sukurtą skaidymo procesu.</span><span class="sxs-lookup"><span data-stu-id="5328b-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="5328b-129">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="5328b-129">Click Lines.</span></span>
    * <span data-ttu-id="5328b-130">Patikrinkite sukurtas žurnalo eilutes.</span><span class="sxs-lookup"><span data-stu-id="5328b-130">Verify the journal lines created.</span></span>  <span data-ttu-id="5328b-131">Sukuriama pradinio turto įsigijimo koregavimo operacija, kad būtų galima sumažinti reikšmę procentine dalimi, nurodyta skaidymo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="5328b-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="5328b-132">Sukuriama tos pačios sumos naujojo turto įsigijimo operacija.</span><span class="sxs-lookup"><span data-stu-id="5328b-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="5328b-133">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="5328b-133">Click Post.</span></span>

