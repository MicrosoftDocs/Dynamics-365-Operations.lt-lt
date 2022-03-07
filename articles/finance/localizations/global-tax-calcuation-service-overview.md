---
title: Mokesčių skaičiavimo apžvalga
description: Šioje temoje paaiškinama bendroji Mokesčių skaičiavimo galimybės apimtis ir funkcijos.
author: wangchen
ms.date: 11/17/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1dff1767b8e19215a2b27f87c45325e6abd1266e
ms.sourcegitcommit: f2a78e0d7d461ca843ac2f9abff7690275db9196
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/09/2022
ms.locfileid: "8105442"
---
# <a name="tax-calculation-overview"></a>Mokesčių skaičiavimo apžvalga

[!include [banner](../includes/banner.md)]

Mokesčių skaičiavimas yra hiper išplečiama kelių nuomotojų paslauga, įgalinanti „Global Tax Engine“ automatizuoti ir supaprastinti mokesčių nustatymo ir skaičiavimo procesą. Visiškai konfigūruotinas mokesčių modulis. Elementai, kuriuos galima konfigūruoti, apima (bet tuo neapsiribojama) apmokestinamą duomenų modelį, mokesčio kodą, mokesčių taikomumo matricą ir mokesčių skaičiavimo formulę. Mokesčių sistema veikia pagrindinių paslaugų „Microsoft Azure“ platformoje ir siūlo modernias technologiją bei proporcingai keičiamumą.

Mokesčių skaičiavimas integruojamas su „Dynamics 365 Finance“ ir „Dynamics 365 Supply Chain Management“. Galiausiai ji taip pat bus „Dynamics 365 Project Operations“ integruota į, ir kitas pirmosios šalies ir trečiosios šalies „Dynamics 365 Commerce“ programas.

