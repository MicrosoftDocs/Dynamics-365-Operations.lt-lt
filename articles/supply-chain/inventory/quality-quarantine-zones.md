---
title: Neatitikimų sulaikymo zonos
description: Šioje temoje aprašoma, kaip sukurti ir naudoti sulaikymo zonas neatitiktims.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93ca74ec4586fffa3b9156aadab887629283b98a
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956763"
---
# <a name="quarantine-zones-for-nonconformances"></a><span data-ttu-id="c6611-103">Neatitikimų sulaikymo zonos</span><span class="sxs-lookup"><span data-stu-id="c6611-103">Quarantine zones for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6611-104">Šioje temoje aprašoma, kaip sukurti ir naudoti sulaikymo zonas neatitiktims.</span><span class="sxs-lookup"><span data-stu-id="c6611-104">This topic describes how to create and use quarantine zones for nonconformances.</span></span>

<span data-ttu-id="c6611-105">Naudokite puslapį **Sulaikymo zonos**, kad apibrėžtumėte zonas, kurios gali būti priskirtos prie neatitikčių.</span><span class="sxs-lookup"><span data-stu-id="c6611-105">You use the **Quarantine zones** page to define zones that can be assigned to nonconformances.</span></span> <span data-ttu-id="c6611-106">Kai sukuriate neatitikčių formą, galite nustatyti sulaikymo zonos ir sulaikymo tipo laukus skirtuke Bendra, **kuris** **yra** **neatitikties** **puslapyje**.</span><span class="sxs-lookup"><span data-stu-id="c6611-106">When you create a nonconformance, you can set the **Quarantine zone** and **Quarantine type** fields on the **General** tab of the **Non conformances** page.</span></span> <span data-ttu-id="c6611-107">Sulaikymo **zonos laukas paprastai nurodo sritį ar** vietą, kurioje yra prekė.</span><span class="sxs-lookup"><span data-stu-id="c6611-107">The **Quarantine zone** field typically indicates the area or location where the item is located.</span></span> <span data-ttu-id="c6611-108">Lauke **Sulaikymo tipas prekė apibrėžiama kaip** Apribotas *naudojimas* arba *Nenaudojama*.</span><span class="sxs-lookup"><span data-stu-id="c6611-108">The **Quarantine type** field defines the item as either *Restricted usage* or *Unusable*.</span></span>

<span data-ttu-id="c6611-109">Kai spausdinate neatitikties arba neatitikties pataisų ataskaitą, galite peržiūrėti sulaikymo zoną, kurioje yra prekė.</span><span class="sxs-lookup"><span data-stu-id="c6611-109">When you print a nonconformance or corrections report for a nonconformance, you can view the quarantine zone where the item is located.</span></span>

<span data-ttu-id="c6611-110">Taip pat galite spausdinti neatitikties žymę.</span><span class="sxs-lookup"><span data-stu-id="c6611-110">You can also print a nonconformance tag for a nonconformance.</span></span> <span data-ttu-id="c6611-111">Ši ataskaita rodo priskirtą sulaikymo zoną ir informaciją apie naudojimą, kuri nurodo, kaip tvarkyti medžiagas su defektais.</span><span class="sxs-lookup"><span data-stu-id="c6611-111">This report shows the assigned quarantine zone and information about usage to provide guidance about how defective material should be handled.</span></span> <span data-ttu-id="c6611-112">Karantino zonos gali atitikti atsargų vietas arba operacijų išteklius.</span><span class="sxs-lookup"><span data-stu-id="c6611-112">The quarantine zones might correspond to inventory locations or operations resources.</span></span>

## <a name="examples-of-quarantine-zones"></a><span data-ttu-id="c6611-113">Sulaikymo zonų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="c6611-113">Examples of quarantine zones</span></span>

### <a name="example-1"></a><span data-ttu-id="c6611-114">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="c6611-114">Example 1</span></span>

<span data-ttu-id="c6611-115">Jūs dirbate elektroninėje gamybos įmonėje, kuri gamina ir paskirsto ttsirbatorius, anglų ir laikmenų gamybas.</span><span class="sxs-lookup"><span data-stu-id="c6611-115">You work at an electronics manufacturing company that produces and distributes televisions, speakers, and media players.</span></span> <span data-ttu-id="c6611-116">Tokiu atveju galite konfigūruoti sulaikymo zoną, kad ji atspindėtų kiekvieną produktų tipą.</span><span class="sxs-lookup"><span data-stu-id="c6611-116">In this case, you can configure a quarantine zone to represent each type of product.</span></span>

### <a name="example-2"></a><span data-ttu-id="c6611-117">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="c6611-117">Example 2</span></span>

<span data-ttu-id="c6611-118">3 talpyklos ir du stelažai naudojami neatitikimo prekėms saugoti.</span><span class="sxs-lookup"><span data-stu-id="c6611-118">Three bins and two racks are used to store items that are nonconforming.</span></span> <span data-ttu-id="c6611-119">Tokiu atveju galite konfigūruoti penkias sulaikymo zonas, po vieną kiekvienam talpyklos ir kiekvienam stelažai.</span><span class="sxs-lookup"><span data-stu-id="c6611-119">In this case, you can configure five quarantine zones, one for each bin and each rack.</span></span>

## <a name="create-a-quarantine-zone"></a><span data-ttu-id="c6611-120">Sukurkite karantino zoną</span><span class="sxs-lookup"><span data-stu-id="c6611-120">Create a quarantine zone</span></span>

1. <span data-ttu-id="c6611-121">Pasirinkite **Atsargų valdymas \> Nustatymas \> Kokybės valdymas \> Sulaikymo zonos**.</span><span class="sxs-lookup"><span data-stu-id="c6611-121">Go to **Inventory management \> Setup \> Quality management \> Quarantine zones**.</span></span>
1. <span data-ttu-id="c6611-122">Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="c6611-122">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="c6611-123">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="c6611-123">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="c6611-124">**Sulaikymo zona** – įveskite unikalų sulaikymo zonos ID arba pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c6611-124">**Quarantine zone** – Enter a unique ID or name for the quarantine zone.</span></span>
    - <span data-ttu-id="c6611-125">**Aprašas** – įveskite išsamų karantino zonos aprašą.</span><span class="sxs-lookup"><span data-stu-id="c6611-125">**Description** – Enter a detailed description of the quarantine zone.</span></span>

1. <span data-ttu-id="c6611-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c6611-126">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6611-127">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c6611-127">Additional resources</span></span>

- [<span data-ttu-id="c6611-128">Kokybės valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="c6611-128">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="c6611-129">Įjungti kiekio ir neatitikties valdymą</span><span class="sxs-lookup"><span data-stu-id="c6611-129">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="c6611-130">Darbuotojai, atsakingi už neatitikties tvirtinimą</span><span class="sxs-lookup"><span data-stu-id="c6611-130">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="c6611-131">Neatitikimų diagnostikos problemos</span><span class="sxs-lookup"><span data-stu-id="c6611-131">Problem types for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="c6611-132">Neatitikimų diagnostikos tipai</span><span class="sxs-lookup"><span data-stu-id="c6611-132">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="c6611-133">Neatitikimų kokybės mokesčiai</span><span class="sxs-lookup"><span data-stu-id="c6611-133">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="c6611-134">Neatitikties operacijos</span><span class="sxs-lookup"><span data-stu-id="c6611-134">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="c6611-135">Sandėlio procesų kokybės valdymas</span><span class="sxs-lookup"><span data-stu-id="c6611-135">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
