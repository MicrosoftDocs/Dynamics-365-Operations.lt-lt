---
title: Pašalintos arba nerekomenduojamos „Dynamics 365 Finance“ funkcijos
description: Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš „Dynamics 365 Finance“.
author: roschlom
ms.date: 04/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: e6a391b10ddaef79e68f47afae7d77135a1c333a
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184130"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Pašalintos arba nerekomenduojamos „Dynamics 365 Finance“ funkcijos

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš „Dynamics 365 Finance“.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nerekomenduojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Šis sąrašas skirtas suteikti jums informacijos apie pašalintas ir nebenaudojamas funkcijas, kad galėtumėte geriau planuoti savo darbą. 

> [!NOTE]
> Išsamios informacijos apie „Finance and Operations“ programų objektus rasite skyriuje [Techninės informacijos ataskaitos](/dynamics/s-e/global/axtechrefrep_61). Galite palyginti skirtingas šių ataskaitų versijas, kad sužinotumėte apie objektus, kurie buvo pakeisti ar pašalinti kiekvienoje iš „Finance and Operations“ programų versijų.

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Pašalintos arba nerekomenduojamos funkcijos, esančios „Finance“ 10.0.20 versijoje

### <a name="rtir-query-invoice-data-request-hu-electronic-reporting-er-format-configuration"></a>„RTIR Sąskaitos faktūros duomenų užklausos (HU) Elektroninės ataskaitos (ER) formato konfigūravimas

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo / pašalinimo priežastis** | Neįtraukta į elektroninių pranešimų apdorojimą, sąveikaujant su vengrų internetine sąskaitų faktūrų išrašymo sistema |
| **Pakeitė kita funkcija?**   | Ne |
| **Paveiktos produkto sritys**         | Prašymas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nerekomenduoja: Nuo 2022 m. balandžio 15 d. planuojame nebeteikti „RTIR Sąskaitos faktūros duomenų užklausos (HU)” formato konfigūracijos palaikymo. |

