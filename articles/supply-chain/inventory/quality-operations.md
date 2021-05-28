---
title: Neatitikties operacijos
description: Šioje temoje aprašoma, kaip sukurti ir naudoti neatitikčių operacijas.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9a6cc88b80f82d77edac0341cb6a3c0db4b42ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022209"
---
# <a name="operations-for-nonconformances"></a><span data-ttu-id="e6d84-103">Neatitikties operacijos</span><span class="sxs-lookup"><span data-stu-id="e6d84-103">Operations for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6d84-104">Šioje temoje aprašoma, kaip sukurti ir naudoti neatitikčių operacijas.</span><span class="sxs-lookup"><span data-stu-id="e6d84-104">This topic describes how to create and use operations for nonconformances.</span></span>

<span data-ttu-id="e6d84-105">Norėdami nurodyti darbų, kurie gali būti atlikti atsiradus patvirtintai neatitikčiai, klasifikaciją, naudokite puslapį **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="e6d84-105">You can use the **Operations** page to define classifications of the work that can be performed for an approved nonconformance.</span></span> <span data-ttu-id="e6d84-106">Priskyrę susijusią operaciją neatitikčiai taip pat galite pateikti išsamią informaciją , pvz., apie susijusią medžiagą, darbo valandas ir papildomas išlaidas, būtinas atliekant operaciją.</span><span class="sxs-lookup"><span data-stu-id="e6d84-106">When you assign a related operation to a nonconformance, you can provide details such as the associated material, labor hours, and charges that are required to do the operation.</span></span> <span data-ttu-id="e6d84-107">Sistema informacija naudojama skaičiuojant operacijos įvertintą savikainą.</span><span class="sxs-lookup"><span data-stu-id="e6d84-107">The system uses this information to calculate an estimated cost for the operation.</span></span> <span data-ttu-id="e6d84-108">Išsami informacija ir įvertinta savikaina naudojamos kaip nuorodos.</span><span class="sxs-lookup"><span data-stu-id="e6d84-108">The detailed information and estimated costs are for reference.</span></span> <span data-ttu-id="e6d84-109">Susijusios kokybės operacijos skiriasi nuo galimų nurodyti gamybos maršruto operacijų.</span><span class="sxs-lookup"><span data-stu-id="e6d84-109">The related operations for quality differ from the operations that can be defined for a production route.</span></span>

> [!NOTE]
> <span data-ttu-id="e6d84-110">Nors galite sekti išlaidas, laiką ir prekes, naudojamas operacijoje, susijusioje su neatitiktimi, jūsų įvesti duomenys yra tik informaciniai.</span><span class="sxs-lookup"><span data-stu-id="e6d84-110">Although you can track costs, time, and the items that are used in an operation that is related to a nonconformance, the data that you enter is only informational.</span></span> <span data-ttu-id="e6d84-111">Jis nėra automatiškai integruotas su DK, atsargų antrašu arba laiko ir **lankomumo** moduliu.</span><span class="sxs-lookup"><span data-stu-id="e6d84-111">It isn't automatically integrated with the general ledger, inventory subledger, or the **Time and attendance** module.</span></span>

## <a name="examples-of-operations"></a><span data-ttu-id="e6d84-112">Operacijų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="e6d84-112">Examples of operations</span></span>

<span data-ttu-id="e6d84-113">Jūs dirbate gamybos įmonei.</span><span class="sxs-lookup"><span data-stu-id="e6d84-113">You work for a manufacturing company.</span></span> <span data-ttu-id="e6d84-114">Neatitiktis buvo sukurta ir patvirtinta prekėms, kurių kokybės tikrinimo atlikti nepavyko.</span><span class="sxs-lookup"><span data-stu-id="e6d84-114">A nonconformance was created and approved for items that failed a quality test.</span></span> <span data-ttu-id="e6d84-115">Buvo sukurtas pataisymas, nurodantis, kad problema buvo susijusi su bloga įrenginio pereime.</span><span class="sxs-lookup"><span data-stu-id="e6d84-115">A correction was created to indicate that the problem was related to a bad bearing on a machine.</span></span> <span data-ttu-id="e6d84-116">Norint pakeisti operaciją reikia atlikti keletą veiksmų, ir sekama kiekvienos operacijos atsakomybė.</span><span class="sxs-lookup"><span data-stu-id="e6d84-116">Several steps are required to replace the bearing, and the responsibility for each operation is tracked.</span></span> <span data-ttu-id="e6d84-117">Pavyzdžiui, gali reikėti atlikti šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="e6d84-117">For example, the following steps might be required:</span></span>

