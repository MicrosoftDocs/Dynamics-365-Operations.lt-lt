---
title: Skaidyti ilgalaikį turtą
description: Šis užduočių vadovas išskaidys vienos turto knygos procentinę dalį naujai turto knygai.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6be9de64265a4d7b5c91af3ee8acfce80c78e0f1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566897"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="5848d-103">Skaidyti ilgalaikį turtą</span><span class="sxs-lookup"><span data-stu-id="5848d-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5848d-104">Šis užduočių vadovas išskaidys vienos turto knygos procentinę dalį naujai turto knygai.</span><span class="sxs-lookup"><span data-stu-id="5848d-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="5848d-105">Jis naudoja vaidmenį Buhalteris ir USMF demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="5848d-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="5848d-106">Kurti naują ilgalaikį turtą</span><span class="sxs-lookup"><span data-stu-id="5848d-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="5848d-107">Eikite į dalį Ilgalaikis turtas > Ilgalaikis turtas > Ilgalaikis turtas.</span><span class="sxs-lookup"><span data-stu-id="5848d-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="5848d-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="5848d-108">Click New.</span></span>
3. <span data-ttu-id="5848d-109">Lauke Ilgalaikio turto grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5848d-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="5848d-110">Pasižymėkite ilgalaikio turto numerį, kuris bus vėliau naudojamas skaidymo procese.</span><span class="sxs-lookup"><span data-stu-id="5848d-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="5848d-111">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5848d-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="5848d-112">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="5848d-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="5848d-113">Skaidyti ilgalaikį turtą</span><span class="sxs-lookup"><span data-stu-id="5848d-113">Split a fixed asset</span></span>
1. <span data-ttu-id="5848d-114">Sąraše raskite ir pasirinkite skaidytiną ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="5848d-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="5848d-115">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="5848d-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="5848d-116">Spustelėkite Knygos.</span><span class="sxs-lookup"><span data-stu-id="5848d-116">Click Books.</span></span>
    * <span data-ttu-id="5848d-117">Pasirinkite, kurią knygą padalinti naujajam turtui.</span><span class="sxs-lookup"><span data-stu-id="5848d-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="5848d-118">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="5848d-118">Click Functions.</span></span>
5. <span data-ttu-id="5848d-119">Spustelėkite Skaidyti ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="5848d-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="5848d-120">Lauke Į ilgalaikį turtą įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5848d-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="5848d-121">Lauke Į knygą spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="5848d-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="5848d-122">Lauke Operacijos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="5848d-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="5848d-123">Lauke Procentas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="5848d-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="5848d-124">Lauke Žurnalo pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5848d-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="5848d-125">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="5848d-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="5848d-126">Registruoti žurnalo operaciją</span><span class="sxs-lookup"><span data-stu-id="5848d-126">Post the journal transaction</span></span>
1. <span data-ttu-id="5848d-127">Eikite į Ilgalaikis turtas > Žurnalo įrašai > Ilgalaikio turto žurnalas.</span><span class="sxs-lookup"><span data-stu-id="5848d-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="5848d-128">Sąraše pasirinkite žurnalą, sukurtą skaidymo procesu.</span><span class="sxs-lookup"><span data-stu-id="5848d-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="5848d-129">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="5848d-129">Click Lines.</span></span>
    * <span data-ttu-id="5848d-130">Patikrinkite sukurtas žurnalo eilutes.</span><span class="sxs-lookup"><span data-stu-id="5848d-130">Verify the journal lines created.</span></span>  <span data-ttu-id="5848d-131">Sukuriama pradinio turto įsigijimo koregavimo operacija, kad būtų galima sumažinti reikšmę procentine dalimi, nurodyta skaidymo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="5848d-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="5848d-132">Sukuriama tos pačios sumos naujojo turto įsigijimo operacija.</span><span class="sxs-lookup"><span data-stu-id="5848d-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="5848d-133">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="5848d-133">Click Post.</span></span>

