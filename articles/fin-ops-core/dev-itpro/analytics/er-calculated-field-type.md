---
title: Apskaičiuoto lauko tipo ER duomenų šaltinių parametrizuotų kvietimų palaikymas
description: Šioje temoje pateikiama informacija apie tai, kaip naudoti ER duomenų šaltinių apskaičiuoto lauko tipą.
author: NickSelin
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c68f0a0e2481c69add8c50a1581466ad0b1483c0
ms.sourcegitcommit: 5472005274f2f94fba82dda90de128f39d8b8390
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759916"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="48697-103">Apskaičiuoto lauko tipo ER duomenų šaltinių parametrizuotų kvietimų palaikymas</span><span class="sxs-lookup"><span data-stu-id="48697-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48697-104">Šioje temoje paaiškinama, kaip galima kurti elektroninių ataskaitų (ER) duomenų šaltinį naudojant **apskaičiuoto lauko** tipą.</span><span class="sxs-lookup"><span data-stu-id="48697-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="48697-105">Šiame duomenų šaltinyje gali būti naudojama ER išraiška, kurią vykdymo metu galima kontroliuoti nurodant parametro argumentų reikšmes, kurios sukonfigūruotos šio duomenų šaltinio kvietimui.</span><span class="sxs-lookup"><span data-stu-id="48697-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="48697-106">Konfigūruodami tokio duomenų šaltinio parametrizuotus kvietimus, galite naudoti vieną duomenų šaltinį daugeliui susiejimų, o tai sumažina bendrą duomenų šaltinių, kuriuos reikia sukonfigūruoti ER modelio susiejimams arba ER formatams, skaičių.</span><span class="sxs-lookup"><span data-stu-id="48697-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="48697-107">Be to, taip supaprastinamas sukonfigūruotas komponentas, o tai sumažina priežiūros išlaidas ir naudojimo išlaidas kitiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="48697-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="48697-108">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="48697-108">Prerequisites</span></span>
<span data-ttu-id="48697-109">Norint įvykdyti šios temos pavyzdžių užduotis, reikia toliau nurodytų prieigų.</span><span class="sxs-lookup"><span data-stu-id="48697-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="48697-110">Prieiga prie vieno iš šių vaidmenų:</span><span class="sxs-lookup"><span data-stu-id="48697-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="48697-111">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="48697-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="48697-112">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="48697-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="48697-113">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="48697-113">System administrator</span></span>

- <span data-ttu-id="48697-114">Prieiga prie „Regulatory Configuration Services“, kuris buvo suteiktos tam pačiam nuomotojui, kaip ir „Finance and Operations“ vienai iš toliau paminėtų vaidmenų:</span><span class="sxs-lookup"><span data-stu-id="48697-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="48697-115">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="48697-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="48697-116">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="48697-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="48697-117">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="48697-117">System administrator</span></span>

