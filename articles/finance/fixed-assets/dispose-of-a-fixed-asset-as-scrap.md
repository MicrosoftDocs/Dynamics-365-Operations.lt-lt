---
title: Nurašyto ilgalaikio turto likvidavimas
description: Temoje aprašomas procesas, kurio metu šalinamos nurašyto ilgalaikio turto, kuris buvo likviduotas, operacijos.
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 42eaa3df5ab09278ed96506d17e1b42d4fc2a9e1
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570269"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a><span data-ttu-id="429a5-103">Nurašyto ilgalaikio turto likvidavimas</span><span class="sxs-lookup"><span data-stu-id="429a5-103">Dispose of a fixed asset as scrap</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="429a5-104">Temoje aprašomas procesas, kurio metu šalinamos nurašyto ilgalaikio turto, kuris buvo likviduotas, operacijos.</span><span class="sxs-lookup"><span data-stu-id="429a5-104">The topic describes the process of eliminating transactions for a fixed asset that was disposed of as scrap.</span></span> <span data-ttu-id="429a5-105">Operacijų, kurias galima pašalinti, tipai apima turto įsigijimo ir sukaupto nusidėvėjimo operacijas bei kitas ilgalaikio turto operacijas.</span><span class="sxs-lookup"><span data-stu-id="429a5-105">The transaction types that can be eliminated include an asset's acquisition and accumulated depreciation transactions and other fixed asset transactions.</span></span> <span data-ttu-id="429a5-106">Šių operacijų panaikinimas paveikia balanso sąskaitas, pvz., įsigijimo koregavimą, nusidėvėjimo koregavimą, perkainojimą, vertės padidinimo ir vertės sumažinimo sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="429a5-106">Elimination of these transactions affects balance sheet accounts, such as acquisition adjustment, depreciation adjustment, revaluation, write-up, and write-down accounts.</span></span>

| <span data-ttu-id="429a5-107">Operacija</span><span class="sxs-lookup"><span data-stu-id="429a5-107">Transaction</span></span>                                         | <span data-ttu-id="429a5-108">Debetas (Dr.)</span><span class="sxs-lookup"><span data-stu-id="429a5-108">Debit (Dr.)</span></span> | <span data-ttu-id="429a5-109">Kreditas (Kr.)</span><span class="sxs-lookup"><span data-stu-id="429a5-109">Credit (Cr.)</span></span> |
|-----------------------------------------------------|-------------|--------------|
| <span data-ttu-id="429a5-110">Dr. sukauptas nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="429a5-110">Dr. Accumulated depreciation</span></span>                        | <span data-ttu-id="429a5-111">X</span><span class="sxs-lookup"><span data-stu-id="429a5-111">X</span></span>           |              |
| <span data-ttu-id="429a5-112">Kr. ilgalaikio turto pelnas/nuostolis</span><span class="sxs-lookup"><span data-stu-id="429a5-112">Cr. Fixed assets gain/loss</span></span>                          |             | <span data-ttu-id="429a5-113">X</span><span class="sxs-lookup"><span data-stu-id="429a5-113">X</span></span>            |
| <span data-ttu-id="429a5-114">Dr. ilgalaikio turto pelnas/nuostolis</span><span class="sxs-lookup"><span data-stu-id="429a5-114">Dr. Fixed assets gain/loss</span></span>                          | <span data-ttu-id="429a5-115">X</span><span class="sxs-lookup"><span data-stu-id="429a5-115">X</span></span>           |              |
| <span data-ttu-id="429a5-116">Kr. ilgalaikio turto įsigijimo sąskaitos</span><span class="sxs-lookup"><span data-stu-id="429a5-116">Cr. Fixed asset acquisition account</span></span>                 |             | <span data-ttu-id="429a5-117">X</span><span class="sxs-lookup"><span data-stu-id="429a5-117">X</span></span>            |
| <span data-ttu-id="429a5-118">Dr. ilgalaikio turto pelnas/nuostolis (balansinė vertė \[NBV\])</span><span class="sxs-lookup"><span data-stu-id="429a5-118">Dr. Fixed assets gain/loss (net book value \[NBV\])</span></span> | <span data-ttu-id="429a5-119">X</span><span class="sxs-lookup"><span data-stu-id="429a5-119">X</span></span>           |              |
| <span data-ttu-id="429a5-120">Kr. ilgalaikio turto pelnas/nuostolis (NBV)</span><span class="sxs-lookup"><span data-stu-id="429a5-120">Cr. Fixed assets gain/loss (NBV)</span></span>                    |             | <span data-ttu-id="429a5-121">X</span><span class="sxs-lookup"><span data-stu-id="429a5-121">X</span></span>            |

