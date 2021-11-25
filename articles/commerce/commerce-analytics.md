---
title: Komercijos analizė (peržiūra)
description: Šioje temoje išsamiai aprašomas analizės galimybių diegimas ir naudojimas programoje Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 11/15/2021
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 7f3e51cc3f7314bd33bca9e598bd0b1c9118caef
ms.sourcegitcommit: 9f8da0ae3dcf3861e8ece2c2df4f693490563d5e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2021
ms.locfileid: "7817458"
---
# <a name="commerce-analytics-preview"></a>Komercijos analizė (peržiūra)

[!include [banner](includes/banner.md)]

Komercijos analizė yra funkcinės analizės galimybė, įtraukta į Dynamics 365 Commerce. Šioje temoje išsamiai aprašoma "Commerce Analytics" ir paaiškinama, kaip ją įdiegti. 

## <a name="system-architecture"></a>Sistemos architektūra
### <a name="key-components"></a>Pagrindiniai komponentai
"Commerce Analytics" sudaro šie pagrindiniai komponentai:
- Parengta naudoti interaktyvias Power BI ataskaitas
- SQL rodiniai Azure Synapse programoje "Analytics"
- Objekto ir ontologijos duomenys "Azure Data Lake"
- Neapdoroti duomenys "Azure" duomenų ežere

!["Commerce Analytics" sistemos architektūra](media/CommerceAnalytics.png)

### <a name="data-flow"></a>Duomenų srautas
#### <a name="step-1-data-generation"></a>1 veiksmas: duomenų generavimas
Duomenys gaunami kaip operacijų duomenys arba elgsenos duomenys iš vieno iš šių šaltinių:
- Skambučių centro partneris naudojant "Commerce HQ" klientą pardavimo užsakymams apdoroti
- Kasininkas pardavimo vietoje (EKA), apdorojanti pardavimo operacijas
- Pardavimai, sukurti naudojant pasirinktines programas naudojant "Headless Commerce" ("Commerce Scale Unit")
- Elektroninės komercijos pirkėjas naršo jūsų elektroninės komercijos svetainėje 
- Elektroninės komercijos pirkėjas, pateikiantis užsakymą jūsų elektroninės komercijos svetainėje
- Duomenys, kuriuos teikia kitos sistemos, pvz., Dynamics 365 Connected Spaces

#### <a name="step-2-ingestion-and-pre-processing"></a>2 veiksmas: nurijimas ir išankstinis apdorojimas
Operacijų duomenys patenka į "Commerce" būstinę tiesiogiai (užsakymai, užfiksuoti tiesiogiai "Commerce HQ" kliente) arba iš "Commerce Scale Unit" (užsakymai, užfiksuoti EKA, el. prekyboje arba pasirinktiniuose klientuose naudojant "Headless Commerce"). 

Tada operacijų duomenys nukopijuojami į "Azure" duomenų ežerą kaip neapdoroti duomenys naudojant **funkciją Eksportuoti į duomenų** ežerą, o duomenys saugomi aplanke "Lentelės". Elektroninės komercijos interneto veiklos duomenys siunčiami tiesiai į duomenų ežerą.

Kitų sistemų, pvz.,, pateikti duomenys Dynamics 365 Connected Spaces taip pat siunčiami tiesiai į duomenų ežerą.

#### <a name="step-3-transformation-and-aggregation"></a>3 veiksmas: transformacija ir agregavimas
Kai neapdoroti duomenys yra duomenų ežere, "Commerce Analytics" tarnyba nuskaito duomenis, transformuoja, agreguoja ir įrašo juos atgal į duomenų ežerą loginių objektų pavidalu aplanke "Objektai" ir susumuoja metriką aplanke "Ontologies". 

#### <a name="step-4-querying"></a>4 veiksmas: užklausimas
Duomenys ežere yra užklausiama per T-SQL sąsaja naudojant Azure Synapse Analytics. Sąsaja apima SQL rodinius, kurie leidžia išorinių užklausų duomenų ežere, tiesiogiai naudojant T-SQL kliento ad hoc analizė, arba per vizualizacijos įrankis, pvz., Power BI.

#### <a name="step-5-modeling-and-serving"></a>5 žingsnis: Modeliavimas ir aptarnavimas
Tada "Analytics" užklausti duomenys Azure Synapse patenka į Power BI semantinį modelį. Atsižvelgiant į duomenų tipą, jie periodiškai importuojami į atmintį Power BI arba tiesiogiai užklausiama vykdymo metu. 

Paskutinis etapas yra skirtas duomenims, kurie turi būti generuojami Power BI vaizduose, kad vartotojai galėtų peržiūrėti ir sąveikauti. 

