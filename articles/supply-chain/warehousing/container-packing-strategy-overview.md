---
title: Konteinerių pakavimo strategijos
description: Šioje temoje aprašomi konteinerių pakavimo strategijų skirtumai ir pateikiami pavyzdžiai.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 4e5faf8e4544b2bcb58f3c578789b2bd379a27b0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572366"
---
# <a name="container-packing-strategies"></a>Konteinerių pakavimo strategijos

[!include [banner](../includes/banner.md)]

*Konteinerių pakavimo strategija* yra strategija, kurią galite naudoti prekių paskirstymui tarp konteinerių apibrėžti. Šioje temoje paaiškinami skirtumai tarp *Pakuoti į visus atidarytus konteinerius* ir *Pakuoti tik į dabartinį konteinerį* strategijų.

- **Pakuoti į visus atidarytus konteinerius** – sistema turi patikrinti visus atidarytus konteinerius, kurie jau buvo sukurti krovimo į konteinerius ciklo metu, kad įsitikintų, jog prekė tilps į vieną iš jų. Pakavimo metu sistema patikrina kiekvieną prekę, kad nustatytų, ar ji tinka bet kuriam anksčiau sukurtam konteineriui. Jei prekė netilps į esamą konteinerį, sistema sukuria naują konteinerį ir taip tęsia toliau, kol užbaigia supakuoti visą užsakymą.

    Pavyzdžiui, *n kiekiui* užsakytų prekių būtinas krovimas į konteinerius. Blogiausiu atveju kiekvieną kartą sistemai apdorojant prekę, netelpančią į jokį esamą konteinerį, iš viso ji atliks (\[(*n-1*) × (*n+1*)\] ÷ 2) patikrinimų, jog įvertintų, ar prekė tilps į esamus konteinerius.

- **Pakuoti tik į dabartinį konteinerį** – sistema privalo patikrinti tik paskutinį sukurtą konteinerį, kad įsitikintų, jog prekė į jį tilps. Pakavimo metu sistema patikrina kiekvieną prekę, kad nustatytų, ar ji tinka naujausiam sukurtam konteineriui. Jei prekė netilps į tą konteinerį, sistema sukuria naują konteinerį ir taip tęsia toliau, kol užbaigia supakuoti visą užsakymą.

    Pavyzdžiui, *n kiekiui* užsakytų prekių būtinas krovimas į konteinerius. Blogiausiu atveju sistema iš viso atliks (*n-1*) patikrinimų, jog įvertintų, ar prekė tilps į konteinerius.

## <a name="example-of-the-flow-for-container-packing-strategies"></a>Konteinerių pakavimo strategijų srauto pavyzdys

Nustatote toliau pateiktas prekes krovimui į konteinerius.

| Prekė | Faktinės dimensijos (plotis × gylis × aukštis) | Svoris |
|---|---|---|
| HDMI kabelis 6' | 1×1×1 | 1 |
| HDMI kabelis 12' | 2×1×1 | 1 |
| HDMI kabelis 18' | 3×1×1 | 2 |

Taip pat nustatote toliau pateiktą dėžę, kuri bus naudojama pakavimui.

| Konteineris | Faktinės dimensijos (ilgis × plotis × aukštis) | Svoris | Tūris |
|---|---|---|---|
| Vidutinė dėžė | 6×3×2 | 10 | 100 |

Galiausiai, jūs nustatote užsakymą, kuriame yra šie produktai ir kiekiai.

| Pardavimo užsakymo eilutė | Kiekis |
|---|---|
| HDMI kabelis 12' | 9 |
| HDMI kabelis 18' | 8 |
| HDMI kabelis 6' | 13 |

Toliau pateiktoje lentelėje apibendrinama, kaip veikia pakavimas į konteinerius, kai naudojate *Pakuoti į visus atidarytus konteinerius* strategiją ir kai naudojate *Pakuoti tik į dabartinį konteinerį* strategiją.

