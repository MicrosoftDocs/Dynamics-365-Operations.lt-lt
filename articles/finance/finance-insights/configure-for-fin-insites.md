---
title: Modulio Finansinės įžvalgos konfigūracija (peržiūros versija)
description: Šioje temoje paaiškinami konfigūravimo veiksmai, kuriuos jums atlikus sistema galės naudotis modulio Finansinės įžvalgos galimybėmis.
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
ms.openlocfilehash: 2443bb057a8b7fe280ed26ecae4e50f671b5e082
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818805"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="aee1a-103">Modulio Finansinės įžvalgos konfigūracija (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="aee1a-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="aee1a-104">Modulyje Finansinės įžvalgos sujungiamos „Microsoft Dynamics 365 Finance“ ir „Microsoft Dataverse“, „Azure“ bei „AI Builder“ funkcijos, kad jūsų organizacijai būtų suteikiami galingi prognozavimo įrankiai.</span><span class="sxs-lookup"><span data-stu-id="aee1a-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="aee1a-105">Šioje temoje paaiškinami konfigūravimo veiksmai, kuriuos jums atlikus sistema galės naudotis modulio Finansinės įžvalgos galimybėmis.</span><span class="sxs-lookup"><span data-stu-id="aee1a-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="aee1a-106">„Dynamics 365 Finance“ diegimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="aee1a-107">Aplinkas galite įdiegti atlikdami toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="aee1a-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="aee1a-108">Portale „Microsoft Dynamics Lifecycle Services“ (LCS) sukurkite arba atnaujinkite „Dynamics 365 Finance“ aplinką.</span><span class="sxs-lookup"><span data-stu-id="aee1a-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="aee1a-109">Aplinkai reikalinga programos 10.0.11 versija / 35 arba naujesnis platformos atnaujinimas.</span><span class="sxs-lookup"><span data-stu-id="aee1a-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="aee1a-110">Aplinka turi būti didelio pasiekiamumo (HA) smėlio dėžės aplinka.</span><span class="sxs-lookup"><span data-stu-id="aee1a-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="aee1a-111">(Šis aplinkos tipas dar vadinamas 2 pakopos aplinka.) Norėdami gauti daugiau informacijos, žr. [Aplinkos planavimas](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="aee1a-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="aee1a-112">Jei naudojate „Contoso“ demonstracinius duomenis, jums reikės papildomų duomenų pavyzdžių, kad galėtumėte naudoti kliento mokėjimo prognozių, grynųjų pinigų srautų prognozių ir biudžeto prognozių funkcijas.</span><span class="sxs-lookup"><span data-stu-id="aee1a-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="aee1a-113">Konfigūruoti „Dataverse“</span><span class="sxs-lookup"><span data-stu-id="aee1a-113">Configure Dataverse</span></span>

<span data-ttu-id="aee1a-114">Galite atlikti toliau nurodytus neautomatinius konfigūravimo veiksmus arba galite pagreitinti konfigūracijos procesą, naudodami pateiktą „Windows PowerShell“ scenarijų.</span><span class="sxs-lookup"><span data-stu-id="aee1a-114">You can complete the manual configuration steps that follow, or you can speed up the configuration process by using the Windows PowerShell script that is provided.</span></span> <span data-ttu-id="aee1a-115">Kai „PowerShell“ scenarijus bus baigtas vykdyti, jis jums pateiks reikšmes, naudotinas konfigūruojant modulį Finansinės įžvalgos.</span><span class="sxs-lookup"><span data-stu-id="aee1a-115">When the PowerShell script has finished running, it will give you values to use to configure Finance insights.</span></span> 

> [!NOTE]
> <span data-ttu-id="aee1a-116">Atidarykite „PowerShell“ kompiuteryje ir vykdykite scenarijų.</span><span class="sxs-lookup"><span data-stu-id="aee1a-116">Open PowerShell on your PC to run the script.</span></span> <span data-ttu-id="aee1a-117">Jums gali reikėti „PowerShell“ 5 versijos.</span><span class="sxs-lookup"><span data-stu-id="aee1a-117">You may need PowerShell version 5.</span></span> <span data-ttu-id="aee1a-118">„Microsoft Azure“ CLI parinktis „Išbandykite“ gali neveikti.</span><span class="sxs-lookup"><span data-stu-id="aee1a-118">The Microsoft Azure CLI "Try it" option may not work.</span></span>

# <a name="manual-configuration-steps"></a>[<span data-ttu-id="aee1a-119">Neautomatinio konfigūravimo veiksmai</span><span class="sxs-lookup"><span data-stu-id="aee1a-119">Manual configuration steps</span></span>](#tab/configuration-steps)

1. <span data-ttu-id="aee1a-120">Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com/) ir atlikite tolesnius veiksmus, kad sukurtumėte naują „Dataverse“ aplinką tame pačiame „Active Directory“ nuomotojuje.</span><span class="sxs-lookup"><span data-stu-id="aee1a-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="aee1a-121">Atidarykite puslapį **Aplinkos**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-121">Open the **Environments** page.</span></span>

        <span data-ttu-id="aee1a-122">[![Puslapis Aplinkos](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="aee1a-122">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="aee1a-123">Pasirinkite **Nauja aplinka**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-123">Select **New environment**.</span></span>
    3. <span data-ttu-id="aee1a-124">Lauke **Tipas** pasirinkite **Smėlio dėžė**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-124">In the **Type** field, select **Sandbox**.</span></span>
    4. <span data-ttu-id="aee1a-125">Parinktį **Kurti duomenų bazę** nustatykite kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-125">Set the **Create Database** option to **Yes**.</span></span>
    5. <span data-ttu-id="aee1a-126">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-126">Select **Next**.</span></span>
    6. <span data-ttu-id="aee1a-127">Pasirinkite savo organizacijos kalbą ir valiutą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-127">Select the language and currency for your organization.</span></span>
    7. <span data-ttu-id="aee1a-128">Priimkite numatytąsias kitų laukų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="aee1a-128">Accept the default values for the other fields.</span></span>
    8. <span data-ttu-id="aee1a-129">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-129">Select **Save**.</span></span>
    9. <span data-ttu-id="aee1a-130">Atnaujinkite puslapį **Aplinkos**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-130">Refresh the **Environments** page.</span></span>
    10. <span data-ttu-id="aee1a-131">Palaukite, kol lauko **Būsena** reikšmė bus atnaujinta į **Parengta**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-131">Wait until the value of the **State** field is updated to **Ready**.</span></span>
    11. <span data-ttu-id="aee1a-132">Užsirašykite „Dataverse“ organizacijos ID.</span><span class="sxs-lookup"><span data-stu-id="aee1a-132">Make a note of the Dataverse organization ID.</span></span>
    12. <span data-ttu-id="aee1a-133">Pasirinkite aplinką, tada – **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-133">Select the environment, and then select **Settings**.</span></span>
    13. <span data-ttu-id="aee1a-134">Pasirinkite **Ištekliai \> Visi senstelėję parametrai**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-134">Select **Resources \> All Legacy Settings**.</span></span>
    14. <span data-ttu-id="aee1a-135">Viršutinėje naršymo juostoje pasirinkite **Parametrai**, tada – **Tinkinimai**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-135">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    15. <span data-ttu-id="aee1a-136">Pasirinkite **Kūrėjo ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-136">Select **Developer Resources**.</span></span>
    16. <span data-ttu-id="aee1a-137">Lauką **Egzemplioriaus nuorodos informacijos ID** nustatykite kaip „Dataverse“ organizacijos ID reikšmę, kuria pasižymėjote anksčiau.</span><span class="sxs-lookup"><span data-stu-id="aee1a-137">Set the **Instance Reference Information ID** field to the Dataverse organization ID value that you made a note of earlier.</span></span>
    17. <span data-ttu-id="aee1a-138">Naršyklės adreso juostoje pasižymėkite „Dataverse“ organizacijos URL.</span><span class="sxs-lookup"><span data-stu-id="aee1a-138">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="aee1a-139">Pavyzdžiui, URL gali būti `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="aee1a-139">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

2. <span data-ttu-id="aee1a-140">Jei planuojate naudoti grynųjų pinigų srauto prognozių arba biudžeto prognozių funkciją, atlikite tolesnius veiksmus, kad atnaujintumėte savo organizacijos komentavimo limitą bent iki 50 megabaitų (MB).</span><span class="sxs-lookup"><span data-stu-id="aee1a-140">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="aee1a-141">Atidarykite [„Power Apps“ portalą](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="aee1a-141">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="aee1a-142">Pasirinkite aplinką, kurią ką tik sukūrėte, tada pasirinkite **Išplėstiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-142">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="aee1a-143">Pasirinkite **Parametrai \> El. pašto konfigūravimas**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-143">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="aee1a-144">Pakeiskite lauko **Didžiausias failo dydis** reikšmę į **51 200**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-144">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="aee1a-145">(Reikšmė išreikšta kilobaitais \[KB\].)</span><span class="sxs-lookup"><span data-stu-id="aee1a-145">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="aee1a-146">Pasirinkite **Gerai**, kad įrašytumėte keitimus.</span><span class="sxs-lookup"><span data-stu-id="aee1a-146">Select **OK** to save your changes.</span></span>

# <a name="windows-powershell-configuration-script"></a>[<span data-ttu-id="aee1a-147">„Windows PowerShell“ konfigūracijos scenarijus</span><span class="sxs-lookup"><span data-stu-id="aee1a-147">Windows PowerShell configuration script</span></span>](#tab/powershell-configuration-script)

```azurecli-interactive
Write-Output 'The following modules need to be present for execution of this script:'
Write-Output '  Microsoft.PowerApps.Administration.PowerShell'
Write-Output '  Microsoft.PowerApps.PowerShell'
Write-Output '  Microsoft.Xrm.Tooling.CrmConnector.PowerShell'

try {
    $moduleConsent = Read-Host 'Is it ok to install or update these modules as needed? (yes/no)'
    if ($moduleConsent -ne 'yes' -and $moduleConsent -ne 'y') {
        Write-Warning 'User declined to install required modules.'
        return
    }

    $module = 'Microsoft.PowerApps.Administration.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '2.0.61' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '2.0.61' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.PowerApps.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '1.0.9' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '1.0.9' -AllowClobber -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.Xrm.Tooling.CrmConnector.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '3.3.0.892' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '3.3.0.892' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    Write-Output '================================================================================='

    $useMfa = $false
    $useMfaPrompt = Read-Host "Does your organization require the use of multi-factor authentication? (yes/no)"
    if ($useMfaPrompt -eq 'yes' -or $useMfaPrompt -eq 'y') {
        $useMfa = $true
    }
    if(-not $useMfa) {
        $credential = Get-Credential -Message 'Power Apps Credential'
    }

    $orgFriendlyName = Read-Host "Enter the name of the CDS Organization to use or create: (blank for 'FinanceInsightsOrg')"
    if ($orgFriendlyName.Trim() -eq '') {
        $orgFriendlyName = 'FinanceInsightsOrg'
    }

    $isDefaultOrgPrompt = Read-Host ("Is '" + $orgFriendlyName + "' the default organization for your tenant? (yes/no)")
    if ($isDefaultOrgPrompt -eq 'yes' -or $isDefaultOrgPrompt -eq 'y') {
        $isDefaultOrg = $true
    }

    if ($credential) {
        Add-PowerAppsAccount -Username $credential.UserName -Password $credential.Password
    }
    else {
        Add-PowerAppsAccount
    }

    if ($isDefaultOrg) {
        $orgMatch = ('(default)')
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { $_.IsDefault -eq $true })
    }
    else {
        $orgMatch = ('{0} (*)' -f $orgFriendlyName)
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.IsDefault -eq $false -and ($_.DisplayName -eq $orgFriendlyName -or $_.DisplayName -like $orgMatch)) })
    }

    $getCrmOrgParams = @{ 'OnlineType' = 'Office365' }
    if ($credential) {
        $getCrmOrgParams.Credential = $credential
    }

    if ($null -eq $environment) {
        Write-Output '================================================================================='
        Write-Output 'PowerApps environment not found. A new one will be provisioned.'

        $invalid = 'invalid'

        $location = $invalid
        $cdsLocations = (Get-AdminPowerAppEnvironmentLocations | Select-Object LocationName).LocationName
        while (-not ($location -in $cdsLocations)) {
            $location = (Read-Host -Prompt "Enter the location in which to create the new PowerApps environment: ('help' to see values)")
            if ($location -eq 'help') {
                $cdsLocations
            }
        }

        $currency = $invalid
        $cdsCurrencies = (Get-AdminPowerAppCdsDatabaseCurrencies -Location $location | Select-Object CurrencyName).CurrencyName
        while ($currency -ne '' -and -not ($currency -in $cdsCurrencies)) {
            $currency = (Read-Host -Prompt "Enter the currency to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($currency -eq 'help') {
                $cdsCurrencies
            }
        }

        $language = $invalid
        $cdsLanguages = (Get-AdminPowerAppCdsDatabaseLanguages -Location $location | Select-Object LanguageName, LanguageDisplayName)
        while ($language -ne '' -and -not ($language -in $cdsLanguages.LanguageName)) {
            $language = (Read-Host -Prompt "Enter the language name to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($language -eq 'help') {
                $cdsLanguages | Format-Table -Property LanguageName, LanguageDisplayName
            }
        }

        Write-Output 'Provisioning PowerApps environment. This may take several minutes.'

        $sleep = 15

        $envParams = @{ 'DisplayName' = $orgFriendlyName; 'EnvironmentSku' = 'Sandbox'; 'ProvisionDatabase' = $true; 'Location' = $location; 'WaitUntilFinished' = $true }
        if ($language.Trim() -ne '') {
            $envParams.LanguageName = $language
        }
        if ($currency.Trim() -ne '') {
            $envParams.CurrencyName = $currency
        }
        $newEnvResult = New-AdminPowerAppEnvironment @envParams
        if (($null -eq $newEnvResult) -or ($newEnvResult.CommonDataServiceDatabaseProvisioningState -ne 'Succeeded')) {
            Write-Warning 'Failed to create to PowerApps environment'
            if ($null -ne $newEnvResult) {
                $newEnvResult
            }
        }
        else {
            $environment = $null
            $retryCount = 0
            while (($null -eq $environment) -and ($retryCount -lt 5)) {
                Start-Sleep -Seconds $sleep
                $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.DisplayName -like $orgMatch) })
            }
            Write-Output ("Provisioned PowerApps environment with name: '" + $environment.DisplayName + "'")
        }

        Write-Output 'Waiting for CDS organization provisioning. This may take several minutes.'
        if (-not $credential) {
            $sleep = 120
            Write-Output 'You may be prompted for credentials multiple times while checking the status of the provisioning.'
        }

        while ($null -eq $crmOrg) {
            Start-Sleep -Seconds $sleep
            $crmOrg = (Get-CrmOrganizations @getCrmOrgParams) | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }
    else {
        $crmOrgs = Get-CrmOrganizations @getCrmOrgParams
        if ($UseDefaultOrganization -eq $true) {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -match $orgMatch }
        }
        else {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }

    Write-Output '================================================================================='
    Write-Output 'Values for PowerAI LCS Add-In:'
    Write-Output ("  CDS organization url:             " + $crmOrg.WebApplicationUrl)
    Write-Output ("  CDS organization ID:              " + $crmOrg.OrganizationId)
}
catch {
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $_.Exception.InnerException
    while ($null -ne $inner) {
        Write-Output 'Inner Exception:'
        Write-Error $_.Exception.Message
        Write-Warning $_.Exception.StackTrace
        $inner = $inner.InnerException
    }
}
```
---

## <a name="configure-the-azure-setup"></a><span data-ttu-id="aee1a-148">„Azure“ sąrankos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-148">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="aee1a-149">„Dataverse“ katalogo ID ir vartotojo „Azure AD“ objekto ID įvedimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-149">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="aee1a-150">Įveskite „Dataverse“ katalogo ID.</span><span class="sxs-lookup"><span data-stu-id="aee1a-150">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="aee1a-151">Atidarykite [„Azure“ portalą](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="aee1a-151">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="aee1a-152">Prisijunkite naudodami vartotojo ID, kuris buvo naudojamas kuriant „Dataverse“ aplinką.</span><span class="sxs-lookup"><span data-stu-id="aee1a-152">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="aee1a-153">Eikite į **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-153">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="aee1a-154">Nukopijuokite elemento **Nuomotojo ID** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aee1a-154">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="aee1a-155">Įveskite vartotojo „Azure Active Directory“ („Azure AD“) objekto ID.</span><span class="sxs-lookup"><span data-stu-id="aee1a-155">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="aee1a-156">[„Azure“ portale](https://portal.azure.com) eikite į **Vartotojai** ir ieškokite vartotojo pagal el. pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-156">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="aee1a-157">Pasirinkite vartotojo vardą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-157">Select the user's name.</span></span>
    3. <span data-ttu-id="aee1a-158">Nukopijuokite elemento **Objekto ID** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aee1a-158">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="aee1a-159">„Azure Cloud Shell“ naudojimas modulio Finansinės įžvalgos „Data Lake“ ištekliams nustatyti</span><span class="sxs-lookup"><span data-stu-id="aee1a-159">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="aee1a-160">„Windows PowerShell“ scenarijaus naudojimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-160">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="aee1a-161">Pateiktas „Windows PowerShell“ scenarijus, kad būtų galima lengvai nustatyti „Azure“ išteklius, aprašytus temoje [Eksportavimo į „Azure Data Lake“ konfigūravimas](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake).</span><span class="sxs-lookup"><span data-stu-id="aee1a-161">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake).</span></span> <span data-ttu-id="aee1a-162">Jei norite nustatyti neautomatiniu būdu, praleiskite šią procedūrą ir vykdykite procedūrą, aprašytą skyriuje [Neautomatinė sąranka](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="aee1a-162">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="aee1a-163">Atlikite tolesnius veiksmus, kad būtų vykdomas „PowerShell“ scenarijus.</span><span class="sxs-lookup"><span data-stu-id="aee1a-163">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="aee1a-164">„Azure“ CLI parinktis „Išbandykite“ arba scenarijaus vykdymas jūsų kompiuteryje gali neveikti.</span><span class="sxs-lookup"><span data-stu-id="aee1a-164">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="aee1a-165">Atlikite šiuos veiksmus, kad sukonfigūruotumėte „Azure“ naudodami „Windows PowerShell“ scenarijų.</span><span class="sxs-lookup"><span data-stu-id="aee1a-165">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="aee1a-166">Turite turėti teises sukurti „Azure“ išteklių grupę, „Azure“ išteklius ir „Azure AD“ programą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-166">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="aee1a-167">Norėdami gauti informacijos apie reikiamas teises, žr. [„Azure AD“ teisių patikrinimas](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="aee1a-167">For information about the required permissions, see [Check Azure AD permissions](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="aee1a-168">[„Azure“ portale](https://portal.azure.com) eikite į savo tikslinę „Azure“ prenumeratą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-168">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="aee1a-169">Pasirinkite mygtuką **„Cloud Shell“**, esantį lauko **Ieška** dešinėje.</span><span class="sxs-lookup"><span data-stu-id="aee1a-169">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="aee1a-170">Pasirinkite **„PowerShell“**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-170">Select **PowerShell**.</span></span>
3. <span data-ttu-id="aee1a-171">Sukurkite saugyklą, jei būsite paraginti tai padaryti.</span><span class="sxs-lookup"><span data-stu-id="aee1a-171">Create storage, if you're prompted to do so.</span></span> <span data-ttu-id="aee1a-172">Tada nusiųskite „Windows PowerShell“ scenarijų į seansą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-172">Then upload the Windows PowerShell script to the session.</span></span>
4. <span data-ttu-id="aee1a-173">Scenarijų paleiskite.</span><span class="sxs-lookup"><span data-stu-id="aee1a-173">Run the script.</span></span>
5. <span data-ttu-id="aee1a-174">Vykdykite raginimus paleisti scenarijų.</span><span class="sxs-lookup"><span data-stu-id="aee1a-174">Follow the prompts to run the script.</span></span>
6. <span data-ttu-id="aee1a-175">Naudokite scenarijaus pateikiamą informaciją, kad į LCS įdiegtumėte papildinį **Eksportavimas į „Data Lake“**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-175">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
7. <span data-ttu-id="aee1a-176">Naudokite scenarijaus pateikiamą informaciją, kad „Finance“ puslapyje **Duomenų ryšiai** įjungtumėte objektų saugyklą (**Sistemos administravimas \> Sistemos parametrai \> Duomenų ryšiai**).</span><span class="sxs-lookup"><span data-stu-id="aee1a-176">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="aee1a-177">Neautomatinė sąranka</span><span class="sxs-lookup"><span data-stu-id="aee1a-177">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="aee1a-178">Programų įtraukimas į „Azure AD“ nuomotoją</span><span class="sxs-lookup"><span data-stu-id="aee1a-178">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="aee1a-179">[„Azure“ portale](https://portal.azure.com) nueikite į **„Azure Active Directory“**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-179">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="aee1a-180">Pasirinkite **Tvarkyti \> Įmonės programos**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-180">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="aee1a-181">Ieškokite tolesnių programų pagal programos ID.</span><span class="sxs-lookup"><span data-stu-id="aee1a-181">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="aee1a-182">Prašymas</span><span class="sxs-lookup"><span data-stu-id="aee1a-182">Application</span></span>                              | <span data-ttu-id="aee1a-183">Programos ID</span><span class="sxs-lookup"><span data-stu-id="aee1a-183">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="aee1a-184">„Microsoft Dynamics ERP Microservices“</span><span class="sxs-lookup"><span data-stu-id="aee1a-184">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="aee1a-185">„0cdb527f-a8d1-4bf8-9436-b352c68682b2“</span><span class="sxs-lookup"><span data-stu-id="aee1a-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="aee1a-186">„Microsoft Dynamics ERP Microservices CDS“</span><span class="sxs-lookup"><span data-stu-id="aee1a-186">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="aee1a-187">„703e2651-d3fc-48f5-942c-74274233dba8“</span><span class="sxs-lookup"><span data-stu-id="aee1a-187">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="aee1a-188">„AI Builder“ autorizavimo tarnyba</span><span class="sxs-lookup"><span data-stu-id="aee1a-188">AI Builder Authorization Service</span></span>         | <span data-ttu-id="aee1a-189">„ad40333e-9910-4b61-b281-e3aeeb8c3ef3“</span><span class="sxs-lookup"><span data-stu-id="aee1a-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="aee1a-190">Jeigu negalite rasti nė vienos iš ankstesnių programų, bandykite atlikti tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="aee1a-190">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="aee1a-191">Vietiniame kompiuteryje pasirinkite meniu **Pradėti** ir ieškokite **powershell**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-191">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="aee1a-192">Pasirinkite ir laikykite (arba dešiniuoju pelės mygtuku spustelėkite) **„Windows PowerShell“**, tada pasirinkite **Paleisti administratoriaus teisėmis**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-192">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="aee1a-193">Vykdykite tolesnę komandą, kad įdiegtumėte **„AzureAD“** modulį.</span><span class="sxs-lookup"><span data-stu-id="aee1a-193">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="aee1a-194">Jei reikalaujama „NuGet“ teikėjo, kad galėtumėte tęsti, pasirinkite **Y**, kad jį įdiegtumėte.</span><span class="sxs-lookup"><span data-stu-id="aee1a-194">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="aee1a-195">Jei pasirodo pranešimas „Nepatikima saugykla“, norėdami tęsti pasirinkite **Y**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-195">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="aee1a-196">Kiekvienai programai, kuri turi būti įtraukta, vykdykite toliau nurodytas komandas, kad įtrauktumėte programą į „Azure AD“.</span><span class="sxs-lookup"><span data-stu-id="aee1a-196">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="aee1a-197">Kai būsite paraginti, prisijunkite kaip „Azure AD“ administratorius.</span><span class="sxs-lookup"><span data-stu-id="aee1a-197">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="aee1a-198">„Azure“ išteklių kūrimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-198">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="aee1a-199">Įsitikinkite, kad sukūrėte tolesnius išteklius tame pačiame „Azure AD“ egzemplioriuje, kaip „Dataverse“ aplinka.</span><span class="sxs-lookup"><span data-stu-id="aee1a-199">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="aee1a-200">Negalite naudoti išteklių iš kito „Azure AD“ egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="aee1a-200">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="aee1a-201">Naujos saugyklos paskyros kūrimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-201">Create a new storage account:</span></span>

    1. <span data-ttu-id="aee1a-202">[„Azure“ portale](https://portal.azure.com) sukurkite saugyklos paskyrą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-202">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="aee1a-203">Dialogo lange **Saugyklos paskyros kūrimas** nustatykite tolesnius laukus.</span><span class="sxs-lookup"><span data-stu-id="aee1a-203">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="aee1a-204">**Vieta** – pasirinkite duomenų centrą, kuriame yra jūsų aplinka.</span><span class="sxs-lookup"><span data-stu-id="aee1a-204">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="aee1a-205">**Našumas** – rekomenduojame pasirinkti **Standartinis**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-205">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="aee1a-206">**Paskyros rūšis** – turite pasirinkti **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-206">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="aee1a-207">Dialogo lange **Išplėstinės parinktys**, prie parinkties **„Data Lake Storage Gen2“** (funkcija **Hierarchninės vardų sritys**) pasirinkite **Įjungti**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-207">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="aee1a-208">Jei šią funkciją išjungsite, negalėsite naudoti duomenų, kuriuos „Finance and Operations“ programos rašo naudodamos tokias tarnybas, kaip „Power BI“ duomenų srautai.</span><span class="sxs-lookup"><span data-stu-id="aee1a-208">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="aee1a-209">Pasirinkite **Peržiūrėti ir kurti**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-209">Select **Review and create**.</span></span> <span data-ttu-id="aee1a-210">Kai diegimas bus baigtas, naujasis išteklius bus rodomas „Azure“ portale.</span><span class="sxs-lookup"><span data-stu-id="aee1a-210">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="aee1a-211">Pereikite į sukurtą saugyklos paskyrą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-211">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="aee1a-212">Kairiajame meniu pasirinkite **Prieigos raktai**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-212">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="aee1a-213">Nukopijuokite ir įrašykite **Key1** arba **Key2** jungimosi eilutę.</span><span class="sxs-lookup"><span data-stu-id="aee1a-213">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="aee1a-214">Nukopijuokite ir įrašykite saugyklos paskyros pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-214">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="aee1a-215">Naujos raktų saugyklos sukūrimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-215">Create a new key vault:</span></span>

    1. <span data-ttu-id="aee1a-216">[„Azure“ portale](https://portal.azure.com) sukurkite raktų saugyklą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-216">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="aee1a-217">Dialogo lango **Raktų saugyklos kūrimas** lauke **Vieta** pasirinkite duomenų centrą, kuriame yra jūsų aplinka.</span><span class="sxs-lookup"><span data-stu-id="aee1a-217">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="aee1a-218">Sukūrę raktų saugyklą, pasirinkite ją sąraše, tada pasirinkite **Slaptieji raktai**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-218">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="aee1a-219">Pasirinkite **Generuoti / importuoti**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-219">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="aee1a-220">Dialogo lango **Slaptojo rakto kūrimas** lauke **Nusiuntimo parinktys** pasirinkite **Neautomatinis**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-220">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="aee1a-221">Įveskite slaptojo rakto pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-221">Enter a name for the secret.</span></span> <span data-ttu-id="aee1a-222">Pasižymėkite pavadinimą, nes jį reikės pateikti vėliau.</span><span class="sxs-lookup"><span data-stu-id="aee1a-222">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="aee1a-223">Lauke **Reikšmė** įveskite jungimosi eilutę, kurią gavote iš saugyklos paskyros atlikdami ankstesnę procedūrą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-223">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="aee1a-224">Pasirinkite **Įjungta**, tada – **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-224">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="aee1a-225">Slaptasis raktas sukuriamas ir įtraukiamas į raktų saugyklą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-225">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="aee1a-226">Nueikite į sritį **Raktų saugyklos apžvalga** ir pasižymėkite DNS pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-226">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="aee1a-227">„Azure AD“ programos sukūrimas ir užregistravimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-227">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="aee1a-228">[„Azure“ portale](https://portal.azure.com) nueikite į **„Azure Active Directory“** ir pasirinkite **Programų registracijos**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-228">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="aee1a-229">Pasirinkite **Nauja programos registracija** ir nustatykite tolesnius laukus.</span><span class="sxs-lookup"><span data-stu-id="aee1a-229">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="aee1a-230">**Pavadinimas** – įveskite programos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-230">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="aee1a-231">**Programos tipas** – pasirinkite **Žiniatinklio API**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-231">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="aee1a-232">**Peradresavimo URI sąranka** – įveskite savo „Dynamics 365“ egzemplioriaus URL, pvz., `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="aee1a-232">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="aee1a-233">Nueikite į ką tik sukurtą programą ir nukopijuokite bei įrašykite jos elemento **Programos (kliento) ID** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aee1a-233">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="aee1a-234">Šią reikšmę reikės pateikti vėliau, kai nustatysite raktų saugyklą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-234">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="aee1a-235">Nueikite į sritį **API teisės** ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="aee1a-235">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="aee1a-236">Pasirinkite **Įtraukti teisę**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-236">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="aee1a-237">Pasirinkite **„Azure“ raktų saugykla**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-237">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="aee1a-238">Pasirinkę perduotąsias teises, pasirinkite **vartotojas\_apsimetimas**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-238">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="aee1a-239">Pasirinkite **Įtraukti teises**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-239">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="aee1a-240">Programos meniu pasirinkite **Sertifikatai ir slaptieji raktai**, tada atlikite tolesnius veiksmus, kad sukurtumėte raktų saugyklos slaptųjų raktų.</span><span class="sxs-lookup"><span data-stu-id="aee1a-240">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="aee1a-241">Pasirinkite **Naujas kliento slaptasis raktas**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-241">Select **New client secret**.</span></span>
        2. <span data-ttu-id="aee1a-242">Lauke **Rakto aprašas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-242">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="aee1a-243">Pasirinkite trukmę, tada – **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-243">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="aee1a-244">Slaptasis raktas sugeneruojamas lauke **Reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-244">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="aee1a-245">Nukopijuokite ir įrašykite slaptąjį raktą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-245">Copy and save the secret value.</span></span>

