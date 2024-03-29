---
title: Elektroninių pranešimų sąranka
description: Šiame straipsnyje pateikiama informacija apie tai, kaip nustatyti elektroninių pranešimų (EM) funkciją.
author: AdamTrukawka
ms.date: 11/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-06-23
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 12beb1adbfa4e2f235c8a7c69e786d342c4a4f68
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279309"
---
# <a name="set-up-electronic-messages"></a>Elektroninių pranešimų sąranka

[!include [banner](../includes/banner.md)]

**Elektroninių pranešimų** (EM) funkcija padeda jums tvarkyti skirtingų dokumentų tipų skirtingus elektroninių ataskaitų procesus. Taikant kai kuriuos sudėtingus scenarijus, palaikančius [ataskaitos funkcijas pagal šalį](electronic-messaging.md#country-specific-regulatory-features-supported-by-the-em-functionality), EM funkcija yra nustatyta taip, kad ji turėtų daug pranešimo būsenų, pranešimo elementų būsenų, veiksmų, papildomų laukų bei vykdomųjų klasių kombinacijų. Galima importuoti šių scenarijų duomenų objektų paketus. Jei naudojate šiuos duomenų objektų paketus, importuokite juos į juridinį subjektą naudodami duomenų valdymo įrankį. Daugiau informacijos apie tai, kaip naudoti duomenų valdymo įrankį, žr. [Duomenų valdymas](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

Jei neimportuojate duomenų objekto paketo, galite rankiniu būdu nustatyti EM funkciją. Tokiu atveju turite nustatyti toliau nurodytus elementus.

- [Numeracija](#sequences)
- [Pranešimo prekių tipai](#types)
- [Pranešimo prekių būsenos](#item)
- [Pranešimo būsenos](#statuses)
- [Papildomi laukai](#additional)
- [Vykdomosios klasės parametrai](#executable)
- [Automatinio įrašų įvedimo veiksmai](#populate)
- [Automatiškai įvesti įrašus iš kelių įmonių](#multiple-companies-populate)
- [Žiniatinklio programos](#applications)
- [Žiniatinklio tarnybos parametrai](#settings)
- [Pranešimų apdorojimo veiksmai](#actions)
- [El. pranešimų apdorojimas](#processing)

Tolesniuose skyriuose pateikiama daugiau informacijos apie šiuos elementus.

## <a name="number-sequences"></a><a id="sequences"></a>Numeravimai

Nustatykite pranešimų ir pranešimų elementų numeracijas. Tada numeracijos naudojamos automatiškai numeruoti pranešimams ir pranešimų elementams. Priskirti numeriai sistemoje yra naudojami kaip unikalūs pranešimų ir pranešimų elementų identifikatoriai. Elektroninių pranešimų numeracijas galite nustatyti eidami į **Didžioji knyga** \> **Didžiosios knygos nustatymai** \> **Didžiosios knygos parametrai**.

## <a name="message-item-types"></a><a id="types"></a>Pranešimo prekių tipai

Pranešimų elementų tipai nurodo įrašų, kurie yra naudojami elektroniniuose pranešimuose, tipus. Galite nustatyti pranešimo elementų tipus eidami į **Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Pranešimo elementų tipai**.

## <a name="message-item-statuses"></a><a id="item"></a>Pranešimo prekių būsenos

Pranešimų elementų būsenos nurodo būsenas, kurios taikomos jūsų nustatomam pranešimo elementų apdorojimui. Galite nustatyti pranešimo elementų būsenas eidami į **Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Pranešimo elementų būsenos**.

Pranešimo elemento būsenos parametras **Leisti naikinti** nurodo, ar jūs galite panaikinti pranešimų elementus, kurie turi nšią būseną puslapyje **Elektroniniai pranešimai** arba **Elektroninių pranešimų elementai**.

## <a name="message-statuses"></a><a id="statuses"></a>Pranešimo būsenos

Nustatykite pranešimo būsenas, kurios turi būti prieinamos pranešimui apdoroti. Galite nustatyti pranešimo būsenas eidami į **Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Pranešimo būsenos**.

Toliau pateiktoje lentelėje aprašomi puslapio **Pranešimų būsenos** laukai.

| Lauko pavadinimas          | Aprašas |
|---------------------|-------------|
| Pranešimo būsena      | Įveskite unikalų pranešimo būsenos pavadinimą. Pranešimų būsenos naudojamos apibūdinti, kokia yra elektroninio laiško būsena kiekvieną akimirką. Jūsų įvedamas pavadinimas rodomas puslapyje **Elektroniniai pranešimai** ir su elektroniniais pranešimais susijusiame žurnale. |
| Aprašas         | Įveskite pranešimo būsenos aprašą. |
| Atsakymo tipas       | Pasirinkit atsako tipą pranešimo būsenai. Atlikus kai kuriuos apdorojimo veiksmus gali būti pateiktas daugiau nei vienas atsako tipas. Pavyzdžiui, tipo **Žiniatinklio tarnyba** veiksmas gali pateikti **Sėkmingai įvykdytas** arba **Techninė klaida** tipų atsakus – tai priklauso nuo vykdymo rezultato. Šiuo atveju nurodykite pranešimų būseną abiems atsako tipams. Daugiau informacijos apie veiksmų tipus ir su jais susijusių atsakymų tipus rasite [šio](#action-types) straipsnio skyriuje Pranešimo apdorojimo veiksmų tipai. |
| Pranešimo prekės būsena | Kartais elektroninio pranešimo būsena turi paveikti susijusių pranešimo elementų būseną. Šiame lauke pasirinkite pranešimo elemento būseną, kad ją susietumėte su pranešimo būsena. |
| Leisti naikinti        | Pasirinkite šį žymės langelį, jei vartotojai turi galėti panaikinti elektroninius pranešimus, kurie turi šią būseną puslapyje **Elektroniniai pranešimai**. |

## <a name="additional-fields"></a><a id="additional"></a>Papildomi laukai

EM funkcija leidžia rinkti įrašus iš operacijų Microsoft Dynamics lentelių 365 finansų kaip pranešimų elementai. Tokiu būdu galite ataskaitoms parengti įrašus, o paskui juos pateikti. Tačiau kartais operacijų lentelėse nepakanka informacijos, kad įrašus būtų galima užpildyti pagal ataskaitų reikalavimus. Norėdami užpildyti visą įrašo informaciją, kuri turi būti pateikta, galite nustatyti papildomų laukų. Papildomus laukus galima susieti su pranešimais ir pranešimų elementais. Galite nustatyti papildomus laukus eidami į **Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Papildomi laukai**.

Toliau pateiktoje lentelėje aprašomi puslapyje **Papildomi laukai** esantys bendrieji laukai.

| Laukas       | Aprašas |
|-------------|-------------|
| Lauko pavadinimas  | Įveskite su procesu susijusių elektroninių pranešimų arba pranešimo elementų papildomo atributo pavadinimą. Šis pavadinimas rodomas vartotojo sąsajoje vykdant procesą. Pavadinimą taip pat galima naudoti su procesu susijusiose Elektroninių ataskaitų (ER) konfigūracijose. |
| Aprašas | Įveskite papildomo lauko aprašą. |
| Vartotojo redaguojamas   | Šią parinktį nustatykite kaip **Taip**, jei vartotojai turėtų galėti pakeisti papildomo lauko reikšmę vartotojo sąsajoje. |
| Skaitiklis     | Šią parinktį nustatykite kaip **Taip**, jei papildomame elektroninio pranešimo lauke turi būti numeracija. Vykdant veiksmą **Elektroninių ataskaitų eksportavimas**, papildomo lauko reikšmė yra užpildoma automatiškai. |
| Paslėpta      | Nustatykite šią pasirinktį į **Taip**, jei papildomas laukas turėtų būti paslėptas vartotojo sąsajos **Elektroninių pranešimų** arba **Elektroninių pranešimų elementų** puslapiuose. |

„FastTab” skirtuke **Reikšmės** galite iš anksto nustatyti reikšmes, kurias gali turėti papildomas laukas. Tada šias reikšmes gali pasirinkti vartotojai. Todėl apdorojimo metu jų nereikia užpildyti rankiniu būdu. Tolesnėje lentelėje aprašomi laukai.

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

## <a name="executable-class-settings"></a><a id="executable"></a>Vykdomosios klasės parametrai

Vykdomoji klasė – tai X++ metodas arba klasė, kurią elektroninių pranešimų apdorojimo procesas gali iškviesti pagal veiksmą, jei šiam procesui reikalingas tam tikras įvertinimas.

Galite rankiniu būdu nustatyti vykdomąjį klasę, kurią reikia iškviesti apdorojimu metu, eidami į **Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Vykdomosios klasės parametrai**. Puslapyje **Vykdomosios klasės parametrai** sukurkite eilutę ir nustatykite šiuos laukus.

| Laukas                 | Aprašas |
|-----------------------|-------------|
| Vykdomoji klasė      | Įveskite pavadinimą, kuris bus naudojamas nustatant pranešimo apdorojimo veiksmą, su kuriuo susieta ši iškviečiama klasė. |
| aprašymas           | Įveskite vykdomosios klasės aprašą. |
| Vykdomosios klasės pavadinimas | Pasirinkite X++ vykdomąją klasę. |
| Vykdymo lygis       | Šis laukas yra nustatomas automatiškai, nes pasirinktos vykdomosios klasės vertė yra nustatyta iš anksto. Šis laukas apriboja vykdomo susijusio įvertinimo lygį. |
| Klasės aprašymas     | Šis laukas yra nustatomas automatiškai, nes pasirinktos vykdomosios klasės vertė yra nustatyta iš anksto. |
| Veiksmo tipas           | Šis laukas yra galimas, kai **\[„EM”\] Vykdomosios klasės veiksmo tipo** funkcija yra įjungta **Funkcijų valdymo** darbo srityje. Naudokite šį lauką norėdami nurodyti vykdomosios klasės veiksmo tipą. Šis laukas leidžia tiksliau valdyti kitus veiksmus, kurie galimi elektroniniam pranešimui puslapyje **Elektroniniai pranešimai**. |

Kai kuriose vykdomosiose klasėse gali būti nustatyta privalomų parametrų, kuriuos reikia nurodyti prieš vykdant vykdomąją klasę pirmą kartą. Norėdami nustatyti šiuos parametrus, veiksmų srityje pasirinkite **Parametrai**. Pasirodžiusiame dialogo lange nustatykite laukus ir tada pasirinkite **Gerai**. Svarbu pasirinkti **Gerai**. Kitu atveju parametrai nebus įrašyti į duomenų bazę ir vykdomoji klasė nebus iškviečiama teisingai.

## <a name="populate-records-actions"></a><a id="populate"></a>Automatinio įrašų įvedimo veiksmai

Naudojate veiksmus įrašams automatiškai įvesti, kuriuos reikia nustatyti įrašams prie pranešimo elementų lentelės pridėti tam, kad juos būtų galima įtraukti į elektroninį pranešimą. Pavyzdžiui, jei jūsų elektroninis pranešimas turi pranešti kliento sąskaitas faktūras, turite nustatyti automatinio įrašų užpildymo veiksmą, susietą su lentelės Kliento SF žurnalas lauku **Duomenų šaltinis**.

Galite nustatyti automatinio įrašų užpildymo veiksmus eidami į **Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Automatinio įrašų užpildymo veiksmai**. Sukurkite naują kiekvieno veiksmo, kuris turi pridėti įrašų prie lentelės, įrašą ir nustatykite toliau nurodytus laukus.

| Laukas       | Aprašas |
|-------------|-------------|
| Vardas        | Įveskite veiksmo, kuris jūsų proceso metu automatiškai užpildo įrašus, pavadinimą. |
| Aprašas | Įveskite automatinio įrašų užpildymo veiksmo aprašą. |

„FastTab“ skirtuke **Duomenų šaltinių nustatymas** įtraukite eilutę kiekvienam duomenų šaltiniui, kuris naudojamas procesui, ir nustatykite toliau nurodytus laukus.

| Laukas                  | aprašymas |
|------------------------|-------------|
| Pavadinimas                   | Įveskite duomenų šaltinio pavadinimą. |
| Pranešimo prekės tipas      | Pasirinkite pranešimo elemento, kurį norite naudoti kuriant duomenų šaltinio įrašus, tipą. |
| Kodo tipas           | Pasirinkite sąskaitos, kurią norite susieti susieta su duomenų šaltinio įrašais, tipą. |
| Pagrindinės lentelės pavadinimas      | Pasirinkite lentelę, kuri bus duomenų šaltinis. |
| Laukas Dokumento numeris  | Pasirinkite lauką, iš kurio bus paimtas dokumento numeris pasirinktoje bendrojoje lentelėje. Šio lauko reikšmė naudojama kaip pranešimo elemento **Dokumento numerio** lauko reikšmė. |
| Laukas Dokumento data    | Pasirinkite lauką, iš kurio bus paimta dokumento data pasirinktoje bendrojoje lentelėje. Šio lauko reikšmė naudojama kaip pranešimo elemento **Pranešimo elemento datos** lauko reikšmė. |
| Laukas Dokumento sąskaita | Pasirinkite lauką, iš kurio bus paimta dokumento paskyra pasirinktoje bendrojoje lentelėje. Šio lauko reikšmė naudojama kaip pranešimo elemento **Paskyros numerio** lauko reikšmė. |
| Įmonė                | Šis laukas galimas, kai funkcija **Visos įmonės užklausos dėl įrašų automatinio įvedimo veiksmų** yra įjungta **Funkcijos valdymo** darbo srityje. Naudokite šią funkciją, kad nustatytumėte visos įmonės duomenų šaltinius, skirtus automatinio įrašų įvedimo veiksmams. Duomenis galima iškviesti iš kelių įmonių. |
| Vartotojo užklausa             | <p>Jei nustatote užklausą pasirinkdami **Redaguoti užklausą** virš tinklelio ir nurodote kriterijus, kurie turi būti taikomi pažymėtai bendrajai lentelei, iš kurios įvedami duomenys, šis žymės langelis bus pasirinktas automatiškai. Priešingu atveju visi įrašai užpildomi iš pasirinkto bendrosios lentelės šaltinio.</p><p>Kai funkcija **Visos įmonės užklausos dėl įrašų automatinio įvedimo veiksmų** yra įjungta **Funkcijų valdymo** srityje, o įrašai turi būti surinkti iš kelių įmonių, pridėkite eilutę kiekvienam papildomam juridiniam subjektui, kuris turi būti įtrauktas į ataskaitą. Kiekvienoje naujoje eilutėje pasirinkite **Redaguoti užklausą** ir nurodykite susijusį kriterijų, būdingą juridiniam subjektui, kuris yra nurodytas eilutės lauke **Įmonė**. Kai baigsite **Duomenų šaltinių nustatymo** tinklelyje bus visų juridinių subjektų, kurie turi būti įtraukti į ataskaitas, eilutės.</p> |

## <a name="populate-records-from-multiple-companies"></a><a id="multiple-companies-populate"></a> Automatiškai įvesti įrašus iš kelių įmonių

Jei jūsų įmonė turi pateikti ataskaitą iš kelių juridinių subjektų toje pačioje finansų duomenų bazėje, nustatykite [automatiškai įvesti visų juridinių subjektų,](#populate) iš kurių duomenys turi būti įtraukti į ataskaitas, įrašus.

Norėdami įgalinti šį pajėgumą savo finansų aplinkoje, atlikite šiuos veiksmus. 

1. Eikite į **darbo sričių** \> **funkcijų valdymą**.
2. Raskite ir pasirinkite **visos įmonės užklausas, skirtas automatiškai įvesti įrašų** veiksmų funkciją sąraše.
3. Pasirinkite **Įjungti dabar**. 

Norėdami nustatyti kelių įmonių [, kurių duomenys turi būti](#populate) įtraukti į ataskaitas, įrašų veiksmus, atlikite šiuos veiksmus.

1. Eikite į **mokesčių** \> **nustatymo elektroninius** \> **pranešimus** \> **užpildyti įrašų veiksmus.**

    Kai visos **įmonės užklausos dėl automatiškai** įvedaų įrašų veiksmų funkcijos įgalintos, duomenų šaltinių nustatymo tinklelyje, **kuris yra veiksmų puslapio Automatiškai įvesti įrašus** **,** yra **įmonės** laukas. Esamiems įrašams, kurie buvo sukurti bendrais [įrašų](#populate) veiksmų nustatymo metu, šiame lauke rodomas dabartinio juridinio subjekto identifikatorius.

2. Duomenų šaltinių **nustatymo tinklelyje** pridėkite kiekvieno filialo juridinio subjekto, kuris turi būti įtrauktas į ataskaitą, eilutę ir nustatykite šiuos laukus.

    | Lauko pavadinimas             | Reikšmė |
    |------------------------|-------|
    | Vardas                   | Įveskite teksto reikšmę, kuri padės suprasti, iš kur gaunamas šis įrašas. Pavyzdžiui, įveskite duomenų **šaltinio pavadinimą – filialas 1**. |
    | Pranešimo prekės tipas      | Pasirinkite pranešimo elemento tipą, kurio reikia jūsų EM apdorojimui. |
    | Kodo tipas           | Nurodykite sąskaitos tipą, kuris būtinas jūsų EM apdorojimui. Jei jūsų EM apdorojime nėra konkrečių sąskaitų tipų, pasirinkite **Visi**. |
    | Pagrindinės lentelės pavadinimas      | Nurodykite pagrindinės lentelės, kurios reikia jūsų EM apdorojimui, pavadinimą. |
    | Laukas Dokumento numeris  | Nurodykite lauką, kuriame yra dokumento numeris įrašuose, kuriuos jūsų EM apdorojimo programa. |
    | Laukas Dokumento data    | Nurodykite lauką, kuriame YRA dokumento data EM apdorojimo įrašuose. |
    | Laukas Dokumento sąskaita | Nurodykite lauką, kuriame yra dokumento sąskaita įrašuose, kuriuos apdorosite EM. |
    | Įmonė                | Pasirinkite filialo juridinio subjekto ID. |
    | Vartotojo užklausa             | Šis žymės langelis automatiškai pasirenkamas, kai pasirenkate kriterijus pasirinkdami Redaguoti **užklausą**. |

3. Kiekvienoje naujoje eilutėje pasirinkite **Redaguoti užklausą** ir **nurodykite susijusius juridinio subjekto kriterijus, nurodytus eilutės** lauke Įmonė.

## <a name="web-applications"></a><a id="applications"></a>Žiniatinklio programos

Naudokite žiniatinklio programų parametrus, jog nustatytumėte žiniatinklio programą taip, kad ji palaikytų „Open Authorization“ („OAuth“) 2.0. „OAuth“ yra atvirasis standartas, kurį naudodami vartotojai savo vardu programai gali suteikti „saugią suteiktąją prieigą“, nebendrindami prieigos kredencialų. Autorizavimo procesą taip pat galite atlikti gaudami autorizavimo kodą ir prieigos atpažinimo ženklą. Žiniatinklio programos parametrus galite nustatyti eidami į **Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Žiniatinklio programos**.

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
| Prieigos atpažinimo ženklo galiojimo laikas baigiasi  | Likęs laikas iki prieigos atpažinimo ženklo galiojimo pabaigos. Šis laukas yra automatiškai atnaujinamas. | 
| Priimti                       | Nurodykite žiniatinklio užklausos ypatybę **Priimti**. Pavyzdžiui, įveskite **application/vnd.hmrc.1.0+json**. |
| Turinio tipas                 | Nurodykite turinio tipą. Pavyzdžiui, įveskite **application/json**. |

Be to, autorizavimo procesui palaikyti puslapio **Žiniatinklio programos** veiksmų srityje pasiekiami tolesni mygtukai.

- **Gauti autorizavimo kodą** – inicijuoti žiniatinklio programos autorizavimą. Ši funkcija naudoja ER formatą, nurodytą **Autorizavimo formato susiejimo** lauke, kad sugeneruotų autorizavimo užklausą.
- **Gauti prieigos atpažinimo ženklą** – inicijuoti prieigos atpažinimo ženklo gavimo procesą.
- **Atnaujinti prieigos atpažinimo ženklą** – atnaujinti prieigos atpažinimo ženklą. Ši funkcija naudoja ER formatą, nurodytą **Importavimo atpažinimo ženklo modelio susiejimo** lauke, kad importuotų informaciją apie gautą prieigos atpažinimo ženklą.

Kai prieigos prie žiniatinklio programos atpažinimo ženklas sistemos duomenų bazėje yra saugomas užšifruotu formatu, jį galima naudoti teikiant užklausas žiniatinklio tarnybai. Dėl saugos, prieigą prie atpažinimo ženklo turi būti apribota tik iki tų saugos vaidmenų, kuriems leidžiama tvarkyti tas užklausas. Jei užklausą bando tvarkyti saugos grupei nepriklausantis asmuo, jis gauna klaidą, kad jam neleidžiama atlikti veiksmų naudojant pasirinktą žiniatinklio programą. Norėdami nustatyti saugos vaidmenis, kurie turėtų prieigą prie prieigos atpažinimo ženklo, naudokite puslapyje **Žiniatinklio programos** esantį „FastTab“ **Saugos vaidmenys**. Jei žiniatinklio programoje nenustatyti saugos vaidmenys, tik sistemos administratorius gali atlikti veiksmus naudodamas žiniatinklio programą.

Kiekvienam veiksmui, kuris turi pasirinktą žiniatinklio programą, „FastTab” skirtukas **Veiksmų žurnalas** įrašo informaciją apie vartotoją, datą ir laiką.

Kai kurios žiniatinklio tarnybos gali reikalauti, kad į užklausas būtų įtrauktos skirtingos antraštės. Sistemos administratorius gali nustatyti papildomas antraštes ir jų reikšmes „FastTab” skirtuke **Papildomos antraštės**, o tada naudoti jas užklausos generavimo metu.

## <a name="web-service-settings"></a><a id="settings"></a>Žiniatinklio tarnybos parametrai

Naudokite žiniatinklio tarnybos parametrus tiesioginiam duomenų perdavimui į žiniatinklio tarnybą nustatyti. Žiniatinklio tarnybos parametrus galite nustatyti eidami į **Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Žiniatinklio tarnybos parametrai**.

Toliau pateiktoje lentelėje aprašomi puslapio **Žiniatinklio tarnybos parametrai** laukai.

| Laukas                          | aprašymas |
|--------------------------------|-------------|
| Žiniatinklio tarnyba                    | Įveskite žiniatinklio tarnybos pavadinimą. |
| aprašymas                    | Įveskite žiniatinklio tarnybos aprašą. |
| Interneto adresas               | <p>Įveskite žiniatinklio tarnybos interneto adresą. Jei nurodyta žiniatinklio tarnybos žiniatinklio programa, o žiniatinklio tarnybos interneto adresas turi būti toks pats, kaip nustatytas tos žiniatinklio programos interneto adresas, pasirinkite **Kopijuoti pagrindinį URL**. Tada pagrindinis žiniatinklio programos URL yra nukopijuojamas į šį lauką.</p><p>**Įspėjimas:** trečiųjų šalių tarnybos ar kitos čia konfigūruojamos tarnybos nereikalauja sertifikato ir gali neatitikti „Microsoft” privatumo standartų. Turėtumėte peržiūrėti kiekvienos tarnybos privatumo dokumentaciją ir dirbti su kiekvienu paslaugų teikėju, kad sužinotumėte daugiau apie teikiamų paslaugų atitikimo lygį. Esate atsakingi už tai, kad šios tarnybos atitiktų jūsų saugos, privatumo ir teisės standartus. Jūs prisiimate atsakomybę už šių tarnybų naudojimą. "Microsoft" nesuteikia aiškaus garantijų, garantų ar sąlygų. Primygtinai rekomenduojame naudoti tik tas tarnybas, kurios užtikrina saugius ir įgaliotus ryšius, pavyzdžiui, HTTPS.</p> |
| Sertifikatas                    | Pasirinkite anksčiau nustatytą „Azure” raktų saugyklos sertifikatą. |
| Žiniatinklio programa                | Pasirinkite anksčiau nustatytą raktų žiniatinklio programą. |
| Atsakymo tipas – XML        | Jei atsakymo tipas yra XML, nustatykite šią parinktį į **Taip**. |
| Užklausos metodas                 | Nurodykite užklausos metodą. HTTP apibrėžia užklausų metodų, nurodančių veiksmą, kuris turi būti atliekamas nurodytiems ištekliams, rinkinį. Užklausos metodas gali būti **GET**, **POST** arba kitas HTTP metodas. |
| Užklausų antraštės                | Nurodykite užklausų antraštes. Užklausos antraštė yra HTTP antraštė, kurią galima naudoti HTTP užklausoje. Ji nėra susijusi su pranešimo turiniu. |
| Priimti                         | Nurodykite žiniatinklio užklausos priėmimo ypatybę. |
| Priimti kodavimą                | Nurodykite kodavimo priėmimo reikšmę. Priimtino kodavimo užklausos HTTP antraštėje skelbiamas turinio kodavimas, kurį klientas gali suprasti. Toks turinio kodavimas dažniausiai yra glaudinimo algoritmas. |
| Turinio tipas                   | Nurodykite turinio tipą. Turinio tipo objekto HTTP antraštė nurodo ištekliaus publikavimo kanalo tipą. |
| Sėkmingas atsakymo kodas       | Nurodykite HTTP būsenos kodą, nurodantį, kad užklausa įvykdyta sėkmingai. |
| Užklausos antraščių formato susiejimas | Pasirinkite ER formatą, naudojamą žiniatinklio užklausų antraštėms generuoti. |

## <a name="message-processing-actions"></a><a id="actions"></a>Pranešimų apdorojimo veiksmai

Naudojate pranešimų apdorojimo veiksmus, kad sukurtumėte savo procesų veiksmus ir nustatytumėte jų parametrus. Galite nustatyti pranešimo apdorojimo veiksmus eidami į **Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Pranešimo apdorojimo veiksmai**.

Toliau pateiktose lentelėse aprašomi puslapio **Pranešimų apdorojimo veiksmai** laukai.

### <a name="general-fasttab"></a>Bendras „FastTab“ skirtukas

| Laukas                                     | aprašymas |
|-------------------------------------------|-------------|
| Veiksmo tipas                               | Pasirinkite veiksmo tipą. Informacijos apie galimas pasirinktis žr. toliau šio [straipsnio skyriuje Pranešimo](#action-types) apdorojimo veiksmų tipai. |
| Formato susiejimas                            | Pasirinkite ER formatą, kuris turi būti iškviestas veiksmui atlikti. Šis laukas galimas tik veiksmų tipams **Elektroninių ataskaitų eksportavimas**, **Elektroninių ataskaitų importavimas** ir **Elektroninių ataskaitų eksportavimo pranešimas**. |
| URL kelio formato susiejimas               | Pasirinkite ER formatą, kuris turi būti iškviestas veiksmui atlikti. Šis formatas yra naudojamas kuriant URL adreso kelią, kuris bus įtrauktas į nurodytą pagrindinį pasirinkto žiniatinklio serverio interneto adresą. Šis laukas taikomas tik tipo **Žiniatinklio tarnyba** veiksmams. |
| Pranešimo prekės tipas                         | Pasirinkite įrašų, kurių veiksmą reikia įvertinti, tipą. Šis laukas galimas veiksmų tipams **Pranešimo elemento vykdymo lygis**, **Elektroninių ataskaitų eksportavimas**, **Elektroninių ataskaitų importavimas** ir **Žiniatinklio tarnyba**, taip pat kai kuriems kitiems tipams. Jei šį lauką paliksite tuščią, bus vertinami visi pranešimų apdorojimui apibrėžti pranešimų elementų tipai. |
| Vykdomoji klasė                          | Pasirinkite esamą vykdomosios klasės parametrą. Šis laukas galimas tik veiksmų tipams **Pranešimo elemento vykdymo lygis** ir **Pranešimo elemento vykdymo lygis**. |
| Automatinio įrašų įvedimo veiksmas                   | Pasirinkite esamą automatiškai įvedamą įrašų veiksmą. Šis laukas galimas tik veiksmų tipui **Automatiškai įvesti įrašus**. |
| Žiniatinklio tarnyba                               | Pasirinkite esamą žiniatinklio tarnybą. Šis laukas taikomas tik tipo **Žiniatinklio tarnyba** veiksmams. |
| Siųstino failo vardas                         | Įvesti priedo prie elektroninio pranešimo, kuris turi būti siunčiamas šiuo veiksmu, pavadinimą. Jei keli priedai turi tokį patį pradinio failo vardą, naujausias bus siunčiamas. Jei nerastas joks priedas, kuriame nurodytas pradinis failo vardas, užklausa bus siunčiama be turinio. Šis laukas taikomas tik tipo **Žiniatinklio tarnyba** veiksmams. |
| Failo vardas                                 | Nurodykite failo, kuris bus veiksmo rezultatas, pavadinimą. Šis failas gali būti atsakas iš žiniatinklio serverio arba generuojama ataskaita. Šis laukas taikomas tik tipų **Žiniatinklio tarnyba** ir **Elektroninių ataskaitų eksportavimo pranešimas** veiksmams. |
| Pridėti failus prie šaltinio dokumentų          | Pasirinkite šį žymės langelį, jei norite pridėti sugeneruotus failus prie įrašų, esančių EM elementų nurodytoje bendrojoje lentelėje. Šis laukas galimas tik **Elektroninių ataskaitų eksportavimas** ir **Žiniatinklio tarnyba** tipų veiksmams. |
| Failus iš išvesties archyvo pridėkite prie prekių | Pasirinkite šį žymės langelį, norėdami iš išvesties archyvo failo išskleisti atskirus XML failus ir pridėti juos prie atitinkamų elektroninio pranešimo elementų. Šis laukas galimas tik **Elektroninių ataskaitų eksportavimo** tipo veiksmams. |
| Pranešimo prekių skaičius vieno eksporto metu        | Nurodykite pranešimo elementų, kuriuos reikia įtraukti į vieną failą (pranešimą), skaičiaus limitą. Šis laukas galimas tik **Elektroninių ataskaitų eksportavimo** tipo veiksmams. |
| ER šaltinio naudojimas                             | Pasirinkite šį žymės langelį, kad importavimui naudotumėte ER šaltinio parametrus. Kitu atveju naudojamas priedas iš elektroninio pranešimo. Šis laukas galimas tik **Elektroninių ataskaitų importavimo** tipo veiksmams. |
| Rodyti dialogo langą                               | Šią parinktį nustatykite kaip **Taip**, jei prieš sugeneruojant ataskaitą vartotojams turi būti rodomas dialogo langas. Šis laukas taikomas tik tipo **Elektroninių ataskaitų eksportavimo pranešimas** veiksmams. |

#### <a name="message-processing-action-types"></a><a id="action-types"></a>Pranešimų apdorojimo veiksmų tipai

Galimos toliau nurodytos lauko **Veiksmo tipas** parinktys.

- **Kurti pranešimą** – naudokite šį veiksmo tipą, kad vartotojai galėtų rankiniu būdu kurti pranešimus puslapyje **Elektroninis pranešimas**. Šio tipo veiksmui negalima nustatyti pradinės būsenos.
- **Automatiškai įvesti įrašus** – šis veiksmo tipas jau turi būti nustatytas. Susiekite jį su automatinio įrašų įvedimo veiksmu, kad veiksmą būtų galima įtraukti į apdorojimą. Daroma prielaida, kad šis veiksmo tipas yra naudojamas atliekant pirmą pranešimo apdorojimo veiksmą (kai iš anksto elektroninių pranešimų nebuvo sukurta) ar kaip veiksmas, kuriuo pranešimo elementai įtraukiami į anksčiau sukurtą pranešimą **Kurti pranešimą** veiksmo tipu. Todėl, naudojant šio tipo veiksmus, galima nustatyti tik pranešimo elementų rezultatų būseną. Pradinę būseną galima nustatyti tik pranešimams.
- **Pranešimo vykdymo lygis** – šį veiksmo tipą naudokite vykdomajai klasei, kuri turi būti įvertinta pranešimo lygiu, nustatyti.
- **Pranešimo elemento vykdymo lygis** – šį veiksmo tipą naudokite vykdomajai klasei, kuri turi būti įvertinta pranešimo elemento lygiu, nustatyti.
- **Elektroninių ataskaitų eksportavimas** – naudokite šį veiksmo tipą veiksmams, kuriais turi būti generuojama ataskaita, pagrįsta ER eksportavimo konfigūracija pranešimo elemento lygiu.
- **Elektroninių ataskaitų eksportavimo pranešimas** – naudokite šį veiksmo tipą veiksmams, kuriais turi būti generuojama ataskaita, pagrįsta ER eksportavimo konfigūracija pranešimo lygiu (pavyzdžiui, kai pranešimas neturi jokių pranešimo elementų).
- **Elektroninių ataskaitų importavimas** – naudokite šį veiksmo tipą veiksmams, kuriais turi būti generuojama ataskaita, pagrįsta ER importavimo konfigūracija.
- **Pranešimų lygio vartotojų apdorojimas** – šį veiksmo tipą naudokite veiksmams, kuriais nurodomas tam tikras rankinis vartotojo veiksmas pranešimų lygiu. Pavyzdžiui, vartotojas gali atnaujinti pranešimų būseną.
- **Vartotojų apdorojimas** – šį veiksmo tipą naudokite veiksmams, kuriais nurodomas tam tikras rankinis vartotojo veiksmas pranešimų elementų lygiu. Pavyzdžiui, vartotojas gali atnaujinti pranešimų elementų būseną.
- **Žiniatinklio tarnyba** – šį veiksmo tipą naudokite veiksmams, kuriais sugeneruota ataskaita turi būti perduodama žiniatinklio tarnybai. Šis veiksmo tipas nenaudojamas Italijos pirkimo ir pardavimo sąskaitų faktūrų ryšių ataskaitoms teikti. Šiam veiksmo tipui, puslapyje **Pranešimų apdorojimo veiksmai** yra „FastTab“ skirtukas **Įvairi informacija**, kuriame galite nurodyti patvirtinimo tekstą. Šis patvirtinimo tekstas rodomas vartotojams prieš apdorojant užklausas, pateiktas pasirinktai žiniatinklio tarnybai.
- **Užklausos tikrinimas** – šį veiksmo tipą naudokite tikrinimui iš serverio prašyti.

### <a name="initial-statuses-fasttab"></a>Pradinių būsenų „FastTab“

> [!NOTE]
> „FastTab“ **Pradinės būsenos** nepasiekiamas, kai veiksmų pradinis veiksmo tipas yra **Kurti pranešimą**.

| Laukas               | Aprašas |
|---------------------|-------------|
| Pranešimo prekės būsena | Pasirinkite pranešimo elemento būseną, pagal kurią turi būti įvertintas pasirinkto pranešimo apdorojimo veiksmas. |
| aprašymas         | Pasirinkto pranešimo elemento būsenos aprašas. |

### <a name="result-statuses-fasttab"></a>Galutinių būsenų „FastTab“

| Laukas               | aprašymas |
|---------------------|-------------|
| Pranešimo būsena      | Pasirinkite pranešimų būsenas, pagal kurias turi būti įvertintas pasirinkto pranešimo apdorojimo veiksmas. Šis laukas galimas tik pranešimų apdorojimo veiksmams, kurie vertinami pranešimo lygiu. Pavyzdžiui, jis pasiekiamas, kai veiksmų tipas yra **Elektroninių ataskaitų eksportavimas** ir **Elektroninių ataskaitų importavimas**, bet nepasiekiamas, kai veiksmų tipas yra **Vartotojų apdorojimas** ir **Pranešimo elemento vykdymo lygis**. |
| aprašymas         | Pasirinkto pranešimo būsenos aprašas. |
| Atsiliepimo tipas       | Pasirinkto pranešimo būsenos atsakymo tipas. |
| Pranešimo prekės būsena | Pasirinkite rodomas būsenas, kurios turi būti prieinamos įvertinus pasirinkto pranešimo apdorojimo veiksmą. Šis laukas galimas tik pranešimų apdorojimo veiksmams, kurie vertinami pranešimo elemento lygiu. Pavyzdžiui, jis galimas veiksmų tipams **Vartotojų apdorojimas** ir **Pranešimo elemento vykdymo lygis**. Šiame lauke pranešimų apdorojimo veiksmams, įvertintiems pranešimo lygiu, rodoma pranešimo elemento būsena, kuri buvo nustatyta pasirinkto pranešimo būsenai. |

Toliau pateikiamoje lentelėje rodomos rezultatų būsenos, kurias reikia nustatyti skirtingiems veiksmų tipams ir atsakų tipams.

| Elektroninio pranešimo veiksmo tipas / atsako tipas | Sėkmingai įvykdyta | Darbo klaida | Techninė klaida | Vartotojo nustatyta | Atšaukti |
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

## <a name="electronic-message-processing"></a><a id="processing"></a>El. pranešimų apdorojimas

Elektroninių pranešimų apdorojimas yra pagrindinė EM funkcionalumo koncepcija. Ji sujungia veiksmus, kuriais turi būti įvertintas elektroninis pranešimas. Veiksmus galima susieti panaudojant pradinę būseną ir rezultatų būseną. Arba veiksmus, kurių tipas **Vartotojų apdorojimas**, galima pradėti savarankiškai. Norėdami nustatyti elektroninių pranešimų apdorojimą, eikite į **Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Elektroninių pranešimų apdorojimas**.

„FastTab“ skirtuke **Veiksmas** galima pridėti iš anksto apibrėžtų veiksmų apdorojimui. Galite nurodyti, ar veiksmą reikia vykdyti atskirai, ar jį galima pradėti apdorojant. Norėdami nurodyti, kad apdorojamą veiksmą gali inicijuoti tik vartotojas, to veiksmo lauką **Vykdyti atskirai** nustatykite kaip **Taip**. Jei veiksmas turi būti pradedamas apdorojant pranešimus arba pranešimų elementus, kurie yra tokios būsenos, kokia nustatyta kaip pradinė to veiksmo būsena, lauką **Vykdyti atskirai** nustatykite kaip **Ne**. Tipo **Vartotojo veiksmas** veiksmus visada reikia vykdyti atskirai.

Kartais kelis veiksmus reikia sujungti į seką, net jei pirmasis veiksmas yra nustatytas atskiram vykdymui. Pavyzdžiui, vartotojas privalo inicijuoti ataskaitos generavimą. Tačiau iš karto po ataskaitos sugeneravimo, ją reikia išsiųsti į žiniatinklio tarnybą, o žiniatinklio tarnybos atsakas turi būti nurodytas sistemoje. Šiuo atveju galite sukurti neatskiriamą veiksmų, kurie visada turi būti vykdomi kartu, seką. „FastTab“ konteineryje **Veiksmas** virš tinklelio pasirinkite **Neatskiriamos sekos** ir sukurkite seką. Tada lauke **Neatskiriama seka** pasirinkite seką visiems veiksmams, kuriuos reikia vykdyti kartu vienoje sekoje. Pavyzdžiui, pirmam sekos veiksmui lauką **Vykdyti atskirai** galima nustatyti į **Taip**, o visiems kitiems veiksmams – į **Ne**.

**Elektroninių ataskaitų eksportavimas** ir **Elektroninių ataskaitų eksportavimo pranešimas** tipų veiksmai vykdo ER formatą, turintį įvesties parametrus. Jei jūsų elektroninio pranešimo apdorojimas apima bet kurio iš šių tipų veiksmus, prieš ataskaitos generavimą turite nurodyti įvesties parametrų reikšmes. Tokiu būdu sistema gali naudoti paketo režimą ataskaitai generuoti. Galite pasirinkti **Parametrai** virš tinklelio, kad nustatytumėte parametrus pasirinktam veiksmo tipui (**Elektroninių ataskaitų eksportavimas** arba **Elektroninių ataskaitų eksportavimo pranešimas**). Pasirinkite **Naudoti parametrus** žymės langelį veiksmui, kuris turi būti vykdomas su paketo režime nurodytais parametrais.

Naudokite „FastTab“ skirtuką **Pranešimo elemento papildomi laukai**, kad pridėtumėte iš anksto apibrėžtų papildomų laukų, susijusių su pranešimo elementais. Turite pridėti papildomų laukų kiekvienam pranešimo elemento, su kuriuo susiję laukai, tipui. Galite nurodyti numatytąją vertę, kuri apdorojimo metu bus priskirta papildomam laukui.

Naudokite „FastTab“ skirtuką **Pranešimo papildomi laukai**, kad pridėtumėte iš anksto apibrėžtų papildomų laukų, susijusių su pranešimais. Galite nurodyti numatytąją vertę, kuri apdorojimo metu bus priskirta papildomam laukui.

Naudokite „FastTab“ skirtuką **Saugos vaidmenys**, kad nustatytumėte saugos vaidmenis, iš anksto apibrėžtus sistemoje konkrečiam apdorojimui. Vartotojai, turintys tam tikrą vaidmenį, matys tik tam vaidmeniui apibrėžtą apdorojimą.

Naudokite „FastTab“ skirtuką **Paketas**, kad nustatytumėte apdorojimą dirbti paketiniu režimu. Patariame nustatyti paketinį režimą tiesioginiam apdorojimui **Elektroninių pranešimų** arba **Elektroninių pranešimų elementų** puslapyje, kai pasirenkate **Vykdyti apdorojimą** veiksmų srityje, kad inicijuotumėte apdorojimą.
