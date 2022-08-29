---
title: Produktų, kurių laikymo laikas ribotas, bendrasis planavimas
description: Šiame straipsnyje aprašoma, kaip nustatyti ir naudoti planavimo priemones, atsižvelgiama į nebaigtų produktų laikymo trukmę.
author: t-benebo
ms.date: 08/10/2022
ms.topic: article
ms.search.form: ReqPlanSched, CustTable, EcoResProductDetailsExtended, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 95c905cbcc3c057dbccf2b7d6e894b1e99ddfba5
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337360"
---
# <a name="master-planning-for-products-with-limited-shelf-life"></a>Produktų, kurių laikymo laikas ribotas, bendrasis planavimas

[!include [banner](../../includes/banner.md)]

Laikymo trukmė – tai laikas, kurį produktas gali būti laikomas, kol jo nebegalima naudoti arba parduoti. Produktų, kurių laikymo laikas ribotas, atveju greičiausiai naudosite pirmojo galiojimo pabaigos, pirmojo iš pirmojo iš (FEFO) sandėlio strategiją, pagal kurią bus prioritetizuojamas prekių suvartojimas ir pardavimas pagal likusį laikymo trukmę. Ši sandėlio strategija yra susijusi su maistu, pasiūlymo ir kitomis prekėmis, kurios apibūdinamos trumpu saugojimo laiku. Pagal FEFO, prekės sandėlyje saugomos kaip prekės prekybos centro lentynoje: produktai, kurių laikymo laikas ilgesnis, padėti į lentynas, kad produktai, kurių laikymo trukmė trumpesnė, būtų siunčiami pirmiausia.

## <a name="using-shelf-life-in-master-planning"></a>Laikymo trukmės naudojimas bendrojo planavimo metu

Šiame skyriuje paaiškinama, kaip bendrasis planavimas siūlo lentynų prekių tiekimą.

Vykdant bendrąjį planą, generuojami siūlomi suplanuoti užsakymai (tiekimas), kurie pateis jūsų poreikį ir sumažins vėlavimą. Jei jūsų plane yra prekių, kurių laikymo laikas ribotas, planavimo skaičiavimai tampa sudėtingesni, nes planas neturi tik sumažinti vėlavimo, bet ir naudoti esamą tiekimą prieš jo galiojimo pabaigą. Plane turi būti bandykite naudoti tiekimą, artimiausią jo galiojimo datai, prieš vėliau pasibaigsiaantį tiekimą. Todėl bendrojo planavimo metu siekia šių tikslų, šia tvarka:

1. Sumažinti vėlavimų sumą.
1. Maksimaliai padidinti FEFO tiekimo sumą.
1. Sumažinti atsargų papildymą.

Kai kuriais atvejais gali kilti konfliktas tarp pirmųjų dviejų tikslų ir reikia pasirinkti: ar norite atidėti siuntą, ar norite naudoti tiekimą, kuris vėliau baigiasi, o ne baigtis tiekti? Jei norite išspręsti šį konfliktą bendrojo planavimo metu, sistema prioritetizuoja, kaip galima sumažinti uždelsimo greitį, kol pasibaigs tiekimo laikas. Apskritai, šis konflikto tipas įvyksta tada, kai laikotarpis gali būti uždelsimas ir padengimas. Todėl rekomenduojame naudoti trumpesnią nei prekės laikymo laikotarpį. Kiti padengimo tipai (pvz., poreikis) nepastebima, kad gali įvykti šio tipo konfliktas.

## <a name="set-up-shelf-life"></a>Nustatyti laikymo trukmę

### <a name="configure-each-master-plan-to-consider-shelf-life"></a>Konfigūruoti kiekvieną bendrąjį planą, kad būtų atsižvelgti į laikymo trukmę

Pagal numatytuosius nustatymus, pagrindiniuose planuose atsižvelgti į laikymo trukmę. Naudokite šią procedūrą, norėdami įgalinti kiekvieno bendrojo plano, kuriam reikia, laikymo trukmės skaičiavimus.

