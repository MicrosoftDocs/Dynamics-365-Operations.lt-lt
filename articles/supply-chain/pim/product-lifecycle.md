---
title: Produkto ciklo būsenos apžvalga
description: Produkto ciklo būsena nurodo išleisto produkto arba produkto varianto ciklo būseną.
author: cvocph
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 20d472c399c75dbbef5e197e8f7f495e81b14ca2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980869"
---
# <a name="product-lifecycle-state-overview"></a><span data-ttu-id="87ad5-103">Produkto ciklo būsenos apžvalga</span><span class="sxs-lookup"><span data-stu-id="87ad5-103">Product lifecycle state overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87ad5-104">Produkto ciklo būsena nurodo išleisto produkto arba produkto varianto ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="87ad5-104">A product lifecycle state documents the lifecycle state of a released product or product variant.</span></span> <span data-ttu-id="87ad5-105">Produkto ciklo būsenas apibrėžia vartotojas, paprastai – produktų vadovas arba produktų bendrųjų duomenų vadovas.</span><span class="sxs-lookup"><span data-stu-id="87ad5-105">Product lifecycle states are defined by the user, typically a product manager or a product master data manager.</span></span> <span data-ttu-id="87ad5-106">Konkrečius verslo procesus, pvz., bendrąjį planavimą, gali paveikti konkreti ciklo būsena.</span><span class="sxs-lookup"><span data-stu-id="87ad5-106">Specific business processes, such as master planning, can be affected by a specific lifecycle state.</span></span>   

<span data-ttu-id="87ad5-107">Išleistą produktą arba produkto variantą galima susieti su produkto ciklo būsena, kuri nurodo, kokia yra esama konkretaus produkto arba varianto būsena.</span><span class="sxs-lookup"><span data-stu-id="87ad5-107">A released product or product variant can be associated with a product lifecycle state that documents in which lifecycle state a specific product or variant is currently in.</span></span> <span data-ttu-id="87ad5-108">Galite nurodyti bet kokį produkto ciklo būsenų skaičių, priskirdami būsenos pavadinimą ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="87ad5-108">You can define any number of product lifecycle states by assigning a state name and description.</span></span> <span data-ttu-id="87ad5-109">Galite pasirinkti vieną ciklo būseną kaip numatytąją naujų išleistų produktų būseną.</span><span class="sxs-lookup"><span data-stu-id="87ad5-109">You can select one lifecycle state as the default state for new released products.</span></span> <span data-ttu-id="87ad5-110">Išleisto produkto variantai perima produkto ciklo būseną iš atitinkamo išleisto bendrojo produkto, kai jie sukuriami.</span><span class="sxs-lookup"><span data-stu-id="87ad5-110">Released product variants inherit their product lifecycle state from their released product master on creation.</span></span> <span data-ttu-id="87ad5-111">Keičiant išleisto bendrojo produkto ciklo būseną galima atnaujinti visus esamus variantus, kurių pradinė būsena tokia pati.</span><span class="sxs-lookup"><span data-stu-id="87ad5-111">When changing the lifecycle state on a released product master, you can choose to update all existing variants that have the same original state.</span></span>  

## <a name="create-a-new-product-lifecycle-state"></a><span data-ttu-id="87ad5-112">Naujos produkto ciklo būsenos kūrimas</span><span class="sxs-lookup"><span data-stu-id="87ad5-112">Create a new product lifecycle state</span></span> 

- <span data-ttu-id="87ad5-113">Norėdami kurti naują produkto ciklo būseną, paleiskite arba perskaitykite užduočių vedlį **Naujos produkto ciklo būsenos kūrimas**.</span><span class="sxs-lookup"><span data-stu-id="87ad5-113">To create a new product lifecycle state, play or read the task guide **Create a new product lifecycle state**.</span></span> 

-  <span data-ttu-id="87ad5-114">Norėdami kurti numatytąją produkto ciklo būseną, paleiskite arba perskaitykite užduočių vedlį **Numatytosios produkto ciklo būsenos kūrimas**.</span><span class="sxs-lookup"><span data-stu-id="87ad5-114">To create a default product lifecycle state, play or read the task guide **Create a default product lifecycle state**.</span></span>   

