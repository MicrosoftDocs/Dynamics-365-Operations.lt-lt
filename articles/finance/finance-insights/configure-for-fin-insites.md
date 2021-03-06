---
title: „Finance Insights” konfigūracija - versijos iki 10.0.19
description: Šioje temoje paaiškinami konfigūravimo veiksmai, kuriuos jums atlikus sistema galės naudotis modulio „Finance Insights” galimybėmis versijoms iki 10.0.19.
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
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 6ad06bb6d041fc060b3a99538f6d4d0af333180f
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186425"
---
# <a name="configuration-for-finance-insights-preview"></a>Modulio „Finance Insights” konfigūracija (peržiūros versija)

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Šios „Finance insights“ nustatymo procedūros galioja iki „Microsoft Dynamics 365 Finance“ 10.0.19 versijoms iki 10.0.19. Norėdami nustatyti „Finance insights“ apie 10.0.20 ir vėlesnę versiją,[žr. „Finance Insights“ konfigūracijos (peržiūra) – 10.0.20 ir vėlesnės versijos](configure-for-fin-insites-PubPrvw.md).

Modulyje „Finance Insights” sujungiamos „Microsoft Dynamics 365 Finance“ ir „Microsoft Dataverse“, „Azure“ bei „AI Builder“ funkcijos, kad jūsų organizacijai būtų suteikiami galingi prognozavimo įrankiai. Šioje temoje paaiškinami konfigūravimo veiksmai, kuriuos jums atlikus sistema galės naudotis modulio „Finance Insights” galimybėmis.

## <a name="deploy-dynamics-365-finance"></a>„Dynamics 365 Finance“ diegimas

Aplinkas galite įdiegti atlikdami toliau pateikiamus veiksmus.