1. Pereikite prie bendrojo **planavimo nustatymo \> planų \>\> 100**.
1. Sąrašo srityje pasirinkite esamą planą arba sukurkite naują.
1. Bendrajame **"** FastTab" nustatykite parinktį **Naudoti laikymo trukmės datas** kaip *Taip*.

### <a name="configure-tracking-dimension-groups-to-track-the-batch-dimension"></a>Konfigūruoti sekimo dimensijų grupes paketo dimensijai sekti

Prekės laikymo trukmę galima sekti tik tuo atveju, jei ta prekė sekama paketo dimensijoje. Kitaip tariant, paketo nuoroda ir reikalaujama data turi būti įrašyta gavimo arba gamybos metu ir per kiekvieną prekės atsargų operaciją. Norėdami valdyti šią pasirinktį, nustatykite vieną ar daugiau sekimo dimensijų grupių, kad būtų galima atlikti reikiamą sekimą, ir tada, jei reikia, priskirkite šioms grupėms atitinkamas prekes.

Norėdami nustatyti sekimo dimensijų grupę paketo dimensijai sekti, naudokite nurodytą procedūrą.

1. Eikite į **produkto informacijos valdymo nustatymą \> Dimensija \> ir variantų grupių sekimo \> dimensijų grupės**.
1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Veiksmų srityje pasirinkite Naujas, kad sukurtumėte **naują** sekimo dimensijų grupę. Įveskite pavadinimą ir aprašymą, tada veiksmų srityje **pasirinkite** Įrašyti.
    - Sąrašo srityje pasirinkite esamą sekimo dimensijų grupę, kurią norite nustatyti paketo dimensijai sekti.

1. Sekimo dimensijos **"FastTab", paketo** numerio **eilutėje, pažymėkite žymės langelius aktyvių** ir faktinių **atsargų** stulpeliuose **.**

### <a name="set-up-shelf-life-for-a-product"></a>Nustatyti produkto laikymo trukmę

Norėdami nustatyti produkto laikymo trukmę, naudokite nurodytą procedūrą.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Sukurkite arba atidarykite produktą, kurį norite nustatyti.
1. Norėdami naudoti laikymo trukmės parametrus, bendrajame "FastTab" nustatykite sekimo dimensijų grupės lauką kaip sekimo dimensijų grupę, **·** **kuri** nustatyta paketo dimensijai sekti. Šį lauką galima nustatyti tik pirmą kartą kuriant produktą. Negalima pakeisti esamų produktų vertės.
1. Skirtuke **Valdyti atsargas** "FastTab" nustatykite šiuos laukus:

    - **Pranešimo apie laikymo** pabaigą laikotarpis dienomis – nurodykite laikotarpį (dienomis), kuriuo turi būti pažymėtas šio produkto paketas, siekiant užtikrinti, kad jis tinkamas suvartojimui ar perpardavimui. Šio lauko vertė pridedama prie paketo pagaminimo datos, kad *būtų* nustatyta pranešimo apie laikymo *pabaigą data*. Galite konfigūruoti sistemą, kad ji sugeneruotų kokybės užsakymus, kai paketas artėja prie pranešimo apie laikymo pabaigą datos.
    - **Laikymo laikotarpis dienomis** – nurodykite dienų skaičių iki šio produkto paketo galiojimo pabaigos. Ši vertė pridedama prie gamybos *datos, kad būtų* nustatyta galiojimo *data*. Paketas laikomas netinkamu po šios datos.
    - **Galiojimo laikotarpis dienomis** – nurodykite laikotarpį (dienomis), po kurio šio produkto paketas vis dar parduodamas, tačiau nebegalima išlaikyti kai kurių pradinių jo ypatybės. Ši vertė pridedama prie gamybos *datos, kad* būtų nustatyta *galiojimo pabaigos data*. Galite vykdyti ataskaitas norėdami identifikuoti atsargas, kurių galiojimo pabaigos data praėjusi. 

### <a name="set-a-sellable-days-rule-for-each-customer"></a>Kiekvienam klientui nustatyti pardavimo dienų taisyklę

