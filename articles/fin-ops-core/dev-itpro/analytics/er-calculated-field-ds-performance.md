---
title: ER sprendimų našumo didinimas įtraukiant parametrizuotų duomenų šaltinių APSKAIČIUOTAS LAUKAS
description: Šioje temoje paaiškinama, kaip galite padėti padidinti elektroninių ataskaitų (ER) sprendimų našumą įtraukdami parametrizuotų duomenų šaltinių APSKAIČIUOTAS LAUKAS.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4ee5a074c5c6d2e2144181e39917b1cc42dfc015
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944847"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a><span data-ttu-id="6ca01-103">ER sprendimų našumo didinimas įtraukiant parametrizuotų duomenų šaltinių APSKAIČIUOTAS LAUKAS</span><span class="sxs-lookup"><span data-stu-id="6ca01-103">Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ca01-104">Šioje temoje aiškinama, kaip galima naudoti vykdomų [elektroninių ataskaitų (ER)](general-electronic-reporting.md) formatų [našumo sekimo](trace-execution-er-troubleshoot-perf.md) informaciją našumo gerinimui sukonfigūruojant parametruojamą duomenų šaltinį **Apskaičiuotas laukas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-104">This topic explains how you can take [performance traces](trace-execution-er-troubleshoot-perf.md) of [Electronic reporting (ER)](general-electronic-reporting.md) formats that are run, and then use the information from those traces to help improve performance by configuring a parameterized **Calculated field** data source.</span></span>

<span data-ttu-id="6ca01-105">Kurdami ER konfigūracijas, kuriomis naudojantis generuojami verslo dokumentai, nurodote būdą, kuriuo naudodamiesi gaunate duomenis iš programos, ir įvedate jį į sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="6ca01-105">As part of the process of designing ER configurations to generate business documents, you define the method that is used to retrieve data from the application and enter it in the generated output.</span></span> <span data-ttu-id="6ca01-106">Sukūrę parametrizuotą ER duomenų šaltinį **Apskaičiuotas laukas**, galite sumažinti duomenų bazės skambučių skaičių ir žymiai sumažinti laiką ir išlaidas, susijusias su ER formato vykdymo informacijos rinkimu.</span><span class="sxs-lookup"><span data-stu-id="6ca01-106">By designing a parametrized ER data source of the **Calculated field** type, you can reduce the number of database calls, and significantly reduce the time and cost that are involved in collecting the details of ER format execution.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6ca01-107">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="6ca01-107">Prerequisites</span></span>

