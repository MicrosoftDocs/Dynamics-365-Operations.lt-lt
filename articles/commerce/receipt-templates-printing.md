---
title: Gavimo kvitų formatų nustatymas ir dizainas
description: Šiame straipsnyje aprašoma, kaip modifikuoti formų maketus, norint kontroliuoti, kaip spausdinami kvitai, SF ir kiti dokumentai. „Dynamics 365 Commerce“ yra formos maketo konstruktoriaus funkcija, kurią naudodami galite lengvai kurti ir modifikuoti įvairių rūšių formų maketus.
author: rubencdelgado
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFormLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 281a5e2be6f43f5a83ef7435b2041423dd5d4caa
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792128"
---
# <a name="set-up-and-design-receipt-formats"></a>Gavimo kvitų formatų nustatymas ir dizainas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip modifikuoti formų maketus, norint kontroliuoti, kaip spausdinami kvitai, SF ir kiti dokumentai. „Dynamics 365 Commerce“ yra formos maketo konstruktoriaus funkcija, kurią naudodami galite lengvai kurti ir modifikuoti įvairių rūšių formų maketus.

> [!IMPORTANT]
> Turite nustatyti formų maketus ir kvitų profilius, kad galėtumėte spausdinti kvitus ir kitus dokumentus naudodami „Retail Modern POS“ ir „Cloud POS“. Į kvito šabloną galite įtraukti kelis formos išdėstymus. Tada kvito šabloną galite priskirti spausdintuvui, modifikuodami aparatūros šabloną.

## <a name="set-up-a-receipt-format"></a>Kvitų formato nustatymas

1. Eikite į **Maženinė prekyba ir komercija** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA** &gt; **Kvito formatai**.
2. Puslapyje **Kvito formatas** spustelėkite **Naujas**, kad skurtumėte naują formos maketą, arba pasirinkite esamą formos maketą.
3. Lauke **Kvito formatas** įveskite formos maketo identifikatorių, tada pasirinkite kvito tipą, taikomą šiam maketui. Taip pat galite įvesti aprašą ir trumpą kvito pavadinimą lauke **Pavadinimas**.
4. „FastTab“ **Bendra** pasirinkite vieną iš toliau nurodytų parinkčių spausdinimo veikimo būdui nurodyti.

    - **Visada spausdinti** – kvitas spausdinamas automatiškai, jei reikia.
    - **Nespausdinti** – kvitas nėra spausdinamas.
    - **Raginti vartotoją** – vartotojas bus paragintas spausdinti kvitą.
    - **Pagal poreikį** – šią parinktis skirta tik dovanų kvitams. Pasirinkus šią parinktį, vartotojas gali spausdinti dovanų kvitą naudodamas puslapį **Grąža**, jei reikia dovanų kvito.

## <a name="print-images"></a>Spausdinti paveikslėlius

Gaunantis kūrėjas apima **Logotipą** kintamąjį, kuris gali būti naudojamas siekiant nurodyti gavime spausdintinus paveikslėlius. Paveikslėliai, įtraukti į gavimus, naudojantys **Logotipo** kintamąjį turi būti vienos chromosomos bitmap (.bmp) failų tipai. Jei .bmp paveikslėlis yra nurodytas gavimo kūrimo įrankyje, tačiau nėra spausdinamas nusiuntus į spausdintuvą, failo dydis gali būti per didelis ir pikselių dimensijos paveikslėlyje nėra suderinamos su spausdintuvu. Jei taip atsitinka, pabandykite sumažinti paveikslėlio failo rezoliuciją.   

## <a name="design-a-receipt-format"></a>Kvito formato kūrimas

Naudokite formų maketo konstruktorių, kad grafiškai sukurtumėte formos dokumento maketą. Puslapyje **Kvito formato dizaineris** yra trys dalys: **Antraštė**, **Eilutės** ir **Poraštė**. Kai kurių tipų formų maketuose naudojami elementai iš visų trijų sekcijų, o kituose tipuose naudojami elementai tik iš vienos arba dviejų sekcijų. Norėdami peržiūrėti elementus, kurie pasiekiami kiekvienoje sekcijoje, spustelėkite atitinkamą mygtuką naršymo srityje, kairėje puslapio pusėje.