*Pardavimo dienų funkcija* užtikrina, kad produktai iš paketo, kurių galiojimas greitai baigsis, nebus siunčiami klientams. Be to, ji užtikrina, kad kai produktai siunčiami klientui, tinkamas pardavimo dienų skaičius vis tiek bus po pristatymo.

Norėdami naudoti pardavimo dienų funkciją, turite nustatyti kiekvienam klientui taikomas kiekvieno produkto (ar produktų grupės) pardavimo dienų skaičių. Turite neautomatiniu būdu užbaigti šį procesą, nes nėra jo duomenų objekto.

Norėdami nustatyti kiekvieno kliento kiekvieno produkto pardavimo dienas, naudokite nurodytą procedūrą.

1. Eikite į **Pardavimas ir rinkodara \> Klientai \> Visi klientai**.
1. Raskite ir pasirinkite klientą, kurį norite nustatyti.
1. Veiksmų srities skirtuko Pardavimas **grupės** Nustatymas **dalyje** Pardavimo **dienos pasirinkite Parduotinos \> dienos**.
1. Pardavimo dienomis **kliento atveju tinklelyje** pateikiamas esamų kiekvieno produkto ar produktų grupės pardavimo dienų taisyklių sąrašas. Norėdami pridėti ar redaguoti eilutes tinklelyje, naudokite veiksmų srities mygtukus. Filtras **pateikiamas**, kad padėtų rasti esamas eilutes.
1. Kiekvienai eilutei nustatykite šiuos laukus:

    - **Prekės kodas** – pasirinkite vieną iš šių verčių, norėdami nurodyti paveiktų prekių aprėptį:

        - *Lentelė* – eilutė taikoma konkrečiai prekei.
        - *Grupė* – eilutė taikoma konkrečiai prekių grupei.
        - *Viskas* – eilutė taikoma visoms prekėms.

    - **Prekės ryšys** – jei lauke **Prekės kodas nustatote** lentelę *·*, pasirinkite konkrečią prekę. Jei lauke Prekės kodas **nustatoma** Grupė *·*, pasirinkite prekių grupę. Jei prekės kodo lauką **nustatote** kaip *Visi*, šis laukas negalimas.
    - **Pardavimo dienos –** įveskite minimalų dienų skaičių, per kurį klientas turi parduoti atitinkančius produktus prieš paketo galiojimo pabaigos datą. Pardavimo dienų vertė priklauso nuo pageidaujamos gavimo datos (arba patvirtintos gavimo datos, jei nustatyta) pagal pardavimo užsakyme atitinkančius produktus.
    - *(Kitos produkto dimensijos)* – jei reikia, norėdami dar labiau apriboti eilutės aprėptį, nurodykite kitas dimensijų **vertes (pvz.,** **Dydis** ir Spalva). Norėdami kontroliuoti, kurios dimensijos rodomos tinklelyje, veiksmų **srityje pasirinkite** Rodyti dimensijas.

### <a name="set-up-all-relevant-products-so-that-they-are-fefo-date-controlled"></a>Nustatyti visus susijusius produktus, kad jie būtų valdomi pagal FEFO datą

Norint, kad darbo dienos veiktų, **kiekviena susijusi prekė turi priklausyti prekių modelių grupei, kurioje pažymėtas FEFO datos** kontrolės žymės langelis.

Norėdami nustatyti prekės modelio grupę, kad ji palaiko pardavimo dienų funkcionalumą, naudokite nurodytą procedūrą.

1. Eikite į **Atsargų valdymas \> Nustatymas \> Atsargos \> Prekių modelių grupės**.
1. Pasirinkite sąrašo srityje esamą grupę arba kurkite naują, veiksmų **srityje** pasirinkdami Naujas.
1. Atsargų strategijų **"** FastTab" pažymėkite **FEFO datos kontroliuojamą** žymės langelį.
1. Jei reikia, nustatykite kitus grupės laukus.

