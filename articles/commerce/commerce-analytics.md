---
title: „Commerce“ analizė (peržiūros versija)
description: Šioje temoje paaiškinama, kaip įdiegti ir naudoti analizės galimybę Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 02/24/2022
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 7e3721421e15bc3e5937691cdbaee51e4d3cdd17
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349748"
---
# <a name="commerce-analytics-preview"></a>„Commerce“ analizė (peržiūros versija)

[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip įdiegti "Commerce Analytics" (peržiūra), funkcinę analizės galimybę, kuri įtraukta į Microsoft Dynamics 365 Commerce.

## <a name="commerce-analytics-preview-live-demo"></a>"Commerce Analytics" (peržiūra) tiesioginė parodomoji versija

Galite išbandyti " [Commerce Analytics" tiesioginį demonstracinį kodą (peržiūra)](https://aka.ms/CommerceAnalyticsDemo).

!["Commerce Analytics" (peržiūra) suvestinė](media/CommerceAnalytics_Summary.png)
!["Commerce Analytics" (peržiūra) mokėjimai](media/CommerceAnalytics_Payments.png)
!["Commerce Analytics" (peržiūros) interneto veikla](media/CommerceAnalytics_WebActivity.png)

## <a name="commerce-analytics-preview-system-architecture"></a>Komercijos analizės (peržiūros) sistemos architektūra

### <a name="key-components"></a>Pagrindiniai komponentai

"Commerce analytics" (Peržiūra) sudaro šie pagrindiniai komponentai:

- Paruoštos naudoti interaktyvios Power BI ataskaitos
- SQL rodiniai Azure Synapse Analytics
- Objekto ir ontologijos duomenys "Azure Data Azure"
- Neapdoroti duomenys duomenų sąs.

![Pagrindiniai "Commerce Analytics" sistemos architektūros komponentai](media/CommerceAnalyticsArchitecture_v2.png)

### <a name="data-flow"></a>Duomenų srautas

#### <a name="step-1-data-generation"></a>1 veiksmas: duomenų generavimas

Duomenys kyla iš vieno iš šių šaltinių kaip operacijų duomenys arba veikimo būdo duomenys:

- Skambučių centras susieja pardavimo užsakymus naudojant "Commerce HQ" klientą.
- Kasininkas kasininkas kasos aparate (EKA) apdoroja pardavimo operacijas.
- Pardavimas kuriamas pasirinktinėse programose naudojant "Headless Commerce" ("Commerce Scale Unit").
- El. komercijos pardavėjas naršo jūsų el. komercijos svetainę.
- El. komercijos pardavėjas jūsų el. komercijos svetainėje gali užsakyti užsakymą.
- Duomenis gamina kitos sistemos, pvz.,Dynamics 365 Connected Spaces

#### <a name="step-2-ingestion-and-pre-processing"></a>2 žingsnis: įdinimas ir išankstinis apdorojimas

Operacijų duomenys eina į "Commerce HQ" tiesiogiai (jei užsakymai užfiksuoti tiesiogiai "Commerce HQ" kliente) arba per "Commerce Scale Unit" (jei užsakymai užfiksuoti EKA, el. prekyboje arba pasirinktiniuose klientuose, kurie naudoja "Headless Commerce").

Tada eksportavimo į duomenis funkcija yra naudojama operacijų duomenims kopijuoti į jūsų duomenis kaip neapdorotus duomenis. Neapdoroti duomenys saugomi duomenų aplanke Lentelės.

El. komercijos interneto veiklos duomenys siunčiami tiesiai į duomenų failą. Duomenys, kuriuos gamina kitos sistemos, Dynamics 365 Connected Spaces pvz., yra siunčiami tiesiai į šių sistemų duomenis.

#### <a name="step-3-transformation-and-aggregation"></a>3 žingsnis: pakeitimas ir sujungimas

Kai neapdoroti duomenys yra jūsų duomenų formoje, "Commerce analytics" tarnyba jį perskaito, transformuoja, sujungiami ir įrašo duomenis į loginių objektų formą (aplanke Objektai) ir sudeda metriką (Aplanke Ontologies).

#### <a name="step-4-querying"></a>4 žingsnis: užklausimas

Azure Synapse Analytics naudojamas duomenų užklausos per Transact-SQL (T-SQL) sąsają duomenims pateikti. Ši sąsaja apima SQL rodinius. SQL rodiniai leidžia duomenų bendrą užklausą duomenų užklausose tiesiogiai per T-SQL klientą (ad hoc analizei) arba vizualizavimo įrankį, pavyzdžiui Power BI, .

#### <a name="step-5-modeling-and-serving"></a>5 žingsnis: modeliavimas ir aptarnavimas

Duomenys, kurių užklausia, Azure Synapse Analytics eina į Power BI semantinio modelio. Atsižvelgiant į duomenų tipą, jie periodiškai Power BI importuojami į atmintį arba tiesiogiai užklausuojami apdorojimo laiku.

Galiausiai duomenys atvaizduojami vaizduose Power BI, kad vartotojai galėtų juos peržiūrėti ir su jais sąveikauti.

## <a name="commerce-analytics-preview-functional-overview"></a>Komercijos analizės (peržiūros) funkcinė apžvalga

### <a name="summary"></a>Suvestinė

"Commerce Analytics" šablono programoje yra šie pagrindiniai ataskaitos puslapiai:

1. [Aukščiausio lygio filtrai](#TopLevelFilters)
2. [Produktai](#ProductsPage)
3. [Klientai](#CustomersPage)
4. [Kanalai](#ChannelsPage)
5. [Pardavimas](#SalesPage)
6. [Paraštės](#MarginsPage)
7. [Grąžinimas](#ReturnsPage)
8. [Nuolaidos](#DiscountsPage)
9. [Mokėjimai](#PaymentsPage)
10. [Klientai](#CustomersPage)
11. [Palyginimas](#ComparisonPage)
12. [Žiniatinklio veikla](#WebActivityPage)
13. [Interneto veikla – aukščiausio lygio filtras](#WebActivityTopLevelFilters)

#### <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Aukščiausio lygio filtrai

- Datos parametrai

    - Metai
    - Ketvirtis
    - Mėnuo
    - Savaitė
    - Diena

- Kanalo parametrai

    - Juridinis subjektas
    - Kanalo tipas
    - Kliento tipas
    - Pardavimo tipas
    - Kanalas
    - Organizacijos hierarchija

- Produkto parametrai

    - Kategorijų hierarchija
    - Kategorija

#### <a name="products"></a><a name="ProductsPage"></a> Produktų

- Pardavimas
- Paraštės
- Grąžinimas

#### <a name="customers"></a><a name="CustomersPage"></a> Klientai

- Pardavimas
- Paraštės
- Grąžinimas

#### <a name="channels"></a><a name="ChannelsPage"></a> Kanalai

- Pardavimas
- Paraštės
- Grąžinimas

### <a name="sales"></a>Pardavimo<a name="SalesPage"></a>

- Pagal pristatymo vietą
- Pagal kanalą / parduotuvę / mokėjimo terminalą
- Pagal darbuotoją
- Pagal datą
- Pagal valandą
- Pagal produkto kategoriją

### <a name="margins"></a><a name="MarginsPage"></a> Paraštės

- Pagal pristatymo vietą
- Šalutinis produktas
- Pagal datą

### <a name="returns"></a><a name="ReturnsPage"></a> Grąžina

- Grąžinimas pagal sumą

    - Pagal parduotuvę
    - Šalutinis produktas
    - Pagal datą

- Grąžinimas pagal operaciją

    - Pagal parduotuvę
    - Šalutinis produktas
    - Pagal datą

### <a name="discounts"></a><a name="DiscountsPage"></a> Nuolaidos

- Pagal parduotuvę
- Šalutinis produktas
- Pagal datą
- Paskirstymas

    - Juridinis subjektas
    - Parduotuvė
    - Nuolaidos tipas
    - Nuolaidos pavadinimas
    - Produktas

### <a name="payments"></a><a name="PaymentsPage"></a> Mokėjimai

- Pagal kanalą / terminalą
- Pagal mokėjimo būdą/tipą
- Pagal datą
- Paskirstymas

    - Juridinis subjektas
    - Kanalo tipas
    - Parduotuvė
    - Mokėjimo terminalas
    - Mokėjimo būdas

### <a name="customers"></a><a name="CustomersPage"></a> Klientai

- Laikotarpio vertė (LTV)

    LTV apskaičiuojamas pagal bendrą sumą, kurią klientas Dynamics 365 Commerce praleidžia visuose pardavimo kanaluose (įskaitant EKA, el. prekybas ir skambučių centrą).

- Recency

    "Recency" skaičiuojamas pagal dienų skaičių nuo paskutinio kliento įsipareigojimo atlikti operaciją organizacijoje. Šiuo metu "recency" atsižvelkite į ne operacijos įsipareigojimo signalus, pvz., el. komercijos naršymo veiklą.

- Dažnumas

    Dažnumas skaičiuojamas remiantis kliento įsipareigojimu atlikti operaciją su organizacija. Šiuo metu dažnumas atsižvelkite į ne operacijos įsipareigojimų signalus, pvz., el. komercijos naršymo veiklą.

- Ryšio ilgis

    Ryšio ilgis skaičiuojamas pagal dienų skaičių, skaičiuojant nuo tada, kai sistemoje buvo sukurtas kliento įrašas.

- Operacijų skaičius

### <a name="comparison"></a><a name="ComparisonPage"></a> Palyginimas

- Produktų palyginimas pagal laikotarpį

    - Pardavimo ir pardavimo skirtumas
    - Marža ir maržos skirtumas

- Klientas pagal laikotarpį

    - Pardavimo ir pardavimo skirtumas
    - Marža ir maržos skirtumas

### <a name="web-activity"></a><a name="WebActivityPage"></a> Interneto veikla

#### <a name="top-level-filters"></a><a name="WebActivityTopLevelFilters"></a> Aukščiausio lygio filtrai

- Datų diapazonas
- Kanalo tipas
- Kanalas
- Kategorijų hierarchija

#### <a name="acquisitions"></a>Įsigijimai

- Puslapių rodiniai

    - Pagal šalį arba regioną
    - Šalutinis produktas
    - Pagal vartotojo prisiregistravęs būseną
    - Pagal datą

- El. komercijos užsakymai
- Konvertavimo kursas

    - Pagal datą

- Konvertavimo piltuvėlis

    - Puslapio rodinys pagal puslapio tipą (pagrindinis puslapis, kategorijos puslapis arba produkto informacijos puslapis)
    - Įtraukti į krepšelį
    - Užbaigti pirkimą
    - Pirkimas

#### <a name="sessions"></a>Seansai

Seansas yra vartotojo apsilankymo jūsų el. komercijos svetainėje dalis. Seansas laikomas baigtu po 30 minučių neaktyvumo arba 24 valandų aktyvaus naudojimo.

- Pagal šalį arba regioną
- Pagal kilmę (išorinis nurodantis)
- Pagal vartotojo prisiregistravęs būseną
- Seansų skaičius

    - Pagal datą
    - Pagal įrašo puslapį

- Užsakymas pagal seansą

    - Pagal datą

- Seansų koeficientas

    Seansas yra seansas, kuriame vartotojas išeina iš karto po to, kai aplankys jūsų el. komercijos svetainę. Daugiau informacijos ieškokite Koeficiento koeficiente.<a1/&a1><a2/ [&a3>](https://en.wikipedia.org/wiki/Bounce_rate)

- Spusteli per seansą

#### <a name="visitors"></a>Lankytojai

Anoniminis naudojimas jūsų el. prekybos svetainėje identifikuojamas unikaliai, remiantis konkrečia naršykle ir konkrečiu įrenginiu, kurį naudoja vartotojas. "Commerce Analytics" nesekti anoniminių anonimas skirtingose naršyklėse arba įrenginiuose. Anoniminis, kuris naudoja tą pačią naršyklę tame pačiame įrenginyje, unikaliai identifikuojamas keliuose vartotojo seansuose, kol naršyklės talpykloje esantys duomenys išvalomi arba išlaikomas laikotarpis (paprastai 12 mėnesių), t. y. tas, kuris iš pradžių įvyksta.

Jei pagal savo el. prekybos svetainę naršote prisiregistravę, "Commerce Analytics" gali pateikti papildomos informacijos apie jas. Ši informacija yra pagrįsta esamais ryšiais, kuriuos jūsų organizacija turi su dabartiniais pirkimo užsakymais visuose pardavimo kanaluose (įskaitant EKA, el. prekybas Dynamics 365 Commerce ir skambučių centrą). Papildoma informacija apima "recency", ryšio ilgį, laikotarpio vertę ir dažnio duomenis.

- Veiksmų marža
- Vidutinis gamybos užsakymų skaičius
- Vidutinis pardavimų vidurkis
- El. komercijos operacijų skaičius

    - Pagal datą
    - Pagal vietą

        Šiuo metu "Commerce analytics" gali pateikti tik šalies / regiono lygio detalumą, kad būtų galima geriau suprasti el. komercijos duomenis.

    - Pagal "recency"

        "Recency" skaičiuojamas pagal dienų skaičių nuo paskutinio kliento įsipareigojimo atlikti operaciją organizacijoje. Šiuo metu "recency" atsižvelkite į ne operacijos įsipareigojimo signalus, pvz., el. komercijos naršymo veiklą.

    - Pagal ryšio ilgį

        Ryšio ilgis skaičiuojamas pagal dienų skaičių, skaičiuojant nuo tada, kai sistemoje buvo sukurtas kliento įrašas.

    - Pagal naudojimo laikotarpio vertę (LTV)

        LTV apskaičiuojamas pagal bendrą sumą, kurią klientas Dynamics 365 Commerce praleidžia visuose pardavimo kanaluose (įskaitant EKA, el. prekybas ir skambučių centrą).

    - Pagal dažnumą

        Dažnumas skaičiuojamas remiantis kliento įsipareigojimu atlikti operaciją su organizacija. Šiuo metu dažnumas atsižvelkite į ne operacijos įsipareigojimų signalus, pvz., el. komercijos naršymo veiklą.

#### <a name="impressions"></a>Parodymų

Įspūdis yra vienas el. komercijos rodinio produkto vaizdo rodinys. Pavyzdžiui, el. komercijos programa eina į pagrindinį jūsų el. komercijos svetainės puslapį ir pardavimo sąrašo pagrindiniame modulyje rodo matų **produktą**. Tada galėsite peržiūrėti tą patį matų produktą modulio **Paėmimai** modulyje. Šiuo atveju, egzistuoja du produkto įspūdis.

Šiuo metu įspūdis sekamas toliau pažymėtuose paviršių:

- Sąrašai (pvz., Rekomenduojama, Parduodama viršuje **,** Paėmimai jums **ir Tendencija** **)** **·**
- Krepšelio modulis
- Ieškos rezultatų konteineris
- Kategorijos ieškos rezultatų konteineris

Šiuo metu produktai, atvaizduoti karuso modulyje arba pasirinktiniuose vaizduose, neskaičiuojami pagal klaidingą metriką.

**Ataskaitoje apie** įspūdį pateikiama ši metrika:

- Įspūdis

    - Pagal puslapio tipą ir modulį

        Puslapio tipas yra bendrasis puslapio tipas, kuris nustatomas kiekvienam jūsų el. komercijos svetainės puslapiui. Modulio tipas yra el. komercijos vaizdo modulio, kuriame rodomas produktas, tipas.

        Norėdami peržiūrėti regėjimus pagal modulį, galite detalizuoti ir peržiūrėti puslapio ir modulio vaizdo vaizdą.

    - Šalutinis produktas
    - Pagal vartotojo prisiregistravęs būseną
    - Pagal datą

- Atspaudų spustelėjimu skaičius

    Įspūdis spustelimas, kai el. komercijos procesas pasirenka produkto vaizdo failą. Paprastai jis imamas į produkto informacijos puslapį.

- Įspūdis dėl spustelėtų tarifas (CTR)

    CTR skaičiuojamas kaip bendras priešingų spustelėjimus skaičius, padalintas iš viso įspūdių skaičiaus.

## <a name="commerce-analytics-preview-installation"></a>"Commerce analytics" (peržiūros) diegimas

> [!NOTE]
> Komercijos analitikai (Peržiūra) peržiūrimi Jungtinių Valstijų, Kanados, Jungtinės Karalystės, Europos, Pietų Rytų Azijos, Rytų Azijos, Australijos ir Japonijos regionuose. Jei jūsų finansų ir operacijų aplinka yra bet kuriame iš šių regionų, Microsoft Dynamics šią funkciją galite įjungti savo aplinkoje naudodami vykdymo ciklo tarnybas (LCS). Prieš naudodami šią funkciją žr. Konfigūruoti eksportavimą [į "Azure Data Azure"](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>"Commerce Analytics" įgalinkite ir konfigūruokite (peržiūra)

Norėdami įdiegti "Commerce Analytics" (peržiūra), turite turėti teises kurti išteklius "Azure" abonemente. Be to, turite turėti teises diegti papildiniai LCS. 

Norėdami įjungti ir konfigūruoti "Commerce analytics" (peržiūra), atlikite šiuos veiksmus.

1. [Įgalinkite ir sukonfigūruokite eksportavimo į duomenų " priedą](#enableExportToDataLake).
1. [Įdiekite ir konfigūruokite darbo Azure Synapse sritį](#configureAzureSynapse).
1. [Įtraukti paslapčių į rakto saugyklą](#addSecrets).
1. [Įjunkite ir sukonfigūruokite "Commerce Analytics" (peržiūra) priedą](#enableCommerceAnalyticsAddin).
1. [Įdiekite šablono Power BI programą](#powerbi).

### <a name="enable-and-configure-the-export-to-data-lake-add-in"></a><a name="enableExportToDataLake"></a> Įjungti ir konfigūruoti eksportavimo į duomenų į duomenų papildą

> [!IMPORTANT]
> Kai konfigūruojate papildinį Eksportuoti į duomenis, išvalykite žymės langelį "Real-time data **changes", kuris yra eksportavimo į duomenų portalo papildinyje nustatymo puslapį, norėdami užtikrinti,** kad pakeitimai realiuoju laiku nėra įgalinti. Peržiūrima **"Real-time Data** Changes" funkcija, todėl "Commerce Analytics" šiuo metu nepalaiko. Jei įgalinsite šią funkciją, "Commerce Analytics" negalės apdoroti jūsų duomenų duomenų pagal duomenų", Power BI o daugelis iš jūsų ataskaitų nerodo duomenų.

"Commerce analytics" (Preview) pasitiki eksportavimo į duomenis "Commerce Headquarters" duomenimis eksportavimo į duomenis į "Commerce Headquarters" funkciją ir išsaugoti duomenis iš naujo. Prieš konfigūruojant "Commerce Analytics" (peržiūra), įgalinkite ir konfigūruokite "Export to Data Azure", [atlikdami veiksmus, aprašytus dalyje Konfigūruoti eksportavimą į "Azure Data Azure"](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

Sukonfigūruokite eksportavimo į duomenų Portalo priedą, pasižymkite pastabą apie šią informaciją, nes jums reikės ją įvesti vėliau:

- <a name="keyVault"></a> Jūsų pateiktos saugyklos domeno vardų sistemos (DNS) pavadinimas.
- Jūsų pateikti slapti vardai, kuriuose yra prašymo ID ir programos slaptojo sąrašo. Daugiau informacijos rasite įtraukti [paslapčių į rakto "Vault"](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a> Darbo srities diegimas ir konfigūravimas Azure Synapse

"Commerce Analytics" (peržiūra) reikalauja, kad jūsų darbo srityje būtų galima parengti "Synapse SQL" pagal Azure Synapse poreikį. Norėdami įdiegti ir konfigūruoti darbo sritį Azure Synapse, atlikite šiuos veiksmus.

1. Įdiekite darbo sritį Azure Synapse savo "Azure" abonemente. Daugiau informacijos rasite Quickstart [: Synapse darbo srities kūrimas](/azure/synapse-analytics/quickstart-create-workspace).
1. <a name="serverlessep"></a> Sukonsologinę darbo sritį, atidarykite išteklių peržiūros puslapį ir pasižymėkite serverio be **serverio SQL galinio punkto** vertę. Šią vertę turėsite saugoti kitame skyriuje "Key Vault".
1. Peržiūros puslapyje pasirinkite saitą Atidaryti " **Synapse Studio"**, norėdami atidaryti savo Azure Synapse darbo srities studiją.
1. Kairiajame **meniu** pasirinkite Valdyti. Norėdami matyti meniu pavadinimus, kairiajame meniu jums gali tekti pasirinkti išskleisti saitą.
1. Dalyje **Saugos grupė** pasirinkite Prieigos **valdymas**. 
1. Pasirinkite **Įtraukti**.
1. Srityje Įtraukti **vaidmens priskyrimą** nustatykite pasirinktis, kaip aprašyta šioje lentelėje.

    | Parinktis | Reikšmė |
    |--------|-------|
    | Aprėptis | Pasirinkite darbo **sritį**. |
    | Vaidmuo | Pasirinkite **Sinapse SQL administratorių**.|
    | Pasirinkti vartotoją | Ieškoti programos, kurią sukūrėte diegiant [eksportavimo į duomenis į duomenų priedą metu, pavadinimo](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createapplication). Kai programa pasirodo ieškos rezultatuose, pasirinkite ją. Programa bus rodoma pasirinktų vartotojų **, grupių ar aptarnavimo pagrindinio skyriaus** skyriuje. |

1. Pasirinkite **Taikyti,** jei norite baigti vaidmens priskyrimą. Programai suteikiamos sinapsės SQL administratoriaus teisės. Todėl konfigūracijoje "Commerce Analytics (Preview) LCS" ji gali kurti reikiamus rodinius.

### <a name="add-secrets-to-the-key-vault"></a><a name="addSecrets"></a> Įtraukti paslapčių į rakto saugyklą

Tame pačiame rakte [" vault](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createkeyvault) ", kurį naudojote konfigūruojant papildinį Eksportuoti į duomenų portalą, turite įtraukti šioje lentelėje rodomas paslapdas. Kiekvienam slaptui jūs turite pateikti slaptą pavadinimą ir nurodytą vertę.

| Pasiūlytas slapto pavadinimas | Slaptojo rakto reikšmė | Slaptos reikšmės pavyzdys |
|---------|---------|---------|
| sinapse-sql serveris | Serverio lauko SQL galinio punkto vertė, kurią nurodėte konfigūravote [darbo Azure Synapse sritį](#serverlessep). | `test-ondemand.sql.azuresynapse.net` |
| <a name="roUser"></a> readonly-sql-p tarp | Slaptažodis, kurį reikia nustatyti SQL tik skaityti skirtame vartotojui. Ataskaita Power BI turės naudoti šį slaptažodį, kad prisijungtų prie serverio serverio SQL. Norėdami nustatyti slaptažodį, vadovaukitės savo organizacijos slaptažodžio strategija. | |

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a> Įgalinti ir konfigūruoti "Commerce Analytics" (peržiūra) priedą

Norėdami įdiegti "Commerce Analytics" (peržiūra) priedą LCS, turite būti LCS aplinkos administratorius, kad būtų galima naudoti aplinką.

Norėdami įdiegti ir konfigūruoti "Commerce Analytics" (peržiūra) priedą, atlikite šiuos veiksmus.

1. Prisiregistruokite [prie LCS](https://lcs.dynamics.com/) ir eikite į aplinką.
2. **Aplinkos puslapio** skirtuke **Aplinkos papildiniai** pasirinkite **Diegti naują priedą**.
3. Dialogo lange pasirinkite " **Commerce analytics" (peržiūra).**-
4. **Nustatymo priedo dialogo** lange įveskite šią informaciją.

    | Informacija | Šaltinis | Reikšmės pavyzdys |
    |---|---|---|
    | Azure Active Directory(Azure AD) Nuomininko ID | Prisiregistruokite prie " [Azure" portalo](https://portal.azure.com/) ir atidarykite **Azure Active Directory** paslaugą. Tada atidarykite **puslapį** Ypatybės ir nukopijuokite vertę lauke **Nuomininko ID**. | `72f988bf-0000-0000-00000-2d7cd011db47` |
    | "Azure" rakto saugyklos DNS pavadinimas | Įveskite savo rakto saugyklos DNS pavadinimą. Sukonfigūruokite eksportavimo [į duomenų portalą priedą, turite pateikti šios vertės pastabą](#keyVault). | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Slapto pavadinimo, kuriame yra programos ID, pavadinimas | Įvesti slaptą pavadinimą, kuriame saugomas programos ID. Sukonfigūruokite eksportavimo [į duomenų portalą priedą, turite pateikti šios vertės pastabą](#keyVault). | `app-id` |
    | Slapto pavadinimas, kuriame yra prašymo slapto vardo | Įvesti slaptą pavadinimą, kuriame saugomas programos slapyme. Sukonfigūruokite eksportavimo [į duomenų portalą priedą, turite pateikti šios vertės pastabą](#keyVault). | `app-secret` |
    | Slapto pavadinimo, kuriame yra serverio nesamas SQL galinis punktas Azure Synapse | Įvesti slaptą pavadinimą, kuriame saugomas serverio serverio duomenų galinis punktas. Jūs turėjote sukurti slaptą, kol pridėti [slapyme paslapyme turi būti rakto vertės.](#addSecrets) | `synapse-sql-server` |
    | Slaptažodis, kuriame yra slaptažodis, nustatytas SQL tik skaityti vartotojams Azure Synapse | Įveskite slaptą pavadinimą, kuriame saugomas slaptažodis, skirtas nustatyti vartotojui, kuriame leidžiama tik skaityti serveryje. Šis vartotojas bus sukurtas už jus ir jis turėtų būti naudojamas Power BI ataskaitoje prisijungti prie serverio serverio neturintis SQL serveris. Jūs turėtumėte sukurti slaptą, kai įtraukėte [slapymečių į rakto vertę](#addSecrets). | `readonly-sql-pwd` |

1. Sutikite su pasiūlymo sąlygomis pažymėdami žymės langelį ir pasirinkite **Diegti**.

    Sistema įdiegia ir sukonfigūruoja "Commerce Analytics" (peržiūra) aplinkos priedą. Šis procesas gali užtrukti keletą minučių. Kai jis baigtas, "**Commerce Analytics" (Peržiūra)** turi būti įrašyta į **aplinkos** puslapį ir būsena turi būti **Įdiegta**.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a> Šablono programos Power BI diegimas

Norėdami įdiegti " Power BI Commerce Analytics" šablono programą (peržiūra), atlikite šiuos veiksmus.

1. Prisiregistruokite portale [Power BI](https://powerbi.microsoft.com/) naudodami savo organizacijos ID.
1. Įdiekite "Commerce Analytics" (peržiūros) Power BI šablonų programą nueidami į [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Taip pat eikite į [AppSource analizės puslapį Dynamics 365 Commerce ir](https://appsource.microsoft.com/product/power-bi/dynamics-365-commerce.dydnamics-365-commerce-analytics) pasirinkite **Gauti dabar**.
1. Jei programą iš naujo įdiegiate pirmą kartą, praleiskite toliau 5 veiksmą. Jei jau įdiegėte jį anksčiau, taikomos šios programos naujinimo parinktys:

    - **Atnaujinkite darbo sritį ir programą** – atnaujinkite esamą šablono programą ir perrašykite esamus programos parametrus, pvz., programos egzemplioriaus pavadinimą ir teisių konfigūracijas.
    - **Atnaujinkite tik darbo srities turinį neatnaujinę programos** – atnaujinkite esamą šablono programą, bet išlaikykite esamus programos parametrus. *Ši pasirinktis yra rekomenduojama programos naujinimų parinktis.*
    - **Įdiekite kitą programos kopiją į naują darbo sritį** – sukurkite naują darbo sritį, tada sukurkite joje esančios šablono programos kopiją. Esama darbo sritis bus atgaktyva.

1. Pasirinkite vieną iš naujinimo pasirinkčių, tada pasirinkite **Diegti**.
1. Atidarykite įdiegtą programą kairiajame **lange** pasirinkdami Programėlės ir ją pasirinkdami.
1. Prijunkite programą prie duomenų šaltinio pasirinkdami **Prisijungti**. Jei programą įdiegėte prieš tai, geltoname pranešimų **juostoje** pasirinkite duomenų saito jungtį Prijungti.
1. Užpildykite toliau nurodytus laukus.

    | Laukas | Reikšmė |
    |---|---|
    | Serveris | Įvesti serverio negalinį SQL galinį punktą, apie kurį padarėte pastabą sukūrę [darbo Azure Synapse sritį](#serverlessep). |
    | Duomenų bazė | Įvesti **CommerceAnalytics**. |
    | Kalba | Pasirinkti vertę iš sąrašo. Šis laukas naudojamas lokalizuoties produktų ir kategorijų pavadinimams. Ši vertė abc nuo abc. |
    | Datų diapazonas | Pasirinkti vertę iš sąrašo. Pasirinkto mėnesių skaičiaus duomenys bus importuoti į duomenų Power BI rinkinį. Jūsų parenkama reikšmė turi įtakos duomenų rinkinio dydžiui ir sinchronizavimui reikalingas laikas. |

1. Pasirinkite **Toliau**. Kai būsite paraginti įvesti kredencialus, kad Azure Synapse būtų galima prisijungti prie SQL duomenų bazės, nustatykite lauko vertes, kaip parodyta pateiktoje lentelėje.

    | Laukas | Reikšmė |
    |---|---|
    | Autentifikavimo metodas | Pasirinkite **pagrindinį**. |
    | Vartotojo vardas | Įvesti **reportreadonlyuser**. |
    | Slaptažodis | Įveskite slaptažodį, kurį [išsaugote "SQL" tik skaitymo vartotojui "key vault"](#roUser). |

1. Pasirinkite **prisijungimą ir prisijungimą**.
1. Palaukite, kol duomenų rinkinys bus sėkmingai atnaujintas. Tada pasirinkite **Redaguoti programą**, norėdami atidaryti programos darbo sritį, kurioje galite peržiūrėti duomenų rinkinio atnaujinimo būseną. Programos darbo srityje taip pat galite pasirinktinai nustatyti automatinio duomenų rinkinio naujinimo grafikus, valdyti teises ir pervardyti programos egzempliorių.

### <a name="privacy"></a><a name="privacy"></a>Privatumas

Mes rūpinamės jūsų privatumu. Norėdami sužinoti daugiau, perskaitykite mūsų [Pareiškimą dėl privatumo](https://go.microsoft.com/fwlink/?LinkId=521839).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