> [!NOTE]
> <span data-ttu-id="429a5-122">Rekomenduojame glaudžiai bendradarbiauti su savo įmonės vyriausiuoju finansininku (CFO) arba kontrolieriumi, kad būtų galima nustatyti teisingas sąskaitas, naudojamas kiekvienam operacijos tipui, taip pat įsitikinti, kad likvidavimo procesas ir generuojamos operacijos tinkamai naujina šias sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="429a5-122">We recommend that you work closely with your company's chief financial officer (CFO) or controller to identify the correct accounts that should be used for each transaction type, and also to verify that the disposal process and the transactions that it generates update those accounts correctly.</span></span>

<span data-ttu-id="429a5-123">Prieš nurašyto ilgalaikio turto likvidavimą, turite sukurti DK sąskaitas, susietas su turto įsigijimo verte, šių metų nusidėvėjimą, praėjusių metų nusidėvėjimą ir turto NBV.</span><span class="sxs-lookup"><span data-stu-id="429a5-123">Before you dispose of a fixed asset as scrap, you must create ledger accounts that are associated with the asset's acquisition value, depreciation for the current year, depreciation for previous years, and the asset's NBV.</span></span> <span data-ttu-id="429a5-124">Ilgalaikio turto operacijų tipai pateikiami puslapyje **Ilgalaikio turto registravimo šablonas**.</span><span class="sxs-lookup"><span data-stu-id="429a5-124">The fixed asset transaction types are listed on the **Fixed assets posting profile** page.</span></span> <span data-ttu-id="429a5-125">Eikite į **Ilgalaikis turtas \> Sąranka \> Ilgalaikio turto registravimo šablonai**, o tada, „FastTab” konteineryje **Likvidavimas** lauke virš tinklelio pasirinkite **Nurašyta**.</span><span class="sxs-lookup"><span data-stu-id="429a5-125">Go to **Fixed assets \> Setup \> Fixed asset posting profiles**, and then, on the **Disposal** FastTab, select **Scrap** in the field above the grid.</span></span> <span data-ttu-id="429a5-126">Toliau pateiktame paveikslėlyje parodytas ilgalaikio turto operacijų tipų sąrašas puslapyje **Ilgalaikio turto registravimo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="429a5-126">The following illustration shows the list of fixed asset transaction types on the **Fixed asset posting profiles** page.</span></span>