Norėdami peržiūrėti arba nustatyti prekės modelių grupę, kuriai priklauso produktas, naudokite nurodytą procedūrą.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Atidarykite produktą, kurį norite patikrinti arba redaguoti.
1. Bendrajame **·** "FastTab" nustatykite prekių **modelių grupės** lauką kaip grupę **, kurioje pažymėtas FEFO datos** valdomas žymės langelis.

## <a name="example-1-simple-fefo-10-day-period-zero-days-of-lead-time"></a>1 pavyzdys: Paprastasis FEFO, 10 dienų laikotarpis, nulinės gamybos laiko dienos

Šiame pavyzdyje pateikiamas pagrindinis laikymo trukmės, kai atliekamas iškvietimas tarp tiekimo užsakymų ir poreikio, kad būtų pasiekti šie sistemos tikslai:

- Sumažinti vėlavimų sumą.
- Maksimaliai padidinti FEFO tiekimo sumą.
- Sumažinti atsargų papildymą.

Sistema turi šiuos prekės ir bendrojo plano parametrus:

- **Padengimo kodas (papildymo strategija):** laikotarpis 
- **Padengimo laikotarpis:** 10 dienų (lygu laikymo laikotarpiui)
- **Laikymo trukmė –** 10 dienų
- **Pardavimo dienos:** 0 dienų
- **Gamybos laikas:** 0 dienų
- **Neigiamos dienos:** 0 dienų
- **Suplanuoto užsakymo tipas (numatytieji prekės užsakymo parametrai):** pirkimo užsakymas

Sistemoje yra tokie prekės pardavimo užsakymai:

- **SO1:** kiekis (kiekis) = 2, pageidaujama pristatymo data = šiandien + 1 diena
- **SO2:** kiekis = 1, pageidaujama pristatymo data = šiandien + 4 dienos
- **SO3:** kiekis = 1, pageidaujama pristatymo data = šiandien + 5 dienos

Dėl visų šių pardavimo užsakymų prekės poreikis yra sukurtas.

Yra toks prekės tiekimas:

- **Turimos atsargos:** kiekis = 1, galiojimo data = šiandien + 5 dienos
- **Pirkimo užsakymas 1 (PO1):** gavimo data = šiandien + 2 dienos, kiekis = 1, galiojimo data = šiandien + 4 dienos

Sistema sukuria tiekimo sąrašą, kuris gali padengti šį poreikį, ir surūšiuoja sąrašą pagal galiojimo datą (naudodama FEFO).

Bendrasis planavimas sukuria reikiamą iškvietimą tarp tiekimo ir poreikio. Taip pat sukuriamas reikiamas poreikis, remiantis tiekimo sąrašu (naudojant FEFO) ir atsižvelgiama į pasiekiamumo datą.

- SO1 gali būti įvykdomas pagal turimą kiekį, bet jo negalima įvykdyti PU1, nes PO1 pasiekiamumo data yra viena diena vėliau nei SO1 reikalauja. Todėl SO1 generuoja poreikį vienam prekių vienetui.
- SO2 gali būti taikomas PO1, nes PO1 bus pristatytas iki pageidaujamo laiko ir galiojimo data vis tiek galios. Todėl SO2 reikalavimą visiškai padengia PU1.
- SO3 nėra taikomas, nes nėra išteklių. Todėl SO3 generuoja poreikį vienam prekių vienetui.

Siekdama įvykdyti visus likusius reikalavimus, sistema turi sukurti šį suplanuotą pirkimo užsakymą:

- **TS1:** gavimo data = šiandien, kiekis = 2, galiojimo data = šiandien + 10 dienų

Šioje lentelėje apibendrinami rezultatai.

| Poreikis | Iškvietimas |
|---|---|
| **SO1:** pristatymo data = šiandien + 1 diena, kiekis = 2 | <p>**Turimos prekės:** kiekis = 1, galiojimo data = šiandien + 5 dienos</p><p>**DAT1:** Gavimo data = šiandien, kiekis = 1, galiojimo data = šiandien + 10 dienų</p> |
| **SO2:** pristatymo data = šiandien + 4 dienos, kiekis = 1 | **EKA:** gavimo data = šiandien + 2 dienos, 1 kiekis, galiojimo data = šiandien + 4 dienos |
| **SO3:** pristatymo data = šiandien + 5 dienos, kiekis = 1 | **TS1:** gavimo data = šiandien, kiekis = 2, galiojimo data = šiandien + 10 dienų |