## <a name="associate-product-lifecycle-states-to-released-products"></a><span data-ttu-id="87ad5-115">Produkto ciklo būsenos susiejimas su išleistais produktais</span><span class="sxs-lookup"><span data-stu-id="87ad5-115">Associate product lifecycle states to released products</span></span>  

<span data-ttu-id="87ad5-116">Yra keli būdai, kaip galima susieti produkto ciklo būseną su išleistais produktais arba produkto variantais.</span><span class="sxs-lookup"><span data-stu-id="87ad5-116">There are multiple ways to associate a product lifecycle state to released products or product variants.</span></span>

-  <span data-ttu-id="87ad5-117">Kuriant naują išleistą produktą, numatytoji **Produkto ciklo būsena** priskiriama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="87ad5-117">On creation of a new released product, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="87ad5-118">Išleidžiant produktą į juridinį subjektą, numatytoji **Produkto ciklo būsena** priskiriama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="87ad5-118">On release of a product to a legal entity, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="87ad5-119">Išleidžiant produkto variantą į juridinį subjektą, **Produkto ciklo būsena**, susieta su išleistu bendruoju produktu šiame juridiniame subjekte, automatiškai priskiriama naujam variantui.</span><span class="sxs-lookup"><span data-stu-id="87ad5-119">On release of a product variant to a legal entity, the **Product lifecycle state** associated to the released product master in this legal entity is automatically assigned to the new variant.</span></span> 

<span data-ttu-id="87ad5-120">Galite neautomatiškai atnaujinti produkto ciklo būseną, naudodami:</span><span class="sxs-lookup"><span data-stu-id="87ad5-120">You can manually update the product lifecycle state by using:</span></span> 

-    <span data-ttu-id="87ad5-121">sąrašo puslapį **Išleisti produktai** arba **Informacijos rodinys**;</span><span class="sxs-lookup"><span data-stu-id="87ad5-121">The **Released products** list page or **Details view**.</span></span> 
-  <span data-ttu-id="87ad5-122">sąrašo puslapį **Išleisti produkto variantai** arba **Informacijos rodinys**.</span><span class="sxs-lookup"><span data-stu-id="87ad5-122">The **Released product variants** list page or **Details view**.</span></span> 
-  <span data-ttu-id="87ad5-123">Raskite pasenusius produktus arba produkto variantus pagal paklausą ir susiekite ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="87ad5-123">Find the obsolete products or product variants based on demand and associate a lifecycle state.</span></span>  

<span data-ttu-id="87ad5-124">Norėdami išsamesnės informacijos apie tai, kaip susieti produkto ciklo būsenas, paleiskite arba perskaitykite du toliau nurodytus užduočių vedlius.</span><span class="sxs-lookup"><span data-stu-id="87ad5-124">For detailed information about how to associate product lifecycle states, play or read the following two task guides.</span></span>

-  <span data-ttu-id="87ad5-125">Norėdami susieti produkto ciklo būseną su išleistu bendruoju produktu, paleiskite arba perskaitykite užduočių vedlį **Produkto ciklo būsenos priskyrimas išleistam bendrajam produktui**.</span><span class="sxs-lookup"><span data-stu-id="87ad5-125">To associate a product lifecycle state to a released product master, play or read the task guide **Assign a product lifecycle state to a released product master**.</span></span> 

-  <span data-ttu-id="87ad5-126">Norėdami susieti produkto ciklo būseną su išleistu produktu, paleiskite arba perskaitykite užduočių vedlį **Produkto ciklo būsenos priskyrimas išleistam produktui**.</span><span class="sxs-lookup"><span data-stu-id="87ad5-126">To associate a product lifecycle state to a release product, play or read the task guide **Assign a product lifecycle state to a released product**.</span></span> 

## <a name="impact-on-master-planning"></a><span data-ttu-id="87ad5-127">Poveikis bendrajam planavimui</span><span class="sxs-lookup"><span data-stu-id="87ad5-127">Impact on master planning</span></span> 

