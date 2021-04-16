---
title: „Regression Suite Automation Tool“ mokymo programos nustatymas ir įdiegimas
description: Šioje temoje mokoma, kaip nustatyti ir įdiegti „Regression suite automation tool“ (RSAT).
author: robinarh
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 725bce4b3aa7feb61bd7d7ded1be07f803424e57
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745202"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="758ac-103">„Regression Suite Automation Tool“ mokymo programos nustatymas ir įdiegimas</span><span class="sxs-lookup"><span data-stu-id="758ac-103">Set up and install Regression suite automation tool tutorial</span></span>

<span data-ttu-id="758ac-104">Ši tema yra mokomoji programa, kuri padeda nustatyti ir pradėti darbą su RSAT ir įrankiais, susietais su RSAT.</span><span class="sxs-lookup"><span data-stu-id="758ac-104">This topic is a tutorial that helps you get setup and get started with RSAT and the tools associated with using RSAT.</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="758ac-105">Naudodamiesi interneto naršyklės įrankiais atsisiųskite ir įrašykite šį puslapį PDF formatu.</span><span class="sxs-lookup"><span data-stu-id="758ac-105">Use your internet browser tools to download and save this page in PDF format.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="758ac-106">Pagrindinės koncepcijos</span><span class="sxs-lookup"><span data-stu-id="758ac-106">Key concepts</span></span>

- <span data-ttu-id="758ac-107">Supraskite diegimo ir būtinųjų komponentų sąranką, kurios reikia įvairioms programoms, palaikančioms „Regression suite automation tool“ (RSAT).</span><span class="sxs-lookup"><span data-stu-id="758ac-107">Understand the installation and prerequisite setup that are required for the various applications that support Regression suite automation tool (RSAT).</span></span>
- <span data-ttu-id="758ac-108">Sužinokite, kaip užduočių įrašymo priemonės funkcija kartu su „Microsoft Dynamics Lifecycle Services“ (LCS) ir „Microsoft Azure DevOps“ leidžia kurti, konfigūruoti, vykdyti, tirti ir pateikti testavimo atvejų ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="758ac-108">Understand how the Task recorder feature, together with Microsoft Dynamics Lifecycle Services (LCS) and Microsoft Azure DevOps, let you create, configure, run, investigate, and report on test cases.</span></span>
- <span data-ttu-id="758ac-109">Įgalinkite funkcinius vartotojus įrašyti verslo užduotis naudojant užduočių įrašymo priemonę ir konvertuoti užduočių įrašus į automatinių testų paketą nereikalaujant rašyti pirminio kodo.</span><span class="sxs-lookup"><span data-stu-id="758ac-109">Empower functional users to record business tasks by using Task recorder, and then convert the task recordings into a suite of automated tests, without having to write source code.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="758ac-110">Prieš pradedant</span><span class="sxs-lookup"><span data-stu-id="758ac-110">Before you begin</span></span>

### <a name="prerequisites"></a><span data-ttu-id="758ac-111">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="758ac-111">Prerequisites</span></span>

- <span data-ttu-id="758ac-112">Norint paleisti šią mokymo programą reikia aplinkos, kurioje veiktų „Microsoft Dynamics 365 for Finance and Operations“ 10.0 (2019 m. balandžio mėn.) arba naujesnė versija.</span><span class="sxs-lookup"><span data-stu-id="758ac-112">An environment that runs Microsoft Dynamics 365 for Finance and Operations version 10.0 (April 2019) or later is required for this tutorial.</span></span> <span data-ttu-id="758ac-113">Klientai, naudojantys „Microsoft Dynamics 365 for Finance and Operations“, gali naudotis ir „Enterprise Edition 7.3“, „Platform Update 20“ (PU20) arba naujesnes versijas.</span><span class="sxs-lookup"><span data-stu-id="758ac-113">For customers who are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, Platform update 20 (PU20) or later is also supported.</span></span>
- <span data-ttu-id="758ac-114">Vartotojas turi turėti administratoriaus teises į šią aplinką.</span><span class="sxs-lookup"><span data-stu-id="758ac-114">The user must have admin rights to the environment.</span></span>
- <span data-ttu-id="758ac-115">Turite turėti prieigą prie kliento nuomotojo LCS ir „Azure DevOps“ (anksčiau žinomos kaip „Microsoft Visual Studio Team Services“ \[VSTS\]).</span><span class="sxs-lookup"><span data-stu-id="758ac-115">You must have access to the customer tenant LCS and Azure DevOps (previously known as Microsoft Visual Studio Team Services \[VSTS\]).</span></span>
- <span data-ttu-id="758ac-116">Vartotojas, kuris kuria ir valdo testavimo paketus, turi turėti „Azure DevOps“ testavimo planavimo arba testavimo vadovo licenciją.</span><span class="sxs-lookup"><span data-stu-id="758ac-116">The user that is creating and managing tests suites must have an Azure DevOps Test Plans or Test Manager license.</span></span> <span data-ttu-id="758ac-117">Šios licencijos irgi suteikia prieigą prie testavimo planų:</span><span class="sxs-lookup"><span data-stu-id="758ac-117">The following licenses will also give you access to Test Plans:</span></span>
    - <span data-ttu-id="758ac-118">„Visual Studio Enterprise“ licencija</span><span class="sxs-lookup"><span data-stu-id="758ac-118">Visual Studio Enterprise license</span></span>
    - <span data-ttu-id="758ac-119">„Visual Studio Test Professional“ licencija</span><span class="sxs-lookup"><span data-stu-id="758ac-119">Visual Studio Test Professional license</span></span>
    - <span data-ttu-id="758ac-120">MSDN platformų prenumeratoriaus licencija</span><span class="sxs-lookup"><span data-stu-id="758ac-120">MSDN Platforms subscriber license</span></span>
- <span data-ttu-id="758ac-121">RSAT turi turėti prieigą prie testavimo aplinkos per interneto naršyklę.</span><span class="sxs-lookup"><span data-stu-id="758ac-121">RSAT must have access to the test environment via a web browser.</span></span>
- <span data-ttu-id="758ac-122">Norėdami sugeneruoti ir redaguoti testavimo parametrus, turite būti įdiegę „Microsoft Excel“.</span><span class="sxs-lookup"><span data-stu-id="758ac-122">To generate and edit test parameters, you must have Microsoft Excel installed.</span></span>

## <a name="configure-azure-devops"></a><span data-ttu-id="758ac-123">Konfigūruoti „Azure DevOps“</span><span class="sxs-lookup"><span data-stu-id="758ac-123">Configure Azure DevOps</span></span>

### <a name="user-eligibility"></a><span data-ttu-id="758ac-124">Vartotojo tinkamumas</span><span class="sxs-lookup"><span data-stu-id="758ac-124">User eligibility</span></span>

<span data-ttu-id="758ac-125">Įsitikinkite, kad vartotojas yra sukurtas „Azure DevOps“ ir turi prenumeratos lygį, kuris suteikia prieigą prie „Azure“ testavimo planų.</span><span class="sxs-lookup"><span data-stu-id="758ac-125">Make sure that the user is created in Azure DevOps and has a subscription level that provides access to Azure Test Plans.</span></span> <span data-ttu-id="758ac-126">„Azure DevOps“ testavimo planų licencija reikalinga tik tada, kai vartotojas sukurs ir tvarkys testavimo atvejus (t. y. ne visi RSAT vartotojai turi turėti šią licenciją).</span><span class="sxs-lookup"><span data-stu-id="758ac-126">An Azure DevOps Test Plans license is required only if the user will create and manage test cases (that is, not all RSAT users require this license).</span></span> <span data-ttu-id="758ac-127">Norėdami gauti informacijos apie licencijos reikalavimus, žr. [Licencijos reikalavimai](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).</span><span class="sxs-lookup"><span data-stu-id="758ac-127">For information about the license requirements, see [License requirements](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).</span></span>

### <a name="create-a-new-azure-devops-project"></a><span data-ttu-id="758ac-128">Naujo „Azure DevOps“ projekto kūrimas</span><span class="sxs-lookup"><span data-stu-id="758ac-128">Create a new Azure DevOps project</span></span>

<span data-ttu-id="758ac-129">RSAT naudoja „Azure DevOps“ testavimo atvejams ir testavimo paketui valdyti, ataskaitoms ir testavimo vykdymo rezultatų analizei.</span><span class="sxs-lookup"><span data-stu-id="758ac-129">RSAT uses Azure Devops for test case and test suite management, reporting, and investigating test run results.</span></span>

