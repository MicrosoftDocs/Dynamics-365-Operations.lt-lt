---
title: Briaunos skalės vienetų diegimas pasirinktinėje aparatūroje naudojant LBD
description: Šioje temoje paaiškinama, kaip parengti vietinės briaunos svarstyklių vienetus naudojant pasirinktinę aparatūrą ir diegimą, pagrįstą vietinės verslo duomenimis (LBD).
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: f1ab0a2c289f48dd8bfb7529f0dcc694a97f18ea
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2021
ms.locfileid: "7729080"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd"></a>Briaunos skalės vienetų diegimas pasirinktinėje aparatūroje naudojant LBD

[!include [banner](../includes/banner.md)]

Kraštų skalės vienetai atlieka svarbus vaidmenį paskirstytoje tiekimo grandinės valdymo ir kokybės topologijoje. Topologijoje galite paskirstyti darbo krūvius savo „Supply Chain Management“ cloud centre ir papildomiems skalės vienetams debesyje arba ant krašto.

Kraštų skalės vienetus galima įdiegti sukuriant vietinę verslo duomenų (LBD) aplinką ir sukonfigūruojant [šią aplinką, kad](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) ji veiktų kaip skalės vienetas jūsų paskirstytoje „supply chain management“ topologijoje. Tai pasiekiama susieant vietinę LBD aplinką su „Supply Chain Management“ aplinka debesyje, kuri sukonfigūruota veikti kaip centras.  

Šioje temoje aprašoma, kaip nustatyti vietinę LBD aplinką kaip kraštų skalės vienetą ir susieti ją su centru.

## <a name="deployment-overview"></a>Talpinimo apžvalga

Toliau pateikta talpinimo veiksmų apžvalga.

1. **Įjunkite savo LBD projekto ciklo tarnybose „Microsoft Dynamics Lifecycle Services“ (LCS).**

