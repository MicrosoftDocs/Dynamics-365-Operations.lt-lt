---
title: Pašalintos arba nebenaudojamos „Dynamics 365 Supply Chain Management“ funkcijos
description: Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš „Dynamics 365 Supply Chain Management“.
author: kamaybac
manager: AnnBe
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7502cd16129431d41d152508fb3b49ff85a5a9f8
ms.sourcegitcommit: f1db998ecfccca660eb15cc2739b12c8463fa54d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2020
ms.locfileid: "3331253"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Pašalintos arba nebenaudojamos „Dynamics 365 Supply Chain Management“ funkcijos

[!include [banner](../includes/banner.md)]

Ši tema bus atnaujinta, kai naujai pašalintos arba nebenaudojamos funkcijos bus užfiksuotos „Dynamics 365 Supply Chain Management“.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Šis sąrašas skirtas suteikti jums informacijos apie pašalintas ir nebenaudojamas funkcijas, kad galėtumėte geriau planuoti savo darbą.

> [!NOTE]
> Išsamios informacijos apie „Finance and Operations“ programų objektus rasite skyriuje [Techninės informacijos ataskaitos](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Galite palyginti skirtingas šių ataskaitų versijas, kad sužinotumėte apie objektus, kurie buvo pakeisti ar pašalinti kiekvienoje iš „Finance and Operations“ programų versijų.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Supply Chain Management“ 10.0.11 versijoje

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Įtaisytojo „Supply Chain Management“ bendrojo planavimo mechanizmo naudojimas paskirstymo scenarijuose

|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Siekiant padidinti našumą ir sumažinti SQL duomenų bazės apkrovą bendrojo planavimo vykdymų metu, įtaisytasis „Supply Chain Management” bendrojo planavimo mechanizmas yra pakeičiamas planavimo optimizavimu. Planavimo optimizavimas leidžia greitai planuoti vykdymus, kuriuos galima atlikti netgi darbo valandomis. Dėl to planuotojai iš karto reaguoja į poreikio arba planavimo parametrų pasikeitimus. |
| **Pakeitė kita funkcija?**   | Taip, planavimo optimizavimas pakeis dabartinį įtaisytąjį „Supply Chain Management“ bendrojo planavimo mechanizmą. |
| **Paveiktos produkto sritys**         | „Supply Chain Management” – bendrasis planavimas |
| **Visuotinio diegimo parinktis**              | Tik debesyje. Planavimo optimizavimas nepalaikomas vietiniuose visuotiniuose diegimuose. |
| **Būsena**                         | Nebenaudojama. Nuo 2021 m. balandžio mėn. paskirstymo scenarijai nebebus palaikomi su įtaisytuoju „Dynamics 365 Supply Chain Management” bendrojo planavimo mechanizmu. Paskirstymo scenarijuose klientai turi naudoti bendrojo planavimo skaičiavimo planavimo optimizavimą. Daugiau informacijos žr. [Planavimo optimizavimo dokumentacija](https://go.microsoft.com/fwlink/?linkid=2105830). Klientai, turintys vietinius visuotinius „Dynamics 365 Supply Chain Management” diegimus, po 2021 m. balandžio mėn. gali toliau naudoti „Supply Chain Management” bendrojo planavimo mechanizmą paskirstymo scenarijuose. Tačiau daugiau funkcijų patobulinimų nebus teikiama. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Ankstesni pranešimai apie pašalintas arba nebenaudojamas funkcijas

Norėdami sužinoti daugiau apie funkcijas, kurios buvo pašalintos arba nebenaudojamos ankstesniuose leidimuose, žr. skyrių [Ankstesniuose leidimuose pašalintos arba nebenaudojamos funkcijos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).