1. Portale „Microsoft Dynamics Lifecycle Services“ (LCS) sukurkite arba atnaujinkite „Dynamics 365 Finance“ aplinką. Aplinkai reikalinga programos 10.0.11 versija / 35 arba naujesnis platformos atnaujinimas.
2. Aplinka turi būti didelio pasiekiamumo (HA) smėlio dėžės aplinka. (Šis aplinkos tipas dar vadinamas 2 pakopos aplinka.) Norėdami gauti daugiau informacijos, žr. [Aplinkos planavimas](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. Jei konfigūruojate „Finance Insights“ smėlio dėžės aplinkoje, jums gali tekti nukopijuoti gamybos duomenis į tą aplinką numatymams dirbti. Numatymo modelis naudoja kelių metų duomenis numatymams sukurti. „Contoso“ demonstruojamuose duomenyse nėra pakankamai praeities duomenų, kad būtų galima nuspėti numatymo modelį. 

## <a name="configure-dataverse"></a>Konfigūruoti „Dataverse“

Norėdami sukonfigūruoti „Finance insights“, „Dataverse“ atlikite nurodytus veiksmus.

1. Atidarykite aplinkos puslapį LCS ir patikrinkite, ar **„Power Platform“** integravimo skyrius jau sąranka.
    1. Jei jis jau nustatytas, turi „Dataverse“ būti pateiktas su aplinka susietas aplinkos „Dynamics 365 Finance“ pavadinimas. Nukopijuokite „Dataverse“ aplinkos pavadinimą.
    2. Jei ji nėra nustatyta, atlikite šiuos veiksmus:
        1. Integravimo **skyriuje** pasirinkite „Power Platform“ nustatymo mygtuką. Tam, kad būtų galima nustatyti aplinką, gali užtrukti iki valandos.
        2. „Dataverse“ aplinka sėkmingai nustatyta „Dataverse“ aplinkos pavadinimas susietas su „Dynamics 365 Finance“ aplinka turi būti įvardytas. Nukopijuokite „Dataverse“ aplinkos pavadinimą.
> [!NOTE]
> Nustatę aplinką, **nepasirinkite** mygtuko **Programų CDS** saito. Tai nėra būtina „Finance insights“ ir bus išjungta galimybė užbaigti reikiamus LCS aplinkos papildiniai.

2. Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com/) ir atlikite tolesnius veiksmus, kad sukurtumėte naują „Dataverse“ aplinką tame pačiame „Active Directory“ nuomotojuje.

    1. Atidarykite puslapį **Aplinkos**.

        [![Puslapis Aplinkos](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)

    2. Pasirinkite „Dataverse“ prieš tai sukurtą aplinką ir tada rinkitės **Parametrai**.
    3. Pasirinkite **Ištekliai \> Visi senstelėję parametrai**.
    4. Viršutinėje naršymo juostoje pasirinkite **Parametrai**, tada – **Tinkinimai**.
    5. Pasirinkite **Kūrėjo ištekliai**.
    6. Nukopijuokite **„Dataverse” organizacijos ID** reikšmę.
    7. Naršyklės adreso juostoje pasižymėkite „Dataverse“ organizacijos URL. Pavyzdžiui, URL gali būti `https://org42b2b3d3.crm.dynamics.com`.

3. Jei planuojate naudoti grynųjų pinigų srauto prognozių arba biudžeto prognozių funkciją, atlikite tolesnius veiksmus, kad atnaujintumėte savo organizacijos komentavimo limitą bent iki 50 megabaitų (MB).

    1. Atidarykite [„Power Apps“ portalą](https://make.powerapps.com).
    2. Pasirinkite aplinką, kurią ką tik sukūrėte, tada pasirinkite **Išplėstiniai parametrai**.
    3. Pasirinkite **Parametrai \> El. pašto konfigūravimas**.
    4. Pakeiskite lauko **Didžiausias failo dydis** reikšmę į **51 200**. (Reikšmė išreikšta kilobaitais \[KB\].)
    5. Pasirinkite **Gerai**, kad įrašytumėte keitimus.

## <a name="configure-the-azure-setup"></a>„Azure“ sąrankos konfigūravimas

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a>„Dataverse“ katalogo ID ir vartotojo „Azure AD“ objekto ID įvedimas

1. Įveskite „Dataverse“ katalogo ID.

    1. Atidarykite [„Azure“ portalą](https://portal.azure.com).
    2. Prisijunkite naudodami vartotojo ID, kuris buvo naudojamas kuriant „Dataverse“ aplinką.
    3. Eikite į **Azure Active Directory**.
    4. Nukopijuokite elemento **Nuomotojo ID** reikšmę.

2. Įveskite vartotojo „Azure Active Directory“ („Azure AD“) objekto ID.

    1. [„Azure“ portale](https://portal.azure.com) eikite į **Vartotojai** ir ieškokite vartotojo pagal el. pašto adresą.
    2. Pasirinkite vartotojo vardą.
    3. Nukopijuokite elemento **Objekto ID** reikšmę.

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>„Azure Cloud Shell“ naudojimas modulio „Finance Insights” „Data Lake“ ištekliams nustatyti

# <a name="use-a-windows-powershell-script"></a>[„Windows PowerShell“ scenarijaus naudojimas](#tab/use-a-powershell-script)

Pateiktas „Windows PowerShell“ scenarijus, kad būtų galima lengvai nustatyti „Azure“ išteklius, aprašytus temoje [Eksportavimo į „Azure Data Lake“ konfigūravimas](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md). Jei norite nustatyti neautomatiniu būdu, praleiskite šią procedūrą ir vykdykite procedūrą, aprašytą skyriuje [Neautomatinė sąranka](#manual-setup).

> [!NOTE]
> Atlikite tolesnius veiksmus, kad būtų vykdomas „PowerShell“ scenarijus. „Azure“ CLI parinktis „Išbandykite“ arba scenarijaus vykdymas jūsų kompiuteryje gali neveikti.

Atlikite šiuos veiksmus, kad sukonfigūruotumėte „Azure“ naudodami „Windows PowerShell“ scenarijų. Turite turėti teises sukurti „Azure“ išteklių grupę, „Azure“ išteklius ir „Azure AD“ programą. Norėdami gauti informacijos apie reikiamas teises, žr. [„Azure AD“ teisių patikrinimas](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. [„Azure“ portale](https://portal.azure.com) eikite į savo tikslinę „Azure“ prenumeratą. Pasirinkite mygtuką **„Cloud Shell“**, esantį lauko **Ieška** dešinėje.
2. Pasirinkite **„PowerShell“**.
3. Sukurkite saugyklą, jei būsite paraginti tai padaryti.
4. Eikite į skirtuką **„Azure“** ir pasirinkite **Kopijuoti**.  
5. Atidarykite „Notepad“ ir įklijuokite „PowerShell" scenarijų. Įrašykite failą kaip ConfigureDataLake.ps1.
6. Į seansą įkelkite „Windows PowerShell" scenarijų naudodami nusiuntimo į „Cloud Shell“ meniu parinktį.
7. Paleiskite scenarijų .\ConfigureDataLake.ps1.
8. Vykdykite raginimus paleisti scenarijų.
9. Naudokite scenarijaus pateikiamą informaciją, kad į LCS įdiegtumėte papildinį **Eksportavimas į „Data Lake“**.
10. Naudokite scenarijaus pateikiamą informaciją, kad „Finance“ puslapyje **Duomenų ryšiai** įjungtumėte objektų saugyklą (**Sistemos administravimas \> Sistemos parametrai \> Duomenų ryšiai**).

### <a name="manual-setup"></a>Neautomatinė sąranka

#### <a name="add-applications-to-the-azure-ad-tenant"></a>Programų įtraukimas į „Azure AD“ nuomotoją

1. [„Azure“ portale](https://portal.azure.com) nueikite į **„Azure Active Directory“**.
2. Pasirinkite **Tvarkyti \> Įmonės programos**.
3. Ieškokite tolesnių programų pagal programos ID.

    | Prašymas                              | Programos ID                               |
    |------------------------------------------|--------------------------------------|
    | „Microsoft Dynamics ERP Microservices“     | „0cdb527f-a8d1-4bf8-9436-b352c68682b2“ |
    | „Microsoft Dynamics ERP Microservices CDS“ | „703e2651-d3fc-48f5-942c-74274233dba8“ |
    | „AI Builder“ autorizavimo tarnyba         | „ad40333e-9910-4b61-b281-e3aeeb8c3ef3“ |

Jeigu negalite rasti nė vienos iš ankstesnių programų, bandykite atlikti tolesnius veiksmus.

1. Vietiniame kompiuteryje pasirinkite meniu **Pradėti** ir ieškokite **powershell**.
2. Pasirinkite ir laikykite (arba dešiniuoju pelės mygtuku spustelėkite) **„Windows PowerShell“**, tada pasirinkite **Paleisti administratoriaus teisėmis**.
3. Vykdykite tolesnę komandą, kad įdiegtumėte **„AzureAD“** modulį.

    `Install-Module -Name AzureAD`

4. Jei reikalaujama „NuGet“ teikėjo, kad galėtumėte tęsti, pasirinkite **Y**, kad jį įdiegtumėte.
5. Jei pasirodo pranešimas „Nepatikima saugykla“, norėdami tęsti pasirinkite **Y**.
6. Kiekvienai programai, kuri turi būti įtraukta, vykdykite toliau nurodytas komandas, kad įtrauktumėte programą į „Azure AD“. Kai būsite paraginti, prisijunkite kaip „Azure AD“ administratorius.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>„Azure“ išteklių kūrimas

> [!NOTE]
> Įsitikinkite, kad sukūrėte tolesnius išteklius tame pačiame „Azure AD“ egzemplioriuje, kaip „Dataverse“ aplinka. Negalite naudoti išteklių iš kito „Azure AD“ egzemplioriaus.

1. Naujos saugyklos paskyros kūrimas

    1. [„Azure“ portale](https://portal.azure.com) sukurkite saugyklos paskyrą.
    2. Dialogo lange **Saugyklos paskyros kūrimas** nustatykite tolesnius laukus.

        - **Vieta** – pasirinkite duomenų centrą, kuriame yra jūsų aplinka.
        - **Našumas** – rekomenduojame pasirinkti **Standartinis**.
        - **Paskyros rūšis** – turite pasirinkti **StorageV2**.

    3. Dialogo lange **Išplėstinės parinktys**, prie parinkties **„Data Lake Storage Gen2“** (funkcija **Hierarchinės vardų sritys**) pasirinkite **Įjungti**. Jei šią funkciją išjungsite, negalėsite naudoti duomenų, kuriuos „Finance and Operations“ programos rašo naudodamos tokias tarnybas, kaip „Power BI“ duomenų srautai.
    4. Pasirinkite **Peržiūrėti ir kurti**. Kai diegimas bus baigtas, naujasis išteklius bus rodomas „Azure“ portale.
    5. Pereikite į sukurtą saugyklos paskyrą.
    6. Kairiajame meniu pasirinkite **Prieigos raktai**.
    7. Nukopijuokite ir įrašykite **Key1** arba **Key2** jungimosi eilutę.
    8. Nukopijuokite ir įrašykite saugyklos paskyros pavadinimą.

2. Naujos raktų saugyklos sukūrimas

    1. [„Azure“ portale](https://portal.azure.com) sukurkite raktų saugyklą.
    2. Dialogo lango **Raktų saugyklos kūrimas** lauke **Vieta** pasirinkite duomenų centrą, kuriame yra jūsų aplinka.
    3. Sukūrę raktų saugyklą, pasirinkite ją sąraše, tada pasirinkite **Slaptieji raktai**.
    4. Pasirinkite **Generuoti / importuoti**.
    5. Dialogo lango **Slaptojo rakto kūrimas** lauke **Nusiuntimo parinktys** pasirinkite **Neautomatinis**.
    6. Įveskite slaptojo rakto pavadinimą. Pasižymėkite pavadinimą, nes jį reikės pateikti vėliau.
    7. Lauke **Reikšmė** įveskite jungimosi eilutę, kurią gavote iš saugyklos paskyros atlikdami ankstesnę procedūrą.
    8. Pasirinkite **Įjungta**, tada – **Kurti**. Slaptasis raktas sukuriamas ir įtraukiamas į raktų saugyklą.
    9. Nueikite į sritį **Raktų saugyklos apžvalga** ir pasižymėkite DNS pavadinimą.

3. „Azure AD“ programos sukūrimas ir užregistravimas

    1. [„Azure“ portale](https://portal.azure.com) nueikite į **„Azure Active Directory“** ir pasirinkite **Programų registracijos**.
    2. Pasirinkite **Nauja programos registracija** ir nustatykite tolesnius laukus.

        - **Pavadinimas** – įveskite programos pavadinimą.
        - **Programos tipas** – pasirinkite **Žiniatinklio API**.
        - **Peradresavimo URI sąranka** – įveskite savo „Dynamics 365“ egzemplioriaus URL, pvz., `https://yourdynamicsinstance.dynamics.com/auth`.

    3. Nueikite į ką tik sukurtą programą ir nukopijuokite bei įrašykite jos elemento **Programos (kliento) ID** reikšmę. Šią reikšmę reikės pateikti vėliau, kai nustatysite raktų saugyklą.
    4. Nueikite į sritį **API teisės** ir atlikite tolesnius veiksmus.

        1. Pasirinkite **Įtraukti teisę**.
        2. Pasirinkite **„Azure“ raktų saugykla**.
        3. Pasirinkę perduotąsias teises, pasirinkite **vartotojas\_apsimetimas**.
        4. Pasirinkite **Įtraukti teises**.

    5. Programos meniu pasirinkite **Sertifikatai \& slaptieji raktai**, tada atlikite tolesnius veiksmus, kad sukurtumėte raktų saugyklos slaptųjų raktų.

        1. Pasirinkite **Naujas kliento slaptasis raktas**.
        2. Lauke **Rakto aprašas** įveskite pavadinimą.
        3. Pasirinkite trukmę, tada – **Įtraukti**. Slaptasis raktas sugeneruojamas lauke **Reikšmė**.
        4. Nukopijuokite ir įrašykite slaptąjį raktą.

4. Raktų saugyklos slaptųjų raktų kūrimas

    1. Pereikite į anksčiau sukurtą raktų saugyklą ir pasirinkite **Slaptieji raktai**.
    2. Su kiekvienu toliau pateiktoje lentelėje esančiu slaptojo rakto pavadinimu atlikite tolesnius veiksmus.

        1. Pasirinkite **Generuoti / importuoti**.
        2. Dialogo lango **Slaptojo rakto kūrimas** lauke **Nusiuntimo parinktys** pasirinkite **Neautomatinis**.
        3. Sukurkite slaptojo rakto pavadinimą ir reikšmę iš tolesnės lentelės.
        4. Pasirinkite **Įjungta**, tada – **Kurti**. Slaptasis raktas sukuriamas ir įtraukiamas į raktų saugyklą.

        | Slaptas pavadinimas                       | Slaptojo rakto reikšmė                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | app-id                            | Programos, kurią sukūrėte anksčiau, ID                                      |
        | app-secret                        | Kliento slaptasis raktas, kurį įrašėte anksčiau                                                    |
        | storage-account-name              | Saugyklos paskyros, kurią sukūrėte anksčiau, pavadinimas, pvz., **1saugyklospaskyra**       |
        | storage-account-connection-string | Jungimosi eilutė, kurią nukopijavote iš saugyklos paskyros puslapio **Prieigos raktai** |

5. Programos autorizavimas norint pasiekti raktų saugyklą

    1. [„Azure“ portale](https://portal.azure.com) atidarykite raktų saugyklą, kurią sukūrėte anksčiau.
    2. Pasirinkite prieigos strategijas.
    3. Su kiekviena toliau pateiktoje lentelėje esančia programa atlikite tolesnius veiksmus.

        1. Pasirinkite **Įtraukti prieigos strategiją**, kad sukurtumėte prieigos strategiją.
        2. Lauke **Slaptųjų raktų teisės** pasirinkite teises iš tolesnės lentelės.
        3. Lauke **Pasirinkti pagrindinį pavadinimą** ieškokite rodomo programos pavadinimo iš tolesnės lentelės.
        4. Pasirinkite **Pasirinkti**.
        5. Pasirinkite **Įtraukti**.
        6. Pasirinkite **Įrašyti**.

        | Prašymas                                              | Teisės |
        |----------------------------------------------------------|-------------|
        | Naujos programos, kurią sukūrėte, rodomas pavadinimas | Get, List   |
        | **„Microsoft Dynamics ERP Microservices“**                 | Get, List   |

6. Vaidmenų priskyrimas, kad būtų galima pasiekti saugyklos paskyrą

    1. [„Azure“ portale](https://portal.azure.com) atidarykite saugyklos paskyrą, kurią sukūrėte anksčiau.
    2. Pasirinkite **Prieigos valdymas (IAM)**, tada – **Vaidmenų priskyrimai**.
    3. Pasirinkite **Įtraukti, įtraukti vaidmens priskyrimą**.
    4. Su kiekviena toliau pateiktoje lentelėje esančia programa atlikite tolesnius veiksmus.

        1. Iš tolesnės lentelės pasirinkite vaidmenį.
        2. Lauką **Kam priskirti prieigą** palikite nustatytą kaip **„Azure AD“ vartotojas, grupė arba pagrindinis tarnybos pavadinimas**.
        3. Lauke **Pasirinkti** įveskite programą iš tolesnės lentelės.
        4. Pasirinkite **Įrašyti**.

        | Prašymas                                              | Vaidmuo                        |
        |----------------------------------------------------------|-----------------------------|
        | Naujos programos, kurią sukūrėte, rodomas pavadinimas | Savininkas                       |
        | Naujos programos, kurią sukūrėte, rodomas pavadinimas | Bendraautorius                 |
        | Naujos programos, kurią sukūrėte, rodomas pavadinimas | Saugyklos paskyros bendraautoris |
        | Naujos programos, kurią sukūrėte, rodomas pavadinimas | Saugyklos didelių dvejetainių objektų duomenų savininkas     |
        | **„AI Builder“ autorizavimo tarnyba**                     | Saugyklos didelių dvejetainių objektų duomenų skaitytojas    |

# <a name="azure-cli"></a>[„Azure“ CLI](#tab/azure-azure-cli)

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



## <a name="configure-the-data-lake"></a>Duomenų telkinio konfigūravimas

Atlikite šiuos veiksmus, kad, naudodami LCS, įtrauktumėte „Azure Data Lake“ papildinį į aplinką.

1. Prisijunkite prie LCS, tada dešinėje puslapio pusėje, prie aplinkos pavadinimo pasirinkite **Išsami informacija**.
2. Skyriuje **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.
3. Pasirinkite papildinį **Eksportavimas į „Data Lake“**.
4. Įveskite toliau nurodytas reikšmes.

    | Reikšmė                                                              | aprašymas |
    |--------------------------------------------------------------------|-------------|
    | „Azure“ prenumeratos nuomotojo ID, nurodantį raktų saugyklos vietą | Nuomotojo ID, nurodantį saugyklos paskyros, programų ir raktų saugyklų vietą. Norėdami rasti šią reikšmę, atidarykite [„Azure“ portalą](https://portal.azure.com), nueikite į **„Azure Active Directory“** ir nukopijuokite elemento **Nuomotojo ID** reikšmę. |
    | Pateikite savo „Key Vault“ DNS pavadinimą                             | Raktų saugyklos DNS pavadinimas, pvz., `https://customkeyvault.vault.azure.net/`. (Ši reikšmė atitinka DNS pavadinimą, kuris naudojamas objektų saugykloje.) |
    | Pateikite slaptąjį raktą, kurį sudaro saugyklos paskyros pavadinimas   | **storage-account-name** |
    | Programos ID, kuris bus naudojamas „Data Lake“ pasiekti, slaptas pavadinimas          | **app-id** |
    | Slaptas pavadinimas, kuris bus naudojamas su programos ID                                 | **app-secret** |

5. Sutikite su sąlygomis ir pasirinkite **Diegti**.

Papildinys bus įdiegtas per kelias minutes.

## <a name="configure-ai-builder"></a>„AI Builder“ konfigūravimas

1. Prisijunkite prie LCS ir atidarykite puslapį **Aplinkos informacija**.
2. Slinkite iki dalies **Aplinkos papildiniai**. Turėtumėte matyti šioje aplinkoje jau įdiegtus papildinius. Jei papildinio **Eksportavimas į „Data Lake“** tarp jų nėra, šį papildinį sukonfigūruokite.
3. Pasirinkite papildinį **Įžvalgų gavimas**.
4. Papildinio **Įžvalgų gavimas** informacijos puslapyje įveskite tolesnes reikšmes.

    | Reikšmė                                                    | Aprašas |
    |----------------------------------------------------------|-------------|
    | CDS organizacijos URL                                     | Organizacijos „Dataverse“ URL nukopijuotas iš aukščiau. |
    | CDS org. ID                                               | Organizacijos „Dataverse“ ID nukopijuotas iš aukščiau. |
5. įjunkite **Ar tai numatytoji nuomotojo aplinka**.
    
## <a name="configure-the-entity-store"></a>Objektų saugyklos konfigūravimas

Atlikite tolesnius veiksmus, kad nustatytumėte objektų saugyklą savo „Finance“ aplinkoje.

1. Nueikite į **Sistemos administravimas \> Sąranka \> Sistemos parametrai \> Duomenų ryšiai**.
2. Nustatykite šiuos raktų saugyklos laukus:

    - **Programos (kliento) ID** – įveskite anksčiau sukurtą programos kliento ID.
    - **Programos slaptasis raktas** – įveskite slaptąjį raktą, kurį įrašėte anksčiau sukurtai programai.
    - **DNS pavadinimas** – domeno vardų sistemos (DNS) pavadinimą galite rasti programos, kurią sukūrėte anksčiau, išsamios informacijos puslapyje.
    - **Slaptojo rakto pavadinimas** – įveskite **storage-account-connection-string**.
3. Įjunkite **Įjungti „Data Lake“ integraciją**.
4. Pasirinkite **Tikrinti „Azure Key Vault"** ir patikrinkite, ar nėra klaidų.
5. Pasirinkite **Tikrinti „Azure" talpyklą** ir patikrinkite, ar nėra klaidų.

## <a name="feedback-and-support"></a>Atsiliepimai ir palaikymas

Jei norite pateikti atsiliepimų ar reikia pagalbos, atsiųskite el. laišką [kliento mokėjimo įžvalgų (peržiūros versija)](mailto:fiap@microsoft.com) el. pašto adresu.

## <a name="privacy-notice"></a>Privatumo pranešimas

Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