<span data-ttu-id="87ad5-128">Produkto ciklo būsena turi tik vieną kontrolės žymę: **Galima planuoti**.</span><span class="sxs-lookup"><span data-stu-id="87ad5-128">The product lifecycle state has only one control flag: **Is active for planning**.</span></span> <span data-ttu-id="87ad5-129">Pagal numatytuosius parametrus šis parametras nustatytas į parinktį **Taip** visose sukurtose produkto ciklo būsenose, bet galima nustatyti parinktį **Ne**.</span><span class="sxs-lookup"><span data-stu-id="87ad5-129">By default, this is set to **Yes** for all created product lifecycle states, but it can be changed to **No**.</span></span> <span data-ttu-id="87ad5-130">Nustačius **Ne**, susieti išleisti produktai arba išleisti produkto variantai yra:</span><span class="sxs-lookup"><span data-stu-id="87ad5-130">When set to **No**, the associated released products or released product variants are:</span></span> 

-  <span data-ttu-id="87ad5-131">neįtraukiami į bendrąjį planavimą;</span><span class="sxs-lookup"><span data-stu-id="87ad5-131">Excluded from master planning.</span></span> 
-  <span data-ttu-id="87ad5-132">neįtraukiami į KS lygio skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="87ad5-132">Excluded from BOM-level calculation.</span></span> 

<span data-ttu-id="87ad5-133">Daugiau informacijos apie tai, kaip naudoti produkto ciklo būseną norint pašalinti produktus iš bendrojo planavimo ir lygio KS skaičiavimo, paleiskite arba perskaitykite užduočių vedlį **Produkto ciklo būsenos kūrimas norint pašalinti produktus iš bendrojo planavimo**.</span><span class="sxs-lookup"><span data-stu-id="87ad5-133">For detailed information about how to use product lifecycle state to exclude products from master planning and BOM-level calculation, play or read the task guide **Create a product lifecycle state to exclude products from Master planning**.</span></span>

> [!NOTE]
> <span data-ttu-id="87ad5-134">Siekiant padidinti efektyvumą, labai rekomenduojame susieti visus pasenusius išleistus produktus arba produkto variantus, ypač dirbant su vienkartinio produkto konfigūracijos variantais, su produkto ciklo būsena, kuri bendrajame planavime yra išjungta.</span><span class="sxs-lookup"><span data-stu-id="87ad5-134">For performance reasons, it is highly recommended to associate all obsolete released products or product variants, especially when working with non-reusable product configuration variants, with a product lifecycle state that is deactivated for master planning.</span></span>  

## <a name="default-migration-import-and-export"></a><span data-ttu-id="87ad5-135">Numatytasis perėjimas, importavimas ir eksportavimas</span><span class="sxs-lookup"><span data-stu-id="87ad5-135">Default migration, import, and export</span></span> 

<span data-ttu-id="87ad5-136">Produktų ciklo būsenas palaiko duomenų objektai ir ciklo būseną galima nustatyti į kintamąją būseną naudojant arba išleisto produkto duomenų objektą, arba išleisto varianto duomenų objektą.</span><span class="sxs-lookup"><span data-stu-id="87ad5-136">The product lifecycle states are supported by data entities, and the lifecycle state can be set to a variable state through either the released product data entity or the released variant data entity.</span></span>

## <a name="find-obsolete-products-and-products-variants"></a><span data-ttu-id="87ad5-137">Pasenusių produktų ir produktų variantų radimas</span><span class="sxs-lookup"><span data-stu-id="87ad5-137">Find obsolete products and products variants</span></span> 

<span data-ttu-id="87ad5-138">Galite vykdyti modeliavimo analizę, norėdami rasti pasenusius išleistus produktus arba produkto variantus ir tada atnaujinti jų produkto ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="87ad5-138">You can run a simulation analysis to find the obsolete released products or product variants and then update their product lifecycle status.</span></span> <span data-ttu-id="87ad5-139">Norėdami rasti pasenusius produktus, paleiskite arba perskaitykite užduočių vedlį **Pasenusių produkto variantų radimas ir produkto ciklo būsenos priskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="87ad5-139">To find obsolete products, play and read the task guide **Find obsolete product variants and assign a product lifecycle state**.</span></span> <span data-ttu-id="87ad5-140">Šiame užduočių vedlyje parodoma, kaip rasti pasenusius išleistus produktus arba produkto variantus ir kaip susieti produkto ciklo būseną su pasenusiais produktais.</span><span class="sxs-lookup"><span data-stu-id="87ad5-140">This task guide shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="87ad5-141">Jame taip pat parodoma, kaip peržiūrėti modeliavimo rezultatus ir įvertinti, kiek produktų ir produkto variantų bus susieti su nauja produkto ciklo būsena vykdant naujinimą be modeliavimo.</span><span class="sxs-lookup"><span data-stu-id="87ad5-141">It also shows hot to view the simulation results and assess how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

