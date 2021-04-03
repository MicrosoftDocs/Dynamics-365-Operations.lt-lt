---
title: Pakeitimų valdymo įjungimas esamiems produktams
description: Šioje temoje paaiškinama, kaip įgalinti esamų produktų pakeitimų valdymą. Joje taip pat aprašomi atvejai, kuriais jūsų gebėjimas įjungti pakeitimų valdymą yra ribotas.
author: t-benebo
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-02
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 8b9f34f5980937da62610d9668a95816ba6054ef
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500867"
---
# <a name="enable-change-management-on-existing-products"></a><span data-ttu-id="75ac4-104">Pakeitimų valdymo įjungimas esamiems produktams</span><span class="sxs-lookup"><span data-stu-id="75ac4-104">Enable change management on existing products</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="75ac4-105">Šioje temoje paaiškinama, kaip įgalinti esamų produktų pakeitimų valdymą.</span><span class="sxs-lookup"><span data-stu-id="75ac4-105">This topic explains how you can enable change management for existing products.</span></span> <span data-ttu-id="75ac4-106">Joje taip pat aprašomi atvejai, kuriais jūsų gebėjimas įjungti pakeitimų valdymą yra ribotas.</span><span class="sxs-lookup"><span data-stu-id="75ac4-106">It also describes cases where your ability to enable change management is limited.</span></span>

<span data-ttu-id="75ac4-107">Įgalinę esamo produkto pakeitimų valdymą, galite sukurti to produkto versijas ir sekti jo naudojimo metu atliktus keitimus.</span><span class="sxs-lookup"><span data-stu-id="75ac4-107">When you enable change management for an existing product, you can create versions of that product and trace changes that are made to it throughout its life.</span></span> <span data-ttu-id="75ac4-108">Todėl galite sekti šiuos pakeitimus naudodami keitimų užsakymus.</span><span class="sxs-lookup"><span data-stu-id="75ac4-108">Therefore, you can track those changes by using change orders.</span></span> <span data-ttu-id="75ac4-109">Norėdami įgalinti pakeitimų valdymą, turite konvertuoti atitinkamus produktus į *inžinerijos prekes* (dar vadinamas inžinerijos produktais).</span><span class="sxs-lookup"><span data-stu-id="75ac4-109">To enable change management, you must convert the relevant products to *engineering items* (also referred to as engineering products).</span></span> <span data-ttu-id="75ac4-110">Inžinerijos produktai – tai produktai, kurių versijos nustatomos ir kurie valdomi atliekant keitimų valdymą.</span><span class="sxs-lookup"><span data-stu-id="75ac4-110">Engineering products are products that are versioned and managed through change management.</span></span> <span data-ttu-id="75ac4-111">Naudodamiesi vedliu pereisite per konvertavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="75ac4-111">A wizard is provided to guide you through the conversion process.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="75ac4-112">Funkcijos įjungimas sistemoje</span><span class="sxs-lookup"><span data-stu-id="75ac4-112">Turn on the feature in your system</span></span>

<span data-ttu-id="75ac4-113">Norėdami naudotis šia galimybe turite atlikti tolesnes užduotis.</span><span class="sxs-lookup"><span data-stu-id="75ac4-113">To use this capability, you must complete the following tasks:</span></span>

