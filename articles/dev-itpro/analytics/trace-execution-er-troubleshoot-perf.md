---
title: ER formato vykdymo sekimas siekiant diagnozuoti našumo problemas
description: Šioje temoje pateikiama informacijos apie tai, kaip elektroninėse ataskaitose (ER) naudojantis našumo sekimo funkcija spręsti našumo problemas.
author: NickSelin
manager: AnnBe
ms.date: 05/08/2019
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
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: aa71db2752889bc905c22bab1cf2fa46d7ee07c7
ms.sourcegitcommit: 67d00b95952faf0db580d341249d4e50be59119c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1576551"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="5b76d-103">ER formatų vykdymo sekimas siekiant diagnozuoti našumo problemas</span><span class="sxs-lookup"><span data-stu-id="5b76d-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5b76d-104">Kurdami elektroninių ataskaitų (ER) konfigūracijas, kuriomis naudojantis generuojami elektroniniai dokumentai, nurodote būdą, kuriuo naudodamiesi gaunate duomenis iš „Microsoft Dynamics 365 for Finance and Operations“, ir įvedate jį į sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="5b76d-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of Microsoft Dynamics 365 for Finance and Operations and enter it in the output that is generated.</span></span> <span data-ttu-id="5b76d-105">Naudojantis ER našumo sekimo funkcija gali pastebimai sutrumpėti laikas, per kurį renkama informacija apie ER formato vykdymą, panaudojant ją našumo problemoms spręsti, ir gali būti patiriama mažiau išlaidų.</span><span class="sxs-lookup"><span data-stu-id="5b76d-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="5b76d-106">Šioje mokymo programoje pateikiama rekomendacijų apie tai, kaip atsižvelgti į įvykdytų „Finance and Operations“ ER formatų našumo sekimus ir kaip panaudoti šiuos sekimus siekiant pagerinti našumą.</span><span class="sxs-lookup"><span data-stu-id="5b76d-106">This tutorial provides guidelines about how to take performance traces for executed ER formats in Finance and Operations, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5b76d-107">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="5b76d-107">Prerequisites</span></span>

<span data-ttu-id="5b76d-108">Norint įvykdyti šios mokymo programos pavyzdžių užduotis, reikia toliau nurodytų prieigų.</span><span class="sxs-lookup"><span data-stu-id="5b76d-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="5b76d-109">Prieiga prie „Finance and Operations“ naudojant vieną iš tolesnių vaidmenų.</span><span class="sxs-lookup"><span data-stu-id="5b76d-109">Access to Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="5b76d-110">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="5b76d-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="5b76d-111">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="5b76d-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="5b76d-112">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="5b76d-112">System administrator</span></span>

- <span data-ttu-id="5b76d-113">Prieiga prie „Regulatory Configuration Services“ (RCS) egzemplioriaus, kuris sukurtas tam pačiam nuomininkui, kaip „Finance and Operations“, vienam iš toliau nurodytų vaidmenų atlikti.</span><span class="sxs-lookup"><span data-stu-id="5b76d-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance and Operations, for one of the following roles:</span></span>

    - <span data-ttu-id="5b76d-114">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="5b76d-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="5b76d-115">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="5b76d-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="5b76d-116">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="5b76d-116">System administrator</span></span>

<span data-ttu-id="5b76d-117">Taip pat turite atsiųsti ir vietoje saugoti toliau nurodytus failus.</span><span class="sxs-lookup"><span data-stu-id="5b76d-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="5b76d-118">Failas</span><span class="sxs-lookup"><span data-stu-id="5b76d-118">File</span></span>                                  | <span data-ttu-id="5b76d-119">Turinys</span><span class="sxs-lookup"><span data-stu-id="5b76d-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="5b76d-120">Našumo sekimo modelis.versija.1</span><span class="sxs-lookup"><span data-stu-id="5b76d-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="5b76d-121">ER duomenų modelio konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="5b76d-121">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| <span data-ttu-id="5b76d-122">Našumo sekimo metaduomenys.versija.1</span><span class="sxs-lookup"><span data-stu-id="5b76d-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="5b76d-123">ER metaduomenų konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="5b76d-123">Sample ER metadata configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| <span data-ttu-id="5b76d-124">Našumo sekimo susiejimas.versija.1.1</span><span class="sxs-lookup"><span data-stu-id="5b76d-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="5b76d-125">ER modelio susiejimo konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="5b76d-125">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="5b76d-126">Našumo sekimo formatas.versija.1.1</span><span class="sxs-lookup"><span data-stu-id="5b76d-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="5b76d-127">ER formato konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="5b76d-127">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="5b76d-128">ER parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="5b76d-128">Configure ER parameters</span></span>

