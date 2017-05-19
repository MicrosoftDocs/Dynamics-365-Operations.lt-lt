---
title: "Mažmeninės prekybos periferinis simuliatorius"
description: "Šioje temoje aprašomas kartu su „Microsoft Dynamics 365 for Operations“ – versija „Retail“ pateikiamas periferinio simuliatoriaus įrankis."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 11a4633b0a1254f3a8cbdcba8d7aa99bb7c936c1
ms.contentlocale: lt-lt
ms.lasthandoff: 04/26/2017


---

# <a name="retail-peripheral-simulator"></a>Mažmeninės prekybos periferinis simuliatorius

[!include[banner](includes/banner.md)]


Šioje temoje aprašomas kartu su „Microsoft Dynamics 365 for Operations“ – versija „Retail“ pateikiamas periferinio simuliatoriaus įrankis.

<a name="overview"></a>Apžvalga
--------

„Microsoft Dynamics 365 for Operations“ – versijos „Retail“ periferinis simuliatorius yra įrankis, kuris padeda nustatyti, tikrinti mažmeninės prekybos aplinkose naudojamus periferinius įrenginius ir šalinti jų triktis. Periferinį simuliatorių galite naudoti norėdami supaprastinti mažmeninės prekybos periferinių įrenginių tikrinimą ir atskirti dėl netinkamos sąrankos arba netinkamai veikiančių įrenginių tvarkyklių atsiradusias problemas. Į periferinio simuliatoriaus sudėtį įeina darbalaukio programa, kurioje pateikiamos virtualios „Dynamics 365 for Operations“ – versijos „Retail“ palaikomų įrenginių versijos. Kiekvieno virtualaus įrenginio skyriuje rodoma įrenginio ir mažmeninės prekybos elektroninio kasos aparato (EKA) sąveika. Jį taip pat galite naudoti norėdami pateikti keliems EKA scenarijams tinkančią įvestį. Periferinis simuliatorius palaiko EKA ir toliau nurodytų virtualių įrenginių sąveiką.

-   **Spausdintuvas** – periferinis simuliatorius gali rodyti EKA spausdintuvui sukonfigūruotus gavimo kvitus.
-   **Eilutės rodinys** – galite sukonfigūruoti, kad virtualiame eilutės rodinyje būtų rodoma faktinio eilutės rodinio veikla.
-   **Magnetinės juostelės skaitytuvas (MSR)** – iš periferinio simuliatoriaus į EKA galite siųsti imituojamus magnetinės juostelės įvykius.
-   **Stalčius** – galite imituoti faktinį grynųjų pinigų stalčių.
-   **2 stalčius** – nustatydami antrą periferinio simuliatoriaus grynųjų pinigų stalčių galite imituoti scenarijus, kuriuose nurodomas vienas, bet dviejomis aktyviomis pamainomis veikiantis EKA registras.
-   **Skaitytuvas** – periferinio simuliatoriaus palaikomas virtualus brūkšninių kodų skaitytuvas gali pateikti brūkšninio kodo nuskaitymo įvykius.
-   **Svarstyklės** – naudodami virtualias svarstykles su elektroniniu kasos aparatu (EKA) galite imituoti pasvertų elementų sąveiką.
-   **Asmeninio identifikavimo numerio (PIN) rinkiklis** – galite simuliuoti PIN rinkiklio operacijas. **Pastaba.** Per mokėjimo jungtį turite įdiegti faktinio PIN rinkiklio palaikymą.
-   **Parašo fiksavimas** – periferinis simuliatorius turi virtualų parašo fiksavimo įrenginį ir galite nustatyti, kad jis paragintų pateikti kai kurioms priemonėms, pavyzdžiui, kliento sąskaitos mokėjimams reikiamus parašus.

Periferinį simuliatorių taip pat galite naudoti norėdami imituoti iš brūkšninių kodų skaitytuvo ir MSR kilusius klavišinius kredito kortelių skaitytuvo įvykius. Virtualus periferinis simuliatorius palaiko būtent EKA skirto objektų susiejimo ir įdėjimo (OEKA) įrenginius.

## <a name="key-scenarios"></a>Pagrindiniai scenarijai
### <a name="troubleshooting"></a>Trikčių šalinimas

