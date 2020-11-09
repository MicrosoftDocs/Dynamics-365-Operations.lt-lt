---
title: Registruoti prekės, kurios pagrindinio sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą
description: Ši procedūra nurodo, kaip reikia užregistruoti elementus naudojant prekių gavimo žurnalą, kai atsargų valdymo modulyje naudojate „pagrindinį sandėliavimą“.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 940fa33b10c5f60f469187b11dd066091581996f
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018473"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a><span data-ttu-id="aaedd-103">Registruoti prekės, kurios pagrindinio sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą</span><span class="sxs-lookup"><span data-stu-id="aaedd-103">Register items for a basic warehousing enabled item using an item an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aaedd-104">Ši procedūra nurodo, kaip reikia užregistruoti elementus naudojant prekių gavimo žurnalą, kai atsargų valdymo modulyje naudojate „pagrindinį sandėliavimą“.</span><span class="sxs-lookup"><span data-stu-id="aaedd-104">This procedure shows you how to register items using the item arrival journal when you are using "basic warehousing" in the Inventory management module.</span></span> <span data-ttu-id="aaedd-105">Paprastai tai atlieka gavimo klerkas.</span><span class="sxs-lookup"><span data-stu-id="aaedd-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="aaedd-106">Galite vykdyti šią procedūrą demonstracinių duomenų įmonėje USMF, naudodami rodomas pavyzdines reikšmes.</span><span class="sxs-lookup"><span data-stu-id="aaedd-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="aaedd-107">Jei nenaudojate USMF, prieš pradėdami šį vadovą turite turėti patvirtintą pirkimo užsakymą su atidaryta pirkimo užsakymo eilute.</span><span class="sxs-lookup"><span data-stu-id="aaedd-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="aaedd-108">Prekė eilutėje turi būti laikoma atsargose.</span><span class="sxs-lookup"><span data-stu-id="aaedd-108">The item on the line must be stocked.</span></span> <span data-ttu-id="aaedd-109">Taip pat prekės turi būti susietos su saugojimo dimensijų grupe, kurioje aktyvūs teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="aaedd-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="aaedd-110">Kurti prekių gavimo žurnalo antraštę</span><span class="sxs-lookup"><span data-stu-id="aaedd-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="aaedd-111">Pasirinkite Atsargų valdymas > Žurnalo įrašai > Prekių gavimas > Prekių gavimas.</span><span class="sxs-lookup"><span data-stu-id="aaedd-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="aaedd-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="aaedd-112">Click New.</span></span>
3. <span data-ttu-id="aaedd-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aaedd-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="aaedd-114">Jei naudojate USMF, galite surinkti WHS.</span><span class="sxs-lookup"><span data-stu-id="aaedd-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="aaedd-115">Jei naudojate kitus duomenis, žurnalas, kurio pavadinimą pasirinksite, turi turėti šias savybes: patikros rinkimo vieta turi būti nustatyta į „Ne“ ir karantino valdymas turi būti nustatytas į „Ne“.</span><span class="sxs-lookup"><span data-stu-id="aaedd-115">If you're using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="aaedd-116">Lauke Važtaraštis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aaedd-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="aaedd-117">Tai yra važtaraščio ID iš tiekėjo išduoto važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="aaedd-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="aaedd-118">Pridėkite unikalų numerį.</span><span class="sxs-lookup"><span data-stu-id="aaedd-118">Add a unique number.</span></span>  
5. <span data-ttu-id="aaedd-119">Lauke Numeris pasirinkite pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="aaedd-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="aaedd-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="aaedd-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="aaedd-121">Į prekių gavimo žurnalą pridėti eilučių</span><span class="sxs-lookup"><span data-stu-id="aaedd-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="aaedd-122">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="aaedd-122">Click Functions.</span></span>
2. <span data-ttu-id="aaedd-123">Spustelėkite Kurti eilutes.</span><span class="sxs-lookup"><span data-stu-id="aaedd-123">Click Create lines.</span></span>
    * <span data-ttu-id="aaedd-124">Į šį žurnalą eilutes galima įvesti rankiniu būdu arba sukurti automatiškai.</span><span class="sxs-lookup"><span data-stu-id="aaedd-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="aaedd-125">Bus parodyta, kaip sukurti automatiškai.</span><span class="sxs-lookup"><span data-stu-id="aaedd-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="aaedd-126">Pažymėkite arba atžymėkite žymės langelį Inicijuoti kiekį.</span><span class="sxs-lookup"><span data-stu-id="aaedd-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="aaedd-127">Kiekis žurnalo eilutėse bus inicijuojamas su kiekiu, neužregistruotu pirkimo užsakymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="aaedd-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="aaedd-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="aaedd-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="aaedd-129">Registruoti žurnalą</span><span class="sxs-lookup"><span data-stu-id="aaedd-129">Post the journal</span></span>
1. <span data-ttu-id="aaedd-130">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="aaedd-130">Click Post.</span></span>
2. <span data-ttu-id="aaedd-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="aaedd-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="aaedd-132">Generuoti produkto gavimo kvitą</span><span class="sxs-lookup"><span data-stu-id="aaedd-132">Generate the product receipt</span></span>
1. <span data-ttu-id="aaedd-133">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="aaedd-133">Click Functions.</span></span>
2. <span data-ttu-id="aaedd-134">Spustelėkite Produkto gavimo kvitas.</span><span class="sxs-lookup"><span data-stu-id="aaedd-134">Click Product receipt.</span></span>
3. <span data-ttu-id="aaedd-135">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="aaedd-135">Click OK.</span></span>

