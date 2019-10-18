---
title: Bangos veiksmo kodai
description: Šioje temoje pateikiama bangos veiksmo kodų ir jų naudojimo apžvalga.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992362"
---
# <a name="wave-step-codes"></a><span data-ttu-id="b011c-103">Bangos veiksmo kodai</span><span class="sxs-lookup"><span data-stu-id="b011c-103">Wave step codes</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a><span data-ttu-id="b011c-104">Apie bangos veiksmo kodus</span><span class="sxs-lookup"><span data-stu-id="b011c-104">About wave step codes</span></span>

<span data-ttu-id="b011c-105">Bangos veiksmo kodai yra kodai, kuriuos vartotojai gali nustatyti ir naudoti konkretiems bangos metodų egzemplioriams susieti su atitinkamu šablonu.</span><span class="sxs-lookup"><span data-stu-id="b011c-105">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="b011c-106">Yra papildymo, krovimo į konteinerius, etikečių spausdinimo, krovinio kūrimo ir rūšiavimo šablonų.</span><span class="sxs-lookup"><span data-stu-id="b011c-106">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="b011c-107">Kai bangos veiksmo kodai nenaudojami, vartotojai turi įvesti laisvos formos tekstą, kad galėtų nurodyti konkretų bangos metodo egzemplioriaus šabloną.</span><span class="sxs-lookup"><span data-stu-id="b011c-107">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="b011c-108">Laisvos formos tekste dažnai būna klaidų, nes vartotojai turi įsitikinti, kad bangos veiksmo tekstas, kurį jie įtraukia į konkretų bangos veiksmo metodą bangos šablone, tiksliai atitinka tikslinio šablono bangos veiksmo tekstą.</span><span class="sxs-lookup"><span data-stu-id="b011c-108">Free text is prone to error, because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="b011c-109">Konkretaus bangos veiksmo tipo bangos veiksmo kodai nustatomi atskirame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="b011c-109">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="b011c-110">Kiekvieno bangos veiksmo metodo egzemplioriaus bangos šablone, kuriam būtinas bangos veiksmo kodas, bangos veiksmo kodas turi būti pasirinktas išplečiamajame sąraše.</span><span class="sxs-lookup"><span data-stu-id="b011c-110">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="b011c-111">Pasirinkus išplečiamajame meniu, pakeičiamas laisvos formos teksto įrašas ir sumažinamas žmogaus padarytos klaidos pavojus ir poveikis.</span><span class="sxs-lookup"><span data-stu-id="b011c-111">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="b011c-112">Sąrankos kodai naudojami norint susieti bangos veiksmo metodą bangos šablone su metodo tiksliniu šablonu.</span><span class="sxs-lookup"><span data-stu-id="b011c-112">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="b011c-113">Bangos veiksmo kodų funkcijos naudoti neprivaloma, o sunaudojimas vyksta per juridinį subjektą.</span><span class="sxs-lookup"><span data-stu-id="b011c-113">Use of the wave step codes feature is optional, and uptake is per legal entity.</span></span> <span data-ttu-id="b011c-114">Todėl, jei konkretus juridinis subjektas naudoja šią funkciją, visų minėto juridinio subjekto esamų bangos veiksmo kodų struktūra atnaujinama.</span><span class="sxs-lookup"><span data-stu-id="b011c-114">Therefore, if a specific legal entity uses the feature, all existing wave step codes in that legal entity are upgraded to the new structure.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="b011c-115">Sąrankos demonstracija</span><span class="sxs-lookup"><span data-stu-id="b011c-115">Setup demo</span></span> 

<span data-ttu-id="b011c-116">Norėdami vykdyti šią demonstraciją, turite įdiegti demonstracinius duomenis ir naudoti **USMF** demonstracinių duomenų įmonę.</span><span class="sxs-lookup"><span data-stu-id="b011c-116">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="b011c-117">Įgalinti bangos veiksmo kodus</span><span class="sxs-lookup"><span data-stu-id="b011c-117">Enable wave step codes</span></span>