Periferinį simuliatorių galite naudoti norėdami šalinti įrenginio sąrankos triktis. Jei neturite periferinio simuliatoriaus arba antro tos pačios klasės įrenginio, gali būti sunku nustatyti, kas sukėlė problemą. Tačiau, jei turite periferinį simuliatorių, galite nustatyti virtualius įrenginius ir naudoti tuos pačius kodų maršrutus ir verslo logiką, kurie naudojami faktiniams įrenginiams. Periferinio simuliatoriaus atžvilgiu pagrindinis skirtumas tarp virtualių įrenginių ir faktinių įrenginių yra aptarnavimo objektas arba įrenginio tvarkyklė. Faktinių įrenginių aptarnavimo objektą pateikia įrenginio gamintojas. O periferinių simuliatorių aptarnavimo objektai pateikiami kaip periferinio simuliatoriaus dalis. Kai periferinis simuliatorius veikia tinkamai, jeigu įrenginys neveikia tinkamai po to, kai aparatūros šablone nurodytas įrenginio pavadinimas pakeičiamas į faktinį įrenginio pavadinimą, galite manyti, kad įvyko klaida, susijusi su gamintojo pateiktu aptarnavimo objektu.

### <a name="training"></a>Mokymasis

Galite naudoti periferinį simuliatorių norėdami įtraukti realistinį kasininkų mokymo sluoksnį, kai galima naudoti fizinės aparatūros sąranką. Kai periferinis simuliatorius įtraukiamas į mokymo scenarijus, kasininkas gali efektyviau sąveikauti su EKA pateikdamas įvestį, pavyzdžiui, produkto brūkšninio kodo nuskaitymus ir dovanų kortelės braukimus ir stebėdamas, kurie kvitai spausdinami atliekant tam tikrą operaciją.

### <a name="testing"></a>Bandymai

Naudodami periferinį simuliatorių galite patikrinti produktų brūkšninius kodus, kvitų formatus ir pan. ir virtualioje aplinkoje jums nereikės diegti fizinės aparatūros. Kadangi nereikia fizinės aparatūros ir aparatūros stotyje arba fiziniame kompiuteryje nebūtina įdiegti EKA kliento, galite greičiau patikrinti tarnybiniame biure atliekamus pakeitimus.

## <a name="set-up-the-peripheral-simulator"></a>Periferinio simuliatoriaus sąranka
### <a name="set-up-a-hardware-profile"></a>Aparatūros šablono nustatymas

1.  Norėdami nustatyti periferinį simuliatorių, eikite į **Mažmeninė prekyba ir prekyba** &gt; **Kanalo nustatymas** &gt; **EKA sąranka** &gt; **EKA šablonai** &gt; **Aparatūros šablonai**.
2.  Norėdami sukurti naują šabloną, spustelėkite **Naujas**.
3.  Įveskite laukų **Šablono numeris** ir **Aprašas** vertes.
4.  Naudodami toliau pateiktą lentelę nustatykite virtualiuosius įrenginius, kuriuos būtina patikrinti. Toliau pateikiamas lentelės stulpelių paaiškinimas.
    -   **Įrenginys** – šiame stulpelyje pateikiamas skirtuko „FastTab“, kurį išplečiate norėdami nustatyti įrenginį, pavadinimas.
    -   **Įrenginio tipas** – šiame stulpelyje pateikiama vertė, kurią pasirenkate įrenginio pavadinimu pažymėtame lauke.
    -   **Įrenginio pavadinimas** – šiame stulpelyje pateikiama tiksli jūsų įvesta įrenginio pavadinimo vertė. **Svarbu:** čia pateikti įrenginio pavadinimai yra būtini, nes aparatūros stotis naudoja šiuos konkrečius pavadinimus kreipdamasi į įrenginius. Jei nenaudosite šių konkrečių pavadinimų, įrenginio nebus galima naudoti.

    | Įrenginys            | Įrenginio tipas | Įrenginio pavadinimas              |
    |-------------------|-------------|--------------------------|
    | Spausdintuvas           | OEKA        | „MockOPOSPrinter“          |
    | Eilutės rodymas      | OEKA        | „MockOPOSLineDisplay“      |
    | MSR               | OEKA        | „MockOPOSMSR“              |
    | Išdavėjas            | OEKA        | „MockOPOSDrawer1“          |
    | 2 stalčius           | OEKA        | „MockOPOSDrawers“          |
    | Skaitytuvas           | OEKA        | „MockOPOSScanner“          |
    | Mastelis             | OEKA        | „MockOPOSScale“            |
    | PIN rinkiklis           | OEKA        | „MockOPOSPinPad“           |
    | Parašo fiksavimas | OEKA        | „MockOPOSSignatureCapture“ |

