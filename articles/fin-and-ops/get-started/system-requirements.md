---
title: "Įdiegtims debesyje taikomi sistemos reikalavimai"
description: "Šioje temoje išvardyti šiai „Microsoft Dynamics 365 Finance and Operations“ „Enterprise‟ leidimo versijai (įdiegtims debesyje) taikomi sistemos reikalavimai."
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 83637b4b2ccc01950e68569b3b8bee1a7cd69855
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="system-requirements-for-cloud-deployments"></a><span data-ttu-id="2d153-103">Įdiegtims debesyje taikomi sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="2d153-103">System requirements for cloud deployments</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2d153-104">Šioje temoje išvardyti šiai „Microsoft Dynamics 365 Finance and Operations“ „Enterprise‟ leidimo versijai (įdiegtims debesyje) taikomi sistemos reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="2d153-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for cloud deployments.</span></span> <span data-ttu-id="2d153-105">Prieš diegdami „Finance and Operations“, kai galėsite, patikrinkite, ar sistema, kurią naudojate, atitinka arba viršija minimalius tinklo, aparatūros ir programinės įrangos reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="2d153-105">Before you install Finance and Operations, when this step is appropriate, verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="2d153-106">Palaikomos žiniatinklio naršyklės</span><span class="sxs-lookup"><span data-stu-id="2d153-106">Supported web browsers</span></span>
<span data-ttu-id="2d153-107">Žiniatinklio programa gali veikti bet kurioje iš tolesnių žiniatinklio naršyklių, veikiančių nurodytose operacinėse sistemose.</span><span class="sxs-lookup"><span data-stu-id="2d153-107">The web application can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="2d153-108">„Microsoft Edge‟ (naujausia viešai pasiekiama versija) sistemoje „Windows 10‟.</span><span class="sxs-lookup"><span data-stu-id="2d153-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="2d153-109">„Internet Explorer 11‟ sistemose „Windows 10‟, „Windows 8.1‟ arba „Windows 7‟.</span><span class="sxs-lookup"><span data-stu-id="2d153-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="2d153-110">„Google Chrome‟ (naujausia viešai pasiekiama versija) sistemose „Windows 10‟, „Windows 8.1‟, „Windows 8‟, „Windows 7‟ arba planšetėje „Google Nexus 10‟.</span><span class="sxs-lookup"><span data-stu-id="2d153-110">Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet</span></span>
-   <span data-ttu-id="2d153-111">„Apple Safari‟ (naujausia viešai pasiekiama versija) sistemoje „Mac OS X 10.10‟ („Yosemite‟), 10.11 („El Capitan‟) arba 10.12 („Sierra‟) arba planšetėje „Apple iPad‟.</span><span class="sxs-lookup"><span data-stu-id="2d153-111">Apple Safari (latest publicly available version) on Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) or 10.12 (Sierra), or Apple iPad</span></span>