<span data-ttu-id="5b76d-129">Kiekvienas „Finance and Operations“ sugeneruotas ER našumo sekimas saugomas kaip vykdymo žurnalo įrašo priedas.</span><span class="sxs-lookup"><span data-stu-id="5b76d-129">Each ER performance trace that is generated in Finance and Operations is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="5b76d-130">Šiems priedams tvarkyti naudojama „Finance and Operations“ dokumentų tvarkymo (DM) sistema.</span><span class="sxs-lookup"><span data-stu-id="5b76d-130">The Document management (DM) framework of Finance and Operations is used to manage these attachments.</span></span> <span data-ttu-id="5b76d-131">Norėdami nurodyti DM dokumento tipą, kuris turėtų būti naudojamas našumo sekimams pridėti, turite iš anksto sukonfigūruoti ER parametrus.</span><span class="sxs-lookup"><span data-stu-id="5b76d-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="5b76d-132">„Finance and Operation“ darbo srityje **Elektroninės ataskaitos** pasirinkite **Elektroninių ataskaitų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-132">In Finance and Operation, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="5b76d-133">Tada puslapyje **Elektroninių ataskaitų parametrai** esančio skirtuko **Priedai** lauke **Kiti** pasirinkite DM dokumento tipą, kuris bus naudojamas našumo sekimui.</span><span class="sxs-lookup"><span data-stu-id="5b76d-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Elektroninių ataskaitų parametrų puslapis „Finance and Operations“](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="5b76d-135">Norint, kad DM dokumento tipu būtų galima naudotis peržvalgos lauke **Kiti**, jis turi būti atitinkamai sukonfigūruotas puslapyje **Dokumentų tipai** (**Organizacijos administravimas \> Dokumentų valdymas \> Dokumentų tipai**):</span><span class="sxs-lookup"><span data-stu-id="5b76d-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="5b76d-136">**Klasė:** pridėti failą</span><span class="sxs-lookup"><span data-stu-id="5b76d-136">**Class:** Attach file</span></span>
- <span data-ttu-id="5b76d-137">**Grupė:** failas</span><span class="sxs-lookup"><span data-stu-id="5b76d-137">**Group:** File</span></span>

