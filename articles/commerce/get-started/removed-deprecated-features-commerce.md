---
title: Pašalintos arba nebenaudojamos „Dynamics 365 Commerce“ funkcijos
description: Šiame straipsnyje aprašomos priemonės, kurios buvo pašalintos arba suplanuotos pašalinti Dynamics 365 Commerce.
author: josaw1
ms.date: 08/23/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 59ffcc00d67f6538980dec8965f894eb51f7230d
ms.sourcegitcommit: 649f1db26da8f20602f11180fc565b7c59eaf545
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337602"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Pašalintos arba nebenaudojamos „Dynamics 365 Commerce“ funkcijos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomos priemonės, kurios buvo pašalintos arba suplanuotos pašalinti Dynamics 365 Commerce.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- Pasenusi *funkcija nėra* aktyvi ir gali būti pašalinta ateityje į atnaujinimą.

Šis sąrašas skirtas suteikti jums informacijos apie pašalintas ir nebenaudojamas funkcijas, kad galėtumėte geriau planuoti savo darbą. 

> [!NOTE]
> Išsami informacija apie finansų ir operacijų programėlių objektus pateikta techninės [nuorodos ataskaitose](/dynamics/s-e/). Galite palyginti skirtingas šių ataskaitų versijas ir sužinoti apie objektus, kurie buvo pakeisti ar pašalinti kiekvienoje finansų ir operacijų programėlių versijoje.

## <a name="features-removed-or-deprecated-in-the-commerce-10029-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Commerce“ 10.0.29 versijoje

### <a name="commerce-parameters-setting---allow-price-adjustments-to-increase-product-price"></a>"Commerce" parametrų nustatymas – leisti koreguoti kainą, kad būtų padidinta produkto kaina

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Turėjome šį parametrą kontroliuoti, ar kainos koregavimo funkcija leidžia padidinti produkto kainą. Kai šis parametras išjungtas, naudojant kainos koregavimo funkcijos organizacijas galima nustatyti tik produkto vieneto kainą, mažesnę nei jo bazinė kaina ir prekybos sutarties pardavimo kaina. Nustatome šio parametro nusidėvėjimą, nes kainos koregavimo funkcija buvo atnaujinta, kad palaikytumėte dviaigius koregavimus (padidėjimą arba sumažėjimą) langelyje. |
| **Pakeitė kita funkcija?**   | Ne |
| **Paveiktos produkto sritys**         | Kainodara ir nuolaidos |
| **Visuotinio diegimo parinktis**              | Viskas |
| **Būsena**                         | Pasenusi: numatyta, kad šis parametras įjungtas, nes "Commerce" versija 10.0.29 yra pašalinta 2023 m. spalio mėn. |

### <a name="commerce-parameters-setting---enable-price-report-for-retail-store"></a>"Commerce" parametrų nustatymas – įgalinti parduotuvės kainos ataskaitą

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Turėjome šį parametrą kontroliuoti, ar kainos ataskaitos funkciją galima naudoti parduotuvės konfigūravimo formoje. Nustatome šio parametro nusidėvėjimą, nes parduotuvės konfigūravimo forma buvo atnaujinta taip, kad visada būtų galima naudoti kainos ataskaitos funkciją kaip standartinę funkciją. |
| **Pakeitė kita funkcija?**   | Ne |
| **Paveiktos produkto sritys**         | Kainodara ir nuolaidos |
| **Visuotinio diegimo parinktis**              | Viskas |
| **Būsena**                         | Pasenusi: šis parametras bus pašalintas 2023 m. spalio mėn. |

