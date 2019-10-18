---
title: Apskaičiuoto lauko tipo ER duomenų šaltinių parametrizuotų kvietimų palaikymas
description: Šioje temoje pateikiama informacija apie tai, kaip naudoti ER duomenų šaltinių apskaičiuoto lauko tipą.
author: NickSelin
manager: AnnBe
ms.date: 09/09/2019
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
ms.openlocfilehash: 86efa927fa97be0d54e965bf33b1a18519025c22
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248682"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="68658-103">Apskaičiuoto lauko tipo ER duomenų šaltinių parametrizuotų kvietimų palaikymas</span><span class="sxs-lookup"><span data-stu-id="68658-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68658-104">Šioje temoje paaiškinama, kaip galima kurti elektroninių ataskaitų (ER) duomenų šaltinį naudojant **apskaičiuoto lauko** tipą.</span><span class="sxs-lookup"><span data-stu-id="68658-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="68658-105">Šiame duomenų šaltinyje gali būti naudojama ER išraiška, kurią vykdymo metu galima kontroliuoti nurodant parametro argumentų reikšmes, kurios sukonfigūruotos šio duomenų šaltinio kvietimui.</span><span class="sxs-lookup"><span data-stu-id="68658-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="68658-106">Konfigūruodami tokio duomenų šaltinio parametrizuotus kvietimus, galite naudoti vieną duomenų šaltinį daugeliui susiejimų, o tai sumažina bendrą duomenų šaltinių, kuriuos reikia sukonfigūruoti ER modelio susiejimams arba ER formatams, skaičių.</span><span class="sxs-lookup"><span data-stu-id="68658-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="68658-107">Be to, taip supaprastinamas sukonfigūruotas komponentas, o tai sumažina priežiūros išlaidas ir naudojimo išlaidas kitiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="68658-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="68658-108">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="68658-108">Prerequisites</span></span>
<span data-ttu-id="68658-109">Norint įvykdyti šios temos pavyzdžių užduotis, reikia toliau nurodytų prieigų.</span><span class="sxs-lookup"><span data-stu-id="68658-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="68658-110">Prieiga prie vieno iš šių vaidmenų:</span><span class="sxs-lookup"><span data-stu-id="68658-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="68658-111">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="68658-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="68658-112">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="68658-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="68658-113">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="68658-113">System administrator</span></span>

- <span data-ttu-id="68658-114">Prieiga prie „Regulatory Configuration Services“ (RCS), kuris sukurtas tam pačiam kaip ir „Finance and Operations“ nuomotojui vienam iš toliau nurodytų vaidmenų:</span><span class="sxs-lookup"><span data-stu-id="68658-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="68658-115">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="68658-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="68658-116">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="68658-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="68658-117">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="68658-117">System administrator</span></span>