<span data-ttu-id="b011c-118">Atlikite šiuos veiksmus, norėdami įjungti bangos veiksmo kodų funkciją.</span><span class="sxs-lookup"><span data-stu-id="b011c-118">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="b011c-119">Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b011c-119">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
2. <span data-ttu-id="b011c-120">Skirtuko **Bendra** FastTab **Bangos apdorojimas** nustatykite parinktį **Įjungti bangos veiksmo kodus** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="b011c-120">On the **General** tab, on the **Wave processing** FastTab, set the **Enable wave step codes** option to **Yes**.</span></span>

<span data-ttu-id="b011c-121">Visų esamų bangos veiksmo laisvos formos tekstų struktūra atnaujinama.</span><span class="sxs-lookup"><span data-stu-id="b011c-121">All existing wave step free texts are upgraded to the new structure.</span></span> <span data-ttu-id="b011c-122">Užbaigus šį naujinimą juridiniame subjekte, parinktis **Įjungti bangos veiksmo kodus** nebebus pasiekiama puslapyje **Sandėlio valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b011c-122">After this upgrade is completed for a legal entity, the **Enable wave step codes** option is no longer available on the **Warehouse management parameters** page.</span></span>

<span data-ttu-id="b011c-123">Patvirtinama atliekant naujinimą, todėl, jei atnaujinti nepavyksta, gaunamas klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="b011c-123">Validations are done during the upgrade, and if the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="b011c-124">Gali nepavykti atnaujinti dėl toliau pateikiamų nesuderinamumų.</span><span class="sxs-lookup"><span data-stu-id="b011c-124">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="b011c-125">Yra besidubliuojančių bangos veiksmo laisvos formos tekstų.</span><span class="sxs-lookup"><span data-stu-id="b011c-125">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="b011c-126">Yra tinkinimų.</span><span class="sxs-lookup"><span data-stu-id="b011c-126">Customizations exist.</span></span>
- <span data-ttu-id="b011c-127">Bangos veiksmo laisvos formos tekstas, susietas su bangos veiksmo metodo egzemplioriumi, neatitinka numatomo šablono tipo.</span><span class="sxs-lookup"><span data-stu-id="b011c-127">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="b011c-128">Pašalinę visus patvirtinimo metu nustatytus nesuderinamumus, galite iš naujo paleisti naujinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="b011c-128">After you've resolved any conflicts that are identified during the validations, you can rerun the upgrade process.</span></span>

<span data-ttu-id="b011c-129">Atnaujinus sėkmingai, atsiranda puslapis **Bangos veiksmo kodai** (**Sandėlio valdymas \> Sąranka \> Bangos \> Bangos veiksmo kodai**).</span><span class="sxs-lookup"><span data-stu-id="b011c-129">When the upgrade succeeds, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="b011c-130">Šiame puslapyje pateikiami bangos veiksmo kodai, kurie buvo atnaujinti, kai buvo įjungta bangos veiksmo kodų funkcija.</span><span class="sxs-lookup"><span data-stu-id="b011c-130">This page lists the wave step codes that were upgraded when the wave step codes feature was turned on.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="b011c-131">Naujų bangos veiksmo kodų kūrimas</span><span class="sxs-lookup"><span data-stu-id="b011c-131">Create new wave step codes</span></span>

<span data-ttu-id="b011c-132">Puslapyje **Bangos veiksmo kodai** galite kurti ir naikinti bangos veiksmo kodus.</span><span class="sxs-lookup"><span data-stu-id="b011c-132">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="b011c-133">Visi nauji bangos veiksmo kodai ir su juo susiję ID turi būti unikalūs visuose bangos veiksmo tipuose ir jie turi būti nurodyti konkrečiame bangos veiksmo tipe.</span><span class="sxs-lookup"><span data-stu-id="b011c-133">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="b011c-134">Bangos veiksmo kodų taikymas</span><span class="sxs-lookup"><span data-stu-id="b011c-134">Apply wave step codes</span></span>