**Pastaba.** Norint imituoti iš brūkšninių kodų skaitytuvo ir MSR kilusius klavišinius kredito kortelių skaitytuvo įvykius speciali aparatūros šablono sąranka nereikalinga.

### <a name="assign-the-hardware-profile-to-a-register"></a>Aparatūros šablono priskyrimas registrui

1.  Sukūrę aparatūros šabloną eikite į **Mažmeninė prekyba ir prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **Registrai**.
2.  Sąraše **EKA registrai** spustelėkite registro, kuris turėtų naudoti periferinį simuliatorių, lauke **Registro numeris** esančią nuorodą.
3.  Spustelėkite **Redaguoti**.
4.  Skyriaus **Šablonai** lauke **Aparatūros šablonas** pasirinkite virtualiems periferiniams įrenginiams sukurtą aparatūros šabloną.
5.  Spustelėkite **Įrašyti**.

### <a name="synchronize-changes-to-the-channel-database"></a>Pakeitimų sinchronizavimas su kanalų duomenų baze

1.  Eikite į **Mažmeninė prekyba ir komercija** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikas**.
2.  Pasirinkite **1090** paskirstymo grafiką.
3.  Spustelėję **Vykdyti dabar** sinchronizuokite EKA pakeitimus.

Susinchronizavus duomenis naujas aparatūros šablonas ir registre atlikti pakeitimai pateikiami kanalų duomenų bazėje.

## <a name="install-the-peripheral-simulator"></a>Periferinio simuliatoriaus diegimas
1.  Eikite į **Mažmeninė prekyba ir prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA šablonai** &gt; **Aparatūros šablonai**.
2.  Spustelėkite **Atsisiųsti**, o po to spustelėkite **PeripheralSimulator**. **Pastaba.** Tam, kad galėtumėte atsisiųsti periferinį simuliatorių, turite išjungti iššokančių langų blokavimo programas.
3.  Kai siuntimas bus baigtas, atidarykite aplanką **Atsisiuntimai** ir dukart spustelėję **VirtualPeripherals.msi** paleiskite diegimo programą.
4.  Įdiekite periferinį simuliatorių naudodami numatytuosius parametrus.

Be periferinio simuliatoriaus iš „Monroe Consulting Services“ turite įdiegti bendruosius valdymo objektus. Priešingu atveju periferinis simuliatorius veiks netinkamai. Norėdami atsisiųsti bendruosius valdymo objektus, eikite į <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Periferinio simuliatoriaus naudojimas
Norėdami paleisti periferinį simuliatorių, savo kompiuteryje spustelėkite **Pradžia**, įveskite **Mažmeninės prekybos periferinis simuliatorius**, o po to pasirodžius rezultatų sąrašui pasirinkite programą. Paleidę periferinį simuliatorių spustelėkite įrenginio pavadinimą, kad pamatytumėte palaikomus įrenginius. Šie įrenginiai išvardijami kaip skirtukai ir jų sąrašas pateikiamas kairėje lango pusėje. Norėdami peržiūrėti tam tikrą įrenginį, spustelėkite to įrenginio skirtuką.

### <a name="line-display-capabilities"></a>Eilutės rodinio galimybės

Eilutės rodinys yra pirmasis įrenginys periferinio simuliatoriaus sąraše. Kai sukonfigūruotas virtualus eilutės rodinys, eilutės elementai jame rodomi taip, kaip buvo nuskaityti atliekant EKA operaciją. Be eilutės elementų rodinyje rodoma bendra suma, kuri turi susidaryti pasirinkus EKA mokėjimo priemonę. Jame taip pat rodoma balansinė suma, kuri turi susidaryti, jeigu įvedama mokėjimo priemonė, bet dar galioja operacijos balansinė suma. Kai EKA nenaudojamas, gali būti rodomas pranešimas, kuriame nurodoma, kad kasos stalčiaus skyrelis uždarytas. Turite sukonfigūruoti pranešimą aparatūros šablono dalies **Eilutės rodinys** skirtuke „FastTab“.

### <a name="cash-drawer-capabilities"></a>Kasos stalčiaus galimybės

