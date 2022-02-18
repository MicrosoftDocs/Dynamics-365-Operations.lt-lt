---
title: Briaunos skalės vienetų diegimas pasirinktinėje aparatūroje naudojant LBD
description: Šioje temoje paaiškinama, kaip parengti vietinės briaunos svarstyklių vienetus naudojant pasirinktinę aparatūrą ir diegimą, pagrįstą vietinės verslo duomenimis (LBD).
author: cabeln
ms.date: 01/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 1204b65e76c107c29a94a61c321064a87c7571fb
ms.sourcegitcommit: 948978183a1da949e35585b28b8e85a63b6c12b1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/25/2022
ms.locfileid: "8024547"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd"></a>Briaunos skalės vienetų diegimas pasirinktinėje aparatūroje naudojant LBD

[!include [banner](../includes/banner.md)]

Kraštų skalės vienetai atlieka svarbus vaidmenį paskirstytoje tiekimo grandinės valdymo ir kokybės topologijoje. Topologijoje galite paskirstyti darbo krūvius savo „Supply Chain Management“ cloud centre ir papildomiems skalės vienetams debesyje arba ant krašto.

Kraštų skalės vienetus galima įdiegti sukuriant vietinę verslo duomenų (LBD) aplinką ir sukonfigūruojant [šią aplinką, kad](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) ji veiktų kaip skalės vienetas jūsų paskirstytoje „supply chain management“ topologijoje. Tai pasiekiama susieant vietinę LBD aplinką su „Supply Chain Management“ aplinka debesyje, kuri sukonfigūruota veikti kaip centras.  

Šioje temoje aprašoma, kaip nustatyti vietinę LBD aplinką kaip kraštų skalės vienetą ir susieti ją su centru.

## <a name="infrastructure-considerations"></a>Infrastruktūros svarstymai

Krašto masto įrenginiai veikia vietinėje aplinkoje, todėl infrastruktūros reikalavimai yra gana panašūs. Tačiau yra tam tikrų skirtumų, į kuriuos reikėtų atkreipti dėmesį:

- Krašto masto vienetai nenaudoja finansinės atskaitomybės, todėl jiems nereikia finansinės atskaitomybės mazgų.
- Gamybos ir sandėliavimo darbo krūviai nėra daug skaičiuojami, todėl pagalvokite apie AOS mazgų skaičiavimo galios dydį.

## <a name="deployment-overview"></a>Talpinimo apžvalga

Toliau pateikta talpinimo veiksmų apžvalga.

1. **Įjunkite savo LBD projekto ciklo tarnybose „Microsoft Dynamics Lifecycle Services“ (LCS).**