<span data-ttu-id="68658-118">Iš [„Microsoft“ atsisiuntimo centro](https://go.microsoft.com/fwlink/?linkid=874684) atsisiųskite suspaustą (suglaudintą) failą **Apskaičiuoto lauko tipo ER duomenų šaltinių parametrizuotų kvietimų palaikymas**.</span><span class="sxs-lookup"><span data-stu-id="68658-118">From the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684), download the zipped (compressed) file **Support parameterized calls of ER data sources of Calculated field type**.</span></span> <span data-ttu-id="68658-119">Jame yra nurodytos ER konfigūracijos, kurias reikia išskleisti ir saugoti vietoje.</span><span class="sxs-lookup"><span data-stu-id="68658-119">It contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="68658-120">**Turinys**</span><span class="sxs-lookup"><span data-stu-id="68658-120">**Content**</span></span>                           | <span data-ttu-id="68658-121">**Failo vardas**</span><span class="sxs-lookup"><span data-stu-id="68658-121">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="68658-122">ER duomenų modelio konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="68658-122">Sample ER data model configuration</span></span>    | <span data-ttu-id="68658-123">Parametrizuotų kvietimų mokymo modelis.versija.1.xml</span><span class="sxs-lookup"><span data-stu-id="68658-123">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="68658-124">ER metaduomenų konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="68658-124">Sample ER metadata configuration</span></span>      | <span data-ttu-id="68658-125">Parametrizuotų kvietimų mokymo metaduomenys.versija.1.xml</span><span class="sxs-lookup"><span data-stu-id="68658-125">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="68658-126">ER modelio susiejimo konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="68658-126">Sample ER model mapping configuration</span></span> | <span data-ttu-id="68658-127">Parametrizuotų kvietimų mokymo susiejimas.versija.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="68658-127">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="68658-128">ER formato konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="68658-128">Sample ER format configuration</span></span>        | <span data-ttu-id="68658-129">Parametrizuotų kvietimų mokymo formatas.versija.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="68658-129">Format to learn parameterized calls.version.1.1.xml</span></span>  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="68658-130">Prisijunkite prie savo RCS egzemplioriaus</span><span class="sxs-lookup"><span data-stu-id="68658-130">Sign in to your RCS instance</span></span>
<span data-ttu-id="68658-131">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc.“ konfigūraciją. Pirmiausia turite atlikti procedūros [Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu](tasks/er-configuration-provider-mark-it-active-2016-11.md) veiksmus:</span><span class="sxs-lookup"><span data-stu-id="68658-131">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="68658-132">Numatytoje ataskaitų srityje pasirinkite **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="68658-132">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="68658-133">Pasirinkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="68658-133">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="68658-134">Importuokite atsisiųstas konfigūracijas į RCS tokia tvarka: duomenų modelis, metaduomenys, modelio susiejimas, formatas.</span><span class="sxs-lookup"><span data-stu-id="68658-134">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="68658-135">Atlikite šiuos veiksmus su kiekviena ER konfigūracija:</span><span class="sxs-lookup"><span data-stu-id="68658-135">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="68658-136">Pasirinkite **Keitimas.**</span><span class="sxs-lookup"><span data-stu-id="68658-136">Select **Exchange.**</span></span>
    2. <span data-ttu-id="68658-137">Pasirinkite **Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="68658-137">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="68658-138">Pasirinkite **Naršyti**, o tada pasirinkite reikiamą ER konfigūraciją XML formatu.</span><span class="sxs-lookup"><span data-stu-id="68658-138">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="68658-139">Pasirinkite **Gerai.**</span><span class="sxs-lookup"><span data-stu-id="68658-139">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="68658-140">Pateikto ER sprendimo peržiūra</span><span class="sxs-lookup"><span data-stu-id="68658-140">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="68658-141">Modelio susiejimo peržiūra</span><span class="sxs-lookup"><span data-stu-id="68658-141">Review model mapping</span></span>

1. <span data-ttu-id="68658-142">Konfigūracijos medyje išplėskite elemento **Parametrizuotų kvietimų mokymo modelis** turinį.</span><span class="sxs-lookup"><span data-stu-id="68658-142">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="68658-143">Pasirinkite **Parametrizuotų kvietimų mokymo susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="68658-143">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="68658-144">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="68658-144">Select **Designer**.</span></span>
4. <span data-ttu-id="68658-145">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="68658-145">Select **Designer**.</span></span>  
   
<span data-ttu-id="68658-146">Šis ER modelio susiejimas sukurtas toliau nurodytiems veiksmams:</span><span class="sxs-lookup"><span data-stu-id="68658-146">This ER model mapping is designed to do the following:</span></span>

- <span data-ttu-id="68658-147">Pateikti mokesčių kodų (duomenų šaltinis **Mokestis**), įrašytų lentelėje **TaxTable**, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="68658-147">Fetch the list of tax codes (**Tax** data source) residing in the   **TaxTable** table.</span></span>
- <span data-ttu-id="68658-148">Pateikti mokesčių operacijų (duomenų šaltinis **Operacija**), įrašytų lentelėje **TaxTrans**, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="68658-148">Fetch the list of tax transactions (**Trans** data source) residing in the   **TaxTrans** table:</span></span>
    
    - <span data-ttu-id="68658-149">Sugrupuoti pateiktų operacijų sąrašą (duomenų šaltinis **Gr**) pagal mokesčio kodą.</span><span class="sxs-lookup"><span data-stu-id="68658-149">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
    - <span data-ttu-id="68658-150">Apskaičiuoti sugrupuotas operacijas po verčių agregavimo pagal mokesčio kodą:</span><span class="sxs-lookup"><span data-stu-id="68658-150">Calculate for grouped transactions following aggregated values per   tax code:</span></span>

        - <span data-ttu-id="68658-151">Mokesčio bazinių verčių suma.</span><span class="sxs-lookup"><span data-stu-id="68658-151">Sum of tax base values.</span></span>
        - <span data-ttu-id="68658-152">Mokesčio verčių suma.</span><span class="sxs-lookup"><span data-stu-id="68658-152">Sum of tax values.</span></span>
        - <span data-ttu-id="68658-153">Mažiausioji taikomo mokesčio tarifo vertė.</span><span class="sxs-lookup"><span data-stu-id="68658-153">Minimum value of applied tax rate.</span></span>

<span data-ttu-id="68658-154">Modelio susiejimas šioje konfigūracijoje taikomas kaip bazinis duomenų modelis visiems šiam modeliui sukurtiems ir vykdomiems „Finance and Operations“ ER formatams.</span><span class="sxs-lookup"><span data-stu-id="68658-154">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="68658-155">Todėl duomenų šaltinių **Mokestis** ir **Gr** turinys tampa prieinamas ER formatams, pvz., abstrakčių duomenų šaltiniams.</span><span class="sxs-lookup"><span data-stu-id="68658-155">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

  ![Modelio susiejimo konstruktoriaus puslapis, kuriame rodomi duomenų šaltiniai „Mokestis“ ir „Gr“](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="68658-157">Uždarykite puslapį **Modelio susiejimo dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="68658-157">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="68658-158">Uždarykite puslapį **Modelio susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="68658-158">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="68658-159">Formato peržiūra</span><span class="sxs-lookup"><span data-stu-id="68658-159">Review format</span></span>

1. <span data-ttu-id="68658-160">Konfigūracijos medyje išplėskite elemento **Parametrizuotų kvietimų mokymo modelis** turinį.</span><span class="sxs-lookup"><span data-stu-id="68658-160">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="68658-161">Pasirinkite **Parametrizuotų kvietimų mokymo formatas**.</span><span class="sxs-lookup"><span data-stu-id="68658-161">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="68658-162">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="68658-162">Select **Designer**.</span></span> <span data-ttu-id="68658-163">Šis ER formatas sukurtas toliau nurodytiems veiksmams:</span><span class="sxs-lookup"><span data-stu-id="68658-163">This ER format is designed to do the following:</span></span>

  - <span data-ttu-id="68658-164">Sugeneruoti mokesčių ataskaitą XML formatu.</span><span class="sxs-lookup"><span data-stu-id="68658-164">Generate a tax statement in XML format.</span></span>
  - <span data-ttu-id="68658-165">Mokesčių ataskaitoje pateiki šiuos apmokestinimo lygius: „reguliarus“, „sumažintas“ ir „nėra“.</span><span class="sxs-lookup"><span data-stu-id="68658-165">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
  - <span data-ttu-id="68658-166">Pateikti įvairią skirtingo išsamumo kiekvieno apmokestinimo lygio informaciją.</span><span class="sxs-lookup"><span data-stu-id="68658-166">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

  ![Formato dizaino įrankio puslapis](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="68658-168">Pasirinkite **Susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="68658-168">Select **Mapping**.</span></span>
5. <span data-ttu-id="68658-169">Išskleiskite elementus **Modelis**, **Duomenys** ir **Suvestinė**.</span><span class="sxs-lookup"><span data-stu-id="68658-169">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

   <span data-ttu-id="68658-170">Apskaičiuotame lauke **Model.Data.Summary.Level** yra išraiška, kuri grąžina apmokestinimo lygio kodą (**Reguliarus**, **Sumažintas**, **Nėra** arba **Kita**) kaip bet kurio mokesčio kodo tekstinę reikšmę, kurią galima gauti iš duomenų šaltinio **Model.Data.Summary** vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="68658-170">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

  ![Formato konstruktoriaus puslapis, kuriame pateikiama informacija apie duomenų modelį „Parametrizuotų kvietimų mokymo modelis“](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="68658-172">Išplėskite elementą **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="68658-172">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="68658-173">Išplėskite elementą **Model**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="68658-173">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
   <span data-ttu-id="68658-174">Duomenų šaltinis **Model**.**Data2.Summary2** yra sukonfigūruotas taip, kad duomenų šaltinio **Model.Data.Summary** operacijų informacija būtų grupuojama pagal apmokestinimo lygį (kurį grąžina apskaičiuotas laukas **Model.Data.Summary.Level**) ir būtų skaičiuojami agreguoti duomenys.</span><span class="sxs-lookup"><span data-stu-id="68658-174">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

  ![Formato konstruktoriaus puslapis, kuriame pateikiama duomenų šaltinio Model.Data2.Summary2 informacija](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="68658-176">Peržiūrėkite apskaičiuotus laukus **Model**.**Data2.Level1**, **Model**.**Data2.Level2** ir **Model**.**Data2.Level3.**</span><span class="sxs-lookup"><span data-stu-id="68658-176">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="68658-177">Šie apskaičiuoti laukai naudojami filtruoti įrašų sąrašui **Model**.**Data2.Summary2** ir pateikia tik įrašus, atitinkančius konkretų apmokestinimo lygį.</span><span class="sxs-lookup"><span data-stu-id="68658-177">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="68658-178">Uždarykite puslapį **Formato dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="68658-178">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="68658-179">Sukurkite išvestinį formatą</span><span class="sxs-lookup"><span data-stu-id="68658-179">Create a derived format</span></span>
<span data-ttu-id="68658-180">Pateiktą formatą galite patobulini į filtrą įtraukdami vieną apskaičiuotą lauką, kad filtravimas būtų atliekamas pagal reikiamą apmokestinimo lygį, o ne naudojant tris esamus laukus: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** ir **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="68658-180">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="68658-181">Reikiamą apmokestinimo lygį galima nurodyti vietoje, kurioje bus kviečiamas šis naujas apskaičiuotas laukas.</span><span class="sxs-lookup"><span data-stu-id="68658-181">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="68658-182">Konfigūracijos medyje išplėskite elemento **Parametrizuotų kvietimų mokymo modelis** turinį.</span><span class="sxs-lookup"><span data-stu-id="68658-182">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="68658-183">Pasirinkite **Parametrizuotų kvietimų mokymo formatas**.</span><span class="sxs-lookup"><span data-stu-id="68658-183">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="68658-184">Pasirinkite **Kurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="68658-184">Select **Create configuration**.</span></span>
4. <span data-ttu-id="68658-185">Pasirinkite **Kildinti iš pavadinimo: parametrizuotų kvietimų mokymo formatas, „Microsoft“**.</span><span class="sxs-lookup"><span data-stu-id="68658-185">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="68658-186">Lauke **Pavadinimas** įveskite **Parametrizuotų kvietimų mokymo formatas (pasirinktinis)**.</span><span class="sxs-lookup"><span data-stu-id="68658-186">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="68658-187">Pasirinkite **Kurti konfigūraciją.**</span><span class="sxs-lookup"><span data-stu-id="68658-187">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="68658-188">Konfigūruokite parametrizuotą apskaičiuotą lauką, kuriame pateikiamas įrašų sąrašas</span><span class="sxs-lookup"><span data-stu-id="68658-188">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="68658-189">Pradėkite naujai apskaičiuoto lauko pridėjimo veiksmus</span><span class="sxs-lookup"><span data-stu-id="68658-189">Start adding a new calculated field</span></span>

1. <span data-ttu-id="68658-190">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="68658-190">Select **Designer**.</span></span>
2. <span data-ttu-id="68658-191">Pasirinkite **Išplėsti / sutraukti**, kad išplėstumėte visus formato elementus.</span><span class="sxs-lookup"><span data-stu-id="68658-191">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="68658-192">Pasirinkite **Susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="68658-192">Select **Mapping**.</span></span>
4. <span data-ttu-id="68658-193">Išplėskite elementą **Modelis**.</span><span class="sxs-lookup"><span data-stu-id="68658-193">Expand the **Model** item.</span></span>
5. <span data-ttu-id="68658-194">Pasirinkite elementą **Modelis.Duomenys2**.</span><span class="sxs-lookup"><span data-stu-id="68658-194">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="68658-195">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="68658-195">Select **Add**.</span></span>
7. <span data-ttu-id="68658-196">Pasirinkite **Funkcijos\\Apskaičiuotas laukas**.</span><span class="sxs-lookup"><span data-stu-id="68658-196">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="68658-197">Lauke **Pavadinimas** įveskite **Lygiai**.</span><span class="sxs-lookup"><span data-stu-id="68658-197">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="68658-198">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="68658-198">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="68658-199">Nurodykite apskaičiuoto lauko pridėjimo parametrą</span><span class="sxs-lookup"><span data-stu-id="68658-199">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="68658-200">Pasirinkite **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="68658-200">Select **Parameters**.</span></span>
2. <span data-ttu-id="68658-201">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="68658-201">Select **New**.</span></span>
3. <span data-ttu-id="68658-202">Lauke **Pavadinimas** įveskite **Mokesčio lygis**.</span><span class="sxs-lookup"><span data-stu-id="68658-202">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="68658-203">Lauke **Tipas** pasirinkite **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="68658-203">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="68658-204">Nurodant parametro argumento tipą, galima naudoti tik primityviuosius duomenų tipus.</span><span class="sxs-lookup"><span data-stu-id="68658-204">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="68658-205">Todėl šiam tikslui negalima naudoti tipų **Įrašų sąrašas**, **Įrašas** ir **Išvardijimas**.</span><span class="sxs-lookup"><span data-stu-id="68658-205">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="68658-206">Didžiausias parametrų, kuriuos galima nurodyti vienam apskaičiuotam laukui, skaičius yra 8.</span><span class="sxs-lookup"><span data-stu-id="68658-206">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Duomenų šaltinių sąrašo parametras](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="68658-208">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="68658-208">Select **OK**.</span></span>

<span data-ttu-id="68658-209">Pridėdami šį parametrą, nurodote sąlygą, kuri turi būti taikoma šiam apskaičiuojamam laukui iškviesti.</span><span class="sxs-lookup"><span data-stu-id="68658-209">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="68658-210">Kai kviečiate šį apskaičiuotą lauką, turite nurodyti parametro **Mokesčio lygis** argumentą, kuris pateikiamas formatu **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="68658-210">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="68658-211">Įsitikinkite, kad parametrus nurodote tik tiems apskaičiuotiems laukams, kurie yra konteineryje (**Įrašų sąrašas**, **Įrašas** arba **Konteineris**).</span><span class="sxs-lookup"><span data-stu-id="68658-211">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="68658-212">Sukonfigūruotas parametras yra pasiekiamas šio apskaičiuoto lauko duomenų šaltinių sąraše.</span><span class="sxs-lookup"><span data-stu-id="68658-212">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="68658-213">Parametrą į sukonfigūruotą išraišką galite įtraukti pasirinkdami **Įtraukti duomenų šaltinį.**</span><span class="sxs-lookup"><span data-stu-id="68658-213">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Duomenų šaltinio laukai](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="68658-215">Nurodykite apskaičiuoto lauko įtraukimo išraišką</span><span class="sxs-lookup"><span data-stu-id="68658-215">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="68658-216">Laukė **Formulė** įveskite:</span><span class="sxs-lookup"><span data-stu-id="68658-216">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="68658-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="68658-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="68658-218">Iš duomenų šaltinių sąrašo pasirinkite parametrą **Mokesčio lygis**.</span><span class="sxs-lookup"><span data-stu-id="68658-218">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="68658-219">Pasirinkite **Įtraukti duomenų šaltinį**.</span><span class="sxs-lookup"><span data-stu-id="68658-219">Select **Add data source**.</span></span>
4. <span data-ttu-id="68658-220">Lauke **Formulė** užbaikite išraišką:</span><span class="sxs-lookup"><span data-stu-id="68658-220">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="68658-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Mokesčio lygis')**</span><span class="sxs-lookup"><span data-stu-id="68658-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="68658-222">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="68658-222">Select **Save**.</span></span>

    ![Duomenų šaltinio lauko informacija](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="68658-224">Uždarykite puslapį **Formulės konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="68658-224">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="68658-225">Užbaikite naujo apskaičiuoto lauko įtraukimą</span><span class="sxs-lookup"><span data-stu-id="68658-225">Finish adding a new calculated field</span></span>

- <span data-ttu-id="68658-226">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="68658-226">Select **OK**.</span></span>

<span data-ttu-id="68658-227">Puslapyje **Formato kūrimo įrankis** sukonfigūruotam parametrizuotam apskaičiuotam laukui **Lygiai** reikia argumento **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="68658-227">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Išplėstas apskaičiuoto lauko lygių sąrašas](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="68658-229">Naudokite sukonfigūruotą apskaičiuotą lauką formato elementams susieti</span><span class="sxs-lookup"><span data-stu-id="68658-229">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="68658-230">Pasirinkite **Model.Data2.Levels**, kad pasirinktumėte sukonfigūruotą apskaičiuotą lauką.</span><span class="sxs-lookup"><span data-stu-id="68658-230">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="68658-231">Pasirinkite formato elementą **Statement.Taxation.Regular**.</span><span class="sxs-lookup"><span data-stu-id="68658-231">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="68658-232">Pasirinkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="68658-232">Select **Bind**.</span></span>
4. <span data-ttu-id="68658-233">Pasirinkite **Taip**, kad patvirtintumėte naudojamo duomenų šaltinio **Level1** pakeitimą nauju duomenų šaltiniu **Lygiai** visuose pasirinkto formato elemento įdėtuosiuose formato elementuose.</span><span class="sxs-lookup"><span data-stu-id="68658-233">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="68658-234">Taikomas susiejimas sukurtas kaip parametrizuoto apskaičiuoto lauko kvietimas.</span><span class="sxs-lookup"><span data-stu-id="68658-234">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="68658-235">Esant numatytiesiems nustatymams, susieto formato elemento pavadinimas yra naudojamas kaip parametrizuoto apskaičiuoto lauko argumentas esant šioms sąlygoms:</span><span class="sxs-lookup"><span data-stu-id="68658-235">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="68658-236">Apskaičiuotas laukas sukonfigūruotas, kad naudotų vieną parametrą.</span><span class="sxs-lookup"><span data-stu-id="68658-236">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="68658-237">Šio parametro duomenų tipas nurodytas kaip **Eilutė.**</span><span class="sxs-lookup"><span data-stu-id="68658-237">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="68658-238">Kai susieto formato elemento pavadinimas yra tuščias, taikomame susiejime naudojamas šio elemento duomenų šaltinio pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="68658-238">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="68658-239">Pasirinkite formato elementą **Statement.Taxation.Reduced**.</span><span class="sxs-lookup"><span data-stu-id="68658-239">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="68658-240">Pasirinkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="68658-240">Select **Bind**.</span></span>
7. <span data-ttu-id="68658-241">Pasirinkite **Taip**, kad patvirtintumėte naudojamo duomenų šaltinio **Level2** pakeitimą nauju duomenų šaltiniu **Lygiai** visuose pasirinkto formato elemento įdėtuosiuose formato elementuose.</span><span class="sxs-lookup"><span data-stu-id="68658-241">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="68658-242">Pasirinkite formato elementą **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="68658-242">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="68658-243">Pasirinkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="68658-243">Select **Bind**.</span></span>
10. <span data-ttu-id="68658-244">Pasirinkite **Taip**, kad patvirtintumėte naudojamo duomenų šaltinio **Level3** pakeitimą nauju duomenų šaltiniu **Lygiai** visuose pasirinkto formato elemento įdėtuosiuose formato elementuose.</span><span class="sxs-lookup"><span data-stu-id="68658-244">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="68658-245">Kai nurodote XML elemento, atitinkančio apmokestinimo lygį, parametrizuoto apskaičiuoto lauko argumentą (pavyzdžiui, **Model.Data2.Levels("Reduced")** kaip tekstinę reikšmę), jums nebereikia to atlikti su įdėtaisiais XML atributais – susiejimuose bus automatiškai paveldėta pirminiame lygyje nurodyta argumento reikšmė (**Model.Data2.Levels.aggregated.Base**, ne **Model.Data2.Levels("Reduced").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="68658-245">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="68658-246">Negalimi pasikartojantys parametrizuoto apskaičiuoto lauko kvietimai.</span><span class="sxs-lookup"><span data-stu-id="68658-246">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="68658-247">Galite pasirinkti **Redaguoti formulę**ir pakeisti pasirinkto susiejimo parametrizuoto apskaičiuoto lauko numatytąjį argumentą.</span><span class="sxs-lookup"><span data-stu-id="68658-247">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="68658-248">Jei šio argumento nėra, vykdymo metu gali kilti klaidų – vartotojai informuojami apie tokią situaciją naudojamo formato patikrinimo metu.</span><span class="sxs-lookup"><span data-stu-id="68658-248">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Tikrinimo įspėjimo pranešimas](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="68658-250">Sukonfigūruokite parametrizuotą apskaičiuotą lauką, kuris pateikia įrašą</span><span class="sxs-lookup"><span data-stu-id="68658-250">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="68658-251">Kai parametrizuotas apskaičiuotas laukas pateikia įrašą, turite leisti atskirų šio įrašo laukų susiejimą su elementais.</span><span class="sxs-lookup"><span data-stu-id="68658-251">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="68658-252">Tokiais atvejais nebus pirminio susiejimo su argumento reikšme parametrizuoto apskaičiuoto lauko iškvietimui – šią reikšmę reikia nurodyti vieno įrašo lauko susiejime.</span><span class="sxs-lookup"><span data-stu-id="68658-252">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="68658-253">Pradėkite naujai apskaičiuoto lauko pridėjimo veiksmus</span><span class="sxs-lookup"><span data-stu-id="68658-253">Start adding a new calculated field</span></span>

1. <span data-ttu-id="68658-254">Pasirinkite elementą **Modelis.Duomenys2**.</span><span class="sxs-lookup"><span data-stu-id="68658-254">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="68658-255">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="68658-255">Select **Add**.</span></span>
3. <span data-ttu-id="68658-256">Pasirinkite **Funkcijos\\Apskaičiuotas laukas**.</span><span class="sxs-lookup"><span data-stu-id="68658-256">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="68658-257">Lauke **Pavadinimas** įveskite **LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="68658-257">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="68658-258">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="68658-258">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="68658-259">Nurodykite apskaičiuoto lauko pridėjimo parametrą</span><span class="sxs-lookup"><span data-stu-id="68658-259">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="68658-260">Pasirinkite **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="68658-260">Select **Parameters**.</span></span>
2. <span data-ttu-id="68658-261">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="68658-261">Select **New**.</span></span>
3. <span data-ttu-id="68658-262">Lauke **Pavadinimas** įveskite **Mokesčio lygis**.</span><span class="sxs-lookup"><span data-stu-id="68658-262">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="68658-263">Lauke **Tipas** pasirinkite **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="68658-263">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="68658-264">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="68658-264">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="68658-265">Nurodykite apskaičiuoto lauko įtraukimo išraišką</span><span class="sxs-lookup"><span data-stu-id="68658-265">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="68658-266">Lauke **Formulė** įveskite šią išraišką:</span><span class="sxs-lookup"><span data-stu-id="68658-266">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="68658-267">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="68658-267">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="68658-268">Pasirinkite parametrą **Apmokestinimo lygis**.</span><span class="sxs-lookup"><span data-stu-id="68658-268">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="68658-269">Pasirinkite **Įtraukti duomenų šaltinį**.</span><span class="sxs-lookup"><span data-stu-id="68658-269">Select **Add data source**.</span></span>
4. <span data-ttu-id="68658-270">Lake **Formulė** papildykite atliekant 1 veiksmą įvestą išraišką įvesdami **'Apmokestinimo lygis'))**, kad galutinė išraiška būtų tokia:</span><span class="sxs-lookup"><span data-stu-id="68658-270">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="68658-271">**FIRSTORNULL(\@.Levels('Apmokestinimo lygis'))**</span><span class="sxs-lookup"><span data-stu-id="68658-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="68658-272">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="68658-272">Select **Save**.</span></span>
6. <span data-ttu-id="68658-273">Uždarykite puslapį **Formulės konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="68658-273">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="68658-274">Užbaikite naujo apskaičiuoto lauko įtraukimą</span><span class="sxs-lookup"><span data-stu-id="68658-274">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="68658-275">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="68658-275">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="68658-276">Naudokite sukonfigūruotą apskaičiuotą lauką formato elementams susieti</span><span class="sxs-lookup"><span data-stu-id="68658-276">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="68658-277">Išplėskite **Model.Data2.LevelRecord**, kad pasirinktumėte sukonfigūruotą apskaičiuotą lauką.</span><span class="sxs-lookup"><span data-stu-id="68658-277">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="68658-278">Išplėskite sukonfigūruoto apskaičiuoto lauko konteinerį **Model.Data2.LevelRecord.aggregated**.</span><span class="sxs-lookup"><span data-stu-id="68658-278">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="68658-279">Pasirinkite lauką **Model.Data2.LevelRecord.aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="68658-279">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="68658-280">Pasirinkite formato elementą **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="68658-280">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="68658-281">Pasirinkite **Atsieti**.</span><span class="sxs-lookup"><span data-stu-id="68658-281">Select **Unbind**.</span></span>
6. <span data-ttu-id="68658-282">Pasirinkite formato elementą **Statement.Taxation.None.Base**.</span><span class="sxs-lookup"><span data-stu-id="68658-282">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="68658-283">Pasirinkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="68658-283">Select **Bind**.</span></span>
8. <span data-ttu-id="68658-284">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="68658-284">Select **Edit formula**.</span></span>
9. <span data-ttu-id="68658-285">Pakeiskite išraišką į **Model.Data2.LevelRecord("None").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="68658-285">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Atnaujinta išraiška](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="68658-287">Pašalinkite nenaudojamus apskaičiuotus laukus</span><span class="sxs-lookup"><span data-stu-id="68658-287">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="68658-288">Pasirinkite **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="68658-288">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="68658-289">Pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="68658-289">Select **Delete**.</span></span>
3. <span data-ttu-id="68658-290">Pasirinkite **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="68658-290">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="68658-291">Pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="68658-291">Select **Delete**.</span></span>
5. <span data-ttu-id="68658-292">Pasirinkite **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="68658-292">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="68658-293">Pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="68658-293">Select **Delete**.</span></span>
7. <span data-ttu-id="68658-294">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="68658-294">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="68658-295">Susiedami formatą jūs pakartotinai kelis kartus panaudojote tą patį apskaičiuotą lauką **Model.Data2.Levels**.</span><span class="sxs-lookup"><span data-stu-id="68658-295">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="68658-296">Daug paprasčiau naudoti ir tvarkyti vieną apskaičiuojamą lauką, o ne kelis panašius laukus.</span><span class="sxs-lookup"><span data-stu-id="68658-296">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="68658-297">Uždarykite puslapį **Formato dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="68658-297">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="68658-298">Užbaikite pakoreguotą išvestinio formato versiją</span><span class="sxs-lookup"><span data-stu-id="68658-298">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="68658-299">„FastTab“ elemente **Versijos** pasirinkite **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="68658-299">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="68658-300">Pasirinkite **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="68658-300">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="68658-301">Eksportuokite užbaigtą išvestinio formato versiją</span><span class="sxs-lookup"><span data-stu-id="68658-301">Export completed version of a derived format</span></span>

1. <span data-ttu-id="68658-302">Konfigūracijų medyje pasirinkite formatą **Parametrizuotų kvietimų mokymo formatas (pasirinktinis)**.</span><span class="sxs-lookup"><span data-stu-id="68658-302">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="68658-303">„FastTab“ elemente **Versijos** pasirinkite 1.1.1 užbaigtą versiją.</span><span class="sxs-lookup"><span data-stu-id="68658-303">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="68658-304">Pasirinkite **Keitimas**.</span><span class="sxs-lookup"><span data-stu-id="68658-304">Select **Exchange**.</span></span>
4. <span data-ttu-id="68658-305">Pasirinkite **Eksportuoti kaip XML failą**.</span><span class="sxs-lookup"><span data-stu-id="68658-305">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="68658-306">Atsisiųstą konfigūraciją išsaugokite vietoje XML formatu.</span><span class="sxs-lookup"><span data-stu-id="68658-306">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="68658-307">Patikrinkite ER formatus</span><span class="sxs-lookup"><span data-stu-id="68658-307">Test ER formats</span></span> 
<span data-ttu-id="68658-308">Galite paleisti pradinį ir patobulintą ER formatus, kad įsitikintumėte, jog sukonfigūruoti parametrizuoti apskaičiuoti laukai veikia tinkamai.</span><span class="sxs-lookup"><span data-stu-id="68658-308">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="68658-309">Importuokite ER konfigūracijas</span><span class="sxs-lookup"><span data-stu-id="68658-309">Import ER configurations</span></span>
<span data-ttu-id="68658-310">Peržiūrėtas konfigūracijas galite importuoti iš RCS naudodami **RCS** tipo ER saugyklą.</span><span class="sxs-lookup"><span data-stu-id="68658-310">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="68658-311">Jei jau atlikote šioje temoje aprašytus veiksmus, [Importuokite elektroninių ataskaitų konfigūracijas iš „Regulatory Configuration Services“](rcs-download-configurations.md), importuoti prieš tai šioje temoje aptartoms konfigūracijoms į aplinką naudokite sukonfigūruotą ER saugyklą.</span><span class="sxs-lookup"><span data-stu-id="68658-311">If you already went through the steps in the topic, [Import Electronic reporting configurations from Regulatory Configuration Services](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="68658-312">Priešingu atveju atlikite toliau nurodytus veiksmus:</span><span class="sxs-lookup"><span data-stu-id="68658-312">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="68658-313">Pasirinkite įmonę **DEMF** ir numatytoje ataskaitų srityje pasirinkite **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="68658-313">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="68658-314">Pasirinkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="68658-314">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="68658-315">Importuokite iš „Microsoft“ atsisiuntimo centro gautas konfigūracijas tokia tvarka: duomenų modelis, modelio susiejimas, formatas.</span><span class="sxs-lookup"><span data-stu-id="68658-315">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="68658-316">Atlikite šiuos veiksmus su kiekviena ER konfigūracija:</span><span class="sxs-lookup"><span data-stu-id="68658-316">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="68658-317">Pasirinkite **Keitimas.**</span><span class="sxs-lookup"><span data-stu-id="68658-317">Select **Exchange.**</span></span>
    2. <span data-ttu-id="68658-318">Pasirinkite **Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="68658-318">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="68658-319">Pasirinkite **Naršyti**, kad galėtumėte pasirinkti reikiamą ER konfigūraciją XML formatu.</span><span class="sxs-lookup"><span data-stu-id="68658-319">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="68658-320">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="68658-320">Select **OK**.</span></span>

4. <span data-ttu-id="68658-321">Importuokite eksportuotą iš RCS formato **Parametrizuotų kvietimų mokymo formatas (pasirinktinis)** 1.1.1 baigtą versiją:</span><span class="sxs-lookup"><span data-stu-id="68658-321">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="68658-322">Pasirinkite **Keitimas.**</span><span class="sxs-lookup"><span data-stu-id="68658-322">Select **Exchange.**</span></span>
    2. <span data-ttu-id="68658-323">Pasirinkite **Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="68658-323">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="68658-324">Pasirinkite **Naršyti**, kad pasirinktumėte vietoje saugomą XML formato failą **Parametrizuotų kvietimų mokymo formatas (pasirinktinis)**.</span><span class="sxs-lookup"><span data-stu-id="68658-324">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="68658-325">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="68658-325">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="68658-326">Vykdykite ER formatus</span><span class="sxs-lookup"><span data-stu-id="68658-326">Run ER formats</span></span>

1. <span data-ttu-id="68658-327">Konfigūracijos medyje išplėskite elemento **Parametrizuotų kvietimų mokymo modelis** turinį.</span><span class="sxs-lookup"><span data-stu-id="68658-327">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="68658-328">Pasirinkite **Parametrizuotų kvietimų mokymo formatas**.</span><span class="sxs-lookup"><span data-stu-id="68658-328">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="68658-329">Viršutinėje juostoje pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="68658-329">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="68658-330">Įrašykite vietoje sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="68658-330">Save the locally generated output.</span></span>
5. <span data-ttu-id="68658-331">Pasirinkite elementą **Parametrizuotų kvietimų mokymo formatas (pasirinktinis)**.</span><span class="sxs-lookup"><span data-stu-id="68658-331">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="68658-332">Viršutinėje juostoje pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="68658-332">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="68658-333">Vietoje įrašykite sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="68658-333">Save the generated output locally.</span></span> 
8. <span data-ttu-id="68658-334">Palyginkite sugeneruotų išvesčių turinį.</span><span class="sxs-lookup"><span data-stu-id="68658-334">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68658-335">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="68658-335">Additional resources</span></span>
[<span data-ttu-id="68658-336">Elektroninių ataskaitų formulių kūrimo įrankis</span><span class="sxs-lookup"><span data-stu-id="68658-336">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