## <a name="commerce-analytics-functional-overview"></a>Komercijos analizės funkcinė apžvalga
### <a name="1-summary"></a>1. Santrauka
#### <a name="top-level-filters"></a>Aukščiausio lygio filtrai
1.  Datos parametrai
    1. Metai
    2. Ketvirtis    
    3. Mėnuo    
    4. Savaitė    
    5. Diena
2. Kanalo parametrai
    1. Juridinis subjektas    
    2. Kanalo tipas    
    3. Kliento tipas    
    4. Pardavimo tipas    
    5. Kanalas    
    6. Organizacijos hierarchijos
3. Produkto parametrai
    1. Kategorijų hierarchija    
    2. Kategorija

#### <a name="a-product"></a>a. Produktas
1. Pardavimas
2. Paraštės
3. Grąžinimas

#### <a name="b-customer"></a>b. Klientas
1. Pardavimas
2. Paraštės
3. Grąžinimas

#### <a name="c-channel"></a>c. Kanalas
1. Pardavimas
2. Paraštės
3. Grąžinimas

### <a name="2-sales"></a>2. Pardavimai
1. Pagal pristatymo vietą
2. Pagal kanalą / parduotuvę / terminalą
3. Pagal darbuotoją
4. Pagal datą
5. Pagal valandą
6. Pagal produkto kategoriją

### <a name="3-margin"></a>3. Marža
1. Pagal pristatymo vietą
2. Šalutinis produktas
3. Pagal datą

### <a name="4-return"></a>4. Grąžinimas
1. Grąžinimas pagal sumą
    1. Pagal parduotuvę    
    2. Šalutinis produktas    
    3. Pagal datą
2. Grąžinimas pagal operaciją
    1. Pagal parduotuvę    
    2. Šalutinis produktas    
    3. Pagal datą

### <a name="5-discount"></a>5. Nuolaida
1. Pagal parduotuvę
2. Šalutinis produktas
3. Pagal datą
4. Paskirstymas
    1. Juridinis subjektas    
    2. Parduotuvė    
    3. Nuolaidos tipas    
    4. Nuolaidos pavadinimas    
    5. Produktas

### <a name="6-payment"></a>6. Mokėjimas
1. Pagal kanalą / terminalą
2. Pagal mokėjimo būdą / tipą
3. Pagal datą
4. Paskirstymas
    1. Juridinis subjektas    
    2. Kanalo tipas    
    3. Parduotuvė    
    4. Mokėjimo terminalas    
    5. Mokėjimo būdas

### <a name="7-customer"></a>7. Klientas
1. Gyvenimo laiko vertė (LTV): gyvavimo laiko vertė apskaičiuojama pagal bendrą sumą, kurią klientas išleidžia visuose "Commerce" pardavimo kanaluose (EKA, el. prekyboje ir skambučių centre).
2. Recency: Recency skaičiuojamas pagal dienų skaičių nuo paskutinio kliento operacijų įtraukimo į organizaciją. Recency neatsižvelgia į ne sandorio įtraukimo signalus, pvz., el. prekybos naršymo veiklą.
3. Dažnumas: dažnis apskaičiuojamas pagal kliento operacijų bendradarbiavimą su organizacija. Dažnumas neatsižvelgia į ne sandorio įtraukimo signalus, pvz., elektroninės komercijos naršymo veiklą.
4. Ryšio ilgis: ryšio ilgis apskaičiuojamas pagal dienų skaičių nuo kliento įrašo sukūrimo sistemoje. 
5. Operacijų skaičius

### <a name="8-comparison"></a>8. Palyginimas
1. Produktų palyginimas pagal laikotarpį
    1. Pardavimo ir pardavimo skirtumas
    2. Maržos ir maržos skirtumas
2. Klientas pagal laikotarpį
    1. Pardavimo ir pardavimo skirtumas
    2. Maržos ir maržos skirtumas

### <a name="9-web-activity"></a>9. Veikla žiniatinklyje

#### <a name="top-level-filters"></a>Aukščiausio lygio filtrai
1. Datų diapazonas
2. Kanalo tipas
3. Kanalas
4. Kategorijų hierarchija

#### <a name="a-acquisition"></a>a. Įsigijimas
1. Puslapių rodiniai
    1. Pagal šalį / regioną    
    2. Šalutinis produktas    
    3. Pagal vartotojo prisijungus būseną    
    4. Pagal datą
2. Elektroninės komercijos užsakymai
3. Konvertavimo kursas
    1. Pagal datą
