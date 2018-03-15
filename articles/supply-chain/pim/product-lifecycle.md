---
title: "Produkto ciklo būsena"
description: "Produkto ciklo būsena nurodo išleisto produkto arba produkto varianto ciklo būseną."
author: cvocph
manager: AnnBe
ms.date: 12/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: conradv
ms.dyn365.ops.version: 7.3
ms.search.validFrom: 2017-12-31
ms.translationtype: HT
ms.sourcegitcommit: 236b0253f20330f09f07dbcfa19257350fb5d37f
ms.openlocfilehash: 8ef72de3f226a3270ac0145a20e4da7dfe64f4ba
ms.contentlocale: lt-lt
ms.lasthandoff: 02/08/2018

---

# <a name="product-lifecycle-state"></a><span data-ttu-id="f1eae-103">Produkto ciklo būsena</span><span class="sxs-lookup"><span data-stu-id="f1eae-103">Product lifecycle state</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f1eae-104">Produkto ciklo būsena nurodo išleisto produkto arba produkto varianto ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="f1eae-104">A product lifecycle state documents the lifecycle state of a released product or product variant.</span></span> <span data-ttu-id="f1eae-105">Produkto ciklo būsenas apibrėžia vartotojas, paprastai – produktų vadovas arba produktų bendrųjų duomenų vadovas.</span><span class="sxs-lookup"><span data-stu-id="f1eae-105">Product lifecycle states are defined by the user, typically a product manager or a product master data manager.</span></span> <span data-ttu-id="f1eae-106">Konkrečius verslo procesus, pvz., bendrąjį planavimą, gali paveikti konkreti ciklo būsena.</span><span class="sxs-lookup"><span data-stu-id="f1eae-106">Specific business processes, such as master planning, can be affected by a specific lifecycle state.</span></span>   
 
<span data-ttu-id="f1eae-107">Išleistą produktą arba produkto variantą galima susieti su produkto ciklo būsena, kuri nurodo, kokia yra esama konkretaus produkto arba varianto būsena.</span><span class="sxs-lookup"><span data-stu-id="f1eae-107">A released product or product variant can be associated with a product lifecycle state that documents in which lifecycle state a specific product or variant is currently in.</span></span> <span data-ttu-id="f1eae-108">Galite nurodyti bet kokį produkto ciklo būsenų skaičių, priskirdami būsenos pavadinimą ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="f1eae-108">You can define any number of product lifecycle states by assigning a state name and description.</span></span> <span data-ttu-id="f1eae-109">Galite pasirinkti vieną ciklo būseną kaip numatytąją naujų išleistų produktų būseną.</span><span class="sxs-lookup"><span data-stu-id="f1eae-109">You can select one lifecycle state as the default state for new released products.</span></span> <span data-ttu-id="f1eae-110">Išleisto produkto variantai perima produkto ciklo būseną iš atitinkamo išleisto bendrojo produkto, kai jie sukuriami.</span><span class="sxs-lookup"><span data-stu-id="f1eae-110">Released product variants inherit their product lifecycle state from their released product master on creation.</span></span> <span data-ttu-id="f1eae-111">Keičiant išleisto bendrojo produkto ciklo būseną galima atnaujinti visus esamus variantus, kurių pradinė būsena tokia pati.</span><span class="sxs-lookup"><span data-stu-id="f1eae-111">When changing the lifecycle state on a released product master, you can choose to update all existing variants that have the same original state.</span></span>  

## <a name="create-a-new-product-lifecycle-state"></a><span data-ttu-id="f1eae-112">Naujos produkto ciklo būsenos kūrimas</span><span class="sxs-lookup"><span data-stu-id="f1eae-112">Create a new product lifecycle state</span></span> 
 
- <span data-ttu-id="f1eae-113">Norėdami kurti naują produkto ciklo būseną, paleiskite arba perskaitykite užduočių vedlį **Naujos produkto ciklo būsenos kūrimas**.</span><span class="sxs-lookup"><span data-stu-id="f1eae-113">To create a new product lifecycle state, play or read the task guide **Create a new product lifecycle state**.</span></span> 

-  <span data-ttu-id="f1eae-114">Norėdami kurti numatytąją produkto ciklo būseną, paleiskite arba perskaitykite užduočių vedlį **Numatytosios produkto ciklo būsenos kūrimas**.</span><span class="sxs-lookup"><span data-stu-id="f1eae-114">To create a default product lifecycle state, play or read the task guide **Create a default product lifecycle state**.</span></span>   

