---
title: Inventoriaus matomumo papildinys
description: Ši tema aprašo, kaip įdiegti ir konfigūruoti inventoriaus matomumo papildinį „Dynamics 365 Supply Chain Management“.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 84f5e949f0c81f840c8a9086d05bbcfc576e42aa
ms.sourcegitcommit: b67665ed689c55df1a67d1a7840947c3977d600c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6017011"
---
# <a name="inventory-visibility-add-in"></a>Inventoriaus matomumo papildinys

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Inventoriaus matomumo papildinys yra nepriklausomos ir labai išdidinamos mikropaslaugos, kurios įjungia realaus laiko turimo inventoriaus sekimą ir taip suteikia bendrą inventoriaus vaizdą.

Visa informacija susijusi su turimu inventoriumi yra eksportuojama į paslaugas esančias šalia realaus laiko per žemo lygio SQL integravimą. Išorės sistemos prieiga prie paslaugų per RESTful API, kurios leidžia laukti turimos informacijos pagal turimą dimensijų rinkinį ir gauti esamų turimų padėčių sąrašą.

Inventoriaus matomumas yra mikrotarnyba, esanti „Microsoft Dataverse“, o tai reiškia, kad galite ją plėsti kurdami „Power Apps“ ir taikydami „Power BI“ norėdami tinkintų funkcijų, atitinkančių jūsų verslo reikalavimus. Taip pat galima pagerinti indeksavimą inventoriaus užklausoms.

Inventoriaus matomumas suteikia konfigūravimo parinktis, kurios leidžia jį integruoti su keliomis trečiųjų šalių sistemomis. Jis palaiko standartizuotą inventoriaus dimensiją, tinkintą plėtinį ir standartizuotus ir konfigūruojamus skaičiuojamus kiekius.

Ši tema aprašo, kaip įdiegti ir konfigūruoti inventoriaus matomumo papildinį „Dynamics 365 Supply Chain Management“ ir kaip naudoti jo programavimo sąsają (API).

## <a name="install-the-inventory-visibility-add-in"></a>Įdiekite Inventoriaus matomumo papildinį

Jums reikia įdiegti jį naudojant „Microsoft Dynamics Lifecycle Services“ (LCS). LCS yra bendradarbiavimo portalas suteikiantis aplinką ir reguliariai naujinamų paslaugų rinkinį, kuris padeda jums valdyti programos gyvavimo ciklą jūsų „Dynamics 365 Finance and Operations“ programose.