![Dokumentų tipų puslapis „Finance and Operations“](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="5b76d-139">Pasirinktas dokumento tipas turi būti pasiekiamas visose dabartinio „Finance and Operations“ egzemplioriaus įmonėse, nes DM priedai skirti įmonei.</span><span class="sxs-lookup"><span data-stu-id="5b76d-139">The selected document type must be available in every company of the current Finance and Operations instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="5b76d-140">RCS parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="5b76d-140">Configure RCS parameters</span></span>

<span data-ttu-id="5b76d-141">„Finance and Operations“ sugeneruoti ER našumo sekimai importuojami į RCS analizei atlikti naudojant ER formato dizaino įrankį ir ER susiejimo dizaino įrankį.</span><span class="sxs-lookup"><span data-stu-id="5b76d-141">ER performance traces that are generated in Finance and Operations will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="5b76d-142">Kadangi ER našumo sekimai saugomi kaip su ER formatu susieto vykdymo žurnalo įrašo priedai, reikia iš anksto konfigūruoti RCS parametrus, kad būtų nurodytas DM dokumento tipas, kuris turėtų būti naudojamas našumo sekimams pridėti.</span><span class="sxs-lookup"><span data-stu-id="5b76d-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="5b76d-143">Jūsų įmonei sukurto RCS egzemplioriaus darbo srityje **Elektroninės ataskaitos** pasirinkite **Elektroninių ataskaitų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="5b76d-144">Tada puslapyje **Elektroninių ataskaitų parametrai** esančio skirtuko **Priedai** lauke **Kiti** pasirinkite DM dokumento tipą, kuris bus naudojamas našumo sekimui.</span><span class="sxs-lookup"><span data-stu-id="5b76d-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![RCS elektroninių ataskaitų parametrų puslapis](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="5b76d-146">Norint, kad DM dokumento tipu būtų galima naudotis peržvalgos lauke **Kiti**, jis turi būti atitinkamai sukonfigūruotas puslapyje **Dokumentų tipai** (**Organizacijos administravimas \> Dokumentų valdymas \> Dokumentų tipai**):</span><span class="sxs-lookup"><span data-stu-id="5b76d-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="5b76d-147">**Klasė:** pridėti failą</span><span class="sxs-lookup"><span data-stu-id="5b76d-147">**Class:** Attach file</span></span>
- <span data-ttu-id="5b76d-148">**Grupė:** failas</span><span class="sxs-lookup"><span data-stu-id="5b76d-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="5b76d-149">ER sprendimo kūrimas</span><span class="sxs-lookup"><span data-stu-id="5b76d-149">Design an ER solution</span></span>

<span data-ttu-id="5b76d-150">Tarkime, kad jau pradėjau kurti naują ER sprendimą, kad būtų sugeneruota nauja ataskaita, kurioje pateikiamos tiekėjo operacijos.</span><span class="sxs-lookup"><span data-stu-id="5b76d-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="5b76d-151">Šiuo metu pasirinkto tiekėjo operacijas rasite puslapyje **Tiekėjo operacijos** (eikite į **Mokėtina suma \> Tiekėjai \> Visi tiekėjai**, pasirinkite tiekėją, paskui veiksmų srities skirtuko **Tiekėjas** grupėje **Operacijos** pasirinkite **Operacijos**).</span><span class="sxs-lookup"><span data-stu-id="5b76d-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="5b76d-152">Tačiau norite vienu metu turėti visas tiekėjo operacijas viename elektroniniame dokumente XML formatu.</span><span class="sxs-lookup"><span data-stu-id="5b76d-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="5b76d-153">Šį sprendimą sudaro kelios ER konfigūracijos, apimančios reikiamą duomenų modelį, metaduomenis, modelio susiejimą ir formato komponentus.</span><span class="sxs-lookup"><span data-stu-id="5b76d-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="5b76d-154">Prisijunkite prie jūsų įmonei sukurto RCS egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="5b76d-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="5b76d-155">Šioje mokymo programoje kursite ir modifikuosite pavyzdinės įmonės **„Litware, Inc.“** konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="5b76d-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="5b76d-156">Todėl įsitikinkite, kad šis konfigūracijos teikėjas buvo pridėtas prie RCS ir pasirinktas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="5b76d-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="5b76d-157">Instrukcijos aprašytos procedūroje [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="5b76d-157">For instructions, see the [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) procedure.</span></span>
3. <span data-ttu-id="5b76d-158">Darbo srityje **Elektroninės ataskaitos** pasirinkite plytelę **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="5b76d-159">Puslapyje **Konfigūracijos** importuokite į RCS kaip būtinąjį komponentą atsisiųstas ER konfigūracijas tokia tvarka: duomenų modelis, metaduomenys, modelio susiejimas, formatas.</span><span class="sxs-lookup"><span data-stu-id="5b76d-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="5b76d-160">Kurdami kiekvieną konfigūraciją atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5b76d-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="5b76d-161">Veiksmų srityje pasirinkite **Keitimas \> Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="5b76d-162">Paspaudę **Naršyti** pasirinkite reikiamą ER konfigūracijos failą XML formatu.</span><span class="sxs-lookup"><span data-stu-id="5b76d-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="5b76d-163">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-163">Select **OK**.</span></span>

    ![RCS puslapis Konfigūracijos](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="5b76d-165">ER vykdymo sekimo sprendimo vykdymas</span><span class="sxs-lookup"><span data-stu-id="5b76d-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="5b76d-166">Tarkime, kad baigėte kurti pirmąją ER sprendimo versiją.</span><span class="sxs-lookup"><span data-stu-id="5b76d-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="5b76d-167">Dabar norite ją patikrinti naudodami savo „Finance and Operations“ egzempliorių ir išanalizuoti vykdymo našumą.</span><span class="sxs-lookup"><span data-stu-id="5b76d-167">You now want to test it in your Finance and Operations instance and analyze execution performance.</span></span>

### <a id='import-configuration'></a><span data-ttu-id="5b76d-168">ER konfigūracijos importavimas iš RCS į „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="5b76d-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="5b76d-169">Prisijunkite prie savo „Finance and Operations“ egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="5b76d-169">Sign in to your Finance and Operations instance.</span></span>
2. <span data-ttu-id="5b76d-170">Dirbdami su šia mokymo programa, konfigūracijas importuosite iš savo RCS egzemplioriaus (kuriame kuriate savo ER komponentus) į savo „Finance and Operations“ egzempliorių (kuriame jas tikrinate ir galiausiai naudojate).</span><span class="sxs-lookup"><span data-stu-id="5b76d-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your Finance and Operations instance (where you test and finally use them).</span></span> <span data-ttu-id="5b76d-171">Todėl turite įsitikinti, kad paruošti visi reikiami artefaktai.</span><span class="sxs-lookup"><span data-stu-id="5b76d-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="5b76d-172">Instrukcijas rasite procedūroje [Elektroninių ataskaitų (ER) konfigūracijų importavimas iš „Regulatory Configuration Services“ (RCS)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations).</span><span class="sxs-lookup"><span data-stu-id="5b76d-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations) procedure.</span></span>
3. <span data-ttu-id="5b76d-173">Atlikę toliau nurodytus veiksmus importuokite konfigūracijas iš RCS į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="5b76d-173">Follow these steps to import the configurations from RCS into Finance and Operations:</span></span>

    1. <span data-ttu-id="5b76d-174">Darbo srityje **Elektroninės ataskaitos** konfigūracijos tiekėjui **„Litware, Inc.“** skirtoje plytelėje pasirinkite **Saugyklos**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="5b76d-175">Puslapyje **Konfigūracijų saugykla** pasirinkite tipo **RCS** saugyklą, paskui pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="5b76d-176">„FastTab“ **Konfigūracijos** pasirinkite konfigūraciją **Našumo sekimo formatas**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="5b76d-177">„FastTab“ **Versijos** pasirinkite pasirinktos ER konfigūracijos versiją **1.1**, paskui pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![„Finance and Operations“ konfigūracijų saugyklos puslapis](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="5b76d-179">Atitinkamų versijų duomenų modeliai ir modelio susiejimo konfigūracijos automatiškai importuojami kaip būtinieji importuotos ER formato konfigūracijos komponentai.</span><span class="sxs-lookup"><span data-stu-id="5b76d-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="5b76d-180">ER veiklos sekimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="5b76d-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="5b76d-181">„Finance and Operations“ eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-181">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="5b76d-182">Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="5b76d-183">Dialogo lango **Vartotojo parametrai** skyriuje **Vykdymo sekimas** atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5b76d-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="5b76d-184">Lauke **Vykdymo sekimo formatas** pasirinkite **Derinti sekimo formatą**, kad būtų galima rinkti informaciją apie ER formato vykdymą.</span><span class="sxs-lookup"><span data-stu-id="5b76d-184">In the **Execution trace format** field, select **Debug trace format** to start to collect the details of ER format execution.</span></span> <span data-ttu-id="5b76d-185">Pasirinkus šią reikšmę, našumo sekimas renka informaciją apie laiką, sugaištą toliau nurodytiems veiksmams atlikti.</span><span class="sxs-lookup"><span data-stu-id="5b76d-185">When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</span></span>

        - <span data-ttu-id="5b76d-186">Kiekvieno duomenims gauti iškviesto modelio susiejimo duomenų šaltinio vykdymas</span><span class="sxs-lookup"><span data-stu-id="5b76d-186">Running each data source in the model mapping that is called to get data</span></span>
        - <span data-ttu-id="5b76d-187">Kiekvieno formato elemento apdorojimas įvedant duomenis į sugeneruotą išvestį</span><span class="sxs-lookup"><span data-stu-id="5b76d-187">Processing each format item to enter data in the output that is generated</span></span>

        <span data-ttu-id="5b76d-188">Laukas **Vykdymo sekimo formatas** naudojamas norint nurodyti sugeneruoto našumo sekimo formatą, kurio vykdymo informacija saugoma, kad būtų galima nustatyti ER formatą ir susiejimo elementus.</span><span class="sxs-lookup"><span data-stu-id="5b76d-188">You use the **Execution trace format** field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</span></span> <span data-ttu-id="5b76d-189">Kaip reikšmę pasirinkę **Derinti sekimo formatą** galėsite analizuoti sekimo turinį naudodami ER operacijų dizaino įrankį ir peržiūrėti sekime minimus ER formato arba siejimo elementus.</span><span class="sxs-lookup"><span data-stu-id="5b76d-189">By selecting **Debug trace format** as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</span></span>

    2. <span data-ttu-id="5b76d-190">Nustatykite tolesnių parinkčių reikšmes **Taip**, kad būtų galima rinkti konkrečią informaciją apie ER modelio susiejimo vykdymą ir ER formato komponentus.</span><span class="sxs-lookup"><span data-stu-id="5b76d-190">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="5b76d-191">**Rinkti užklausų statistiką** – įjungus šią parinktį, našumo sekimas renka toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="5b76d-191">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="5b76d-192">Duomenų šaltinių atliktų duomenų bazės iškvietimų skaičius</span><span class="sxs-lookup"><span data-stu-id="5b76d-192">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="5b76d-193">Pasikartojančių iškvietimų į duomenų bazę skaičius</span><span class="sxs-lookup"><span data-stu-id="5b76d-193">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="5b76d-194">Informacija apie duomenų bazės iškvietimams atlikti naudotus SQL išrašus</span><span class="sxs-lookup"><span data-stu-id="5b76d-194">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="5b76d-195">**Talpyklos sekimo prieiga** – įjungus šią parinktį, našumo sekimas renka informaciją apie ER modelio susiejimo talpyklos naudojimą.</span><span class="sxs-lookup"><span data-stu-id="5b76d-195">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="5b76d-196">**Sekimo duomenų prieiga** – įjungus šią parinktį, našumo sekimas renka informaciją apie iškvietimų į įvykdytų įrašo sąrašo tipo duomenų šaltinių duomenų bazę skaičių.</span><span class="sxs-lookup"><span data-stu-id="5b76d-196">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="5b76d-197">**Sekimų sąrašo išvardijimas** – įjungus šią parinktį, našumo sekimas renka informaciją apie iš įrašo sąrašo tipo duomenų šaltinių pageidaujamų įrašų skaičių.</span><span class="sxs-lookup"><span data-stu-id="5b76d-197">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5b76d-198">Dialogo lange **Vartotojo parametrai** nurodyti vartotojo ir dabartinės įmonės parametrai.</span><span class="sxs-lookup"><span data-stu-id="5b76d-198">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![„Finance and Operations“ vartotojo parametrų dialogo langas](./media/GER-PerfTrace-GER-UserParameters.png)

### <a id='run-format'></a><span data-ttu-id="5b76d-200">ER formato vykdymas</span><span class="sxs-lookup"><span data-stu-id="5b76d-200">Run the ER format</span></span>

1. <span data-ttu-id="5b76d-201">„Finance and Operations“ pasirinkite įmonę **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-201">In Finance and Operations, select the **DEMF** company.</span></span>
2. <span data-ttu-id="5b76d-202">Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-202">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="5b76d-203">Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite elementą **Našumo sekimo formatas**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-203">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="5b76d-204">Veiksmų srityje pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-204">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="5b76d-205">Atkreipkite dėmesį, kad sugeneruotame faile pateikiama informacijos apie 265 šešių tiekėjų operacijas.</span><span class="sxs-lookup"><span data-stu-id="5b76d-205">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="5b76d-206">Vykdymo sekimo peržiūra</span><span class="sxs-lookup"><span data-stu-id="5b76d-206">Review the execution trace</span></span>

### <a id='export-trace'></a><span data-ttu-id="5b76d-207">Sugeneruoto sekimo eksportavimas iš „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="5b76d-207">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="5b76d-208">Našumo sekimai atsiejami nuo šaltinio ER formato ir gali būti išdėstyti eilutėmis išoriniame ZIP faile.</span><span class="sxs-lookup"><span data-stu-id="5b76d-208">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="5b76d-209">„Finance and Operations“ eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos derinimo žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-209">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="5b76d-210">Puslapio **Elektroninių ataskaitų vykdymo žurnalai** kairiosios srities lauke **Konfigūracijos pavadinimas** pasirinkite **Našumo sekimo formatą**, kad rastumėte žurnalo įrašus, sugeneruotus vykdant konfigūraciją **Našumo sekimo formatas**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-210">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="5b76d-211">Paspauskite viršutiniame dešiniajame puslapio kampe esantį mygtuką (sąvaržėlės simbolis) **Priedai** arba paspauskite **Ctrl+Shift+A**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-211">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![„Finance and Operations“ puslapio Elektroninių ataskaitų vykdymo žurnalai mygtukas Priedai](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="5b76d-213">Norėdami gauti našumo sekimą kaip ZIP failą ir saugoti jį vietoje, puslapio **Elektroninių ataskaitų vykdymo žurnalų priedai** veiksmų srityje pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-213">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![„Finance and Operations“ puslapio Elektroninių ataskaitų vykdymo žurnalai priedai](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="5b76d-215">Sugeneruotame sekime yra nuoroda į šaltinio ER ataskaitą naudojant unikalų ataskaitos identifikatorių tik **GUID** formatu.</span><span class="sxs-lookup"><span data-stu-id="5b76d-215">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="5b76d-216">Į formato versijos numeravimą neatsižvelgiama.</span><span class="sxs-lookup"><span data-stu-id="5b76d-216">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="5b76d-217">Atkreipkite dėmesį, kad ryšys tarp įvykdyto ER formatui sugeneruoto našumo sekimo ir ER modelio susiejimo paremtas naudotu šakniniu aprašu ir bendru duomenų modeliu.</span><span class="sxs-lookup"><span data-stu-id="5b76d-217">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="5b76d-218">Į formato ir modelio susiejimo versijos numeravimą neatsižvelgiama.</span><span class="sxs-lookup"><span data-stu-id="5b76d-218">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="5b76d-219">Taip pat neatsižvelgiama į modelio susiejimo žymę **Numatytasis modelių susiejimui**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-219">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a id='import-trace'></a><span data-ttu-id="5b76d-220">Sugeneruoto sekimo importavimas į RCS</span><span class="sxs-lookup"><span data-stu-id="5b76d-220">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="5b76d-221">RCS darbo srityje **Elektroninės ataskaitos** pasirinkite plytelę **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-221">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="5b76d-222">Puslapio **Konfigūracijos** konfigūracijų medyje išplėskite elementą **Našumo sekimo modelis** ir pasirinkite elementą **Našumo sekimo formatas**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-222">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="5b76d-223">Veiksmų srityje pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-223">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="5b76d-224">Puslapio **Formato dizaino įrankis** veiksmų srityje pasirinkite **Našumo sekimas**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-224">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="5b76d-225">Dialogo lange **Našumo sekimo rezultato parametrai** pasirinkite **Importuoti našumo sekimą**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-225">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="5b76d-226">Paspaudę **Naršyti** pasirinkite anksčiau iš „Finance and Operations“ eksportuotą ZIP failą.</span><span class="sxs-lookup"><span data-stu-id="5b76d-226">Select **Browse** to select the zip file that you exported from Finance and Operations earlier.</span></span>
7. <span data-ttu-id="5b76d-227">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-227">Select **OK**.</span></span>

    ![Našumo sekimo rezultato parametrų dialogo langas, esantis RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="5b76d-229">Našumo sekimo naudojimas analizei naudojantis RCS – Formato vykdymas</span><span class="sxs-lookup"><span data-stu-id="5b76d-229">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="5b76d-230">RCS puslapyje **Formato dizaino įrankis** pasirinkę **Išplėsti / sutraukti** išplėskite visų formato elementų turinį.</span><span class="sxs-lookup"><span data-stu-id="5b76d-230">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="5b76d-231">Atkreipkite dėmesį, kad rodoma papildomos informacijos apie kai kuriuos dabartinio formato elementus.</span><span class="sxs-lookup"><span data-stu-id="5b76d-231">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="5b76d-232">Faktinis laikas, sugaištas įvedant duomenis į sugeneruotą išvestį naudojant formato elementą</span><span class="sxs-lookup"><span data-stu-id="5b76d-232">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="5b76d-233">Tas pats laikas išreikštas kaip viso laiko, praleisto generuojant visą išvestį, procentinė dalis</span><span class="sxs-lookup"><span data-stu-id="5b76d-233">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![RCS formato dizaino įrankio puslapis](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="5b76d-235">Uždarykite puslapį **Formato dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-235">Close **Format designer** page.</span></span>

### <a id='use-trace'></a><span data-ttu-id="5b76d-236">Našumo sekimo naudojimas analizei naudojantis RCS – Modelio susiejimas</span><span class="sxs-lookup"><span data-stu-id="5b76d-236">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="5b76d-237">RCS puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite elementą **Našumo sekimo susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-237">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="5b76d-238">Veiksmų srityje pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-238">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="5b76d-239">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-239">Select **Designer**.</span></span>
4. <span data-ttu-id="5b76d-240">Puslapio **Modelio susiejimo dizaino įrankis** veiksmų srityje pasirinkite **Našumo sekimas**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-240">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="5b76d-241">Pasirinkite anksčiau importuotą sekimą.</span><span class="sxs-lookup"><span data-stu-id="5b76d-241">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="5b76d-242">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-242">Select **OK**.</span></span>

<span data-ttu-id="5b76d-243">Atkreipkite dėmesį, kad atsiranda naujos informacijos apie kai kuriuos dabartinio modelio susiejimo duomenų šaltinio elementus.</span><span class="sxs-lookup"><span data-stu-id="5b76d-243">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="5b76d-244">Faktinis laikas, sugaištas gaunant duomenis naudojant duomenų šaltinį</span><span class="sxs-lookup"><span data-stu-id="5b76d-244">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="5b76d-245">Tas pats laikas, išreikštas kaip viso laiko, praleisto vykdant visą modelio susiejimą, procentinė dalis</span><span class="sxs-lookup"><span data-stu-id="5b76d-245">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="5b76d-246">Atkreipkite dėmesį, kad ER informuoja tuo atveju, kai dabartinis modelio susiejimas sutampa su duomenų bazės užklausomis, kai paleistas duomenų šaltinis VendTable/\<Relations/VendTrans.VendTable\_AccountNum.</span><span class="sxs-lookup"><span data-stu-id="5b76d-246">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="5b76d-247">Šis pasikartojimas įvyksta todėl, kad kiekvieno pasikartojančio tiekėjo įrašo atveju tiekėjo operacijų sąrašas iškviečiamas du kartus.</span><span class="sxs-lookup"><span data-stu-id="5b76d-247">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="5b76d-248">Vienas iškvietimas atliekamas norint į duomenų modelį įvesti informaciją apie kiekvieną operaciją pagal sukonfigūruotus susiejimus.</span><span class="sxs-lookup"><span data-stu-id="5b76d-248">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="5b76d-249">Vienas iškvietimas atliekamas norint įvesti apskaičiuotą kiekvieno duomenų modelio tiekėjo operacijų skaičių.</span><span class="sxs-lookup"><span data-stu-id="5b76d-249">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![Pranešimas apie pasikartojančias RCS puslapio Modelio susiejimo dizaino įrankis duomenų bazės užklausas](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="5b76d-251">Reikšmė **\[q:530\]** nurodo, kad lentelė VendTrans buvo iškviesta 530 kartų, kad į duomenų šaltinį VendTable/\<Relations/VendTrans.VendTable\_AccountNum būtų pateiktas tos lentelės įrašas.</span><span class="sxs-lookup"><span data-stu-id="5b76d-251">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="5b76d-252">Reikšmė **\[530\]** nurodo, kad duomenų šaltinis VendTable/\<Relations/VendTrans.VendTable\_AccountNum buvo iškviestas 530 kartus, kad būtų pateiktas to duomenų šaltinio įrašas ir duomenų modelyje būtų įvesta jo informacija.</span><span class="sxs-lookup"><span data-stu-id="5b76d-252">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="5b76d-253">Rekomenduojame naudoti duomenų šaltiniui VendTable/\<Relations/VendTrans.VendTable\_AccountNum skirtą talpyklą, kad sumažėtų siekiant gauti informacijos apie 265 operacijas atliktų iškvietimų skaičius ir pagerėtų modelio susiejimo našumas.</span><span class="sxs-lookup"><span data-stu-id="5b76d-253">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="5b76d-254">Taip pat gali būti naudinga sumažinti į duomenų šaltinį LedgerTransTypeList atliktų iškvietimų skaičių.</span><span class="sxs-lookup"><span data-stu-id="5b76d-254">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="5b76d-255">Šis duomenų šaltinis naudojamas norint susieti kiekvieną išvardijimo **LedgerTransType** reikšmę su jos žyme.</span><span class="sxs-lookup"><span data-stu-id="5b76d-255">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="5b76d-256">Naudodami šį duomenų šaltinį, galite rasti atitinkamą žymę ir įvesti ją kiekvieno tiekėjo operacijos duomenų modelyje.</span><span class="sxs-lookup"><span data-stu-id="5b76d-256">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="5b76d-257">Dabartinis iškvietimų į šį duomenų šaltinį skaičius (9027) gana didelis, turint omenyje, kad apdorojamos 265 operacijos.</span><span class="sxs-lookup"><span data-stu-id="5b76d-257">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![RCS puslapis Modelio susiejimo dizaino įrankis, kuriame rodomi 9027 iškvietimai į duomenų šaltinį](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="5b76d-259">Patobulinkite modelio susiejimą pagal iš vykdymo sekimo gautą informacija</span><span class="sxs-lookup"><span data-stu-id="5b76d-259">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="5b76d-260">Modelio susiejimo logikos keitimas</span><span class="sxs-lookup"><span data-stu-id="5b76d-260">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="5b76d-261">Atlikite toliau nurodytus veiksmus, kad būtų kaupiama talpykloje ir išvengiama pasikartojančių iškvietimų į duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="5b76d-261">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="5b76d-262">RCS puslapio **Modelio susiejimo dizaino įrankis** srityje **Duomenų šaltiniai** pasirinkite elementą **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-262">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="5b76d-263">Pasirinkite **Talpykla**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-263">Select **Cache**.</span></span>
    3. <span data-ttu-id="5b76d-264">Išplėskite elementą **VendTable**, išplėskite duomenų šaltinio VendTable ryšių „vienas su daugeliu“ sąrašą (elementas **\<Ryšiai**) ir pasirinkite elementą **VendTrans.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-264">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="5b76d-265">Pasirinkite **Talpykla**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-265">Select **Cache**.</span></span>

    ![Kaupimo talpykloje nustatymas, kad būtų išvengta pasikartojančių iškvietimų](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="5b76d-267">Atlikite toliau nurodytus veiksmus, norėdami, kad duomenų šaltinis LedgerTransTypeList patektų į duomenų šaltinio VendTable sritį.</span><span class="sxs-lookup"><span data-stu-id="5b76d-267">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="5b76d-268">Srityje **Duomenų šaltinio tipai** išplėskite elementą **Funkcijos** ir pasirinkite elementą **Apskaičiuotasis laukas**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-268">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="5b76d-269">Srityje **Duomenų šaltiniai** pasirinkite elementą **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-269">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="5b76d-270">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-270">Select **Add**.</span></span>
    4. <span data-ttu-id="5b76d-271">Lauke **Pavadinimas** įveskite **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-271">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="5b76d-272">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-272">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="5b76d-273">Lauke **Formulė** įveskite **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-273">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="5b76d-274">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-274">Select **Save**.</span></span>
    8. <span data-ttu-id="5b76d-275">Uždarykite puslapį **Formulės rengyklė**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-275">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="5b76d-276">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-276">Click **OK**.</span></span>

3. <span data-ttu-id="5b76d-277">Atlikę toliau nurodytus veiksmus atlikite lauko **\$TransType** talpyklinius mainus.</span><span class="sxs-lookup"><span data-stu-id="5b76d-277">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="5b76d-278">Pasirinkite elementą **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-278">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="5b76d-279">Pasirinkite **Talpykla**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-279">Select **Cache**.</span></span>
    3. <span data-ttu-id="5b76d-280">Pasirinkite elementą **VendTable.\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-280">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="5b76d-281">Pasirinkite **Talpykla**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-281">Select **Cache**.</span></span>

    ![Lauko $TransType kaupimo talpykloje sąranka](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="5b76d-283">Atlikę toliau nurodytus veiksmus pakeiskite lauką **\$TransTypeRecord**, kad jis galėtų naudoti talpykloje esantį lauką **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-283">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="5b76d-284">Srityje **Duomenų šaltiniai** išplėskite elementą **VendTable**, išplėskite elementą **\<Ryšiai**, išplėskite elementą **VendTrans.VendTable\_AccountNum** ir pasirinkite elementą **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-284">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="5b76d-285">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-285">Select **Edit**.</span></span>
    3. <span data-ttu-id="5b76d-286">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-286">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="5b76d-287">Lauke **Formulė** suraskite toliau nurodytą išraišką.</span><span class="sxs-lookup"><span data-stu-id="5b76d-287">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="5b76d-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="5b76d-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="5b76d-289">Lauke **Formulė** įveskite toliau nurodytą išraišką.</span><span class="sxs-lookup"><span data-stu-id="5b76d-289">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="5b76d-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="5b76d-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="5b76d-291">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-291">Select **Save**.</span></span>
    7. <span data-ttu-id="5b76d-292">Uždarykite puslapį **Formulės rengyklė**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-292">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="5b76d-293">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-293">Select **OK**.</span></span>

5. <span data-ttu-id="5b76d-294">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-294">Select **Save**.</span></span>
6. <span data-ttu-id="5b76d-295">Uždarykite puslapį **Modelio susiejimo dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-295">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="5b76d-296">Uždarykite puslapį **Modelio susiejimai**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-296">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="5b76d-297">Modifikuotos ER modelio susiejimo versijos užbaigimas</span><span class="sxs-lookup"><span data-stu-id="5b76d-297">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="5b76d-298">RCS puslapio **Konfigūracijos** „FastTab“ **Versijos** pasirinkite konfigūracijos **Našumo sekimo susiejimas** versiją **1.2**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-298">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="5b76d-299">Pasirinkti **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-299">Select **Change status**.</span></span>
3. <span data-ttu-id="5b76d-300">Pasirinkite **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-300">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-finance-and-operations"></a><span data-ttu-id="5b76d-301">Modifikuotos ER modelio susiejimo konfigūracijos importavimas iš RCS į „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="5b76d-301">Import the modified ER model mapping configuration from RCS into Finance and Operations</span></span>

<span data-ttu-id="5b76d-302">Pakartokite veiksmus, aprašytus ankstesniame šios temos skyriuje [ER konfigūracijos importavimas iš RCS į „Finance and Operations“](#import-configuration) ir importuokite konfigūracijos **Našumo sekimo susiejimas** versiją 1.2 į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="5b76d-302">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration into Finance and Operations.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="5b76d-303">Modifikuoto ER vykdymo sekimo sprendimo vykdymas</span><span class="sxs-lookup"><span data-stu-id="5b76d-303">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="5b76d-304">ER formato vykdymas</span><span class="sxs-lookup"><span data-stu-id="5b76d-304">Run the ER format</span></span>

<span data-ttu-id="5b76d-305">Pakartoję ankstesniame šios temos skyriuje [ER formato vykdymas](#run-format) nurodytus veiksmus sugeneruokite naują našumo sekimą.</span><span class="sxs-lookup"><span data-stu-id="5b76d-305">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="5b76d-306">Vykdymo sekimo peržiūra</span><span class="sxs-lookup"><span data-stu-id="5b76d-306">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-finance-and-operations"></a><span data-ttu-id="5b76d-307">Sugeneruoto sekimo eksportavimas iš „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="5b76d-307">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="5b76d-308">Pakartoję ankstesniame šios temos skyriuje [Sugeneruoto sekimo eksportavimas iš „Finance and Operations“](#export-trace) nurodytus veiksmus vietiniame tinkle įrašykite naują našumo sekimą.</span><span class="sxs-lookup"><span data-stu-id="5b76d-308">Repeat the steps in the [Export the generated trace from Finance and Operations](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="5b76d-309">Sugeneruoto sekimo importavimas į RCS</span><span class="sxs-lookup"><span data-stu-id="5b76d-309">Import the generated trace into RCS</span></span>

<span data-ttu-id="5b76d-310">Pakartoję ankstesniame šios temos skyriuje [Sugeneruoto sekimo importavimas į RCS](#import-trace) nurodytus veiksmus importuokite naują našumo sekimą į RCS.</span><span class="sxs-lookup"><span data-stu-id="5b76d-310">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="5b76d-311">Našumo sekimo naudojimas analizei naudojantis RCS – Modelio susiejimas</span><span class="sxs-lookup"><span data-stu-id="5b76d-311">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="5b76d-312">Pakartoję ankstesniame šios temos skyriuje [Našumo sekimo naudojimas analizei naudojantis RCS – Modelio susiejimas](#use-trace) nurodytus veiksmus išanalizuokite naujausią našumo sekimą.</span><span class="sxs-lookup"><span data-stu-id="5b76d-312">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="5b76d-313">Atkreipkite dėmesį, kad atlikus modelio susiejimo pakeitimus, nebeliko pasikartojančių užklausų į duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="5b76d-313">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="5b76d-314">Taip pat sumažėjo šio modelio susiejimo iškvietimų į duomenų bazės lenteles ir duomenų šaltinius skaičius.</span><span class="sxs-lookup"><span data-stu-id="5b76d-314">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="5b76d-315">Todėl pagerėjo viso ER sprendimo našumas.</span><span class="sxs-lookup"><span data-stu-id="5b76d-315">Therefore, the performance of the whole ER solution has improved.</span></span>

![RCS puslapio modelio susiejimo dizaino įrankio duomenų šaltinio VendTable informacijos sekimas](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="5b76d-317">Sekimo informacijoje duomenų šaltinio VendTable reikšmė **\[12\]** nurodo, kad šis duomenų šaltinis buvo iškviestas 12 kartų.</span><span class="sxs-lookup"><span data-stu-id="5b76d-317">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="5b76d-318">Reikšmė **\[Q:6\]** nurodo, kad šeši iškvietimai paversti duomenų bazės iškvietimais lentelėje VendTable.</span><span class="sxs-lookup"><span data-stu-id="5b76d-318">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="5b76d-319">Reikšmė **\[C:6\]** nurodo, kad iš duomenų bazės surinkti įrašai buvo įrašyti į talpyklą, o šeši kiti iškvietimai apdoroti naudojant talpyklą.</span><span class="sxs-lookup"><span data-stu-id="5b76d-319">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="5b76d-320">Atkreipkite dėmesį, kad iškvietimų į duomenų šaltinį LedgerTransTypeList skaičius sumažėjo nuo 9027 iki 240.</span><span class="sxs-lookup"><span data-stu-id="5b76d-320">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![RCS puslapio modelio susiejimo dizaino įrankio duomenų šaltinio LedgerTransTypeList informacijos sekimas](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-finance-and-operations"></a><span data-ttu-id="5b76d-322">Vykdymo sekimo peržiūra naudojant „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="5b76d-322">Review the execution trace in Finance and Operations</span></span>

<span data-ttu-id="5b76d-323">Galimybė naudotis ER sistemos dizaino įrankiu gali būti siūloma ne tik RCS, bet ir kai kuriose „Finance and Operations“ versijose.</span><span class="sxs-lookup"><span data-stu-id="5b76d-323">In addition to RCS, some versions of Finance and Operations might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="5b76d-324">Šiose „Finance and Operations“ versijose galima įjungti parinktį **Kūrimo režimo įjungimas**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-324">These versions of Finance and Operations have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="5b76d-325">Šią pasirinktį galite rasti puslapio **Elektroninių ataskaitų parametrai**, kurį galite atidaryti darbo srityje **Elektroninės ataskaitos**, skirtuke **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-325">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Dizaino režimo parinkties įgalinimas „Finance and Operations“ puslapyje Elektroninių ataskaitų parametrai](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="5b76d-327">Jei naudojatės viena iš šių „Finance and Operations“ versijų, sugeneruotų našumo sekimų informaciją galite analizuoti tiesiogiai naudodamiesi „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="5b76d-327">If you use one of these versions of Finance and Operations, you can analyze the details of generated performance traces directly in Finance and Operations.</span></span> <span data-ttu-id="5b76d-328">Nereikia eksportuoti informacijos iš „Finance and Operation“ ir importuoti ją į RCS.</span><span class="sxs-lookup"><span data-stu-id="5b76d-328">You don't have to export them from Finance and Operation and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="5b76d-329">Vykdymo sekimo peržiūra naudojantis išoriniais įrankiais</span><span class="sxs-lookup"><span data-stu-id="5b76d-329">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="5b76d-330">Vartotojo parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="5b76d-330">Configure user parameters</span></span>

1. <span data-ttu-id="5b76d-331">„Finance and Operations“ eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-331">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="5b76d-332">Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-332">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="5b76d-333">Dialogo lango **Vartotojo parametrai** skyriaus **Vykdymo sekimas** lauke **Vykdymo sekimo formatas** pasirinkite **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="5b76d-333">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="5b76d-334">ER formato vykdymas</span><span class="sxs-lookup"><span data-stu-id="5b76d-334">Run the ER format</span></span>

<span data-ttu-id="5b76d-335">Pakartoję ankstesniame šios temos skyriuje [ER formato vykdymas](#run-format) nurodytus veiksmus sugeneruokite naują našumo sekimą.</span><span class="sxs-lookup"><span data-stu-id="5b76d-335">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="5b76d-336">Atkreipkite dėmesį, kad interneto naršyklėje siūloma atsisiųsti ZIP failą.</span><span class="sxs-lookup"><span data-stu-id="5b76d-336">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="5b76d-337">Šiame faile pateikiamas našumo sekimas PerfView formatu.</span><span class="sxs-lookup"><span data-stu-id="5b76d-337">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="5b76d-338">Naudodamiesi PerfView našumo analizės įrankiu galite išanalizuoti informaciją apie ER formato vykdymą.</span><span class="sxs-lookup"><span data-stu-id="5b76d-338">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>