1. **Nustatykite ir įdiekite LBD aplinką su tuščia *duomenų* baze.**

    Norėdami įdiegti LBD aplinką su naujausia topologija ir tuščia duomenų baze, naudokite LCS. Norėdami gauti daugiau informacijos, žr. [nustatymą ir toliau šioje temoje įdiekite LBD aplinką](#set-up-deploy) su tuščiu duomenų bazės sekcija. Turite naudoti Supply Chain Management 10.0.21 arba naujesnę versiją koncentratoriaus ir mastelio vieneto aplinkose.

1. **Įkelkite paskirties paketus į LBD projekto turtą LCS.**

    Paruoškite programą, platformą ir tinkinimo paketus, kuriuos naudojate tarp centro ir kraštų skalės vieneto. Norėdami gauti daugiau informacijos, [toliau šioje temoje skyriuje LDB projekto turtą rasite nusiuntimo paskirties paketus](#upload-packages).

1. **LBD aplinkos aptarnavimas su paskirties pakuotėmis.**

    Šis žingsnis užtikrina, kad ta pati versija ir pritaikymai yra įdiegti centre ir toliau. Norėdami gauti daugiau informacijos, toliau šioje [temoje žr. skyrių Paslauga LBD aplinkoje](#service-target-packages) su paskirties paketais.

1. **Atlikite skalės vieneto konfigūravimą ir darbo krūvio priskyrimą.**

    Norėdami gauti daugiau informacijos, toliau šioje [temoje žr. skyrių Priskirti savo LBD krašto skalės](#assign-edge-to-hub) vienetą prie centro skyriaus.

Likusiuose šios temos skyriuose pateikiama daugiau informacijos, kaip atlikti šiuos veiksmus.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Nustatykite ir įdiekite LBD aplinką su tuščia duomenų baze

Šis veiksmas sukuria funkcinę LBD aplinką. Tačiau aplinka nebūtinai turi tas pačias programos ir pagrindo versijas kaip ir centro aplinka. Be to, dar trūksta pritaikymų ir jis dar neįgalintas veikti kaip skalės vienetas.

1. Laikykitės instrukcijų [Nustatyti ir talpinti patalpų aplinkas („Platform update 41“ar naujesnės versijos)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Turite naudoti Supply Chain Management 10.0.21 arba naujesnę versiją koncentratoriaus ir mastelio vieneto aplinkose. Be to, turite naudoti infrastruktūros scenarijų 2.12.0 arba naujesnę versiją. 

    > [!IMPORTANT]
    > Prieš pabaigdami šios temos **veiksmus**, perskaitykite likusią šio skyriaus dalį.

1. Prieš aprašę savo konfigūraciją faile \\ConfigTemplate.xml, paleiskite šį scenarijų:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Šis scenarijus pašalins bet kokią konfigūraciją, kurios nereikia norint įdiegti briaunos skalės vienetus.

1. Nustatykite duomenų bazę, kurioje yra tušti duomenys, kaip aprašyta [konfigūruoti duomenų bazes](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Šiam veiksmui naudoti tuščią data.bak failą.
1. Kai baigsite [Konfigūruoti duomenų bazes](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) veiksme, paleiskite šį scenarijų, kad sukonfigūruotumėte mastelio vieneto Alm Orchestrator duomenų bazę.

    > [!NOTE]
    > Nekonfigūruokite finansinės atskaitomybės duomenų bazės [Konfigūruoti duomenų bazes](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) žingsnis.

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EdgeScaleUnit
    ```

    Scenarijus Initialize-Database.ps1 atlieka šiuos veiksmus:

    1. Sukurkite tuščią duomenų bazę, pavadintą **ScaleUnitAlmDb**.
    2. Suskirstykite vartotojus į duomenų bazės vaidmenis pagal šią lentelę.

        | Vartotojas            | Tipas | Duomenų bazės vaidmuo |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | gMSA | db\_ savininkas     |

1. Toliau vykdykite instrukcijas [Nustatykite ir įdiekite vietines aplinkas (41 ir naujesnės versijos platformos naujinimas)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md).
1. Kai baigsite [Konfigūruokite AD FS](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) žingsnis, atlikite šiuos veiksmus:

    1. Sukurkite naują „Active Directory Federation Services“ (AD FS) programą, kuri leis „Alm Orchestration“ tarnybai susisiekti su jūsų taikomųjų programų objektų serveriu (AOS).

        ```powershell
        # Host URL is your DNS record\host name for accessing the AOS
        .\Create-ADFSServerApplicationForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
        ```

    1. Sukurti naują Azure Active Directory (Azure AD) programa, kuri leis Alm Orchestration tarnybai susisiekti su Scale Unit Management paslauga.

        ```powershell
        # Example .\Create-SumAADApplication.ps1 -ConfigurationFilePath ..\ConfigTemplate.xml -TenantId '6240a19e-86f1-41af-91ab-dbe29dbcfb95' -ApplicationDisplayName 'EdgeAgent-SUMCommunication-EN01'
        .\Create-SumAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                       -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                       -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
        ```

1. Toliau vykdykite instrukcijas [Nustatykite ir įdiekite vietines aplinkas (41 ir naujesnės versijos platformos naujinimas)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Kai turite įvesti vietinio agento konfigūraciją, įsitikinkite, kad įgalinote krašto mastelio vieneto funkcijas ir pateikiate visus reikiamus parametrus.

    ![Krašto mastelio vieneto funkcijų įgalinimas.](media/EnableEdgeScaleUnitFeatures.png "Krašto mastelio vieneto funkcijų įgalinimas.")

1. Prieš diegdami aplinką iš LCS, nustatykite išankstinio diegimo scenarijų. Dėl daugiau informacijos, žr. [Vietinio agento išankstinio ir vėlesnio visuotinio diegimo scenarijai](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Nukopijuokite Configure-CloudAndEdge.ps1 scenarijų iš **ScaleUnit** aplankas **Infrastruktūros scenarijai** prie **Scenarijai** aplanką agento failų saugyklos dalyje, kuri buvo nustatyta aplinkoje. Įprastas maršrutas yra  \\\\lbdiscsi01\\agentas\\Scenarijai.
    2. Sukurkite **PreDeployment.ps1** scenarijų, kuris iškviečiami scenarijus naudojant reikiamus parametrus. Išankstinio diegimo scenarijus turi būti laikomas scenarijų aplanke agento bendro naudojimo failų **saugykloje**. Kitu atveju jos paleisti negalima. Įprastas maršrutas yra \\\\lbdiscsi01\\agentas\\Scenarijai\\PreDeployment.ps1.

        PreDeployment.ps1 scenarijaus turinys bus panašus į toliau pateikiamą pavyzdį.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        . $PSScriptRoot\Configure-CloudAndEdge.ps1 -AgentShare $agentShare -InstanceId '@A'
        ```

        > [!NOTE]
        > Parametras InstanceId turi būti tik du simboliai. Pirmasis simbolis yra @ ir antrasis gali būti bet kokia didžiosios raidė anglų abėcėlės tvarka.
        >
        > - Tinkamos vertės:
        >   - @D
        >   - @X
        > - Negaliojančios vertės:
        >   - @a
        >   - @4
        >   - @#

1. Įdiekite aplinką naudodami naujausią bazinę topologiją, kuri yra.
1. Įdiegę aplinką, atlikite šiuos veiksmus:

    1. Vykdykite šias SQL komandas savo verslo duomenų bazėje (AXDB).

        ```sql
        ALTER TABLE dbo.NUMBERSEQUENCETABLE ENABLE CHANGE_TRACKING WITH (TRACK_COLUMNS_UPDATED = ON)
        delete from NumberSequenceTable
        delete from NumberSequenceReference
        delete from NumberSequenceScope
        delete from FeatureManagementMetadata
        delete from FeatureManagementState
        delete from SysFeatureStateV0
        ```

    1. Padidinkite vienu metu vykstantį didžiausią paketinį seansą iki vertės, kuri yra didesnė nei 4.

        ```sql
        Update batchserverconfig set maxbatchsessions = '<Replace with number of concurrent batch tasks you want>'
        ```

    1. Patikrinkite, ar jūsų verslo duomenų bazėje (AXDB) įgalintas pakeitimų stebėjimas.

        1. Atidarykite „SQL Server Management Studio“ (SSMS).
        1. Pasirinkite ir palaikykite (arba dešiniuoju pelės mygtuku spustelėkite) savo verslo duomenų bazę (AXDB), tada pasirinkite **Savybės**.
        1. Pasirodžiusiame lange pasirinkite **Keisti stebėjimą**, tada nustatykite šias reikšmes:

            - **Keitimų sekimas:** *teisinga*
            - **Užlaikymo laikotarpis:** *7*
            - **Užlaikymo vienetai:** *Dienos*
            - **Automatinis valymas:** *Teisinga*

    1. Pridėkite anksčiau sukurtą AD FS programos ID (naudodami scenarijų Create-ADFSServerApplicationForEdgeScaleUnits.ps1) prie Azure AD taikomųjų programų lentelę savo mastelio vienete. Šį veiksmą galite atlikti rankiniu būdu naudodami vartotojo sąsają (UI). Arba galite jį užbaigti naudodami duomenų bazę, naudodami šį scenarijų.

        ```sql
        DECLARE @ALMOrchestratorId NVARCHAR(76) = '<Replace with the ADFS Application ID created in a previous step>';

        IF NOT EXISTS (SELECT TOP 1 1 FROM SysAADClientTable WHERE AADClientId = @ALMOrchestratorId)
        BEGIN
            INSERT INTO SysAADClientTable (AADClientId, UserId, Name, ModifiedBy, CreatedBy)
            VALUES (@ALMOrchestratorId, 'ScaleUnitManagement', 'Scale Unit Management', 'Admin', 'Admin');
        END
        ```

## <a name="set-up-an-azure-key-vault-and-an-azure-ad-application-to-enable-communication-between-scale-units"></a><a name="set-up-keyvault"></a> Nustatykite „Azure“ raktų saugyklą ir Azure AD programa, leidžianti palaikyti ryšį tarp masto vienetų

1. Kai jūsų aplinka bus įdiegta, sukurkite papildomą Azure AD programa, leidžianti užtikrinti patikimą ryšį tarp stebulės ir svarstyklių įrenginio.

    ```powershell
    .\Create-SpokeToHubAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                          -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                          -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
    ```

1. Sukūrę programą, turite sukurti kliento paslaptį ir išsaugoti informaciją Azure raktų saugykloje. Be to, turite suteikti prieigą prie Azure AD sukurta programa, kad ji galėtų nuskaityti raktų saugykloje saugomas paslaptis. Jūsų patogumui šis scenarijus automatiškai atliks visus reikiamus veiksmus.

    ```powershell
    .\Create-SpokeToHubAADAppSecrets.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                         -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                         -SubscriptionName '<Any subscription within your tenant>' `
                                         -ResourceGroupName '<Any resource group within your subscription>' `
                                         -KeyVaultName '<Any key vault within your resource group>' `
                                         -Location '<Any Azure location where Azure Key Vault is available>' `
                                         -LCSEnvironmentId '<The LCS environment ID of your deployed scale unit>' `
    ```

    > [!NOTE]
    > Jei nėra raktų saugyklos, kurioje nurodyta **KeyVaultName** reikšmė egzistuoja, scenarijus ją automatiškai sukuria.

1. Pridėkite Azure AD programos ID, kurį ką tik sukūrėte (kai naudojate Create-SpokeToHubAADApplication.ps1 scenarijų)Azure AD programų lentelę savo centre. Šį veiksmą galite atlikti rankiniu būdu naudodami vartotojo sąsają.

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Įkelkite paskirties paketus į LBD projekto turtą LCS

Šis veiksmas paruošia programos versiją, platformos versiją ir pritaikymus, kurie bus pereiti prie jūsų LBD svarstyklių aplinkos.

1. Įkelkite tą patį sujungtos programos / platformos paketą, kuris buvo pritaikytas centro aplinkai, į LCS vietinio projekto turto biblioteką.
1. Gaukite tinkintą talpinimo paketą, kuris buvo pritaikytas centro aplinkai ir atnaujintas į LCS vietinio projekto turto biblioteką.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>LBD aplinkos aptarnavimas su paskirties pakuotėmis

Šis veiksmas paruošia programos versiją, platformos versiją ir pritaikymus, kurie bus pereiti prie jūsų LBD svarstyklių aplinkos su centru.

1. Aptarnavimas LBD aplinkoje su sujungtos programos / platformos paketu, kurį nusiuntėte atlikdami ankstesnį veiksmą.
1. Aptarnavimas LBD aplinkoje su sujungtos tinkintu talpinimo paketu, kurį nusiuntėte atlikdami ankstesnį veiksmą.

    ![LCS naujinimų taikymas.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "LCS naujinimų taikymas")

    ![Tinkinimo paketo pasirinkimas.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Tinkinimo paketo pasirinkimas")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Priskirkite savo LBD briaunos svarstyklių vienetą prie centro

Jūs konfigūruojate ir valdote savo krašto mastelio bloką per Scale Unit Management portalą. Daugiau informacijos žr [Tvarkykite mastelio vienetus ir darbo krūvius naudodami Scale Unit Manager portalą](./cloud-edge-landing-page.md#scale-unit-manager-portal).

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
