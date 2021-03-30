---
title: Sandėlio operacijų produktų filtrų konfigūravimas
description: Šioje temoje apžvelgiama, kaip konfigūruoti produktų filtrus ir filtrų kodus, norint sandėlyje suskirstyti atsargų prekes. Taip pat galite naudoti filtrus, norėdami nustatyti klientus, galinčius užsisakyti konkrečią prekę, bei kurias prekes galima įsigyti iš konkretaus tiekėjo.
author: Mirzaab
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSFilters,WHSFilterGroupTable,EcoResProductDetailsExtended,WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 922ff818e069f41c139cc00db9161dc6e113888b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973740"
---
# <a name="configure-product-filters-for-warehouse-transactions"></a><span data-ttu-id="0f7e1-104">Sandėlio operacijų produktų filtrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="0f7e1-104">Configure product filters for warehouse transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f7e1-105">Šioje temoje apžvelgiama, kaip konfigūruoti produktų filtrus ir filtrų kodus, norint sandėlyje suskirstyti atsargų prekes.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-105">This topic describes how to configure product filters and filter codes to categorize inventory items in a warehouse.</span></span> <span data-ttu-id="0f7e1-106">Taip pat galite naudoti filtrus, norėdami nustatyti klientus, galinčius užsisakyti konkrečią prekę, bei kurias prekes galima nusipirkti iš konkretaus tiekėjo.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-106">You can also use filters to specify which customers can order a particular item and which items can be purchased from a particular vendor.</span></span>

<span data-ttu-id="0f7e1-107">Be to, galite nustatyti ir naudoti produktų filtrus, kad sandėlyje būtų automatiškai tvarkomos atsargų prekės, o filtruotos prekės būtų sujungtos į filtrų grupes.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-107">Additionally, you can set up and use product filters to automatically organize inventory items in a warehouse and combine filtered items into filter groups.</span></span> <span data-ttu-id="0f7e1-108">Filtrus galima naudoti prekių suskirstymui į kategorijas, skirtas tvarkymo, pirkimo ir pardavimo procesams.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-108">Filters can be used to put items into categories for handling, purchasing, and selling processes.</span></span> <span data-ttu-id="0f7e1-109">Galbūt norėsite sugrupuoti prekes arba atskirti jas viena nuo kitos, kai jų apdorojimo būdas yra pagrįstas svorio arba tvarkymo apribojimais.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-109">You might want to group items together or separate them from each other when the way that they are handled is based on weight or handling restrictions.</span></span> <span data-ttu-id="0f7e1-110">Taip pat, galite nurodyti, iš kurių klientų ar tiekėjų prekę galima pirkti arba parduoti.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-110">You can also specify which customers or vendors an item can be purchased from or sold to.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0f7e1-111">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="0f7e1-111">Prerequisites</span></span>

<span data-ttu-id="0f7e1-112">Pateiktoje lentelėje parodytos būtinosios sąlygos, kurias reikia įvykdyti prieš pradedant.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-112">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="0f7e1-113">Būtinoji sąlyga</span><span class="sxs-lookup"><span data-stu-id="0f7e1-113">Prerequisite</span></span> | <span data-ttu-id="0f7e1-114">Instrukcijos</span><span class="sxs-lookup"><span data-stu-id="0f7e1-114">Instructions</span></span> |
|---|---|
| <span data-ttu-id="0f7e1-115">Prieš pradėdami konfigūruoti produktus **Išleisto produkto informacijos** puslapyje, turite įjungti sandėlio apdorojimą produkto saugojimo dimensijos grupei.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-115">Before you start to configure products on the **Released product details** page, you must turn on warehouse processing for the product's storage dimension group.</span></span> | <span data-ttu-id="0f7e1-116">Eikite į **Produkto informacijos valdymas \> Sąranka \> Dimensija ir variantų grupės \> Saugojimo dimensijos grupės** ir pasirinkite arba sukurkite saugojimo dimensijos grupę, kur parinktis **Naudoti sandėlio valdymo procesus** nustatyta į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-116">Go to **Product information management \> Setup \> Dimension and variant groups \> Storage dimension groups**, and select or create a storage dimension group where the **Use warehouse management processes** option is set to *Yes*.</span></span> |
| <span data-ttu-id="0f7e1-117">Jei naudosite kliento filtrus ir (arba) tiekėjo filtrus, turite įgalinti jų naudojimą Sandėlio valdymo parametruose.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-117">If you will use customer filters and/or vendor filters, you must enable their use in Warehouse management parameters.</span></span> | <span data-ttu-id="0f7e1-118">Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span> <span data-ttu-id="0f7e1-119">Skirtuke **Produktų filtrai** nustatykite parinktis **Įgalinti kliento filtrus** ir (arba) **Įgalinti tiekėjo filtrus** į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-119">On the **Product filters** tab, set the **Enable customer filters** and/or **Enable vendor filters** option  to *Yes*.</span></span> |