4. Konvertavimo piltuvas
    1. Puslapio rodinys pagal puslapio tipą (pagrindinis puslapis, kategorijos puslapis, išsamios produkto informacijos puslapis)  
    2. Dėti į krepšelį    
    3. Pirkimo užbaigimas   
    4. Pirkimas

#### <a name="b-session"></a>b. Seansas
Seansas apibrėžiamas kaip vartotojo apsilankymo jūsų elektroninės komercijos svetainėje epizodas. Seansas laikomas baigtu po 30 minučių neveiklumo arba po 24 valandų aktyvaus naudojimo.
1. Pagal šalį / regioną
2. Pagal kilmę (išorinis persiuntėjas)
3. Pagal vartotojo prisijungus būseną
4. Seansų skaičius
    1. Pagal datą    
    2. Pagal įrašo puslapį
5. Užsakymas per seansą
    1. Pagal datą
6. Seanso atmetimo rodiklis: seanso atmetimas apibrėžiamas kaip seansas, kai vartotojas iš karto išeina apsilankęs jūsų elektroninės komercijos svetainėje. 
7. Paspaudimai per seansą

#### <a name="c-visitor"></a>c. Lankytojas
Anoniminis lankytojas jūsų elektroninės komercijos svetainėje nustatomas pagal unikalų identifikatorių toje konkrečioje naršyklėje tame konkrečiame įrenginyje. "Commerce Analytics" neseka anoniminių naudotojų skirtingose naršyklėse ar įrenginiuose. Anoniminis vartotojas, naudojantis tą pačią naršyklę tame pačiame kompiuteryje, yra unikaliai identifikuojamas keliuose vartotojo seansuose, kol naršyklės talpyklos duomenys išvalomi arba paprastai iki 12 mėnesių laikotarpio, atsižvelgiant į tai, kas įvyks anksčiau.

"Commerce Analytics" gali suteikti daugiau informacijos apie lankytojus, kurie naršo jūsų el. prekybos svetainėje prisijungdami. Informacija pagrįsta jūsų esamais santykiais su šiais vartotojais, įskaitant pirkimus, kuriuos vartotojai įsigijo iš jūsų organizacijos visuose "Commerce" pardavimo kanaluose (EKA, skambučių centre ir el. prekyboje), ir apima atsitraukimą, ryšio trukmę, viso gyvenimo vertę ir dažnumą.

1. Lankytojų marža
2. Lankytojų vidutiniai užsakymai
3. Lankytojų vidutinis pardavimas
4. Elektroninės komercijos lankytojų skaičius
    1. Pagal datą
    2. Pagal vietovę: "Commerce Analytics" gali pateikti tik vietos nustatymo įžvalgų, skirtų elektroninės komercijos lankytojams, detalumą šalies / regiono lygiu.     
    3. Pagal atsitraukimą: recency skaičiuojamas pagal dienų skaičių nuo paskutinio kliento operacijų įtraukimo į organizaciją. Recency neatsižvelgia į ne sandorio įtraukimo signalus, pvz., el. prekybos naršymo veiklą.    
    4. Pagal ryšio trukmę: ryšio ilgis apskaičiuojamas pagal dienų skaičių nuo kliento įrašo sukūrimo sistemoje.     
    5. Pagal viso gyvenimo vertę (LTV): gyvenimo laiko vertė apskaičiuojama pagal bendrą sumą, kurią klientas išleidžia visuose "Commerce" pardavimo kanaluose (EKA, el. prekyboje ir skambučių centre).
    6. Pagal dažnumą: dažnumas apskaičiuojamas pagal kliento operacijų bendradarbiavimą su organizacija. Dažnumas neatsižvelgia į ne sandorio įtraukimo signalus, pvz., elektroninės komercijos naršymo veiklą.

#### <a name="d-impression"></a>d. Įspūdį
Parodymas apibrėžiamas kaip kiekvienas elektroninės komercijos lankytojo produkto vaizdo peržiūra. Pavyzdžiui, jei elektroninės komercijos lankytojas pereina į pagrindinį jūsų svetainės puslapį ir peržiūri jogos kilimėlio produktą populiariausio sąrašo modulyje, taip pat peržiūri tą patį jogos kilimėlio produktą iš sąrašo modulio, šios sąveikos laikomos dviem produkto parodymais. Parodymai seka produkto vaizdus šiuose paviršiuose:
1. Sąrašai (pvz., rekomenduojama, populiariausias pardavimas, pasirinkimai jums, tendencijos)
2. Krepšelio modulis
3. Ieškos rezultatų konteineris
4. Kategorijos ieškos rezultatų konteineris
    