<span data-ttu-id="429a5-127">[![Nurašyto turto likvidavimas, 1 pav.](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span><span class="sxs-lookup"><span data-stu-id="429a5-127">[![Disposing of an asset as scap, Fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span></span>

<span data-ttu-id="429a5-128">Toliau pateiktame pavyzdyje ilgalaikis turtas buvo įsigytas 2018 m. sausio 1 d. ir jis bus nurašytas 2019 m. kovo 31 d.</span><span class="sxs-lookup"><span data-stu-id="429a5-128">For the following example, a fixed asset was acquired on January 1, 2018, and it will be scrapped on March 31, 2019.</span></span>

- <span data-ttu-id="429a5-129">**Įsigijimo kaina:** 24 000,00 JAV doleriai (USD)</span><span class="sxs-lookup"><span data-stu-id="429a5-129">**Acquisition price:** 24,000.00 US dollars (USD)</span></span>
- <span data-ttu-id="429a5-130">**Dėvėjimo laikas:** dveji metai</span><span class="sxs-lookup"><span data-stu-id="429a5-130">**Service life:** Two years</span></span>
- <span data-ttu-id="429a5-131">**Nusidėvėjimo metodas:** tiesiogiai proporcingas dėvėjimo laikas</span><span class="sxs-lookup"><span data-stu-id="429a5-131">**Depreciation method:** Straight line service life</span></span>
- <span data-ttu-id="429a5-132">**Nusidėvėjimo suma:** 1 000,00 USD per mėnesį</span><span class="sxs-lookup"><span data-stu-id="429a5-132">**Depreciation amount:** 1,000.00 USD per month</span></span>

<span data-ttu-id="429a5-133">Ilgalaikio turto NBV apskaičiuojama pagal toliau nurodytą formulę.</span><span class="sxs-lookup"><span data-stu-id="429a5-133">The NBV of a fixed asset is calculated by using the following formula:</span></span>

<span data-ttu-id="429a5-134">Balansinė vertė = įsigijimo kaina – nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="429a5-134">Net book value = Acquisition price – Depreciation</span></span>

<span data-ttu-id="429a5-135">Šiame pavyzdyje ilgalaikis turtas buvo įsigytas ir dėvėtas 15 mėnesių, nuo 2018 m. sausio mėn. iki 2019 m. kovo mėn.</span><span class="sxs-lookup"><span data-stu-id="429a5-135">In this example, the fixed asset was acquired and was depreciated for 15 months, from January 2018 through March 2019.</span></span> <span data-ttu-id="429a5-136">Todėl turto NBV yra 9 000,00 USD (24 000,00 USD – 15 000,00 USD).</span><span class="sxs-lookup"><span data-stu-id="429a5-136">Therefore, the asset's NBV is 9,000.00 USD (24,000.00 USD – 15,000.00 USD).</span></span>

<span data-ttu-id="429a5-137">[![Ilgalaikio turto nusidėvėjimo pavyzdžiai](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span><span class="sxs-lookup"><span data-stu-id="429a5-137">[![Fixed asset depreciation example](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span></span>


<span data-ttu-id="429a5-138">Norėdami sukurti likvidavimo žurnalą, eikite į **Ilgalaikis turtas \> Žurnalo įrašai \> Ilgalaikio turto žurnalas**, tada veiksmų srityje pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="429a5-138">To create a disposal journal, go to **Fixed assets \> Journal entries \> Fixed assets journal**, and then, on the Action Pane, select **Lines**.</span></span> <span data-ttu-id="429a5-139">Pasirinkite **Likvidavimas – nurašymas** ir pasirinkite ilgalaikio turto ID.</span><span class="sxs-lookup"><span data-stu-id="429a5-139">Select **Disposal – scrap**, and then select a fixed asset ID.</span></span> <span data-ttu-id="429a5-140">Norėdami visiškai likviduoti turtą, neįveskite vertės į lauką **Debetas** arba į lauką **Kreditas** .</span><span class="sxs-lookup"><span data-stu-id="429a5-140">To fully dispose of the asset, don't enter a value in either the **Debit** field or the **Credit** field.</span></span>

<span data-ttu-id="429a5-141">[![Ilgalaikio turto žurnalas](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span><span class="sxs-lookup"><span data-stu-id="429a5-141">[![Fixed assets journal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span></span>

<span data-ttu-id="429a5-142">Nurašyto ilgalaikio turto likvidavimo operacija pakeičia ilgalaikio turto knygos laukų vertes toliau nurodytais būdais.</span><span class="sxs-lookup"><span data-stu-id="429a5-142">The fixed asset disposal scrap transaction changes the field values for the fixed asset book in the following ways:</span></span>

- <span data-ttu-id="429a5-143">Skyriuje **Balansas**, laukas **Būsena** atnaujinamas į **Nurašyta**.</span><span class="sxs-lookup"><span data-stu-id="429a5-143">In the **Balance** section, the **Status** field is updated to **Scrapped**.</span></span>
- <span data-ttu-id="429a5-144">Skyriuje **Išdavimas**, laukas **Likvidavimo data** nustatomas į datą, kada turtas buvo nurašytas.</span><span class="sxs-lookup"><span data-stu-id="429a5-144">In the **Issue** section, the **Disposal date** field is set to the date when the asset was scrapped.</span></span>

<span data-ttu-id="429a5-145">[![Ilgalaikio turto žurnalo informacija](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span><span class="sxs-lookup"><span data-stu-id="429a5-145">[![Fixed assets journal detail](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span></span>

<span data-ttu-id="429a5-146">Toliau pateiktame paveikslėlyje parodytas ilgalaikio turto balansas.</span><span class="sxs-lookup"><span data-stu-id="429a5-146">The following illustration shows the fixed asset balance.</span></span>

<span data-ttu-id="429a5-147">[![Ilgalaikio turto balansas](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span><span class="sxs-lookup"><span data-stu-id="429a5-147">[![Fixed asset balance](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span></span>

<span data-ttu-id="429a5-148">Toliau pateiktame paveikslėlyje parodytas užregistruotas kvitas.</span><span class="sxs-lookup"><span data-stu-id="429a5-148">The following illustration shows the voucher that is posted.</span></span>

<span data-ttu-id="429a5-149">[![Balansinė vertė](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span><span class="sxs-lookup"><span data-stu-id="429a5-149">[![Net book value](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span></span>
