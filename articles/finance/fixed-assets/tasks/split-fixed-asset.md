---
title: Ilgalaikio turto skaidymas
description: Šioje temoje paaiškinta, kaip vienos turto knygos procentinę dalį padalinti naujai turto knygai.
author: saraschi2
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa21d5698275ff691ca83d29abd297a796b652d1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823913"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="328df-103">Ilgalaikio turto skaidymas</span><span class="sxs-lookup"><span data-stu-id="328df-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="328df-104">Šioje temoje paaiškinta, kaip vienos turto knygos procentinę dalį padalinti naujai turto knygai.</span><span class="sxs-lookup"><span data-stu-id="328df-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="328df-105">Jis naudoja vaidmenį Buhalteris ir USMF demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="328df-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="328df-106">Kurti naują ilgalaikį turtą</span><span class="sxs-lookup"><span data-stu-id="328df-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="328df-107">Naršymo srityje eikite į **Moduliai \> Ilgalaikis turtas \> Ilgalaikis turtas \> Ilgalaikis turtas**.</span><span class="sxs-lookup"><span data-stu-id="328df-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="328df-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="328df-108">Select **New**.</span></span>
3. <span data-ttu-id="328df-109">Lauke **Ilgalaikio turto grupė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="328df-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="328df-110">Pasižymėkite ilgalaikio turto numerį, kuris bus vėliau naudojamas skaidymo procese.</span><span class="sxs-lookup"><span data-stu-id="328df-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="328df-111">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="328df-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="328df-112">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="328df-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="328df-113">Ilgalaikio turto skaidymas</span><span class="sxs-lookup"><span data-stu-id="328df-113">Split a fixed asset</span></span>

<span data-ttu-id="328df-114">Prieš suskaidant visiškai nusidėvusį turtą, turto knygos būseną reikia rankiniu būdu pakeisti iš **Uždaryta** į **Atidaryta**.</span><span class="sxs-lookup"><span data-stu-id="328df-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="328df-115">Šis veiksmas būtinas, nes knygos būsena turi būti **Atidaryta**, jei turite užregistruoti turto operacijas (pvz., likvidavimo pardavimo).</span><span class="sxs-lookup"><span data-stu-id="328df-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="328df-116">Taip pat turite įjungti parametrą **Leisti kelias operacijas viename kvite**, kuris yra puslapio **DK parametrai** skirtuke **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="328df-116">You must also turn on the **Allow multiple transactions within one voucher** parameter on the **General** tab of the **General ledger parameters** page.</span></span> <span data-ttu-id="328df-117">Kai pasikeičia turto knygos būsena ir viename kvite leidžiamos kelios operacijos, atlikite šiuos veiksmus, kad padalytumėte turtą.</span><span class="sxs-lookup"><span data-stu-id="328df-117">After the asset book status is changed and multiple transactions within one voucher have been allowed, complete the following steps to split the asset.</span></span>

1. <span data-ttu-id="328df-118">Sąraše raskite ir pasirinkite ilgalaikio turto, kurį norite skaidyti, nuorodą.</span><span class="sxs-lookup"><span data-stu-id="328df-118">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="328df-119">Pasirinkite **Knygos**.</span><span class="sxs-lookup"><span data-stu-id="328df-119">Select **Books**.</span></span> <span data-ttu-id="328df-120">Pasirinkite, kurią knygą padalinti naujajam turtui.</span><span class="sxs-lookup"><span data-stu-id="328df-120">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="328df-121">Pasirinkite **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="328df-121">Select **Functions**.</span></span>
4. <span data-ttu-id="328df-122">Pasirinkite **Skaidyti ilgalaikį turtą**.</span><span class="sxs-lookup"><span data-stu-id="328df-122">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="328df-123">Lauke **Į ilgalaikį turtą** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="328df-123">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="328df-124">Lauke **Į knygą** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="328df-124">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="328df-125">Lauke **Operacijos data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="328df-125">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="328df-126">Lauke **Procentas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="328df-126">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="328df-127">Lauke **Žurnalo pavadinimas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="328df-127">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="328df-128">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="328df-128">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="328df-129">Registruoti žurnalo operaciją</span><span class="sxs-lookup"><span data-stu-id="328df-129">Post the journal transaction</span></span>

1. <span data-ttu-id="328df-130">Naršymo srityje eikite į **Moduliai \> Ilgalaikis turtas \> Žurnalo įrašai \> Ilgalaikio turto žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="328df-130">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="328df-131">Sąraše pasirinkite žurnalą, sukurtą skaidymo procesu.</span><span class="sxs-lookup"><span data-stu-id="328df-131">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="328df-132">Pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="328df-132">Select **Lines**.</span></span>

    - <span data-ttu-id="328df-133">Patikrinkite sukurtas žurnalo eilutes.</span><span class="sxs-lookup"><span data-stu-id="328df-133">Verify the journal lines created.</span></span>
    - <span data-ttu-id="328df-134">Sukuriama pradinio turto įsigijimo koregavimo operacija, kad būtų galima sumažinti reikšmę procentine dalimi, nurodyta skaidymo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="328df-134">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="328df-135">Sukuriama tos pačios sumos naujojo turto įsigijimo operacija.</span><span class="sxs-lookup"><span data-stu-id="328df-135">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="328df-136">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="328df-136">Select **Post**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]