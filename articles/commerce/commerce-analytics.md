---
title: Komercijos analitikai (peržiūra)
description: Šioje temoje paaiškinama, kaip įdiegti ir naudoti analizės galimybę Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 11/23/2021
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 8cfe2af756315b5be3eb22d99376a96166fffc52
ms.sourcegitcommit: f9fca3d55b47e615e5ef64669dab184e057ec234
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/23/2021
ms.locfileid: "7862778"
---
# <a name="commerce-analytics-preview"></a>Komercijos analitikai (peržiūra)

[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip įdiegti "Commerce Analytics" (peržiūra), funkcinę analizės galimybę, kuri įtraukta į Microsoft Dynamics 365 Commerce.

## <a name="commerce-analytics-preview-live-demo"></a>"Commerce Analytics" (peržiūra) tiesioginė parodomoji versija

Galite išbandyti ["Commerce Analytics" tiesioginį demonstracinį kodą (peržiūra)](https://aka.ms/CommerceAnalyticsDemo).

!["Commerce Analytics" (peržiūra) suvestinė](media/CommerceAnalytics_Summary.png)
!["Commerce Analytics" (peržiūra) mokėjimai](media/CommerceAnalytics_Payments.png)
!["Commerce Analytics" (peržiūros) interneto veikla](media/CommerceAnalytics_WebActivity.png)


## <a name="commerce-analytics-preview-system-architecture"></a>Komercijos analizės (peržiūros) sistemos architektūra

### <a name="key-components"></a>Pagrindiniai komponentai

"Commerce analytics" (Peržiūra) sudaro šie pagrindiniai komponentai:

- Paruoštos naudoti interaktyvios Power BI ataskaitos
- SQL rodiniai Azure Synapse analitikoje
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
- Duomenis gamina kitos sistemos, Dynamics 365 Connected Spaces pvz.,

#### <a name="step-2-ingestion-and-pre-processing"></a>2 žingsnis: įdinimas ir išankstinis apdorojimas

Operacijų duomenys eina į "Commerce HQ" tiesiogiai (jei užsakymai užfiksuoti tiesiogiai "Commerce HQ" kliente) arba per "Commerce Scale Unit" (jei užsakymai užfiksuoti EKA, el. prekyboje arba pasirinktiniuose klientuose, kurie naudoja "Headless Commerce").

Tada eksportavimo į duomenis funkcija yra naudojama operacijų duomenims kopijuoti į jūsų duomenis kaip neapdorotus duomenis. Neapdoroti duomenys saugomi duomenų aplanke Lentelės.

El. komercijos interneto veiklos duomenys siunčiami tiesiai į duomenų failą. Duomenys, kuriuos gamina kitos sistemos, Dynamics 365 Connected Spaces pvz., yra siunčiami tiesiai į šių sistemų duomenis.

#### <a name="step-3-transformation-and-aggregation"></a>3 žingsnis: pakeitimas ir sujungimas

Kai neapdoroti duomenys yra jūsų duomenų formoje, "Commerce analytics" tarnyba jį perskaito, transformuoja, sujungiami ir įrašo duomenis į loginių objektų formą (aplanke Objektai) ir sudeda metriką (Aplanke Ontologies).

#### <a name="step-4-querying"></a>4 žingsnis: užklausimas

Azure Synapse Analitika naudojama duomenų užklausai pateikti naudojant Transact-SQL (T-SQL) sąsają. Ši sąsaja apima SQL rodinius. SQL rodiniai leidžia duomenų bendrą užklausą duomenų užklausose tiesiogiai per T-SQL klientą (ad hoc analizei) arba vizualizavimo įrankį, Power BI pavyzdžiui, .

#### <a name="step-5-modeling-and-serving"></a>5 žingsnis: modeliavimas ir aptarnavimas

Duomenys, kurių užklausia Azure Synapse "Analytics", Power BI pereina į semantinio modelio modelį. Atsižvelgiant į duomenų tipą, jie periodiškai importuojami į atmintį arba tiesiogiai užklausuojami Power BI apdorojimo laiku.

Galiausiai duomenys atvaizduojami Power BI vaizduose, kad vartotojai galėtų juos peržiūrėti ir su jais sąveikauti.

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

####  <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Aukščiausio lygio filtrai

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

####  <a name="products"></a><a name="ProductsPage"></a> Produktų

- Pardavimas
- Paraštės
- Grąžinimas

####  <a name="customers"></a><a name="CustomersPage"></a> Klientai

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

    LTV apskaičiuojamas pagal bendrą sumą, kurią klientas praleidžia visuose pardavimo Dynamics 365 Commerce kanaluose (įskaitant EKA, el. prekybas ir skambučių centrą).

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
    - Dėti į krepšelį
    - Pirkimo užbaigimas
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

    Seansas yra seansas, kuriame vartotojas išeina iš karto po to, kai aplankys jūsų el. komercijos svetainę. Daugiau informacijos ieškokite [Koeficiento koeficiente.<a1/&a1><a2/&a3>](https://en.wikipedia.org/wiki/Bounce_rate)

- Spusteli per seansą

#### <a name="visitors"></a>Lankytojai

Anoniminis naudojimas jūsų el. prekybos svetainėje identifikuojamas unikaliai, remiantis konkrečia naršykle ir konkrečiu įrenginiu, kurį naudoja vartotojas. "Commerce Analytics" nesekti anoniminių anonimas skirtingose naršyklėse arba įrenginiuose. Anoniminis, kuris naudoja tą pačią naršyklę tame pačiame įrenginyje, unikaliai identifikuojamas keliuose vartotojo seansuose, kol naršyklės talpykloje esantys duomenys išvalomi arba išlaikomas laikotarpis (paprastai 12 mėnesių), t. y. tas, kuris iš pradžių įvyksta.

Jei pagal savo el. prekybos svetainę naršote prisiregistravę, "Commerce Analytics" gali pateikti papildomos informacijos apie jas. Ši informacija yra pagrįsta esamais ryšiais, kuriuos jūsų organizacija turi su dabartiniais pirkimo užsakymais visuose pardavimo kanaluose Dynamics 365 Commerce (įskaitant EKA, el. prekybas ir skambučių centrą). Papildoma informacija apima "recency", ryšio ilgį, laikotarpio vertę ir dažnio duomenis.

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

        LTV apskaičiuojamas pagal bendrą sumą, kurią klientas praleidžia visuose pardavimo Dynamics 365 Commerce kanaluose (įskaitant EKA, el. prekybas ir skambučių centrą).

    - Pagal dažnumą

        Dažnumas skaičiuojamas remiantis kliento įsipareigojimu atlikti operaciją su organizacija. Šiuo metu dažnumas atsižvelkite į ne operacijos įsipareigojimų signalus, pvz., el. komercijos naršymo veiklą.

#### <a name="impressions"></a>Parodymų

Įspūdis yra vienas el. komercijos rodinio produkto vaizdo rodinys. Pavyzdžiui, el. komercijos programa eina į pagrindinį jūsų el. komercijos svetainės puslapį ir pardavimo sąrašo pagrindiniame modulyje rodo **matų** produktą. Tada galėsite peržiūrėti tą patį matų produktą modulio **Paėmimai** modulyje. Šiuo atveju, egzistuoja du produkto įspūdis. 

Šiuo metu įspūdis sekamas toliau pažymėtuose paviršių:

- Sąrašai (pvz., **Rekomenduojama**, **Parduodama** viršuje, **Paėmimai** jums ir **Tendencija**)
- Krepšelio modulis
- Ieškos rezultatų konteineris
- Kategorijos ieškos rezultatų konteineris

Šiuo metu produktai, atvaizduoti karuso modulyje arba pasirinktiniuose vaizduose, neskaičiuojami pagal klaidingą metriką.

**Ataskaitoje** apie įspūdį pateikiama ši metrika:

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
> Komercijos analitikai (Peržiūra) peržiūrimi Jungtinių Valstijų, Kanados, Jungtinės Karalystės, Europos, Pietų Rytų Azijos, Rytų Azijos, Australijos ir Japonijos regionuose. Jei jūsų aplinka yra bet kuriame iš šių regionų, šią funkciją galite įjungti savo aplinkoje naudodami ciklo Finance and Operations Microsoft Dynamics tarnybas (LCS). Prieš naudodami šią funkciją žr. Konfigūruoti [eksportavimą į "Azure Data](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) Azure".

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>"Commerce Analytics" įgalinkite ir konfigūruokite (peržiūra)

Norėdami įdiegti "Commerce Analytics" (peržiūra), turite turėti teises kurti išteklius "Azure" abonemente. Be to, turite turėti teises diegti papildiniai LCS. Čia pateikiama veiksmų apžvalga:

1. [Pateikti "Commerce Analytics" peržiūros formą](#joinPreview) (peržiūra).
2. [Įgalinti ir konfigūruoti eksportavimą į duomenų](#enableExportToDataLake) importavimą.
3. [Įjunkite ir sukonfigūruokite "Commerce Analytics" (peržiūra)](#enableCommerceAnalyticsAddin) priedą.
4. [Sugeneruokite jūsų saugojimo sąskaitos bendrai naudojamos prieigos parašo (SAS) atpažinimo](#getSASToken) ženklą.
5. [Atsisiųskite diegimo scenarijus Azure Synapse](#downloadSynapseDeploymentScripts) rodiniuose.
6. [Įdiekite ir konfigūruokite Azure Synapse darbo](#configureAzureSynapse) sritį.
7. [Įdiekite Power BI šablono](#powerbi) programą.

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a> Pateikti "Commerce Analytics" peržiūros formą (peržiūra)

Pateikti ["Commerce Analytics" peržiūros formą](https://forms.office.com/r/vW5VLJGXZ2) (peržiūra). Leisti apdoroti formą iki trijų darbo dienų. Jį apdorous, patvirtinimo el. laiškas bus nusiųstas el. pašto adresu, kurį pateikėte formoje.

### <a name="enable-and-configure-export-to-data-lake"></a><a name="enableExportToDataLake"></a> Įgalinti ir konfigūruoti eksportavimą į duomenų apie duomenis

"Commerce analytics" (Preview) pasitiki eksportavimo į duomenis į duomenų portalą funkcija, kuri leidžia eksportuoti "Commerce HQ" duomenis į duomenų importavimo ir duomenų peržiūros funkciją. Prieš konfigūruojant "Commerce Analytics" (peržiūra), įgalinkite ir konfigūruokite "Export to Data Azure", atlikdami veiksmus, aprašytus dalyje Konfigūruoti [eksportavimą į "Azure Data](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) Azure".

Konfigūruodami eksportavimą į duomenų Apie duomenų išrašą, pasižymėti toliau nurodytą informaciją, nes ją reikės įvesti vėliau:

- <a name="keyVault"></a> Rakto saugyklos domeno vardų sistemos (DNS) pavadinimas ir slapti pavadinimai, kur saugote programos ID ir programos slaptažodį. Daugiau informacijos rasite įtraukti [paslapčių į rakto "Vault".](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets)
- <a name="storageAccount"></a> Duomenų serverio egzemplioriaus saugojimo sąskaitos pavadinimas. Daugiau informacijos ieškokite [savo abonemento duomenų saugojimo (Gen2) sąskaitos kūrimas](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription).

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a> Įgalinti ir konfigūruoti "Commerce Analytics" (peržiūra) priedą

Norėdami įdiegti "Commerce Analytics" (peržiūra) priedą LCS, turite būti LCS aplinkos administratorius, kad būtų galima naudoti aplinką.

Norėdami įdiegti ir konfigūruoti "Commerce Analytics" (peržiūra) priedą, atlikite šiuos veiksmus.

1. Prisiregistruokite [prie LCS](https://lcs.dynamics.com/) ir eikite į aplinką.
2. Aplinkos **puslapio** skirtuke **Aplinkos** papildiniai pasirinkite Diegti naują **priedą**.
3. Dialogo lange pasirinkite **"Commerce analytics"** (peržiūra).

    Jei **"Commerce Analytics"** (Peržiūra) nėra sąraše, įsitikinkite, kad esate prijungę prie "Insider" programos.

4. Nustatymo **priedo dialogo** lange įveskite šią informaciją.

    | Informacija | Šaltinis | Reikšmės pavyzdys |
    |---|---|---|
    | Azure AD Jūsų aplinkos nuomininko ID | Prisiregistruokite prie ["Azure"](https://portal.azure.com/) portalo ir atidarykite **Azure Active Directory** paslaugą. Tada **atidarykite** puslapį Ypatybės ir nukopijuokite reikšmę lauke **Katalogo** ID. | 72f988 pagal-0000-0000-00000-2d7cd011db47 |
    | Jūsų rakto saugyklos DNS pavadinimas | Įveskite [savo rakto saugyklos DNS](#keyVault) pavadinimą. Turite padaryti šios vertės pastabą ankstesniame skyriuje. | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Neslapti, kuriame yra prašymo ID | Įvesti [slaptą pavadinimą, kuriame saugomas programos](#keyVault) ID. Turite padaryti šios vertės pastabą ankstesniame skyriuje. | app-id |
    | Neslapti, kuriame yra prašymo slapyme | Įvesti [slaptą pavadinimą, kuriame saugomas programos](#keyVault) slapyme. Turite padaryti šios vertės pastabą ankstesniame skyriuje. | app-secret |

5. Priimkite pasiūlymo sąlygas pažymėdami žymės langelį ir pasirinkite **Diegti**.

    Sistema įdiegia ir sukonfigūruoja "Commerce Analytics" (peržiūra) aplinkos priedą. Šis procesas gali užtrukti keletą minučių. Kai jis baigtas, **"Commerce Analytics" (Peržiūra) turi būti įrašyta į aplinkos** **puslapį**, o būsena turi būti **Įdiegta**.

### <a name="generate-a-sas-token-for-your-storage-account"></a><a name="getSASToken"></a> Generuoti jūsų saugojimo sąskaitos SAS atpažinimo ženklą

SAS atpažinimo ženklas įgalina išorinius objektus pasiekti jūsų saugyklos sąskaitą ir turėti konkrečius teisių rinkinius, skirtas ribotam laikui. Azure Synapse naudos SAS atpažinimo ženklą, kad būtų galima pasiekti duomenų ats.

> [!NOTE]
> Dėl žinomo "Commerce analytics" (Peržiūra) apribojimo egzempliorius praras prieigą prie duomenų failo, kai Azure Synapse SAS atpažinimo ženklas baigs galioti. Todėl, kai generuojate SAS atpažinimo ženklą, turėtumėte nustatyti maksimalią galiojimo datą, kurią leidžia jūsų organizacijos saugos strategijos.

Norėdami generuoti SAS atpažinimo ženklą, atlikite šiuos veiksmus.

1. "Azure" portale eikite į [saugojimo sąskaitą,](#storageAccount) kurią sukūrėte konfigūruojant eksportavimą į duomenų "Azure".
2. Kairiajame lange po saugojimo sąskaita pasirinkite Bendrai naudojamos **prieigos** parašas.
3. **SAS pasirinkčių** puslapyje nustatykite šiuos laukus.

    | Laukas | Vertė |
    |---|---|
    | Leidžiamos paslaugos | Pasirinkite **BLOB**. |
    | Leidžiami išteklių tipai | Pasirinkite **aptarnavimas**, **konteineris** ir **objektas**. |
    | Leidžiamos teisės | Pasirinkite **Skaityti**, **Rašyti**, **Naikinti**, **·** **Sąrašas**, Įtraukti ir **Kurti**. |
    | BLOB versijos naujinimo teisės | Pasirinkite **Įgalina versijų** panaikinimą. |
    | Pradžios ir galiojimo data / laikas | Atitinkamai nustatykite SAS atpažinimo ženklo pradžios ir pabaigos datą bei laiką. |
    | Leidžiami IP adresai | Palikite šį lauką tuščią. |
    | Leidžiami protokolas | Pasirinkite **tik** HTTPS. |
    | Pageidaujama maršruto pakopa | Pasirinkti **pagrindinį (numatytąjį)**. |
    | Pasirašymo raktas | Atitinkamai **pasirinkite** **key1 arba** key2. |

4. Pasirinkite **Generuoti SAS ir jungimosi** eilutę.
5. Nukopijuokite **SAS atpažinimo ženklo lauko vertę ir įklijuokite į teksto** doroklį, pvz., Notepad.

### <a name="download-the-deployment-scripts-for-azure-synapse-views"></a><a name="downloadSynapseDeploymentScripts"></a> Atsisiųsti rodinių diegimo Azure Synapse scenarijus

Norėdami kurti ir publikuoti reikiamus rodinius Azure Synapse darbo srityje, turite paleisti scenarijų rinkinį. Norėdami atsisiųsti scenarijus, atlikite šiuos veiksmus.

1. GitHub, eikite į [microsoft/Dynamics365Commerce.Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugyklą (repo).
2. Atsisiųskite scenarijus į savo vietinį kompiuterį, atmesdami repo ar atsisiuntimą kaip pašto failą.

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a> Darbo srities diegimas ir Azure Synapse konfigūravimas

Norėdami įdiegti ir konfigūruoti darbo Azure Synapse sritį, atlikite šiuos veiksmus.

1. Įdiekite darbo Azure Synapse sritį savo "Azure" abonemente. Daugiau informacijos rasite [Quickstart: Synapse darbo srities](/azure/synapse-analytics/quickstart-create-workspace) kūrimas.
2. Notepad arba kitame teksto doroklyje iš vietinio kompiuterio aplanko, kurį įterpėte arba atsisiuntėte **Dynamics365Commerce.Solutions repo į ankstesnį skyrių, atidarykite SetupSynapse.sql scenarijaus** failą. Scenarijaus failas bus aplanke /Pipeline/CommerceAnalyticsSynapse/. Scenarijuje pakeiskite vietos rezervavimo ženklo tekstą vertėmis, kaip parodyta pateiktoje lentelėje.

    | Vietos rezervavimo ženklo tekstas | Atkuriamoji vertė |
    |---|---|
    | placeholder_storageaccount | Saugojimo sąskaitos, kurią [sukūrėte](#storageAccount) konfigūruojant Eksportuoti į duomenų importavimą į duomenų atminties programą, pavadinimas. |
    | <a name="phContainer"></a> placeholder_container | Saugojimo konteinerio, kuris buvo sukurtas jūsų duomenų "Jav" egzemplioriuje po to, kai sėkmingai įdiegėte eksportavimą į duomenų į duomenų LCS priedą, pavadinimas. Norėdami gauti konteinerio pavadinimą, turite naudoti saugojimo naršyklę "Azure" portale, norėdami naršyti jūsų saugyklos sąskaitą. |
    | placeholder_sastoken | Sugeneruotas [SAS](#getSASToken) atpažinimo ženklas. Įsitikinkite, kad pašalinti **klaustuką** (?) iš SAS atpažinimo ženklo vertės pradžios. |
    | <a name="phUserPwd"></a> placeholder_password | Jūsų pasirinktame slaptažodyje yra didelis slaptažodis. Pasižymėkite šį slaptažodį. Jis bus nustatytas kaip naujo **reportreadonlyuser abonemento,** kurį sukuria scenarijus, slaptažodis. **Neįveskite** **sqladminuser abonemento** slaptažodžio. |

3. Nukopijuokite atnaujintą scenarijaus failo turinį.
4. "Azure" portale eikite į naują darbo Azure Synapse sritį. Peržiūros **puslapyje** pasirinkite Atidaryti **"Synapse** Studio".
5. "Synapse Studio" pasirinkite Naujas SQL scenarijus ir į SQL scenarijaus rengyklę **\>** įklijuokite scenarijaus failo turinį.
6. Įsitikinkite, kad **laukas Naudoti duomenų bazę nustatytas kaip** **bendrasis**.
7. Pasirinkite **Vykdyti** ir palaukite, kol scenarijus bus baigtas vykdyti. Sėkmingai vykdant scenarijų bus sukurta "Commerce Analytics" duomenų bazė, kredencialai, skirti duomenims pasiekti ir tik skaitomas vartotojo abonementas, kuris bus naudojamas prisijungti Power BI prie Azure Synapse egzemplioriaus.
8. Vietiniame kompiuteryje atidarykite "Windows PowerShell" administratoriaus režimu ir eikite į aplanką /Pipeline/CommerceAnalyticsSynapse/, esantį aplanke, į kurį atsisiuntėte Dynamics365Commerce.Solutions repo.
9. Nustatykite "Windows PowerShell" vykdymo strategiją vykdydami šią komandą.

    ```powershell
    Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
    ```

10. Jei "SQL Server PowerShell" modulis dar neįdiegtas, įdiekite jį vykdydami šią komandą.

    ```powershell
    Install-Module sqlserver
    ```

    > [!NOTE]
    > Diegiant modulį, gali būti, kad jus paragins įdiegti NuGet teikėją. Šiuo atveju pasirinkite Y, norėdami **įdiegti** NuGet teikėją. Taip pat galite būti paraginti patvirtinti, kad iš naujo įdiegiate modulius iš nepatikimų saugyklų. Tokiu atveju pasirinkite **Y,** kad įdiegtumėte toliau. Galite pasirinktinai paleisti **Set-PSRepository cmdlet, norėdami** užtikrinti **PS Yra saugyklos** pasitikėjimą.

11. Publikuokite Azure Synapse rodinius vykdydami šią komandą.

    ```powershell
    .\PublishSynapseViews.ps1 -serverName SERVER_NAME -password PASSWORD -storageAccount STORAGE_ACCOUNT -containerName CONTAINER_NAME -datarootpath DATA_ROOT_PATH
    ```

    Vykdykite šią komandą, pakeiskite vietos rezervavimo ženklo vertes, kaip parodyta pateiktoje lentelėje.

    | Vietos rezervavimo ženklo reikšmė | Atkuriamoji vertė |
    |---|---|
    | SERVER_NAME | Serverio be serverio Azure Synapse SQL galinio punkto pavadinimas. Šią vertę galite gauti **iš** "Azure" portalo Azure Synapse darbo srities apžvalgos puslapio. |
    | SLAPTAŽODĮ | **sqladminuser abonemento** slaptažodis. |
    | STORAGE_ACCOUNT | Duomenų Vardo saugojimo sąskaitos pavadinimas. |
    | CONTAINER_NAME | Konteinerio, kurį sukūrė funkcija Eksportuoti į duomenų importavimą, pavadinimas. Šis konteineris yra tas pats konteineris, kurį [nurodėte placeholder_container](#phContainer) 2 veiksmo metu. |
    | DATA_ROOT_PATH | Aplanko pavadinimas konteineryje, kuriame yra visi duomenys. |

    > [!NOTE]
    > Naudodami "Azure" saugyklos naršyklę ir duomenų "Azure" portalo duomenų "Azure" saugyklos sąskaitą, galite rasti saugyklos sąskaitos pavadinimą, konteinerio pavadinimą ir duomenų šakninį kelią.

12. Palaukite, kol scenarijus bus paleistas. Sėkmingai vykdant scenarijų SQL rodiniai bus sukurti be serverio Azure Synapse duomenų SQL egzemplioriuje.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a> Šablono Power BI programos diegimas

Norėdami įdiegti Power BI "Commerce Analytics" šablono programą (peržiūra), atlikite šiuos veiksmus.

1. Prisiregistruokite [Power BI](https://powerbi.microsoft.com/) portale naudodami savo organizacijos ID.
2. Įdiekite "Commerce Analytics" (peržiūros) Power BI šablonų programą nueidami į [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Galite gauti įspėjimą, kuris reiškia, kad programos nėra sąraše AppSource. Pasirinkti **Diegti**.
3. Jei programą iš naujo įdiegiate pirmą kartą, praleiskite toliau 5 veiksmą. Jei šią programą įdiegėte anksčiau, rodomos šios programos atnaujinimo parinktys:

    - **Atnaujinkite darbo sritį ir programą – atnaujinkite esamą šablono programą ir perrašykite esamus programos parametrus, pvz., programos egzemplioriaus pavadinimą** ir teisių konfigūracijas.
    - **Atnaujinkite tik darbo srities turinį neatnaujinę programos** – atnaujinkite esamą šablono programą, bet išlaikykite esamus programos parametrus. *Ši pasirinktis yra rekomenduojama programos naujinimų parinktis.*
    - **Įdiekite kitą programos kopiją į naują darbo sritį – sukurkite naują darbo sritį, tada sukurkite joje** esančios šablono programos kopiją. Esama darbo sritis bus atgaktyva.

4. Pasirinkite vieną iš atnaujinimo pasirinkčių, tada pasirinkite **Diegti**.
5. Atidarykite įdiegtą programą **kairiajame** lange pasirinkdami Programėlės ir ją pasirinkdami.
6. Prijunkite programą prie duomenų šaltinio pasirinkdami **Prisijungti**. Jei programą įdiegėte prieš tai, geltoname pranešimų **juostoje** pasirinkite duomenų saito jungtį Prijungti.
7. Užpildykite toliau nurodytus laukus.

    | Laukas | Vertė |
    |---|---|
    | Serveris | Įveskite serverio be serverio Azure Synapse SQL galinio punkto, kurį sukūrėte ankstesniame skyriuje, pavadinimą. Šią vertę galite gauti **iš** "Azure" portalo Azure Synapse darbo srities apžvalgos puslapio. |
    | Duomenų bazė | Įveskite **CommerceAnalytics.** |
    | Kalba | Pasirinkti vertę iš sąrašo. Šis laukas naudojamas lokalizuoties produktų ir kategorijų pavadinimams. Ši vertė abc nuo abc. |
    | Datų diapazonas | Pasirinkti vertę iš sąrašo. Pasirinkto mėnesių skaičiaus duomenys bus importuoti į duomenų Power BI rinkinį. Jūsų parenkama reikšmė turi įtakos duomenų rinkinio dydžiui ir sinchronizavimui reikalingas laikas. |

8. Pasirinkite **Toliau**. Jus paragins įvesti kredencialus, kad būtų galima prisijungti prie Azure Synapse SQL duomenų bazės. Nustatyti laukus, kaip parodyta šioje lentelėje.

    | Laukas | Vertė |
    |---|---|
    | Autentifikavimo metodas | Pasirinkite **pagrindinį**. |
    | Vartotojo vardas | Įveskite **reportreadonlyuser.** |
    | Slaptažodis | Įveskite reikšmę, kurią [pakeitėte placeholder_password](#phUserPwd) vietos rezervavimo ženklus SetupSynapse.sql scenarijuje. Šis slaptažodis yra abonemento **reportreadonlyuser** slaptažodis. |

9. Pasirinkite **prisijungimą ir** prisijunkite.
10. Palaukite, kol duomenų rinkinys bus sėkmingai atnaujintas. Tada pasirinkite **mygtuką Redaguoti** programą, norėdami atidaryti programos darbo sritį, kurioje galite peržiūrėti duomenų rinkinio atnaujinimo būseną. Programos darbo srityje taip pat galite pasirinktinai nustatyti automatinio duomenų rinkinio naujinimo grafikus, valdyti teises ir pervardyti programos egzempliorių.

### <a name="privacy"></a><a name="privacy"></a>Privatumas

Mes rūpinamės jūsų privatumu. Norėdami sužinoti daugiau, perskaitykite mūsų [Pareiškimą dėl privatumo](https://go.microsoft.com/fwlink/?LinkId=521839).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