### <a name="commerce-parameters-setting---use-todays-date-to-calculate-prices"></a>"Commerce" parametrų nustatymas – skaičiuojant kainas naudoti šiandienos datą

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Tiekimo grandinės valdymo (SCM) kainodaros sistema palaiko kainų skaičiavimą, pagrįstą pageidaujama siuntimo data arba pageidaujama gavimo data, kartu su šiandienos data. "Commerce" kainodaros modulis palaiko tik kainos skaičiavimą, pagrįstą šiandienos data. Klientams, kurie naudoja ir SCM, ir "Commerce" galimybes, pateikėme šį parametrą ir rekomenduojama, kad klientai visada jį nustatytų kaip "Taip **",** kad du kainų klientai galėtų veikti kartu. Nustatome šio parametro nusidėvėjimą, nes jis nekeičia skaičiavimo veikimo būdo ir yra perteklinis. |
| **Pakeitė kita funkcija?**   | Ne |
| **Paveiktos produkto sritys**         | Kainodara ir nuolaidos |
| **Visuotinio diegimo parinktis**              | Viskas |
| **Būsena**                         | Pasenusi: numatyta, kad šis parametras įjungtas, nes "Commerce" versija 10.0.29 yra pašalinta 2023 m. spalio mėn. |

## <a name="feature-deprecation-effective-july-2022"></a>Priemonės pasenusios 2022 m. liepos mėn.

### <a name="commerce-analytics-preview"></a>„Commerce“ analizė (peržiūros versija)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Komanda Dynamics 365 Commerce išanalizvo "Commerce analytics" (Peržiūra) priemonės naudojimą ir naudojimą, be to, buvo priimtas sprendimas daugiau nebesikelti į priekį ir nustatyti funkciją bendro užimtumo.   |
| **Pakeitė kita funkcija?**   | Šiuo metu "Commerce analytics" (Peržiūra) nebus pakeista kita funkcija ar sprendimas. Neapdorotų operacijų ir pagrindinių duomenų eksportavimas iš finansų ir operacijų programėlių į "Azure Data Pvm" išlieka pasiekiamas, [kaip paaiškinta finansų ir operacijų programėlių eksportavime į duomenis](../../fin-ops-core/dev-itpro/data-entities/finance-data-azure-data-lake.md). Partneriai ir klientai gali sverti, kad duomenų srautas kuriamas pagal verslo poreikius skirtas analizės ataskaitas.
| **Paveiktos produkto sritys**         | „Commerce“ analizė (peržiūros versija) |
| **Visuotinio diegimo parinktis**              | Viskas |
| **Būsena**                         | Ieškome šios priemonės išjungti iki 2022 metų rugpjūčio 30 d.  Nuo šios datos į priekį nebus atnaujinama dabartinėse ataskaitose, kurią Power BI pateikė "Commerce analytics" (peržiūra).     |

## <a name="features-removed-or-deprecated-in-the-commerce-10021-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Commerce“ 10.0.21 versijoje

[!include [banner](../includes/preview-banner.md)]

### <a name="overlapping-discounts-handling-setting-in-commerce-parameters"></a>Iš dalies sutampančių nuolaidų tvarkymo parametras „Commerce" parametruose