## <a name="set-up-product-filters"></a><span data-ttu-id="0f7e1-120">Produktų filtrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="0f7e1-120">Set up product filters</span></span>

<span data-ttu-id="0f7e1-121">Produktų filtrai pateikia iki 10 **Filtro pavadinimo** charakteristikų, kurios yra išvardijimo („enum”) reikšmės.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-121">Product filters provide up to 10 **Filter title** characteristics, which are enumeration (enum) values.</span></span> <span data-ttu-id="0f7e1-122">Šias išvardijimo reikšmes galima pasirinkti kuriant produktų filtrą.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-122">These enum values are available for selection when you create a product filter.</span></span> <span data-ttu-id="0f7e1-123">Išvardijimo reikšmes nuo *1 kodo* iki *10 kodo* yra apibrėžtos sistemos ir atitinka konkrečią prekės charakteristiką arba atributą.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-123">The enum values *Code 1* through *Code 10* are system-defined and represent a specific characteristic or attribute of an item.</span></span> <span data-ttu-id="0f7e1-124">Pavyzdžiui, *1 kodas* gali rodyti prekes, kurios turi pavojingos medžiagos klasifikaciją.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-124">For example, *Code 1* might represent items that have a hazardous material classification.</span></span> <span data-ttu-id="0f7e1-125">*2 kodas* gali rodyti prekes, kurias gali pirkti tik tiekėjai.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-125">*Code 2* might represent items that only vendors can purchase.</span></span> <span data-ttu-id="0f7e1-126">Tada produktų filtrai apibrėžia konkrečią **Filtro kodo** reikšmę, susietą su **Filtro pavadinimo** reikšme.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-126">Product filters then define the specific **Filter code** value that is associated with a **Filter title** value.</span></span>

1. <span data-ttu-id="0f7e1-127">Eikite į **Sandėlio valdymas \> Sąranka \> Produktų filtrai \> Produktų filtrai**.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-127">Go to **Warehouse management \> Setup \> Product filters \> Product filters**.</span></span>
1. <span data-ttu-id="0f7e1-128">Veiksmų srityje pasirinkite **Naujas** produktų filtro pridėjimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-128">On the Action Pane, select **New** to add a product filter to the grid.</span></span>
1. <span data-ttu-id="0f7e1-129">Lauke **Filtro pavadinimas** pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-129">In the **Filter title** field, select a value.</span></span>
1. <span data-ttu-id="0f7e1-130">Lauke **Filtro kodas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-130">In the **Filter code** field, enter a value.</span></span>

    <span data-ttu-id="0f7e1-131">![Produktų filtro nustatymas](media/Product_Filters10.png "Produktų filtro nustatymas")</span><span class="sxs-lookup"><span data-stu-id="0f7e1-131">![Setting up a product filter](media/Product_Filters10.png "Setting up a product filter")</span></span>

