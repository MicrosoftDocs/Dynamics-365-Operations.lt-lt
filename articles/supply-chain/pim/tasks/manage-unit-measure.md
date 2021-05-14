---
title: Matavimo vienetų valdymas
description: Ši tema aprašo, kaip apibrėžti matavimo vienetą, pateikti vieneto vertimus ir jo aprašą ir apibrėžti susijusių vienetų konvertavimo taisykles.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d36839cd8e3398225d3421bf0f268068599ca49f
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921346"
---
# <a name="manage-units-of-measure"></a><span data-ttu-id="3f202-103">Matavimo vienetų valdymas</span><span class="sxs-lookup"><span data-stu-id="3f202-103">Manage units of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f202-104">Ši tema aprašo, kaip apibrėžti matavimo vienetą, pateikti vieneto vertimus ir jo aprašą ir apibrėžti susijusių vienetų konvertavimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="3f202-104">This topic describes how to define a unit of measure, provide translations for the unit and its description, and define conversion rules for related units.</span></span>

## <a name="open-the-units-page"></a><span data-ttu-id="3f202-105">Atidarykite vienetų puslapį</span><span class="sxs-lookup"><span data-stu-id="3f202-105">Open the Units page</span></span>

<span data-ttu-id="3f202-106">Norėdami sukurti ir dirbti su jūsų sistemoje galimais matavimo vienetais, eikite į Organizacijos **administravimo \> vienetų \> nustatymo \>** vienetus.</span><span class="sxs-lookup"><span data-stu-id="3f202-106">To create and work with the units of measure that are available in your system, go to **Organization administration \> Setup \> Units \> Units**.</span></span>

<span data-ttu-id="3f202-107">Likusiuose šios temos skyriuose aprašoma, ką galima padaryti **vienetų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="3f202-107">The remaining sections of this topic describe what you can do on the **Units** page.</span></span>

## <a name="create-standard-units-and-conversions"></a><span data-ttu-id="3f202-108">Standartinių vienetų ir konvertavimų kūrimas</span><span class="sxs-lookup"><span data-stu-id="3f202-108">Create standard units and conversions</span></span>

<span data-ttu-id="3f202-109">Jei jūsų sistemoje dar nėra dažniausiai naudojamų metrinės sistemos ir (arba) JAV įprastinio sistemos (USCS) matavimo vienetų, vieneto nustatymo vedlys gali padėti greitai pradėti pradedant nuo pagrindinių vienetų apibrėžimų ir konvertavimų.</span><span class="sxs-lookup"><span data-stu-id="3f202-109">If your system doesn't already include the most commonly used units of measure for the metric system and/or the US customary system (USCS), the unit setup wizard can help you quickly get started with basic unit definitions and conversions.</span></span> <span data-ttu-id="3f202-110">Norėdami užbaigti vedlį, veiksmų srityje pasirinkite Vienetų kūrimo vedlys, tada **vykdykite** ekrano instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="3f202-110">To complete the wizard, select **Unit creation wizard** on the Action Pane, and then follow the on-screen instructions.</span></span>

## <a name="create-or-edit-a-unit-of-measure"></a><span data-ttu-id="3f202-111">Kurti ar redaguoti matavimo vienetą</span><span class="sxs-lookup"><span data-stu-id="3f202-111">Create or edit a unit of measure</span></span>

<span data-ttu-id="3f202-112">Norėdami kurti arba redaguoti matavimo vienetą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3f202-112">To create or edit a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="3f202-113">Atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="3f202-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="3f202-114">Norėdami redaguoti esamą vienetą, pasirinkite jį sąrašo srityje.</span><span class="sxs-lookup"><span data-stu-id="3f202-114">To edit an existing unit, select it in the list pane.</span></span>
    - <span data-ttu-id="3f202-115">Norėdami sukurti naują vienetą, pasirinkite **Nauja** veiksmų juostoje.</span><span class="sxs-lookup"><span data-stu-id="3f202-115">To create a new unit, select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="3f202-116">Naujojo įrašo antraštėje nustatykite toliau pateiktus laukus:</span><span class="sxs-lookup"><span data-stu-id="3f202-116">On the header of the record, set the following fields:</span></span>

    - <span data-ttu-id="3f202-117">**Vienetas** – įveskite identifikatorių arba simbolį, naudotiį vienetą nurodyti sistemos kalba.</span><span class="sxs-lookup"><span data-stu-id="3f202-117">**Unit** – Enter the ID or symbol to use to refer to the unit in the system language.</span></span> <span data-ttu-id="3f202-118">Šis ID arba simbolis paprastai yra įprasta vieneto santrumpa, pvz., *kiekvienai* arba *centimetro* cm.</span><span class="sxs-lookup"><span data-stu-id="3f202-118">This ID or symbol is usually a common abbreviation for the unit, such as *ea* for each or *cm* for centimeter.</span></span>
    - <span data-ttu-id="3f202-119">**Aprašas** – Įveskite matavimo vieneto aprašomąjį pavadinimą sistemos kalba.</span><span class="sxs-lookup"><span data-stu-id="3f202-119">**Description** – Enter a descriptive name for the unit in the system language.</span></span> <span data-ttu-id="3f202-120">Šis pavadinimas paprastai yra visas vieneto pavadinimas, pvz., *Kiekvienas* arba *Centimetras*.</span><span class="sxs-lookup"><span data-stu-id="3f202-120">This name is usually the full name of the unit, such as *Each* or *Centimeter*.</span></span>

