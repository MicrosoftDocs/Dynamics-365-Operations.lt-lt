---
title: Pašalintos arba nebenaudojamos „Dynamics 365 Commerce“ funkcijos
description: Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš „Dynamics 365 Commerce“.
author: josaw
ms.date: 04/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 213ed2091b1f2359f2481b162cba07812b3ffe90
ms.sourcegitcommit: 9e1129d30fc4491b82942a3243e6d580f3af0a29
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2022
ms.locfileid: "8649080"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Pašalintos arba nebenaudojamos „Dynamics 365 Commerce“ funkcijos

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš „Dynamics 365 Commerce“.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nerekomenduojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Šis sąrašas skirtas suteikti jums informacijos apie pašalintas ir nebenaudojamas funkcijas, kad galėtumėte geriau planuoti savo darbą. 

> [!NOTE]
> Išsamią informaciją apie objektus "Finance and Operations" programose galima rasti techninėse informacinėse [ataskaitose](/dynamics/s-e/). Galite palyginti skirtingas šių ataskaitų versijas, kad sužinotumėte apie objektus, kurie pasikeitė arba buvo pašalinti kiekvienoje "Finance and Operations" programų versijoje.

## <a name="features-removed-or-deprecated-in-the-commerce-10025-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Commerce“ 10.0.25 versijoje

### <a name="modern-point-of-sale-mpos"></a>Modernusis elektroninis kasos aparatas (MPOS)

Šiuolaikinės prekybos vietos (MPOS) programa bus nebenaudojama "Commerce" 10.0.25 versijoje ir pakeista "Store Commerce" programa.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Parduotuvėje esančios programos yra daugiakanalio pasiūlymo kertinis Dynamics 365 Commerce akmuo. Mes nuolat diegiame naujoves, kad suteiktume modernią ir išmanią parduotuvių patirtį, o siekdami toliau modernizuoti savo sprendimą, diegiame naujus pakeitimų rinkinius, kurie žymiai pagerins IT operacijas ir naudotojų patirtį naudojant mūsų esamas parduotuvių programas "Windows". Naujoji "Store Commerce" programa yra esamų MPOS technologijų atnaujinimas. Tai užtikrina geresnį našumą, patikimumą ir ilgalaikį palaikymą "Windows" platformoje ir pašalina poreikį perpakuoti programą su kiekvienu atnaujinimu. |
| **Pakeitė kita funkcija?**   |  [„Store Commerce“](../dev-itpro/store-commerce.md) |
| **Paveiktos produkto sritys**         | Šiuolaikinė pardavimo vieta |
| **Visuotinio diegimo parinktis**              | Viskas |
| **Būsena**                         | Nebenaudojama: nuo "Commerce" 10.0.25 versijos išleidimo MPOS diegimo programa, išsiųsta per LCS virtualias mašinas (VM), bus pašalinta 2023 m. Spalio mėn. |

## <a name="features-removed-or-deprecated-in-the-commerce-10021-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Commerce“ 10.0.21 versijoje

[!include [banner](../includes/preview-banner.md)]

### <a name="overlapping-discounts-handling-setting-in-commerce-parameters"></a>Iš dalies sutampančių nuolaidų tvarkymo parametras „Commerce" parametruose

„Commerce" **Persidengiančių nuolaidų tvarkymi** nustatymų **„Commerce“ parametrai** puslapis nebegalioja „Commerce“ versijoje 10.0.21. Eja į priekį „Commerce pricing engine" naudos vieną algoritmą, kad nustatytų optimalų persidengiančių nuolaidų derinį.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo / pašalinimo priežastis** | <p>„Commerce" parametruose **esantis persidengiančių nuolaidų** nustatymai „Commerce“ parametruosi valdiklis, kaip „Commerce“ kainų variklis ieško ir nustato pasirinktinas persidengiančių nuolaidų derinius. Šiuo metu jis siūlo tris pasirinktis:<p><ul><li> **Geriausias našumas** – ši pasirinktis naudoja išplėstinį heuristikos algoritmą ir [ribinės vertės vertinimo](../optimal-combination-overlapping-discounts.md) metodą, siekiant nustatyti prioritetą, įvertinti ir nustatyti geriausią nuolaidų kombinaciją laiku.</li><li>**Subalansuotas skaičiavimas** – dabartinio kodo pagrindu ši pasirinktis veikia kaip ir **našumo našumo** pasirinktis. Todėl iš esmės tai yra pasikartojanti pasirinktis.</li><li>**Išsamus skaičiavimas** – ši pasirinktis naudoja seną algoritmą, kuris kainų skaičiavimo metu naudoja visas galimas nuolaidų kombinacijas. Užsakymams, kurie turi dideles eilutes ir kiekius, ši pasirinktis gali sukelti našumo problemų.</li></ul><p>Norėdami supaprastinti konfigūraciją, pagerinti našumą ir sumažinti incidentus, kuriuos sukėlė senasis algoritmas, visiškai pašalinsime persidengiančių **nuolaidų tvarkymo parametrą** ir atnaujinsime vidinę Komercijos kainodaros modulio logiką, kad dabar būtų naudojamas tik išplėstinis algoritmas (t. t. algoritmas, esantis be **geriausios našumo** pasirinkties).</p> |
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

