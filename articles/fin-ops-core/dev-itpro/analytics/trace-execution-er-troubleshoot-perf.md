---
title: ER formatų vykdymo sekimas siekiant diagnozuoti našumo problemas
description: Šioje temoje pateikiama informacijos apie tai, kaip elektroninėse ataskaitose (ER) naudojantis našumo sekimo funkcija spręsti našumo problemas.
author: NickSelin
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7fbec962fea374afdbabaad48a42dad380708678
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295578"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="bba82-103">ER formatų vykdymo sekimas siekiant diagnozuoti našumo problemas</span><span class="sxs-lookup"><span data-stu-id="bba82-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="bba82-104">Kurdami elektroninių ataskaitų (ER) konfigūracijas, kuriomis naudojantis generuojami elektroniniai dokumentai, nurodote būdą, kuriuo naudodamiesi gaunate duomenis iš programos, ir įvedate jį į sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="bba82-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="bba82-105">Naudojantis ER našumo sekimo funkcija gali pastebimai sutrumpėti laikas, per kurį renkama informacija apie ER formato vykdymą, panaudojant ją našumo problemoms spręsti, ir gali būti patiriama mažiau išlaidų.</span><span class="sxs-lookup"><span data-stu-id="bba82-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="bba82-106">Šioje mokymo programoje pateikiama rekomendacijų apie tai, kaip atsižvelgti į įvykdytų ER formatų našumo sekimus ir kaip panaudoti šiuos sekimus siekiant pagerinti našumą.</span><span class="sxs-lookup"><span data-stu-id="bba82-106">This tutorial provides guidelines about how to take performance traces for executed ER formats, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bba82-107">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="bba82-107">Prerequisites</span></span>

<span data-ttu-id="bba82-108">Norint įvykdyti šios mokymo programos pavyzdžių užduotis, reikia toliau nurodytų prieigų.</span><span class="sxs-lookup"><span data-stu-id="bba82-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="bba82-109">Prieiga prie vieno iš toliau pateikiamų vaidmenų.</span><span class="sxs-lookup"><span data-stu-id="bba82-109">Access to one of the following roles:</span></span>

    - <span data-ttu-id="bba82-110">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="bba82-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="bba82-111">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="bba82-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="bba82-112">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="bba82-112">System administrator</span></span>

- <span data-ttu-id="bba82-113">Prieiga prie „Regulatory Configuration Services“ (RCS) egzemplioriaus, sukonfigūruoto tam pačiam nuomininkui, kuriam sukonfigūruota programa, vienam iš toliau nurodytų vaidmenų atlikti.</span><span class="sxs-lookup"><span data-stu-id="bba82-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as the application, for one of the following roles:</span></span>

    - <span data-ttu-id="bba82-114">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="bba82-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="bba82-115">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="bba82-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="bba82-116">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="bba82-116">System administrator</span></span>

<span data-ttu-id="bba82-117">Taip pat turite atsiųsti ir vietoje saugoti toliau nurodytus failus.</span><span class="sxs-lookup"><span data-stu-id="bba82-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="bba82-118">Failas</span><span class="sxs-lookup"><span data-stu-id="bba82-118">File</span></span>                                  | <span data-ttu-id="bba82-119">Turinys</span><span class="sxs-lookup"><span data-stu-id="bba82-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="bba82-120">Našumo sekimo modelis.versija.1</span><span class="sxs-lookup"><span data-stu-id="bba82-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="bba82-121">ER duomenų modelio konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="bba82-121">Sample ER data model configuration</span></span>](https://download.microsoft.com/download/0/a/a/0aa84e48-8040-4c46-b542-e3bf15c9b2ad/Performancetracemodelversion.1.xml)    |
| <span data-ttu-id="bba82-122">Našumo sekimo metaduomenys.versija.1</span><span class="sxs-lookup"><span data-stu-id="bba82-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="bba82-123">ER metaduomenų konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="bba82-123">Sample ER metadata configuration</span></span>](https://download.microsoft.com/download/a/9/3/a937e8c4-1f8a-43e4-83ee-7d599cf7d983/Performancetracemetadataversion.1.xml)      |
| <span data-ttu-id="bba82-124">Našumo sekimo susiejimas.versija.1.1</span><span class="sxs-lookup"><span data-stu-id="bba82-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="bba82-125">ER modelio susiejimo konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="bba82-125">Sample ER model mapping configuration</span></span>](https://download.microsoft.com/download/7/7/3/77379bdc-7b22-4cfc-9b64-a9147599f931/Performancetracemappingversion1.1.xml) |
| <span data-ttu-id="bba82-126">Našumo sekimo formatas.versija.1.1</span><span class="sxs-lookup"><span data-stu-id="bba82-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="bba82-127">ER formato konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="bba82-127">Sample ER format configuration</span></span>](https://download.microsoft.com/download/8/6/8/868ba581-5a06-459e-b173-fb00f038b37f/Performancetraceformatversion1.1.xml)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="bba82-128">ER parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="bba82-128">Configure ER parameters</span></span>

