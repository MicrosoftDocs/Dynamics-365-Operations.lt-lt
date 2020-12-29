---
title: Siuntos konsolidacijos strategijų konfigūravimas
description: Šioje temoje paaiškinama, kaip nustatyti numatytąsias ir pasirinktines siuntos konsolidacijos strategijas.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: adb88bbd29a89a1d18d7fd4781c2541ffb4e721f
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433937"
---
# <a name="configure-shipment-consolidation-policies"></a>Siuntos konsolidacijos strategijų konfigūravimas

[!include [banner](../includes/banner.md)]

Siuntos konsolidacijos procesas, naudojantis siuntos konsolidacijos strategijas, sudaro galimybę automatizuotai siuntos konsolidacijai automatizuoto ir rankinio paleidimo į sandėlį metu. Įjungę šią funkciją, turite sukonfigūruoti pradines strategijas. Jei strategijos nesukonfigūruotos, kiekviena pardavimo eilutė sugeneruos atskirą siuntą, turinčią vieną krovinio eilutę.

Šioje temoje pateikiami scenarijai rodo, kaip nustatyti numatytąsias ir pasirinktines siuntos konsolidacijos strategijas.

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>Siuntos konsolidacijos strategijų funkcijos įjungimas

> [!IMPORTANT]
> Pagal [pirmąjį scenarijų](#scenario-1), aprašytą šioje temoje, pirmiausia nustatysite sandėlį, kad jis naudotų ankstesnę siuntos konsolidacijos funkciją. Tada padarysite siuntos konsolidacijos strategijas pasiekiamomis. Tokiu būdu galite išbandyti naujinimo scenarijaus veikimą. Jeigu planuojate naudoti demonstracinių duomenų aplinką pirmojo scenarijaus vykdyme, neįjunkite funkcijos prieš scenarijaus vykdymą.

Kad galėtumėte naudoti funkciją *Siuntos konsolidacijos strategijos*, turite ją įjungti jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *sandėlio valdymas*
- **Funkcijos pavadinimas:** *Konsoliduoti siuntą*

## <a name="make-demo-data-available"></a>Leidimas naudoti demonstracinius duomenis

Kiekvienas šioje temoje esantis scenarijus nurodo reikšmes ir įrašus, įtrauktus į standartinius „Microsoft Dynamics 365 Supply Chain Management” demonstracinius duomenis. Jei norite naudoti čia pateiktas reikšmes atlikdami pratimus, įsitikinkite, kad dirbate aplinkoje, kurioje įdiegti demonstraciniai duomenys, ir prieš pradėdami nustatykite juridinį subjektą į **USMF**.

## <a name="scenario-1-configure-default-shipment-consolidation-policies"></a><a name="scenario-1"></a>1 scenarijus: numatytųjų siuntos konsolidacijos strategijų konfigūravimas

Yra du toliau pateikti atvejai, kai turite sukonfigūruoti mažiausią numatytųjų strategijų skaičių įjungę funkciją *Siuntos konsolidacijos strategijos*.

- Naujinate aplinką, kurioje jau yra duomenų.
- Nustatote visiškai naują aplinką.

### <a name="upgrade-an-environment-where-warehouses-are-already-configured-for-cross-order-consolidation"></a>Aplinkos, kurioje sandėliai jau sukonfigūruoti kelių užsakymų konsolidacijai, naujinimas

Pradėjus šią procedūrą, funkcija *Siuntos konsolidacijos strategijos* turi būti išjungta, kad būtų galima imituoti aplinką, kurioje jau buvo naudojama pagrindinė kelių užsakymų konsolidacijos funkcija. Tada galėsite naudoti funkcijų valdymą funkcijai įjungti, kad sužinotumėte, kaip po naujinimo nustatyti siuntos konsolidacijos strategijas.

Atlikite tolesnius veiksmus, norėdami nustatyti numatytąsias siuntos konsolidacijos strategijas aplinkoje, kurioje sandėliai jau sukonfigūruoti kelių užsakymų konsolidacijai.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlis \> Sandėliai**.
1. Sąraše raskite ir atidarykite pageidaujamą sandėlio įrašą (pavyzdžiui, *24* sandėlį **USMF** demonstraciniuose duomenyse).
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. „FastTab” **Sandėlis** nustatykite parinktį **Konsoliduoti siuntą išleidžiant ją į sandėlį** į *Taip*.
1. Pakartokite 2–4 žingsnius visiems kitiems sandėliams, kuriems būtina konsolidacija.
1. Uždarykite puslapį.
1. Naudokite [funkcijų valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kad įjungtumėte funkciją *Siuntos konsolidacijos strategijos*. **Funkcijų valdymo** darbo srityje ši funkcija pavadinta *Konsoliduoti siuntą*.
1. Eikite į **Sandėlio valdymas \> Sąranka \> Išleidimas į sandėlį \> Siuntos konsolidacijos strategijos**. Jums gali reikėti atnaujinti naršyklę, kad, įjungę funkciją, matytumėte naują meniu elementą **Siuntos konsolidacijos strategijos**.
1. Veiksmų srityje pasirinkite **Kurti numatytąją sąranką**, kad sukurtumėte tolesnes strategijas.

    - **CrossOrder** strategija, skirta *pardavimo užsakymų* strategijos tipui (jei turite bent vieną sandėlį, nustatytą naudoti ankstesnę konsolidacijos funkciją)
    - **Numatytoji** strategija, skirta *pardavimo užsakymų* strategijos tipui
    - **Numatytoji** strategija, skirta *perkėlimo išdavimo* strategijos tipui
    - **CrossOrder** strategija, skirta *perkėlimo išdavimo* strategijos tipui (jei turite bent vieną sandėlį, nustatytą naudoti ankstesnę konsolidacijos funkciją)

    > [!NOTE]
    > - Abi **kelių užsakymų** strategijos tą patį laukų rinkinį laiko ankstesne logika, išskyrus užsakymo numerio lauką. (Šis laukas naudojamas norint konsoliduoti eilutes į siuntas, remiantis tokiais veiksniais kaip sandėlis, pristatymo transportavimo būdas ir adresas.)
    > - Abi **numatytosios** strategijos tą patį laukų rinkinį laiko ankstesne logika, įskaitant užsakymo numerio lauką. (Šis laukas naudojamas norint konsoliduoti eilutes į siuntas, remiantis tokiais veiksniais kaip užsakymo numeris, sandėlis, pristatymo transportavimo būdas ir adresas.)

1. Pasirinkite **CrossOrder** strategiją, skirtą *pardavimo užsakymų* strategijos tipui, tada veiksmų srityje pasirinkite **Redaguoti užklausą**.
1. Atkreipkite dėmesį, kad užklausos rengyklės dialogo lange išvardyti sandėliai, kurių parinktis **Konsoliduoti siuntą išleidžiant ją į sandėlį** nustatyta į *Taip*. Todėl jie įtraukiami į užklausą.

### <a name="create-default-policies-for-a-new-environment"></a>Numatytųjų naujos aplinkos strategijų kūrimas

Atlikite tolesnius veiksmus, norėdami nustatyti numatytąsias siuntos konsolidacijos strategijas visiškai naujoje aplinkoje.

1. Naudokite [funkcijų valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kad įjungtumėte funkciją *Siuntos konsolidacijos strategijos*, jei jos dar neįjungėte. **Funkcijų valdymo** darbo srityje ši funkcija pavadinta *Konsoliduoti siuntą*.
1. Eikite į **Sandėlio valdymas \> Sąranka \> Išleidimas į sandėlį \> Siuntos konsolidacijos strategijos**.
1. Veiksmų srityje pasirinkite **Kurti numatytąją sąranką**, kad sukurtumėte tolesnes strategijas.

    - **Numatytoji** strategija, skirta *pardavimo užsakymų* strategijos tipui
    - **Numatytoji** strategija, skirta *perkėlimo išdavimo* strategijos tipui

    > [!NOTE]
    > Abi **numatytosios** strategijos tą patį laukų rinkinį laiko ankstesne logika, įskaitant užsakymo numerio lauką. (Šis laukas naudojamas norint konsoliduoti eilutes į siuntas, remiantis tokiais veiksniais kaip užsakymo numeris, sandėlis, pristatymo transportavimo būdas ir adresas.)

## <a name="scenario-2-configure-custom-shipment-consolidation-policies"></a>2 scenarijus: pasirinktinių siuntos konsolidacijos strategijų konfigūravimas

Šis scenarijus nurodo, kaip nustatyti pasirinktines siuntos konsolidacijos strategijas. Pasirinktinės strategijos gali palaikyti sudėtingus verslo poreikius, kai siuntos konsolidacija priklauso nuo kelių sąlygų. Kiekviename tolesniame šio scenarijaus strategijos pavyzdyje įtrauktas trumpas verslo atvejo aprašymas. Šias pavyzdines strategijas reikia nustatyti seka, užtikrinančia piramidės tipo užklausų vertinimą. (Kitaip tariant, strategijos, turinčios daugiausiai sąlygų, turi būti vertinamos kaip turinčios didžiausią prioritetą.)

### <a name="turn-on-the-feature-and-prepare-master-data-for-this-scenario"></a>Funkcijos įjungimas ir šio scenarijaus bendrųjų duomenų rengimas

Kad galėtumėte pradėti šiame scenarijuje pateiktus pratimus, turite įjungti funkciją ir parengti bendruosius duomenis, reikalingus norint filtruoti, kaip aprašyta tolesniuose poskirsniuose. (Šios būtinosios sąlygos taip pat taikomos scenarijams, pateiktiems [Scenarijų, kaip naudoti siuntos konsolidacijos strategijas, pavyzdžiai](#example-scenarios).)

#### <a name="turn-on-the-feature-and-create-the-default-policies"></a>Funkcijos įjungimas ir numatytųjų strategijų kūrimas

Norėdami įjungti funkciją, naudokite funkcijų valdymą, jei jos dar neįjungėte, ir sukurkite numatytąsias konsolidacijos strategijas, aprašytas [1 scenarijuje](#scenario-1).

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
1. Uždarykite puslapį ir pakartokite 4 ir 5 veiksmus klientui, kurio sąskaitos numeris yra *US-004*.

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
1. Pasirinkite mygtuką **Įtraukti** ![Rodyklė dešinėn](media/forward-button.png), kad perkeltumėte lauką į sąrašą **Pasirinkti laukai**.
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
1. Pasirinkite mygtuką **Įtraukti** ![Rodyklė dešinėn](media/forward-button.png), kad perkeltumėte lauką į sąrašą **Pasirinkti laukai**.
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
1. Pasirinkite mygtuką **Įtraukti** ![Rodyklė dešinėn](media/forward-button.png), kad perkeltumėte lauką į sąrašą **Pasirinkti laukai**.
1. Sąraše **Likę laukai** pasirinkite eilutę, kurioje laukas **Lauko pavadinimas** nustatytas į *Pristatymo būdas*.
1. Pasirinkite mygtuką **Įtraukti** ![Rodyklė dešinėn](media/forward-button.png), kad perkeltumėte lauką į sąrašą **Pasirinkti laukai**.
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
1. Pasirinkite mygtuką **Įtraukti** ![Rodyklė dešinėn](media/forward-button.png), kad perkeltumėte lauką į sąrašą **Pasirinkti laukai**.
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

Paprastai šis verslo atvejis gali būti sprendžiamas naudojant numatytąsias strategijas, kurias sukūrėte [1 scenarijuje](#scenario-1). Tačiau taip pat galite rankiniu būdu sukurti panašias strategijas atlikdami tolesnius veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Išleidimas į sandėlį \> Siuntos konsolidacijos strategijos**.
1. Nustatykite lauką **Strategijos tipas** į *Pardavimo užsakymai*.
1. Veiksmų srityje pasirinkite **Naujas**, norėdami sukurti strategiją, turinčią tolesnius parametrus.

    - **Strategijos pavadinimas:** *Keli užsakymai*
    - **Strategijos aprašymas:** *konkrečių sandėlių kelių užsakymų konsolidacija*

1. Parinktį **Konsoliduoti su atviromis siuntomis** palikite nustatytą į *Ne*.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. „FastTab” **Konsolidavimo laukai** lauke **Likę laukai** pasirinkite eilutę, kurioje laukas **Lauko pavadinimas** nustatytas į *Pristatymo būdas*.
1. Pasirinkite mygtuką **Įtraukti** ![Rodyklė dešinėn](media/forward-button.png), kad perkeltumėte lauką į sąrašą **Pasirinkti laukai**.
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

Tolesniuose scenarijuose vaizduojama, kaip galima naudoti siuntų konsolidacijos strategijas, kurias sukūrėte skaitydami šią temą. Kiekvienas scenarijus apžvelgia siuntos konsolidacijos procesą, naudojantį siuntos konsolidacijos strategijas automatizuoto ar rankinio paleidimo į sandėlį metu.

- 1 scenarijus: [siuntų konsolidacija jas paleidus į sandėlį naudojant automatinį pardavimo užsakymų išleidimą](../warehousing/consolidate-shipments-automatic.md)
- 2 scenarijus: [siuntų konsolidacija, kai siuntos konsolidacijos strategija perrašyta iš išleidimo į sandėlio puslapį](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- 3 scenarijus: [siuntų konsolidacija naudojant išleidimą į sandėlį iš krovinio planavimo darbo srities](../warehousing/consolidate-shipments-load-planning-workbench.md)
- 4 scenarijus: [siuntų konsolidacija naudojant siuntų konsolidacijos darbo sritį](../warehousing/consolidate-shipments-manual-workbench.md)
- 5 scenarijus: [siuntų konsolidacija rankiniu būdu naudojant puslapį Konsoliduoti siuntas](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>Papildomi ištekliai

- [Siuntos konsolidacijos strategijos](about-shipment-consolidation-policies.md)
