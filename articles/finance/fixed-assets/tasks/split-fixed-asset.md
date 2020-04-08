---
title: Ilgalaikio turto skaidymas
description: Šioje temoje paaiškinta, kaip vienos turto knygos procentinę dalį padalinti naujai turto knygai.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85ccf187e77faf338ac29452d823c3652b806a21
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138120"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="02910-103">Ilgalaikio turto skaidymas</span><span class="sxs-lookup"><span data-stu-id="02910-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02910-104">Šioje temoje paaiškinta, kaip vienos turto knygos procentinę dalį padalinti naujai turto knygai.</span><span class="sxs-lookup"><span data-stu-id="02910-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="02910-105">Jis naudoja vaidmenį Buhalteris ir USMF demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="02910-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="02910-106">Kurti naują ilgalaikį turtą</span><span class="sxs-lookup"><span data-stu-id="02910-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="02910-107">Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Ilgalaikis turtas > Ilgalaikis turtas**.</span><span class="sxs-lookup"><span data-stu-id="02910-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="02910-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="02910-108">Select **New**.</span></span>
3. <span data-ttu-id="02910-109">Lauke **Ilgalaikio turto grupė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="02910-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="02910-110">Pasižymėkite ilgalaikio turto numerį, kuris bus vėliau naudojamas skaidymo procese.</span><span class="sxs-lookup"><span data-stu-id="02910-110">Note the fixed asset number to use in the split process later.</span></span>  
4. <span data-ttu-id="02910-111">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="02910-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="02910-112">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="02910-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="02910-113">Ilgalaikio turto skaidymas</span><span class="sxs-lookup"><span data-stu-id="02910-113">Split a fixed asset</span></span>
1. <span data-ttu-id="02910-114">Sąraše raskite ir pasirinkite ilgalaikio turto, kurį norite skaidyti, nuorodą.</span><span class="sxs-lookup"><span data-stu-id="02910-114">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="02910-115">Pasirinkite **Knygos**.</span><span class="sxs-lookup"><span data-stu-id="02910-115">Select **Books**.</span></span> <span data-ttu-id="02910-116">Pasirinkite, kurią knygą padalinti naujajam turtui.</span><span class="sxs-lookup"><span data-stu-id="02910-116">Select the book to split to the new asset.</span></span>  
3. <span data-ttu-id="02910-117">Pasirinkite **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="02910-117">Select **Functions**.</span></span>
4. <span data-ttu-id="02910-118">Pasirinkite **Skaidyti ilgalaikį turtą**.</span><span class="sxs-lookup"><span data-stu-id="02910-118">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="02910-119">Lauke **Į ilgalaikį turtą** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="02910-119">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="02910-120">Lauke **Į knygą** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="02910-120">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="02910-121">Lauke **Operacijos data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="02910-121">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="02910-122">Lauke **Procentas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="02910-122">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="02910-123">Lauke **Žurnalo pavadinimas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="02910-123">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="02910-124">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="02910-124">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="02910-125">Registruoti žurnalo operaciją</span><span class="sxs-lookup"><span data-stu-id="02910-125">Post the journal transaction</span></span>
1. <span data-ttu-id="02910-126">Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Žurnalo įrašai > Ilgalaikio turto žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="02910-126">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="02910-127">Sąraše pasirinkite žurnalą, sukurtą skaidymo procesu.</span><span class="sxs-lookup"><span data-stu-id="02910-127">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="02910-128">Pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="02910-128">Select **Lines**.</span></span>

    - <span data-ttu-id="02910-129">Patikrinkite sukurtas žurnalo eilutes.</span><span class="sxs-lookup"><span data-stu-id="02910-129">Verify the journal lines created.</span></span>  
    - <span data-ttu-id="02910-130">Sukuriama pradinio turto įsigijimo koregavimo operacija, kad būtų galima sumažinti reikšmę procentine dalimi, nurodyta skaidymo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="02910-130">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  
    - <span data-ttu-id="02910-131">Sukuriama tos pačios sumos naujojo turto įsigijimo operacija.</span><span class="sxs-lookup"><span data-stu-id="02910-131">An Acquisition transaction is created for the new asset for the same amount.</span></span>  

4. <span data-ttu-id="02910-132">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="02910-132">Select **Post**.</span></span>

