---
title: Padengimo parametrai
description: "Bendrasis planavimas naudoja padengimo parametrus prekės poreikiui apskaičiuoti."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fb11a470d98a9742749daaac3244a5bb0d3a689c
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="coverage-settings"></a><span data-ttu-id="72c40-103">Padengimo parametrai</span><span class="sxs-lookup"><span data-stu-id="72c40-103">Coverage settings</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="72c40-104">Bendrasis planavimas naudoja padengimo parametrus prekės poreikiui apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="72c40-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="72c40-105">Galite nurodyti padengimo parametrus keliais būdais:</span><span class="sxs-lookup"><span data-stu-id="72c40-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="72c40-106">Nurodykite padengimo grupės padengimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="72c40-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="72c40-107">Galite sukurti padengimo grupę, kurioje būtų visų su padengimo grupe susijusių produktų parametrai.</span><span class="sxs-lookup"><span data-stu-id="72c40-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="72c40-108">Norėdami sukurti padengimo grupę spustelėkite **Bendrasis planavimas &gt; Sąranka &gt; Padengimas &gt; Padengimo grupės**.</span><span class="sxs-lookup"><span data-stu-id="72c40-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="72c40-109">Padengimo grupę galite susieti su produktu.</span><span class="sxs-lookup"><span data-stu-id="72c40-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="72c40-110">Jei saitas yra konkrečios teritorijos, sandėlio ar produkto dimensijos, naudokite puslapio **Prekės padengimas** lauką **Padengimo grupė**.</span><span class="sxs-lookup"><span data-stu-id="72c40-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="72c40-111">Jei saitas yra bendrasis, neatsižvelgdami į produkto dimensijas, naudokite puslapio **Produkto informacija** „FastTab“ skirtuke **Planas** esančią parinktį **Padengimo grupė**.</span><span class="sxs-lookup"><span data-stu-id="72c40-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="72c40-112">Jei padengimo grupės nesusiejate su produktu, bendrojo planavimo funkcija kaip numatytąją naudoja puslapyje **Bendrojo planavimo parametrai** nurodytą parinktį **Bendroji padengimo grupė**.</span><span class="sxs-lookup"><span data-stu-id="72c40-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="72c40-113">Nurodykite produkto padengimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="72c40-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="72c40-114">Galite sukurti konkretaus produkto padengimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="72c40-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="72c40-115">Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="72c40-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="72c40-116">Pasirinkite produktą, dalyje **Veiksmų sritis** esančio skirtuko **Planas** lauke **Padengimo grupė** spustelėkite **Prekės padengimas**, kad būtų atidarytas puslapis **Prekės padengimas**.</span><span class="sxs-lookup"><span data-stu-id="72c40-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="72c40-117">Jei produktas jau susietas su padengimo grupe, galite nepaisyti padengimo grupės parametrų, naudodami lauką **Nepaisyti**.</span><span class="sxs-lookup"><span data-stu-id="72c40-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="72c40-118">Padengimo parametrams puslapyje**Prekės padengimas** teikiama pirmenybė prieš parametrus puslapyje **Padengimo grupė**.</span><span class="sxs-lookup"><span data-stu-id="72c40-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="72c40-119">Nurodykite produkto padengimo parametrus naudodami vedlį.</span><span class="sxs-lookup"><span data-stu-id="72c40-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="72c40-120">Vedlys yra išsamus instruktorius, padedantis nustatyti pirminius prekės padengimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="72c40-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="72c40-121">Puslapyje **Prekės padengimas** spustelėkite **Vedlys**, kad būtų atidarytas **Prekės padengimo vedlys**.</span><span class="sxs-lookup"><span data-stu-id="72c40-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

-   <span data-ttu-id="72c40-122">Nurodykite dimensijos grupės padengimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="72c40-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="72c40-123">Spustelėkite **Produkto informacijos valdymas &gt; Bendra &gt; Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="72c40-123">Click **Product information management &gt; Common &gt; Released products**.</span></span> <span data-ttu-id="72c40-124">Puslapio **Patvirtinto produkto informacija** skirtuke **Bendra** esančioje grupėje **Administravimas** spustelėkite saitą **Saugojimo dimensijų grupė**.</span><span class="sxs-lookup"><span data-stu-id="72c40-124">On the **Released product detail **page, on the **General** tab, in the **Administration** group, click the **Storage dimension group** link.</span></span> <span data-ttu-id="72c40-125">Puslapyje **Saugojimo dimensijų grupė** pasirinkite lauką **Padengimo planas dimensijomis**, kad sukurtumėte saugojimo dimensijų grupės dimensijos padengimo nustatymus.</span><span class="sxs-lookup"><span data-stu-id="72c40-125">On the **Storage dimension group** page, select the **Coverage plan by dimension** field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="72c40-126">Visose produkto dimensijose, pvz., konfigūracijos, spalvos, dydžio, stiliaus, turi būti pasirinktas laukas **Padengimo planas pagal dimensiją**.</span><span class="sxs-lookup"><span data-stu-id="72c40-126">All product dimensions, such as configuration, color, size, style, must have the **Coverage plan by dimension** field selected.</span></span>



<a name="see-also"></a><span data-ttu-id="72c40-127">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="72c40-127">See also</span></span>
--------

[<span data-ttu-id="72c40-128">Bendrieji planai</span><span class="sxs-lookup"><span data-stu-id="72c40-128">Master plans</span></span>](master-plans.md)