## <a name="associate-product-lifecycle-states-to-released-products"></a><span data-ttu-id="f1eae-115">Produkto ciklo būsenos susiejimas su išleistais produktais</span><span class="sxs-lookup"><span data-stu-id="f1eae-115">Associate product lifecycle states to released products</span></span>  

<span data-ttu-id="f1eae-116">Yra keli būdai, kaip galima susieti produkto ciklo būseną su išleistais produktais arba produkto variantais.</span><span class="sxs-lookup"><span data-stu-id="f1eae-116">There are multiple ways to associate a product lifecycle state to released products or product variants.</span></span>

-  <span data-ttu-id="f1eae-117">Kuriant naują išleistą produktą, numatytoji **Produkto ciklo būsena** priskiriama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="f1eae-117">On creation of a new released product, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="f1eae-118">Išleidžiant produktą į juridinį subjektą, numatytoji **Produkto ciklo būsena** priskiriama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="f1eae-118">On release of a product to a legal entity, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="f1eae-119">Išleidžiant produkto variantą į juridinį subjektą, **Produkto ciklo būsena**, susieta su išleistu bendruoju produktu šiame juridiniame subjekte, automatiškai priskiriama naujam variantui.</span><span class="sxs-lookup"><span data-stu-id="f1eae-119">On release of a product variant to a legal entity, the **Product lifecycle state** associated to the released product master in this legal entity is automatically assigned to the new variant.</span></span> 

<span data-ttu-id="f1eae-120">Galite neautomatiškai atnaujinti produkto ciklo būseną, naudodami:</span><span class="sxs-lookup"><span data-stu-id="f1eae-120">You can manually update the product lifecycle state by using:</span></span> 

-    <span data-ttu-id="f1eae-121">sąrašo puslapį **Išleisti produktai** arba **Informacijos rodinys**;</span><span class="sxs-lookup"><span data-stu-id="f1eae-121">The **Released products** list page or **Details view**.</span></span> 
-  <span data-ttu-id="f1eae-122">sąrašo puslapį **Išleisti produkto variantai** arba **Informacijos rodinys**.</span><span class="sxs-lookup"><span data-stu-id="f1eae-122">The **Released product variants** list page or **Details view**.</span></span> 
-  <span data-ttu-id="f1eae-123">Raskite pasenusius produktus arba produkto variantus pagal paklausą ir susiekite ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="f1eae-123">Find the obsolete products or product variants based on demand and associate a lifecycle state.</span></span>  

<span data-ttu-id="f1eae-124">Norėdami išsamesnės informacijos apie tai, kaip susieti produkto ciklo būsenas, paleiskite arba perskaitykite du toliau nurodytus užduočių vedlius.</span><span class="sxs-lookup"><span data-stu-id="f1eae-124">For detailed information about how to associate product lifecycle states, play or read the following two task guides.</span></span>

-  <span data-ttu-id="f1eae-125">Norėdami susieti produkto ciklo būseną su išleistu bendruoju produktu, paleiskite arba perskaitykite užduočių vedlį **Produkto ciklo būsenos priskyrimas išleistam bendrajam produktui**.</span><span class="sxs-lookup"><span data-stu-id="f1eae-125">To associate a product lifecycle state to a released product master, play or read the task guide **Assign a product lifecycle state to a released product master**.</span></span> 

-  <span data-ttu-id="f1eae-126">Norėdami susieti produkto ciklo būseną su išleistu produktu, paleiskite arba perskaitykite užduočių vedlį **Produkto ciklo būsenos priskyrimas išleistam produktui**.</span><span class="sxs-lookup"><span data-stu-id="f1eae-126">To associate a product lifecycle state to a release product, play or read the task guide **Assign a product lifecycle state to a released product**.</span></span> 

## <a name="impact-on-master-planning"></a><span data-ttu-id="f1eae-127">Poveikis bendrajam planavimui</span><span class="sxs-lookup"><span data-stu-id="f1eae-127">Impact on master planning</span></span> 

