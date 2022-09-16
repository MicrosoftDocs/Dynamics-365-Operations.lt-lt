---
title: Siuntos konsolidacijos strategijų konfigūravimas
description: Šiame straipsnyje paaiškinama, kaip nustatyti numatytąsias ir pasirinktines siuntos konsolidavimo strategijas.
author: Mirzaab
ms.date: 09/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0312d425d2ebc5311e894030423a916b90f1881a
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427988"
---
# <a name="configure-shipment-consolidation-policies"></a>Siuntos konsolidacijos strategijų konfigūravimas

[!include [banner](../includes/banner.md)]

Siuntos konsolidacijos procesas, naudojantis siuntos konsolidacijos strategijas, sudaro galimybę automatizuotai siuntos konsolidacijai automatizuoto ir rankinio paleidimo į sandėlį metu. Įjungę šią funkciją, turite sukonfigūruoti pradines strategijas. Jei strategijos nesukonfigūruotos, kiekviena pardavimo eilutė sugeneruos atskirą siuntą, turinčią vieną krovinio eilutę.

Scenarijai, pateikti šiame straipsnyje, parodo, kaip nustatyti numatytąsias ir pasirinktines siuntos konsolidavimo strategijas.

> [!WARNING]
> Jei atnaujinsite "Microsoft Dynamics 365 Supply Chain Management " sistemą, kurioje naudojate siuntos konsolidavimo funkciją, konsolidavimas gali nustoti veikti taip, kaip tikitės, nebent vadovausitės čia pateikta patarimami.
>
> Tiekimo grandinės valdymo *diegimuose* **, kuriuose siuntos konsolidavimo strategijos priemonė išjungta,** įgalinate siuntos konsolidavimą naudodami kiekvieno atskiro sandėlio konsoliduotos siuntos parametrus išleidžiant į sandėlį. Ši funkcija privaloma versijoje 10.0.29. Kai jis įjungtas, **konsoliduota** siunta išleidžiant ją į sandėlį tampa paslėpta, *o* funkcija pakeičiama siuntos konsolidavimo strategija, aprašytomis šiame straipsnyje. Kiekviena strategija nustato konsolidavimo taisykles ir pateikia užklausą, kuri kontroliuoja, kur taikoma strategija. Kai pirmą kartą įjungsite funkciją, siuntos konsolidavimo strategijų puslapyje nebus nurodyta **jokia siuntos konsolidavimo** strategija. Kai strategijos apibrėžiamos, sistema naudoja senesnį veikimo būdą. Todėl kiekvienas esamas sandėlis laikosi jos **Konsoliduotos siuntos išleidžiant į** sandėlį parametro, net jei šis parametras dabar paslėptas. Tačiau, kai sukuriate bent vieną siuntos konsolidavimo strategiją, **konsoliduotos** siuntos išleidžiant į sandėlį parametrai nebegalioja, o konsolidavimo funkciją visiškai kontroliuoja strategijos.
>
> Nustačius bent vieną siuntos konsolidavimo strategiją, sistema kiekvieną kartą, kai užsakymas išleidžiamas į sandėlį, patikrins konsolidavimo strategijas. Sistema apdoroja strategijas naudodama rangą, kuris apibrėžiamas kiekvienos strategijos strategijos **sekos** verte. Ji taiko pirmąją strategiją, pagal kurią užklausa atitinka naują užsakymą. Jei jokios užklausos nesutampa su užsakymu, kiekviena užsakymo eilutė sugeneruoja atskirą siuntą, turiinę vieną krovinio eilutę. Todėl, kaip atsarginę, rekomenduojame sukurti numatytąją strategiją, kuri taikoma visiems sandėliams ir grupėms pagal užsakymo numerį. Suteikti šiai atsarginei strategijai **aukščiausią** strategijos sekos reikšmę, kad ji būtų apdorota paskutinė.
>
> Norėdami perkurti senstelėjusį elgseną, turite sukurti strategiją, kuri negrupuoti pagal užsakymo numerį ir kuri turi užklausos kriterijus, kuriuose nurodyti visi atitinkami sandėliai.

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>Siuntos konsolidacijos strategijų funkcijos įjungimas

