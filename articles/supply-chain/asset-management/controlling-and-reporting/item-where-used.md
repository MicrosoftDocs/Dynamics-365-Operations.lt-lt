---
title: Kur naudota prekė
description: Šioje temoje aiškinama, kaip sužinoti, kur prekė naudojama modulyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetItemWhereUsed, EntAssetItemWhereUsedCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ef020c6a917f0a2c358f775991182e1e494d45d6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253763"
---
# <a name="item-where-used"></a><span data-ttu-id="25c81-103">Kur naudota prekė</span><span class="sxs-lookup"><span data-stu-id="25c81-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="25c81-104">Galite atlikti tam tikros prekės apskaičiavimą, kad sužinotumėte, kur prekė panaudota modulyje Turto valdymas.</span><span class="sxs-lookup"><span data-stu-id="25c81-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="25c81-105">Gavus rezultatus, pateikiamas kontekstas, kuriame prekė buvo naudota per egzistavimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="25c81-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="25c81-106">Puslapį **Kur naudota prekė** galima atsiversti naudojant pagrindinį modulio Turto valdymas meniu; minėtą puslapį taip pat galima pasiekti atsivertus toliau pateikiamus puslapius.</span><span class="sxs-lookup"><span data-stu-id="25c81-106">The **Item where used** page can be opened from the main Asset Management menu, and it can also be accessed from the following pages:</span></span>

- [<span data-ttu-id="25c81-107">Turto KS</span><span class="sxs-lookup"><span data-stu-id="25c81-107">Asset BOMs</span></span>](../objects/object-BOM.md)

- [<span data-ttu-id="25c81-108">Turto tipo numatytųjų reikšmių atsarginės dalys</span><span class="sxs-lookup"><span data-stu-id="25c81-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [<span data-ttu-id="25c81-109">Priežiūros užduoties tipo kategorijos ir priežiūros užduočių tipai, priežiūros užduočių tipo variantai, priežiūros užduočių prekyba ir prižiūrimo turto kontroliniai sąrašai</span><span class="sxs-lookup"><span data-stu-id="25c81-109">Maintenance job type categories and maintenance job types, maintenance job type variants, maintenance job trades, and maintenance checklists</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [<span data-ttu-id="25c81-110">Priežiūros prognozė</span><span class="sxs-lookup"><span data-stu-id="25c81-110">Maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

- [<span data-ttu-id="25c81-111">Įsigijimas</span><span class="sxs-lookup"><span data-stu-id="25c81-111">Procurement</span></span>](../work-orders/procurement.md)

- [<span data-ttu-id="25c81-112">Darbo užsakymo pirkimas</span><span class="sxs-lookup"><span data-stu-id="25c81-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="25c81-113">Apskaičiavimo Kur naudota prekė atlikimas</span><span class="sxs-lookup"><span data-stu-id="25c81-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="25c81-114">Spustelėkite **Turto valdymas** > **Užklausos** > **Kur naudota prekė** arba pasirinkite mygtuką **Kur naudota prekė** viename iš pirmiau minėtų puslapių.</span><span class="sxs-lookup"><span data-stu-id="25c81-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="25c81-115">Dialogo lange **Kur naudota prekė** lauke **Prekės numeris** pasirinkite prekę, kurios apskaičiavimą norite atlikti.</span><span class="sxs-lookup"><span data-stu-id="25c81-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="25c81-116">Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti prekės eilutėse.</span><span class="sxs-lookup"><span data-stu-id="25c81-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="25c81-117">Pavyzdžiui, jei lauke įrašysite skaičių „1“ ir funkcinių vietų struktūroje yra keletas lygių, visos funkcinės vietos prekės eilutės bus rodomos aukščiausiame lygyje.</span><span class="sxs-lookup"><span data-stu-id="25c81-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="25c81-118">Todėl eilutės ryšys / kiekis gali būti žemesniame lygyje esančių funkcinių vietų suma.</span><span class="sxs-lookup"><span data-stu-id="25c81-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="25c81-119">Jei lauke **Lygis** įrašysite skaičių „0“, matysite išsamų rezultatą, rodantį visas prekių eilutes visuose funkcinių vietų lygiuose, su kuriais jos yra susijusios.</span><span class="sxs-lookup"><span data-stu-id="25c81-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="25c81-120">Skyriuje **Įtraukti** perjungimo mygtukuose, kuriuos norite įtraukti į apskaičiavimą, pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="25c81-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="25c81-121">Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25c81-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="25c81-122">Skirtuke **Kur naudota prekė** pasirinkite mygtukus **Grupuoti pagal**, kad būtų rodomas pageidaujamas apskaičiavimo išsamumo lygis.</span><span class="sxs-lookup"><span data-stu-id="25c81-122">On the **Item where used** tab, select the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="25c81-123">Pažymėti mygtukai **Grupuoti pagal** yra paryškinti.</span><span class="sxs-lookup"><span data-stu-id="25c81-123">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="25c81-124">Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.</span><span class="sxs-lookup"><span data-stu-id="25c81-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="25c81-125">Spustelėkite **Rodyti dimensijas**, jei norite matyti dimensijas, susijusias su preke, ir pasirinkite rodytinas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="25c81-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

## <a name="example"></a><span data-ttu-id="25c81-126">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="25c81-126">Example</span></span>

<span data-ttu-id="25c81-127">Toliau pateiktoje ekrano kopijoje rodomas apskaičiavimo Kur naudota prekė, kai prekių skaičius yra „1000“, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="25c81-127">In the screenshot below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![Apskaičiavimo Kur naudota prekė pavyzdys](media/12-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]