---
title: Neatitikimų diagnostikos problemos
description: Šioje temoje aprašoma, kaip sukurti ir naudoti problemos tipo neatitiktims.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df509365f5c900898921acfbda380b5e20c7a251
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956764"
---
# <a name="problem-types-for-nonconformances"></a><span data-ttu-id="b76ef-103">Neatitikimų diagnostikos problemos</span><span class="sxs-lookup"><span data-stu-id="b76ef-103">Problem types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b76ef-104">Šioje temoje aprašoma, kaip sukurti ir naudoti problemos tipo neatitiktims.</span><span class="sxs-lookup"><span data-stu-id="b76ef-104">This topic describes how to create and use problem types for nonconformances.</span></span>

<span data-ttu-id="b76ef-105">Naudodami puslapį **Problemų tipai** apibrėžkite kokybės problemų, su kuriomis galima susidurti įvairiuose neatitikimo tipuose, klasifikaciją.</span><span class="sxs-lookup"><span data-stu-id="b76ef-105">You use the **Problem types** page to define a classification of the quality problems that might occur for the various nonconformance types.</span></span> <span data-ttu-id="b76ef-106">Turite nurodyti kiekvieno sukurto problemos tipo neatitiktys, su kuria gali būti naudojamas problemos tipas, tipus.</span><span class="sxs-lookup"><span data-stu-id="b76ef-106">For each problem type that you create, you must specify the types of nonconformances that the problem type can be used with.</span></span> <span data-ttu-id="b76ef-107">Galite nustatyti šiuos neatitikimo tipus:</span><span class="sxs-lookup"><span data-stu-id="b76ef-107">You can set up the following nonconformance types:</span></span>

- <span data-ttu-id="b76ef-108">**Vidinis – šio tipo neatitiktis yra susijusios su turimomis** atsargomis (pvz., kokybės užsakymais arba sulaikymo užsakymais).</span><span class="sxs-lookup"><span data-stu-id="b76ef-108">**Internal** – Nonconformances of this type are related to on-hand inventory (for example, quality orders or quarantine orders).</span></span>
- <span data-ttu-id="b76ef-109">**Klientas** – šio tipo neatitiktis susijusios su pardavimo užsakymais.</span><span class="sxs-lookup"><span data-stu-id="b76ef-109">**Customer** – Nonconformances of this type are related to sales orders.</span></span>
- <span data-ttu-id="b76ef-110">**Tiekėjas** – šio tipo neatitiktis susijusios su pirkimo užsakymais.</span><span class="sxs-lookup"><span data-stu-id="b76ef-110">**Vendor** – Nonconformances of this type are related to purchase orders.</span></span>
- <span data-ttu-id="b76ef-111">**Paslaugos užklausa** – šio tipo neatitiktis susijusios su paslaugų užsakymais.</span><span class="sxs-lookup"><span data-stu-id="b76ef-111">**Service request** – Nonconformances of this type are related to service orders.</span></span>
- <span data-ttu-id="b76ef-112">**Gamyba** – Šio tipo neatitiktys yra susijusios su paketo užsakymais ar gamybos užsakymais.</span><span class="sxs-lookup"><span data-stu-id="b76ef-112">**Production** – Nonconformances of this type are related to batch orders or production orders.</span></span>
- <span data-ttu-id="b76ef-113">**Bendro produkto gamyba** – Šio tipo neatitiktys yra susijusios su paketo užsakymais ar bendro produkto užsakymais.</span><span class="sxs-lookup"><span data-stu-id="b76ef-113">**Co-product production** – Nonconformances of this type are related to batch orders for co-products.</span></span>

<span data-ttu-id="b76ef-114">Kai sukuriate naują problemos tipą, veiksmų srityje pasirinkite Neatitikties tipai, kad sukurtumėte vieno ar daugiau neatitikties tipų, kurie leidžiami problemos **tipui**, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="b76ef-114">When you create a new problem type, select **Non conformance types** on the Action Pane to create a list of one or more nonconformance types that are authorized for the problem type.</span></span> <span data-ttu-id="b76ef-115">Pvz., problemos tipas, susijęs su defekto kodu, gali būti pritaikytas visiems neatitikties tipams.</span><span class="sxs-lookup"><span data-stu-id="b76ef-115">For example, a problem type that is related to a defect code might apply to all nonconformance types.</span></span> <span data-ttu-id="b76ef-116">Tačiau problemos tipas, susijęs su kliento nusiskundimais, gali būti taikomas tik **kliento** ir **aptarnavimo** užklausos neatitikties tipams.</span><span class="sxs-lookup"><span data-stu-id="b76ef-116">However, a problem type that is related to customer complaints might apply only to the **Customer** and **Service request** nonconformance types.</span></span>

## <a name="examples-of-problem-types"></a><span data-ttu-id="b76ef-117">Problemų tipų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="b76ef-117">Examples of problem types</span></span>

<span data-ttu-id="b76ef-118">Toliau pateikiami keletas scenarijų problemų tipams, kurie gali būti naudojami su skirtingais neatitikties tipais:</span><span class="sxs-lookup"><span data-stu-id="b76ef-118">Here are some examples of scenarios for problem types that can be used with the different nonconformance types:</span></span>