- <span data-ttu-id="6ca01-108">Norėdami atlikti šioje temoje pateiktus pavyzdžius, turite turėti prieigą prie vieno iš toliau nurodytų [vaidmenų](../sysadmin/tasks/assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="6ca01-108">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="6ca01-109">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="6ca01-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="6ca01-110">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="6ca01-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="6ca01-111">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="6ca01-111">System administrator</span></span>

- <span data-ttu-id="6ca01-112">Įmonė turi būti nustatyta kaip **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-112">The company must be set to **DEMF**.</span></span>
- <span data-ttu-id="6ca01-113">Norėdami atsisiųsti pavyzdinio „Microsoft“ ER sprendimo, kurio reikia šios temos pavyzdžiams įvykdyti, komponentus, atlikite šios temos [1 priede](#appendix1) nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6ca01-113">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the sample Microsoft ER solution that is required to complete the examples in this topic.</span></span>
- <span data-ttu-id="6ca01-114">Norėdami sukonfigūruoti minimalų ER parametrų rinkinį, kurio reikia norint naudoti ER sistemą, kad būtų galima pagerinti pavyzdinio „Microsoft“ ER sprendimo našumą, atlikite šios temos [2 priede](#appendix2) nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6ca01-114">Follow the steps in [Appendix 2](#appendix2) of this topic to configure the minimal set of ER parameters that is required to use the ER framework to help improve the performance of the sample Microsoft ER solution.</span></span>

## <a name="import-the-sample-er-solution"></a><span data-ttu-id="6ca01-115">Pavyzdinio ER sprendimo importavimas</span><span class="sxs-lookup"><span data-stu-id="6ca01-115">Import the sample ER solution</span></span>

<span data-ttu-id="6ca01-116">Tarkime, kad turite sukurti ER sprendimą, kad būtų sugeneruota nauja ataskaita, kurioje pateikiamos tiekėjo operacijos.</span><span class="sxs-lookup"><span data-stu-id="6ca01-116">Imagine that you must design an ER solution to generate a new report that shows vendor transactions.</span></span> <span data-ttu-id="6ca01-117">Šiuo metu pasirinkto tiekėjo operacijas rasite puslapyje **Tiekėjo operacijos** (eikite į **Mokėtina suma** \> **Tiekėjai** \> **Visi tiekėjai**, pasirinkite tiekėją, paskui veiksmų srities skirtuko **Tiekėjas** grupėje **Operacijos** pasirinkite **Operacijos**).</span><span class="sxs-lookup"><span data-stu-id="6ca01-117">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable** \> **Vendors** \> **All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="6ca01-118">Tačiau norite turėti visas tiekėjo operacijas viename elektroniniame dokumente XML formatu.</span><span class="sxs-lookup"><span data-stu-id="6ca01-118">However, you want to have all vendor transactions together in one electronic document in XML format.</span></span> <span data-ttu-id="6ca01-119">Šį sprendimą sudaro kelios ER konfigūracijos, apimančios reikiamą duomenų modelį, modelio susiejimą ir formato komponentus.</span><span class="sxs-lookup"><span data-stu-id="6ca01-119">This solution will consist of several ER configurations that contain the required data model, model mapping, and format components.</span></span>

<span data-ttu-id="6ca01-120">Pirmas veiksmas yra importuoti pavyzdinį ER sprendimą, kad būtų galima sugeneruoti tiekėjo operacijų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="6ca01-120">The first step is to import the sample ER solution to generate a vendor transactions report.</span></span>

1. <span data-ttu-id="6ca01-121">Prisijunkite prie jūsų įmonei sukurto „Microsoft Dynamics 365 Finance” egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="6ca01-121">Sign in to the instance of Microsoft Dynamics 365 Finance that is provisioned for your company.</span></span>
2. <span data-ttu-id="6ca01-122">Šioje temoje kursite ir modifikuosite pavyzdinės įmonės **„Litware, Inc.“** konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="6ca01-122">In this topic, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="6ca01-123">Įsitikinkite, kad šis konfigūracijos teikėjas buvo įtrauktas į jūsų „Finance“ egzempliorių ir pažymėtas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="6ca01-123">Make sure that this configuration provider has been added to your Finance instance and is marked as active.</span></span> <span data-ttu-id="6ca01-124">Daugiau informacijos žr. [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="6ca01-124">For more information, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="6ca01-125">Darbo srityje **Elektroninės ataskaitos** pasirinkite plytelę **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-125">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="6ca01-126">Puslapyje **Konfigūracijos** importuokite į „Finance” kaip būtinąjį komponentą atsisiųstas ER konfigūracijas tokia tvarka: duomenų modelis, modelio susiejimas, formatas.</span><span class="sxs-lookup"><span data-stu-id="6ca01-126">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into Finance, in the following order: data model, model mapping, format.</span></span> <span data-ttu-id="6ca01-127">Kurdami kiekvieną konfigūraciją atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6ca01-127">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="6ca01-128">Veiksmų srityje pasirinkite **Pakeisti** \> **Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-128">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="6ca01-129">Paspaudę **Naršyti** pasirinkite ER konfigūracijos failą XML formatu.</span><span class="sxs-lookup"><span data-stu-id="6ca01-129">Select **Browse**, and select the appropriate file for the ER configuration in XML format.</span></span>
    3. <span data-ttu-id="6ca01-130">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-130">Select **OK**.</span></span>

![Puslapyje Konfigūracijos importuotos konfigūracijos](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a><span data-ttu-id="6ca01-132">Pavyzdinio ER sprendimo peržiūra</span><span class="sxs-lookup"><span data-stu-id="6ca01-132">Review the sample ER solution</span></span>

### <a name="review-the-model-mapping"></a><span data-ttu-id="6ca01-133">Modelio susiejimo peržiūra</span><span class="sxs-lookup"><span data-stu-id="6ca01-133">Review the model mapping</span></span>

1. <span data-ttu-id="6ca01-134">Puslapyje **Konfigūravimai**, konfigūravimo medyje, išplėskite **Našumo didinimo modelis** ir pasirinkite **Našumo didinimo susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-134">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="6ca01-135">Veiksmų srityje pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-135">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="6ca01-136">Veiksmų srities puslapyje **Duomenų šaltinio susiejimo modelis** pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-136">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>

    <span data-ttu-id="6ca01-137">Šis ER modelio susiejimas sukurtas toliau nurodytiems veiksmams atlikti.</span><span class="sxs-lookup"><span data-stu-id="6ca01-137">This ER model mapping is designed to perform the following actions:</span></span>

    - <span data-ttu-id="6ca01-138">Raskite tiekėjo operacijų, saugomų lentelėje VendTrans, sąrašą (duomenų šaltinis **Operacija**).</span><span class="sxs-lookup"><span data-stu-id="6ca01-138">Fetch the list of vendor transactions that are stored in the VendTrans table (**Trans** data source).</span></span>
    - <span data-ttu-id="6ca01-139">Lentelėje VendTable raskite kiekvienos operacijos tiekėjo įrašą, kuriame buvo užregistruota operacija (duomenų šaltinis **\#Tiekėjas**)</span><span class="sxs-lookup"><span data-stu-id="6ca01-139">For every transaction, fetch, from the VendTable table, the record of a vendor that the transaction has been posted for (**\#Vend** data source).</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ca01-140">Duomenų šaltinis **\#Tiekėjas** sukonfigūruotas, kad būtų galima gauti atitinkamą tiekėjo įrašą naudojant esamą ryšį „daugelis su vienu“ **\@.'\>Relations'.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-140">The **\#Vend** data source is configured to fetch the corresponding vendor record by using the existing many-to-one relation **\@.'\>Relations'.VendTable\_AccountNum**.</span></span>

    <span data-ttu-id="6ca01-141">Modelio žemėlapio nustatymas šiame konfigūravime įgyvendina pagrindinius duomenų modelius bet kuriems ER formatams sukurtiems šiam modeliui ir vykdomiems „Finance“.</span><span class="sxs-lookup"><span data-stu-id="6ca01-141">The model mapping in this configuration implements the base data model for any ER formats that are created for this model and run in Finance.</span></span> <span data-ttu-id="6ca01-142">Todėl duomenų šaltinio **Operacija** turinys tampa prieinamas ER formatams, pvz., abstraktiems **modelio** duomenų šaltiniams.</span><span class="sxs-lookup"><span data-stu-id="6ca01-142">Therefore, the content of the **Trans** data source is exposed for ER formats such as abstract **model** data sources.</span></span>

    ![Duomenų šaltinis Operacija puslapyje Modelio susiejimo dizaino įrankis](media/er-calculated-field-ds-performance-mapping-1.png)

4. <span data-ttu-id="6ca01-144">Uždarykite puslapį **Modelio susiejimo dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-144">Close the **Model mapping designer** page.</span></span>
5. <span data-ttu-id="6ca01-145">Uždarykite puslapį **Duomenų šaltinio susiejimo modelis**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-145">Close the **Model to datasource mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="6ca01-146">Formato peržiūra</span><span class="sxs-lookup"><span data-stu-id="6ca01-146">Review format</span></span>

1. <span data-ttu-id="6ca01-147">Puslapyje **Konfigūravimai**, konfigūravimo medyje, išplėskite **Našumo didinimo modelis** ir pasirinkite **Našumo didinimo formatas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-147">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement format**.</span></span>
2. <span data-ttu-id="6ca01-148">Veiksmų srityje pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-148">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="6ca01-149">Puslapio **Formato dizaino įrankis** skirtuke **Susiejimas** pasirinkite **Išplėsti / sutraukti**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-149">On the **Format designer** page, on the **Mapping** tab, select **Expand/Collapse**.</span></span>
4. <span data-ttu-id="6ca01-150">Išskleiskite elementus **Modelis**, **Duomenys** ir **Operacija**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-150">Expand the **Model**, **Data,** and **Transaction** items.</span></span>

    <span data-ttu-id="6ca01-151">Šis ER formatas sukurtas generuoti tiekėjo operacijų ataskaitą XML formatu.</span><span class="sxs-lookup"><span data-stu-id="6ca01-151">This ER format is designed to generate a vendor transactions report in XML format.</span></span>

    ![Duomenų šaltinių ir sukonfigūruotų formato elementų susiejimų formatavimas formato dizaino įrankio puslapyje](media/er-calculated-field-ds-performance-format.png)

5. <span data-ttu-id="6ca01-153">Uždarykite puslapį **Formato dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-153">Close the **Format designer** page.</span></span>

## <a name="run-the-sample-er-solution-to-trace-execution"></a><span data-ttu-id="6ca01-154">Pavyzdinio ER vykdymo sekimo sprendimo vykdymas</span><span class="sxs-lookup"><span data-stu-id="6ca01-154">Run the sample ER solution to trace execution</span></span>

<span data-ttu-id="6ca01-155">Tarkime, kad baigėte kurti pirmąją ER sprendimo versiją.</span><span class="sxs-lookup"><span data-stu-id="6ca01-155">Imagine that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="6ca01-156">Dabar norite patikrinti sprendimą naudodami savo „Finance“ egzempliorių ir išanalizuoti vykdymo našumą.</span><span class="sxs-lookup"><span data-stu-id="6ca01-156">You now want to test the solution in your Finance instance and analyze the execution performance.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="6ca01-157">ER našumo sekimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="6ca01-157">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="6ca01-158">Pasirinkite įmonę **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-158">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="6ca01-159">Atlikite veiksmus, nurodytus [ER našumo sekimo įjungimas](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace), kad būtų sugeneruotas našumo sekimas, kai vykdomas ER formatas.</span><span class="sxs-lookup"><span data-stu-id="6ca01-159">Follow the steps in [Turn on the ER performance trace](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) to generate a performance trace while an ER format is run.</span></span>

    ![Vartotojo parametrų dialogo langas](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a><span data-ttu-id="6ca01-161">ER formato vykdymas</span><span class="sxs-lookup"><span data-stu-id="6ca01-161">Run the ER format</span></span>

1. <span data-ttu-id="6ca01-162">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-162">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6ca01-163">Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite **Našumo didinimo formatas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-163">On the **Configurations** page, in the configuration tree, select **Performance improvement format**.</span></span>
3. <span data-ttu-id="6ca01-164">Veiksmų srityje pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-164">On the Action Pane, select **Run**.</span></span>

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a><span data-ttu-id="6ca01-165">Našumo sekimo naudojimas modelio susiejimo našumui analizuoti</span><span class="sxs-lookup"><span data-stu-id="6ca01-165">Use the performance trace to analyze model mapping performance</span></span>

1. <span data-ttu-id="6ca01-166">Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite **Našumo didinimo susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-166">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="6ca01-167">Veiksmų srityje pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-167">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="6ca01-168">Veiksmų srities puslapyje **Modelio susiejimai** pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-168">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="6ca01-169">Puslapio **Modelio susiejimo dizaino įrankis** veiksmų srityje pasirinkite **Našumo sekimas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-169">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="6ca01-170">Pasirinkite naujausią sugeneruotą sekimą ir pasirinkite **Gerai** .</span><span class="sxs-lookup"><span data-stu-id="6ca01-170">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="6ca01-171">Atsiranda naujos informacijos apie kai kuriuos dabartinio modelio susiejimo duomenų šaltinio elementus.</span><span class="sxs-lookup"><span data-stu-id="6ca01-171">New information is now available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="6ca01-172">Faktinis laikas, sugaištas gaunant duomenis naudojant duomenų šaltinį</span><span class="sxs-lookup"><span data-stu-id="6ca01-172">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="6ca01-173">Tas pats laikas, išreikštas kaip viso laiko, praleisto vykdant visą modelio susiejimą, procentinė dalis</span><span class="sxs-lookup"><span data-stu-id="6ca01-173">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

![Vykdymo laiko informacija puslapyje Modelio susiejimo dizaino įrankis](./media/er-calculated-field-ds-performance-mapping-2.png)

<span data-ttu-id="6ca01-175">Tinklelyje **Našumo statistika** parodyta, kad duomenų šaltinis **Operacija** iškviečia lentelę VendTrans vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="6ca01-175">The **Performance statistics** grid shows that the **Trans** data source calls the VendTrans table one time.</span></span> <span data-ttu-id="6ca01-176">Duomenų šaltinio **Operacija** reikšmė **\[265\]\[Q:265\]** nurodo, kad 265 tiekėjo operacijos buvo gautos iš programos lentelės ir grąžintos į duomenų modelį.</span><span class="sxs-lookup"><span data-stu-id="6ca01-176">The value **\[265\]\[Q:265\]** of the **Trans** data source indicates that 265 vendor transactions have been fetched from the application table and returned to the data model.</span></span>

<span data-ttu-id="6ca01-177">Tinklelis **Našumo statistika** taip pat parodo, kad dabartinis modelio susiejimas dubliuoja duomenų bazės užklausas, kai vykdomas duomenų šaltinis **\#Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-177">The **Performance statistics** grid also shows that the current model mapping duplicates database requests while the **\#Vend** data source is run.</span></span> <span data-ttu-id="6ca01-178">Šis dubliavimas įvyksta dėl toliau pateiktų priežasčių.</span><span class="sxs-lookup"><span data-stu-id="6ca01-178">This duplication occurs for the following reasons:</span></span>

- <span data-ttu-id="6ca01-179">Tiekėjo lentelė iškviečiama dviem kartus kiekvienai iš 265 pasikartojančių tiekėjo operacijų, iš viso įvykdoma 530 iškvietimų.</span><span class="sxs-lookup"><span data-stu-id="6ca01-179">The vendor table is called two times for each of the 265 iterated vendor transactions, for a total of 530 calls:</span></span>

    - <span data-ttu-id="6ca01-180">Vienas iškvietimas atliekamas norint įvesti tiekėjo kodo numerį.</span><span class="sxs-lookup"><span data-stu-id="6ca01-180">One call is made to enter the vendor account number.</span></span>
    - <span data-ttu-id="6ca01-181">Vienas iškvietimas atliekamas norint įvesti tiekėjo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="6ca01-181">One call is made to enter the vendor name.</span></span>

- <span data-ttu-id="6ca01-182">Tiekėjo lentelė iškviečiama kiekvienai pasikartojančiai tiekėjo operacijai, net jei buvo užregistruotos tik penkių tiekėjų gautos operacijos.</span><span class="sxs-lookup"><span data-stu-id="6ca01-182">The vendor table is called for each iterated vendor transaction, even though the fetched transactions have been posted for only five vendors.</span></span> <span data-ttu-id="6ca01-183">Iš 530 iškvietimų 525 yra dublikatai.</span><span class="sxs-lookup"><span data-stu-id="6ca01-183">Of the 530 calls, 525 are duplicates.</span></span> <span data-ttu-id="6ca01-184">Toliau pateiktame paveikslėlyje parodytas pranešimas apie pasikartojančius iškvietimus, kurį gaunate (duomenų bazės užklausos).</span><span class="sxs-lookup"><span data-stu-id="6ca01-184">The following illustration shows the message that you receive about duplicate calls (database requests).</span></span>

![Pranešimas apie pasikartojančias duomenų bazės užklausas puslapyje Modelio susiejimo dizaino įrankis](./media/er-calculated-field-ds-performance-mapping-2a.png)

<span data-ttu-id="6ca01-186">Atkreipkite dėmesį, kad daugiau nei 80 procentų (maždaug šešios sekundės) viso modelio susiejimo vykdymo laiko (apytiksliai aštuonių sekundžių) buvo panaudota gaunant reikšmes iš programos lentelės VendTable.</span><span class="sxs-lookup"><span data-stu-id="6ca01-186">Of the total model mapping execution time (approximately eight seconds), notice that more than 80 percent (approximately six seconds) has been spent retrieving values from the VendTable application table.</span></span> <span data-ttu-id="6ca01-187">Šis procentas yra per didelis dviems penkių tiekėjų atributams, palyginti su programos lentelės VendTrans informacijos kiekiu.</span><span class="sxs-lookup"><span data-stu-id="6ca01-187">That percentage is too large for two attributes of five vendors, compared with the volume of information from the VendTrans application table.</span></span>

<span data-ttu-id="6ca01-188">Norėdami sumažinti atliekamų iškvietimų skaičių, kad būtų galima gauti kiekvienos operacijos tiekėjo informaciją ir padidinti modelio susiejimo našumą, naudokite duomenų šaltinio **\#Tiekėjas** kaupimą talpykloje.</span><span class="sxs-lookup"><span data-stu-id="6ca01-188">To reduce the number of calls that are made to get the vendor details for every transaction, and to improve the performance of the model mapping, you can use caching for the **\#Vend** data source.</span></span>

> [!NOTE]
> <span data-ttu-id="6ca01-189">Duomenų šaltinis **Operacija\\\#Tiekėjas** bus kaupiamas talpykloje vykdymo metu, duomenų šaltinio **Operacija** dabartinės operacijos aprėptyje.</span><span class="sxs-lookup"><span data-stu-id="6ca01-189">The **Trans\\\#Vend** data source will be cached in the scope of the current transaction of the **Trans** data source at runtime.</span></span>

<span data-ttu-id="6ca01-190">Kaupdami duomenų šaltinį **\#Tiekėjas** saugykloje sumažinate pasikartojančių iškvietimų skaičių nuo 525 iki 260, tačiau pilnai nepašalinate dubliavimo.</span><span class="sxs-lookup"><span data-stu-id="6ca01-190">By caching the **\#Vend** data source, you reduce the number of duplicated calls from 525 to 260, but you don't completely eliminate the duplication.</span></span> <span data-ttu-id="6ca01-191">Norėdami visiškai pašalinti dubliavimą, galite sukonfigūruoti naują parametrizuotą duomenų šaltinį, kurio tipas yra **Apskaičiuotas laukas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-191">To completely eliminate duplication, you can configure a new parameterized data source of the **Calculated field** type.</span></span>

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="6ca01-192">Patobulinkite modelio susiejimą pagal iš vykdymo sekimo gautą informacija</span><span class="sxs-lookup"><span data-stu-id="6ca01-192">Improve the model mapping based on information from the execution trace</span></span>

### <a name="change-the-logic-of-the-model-mapping"></a><span data-ttu-id="6ca01-193">Modelio susiejimo logikos keitimas</span><span class="sxs-lookup"><span data-stu-id="6ca01-193">Change the logic of the model mapping</span></span>

<span data-ttu-id="6ca01-194">Atlikite toliau pateiktus veiksmus, norėdami naudoti kaupimą talpykloje ir duomenų šaltinį, kurio tipas yra **Apskaičiuotas laukas**, kad išvengtumėte pasikartojančių iškvietimų į duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="6ca01-194">Follow these steps to use caching and a data source of the **Calculated field** type, to help prevent duplicate calls to the database.</span></span>

1. <span data-ttu-id="6ca01-195">Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite **Našumo didinimo susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-195">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="6ca01-196">Veiksmų srityje pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-196">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="6ca01-197">Veiksmų srities puslapyje **Modelio susiejimai** pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-197">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="6ca01-198">Puslapyje **Modelio susiejimo dizaino įrankis** atlikite toliau pateiktus veiksmus, norėdami įtraukti duomenų šaltinį, kurio tipas yra **Lentelės įrašai**, kad pasiektumėte įrašus programos lentelėje VendTable.</span><span class="sxs-lookup"><span data-stu-id="6ca01-198">On the **Model mapping designer** page, follow these steps to add a data source of the **Table records** type to access records in the VendTable application table:</span></span>

    1. <span data-ttu-id="6ca01-199">Srityje **Duomenų šaltinio tipai** išplėskite **„Dynamics 365 for Operations”** ir pasirinkite **Lentelės įrašai**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-199">In the **Data source types** pane, expand **Dynamics 365 for Operations**, and select **Table records**.</span></span>
    2. <span data-ttu-id="6ca01-200">Pasirinkite **Įtraukti šaknį**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-200">Select **Add root**.</span></span>
    3. <span data-ttu-id="6ca01-201">Dialogo lango lauke **Pavadinimas** įveskite **Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-201">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    4. <span data-ttu-id="6ca01-202">Lauke **Lentelė** įveskite **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-202">In the **Table** field, enter **VendTable**.</span></span>
    5. <span data-ttu-id="6ca01-203">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-203">Select **OK**.</span></span>

5. <span data-ttu-id="6ca01-204">Galite parametrizuoti iškvietimus į duomenų šaltinius, kurių tipas yra **Apskaičiuotas laukas**, tik jei šie duomenų šaltiniai yra konteineryje.</span><span class="sxs-lookup"><span data-stu-id="6ca01-204">You can parameterize calls to data sources of the **Calculated field** type only if those data sources reside in a container.</span></span> <span data-ttu-id="6ca01-205">Todėl atlikite toliau pateiktus veiksmus, norėdami įtraukti duomenų šaltinį, kurio tipas yra **Tuščias konteineris**, kad būtų galima apdoroti naują parametrizuotą duomenų šaltinį, kurio tipas yra **Apskaičiuotas laukas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-205">Therefore, follow these steps to add a data source of the **Empty container** type to hold a new parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="6ca01-206">Srityje **Duomenų šaltinio tipai** išplėskite **Bendra** ir pasirinkite **Tuščias konteineris**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-206">In the **Data source types** pane, expand **General**, and select **Empty container**.</span></span>
    2. <span data-ttu-id="6ca01-207">Pasirinkite **Įtraukti šaknį**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-207">Select **Add root**.</span></span>
    3. <span data-ttu-id="6ca01-208">Dialogo lango lauke **Pavadinimas** įveskite **Dėžė**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-208">In the dialog box, in the **Name** field, enter **Box**.</span></span>
    3. <span data-ttu-id="6ca01-209">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-209">Select **OK**.</span></span>

    ![Duomenų šaltinis Dėžė puslapyje Modelio susiejimo dizaino įrankis](./media/er-calculated-field-ds-performance-mapping-3.png)

6. <span data-ttu-id="6ca01-211">Atlikite toliau pateiktus veiksmus, norėdami įtraukti parametrizuotą duomenų šaltinį, kurio tipas yra **Apskaičiuotas laukas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-211">Follow these steps to add a parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="6ca01-212">Srityje **Duomenų šaltiniai** pasirinkite **Dėžė**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-212">In the **Data sources** pane, select **Box**.</span></span>
    2. <span data-ttu-id="6ca01-213">Srityje **Duomenų šaltinio tipai** išplėskite **Funkcijos** ir pasirinkite **Apskaičiuotasis laukas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-213">In the **Data source types** pane, expand **Functions**, and select **Calculated field**.</span></span>
    3. <span data-ttu-id="6ca01-214">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-214">Select **Add**.</span></span>
    4. <span data-ttu-id="6ca01-215">Dialogo lango lauke **Pavadinimas** įveskite **Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-215">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    5. <span data-ttu-id="6ca01-216">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-216">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="6ca01-217">Puslapyje **Formulės dizaino įrankis** pasirinkite **Parametrai**, norėdami nurodyti parametrus, kuriuos reikia pateikti, kai šis duomenų šaltinis iškviečiamas.</span><span class="sxs-lookup"><span data-stu-id="6ca01-217">On the **Formula designer** page, select **Parameters** to specify the parameters that must be provided when this data source is called.</span></span>
    7. <span data-ttu-id="6ca01-218">Dialogo lange **Parametrai** pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-218">In the **Parameters** dialog box, select **New**.</span></span>
    8. <span data-ttu-id="6ca01-219">Lauke **Pavadinimas** įveskite **parmVendAccNumber**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-219">In the **Name** field, enter **parmVendAccNumber**.</span></span>
    9. <span data-ttu-id="6ca01-220">Lauke **Tipas** pasirinkite **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-220">In the **Type** field, select **String**.</span></span>
    10. <span data-ttu-id="6ca01-221">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-221">Select **OK**.</span></span>
    11. <span data-ttu-id="6ca01-222">Lauke **Formulė** įveskite **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))** .</span><span class="sxs-lookup"><span data-stu-id="6ca01-222">In the **Formula** field, enter **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span></span>
    12. <span data-ttu-id="6ca01-223">Pasirinkite **Įrašyti** ir uždarykite puslapį **Formulių dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-223">Select **Save**, and close the **Formula designer** page.</span></span>
    13. <span data-ttu-id="6ca01-224">Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="6ca01-224">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="6ca01-225">Atlikite toliau pateiktus veiksmus, kad įtrauktas duomenų šaltinis būtų pažymėtas kaip kaupiamas talpykloje vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="6ca01-225">Follow these steps to mark the added data source as cached during the execution:</span></span>

    1. <span data-ttu-id="6ca01-226">Srityje **Duomenų šaltiniai** pasirinkite **Dėžė\\Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-226">In the **Data sources** pane, select **Box\\Vend**.</span></span>
    2. <span data-ttu-id="6ca01-227">Pasirinkite **Talpykla**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-227">Select **Cache**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ca01-228">Duomenų šaltinis **Dėžė\\Tiekėjas** bus kaupiamas talpykloje vykdymo metu, visų duomenų šaltinio **Operacija** tiekėjo operacijų aprėptyje.</span><span class="sxs-lookup"><span data-stu-id="6ca01-228">The **Box\\Vend** data source will be cached in the scope of all vendor transactions of the **Trans** data source at runtime.</span></span>

8. <span data-ttu-id="6ca01-229">Atlikite toliau pateiktus veiksmus, norėdami atnaujinti įdėtąjį duomenų šaltinį **Operacija\\\#Tiekėjas**, kad jis naudotų duomenų šaltinį **Dėžė\\Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-229">Follow these steps to update the nested **Trans\\\#Vend** data source so that it uses the **Box\\Vend** data source:</span></span>

    1. <span data-ttu-id="6ca01-230">Srityje **Duomenų šaltiniai** išplėskite **Operacija**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-230">In the **Data sources** pane, expand **Trans**.</span></span>
    2. <span data-ttu-id="6ca01-231">Pasirinkite duomenų šaltinį **Operacija\\\#Tiekėjas** ir pasirinkite **Redaguoti** \> **Redaguoti formulę** .</span><span class="sxs-lookup"><span data-stu-id="6ca01-231">Select the **Trans\\\#Vend** data source, and then select **Edit** \> **Edit formula**.</span></span>
    3. <span data-ttu-id="6ca01-232">Puslapio **Formulės dizaino įrankis** lauke **Formulė** įveskite **Box.Vend(\@.AccountNum)** .</span><span class="sxs-lookup"><span data-stu-id="6ca01-232">On the **Formula designer** page, in the **Formula** field, enter **Box.Vend(\@.AccountNum)**.</span></span>
    4. <span data-ttu-id="6ca01-233">Pasirinkite **Įrašyti** ir uždarykite puslapį **Formulių dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-233">Select **Save**, and then close the **Formula designer** page.</span></span>
    5. <span data-ttu-id="6ca01-234">Pasirinkite **Gerai** , kad užbaigtumėte jūsų keitimus pasirinktame duomenų šaltinyje.</span><span class="sxs-lookup"><span data-stu-id="6ca01-234">Select **OK** to complete your changes to the selected data source.</span></span>

9. <span data-ttu-id="6ca01-235">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-235">Select **Save**.</span></span>

    ![Duomenų šaltinis Tiekėjas puslapyje Modelio susiejimo dizaino įrankis](./media/er-calculated-field-ds-performance-mapping-4.png)

10. <span data-ttu-id="6ca01-237">Uždarykite puslapį **Modelio susiejimo dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-237">Close the **Model mapping designer** page.</span></span>
11. <span data-ttu-id="6ca01-238">Uždarykite puslapį **Modelio susiejimai**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-238">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="6ca01-239">Modifikuotos ER modelio susiejimo versijos užbaigimas</span><span class="sxs-lookup"><span data-stu-id="6ca01-239">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="6ca01-240">Puslapio **Konfigūracijos** „FastTab“ **Versijos** pasirinkite konfigūracijos **Našumo didinimo susiejimas** versiją **1.2**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-240">On the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance improvement mapping** configuration.</span></span>
2. <span data-ttu-id="6ca01-241">Pasirinkite **Keisti būseną** \> **Baigti** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-241">Select **Change status** \> **Complete**, and then select **OK**.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="6ca01-242">Modifikuoto ER vykdymo sekimo sprendimo vykdymas</span><span class="sxs-lookup"><span data-stu-id="6ca01-242">Run the modified ER solution to trace execution</span></span>

<span data-ttu-id="6ca01-243">Pakartoję ankstesniame šios temos skyriuje [ER formato vykdymas](#run-format) nurodytus veiksmus sugeneruokite naują našumo sekimą.</span><span class="sxs-lookup"><span data-stu-id="6ca01-243">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a><span data-ttu-id="6ca01-244">Našumo sekimo naudojimas modelio susiejimo koregavimams analizuoti</span><span class="sxs-lookup"><span data-stu-id="6ca01-244">Use the performance trace to analyze adjustments to the model mapping</span></span> 

1. <span data-ttu-id="6ca01-245">Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite **Našumo didinimo susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-245">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="6ca01-246">Veiksmų srityje pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-246">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="6ca01-247">Veiksmų srities puslapyje **Modelio susiejimai** pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-247">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="6ca01-248">Puslapio **Modelio susiejimo dizaino įrankis** veiksmų srityje pasirinkite **Našumo sekimas**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-248">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="6ca01-249">Pasirinkite naujausią sugeneruotą sekimą ir pasirinkite **Gerai** .</span><span class="sxs-lookup"><span data-stu-id="6ca01-249">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="6ca01-250">Atkreipkite dėmesį, kad atlikus modelio susiejimo pakeitimus, nebeliko pasikartojančių užklausų į duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="6ca01-250">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="6ca01-251">Taip pat sumažėjo šio modelio susiejimo iškvietimų į duomenų bazės lenteles ir duomenų šaltinius skaičius.</span><span class="sxs-lookup"><span data-stu-id="6ca01-251">The number of calls to database tables and data sources for this model mapping has also been reduced.</span></span>

![Informacijos sekimas 1 puslapyje Modelio susiejimo dizaino įrankis](./media/er-calculated-field-ds-performance-mapping-5.png)

<span data-ttu-id="6ca01-253">Bendras vykdymo laikas buvo sumažintas 20 kartų (nuo maždaug 8 sekundžių iki maždaug 400 milisekundžių).</span><span class="sxs-lookup"><span data-stu-id="6ca01-253">The total execution time has been reduced about 20 times (from about 8 seconds to about 400 milliseconds).</span></span> <span data-ttu-id="6ca01-254">Todėl pagerėjo viso ER sprendimo našumas.</span><span class="sxs-lookup"><span data-stu-id="6ca01-254">Therefore, the performance of the whole ER solution has been improved.</span></span>

![Informacijos sekimas 2 puslapyje Modelio susiejimo dizaino įrankis](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a><span data-ttu-id="6ca01-256">1 priedas: pavyzdinio „Microsoft” ER sprendimo komponentų atsisiuntimas</span><span class="sxs-lookup"><span data-stu-id="6ca01-256">Appendix 1: Download the components of the sample Microsoft ER solution</span></span>

<span data-ttu-id="6ca01-257">Turite atsiųsti ir vietoje saugoti toliau nurodytus failus.</span><span class="sxs-lookup"><span data-stu-id="6ca01-257">You must download the following files and store them locally.</span></span>

| <span data-ttu-id="6ca01-258">Failas</span><span class="sxs-lookup"><span data-stu-id="6ca01-258">File</span></span>                                        | <span data-ttu-id="6ca01-259">Turinys</span><span class="sxs-lookup"><span data-stu-id="6ca01-259">Content</span></span> |
|---------------------------------------------|---------|
| <span data-ttu-id="6ca01-260">Našumo didinimo model.version.1</span><span class="sxs-lookup"><span data-stu-id="6ca01-260">Performance improvement model.version.1</span></span>     | [<span data-ttu-id="6ca01-261">ER duomenų modelio konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="6ca01-261">Sample ER data model configuration</span></span>](https://download.microsoft.com/download/4/6/f/46f0f3fa-782b-414a-8f7b-b6c64a388661/Performance_improvement_model.version.1.xml) |
| <span data-ttu-id="6ca01-262">Našumo didinimo mapping.version.1.1</span><span class="sxs-lookup"><span data-stu-id="6ca01-262">Performance improvement mapping.version.1.1</span></span> | [<span data-ttu-id="6ca01-263">ER modelio susiejimo konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="6ca01-263">Sample ER model mapping configuration</span></span>](https://download.microsoft.com/download/8/9/1/8913a763-afb8-4bf4-aaf1-95ad793ffc5a/Performance_improvement_mapping.version.1.1.xml) |
| <span data-ttu-id="6ca01-264">Našumo didinimo format.version.1.1</span><span class="sxs-lookup"><span data-stu-id="6ca01-264">Performance improvement format.version.1.1</span></span>  | [<span data-ttu-id="6ca01-265">ER formato konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="6ca01-265">Sample ER format configuration</span></span>](https://download.microsoft.com/download/9/0/c/90c75963-bc78-4edc-9096-556bbe281f10/Performance_improvement_format.version.1.1.xml) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a><span data-ttu-id="6ca01-266">2 priedas: ER sistemos konfigūracija</span><span class="sxs-lookup"><span data-stu-id="6ca01-266">Appendix 2: Configure the ER framework</span></span>

<span data-ttu-id="6ca01-267">Prieš pradėdami naudoti ER sistemą, kad būtų padidintas pavyzdinio „Microsoft” ER sprendimo našumas, turite sukonfigūruoti minimalų ER parametrų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="6ca01-267">Before you can start to use the ER framework to improve the performance of the sample Microsoft ER solution, you must configure the minimal set of ER parameters.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="6ca01-268">ER parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="6ca01-268">Configure ER parameters</span></span>

1. <span data-ttu-id="6ca01-269">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-269">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6ca01-270">**Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** pasirinkite **Elektroninių ataskaitų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-270">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="6ca01-271">**Elektroninių ataskaitų parametrai** puslapyje **Bendra** skirtuke nustatykite **Įjungti dizaino režimą** parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-271">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="6ca01-272">**Priedai** skirtuke nustatykite tolesnius parametrus:</span><span class="sxs-lookup"><span data-stu-id="6ca01-272">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="6ca01-273">**Konfigūracijos** lauke pasirinkite **Failas** tipą, skirtą **DEMF** įmonei.</span><span class="sxs-lookup"><span data-stu-id="6ca01-273">In the **Configurations** field, select the **File** type for the **DEMF** company.</span></span>
    - <span data-ttu-id="6ca01-274"> **Užduoties archyvas**, **Laikini**, **Bazinė linija** ir **Kiti** laukuose pasirinkite **Failas** tipą.</span><span class="sxs-lookup"><span data-stu-id="6ca01-274">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="6ca01-275">Norėdami sužinoti daugiau apie ER parametrus, žr. [ER sistemos konfigūracija](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6ca01-275">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="6ca01-276">ER konfigūracijos tiekėjo aktyvavimas</span><span class="sxs-lookup"><span data-stu-id="6ca01-276">Activate an ER configuration provider</span></span>

<span data-ttu-id="6ca01-277">Kiekviena pridėta ER konfigūracija pažymėta kaip priklausanti ER konfigūracijos teikėjui.</span><span class="sxs-lookup"><span data-stu-id="6ca01-277">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="6ca01-278">ER konfigūracijos tiekėjas, kuris aktyvuojamas **Elektroninė ataskaita** darbo srityje naudojamas šiam tikslui.</span><span class="sxs-lookup"><span data-stu-id="6ca01-278">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="6ca01-279">Todėl turite aktyvuoti ER konfigūracijos tiekėją **Elektroninė ataskaita** darbo srityje prieš pridėdami ar redaguodami ER konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="6ca01-279">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="6ca01-280">Tik ER konfigūracijos savininkas gali redaguoti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="6ca01-280">Only the owner of an ER configuration can edit the configuration.</span></span> <span data-ttu-id="6ca01-281">Todėl prieš redaguojant ER konfigūraciją atitinkamas ER konfigūracijos tiekėjas turi būti aktyvuotas **Elektroninė ataskaita** darbo srityje.</span><span class="sxs-lookup"><span data-stu-id="6ca01-281">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="6ca01-282">ER konfigūracijos teikėjų sąrašo peržiūra</span><span class="sxs-lookup"><span data-stu-id="6ca01-282">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="6ca01-283">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-283">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6ca01-284">**Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** skyriuje pasirinkite **Konfigūracijos tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-284">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="6ca01-285">**Konfigūracijos teikėjo lentelė** puslapyje kiekvienas teikėjo įrašas turi unikalų pavadinimą ir URL.</span><span class="sxs-lookup"><span data-stu-id="6ca01-285">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="6ca01-286">Peržiūrėkite šio puslapio turinį.</span><span class="sxs-lookup"><span data-stu-id="6ca01-286">Review the contents of this page.</span></span> <span data-ttu-id="6ca01-287">Jei įrašas, skirtas **Litware, Inc.** jau yra, praleiskite sekančią procedūrą, [Pridėkite naują ER konfigūracijos teikėją](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="6ca01-287">If a record for **Litware, Inc.** already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="6ca01-288">Pridėkite naują ER konfigūracijos tiekėją</span><span class="sxs-lookup"><span data-stu-id="6ca01-288">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="6ca01-289">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-289">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6ca01-290">**Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** skyriuje pasirinkite **Konfigūracijos tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-290">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="6ca01-291">**Konfigūracijos tiekėjai** puslapyje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-291">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="6ca01-292">Lauke **Pavadinimas** įveskite **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="6ca01-292">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="6ca01-293">**Internetinis adresas** lauke įveskite `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="6ca01-293">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="6ca01-294">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-294">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="6ca01-295">ER konfigūracijos tiekėjo aktyvavimas</span><span class="sxs-lookup"><span data-stu-id="6ca01-295">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="6ca01-296">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-296">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6ca01-297">**Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos teikėjai** dalyje pasirinkite **„Litware, Inc.”** plytelę ir pasirinkite **Nustatyti kaip aktyvų**.</span><span class="sxs-lookup"><span data-stu-id="6ca01-297">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="6ca01-298">Daugiau informacijos apie ER konfigūracijos tiekėjus žr. [Konfigūracijos teikėjų kūrimas pažymint juos kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="6ca01-298">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ca01-299">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="6ca01-299">Additional resources</span></span>

- [<span data-ttu-id="6ca01-300">Elektroninių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="6ca01-300">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="6ca01-301">ER formatų vykdymo sekimas siekiant diagnozuoti našumo problemas</span><span class="sxs-lookup"><span data-stu-id="6ca01-301">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="6ca01-302">Apskaičiuoto lauko tipo ER duomenų šaltinių parametrizuotų kvietimų palaikymas</span><span class="sxs-lookup"><span data-stu-id="6ca01-302">Support parameterized calls of ER data sources of the Calculated field type</span></span>](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