1. <span data-ttu-id="3f202-121">„FastTab“ **Bendra** nustatykite toliau pateikiamus laukus.</span><span class="sxs-lookup"><span data-stu-id="3f202-121">On the **General** FastTab, set the following fields:</span></span><!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - <span data-ttu-id="3f202-122">**Vieneto** klasė – pasirinkite vieneto matavimo ypatybę (pvz., ilgį, sritį, masę arba kiekį).</span><span class="sxs-lookup"><span data-stu-id="3f202-122">**Unit class** – Select the property that the unit measures (such as length, area, mass, or quantity).</span></span>
    - <span data-ttu-id="3f202-123">**Vienetų sistema** – pasirinkite matavimo sistemą, kuriai priklauso vienetas (*Metriniai vienetai* arba *Jungtinių Valstijų pasirinktiniai* vienetai).</span><span class="sxs-lookup"><span data-stu-id="3f202-123">**System of units** – Select the measurement system that the unit belongs to (*Metric units* or *United States customary units*).</span></span>
    - <span data-ttu-id="3f202-124">**Pagrindinis** vienetas – nustatykite šią *pasirinktį kaip Taip* , jei norite dabartinį vienetą naudoti kaip pagrindinį vieneto klasės vienetą.</span><span class="sxs-lookup"><span data-stu-id="3f202-124">**Base unit** – Set this option to *Yes* to use the current unit as the base unit for its unit class.</span></span> <span data-ttu-id="3f202-125">Šiuo atveju vienetų klasėje turite nurodyti tik pagrindinio vieneto ir kiekvieno papildomo vieneto konvertavimo koeficientą.</span><span class="sxs-lookup"><span data-stu-id="3f202-125">In this case, you only have to specify the conversion factor between the base unit and each additional unit in the unit class.</span></span> <span data-ttu-id="3f202-126">Sistema gali konvertuoti visus tos vieneto klasės vienetus.</span><span class="sxs-lookup"><span data-stu-id="3f202-126">The system can then convert between all units in that unit class.</span></span> <span data-ttu-id="3f202-127">Todėl lengviau nustatyti konvertavimą.</span><span class="sxs-lookup"><span data-stu-id="3f202-127">Therefore, it's easier to set up conversions.</span></span>

        <span data-ttu-id="3f202-128">Pavyzdžiui, jei galonas yra pagrindinis tūrio vieneto klasės vienetas, turite nustatyti tik konvertavimo koeficientus iš litro į galoną ir *iš* pinto į galoną.</span><span class="sxs-lookup"><span data-stu-id="3f202-128">For example, if gallon is the base unit for the *Volume* unit class, you only have to set up conversion factors from quart to gallon and from pint to gallon.</span></span> <span data-ttu-id="3f202-129">Sistema taip pat gali konvertuoti iš kvorto į pint.</span><span class="sxs-lookup"><span data-stu-id="3f202-129">The system can then also convert from quart to pint.</span></span>

        <span data-ttu-id="3f202-130">Vienoje vieneto klasėje gali būti tik vienas pagrindinis vienetas.</span><span class="sxs-lookup"><span data-stu-id="3f202-130">You can have only one base unit per unit class.</span></span>

    - <span data-ttu-id="3f202-131">**Sistemos** vienetas – nustatykite šią *pasirinktį kaip Taip* , jei norite dabartinį vienetą naudoti kaip prisiimtus visus matavimus klasės vienete.</span><span class="sxs-lookup"><span data-stu-id="3f202-131">**System unit** – Set this option to *Yes* to use the current unit as the assumed unit for all unspecified measurements in its unit class.</span></span> <span data-ttu-id="3f202-132">Pavyzdžiui, jei laukas, kuris naudojamas kiekiui įvesti, neleidžia nurodyti vieneto (jei vartotojas nepasirinko vieneto), sistema naudoja vienetą, kuris nustatytas kaip kiekio vieneto klasės sistemos *vienetas*.</span><span class="sxs-lookup"><span data-stu-id="3f202-132">For example, if a field that is used to enter a quantity doesn't allow a unit to be specified (of if the user doesn't select a unit), the system uses the unit that is set as the system unit for the *Quantity* unit class.</span></span> <span data-ttu-id="3f202-133">Vienoje vieneto klasėje gali būti tik vienas sistemos vienetas.</span><span class="sxs-lookup"><span data-stu-id="3f202-133">You can have only one system unit per unit class.</span></span>
    - <span data-ttu-id="3f202-134">**Dešimtainis tikslumas – nurodykite dešimtainių dalių vietų, kurios yra nurodytos dabartiniam vienetui arba kurias reikia** apvalinti, skaičių.</span><span class="sxs-lookup"><span data-stu-id="3f202-134">**Decimal precision** – Specify the number of decimal places that values that are specified for the current unit or converted to it should be rounded to.</span></span>

