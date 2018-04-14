--- 
title: "Registruoti prekės, kurios pagrindinė sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą"
description: "Ši procedūra jums parodo, kaip registruoti prekes, naudojant prekių gavimo žurnalą, kai modulyje Atsargų valdymas naudojate „pagrindinį sandėliavimą‟."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ab824bd99347cbd090e99435217f9ce8ae992b3d
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="239e6-103">Registruoti prekės, kurios pagrindinė sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą</span><span class="sxs-lookup"><span data-stu-id="239e6-103">Register items for a basic warehousing enabled item using an item arrival journal</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="239e6-104">Ši procedūra jums parodo, kaip registruoti prekes, naudojant prekių gavimo žurnalą, kai modulyje Atsargų valdymas naudojate „pagrindinį sandėliavimą‟.</span><span class="sxs-lookup"><span data-stu-id="239e6-104">This procedure shows you how to register items using the item arrival journal when you are using “basic warehousing” in the Inventory management module.</span></span> <span data-ttu-id="239e6-105">Paprastai tai atlieka gavimo klerkas.</span><span class="sxs-lookup"><span data-stu-id="239e6-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="239e6-106">Galite vykdyti šią procedūrą demonstracinių duomenų įmonėje USMF, naudodami rodomas pavyzdines reikšmes.</span><span class="sxs-lookup"><span data-stu-id="239e6-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="239e6-107">Jei nenaudojate USMF, prieš pradėdami šį vadovą turite turėti patvirtintą pirkimo užsakymą su atidaryta pirkimo užsakymo eilute.</span><span class="sxs-lookup"><span data-stu-id="239e6-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="239e6-108">Prekė eilutėje turi būti laikoma atsargose, nenaudoti produktų variantų ir neturėti sekimo dimensijų.</span><span class="sxs-lookup"><span data-stu-id="239e6-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="239e6-109">Taip pat prekės turi būti susietos su saugojimo dimensijų grupe, kurioje aktyvūs teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="239e6-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="239e6-110">Kurti prekių gavimo žurnalo antraštę</span><span class="sxs-lookup"><span data-stu-id="239e6-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="239e6-111">Pasirinkite Atsargų valdymas > Žurnalo įrašai > Prekių gavimas > Prekių gavimas.</span><span class="sxs-lookup"><span data-stu-id="239e6-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="239e6-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="239e6-112">Click New.</span></span>
3. <span data-ttu-id="239e6-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="239e6-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="239e6-114">Jei naudojate USMF, galite surinkti WHS.</span><span class="sxs-lookup"><span data-stu-id="239e6-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="239e6-115">Jei naudojate kitus duomenis, žurnalas, kurio pavadinimą pasirinkote, turi turėti toliau nurodytas ypatybes: tikrinti paėmimo vietą turi būti nustatyta į Ne ir Sulaikymo valdymas turi būti nustatyta į Ne.</span><span class="sxs-lookup"><span data-stu-id="239e6-115">If you’re using other data, the journal whose name you choose has to have the following properties: check picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="239e6-116">Lauke Važtaraštis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="239e6-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="239e6-117">Tai yra važtaraščio ID iš tiekėjo išduoto važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="239e6-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="239e6-118">Pridėkite unikalų numerį.</span><span class="sxs-lookup"><span data-stu-id="239e6-118">Add a unique number.</span></span>  
5. <span data-ttu-id="239e6-119">Lauke Numeris pasirinkite pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="239e6-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="239e6-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="239e6-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="239e6-121">Į prekių gavimo žurnalą pridėti eilučių</span><span class="sxs-lookup"><span data-stu-id="239e6-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="239e6-122">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="239e6-122">Click Functions.</span></span>
2. <span data-ttu-id="239e6-123">Spustelėkite Kurti eilutes.</span><span class="sxs-lookup"><span data-stu-id="239e6-123">Click Create lines.</span></span>
    * <span data-ttu-id="239e6-124">Į šį žurnalą eilutes galima įvesti rankiniu būdu arba sukurti automatiškai.</span><span class="sxs-lookup"><span data-stu-id="239e6-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="239e6-125">Bus parodyta, kaip sukurti automatiškai.</span><span class="sxs-lookup"><span data-stu-id="239e6-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="239e6-126">Pažymėkite arba atžymėkite žymės langelį Inicijuoti kiekį.</span><span class="sxs-lookup"><span data-stu-id="239e6-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="239e6-127">Kiekis žurnalo eilutėse bus inicijuojamas su kiekiu, neužregistruotu pirkimo užsakymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="239e6-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="239e6-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="239e6-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="239e6-129">Registruoti žurnalą</span><span class="sxs-lookup"><span data-stu-id="239e6-129">Post the journal</span></span>
1. <span data-ttu-id="239e6-130">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="239e6-130">Click Post.</span></span>
2. <span data-ttu-id="239e6-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="239e6-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="239e6-132">Generuoti produkto gavimo kvitą</span><span class="sxs-lookup"><span data-stu-id="239e6-132">Generate the product receipt</span></span>
1. <span data-ttu-id="239e6-133">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="239e6-133">Click Functions.</span></span>
2. <span data-ttu-id="239e6-134">Spustelėkite Produkto gavimo kvitas.</span><span class="sxs-lookup"><span data-stu-id="239e6-134">Click Product receipt.</span></span>
3. <span data-ttu-id="239e6-135">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="239e6-135">Click OK.</span></span>