| Pakuoti į visus atidarytus konteinerius | Pakuoti į dabartinį konteinerį |
|---|---|
| <p>HDMI kabelis 12':</p><ol><li>Sukurkite naują konteinerį, CONT0001.</li><li>Įdėkite 9 vienetus į CONT0001 konteinerį.</li></ol> | <p>HDMI kabelis 12':</p><ol><li>Sukurkite naują konteinerį, CONT0001.</li><li>Įdėkite 9 vienetus į CONT0001 konteinerį.</li></ol> |
| <p>HDMI kabelis 18':</p><ol><li>Patikrinkite, ar prekė gali tilpti į CONT0001 konteinerį.</li><li>Sukurkite naują konteinerį, CONT0002.</li><li>Įdėkite 5 vienetus į CONT0002 konteinerį.</li><li>Sukurkite naują konteinerį, CONT0003.</li><li>Įdėkite 3 vienetus į CONT0003 konteinerį.</li></ol> | <p>HDMI kabelis 18':</p><ol><li>Patikrinkite, ar prekė gali tilpti į CONT0001 konteinerį.</li><li>Sukurkite naują konteinerį, CONT0002.</li><li>Įdėkite 5 vienetus į CONT0002 konteinerį.</li><li>Sukurkite naują konteinerį, CONT0003.</li><li>Įdėkite 3 vienetus į CONT0003 konteinerį.</li></ol> |
| <p>HDMI kabelis 6':</p><ol><li>Patikrinkite, ar prekė gali tilpti į CONT0001 konteinerį.</li><li>Įdėkite 1 vienetą į CONT0001 konteinerį.</li><li>Patikrinkite, ar prekė gali tilpti į CONT0002 konteinerį.</li><li>Patikrinkite, ar prekė gali tilpti į CONT0003 konteinerį.</li><li>Įdėkite 4 vienetus į CONT0003 konteinerį.</li><li>Sukurkite naują konteinerį, CONT0004.</li><li>Įdėkite 8 vienetus į CONT0004 konteinerį.</li></ol> | <p>HDMI kabelis 6':</p><ol><li>Patikrinkite, ar prekė gali tilpti į CONT0003 konteinerį.</li><li>Įdėkite 4 vienetus į CONT0003 konteinerį.</li><li>Sukurkite naują konteinerį, CONT0004.</li><li>Įdėkite 9 vienetus į CONT0004 konteinerį.</li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a>Pavyzdinis scenarijus: Vieno užsakymo pakavimas į vieną konteinerį

Šiame skyriuje pateikiamas scenarijus, kai sistema yra nustatyta konsoliduoti kelis užsakymus į vieną siuntą. Todėl krovimas į konteinerius bus atliekamas iš pardavimo užsakymo, siekiant užtikrinti, kad kiekvienas užsakymas, kuriame yra keli produktai, būtų supakuotas į vieną konteinerį.

Naudodami šią funkciją galite susitvarkyti su scenarijais, kuriuose turite supakuoti tik vieną pardavimo užsakymą kiekviename konteineryje, kad paskirstymo centras galėtų paskirstyti pilnus konteinerius tarp mažmeninės prekybos parduotuvių. Be mažmeninės prekybos scenarijų (užsakymas pagal parduotuvę ir siuntimas į prekių skirstymo paskirstymo centrą), šis principas taip pat dažnai naudojamas „lean” tiekimo grandinėse (pardavimo užsakymas pagal „reikiamu laiku” gamybos eilutę).

Šiame scenarijuje rodoma, kaip galite sumažinti konteinerių, kurie įvertinami pakuojant, skaičių naudodami *Pakuoti tik į dabartinį konteinerį* krovimo į konteinerius strategiją.

### <a name="prerequisites"></a>Būtinieji komponentai

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a>Siuntų konsolidavimo funkcijos įjungimas sistemoje

