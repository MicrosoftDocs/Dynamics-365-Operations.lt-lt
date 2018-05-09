---
title: "Produktų konfigūravimas pagal dimensijas"
description: "Produktų konfigūravimas pagal dimensijas nurodo paprastą sprendimą norint kurti daug produkto variantų iš vieno bendrojo produkto ir jo KS."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 18e53494b5cdb49c0bf7e8c311f17bfdbff78b0d
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="dimension-based-product-configuration"></a><span data-ttu-id="5f3fc-103">Produktų konfigūravimas pagal dimensijas</span><span class="sxs-lookup"><span data-stu-id="5f3fc-103">Dimension-based product configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f3fc-104">Produktų konfigūravimas pagal dimensijas nurodo paprastą sprendimą norint kurti daug produkto variantų iš vieno bendrojo produkto ir jo KS.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-104">Dimension-based product configuration represents a simple solution for creating many product variants from a single product master and its bill of materials.</span></span>

<span data-ttu-id="5f3fc-105">Produktų konfigūravimas pagal dimensijas yra viena iš trijų integruotų produktų konfigūravimo technologijų.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-105">Dimension-based product configuration is one of the three built-in product configuration technologies.</span></span> <span data-ttu-id="5f3fc-106">Kitos dvi technologijos yra iš anksto apibrėžti variantai ir konfigūravimas pagal apribojimus.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-106">The two other technologies are predefined variants and constraint-based configuration.</span></span> <span data-ttu-id="5f3fc-107">Visos trys technologijos kaip pradžios tašką naudoja bendrąjį produktą ir naudotojui leidžia kurti daug vieno bendrojo produkto variantų.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-107">All three technologies use a product master as the starting point and allow the user to create many product variants for one product master.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="5f3fc-108">Pagrindinės koncepcijos</span><span class="sxs-lookup"><span data-stu-id="5f3fc-108">Key concepts</span></span>
<span data-ttu-id="5f3fc-109">Produktų konfigūravimas pagal dimensijas paremtas tolesnėmis pagrindinėmis koncepcijomis.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-109">Dimension-based product configuration is based on the following key concepts:</span></span>

-   <span data-ttu-id="5f3fc-110">Bendrieji produktai</span><span class="sxs-lookup"><span data-stu-id="5f3fc-110">Product masters</span></span>
-   <span data-ttu-id="5f3fc-111">Konfigūracijų produkto dimensija</span><span class="sxs-lookup"><span data-stu-id="5f3fc-111">Configuration product dimension</span></span>
-   <span data-ttu-id="5f3fc-112">Konfigūracijų grupės</span><span class="sxs-lookup"><span data-stu-id="5f3fc-112">Configuration groups</span></span>
-   <span data-ttu-id="5f3fc-113">Komplektavimo specifikacijos (KS)</span><span class="sxs-lookup"><span data-stu-id="5f3fc-113">Bill of materials (BOM)</span></span>
-   <span data-ttu-id="5f3fc-114">Konfigūracijos maršrutas</span><span class="sxs-lookup"><span data-stu-id="5f3fc-114">Configuration route</span></span>
-   <span data-ttu-id="5f3fc-115">Konfigūracijos taisyklės</span><span class="sxs-lookup"><span data-stu-id="5f3fc-115">Configuration rules</span></span>

### <a name="product-masters"></a><span data-ttu-id="5f3fc-116">Bendrieji produktai</span><span class="sxs-lookup"><span data-stu-id="5f3fc-116">Product masters</span></span>

<span data-ttu-id="5f3fc-117">Bendrasis produktas yra pradinis bet kokio produktų konfigūravimo proceso taškas.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-117">A product master is the starting point for any product configuration process.</span></span> <span data-ttu-id="5f3fc-118">Norint produktus konfigūruoti pagal dimensijas, reikia bendrojo produkto su šia konkrečia konfigūravimo technologija ir produkto dimensijų grupės, kurioje būtų konfigūracijų produkto dimensija.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-118">For the dimension-based product configuration, you need a product master with this particular configuration technology and a product dimension group that includes the configuration product dimension.</span></span>

### <a name="configuration-product-dimension"></a><span data-ttu-id="5f3fc-119">Konfigūracijų produkto dimensija</span><span class="sxs-lookup"><span data-stu-id="5f3fc-119">Configuration product dimension</span></span>

<span data-ttu-id="5f3fc-120">Konfigūracijų produkto dimensija naudojama indentifikuoti bendrojo produkto su konfigūravimo pagal dimensijas technologija variantams.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-120">The configuration product dimension is used to identify the product variants for a product master with the dimension-based configuration technology.</span></span> <span data-ttu-id="5f3fc-121">Konfigūracijos dimensijos reikšmę įveda naudotojas, ir ji turėtų padėti identifikuoti atskirus produktų variantus.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-121">The configuration dimension value is entered by the user and should help to identify the individual product variants.</span></span>

