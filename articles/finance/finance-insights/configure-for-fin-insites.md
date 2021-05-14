---
title: Modulio „Finance Insights” konfigūracija (peržiūros versija)
description: Šioje temoje paaiškinami konfigūravimo veiksmai, kuriuos jums atlikus sistema galės naudotis modulio „Finance Insights” galimybėmis.
author: ShivamPandey-msft
ms.date: 11/25/2020
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
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 60e4d69157d7b73bd9e47310adae320687230080
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941231"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="80e76-103">Modulio „Finance Insights” konfigūracija (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="80e76-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="80e76-104">Modulyje „Finance Insights” sujungiamos „Microsoft Dynamics 365 Finance“ ir „Microsoft Dataverse“, „Azure“ bei „AI Builder“ funkcijos, kad jūsų organizacijai būtų suteikiami galingi prognozavimo įrankiai.</span><span class="sxs-lookup"><span data-stu-id="80e76-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="80e76-105">Šioje temoje paaiškinami konfigūravimo veiksmai, kuriuos jums atlikus sistema galės naudotis modulio „Finance Insights” galimybėmis.</span><span class="sxs-lookup"><span data-stu-id="80e76-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="80e76-106">„Dynamics 365 Finance“ diegimas</span><span class="sxs-lookup"><span data-stu-id="80e76-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="80e76-107">Aplinkas galite įdiegti atlikdami toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="80e76-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="80e76-108">Portale „Microsoft Dynamics Lifecycle Services“ (LCS) sukurkite arba atnaujinkite „Dynamics 365 Finance“ aplinką.</span><span class="sxs-lookup"><span data-stu-id="80e76-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="80e76-109">Aplinkai reikalinga programos 10.0.11 versija / 35 arba naujesnis platformos atnaujinimas.</span><span class="sxs-lookup"><span data-stu-id="80e76-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="80e76-110">Aplinka turi būti didelio pasiekiamumo (HA) smėlio dėžės aplinka.</span><span class="sxs-lookup"><span data-stu-id="80e76-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="80e76-111">(Šis aplinkos tipas dar vadinamas 2 pakopos aplinka.) Norėdami gauti daugiau informacijos, žr. [Aplinkos planavimas](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="80e76-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="80e76-112">Jeigu naudojate „Contoso” demonstracinius duomenis, jums reikės papildomų duomenų pavyzdžių, kad galėtumėte naudoti kliento mokėjimo prognozių, grynųjų pinigų srautų prognozių ir biudžeto prognozių funkcijas.</span><span class="sxs-lookup"><span data-stu-id="80e76-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="80e76-113">Konfigūruoti „Dataverse“</span><span class="sxs-lookup"><span data-stu-id="80e76-113">Configure Dataverse</span></span>

<span data-ttu-id="80e76-114">Norėdami sukonfigūruoti „Finance insights“, „Dataverse“ atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="80e76-114">Use the following steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="80e76-115">Atidarykite aplinkos puslapį LCS ir patikrinkite, ar **„Power Platform“** integravimo skyrius jau sąranka.</span><span class="sxs-lookup"><span data-stu-id="80e76-115">Open the environment page in LCS and verify that the **Power Platform Integration** section is already setup.</span></span>
    1. <span data-ttu-id="80e76-116">Jei jis jau nustatytas, turi „Dataverse“ būti pateiktas su aplinka susietas aplinkos „Dynamics 365 Finance“ pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="80e76-116">If it is already set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="80e76-117">Nukopijuokite „Dataverse“ aplinkos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="80e76-117">Copy the Dataverse environment name.</span></span>
    2. <span data-ttu-id="80e76-118">Jei ji nėra nustatyta, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="80e76-118">If it is not set up, follow these steps:</span></span>
        1. <span data-ttu-id="80e76-119">Integravimo **skyriuje** pasirinkite „Power Platform“ nustatymo mygtuką.</span><span class="sxs-lookup"><span data-stu-id="80e76-119">Select the **Setup** button in the Power Platform Integration section.</span></span> <span data-ttu-id="80e76-120">Tam, kad būtų galima nustatyti aplinką, gali užtrukti iki valandos.</span><span class="sxs-lookup"><span data-stu-id="80e76-120">It may take up to an hour for the environment to be set up.</span></span>
        2. <span data-ttu-id="80e76-121">„Dataverse“ aplinka sėkmingai nustatyta „Dataverse“ aplinkos pavadinimas susietas su „Dynamics 365 Finance“ aplinka turi būti įvardytas.</span><span class="sxs-lookup"><span data-stu-id="80e76-121">If the Dataverse environment is successfully set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="80e76-122">Nukopijuokite „Dataverse“ aplinkos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="80e76-122">Copy the Dataverse environment name.</span></span>
> [!NOTE]
> <span data-ttu-id="80e76-123">Nustatę aplinką, **nepasirinkite** mygtuko **Programų CDS** saito.</span><span class="sxs-lookup"><span data-stu-id="80e76-123">After completing the environment set up, **DO NOT** select the **Link to CDS for Apps** button.</span></span> <span data-ttu-id="80e76-124">Tai nėra būtina „Finance insights“ ir bus išjungta galimybė užbaigti reikiamus LCS aplinkos papildiniai.</span><span class="sxs-lookup"><span data-stu-id="80e76-124">This is not needed for Finance Insights and will disable the ability to complete the required Environment Add-ins in LCS.</span></span>

