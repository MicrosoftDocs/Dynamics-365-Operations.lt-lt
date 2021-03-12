---
title: Pagrindinės išleisto bendrojo produkto sąrankos baigimas
description: Ši procedūra nurodo, kaip atlikti minimalų nustatymą, kurio reikia prieš naudojant bendrąjį produktą KS versijose.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 668b60efa55fa553cf308d5bfc5da7e23f460366
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987034"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="403bc-103">Pagrindinės išleisto bendrojo produkto sąrankos baigimas</span><span class="sxs-lookup"><span data-stu-id="403bc-103">Complete basic setup of a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="403bc-104">Ši procedūra nurodo, kaip atlikti minimalų nustatymą, kurio reikia prieš naudojant bendrąjį produktą KS versijose.</span><span class="sxs-lookup"><span data-stu-id="403bc-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="403bc-105">Tai yra trečioji iš aštuonių procedūrų, kuriomis paaiškinama, kaip kurti konfigūravimo pagal dimensijas kombinacijas.</span><span class="sxs-lookup"><span data-stu-id="403bc-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="403bc-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="403bc-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="403bc-107">Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="403bc-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="403bc-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="403bc-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="403bc-109">Pasirinkite bendrąjį produktą, kurį paleidote antrojoje procedūroje.</span><span class="sxs-lookup"><span data-stu-id="403bc-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="403bc-110">Šis bendrasis produktas sukurtas su konfigūravimo pagal dimensijas technologija.</span><span class="sxs-lookup"><span data-stu-id="403bc-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="403bc-111">Veiksmų srityje spustelėkite **Produktas**.</span><span class="sxs-lookup"><span data-stu-id="403bc-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="403bc-112">Spustelėdami **Dimensijų grupės** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="403bc-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="403bc-113">Lauke **Saugojimo dimensijų grupė** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="403bc-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="403bc-114">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="403bc-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="403bc-115">Saugojimo dimensijų grupė nustato, kurios saugojimo dimensijos bus naudojamos produktų operacijoms.</span><span class="sxs-lookup"><span data-stu-id="403bc-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="403bc-116">Šioje procedūroje pasirinkite **Svetainė**.</span><span class="sxs-lookup"><span data-stu-id="403bc-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="403bc-117">Lauke **Sekimo dimensijų grupė** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="403bc-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="403bc-118">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="403bc-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="403bc-119">Sekimo dimensijų grupė nustato, kurios sekimo dimensijos bus naudojamos produktų operacijoms.</span><span class="sxs-lookup"><span data-stu-id="403bc-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="403bc-120">Šioje procedūroje pasirinkite **Nėra**.</span><span class="sxs-lookup"><span data-stu-id="403bc-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="403bc-121">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="403bc-121">Click **OK**.</span></span>
10. <span data-ttu-id="403bc-122">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="403bc-122">Click **Edit**.</span></span>
11. <span data-ttu-id="403bc-123">Lauke **Prekių modelių grupė** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="403bc-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="403bc-124">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="403bc-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="403bc-125">Prekių modelių grupėse yra nustatymų, kurie nulemia, kaip prekės kontroliuojamos ir tvarkomos jas gaunant ir išduodant.</span><span class="sxs-lookup"><span data-stu-id="403bc-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="403bc-126">Jie taip pat nustato, kaip skaičiuojamas prekių suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="403bc-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="403bc-127">Šioje procedūroje pasirinkite **FIFO**.</span><span class="sxs-lookup"><span data-stu-id="403bc-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="403bc-128">Išplėskite dalį **Valdyti išlaidas**.</span><span class="sxs-lookup"><span data-stu-id="403bc-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="403bc-129">Lauke **Prekių grupė** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="403bc-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="403bc-130">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="403bc-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="403bc-131">Prekių grupės naudojamos atsargoms valdyti dalijant atsargų prekes į grupes.</span><span class="sxs-lookup"><span data-stu-id="403bc-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="403bc-132">Šioje procedūroje pasirinkite **CarAudio**.</span><span class="sxs-lookup"><span data-stu-id="403bc-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="403bc-133">Veiksmų srityje pasirinkite **Planas**.</span><span class="sxs-lookup"><span data-stu-id="403bc-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="403bc-134">Pasirinkite **Numatytieji užsakymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="403bc-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="403bc-135">Dalyje **Numatytojo užsakymo tipo laukas** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="403bc-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="403bc-136">Pasirinkite **Gamyba** nurodydami, kad numatytoji šio bendrojo produkto tiekimo parinktis yra jo gamyba.</span><span class="sxs-lookup"><span data-stu-id="403bc-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="403bc-137">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="403bc-137">Select **Save**.</span></span>
20. <span data-ttu-id="403bc-138">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="403bc-138">Close the page.</span></span>
21. <span data-ttu-id="403bc-139">Uždarykite formą **Išleisto produkto informacija**.</span><span class="sxs-lookup"><span data-stu-id="403bc-139">Close the **Released product details** form.</span></span>