1. <span data-ttu-id="3f202-135">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3f202-135">On the Action Pane, select **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="3f202-136">Apibrėžti vieneto vertimus</span><span class="sxs-lookup"><span data-stu-id="3f202-136">Define unit translations</span></span>

<span data-ttu-id="3f202-137">Norėdami nurodyti ID arba simbolio vertimus ir matavimo vieneto aprašymą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3f202-137">To define translations for the ID or symbol and the description for a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="3f202-138">Sukurkite arba pasirinkite vienetą, į lauką kursite vertimus.</span><span class="sxs-lookup"><span data-stu-id="3f202-138">Create or select the unit to create translations for.</span></span>
1. <span data-ttu-id="3f202-139">Veiksmų srityje pasirinkite **Vieneto tekstai**.</span><span class="sxs-lookup"><span data-stu-id="3f202-139">On the Action Pane, select **Unit texts**.</span></span>

    <span data-ttu-id="3f202-140">Rodomas **puslapis** Vieneto tekstai.</span><span class="sxs-lookup"><span data-stu-id="3f202-140">The **Unit texts** page appears.</span></span> <span data-ttu-id="3f202-141">Šį puslapį naudojate pasirinkto vieneto ID arba simbolio vertimams nustatyti.</span><span class="sxs-lookup"><span data-stu-id="3f202-141">You use this page to define translations for the ID or symbol for the selected unit.</span></span> <span data-ttu-id="3f202-142">Tada šiuos vertimus galima naudoti išoriniuose dokumentuose kliento ar tiekėjo kalba.</span><span class="sxs-lookup"><span data-stu-id="3f202-142">Those translations can then be used on external documents in customer-specific or vendor-specific languages.</span></span>

1. <span data-ttu-id="3f202-143">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="3f202-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3f202-144">**Kalba** – laukelyje pasirinkite kalbą norėdami išversti vieneto ID ar simbolį.</span><span class="sxs-lookup"><span data-stu-id="3f202-144">In the **Language** field, select the language to translate the unit ID or symbol to.</span></span>
1. <span data-ttu-id="3f202-145">Į **lauką** Tekstas įveskite vieneto ID arba simbolio vertimą pasirinkta kalba.</span><span class="sxs-lookup"><span data-stu-id="3f202-145">In the **Text** field, enter the translation of the unit ID or symbol in the selected language.</span></span>
1. <span data-ttu-id="3f202-146">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3f202-146">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="3f202-147">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3f202-147">Close the page.</span></span>
1. <span data-ttu-id="3f202-148">**Veiksmų srityje** pasirinkite **Išversti vienetų aprašai**.</span><span class="sxs-lookup"><span data-stu-id="3f202-148">On the **Action Pane**, select **Translated unit descriptions**.</span></span>

    <span data-ttu-id="3f202-149">Rodomas **išverstų vienetų** aprašų puslapis.</span><span class="sxs-lookup"><span data-stu-id="3f202-149">The **Translated unit descriptions** page appears.</span></span> <span data-ttu-id="3f202-150">Šį puslapį naudojate norėdami nustatyti pasirinkto vieneto aprašus konkrečia kalba.</span><span class="sxs-lookup"><span data-stu-id="3f202-150">You use this page to define language-specific descriptions for the selected unit.</span></span>