<span data-ttu-id="2d153-112">Norėdami rasti naujausią kiekvienos žiniatinklio naršyklės leidimą, eikite į programinės įrangos gamintojo svetainę.</span><span class="sxs-lookup"><span data-stu-id="2d153-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> -   <span data-ttu-id="2d153-113">Kad užduočių įrašymo priemonė galėtų fiksuoti ekrano nuotraukas ir įtraukti į sugeneruotus „Microsoft Word‟ dokumentus, būtina įdiegti negalutinį „Chrome‟ plėtinį.</span><span class="sxs-lookup"><span data-stu-id="2d153-113">You must install a pre-release Chrome extension to enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated.</span></span> <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> -   <span data-ttu-id="2d153-114">Darbo eigos rengyklė paleidžiama kaip „ClickOnce“ taikomoji programa.</span><span class="sxs-lookup"><span data-stu-id="2d153-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="2d153-115">Tik „Microsoft Edge“ ir „Internet Explorer“ (palaikomoje „Microsoft Windows“ versijoje) palaiko „ClickOnce“ taikomąsias programas.</span><span class="sxs-lookup"><span data-stu-id="2d153-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="2d153-116">Darbo eigos rengyklės „ClickOnce“ taikomajai programai reikia 64 bitų suderinamos operacinės sistemos.</span><span class="sxs-lookup"><span data-stu-id="2d153-116">The Workflow Editor ClickOnce application requires a 64-bit-compatible operating system.</span></span>
> -   <span data-ttu-id="2d153-117">Finansinėms ataskaitoms skirtas ataskaitų konstruktorius paleidžiama kaip „ClickOnce“ taikomoji programa.</span><span class="sxs-lookup"><span data-stu-id="2d153-117">The Report Designer for Financial reporting is started as a ClickOnce application.</span></span> <span data-ttu-id="2d153-118">Jam reikia 64 bitų suderinamos operacinės sistemos.</span><span class="sxs-lookup"><span data-stu-id="2d153-118">It requires a 64-bit-compatible operating system.</span></span> <span data-ttu-id="2d153-119">Jei naudojate „Chrome“, turite įdiegti plėtinį „ClickOnce“, kad galėtumėte atsisiųsti ataskaitų dizaino įrankio klientą.</span><span class="sxs-lookup"><span data-stu-id="2d153-119">If you’re using Chrome, you must install a ClickOnce extension to download the Report Designer client.</span></span> <span data-ttu-id="2d153-120">Jei naudojate „Chrome“ inkognito režimu, įsitikinkite, kad plėtinys „ClickOnce“ nustatytas veikti ir inkognito režimu.</span><span class="sxs-lookup"><span data-stu-id="2d153-120">If you use Chrome in Incognito mode, make sure that the ClickOnce extension is also enabled for Incognito mode.</span></span>
> -   <span data-ttu-id="2d153-121">Norint peržiūrėti PDF failus, rekomenduojame naudoti naršykles, pvz., „Microsoft Edge“ (naujausią viešai prieinamą versiją) sistemoje „Windows 10“ arba „Google Chrome“ (naujausią viešai prieinamą versiją) sistemoje „Windows 10“, „Windows 8.1“, „Windows 8“ ar „Windows 7“ arba „Google" Nexus 10“ planšetiniame kompiuteryje.</span><span class="sxs-lookup"><span data-stu-id="2d153-121">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>

### <a name="supported-web-browsers-for-retail-cloud-pos"></a><span data-ttu-id="2d153-122">Palaikomos „Retail Cloud POS‟ žiniatinklio naršyklės</span><span class="sxs-lookup"><span data-stu-id="2d153-122">Supported web browsers for Retail Cloud POS</span></span>

<span data-ttu-id="2d153-123">„Retail Cloud POS‟ gali veikti bet kurioje iš tolesnių žiniatinklio naršyklių, veikiančių nurodytose operacinėse sistemose.</span><span class="sxs-lookup"><span data-stu-id="2d153-123">Retail Cloud POS can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="2d153-124">„Microsoft Edge‟ (naujausia viešai pasiekiama versija) sistemoje „Windows 10‟.</span><span class="sxs-lookup"><span data-stu-id="2d153-124">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="2d153-125">„Internet Explorer 11‟ sistemose „Windows 10‟, „Windows 8.1‟ arba „Windows 7‟.</span><span class="sxs-lookup"><span data-stu-id="2d153-125">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="2d153-126">„Chrome‟ (naujausia viešai pasiekiama versija) sistemoje „Windows 10‟, „Windows 8.1“ arba „Windows 7“.</span><span class="sxs-lookup"><span data-stu-id="2d153-126">Chrome (latest publicly available version) on Windows 10, Windows 8.1, or Windows 7</span></span>

## <a name="network-requirements"></a><span data-ttu-id="2d153-127">Tinklo reikalavimai</span><span class="sxs-lookup"><span data-stu-id="2d153-127">Network requirements</span></span>
-   <span data-ttu-id="2d153-128">„Finance and Operations“ skirta tinklams, kurių laukimo laikas ne didesnis nei 250–300 milisekundžių (ms).</span><span class="sxs-lookup"><span data-stu-id="2d153-128">Finance and Operations is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="2d153-129">Tai – laukimo laikas iš naršyklės kliento iki „Microsoft Azure“ duomenų centro, kuriame yra „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="2d153-129">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts Finance and Operations.</span></span> <span data-ttu-id="2d153-130">Rekomenduojame tinklo laukimo laiką patikrinti <http://www.azurespeed.com>.</span><span class="sxs-lookup"><span data-stu-id="2d153-130">We recommend that you test network latency at <http://www.azurespeed.com>.</span></span>
-   <span data-ttu-id="2d153-131">„Finance and Operations“ pralaidumo reikalavimai priklauso nuo jūsų scenarijaus.</span><span class="sxs-lookup"><span data-stu-id="2d153-131">Bandwidth requirements for Finance and Operations depend on your scenario.</span></span> <span data-ttu-id="2d153-132">Labiausiai įprastiems scenarijams reikia didesnio nei 50 kilobitų per sekundę (KB/s) pralaidumo.</span><span class="sxs-lookup"><span data-stu-id="2d153-132">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="2d153-133">Tačiau tiems scenarijams, kurių mokamosios krovos reikalavimai aukšti, pvz., darbo sritims arba scenarijams, kurie apima nemažai tinkinimo, rekomenduojamas didesnis pralaidumas.</span><span class="sxs-lookup"><span data-stu-id="2d153-133">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="2d153-134">Apskritai „Finance and Operations“ yra optimizuotas internetui.</span><span class="sxs-lookup"><span data-stu-id="2d153-134">In general, Finance and Operations is optimized for the internet.</span></span> <span data-ttu-id="2d153-135">Kreipimosi ciklų iš naršyklės kliento į „Azure“ duomenų centrą skaičius yra labai mažas, o visa mokamoji krova yra suglaudinta.</span><span class="sxs-lookup"><span data-stu-id="2d153-135">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span> 