1. Eikite į **Maženinė prekyba ir komercija** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA** &gt; **Kvito formatai**.
2. Puslapyje **Kvito formatas** pasirinkite formos maketą ir tada spustelėkite **Dizaino įrankis**.
3. Spustelėkite **Paleisti**, kad pradėtumėte diegti „Commerce“ dizaino įrankio pagrindinį kompiuterį.
4. „Internet Explorer“ apačioje rodomoje pranešimų juostoje spustelėkite **Atidaryti**, kad pradėtumėte diegti vieno spustelėjimo dizaino įrankį. (Kitose naršyklėse pranešimų juosta gali būti rodoma kitoje vietoje.) Vykdymo indikatorius rodo diegimo proceso eigą.
5. Kai diegimas baigtas, įveskite savo „Commerce“ vartotojo vardą ir slaptažodį, tada spustelėkite **Prisijungti**, kad paleistumėte dizaino įrankį.
6. Kai kredencialai patvirtinti ir dizaino įrankis paleistas, galima pradėti kurti kvito formatą arba modifikuoti esamą formatą.
7. Norėdami kurti formos elementus, pasirinkite sekciją **Antraštė**, **Eilutės** arba **Poraštė**, tada nuvilkite elementą iš sekcijos į darbo sritį. Daugelyje elementų yra kintamųjų, kurie automatiškai įvedami kartu su duomenimis iš duomenų bazės. Kiti elementai, pvz., **Tekstas**, suteikia galimybę spausdinti pasirinktinį tekstą kvite.

    > [!NOTE]
    > Galite nurodyti, kiek eilučių apima kiekviena sekcija, koreguodami skaičių apatiniame dešiniajame tos sekcijos kampe. Kad būtų lengviau modifikuoti sritį, padidinkite jos aukštį vilkdami srities apačioje esančią dydžio keitimo juostą. Sekcijos aukštis darbo srityje neturi įtakos eilučių skaičiui faktiniame kvite.

8. Nuvilkę elementą į darbo sritį, nustatykite dalies ypatybes puslapio apačioje esančioje srityje **Objekto informacija**. Įveskite vieną arba daugiau iš toliau nurodytų parametrų.

    - **Lygiuoti** – nustatykite lauko lygiavimą kaip **Kairėje** arba **Dešinėje**.
    - **Užpildo simbolis** – nurodykite tarpų simbolį. Pagal numatytuosius parametrus naudojamas tuščias tarpas, bet galite įvesti kitą simbolį.
    - **Prefiksas** – įveskite reikšmę, kuri rodoma lauko pradžioje. Šis parametras taikomas tik maketo sekcijai **Eilutės**.
    - **Simboliai** – nurodykite maksimalų simbolių, kuriuos galima įvesti laukei, jei elementas yra kintamasis, skaičių. Jei tekstas lauke yra ilgesnis už nurodytą simbolių skaičių, tekstas sutrumpinamas, kad tilptų lauke.
    - **Kintamasis** – šis žymės langelis pažymimas automatiškai, jei elemente yra kintamasis ir jo negalima tinkinti.
    - **Šrifto tipas** – nustatykite šrifto stilių **Įprastas** arba **Paryškintasis**. Paryškintosios raidės užima dvigubai daugiau vietos nei įprastos raidės. Todėl kai kurie simboliai gali būti sutrumpinti.
    - **Šrifto dydis** – nustatykite šrifto dydį **Įprastas** arba **Didelis**. Didelės raidės yra dvigubai aukštesnės nei įprastos raidės. Todėl, naudojant dideles raides, kvite gali persidengti tekstas.
    - **Naikinti** – spustelėkite šį mygtuką, jei norite pašalinti pasirinktą dalį iš formos maketo.

## <a name="assign-receipt-profiles"></a>Kvitų šablonų priskyrimas

Kvitų šablonai yra tiesiogiai priskiriami spausdintuvams naudojant aparatūros šabloną.

1. Atidarykite aparatūros šabloną, spausdami **Maženinė prekyba ir komercija** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA profiliai** &gt; **Aparatūros šablonas**.
2. Pasirinkite spausdintuvą, tada lauke **Kvito šablonas** priskirkite kvito šabloną, kuris bus naudojamas registre.

> [!NOTE]
> Jei naudojami du spausdintuvai, vieną spausdintuvą galima naudoti standartiniams 40 stulpelių terminiams kvitams spausdinti. Antrasis spausdintuvas paprastai yra naudojamas gavimo tipams, kuriuose reikia pateikti daugiau informacijos, per visą puslapį spausdinti. Šie gavimo tipai apima kliento užsakymų kvitus ir kliento SF.


[!INCLUDE[footer-include](../includes/footer-banner.md)]