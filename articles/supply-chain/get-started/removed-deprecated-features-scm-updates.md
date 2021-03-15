---
title: Pašalintos arba nebenaudojamos „Dynamics 365 Supply Chain Management“ funkcijos
description: Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš „Dynamics 365 Supply Chain Management“.
author: kamaybac
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 9d3faa34812130a040e625a6af4f047c2b8fca08
ms.sourcegitcommit: 79621e667cd7f48ba3bdbf2731f6f33d8e9f57f6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5154308"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Pašalintos arba nebenaudojamos „Dynamics 365 Supply Chain Management“ funkcijos

[!include [banner](../includes/banner.md)]

Ši tema bus atnaujinta, kai naujai pašalintos arba nebenaudojamos funkcijos bus užfiksuotos „Dynamics 365 Supply Chain Management“.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Šis sąrašas skirtas suteikti jums informacijos apie pašalintas ir nebenaudojamas funkcijas, kad galėtumėte geriau planuoti savo darbą.

> [!NOTE]
> Išsamios informacijos apie „Finance and Operations“ programų objektus rasite skyriuje [Techninės informacijos ataskaitos](https://docs.microsoft.com/dynamics/s-e/). Galite palyginti skirtingas šių ataskaitų versijas, kad sužinotumėte apie objektus, kurie buvo pakeisti ar pašalinti kiekvienoje iš „Finance and Operations“ programų versijų.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Supply Chain Management“ 10.0.15 versijoje

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>„Internet Explorer“ 11 palaikymas „Dynamics 365“ nebegalioja

|   |  |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Nuo 2020 m. gruodžio „Microsoft Internet Explorer 11“ palaikymas visuose „Dynamics 365“ produktuose yra nutraukiamas, o „Internet Explorer 11“ nebus palaikomas nuo 2021m. rugpjūčio.<br><br>Tai paveiks klientus, kurie naudoja „Dynamics 365“ produktus, skirtus naudoti „Internet Explorer 11“ sąsają. Nuo 2021m. rugpjūčio „Internet Explorer 11“ nebus palaikomas tokiuose „Dynamics 365“ produktuose. |
| **Pakeitė kita funkcija?**   | Rekomenduojame klientams naudoti „Microsoft Edge“.|
| **Paveiktos produkto sritys**         | Visi „Dynamics 365“ produktai |
| **Visuotinio diegimo parinktis**              | Visos|
| **Būsena**                         | Nebenaudojama. „Internet Explorer“ 11 nebebus palaikomas po 2021 m. rugpjūčio.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Naudokite sukurtą „Supply Chain Management“ pagrindinį planavimo variklį gamybos scenarijams

|   |  |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Siekiant padidinti našumą ir sumažinti SQL duomenų bazės apkrovą bendrojo planavimo vykdymų metu, įtaisytasis „Supply Chain Management” bendrojo planavimo mechanizmas yra pakeičiamas planavimo optimizavimu. Planavimo optimizavimas leidžia greitai planuoti vykdymus, kuriuos galima atlikti netgi darbo valandomis. Dėl to planuotojai iš karto reaguoja į poreikio arba planavimo parametrų pasikeitimus. |
| **Pakeitė kita funkcija?**   | Taip, planavimo optimizavimas pakeis dabartinį įtaisytąjį „Supply Chain Management“ bendrojo planavimo mechanizmą. |
| **Paveiktos produkto sritys**         | „Supply Chain Management” – bendrasis planavimas |
| **Visuotinio diegimo parinktis**              | Tik debesyje. Planavimo optimizavimas nepalaikomas vietiniuose visuotiniuose diegimuose. |
| **Būsena**                         | Nebenaudojama. Nuo 2021 m. spalio 1 d. gamybos scenarijai nebebus palaikomi su įdiegtu „Dynamics 365 Supply Chain Management“ pagrindinio planavimo varikliu. Planavimo scenarijams, klientai privalo naudoti „Planning Optimization“ pagrindinio planavimo apskaičiavimams. Daugiau informacijos žr. [Planavimo optimizavimo dokumentacija](https://go.microsoft.com/fwlink/?linkid=2105830). Klientai su patalpose esančiu „Dynamics 365 Supply Chain Management“ talpinimu gali ir toliau naudoti „Supply Chain Management“ pagrindinio planavimo variklį gamybos scenarijams po 2021 m. spalio mėnesio. Tačiau daugiau funkcijų patobulinimų nebus teikiama. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Supply Chain Management“ 10.0.11 versijoje

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Įtaisytojo „Supply Chain Management“ bendrojo planavimo mechanizmo naudojimas paskirstymo scenarijuose

|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Siekiant padidinti našumą ir sumažinti SQL duomenų bazės apkrovą bendrojo planavimo vykdymų metu, įtaisytasis „Supply Chain Management” bendrojo planavimo mechanizmas yra pakeičiamas planavimo optimizavimu. Planavimo optimizavimas leidžia greitai planuoti vykdymus, kuriuos galima atlikti netgi darbo valandomis. Dėl to planuotojai iš karto reaguoja į poreikio arba planavimo parametrų pasikeitimus. |
| **Pakeitė kita funkcija?**   | Taip, planavimo optimizavimas pakeis dabartinį įtaisytąjį „Supply Chain Management“ bendrojo planavimo mechanizmą. |
| **Paveiktos produkto sritys**         | „Supply Chain Management” – bendrasis planavimas |
| **Visuotinio diegimo parinktis**              | Tik debesyje. Planavimo optimizavimas nepalaikomas vietiniuose visuotiniuose diegimuose. |
| **Būsena**                         | Nebenaudojama. Nuo 2021 m. balandžio 1 d. paskirstymo scenarijai nebebus palaikomi su įdiegtu „Dynamics 365 Supply Chain Management“ pagrindinio planavimo varikliu. Paskirstymo scenarijuose klientai turi naudoti bendrojo planavimo skaičiavimo planavimo optimizavimą. Daugiau informacijos žr. [Planavimo optimizavimo dokumentacija](https://go.microsoft.com/fwlink/?linkid=2105830). Klientai, turintys vietinius visuotinius „Dynamics 365 Supply Chain Management” diegimus, po 2021 m. balandžio mėn. gali toliau naudoti „Supply Chain Management” bendrojo planavimo mechanizmą paskirstymo scenarijuose. Tačiau daugiau funkcijų patobulinimų nebus teikiama. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Ankstesni pranešimai apie pašalintas arba nebenaudojamas funkcijas

Norėdami sužinoti daugiau apie funkcijas, kurios buvo pašalintos arba nebenaudojamos ankstesniuose leidimuose, žr. skyrių [Ankstesniuose leidimuose pašalintos arba nebenaudojamos funkcijos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]