### <a name="french-fec-audit-file-electronic-reporting-er-format-for-france-under-german-audit-file-output-format"></a>Prancūzijos FEC audito failo Prancūzijos elektroninių ataskaitų (ER) formatas pagal „Vokietijos audito failo išeigos" formatą

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo / pašalinimo priežastis** | Pakeičiama nauju „FEC audito failo (FR)“ formatu |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Prašymas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Pasenusi: iki 2022 m. gegužės 1 d. planuojame nebepalaikome Prancūzijos FEC audito failo Prancūzijos elektroninių ataskaitų (ER) formato, formato „Vokietijos audito failo išvestis". Naujas FEC audito failo (FR) formatas įvestas po „Duomenų eksportavimo modeliu". |

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Pašalintos arba nerekomenduojamos „Finance“ 10.0.17 versijos funkcijos

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>LCS saugykla kaip elektroninių ataskaitų konfigūracijų saugojimo parinktis

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Pakeista nauja „Regulatory Configuration Services” (RCS) visuotine saugykla |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | „Dynamics 365 Finance”, „Supply Chain Management” ir „Project Operations” produktai|
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nerekomenduojama: nuo 2022 m. balandžio 1 d. nebepalaikysime „Microsoft Dynamics Lifecycle Services” (LCS) saugyklos kaip elektroninių ataskaitų (ER) konfigūracijų saugojimo parinkties. Naujos „Microsoft” ER konfigūracijos bus publikuojamos ir jas bus galima atsisiųsti tik iš visuotinės saugyklos. Visuotinę saugyklą galima pasiekti iš „Dynamics 365” produktų ir RCS. Norėdami gauti daugiau informacijos, žr. [Importuoti ER konfigūracijas iš RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) ir [„Regulatory Configuration Service“ - „Lifecycle Services“ talpinimas nebegalioja](../localizations/rcs-lcs-repo-dep-faq.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Pašalintos arba nerekomenduojamos funkcijos, esančios „Finance“ 10.0.16 versijoje

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a>„PVM deklaravimas (CZ)“ ir „Valdymo pareiškimo eksportavimas (CZ)“ elektroninės sąskaitos formatai Čekijai

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Pakeitimas naujais formatais |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Prašymas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nebegalioja: 2022 m. sausio 22 d. planuojame nebepalaikyti „PVM deklaracijos (CZ)“, „Valdymo pareiškimo eksportavimo (CZ)“ Elektroninių ataskaitos (ER) formatų. Nauja PVM deklaracija XML (CZ), PVM deklaracijos „Excel“ (CZ), PVM valdymo pareiškimas XML (CZ) formatai yra pristatomi „Mokesčių deklaracijos“ modelyje. |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>„DK operacijos eksporto formatas (BE)“ elektroninės ataskaitos formatas ir atitinkamas „DK operacijos eksportas (BE)“ modelis, skirtas Belgijai

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Pakeičiamas nauju ER formatu modelyje „Standartinis audito failas (SAF-T)“.  |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Prašymas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nerekomenduojama: nuo 2021 m. gruodžio 1 d. planuojame nebepalaikyti „DK operacijos eksportavimo formatas (BE)“ elektroninių ataskaitų (ER) formato ir atitinkamo „DK operacijos eksportas (BE)“ modelio. Naujas „DK duomenų eksportavimas (BE)“ formatas kartu su „DK duomenų modelio susiejimas“ pristatomi modelyje „Standartinis audito failas (SAF-T)“. |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>PVM 100 ataskaita, skirta Jungtinei Karalystei SSRS formatu

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Pakeičiamas nauju ER formatu – „PVM deklaracijos „Excel“ (UK)“ formatas, esantis „mokesčių deklaracijos modelyje“.  |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Prašymas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nerekomenduojama: nuo 2021 m. gruodžio 1 d. planuojame nebepalaikyti „PVM 100 ataskaita“ SSRS formatu. Naujas „PVM deklaracijos „Excel“ (UK)“ formatas, esantis „mokesčių deklaracijos modelyje“, įtrauktas į [MTD PVM funkciją](../localizations/emea-gbr-mtd-vat-integration.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Pašalintos arba nerekomenduojamos funkcijos, esančios „Finance“ 10.0.15 versijoje

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>„Internet Explorer 11“ palaikymas „Dynamics 365“ yra nutrauktas

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Nuo 2020 m. gruodžio „Microsoft Internet Explorer 11“ palaikymas visuose „Dynamics 365“ produktuose yra nutraukiamas, o „Internet Explorer 11“ nebus palaikomas nuo 2021m. rugpjūčio.<br><br>Tai paveiks klientus, kurie naudoja „Dynamics 365“ produktus, skirtus naudoti „Internet Explorer 11“ sąsają. Nuo 2021m. rugpjūčio „Internet Explorer 11“ nebus palaikomas tokiuose „Dynamics 365“ produktuose. |
| **Pakeitė kita funkcija?**   | Rekomenduojame klientams naudoti „Microsoft Edge“.|
| **Paveiktos produkto sritys**         | Visi „Dynamics 365“ produktai |
| **Visuotinio diegimo parinktis**              | Visos|
| **Būsena**                         | Nerekomenduojama. „Internet Explorer 11“ nebus palaikoma nuo 2021 m. rugpjūčio.|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Pašalintos arba nerekomenduojamos funkcijos, esančios „Finance“ 10.0.12 versijoje

### <a name="not-deprecated-polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Nepanaikinta: Lenkijos SSRS ataskaitos: pardavimo PVM registras, pirkimo PVM registras, ES suvestinės PVM registras – funkcijos nuoroda PL-00014

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo / pašalinimo priežastis** | Nėra teisiškai reikalaujama.  |
| **Pakeitė kita funkcija?**   | Taip (standartinis audito failas, kuriame yra PVM deklaracija, „Excel“ formatu – JPK_VDEK) |
| **Paveiktos produkto sritys**         | Prašymas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nepanaikinta: nuo 2021 m. balandžio 27 d. planuojame tęsti šių SSRS ataskaitų palaikymą: **pardavimo PVM registrą, pirkimo PVM registrą, ES suvestinės PVM registrą – funkcijos nuoroda PL-00014**. Bus įvedamas „Excel“ formato pavyzdys, skirtas standartiniam audito failui kartu su PVM deklaracija (JPK_VDEK) taip pat buvo įtrauktas. |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Pašalintos arba nerekomenduojamos funkcijos, esančios „Finance“ 10.0.11 versijoje

### <a name="norwegian-standard-main-accounts"></a>Norvegijos standartinės pagrindinės sąskaitos

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo / pašalinimo priežastis** | Pertvarka  |
| **Pakeitė kita funkcija?**   | Taip (pakeista programai būdingais ER formato parametrais) |
| **Paveiktos produkto sritys**         | Programos |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nerekomenduojama: nuo 2021 m. balandžio 1 d. planuojame nebepalaikyti funkcijų, susijusių su standartinėmis pagrindinėmis sąskaitomis: nuorodos lauko, susijusios lentelės, duomenų objekto. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Pašalintos arba nerekomenduojamos funkcijos, esančios „Finance“ 10.0.7 versijoje

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Darbo eigos užklausos keitimo dialogo lange nebėra vartotojų pasirinkimo išplečiamojo sąrašo

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo / pašalinimo priežastis** | Pakeista į funkciją su sąskaitų grupių pasirinkimu.  |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Darbo eiga |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nerekomenduojama: nuo 2020 m. gruodžio 1 d. planuojame nebepalaikyti Kinijos kvitų tipų nustatymų be sąskaitų grupių pasirinkimo. Daugiau informacijos apie naują dizainą rasite [„Kas naujo 10.0.7 versijoje“](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Ankstesni pranešimai apie pašalintas arba nerekomenduojamas funkcijas
Norėdami sužinoti daugiau apie funkcijas, kurios buvo pašalintos arba nebenaudojamos ankstesniuose leidimuose, žr. skyrių [Ankstesniuose leidimuose pašalintos arba nebenaudojamos funkcijos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
