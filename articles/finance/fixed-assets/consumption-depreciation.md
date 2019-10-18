---
title: Produkcijos metodas
description: Šiame straipsnyje apžvelgtas nusidėvėjimo Naudojimo metodas.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c9d95a7a45ed99c63516749285126c786685c87
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187319"
---
# <a name="consumption-depreciation"></a><span data-ttu-id="a1006-103">Produkcijos metodas</span><span class="sxs-lookup"><span data-stu-id="a1006-103">Consumption depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1006-104">Šiame straipsnyje apžvelgtas nusidėvėjimo Naudojimo metodas.</span><span class="sxs-lookup"><span data-stu-id="a1006-104">This article gives an overview of the Consumption method of depreciation.</span></span>

<span data-ttu-id="a1006-105">Jei nustatote ilgalaikio turto nusidėvėjimo profilį ir **Nusidėvėjimo profilių** puslapio lauke **Metodas** pasirenkate **Naudojimas**, ilgalaikis turtas nusidėvėjimo profiliui priskiriamas pagal jo naudojimą.</span><span class="sxs-lookup"><span data-stu-id="a1006-105">If you set up a depreciation profile for fixed assets and select **Consumption** in the **Method** field on the **Depreciation profiles** page, fixed assets are assigned to the depreciation profile based on their usage.</span></span> <span data-ttu-id="a1006-106">**Nusidėvėjimo profilių** puslapyje procentų ir intervalų nustatyti nereikia.</span><span class="sxs-lookup"><span data-stu-id="a1006-106">You don't have to set up percentages and intervals on the **Depreciation profiles** page.</span></span> <span data-ttu-id="a1006-107">Kai sukuriate nusidėvėjimo profilį, kuris naudoja Naudojimo metodą, metodą nustatyti galite įvairiais būdais.</span><span class="sxs-lookup"><span data-stu-id="a1006-107">After you create a depreciation profile that uses the Consumption method, you can set up the method in various ways.</span></span>