Toliau pateikta iliustracija rodo šio pavyzdžio laiko juostą.

![1 pavyzdys: Paprastasis FEFO, 10 dienų laikotarpis, nulinės gamybos laiko dienos.](media/fefo-example-1.png "1 pavyzdys: Paprastasis FEFO, 10 dienų laikotarpis, nulinės gamybos laiko dienos")

## <a name="example-2-simple-fefo-requirement-three-days-of-lead-time"></a>2 pavyzdys: Paprastasis FEFO, poreikis, trys gamybos laiko dienos

Šis pavyzdys rodo, kaip sistemos bandymas sumažinti vėlavimą kartais gali trukti per daug.

Sistema turi šiuos prekės ir bendrojo plano parametrus:

- **Padengimo kodas (papildymo strategija):** reikalavimas
- **Laikymo trukmė –** 10 dienų
- **Pardavimo dienos:** 0 dienų
- **Gamybos laikas:** nustatė šios tiekėjo prekybos sutartys:

    - **1 prekybos sutartis:** jei kiekis = 1, gamybos laikas = 4
    - **2 prekybos sutartis:** jei kiekis = 2, gamybos laikas = 3

- **Neigiamos dienos:** 0 dienų
- **Suplanuoto užsakymo tipas (numatytieji prekės užsakymo parametrai):** pirkimo užsakymas

Sistemoje yra toks pardavimo užsakymas:

- **SO1:** kiekis = 2, pageidaujama pristatymo data = šiandien + 3 dienos

Šį poreikį padengia esamas tiekimas ir patvirtintas pirkimo užsakymas:

- **Turimos atsargos:** turima = šiandien, kiekis = 1, galiojimo data = šiandien + 2 dienos
- **EKA:** gavimo data = šiandien + 3 dienos, kiekis = 1, galiojimo data = šiandien + 4 dienos

Negalima įvykdyti turimų atsargų SO1, nes atsargų galiojimo data yra prieš siuntimo datą. PO1 gali padengti SO1 reikalavimą tik 1 kiekiu. Todėl SO1 generuoja poreikį vienam prekių vienetui. Šiam poreikiui patenkinti sistema sukuria suplanuotą pirkimo užsakymą (ĮVERTINIMŲ1).

Sistema turi dvi prekybos sutartis (viena – 1 kiekis, gamybos laikas = 4 dienos, o viena – 2, gamybos laikas = 3 dienos). Todėl sistema mėgina sumažinti vėlavimą, sukurdama suplanuotą pirkimo užsakymą (²1), kuris atitinka antrą prekybos sutartį. Rezultatas yra pristatymo perviršis (kiekis = 2, galiojimo data = šiandien + 10 dienų).

Šioje lentelėje apibendrinami rezultatai.

| Poreikis | Iškvietimas |
|---|---|
| **SO1:** pristatymo data = šiandien + 3 dienos, kiekis = 2 | <p>**EKA:** gavimo data = šiandien + 3 dienos, kiekis = 1, galiojimo data = šiandien + 4 dienos</p><p>**TS1:** gavimo data = šiandien + 3 dienos, kiekis = 1, galiojimo data = šiandien + 10 dienų</p> |

Toliau pateikta iliustracija rodo šio pavyzdžio laiko juostą.

![2 pavyzdys: Paprastasis FEFO, poreikis, trys gamybos laiko dienos.](media/fefo-example-2.png "2 pavyzdys: Paprastasis FEFO, poreikis, trys gamybos laiko dienos")

## <a name="example-3-simple-fefo-requirement-three-days-of-lead-time-five-sellable-days"></a>3 pavyzdys: Paprastasis FEFO, poreikis, trys gamybos laiko dienos, penkios pardavimo dienos

