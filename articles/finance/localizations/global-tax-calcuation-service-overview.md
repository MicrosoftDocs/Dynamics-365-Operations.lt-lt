---
title: Mokesčių skaičiavimo apžvalga
description: Šiame straipsnyje paaiškinama bendroji mokesčių skaičiavimo galimybės apimtis ir funkcijos.
author: EricWangChen
ms.date: 09/08/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.search.form: TaxIntegrationTaxServiceParameters
ms.openlocfilehash: cafc4c7089e0c042fc65c1e3fd21f8f1e930b785
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689890"
---
# <a name="tax-calculation-overview"></a>Mokesčių skaičiavimo apžvalga

[!include [banner](../includes/banner.md)]

Mokesčių skaičiavimas yra hiper išplečiama kelių nuomotojų paslauga, įgalinanti „Global Tax Engine“ automatizuoti ir supaprastinti mokesčių nustatymo ir skaičiavimo procesą. Visiškai konfigūruotinas mokesčių modulis. Elementai, kuriuos galima konfigūruoti, apima (bet tuo neapsiribojama) apmokestinamą duomenų modelį, mokesčio kodą, mokesčių taikomumo matricą ir mokesčių skaičiavimo formulę. Mokesčių sistema veikia pagrindinių paslaugų „Microsoft Azure“ platformoje ir siūlo modernias technologiją bei proporcingai keičiamumą.

Mokesčių skaičiavimas integruoja su "Dynamics 365" finansais ir Dynamics 365 Supply Chain Management. Galiausiai ji taip pat bus „Dynamics 365 Project Operations“ integruota į, ir kitas pirmosios šalies ir trečiosios šalies „Dynamics 365 Commerce“ programas.

> [!IMPORTANT]
> Kai įgalinate papildinį Mokesčių skaičiavimas, kai kurios su susijusiais duomenimis susijusios operacijos gali būti atliekamos ne duomenų centre, kuris tvarko jūsų aptarnavimo duomenis. Prieš įgalindami papildinį Mokesčių skaičiavimas, peržiūrėkite [sąlygas](https://go.microsoft.com/fwlink/?linkid=2156043). Mes rūpinamės jūsų privatumu. Norėdami sužinoti daugiau, perskaitykite mūsų [Pareiškimą dėl privatumo](https://go.microsoft.com/fwlink/?LinkId=521839).

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
- Brazilija
- Kanada
- Europa
- Prancūzija
- Indija
- Japonija
- Pietų Afrika
- Šveicarija
- Jungtiniai Arabų Emyratai
- Jungtinė Karalystė
- Jungtinės Valstijos

> [!NOTE]
> Mokesčių skaičiavimas nepalaiko ankstesnių „Dynamics 365“ versijų, pvz., „Dynamics AX 2012“ ar vietinių „Dynamics 365“ įdiegčių.

## <a name="versions"></a>Versijos
Rekomenduojame importuoti ir nustatyti savo mokesčių skaičiavimo konfigūraciją su versija, kuri atitinka jūsų finansų arba tiekimo grandinės valdymo versiją.

| Finansų arba tiekimo grandinės valdymo versija | Mokesčių konfigūracijos versija               |
| --------------- | --------------------------------------- |
| 10.0.31         | Mokesčių skaičiavimo konfigūracija 40.56.240 |
| 10.0.30         | Mokesčių skaičiavimo konfigūracija 40.55.239 |
| 10.0.29         | Mokesčių skaičiavimo konfigūracija 40.55.236 |
| 10.0.28         | Mokesčių skaičiavimo konfigūracija 40.54.234 |
| 10.0.27         | Mokesčių skaičiavimo konfigūracija 40.54.234 |


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

Šioje lentelėje išvardijamos atitinkamoje versijoje palaikomos operacijos.

| Versija | Operacijos |
|---------|--------------|
| 10.0.29 | Periodiniai žurnalai |
| 10.0.28 | Tiekėjo mokėjimų žurnalas<br> Klientų mokėjimų žurnalas | 
| 10.0.26 | Pagrindiniai žurnalai<br> Tiekėjo SF žurnalas |
| 10.0.23 | Laisvos formos sąskaita faktūra |
| 10.0.21| Pardavimas<br><ul><li>Pardavimo pasiūlymas</li><li>Pardavimo užsakymas</li><li>Patvirtinimas</li><li>Išrinkimo dokumentas</li><li>Važtaraštis</li><li>Pardavimo sąskaita faktūra</li><li>Kredito sąskaita</li><li>Grąžinimo užsakymas</li><li>Antraštės įvairūs keitimai</li><li>Įvairių išlaidų eilutė</li></ul>Pirkimas<br><ul><li>Pirkimo užsakymas</li><li>Patvirtinimas</li><li>Gavimų sąrašas</li><li>Gavimo dokumentas</li><li>Pirkimo SF</li><li>Antraštės įvairūs keitimai</li><li>Įvairių išlaidų eilutė</li><li>Kredito sąskaita</li><li>Grąžinimo užsakymas</li><li>Pirkimo paraiška</li><li>Papildomos pirkimo paraiškos eilutės išlaidos</li><li>Pasiūlymo patvirtinimas</li><li>Pasiūlymo patvirtinimo antraštės papildomos išlaidos</li><li>Pasiūlymo patvirtinimo eilutės papildomos išlaidos</li></ul>Inventorizacijos<ul><li>Perlaidos užsakymas - siuntimas</li><li>Perlaidos užsakymas - gavimas</li></ul>|

## <a name="supported-countriesregions"></a>Palaikomos šalys / regionai

Mokesčių skaičiavimą galima paleisti naudojant palaikomas lokalizavimo priemones. Šioje lentelėje išvardijamos juridinio subjekto pagrindinio adreso šalys / regionai.

| Versija | Šalis / regionas |
|---------|----------------|
| 10.0.26 | -Kinija <br>-Čekijos Respublika<br>-Ispanija |
| 10.0.24 | Meksika |
| 10.0.23 | -Tailandas <br>-Japonija <br>-Malaizija <br>-Singapūras |
| 10.0.22 | -Australija<br>-Bahreinas <br>-Kanada<br>-Egiptas <br>– Honkongo SAR <br>-Kuveitas <br>-Naujoji Zelandija <br>-Omanas <br>-Kataras <br>- Saudo Arabų <br>-Pietų Afrika <br>- Jungtiniai Arabų Emyratai |
| 10.0.21 | -Austrija <br>-Belgija <br>-Danija <br>-Estija <br>-Suomija <br>-Prancūzija <br>-Vokietija <br>-Vengrija <br>-Islandija <br>-Airija <br>-Italija <br>-Latvija <br>-Lietuva <br>-Nyderlandai <br>-Norvegija <br>-Lenkija <br>-Švedija <br>-Šveicarija <br>-Jungtinė Karalystė <br>-Jungtinės Amerikos Valstijos |

Jei šalis / regionas nėra lokalizuotas Microsoft, mokesčių skaičiavimą taip pat galima įgalinti ir paleisti kartu su kitomis visuotinomis funkcijomis.

## <a name="related-resources"></a>Susiję ištekliai

[Darbo su mokesčių paslaugomi pradžia](./global-get-started-with-tax-calculation-service.md)

[Kelių PVM registracijų numeris](./emea-multiple-vat-registration-numbers.md)

[Mokesčių priemonės perkėlimo užsakymo palaikymas](./tasks/tax-feature-support-for-transfer-order.md)

[Kaip sukurti plėtinį mokesčių tarnybose](./tax-service-add-data-fields-tax-integration-by-extension.md)
