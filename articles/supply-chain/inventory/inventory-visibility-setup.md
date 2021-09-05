---
title: Atsargų matomumo nustatymas
description: Ši tema aprašo, kaip įdiegti ir konfigūruoti inventoriaus matomumo papildinį „ Microsoft Dynamics 365 Supply Chain Management“.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 8573fe01abb1c6092012baf85e8b7df40b74a31f
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343589"
---
# <a name="set-up-inventory-visibility"></a>Atsargų matomumo nustatymas

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Ši tema aprašo, kaip įdiegti ir konfigūruoti inventoriaus matomumo papildinį „ Microsoft Dynamics 365 Supply Chain Management“.

Jums būtina naudoti „Microsoft Dynamics Lifecycle Services“ (LCS) siekiant įdiegti inventoriaus matomumo papildinį. LCS yra bendradarbiavimo portalas suteikiantis aplinką ir reguliariai naujinamų paslaugų rinkinį, kuris padeda jums valdyti programos gyvavimo ciklą jūsų „finance and operations“ programose.

Dėl daugiau informacijos, žr. [„Lifecycle Services“ ištekliai](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

## <a name="inventory-visibility-prerequisites"></a>Atsargų matomumo išankstinės sąlygos

Prieš jums įdiegiant inventoriaus matomumo papildinį, atlikite šiuos veiksmus:

- Gaukite LCS diegimo projektą su mažiausiai viena patalpinta aplinka.
- Įsitikinkite, kad baigtos būtinosios priedų nustatymo sąlygos, pateikiamos skyriuje Priedų apžvalga buvo patenkintos. Informacijos apie šias būtinąsias sąlygas rasite [Priedų apžvalga](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Atsargų matomumui nereikia dvigubo rašymo susiejimo.
- Kreipkitės į atsargų matomumo produkto komandą el. paštu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), kad gautumėte šiuos tris reikalingus failus:

    - `InventoryServiceApplication.PackageDeployer.zip`
    - `Inventory Visibility Integration.zip` (jei jūsų vykdoma „Supply Chain Management” versija yra ankstesnė nei 10.0.18 versija)

> [!NOTE]
> Šiuo metu palaikomos šalys ir regionai yra Kanada (HOU, ECA), Jungtinės Valstijos (ISPANIJOS, ESS), Europos Sąjunga (NEU, WEU), Jungtinė Karalystė (SUK,VZK) ir Australija (HOU, SEAU).

Jei turite kokių klausimų apie šias būtinąsias sąlygas, susisiekite su papildinio produkto komanda.

## <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>„Dataverse“ nustatymas

Norėdami nustatyti, kad jį būtų galima naudoti su atsargų matomumu, naudokite „package deployer“ įrankį atsargų „Dataverse“ matomumo paketui diegti. Toliau pateikti poskyriai aprašo, kaip užbaigti visas šias užduotis.

> [!NOTE]
> Šiuo metu „Dataverse“ palaikomos tik aplinkos, kurios sukurtos naudojant LCS. Jei jūsų aplinka buvo sukurta kokiu nors kitu būdu (pavyzdžiui, naudojant administravimo centrą) ir jei ji susieta su jūsų „Supply Chain Management“ aplinka, pirmiausia turite susisiekti su atsargų matomumo produktų komanda, kad išspręskite susiejimo „Dataverse“, „Power Apps“ problemą. Galite tada įdiekti Inventoriaus matomumo papildinį.

### <a name="migrate-from-an-old-version-of-the-dataverse-solution"></a>Perkelti iš senos sprendimo „Dataverse“ versijos

Jei įdiegėte senesnę atsargų matomumo sprendimo versiją, norėdami „Dataverse“ atnaujinti versiją, naudokite šias instrukcijas. Galima naudoti du atvejus:

- **1 atvejis:** Jei neautomatiniu būdu „Dataverse“ nustatote importuodami `Inventory Visibility Dataverse Solution_1_0_0_2_managed.zip` sprendimą, atlikite šiuos veiksmus:

    1. Atsisiųsti kitus šiuos tris failus:

        - `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip`
        - `InventoryServiceBase_managed.cab`
        - `InventoryServiceApplication.PackageDeployer.zip`

    1. Importuokite `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip` rankiniu būdu ir `InventoryServiceBase_managed.cab` „Dataverse“ atlikite šiuos veiksmus:

        1. Atidarykite savo „Dataverse“ aplinkos URL.
        1. Atverkite puslapį **Sprendimai**.
        1. Pasirinkite **Importuoti**.

    1. Norėdami diegti paketą naudokite „package deployer“ `InventoryServiceApplication.PackageDeployer.zip` įrankį. Norėdami gauti daugiau instrukcijų, žr. [pakuotės skyrių toliau šioje temoje, naudokite „package deployer“](#deploy-package) įrankį.

- **2 atvejis:** Jei nustatote „Dataverse“ naudojant „package deployer“ įrankį prieš įdiegiant seną `.*PackageDeployer.zip` paketą, atsisiųskite `InventoryServiceApplication.PackageDeployer.zip`, ir atnaujinkite. Norėdami gauti daugiau instrukcijų, žr. [pakuotės skyrių toliau šioje temoje, naudokite „package deployer“ priemonės](#deploy-package) įrankį.

### <a name="use-the-package-deployer-tool-to-deploy-the-package"></a><a name="deploy-package"></a>Norėdami diegti paketą naudokite „package deployer“ priemonės įrankį

1. Įdiekite programavimo įrankius, kaip aprašyta [atsisiuntimo „NuGet“ įrankiuose](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).
1. Atblokuokite `InventoryServiceApplication.PackageDeployer.zip` failą, kurį atsisiųstą iš komandų grupės, atlikite šiuos veiksmus:

    1. Pasirinkite ir palaikykite (arba dešiniuoju pelės mygtuku spustelėkite) įrašą ir pasirinkite **Ypatybės**.
    1. Dialogo lango **Ypatybės** skirtuke **Bendra** suraskite saugos **skyrių** pasirinkite **Atblokuoti** ir taikykite keitimą. Jei skirtuke **Bendra** nėra **saugos** skyriaus, failas neužblokuojamas. Šiuo atveju, atlikite kitą žingsnį.

    ![Atblokuoti atsisiųstą failą](media/unblock-file.png "Atblokuoti atsisiųstą failą")

1. Išskeikite, `InventoryServiceApplication.PackageDeployer.zip` kad rastumėte šiuos elementus:

    - „`InventoryServiceApplication`“ aplankas
    - `[Content_Types].xml` failas
    - `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll` failas

1. Kopijuoti kiekvieną iš šių elementų į `.\Tools\PackageDeployment` katalogą. (Šis katalogas buvo sukurtas, kai įdiegėte programavimo įrankius.)
1. Vykdykite `.\Tools\PackageDeployment\PackageDeployer.exe` ir sekite ekrane pateikiamas instrukcijas, kad importuotumėte sprendimus.

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Įdiekite Inventoriaus matomumo papildinį

Prieš įdiegsdami priedą, užregistruokite programą ir pridėkite kliento slaptažodį Azure Active Directory (Azure AD) pagal savo „Azure" abonementą. Instrukcijų ieškokite Registruoti [programą ir Pridėti kliento](/azure/active-directory/develop/quickstart-register-app) ir [Įtraukti kliento raktą](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Įsitikinkite, kad užsirašėte **Programos (kliento) ID**, **Kliento raktą**, ir **Nuomotojo ID** vertes, nes Jums jų reikės vėliau.

Kai užregistruojate programą ir pridedate kliento slaptą seką, atlikite šiuos veiksmus, kad įdiegtumėte atsargų „Azure AD“ matomumo priedą.

1. Prisijunkite prie [LCS](https://lcs.dynamics.com/Logon/Index).
1. Pagrindiniame puslapyje pasirinkite projektą, kuriame jūsų aplinka talpinta.
1. Projekto puslapyje pasirinkite aplinką, kurioje norite įdiegti papildinį.
1. Aplinkos puslapyje slinkite žemyn, kol pamatysite skyrių **Aplinkos priedai** skyriuje **„Power Platform“ integravimas** skyriuje. Ten galite rasti aplinkos „Dataverse“ pavadinimą.
1. Skyriuje **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.

    ![Aplinkos puslapis LCS](media/inventory-visibility-environment.png "Aplinkos puslapis LCS")

1. Rinkitės **Diegti naują papildinį** nuorodą. Pasirodo esamų atvirų papildinių sąrašas.
1. Sąraše rinkitės **Atsargų matomumas**.
1. Tada nustatykite šiuos laukus savo aplinkai:

    - **AAD programos (kliento) ID** – Įveskite „Azure AD“ programos ID, kurią sukūrėte ir anksčiau užsirašėte.
    - **ADD nuomotojo ID** – Įveskite anksčiau pasižymėtą nuomotojo ID.

    ![Įtraukite į papildinių puslapį](media/inventory-visibility-setup.png "Įtraukite į papildinių puslapį")

1. Sutikite su sąlygomis ir terminais pasirinkę **Sąlygos ir terminai** žymimą laukelį.
1. Pasirinkti **Diegti**. Papildinio būsena bus rodoma kaip **diegiama**. Tada, kai diegimas bus baigtas, paleiskite iš naujo puslapį. Būsena turi pasikeisti į **Įdiegta**.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Išdiekite Inventoriaus matomumo papildinį

Norėdami pašalinti atsargų matomumo priedą, **Išdiegti** LCS puslapyje pasirinkite. Pašalinimo procesas pašalina atsargų matomumo priedą, išregistruojami iš LCS ir panaikinami visi laikini duomenys, saugomi atsargų matomumo duomenų talpykloje. Tačiau pirminiai atsargų duomenys, saugomi jūsų „Dataverse“ abonemente, nėra naikinami.

Norėdami pašalinti savo abonemente saugomus atsargų duomenis, savo „Dataverse“ prenumeratoje atverkite [„Power Apps“](https://make.powerapps.com), rinkitės **Aplinka** naršymo juostoje ir rinkitės „Dataverse“ aplinką, kuri yra susieta su Jūsų LCS aplinka. Tada eikite į **sprendimus** ir panaikinkite šiuos penkis sprendimus:

- Atsargų matomumo programos inkaro sprendimas „Dynamics 365" sprendimuose
- „Dynamics 365" FNO SCM atsargų matomumo programų sprendimas
- Atsargų saugumo konfigūravimas
- Atsargų matomumo atskiras dėmuo
- „Dynamics 365" FNO SCM atsargų matomumo pagrindo sprendimas

Kai panaikinate šiuos sprendimus, duomenys, saugomi lentelėse, taip pat bus panaikinti.

## <a name="set-up-supply-chain-management"></a><a name="setup-dynamics-scm"></a>„Supply Chain Management“ nustatymas

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Aplinkos matomumo integravimo paketo diegimas

Jei naudojate „Supply Chain Management” 10.0.17 ar senesnę versiją, susisiekite su atsargų matomumo samdymo palaikymo komanda el. paštu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), kad gautumėte paketo failą. Tada įdiekite paketą LCS.

> [!NOTE]
> Jei diegiant įvyksta versijų neatitikimo klaida, turite rankiniu būdu importuoti X++ projektą į savo programavimo aplinką. Tada sukurkite diegiamą paketą savo programavimo aplinkoje ir įdiekite jį savo gamybos aplinkoje.
>
> Kodas įtrauktas į „Supply Chain Management” 10.0.18 versiją. Jei naudojate tą ar vėlesnę versiją, įdiegti nereikia.

Įsitikinkite, kad šios priemonės yra įjungtos jūsų „Supply Chain Management” aplinkoje. (Numatyta, kad jos yra įjungtos.)

| Funkcijos aprašymas | Kodo versija | Klasės kaitaliojimas |
|---|---|---|
| Atsargų dimensijų naudojimo „InventSum“ lentelėje įjungimas arba išjungimas      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Atsargų dimensijų naudojimo „InventSumDelta“ lentelėje įjungimas arba išjungimas | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Atsargų matomumo integravimo nustatymas

1. „Supply Chain Management” atidarykite darbo sritį **[Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** ir įjunkite funkciją *Atsargų matomumo integravimas*.
1. Eikite į **Atsargų valdymas \> Nustatymas \> Atsargų matomumo integravimo parametrai** ir įveskite aplinkos, kurioje paleidžiamas atsargų matomumas, URL. Daugiau informacijos žr. [Surasti paslaugų galinį tašką](inventory-visibility-power-platform.md#get-service-endpoint).
1. Eikite į **Atsargų valdymas \> Periodinis \> Atsargų matomumo integravimas** ir įjunkite užduotį. Visi atsargų keitimo įvykiai iš „Supply Chain Management” dabar bus užregistruoti atsargų matomumo srityje.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