Šiame pavyzdyje parodyta, kaip veikia laikymo trukmė, kai pridedama prekės pardavimo dienų.

Sistema turi šiuos prekės ir bendrojo plano parametrus:

- **Padengimo kodas (papildymo strategija):** reikalavimas
- **Laikymo trukmė –** 10 dienų
- **Pardavimo dienos:** 5 dienos
- **Gamybos laikas:** 5 dienos
- **Neigiamos dienos:** 0 dienų
- **Suplanuoto užsakymo tipas (numatytieji prekės užsakymo parametrai):** pirkimo užsakymas

Sistemoje yra tokie pardavimo užsakymai:

- **SO1:** kiekis = 2, pageidaujama pristatymo data = šiandien + 2 dienos
- **SO2:** kiekis = 1, pageidaujama pristatymo data = šiandien + 3 dienos
- **SO3:** kiekis = 1, pageidaujama pristatymo data = šiandien + 5 dienos

Šį poreikį gali padengti esamas tiekimas ir patvirtintas pirkimo užsakymas:

- **Turimos atsargos:** turima = šiandien, kiekis = 1, galiojimo data = šiandien + 6 dienos
- **EKA:** gavimo data = šiandien + 2 dienos, kiekis = 3, galiojimo data = šiandien + 10 dienų

Sistema sukuria iškvietimo kandidatų sąrašą, paremtą tiekimo (FEFO) sąrašu ir užimtumo datomis. Todėl turimos atsargos negali įvykdyti SO1, nes tos atsargos baigia galioti prieš pardavimo dienų, kurių reikalauja klientas, pabaigą (pageidaujama gavimo data + 5 dienos). PO1 gali padengti SO1 poreikį dviem vienetais, o SO2 – vienu vienetu. Todėl tik SO3 vis dar nepadengė vieno prekių vieneto poreikio. Šiam reikalavimui patenkinti sistema sukuria tokį suplanuotą pirkimo užsakymą:

- **PP01:** gavimo data = šiandien + 5 dienos, kiekis = 1, galiojimo data = šiandien + 10 dienų

Šioje lentelėje apibendrinami rezultatai.

| Poreikis | Iškvietimas |
|---|---|
| **SO1:** pristatymo data = šiandien + 2 dienos, kiekis = 2 | **EKA:** gavimo data = šiandien + 2 dienos, kiekis = 2, galiojimo data = šiandien + 10 dienų |
| **SO2:** pristatymo data = šiandien + 3 dienos, kiekis = 1 | **EKA:** gavimo data = šiandien + 2 dienos, kiekis = 1, galiojimo data = šiandien + 10 dienų |
| **SO3:** pristatymo data = šiandien + 5 dienos, kiekis = 1 | **TS1:** gavimo data = šiandien + 5 dienos, kiekis = 1, galiojimo data = šiandien + 10 dienų |

Toliau pateikta iliustracija rodo šio pavyzdžio laiko juostą.

![3 pavyzdys: Paprastasis FEFO, poreikis, trys gamybos laiko dienos, penkios pardavimo dienos.](media/fefo-example-3.png "3 pavyzdys: Paprastasis FEFO, poreikis, trys gamybos laiko dienos, penkios pardavimo dienos")

## <a name="example-4-simple-fefo-period-lead-time-depends-on-the-quantity"></a>4 pavyzdys: Paprastasis FEFO, laikotarpis, gamybos laikas, priklauso nuo kiekio

Šis pavyzdys rodo, kaip sistemos bandymas sumažinti vėlavimą kartais gali trukti per daug.

Sistema turi šiuos prekės ir bendrojo plano parametrus:

- **Padengimo kodas (papildymo strategija):** laikotarpis
- **Padengimo laikotarpis:** 10 dienų (lygu laikymo laikotarpiui)
- **Laikymo trukmė –** 10 dienų
- **Pardavimo dienos:** 0 dienų
- **Gamybos laikas:** nustatė šios tiekėjo prekybos sutartys:

    - **1 prekybos sutartis:** jei kiekis = 1, gamybos laikas = 5
    - **2 prekybos sutartis:** jei kiekis = 2, gamybos laikas = 0