4. <span data-ttu-id="aee1a-246">Raktų saugyklos slaptųjų raktų kūrimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-246">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="aee1a-247">Pereikite į anksčiau sukurtą raktų saugyklą ir pasirinkite **Slaptieji raktai**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-247">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="aee1a-248">Su kiekvienu toliau pateiktoje lentelėje esančiu slaptojo rakto pavadinimu atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="aee1a-248">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="aee1a-249">Pasirinkite **Generuoti / importuoti**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-249">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="aee1a-250">Dialogo lango **Slaptojo rakto kūrimas** lauke **Nusiuntimo parinktys** pasirinkite **Neautomatinis**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-250">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="aee1a-251">Sukurkite slaptojo rakto pavadinimą ir reikšmę iš tolesnės lentelės.</span><span class="sxs-lookup"><span data-stu-id="aee1a-251">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="aee1a-252">Pasirinkite **Įjungta**, tada – **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-252">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="aee1a-253">Slaptasis raktas sukuriamas ir įtraukiamas į raktų saugyklą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-253">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="aee1a-254">Slaptas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-254">Secret name</span></span>                       | <span data-ttu-id="aee1a-255">Slaptojo rakto reikšmė</span><span class="sxs-lookup"><span data-stu-id="aee1a-255">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="aee1a-256">app-id</span><span class="sxs-lookup"><span data-stu-id="aee1a-256">app-id</span></span>                            | <span data-ttu-id="aee1a-257">Programos, kurią sukūrėte anksčiau, ID</span><span class="sxs-lookup"><span data-stu-id="aee1a-257">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="aee1a-258">app-secret</span><span class="sxs-lookup"><span data-stu-id="aee1a-258">app-secret</span></span>                        | <span data-ttu-id="aee1a-259">Kliento slaptasis raktas, kurį įrašėte anksčiau</span><span class="sxs-lookup"><span data-stu-id="aee1a-259">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="aee1a-260">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="aee1a-260">storage-account-name</span></span>              | <span data-ttu-id="aee1a-261">Saugyklos paskyros, kurią sukūrėte anksčiau, pavadinimas, pvz., **1saugyklospaskyra**</span><span class="sxs-lookup"><span data-stu-id="aee1a-261">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="aee1a-262">storage-account-connection-string</span><span class="sxs-lookup"><span data-stu-id="aee1a-262">storage-account-connection-string</span></span> | <span data-ttu-id="aee1a-263">Jungimosi eilutė, kurią nukopijavote iš saugyklos paskyros puslapio **Prieigos raktai**</span><span class="sxs-lookup"><span data-stu-id="aee1a-263">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="aee1a-264">Programos autorizavimas norint pasiekti raktų saugyklą</span><span class="sxs-lookup"><span data-stu-id="aee1a-264">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="aee1a-265">[„Azure“ portale](https://portal.azure.com) atidarykite raktų saugyklą, kurią sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="aee1a-265">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="aee1a-266">Pasirinkite prieigos strategijas.</span><span class="sxs-lookup"><span data-stu-id="aee1a-266">Select the access policies.</span></span>
    3. <span data-ttu-id="aee1a-267">Su kiekviena toliau pateiktoje lentelėje esančia programa atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="aee1a-267">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="aee1a-268">Pasirinkite **Įtraukti prieigos strategiją**, kad sukurtumėte prieigos strategiją.</span><span class="sxs-lookup"><span data-stu-id="aee1a-268">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="aee1a-269">Lauke **Slaptųjų raktų teisės** pasirinkite teises iš tolesnės lentelės.</span><span class="sxs-lookup"><span data-stu-id="aee1a-269">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="aee1a-270">Lauke **Pasirinkti pagrindinį pavadinimą** ieškokite rodomo programos pavadinimo iš tolesnės lentelės.</span><span class="sxs-lookup"><span data-stu-id="aee1a-270">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="aee1a-271">Pasirinkite **Pasirinkti**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-271">Select **Select**.</span></span>
        5. <span data-ttu-id="aee1a-272">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-272">Select **Add**.</span></span>
        6. <span data-ttu-id="aee1a-273">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-273">Select **Save**.</span></span>

        | <span data-ttu-id="aee1a-274">Prašymas</span><span class="sxs-lookup"><span data-stu-id="aee1a-274">Application</span></span>                                              | <span data-ttu-id="aee1a-275">Teisės</span><span class="sxs-lookup"><span data-stu-id="aee1a-275">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="aee1a-276">Naujos programos, kurią sukūrėte, rodomas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-276">The display name of the new application that you created</span></span> | <span data-ttu-id="aee1a-277">Get, List</span><span class="sxs-lookup"><span data-stu-id="aee1a-277">Get, List</span></span>   |
        | <span data-ttu-id="aee1a-278">**„Microsoft Dynamics ERP Microservices“**</span><span class="sxs-lookup"><span data-stu-id="aee1a-278">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="aee1a-279">Get, List</span><span class="sxs-lookup"><span data-stu-id="aee1a-279">Get, List</span></span>   |

