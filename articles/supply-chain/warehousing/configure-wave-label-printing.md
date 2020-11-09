---
title: Nustatykite ir naudokite bangos žymos spausdinimą
description: Šioje temoje aprašytas bangos žymos spausdinimas ir paaiškinta, kaip ją nustatyti.
author: GarmMSFT
manager: PJacobse
ms.date: 05/01/2020
ms.topic: configure-wave-label-printing
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 1f51ed9f05caede3d4f320ddb6b705e67df9aa1f
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016960"
---
# <a name="set-up-and-use-wave-label-printing"></a>Nustatykite ir naudokite bangos žymos spausdinimą

[!include [banner](../includes/banner.md)]

Bangos žymos spausdinimas siūlo alternatyvią prieigą prie žymos spausdinimo įtraukiant naują bangos žingsnio metodą, leidžiantį jums sukurti ir spausdinti žymos tiesiogiai iš bango šablono bangos vykdymo metu. Dėl to, žymės visuomet bus prieinamos prieš tai, kai darbuotojai vykdys darbo užsakymą mobiliame prietaise. Darbuotojai gali įtraukti reikiamas žymes paėmimo metu, o ne po jo.

Bangos žymos spausdinimas naudoja „Zebra Programming Language“ (ZPL) žymos maketo kūrimui. Žymos maketas yra padalintas į tris skyrius (antraštė, vidurye ir poraštė) ir leidžia kurti pasikartojančią struktūra turinčias žymes. Bangos žymos šablonai sako sistemai, kurią žymos maketą reikia naudoti. Vartotojai gali nurodyti, kurį spausdintuvą naudoti. Jie taip pat gali atspausdinti žymes keliuose spausdintuvuose tuo pačiu metu, jei to reikia. **Bangos žymos istorijos** puslapis rodo žymių, kurios buvo sukurtos naudojant šį nustatymą, įrašą.

Galite atspausdinti ir palyginti žymes pagal darbo antraštes, nes galite atspausdinti padalintas žymes pagal darbo antraštes ir atspausdinti talpyklos turinio žymes, dėžės žymes ir kitas panašias žymes.

> [!NOTE]
> Ši funkcija nepakeičia esančios žymos spausdinimo funkcijos, kuri yra pagrįsta dokumento maršrutu.

Bangos žymos spausdinimas siūlo šiuo pagerinimus:

- Spausdinkite žymos pagal dėžių numerį vienoje darbo linijoje nenaudojant talpinimo į talpyklas. („dėžė“ yra objektas sukurtas objekto sekos grupės linijose.)
- Atspausdinkite keletą skirtingų žymių sekų (pavyzdžiui, dėžės ir padėklo žymes).
- Įtraukite žymos numeravimą (pavyzdžiui, 1/124, 2/124, ... 124/124) ir nustatykite numeravimo intervalą (pavyzdžiui, darbo liniją, apkrovos liniją ar siuntimą).
- Sukurkite ir atspausdinkite važtarščio identifikavimo numerį žymėse prieš važtaraščio sugeneravimą.
- Sukurkite unikalų serijinį siuntimo talpyklos kodą (SSCC) kiekvienai dėžėi ir įtraukite jį į kiekvieną žymę.
- Sukurkite GS1-atitinkančias numerio sekas važtaraščio identifikavimo kodamas ir SSCC kodams.
- Etikečių naujas spausdinimas mobiliame prietaise ir praturtintame kliente.
- Panaikinkite žymes (pavyzdžiui, trumpo paėmimo scenarijuose) ir spausdinkite juos dar kartą.
- Išvalykite bangos žymės istoriją.
- Dokumento maršruto pagerinimais yra dalijimasi tarp dokumento maršruto maketų ir bangos žymos maketų. (Dėl išsamesnės informacijos, žr. [Dokumento maršruto maketas licencijų numeriams](../warehousing/document-routing-layout-for-license-plates.md).)

Šie pagerinimai padaro žymos dėžes efektyvesnes prieš sudėjimą ant padėklų. Jie ypač pasitarnauja bendrovėms siunčiančioms dideliems prekybininkams, kurie automatiškai patvirtina užsakymo kvitą nuskaitydami kiekvieną dėžę atskirai.

> [!NOTE]
> Galite įgyvendinti konfigūraciją scenarijams, kurie aprašyti šiame skyriuje atskirai ar kartu, priklausomai nuo verslo reikalavimų. Galite suprojektuoti keletą bangos žymos šablonų, kurie dirba sekoje (kaip parodyta scenarijuje 3). Pavyzdžiui, galite naudoti scenarijų 1 tam, kad atspausdintumėte dėžės žymes ir scnearijų 2, kad atspausdintumėte padėklo žymes (jei padėklai sandėlyje skiriasi dydžiu ir sudėtimi).

## <a name="turn-on-the-wave-label-printing-feature"></a>Įjunkite bangos žymos spausdinimo savybę

Prieš naudodami šią funkciją, *Bangos žymos spausdinimas* savybę, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Ten ši funkcija pateikiama taip:

- **Modulis:** *Sandėlio valdymas*
- **Savybės pavadinimas:** *Bangos žymos spausdinimas*

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a>Scenarijus 1: Bangos žymos spausdinimas, kai atskira bangos žymė yra sukuriama

Šis scenarijus rodo, kaip bendrovė gali spausdinti siuntimo žymes dideliems prekybininkams, kurie automatiškai tvirtina užsakymo kvitus nuskaitydami kiekvieną dėžę atskirai.

Šis scenarijus parodo srautą nuo pradžios iki galo.

### <a name="make-demo-data-available"></a>Demonstracinių duomenų įgalinimas

Šio scenarijaus įgyvendinimui, privalote turėti įdiegtus demo duomenis ir pasirinkti **USMF** juridinį asmenį.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Įsitikinkite, kad bangos žymos metodas yra prieinamas

Jums gali reikėti iš naujo sukurti bangos proceso metodus tam, kad padarytumėte prieinamą bangos etiketės spausdinimo metodą.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Bangos \> Bangos apdorojimo metodai**.
1. Patvirinkite, kad **bangos žymos spausdinimas** yra sąraše. Jei jo nėra, pasirinkite **Iš naujo kurti metodu** veiksmų juostoje ir juos įtraukite.

### <a name="configure-a-wave-template"></a>Sukonfigūruokite bangos šabloną