- **Neigiamos dienos:** 0 dienų
- **Suplanuoto užsakymo tipas (numatytieji prekės užsakymo parametrai):** pirkimo užsakymas

Sistemoje yra tokie pardavimo užsakymai:

- **SO1:** kiekis = 1, pageidaujama pristatymo data = šiandien
- **SO2:** kiekis = 1, pageidaujama pristatymo data = šiandien + 6 dienos

Šį poreikį iš dalies gali padengti esamas tiekimas iš šių patvirtintų pirkimo užsakymų:

- **EKA:** gavimo data = šiandien + 1 diena, kiekis = 1, galiojimo data = šiandien + 2 dienos
- **EKA:** gavimo data = šiandien + 3 dienos, kiekis = 1, galiojimo data = šiandien + 7 dienos

Sistema turi dvi prekybos sutartis (viena – kiekis = 1, gamybos laikas = 5 dienos, o viena – 2, gamybos laikas = 0 dienų). Todėl sistema mėgina sumažinti atidėjimą, sukurdama tokį suplanuotą pirkimo užsakymą, kuris atitinka antrą prekybos sutartį:

- **PP01:** gavimo data = šiandien, kiekis = 2, galiojimo data = šiandien + 10 dienų

SO1 bus vieną vienetą išINKITĖS 1. SO2 bus taikomas PO2, nes PU2 greit baigs galioti anksčiau nei NE1.

Šioje lentelėje apibendrinami rezultatai.

| Poreikis | Iškvietimas |
|---|---|
| **SO1:** pristatymo data = šiandien, kiekis = 1 | **DAT1:** Gavimo data = šiandien, kiekis = 1, galiojimo data = šiandien + 10 dienų |
| **SO2:** pristatymo data = šiandien + 6 dienos, kiekis = 1 | **EKA:** gavimo data = šiandien + 3 dienos, kiekis = 1, galiojimo data = šiandien + 7 dienos |

> [!NOTE]
> PO1 naudojamas, nes jis bus pristatytas per vėlai S01 ir baigs galioti prieš pristatęs S02. VZ., TS1 per daug užsakė vieną vienetą, kad gamybos laikas būtų 0 (nulis), pagal 2 prekybos sutartį.

Toliau pateikta iliustracija rodo šio pavyzdžio laiko juostą.

![4 pavyzdys: Paprastasis FEFO, laikotarpis, gamybos laikas, priklauso nuo kiekio.](media/fefo-example-4.png "4 pavyzdys: Paprastasis FEFO, laikotarpis, gamybos laikas, priklauso nuo kiekio")

## <a name="example-5-simple-fefo-requirement-10-negative-days"></a>5 pavyzdys: PaprastasIS FEFO, reikalavimas, 10 neigiamų dienų

<!-- KFM: This is more of a negative days example than a shelf life example. We should point out more explicitly how shelf life affects this situation (or maybe otherwise remove this example). -->

Šis pavyzdys rodo, kaip veikia laikymo trukmė, kai prekei pridedamas daug neigiamų dienų. Neigiamos dienos yra dienų skaičius, kurį norite laukti prieš užsakę prekės, kurios atsargų neigiamas, papildymą. Sistema nesukuria tiekimo, nebent viršijamas neigiamų dienų skaičius.

Sistema turi šiuos prekės ir bendrojo plano parametrus:

- **Padengimo kodas (papildymo strategija):** reikalavimas
- **Gamybos laikas:** 0 dienų
- **Neigiamos dienos:** 10 dienų
- **Suplanuoto užsakymo tipas (numatytieji prekės užsakymo parametrai):** pirkimo užsakymas

Sistemoje yra toks pardavimo užsakymas:

- **SO1:** kiekis = 1, pageidaujama pristatymo data = šiandien

Šį poreikį gali padengti dabartinis tiekimas iš šio patvirtintų pirkimo užsakymų:

- **EKA:** gavimo data = šiandien + 3 dienos, kiekis = 1, galiojimo data = šiandien + 5 dienos