Šis scenarijus naudoja *Konsoliduoti siuntas* funkciją. Jei ši funkcija dar negalima jūsų sistemoje, turite įjungti ją naudodami [Funkcijų valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

#### <a name="make-demo-data-available"></a>Demonstracinių duomenų įgalinimas

Šis scenarijus nurodo reikšmes ir įrašus, įtrauktus į standartinius „Microsoft Dynamics 365 Supply Chain Management” demonstracinius duomenis. Jei norite naudoti čia pateiktas reikšmes atlikdami pratimus, įsitikinkite, kad dirbate aplinkoje, kurioje įdiegti demonstraciniai duomenys, ir prieš pradėdami nustatykite juridinį subjektą į **USMF**.

### <a name="inspect-or-create-container-types"></a>Konteinerių tipų tikrinimas ar kūrimas

Norėdami patikrinti konteinerių tipus arba, jei reikia, sukurti naujus konteinerių tipus, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas** \> **Nustatymas** \> **Konteineriai** \> **Konteinerių tipai**.
1. Įsitikinkite, kad kiekvienas iš toliau pateiktų konteinerio tipų yra galimas jūsų demonstraciniuose duomenyse. Redaguokite arba sukurkite konteinerių tipus, jei reikia.

    - 1 konteinerio tipas:

        - **Konteinerio tipo kodas:** *Didelė dėžė*
        - **Aprašas:** *Didelė dėžė*
        - **Didžiausias grynasis svoris:** *100*
        - **Tūris:** *400*
        - **Ilgis:** *4*
        - **Plotis:** *10*
        - **Aukštis:** *10*

    - 2 konteinerio tipas:

        - **Konteinerio tipo kodas:** *Vidutinė dėžė*
        - **Aprašas:** *Vidutinė dėžė*
        - **Didžiausias grynasis svoris:** *50*
        - **Tūris:** *200*
        - **Ilgis:** *2*
        - **Plotis:** *10*
        - **Aukštis:** *10*

    - 3 konteinerio tipas:

        - **Konteinerio tipo kodas:** *Maža dėžė*
        - **Aprašas:** *Maža dėžė*
        - **Didžiausias grynasis svoris:** *20*
        - **Tūris:** *100*
        - **Ilgis:** *1*
        - **Plotis:** *10*
        - **Aukštis:** *10*

### <a name="inspect-or-create-container-groups"></a>Konteinerių grupių tikrinimas arba kūrimas

Norėdami patikrinti konteinerių grupes arba, jei reikia, sukurti naujas konteinerių grupes, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas** \> **Nustatymas** \> **Konteineriai** \> **Konteinerių grupės**.
1. Įsitikinkite, kad toliau pateikta konteinerio grupė yra galima jūsų demonstraciniuose duomenyse. Jei ji negalima, pasirinkite **Nauja**, kad ją sukurtumėte.

    - **Konteinerių grupės ID:** *Dėžės*
    - **Aprašas:** *Dėžių dydžiai*

1. Įsitikinkite, kad „FastTab” **Išsami informacija** konteinerių grupei *Dėžės* yra toliau pateiktos eilutės. Jei jų nėra, pasirinkite **Nauja**, kad jas įtrauktumėte.

    - Eilutė 1:

        - **Sekos numeris:** *1*
        - **Talpyklos tipas:** *Plati dėžė*
        - **Konteinerio efektyvumo procentas:** *100*

    - Eilutė 2:

        - **Sekos numeris:** *2*
        - **Konteinerio tipas:** *Vidutinė dėžė*
        - **Konteinerio efektyvumo procentas:** *100*

    - Eilutė 3:

        - **Sekos numeris:** *3*
        - **Konteinerio tipas:** *Maža dėžė*
        - **Konteinerio efektyvumo procentas:** *100*

### <a name="create-a-new-container-build-template"></a>Sukurkite naują konteinerio kūrimo šabloną

Norėdami sukurti naują konteinerio kūrimo šabloną, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas** \> **Nustatymas** \> **Konteineriai** \> **Konteinerio kūrimo šablonas**.
1. Pasirinkite **Naujas** norėdami sukurti konteinerio kūrimo šabloną, kuris turi šiuos parametrus:

    - **Sekos numeris:** *1*
    - **Konteinerio šablono ID:** *Dėžė*
    - **Konteinerių grupės ID:** *Dėžės*
    - **Pagrindiniai užklausų tipai:** *Pardavimų paskirstymo eilutė*
    - **Bangos veiksmo kodas:** *234*
    - **Leisti skaidyti paėmimus:** *Taip*
    - **Konteinerių pakavimo strategija:** *Pakuoti tik į dabartinį konteinerį*
    - **Paketas pagal krypties vienetą:** *Ne*

1. Kol naujo šablono eilutė vis dar pasirinkta, pasirinkite **Redaguoti užklausą** veiksmų srityje.
1. Atsiranda standartinis užklausų rengyklės dialogo langas. Skirtuke **Rikiavimas** pasirinkite **Įtraukti** norėdami įtraukti eilutę, turinčią toliau pateiktus parametrus:

    - **Lentelė:** *Laikinos darbo operacijos*
    - **Išvestinė lentelė:** *Laikinos darbo operacijos*
    - **Laukas:** *Užsakymo numeris*
    - **Paieškos kryptis:** *Didėjanti*

    > [!IMPORTANT]
    > Norėdami išvengti visų kitų atvirų konteinerių perkrovos ir pagreitinti procesą vienu metu pažymėdami vieną konteinerį, naudokite *Pakuoti tik į dabartinį konteinerį* strategiją bei rikiavimą pagal užsakymo numerį. Šis derinys veiks kaip darbo skaidymas darbo šablone.

1. Pasirinkite **Gerai** užklausos tvarkyklės teksto langui uždaryti.
1. Kol naujo šablono eilutė vis dar pasirinkta, pasirinkite **Konteinerių maišymo apribojimai** veiksmų srityje.

    Dabar įtrauksite apribojimą, pagal kurį prekės iš vieno užsakymo bus kraunamos į vieną konteinerį. Prekės iš bet kurio kito užsakymo bus kraunamos į atskirą konteinerį.

1. Pasirinkite **Naujas** norėdami sukurti maišymo apribojimą, kuris turi šiuos parametrus:

    - **Lentelė:** *pardavimo užsakymai*
    - **Lauko pasirinktis:** *Pardavimo Id* (Laukas bus rodomas kaip *Pardavimo užsakymas* tinklelyje.)

1. Pasirinkite **Gerai** norėdami įtraukti apribojimą.
1. Uždarykite puslapį.

### <a name="set-up-a-wave-template-for-containerization"></a>Krovimo į konteinerius bangos šablono nustatymas

Norėdami nustatyti bangos šabloną atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.
1. Sąrašo srityje nustatykite **Bangos šablono tipo** laukelį į *Siuntimas*.
1. Sąraše pasirinkite **63 krovimas į konteinerius** šabloną.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. **Metodai** „FastTab“ **Pasirinkti metodai** stulpelyje suraskite šią eilutę:

    - **Metodo pavadinimas:** *pakavimas į konteinerius*
    - **Pavadinimas:** *Pakavimas į konteinerius*

1. Nustatykite **Bangos žingsnio kodo** lauką šiai eilutei į *234*.

### <a name="set-up-a-work-template"></a>Darbo šablono nustatymas

Norėdami nustatyti darbo šabloną atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.
1. Nustatykite lauką **Darbo užsakymo tipas** į *Pardavimo užsakymai*.
1. Tinklelyje **Peržiūra** raskite ir pasirinkite darbo šabloną, kuris turėtų būti naudojamas atskirų užsakymų pakavimui į konteinerius. Šiame scenarijuje pasirinkite **63 paėmimo į konteinerį** šabloną.
1. Veiksmų srityje pasirinkite **Redaguoti užklausą**.
1. Atsiranda standartinis užklausų rengyklės dialogo langas. Skirtuke **Rūšiavimas** įtraukite toliau pateiktas eilutes:

    - Eilutė 1:

        - **Lentelė:** *Laikinos darbo operacijos*
        - **Išvestinė lentelė:** *Laikinos darbo operacijos*
        - **Laukas:** *Siuntos ID*
        - **Paieškos kryptis:** *Didėjanti*

    - Eilutė 2:

        - **Lentelė:** *Laikinos darbo operacijos*
        - **Išvestinė lentelė:** *Laikinos darbo operacijos*
        - **Laukas:** *Užsakymo numeris*
        - **Paieškos kryptis:** *Didėjanti*

    - Eilutė 3:

        - **Lentelė:** *Laikinos darbo operacijos*
        - **Išvestinė lentelė:** *Laikinos darbo operacijos*
        - **Laukas:** *Konteinerio ID*
        - **Paieškos kryptis:** *Didėjanti*

1. Pasirinkite **Gerai** užklausos tvarkyklės teksto langui uždaryti.
1. Jūs gaunate šį pranešimą: „Grupavimas bus perkrautas, ar tęsti?“ Pasirinkite **Taip** tam, kad tęstumėte.
1. Kol šablonas **63 paėmimas į konteinerį** vis dar pasirinktas, pasirinkite **Darbo antraštės lūžiai** veiksmų srityje.

    Dabar pritaikysite parametrus norėdami skaidyti darbą, kad kiekvienas užsakymo konteineris būtų susietas su vienu darbo užsakymu.

1. Kiekvienai eilutei pasirinkite **Grupuoti pagal šį lauką** žymės langelį **Darbo antraštės lūžiai** puslapyje (**Siuntos ID**, **Užsakymo numeris** ir **Konteinerio ID**).
1. Uždarykite puslapį.

### <a name="set-up-shipment-consolidation-policies"></a>Siuntos konsolidacijos strategijų nustatymas

Norėdami nustatyti siuntos konsolidacijos strategiją, atlikite toliau nurodytus veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Išleidimas į sandėlį \> Siuntos konsolidacijos strategijos**.
1. Sąrašo srityje nustatykite lauką **Strategijos tipas** į *Pardavimo užsakymai*.
1. Pasirinkite **Numatytąją** strategiją sąraše.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. „FastTab” **Konsolidavimo laukai** sąraše **Pasirinkti laukai** pasirinkite eilutę, kurioje laukas **Lauko pavadinimas** nustatytas į *Užsakymo numeris*.
1. Pasirinkite **Pašalinti** mygtuką ![Rodyklė kairėn.](media/backward-button.png) lauko perkėlimui į **Likę laukai** sąrašą.
1. Veiksmų srityje pasirinkite **Įrašyti**.

### <a name="set-up-physical-dimensions-for-the-product"></a>Faktinių produkto dimensijų nustatymas

Norėdami nustatyti faktines produktų, kurie bus naudojami šiame scenarijuje, dimensijas, atlikite tolesnius veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Pasirinkite produktą, kurio laukas **Prekės numeris** nustatytas į *„A0001”*.
1. Veiksmų juostoje, **Inventoriaus valdymo** skirtuke, **Sandėlio** grupėje, pasirinkite **Fiziniai matmenys**.
1. Puslapyje **Faktinės dimensijos** turėtumėte matyti šią eilutę tinklelyje:

    - **Vienetas:** *vnt*
    - **Bruto svoris:** *3,00*
    - **Plotis:** *2,00*
    - **Gylis:** *2,00*
    - **Aukštis:** *4,00*
    - **Tūris:** *16,00*

1. Uždarykite puslapį.
1. Pasirinkite produktą, kurio **Prekės numerio** laukas nustatytas į *„A0002”*.
1. Veiksmų juostoje, **Inventoriaus valdymo** skirtuke, **Sandėlio** grupėje, pasirinkite **Fiziniai matmenys**.
1. Puslapyje **Faktinės dimensijos** turėtumėte matyti šią eilutę tinklelyje:

    - **Vienetas:** *vnt*
    - **Bruto svoris:** *4,00*
    - **Plotis:** *3,00*
    - **Gylis:** *1,00*
    - **Aukštis:** *3,00*
    - **Tūris:** *9,00*

### <a name="create-sales-order-1"></a>1 pardavimo užsakymo kūrimas

Norėdami sukurti pardavimo užsakymą, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Atsiranda dialogo langas, skirtas naujo pardavimo užsakymui kūrimui. Nustatykite toliau nurodytas reikšmes.

    - **Kliento sąskaita:** *US-001*
    - **Sandėlis:** *63*

1. Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.
1. Naujas pardavimo užsakymas yra atidarytas. „FastTab” **Pardavimo užsakymo eilutės** įtraukite toliau pateiktas pardavimo eilutes:

    - Eilutė 1:

        - **Prekės numeris:** *A0001*
        - **Kiekis:** *2*

    - Eilutė 2:

        - **Prekės numeris:** *A0002*
        - **Kiekis:** *2*

1. Pasirinkite pirmą eilutę, o tada pasirinkite **Atsargos \> Rezervavimas**.
1. **Rezervacijos** puslapyje pasirinkite **Rezervavimo vieta**. Tada uždarykite puslapį.
1. Pakartokite pirmus du antrosios eilutės veiksmus.
1. Uždarykite puslapį.

### <a name="create-sales-order-2"></a>Pardavimo užsakymo 2 sukūrimas

Norėdami sukurti antrą pardavimo užsakymą, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Atsiranda dialogo langas, skirtas naujo pardavimo užsakymui kūrimui. Nustatykite toliau nurodytas reikšmes.

    - **Kliento sąskaita:** *US-001*
    - **Sandėlis:** *63*

1. Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.
1. Naujas pardavimo užsakymas yra atidarytas. „FastTab” **Pardavimo užsakymo eilutės** įtraukite toliau pateiktas pardavimo eilutes:

    - Eilutė 1:

        - **Prekės numeris:** *A0001*
        - **Kiekis:** *4*

    - Eilutė 2:

        - **Prekės numeris:** *A0002*
        - **Kiekis:** *4*

1. Pasirinkite pirmą eilutę, o tada pasirinkite **Atsargos \> Rezervavimas**.
1. **Rezervacijos** puslapyje pasirinkite **Rezervavimo vieta**. Tada uždarykite puslapį.
1. Pakartokite pirmus du antrosios eilutės veiksmus.
1. Uždarykite puslapį.

### <a name="create-the-load"></a>Krovinio kūrimas

Norėdami sukurti krovinį kiekvienam šiame scenarijuje sukurtam užsakymui ir tada išleisti jį į sandėlį, atlikite tolesnius veiksmus.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Krovinio planavimo darbo sritis**.
1. Skirtuke **Pardavimo eilutės** raskite ir pasirinkite visas pardavimo užsakymo eilutes iš pardavimo užsakymų, sukurtų šiam scenarijui.
1. Veiksmų srities **Tiekti ir pareikalauti** skirtuke **Pridėti** grupėje pasirinkite **Į naują krovinį**. Pasirinktos užsakymo eilutės įtraukiamos į naują krovinį.
1. Dialogo lango **Krovinio šablono priskyrimas** lauke **Krovinio šablono ID** pasirinkite krovinio šabloną, pavyzdžiui, *40' konteineris*.
1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.
1. Dalyje **Kroviniai** raskite ir pasirinkite ką tik sukurtą krovinį.
1. Pasirinkite **Išleisti \> Išleisti į sandėlį**.
1. Dialogo lange **Išleisti į sandėlį** pasirinkite **GERAI**, kad išleistumėte pasirinktą krovinį į sandėlį.

### <a name="verify-the-shipments-and-containers"></a>Siuntų ir konteinerių patikrinimas

Toliau pateikta procedūra jums leidžia patikrinti sukurtas siuntas. Naudokite ją peržiūrėti užsakymui, kurį sukūrėte šiam scenarijui, kad įsitikintumėte gavę numatytus rezultatus.

1. Eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos**.
1. Raskite ir pasirinkite siuntą, kuri buvo sukurta ką tik išleistam kroviniui.
1. Veiksmų srities skirtuke **Transportavimas** pasirinkite **Rodyti konteinerius**.
1. Patvirtinkite, kad prekės iš pardavimo užsakymų buvo sukrautos į du skirtingus konteinerius.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Krovimas į konteinerius](wave-containerization.md)
