---
title: Elektroniniai pranešimai
description: Šioje temoje pateikiama „Microsoft Dynamics 365 for Finance and Operations“ elektroninių pranešimų apžvalga ir nustatymo informacija.
author: ShylaThompson
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 2753f2828b4890d9893a1538e905bd7061e1bc33
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536876"
---
# <a name="electronic-messaging"></a>Elektroniniai pranešimai

[!include [banner](../includes/banner.md)]
[!include [preview-banner](../includes/preview-banner.md)]

Šioje temoje pateikiama „Microsoft Dynamics 365 for Finance and Operations“ elektroninių pranešimų apžvalga ir nustatymo informacija.

Neseniai įvairių šalių ir regionų vyriausybės bei teisės aktų leidybos institucijos visame pasaulyje įvykdė tose šalyse ar regionuose registruotų įmonių ataskaitų teikimo reikalavimus. Reikalavimų tikslas – įgalinti gauti duomenis iš tų įmonių elektroniniu formatu tiesiogiai iš sistemų, kuriose jie buvo apskaičiuoti, saugomi ir apdoroti.

„Finance and Operations“ elektroninių pranešimų funkcionalumą palaiko įvairių procesų elektroninės veiklos suderinamumas tarp „Finance and Operations“ ir sistemų, kurias vyriausybės ir teisės aktų leidybos institucijos siūlo ataskaitoms teikti bei oficialiai informacijai teikti ir gauti.