1. <span data-ttu-id="0f7e1-132">Lauke **Aprašas** įveskite kodo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-132">In the **Description** field, enter a name for the code.</span></span> <span data-ttu-id="0f7e1-133">Pavyzdžiui, *2 kodas* gali rodyti tiekėjus.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-133">For example, *Code 2* might represent vendors.</span></span> <span data-ttu-id="0f7e1-134">Tada galite sukurti produktų filtrą konkrečiam tiekėjui ar tiekėjų grupei.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-134">You can then create a product filter for a specific vendor or group of vendors.</span></span> <span data-ttu-id="0f7e1-135">Daugiau informacijos žiūrėkite tolesniame šios temos skyriuje [Tiekėjų filtrų kodų nustatymas](#vendor-product-filters).</span><span class="sxs-lookup"><span data-stu-id="0f7e1-135">For more information, see the [Setup vendor filter codes](#vendor-product-filters) section later in this topic.</span></span>

    <span data-ttu-id="0f7e1-136">![Produktų filtrų rinkinys](media/Product_Filters.png "Produktų filtrų rinkinys")</span><span class="sxs-lookup"><span data-stu-id="0f7e1-136">![Set of product filters](media/Product_Filters.png "Set of product filters")</span></span>

## <a name="set-up-product-filter-groups"></a><span data-ttu-id="0f7e1-137">Produktų filtrų grupių nustatymas</span><span class="sxs-lookup"><span data-stu-id="0f7e1-137">Set up product filter groups</span></span>

<span data-ttu-id="0f7e1-138">Galite naudoti filtrų grupes filtrų kodams grupuoti.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-138">You can use filter groups to group filter codes.</span></span> <span data-ttu-id="0f7e1-139">Ši galimybė yra naudinga, kai grupė naudojama vietos nurodymo užklausoje ir norite ieškoti grupės, o ne kodų sekos.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-139">This capability is helpful when a group is used in a query in a location directive, and you want to search for the group instead of a series of codes.</span></span> <span data-ttu-id="0f7e1-140">Kiekviena filtrų grupė yra susieta su prekių grupe.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-140">Each filter group is associated with an item group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f7e1-141">Ne visos filtrų grupės yra galimos filtrų kodams, didesnėms nei *4 kodas* (tai yra, nuo *5 kodo* iki *10 kodo*).</span><span class="sxs-lookup"><span data-stu-id="0f7e1-141">Not all product filter groups are available for filter codes that are higher than *Code 4* (that is, *Code 5* through *Code 10*).</span></span> <span data-ttu-id="0f7e1-142">Pavyzdžiui, nors išleistiems produktams bus įtraukti visi produktų filtrų kodai, filtrų kodų grupavimas nebus atnaujintas.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-142">For example, for released products, although all the product filter codes will be added, the grouping of filter codes won't be updated.</span></span> <span data-ttu-id="0f7e1-143">Šis veikimo būdas gali būti atnaujintas naujesniuose leidimuose.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-143">This behavior might be updated in later releases.</span></span>

<span data-ttu-id="0f7e1-144">Norėdami nustatyti filtrų grupes, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-144">To set up filter groups, follow these steps.</span></span>