> [!IMPORTANT]
> Kai įgalinate papildinį Mokesčių skaičiavimas, kai kurios su susijusiais duomenimis susijusios operacijos gali būti atliekamos ne duomenų centre, kuris tvarko jūsų aptarnavimo duomenis. Prieš įgalindami papildinį Mokesčių skaičiavimas, peržiūrėkite [sąlygas](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md). Mes rūpinamės jūsų privatumu. Norėdami sužinoti daugiau, perskaitykite mūsų [Pareiškimą dėl privatumo](https://go.microsoft.com/fwlink/?LinkId=521839).

Mokesčių skaičiavimas yra mikrotarnyba pagrįstas mokesčių mechanizmas, siūlantis eksponentinį išplečiamumą ir galintis padėti atlikti tolesnes užduotis.

- Naudojant patobulintą nustatymo mechanizmą automatiškai nustatyti tinkamą PVM grupę, prekių PVM grupę ir mokesčių kodus.
- Palaikyti kelis vieno juridinio subjekto mokesčių registracijos numerius ir automatiškai nustatyti tinkamą apmokestinamų operacijų mokesčių registracijos numerį.
- Palaikyti perkėlimo užsakymų mokesčių nustatymą, skaičiavimą, registravimą ir sudengimą.
- Pagal konkrečius verslo poreikius apibrėžti konfigūruojamąsias mokesčių skaičiavimo formules ir sąlygas.
- Bendrinti mokesčių nustatymo ir skaičiavimo sprendimą keliems juridiniams subjektams, norint sumažinti tvarkymo darbų apimtį ir išvengti klaidų.
- Palaikyti kliento ir tiekėjo mokesčių registracijos numerių nustatymo funkciją.
- Palaikyti sąrašo kodų nustatymo funkciją.
- Palaikyti mokesčių skaičiavimo parametrus mokesčių jurisdikcijos lygiu.

Norėdami naudoti papildinį Mokesčių skaičiavimas, jį įdiekite savo „Microsoft Dynamics Lifecycle Services“ projekte. Tada užbaikite sąranką sprendime [„Regulatory Configuration Service“](https://marketing.configure.global.dynamics.com/) ir įjunkite papildinį Mokesčių skaičiavimas sprendime „Finance and Supply Chain Management“. Daugiau informacijos žr. [Darbo su mokesčių paslaugų pradžia](global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Prieinamumas

Mokesčių skaičiavimas paprastai pasiekiamas gamybos aplinkose visiems klientams nuo 10.0.21 versijos.

Ateityje atsiras naujų funkcijų. Dažnai tikrinkite naujausią leidimų planą, kad sužinotumėte apie palaikomų funkcijų padengimą ir aprėptį.

Mokesčių skaičiavimas yra įdiegtas toliau nurodytose „Azure" geografinėse srityse. Atsižvelgiant į klientų poreikius, bus įtraukta daugiau „Azure" geografinių vietovių.

- Azijos ir Ramiojo vandenyno regionas
- Australija
- Kanada
- Europa
- Japonija
- Jungtinė Karalystė
- Jungtinės Valstijos

> [!NOTE]
> Mokesčių skaičiavimas nepalaiko ankstesnių „Dynamics 365“ versijų, pvz., „Dynamics AX 2012“ ar vietinių „Dynamics 365“ įdiegčių.

## <a name="versions"></a>Versijos
Rekomenduojame importuoti ir nustatyti savo mokesčių skaičiavimo konfigūraciją su versija, kuri atitinka jūsų finansų arba tiekimo grandinės valdymo versiją.

| Finansų arba tiekimo grandinės valdymo versija | Mokesčių konfigūracijos versija               |
| --------------- | --------------------------------------- |
| 10.0.18         | Mokesčių konfigūracija – Europa 30.12.82     |
| 10.0.19         | Mokesčių skaičiavimo konfigūracija 36.38.193 |
| 10.0.20         | Mokesčių skaičiavimo konfigūracija 40.43.208 |
| 10.0.21         | Mokesčių skaičiavimo konfigūracija 40.48.215 |
| 10.0.22         | Mokesčių skaičiavimo konfigūracija 40.48.215 |
| 10.0.23         | Mokesčių skaičiavimo konfigūracija 40.50.221 |
| 10.0.24         | Mokesčių skaičiavimo konfigūracija 40.50.225 |
| 10.0.25         | Mokesčių skaičiavimo konfigūracija 40.50.225 |


## <a name="data-flow"></a>Duomenų srautas

Čia yra mokesčių skaičiavimo duomenų srauto proceso struktūra. 

1. Sprendime RCS peržiūrėkite ir importuokite apmokestinamų dokumentų modelių konfigūracijas bei modelių susiejimo konfigūracijas. Jei konfigūracijas turite išplėsti išplėstiniam scenarijui, žr. [Duomenų laukų įtraukimas į mokesčių konfigūracijas](tax-service-add-data-fields-tax-configurations.md).
2. Sprendime RCS kurkite arba tvarkykite mokesčių funkcijas. Galite naudoti mokesčių funkcijas, norėdami tvarkyti mokesčių tarifus ir mokesčių taikymo taisykles.
3. Kai mokesčių funkcijų sąranka baigta, publikuokite mokesčių konfigūracijas ir mokesčių funkcijas iš RCS į visuotinę saugyklą.
4. Sprendime „Finance“ pasirinkite, kurią mokesčių funkcijos nustatymo versiją naudoti konkrečiam juridiniam subjektui.
5. Sprendime „Finance and Supply Chain Management“ operacijos naudokite įprastai. Kai reikalingas Mokesčių skaičiavimas, klientas renka informaciją iš operacijos, pvz., pardavimo ar pirkimo užsakymo, ir supakuoja informaciją kaip mokamąją krovą. Tada bus išsiųsta užklausa mokesčiams apskaičiuoti.
6. Mokesčių skaičiavimo užklausa gaunama iš kliento ir skaičiavimas baigiamas. Tada mokesčių rezultatas pateikiamas klientui.
7. „Dynamics 365“ klientas gauna mokesčių rezultatą ir PVM puslapyje pateikia mokesčių skaičiavimo rezultatą.

## <a name="supported-transactions"></a>Palaikomos operacijos

Papildinį Mokesčių skaičiavimas galima įgalinti naudojant operacijas. 

10.0.21 versijoje palaikomos tolesnės operacijos. 

- Pardavimas

    - Pardavimo pasiūlymas
    - Pardavimo užsakymas
    - Patvirtinimas
    - Išrinkimo dokumentas
    - Važtaraštis
    - Pardavimo sąskaita faktūra
    - Kredito sąskaita
    - Grąžinimo užsakymas
    - Antraštės įvairūs keitimai
    - Įvairių išlaidų eilutė

- Pirkimas

    - Pirkimo užsakymas
    - Patvirtinimas
    - Gavimų sąrašas
    - Gavimo dokumentas
    - Pirkimo SF
    - Antraštės įvairūs keitimai
    - Įvairių išlaidų eilutė
    - Kredito sąskaita
    - Grąžinimo užsakymas
    - Pirkimo paraiška
    - Papildomos pirkimo paraiškos eilutės išlaidos
    - Pasiūlymo patvirtinimas
    - Pasiūlymo patvirtinimo antraštės papildomos išlaidos
    - Pasiūlymo patvirtinimo eilutės papildomos išlaidos

- Atsargos

    - Perlaidos užsakymas - siuntimas
    - Perlaidos užsakymas - gavimas

10.0.23 versijoje palaikomos tolesnės operacijos. 

- Laisvos formos sąskaita faktūra

## <a name="supported-countriesregions"></a>Palaikomos šalys / regionai

Papildinį Mokesčių skaičiavimas gali įjungti juridinis subjektas. 

10.0.21 versijoje palaikomos tolesnės juridinio subjekto pagrindinio adreso šalys / regionai.

- Austrija
- Belgija
- Danija
- Estija
- Suomija
- Prancūzija
- Vokietija
- Vengrija
- Islandija
- Italija
- Latvija
- Lietuva
- Nyderlandai
- Norvegija
- Lenkija
- Švedija
- Šveicarija
- Jungtinė Karalystė
- Jungtinės Valstijos

10.0.22 versijoje palaikomos tolesnės juridinio subjekto pagrindinio adreso šalys / regionai.

- Australija
- Bahreinas
- Kanada
- Egiptas
- Honkongo SAR
- Kuveitas
- Naujoji Zelandija
- Omanas
- Kataras
- Saudo Arabijos
- Pietų Afrika
- Jungtiniai Arabų Emyratai

10.0.23 versijoje palaikomos tolesnės juridinio subjekto pagrindinio adreso šalys / regionai.

- Tailandas
- Japonija
- Malaizija
- Singapūras

10.0.24 versijoje palaikomos tolesnės juridinio subjekto pagrindinio adreso šalys / regionai.

- Meksika

## <a name="related-resources"></a>Susiję ištekliai

[Darbo su mokesčių paslaugomi pradžia](./global-get-started-with-tax-calculation-service.md)

[Kelių PVM registracijų numeris](./emea-multiple-vat-registration-numbers.md)

[Mokesčių priemonės perkėlimo užsakymo palaikymas](./tasks/tax-feature-support-for-transfer-order.md)

[Kaip sukurti plėtinį mokesčių tarnybose](./tax-service-add-data-fields-tax-integration-by-extension.md)