1. <span data-ttu-id="75ac4-114">Įjunkite inžinerinių keitimų valdymo funkciją ir jos konfigūracijos raktą, kaip aprašyta skyriuje [Inžinerinių keitimų valdymo apžvalga](product-engineering-overview.md).</span><span class="sxs-lookup"><span data-stu-id="75ac4-114">Enable the Engineering change management feature and its configuration key as described in [Engineering change management overview](product-engineering-overview.md).</span></span>
1. <span data-ttu-id="75ac4-115">Funkcijų valdymo srityje įjunkite funkciją *Keitimų valdymo įjungimas esamiems produktams*.</span><span class="sxs-lookup"><span data-stu-id="75ac4-115">Turn on the *Enable change management on existing products* feature in feature management.</span></span> <span data-ttu-id="75ac4-116">Daugiau informacijos žr. [Funkcijų valdymo apžvalga](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="75ac4-116">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="restrictions-and-limitations"></a><span data-ttu-id="75ac4-117">Suvaržymai ir apribojimai</span><span class="sxs-lookup"><span data-stu-id="75ac4-117">Restrictions and limitations</span></span>

<span data-ttu-id="75ac4-118">Ne visus produktų tipus galima konvertuoti į visus kitus tipus.</span><span class="sxs-lookup"><span data-stu-id="75ac4-118">Not all product types can be converted to all other types.</span></span> <span data-ttu-id="75ac4-119">Taikomi šie suvaržymai ir apribojimai:</span><span class="sxs-lookup"><span data-stu-id="75ac4-119">The following restrictions and limitations apply:</span></span>

- <span data-ttu-id="75ac4-120">Konvertuojant produktą į inžinerijos produktą, jis lieka *produktu*.</span><span class="sxs-lookup"><span data-stu-id="75ac4-120">When you convert a product to an engineering product, it remains a *product*.</span></span> <span data-ttu-id="75ac4-121">Jis netampa *pagrindiniu produktu*.</span><span class="sxs-lookup"><span data-stu-id="75ac4-121">It doesn't become a *product master*.</span></span>
- <span data-ttu-id="75ac4-122">Kai konvertuojate bendrąjį produktą, kuris turi tam tikrą dimensijų rinkinį, tos dimensijos tvarkomos atlikus keitimą.</span><span class="sxs-lookup"><span data-stu-id="75ac4-122">When you convert a product master that has a specific set of dimensions, those dimensions are maintained after the change.</span></span> <span data-ttu-id="75ac4-123">Pavyzdžiui, jei konvertuojate bendrąjį produktą, kuris turi dydžio dimensiją, jis išlaikys dydžio dimensiją.</span><span class="sxs-lookup"><span data-stu-id="75ac4-123">For example, if you convert a product master that has the size dimension, it will keep the size dimension.</span></span>

<span data-ttu-id="75ac4-124">Todėl, jei turite išskirtąjį produktą, jį galite keisti tik į inžinerijos produktą, kuris operacijų metu neseka produkto dimensijos (t. y. jei versijos dimensija nėra naudojama).</span><span class="sxs-lookup"><span data-stu-id="75ac4-124">Therefore, if you have a distinct product, you can change it only to an engineering product that doesn't track the product dimension in transactions (that is, the version dimension isn't used).</span></span> <span data-ttu-id="75ac4-125">Daugiau informacijos apie šias problemas rasite likusiuose šios temos skyriuose.</span><span class="sxs-lookup"><span data-stu-id="75ac4-125">See the remaining sections of this topic for more information about these issues.</span></span>

## <a name="prepare-for-conversion-by-creating-all-required-engineering-product-categories"></a><span data-ttu-id="75ac4-126">Pasirengimas konvertuoti sukuriant visas reikiamas inžinerijos produktų kategorijas</span><span class="sxs-lookup"><span data-stu-id="75ac4-126">Prepare for conversion by creating all required engineering product categories</span></span>

<span data-ttu-id="75ac4-127">*Inžinerijos produktų kategorija* turi būti priskirta kiekvienam inžinerijos produktui.</span><span class="sxs-lookup"><span data-stu-id="75ac4-127">An *engineering product category* must be assigned to every engineering product.</span></span> <span data-ttu-id="75ac4-128">Šį priskyrimą padarysite paleisdami vedlį **Konvertavimas į inžinerinį produktą**.</span><span class="sxs-lookup"><span data-stu-id="75ac4-128">You will do this assignment when you run the **Convert to engineering product** wizard.</span></span> <span data-ttu-id="75ac4-129">*Kad* būtų galima konvertuoti šiuos produktus, pirmiausia visiems atitinkamiems standartiniams produktams gali būti taikomos inžinerinių produktų kategorijos.</span><span class="sxs-lookup"><span data-stu-id="75ac4-129">Engineering product categories must exist for all relevant standard products *before* you can convert those products.</span></span>