Produktai, pagaminti karuselės modulyje arba pagal pasirinktinę vaizdinę medžiagą, į parodymų metriką neįskaičiuojami.

**Parodymų ataskaitos** puslapyje pateikiama ši metrika:
1. Parodymų skaičius
    1. Pagal puslapio tipą ir modulį: puslapio tipas yra bendrasis puslapio tipas, apibrėžtas kiekvienam jūsų elektroninės komercijos svetainės puslapiui. Modulio tipas apibrėžia elektroninės komercijos vaizdinio modulio tipą, kuriame rodomas produktas. Jums gali tekti detalizuoti puslapio ir modulio vaizdinę medžiagą, kad galėtumėte peržiūrėti parodymus pagal modulį.    
    2. Šalutinis produktas    
    3. Pagal vartotojo prisijungus būseną    
    4. Pagal datą
2. Parodymų paspaudimų skaičius: parodymų paspaudimas apibrėžiamas kaip elektroninės komercijos lankytojas, spustelėjęs produkto vaizdinį vaizdą, kuris paprastai pereis vartotojus į to produkto išsamios informacijos puslapį.     
3. Parodymų paspaudimų rodiklis (PR): paspaudimų rodiklis apibrėžiamas kaip bendras parodymų paspaudimų skaičius, padalytas iš bendro parodymų skaičiaus.

## <a name="install-commerce-analytics"></a>"Commerce Analytics" diegimas

