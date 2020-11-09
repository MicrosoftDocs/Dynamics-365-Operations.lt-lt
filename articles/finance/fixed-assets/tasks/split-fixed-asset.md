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
ms.openlocfilehash: 40703622bc8c7a21451d31e7606596c5edbe90f7
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000298"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="5292f-103">Ilgalaikio turto skaidymas</span><span class="sxs-lookup"><span data-stu-id="5292f-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5292f-104">Šioje temoje paaiškinta, kaip vienos turto knygos procentinę dalį padalinti naujai turto knygai.</span><span class="sxs-lookup"><span data-stu-id="5292f-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="5292f-105">Jis naudoja vaidmenį Buhalteris ir USMF demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="5292f-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="5292f-106">Kurti naują ilgalaikį turtą</span><span class="sxs-lookup"><span data-stu-id="5292f-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="5292f-107">Naršymo srityje eikite į **Moduliai \> Ilgalaikis turtas \> Ilgalaikis turtas \> Ilgalaikis turtas**.</span><span class="sxs-lookup"><span data-stu-id="5292f-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="5292f-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="5292f-108">Select **New**.</span></span>
3. <span data-ttu-id="5292f-109">Lauke **Ilgalaikio turto grupė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5292f-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="5292f-110">Pasižymėkite ilgalaikio turto numerį, kuris bus vėliau naudojamas skaidymo procese.</span><span class="sxs-lookup"><span data-stu-id="5292f-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="5292f-111">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5292f-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="5292f-112">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="5292f-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="5292f-113">Ilgalaikio turto skaidymas</span><span class="sxs-lookup"><span data-stu-id="5292f-113">Split a fixed asset</span></span>

<span data-ttu-id="5292f-114">Prieš suskaidant visiškai nusidėvusį turtą, turto knygos būseną reikia rankiniu būdu pakeisti iš **Uždaryta** į **Atidaryta**.</span><span class="sxs-lookup"><span data-stu-id="5292f-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="5292f-115">Šis veiksmas būtinas, nes knygos būsena turi būti **Atidaryta** , jei turite užregistruoti turto operacijas (pvz., likvidavimo pardavimo).</span><span class="sxs-lookup"><span data-stu-id="5292f-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="5292f-116">Pakeitę turto knygos būseną, atlikite toliau pateiktus veiksmus, norėdami skaidyti turtą.</span><span class="sxs-lookup"><span data-stu-id="5292f-116">After the asset book status is changed, follow these steps to split the asset.</span></span>

1. <span data-ttu-id="5292f-117">Sąraše raskite ir pasirinkite ilgalaikio turto, kurį norite skaidyti, nuorodą.</span><span class="sxs-lookup"><span data-stu-id="5292f-117">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="5292f-118">Pasirinkite **Knygos**.</span><span class="sxs-lookup"><span data-stu-id="5292f-118">Select **Books**.</span></span> <span data-ttu-id="5292f-119">Pasirinkite, kurią knygą padalinti naujajam turtui.</span><span class="sxs-lookup"><span data-stu-id="5292f-119">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="5292f-120">Pasirinkite **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="5292f-120">Select **Functions**.</span></span>
4. <span data-ttu-id="5292f-121">Pasirinkite **Skaidyti ilgalaikį turtą**.</span><span class="sxs-lookup"><span data-stu-id="5292f-121">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="5292f-122">Lauke **Į ilgalaikį turtą** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5292f-122">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="5292f-123">Lauke **Į knygą** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="5292f-123">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="5292f-124">Lauke **Operacijos data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="5292f-124">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="5292f-125">Lauke **Procentas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="5292f-125">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="5292f-126">Lauke **Žurnalo pavadinimas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5292f-126">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="5292f-127">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5292f-127">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="5292f-128">Registruoti žurnalo operaciją</span><span class="sxs-lookup"><span data-stu-id="5292f-128">Post the journal transaction</span></span>

1. <span data-ttu-id="5292f-129">Naršymo srityje eikite į **Moduliai \> Ilgalaikis turtas \> Žurnalo įrašai \> Ilgalaikio turto žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="5292f-129">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="5292f-130">Sąraše pasirinkite žurnalą, sukurtą skaidymo procesu.</span><span class="sxs-lookup"><span data-stu-id="5292f-130">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="5292f-131">Pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="5292f-131">Select **Lines**.</span></span>

    - <span data-ttu-id="5292f-132">Patikrinkite sukurtas žurnalo eilutes.</span><span class="sxs-lookup"><span data-stu-id="5292f-132">Verify the journal lines created.</span></span>
    - <span data-ttu-id="5292f-133">Sukuriama pradinio turto įsigijimo koregavimo operacija, kad būtų galima sumažinti reikšmę procentine dalimi, nurodyta skaidymo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="5292f-133">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="5292f-134">Sukuriama tos pačios sumos naujojo turto įsigijimo operacija.</span><span class="sxs-lookup"><span data-stu-id="5292f-134">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="5292f-135">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="5292f-135">Select **Post**.</span></span>