1. <span data-ttu-id="3f202-151">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="3f202-151">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3f202-152">**Kalba** – laukelyje pasirinkite kalbą norėdami išversti vieneto ID ar aprašą.</span><span class="sxs-lookup"><span data-stu-id="3f202-152">In the **Language** field, select the language to translate the unit description to.</span></span>
1. <span data-ttu-id="3f202-153">Į **Aprašą** Tekstas įveskite vieneto ID arba aprašo vertimą pasirinkta kalba.</span><span class="sxs-lookup"><span data-stu-id="3f202-153">In the **Description** field, enter the translation of the unit description in the selected language.</span></span>
1. <span data-ttu-id="3f202-154">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3f202-154">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="3f202-155">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3f202-155">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="3f202-156">Apibrėžti vieneto konvertavimo taisykles</span><span class="sxs-lookup"><span data-stu-id="3f202-156">Define unit conversion rules</span></span>

<span data-ttu-id="3f202-157">Norėdami nustatyti konvertavimo tarp matavimo vienetų taisykles, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3f202-157">To define rules for conversions between units of measure, follow these steps.</span></span>

1. <span data-ttu-id="3f202-158">Sukurkite arba pasirinkite vienetą norėdami nustatyti vertimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="3f202-158">Create or select the unit to define conversion rules for.</span></span>
1. <span data-ttu-id="3f202-159">Veiksmų srityje pasirinkite **Vieneto pavertimas**.</span><span class="sxs-lookup"><span data-stu-id="3f202-159">On the Action Pane, select **Unit conversions**.</span></span>

    <span data-ttu-id="3f202-160">Atidaromas puslapis **Vienetų konvertavimas**.</span><span class="sxs-lookup"><span data-stu-id="3f202-160">The **Unit conversions** page appears.</span></span> <span data-ttu-id="3f202-161">Naudojate šį puslapį, kad nustatytumėte pasirinkto vieneto keitimą į ir iš kitų vienetų vieneto klasėje.</span><span class="sxs-lookup"><span data-stu-id="3f202-161">You use this page to define rules for converting the selected unit to and from other units in the unit class.</span></span>

1. <span data-ttu-id="3f202-162">Pasirinkite vieną iš šių skirtukų priklausomai nuo konvertavimo tipo, kurį norite nustatyti:</span><span class="sxs-lookup"><span data-stu-id="3f202-162">Select one of the following tabs, depending on the type of conversion that you want to set up:</span></span>

    - <span data-ttu-id="3f202-163">**Standartiniai konvertavimai** – nustatyti standartines konvertavimo taisykles visiems produktams.</span><span class="sxs-lookup"><span data-stu-id="3f202-163">**Standard conversions** – Set up standard conversion rules for all products.</span></span>
    - <span data-ttu-id="3f202-164">**Konvertavimai klasės viduje** – nustatyti su konkrečiu produktu taikomas tos pačios vieneto klasės vienetų konvertavimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="3f202-164">**Intra-class conversions** – Set up product-specific conversion rules for units in the same unit class.</span></span>
    - <span data-ttu-id="3f202-165">**Konvertavimai klasės viduje** – nustatyti su konkrečiu produktu taikomas tos pačios vieneto klasės vienetų konvertavimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="3f202-165">**Inter-class conversions** – Set up product-specific conversion rules for units across unit classes.</span></span>

1. <span data-ttu-id="3f202-166">Atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="3f202-166">Follow one of these steps:</span></span>

    - <span data-ttu-id="3f202-167">Norėdami sukurti naują keitimą, pasirinkite **Nauja** įrankių juostoje.</span><span class="sxs-lookup"><span data-stu-id="3f202-167">To create a new conversion, select **New** on the toolbar.</span></span>
    - <span data-ttu-id="3f202-168">Norėdami redaguoti esamą konvertavimą, pasirinkite konvertavimą tinklelyje ir įrankių **juostoje** pasirinkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="3f202-168">To edit an existing conversion, select the conversion in the grid, and then select **Edit** on the toolbar.</span></span>

