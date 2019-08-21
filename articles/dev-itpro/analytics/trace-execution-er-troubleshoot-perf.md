---
title: ER formato vykdymo sekimas siekiant diagnozuoti našumo problemas
description: Šioje temoje pateikiama informacijos apie tai, kaip elektroninėse ataskaitose (ER) naudojantis našumo sekimo funkcija spręsti našumo problemas.
author: NickSelin
manager: AnnBe
ms.date: 06/12/2019
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
ms.openlocfilehash: 7ec16bea1e4f7685f95178f848ba7348a06c31f3
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741508"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="b33e2-103">ER formatų vykdymo sekimas siekiant diagnozuoti našumo problemas</span><span class="sxs-lookup"><span data-stu-id="b33e2-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b33e2-104">Kurdami elektroninių ataskaitų (ER) konfigūracijas, kuriomis naudojantis generuojami elektroniniai dokumentai, nurodote būdą, kuriuo naudodamiesi gaunate duomenis iš „Microsoft Dynamics 365 for Finance and Operations“, ir įvedate jį į sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="b33e2-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of Microsoft Dynamics 365 for Finance and Operations and enter it in the output that is generated.</span></span> <span data-ttu-id="b33e2-105">Naudojantis ER našumo sekimo funkcija gali pastebimai sutrumpėti laikas, per kurį renkama informacija apie ER formato vykdymą, panaudojant ją našumo problemoms spręsti, ir gali būti patiriama mažiau išlaidų.</span><span class="sxs-lookup"><span data-stu-id="b33e2-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="b33e2-106">Šioje mokymo programoje pateikiama rekomendacijų apie tai, kaip atsižvelgti į įvykdytų „Finance and Operations“ ER formatų našumo sekimus ir kaip panaudoti šiuos sekimus siekiant pagerinti našumą.</span><span class="sxs-lookup"><span data-stu-id="b33e2-106">This tutorial provides guidelines about how to take performance traces for executed ER formats in Finance and Operations, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b33e2-107">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="b33e2-107">Prerequisites</span></span>

<span data-ttu-id="b33e2-108">Norint įvykdyti šios mokymo programos pavyzdžių užduotis, reikia toliau nurodytų prieigų.</span><span class="sxs-lookup"><span data-stu-id="b33e2-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="b33e2-109">Prieiga prie „Finance and Operations“ naudojant vieną iš tolesnių vaidmenų.</span><span class="sxs-lookup"><span data-stu-id="b33e2-109">Access to Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="b33e2-110">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="b33e2-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="b33e2-111">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="b33e2-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="b33e2-112">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="b33e2-112">System administrator</span></span>

- <span data-ttu-id="b33e2-113">Prieiga prie „Regulatory Configuration Services“ (RCS) egzemplioriaus, kuris sukurtas tam pačiam nuomininkui, kaip „Finance and Operations“, vienam iš toliau nurodytų vaidmenų atlikti.</span><span class="sxs-lookup"><span data-stu-id="b33e2-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance and Operations, for one of the following roles:</span></span>

    - <span data-ttu-id="b33e2-114">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="b33e2-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="b33e2-115">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="b33e2-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="b33e2-116">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="b33e2-116">System administrator</span></span>

<span data-ttu-id="b33e2-117">Taip pat turite atsiųsti ir vietoje saugoti toliau nurodytus failus.</span><span class="sxs-lookup"><span data-stu-id="b33e2-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="b33e2-118">Failas</span><span class="sxs-lookup"><span data-stu-id="b33e2-118">File</span></span>                                  | <span data-ttu-id="b33e2-119">Turinys</span><span class="sxs-lookup"><span data-stu-id="b33e2-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="b33e2-120">Našumo sekimo modelis.versija.1</span><span class="sxs-lookup"><span data-stu-id="b33e2-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="b33e2-121">ER duomenų modelio konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="b33e2-121">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| <span data-ttu-id="b33e2-122">Našumo sekimo metaduomenys.versija.1</span><span class="sxs-lookup"><span data-stu-id="b33e2-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="b33e2-123">ER metaduomenų konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="b33e2-123">Sample ER metadata configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| <span data-ttu-id="b33e2-124">Našumo sekimo susiejimas.versija.1.1</span><span class="sxs-lookup"><span data-stu-id="b33e2-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="b33e2-125">ER modelio susiejimo konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="b33e2-125">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="b33e2-126">Našumo sekimo formatas.versija.1.1</span><span class="sxs-lookup"><span data-stu-id="b33e2-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="b33e2-127">ER formato konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="b33e2-127">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="b33e2-128">ER parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="b33e2-128">Configure ER parameters</span></span>

<span data-ttu-id="b33e2-129">Kiekvienas „Finance and Operations“ sugeneruotas ER našumo sekimas saugomas kaip vykdymo žurnalo įrašo priedas.</span><span class="sxs-lookup"><span data-stu-id="b33e2-129">Each ER performance trace that is generated in Finance and Operations is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="b33e2-130">Šiems priedams tvarkyti naudojama „Finance and Operations“ dokumentų tvarkymo (DM) sistema.</span><span class="sxs-lookup"><span data-stu-id="b33e2-130">The Document management (DM) framework of Finance and Operations is used to manage these attachments.</span></span> <span data-ttu-id="b33e2-131">Norėdami nurodyti DM dokumento tipą, kuris turėtų būti naudojamas našumo sekimams pridėti, turite iš anksto sukonfigūruoti ER parametrus.</span><span class="sxs-lookup"><span data-stu-id="b33e2-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="b33e2-132">„Finance and Operation“ darbo srityje **Elektroninės ataskaitos** pasirinkite **Elektroninių ataskaitų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-132">In Finance and Operation, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="b33e2-133">Tada puslapyje **Elektroninių ataskaitų parametrai** esančio skirtuko **Priedai** lauke **Kiti** pasirinkite DM dokumento tipą, kuris bus naudojamas našumo sekimui.</span><span class="sxs-lookup"><span data-stu-id="b33e2-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Elektroninių ataskaitų parametrų puslapis „Finance and Operations“](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="b33e2-135">Norint, kad DM dokumento tipu būtų galima naudotis peržvalgos lauke **Kiti**, jis turi būti atitinkamai sukonfigūruotas puslapyje **Dokumentų tipai** (**Organizacijos administravimas \> Dokumentų valdymas \> Dokumentų tipai**):</span><span class="sxs-lookup"><span data-stu-id="b33e2-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="b33e2-136">**Klasė:** pridėti failą</span><span class="sxs-lookup"><span data-stu-id="b33e2-136">**Class:** Attach file</span></span>
- <span data-ttu-id="b33e2-137">**Grupė:** failas</span><span class="sxs-lookup"><span data-stu-id="b33e2-137">**Group:** File</span></span>

