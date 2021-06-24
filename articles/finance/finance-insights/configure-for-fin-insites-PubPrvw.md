---
title: „Finance Insights“ konfigūracija, skirta viešai peržiūrai (peržiūra) – 10.0.20 ir vėlesnė versija
description: Šioje temoje paaiškinami kaip konfigūruoti sistemą su galimybėmis prieinamomis „Finance Insights” viešos peržiūros versijoje 10.0.20 ir vėlesnėse.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 613bd4816e2f0c4fbb56cf79779a08c6a09592bd
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222617"
---
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a><span data-ttu-id="c4bad-103">„Finance Insights“ konfigūracija, skirta viešai peržiūrai (peržiūra) – 10.0.20 ir vėlesnė versija</span><span class="sxs-lookup"><span data-stu-id="c4bad-103">Configuration for Finance insights for public preview (preview) - version 10.0.20 and later</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c4bad-104">Modulyje „Finance Insights” sujungiamos „Microsoft Dynamics 365 Finance“ ir „Dataverse“, „Azure“ bei „AI Builder“ funkcijos, kad jūsų organizacijai būtų suteikiami galingi prognozavimo įrankiai.</span><span class="sxs-lookup"><span data-stu-id="c4bad-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="c4bad-105">Šioje temoje paaiškinami kaip konfigūruoti sistemą su „Dynamics 365 Finance“ versija 10.0.20 tam, kad galėtumėte naudoti galimybes prieinamas „Finance Insights“ viešojoje peržiūroje.</span><span class="sxs-lookup"><span data-stu-id="c4bad-105">This topic explains how to configure Dynamics 365 Finance version 10.0.20 so that your system can use the capabilities that are available in Finance insights public preview.</span></span>