<span data-ttu-id="75ac4-130">Inžinerijos produktų kategorija yra inžinerijos produkto kūrimo pagrindas, kuris apibrėžia numatytųjų verčių ir strategijų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="75ac4-130">The engineering product category provides a basis for creating an engineering product, and it establishes a set of default values and policies.</span></span> <span data-ttu-id="75ac4-131">Inžinerinio produkto kategorija turi sutapti su produktu, kuriam jį galite priskirti.</span><span class="sxs-lookup"><span data-stu-id="75ac4-131">The engineering product category must match the product that you assign it to.</span></span> <span data-ttu-id="75ac4-132">Pavyzdžiui, produkto tipas ir dimensijų grupė turi atitikti ir produktą, ir gamybos produktų kategoriją.</span><span class="sxs-lookup"><span data-stu-id="75ac4-132">For example, the product type and dimension group must match both the product and its engineering product category.</span></span> <span data-ttu-id="75ac4-133">Dėl daugiau informacijos apie inžinerijos duomenis, žr. [Inžinerijos versijos ir inžinerijos produkto kategorijos](engineering-versions-product-category.md).</span><span class="sxs-lookup"><span data-stu-id="75ac4-133">For more information, see [Engineering versions and engineering product categories](engineering-versions-product-category.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="75ac4-134">Vedlys **Konvertuoti į inžinerijos produktą** produktą gali konvertuoti tik į tokius inžinerijos produktus, kurių versija nėra sekama operacijose.</span><span class="sxs-lookup"><span data-stu-id="75ac4-134">The **Convert to engineering product** wizard can convert product only to engineering products where the version isn't tracked in transactions.</span></span> <span data-ttu-id="75ac4-135">Todėl parinktį **Operacijų sekimo versija** reikia nustatyti kaip *Ne* inžinerijos produktų kategorijoms, kurias kuriate esamiems produktams konvertuoti.</span><span class="sxs-lookup"><span data-stu-id="75ac4-135">Therefore, the **Track version in transactions** option must be set to *No* for engineering product categories that you create to convert existing products.</span></span>

<span data-ttu-id="75ac4-136">Informacijos apie inžinerijos produktų kategorijų kūrimą žr. [Inžinerijos versijos ir inžinerijos produkto kategorijos](engineering-versions-product-category.md).</span><span class="sxs-lookup"><span data-stu-id="75ac4-136">For information about how to create engineering product categories, see [Engineering versions and engineering product categories](engineering-versions-product-category.md).</span></span>

## <a name="run-the-convert-to-engineering-product-wizard"></a><span data-ttu-id="75ac4-137">Konvertavimo į inžinerijos produktų vedlio paleidimas</span><span class="sxs-lookup"><span data-stu-id="75ac4-137">Run the Convert to engineering product wizard</span></span>

<span data-ttu-id="75ac4-138">Vedlys **Konvertuoti į inžinerijos produktą** padeda konvertuoti vieną ar kelis esamus produktus į inžinerijos produktus.</span><span class="sxs-lookup"><span data-stu-id="75ac4-138">The **Convert to engineering product** wizard helps you convert one or more existing products to engineering products.</span></span> <span data-ttu-id="75ac4-139">Jis produktus konvertuoja į inžinerijos produktus (produktų versijas), kai versija operacijų metu nėra sekama (t. y. jei versijos dimensija nenaudojama).</span><span class="sxs-lookup"><span data-stu-id="75ac4-139">It converts the products into engineering products (versioned products) where the version isn't tracked in transactions (that is, the version dimension isn't used).</span></span> <span data-ttu-id="75ac4-140">Baigus konvertuoti, produktus galima valdyti naudojant inžinerijos pakeitimų valdymą.</span><span class="sxs-lookup"><span data-stu-id="75ac4-140">After the conversion is completed, you can manage the products by using Engineering change management.</span></span>

<span data-ttu-id="75ac4-141">Konvertavimas yra nuolatinis.</span><span class="sxs-lookup"><span data-stu-id="75ac4-141">The conversion is permanent.</span></span> <span data-ttu-id="75ac4-142">Todėl vėliau jo atšaukti negalėsite.</span><span class="sxs-lookup"><span data-stu-id="75ac4-142">Therefore, you won't be able to reverse it later.</span></span> 

