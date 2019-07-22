---
title: Sugeneruotų ER ataskaitų rezultatų sekimo ir palyginimo su bazinėmis vertėmis patobulinimai
description: Šioje temoje pateikiama informacija apie tai, kaip pagerinta ER pagrindinės informacijos funkcija „Microsoft Dynamics 365 for Finance and Operations“ 10.0.3 versijoje (2019 m. birželio mėn.).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 222a415f686c8028fc2a414f97eed0291d850ae7
ms.sourcegitcommit: 9917df8c0c9320955c61186cd922c8df894a4f25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/21/2019
ms.locfileid: "1700687"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a><span data-ttu-id="3537d-103">Sugeneruotų ER ataskaitų rezultatų sekimo ir palyginimo su bazinėmis vertėmis patobulinimai</span><span class="sxs-lookup"><span data-stu-id="3537d-103">Improvements in tracing the results of generated ER reports and comparing them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3537d-104">Šioje temoje aprašomas pirmasis patobulinimų, kurie atlikti kuriant elektroninių ataskaitų (ER) sistemą, rinkinys.</span><span class="sxs-lookup"><span data-stu-id="3537d-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="3537d-105">Šie patobulinimai galimi „Microsoft Dynamics 365 for Finance and Operations“ 10.0.3 (2019 m. birželio mėn.) ir naujesnėse versijose.</span><span class="sxs-lookup"><span data-stu-id="3537d-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="3537d-106">Automatizuokite pagrindinių taisyklių nustatymą</span><span class="sxs-lookup"><span data-stu-id="3537d-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="3537d-107">Temoje [Sugeneruotų ataskaitų rezultatų sekimas ir jų palyginimas su bazinėmis vertėmis](er-trace-reports-compare-baseline.md) paaiškinama, kaip konfigūruoti ER sistemą, siekiant surinkti informaciją apie ER formato vykdymą ir įvertinti šio vykdymo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="3537d-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="3537d-108">Šioje temoje pateiktame pavyzdyje parodyti veiksmai, kuriuos reikia atlikti.</span><span class="sxs-lookup"><span data-stu-id="3537d-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="3537d-109">Toliau pateikiami kai kurie veiksmai.</span><span class="sxs-lookup"><span data-stu-id="3537d-109">Here are some of the steps:</span></span>

- <span data-ttu-id="3537d-110">Vykdykite ER formatą, kad būtų sugeneruotas siunčiamas failas, ir išsaugokite failą vietoje.</span><span class="sxs-lookup"><span data-stu-id="3537d-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="3537d-111">Įtraukite vietoje saugomą failą kaip pagrindinės informacijos, kuri buvo pridėta prie ER formato, priedą.</span><span class="sxs-lookup"><span data-stu-id="3537d-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="3537d-112">Konfigūruokite įtrauktos pagrindinės informacijos pagrindinę taisyklę.</span><span class="sxs-lookup"><span data-stu-id="3537d-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="3537d-113">Ši konfigūracija apima toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3537d-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="3537d-114">Nurodykite ER formato elementą, naudojamą siunčiamam failui generuoti.</span><span class="sxs-lookup"><span data-stu-id="3537d-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="3537d-115">Pasirinkite priedą, nurodantį sugeneruotą siunčiamą failą.</span><span class="sxs-lookup"><span data-stu-id="3537d-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="3537d-116">Šiuos veiksmus reikia atlikti patiems, net jei naujos ER galimybės leidžia juos atlikti automatiškai.</span><span class="sxs-lookup"><span data-stu-id="3537d-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="3537d-117">Norėdami daugiau sužinoti apie šią funkciją, atlikite toliau pateiktą pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="3537d-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="3537d-118">Pavyzdys. Automatizuokite pagrindinių taisyklių nustatymą</span><span class="sxs-lookup"><span data-stu-id="3537d-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="3537d-119">Norėdami atlikti šiame pavyzdyje nurodytus veiksmus, pirmiausia turite atlikti veiksmus, aprašytus pavyzdyje, esančiame temos [Sugeneruotų ataskaitų rezultatų sekimas ir jų palyginimas su bazinėmis vertėmis](er-trace-reports-compare-baseline.md) skyriuje „Naujos pagrindinės informacijos įtraukimas pagal sukurtą ER formatą“.</span><span class="sxs-lookup"><span data-stu-id="3537d-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="3537d-120">Įtrauktos pagrindinės informacijos peržiūra</span><span class="sxs-lookup"><span data-stu-id="3537d-120">Review added baseline</span></span>

