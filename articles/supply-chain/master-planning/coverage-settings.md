---
title: Padengimo parametrai
description: Šioje temoje pateikiama informacija apie padengimo parametrus, kurie bendrojo planavimo metu naudojami prekių poreikiui skaičiuoti.
author: roxanadiaconu
manager: AnnBe
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a63184852751bb65fb7e80d721f8c48fd847609
ms.sourcegitcommit: edfd805356894710488ce07cb1c89313f448b222
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2019
ms.locfileid: "1998976"
---
# <a name="coverage-settings"></a><span data-ttu-id="425ce-103">Padengimo parametrai</span><span class="sxs-lookup"><span data-stu-id="425ce-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="425ce-104">Bendrasis planavimas naudoja padengimo parametrus prekės poreikiui apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="425ce-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="425ce-105">Galite nurodyti padengimo parametrus keliais būdais:</span><span class="sxs-lookup"><span data-stu-id="425ce-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="425ce-106">Nurodykite padengimo grupės padengimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="425ce-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="425ce-107">Galite sukurti padengimo grupę, kurioje būtų visų su padengimo grupe susijusių produktų parametrai.</span><span class="sxs-lookup"><span data-stu-id="425ce-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="425ce-108">Norėdami sukurti padengimo grupę, eikite į **Bendrasis planavimas &gt; Sąranka &gt; Padengimas &gt; Padengimo grupės**.</span><span class="sxs-lookup"><span data-stu-id="425ce-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="425ce-109">Padengimo grupę galite susieti su produktu.</span><span class="sxs-lookup"><span data-stu-id="425ce-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="425ce-110">Jei saitas yra konkrečios teritorijos, sandėlio ar produkto dimensijos, naudokite puslapio **Prekės padengimas** lauką **Padengimo grupė**.</span><span class="sxs-lookup"><span data-stu-id="425ce-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="425ce-111">Jei saitas yra bendrasis, neatsižvelgdami į produkto dimensijas, naudokite puslapio **Produkto informacija** sparčiajame skirtuke **Planas** esantį lauką **Padengimo grupė**.</span><span class="sxs-lookup"><span data-stu-id="425ce-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="425ce-112">Pagal numatytuosius parametrus, jei padengimo grupės nesusiejate su produktu, bendrojo planavimo funkcija kaip numatytąją naudoja puslapyje **Bendrojo planavimo parametrai** nurodytą parinktį Bendroji padengimo grupė.</span><span class="sxs-lookup"><span data-stu-id="425ce-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="425ce-113">Nurodykite produkto padengimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="425ce-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="425ce-114">Galite sukurti konkretaus produkto padengimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="425ce-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="425ce-115">Eikite į **Produkto informacijos valdymas &gt; Produktai &gt; Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="425ce-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="425ce-116">Pasirinkite produktą ir Veiksmų srities skirtuko **Planas** lauke **Padengimo** grupėje pasirinkite **Prekės padengimas**, kad būtų atidarytas puslapis **Prekės padengimas**.</span><span class="sxs-lookup"><span data-stu-id="425ce-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="425ce-117">Jei produktas jau susietas su padengimo grupe, galite nepaisyti padengimo grupės parametrų, naudodami lauką **Nepaisyti**.</span><span class="sxs-lookup"><span data-stu-id="425ce-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="425ce-118">Padengimo parametrams puslapyje**Prekės padengimas** teikiama pirmenybė prieš parametrus puslapyje **Padengimo grupė**.</span><span class="sxs-lookup"><span data-stu-id="425ce-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="425ce-119">Nurodykite produkto padengimo parametrus naudodami vedlį.</span><span class="sxs-lookup"><span data-stu-id="425ce-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="425ce-120">Vediklis nuosekliai pademonstruos pagrindinių prekės padengimo parametrų sąrankos procesą.</span><span class="sxs-lookup"><span data-stu-id="425ce-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="425ce-121">Veiksmų srities puslapyje **Prekės padengimas** pasirinkite **Vedlys**, kad būtų atidarytas **Prekės padengimo vedlys**.</span><span class="sxs-lookup"><span data-stu-id="425ce-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="425ce-122">Nurodykite dimensijos grupės padengimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="425ce-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="425ce-123">Eikite į **Produkto informacijos valdymas &gt; Produktai &gt; Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="425ce-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="425ce-124">Puslapio **Patvirtinto produkto informacija** sparčiajame skirtuke **Bendra** esančioje sekcijoje **Administravimas** pasirinkite saitą lauke **Saugojimo dimensijų grupė**.</span><span class="sxs-lookup"><span data-stu-id="425ce-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="425ce-125">Puslapyje **Saugojimo dimensijų grupės** pasirinkite žymės laukelį **Padengimo planas dimensijomis**, kad sukurtumėte saugojimo dimensijų grupės dimensijos padengimo nustatymus.</span><span class="sxs-lookup"><span data-stu-id="425ce-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="425ce-126">Visose produkto dimensijose, pvz., konfigūracijos, spalvos, dydžio, stiliaus, turi būti pasirinktas laukas **Padengimo planas pagal dimensiją**.</span><span class="sxs-lookup"><span data-stu-id="425ce-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>


