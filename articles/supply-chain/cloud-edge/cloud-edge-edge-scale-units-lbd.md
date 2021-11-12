---
title: Briaunos skalės vienetų diegimas pasirinktinėje aparatūroje naudojant LBD (peržiūra)
description: Šioje temoje paaiškinama, kaip parengti vietinės briaunos svarstyklių vienetus naudojant pasirinktinę aparatūrą ir diegimą, pagrįstą vietinės verslo duomenimis (LBD).
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0ebbdaab9d6f040497d3158db2712e102b6e9aa8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678986"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd-preview"></a>Briaunos skalės vienetų diegimas pasirinktinėje aparatūroje naudojant LBD (peržiūra)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)] <!--KFM: Until 11/1/2021 -->

Kraštų skalės vienetai atlieka svarbus vaidmenį paskirstytoje tiekimo grandinės valdymo ir kokybės topologijoje. Topologijoje galite paskirstyti darbo krūvius savo „Supply Chain Management“ cloud centre ir papildomiems skalės vienetams debesyje arba ant krašto.

Kraštų skalės vienetus galima įdiegti sukuriant vietinę verslo duomenų (LBD) aplinką ir sukonfigūruojant [šią aplinką, kad](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) ji veiktų kaip skalės vienetas jūsų paskirstytoje „supply chain management“ topologijoje. Tai pasiekiama susieant vietinę LBD aplinką su „Supply Chain Management“ aplinka debesyje, kuri sukonfigūruota veikti kaip centras.  

