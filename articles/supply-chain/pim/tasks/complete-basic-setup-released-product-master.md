--- 
title: "Baigti pagrindinį išleisto bendrojo produkto nustatymą"
description: "Ši procedūra nurodo, kaip atlikti minimalų nustatymą, kurio reikia prieš naudojant bendrąjį produktą KS versijose."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 0d3a91977c38c0ce0f9fe114bec943c7cb32a5d4
ms.contentlocale: lt-lt
ms.lasthandoff: 09/14/2018

---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="1f535-103">Baigti pagrindinį išleisto bendrojo produkto nustatymą</span><span class="sxs-lookup"><span data-stu-id="1f535-103">Complete basic setup of a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1f535-104">Ši procedūra nurodo, kaip atlikti minimalų nustatymą, kurio reikia prieš naudojant bendrąjį produktą KS versijose.</span><span class="sxs-lookup"><span data-stu-id="1f535-104">This procedure shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="1f535-105">Tai yra trečioji iš aštuonių procedūrų, kuriomis paaiškinama, kaip kurti konfigūravimo pagal dimensijas kombinacijas.</span><span class="sxs-lookup"><span data-stu-id="1f535-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="1f535-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="1f535-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="1f535-107">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="1f535-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="1f535-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="1f535-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1f535-109">Pasirinkite bendrąjį produktą, kurį paleidote antrojoje procedūroje.</span><span class="sxs-lookup"><span data-stu-id="1f535-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="1f535-110">Šis bendrasis produktas sukurtas su konfigūravimo pagal dimensijas technologija.</span><span class="sxs-lookup"><span data-stu-id="1f535-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="1f535-111">Veiksmų srityje spustelėkite „Produktas“.</span><span class="sxs-lookup"><span data-stu-id="1f535-111">On the Action Pane, click Product.</span></span>
4. <span data-ttu-id="1f535-112">Spustelėdami „Dimensijų grupės“ atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1f535-112">Click Dimension groups to open the drop dialog.</span></span>
5. <span data-ttu-id="1f535-113">Lauke Saugojimo dimensijų grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="1f535-113">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="1f535-114">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="1f535-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1f535-115">Saugojimo dimensijų grupė nustato, kurios saugojimo dimensijos bus naudojamos produktų operacijoms.</span><span class="sxs-lookup"><span data-stu-id="1f535-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="1f535-116">Šioje procedūroje pasirinkite „Svetainė“.</span><span class="sxs-lookup"><span data-stu-id="1f535-116">Select Site for this procedure.</span></span>  
7. <span data-ttu-id="1f535-117">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1f535-117">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="1f535-118">Lauke Sekimo dimensijų grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="1f535-118">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="1f535-119">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="1f535-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1f535-120">Sekimo dimensijų grupė nustato, kurios sekimo dimensijos bus naudojamos produktų operacijoms.</span><span class="sxs-lookup"><span data-stu-id="1f535-120">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="1f535-121">Šioje procedūroje pasirinkite „Nėra“.</span><span class="sxs-lookup"><span data-stu-id="1f535-121">Select None for this procedure.</span></span>  
10. <span data-ttu-id="1f535-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1f535-122">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="1f535-123">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="1f535-123">Click OK.</span></span>
12. <span data-ttu-id="1f535-124">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1f535-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="1f535-125">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="1f535-125">Click Edit.</span></span>
    * <span data-ttu-id="1f535-126">Atidarykite formą „Išleisto produkto informacija“, bus toliau tęsiamas užduoties nustatymas.</span><span class="sxs-lookup"><span data-stu-id="1f535-126">Open the Released product details form to continue the setup task.</span></span>  
14. <span data-ttu-id="1f535-127">Lauke Prekių modelių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="1f535-127">In the Item model group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="1f535-128">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="1f535-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1f535-129">Prekių modelių grupėse yra nustatymų, kurie nulemia, kaip prekės kontroliuojamos ir tvarkomos jas gaunant ir išduodant.</span><span class="sxs-lookup"><span data-stu-id="1f535-129">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="1f535-130">Jie taip pat nustato, kaip skaičiuojamas prekių suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="1f535-130">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="1f535-131">Šioje procedūroje pasirinkite FIFO.</span><span class="sxs-lookup"><span data-stu-id="1f535-131">Select   FIFO for this procedure.</span></span>  
16. <span data-ttu-id="1f535-132">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1f535-132">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="1f535-133">Išplėskite arba sutraukite dalį Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="1f535-133">Expand or collapse the Manage costs section.</span></span>
18. <span data-ttu-id="1f535-134">Lauke Prekių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="1f535-134">In the Item group field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="1f535-135">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="1f535-135">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1f535-136">Prekių grupės naudojamos atsargoms valdyti dalijant atsargų prekes į grupes.</span><span class="sxs-lookup"><span data-stu-id="1f535-136">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="1f535-137">Šioje procedūroje pasirinkite „CarAudio“.</span><span class="sxs-lookup"><span data-stu-id="1f535-137">Select   CarAudio for this procedure.</span></span>  
20. <span data-ttu-id="1f535-138">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1f535-138">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="1f535-139">Veiksmų srityje spustelėkite Planuoti.</span><span class="sxs-lookup"><span data-stu-id="1f535-139">On the Action Pane, click Plan.</span></span>
22. <span data-ttu-id="1f535-140">Spustelėkite Numatytosios užsakymo nuostatos.</span><span class="sxs-lookup"><span data-stu-id="1f535-140">Click Default order settings.</span></span>
23. <span data-ttu-id="1f535-141">Lauke „Numatytasis užsakymo tipas“ pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="1f535-141">In the Default order type field, select an option.</span></span>
    * <span data-ttu-id="1f535-142">Pasirinkite „Gamyba“ nurodydami, kad numatytoji šio bendrojo produkto tiekimo parinktis yra jo gamyba.</span><span class="sxs-lookup"><span data-stu-id="1f535-142">Select Production to specify that the default supply option for this product master is to produce it.</span></span>  
24. <span data-ttu-id="1f535-143">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1f535-143">Close the page.</span></span>
25. <span data-ttu-id="1f535-144">Uždarykite formą „Išleisto produkto informacija“.</span><span class="sxs-lookup"><span data-stu-id="1f535-144">Close the Released product details form.</span></span>