> [!NOTE]
> Komercijos analizė yra peržiūros etape JAV, Kanadoje, Jungtinėje Karalystėje, Europoje, Pietryčių Azijoje, Rytų Azijoje, Australijoje ir Japonijos regionuose. Jei jūsų aplinka yra bet kuriame iš šių regionų, galite įgalinti "Commerce analytics" jūsų aplinkoje naudodami ciklo Microsoft Dynamics tarnybas (LCS). Prieš naudodami "Commerce Analytics", žr. [Konfigūruoti eksportavimą į "Azure Data Azure"](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics"></a>Įgalinti ir konfigūruoti "Commerce Analytics"
Norint įdiegti "Commerce Analytics", reikia turėti teises kurti išteklius "Azure" abonemente ir teises diegti papildinį "LCS". Atlikite toliau aprašytus veiksmus, kad įgalintumėte ir konfigūruokite "Commerce Analytics".
1. [Pateikti "Commerce Analytics" peržiūros formą (peržiūra)](#submit-the-preview-intake-form-for-commerce-analytics).
2. [Įgalinti ir konfigūruoti eksportavimą į duomenų Apie](#enable-and-configure-export-to-data-lake).
3. [Įgalinkite ir konfigūruokite "Commerce Analytics" (peržiūra) priedą](#enable-and-configure-commerce-analytics-add-in).
4. [Generuoti saugojimo sąskaitos SAS atpažinimo](#generate-storage-account-sas-token) ženklą.
5. [Atsisiųskite peržiūros diegimo Azure Synapse](#download-deployment-scripts-for-azure-synapse-views) scenarijus.
6. [Įdiekite ir konfigūruokite Azure Synapse darbo](#install-and-configure-azure-synapse-workspace) sritį.
7. [Įdiekite Power BI šablono](#install-power-bi-template-app) programą. 

### <a name="submit-the-preview-intake-form-for-commerce-analytics"></a>Pateikti "Commerce Analytics" peržiūros formos formą
Užpildykite ir pateikite ["Commerce analytics" (peržiūra)](https://forms.office.com/r/vW5VLJGXZ2) formą. Kad užklausa būtų apdorota, leiskite apdoroti iki trijų darbo dienų. Apdorous formą, patvirtinimo el. laiškas bus išsiųstas el. pašto adresu, kuris yra pateiktas formoje.

### <a name="enable-and-configure-export-to-data-lake"></a>Įgalinti ir konfigūruoti eksportavimą į duomenų apie duomenis
"Commerce analytics" pasitiki eksportavimo į duomenis į duomenų į nuosumą funkcija, kad "Commerce HQ" duomenys būtų eksportuojami į **·** "Azure Data Azure" ir toliau šie duomenys būtų nuolat eksportuojami į "Azure Data Azure". Prieš konfigūruokite "Commerce Analytics", įgalinkite ir konfigūruokite "Export to Data Į Data Į" parametrus, atlikdami veiksmus, nurodytus skyriuje Eksportavimo į **·**["Azure Data Azure" paslaugų](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) konfigūravimas. Konfigūruojant **funkciją Eksportuoti į duomenų iš** duomenų, atkreipkite dėmesį į šią informaciją. Šią informaciją turėsite įvesti atlikite toliau.
1. Raktas rodo saugyklos DNS pavadinimą ir slaptus pavadinimus, kur saugote programos ID ir programos slaptažodį. Daugiau informacijos rasite įtraukti [paslapčių į rakto "Vault".](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets)
2. "Azure" duomenų į įrenginį egzemplioriaus saugojimo sąskaitos pavadinimas. Daugiau informacijos ieškokite [abonemento duomenų saugojimo (Gen2) sąskaitos](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription) kūrimas.

### <a name="enable-and-configure-commerce-analytics-add-in"></a>Įjungti ir konfigūruoti "Commerce Analytics" papildą
Norėdami įdiegti "Commerce Analytics" papildinę LCS, turite būti LCS aplinkos administratorius, kad būtų galima naudoti aplinką.

Norint konfigūruoti "Commerce Analytics" papildinį, reikės šios informacijos. 

|Laukas | Informacijos šaltinis| Pavyzdys|
|----|----|----|
|Azure AD Jūsų aplinkos nuomininko ID| Jūsų Azure AD nuomininko ID "Azure" portale. Prisiregistruokite prie **"Azure"** portalo ir atidarykite **Azure Active Directory** paslaugą. Atidarykite **·** ypatybes ir nukopijuokite reikšmę lauke **Katalogo** ID.| 72f988freo-0000-0000-00000-2d7cd011db47|
|Jūsų rakto saugyklos DNS pavadinimas|Įveskite [savo rakto saugyklos DNS](#enable-and-configure-export-to-data-lake) pavadinimą.| `https://contosod365datafeedpoc.vault.azure.net/`|
|Neslapti, kuriame yra prašymo ID| Įvesti [slaptą](#enable-and-configure-export-to-data-lake) pavadinimą, kuriame saugomas programos ID. Tai ta pati vertė, kurią naudojote diegdami **add-in Eksportavimą į duomenų** importavimą.|app-id|
|Neslapti, kuriame yra prašymo slapyme| Įvesti [slaptą](#enable-and-configure-export-to-data-lake) pavadinimą, kuriame saugomas programos slapyme. Tai ta pati vertė, kurią naudojote diegdami **add-in Eksportavimą į duomenų** importavimą.| app-secret|

1. Prisiregistruokite [prie ciklo tarnybų ir pereikite prie](https://lcs.dynamics.com/) aplinkos.
2. Aplinkos **·** puslapyje pasirinkite skirtuką Aplinkos **·** priedai.
3. Pasirinkite **Diegti naują priedą ir dialogo lange pasirinkite** **"Commerce analytics" (peržiūra).** Jei **"Commerce Analytics"** (Peržiūra) nėra sąraše, įsitikinkite, kad esate prijungę prie "Insider" programos.
4. Nustatymo **priedo dialogo lange** įveskite reikiamą informaciją, kaip apibūdinta pirmiau pateiktoje lentelėje.
5. Priimkite pasiūlymo sąlygas pažymėdami žymės langelį ir pasirinkite **·** Diegti.

Sistema įdiegia ir sukonfigūruoja aplinkos "Commerce Analytics" (Peržiūra). Operacija gali užtrukti keletą minučių. Baigus diegti ir konfigūruoti, **"Commerce Analytics" (Peržiūra)** pateikiama aplinkos puslapyje ir būsena yra **·** **Įdiegta**.

### <a name="generate-storage-account-sas-token"></a>Generuoti saugojimo sąskaitos SAS atpažinimo ženklą
> [!NOTE]
> Žinomas "Commerce Analytics" (Peržiūra) apribojimas yra tai, kad egzempliorius praras prieigą prie duomenų failo, kai Azure Synapse SAS atpažinimo ženklas baigs galioti. Turėtumėte nustatyti didžiausią galiojimo datą, kurią leidžia jūsų organizacijos saugos strategijos, kai generuojate bendrai naudojamos prieigos parašo (SAS) atpažinimo ženklą.

SAS atpažinimo ženklas įgalina išorinius objektus pasiekti jūsų saugyklos abonementą su konkrečiais teisių rinkinys, skirtas ribotam laikui. Azure Synapse naudojant SAS atpažinimo ženklą bus galima pasiekti duomenis, esančių "Azure Data Azure Azure". Norėdami sugeneruoti SAS atpažinimo ženklą, atlikite toliau nurodytus veiksmus.
1. Eikite į "Azure" portalo saugojimo sąskaitą, kurią sukūrėte konfigūruodami eksportavimą į duomenų "Azure", kaip aprašyta savo abonemento **·**["Create data Azure" (Gen2)](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription) sąskaitoje.
2. Kairėje **pusėje** esančioje Pasirinkčių srityje po saugojimo sąskaita pasirinkite Bendrai **naudojamos prieigos** parašas.
3. SAS pasirinkčių puslapyje pasirinkite šias pasirinktis:

    | Parinkties pavadinimas | Parinkties vertė |
    |-------------|--------------|
    | Leidžiamos paslaugos | Pasirinkite **·** BLOB. |
    | Leidžiami išteklių tipai | Pasirinkite **·** Paslauga, **Konteineris** ir **·** Objektas.|
    | Leidžiamos teisės | Pasirinkite **·** Skaityti, **·** Rašyti, **·** Naikinti, **·** **·** Sąrašas, Įtraukti ir **·** Kurti. |
    | BLOB versijos naujinimo teisės | Pasirinkite **Įgalina versijų** panaikinimą. |
    | Pradžios ir galiojimo data / laikas | Tinkamai nustatykite SAS atpažinimo ženklo pabaigos datą ir laiką. |
    | Leidžiami IP adresai | Palikite tuščią. |
    | Leidžiami protokolas | Pasirinkite **tik** HTTPS. |
    | Pageidaujama maršruto pakopa | Pasirinkti **pagrindinį (numatytąjį)**. |
    | Pasirašymo raktas | Atitinkamai **pasirinkite 1** arba **·** 2 klavišą. |

4. Pasirinkite **Generuoti SAS ir jungimosi** eilutę.
5. Kopijuoti reikšmę iš **SAS atpažinimo ženklo** teksto lauko į teksto rengyklę, pvz., Notepad.

### <a name="download-deployment-scripts-for-azure-synapse-views"></a>Atsisiųsti rodinių diegimo Azure Synapse scenarijus
Norėdami sukurti ir paskelbti reikiamus rodinius Azure Synapse darbo srityje, turite atsisiųsti ir vykdyti scenarijų rinkinį. Norėdami atsisiųsti scenarijus atlikite toliau nurodytus veiksmus.
1. Eikite į ["microsoft/Dynamics365Commerce.Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) GitHub repo". Scenarijus galimas atask.
2. Norėdami atsisiųsti scenarijus į savo vietinį įrenginį, galite arba atsekite ats. arba atsisiųsti repo kaip pašto failą.

### <a name="install-and-configure-azure-synapse-workspace"></a>Darbo srities įdiegimas ir Azure Synapse konfigūravimas
Norėdami įdiegti ir konfigūruoti darbo Azure Synapse sritį, atlikite toliau nurodytus veiksmus.
1. Įdiekite Azure Synapse darbo sritį savo "Azure" abonemente pagal veiksmus, aprašytus ["Quickstart": sukurkite sinapsės darbo](/azure/synapse-analytics/quickstart-create-workspace) sritį.
2. Atidarykite SetupSynapse.sql scenarijaus failą Notepad iš vietinio kompiuterio aplanko, kuriame įkėlėte arba atsisiuntėte Dynamics365Commerce.Solutions repo. Norėdami gauti daugiau informacijos, [žr. "Atsisiųsti diegimo scenarijus" Azure Synapse](#download-deployment-scripts-for-azure-synapse-views) rodiniuose. Scenarijaus failas bus aplanke "/Pipeline/CommerceAnalyticsSynapse/". Redaguokite scenarijų, norėdami pakeisti vietos rezervavimo ženklo tekstą toliau reikšmėmis.

   | Vietos rezervavimo ženklo tekstas | Atkuriamoji vertė |
   |------------------|-------------------|
   | placeholder_storageaccount | Pakeiskite saugojimo sąskaitos, kurią sukūrėte konfigūruodami eksportavimą į duomenų vedlį, pavadinimą, kaip nurodyta abonemento sąskaitoje Kurti duomenų **·**[saugyklas (Gen2).](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription) |
   | <a name="phContainer"></a> placeholder_container | Pakeiskite saugojimo konteinerio, sukurto "Azure Data Azure Data Azure" egzemplioriuje, pavadinimą po to, kai įdiegite "Export **to Data Azure"** papildinę į LCS. Norėdami gauti konteinerio pavadinimą, norėdami naršyti saugyklos abonementą turite naudoti "Storage Explorer" "Azure" portale. |
   | placeholder_sastoken | Pakeiskite SAS atpažinimo ženklu, kurį nukopijuoote atpažinimo ženklu [Gauti saugojimo sąskaitos SAS.](#generate-storage-account-sas-token) Įsitikinkite, kad **·** SAS atpažinimo ženklo reikšmės pradžioje reikia pašalinti ?. |
   | <a name="phUserPwd"></a> placeholder_password | Pakeiskite savo pasirinktame slaptažodyje. Pasižymėkite slaptažodį. Slaptažodis bus nustatytas kaip naujo "reportreadonlyuser" abonemento, kurį kurs scenarijus, slaptažodis. **Čia** neįveskite abonemento sqladminuser slaptažodžio.  |

3. Eikite į naują darbo Azure Synapse sritį "Azure" portale. Pasirinkite parinktį **Atidaryti "Synapse** Studio" peržiūros **·** puslapyje.
4. Nukopijuokite turinį, `SetupSynapse.sql` kurį atnaujinote anksčiau 2 veiksme. "Synapse Studio" "Azure" portale pasirinkite **> SQL** scenarijų. Įklijuokite turinį į SQL scenarijaus rengyklę, esačių studijoje "Synapse Studio".
5. Patikrinkite, **ar Naudojimo duomenų bazė nustatyta kaip** **·** Pagrindinė. Pasirinkite **·** Vykdyti, kad būtų vykdomas scenarijus.
6. Palaukite, kol bus užbaigtas scenarijus. Scenarijus sukurs "Commerce Analytics" duomenų bazę, kredencialus, siekiant pasiekti "Azure Data Azure" ir tik skaitomą vartotojo abonementą, kurį naudoja jungiasi prie Power BI Azure Synapse egzemplioriaus.
7. Vietiniame kompiuteryje atidarykite "PowerShell" administratoriaus režimu. Eikite į aplanką "/Pipeline/CommerceAnalyticsSynapse/", esantį aplanke, kuriame įkėlėte ar atsisiuntėte Dynamics365Commerce.Solutions repo, kaip apibrėžta rodinių atsisiuntimo diegimo [Azure Synapse](#download-deployment-scripts-for-azure-synapse-views) scenarijuose.
8. "PowerShell" vykdymo strategiją nustatykite naudodami šią komandą "PowerShell" lange:

   ```powershell
   Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
   ```
   
9. Įdiekite SQL serverio "PowerShell" modulį paleisdami šią komandą "PowerShell" lange:

   ```powershell
   Install-Module sqlserver
   ```
   
   > [!NOTE]
   > Jei jau įdiegėte SQL serverio modulį, galite praleisti šį veiksmą. Diegiant šį modulį, gali būti, kad jus paragins įdiegti NuGet teikėją. Jei **norite toliau diegti** tiekėją, paspauskite NuGet Y. Taip pat galite gauti pranešimą, kurį diegiate modulius iš nepatikimų saugyklų. Jei **norite** tęsti diegimą, paspauskite Y. Jei norite, galite paleisti `Set-PSRepository` cmdlet, kad būtų pasitikite `PSGallery` saugykla.
   
10. Publikuokite Azure Synapse rodinius vykdydami šią komandą "PowerShell" lange:

    ```powershell
    .\PublishSynapseViews.ps1 -serverName SERVER_NAME -password PASSWORD -storageAccount STORAGE_ACCOUNT -containerName CONTAINER_NAME -datarootpath DATA_ROOT_PATH
    ```
    
    Pakeiskite komandos vietos rezervavimo ženklo vertes taip:
    
    | Vietos rezervavimo ženklo reikšmė | Atkuriamoji vertė |
    |-------------------|-------------------|
    | SERVER_NAME | Pakeisti serverio be serverio Azure Synapse SQL galinio punkto pavadinimu. Šią vertę galite gauti iš Azure Synapse **"Azure" portalo** darbo srities apžvalgos puslapio. |
    | SLAPTAŽODĮ | Pakeiskite sqladminuser slaptažodį. |
    | STORAGE_ACCOUNT | Pakeiskite "Azure Data Azure Azure" saugyklos sąskaitos pavadinimą. |
    | CONTAINER_NAME | Pakeiskite konteinerio, kurį sukūrė Eksportavimas į **duomenų importavimą,** pavadinimu. Pavadinimas yra skirtas tam pačiam konteineriui, kurį nurodėte [placeholder_container](#install-and-configure-azure-synapse-workspace) vertės viršuje. |
    | DATA_ROOT_PATH | Pakeisti aplanko pavadinimą po konteineriu, kuriame yra visi duomenys. |

    > [!NOTE]
    > Naudodami "Azure" saugyklos naršyklę ir "Azure" duomenų "Azure" duomenų saugyklas, galite rasti saugyklos sąskaitos pavadinimą, konteinerio pavadinimą ir duomenų šakninį kelią.

11. Palaukite, kol bus užbaigtas scenarijus. Scenarijus sukurs SQL rodinius be serverio Azure Synapse duomenų SQL egzemplioriuje.

### <a name="install-power-bi-template-app"></a>Šablono Power BI programos diegimas
Norėdami įdiegti Power BI "Commerce Analytics" šablono programą, atlikite toliau nurodytus veiksmus.
1. Prisiregistruokite [Power BI prie](https://powerbi.microsoft.com/) portalo naudodami savo organizacijos ID.
2. Įdiekite "Commerce Power BI Analytics" šablono programą nueidami [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp) į. Galite gauti įspėjimą apie programos sąrašą, kuris nėra AppSource išvardytas. Pasirinkti **Diegti**.
3. Jei tai pirmas kartas, kai diegiate programą, pereikite prie 5 veiksmo. Jei jau įdiegėte šią programą, bus pateiktos šios parinktys, norint atnaujinti programą.
   1. Atnaujinkite darbo sritį ir programą: ši parinktis atnaujina esamą šablono programą ir perrašo programos parametrus, pvz., programos egzemplioriaus pavadinimą ir teisių konfigūracijas.
   2. Atnaujinkite darbo srities turinį neatnaujinę programos: ši parinktis atnaujina esamą šablono programą ir išlaiko jūsų programos parametrus. Tai yra **rekomenduojama programos naujinimo** pasirinktis.
   3. Įdiekite kitą programos kopiją į naują darbo sritį: šia pasirinktimi sukuriama nauja programos kopija naujoje darbo srityje, kuri bus sukurta jums. Esama darbo sritis liekacto.      
4. Pasirinkite vieną iš anksčiau nurodytų pasirinkčių ir pasirinkite **·** Diegti.
5. Atidarykite įdiegtą programą, **·** kairėje srityje pasirinkdami programėlių meniu elementą ir pasirinkdami programėlę.
6. Prijunkite programą prie duomenų šaltinio pasirinkdami **·** Prisijungti. Jei tai ne pirmas kartas, kai diegiate programą, **geltonai informacijos** juostoje pasirinkite Prijungti savo duomenis.
7. Įveskite šias parametrų vertes:

   | Parametro pavadinimas | Vertė |
   |----------------|-------|
   | Serveris       | Įveskite serverio be serverio SQL Azure Synapse galinio punkto, kurį sukūrėte skyriuje Diegti ir [Konfigūruoti darbo Azure Synapse](#install-and-configure-azure-synapse-workspace) sritį, pavadinimą. Šią vertę galima rasti Azure Synapse **"Azure" portalo** darbo srities apžvalgos puslapyje. |
   | Duomenų bazė | Įveskite vertę "CommerceAnalytics".
   | Kalba | Pasirinkite vertę iš išplečiamojo sąrašo. Parametras naudojamas lokalizuoties produktų ir kategorijų pavadinimams. Ši vertė abc nuo abc. |
   | Datų diapazonas | Pasirinkite vertę iš išplečiamojo sąrašo. Pasirinkto mėnesių skaičiaus duomenys bus importuoti į duomenų Power BI rinkinį. Duomenų rinkinio dydis ir sinchronizavimui reikalingas laikas priklauso nuo jūsų pasirinkties reikšmės. |

8. Pasirinkite **Toliau**. Jums bus pasiūlyta įvesti kredencialus, kurie bus naudojami jungiantis prie Azure Synapse SQL duomenų bazės. Įveskite šias vertes:

   | Parametro pavadinimas | Vertė |
   |----------------|-------|
   |Autentifikavimo metodas|Pasirinkite **pagrindinį**.|
   |Vartotojo vardas| Įveskite "reportreadonlyuser".|
   |Slaptažodis|Įveskite reikšmę, kurią naudojote [placeholder_password](#install-and-configure-azure-synapse-workspace) setupSynapse.sql scenarijuje. Tai yra abonemento reportreadonlyuser slaptažodis.| 

9. Pasirinkite **prisijungimą ir** prisijunkite.
10. Palaukite, kol bus atnaujintas duomenų rinkinys. Tada, pasirinkdami piktogramą Redaguoti, eikite **į programos darbo** sritį. Darbo srityje galite patikrinti duomenų rinkinio atnaujinimo būseną. Taip pat galite nustatyti savo duomenų rinkinio automatinio atnaujinimo grafikus, tvarkyti teises ir pervardyti programos egzempliorių.

### <a name="privacy"></a>Privatumas
Mes rūpinamės jūsų privatumu. Norėdami daugiau sužinoti apie privatumą, perskaitykite mūsų [privatumo](https://go.microsoft.com/fwlink/?LinkId=521839) patvirtinimą.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
