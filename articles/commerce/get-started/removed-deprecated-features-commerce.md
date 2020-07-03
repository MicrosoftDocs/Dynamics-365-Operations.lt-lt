---
title: Pašalintos arba nebenaudojamos „Dynamics 365 Commerce“ funkcijos
description: Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš „Dynamics 365 Commerce“.
author: josaw
manager: AnnBe
ms.date: 06/10/2020
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
ms.openlocfilehash: 64241ef1c25359c7b3b305c4e8f2b24de7e8f5e4
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443923"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Pašalintos arba nebenaudojamos „Dynamics 365 Commerce“ funkcijos

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš „Dynamics 365 Commerce“.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Šis sąrašas skirtas suteikti jums informacijos apie pašalintas ir nebenaudojamas funkcijas, kad galėtumėte geriau planuoti savo darbą. 

> [!NOTE]
> Išsamios informacijos apie „Finance and Operations“ programų objektus rasite skyriuje [Techninės informacijos ataskaitos](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Galite palyginti skirtingas šių ataskaitų versijas, kad sužinotumėte apie objektus, kurie buvo pakeisti ar pašalinti kiekvienoje iš „Finance and Operations“ programų versijų.

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Commerce“ 10.0.11 versijoje
### <a name="data-action-hooks"></a>Duomenų veiksmų trikčių gaudyklės
|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Duomenų veiksmų trikčių gaudyklė nebeaktyvi dėl našumo problemų. |
| **Pakeitė kita funkcija?**   | Vietoj to rekomenduojama, naudoti [duomenų veiksmų perrašymus](../e-commerce-extensibility/data-action-overrides.md), kad modifikuotumėte verslo logiką duomenų veiksmų sluoksnyje.|
| **Paveiktos produkto sritys**         | El. prekybos išplėtimo duomenų veiksmai |
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
