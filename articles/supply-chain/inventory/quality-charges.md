---
title: Neatitikties operacijų mokesčiai
description: Šioje temoje aprašoma, kaip kurti kokybės mokesčius, kuriuos galima naudoti su neatitikties operacijomis.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfa424e94048aa9eb1ce4da9aa69e8d4df71cefb
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956757"
---
# <a name="charges-for-nonconformance-operations"></a><span data-ttu-id="8beb9-103">Neatitikties operacijų mokesčiai</span><span class="sxs-lookup"><span data-stu-id="8beb9-103">Charges for nonconformance operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8beb9-104">Šioje temoje aprašoma, kaip kurti kokybės mokesčius, kuriuos galima naudoti su neatitikties operacijomis.</span><span class="sxs-lookup"><span data-stu-id="8beb9-104">This topic describes how to create quality charges that can be used with operations for a nonconformance.</span></span>

<span data-ttu-id="8beb9-105">Naudojate **Kokybės išlaidos** puslapį norėdami nustatyti mokesčių tipus, kuriuos galite pritaikyti neatitikties operacijoms.</span><span class="sxs-lookup"><span data-stu-id="8beb9-105">You use the **Quality charges** page to define the types of charges that can be added to operations for a nonconformance.</span></span> <span data-ttu-id="8beb9-106">Mokesčiai leidžia jums sekti išsamią informaciją apie mokesčius ar mokesčius, kuriuos esate skolingi klientui už produktų neatitikimą arba kurią tiekėjas skolingas jums už gautas neatitiktis produktus.</span><span class="sxs-lookup"><span data-stu-id="8beb9-106">Charges let you track details about fees or charges that you owe to a customer for nonconforming products, or that a vendor owes to you for nonconforming products that you received.</span></span> <span data-ttu-id="8beb9-107">Taip pat galite naudoti išlaidas išlaidoms, kurių reikia išoriniams tiekėjams arba tarnyboms, norėdami atlikti operaciją, sekti.</span><span class="sxs-lookup"><span data-stu-id="8beb9-107">You might also use charges to track costs that are required for external vendors or services to perform an operation.</span></span>

## <a name="examples-of-quality-charges"></a><span data-ttu-id="8beb9-108">Kokybės išlaidų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="8beb9-108">Examples of quality charges</span></span>

<span data-ttu-id="8beb9-109">Jūs dirbate gamybos įmonei.</span><span class="sxs-lookup"><span data-stu-id="8beb9-109">You work for a manufacturing company.</span></span> <span data-ttu-id="8beb9-110">Jūsų įmonėje yra sutarčių su keliais tiekėjais.</span><span class="sxs-lookup"><span data-stu-id="8beb9-110">Your company has contracts with several vendors.</span></span> <span data-ttu-id="8beb9-111">Šios sutartys apibūdina laiku siųstus siuntų, sugadinimo ir produktų kokybės standartus.</span><span class="sxs-lookup"><span data-stu-id="8beb9-111">Those contracts outline standards for on-time shipment, damages, and product quality for items.</span></span> <span data-ttu-id="8beb9-112">Taip pat keli jūsų klientai su savo įmone yra su sutartimis dėl grąžinimo, sugadinimo ir produkto kokybės.</span><span class="sxs-lookup"><span data-stu-id="8beb9-112">Likewise, several of your customers have agreements with your company about returns, damages, and product quality.</span></span>