## <a name="set-up-and-use-consumption-depreciation"></a><span data-ttu-id="a1006-108">Nustatyti ir naudoti nusidėvėjimą pagal naudojimą</span><span class="sxs-lookup"><span data-stu-id="a1006-108">Set up and use consumption depreciation</span></span>
1.  <span data-ttu-id="a1006-109">**Nusidėvėjimo profilių** puslapyje sukurkite nusidėvėjimo profilį.</span><span class="sxs-lookup"><span data-stu-id="a1006-109">On the **Depreciation profiles** page, create the depreciation profile.</span></span> <span data-ttu-id="a1006-110">Skaičiuojant suvartojimą, nusidėvėjimo profilis turi turėti ID ir pavadinimą, o **Metodo** lauke reikia pasirinkti **Naudojimas**.</span><span class="sxs-lookup"><span data-stu-id="a1006-110">For consumption calculations, the depreciation profile must have an ID and a name, and **Consumption** must be selected in the **Method** field.</span></span>
2.  <span data-ttu-id="a1006-111">**Naudojimo koeficientų** puslapyje nustatykite naudojimo koeficientus.</span><span class="sxs-lookup"><span data-stu-id="a1006-111">On the **Consumption factors** page, set up consumption factors.</span></span> <span data-ttu-id="a1006-112">Kiekvienas naudojimo koeficientas turi turėti ID ir pavadinimą bei naudojimo koeficientą, nurodytą kaip kiekį arba procentą.</span><span class="sxs-lookup"><span data-stu-id="a1006-112">Each consumption factor must have an ID and a name, and a consumption factor that is specified as either a quantity or a percentage.</span></span>
3.  <span data-ttu-id="a1006-113">**Naudojimo vienetų** puslapyje nustatykite naudojimo vienetus.</span><span class="sxs-lookup"><span data-stu-id="a1006-113">On the **Consumption units** page, set up consumption units.</span></span> <span data-ttu-id="a1006-114">Kiekvienas naudojimo vienetas turi turėti ID ir pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="a1006-114">Each consumption unit must have an ID and a name.</span></span> <span data-ttu-id="a1006-115">Nusidėvėjimo vienetai naudojami skaičiuojant nusidėvėjimą pagal naudojimą **Nusidėvėjimo pagal naudojimą** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a1006-115">Depreciation units are used to calculate consumption depreciation on the **Consumption depreciation** page.</span></span> <span data-ttu-id="a1006-116">Vienetų pavyzdžiai: kilometras (km), kilogramas (kg) ir valanda.</span><span class="sxs-lookup"><span data-stu-id="a1006-116">Examples of units are kilometer (km), kilogram (kg), and hour.</span></span>
4.  <span data-ttu-id="a1006-117">**Ilgalaikio turto** puslapyje nustatykite atskirą ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="a1006-117">On the **Fixed assets** page, set up individual fixed assets.</span></span> <span data-ttu-id="a1006-118">Kiekvienam ilgalaikiam turtui parinkite vertinimo modelius ir nusidėvėjimo knygas, turinčius nusidėvėjimo profilius.</span><span class="sxs-lookup"><span data-stu-id="a1006-118">For each fixed asset, select value models and depreciation books that have depreciation profiles.</span></span> <span data-ttu-id="a1006-119">Jei bet kuris jūsų ilgalaikis turtas naudoja nusidėvėjimo profilius, paremtus Naudojimo metodu, turite nustatyti nusidėvėjimo pagal naudojimą vertinimo modelius ar nusidėvėjimo knygas.</span><span class="sxs-lookup"><span data-stu-id="a1006-119">You must set up value models or depreciation books for consumption depreciation if any of your fixed assets use depreciation profiles that are based on the Consumption method.</span></span> <span data-ttu-id="a1006-120">Ši sąranka atliekama arba **Vertinimo modelių** puslapio skirtuke **Nusidėvėjimas**, arba **Nusidėvėjimo profilio** puslapio „FastTab‟**Bendra**.</span><span class="sxs-lookup"><span data-stu-id="a1006-120">This setup is done either on the **Depreciation** tab of the **Value models** page or on the **General** FastTab of the **Depreciation profile** page.</span></span> <span data-ttu-id="a1006-121">Tą patį vertinimo modelį galite naudoti keliems ilgalaikio turto objektams.</span><span class="sxs-lookup"><span data-stu-id="a1006-121">You can use the same value model for multiple fixed assets.</span></span> <span data-ttu-id="a1006-122">Nusidėvėjimo šablonai yra ilgalaikiam turtui parinkto vertinimo modelio arba nusidėvėjimo knygos dalis.</span><span class="sxs-lookup"><span data-stu-id="a1006-122">Depreciation profiles are part of the value model or depreciation book that you select for each fixed asset.</span></span> <span data-ttu-id="a1006-123">Tiesiogiai **Ilgalaikio turto** puslapyje pridėti ar modifikuoti nusidėvėjimo profilių negalima.</span><span class="sxs-lookup"><span data-stu-id="a1006-123">You can't add or modify depreciation profiles directly on the **Fixed assets** page.</span></span> <span data-ttu-id="a1006-124">Modifikuoti nusidėvėjimo profilius galite tik **Nusidėvėjimo knygų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a1006-124">You can modify depreciation profiles only on the **Depreciation books** page.</span></span>
5.  <span data-ttu-id="a1006-125">**Vertinimo modelių** puslapyje arba **Nusidėvėjimo knygų** puslapyje, **Nusidėvėjimo pagal naudojimą** laukų grupėje įveskite informaciją į toliau nurodytus laukus.</span><span class="sxs-lookup"><span data-stu-id="a1006-125">On the **Value models** page or the **Depreciation books** page, in the **Consumption depreciation** field group, enter information in the following fields:</span></span>
    -   <span data-ttu-id="a1006-126">Naudojimo koeficientas</span><span class="sxs-lookup"><span data-stu-id="a1006-126">Consumption factor</span></span>
    -   <span data-ttu-id="a1006-127">Vienetas</span><span class="sxs-lookup"><span data-stu-id="a1006-127">Unit</span></span>
    -   <span data-ttu-id="a1006-128">Nusidėvėjimo vienetai</span><span class="sxs-lookup"><span data-stu-id="a1006-128">Unit depreciation</span></span>
    -   <span data-ttu-id="a1006-129">Įvertintas suvartojimas</span><span class="sxs-lookup"><span data-stu-id="a1006-129">Estimated consumption</span></span>

    <span data-ttu-id="a1006-130">Lauke **Užregistruotas naudojimas** rodomas nusidėvėjimas pagal naudojimą, išreikštas vienetais ir užregistruotas ilgalaikio turto ir vertinimo modelio derinyje arba nusidėvėjimo knygoje.</span><span class="sxs-lookup"><span data-stu-id="a1006-130">The **Posted consumption** field shows the consumption depreciation, in units, that has already been posted either for the combination of the fixed asset and value model, or for the depreciation book.</span></span> <span data-ttu-id="a1006-131">Šio lauko reikšmės rankiniu būdu atnaujinti negalite.</span><span class="sxs-lookup"><span data-stu-id="a1006-131">You can't manually update the value in this field.</span></span>