EKA plėtinių kūrimas naudojant "ModernPos.sln", "CloudPos.sln, POS. Extension.csproj ir EKA aplankas nebenaudojamas 10.0.21 leidime. Tęskite toliau, naudokite nuo EKA nepriklausomos pakuotės SDK, skirtą EKA plėtinių.

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
| **Nebenaudojimo/pašalinimo priežastis** | Pradėdami šiame leidime, **„Commerce“ grafiko kūrimo parametrai** formoje „Dynamics 365“ būstinėje, laukelis **Visas duomenų rinkinio kūrimo intervalas dienomis** nebegalios. Taip pat nuo šio leidimo laukelis bus vizualiai pašalintas taip, kad vertės keisti nepavyks. Vertė liks **0**. |
| **Pakeitė kita funkcija?**   | Ne |
| **Paveiktos produkto sritys**         | „Dynamics 365 Commerce” |
| **Visuotinio diegimo parinktis**              | Visos|
| **Būsena**                         | Nebenaudojama. Nenaudokite šio laukelio ir nekeiskite vertės jame.|

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
| **Pakeitė kita funkcija?**   | Rekomenduojama naudoti „IController“ klasės plėtinio modelį importuojant „NuGet“ (Microsoft.Dynamics.Commerce.Hosting.Contracts) paketą. |
| **Paveiktos produkto sritys**         | Kompiuterinės įrangos stoties plėtiniai |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: nuo 10.0.11 leidimo. |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Commerce“ 10.0.10 versijoje
### <a name="pos-operation-803---picking-and-receiving"></a>EKA 803 operacija – paėmimas ir gavimas
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Operacijų paėmimas ir gavimas nebenaudojamas dėl naujos operacijų pertvarkos. |
| **Pakeitė kita funkcija?**   | Taip. Jie pakeičiami dviem naujomis EKA operacijomis: gaunama operacija (804) ir siunčiama operacija (805).|
| **Paveiktos produkto sritys**         | Elektroninio kasos aparato (EKA) programa |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: nuo 10.0.10 versijos išleidimo paėmimo ir gavimo operacijos nebegaus naujų funkcijų naujinimų. Būsimuose leidimuose bus atliktos tik kritinių operacijos klaidų pataisos. Visi klientai skatinami pereiti prie naujų [gaunamų operacijų](../pos-inbound-inventory-operation.md) ir [siunčiamų operacijų](../pos-outbound-inventory-operation.md), kurios ir toliau bus mūsų ilgalaikio produktų veiksmų plano dalis. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Commerce“ 10.0.7 versijoje
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>„Commerce” GetProductAvailabilities ir GetAvailableInventoryNearby API
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Buvo sukurtos naujos optimizuotos API, kad pakeistų GetProductAvailabilities ir GetAvailableInventoryNearby API. |
| **Pakeitė kita funkcija?**   | Taip, jos pakeičiamos GetEstimatedAvailability ir GetEstimatedProductWarehouseAvailability API. |
| **Paveiktos produkto sritys**         | „e-Commerce“ programos SDK |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: nuo 10.0.7 versijos išleidimo nebebus GetProductAvailabilities ir GetAvailableInventoryNearby inžinerinių investicijų. Organizacijos, naudojančios šias API „e-Commerce“ diegimuose, turėtų konvertuoti į naujas GetEstimatedAvailability ir GetEstimatedProductWarehouseAvailability API ir įjungti [funkciją Optimizuotas produkto pasiekiamumo skaičiavimas](../calculated-inventory-retail-channels.md).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Ankstesni pranešimai apie pašalintas arba nebenaudojamas funkcijas
Norėdami sužinoti daugiau apie funkcijas, kurios buvo pašalintos arba nebenaudojamos ankstesniuose leidimuose, žr. skyrių [Ankstesniuose leidimuose pašalintos arba nebenaudojamos funkcijos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