„Commerce" **Persidengiančių nuolaidų tvarkymi** nustatymų **„Commerce“ parametrai** puslapis nebegalioja „Commerce“ versijoje 10.0.21. Eja į priekį „Commerce pricing engine" naudos vieną algoritmą, kad nustatytų optimalų persidengiančių nuolaidų derinį.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo / pašalinimo priežastis** | <p>„Commerce" parametruose **esantis persidengiančių nuolaidų** nustatymai „Commerce“ parametruosi valdiklis, kaip „Commerce“ kainų variklis ieško ir nustato pasirinktinas persidengiančių nuolaidų derinius. Šiuo metu jis siūlo tris pasirinktis:<p><ul><li> **Geriausias našumas** – ši pasirinktis naudoja išplėstinį heuristikos algoritmą ir [ribinės vertės vertinimo](../optimal-combination-overlapping-discounts.md) metodą, siekiant nustatyti prioritetą, įvertinti ir nustatyti geriausią nuolaidų kombinaciją laiku.</li><li>**Subalansuotas skaičiavimas** – dabartinio kodo pagrindu ši pasirinktis veikia kaip ir **našumo našumo** pasirinktis. Todėl iš esmės tai yra pasikartojanti pasirinktis.</li><li>**Išsamus skaičiavimas** – ši pasirinktis naudoja seną algoritmą, kuris kainų skaičiavimo metu naudoja visas galimas nuolaidų kombinacijas. Užsakymams, kurie turi dideles eilutes ir kiekius, ši pasirinktis gali sukelti našumo problemų.</li></ul><p>Norėdami palengvinti konfigūravimą, pagerinti našumą ir sumažinti seno algoritmo sukeliamus incidentus, **visiškai pašalinsime persidengiančių nuolaidų tvarkymo parametrą ir atnaujinsime vidinę Komercijos kainodaros modulio logiką, kad dabar būtų naudojamas tik išplėstinis algoritmas (t. t. algoritmas,** **esantis** be geriausios našumo pasirinkties).</p> |
| **Pakeitė kita funkcija?**   | Ne. Rekomenduojame organizacijoms, kurios naudoja **subalansuotų skaičiavimų** ar **išsamių skaičiavimų** pasirinktį pakeisti į parinktį **Geriausias našumas** prieš panaudoant šią funkciją. |
| **Paveiktos produkto sritys**         | Kainodara ir nuolaidos |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Kaip 10.0.21 leidimą **persidengiančių nuolaidų valdymo** parametras bus pašalintas iš „Commerce" parametrų 2022 m. spalio mėn. |

### <a name="retail-sdk-distributed-by-using-lifecycle-services"></a>"Retail" SDK paskirstyta naudojant „Lifecycle Services“

"Retail SDK" pristatoma „Lifecycle Services“ (LCS). Šis paskirstymo režimas pasenusis išleidžiant 10.0.21. O taip, „Retail SDK" nuorodų paketai, bibliotekos ir pavyzdžiai bus publikuojami GitHub viešose saugyklose.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo / pašalinimo priežastis** | „Retail SDK" pristatoma LCS. LCS procesas užtrunka keletą valandų, todėl procesas turi būti kartojamas naudojant kiekvieną naujinimą. O taip, „Retail SDK" nuorodų paketai, bibliotekos ir pavyzdžiai bus publikuojami GitHub viešose saugyklose. Plėtinių pavyzdžiai ir nuorodų pakuotės gali būti nesunkiai suvartojami, o atnaujinimas baigiamas po kelių minučių. |
| **Pakeitė kita funkcija?**   |  [Atsisiųsti „Retail SDK“ pavyzdžius ir nuorodos paketus iš GitHub bei NuGet](../dev-itpro/retail-sdk/sdk-github.md) |
| **Paveiktos produkto sritys**         | Mažmeninės prekybos SDK |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Pasenusi: nuo 10.0.21 leidimo SDK, išsiųstas per LCS VMs, bus pašalintas 2023 m. spalio mėn. |

### <a name="retail-deployable-package-and-combined-pos-hardware-station-and-cloud-scale-unit-installers"></a>"Retail" diegiamas paketas ir sujungti EKA, "Hardware" stotis ir debesies skalės vienetų diegimo programos