Dėl daugiau informacijos, žr. [„Lifecycle Services“ ištekliai](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="inventory-visibility-add-in-prerequisites"></a>Atsargų matomumo išankstinės sąlygos

Prieš jums įdiegiant inventoriaus matomumo papildinį, atlikite šiuos veiksmus:

- Gaukite LCS diegimo projektą su mažiausiai viena patalpinta aplinka.
- Įsitikinkite, kad baigtos būtinosios priedų nustatymo sąlygos, pateikiamos skyriuje [Priedų apžvalga](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) buvo patenkintos. Atsargų matomumui nereikia dvigubo rašymo susiejimo.
- Kreipkitės į atsargų matomumo komandą el. paštu [inventvisibilitysupp@microsoft.com ](mailto:inventvisibilitysupp@microsoft.com), kad gautumėte šiuos tris reikalingus failus:
  - `Inventory Visibility Dataverse Solution.zip`
  - `Inventory Visibility Configuration Trigger.zip`
  - `Inventory Visibility Integration.zip` (jei jūsų vykdoma „Supply Chain Management” versija yra ankstesnė nei 10.0.18 versija)
- Kitu atveju, kreipkitės į atsargų matomumo komandą el. paštu [inventvisibilitysupp@microsoft.com ](mailto:inventvisibilitysupp@microsoft.com), kad gautumėte paketo „Package Deployer“. Šiuos paketus gali naudoti oficialus „Package Deployer“ įrankis.
  - `InventoryServiceBase.PackageDeployer.zip`
  - `InventoryServiceApplication.PackageDeployer.zip` (šiame pakete yra visi paketo pakeitimai `InventoryServiceBase` ir papildomi vartotojo sąsajos programos komponentai)
- Vadovaukitės instrukcijomis, pateiktomis [Greitas pasirengimas darbui: Programos registravimas su „Microsoft” tapatybės platforma](/azure/active-directory/develop/quickstart-register-app), kad užregistruotumėte programą ir įtrauktumėte kliento slaptąjį raktą į AAD pagal jūsų „Azure” prenumeratą.
  - [Programos įtraukimas](/azure/active-directory/develop/quickstart-register-app)
  - [Kliento slaptojo rakto įtraukimas](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
  - Tolesniuose veiksmuose bus naudojami **Programos (Kliento) ID** ir **Kliento slaptasis raktas** ir **Nuomotojo ID**.

> [!NOTE]
> Šiuo metu palaikomos šalys ir regionai yra Kanada, Jungtinės Valstijos ir Europos Sąjunga (ES).

Jei turite kokių klausimų apie šias būtinąsias sąlygas, susisiekite su papildinio produkto komanda.

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>„Dataverse“ nustatymas

Norėdami nustatyti naudoti su atsargų matomumu, pirmiausia turite paruošti būtinąsias sąlygas ir nuspręsti, ar nustatyti „Package Deployer“ įrankį, ar rankiniu būdu importuodami sprendimus (abiejų „Dataverse“ daryti „Dataverse“ nereikia). Tada, įdiekite Inventoriaus matomumo papildinį. Toliau pateikti poskyriai aprašo, kaip užbaigti visas šias užduotis.

#### <a name="prepare-dataverse-prerequisites"></a>Paruošti „Dataverse“ būtinąsias sąlygas

Prieš pradėdami „Dataverse“ nustatyti, pridėkite aptarnavimo principą savo nuomininkui, atlikdami šiuos veiksmus:

1. Įdiekite „Azure AD“ „PowerShell“ v2 modulį, kaip aprašyta skyriuje [„Azure Active Directory“ „PowerShell for Graph“ diegimas](/powershell/azure/active-directory/install-adv2).

1. Paleiskite šią „PowerShell“ komandą:

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)
    
    New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
    ```

#### <a name="set-up-dataverse-using-the-package-deployer-tool"></a>Nustatyti „Dataverse“ naudojant „Package Deployer“ įrankį

Jei turite būtinųjų komponentų, naudokite šią procedūrą, jei norite nustatyti „Dataverse“ naudodami „Package Deployer“ įrankį. Daugiau informacijos apie tai, kaip importuoti sprendimus neautomatiniu būdu, rasite kitame skyriuje (neduokite abiejų).

1. Įdiekite programavimo įrankius, kaip aprašyta [atsisiuntimo „NuGet“ įrankiuose](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).

1. Atsižvelgdami į savo verslo poreikius, pasirinkite `InventoryServiceBase` pakuotę arba `InventoryServiceApplication` pakuotę.

1. Importuoti sprendimus:
    1. `InventoryServiceBase` paketui:
        - Išpakuokite `InventoryServiceBase.PackageDeployer.zip`
        - Rasti `InventoryServiceBase` aplanką, `[Content_Types].xml` failą, `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll` failą, `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` failą ir `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` failą. 
        - Nukopijuokite kiekvieną iš šių aplankų ir rinkmenų į `.\Tools\PackageDeployment` katalogą, kuris buvo sukurtas įdiegus programuotojo įrankius.
    1. `InventoryServiceApplication` paketui:
        - Išpakuokite `InventoryServiceApplication.PackageDeployer.zip`
        - Rasti `InventoryServiceApplication` aplanką, `[Content_Types].xml` failą, `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll` failą, `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` failą ir `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` failą.
        - Nukopijuokite kiekvieną iš šių aplankų ir rinkmenų į `.\Tools\PackageDeployment` katalogą, kuris buvo sukurtas įdiegus programuotojo įrankius.
    1. Vykdyti `.\Tools\PackageDeployment\PackageDeployer.exe`. Norėdami importuoti sprendimus vykdykite ekrane pateiktas instrukcijas.

1. Priskirkite saugos vaidmenis programos vartotojui.
    1. Atidarykite savo „Dataverse“ aplinkos URL.
    1. Eikite į **išplėstinių parametrų \> sistemos \> saugos \> vartotojus** ir raskite vartotoją **# InventoryVisibility**.
    1. Pasirinkite **Priskirti vaidmenį**, tada pasirinkite **Sistemos administratorius**. Jei yra vaidmuo pavadinimu **„Common Data Service“ naudotojas**, pasirinkite jį taip pat.

#### <a name="set-up-dataverse-manually-by-importing-solutions"></a>Neautomatiniu būdu „Dataverse“ nustatyti importuojant sprendimus

Jei turite būtinųjų komponentų, naudokite šią procedūrą, jei norite nustatyti „Dataverse“ rankiniu būdu importuojant sprendimus. Norėdami gauti daugiau informacijos, kaip naudoti „Package Deployer“ įrankį, žr. ankstesniame skyriuje (ne atlikite abu).

1. Sukurkite programos naudotoją „Dataverse“ atsargų matomumui:

    1. Atidarykite savo „Dataverse“ aplinkos URL.
    1. Eikite į **Išplėstiniai nustatymai \> Sistema \> Sauga \> Naudotojai** ir sukurkite programos naudotoją. Naudokite peržiūros meniu, kad puslapio rodinį pakeistumėte į **Programos naudotojai**.
    1. Pasirinkite **Naujas**. Programos ID nustatykite kaip *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*. (Išsaugant keitimus objekto ID įkeliamas automatiškai.) Pavadinimą galima pritaikyti. Pavyzdžiui, jį galima pakeisti į *Atsargų matomumas*. Jums pabaigus, pasirinkite **Įrašyti**.
    1. Pasirinkite **Priskirti vaidmenį**, tada pasirinkite **Sistemos administratorius**. Jei yra vaidmuo pavadinimu **„Common Data Service“ naudotojas**, pasirinkite ir jį.

    Daugiau informacijos žr. skyriuje [Programos naudotojo kūrimas](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

1. Jei jūsų „Dataverse” numatytoji kalba nėra **Anglų**:

    1. Eikite į **Išplėstiniai parametrai \> Administravimas \> Kalbos**,
    1. Pasirinkite **Anglų (LanguageCode=1033)** ir pasirinkite **Taikyti**.

1. Importuokite failą `Inventory Visibility Dataverse Solution.zip`, kuriame yra su „Dataverse“ konfigūracija susiję objektai ir „Power Apps“:

    1. Eikite į puslapį **Sprendimai**.
    1. Pasirinkite **Importuoti**.

1. Importuokite konfigūracijos atnaujinimo paleidiklio eigą:

    1. Eikite į puslapį „Microsoft Flow“.
    1. Patikrinkite, ar yra ryšys, pavadintas „*Dataverse“ (senesnis)*. (Jei ne, sukurkite jį.)
    1. Importuokite failą `Inventory Visibility Configuration Trigger.zip`. Jį importavus srityje **Mano srautai** bus rodomas paleidiklis.
    1. Inicijuokite šiuos keturis kintamuosius, atsižvelgdami į aplinkos informaciją:

        - „Azure“ nuomininko ID
        - „Azure“ programos kliento ID
        - „Azure“ programos kliento raktas
        - Atsargų matomumo galinis punktas

            Daugiau informacijos apie šį kintamąjį žr. toliau šioje temoje pateikiamame skyriuje [Atsargų matomumo integravimo nustatymas](#setup-inventory-visibility-integration).

        ![Konfigūracijos paleidiklis](media/configuration-trigger.png "Konfigūracijos paleidiklis")

    1. Pasirinkite **Įjungti**.

### <a name="install-the-add-in"></a><a name="install-add-in"></a>Papildinio įdiegimas

Norėdami įdiegti inventoriaus matomumo papildinį, atlikite šiuos veiksmus:

1. Prisijunkite prie [„Lifecycle Services“ (LCS)](https://lcs.dynamics.com/Logon/Index) portalo.
1. Pagrindiniame puslapyje pasirinkite projektą, kuriame jūsų aplinka talpinta.
1. Projekto puslapyje pasirinkite aplinką, kurioje norite įdiegti papildinį.
1. Aplinkos puslapyje slinkite žemyn, kol pamatysite skyrių **Aplinkos priedai**, skyriuje **„Power Platform“ integravimas**, kuriame rasite „Dataverse“ aplinkos pavadinimą.
1. Skyriuje **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.

    ![Aplinkos puslapis LCS](media/inventory-visibility-environment.png "Aplinkos puslapis LCS")

1. Rinkitės **Diegti naują papildinį** nuorodą. Esamų atvirų papildinių sąrašas.
1. Sąraše pasirinkite **Atsargų matomumas**.
1. Įveskite šias vertes savo aplinkos laukeliuose:

    - **AAD programos (kliento) ID**
    - **ĮTRAUKITE nuomotojo ID**

    ![Įtraukite į nustatymų puslapį](media/inventory-visibility-setup.png "Papildinio nustatymus puslapis")

1. Sutikite su sąlygomis ir terminais pasirinkę **Sąlygos ir terminai** žymimą laukelį.
1. Pasirinkti **Diegti**. Papildinio būsena bus rodoma kaip **diegiama**. Kai pasibaigs, paleiskite iš naujo puslapį, kad matytumėte būsenos keitimą į **Diegta**.

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a>Papildinio šalinimas

Norėdami išdiegti papildinį, pasirinkite **Išdiegti**. Atnaujinus LCS inventoriaus matomumo papildinys bus panaikintas. Atlikus išdiegimo procesą pašalinama papildinio registracija ir pradedamas darbas siekiant išvalyti visus verslo duomenis laikomus paslaugose.

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a>Turimų atsargų duomenų iš „Supply Chain Management” naudojimas

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Aplinkos matomumo integravimo paketo diegimas

Jei naudojate „Supply Chain Management” 10.0.17 ar senesnę versiją, susisiekite su atsargų matomumo samdymo palaikymo komanda el. paštu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), kad gautumėte paketo failą. Tada įdiekite paketą LCS.

> [!NOTE]
> Jei diegiant įvyksta versijų neatitikimo klaida, turite rankiniu būdu importuoti X++ projektą į savo programavimo aplinką. Tada sukurkite diegiamą paketą savo programavimo aplinkoje ir įdiekite jį savo gamybos aplinkoje.
> 
> Kodas įtrauktas į „Supply Chain Management” 10.0.18 versiją. Jei naudojate tą ar vėlesnę versiją, įdiegti nereikia.

Įsitikinkite, kad šios priemonės yra įjungtos jūsų „Supply Chain Management” aplinkoje. (Numatyta, kad jos yra įjungtos.)

| Funkcijos aprašymas | Kodo versija | Klasės kaitaliojimas |
|---|---|---|
| Atsargų dimensijų naudojimo „InventSum“ lentelėje įjungimas arba išjungimas | 10.0.11 | InventUseDimOfInventSumToggle |
| Atsargų dimensijų naudojimo „InventSumDelta“ lentelėje įjungimas arba išjungimas | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Atsargų matomumo integravimo nustatymas

1. „Supply Chain Management” atidarykite darbo sritį **[Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** ir įjunkite funkciją **Atsargų matomumo integravimas**.
1. Eikite į **Atsargų valdymas \> Nustatymas \> Atsargų matomumo integravimo parametrai** ir įveskite aplinkos, kurioje paleidžiamas atsargų matomumas, URL.

    Raskite savo LCS aplinkos „Azure“ regioną, o tada įveskite URL. URL forma yra tokia:

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    Pavyzdžiui, jei esate Europoje, jūsų aplinkos URL bus vienas iš šių:

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    Šiuo metu naudojami nurodyti regionai.

    | „Azure“ regionas | Trumpas regiono pavadinimas |
    |---|---|
    | Rytų Australija | eau |
    | Pietryčių Australija | seau |
    | Centrinė Kanada | cca |
    | Rytų Kanada | eca |
    | Šiaurės Europa | neu |
    | Vakarų Europa | weu |
    | Rytų JAV | eus |
    | Vakarų JAV | wus |

1. Eikite į **Atsargų valdymas \> Periodinis \> Atsargų matomumo integravimas** ir įjunkite užduotį. Visi atsargų keitimo įvykiai iš „Supply Chain Management” dabar bus užregistruoti atsargų matomumo srityje.

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a>Vieša inventoriaus matomumo API

Vieša REST API inventoriaus matomumo papildinio nustatymuose nurodo kai kuriuos integravimo galutinius taškus. Jis palaiko tris pagrindines sąveikos rūšis:

- Turimų atsargų pakeitimų į papildinio formą išorės sistemoje registravimas
- Dabartinių turimų kiekių užklausos iš išorės sistemos
- Automatinis sinchronizavimas su turimomis „Supply Chain Management“ atsargomis.

Automatinis sinchronizavimas nėra viešosios API dalis. Vietoje to jis tvarkomas fone, aplinkoms, kuriose įjungtas atsargų matomumo priedas.

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Autentifikavimas

Platformos saugos atpažinimo ženklas naudojamas atsargų matomumo priedui iškviesti. Todėl turite sugeneruoti *„Azure Active Directory“ („Azure AD“) atpažinimo ženklą*, naudodami savo „Azure AD“ programą. Tada turite naudoti „Azure AD“ atpažinimo ženklą, kad iš saugos tarnybos gautumėte *prieigos atpažinimo ženklą*.

Gaukite saugos paslaugų žymą atlikdami šiuos veiksmus:

1. Prisijunkite prie „Azure” portalo ir naudokite jį rasti `clientId` ir `clientSecret` jūsų „Supply Chain Management” programai.
1. Iškvieskite „Azure Active Directory” atpažinimo ženklą (`aadToken`) pateikdami HTTP užklausą su šiomis ypatybes:
    - **„URL”** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **Metodas** - `GET`
    - **Teksto turinys (formos duomenys)**:

        | raktas | vertė |
        | --- | --- |
        | „client_id” | „${aadAppId}“ |
        | „client_secret” | „${aadAppSecret}“ |
        | „grant_type” | „client_credentials” |
        | ištekliai | „0cdb527f-a8d1-4bf8-9436-b352c68682b2“ |
1. Turėtumėte gauti `aadToken` kaip atsakymą, panašų į šį pavyzdį.

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "expires_on": "1610466645",
        "not_before": "1610462745",
        "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. Suformuluokite JSON užklausą, panašią į šią:

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    Kur:
    - Reikšmė `client_assertion` turi būti `aadToken`, kurį gavote ankstesniame veiksme.
    - Reikšmė `context` turi būti aplinkos ID, kuriame norite diegti papildinį.
    - Nustatykite visas kitas reikšmes, kaip parodyta pavyzdyje.

1. Pateikite HTTP užklausą su šiomis ypatybes:
    - **„URL”** - `https://securityservice.operations365.dynamics.com/token`
    - **Metodas** - `POST`
    - **HTTP antraštė** – įtraukite API versiją (raktas yra `Api-Version` ir reikšmė yra `1.0`)
    - **Teksto turinys** – įtraukite JSON užklausą, kurią sukūrėte ankstesniu veiksmu.

1. Gausite  `access_token` atsakyme. Dėl to jums reikia geresnės žymos siekiant iškviesti inventoriaus papildinio API. Toliau pateikiamas pavyzdys.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a>Užklausos pavyzdys

Jūsų nuorodai, čia yra http užklausos pavyzdys, jūs galite naudoti bet kokius įrankius ar kodavimo kalbą šiai užklausai išsiųsti, pavyzdžiui ``Postman``.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a>Konfigūruoti Inventoriaus matomumo vieša API

Prieš naudodami paslaugas, turite užbaigti konfigūravimus aprašytus tolesniuose poskyriuose. Konfigūravimas gali skirtis priklausomai nuo jūsų aplinkos išsamios informacijos. Jis iš esmės turi keturias dalis:

- [Dalijimas](#partitioning)
- [Dimensijos konfigūravimai](#dimension-configurations)
- [Indeksavimas](#indexing)
- [Tinkintas matavimas](#custom-measurement)

#### <a name="partitioning"></a>Dalijimas

Dalijimas gali stipriai paveikti matomumo papildinio veikimą. Gera mintis būtų nustatyti schemą, kuri leidžia mažoms duomenų grupėms veikti vis dar leidžiant svarbias duomenų užklausa.

Visuomet `organizationId` (`dataAreaId` „Supply Chain Management“) bus dalijimo dalis ir pagal nutylėjimą papildinys nustatytas į dimensijų dalijimą kaip *Saitas + Vieta*. Tai reiškia, kad paslaugos turi būti visuomet laukiamos su šia dimensija filtruose.

> [!NOTE]
> *Saitas* ir *Vieta* yra dvi pagrindinės dimensijos inventoriaus matomume. „Supply Chain Management“ dimensijos yra vadinamos *Saitas* (`InventSiteId`) ir *Sandėlis* (`InventLocationId`)

### <a name="dimension-configurations"></a>Dimensijos konfigūravimai

Inventoriaus matomumas suteikia pagrindinių numatytų dimensijų sąrašą siekiant integruoti kelis sistemos išteklius.

Tolesnė lentelė pateikia inventoriaus dimensijas, kurios bus numatytieji vardai inventoriaus papildinyje.

| Dimensijos tipas | Dimensijos pavadinimas |
|---|---|
| Produktas | `ColorId` |
| Produktas | `SizeId` |
| Produktas | `StyleId` |
| Produktas | `ConfigId` |
| Sekimas | `BatchId` |
| Sekimas | `SerialId` |
| Buvimo vieta | `LocationId` |
| Buvimo vieta | `SiteId` |
| Inventoriaus būsena | `StatusId` |
| Sandėliui konkretus | `WMSLocationId` |
| Sandėliui konkretus | `WMSPalletId` |
| Sandėliui konkretus | `LicensePlateId` |

> [!NOTE]
> Dimensijos tipas įrašytas ankstesnėje lentelėje tik nuorodų tikslais. Jums nereikia nustatyti dimensijos tipo inventoriaus matomume.

Jei tinkinta dimensija yra ir jai reikia patekti į eigą į numatytąją vertę, kai suvartojama inventoriaus matomume, ją galite konfigūruoti **TInkinta dimensija** pavadinime inventoriaus matomume.

Išorės sistemos prieiga prie „Inventory Visibility“ per RESTful API, kurios leidžia turėti informaciją pagal suteiktus laukiančius dimensijų rinkinius. Dėl integravimo inventoriaus matomumas jums leidžia konfigūruoti *išorės kanalo duomenų šaltinį* ir šaltinio nurodymą *tikslinis nurodymas* inventoriaus matomume.

Tikslines nurodymas turi būti vienas iš:

- Numatyti Inventoriaus matomumo nurodymai
- Pasirinktinės dimensijos

Nurodymo konfigūravimo tikslas yra standartizuoti daugelio sistemų integravimą užklausai dimensijose ir publikuoti įvykį su dimensijomis.

#### <a name="indexing"></a>Indeksavimas

Didžiąją laiko dalį, inventoriaus turima užklausa nebus tik aukščiausia „bendra“ reikšmė, bet galite matyti rezultatus apibendrintus pagal inventoriaus nurodymus.

Inventoriaus matomumas suteikia lankstumo ir leidžia jums nustatyti indeksavimą, kurie paremti nurodymu ir jų deriniu.

> [!NOTE]
> Šiuo metu galite konfigūruoti indeksu iki daugiausiai penkių. Turite atsargiai apgalvoti, kurie nurodymai ar derinys bus naudojamas siekiant įdiegti užtikrinant, kad atitiks jis jūsų verslo poreikius. Pavyzdžiui, jei norite laukti produktų tokia tvarka:

- Laukti bendrintų produktų turimų *Spalva* ir *Dydis* nurodymuose.
- Kai kada norite tik laukti produkto bendrai.

Turite du indeksus nustatytus kaip:

- `["ColorId", "SizeId"]`
- `[]`

Tuštinkite skliaustelius pagal produkto ID su dalijimu.

Indeksavimas nustato, kaip galite grupuoti savo rezultatus pagal `groupBy` laukimo nustatymus. Tokiu atveju, jei nenustatėte jokių `groupBy` verčių, gausite bendrus `productid`. Kitaip, jei nustatėte `groupBy` kaip `groupBy=ColorId&groupBy=SizeId`, gausite padaugintas eilutes grąžintas pagal kitą spalvą ir dydžio derinius sistemoje.

Galite padėti savo laukimo kriterijus pagal būtiną tekstą.

Čia yra pavyzdys laukimui gaminiui su spalvos ir dydžio deriniu.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

Šiuo metu iš lauko `filters` tik `ProductId` palaiko kelias reikšmes. Jei `ProductId` yra tuščias masyvas, bus pateiktos visų produktų užklausos.

#### <a name="custom-measurement"></a>Tinkintas matavimas

Numatytieji matavimo kiekiai yra siejami su „Supply Chain Management”. Tačiau gali reikėti kiekio, kuris būtų pagamintas iš numatytųjų matavimų kombinacijos. Tam, turite turėti tinkintų kiekių konfigūravimą, kuris bus įtrauktas į išvesties turimas užklausas.

Ši funkcija paprasčiausiai leidžia jums nustatyti priemonės rinkinį, kuris bus įtrauktas ir (arba) nustatys priemones išimtas siekiant suformuoti tinkintą priemonę.

Pavyzdžiui, tolesnė laukimo sąlygas, ji konfigūruos tinkintų priemonių kiekį kaip `MyCustomAvailableforReservation` tam, kad būtų suvartota vartojimo sistemos.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| Vartojimo sistema | Skaičiuotos priemonės | Duomenų šaltinis | Keitikas | Keitiko apskaičiavimo tipas |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | Priedas |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | Priedas |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | Atimtis |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | Priedas |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | Atimtis |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | Priedas |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | Priedas |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | Atimtis |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | Atimtis |

Su tuo, laukimas tinkinto matavimo kiekyje grįš į tolesnę išvestį.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Išvestis `MyCustomAvailableforReservation` paremta apskaičiavimo nustatymais tinkintuose matavimuose:  
 *100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*

### <a name="posting-on-hand-changes"></a>Turimų keitimų publikavimas

Tikslus URL, į kurį bus publikuojamas įvykis bus publikuojamas priklausomai nuo geografinio regiono. Jo forma bus:

`https://{serviceURL}/api/environment/{environmentId}/onhand`

Kai jis autentifikuotas, šis URL gali būti naudojamas kartu su HTTP `POST` metodu, kad siųstumėte turimus keitimo įvykius į paslaugas.

Konkreti antraštė naudojamas siekiant pranešti su „Dynamics 365“ paslaugomis per HTTP užklausas nustatant aplinkos ID „Supply Chain Management“ elemento duomenis su juo susietais. Pvz.:

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a>Publikavimo turimų keitimų laukimo pavyzdys 1

Šis pavyzdys rodo scenarijų, kai jau nustatėte dimensijos konfigūravimą „Power Apps“.

Naudokite tolesnę užklausą norėdami konfigūruoti dimensijos žemėlapį „Power Apps“:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Atsiminkite, kad galite nustatyti `dimensionDataSource` ir naudoti tinkintas dimensijas savo užklausose. Sistema automatiškai pavers tinkintas dimensijas į pagrindines.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a>Publikavimo turimų keitimų laukimo pavyzdys 2

Pavyzdys rodo scenarijų, kuriame jokie žemėlapiai nenustatyti dimensijos konfigūravimui „Power Apps“, todėl publikavimas taip pat turi naudoti pagrindinę dimensiją. Visos dimensijos turi būti pagrindinės, kai  `dimensionDataSource` laukelis yra nulio reikšmės, tuščias ar balta erdvė.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a>JSON dokumento laukelio ypatybės

Laukeliai iš JSON užklausų pavyzdžių, pateikti anksčiau turi ypatybes išvardytas tolesnėje lentelėje.

| Lauko ID | aprašymas |
|---|---|
| `id` | Unikalus ID konkrečiam keitimo įvykiui. Šis ID naudojamas siekiant užtikrinti, kad jei komunikacija su paslaugomis nepavyksta publikavimo metu, pakartotinis pateikimo įvykis nevyks tame pačiame taške sistemai skaičiuojant dukart. |
| `organizationId` | Organizacijos identifikatorius susietas su įvykiu. Tai patalpina „Supply Chain Management“ organizacijas ar duomenų srities ID. |
| `productId` | Aptariamas produkto identifikatorius. |
| `quantity` | Kiekis, pagal kurį turimi poreikiai keičiami. Jeigu, pavyzdžiui, 10 naujų riestainių buvo įtraukti į lentyną, vertė yra 10. Jei 3 riestainiai buvo pašalinti nuo lentynos ar parduoti, ši vertė bus -3. |
| `dimensionDataSource` | Duomenų šaltinio dimensijų naudojimas publikavimo keitimo įvykyje ir eilėje. Jei nurodėte duomenų šaltinį, galite naudoti tinkintas dimensijas iš konkretaus duomenų šaltinio. Su dimensijos konfigūravimu, inventoriaus matomumas gali žymėti tinkintas dimensijas į bendras nustatytas dimensijas. Jei `dimensionDataSource` nenurodyta, galite tik naudoti bendras numatytąsias dimensijas savo eilėse.   |
| `dimensions` | Dinaminis rakto maišas/verčių poros. Jos nustatys keletą dimensijų „Supply Chain Management“, tačiau galite taip pat įtraukti tinkintas dimensijas (tokias kaip *Šaltinis*), kurios nustatys, ar įvykis ateina iš „Supply Chain Management“ ar išorės sistemos. |

### <a name="querying-current-on-hand"></a>Esamas turimas laukimas

Laukimo galutinis taškas esamame turimame bus panašus URL:

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

Jis bus laukiamas su HTTP `POST` metodu.

#### <a name="current-on-hand-query-example-1"></a>Esamas turimas laukimo pavyzdys 1

Šis pavyzdys rodo scenarijų, kai jau turite baigtą dimensijos konfigūravimą „Power Apps“.

Naudokite tolesnę užklausą norėdami konfigūruoti dimensijos žemėlapį „Power Apps“:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Atsiminkite, kad galite nustatyti `dimensionDataSource` ir naudoti tinkintas dimensijas savo užklausose. Sistema automatiškai pavers tinkintas dimensijas į pagrindines. Galite nustatyti `DimensionDataSource` esančius `filters` ir nurodyti tinkintas dimensijas tiek `filters` , tiek ir `groupByValues`. Sistema automatiškai pavers tinkintas dimensijas į pagrindines.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a>Esamas turimas laukimo pavyzdys 2

Pavyzdys rodo scenarijų, kuriame jokie žemėlapiai nenustatyti dimensijos konfigūravimui „Power Apps“, todėl publikavimas taip pat turi naudoti pagrindinę dimensiją. Visos dimensijos turi būti pagrindinės, kai `dimensionDataSource` laukelis skyriuje `filters` yra nulio reikšmės, tuščias ar balta erdvė.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a>Grįžtamojo rezultato pavyzdys

Laukimas rodomas ankstesniuose pavyzdžiuose gali grįžti kaip rezultatas.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Pastebėkite, kad kiekių laukeliai yra struktūruoti kaip priemonių žodynas ir su jomis susijusios vertės.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