1. <span data-ttu-id="3537d-121">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="3537d-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="3537d-122">Pasirinkite **Pagrindinė informacija**.</span><span class="sxs-lookup"><span data-stu-id="3537d-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3537d-123">Veiksmų srities mygtukas **Pagrindinė informacija** yra tik tada, kai įjungtas šios įmonės ER vartotojo parametras **Vykdyti derinimo režimu**.</span><span class="sxs-lookup"><span data-stu-id="3537d-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="3537d-124">Įtraukta pasirinkto formato **Formatas, kuris turi mokytis ER pagrindinę informaciją** pagrindinė informacija, tačiau dar neįtrauktos šios pagrindinės informacijos pagrindinės taisyklės.</span><span class="sxs-lookup"><span data-stu-id="3537d-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="3537d-125">![Elektroninių ataskaitų formato pagrindinės informacijos puslapis](media/GER-BaselineSample-AddBaseline2.PNG "Elektroninių ataskaitų formato pagrindinės informacijos puslapio ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="3537d-125">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="3537d-126">Naujos pagrindinės taisyklės kūrimas</span><span class="sxs-lookup"><span data-stu-id="3537d-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="3537d-127">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="3537d-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="3537d-128">Medyje išplėskite **Modelis, kuris turi mokytis ER pagrindinę informaciją**.</span><span class="sxs-lookup"><span data-stu-id="3537d-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="3537d-129">Medyje pasirinkite **Modelis, kuris turi mokytis ER pagrindinę informaciją\\Formatas, kuris turi mokytis ER pagrindinę informaciją**.</span><span class="sxs-lookup"><span data-stu-id="3537d-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="3537d-130">„FastTab“ **Versijos** pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="3537d-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="3537d-131">Lauke **Įveskite ID** įveskite **1**.</span><span class="sxs-lookup"><span data-stu-id="3537d-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="3537d-132">Nustatykite parinkties **Kurti pagrindinės informacijos failus** reikšmę kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="3537d-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="3537d-133">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3537d-133">Select **OK**.</span></span>

    <span data-ttu-id="3537d-134">![Elektroninių ataskaitų parametrų dialogo langas](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Elektroninių ataskaitų parametrų dialogo lango ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="3537d-134">![Electronic report parameters dialog box](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Screenshot of the Electronic report parameters dialog box")</span></span>

8. <span data-ttu-id="3537d-135">Pasirinkite **Pagrindinė informacija**.</span><span class="sxs-lookup"><span data-stu-id="3537d-135">Select **Baselines**.</span></span>

    <span data-ttu-id="3537d-136">![Elektroninių ataskaitų formato pagrindinės informacijos puslapis](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Elektroninių ataskaitų formato pagrindinės informacijos puslapio ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="3537d-136">![Electronic reporting format baselines page](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="3537d-137">Sugeneruotas siuntimo failas buvo automatiškai pridėtas prie vykdyto ER formato pagrindinės informacijos.</span><span class="sxs-lookup"><span data-stu-id="3537d-137">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="3537d-138">Pagrindinė taisyklė buvo automatiškai įtraukta į šią pagrindinę informaciją; joje yra ir nuoroda į pridėtą failą.</span><span class="sxs-lookup"><span data-stu-id="3537d-138">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="3537d-139">Lauke **Pavadinimas** įveskite **1 pagrindinė informacija**.</span><span class="sxs-lookup"><span data-stu-id="3537d-139">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="3537d-140">Lauke **Failo vardo šablonas** įveskite **.xml**.</span><span class="sxs-lookup"><span data-stu-id="3537d-140">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="3537d-141">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3537d-141">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="3537d-142">Formato vykdymas</span><span class="sxs-lookup"><span data-stu-id="3537d-142">Run the format</span></span>

<span data-ttu-id="3537d-143">Dabar esate pasiruošę atlikti likusius veiksmus, nurodytus pavyzdyje, esančiame temoje [Sugeneruotų ataskaitų rezultatų sekimas ir jų palyginimas su bazinėmis vertėmis](er-trace-reports-compare-baseline.md), pradedant nuo skyriaus „Vykdyti sukurtą ER formatą ir peržiūrėti žurnalą, kad būtų išanalizuoti rezultatai“.</span><span class="sxs-lookup"><span data-stu-id="3537d-143">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="3537d-144">Kai panaikinate automatiškai įtrauktą pagrindinę taisyklę, esančią „FastTab“ **Pagrindinė informacija**, nurodytas priedas nėra automatiškai panaikinamas.</span><span class="sxs-lookup"><span data-stu-id="3537d-144">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="3537d-145">Konfigūruokite pagrindinę informaciją, kad ji ignoruotų nuolat besikeičiančias ER išvesties dalis</span><span class="sxs-lookup"><span data-stu-id="3537d-145">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="3537d-146">Sukūrus ER formatą, kuriame yra informacijos, kuri keičiasi vykdant formatą, turi būti reikalaujama, kad, norint palyginti sugeneruotus rezultatus su bazinėmis vertėmis, reikia naudoti ER pagrindinės informacijos funkciją.</span><span class="sxs-lookup"><span data-stu-id="3537d-146">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="3537d-147">Pavyzdžiui, informacija gali būti sugeneruoto dokumento vykdymo data ir laikas arba unikalusis identifikatorius skirtingais formatais (visuotinis unikalusis identifikatorius \[GUID\] ir t. t.).</span><span class="sxs-lookup"><span data-stu-id="3537d-147">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="3537d-148">Naujosios ER galimybės leidžia sukonfigūruoti pagrindinę taisyklę, kad būtų nepaisoma ER formato besikeičiančių elementų, kai formatas yra vykdomas siekiant palyginti bazines vertes su formato vykdymo rezultatais.</span><span class="sxs-lookup"><span data-stu-id="3537d-148">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="3537d-149">Norėdami daugiau sužinoti apie šią funkciją, atlikite toliau pateiktą pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="3537d-149">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="3537d-150">Pavyzdys. Konfigūruokite pagrindinę informaciją, kad ji ignoruotų nuolat besikeičiančias ER išvesties dalis</span><span class="sxs-lookup"><span data-stu-id="3537d-150">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="3537d-151">Norėdami atlikti šiame pavyzdyje nurodytus veiksmus, pirmiausia turite atlikti veiksmus, aprašytus pavyzdyje, esančiame temoje [Sugeneruotų ataskaitų rezultatų sekimas ir jų palyginimas su bazinėmis vertėmis](er-trace-reports-compare-baseline.md).</span><span class="sxs-lookup"><span data-stu-id="3537d-151">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="3537d-152">Sukonfigūruoto ER formato modifikavimas</span><span class="sxs-lookup"><span data-stu-id="3537d-152">Modify a configured ER format</span></span>

1. <span data-ttu-id="3537d-153">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="3537d-153">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="3537d-154">Medyje išplėskite **Modelis, kuris turi mokytis ER pagrindinę informaciją**.</span><span class="sxs-lookup"><span data-stu-id="3537d-154">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="3537d-155">Medyje pasirinkite **Modelis, kuris turi mokytis ER pagrindinę informaciją\\Formatas, kuris turi mokytis ER pagrindinę informaciją**.</span><span class="sxs-lookup"><span data-stu-id="3537d-155">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="3537d-156">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="3537d-156">Select **Designer**.</span></span>
5. <span data-ttu-id="3537d-157">Medyje pasirinkite **Išvestis\\Dokumentas**.</span><span class="sxs-lookup"><span data-stu-id="3537d-157">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="3537d-158">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="3537d-158">Select **Add**.</span></span>
7. <span data-ttu-id="3537d-159">Išplečiamojo dialogo lango medyje pasirinkite **XML\\Atributas**.</span><span class="sxs-lookup"><span data-stu-id="3537d-159">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="3537d-160">Lauke **Pavadinimas** įveskite **ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="3537d-160">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="3537d-161">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3537d-161">Select **OK**.</span></span>
10. <span data-ttu-id="3537d-162">Medžio skirtuke **Susiejimas** pasirinkite **Išvestis\\Dokumentas\\ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="3537d-162">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="3537d-163">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="3537d-163">Select **Edit formula**.</span></span>
12. <span data-ttu-id="3537d-164">Lauke **Formulė** įveskite toliau nurodytą išraišką: **DATETIMEFORMAT(NOW(), "O")**.</span><span class="sxs-lookup"><span data-stu-id="3537d-164">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="3537d-165">Pasirinkite **Įrašyti**, tada pasirinkite **Testuoti**.</span><span class="sxs-lookup"><span data-stu-id="3537d-165">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="3537d-166">Norėdami dar kartą testuoti sukonfigūruotą išraišką pasirinkite **Testuoti**.</span><span class="sxs-lookup"><span data-stu-id="3537d-166">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="3537d-167">![Formulių dizaino įrankio puslapis](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Formulių dizaino įrankio puslapio ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="3537d-167">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="3537d-168">Skirtuke **Testo vykdymo rezultatas** nurodoma, kad sukonfigūruota išraiška ją iškvietus pateikia kitą datos ir laiko vertę.</span><span class="sxs-lookup"><span data-stu-id="3537d-168">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="3537d-169">Uždarykite puslapį **Formulių kūrimo įrankis** ir pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3537d-169">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="3537d-170">![Formato dizaino įrankio puslapis](media/GER-BaselineSample-FormatMappingDesign2.PNG "Formato dizaino įrankio puslapio ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="3537d-170">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="3537d-171">Uždarykite puslapį **Formato dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="3537d-171">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="3537d-172">Esamos pagrindinės taisyklės šalinimas</span><span class="sxs-lookup"><span data-stu-id="3537d-172">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="3537d-173">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="3537d-173">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="3537d-174">Pasirinkite **Pagrindinė informacija**.</span><span class="sxs-lookup"><span data-stu-id="3537d-174">Select **Baselines**.</span></span>
3. <span data-ttu-id="3537d-175">Pagrindinės informacijos sąraše pasirinkite pagrindinę informaciją, kuri sukonfigūruota formatui **Formatas, kuris turi mokytis ER pagrindinę informaciją**.</span><span class="sxs-lookup"><span data-stu-id="3537d-175">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="3537d-176">Norėdami pašalinti anksčiau sukonfigūruotą pagrindinę taisyklę „FastTab“ **Pagrindinė informacija** pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="3537d-176">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="3537d-177">![Elektroninių ataskaitų formato pagrindinės informacijos puslapis](media/GER-BaselineSample-AddBaseline3.PNG "Elektroninių ataskaitų formato pagrindinės informacijos puslapio ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="3537d-177">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="3537d-178">Apibrėžkite sukurto ER formato susiejimų keitimus</span><span class="sxs-lookup"><span data-stu-id="3537d-178">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="3537d-179">Puslapio **Konfigūracijos** „FastTab“ **Pakeitimai** pasirinkite **Pasirinkite komponentus**.</span><span class="sxs-lookup"><span data-stu-id="3537d-179">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="3537d-180">Formato komponentų medyje išplėskite **Išvestis**, išplėskite **Išvestis\\Dokumentas**, tada pažymėkite žymės langelį **Išvestis\\Dokumentas\\ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="3537d-180">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>

    <span data-ttu-id="3537d-181">![Komponentų pasirinkimo dialogo langas](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Komponentų pasirinkimo dialogo lango ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="3537d-181">![Select Components dialog box](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Screenshot of the Select Components dialog box")</span></span>

3. <span data-ttu-id="3537d-182">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3537d-182">Select **OK**.</span></span>

<span data-ttu-id="3537d-183">![Elektroninių ataskaitų formato pagrindinės informacijos puslapis](media/GER-BaselineSample-AddBaseline4.PNG "Elektroninių ataskaitų formato pagrindinės informacijos puslapio ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="3537d-183">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="3537d-184">Pasirinktas ER formato komponentas buvo įtrauktas į komponentų sąrašą „FastTab“ **Pakeitimai**.</span><span class="sxs-lookup"><span data-stu-id="3537d-184">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="3537d-185">Kai pagrindinis ER formatas vykdomas derinimo režimu, kiekvieno komponento formato susiejimas bus pakeistas susiejiimu, kuris parodytas stulpelyje **Susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="3537d-185">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="3537d-186">Norėdami pakeisti numatytąjį susiejimą komponento, kuris yra nurodytas „FastTab“ **Pakeitimai**, pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="3537d-186">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="3537d-187">Naujos pagrindinės taisyklės kūrimas</span><span class="sxs-lookup"><span data-stu-id="3537d-187">Make a new baseline rule</span></span>

<span data-ttu-id="3537d-188">Atlikite veiksmus, aprašytus anksčiau šios temos skyriuje „Pavyzdys. Automatizuokite pagrindinių taisyklių nustatymą“.</span><span class="sxs-lookup"><span data-stu-id="3537d-188">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="3537d-189">Pranešimas įspėja, kad siunčiamas failas buvo sugeneruotas naudojant pagrindinės informacijos parametrus ir kad įvyko priverstinis formato susiejimų pakeitimas.</span><span class="sxs-lookup"><span data-stu-id="3537d-189">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="3537d-190">![Pranešimas konfigūracijų puslapyje](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Pranešimo konfigūracijų puslapyje ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="3537d-190">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="3537d-191">Įspėjimų apie formato susiejimų pakeitimą slėpimas</span><span class="sxs-lookup"><span data-stu-id="3537d-191">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="3537d-192">Nustatydami tam tikrus ER parametrus, galite paslėpti pranešimus, įspėjančius apie formato susiejimų pakeitimą.</span><span class="sxs-lookup"><span data-stu-id="3537d-192">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="3537d-193">Šis slėpimas gali būti naudingas, kai formato susiejimai pakeičiami režimu be priežiūros, naudojant „Regression Suite Automation Tool“.</span><span class="sxs-lookup"><span data-stu-id="3537d-193">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="3537d-194">Šiuo atveju įspėjimas gali būti laikomas kaip vykdomo testavimo atvejo triktis.</span><span class="sxs-lookup"><span data-stu-id="3537d-194">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="3537d-195">Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos** pasirinkite **Vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="3537d-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="3537d-196">Nustatykite parinkties **Slėpti pagrindinės informacijos įspėjimus** reikšmę kaip **Taip**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3537d-196">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

<span data-ttu-id="3537d-197">![Vartotojo parametrų dialogo langas](media/GER-BaselineSample-ERUserParameters1.png "Vartotojo parametrų dialogo lango ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="3537d-197">![User parameters dialog box](media/GER-BaselineSample-ERUserParameters1.png "Screenshot of the User parameters dialog box")</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="3537d-198">Peržiūrėkite sugeneruotą pagrindinės informacijos failą</span><span class="sxs-lookup"><span data-stu-id="3537d-198">Review the generated baseline file</span></span>

1. <span data-ttu-id="3537d-199">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="3537d-199">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="3537d-200">Pasirinkite **Pagrindinė informacija**.</span><span class="sxs-lookup"><span data-stu-id="3537d-200">Select **Baselines**.</span></span>
3. <span data-ttu-id="3537d-201">Pasirinkite **Priedai**.</span><span class="sxs-lookup"><span data-stu-id="3537d-201">Select **Attachments**.</span></span>

    <span data-ttu-id="3537d-202">![Priedų puslapis](media/GER-BaselineSample-AttachedBaselineFile.PNG "Priedų puslapio ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="3537d-202">![Attachments page](media/GER-BaselineSample-AttachedBaselineFile.PNG "Screenshot of the Attachments page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="3537d-203">Sugeneruotame faile yra vykdymo datos ir laiko tekstas (**#**) iš susiejimo, kuris buvo sukonfigūruotas įtrauktoje pagrindinėje taisyklėje, o ne iš formato susiejimo.</span><span class="sxs-lookup"><span data-stu-id="3537d-203">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>

4. <span data-ttu-id="3537d-204">Uždarykite puslapį **Priedai**.</span><span class="sxs-lookup"><span data-stu-id="3537d-204">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="3537d-205">Vykdyti sukurtą ER formatą ir peržiūrėti žurnalą, kad būtų išanalizuoti rezultatai</span><span class="sxs-lookup"><span data-stu-id="3537d-205">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="3537d-206">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="3537d-206">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="3537d-207">Medyje išplėskite **Modelis, kuris turi mokytis ER pagrindinę informaciją**.</span><span class="sxs-lookup"><span data-stu-id="3537d-207">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="3537d-208">Medyje pasirinkite **Modelis, kuris turi mokytis ER pagrindinę informaciją\\Formatas, kuris turi mokytis ER pagrindinę informaciją**.</span><span class="sxs-lookup"><span data-stu-id="3537d-208">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="3537d-209">„FastTab“ **Versijos** pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="3537d-209">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="3537d-210">Lauke **Įveskite ID** įveskite **1**.</span><span class="sxs-lookup"><span data-stu-id="3537d-210">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="3537d-211">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3537d-211">Select **OK**.</span></span>
7. <span data-ttu-id="3537d-212">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos derinimo žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="3537d-212">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="3537d-213">Vykdymo žurnale yra informacijos apie sugeneruoto failo palyginimo su sukonfigūruota pagrindine informacija rezultatus.</span><span class="sxs-lookup"><span data-stu-id="3537d-213">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="3537d-214">Žurnalas nurodo, kad sugeneruotas failas ir pagrindinė informacija yra vienodi, net jei vykdytame formate yra susiejimas, kad siunčiamame faile būtų galima įvesti nuolat besikeičiančias datos ir laiko vertes.</span><span class="sxs-lookup"><span data-stu-id="3537d-214">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="3537d-215">Nors siuntimo failas buvo sugeneruotas naudojant pagrindinės informacijos parametrus, kurie lėmė priverstinį formato susiejimų pakeitimą, negaunate įspėjimų apie pakeitimą.</span><span class="sxs-lookup"><span data-stu-id="3537d-215">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="3537d-216">Pagrindinės informacijos parametrų keitimas tarp aplinkų</span><span class="sxs-lookup"><span data-stu-id="3537d-216">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="3537d-217">Pagrindinės informacijos parametrų eksportavimas</span><span class="sxs-lookup"><span data-stu-id="3537d-217">Export baseline settings</span></span>

<span data-ttu-id="3537d-218">Naujos ER galimybės leidžia eksportuoti pasirinkto ER formato pagrindinės informacijos parametrus iš dabartinės „Finance and Operations“ aplinkos ir juos išsaugoti kaip XML failus.</span><span class="sxs-lookup"><span data-stu-id="3537d-218">The new ER capabilities let you export baseline settings for the selected ER format from the current Finance and Operations environment and store them as XML files.</span></span> 

<span data-ttu-id="3537d-219">Norėdami eksportuoti pagrindinės informacijos parametrus puslapyje **Elektroninių ataskaitų formato pagrindinė informacija** pasirinkite **Eksportuoti**.</span><span class="sxs-lookup"><span data-stu-id="3537d-219">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="3537d-220">Importuoti bazinius parametrus</span><span class="sxs-lookup"><span data-stu-id="3537d-220">Import baseline settings</span></span>

<span data-ttu-id="3537d-221">Eksportuotus pagrindinės informacijos parametrus galima importuoti į kitą „Finance and Operations“ aplinką.</span><span class="sxs-lookup"><span data-stu-id="3537d-221">Exported baseline settings can be imported into a different Finance and Operations environment.</span></span> <span data-ttu-id="3537d-222">Aplinka pirmiausia turi būti importuota kaip ER formatas.</span><span class="sxs-lookup"><span data-stu-id="3537d-222">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="3537d-223">Tada galima importuoti pagrindinės informacijos parametrus.</span><span class="sxs-lookup"><span data-stu-id="3537d-223">You can then import the baseline settings.</span></span>

<span data-ttu-id="3537d-224">Norėdami importuoti pagrindinės informacijos parametrus iš vietoje saugomo XML failo puslapyje **Elektroninių ataskaitų formato pagrindinė informacija** pasirinkite **Importuoti**, tada pasirinkite **Naršyti**, kad pasirinktumėte XML failą.</span><span class="sxs-lookup"><span data-stu-id="3537d-224">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="3537d-225">![Pagrindinės informacijos parametrų importavimo dialogo langas](media/GER-BaselineSample-ImportBaseline1.PNG "Pagrindinės informacijos parametrų importavimo dialogo lango ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="3537d-225">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="3537d-226">Norėdami importuoti pagrindinės informacijos parametrus iš XML failo, kuris saugomas „Microsoft SharePoint Server“ atsižvelgdami į dabartinius dokumentų valdymo parametrus ir pasirinktą dokumento tipą puslapyje **Elektroninių ataskaitų formato pagrindinė informacija** pasirinkite **Importuoti iš šaltinio**.</span><span class="sxs-lookup"><span data-stu-id="3537d-226">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="3537d-227">Tada pasirinkti dokumento tipą ir XML failą.</span><span class="sxs-lookup"><span data-stu-id="3537d-227">Then select the document type and the XML file.</span></span> <span data-ttu-id="3537d-228">Būtinas dokumento tipas, kad būtų galima pasiekti „SharePoint“ aplanką, turi būti sukonfigūruotas iš anksto.</span><span class="sxs-lookup"><span data-stu-id="3537d-228">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="3537d-229">![Importavimo iš šaltinio dialogo langas](media/GER-BaselineSample-ImportBaseline2.PNG "Importavimo iš šaltinio dialogo lango ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="3537d-229">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="3537d-230">Galite naudoti užduočių įrašymo priemonę, kad įrašytumėte reikalingus dokumento tipo ir failo vardo pasirinkimo veiksmus dialogo lange **Importuoti iš šaltinio**.</span><span class="sxs-lookup"><span data-stu-id="3537d-230">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="3537d-231">Tokiu būdu galite išlaikyti privalomus pagrindinės informacijos parametrus „SharePoint Server“, o tada juos automatiškai importuoti, leisdami užduoties įrašą, kai vykdote automatinius testus naudodami „Regression Suite Automation Tool“.</span><span class="sxs-lookup"><span data-stu-id="3537d-231">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3537d-232">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3537d-232">Additional resources</span></span>

- [<span data-ttu-id="3537d-233">Sugeneruotų ataskaitų rezultatų sekimas ir jų palyginimas su bazinėmis vertėmis</span><span class="sxs-lookup"><span data-stu-id="3537d-233">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="3537d-234">Užduoties įrašymo priemonė</span><span class="sxs-lookup"><span data-stu-id="3537d-234">Task recorder</span></span>](../user-interface/task-recorder.md)