Bangos šablonas leidžia jums susieti konkrečius bangų metodų atvejus pagal atitinkantį bangos žymos šabloną.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.
1. Pasirinkite šabloną, tokį kaip **62 siuntimo nustatytąjį**.
1. **Metodai** „FastTab“, patraukite **bangos žymosspausdinimo** metodą į **Pasirinkti metodai** stulpelį.
1. **Pasirinkti metodai** stulpelyje, pasirinkite **bangos žymosspausdinimo** metodą ir nustatykite jo **Bangos žingsnio kodo** laukelį į *Spausdinti žymę*. Dėl išsamesnės informacijos apie bangos žingsnio kodus, žr. [Bangos žingsnio kodai](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Sukurkite bangos žymosmaketą

Žymos maketas kontroliuoja, kokia informacija yra spausdinama žymėje ir kaip ji yra padėta. Čia galite įvesti ZPL kodą, kuris nusiunčiamas spausdintuvui.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Dokumento maršrutas \> bangos žymos maketai**.
1. Sukurkite įrašą, kuris turi šiuos nustatymus:

    - **Žymos maketo identifikavimo numeris:** *Dėžė*
    - **Aprašas:** *Dėžė (SSCC)*

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Veiksmų juostoje pasirinkite **bangos žymoseilutės nustatymai**.

    Pasirodo **bangos žymoseilutės nustatymai** langas. Čia galite sukonfigūruoti dinaminę žymos dalį.

1. Įtraukite eilutę, kuri turi šiuos nustatymus:

    - **Eilutės Identifikavimo kodas:** *Bangos žymė*
    - **Eilutės lentelės pavadinimas:** *WHSWaveLabel*
    - **Eilutės pradžios padėtis:** *0*

        Šis laukelis apibrėžia vertikalią padėtį, kurioje eilutė prasideda žymėje.

    - **Eilutės aukštis:** *0*

        Laukelis apibrėžia kiekvienos eilutės aukštį (taškais) pagal ZPL standartą. Eilutės aukštis yra teigiamas horizontalioms žymėms ir neigiamas vertikalioms. Kadangi yra tik viena eilutė šiame pavyzdyje, galite nustatyti vertę į *0* (nulį).

    - **Eilutės puslapyje:** *1*

        Šis laukelis parodo eilučių skaičių, kuris gali būti atspausdintas kiekvienoje žymėje.

        > [!NOTE]
        > Šis nustatymas nulems, kad atskira ZPL žymė bus spausdinima kiekvienam įrašui bangos žymių lentelėje.

1. Uždarykite puslapį.
1. Veiksmų srityje pasirinkite **Redaguoti užklausą**.
1. Užklausos tvarkyklės teksto laukelyje, **Intervalas** skirtuke įtraukite eilutę su šiais nustatymais:

    - **Lentelė:** *Darbo eilutės*
    - **Išvestinė lentelė:** *Darbo eilutės*
    - **Laukas:** *Darbo tipas*
    - **Kriterijai:** *Paėmimas*

    Ši užklausa užtikrina, kad tik paėmimo tipo darbo linijos bus atspausdintos žymėje, o ne padėjimo tipo darbo linijos.

1. Jei norite galėti atspausdinti važtaraščio identifikavimo kodą **Sujungimai** skirtuke, pasirinkite **Darbo linijų** lentelę ir prijunkite prie jo **Siuntimai** lentelę.
1. Uždarykite užklausos tvarkylės teksto laukelį.
1. **Spausdintuvo teksto maketas** „FastTab“ turi tris skyrius, kuriuose galite rašyti spausdintuvo kodą: **Antraštės skyrius** , **Vidurinės dalies skyrius** ir **Poraštės skyrius**. **Antraštės skyrius** skyriuje, **Žymos antraštė** laukelyje įveskite ZPL kodą būtinai antraštei. Pavyzdžiui, jei naudojate „Zebra“ spaudintuvus, galite naudoti šį kodą.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. **Vidurinės dalies skyrius** skyriuje, **Žymos vidurinė dalis** laukelyje įveskite ZPL kodą būtinai vidurinei daliai. Toliau pateikiamas pavyzdys.

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. **Vidurinės dalies skyrius** skyriuje, **Žymos apatinė dalis** laukelyje įveskite ZPL kodą būtinai apatinei daliai. Toliau pateikiamas pavyzdys.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Šie nustatymai atspausdins vieną kiekvienos žymos kopiją. Jei jums reikia daugiau kopijų (pavyzdžiui, vienos kopijos vienai padėklo pusei), nustatykite **n** vertę **\^PQn** skyriui poraštėje reikiamam kopijų skaičiui. Pavyzdžiui, keturių kiekvienos žymos kopijų spausdinimui, nustatykite **\^PQ4**.

Jūsų žymė dabar paruošta naudojimui.

### <a name="create-a-wave-label-type"></a>Sukurkite bangos žymostipą

bangos žymostipai naudojami susieti bangos žymosšablonus su padalinio esančio jo sekos grupės linijose.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Dokumento maršrutas \> bangos žymostipai**.
1. Įtraukite bangos etiketės tipą, kuris turi šiuos nustatymus:

    - **Žymos tipas:** *Dėžė*
    - **Aprašas:** *Dėžė*

### <a name="set-up-unit-sequence-groups"></a>Nustatyti vienetų sekų grupes

Po to, nustatykite objekto sekos grupę bangos žymostipui.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Sandėlis \> Padalinio sekos grupės**.
1. Pasirinkite **Ea Box PL** grupę.
1. **Dėžutė** linijoje nustatykite **Bangos lygio tipas** laukelį į *Dėžė*.

### <a name="create-a-wave-label-template"></a>Sukurkite bangos žymosšabloną

Po to, sukurkite bangos žymosšabloną bangos žymostipui.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Dokumento maršrutas \> bangos žymosšablonai**.
1. Įtraukite bangos lygio šabloną ir nustatykite šias vertes antraštėje:

    - **Žymos šablono pavadinimas:** *Dėžių žymės*
    - **Aprašas:** *Dėžės žymės*
    - **Bangos žingsnio kodas:** *PrintLabel*
    - **Sandėlis:** *62*

1. **Bendra** „FastTab“, nustatykite **bangos žymostipas** laukelį į *Dėžė*.
1. **bangos žymosšablono informacijoje** „FastTab“, įtraukite naują eilutę turinčią šiuos nustatymus:

    - **Žymos maketo identifikavimo numeris:** *Dėžė*
    - **Spausdintuvo pavadinimas:** Pasirinkite tinkamą ZPL spausdintuvą.
    - **Vykdykite užklausą:** *Taip* (Šis pasirinkimas yra pasirenkamas, tačiau rekomenduojamas optimaliam veikimui.)

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Pasirenkamas: Jei nustatote klientui konkretų žymos maketą, privalote sukurti užklausą tam, kad rastumėte kliento paskyrą. **bangos žymos šablono informacijoje** „FastTab“, pasirinkite **Redaguoti užklausą**. Tuomet, užklausos tvarkyklės teksto laukelyje, **Intervalas** skirtuke įtraukite eilutę su šiais nustatymais:

    - **Lentelė:** *Siuntos*
    - **Išvestinė lentelė:** *Siuntos*
    - **Laukelis:** *Paskyros numeris*
    - **Kriterijai:** Įveskite reikiamą kliento paskyros numerį.

    Kai baigsite, pasirinkite **OK** užklausos tvarkyklės teksto langui uždaryti.

1. Veiksmų juostoje pasirinkite **Redaguoti užklausą** tam, kad atvertumėte užklausos tvarkyklės teksto laukelį visam žymos šablonui.
1. Užklausos tvarkyklės teksto laukelyje, **Rūšiavimas** skirtuke įtraukite eilutę su šiais nustatymais:

    - **Lentelė:** *Darbo eilutės*
    - **Išvestinė lentelė:** *Darbo eilutės*
    - **Laukelis:** *Nuorodos krovimo linijos identifikavimo numeris (Record-ID)*
    - **Paieškos kryptis:** *Didėjanti*

1. Pasirinkite **OK** užklausos tvarkyklės teksto langui uždaryti.
1. Pranšimo laukelis paskatins jus patvirtinti grupavimo perkrovimo veiksmą. Pasirinkite **taip** tam, kad tęstumėte.
1. Veiksmų juostoje pasirinkite **bangos žymos šablono grupė**.
1. **bangos žymos šablono grupės** teksto laukelyje, pasirinkite eilutę, kurioje **Nuorodos laukelio pavadinimas** laukelis nustatytas į *Nuorodos krovimo linijos identifikavimo kodas* ir tuomet pasirinkite **Žymos kūrėjo identifikavimo kodas** žymimą laukelį šioje eilutėje.

    > [!NOTE]
    > Šie nustatyimai sukurs vieną žymos seką („Dėžė 1 X“) vienai krovimo linijai bangoje nepriklausomai nuo darbo grupės nustatymų. Ši žymės seka gali būti atspausdinta žymos makete.

### <a name="configure-number-sequence-extensions"></a>Konfigūruokite numerio sekos plėtinius

Numerio sekos plėtiniai valdo GS1 atitiktį su specifinėmis numerio sekomis. Konfigūravimas yra pasirenkamas esamam scenarijui. Dėl platesnės informacijos ir konfigūravimo instrukcijų, žr. [Konfigūruoti numerio sekos plėtinius](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Sukuria prekybos užsakymą ir išleidžia jį į sandėlį

1. Eikite į **Prekyba ir komercija \> Prekybos užsakymas \> Visi prekybos užsakymai**.
1. Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-001*
    - **Sandėlis:** *62*

1. Įtraukite dvi prekybos užsakymo eilutes, turinčias šiuos nustatymus:

    - Prekybos užsakymo linija 1:

        - **Prekės numeris:** *A0001*
        - **Kiekis:** *9024*
        - **Padalinys:** *ea* (9024 ea = 376 dėžė = 47 padėklai)

    - Prekybos užsakymo linija 2:

        - **Prekės numeris:** *A0002*
        - **Kiekis:** *9016*
        - **Padalinys:** *ea* (9016 ea = 322 Box = 46 PL)

    > [!NOTE]
    > Čia pateikiami objektai ir kiekiai yra tik pavyzdžiai. Jie privalo naudoti objekto sekos grupę, kurią nustatėte anksčiau, atitinkantys objekto pakeitimai iš *ea* į *Box* į *PL* turi būti jiems nustatyti ir jie privalo turėti prekių sandėlyje  *62*. Dėl platesnės informacijos, žr. [Matavimo vienetas ir sandėliavimo politika](unit-measure-stocking-policies.md).

1. Pasirinkite prekybos užsakymo liniją 1: Vėliau **Prekybos užsakymo linijos** skyriuje, **Inventoriaus** meniu, pasirinkite **Rezervacijos**.
1. **Rezervacijos** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** ir tuomet uždarykite puslapį.
1. Pakartokite 4 ir 5 žingsnius kiekvienai prekybos užsakymo eilutei 2.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.

    Atistinka šis įvykis:

    - Sistema apdoroja sukurtą siuntimą naudodama šabloną apimantį žymos spausdinimo žingsnį. Žymos maketas bus naudojamas nustatant žymos formatą ir galutinis rezultatas bus žymė turinti penkias eilutes ir ji yra atspausdinta spausdintuve pasirinktame žymos šablone.
    - Bangos žymės yra sukuriamos ir atspausdinamos. Žymių skaičius bus lygus dėžių skaičiui (šiame pavyzdyje, 376 dėžės linijai 1 ir 322 dėžės linijai 2).
    - Naujas važtaraščio identifikavimo kodas sukuriamas siuntimams. Jei sukonfigūravote numerio sekos plėtinius, bangos žymos identifikavimo kodas seks **SSCC-18** numerio formatą. 

Galite peržiūrėti ir iš naujo atspausdinti bangos žymes tolesniuose puslapiuose. Veiksmų juostoje kiekviename puslapyje, **Siuntimai** skirtuke, **Susijusi informacija** grupėje, pasirinkite **Bangos žymės**.

- Visi siuntimai \> Siuntimo informacija
- Visi krovimai \> Krovimo informacija
- Visos bangos
- Bangos žymės
- Bangos žymos retrospektyva

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a>Scenarijus 2: Bangos žymos spausdinimas talpinimui į talpyklas (be bangos žymos įrašų)

Šis scenarijus leidžia jums spausdinti bangos žymes naudojant talpinimą į talpyklas automatiškai skaidyti elementus į dėžės ir dėl to nereikalauja bangos žymos įrašo. Šiuo atveju, talpyklos identifikavimo kodas veikia kaip SSCC žymuo.

Čia pateikiami pagrindiniai skirtumai tarp šio scenarijaus ir scenarijaus 1:

- **Bangos žymos šablonai:** Nepasirinksite bangos žymos tipo bangos žymos šablone ir jums nereikės žymos kūrimo grupavimo. Kitu atveju, jūs konfigūruosite bangos žymos šabloną ir susiesite bangos šabloną tokiu pačiu būdu aprašytu scenarijuje 1. Privalote palikti bangos žymos tipą tuščią, kad apsaugotumėte bangos žymą nuo sukūrimo.
- **Bangos žymos maketai** Sukonfigūruosite bangos žymos maketo eilutės nustatymus darbo linijai vietoje bangos žymos įrašų. Privalote sukonfigūruoti eilutės nustatymus žymos maketui naudodami **WHSWorkLine** lentelę vietoje **WHSWaveLabel** lentelės. **Eilutės puslapyje** nustatymai kontroliuoja eilutės numerius, kuriuos turi vidurinė sritis. 

Šis konfigiūravimas taip pat tinkamas verslo scenarijams, kai daugelis skirtingų objektų yra supakuojami į vieną žymos dėžę ar į padėklą ir toks pakavimo procesas gali būti nustatytas sukuriant darbą (pavyzdžiui, darbą sugrupuotą siuntimo).

Šis scenarijus parodo srautą nuo pradžios iki galo.

### <a name="make-demo-data-available"></a>Demonstracinių duomenų įgalinimas

Šio scenarijaus įgyvendinimui, privalote turėti įdiegtus demo duomenis ir pasirinkti **USMF** juridinį asmenį.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Įsitikinkite, kad bangos žymos metodas yra prieinamas

Jums gali reikėti iš naujo sukurti bangos proceso metodus tam, kad padarytumėte prieinamą bangos etiketės spausdinimo metodą.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Bangos \> Bangos apdorojimo metodai**.
1. Patvirinkite, kad **bangos žymos spausdinimas** yra sąraše. Jei jo nėra, pasirinkite **Iš naujo kurti metodu** veiksmų juostoje ir juos įtraukite.

### <a name="set-up-a-wave-template"></a>Bangos šablono nustatymas

Bangos šablonas leidžia jums susieti konkrečius bangų metodų atvejus pagal atitinkantį bangos žymos šabloną.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.
1. Pasirinkite šabloną, tokį kaip **63 talpinimas į talpyklas**.
1. **Metodai** „FastTab“, patraukite **bangos žymosspausdinimo** metodą į **Pasirinkti metodai** stulpelį.
1. **Pasirinkti metodai** stulpelyje, pasirinkite **bangos žymosspausdinimo** metodą ir nustatykite jo **Bangos žingsnio kodo** laukelį į *Spausdinti žymę*. Dėl išsamesnės informacijos apie bangos žingsnio kodus, žr. [Bangos žingsnio kodai](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Sukurkite bangos žymosmaketą

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Dokumento maršrutas \> bangos žymos maketai**.
1. Sukurkite įrašą, kuris turi šiuos nustatymus:

    - **Žymos maketo identifikavimo numeris:** *Dėžė*
    - **Aprašas:** *Dėžė (SSCC)*

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Veiksmų juostoje pasirinkite **bangos žymoseilutės nustatymai**.

    Pasirodo **bangos žymoseilutės nustatymai** langas. Čia galite sukonfigūruoti dinaminę žymos dalį.

1. Įtraukite eilutę, kuri turi šiuos nustatymus:

    - **Eilutės identifikavimo kodas:** *Darbo eilutė*
    - **Eilutės lentelės pavadinimas:** *WHSWaveLine*
    - **Eilutės pradžios padėtis:** *500*

        Šis laukelis apibrėžia vertikalią padėtį, kurioje eilutė prasideda žymėje.

    - **Eilutės aukštis:** *50*

        Šis laukelis nulemia kiekvienos eilutės aukštį. Eilutės aukštis yra teigiamas horizontalioms žymėms ir neigiamas vertikalioms.

    - **Eilutės puslapyje:** *5*

        Šis laukelis parodo eilučių skaičių, kuris gali būti atspausdintas kiekvienoje žymėje.

        > [!NOTE]
        > Šie nustatymai atspausdins keletą ZPL žymių darbui, kuriose kiekvienas puslapis gali turėti iki penkių darbo eilučių. Pavyzdžiui, jei žymė atspausdinama talpyklai turinčiai 12 eilučių, trys eilutės bus atspausdintos. Jei norite atspausdinti atskirą žymę kiekvienai paėmimo linijai, nustatykite jos vertę į *1*.

1. Uždarykite puslapį.
1. Veiksmų srityje pasirinkite **Redaguoti užklausą**.
1. Užklausos tvarkyklės teksto laukelyje, **Intervalas** skirtuke įtraukite eilutę su šiais nustatymais:

    - **Lentelė:** *Darbo eilutės*
    - **Išvestinė lentelė:** *Darbo eilutės*
    - **Laukas:** *Darbo tipas*
    - **Kriterijai:** *Paėmimas*

1. Jei norite galėti atspausdinti važtaraščio identifikavimo kodą **Sujungimai** skirtuke, pasirinkite **Darbo linijų** lentelę ir prijunkite prie jo **Siuntimai** lentelę.
1. Uždarykite užklausos tvarkylės teksto laukelį.
1. **Spausdintuvo teksto maketas** „FastTab“ turi tris skyrius, kuriuose galite rašyti spausdintuvo kodą: **Antraštės skyrius** , **Vidurinės dalies skyrius** ir **Poraštės skyrius**. **Antraštės skyrius** skyriuje, **Žymos antraštė** laukelyje įveskite ZPL kodą būtinai antraštei. Pavyzdžiui, jei naudojate „Zebra“ spaudintuvus, galite naudoti šį kodą.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. **Vidurinės dalies skyrius** skyriuje, **Žymos vidurinė dalis** laukelyje įveskite ZPL kodą būtinai vidurinei daliai. Toliau pateikiamas pavyzdys.

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. **Vidurinės dalies skyrius** skyriuje, **Žymos apatinė dalis** laukelyje įveskite ZPL kodą būtinai apatinei daliai. Toliau pateikiamas pavyzdys.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Šie nustatymai atspausdins vieną kiekvienos žymos kopiją. Jei jums reikia daugiau kopijų (pavyzdžiui, vienos kopijos vienai padėklo pusei), nustatykite **n** vertę **\^PQn** skyriui poraštėje reikiamam kopijų skaičiui. Pavyzdžiui, keturių kiekvienos žymos kopijų spausdinimui, nustatykite **\^PQ4**.

Jūsų žymė dabar paruošta naudojimui.

### <a name="create-a-wave-label-template"></a>Sukurkite bangos žymosšabloną

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Dokumento maršrutas \> bangos žymosšablonai**.
1. Įtraukite bangos lygio šabloną ir nustatykite šias vertes antraštėje:

    - **Žymos šablono pavadinimas:** *Talpyklų žymės*
    - **Aprašas:** *Talpyklų žymės*
    - **Bangos žingsnio kodas:** *PrintLabel*
    - **Sandėlis:** *63*

1. **Bangos žymos šablono informacijoje** „FastTab“, įtraukite eilutę turinčią šiuos nustatymus:

    - **Žymos maketo identifikavimo numeris:** *Talpykla*
    - **Spausdintuvo pavadinimas:** Pasirinkite tinkamą ZPL spausdintuvą.
    - **Vykdykite užklausą:** *Taip* (Šis pasirinkimas yra pasirenkamas, tačiau rekomenduojamas optimaliam veikimui.)

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Pasirenkamas: Jei nustatote klientui konkretų žymos maketą, privalote sukurti užklausą tam, kad rastumėte kliento paskyrą. **bangos žymos šablono informacijoje** „FastTab“, pasirinkite **Redaguoti užklausą**. Tuomet, užklausos tvarkyklės teksto laukelyje, **Intervalas** skirtuke įtraukite eilutę su šiais nustatymais:

    - **Lentelė:** *Siuntos*
    - **Išvestinė lentelė:** *Siuntos*
    - **Laukelis:** *Paskyros numeris*
    - **Kriterijai:** Įveskite reikiamą kliento paskyros numerį.

    Kai baigsite, pasirinkite **OK** užklausos tvarkyklės teksto langui uždaryti.

### <a name="configure-number-sequence-extensions"></a>Konfigūruokite numerio sekos plėtinius

Numerio sekos plėtiniai valdo GS1 atitiktį su specifinėmis numerio sekomis. Konfigūravimas yra pasirenkamas esamam scenarijui. Dėl platesnės informacijos ir konfigūravimo instrukcijų, žr. [Konfigūruoti numerio sekos plėtinius](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Sukuria prekybos užsakymą ir išleidžia jį į sandėlį

1. Eikite į **Prekyba ir komercija \> Prekybos užsakymas \> Visi prekybos užsakymai**.
1. Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-001*
    - **Sandėlis:** *63*

1. Įtraukite penkias prekybos užsakymo eilutes:

    - Prekybos užsakymo linija 1:

        - **Prekės numeris:** *A0001*
        - **Kiekis:** *10*

    - Prekybos užsakymo linija 2:

        - **Prekės numeris:** *A0002*
        - **Kiekis:** *20*

    - Prekybos užsakymo linija 3:

        - **Prekės numeris:** *L0006*
        - **Kiekis:** *20*

    - Prekybos užsakymo linija 4:

        - **Prekės numeris:** *L0100*
        - **Kiekis:** *40*

    - Prekybos užsakymo linija 5:

        - **Prekės numeris:** *L0101*
        - **Kiekis:** *50*

    > [!NOTE]
    > Čia pateikiami objektai ir kiekiai yra tik pavyzdžiai. Jie turi turėti prekių nurodytame sandėlyje.

1. Pasirinkite prekybos užsakymo liniją 1: Vėliau **Prekybos užsakymo linijos** skyriuje, **Inventoriaus** meniu, pasirinkite **Rezervacijos**.
1. **Rezervacijos** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** ir tuomet uždarykite puslapį.
1. Pakartokite 4 ir 5 žingsnius kiekvienai prekybos užsakymo eilutei.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.

    Atistinka šis įvykis:

    - Sistema apdoroja sukurtą siuntimą naudodama šabloną apimantį žymos spausdinimo žingsnį. Žymos maketas bus naudojamas nustatant žymos formatą ir galutinis rezultatas bus žymė turinti penkias eilutes ir ji yra atspausdinta spausdintuve pasirinktame žymos šablone.
    - Naujas važtaraščio identifikavimo kodas sukuriamas siuntimams. Jei sukonfigūravote numerio sekos plėtinius, bangos žymos identifikavimo kodas seks **SSCC-18** numerio formatą. 

Galite atspausdinti iš naujo šias bangos žymes eidami į **Sandėlio valdymas \> Užklausos ir atsakymai \> Bangos žymos istorija**.

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a>Scenarijus 3: Bangos žymos spausdinimas kelių kainų žymėms

Šis scenarijus rodo, kaip naudoti bangos žymos spausdinimo funkciją, kai sandėlio procesai reikalauja kelių kainų siuntimo žymėms. Pavyzdžiui, atskiros žymos gali turėti spausdinamas dėžės ir padėklus bei tarpo žymė gali būti atspausdinta visam siuntimui. Tarpo žymos yra atskiro tipo žymos, kurios gali būti naudojamos kaip skirtukai tarp ritinių ir konteinerių, tokių kaip žymės siuntimo identifikavimo kodui ir brūkšniniam kodui taip, kad žymės gali būti lengvai rūšiuojamos po jų spausdinimo.

Pagrindinis skirtumas tarp šio scenarijaus konfigūravimo ir scenarijus 1 konfigūravimo, kartu su tuo, kad tarpo žymės yra įjungtos, yra tas, kad daugelis bangos žymių tipų turi būti susieti su bangos žymos šablonais ir padalinio sekos grupės linijomis. Konfigūravimo užbaigimui, nustatykite toliau apteiktus elementus šiame scenarijui:

- **Bangos apdorojimo metodai:** Pažymėsite bangos žymos metodą kaip „pasikartojantį“, įtrauksite jį du (ar daugiau) laikų bangos šablone ir nustatysite skirtingus bangos žingsnio kodus.
- **Bangos žymos šablonai:** Sukonfigūruosite bangos žymos šablonus ir susiesite juos su bangos šablonu. Kiekvienas bangos žymos šablonas turi savo bangos žymostipą.
- **Bangos žymos maketai:** Sukursite keletą bangos žymos maketų. Bus atskiras žymos maketas kiekvienai žymos kainai ir taip pat bus atstumo žymos maketas.

Šis scenarijus parodo srautą nuo pradžios iki galo.

### <a name="make-demo-data-available"></a>Demonstracinių duomenų įgalinimas

Šio scenarijaus įgyvendinimui, privalote turėti įdiegtus demo duomenis ir pasirinkti **USMF** juridinį asmenį.

### <a name="set-up-a-wave-process-method"></a>Nustatykite bangos proceso metodą

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Bangos \> Bangos apdorojimo metodai**.
1. Patvirinkite, kad **bangos žymos spausdinimas** yra sąraše. Jei jo nėra, pasirinkite **Iš naujo kurti metodu** veiksmų juostoje ir juos įtraukite.
1. **Bangos žymos spausdinimo** metodui pasirinkite **Padaryti metodą pasikartojantį** žymimą laukelį.

### <a name="set-up-a-wave-template"></a>Bangos šablono nustatymas

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.
2. Pasirinkite šabloną, tokį kaip **62 siuntimo nustatytąjį**.
3. **Metodai** „FastTab“, patraukite **bangos žymosspausdinimo** metodą į **Pasirinkti metodai** stulpelį.
4. **Pasirinkti metodai** stulpelyje priskirkite **Bangos žingsnio kodo** vertę, tokią kaip *Dėžė* prie **Bangos žymos spausdinimo** metodo. Dėl išsamesnės informacijos apie bangos žingsnio kodus, žr. [Bangos žingsnio kodai](wave-step-codes.md).
5. Patraukite **Bangos žymos spausdinimo** metodą į **Pasirinkti metodai** stulpelį antrą kartą.
6. **Pasirinkti metodai** stulpelyje priskirkite kitą **Bangos žingsnio kodo** vertę, tokią kaip *Padėklas* prie antrojo **Bangos žymos spausdinimo** metodo. Dėl išsamesnės informacijos apie bangos žingsnio kodus, žr. [Bangos žingsnio kodai](wave-step-codes.md).

### <a name="create-three-wave-label-layouts"></a>Sukurkite tris bangos žymių maketus

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Dokumento maršrutas \> bangos žymos maketai**.
1. Sukurkite įrašą, kuris turi šiuos nustatymus:

    - **Žymos maketo identifikavimo numeris:** *Dėžė*
    - **Aprašas:** *Dėžė (SSCC)*

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Veiksmų juostoje pasirinkite **bangos žymoseilutės nustatymai**.

    Pasirodo **bangos žymoseilutės nustatymai** langas. Čia galite sukonfigūruoti dinaminę žymos dalį.

1. Įtraukite eilutę, kuri turi šiuos nustatymus:

    - **Eilutės Identifikavimo kodas:** *Bangos žymė*
    - **Eilutės lentelės pavadinimas:** *WHSWaveLabel*
    - **Eilutės pradžios padėtis:** *0*

        Šis laukelis apibrėžia vertikalią padėtį, kurioje eilutė prasideda žymėje.

    - **Eilutės aukštis:** *0*

        Laukelis apibrėžia kiekvienos eilutės aukštį (taškais) pagal ZPL standartą. Eilutės aukštis yra teigiamas horizontalioms žymėms ir neigiamas vertikalioms. Kadangi yra tik viena eilutė šiame pavyzdyje, galite nustatyti vertę į *0* (nulį).

    - **Eilutės puslapyje:** *1*

        Šis laukelis parodo eilučių skaičių, kuris gali būti atspausdintas kiekvienoje žymėje.

        > [!NOTE]
        > Šis nustatymas nulems, kad atskira ZPL žymė bus spausdinima kiekvienam įrašui bangos žymių lentelėje.

1. Uždarykite puslapį.
1. Veiksmų srityje pasirinkite **Redaguoti užklausą**.
1. Užklausos tvarkyklės teksto laukelyje, **Intervalas** skirtuke įtraukite eilutę su šiais nustatymais:

    - **Lentelė:** *Darbo eilutės*
    - **Išvestinė lentelė:** *Darbo eilutės*
    - **Laukas:** *Darbo tipas*
    - **Kriterijai:** *Paėmimas*

    Ši užklausa užtikrina, kad tik paėmimo tipo darbo linijos bus atspausdintos žymėje, o ne padėjimo tipo darbo linijos.

1. Jei norite galėti atspausdinti važtaraščio identifikavimo kodą **Sujungimai** skirtuke, pasirinkite **Darbo linijų** lentelę ir prijunkite prie jo **Siuntimai** lentelę. 
1. Uždarykite užklausos tvarkylės teksto laukelį.
1. **Spausdintuvo teksto maketas** „FastTab“ turi tris skyrius, kuriuose galite rašyti spausdintuvo kodą: **Antraštės skyrius** , **Vidurinės dalies skyrius** ir **Poraštės skyrius**. **Antraštės skyrius** skyriuje, **Žymos antraštė** laukelyje įveskite ZPL kodą būtinai antraštei. Pavyzdžiui, jei naudojate „Zebra“ spaudintuvus, galite naudoti šį kodą.


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. **Vidurinės dalies skyrius** skyriuje, **Žymos vidurinė dalis** laukelyje įveskite ZPL kodą būtinai vidurinei daliai. Toliau pateikiamas pavyzdys.

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. **Vidurinės dalies skyrius** skyriuje, **Žymos apatinė dalis** laukelyje įveskite ZPL kodą būtinai apatinei daliai. Toliau pateikiamas pavyzdys.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Šie nustatymai atspausdins vieną kiekvienos žymos kopiją. Jei jums reikia daugiau kopijų (pavyzdžiui, vienos kopijos vienai padėklo pusei), nustatykite **n** vertę **\^PQn** skyriui poraštėje reikiamam kopijų skaičiui. Pavyzdžiui, keturių kiekvienos žymos kopijų spausdinimui, nustatykite **\^PQ4**.

1. Pirmoji žymė dabar paruošta naudojimui.
1. Sukurkite antrą maketo įrašą, kuris turi šiuos nustatymus:

    - **Žymėas maketo identifikavimo numeris:** *Padėklas*
    - **Aprašas:** *Padėklas*

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Veiksmų juostoje pasirinkite **bangos žymoseilutės nustatymai**.

    Pasirodo **bangos žymoseilutės nustatymai** langas. Čia galite sukonfigūruoti dinaminę žymos dalį.

1. Įtraukite eilutę, kuri turi šiuos nustatymus:

    - **Eilutės Identifikavimo kodas:** *Bangos žymė*
    - **Eilutės lentelės pavadinimas:** *WHSWaveLabel*
    - **Eilutės pradžios padėtis:** *0*

        Šis laukelis apibrėžia vertikalią padėtį, kurioje eilutė prasideda žymėje.

    - **Eilutės aukštis:** *0*

        Laukelis apibrėžia kiekvienos eilutės aukštį (taškais) pagal ZPL standartą. Eilutės aukštis yra teigiamas horizontalioms žymėms ir neigiamas vertikalioms. Kadangi yra tik viena eilutė šiame pavyzdyje, galite nustatyti vertę į *0* (nulį).

    - **Eilutės puslapyje:** *1*

        Šis laukelis parodo eilučių skaičių, kuris gali būti atspausdintas kiekvienoje žymėje.

        > [!NOTE]
        > Šis nustatymas nulemia, kad atskira ZPL žymė bus spausdinima kiekvienam įrašui bangos žymių lentelėje.

1. Uždarykite puslapį.
1. Veiksmų srityje pasirinkite **Redaguoti užklausą**.
1. Užklausos tvarkyklės teksto laukelyje, **Intervalas** skirtuke įtraukite eilutę su šiais nustatymais:

    - **Lentelė:** *Darbo eilutės*
    - **Išvestinė lentelė:** *Darbo eilutės*
    - **Laukas:** *Darbo tipas*
    - **Kriterijai:** *Paėmimas*

    Ši užklausa užtikrina, kad tik paėmimo tipo darbo linijos bus atspausdintos žymėje, o ne padėjimo tipo darbo linijos.

1. Jei norite galėti atspausdinti važtaraščio identifikavimo kodą **Sujungimai** skirtuke, pasirinkite **Darbo linijų** lentelę ir prijunkite prie jo **Siuntimai** lentelę.
1. Uždarykite užklausos tvarkylės teksto laukelį.
1. **Spausdintuvo teksto maketas** „FastTab“ turi tris skyrius, kuriuose galite rašyti spausdintuvo kodą: **Antraštės skyrius** , **Vidurinės dalies skyrius** ir **Poraštės skyrius**. **Antraštės skyrius** skyriuje, **Žymos antraštė** laukelyje įveskite ZPL kodą būtinai antraštei. Pavyzdžiui, jei naudojate „Zebra“ spaudintuvus, galite naudoti šį kodą.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. **Vidurinės dalies skyrius** skyriuje, **Žymos vidurinė dalis** laukelyje įveskite ZPL kodą būtinai vidurinei daliai. Toliau pateikiamas pavyzdys.

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. **Vidurinės dalies skyrius** skyriuje, **Žymos apatinė dalis** laukelyje įveskite ZPL kodą būtinai apatinei daliai. Toliau pateikiamas pavyzdys.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Šie nustatymai atspausdins vieną kiekvienos žymos kopiją. Jei jums reikia daugiau kopijų (pavyzdžiui, vienos kopijos vienai padėklo pusei), nustatykite **n** vertę **\^PQn** skyriui poraštėje reikiamam kopijų skaičiui. Pavyzdžiui, keturių kiekvienos žymos kopijų spausdinimui, nustatykite **\^PQ4**.

1. Antroji žymė dabar paruošta naudojimui.
1. Sukurkite trečią maketo įrašą, kuris turi šiuos nustatymus:

    - **Žymėas maketo identifikavimo numeris:** *Tarpas*
    - **Aprašas:** *Tarpo žymė*

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. **Spausdintuvo teksto maketas** „FastTab“ turi tris skyrius, kuriuose galite rašyti spausdintuvo kodą: **Antraštės skyrius** , **Vidurinės dalies skyrius** ir **Poraštės skyrius**. **Antraštės skyrius** skyriuje, **Žymos antraštė** laukelyje įveskite ZPL kodą būtinai antraštei. Toliau pateikiamas pavyzdys.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. Šįkart, nereikia jokios vidurinės dalies. Dėl to, tiesiog įveskite būtiną tekstą **Poraštės skyrius** skyriuje. Toliau pateikiamas pavyzdys.

    ```plaintext
    ^XZ
    ```

    Trečioji žymė dabar paruošta naudojimui.

    > [!NOTE]
    > Ši trečioji etiketė yra žymos tarpas, kuris bus naudojamas atskirti žymių ritinius.

### <a name="create-two-wave-label-types"></a>Sukurkite du bangos žymių tipus

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Dokumento maršrutas \> bangos žymostipai**.
1. Sukurkite įrašą, kuris turi šiuos nustatymus:

    - **Žymos tipas:** *Dėžė*
    - **Aprašas:** *Dėžė*

1. Sukurkite antrą įrašą, kuris turi šiuos nustatymus:

    - **Žymos tipas:** *Padėklas*
    - **Aprašas:** *Padėklas*

### <a name="set-up-unit-sequence-groups"></a>Nustatyti vienetų sekų grupes

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Sandėlis \> Padalinio sekos grupės**.
1. Pasirinkite ar sukurkite **Ea Box PL** grupę.
1. **Dėžutė** linijoje nustatykite **Bangos lygio tipas** laukelį į *Dėžė*.
1. **PL** linijoje nustatykite **Bangos lygio tipas** laukelį į *Padėklas*.

### <a name="create-wave-label-templates"></a>Sukurkite bangos žymos šablonus

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Dokumento maršrutas \> bangos žymosšablonai**.
1. Sukurkite žymos šabloną, kuris turi šiuos nustatymus:

    - **Žymos šablono pavadinimas:** *Dėžių žymės*
    - **Aprašas:** *Dėžės žymės*
    - **Bangos žingsnio kodas:** *Dėžė*
    - **Sandėlis:** *62*

1. **Bendra** „FastTab“, nustatykite **Bangos žymos tipas** laukelyje pasirinkite vertę, tokią kaip *Dėžė*.
1. **Bangos žymos šablono informacijoje** „FastTab“, įtraukite eilutę turinčią šiuos nustatymus:

    - **Žymos maketo identifikavimo numeris:** *Dėžė*
    - **Spausdintuvo pavadinimas:** Pasirinkite tinkamą ZPL spausdintuvą.
    - **Vykdykite užklausą:** *Taip* (Šis pasirinkimas yra pasirenkamas, tačiau rekomenduojamas optimaliam veikimui.)

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Pasirenkamas: Jei nustatote klientui konkretų žymos maketą, privalote sukurti užklausą tam, kad rastumėte kliento paskyrą. **bangos žymos šablono informacijoje** „FastTab“, pasirinkite **Redaguoti užklausą**. Tuomet, užklausos tvarkyklės teksto laukelyje, **Intervalas** skirtuke įtraukite eilutę su šiais nustatymais:

    - **Lentelė:** *Siuntos*
    - **Išvestinė lentelė:** *Siuntos*
    - **Laukelis:** *Paskyros numeris*
    - **Kriterijai:** Įveskite reikiamą kliento paskyros numerį.

    Kai baigsite, pasirinkite **OK** užklausos tvarkyklės teksto langui uždaryti.

1. Veiksmų juostoje pasirinkite **Redaguoti užklausą** tam, kad atvertumėte užklausos tvarkyklės teksto laukelį visam žymos šablonui.
1. Užklausos tvarkyklės teksto laukelyje, **Rūšiavimas** skirtuke įtraukite eilutę su šiais nustatymais:

    - **Lentelė:** *Darbo eilutės*
    - **Išvestinė lentelė:** *Darbo eilutės*
    - **Laukelis:** *Nuorodos krovimo linijos identifikavimo numeris (Record-ID)*
    - **Paieškos kryptis:** *Didėjanti*

1. Įtraukite antrą eilutę, kuri turi šiuos nustatymus:

    - **Lentelė:** *Darbo eilutės*
    - **Išvestinė lentelė:** *Darbo eilutės*
    - **Laukas:** *Siuntos ID*
    - **Paieškos kryptis:** *Didėjanti*

1. Pasirinkite **OK** užklausos tvarkyklės teksto langui uždaryti.
1. Pranšimo laukelis paskatins jus patvirtinti grupavimo perkrovimo veiksmą. Pasirinkite **taip** tam, kad tęstumėte.
1. Veiksmų juostoje pasirinkite **bangos žymos šablono grupė**.
1. **Bangos žymos šablono grupės** teksto laukelyje, pasirinkite eilutę, kurioje **Nuorodos laukelio pavadinimas** laukelis nustatytas į *Siuntimo identifikavimo kodas* , nustatykite šias vertes:

    - **Spausdinimo tarpo žymė:** Pasirinkite šį žymimą laukelį.
    - **Žymos maketo identifikavimo kodas:** Pasirinkite tarpo žymę. (Pavyzdžiui, pasirinkite *Tarpo* žymos maketą, kurį sukūrėte anksčiau šiame scnarijuje.)
    - **Spausdintuvo pavadinimas:** Pasirinkite spausdintuvą tarpo žymei. (Dažniausiai, dėl žymių ritinių skaidymo tikslų, turite pasirinkti tą patį spausdintuvą, kuris pasirinktas **Bangos žymos šablono informacijos** „FastTab“. Nepaisant to, kiti scenarijai yra galimi.)

1. Eilutėje, kurioje **Nuorodos žymos pavadinimas** laukelis nustatytas *Nuorodos krovimo linijos identifikavimo kodas* , pasirinkite **Žymos kūrėjo identifikavimo kodas** žymimą laukelį.

    > [!NOTE]
    > Šie nustatyimai sukurs vieną žymos seką („Dėžė 1 X“) vienai krovimo linijai bangoje nepriklausomai nuo darbo grupės nustatymų. Ši žymos seka gali būti atspausdinta viename žymos makete. Taip pat, žymos skirtingiems siuntimams bus atskirtos pasirinkta tarpo žyme.

1. Pasirinkite **OK** tam, kad uždarytumėte **Bangos žymos šablono grupės** teksto laukelį.
1. Sukurkite antrą žymos šabloną, kuris turi šiuos nustatymus:

    - **Žymos šablono pavadinimas:** *Padėklo žymės*
    - **Aprašas:** *Padėklo žymos*
    - **Bangos žingsnio kodas:** *Padėklas*
    - **Sandėlis:** *62*

1. **Bendra** „FastTab“, nustatykite **Bangos žymos tipas** laukelyje pasirinkite vertę, tokią kaip *Padėklas*.
1. **Bangos žymos šablono informacijoje** „FastTab“, įtraukite eilutę turinčią šiuos nustatymus:

    - **Žymėas maketo identifikavimo numeris:** *Padėklas*
    - **Spausdintuvo pavadinimas:** Pasirinkite tinkamą ZPL spausdintuvą.
    - **Vykdykite užklausą:** *Taip* (Šis pasirinkimas yra pasirenkamas, tačiau rekomenduojamas optimaliam veikimui.)

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Pasirenkamas: Jei nustatote klientui konkretų žymos maketą, privalote sukurti užklausą tam, kad rastumėte kliento paskyrą. **bangos žymos šablono informacijoje** „FastTab“, pasirinkite **Redaguoti užklausą**. Tuomet, užklausos tvarkyklės teksto laukelyje, **Intervalas** skirtuke įtraukite eilutę su šiais nustatymais:

    - **Lentelė:** *Siuntos*
    - **Išvestinė lentelė:** *Siuntos*
    - **Laukelis:** *Paskyros numeris*
    - **Kriterijai:** Įveskite reikiamą kliento paskyros numerį.

    Kai baigsite, pasirinkite **OK** užklausos tvarkyklės teksto langui uždaryti. 

1. Veiksmų juostoje pasirinkite **Redaguoti užklausą** tam, kad atvertumėte užklausos tvarkyklės teksto laukelį visam žymos šablonui.
1. Užklausos tvarkyklės teksto laukelyje, **Rūšiavimas** skirtuke įtraukite eilutę su šiais nustatymais:

    - **Lentelė:** *Darbo eilutės*
    - **Išvestinė lentelė:** *Darbo eilutės*
    - **Laukelis:** *Nuorodos krovimo linijos identifikavimo numeris (Record-ID)*
    - **Paieškos kryptis:** *Didėjanti*

1. Įtraukite antrą eilutę, kuri turi šiuos nustatymus:

    - **Lentelė:** *Darbo eilutės*
    - **Išvestinė lentelė:** *Darbo eilutės*
    - **Laukas:** *Siuntos ID*
    - **Paieškos kryptis:** *Didėjanti*

1. Pasirinkite **OK** užklausos tvarkyklės teksto langui uždaryti.
1. Pranšimo laukelis paskatins jus patvirtinti grupavimo perkrovimo veiksmą. Pasirinkite **taip** tam, kad tęstumėte.
1. Veiksmų juostoje pasirinkite **bangos žymos šablono grupė**.
1. **Bangos žymos šablono grupės** teksto laukelyje, pasirinkite eilutę, kurioje **Nuorodos laukelio pavadinimas** laukelis nustatytas į *Siuntimo identifikavimo kodas* , nustatykite šias vertes:

    - **Spausdinimo tarpo žymė:** Pasirinkite šį žymimą laukelį.
    - **Žymos maketo identifikavimo kodas:** Pasirinkite tarpo žymę. (Pavyzdžiui, pasirinkite *Tarpo* žymos maketą, kurį sukūrėte anksčiau šiame scnarijuje.)
    - **Spausdintuvo pavadinimas:** Pasirinkite spausdintuvą tarpo žymei. (Dažniausiai, dėl žymių ritinių skaidymo tikslų, turite pasirinkti tą patį spausdintuvą, kuris pasirinktas **Bangos žymos šablono informacijos** „FastTab“. Nepaisant to, kiti scenarijai yra galimi.)

1. Eilutėje, kurioje **Nuorodos žymos pavadinimas** laukelis nustatytas *Nuorodos krovimo linijos identifikavimo kodas* , pasirinkite **Žymos kūrėjo identifikavimo kodas** žymimą laukelį.

    > [!NOTE]
    > Šie nustatyimai sukurs vieną žymos seką („Dėžė 1 X“) vienai krovimo linijai bangoje nepriklausomai nuo darbo grupės nustatymų. Ši žymos seka gali būti atspausdinta viename žymos makete. Taip pat, žymos skirtingiems siuntimams bus atskirtos pasirinkta tarpo žyme.

### <a name="configure-number-sequence-extensions"></a>Konfigūruokite numerio sekos plėtinius

Numerio sekos plėtiniai valdo GS1 atitiktį su specifinėmis numerio sekomis. Konfigūravimas yra pasirenkamas esamam scenarijui. Dėl platesnės informacijos ir konfigūravimo instrukcijų, žr. [Konfigūruoti numerio sekos plėtinius](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Sukuria prekybos užsakymą ir išleidžia jį į sandėlį

1. Eikite į **Prekyba ir komercija \> Prekybos užsakymas \> Visi prekybos užsakymai**.
1. Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-001*
    - **Sandėlis:** *62*

1. Įtraukite dvi prekybos užsakymo eilutes:

    - Prekybos užsakymo linija 1:

        - **Prekės numeris:** *A0001*
        - **Kiekis:** *9024*
        - **Padalinys:** *ea* (9024 ea = 376 dėžė = 47 padėklai)

    - Prekybos užsakymo linija 2:

        - **Prekės numeris:** *A0002*
        - **Kiekis:** *9016*
        - **Padalinys:** *ea* (9016 ea = 322 Box = 46 PL)

    > [!NOTE]
    > Čia pateikiami objektai ir kiekiai yra tik pavyzdžiai. Jie privalo naudoti objekto sekos grupę, kurią nustatėte anksčiau, atitinkantys objekto pakeitimai iš *ea* į *Box* į *PL* turi būti jiems nustatyti ir jie privalo turėti prekių sandėlyje  *62*. Dėl platesnės informacijos, žr. [Matavimo vienetas ir sandėliavimo politika](unit-measure-stocking-policies.md).

1. Pasirinkite prekybos užsakymo liniją 1: Vėliau **Prekybos užsakymo linijos** skyriuje, **Inventoriaus** meniu, pasirinkite **Rezervacijos**.
1. **Rezervacijos** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** ir tuomet uždarykite puslapį.
1. Pakartokite 4 ir 5 žingsnius kiekvienai prekybos užsakymo eilutei 2.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.

    Atistinka šis įvykis: 

    - Sistema apdoroja sukurtą siuntimą naudodama šabloną apimantį žymos spausdinimo žingsnį. Žymos maketas bus naudojamas nustatant žymos formatą ir galutinis rezultatas bus žymė turinti penkias eilutes ir ji yra atspausdinta spausdintuve pasirinktame žymos šablone.
    - Bangos žymės yra sukuriamos ir atspausdinamos. Žymių skaičius bus lygus dėžių skaičiui (pavyzdžiui, šiuo atveju 376 dėžės žymai eilutėje 1, 322 dėžės žymei linijoje 2, 47 padėklai žymos linijoje 1, 47 padėklai žymos linijoje 2 ir dvi tarpų žymos turinčios siuntimo identifikavimo kodą).
    - Naujas važtaraščio identifikavimo kodas sukuriamas siuntimams. Jei sukonfigūravote numerio sekos plėtinius, bangos žymos identifikavimo kodas seks **SSCC-18** numerio formatą. 

Galite peržiūrėti ir iš naujo atspausdinti bangos etiketes tolesniuose puslapiuose:

- Visi siuntimai \> Siuntimo informacija
- Visi krovimai \> Krovimo informacija
- Visos bangos
- Bangos žymės
- Bangos žymos retrospektyva

Didžiojoje dalyje šių puslapių, galite rasti atitinkamą funkciją pasirinkę **Bangos žymės**  **Susijusi informacija** grupėje **Siuntimai** skirtuke veiksmų juostoje.
