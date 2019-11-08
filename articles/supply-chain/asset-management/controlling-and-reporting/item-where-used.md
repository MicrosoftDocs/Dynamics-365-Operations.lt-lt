---
title: Kur naudota prekė
description: Šioje temoje aiškinama, kaip sužinoti, kur prekė naudojama modulyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 511108e689c10e27a42253d95b02e5394f9eb713
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652361"
---
# <a name="item-where-used"></a><span data-ttu-id="0e2eb-103">Kur naudota prekė</span><span class="sxs-lookup"><span data-stu-id="0e2eb-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0e2eb-104">Galite atlikti tam tikros prekės apskaičiavimą, kad sužinotumėte, kur prekė panaudota modulyje Turto valdymas.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="0e2eb-105">Gavus rezultatus, pateikiamas kontekstas, kuriame prekė buvo naudota per egzistavimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="0e2eb-106">Puslapį **Kur naudota prekė** galima atsiversti naudojant pagrindinį modulio Turto valdymas meniu; minėtą puslapį taip pat galima pasiekti atsivertus toliau pateikiamus puslapius.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-106">The **Item where used** page can be opened from the main Asset Management menu, and it can also be accessed from the following pages:</span></span>

- [<span data-ttu-id="0e2eb-107">Turto KS</span><span class="sxs-lookup"><span data-stu-id="0e2eb-107">Asset BOM</span></span>](../objects/object-BOM.md)

- [<span data-ttu-id="0e2eb-108">Turto tipo numatytųjų reikšmių atsarginės dalys</span><span class="sxs-lookup"><span data-stu-id="0e2eb-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md)

- [<span data-ttu-id="0e2eb-109">Priežiūros užduočių tipų numatytųjų reikšmių prognozės prekės prognozė</span><span class="sxs-lookup"><span data-stu-id="0e2eb-109">Item forecast on Maintenance job type defaults forecast</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [<span data-ttu-id="0e2eb-110">Darbo užsakymo priežiūros prognozė</span><span class="sxs-lookup"><span data-stu-id="0e2eb-110">Work order maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

- [<span data-ttu-id="0e2eb-111">Darbo užsakymo pirkimo paraiška</span><span class="sxs-lookup"><span data-stu-id="0e2eb-111">Work order purchase requisition</span></span>](../work-orders/procurement.md)

- [<span data-ttu-id="0e2eb-112">Darbo užsakymo pirkimas</span><span class="sxs-lookup"><span data-stu-id="0e2eb-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="0e2eb-113">Apskaičiavimo Kur naudota prekė atlikimas</span><span class="sxs-lookup"><span data-stu-id="0e2eb-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="0e2eb-114">Spustelėkite **Turto valdymas** > **Užklausos** > **Kur naudota prekė** arba pasirinkite mygtuką **Kur naudota prekė** viename iš pirmiau minėtų puslapių.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="0e2eb-115">Dialogo lange **Kur naudota prekė** lauke **Prekės numeris** pasirinkite prekę, kurios apskaičiavimą norite atlikti.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="0e2eb-116">Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti prekės eilutėse.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="0e2eb-117">Pavyzdžiui, jei lauke įrašysite skaičių „1“ ir funkcinių vietų struktūroje yra keletas lygių, visos funkcinės vietos prekės eilutės bus rodomos aukščiausiame lygyje.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="0e2eb-118">Todėl eilutės ryšys / kiekis gali būti žemesniame lygyje esančių funkcinių vietų suma.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="0e2eb-119">Jei lauke **Lygis** įrašysite skaičių „0“, matysite išsamų rezultatą, rodantį visas prekių eilutes visuose funkcinių vietų lygiuose, su kuriais jos yra susijusios.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="0e2eb-120">Skyriuje **Įtraukti** perjungimo mygtukuose, kuriuos norite įtraukti į apskaičiavimą, pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="0e2eb-121">Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="0e2eb-122">Skirtuke **Kur naudota prekė** pasirinkite mygtukus **Grupuoti pagal**, kad būtų rodomas pageidaujamas apskaičiavimo išsamumo lygis.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-122">On the **Item where used** tab, select the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="0e2eb-123">Pažymėti mygtukai **Grupuoti pagal** yra paryškinti.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-123">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="0e2eb-124">Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="0e2eb-125">Spustelėkite **Rodyti dimensijas**, jei norite matyti dimensijas, susijusias su preke, ir pasirinkite rodytinas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

## <a name="example"></a><span data-ttu-id="0e2eb-126">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="0e2eb-126">Example</span></span>

<span data-ttu-id="0e2eb-127">Toliau pateiktoje ekrano kopijoje rodomas apskaičiavimo Kur naudota prekė, kai prekių skaičius yra „1000“, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-127">In the screenshot below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![Apskaičiavimo Kur naudota prekė pavyzdys](media/12-controlling-and-reporting.png)

