--- 
title: "Kurti produkto konfigūracijos modelį"
description: "Ši procedūra nurodo, kaip kurti produkto konfigūracijos modelį ir įvesti pagrindinę informaciją, pvz., atributus ir pakomponenčius."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 866a4f29723e10eb0a1e1be86d6d4f6da8a69b1c
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="b8856-103">Kurti produkto konfigūracijos modelį</span><span class="sxs-lookup"><span data-stu-id="b8856-103">Create a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8856-104">Ši procedūra nurodo, kaip kurti produkto konfigūracijos modelį ir įvesti pagrindinę informaciją, pvz., atributus ir pakomponenčius.</span><span class="sxs-lookup"><span data-stu-id="b8856-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="b8856-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="b8856-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="b8856-106">Produkto modelio kūrimas</span><span class="sxs-lookup"><span data-stu-id="b8856-106">Create a product model</span></span>
1. <span data-ttu-id="b8856-107">Spustelėkite Produkto varianto modelio aprašą.</span><span class="sxs-lookup"><span data-stu-id="b8856-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="b8856-108">Spustelėkite Produkto konfigūracijos modeliai.</span><span class="sxs-lookup"><span data-stu-id="b8856-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="b8856-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b8856-109">Click New.</span></span>
4. <span data-ttu-id="b8856-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b8856-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="b8856-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b8856-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="b8856-112">Lauke Sprendimo priemonės strategija pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="b8856-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="b8856-113">Sprendimo priemonės strategija nustato, kaip tvarkomi produktų konfigūravimo pagal apribojimus modelio apribojimai.</span><span class="sxs-lookup"><span data-stu-id="b8856-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="b8856-114">Šis pasirinkimas gali turėti įtakos produkto konfigūracijos modelio našumui.</span><span class="sxs-lookup"><span data-stu-id="b8856-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="b8856-115">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b8856-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="b8856-116">Šakninis komponentas nurodo produkto konfigūracijos modelį, tačiau jį galima naudoti kituose produkto modeliuose.</span><span class="sxs-lookup"><span data-stu-id="b8856-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="b8856-117">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b8856-117">Click OK.</span></span>
9. <span data-ttu-id="b8856-118">Lauke Pakartotinai naudoti konfigūracijas pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="b8856-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="b8856-119">Jei pakartotinis konfigūracijos parametras yra nustatytas į Taip, sistema patikrins, ar yra identiškų konfigūracijų po kiekvieno konfigūracijos seanso ir pakartotinai jas naudos, jei ras tikslų atitikimą.</span><span class="sxs-lookup"><span data-stu-id="b8856-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="b8856-120">Įtraukti atributų</span><span class="sxs-lookup"><span data-stu-id="b8856-120">Add attributes</span></span>
1. <span data-ttu-id="b8856-121">Išplėskite skyrių Atributai.</span><span class="sxs-lookup"><span data-stu-id="b8856-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="b8856-122">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="b8856-122">Click Add.</span></span>
3. <span data-ttu-id="b8856-123">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b8856-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b8856-124">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b8856-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="b8856-125">Lauke Sprendimo priemonės pavadinimas įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="b8856-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="b8856-126">Produkto konfigūravimo priemonė apribojimo sprendimo priemonė naudoja Sprendimo priemonės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="b8856-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="b8856-127">Jame negali būti tarpų arba specialiųjų simbolių, išskyrus _ (pabraukimo brūkšnys).</span><span class="sxs-lookup"><span data-stu-id="b8856-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="b8856-128">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b8856-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="b8856-129">Aprašo tekstas rodomas konfigūracijos vartotojui ir todėl gali padėti pasirenkant tinkamą atributo vertę.</span><span class="sxs-lookup"><span data-stu-id="b8856-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="b8856-130">Lauke Atributo tipas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="b8856-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="b8856-131">Atributo tipas nustato, kurios vertės yra galimos atributui.</span><span class="sxs-lookup"><span data-stu-id="b8856-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="b8856-132">Pažymėkite žymės langelį Įtraukti į pakartotinį naudojimą.</span><span class="sxs-lookup"><span data-stu-id="b8856-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="b8856-133">Ši pasirinktis galima tik tokiu atveju, jei pasirinkta pasirinktis Pakartotinai naudoti konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="b8856-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="b8856-134">Įtraukiant atributą į pakartotinio naudojimą žymės langelį reiškia, kad šis atributas bus svarstomas, kai sistema ieškos tikslaus atitikimo.</span><span class="sxs-lookup"><span data-stu-id="b8856-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="b8856-135">Įtraukti pakomponenčius</span><span class="sxs-lookup"><span data-stu-id="b8856-135">Add subcomponents</span></span>
1. <span data-ttu-id="b8856-136">Išplėskite skyrių Pakomponenčiai.</span><span class="sxs-lookup"><span data-stu-id="b8856-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="b8856-137">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="b8856-137">Click Add.</span></span>
3. <span data-ttu-id="b8856-138">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b8856-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b8856-139">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b8856-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="b8856-140">Lauke Sprendimo priemonės pavadinimas įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="b8856-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="b8856-141">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b8856-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="b8856-142">Lauke Komponentas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="b8856-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="b8856-143">Kiekvienas pakomponentis turi nurodyti į komponento aprašą.</span><span class="sxs-lookup"><span data-stu-id="b8856-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="b8856-144">Šis dizainas palaiko pakartotinio naudojimo komponentus ir užtikrina, kad nustačius komponentą, jį galima naudoti daugelyje produkto modelių.</span><span class="sxs-lookup"><span data-stu-id="b8856-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="b8856-145">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b8856-145">Click Save.</span></span>
9. <span data-ttu-id="b8856-146">Spustelėkite KS eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="b8856-146">Click BOM line details.</span></span>
    * <span data-ttu-id="b8856-147">KS eilutės informacijos forma leidžia vartotojui pasirinkti reikiamas pakomponenčio ypatybes.</span><span class="sxs-lookup"><span data-stu-id="b8856-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="b8856-148">Kiekvienai ypatybei gali būti suteikta fiksuota vertė arba ji gali būti susieta su atributu.</span><span class="sxs-lookup"><span data-stu-id="b8856-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="b8856-149">Susiejus su atributu, bus gautos skirtingos KS eilutės ypatybės vertės, atsižvelgiant į konfigūracijos pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="b8856-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="b8856-150">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b8856-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="b8856-151">Kiekvienas pakomponentis nurodo konfigūruojamą bendrąjį produktą su konfigūravimo pagal apribojimus technologija.</span><span class="sxs-lookup"><span data-stu-id="b8856-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="b8856-152">Nuoroda pateikiama pagal prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="b8856-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="b8856-153">Pažymėkite žymės langelį Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="b8856-153">Select the Set check box.</span></span>
12. <span data-ttu-id="b8856-154">Lauke Skaičiavimas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="b8856-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="b8856-155">Nustačius skaičiavimo pasirinktį užtikrinama, kad produktas bus įtrauktas vykdant šio produkto savikainos skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="b8856-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="b8856-156">Spustelėkite skirtuką Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="b8856-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="b8856-157">Pažymėkite žymės langelį Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="b8856-157">Select the Set check box.</span></span>
15. <span data-ttu-id="b8856-158">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b8856-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b8856-159">Kiekio laukas nustato, kiek šio produkto bus suvartota sukonfigūruotam produktui.</span><span class="sxs-lookup"><span data-stu-id="b8856-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="b8856-160">Pažymėkite žymės langelį Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="b8856-160">Select the Set check box.</span></span>
17. <span data-ttu-id="b8856-161">Lauke Gaminių kiekiui įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b8856-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="b8856-162">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b8856-162">Click OK.</span></span>