<span data-ttu-id="87ad5-142">Vykdydami analizę modeliavimo režimu, produktai ir produkto variantai, identifikuoti kaip pasenę, rodomi konkrečioje formoje, kurioje juos galima lengvai peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="87ad5-142">By running the analysis in a simulation mode, the products and product variants identified as obsolete are displayed in a specific form, where they can easily be reviewed.</span></span> <span data-ttu-id="87ad5-143">Atliekant analizę ieškoma operacijų ir konkrečių bendrųjų duomenų, kad būtų identifikuoti produktai, kurių poreikio nėra per kintantį laikotarpį ir iš poreikio negalima generuoti jokių bendrųjų duomenų.</span><span class="sxs-lookup"><span data-stu-id="87ad5-143">The analysis searches for transactions and specific master data to identify products that have no demand within a variable period and no master data that can result in demand.</span></span> <span data-ttu-id="87ad5-144">Naujų išleistų produktų per kintantį laikotarpį galima neįtraukti į analizę.</span><span class="sxs-lookup"><span data-stu-id="87ad5-144">New released products within a variable period can be excluded from the analysis.</span></span> <span data-ttu-id="87ad5-145">Kai analizės modeliavimas pateikia numatytąjį rezultatą, vartotojas gali vykdyti analizę ir nustatyti visų produktų, kurie analizėje nurodyti kaip pasenę, naują produkto ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="87ad5-145">When the analysis simulation returns the expected result, the user can run the analysis and set a new product lifecycle state to all products identified as obsolete by the analysis.</span></span>  

> [!NOTE]
> <span data-ttu-id="87ad5-146">Atminkite, kad visą analizę ir naujinimą reikia atlikti tame pačiame juridiniame subjekte.</span><span class="sxs-lookup"><span data-stu-id="87ad5-146">Note that all analysis and updates must be done within the same legal entity.</span></span>  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a><span data-ttu-id="87ad5-147">Išleistų produktų arba produkto variantų pasirinkimo ir naujinimo kriterijai</span><span class="sxs-lookup"><span data-stu-id="87ad5-147">Criteria to select and update released products or product variants</span></span> 

<span data-ttu-id="87ad5-148">Naudokite toliau nurodytus išleistų produktų arba produkto variantų pasirinkimo ir naujinimo kriterijus.</span><span class="sxs-lookup"><span data-stu-id="87ad5-148">Use the following criteria to select and update the released products and product variants:</span></span> 

