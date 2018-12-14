---
title: "Elektroniniai pranešimai"
description: "Šioje temoje pateikiama „Microsoft Dynamics 365 for Finance and Operations“ elektroninių pranešimų apžvalga ir nustatymo informacija."
author: ShylaThompson
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 232398a6c4193d0074881e26fff361deb9784bf2
ms.openlocfilehash: 082ad886f40a52457900523f44158da3ed939458
ms.contentlocale: lt-lt
ms.lasthandoff: 12/04/2018

---

# <a name="electronic-messaging"></a>Elektroniniai pranešimai

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama „Microsoft Dynamics 365 for Finance and Operations“ elektroninių pranešimų apžvalga ir nustatymo informacija.

Neseniai įvairių šalių ir regionų vyriausybės bei teisės aktų leidybos institucijos visame pasaulyje įvykdė tose šalyse ar regionuose registruotų įmonių ataskaitų teikimo reikalavimus. Reikalavimų tikslas – įgalinti gauti duomenis iš tų įmonių elektroniniu formatu tiesiogiai iš sistemų, kuriose jie buvo apskaičiuoti, saugomi ir apdoroti.

„Finance and Operations“ elektroninių pranešimų funkcionalumą palaiko įvairių procesų elektroninės veiklos suderinamumas tarp „Finance and Operations“ ir sistemų, kurias vyriausybės ir teisės aktų leidybos institucijos siūlo ataskaitoms teikti bei oficialiai informacijai teikti ir gauti.