> [!NOTE]
> <span data-ttu-id="758ac-130">Galite naudoti esamą „Azure DevOps“ projektą.</span><span class="sxs-lookup"><span data-stu-id="758ac-130">You can use an existing Azure DevOps project.</span></span> <span data-ttu-id="758ac-131">Tačiau, jei jūsų esamas „Azure DevOps“ projektas nustatytas taip, kad jis būtų su pasirinktiniu šablonu, jums bus parodytas klaidos pranešimas VSTS sinchronizavimo triktis, kai sinchronizuojate testavimo atvejus iš verslo procesų modeliavimo įrankio (BPM) su „Azure DevOps“ (žr. skyrių [Sinchronizavimo iš BPM su „Azure DevOps“ testavimas](#test-the-synchronization-from-bpm-to-azure-devops)).</span><span class="sxs-lookup"><span data-stu-id="758ac-131">However, if your existing Azure DevOps project is set up so that it has a custom template, you will receive a "VSTS Sync Failure" error when you sync test cases from Business process modeler (BPM) to Azure DevOps (see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section).</span></span> <span data-ttu-id="758ac-132">Jei pasirinktiniam šablonui pritaikytos šios geriausios praktikos, galėsite sinchronizuoti testavimo atvejus su „Azure DevOps“.</span><span class="sxs-lookup"><span data-stu-id="758ac-132">If the following best practices have been followed for the custom template, you will be able to sync the test cases to Azure DevOps.</span></span> <span data-ttu-id="758ac-133">(Šie geriausios praktikos pavyzdžiai pateikti klaidos pranešime.)</span><span class="sxs-lookup"><span data-stu-id="758ac-133">(These best practices are listed in the error message.)</span></span>

- <span data-ttu-id="758ac-134">Nepanaikinkite jokių darbo elementų tipų ar netipinių laukų.</span><span class="sxs-lookup"><span data-stu-id="758ac-134">Do not delete any work item types or out-of-the-box fields.</span></span>
- <span data-ttu-id="758ac-135">Nepanaikinkite jokių darbo elemento tipo būsenų.</span><span class="sxs-lookup"><span data-stu-id="758ac-135">Do not delete any state of a work item type.</span></span>
- <span data-ttu-id="758ac-136">Į darbo elemento tipą neįtraukite jokių privalomų laukų.</span><span class="sxs-lookup"><span data-stu-id="758ac-136">Do not add any required fields to a work item type.</span></span>

![Klaidos pranešimas, kuriame pateikiamas geriausios praktikos pavyzdžių sąrašas](./media/setup_rsa_tool_02.png)

<span data-ttu-id="758ac-138">Kitu atveju pagal šią mokomąją programą rekomenduojame sukurti naują „Azure DevOps“ projektą.</span><span class="sxs-lookup"><span data-stu-id="758ac-138">Otherwise, for this tutorial, we recommend that you create a new Azure DevOps project.</span></span> <span data-ttu-id="758ac-139">Norėdami gauti daugiau informacijos, žr. [Problemos, kylančios sinchronizuojant su BPM naudojant pasirinktinį „Azure DevOps“ (VSTS proceso šabloną](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/)).</span><span class="sxs-lookup"><span data-stu-id="758ac-139">For more information, see [Issues when syncing to BPM using a custom Azure DevOps (VSTS) process template](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span></span>

1. <span data-ttu-id="758ac-140">Atidarykite „Azure DevOps“ URL (`https://dev.azure.com/<Azure DevOps Name>`).</span><span class="sxs-lookup"><span data-stu-id="758ac-140">Open the Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).</span></span>
2. <span data-ttu-id="758ac-141">Pasirinkite **Kurti projektą** viršutiniame dešiniajame „Azure DevOps“ puslapio kampe.</span><span class="sxs-lookup"><span data-stu-id="758ac-141">Select **Create project** in the upper-right corner of the Azure DevOps page.</span></span>

    ![Projekto kūrimo mygtukas](./media/setup_rsa_tool_03.png)

3. <span data-ttu-id="758ac-143">Užpildykite šiuos laukus ir pasirinkite **Kurti**:</span><span class="sxs-lookup"><span data-stu-id="758ac-143">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="758ac-144">**Projekto pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="758ac-144">**Project name**</span></span>
    - <span data-ttu-id="758ac-145">**Versijų valdymas** – pasirinkite **Team Foundation Version Control**.</span><span class="sxs-lookup"><span data-stu-id="758ac-145">**Version control** – Select **Team Foundation Version Control**.</span></span> <span data-ttu-id="758ac-146">Atkreipkite dėmesį, kad numatytoji parinktis **Git** nepalaikoma.</span><span class="sxs-lookup"><span data-stu-id="758ac-146">Note that the default option, **Git**, isn't supported.</span></span>
    - <span data-ttu-id="758ac-147">**Darbo elemento apdorojimas**</span><span class="sxs-lookup"><span data-stu-id="758ac-147">**Work item process**</span></span>

    ![Naujo projekto kūrimo dialogo langas](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a><span data-ttu-id="758ac-149">Asmeninės prieigos atpažinimo ženklo kūrimas</span><span class="sxs-lookup"><span data-stu-id="758ac-149">Create a personal access token</span></span>

<span data-ttu-id="758ac-150">Šiojo mokymo programoje naudosite LCS verslo procesų modeliavimo įrankį (BPM) ir kursite testavimo atvejų biblioteką bei sinchronizuosite testavimo atvejus su „Azure DevOps“.</span><span class="sxs-lookup"><span data-stu-id="758ac-150">In this tutorial, you will use the LCS Business Process Modeler (BPM) to create a test case library and synchronize your test cases with Azure DevOps.</span></span> <span data-ttu-id="758ac-151">Jums reikės asmeninės prieigos atpažinimo ženklo, kad galėtumėte sinchronizuoti BPM su „Azure DevOps“.</span><span class="sxs-lookup"><span data-stu-id="758ac-151">You will need a personal access token to sync BPM with Azure DevOps.</span></span>

1. <span data-ttu-id="758ac-152">„Azure DevOps“ projekto puslapio viršutiniame dešiniajame kampe pasirinkite profilio piktogramą, tada pasirinkite **Sauga**.</span><span class="sxs-lookup"><span data-stu-id="758ac-152">Select the profile icon in the upper-right corner of the page for your Azure DevOps project, and then select **Security**.</span></span>

    ![Saugos komanda](./media/setup_rsa_tool_05.png)

2. <span data-ttu-id="758ac-154">Kairiojoje srityje, dalyje **Sauga**, pasirinkite **Asmeninės prieigos atpažinimo ženklai**.</span><span class="sxs-lookup"><span data-stu-id="758ac-154">In the left pane, under **Security**, select **Personal access tokens**.</span></span> <span data-ttu-id="758ac-155">Tada pasirinkite **Naujas atpažinimo ženklas**.</span><span class="sxs-lookup"><span data-stu-id="758ac-155">Then select **New Token**.</span></span>

    ![Naujo atpažinimo ženklo mygtukas, esantis vartotojo parametrų skirtuke Asmeninės prieigos atpažinimo ženklai](./media/setup_rsa_tool_06.png)

3. <span data-ttu-id="758ac-157">Užpildykite šiuos laukus ir pasirinkite **Kurti**:</span><span class="sxs-lookup"><span data-stu-id="758ac-157">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="758ac-158">**Pavadinimas / vardas ir (arba) pavardė**</span><span class="sxs-lookup"><span data-stu-id="758ac-158">**Name**</span></span>
    - <span data-ttu-id="758ac-159">**Galiojimo laikas (UTC)** – pasirinkite **Pasirinktinis**, o tada naudokite datos parinkiklį, kad pasirinktumėte paskutinę galimą datą.</span><span class="sxs-lookup"><span data-stu-id="758ac-159">**Expiration (UTC)** – Select **Custom defined**, and then use the date picker to select the last available date.</span></span>
    - <span data-ttu-id="758ac-160">**Aprėptis** – pasirinkite parinktį **Visa prieiga**.</span><span class="sxs-lookup"><span data-stu-id="758ac-160">**Scopes** – Select the **Full access** option.</span></span>

    ![Naujo asmeninės prieigos atpažinimo ženklo kūrimo dialogo langas](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > <span data-ttu-id="758ac-162">Pasižymėkite sukurtą asmeninės prieigos atpažinimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="758ac-162">Make a note of the personal access token that is created.</span></span> <span data-ttu-id="758ac-163">Jums jo reikės vėliau nustačius RSAT konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="758ac-163">You will need it later when you set up the RSAT configuration.</span></span>

    ![Asmeninės prieigos atpažinimo ženklas](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a><span data-ttu-id="758ac-165">LCS projekto konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="758ac-165">Configure the LCS project</span></span>

<span data-ttu-id="758ac-166">Turite turėti „Lifecycle Services“ (LCS) projektą pagrindinei testavimo bibliotekai.</span><span class="sxs-lookup"><span data-stu-id="758ac-166">You need a Lifecycle Services (LCS) project for your master test library.</span></span> <span data-ttu-id="758ac-167">LCS verslo procesų modeliavimo įrankis (BPM) naudojamas kaip pagrindinė jūsų testavimo atvejų biblioteka.</span><span class="sxs-lookup"><span data-stu-id="758ac-167">The LCS Business Process Modeler (BPM) is used as the master library for your test cases.</span></span> <span data-ttu-id="758ac-168">BPM naudojamas testavimo bibliotekoms valdyti ir paskirstyti po LCS projektus.</span><span class="sxs-lookup"><span data-stu-id="758ac-168">BPM is used to manage and distribute test libraries across LCS projects.</span></span> <span data-ttu-id="758ac-169">Pavyzdžiui, „Microsoft“ partnerio arba nepriklausomo programinės įrangos tiekėjo (ISV) kūrimo testavimo bibliotekos pateiks testavimo atvejus BPM bibliotekų forma.</span><span class="sxs-lookup"><span data-stu-id="758ac-169">For example, a Microsoft partner or independent software vendor (ISV) building test libraries will release test cases in the form of BPM libraries.</span></span> <span data-ttu-id="758ac-170">Naudojant BPM testavimo atvejai tvarkomi pagal verslo procesą.</span><span class="sxs-lookup"><span data-stu-id="758ac-170">In BPM, test cases are organized by business process.</span></span> <span data-ttu-id="758ac-171">BPM nenustato vykdymo tvarkos ar teigiamų testavimo rezultatų dažnumo.</span><span class="sxs-lookup"><span data-stu-id="758ac-171">BPM doesn't define the execution order or frequency of your test pass.</span></span> <span data-ttu-id="758ac-172">Šie duomenys valdomi „Azure DevOps“, kaip aprašyta toliau šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="758ac-172">These details are managed in Azure DevOps, as described later in this topic.</span></span>  

<span data-ttu-id="758ac-173">Savo LCS projektui galite naudoti esamą klientų įdiegimo arba partnerių projektą.</span><span class="sxs-lookup"><span data-stu-id="758ac-173">For your LCS project, you can use an existing customer implementation or partner project.</span></span>

### <a name="update-the-lcs-language"></a><span data-ttu-id="758ac-174">LCS kalbos naujinimas</span><span class="sxs-lookup"><span data-stu-id="758ac-174">Update the LCS language</span></span>

> [!NOTE]
> <span data-ttu-id="758ac-175">Norint tinkamai parodyti verslo procesus vartotojo sąsajoje (UI) turi būti nustatyta LCS pageidaujama kalba **anglų (Jungtinės Valstijos)**.</span><span class="sxs-lookup"><span data-stu-id="758ac-175">For the user interface (UI) to correctly show business processes, the LCS preferred language must be set to **English (United States)**.</span></span>

1. <span data-ttu-id="758ac-176">Eikite į LCS diegimo projektą.</span><span class="sxs-lookup"><span data-stu-id="758ac-176">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="758ac-177">Paspauskite viršutiniame dešiniajame puslapio kampe esantį mygtuką **Parametrai** (krumpliaračio simbolis), o paskui pasirinkite **Kalbos nuostata**.</span><span class="sxs-lookup"><span data-stu-id="758ac-177">Select the **Settings** button (the gear symbol) in the upper-right corner, and then select **Language preference**.</span></span>

    ![Kalbos nuostatų atnaujinimas](./media/setup_rsa_tool_09.png)

3. <span data-ttu-id="758ac-179">Lauke **Pageidaujama kalba** pasirinkite **anglų (Jungtinės Valstijos)**, tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-179">In the **Preferred language** field, select **English (United States)**, and then select **Save**.</span></span>

    ![Vartotojo parametrų skirtukas Kalbos nuostata](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a><span data-ttu-id="758ac-181">LCS konfigūravimas, kad būtų galima prisijungti prie „Azure DevOps“ projekto</span><span class="sxs-lookup"><span data-stu-id="758ac-181">Configure LCS to connect to the Azure DevOps project</span></span>

<span data-ttu-id="758ac-182">Jeigu anksčiau sukūrėte naują „Azure DevOps“ projektą, konfigūruokite LCS projektą, kad prie jo galėtumėte prisijungti.</span><span class="sxs-lookup"><span data-stu-id="758ac-182">If you created a new Azure DevOps project earlier, configure the LCS project to connect to it.</span></span> <span data-ttu-id="758ac-183">Arba jei jūsų LCS projektas jau prijungtas prie jūsų „Azure DevOps“ projekto, galite pereiti prie kito skyriaus.</span><span class="sxs-lookup"><span data-stu-id="758ac-183">Otherwise, if your LCS project is already connected to your Azure DevOps project, you can continue to the next section.</span></span>

1. <span data-ttu-id="758ac-184">Eikite į LCS diegimo projektą.</span><span class="sxs-lookup"><span data-stu-id="758ac-184">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="758ac-185">Pasirinkite mygtuką **Meniu**, tada pasirinkite **Projekto parametrai**.</span><span class="sxs-lookup"><span data-stu-id="758ac-185">Select the **Menu** button, and then select **Project settings**.</span></span>

    ![Komanda Projekto parametrai](./media/setup_rsa_tool_11.png)

3. <span data-ttu-id="758ac-187">Kairiojoje srityje pasirinkite **Visual Studio Team Services**, tada pasirinkite **Nustatyti „Visual Studio Team Services“**.</span><span class="sxs-lookup"><span data-stu-id="758ac-187">In the left pane, select **Visual Studio Team Services**, and then select **Setup Visual Studio Team Services**.</span></span>

    ![Skirtukas „Visual Studio Team Services“ projekto parametruose](./media/setup_rsa_tool_12.png)

4. <span data-ttu-id="758ac-189">Lauke **Azure DevOps svetainės URL** įveskite „Azure DevOps“ svetainės URL.</span><span class="sxs-lookup"><span data-stu-id="758ac-189">In the **Azure DevOps site URL** field, enter the URL of the Azure DevOps site.</span></span> <span data-ttu-id="758ac-190">Lauke **Asmeninės prieigos atpažinimo ženklas** įveskite anksčiau sukurtą asmeninį prieigos atpažinimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="758ac-190">In the **Personal access token** field, enter the personal access token that was created earlier.</span></span>

    > [!NOTE]
    > <span data-ttu-id="758ac-191">Nors VSTS dabar žinoma kaip „Azure DevOps“, norėdami sujungti LCS su savo „Azure DevOps“ projektu, naudokite seną URL.</span><span class="sxs-lookup"><span data-stu-id="758ac-191">Although VSTS is now known as Azure DevOps, to connect LCS to your Azure DevOps project, use the old URL.</span></span> <span data-ttu-id="758ac-192">Pavyzdžiui, šioje mokymo programoje „Azure DevOps“ naudojamas URL yra `https://dev.azure.com/D365FOFastTrack/`.</span><span class="sxs-lookup"><span data-stu-id="758ac-192">For example, the Azure DevOps URL that is used in this tutorial is `https://dev.azure.com/D365FOFastTrack/`.</span></span> <span data-ttu-id="758ac-193">Tačiau šioje iliustracijoje jis įvestas kaip `https://D365FOFastTrack.visualstudio.com/`.</span><span class="sxs-lookup"><span data-stu-id="758ac-193">However, in the following illustration, it's entered as `https://D365FOFastTrack.visualstudio.com/`.</span></span>

    ![1 „Visual Studio Team Services“ nustatymo veiksmas](./media/setup_rsa_tool_13.png)

5. <span data-ttu-id="758ac-195">Pasirinkite **Tęsti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-195">Select **Continue**.</span></span>
6. <span data-ttu-id="758ac-196">Lauke **„Visual Studio Team Services“ projektas** pasirinktoje svetainėje pasirinkite VSTS projektą, kurį norite susieti su LCS projektu.</span><span class="sxs-lookup"><span data-stu-id="758ac-196">In the **Visual Studio Team Services project** field, select the VSTS project on the selected site to link with the LCS project.</span></span> <span data-ttu-id="758ac-197">Pagal numatytuosius parametrus lauko **Proceso šablonas** reikšmė yra **Agile**.</span><span class="sxs-lookup"><span data-stu-id="758ac-197">The **Process template** field is set to **Agile** by default.</span></span> <span data-ttu-id="758ac-198">Norėdami naudoti pasirinktinį šabloną, peržiūrėkite geriausios praktikos gaires, esančias skyriuje [Naujo „Azure DevOps“ projekto kūrimas](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="758ac-198">For a custom template, review the best practice guidance in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span> <span data-ttu-id="758ac-199">Tada pasirinkite **Tęsti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-199">Then select **Continue**.</span></span>

    ![2 „Visual Studio Team Services“ nustatymo veiksmas](./media/setup_rsa_tool_14.png)

7. <span data-ttu-id="758ac-201">Peržiūrėti parametrus ir pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-201">Review your settings, and then select **Save**.</span></span>

    ![3 „Visual Studio Team Services“ nustatymo veiksmas](./media/setup_rsa_tool_15.png)

8. <span data-ttu-id="758ac-203">Pasirinkite **Įgalioti**, kad leistumėte LCS pasiekti sukonfigūruotą „Azure DevOps“ svetainę jūsų vardu ir įjungti funkcijas, kurios integruoja su VSTS.</span><span class="sxs-lookup"><span data-stu-id="758ac-203">Select **Authorize** to authorize LCS to access the configured Azure DevOps site on your behalf and to turn on features that integrate with VSTS.</span></span>

    ![Mygtukas Įgalioti](./media/setup_rsa_tool_16.png)

9. <span data-ttu-id="758ac-205">Parodomas pranešimas: „Būsite nukreipti į vietinę svetainę, kad būtų galima įgalioti LCS prisijungti prie „Visual Studio Team Services“ jūsų vardu.</span><span class="sxs-lookup"><span data-stu-id="758ac-205">A message box appears that states, "You are about to be redirected to an eternal site to authorize LCS to connect to Visual Studio Team Services on your behalf.</span></span> <span data-ttu-id="758ac-206">Tęsti?“</span><span class="sxs-lookup"><span data-stu-id="758ac-206">Proceed?"</span></span> <span data-ttu-id="758ac-207">Pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="758ac-207">Select **Yes**.</span></span>

    ![Pranešimo laukas](./media/setup_rsa_tool_17.png)

10. <span data-ttu-id="758ac-209">Pasirinkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-209">Select **Accept**.</span></span>

    ![Prieigos įgaliojimas](./media/setup_rsa_tool_18.png)

11. <span data-ttu-id="758ac-211">Jei esate įgaliotas kaip vartotojas, UI jus grąžins į LCS projekto parametrų puslapį.</span><span class="sxs-lookup"><span data-stu-id="758ac-211">If you're authorized as a user, the UI should you return to the LCS project settings page.</span></span>

    ![Įgaliotasis vartotojas](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a><span data-ttu-id="758ac-213">Naujos BPM bibliotekos kūrimas</span><span class="sxs-lookup"><span data-stu-id="758ac-213">Create a new BPM library</span></span>

1. <span data-ttu-id="758ac-214">Eikite į LCS diegimo projektą.</span><span class="sxs-lookup"><span data-stu-id="758ac-214">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="758ac-215">Pasirinkite mygtuką **Meniu**, tada pasirinkite **Verslo procesų modeliavimo įrankis**.</span><span class="sxs-lookup"><span data-stu-id="758ac-215">Select the **Menu** button, and then select **Business process modeler**.</span></span>

    ![Komanda Verslo procesų modeliavimo įrankis](./media/setup_rsa_tool_20.png)

3. <span data-ttu-id="758ac-217">Pasirinkite **Nauja biblioteka**.</span><span class="sxs-lookup"><span data-stu-id="758ac-217">Select **New library**.</span></span>

    ![Mygtukas Nauja biblioteka](./media/setup_rsa_tool_21.png)

4. <span data-ttu-id="758ac-219">Lauke **Bibliotekos pavadinimas** įveskite pavadinimą ir pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-219">In the **Library name** field, enter a name, and then select **Create**.</span></span> <span data-ttu-id="758ac-220">Šioje mokomojoje programoje pavadinkite BPM biblioteką **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="758ac-220">For this tutorial, name the BPM library **RSAT**.</span></span>

    ![Naujos bibliotekos kūrimo dialogo langas](./media/setup_rsa_tool_22.png)

5. <span data-ttu-id="758ac-222">Atidarykite naują **RSAT** BPM biblioteką.</span><span class="sxs-lookup"><span data-stu-id="758ac-222">Open the new **RSAT** BPM library.</span></span>
6. <span data-ttu-id="758ac-223">Pasirinkite procesą **Pavyzdinis pagrindinio verslo procesas**, tada dešinėje pusėje pasirinkite **Redagavimo režimas**.</span><span class="sxs-lookup"><span data-stu-id="758ac-223">Select the **Sample Core Business Process** process, and then, on the right, select **Edit mode**.</span></span>

    ![Mygtukas Redagavimo režimas](./media/setup_rsa_tool_23.png)

7. <span data-ttu-id="758ac-225">Pakeiskite abiejų laukų **Pavadinimas** ir **Aprašas** reikšmes, kad **sukurtumėte produktą**.</span><span class="sxs-lookup"><span data-stu-id="758ac-225">Change the value of both the **Name** field and the **Description** field to **Create a product**.</span></span> <span data-ttu-id="758ac-226">Tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-226">Then select **Save**.</span></span>

    ![Laukai Pavadinimas ir Aprašas](./media/setup_rsa_tool_24.png)

## <a name="environment"></a><span data-ttu-id="758ac-228">Aplinka</span><span class="sxs-lookup"><span data-stu-id="758ac-228">Environment</span></span>

### <a name="version-requirement"></a><span data-ttu-id="758ac-229">Versijos reikalavimas</span><span class="sxs-lookup"><span data-stu-id="758ac-229">Version requirement</span></span>

<span data-ttu-id="758ac-230">Būtina turėti testavimo ar smėlio dėžės aplinką, kurioje veikia 10 versija.</span><span class="sxs-lookup"><span data-stu-id="758ac-230">A test or sandbox environment that runs version 10 is required.</span></span> <span data-ttu-id="758ac-231">Klientai, naudojantys 7.3 versiją, gali naudotis ir „Platform Update 20“ arba naujesnes versijas.</span><span class="sxs-lookup"><span data-stu-id="758ac-231">For customers that are using version 7.3, Platform update 20 or later is also supported.</span></span>

> [!NOTE]
> <span data-ttu-id="758ac-232">RSAT turi turėti prieigą prie jūsų testavimo aplinkos per interneto naršyklę.</span><span class="sxs-lookup"><span data-stu-id="758ac-232">RSAT must have access to your test environment via a web browser.</span></span>

### <a name="user-criteria"></a><span data-ttu-id="758ac-233">Vartotojo kriterijai</span><span class="sxs-lookup"><span data-stu-id="758ac-233">User criteria</span></span>

<span data-ttu-id="758ac-234">Vartotojas turi turėti administratoriaus teises į šią aplinką.</span><span class="sxs-lookup"><span data-stu-id="758ac-234">The user must have admin rights to this environment.</span></span>

### <a name="set-up-help-settings-to-connect-with-lcs"></a><span data-ttu-id="758ac-235">Žinyno parametrų, kad būtų galima prisijungti prie LCS, nustatymas</span><span class="sxs-lookup"><span data-stu-id="758ac-235">Set up Help settings to connect with LCS</span></span>

<span data-ttu-id="758ac-236">Šis veiksmas reikalingas, kad būtų galima prisijungti prie LCS, kad užduoties įrašus būtų galima įrašyti į atitinkamą BPM biblioteką, esančią LCS, naudojant klientą.</span><span class="sxs-lookup"><span data-stu-id="758ac-236">This step is required in order to connect with LCS so that task recordings can be saved to the appropriate BPM library in LCS through the client.</span></span>

1. <span data-ttu-id="758ac-237">Atidarykite kliento programą.</span><span class="sxs-lookup"><span data-stu-id="758ac-237">Open the client.</span></span>
2. <span data-ttu-id="758ac-238">Eikite į **Sistemos administravimas \> Sąranka \> Sistemos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="758ac-238">Go to **System Administration \> Setup \> System parameters**.</span></span>
3. <span data-ttu-id="758ac-239">Skirtuko **Žinynas** lauke **„Lifecycle Services“ žinyno konfigūracija** pasirinkite atitinkamą LCS projektą (šioje mokomojoje programoje **RSAT**).</span><span class="sxs-lookup"><span data-stu-id="758ac-239">On the **Help** tab, in the **Lifecycle Services help configuration** field, select the relevant LCS project (**RSAT** for this tutorial).</span></span>

    ![„Lifecycle Services“ žinyno konfigūracijos laukas, esantis žinyno skirtuke](./media/setup_rsa_tool_25.png)

    <span data-ttu-id="758ac-241">BPM bibliotekos yra užpildomos pagal atitinkamą LCS projektą.</span><span class="sxs-lookup"><span data-stu-id="758ac-241">BPM libraries are filled in under the appropriate LCS project.</span></span>

4. <span data-ttu-id="758ac-242">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-242">Select **Save**.</span></span>
5. <span data-ttu-id="758ac-243">Gali reikėti atnaujinti naršyklę, kad pamatytumėte atnaujintą žinyno turinį.</span><span class="sxs-lookup"><span data-stu-id="758ac-243">You might have to refresh the browser to see the updated Help content.</span></span>

    ![Perspėjimas dėl naršyklės atnaujinimo](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a><span data-ttu-id="758ac-245">Užduočių įrašai</span><span class="sxs-lookup"><span data-stu-id="758ac-245">Task recordings</span></span>

> [!NOTE]
> <span data-ttu-id="758ac-246">Įsitikinkite, kad visi jūsų užduočių įrašai prasideda pagrindinėje ataskaitų srityje.</span><span class="sxs-lookup"><span data-stu-id="758ac-246">Make sure that all your task recordings start on the main dashboard.</span></span> <span data-ttu-id="758ac-247">Atskirus įrašus saugokite trumpai ir sutelkti dėmesį į vieną verslo užduotį, pvz., pardavimo užsakymo kūrimo.</span><span class="sxs-lookup"><span data-stu-id="758ac-247">Keep individual recordings short, and focus on one business task, such as creating a sales order.</span></span>

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a><span data-ttu-id="758ac-248">Užduoties įrašo kūrimas ir įrašymas į BPM biblioteką</span><span class="sxs-lookup"><span data-stu-id="758ac-248">Create a task recording and save it to the BPM library</span></span>

<span data-ttu-id="758ac-249">Kurkite atitinkamus užduoties įrašus, kuriuos galite pridėti prie paprasto verslo proceso, sukurto naujoje BPM bibliotekoje.</span><span class="sxs-lookup"><span data-stu-id="758ac-249">Create a corresponding task recording that you can attach to the simple business process that was created in the new BPM library.</span></span>

1. <span data-ttu-id="758ac-250">Atidarykite kliento programą.</span><span class="sxs-lookup"><span data-stu-id="758ac-250">Open the client.</span></span>
2. <span data-ttu-id="758ac-251">Pagrindinėje ataskaitų srityje pasirinkite mygtuką **Parametrai** (krumpliaračio simbolis), tada pasirinkite **Užduočių įrašymo priemonė**.</span><span class="sxs-lookup"><span data-stu-id="758ac-251">On the main dashboard, select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>

    ![Užduočių įrašymo priemonės iš parametrų meniu pasirinkimas](./media/setup_rsa_tool_27.png)

3. <span data-ttu-id="758ac-253">Pasirinkite **Kurti įrašą**.</span><span class="sxs-lookup"><span data-stu-id="758ac-253">Select **Create recording**.</span></span>

    ![Mygtukas Kurti įrašą](./media/setup_rsa_tool_28.png)

4. <span data-ttu-id="758ac-255">Užpildykite laukus **Įrašo pavadinimas** ir **Įrašo aprašas** ir pasirinkite **Pradėti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-255">Fill in the **Recording name** and **Recording description** fields, and then select **Start**.</span></span>

    ![Laukai Įrašo pavadinimas ir Įrašo aprašas](./media/setup_rsa_tool_29.png)

5. <span data-ttu-id="758ac-257">Įrašykite produkto kūrimo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="758ac-257">Record the steps for creating a product.</span></span> <span data-ttu-id="758ac-258">Baigę pasirinkite **Stabdyti**, kad sustabdytumėte įrašą.</span><span class="sxs-lookup"><span data-stu-id="758ac-258">When you've finished, select **Stop** to stop recording.</span></span>

    ![Produkto kūrimo veiksmai](./media/setup_rsa_tool_30.png)

6. <span data-ttu-id="758ac-260">Pasirinkite **Įrašyti į „Lifecycle Services“**.</span><span class="sxs-lookup"><span data-stu-id="758ac-260">Select **Save to Lifecycle Services**.</span></span>

    ![Užduoties įrašo išsaugojimas į „Lifecycle Services”](./media/setup_rsa_tool_31.png)

    <span data-ttu-id="758ac-262">Bibliotekos informacija įkeliama iš LCS.</span><span class="sxs-lookup"><span data-stu-id="758ac-262">Library information is loaded from LCS.</span></span>

    ![Bibliotekos informacijos įkėlimas](./media/setup_rsa_tool_32.png)

7. <span data-ttu-id="758ac-264">Pasirinkti BPM biblioteką, kurią reikia susieti su užduoties įrašu.</span><span class="sxs-lookup"><span data-stu-id="758ac-264">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="758ac-265">Šioje mokomojoje programoje pasirinkite **RSAT** BPM biblioteką, kuri buvo sukurta anksčiau, ir verslo procesą **Kurti produktą**.</span><span class="sxs-lookup"><span data-stu-id="758ac-265">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Create a product** business process under it.</span></span> <span data-ttu-id="758ac-266">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="758ac-266">Then select **OK**.</span></span>

    ![Užduoties įrašo susiejimas su BPM biblioteka ir verslo procesu](./media/setup_rsa_tool_33.png)

    <span data-ttu-id="758ac-268">Rodomas pranešimas „Įrašyta į „Lifecycle Services“.</span><span class="sxs-lookup"><span data-stu-id="758ac-268">A "Saving to Lifecycle Services was successful" message appears.</span></span>

    ![Pranešimas apie sėkmingą įrašymą į LCS](./media/setup_rsa_tool_34.png)

8. <span data-ttu-id="758ac-270">Jei užduoties įrašą norite įrašyti vietoje, o tada nusiųsti jį į BPM per LCS, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="758ac-270">If you want to save the task recording locally and then upload it to BPM through LCS, follow these steps:</span></span>

    1. <span data-ttu-id="758ac-271">Baigę įrašyti, pasirinkite **Įrašyti į šį kompiuterį**.</span><span class="sxs-lookup"><span data-stu-id="758ac-271">After the recording is completed, select **Save to this PC**.</span></span>

        ![Įrašyti šiame kompiuteryje](./media/setup_rsa_tool_35.png)

    2. <span data-ttu-id="758ac-273">Naršyklės pranešimų juostoje pasirinkite **Įrašyti** arba **Įrašyti kaip**, kad būtų įrašytas failas vietiniame kompiuteryje.</span><span class="sxs-lookup"><span data-stu-id="758ac-273">In the browser's Notification bar, select **Save** or **Save As** to save the file on your local computer.</span></span>

        ![Pranešimų juosta](./media/setup_rsa_tool_36.png)

    3. <span data-ttu-id="758ac-275">Eikite į **RSAT** BPM biblioteką ir pasirinkite verslo procesą, į kurį įrašysite užduoties įrašą.</span><span class="sxs-lookup"><span data-stu-id="758ac-275">Go to the **RSAT** BPM library, and select the business process to save the task recording against.</span></span>
    4. <span data-ttu-id="758ac-276">Skirtuke **Peržiūra** pasirinkite **Nusiųsti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-276">On the **Overview** tab, select **Upload**.</span></span>

        ![Nusiuntimo mygtukas](./media/setup_rsa_tool_37.png)

    5. <span data-ttu-id="758ac-278">Pasirinkite **Naršyti** ir pasirinkite. axtr failą, kurį įrašėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="758ac-278">Select **Browse**, and select the .axtr file that you saved earlier.</span></span> <span data-ttu-id="758ac-279">Tada pasirinkite **Nusiųsti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-279">Then select **Upload**.</span></span>

        ![.axtr failo pasirinkimas nusiųsti](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a><span data-ttu-id="758ac-281">Tikrinti sinchronizavimą iš BPM su „Azure DevOps“</span><span class="sxs-lookup"><span data-stu-id="758ac-281">Test the synchronization from BPM to Azure DevOps</span></span>

<span data-ttu-id="758ac-282">Dabar, kai užduoties įrašas yra pridėtas prie verslo proceso, turite patikrinti, ar verslo procesą ir susietą užduoties įrašą galima sinchronizuoti su „Azure DevOps“ kaip funkciją ir testavimo atvejį (atitinkamai), naudojant VSTS sinchronizavimo funkciją LCS.</span><span class="sxs-lookup"><span data-stu-id="758ac-282">Now that a task recording is attached to the business process, you must validate that the business process and the associated task recording can be synced to Azure DevOps as a feature and a test case (respectively) by using the VSTS sync feature in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="758ac-283">Atitinkamas „Azure DevOps“ sukurtas darbo elemento tipas gali skirtis; jis priklauso nuo proceso šablono, kurį pasirinkote konfigūruodami LCS projektą su „Azure DevOps“, kaip aprašyta skyriuje [Naujo „Azure DevOps“ projekto kūrimas](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="758ac-283">The corresponding work item type that is created in Azure DevOps will vary, depending on the process template that you selected when you configured the LCS project with Azure DevOps, as described in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span>

1. <span data-ttu-id="758ac-284">Eikite į BPM biblioteką ir atidarykite anksčiau sukurtą **RSAT** biblioteką.</span><span class="sxs-lookup"><span data-stu-id="758ac-284">Go to the BPM library, and open the **RSAT** library that you created earlier.</span></span>
2. <span data-ttu-id="758ac-285">Pasirinkite daugtaškio mygtuką (**...**) ir pasirinkite **VSTS sinchronizavimas**.</span><span class="sxs-lookup"><span data-stu-id="758ac-285">Select the ellipsis button (**...**), and select **VSTS sync**.</span></span>

    ![VSTS sinchronizavimo komanda daugtaškio meniu](./media/setup_rsa_tool_39.png)

    <span data-ttu-id="758ac-287">Kai bus baigtas VSTS sinchronizavimas, kairėje pusėje rodomas skirtukas **Reikalavimai**, kuriame yra ir atitinkamas „Azure DevOps“ darbo elementas.</span><span class="sxs-lookup"><span data-stu-id="758ac-287">After VSTS sync is completed, a **Requirements** tab appears on the left side and includes the corresponding Azure DevOps work item.</span></span>

    > [!NOTE]
    > <span data-ttu-id="758ac-288">Darbo elementas, sukurtas „Azure DevOps“, turės BPM bibliotekos pavadinimą kaip pavadinimo prefiksą.</span><span class="sxs-lookup"><span data-stu-id="758ac-288">The work item that is created in Azure DevOps will have the BPM library name as the title prefix.</span></span>

    ![Skirtukas Reikalavimai](./media/setup_rsa_tool_40.png)

3. <span data-ttu-id="758ac-290">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="758ac-290">Refresh the page.</span></span>
4. <span data-ttu-id="758ac-291">Pasirinkite daugtaškio mygtuką (**...**). Matysite papildomą parinktį **Sinchronizuoti testavimo atvejus**.</span><span class="sxs-lookup"><span data-stu-id="758ac-291">Select the ellipsis button (**...**). You will see an additional option, **Sync test cases**.</span></span> <span data-ttu-id="758ac-292">Pasirinkite šią parinktį.</span><span class="sxs-lookup"><span data-stu-id="758ac-292">Select this option.</span></span>

    ![Testavimo atvejų sinchronizavimo komanda daugtaškio meniu](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > <span data-ttu-id="758ac-294">Jei atnaujinus puslapį parinkties **Sinchronizuoti testavimo atvejus** nėra, eikite į pagrindinį BPM puslapį ir pasirinkite visos bibliotekos parinktį **Sinchronizuoti testavimo atvejus**.</span><span class="sxs-lookup"><span data-stu-id="758ac-294">If the **Sync test cases** option isn't available after you refresh the page, go to main page for BPM, and select **Sync test cases** for the whole library itself.</span></span> <span data-ttu-id="758ac-295">Tokiu būdu galite efektyviai vykdyti visos bibliotekos sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="758ac-295">In this way, you effectively force a synchronization for the whole library.</span></span>
    >
    > ![Visos bibliotekos testavimo atvejų sinchronizavimo pasirinkimas](./media/setup_rsa_tool_42.png)

    <span data-ttu-id="758ac-297">Baigus sinchronizuoti testavimo atvejus, skirtuke **Reikalavimai** sukuriamas naujas testavimo atvejis.</span><span class="sxs-lookup"><span data-stu-id="758ac-297">After Sync test cases is completed, a new test case is created on the **Requirements** tab.</span></span>

    ![Naujas testavimo atvejis skirtuke Reikalavimai](./media/setup_rsa_tool_43.png)

5. <span data-ttu-id="758ac-299">Eikite į savo „Azure DevOps“ projektą ir pasirinkite **Sritys \> Darbo elementai**.</span><span class="sxs-lookup"><span data-stu-id="758ac-299">Go to your Azure DevOps project, and select **Boards \> Work Items**.</span></span>

    ![Darbo elementų komanda srityse](./media/setup_rsa_tool_44.png)

6. <span data-ttu-id="758ac-301">Patikrinkite, ar yra darbo elementas ir testavimo atvejis, kuriuos sukūrėte per BPM sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="758ac-301">Validate that the work item and test case that you created through BPM synchronization exist.</span></span>

    ![Darbo elementas ir testavimo atvejis](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a><span data-ttu-id="758ac-303">RSAT konfigūravimas ir diegimas</span><span class="sxs-lookup"><span data-stu-id="758ac-303">Install and Configure RSAT</span></span>

<span data-ttu-id="758ac-304">RSAT galima įdiegti bet kuriame kompiuteryje, kuriame veikia „Windows 10“ ir kuris gali prisijungti prie aplinkos per interneto naršyklę („Internet Explorer“ arba „Google Chrome“).</span><span class="sxs-lookup"><span data-stu-id="758ac-304">RSAT can be installed on any computer that runs Windows 10 and that can connect to the environment via a web browser (Internet Explorer or Google Chrome).</span></span>

> [!NOTE]
> <span data-ttu-id="758ac-305">Prieš diegiant naują įrankio versiją, rekomenduojame pašalinti ankstesnę jo versiją.</span><span class="sxs-lookup"><span data-stu-id="758ac-305">Before you install a new version of the tool, we recommend that you uninstall the previous version.</span></span>

### <a name="install-an-authentication-certificate"></a><span data-ttu-id="758ac-306">Autentifikavimo sertifikato diegimas</span><span class="sxs-lookup"><span data-stu-id="758ac-306">Install an authentication certificate</span></span>

<span data-ttu-id="758ac-307">Norėdami įjungti autentifikavimą, turite sugeneruoti ir įdiegti sertifikatą tame pačiame kompiuteryje, kuriame veikia RSAT.</span><span class="sxs-lookup"><span data-stu-id="758ac-307">To enable authentication, you must generate and install a certificate on the same computer that RSAT is running on.</span></span>

#### <a name="generate-a-certificate"></a><span data-ttu-id="758ac-308">Sertifikato generavimas</span><span class="sxs-lookup"><span data-stu-id="758ac-308">Generate a certificate</span></span>

1. <span data-ttu-id="758ac-309">Norėdami sugeneruoti sertifikato failą, atidarykite „Microsoft Windows PowerShell“ langą kaip administratorius ir vykdykite šią komandą.</span><span class="sxs-lookup"><span data-stu-id="758ac-309">To generate a certificate file, open a Microsoft Windows PowerShell window as an admin, and run the following command.</span></span>

    ```powershell
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. <span data-ttu-id="758ac-310">Atidarykite sertifikatų tvarkyklę dialogo lange **Vykdyti** įvesdami **certlm.msc** ir patvirtinkite, kad **D365 automatizuoto testavimo sertifikatas** sukurtas pagal **Asmeninis \> Sertifikatai**.</span><span class="sxs-lookup"><span data-stu-id="758ac-310">Open certificate manager by entering **certlm.msc** in the **Run** dialog box, and confirm that the **D365 Automated testing certificate** certificate is created under **Personal \> Certificates**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="758ac-311">Būtinai įveskite **certlm.msc**, o ne **certmgr.msc**, nes sertifikatai saugomi vietiniame kompiuteryje.</span><span class="sxs-lookup"><span data-stu-id="758ac-311">Be sure to enter **certlm.msc**, not **certmgr.msc**, because the certificates are stored on the local computer.</span></span>

    ![D365 automatizuotas testavimo sertifikato sertifikatas](./media/setup_rsa_tool_46.png)

3. <span data-ttu-id="758ac-313">Spustelėkite dešiniuoju pelės mygtuku sertifikatą ir pasirinkite **Kopijuoti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-313">Right-click the certificate, and then select **Copy**.</span></span>
4. <span data-ttu-id="758ac-314">Eikite į **Patikimos šakninės sertifikavimo tarnybos \> Sertifikatai**.</span><span class="sxs-lookup"><span data-stu-id="758ac-314">Go to **Trusted Root Certification Authorities \> Certificates**.</span></span>

    ![Sertifikatų aplankas, esantis aplanke Patikimos šakninės sertifikavimo tarnybos](./media/setup_rsa_tool_47.png)

5. <span data-ttu-id="758ac-316">Meniu **Veiksmas** pasirinkite **Įklijuoti**, kad nukopijuotumėte sertifikatą į vietą **Patikimos šakninės sertifikavimo tarnybos**.</span><span class="sxs-lookup"><span data-stu-id="758ac-316">On the **Action** menu, select **Paste** to copy the certificate to the **Trusted Root Certification Authorities** location.</span></span>

    ![Meniu Veiksmas komanda Įklijuoti](./media/setup_rsa_tool_48.png)

6. <span data-ttu-id="758ac-318">Norėdami gauti įdiegto sertifikato kontrolinį kodą tarpų ir specialiųjų simbolių, atidarykite „Windows PowerShell“ langą kaip administratorius ir vykdykite šias komandas.</span><span class="sxs-lookup"><span data-stu-id="758ac-318">To get the thumbprint of the installed certificate, but without spaces or special characters, open a Windows PowerShell window as an admin, and run the following commands.</span></span>

    ```powershell
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > <span data-ttu-id="758ac-319">Įrašykite kontrolinį kodą, nes jums reikės jo vėliau, kai atnaujinsite programos objektų serverio (AOS) .wif failus ir nustatysite RSAT konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="758ac-319">Save the thumbprint, because you will need it later when you update the .wif files for Application Object Server (AOS) and set up the RSAT configuration.</span></span>

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a><span data-ttu-id="758ac-320">AOS kompiuterio konfigūravimas, kad būtų patikimas ryšys</span><span class="sxs-lookup"><span data-stu-id="758ac-320">Configure the AOS computer to trust the connection</span></span>

> [!NOTE]
> <span data-ttu-id="758ac-321">Jei aplinka yra 2 arba aukštesnės pakopos aplinka, sertifikato nykščio atspaudas turi būti atnaujintas wif.config faile **visuose** aplinkos AOS kompiuteriuose.</span><span class="sxs-lookup"><span data-stu-id="758ac-321">If the environment is a Tier 2+ environment, the certificate thumbprint must be updated in the wif.config file for **all** AOS computers for the environment.</span></span>

1. <span data-ttu-id="758ac-322">Užmegzkite nuotolinio darbalaukio protokolo (RDP) ryšį su AOS kompiuteriu.</span><span class="sxs-lookup"><span data-stu-id="758ac-322">Establish a Remote Desktop Protocol (RDP) connection to the AOS computer.</span></span> <span data-ttu-id="758ac-323">Išsami prisijungimo informacija yra nurodyta LCS aplinkos informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="758ac-323">Sign-in details are available on the environment details page in LCS.</span></span>
2. <span data-ttu-id="758ac-324">Atidarykite „Microsoft“ informacines interneto paslaugas (IIS) ir svetainių sąraše raskite **AOSService**.</span><span class="sxs-lookup"><span data-stu-id="758ac-324">Open Microsoft Internet Information Services (IIS), and find **AOSService** in the list of sites.</span></span>

    ![AOSService svetainių sąraše](./media/setup_rsa_tool_49.png)

3. <span data-ttu-id="758ac-326">Dešiniuoju pelės mygtuku spustelėkite **Naršyti**, kad atidarytumėte aplanką **\<Drive\>: \\AosService\\WebRoot**.</span><span class="sxs-lookup"><span data-stu-id="758ac-326">Right-click **Explore** to open the **\<Drive\>: \\AosService\\WebRoot** folder.</span></span> <span data-ttu-id="758ac-327">Raskite **wif.config** failą.</span><span class="sxs-lookup"><span data-stu-id="758ac-327">Find the **wif.config** file.</span></span>

    ![Wif.config failas „WebRoot“ aplanke](./media/setup_rsa_tool_50.png)

4. <span data-ttu-id="758ac-329">Atnaujinkite **wif.config** failą įtraukdami naują savo sertifikato tarnybos įrašą nurodydami sertifikato ir tarnybos pavadinimus, kaip parodyta šiame pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="758ac-329">Update the **wif.config** file by adding a new authority entry for your certificate and authority name, as shown in the following example.</span></span>

    ```Xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > <span data-ttu-id="758ac-330">Jei keli vartotojai naudoja tą pačią programą, kiekvienas vartotojas turi sugeneruoti atskirus nykščio atspaudus, o kiekvienas iš šių nykščio atspaudų turi būti įtrauktas į skiltį **\<keys\>**.</span><span class="sxs-lookup"><span data-stu-id="758ac-330">If multiple users are using the same application, each user must generate separate thumbprints, and each of those thumbprints must be added in the **\<keys\>** section.</span></span>

5. <span data-ttu-id="758ac-331">Jei yra daugiau nei vienas AOS kompiuteris, pakartokite 3–4 veiksmus su kiekvienu papildomu kompiuteriu.</span><span class="sxs-lookup"><span data-stu-id="758ac-331">If there is more than one AOS computer, repeat steps 3 through 4 for each additional computer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="758ac-332">Skirtingai nei senesnėse 2 pakopos aplinkose, naujos 2 pakopos aplinkos yra įdiegtos naudojant du AOS egzempliorius.</span><span class="sxs-lookup"><span data-stu-id="758ac-332">Unlike older Tier 2 environments, new Tier 2 environments are deployed with two AOS instances.</span></span>

6. <span data-ttu-id="758ac-333">Vykdykite **iisreset** visuose AOS kompiuteriuose.</span><span class="sxs-lookup"><span data-stu-id="758ac-333">Run **iisreset** on all the AOS computers.</span></span>

    > [!NOTE]
    > <span data-ttu-id="758ac-334">Jei neturite administratoriaus teisių vykdyti **iisreset** 1 pakopos kompiuteryje, LCS aplinkos informacijos puslapyje pasirinkite Prižiūrėti > Iš naujo paleisti tarnybas.</span><span class="sxs-lookup"><span data-stu-id="758ac-334">If you don't have admin rights to run **iisreset** on a Tier 1 computer, on the Environment details page in LCS, select Maintain > Restart services.</span></span>

#### <a name="tier-2-environment"></a><span data-ttu-id="758ac-335">2 ir aukštesnės pakopos aplinka</span><span class="sxs-lookup"><span data-stu-id="758ac-335">Tier 2+ environment</span></span>

<span data-ttu-id="758ac-336">Jei naudojama 2 ar aukštesnės pakopos („Standard“ lygio priėmimo testavimo smėlio dėžė arba naujesnė) aplinka, patikrinkite arba nustatykite nurodytą registro parametrą kompiuteryje, kuriame įdiegta RSAT.</span><span class="sxs-lookup"><span data-stu-id="758ac-336">If a Tier 2+ (Standard Acceptance Test sandbox or higher) environment is used, verify or set the following registry setting on the computer where RSAT is installed.</span></span> <span data-ttu-id="758ac-337">Šis veiksmas būtinas, nes padeda išvengti autentifikavimo arba RSAT ryšio klaidų.</span><span class="sxs-lookup"><span data-stu-id="758ac-337">This step is required because it helps you avoid authentication or RSAT connection errors.</span></span>

```PowerShell
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a><span data-ttu-id="758ac-338">RSAT įdiegimas</span><span class="sxs-lookup"><span data-stu-id="758ac-338">Install RSAT</span></span>

1. <span data-ttu-id="758ac-339">Eikite į <https://www.microsoft.com/download/details.aspx?id=57357> ir pasirinkite **Atsisiųsti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-339">Go to <https://www.microsoft.com/download/details.aspx?id=57357>, and select **Download**.</span></span>
2. <span data-ttu-id="758ac-340">Pasirinkite visus failus, tada pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="758ac-340">Select all the files, and then select **Next**.</span></span>

    ![Visų failų pasirinkimas](./media/setup_rsa_tool_51.png)

3. <span data-ttu-id="758ac-342">Norėdami paleisti diegimo programą, du kartus spustelėkite. msi paketą.</span><span class="sxs-lookup"><span data-stu-id="758ac-342">Double-click the .msi package to run the installer.</span></span> <span data-ttu-id="758ac-343">Tada, kai diegimas bus baigtas, pasirinkite **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-343">Then, when the installation is completed, select **Finish**.</span></span>

    ![RSAT diegimo programos failas](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a><span data-ttu-id="758ac-345">„Selenium“ ir naršyklių tvarkyklių įdiegimas</span><span class="sxs-lookup"><span data-stu-id="758ac-345">Install Selenium and browser drivers</span></span>

<span data-ttu-id="758ac-346">Jei naudojate senesnes RSAT versijas, turite įdiegti „Selenium“ ir naršyklių tvarkykles.</span><span class="sxs-lookup"><span data-stu-id="758ac-346">In older versions of RSAT, you had to install Selenium and browser drivers.</span></span> <span data-ttu-id="758ac-347">Jums nebereikia diegti šių tvarkyklių, nes jos įdiegtos automatiškai.</span><span class="sxs-lookup"><span data-stu-id="758ac-347">You no longer have to install these drivers because they are automatically installed.</span></span>

1. <span data-ttu-id="758ac-348">Pirmą kartą atidarę RSAT, būsite paraginti automatiškai atsisiųsti ir įdiegti „Selenium“.</span><span class="sxs-lookup"><span data-stu-id="758ac-348">The first time that you open RSAT, you're prompted to automatically download and install Selenium.</span></span> <span data-ttu-id="758ac-349">Daugiau informacijos rasite skyriuje [RSAT konfigūravimas](#configure-rsat).</span><span class="sxs-lookup"><span data-stu-id="758ac-349">For more information, see the [Configure RSAT](#configure-rsat) section.</span></span>
2. <span data-ttu-id="758ac-350">Kad galėtumėte vykdyti testavimo atvejį, būsite paraginti automatiškai atsisiųsti ir įdiegti naršyklės tvarkyklę, atitinkančią numatytąją naršyklę, kuri pasirenkama atliekant RSAT konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="758ac-350">Before you can run a test case, you're prompted to automatically download and install the browser driver that corresponds to the default browser that is selected in the RSAT configuration.</span></span> <span data-ttu-id="758ac-351">Daugiau informacijos rasite skyriuje [Testavimo atvejo įkėlimas ir vykdymas](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="758ac-351">For more information, see the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

## <a name="get-started-with-rsat"></a><span data-ttu-id="758ac-352">Darbo su RSAT“ pradžia</span><span class="sxs-lookup"><span data-stu-id="758ac-352">Get started with RSAT</span></span>

### <a name="create-a-test-plan-and-test-suites"></a><span data-ttu-id="758ac-353">Testavimo plano ir testavimo paketų kūrimas</span><span class="sxs-lookup"><span data-stu-id="758ac-353">Create a test plan and test suites</span></span>

1. <span data-ttu-id="758ac-354">Eikite į „Azure DevOps“ projektą ir pasirinkti **Testavimo planai**.</span><span class="sxs-lookup"><span data-stu-id="758ac-354">Go to the Azure DevOps project, and select **Test Plans**.</span></span>

    ![Komanda Testavimo planai](./media/setup_rsa_tool_53.png)

2. <span data-ttu-id="758ac-356">Pasirinkite **Naujas testavimo planas**.</span><span class="sxs-lookup"><span data-stu-id="758ac-356">Select **New Test Plan**.</span></span>

    ![Mygtukas Naujas testavimo planas](./media/setup_rsa_tool_54.png)

3. <span data-ttu-id="758ac-358">Užpildykite lauką **Pavadinimas** ir pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-358">Fill in the **Name** field, and then select **Create**.</span></span> <span data-ttu-id="758ac-359">Šioje mokomojoje programoje pavadinkite testavimo planą **RSAT testavimo planas**.</span><span class="sxs-lookup"><span data-stu-id="758ac-359">For this tutorial, name the test plan **RSAT Test Plan**.</span></span>

    ![Naujo testavimo plano dialogo langas](./media/setup_rsa_tool_55.png)

4. <span data-ttu-id="758ac-361">Pasirinkite pliuso ženklą (**+**), tada pasirinkite **Statinis paketas**, kad sukurtumėte statinį paketą pagal naują testavimo planą.</span><span class="sxs-lookup"><span data-stu-id="758ac-361">Select the plus sign (**+**), and then select **Static suite** to create a static suite under the new test plan.</span></span> <span data-ttu-id="758ac-362">Pavadinkite naują testavimo paketą **T01 – Make to Stock**.</span><span class="sxs-lookup"><span data-stu-id="758ac-362">Name the new test suite **T01 – Make to Stock**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="758ac-363">Taip pat galite sukurti užklausa pagrįstą paketą, jei norite, kad naujieji testavimo atvejai būtų automatiškai įtraukiami iš BPM į RSAT testavimo paketą.</span><span class="sxs-lookup"><span data-stu-id="758ac-363">You can also create a query-based suite, if you want the new test cases from BPM to be automatically pulled into the RSAT test suite.</span></span>

    ![Statinio paketo sukūrimas](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a><span data-ttu-id="758ac-365">Testavimo atvejų pridėjimas prie testavimo paketų</span><span class="sxs-lookup"><span data-stu-id="758ac-365">Attach test cases to test suites</span></span>

1. <span data-ttu-id="758ac-366">Pasirinkite **Įtraukti esamus** dešinėje pusėje, kad būtų įtraukti esami testavimo atvejai į testavimo paketą.</span><span class="sxs-lookup"><span data-stu-id="758ac-366">Select **Add existing** on the right side to add existing test cases to the test suite.</span></span>

    ![Esamų įtraukimo mygtukas](./media/setup_rsa_tool_57.png)

2. <span data-ttu-id="758ac-368">Puslapyje **Įtraukti testavimo atvejus į paketą** pasirinkite **Vykdyti užklausą** ir pasirinkite testavimo atvejį, kurį norite įtraukti į testavimo paketą.</span><span class="sxs-lookup"><span data-stu-id="758ac-368">On the **Add test cases to suite** page, select **Run query**, and then select the test case to add to the test suite.</span></span> <span data-ttu-id="758ac-369">Šioje mokomojoje programoje pasirinkite **Kurti naują produktą** testavimo atvejį.</span><span class="sxs-lookup"><span data-stu-id="758ac-369">For this tutorial, select the **Create a new product** test case.</span></span> <span data-ttu-id="758ac-370">Tada pasirinkite **Įtraukti testavimo atvejus** apatiniame dešiniajame puslapio kampe (šis mygtukas šioje iliustracijoje neparodytas).</span><span class="sxs-lookup"><span data-stu-id="758ac-370">Then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Mygtukas Vykdyti užklausą](./media/setup_rsa_tool_58.png)

    <span data-ttu-id="758ac-372">Testavimo atvejis įtraukiamas į testavimo paketą **T01-Make to Stock**.</span><span class="sxs-lookup"><span data-stu-id="758ac-372">The test case is added to the **T01-Make to Stock** test suite.</span></span>

    ![Testavimo atvejis įtrauktas į testavimo paketą](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a><span data-ttu-id="758ac-374">Konfigūruoti RSAT</span><span class="sxs-lookup"><span data-stu-id="758ac-374">Configure RSAT</span></span>

1. <span data-ttu-id="758ac-375">Atidarykite RSAT.</span><span class="sxs-lookup"><span data-stu-id="758ac-375">Open RSAT.</span></span>

    ![RSAT piktograma](./media/setup_rsa_tool_60.png)

2. <span data-ttu-id="758ac-377">Gaunate įspėjamąjį pranešimą, kuriame teigiama, kad „Regression Suite Automation Tool“ reikia „Selenium“; ar norite ją automatiškai atsisiųsti ir įdiegti dabar?“</span><span class="sxs-lookup"><span data-stu-id="758ac-377">You receive a warning message that states, "The Regression Suite Automation Tool requires Selenium, do you want to automatically download and install it now?"</span></span> <span data-ttu-id="758ac-378">Pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="758ac-378">Select **Yes**.</span></span>

    ![Įspėjimo pranešimas, kad „Regression Suite Automation Tool” reikia seleno](./media/setup_rsa_tool_61.png)

3. <span data-ttu-id="758ac-380">Viršutiniame dešiniajame kampe pasirinkite mygtuką **Parametrai** (krumpliaračio simbolis), tada pasirodžiusiame dialogo lange užpildykite šiuos laukus:</span><span class="sxs-lookup"><span data-stu-id="758ac-380">Select the **Settings** button (the gear symbol) in the upper-right corner, and then, in the dialog box that appears, fill in the following fields:</span></span>

    - <span data-ttu-id="758ac-381">**Azure DevOps URL** – įveskite savo „Azure DevOps“ projekto URL, pvz., `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span><span class="sxs-lookup"><span data-stu-id="758ac-381">**Azure DevOps Url** – Enter the URL of your Azure DevOps project, such as `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>
    - <span data-ttu-id="758ac-382">**Prieigos atpažinimo ženklas** – įveskite prieigos atpažinimo ženklą, kuris leidžia įrankiui prisijungti prie „Azure DevOps“.</span><span class="sxs-lookup"><span data-stu-id="758ac-382">**Access Token** – Enter the access token that lets the tool connect to Azure DevOps.</span></span> <span data-ttu-id="758ac-383">Naudokite anksčiau sukurtu asmeninės prieigos atpažinimo ženklu.</span><span class="sxs-lookup"><span data-stu-id="758ac-383">Use the personal access token that you created earlier in this tutorial.</span></span> <span data-ttu-id="758ac-384">Norėdami gauti daugiau informacijos, žr. [Prieigos autentifikavimas naudojant asmeninės prieigos atpažinimo ženklus](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span><span class="sxs-lookup"><span data-stu-id="758ac-384">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span>
    - <span data-ttu-id="758ac-385">**Projekto pavadinimas** – pasirinkite savo „Azure DevOps“ projekto pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="758ac-385">**Project Name** – Select the name of your Azure DevOps project.</span></span>
    - <span data-ttu-id="758ac-386">**Testavimo planas** – pasirinkite „Azure DevOps“ testavimo planą, kuriame yra jūsų testavimo atvejų.</span><span class="sxs-lookup"><span data-stu-id="758ac-386">**Test Plan** – Select the Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="758ac-387">Norėdami gauti daugiau informacijos, žr. [Testavimo planų ir testavimo paketų kūrimas](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span><span class="sxs-lookup"><span data-stu-id="758ac-387">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> <span data-ttu-id="758ac-388">Pasirinkę testavimo planą, pasirinkite **Tikrinti ryšį**, kad būtų galima tikrinti ryšį su „Azure DevOps“.</span><span class="sxs-lookup"><span data-stu-id="758ac-388">After you select a test plan, select **Test Connection** to test your connection to Azure DevOps.</span></span>
    - <span data-ttu-id="758ac-389">**Pagrindinio kompiuterio pavadinimas** – įveskite testavimo aplinkos pagrindinio kompiuterio pavadinimą, pvz., **\<myaos\>.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="758ac-389">**Hostname** – Enter the host name of the test environment, such as **\<myaos\>.cloudax.dynamics.com**.</span></span> <span data-ttu-id="758ac-390">Neįtraukite **https://** arba **http://** prefikso.</span><span class="sxs-lookup"><span data-stu-id="758ac-390">Don't include the **https://** or **http://** prefix.</span></span>
    - <span data-ttu-id="758ac-391">**SOAP pagrindinio kompiuterio pavadinimas** – įveskite testavimo aplinkos SOAP pagrindinio kompiuterio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="758ac-391">**SOAP Hostname** – Enter the SOAP host name of the test environment.</span></span> <span data-ttu-id="758ac-392">Paprastai SOAP pagrindinio kompiuterio pavadinimas yra toks pat kaip pagrindinio kompiuterio pavadinimas, bet jame yra **soap** sufiksas.</span><span class="sxs-lookup"><span data-stu-id="758ac-392">Typically, the SOAP host name is the same as the host name, but it has a **soap** suffix.</span></span> <span data-ttu-id="758ac-393">Štai pavyzdys: **\<myaos\>soap.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="758ac-393">Here is an example: **\<myaos\>soap.cloudax.dynamics.com**.</span></span> <span data-ttu-id="758ac-394">Neįtraukite **https://** arba **http://** prefikso.</span><span class="sxs-lookup"><span data-stu-id="758ac-394">Don't include the **https://** or **http://** prefix.</span></span>

        > [!NOTE]
        > <span data-ttu-id="758ac-395">Norėdami rasti pagrindinio kompiuterio pavadinimą ir SOAP pagrindinio kompiuterio pavadinimą, atidarykite IIS tvarkyklę, dešiniuoju pelės mygtuku spustelėkite **Svetainės \> AOSService**, tada pasirinkite **Redaguoti susiejimus**.</span><span class="sxs-lookup"><span data-stu-id="758ac-395">To find the host name and SOAP host name, open IIS Manager, right-click **Sites \> AOSService**, and then select **Edit bindings**.</span></span> <span data-ttu-id="758ac-396">Stulpelyje **Pagrindinio kompiuterio pavadinimas** pateikiami pagrindinio kompiuterio pavadinimas ir SOAP pagrindinio kompiuterio pavadinimas (SOAP pagrindinio kompiuterio pavadinime yra sufiksas **soap** URL).</span><span class="sxs-lookup"><span data-stu-id="758ac-396">The values in the **Host Name** column give you the host name and SOAP host name (the SOAP host name has the suffix **soap** in the URL).</span></span>

        ![Pagrindinio kompiuterio pavadinimas ir SOAP pagrindinio kompiuterio pavadinimas stulpelyje Pagrindinio kompiuterio pavadinimas](./media/setup_rsa_tool_63.png)

    - <span data-ttu-id="758ac-398">**Administratoriaus vartotojo vardas** – įveskite testavimo aplinkos administratoriaus vartotojo el. pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="758ac-398">**Admin user name** – Enter the email address of an admin user in the test environment.</span></span>
    - <span data-ttu-id="758ac-399">**Kontrolinis kodas** – įveskite autentifikavimo sertifikato kontrolinį kodą, kaip pirmiau aprašyta šioje mokomojoje programoje.</span><span class="sxs-lookup"><span data-stu-id="758ac-399">**Thumbprint** – Enter the thumbprint of the authentication certificate, as described earlier in this tutorial.</span></span>
    - <span data-ttu-id="758ac-400">**Darbo katalogas** – nurodykite aplanko, kuriame saugomi testavimo automatizavimo failai, pvz., „Excel“ testavimo duomenų failai, vietą.</span><span class="sxs-lookup"><span data-stu-id="758ac-400">**Working directory** – Specify the folder location for storing test automation files, such as Excel test data files.</span></span> <span data-ttu-id="758ac-401">Pavyzdžiui, įveskite arba pasirinkite **C:\\Temp\\RegressionTool**.</span><span class="sxs-lookup"><span data-stu-id="758ac-401">For example, enter or select **C:\\Temp\\RegressionTool**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="758ac-402">Jeigu aplanko pavadinime yra tarpų, vykdyti nepavyks, nes aplanko nepavyks rasti.</span><span class="sxs-lookup"><span data-stu-id="758ac-402">If the name of the folder has spaces, execution will fail because the folder can't be found.</span></span> <span data-ttu-id="758ac-403">Ši problema yra jau žinoma; ji nebeturi kilti naujausioje įrankio versijoje.</span><span class="sxs-lookup"><span data-stu-id="758ac-403">This issue is a known issue and should be fixed in the latest version of the tool.</span></span>

    - <span data-ttu-id="758ac-404">**Numatytoji naršyklė** – pasirinkite **Internet Explorer** arba **Google Chrome**.</span><span class="sxs-lookup"><span data-stu-id="758ac-404">**Default browser** – Select either **Internet Explorer** or **Google Chrome**.</span></span> <span data-ttu-id="758ac-405">Įsitikinkite, kad įdiegtos tinkamos naršyklių tvarkyklės.</span><span class="sxs-lookup"><span data-stu-id="758ac-405">Make sure that the appropriate browser drivers have been installed.</span></span>
    - <span data-ttu-id="758ac-406">**Testavimo vykdymo skirtasis laikas** – nurodykite testavimo vykdymo laiką minutėmis.</span><span class="sxs-lookup"><span data-stu-id="758ac-406">**Test run timeout** – Specify the time-out period, in minutes, for test runs.</span></span> <span data-ttu-id="758ac-407">Pasibaigus skirtajam laikui, visi aktyvūs langai yra uždaromi, todėl laukiantys testavimo atvejai lieka neįvykdyti.</span><span class="sxs-lookup"><span data-stu-id="758ac-407">When the time-out period elapses, all active windows are closed, and pending test cases fail.</span></span>
    - <span data-ttu-id="758ac-408">**Testavimo veiksmo skirtasis laikas** – šis laukas kontroliuoja „Finance and Operation“ aplinkos serverio užklausų skirtojo laiko periodą minutėmis.</span><span class="sxs-lookup"><span data-stu-id="758ac-408">**Test action timeout** – This field controls the time-out period, in minutes, for Finance and Operation environment server requests.</span></span> <span data-ttu-id="758ac-409">Paprastai turi užtekti numatytosios vertės (2 min.).</span><span class="sxs-lookup"><span data-stu-id="758ac-409">Usually, the default value (2 minutes) should be enough.</span></span> <span data-ttu-id="758ac-410">Tačiau lėtesnių aplinkų atvejais galite pageidauti padidinti vertę, jei įvyksta su skirtuoju laiku susijusių klaidų.</span><span class="sxs-lookup"><span data-stu-id="758ac-410">However, for slower environments, you might want to increase the value if errors that are related to time-outs occur.</span></span>
    - <span data-ttu-id="758ac-411">**Įmonės pavadinimas** – įveskite įmonės pavadinimą, kuris bus naudojamas kaip numatytoji įmonė kuriant „Excel“ parametrų failus.</span><span class="sxs-lookup"><span data-stu-id="758ac-411">**Company name** – Enter the company name to use as your default company when Excel parameter files are created.</span></span> <span data-ttu-id="758ac-412">Vėliau įmonę galite pakeisti redaguodami „Excel“ parametrų failą.</span><span class="sxs-lookup"><span data-stu-id="758ac-412">You can change the company later by editing the Excel parameter file.</span></span>

    ![Dialogo langas Parametrai](./media/setup_rsa_tool_62.png)

4. <span data-ttu-id="758ac-414">Pasirinkite **Taikyti**, kad būtų pritaikyti ir įrašyti parametrai.</span><span class="sxs-lookup"><span data-stu-id="758ac-414">Select **Apply** to apply and save your settings.</span></span>

    <span data-ttu-id="758ac-415">Norėdami įrašyti savo dabartinius parametrus į kompiuteryje esantį konfigūracijos failą, pasirinkite **Įrašyti kaip**.</span><span class="sxs-lookup"><span data-stu-id="758ac-415">To save your current settings to a configuration file on your computer, select **Save as**.</span></span> <span data-ttu-id="758ac-416">Norėdami atkurti savo parametrus iš kompiuteryje esančio konfigūracijos failo, pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-416">To restore your settings from a configuration file on your computer, select **Open**.</span></span>

5. <span data-ttu-id="758ac-417">Pasirinkite **Uždaryti** norėdami uždaryti dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="758ac-417">Select **Close** to close the dialog box.</span></span>

### <a name="load-and-run-test-cases"></a><span data-ttu-id="758ac-418">Testavimo atvejų įkėlimas ir vykdymas</span><span class="sxs-lookup"><span data-stu-id="758ac-418">Load and run test cases</span></span>

1. <span data-ttu-id="758ac-419">Pasirinkite **Įkelti**, kad būtų įkeltas **RSAT testavimo planas** iš „Azure DevOps“ projekto.</span><span class="sxs-lookup"><span data-stu-id="758ac-419">Select **Load** to load the **RSAT Test Plan** test plan from the Azure DevOps project.</span></span>

    ![Įkėlimo mygtukas](./media/setup_rsa_tool_64.png)

2. <span data-ttu-id="758ac-421">Pasirinkite **Kurti naują produktą** testavimo atvejį iš testavimo paketo, tada pasirinkite **Naujas \> Generuoti testavimo vykdymo ir parametrų failus**.</span><span class="sxs-lookup"><span data-stu-id="758ac-421">Select the **Create a new product** test case from the test suite, and then select **New \> Generate Test Execution and Parameter files**.</span></span>

    ![Komanda Generuoti testavimo vykdymo ir parametrų failus meniu Naujas](./media/setup_rsa_tool_65.png)

    <span data-ttu-id="758ac-423">„Excel“ parametrų failas sukuriamas vietiniame aplanke, kurį nurodėte RSAT konfigūracijoje (pvz., **C:\\Temp\\RegressionTool**).</span><span class="sxs-lookup"><span data-stu-id="758ac-423">The Excel parameter file is created in the local folder that you specified in the RSAT configuration (for example, **C:\\Temp\\RegressionTool**).</span></span>

    ![„Excel“ parametrų failas sukurtas](./media/setup_rsa_tool_66.png)

3. <span data-ttu-id="758ac-425">Jei norite įrašyti parametrų failus, pasirinkite **Nusiųsti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-425">If you want to save the parameter files, select **Upload**.</span></span> <span data-ttu-id="758ac-426">Visų pasirinktų testavimo atvejų testavimo automatizavimo failai yra nusiunčiami į „Azure DevOps“ naudoti ateityje.</span><span class="sxs-lookup"><span data-stu-id="758ac-426">Test automation files of all selected test cases are uploaded to Azure DevOps for future use.</span></span> <span data-ttu-id="758ac-427">(Tarp šitų failų yra „Excel“ testavimo parametrų failai.)</span><span class="sxs-lookup"><span data-stu-id="758ac-427">(These files include Excel test parameter files.)</span></span>

    <span data-ttu-id="758ac-428">Tokiu būdu galite pasirinkti **Įkelti** norėdami įkelti parametrų failus (ir automatizavimo failus) iš testavimo atvejo tiesiai iš „Azure DevOps“.</span><span class="sxs-lookup"><span data-stu-id="758ac-428">In this way, you can select **Load** to load the parameter files (and automation files) from the test case directly from Azure DevOps.</span></span> <span data-ttu-id="758ac-429">Nereikia iš naujo sugeneruoti parametrų failų.</span><span class="sxs-lookup"><span data-stu-id="758ac-429">You don't have to regenerate the parameter files.</span></span> <span data-ttu-id="758ac-430">Šis metodas bus svarbus vėliau, kai norėsite, kad parametrų failo pakeitimai būtų išlaikyti ir jie nebūtų perrašyti.</span><span class="sxs-lookup"><span data-stu-id="758ac-430">This approach will become important later, when you want to keep the modifications in the parameter file and don't want them to be overwritten.</span></span>

4. <span data-ttu-id="758ac-431">Norėdami patikrinti, ar automatizavimo failai ir parametrų failai yra įrašomi „Azure DevOps“, eikite į „Azure DevOps“ projektą, pasirinkite **Sritys \> Darbo elementai**, tada pasirinkite **Kurti naują produktą** testavimo atvejį.</span><span class="sxs-lookup"><span data-stu-id="758ac-431">To verify that the automation files and parameter files are saved to Azure DevOps, go to the Azure DevOps project, select **Boards \> Work Items**, and select the **Create a new product** test case.</span></span> <span data-ttu-id="758ac-432">Skirtuke **Priedai** turite matyti keturis failus:</span><span class="sxs-lookup"><span data-stu-id="758ac-432">On the **Attachments** tab, you should see four files:</span></span>

    - <span data-ttu-id="758ac-433">**.cs** – C\# automatizavimo failas</span><span class="sxs-lookup"><span data-stu-id="758ac-433">**.cs** – C\# automation file</span></span>
    - <span data-ttu-id="758ac-434">**.dll** – kompiliuotas automatizavimo failas kaip rinkinys</span><span class="sxs-lookup"><span data-stu-id="758ac-434">**.dll** – Compiled automation file as an assembly</span></span>
    - <span data-ttu-id="758ac-435">**.xlsx** – „Excel“ parametrų failas</span><span class="sxs-lookup"><span data-stu-id="758ac-435">**.xlsx** – Excel parameter file</span></span>
    - <span data-ttu-id="758ac-436">**.xml** – įrašymo failas</span><span class="sxs-lookup"><span data-stu-id="758ac-436">**.xml** – Recording file</span></span>

    ![Failai skirtuke Priedai](./media/setup_rsa_tool_67.png)

5. <span data-ttu-id="758ac-438">Pasirinkite norimą vykdyti testavimo atvejį ir pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-438">Select the test case to run, and then select **Run**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="758ac-439">Prieš vykdydami testavimo atvejus, jei naudojate „Internet Explorer“ kaip naršyklę, įsitikinkite, kad jūsų darbalaukio skiriamoji geba nustatyta kaip **100%** **„Windows“ ekrano parametrai \> Mastelis ir išdėstymas**.</span><span class="sxs-lookup"><span data-stu-id="758ac-439">Before you run test cases, if you're using Internet Explorer as the browser, make sure that your desktop resolution is set to **100%** at **Windows Display settings \> Scale and layout**.</span></span> <span data-ttu-id="758ac-440">Jei negalite pakeisti šio parametro virtualiajame kompiuteryje (VM), jį pakeiskite kliente (nešiojamajame kompiuteryje), iš kurio bandote pasiekti VM.</span><span class="sxs-lookup"><span data-stu-id="758ac-440">If you can't change this setting on a virtual machine (VM), change it on the client (laptop) that you're trying to access the VM from.</span></span> <span data-ttu-id="758ac-441">Tada skiriamosios gebos parametrus perims VM ekrano parametrai.</span><span class="sxs-lookup"><span data-stu-id="758ac-441">The resolution settings will then be inherited by the VM display settings.</span></span>

    ![Darbalaukio skiriamoji geba nustatyta kaip 100 %](./media/setup_rsa_tool_68.png)

6. <span data-ttu-id="758ac-443">Jei sistemoje neįdiegta naršyklių tvarkyklių, gausite įspėjamąjį pranešimą, kuriame teigiama, kad „Šiai operacijai atlikti reikia \<browser name\> tvarkyklės.</span><span class="sxs-lookup"><span data-stu-id="758ac-443">If the browser drivers aren't installed in the system, you receive a warning message that states, "This operation requires the \<browser name\> driver.</span></span> <span data-ttu-id="758ac-444">Ar norite automatiškai atsisiųsti ir įdiegti ją dabar?“</span><span class="sxs-lookup"><span data-stu-id="758ac-444">Do you want to automatically downloads and install it now?"</span></span> <span data-ttu-id="758ac-445">Pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="758ac-445">Select **Yes**.</span></span>

    ![Įspėjimo pranešimas „Internet Explorer“ atveju](./media/setup_rsa_tool_69.png)

    ![Įspėjimo pranešimas „Chrome“ atveju](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > <span data-ttu-id="758ac-448">Jei naudojate „Chrome“ kaip naršyklę ir gaunate klaidos pranešimą, kuriame nurodoma, kad seansas nebuvo sukurtas, nes „Chrome“ versija netinkama, atsisiųskite naujausią „Chrome“ tvarkyklę iš <http://chromedriver.chromium.org/downloads> į **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** aplanką.</span><span class="sxs-lookup"><span data-stu-id="758ac-448">If you're using Chrome as the browser and receive an error message that states that the session wasn't created because the Chrome version isn't correct, download the latest Chrome driver from <http://chromedriver.chromium.org/downloads> to the **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** folder.</span></span>

    ![Klaidos pranešimas „Chrome“ atveju](./media/setup_rsa_tool_71.png)

    <span data-ttu-id="758ac-450">Testavimo atvejis vykdomas ir laukas **Rezultatai** atnaujinamas.</span><span class="sxs-lookup"><span data-stu-id="758ac-450">The test case is run, and the **Result** field is updated.</span></span>

    ![Atnaujintas rezultatų laukas](./media/setup_rsa_tool_72.png)

    <span data-ttu-id="758ac-452">Jei vadovavotės šia mokomąja medžiaga, kaip parašyta, **Sukurti naują produktą** testavimo atvejo rezultatas bus neigiamas, nes produkto kūrimo užduoties įrašas įrašė produkto pavadinimą kaip užprogramuota vertė.</span><span class="sxs-lookup"><span data-stu-id="758ac-452">If you've followed this tutorial as it's written, the **Create a new product** test case will fail, because the task recording for creating a product saved the product name as a hard-coded value.</span></span> <span data-ttu-id="758ac-453">Jei iš naujo įvykdysite tą patį testavimo atvejį, turėtumėte gauti klaidos pranešimą, nes produktas jau yra.</span><span class="sxs-lookup"><span data-stu-id="758ac-453">If you rerun the same test case, you should receive an error message, because the product already exists.</span></span>

    ![Rezultatų lauko reikšmė Nepavyko](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a><span data-ttu-id="758ac-455">Testavimo rezultatų peržiūra</span><span class="sxs-lookup"><span data-stu-id="758ac-455">View the test results</span></span>

1. <span data-ttu-id="758ac-456">Dukart spustelėkite nepavykusį testavimo atvejį.</span><span class="sxs-lookup"><span data-stu-id="758ac-456">Double-click the failed test case.</span></span>

    <span data-ttu-id="758ac-457">Gaunate klaidos pranešimą.</span><span class="sxs-lookup"><span data-stu-id="758ac-457">You receive an error message.</span></span>

    ![Klaidos pranešimas](./media/setup_rsa_tool_73.png)

2. <span data-ttu-id="758ac-459">Pasirinkite **Informacija**, kad būtų galima peržiūrėti visą klaidos pranešimą.</span><span class="sxs-lookup"><span data-stu-id="758ac-459">Select **Details** to view the whole error message.</span></span>

    ![Visas klaidos pranešimas](./media/setup_rsa_tool_74.png)

3. <span data-ttu-id="758ac-461">Norėdami peržiūrėti išsamią klaidos pranešimo versiją „Azure DevOps“, pasirinkite **Atidaryti „Azure DevOps“**.</span><span class="sxs-lookup"><span data-stu-id="758ac-461">To view a detailed version of the error message in Azure DevOps, select **Open in Azure DevOps**.</span></span> <span data-ttu-id="758ac-462">„Azure DevOps“ galite peržiūrėti testavimo atvejo būseną ir išsamų klaidos pranešimą.</span><span class="sxs-lookup"><span data-stu-id="758ac-462">In Azure DevOps, you can view the status of the test case and the detailed error message.</span></span>

    ![Išsamus klaidos pranešimas, rodomas „Azure DevOps“](./media/setup_rsa_tool_75.png)

4. <span data-ttu-id="758ac-464">Norėdami tiesiogiai „Azure DevOps“ projekte peržiūrėti testavimo rezultatus, eikite į **Testavimo planai \> Testavimo planai \> Vykdymai**.</span><span class="sxs-lookup"><span data-stu-id="758ac-464">To view the test results directly in the Azure DevOps project, go to **Test Plans \> Test Plans \> Runs**.</span></span> <span data-ttu-id="758ac-465">Du kartus spustelėkite testavimo vykdymą, kurio daugiau informacijos norite matyti.</span><span class="sxs-lookup"><span data-stu-id="758ac-465">Double-click the test run that you want to see more details for.</span></span>

    ![Testavimo vykdymų „Azure DevOps“ sąrašas](./media/setup_rsa_tool_76.png)

5. <span data-ttu-id="758ac-467">Skirtuke **Vykdymo suvestinė** rodoma, kad testavimo atvejis nesėkmingas, bet faktinis klaidos pranešimas nepateikiamas.</span><span class="sxs-lookup"><span data-stu-id="758ac-467">The **Run summary** tab indicates that the test case failed, but it doesn't provide the actual error message.</span></span> <span data-ttu-id="758ac-468">Norėdami peržiūrėti išsamų klaidos pranešimą, pasirinkite skirtuką **Testavimo rezultatai**.</span><span class="sxs-lookup"><span data-stu-id="758ac-468">To view the detailed error message, select the **Test results** tab.</span></span>

    ![Skirtukas Vykdymo suvestinė](./media/setup_rsa_tool_77.png)

    <span data-ttu-id="758ac-470">Skirtuke **Testavimo rezultatai** pateikiama testavimo atvejo informacija, taip pat rezultatas ir klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="758ac-470">The **Test results** tab provides the test case information, together with the outcome and the error message.</span></span>

    ![Skirtukas Testavimo rezultatai](./media/setup_rsa_tool_78.png)

6. <span data-ttu-id="758ac-472">Du kartus spustelėkite reikiamą įrašą, kad peržiūrėtumėte išsamų klaidos pranešimą.</span><span class="sxs-lookup"><span data-stu-id="758ac-472">Double-click the relevant record to view the detailed error message.</span></span>

    ![Išsamus klaidos pranešimas](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > <span data-ttu-id="758ac-474">Visus klaidos pranešimus taip pat galima rasti vietoje **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span><span class="sxs-lookup"><span data-stu-id="758ac-474">All error messages are also available locally in **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span></span>

7. <span data-ttu-id="758ac-475">Taip pat galite eksportuoti testavimo vykdymo rezultatus iš testavimo plano pasirinkdami **Eksportuoti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-475">You can also export the test run results from the test plan level by selecting **Export**.</span></span>

    ![Testavimo plano eksportavimas](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a><span data-ttu-id="758ac-477">„Excel“ parametrų failo modifikavimas</span><span class="sxs-lookup"><span data-stu-id="758ac-477">Modify the Excel parameter file</span></span>

1. <span data-ttu-id="758ac-478">Atidarykite RSAT.</span><span class="sxs-lookup"><span data-stu-id="758ac-478">Open RSAT.</span></span>
2. <span data-ttu-id="758ac-479">Pasirinkite testavimo atvejį ir pasirinkite **Redaguoti**, norėdami atidaryti „Excel“ parametrų failą.</span><span class="sxs-lookup"><span data-stu-id="758ac-479">Select the test case, and then select **Edit** to open the Excel parameter file.</span></span>

    <span data-ttu-id="758ac-480">Lape **EcoResProductCreate** atkreipkite dėmesį, kad lauko **Produkto numeris** vertė yra užprogramuota.</span><span class="sxs-lookup"><span data-stu-id="758ac-480">On the **EcoResProductCreate** sheet, notice that the value of the **Product number** field is hard-coded.</span></span> <span data-ttu-id="758ac-481">Prieš dar kartą vykdydami testavimo atvejį, turite atnaujinti šį lauką nauju produkto numeriu.</span><span class="sxs-lookup"><span data-stu-id="758ac-481">You must update this field to a new product number before you run the test case again.</span></span>

3. <span data-ttu-id="758ac-482">Norėdami, kad būtų sugeneruotas unikalus kiekvieno vykdymo produkto numeris ir nereikėtų iš naujo atidaryti „Excel“ parametrų failo ir kiekvieną kartą patiems atnaujinti produkto numerio, naudokite šią „Excel“ formulę.</span><span class="sxs-lookup"><span data-stu-id="758ac-482">To generate a unique product number for each run without having to reopen the Excel parameter file and manually update the product number every time, use the following Excel formula.</span></span>

    ```vba
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > <span data-ttu-id="758ac-483">Be skirtuko **Bendra**, „Excel“ parametrų faile yra kiekvieno formos puslapio testavimo atvejų apsilankymų duomenų skirtukas.</span><span class="sxs-lookup"><span data-stu-id="758ac-483">In addition to the **General** tab, the Excel parameter file contains a data tab for every form page the test case visits.</span></span>

    ![Laukas Produkto numeris](./media/setup_rsa_tool_81.png)

4. <span data-ttu-id="758ac-485">Pasirinkite **Įrašyti** ir uždarykite „Excel“ darbaknygę.</span><span class="sxs-lookup"><span data-stu-id="758ac-485">Select **Save**, and then close the Excel workbook.</span></span>
5. <span data-ttu-id="758ac-486">Pasirinkite **Nusiųsti**, kad įrašytumėte „Excel“ parametrų failą į „Azure DevOps“.</span><span class="sxs-lookup"><span data-stu-id="758ac-486">Select **Upload** to save the Excel parameter file to Azure DevOps.</span></span>

    ![Sėkmingo nusiuntimo pranešimas](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > <span data-ttu-id="758ac-488">Norėdami vykdyti testavimo atvejus konkretaus vartotojo kontekste „Excel“ parametrų failo skirtuko **Bendra** lauke **Tikrinti vartotoją** įveskite vartotojo el. pašto ID.</span><span class="sxs-lookup"><span data-stu-id="758ac-488">To run test cases in a specific user context, enter the user's email ID in the **Test User** field on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="758ac-489">Naujausioje RSAT versijoje laukų išdėstymas, esantis „Excel“ parametrų faile, atnaujintas, bet koncepcija išlieka ta pati.</span><span class="sxs-lookup"><span data-stu-id="758ac-489">In the latest version of RSAT, the layout of the fields in the Excel parameter file has been updated, but the concept remains the same.</span></span>
    >
    > ![Laukas Tikrinti vartotoją](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a><span data-ttu-id="758ac-491">Rezultatų tikrinimas</span><span class="sxs-lookup"><span data-stu-id="758ac-491">Validate the results</span></span>

- <span data-ttu-id="758ac-492">Pasirinkite **Vykdyti**, kad iš naujo įvykdytumėte testavimo atvejį, ir patikrinkite, ar jo rezultatas teigiamas.</span><span class="sxs-lookup"><span data-stu-id="758ac-492">Select **Run** to rerun the test case, and verify that the test case has passed.</span></span> <span data-ttu-id="758ac-493">Testavimo rezultatus galite peržiūrėti, kaip aprašyta skyriuje [Testavimo rezultatų peržiūra](#view-the-test-results).</span><span class="sxs-lookup"><span data-stu-id="758ac-493">You can view the test results as described in the [View the test results](#view-the-test-results) section.</span></span>

    ![Rezultatų lauko reikšmė Pavyko](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a><span data-ttu-id="758ac-495">Testavimo atvejų sujungimas</span><span class="sxs-lookup"><span data-stu-id="758ac-495">Chaining of test cases</span></span>

<span data-ttu-id="758ac-496">Viena iš pagrindinių RSAT funkcijų – testavimo atvejų sujungimas (t. y. testavimo galimybė pereiti prie kitų testų).</span><span class="sxs-lookup"><span data-stu-id="758ac-496">One key feature of RSAT is the chaining of test cases (that is, the capability of a test to pass values to other tests).</span></span> <span data-ttu-id="758ac-497">Testavimo atvejai vykdomi pagal „Azure DevOps“ testavimo plane nustatytą tvarką.</span><span class="sxs-lookup"><span data-stu-id="758ac-497">Test cases are run according to their defined order in the Azure DevOps test plan.</span></span> <span data-ttu-id="758ac-498">(Šią tvarką taip pat galima atnaujinti patiems testavimo įrankyje.) Todėl, jei norite perkelti kintamuosius iš vieno testavimo atvejo į kitą, labai svarbu, kad testai eitų tinkama tvarka.</span><span class="sxs-lookup"><span data-stu-id="758ac-498">(This order can also be updated in the test tool itself.) Therefore, if you want to pass variables from one test case to another, it's very important that the tests be in the correct order.</span></span>

<span data-ttu-id="758ac-499">Šiame skyriuje sukursite įrašytą kintamąjį pirmame testavimo atvejyje, sukursite antrą testavimo atvejį ir perduosite įrašytą kintamąjį iš pirmo testavimo atvejo į antrą testavimo atvejį.</span><span class="sxs-lookup"><span data-stu-id="758ac-499">In this section, you will create a saved variable in the first test case, create a second test case, and pass the saved variable from the first test case to the second test case.</span></span> <span data-ttu-id="758ac-500">Tada vykdysite testavimo atvejus kaip grandininį testavimo atvejį RSAT.</span><span class="sxs-lookup"><span data-stu-id="758ac-500">You will then run the test cases as a chained test case in RSAT.</span></span>

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a><span data-ttu-id="758ac-501">Esamo užduoties įrašo modifikavimas įrašytam kintamajam sukurti</span><span class="sxs-lookup"><span data-stu-id="758ac-501">Modify an existing task recording to create a saved variable</span></span>

1. <span data-ttu-id="758ac-502">Atidarykite kliento programą.</span><span class="sxs-lookup"><span data-stu-id="758ac-502">Open the client.</span></span>
2. <span data-ttu-id="758ac-503">Pasirinkite mygtuką **Parametrai** (krumpliaračio simbolis), tada pasirinkite **Užduočių įrašymo priemonė**.</span><span class="sxs-lookup"><span data-stu-id="758ac-503">Select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>
3. <span data-ttu-id="758ac-504">Pasirinkite **Redaguoti įrašą**.</span><span class="sxs-lookup"><span data-stu-id="758ac-504">Select **Edit Recording**.</span></span>

    ![Mygtukas Redaguoti įrašą](./media/setup_rsa_tool_85.png)

4. <span data-ttu-id="758ac-506">Pasirinkite **Atidaryti iš „Lifecycle Services“**.</span><span class="sxs-lookup"><span data-stu-id="758ac-506">Select **Open from Lifecycle Services**.</span></span>

    ![Mygtukas Atidaryti iš „Lifecycle Services“](./media/setup_rsa_tool_86.png)

5. <span data-ttu-id="758ac-508">Pasirinkite **Pasirinkti „Lifecycle Services“ biblioteką**.</span><span class="sxs-lookup"><span data-stu-id="758ac-508">Select **Select the Lifecycle Services library**.</span></span>

    ![Mygtukas Pasirinkti „Lifecycle Services“ biblioteką](./media/setup_rsa_tool_87.png)

    <span data-ttu-id="758ac-510">BPM bibliotekos įkeliamos iš LCS.</span><span class="sxs-lookup"><span data-stu-id="758ac-510">BPM libraries are loaded from LCS.</span></span>

    ![BPM bibliotekų įkėlimas](./media/setup_rsa_tool_88.png)

6. <span data-ttu-id="758ac-512">Kai BPM bibliotekos įkeliamos iš LCS, pasirinkite **RSAT** BPM biblioteką ir **Kurti naują produktą** verslo procesą, su kuriuo susietas užduoties įrašas.</span><span class="sxs-lookup"><span data-stu-id="758ac-512">After the BPM libraries are loaded from LCS, select the **RSAT** BPM library and the **Create a new product** business process that the task recording was associated with.</span></span> <span data-ttu-id="758ac-513">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="758ac-513">Then select **OK**.</span></span>

    ![BPM bibliotekos ir verslo proceso pasirinkimas](./media/setup_rsa_tool_89.png)

7. <span data-ttu-id="758ac-515">Tinkamo užduoties įrašo pavadinimas įvedamas į lauką **Įrašo pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="758ac-515">The name of the appropriate task recording is entered in the **Recording name** field.</span></span> <span data-ttu-id="758ac-516">Pasirinkite **Paleisti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-516">Select **Start**.</span></span>

    ![Lauke Įrašo pavadinimas esantis užduoties įrašo pavadinimas](./media/setup_rsa_tool_90.png)

8. <span data-ttu-id="758ac-518">Eikite į **Produkto informacijos valdymas \> Produktai** ir pasirinkite **Naujas**, kad būtų atidarytas puslapis, kuriame buvo įrašytas pradinis užduoties įrašas **Kurti produktą**.</span><span class="sxs-lookup"><span data-stu-id="758ac-518">Go to **Product information management \> Products**, and select **New** to open the page where the original task recording, **Create a product**, was recorded.</span></span>
9. <span data-ttu-id="758ac-519">Pasirinkite **Įterpti veiksmą**.</span><span class="sxs-lookup"><span data-stu-id="758ac-519">Select **Insert step**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="758ac-520">Naujas veiksmas įterpiamas **po** veiksmo, kurį pasirinkote srityje.</span><span class="sxs-lookup"><span data-stu-id="758ac-520">The new step is inserted **after** the step that you selected in the pane.</span></span>

    ![Mygtukas Įterpti veiksmą](./media/setup_rsa_tool_91.png)

10. <span data-ttu-id="758ac-522">Dešiniuoju pelės mygtuku spustelėkite lauką **Produkto numeris** ir pasirinkite **Užduočių įrašymo priemonė \> Kopijuoti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-522">Right-click the **Product number** field, and then select **Task recorder \> Copy**.</span></span>

    ![Kopijavimo komanda](./media/setup_rsa_tool_92.png)

11. <span data-ttu-id="758ac-524">Naujas veiksmas įtraukiamas į sritį.</span><span class="sxs-lookup"><span data-stu-id="758ac-524">A new step is added in the pane.</span></span> <span data-ttu-id="758ac-525">Pasižymėkite lauko **Produkto numeris** vertę, nes jos reikės vėliau.</span><span class="sxs-lookup"><span data-stu-id="758ac-525">Make a note of the value in the **Product number** field, because you will need it later.</span></span>

    ![Naujas veiksmas įtrauktas](./media/setup_rsa_tool_93.png)

12. <span data-ttu-id="758ac-527">Pasirinkite **Baigta redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-527">Select **Done editing**.</span></span>
13. <span data-ttu-id="758ac-528">Pasirinkite **Įrašyti į „Lifecycle Services“** ir susiekite naują užduoties įrašą su ta pačia BPM biblioteka ir verslo procesu, su kuriais susietas pradinis užduoties įrašas.</span><span class="sxs-lookup"><span data-stu-id="758ac-528">Select **Save to Lifecycle Services**, and associate the new task recording with the same BPM library and business process that the original task recording was associated with.</span></span> <span data-ttu-id="758ac-529">Norėdami gauti daugiau informacijos, žr. skyrių [Užduoties įrašo kūrimas ir įrašymas į BPM biblioteką](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="758ac-529">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>
14. <span data-ttu-id="758ac-530">Eikite į BPM biblioteką ir pasirinkite **Sinchronizuoti testavimo atvejus**, kad būtų perrašytas užduoties įrašas, kuris yra pridėtas prie testavimo atvejo „Azure DevOps“, kaip aprašyta skyriuje [Tikrinti sinchronizavimą iš BPM su „Azure DevOps“](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="758ac-530">Go to the BPM library, and select **Sync testcases** to overwrite the task recording that is attached to the test case in Azure DevOps, as described in the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>
15. <span data-ttu-id="758ac-531">Atidarykite RSAT ir pasirinkite **Įkelti**, kad iš naujo būtų įkelti visi testavimo paketo atvejai.</span><span class="sxs-lookup"><span data-stu-id="758ac-531">Open RSAT, and select **Load** to reload all the test cases in the test suite.</span></span> <span data-ttu-id="758ac-532">Turite iš naujo sugeneruoti atitinkamo testavimo atvejo automatizavimo ir parametrų failus, pasirinkdami testavimo atvejį, o tada pasirinkdami **Naujas \> Generuoti testavimo vykdymo ir parametrų failus**, kaip aprašyta skyriuje [Testavimo atvejų įkėlimas ir vykdymas](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="758ac-532">You must regenerate the automation and parameter files for the appropriate test case by selecting the test case and then selecting **New \> Generate Test Execution and Parameter files**, as described in the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="758ac-533">Jei „Excel“ parametrų failas buvo paliktas atidarytas, iš naujo sugeneruoti nepavyks.</span><span class="sxs-lookup"><span data-stu-id="758ac-533">If the Excel parameter file was left open, regeneration will fail.</span></span> <span data-ttu-id="758ac-534">Todėl prieš generuodami naują „Excel“ parametrų failą įsitikinkite, kad „Excel“ parametrų failas yra uždarytas.</span><span class="sxs-lookup"><span data-stu-id="758ac-534">Therefore, make sure that the Excel parameter file for the test case is closed before you generate the new Excel parameter file.</span></span>

16. <span data-ttu-id="758ac-535">Pasirinkite **Redaguoti**, kad būtų atidarytas naujas „Excel“ parametrų failas.</span><span class="sxs-lookup"><span data-stu-id="758ac-535">Select **Edit** to open the new Excel parameter file.</span></span> <span data-ttu-id="758ac-536">9 eilutėje matysite naują įrašą **Įrašytas kintamasis**.</span><span class="sxs-lookup"><span data-stu-id="758ac-536">You will see a new **Saved variable** entry on line 9.</span></span> <span data-ttu-id="758ac-537">Šis kintamasis **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** įrašomas užduoties įrašo XML faile ir gali būti naudojamas vėlesniuose testavimuose.</span><span class="sxs-lookup"><span data-stu-id="758ac-537">This variable, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, is saved in the task recording's XML file and can be used in subsequent tests.</span></span>

    ![Įrašyto kintamojo įrašas](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a><span data-ttu-id="758ac-539">Naujo testavimo atvejo kūrimas</span><span class="sxs-lookup"><span data-stu-id="758ac-539">Create a new test case</span></span>

1. <span data-ttu-id="758ac-540">Eikite į **RSAT** BPM biblioteką.</span><span class="sxs-lookup"><span data-stu-id="758ac-540">Go to the **RSAT** BPM library.</span></span>
2. <span data-ttu-id="758ac-541">Pasirinkite procesą **Pavyzdinis pagalbos verslo procesas**, tada dešinėje pusėje pasirinkite **Redagavimo režimas**.</span><span class="sxs-lookup"><span data-stu-id="758ac-541">Select the **Sample Support Business Process** process, and then, on the right, select **Edit mode**.</span></span>
3. <span data-ttu-id="758ac-542">Pakeiskite abiejų laukų **Pavadinimas** ir **Aprašas** reikšmes, kad būtų **išleistas produktas**.</span><span class="sxs-lookup"><span data-stu-id="758ac-542">Change the value of both the **Name** field and the **Description** field to **Release a product**.</span></span> <span data-ttu-id="758ac-543">Tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-543">Then select **Save**.</span></span>

    ![Pavadinimas ir aprašas pakeisti, kad būtų išleistas produktas](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a><span data-ttu-id="758ac-545">Naujo užduoties įrašo, kuriame būtų funkcija Tikrinti, kūrimas</span><span class="sxs-lookup"><span data-stu-id="758ac-545">Create a new task recording that has a Validate function</span></span>

- <span data-ttu-id="758ac-546">Sukurkite užduoties įrašą, kad būtų išleistas anksčiau USRT juridiniam subjektui sukurtas produktas.</span><span class="sxs-lookup"><span data-stu-id="758ac-546">Create a task recording to release the product that was created earlier to the USRT legal entity.</span></span> <span data-ttu-id="758ac-547">Norėdami gauti daugiau informacijos, žr. skyrių [Užduoties įrašo kūrimas ir įrašymas į BPM biblioteką](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="758ac-547">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="758ac-548">Jei tai yra grandininiai testavimo atvejai, visada rekomenduojame rasti arba filtruoti įrašą, kurio jums reikia, *patiems įvedant lauko vertę*.</span><span class="sxs-lookup"><span data-stu-id="758ac-548">For chained test cases, we always recommend that you find or filter for the record that you require by *manually typing the value of the field*.</span></span> <span data-ttu-id="758ac-549">Tokiu būdu įrankis gali nustatyti įrašą, kuriam turi būti atliktas veiksmas kitame testavimo atvejyje.</span><span class="sxs-lookup"><span data-stu-id="758ac-549">In that way, the tool can determine the record that the action must be taken against in the subsequent test case.</span></span>

    ![Naujas užduoties įrašas, kuriame yra funkcija Tikrinti](./media/setup_rsa_tool_96.png)

    <span data-ttu-id="758ac-551">Kaip rodo ankstesnė iliustracija, kai produktas randamas naudojant spartųjį filtrą, bet prieš jums pasirenkant **Išleisti produktus**, patikrinkite lauko **Produkto numeris** vertę, kad įsitikintumėte, jog produkto ID yra produkto ID, kuris buvo sukurtas anksčiau.</span><span class="sxs-lookup"><span data-stu-id="758ac-551">As the preceding illustration shows, after the product is found by using the Quick Filter, but before you select **Release products**, you validate the value of the **Product number** field to make sure that the product ID is the product ID that was created earlier.</span></span> <span data-ttu-id="758ac-552">Norėdami patikrinti vertę, dešiniuoju pelės mygtuku spustelėkite lauką **Produkto numeris**, tada pasirinkite **Užduočių įrašymo priemonė \> Tikrinti \> Dabartinė vertė**.</span><span class="sxs-lookup"><span data-stu-id="758ac-552">To validate the value, right-click the **Product number** field, and then select **Task recorder \> Validate \> Current Value**.</span></span>

    ![Dabartinės vertės tikrinimas](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a><span data-ttu-id="758ac-554">Užduoties įrašo įrašymas BPM</span><span class="sxs-lookup"><span data-stu-id="758ac-554">Save the task recording to BPM</span></span>

1. <span data-ttu-id="758ac-555">Baigę užduoties įrašą, pasirinkite **Įrašyti į „Lifecycle Services“**.</span><span class="sxs-lookup"><span data-stu-id="758ac-555">After the task recording is completed, select **Save to Lifecycle Services**.</span></span>

    ![Baigtos užduoties įrašo išsaugojimas į „Lifecycle Services”](./media/setup_rsa_tool_98.png)

2. <span data-ttu-id="758ac-557">Bibliotekos informacija įkeliama iš LCS.</span><span class="sxs-lookup"><span data-stu-id="758ac-557">Library information is loaded from LCS.</span></span>

    ![Bibliotekos informacijos įkėlimas iš LCS](./media/setup_rsa_tool_99.png)

3. <span data-ttu-id="758ac-559">Pasirinkti BPM biblioteką, kurią reikia susieti su užduoties įrašu.</span><span class="sxs-lookup"><span data-stu-id="758ac-559">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="758ac-560">Šioje mokomojoje programoje pasirinkite **RSAT** BPM biblioteką, kuri buvo sukurta anksčiau, ir verslo procesą **Išleisti produktą**.</span><span class="sxs-lookup"><span data-stu-id="758ac-560">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Release a product** business process under it.</span></span> <span data-ttu-id="758ac-561">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="758ac-561">Then select **OK**.</span></span>

#### <a name="sync-bpm-to-azure-devops"></a><span data-ttu-id="758ac-562">BPM sinchronizavimas su „Azure DevOps“</span><span class="sxs-lookup"><span data-stu-id="758ac-562">Sync BPM to Azure DevOps</span></span>

1. <span data-ttu-id="758ac-563">Eikite į BPM biblioteką ir atidarykite **RSAT** biblioteką.</span><span class="sxs-lookup"><span data-stu-id="758ac-563">Go to the BPM library, and open the **RSAT** library.</span></span>
2. <span data-ttu-id="758ac-564">Pasirinkite **VSTS sinchronizavimas**, tada pasirinkite **Sinchronizuoti testavimo atvejus**.</span><span class="sxs-lookup"><span data-stu-id="758ac-564">Select **VSTS sync** and then **Sync test cases**.</span></span> <span data-ttu-id="758ac-565">Norėdami gauti daugiau informacijos, žr. skyrių [Tikrinti sinchronizavimą iš BPM su „Azure DevOps“](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="758ac-565">For more information, see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>

    <span data-ttu-id="758ac-566">Baigus sinchronizuoti, naujas verslo proceso **Išleisti produktą** darbo elementas ir atitinkamas testavimo atvejis rodomi „Azure DevOps“ **Sritys \> Darbo elementai**.</span><span class="sxs-lookup"><span data-stu-id="758ac-566">After the synchronization is completed, the new work item and the corresponding test case for the **Release a product** business process appear in Azure DevOps at **Boards \> Work Items**.</span></span>

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a><span data-ttu-id="758ac-567">Naujo testavimo atvejo įtraukimas į esamą testavimo paketą</span><span class="sxs-lookup"><span data-stu-id="758ac-567">Add the new test case to the existing test suite</span></span>

1. <span data-ttu-id="758ac-568">Eikite į **Testavimo planai \> Testavimo planai** ir pasirinkite planą **RSAT testavimo planas**.</span><span class="sxs-lookup"><span data-stu-id="758ac-568">Go to **Test plans \> Test plans**, and select the **RSAT Test Plan** plan.</span></span>
2. <span data-ttu-id="758ac-569">Pasirinkite **Įtraukti esamą**.</span><span class="sxs-lookup"><span data-stu-id="758ac-569">Select **Add existing**.</span></span>
3. <span data-ttu-id="758ac-570">Puslapyje **Įtraukti testavimo atvejus į paketą** pasirinkite **Vykdyti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="758ac-570">On the **Add test cases to suite** page, select **Run query**.</span></span>
4. <span data-ttu-id="758ac-571">Pasirinkite naują testavimo atvejį, kuris buvo sukurtas **Išleisti produktą**, o tada apatiniame dešiniajame puslapio kampe pasirinkite **Įtraukti testavimo atvejus** (šis mygtukas šioje iliustracijoje neparodytas).</span><span class="sxs-lookup"><span data-stu-id="758ac-571">Select the new test case that was created for **Release a product**, and then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Testavimo atvejų įtraukimo į paketą puslapis](./media/setup_rsa_tool_100.png)

    <span data-ttu-id="758ac-573">Dabar testavimo pakete yra du testavimo atvejai.</span><span class="sxs-lookup"><span data-stu-id="758ac-573">The test suite now has two test cases.</span></span>

    ![Du testavimo atvejai testavimo pakete](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a><span data-ttu-id="758ac-575">Testavimo atvejų įkėlimas į RSAT</span><span class="sxs-lookup"><span data-stu-id="758ac-575">Load test cases into RSAT</span></span>

1. <span data-ttu-id="758ac-576">Atidarykite RSAT ir pasirinkite **Įkelti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-576">Open RSAT, and select **Load**.</span></span>
2. <span data-ttu-id="758ac-577">Testavimo atvejai įkeliami, o jūs gausite įspėjimą, kad „Šis veiksmas perrašys „Excel“ testavimo duomenų failus ir vietiniai pakeitimai bus prarasti.</span><span class="sxs-lookup"><span data-stu-id="758ac-577">The test cases are loaded, and you receive a warning that states, "This action will overwrite Excel test data files, local changes will be lost.</span></span> <span data-ttu-id="758ac-578">Ar norite tęsti?“</span><span class="sxs-lookup"><span data-stu-id="758ac-578">Do you want to proceed?"</span></span> <span data-ttu-id="758ac-579">Pasirinkite **Taip**, jei norite atnaujinti „Excel“ parametrų failus vietinėje sistemoje, o ne „Excel“ parametrų failus, nusiųstus į „Azure DevOps“.</span><span class="sxs-lookup"><span data-stu-id="758ac-579">Select **Yes** to update the Excel parameter files in the local system but not the Excel parameter files that were uploaded to Azure DevOps.</span></span>

    ![Šiuo veiksmu bus perrašyti „Excel” tikrinimo duomenų failai](./media/setup_rsa_tool_102.png)

    <span data-ttu-id="758ac-581">Įkeliami abu testavimo atvejai kartu su pirmojo testavimo atveju „Excel“ parametrų failu.</span><span class="sxs-lookup"><span data-stu-id="758ac-581">Both the test cases are loaded, together with the Excel parameter file for the first test case.</span></span> <span data-ttu-id="758ac-582">Kadangi paskutinio vykdymo metu pasirinkote **Nusiųsti**, parametrų failai yra ištraukiami iš „Azure DevOps“.</span><span class="sxs-lookup"><span data-stu-id="758ac-582">Because you selected **Upload** in the last run, the parameter files are pulled from Azure DevOps.</span></span>

    ![Įkelti testavimo atvejai](./media/setup_rsa_tool_103.png)

3. <span data-ttu-id="758ac-584">Pasirinkite tik antrą testavimo atvejį ir pasirinkite **Naujas \> Generuoti testavimo vykdymo ir parametrų failus**.</span><span class="sxs-lookup"><span data-stu-id="758ac-584">Select only the second test case, and then select **New \> Generate test execution and parameter files**.</span></span>

#### <a name="edit-the-excel-parameter-file"></a><span data-ttu-id="758ac-585">„Excel“ parametrų failo redagavimas</span><span class="sxs-lookup"><span data-stu-id="758ac-585">Edit the Excel parameter file</span></span>

1. <span data-ttu-id="758ac-586">Pasirinkite tik antrą testavimo atvejį ir pasirinkite **Redaguoti**, kad atidarytumėte atitinkamą „Excel“ parametrų failą.</span><span class="sxs-lookup"><span data-stu-id="758ac-586">Select only the second test case, and then select **Edit** to open the corresponding Excel parameter file.</span></span>
2. <span data-ttu-id="758ac-587">Kopijuokite **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** įrašytą kintamąjį (žr. skyrių [Esamo užduoties įrašo modifikavimas įrašytam kintamajam sukurti](#modify-an-existing-task-recording-to-create-a-saved-variable)) iš pirmo testavimo atvejo į visus laukus, kur naudojamas produkto numeris.</span><span class="sxs-lookup"><span data-stu-id="758ac-587">Copy the **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** saved variable (see the [Modify an existing task recording to create a saved variable](#modify-an-existing-task-recording-to-create-a-saved-variable) section) from the first test case into all the fields where the product number is used.</span></span> <span data-ttu-id="758ac-588">Šiuo atveju nukopijuojate kintamąjį į laukus **Produkto numeris** ir **Tikrinti produkto numerį**, esančius lape **EcoResProductListPage**.</span><span class="sxs-lookup"><span data-stu-id="758ac-588">In this case, you copy the variable into the **Product number** and **Validate Product number** fields on the **EcoResProductListPage** sheet.</span></span>

    ![Laukai Produkto numeris ir Tikrinti produkto numerį](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > <span data-ttu-id="758ac-590">Kintamuosius galima perduoti iš vieno testo į kitą tik to paties testavimo vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="758ac-590">Variables can be passed between tests only during the same test run.</span></span> <span data-ttu-id="758ac-591">Kintamųjų pavadinimai turi tiksliai sutapti.</span><span class="sxs-lookup"><span data-stu-id="758ac-591">The names of the variables must match exactly.</span></span>

3. <span data-ttu-id="758ac-592">Pasirinkite **Įrašyti** ir uždarykite „Excel“ darbaknygę.</span><span class="sxs-lookup"><span data-stu-id="758ac-592">Select **Save**, and then close the Excel workbook.</span></span>
4. <span data-ttu-id="758ac-593">Pasirinkite **Nusiųsti**, kad įrašytumėte keitimus, atliktus „Excel“ parametrų faile.</span><span class="sxs-lookup"><span data-stu-id="758ac-593">Select **Upload** to save the changes that you made to the Excel parameter file.</span></span>

#### <a name="run-the-chained-test-cases"></a><span data-ttu-id="758ac-594">Grandininių testavimo atvejų vykdymas</span><span class="sxs-lookup"><span data-stu-id="758ac-594">Run the chained test cases</span></span>

1. <span data-ttu-id="758ac-595">Pasirinkite abu testavimo atvejus ir pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="758ac-595">Select both the test cases, and then select **Run**.</span></span>
2. <span data-ttu-id="758ac-596">Patikrinkite, ar abiejų testavimo atvejų rezultatai teigiami.</span><span class="sxs-lookup"><span data-stu-id="758ac-596">Verify that both test cases have passed.</span></span>

    ![Rezultatų laukas nustatytas kaip Sėkmingas abiejų testavimo atvejų](./media/setup_rsa_tool_105.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]