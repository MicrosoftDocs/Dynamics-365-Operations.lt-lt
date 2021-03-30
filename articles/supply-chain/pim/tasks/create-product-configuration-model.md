---
title: Kurti produkto konfigūracijos modelį
description: Ši procedūra nurodo, kaip kurti produkto konfigūracijos modelį ir įvesti pagrindinę informaciją, pvz., atributus ir pakomponenčius.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e89c2c1659b8e995350762cb9e9b77a1e10c831f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218518"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="057b6-103">Kurti produkto konfigūracijos modelį</span><span class="sxs-lookup"><span data-stu-id="057b6-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="057b6-104">Ši procedūra nurodo, kaip kurti produkto konfigūracijos modelį ir įvesti pagrindinę informaciją, pvz., atributus ir pakomponenčius.</span><span class="sxs-lookup"><span data-stu-id="057b6-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="057b6-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="057b6-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="057b6-106">Produkto modelio kūrimas</span><span class="sxs-lookup"><span data-stu-id="057b6-106">Create a product model</span></span>
1. <span data-ttu-id="057b6-107">Spustelėkite Produkto varianto modelio aprašą.</span><span class="sxs-lookup"><span data-stu-id="057b6-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="057b6-108">Spustelėkite Produkto konfigūracijos modeliai.</span><span class="sxs-lookup"><span data-stu-id="057b6-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="057b6-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="057b6-109">Click New.</span></span>
4. <span data-ttu-id="057b6-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="057b6-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="057b6-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="057b6-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="057b6-112">Lauke Sprendimo priemonės strategija pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="057b6-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="057b6-113">Sprendimo priemonės strategija nustato, kaip tvarkomi produktų konfigūravimo pagal apribojimus modelio apribojimai.</span><span class="sxs-lookup"><span data-stu-id="057b6-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="057b6-114">Šis pasirinkimas gali turėti įtakos produkto konfigūracijos modelio našumui.</span><span class="sxs-lookup"><span data-stu-id="057b6-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="057b6-115">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="057b6-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="057b6-116">Šakninis komponentas nurodo produkto konfigūracijos modelį, tačiau jį galima naudoti kituose produkto modeliuose.</span><span class="sxs-lookup"><span data-stu-id="057b6-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="057b6-117">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="057b6-117">Click OK.</span></span>
9. <span data-ttu-id="057b6-118">Lauke Pakartotinai naudoti konfigūracijas pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="057b6-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="057b6-119">Jei pakartotinis konfigūracijos parametras yra nustatytas į Taip, sistema patikrins, ar yra identiškų konfigūracijų po kiekvieno konfigūracijos seanso ir pakartotinai jas naudos, jei ras tikslų atitikimą.</span><span class="sxs-lookup"><span data-stu-id="057b6-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="057b6-120">Įtraukti atributų</span><span class="sxs-lookup"><span data-stu-id="057b6-120">Add attributes</span></span>
1. <span data-ttu-id="057b6-121">Išplėskite skyrių Atributai.</span><span class="sxs-lookup"><span data-stu-id="057b6-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="057b6-122">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="057b6-122">Click Add.</span></span>
3. <span data-ttu-id="057b6-123">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="057b6-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="057b6-124">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="057b6-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="057b6-125">Lauke Sprendimo priemonės pavadinimas įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="057b6-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="057b6-126">Produkto konfigūravimo priemonė apribojimo sprendimo priemonė naudoja Sprendimo priemonės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="057b6-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="057b6-127">Jame negali būti tarpų arba specialiųjų simbolių, išskyrus _ (pabraukimo brūkšnys).</span><span class="sxs-lookup"><span data-stu-id="057b6-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="057b6-128">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="057b6-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="057b6-129">Aprašo tekstas rodomas konfigūracijos vartotojui ir todėl gali padėti pasirenkant tinkamą atributo vertę.</span><span class="sxs-lookup"><span data-stu-id="057b6-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="057b6-130">Lauke Atributo tipas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="057b6-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="057b6-131">Atributo tipas nustato, kurios vertės yra galimos atributui.</span><span class="sxs-lookup"><span data-stu-id="057b6-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="057b6-132">Pažymėkite žymės langelį Įtraukti į pakartotinį naudojimą.</span><span class="sxs-lookup"><span data-stu-id="057b6-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="057b6-133">Ši pasirinktis galima tik tokiu atveju, jei pasirinkta pasirinktis Pakartotinai naudoti konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="057b6-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="057b6-134">Įtraukiant atributą į pakartotinio naudojimą žymės langelį reiškia, kad šis atributas bus svarstomas, kai sistema ieškos tikslaus atitikimo.</span><span class="sxs-lookup"><span data-stu-id="057b6-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="057b6-135">Įtraukti pakomponenčius</span><span class="sxs-lookup"><span data-stu-id="057b6-135">Add subcomponents</span></span>
1. <span data-ttu-id="057b6-136">Išplėskite skyrių Pakomponenčiai.</span><span class="sxs-lookup"><span data-stu-id="057b6-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="057b6-137">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="057b6-137">Click Add.</span></span>
3. <span data-ttu-id="057b6-138">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="057b6-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="057b6-139">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="057b6-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="057b6-140">Lauke Sprendimo priemonės pavadinimas įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="057b6-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="057b6-141">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="057b6-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="057b6-142">Lauke Komponentas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="057b6-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="057b6-143">Kiekvienas pakomponentis turi nurodyti į komponento aprašą.</span><span class="sxs-lookup"><span data-stu-id="057b6-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="057b6-144">Šis dizainas palaiko pakartotinio naudojimo komponentus ir užtikrina, kad nustačius komponentą, jį galima naudoti daugelyje produkto modelių.</span><span class="sxs-lookup"><span data-stu-id="057b6-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="057b6-145">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="057b6-145">Click Save.</span></span>
9. <span data-ttu-id="057b6-146">Spustelėkite KS eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="057b6-146">Click BOM line details.</span></span>
    * <span data-ttu-id="057b6-147">KS eilutės informacijos forma leidžia vartotojui pasirinkti reikiamas pakomponenčio ypatybes.</span><span class="sxs-lookup"><span data-stu-id="057b6-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="057b6-148">Kiekvienai ypatybei gali būti suteikta fiksuota vertė arba ji gali būti susieta su atributu.</span><span class="sxs-lookup"><span data-stu-id="057b6-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="057b6-149">Susiejus su atributu, bus gautos skirtingos KS eilutės ypatybės vertės, atsižvelgiant į konfigūracijos pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="057b6-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="057b6-150">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="057b6-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="057b6-151">Kiekvienas pakomponentis nurodo konfigūruojamą bendrąjį produktą su konfigūravimo pagal apribojimus technologija.</span><span class="sxs-lookup"><span data-stu-id="057b6-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="057b6-152">Nuoroda pateikiama pagal prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="057b6-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="057b6-153">Pažymėkite žymės langelį Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="057b6-153">Select the Set check box.</span></span>
12. <span data-ttu-id="057b6-154">Lauke Skaičiavimas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="057b6-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="057b6-155">Nustačius skaičiavimo pasirinktį užtikrinama, kad produktas bus įtrauktas vykdant šio produkto savikainos skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="057b6-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="057b6-156">Spustelėkite skirtuką Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="057b6-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="057b6-157">Pažymėkite žymės langelį Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="057b6-157">Select the Set check box.</span></span>
15. <span data-ttu-id="057b6-158">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="057b6-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="057b6-159">Kiekio laukas nustato, kiek šio produkto bus suvartota sukonfigūruotam produktui.</span><span class="sxs-lookup"><span data-stu-id="057b6-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="057b6-160">Pažymėkite žymės langelį Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="057b6-160">Select the Set check box.</span></span>
17. <span data-ttu-id="057b6-161">Lauke Gaminių kiekiui įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="057b6-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="057b6-162">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="057b6-162">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]