<span data-ttu-id="b011c-135">Nustačius atitinkamus bangos veiksmo kodus, jie gali būti taikomi bangos proceso metodams.</span><span class="sxs-lookup"><span data-stu-id="b011c-135">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="b011c-136">Norėdami taikyti bangos veiksmo kodus, pereikite prie tinkamo tikslinio šablono.</span><span class="sxs-lookup"><span data-stu-id="b011c-136">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="b011c-137">Toliau pateikiami tiksliniai šablonai, kuriuos nurodo bangos veiksmo kodai.</span><span class="sxs-lookup"><span data-stu-id="b011c-137">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="b011c-138">**Papildymo šablonai:** Sandėlio valdymas \> Sąranka \> Papildymas \> Papildymo šablonai</span><span class="sxs-lookup"><span data-stu-id="b011c-138">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="b011c-139">**Krovinio kūrimo šablonai:** Sandėlio valdymas \> Sąranka \> Krovinys \> Krovinio kūrimo šablonai</span><span class="sxs-lookup"><span data-stu-id="b011c-139">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="b011c-140">**Rūšiavimo šablonai:** Sandėlio valdymas \> Sąranka \> Pakavimas \> Siuntimo rūšiavimo šablonai</span><span class="sxs-lookup"><span data-stu-id="b011c-140">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="b011c-141">**Krovimo į konteinerius šablonai:** Sandėlio valdymas \> Sąranka \> Konteineriai \> Konteinerių kūrimo šablonai</span><span class="sxs-lookup"><span data-stu-id="b011c-141">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="b011c-142">**Etikečių spausdinimo šablonai:** Sandėlio valdymas \>Sąranka \> Dokumento maršruto planavimas \>Bangos etikečių šablonai</span><span class="sxs-lookup"><span data-stu-id="b011c-142">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="b011c-143">Šablonai šiame sąraše taikomi tada, kai jie yra nurodyti bangos proceso metode, kuris pasirinktas bangos šablone.</span><span class="sxs-lookup"><span data-stu-id="b011c-143">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="b011c-144">Kai bangos proceso metode esantis bangos veiksmo kodas bangos šablone atitinka bangos veiksmo kodą viename iš šablonų tipų, taikomas šablonas.</span><span class="sxs-lookup"><span data-stu-id="b011c-144">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="b011c-145">Pavyzdinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="b011c-145">Sample scenario</span></span>

<span data-ttu-id="b011c-146">Ši procedūra padeda užtikrinti, kad jūsų sukurtas papildymo šablonas bus taikomas bangos šablonui.</span><span class="sxs-lookup"><span data-stu-id="b011c-146">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="b011c-147">Eikite į **Sandėlio valdymas \> Sąranka \> Bangos \> Bangos veiksmo kodai** ir sukurkite bangos veiksmo kodą tipui **Papildymas**.</span><span class="sxs-lookup"><span data-stu-id="b011c-147">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="b011c-148">Eikite į **Sandėlio valdymas \> Sąranka \> Papildymas \> Papildymo šablonai** ir sukurkite papildymo šabloną.</span><span class="sxs-lookup"><span data-stu-id="b011c-148">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="b011c-149">Papildymo šablone pasirinkite bangos veiksmo kodą, kurį sukūrėte tipui **Papildymas**.</span><span class="sxs-lookup"><span data-stu-id="b011c-149">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="b011c-150">Eikite į **Sandėlio valdymas \>Sąranka \> Bangos \>Bangos šablonai**ir pasirinkite norimą naudoti bangos šabloną.</span><span class="sxs-lookup"><span data-stu-id="b011c-150">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="b011c-151">Šablono FastTab **Metodai** pasirinkite metodą **Papildymas**.</span><span class="sxs-lookup"><span data-stu-id="b011c-151">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="b011c-152">Lauke **Bangos veiksmo kodas** pasirinkite bangos veiksmo kodą, kurį pasirinkote papildymo šablone.</span><span class="sxs-lookup"><span data-stu-id="b011c-152">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>