## <a name="coverage-codes"></a><span data-ttu-id="425ce-127">Padengimo kodai</span><span class="sxs-lookup"><span data-stu-id="425ce-127">Coverage codes</span></span>

<span data-ttu-id="425ce-128">Bendrąjį planavimą galima konfigūruoti, kad būtų naudojami skirtingi papildymo metodai.</span><span class="sxs-lookup"><span data-stu-id="425ce-128">Master planning can be configured to use different replenishment methods.</span></span> <span data-ttu-id="425ce-129">Papildymo metodai ar partijų dydžio nustatymo metodai yra sistemos naudojami metodai, siekiant nustatyti įsigytų arba pagamintų prekių paketo dydį.</span><span class="sxs-lookup"><span data-stu-id="425ce-129">The replenishment methods or lot-sizing methods are the techniques used by the system to determine the batch size for purchased or produced items.</span></span> 

<span data-ttu-id="425ce-130">Kiekvienam papildymo metodui priskiriamas vienas toliau pateiktų padengimo kodų.</span><span class="sxs-lookup"><span data-stu-id="425ce-130">Each replenishment method is assigned one of the following coverage codes:</span></span>

- <span data-ttu-id="425ce-131">**Rankinis** – partijos dydžio nustatymo metodas, kai sistema nenurodo prekės pirkimo, perkėlimo ar gamybos užsakymų.</span><span class="sxs-lookup"><span data-stu-id="425ce-131">**Manual** - The lot-sizing method where the system does not suggest purchased, transfer, or production orders for the item.</span></span> <span data-ttu-id="425ce-132">Prekės planuotojas bus atsakingas už būtinų prekės papildymo užsakymų kūrimą.</span><span class="sxs-lookup"><span data-stu-id="425ce-132">The planner for the item will be in charge of creating the required orders for the replenishment of the item.</span></span>
- <span data-ttu-id="425ce-133">**Pagal poreikius** – partijos dydžio nustatymo metodas, pagal kurį sistema sukuria suplanuotą pirkimo, perkėlimo ar gamybos užsakymą kiekvienam prekės reikalavimui.</span><span class="sxs-lookup"><span data-stu-id="425ce-133">**Per requirement** - The lot-sizing method in which the system creates a planned purchase, transfer, or production order per requirement for the item.</span></span> <span data-ttu-id="425ce-134">Tai dažniausiai naudojama brangiems objektams su kintama paklausa.</span><span class="sxs-lookup"><span data-stu-id="425ce-134">This is generally used for expensive items with intermittent demand.</span></span>  
- <span data-ttu-id="425ce-135">**Per laikotarpį** – partijos dydžio nustatymo metodas, kuris sujungia visą laikotarpio paklausą į vieną prekės užsakymą.</span><span class="sxs-lookup"><span data-stu-id="425ce-135">**Per period** - The lot-sizing method that combines all the demand for a period into one order for the item.</span></span> <span data-ttu-id="425ce-136">Užsakymas bus suplanuotas pirmai laikotarpio dienai, o jo kiekis patenkins grynuosius poreikius nustatyto laikotarpio metu.</span><span class="sxs-lookup"><span data-stu-id="425ce-136">The order will be planned for the first day of the period and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="425ce-137">Laikotarpis pradedamas nuo pirmo prekės poreikio ir apima nustatytą laiko trukmę.</span><span class="sxs-lookup"><span data-stu-id="425ce-137">The period starts with the first demand of the item and covers the defined length in time.</span></span> <span data-ttu-id="425ce-138">Kitas laikotarpis prasidės nuo kitų prekės reikalavimų.</span><span class="sxs-lookup"><span data-stu-id="425ce-138">The next period will start with the next requirements of the item.</span></span>
- <span data-ttu-id="425ce-139">**Min./maks.** – partijos dydžio nustatymo metodas, kuriame yra atsargų papildymas iki tam tikro lygio, kai prognozuojama, kad turimos atsargos yra žemiau ribinės reikšmės.</span><span class="sxs-lookup"><span data-stu-id="425ce-139">**Min/Max** - The lot-sizing method that contains the replenishment of inventory up to a certain level when the predicted on-hand is below a threshold.</span></span> <span data-ttu-id="425ce-140">Papildymo kiekis bus skirtumas tarp maksimalaus lygio ir prognozuojamo turimų atsargų lygio.</span><span class="sxs-lookup"><span data-stu-id="425ce-140">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="425ce-141">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="425ce-141">Additional resources</span></span>

[<span data-ttu-id="425ce-142">Bendrieji planai</span><span class="sxs-lookup"><span data-stu-id="425ce-142">Master plans</span></span>](master-plans.md)