<span data-ttu-id="48697-118">Taip pat turite atsiųsti ir vietoje saugoti toliau nurodytus failus.</span><span class="sxs-lookup"><span data-stu-id="48697-118">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="48697-119">**Turinys**</span><span class="sxs-lookup"><span data-stu-id="48697-119">**Content**</span></span>                           | <span data-ttu-id="48697-120">**Failo vardas**</span><span class="sxs-lookup"><span data-stu-id="48697-120">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="48697-121">ER duomenų modelio konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="48697-121">Sample ER data model configuration</span></span>    | [<span data-ttu-id="48697-122">Parametrizuotų kvietimų mokymo modelis.versija.1.xml</span><span class="sxs-lookup"><span data-stu-id="48697-122">Model to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| <span data-ttu-id="48697-123">ER metaduomenų konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="48697-123">Sample ER metadata configuration</span></span>      | [<span data-ttu-id="48697-124">Parametrizuotų kvietimų mokymo metaduomenys.versija.1.xml</span><span class="sxs-lookup"><span data-stu-id="48697-124">Metadata to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| <span data-ttu-id="48697-125">ER modelio susiejimo konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="48697-125">Sample ER model mapping configuration</span></span> | [<span data-ttu-id="48697-126">Parametrizuotų kvietimų mokymo susiejimas.versija.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="48697-126">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="48697-127">ER formato konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="48697-127">Sample ER format configuration</span></span>        | [<span data-ttu-id="48697-128">Parametrizuotų kvietimų mokymo formatas.versija.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="48697-128">Format to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="48697-129">Prisijunkite prie savo RCS egzemplioriaus</span><span class="sxs-lookup"><span data-stu-id="48697-129">Sign in to your RCS instance</span></span>
<span data-ttu-id="48697-130">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc.“ konfigūraciją. Pirmiausia naudodami RCS turite atlikti tolesnius procedūros [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md) veiksmus.</span><span class="sxs-lookup"><span data-stu-id="48697-130">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="48697-131">Numatytoje ataskaitų srityje pasirinkite **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="48697-131">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="48697-132">Pasirinkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="48697-132">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="48697-133">Importuokite atsisiųstas konfigūracijas į RCS tokia tvarka: duomenų modelis, metaduomenys, modelio susiejimas, formatas.</span><span class="sxs-lookup"><span data-stu-id="48697-133">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="48697-134">Atlikite šiuos veiksmus su kiekviena ER konfigūracija:</span><span class="sxs-lookup"><span data-stu-id="48697-134">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="48697-135">Pasirinkite **Keitimas.**</span><span class="sxs-lookup"><span data-stu-id="48697-135">Select **Exchange.**</span></span>
    2. <span data-ttu-id="48697-136">Pasirinkite **Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="48697-136">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="48697-137">Pasirinkite **Naršyti**, o tada pasirinkite reikiamą ER konfigūraciją XML formatu.</span><span class="sxs-lookup"><span data-stu-id="48697-137">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="48697-138">Pasirinkite **Gerai.**</span><span class="sxs-lookup"><span data-stu-id="48697-138">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="48697-139">Pateikto ER sprendimo peržiūra</span><span class="sxs-lookup"><span data-stu-id="48697-139">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="48697-140">Modelio susiejimo peržiūra</span><span class="sxs-lookup"><span data-stu-id="48697-140">Review model mapping</span></span>

1. <span data-ttu-id="48697-141">Konfigūracijos medyje išplėskite elemento **Parametrizuotų kvietimų mokymo modelis** turinį.</span><span class="sxs-lookup"><span data-stu-id="48697-141">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="48697-142">Pasirinkite **Parametrizuotų kvietimų mokymo susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="48697-142">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="48697-143">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="48697-143">Select **Designer**.</span></span>
4. <span data-ttu-id="48697-144">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="48697-144">Select **Designer**.</span></span>  
   
    <span data-ttu-id="48697-145">Šis ER modelio susiejimas sukurtas toliau nurodytiems veiksmams:</span><span class="sxs-lookup"><span data-stu-id="48697-145">This ER model mapping is designed to do the following:</span></span>

    - <span data-ttu-id="48697-146">Pateikti mokesčių kodų (duomenų šaltinis **Mokestis**), įrašytų lentelėje **TaxTable**, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="48697-146">Fetch the list of tax codes (**Tax** data source) residing in the **TaxTable** table.</span></span>
    - <span data-ttu-id="48697-147">Pateikti mokesčių operacijų (duomenų šaltinis **Operacija**), įrašytų lentelėje **TaxTrans**, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="48697-147">Fetch the list of tax transactions (**Trans** data source) residing in the **TaxTrans** table:</span></span>
    
        - <span data-ttu-id="48697-148">Sugrupuoti pateiktų operacijų sąrašą (duomenų šaltinis **Gr**) pagal mokesčio kodą.</span><span class="sxs-lookup"><span data-stu-id="48697-148">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
        - <span data-ttu-id="48697-149">Apskaičiuoti sugrupuotas operacijas po verčių agregavimo pagal mokesčio kodą.</span><span class="sxs-lookup"><span data-stu-id="48697-149">Calculate for grouped transactions following aggregated values per tax code:</span></span>

            - <span data-ttu-id="48697-150">Mokesčio bazinių verčių suma.</span><span class="sxs-lookup"><span data-stu-id="48697-150">Sum of tax base values.</span></span>
            - <span data-ttu-id="48697-151">Mokesčio verčių suma.</span><span class="sxs-lookup"><span data-stu-id="48697-151">Sum of tax values.</span></span>
            - <span data-ttu-id="48697-152">Mažiausioji taikomo mokesčio tarifo vertė.</span><span class="sxs-lookup"><span data-stu-id="48697-152">Minimum value of applied tax rate.</span></span>

    <span data-ttu-id="48697-153">Modelio žemėlapio nustatymas šiame konfigūravime įgyvendina pagrindinius duomenų modelius bet kuriems ER formatams sukurtiems šiam modeliui ir įgyvendintiems „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="48697-153">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="48697-154">Todėl duomenų šaltinių **Mokestis** ir **Gr** turinys tampa prieinamas ER formatams, pvz., abstrakčių duomenų šaltiniams.</span><span class="sxs-lookup"><span data-stu-id="48697-154">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

    ![Modelio susiejimo konstruktoriaus puslapis, kuriame rodomi duomenų šaltiniai „Mokestis“ ir „Gr“](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="48697-156">Uždarykite puslapį **Modelio susiejimo dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="48697-156">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="48697-157">Uždarykite puslapį **Modelio susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="48697-157">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="48697-158">Formato peržiūra</span><span class="sxs-lookup"><span data-stu-id="48697-158">Review format</span></span>

1. <span data-ttu-id="48697-159">Konfigūracijos medyje išplėskite elemento **Parametrizuotų kvietimų mokymo modelis** turinį.</span><span class="sxs-lookup"><span data-stu-id="48697-159">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="48697-160">Pasirinkite **Parametrizuotų kvietimų mokymo formatas**.</span><span class="sxs-lookup"><span data-stu-id="48697-160">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="48697-161">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="48697-161">Select **Designer**.</span></span> <span data-ttu-id="48697-162">Šis ER formatas sukurtas toliau nurodytiems veiksmams:</span><span class="sxs-lookup"><span data-stu-id="48697-162">This ER format is designed to do the following:</span></span>

    - <span data-ttu-id="48697-163">Sugeneruoti mokesčių ataskaitą XML formatu.</span><span class="sxs-lookup"><span data-stu-id="48697-163">Generate a tax statement in XML format.</span></span>
    - <span data-ttu-id="48697-164">Mokesčių ataskaitoje pateiki šiuos apmokestinimo lygius: „reguliarus“, „sumažintas“ ir „nėra“.</span><span class="sxs-lookup"><span data-stu-id="48697-164">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
    - <span data-ttu-id="48697-165">Pateikti įvairią skirtingo išsamumo kiekvieno apmokestinimo lygio informaciją.</span><span class="sxs-lookup"><span data-stu-id="48697-165">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

    ![Formato dizaino įrankio puslapis](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="48697-167">Pasirinkite **Susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="48697-167">Select **Mapping**.</span></span>
5. <span data-ttu-id="48697-168">Išskleiskite elementus **Modelis**, **Duomenys** ir **Suvestinė**.</span><span class="sxs-lookup"><span data-stu-id="48697-168">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

    <span data-ttu-id="48697-169">Apskaičiuotame lauke **Model.Data.Summary.Level** yra išraiška, kuri grąžina apmokestinimo lygio kodą (**Reguliarus**, **Sumažintas**, **Nėra** arba **Kita**) kaip bet kurio mokesčio kodo tekstinę reikšmę, kurią galima gauti iš duomenų šaltinio **Model.Data.Summary** vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="48697-169">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

    ![Formato konstruktoriaus puslapis, kuriame pateikiama informacija apie duomenų modelį „Parametrizuotų kvietimų mokymo modelis“](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="48697-171">Išplėskite elementą **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="48697-171">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="48697-172">Išplėskite elementą **Model**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="48697-172">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
    <span data-ttu-id="48697-173">Duomenų šaltinis **Model**.**Data2.Summary2** yra sukonfigūruotas taip, kad duomenų šaltinio **Model.Data.Summary** operacijų informacija būtų grupuojama pagal apmokestinimo lygį (kurį grąžina apskaičiuotas laukas **Model.Data.Summary.Level**) ir būtų skaičiuojami agreguoti duomenys.</span><span class="sxs-lookup"><span data-stu-id="48697-173">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

    ![Formato konstruktoriaus puslapis, kuriame pateikiama duomenų šaltinio Model.Data2.Summary2 informacija](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="48697-175">Peržiūrėkite apskaičiuotus laukus **Model**.**Data2.Level1**, **Model**.**Data2.Level2** ir **Model**.**Data2.Level3.**</span><span class="sxs-lookup"><span data-stu-id="48697-175">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="48697-176">Šie apskaičiuoti laukai naudojami filtruoti įrašų sąrašui **Model**.**Data2.Summary2** ir pateikia tik įrašus, atitinkančius konkretų apmokestinimo lygį.</span><span class="sxs-lookup"><span data-stu-id="48697-176">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="48697-177">Uždarykite puslapį **Formato dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="48697-177">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="48697-178">Sukurkite išvestinį formatą</span><span class="sxs-lookup"><span data-stu-id="48697-178">Create a derived format</span></span>
<span data-ttu-id="48697-179">Pateiktą formatą galite patobulini į filtrą įtraukdami vieną apskaičiuotą lauką, kad filtravimas būtų atliekamas pagal reikiamą apmokestinimo lygį, o ne naudojant tris esamus laukus: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** ir **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="48697-179">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="48697-180">Reikiamą apmokestinimo lygį galima nurodyti vietoje, kurioje bus kviečiamas šis naujas apskaičiuotas laukas.</span><span class="sxs-lookup"><span data-stu-id="48697-180">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="48697-181">Konfigūracijos medyje išplėskite elemento **Parametrizuotų kvietimų mokymo modelis** turinį.</span><span class="sxs-lookup"><span data-stu-id="48697-181">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="48697-182">Pasirinkite **Parametrizuotų kvietimų mokymo formatas**.</span><span class="sxs-lookup"><span data-stu-id="48697-182">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="48697-183">Pasirinkite **Kurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="48697-183">Select **Create configuration**.</span></span>
4. <span data-ttu-id="48697-184">Pasirinkite **Kildinti iš pavadinimo: parametrizuotų kvietimų mokymo formatas, „Microsoft“**.</span><span class="sxs-lookup"><span data-stu-id="48697-184">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="48697-185">Lauke **Pavadinimas** įveskite **Parametrizuotų kvietimų mokymo formatas (pasirinktinis)**.</span><span class="sxs-lookup"><span data-stu-id="48697-185">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="48697-186">Pasirinkite **Kurti konfigūraciją.**</span><span class="sxs-lookup"><span data-stu-id="48697-186">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="48697-187">Konfigūruokite parametrizuotą apskaičiuotą lauką, kuriame pateikiamas įrašų sąrašas</span><span class="sxs-lookup"><span data-stu-id="48697-187">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="48697-188">Pradėkite naujai apskaičiuoto lauko pridėjimo veiksmus</span><span class="sxs-lookup"><span data-stu-id="48697-188">Start adding a new calculated field</span></span>

1. <span data-ttu-id="48697-189">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="48697-189">Select **Designer**.</span></span>
2. <span data-ttu-id="48697-190">Pasirinkite **Išplėsti / sutraukti**, kad išplėstumėte visus formato elementus.</span><span class="sxs-lookup"><span data-stu-id="48697-190">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="48697-191">Pasirinkite **Susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="48697-191">Select **Mapping**.</span></span>
4. <span data-ttu-id="48697-192">Išplėskite elementą **Modelis**.</span><span class="sxs-lookup"><span data-stu-id="48697-192">Expand the **Model** item.</span></span>
5. <span data-ttu-id="48697-193">Pasirinkite elementą **Modelis.Duomenys2**.</span><span class="sxs-lookup"><span data-stu-id="48697-193">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="48697-194">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="48697-194">Select **Add**.</span></span>
7. <span data-ttu-id="48697-195">Pasirinkite **Funkcijos\\Apskaičiuotas laukas**.</span><span class="sxs-lookup"><span data-stu-id="48697-195">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="48697-196">Lauke **Pavadinimas** įveskite **Lygiai**.</span><span class="sxs-lookup"><span data-stu-id="48697-196">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="48697-197">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="48697-197">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="48697-198">Nurodykite apskaičiuoto lauko pridėjimo parametrą</span><span class="sxs-lookup"><span data-stu-id="48697-198">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="48697-199">Pasirinkite **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="48697-199">Select **Parameters**.</span></span>
2. <span data-ttu-id="48697-200">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="48697-200">Select **New**.</span></span>
3. <span data-ttu-id="48697-201">Lauke **Pavadinimas** įveskite **Mokesčio lygis**.</span><span class="sxs-lookup"><span data-stu-id="48697-201">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="48697-202">Lauke **Tipas** pasirinkite **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="48697-202">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="48697-203">Nurodant parametro argumento tipą, galima naudoti tik primityviuosius duomenų tipus.</span><span class="sxs-lookup"><span data-stu-id="48697-203">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="48697-204">Todėl šiam tikslui negalima naudoti tipų **Įrašų sąrašas**, **Įrašas** ir **Išvardijimas**.</span><span class="sxs-lookup"><span data-stu-id="48697-204">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="48697-205">Didžiausias parametrų, kuriuos galima nurodyti vienam apskaičiuotam laukui, skaičius yra 8.</span><span class="sxs-lookup"><span data-stu-id="48697-205">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Duomenų šaltinių sąrašo parametras](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="48697-207">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="48697-207">Select **OK**.</span></span>

<span data-ttu-id="48697-208">Pridėdami šį parametrą, nurodote sąlygą, kuri turi būti taikoma šiam apskaičiuojamam laukui iškviesti.</span><span class="sxs-lookup"><span data-stu-id="48697-208">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="48697-209">Kai kviečiate šį apskaičiuotą lauką, turite nurodyti parametro **Mokesčio lygis** argumentą, kuris pateikiamas formatu **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="48697-209">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="48697-210">Įsitikinkite, kad parametrus nurodote tik tiems apskaičiuotiems laukams, kurie yra konteineryje (**Įrašų sąrašas**, **Įrašas** arba **Konteineris**).</span><span class="sxs-lookup"><span data-stu-id="48697-210">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="48697-211">Sukonfigūruotas parametras yra pasiekiamas šio apskaičiuoto lauko duomenų šaltinių sąraše.</span><span class="sxs-lookup"><span data-stu-id="48697-211">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="48697-212">Parametrą į sukonfigūruotą išraišką galite įtraukti pasirinkdami **Įtraukti duomenų šaltinį.**</span><span class="sxs-lookup"><span data-stu-id="48697-212">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Duomenų šaltinio laukai](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="48697-214">Nurodykite apskaičiuoto lauko įtraukimo išraišką</span><span class="sxs-lookup"><span data-stu-id="48697-214">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="48697-215">Laukė **Formulė** įveskite:</span><span class="sxs-lookup"><span data-stu-id="48697-215">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="48697-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="48697-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="48697-217">Iš duomenų šaltinių sąrašo pasirinkite parametrą **Mokesčio lygis**.</span><span class="sxs-lookup"><span data-stu-id="48697-217">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="48697-218">Pasirinkite **Įtraukti duomenų šaltinį**.</span><span class="sxs-lookup"><span data-stu-id="48697-218">Select **Add data source**.</span></span>
4. <span data-ttu-id="48697-219">Lauke **Formulė** užbaikite išraišką:</span><span class="sxs-lookup"><span data-stu-id="48697-219">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="48697-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Mokesčio lygis')**</span><span class="sxs-lookup"><span data-stu-id="48697-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="48697-221">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="48697-221">Select **Save**.</span></span>

    ![Duomenų šaltinio lauko informacija](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="48697-223">Uždarykite puslapį **Formulės konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="48697-223">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="48697-224">Užbaikite naujo apskaičiuoto lauko įtraukimą</span><span class="sxs-lookup"><span data-stu-id="48697-224">Finish adding a new calculated field</span></span>

- <span data-ttu-id="48697-225">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="48697-225">Select **OK**.</span></span>

<span data-ttu-id="48697-226">Puslapyje **Formato kūrimo įrankis** sukonfigūruotam parametrizuotam apskaičiuotam laukui **Lygiai** reikia argumento **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="48697-226">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Išplėstas apskaičiuoto lauko lygių sąrašas](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="48697-228">Naudokite sukonfigūruotą apskaičiuotą lauką formato elementams susieti</span><span class="sxs-lookup"><span data-stu-id="48697-228">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="48697-229">Pasirinkite **Model.Data2.Levels**, kad pasirinktumėte sukonfigūruotą apskaičiuotą lauką.</span><span class="sxs-lookup"><span data-stu-id="48697-229">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="48697-230">Pasirinkite formato elementą **Statement.Taxation.Regular**.</span><span class="sxs-lookup"><span data-stu-id="48697-230">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="48697-231">Pasirinkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="48697-231">Select **Bind**.</span></span>
4. <span data-ttu-id="48697-232">Pasirinkite **Taip**, kad patvirtintumėte naudojamo duomenų šaltinio **Level1** pakeitimą nauju duomenų šaltiniu **Lygiai** visuose pasirinkto formato elemento įdėtuosiuose formato elementuose.</span><span class="sxs-lookup"><span data-stu-id="48697-232">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="48697-233">Taikomas susiejimas sukurtas kaip parametrizuoto apskaičiuoto lauko kvietimas.</span><span class="sxs-lookup"><span data-stu-id="48697-233">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="48697-234">Esant numatytiesiems nustatymams, susieto formato elemento pavadinimas yra naudojamas kaip parametrizuoto apskaičiuoto lauko argumentas esant šioms sąlygoms:</span><span class="sxs-lookup"><span data-stu-id="48697-234">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="48697-235">Apskaičiuotas laukas sukonfigūruotas, kad naudotų vieną parametrą.</span><span class="sxs-lookup"><span data-stu-id="48697-235">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="48697-236">Šio parametro duomenų tipas nurodytas kaip **Eilutė.**</span><span class="sxs-lookup"><span data-stu-id="48697-236">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="48697-237">Kai susieto formato elemento pavadinimas yra tuščias, taikomame susiejime naudojamas šio elemento duomenų šaltinio pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="48697-237">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="48697-238">Pasirinkite formato elementą **Statement.Taxation.Reduced**.</span><span class="sxs-lookup"><span data-stu-id="48697-238">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="48697-239">Pasirinkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="48697-239">Select **Bind**.</span></span>
7. <span data-ttu-id="48697-240">Pasirinkite **Taip**, kad patvirtintumėte naudojamo duomenų šaltinio **Level2** pakeitimą nauju duomenų šaltiniu **Lygiai** visuose pasirinkto formato elemento įdėtuosiuose formato elementuose.</span><span class="sxs-lookup"><span data-stu-id="48697-240">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="48697-241">Pasirinkite formato elementą **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="48697-241">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="48697-242">Pasirinkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="48697-242">Select **Bind**.</span></span>
10. <span data-ttu-id="48697-243">Pasirinkite **Taip**, kad patvirtintumėte naudojamo duomenų šaltinio **Level3** pakeitimą nauju duomenų šaltiniu **Lygiai** visuose pasirinkto formato elemento įdėtuosiuose formato elementuose.</span><span class="sxs-lookup"><span data-stu-id="48697-243">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="48697-244">Kai nurodote XML elemento, atitinkančio apmokestinimo lygį, parametrizuoto apskaičiuoto lauko argumentą (pavyzdžiui, **Model.Data2.Levels("Reduced")** kaip tekstinę reikšmę), jums nebereikia to atlikti su įdėtaisiais XML atributais – susiejimuose bus automatiškai paveldėta pirminiame lygyje nurodyta argumento reikšmė (**Model.Data2.Levels.aggregated.Base**, ne **Model.Data2.Levels("Reduced").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="48697-244">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="48697-245">Negalimi pasikartojantys parametrizuoto apskaičiuoto lauko kvietimai.</span><span class="sxs-lookup"><span data-stu-id="48697-245">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="48697-246">Galite pasirinkti **Redaguoti formulę**ir pakeisti pasirinkto susiejimo parametrizuoto apskaičiuoto lauko numatytąjį argumentą.</span><span class="sxs-lookup"><span data-stu-id="48697-246">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="48697-247">Jei šio argumento nėra, vykdymo metu gali kilti klaidų – vartotojai informuojami apie tokią situaciją naudojamo formato patikrinimo metu.</span><span class="sxs-lookup"><span data-stu-id="48697-247">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Tikrinimo įspėjimo pranešimas](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="48697-249">Sukonfigūruokite parametrizuotą apskaičiuotą lauką, kuris pateikia įrašą</span><span class="sxs-lookup"><span data-stu-id="48697-249">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="48697-250">Kai parametrizuotas apskaičiuotas laukas pateikia įrašą, turite leisti atskirų šio įrašo laukų susiejimą su elementais.</span><span class="sxs-lookup"><span data-stu-id="48697-250">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="48697-251">Tokiais atvejais nebus pirminio susiejimo su argumento reikšme parametrizuoto apskaičiuoto lauko iškvietimui – šią reikšmę reikia nurodyti vieno įrašo lauko susiejime.</span><span class="sxs-lookup"><span data-stu-id="48697-251">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="48697-252">Pradėkite naujai apskaičiuoto lauko pridėjimo veiksmus</span><span class="sxs-lookup"><span data-stu-id="48697-252">Start adding a new calculated field</span></span>

1. <span data-ttu-id="48697-253">Pasirinkite elementą **Modelis.Duomenys2**.</span><span class="sxs-lookup"><span data-stu-id="48697-253">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="48697-254">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="48697-254">Select **Add**.</span></span>
3. <span data-ttu-id="48697-255">Pasirinkite **Funkcijos\\Apskaičiuotas laukas**.</span><span class="sxs-lookup"><span data-stu-id="48697-255">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="48697-256">Lauke **Pavadinimas** įveskite **LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="48697-256">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="48697-257">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="48697-257">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="48697-258">Nurodykite apskaičiuoto lauko pridėjimo parametrą</span><span class="sxs-lookup"><span data-stu-id="48697-258">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="48697-259">Pasirinkite **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="48697-259">Select **Parameters**.</span></span>
2. <span data-ttu-id="48697-260">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="48697-260">Select **New**.</span></span>
3. <span data-ttu-id="48697-261">Lauke **Pavadinimas** įveskite **Mokesčio lygis**.</span><span class="sxs-lookup"><span data-stu-id="48697-261">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="48697-262">Lauke **Tipas** pasirinkite **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="48697-262">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="48697-263">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="48697-263">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="48697-264">Nurodykite apskaičiuoto lauko įtraukimo išraišką</span><span class="sxs-lookup"><span data-stu-id="48697-264">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="48697-265">Lauke **Formulė** įveskite šią išraišką:</span><span class="sxs-lookup"><span data-stu-id="48697-265">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="48697-266">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="48697-266">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="48697-267">Pasirinkite parametrą **Apmokestinimo lygis**.</span><span class="sxs-lookup"><span data-stu-id="48697-267">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="48697-268">Pasirinkite **Įtraukti duomenų šaltinį**.</span><span class="sxs-lookup"><span data-stu-id="48697-268">Select **Add data source**.</span></span>
4. <span data-ttu-id="48697-269">Lake **Formulė** papildykite atliekant 1 veiksmą įvestą išraišką įvesdami **'Apmokestinimo lygis'))**, kad galutinė išraiška būtų tokia:</span><span class="sxs-lookup"><span data-stu-id="48697-269">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="48697-270">**FIRSTORNULL(\@.Levels('Apmokestinimo lygis'))**</span><span class="sxs-lookup"><span data-stu-id="48697-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="48697-271">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="48697-271">Select **Save**.</span></span>
6. <span data-ttu-id="48697-272">Uždarykite puslapį **Formulės konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="48697-272">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="48697-273">Užbaikite naujo apskaičiuoto lauko įtraukimą</span><span class="sxs-lookup"><span data-stu-id="48697-273">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="48697-274">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="48697-274">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="48697-275">Naudokite sukonfigūruotą apskaičiuotą lauką formato elementams susieti</span><span class="sxs-lookup"><span data-stu-id="48697-275">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="48697-276">Išplėskite **Model.Data2.LevelRecord**, kad pasirinktumėte sukonfigūruotą apskaičiuotą lauką.</span><span class="sxs-lookup"><span data-stu-id="48697-276">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="48697-277">Išplėskite sukonfigūruoto apskaičiuoto lauko konteinerį **Model.Data2.LevelRecord.aggregated**.</span><span class="sxs-lookup"><span data-stu-id="48697-277">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="48697-278">Pasirinkite lauką **Model.Data2.LevelRecord.aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="48697-278">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="48697-279">Pasirinkite formato elementą **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="48697-279">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="48697-280">Pasirinkite **Atsieti**.</span><span class="sxs-lookup"><span data-stu-id="48697-280">Select **Unbind**.</span></span>
6. <span data-ttu-id="48697-281">Pasirinkite formato elementą **Statement.Taxation.None.Base**.</span><span class="sxs-lookup"><span data-stu-id="48697-281">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="48697-282">Pasirinkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="48697-282">Select **Bind**.</span></span>
8. <span data-ttu-id="48697-283">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="48697-283">Select **Edit formula**.</span></span>
9. <span data-ttu-id="48697-284">Pakeiskite išraišką į **Model.Data2.LevelRecord("None").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="48697-284">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Atnaujinta išraiška](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="48697-286">Pašalinkite nenaudojamus apskaičiuotus laukus</span><span class="sxs-lookup"><span data-stu-id="48697-286">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="48697-287">Pasirinkite **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="48697-287">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="48697-288">Pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="48697-288">Select **Delete**.</span></span>
3. <span data-ttu-id="48697-289">Pasirinkite **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="48697-289">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="48697-290">Pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="48697-290">Select **Delete**.</span></span>
5. <span data-ttu-id="48697-291">Pasirinkite **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="48697-291">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="48697-292">Pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="48697-292">Select **Delete**.</span></span>
7. <span data-ttu-id="48697-293">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="48697-293">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="48697-294">Susiedami formatą jūs pakartotinai kelis kartus panaudojote tą patį apskaičiuotą lauką **Model.Data2.Levels**.</span><span class="sxs-lookup"><span data-stu-id="48697-294">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="48697-295">Daug paprasčiau naudoti ir tvarkyti vieną apskaičiuojamą lauką, o ne kelis panašius laukus.</span><span class="sxs-lookup"><span data-stu-id="48697-295">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="48697-296">Uždarykite puslapį **Formato dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="48697-296">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="48697-297">Užbaikite pakoreguotą išvestinio formato versiją</span><span class="sxs-lookup"><span data-stu-id="48697-297">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="48697-298">„FastTab“ elemente **Versijos** pasirinkite **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="48697-298">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="48697-299">Pasirinkite **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="48697-299">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="48697-300">Eksportuokite užbaigtą išvestinio formato versiją</span><span class="sxs-lookup"><span data-stu-id="48697-300">Export completed version of a derived format</span></span>

1. <span data-ttu-id="48697-301">Konfigūracijų medyje pasirinkite formatą **Parametrizuotų kvietimų mokymo formatas (pasirinktinis)**.</span><span class="sxs-lookup"><span data-stu-id="48697-301">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="48697-302">„FastTab“ elemente **Versijos** pasirinkite 1.1.1 užbaigtą versiją.</span><span class="sxs-lookup"><span data-stu-id="48697-302">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="48697-303">Pasirinkite **Keitimas**.</span><span class="sxs-lookup"><span data-stu-id="48697-303">Select **Exchange**.</span></span>
4. <span data-ttu-id="48697-304">Pasirinkite **Eksportuoti kaip XML failą**.</span><span class="sxs-lookup"><span data-stu-id="48697-304">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="48697-305">Atsisiųstą konfigūraciją išsaugokite vietoje XML formatu.</span><span class="sxs-lookup"><span data-stu-id="48697-305">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="48697-306">Patikrinkite ER formatus</span><span class="sxs-lookup"><span data-stu-id="48697-306">Test ER formats</span></span> 
<span data-ttu-id="48697-307">Galite paleisti pradinį ir patobulintą ER formatus, kad įsitikintumėte, jog sukonfigūruoti parametrizuoti apskaičiuoti laukai veikia tinkamai.</span><span class="sxs-lookup"><span data-stu-id="48697-307">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="48697-308">Importuokite ER konfigūracijas</span><span class="sxs-lookup"><span data-stu-id="48697-308">Import ER configurations</span></span>
<span data-ttu-id="48697-309">Peržiūrėtas konfigūracijas galite importuoti iš RCS naudodami **RCS** tipo ER saugyklą.</span><span class="sxs-lookup"><span data-stu-id="48697-309">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="48697-310">Jei jau atlikote temoje [Elektroninių ataskaitų (ER) konfigūracijų importavimas iš „Regulatory Configuration Services“ (RCS)](rcs-download-configurations.md) aprašytus veiksmus, naudodami sukonfigūruotą ER saugyklą į savo aplinką importuokite prieš tai šioje temoje aptartas konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="48697-310">If you already went through the steps in the topic, [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="48697-311">Priešingu atveju atlikite toliau nurodytus veiksmus:</span><span class="sxs-lookup"><span data-stu-id="48697-311">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="48697-312">Pasirinkite įmonę **DEMF** ir numatytoje ataskaitų srityje pasirinkite **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="48697-312">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="48697-313">Pasirinkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="48697-313">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="48697-314">Importuokite iš „Microsoft“ atsisiuntimo centro gautas konfigūracijas tokia tvarka: duomenų modelis, modelio susiejimas, formatas.</span><span class="sxs-lookup"><span data-stu-id="48697-314">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="48697-315">Atlikite šiuos veiksmus su kiekviena ER konfigūracija:</span><span class="sxs-lookup"><span data-stu-id="48697-315">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="48697-316">Pasirinkite **Keitimas.**</span><span class="sxs-lookup"><span data-stu-id="48697-316">Select **Exchange.**</span></span>
    2. <span data-ttu-id="48697-317">Pasirinkite **Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="48697-317">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="48697-318">Pasirinkite **Naršyti**, kad galėtumėte pasirinkti reikiamą ER konfigūraciją XML formatu.</span><span class="sxs-lookup"><span data-stu-id="48697-318">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="48697-319">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="48697-319">Select **OK**.</span></span>

4. <span data-ttu-id="48697-320">Importuokite eksportuotą iš RCS formato **Parametrizuotų kvietimų mokymo formatas (pasirinktinis)** 1.1.1 baigtą versiją:</span><span class="sxs-lookup"><span data-stu-id="48697-320">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="48697-321">Pasirinkite **Keitimas.**</span><span class="sxs-lookup"><span data-stu-id="48697-321">Select **Exchange.**</span></span>
    2. <span data-ttu-id="48697-322">Pasirinkite **Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="48697-322">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="48697-323">Pasirinkite **Naršyti**, kad pasirinktumėte vietoje saugomą XML formato failą **Parametrizuotų kvietimų mokymo formatas (pasirinktinis)**.</span><span class="sxs-lookup"><span data-stu-id="48697-323">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="48697-324">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="48697-324">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="48697-325">Vykdykite ER formatus</span><span class="sxs-lookup"><span data-stu-id="48697-325">Run ER formats</span></span>

1. <span data-ttu-id="48697-326">Konfigūracijos medyje išplėskite elemento **Parametrizuotų kvietimų mokymo modelis** turinį.</span><span class="sxs-lookup"><span data-stu-id="48697-326">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="48697-327">Pasirinkite **Parametrizuotų kvietimų mokymo formatas**.</span><span class="sxs-lookup"><span data-stu-id="48697-327">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="48697-328">Viršutinėje juostoje pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="48697-328">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="48697-329">Įrašykite vietoje sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="48697-329">Save the locally generated output.</span></span>
5. <span data-ttu-id="48697-330">Pasirinkite elementą **Parametrizuotų kvietimų mokymo formatas (pasirinktinis)**.</span><span class="sxs-lookup"><span data-stu-id="48697-330">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="48697-331">Viršutinėje juostoje pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="48697-331">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="48697-332">Vietoje įrašykite sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="48697-332">Save the generated output locally.</span></span> 
8. <span data-ttu-id="48697-333">Palyginkite sugeneruotų išvesčių turinį.</span><span class="sxs-lookup"><span data-stu-id="48697-333">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48697-334">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="48697-334">Additional resources</span></span>

- [<span data-ttu-id="48697-335">Elektroninių ataskaitų (ER) formulių kūrimo įrankis</span><span class="sxs-lookup"><span data-stu-id="48697-335">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="48697-336">ER sprendimų našumo didinimas įtraukiant parametrizuotų duomenų šaltinių APSKAIČIUOTAS LAUKAS</span><span class="sxs-lookup"><span data-stu-id="48697-336">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)

