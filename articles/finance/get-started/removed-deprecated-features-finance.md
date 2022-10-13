---
title: Pašalintos arba nebenaudojamos „Dynamics 365 Finance“ funkcijos
description: Šiame straipsnyje aprašomos priemonės, kurios buvo pašalintos arba suplanuotos pašalinti iš "Dynamics 365 Finance".
author: kfend
ms.date: 10/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 516b2b6091fa620b21eebba25f56ff55aa282ffc
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643800"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Pašalintos arba nebenaudojamos „Dynamics 365 Finance“ funkcijos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomos priemonės, kurios buvo pašalintos arba suplanuotos pašalinti iš "Dynamics 365 Finance".

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nerekomenduojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Šis sąrašas skirtas suteikti jums informacijos apie pašalintas ir nebenaudojamas funkcijas, kad galėtumėte geriau planuoti savo darbą. 

> [!NOTE]
> Išsami informacija apie finansų ir operacijų programėlių objektus pateikta techninės [nuorodos ataskaitose](/dynamics/s-e/global/axtechrefrep_61). Galite palyginti skirtingas šių ataskaitų versijas ir sužinoti apie objektus, kurie buvo pakeisti ar pašalinti kiekvienoje finansų ir operacijų programėlių versijoje.

## <a name="features-removed-or-deprecated-in-the-finance-10031-release"></a>Pašalintos arba nerekomenduojamos funkcijos, esančios „Finance“ 10.0.31 versijoje

### <a name="edifact-paymul-at-configuration-under-payment-model"></a>EDIFACT PAYMUL (AT) konfigūracija pagal mokėjimo modelį

| &nbsp;  | &nbsp;  |
|---|---|
| **Nerekomendavimo/pašalinimo priežastis** | Pakeičiamas nauju formatu, pagrįstu ISO 20022 001.001.09. | 
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Taikymas |
| **Visuotinio diegimo parinktis**              | Viskas |
| **Būsena**                         | Pasenusi: Austrijos bankai nusidėvi EDICFACT-PAYMUL tarptautinių mokėjimų metu iki 2022 m. lapkričio mėn. ir pakeis jį XML versijos 001.001.09N. Nauja konfigūracija buvo įtraukta į visuotinės konfigūracijos saugyklą, kuri įgalina vartotojus užpildyti tarptautinių mokėjimų užklausą. |

## <a name="features-removed-or-deprecated-in-the-finance-10030-release"></a>Pašalintos arba nerekomenduojamos funkcijos, esančios „Finance“ 10.0.30 versijoje

### <a name="revenue-recognition"></a>Įplaukų pripažinimas