1. <span data-ttu-id="3f202-169">Pasirodžiusiame iškritusiame teksto lange nustatykite tolesnius laukus:</span><span class="sxs-lookup"><span data-stu-id="3f202-169">In the drop-down dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="3f202-170">**Produktas** – pasirinkite konkretų produktą, kurį taikomas konvertavimas.</span><span class="sxs-lookup"><span data-stu-id="3f202-170">**Product** – Select the specific product that the conversion applies to.</span></span> <span data-ttu-id="3f202-171">Šis laukas galimas tik konvertavimams tarp klasių ir tarp klasių.</span><span class="sxs-lookup"><span data-stu-id="3f202-171">This field is available only for intra-class and inter-class conversions.</span></span>
    - <span data-ttu-id="3f202-172">**Formulės** maketas – palikti šį lauką nustatytą kaip *Paprastas,* kad būtų nurodytas paprastas konvertavimas, turintis vieną koeficientą.</span><span class="sxs-lookup"><span data-stu-id="3f202-172">**Formula layout** – Leave this field set to *Simple* to specify a simple conversion that has a single factor.</span></span> <span data-ttu-id="3f202-173">Norėdami nustatyti *sudėtingesnę* lygtį, nustatykite ją išplėstiniu nustatymu.</span><span class="sxs-lookup"><span data-stu-id="3f202-173">Set it to *Advanced* to set up a more complex equation.</span></span> <span data-ttu-id="3f202-174">Išplėstinių lygčių formatas skiriasi, atsižvelgiant į vieneto klasę.</span><span class="sxs-lookup"><span data-stu-id="3f202-174">The format for advanced equations varies, depending on the unit class.</span></span>
    - <span data-ttu-id="3f202-175">**Nuo vieneto** – šiame lauke rodomas pasirinktas vienetas.</span><span class="sxs-lookup"><span data-stu-id="3f202-175">**From unit** – This field shows the selected unit.</span></span> <span data-ttu-id="3f202-176">Paprastai vertės keisti nereikia.</span><span class="sxs-lookup"><span data-stu-id="3f202-176">Usually, you should not change the value.</span></span> <span data-ttu-id="3f202-177">(Jei vertę pakeisite, turite atidaryti langą **Pasirinkto vieneto** vienetų konvertavimo puslapis, kuriame galite peržiūrėti naują konvertavimą jį įrašius.)</span><span class="sxs-lookup"><span data-stu-id="3f202-177">(If you do change the value, you must open the **Unit conversions** page for the selected unit to view your new conversion after you save it.)</span></span>
    - <span data-ttu-id="3f202-178">**Į vienetą** – pasirinkite vienetą, į jį konvertuoti.</span><span class="sxs-lookup"><span data-stu-id="3f202-178">**To unit** – Select the unit to convert to.</span></span>
    - <span data-ttu-id="3f202-179">**Apvalinimas** – pasirinkti, kaip apvalinti trupmenas, remiantis pasirinkto vieneto **Dešimtainio tikslumo** pasirinkto vieneto vertė (*Iki artimiausios*, *Aukštyn*, ar *Žemyn*).</span><span class="sxs-lookup"><span data-stu-id="3f202-179">**Rounding** – Select how fractions should be rounded, based on the **Decimal precision** value of the selected unit (*To nearest*, *Up*, or *Down*).</span></span>
    - <span data-ttu-id="3f202-180">**Konvertavimo formulė – naudoti likusius laukus išplečiamojo dialogo lango viršuje, norint nurodyti dviejų** vienetų konvertavimo formulę.</span><span class="sxs-lookup"><span data-stu-id="3f202-180">**Conversion formula** – Use the remaining fields at the top of the drop-down dialog box to specify the formula for converting between the two units.</span></span> <span data-ttu-id="3f202-181">Galimi laukai skiriasi atsižvelgiant į pasirinktą vieneto klasę ir formulės maketą.</span><span class="sxs-lookup"><span data-stu-id="3f202-181">The available fields vary, depending on the unit class and formula layout that you've selected.</span></span>

1. <span data-ttu-id="3f202-182">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3f202-182">Select **OK**.</span></span>
1. <span data-ttu-id="3f202-183">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3f202-183">Close the page.</span></span>

> [!TIP]
> <span data-ttu-id="3f202-184">Taip pat galite nustatyti vieneto konvertavimą produkto variantui.</span><span class="sxs-lookup"><span data-stu-id="3f202-184">You can also set up unit conversions per product variant.</span></span> <span data-ttu-id="3f202-185">Dėl išsamesnės informacijos, žr. [Produkto varianto matavimo vieneto konvertavimas](../uom-conversion-per-product-variant.md).</span><span class="sxs-lookup"><span data-stu-id="3f202-185">For more information, see [Unit of measure conversion per product variant](../uom-conversion-per-product-variant.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