Kasos stalčius yra antras įrenginys periferinio simuliatoriaus sąraše. Kai sukonfigūruota, kad aparatūros šablonas naudotų virtualius grynųjų pinigų stalčius, EKA atidaro aktyviosios pamainos grynųjų pinigų stalčių, kai atliekamos stalčiaus operacijos, pavyzdžiui, mokėjimo priemonių deklaravimai, ir tada kasininkas gali pakeisti arba įdėti grynųjų pinigų atlikdamas standartines atsiskaitymo grynaisiais pinigais operacijas. Virtualūs grynųjų pinigų stalčiai pažymėti etiketėmis **Pagrindinis stalčius** ir **Antrinis stalčius**. Šios etiketės atitinka atitinkamas aparatūros šablono reikšmes Stalčius ir 2 stalčius. Uždarius stalčių rodomas uždaryto grynųjų pinigų stalčiaus vaizdas, o uždaryto grynųjų pinigų stalčiaus mygtuko etiketė pažymima užrašu **Atidaryti stalčių**. Spustelėjus šį mygtuką vaizdas pakeičiamas atidaryto grynųjų pinigų stalčiaus vaizdu, nurodančiu, kad stalčius dabar atidarytas. Atidaryto grynųjų pinigų stalčiaus mygtuko etiketė pažymima **Uždaryti stalčių**. Atlikus kelias EKA operacijas grynųjų pinigų stalčius gali atsidaryti. Esant atidarytam grynųjų pinigų stalčiui daugumos operacijų atlikti negalima. Išimtys suteikiamos kai kurioms dienos pabaigos procedūroms. Jei EKA vartotojas gauna klaidos pranešimą, kuriame nurodoma, kad operacijos negalima atlikti kol atidarytas grynųjų pinigų stalčius, norėdamas tęsti vartotojas turi uždaryti virtualų arba faktinį grynųjų pinigų stalčių. Jeigu aparatūros šablone grynųjų pinigų stalčius pažymėtas užrašu **Bendrai naudojamas**, sistema netikrina, ar prieš atliekant operaciją stalčius uždarytas. Operacija atliekama kaip įprasta, net jei grynųjų pinigų stalčius atidarytas. Tokiu būdu palaikomi scenarijai, kai grynųjų pinigų stalčius bendrai naudoja pardavimų partneriai ir kai vienas partneris naudoja grynųjų pinigų stalčių, o kitas savo EKA įrenginyje atlieka nesusijusias užduotis. Atlikti kasos stalčiaus pakeitimai nėra matomi tol, kol neuždaroma dabartinė pamaina ir neatidaroma nauja pamaina.

### <a name="msr-capabilities"></a>MSR galimybės

Kadangi periferinis simuliatorius veikia ir naudojant OPOS režimą, ir klavišinį kredito kortelių skaitytuvo režimą, jis palaiko virtualias MSR operacijas. Jei naudojamas OPOS režimas, reikia, kad naudojant aparatūros šabloną MSR būtų sukonfigūruotas veikti kaip OPOS įrenginys. Naudojant klavišinį kredito kortelių skaitytuvo režimą klavišinio kredito kortelių skaitytuvo duomenų įvykiai tiesiog siunčiami į „Microsoft Windows“. OEKA ir klavišinis kredito kortelių skaitytuvo režimas skiriasi ne tik sąranka, bet ir šiais požymiais:

-   Naudojant EKA klientą OEKA MSR įrenginiuose galima naudoti specialius scenarijus, pavyzdžiui, scenarijus, kuriuos naudojant leidžiama įvesti magnetinės juostos duomenų lojalumo arba dovanų kortelės numerį.
-   Naudojant klavišinį kredito kortelių skaitytuvo režimą periferinis simuliatorius siunčia klavišinio kredito kortelių skaitytuvo duomenis į lauką, kuris aktyvus siunčiant duomenis. Šis elgesys panašus į elgesį, kai duomenys įvedami naudojant klaviatūrą. Norėdamas naudoti MSR kaip klavišinį kredito kortelių skaitytuvą, vartotojas privalo įjungti „Retail Modern POS“ (MPOS), kad įsitikintų, jog duomenys gauti tinkamame lauke. Todėl galite sukonfigūruoti atidėjimą, kad vartotojas turėtų laiko įsitikinti, kad duomenys bus nusiųsti į tinkamą lauką.

#### <a name="testing-gift-and-payment-card-swipes"></a>Braukimas bandymo dovanos ir mokėjimo kortele