<span data-ttu-id="75ac4-143">Kiekvienas konvertuotas inžinerijos produktas ir toliau bus išleidžiamas tose pačiose įmonėse, kuriose buvo išleistas pradinis produktas.</span><span class="sxs-lookup"><span data-stu-id="75ac4-143">Each converted engineering product will continue to be released in the same companies that the original product was released in.</span></span> <span data-ttu-id="75ac4-144">Tačiau inžinerinė komplektavimo specifikacija (KS) ir maršrutai toms įmonėms nėra automatiškai išleidžiami.</span><span class="sxs-lookup"><span data-stu-id="75ac4-144">However, the engineering bill of materials (BOM) and routes won't automatically be released to those companies.</span></span>

<span data-ttu-id="75ac4-145">Norėdami paleisti vedlį **Konvertuoti į inžinerijos produktą** ir konvertuoti produktą į inžinerijos produktą, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="75ac4-145">Follow these steps to run the **Convert to engineering product** wizard and convert a product to an engineering product.</span></span>

1. <span data-ttu-id="75ac4-146">Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="75ac4-146">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="75ac4-147">Tinklelyje pasirinkite žymės langelį kiekvienam produktui, kurį norite konvertuoti.</span><span class="sxs-lookup"><span data-stu-id="75ac4-147">In the grid, select the check box for each product that you want to convert.</span></span>
1. <span data-ttu-id="75ac4-148">Veiksmų srityje, skirtuke **Inžinierius** grupėje **Inžinerinių pakeitimų valdymas** pasirinkite **Konvertuoti į inžinerijos produktą**, kad atidarytumėte vedlį.</span><span class="sxs-lookup"><span data-stu-id="75ac4-148">On the Action Pane, on the **Engineer** tab, in the **Engineering change management** group, select **Convert to engineering product** to open the wizard.</span></span>
1. <span data-ttu-id="75ac4-149">Pirmasis vedlio puslapis yra **Sveiki!**.</span><span class="sxs-lookup"><span data-stu-id="75ac4-149">The first page of the wizard is the **Welcome** page.</span></span> <span data-ttu-id="75ac4-150">Jei dar nesate susipažinę su konvertavimo procesu, atidžiai perskaitykite šiame puslapyje pateikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="75ac4-150">If you aren't already familiar with the conversion process, carefully read the information on this page.</span></span> <span data-ttu-id="75ac4-151">Kai būsite pasirengę tęsti, pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="75ac4-151">When you're ready to continue, select **Next**.</span></span>
1. <span data-ttu-id="75ac4-152">Puslapyje **Pasirinkti produktų, kuriuos norite konvertuoti, duomenis** rodomas kiekvienas produktas, kurį pasirinkote prieš atidarydami vedlį.</span><span class="sxs-lookup"><span data-stu-id="75ac4-152">The **Select details for the products to be converted** page shows each product that you selected before you opened the wizard.</span></span> <span data-ttu-id="75ac4-153">Patikrinkite sąrašą.</span><span class="sxs-lookup"><span data-stu-id="75ac4-153">Inspect the list.</span></span> <span data-ttu-id="75ac4-154">Naudodami įrankių juostos mygtukus **Naujas** ir **Trinti** pridėkite arba pašalinkite reikiamus produktus.</span><span class="sxs-lookup"><span data-stu-id="75ac4-154">Use the **New** and **Delete** buttons on the toolbar to add or remove products as you require.</span></span>
1. <span data-ttu-id="75ac4-155">Norėdami kiekvienam pateiktam produktui priskirti numatytąsias vertes, naudokite šiuos tinklelio viršuje esančius laukelius.</span><span class="sxs-lookup"><span data-stu-id="75ac4-155">Use the following fields at the top of the grid to assign default values to every product that is listed.</span></span> <span data-ttu-id="75ac4-156">(Pasibaigus konvertavimui, galėsite keisti šias atskirų produktų vertes.) Numatytosios vertės nebus priskirtos produktams, kuriems jau priskirta atitinkama vertė.</span><span class="sxs-lookup"><span data-stu-id="75ac4-156">(You will be able to change these values for individual products after the conversion is completed.) Default values won't be assigned to products where a relevant value has already been assigned.</span></span>

    - <span data-ttu-id="75ac4-157">**Numatytoji inžinerijos kategorija** – pasirinkite pirminę inžinerijos produkto kategoriją, kurią norite priskirti kiekvienam išvardytam produktui.</span><span class="sxs-lookup"><span data-stu-id="75ac4-157">**Default engineering category** – Select an initial engineering product category to assign to every listed product.</span></span> <span data-ttu-id="75ac4-158">Jūsų pasirinkta kategorija bus taikoma tik su ja suderinamiems produktams.</span><span class="sxs-lookup"><span data-stu-id="75ac4-158">The category that you select will be applied only to products that are compatible with it.</span></span>
    - <span data-ttu-id="75ac4-159">**Numatytoji versija** – įveskite pradinę produkto versiją, kurią norite priskirti kiekvienam pateiktam produktui.</span><span class="sxs-lookup"><span data-stu-id="75ac4-159">**Default version** – Enter the initial product version to assign to every listed product.</span></span> <span data-ttu-id="75ac4-160">Kiekvienam inžinerijos produktui priskirta bent viena inžinerijos versija.</span><span class="sxs-lookup"><span data-stu-id="75ac4-160">Every engineering product has at least one engineering version.</span></span>
    - <span data-ttu-id="75ac4-161">**Numatytoji ciklo būsena** – pasirinkite pradinę produkto ciklo būseną, kuri bus priskirta kiekvienam išvardytam produktui.</span><span class="sxs-lookup"><span data-stu-id="75ac4-161">**Default lifecycle state** – Select the initial product lifecycle state to assign to every listed product.</span></span>
    - <span data-ttu-id="75ac4-162">**Dabartinė KS bus inžinerijos produkto dalis** – pažymėkite šį žymės langelį, jei kiekvieno išvardytų produktų dabartinė KS turi būti naudojama kaip inžinerijos produkto KS.</span><span class="sxs-lookup"><span data-stu-id="75ac4-162">**Current BOM will be part of the engineering product** – Select this check box if the current BOM for each listed product should be used as a BOM for the engineering product.</span></span>

    <span data-ttu-id="75ac4-163">Daugiau informacijos apie produkto parametrus ieškokite kitame veiksme.</span><span class="sxs-lookup"><span data-stu-id="75ac4-163">For more information about product settings, see the next step.</span></span>