Elektroninių pranešimų funkcija yra integruota į modulį **Elektroninės ataskaitos** (ER). Todėl elektroniniams pranešimams galite nustatyti ER formatus. Daugiau informacijos žr. [Elektroninės ataskaitos (ER)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

Elektroniniai pranešimai grindžiami toliau nurodytais objektais.

- **Elektroninis pranešimas** – ataskaita arba deklaracija, kuri turi būti pateikta ir (arba) perduota įmonės viduje. Pavyzdys yra ataskaita, siunčiama mokesčių inspekcijai.
- **Elektroninio pranešimo elementai** – įrašai, kurie turi būti įtraukti į pateikiamą pranešimą.
- **Elektroninių pranešimų apdorojimas** – susietų arba nesusietų veiksmų grandinė, kuri turi būti vykdoma norint surinkti reikiamus duomenis, generuoti ataskaitas, saugoti duomenis „Microsoft Azure“ didelių dvejetainių objektų saugykloje, perduoti ataskaitas ne sistemoje, gauti atsakymus ne iš sistemos bei atnaujinti duomenų bazę, remiantis gauta informacija.

Toliau pateiktoje iliustracijoje parodytas elektroninių pranešimų duomenų srautas.

![Elektroninių pranešimų duomenų srautas](media/electronic-messaging-data-flow.png)

Elektroninių pranešimų funkcija palaiko toliau nurodytus scenarijus.

- Rankiniu būdu kurti pranešimus ir generuoti ataskaitas, grindžiamas susietais įvairių tipų ER eksportavimo formatais: „Microsoft Excel“, XML, „JavaScript Object Notation“ (JSON), PDF, tekstu ir „Microsoft Word“.
- Automatiškai kurti ir apdoroti pranešimus, grindžiamus informacija, kurios buvo prašoma, ir gauta informacija iš institucijos naudojant susietą ER importavimo formatą.
- Rinkti ir apdoroti informaciją iš duomenų šaltinio („Finance and Operations“ lentelės) kaip pranešimo elementų.
- Saugoti papildomą informaciją ir įvertinti įvairias vertes, iškviečiant konkrečiai apibrėžtas vykdomąsias klases, susijusias su pranešimais ar pranešimų elementais.
- Sujungti surinktą į pranešimo elementus informaciją, išskaidyti šią informaciją pagal pranešimą ir generuoti ataskaitas, kurios susietos ER eksportavimo formatais.
- Perduoti ataskaitas, sugeneruotas žiniatinklio tarnybai naudojant saugos informaciją, saugomą „Azure Key Vault“.
- Gauti atsakymą iš žiniatinklio tarnybos, interpretuoti atsakymą ir prireikus atnaujinti „Finance and Operations“ duomenis.
- Saugoti ir peržiūrėti visas sugeneruotas ataskaitas.
- Saugoti ir peržiūrėti visą žurnalo informaciją, susijusią su veiksmais, vykdomais pranešimui ar pranešimo elementui.
- Valdyti apdorojimo procesą naudojant įvairias pranešimo ir pranešimo elementų būsenas.

## <a name="set-up-electronic-messaging"></a>Nustatyti elektroninius pranešimus

Elektroniniai pranešimai gali padėti palaikyti skirtingiems dokumentų tipams skirtų įvairių elektroninių ataskaitų teikimo procesus. Taikant kai kuriuos sudėtingus scenarijus nustatyta, kad elektroniniai pranešimai turėtų daug pranešimo būsenų, pranešimo elementų būsenų, veiksmų, papildomų laukų bei vykdomųjų klasių kombinacijų. Galima importuoti šių scenarijų duomenų objektų paketus. Jei naudojate šiuos duomenų objektų paketus, turite juos importuoti į juridinį subjektą naudodami duomenų valdymo įrankį. Daugiau informacijos apie tai, kaip naudoti duomenų valdymo įrankį, žr. [Duomenų valdymas](../../dev-itpro/data-entities/data-entities-data-packages.md).

Jei neimportuojate duomenų objekto paketo, galite rankiniu būdu nustatyti elektroninių pranešimų funkciją. Tokiu atveju turite nustatyti toliau nurodytus elementus. 

- [Numeracijos](#number-sequences)
- [Pranešimų elementų tipai ir būsenos](#message-item-types-and-statuses)
- [Pranešimo būsenos](#message-statuses)
- [Papildomi laukai](#additional-fields)
- [Vykdomosios klasės parametrai](#executable-class-settings)
- [Automatinio įrašų įvedimo veiksmai](#populate-records-actions)
- [Žiniatinklio tarnybos parametrai](#web-service-settings)
- [Pranešimų apdorojimo veiksmai](#message-processing-actions)
- [El. pranešimų apdorojimas](#electronic-message-processing)

Tolesniuose skyriuose pateikiama daugiau informacijos apie šiuos elementus.

### <a name="number-sequences"></a>Numeravimai

Nustatykite pranešimų ir pranešimų elementų numeracijas. Numeracijos naudojamos pranešimams ir pranešimų elementams automatiškai sunumeruoti, o priskirti numeriai bus naudojami kaip unikalūs sistemos pranešimų ir pranešimų elementų identifikatoriai. Elektroninių pranešimų numeracijas galite nustatyti puslapyje **Didžiosios knygos parametrai** (**Didžioji knyga** \> **Didžiosios knygos nustatymas** \> **Didžiosios knygos parametrai**).

### <a name="message-item-types-and-statuses"></a>Pranešimų elementų tipai ir būsenos

Pranešimų elementų tipai nurodo įrašų, kurie bus naudojami elektroniniuose pranešimuose, tipus. Pranešimų elementų tipus galite nustatyti puslapyje **Pranešimų elementų tipai** (**Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Pranešimų elementų tipai**).

Pranešimų elementų būsenos nurodo būsenas, kurios bus taikomos jūsų nustatomam pranešimo elementų apdorojimui. Pranešimų elementų būsenas galite nustatyti puslapyje **Pranešimų elementų būsenos** (**Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Pranešimų elementų būsenos**).

### <a name="message-statuses"></a>Pranešimo būsenos

Nustatykite pranešimo būsenas, kurios turi būti prieinamos pranešimui apdoroti. Pranešimo būsenas galite nustatyti puslapyje **Pranešimo būsenos** (**Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Pranešimo būsenos**).

### <a name="additional-fields"></a>Papildomi laukai

Elektroninių pranešimų funkcija leidžia automatiškai įvesti įrašus iš operacijų lentelės. Tokiu būdu galite ataskaitoms parengti įrašus, o paskui juos pateikti. Kartais operacijų lentelėje nebūna pakankamai informacijos, kad būtų galima pateikti įrašą pagal ataskaitos reikalavimus. Užpildyti visą informaciją, kuri turi būti pateikta įrašant, galite nustatydami papildomus laukus. Papildomi laukai gali būti susieti su pranešimais ir pranešimų elementais. Papildomus laukus galite nustatyti puslapyje **Papildomi laukai** (**Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Papildomi laukai**).

Toliau pateiktoje lentelėje aprašomi puslapyje **Papildomi laukai** esantys laukai.

| Laukas                | aprašymas |
|----------------------|-------------|
| Lauko pavadinimas           | Įveskite su procesu susijusių pranešimo elementų papildomo atributo pavadinimą. Šis pavadinimas rodomas vartotojo sąsajoje vykdant procesą. Jį taip pat galima naudoti su procesu susijusiose ER konfigūracijose. |
| aprašymas          | Įveskite su procesu susijusių pranešimo elementų papildomo atributo aprašą. |
| Lauko vertė          | Įveskite lauko vertę, kurią naudosite pranešimo elemento atžvilgiu ataskaitų teikimo metu. |
| Lauko aprašas    | Įveskite lauko vertės, kurią naudosite pranešimo elemento atžvilgiu ataskaitų teikimo metu, aprašą. |
| Kodo tipas         | Kai kurios papildomos laukų vertės gali būti apribotos konkrečių sąskaitų tipais. Pasirinkite vieną šių verčių: **Visi**, **Klientas** arba **Tiekėjas**. |
| Sąskaitos kodas         | Jei pasirinkote **Klientas** arba **Tiekėjas** lauke **Sąskaitos tipas**, galite dar labiau apriboti lauko verčių naudojimą iki konkrečios grupės arba lentelės. |
| Sąskaitos/grupės Nr. | Jei pasirinkote **Klientas** arba **Tiekėjas** lauke **Sąskaitos tipas** ir įvedėte grupę arba lentelę lauke **Sąskaitos kodas**, šiame lauke galite įvesti konkrečią grupę arba sąveikos objektą. |
| Galioja            | Nurodykite datą, nuo kurios reikia atsižvelgti į vertę. |
| Galiojimo pabaiga           | Nurodykite datą, nuo kurios reikia nepaisyti vertės. |

### <a name="executable-class-settings"></a>Vykdomosios klasės parametrai

Vykdomoji klasė – tai X++ metodas arba klasė, kurią elektroninių pranešimų apdorojimo procesas gali iškviesti pagal veiksmą, jei šiam procesui reikalingas tam tikras įvertinimas.

Vykdomąją klasę galite nustatyti rankiniu būdu puslapyje **Vykdomosios klasės parametrai** (**Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Vykdomosios klasės parametrai**). Sukurkite eilutę ir nustatykite toliau nurodytus laukus.

| Laukas                 | aprašymas |
|-----------------------|-------------|
| Vykdomoji klasė      | Įveskite pavadinimą, kuris bus naudojamas nustatant pranešimo apdorojimo veiksmą, su kuriuo susieta ši iškviečiama klasė. |
| aprašymas           | Įveskite vykdomosios klasės aprašą. |
| Vykdomosios klasės pavadinimas | Pasirinkite X++ vykdomąją klasę. |
| Vykdymo lygis       | Šis laukas nustatomas automatiškai, nes pasirinktos vykdomosios klasės vertė turi būti nustatyta iš anksto. Šis laukas riboja vykdomo susijusio įvertinimo lygį. |
| Klasės aprašas     | Šis laukas nustatomas automatiškai, nes pasirinktos vykdomosios klasės vertė turi būti nustatyta iš anksto. |

### <a name="populate-records-actions"></a>Automatinio įrašų įvedimo veiksmai

Naudojate veiksmus įrašams automatiškai įvesti, kuriuos reikia nustatyti įrašams prie pranešimo elementų lentelės pridėti, kad juos būtų galima įtraukti į elektroninį pranešimą. Pavyzdžiui, jei jūsų elektroninis pranešimas turi pranešti kliento SF, turite nustatyti veiksmą **Automatiškai įvesti įrašus**, kuris susietas su lentele **Kliento SF žurnalas** (lauke **Duomenų šaltinis**). Veiksmus įrašams automatiškai įvesti galite nustatyti puslapyje **Automatinio įrašų įvedimo veiksmas** (**Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Automatinio įrašų įvedimo veiksmai**). Sukurkite naują kiekvieno veiksmo, kuris turi pridėti įrašų prie lentelės, įrašą ir nustatykite toliau nurodytus laukus.

| Laukas       | aprašymas                                                               |
|-------------|---------------------------------------------------------------------------|
| Pavadinimas / vardas ir (arba) pavardė        | Įveskite veiksmo, kuris į jūsų procesą automatiškai įveda įrašus, pavadinimą.       |
| aprašymas | Įveskite veiksmo, kuris į jūsų procesą automatiškai įveda įrašus, aprašą. |

„FastTab“ skirtuke **Duomenų šaltinių nustatymas** įtraukite eilutę kiekvienam duomenų šaltiniui, kuris naudojamas procesui, ir nustatykite toliau nurodytus laukus.

| Laukas                  | aprašymas |
|------------------------|-------------|
| Pavadinimas / vardas ir (arba) pavardė                   | Įveskite duomenų šaltinio pavadinimą. |
| Pranešimo prekės tipas      | Pasirinkite pranešimo elemento, kuris turi būti naudojamas kuriant duomenų šaltinio įrašus, tipą. |
| Kodo tipas           | Pasirinkite sąskaitos, kuri turi būti susieta su duomenų šaltinio įrašais, tipą. |
| Pagrindinės lentelės pavadinimas      | Pasirinkite „Finance and Operations“ lentelę, kuri turi būti duomenų šaltinis. |
| Laukas Dokumento numeris  | Pasirinkite lauką, iš kurio turi būti paimtas dokumento numeris pasirinktoje lentelėje. |
| Laukas Dokumento data    | Pasirinkite lauką, iš kurio turi būti paimta dokumento data pasirinktoje lentelėje. |
| Laukas Dokumento sąskaita | Pasirinkite lauką, iš kurio turi būti paimta dokumento sąskaita pasirinktoje lentelėje. |
| Vartotojo užklausa             | Jei šis žymės langelis pažymėtas, galite nustatyti užklausą pasirinkdami virš tinklelio esantį lauką **Redaguoti užklausą**. Priešingu atveju visi įrašai bus automatiškai įvesti iš duomenų šaltinio. |

### <a name="web-service-settings"></a>Žiniatinklio tarnybos parametrai

Naudojate žiniatinklio tarnybos parametrus tiesioginiam duomenų perdavimui į žiniatinklio tarnybą nustatyti. Žiniatinklio tarnybos parametrus galite nustatyti puslapyje **Žiniatinklio tarnybos parametrai** (**Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Žiniatinklio tarnybos parametrai**).

Toliau pateiktoje lentelėje aprašomi puslapio **Žiniatinklio tarnybos parametrai** laukai.

| Laukas                   | aprašymas |
|-------------------------|-------------|
| Tinklo tarnyba             | Įveskite žiniatinklio tarnybos pavadinimą. |
| aprašymas             | Įveskite žiniatinklio tarnybos aprašą. |
| Interneto adresas        | Įveskite žiniatinklio tarnybos interneto adresą. |
| Sertifikatas             | Pasirinkite anksčiau nustatytą raktų saugyklos sertifikatą. |
| Atsakymo tipas – XML | Jei atsakymo tipas yra XML, nustatykite šią parinktį į **Taip**. |
| Užklausos metodas          | Nurodykite užklausos metodą. HTTP apibrėžia užklausų metodų, nurodančių veiksmą, kuris turi būti atliekamas nurodytiems ištekliams, rinkinį. Galimas metodas **GAUTI**, **REGISTRUOTI** arba kitas HTTP metodas. |
| Užklausų antraštės         | Nurodykite užklausų antraštes. Užklausos antraštė – tai HTTP antraštė, kuri gali būti naudojama HTTP užklausai ir kuri nesusijusi su pranešimo turiniu. |
| Priimti kodavimą         | Nurodykite priimtiną kodavimą. Priimtino kodavimo užklausos HTTP antraštėje skelbiamas turinio kodavimas, kurį klientas gali suprasti. Toks turinio kodavimas dažniausiai yra glaudinimo algoritmas. |
| Turinio tipas            | Nurodykite turinio tipą. Turinio tipo objekto antraštė nurodo išteklių publikavimo kanalo tipą. |

### <a name="message-processing-actions"></a>Pranešimų apdorojimo veiksmai

Naudojate pranešimų apdorojimo veiksmus, kad sukurtumėte savo procesų veiksmus ir nustatytumėte jų parametrus. Pranešimų apdorojimo veiksmus galite nustatyti puslapyje **Pranešimų apdorojimo veiksmai** (**Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Pranešimų apdorojimo veiksmai**).

Toliau pateiktose lentelėse aprašomi puslapio **Pranešimų apdorojimo veiksmai** laukai.

#### <a name="general-fasttab"></a>Bendras „FastTab“ skirtukas

| Laukas                   | aprašymas |
|-------------------------|-------------|
| Veiksmo tipas             | Pasirinkite veiksmo tipą. Informacijos apie galimas parinktis žr. skyriuje [Pranešimų apdorojimo veiksmų tipai](#message-processing-action-types). |
| Formato susiejimas          | Pasirinkite ER formatą, kuris turi būti iškviestas veiksmui atlikti. Šis laukas galimas tik veiksmų tipams **Elektroninių ataskaitų eksportavimas**, **Elektroninių ataskaitų importavimas** ir **Elektroninių ataskaitų eksportavimo pranešimas**. |
| Pranešimo prekės tipas       | Pasirinkite įrašų, kurių veiksmą reikia įvertinti, tipą. Šis laukas galimas veiksmų tipams **Pranešimo elemento vykdymo lygis**, **Elektroninių ataskaitų eksportavimas** ir **Elektroninių ataskaitų importavimas**, taip pat kai kuriems kitiems tipams. Jei šį lauką paliksite tuščią, bus vertinami visi pranešimų apdorojimui apibrėžti pranešimų elementų tipai. |
| Vykdomoji klasė        | Pasirinkite anksčiau sukurtus vykdomosios klasės parametrus. Šis laukas galimas tik veiksmų tipams **Pranešimo elemento vykdymo lygis** ir **Pranešimo elemento vykdymo lygis**. |
| Automatinio įrašų įvedimo veiksmas | Pasirinkite anksčiau nustatytą automatinio įrašų įvedimo veiksmą. Šis laukas galimas tik veiksmų tipui **Automatiškai įvesti įrašus**. |

##### <a name="message-processing-action-types"></a>Pranešimų apdorojimo veiksmų tipai

Galimos toliau nurodytos lauko **Veiksmo tipas** parinktys.

- **Automatiškai įvesti įrašus** – veiksmas **Automatiškai įvesti įrašus** turi būti nustatytas anksčiau. Susiekite jį su veiksmo tipu **Automatiškai įvesti įrašus**, kad jį būtų galima įtraukti į apdorojimą. Laikoma, kad šis veiksmo tipas naudojamas pirmam veiksmui apdorojant pranešimus. Todėl šio tipo veiksmui galima nustatyti tik rezultatų būseną. Pradinės būsenos nustatyti negalima.
- **Kurti pranešimą** – naudokite šį tipą, kad vartotojai galėtų rankiniu būdu kurti pranešimus puslapyje **Elektroninis pranešimas**. Šio tipo veiksmui negalima nustatyti pradinės būsenos.
- **Pranešimo vykdymo lygis** – naudokite šį tipą vykdomajai klasei, kuri turi būti įvertinta pranešimo lygiu, nustatyti.
- **Pranešimo elemento vykdymo lygis** – naudokite šį tipą vykdomajai klasei, kuri turi būti įvertinta pranešimo elemento lygiu, nustatyti.
- **Elektroninių ataskaitų eksportavimas** – naudokite šį tipą veiksmams, kuriais turi būti generuojama ataskaita, grindžiama ER eksportavimo konfigūracija pranešimo elemento lygiu.
- **Elektroninių ataskaitų eksportavimo pranešimas** – naudokite šį tipą veiksmams, kuriais turi būti generuojama ataskaita, grindžiama ER eksportavimo konfigūracija pranešimo lygiu (pavyzdžiui, kai pranešimas neturi jokių pranešimo elementų).
- **Elektroninių ataskaitų importavimas** – naudokite šį tipą veiksmams, kuriais turi būti generuojama ataskaita, grindžiama ER importavimo konfigūracija.
- **Pranešimų lygio vartotojų apdorojimas** – naudokite šį tipą veiksmams, kuriais nurodomi tam tikri rankiniai vartotojo veiksmai. Pavyzdžiui, vartotojas gali atnaujinti pranešimų būseną.
- **Vartotojų apdorojimas** – naudokite šį tipą veiksmams, kuriais nurodomas tam tikras rankinis vartotojo veiksmas. Pavyzdžiui, vartotojas gali atnaujinti pranešimų elementų būseną.
- **Žiniatinklio tarnyba** – naudokite šį tipą veiksmams, kuriais žiniatinklio tarnybai turi būti perduodama sugeneruota ataskaita. Šis veiksmo tipas nenaudojamas Italijos pirkimo ir pardavimo sąskaitų faktūrų ryšių ataskaitoms teikti.
- **Užklausos tikrinimas** – naudokite šį tipą tikrinimui iš serverio prašyti.

#### <a name="initial-statuses-fasttab"></a>Pradinių būsenų „FastTab“

> [!NOTE]
> „FastTab“ skirtuko **Pradinės būsenos** negalima naudoti veiksmams, kurių pradinis tipas yra **Automatiškai įvesti įrašus** arba **Kurti pranešimą**.

| Laukas               | aprašymas                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| Pranešimo prekės būsena | Pasirinkite pranešimo elemento būseną, pagal kurią turi būti įvertintas pasirinkto pranešimo apdorojimo veiksmas. |
| aprašymas         | Pasirinkto pranešimo elemento būsenos aprašas.                                                  |

#### <a name="result-statuses-fasttab"></a>Galutinių būsenų „FastTab“

| Laukas               | aprašymas |
|---------------------|-------------|
| Pranešimo būsena      | Pasirinkite pranešimų būsenas, pagal kurias turi būti įvertintas pasirinkto pranešimo apdorojimo veiksmas. Šis laukas galimas tik pranešimų apdorojimo veiksmams, kurie vertinami pranešimo lygiu. Pavyzdžiui, jis galimas veiksmų tipams **Elektroninių ataskaitų eksportavimas** ir **Elektroninių ataskaitų importavimas**. Jis negalimas veiksmų tipams **Vartotojų apdorojimas** ir **Pranešimo elemento vykdymo lygis**. |
| aprašymas         | Pasirinkto pranešimo būsenos aprašas. |
| Atsiliepimo tipas       | Pasirinkto pranešimo būsenos atsakymo tipas. |
| Pranešimo prekės būsena | Pasirinkite rodomas būsenas, kurios turi būti prieinamos įvertinus pasirinkto pranešimo apdorojimo veiksmą. Šis laukas galimas tik pranešimų apdorojimo veiksmams, kurie vertinami pranešimo elemento lygiu. Pavyzdžiui, jis galimas veiksmų tipams **Vartotojų apdorojimas** ir **Pranešimo elemento vykdymo lygis**. Šiame lauke pranešimų apdorojimo veiksmams, įvertintiems pranešimo lygiu, rodoma pranešimo elemento būsena, kuri buvo nustatyta pasirinkto pranešimo būsenai. |

### <a name="electronic-message-processing"></a>El. pranešimų apdorojimas

Elektroninių pranešimų apdorojimas yra pagrindinė elektroninių pranešimų funkcionalumo koncepcija. Ji sujungia veiksmus, kuriais turi būti įvertintas elektroninis pranešimas. Veiksmus galima susieti naudojant pradinę būseną ir rezultatų būseną. Arba veiksmus, kurių tipas **Vartotojų apdorojimas**, galima pradėti savarankiškai. Puslapyje **Elektroninių pranešimų apdorojimas** (**Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Elektroninių pranešimų apdorojimas**) taip pat galite pasirinkti papildomus laukus, kurie turi būti palaikomi apdorojant.

„FastTab“ skirtuke **Veiksmas** galima pridėti iš anksto apibrėžtų veiksmų apdorojimui. Galite nurodyti, ar veiksmą reikia vykdyti atskirai, ar jį galima inicijuoti apdorojant. (Vartotojo veiksmai turi būti vykdomi atskirai.)

„FastTab“ skirtuke **Pranešimo elemento papildomi laukai** galima pridėti iš anksto apibrėžtų papildomų laukų, susijusių su pranešimo elementais. Turite pridėti papildomų laukų kiekvienam pranešimo elemento, su kuriuo susiję laukai, tipui.

„FastTab“ skirtuke **Pranešimo papildomi laukai** galima pridėti iš anksto apibrėžtų papildomų laukų, susijusių su pranešimais.

„FastTab“ skirtuke **Saugos vaidmenys** galima nustatyti saugos vaidmenis, iš anksto apibrėžtus sistemoje konkrečiam apdorojimui. Vartotojai, turintys konkretų vaidmenį, matys tik tam vaidmeniui apibrėžtą apdorojimą.

„FastTab“ skirtuke **Paketas** galima nustatyti apdorojimą dirbti paketiniu režimu.

## <a name="work-with-electronic-messages-functionality"></a>Darbas su elektroninių pranešimų funkcija

Jei dirbate pranešimo lygiu, puslapis **Elektroniniai pranešimai** (**Mokesčiai** \> **Užklausos ir ataskaitos** \> **Elektroniniai pranešimai** \> **Elektroniniai pranešimai**) bus naudingesnis. Jei dirbate duomenų rinkinio (pranešimo elemento) lygiu, puslapis **Elektroninio pranešimo elementai** (**Mokesčiai** \> **Užklausos ir ataskaitos** \> **Elektroniniai pranešimai** \> **Elektroninio pranešimo elementai**) bus naudingesnis.

### <a name="electronic-messages"></a>El. pranešimai

Puslapyje **Elektroniniai pranešimai** pateikiamas jums prieinamas apdorojimas pagal jūsų vaidmenį. Saugos vaidmenys yra susieti su apdorojimu nustatant šį apdorojimą. Kiekvienam jums prieinamam apdorojimui puslapyje pateikiami elektroniniai pranešimai ir su jais susijusi informacija.

„FastTab“ skirtuke **Pranešimai** rodomi pasirinkto apdorojimo elektroniniai pranešimai. Priklausomai nuo pasirinkto pranešimo būsenos ir iš anksto apibrėžto apdorojimo, galite vykdyti kelis veiksmus pasirinkdami virš tinklelio esančius mygtukus.

- **Naujas** – šis mygtukas susietas su veiksmų tipu **Kurti pranešimą**.
- **Naikinti** – šį mygtuką galima naudoti, jei pažymėtas žymės langelis **Leisti naikinti**, skirtas pasirinkto pranešimo dabartinei būsenai.
- **Generuoti ataskaitą** – šis mygtukas susietas su veiksmų tipu **Elektroninių ataskaitų eksportavimo pranešimas**.
- **Siųsti ataskaitą** – šis mygtukas susietas su veiksmų tipu **Žiniatinklio tarnyba**.
- **Atnaujinti būseną** – šis mygtukas susietas su veiksmų tipu **Pranešimų lygio vartotojų apdorojimas**.
- **Pranešimo elementai** – atidaromas puslapis **Elektroninio pranešimo elementai**.

„FastTab“ skirtuke **Veiksmų žurnalas** rodoma informacija apie visus veiksmus, kurie buvo vykdomi pasirinktam pranešimui.

„FastTab“ skirtuke **Pranešimo papildomi laukai** rodomi visi papildomi laukai, kuriais apibrėžiami pranešimai nustatant apdorojimą. Jame taip pat rodomos tų papildomų laukų vertės.

„FastTab“ skirtuke **Pranešimo elementai** rodomi visi su pasirinktu pranešimu susiję pranešimo elementai.

Galite peržiūrėti visus pasirinkto pranešimo priedus. Šie priedai yra jau sugeneruotos ir gautos ataskaitos. Norėdami peržiūrėti priedus, pasirinkite pranešimą, tada veiksmų srityje pasirinkite mygtuką **Priedas**.

![Priedo mygtukas](media/attachment-icon.png)

Puslapyje **Priedai** rodomi visi su pranešimu susiję priedai. Norėdami peržiūrėti failą, pasirinkite jį iš sąrašo kairėje, tada veiksmų srityje pasirinkite **Atidaryti**.

![Mygtukas Atidaryti](media/open-button.png)

Norėdami peržiūrėti priedą, susijusį su konkrečiu veiksmu, kuris anksčiau buvo vykdomas pranešimui, pasirinkite pranešimą puslapyje **Elektroniniai pranešimai**, tada „FastTab“ skirtuke **Veiksmų žurnalas** pasirinkite veiksmą. Tada veiksmų srityje pasirinkite mygtuką **Priedas**.

Taip pat galite vykdyti visą apdorojimą arba tik konkretų veiksmą, veiksmų srityje pasirinkdami **Vykdyti apdorojimą**.

### <a name="electronic-message-items"></a>El. pranešimų prekės

Puslapyje **Elektroninio pranešimo elementai** pateikiami visi pranešimo elementai ir veiksmų, kurie buvo vykdomi kiekvienam pranešimo elementui, žurnalas. Jame taip pat rodomi papildomi laukai, kuriais apibrėžiami pranešimo elementai, ir tų papildomų laukų vertės.

Toliau pateiktoje lentelėje aprašomi skirtuko **Pranešimo elementai** laukai.

<table>
<thead>
<tr>
<th>Laukas</th>
<th>aprašymas</th>
</tr>
</thead>
<tbody>
<tr>
<td>Vykdymas</td>
<td>Apdorojimo, kuris buvo naudojamas pranešimo elementui sukurti, pavadinimas.</td>
</tr>
<tr>
<td>Pranešimo prekė</td>
<td>Pranešimo elemento ID. Šis ID priskiriamas automatiškai pagal numeraciją <strong>Pranešimo elementas</strong>, kuri apibrėžta puslapyje <strong>Didžiosios knygos parametrai</strong>.</td>
</tr>
<tr>
<td>Pranešimo prekės data</td>
<td>Pranešimo elemento sukūrimo data.</td>
</tr>
<tr>
<td>Pranešimo prekės tipas</td>
<td>Pranešimo elemento tipas. Tam pačiam apdorojimui galima nustatyti kelių tipų pranešimų elementus (pavyzdžiui, <strong>Gaunamos SF</strong> ir <strong>Siunčiamos SF</strong>). Šis laukas gali būti automatiškai užpildytas tik tada, kai sąskaita faktūra įtraukiama į pranešimo elementų lentelę.</td>
</tr>
<tr>
<td>Pranešimo prekės būsena</td>
<td>Faktinė pranešimo elemento būsena. Galimos būsenos skiriasi priklausomai nuo pranešimo elemento tipo. Štai keletas pavyzdžių:
<ul>
<li><strong>Automatiškai įvesta</strong> – įrašas pridėtas prie pranešimo elementų lentelės.</li>
<li><strong>Įvertinta</strong> – apskaičiuoti papildomi pranešimo elemento atributai.</li>
<li><strong>Pateikta</strong> – pranešimo elementas sėkmingai įtrauktas į ataskaitą.</li>
<li><strong>Neįtraukta</strong> – ši būsena gali būti naudinga, jei turite pašalinti kai kuriuos pranešimo elementus iš ataskaitos prieš ją eksportuodami.</li>
</ul>
</td>
</tr>
<tr>
<td>Perdavimo data</td>
<td>Pranešimo elemento perdavimo apdorojimui, kuris automatiškai perduoda sugeneruotą ataskaitą ne sistemoje, data.</td>
</tr>
<tr>
<td>Dokumento numeris</td>
<td>Šis laukas užpildomas automatiškai pagal automatinio įrašų įvedimo veiksmo nustatymą. Šis laukas gali būti automatiškai užpildytas tik tada, kai sąskaita faktūra įtraukiama į pranešimo elementų lentelę.</td>
</tr>
<tr>
<td>Sąskaitos numeris</td>
<td>Kliento arba tiekėjo sąskaitos numeris (arba kita lauko vertė, atsižvelgiant į lauką, kuriuo apibrėžtas veiksmas <strong>Automatiškai įvesti įrašus</strong>). Šis laukas gali būti automatiškai užpildytas tik tada, kai sąskaita faktūra įtraukiama į pranešimo elementų lentelę.</td>
</tr>
<tr>
<td>Pranešimas</td>
<td>Pranešimo numeris. Šis numeris priskiriamas automatiškai pagal numeraciją <strong>Pranešimas</strong>, kuri apibrėžta puslapyje <strong>Didžiosios knygos parametrai</strong>.</td>
</tr>
<tr>
<td>Pranešimo būsena</td>
<td>Faktinė elektroninio pranešimo būsena.</td>
</tr>
<tr>
<td>Kitas veiksmas</td>
<td>Tolesni veiksmai, kuriuos galima inicijuoti dabartinei pranešimo elemento būsenai.</td>
</tr>
</tbody>
</table>

Skirtuke **Papildomi laukai** rodomi papildomi pasirinkto pranešimo elemento laukai ir jų vertės.

#### <a name="run-processing"></a>Vykdyti apdorojimą

Veiksmų srityje pasirinkite **Vykdyti apdorojimą** pranešimo elementų apdorojimui vykdyti. Norėdami vykdyti konkretų veiksmą, dialogo lange **Vykdyti apdorojimą** parinktį **Pasirinkti veiksmą** nustatykite į **Taip**, tada pasirinkite veiksmą. Norėdami vykdyti visą apdorojimą, parinktį **Pasirinkti veiksmą** palikite nustatytą į **Ne**.

#### <a name="generate-report"></a>Generuoti ataskaitą

Norėdami sugeneruoti ataskaitą, veiksmų srityje pasirinkite **Generuoti ataskaitą**. Šis mygtukas susietas su veiksmų tipu **Elektroninių ataskaitų eksportavimas**.

#### <a name="update-status"></a>Atnaujinti būseną

Norėdami atnaujinti vieno ar daugiau pranešimo elementų būseną, veiksmų srityje pasirinkite **Atnaujinti būseną**. Norėdami pasirinkti atnaujinti pranešimo elementus, dialogo lange **Atnaujinti būseną** naudokite „FastTab“ skirtuką **Įtrauktini įrašai**. Įsitikinkite, kad teisingai apibrėžiate pasirinkimo kriterijus, nes pranešimų elementų būsenos atnaujinamos pagal šiuos kriterijus, pradinę pasirinkto veiksmo būseną ir vertę **Nauja būsena**, kurią nustatote. Baigus būsenos atnaujinimą bus sunku nustatyti, kurie elementai ką tik buvo atnaujinti. Todėl bus sunku atkurti būsenos naujinimus.

#### <a name="electronic-messages"></a>El. pranešimai

Norėdami peržiūrėti elektroninį pranešimą, susijusį su pasirinkto pranešimo elementu, veiksmų srityje pasirinkite **Elektroninis pranešimas**.

Taip pat galite peržiūrėti visus pranešimo elementą atitinkančius failus. Pasirinkite pranešimo elemento lauką **Pranešimas** arba veiksmų srityje pasirinkite **Elektroninis pranešimas**. Puslapyje **Elektroninis pranešimas** pasirinkite pranešimą ataskaitai peržiūrėti, tada veiksmų srityje pasirinkite mygtuką **Priedas**.

![Priedo mygtukas](media/attachment-icon.png)

Puslapyje **Priedai** rodomi visi su pranešimu susiję priedai. Norėdami peržiūrėti failą, pasirinkite jį iš sąrašo kairėje, tada veiksmų srityje pasirinkite **Atidaryti**.

![Mygtukas Atidaryti](media/open-button.png)

#### <a name="original-document"></a>Originalus dokumentas

Norėdami atidaryti pasirinkto pranešimo elemento originalų dokumentą, veiksmų srityje pasirinkite **Originalus dokumentas**.

## <a name="example"></a>Pavyzdys

Sukūrę savo ER formatą, susieję jį su duomenų šaltiniais ir užbaigę, galite paleisti jį naudodami darbo sritį **Elektroninės ataskaitos**. Generuojama ataskaita, kurią galite įrašyti vietoje.

Norėdami kontroliuoti šiuos ataskaitų teikimo proceso aspektus, turite nustatyti elektroninių pranešimų apdorojimą.

- Užregistruokite informaciją apie tai, kas sugeneravo ataskaitą.
- Užregistruokite, kada buvo sugeneruota ataskaita.
- Įrašykite ankstesnių laikotarpių sugeneruotas ataskaitas.

Šiame skyriuje pateikiamas pavyzdys, rodantis, kaip galite nustatyti elektroninių pranešimų funkciją ataskaitų teikimo procesui sukurti.

### <a name="set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Nustatykite ir vykdykite apdorojimą norėdami iškviesti paprastą ER eksportavimo formatą „Excel“ ataskaitai sugeneruoti

Šiame skyriuje pateikiamas pavyzdys, rodantis, kaip galite nustatyti elektroninius pranešimus ataskaitai, kuri pagrįsta „Excel“ ER eksportavimo formatu, generuoti. Pagal šį pavyzdį „Excel“ ER eksportavimo formatas jau turi būti sukurtas, susietas su duomenų šaltiniais ir užbaigtas. Elektroninių pranešimų numeracija jau turi būti nustatyta.

Tai naudinga, jei kurdami apdorojimą pirmiausia apibrėžiate apdorojimo veiksmus ir būsenas, kurios bus nustatytos. Šioje iliustracijoje rodoma, kaip pagal šį pavyzdį atrodo apdorojimas.

![Apdorojimo schema](media/processing-scheme.png)

#### <a name="create-message-statuses"></a>Kurti pranešimo būsenas

1. Eikite į **Mokesčiai \> Nustatymas \> Elektroniniai pranešimai \> Pranešimo būsenos**.
2. Kurti toliau nurodytas pranešimo būsenas.

    - Naujas
    - Parengta
    - Sugeneruota

    ![Pranešimo būsenos](media/message-statuses.png)

3. Būsenos **Nauja** eilutėje pažymėkite žymės langelį **Leisti naikinti**, kad vartotojai galėtų panaikinti šią būseną turinčius pranešimus.

#### <a name="create-additional-fields"></a>Kurti papildomus laukus

1. Eikite į **Mokesčiai \> Nustatymas \> Elektroniniai pranešimai \> Papildomi laukai**.
2. Pridėkite papildomą lauką ir jo vertes. Toliau pateikiamas pavyzdys.

    ![Papildomi laukai](media/additional-fields.png)

3. Parinktį **Vartotojo redaguojamas** nustatykite į **Taip**, kad vartotojai galėtų redaguoti lauką.

#### <a name="create-message-processing-actions"></a>Kurti pranešimų apdorojimo veiksmus

Pavyzdžiui, galite sukurti toliau nurodytus veiksmus.

- **Kurti pranešimą**
- **Atnaujinti į parengtą**
- **Generuoti ataskaitą**
- **Atnaujinti į pradinę būseną** (pasirinktinai)

1. Eikite į **Mokesčiai \> Nustatymas \> Elektroniniai pranešimai \> Pranešimų apdorojimo veiksmai**.
2. Kurti veiksmą, kurio pavadinimas **Kurti pranešimą**. „FastTab“ skirtuko **Bendras** lauke **Veiksmo tipas** pasirinkite **Kurti pranešimą**.
3. Kurti veiksmą, kurio pavadinimas **Atnaujinti į parengtą**, ir nustatyti toliau nurodytus laukus.

    - „FastTab“ skirtuko **Bendras** lauke **Veiksmo tipas** pasirinkite **Pranešimų lygio vartotojų apdorojimas**.
    - „FastTab“ skirtuko **Pradinės būsenos** lauke **Pranešimo būsena** pasirinkite **Nauja**.
    - „FastTab“ skirtuko **Galutinės būsenos** lauke **Pranešimo būsena** pasirinkite **Parengta**. Lauke **Atsakymo tipas** įveskite **Sėkmingai įvykdyta**.

4. Kurti veiksmą, kurio pavadinimas **Generuoti ataskaitą**, ir nustatyti toliau nurodytus laukus.

    - „FastTab“ skirtuko **Bendras** lauke **Veiksmo tipas** pasirinkite **Elektroninių ataskaitų eksportavimas**. Lauke **Formato susiejimas** pasirinkite ER eksportavimo formatą. Parinktys yra **Excel**, **XML**, **JSON**, **Tekstas** ir **Kita**.
    - „FastTab“ skirtuko **Pradinės būsenos** lauke **Pranešimo būsena** pasirinkite **Parengta**.
    - „FastTab“ skirtuko **Galutinės būsenos** lauke **Pranešimo būsena** pasirinkite **Sugeneruota**. Lauke **Atsakymo tipas** įveskite **Sėkmingai įvykdyta**.

    ![Generuoti ataskaitos veiksmą](media/generate-report-action.png)

5. Pasirinktinai. Norėdami leisti vartotojams pakartotinai keletą kartų generuoti ataskaitą, galite sukurti veiksmą **Atnaujinti į pradinę būseną** ir nustatyti toliau nurodytus laukus.

    - „FastTab“ skirtuko **Bendras** lauke **Veiksmo tipas** pasirinkite **Pranešimų lygio vartotojų apdorojimas**.
    - „FastTab“ skirtuko **Pradinės būsenos** lauke **Pranešimo būsena** pasirinkite **Sugeneruota**.
    - „FastTab“ skirtuko **Galutinės būsenos** lauke **Pranešimo būsena** pasirinkite **Parengta** arba (ir) **Nauja**. Lauke **Atsakymo tipas** įveskite **Sėkmingai įvykdyta**.

#### <a name="electronic-message-processing"></a>El. pranešimų apdorojimas

Šiame pavyzdyje visi veiksmai turi būti nustatyti taip, kad jie būtų vykdomi atskirai. Daroma prielaida, kad kiekvieną veiksmą inicijuos vartotojas.

1. Eikite į **Mokesčiai \> Nustatymas \> Elektroniniai pranešimai \> Elektroninių pranešimų apdorojimas**.
2. Prie savo apdorojimo pridėkite įrašą ir įtraukite visus anksčiau apibrėžtus veiksmus bei papildomą lauką.
3. Pasirinktinai. „FastTab“ skirtuke **Saugos vaidmenys** apibrėžkite savo apdorojimo saugos vaidmenis, kad apribotumėte prieigą prie konkrečių ataskaitų.
4. Eikite į **Mokesčiai \> Užklausos ir ataskaitos \> Elektroniniai pranešimai \> Elektroniniai pranešimai**.
5. Pasirinkite **Naujas** pranešimui sukurti. Šiuo metu galite pridėti datas ir aprašą. Taip pat galite atnaujinti papildomo lauko vertę, kaip jums reikia.

    ![Kurti elektroninį pranešimą](media/create-electronic-message.png)

„FastTab“ skirtuke **Veiksmų žurnalas** esančiame tinklelyje automatiškai užpildomas visų pranešime atliekamų veiksmų žurnalas.

Dabar galite panaikinti arba atnaujinti pranešimo būseną. Norėdami atnaujinti pranešimo būseną, pasirinkite **Atnaujinti būseną**, tada lauke **Nauja būsena** pasirinkite **Parengta**. Tada pasirinkite **Gerai**.

![Atnaujinti pranešimo būseną](media/update-status.png)

Pranešimo būsena atnaujinta į **Parengta** ir dabar galite generuoti ataskaitą pasirinkdami **Generuoti ataskaitą**. Ataskaita sugeneruota, o pranešimo būsena ir veiksmų žurnalas atnaujinti. Norėdami peržiūrėti sugeneruotą ataskaitą, veiksmų srityje pasirinkite mygtuką **Priedas**.