### <a name="configuration-groups"></a><span data-ttu-id="5f3fc-122">Konfigūracijų grupės</span><span class="sxs-lookup"><span data-stu-id="5f3fc-122">Configuration groups</span></span>

<span data-ttu-id="5f3fc-123">Konfigūracijos grupės apibrėžiamos centrinėje saugykloje ir gali būti naudojamos su visais produktų konfigūravimo pagal dimensijas modeliais.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-123">Configuration groups are defined in a central repository and can be used for all dimension-based product configuration models.</span></span> <span data-ttu-id="5f3fc-124">Konfigūracijos grupės susietos su atskiromis KS eilutėmis ir kartu sudaro tarpusavyje nesuderinamų eilučių grupę.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-124">Configuration groups are associated to the individual BOM lines and hold together a group of lines that are mutually exclusive.</span></span> <span data-ttu-id="5f3fc-125">Tai reiškia, kad vienam produkto variantui galima parinkti tik vieną grupės eilutę.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-125">This means that only one line in a group can be selected for a single product variant.</span></span>

### <a name="bill-of-materials-bom"></a><span data-ttu-id="5f3fc-126">Komplektavimo specifikacijos (KS)</span><span class="sxs-lookup"><span data-stu-id="5f3fc-126">Bill of materials (BOM)</span></span>

<span data-ttu-id="5f3fc-127">KS – tai produktų konfigūravimo pagal dimensijas kūrimo blokai.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-127">The BOM represent the building blocks for a dimension-based product configuration.</span></span> <span data-ttu-id="5f3fc-128">Ji turi apimti visus skirtingus produktus, kuriuos galima naudoti su bet kuriuo produkto variantu.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-128">It must include all the different products that can be used in any product variant.</span></span> <span data-ttu-id="5f3fc-129">Kiekviena KS eilutė gali nurodyti į konfigūracijos grupę.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-129">Each line in the BOM can reference a configuration group.</span></span> <span data-ttu-id="5f3fc-130">Jei eilutė nenurodo į konfigūracijos grupę, ji bus įtraukta į visus produkto variantus.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-130">If a line doesn’t reference a configuration group, it will be included in all product variants.</span></span>

### <a name="configuration-route"></a><span data-ttu-id="5f3fc-131">Konfigūracijos maršrutas</span><span class="sxs-lookup"><span data-stu-id="5f3fc-131">Configuration route</span></span>

<span data-ttu-id="5f3fc-132">Konfigūracijos maršrutas nustato konfigūracijos grupių seką: kaip jos bus rodomos naudotojui vykdant produktų konfigūravimą.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-132">The configuration route determines the sequence of the configuration groups, as they will be displayed to the user during the product configuration process.</span></span>

### <a name="configuration-rules"></a><span data-ttu-id="5f3fc-133">Konfigūracijos taisyklės</span><span class="sxs-lookup"><span data-stu-id="5f3fc-133">Configuration rules</span></span>

<span data-ttu-id="5f3fc-134">Konfigūracijos taisyklės – tai mechanizmas, skirtas užtikrinti, kad produktas, įtrauktas į vieną KS konfigūracijos grupę, lemtų produkto kitoje tos pačios KS konfigūracijos grupėje išėmimą arba įtraukimą.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-134">The configuration rules represent a mechanism for ensuring that a product included in one configuration group in a BOM enforces either an inclusion or an exclusion of a product in a different configuration group in the same BOM.</span></span>