1. <span data-ttu-id="75ac4-164">Peržiūrėkite kiekvieną tinklelyje nurodytą produktą ir įvertinkite, ar gerai jam priskiriamos numatytosios vertės.</span><span class="sxs-lookup"><span data-stu-id="75ac4-164">Review each product that is listed in the grid, and evaluate how well the default values that you assigned apply to it.</span></span> <span data-ttu-id="75ac4-165">Peržiūrėkite šią kiekvienos eilutės informaciją ir nustatykite atitinkamus laukelius:</span><span class="sxs-lookup"><span data-stu-id="75ac4-165">For each row, review the following information and set any relevant fields:</span></span>

    - <span data-ttu-id="75ac4-166">**Produkto numeris** – produkto numeris.</span><span class="sxs-lookup"><span data-stu-id="75ac4-166">**Product number** – The product number.</span></span>
    - <span data-ttu-id="75ac4-167">**Produkto pavadinimas** – produkto pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="75ac4-167">**Product name** – The name of the product.</span></span>
    - <span data-ttu-id="75ac4-168">**Inžinerijos kategorija** – pasirinkite inžinerijos produkto kategoriją, kuriai turėtų priklausyti produktas jį konvertavus.</span><span class="sxs-lookup"><span data-stu-id="75ac4-168">**Engineering category** – Select the engineering product category that the product should belong to after it's converted.</span></span> <span data-ttu-id="75ac4-169">Kiekvienam produktui turi būti skirta atitinkama kategorija, kaip paaiškinta ankstesniame šios temos skyriuje.</span><span class="sxs-lookup"><span data-stu-id="75ac4-169">An appropriate category must already exist for each product, as was explained in the previous section of this topic.</span></span> <span data-ttu-id="75ac4-170">Kiekvienam produktui turite priskirti kategoriją.</span><span class="sxs-lookup"><span data-stu-id="75ac4-170">You must assign a category to every product.</span></span>
    - <span data-ttu-id="75ac4-171">**Versija** – įveskite pradinę produkto versiją, kurią norite priskirti kiekvienam konvertuotam produktui.</span><span class="sxs-lookup"><span data-stu-id="75ac4-171">**Version** – Enter the product version to assign to the product after it's converted.</span></span> <span data-ttu-id="75ac4-172">Pavyzdžiui, galite pasirinkti skaičių, atitinkantį jau naudojamos numeracijos numerį.</span><span class="sxs-lookup"><span data-stu-id="75ac4-172">For example, you might select a number that fits in the number sequence that your category already uses.</span></span> <span data-ttu-id="75ac4-173">Kiekviena inžinerijos versija talpina su inžinerija susijusius duomenis, kurie konkretūs tai versijai.</span><span class="sxs-lookup"><span data-stu-id="75ac4-173">Each engineering version stores the engineering-relevant data that is specific to that version.</span></span> <span data-ttu-id="75ac4-174">Dėl daugiau informacijos apie inžinerijos duomenis, žr. [Inžinerijos versijos ir inžinerijos produkto kategorijos](engineering-versions-product-category.md).</span><span class="sxs-lookup"><span data-stu-id="75ac4-174">For more information, see [Engineering versions and engineering product categories](engineering-versions-product-category.md).</span></span>
    - <span data-ttu-id="75ac4-175">**Produkto ciklo būsena** – pasirinkite produkto ciklo būseną, kurioje produktas turėtų būti jį konvertavus.</span><span class="sxs-lookup"><span data-stu-id="75ac4-175">**Product lifecycle state** – Select the product lifecycle state that the product should be in after it's converted.</span></span> <span data-ttu-id="75ac4-176">Produkto ciklo būsena leidžia kontroliuoti, kurios operacijos leidžiamos duotai inžinerijos versijai.</span><span class="sxs-lookup"><span data-stu-id="75ac4-176">The product lifecycle state lets you to control which transactions are allowed for a given engineering version.</span></span> <span data-ttu-id="75ac4-177">Dėl daugiau informacijos, žr. [Produkto gyvavimo ciklo būsenos ir perlaidos](product-lifecycle-state-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="75ac4-177">For more information, see [Product lifecycle states and transactions](product-lifecycle-state-transactions.md).</span></span>
    - <span data-ttu-id="75ac4-178">**Turi KS** – pažymėtas žymės langelis rodo, kad produktas turi KS.</span><span class="sxs-lookup"><span data-stu-id="75ac4-178">**Has BOM** – A selected check box indicates that the product has a BOM.</span></span> <span data-ttu-id="75ac4-179">Šio žymės langelio nustatymas gali padėti nuspręsti, kaip žymės langelį **Dabartinė KD bus inžinerinio produkto dalis**.</span><span class="sxs-lookup"><span data-stu-id="75ac4-179">The setting of this check box can help you decide how to set the **Current BOM will be part of the engineering product** check box.</span></span>
    - <span data-ttu-id="75ac4-180">**Dabartinė KS bus inžinerijos produkto dalis** – pažymėkite šį žymės langelį, jei produkto dabartinė KS turi būti naudojama kaip inžinerijos produkto KS.</span><span class="sxs-lookup"><span data-stu-id="75ac4-180">**Current BOM will be part of the engineering product** – Select this check box if the current BOM of the product should be used as a BOM for the engineering product.</span></span> <span data-ttu-id="75ac4-181">Šią KS tvarkys inžinerinio keitimo valdymas.</span><span class="sxs-lookup"><span data-stu-id="75ac4-181">That BOM will then be managed by Engineering change management.</span></span> <span data-ttu-id="75ac4-182">Jei nėra produkto KS arba jei norite rankiniu būdu kurti konvertuoto produkto KS vėliau, išvalykite šį žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="75ac4-182">If the product doesn't have a BOM, or if you prefer to manually create a BOM for the converted product later, clear this check box.</span></span>
    - <span data-ttu-id="75ac4-183">**Yra klaidų** – pažymėtas žymės langelis rodo, kad produkto nustatyme yra viena ar daugiau klaidų.</span><span class="sxs-lookup"><span data-stu-id="75ac4-183">**Has errors** – A selected check box indicates that the product setup has one or more errors.</span></span> <span data-ttu-id="75ac4-184">Pavyzdžiui, produkto tipas arba dimensijų grupė gali nesutapti su kategorija.</span><span class="sxs-lookup"><span data-stu-id="75ac4-184">For example, the product type or the dimension group might not match in the category.</span></span> <span data-ttu-id="75ac4-185">Produktai, kuriuose yra klaidų, bus praleisti ir nebus konvertuoti.</span><span class="sxs-lookup"><span data-stu-id="75ac4-185">Products that have errors will be skipped and won't be converted.</span></span>