![Dokumentų tipų puslapis „Finance and Operations“](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="b33e2-139">Pasirinktas dokumento tipas turi būti pasiekiamas visose dabartinio „Finance and Operations“ egzemplioriaus įmonėse, nes DM priedai skirti įmonei.</span><span class="sxs-lookup"><span data-stu-id="b33e2-139">The selected document type must be available in every company of the current Finance and Operations instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="b33e2-140">RCS parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="b33e2-140">Configure RCS parameters</span></span>

<span data-ttu-id="b33e2-141">„Finance and Operations“ sugeneruoti ER našumo sekimai importuojami į RCS analizei atlikti naudojant ER formato dizaino įrankį ir ER susiejimo dizaino įrankį.</span><span class="sxs-lookup"><span data-stu-id="b33e2-141">ER performance traces that are generated in Finance and Operations will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="b33e2-142">Kadangi ER našumo sekimai saugomi kaip su ER formatu susieto vykdymo žurnalo įrašo priedai, reikia iš anksto konfigūruoti RCS parametrus, kad būtų nurodytas DM dokumento tipas, kuris turėtų būti naudojamas našumo sekimams pridėti.</span><span class="sxs-lookup"><span data-stu-id="b33e2-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="b33e2-143">Jūsų įmonei sukurto RCS egzemplioriaus darbo srityje **Elektroninės ataskaitos** pasirinkite **Elektroninių ataskaitų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="b33e2-144">Tada puslapyje **Elektroninių ataskaitų parametrai** esančio skirtuko **Priedai** lauke **Kiti** pasirinkite DM dokumento tipą, kuris bus naudojamas našumo sekimui.</span><span class="sxs-lookup"><span data-stu-id="b33e2-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![RCS elektroninių ataskaitų parametrų puslapis](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="b33e2-146">Norint, kad DM dokumento tipu būtų galima naudotis peržvalgos lauke **Kiti**, jis turi būti atitinkamai sukonfigūruotas puslapyje **Dokumentų tipai** (**Organizacijos administravimas \> Dokumentų valdymas \> Dokumentų tipai**):</span><span class="sxs-lookup"><span data-stu-id="b33e2-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="b33e2-147">**Klasė:** pridėti failą</span><span class="sxs-lookup"><span data-stu-id="b33e2-147">**Class:** Attach file</span></span>
- <span data-ttu-id="b33e2-148">**Grupė:** failas</span><span class="sxs-lookup"><span data-stu-id="b33e2-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="b33e2-149">ER sprendimo kūrimas</span><span class="sxs-lookup"><span data-stu-id="b33e2-149">Design an ER solution</span></span>

<span data-ttu-id="b33e2-150">Tarkime, kad jau pradėjau kurti naują ER sprendimą, kad būtų sugeneruota nauja ataskaita, kurioje pateikiamos tiekėjo operacijos.</span><span class="sxs-lookup"><span data-stu-id="b33e2-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="b33e2-151">Šiuo metu pasirinkto tiekėjo operacijas rasite puslapyje **Tiekėjo operacijos** (eikite į **Mokėtina suma \> Tiekėjai \> Visi tiekėjai**, pasirinkite tiekėją, paskui veiksmų srities skirtuko **Tiekėjas** grupėje **Operacijos** pasirinkite **Operacijos**).</span><span class="sxs-lookup"><span data-stu-id="b33e2-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="b33e2-152">Tačiau norite vienu metu turėti visas tiekėjo operacijas viename elektroniniame dokumente XML formatu.</span><span class="sxs-lookup"><span data-stu-id="b33e2-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="b33e2-153">Šį sprendimą sudaro kelios ER konfigūracijos, apimančios reikiamą duomenų modelį, metaduomenis, modelio susiejimą ir formato komponentus.</span><span class="sxs-lookup"><span data-stu-id="b33e2-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="b33e2-154">Prisijunkite prie jūsų įmonei sukurto RCS egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="b33e2-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="b33e2-155">Šioje mokymo programoje kursite ir modifikuosite pavyzdinės įmonės **„Litware, Inc.“** konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="b33e2-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="b33e2-156">Todėl įsitikinkite, kad šis konfigūracijos teikėjas buvo pridėtas prie RCS ir pasirinktas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="b33e2-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="b33e2-157">Instrukcijos aprašytos procedūroje [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="b33e2-157">For instructions, see the [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) procedure.</span></span>
3. <span data-ttu-id="b33e2-158">Darbo srityje **Elektroninės ataskaitos** pasirinkite plytelę **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="b33e2-159">Puslapyje **Konfigūracijos** importuokite į RCS kaip būtinąjį komponentą atsisiųstas ER konfigūracijas tokia tvarka: duomenų modelis, metaduomenys, modelio susiejimas, formatas.</span><span class="sxs-lookup"><span data-stu-id="b33e2-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="b33e2-160">Kurdami kiekvieną konfigūraciją atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b33e2-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="b33e2-161">Veiksmų srityje pasirinkite **Keitimas \> Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="b33e2-162">Paspaudę **Naršyti** pasirinkite reikiamą ER konfigūracijos failą XML formatu.</span><span class="sxs-lookup"><span data-stu-id="b33e2-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="b33e2-163">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-163">Select **OK**.</span></span>

    ![RCS puslapis Konfigūracijos](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="b33e2-165">ER vykdymo sekimo sprendimo vykdymas</span><span class="sxs-lookup"><span data-stu-id="b33e2-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="b33e2-166">Tarkime, kad baigėte kurti pirmąją ER sprendimo versiją.</span><span class="sxs-lookup"><span data-stu-id="b33e2-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="b33e2-167">Dabar norite ją patikrinti naudodami savo „Finance and Operations“ egzempliorių ir išanalizuoti vykdymo našumą.</span><span class="sxs-lookup"><span data-stu-id="b33e2-167">You now want to test it in your Finance and Operations instance and analyze execution performance.</span></span>

### <a id='import-configuration'></a><span data-ttu-id="b33e2-168">ER konfigūracijos importavimas iš RCS į „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="b33e2-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="b33e2-169">Prisijunkite prie savo „Finance and Operations“ egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="b33e2-169">Sign in to your Finance and Operations instance.</span></span>
2. <span data-ttu-id="b33e2-170">Dirbdami su šia mokymo programa, konfigūracijas importuosite iš savo RCS egzemplioriaus (kuriame kuriate savo ER komponentus) į savo „Finance and Operations“ egzempliorių (kuriame jas tikrinate ir galiausiai naudojate).</span><span class="sxs-lookup"><span data-stu-id="b33e2-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your Finance and Operations instance (where you test and finally use them).</span></span> <span data-ttu-id="b33e2-171">Todėl turite įsitikinti, kad paruošti visi reikiami artefaktai.</span><span class="sxs-lookup"><span data-stu-id="b33e2-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="b33e2-172">Instrukcijas rasite procedūroje [Elektroninių ataskaitų (ER) konfigūracijų importavimas iš „Regulatory Configuration Services“ (RCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations).</span><span class="sxs-lookup"><span data-stu-id="b33e2-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations) procedure.</span></span>
3. <span data-ttu-id="b33e2-173">Atlikę toliau nurodytus veiksmus importuokite konfigūracijas iš RCS į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="b33e2-173">Follow these steps to import the configurations from RCS into Finance and Operations:</span></span>

    1. <span data-ttu-id="b33e2-174">Darbo srityje **Elektroninės ataskaitos** konfigūracijos tiekėjui **„Litware, Inc.“** skirtoje plytelėje pasirinkite **Saugyklos**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="b33e2-175">Puslapyje **Konfigūracijų saugykla** pasirinkite tipo **RCS** saugyklą, paskui pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="b33e2-176">„FastTab“ **Konfigūracijos** pasirinkite konfigūraciją **Našumo sekimo formatas**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="b33e2-177">„FastTab“ **Versijos** pasirinkite pasirinktos ER konfigūracijos versiją **1.1**, paskui pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![„Finance and Operations“ konfigūracijų saugyklos puslapis](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="b33e2-179">Atitinkamų versijų duomenų modeliai ir modelio susiejimo konfigūracijos automatiškai importuojami kaip būtinieji importuotos ER formato konfigūracijos komponentai.</span><span class="sxs-lookup"><span data-stu-id="b33e2-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="b33e2-180">ER veiklos sekimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="b33e2-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="b33e2-181">„Finance and Operations“ eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-181">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="b33e2-182">Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="b33e2-183">Dialogo lango **Vartotojo parametrai** skyriuje **Vykdymo sekimas** atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b33e2-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="b33e2-184">Lauke **Vykdymo sekimo formatas** pasirinkite **Derinti sekimo formatą**, kad būtų galima rinkti informaciją apie ER formato vykdymą.</span><span class="sxs-lookup"><span data-stu-id="b33e2-184">In the **Execution trace format** field, select **Debug trace format** to start to collect the details of ER format execution.</span></span> <span data-ttu-id="b33e2-185">Pasirinkus šią reikšmę, našumo sekimas renka informaciją apie laiką, sugaištą toliau nurodytiems veiksmams atlikti.</span><span class="sxs-lookup"><span data-stu-id="b33e2-185">When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</span></span>

        - <span data-ttu-id="b33e2-186">Kiekvieno duomenims gauti iškviesto modelio susiejimo duomenų šaltinio vykdymas</span><span class="sxs-lookup"><span data-stu-id="b33e2-186">Running each data source in the model mapping that is called to get data</span></span>
        - <span data-ttu-id="b33e2-187">Kiekvieno formato elemento apdorojimas įvedant duomenis į sugeneruotą išvestį</span><span class="sxs-lookup"><span data-stu-id="b33e2-187">Processing each format item to enter data in the output that is generated</span></span>

        <span data-ttu-id="b33e2-188">Laukas **Vykdymo sekimo formatas** naudojamas norint nurodyti sugeneruoto našumo sekimo formatą, kurio vykdymo informacija saugoma, kad būtų galima nustatyti ER formatą ir susiejimo elementus.</span><span class="sxs-lookup"><span data-stu-id="b33e2-188">You use the **Execution trace format** field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</span></span> <span data-ttu-id="b33e2-189">Kaip reikšmę pasirinkę **Derinti sekimo formatą** galėsite analizuoti sekimo turinį naudodami ER operacijų dizaino įrankį ir peržiūrėti sekime minimus ER formato arba siejimo elementus.</span><span class="sxs-lookup"><span data-stu-id="b33e2-189">By selecting **Debug trace format** as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</span></span>

    2. <span data-ttu-id="b33e2-190">Nustatykite tolesnių parinkčių reikšmes **Taip**, kad būtų galima rinkti konkrečią informaciją apie ER modelio susiejimo vykdymą ir ER formato komponentus.</span><span class="sxs-lookup"><span data-stu-id="b33e2-190">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="b33e2-191">**Rinkti užklausų statistiką** – įjungus šią parinktį, našumo sekimas renka toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="b33e2-191">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="b33e2-192">Duomenų šaltinių atliktų duomenų bazės iškvietimų skaičius</span><span class="sxs-lookup"><span data-stu-id="b33e2-192">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="b33e2-193">Pasikartojančių iškvietimų į duomenų bazę skaičius</span><span class="sxs-lookup"><span data-stu-id="b33e2-193">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="b33e2-194">Informacija apie duomenų bazės iškvietimams atlikti naudotus SQL išrašus</span><span class="sxs-lookup"><span data-stu-id="b33e2-194">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="b33e2-195">**Talpyklos sekimo prieiga** – įjungus šią parinktį, našumo sekimas renka informaciją apie ER modelio susiejimo talpyklos naudojimą.</span><span class="sxs-lookup"><span data-stu-id="b33e2-195">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="b33e2-196">**Sekimo duomenų prieiga** – įjungus šią parinktį, našumo sekimas renka informaciją apie iškvietimų į įvykdytų įrašo sąrašo tipo duomenų šaltinių duomenų bazę skaičių.</span><span class="sxs-lookup"><span data-stu-id="b33e2-196">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="b33e2-197">**Sekimų sąrašo išvardijimas** – įjungus šią parinktį, našumo sekimas renka informaciją apie iš įrašo sąrašo tipo duomenų šaltinių pageidaujamų įrašų skaičių.</span><span class="sxs-lookup"><span data-stu-id="b33e2-197">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b33e2-198">Dialogo lange **Vartotojo parametrai** nurodyti vartotojo ir dabartinės įmonės parametrai.</span><span class="sxs-lookup"><span data-stu-id="b33e2-198">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![„Finance and Operations“ vartotojo parametrų dialogo langas](./media/GER-PerfTrace-GER-UserParameters.png)

### <a id='run-format'></a><span data-ttu-id="b33e2-200">ER formato vykdymas</span><span class="sxs-lookup"><span data-stu-id="b33e2-200">Run the ER format</span></span>

1. <span data-ttu-id="b33e2-201">„Finance and Operations“ pasirinkite įmonę **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-201">In Finance and Operations, select the **DEMF** company.</span></span>
2. <span data-ttu-id="b33e2-202">Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-202">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="b33e2-203">Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite elementą **Našumo sekimo formatas**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-203">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="b33e2-204">Veiksmų srityje pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-204">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="b33e2-205">Atkreipkite dėmesį, kad sugeneruotame faile pateikiama informacijos apie 265 šešių tiekėjų operacijas.</span><span class="sxs-lookup"><span data-stu-id="b33e2-205">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="b33e2-206">Vykdymo sekimo peržiūra</span><span class="sxs-lookup"><span data-stu-id="b33e2-206">Review the execution trace</span></span>

### <a id='export-trace'></a><span data-ttu-id="b33e2-207">Sugeneruoto sekimo eksportavimas iš „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="b33e2-207">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="b33e2-208">Našumo sekimai atsiejami nuo šaltinio ER formato ir gali būti išdėstyti eilutėmis išoriniame ZIP faile.</span><span class="sxs-lookup"><span data-stu-id="b33e2-208">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="b33e2-209">„Finance and Operations“ eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos derinimo žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-209">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="b33e2-210">Puslapio **Elektroninių ataskaitų vykdymo žurnalai** kairiosios srities lauke **Konfigūracijos pavadinimas** pasirinkite **Našumo sekimo formatą**, kad rastumėte žurnalo įrašus, sugeneruotus vykdant konfigūraciją **Našumo sekimo formatas**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-210">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="b33e2-211">Paspauskite viršutiniame dešiniajame puslapio kampe esantį mygtuką (sąvaržėlės simbolis) **Priedai** arba paspauskite **Ctrl+Shift+A**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-211">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![„Finance and Operations“ puslapio Elektroninių ataskaitų vykdymo žurnalai mygtukas Priedai](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="b33e2-213">Norėdami gauti našumo sekimą kaip ZIP failą ir saugoti jį vietoje, puslapio **Elektroninių ataskaitų vykdymo žurnalų priedai** veiksmų srityje pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-213">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![„Finance and Operations“ puslapio Elektroninių ataskaitų vykdymo žurnalai priedai](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="b33e2-215">Sugeneruotame sekime yra nuoroda į šaltinio ER ataskaitą naudojant unikalų ataskaitos identifikatorių tik **GUID** formatu.</span><span class="sxs-lookup"><span data-stu-id="b33e2-215">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="b33e2-216">Į formato versijos numeravimą neatsižvelgiama.</span><span class="sxs-lookup"><span data-stu-id="b33e2-216">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="b33e2-217">Atkreipkite dėmesį, kad ryšys tarp įvykdyto ER formatui sugeneruoto našumo sekimo ir ER modelio susiejimo paremtas naudotu šakniniu aprašu ir bendru duomenų modeliu.</span><span class="sxs-lookup"><span data-stu-id="b33e2-217">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="b33e2-218">Į formato ir modelio susiejimo versijos numeravimą neatsižvelgiama.</span><span class="sxs-lookup"><span data-stu-id="b33e2-218">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="b33e2-219">Taip pat neatsižvelgiama į modelio susiejimo žymę **Numatytasis modelių susiejimui**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-219">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a id='import-trace'></a><span data-ttu-id="b33e2-220">Sugeneruoto sekimo importavimas į RCS</span><span class="sxs-lookup"><span data-stu-id="b33e2-220">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="b33e2-221">RCS darbo srityje **Elektroninės ataskaitos** pasirinkite plytelę **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-221">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="b33e2-222">Puslapio **Konfigūracijos** konfigūracijų medyje išplėskite elementą **Našumo sekimo modelis** ir pasirinkite elementą **Našumo sekimo formatas**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-222">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="b33e2-223">Veiksmų srityje pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-223">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="b33e2-224">Puslapio **Formato dizaino įrankis** veiksmų srityje pasirinkite **Našumo sekimas**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-224">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="b33e2-225">Dialogo lange **Našumo sekimo rezultato parametrai** pasirinkite **Importuoti našumo sekimą**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-225">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="b33e2-226">Paspaudę **Naršyti** pasirinkite anksčiau iš „Finance and Operations“ eksportuotą ZIP failą.</span><span class="sxs-lookup"><span data-stu-id="b33e2-226">Select **Browse** to select the zip file that you exported from Finance and Operations earlier.</span></span>
7. <span data-ttu-id="b33e2-227">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-227">Select **OK**.</span></span>

    ![Našumo sekimo rezultato parametrų dialogo langas, esantis RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="b33e2-229">Našumo sekimo naudojimas analizei naudojantis RCS – Formato vykdymas</span><span class="sxs-lookup"><span data-stu-id="b33e2-229">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="b33e2-230">RCS puslapyje **Formato dizaino įrankis** pasirinkę **Išplėsti / sutraukti** išplėskite visų formato elementų turinį.</span><span class="sxs-lookup"><span data-stu-id="b33e2-230">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="b33e2-231">Atkreipkite dėmesį, kad rodoma papildomos informacijos apie kai kuriuos dabartinio formato elementus.</span><span class="sxs-lookup"><span data-stu-id="b33e2-231">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="b33e2-232">Faktinis laikas, sugaištas įvedant duomenis į sugeneruotą išvestį naudojant formato elementą</span><span class="sxs-lookup"><span data-stu-id="b33e2-232">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="b33e2-233">Tas pats laikas išreikštas kaip viso laiko, praleisto generuojant visą išvestį, procentinė dalis</span><span class="sxs-lookup"><span data-stu-id="b33e2-233">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![RCS formato dizaino įrankio puslapis](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="b33e2-235">Uždarykite puslapį **Formato dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-235">Close **Format designer** page.</span></span>

### <a id='use-trace'></a><span data-ttu-id="b33e2-236">Našumo sekimo naudojimas analizei naudojantis RCS – Modelio susiejimas</span><span class="sxs-lookup"><span data-stu-id="b33e2-236">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="b33e2-237">RCS puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite elementą **Našumo sekimo susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-237">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="b33e2-238">Veiksmų srityje pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-238">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="b33e2-239">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-239">Select **Designer**.</span></span>
4. <span data-ttu-id="b33e2-240">Puslapio **Modelio susiejimo dizaino įrankis** veiksmų srityje pasirinkite **Našumo sekimas**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-240">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="b33e2-241">Pasirinkite anksčiau importuotą sekimą.</span><span class="sxs-lookup"><span data-stu-id="b33e2-241">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="b33e2-242">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-242">Select **OK**.</span></span>

<span data-ttu-id="b33e2-243">Atkreipkite dėmesį, kad atsiranda naujos informacijos apie kai kuriuos dabartinio modelio susiejimo duomenų šaltinio elementus.</span><span class="sxs-lookup"><span data-stu-id="b33e2-243">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="b33e2-244">Faktinis laikas, sugaištas gaunant duomenis naudojant duomenų šaltinį</span><span class="sxs-lookup"><span data-stu-id="b33e2-244">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="b33e2-245">Tas pats laikas, išreikštas kaip viso laiko, praleisto vykdant visą modelio susiejimą, procentinė dalis</span><span class="sxs-lookup"><span data-stu-id="b33e2-245">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="b33e2-246">Atkreipkite dėmesį, kad ER informuoja tuo atveju, kai dabartinis modelio susiejimas sutampa su duomenų bazės užklausomis, kai paleistas duomenų šaltinis VendTable/\<Relations/VendTrans.VendTable\_AccountNum.</span><span class="sxs-lookup"><span data-stu-id="b33e2-246">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="b33e2-247">Šis pasikartojimas įvyksta todėl, kad kiekvieno pasikartojančio tiekėjo įrašo atveju tiekėjo operacijų sąrašas iškviečiamas du kartus.</span><span class="sxs-lookup"><span data-stu-id="b33e2-247">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="b33e2-248">Vienas iškvietimas atliekamas norint į duomenų modelį įvesti informaciją apie kiekvieną operaciją pagal sukonfigūruotus susiejimus.</span><span class="sxs-lookup"><span data-stu-id="b33e2-248">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="b33e2-249">Vienas iškvietimas atliekamas norint įvesti apskaičiuotą kiekvieno duomenų modelio tiekėjo operacijų skaičių.</span><span class="sxs-lookup"><span data-stu-id="b33e2-249">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![Pranešimas apie pasikartojančias RCS puslapio Modelio susiejimo dizaino įrankis duomenų bazės užklausas](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="b33e2-251">Reikšmė **\[q:530\]** nurodo, kad lentelė VendTrans buvo iškviesta 530 kartų, kad į duomenų šaltinį VendTable/\<Relations/VendTrans.VendTable\_AccountNum būtų pateiktas tos lentelės įrašas.</span><span class="sxs-lookup"><span data-stu-id="b33e2-251">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="b33e2-252">Reikšmė **\[530\]** nurodo, kad duomenų šaltinis VendTable/\<Relations/VendTrans.VendTable\_AccountNum buvo iškviestas 530 kartus, kad būtų pateiktas to duomenų šaltinio įrašas ir duomenų modelyje būtų įvesta jo informacija.</span><span class="sxs-lookup"><span data-stu-id="b33e2-252">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="b33e2-253">Rekomenduojame naudoti duomenų šaltiniui VendTable/\<Relations/VendTrans.VendTable\_AccountNum skirtą talpyklą, kad sumažėtų siekiant gauti informacijos apie 265 operacijas atliktų iškvietimų skaičius ir pagerėtų modelio susiejimo našumas.</span><span class="sxs-lookup"><span data-stu-id="b33e2-253">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="b33e2-254">Taip pat gali būti naudinga sumažinti į duomenų šaltinį LedgerTransTypeList atliktų iškvietimų skaičių.</span><span class="sxs-lookup"><span data-stu-id="b33e2-254">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="b33e2-255">Šis duomenų šaltinis naudojamas norint susieti kiekvieną išvardijimo **LedgerTransType** reikšmę su jos žyme.</span><span class="sxs-lookup"><span data-stu-id="b33e2-255">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="b33e2-256">Naudodami šį duomenų šaltinį, galite rasti atitinkamą žymę ir įvesti ją kiekvieno tiekėjo operacijos duomenų modelyje.</span><span class="sxs-lookup"><span data-stu-id="b33e2-256">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="b33e2-257">Dabartinis iškvietimų į šį duomenų šaltinį skaičius (9027) gana didelis, turint omenyje, kad apdorojamos 265 operacijos.</span><span class="sxs-lookup"><span data-stu-id="b33e2-257">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![RCS puslapis Modelio susiejimo dizaino įrankis, kuriame rodomi 9027 iškvietimai į duomenų šaltinį](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="b33e2-259">Patobulinkite modelio susiejimą pagal iš vykdymo sekimo gautą informacija</span><span class="sxs-lookup"><span data-stu-id="b33e2-259">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="b33e2-260">Modelio susiejimo logikos keitimas</span><span class="sxs-lookup"><span data-stu-id="b33e2-260">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="b33e2-261">Atlikite toliau nurodytus veiksmus, kad būtų kaupiama talpykloje ir išvengiama pasikartojančių iškvietimų į duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="b33e2-261">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="b33e2-262">RCS puslapio **Modelio susiejimo dizaino įrankis** srityje **Duomenų šaltiniai** pasirinkite elementą **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-262">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="b33e2-263">Pasirinkite **Talpykla**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-263">Select **Cache**.</span></span>
    3. <span data-ttu-id="b33e2-264">Išplėskite elementą **VendTable**, išplėskite duomenų šaltinio VendTable ryšių „vienas su daugeliu“ sąrašą (elementas **\<Ryšiai**) ir pasirinkite elementą **VendTrans.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-264">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="b33e2-265">Pasirinkite **Talpykla**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-265">Select **Cache**.</span></span>

    ![Kaupimo talpykloje nustatymas, kad būtų išvengta pasikartojančių iškvietimų](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="b33e2-267">Atlikite toliau nurodytus veiksmus, norėdami, kad duomenų šaltinis LedgerTransTypeList patektų į duomenų šaltinio VendTable sritį.</span><span class="sxs-lookup"><span data-stu-id="b33e2-267">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="b33e2-268">Srityje **Duomenų šaltinio tipai** išplėskite elementą **Funkcijos** ir pasirinkite elementą **Apskaičiuotasis laukas**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-268">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="b33e2-269">Srityje **Duomenų šaltiniai** pasirinkite elementą **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-269">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="b33e2-270">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-270">Select **Add**.</span></span>
    4. <span data-ttu-id="b33e2-271">Lauke **Pavadinimas** įveskite **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-271">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="b33e2-272">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-272">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="b33e2-273">Lauke **Formulė** įveskite **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-273">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="b33e2-274">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-274">Select **Save**.</span></span>
    8. <span data-ttu-id="b33e2-275">Uždarykite puslapį **Formulės rengyklė**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-275">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="b33e2-276">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-276">Click **OK**.</span></span>

3. <span data-ttu-id="b33e2-277">Atlikę toliau nurodytus veiksmus atlikite lauko **\$TransType** talpyklinius mainus.</span><span class="sxs-lookup"><span data-stu-id="b33e2-277">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="b33e2-278">Pasirinkite elementą **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-278">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="b33e2-279">Pasirinkite **Talpykla**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-279">Select **Cache**.</span></span>
    3. <span data-ttu-id="b33e2-280">Pasirinkite elementą **VendTable.\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-280">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="b33e2-281">Pasirinkite **Talpykla**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-281">Select **Cache**.</span></span>

    ![Lauko $TransType kaupimo talpykloje sąranka](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="b33e2-283">Atlikę toliau nurodytus veiksmus pakeiskite lauką **\$TransTypeRecord**, kad jis galėtų naudoti talpykloje esantį lauką **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-283">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="b33e2-284">Srityje **Duomenų šaltiniai** išplėskite elementą **VendTable**, išplėskite elementą **\<Ryšiai**, išplėskite elementą **VendTrans.VendTable\_AccountNum** ir pasirinkite elementą **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-284">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="b33e2-285">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-285">Select **Edit**.</span></span>
    3. <span data-ttu-id="b33e2-286">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-286">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="b33e2-287">Lauke **Formulė** suraskite toliau nurodytą išraišką.</span><span class="sxs-lookup"><span data-stu-id="b33e2-287">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="b33e2-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="b33e2-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="b33e2-289">Lauke **Formulė** įveskite toliau nurodytą išraišką.</span><span class="sxs-lookup"><span data-stu-id="b33e2-289">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="b33e2-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="b33e2-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="b33e2-291">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-291">Select **Save**.</span></span>
    7. <span data-ttu-id="b33e2-292">Uždarykite puslapį **Formulės rengyklė**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-292">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="b33e2-293">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-293">Select **OK**.</span></span>

5. <span data-ttu-id="b33e2-294">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-294">Select **Save**.</span></span>
6. <span data-ttu-id="b33e2-295">Uždarykite puslapį **Modelio susiejimo dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-295">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="b33e2-296">Uždarykite puslapį **Modelio susiejimai**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-296">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="b33e2-297">Modifikuotos ER modelio susiejimo versijos užbaigimas</span><span class="sxs-lookup"><span data-stu-id="b33e2-297">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="b33e2-298">RCS puslapio **Konfigūracijos** „FastTab“ **Versijos** pasirinkite konfigūracijos **Našumo sekimo susiejimas** versiją **1.2**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-298">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="b33e2-299">Pasirinkti **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-299">Select **Change status**.</span></span>
3. <span data-ttu-id="b33e2-300">Pasirinkite **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-300">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-finance-and-operations"></a><span data-ttu-id="b33e2-301">Modifikuotos ER modelio susiejimo konfigūracijos importavimas iš RCS į „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="b33e2-301">Import the modified ER model mapping configuration from RCS into Finance and Operations</span></span>

<span data-ttu-id="b33e2-302">Pakartokite veiksmus, aprašytus ankstesniame šios temos skyriuje [ER konfigūracijos importavimas iš RCS į „Finance and Operations“](#import-configuration) ir importuokite konfigūracijos **Našumo sekimo susiejimas** versiją 1.2 į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="b33e2-302">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration into Finance and Operations.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="b33e2-303">Modifikuoto ER vykdymo sekimo sprendimo vykdymas</span><span class="sxs-lookup"><span data-stu-id="b33e2-303">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="b33e2-304">ER formato vykdymas</span><span class="sxs-lookup"><span data-stu-id="b33e2-304">Run the ER format</span></span>

<span data-ttu-id="b33e2-305">Pakartoję ankstesniame šios temos skyriuje [ER formato vykdymas](#run-format) nurodytus veiksmus sugeneruokite naują našumo sekimą.</span><span class="sxs-lookup"><span data-stu-id="b33e2-305">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="b33e2-306">Vykdymo sekimo peržiūra</span><span class="sxs-lookup"><span data-stu-id="b33e2-306">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-finance-and-operations"></a><span data-ttu-id="b33e2-307">Sugeneruoto sekimo eksportavimas iš „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="b33e2-307">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="b33e2-308">Pakartoję ankstesniame šios temos skyriuje [Sugeneruoto sekimo eksportavimas iš „Finance and Operations“](#export-trace) nurodytus veiksmus vietiniame tinkle įrašykite naują našumo sekimą.</span><span class="sxs-lookup"><span data-stu-id="b33e2-308">Repeat the steps in the [Export the generated trace from Finance and Operations](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="b33e2-309">Sugeneruoto sekimo importavimas į RCS</span><span class="sxs-lookup"><span data-stu-id="b33e2-309">Import the generated trace into RCS</span></span>

<span data-ttu-id="b33e2-310">Pakartoję ankstesniame šios temos skyriuje [Sugeneruoto sekimo importavimas į RCS](#import-trace) nurodytus veiksmus importuokite naują našumo sekimą į RCS.</span><span class="sxs-lookup"><span data-stu-id="b33e2-310">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="b33e2-311">Našumo sekimo naudojimas analizei naudojantis RCS – Modelio susiejimas</span><span class="sxs-lookup"><span data-stu-id="b33e2-311">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="b33e2-312">Pakartoję ankstesniame šios temos skyriuje [Našumo sekimo naudojimas analizei naudojantis RCS – Modelio susiejimas](#use-trace) nurodytus veiksmus išanalizuokite naujausią našumo sekimą.</span><span class="sxs-lookup"><span data-stu-id="b33e2-312">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="b33e2-313">Atkreipkite dėmesį, kad atlikus modelio susiejimo pakeitimus, nebeliko pasikartojančių užklausų į duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="b33e2-313">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="b33e2-314">Taip pat sumažėjo šio modelio susiejimo iškvietimų į duomenų bazės lenteles ir duomenų šaltinius skaičius.</span><span class="sxs-lookup"><span data-stu-id="b33e2-314">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="b33e2-315">Todėl pagerėjo viso ER sprendimo našumas.</span><span class="sxs-lookup"><span data-stu-id="b33e2-315">Therefore, the performance of the whole ER solution has improved.</span></span>

![RCS puslapio modelio susiejimo dizaino įrankio duomenų šaltinio VendTable informacijos sekimas](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="b33e2-317">Sekimo informacijoje duomenų šaltinio VendTable reikšmė **\[12\]** nurodo, kad šis duomenų šaltinis buvo iškviestas 12 kartų.</span><span class="sxs-lookup"><span data-stu-id="b33e2-317">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="b33e2-318">Reikšmė **\[Q:6\]** nurodo, kad šeši iškvietimai paversti duomenų bazės iškvietimais lentelėje VendTable.</span><span class="sxs-lookup"><span data-stu-id="b33e2-318">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="b33e2-319">Reikšmė **\[C:6\]** nurodo, kad iš duomenų bazės surinkti įrašai buvo įrašyti į talpyklą, o šeši kiti iškvietimai apdoroti naudojant talpyklą.</span><span class="sxs-lookup"><span data-stu-id="b33e2-319">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="b33e2-320">Atkreipkite dėmesį, kad iškvietimų į duomenų šaltinį LedgerTransTypeList skaičius sumažėjo nuo 9027 iki 240.</span><span class="sxs-lookup"><span data-stu-id="b33e2-320">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![RCS puslapio modelio susiejimo dizaino įrankio duomenų šaltinio LedgerTransTypeList informacijos sekimas](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-finance-and-operations"></a><span data-ttu-id="b33e2-322">Vykdymo sekimo peržiūra naudojant „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="b33e2-322">Review the execution trace in Finance and Operations</span></span>

<span data-ttu-id="b33e2-323">Galimybė naudotis ER sistemos dizaino įrankiu gali būti siūloma ne tik RCS, bet ir kai kuriose „Finance and Operations“ versijose.</span><span class="sxs-lookup"><span data-stu-id="b33e2-323">In addition to RCS, some versions of Finance and Operations might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="b33e2-324">Šiose „Finance and Operations“ versijose galima įjungti parinktį **Kūrimo režimo įjungimas**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-324">These versions of Finance and Operations have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="b33e2-325">Šią pasirinktį galite rasti puslapio **Elektroninių ataskaitų parametrai**, kurį galite atidaryti darbo srityje **Elektroninės ataskaitos**, skirtuke **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-325">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Dizaino režimo parinkties įgalinimas „Finance and Operations“ puslapyje Elektroninių ataskaitų parametrai](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="b33e2-327">Jei naudojatės viena iš šių „Finance and Operations“ versijų, sugeneruotų našumo sekimų informaciją galite analizuoti tiesiogiai naudodamiesi „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="b33e2-327">If you use one of these versions of Finance and Operations, you can analyze the details of generated performance traces directly in Finance and Operations.</span></span> <span data-ttu-id="b33e2-328">Nereikia eksportuoti informacijos iš „Finance and Operation“ ir importuoti ją į RCS.</span><span class="sxs-lookup"><span data-stu-id="b33e2-328">You don't have to export them from Finance and Operation and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="b33e2-329">Vykdymo sekimo peržiūra naudojantis išoriniais įrankiais</span><span class="sxs-lookup"><span data-stu-id="b33e2-329">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="b33e2-330">Vartotojo parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="b33e2-330">Configure user parameters</span></span>

1. <span data-ttu-id="b33e2-331">„Finance and Operations“ eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-331">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="b33e2-332">Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-332">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="b33e2-333">Dialogo lango **Vartotojo parametrai** skyriaus **Vykdymo sekimas** lauke **Vykdymo sekimo formatas** pasirinkite **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-333">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="b33e2-334">ER formato vykdymas</span><span class="sxs-lookup"><span data-stu-id="b33e2-334">Run the ER format</span></span>

<span data-ttu-id="b33e2-335">Pakartoję ankstesniame šios temos skyriuje [ER formato vykdymas](#run-format) nurodytus veiksmus sugeneruokite naują našumo sekimą.</span><span class="sxs-lookup"><span data-stu-id="b33e2-335">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="b33e2-336">Atkreipkite dėmesį, kad interneto naršyklėje siūloma atsisiųsti ZIP failą.</span><span class="sxs-lookup"><span data-stu-id="b33e2-336">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="b33e2-337">Šiame faile pateikiamas našumo sekimas PerfView formatu.</span><span class="sxs-lookup"><span data-stu-id="b33e2-337">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="b33e2-338">Naudodamiesi PerfView našumo analizės įrankiu galite išanalizuoti informaciją apie ER formato vykdymą.</span><span class="sxs-lookup"><span data-stu-id="b33e2-338">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![Įvykdyto ER formato informacijos sekimas naudojant „PerfView“](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="b33e2-340">Norėdami peržiūrėti vykdymo sekimą, apimantį duomenų bazės užklausas, naudokite išorinius įrankius</span><span class="sxs-lookup"><span data-stu-id="b33e2-340">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="b33e2-341">Dėl patobulinimų, atliktų ER sistemoje, efektyvumo sekimo duomenys, sugeneruoti „PerfView“ formatu, dabar teikia daugiau išsamios informacijos apie ER formato vykdymą.</span><span class="sxs-lookup"><span data-stu-id="b33e2-341">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="b33e2-342">Naudojant „Microsoft Dynamics 365 for Finance and Operations“ 10.0.4 versiją (2019 m. liepos mėn.), šiuose sekimo duomenyse taip pat gali būti pateikiama informacija apie vykdytas SQL užklausas į programos duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="b33e2-342">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="b33e2-343">Vartotojo parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="b33e2-343">Configure user parameters</span></span>

1. <span data-ttu-id="b33e2-344">Programoje „Finance and Operations“ eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-344">In Finance and Operations, go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="b33e2-345">Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="b33e2-346">Dialogo lango **Vartotojo parametrai** skyriuje **Vykdymo sekimas** nustatykite toliau nurodytus parametrus.</span><span class="sxs-lookup"><span data-stu-id="b33e2-346">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="b33e2-347">Lauke **Vykdymo sekimo formatas** pasirinkite **„PerfView“ XML**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-347">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="b33e2-348">Nustatykite parinkties **Rinkti užklausų statistiką** reikšmę **Taip**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-348">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="b33e2-349">Nustatykite parinkties **Įjungti profilį** reikšmę **Taip**.</span><span class="sxs-lookup"><span data-stu-id="b33e2-349">Set the **Trace query** option to **Yes**.</span></span>

    ![„Finance and Operations“ vartotojo parametrų dialogo langas](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="b33e2-351">ER formato vykdymas</span><span class="sxs-lookup"><span data-stu-id="b33e2-351">Run the ER format</span></span>

<span data-ttu-id="b33e2-352">Pakartoję ankstesniame šios temos skyriuje [ER formato vykdymas](#run-format) nurodytus veiksmus sugeneruokite naują našumo sekimą.</span><span class="sxs-lookup"><span data-stu-id="b33e2-352">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="b33e2-353">Atkreipkite dėmesį, kad interneto naršyklėje siūloma atsisiųsti ZIP failą.</span><span class="sxs-lookup"><span data-stu-id="b33e2-353">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="b33e2-354">Šiame faile pateikiamas našumo sekimas PerfView formatu.</span><span class="sxs-lookup"><span data-stu-id="b33e2-354">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="b33e2-355">Naudodamiesi PerfView našumo analizės įrankiu galite išanalizuoti informaciją apie ER formato vykdymą.</span><span class="sxs-lookup"><span data-stu-id="b33e2-355">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="b33e2-356">Dabar šis sekimas apims informaciją apie SQL duomenų bazės prieigą vykdant ER formatą.</span><span class="sxs-lookup"><span data-stu-id="b33e2-356">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![Įvykdyto ER formato informacijos sekimas naudojant „PerfView“](./media/GER-PerfTrace2-PerfViewTrace2.PNG)