6. <span data-ttu-id="aee1a-280">Vaidmenų priskyrimas, kad būtų galima pasiekti saugyklos paskyrą</span><span class="sxs-lookup"><span data-stu-id="aee1a-280">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="aee1a-281">[„Azure“ portale](https://portal.azure.com) atidarykite saugyklos paskyrą, kurią sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="aee1a-281">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="aee1a-282">Pasirinkite **Prieigos valdymas (IAM)**, tada – **Vaidmenų priskyrimai**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-282">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="aee1a-283">Pasirinkite **Įtraukti, įtraukti vaidmens priskyrimą**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-283">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="aee1a-284">Su kiekviena toliau pateiktoje lentelėje esančia programa atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="aee1a-284">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="aee1a-285">Iš tolesnės lentelės pasirinkite vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="aee1a-285">Select the role from the following table.</span></span>
        2. <span data-ttu-id="aee1a-286">Lauką **Kam priskirti prieigą** palikite nustatytą kaip **„Azure AD“ vartotojas, grupė arba pagrindinis tarnybos pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-286">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="aee1a-287">Lauke **Pasirinkti** įveskite programą iš tolesnės lentelės.</span><span class="sxs-lookup"><span data-stu-id="aee1a-287">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="aee1a-288">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-288">Select **Save**.</span></span>

        | <span data-ttu-id="aee1a-289">Prašymas</span><span class="sxs-lookup"><span data-stu-id="aee1a-289">Application</span></span>                                              | <span data-ttu-id="aee1a-290">Vaidmuo</span><span class="sxs-lookup"><span data-stu-id="aee1a-290">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="aee1a-291">Naujos programos, kurią sukūrėte, rodomas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-291">The display name of the new application that you created</span></span> | <span data-ttu-id="aee1a-292">Savininkas</span><span class="sxs-lookup"><span data-stu-id="aee1a-292">Owner</span></span>                       |
        | <span data-ttu-id="aee1a-293">Naujos programos, kurią sukūrėte, rodomas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-293">The display name of the new application that you created</span></span> | <span data-ttu-id="aee1a-294">Bendraautorius</span><span class="sxs-lookup"><span data-stu-id="aee1a-294">Contributor</span></span>                 |
        | <span data-ttu-id="aee1a-295">Naujos programos, kurią sukūrėte, rodomas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-295">The display name of the new application that you created</span></span> | <span data-ttu-id="aee1a-296">Saugyklos paskyros bendraautoris</span><span class="sxs-lookup"><span data-stu-id="aee1a-296">Storage Account Contributor</span></span> |
        | <span data-ttu-id="aee1a-297">Naujos programos, kurią sukūrėte, rodomas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-297">The display name of the new application that you created</span></span> | <span data-ttu-id="aee1a-298">Saugyklos didelių dvejetainių objektų duomenų savininkas</span><span class="sxs-lookup"><span data-stu-id="aee1a-298">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="aee1a-299">**„AI Builder“ autorizavimo tarnyba**</span><span class="sxs-lookup"><span data-stu-id="aee1a-299">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="aee1a-300">Saugyklos didelių dvejetainių objektų duomenų skaitytojas</span><span class="sxs-lookup"><span data-stu-id="aee1a-300">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="aee1a-301">„Azure“ CLI</span><span class="sxs-lookup"><span data-stu-id="aee1a-301">Azure CLI</span></span>](#tab/azure-azure-cli)

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

## <a name="configure-the-entity-store"></a><span data-ttu-id="aee1a-302">Objektų saugyklos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-302">Configure the entity store</span></span>

<span data-ttu-id="aee1a-303">Atlikite tolesnius veiksmus, kad nustatytumėte objektų saugyklą savo „Finance“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="aee1a-303">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="aee1a-304">Nueikite į **Sistemos administravimas \> Sąranka \> Sistemos parametrai \> Duomenų ryšiai**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-304">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="aee1a-305">Parinktį **Įjungti „Data Lake“ integraciją** nustatykite kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-305">Set the **Enable Data Lake integration** option to **Yes**.</span></span>
3. <span data-ttu-id="aee1a-306">Nustatykite tolesnius raktų saugyklos laukus.</span><span class="sxs-lookup"><span data-stu-id="aee1a-306">Set the following Key Vault fields:</span></span>

    - <span data-ttu-id="aee1a-307">**Programos (kliento) ID** – įveskite anksčiau sukurtą programos kliento ID.</span><span class="sxs-lookup"><span data-stu-id="aee1a-307">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="aee1a-308">**Programos slaptasis raktas** – įveskite slaptąjį raktą, kurį įrašėte anksčiau sukurtai programai.</span><span class="sxs-lookup"><span data-stu-id="aee1a-308">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="aee1a-309">**DNS pavadinimas** – domeno vardų sistemos (DNS) pavadinimą galite rasti programos, kurią sukūrėte anksčiau, išsamios informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="aee1a-309">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="aee1a-310">**Slaptojo rakto pavadinimas** – įveskite **storage-account-connection-string**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-310">**Secret name** – Enter **storage-account-connection-string**.</span></span>

## <a name="configure-the-data-lake"></a><span data-ttu-id="aee1a-311">Duomenų telkinio konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-311">Configure the data lake</span></span>

<span data-ttu-id="aee1a-312">Atlikite šiuos veiksmus, kad, naudodami LCS, įtrauktumėte „Azure Data Lake“ papildinį į aplinką.</span><span class="sxs-lookup"><span data-stu-id="aee1a-312">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="aee1a-313">Prisijunkite prie LCS, tada dešinėje puslapio pusėje, prie aplinkos pavadinimo pasirinkite **Išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-313">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="aee1a-314">Skyriuje **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-314">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="aee1a-315">Pasirinkite papildinį **Eksportavimas į „Data Lake“**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-315">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="aee1a-316">Įveskite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="aee1a-316">Enter the following values.</span></span>

    | <span data-ttu-id="aee1a-317">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="aee1a-317">Value</span></span>                                                              | <span data-ttu-id="aee1a-318">aprašymas</span><span class="sxs-lookup"><span data-stu-id="aee1a-318">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="aee1a-319">„Azure“ prenumeratos nuomotojo ID, nurodantį raktų saugyklos vietą</span><span class="sxs-lookup"><span data-stu-id="aee1a-319">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="aee1a-320">Nuomotojo ID, nurodantį saugyklos paskyros, programų ir raktų saugyklų vietą.</span><span class="sxs-lookup"><span data-stu-id="aee1a-320">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="aee1a-321">Norėdami rasti šią reikšmę, atidarykite [„Azure“ portalą](https://portal.azure.com), nueikite į **„Azure Active Directory“** ir nukopijuokite elemento **Nuomotojo ID** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aee1a-321">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="aee1a-322">Pateikite savo „Key Vault“ DNS pavadinimą</span><span class="sxs-lookup"><span data-stu-id="aee1a-322">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="aee1a-323">Raktų saugyklos DNS pavadinimas, pvz., `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="aee1a-323">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="aee1a-324">(Ši reikšmė atitinka DNS pavadinimą, kuris naudojamas objektų saugykloje.)</span><span class="sxs-lookup"><span data-stu-id="aee1a-324">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="aee1a-325">Pateikite slaptąjį raktą, kurį sudaro saugyklos paskyros pavadinimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-325">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="aee1a-326">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="aee1a-326">**storage-account-name**</span></span> |
    | <span data-ttu-id="aee1a-327">Programos ID, kuris bus naudojamas „Data Lake“ pasiekti, slaptas pavadinimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-327">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="aee1a-328">**app-id**</span><span class="sxs-lookup"><span data-stu-id="aee1a-328">**app-id**</span></span> |
    | <span data-ttu-id="aee1a-329">Slaptas pavadinimas, kuris bus naudojamas su programos ID</span><span class="sxs-lookup"><span data-stu-id="aee1a-329">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="aee1a-330">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="aee1a-330">**app-secret**</span></span> |

5. <span data-ttu-id="aee1a-331">Sutikite su sąlygomis ir pasirinkite **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-331">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="aee1a-332">Papildinys bus įdiegtas per kelias minutes.</span><span class="sxs-lookup"><span data-stu-id="aee1a-332">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="aee1a-333">„AI Builder“ konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-333">Configure AI Builder</span></span>

1. <span data-ttu-id="aee1a-334">Prisijunkite prie LCS ir atidarykite puslapį **Aplinkos informacija**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-334">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="aee1a-335">Slinkite iki dalies **Aplinkos papildiniai**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-335">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="aee1a-336">Turėtumėte matyti šioje aplinkoje jau įdiegtus papildinius.</span><span class="sxs-lookup"><span data-stu-id="aee1a-336">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="aee1a-337">Jei papildinio **Eksportavimas į „Data Lake“** tarp jų nėra, šį papildinį sukonfigūruokite.</span><span class="sxs-lookup"><span data-stu-id="aee1a-337">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="aee1a-338">Pasirinkite papildinį **Įžvalgų gavimas**.</span><span class="sxs-lookup"><span data-stu-id="aee1a-338">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="aee1a-339">Papildinio **Įžvalgų gavimas** informacijos puslapyje įveskite tolesnes reikšmes.</span><span class="sxs-lookup"><span data-stu-id="aee1a-339">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="aee1a-340">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="aee1a-340">Value</span></span>                                                    | <span data-ttu-id="aee1a-341">aprašymas</span><span class="sxs-lookup"><span data-stu-id="aee1a-341">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="aee1a-342">CDS organizacijos URL</span><span class="sxs-lookup"><span data-stu-id="aee1a-342">CDS Organization URL</span></span>                                     | <span data-ttu-id="aee1a-343">„Dataverse“ egzemplioriaus „Dataverse“ organizacijos URL.</span><span class="sxs-lookup"><span data-stu-id="aee1a-343">The Dataverse organization URL of the Dataverse instance.</span></span> <span data-ttu-id="aee1a-344">Norėdami rasti šią reikšmę, atidarykite [„Power Apps“ portalą](https://make.powerapps.com), pasirinkite mygtuką **Parametrai** (krumpliaračio simbolis) viršutiniame dešiniajame kampe, pasirinkite **Išplėstiniai parametrai** ir nukopijuokite URL.</span><span class="sxs-lookup"><span data-stu-id="aee1a-344">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Advanced settings**, and copy the URL.</span></span> <span data-ttu-id="aee1a-345">(URL baigiasi „dynamics.com.“)</span><span class="sxs-lookup"><span data-stu-id="aee1a-345">(The URL ends with "dynamics.com.")</span></span> |
    | <span data-ttu-id="aee1a-346">CDS org. ID</span><span class="sxs-lookup"><span data-stu-id="aee1a-346">CDS Org ID</span></span>                                               | <span data-ttu-id="aee1a-347">„Dataverse“ egzemplioriaus aplinkos ID.</span><span class="sxs-lookup"><span data-stu-id="aee1a-347">The environment ID of the Dataverse instance.</span></span> <span data-ttu-id="aee1a-348">Norėdami rasti šią reikšmę, atidarykite [„Power Apps“ portalą](https://make.powerapps.com), pasirinkite mygtuką **Parametrai** (krumpliaračio simbolis) viršutiniame dešiniajame kampe, pasirinkite **Tinkinimai \> Kūrėjo ištekliai \> Egzemplioriaus nurodos informacija** ir nukopijuokite **ID** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aee1a-348">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Customizations \> Developer resources \> Instance Reference Information**, and copy the **ID** value.</span></span> |
    | <span data-ttu-id="aee1a-349">CDS nuomotojo ID (katalogo ID iš AAD)</span><span class="sxs-lookup"><span data-stu-id="aee1a-349">CDS Tenant ID (Directory ID from AAD)</span></span>               | <span data-ttu-id="aee1a-350">„Dataverse“ egzemplioriaus nuomotojo ID.</span><span class="sxs-lookup"><span data-stu-id="aee1a-350">The tenant ID of the Dataverse instance.</span></span> <span data-ttu-id="aee1a-351">Norėdami rasti šią reikšmę, atidarykite [„Azure“ portalą](https://portal.azure.com), nueikite į **„Azure Active Directory“** ir nukopijuokite elemento **Nuomotojo ID** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aee1a-351">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="aee1a-352">Pateikite sistemos administratoriaus vaidmenį turinčio vartotojo objekto ID</span><span class="sxs-lookup"><span data-stu-id="aee1a-352">Provide user object ID who has system administrator role</span></span> | <span data-ttu-id="aee1a-353">Vartotojo „Azure AD“ objekto ID tarnyboje „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="aee1a-353">The Azure AD user object ID of the user in Dataverse.</span></span> <span data-ttu-id="aee1a-354">Šis vartotojas turi būti „Dataverse“ egzemplioriaus sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="aee1a-354">This user must be a system administrator of the Dataverse instance.</span></span> <span data-ttu-id="aee1a-355">Norėdami rasti šią reikšmę, atidarykite [„Azure“ portalą](https://portal.azure.com), nueikite į **„Azure Active Directory“ \> Vartotojai**, pasirinkite vartotoją, tada dalyje **Tapatybė** nukopijuokite elemento **Objekto ID** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aee1a-355">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory \> Users**, select the user, and then, in the **Identity** section, copy the **Object ID** value.</span></span> |
    | <span data-ttu-id="aee1a-356">Ar tai numatytoji nuomotojo CDS aplinka?</span><span class="sxs-lookup"><span data-stu-id="aee1a-356">Is this the default CDS environment for the tenant?</span></span>      | <span data-ttu-id="aee1a-357">Jei „Dataverse“ egzempliorius buvo pirmas sukurtas gamybos egzempliorius, pažymėkite šį žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="aee1a-357">If the Dataverse instance was the first production instance that was created, select this check box.</span></span> <span data-ttu-id="aee1a-358">Jei „Dataverse“ egzempliorius buvo sukurtas neautomatiniu būdu, išvalykite šį žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="aee1a-358">If the Dataverse instance was manually created, clear this check box.</span></span> |

## <a name="feedback-and-support"></a><span data-ttu-id="aee1a-359">Atsiliepimai ir palaikymas</span><span class="sxs-lookup"><span data-stu-id="aee1a-359">Feedback and support</span></span>

<span data-ttu-id="aee1a-360">Jei norite pateikti atsiliepimų ar reikia pagalbos, atsiųskite el. laišką [kliento mokėjimo įžvalgų (peržiūros versija)](mailto:fiap@microsoft.com) el. pašto adresu.</span><span class="sxs-lookup"><span data-stu-id="aee1a-360">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="aee1a-361">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="aee1a-361">Privacy notice</span></span>

<span data-ttu-id="aee1a-362">Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.</span><span class="sxs-lookup"><span data-stu-id="aee1a-362">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]