<span data-ttu-id="f1eae-128">Produkto ciklo būsena turi tik vieną kontrolės žymę: **Galima planuoti**.</span><span class="sxs-lookup"><span data-stu-id="f1eae-128">The product lifecycle state has only one control flag: **Is active for planning**.</span></span> <span data-ttu-id="f1eae-129">Pagal numatytuosius parametrus šis parametras nustatytas į parinktį **Taip** visose sukurtose produkto ciklo būsenose, bet galima nustatyti parinktį **Ne**.</span><span class="sxs-lookup"><span data-stu-id="f1eae-129">By default, this is set to **Yes** for all created product lifecycle states, but it can be changed to **No**.</span></span> <span data-ttu-id="f1eae-130">Nustačius **Ne**, susieti išleisti produktai arba išleisti produkto variantai yra:</span><span class="sxs-lookup"><span data-stu-id="f1eae-130">When set to **No**, the associated released products or released product variants are:</span></span> 

-  <span data-ttu-id="f1eae-131">neįtraukiami į bendrąjį planavimą;</span><span class="sxs-lookup"><span data-stu-id="f1eae-131">Excluded from master planning.</span></span> 
-  <span data-ttu-id="f1eae-132">neįtraukiami į KS lygio skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="f1eae-132">Excluded from BOM-level calculation.</span></span> 

<span data-ttu-id="f1eae-133">Daugiau informacijos apie tai, kaip naudoti produkto ciklo būseną norint pašalinti produktus iš bendrojo planavimo ir lygio KS skaičiavimo, paleiskite arba perskaitykite užduočių vedlį **Produkto ciklo būsenos kūrimas norint pašalinti produktus iš bendrojo planavimo**.</span><span class="sxs-lookup"><span data-stu-id="f1eae-133">For detailed information about how to use product lifecycle state to exclude products from master planning and BOM-level calculation, play or read the task guide **Create a product lifecycle state to exclude products from Master planning**.</span></span>

> [!NOTE]
> <span data-ttu-id="f1eae-134">Siekiant padidinti efektyvumą, labai rekomenduojame susieti visus pasenusius išleistus produktus arba produkto variantus, ypač dirbant su vienkartinio produkto konfigūracijos variantais, su produkto ciklo būsena, kuri bendrajame planavime yra išjungta.</span><span class="sxs-lookup"><span data-stu-id="f1eae-134">For performance reasons, it is highly recommended to associate all obsolete released products or product variants, especially when working with non-reusable product configuration variants, with a product lifecycle state that is deactivated for master planning.</span></span>  
 
## <a name="default-migration-import-and-export"></a><span data-ttu-id="f1eae-135">Numatytasis perėjimas, importavimas ir eksportavimas</span><span class="sxs-lookup"><span data-stu-id="f1eae-135">Default migration, import, and export</span></span> 

<span data-ttu-id="f1eae-136">Produkto ciklo būsenų nepalaiko duomenų objektai ir ciklo būsenos negalima nustatyti į kintamąją būseną naudojant išleisto produkto duomenų objektus.</span><span class="sxs-lookup"><span data-stu-id="f1eae-136">The product lifecycle states are not supported by data entities, and the lifecycle state cannot be set to a variable state through the released product data entities.</span></span>

-  <span data-ttu-id="f1eae-137">Vykdant perėjimą iš ankstesnių leidimų, visų produktų ir produkto variantų ciklo būsena bus nenurodyta.</span><span class="sxs-lookup"><span data-stu-id="f1eae-137">On migration from previous releases, the lifecycle state of all products and product variants will be blank.</span></span>  
-  <span data-ttu-id="f1eae-138">Kai importuojami išleisti produktai naudojant duomenų objektą, kuriant bus taikoma numatytoji ciklo būsena.</span><span class="sxs-lookup"><span data-stu-id="f1eae-138">When importing released products through a data entity, the default lifecycle state will be applied on creation.</span></span>  
-  <span data-ttu-id="f1eae-139">Kai importuojami išleisti produkto variantai naudojant duomenų objektą, bus importuojama išleisto bendrojo produkto ciklo būsena.</span><span class="sxs-lookup"><span data-stu-id="f1eae-139">When importing released product variants through a data entity, the product lifecycle state of the released product master will be imported.</span></span>   
 
## <a name="find-obsolete-products-and-products-variants"></a><span data-ttu-id="f1eae-140">Pasenusių produktų ir produktų variantų radimas</span><span class="sxs-lookup"><span data-stu-id="f1eae-140">Find obsolete products and products variants</span></span> 
 