1. <span data-ttu-id="0f7e1-145">Eikite į **Sandėlio valdymas \> Sąranka \> Produktų filtrai \> Produktų filtrų grupės**.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-145">Go to **Warehouse management \> Setup \> Product filters \> Product filter groups**.</span></span>
1. <span data-ttu-id="0f7e1-146">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-146">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0f7e1-147">Laukuose **1 grupė** ir **2 grupė** įveskite pavadinimus, kurie bus naudojami skirstant prekes į kategorijas.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-147">In the **Group 1** and **Group 2** fields, enter the names that will be used to categorize items.</span></span>
1. <span data-ttu-id="0f7e1-148">„FastTab” skirtuke **Išsami informacija** pasirinkite **Nauja** pridėti naujai eilutei.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-148">On the **Details** FastTab, select **New** to add a line.</span></span>
1. <span data-ttu-id="0f7e1-149">Laukuose **Pradžios data/laikas** ir **Pabaigos data/laikas** įveskite filtrų grupės pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-149">In the **Start date/time** and **End date/time** fields, enter start and end dates for the filter group.</span></span>
1. <span data-ttu-id="0f7e1-150">Lauke **Prekių grupė** pasirinkite prekių grupę, kuriai norite taikyti produktų filtrą.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-150">In the **Item group** field, select the item group that the product filter should apply to.</span></span>
1. <span data-ttu-id="0f7e1-151">Laukuose nuo **1 kodas** iki **10 kodas** pasirinkite filtrų kodus jų įtraukimui į grupę, kaip reikalaujama.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-151">In the **Code 1** through **Code 10** fields, select the filter codes to include in the group, as required.</span></span>

    <span data-ttu-id="0f7e1-152">![Prekių grupė](media/ProdFilterGroup.png "Prekių grupė")</span><span class="sxs-lookup"><span data-stu-id="0f7e1-152">![Item group](media/ProdFilterGroup.png "Item group")</span></span>

> [!NOTE]
> <span data-ttu-id="0f7e1-153">Jei uždarydami puslapį gaunate klaidos pranešimą, galimai trūksta kodo nustatymo.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-153">If you receive an error message when you close the page, a code setup might be missing.</span></span> <span data-ttu-id="0f7e1-154">Puslapyje **Prekių grupės** galite padaryti kodus privalomus prekių grupei pasirinkdami žymės langelius **Priskirti 1 filtro kodą prekės grupei**, **Priskirti 2 filtro kodą prekės grupei** ir taip toliau.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-154">On the **Item groups** page, you can make the codes mandatory for an item group by selecting the **Assign filter code 1 for item group**, **Assign filter code 2 for item group**, and so on, check boxes.</span></span>

## <a name="set-up-filter-codes-on-item-groups"></a><span data-ttu-id="0f7e1-155">Nustatykite filtrų kodus prekių grupėms</span><span class="sxs-lookup"><span data-stu-id="0f7e1-155">Set up filter codes on item groups</span></span>

<span data-ttu-id="0f7e1-156">Nustatydami prekių grupės filtrų kodus, galite sukurti kodus, kurie yra būtini produktams, susietiems su ta prekių grupe.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-156">By setting up filter codes on an item group, you can make the codes that are required for products that are attached to that item group.</span></span>

<span data-ttu-id="0f7e1-157">Norėdami nustatyti filtrų kodus prekių grupėms, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-157">To set up filter codes on item groups, follow these steps.</span></span>

1. <span data-ttu-id="0f7e1-158">Eikite į **Atsargų valdymas \> Nustatymas \> Atsargos \> Prekių grupės**.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-158">Go to **Inventory management \> Setup \> Inventory \> Item groups**.</span></span>
1. <span data-ttu-id="0f7e1-159">Veiksmų srityje pasirinkite **Nauja** prekių grupės sukūrimui.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-159">On the Action Pane, select **New** to create an item group.</span></span>
1. <span data-ttu-id="0f7e1-160">Lauke **Prekių grupė** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-160">In the **Item group** field, enter a name.</span></span>
1. <span data-ttu-id="0f7e1-161">Lauke **Pavadinimas** įveskite aprašomąjį pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-161">In the **Name** field, enter a description.</span></span>
1. <span data-ttu-id="0f7e1-162">„FastTab“ skirtuko **Sandėlis** skyriuje **Reikalaujamas filtras** pasirinkite žymės langelius filtrų kodams, kurie turi būti nustatyti su prekių grupe susietiems produktams.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-162">On the **Warehouse** FastTab, in the **Filter required** section, select the check boxes for the filter codes that must be specified for products that are associated with the item group.</span></span>

    <span data-ttu-id="0f7e1-163">Norėdami atnaujinti išleistą produktą, veiksmo srityje atidarykite jo puslapį **Išleisto produkto informacija** ir pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-163">To update a released product, open its **Released product details** page, and then, on the Action Pane, select **Edit**.</span></span> <span data-ttu-id="0f7e1-164">Tada su kodais susieti filtrai tampa prieinami **Sandėlio** „FastTab” skirtuke.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-164">The filters that are associated with codes then become available on the **Warehouse** FastTab.</span></span>

    <span data-ttu-id="0f7e1-165">![Prekių grupės](media/ItemGroup10.png "Prekių grupės")</span><span class="sxs-lookup"><span data-stu-id="0f7e1-165">![Item groups](media/ItemGroup10.png "Item groups")</span></span>