> [!NOTE]
> <span data-ttu-id="c4bad-106">Šioje temoje aprašyti konfigūracijos veiksmai taikomi tik „Finance“ versijai 10.0.20 arba vėlesnei finansų versijai.</span><span class="sxs-lookup"><span data-stu-id="c4bad-106">The configuration steps that are described in this topic apply only to Finance version 10.0.20 and later.</span></span> <span data-ttu-id="c4bad-107">Norėdami nustatyti finansų žinių apie 10.0.19 ir ankstesnę versiją,[žr. „Finance Insights“ versijos iki 10.0.18 ir vėlesnės](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="c4bad-107">'To set up Finance insights on version 10.0.19 and earlier, see [Configuration for Finance insights - versions up to 10.0.18](configure-for-fin-insites.md).</span></span>

## <a name="deploy-finance"></a><span data-ttu-id="c4bad-108">Finansų diegimas</span><span class="sxs-lookup"><span data-stu-id="c4bad-108">Deploy Finance</span></span>

<span data-ttu-id="c4bad-109">Norėdami talpinti aplinkas, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c4bad-109">Follow these steps to deploy the environments.</span></span>

1. <span data-ttu-id="c4bad-110">Portale „Microsoft Dynamics Lifecycle Services“ (LCS), kurkite ar naujinkite „Finance“ aplinką.</span><span class="sxs-lookup"><span data-stu-id="c4bad-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Finance environment.</span></span> <span data-ttu-id="c4bad-111">Aplinkai reikalinga programos 10.0.20 versija ar naujesnė „Finance and Operations“ programoms.</span><span class="sxs-lookup"><span data-stu-id="c4bad-111">The environment requires app version 10.0.20 or later of Finance and Operations apps.</span></span>
2. <span data-ttu-id="c4bad-112">Aplinka turi būti didelio pasiekiamumo (HA) smėlio dėžės aplinka.</span><span class="sxs-lookup"><span data-stu-id="c4bad-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="c4bad-113">(Šis aplinkos tipas dar vadinamas 2 pakopos aplinka.) Norėdami gauti daugiau informacijos, žr. [Aplinkos planavimas](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="c4bad-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="c4bad-114">Jei konfigūruojate „Finance Insights“ smėlio dėžės aplinkoje, jums gali tekti nukopijuoti gamybos duomenis į tą aplinką numatymams dirbti.</span><span class="sxs-lookup"><span data-stu-id="c4bad-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="c4bad-115">Numatymo modelis naudoja kelių metų duomenis numatymams sukurti.</span><span class="sxs-lookup"><span data-stu-id="c4bad-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="c4bad-116">„Contoso“ demonstruojamuose duomenyse nėra pakankamai praeities duomenų, kad būtų galima nuspėti numatymo modelį.</span><span class="sxs-lookup"><span data-stu-id="c4bad-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="c4bad-117">Konfigūruoti „Dataverse“</span><span class="sxs-lookup"><span data-stu-id="c4bad-117">Configure Dataverse</span></span>

<span data-ttu-id="c4bad-118">Norėdami sukonfigūruoti „Finance insights“, „Dataverse“ atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c4bad-118">Follow these steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="c4bad-119">Atidarykite aplinkos puslapį LCS ir patikrinkite, ar **„Power Platform“** integravimo skyrius jau sąranka.</span><span class="sxs-lookup"><span data-stu-id="c4bad-119">In LCS, open the environment page, and verify that the **Power Platform Integration** section is already set up.</span></span>

    - <span data-ttu-id="c4bad-120">Jei jis jau nustatytas, turi „Dataverse“ būti pateiktas su aplinka susietas aplinkos „Finance“ sąrašu.</span><span class="sxs-lookup"><span data-stu-id="c4bad-120">If it's already set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>
    - <span data-ttu-id="c4bad-121">Jei ji nenustatyta, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="c4bad-121">If it isn't yet set up, follow these steps:</span></span>

        1. <span data-ttu-id="c4bad-122">**„Power Platform“ integravimas** srityje rinkitės **Nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-122">In the **Power Platform Integration** section, select **Setup**.</span></span> <span data-ttu-id="c4bad-123">Aplinkos nustatymas gali užtrukti iki valandos.</span><span class="sxs-lookup"><span data-stu-id="c4bad-123">Setup of the environment might take up to an hour.</span></span>
        2. <span data-ttu-id="c4bad-124">Jei „Dataverse“ aplinka sėkmingai nustatyta, „Dataverse“ aplinkos pavadinimas susietas su „Finance“ aplinka sąraše.</span><span class="sxs-lookup"><span data-stu-id="c4bad-124">If the Dataverse environment is successfully set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>

        > [!NOTE]
        > <span data-ttu-id="c4bad-125">Užbaigę aplinkos sąranką **ne** pasirinkite **Susieti programėlių CDS**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-125">After you complete the environment setup, do **not** select **Link to CDS for Apps**.</span></span> <span data-ttu-id="c4bad-126">Šis mygtukas nebūtinas norint gauti „Finance insights“.</span><span class="sxs-lookup"><span data-stu-id="c4bad-126">This button isn't required for Finance insights.</span></span> <span data-ttu-id="c4bad-127">Jei jį pasirinksite, negalėsite konfigūruoti reikiamos aplinkos papildiniai LCS.</span><span class="sxs-lookup"><span data-stu-id="c4bad-127">If you select it, you won't be able to configure the required environment add-ins in LCS.</span></span>

## <a name="configure-azure"></a><span data-ttu-id="c4bad-128">Konfigūruoti „Azure"</span><span class="sxs-lookup"><span data-stu-id="c4bad-128">Configure Azure</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="c4bad-129">„Azure Cloud Shell“ naudojimas modulio „Finance Insights” „Data Lake“ ištekliams nustatyti</span><span class="sxs-lookup"><span data-stu-id="c4bad-129">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="c4bad-130">„Windows PowerShell“ scenarijaus naudojimas</span><span class="sxs-lookup"><span data-stu-id="c4bad-130">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="c4bad-131">Pateiktas „Windows PowerShell“ scenarijus, kad būtų galima lengvai nustatyti „Azure“ išteklius, aprašytus temoje [Eksportavimo į „Azure Data Lake“ konfigūravimas](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="c4bad-131">A Windows PowerShell script has been provided so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="c4bad-132">Jei norite nustatyti rankiniu būdu, praleiskite šią procedūrą ir užbaikite procedūrą, aprašytą [Neautomatinė sąranka](#manual-setup) skyriuje.</span><span class="sxs-lookup"><span data-stu-id="c4bad-132">If you prefer to do the setup manually, skip this procedure, and complete the procedure in the [Manual setup](#manual-setup) section instead.</span></span>

> [!NOTE]
> <span data-ttu-id="c4bad-133">Norėdami vykdyti „Windows PowerShell" scenarijų, naudokite nurodytą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="c4bad-133">Use the following procedure to run the Windows PowerShell script.</span></span> <span data-ttu-id="c4bad-134">Nustatymas gali neveikti, jei naudojate parinktį **Išbandyti ją** „Azure" CLI ar jei scenarijus paleidžiamas kompiuteryje.</span><span class="sxs-lookup"><span data-stu-id="c4bad-134">The setup might not work if you use the **Try it** option in Azure CLI or if you run the script on your computer.</span></span>

<span data-ttu-id="c4bad-135">Atlikite šiuos veiksmus, norėdami sukonfigūruoti „Azure“ naudodami „Windows PowerShell“ scenarijų.</span><span class="sxs-lookup"><span data-stu-id="c4bad-135">Follow these steps to use the Windows PowerShell script to configure Azure.</span></span> <span data-ttu-id="c4bad-136">Turite turėti teises sukurti „Azure“ išteklių grupę, „Azure“ išteklius ir „Azure AD“ programą.</span><span class="sxs-lookup"><span data-stu-id="c4bad-136">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="c4bad-137">Norėdami gauti informacijos apie reikiamas teises, žr. [„Azure AD“ teisių patikrinimas](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="c4bad-137">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="c4bad-138">[„Azure“ portale](https://portal.azure.com) eikite į savo tikslinę „Azure“ prenumeratą.</span><span class="sxs-lookup"><span data-stu-id="c4bad-138">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span>
2. <span data-ttu-id="c4bad-139">Pasirinkite mygtuką **„Cloud Shell“**, esantį lauko **Ieška** dešinėje.</span><span class="sxs-lookup"><span data-stu-id="c4bad-139">Select **Cloud Shell** to the right of the **Search** field.</span></span>
3. <span data-ttu-id="c4bad-140">Pasirinkite **„PowerShell“**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-140">Select **PowerShell**.</span></span>
4. <span data-ttu-id="c4bad-141">Sukurkite saugyklą, jei būsite paraginti tai sukurti.</span><span class="sxs-lookup"><span data-stu-id="c4bad-141">Create storage if you're prompted to create it.</span></span>
5. <span data-ttu-id="c4bad-142">Eikite į skirtuką **„Azure“** ir pasirinkite **Kopijuoti**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-142">On the **Azure CLI** tab, select **Copy**.</span></span>
6. <span data-ttu-id="c4bad-143">Programoje „Notepad“ atidarykite naują failą ir įklijuokite į „Windows PowerShell" scenarijų.</span><span class="sxs-lookup"><span data-stu-id="c4bad-143">In Notepad, open a new file, and paste in the Windows PowerShell script.</span></span>
7. <span data-ttu-id="c4bad-144">Įrašykite failą kaip **ConfigureDataLake.ps1**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-144">Save the file as **ConfigureDataLake.ps1**.</span></span>
8. <span data-ttu-id="c4bad-145">Į seansą įkelkite „Windows PowerShell" scenarijų naudodami nusiuntimo į „Cloud Shell“ meniu parinktį.</span><span class="sxs-lookup"><span data-stu-id="c4bad-145">Upload the Windows PowerShell script to the session by using the menu option for upload in Cloud Shell.</span></span>
9. <span data-ttu-id="c4bad-146">Paleiskite **.\ConfigureDataLake.ps1** scenarijų.</span><span class="sxs-lookup"><span data-stu-id="c4bad-146">Run the **.\ConfigureDataLake.ps1** script.</span></span>
10. <span data-ttu-id="c4bad-147">Vykdykite raginimus paleisti scenarijų.</span><span class="sxs-lookup"><span data-stu-id="c4bad-147">Follow the prompts to run the script.</span></span>
11. <span data-ttu-id="c4bad-148">Naudokite scenarijaus pateikiamą informaciją, kad į LCS įdiegtumėte papildinį Eksportavimas į „Data Lake“.</span><span class="sxs-lookup"><span data-stu-id="c4bad-148">Use the information from the script output to install the Export to Data Lake add-in in LCS.</span></span>

### <a name="manual-setup"></a><span data-ttu-id="c4bad-149">Neautomatinė sąranka</span><span class="sxs-lookup"><span data-stu-id="c4bad-149">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="c4bad-150">Programų įtraukimas į „Azure AD“ nuomotoją</span><span class="sxs-lookup"><span data-stu-id="c4bad-150">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="c4bad-151">[„Azure“ portale](https://portal.azure.com) nueikite į **„Azure Active Directory“**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-151">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="c4bad-152">Pasirinkite **Tvarkyti \> Įmonės programos**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-152">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="c4bad-153">Ieškokite tolesnių programų pagal programos ID.</span><span class="sxs-lookup"><span data-stu-id="c4bad-153">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="c4bad-154">Prašymas</span><span class="sxs-lookup"><span data-stu-id="c4bad-154">Application</span></span>                              | <span data-ttu-id="c4bad-155">Programos ID</span><span class="sxs-lookup"><span data-stu-id="c4bad-155">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="c4bad-156">„Microsoft Dynamics ERP Microservices“</span><span class="sxs-lookup"><span data-stu-id="c4bad-156">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="c4bad-157">„0cdb527f-a8d1-4bf8-9436-b352c68682b2“</span><span class="sxs-lookup"><span data-stu-id="c4bad-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="c4bad-158">„Microsoft Dynamics ERP Microservices CDS“</span><span class="sxs-lookup"><span data-stu-id="c4bad-158">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="c4bad-159">„703e2651-d3fc-48f5-942c-74274233dba8“</span><span class="sxs-lookup"><span data-stu-id="c4bad-159">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="c4bad-160">„AI Builder“ autorizavimo tarnyba</span><span class="sxs-lookup"><span data-stu-id="c4bad-160">AI Builder Authorization Service</span></span>         | <span data-ttu-id="c4bad-161">„ad40333e-9910-4b61-b281-e3aeeb8c3ef3“</span><span class="sxs-lookup"><span data-stu-id="c4bad-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="c4bad-162">Jeigu negalite rasti nė vienos iš ankstesnių programų, bandykite atlikti tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c4bad-162">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="c4bad-163">Vietiniame kompiuteryje pasirinkite meniu **Pradėti** ir ieškokite **powershell**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-163">On your local computer, on the **Start** menu, search for **powershell**.</span></span>
2. <span data-ttu-id="c4bad-164">Pasirinkite ir laikykite (arba dešiniuoju pelės mygtuku spustelėkite) **„Windows PowerShell“**, tada pasirinkite **Paleisti administratoriaus teisėmis**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-164">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="c4bad-165">Vykdykite tolesnę komandą, kad įdiegtumėte **„AzureAD“** modulį.</span><span class="sxs-lookup"><span data-stu-id="c4bad-165">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="c4bad-166">Jei reikalaujama „NuGet“ teikėjo, kad galėtumėte tęsti, pasirinkite **Y**, kad jį įdiegtumėte.</span><span class="sxs-lookup"><span data-stu-id="c4bad-166">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="c4bad-167">Jei gausite pranešimą „Nepatikima saugykla“, norėdami tęsti pasirinkite **Y**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-167">If you receive an "Untrusted repository" message, select **Y** to continue.</span></span>
6. <span data-ttu-id="c4bad-168">Kiekvienai programai, kuri turi būti įtraukta, vykdykite toliau nurodytas komandas, kad įtrauktumėte programą į „Azure AD“.</span><span class="sxs-lookup"><span data-stu-id="c4bad-168">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="c4bad-169">Kai būsite paraginti, prisijunkite kaip „Azure AD“ administratorius.</span><span class="sxs-lookup"><span data-stu-id="c4bad-169">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="c4bad-170">„Azure“ išteklių kūrimas</span><span class="sxs-lookup"><span data-stu-id="c4bad-170">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="c4bad-171">Įsitikinkite, kad sukūrėte tolesnius išteklius tame pačiame „Azure AD“ egzemplioriuje, kaip „Dataverse“ aplinka.</span><span class="sxs-lookup"><span data-stu-id="c4bad-171">Make sure that you create the following resources in the same Azure AD instance that the Dataverse environment is in.</span></span> <span data-ttu-id="c4bad-172">Negalite naudoti išteklių iš kito „Azure AD“ egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="c4bad-172">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="c4bad-173">Naujos saugyklos paskyros kūrimas:</span><span class="sxs-lookup"><span data-stu-id="c4bad-173">Create a storage account:</span></span>

    1. <span data-ttu-id="c4bad-174">[„Azure“ portale](https://portal.azure.com) sukurkite saugyklos paskyrą.</span><span class="sxs-lookup"><span data-stu-id="c4bad-174">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="c4bad-175">Dialogo lange **Saugyklos paskyros kūrimas** nustatykite tolesnius laukus.</span><span class="sxs-lookup"><span data-stu-id="c4bad-175">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="c4bad-176">**Vieta** – pasirinkite duomenų centrą, kuriame yra jūsų aplinka.</span><span class="sxs-lookup"><span data-stu-id="c4bad-176">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="c4bad-177">**Našumas** – rekomenduojame pasirinkti **Standartinis**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-177">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="c4bad-178">**Paskyros rūšis** – turite pasirinkti **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-178">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="c4bad-179">Dialogo lange **Išplėstinės parinktys**, prie parinkties **„Data Lake Storage Gen2“** (funkcija **Hierarchinės vardų sritys**) pasirinkite **Įjungti**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-179">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="c4bad-180">Jei funkcijos neįjungsite, negalėsite naudoti duomenų, kuriuos „Finance and Operations“ programos rašo naudodamos tokias tarnybas, kaip „Power BI“ duomenų srautai.</span><span class="sxs-lookup"><span data-stu-id="c4bad-180">If you don't enable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="c4bad-181">Pasirinkite **Peržiūrėti ir kurti**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-181">Select **Review and create**.</span></span> <span data-ttu-id="c4bad-182">Kai diegimas bus baigtas, naujasis išteklius bus rodomas „Azure“ portale.</span><span class="sxs-lookup"><span data-stu-id="c4bad-182">When the deployment is completed, the new resource is shown in the Azure portal.</span></span>
    5. <span data-ttu-id="c4bad-183">Pereikite į sukurtą saugyklos paskyrą.</span><span class="sxs-lookup"><span data-stu-id="c4bad-183">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="c4bad-184">Kairiajame meniu pasirinkite **Prieigos raktai**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-184">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="c4bad-185">Nukopijuokite ir įrašykite saugyklos paskyros pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c4bad-185">Copy and save the name of the storage account.</span></span> <span data-ttu-id="c4bad-186">Šią reikšmę reikės pateikti vėliau, kai nustatysite raktų saugyklą.</span><span class="sxs-lookup"><span data-stu-id="c4bad-186">You will have to provide this value later, when you set up key vault secrets.</span></span>

2. <span data-ttu-id="c4bad-187">Naujos raktų saugyklos sukūrimas:</span><span class="sxs-lookup"><span data-stu-id="c4bad-187">Create a key vault:</span></span>

    1. <span data-ttu-id="c4bad-188">[„Azure“ portale](https://portal.azure.com) sukurkite raktų saugyklą.</span><span class="sxs-lookup"><span data-stu-id="c4bad-188">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="c4bad-189">Dialogo lango **Raktų saugyklos kūrimas** lauke **Vieta** pasirinkite duomenų centrą, kuriame yra jūsų aplinka.</span><span class="sxs-lookup"><span data-stu-id="c4bad-189">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="c4bad-190">Kai sukuriama "Key Vault", eikite į **„Key Vault"** apžvalgą ir kopijuokite ir įrašykite DNS pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c4bad-190">After key vault is created, go to **Key Vault Overview**, and copy and save the DNS name.</span></span> <span data-ttu-id="c4bad-191">Šią reikšmę reikės pateikti vėliau, kai nustatysite raktų saugyklą „Data Lake“ priede.</span><span class="sxs-lookup"><span data-stu-id="c4bad-191">You will have to provide this value later, when you set up the Data Lake add-in.</span></span>

3. <span data-ttu-id="c4bad-192">„Azure AD“ programos sukūrimas ir užregistravimas</span><span class="sxs-lookup"><span data-stu-id="c4bad-192">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="c4bad-193">[„Azure“ portale](https://portal.azure.com) nueikite į **„Azure Active Directory“** ir pasirinkite **Programų registracijos**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-193">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="c4bad-194">Pasirinkite **Nauja programos registracija** ir nustatykite tolesnius laukus.</span><span class="sxs-lookup"><span data-stu-id="c4bad-194">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="c4bad-195">**Pavadinimas** – įveskite programos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c4bad-195">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="c4bad-196">**Programos tipas** – pasirinkite **Žiniatinklio API**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-196">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="c4bad-197">**Peradresavimo URI sąranka** – įveskite savo „Dynamics 365“ egzemplioriaus URL, pvz., `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="c4bad-197">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="c4bad-198">Nueikite į ką tik sukurtą programą ir nukopijuokite bei įrašykite jos elemento **Programos (kliento) ID** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c4bad-198">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="c4bad-199">Šią reikšmę reikės pateikti vėliau, kai nustatysite raktų saugyklą.</span><span class="sxs-lookup"><span data-stu-id="c4bad-199">You will have to provide this value later, when you set up key vault secrets.</span></span>
    4. <span data-ttu-id="c4bad-200">Nueikite į sritį **API teisės** ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c4bad-200">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="c4bad-201">Pasirinkite **Įtraukti teisę**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-201">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="c4bad-202">Pasirinkite **„Azure“ raktų saugykla**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-202">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="c4bad-203">Pasirinkę perduotąsias teises, pasirinkite **vartotojas\_apsimetimas**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-203">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="c4bad-204">Pasirinkite **Įtraukti teises**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-204">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="c4bad-205">Programos meniu pasirinkite **Sertifikatai \& slaptieji raktai**, tada atlikite tolesnius veiksmus, kad sukurtumėte raktų saugyklos slaptųjų raktų.</span><span class="sxs-lookup"><span data-stu-id="c4bad-205">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="c4bad-206">Pasirinkite **Naujas kliento slaptasis raktas**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-206">Select **New client secret**.</span></span>
        2. <span data-ttu-id="c4bad-207">Lauke **Rakto aprašas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c4bad-207">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="c4bad-208">Pasirinkite trukmę, tada – **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-208">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="c4bad-209">Slaptasis raktas sugeneruojamas lauke **Reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-209">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="c4bad-210">Nukopijuokite ir įrašykite kliento slaptą raktą.</span><span class="sxs-lookup"><span data-stu-id="c4bad-210">Copy and save the client secret value.</span></span> <span data-ttu-id="c4bad-211">Šią reikšmę reikės pateikti vėliau, kai nustatysite raktų saugyklą.</span><span class="sxs-lookup"><span data-stu-id="c4bad-211">You will have to provide this value later, when you set up key vault secrets.</span></span>

4. <span data-ttu-id="c4bad-212">Raktų saugyklos slaptųjų raktų kūrimas</span><span class="sxs-lookup"><span data-stu-id="c4bad-212">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="c4bad-213">Pereikite į anksčiau sukurtą raktų saugyklą ir pasirinkite **Slaptieji raktai**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-213">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="c4bad-214">Su kiekvienu toliau pateiktoje lentelėje esančiu slaptojo rakto pavadinimu atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c4bad-214">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="c4bad-215">Pasirinkite **Generuoti / importuoti**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-215">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="c4bad-216">Dialogo lango **Slaptojo rakto kūrimas** lauke **Nusiuntimo parinktys** pasirinkite **Neautomatinis**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-216">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="c4bad-217">Sukurkite slaptojo rakto pavadinimą ir reikšmę iš tolesnės lentelės.</span><span class="sxs-lookup"><span data-stu-id="c4bad-217">Create the secret name and value from the table.</span></span>
        4. <span data-ttu-id="c4bad-218">Pasirinkite **Įjungta**, tada – **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-218">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="c4bad-219">Slaptasis raktas sukuriamas ir įtraukiamas į raktų saugyklą.</span><span class="sxs-lookup"><span data-stu-id="c4bad-219">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="c4bad-220">Slaptas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="c4bad-220">Secret name</span></span>                       | <span data-ttu-id="c4bad-221">Slaptojo rakto reikšmė</span><span class="sxs-lookup"><span data-stu-id="c4bad-221">Secret value</span></span>                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | <span data-ttu-id="c4bad-222">app-id</span><span class="sxs-lookup"><span data-stu-id="c4bad-222">app-id</span></span>                            | <span data-ttu-id="c4bad-223">Programos, kurią sukūrėte anksčiau, ID.</span><span class="sxs-lookup"><span data-stu-id="c4bad-223">The app ID of the application that you created earlier.</span></span>                                      |
        | <span data-ttu-id="c4bad-224">app-secret</span><span class="sxs-lookup"><span data-stu-id="c4bad-224">app-secret</span></span>                        | <span data-ttu-id="c4bad-225">Kliento slaptasis raktas, kurį įrašėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="c4bad-225">The client secret that you saved earlier.</span></span>                                                    |
        | <span data-ttu-id="c4bad-226">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="c4bad-226">storage-account-name</span></span>              | <span data-ttu-id="c4bad-227">Saugyklos paskyros, kurią sukūrėte anksčiau, pavadinimas, pvz., **1saugyklospaskyra**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-227">The name of the storage account that you created earlier, such as **storageaccount1**.</span></span>       |

5. <span data-ttu-id="c4bad-228">Programos autorizavimas norint pasiekti raktų saugyklą</span><span class="sxs-lookup"><span data-stu-id="c4bad-228">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="c4bad-229">[„Azure“ portale](https://portal.azure.com) atidarykite raktų saugyklą, kurią sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="c4bad-229">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="c4bad-230">Pasirinkite prieigos strategijas.</span><span class="sxs-lookup"><span data-stu-id="c4bad-230">Select the access policies.</span></span>
    3. <span data-ttu-id="c4bad-231">Su kiekviena toliau pateiktoje lentelėje esančia programa atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c4bad-231">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="c4bad-232">Pasirinkite **Įtraukti prieigos strategiją**, kad sukurtumėte prieigos strategiją.</span><span class="sxs-lookup"><span data-stu-id="c4bad-232">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="c4bad-233">Lauke **Slaptųjų raktų teisės** pasirinkite teises iš tolesnės lentelės.</span><span class="sxs-lookup"><span data-stu-id="c4bad-233">In the **Secret permissions** field, select the permissions from the table.</span></span>
        3. <span data-ttu-id="c4bad-234">Lauke **Pasirinkti pagrindinį pavadinimą** ieškokite rodomo programos pavadinimo iš tolesnės lentelės.</span><span class="sxs-lookup"><span data-stu-id="c4bad-234">In the **Select principal** field, search for the application display name from the table.</span></span>
        4. <span data-ttu-id="c4bad-235">Pasirinkite **Pasirinkti**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-235">Select **Select**.</span></span>
        5. <span data-ttu-id="c4bad-236">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-236">Select **Add**.</span></span>
        6. <span data-ttu-id="c4bad-237">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-237">Select **Save**.</span></span>

        | <span data-ttu-id="c4bad-238">Prašymas</span><span class="sxs-lookup"><span data-stu-id="c4bad-238">Application</span></span>                                              | <span data-ttu-id="c4bad-239">Teisės</span><span class="sxs-lookup"><span data-stu-id="c4bad-239">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="c4bad-240">Naujos programos, kurią sukūrėte, rodomas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="c4bad-240">The display name of the new application that you created</span></span> | <span data-ttu-id="c4bad-241">Get, List</span><span class="sxs-lookup"><span data-stu-id="c4bad-241">Get, List</span></span>   |
        | <span data-ttu-id="c4bad-242">**„Microsoft Dynamics ERP Microservices“**</span><span class="sxs-lookup"><span data-stu-id="c4bad-242">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="c4bad-243">Get, List</span><span class="sxs-lookup"><span data-stu-id="c4bad-243">Get, List</span></span>   |

6. <span data-ttu-id="c4bad-244">Vaidmenų priskyrimas, kad būtų galima pasiekti saugyklos paskyrą</span><span class="sxs-lookup"><span data-stu-id="c4bad-244">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="c4bad-245">[„Azure“ portale](https://portal.azure.com) atidarykite saugyklos paskyrą, kurią sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="c4bad-245">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="c4bad-246">Pasirinkite **Prieigos valdymas (IAM)**, tada – **Vaidmenų priskyrimai**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-246">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="c4bad-247">Pasirinkite **Įtraukti, įtraukti vaidmens priskyrimą**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-247">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="c4bad-248">Su kiekviena toliau pateiktoje lentelėje esančia programa atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c4bad-248">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="c4bad-249">Iš tolesnės lentelės pasirinkite vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="c4bad-249">Select the role from the table.</span></span>
        2. <span data-ttu-id="c4bad-250">Lauką **Kam priskirti prieigą** palikite nustatytą kaip **„Azure AD“ vartotojas, grupė arba pagrindinis tarnybos pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-250">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="c4bad-251">Lauke **Pasirinkti** įveskite programą iš tolesnės lentelės.</span><span class="sxs-lookup"><span data-stu-id="c4bad-251">In the **Select** field, enter the application from the table.</span></span>
        4. <span data-ttu-id="c4bad-252">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-252">Select **Save**.</span></span>

        | <span data-ttu-id="c4bad-253">Prašymas</span><span class="sxs-lookup"><span data-stu-id="c4bad-253">Application</span></span>                                              | <span data-ttu-id="c4bad-254">Vaidmuo</span><span class="sxs-lookup"><span data-stu-id="c4bad-254">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="c4bad-255">Naujos programos, kurią sukūrėte, rodomas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="c4bad-255">The display name of the new application that you created</span></span> | <span data-ttu-id="c4bad-256">Savininkas</span><span class="sxs-lookup"><span data-stu-id="c4bad-256">Owner</span></span>                       |
        | <span data-ttu-id="c4bad-257">Naujos programos, kurią sukūrėte, rodomas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="c4bad-257">The display name of the new application that you created</span></span> | <span data-ttu-id="c4bad-258">Bendraautorius</span><span class="sxs-lookup"><span data-stu-id="c4bad-258">Contributor</span></span>                 |
        | <span data-ttu-id="c4bad-259">Naujos programos, kurią sukūrėte, rodomas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="c4bad-259">The display name of the new application that you created</span></span> | <span data-ttu-id="c4bad-260">Saugyklos paskyros bendraautoris</span><span class="sxs-lookup"><span data-stu-id="c4bad-260">Storage Account Contributor</span></span> |
        | <span data-ttu-id="c4bad-261">Naujos programos, kurią sukūrėte, rodomas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="c4bad-261">The display name of the new application that you created</span></span> | <span data-ttu-id="c4bad-262">Saugyklos didelių dvejetainių objektų duomenų savininkas</span><span class="sxs-lookup"><span data-stu-id="c4bad-262">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="c4bad-263">**„AI Builder“ autorizavimo tarnyba**</span><span class="sxs-lookup"><span data-stu-id="c4bad-263">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="c4bad-264">Saugyklos didelių dvejetainių objektų duomenų skaitytojas</span><span class="sxs-lookup"><span data-stu-id="c4bad-264">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="c4bad-265">„Azure“ CLI</span><span class="sxs-lookup"><span data-stu-id="c4bad-265">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}
```
---

## <a name="configure-the-export-to-data-lake-add-in"></a><span data-ttu-id="c4bad-266">Eksportavimo į „Azure Data Lake“ priedą konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="c4bad-266">Configure the Export to Data Lake add-in</span></span>

<span data-ttu-id="c4bad-267">Atlikite šiuos veiksmus, kad, naudodami LCS, įtrauktumėte eksportavimo „Azure Data Lake“ papildinį į aplinką.</span><span class="sxs-lookup"><span data-stu-id="c4bad-267">Follow these steps to use LCS to add the Export to Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="c4bad-268">Prisijunkite prie LCS, tada dešinėje puslapio pusėje, prie aplinkos pavadinimo pasirinkite **Išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-268">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="c4bad-269">Skyriuje **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-269">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="c4bad-270">Pasirinkite papildinį **Eksportavimas į „Data Lake“**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-270">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="c4bad-271">Įveskite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="c4bad-271">Enter the following values.</span></span>

    | <span data-ttu-id="c4bad-272">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="c4bad-272">Value</span></span>                                                              | <span data-ttu-id="c4bad-273">aprašymas</span><span class="sxs-lookup"><span data-stu-id="c4bad-273">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="c4bad-274">„Azure“ prenumeratos nuomotojo ID, nurodantį raktų saugyklos vietą</span><span class="sxs-lookup"><span data-stu-id="c4bad-274">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="c4bad-275">Nuomotojo ID, nurodantį saugyklos paskyros, programų ir raktų saugyklų vietą.</span><span class="sxs-lookup"><span data-stu-id="c4bad-275">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="c4bad-276">Norėdami gauti šią reikšmę, atidarykite [„Azure“ portalą](https://portal.azure.com), nueikite į **„Azure Active Directory“** ir nukopijuokite elemento **Nuomotojo ID** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c4bad-276">To obtain this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="c4bad-277">Pateikite savo „Key Vault“ DNS pavadinimą</span><span class="sxs-lookup"><span data-stu-id="c4bad-277">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="c4bad-278">Raktų saugyklos DNS pavadinimas, pvz., `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="c4bad-278">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> |
    | <span data-ttu-id="c4bad-279">Pateikite slaptąjį raktą, kurį sudaro saugyklos paskyros pavadinimas</span><span class="sxs-lookup"><span data-stu-id="c4bad-279">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="c4bad-280">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="c4bad-280">**storage-account-name**</span></span> |
    | <span data-ttu-id="c4bad-281">Programos ID, kuris bus naudojamas „Data Lake“ pasiekti, slaptas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="c4bad-281">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="c4bad-282">**app-id**</span><span class="sxs-lookup"><span data-stu-id="c4bad-282">**app-id**</span></span> |
    | <span data-ttu-id="c4bad-283">Programos kliento slapto vardo slapto vardas</span><span class="sxs-lookup"><span data-stu-id="c4bad-283">Secret name for App client secret</span></span>                                  | <span data-ttu-id="c4bad-284">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="c4bad-284">**app-secret**</span></span> |

5. <span data-ttu-id="c4bad-285">Sutikite su sąlygomis ir tada pasirinkite **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-285">Agree to the terms, and then select **Install**.</span></span>

<span data-ttu-id="c4bad-286">Papildinys bus įdiegtas per kelias minutes.</span><span class="sxs-lookup"><span data-stu-id="c4bad-286">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-the-finance-insights-add-in"></a><span data-ttu-id="c4bad-287">„Finance insights“ konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="c4bad-287">Configure the Finance insights add-in</span></span>

> [!NOTE]
> <span data-ttu-id="c4bad-288">Jei anksčiau įdiegėte priedą Gauti žinių, pašalinkite jį prieš pradėdami nurodytą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="c4bad-288">If you previously installed the Get insights add-in, uninstall it before you complete the following procedure.</span></span>

<span data-ttu-id="c4bad-289">Norėdami įdiegti „Finance insights“ priedą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c4bad-289">Follow these steps to install the Finance insights add-in.</span></span>

1. <span data-ttu-id="c4bad-290">Prisijunkite prie LCS, tada dešinėje puslapio pusėje, prie aplinkos pavadinimo pasirinkite **Išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-290">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="c4bad-291">Skyriuje **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-291">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="c4bad-292">RInkitės **„Finance insights“** priedą.</span><span class="sxs-lookup"><span data-stu-id="c4bad-292">Select the **Finance insights** add-in.</span></span>
4. <span data-ttu-id="c4bad-293">Sutikite su sąlygomis ir tada pasirinkite **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="c4bad-293">Agree to the terms, and then select **Install**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="c4bad-294">Atsiliepimai ir palaikymas</span><span class="sxs-lookup"><span data-stu-id="c4bad-294">Feedback and support</span></span>

<span data-ttu-id="c4bad-295">Jei domitės atsiliepimo pateikimu arba jei norite pagalbos, nusiųskite laišką [„Finance insights“ (peržiūros versija)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="c4bad-295">If you're interested in providing feedback, or if you require support, send an email to [Finance insights (Preview)](mailto:fiap@microsoft.com).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