> [!WARNING]
> <span data-ttu-id="2d153-136">Neskaičiuokite pralaidumo iš kliento vietos reikalavimų, vartotojų skaičių padauginę iš minimalių pralaidumo reikalavimų.</span><span class="sxs-lookup"><span data-stu-id="2d153-136">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="2d153-137">Tam tikros vietos naudojimą vienu metu labai sunku apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="2d153-137">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="2d153-138">Klientams, kurie susirūpinę dėl pralaidumo reikalavimų, rekomenduojama naudoti „Finance and Operations“ peržiūros versiją.</span><span class="sxs-lookup"><span data-stu-id="2d153-138">Customers who are concerned about bandwidth requirements should use a preview version of Finance and Operations.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="2d153-139">„.NET Framework“ reikalavimai</span><span class="sxs-lookup"><span data-stu-id="2d153-139">.NET Framework requirements</span></span>
<span data-ttu-id="2d153-140">„Finance and Operations“ reikia „Microsoft.NET Framework“ 4.6.2 versijos visoms vieno paspaudimo taikomosioms programoms, pvz., dokumento maršruto planavimo agentui.</span><span class="sxs-lookup"><span data-stu-id="2d153-140">Finance and Operations requires the Microsoft .NET Framework version 4.6.2 for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="2d153-141">Diegimo instrukcijų žr. [„.NET Framework“ diegimas](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="2d153-141">For installation instructions, see [Installing the .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="2d153-142">Palaikomos „Microsoft Office“ taikomosios programos</span><span class="sxs-lookup"><span data-stu-id="2d153-142">Supported Microsoft Office applications</span></span>
<span data-ttu-id="2d153-143">„Finance and Operations“ įdiegtys debesyje ir vietinės įdiegtys palaiko toliau nurodytas „Microsoft Office“ programas.</span><span class="sxs-lookup"><span data-stu-id="2d153-143">The following Microsoft Office applications are supported in cloud and on-premises deployments of Finance and Operations:</span></span>

-   <span data-ttu-id="2d153-144">Kad galėtumėte naudoti „Microsoft Excel“ papildinius, turi būti įdiegta „Windows“ arba „Mac“ skirta „Microsoft Office 2016“.</span><span class="sxs-lookup"><span data-stu-id="2d153-144">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="2d153-145">Išsamios informacijos apie versijų reikalavimus žr. [„Office“ integravimo trikčių šalinimas](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="2d153-145">For more information about version requirements, see [Office integration troubleshooting](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span></span>
-   <span data-ttu-id="2d153-146">Norėdami peržiūrėti dokumentus, sugeneruotus naudojant funkciją Eksportuoti į „Excel“ arba Eksportuoti į „Word“, turi būti įdiegta „Microsoft Office 2007“ arba naujesnė versija.</span><span class="sxs-lookup"><span data-stu-id="2d153-146">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="retail-modern-pos-requirements"></a><span data-ttu-id="2d153-147">„Retail Modern POS“ reikalavimai</span><span class="sxs-lookup"><span data-stu-id="2d153-147">Retail Modern POS requirements</span></span>

> [!NOTE]
> <span data-ttu-id="2d153-148">Jei „Retail Modern POS“ naudos autonominę duomenų bazę, kompiuteris turi atitikti visus sistemos reikalavimus, skirtus „Microsoft SQL Server“.</span><span class="sxs-lookup"><span data-stu-id="2d153-148">If Retail Modern POS will use an offline database, the computer must meet all system requirements for Microsoft SQL Server.</span></span> <span data-ttu-id="2d153-149">„Retail Modern POS“ autonominė duomenų bazė veiks „Microsoft SQL Server 2012“ su 3 pakeitimų paketu ar vėlesnėje versijoje, „Microsoft SQL Server 2014“ su 2 pakeitimų paketu ar vėlesnėje versijoje ir „Microsoft SQL Server 2016“.</span><span class="sxs-lookup"><span data-stu-id="2d153-149">A Retail Modern POS offline database will work on Microsoft SQL Server 2012 with Service Pack 3 or later, Microsoft SQL Server 2014 with Service Pack 2 or later, and Microsoft SQL Server 2016.</span></span> <span data-ttu-id="2d153-150">Rekomenduojame visada naudoti naujausią versiją ir įdiegti naujausius pakeitimų paketus.</span><span class="sxs-lookup"><span data-stu-id="2d153-150">We recommend that you always use the latest version that is available, and that you install all the latest service packs.</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="2d153-151">Palaikomos operacinės sistemos</span><span class="sxs-lookup"><span data-stu-id="2d153-151">Supported operating systems</span></span>

-   <span data-ttu-id="2d153-152">„Retail Modern POS“ yra 32 bitų taikomoji programa, bet ji vykdoma ir x86, ir x64 architektūrose.</span><span class="sxs-lookup"><span data-stu-id="2d153-152">Retail Modern POS is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="2d153-153">„Retail Modern POS“ palaikoma tik „Windows 10 Pro“, „Enterprise“ ir „Enterprise Long Term Servicing Branch“ (LTSB) leidimai.</span><span class="sxs-lookup"><span data-stu-id="2d153-153">Retail Modern POS is supported only on Windows 10 Pro, Enterprise, and Enterprise Long Term Servicing Branch (LTSB) editions.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="2d153-154">Minimalūs sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="2d153-154">Minimum system requirements</span></span>

-   <span data-ttu-id="2d153-155">Mažiausia palaikoma skiriamoji geba yra 1280 × 1024.</span><span class="sxs-lookup"><span data-stu-id="2d153-155">The minimum supported resolution is 1,280 × 1,024.</span></span>
-   <span data-ttu-id="2d153-156">Kompiuteris, kuriame vykdoma „Retail Modern POS“, turi atitikti šiuos reikalavimus:</span><span class="sxs-lookup"><span data-stu-id="2d153-156">The computer that Retail Modern POS runs on must meet these requirements:</span></span>

    -   <span data-ttu-id="2d153-157">Jame turi būti mažiausiai dviejų branduolių procesorius, veikiantis ne mažiau kaip 2 gigahercų (GHz) dažniu.</span><span class="sxs-lookup"><span data-stu-id="2d153-157">It must have, at a minimum, a dual-core processor that runs at no less than 2 gigahertz (GHz).</span></span>
    -   <span data-ttu-id="2d153-158">Turi turėti mažiausiai 3 gigabaitus (GB) RAM.</span><span class="sxs-lookup"><span data-stu-id="2d153-158">It must have, at a minimum, 3 gigabytes (GB) of random-access memory (RAM).</span></span>
    -   <span data-ttu-id="2d153-159">Būtina interneto prieiga.</span><span class="sxs-lookup"><span data-stu-id="2d153-159">It must have internet access.</span></span>

## <a name="retail-hardware-station-requirements"></a><span data-ttu-id="2d153-160">„Retail“ aparatūros stoties reikalavimai</span><span class="sxs-lookup"><span data-stu-id="2d153-160">Retail hardware station requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="2d153-161">Palaikomos operacinės sistemos</span><span class="sxs-lookup"><span data-stu-id="2d153-161">Supported operating systems</span></span>

-   <span data-ttu-id="2d153-162">„Retail“ aparatūros stotis yra 32 bitų taikomoji programa, bet ji vykdoma ir x86, ir x64 architektūrose.</span><span class="sxs-lookup"><span data-stu-id="2d153-162">Retail hardware station is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="2d153-163">„Retail“ aparatūros stotį palaiko šios operacinės sistemos:</span><span class="sxs-lookup"><span data-stu-id="2d153-163">Retail hardware station is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="2d153-164">„Windows 7 Professional“, „Enterprise“ ir „Ultimate“ leidimuose</span><span class="sxs-lookup"><span data-stu-id="2d153-164">Windows 7 Professional, Enterprise, and Ultimate editions</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="2d153-165">„Windows 7“ palaikoma tik jei sistemoje neautomatiškai įdiegta „Internet Explorer 11“.</span><span class="sxs-lookup"><span data-stu-id="2d153-165">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>

    -   <span data-ttu-id="2d153-166">„Windows 8.1“ 1 naujinimas „Professional“, „Enterprise“ ir įdėtieji leidimai</span><span class="sxs-lookup"><span data-stu-id="2d153-166">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="2d153-167">„Windows 10 Pro“, „Enterprise“ ir „Enterprise LTSB“ leidimai</span><span class="sxs-lookup"><span data-stu-id="2d153-167">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="2d153-168">Minimalūs sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="2d153-168">Minimum system requirements</span></span>

<span data-ttu-id="2d153-169">Kompiuteris turi atitikti visus sistemos reikalavimus, norint įdiegti ir naudoti šiuos elementus:</span><span class="sxs-lookup"><span data-stu-id="2d153-169">The computer must meet all system requirements for installing and using the following items:</span></span>

-   <span data-ttu-id="2d153-170">Interneto informacijos tarnybos (IIS)</span><span class="sxs-lookup"><span data-stu-id="2d153-170">Internet Information Services (IIS)</span></span>
-   <span data-ttu-id="2d153-171">trečiųjų šalių aparatūrą;</span><span class="sxs-lookup"><span data-stu-id="2d153-171">Third-party hardware</span></span>

## <a name="retail-store-scale-unit-requirements"></a><span data-ttu-id="2d153-172">„Retail Store Scale Unit“ reikalavimus;</span><span class="sxs-lookup"><span data-stu-id="2d153-172">Retail Store Scale Unit requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="2d153-173">palaikomas operacines sistemas.</span><span class="sxs-lookup"><span data-stu-id="2d153-173">Supported operating systems</span></span>

-   <span data-ttu-id="2d153-174">„Retail Store Scale Unit“ yra 32 bitų taikomoji programa, bet vykdoma ir x86, ir x64 architektūrose.</span><span class="sxs-lookup"><span data-stu-id="2d153-174">Retail Store Scale Unit is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="2d153-175">„Retail Store Scale Unit“ palaikoma šiose operacinėse sistemose:</span><span class="sxs-lookup"><span data-stu-id="2d153-175">Retail Store Scale Unit is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="2d153-176">„Windows 7 Professional“, „Enterprise“ ir „Ultimate“ leidimuose</span><span class="sxs-lookup"><span data-stu-id="2d153-176">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="2d153-177">„Windows 8.1“ 1 naujinimas „Professional“, „Enterprise“ ir įdėtieji leidimai</span><span class="sxs-lookup"><span data-stu-id="2d153-177">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="2d153-178">„Windows 10 Pro“, „Enterprise“ ir „Enterprise LTSB“ leidimai</span><span class="sxs-lookup"><span data-stu-id="2d153-178">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="2d153-179">Minimalūs sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="2d153-179">Minimum system requirements</span></span>

-   <span data-ttu-id="2d153-180">4 GB RAM</span><span class="sxs-lookup"><span data-stu-id="2d153-180">4 GB of RAM</span></span>
-   <span data-ttu-id="2d153-181">1,6 GHz didžiausia CPU sparta branduolyje (Mažiausiai dviejų branduolių.)</span><span class="sxs-lookup"><span data-stu-id="2d153-181">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="2d153-182">Bent 10 GB laisvos vietos (Kanalo duomenų bazei reikia daug vietos.)</span><span class="sxs-lookup"><span data-stu-id="2d153-182">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

### <a name="recommended-system-requirements"></a><span data-ttu-id="2d153-183">Rekomenduojami sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="2d153-183">Recommended system requirements</span></span>

-   <span data-ttu-id="2d153-184">6 GB RAM</span><span class="sxs-lookup"><span data-stu-id="2d153-184">6 GB of RAM</span></span>
-   <span data-ttu-id="2d153-185">2,4 GHz i7 (arba atitikmuo) didžiausia CPU sparta branduolyje (Rekomenduojama keturių branduolių.)</span><span class="sxs-lookup"><span data-stu-id="2d153-185">2.4 GHz i7 (or equivalent) peak CPU speed per core (Four cores are recommended.)</span></span>
-   <span data-ttu-id="2d153-186">Bent 10 GB laisvos vietos (Kanalo duomenų bazei reikia daug vietos.)</span><span class="sxs-lookup"><span data-stu-id="2d153-186">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="connector-requirements"></a><span data-ttu-id="2d153-187">Jungčių reikalavimai</span><span class="sxs-lookup"><span data-stu-id="2d153-187">Connector requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="2d153-188">Palaikomos operacinės sistemos</span><span class="sxs-lookup"><span data-stu-id="2d153-188">Supported operating systems</span></span>

-   <span data-ttu-id="2d153-189">„Microsoft Dynamics AX‟ jungtis turi dvi atskiras diegimo programas – vieną „Async Server Connector service‟ ir vieną „Real-time service for Dynamics AX 2012 R3‟.</span><span class="sxs-lookup"><span data-stu-id="2d153-189">The Connector for Microsoft Dynamics AX has two separate installers, one for Async Server Connector service and one for Real-time service for Dynamics AX 2012 R3.</span></span>
-   <span data-ttu-id="2d153-190">Abu komponentai yra 32 bitų programos, tačiau veikia ir x86, ir x64 architektūrose.</span><span class="sxs-lookup"><span data-stu-id="2d153-190">Both components are 32-bit applications, but they will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="2d153-191">Abu komponentai palaikomi tolesnėse operacinėse sistemose.</span><span class="sxs-lookup"><span data-stu-id="2d153-191">Both components are supported on the following operating systems:</span></span>

    -   <span data-ttu-id="2d153-192">„Windows 7 Professional“, „Enterprise“ ir „Ultimate“ leidimuose</span><span class="sxs-lookup"><span data-stu-id="2d153-192">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="2d153-193">„Windows 8.1“ 1 naujinimas „Professional“, „Enterprise“ ir įdėtieji leidimai</span><span class="sxs-lookup"><span data-stu-id="2d153-193">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="2d153-194">„Windows 10 Pro“, „Enterprise“ ir „Enterprise LTSB“ leidimai</span><span class="sxs-lookup"><span data-stu-id="2d153-194">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>
    -   <span data-ttu-id="2d153-195">„Microsoft Windows Server 2012 R2“ ir „Microsoft Windows Server 2016“</span><span class="sxs-lookup"><span data-stu-id="2d153-195">Microsoft Windows Server 2012 R2 and Microsoft Windows Server 2016</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="2d153-196">Minimalūs sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="2d153-196">Minimum system requirements</span></span>
-   <span data-ttu-id="2d153-197">2 GB RAM, (rekomenduojama 4 GB RAM).</span><span class="sxs-lookup"><span data-stu-id="2d153-197">2 GB of RAM (4 GB of RAM are recommended.)</span></span>
-   <span data-ttu-id="2d153-198">1,6 GHz didžiausia CPU sparta branduolyje (Mažiausiai dviejų branduolių.)</span><span class="sxs-lookup"><span data-stu-id="2d153-198">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="2d153-199">Bent 10 GB laisvos vietos (Kanalo duomenų bazei reikia daug vietos.)</span><span class="sxs-lookup"><span data-stu-id="2d153-199">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="2d153-200">Reikalavimai norint kurti vietiniuose virtualiuosiuose įrenginiuose</span><span class="sxs-lookup"><span data-stu-id="2d153-200">Requirements for development on local VMs</span></span>
<span data-ttu-id="2d153-201">Išsamesnės informacijos apie reikalavimus norint kurti vietiniuose virtualiuosiuose įrenginiuose (VM) žr. [VM vykdymas vietoje](../../dev-itpro/dev-tools/access-instances.md).</span><span class="sxs-lookup"><span data-stu-id="2d153-201">For information about the requirements for development on local virtual machines (VMs), see [VM running on-premises](../../dev-itpro/dev-tools/access-instances.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="2d153-202">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="2d153-202">See also</span></span>

[<span data-ttu-id="2d153-203">„Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidimo įvertinimo kopijos gavimas</span><span class="sxs-lookup"><span data-stu-id="2d153-203">Get an evaluation copy of Dynamics 365 for Finance and Operations, Enterprise edition</span></span>](../../dev-itpro/dev-tools/get-evaluation-copy.md)