Kraštų skalės vienetai šiuo metu peržiūrimi. Todėl šio tipo aplinką galima naudoti tik pagal [peržiūros terminus](https://aka.ms/scmcnepreviewterms).

Šioje temoje aprašoma, kaip nustatyti vietinę LBD aplinką kaip kraštų skalės vienetą ir susieti ją su centru.

## <a name="deployment-overview"></a>Talpinimo apžvalga

Toliau pateikta talpinimo veiksmų apžvalga.

1. **Įjunkite savo LBD projekto ciklo tarnybose „Microsoft Dynamics Lifecycle Services“ (LCS).**

    Peržiūros metu LBD briaunos skalės vienetai skirti esamiems LBD klientams. Papildomos 60 dienų apribotos LBD smėlio dėžės atminties dėžių bus pateiktos tik tam tikrose klientų situacijose.

1. **Nustatykite ir įdiekite LBD aplinką su tuščia *duomenų* baze.**

    Norėdami įdiegti LBD aplinką su naujausia topologija ir tuščia duomenų baze, naudokite LCS. Norėdami gauti daugiau informacijos, žr. [nustatymą ir toliau šioje temoje įdiekite LBD aplinką](#set-up-deploy) su tuščiu duomenų bazės sekcija. Turite naudoti „Supply Chain Management“ 10.0.19 versiją naudodami 43 arba aukštesnę platformos naujinimą visose centro ir skalės vieneto aplinkose.

1. **Įkelkite paskirties paketus į LBD projekto turtą LCS.**

    Paruoškite programą, platformą ir tinkinimo paketus, kuriuos naudojate tarp centro ir kraštų skalės vieneto. Norėdami gauti daugiau informacijos, [toliau šioje temoje skyriuje LDB projekto turtą rasite nusiuntimo paskirties paketus](#upload-packages).

1. **LBD aplinkos aptarnavimas su paskirties pakuotėmis.**

    Šis žingsnis užtikrina, kad ta pati versija ir pritaikymai yra įdiegti centre ir toliau. Norėdami gauti daugiau informacijos, toliau šioje [temoje žr. skyrių Paslauga LBD aplinkoje](#service-target-packages) su paskirties paketais.

1. **Atlikite skalės vieneto konfigūravimą ir darbo krūvio priskyrimą.**

    Norėdami gauti daugiau informacijos, toliau šioje [temoje žr. skyrių Priskirti savo LBD krašto skalės](#assign-edge-to-hub) vienetą prie centro skyriaus.

Likusiuose šios temos skyriuose pateikiama daugiau informacijos, kaip atlikti šiuos veiksmus.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Nustatykite ir įdiekite LBD aplinką su tuščia duomenų baze

Šis veiksmas sukuria funkcinę LBD aplinką. Tačiau aplinka nebūtinai turi tas pačias programos ir pagrindo versijas kaip ir centro aplinka. Be to, dar trūksta pritaikymų ir jis dar neįgalintas veikti kaip skalės vienetas.

1. Laikykitės instrukcijų [Nustatyti ir talpinti patalpų aplinkas („Platform update 41“ar naujesnės versijos)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Turite naudoti „Supply Chain Management“ 10.0.19 versiją naudodami 43 arba aukštesnę platformos naujinimą visose centro ir skalės vieneto aplinkose

    > [!IMPORTANT]
    > Prieš pabaigdami šios temos **veiksmus**, perskaitykite likusią šio skyriaus dalį.

1. Prieš aprašę savo konfigūraciją faile \\ConfigTemplate.xml, paleiskite šį scenarijų:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Šis scenarijus pašalins bet kokią konfigūraciją, kurios nereikia norint įdiegti briaunos skalės vienetus.

1. Nustatykite duomenų bazę, kurioje yra tušti duomenys, kaip aprašyta [konfigūruoti duomenų bazes](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Šiam veiksmui naudoti tuščią data.bak failą.
1. Nustatykite išankstinio diegimo scenarijų. Dėl daugiau informacijos, žr. [Vietinio agento išankstinio ir vėlesnio visuotinio diegimo scenarijai](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Nukopijuokite turinį iš infrastruktūros scenarijų aplanko **ScaleUnit** katalogą **Infrastruktūros scenarijai** į **Scenarijai** katalogo agento failo talpinimo bendrinime, kuris buvo nustatytas aplinkoje. Įprastas maršrutas yra  \\\\lbdiscsi01\\agentas\\Scenarijai.
    2. Sukurkite **PreDeployment.ps1** scenarijų, kuris iškviečiami scenarijus naudojant reikiamus parametrus. Išankstinio diegimo scenarijus turi būti laikomas scenarijų aplanke agento bendro naudojimo failų **saugykloje**. Kitu atveju jos paleisti negalima. Įprastas maršrutas yra \\\\lbdiscsi01\\agentas\\Scenarijai\\PreDeployment.ps1.

        PreDeployment.ps1 scenarijaus turinys bus panašus į toliau pateikiamą pavyzdį.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        & $agentShare\Scripts\Configure-CloudandEdge.ps1 -AgentShare $agentShare -InstanceId '@A' -DatabaseServer 'lbdsqla01.contoso.com' -DatabaseName 'AXDB'
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

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Įkelkite paskirties paketus į LBD projekto turtą LCS

Šis veiksmas paruošia programos versiją, platformos versiją ir pritaikymus, kurie bus pereiti prie jūsų LBD svarstyklių aplinkos.

1. Įkelkite tą patį sujungtos programos / platformos paketą, kuris buvo pritaikytas centro aplinkai, į LCS vietinio projekto turto biblioteką.
1. Gaukite tinkintą talpinimo paketą, kuris buvo pritaikytas centro aplinkai ir atnaujintas į LCS vietinio projekto turto biblioteką.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>LBD aplinkos aptarnavimas su paskirties pakuotėmis

Šis veiksmas paruošia programos versiją, platformos versiją ir pritaikymus, kurie bus pereiti prie jūsų LBD svarstyklių aplinkos su centru.

1. Aptarnavimas LBD aplinkoje su sujungtos programos / platformos paketu, kurį nusiuntėte atlikdami ankstesnį veiksmą.
1. Aptarnavimas LBD aplinkoje su sujungtos tinkintu talpinimo paketu, kurį nusiuntėte atlikdami ankstesnį veiksmą.

    ![Pasirinkdami Tvarkyti > Taikyti naujinimus LCS.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Pasirinkdami Tvarkyti > Taikyti naujinimus LCS")

    ![Tinkinimo paketo pasirinkimas.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Tinkinimo paketo pasirinkimas")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Priskirkite savo LBD briaunos svarstyklių vienetą prie centro

Peržiūrėdami kraštų skalės vienetus, privalote naudoti skalės vieneto diegimo ir konfigūravimo įrankius, kuriuos galima naudoti GitHub [norėdami priskirti savo LBD krašto svarstyklių vienetą](https://github.com/microsoft/SCMScaleUnitDevTools) prie centro. Procesas įgalina LBD konfigūraciją veikti kaip krašto skalės vienetas ir susieja ją su centru. Procesas panašus į "one-box" programavimo aplinkos konfigūravimą.

1. Atsisiųskite naujausią [SCMScaleUnitDevTools](https://github.com/microsoft/SCMScaleUnitDevTools/releases) leidimą ir išskleisti failo turinį.
1. Sukurkite failo kopiją `UserConfig.sample.xml` ir pavadinkite ją `UserConfig.xml`.
1. Sukurkite „Microsoft Azure Active Directory“ („Azure AD“) programą savo „Azure AD“ nuomotojuje, kaip minėta [Talpinimo gidas skalės vienetams ir darbo apkrovoms](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#aad-application-registrations).
    1. Sukūrę, savo centre „Azure AD“ nueikite į programų formą (SysAADClientTable).
    1. Sukurkite naują įrašą ir nustatykite **kliento ID** kaip programos, kurią sukūrėte, ID. Nustatykite **Pavadinimą** į *ScaleUnits* ir **vartotojo ID** į *Administratorius*.

1. Sukurkite „Active Directory Federation Service" (AD FS) programą, kaip nurodyta [Skalės vieneto ir darbo krūvio diegimo vadove](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#adfs-application-registrations).
    1. Sukūrę, savo centre „Azure AD“ nueikite į programų formą (SysAADClientTable) ant jūsų krašto skalės vieneto.
    1. Sukurkite naują įrašą ir nustatykite **kliento ID** kaip programos, kurią sukūrėte, ID. Nustatykite **Vartotojo ID** į *administratorius*.

1. Modifikuoti `UserConfig.xml` failą.
    1. Į `InterAOSAADConfiguration` skyrių įveskite informaciją iš anksčiau „Azure AD“ sukurtos programos.
        - Elemente `AppId` įveskite „Azure" programos ID.
        - Elemente `AppSecret` įveskite „Azure" raktą programos ID.
        - Elemente `Authority` turi būti URL, nurodantis jūsų nuomininko saugos įgaliojimus.

        ```xml
        <InterAOSAADConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopty56TGUedDTVhtER-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </InterAOSAADConfiguration>
        ```

    1. Pirmiausia `ScaleUnitConfiguration` skyriuje `ScaleUnitInstance` keiskite `AuthConfiguration` skyrių.
        - Elemente `AppId` įveskite „Azure" programos ID.
        - Elemente `AppSecret` įveskite „Azure" raktą programos ID.
        - Elemente `Authority` turi būti URL, nurodantis jūsų nuomininko saugos įgaliojimus.

        ```xml
        <AuthConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopdz.6d3DTVOtf9Lo-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </AuthConfiguration>
        ```

    1. Taip pat, tam pačiam `ScaleUnitInstance`, nustatykite šias vertes:
        - Elemente `Domain` nurodykite savo centro URL. Pavyzdžiui: `https://cloudhub.sandbox.operations.dynamics.com/`
        - Elemente `EnvironmentType` įsitikinkite, kad `LCSHosted` vertė nustatyta.

    1. Pirmiausia `ScaleUnitConfiguration` skyriuje antram `ScaleUnitInstance` keiskite `AuthConfiguration` skyrių.
        - Elemente `AppId` įveskite „AD FS" programos ID.
        - Elemente `AppSecret` įveskite „AD FS" raktą programos ID.
        - Elemente `Authority` turi būti AD FS egzemplioriaus URL.

        ```xml
        <AuthConfiguration>
            <AppId>26b16f25-21d8-4d36-987b-62df292895aa</AppId>
            <AppSecret>iZFfObgI6lLtY9kEbBjEFV98NqI5_YZ0e5SBcWER</AppSecret>
            <Authority>https://adfs.contoso.com/adfs</Authority>
        </AuthConfiguration>
        ```

    1. Taip pat, tam pačiam `ScaleUnitInstance`, nustatykite šias vertes:
        - Elemente `Domain` nurodykite savo centro URL krašto skalės vienetui. Pavyzdžiui: https://ax.contoso.com/
        - Elemente įsitikinkite, kad `EnvironmentType` elementas yra LBD nustatytas.
        - Elemente `ScaleUnitId` įveskite tą pačią vertę, kurią nurodėte `InstanceId` konfigūruodami `Configure-CloudandEdge.ps1` išankstinio diegimo scenarijų.

        > [!NOTE]
        > Jei nenaudokite numatytojo ID (@A), įsitikinkite, kad atnaujinsite kiekvieno ConfiguredWorkload ScaleUnitId sekcijoje Darbo krūviai.

1. Atidarykite „PowerShell" ir pereikite į aplanką, kuriame yra `UserConfig.xml` failas.

1. Vykdykite įrankį su šia komanda.

    ```powershell
    .\CLI.exe
    ```

    > [!NOTE]
    > Po kiekvieno veiksmo, turite iš naujo paleisti įrankį.

1. Į įrankį pasirinkite **2. Paruoškite darbo krūvio diegimo aplinkas**. Tada vykdykite šiuos veiksmus:
    1. Pasirinkite **1. Paruoškite centrą**.
    1. Pasirinkite **2. Paruoškite skalės vienetą**.

    > [!NOTE]
    > Jei šios komandos nevykdote iš valymo diegimo ir jos atlikti nepavyko, atlikite šiuos veiksmus:
    >
    > - Pašalinti visus aplanko aplankus `aos-storage` (išskyrus `GACAssemblies`).
    > - Savo verslo duomenų bazėje (AXDB) vykdykite šią SQL komandą:
    >
    > ```sql 
    > delete from storagefoler
    > ```

1. Savo verslo duomenų bazėje (AXDB) vykdykite šią SQL komandą:

    ```sql
    delete from FEATUREMANAGEMENTMETADATA
    delete from FEATUREMANAGEMENTSTATE
    delete from NUMBERSEQUENCESCOPE
    ```

1. Keitimų sekimo įgalinimas jūsų verslo duomenų bazėje (AXDB)
    1. Start SQL „Server Management Studio“ (SSMS).
    1. Dešiniuoju pelės klavišu spustelėkite savo verslo duomenų bazę (AXDB) ir pasirinkite ypatybes.
    1. Atidarytuose languose pasirinkite **Keitimų sekimas** ir atlikite šiuos parametrus:

        - **Keitimų sekimas:** *teisinga*
        - **Užlaikymo laikotarpis:** *7*
        - **Užlaikymo vienetai:** *Dienos*
        - **Automatinis valymas:** *Teisinga*

1. Į įrankį pasirinkite **3. Įdiekite darbo krūvius**. Tada vykdykite šiuos veiksmus:
    1. Pasirinkite **1. Įdiekite hub**.
    1. Pasirinkite **2. Įdiekite svarstyklių vienetais**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