Kadangi sistema sukonfigūruota leisti 10 neigiamų dienų, ji padengia SO1 poreikį naudodama PO1, net jei rezultatas bus trijų dienų atidėjimas, nes SO1 sukurs neigiamas atsargas, kol BUS pristatyta PO1. Nėra sukurtas suplanuotas pirkimo užsakymas, net jei gamybos laikas yra 0 (nulis), todėl suplanuoto pirkimo užsakymo kūrimas sumažins vėlavimą.

Šioje lentelėje apibendrinami rezultatai.

| Poreikis | Iškvietimas |
|---|---|
| **SO1:** pristatymo data = šiandien, kiekis = 1 | **EKA:** gavimo data = šiandien + 3 dienos, kiekis = 1, galiojimo data = šiandien + 5 dienos |

Toliau pateikta iliustracija rodo šio pavyzdžio laiko juostą.

![5 pavyzdys: PaprastasIS FEFO, reikalavimas, 10 neigiamų dienų.](media/fefo-example-5.png "5 pavyzdys: PaprastasIS FEFO, reikalavimas, 10 neigiamų dienų")

## <a name="example-6-simple-fefo-requirement-five-negative-days"></a>6 pavyzdys: PaprastasIS FEFO, reikalavimas, penkios neigiamos dienos

Šiame pavyzdyje parodyta, kaip veikia laikymo trukmė, kai prekės neigiamų dienų skaičius yra mažesnis nei jos laikymo laikotarpis.

Sistema turi šiuos prekės ir bendrojo plano parametrus:

- **Padengimo kodas (papildymo strategija):** reikalavimas
- **Pardavimo dienos:** 0 dienų
- **Gamybos laikas:** 0 dienų
- **Neigiamos dienos:** 5 dienos
- **Suplanuoto užsakymo tipas (numatytieji prekės užsakymo parametrai):** pirkimo užsakymas

Sistemoje yra toks pardavimo užsakymas:

- **SO1:** kiekis = 2, pageidaujama pristatymo data = šiandien

Šį poreikį gali padengti esamas tiekimas iš šių patvirtintų pirkimo užsakymų:

- **EKA:** gavimo data = šiandiena, kiekis = 1, galiojimo data = šiandien + 1 diena
- **EKA:** gavimo data = šiandien + 2 dienos, kiekis = 1, galiojimo data = šiandien + 3 dienos

Tačiau sistema turi laikytis apribojimo, kad išsiųstų prekių galiojimo laikas siuntos metu negali būti pasibaigęs. Todėl SO1 negalima naudoti ir PO2, ir PO1, nes PO1 galiojimo laikas baigiasi prieš PU2 atvykimą. Sistema sukuria šį suplanuotą pirkimo užsakymą, kad būtų užbaigtas so1 poreikis:

- **DAT1:** Gavimo data = šiandien, kiekis = 1, galiojimo data = šiandien + 10 dienų

Sistema gali pasinaudoti penkiomis neigiamomis dienomis ir naudoti PO2 bei OF1, kad padengtų SO1. Tačiau dėl šio požiūrio pristatymas bus atidėtas, kol bus pristatyta po2, o PO1 kol kas baigs galioti. Todėl sistema padengia SO1 naudodamaVZ1 ir PO1.

Šioje lentelėje apibendrinami rezultatai.

| Poreikis | Iškvietimas |
|---|---|
| **SO1:** pristatymo data = šiandien, kiekis = 2 | <p>**EKA:** gavimo data = šiandiena, kiekis = 1, galiojimo data = šiandien + 1 diena</p><p>**DAT1:** Gavimo data = šiandien, kiekis = 1, galiojimo data = šiandien + 10 dienų</p> |

Toliau pateikta iliustracija rodo šio pavyzdžio laiko juostą.

![6 pavyzdys: Paprastasis FEFO, poreikis, penkios neigiamos dienos.](media/fefo-example-6.png "6 pavyzdys: PaprastasIS FEFO, reikalavimas, penkios neigiamos dienos")