## <a name="product-modeling-process"></a><span data-ttu-id="5f3fc-135">Produkto modeliavimo procesas</span><span class="sxs-lookup"><span data-stu-id="5f3fc-135">Product modeling process</span></span>
<span data-ttu-id="5f3fc-136">Natūrali dimensijomis paremto produkto modelio kūrimo seka pradedama apibrėžiant aktualias konfigūracijos grupes.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-136">The natural sequence for building a product model for a dimension-based product starts with defining the relevant configuration groups.</span></span> <span data-ttu-id="5f3fc-137">Svarbu užtikrinti, kad visi produktai, kurie bus naudojami KS, išleisti į įmonę, kuriai sukurtas produkto modelis.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-137">It is important to ensure that all products which will be used in the BOM have been released to the company that the product model is built for.</span></span> <span data-ttu-id="5f3fc-138">Pasirūpinęs šiais kūrimo blokais, naudotojas gali kurti KS ir visoms aktualioms KS eilutėms priskirti konfigūracijos grupes.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-138">With these building blocks in place, the user can create the BOM and assign configuration groups to all relevant BOM lines.</span></span> <span data-ttu-id="5f3fc-139">Kai KS baigta, galima apibrėžti konfigūracijos maršrutą, kad konfigūracijos grupės būtų surikiuotos tinkama tvarka.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-139">When the BOM is complete, a configuration route can be defined for ordering the configuration groups in the proper sequence.</span></span> <span data-ttu-id="5f3fc-140">[![Dimensijomis paremtų produktų modeliavimo procesas](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Jei skirtingose konfigūracijos grupėse yra tam tikrų produktų, kuriuos arba reikia naudoti kartu, arba nereikia, galite sukurti konfigūracijos taisykles, kurios užtikrins šiuos produktų ryšius.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-140">[![Dimension-based product modeling process](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) If there are certain products from different configuration groups that either must or must not be used together, you can create configuration rules that will enforce these product relationships.</span></span> <span data-ttu-id="5f3fc-141">Kai, naudojant KS versiją, KS susieta su dimensijomis paremtu bendruoju produktu, ir jie abu patvirtinti bei suaktyvinti, galite kurti produktų konfigūracijų ir įvesti kiekvienos konfigūracijos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-141">After the BOM has been tied together with a dimension-based product master through a BOM version and both have been approved and activated, you can create product configurations and enter a name for each configuration.</span></span> <span data-ttu-id="5f3fc-142">Konfigūracijas galima apibrėžti prieš sugeneruojant bet kokias operacijas, arba tai galima atlikti atsiradus tam tikros konfigūracijos poreikiui.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-142">The configurations can be defined before any transactions are generated or it can be done when the need for a certain configuration occurs.</span></span>

### <a name="suggested-use"></a><span data-ttu-id="5f3fc-143">Rekomenduojama paskirtis</span><span class="sxs-lookup"><span data-stu-id="5f3fc-143">Suggested use</span></span>

<span data-ttu-id="5f3fc-144">Konfigūravimo pagal dimensijas technologiją geriausia naudoti su ribotos įvairovės produktais su standartinių produkto dimensijų dydžio, spalvos, stiliaus deriniu ir kai konfigūracija netinka identifikuoti konkrečiam produkto variantui.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-144">The dimension-based configuration technology is best used for products with limited variability and the combination of the standard product dimensions size, color, style, and configuration is unsuitable for identifying a specific product variant.</span></span> <span data-ttu-id="5f3fc-145">Pavyzdys galėtų būti dviratis, kurio nurodytas rėmo aukštis, ratų dydis, stabdžių tipai ir skirtingos pavaros.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-145">An example could be bicycle with frame height, wheel size, brake types, and different gears.</span></span>

### <a name="next-step"></a><span data-ttu-id="5f3fc-146">Kitas veiksmas</span><span class="sxs-lookup"><span data-stu-id="5f3fc-146">Next step</span></span> 

<span data-ttu-id="5f3fc-147">Toliau nurodyti aštuoni užduočių vedliai išvardyti tokia tvarka, kokia juos turite atlikti.</span><span class="sxs-lookup"><span data-stu-id="5f3fc-147">The following eight task guides are listed in the order in which you should complete them.</span></span> 

1.  [<span data-ttu-id="5f3fc-148">Dimensijomis pagrįsto bendrojo produkto kūrimas (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="5f3fc-148">Create a dimension-based product master (Task guide)</span></span>](tasks/create-dimension-based-product-master.md)
2.  [<span data-ttu-id="5f3fc-149">Dimensijomis pagrįsto bendrojo produkto išleidimas (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="5f3fc-149">Release a dimension-based product master (Task guide)</span></span>](tasks/release-dimension-based-product-master.md)
3.  [<span data-ttu-id="5f3fc-150">Pagrindinė išleisto bendrojo produkto sąranka (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="5f3fc-150">Complete basic setup of a released product master (Task guide)</span></span>](tasks/complete-basic-setup-released-product-master.md)
4.  [<span data-ttu-id="5f3fc-151">Konfigūracijų grupių apibrėžimas (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="5f3fc-151">Define configuration groups (Task guide)</span></span>](tasks/define-configuration-groups.md)
5.  [<span data-ttu-id="5f3fc-152">Dimensijomis paremto bendrojo produkto komplektavimo specifikacijos kūrimas (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="5f3fc-152">Create a bill of materials for a dimension-based product master (Task guide)</span></span>](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [<span data-ttu-id="5f3fc-153">Konfigūracijų maršrutų apibrėžimas (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="5f3fc-153">Define configuration routes (Task guide)</span></span>](tasks/define-configuration-route.md)
7.  [<span data-ttu-id="5f3fc-154">Konfigūravimo taisyklių kūrimas (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="5f3fc-154">Create configuration rules (Task guide)</span></span>](tasks/create-configuration-rules.md)
8.  [<span data-ttu-id="5f3fc-155">Konfigūracijų pagal dimensijas kūrimas (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="5f3fc-155">Create dimension-based configurations (Task guide)</span></span>](tasks/create-dimension-based-configurations.md)