Mažmeninės prekybos diegiami paketai, sugeneruoti naudojant „Retail SDK MSBuild", pasenusi 10.0.21. Tęskite toliau, naudodami debesies skalės vieneto (CSU) paketą debesies svarstyklių plėtinams (, kanalų duomenų bazei, begalutinių komercijos API, mokėjimams ir pardavimo debesies taškams „Commerce Runtime“ (EKA)). Naudokite tik plėtinio diegimo programas, skirtas EKA, "Hardware" stotis ir debesies skalės vienetui.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo / pašalinimo priežastis** | "Retail" diegiamas paketas yra sujungtas paketas, kuriame yra visas plėtinių paketų ir diegimo priemonių rinkinys. Šis sujungtas paketas tampa sudėtingas, nes CSU plėtiniai pereis į debesies skalės vienetą ir diegimo programos bus įdiegtos parduotuvėse. Diegimo programos apima plėtinį ir pagrindinį produktą, dėl to naujinimai yra sudėtingi. Kiekvieną kartą atnaujinus reikia sukurti kodų suliejimą ir pakuotės yra generuojamos. Siekiant supaprastinti šį procesą, plėtiniai paketai atskiriami į komponentus, kad būtų lengviau diegti ir valdyti. Naudojant naują būdą, plėtiniai ir pagrindiniai produktų diegimo programos yra atskiriami ir gali būti nepriklausomai aptarnaujami ir atnaujinti be kodų suliejimo arba perpakavimo.|
| **Pakeitė kita funkcija?**   | CSU plėtiniai, EKA plėtinių diegimo programos, aparatūros stoties plėtinių diegimo programos |
| **Paveiktos produkto sritys**         | „Dynamics 365 Commerce“ plėtinių paketas ir diegimas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Pasenusi: kaip 10.0.21 leidimo versija, LCS "RetailDeployablePackage" diegimo palaikymas bus pašalintas 2022 m. spalio mėn. |

Daugiau informacijos, žr.:

+ [Generuoti atskirą „Commerce Cloud Scale Unit" (CSU) paketą](../dev-itpro/retail-sdk/retail-sdk-packaging.md#generate-a-separate-package-for-commerce-cloud-scale-unit-csu)
+ [„Modern POS“ plėtinių paketo kūrimas](../dev-itpro/pos-extension/mpos-extension-packaging.md)
+ [EKA integravimas su nauju aparatūros įrenginiu](../dev-itpro/hardware-device-extension.md)
+ Kodo pavyzdžiai
    + [„Cloud Scale Unit“](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit)
    + [POS, CSU ir Hardware stotis](https://github.com/microsoft/Dynamics365Commerce.InStore)

### <a name="modernpossln-and-cloudpossln-in-the-retail-sdk"></a>ModernPos.Sln ir CloudPos.sln mažmeninės prekybos SDK

EKA plėtinio kūrimas naudojant ModernPos.sln, CloudPos.sln, EKA. Extension.csproj ir EKA aplankas yra pasenusias leidime 10.0.21. Tęskite toliau, naudokite nuo EKA nepriklausomos pakuotės SDK, skirtą EKA plėtinių.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo / pašalinimo priežastis** | Naudojant ankstesnes "Retail SDK" versijas, jei yra EKA plėtinių, norint atnaujinti į naujausią EKA versiją reikia sulieti kodus ir iš naujo supakuoti. Kodų suliejimas užims daug laiko reikalaujaį atnaujinimo procesą, o jūs turėjote saugykloje tvarkyti visą "Retail SDK". Taip pat turėjote sukompiliuoti POS.App projektas. Naudodami nepriklausomą pakavimo modelį, turite prižiūrėti tik savo plėtinį. Atnaujinant į naujausią EKA plėtinių versiją, nes taip paprasta atnaujinti paketo versiją, „NuGet“ kurią naudoja jūsų projektas. Plėtinius galima įdiegti nepriklausomai, o tarnybos naudoja plėtinių diegimo įdiegtis. Pagrindinį EKA galima įdiegti ir prižiūrėti atskirai, be to, nereikia jokio kodų suliejimo ar perpakavimo su pagrindinės diegimo programos ar kodo. |
| **Pakeitė kita funkcija?**   | [EKA nepriklausomo paketo SDK](../dev-itpro/pos-extension/pos-extension-getting-started.md) |
| **Paveiktos produkto sritys**         | „Dynamics 365 Commerce“ EKA plėtinių paketas ir diegimas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Pasenusi: išleidus 10.0.21 versiją, palaikomi sujungti EKA paketai ir plėtinio modelis naudojant ModernPos.Sln, CloudPOs.sln ir EKA. "Retail SDK" extensons.csproj bus pašalintas 2023 m. spalio mėn. |

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Commerce“ 10.0.17 versijoje

### <a name="full-dataset-generation-interval-is-deprecated"></a>Visas duomenų rinkinio kūrimo intervalas nebegalioja

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Pradėdami šiame leidime, **„Commerce“ grafiko kūrimo parametrai** formoje „Dynamics 365“ būstinėje, laukelis **Visas duomenų rinkinio kūrimo intervalas dienomis** nebegalios. Laukas taip pat paleidžiamas šiame leidime, todėl laukas bus vizuališkai pašalintas, kad vertės būtų galima redaguoti. Vertė liks **0**. |
| **Pakeitė kita funkcija?**   | Ne |
| **Paveiktos produkto sritys**         | Dynamics 365 Commerce |
| **Visuotinio diegimo parinktis**              | Viskas|
| **Būsena**                         | Nerekomenduojama. Nenaudokite šio lauko arba pakeiskite jo vertę.|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Commerce“ 10.0.15 versijoje

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>„Internet Explorer“ 11 palaikymas „Dynamics 365“ nebegalioja

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Nuo 2020 m. gruodžio „Microsoft Internet Explorer 11“ palaikymas visuose „Dynamics 365“ produktuose yra nutraukiamas, o „Internet Explorer 11“ nebus palaikomas nuo 2021m. rugpjūčio.<br><br>Tai paveiks klientus, kurie naudoja „Dynamics 365“ produktus, skirtus naudoti „Internet Explorer 11“ sąsają. Nuo 2021m. rugpjūčio „Internet Explorer 11“ nebus palaikomas tokiuose „Dynamics 365“ produktuose. |
| **Pakeitė kita funkcija?**   | Rekomenduojame klientams naudoti „Microsoft Edge“.|
| **Paveiktos produkto sritys**         | Visi „Dynamics 365“ produktai |
| **Visuotinio diegimo parinktis**              | Visos|
| **Būsena**                         | Nerekomenduojama. „Internet Explorer 11“ nebus palaikoma nuo 2021 m. rugpjūčio.|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Commerce“ 10.0.11 versijoje
### <a name="data-action-hooks"></a>Duomenų veiksmų trikčių gaudyklės
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Duomenų veiksmų trikčių gaudyklė nebeaktyvi dėl našumo problemų. |
| **Pakeitė kita funkcija?**   | Rekomenduojame naudoti [duomenų veiksmų perrašymus](../e-commerce-extensibility/data-action-overrides.md) verslo logikos duomenų veiksmų sluoksnyje keitimui.|
| **Paveiktos produkto sritys**         | „e-Commerce“ praplėtimo duomenų veiksmai |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: nuo 10.0.11 leidimo. |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Mažmeninės prekybos SDK pagalba „Visual Studio 2015“, msbuild 14.0, ir „Retail SDK“\Referencinės bibliotekos ir įrankiai
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | „Retail SDK“ pagalba „Visual Studio 2015“ buvo panaikinta ir atnaujinta tam, kad padėtų VS 2017, „msbuild 15.0“ ir visas referencines bibliotekas ir komercijos serverio generatoriaus įrankį „RetailSDK“\Referencinį kataloge, kuris buvo perkeltas į „NuGet“ paketus tam, kad būtų palengvintas plėtinio modelis ir SDK pagerinimo procesas.|
| **Pakeitė kita funkcija?**   | Rekomenduojame jums sekti informaciją [Perkelti „Retail SDK“ iš „Visual Studio 2015“ į „Visual Studio 2017“](../dev-itpro/retail-sdk/migrate-sdk.md) savo sistemos atnaujinimui. |
| **Paveiktos produkto sritys**         | „Retail SDK“ plėtiniai |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: nuo 10.0.11 leidimo. |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>„Retail Server Extension“ naudojantis „IEdmModelExtender“ ir „CommerceController“
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | „Retail“ serverio plėtinys naudojantis „IEdmModelExtender“ ir „CommerceControllerׅ“ buvo pašalintas tam, kad būtų pateiktas supaprastintas plėtinio modelis. Naujoji versija turės tik valdiklio klasę be papildomo „IEdmModelExtender“ klasės versijos. Tai taip pat panaikina priklausomybę nuo konkrečios „OData“ versijos (jei „OData“ versija yra atnaujinama, ji gali sugadinti plėtinius.) |
| **Pakeitė kita funkcija?**   |  Rekomenduojame naudoti „IController“ klasės plėtinio modelį importuojant „NuGet“ (Microsoft.Dynamics.Commerce.Hosting.Contracts) paketą. |
| **Paveiktos produkto sritys**         | „Retail“ serverio plėtiniai |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: nuo 10.0.11 leidimo. |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>Kompiuterinės įrangos stoties plėtinys naudojantis „IHardwareStationController“
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Kompiuterinės įrangos plėtinys naudojantis „IHardwareStationController“ buvo pašalintas tam, kad būtų pateiktas supaprastintas plėtinio modelis. Naujos versijos turės tik „IController“ klasę be jokios papildomos klasės versijos ir taip bus išvengta priklausomybės nuo pagrindinių kompiuterinės įrangos stoties bibliotekų, nes ankstesnis plėtinys turėjo remtis keliomis bibliotekomis.) |
| **Pakeitė kita funkcija?**   | Rekomenduojama naudoti IController NuGet klasės plėtinio modelį importuojant paketą (Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **Paveiktos produkto sritys**         | Kompiuterinės įrangos stoties plėtiniai |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: nuo 10.0.11 leidimo. |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Commerce“ 10.0.10 versijoje
### <a name="pos-operation-803---picking-and-receiving"></a>EKA 803 operacija – paėmimas ir gavimas
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Operacijų paėmimas ir gavimas nebenaudojamas dėl naujos operacijų pertvarkos. |
| **Pakeitė kita funkcija?**   | Taip. Jis pakeistas dviem naujomis EKA operacijomis: gavimo operacija (804) ir siuntimo operacija (805).|
| **Paveiktos produkto sritys**         | Elektroninio kasos aparato (EKA) programa |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: nuo 10.0.10 versijos išleidimo paėmimo ir gavimo operacijos nebegaus naujų funkcijų naujinimų. Būsimuose leidimuose bus atliktos tik kritinių operacijos klaidų pataisos. Visi klientai skatinami pereiti prie naujų [gaunamų operacijų](../pos-inbound-inventory-operation.md) ir [siunčiamų operacijų](../pos-outbound-inventory-operation.md), kurios ir toliau bus mūsų ilgalaikio produktų veiksmų plano dalis. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Commerce“ 10.0.7 versijoje
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Komercijos GetProductAvailabilities ir GetAvailableInventoryNearby APIs
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Buvo sukurtos naujos optimizuotos API, kad pakeistų GetProductAvailabilities ir GetAvailableInventoryNearby API. |
| **Pakeitė kita funkcija?**   | Taip: jį pakeitė GetEstimatedAvailability ir GetEstimatedProductWarewareavailability APIs. |
| **Paveiktos produkto sritys**         | „e-Commerce“ programos SDK |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: nuo 10.0.7 versijos išleidimo nebebus GetProductAvailabilities ir GetAvailableInventoryNearby inžinerinių investicijų. Organizacijos, naudojančios šias API „e-Commerce“ diegimuose, turėtų konvertuoti į naujas GetEstimatedAvailability ir GetEstimatedProductWarehouseAvailability API ir įjungti [funkciją Optimizuotas produkto pasiekiamumo skaičiavimas](../calculated-inventory-retail-channels.md).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Ankstesni pranešimai apie pašalintas arba nebenaudojamas funkcijas
Norėdami sužinoti daugiau apie funkcijas, kurios buvo pašalintos arba nebenaudojamos ankstesniuose leidimuose, žr. skyrių [Ankstesniuose leidimuose pašalintos arba nebenaudojamos funkcijos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