1. <span data-ttu-id="0f7e1-166">Skyriuje **Prekių grupės filtras** pasirinkite žymės langelius grupėms, kurie turi atitikti filtro grupę, kuri yra numatytoji filtro grupė prekei.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-166">In the **Item group filter** section, select the check boxes for the filters that must match for the filter group to be the default filter group for an item.</span></span>

    <span data-ttu-id="0f7e1-167">Pavyzdžiui, jei pasirinkti **Naudoti 1 filtro kodą** ir **Naudoti 2 filtro kodą** žymės langeliai, abu prekės 1 ir 2 filtrų kodai turi atitikti filtrų grupės konfigūraciją prekės grupei, nes tik tokiu atveju bus galima pasirinkti filtrų grupę.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-167">For example, if the **Use filter code 1** and **Use filter code 2** check boxes are selected, both filter code 1 and filter code 2 of the item must match the setup of the filter group for the item group before the filter group can be selected.</span></span> <span data-ttu-id="0f7e1-168">Kai kuriate naują prekė, pasirinkta filtro grupė bus numatytoji filtro grupė **1 grupė** ir **2 grupė** laukuose, esančiuose **Sandėlio** „FastTab skirtuke”, **Išleisto produkto informacija** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-168">When you create a new item, the selected filter group will be the default filter group in the **Group 1** and **Group 2** fields on the **Warehouse** FastTab of the **Released product details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f7e1-169">Produktų filtro kodai įgalinami tik prekėms, naudojančioms išplėstinį sandėlio valdymą.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-169">Product filter codes are enabled only for items that use advanced warehouse management.</span></span>

## <a name="specify-filter-codes-for-released-products"></a><span data-ttu-id="0f7e1-170">Filtrų kodų nurodymas išleistiems produktams</span><span class="sxs-lookup"><span data-stu-id="0f7e1-170">Specify filter codes for released products</span></span>

<span data-ttu-id="0f7e1-171">Norėdami nustatyti filtrų kodus išleistiems produktams, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-171">Follow these steps to specify filter codes for released products.</span></span> <span data-ttu-id="0f7e1-172">Pavyzdžiui, galite naudoti filtrų kodus grupuoti pavojingiems produktams, kuriuos perka tam tikras tiekėjas.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-172">For example, you can use filter codes to group hazardous products that specific vendors purchase.</span></span>

1. <span data-ttu-id="0f7e1-173">Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-173">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="0f7e1-174">Veiksmų srityje pasirinkite **Naujas** produktui sukurti.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-174">On the Action Pane, select **New** to create a product.</span></span>
1. <span data-ttu-id="0f7e1-175">Dialogo lange **Naujas išleistas produktas** įveskite duomenis, kurių reikia norint sukurti naujo produkto pagrindą, o tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-175">In the **New released product** dialog box, enter the data that is required to create the base of a new product, and then select **OK**.</span></span>

    <span data-ttu-id="0f7e1-176">Produktų filtrų kodai nėra įgalinti, nebent su produktu susieta prekių grupė yra sukonfigūruota filtrų kodams.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-176">Product filter codes aren't enabled unless the item group that is attached to the product has been configured for filter codes.</span></span>

    <span data-ttu-id="0f7e1-177">Daugiau informacijos žiūrėkite [Naujo produkto kūrimas](../pim/tasks/create-new-product.md).</span><span class="sxs-lookup"><span data-stu-id="0f7e1-177">For more information, see [Create a new product](../pim/tasks/create-new-product.md).</span></span>