<span data-ttu-id="f1eae-141">Galite vykdyti modeliavimo analizę, norėdami rasti pasenusius išleistus produktus arba produkto variantus ir tada atnaujinti jų produkto ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="f1eae-141">You can run a simulation analysis to find the obsolete released products or product variants and then update their product lifecycle status.</span></span> <span data-ttu-id="f1eae-142">Norėdami rasti pasenusius produktus, paleiskite arba perskaitykite užduočių vedlį **Pasenusių produkto variantų radimas ir produkto ciklo būsenos priskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="f1eae-142">To find obsolete products, play and read the task guide **Find obsolete product variants and assign a product lifecycle state**.</span></span> <span data-ttu-id="f1eae-143">Šiame užduočių vedlyje parodoma, kaip rasti pasenusius išleistus produktus arba produkto variantus ir kaip susieti produkto ciklo būseną su pasenusiais produktais.</span><span class="sxs-lookup"><span data-stu-id="f1eae-143">This task guide shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="f1eae-144">Jame taip pat parodoma, kaip peržiūrėti modeliavimo rezultatus ir įvertinti, kiek produktų ir produkto variantų bus susieti su nauja produkto ciklo būsena vykdant naujinimą be modeliavimo.</span><span class="sxs-lookup"><span data-stu-id="f1eae-144">It also shows hot to view the simulation results and assess how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  
 
<span data-ttu-id="f1eae-145">Vykdydami analizę modeliavimo režimu, produktai ir produkto variantai, identifikuoti kaip pasenę, rodomi konkrečioje formoje, kurioje juos galima lengvai peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="f1eae-145">By running the analysis in a simulation mode, the products and product variants identified as obsolete are displayed in a specific form, where they can easily be reviewed.</span></span> <span data-ttu-id="f1eae-146">Atliekant analizę ieškoma operacijų ir konkrečių bendrųjų duomenų, kad būtų identifikuoti produktai, kurių poreikio nėra per kintantį laikotarpį ir iš poreikio negalima generuoti jokių bendrųjų duomenų.</span><span class="sxs-lookup"><span data-stu-id="f1eae-146">The analysis searches for transactions and specific master data to identify products that have no demand within a variable period and no master data that can result in demand.</span></span> <span data-ttu-id="f1eae-147">Naujų išleistų produktų per kintantį laikotarpį galima neįtraukti į analizę.</span><span class="sxs-lookup"><span data-stu-id="f1eae-147">New released products within a variable period can be excluded from the analysis.</span></span> <span data-ttu-id="f1eae-148">Kai analizės modeliavimas pateikia numatytąjį rezultatą, vartotojas gali vykdyti analizę ir nustatyti visų produktų, kurie analizėje nurodyti kaip pasenę, naują produkto ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="f1eae-148">When the analysis simulation returns the expected result, the user can run the analysis and set a new product lifecycle state to all products identified as obsolete by the analysis.</span></span>  
 
> [!NOTE]
> <span data-ttu-id="f1eae-149">Atminkite, kad visą analizę ir naujinimą reikia atlikti tame pačiame juridiniame subjekte.</span><span class="sxs-lookup"><span data-stu-id="f1eae-149">Note that all analysis and updates must be done within the same legal entity.</span></span>  
 
## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a><span data-ttu-id="f1eae-150">Išleistų produktų arba produkto variantų pasirinkimo ir naujinimo kriterijai</span><span class="sxs-lookup"><span data-stu-id="f1eae-150">Criteria to select and update released products or product variants</span></span> 
 
<span data-ttu-id="f1eae-151">Naudokite toliau nurodytus išleistų produktų arba produkto variantų pasirinkimo ir naujinimo kriterijus.</span><span class="sxs-lookup"><span data-stu-id="f1eae-151">Use the following criteria to select and update the released products and product variants:</span></span> 