1. <span data-ttu-id="e6d84-118">Gamybos eilutė sustabdyta ir vykdomas išvalomas režimas.</span><span class="sxs-lookup"><span data-stu-id="e6d84-118">The production line is stopped, and the clean-out routine is performed.</span></span>
1. <span data-ttu-id="e6d84-119">Priežiūros personalas pakeičia esamą.</span><span class="sxs-lookup"><span data-stu-id="e6d84-119">Maintenance personnel replace the bearing.</span></span>
1. <span data-ttu-id="e6d84-120">Kokybės užtikrinimo personalas tikrina mašiną prieš įjungdami jį atgal.</span><span class="sxs-lookup"><span data-stu-id="e6d84-120">Quality assurance personnel inspect the machine before it's turned back on.</span></span>

<span data-ttu-id="e6d84-121">Pavyzdžiui, šios operacijos gali būti sukurtos, kad atspindėtų darbą, kuris turi būti atliktas:</span><span class="sxs-lookup"><span data-stu-id="e6d84-121">For this example, the following operations can be created to represent the work that must be done:</span></span>

- <span data-ttu-id="e6d84-122">Sustabdyti gamybos eilutę.</span><span class="sxs-lookup"><span data-stu-id="e6d84-122">Stop the production line.</span></span>
- <span data-ttu-id="e6d84-123">Išvalykite gamybos eilutę.</span><span class="sxs-lookup"><span data-stu-id="e6d84-123">Clean out the production line.</span></span>
- <span data-ttu-id="e6d84-124">Vykdyti mašinos priežiūrą.</span><span class="sxs-lookup"><span data-stu-id="e6d84-124">Perform machine maintenance.</span></span>
- <span data-ttu-id="e6d84-125">Patikrinti įrenginį.</span><span class="sxs-lookup"><span data-stu-id="e6d84-125">Inspect the machine.</span></span>

## <a name="create-an-operation"></a><span data-ttu-id="e6d84-126">Kurti veiksmą</span><span class="sxs-lookup"><span data-stu-id="e6d84-126">Create an operation</span></span>

1. <span data-ttu-id="e6d84-127">Eikite į **Atsargų valdymas \> Nustatymas \> Kokybės valdymas \> Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="e6d84-127">Go to **Inventory management \> Setup \> Quality management \> Operations**.</span></span>
1. <span data-ttu-id="e6d84-128">Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="e6d84-128">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="e6d84-129">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="e6d84-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e6d84-130">**Operacija** – įveskite unikalų tikrinimo prietaiso ID pavadinimą ar operaciją.</span><span class="sxs-lookup"><span data-stu-id="e6d84-130">**Operation** – Enter a unique ID or name for the operation.</span></span>
    - <span data-ttu-id="e6d84-131">**Aprašas** – įveskite išsamų bandymo operacijos aprašą.</span><span class="sxs-lookup"><span data-stu-id="e6d84-131">**Description** – Enter a detailed description of the operation.</span></span>
    - <span data-ttu-id="e6d84-132">**Tipas – jei operacija gali būti naudojama tik su neatitiktimis, susijusiomis su konkrečiu užsakymo tipu, pasirinkite užsakymo tipą (Pirkimo užsakymas** arba *arba Pardavimo* *užsakymas*).</span><span class="sxs-lookup"><span data-stu-id="e6d84-132">**Type** – If the operation can be used only with nonconformances that are related to a specific type of order, select the order type (*Purchase order* or *Sales order*).</span></span>

1. <span data-ttu-id="e6d84-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e6d84-133">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6d84-134">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e6d84-134">Additional resources</span></span>

- [<span data-ttu-id="e6d84-135">Kokybės valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="e6d84-135">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="e6d84-136">Įjungti kiekio ir neatitikties valdymą</span><span class="sxs-lookup"><span data-stu-id="e6d84-136">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="e6d84-137">Neatitikimo kūrimas ir apdorojimas</span><span class="sxs-lookup"><span data-stu-id="e6d84-137">Create and process nonconformances</span></span>](tasks/create-process-non-conformance.md)
- [<span data-ttu-id="e6d84-138">Darbuotojai, atsakingi už neatitikties tvirtinimą</span><span class="sxs-lookup"><span data-stu-id="e6d84-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="e6d84-139">Neatitikimų sulaikymo zonos</span><span class="sxs-lookup"><span data-stu-id="e6d84-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="e6d84-140">Neatitikimų diagnostikos tipai</span><span class="sxs-lookup"><span data-stu-id="e6d84-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="e6d84-141">Neatitikimų kokybės mokesčiai</span><span class="sxs-lookup"><span data-stu-id="e6d84-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="e6d84-142">Neatitikimų diagnostikos problemos</span><span class="sxs-lookup"><span data-stu-id="e6d84-142">Problem types for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="e6d84-143">Sandėlio procesų kokybės valdymas</span><span class="sxs-lookup"><span data-stu-id="e6d84-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