1. <span data-ttu-id="0f7e1-178">„FastTab” skirtuko **Sandėlis** skyriuje **Produktų filtrų kodai** pasirinkite filtrų kodus nuo **1 kodo** iki **10 kodo** laukų, kaip reikalaujama, kad būtų galima nurodyti produkto filtrų kodus.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-178">On the **Warehouse** FastTab, in the **Product filter codes** section, select filter codes for the **Code 1** through **Code 10** fields, as required, to specify filter codes for the product.</span></span>

## <a name="set-up-generally-available-items"></a><span data-ttu-id="0f7e1-179">Bendrai pasiekiamų prekių nustatymas</span><span class="sxs-lookup"><span data-stu-id="0f7e1-179">Set up generally available items</span></span>

<span data-ttu-id="0f7e1-180">Galite nustatyti, kad konkrečios atsargų prekės būtų pasiekiamos tik klientams, tik tiekėjams, arba tiek klientams, tiek tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-180">You can make specific inventory items available only for customers, only for vendors, or for both customers and vendors.</span></span>

> [!NOTE]
> <span data-ttu-id="0f7e1-181">Klientų ir tiekėjų filtrai netaikomi jokiai prekei, kuri nustatyta kaip bendrai pasiekiama prekė.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-181">Customer and vendor filters don't apply to any item that is set up as generally available.</span></span>

<span data-ttu-id="0f7e1-182">Norėdami nustatyti bendrai pasiekiamas prekes, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-182">To set up generally available items, follow these steps.</span></span>

1. <span data-ttu-id="0f7e1-183">Eikite į **Sandėlio valdymas \> Sąranka \> Produktų filtrai \> Bendrai pasiekiami produktai**.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-183">Go to **Warehouse management \> Setup \> Product filters \> Generally available products**.</span></span>
1. <span data-ttu-id="0f7e1-184">Veiksmų srityje pasirinkite **Naujas** įrašui sukurti.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-184">On the Action Pane, select **New** to create a record.</span></span>
1. <span data-ttu-id="0f7e1-185">Lauke **Klientas ir tiekėjas** pasirinkite *Klientas*, *Tiekėjas* arba *Visi* tam, kad padarytumėte prekes prieinamas klientams, tiekėjams arba abiems.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-185">In the **Customer or vendor** field, select *Customer*, *Vendor*, or *All* to make the items available for customers, vendors, or both.</span></span>
1. <span data-ttu-id="0f7e1-186">Lauke **Pradžios data/laikas** įveskite datą ir laiką, kada prekė taps prieinama.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-186">In the **Start date/time** field, enter the date and time when the item will become available.</span></span>
1. <span data-ttu-id="0f7e1-187">Lauke **Prekių grupė** pasirinkite prekių grupę.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-187">In the **Item group** field, select an item group.</span></span>
1. <span data-ttu-id="0f7e1-188">Laukuose nuo **1 kodo** iki **10 kodo** pasirinkite filtrų kodus, kuriuos naudojant bus apribotos bendrai pasiekiamos prekės.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-188">In the **Code 1** through **Code 10** fields, select the filter codes to limit the items that are generally available.</span></span>

    <span data-ttu-id="0f7e1-189">Pasirinkę prekių grupę, nustatote ją kaip bendrai pasiekiamą.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-189">When you select an item group, you set that group of items as generally available.</span></span> <span data-ttu-id="0f7e1-190">Pasirinkdami filtrų kodus šiuose laukuose, apribojate pasiekiamas prekes.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-190">By selecting filter codes in these fields, you limit the items that are available.</span></span>