2. <span data-ttu-id="80e76-125">Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com/) ir atlikite tolesnius veiksmus, kad sukurtumėte naują „Dataverse“ aplinką tame pačiame „Active Directory“ nuomotojuje.</span><span class="sxs-lookup"><span data-stu-id="80e76-125">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="80e76-126">Atidarykite puslapį **Aplinkos**.</span><span class="sxs-lookup"><span data-stu-id="80e76-126">Open the **Environments** page.</span></span>

        <span data-ttu-id="80e76-127">[![Puslapis Aplinkos](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="80e76-127">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="80e76-128">Pasirinkite „Dataverse“ prieš tai sukurtą aplinką ir tada rinkitės **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="80e76-128">Select the Dataverse environment created above and then select **Settings**.</span></span>
    3. <span data-ttu-id="80e76-129">Pasirinkite **Ištekliai \> Visi senstelėję parametrai**.</span><span class="sxs-lookup"><span data-stu-id="80e76-129">Select **Resources \> All Legacy Settings**.</span></span>
    4. <span data-ttu-id="80e76-130">Viršutinėje naršymo juostoje pasirinkite **Parametrai**, tada – **Tinkinimai**.</span><span class="sxs-lookup"><span data-stu-id="80e76-130">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    5. <span data-ttu-id="80e76-131">Pasirinkite **Kūrėjo ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="80e76-131">Select **Developer Resources**.</span></span>
    6. <span data-ttu-id="80e76-132">Nukopijuokite **„Dataverse” organizacijos ID** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="80e76-132">Copy the **Dataverse organization ID** value.</span></span>
    7. <span data-ttu-id="80e76-133">Naršyklės adreso juostoje pasižymėkite „Dataverse“ organizacijos URL.</span><span class="sxs-lookup"><span data-stu-id="80e76-133">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="80e76-134">Pavyzdžiui, URL gali būti `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="80e76-134">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

3. <span data-ttu-id="80e76-135">Jei planuojate naudoti grynųjų pinigų srauto prognozių arba biudžeto prognozių funkciją, atlikite tolesnius veiksmus, kad atnaujintumėte savo organizacijos komentavimo limitą bent iki 50 megabaitų (MB).</span><span class="sxs-lookup"><span data-stu-id="80e76-135">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="80e76-136">Atidarykite [„Power Apps“ portalą](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="80e76-136">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="80e76-137">Pasirinkite aplinką, kurią ką tik sukūrėte, tada pasirinkite **Išplėstiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="80e76-137">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="80e76-138">Pasirinkite **Parametrai \> El. pašto konfigūravimas**.</span><span class="sxs-lookup"><span data-stu-id="80e76-138">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="80e76-139">Pakeiskite lauko **Didžiausias failo dydis** reikšmę į **51 200**.</span><span class="sxs-lookup"><span data-stu-id="80e76-139">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="80e76-140">(Reikšmė išreikšta kilobaitais \[KB\].)</span><span class="sxs-lookup"><span data-stu-id="80e76-140">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="80e76-141">Pasirinkite **Gerai**, kad įrašytumėte keitimus.</span><span class="sxs-lookup"><span data-stu-id="80e76-141">Select **OK** to save your changes.</span></span>

## <a name="configure-the-azure-setup"></a><span data-ttu-id="80e76-142">„Azure“ sąrankos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="80e76-142">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="80e76-143">„Dataverse“ katalogo ID ir vartotojo „Azure AD“ objekto ID įvedimas</span><span class="sxs-lookup"><span data-stu-id="80e76-143">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="80e76-144">Įveskite „Dataverse“ katalogo ID.</span><span class="sxs-lookup"><span data-stu-id="80e76-144">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="80e76-145">Atidarykite [„Azure“ portalą](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="80e76-145">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="80e76-146">Prisijunkite naudodami vartotojo ID, kuris buvo naudojamas kuriant „Dataverse“ aplinką.</span><span class="sxs-lookup"><span data-stu-id="80e76-146">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="80e76-147">Eikite į **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="80e76-147">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="80e76-148">Nukopijuokite elemento **Nuomotojo ID** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="80e76-148">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="80e76-149">Įveskite vartotojo „Azure Active Directory“ („Azure AD“) objekto ID.</span><span class="sxs-lookup"><span data-stu-id="80e76-149">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="80e76-150">[„Azure“ portale](https://portal.azure.com) eikite į **Vartotojai** ir ieškokite vartotojo pagal el. pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="80e76-150">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="80e76-151">Pasirinkite vartotojo vardą.</span><span class="sxs-lookup"><span data-stu-id="80e76-151">Select the user's name.</span></span>
    3. <span data-ttu-id="80e76-152">Nukopijuokite elemento **Objekto ID** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="80e76-152">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="80e76-153">„Azure Cloud Shell“ naudojimas modulio „Finance Insights” „Data Lake“ ištekliams nustatyti</span><span class="sxs-lookup"><span data-stu-id="80e76-153">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="80e76-154">„Windows PowerShell“ scenarijaus naudojimas</span><span class="sxs-lookup"><span data-stu-id="80e76-154">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="80e76-155">Pateiktas „Windows PowerShell“ scenarijus, kad būtų galima lengvai nustatyti „Azure“ išteklius, aprašytus temoje [Eksportavimo į „Azure Data Lake“ konfigūravimas](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="80e76-155">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="80e76-156">Jei norite nustatyti neautomatiniu būdu, praleiskite šią procedūrą ir vykdykite procedūrą, aprašytą skyriuje [Neautomatinė sąranka](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="80e76-156">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="80e76-157">Atlikite tolesnius veiksmus, kad būtų vykdomas „PowerShell“ scenarijus.</span><span class="sxs-lookup"><span data-stu-id="80e76-157">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="80e76-158">„Azure“ CLI parinktis „Išbandykite“ arba scenarijaus vykdymas jūsų kompiuteryje gali neveikti.</span><span class="sxs-lookup"><span data-stu-id="80e76-158">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="80e76-159">Atlikite šiuos veiksmus, kad sukonfigūruotumėte „Azure“ naudodami „Windows PowerShell“ scenarijų.</span><span class="sxs-lookup"><span data-stu-id="80e76-159">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="80e76-160">Turite turėti teises sukurti „Azure“ išteklių grupę, „Azure“ išteklius ir „Azure AD“ programą.</span><span class="sxs-lookup"><span data-stu-id="80e76-160">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="80e76-161">Norėdami gauti informacijos apie reikiamas teises, žr. [„Azure AD“ teisių patikrinimas](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="80e76-161">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="80e76-162">[„Azure“ portale](https://portal.azure.com) eikite į savo tikslinę „Azure“ prenumeratą.</span><span class="sxs-lookup"><span data-stu-id="80e76-162">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="80e76-163">Pasirinkite mygtuką **„Cloud Shell“**, esantį lauko **Ieška** dešinėje.</span><span class="sxs-lookup"><span data-stu-id="80e76-163">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="80e76-164">Pasirinkite **„PowerShell“**.</span><span class="sxs-lookup"><span data-stu-id="80e76-164">Select **PowerShell**.</span></span>
3. <span data-ttu-id="80e76-165">Sukurkite saugyklą, jei būsite paraginti tai padaryti.</span><span class="sxs-lookup"><span data-stu-id="80e76-165">Create storage if you're prompted to do so.</span></span>
4. <span data-ttu-id="80e76-166">Eikite į skirtuką **„Azure“** ir pasirinkite **Kopijuoti**.</span><span class="sxs-lookup"><span data-stu-id="80e76-166">Go to the **Azure CLI** tab and select **Copy**.</span></span>  
5. <span data-ttu-id="80e76-167">Atidarykite „Notepad“ ir įklijuokite „PowerShell" scenarijų.</span><span class="sxs-lookup"><span data-stu-id="80e76-167">Open Notepad and paste the PowerShell script.</span></span> <span data-ttu-id="80e76-168">Įrašykite failą kaip ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="80e76-168">Save the file as ConfigureDataLake.ps1.</span></span>
6. <span data-ttu-id="80e76-169">Į seansą įkelkite „Windows PowerShell" scenarijų naudodami nusiuntimo į „Cloud Shell“ meniu parinktį.</span><span class="sxs-lookup"><span data-stu-id="80e76-169">Upload the Windows PowerShell script to the session using the menu option for upload in Cloud Shell.</span></span>
7. <span data-ttu-id="80e76-170">Paleiskite scenarijų .\ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="80e76-170">Run the script .\ConfigureDataLake.ps1.</span></span>
8. <span data-ttu-id="80e76-171">Vykdykite raginimus paleisti scenarijų.</span><span class="sxs-lookup"><span data-stu-id="80e76-171">Follow the prompts to run the script.</span></span>
9. <span data-ttu-id="80e76-172">Naudokite scenarijaus pateikiamą informaciją, kad į LCS įdiegtumėte papildinį **Eksportavimas į „Data Lake“**.</span><span class="sxs-lookup"><span data-stu-id="80e76-172">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
10. <span data-ttu-id="80e76-173">Naudokite scenarijaus pateikiamą informaciją, kad „Finance“ puslapyje **Duomenų ryšiai** įjungtumėte objektų saugyklą (**Sistemos administravimas \> Sistemos parametrai \> Duomenų ryšiai**).</span><span class="sxs-lookup"><span data-stu-id="80e76-173">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="80e76-174">Neautomatinė sąranka</span><span class="sxs-lookup"><span data-stu-id="80e76-174">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="80e76-175">Programų įtraukimas į „Azure AD“ nuomotoją</span><span class="sxs-lookup"><span data-stu-id="80e76-175">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="80e76-176">[„Azure“ portale](https://portal.azure.com) nueikite į **„Azure Active Directory“**.</span><span class="sxs-lookup"><span data-stu-id="80e76-176">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="80e76-177">Pasirinkite **Tvarkyti \> Įmonės programos**.</span><span class="sxs-lookup"><span data-stu-id="80e76-177">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="80e76-178">Ieškokite tolesnių programų pagal programos ID.</span><span class="sxs-lookup"><span data-stu-id="80e76-178">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="80e76-179">Prašymas</span><span class="sxs-lookup"><span data-stu-id="80e76-179">Application</span></span>                              | <span data-ttu-id="80e76-180">Programos ID</span><span class="sxs-lookup"><span data-stu-id="80e76-180">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="80e76-181">„Microsoft Dynamics ERP Microservices“</span><span class="sxs-lookup"><span data-stu-id="80e76-181">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="80e76-182">„0cdb527f-a8d1-4bf8-9436-b352c68682b2“</span><span class="sxs-lookup"><span data-stu-id="80e76-182">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="80e76-183">„Microsoft Dynamics ERP Microservices CDS“</span><span class="sxs-lookup"><span data-stu-id="80e76-183">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="80e76-184">„703e2651-d3fc-48f5-942c-74274233dba8“</span><span class="sxs-lookup"><span data-stu-id="80e76-184">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="80e76-185">„AI Builder“ autorizavimo tarnyba</span><span class="sxs-lookup"><span data-stu-id="80e76-185">AI Builder Authorization Service</span></span>         | <span data-ttu-id="80e76-186">„ad40333e-9910-4b61-b281-e3aeeb8c3ef3“</span><span class="sxs-lookup"><span data-stu-id="80e76-186">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="80e76-187">Jeigu negalite rasti nė vienos iš ankstesnių programų, bandykite atlikti tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="80e76-187">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="80e76-188">Vietiniame kompiuteryje pasirinkite meniu **Pradėti** ir ieškokite **powershell**.</span><span class="sxs-lookup"><span data-stu-id="80e76-188">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="80e76-189">Pasirinkite ir laikykite (arba dešiniuoju pelės mygtuku spustelėkite) **„Windows PowerShell“**, tada pasirinkite **Paleisti administratoriaus teisėmis**.</span><span class="sxs-lookup"><span data-stu-id="80e76-189">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="80e76-190">Vykdykite tolesnę komandą, kad įdiegtumėte **„AzureAD“** modulį.</span><span class="sxs-lookup"><span data-stu-id="80e76-190">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="80e76-191">Jei reikalaujama „NuGet“ teikėjo, kad galėtumėte tęsti, pasirinkite **Y**, kad jį įdiegtumėte.</span><span class="sxs-lookup"><span data-stu-id="80e76-191">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="80e76-192">Jei pasirodo pranešimas „Nepatikima saugykla“, norėdami tęsti pasirinkite **Y**.</span><span class="sxs-lookup"><span data-stu-id="80e76-192">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="80e76-193">Kiekvienai programai, kuri turi būti įtraukta, vykdykite toliau nurodytas komandas, kad įtrauktumėte programą į „Azure AD“.</span><span class="sxs-lookup"><span data-stu-id="80e76-193">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="80e76-194">Kai būsite paraginti, prisijunkite kaip „Azure AD“ administratorius.</span><span class="sxs-lookup"><span data-stu-id="80e76-194">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="80e76-195">„Azure“ išteklių kūrimas</span><span class="sxs-lookup"><span data-stu-id="80e76-195">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="80e76-196">Įsitikinkite, kad sukūrėte tolesnius išteklius tame pačiame „Azure AD“ egzemplioriuje, kaip „Dataverse“ aplinka.</span><span class="sxs-lookup"><span data-stu-id="80e76-196">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="80e76-197">Negalite naudoti išteklių iš kito „Azure AD“ egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="80e76-197">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="80e76-198">Naujos saugyklos paskyros kūrimas</span><span class="sxs-lookup"><span data-stu-id="80e76-198">Create a new storage account:</span></span>

    1. <span data-ttu-id="80e76-199">[„Azure“ portale](https://portal.azure.com) sukurkite saugyklos paskyrą.</span><span class="sxs-lookup"><span data-stu-id="80e76-199">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="80e76-200">Dialogo lange **Saugyklos paskyros kūrimas** nustatykite tolesnius laukus.</span><span class="sxs-lookup"><span data-stu-id="80e76-200">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="80e76-201">**Vieta** – pasirinkite duomenų centrą, kuriame yra jūsų aplinka.</span><span class="sxs-lookup"><span data-stu-id="80e76-201">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="80e76-202">**Našumas** – rekomenduojame pasirinkti **Standartinis**.</span><span class="sxs-lookup"><span data-stu-id="80e76-202">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="80e76-203">**Paskyros rūšis** – turite pasirinkti **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="80e76-203">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="80e76-204">Dialogo lange **Išplėstinės parinktys**, prie parinkties **„Data Lake Storage Gen2“** (funkcija **Hierarchinės vardų sritys**) pasirinkite **Įjungti**.</span><span class="sxs-lookup"><span data-stu-id="80e76-204">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="80e76-205">Jei šią funkciją išjungsite, negalėsite naudoti duomenų, kuriuos „Finance and Operations“ programos rašo naudodamos tokias tarnybas, kaip „Power BI“ duomenų srautai.</span><span class="sxs-lookup"><span data-stu-id="80e76-205">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="80e76-206">Pasirinkite **Peržiūrėti ir kurti**.</span><span class="sxs-lookup"><span data-stu-id="80e76-206">Select **Review and create**.</span></span> <span data-ttu-id="80e76-207">Kai diegimas bus baigtas, naujasis išteklius bus rodomas „Azure“ portale.</span><span class="sxs-lookup"><span data-stu-id="80e76-207">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="80e76-208">Pereikite į sukurtą saugyklos paskyrą.</span><span class="sxs-lookup"><span data-stu-id="80e76-208">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="80e76-209">Kairiajame meniu pasirinkite **Prieigos raktai**.</span><span class="sxs-lookup"><span data-stu-id="80e76-209">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="80e76-210">Nukopijuokite ir įrašykite **Key1** arba **Key2** jungimosi eilutę.</span><span class="sxs-lookup"><span data-stu-id="80e76-210">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="80e76-211">Nukopijuokite ir įrašykite saugyklos paskyros pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="80e76-211">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="80e76-212">Naujos raktų saugyklos sukūrimas</span><span class="sxs-lookup"><span data-stu-id="80e76-212">Create a new key vault:</span></span>

    1. <span data-ttu-id="80e76-213">[„Azure“ portale](https://portal.azure.com) sukurkite raktų saugyklą.</span><span class="sxs-lookup"><span data-stu-id="80e76-213">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="80e76-214">Dialogo lango **Raktų saugyklos kūrimas** lauke **Vieta** pasirinkite duomenų centrą, kuriame yra jūsų aplinka.</span><span class="sxs-lookup"><span data-stu-id="80e76-214">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="80e76-215">Sukūrę raktų saugyklą, pasirinkite ją sąraše, tada pasirinkite **Slaptieji raktai**.</span><span class="sxs-lookup"><span data-stu-id="80e76-215">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="80e76-216">Pasirinkite **Generuoti / importuoti**.</span><span class="sxs-lookup"><span data-stu-id="80e76-216">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="80e76-217">Dialogo lango **Slaptojo rakto kūrimas** lauke **Nusiuntimo parinktys** pasirinkite **Neautomatinis**.</span><span class="sxs-lookup"><span data-stu-id="80e76-217">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="80e76-218">Įveskite slaptojo rakto pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="80e76-218">Enter a name for the secret.</span></span> <span data-ttu-id="80e76-219">Pasižymėkite pavadinimą, nes jį reikės pateikti vėliau.</span><span class="sxs-lookup"><span data-stu-id="80e76-219">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="80e76-220">Lauke **Reikšmė** įveskite jungimosi eilutę, kurią gavote iš saugyklos paskyros atlikdami ankstesnę procedūrą.</span><span class="sxs-lookup"><span data-stu-id="80e76-220">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="80e76-221">Pasirinkite **Įjungta**, tada – **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="80e76-221">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="80e76-222">Slaptasis raktas sukuriamas ir įtraukiamas į raktų saugyklą.</span><span class="sxs-lookup"><span data-stu-id="80e76-222">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="80e76-223">Nueikite į sritį **Raktų saugyklos apžvalga** ir pasižymėkite DNS pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="80e76-223">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="80e76-224">„Azure AD“ programos sukūrimas ir užregistravimas</span><span class="sxs-lookup"><span data-stu-id="80e76-224">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="80e76-225">[„Azure“ portale](https://portal.azure.com) nueikite į **„Azure Active Directory“** ir pasirinkite **Programų registracijos**.</span><span class="sxs-lookup"><span data-stu-id="80e76-225">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="80e76-226">Pasirinkite **Nauja programos registracija** ir nustatykite tolesnius laukus.</span><span class="sxs-lookup"><span data-stu-id="80e76-226">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="80e76-227">**Pavadinimas** – įveskite programos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="80e76-227">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="80e76-228">**Programos tipas** – pasirinkite **Žiniatinklio API**.</span><span class="sxs-lookup"><span data-stu-id="80e76-228">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="80e76-229">**Peradresavimo URI sąranka** – įveskite savo „Dynamics 365“ egzemplioriaus URL, pvz., `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="80e76-229">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="80e76-230">Nueikite į ką tik sukurtą programą ir nukopijuokite bei įrašykite jos elemento **Programos (kliento) ID** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="80e76-230">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="80e76-231">Šią reikšmę reikės pateikti vėliau, kai nustatysite raktų saugyklą.</span><span class="sxs-lookup"><span data-stu-id="80e76-231">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="80e76-232">Nueikite į sritį **API teisės** ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="80e76-232">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="80e76-233">Pasirinkite **Įtraukti teisę**.</span><span class="sxs-lookup"><span data-stu-id="80e76-233">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="80e76-234">Pasirinkite **„Azure“ raktų saugykla**.</span><span class="sxs-lookup"><span data-stu-id="80e76-234">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="80e76-235">Pasirinkę perduotąsias teises, pasirinkite **vartotojas\_apsimetimas**.</span><span class="sxs-lookup"><span data-stu-id="80e76-235">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="80e76-236">Pasirinkite **Įtraukti teises**.</span><span class="sxs-lookup"><span data-stu-id="80e76-236">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="80e76-237">Programos meniu pasirinkite **Sertifikatai \& slaptieji raktai**, tada atlikite tolesnius veiksmus, kad sukurtumėte raktų saugyklos slaptųjų raktų.</span><span class="sxs-lookup"><span data-stu-id="80e76-237">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="80e76-238">Pasirinkite **Naujas kliento slaptasis raktas**.</span><span class="sxs-lookup"><span data-stu-id="80e76-238">Select **New client secret**.</span></span>
        2. <span data-ttu-id="80e76-239">Lauke **Rakto aprašas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="80e76-239">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="80e76-240">Pasirinkite trukmę, tada – **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="80e76-240">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="80e76-241">Slaptasis raktas sugeneruojamas lauke **Reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="80e76-241">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="80e76-242">Nukopijuokite ir įrašykite slaptąjį raktą.</span><span class="sxs-lookup"><span data-stu-id="80e76-242">Copy and save the secret value.</span></span>

4. <span data-ttu-id="80e76-243">Raktų saugyklos slaptųjų raktų kūrimas</span><span class="sxs-lookup"><span data-stu-id="80e76-243">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="80e76-244">Pereikite į anksčiau sukurtą raktų saugyklą ir pasirinkite **Slaptieji raktai**.</span><span class="sxs-lookup"><span data-stu-id="80e76-244">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="80e76-245">Su kiekvienu toliau pateiktoje lentelėje esančiu slaptojo rakto pavadinimu atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="80e76-245">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="80e76-246">Pasirinkite **Generuoti / importuoti**.</span><span class="sxs-lookup"><span data-stu-id="80e76-246">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="80e76-247">Dialogo lango **Slaptojo rakto kūrimas** lauke **Nusiuntimo parinktys** pasirinkite **Neautomatinis**.</span><span class="sxs-lookup"><span data-stu-id="80e76-247">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="80e76-248">Sukurkite slaptojo rakto pavadinimą ir reikšmę iš tolesnės lentelės.</span><span class="sxs-lookup"><span data-stu-id="80e76-248">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="80e76-249">Pasirinkite **Įjungta**, tada – **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="80e76-249">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="80e76-250">Slaptasis raktas sukuriamas ir įtraukiamas į raktų saugyklą.</span><span class="sxs-lookup"><span data-stu-id="80e76-250">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="80e76-251">Slaptas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="80e76-251">Secret name</span></span>                       | <span data-ttu-id="80e76-252">Slaptojo rakto reikšmė</span><span class="sxs-lookup"><span data-stu-id="80e76-252">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="80e76-253">app-id</span><span class="sxs-lookup"><span data-stu-id="80e76-253">app-id</span></span>                            | <span data-ttu-id="80e76-254">Programos, kurią sukūrėte anksčiau, ID</span><span class="sxs-lookup"><span data-stu-id="80e76-254">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="80e76-255">app-secret</span><span class="sxs-lookup"><span data-stu-id="80e76-255">app-secret</span></span>                        | <span data-ttu-id="80e76-256">Kliento slaptasis raktas, kurį įrašėte anksčiau</span><span class="sxs-lookup"><span data-stu-id="80e76-256">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="80e76-257">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="80e76-257">storage-account-name</span></span>              | <span data-ttu-id="80e76-258">Saugyklos paskyros, kurią sukūrėte anksčiau, pavadinimas, pvz., **1saugyklospaskyra**</span><span class="sxs-lookup"><span data-stu-id="80e76-258">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="80e76-259">storage-account-connection-string</span><span class="sxs-lookup"><span data-stu-id="80e76-259">storage-account-connection-string</span></span> | <span data-ttu-id="80e76-260">Jungimosi eilutė, kurią nukopijavote iš saugyklos paskyros puslapio **Prieigos raktai**</span><span class="sxs-lookup"><span data-stu-id="80e76-260">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="80e76-261">Programos autorizavimas norint pasiekti raktų saugyklą</span><span class="sxs-lookup"><span data-stu-id="80e76-261">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="80e76-262">[„Azure“ portale](https://portal.azure.com) atidarykite raktų saugyklą, kurią sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="80e76-262">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="80e76-263">Pasirinkite prieigos strategijas.</span><span class="sxs-lookup"><span data-stu-id="80e76-263">Select the access policies.</span></span>
    3. <span data-ttu-id="80e76-264">Su kiekviena toliau pateiktoje lentelėje esančia programa atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="80e76-264">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="80e76-265">Pasirinkite **Įtraukti prieigos strategiją**, kad sukurtumėte prieigos strategiją.</span><span class="sxs-lookup"><span data-stu-id="80e76-265">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="80e76-266">Lauke **Slaptųjų raktų teisės** pasirinkite teises iš tolesnės lentelės.</span><span class="sxs-lookup"><span data-stu-id="80e76-266">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="80e76-267">Lauke **Pasirinkti pagrindinį pavadinimą** ieškokite rodomo programos pavadinimo iš tolesnės lentelės.</span><span class="sxs-lookup"><span data-stu-id="80e76-267">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="80e76-268">Pasirinkite **Pasirinkti**.</span><span class="sxs-lookup"><span data-stu-id="80e76-268">Select **Select**.</span></span>
        5. <span data-ttu-id="80e76-269">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="80e76-269">Select **Add**.</span></span>
        6. <span data-ttu-id="80e76-270">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="80e76-270">Select **Save**.</span></span>

        | <span data-ttu-id="80e76-271">Prašymas</span><span class="sxs-lookup"><span data-stu-id="80e76-271">Application</span></span>                                              | <span data-ttu-id="80e76-272">Teisės</span><span class="sxs-lookup"><span data-stu-id="80e76-272">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="80e76-273">Naujos programos, kurią sukūrėte, rodomas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="80e76-273">The display name of the new application that you created</span></span> | <span data-ttu-id="80e76-274">Get, List</span><span class="sxs-lookup"><span data-stu-id="80e76-274">Get, List</span></span>   |
        | <span data-ttu-id="80e76-275">**„Microsoft Dynamics ERP Microservices“**</span><span class="sxs-lookup"><span data-stu-id="80e76-275">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="80e76-276">Get, List</span><span class="sxs-lookup"><span data-stu-id="80e76-276">Get, List</span></span>   |

6. <span data-ttu-id="80e76-277">Vaidmenų priskyrimas, kad būtų galima pasiekti saugyklos paskyrą</span><span class="sxs-lookup"><span data-stu-id="80e76-277">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="80e76-278">[„Azure“ portale](https://portal.azure.com) atidarykite saugyklos paskyrą, kurią sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="80e76-278">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="80e76-279">Pasirinkite **Prieigos valdymas (IAM)**, tada – **Vaidmenų priskyrimai**.</span><span class="sxs-lookup"><span data-stu-id="80e76-279">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="80e76-280">Pasirinkite **Įtraukti, įtraukti vaidmens priskyrimą**.</span><span class="sxs-lookup"><span data-stu-id="80e76-280">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="80e76-281">Su kiekviena toliau pateiktoje lentelėje esančia programa atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="80e76-281">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="80e76-282">Iš tolesnės lentelės pasirinkite vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="80e76-282">Select the role from the following table.</span></span>
        2. <span data-ttu-id="80e76-283">Lauką **Kam priskirti prieigą** palikite nustatytą kaip **„Azure AD“ vartotojas, grupė arba pagrindinis tarnybos pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="80e76-283">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="80e76-284">Lauke **Pasirinkti** įveskite programą iš tolesnės lentelės.</span><span class="sxs-lookup"><span data-stu-id="80e76-284">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="80e76-285">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="80e76-285">Select **Save**.</span></span>

        | <span data-ttu-id="80e76-286">Prašymas</span><span class="sxs-lookup"><span data-stu-id="80e76-286">Application</span></span>                                              | <span data-ttu-id="80e76-287">Vaidmuo</span><span class="sxs-lookup"><span data-stu-id="80e76-287">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="80e76-288">Naujos programos, kurią sukūrėte, rodomas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="80e76-288">The display name of the new application that you created</span></span> | <span data-ttu-id="80e76-289">Savininkas</span><span class="sxs-lookup"><span data-stu-id="80e76-289">Owner</span></span>                       |
        | <span data-ttu-id="80e76-290">Naujos programos, kurią sukūrėte, rodomas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="80e76-290">The display name of the new application that you created</span></span> | <span data-ttu-id="80e76-291">Bendraautorius</span><span class="sxs-lookup"><span data-stu-id="80e76-291">Contributor</span></span>                 |
        | <span data-ttu-id="80e76-292">Naujos programos, kurią sukūrėte, rodomas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="80e76-292">The display name of the new application that you created</span></span> | <span data-ttu-id="80e76-293">Saugyklos paskyros bendraautoris</span><span class="sxs-lookup"><span data-stu-id="80e76-293">Storage Account Contributor</span></span> |
        | <span data-ttu-id="80e76-294">Naujos programos, kurią sukūrėte, rodomas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="80e76-294">The display name of the new application that you created</span></span> | <span data-ttu-id="80e76-295">Saugyklos didelių dvejetainių objektų duomenų savininkas</span><span class="sxs-lookup"><span data-stu-id="80e76-295">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="80e76-296">**„AI Builder“ autorizavimo tarnyba**</span><span class="sxs-lookup"><span data-stu-id="80e76-296">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="80e76-297">Saugyklos didelių dvejetainių objektų duomenų skaitytojas</span><span class="sxs-lookup"><span data-stu-id="80e76-297">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="80e76-298">„Azure“ CLI</span><span class="sxs-lookup"><span data-stu-id="80e76-298">Azure CLI</span></span>](#tab/azure-azure-cli)

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



## <a name="configure-the-data-lake"></a><span data-ttu-id="80e76-299">Duomenų telkinio konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="80e76-299">Configure the data lake</span></span>

<span data-ttu-id="80e76-300">Atlikite šiuos veiksmus, kad, naudodami LCS, įtrauktumėte „Azure Data Lake“ papildinį į aplinką.</span><span class="sxs-lookup"><span data-stu-id="80e76-300">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="80e76-301">Prisijunkite prie LCS, tada dešinėje puslapio pusėje, prie aplinkos pavadinimo pasirinkite **Išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="80e76-301">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="80e76-302">Skyriuje **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="80e76-302">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="80e76-303">Pasirinkite papildinį **Eksportavimas į „Data Lake“**.</span><span class="sxs-lookup"><span data-stu-id="80e76-303">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="80e76-304">Įveskite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="80e76-304">Enter the following values.</span></span>

    | <span data-ttu-id="80e76-305">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="80e76-305">Value</span></span>                                                              | <span data-ttu-id="80e76-306">aprašymas</span><span class="sxs-lookup"><span data-stu-id="80e76-306">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="80e76-307">„Azure“ prenumeratos nuomotojo ID, nurodantį raktų saugyklos vietą</span><span class="sxs-lookup"><span data-stu-id="80e76-307">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="80e76-308">Nuomotojo ID, nurodantį saugyklos paskyros, programų ir raktų saugyklų vietą.</span><span class="sxs-lookup"><span data-stu-id="80e76-308">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="80e76-309">Norėdami rasti šią reikšmę, atidarykite [„Azure“ portalą](https://portal.azure.com), nueikite į **„Azure Active Directory“** ir nukopijuokite elemento **Nuomotojo ID** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="80e76-309">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="80e76-310">Pateikite savo „Key Vault“ DNS pavadinimą</span><span class="sxs-lookup"><span data-stu-id="80e76-310">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="80e76-311">Raktų saugyklos DNS pavadinimas, pvz., `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="80e76-311">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="80e76-312">(Ši reikšmė atitinka DNS pavadinimą, kuris naudojamas objektų saugykloje.)</span><span class="sxs-lookup"><span data-stu-id="80e76-312">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="80e76-313">Pateikite slaptąjį raktą, kurį sudaro saugyklos paskyros pavadinimas</span><span class="sxs-lookup"><span data-stu-id="80e76-313">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="80e76-314">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="80e76-314">**storage-account-name**</span></span> |
    | <span data-ttu-id="80e76-315">Programos ID, kuris bus naudojamas „Data Lake“ pasiekti, slaptas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="80e76-315">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="80e76-316">**app-id**</span><span class="sxs-lookup"><span data-stu-id="80e76-316">**app-id**</span></span> |
    | <span data-ttu-id="80e76-317">Slaptas pavadinimas, kuris bus naudojamas su programos ID</span><span class="sxs-lookup"><span data-stu-id="80e76-317">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="80e76-318">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="80e76-318">**app-secret**</span></span> |

5. <span data-ttu-id="80e76-319">Sutikite su sąlygomis ir pasirinkite **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="80e76-319">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="80e76-320">Papildinys bus įdiegtas per kelias minutes.</span><span class="sxs-lookup"><span data-stu-id="80e76-320">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="80e76-321">„AI Builder“ konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="80e76-321">Configure AI Builder</span></span>

1. <span data-ttu-id="80e76-322">Prisijunkite prie LCS ir atidarykite puslapį **Aplinkos informacija**.</span><span class="sxs-lookup"><span data-stu-id="80e76-322">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="80e76-323">Slinkite iki dalies **Aplinkos papildiniai**.</span><span class="sxs-lookup"><span data-stu-id="80e76-323">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="80e76-324">Turėtumėte matyti šioje aplinkoje jau įdiegtus papildinius.</span><span class="sxs-lookup"><span data-stu-id="80e76-324">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="80e76-325">Jei papildinio **Eksportavimas į „Data Lake“** tarp jų nėra, šį papildinį sukonfigūruokite.</span><span class="sxs-lookup"><span data-stu-id="80e76-325">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="80e76-326">Pasirinkite papildinį **Įžvalgų gavimas**.</span><span class="sxs-lookup"><span data-stu-id="80e76-326">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="80e76-327">Papildinio **Įžvalgų gavimas** informacijos puslapyje įveskite tolesnes reikšmes.</span><span class="sxs-lookup"><span data-stu-id="80e76-327">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="80e76-328">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="80e76-328">Value</span></span>                                                    | <span data-ttu-id="80e76-329">Aprašas</span><span class="sxs-lookup"><span data-stu-id="80e76-329">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="80e76-330">CDS organizacijos URL</span><span class="sxs-lookup"><span data-stu-id="80e76-330">CDS Organization URL</span></span>                                     | <span data-ttu-id="80e76-331">Organizacijos „Dataverse“ URL nukopijuotas iš aukščiau.</span><span class="sxs-lookup"><span data-stu-id="80e76-331">The Dataverse organization URL copied from above.</span></span> |
    | <span data-ttu-id="80e76-332">CDS org. ID</span><span class="sxs-lookup"><span data-stu-id="80e76-332">CDS Org ID</span></span>                                               | <span data-ttu-id="80e76-333">Organizacijos „Dataverse“ ID nukopijuotas iš aukščiau.</span><span class="sxs-lookup"><span data-stu-id="80e76-333">The Dataverse organization ID copied from above.</span></span> |
5. <span data-ttu-id="80e76-334">įjunkite **Ar tai numatytoji nuomotojo aplinka**.</span><span class="sxs-lookup"><span data-stu-id="80e76-334">Enable **Is this the default environment for you Tenant**.</span></span>
    
## <a name="configure-the-entity-store"></a><span data-ttu-id="80e76-335">Objektų saugyklos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="80e76-335">Configure the entity store</span></span>

<span data-ttu-id="80e76-336">Atlikite tolesnius veiksmus, kad nustatytumėte objektų saugyklą savo „Finance“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="80e76-336">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="80e76-337">Nueikite į **Sistemos administravimas \> Sąranka \> Sistemos parametrai \> Duomenų ryšiai**.</span><span class="sxs-lookup"><span data-stu-id="80e76-337">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="80e76-338">Nustatykite šiuos raktų saugyklos laukus:</span><span class="sxs-lookup"><span data-stu-id="80e76-338">Set the following key vault fields:</span></span>

    - <span data-ttu-id="80e76-339">**Programos (kliento) ID** – įveskite anksčiau sukurtą programos kliento ID.</span><span class="sxs-lookup"><span data-stu-id="80e76-339">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="80e76-340">**Programos slaptasis raktas** – įveskite slaptąjį raktą, kurį įrašėte anksčiau sukurtai programai.</span><span class="sxs-lookup"><span data-stu-id="80e76-340">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="80e76-341">**DNS pavadinimas** – domeno vardų sistemos (DNS) pavadinimą galite rasti programos, kurią sukūrėte anksčiau, išsamios informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="80e76-341">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="80e76-342">**Slaptojo rakto pavadinimas** – įveskite **storage-account-connection-string**.</span><span class="sxs-lookup"><span data-stu-id="80e76-342">**Secret name** – Enter **storage-account-connection-string**.</span></span>
3. <span data-ttu-id="80e76-343">Įjunkite **Įjungti „Data Lake“ integraciją**.</span><span class="sxs-lookup"><span data-stu-id="80e76-343">Enable **Enable Data Lake integration**.</span></span>
4. <span data-ttu-id="80e76-344">Pasirinkite **Tikrinti „Azure Key Vault"** ir patikrinkite, ar nėra klaidų.</span><span class="sxs-lookup"><span data-stu-id="80e76-344">Select **Test Azure Key Vault** and verify there are no errors.</span></span>
5. <span data-ttu-id="80e76-345">Pasirinkite **Tikrinti „Azure" talpyklą** ir patikrinkite, ar nėra klaidų.</span><span class="sxs-lookup"><span data-stu-id="80e76-345">Select **Test Azure storage** and verify there are no errors.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="80e76-346">Atsiliepimai ir palaikymas</span><span class="sxs-lookup"><span data-stu-id="80e76-346">Feedback and support</span></span>

<span data-ttu-id="80e76-347">Jei norite pateikti atsiliepimų ar reikia pagalbos, atsiųskite el. laišką [kliento mokėjimo įžvalgų (peržiūros versija)](mailto:fiap@microsoft.com) el. pašto adresu.</span><span class="sxs-lookup"><span data-stu-id="80e76-347">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="80e76-348">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="80e76-348">Privacy notice</span></span>

<span data-ttu-id="80e76-349">Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.</span><span class="sxs-lookup"><span data-stu-id="80e76-349">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