-    <span data-ttu-id="f1eae-152">Produkto arba produkto varianto produkto ciklo būsena turi skirtis nuo naujos norimos būsenos.</span><span class="sxs-lookup"><span data-stu-id="f1eae-152">The product lifecycle state of the product or product variant must be different from the new desired state.</span></span> 
-  <span data-ttu-id="f1eae-153">Produktas arba produkto variantas buvo sukurtas prieš keletą dienų atsižvelgiant į dienų skaičių, kuris įvestas pasirinkimo dialogo lange.</span><span class="sxs-lookup"><span data-stu-id="f1eae-153">The product or product variant was created some days ago based on the number of days that you enter in the selection dialog box.</span></span> 
-  <span data-ttu-id="f1eae-154">Nėra produkto arba produkto varianto atvirų gamybos užsakymų (= būsena < baigėsi).</span><span class="sxs-lookup"><span data-stu-id="f1eae-154">There are no open production orders (= status < ended) for the product or product variant.</span></span> 
-  <span data-ttu-id="f1eae-155">Nėra produkto arba produkto varianto atvirų atsargų operacijų (= būsena išdavimas ReservPhysical į QuotationIssue arba būsenos gavimas Registrered į QuotationReceipt).</span><span class="sxs-lookup"><span data-stu-id="f1eae-155">There are no open inventory transactions (= status issue ReservPhysical to QuotationIssue or status receipt Registrered to QuotationReceipt) for the product or product variant.</span></span> 
-  <span data-ttu-id="f1eae-156">Nėra produkto arba produkto varianto atsargų operacijų per paskutines dienas.</span><span class="sxs-lookup"><span data-stu-id="f1eae-156">There are no inventory transactions within the last number of days for the product or product variant.</span></span> 
-  <span data-ttu-id="f1eae-157">Nėra produkto arba produkto varianto ateities poreikio arba tiekimo prognozės.</span><span class="sxs-lookup"><span data-stu-id="f1eae-157">There is no future demand or supply forecast for the product or product variant.</span></span>  
-  <span data-ttu-id="f1eae-158">Produkto arba produkto varianto minimalus atsargų lygis nenustatytas prekės padengime.</span><span class="sxs-lookup"><span data-stu-id="f1eae-158">No minimum stock level has been set in item coverage for the product or product variant.</span></span> 
-  <span data-ttu-id="f1eae-159">Nėra produkto arba produkto varianto aktyvių fiksuoto kiekio „kanban“ taisyklių.</span><span class="sxs-lookup"><span data-stu-id="f1eae-159">No active fixed quantity kanban rule for the product or product variant.</span></span>  
-  <span data-ttu-id="f1eae-160">Nėra produkto arba produkto varianto aptarnavimo užsakymo eilučių.</span><span class="sxs-lookup"><span data-stu-id="f1eae-160">No service order line for the product or product variant.</span></span> 
-  <span data-ttu-id="f1eae-161">Nėra produkto arba produkto varianto aktyvių ar būsimų pardavimo arba pirkimo sutarties eilučių.</span><span class="sxs-lookup"><span data-stu-id="f1eae-161">No active or future sales or purchase agreement lines for the product or product variant.</span></span> 
-  <span data-ttu-id="f1eae-162">Produktas arba produkto variantas nenaudojamas KS, susietoje su produkto arba varianto, kuris planavime nustatytas kaip aktyvus, nepasibaigusia patvirtinta KS versija.</span><span class="sxs-lookup"><span data-stu-id="f1eae-162">The product or product variant is not used in a BOM that is associated with a non-expired approved BOM version for a product or variant that is active for planning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1eae-163">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="f1eae-163">Related topics</span></span>

-  [<span data-ttu-id="f1eae-164">Naujos produkto ciklo būsenos kūrimas (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="f1eae-164">Create a new product lifecycle state (Task guide)</span></span>](tasks/new-product-lifecycle-state.md)
-  [<span data-ttu-id="f1eae-165">Numatytosios produkto ciklo būsenos kūrimas (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="f1eae-165">Create a default product lifecycle state (Task guide)</span></span>](tasks/default-product-lifecycle-state.md)
-  [<span data-ttu-id="f1eae-166">Produkto ciklo būsenos priskyrimas išleistam bendrajam produktui (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="f1eae-166">Assign a product lifecycle state to a released product master (Task guide)</span></span>](tasks/product-lifecycle-state-released-product-master.md)
-  [<span data-ttu-id="f1eae-167">Produkto ciklo būsenos priskyrimas išleistam produktui (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="f1eae-167">Assign a product lifecycle state to a released product (Task guide)</span></span>](tasks/product-lifecycle-state-released-product.md)
-  [<span data-ttu-id="f1eae-168">Pasenusių produkto variantų radimas ir produkto ciklo būsenos priskyrimas (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="f1eae-168">Find obsolete product variants and assign a product lifecycle state (Task guide)</span></span>](tasks/obsolete-product-variants.md)
-  [<span data-ttu-id="f1eae-169">Produkto ciklo būsenos kūrimas norint pašalinti produktus iš bendrojo planavimo (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="f1eae-169">Create a product lifecycle state to exclude products from Master planning (Task guide)</span></span>](tasks/exclude-products-master-planning.md)

