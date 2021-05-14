---
title: Kurti produkto konfigūracijos modelį
description: Ši procedūra nurodo, kaip kurti produkto konfigūracijos modelį ir įvesti pagrindinę informaciją, pvz., atributus ir pakomponenčius.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cb9e33d7bab6ca9cd378ec40baa796d1a933ece
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921370"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="59d31-103">Kurti produkto konfigūracijos modelį</span><span class="sxs-lookup"><span data-stu-id="59d31-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="59d31-104">Ši procedūra nurodo, kaip kurti produkto konfigūracijos modelį ir įvesti pagrindinę informaciją, pvz., atributus ir pakomponenčius.</span><span class="sxs-lookup"><span data-stu-id="59d31-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="59d31-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="59d31-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="59d31-106">Produkto modelio kūrimas</span><span class="sxs-lookup"><span data-stu-id="59d31-106">Create a product model</span></span>

1. <span data-ttu-id="59d31-107">Eikite į **Produkto informacijos valdymas \> Produktai \> Produkto konfigūracijos modeliai**.</span><span class="sxs-lookup"><span data-stu-id="59d31-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="59d31-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="59d31-108">Select **New**.</span></span>
1. <span data-ttu-id="59d31-109">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="59d31-109">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="59d31-110">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="59d31-110">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="59d31-111">Lauke **Sprendimo priemonės** strategija pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="59d31-111">In the **Solver strategy** field, select an option.</span></span>
    * <span data-ttu-id="59d31-112">Sprendimo priemonės strategija nustato, kaip tvarkomi produktų konfigūravimo pagal apribojimus modelio apribojimai.</span><span class="sxs-lookup"><span data-stu-id="59d31-112">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="59d31-113">Šis pasirinkimas gali turėti įtakos produkto konfigūracijos modelio našumui.</span><span class="sxs-lookup"><span data-stu-id="59d31-113">This selection can have an impact on the performance of the product configuration model.</span></span>  
1. <span data-ttu-id="59d31-114">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="59d31-114">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="59d31-115">Šakninis komponentas nurodo produkto konfigūracijos modelį, tačiau jį galima naudoti kituose produkto modeliuose.</span><span class="sxs-lookup"><span data-stu-id="59d31-115">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
1. <span data-ttu-id="59d31-116">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="59d31-116">Select **OK**.</span></span>
1. <span data-ttu-id="59d31-117">Lauke **Pakartotinai naudoti** konfigūracijas pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="59d31-117">In the **Reuse configurations** field, select an option.</span></span>
    * <span data-ttu-id="59d31-118">Jei pakartotinis konfigūracijos parametras yra nustatytas į Taip, sistema patikrins, ar yra identiškų konfigūracijų po kiekvieno konfigūracijos seanso ir pakartotinai jas naudos, jei ras tikslų atitikimą.</span><span class="sxs-lookup"><span data-stu-id="59d31-118">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="59d31-119">Įtraukti atributų</span><span class="sxs-lookup"><span data-stu-id="59d31-119">Add attributes</span></span>

1. <span data-ttu-id="59d31-120">Išplėskite skyrių **Atributai**.</span><span class="sxs-lookup"><span data-stu-id="59d31-120">Expand the **Attributes** section.</span></span>
2. <span data-ttu-id="59d31-121">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="59d31-121">Select **Add**.</span></span>
3. <span data-ttu-id="59d31-122">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="59d31-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="59d31-123">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="59d31-123">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="59d31-124">Lauke **Sprendimo priemonės** pavadinimas įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="59d31-124">In the **Solver name** field, type a value.</span></span>
    * <span data-ttu-id="59d31-125">Produkto konfigūravimo priemonė apribojimo sprendimo priemonė naudoja Sprendimo priemonės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="59d31-125">The solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="59d31-126">Jame negali būti tarpų arba specialiųjų simbolių, išskyrus _ (pabraukimo brūkšnys).</span><span class="sxs-lookup"><span data-stu-id="59d31-126">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="59d31-127">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="59d31-127">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="59d31-128">Aprašo tekstas rodomas konfigūracijos vartotojui ir todėl gali padėti pasirenkant tinkamą atributo vertę.</span><span class="sxs-lookup"><span data-stu-id="59d31-128">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="59d31-129">Lauke **Atributo tipas** įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="59d31-129">In the **Attribute type** field, enter or select a value.</span></span>
    * <span data-ttu-id="59d31-130">Atributo tipas nustato, kurios vertės yra galimos atributui.</span><span class="sxs-lookup"><span data-stu-id="59d31-130">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="59d31-131">Pažymėkite **Įtraukti į pakartotinį naudojimą** laukelį.</span><span class="sxs-lookup"><span data-stu-id="59d31-131">Select the **Include in reuse** check box.</span></span>
    * <span data-ttu-id="59d31-132">Ši pasirinktis galima tik tokiu atveju, jei pasirinkta pasirinktis Pakartotinai naudoti konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="59d31-132">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="59d31-133">Įtraukiant atributą į pakartotinio naudojimą žymės langelį reiškia, kad šis atributas bus svarstomas, kai sistema ieškos tikslaus atitikimo.</span><span class="sxs-lookup"><span data-stu-id="59d31-133">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="59d31-134">Įtraukti pakomponenčius</span><span class="sxs-lookup"><span data-stu-id="59d31-134">Add subcomponents</span></span>