Naudodami virtualųjį periferinio simuliatoriaus pateikiamą MSR taip pat galite sukonfigūruoti specialius MSR duomenis, kad patikrintumėte braukimo dovanų ir mokėjimo kortelėmis scenarijus. Norėdami sukurti kortelę, spustelėkite pliuso ženklu (**+**) pažymėtą mygtuką ir pasirinkite kortelės tipą. Po to nurodykite kortelės numerį arba sekimo duomenis, kurie turi būti siunčiami į EKA, taip pat nurodant reikiamos kortelės galiojimo pabaigos mėnesį ir metus. Lauke **Kortelės tipas** pasirinkta vertė yra tiesiog etiketė, kurią galima susieti su kortele. Naudojant šią etiketę lengviau identifikuoti korteles, kai jos braukiamos periferinius simuliatoriumi. Naudodami virš kortelės vaizdo esančius kairiosios rodyklės (**&lt;**) ir dešiniosios rodyklės (**&gt;**) mygtukus galite pasirinkti naudojant periferinį simuliatorių sukonfigūruotas korteles. Galite redaguoti ir panaikinti korteles naudodami šalia pliuso ženklu (**+**) pažymėto mygtuko esančius mygtukus **Redaguoti** ir **Naikinti**.

### <a name="pin-pad"></a>PIN rinkiklis

Sukonfigūruodami PIN rinkiklio simuliatorių galite imituoti OEKA PIN rinkiklį. Kai elektrininio lėšų pervedimo (EFT) operacija atliekama naudojant EKA ir reikia įvesti PIN, aparatūros stotis pasiūlo PIN įrenginiui paraginti įvesti PIN. Norint, kad veiktų periferinio simuliatoriaus PIN rinkiklis, reikia, kad būtų palaikoma EFT mokėjimo jungtis.

### <a name="printer"></a>Spausdintuvas

Virtualus periferinis spausdintuvas tiesiog rodo EKA atspausdintus gavimo kvitus. Jeigu atliekant spausdinimo operaciją sukuriami keli gavimo kvitai, galite slinkti per gavimo kvitus.

#### <a name="configure-receipt-printing"></a>Kvitų spausdinimo konfigūravimas

1.  Eikite į **Mažmeninė prekyba ir prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA šablonai** &gt; **Aparatūros šablonai**.
2.  Pasirinkite virtualiems periferiniams įrenginiams sukurtą aparatūros šabloną.
3.  Dalies **Spausdintuvas** skirtuke „FastTab“ spustelėkite **Redaguoti**.
4.  Lauke **Kvito šablono ID** pasirinkite kvito šabloną.
5.  Spustelėkite **Įrašyti**.

### <a name="scale"></a>Mastelis

Kai į EKA operaciją įtraukiamas svarstyklių produktas ir sukonfigūruojamos svarstyklės, EKA gauna ant svarstyklių esantį svorį. Naudojant tiek virtualiąją, tiek faktinę skalę produktas arba svoris turi būti nurodomas prieš tai, kai produktas įtraukiamas į operaciją. Prieš įtraukdami svarstyklių produktą į operaciją, eikite į periferinio simuliatoriaus svarstykles ir naudodami pliuso ženklo (**+**) ir minuso ženklo (**–**) mygtukus pakoreguokite svorį, kurį turi pranešti svarstyklės. Taip pat galite įvesti norimą svorį tiesiai lauke **Dabartinė reikšmė**. Galite koreguoti svarstyklių svorio vienetus naudodami pliuso ženklą (**+**), mygtukus **Redaguoti** ir **Naikinti**. Tokiu būdu vienetus galima nurodyti pagal pasvertus produktus arba vietą, kurioje naudojamos svarstyklės.

#### <a name="configure-a-scale-product"></a>Svarstyklių produkto konfigūravimas

1.  Eikite į **Mažmeninė prekyba ir** **prekyba** &gt; **Produktai ir kategorijos** &gt; **Patvirtinti produktai pagal kategoriją**.
2.  Atidarykite produkto įrašą.
3.  Pasirinkite svertiną produktą.
4.  Dalies **Mažmeninė prekyba** skirtuke „FastTab“ pakeiskite dalies **Svarstyklių produktas** parinktį iš **Ne** į **Taip**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Pakeitimų sinchronizavimas su kanalų duomenų baze

1.  Eikite į **Mažmeninė prekyba ir komercija** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikas**.
2.  Pasirinkite **1040** paskirstymo grafiką.
3.  Spustelėję **Vykdyti dabar** sinchronizuokite EKA pakeitimus.

Susinchronizavus duomenis, kai svarstyklių produktas įtrauktas į EKA operaciją, EKA patikrina ant svarstyklių esantį svorį.

### <a name="signature-capture"></a>Parašo fiksavimas