Norėdami naudoti siuntos *konsolidavimo strategijos* funkciją, ją turite įjungti savo sistemoje. Kaip ir tiekimo grandinės valdymo versija 10.0.29, ši funkcija yra privaloma ir jos išjungti negalima. Jei naudojate senesnę nei 10.0.29 versiją, tada *·*[administratoriai gali įjungti arba išjungti šią funkciją ieškodami siuntos konsolidavimo strategijų funkcijos funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo srityje.

## <a name="set-up-your-initial-consolidation-policies"></a><a name="initial-policies"></a> Nustatykite pradines konsolidacijos strategijas

Jei dirbate su *nauja* sistema arba sistema, kurioje pirmą kartą ką tik įjungta siuntos konsolidavimo strategijų funkcija, norėdami nustatyti pradines siuntos konsolidavimo strategijas, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Išleidimas į sandėlį \> Siuntos konsolidacijos strategijos**.
1. Veiksmų srityje pasirinkite **Kurti numatytąją sąranką**, kad sukurtumėte tolesnes strategijas.

    - Strategija, kurios tipas Pardavimo *užsakymų* strategija *yra* Numatytoji.
    - Strategija, kurios tipas Perkėlimo *išdavimo* strategija *yra* numatytoji.
    - Strategija, kurios perkėlimo išdavimo *strategijos tipo pavadinimas* CrossOrder *·*. (Ši strategija sukuriama tik tada, jei esate turėję bent vieną sandėlį, kuriame yra senesnė nei **Įgalintas siuntos konsolidavimas išleidžiant į sandėlį** .)
    - Strategija, kurios tipas yra *Pardavimo užsakymų strategijos* pavadinimas *CrossOrder*. (Ši strategija sukuriama tik tada, jei esate turėję bent vieną sandėlį, kuriame yra senesnė nei **Įgalintas siuntos konsolidavimas išleidžiant į sandėlį** .)

    > [!NOTE]
    > - Abi *CrossOrder strategijos* turi atsižvelgti į tą patį laukų rinkinį kaip ir ankstesnė logika. Tačiau jie taip pat atsižvelkite į užsakymo numerio lauką. (Šis laukas naudojamas norint konsoliduoti eilutes į siuntas, remiantis tokiais veiksniais kaip sandėlis, pristatymo transportavimo būdas ir adresas.)
    > - Abi *numatytosios* strategijos turi atsižvelgti į tą patį laukų rinkinį kaip ir ankstesnė logika. Tačiau jie taip pat atsižvelkite į užsakymo numerio lauką. (Šis laukas naudojamas norint konsoliduoti eilutes į siuntas, remiantis tokiais veiksniais kaip užsakymo numeris, sandėlis, pristatymo transportavimo būdas ir adresas.)

1. Jei sistema pardavimo užsakymų *strategijos tipui sugeneravo* *CrossOrder* strategiją, pasirinkite ją, tada veiksmų srityje pasirinkite Redaguoti **užklausą**. Užklausų doroklyje galite matyti, kuriems **iš** jūsų sandėlių anksčiau buvo įgalinti sandėlio parametrai Konsoliduoti siuntą išleidžiant į sandėlį. Todėl ši strategija iš naujo sukurs ankstesnius šių sandėlių parametrus.
1. Pritaikykite naujas numatytąsias strategijas pagal tai, kaip reikia, pridėdami arba pašalindami laukus ir (arba) redaguodami užklausas. Taip pat galite įtraukti tiek naujų strategijų, kiek jums reikia. Pavyzdžių, kurie parodo, kaip pritaikyti ir konfigūruoti savo strategijas, ieškokite toliau šiame straipsnyje pateiktame pavyzdyje.

## <a name="scenario-configure-custom-shipment-consolidation-policies"></a>Scenarijus: konfigūruoti pasirinktines siuntimo konsolidavimo strategijas

Šiame scenarijuje pateikiamas pavyzdys, kuriame parodyta, kaip nustatyti pasirinktines siuntos konsolidavimo strategijas ir patikrinti jas naudojant demonstracinius duomenis. Pasirinktinės strategijos gali palaikyti sudėtingus verslo poreikius, kai siuntos konsolidacija priklauso nuo kelių sąlygų. Kiekviename tolesniame šio scenarijaus strategijos pavyzdyje įtrauktas trumpas verslo atvejo aprašymas. Šias pavyzdines strategijas reikia nustatyti seka, užtikrinančia piramidės tipo užklausų vertinimą. (Kitaip tariant, strategijos, turinčios daugiausiai sąlygų, turi būti vertinamos kaip turinčios didžiausią prioritetą.)

### <a name="make-demo-data-available"></a>Demonstracinių duomenų įgalinimas

Šis scenarijus nurodo vertes ir įrašus, įtrauktus į standartinius demonstracinius [duomenis](../../fin-ops-core/fin-ops/get-started/demo-data.md), kurie pateikiami tiekimo grandinės valdymui. Jei norite naudoti čia pateiktas reikšmes atlikdami pratimus, įsitikinkite, kad dirbate aplinkoje, kurioje įdiegti demonstraciniai duomenys, ir prieš pradėdami nustatykite juridinį subjektą į *USMF*.

### <a name="prepare-master-data-for-this-scenario"></a>Parengti šio scenarijaus pagrindinius duomenis

Prieš pradėdami atlikti šio scenarijaus užduotis, turite paruošti pagrindinius duomenis, reikalingus filtravimui atlikti, kaip aprašyta toliau aprašytus poskyrius. (Šios būtinosios sąlygos taip pat taikomos scenarijams, kurie išvardyti [Pavyzdiniai scenarijai, kaip naudoti siuntos konsolidavimo strategijų skyrių](#example-scenarios) .)

#### <a name="create-two-new-product-filter-codes"></a>Dviejų naujų produktų filtravimo kodų kūrimas

1. Eikite į **Sandėlio valdymas \> Sąranka \> Produktų filtrai \> Produktų filtrai** ir įtraukite du tolesnius produktų filtrus.

    - 1 produktų filtras:

        - **Filtro kodas:** *Degus*
        - **Filtro pavadinimas:** *4 kodas*

    - 2 produktų filtras:

        - **Filtro kodas:** *Sprogus*
        - **Filtro pavadinimas:** *4 kodas*

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.
1. Atidarykite produktą, kurio prekės numeris yra *M9200*. (Pasirinktam produktui turi būti įjungtas išplėstinių sandėlio \[WMS\] procesų naudojimas ir šiam produktui iš anksto įjungtas **USMF** demonstracinių duomenų WMS procesų naudojimas.)
1. „FastTab” **Sandėlis** nustatykite lauką **4 kodas** į *Degus*.
1. Uždarykite puslapį.
1. Atidarykite produktą, kurio prekės numeris yra *M9201*. (Šiam produktui taip pat iš anksto įjungtas **USMF** demonstracinių duomenų WMS procesų naudojimas.)
1. „FastTab” **Sandėlis** nustatykite lauką **4 kodas** į *Sprogus*.
1. Uždarykite puslapį.

#### <a name="create-a-new-transportation-mode-of-delivery"></a>Naujo pristatymo transportavimo būdo kūrimas

1. Eikite į **Transportavimo valdymas \> Sąranka \> Vežėjai \> Būdas**.
1. Sukurkite transportavimo būdą, kuris bus naudojamas konsolidavimo užklausose, ir pavadinkite jį *Oro keliai*.
1. Eikite į **Transportavimo valdymas \> Nustatymas \> Vežėjai \> Siuntų vežėjai**.
1. Sukurkite vežėją, kuriam nustatyti tolesni parametrai.

    - **Siuntos vežėjas:** *oro keliai*
    - **Pavadinimas:** *Oro keliai*
    - **Būdas:** *oro keliai*

1. Naujo vežėjo „FastTab” **Paslaugos** įtraukite eilutę, kurioje yra tolesni parametrai.

    - **Vežėjo paslauga:** *oro*
    - **Transportavimo būdas:** *oru*

1. Veiksmų srityje pasirinkite **Įrašyti**.

    > [!NOTE]
    > Kai įrašote naują vežėją, naujos tinklelio **Paslaugos** eilutės laukas **Pristatymo būdas** automatiškai nustatomas į *Airwa-Air*. Kai naudojate pardavimo užsakymo pristatymo būdą *Airwa-Air*, transportavimo būdas *Oro keliai* bus naudojamas susijusioms siuntoms.

#### <a name="create-an-order-pool"></a>Užsakymų telkinio kūrimas

1. Eikite į **Pardavimas ir rinkodara \> Sąranka \> Pardavimo užsakymai \> Užsakymų telkiniai**.
1. Sukurkite užsakymų telkinį, kuris bus naudojamas konsolidavimo užklausoje. Šiame užsakymų telkinyje turi būti nustatyti tolesni parametrai.

    - **Telkinys:** įveskite sveikąjį skaičių, kuris nenaudojamas jokiame kitame telkinyje.
    - **Pavadinimas:** *ShipCons*

1. Eikite į **Pardavimas ir rinkodara \> Klientai \> Visi klientai**.
1. Atidarykite klientą, kurio sąskaitos numeris yra *US-003*.
1. „FastTab” **Pardavimo užsakymo numatytieji nustatymai** nustatykite lauką **Pardavimo užsakymų telkinys** į ką tik sukurtą užsakymų telkinį.
1. Uždarykite puslapį, tada pakartokite 4 ir 5 žingsnius kliento, kuris turi sąskaitos numerį *JAV-004*.

### <a name="create-example-policy-1"></a>1 strategijos pavyzdžio kūrimas

Šiame pavyzdyje sukursite strategiją *Klientas + Būdas*, kuri galės būti naudojama tolesniais verslo atvejais.

- Strategija pateiks užklausą konkrečiai kliento sąskaitai (*US-001*) ir konkrečiam pristatymo būdui (*Airwa-Air*).
- Konsolidacija su atviromis siuntomis yra išjungta.
- Konsolidacija atliekama pagal užsakymo ID. (Kitaip tariant, bus atskiros siuntos pagal užsakymą, sandėlį ir t. t.)

Atlikite šiuos veiksmus, norėdami sukurti šio verslo atvejo siuntos konsolidacijos strategiją.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Išleidimas į sandėlį \> Siuntos konsolidacijos strategijos**.
1. Nustatykite lauką **Strategijos tipas** į *Pardavimo užsakymai*.
1. Veiksmų srityje pasirinkite **Naujas**, norėdami sukurti strategiją, turinčią tolesnius parametrus.

    - **Strategijos pavadinimas:** *CustomerMode*
    - **Strategijos aprašymas:** *kliento sąskaita ir pristatymo būdas*

1. Parinktį **Konsoliduoti su atviromis siuntomis** palikite nustatytą į *Ne*.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. „FastTab” **Konsolidavimo laukai** sąraše **Likę laukai** pasirinkite eilutę, kurioje laukas **Lauko pavadinimas** nustatytas į *Pristatymo būdas*.
1. Pasirinkite mygtuką **Įtraukti** ![Rodyklė dešinėn.](media/forward-button.png) lauko perkėlimui į **Pasirinkti laukai** sąrašą.
1. Veiksmų srityje pasirinkite **Redaguoti užklausą**.
1. Užklausos rengyklės dialogo lango skirtuko **Diapazonas** tinklelyje raskite eilutę, kurioje laukas **Laukas** nustatytas į *Kliento sąskaita*, ir nustatykite tos eilutės lauką **Kriterijai** į *US-001*.
1. Pasirinkite **Įtraukti**, norėdami įtraukti eilutę, kuriai nustatyti tolesni parametrai, į tinklelį.

    - **Lentelė:** *užsakymo eilutės*
    - **Išvestinė lentelė:** *užsakymo eilutės*
    - **Laukas:** *pristatymo būdas*
    - **Kriterijai:** *Airwa-Air*

1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.

> [!NOTE]
> Šiuo verslo atveju kliento *US-001* užsakymo eilutės, naudojančios pristatymo būdą *Airwa-Air*, nebus konsoliduojamos užsakymuose. Ši strategija turi būti pirmiausia naudojama eilės tvarka tais atvejais, kai šio kliento visų kitų pristatymo būdų siuntos yra konsoliduojamos.

### <a name="create-example-policy-2"></a>2 strategijos pavyzdžio kūrimas

Šiame pavyzdyje sukursite strategiją *Pavojingos prekės*, kuri galės būti naudojama tolesniais verslo atvejais.

- Strategija pateiks užklausą konkrečiam filtro kodui (*pavojingas*) ir konkrečiam pristatymo būdui (*Airwa-Air*).
- Konsolidacija su atviromis siuntomis yra įjungta.
- Konsolidacija atliekama užsakymuose. (Kitaip tariant, bus atskiros siuntos pagal sąskaitą, sandėlį ir t. t., bet tik užklausoje nurodytoje prekių grupėje.)

Atlikite šiuos veiksmus, norėdami sukurti šio verslo atvejo siuntos konsolidacijos strategiją.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Išleidimas į sandėlį \> Siuntos konsolidacijos strategijos**.
1. Nustatykite lauką **Strategijos tipas** į *Pardavimo užsakymai*.
1. Veiksmų srityje pasirinkite **Naujas**, norėdami sukurti strategiją, turinčią tolesnius parametrus.

    - **Strategijos pavadinimas:** *Prekės tipas*
    - **Strategijos aprašymas:** *konsoliduoti to pačio tipo prekę užsakymuose*

1. Nustatykite parinktį **Konsoliduoti su atviromis siuntomis** į *Taip*.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. „FastTab” **Konsolidavimo laukai** sąraše **Likę laukai** pasirinkite eilutę, kurioje laukas **Lauko pavadinimas** nustatytas į *Pristatymo būdas*.
1. Pasirinkite mygtuką **Įtraukti** ![Rodyklė dešinėn.](media/forward-button.png) lauko perkėlimui į **Pasirinkti laukai** sąrašą.
1. Veiksmų srityje pasirinkite **Redaguoti užklausą**.
1. Užklausos rengyklės dialogo lango skirtuko **Sujungimai** medyje išplėskite ir pasirinkite **Lentelės \> Krovinio informacija**.
1. Pasirinkite **Įtraukti lentelės sujungimą**.
1. Atsiradusiame ryšių tinklelyje raskite ir pasirinkite eilutę, kurioje laukas **Ryšys** nustatytas į *Sandėlio prekės numeris (prekės numeris)*, tada pasirinkite **Pasirinkti**. 
1. Skirtuke **Diapazonas** pasirinkite **Įtraukti**, kad įtrauktumėte eilutę, kuriai nustatyti tolesni parametrai, į tinklelį.

    - **Lentelė:** *sandėlio prekės numeris*
    - **Išvestinė lentelė:** *sandėlio prekės numeris*
    - **Laukas:** *4 kodas*
    - **Kriterijai:** *degus*

1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.

> [!NOTE]
> Šiuo verslo atveju visos užsakymo eilutės, kuriose prekės turi konkretų filtro kodą (t. y. filtro kodą, kuriame laukas **4 kodas** nustatytas į *Degus*), bus konsoliduojamos su kitomis to paties tipo prekėmis užsakymuose. Jei toje pačioje sąskaitoje, sandėlyje ir prekių grupėje yra atvira siunta, prie jos bus pridėtos naujos eilutės.

### <a name="create-example-policy-3"></a>3 strategijos pavyzdžio kūrimas

Šiame pavyzdyje sukursite strategiją *Klientų reikalavimai*, kuri galės būti naudojama tolesniais verslo atvejais.

- Strategija pateiks užklausą konkrečiai kliento sąskaitai.
- Konsolidacija su atviromis siuntomis yra įjungta.
- Konsolidacija atliekama užsakymuose remiantis kliento paraiškomis. (Kitaip tariant, keli užsakymai bus sugrupuoti į siuntas pagal tą patį kliento paraiškos numerį ir sandėlį.)

Atlikite šiuos veiksmus, norėdami sukurti šio verslo atvejo siuntos konsolidacijos strategiją.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Išleidimas į sandėlį \> Siuntos konsolidacijos strategijos**.
1. Nustatykite lauką **Strategijos tipas** į *Pardavimo užsakymai*.
1. Veiksmų srityje pasirinkite **Naujas**, norėdami sukurti strategiją, turinčią tolesnius parametrus.

    - **Strategijos pavadinimas:** *CustomerOrderNo*
    - **Strategijos aprašymas:** *konsoliduoti eilutes pagal kliento PU*

1. Nustatykite parinktį **Konsoliduoti su atviromis siuntomis** į *Taip*.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. „FastTab” **Konsolidavimo laukai** sąraše **Likę laukai** pasirinkite eilutę, kurioje laukas **Lauko pavadinimas** nustatytas į *Kliento paraiška*.
1. Pasirinkite mygtuką **Įtraukti** ![Rodyklė dešinėn.](media/forward-button.png) lauko perkėlimui į **Pasirinkti laukai** sąrašą.
1. Sąraše **Likę laukai** pasirinkite eilutę, kurioje laukas **Lauko pavadinimas** nustatytas į *Pristatymo būdas*.
1. Pasirinkite mygtuką **Įtraukti** ![Rodyklė dešinėn.](media/forward-button.png) lauko perkėlimui į **Pasirinkti laukai** sąrašą.
1. Veiksmų srityje pasirinkite **Redaguoti užklausą**.
1. Užklausos rengyklės dialogo lango skirtuke **Diapazonas** raskite eilutę, kurioje laukas **Laukas** nustatytas į *Kliento sąskaita*, ir nustatykite tos eilutės lauką **Kriterijai** į *US-001*.
1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.

> [!NOTE]
> Šiuo verslo atveju visos užsakymo eilutės, kuriose pardavimo užsakymai turi tą patį kliento paraiškos numerį, bus konsoliduojamos į vieną siuntą, neatsižvelgiant į pardavimo užsakymo numerį. (Kliento paraiškos numeris naudojamas kaip kliento pirkimo užsakymo \[PU\] numeris.) Jei toje pačioje sąskaitoje, sandėlyje ir kliento paraiškoje yra atvira siunta, prie jos bus pridėtos naujos eilutės. Ši strategija gali būti naudojama, jei klientas kelis kartus per dieną siunčia papildomas užsakymo eilutes, turinčias tą patį PU numerį, ir nori visas eilutes sugrupuoti į vieną siuntą. (Kitaip tariant, bus vienas važtaraštis (bill of lading) ir vienas važtaraštis (packing slip).)

### <a name="create-example-policy-4"></a>4 strategijos pavyzdžio kūrimas

Šiame pavyzdyje sukursite strategiją *Klientai, leidžiantys konsolidaciją*, kuri galės būti naudojama tolesniais verslo atvejais.

- Strategija pateiks užklausą konkrečiam užsakymų telkiniui, kad galėtų nustatyti klientus, priimančius konsoliduotas siuntas.
- Konsolidacija su atviromis siuntomis yra išjungta.
- Konsolidacija atliekama užsakymuose naudojant laukus, pasirinktus pagal numatytąją „CrossOrder“ strategiją (kad būtų dubliuotas pirmiau naudotas žymės langelis **Konsoliduoti siuntą išleidžiant ją į sandėlį**).

- Galite nepaisyti pardavimo užsakymo taisyklės pasirinkdami kitą užsakymų telkinį.

Atlikite šiuos veiksmus, norėdami sukurti šio verslo atvejo siuntos konsolidacijos strategiją.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Išleidimas į sandėlį \> Siuntos konsolidacijos strategijos**.
1. Nustatykite lauką **Strategijos tipas** į *Pardavimo užsakymai*.
1. Veiksmų srityje pasirinkite **Naujas**, norėdami sukurti strategiją, turinčią tolesnius parametrus.

    - **Strategijos pavadinimas:** *Užsakymų telkinys*
    - **Strategijos aprašymas:** *konsoliduoti užsakymuose pagal užsakymų telkinį*

1. Parinktį **Konsoliduoti su atviromis siuntomis** palikite nustatytą į *Ne*.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. „FastTab” **Konsolidavimo laukai** sąraše **Likę laukai** pasirinkite eilutę, kurioje laukas **Lauko pavadinimas** nustatytas į *Pristatymo būdas*.
1. Pasirinkite mygtuką **Įtraukti** ![Rodyklė dešinėn.](media/forward-button.png) lauko perkėlimui į **Pasirinkti laukai** sąrašą.
1. Veiksmų srityje pasirinkite **Redaguoti užklausą**.
1. Užklausos rengyklės dialogo lango skirtuke **Diapazonas** pasirinkite **Įtraukti**, kad įtrauktumėte eilutę, kuriai nustatyti tolesni parametrai, į tinklelį.

    - **Lentelė:** *pardavimo užsakymai*
    - **Išvestinė lentelė:** *pardavimo užsakymai*
    - **Laukas:** *telkinys*
    - **Kriterijai:** *ShipCons*

1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.

> [!NOTE]
> Šiuo verslo atveju visos užsakymo eilutės, kuriose pardavimo užsakymai priklauso tam pačiam užsakymų telkiniui, bus konsoliduojamos į vieną siuntą toje pačioje sąskaitoje, sandėlyje ir pristatymo transportavimo būde pardavimo užsakymuose. Vietoj užsakymų telkinio galite naudoti bet kurį kitą lauką, norėdami atskirti klientų grupes ir pagal numatytuosius nustatymus naudoti pardavimo užsakymo antraštę. Galite naudoti šį būdą, jei klientas, o ne sandėlis, reiškia konsolidavimo poreikį. (Ankstesnėje konsolidacijos logikoje sandėlis reiškė konsolidavimo poreikį.)

### <a name="create-example-policy-5"></a>5 strategijos pavyzdžio kūrimas

Šiame pavyzdyje sukursite strategiją *Sandėliai, leidžiantys konsolidaciją*, kuri galės būti naudojama tolesniais verslo atvejais.

- Strategija pateiks užklausą konkrečiam užsakymų telkiniui, kad galėtų nustatyti sandėlius, galinčius konsoliduoti siuntas.
- Konsolidacija su atviromis siuntomis yra išjungta.
- Konsolidacija atliekama užsakymuose naudojant laukus, pasirinktus pagal numatytąją „CrossOrder“ strategiją (kad būtų dubliuotas pirmiau naudotas žymės langelis **Konsoliduoti siuntą išleidžiant ją į sandėlį**).

Paprastai šis verslo atvejis gali būti išspręstas naudojant numatytąsias strategijas, kurias sukūrėte pradinėse [konsolidacijos strategijose](#initial-policies). Tačiau taip pat galite rankiniu būdu sukurti panašias strategijas atlikdami tolesnius veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Išleidimas į sandėlį \> Siuntos konsolidacijos strategijos**.
1. Nustatykite lauką **Strategijos tipas** į *Pardavimo užsakymai*.
1. Veiksmų srityje pasirinkite **Naujas**, norėdami sukurti strategiją, turinčią tolesnius parametrus.

    - **Strategijos pavadinimas:** *Keli užsakymai*
    - **Strategijos aprašymas:** *konkrečių sandėlių kelių užsakymų konsolidacija*

1. Parinktį **Konsoliduoti su atviromis siuntomis** palikite nustatytą į *Ne*.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. „FastTab” **Konsolidavimo laukai** lauke **Likę laukai** pasirinkite eilutę, kurioje laukas **Lauko pavadinimas** nustatytas į *Pristatymo būdas*.
1. Pasirinkite mygtuką **Įtraukti** ![Rodyklė dešinėn.](media/forward-button.png) lauko perkėlimui į **Pasirinkti laukai** sąrašą.
1. Veiksmų srityje pasirinkite **Redaguoti užklausą**.
1. Užklausos rengyklės dialogo lango skirtuke **Diapazonas** raskite eilutę, kurioje laukas **Laukas** nustatytas į *Sandėlis*, ir nustatykite tos eilutės lauką **Kriterijai** į *61, 63*.
1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.

### <a name="set-the-order"></a>Užsakymo nustatymas

Dabar, kai sukūrėte visas strategijas, turite nustatyti tvarką, kuria jos bus taikomos. Norėdami naudoti piramidės tipo būdą, kai strategijos, turinčios daugiausiai sąlygų, vertinamos kaip turinčios didžiausią prioritetą, atlikite tolesnius veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Išleidimas į sandėlį \> Siuntos konsolidacijos strategijos**.
1. Nustatykite lauką **Strategijos tipas** į *Pardavimo užsakymai*.
1. Pasirinkite kiekvieną strategiją, nurodytą kairiajame stulpelyje, tada veiksmų srityje naudokite mygtukus **Perkelti aukštyn** ir **Perkelti žemyn**, kad strategijos būtų išdėstytos tolesne tvarka.

    1. CustomerMode
    1. Prekės tipas
    1. CustomerOrderNo
    1. Užsakymų telkinys
    1. Keli užsakymai
    1. Numatyta

## <a name="example-scenarios-of-how-to-use-shipment-consolidation-policies"></a><a name="example-scenarios"></a> Scenarijų, kaip naudoti siuntų konsolidacijos strategijas, pavyzdžiai

Toliau pateiktame scenarijuje iliustruojama, kaip galite naudoti siuntos konsolidavimo strategijas, kurias sukūrėte skaitant šį straipsnį. Kiekvienas scenarijus apžvelgia siuntos konsolidacijos procesą, naudojantį siuntos konsolidacijos strategijas automatizuoto ar rankinio paleidimo į sandėlį metu.

- 1 scenarijus: [siuntų konsolidacija jas paleidus į sandėlį naudojant automatinį pardavimo užsakymų išleidimą](../warehousing/consolidate-shipments-automatic.md)
- 2 scenarijus: [siuntų konsolidacija, kai siuntos konsolidacijos strategija perrašyta iš išleidimo į sandėlio puslapį](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- 3 scenarijus: [siuntų konsolidacija naudojant išleidimą į sandėlį iš krovinio planavimo darbo srities](../warehousing/consolidate-shipments-load-planning-workbench.md)
- 4 scenarijus: [siuntų konsolidacija naudojant siuntų konsolidacijos darbo sritį](../warehousing/consolidate-shipments-manual-workbench.md)
- 5 scenarijus: [siuntų konsolidacija rankiniu būdu naudojant puslapį Konsoliduoti siuntas](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>Papildomi ištekliai

- [Siuntos konsolidavimo strategijų peržiūra](about-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