- <span data-ttu-id="b76ef-119">**Klientas:** klientas užpildė pakeitimus, klientas pateikė grąžinimą arba kokybės specifikacijų nebuvo.</span><span class="sxs-lookup"><span data-stu-id="b76ef-119">**Customer:** A customer filed a complaint, a customer made a return, or quality specifications weren't met.</span></span>
- <span data-ttu-id="b76ef-120">**Tiekėjas: produktas buvo sugadintas, kokybės specifikacijos įvykdytos** arba gautas netinkamas produktas.</span><span class="sxs-lookup"><span data-stu-id="b76ef-120">**Vendor:** The product was damaged, quality specifications weren't met, or the wrong product was received.</span></span>
- <span data-ttu-id="b76ef-121">**Aptarnavimo** užklausa: nebuvo įvykdytos kokybės specifikacijos, klientas užpildė priežiūrą arba reikalinga įrenginio priežiūra.</span><span class="sxs-lookup"><span data-stu-id="b76ef-121">**Service request:** Quality specifications weren't met, a customer filed a complaint, or machine maintenance is required.</span></span>
- <span data-ttu-id="b76ef-122">**Gamyba:** neatitinka kokybės specifikacijų, reikalinga įrenginio priežiūra arba produktas buvo sugadintas.</span><span class="sxs-lookup"><span data-stu-id="b76ef-122">**Production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>
- <span data-ttu-id="b76ef-123">**Bendro produkto gamyba:** neatitinka kokybės specifikacijų, reikalinga įrenginio priežiūra arba produktas buvo sugadintas.</span><span class="sxs-lookup"><span data-stu-id="b76ef-123">**Co-product production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a><span data-ttu-id="b76ef-124">Kurti problemos tipą ir priskirti jį neatitikties tipams</span><span class="sxs-lookup"><span data-stu-id="b76ef-124">Create a problem type and assign it to nonconformance types</span></span>

1. <span data-ttu-id="b76ef-125">Pasirinkite **Atsargų valdymas \> Nustatymas \> Kokybės valdymas \> Problemų tipai**.</span><span class="sxs-lookup"><span data-stu-id="b76ef-125">Go to **Inventory management \> Setup \> Quality management \> Problem types**.</span></span>
1. <span data-ttu-id="b76ef-126">Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="b76ef-126">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b76ef-127">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="b76ef-127">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="b76ef-128">**Problemos tipas** – Įveskite unikalų ID ar problemos tipo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="b76ef-128">**Problem type** – Enter a unique ID or name for the problem type.</span></span>
    - <span data-ttu-id="b76ef-129">**Aprašas** – įveskite išsamų problemos tipo aprašą.</span><span class="sxs-lookup"><span data-stu-id="b76ef-129">**Description** – Enter a detailed description of the problem type.</span></span>

1. <span data-ttu-id="b76ef-130">Kol nauja eilutė vis dar pasirinkta, **veiksmų srityje pasirinkite** Neatitikties tipai.</span><span class="sxs-lookup"><span data-stu-id="b76ef-130">While the new row is still selected, select **Non conformance types** on the Action Pane.</span></span>
1. <span data-ttu-id="b76ef-131">Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="b76ef-131">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b76ef-132">Tada naujoje eilutėje nustatykite neatitikties tipo lauką kaip neatitikties tipą, **kurį norite leisti naudoti problemos** tipui.</span><span class="sxs-lookup"><span data-stu-id="b76ef-132">Then, for the new row, set the **Non conformance type** field to the nonconformance type that you want to allow for the problem type.</span></span>
1. <span data-ttu-id="b76ef-133">Pakartokite ankstesnį veiksmą su kiekvienu papildomu neatitikties tipu, kurį norite autorizuoti problemos tipui.</span><span class="sxs-lookup"><span data-stu-id="b76ef-133">Repeat the previous step for each additional nonconformance type that you want to authorize for the problem type.</span></span>
1. <span data-ttu-id="b76ef-134">Uždarykite puslapius.</span><span class="sxs-lookup"><span data-stu-id="b76ef-134">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b76ef-135">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b76ef-135">Additional resources</span></span>

- [<span data-ttu-id="b76ef-136">Kokybės valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="b76ef-136">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="b76ef-137">Įjungti kiekio ir neatitikties valdymą</span><span class="sxs-lookup"><span data-stu-id="b76ef-137">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="b76ef-138">Darbuotojai, atsakingi už neatitikties tvirtinimą</span><span class="sxs-lookup"><span data-stu-id="b76ef-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="b76ef-139">Neatitikimų sulaikymo zonos</span><span class="sxs-lookup"><span data-stu-id="b76ef-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="b76ef-140">Neatitikimų diagnostikos tipai</span><span class="sxs-lookup"><span data-stu-id="b76ef-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="b76ef-141">Neatitikimų kokybės mokesčiai</span><span class="sxs-lookup"><span data-stu-id="b76ef-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="b76ef-142">Neatitikties operacijos</span><span class="sxs-lookup"><span data-stu-id="b76ef-142">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="b76ef-143">Sandėlio procesų kokybės valdymas</span><span class="sxs-lookup"><span data-stu-id="b76ef-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
