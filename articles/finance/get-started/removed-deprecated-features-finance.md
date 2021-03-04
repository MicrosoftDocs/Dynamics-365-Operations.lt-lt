---
title: Pašalintos arba nebenaudojamos „Dynamics 365 Finance“ funkcijos
description: Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš „Dynamics 365 Finance“.
author: roschlom
manager: AnnBe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: a406db6d78302fa05596a58fffb7464222d4bfea
ms.sourcegitcommit: 069ed5789517b550065e5e2317658fec4027359e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/07/2020
ms.locfileid: "4689499"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Pašalintos arba nebenaudojamos „Dynamics 365 Finance“ funkcijos

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš „Dynamics 365 Finance“.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Šis sąrašas skirtas suteikti jums informacijos apie pašalintas ir nebenaudojamas funkcijas, kad galėtumėte geriau planuoti savo darbą. 

> [!NOTE]
> Išsamios informacijos apie „Finance and Operations“ programų objektus rasite skyriuje [Techninės informacijos ataskaitos](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Galite palyginti skirtingas šių ataskaitų versijas, kad sužinotumėte apie objektus, kurie buvo pakeisti ar pašalinti kiekvienoje iš „Finance and Operations“ programų versijų.

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Finance“ 10.0.16 versijoje

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>„DK operacijos eksporto formatas (BE)“ elektroninės ataskaitos formatas ir atitinkamas „DK operacijos eksportas (BE)“ modelis, skirtas Belgijai

|   |  |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Pakeičiamas nauju ER formatu modelyje „Standartinis audito failas (SAF-T)“.  |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Prašymas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nerekomenduojama: nuo 2021 m. gruodžio 1 d. planuojame nebepalaikyti „DK operacijos eksportavimo formatas (BE)“ elektroninių ataskaitų (ER) formato ir atitinkamo „DK operacijos eksportas (BE)“ modelio. Naujas „DK duomenų eksportavimas (BE)“ formatas kartu su „DK duomenų modelio susiejimas“ pristatomi modelyje „Standartinis audito failas (SAF-T)“. |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>PVM 100 ataskaita, skirta Jungtinei Karalystei SSRS formatu

|   |  |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Pakeičiamas nauju ER formatu – „PVM deklaracijos „Excel“ (UK)“ formatas, esantis „mokesčių deklaracijos modelyje“.  |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Prašymas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nerekomenduojama: nuo 2021 m. gruodžio 1 d. planuojame nebepalaikyti „PVM 100 ataskaita“ SSRS formatu. Naujas „PVM deklaracijos „Excel“ (UK)“ formatas, esantis „mokesčių deklaracijos modelyje“, įtrauktas į [MTD PVM funkciją](../localizations/emea-gbr-mtd-vat-integration.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Finance“ 10.0.15 versijoje

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>„Internet Explorer 11“ palaikymas „Dynamics 365“ yra nutrauktas

|   |  |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Nuo 2020 m. gruodžio „Microsoft Internet Explorer 11“ palaikymas visuose „Dynamics 365“ produktuose yra nutraukiamas, o „Internet Explorer 11“ nebus palaikomas nuo 2021m. rugpjūčio.<br><br>Tai paveiks klientus, kurie naudoja „Dynamics 365“ produktus, skirtus naudoti „Internet Explorer 11“ sąsają. Nuo 2021m. rugpjūčio „Internet Explorer 11“ nebus palaikomas tokiuose „Dynamics 365“ produktuose. |
| **Pakeitė kita funkcija?**   | Rekomenduojame klientams naudoti „Microsoft Edge“.|
| **Paveiktos produkto sritys**         | Visi „Dynamics 365“ produktai |
| **Visuotinio diegimo parinktis**              | Visos|
| **Būsena**                         | Nebenaudojama. „Internet Explorer 11“ nebus palaikoma nuo 2021 m. rugpjūčio.|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Finance“ 10.0.12 versijoje

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Lenkijos SSRS ataskaitos: pardavimo PVM registras, pirkimo PVM registras, ES suvestinės PVM registras – funkcijos nuoroda PL-00014

|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Nėra teisiškai reikalaujama.  |
| **Pakeitė kita funkcija?**   | Taip (standartinis audito failas, kuriame yra PVM deklaracija, „Excel“ formatu – JPK_VDEK) |
| **Paveiktos produkto sritys**         | Programos |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: iki 2021 m. liepos 1 d. planuojame nutraukti šių SSRS ataskaitų palaikymą: **pardavimo PVM registrą, pirkimo PVM registrą, ES suvestinės PVM registrą – funkcijos nuoroda PL-00014**. Bus įvedamas „Excel“ formato pavyzdys, skirtas standartiniam audito failui kartu su PVM deklaracija (JPK_VDEK). |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Finance“ 10.0.11 versijoje

### <a name="norwegian-standard-main-accounts"></a>Norvegijos standartinės pagrindinės sąskaitos

|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Pertvarka  |
| **Pakeitė kita funkcija?**   | Taip (pakeista programai būdingais ER formato parametrais) |
| **Paveiktos produkto sritys**         | Programos |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: nuo 2021 m. balandžio 1 d. planuojame nebepalaikyti funkcijų, susijusių su standartinėmis pagrindinėmis sąskaitomis: nuorodos lauko, susijusios lentelės, duomenų objekto. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Finance“ 10.0.7 versijoje

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Darbo eigos užklausos keitimo dialogo lange nebėra vartotojų pasirinkimo išplečiamojo sąrašo
|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Pakeista į funkciją su sąskaitų grupių pasirinkimu.  |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Darbo eiga |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: nuo 2020 m. gruodžio 1 d. planuojame nebepalaikyti Kinijos kvitų tipų nustatymų be sąskaitų grupių pasirinkimo. Daugiau informacijos apie naują dizainą rasite [„Kas naujo 10.0.7 versijoje“](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Ankstesni pranešimai apie pašalintas arba nebenaudojamas funkcijas
Norėdami sužinoti daugiau apie funkcijas, kurios buvo pašalintos arba nebenaudojamos ankstesniuose leidimuose, žr. skyrių [Ankstesniuose leidimuose pašalintos arba nebenaudojamos funkcijos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]