1. <span data-ttu-id="75ac4-186">Baigę įrankių juostoje pasirinkite **Tikrinti** ir patikrinkite produkto sąranką.</span><span class="sxs-lookup"><span data-stu-id="75ac4-186">When you've finished, select **Validate** on the toolbar to validate the product setup.</span></span> <span data-ttu-id="75ac4-187">Kiekvienos eilutės žymės langelis **Yra klaidų** bus atnaujintas taip, kad būtų rodoma produkto būsena.</span><span class="sxs-lookup"><span data-stu-id="75ac4-187">For each row, the **Has errors** check box will be updated to indicate the product's status.</span></span> <span data-ttu-id="75ac4-188">Koreguokite vertes, kol kiekviename produkte nebeliks klaidų.</span><span class="sxs-lookup"><span data-stu-id="75ac4-188">Adjust the values until the setup of every product is free of errors.</span></span>
1. <span data-ttu-id="75ac4-189">Tinkamai nustatę visus produktus, norėdami tęsti pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="75ac4-189">When all the products are set up correctly, select **Next** to continue.</span></span>
1. <span data-ttu-id="75ac4-190">Puslapyje **Patvirtinti pasirinkimą** rodomas produktų, kurių sąrankoje nėra klaidų ir kurie yra paruošti konvertavimui, skaičius.</span><span class="sxs-lookup"><span data-stu-id="75ac4-190">The **Confirm selection** page shows the number of products that have no errors in their setup and are therefore ready for conversion.</span></span> <span data-ttu-id="75ac4-191">Jame taip pat rodomas produktų, kurie dėl klaidų bus praleisti, skaičius.</span><span class="sxs-lookup"><span data-stu-id="75ac4-191">It also shows the number of products that will be skipped because of errors.</span></span> <span data-ttu-id="75ac4-192">Kad konvertavimą paleistumėte į paketinę užduotį, parinktį **Paleisti pakete** į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="75ac4-192">To run the conversion as a batch job, set the **Run in batch** option to *Yes*.</span></span>
1. <span data-ttu-id="75ac4-193">Pasirinkite **Baigti**, kad pritaikytumėte parametrus ir pradėtumėte konvertuoti produktus į inžinerinius produktus.</span><span class="sxs-lookup"><span data-stu-id="75ac4-193">Select **Finish** to apply your settings and start to convert the products to engineering products.</span></span>

> [!NOTE]
> <span data-ttu-id="75ac4-194">Jei sistema nustatyta taip, kad rankiniu būdu priimtų produktus prieš juos išleidžiant, kiekvieną konvertuotą produktą reikia priimti naudojant puslapį **Atviras produktų išleidimas**.</span><span class="sxs-lookup"><span data-stu-id="75ac4-194">If your system is set up to manually accept products before they are released, you must accept each converted product by using the **Open product releases** page in the appropriate companies.</span></span> <span data-ttu-id="75ac4-195">Daugiau informacijos žr. [Peržiūrėti ir priimti produktą prieš jo leidimą į vietinę bendrovę](engineering-scenarios.md#accept).</span><span class="sxs-lookup"><span data-stu-id="75ac4-195">For more information, see [Review and accept the product before you release it in the local company](engineering-scenarios.md#accept).</span></span>