-    <span data-ttu-id="87ad5-149">Produkto arba produkto varianto produkto ciklo būsena turi skirtis nuo naujos norimos būsenos.</span><span class="sxs-lookup"><span data-stu-id="87ad5-149">The product lifecycle state of the product or product variant must be different from the new desired state.</span></span> 
-  <span data-ttu-id="87ad5-150">Produktas arba produkto variantas buvo sukurtas prieš keletą dienų atsižvelgiant į dienų skaičių, kuris įvestas pasirinkimo dialogo lange.</span><span class="sxs-lookup"><span data-stu-id="87ad5-150">The product or product variant was created some days ago based on the number of days that you enter in the selection dialog box.</span></span> 
-  <span data-ttu-id="87ad5-151">Nėra produkto arba produkto varianto atvirų gamybos užsakymų (= būsena < baigėsi).</span><span class="sxs-lookup"><span data-stu-id="87ad5-151">There are no open production orders (= status < ended) for the product or product variant.</span></span> 
-  <span data-ttu-id="87ad5-152">Nėra produkto arba produkto varianto atvirų atsargų operacijų (= būsena išdavimas ReservPhysical į QuotationIssue arba būsenos gavimas Registrered į QuotationReceipt).</span><span class="sxs-lookup"><span data-stu-id="87ad5-152">There are no open inventory transactions (= status issue ReservPhysical to QuotationIssue or status receipt Registrered to QuotationReceipt) for the product or product variant.</span></span> 
-  <span data-ttu-id="87ad5-153">Nėra produkto arba produkto varianto atsargų operacijų per paskutines dienas.</span><span class="sxs-lookup"><span data-stu-id="87ad5-153">There are no inventory transactions within the last number of days for the product or product variant.</span></span> 
-  <span data-ttu-id="87ad5-154">Nėra produkto arba produkto varianto ateities poreikio arba tiekimo prognozės.</span><span class="sxs-lookup"><span data-stu-id="87ad5-154">There is no future demand or supply forecast for the product or product variant.</span></span>  
-  <span data-ttu-id="87ad5-155">Produkto arba produkto varianto minimalus atsargų lygis nenustatytas prekės padengime.</span><span class="sxs-lookup"><span data-stu-id="87ad5-155">No minimum stock level has been set in item coverage for the product or product variant.</span></span> 
-  <span data-ttu-id="87ad5-156">Nėra produkto arba produkto varianto aktyvių fiksuoto kiekio „kanban“ taisyklių.</span><span class="sxs-lookup"><span data-stu-id="87ad5-156">No active fixed quantity kanban rule for the product or product variant.</span></span>  
-  <span data-ttu-id="87ad5-157">Nėra produkto arba produkto varianto aptarnavimo užsakymo eilučių.</span><span class="sxs-lookup"><span data-stu-id="87ad5-157">No service order line for the product or product variant.</span></span> 
-  <span data-ttu-id="87ad5-158">Nėra produkto arba produkto varianto aktyvių ar būsimų pardavimo arba pirkimo sutarties eilučių.</span><span class="sxs-lookup"><span data-stu-id="87ad5-158">No active or future sales or purchase agreement lines for the product or product variant.</span></span> 
-  <span data-ttu-id="87ad5-159">Produktas arba produkto variantas nenaudojamas KS, susietoje su produkto arba varianto, kuris planavime nustatytas kaip aktyvus, nepasibaigusia patvirtinta KS versija.</span><span class="sxs-lookup"><span data-stu-id="87ad5-159">The product or product variant is not used in a BOM that is associated with a non-expired approved BOM version for a product or variant that is active for planning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87ad5-160">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="87ad5-160">Related topics</span></span>

-  [<span data-ttu-id="87ad5-161">Naujos produkto ciklo būsenos kūrimas</span><span class="sxs-lookup"><span data-stu-id="87ad5-161">Create a new product lifecycle state</span></span>](tasks/new-product-lifecycle-state.md)
-  [<span data-ttu-id="87ad5-162">Numatytosios produkto ciklo būsenos kūrimas</span><span class="sxs-lookup"><span data-stu-id="87ad5-162">Create a default product lifecycle state</span></span>](tasks/default-product-lifecycle-state.md)
-  [<span data-ttu-id="87ad5-163">Produkto ciklo būsenos priskyrimas išleistam bendrajam produktui</span><span class="sxs-lookup"><span data-stu-id="87ad5-163">Assign a product lifecycle state to a released product master</span></span>](tasks/product-lifecycle-state-released-product-master.md)
-  [<span data-ttu-id="87ad5-164">Produkto ciklo būsenos priskyrimas išleistam produktui</span><span class="sxs-lookup"><span data-stu-id="87ad5-164">Assign a product lifecycle state to a released product</span></span>](tasks/product-lifecycle-state-released-product.md)
-  [<span data-ttu-id="87ad5-165">Pasenusių produkto variantų radimas ir produkto ciklo būsenos priskyrimas</span><span class="sxs-lookup"><span data-stu-id="87ad5-165">Find obsolete product variants and assign a product lifecycle state</span></span>](tasks/obsolete-product-variants.md)
-  [<span data-ttu-id="87ad5-166">Produkto ciklo būsenos kūrimas norint pašalinti produktus iš bendrojo planavimo</span><span class="sxs-lookup"><span data-stu-id="87ad5-166">Create a product lifecycle state to exclude products from Master planning</span></span>](tasks/exclude-products-master-planning.md)