1. <span data-ttu-id="59d31-135">Išplėskite skyrių **Pakomponenčiai**.</span><span class="sxs-lookup"><span data-stu-id="59d31-135">Expand the **Subcomponents** section.</span></span>
2. <span data-ttu-id="59d31-136">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="59d31-136">Select **Add**.</span></span>
3. <span data-ttu-id="59d31-137">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="59d31-137">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="59d31-138">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="59d31-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="59d31-139">Lauke **Sprendimo priemonės** pavadinimas įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="59d31-139">In the **Solver name** field, type a value.</span></span>
6. <span data-ttu-id="59d31-140">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="59d31-140">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="59d31-141">Lauke **Komponentas** įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="59d31-141">In the **Component** field, enter or select a value.</span></span>
    * <span data-ttu-id="59d31-142">Kiekvienas pakomponentis turi nurodyti į komponento aprašą.</span><span class="sxs-lookup"><span data-stu-id="59d31-142">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="59d31-143">Šis dizainas palaiko pakartotinio naudojimo komponentus ir užtikrina, kad nustačius komponentą, jį galima naudoti daugelyje produkto modelių.</span><span class="sxs-lookup"><span data-stu-id="59d31-143">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="59d31-144">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="59d31-144">Select **Save**.</span></span>
9. <span data-ttu-id="59d31-145">Pasirinkite **BOM eilutės** informaciją.</span><span class="sxs-lookup"><span data-stu-id="59d31-145">Select **BOM line details**.</span></span>
    * <span data-ttu-id="59d31-146">KS eilutės informacijos forma leidžia vartotojui pasirinkti reikiamas pakomponenčio ypatybes.</span><span class="sxs-lookup"><span data-stu-id="59d31-146">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="59d31-147">Kiekvienai ypatybei gali būti suteikta fiksuota vertė arba ji gali būti susieta su atributu.</span><span class="sxs-lookup"><span data-stu-id="59d31-147">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="59d31-148">Susiejus su atributu, bus gautos skirtingos KS eilutės ypatybės vertės, atsižvelgiant į konfigūracijos pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="59d31-148">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="59d31-149">Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="59d31-149">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="59d31-150">Kiekvienas pakomponentis nurodo konfigūruojamą bendrąjį produktą su konfigūravimo pagal apribojimus technologija.</span><span class="sxs-lookup"><span data-stu-id="59d31-150">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="59d31-151">Nuoroda pateikiama pagal prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="59d31-151">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="59d31-152">Pažymėkite **Nustatyti** laukelį.</span><span class="sxs-lookup"><span data-stu-id="59d31-152">Select the **Set** check box.</span></span>
12. <span data-ttu-id="59d31-153">Lauke **Skaičiavimas** pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="59d31-153">Select **Yes** in the **Calculation** field.</span></span>
    * <span data-ttu-id="59d31-154">Nustačius skaičiavimo pasirinktį užtikrinama, kad produktas bus įtrauktas vykdant šio produkto savikainos skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="59d31-154">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="59d31-155">Pasirinkite skirtuką **Nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="59d31-155">Select the **Setup** tab.</span></span>
14. <span data-ttu-id="59d31-156">Pažymėkite **Nustatyti** laukelį.</span><span class="sxs-lookup"><span data-stu-id="59d31-156">Select the **Set** check box.</span></span>
15. <span data-ttu-id="59d31-157">Lauke **Kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="59d31-157">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="59d31-158">Kiekio laukas nustato, kiek šio produkto bus suvartota sukonfigūruotam produktui.</span><span class="sxs-lookup"><span data-stu-id="59d31-158">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="59d31-159">Pažymėkite **Nustatyti** laukelį.</span><span class="sxs-lookup"><span data-stu-id="59d31-159">Select the **Set** check box.</span></span>
17. <span data-ttu-id="59d31-160">Lauke **Pagal serijas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="59d31-160">In the **Per series** field, enter a number.</span></span>
18. <span data-ttu-id="59d31-161">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="59d31-161">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]