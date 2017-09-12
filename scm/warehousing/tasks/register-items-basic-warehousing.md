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
ms.sourcegitcommit: a5fa86bace459d694ab0a2ec289e11b0e4420932
ms.openlocfilehash: 184f38347e2525f3efef9b0d55003a94a75380d4
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="b69d1-103">Registruoti prekės, kurios pagrindinė sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą</span><span class="sxs-lookup"><span data-stu-id="b69d1-103">Register items for a basic warehousing enabled item using an item arrival journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b69d1-104">Ši procedūra jums parodo, kaip registruoti prekes, naudojant prekių gavimo žurnalą, kai modulyje Atsargų valdymas naudojate „pagrindinį sandėliavimą‟.</span><span class="sxs-lookup"><span data-stu-id="b69d1-104">This procedure shows you how to register items using the item arrival journal when you are using “basic warehousing” in the Inventory management module.</span></span> <span data-ttu-id="b69d1-105">Paprastai tai atlieka gavimo klerkas.</span><span class="sxs-lookup"><span data-stu-id="b69d1-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="b69d1-106">Galite vykdyti šią procedūrą demonstracinių duomenų įmonėje USMF, naudodami rodomas pavyzdines reikšmes.</span><span class="sxs-lookup"><span data-stu-id="b69d1-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="b69d1-107">Jei nenaudojate USMF, prieš pradėdami šį vadovą turite turėti patvirtintą pirkimo užsakymą su atidaryta pirkimo užsakymo eilute.</span><span class="sxs-lookup"><span data-stu-id="b69d1-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="b69d1-108">Prekė eilutėje turi būti laikoma atsargose, nenaudoti produktų variantų ir neturėti sekimo dimensijų.</span><span class="sxs-lookup"><span data-stu-id="b69d1-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="b69d1-109">Taip pat prekės turi būti susietos su saugojimo dimensijų grupe, kurioje aktyvūs teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="b69d1-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="b69d1-110">Kurti prekių gavimo žurnalo antraštę</span><span class="sxs-lookup"><span data-stu-id="b69d1-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="b69d1-111">Pasirinkite Atsargų valdymas > Žurnalo įrašai > Prekių gavimas > Prekių gavimas.</span><span class="sxs-lookup"><span data-stu-id="b69d1-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="b69d1-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b69d1-112">Click New.</span></span>
3. <span data-ttu-id="b69d1-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b69d1-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="b69d1-114">Jei naudojate USMF, galite surinkti WHS.</span><span class="sxs-lookup"><span data-stu-id="b69d1-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="b69d1-115">Jei naudojate kitus duomenis, žurnalas, kurio pavadinimą pasirinkote, turi turėti toliau nurodytas ypatybes: Tikrinti paėmimo vietą turi būti nustatyta į Ne ir Sulaikymo valdymas turi būti nustatyta į Ne.</span><span class="sxs-lookup"><span data-stu-id="b69d1-115">If you’re using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="b69d1-116">Lauke Važtaraštis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b69d1-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="b69d1-117">Tai yra važtaraščio ID iš tiekėjo išduoto važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="b69d1-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="b69d1-118">Pridėkite unikalų numerį.</span><span class="sxs-lookup"><span data-stu-id="b69d1-118">Add a unique number.</span></span>  
5. <span data-ttu-id="b69d1-119">Lauke Numeris pasirinkite pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b69d1-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="b69d1-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b69d1-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="b69d1-121">Į prekių gavimo žurnalą pridėti eilučių</span><span class="sxs-lookup"><span data-stu-id="b69d1-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="b69d1-122">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="b69d1-122">Click Functions.</span></span>
2. <span data-ttu-id="b69d1-123">Spustelėkite Kurti eilutes.</span><span class="sxs-lookup"><span data-stu-id="b69d1-123">Click Create lines.</span></span>
    * <span data-ttu-id="b69d1-124">Į šį žurnalą eilutes galima įvesti rankiniu būdu arba sukurti automatiškai.</span><span class="sxs-lookup"><span data-stu-id="b69d1-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="b69d1-125">Bus parodyta, kaip sukurti automatiškai.</span><span class="sxs-lookup"><span data-stu-id="b69d1-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="b69d1-126">Pažymėkite arba atžymėkite žymės langelį Inicijuoti kiekį.</span><span class="sxs-lookup"><span data-stu-id="b69d1-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="b69d1-127">Kiekis žurnalo eilutėse bus inicijuojamas su kiekiu, neužregistruotu pirkimo užsakymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b69d1-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="b69d1-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b69d1-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="b69d1-129">Registruoti žurnalą</span><span class="sxs-lookup"><span data-stu-id="b69d1-129">Post the journal</span></span>
1. <span data-ttu-id="b69d1-130">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="b69d1-130">Click Post.</span></span>
2. <span data-ttu-id="b69d1-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b69d1-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="b69d1-132">Generuoti produkto gavimo kvitą</span><span class="sxs-lookup"><span data-stu-id="b69d1-132">Generate the product receipt</span></span>
1. <span data-ttu-id="b69d1-133">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="b69d1-133">Click Functions.</span></span>
2. <span data-ttu-id="b69d1-134">Spustelėkite Produkto gavimo kvitas.</span><span class="sxs-lookup"><span data-stu-id="b69d1-134">Click Product receipt.</span></span>
3. <span data-ttu-id="b69d1-135">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b69d1-135">Click OK.</span></span>