1. **Nustatykite ir įdiekite LBD aplinką su tuščia *duomenų* baze.**

    Norėdami įdiegti LBD aplinką su naujausia topologija ir tuščia duomenų baze, naudokite LCS. Norėdami gauti daugiau informacijos, žr. [nustatymą ir toliau šioje temoje įdiekite LBD aplinką](#set-up-deploy) su tuščiu duomenų bazės sekcija. Turite naudoti tiekimo grandinės valdymo 10.0.21 arba vėlesnę versiją visose centro ir skalės vieneto aplinkose.

1. **Įkelkite paskirties paketus į LBD projekto turtą LCS.**

    Paruoškite programą, platformą ir tinkinimo paketus, kuriuos naudojate tarp centro ir kraštų skalės vieneto. Norėdami gauti daugiau informacijos, [toliau šioje temoje skyriuje LDB projekto turtą rasite nusiuntimo paskirties paketus](#upload-packages).

1. **LBD aplinkos aptarnavimas su paskirties pakuotėmis.**

    Šis žingsnis užtikrina, kad ta pati versija ir pritaikymai yra įdiegti centre ir toliau. Norėdami gauti daugiau informacijos, toliau šioje [temoje žr. skyrių Paslauga LBD aplinkoje](#service-target-packages) su paskirties paketais.

1. **Atlikite skalės vieneto konfigūravimą ir darbo krūvio priskyrimą.**

    Norėdami gauti daugiau informacijos, toliau šioje [temoje žr. skyrių Priskirti savo LBD krašto skalės](#assign-edge-to-hub) vienetą prie centro skyriaus.

Likusiuose šios temos skyriuose pateikiama daugiau informacijos, kaip atlikti šiuos veiksmus.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a> Nustatykite ir įdiekite LBD aplinką su tuščia duomenų baze

Šis veiksmas sukuria funkcinę LBD aplinką. Tačiau aplinka nebūtinai turi tas pačias programos ir pagrindo versijas kaip ir centro aplinka. Be to, dar trūksta pritaikymų ir jis dar neįgalintas veikti kaip skalės vienetas.

1. Laikykitės instrukcijų [Nustatyti ir talpinti patalpų aplinkas („Platform update 41“ar naujesnės versijos)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Turite naudoti tiekimo grandinės valdymo 10.0.21 arba vėlesnę versiją visose centro ir skalės vieneto aplinkose. Be to, turite naudoti 2.12.0 arba vėlesnę infrastruktūros scenarijų versiją. 

    > [!IMPORTANT]
    > Prieš pabaigdami šios temos **veiksmus**, perskaitykite likusią šio skyriaus dalį.

1. Prieš aprašę savo konfigūraciją faile \\ ConfigTemplate.xml, paleiskite šį scenarijų:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Šis scenarijus pašalins bet kokią konfigūraciją, kurios nereikia norint įdiegti briaunos skalės vienetus.

1. Nustatykite duomenų bazę, kurioje yra tušti duomenys, kaip aprašyta [konfigūruoti duomenų bazes](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Šiam veiksmui naudoti tuščią data.bak failą.
1. Baigę duomenų bazių konfigūravimo veiksmą, vykdykite toliau nurodytą scenarijų, norėdami sukonfigūruoti [skalės](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) vieneto konvertavimo instrumentatoriaus duomenų bazę.

    > [!NOTE]
    > Nekonfigūruokite finansinių ataskaitų duomenų bazės [atliekant duomenų bazės konfigūravimo](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) veiksmą.

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EdgeScaleUnit
    ```

    Inicializuoti duomenų bazę.ps1 scenarijus atlieka šiuos veiksmus:

    1. Sukurkite tuščią duomenų bazę, **pavadintą ScaleUnitDb**.
    2. Susiekite vartotojus su duomenų bazės vaidmenimis, remiantis šia lentele.

        | Vartotojas            | Tipas | Duomenų bazės vaidmuo |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | Asociacija | Db \_ savininkas     |

1. Toliau vadovaukitės sąrankos instrukcijomis [ir įdiekite vietinę aplinką (41 ir vėlesnė platformos naujinimas)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md).
1. Baigę konfigūruoti AD [FS](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) veiksmą, atlikite šiuos veiksmus:

    1. Sukurkite naują "Active Directory" federacijos tarnybų (AD FS) programą, kuri įgalins "Įvertinimų instrumentavimo" tarnybą palaikyti ryšį su programos objektų serveriu (AOS).

        ```powershell
        # Host URL is your DNS record\host name for accessing the AOS
        .\Create-ADFSServerApplicationForEdgeScaleUnits.ps1 -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
        ```

    1. Sukurkite naują Azure Active Directory Azure AD () programą, kuri įgalins Jav instrumentavimo tarnybą susisiekti su svarstyklių vienetų valdymo tarnyba.

        ```powershell
        # Example .\Create-SumAADApplication.ps1 -ConfigurationFilePath ..\ConfigTemplate.xml -TenantId '6240a19e-86f1-41af-91ab-dbe29dbcfb95' -ApplicationDisplayName 'EdgeAgent-SUMCommunication-EN01'
        .\Create-SumAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                       -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                       -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
        ```

1. Toliau vadovaukitės sąrankos instrukcijomis [ir įdiekite vietinę aplinką (41 ir vėlesnė platformos naujinimas)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Kai turite įvesti vietinio agento konfigūraciją, įsitikinkite, kad įgalinsite "Edge Scale" vieneto funkcijas ir pateikite visus reikiamus parametrus.

    ![Įgalina briaunos skalės vieneto funkcijas.](media/EnableEdgeScaleUnitFeatures.png "Įgalina briaunos skalės vieneto funkcijas.")

1. Prieš diegdami aplinką iš LCS, nustatykite išankstinio diegimo scenarijų. Dėl daugiau informacijos, žr. [Vietinio agento išankstinio ir vėlesnio visuotinio diegimo scenarijai](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Nukopijuokite scenarijų Configure-CloudAndEdge.ps1 iš aplanko ScaleUnit infrastruktūros scenarijuose į aplanką Scenarijai, esantį agento failų saugykloje, kuri nustatyta **·** **·** **·** aplinkoje. Įprastas maršrutas yra  \\\\ lbdiscsi01\\ agentas\\ Scenarijai.
    2. Sukurkite **PreDeployment.ps1** scenarijų, kuris iškviečiami scenarijus naudojant reikiamus parametrus. Išankstinio diegimo scenarijus turi būti laikomas scenarijų aplanke agento bendro naudojimo failų **saugykloje**. Kitu atveju jos paleisti negalima. Įprastas maršrutas yra \\\\ lbdiscsi01\\ agentas\\ Scenarijai\\ PreDeployment.ps1.

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

    1. Savo verslo duomenų bazėje (AXDB) vykdykite šias SQL komandas.

        ```sql
        ALTER TABLE dbo.NUMBERSEQUENCETABLE ENABLE CHANGE_TRACKING WITH (TRACK_COLUMNS_UPDATED = ON)
        delete from NumberSequenceTable
        delete from NumberSequenceReference
        delete from NumberSequenceScope
        delete from FeatureManagementMetadata
        delete from FeatureManagementState
        delete from SysFeatureStateV0
        ```

    1. Padidinkite vienu metu e pačiu metu seanso maksimalų seansą iki daugiau nei 4 reikšmės.

        ```sql
        Update batchserverconfig set maxbatchsessions = '<Replace with number of concurrent batch tasks you want>'
        ```

    1. Patikrinkite, ar jūsų verslo duomenų bazėje (AXDB) įgalintas keitimų sekimas.

        1. Atidarykite SQL serverio valdymo studiją (SSMS).
        1. Pasirinkite ir sulaikykite (arba spustelėkite dešiniuoju pelės mygtuku) savo verslo duomenų bazę (AXDB), tada pasirinkite **·** Ypatybės.
        1. Rodomame lange pasirinkite **Keitimų** sekimas ir nustatykite šias vertes:

            - **Keitimų sekimas:** *teisinga*
            - **Užlaikymo laikotarpis:** *7*
            - **Užlaikymo vienetai:** *Dienos*
            - **Automatinis valymas:** *Teisinga*

    1. Pridėkite AD FS programos ID, kurį sukūrėte anksčiau (naudodami create-ADFSServerApplicationForEdgeScaleUnits.ps1 scenarijų) į programų lentelę savo skalės Azure AD vienete. Šį veiksmą galite atlikti rankiniu būdu naudodami vartotojo sąsają (vartotojo SĄSAJĄ). Taip pat galite užbaigti ją per duomenų bazę naudodami šį scenarijų.

        ```sql
        DECLARE @ALMOrchestratorId NVARCHAR(76) = '<Replace with the ADFS Application ID created in a previous step>';

        IF NOT EXISTS (SELECT TOP 1 1 FROM SysAADClientTable WHERE AADClientId = @ALMOrchestratorId)
        BEGIN
            INSERT INTO SysAADClientTable (AADClientId, UserId, Name, ModifiedBy, CreatedBy)
            VALUES (@ALMOrchestratorId, 'ScaleUnitManagement', 'Scale Unit Management', 'Admin', 'Admin');
        END
        ```

## <a name="set-up-an-azure-key-vault-and-an-azure-ad-application-to-enable-communication-between-scale-units"></a><a name="set-up-keyvault"></a> Nustatyti "Azure" rakto saugyklą ir programą, Azure AD kad būtų galima įjungti svarstyklių vienetų ryšį

1. Įdiegus aplinką, sukurkite papildomą programą, kuri įgalina patikimą ryšį tarp Azure AD jūsų centro ir svarstyklių vieneto.

    ```powershell
    .\Create-SpokeToHubAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                          -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                          -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
    ```

1. Kai sukuriate programą, turite sukurti kliento slaptą ir išsaugoti informaciją "Azure" rakto saugykloje. Be to, turite suteikti prieigą prie sukurtos programos, kad ji galėtų nuskaityti rakto saugykloje Azure AD saugomus paslapius. Jūsų patogumui toliau pateikiamas scenarijus automatiškai atliks visus reikalingus veiksmus.

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
    > Jei nėra kodo saugyklos, kuri turi nurodytą **KeyVaultName** vertę, scenarijus automatiškai sukuria vieną.

1. Įtraukite ką tik sukurtą programos Azure AD ID (naudodami scenarijų Create-SgToHubAADApplication.ps1) į programų lentelę savo Azure AD centre. Šį veiksmą galite atlikti naudodami vartotojo sąsają.

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a> Įkelkite paskirties paketus į LBD projekto turtą LCS

Šis veiksmas paruošia programos versiją, platformos versiją ir pritaikymus, kurie bus pereiti prie jūsų LBD svarstyklių aplinkos.

1. Įkelkite tą patį sujungtos programos / platformos paketą, kuris buvo pritaikytas centro aplinkai, į LCS vietinio projekto turto biblioteką.
1. Gaukite tinkintą talpinimo paketą, kuris buvo pritaikytas centro aplinkai ir atnaujintas į LCS vietinio projekto turto biblioteką.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a> LBD aplinkos aptarnavimas su paskirties pakuotėmis

Šis veiksmas paruošia programos versiją, platformos versiją ir pritaikymus, kurie bus pereiti prie jūsų LBD svarstyklių aplinkos su centru.

1. Aptarnavimas LBD aplinkoje su sujungtos programos / platformos paketu, kurį nusiuntėte atlikdami ankstesnį veiksmą.
1. Aptarnavimas LBD aplinkoje su sujungtos tinkintu talpinimo paketu, kurį nusiuntėte atlikdami ankstesnį veiksmą.

    ![Taikomi LCS naujinimai.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Taikomi LCS naujinimai")

    ![Tinkinimo paketo pasirinkimas.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Tinkinimo paketo pasirinkimas")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a> Priskirkite savo LBD briaunos svarstyklių vienetą prie centro

Konfigūruojate ir valdote savo kraštų skalės vienetą naudodami svarstyklių valdymo portalą. Daugiau informacijos ieškokite Skyriuje Valdyti [skalės vienetus ir darbo krūvius naudojant skalės vieneto tvarkytuvo](./cloud-edge-landing-page.md#scale-unit-manager-portal) portalą.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