## <a name="set-up-customer-product-filters"></a><span data-ttu-id="0f7e1-191">Kliento produktų filtrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="0f7e1-191">Set up customer product filters</span></span>

<span data-ttu-id="0f7e1-192">Galite naudoti šią pasirinktinę procedūrą nurodyti prekes, kurios turėtų būti pasiekiamos klientui, kaip ir prekės padarytos prieinamomis naudojant filtro konfigūraciją **Bendrai pasiekiamų prekių** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-192">You can use this optional procedure to specify items that should be available for a customer in addition to the items that are made available via the filter setup on the **Generally available items** page.</span></span> <span data-ttu-id="0f7e1-193">Galite nustatyti kelis filtrus vienam klientui.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-193">You can set up multiple filters for a single customer.</span></span>

<span data-ttu-id="0f7e1-194">Kliento filtrų kodų nustatymui atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-194">To set up customer filter codes, follow these steps.</span></span>

1. <span data-ttu-id="0f7e1-195">Eikite į **Pardavimas ir rinkodara \> Klientai \> Visi klientai**.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-195">Go to **Sales and marketing \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="0f7e1-196">Pasirinkti klientą.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-196">Select a customer.</span></span>
1. <span data-ttu-id="0f7e1-197">Veiksmų srities skirtuko **Klientas** grupėje **Nustatyti** pasirinkite **Produktų filtrai**.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-197">On the Action Pane, on the **Customer** tab, in the **Set up** group, select **Product filters**.</span></span>
1. <span data-ttu-id="0f7e1-198">Veiksmų srities puslapyje **Produkto filtrų kodai** pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-198">On the **Product filter codes** page, on the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0f7e1-199">Laukuose **Pradžios data/laikas** ir **Pabaigos data/laikas** įveskite pasirinktos prekių grupės pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-199">In the **Start date/time** and **End date/time** fields, enter start and end dates for the selected item group.</span></span>
1. <span data-ttu-id="0f7e1-200">Lauke **Prekių grupė** pasirinkite prekių grupę.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-200">In the **Item group** field, select an item group.</span></span>
1. <span data-ttu-id="0f7e1-201">Laukuose nuo **1 kodo** iki **10 kodo** pasirinkite filtrų kodus, kurie bus naudojami kaip apribojimo kriterijai prekėms, pasiekiamoms klientams pasirinktoje prekių grupėje.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-201">In the **Code 1** through **Code 10** fields, select the filter codes to use as criteria to limit the items that are available for customers in the selected item group.</span></span> <span data-ttu-id="0f7e1-202">Turite pasirinkti kiekvienam filtro kodui, nustatytam prekės grupei.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-202">You must make a selection for every filter code that is set up for the item group.</span></span>

## <a name="set-up-vendor-product-filters"></a><a name="vendor-product-filters"></a><span data-ttu-id="0f7e1-203">Tiekėjo produktų filtrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="0f7e1-203">Set up vendor product filters</span></span>

<span data-ttu-id="0f7e1-204">Galite naudoti šią pasirinktinę procedūrą nurodyti prekes, kurios turėtų būti pasiekiamos tiekėjui, kaip ir prekės padarytos prieinamomis naudojant filtro konfigūraciją **Bendrai pasiekiamų prekių** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-204">You can use this optional procedure to specify items that should be available for a vendor in addition to the items that are made available via the filter setup on the **Generally available items** page.</span></span> <span data-ttu-id="0f7e1-205">Vienam tiekėjui galite nustatyti kelis filtrus.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-205">You can set up multiple filters for a single vendor.</span></span>

<span data-ttu-id="0f7e1-206">Tiekėjo filtrų kodų nustatymui atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-206">To set up vendor filter codes, follow these steps.</span></span>