Kai naudojamai mokėjimo priemonei reikalingas parašas, virtualus parašo fiksavimo įrenginys paragina vartotoją pateikti parašą naudojant virtualųjį parašo fiksavimo rinkiklį. Vartotojas gali patvirtinti parašą, kad jis būtų rodomas EKA. Tada kasininkas gali priimti parašą. Tada parašas įrašomas kartu su mokėjimo priemone ir kartu su kitais operacijų duomenimis sinchronizuojamas su tarnybiniu biuru.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Mokėjimo priemonės parašo reikalavimo parinkties nustatymas

1.  Eikite į **Mažmeninė prekyba ir prekyba** &gt; **Kanalai** &gt; **Mažmeninės prekybos parduotuvės** &gt; **Visos mažmeninės prekybos parduotuvės**.
2.  Pasirinkite mažmeninės prekybos parduotuvę.
3.  Spustelėkite **Redaguoti**.
4.  Spustelėkite **Nustatyti**, o po to skyriuje **Nustatyti** spustelėkite **Mokėjimo būdai**.
5.  Spustelėkite **Redaguoti**.
6.  Pasirinkti mokėjimo būdą, kuriuo naudojantis reikalingas parašas.
7.  Skyriaus **Bendrosios nuostatos** dalyje **Parašo fiksavimas** nustatykite parametro **Naudoti parašo fiksavimo įrenginį** parinktį **Taip**.
8.  Lauke **Minimali parašo fiksavimo suma** įveskite minimalią sumą, kuri turėtų sužadinti parašo fiksavimą.

#### <a name="synchronize-changes-to-the-channel-database"></a>Pakeitimų sinchronizavimas su kanalų duomenų baze

1.  Eikite į **Mažmeninė prekyba ir komercija** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikas**.
2.  Pasirinkite **1070** paskirstymo grafiką.
3.  Spustelėję **Vykdyti dabar** sinchronizuokite EKA pakeitimus.

Susinchronizavus duomenis, kai naudojama mokėjimo priemonė, kuriai reikalingas parašas, o suma neviršija parašo slenkstinės vertės sumos, EKA paragina pateikti parašą naudojant virtualųjį parašo fiksavimo įrenginį.

## <a name="additional-configuration"></a>Papildoma konfigūracija
Galite redaguoti periferinio simuliatoriaus konfigūracijos failą, kad jis būtų tiksliau nukreiptas į jūsų tikrinamus scenarijus. Konfigūracijos failą galite rasti adresu C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Konfigūracijos faile nurodomi vienetai, kuriuos galima naudoti atliekant bandymus ant svarstyklių, kortelių tipai, kuriuos galima tikrinti ir brūkšninių kodų tipai. Pavyzdžiui, keisdami konfigūracijos failo teksto vertes galite įtraukti naują kortelės tipą arba matavimo vienetą, kuriuos galima pasirinkti vykdant operacijas. Paleidus programą iš naujo bus rodomos naujos vertės.

## <a name="troubleshooting"></a>Trikčių šalinimas
Periferinio simuliatoriaus veiklos registruojamos naudojant periferinį simuliatorių. Žurnalą galite rasti adresu C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Periferinis simuliatorius taip pat praneša apie problemas „Windows“ įvykių žurnale, kurį galite pasiekti adresu **Programų ir paslaugų žurnalai** &gt; **„Microsoft“** &gt; **„DynamicsAX“**. Jeigu naudojant MPOS ar periferinį simuliatorių pakeitimai, kuriuos atlikote aparatūros šablonui arba kitose srityse nematomi, paskirstymo planuoklio užduotis, kurias naudojote sinchronizuodami duomenis kanalo duomenų bazėje. Jei pakeitimai buvo susinchronizuoti, bet vis dar nematomi naudojant EKA, iš naujo paleiskite EKA klientą. Sukonfigūruotiems grynųjų pinigų stalčiams atlikti pakeitimai neįsigalios, kol nebus sukurta nauja pamaina. Todėl, jeigu atliekate grynųjų pinigų stalčių pakeitimus, būtinai uždarykite esamą pamainą, kad patikrintumėte naują grynųjų pinigų stalčiaus sąranką. Kartais, jeigu iš „Monroe Consulting Services“ gamintojo tvarkyklė įdiegta vėliau negu bendrieji valdymo objektai, dėl tvarkyklės bendrieji valdymo objektai gali veikti netinkamai. Tokiu atveju turite iš naujo įdiegti bendruosius valdymo objektus.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Periferinių mažmeninės prekybos įrenginių apžvalga](retail-peripherals-overview.md)