<span data-ttu-id="bba82-129">Kiekvienas programoje sugeneruotas ER našumo sekimas saugomas kaip vykdymo žurnalo įrašo priedas.</span><span class="sxs-lookup"><span data-stu-id="bba82-129">Each ER performance trace that is generated in the application is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="bba82-130">Šiems priedams tvarkyti naudojama dokumentų tvarkymo (DM) sistema.</span><span class="sxs-lookup"><span data-stu-id="bba82-130">The Document management (DM) framework is used to manage these attachments.</span></span> <span data-ttu-id="bba82-131">Norėdami nurodyti DM dokumento tipą, kuris turėtų būti naudojamas našumo sekimams pridėti, turite iš anksto sukonfigūruoti ER parametrus.</span><span class="sxs-lookup"><span data-stu-id="bba82-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="bba82-132">Darbo srityje **Elektroninės ataskaitos** pasirinkite **Elektroninių ataskaitų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="bba82-132">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="bba82-133">Tada puslapyje **Elektroninių ataskaitų parametrai** esančio skirtuko **Priedai** lauke **Kiti** pasirinkite DM dokumento tipą, kuris bus naudojamas našumo sekimui.</span><span class="sxs-lookup"><span data-stu-id="bba82-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Elektroninių ataskaitų parametrų puslapis](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="bba82-135">Norint, kad DM dokumento tipu būtų galima naudotis peržvalgos lauke **Kiti**, jis turi būti atitinkamai sukonfigūruotas puslapyje **Dokumentų tipai** (**Organizacijos administravimas \> Dokumentų valdymas \> Dokumentų tipai**):</span><span class="sxs-lookup"><span data-stu-id="bba82-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="bba82-136">**Klasė:** pridėti failą</span><span class="sxs-lookup"><span data-stu-id="bba82-136">**Class:** Attach file</span></span>
- <span data-ttu-id="bba82-137">**Grupė:** failas</span><span class="sxs-lookup"><span data-stu-id="bba82-137">**Group:** File</span></span>

![Puslapis Dokumentų tipai](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="bba82-139">Pasirinktas dokumento tipas turi būti pasiekiamas visose dabartinio egzemplioriaus įmonėse, nes DM priedai skirti konkrečioms įmonėms.</span><span class="sxs-lookup"><span data-stu-id="bba82-139">The selected document type must be available in every company of the current instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="bba82-140">RCS parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="bba82-140">Configure RCS parameters</span></span>

<span data-ttu-id="bba82-141">Sugeneruoti ER našumo sekimai importuojami į RCS analizei atlikti naudojant ER formato dizaino įrankį ir ER susiejimo dizaino įrankį.</span><span class="sxs-lookup"><span data-stu-id="bba82-141">ER performance traces that are generated will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="bba82-142">Kadangi ER našumo sekimai saugomi kaip su ER formatu susieto vykdymo žurnalo įrašo priedai, reikia iš anksto konfigūruoti RCS parametrus, kad būtų nurodytas DM dokumento tipas, kuris turėtų būti naudojamas našumo sekimams pridėti.</span><span class="sxs-lookup"><span data-stu-id="bba82-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="bba82-143">Jūsų įmonei sukurto RCS egzemplioriaus darbo srityje **Elektroninės ataskaitos** pasirinkite **Elektroninių ataskaitų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="bba82-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="bba82-144">Tada puslapyje **Elektroninių ataskaitų parametrai** esančio skirtuko **Priedai** lauke **Kiti** pasirinkite DM dokumento tipą, kuris bus naudojamas našumo sekimui.</span><span class="sxs-lookup"><span data-stu-id="bba82-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![RCS elektroninių ataskaitų parametrų puslapis](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="bba82-146">Norint, kad DM dokumento tipu būtų galima naudotis peržvalgos lauke **Kiti**, jis turi būti atitinkamai sukonfigūruotas puslapyje **Dokumentų tipai** (**Organizacijos administravimas \> Dokumentų valdymas \> Dokumentų tipai**):</span><span class="sxs-lookup"><span data-stu-id="bba82-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="bba82-147">**Klasė:** pridėti failą</span><span class="sxs-lookup"><span data-stu-id="bba82-147">**Class:** Attach file</span></span>
- <span data-ttu-id="bba82-148">**Grupė:** failas</span><span class="sxs-lookup"><span data-stu-id="bba82-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="bba82-149">ER sprendimo kūrimas</span><span class="sxs-lookup"><span data-stu-id="bba82-149">Design an ER solution</span></span>

<span data-ttu-id="bba82-150">Tarkime, kad jau pradėjau kurti naują ER sprendimą, kad būtų sugeneruota nauja ataskaita, kurioje pateikiamos tiekėjo operacijos.</span><span class="sxs-lookup"><span data-stu-id="bba82-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="bba82-151">Šiuo metu pasirinkto tiekėjo operacijas rasite puslapyje **Tiekėjo operacijos** (eikite į **Mokėtina suma \> Tiekėjai \> Visi tiekėjai**, pasirinkite tiekėją, paskui veiksmų srities skirtuko **Tiekėjas** grupėje **Operacijos** pasirinkite **Operacijos**).</span><span class="sxs-lookup"><span data-stu-id="bba82-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="bba82-152">Tačiau norite vienu metu turėti visas tiekėjo operacijas viename elektroniniame dokumente XML formatu.</span><span class="sxs-lookup"><span data-stu-id="bba82-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="bba82-153">Šį sprendimą sudaro kelios ER konfigūracijos, apimančios reikiamą duomenų modelį, metaduomenis, modelio susiejimą ir formato komponentus.</span><span class="sxs-lookup"><span data-stu-id="bba82-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="bba82-154">Prisijunkite prie jūsų įmonei sukurto RCS egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="bba82-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="bba82-155">Šioje mokymo programoje kursite ir modifikuosite pavyzdinės įmonės **„Litware, Inc.“** konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="bba82-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="bba82-156">Todėl įsitikinkite, kad šis konfigūracijos teikėjas buvo pridėtas prie RCS ir pasirinktas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="bba82-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="bba82-157">Instrukcijos aprašytos procedūroje [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="bba82-157">For instructions, see the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>
3. <span data-ttu-id="bba82-158">Darbo srityje **Elektroninės ataskaitos** pasirinkite plytelę **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="bba82-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="bba82-159">Puslapyje **Konfigūracijos** importuokite į RCS kaip būtinąjį komponentą atsisiųstas ER konfigūracijas tokia tvarka: duomenų modelis, metaduomenys, modelio susiejimas, formatas.</span><span class="sxs-lookup"><span data-stu-id="bba82-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="bba82-160">Kurdami kiekvieną konfigūraciją atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="bba82-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="bba82-161">Veiksmų srityje pasirinkite **Keitimas \> Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="bba82-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="bba82-162">Paspaudę **Naršyti** pasirinkite reikiamą ER konfigūracijos failą XML formatu.</span><span class="sxs-lookup"><span data-stu-id="bba82-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="bba82-163">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="bba82-163">Select **OK**.</span></span>

    ![RCS puslapis Konfigūracijos](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="bba82-165">ER vykdymo sekimo sprendimo vykdymas</span><span class="sxs-lookup"><span data-stu-id="bba82-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="bba82-166">Tarkime, kad baigėte kurti pirmąją ER sprendimo versiją.</span><span class="sxs-lookup"><span data-stu-id="bba82-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="bba82-167">Dabar norite ją patikrinti naudodami savo egzempliorių ir išanalizuoti vykdymo našumą.</span><span class="sxs-lookup"><span data-stu-id="bba82-167">You now want to test it in your instance and analyze execution performance.</span></span>

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a><span data-ttu-id="bba82-168">ER konfigūracijų importavimas iš RCS į „Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="bba82-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="bba82-169">Prisijunkite prie programos egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="bba82-169">Sign in to your application instance.</span></span>
2. <span data-ttu-id="bba82-170">Dirbdami su šia mokymo programa, konfigūracijas importuosite iš savo RCS egzemplioriaus (kuriame kuriate savo ER komponentus) į savo egzempliorių (kuriame jas tikrinate ir galiausiai naudojate).</span><span class="sxs-lookup"><span data-stu-id="bba82-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your instance (where you test and finally use them).</span></span> <span data-ttu-id="bba82-171">Todėl turite įsitikinti, kad paruošti visi reikiami artefaktai.</span><span class="sxs-lookup"><span data-stu-id="bba82-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="bba82-172">Instrukcijas rasite procedūroje [Elektroninių ataskaitų (ER) konfigūracijų importavimas iš „Regulatory Configuration Services“ (RCS)](rcs-download-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="bba82-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md) procedure.</span></span>
3. <span data-ttu-id="bba82-173">Atlikdami toliau nurodytus veiksmus importuokite konfigūracijas iš RCS į programą.</span><span class="sxs-lookup"><span data-stu-id="bba82-173">Follow these steps to import the configurations from RCS into the application:</span></span>

    1. <span data-ttu-id="bba82-174">Darbo srityje **Elektroninės ataskaitos** konfigūracijos tiekėjui **„Litware, Inc.“** skirtoje plytelėje pasirinkite **Saugyklos**.</span><span class="sxs-lookup"><span data-stu-id="bba82-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="bba82-175">Puslapyje **Konfigūracijų saugykla** pasirinkite tipo **RCS** saugyklą, paskui pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="bba82-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="bba82-176">„FastTab“ **Konfigūracijos** pasirinkite konfigūraciją **Našumo sekimo formatas**.</span><span class="sxs-lookup"><span data-stu-id="bba82-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="bba82-177">„FastTab“ **Versijos** pasirinkite pasirinktos ER konfigūracijos versiją **1.1**, paskui pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="bba82-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Konfigūracijos saugyklos puslapis](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="bba82-179">Atitinkamų versijų duomenų modeliai ir modelio susiejimo konfigūracijos automatiškai importuojami kaip būtinieji importuotos ER formato konfigūracijos komponentai.</span><span class="sxs-lookup"><span data-stu-id="bba82-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="bba82-180">ER veiklos sekimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="bba82-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="bba82-181">Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="bba82-181">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="bba82-182">Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="bba82-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="bba82-183">Dialogo lango **Vartotojo parametrai** skyriuje **Vykdymo sekimas** atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="bba82-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="bba82-184">Lauke **Vykdymo sekimo formatas** nurodykite sugeneruoto našumo sekimo formatą, kurio vykdymo informacija turėtų būtų saugoma ER formatui ir susiejimo elementams:</span><span class="sxs-lookup"><span data-stu-id="bba82-184">In the **Execution trace format** field, specify the format of the generated performance trace that the execution details should be stored in for ER format and mapping elements:</span></span>

        - <span data-ttu-id="bba82-185">**Derinti sekimo formatą** – pasirinkite šią reikšmę, jei planuojate interaktyviai paleisti ER formatą, turintį trumpą vykdymo laiką.</span><span class="sxs-lookup"><span data-stu-id="bba82-185">**Debug trace format** – Select this value if you plan to interactively run an ER format that has a short execution time.</span></span> <span data-ttu-id="bba82-186">Tada pradedamas išsamios ER formato vykdymo informacijos rinkinys.</span><span class="sxs-lookup"><span data-stu-id="bba82-186">The collection of details about ER format execution is then started.</span></span> <span data-ttu-id="bba82-187">Pasirinkus šią reikšmę, našumo sekimas surenka informaciją apie laiką, praleistą toliau nurodytiems veiksmams atlikti:</span><span class="sxs-lookup"><span data-stu-id="bba82-187">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="bba82-188">Kiekvieno duomenims gauti iškviesto modelio susiejimo duomenų šaltinio vykdymas</span><span class="sxs-lookup"><span data-stu-id="bba82-188">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="bba82-189">Kiekvieno formato elemento apdorojimas įvedant duomenis į sugeneruotą išvestį</span><span class="sxs-lookup"><span data-stu-id="bba82-189">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="bba82-190">Jei pasirenkate **Derinti sekimo formatą** reikšmę, galėsite analizuoti sekimo turinį ER operacijų dizaino įrankyje.</span><span class="sxs-lookup"><span data-stu-id="bba82-190">If you select the **Debug trace format** value, you can analyze the content of the trace in the ER Operation designer.</span></span> <span data-ttu-id="bba82-191">Ten galite peržiūrėti ER formatą arba susiejimo elementus, kurie nurodyti sekime.</span><span class="sxs-lookup"><span data-stu-id="bba82-191">There, you can view the ER format or mapping elements that are mentioned in the trace.</span></span>

        - <span data-ttu-id="bba82-192">**Agreguotas sekimo formatas** – pasirinkite šią reikšmę, jei planuojate paleisti ER formatą, turintį ilgą vykdymo laiką paketiniu režimu.</span><span class="sxs-lookup"><span data-stu-id="bba82-192">**Aggregated trace format** – Select this value if you plan to run an ER format that has a long execution time in batch mode.</span></span> <span data-ttu-id="bba82-193">Tada pradedamas agreguotos išsamios ER formato vykdymo informacijos rinkinys.</span><span class="sxs-lookup"><span data-stu-id="bba82-193">The collection of the aggregated details about ER format execution is then started.</span></span> <span data-ttu-id="bba82-194">Pasirinkus šią reikšmę, našumo sekimas surenka informaciją apie laiką, praleistą toliau nurodytiems veiksmams atlikti:</span><span class="sxs-lookup"><span data-stu-id="bba82-194">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="bba82-195">Kiekvieno duomenims gauti iškviesto modelio susiejimo duomenų šaltinio vykdymas</span><span class="sxs-lookup"><span data-stu-id="bba82-195">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="bba82-196">Kiekvieno duomenims gauti iškviesto formato susiejimo duomenų šaltinio vykdymas</span><span class="sxs-lookup"><span data-stu-id="bba82-196">Running each data source in the format mapping that is called to get data</span></span>
            - <span data-ttu-id="bba82-197">Kiekvieno formato elemento apdorojimas įvedant duomenis į sugeneruotą išvestį</span><span class="sxs-lookup"><span data-stu-id="bba82-197">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="bba82-198">**Agreguoto sekimo formato** reikšmė galima 10.0.20 ir vėlesnėse „Microsoft Dynamics 365 Finance” versijose.</span><span class="sxs-lookup"><span data-stu-id="bba82-198">The **Aggregated trace format** value is available in Microsoft Dynamics 365 Finance version 10.0.20 and later.</span></span>

            <span data-ttu-id="bba82-199">ER formato dizaino įrankyje ir ER modelio susiejimo dizaino įrankyje galite peržiūrėti bendrą vieno komponento vykdymo laiką.</span><span class="sxs-lookup"><span data-stu-id="bba82-199">In the ER format designer and ER model mapping designer, you can view the total execution time for a single component.</span></span> <span data-ttu-id="bba82-200">Be to, sekimas apima išsamią vykdymo informaciją, pavyzdžiui, vykdymų skaičių ir minimalų bei maksimalų vieno vykdymo laiką.</span><span class="sxs-lookup"><span data-stu-id="bba82-200">Additionally, the trace contains details about the execution, such as the number of executions, and the minimum and maximum time of a single execution.</span></span>

            > [!NOTE]
            > <span data-ttu-id="bba82-201">Šis sekimas yra surenkamas remiantis sekamų komponentų maršrutu.</span><span class="sxs-lookup"><span data-stu-id="bba82-201">This trace is collected based on the traced components path.</span></span> <span data-ttu-id="bba82-202">Todėl statistiniai duomenys gali būti klaidingi, kai viename pirminiame komponente yra keli antriniai komponentai, neturintys pavadinimo, arba kai keli antriniai komponentai yra to paties pavadinimo.</span><span class="sxs-lookup"><span data-stu-id="bba82-202">Therefore, the statistics might be incorrect when a single parent component contains several unnamed child components, or when several child components have the same name.</span></span>

    2. <span data-ttu-id="bba82-203">Nustatykite tolesnių parinkčių reikšmes **Taip**, kad būtų galima rinkti konkrečią informaciją apie ER modelio susiejimo vykdymą ir ER formato komponentus.</span><span class="sxs-lookup"><span data-stu-id="bba82-203">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="bba82-204">**Rinkti užklausų statistiką** – įjungus šią parinktį, našumo sekimas renka toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="bba82-204">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="bba82-205">Duomenų šaltinių atliktų duomenų bazės iškvietimų skaičius</span><span class="sxs-lookup"><span data-stu-id="bba82-205">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="bba82-206">Pasikartojančių iškvietimų į duomenų bazę skaičius</span><span class="sxs-lookup"><span data-stu-id="bba82-206">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="bba82-207">Informacija apie duomenų bazės iškvietimams atlikti naudotus SQL išrašus</span><span class="sxs-lookup"><span data-stu-id="bba82-207">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="bba82-208">**Talpyklos sekimo prieiga** – įjungus šią parinktį, našumo sekimas renka informaciją apie ER modelio susiejimo talpyklos naudojimą.</span><span class="sxs-lookup"><span data-stu-id="bba82-208">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="bba82-209">**Sekimo duomenų prieiga** – įjungus šią parinktį, našumo sekimas renka informaciją apie iškvietimų į įvykdytų įrašo sąrašo tipo duomenų šaltinių duomenų bazę skaičių.</span><span class="sxs-lookup"><span data-stu-id="bba82-209">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="bba82-210">**Sekimų sąrašo išvardijimas** – įjungus šią parinktį, našumo sekimas renka informaciją apie iš įrašo sąrašo tipo duomenų šaltinių pageidaujamų įrašų skaičių.</span><span class="sxs-lookup"><span data-stu-id="bba82-210">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bba82-211">Dialogo lange **Vartotojo parametrai** nurodyti vartotojo ir dabartinės įmonės parametrai.</span><span class="sxs-lookup"><span data-stu-id="bba82-211">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Vartotojo parametrų dialogo langas](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a><span data-ttu-id="bba82-213">ER formato vykdymas</span><span class="sxs-lookup"><span data-stu-id="bba82-213">Run the ER format</span></span>

1. <span data-ttu-id="bba82-214">Pasirinkite įmonę **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="bba82-214">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="bba82-215">Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="bba82-215">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="bba82-216">Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite elementą **Našumo sekimo formatas**.</span><span class="sxs-lookup"><span data-stu-id="bba82-216">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="bba82-217">Veiksmų srityje pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="bba82-217">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="bba82-218">Atkreipkite dėmesį, kad sugeneruotame faile pateikiama informacijos apie 265 šešių tiekėjų operacijas.</span><span class="sxs-lookup"><span data-stu-id="bba82-218">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="bba82-219">Vykdymo sekimo peržiūra</span><span class="sxs-lookup"><span data-stu-id="bba82-219">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a><span data-ttu-id="bba82-220">Sugeneruotos sekimo programos eksportavimas iš programos</span><span class="sxs-lookup"><span data-stu-id="bba82-220">Export the generated trace from the application</span></span>

<span data-ttu-id="bba82-221">Našumo sekimai atsiejami nuo šaltinio ER formato ir gali būti išdėstyti eilutėmis išoriniame ZIP faile.</span><span class="sxs-lookup"><span data-stu-id="bba82-221">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="bba82-222">Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos derinimo žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="bba82-222">Go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="bba82-223">Puslapio **Elektroninių ataskaitų vykdymo žurnalai** kairiosios srities lauke **Konfigūracijos pavadinimas** pasirinkite **Našumo sekimo formatą**, kad rastumėte žurnalo įrašus, sugeneruotus vykdant konfigūraciją **Našumo sekimo formatas**.</span><span class="sxs-lookup"><span data-stu-id="bba82-223">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="bba82-224">Paspauskite viršutiniame dešiniajame puslapio kampe esantį mygtuką (sąvaržėlės simbolis) **Priedai** arba paspauskite **Ctrl+Shift+A**.</span><span class="sxs-lookup"><span data-stu-id="bba82-224">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Puslapio Elektroninių ataskaitų vykdymo žurnalai mygtukas Priedai](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="bba82-226">Norėdami gauti našumo sekimą kaip ZIP failą ir saugoti jį vietoje, puslapio **Elektroninių ataskaitų vykdymo žurnalų priedai** veiksmų srityje pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="bba82-226">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Elektroninių ataskaitų vykdymo žurnalų priedai](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="bba82-228">Sugeneruotame sekime yra nuoroda į šaltinio ER ataskaitą naudojant unikalų ataskaitos identifikatorių tik **GUID** formatu.</span><span class="sxs-lookup"><span data-stu-id="bba82-228">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="bba82-229">Į formato versijos numeravimą neatsižvelgiama.</span><span class="sxs-lookup"><span data-stu-id="bba82-229">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="bba82-230">Atkreipkite dėmesį, kad ryšys tarp įvykdyto ER formatui sugeneruoto našumo sekimo ir ER modelio susiejimo paremtas naudotu šakniniu aprašu ir bendru duomenų modeliu.</span><span class="sxs-lookup"><span data-stu-id="bba82-230">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="bba82-231">Į formato ir modelio susiejimo versijos numeravimą neatsižvelgiama.</span><span class="sxs-lookup"><span data-stu-id="bba82-231">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="bba82-232">Taip pat neatsižvelgiama į modelio susiejimo žymę **Numatytasis modelių susiejimui**.</span><span class="sxs-lookup"><span data-stu-id="bba82-232">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a><span data-ttu-id="bba82-233">Sugeneruoto sekimo importavimas į RCS</span><span class="sxs-lookup"><span data-stu-id="bba82-233">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="bba82-234">RCS darbo srityje **Elektroninės ataskaitos** pasirinkite plytelę **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="bba82-234">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="bba82-235">Puslapio **Konfigūracijos** konfigūracijų medyje išplėskite elementą **Našumo sekimo modelis** ir pasirinkite elementą **Našumo sekimo formatas**.</span><span class="sxs-lookup"><span data-stu-id="bba82-235">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="bba82-236">Veiksmų srityje pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="bba82-236">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="bba82-237">Puslapio **Formato dizaino įrankis** veiksmų srityje pasirinkite **Našumo sekimas**.</span><span class="sxs-lookup"><span data-stu-id="bba82-237">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="bba82-238">Dialogo lange **Našumo sekimo rezultato parametrai** pasirinkite **Importuoti našumo sekimą**.</span><span class="sxs-lookup"><span data-stu-id="bba82-238">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="bba82-239">Pasirinkite **Naršyti** ir pasirinkite ZIP failą, kurį eksportavote anksčiau.</span><span class="sxs-lookup"><span data-stu-id="bba82-239">Select **Browse** to select the zip file that you exported earlier.</span></span>
7. <span data-ttu-id="bba82-240">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="bba82-240">Select **OK**.</span></span>

    ![Našumo sekimo rezultato parametrų dialogo langas, esantis RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="bba82-242">Našumo sekimo naudojimas analizei naudojantis RCS – Formato vykdymas</span><span class="sxs-lookup"><span data-stu-id="bba82-242">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="bba82-243">RCS puslapyje **Formato dizaino įrankis** pasirinkę **Išplėsti / sutraukti** išplėskite visų formato elementų turinį.</span><span class="sxs-lookup"><span data-stu-id="bba82-243">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="bba82-244">Atkreipkite dėmesį, kad rodoma papildomos informacijos apie kai kuriuos dabartinio formato elementus.</span><span class="sxs-lookup"><span data-stu-id="bba82-244">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="bba82-245">Faktinis laikas, sugaištas įvedant duomenis į sugeneruotą išvestį naudojant formato elementą</span><span class="sxs-lookup"><span data-stu-id="bba82-245">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="bba82-246">Tas pats laikas išreikštas kaip viso laiko, praleisto generuojant visą išvestį, procentinė dalis</span><span class="sxs-lookup"><span data-stu-id="bba82-246">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![RCS formato dizaino įrankio puslapis](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="bba82-248">Uždarykite puslapį **Formato dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="bba82-248">Close **Format designer** page.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a><span data-ttu-id="bba82-249">Našumo sekimo naudojimas analizei naudojantis RCS – Modelio susiejimas</span><span class="sxs-lookup"><span data-stu-id="bba82-249">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="bba82-250">RCS puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite elementą **Našumo sekimo susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="bba82-250">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="bba82-251">Veiksmų srityje pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="bba82-251">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="bba82-252">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="bba82-252">Select **Designer**.</span></span>
4. <span data-ttu-id="bba82-253">Puslapio **Modelio susiejimo dizaino įrankis** veiksmų srityje pasirinkite **Našumo sekimas**.</span><span class="sxs-lookup"><span data-stu-id="bba82-253">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="bba82-254">Pasirinkite anksčiau importuotą sekimą.</span><span class="sxs-lookup"><span data-stu-id="bba82-254">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="bba82-255">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="bba82-255">Select **OK**.</span></span>

<span data-ttu-id="bba82-256">Atkreipkite dėmesį, kad atsiranda naujos informacijos apie kai kuriuos dabartinio modelio susiejimo duomenų šaltinio elementus.</span><span class="sxs-lookup"><span data-stu-id="bba82-256">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="bba82-257">Faktinis laikas, sugaištas gaunant duomenis naudojant duomenų šaltinį</span><span class="sxs-lookup"><span data-stu-id="bba82-257">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="bba82-258">Tas pats laikas, išreikštas kaip viso laiko, praleisto vykdant visą modelio susiejimą, procentinė dalis</span><span class="sxs-lookup"><span data-stu-id="bba82-258">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="bba82-259">Atkreipkite dėmesį, kad ER informuoja tuo atveju, kai dabartinis modelio susiejimas sutampa su duomenų bazės užklausomis, kai paleistas duomenų šaltinis VendTable/\<Relations/VendTrans.VendTable\_AccountNum.</span><span class="sxs-lookup"><span data-stu-id="bba82-259">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="bba82-260">Šis pasikartojimas įvyksta todėl, kad kiekvieno pasikartojančio tiekėjo įrašo atveju tiekėjo operacijų sąrašas iškviečiamas du kartus.</span><span class="sxs-lookup"><span data-stu-id="bba82-260">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="bba82-261">Vienas iškvietimas atliekamas norint į duomenų modelį įvesti informaciją apie kiekvieną operaciją pagal sukonfigūruotus susiejimus.</span><span class="sxs-lookup"><span data-stu-id="bba82-261">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="bba82-262">Vienas iškvietimas atliekamas norint įvesti apskaičiuotą kiekvieno duomenų modelio tiekėjo operacijų skaičių.</span><span class="sxs-lookup"><span data-stu-id="bba82-262">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![Pranešimas apie pasikartojančias RCS puslapio Modelio susiejimo dizaino įrankis duomenų bazės užklausas](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="bba82-264">Reikšmė **\[q:530\]** nurodo, kad lentelė VendTrans buvo iškviesta 530 kartų, kad į duomenų šaltinį VendTable/\<Relations/VendTrans.VendTable\_AccountNum būtų pateiktas tos lentelės įrašas.</span><span class="sxs-lookup"><span data-stu-id="bba82-264">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="bba82-265">Reikšmė **\[530\]** nurodo, kad duomenų šaltinis VendTable/\<Relations/VendTrans.VendTable\_AccountNum buvo iškviestas 530 kartus, kad būtų pateiktas to duomenų šaltinio įrašas ir duomenų modelyje būtų įvesta jo informacija.</span><span class="sxs-lookup"><span data-stu-id="bba82-265">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="bba82-266">Rekomenduojame naudoti duomenų šaltiniui VendTable/\<Relations/VendTrans.VendTable\_AccountNum skirtą talpyklą, kad sumažėtų siekiant gauti informacijos apie 265 operacijas atliktų iškvietimų skaičius ir pagerėtų modelio susiejimo našumas.</span><span class="sxs-lookup"><span data-stu-id="bba82-266">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="bba82-267">Taip pat gali būti naudinga sumažinti į duomenų šaltinį LedgerTransTypeList atliktų iškvietimų skaičių.</span><span class="sxs-lookup"><span data-stu-id="bba82-267">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="bba82-268">Šis duomenų šaltinis naudojamas norint susieti kiekvieną išvardijimo **LedgerTransType** reikšmę su jos žyme.</span><span class="sxs-lookup"><span data-stu-id="bba82-268">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="bba82-269">Naudodami šį duomenų šaltinį, galite rasti atitinkamą žymę ir įvesti ją kiekvieno tiekėjo operacijos duomenų modelyje.</span><span class="sxs-lookup"><span data-stu-id="bba82-269">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="bba82-270">Dabartinis iškvietimų į šį duomenų šaltinį skaičius (9027) gana didelis, turint omenyje, kad apdorojamos 265 operacijos.</span><span class="sxs-lookup"><span data-stu-id="bba82-270">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![RCS puslapis Modelio susiejimo dizaino įrankis, kuriame rodomi 9027 iškvietimai į duomenų šaltinį](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="bba82-272">Patobulinkite modelio susiejimą pagal iš vykdymo sekimo gautą informacija</span><span class="sxs-lookup"><span data-stu-id="bba82-272">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="bba82-273">Modelio susiejimo logikos keitimas</span><span class="sxs-lookup"><span data-stu-id="bba82-273">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="bba82-274">Atlikite toliau nurodytus veiksmus, kad būtų kaupiama talpykloje ir išvengiama pasikartojančių iškvietimų į duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="bba82-274">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="bba82-275">RCS puslapio **Modelio susiejimo dizaino įrankis** srityje **Duomenų šaltiniai** pasirinkite elementą **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="bba82-275">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="bba82-276">Pasirinkite **Talpykla**.</span><span class="sxs-lookup"><span data-stu-id="bba82-276">Select **Cache**.</span></span>
    3. <span data-ttu-id="bba82-277">Išplėskite elementą **VendTable**, išplėskite duomenų šaltinio VendTable ryšių „vienas su daugeliu“ sąrašą (elementas **\<Ryšiai**) ir pasirinkite elementą **VendTrans.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="bba82-277">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="bba82-278">Pasirinkite **Talpykla**.</span><span class="sxs-lookup"><span data-stu-id="bba82-278">Select **Cache**.</span></span>

    ![Kaupimo talpykloje nustatymas, kad būtų išvengta pasikartojančių iškvietimų](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="bba82-280">Atlikite toliau nurodytus veiksmus, norėdami, kad duomenų šaltinis LedgerTransTypeList patektų į duomenų šaltinio VendTable sritį.</span><span class="sxs-lookup"><span data-stu-id="bba82-280">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="bba82-281">Srityje **Duomenų šaltinio tipai** išplėskite elementą **Funkcijos** ir pasirinkite elementą **Apskaičiuotasis laukas**.</span><span class="sxs-lookup"><span data-stu-id="bba82-281">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="bba82-282">Srityje **Duomenų šaltiniai** pasirinkite elementą **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="bba82-282">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="bba82-283">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="bba82-283">Select **Add**.</span></span>
    4. <span data-ttu-id="bba82-284">Lauke **Pavadinimas** įveskite **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="bba82-284">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="bba82-285">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="bba82-285">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="bba82-286">Lauke **Formulė** įveskite **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="bba82-286">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="bba82-287">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="bba82-287">Select **Save**.</span></span>
    8. <span data-ttu-id="bba82-288">Uždarykite puslapį **Formulės rengyklė**.</span><span class="sxs-lookup"><span data-stu-id="bba82-288">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="bba82-289">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="bba82-289">Click **OK**.</span></span>

3. <span data-ttu-id="bba82-290">Atlikę toliau nurodytus veiksmus atlikite lauko **\$TransType** talpyklinius mainus.</span><span class="sxs-lookup"><span data-stu-id="bba82-290">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="bba82-291">Pasirinkite elementą **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="bba82-291">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="bba82-292">Pasirinkite **Talpykla**.</span><span class="sxs-lookup"><span data-stu-id="bba82-292">Select **Cache**.</span></span>
    3. <span data-ttu-id="bba82-293">Pasirinkite elementą **VendTable.\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="bba82-293">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="bba82-294">Pasirinkite **Talpykla**.</span><span class="sxs-lookup"><span data-stu-id="bba82-294">Select **Cache**.</span></span>

    ![Lauko $TransType kaupimo talpykloje sąranka](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="bba82-296">Atlikę toliau nurodytus veiksmus pakeiskite lauką **\$TransTypeRecord**, kad jis galėtų naudoti talpykloje esantį lauką **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="bba82-296">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="bba82-297">Srityje **Duomenų šaltiniai** išplėskite elementą **VendTable**, išplėskite elementą **\<Ryšiai**, išplėskite elementą **VendTrans.VendTable\_AccountNum** ir pasirinkite elementą **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.</span><span class="sxs-lookup"><span data-stu-id="bba82-297">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="bba82-298">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="bba82-298">Select **Edit**.</span></span>
    3. <span data-ttu-id="bba82-299">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="bba82-299">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="bba82-300">Lauke **Formulė** suraskite toliau nurodytą išraišką.</span><span class="sxs-lookup"><span data-stu-id="bba82-300">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="bba82-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="bba82-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="bba82-302">Lauke **Formulė** įveskite toliau nurodytą išraišką.</span><span class="sxs-lookup"><span data-stu-id="bba82-302">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="bba82-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="bba82-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="bba82-304">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="bba82-304">Select **Save**.</span></span>
    7. <span data-ttu-id="bba82-305">Uždarykite puslapį **Formulės rengyklė**.</span><span class="sxs-lookup"><span data-stu-id="bba82-305">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="bba82-306">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="bba82-306">Select **OK**.</span></span>

5. <span data-ttu-id="bba82-307">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="bba82-307">Select **Save**.</span></span>
6. <span data-ttu-id="bba82-308">Uždarykite puslapį **Modelio susiejimo dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="bba82-308">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="bba82-309">Uždarykite puslapį **Modelio susiejimai**.</span><span class="sxs-lookup"><span data-stu-id="bba82-309">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="bba82-310">Modifikuotos ER modelio susiejimo versijos užbaigimas</span><span class="sxs-lookup"><span data-stu-id="bba82-310">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="bba82-311">RCS puslapio **Konfigūracijos** „FastTab“ **Versijos** pasirinkite konfigūracijos **Našumo sekimo susiejimas** versiją **1.2**.</span><span class="sxs-lookup"><span data-stu-id="bba82-311">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="bba82-312">Pasirinkti **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="bba82-312">Select **Change status**.</span></span>
3. <span data-ttu-id="bba82-313">Pasirinkite **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="bba82-313">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a><span data-ttu-id="bba82-314">Modifikuotos ER modelio susiejimo konfigūracijos importavimas iš RCS į programą</span><span class="sxs-lookup"><span data-stu-id="bba82-314">Import the modified ER model mapping configuration from RCS into the application</span></span>

<span data-ttu-id="bba82-315">Pakartokite veiksmus, aprašytus ankstesniame šios temos skyriuje [ER konfigūracijos importavimas iš RCS į „Finance and Operations“](#import-configuration) ir importuokite konfigūracijos **Našumo sekimo susiejimas** 1.2 versiją.</span><span class="sxs-lookup"><span data-stu-id="bba82-315">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="bba82-316">Modifikuoto ER vykdymo sekimo sprendimo vykdymas</span><span class="sxs-lookup"><span data-stu-id="bba82-316">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="bba82-317">ER formato vykdymas</span><span class="sxs-lookup"><span data-stu-id="bba82-317">Run the ER format</span></span>

<span data-ttu-id="bba82-318">Pakartoję ankstesniame šios temos skyriuje [ER formato vykdymas](#run-format) nurodytus veiksmus sugeneruokite naują našumo sekimą.</span><span class="sxs-lookup"><span data-stu-id="bba82-318">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="work-with-the-execution-trace"></a><span data-ttu-id="bba82-319">Darbas su vykdymo sekimu</span><span class="sxs-lookup"><span data-stu-id="bba82-319">Work with the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><span data-ttu-id="bba82-320">Sugeneruotos sekimo eksportavimas iš programos</span><span class="sxs-lookup"><span data-stu-id="bba82-320">Export the generated trace from the application</span></span>

<span data-ttu-id="bba82-321">Pakartoję ankstesniame šios temos skyriuje [Sugeneruoto sekimo eksportavimas iš programos](#export-trace) nurodytus veiksmus, vietiniame tinkle įrašykite naują našumo sekimą.</span><span class="sxs-lookup"><span data-stu-id="bba82-321">Repeat the steps in the [Export the generated trace from the application](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="bba82-322">Sugeneruoto sekimo importavimas į RCS</span><span class="sxs-lookup"><span data-stu-id="bba82-322">Import the generated trace into RCS</span></span>

<span data-ttu-id="bba82-323">Pakartoję ankstesniame šios temos skyriuje [Sugeneruoto sekimo importavimas į RCS](#import-trace) nurodytus veiksmus importuokite naują našumo sekimą į RCS.</span><span class="sxs-lookup"><span data-stu-id="bba82-323">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="bba82-324">Našumo sekimo naudojimas analizei naudojantis RCS – Modelio susiejimas</span><span class="sxs-lookup"><span data-stu-id="bba82-324">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="bba82-325">Pakartoję ankstesniame šios temos skyriuje [Našumo sekimo naudojimas analizei naudojantis RCS – Modelio susiejimas](#use-trace) nurodytus veiksmus išanalizuokite naujausią našumo sekimą.</span><span class="sxs-lookup"><span data-stu-id="bba82-325">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="bba82-326">Atkreipkite dėmesį, kad atlikus modelio susiejimo pakeitimus, nebeliko pasikartojančių užklausų į duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="bba82-326">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="bba82-327">Taip pat sumažėjo šio modelio susiejimo iškvietimų į duomenų bazės lenteles ir duomenų šaltinius skaičius.</span><span class="sxs-lookup"><span data-stu-id="bba82-327">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="bba82-328">Todėl pagerėjo viso ER sprendimo našumas.</span><span class="sxs-lookup"><span data-stu-id="bba82-328">Therefore, the performance of the whole ER solution has improved.</span></span>

![RCS puslapio modelio susiejimo dizaino įrankio duomenų šaltinio VendTable informacijos sekimas](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="bba82-330">Sekimo informacijoje duomenų šaltinio VendTable reikšmė **\[12\]** nurodo, kad šis duomenų šaltinis buvo iškviestas 12 kartų.</span><span class="sxs-lookup"><span data-stu-id="bba82-330">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="bba82-331">Reikšmė **\[Q:6\]** nurodo, kad šeši iškvietimai paversti duomenų bazės iškvietimais lentelėje VendTable.</span><span class="sxs-lookup"><span data-stu-id="bba82-331">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="bba82-332">Reikšmė **\[C:6\]** nurodo, kad iš duomenų bazės surinkti įrašai buvo įrašyti į talpyklą, o šeši kiti iškvietimai apdoroti naudojant talpyklą.</span><span class="sxs-lookup"><span data-stu-id="bba82-332">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="bba82-333">Atkreipkite dėmesį, kad iškvietimų į duomenų šaltinį LedgerTransTypeList skaičius sumažėjo nuo 9027 iki 240.</span><span class="sxs-lookup"><span data-stu-id="bba82-333">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![RCS puslapio modelio susiejimo dizaino įrankio duomenų šaltinio LedgerTransTypeList informacijos sekimas](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a><span data-ttu-id="bba82-335">Vykdymo sekimo peržiūra programoje</span><span class="sxs-lookup"><span data-stu-id="bba82-335">Review the execution trace in the application</span></span>

<span data-ttu-id="bba82-336">Galimybė naudotis ER sistemos dizaino įrankiu gali būti siūloma ne tik RCS, bet ir kai kuriose versijose.</span><span class="sxs-lookup"><span data-stu-id="bba82-336">In addition to RCS, some versions might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="bba82-337">Šiose versijose galima įjungti parinktį **Kūrimo režimo įjungimas**.</span><span class="sxs-lookup"><span data-stu-id="bba82-337">These versions have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="bba82-338">Šią pasirinktį galite rasti puslapio **Elektroninių ataskaitų parametrai**, kurį galite atidaryti darbo srityje **Elektroninės ataskaitos**, skirtuke **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="bba82-338">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Kūrimo režimo parinkties įjungimas Elektroninių ataskaitų parametrų puslapyje](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="bba82-340">Jei naudojatės viena iš šių versijų, sugeneruotų našumo sekimų informaciją galite analizuoti tiesiogiai programoje.</span><span class="sxs-lookup"><span data-stu-id="bba82-340">If you use one of these versions, you can analyze the details of generated performance traces directly in the application.</span></span> <span data-ttu-id="bba82-341">Nereikia eksportuoti informacijos iš programos ir importuoti ją į RCS.</span><span class="sxs-lookup"><span data-stu-id="bba82-341">You don't have to export them from the application and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="bba82-342">Vykdymo sekimo peržiūra naudojantis išoriniais įrankiais</span><span class="sxs-lookup"><span data-stu-id="bba82-342">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="bba82-343">Vartotojo parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="bba82-343">Configure user parameters</span></span>

1. <span data-ttu-id="bba82-344">Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="bba82-344">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="bba82-345">Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="bba82-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="bba82-346">Dialogo lango **Vartotojo parametrai** skyriaus **Vykdymo sekimas** lauke **Vykdymo sekimo formatas** pasirinkite **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="bba82-346">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="bba82-347">ER formato vykdymas</span><span class="sxs-lookup"><span data-stu-id="bba82-347">Run the ER format</span></span>

<span data-ttu-id="bba82-348">Pakartoję ankstesniame šios temos skyriuje [ER formato vykdymas](#run-format) nurodytus veiksmus sugeneruokite naują našumo sekimą.</span><span class="sxs-lookup"><span data-stu-id="bba82-348">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="bba82-349">Atkreipkite dėmesį, kad interneto naršyklėje siūloma atsisiųsti ZIP failą.</span><span class="sxs-lookup"><span data-stu-id="bba82-349">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="bba82-350">Šiame faile pateikiamas našumo sekimas PerfView formatu.</span><span class="sxs-lookup"><span data-stu-id="bba82-350">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="bba82-351">Naudodamiesi PerfView našumo analizės įrankiu galite išanalizuoti informaciją apie ER formato vykdymą.</span><span class="sxs-lookup"><span data-stu-id="bba82-351">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![Našumo sekimo informacija „PerfView” formatu](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="bba82-353">Norėdami peržiūrėti vykdymo sekimą, apimantį duomenų bazės užklausas, naudokite išorinius įrankius</span><span class="sxs-lookup"><span data-stu-id="bba82-353">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="bba82-354">Dėl patobulinimų, atliktų ER sistemoje, efektyvumo sekimo duomenys, sugeneruoti „PerfView“ formatu, dabar teikia daugiau išsamios informacijos apie ER formato vykdymą.</span><span class="sxs-lookup"><span data-stu-id="bba82-354">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="bba82-355">Naudojant „Microsoft Dynamics 365 for Finance and Operations“ 10.0.4 versiją (2019 m. liepos mėn.), šiuose sekimo duomenyse taip pat gali būti pateikiama informacija apie vykdytas SQL užklausas į programos duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="bba82-355">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="bba82-356">Vartotojo parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="bba82-356">Configure user parameters</span></span>

1. <span data-ttu-id="bba82-357">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="bba82-357">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="bba82-358">Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="bba82-358">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="bba82-359">Dialogo lango **Vartotojo parametrai** skyriuje **Vykdymo sekimas** nustatykite toliau nurodytus parametrus.</span><span class="sxs-lookup"><span data-stu-id="bba82-359">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="bba82-360">Lauke **Vykdymo sekimo formatas** pasirinkite **„PerfView“ XML**.</span><span class="sxs-lookup"><span data-stu-id="bba82-360">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="bba82-361">Nustatykite parinkties **Rinkti užklausų statistiką** reikšmę **Taip**.</span><span class="sxs-lookup"><span data-stu-id="bba82-361">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="bba82-362">Nustatykite parinkties **Įjungti profilį** reikšmę **Taip**.</span><span class="sxs-lookup"><span data-stu-id="bba82-362">Set the **Trace query** option to **Yes**.</span></span>

    ![Skyrius Vykdymo sekimas, dialogo langas Vartotojo parametrai](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="bba82-364">ER formato vykdymas</span><span class="sxs-lookup"><span data-stu-id="bba82-364">Run the ER format</span></span>

<span data-ttu-id="bba82-365">Pakartoję ankstesniame šios temos skyriuje [ER formato vykdymas](#run-format) nurodytus veiksmus sugeneruokite naują našumo sekimą.</span><span class="sxs-lookup"><span data-stu-id="bba82-365">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="bba82-366">Atkreipkite dėmesį, kad interneto naršyklėje siūloma atsisiųsti ZIP failą.</span><span class="sxs-lookup"><span data-stu-id="bba82-366">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="bba82-367">Šiame faile pateikiamas našumo sekimas PerfView formatu.</span><span class="sxs-lookup"><span data-stu-id="bba82-367">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="bba82-368">Naudodamiesi PerfView našumo analizės įrankiu galite išanalizuoti informaciją apie ER formato vykdymą.</span><span class="sxs-lookup"><span data-stu-id="bba82-368">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="bba82-369">Dabar šis sekimas apims informaciją apie SQL duomenų bazės prieigą vykdant ER formatą.</span><span class="sxs-lookup"><span data-stu-id="bba82-369">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![Įvykdyto ER formato informacijos sekimas naudojant „PerfView“](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a><span data-ttu-id="bba82-371">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="bba82-371">Additional resources</span></span>

- [<span data-ttu-id="bba82-372">Elektroninių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="bba82-372">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="bba82-373">ER sprendimų našumo didinimas įtraukiant parametrizuotų duomenų šaltinių APSKAIČIUOTAS LAUKAS</span><span class="sxs-lookup"><span data-stu-id="bba82-373">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