1. <span data-ttu-id="0f7e1-207">Eikite į **Įsigijimas ir šaltinio pasirinkimas \> Tiekėjai \> Visi tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-207">Go to **Procurement and sourcing \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="0f7e1-208">Pasirinkite tiekėją.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-208">Select a vendor.</span></span>
1. <span data-ttu-id="0f7e1-209">Veiksmų srities skirtuko **Tiekėjas** grupėje **Nustatyti** pasirinkite **Produktų filtrai**.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-209">On the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Product filters**.</span></span>
1. <span data-ttu-id="0f7e1-210">Veiksmų srities puslapyje **Filtrų kodai** pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-210">On the **Filter codes** page, on the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0f7e1-211">Laukuose **Pradžios data/laikas** ir **Pabaigos data/laikas** įveskite pasirinktos prekių grupės pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-211">In the **Start date/time** and **End date/time** fields, enter start and end dates for the selected item group.</span></span>
1. <span data-ttu-id="0f7e1-212">Lauke **Prekių grupė** pasirinkite prekių grupę.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-212">In the **Item group** field, select an item group.</span></span>
1. <span data-ttu-id="0f7e1-213">Laukuose nuo **1 kodo** iki **10 kodo** pasirinkite filtrų kodus, kurie bus naudojami kaip apribojimo kriterijai prekėms, pasiekiamoms tiekėjams pasirinktoje prekių grupėje.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-213">In the **Code 1** through **Code 10** fields, select the filter codes to use as criteria to limit the items that are available for vendors in the selected item group.</span></span> <span data-ttu-id="0f7e1-214">Turite pasirinkti kiekvienam filtro kodui, nustatytam prekės grupei.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-214">You must make a selection for every filter code that is set up for the item group.</span></span>

> [!NOTE]
> <span data-ttu-id="0f7e1-215">Tiekėjo produktų filtro konfigūracija taikoma išleistiems produktams, kuriuose įgalinti sandėlio valdymo procesai susietai saugojimo dimensijų grupei.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-215">The setup of vendor product filters applies to released products where warehouse management processes are enabled for the associated storage dimension group.</span></span> <span data-ttu-id="0f7e1-216">Filtro kodai naudojami siekiant nustatyti, ar sistema leis vartotojams įsigyti tam tikrą prekę iš tam tikro tiekėjo, kai jie kuria pirkimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-216">The filter codes are used to determine whether the system will allow users to purchase a given item from a given vendor when they create purchase order lines.</span></span> <span data-ttu-id="0f7e1-217">„Microsoft Dynamics 365 Supply Chain Management” yra du tiekėjo patvirtinimo tvarkymo metodai.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-217">Microsoft Dynamics 365 Supply Chain Management has two methods for handling vendor approval.</span></span> <span data-ttu-id="0f7e1-218">Jei yra vienas ar daugiau išleistų produktų, kurio laukas **Patvirtinto tiekėjo patikrinimo metodas** yra nustatytas į *Tik įspėjimas* arba *Neleidžiama*, abu tiekėjo patvirtinimo metodai gali būti įjungti toms prekėms.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-218">If one or more released products exist where the **Approved vendor check method** field is set to *Warning only* or *Not allowed*, both vendor approval methods could be enabled for those items.</span></span> <span data-ttu-id="0f7e1-219">Ši situacija gali sukelti problemų, kai vartotojai kuria pirkimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="0f7e1-219">This situation might cause issues when users create purchase order lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f7e1-220">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="0f7e1-220">See also</span></span>

[<span data-ttu-id="0f7e1-221">Daugiau informacijos ieškokite tinklaraščio įraše WMS-sandėlio filtrų kodai</span><span class="sxs-lookup"><span data-stu-id="0f7e1-221">For more information see the blog post WMS-Warehouse Filter Codes</span></span>](http://blog.dynamics-for-operations.com/2017/09/26/wms-warehouse-filter-codes/)