## <a name="examples"></a><span data-ttu-id="a1006-132">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="a1006-132">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="a1006-133">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="a1006-133">Example 1</span></span>

<span data-ttu-id="a1006-134">Šis naudojimo koeficientas nustatytas sausio 31 d.:</span><span class="sxs-lookup"><span data-stu-id="a1006-134">The following consumption factor is set up for January 31:</span></span>

-   <span data-ttu-id="a1006-135">Kiekis yra 1 000.</span><span class="sxs-lookup"><span data-stu-id="a1006-135">The quantity is 1,000.</span></span>
-   <span data-ttu-id="a1006-136">Nurodyta ilgalaikio turto vieneto nusidėvėjimo kaina yra 1,5.</span><span class="sxs-lookup"><span data-stu-id="a1006-136">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>

<span data-ttu-id="a1006-137">Sausio 31 d. nusidėvėjimo pasiūlymas yra toks: Kiekis x Vieneto nusidėvėjimas 1 000 x 1,5 = 1 500 Jei nurodytas ilgalaikio turto koeficientas yra procento koeficientas, ilgalaikio turto vertinimo modelio kiekis, įvertintas **Įvertinto naudojimo** lauke, yra padauginamas iš nustatyto pasirinktos pabaigos datos procento.</span><span class="sxs-lookup"><span data-stu-id="a1006-137">The depreciation proposal on January 31 is as follows: Quantity × Unit depreciation 1,000 × 1.5 = 1,500 If the factor that is specified for the fixed asset is a percentage factor, the quantity that is estimated in the **Estimated consumption** field for the value model of the fixed asset is multiplied by the percentage that is set up for the selected end date.</span></span> <span data-ttu-id="a1006-138">Gautas kiekis tada yra siūlomas kaip laikotarpio nusidėvėjimo kiekis.</span><span class="sxs-lookup"><span data-stu-id="a1006-138">The resulting quantity is then suggested as the depreciation quantity for the period.</span></span>

### <a name="example-2"></a><span data-ttu-id="a1006-139">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="a1006-139">Example 2</span></span>

<span data-ttu-id="a1006-140">Šis nusidėvėjimo pagal suvartojimą koeficientas nustatytas sausio 31 d.:</span><span class="sxs-lookup"><span data-stu-id="a1006-140">The following factor for consumption depreciation is set up for January 31:</span></span>

-   <span data-ttu-id="a1006-141">Procentinė dalis yra 10 procentų.</span><span class="sxs-lookup"><span data-stu-id="a1006-141">The percentage is 10 percent.</span></span>
-   <span data-ttu-id="a1006-142">Nurodyta ilgalaikio turto vieneto nusidėvėjimo kaina yra 1,5.</span><span class="sxs-lookup"><span data-stu-id="a1006-142">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>
-   <span data-ttu-id="a1006-143">Įvertintas ilgalaikio turto kiekis yra 2 000.</span><span class="sxs-lookup"><span data-stu-id="a1006-143">The estimated quantity of the fixed asset is 2,000.</span></span>

<span data-ttu-id="a1006-144">Sausio 31 d. nusidėvėjimo pasiūlymas yra toks: Įvertintas kiekis x Procentas x Vieneto nusidėvėjimas 2 000 x 0,10 x 1,5 = 300</span><span class="sxs-lookup"><span data-stu-id="a1006-144">The depreciation proposal on January 31 is as follows: Estimated quantity × Percentage × Unit depreciation 2,000 × .10 × 1.5 = 300</span></span>



