---
title: Nustatyti įsigijimo kategorijų hierarchiją
description: Ši procedūra nurodo, kaip sukurti naujų mazgų įsigijimo kategorijų hierarchijoje ir kaip konfigūruoti įsigijimo kategoriją, kuri bus naudojama įsigijimo procese.
author: mkirknel
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eaab2093eb2531b63f27717d828f7064a8f9ed1d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207513"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="29431-103">Nustatyti įsigijimo kategorijų hierarchiją</span><span class="sxs-lookup"><span data-stu-id="29431-103">Set up a procurement category hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="29431-104">Ši procedūra nurodo, kaip sukurti naujų mazgų įsigijimo kategorijų hierarchijoje ir kaip konfigūruoti įsigijimo kategoriją, kuri bus naudojama įsigijimo procese.</span><span class="sxs-lookup"><span data-stu-id="29431-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="29431-105">Šias užduotis paprastai atlieka pirkimo vadybininkas.</span><span class="sxs-lookup"><span data-stu-id="29431-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="29431-106">Šią procedūrą galėsite pradėti tik esant įsigijimo tipo kategorijų hierarchijai.</span><span class="sxs-lookup"><span data-stu-id="29431-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="29431-107">Jei naudojate demonstracinių duomenų įmonę, šią procedūrą galite vykdyti su USMF įmonėje.</span><span class="sxs-lookup"><span data-stu-id="29431-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="29431-108">Įtraukiti naują įsigijimo kategoriją</span><span class="sxs-lookup"><span data-stu-id="29431-108">Add a new procurement category</span></span>
1. <span data-ttu-id="29431-109">Eikite į **Naršymo sritis > Moduliai > Įsigijimas ir šaltiniai > Konsignacija > Įsigijimo kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="29431-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="29431-110">Veiksmų srityje pasirinkite **Redaguoti kategorijų hierarchiją**.</span><span class="sxs-lookup"><span data-stu-id="29431-110">On the action pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="29431-111">Kairiojoje puslapio pusėje rodoma dabartinė įsigijimo kategorijų hierarchija.</span><span class="sxs-lookup"><span data-stu-id="29431-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="29431-112">Ketinate pakeisti hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="29431-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="29431-113">Veiksmų srityje pasirinkite **Naujas kategorijos mazgas**.</span><span class="sxs-lookup"><span data-stu-id="29431-113">On the action pane, select **New category node**.</span></span> <span data-ttu-id="29431-114">Sistema pasirenka viršutinį mazgą pagal numatytuosius nustatymus.</span><span class="sxs-lookup"><span data-stu-id="29431-114">The system selects the top node by default.</span></span> <span data-ttu-id="29431-115">Jei vykdote šią procedūrą kaip užduoties vadovą, galite spustelėti mygtuką „Atrakinti“ ir pasirinkti kitą pirminį mazgą, į kurį galėsite įterpti savo naująjį mazgą.</span><span class="sxs-lookup"><span data-stu-id="29431-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="29431-116">Tai atlikę, vėl užrakinkite užduoties vadovą, o tada spustelėkite „Nauja kategorijos mazgas“.</span><span class="sxs-lookup"><span data-stu-id="29431-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="29431-117">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="29431-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="29431-118">Lauke **Aprašo laukas**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="29431-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="29431-119">Lauke **Patogus pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="29431-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="29431-120">Pasirinktinai galite įvesti patogų pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="29431-120">The friendly name is optional.</span></span> <span data-ttu-id="29431-121">Jis bus rodomas kategorijos peržvalgose kartu su kategorijos pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="29431-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="29431-122">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="29431-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="29431-123">Įtraukti produktus į naują įsigijimo kategoriją</span><span class="sxs-lookup"><span data-stu-id="29431-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="29431-124">Eikite į **Įsigijimas ir šaltiniai > Konsignacija > Įsigijimo kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="29431-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="29431-125">Pasirinkite mazgą, kurį ką tik pridėjote.</span><span class="sxs-lookup"><span data-stu-id="29431-125">Select the node you just added.</span></span> <span data-ttu-id="29431-126">Jei vykdote šią procedūrą kaip užduoties vadovą, gali reikėti atrakinti užduoties vadovą, kad pasirinktumėte mazgą.</span><span class="sxs-lookup"><span data-stu-id="29431-126">If you're running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="29431-127">Perjunkite skyriaus **Produktai** išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="29431-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="29431-128">Spustelėkite **Įtraukti**, kad susietumėte produktus su įsigijimo kategorija.</span><span class="sxs-lookup"><span data-stu-id="29431-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="29431-129">Pasirinkite produktus, kuriuos norite įtraukti į įsigijimo kategoriją.</span><span class="sxs-lookup"><span data-stu-id="29431-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="29431-130">Pasirinkę rodyklę, įtraukite produktus į lentelę **Pasirinkta**.</span><span class="sxs-lookup"><span data-stu-id="29431-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="29431-131">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="29431-131">Select **OK**.</span></span>
