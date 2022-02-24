---
title: Pašalintos arba nebenaudojamos „Dynamics 365 Commerce“ funkcijos
description: Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš „Dynamics 365 Commerce“.
author: josaw
manager: AnnBe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 37b541ff5037a38b60dbfd6a6c071f55afcc1304
ms.sourcegitcommit: 069ed5789517b550065e5e2317658fec4027359e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/07/2020
ms.locfileid: "4689541"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Pašalintos arba nebenaudojamos „Dynamics 365 Commerce“ funkcijos

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš „Dynamics 365 Commerce“.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Šis sąrašas skirtas suteikti jums informacijos apie pašalintas ir nebenaudojamas funkcijas, kad galėtumėte geriau planuoti savo darbą. 

> [!NOTE]
> Išsamios informacijos apie „Finance and Operations“ programų objektus rasite skyriuje [Techninės informacijos ataskaitos](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Galite palyginti skirtingas šių ataskaitų versijas, kad sužinotumėte apie objektus, kurie buvo pakeisti ar pašalinti kiekvienoje iš „Finance and Operations“ programų versijų.

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Commerce“ 10.0.15 versijoje

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>„Internet Explorer“ 11 palaikymas „Dynamics 365“ nebegalioja

|   |  |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Įsigaliojęs 2020 m. gruodį, „Microsoft Internet Explorer“ 11 palaikymas visiems „Dynamics 365“ produktams nebegalioja ir „Internet Explorer“ 11 nebebus palaikomas po 2021 m. rugpjūčio.<br><br>Tai paveiks klientus, kurie naudoja „Dynamics 365“ produktus, skirtus naudoti per „Internet Explorer“ 11 sąsają. Po 2021 m. rugpjūčio „Internet Explorer“ 11 nebepalaikys šių „Dynamics 365“ produktų. |
| **Pakeitė kita funkcija?**   | Rekomenduojame klientams pereiti prie „Microsoft Edge“.|
| **Paveiktos produkto sritys**         | Visi „Dynamics 365“ produktai |
| **Visuotinio diegimo parinktis**              | Visos|
| **Būsena**                         | Nebenaudojama. „Internet Explorer“ 11 nebebus palaikomas po 2021 m. rugpjūčio.|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Commerce“ 10.0.11 versijoje
### <a name="data-action-hooks"></a>Duomenų veiksmų trikčių gaudyklės
|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Duomenų veiksmų trikčių gaudyklė nebeaktyvi dėl našumo problemų. |
| **Pakeitė kita funkcija?**   | Rekomenduojame naudoti [duomenų veiksmų užrašymus](../e-commerce-extensibility/data-action-overrides.md) verslo logikos duomenų veiksmų sluoksnyje keitimui.|
| **Paveiktos produkto sritys**         | „e-Commerce“ praplėtimo duomenų veiksmai |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: nuo 10.0.11 leidimo. |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Mažmeninės prekybos SDK pagalba „Visual Studio 2015“, msbuild 14.0, ir „Retail SDK“\Referencinės bibliotekos ir įrankiai
|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | „Retail SDK“ pagalba „Visual Studio 2015“ buvo panaikinta ir atnaujinta tam, kad padėtų VS 2017, „msbuild 15.0“ ir visas referencines bibliotekas ir komercijos serverio generatoriaus įrankį „RetailSDK“\Referencinį kataloge, kuris buvo perkeltas į „NuGet“ paketus tam, kad būtų palengvintas plėtinio modelis ir SDK pagerinimo procesas.|
| **Pakeitė kita funkcija?**   | Rekomenduojame jums sekti informaciją [Perkelti „Retail SDK“ iš „Visual Studio 2015“ į „Visual Studio 2017“](../dev-itpro/retail-sdk/migrate-sdk.md) savo sistemos atnaujinimui. |
| **Paveiktos produkto sritys**         | „Retail SDK“ plėtiniai |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: nuo 10.0.11 leidimo. |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>„Retail Server Extension“ naudojantis „IEdmModelExtender“ ir „CommerceController“
|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | „Retail“ serverio plėtinys naudojantis „IEdmModelExtender“ ir „CommerceControllerׅ“ buvo pašalintas tam, kad būtų pateiktas supaprastintas plėtinio modelis. Naujoji versija turės tik valdiklio klasę be papildomo „IEdmModelExtender“ klasės versijos. Tai taip pat panaikina priklausomybę nuo konkrečios „OData“ versijos (jei „OData“ versija yra atnaujinama, ji gali sugadinti plėtinius.) |
| **Pakeitė kita funkcija?**   |  Rekomenduojame naudoti „IController“ klasės plėtinio modelį importuojant „NuGet“ (Microsoft.Dynamics.Commerce.Hosting.Contracts) paketą. |
| **Paveiktos produkto sritys**         | „Retail“ serverio plėtiniai |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: nuo 10.0.11 leidimo. |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>Kompiuterinės įrangos stoties plėtinys naudojantis „IHardwareStationController“
|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Kompiuterinės įrangos plėtinys naudojantis „IHardwareStationController“ buvo pašalintas tam, kad būtų pateiktas supaprastintas plėtinio modelis. Naujos versijos turės tik „IController“ klasę be jokios papildomos klasės versijos ir taip bus išvengta priklausomybės nuo pagrindinių kompiuterinės įrangos stoties bibliotekų, nes ankstesnis plėtinys turėjo remtis keliomis bibliotekomis.) |
| **Pakeitė kita funkcija?**   | Rekomenduojama naudoti „IController“ klasės plėtinio modelį importuojant „NuGet“ (Microsoft.Dynamics.Commerce.Hosting.Contracts) paketą. |
| **Paveiktos produkto sritys**         | Kompiuterinės įrangos stoties plėtiniai |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: nuo 10.0.11 leidimo. |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Commerce“ 10.0.10 versijoje
### <a name="pos-operation-803---picking-and-receiving"></a>EKA 803 operacija – paėmimas ir gavimas
|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Operacijų paėmimas ir gavimas nebenaudojamas dėl naujos operacijų pertvarkos. |
| **Pakeitė kita funkcija?**   | Taip. Jie pakeičiami dviem naujomis EKA operacijomis: gaunama operacija (804) ir siunčiama operacija (805).|
| **Paveiktos produkto sritys**         | Elektroninio kasos aparato (EKA) programa |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: nuo 10.0.10 versijos išleidimo paėmimo ir gavimo operacijos nebegaus naujų funkcijų naujinimų. Būsimuose leidimuose bus atliktos tik kritinių operacijos klaidų pataisos. Visi klientai skatinami pereiti prie naujų [gaunamų operacijų](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) ir [siunčiamų operacijų](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), kurios ir toliau bus mūsų ilgalaikio produktų veiksmų plano dalis. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Commerce“ 10.0.7 versijoje
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>„Commerce” GetProductAvailabilities ir GetAvailableInventoryNearby API
|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Buvo sukurtos naujos optimizuotos API, kad pakeistų GetProductAvailabilities ir GetAvailableInventoryNearby API. |
| **Pakeitė kita funkcija?**   | Taip, jos pakeičiamos GetEstimatedAvailability ir GetEstimatedProductWarehouseAvailability API. |
| **Paveiktos produkto sritys**         | „e-Commerce“ programos SDK |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: nuo 10.0.7 versijos išleidimo nebebus GetProductAvailabilities ir GetAvailableInventoryNearby inžinerinių investicijų. Organizacijos, naudojančios šias API „e-Commerce“ diegimuose, turėtų konvertuoti į naujas GetEstimatedAvailability ir GetEstimatedProductWarehouseAvailability API ir įjungti [funkciją Optimizuotas produkto pasiekiamumo skaičiavimas](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Ankstesni pranešimai apie pašalintas arba nebenaudojamas funkcijas
Norėdami sužinoti daugiau apie funkcijas, kurios buvo pašalintos arba nebenaudojamos ankstesniuose leidimuose, žr. skyrių [Ankstesniuose leidimuose pašalintos arba nebenaudojamos funkcijos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).