<span data-ttu-id="8beb9-113">Mokesčio struktūra apibrėžiama kiekvienai dalyje ir nurodoma sutartyje.</span><span class="sxs-lookup"><span data-stu-id="8beb9-113">A fee structure is defined for each circumstance and specified in the contract.</span></span> <span data-ttu-id="8beb9-114">Galite konfigūruoti kokybės mokesčius, norėdami nurodyti įvairius išlaidų tipus, pvz., *Nuostoliai*, *Pavėluota siunta* ir *Kokybės*.</span><span class="sxs-lookup"><span data-stu-id="8beb9-114">You can configure quality charges to outline the various types of charges, such as *Damages*, *Late shipment*, and *Quality*.</span></span> <span data-ttu-id="8beb9-115">Tada, kai sukuriate neatitiką, pridedate vieną ar daugiau operacijų.</span><span class="sxs-lookup"><span data-stu-id="8beb9-115">Then, when you create a nonconformance, you add one or more operations.</span></span> <span data-ttu-id="8beb9-116">Norėdami nurodyti išsamią kiekvienos operacijos **informaciją** apie mokesčius, pasirinkite Mokesčiai.</span><span class="sxs-lookup"><span data-stu-id="8beb9-116">For each operation, you select **Charges** to define the details about the fees.</span></span>

## <a name="create-a-quality-charge"></a><span data-ttu-id="8beb9-117">Kurti kokybės mokestį</span><span class="sxs-lookup"><span data-stu-id="8beb9-117">Create a quality charge</span></span>

1. <span data-ttu-id="8beb9-118">Pasirinkite **Atsargų valdymas \> Nustatymas \> Kokybės valdymas \> Kokybės išlaidos**.</span><span class="sxs-lookup"><span data-stu-id="8beb9-118">Go to **Inventory management \> Setup \> Quality management \> Quality charges**.</span></span>
1. <span data-ttu-id="8beb9-119">Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="8beb9-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="8beb9-120">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="8beb9-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="8beb9-121">**Išlaidų kodas** – įveskite unikalų kokybės mokesčio ID arba pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="8beb9-121">**Charges code** – Enter a unique ID or name for the quality charge.</span></span>
    - <span data-ttu-id="8beb9-122">**Aprašas** – įveskite išsamų kokybės mokesčių aprašą.</span><span class="sxs-lookup"><span data-stu-id="8beb9-122">**Description** – Enter a detailed description of the quality charge.</span></span>

1. <span data-ttu-id="8beb9-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8beb9-123">Close the page.</span></span>

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a><span data-ttu-id="8beb9-124">Kokybės mokesčio įtraukimas į operaciją, kad neatitiktis</span><span class="sxs-lookup"><span data-stu-id="8beb9-124">Add a quality charge to an operation for a nonconformance</span></span>

<span data-ttu-id="8beb9-125">Išsamesnės informacijos apie tai, kaip pridėti operacijas prie neatitikties ir taikyti joms išlaidas, ieškokite [Neatitikimų](quality-operations.md) operacijos.</span><span class="sxs-lookup"><span data-stu-id="8beb9-125">For details about how to add operations to a nonconformance and apply charges to them, see [Operations for nonconformances](quality-operations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8beb9-126">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="8beb9-126">Additional resources</span></span>

- [<span data-ttu-id="8beb9-127">Kokybės valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="8beb9-127">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="8beb9-128">Įjungti kiekio ir neatitikties valdymą</span><span class="sxs-lookup"><span data-stu-id="8beb9-128">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="8beb9-129">Darbuotojai, atsakingi už neatitikties tvirtinimą</span><span class="sxs-lookup"><span data-stu-id="8beb9-129">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="8beb9-130">Neatitikimų sulaikymo zonos</span><span class="sxs-lookup"><span data-stu-id="8beb9-130">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="8beb9-131">Neatitikimų diagnostikos tipai</span><span class="sxs-lookup"><span data-stu-id="8beb9-131">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="8beb9-132">Neatitikimų kokybės mokesčiai</span><span class="sxs-lookup"><span data-stu-id="8beb9-132">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="8beb9-133">Neatitikties operacijos</span><span class="sxs-lookup"><span data-stu-id="8beb9-133">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="8beb9-134">Sandėlio procesų kokybės valdymas</span><span class="sxs-lookup"><span data-stu-id="8beb9-134">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