Elektroninių pranešimų funkcija yra integruota į modulį **Elektroninės ataskaitos** (ER). Todėl elektroniniams pranešimams galite nustatyti ER formatus. Daugiau informacijos žr. [Elektroninės ataskaitos (ER)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

Elektroniniai pranešimai grindžiami toliau nurodytais objektais.

- **Elektroninis pranešimas** – ataskaita arba deklaracija, kuri turi būti pateikta ir (arba) perduota įmonės viduje. Pavyzdys yra ataskaita, siunčiama mokesčių inspekcijai.
- **Elektroninio pranešimo elementai** – įrašai, kurie turi būti įtraukti į pateikiamą pranešimą.
- **Elektroninių pranešimų apdorojimas** – veiksmų grandinė, kuri turi būti vykdoma norint surinkti reikiamus duomenis, generuoti ataskaitas, saugoti duomenis „Microsoft Azure“ didelių dvejetainių objektų saugykloje, perduoti ataskaitas ne sistemoje, gauti atsakymus ne iš sistemos bei, remiantis gauta informacija, atnaujinti duomenų bazę. Grandinės veiksmai gali būti susieti arba atsieti

Toliau pateiktoje iliustracijoje parodytas elektroninių pranešimų duomenų srautas.

![Elektroninių pranešimų duomenų srautas](media/electronic-messaging-data-flow.png)

Elektroninių pranešimų funkcija palaiko toliau nurodytus scenarijus.

- Rankiniu būdu kurti pranešimus ir generuoti ataskaitas, grindžiamas susietais įvairių tipų ER eksportavimo formatais: „Microsoft Excel“, XML, „JavaScript Object Notation“ (JSON), PDF, tekstu ir „Microsoft Word“.
- Automatiškai kurti ir apdoroti pranešimus, grindžiamus informacija, kurios buvo prašoma, ir gauta informacija iš institucijos naudojant susietą ER importavimo formatą.
- Rinkti ir apdoroti informaciją iš duomenų šaltinio kaip pranešimo elementų. Duomenų šaltinis yra „Finance and Operations“ lentelė.
- Saugoti papildomą informaciją ir įvertinti įvairias vertes, iškviečiant konkrečiai apibrėžtas vykdomąsias klases, susijusias su pranešimais ar pranešimų elementais.
- Sujungti surinktą į pranešimo elementus informaciją, išskaidyti šią informaciją pagal pranešimą ir generuoti ataskaitas, kurios susietos ER eksportavimo formatais.
- Sugeneruotas ataskaitas perduoti žiniatinklio tarnybai naudojant saugos informaciją, saugomą sprendime „Azure Key Vault“.
- Gauti atsakymą iš žiniatinklio tarnybos, interpretuoti atsakymą ir atitinkamai atnaujinti „Finance and Operations“ duomenis.
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
- [Žiniatinklio programos](#web-applications)
- [Žiniatinklio tarnybos parametrai](#web-service-settings)
- [Pranešimų apdorojimo veiksmai](#message-processing-actions)
- [El. pranešimų apdorojimas](#electronic-message-processing)

Tolesniuose skyriuose pateikiama daugiau informacijos apie šiuos elementus.

### <a name="number-sequences"></a>Numeravimai

Nustatykite pranešimų ir pranešimų elementų numeracijas. Numeracijos naudojamos pranešimams ir pranešimų elementams automatiškai numeruoti. Priskirti numeriai sistemoje bus naudojami kaip unikalūs pranešimų ir pranešimų elementų identifikatoriai. Elektroninių pranešimų numeracijas galite nustatyti puslapyje **Didžiosios knygos parametrai** (**Didžioji knyga** \> **Didžiosios knygos nustatymas** \> **Didžiosios knygos parametrai**).

### <a name="message-item-types-and-statuses"></a>Pranešimų elementų tipai ir būsenos

Pranešimų elementų tipai nurodo įrašų, kurie bus naudojami elektroniniuose pranešimuose, tipus. Pranešimų elementų tipus galite nustatyti puslapyje **Pranešimų elementų tipai** (**Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Pranešimų elementų tipai**).

Pranešimų elementų būsenos nurodo būsenas, kurios bus taikomos jūsų nustatomam pranešimo elementų apdorojimui. Pranešimų elementų būsenas galite nustatyti puslapyje **Pranešimų elementų būsenos** (**Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Pranešimų elementų būsenos**).

Pranešimo elemento būsenos parametras **Leisti naikinti** nurodo, ar vartotojai gali panaikinti pranešimų elementus, kurie yra šios būsenos puslapiuose **Elektroniniai pranešimai** arba **Elektroninių pranešimų elementai**.

### <a name="message-statuses"></a>Pranešimo būsenos

Nustatykite pranešimo būsenas, kurios turi būti prieinamos pranešimui apdoroti. Pranešimo būsenas galite nustatyti puslapyje **Pranešimo būsenos** (**Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Pranešimo būsenos**).

Toliau pateiktoje lentelėje aprašomi puslapio **Pranešimų būsenos** laukai.

| Lauko pavadinimas          | Aprašas |
|---------------------|-------------|
| Pranešimo būsena      | Įveskite unikalų pranešimo būsenos pavadinimą. Pranešimų būsenos naudojamos apibūdinti, kokia yra elektroninio laiško būsena kiekvieną akimirką. Jūsų įvedamas pavadinimas rodomas puslapyje **Elektroniniai pranešimai** ir su elektroniniais pranešimais susijusiame žurnale. |
| Aprašas         | Įveskite pranešimo būsenos aprašą. |
| Atsiliepimo tipas       | Pasirinkite pranešimo būsenos atsako tipą. Atlikus kai kuriuos apdorojimo veiksmus gali būti pateiktas daugiau nei vienas atsako tipas. Pavyzdžiui, tipo **Žiniatinklio tarnyba** veiksmai gali pateikti tipo **Sėkmingai įvykdytas** arba **Techninė klaida** atsakus – tai priklauso nuo vykdymo rezultato. Šiuo atveju turite nurodyti abiejų tipų atsakų pranešimų būsenas. Norėdami gauti daugiau informacijos apie veiksmų tipus ir su jais susijusius atsakų tipus, žr. [Pranešimų apdorojimo veiksmų tipai](#message-processing-action-types). |
| Pranešimo prekės būsena | Kartais elektroninio pranešimo būsena turi paveikti susijusių pranešimo elementų būseną. Šiame lauke pasirinkite pranešimo elemento būseną, kad ją susietumėte su pranešimo būsena. |
| Leisti naikinti        | Pažymėkite šį žymės langelį, jei vartotojai turi galėti panaikinti elektroninius pranešimus, kurie yra šios būsenos puslapyje **Elektroniniai pranešimai**. |

### <a name="additional-fields"></a>Papildomi laukai

Elektroninių pranešimų funkcija leidžia užpildyti įrašus iš operacijų lentelės. Tokiu būdu galite ataskaitoms parengti įrašus, o paskui juos pateikti. Tačiau kartais operacijų lentelėse nepakanka informacijos, kad įrašus būtų galima užpildyti pagal ataskaitų reikalavimus. Norėdami užpildyti visą įrašo informaciją, kuri turi būti pateikta, galite nustatyti papildomų laukų. Papildomi laukai gali būti susieti su pranešimais ir pranešimų elementais. Papildomus laukus galite nustatyti puslapyje **Papildomi laukai** (**Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Papildomi laukai**).

Toliau pateiktoje lentelėje aprašomi puslapyje **Papildomi laukai** esantys bendrieji laukai.

| Laukas       | Aprašas |
|-------------|-------------|
| Lauko pavadinimas  | Įveskite su procesu susijusių pranešimo elementų papildomo atributo pavadinimą. Šis pavadinimas rodomas vartotojo sąsajoje vykdant procesą. Jį taip pat galima naudoti su procesu susijusiose ER konfigūracijose. |
| Aprašas | Įveskite papildomo lauko aprašą. |
| Vartotojo redaguojamas   | Šią parinktį nustatykite kaip **Taip**, jei vartotojai turi galėti vartotojo sąsajoje pakeisti papildomo lauko reikšmę. |
| Skaitiklis     | Šią parinktį nustatykite kaip **Taip**, jei papildomame elektroninio pranešimo lauke turi būti numeracija. Vykdant veiksmą **Elektroninių ataskaitų eksportavimas**, papildomo lauko reikšmė bus užpildyta automatiškai. |
| Paslėpta      | Šią parinktį nustatykite kaip **Taip**, jei papildomas laukas vartotojo sąsajoje turi būti paslėptas. |

Kiekviename papildomame lauke gali būti skirtingos reikšmės, kurias reikia apdoroti. Šios reikšmės nustatomos „FastTab“ konteineryje **Reikšmės**. Tolesnėje lentelėje aprašomi laukai.

| Laukas                | Aprašas |
|----------------------|-------------|
| Lauko vertė          | Įveskite lauko reikšmę, kurią naudosite su pranešimu arba pranešimo elementu teikdami ataskaitas. |
| Aprašas          | Įveskite lauko reikšmės aprašą. |
| Kodo tipas         | Kai kurios laukų reikšmės gali būti taikomos tik konkrečių tipų klientams. Pasirinkite vieną šių verčių: **Visi**, **Klientas** arba **Tiekėjas**. |
| Sąskaitos kodas         | Jei lauke **Kliento tipas** pasirinkote **Klientas** arba **Tiekėjas**, lauko reikšmės naudojimą galite dar labiau apriboti iki konkrečios grupės arba lentelės. |
| Sąskaitos/grupės Nr. | Jei pasirinkote **Klientas** arba **Tiekėjas** lauke **Sąskaitos tipas** ir įvedėte grupę arba lentelę lauke **Sąskaitos kodas**, šiame lauke galite įvesti konkrečią grupę arba sąveikos objektą. |
| Galioja            | Nurodykite datą, nuo kurios reikia atsižvelgti į vertę. |
| Galiojimo pabaiga           | Nurodykite datą, nuo kurios reikia nepaisyti vertės. |

Pagal numatytuosius parametrus kriterijų, kuriuos nustato laukai **Kliento / grupės numeris**, **Kliento kodas**, **Įsigalioja** ir **Galiojimo pabaiga**, kombinacijos neturi įtakos parenkant papildomų laukų reikšmes. Tačiau šias kombinacijas galima naudoti vykdomojoje klasėje siekiant įdiegti konkrečią logiką, apskaičiuojančią papildomų laukų reikšmes.

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

Kai kuriose vykdomosiose klasėse gali būti nustatyta privalomų parametrų, kuriuos reikia nurodyti prieš vykdant vykdomąją klasę pirmą kartą. Norėdami nustatyti šiuos parametrus, veiksmų srityje pasirinkite **Parametrai**, nustatykite pasirodžiusiame dialogo lange esančius laukus ir pasirinkite **Gerai**. Svarbu pasirinkti **Gerai**. Kitu atveju parametrai nebus įrašyti į duomenų bazę ir vykdomoji klasė nebus iškviečiama teisingai.

### <a name="populate-records-actions"></a>Automatinio įrašų įvedimo veiksmai

Naudojate veiksmus įrašams automatiškai įvesti, kuriuos reikia nustatyti įrašams prie pranešimo elementų lentelės pridėti, kad juos būtų galima įtraukti į elektroninį pranešimą. Pavyzdžiui, jei jūsų elektroninis pranešimas turi pranešti kliento sąskaitas faktūras, turite nustatyti automatinio įrašų užpildymo veiksmą, susietą su lentelės Kliento SF žurnalas lauku **Duomenų šaltinis**. Veiksmus įrašams automatiškai įvesti galite nustatyti puslapyje **Automatinio įrašų įvedimo veiksmas** (**Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Automatinio įrašų įvedimo veiksmai**). Sukurkite naują kiekvieno veiksmo, kuris turi pridėti įrašų prie lentelės, įrašą ir nustatykite toliau nurodytus laukus.

| Laukas       | Aprašas |
|-------------|-------------|
| Vardas        | Įveskite veiksmo, kuris jūsų proceso metu automatiškai užpildo įrašus, pavadinimą. |
| Aprašas | Įveskite automatinio įrašų užpildymo veiksmo aprašą. |

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
| Vartotojo užklausa             | Jei šis žymės langelis pažymėtas, galite nustatyti užklausą pasirinkdami virš tinklelio esantį lauką **Redaguoti užklausą**. Priešingu atveju visi įrašai bus užpildyti iš pasirinkto duomenų šaltinio. |

### <a name="web-applications"></a>Žiniatinklio programos

Naudodami žiniatinklio programų parametrus nustatote, kad žiniatinklio programa palaikytų „Open Authorization“ („OAuth“) 2.0. „OAuth“ yra atvirasis standartas, kurį naudodami vartotojai savo vardu programai gali suteikti „saugią suteiktąją prieigą“, nebendrindami prieigos kredencialų. Autorizavimo procesą taip pat galite atlikti gaudami autorizavimo kodą ir prieigos atpažinimo ženklą. Žiniatinklio programos parametrus galite nustatyti puslapyje **Žiniatinklio programos** (**Mokesčiai** \> **Sąranka** \> **Elektroniniai pranešimai** \> **Žiniatinklio programos**).

Toliau pateiktoje lentelėje aprašomi puslapio **Žiniatinklio programos** laukai.

| Laukas                        | Aprašas |
|------------------------------|-------------|
| Programos pavadinimas             | Įveskite žiniatinklio programos pavadinimą. |
| Aprašas                  | Įveskite žiniatinklio programos aprašą. |
| Pagrindinis URL                     | Įveskite žiniatinklio programos pagrindinį interneto adresą. |
| Autorizavimo URL kelias       | Nurodykite kelią, naudojamą autorizavimo URL sukurti. |
| Atpažinimo ženklo URL kelias               | Nurodykite kelią, naudojamą atpažinimo ženklo URL sukurti. |
| Nukreipimo URL                 | Įveskite nukreipimo URL. |
| Kliento ID                    | Įveskite žiniatinklio programos kliento ID. |
| Kliento paslaptis                | Įveskite žiniatinklio programos kliento paslaptį. |
| Serverio atpažinimo ženklas                 | Įveskite žiniatinklio programos atpažinimo ženklą. |
| Autorizavimo formato susiejimas | Pasirinkite ER formatą, naudojamą autorizavimo užklausai generuoti. |
| Importuoti atpažinimo ženklo modelio susiejimą   | Pasirinkite ER importavimo modelio susiejimą, naudojamą prieigos atpažinimo ženklui saugoti. |
| Suteikta apimtis                | Programai teikiamoms užklausoms suteikiama aprėptis. Šis laukas yra automatiškai atnaujinamas. |
| Prieigos atpažinimo ženklo galiojimo laikas baigiasi  | Likęs laikas iki prieigos atpažinimo ženklo galiojimo pabaigos. | 
| Priimti                       | Nurodykite žiniatinklio užklausos ypatybę **Priimti**. Pavyzdžiui, įveskite **application/vnd.hmrc.1.0+json**. |
| Turinio tipas                 | Nurodykite turinio tipą. Pavyzdžiui, įveskite **application/json**. |

Be to, autorizavimo procesui palaikyti puslapio **Žiniatinklio programos** veiksmų srityje pasiekiami tolesni mygtukai.

- **Gauti autorizavimo kodą** – inicijuoti žiniatinklio programos autorizavimą.
- **Gauti prieigos atpažinimo ženklą** – inicijuoti prieigos atpažinimo ženklo gavimo procesą.
- **Atnaujinti prieigos atpažinimo ženklą** – atnaujinti prieigos atpažinimo ženklą.

Kai prieigos prie žiniatinklio programos atpažinimo ženklas sistemos duomenų bazėje yra saugomas užšifruotu formatu, jį galima naudoti teikiant užklausas žiniatinklio tarnybai. Dėl saugos prieigą prie prieigos atpažinimo ženklo reikia skirti tik tiems saugos vaidmenims, kuriems būtina leisti tvarkyti tas užklausas. Jei tvarkyti užklausą bando ne saugos grupės vartotojai, jie gauna klaidą, kad jiems neleidžiama atlikti veiksmų pasirinktoje žiniatinklio programoje. Norėdami nustatyti saugos vaidmenis, kurie privalo turėti prieigą prie prieigos atpažinimo ženklo, naudokite puslapyje **Žiniatinklio programos** esantį „FastTab“ **Saugos vaidmenys**. Jei žiniatinklio programos saugos vaidmenų nenustatoma, šioje žiniatinklio programoje veiksmus gali atlikti tik sistemos administratorius.

### <a name="web-service-settings"></a>Žiniatinklio tarnybos parametrai

Naudojate žiniatinklio tarnybos parametrus tiesioginiam duomenų perdavimui į žiniatinklio tarnybą nustatyti. Žiniatinklio tarnybos parametrus galite nustatyti puslapyje **Žiniatinklio tarnybos parametrai** (**Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Žiniatinklio tarnybos parametrai**).

Toliau pateiktoje lentelėje aprašomi puslapio **Žiniatinklio tarnybos parametrai** laukai.

| Laukas                          | aprašymas |
|--------------------------------|-------------|
| Tinklo tarnyba                    | Įveskite žiniatinklio tarnybos pavadinimą. |
| aprašymas                    | Įveskite žiniatinklio tarnybos aprašą. |
| Interneto adresas               | Įveskite žiniatinklio tarnybos interneto adresą. Jei nurodyta žiniatinklio tarnybos žiniatinklio programa, o žiniatinklio tarnybos interneto adresas turi būti toks pats, kaip nustatytas tos žiniatinklio programos interneto adresas, pasirinkite **Kopijuoti pagrindinį URL**, kad į ši lauką nukopijuotumėte pagrindinį žiniatinklio programos URL. |
| Sertifikatas                    | Pasirinkite anksčiau nustatytą raktų saugyklos sertifikatą. |
| Žiniatinklio programa                | Pasirinkite anksčiau nustatytą raktų saugyklos sertifikatą. |
| Atsakymo tipas – XML        | Jei atsakymo tipas yra XML, nustatykite šią parinktį į **Taip**. |
| Užklausos metodas                 | Nurodykite užklausos metodą. HTTP apibrėžia užklausų metodų, nurodančių veiksmą, kuris turi būti atliekamas nurodytiems ištekliams, rinkinį. Užklausos metodas gali būti **GET**, **POST** arba kitas HTTP metodas. |
| Užklausų antraštės                | Nurodykite užklausų antraštes. Užklausos antraštė – tai HTTP antraštė, kuri gali būti naudojama HTTP užklausai ir kuri nesusijusi su pranešimo turiniu. |
| Priimti                         | Nurodykite žiniatinklio užklausos ypatybę **Priimti**. |
| Priimti kodavimą                | Nurodykite elemento **Priimti kodavimą** reikšmę. Priimtino kodavimo užklausos HTTP antraštėje skelbiamas turinio kodavimas, kurį klientas gali suprasti. Toks turinio kodavimas dažniausiai yra glaudinimo algoritmas. |
| Turinio tipas                   | Nurodykite turinio tipą. Turinio tipo objekto HTTP antraštė nurodo ištekliaus publikavimo kanalo tipą. |
| Sėkmingas atsakymo kodas       | Nurodykite HTTP būsenos kodą, nurodantį, kad užklausa įvykdyta sėkmingai. |
| Užklausos antraščių formato susiejimas | Pasirinkite ER formatą, naudojamą žiniatinklio užklausų antraštėms generuoti. |

### <a name="message-processing-actions"></a>Pranešimų apdorojimo veiksmai

Naudojate pranešimų apdorojimo veiksmus, kad sukurtumėte savo procesų veiksmus ir nustatytumėte jų parametrus. Pranešimų apdorojimo veiksmus galite nustatyti puslapyje **Pranešimų apdorojimo veiksmai** (**Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Pranešimų apdorojimo veiksmai**).

Toliau pateiktose lentelėse aprašomi puslapio **Pranešimų apdorojimo veiksmai** laukai.

#### <a name="general-fasttab"></a>Bendras „FastTab“ skirtukas

| Laukas                       | aprašymas |
|-----------------------------|-------------|
| Veiksmo tipas                 | Pasirinkite veiksmo tipą. Informacijos apie galimas parinktis žr. skyriuje [Pranešimų apdorojimo veiksmų tipai](#message-processing-action-types). |
| Formato susiejimas              | Pasirinkite ER formatą, kuris turi būti iškviestas veiksmui atlikti. Šis laukas galimas tik veiksmų tipams **Elektroninių ataskaitų eksportavimas**, **Elektroninių ataskaitų importavimas** ir **Elektroninių ataskaitų eksportavimo pranešimas**. |
| URL kelio formato susiejimas | Pasirinkite ER formatą, kuris turi būti iškviestas veiksmui atlikti. Šis laukas taikomas tik tipo **Žiniatinklio tarnyba** veiksmams. Jis naudojamas kuriant URL adreso kelią, kuris bus įtrauktas į nurodytą pagrindinį pasirinkto žiniatinklio serverio interneto adresą. |
| Pranešimo prekės tipas           | Pasirinkite įrašų, kurių veiksmą reikia įvertinti, tipą. Šis laukas taikomas veiksmų tipams **Pranešimo elemento vykdymo lygis**, **Elektroninių ataskaitų eksportavimas**, **Elektroninių ataskaitų importavimas** ir **Žiniatinklio tarnyba** bei kai kuriems kitiems tipams. Jei šį lauką paliksite tuščią, bus vertinami visi pranešimų apdorojimui apibrėžti pranešimų elementų tipai. |
| Vykdomoji klasė            | Pasirinkite anksčiau sukurtus vykdomosios klasės parametrus. Šis laukas galimas tik veiksmų tipams **Pranešimo elemento vykdymo lygis** ir **Pranešimo elemento vykdymo lygis**. |
| Automatinio įrašų įvedimo veiksmas     | Pasirinkite anksčiau nustatytą automatinio įrašų įvedimo veiksmą. Šis laukas galimas tik veiksmų tipui **Automatiškai įvesti įrašus**. |
| Tinklo tarnyba                 | Pasirinkite pirmiau nustatytą žiniatinklio tarnybą. Šis laukas taikomas tik tipo **Žiniatinklio tarnyba** veiksmams. |
| Failo vardas                   | Nurodykite failo, kuris bus veiksmo rezultatas, pavadinimą. Šis failas gali būti atsakas iš žiniatinklio serverio arba generuojama ataskaita. Šis laukas taikomas tik tipų **Žiniatinklio tarnyba** ir **Elektroninių ataskaitų eksportavimo pranešimas** veiksmams. |
| Rodyti dialogo langą                 | Šią parinktį nustatykite kaip **Taip**, jei prieš ataskaitos generavimą vartotojams turi būti rodomas dialogo langas. Šis laukas taikomas tik tipo **Elektroninių ataskaitų eksportavimo pranešimas** veiksmams. |

##### <a name="message-processing-action-types"></a>Pranešimų apdorojimo veiksmų tipai

Galimos toliau nurodytos lauko **Veiksmo tipas** parinktys.

- **Kurti pranešimą** – naudokite šį veiksmo tipą, kad vartotojai galėtų rankiniu būdu kurti pranešimus puslapyje **Elektroninis pranešimas**. Šio tipo veiksmui negalima nustatyti pradinės būsenos.
- **Automatiškai užpildyti įrašus** – anksčiau turi būti nustatytas tipo **Automatiškai užpildyti įrašus** veiksmas. Šį veiksmo tipą susiekite su automatinio įrašų užpildymo veiksmu, kad tą veiksmą būtų galima įtraukti į apdorojimą. Daroma prielaida, kad šis veiksmo tipas naudojamas atliekant pirmą pranešimo apdorojimo veiksmą (kai iš anksto elektroninių pranešimų nebuvo sukurta) ar kaip veiksmas, kuriuo pranešimo elementai įtraukiami į anksčiau sukurtą pranešimą (tipo **Kurti pranešimą** veiksmu). Todėl, naudojant šio tipo veiksmus, galima nustatyti tik pranešimo elementų rezultatų būseną. Pradinę būseną galima nustatyti tik pranešimams.
- **Pranešimo vykdymo lygis** – šį veiksmo tipą naudokite vykdomajai klasei, kuri turi būti įvertinta pranešimo lygiu, nustatyti.
- **Pranešimo elemento vykdymo lygis** – šį veiksmo tipą naudokite vykdomajai klasei, kuri turi būti įvertinta pranešimo elemento lygiu, nustatyti.
- **Elektroninių ataskaitų eksportavimas** – šį veiksmo tipą naudokite veiksmams, kuriais turi būti generuojama ataskaita, grindžiama ER eksportavimo konfigūracija pranešimo elemento lygiu.
- **Elektroninių ataskaitų eksportavimo pranešimas** – šį veiksmo tipą naudokite veiksmams, kuriais turi būti generuojama ataskaita, grindžiama ER eksportavimo konfigūracija pranešimo lygiu (pavyzdžiui, kai pranešimas neturi jokių pranešimo elementų).
- **Elektroninių ataskaitų importavimas** – šį veiksmo tipą naudokite veiksmams, kuriais turi būti generuojama ataskaita, grindžiama ER importavimo konfigūracija.
- **Pranešimų lygio vartotojų apdorojimas** – šį veiksmo tipą naudokite veiksmams, kuriais nurodomas tam tikras rankinis vartotojo veiksmas pranešimų lygiu. Pavyzdžiui, vartotojas gali atnaujinti pranešimų būseną.
- **Vartotojų apdorojimas** – šį veiksmo tipą naudokite veiksmams, kuriais nurodomas tam tikras rankinis vartotojo veiksmas pranešimų elementų lygiu. Pavyzdžiui, vartotojas gali atnaujinti pranešimų elementų būseną.
- **Žiniatinklio tarnyba** – šį veiksmo tipą naudokite veiksmams, kuriais sugeneruota ataskaita turi būti perduodama žiniatinklio tarnybai. Šis veiksmo tipas nenaudojamas Italijos pirkimo ir pardavimo sąskaitų faktūrų ryšių ataskaitoms teikti. Jei veiksmų tipas yra **Žiniatinklio tarnyba**, puslapyje **Pranešimų apdorojimo veiksmai** yra „FastTab“ **Įvairi informacija**, kuriame galite nurodyti patvirtinimo tekstą. Šis patvirtinimo tekstas bus rodomas vartotojams prieš apdorojant pasirinktai žiniatinklio tarnybai pateiktas užklausas.
- **Užklausos tikrinimas** – šį veiksmo tipą naudokite tikrinimui iš serverio prašyti.

#### <a name="initial-statuses-fasttab"></a>Pradinių būsenų „FastTab“

> [!NOTE]
> „FastTab“ **Pradinės būsenos** nepasiekiamas, kai veiksmų pradinis veiksmo tipas yra **Kurti pranešimą**.

| Laukas               | Aprašas |
|---------------------|-------------|
| Pranešimo prekės būsena | Pasirinkite pranešimo elemento būseną, pagal kurią turi būti įvertintas pasirinkto pranešimo apdorojimo veiksmas. |
| aprašymas         | Pasirinkto pranešimo elemento būsenos aprašas. |

#### <a name="result-statuses-fasttab"></a>Galutinių būsenų „FastTab“

| Laukas               | aprašymas |
|---------------------|-------------|
| Pranešimo būsena      | Pasirinkite pranešimų būsenas, pagal kurias turi būti įvertintas pasirinkto pranešimo apdorojimo veiksmas. Šis laukas galimas tik pranešimų apdorojimo veiksmams, kurie vertinami pranešimo lygiu. Pavyzdžiui, jis pasiekiamas, kai veiksmų tipas yra **Elektroninių ataskaitų eksportavimas** ir **Elektroninių ataskaitų importavimas**, bet nepasiekiamas, kai veiksmų tipas yra **Vartotojų apdorojimas** ir **Pranešimo elemento vykdymo lygis**. |
| aprašymas         | Pasirinkto pranešimo būsenos aprašas. |
| Atsiliepimo tipas       | Pasirinkto pranešimo būsenos atsakymo tipas. |
| Pranešimo prekės būsena | Pasirinkite rodomas būsenas, kurios turi būti prieinamos įvertinus pasirinkto pranešimo apdorojimo veiksmą. Šis laukas galimas tik pranešimų apdorojimo veiksmams, kurie vertinami pranešimo elemento lygiu. Pavyzdžiui, jis galimas veiksmų tipams **Vartotojų apdorojimas** ir **Pranešimo elemento vykdymo lygis**. Šiame lauke pranešimų apdorojimo veiksmams, įvertintiems pranešimo lygiu, rodoma pranešimo elemento būsena, kuri buvo nustatyta pasirinkto pranešimo būsenai. |

Toliau pateikiamoje lentelėje rodomos rezultatų būsenos, kurias reikia nustatyti skirtingiems veiksmų tipams ir atsakų tipams.

| Elelktroninio pranešimo veiksmo tipas / atsako tipas | Sėkmingai įvykdyta | Darbo klaida | Techninė klaida | Vartotojo nustatyta | Atšaukti |
|----------------------------------------------|-----------------------|----------------|-----------------|--------------|--------|
| Kurti pranešimą                               | X                     |                |                 |              |        |
| Elektroninių ataskaitų eksportavimas                  | X                     |                |                 |              |        |
| Elektroninių ataskaitų importavimas                  |                       |                |                 |              |        |
| Tinklo tarnyba                                  | X                     |                | X               |              |        |
| Vartotojo apdorojamas                              |                       |                |                 |              |        |
| Pranešimo vykdymo lygis                      |                       |                |                 |              |        |
| Automatiškai įvesti įrašus                             |                       |                |                 |              |        |
| Pranešimo prekės vykdymo lygis                 |                       |                |                 |              |        |
| Užklausos tikrinimas                         | X                     | X              | X               |              |        |
| Elektroninių ataskaitų eksportavimo pranešimas          | X                     |                |                 |              |        |
| Pranešimų lygio vartotojų apdorojimas                |                       |                |                 |              |        |

### <a name="electronic-message-processing"></a>El. pranešimų apdorojimas

Elektroninių pranešimų apdorojimas yra pagrindinė elektroninių pranešimų funkcionalumo koncepcija. Ji sujungia veiksmus, kuriais turi būti įvertintas elektroninis pranešimas. Veiksmus galima susieti naudojant pradinę būseną ir rezultatų būseną. Arba veiksmus, kurių tipas **Vartotojų apdorojimas**, galima pradėti savarankiškai. Puslapyje **Elektroninių pranešimų apdorojimas** (**Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Elektroninių pranešimų apdorojimas**) taip pat galite pasirinkti papildomus laukus, kurie turi būti palaikomi apdorojant pranešimo lygiu arba pranešimo elementų lygiu.

„FastTab“ skirtuke **Veiksmas** galima pridėti iš anksto apibrėžtų veiksmų apdorojimui. Galite nurodyti, ar veiksmą reikia vykdyti atskirai, ar jį galima pradėti apdorojant. Norėdami nurodyti, kad apdorojamą veiksmą gali inicijuoti tik vartotojas, to veiksmo lauką **Vykdyti atskirai** nustatykite kaip **Taip**. Jei veiksmas turi būti pradedamas apdorojant pranešimus arba pranešimų elementus, kurie yra tokios būsenos, kokia nustatyta kaip pradinė to veiksmo būsena, lauką **Vykdyti atskirai** nustatykite kaip **Ne**. Tipo **Vartotojo veiksmas** veiksmus visada reikia vykdyti atskirai.

Kartais kelis veiksmus reikia sujungti į seką, net jei pirmasis veiksmas yra nustatytas būti vykdomas atskirai. Pavyzdžiui, vartotojas turi inicijuoti ataskaitos generavimą, tačiau iš karto po ataskaitos sugeneravimo ją reikia siųsti į žiniatinklio tarnybą, o žiniatinklio tarnybos atsakas turi būti nurodytas sistemoje. Šioje situacijoje galite sukurti neatskiriamą veiksmų, kurie visada turi būti vykdomi kartu, seką. „FastTab“ konteineryje **Veiksmas** virš tinklelio pasirinkite **Neatskiriamos sekos** ir sukurkite seką. Tada lauke **Neatskiriama seka** pasirinkite visų veiksmų, kuriuos reikia vykdyti kartu, seką. Šiuo atveju pirmam sekos veiksmui lauką **Vykdyti atskirai** galima nustatyti kaip **Taip**, tačiau visiems kitiems veiksmams – **Ne**.

„FastTab“ skirtuke **Pranešimo elemento papildomi laukai** galima pridėti iš anksto apibrėžtų papildomų laukų, susijusių su pranešimo elementais. Turite pridėti papildomų laukų kiekvienam pranešimo elemento, su kuriuo susiję laukai, tipui.

„FastTab“ skirtuke **Pranešimo papildomi laukai** galima pridėti iš anksto apibrėžtų papildomų laukų, susijusių su pranešimais.

„FastTab“ skirtuke **Saugos vaidmenys** galima nustatyti saugos vaidmenis, iš anksto apibrėžtus sistemoje konkrečiam apdorojimui. Vartotojai, turintys konkretų vaidmenį, matys tik tam vaidmeniui apibrėžtą apdorojimą.

„FastTab“ skirtuke **Paketas** galima nustatyti apdorojimą dirbti paketiniu režimu.

## <a name="work-with-the-electronic-messages-functionality"></a>Darbas su elektroninių pranešimų funkcija

Jei dirbate pranešimo lygiu, puslapis **Elektroniniai pranešimai** (**Mokesčiai** \> **Užklausos ir ataskaitos** \> **Elektroniniai pranešimai** \> **Elektroniniai pranešimai**) bus naudingesnis. Jei dirbate duomenų rinkinio (pranešimo elemento) lygiu, puslapis **Elektroninio pranešimo elementai** (**Mokesčiai** \> **Užklausos ir ataskaitos** \> **Elektroniniai pranešimai** \> **Elektroninio pranešimo elementai**) bus naudingesnis.

### <a name="electronic-messages"></a>El. pranešimai

Puslapyje **Elektroniniai pranešimai** pateikiamas jums prieinamas apdorojimas pagal jūsų vaidmenį. Saugos vaidmenys yra susieti su apdorojimu nustatant šį apdorojimą. Kiekvienam jums prieinamam apdorojimui puslapyje pateikiami elektroniniai pranešimai ir su jais susijusi informacija.

„FastTab“ skirtuke **Pranešimai** rodomi pasirinkto apdorojimo elektroniniai pranešimai. Kai kuriuos veiksmus galite vykdyti naudodami toliau nurodytus virš tinklelio esančius mygtukus – tai priklauso nuo pasirinkto pranešimo būsenos ir iš anksto nustatyto apdorojimo.

- **Naujas** – šis mygtukas susietas su veiksmų tipu **Kurti pranešimą**.
- **Naikinti** – šį mygtuką galima naudoti, jei pažymėtas žymės langelis **Leisti naikinti**, skirtas pasirinkto pranešimo dabartinei būsenai.
- **Surinkti duomenis** – šis mygtukas susietas su tipo **Automatiškai įvesti įrašus** veiksmais.
- **Generuoti ataskaitą** – šis mygtukas susietas su veiksmų tipu **Elektroninių ataskaitų eksportavimo pranešimas**.
- **Siųsti ataskaitą** – šis mygtukas susietas su veiksmų tipu **Žiniatinklio tarnyba**.
- **Importuoti atsaką** – šis mygtukas susietas su tipo **Elektroninių ataskaitų importavimas** veiksmais.
- **Atnaujinti būseną** – šis mygtukas susietas su veiksmų tipu **Pranešimų lygio vartotojų apdorojimas**.
- **Pranešimo elementai** – atidaromas puslapis **Elektroninio pranešimo elementai**.

„FastTab“ skirtuke **Veiksmų žurnalas** rodoma informacija apie visus veiksmus, kurie buvo vykdomi pasirinktam pranešimui. Jei dėl veiksmo įvyko klaida, informacija apie klaidą pridedama prie susijusios tinklelio eilutės. Norėdami peržiūrėti informaciją apie klaidą, pasirinkite tinklelio eilutę, tada – viršutiniame dešiniajame puslapio kampe esantį mygtuką **Priedas** (sąvaržėlės simbolis).

„FastTab“ skirtuke **Pranešimo papildomi laukai** rodomi visi papildomi laukai, kuriais apibrėžiami pranešimai nustatant apdorojimą. Jame taip pat rodomos tų papildomų laukų vertės.

„FastTab“ skirtuke **Pranešimo elementai** rodomi visi su pasirinktu pranešimu susiję pranešimo elementai. Kai kuriuos veiksmus galite vykdyti naudodami toliau nurodytus virš tinklelio esančius mygtukus – tai priklauso nuo pasirinkto pranešimo elemento būsenos.

- **Naikinti** – šį mygtuką galima naudoti, jei pažymėtas žymės langelis **Leisti naikinti**, skirtas pasirinkto pranešimo elemento dabartinei būsenai.
- **Atnaujinti būseną** – šis mygtukas susietas su veiksmų tipu **Vartotojų apdorojimas**.
- **Pradinis dokumentas** – atidaromas puslapis, kuriame rodomas pradinis pasirinkto pranešimo elemento dokumentas.

Visos sugeneruotos ir gautos pranešimo ataskaitos yra pridedamos prie to pranešimo. Norėdami peržiūrėti su pranešimu susijusius priedus, pasirinkite pranešimą, tada – viršutiniame dešiniajame puslapio kampe esantį mygtuką **Priedas** (sąvaržėlės simbolis).

![Priedo mygtukas](media/attachment-icon.png)

Puslapyje **Priedai** rodomi visi su pasirinktu pranešimu susiję priedai. Norėdami peržiūrėti failą, pasirinkite jį iš sąrašo kairėje, tada veiksmų srityje pasirinkite **Atidaryti**.

![Mygtukas Atidaryti](media/open-button.png)

Taip pat galite peržiūrėti priedus, susijusius su konkrečiu anksčiau vykdytu pranešimo veiksmu. Puslapio **Elektroniniai pranešimai** „FastTab“ konteinerio **Pranešimai** „FastTab“ konteineryje **Veiksmų žurnalas** pasirinkite pranešimą, tada – viršutiniame dešiniajame puslapio kampe esantį mygtuką **Priedas**.

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
<td>Kliento arba tiekėjo kliento numeris (arba kita lauko reikšmė – tai priklauso nuo lauko, kuriuo apibrėžtas automatinio įrašų įvedimo veiksmas). Šis laukas gali būti automatiškai užpildytas tik tada, kai sąskaita faktūra įtraukiama į pranešimo elementų lentelę.</td>
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
<td>Tolesni veiksmai, kuriuos galima pradėti, kai pranešimo elementas yra dabartinės būsenos.</td>
</tr>
</tbody>
</table>

Skirtuke **Papildomi laukai** rodomi papildomi pasirinkto pranešimo elemento laukai ir jų vertės.

#### <a name="run-processing"></a>Vykdyti apdorojimą

Veiksmų srityje pasirinkite **Vykdyti apdorojimą** pranešimo elementų apdorojimui vykdyti. Norėdami vykdyti konkretų veiksmą, dialogo lange **Vykdyti apdorojimą** parinktį **Pasirinkti veiksmą** nustatykite kaip **Taip**, tada pasirinkite veiksmą. Norėdami vykdyti visą apdorojimą, parinktį **Pasirinkti veiksmą** palikite nustatytą kaip **Ne**.

#### <a name="generate-report"></a>Generuoti ataskaitą

Norėdami sugeneruoti ataskaitą, veiksmų srityje pasirinkite **Generuoti ataskaitą**. Šis mygtukas susietas su veiksmų tipu **Elektroninių ataskaitų eksportavimas**.

#### <a name="update-status"></a>Atnaujinti būseną

Norėdami atnaujinti vieno ar daugiau pranešimo elementų būseną, veiksmų srityje pasirinkite **Atnaujinti būseną**. Norėdami pasirinkti naujintinus pranešimo elementus, dialogo lange **Atnaujinti būseną** naudokite „FastTab“ **Įtrauktini įrašai**. Įsitikinkite, kad teisingai apibrėžiate pasirinkimo kriterijus, nes pranešimų elementų būsenos atnaujinamos pagal šiuos kriterijus, pradinę pasirinkto veiksmo būseną ir reikšmę **Nauja būsena**, kurią nurodote. Baigus būsenos atnaujinimą bus sunku nustatyti, kurie elementai buvo atnaujinti. Todėl bus sunku atšaukti būsenos naujinimą.

#### <a name="electronic-messages"></a>El. pranešimai

Norėdami peržiūrėti elektroninį pranešimą, susijusį su pasirinktu pranešimo elementu, veiksmų srityje pasirinkite **Elektroniniai pranešimai**.

Taip pat galite peržiūrėti visus failus, susijusius su konkrečiu pranešimo elementu. Pasirinkite pranešimo elemento lauką **Pranešimas** arba veiksmų srityje pasirinkite **Elektroniniai pranešimai**. Tada puslapyje **Elektroninis pranešimas** pasirinkite pranešimą, kurio failus norite peržiūrėti, tada pasirinkite viršutiniame dešiniajame puslapio kampe esantį mygtuką **Priedas** (sąvaržėlės simbolis).

![Priedo mygtukas](media/attachment-icon.png)

Puslapyje **Priedai** rodomi visi su pranešimu susiję priedai. Norėdami peržiūrėti failą, pasirinkite jį iš sąrašo kairėje, tada veiksmų srityje pasirinkite **Atidaryti**.

![Mygtukas Atidaryti](media/open-button.png)

#### <a name="original-document"></a>Originalus dokumentas

Norėdami atidaryti pasirinkto pranešimo elemento originalų dokumentą, veiksmų srityje pasirinkite **Originalus dokumentas**.

## <a name="example-set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Pavyzdys. Apdorojimo nustatymas ir vykdymas norint iškviesti paprastą ER eksportavimo formatą „Excel“ ataskaitai sugeneruoti

Sukūrę savo ER formatą, susieję jį su duomenų šaltiniais ir užbaigę, galite paleisti jį naudodami darbo sritį **Elektroninės ataskaitos**. Sugeneruojama ataskaita, kurią galite įrašyti vietoje.

Norėdami kontroliuoti šiuos ataskaitų teikimo proceso aspektus, turite nustatyti elektroninių pranešimų apdorojimą.

- Užregistruokite informaciją apie tai, kas sugeneravo ataskaitą.
- Užregistruokite informaciją apie tai, kada ataskaita buvo sugeneruota.
- Įrašykite ankstesnių laikotarpių sugeneruotas ataskaitas.

Šiame skyriuje pateikiamas pavyzdys, rodantis, kaip galite nustatyti elektroninius pranešimus ataskaitai, kuri pagrįsta „Excel“ ER eksportavimo formatu, generuoti. Jei norite vadovautis šiuo pavyzdžiu, „Excel“ ER eksportavimo formatas jau turi būti sukurtas, susietas su duomenų šaltiniais ir užbaigtas. Be to, jau turi būti nustatyta elektroninių pranešimų numeracija.

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
    - „FastTab“ konteineryje **Rezultatų būsenos** įtraukite atskirą eilutę kiekvienai iš dviejų pranešimo būsenų (**Paruoštas** ir **Naujas**). Abiejose eilutėse lauką **Atsako tipas** nustatykite kaip **Sėkmingai įvykdytas**.

#### <a name="electronic-message-processing"></a>El. pranešimų apdorojimas

Šiame pavyzdyje visi veiksmai turi būti nustatyti taip, kad jie būtų vykdomi atskirai. Daroma prielaida, kad kiekvieną veiksmą inicijuos vartotojas.

1. Eikite į **Mokesčiai \> Nustatymas \> Elektroniniai pranešimai \> Elektroninių pranešimų apdorojimas**.
2. Prie savo apdorojimo pridėkite įrašą ir įtraukite visus anksčiau apibrėžtus veiksmus bei papildomą lauką.
3. Pasirinktinai. „FastTab“ konteineryje **Saugos vaidmenys** apibrėžkite savo apdorojimo saugos vaidmenis, kad apribotumėte prieigą prie konkrečių ataskaitų.
4. Eikite į **Mokesčiai \> Užklausos ir ataskaitos \> Elektroniniai pranešimai \> Elektroniniai pranešimai**.
5. Pasirinkite **Naujas** pranešimui sukurti. Šiuo metu galite pridėti datas ir aprašą. Taip pat galite atnaujinti papildomo lauko vertę, kaip jums reikia.

    ![Kurti elektroninį pranešimą](media/create-electronic-message.png)

„FastTab“ skirtuke **Veiksmų žurnalas** esančiame tinklelyje automatiškai užpildomas visų pranešime atliekamų veiksmų žurnalas.

Dabar galite panaikinti arba atnaujinti pranešimo būseną. Norėdami atnaujinti pranešimo būseną, pasirinkite **Atnaujinti būseną**. Lauke **Nauja būsena** pasirinkite **Paruoštas**, tada – **Gerai**.

![Atnaujinti pranešimo būseną](media/update-status.png)

Pranešimo būsena atnaujinta į **Parengta** ir dabar galite generuoti ataskaitą pasirinkdami **Generuoti ataskaitą**. Ataskaita sugeneruota, o pranešimo būsena ir veiksmų žurnalas atnaujinti. Norėdami peržiūrėti sugeneruotą ataskaitą, pasirinkite viršutiniame dešiniajame puslapio kampe esantį mygtuką **Priedas** (sąvaržėlės simbolis).
