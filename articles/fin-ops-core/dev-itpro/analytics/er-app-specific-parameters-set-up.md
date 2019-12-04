---
title: ER formato parametrų nustatymas kiekvienam juridiniui subjektui
description: Šioje temoje paaiškinama, kaip galite nustatyti modulio Elektroninės ataskaitos (ER) formato parametrus kiekvienam juridiniam subjektui.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 9c5884bba494d2dd44f9204667144402a88ddec8
ms.sourcegitcommit: d6196d83c7b9166ddb4fe43a91e6bd0ad9da2099
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/31/2019
ms.locfileid: "2694343"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a><span data-ttu-id="45d80-103">ER formato parametrų nustatymas kiekvienam juridiniui subjektui</span><span class="sxs-lookup"><span data-stu-id="45d80-103">Set up the parameters of an ER format per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="45d80-104">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="45d80-104">Prerequisites</span></span>

<span data-ttu-id="45d80-105">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, aprašytus temoje [Kaip sukonfigūruoti, kad būtų naudojami ER formatų parametrai, nurodyti kiekvienam juridiniam subjektui](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-105">To complete these steps, you must first complete the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span>

<span data-ttu-id="45d80-106">Norėdami atlikti šioje temoje pateiktus pavyzdžius, turite turėti prieigą prie „Microsoft Dynamics 365 Finance“ („Finance“) ir vieną iš tolesnių vaidmenų.</span><span class="sxs-lookup"><span data-stu-id="45d80-106">To complete the examples in this topic, you must have access to Microsoft Dynamics 365 Finance (Finance) for one of the following roles:</span></span>

- <span data-ttu-id="45d80-107">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="45d80-107">Electronic reporting developer</span></span>
- <span data-ttu-id="45d80-108">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="45d80-108">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="45d80-109">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="45d80-109">System administrator</span></span>

## <a name="import-er-configurations"></a><span data-ttu-id="45d80-110">Importuokite ER konfigūracijas</span><span class="sxs-lookup"><span data-stu-id="45d80-110">Import ER configurations</span></span>

1.  <span data-ttu-id="45d80-111">Prisijunkite prie savo aplinkos.</span><span class="sxs-lookup"><span data-stu-id="45d80-111">Sign in to your environment.</span></span>
2.  <span data-ttu-id="45d80-112">Numatytoje ataskaitų srityje pasirinkite **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="45d80-112">On the default dashboard, select **Electronic reporting**.</span></span>
3.  <span data-ttu-id="45d80-113">Pasirinkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="45d80-113">Select **Reporting configurations**.</span></span>
4.  <span data-ttu-id="45d80-114">Į dabartinį „Finance“ egzempliorių importuokite konfigūracijas, kurias eksportavote iš „Regulatory Configuration Service“ (RCS) atlikdami veiksmus, aprašytus temoje [Kaip sukonfigūruoti, kad būtų naudojami ER formatų parametrai, nurodyti kiekvienam juridiniam subjektui](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-114">Import, into the current instance of Finance, the configurations that you exported from Regulatory Configuration Services (RCS) while you were completing the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span> <span data-ttu-id="45d80-115">Šiuos veiksmus atlikite su kiekviena modulio Elektroninės ataskaitos (ER) konfigūracija šia tvarka: duomenų modelis, modelio susiejimas ir formatai.</span><span class="sxs-lookup"><span data-stu-id="45d80-115">Follow these steps for each Electronic reporting (ER) configuration, in the following order: data model, model mapping, and formats.</span></span>

    1. <span data-ttu-id="45d80-116">Pasirinkite **Keistis \> Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="45d80-116">Select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="45d80-117">Paspaudę **Naršyti** pasirinkite reikiamos ER konfigūracijos failą XML formatu.</span><span class="sxs-lookup"><span data-stu-id="45d80-117">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="45d80-118">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="45d80-118">Select **OK**.</span></span>
    
    <span data-ttu-id="45d80-119">Toliau pateiktoje iliustracijoje pateikiamos konfigūracijos, kurias reikia turėti atlikus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="45d80-119">The following illustration shows the configurations that you must have when you've finished.</span></span>

    ![ER konfigūracijų puslapis](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a><span data-ttu-id="45d80-121">DEMF įmonės parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="45d80-121">Set up parameters for the DEMF company</span></span>

<span data-ttu-id="45d80-122">Naudodami ER sistemą, ER formato parametrus galite nustatyti konkrečiai programai.</span><span class="sxs-lookup"><span data-stu-id="45d80-122">You can use the ER framework to set up application-specific parameters for an ER format.</span></span>

1.  <span data-ttu-id="45d80-123">Pasirinkite juridinį subjektą **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="45d80-123">Select the **DEMF** legal entity.</span></span>
2.  <span data-ttu-id="45d80-124">Konfigūracijų medyje pasirinkite formatą **Mokymo, kaip peržvelgti LE duomenis, formatas**.</span><span class="sxs-lookup"><span data-stu-id="45d80-124">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
3.  <span data-ttu-id="45d80-125">Veiksmų srities skirtuko **Konfigūracijos** grupėje **Konkrečių programų parametrai** pasirinkite **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="45d80-125">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>

    ![ER konkrečių programų parametrų puslapis](./media/GER-AppSpecParms-LookupForm.PNG)
    
    <span data-ttu-id="45d80-127">Puslapyje **Konkrečių programų parametrai** galite konfigūruoti formato **Mokymo, kaip peržvelgti LE duomenis, formatas** duomenų šaltinio **Išrinkiklis** taisykles.</span><span class="sxs-lookup"><span data-stu-id="45d80-127">On the **Application specific parameters** page, you can configure the rules for the **Selector** data source of the **Format to learn how to lookup LE data** format.</span></span>
    
    <span data-ttu-id="45d80-128">Jei baziniame ER formate bus keli tipo **Peržvalga** duomenų šaltiniai, pradėti konfigūruoti norimo duomenų šaltinio taisyklių rinkinį galėsite tik norimą duomenų šaltinį pasirinkę „FastTab“ elemente **Peržvalgos**.</span><span class="sxs-lookup"><span data-stu-id="45d80-128">If the base ER format will contain several data sources of the **Lookup** type, you must select the desired data source on the **Lookups** FastTab before you can start to configure the set of rules for the data source.</span></span>
    
    <span data-ttu-id="45d80-129">Kiekviename duomenų šaltinyje galite konfigūruoti atskiras kiekvienos pasirinkto ER formato versijos taisykles.</span><span class="sxs-lookup"><span data-stu-id="45d80-129">For each data source, you can configure separate rules for each version of the selected ER format.</span></span>
    
    <span data-ttu-id="45d80-130">Visas taisyklių rinkinys, skirtas visiems peržvalgos duomenų šaltiniams, kurie yra pasiekiami pasirinktoje bazinio ER formato versijoje, sudaro ER formato konkrečių programų parametrus.</span><span class="sxs-lookup"><span data-stu-id="45d80-130">The whole set of rules for all lookup data sources that are available in the selected version of the base ER format makes up the application-specific parameters for the ER format.</span></span>

4.  <span data-ttu-id="45d80-131">Pasirinkite ER formato versiją **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="45d80-131">Select version **1.1.1** of the ER format.</span></span>
5.  <span data-ttu-id="45d80-132">„FastTab“ elemente **Sąlygos** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="45d80-132">On the **Conditions** FastTab, select **Add**.</span></span>
6.  <span data-ttu-id="45d80-133">Naujo įrašo lauke **Kodas** pasirinkite išplečiamąją rodyklę, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="45d80-133">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="45d80-134">Peržvalgoje pateikiamas pasirenkamų mokesčių kodų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="45d80-134">The lookup presents the list of tax codes for selection.</span></span> <span data-ttu-id="45d80-135">Šį sąrašą pateikia duomenų šaltinis **Model.Data.Tax**, sukonfigūruotas baziniame ER formate.</span><span class="sxs-lookup"><span data-stu-id="45d80-135">This list is returned by the **Model.Data.Tax** data source that has been configured in the base ER format.</span></span> <span data-ttu-id="45d80-136">Kadangi šiame duomenų šaltinyje yra laukas **Pavadinimas**, peržvalgoje rodomas kiekvieno mokesčio kodo pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="45d80-136">Because this data source contains the **Name** field, the name of each tax code appears in the lookup.</span></span>

    ![ER konkrečių programų parametrų puslapis](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  <span data-ttu-id="45d80-138">Pasirinkite mokesčio kodą **VAT19**.</span><span class="sxs-lookup"><span data-stu-id="45d80-138">Select the **VAT19** tax code.</span></span>
8.  <span data-ttu-id="45d80-139">Naujo įrašo lauke **Peržvalgos rezultatas** pasirinkite išplečiamąją rodyklę, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="45d80-139">In the **Lookup result** field of the new record, select the drop-down arrow to open the lookup.</span></span> <span data-ttu-id="45d80-140">Peržvalgoje pateikiamas pasirenkamų formatų išvardijimo TaxationLevel reikšmių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="45d80-140">The lookup presents the list of values for the TaxationLevel format enumeration for selection.</span></span>

    <span data-ttu-id="45d80-141">Atkreipkite dėmesį, kad, jei kaip pageidajama vartotojo, kuriuo esate prisijungę, kalba pasirinkta vokiečių k., peržvalgos reikšmių žymos bus vokiečių k. (jei jos išverstos baziniame ER formate).</span><span class="sxs-lookup"><span data-stu-id="45d80-141">Note that, if German is selected as the preferred language of the user that you're signed in as, the labels of the values in the lookup will be in German, provided that they have been translated in the base ER format.</span></span> <span data-ttu-id="45d80-142">Be to, jei peržvalgos duomenų šaltinio žyma išversta, ji skirtuke **Peržvalgos** bus rodoma vartotojo pageidaujama kalba.</span><span class="sxs-lookup"><span data-stu-id="45d80-142">Additionally, if the label of a lookup data source has been translated, that label will appear in the user's preferred language on the **Lookups** tab.</span></span>

    ![ER konkrečių programų parametrų puslapis](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  <span data-ttu-id="45d80-144">Pasirinkite reikšmę **Įprastas apmokestinimas**.</span><span class="sxs-lookup"><span data-stu-id="45d80-144">Select the **Regular taxation** value.</span></span>

    <span data-ttu-id="45d80-145">Įtraukdami šį įrašą, apibrėžiate tokią taisyklę: kai reikalaujamas peržvalgos duomenų šaltinis **Išrinkiklis** ir kaip argumentas perduodamas mokesčio kodas **VAT19**, kaip reikalaujamas apmokestinimo lygis bus pateiktas **Įprastas apmokestinimas**.</span><span class="sxs-lookup"><span data-stu-id="45d80-145">By adding this record, you define the following rule: Whenever the **Selector** lookup data source is requested, and the **VAT19** tax code is passed as an argument, **Regular taxation** will be returned as the requested taxation level.</span></span>

10. <span data-ttu-id="45d80-146">Pasirinkite **Įtraukti** ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="45d80-146">Select **Add**, and then follow these steps:</span></span>

    1. <span data-ttu-id="45d80-147">Lauke **Kodas** pasirinkite mokesčio kodą **InVAT19**.</span><span class="sxs-lookup"><span data-stu-id="45d80-147">In the **Code** field, select the **InVAT19** tax code.</span></span>
    2. <span data-ttu-id="45d80-148">Lauke **Peržvalgos rezultatas** pasirinkite reikšmę **Įprastas apmokestinimas**.</span><span class="sxs-lookup"><span data-stu-id="45d80-148">In the **Lookup result** field, select the **Regular taxation** value.</span></span>
    
11. <span data-ttu-id="45d80-149">Dar kartą pasirinkite **Įtraukti** ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="45d80-149">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="45d80-150">Lauke **Kodas** pasirinkite mokesčio kodą **VAT7**.</span><span class="sxs-lookup"><span data-stu-id="45d80-150">In the **Code** field, select the **VAT7** tax code.</span></span>
    2. <span data-ttu-id="45d80-151">Lauke **Peržvalgos rezultatas** pasirinkite reikšmę **Sumažintas apmokestinimas**.</span><span class="sxs-lookup"><span data-stu-id="45d80-151">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
12. <span data-ttu-id="45d80-152">Dar kartą pasirinkite **Įtraukti** ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="45d80-152">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="45d80-153">Lauke **Kodas** pasirinkite mokesčio kodą **InVAT7**.</span><span class="sxs-lookup"><span data-stu-id="45d80-153">In the **Code** field, select the **InVAT7** tax code.</span></span>
    2. <span data-ttu-id="45d80-154">Lauke **Peržvalgos rezultatas** pasirinkite reikšmę **Sumažintas apmokestinimas**.</span><span class="sxs-lookup"><span data-stu-id="45d80-154">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
13. <span data-ttu-id="45d80-155">Dar kartą pasirinkite **Įtraukti** ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="45d80-155">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="45d80-156">Lauke **Kodas** pasirinkite mokesčio kodą **THIRD**.</span><span class="sxs-lookup"><span data-stu-id="45d80-156">In the **Code** field, select the **THIRD** tax code.</span></span>
    2. <span data-ttu-id="45d80-157">Lauke **Peržvalgos rezultatas** pasirinkite reikšmę **Apmokestinimo nėra**.</span><span class="sxs-lookup"><span data-stu-id="45d80-157">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
14. <span data-ttu-id="45d80-158">Dar kartą pasirinkite **Įtraukti** ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="45d80-158">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="45d80-159">Lauke **Kodas** pasirinkite mokesčio kodą **InVAT0**.</span><span class="sxs-lookup"><span data-stu-id="45d80-159">In the **Code** field, select the **InVAT0** tax code.</span></span>
    2. <span data-ttu-id="45d80-160">Lauke **Peržvalgos rezultatas** pasirinkite reikšmę **Apmokestinimo nėra**.</span><span class="sxs-lookup"><span data-stu-id="45d80-160">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
15. <span data-ttu-id="45d80-161">Dar kartą pasirinkite **Įtraukti** ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="45d80-161">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="45d80-162">Lauke **Kodas** pasirinkite parinktį **\*Ne tuščia\***.</span><span class="sxs-lookup"><span data-stu-id="45d80-162">In the **Code** field, select the **\*Not blank\*** option.</span></span>
    2. <span data-ttu-id="45d80-163">Lauke **Peržvalgos rezultatas** pasirinkite reikšmę **Kita**.</span><span class="sxs-lookup"><span data-stu-id="45d80-163">In the **Lookup result** field, select the **Other** value.</span></span>
    
    <span data-ttu-id="45d80-164">Įtraukdami šį pastarąjį įrašą, apibrėžiate tokią taisyklę: kai mokesčio kodas, perduodamas kaip argumentas, netenkina nė vienos iš ankstesnių taisyklių, peržvalgos duomenų šaltinis kaip reikalaujamą apmokestinimo lygį pateiks **Kita**.</span><span class="sxs-lookup"><span data-stu-id="45d80-164">By adding this last record, you define the following rule: Whenever the tax code that is passed as an argument doesn't satisfy any of the previous rules, the lookup data source will return **Other** as the requested taxation level.</span></span>

    ![ER konkrečių programų parametrų puslapis](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. <span data-ttu-id="45d80-166">Lauke **Būsena** pasirinkite **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="45d80-166">In the **State** field, select **Completed**.</span></span>

    <span data-ttu-id="45d80-167">Paleidus ER formato versiją, kurios būsena yra **Baigta** arba **Bendrai naudojama**, šio taisyklių rinkinio būsena turi būti **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="45d80-167">When you run an ER format version that has a status of either **Completed** or **Shared**, this set of rules must be in the **Completed** state.</span></span> <span data-ttu-id="45d80-168">Kitu atveju, formatui bandant įkelti duomenis iš šio taisyklių rinkinio, tuo pačiu metu paleidus peržvalgos duomenų šaltinį **Išrinkiklis**, bazinio ER formato vykdymas bus pertrauktas.</span><span class="sxs-lookup"><span data-stu-id="45d80-168">Otherwise, execution of the base ER format will be interrupted when the format tries to load data from this set of rules while the **Selector** lookup data source is being run.</span></span>
    
    <span data-ttu-id="45d80-169">Paleidus ER formato versiją, kurios būsena yra **Juodraštis**, bazinis ER formatas gali pasiekti šį taisyklių rinkinį – nesvarbu, kokia jo būsena.</span><span class="sxs-lookup"><span data-stu-id="45d80-169">When you run an ER format version that has a status of **Draft**, the base ER format can access this set of rules, regardless of its state.</span></span>
    
17. <span data-ttu-id="45d80-170">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="45d80-170">Select **Save**.</span></span>
18. <span data-ttu-id="45d80-171">Puslapį **Konkrečių programų parametrai** uždarykite.</span><span class="sxs-lookup"><span data-stu-id="45d80-171">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-demf-company"></a><span data-ttu-id="45d80-172">ER formato vykdymas DEMF įmonėje</span><span class="sxs-lookup"><span data-stu-id="45d80-172">Run the ER format in the DEMF company</span></span>

1.  <span data-ttu-id="45d80-173">Konfigūracijų medyje pasirinkite formatą **Mokymo, kaip peržvelgti LE duomenis, formatas**.</span><span class="sxs-lookup"><span data-stu-id="45d80-173">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="45d80-174">Veiksmų srityje pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="45d80-174">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="45d80-175">Pasirodžiusiame dialogo lange pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="45d80-175">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="45d80-176">Atsisiųskite sugeneruotą išrašą ir jį išsaugokite vietiniame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="45d80-176">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="45d80-177">Atkreipkite dėmesį, kad sugeneruotame išraše mokesčio kodo **InVAT7** suvestinė perkelta į lygį **Sumažintas**, o mokesčių kodų **VAT19** ir **InVA19** suvestinės perkeltos į lygį **Įprastas**.</span><span class="sxs-lookup"><span data-stu-id="45d80-177">In the generated statement, notice that the summary of the **InVAT7** tax code has been put on the **Reduced** level, and the summaries of the **VAT19** and **InVA19** tax codes have been put on the **Regular** level.</span></span> <span data-ttu-id="45d80-178">Tokį veikimo būdą nustato nuo juridinio subjekto priklausomų taisyklių rinkinio konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="45d80-178">This behavior is determined by the configuration in the legal entity–dependent set of rules.</span></span>
    
5.  <span data-ttu-id="45d80-179">Nueikite į **Mokestis \> Netiesioginiai mokesčiai \> PVM \> PVM kodai**.</span><span class="sxs-lookup"><span data-stu-id="45d80-179">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>
6.  <span data-ttu-id="45d80-180">Pasirinkite mokesčio kodą **InVAT7**.</span><span class="sxs-lookup"><span data-stu-id="45d80-180">Select the **InVAT7** tax code.</span></span>
7.  <span data-ttu-id="45d80-181">Veiksmų srities skirtuko **PVM kodas** grupėje **Užklausos** pasirinkę **Registruotas PVM**, galite peržiūrėti informaciją apie mokesčio reikšmę ir taikomą kiekvieno mokesčio kodo tarifą.</span><span class="sxs-lookup"><span data-stu-id="45d80-181">On the Action Pane, on the **Sales tax code** tab, in the **Inquiries** group, select **Posted sales tax** to view information about the tax value and applied tax rate per tax code.</span></span>

    ![Registruoto PVM puslapis](./media/GER-AppSpecParms-Statement.PNG)

8.  <span data-ttu-id="45d80-183">Puslapį Registruotas PVM uždarykite.</span><span class="sxs-lookup"><span data-stu-id="45d80-183">Close the Posted sales tax page.</span></span>

## <a name="set-up-parameters-for-the-usmf-company"></a><span data-ttu-id="45d80-184">USMF įmonės parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="45d80-184">Set up parameters for the USMF company</span></span>

1.  <span data-ttu-id="45d80-185">Pasirinkite juridinį subjektą **USMF**.</span><span class="sxs-lookup"><span data-stu-id="45d80-185">Select the **USMF** legal entity.</span></span>
2.  <span data-ttu-id="45d80-186">Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="45d80-186">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="45d80-187">Konfigūracijų medyje išplėskite elementą **Parametrizuotų iškvietų mokymo modelis**, tada – elementą **Parametrizuotų iškvietų mokymo formatas** ir pasirinkite formatą **Mokymo, kaip peržvelgti LE duomenis, formatas**.</span><span class="sxs-lookup"><span data-stu-id="45d80-187">In the configurations tree, expand the **Model to learn parameterized calls** item, expand the **Format to learn parameterized calls** item, and select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="45d80-188">Veiksmų srities skirtuko **Konfigūracijos** grupėje **Konkrečių programų parametrai** pasirinkite **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="45d80-188">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="45d80-189">Pasirinkite pasirinkto ER formato versiją **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="45d80-189">Select version **1.1.1** of the selected ER format.</span></span>
6.  <span data-ttu-id="45d80-190">„FastTab“ elemente **Sąlygos** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="45d80-190">On the **Conditions** FastTab, select **Add**.</span></span>
7.  <span data-ttu-id="45d80-191">Naujo įrašo lauke **Kodas** pasirinkite išplečiamąją rodyklę, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="45d80-191">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="45d80-192">Dabar peržvalgoje pateikiamas pasirenkamų **USMF** įmonės mokesčių kodų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="45d80-192">The lookup now presents the list of tax codes for the **USMF** company tax for selection.</span></span>

    ![ER konkrečių programų parametrų puslapis](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  <span data-ttu-id="45d80-194">Pasirinkite mokesčio kodą **EXEMPT**.</span><span class="sxs-lookup"><span data-stu-id="45d80-194">Select the **EXEMPT** tax code.</span></span>
9.  <span data-ttu-id="45d80-195">Naujo įrašo lauke **Peržvalgos rezultatas** pasirinkite reikšmę **Apmokestinimo nėra**.</span><span class="sxs-lookup"><span data-stu-id="45d80-195">In the **Lookup resul**t field of the new record, select the **No taxation** value.</span></span>
10. <span data-ttu-id="45d80-196">Dar kartą pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="45d80-196">Select **Add** again.</span></span>
11. <span data-ttu-id="45d80-197">Naujo įrašo lauke **Kodas** pasirinkite parinktį **\*Ne tuščia\***.</span><span class="sxs-lookup"><span data-stu-id="45d80-197">In the **Code** field of the new record, select the **\*Not blank\*** option.</span></span>
12. <span data-ttu-id="45d80-198">Naujo įrašo lauke **Peržvalgos rezultatas** pasirinkite reikšmę **Įprastas apmokestinimas**.</span><span class="sxs-lookup"><span data-stu-id="45d80-198">In the **Lookup result** field of the new record, select the **Regular taxation** value.</span></span>
13. <span data-ttu-id="45d80-199">Lauke **Būsena** pasirinkite **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="45d80-199">In the **State** field, select **Completed**.</span></span>
14. <span data-ttu-id="45d80-200">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="45d80-200">Select **Save**.</span></span>

    ![ER konkrečių programų parametrų puslapis](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. <span data-ttu-id="45d80-202">Puslapį **Konkrečių programų parametrai** uždarykite.</span><span class="sxs-lookup"><span data-stu-id="45d80-202">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-usmf-company"></a><span data-ttu-id="45d80-203">ER formato vykdymas USMF įmonėje</span><span class="sxs-lookup"><span data-stu-id="45d80-203">Run the ER format in the USMF company</span></span>

1.  <span data-ttu-id="45d80-204">Konfigūracijų medyje pasirinkite formatą **Mokymo, kaip peržvelgti LE duomenis, formatas**.</span><span class="sxs-lookup"><span data-stu-id="45d80-204">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="45d80-205">Veiksmų srityje pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="45d80-205">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="45d80-206">Pasirodžiusiame dialogo lange pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="45d80-206">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="45d80-207">Atsisiųskite sugeneruotą išrašą ir jį išsaugokite vietiniame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="45d80-207">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="45d80-208">Atkreipkite dėmesį, kad sugeneruotame išraše tą patį ER formatą dar kartą panaudojote kitam juridiniam subjektui, tačiau ER formato nepakoregavę.</span><span class="sxs-lookup"><span data-stu-id="45d80-208">In the generated statement, notice that you've now reused the same ER format for a different legal entity, but without making any adjustments to the ER format.</span></span>

## <a name="reuse-legal-entitydependent-parameters"></a><span data-ttu-id="45d80-209">Pakartotinis nuo juridinio subjekto priklausomų parametrų naudojimas</span><span class="sxs-lookup"><span data-stu-id="45d80-209">Reuse legal entity–dependent parameters</span></span>

### <a name="export-parameters"></a><span data-ttu-id="45d80-210">Eksportavimo parametrai</span><span class="sxs-lookup"><span data-stu-id="45d80-210">Export parameters</span></span>

1.  <span data-ttu-id="45d80-211">Eikite į **Organizacijos administravimas \> Darbo sritys \> Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="45d80-211">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2.  <span data-ttu-id="45d80-212">Pasirinkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="45d80-212">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="45d80-213">Konfigūracijų medyje pasirinkite formatą **Mokymo, kaip peržvelgti LE duomenis, formatas**.</span><span class="sxs-lookup"><span data-stu-id="45d80-213">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="45d80-214">Veiksmų srities skirtuko **Konfigūracijos** grupėje **Konkrečių programų parametrai** pasirinkite **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="45d80-214">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="45d80-215">Pasirinkite ER formato versiją **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="45d80-215">Select version **1.1.1** of the ER format.</span></span>
6.  <span data-ttu-id="45d80-216">Veiksmų srityje pasirinkite **Eksportuoti**.</span><span class="sxs-lookup"><span data-stu-id="45d80-216">On the Action Pane, select **Export**.</span></span>
7.  <span data-ttu-id="45d80-217">Atsisiųskite sugeneruotą failą ir jį išsaugokite vietiniame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="45d80-217">Download the file that is generated and store it locally.</span></span>

    <span data-ttu-id="45d80-218">Sukonfigūruotas konkrečių programų parametrų rinkinys dabar eksportuotas kaip XML failas.</span><span class="sxs-lookup"><span data-stu-id="45d80-218">The configured set of application-specific parameters has now been exported as an XML file.</span></span>

### <a name="import-parameters"></a><span data-ttu-id="45d80-219">Parametrų importavimas</span><span class="sxs-lookup"><span data-stu-id="45d80-219">Import parameters</span></span>

1.  <span data-ttu-id="45d80-220">Pasirinkite ER formato versiją **1.1.2**.</span><span class="sxs-lookup"><span data-stu-id="45d80-220">Select version **1.1.2** of the ER format.</span></span>
2.  <span data-ttu-id="45d80-221">Veiksmų srityje pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="45d80-221">On the Action Pane, select **Import**.</span></span>
3.  <span data-ttu-id="45d80-222">Pasirinkite **Taip**, kad patvirtintumėte, jog norite perrašyti esamus šios formato versijos konkrečių programų parametrus.</span><span class="sxs-lookup"><span data-stu-id="45d80-222">Select **Yes** to confirm that you want to override the existing application-specific parameters for this format version.</span></span>
4.  <span data-ttu-id="45d80-223">Pasirinkę **Naršyti** raskite failą, kuriame yra eksportuoti versijos **1.1.1** konkrečių programų parametrai.</span><span class="sxs-lookup"><span data-stu-id="45d80-223">Select **Browse** to find the file that contains the exported application-specific parameters for version **1.1.1**.</span></span>
5.  <span data-ttu-id="45d80-224">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="45d80-224">Select **OK**.</span></span>

    <span data-ttu-id="45d80-225">ER formato **1.1.2** versijoje dabar yra tie patys konkrečių programų parametrai, kuriuos iš pradžių sukonfigūravote **1.1.1** versijoje.</span><span class="sxs-lookup"><span data-stu-id="45d80-225">Version **1.1.2** of the ER format now has the same application-specific parameters that you originally configured for version **1.1.1**.</span></span>
    
    <span data-ttu-id="45d80-226">Atkreipkite dėmesį, kad ER formato konkrečių programų parametrai priklauso nuo juridinio subjekto.</span><span class="sxs-lookup"><span data-stu-id="45d80-226">Note that the application-specific parameters of an ER format are legal entity–dependent.</span></span> <span data-ttu-id="45d80-227">Norėdami vienam juridiniam subjektui sukonfigūruotus konkrečių programų parametrus pakartotinai naudoti kitam juridiniam subjektui, turite juos eksportuoti būdami prisijungę prie pirmojo juridinio subjekto ir importuoti prisijungę prie kito juridinio subjekto.</span><span class="sxs-lookup"><span data-stu-id="45d80-227">To reuse the application-specific parameters that were configured for one legal entity in a different legal entity, you must export them while you're signed in to the first legal entity and then import them after you sign in to the other legal entity.</span></span>

    <span data-ttu-id="45d80-228">Šį metodą taip pat galite naudoti norėdami su ER formatu susijusius konkrečių programų parametrus, kurie iš pradžių buvo sukonfigūruoti viename „Finance“ egzemplioriuje, perkelti į kitą „Finance“ egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="45d80-228">You can also use this approach to transfer an ER format related application-specific parameters that were originally configured in one instance of Finance to another instance of Finance.</span></span>

    <span data-ttu-id="45d80-229">Turėkite omenyje, kad, jei konkrečių programų parametrus sukonfigūruosite vienai ER formato versijai ir į dabartinį „Finance“ egzempliorių importuosite naujesnę to paties formato versiją, esami konkrečių programų parametrai importuoti versijai nebus taikomi.</span><span class="sxs-lookup"><span data-stu-id="45d80-229">Be aware that if you configure application-specific parameters for one version of an ER format and import a higher version of the same format into the current Finance instance, the existing application-specific parameters won't be applied for the imported version.</span></span>
    
    <span data-ttu-id="45d80-230">Taip pat žinokite, kad, kai pasirenkate importuotiną failą, jo konkrečių programų parametrų struktūra palyginama su atitinkamo tipo **Peržvalga** duomenų šaltinio, esančio pasirinktame importuoti ER formate, struktūra.</span><span class="sxs-lookup"><span data-stu-id="45d80-230">Also be aware that, when you select a file for import, the structure of the application-specific parameters in that file is compared with the structure of the corresponding data source of the **Lookup** type in the ER format that is selected for import.</span></span> <span data-ttu-id="45d80-231">Importavimas atliekamas, kai kiekvieno konkrečios programos parametro struktūra sutampa su atitinkamo duomenų šaltinio, esančio importuoti pasirinktame ER formate, struktūra.</span><span class="sxs-lookup"><span data-stu-id="45d80-231">The import is done when the structure of each application-specific parameter matches the structure of the corresponding data source in the ER format that is selected for import.</span></span> <span data-ttu-id="45d80-232">Jei struktūros nesutampa, gaunate įspėjamąjį pranešimą, kuriame nurodoma, kad importuoti negalima.</span><span class="sxs-lookup"><span data-stu-id="45d80-232">If the structures don't match, you receive a warning message that states that the import can't be done.</span></span> <span data-ttu-id="45d80-233">Jei importavimą atliksite priverstinai, esami pasirinkto ER formato konkrečių programų parametrai bus išvalyti ir juos turėsite nustatyti nuo pradžių.</span><span class="sxs-lookup"><span data-stu-id="45d80-233">If you force the import to be done, the existing application-specific parameters for the selected ER format will be cleaned up, and you must set them up from the beginning.</span></span>

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a><span data-ttu-id="45d80-234">Ryšys tarp konkrečių programų parametrų ir ER formato</span><span class="sxs-lookup"><span data-stu-id="45d80-234">Relationship between application-specific parameters and an ER format</span></span>

<span data-ttu-id="45d80-235">Ryšį tarp ER formato ir jo konkrečių programų parametrų nustato ER formato nuo egzempliorius nepriklausomas unikalus identifikavimo kodas.</span><span class="sxs-lookup"><span data-stu-id="45d80-235">The relationship between an ER format and its application-specific parameters is established by the ER format's instance-independent unique identification code.</span></span> <span data-ttu-id="45d80-236">Todėl, ER formatą pašalinus iš „Finance“, sukonfigūruoti to ER formato konkrečių programų parametrai išsaugomi dabartiniame „Finance“ egzemplioriuje.</span><span class="sxs-lookup"><span data-stu-id="45d80-236">Therefore, when you remove an ER format from Finance, the application-specific parameters that are configured for the ER format are kept in the current instance of Finance.</span></span> <span data-ttu-id="45d80-237">Juos galima pasiekti, kai bazinis ER formatas vėl importuojamas į šį „Finance“ egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="45d80-237">They can be accessed whenever the base ER format is reimported into this instance of Finance.</span></span>

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a><span data-ttu-id="45d80-238">Prieiga prie konkrečių programų parametrų naudojant ER sistemą</span><span class="sxs-lookup"><span data-stu-id="45d80-238">Access application-specific parameters by using the ER framework</span></span>

<span data-ttu-id="45d80-239">Ankstesniame pavyzdyje ER formato konkrečių programų parametrus pasiekėte naudodami ER sistemą.</span><span class="sxs-lookup"><span data-stu-id="45d80-239">In the preceding example, you have accessed application-specific parameters of an ER format by using the ER framework.</span></span> <span data-ttu-id="45d80-240">Naudojant šį metodą, negalima apriboti prieigos prie ER formato konkrečių programų parametrų.</span><span class="sxs-lookup"><span data-stu-id="45d80-240">This approach doesn't let you restrict access to the application-specific parameters of a specific ER format.</span></span> <span data-ttu-id="45d80-241">Jei turite taikyti tokius apribojimus, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="45d80-241">If you must apply such restrictions, follow these steps.</span></span> 

1.  <span data-ttu-id="45d80-242">Dar kartą panaudokite meniu elementą **ERSolutionAppSpecificParametersDesigner** arba įdiekite savo meniu elementą **ERSolutionAppSpecificParametersDesigner**.</span><span class="sxs-lookup"><span data-stu-id="45d80-242">Either reuse an existing **ERSolutionAppSpecificParametersDesigner** menu item, or implement your own **ERSolutionAppSpecificParametersDesigner** menu item.</span></span>

    ![„Visual Studio“ puslapis](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  <span data-ttu-id="45d80-244">Atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="45d80-244">Follow one of these steps:</span></span>

    1.  <span data-ttu-id="45d80-245">Sukurkite naują meniu elemento mygtuką ir jį susiekite su atitinkamu lentelės **ERSolutionTable** įrašu, jo ypatybę **Duomenų šaltinis** nustatydami kaip **ERSolutionTable**.</span><span class="sxs-lookup"><span data-stu-id="45d80-245">Create a new menu item button, and link it to the corresponding record from the **ERSolutionTable** table by setting its **Data Source** property to **ERSolutionTable**.</span></span>
    
        ![„Visual Studio“ puslapis](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  <span data-ttu-id="45d80-247">Sukurkite paprastą mygtuką ir perrašykite jo metodą **Spustelėta**, kaip parodyta tolesniame pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="45d80-247">Create a simple button, and override the **Clicked** method as shown in the following example.</span></span>
    
        <span data-ttu-id="45d80-248">Naudodami šį metodą, galite nurodyti unikalų sprendimo ID (apibrėžtą reikšme **GUID**), kad būtų leidžiama pasiekti tik konkretaus ER formato ir iš jo išvestų kopijų konkrečių programų parametrus.</span><span class="sxs-lookup"><span data-stu-id="45d80-248">By using this approach, you can specify a unique solution ID (defined via the **GUID** value) to allow access to the application-specific parameters of only a specific ER format and descendant copies that have been derived from it.</span></span>
        
        ```
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a><span data-ttu-id="45d80-249">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="45d80-249">Additional resources</span></span>

[<span data-ttu-id="45d80-250">Elektroninių ataskaitų formulių kūrimo įrankis</span><span class="sxs-lookup"><span data-stu-id="45d80-250">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="45d80-251">Kaip sukonfigūruoti, kad būtų naudojami ER formatų parametrai, nurodyti kiekvienam juridiniam subjektui</span><span class="sxs-lookup"><span data-stu-id="45d80-251">Configure ER formats to use parameters that are specified per legal entity</span></span>](er-app-specific-parameters-configure-format.md)