[Įplaukų pripažinimas](../../finance/accounts-receivable/revenue-recognition-overview.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Nerekomendavimo/pašalinimo priežastis** |Pakeista patobulintos funkcijos, abonementinis [atsiskaitymas](../../finance/accounts-receivable/subscription-billing-summary.md)
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys** | Taikymas |
| **Visuotinio diegimo parinktis** | Viskas |
| **Būsena** | Pasenusi: po 2023 m. balandžio mėn. "Dynamics 365 Finance" įplaukų atpažinimo funkcijos nebegaus palaikymo su pataisymais. Klientų bus prašoma naudoti patobulintą funkciją – abonemento [sąskaitas](../../finance/accounts-receivable/subscription-billing-summary.md). 2023 m. spalio mėn. Įplaukų pripažinimo priemonė nebebus galima. Klientų bus prašoma pereiti prie patobulintos abonemento atsiskaitymo funkcijos. Grupavimo funkcijai kaip įplaukų atpažinimo daliai šiuo metu nėra suplanuoto pakeitimo funkcijos.|

## <a name="features-removed-or-deprecated-in-the-finance-10029-release"></a>Pašalintos arba nerekomenduojamos funkcijos, esančios „Finance“ 10.0.29 versijoje

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>Atsargų perkėlimo užsakymai, kurių perkėlimo kainai taikomas mokestis

[Atsargų perkėlimo užsakymai, kurių perkėlimo kainai taikomas mokestis](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Nerekomendavimo/pašalinimo priežastis** | Pakeista patobulinta funkcija, Atsargų perkėlimo [užsakymai Indijai](../../finance/localizations/apac-ind-stock-transfer.md)|
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys** | Taikymas |
| **Visuotinio diegimo parinktis** | Viskas |
| **Būsena** | Pasenusi: po 2023 m. balandžio mėn. atsargų perkėlimo užsakymai, kurie turi mokesčių už perkėlimo kainos funkciją, **nebegaus** palaikymo su pataisomis ir saugos pataisomis. Klientų bus prašoma naudoti patobulintą funkciją – atsargų [perkėlimo užsakymus Indijai](../../finance/localizations/apac-ind-stock-transfer.md). Po 2023 m. spalio mėn. atsargų perkėlimo užsakymai, **kurie** turi mokesčių už perkėlimo kainos funkciją, nebegalės būti prieinami, o klientų bus prašoma pereiti prie patobulintos funkcijos. |

### <a name="bank-statement-import-and-export-of-positive-pay-file"></a>Banko išrašo importavimas ir teigiamo mokėjimo failo eksportavimas

| &nbsp;  | &nbsp;  |
|---|---|
| **Nerekomendavimo/pašalinimo priežastis** |Pakeista patobulintų funkcijų, importuoti banko išrašus ir eksportuoti teigiamų išmokų failus.| 
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Taikymas |
| **Visuotinio diegimo parinktis**              | Viskas |
| **Būsena**                         | Pasenusi: XSLT funkcija, skirta failams importuoti ir eksportuoti, daugiau nebepalaiko klaidų pataisų ir saugos pataisų. Klientai bus paprašyti naudoti patobulintą funkciją: [...](../../finance/accounts-payable/set-up-positive-pay-er.md)[nustatyti teigiamų mokėjimo failus naudojant elektronines ataskaitas ir nustatyti išplėstinį banko suderinimo importavimą naudojant elektronines ataskaitas.](../../finance/accounts-payable/import-bai2-er.md) Po 2022 m. rugsėjo mėn. XSLT funkcijos nebebus galimos, o klientų bus prašoma pereiti prie patobulintos funkcijos.|


## <a name="features-removed-or-deprecated-in-the-finance-10026-release"></a>Pašalintos arba nerekomenduojamos funkcijos, esančios „Finance“ 10.0.26 versijoje

### <a name="sales-tax-report-for-finland-design-based-on-reporting-codes"></a>Suomijos PVM ataskaita (dizainas, pagrįstas ataskaitų kodais)

[PVM ataskaita (Suomija)](../localizations/emea-fin-sales-tax-payment-report-finland.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Pakeista nauju PVM deklaracijos dizainu, Suomijos [PVM deklaracija](../localizations/emea-fin-vat-declaration.md). |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Taikymas |
| **Visuotinio diegimo parinktis**              | Viskas |
| **Būsena**                         | Pasenusi: iki 2023 m. kovo 1 d. planuojame nebepalaikome Suomijos PVM ataskaitos (Suomijos ataskaitos maketo). Nauji **PVM deklaracijos TXT (FI**) ir **PVM deklaracijos Excel (FI)** elektroninių ataskaitų (ER) formatai pateikiami pagal mokesčių **deklaracijos** modelį. |

## <a name="features-removed-or-deprecated-in-the-finance-10024-release"></a>Pašalintos arba nerekomenduojamos funkcijos, esančios „Finance“ 10.0.24 versijoje

### <a name="sales-tax-report-for-sweden-design-based-on-reporting-codes"></a>Švedijos PVM ataskaita (dizainas, pagrįstas ataskaitų kodais)

[PVM ataskaita (Švedija)](../localizations/emea-swe-sales-tax-payment-report-sweden.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Pakeista nauju PVM deklaracijos dizainu, [Švedijos PVM deklaracija](../localizations/emea-swe-vat-declaration-sweden.md) |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Taikymas |
| **Visuotinio diegimo parinktis**              | Viskas |
| **Būsena**                         | Pasenusi: iki 2022 m. gruodžio 1 d. planuojame nebepalaikome Švedijos PVM ataskaitos (švediškos ataskaitos maketo). Nauji **PVM deklaracijos XML (SE**) ir **PVM deklaracijos Excel (SE)** elektroninių ataskaitų (ER) formatai pateikiami pagal mokesčių **deklaracijos** modelį. |

### <a name="vat-statement-for-austria-design-based-on-reporting-codes"></a>Austrijos PVM išrašas (dizainas, paremtas ataskaitų kodais)

[PVM išrašo informacija, skirta Austrijai](../localizations/emea-aut-vat-statement-details.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Pakeista nauju PVM deklaracijos dizainu, [Austrijos PVM deklaracija](../localizations/emea-aut-vat-declaration-austria.md) |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Taikymas |
| **Visuotinio diegimo parinktis**              | Viskas |
| **Būsena**                         | Pasenusi: iki 2022 **m. gruodžio 1 d. planuojame nebepalaikome PVM deklaracijos (AT) elektroninės ataskaitos (ER)** formato pagal **PVM deklaracijos modelį**. Nauji **PVM deklaracijos XML (AT) ir** **PVM deklaracijos Excel (AT)** formatai pateikiami mokesčių **deklaracijos modelyje**. |

### <a name="elster-declaration-for-germany-design-based-on-reporting-codes"></a>ELSTER deklaracija Vokietijai (dizainas, pagrįstas ataskaitų kodais)

[PVM išrašas](../localizations/emea-de-vat-declaration.md)</br>
[Nustatyti Elektroninę Vokietijos mokesčių deklaraciją](../../fin-ops-core/dev-itpro/analytics/tasks/setup-electronic-tax-declaration-germany.md)</br>
[Elektroninis PVM deklaracijos perkėlimas (ELSTER)](../localizations/tasks/de-00003-electronic-transmission-elster.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Pakeista nauju PVM deklaracijos dizainu, [Vokietijos PVM deklaracija](../localizations/emea-deu-vat-declaration-germany.md) |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Taikymas |
| **Visuotinio diegimo parinktis**              | Viskas |
| **Būsena**                         | Pasenusi: iki 2022 **m. gruodžio 1 d. planuojame nebepalaikome Elster (DE)** **ir Elster** modelio elektroninių ataskaitų (ER) formatų. Nauji **PVM deklaracijos XML (DE) ir** **PVM deklaracijos Excel (DE)** formatai pateikiami pagal mokesčių **deklaracijos** modelį. |

### <a name="ob-declaration-for-netherlands-design-based-on-reporting-codes"></a>Nyderlandų OB deklaracija (dizainas, pagrįstas ataskaitų kodais)

[OB deklaracija](../localizations/emea-nl-vat-declaration.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Pakeista nauju PVM deklaracijos dizainu, [Olandijos PVM deklaracija](../localizations/emea-nl-vat-declaration-netherlands.md) |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Taikymas |
| **Visuotinio diegimo parinktis**              | Viskas |
| **Būsena**                         | Pasenęs: iki 2022 **m. gruodžio 1 d. planuojame nebepalaikome OB deklaracijos (NL) ir OB** deklaracijos modelio elektroninių ataskaitų (ER) **formatų**. Nauji **PVM deklaracijos XML (NL) ir** **PVM deklaracijos Excel (NL)** formatai pateikiami mokesčių **deklaracijos modelyje**. |

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
| **Paveiktos produkto sritys**         | "Dynamics 365" finansų, tiekimo grandinės valdymo ir projekto operacijų produktai|
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

