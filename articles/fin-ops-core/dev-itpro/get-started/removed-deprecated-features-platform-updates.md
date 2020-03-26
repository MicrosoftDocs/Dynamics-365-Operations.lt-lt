---
title: Pašalintos arba nebenaudojamos platformos funkcijos
description: Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama šalinti iš „Finance and Operations“ programų platformos naujinių.
author: sericks007
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: d394f5ca84efc5beb943d349e45a3d2c9639d83c
ms.sourcegitcommit: 75974ae567bb0eacf0f65cac992b34ce5c680b93
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/03/2020
ms.locfileid: "3095779"
---
# <a name="removed-or-deprecated-platform-features"></a>Pašalintos arba nebenaudojamos platformos funkcijos

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama šalinti iš „Finance and Operations“ programų platformos naujinių.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Šis sąrašas skirtas suteikti jums informacijos apie pašalintas ir nebenaudojamas funkcijas, kad galėtumėte geriau planuoti savo darbą. 

> [!NOTE]
> Išsamios informacijos apie „Finance and Operations“ programų objektus rasite skyriuje [Techninės informacijos ataskaitos](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Galite palyginti skirtingas šių ataskaitų versijas, kad sužinotumėte apie objektus, kurie buvo pakeisti ar pašalinti kiekvienoje iš „Finance and Operations“ programų versijų.

## <a name="platform-update-32"></a>Platformos „update 32“

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Darbo eigos užklausos keitimo dialogo lange nebėra vartotojų pasirinkimo išplečiamojo sąrašo
|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Dėl sąrašo galėjo kilti saugos problemų, nes keitimo užklausa galėjo būti nusiųsta nenumatytam vartotojui. Taip pat kilo tinkamumo naudoti problema, nes vartotojas buvo verčiamas nustatyti darbo eigos iniciatorių ir pasirinkti jį rankiniu būdu.  |
| **Pakeitė kita funkcija?**   | Ne |
| **Paveiktos produkto sritys**         | Darbo eiga |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Vartotojų pasirinkimo išplečiamasis sąrašas buvo pašalintas iš „Platform update 32“ keitimo užklausos dialogo lango. Užklausos keitimo užklausos bus automatiškai siunčiamos iniciatoriui, kaip numatyta. Norėdami gauti daugiau informacijos apie šią funkciją, žr. skyrių [Darbo eigos patvirtinimo procesų veiksmai](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Sunumeruoti dokumentai, kuriuos generuoja debesies paslauga, nebepalaiko įterptųjų detalizuotų nuorodų 
|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Naršymo URL, įterpti į paslaugos generuojamus dokumentus, gali būti slaptų verslo duomenų. Norėdami apsaugoti kliento duomenis, saugumo sumetimais pašalinsime įterptųjų detalizuotų nuorodų, esančių dokumentuose, palaikymą. Dėl šio pakeitimo vartotojai galės kurti dokumentus našiai ir interaktyviai.  |
| **Pakeitė kita funkcija?**   | nr. |
| **Paveiktos produkto sritys**         | Ataskaitos |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Ši funkcija yra šalinama iš paslaugos.<br><br>Šiuolaikinis klientas siūlo daugybę galimybių, kaip kurti vaizdus, kuriuose yra automatiškai sugeneruotų nuorodų, padedančių naršyti programoje. Rekomenduojama paslaugoje esančius sunumeruotus dokumentus naudoti išoriniams ryšiams, kurie gavėjams siunčiami el. paštu, archyvuojami ir spausdinami. Patobulinome dokumentų peržiūrą tiesiogiai naršyklėje, per kurią suteikiama tiesioginė prieiga prie vietinių spausdintuvų. Daugiau informacijos ieškokite [„PDF dokumentų peržiūra naudojant įdėtąją peržiūros programą“](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Ankstesni pranešimai apie pašalintas arba nebenaudojamas funkcijas
Norėdami sužinoti daugiau apie funkcijas, kurios buvo pašalintos arba nebenaudojamos ankstesniuose leidimuose, žr. skyrių [Ankstesniuose leidimuose pašalintos arba nebenaudojamos funkcijos](../migration-upgrade/deprecated-features.md).

