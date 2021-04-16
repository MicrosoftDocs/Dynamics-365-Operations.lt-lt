---
title: Tvirtinimas ir perkėlimas
description: Šioje temoje paaiškinama, kaip naudoti patvirtinimo ir perkėlimo funkciją, leidžiančią vartotojams išsiųsti iš sandėlio krovinius prieš baigiant visus su šiais kroviniais susijusius darbus.
author: mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate,WHSWorkTemplateTable,WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 2ab2d720f7f0425f0c2fd5d79d684a02b452e4d7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828423"
---
# <a name="confirm-and-transfer"></a>Tvirtinimas ir perkėlimas

[!include [banner](../includes/banner.md)]

*Patvirtinti ir perkelti* funkcija leidžia vartotojams išsiųsti krovinius iš sandėlio prieš baigiant visus darbus, susijusius su tais kroviniais. Kai siunta, kurioje yra krovinio eilutės, kurios nebuvo visiškai paimtos, gaunama, patvirtinantis vartotojas paraginamas arba išskaidyti likusius kiekius naujame krovinyje arba atšaukti nebaigtus kiekius.

Sistemos, kurios nustatytos taip, kad leistų išskaidyti palaikymo scenarijus, kai suplanuoti ir iš dalies pakrauti kroviniai turi būti pritaikyti dėl naujų arba besikeičiančių aplinkybių.

Kliento programa apima logiką, kuri leidžia iš dalies įkeltą krovinį uždaryti ir patvirtinti kaip išsiųstą. Visos likusios siuntos ir krovinio eilutės (įskaitant visas arba dalinių eilučių kiekius) perkeliamos į naujai sukurtą krovinį ir siuntą, jei šis perjungimas yra būtinas ir sąranka leidžia. Naujos siuntos ir kroviniai automatiškai sukuriami, atsižvelgiant į pradinį siuntos ir krovinio sukūrimą, o jų pagrindiniai atributai išlieka nepakeisti. Taip pat yra parinktis automatiškai atšaukti likusius kiekius, jei dar nesukurtas darbo užsakymas ir vartotojas mano, kad šis atšaukimas būtinas.

Ši funkcija palaiko scenarijus, kuriuose visas krovinys netelpa į vieną sunkvežimį, arba kai dalis krovinio turi būti išvežta iš sandėlio, kol likusi krovinio dalis bus paruošta išsiųsti. Šiuose scenarijuose likę produktai gali būti perkelti į naują krovinį, todėl pakrauti į naują sunkvežimį. Todėl, kad ši funkcija gali būti naudojama su kroviniais, kurie kitu atveju siunčiami pilnai pakrovus, ji suteikia papildomas galimybes, kad transporto vadybininkai galėtų spręsti nestandartinius arba nenumatytus scenarijus.

Kai krovinys suskaidytas *Patvirtinti ir perkelti* funkcija atlieka šiuos veiksmus:

- Nauji kroviniai ir siuntos sukuriamos atsiradus poreikiui. Kiekvienam kroviniui arba siuntai bus suteikti daugiausiai tie patys pirminio krovinio ar siuntos atributai. Išimtis yra krovinio būsena, kuri bus perskaičiuota pagal darbo būseną.
- Vartotojas informuojamas, kad sukurtas naujas krovinys. Vartotojas taip pat informuojamas apie naujo krovinio ID.
- Krovinio eilutės, darbo antraštės ir darbo eilutės, kurios buvo išskaidytos ir atnaujintos naujo krovinio ir siuntos informacija.
- Jei visa siunta yra išskaidyta, siunta tvarkoma ir atnaujinama, ir tik krovinio nuorodos atnaujinamos. Jei siuntą reikia išskaidyti, sukuriama nauja siunta.

Kai likę kiekiai atšaukiami, bet kokie krovinio eilutės kiekiai, kurie nebuvo paimti ir kurie neturi su jomis susijusio neatšaukto darbo yra pašalinami iš krovinio. Jei darbas dar yra vykdomas, vartotojas gali tik išskaidyti krovinį. Likusių kiekių atšaukti negalima.

Galite skaidyti tik tuos krovinius, kurie atitinka visus šiuos kriterijus:

- Viena ar daugiau krovinio eilučių pakėlė kiekius.
- Krovinio būsena yra „neįkeltas”.
- Nėra krovinio eilutės duomenų. (Šie duomenys sukuriami kuriant numerio lentelės konsolidaciją išdėstymo vietoje ir *Patvirtinti ir perkelti* funkcija nepalaiko numerio lentelės konsolidacijos.)
- Nėra laukiama atsargų, kurios turi būti supakuotos, pakavimo vietoje. (*Patvirtinti ir perkelti* funkcija nepalaiko atsargų, paimtų į paketo stotį, bet kurios dar nebuvo supakuotos.)

> [!NOTE]
> Ši funkcija skiriasi nuo transportavimo krovinio funkcijos, kuri turėtų būti naudojama sandėliuose, kurie niekuomet neplanuoja ir nekuria krovinių prieš paėmimą, bet vietoj to atlaisvina vietos transportavimui, kai paėmimas baigiamas.
>
> Naudokite *Patvirtinti ir perkelti* funkciją tokiose situacijose, kai kroviniai paprastai planuojami ir sukuriami iš anksto, tačiau kartais pasitaiko išimčių, kai krovinys netelpa į transporto priemonę (pvz., sunkvežimį).

## <a name="turn-on-confirm-and-transfer"></a>Įjungti patvirtinti ir perkelti

Prieš naudojantis *Patvirtinti ir perkelti* funkciją, įjunkite ją savo sistemoje. Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *sandėlio valdymas*
- **Funkcijos pavadinimas:** *Patvirtinti ir perkelti*

## <a name="set-up-confirm-and-transfer"></a>Nustatyti patvirtinti ir perkelti

Norėdami naudoti *Patvirtinti ir perkelti* funkciją, turite ją įjungti visuose susijusiuose krovinio šablonuose. Be to, atsižvelgdami į savo reikalavimus, galite tekti paruošti darbo šablonus, kad funkcija veiktų. Jei norite dirbti su pavyzdiniu scenarijumi, pateiktu šioje temoje, nustatykite sistemą, kaip aprašyta šiame skyriuje. (Šis scenarijus paremtas **USMF** parodomosios versijos duomenimis.)

### <a name="prepare-your-load-templates"></a>Paruoškite savo krovinio šablonus

1. Eikite į **Sandėlio valdymas \> Sąranka \> Krovinys \> Krovinio šablonai**.
1. Veiksmų srityje pasirinkite **Redaguoti**, kad pakeistumėte puslapio režimą į redagavimo.
1. Pažymėkite kiekvieno esamo šablono, kuriam norite įjungti funkciją, **Lesti išskaidyti krovinį siuntos patvirtinimo metu** žymės laukelį. Taip pat galite pasirinkti **Nauja**, kad sukurtumėte naują šabloną ir sukonfigūruotumėte jį pagal savo poreikius. Kiekvienam jūsų sukurtam kroviniui naudojant tą šabloną bus pritaikyta ši funkcija. (Jei dirbate su **USMF** parodomosios versijos duomenimis, įjunkite funkciją, skirtą **20' konteineris** krovinio šablonui.)

### <a name="prepare-your-work-templates"></a>Paruoškite savo darbo šablonus

Šis parametras nebūtinas visose situacijose. Čia rodomas pavyzdys užtikrina, kad darbas gali būti suskirstytas pagal siuntą, kad veiktų vėliau šioje temoje pateikiamas pavyzdys. Taip pat yra ir kitų būdų pasiekti šį rezultatą.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.
1. Viršutinėje puslapio dalyje esančiame tinklelyje pasirinkite esamą darbo šabloną, kuriame norite nustatyti *Patvirtinti ir perkelti* funkciją. (Jei dirbate su **USMF** parodomosios versijos duomenimis pasirinkite **51 paėmimo etapas** darbo šabloną.) Arba sukurkite naują darbo šabloną.
1. Veiksmų srityje pasirinkite **Redaguoti užklausą**, kad atidarytumėte **Pardavimai** dialogo langą.
1. **Pardavimai** dialogo lange **Rūšiavimas** skirtuke pasirinkite **Pridėti**, kad pridėtumėte eilutę tinklelyje.
1. Naujoje eilutėje nustatykite šias vertes:

    - **Lentelė:** *Laikinos darbo operacijos*
    - **Išvestinė lentelė:** *Laikinos darbo operacijos*
    - **Laukas:** *Siuntos ID*
    - **Ieškos kryptis:** *Didėjanti*

1. Pasirinkite **Gerai**, kad įrašytumėte parametrus ir uždarytumėte **Pardavimai** dialogo langą.
1. Jei gaunate pranešimą, kuriame teigiama, kad grupavimas bus nustatytas iš naujo, pasirinkite **Taip**, kad tęstumėte.
1. Tinklelyje, esančiame viršutinėje **Darbo šablonai** puslapio dalyje pasirinkite jūsų ką tik redaguotą šabloną ir tada Veiksmų srityje pasirinkite **Darbo antraštės lūžiai**.
1. Veiksmų srityje pasirinkite **Redaguoti**, kad pakeistumėte puslapio režimą į redagavimo.
1. Tinklelyje nustatykite šias vertes:

    - **Lentelės pavadinimas** *Laikinos darbo operacijos*
    - **Lauko pavadinimas:** *Siuntos ID*
    - **Grupuoti pagal šį lauką:** Pažymėkite šį žymės langelį.

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Uždarykite puslapį.

## <a name="scenario"></a>Scenarijus

Šiame scenarijuje parodytas pavyzdys, kai paėmimo procesas dar nebaigtas, bet iki šiol paimtos prekės turi būti vis tiek pakrautos į sunkvežimį ir išsiųstos. Todėl vartotojas gali išskaidyti nepaimto krovinio eilutes į naują krovinį. Bus automatiškai atnaujinti visi duomenų ryšiai.

> [!NOTE]
> Tam tikros vertės, aprašytos šiame scenarijuje, pagrįstos **USMF** parodomosios versijos duomenimis. Rekomenduojame naudoti šiuos parodomosios versijos duomenis, kol demonstruojate ar mokotės naudotis funkcija. Jei nenaudojate **USMF** parodomosios versijos duomenų, pagal poreikį pakeiskite juos savomis vertėmis.

### <a name="step-1-create-a-load-that-has-multiple-load-lines"></a>1-as veiksmas: sukurkite krovinį, turintį kelias krovinio eilutes

Prieš jums naudojantis šia funkcija, turite turėti krovinį, kuriame yra kelios krovinio eilutės. Taip pat turite įsitikinti, kad paėmimo vietose yra pakankamai visų prekių atsargų pardavimų užsakymams, kuriuos sukursite ateityje. Peržiūrėkite vietos nurodymo nustatymą ( **Sandėlio valdymas \>Sąranka \>Vietos nurodymai**) ir pasižymėkite paėmimo vietas, naudojamas pardavimo užsakymo paėmimui. Jei reikia koreguoti atsargas, kurti rankinius perkėlimus, pagal poreikį naudokite papildymą arba bet kokį kitą srautą.

Norėdami sukurti tinkamą krovinį, pirmiausia kurkite tris pardavimų užsakymus atlikdami šiuos veiksmus.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Veiksmų srityje pasirinkite **Nauja**, kad atidarytumėte dialogo langą **Sukurti pardavimų užsakymą**.
1. **Sukurti pardavimo užsakymą** dialogo lange nustatykite šias vertes (mažiausiai):

    - **Klientas** „FastTab” skirtuke nustatykite **Kliento paskyra** lauką į *US-004* (*Urvų didmeninė prekyba*).
    - „FastTab“ **Bendra** skirtuke nustatykite **Sandėlis** lauką į *51*.

1. Pasirinkite **Gerai** naujam pardavimo užsakymui sukurti ir uždarykite **Kurti pardavimo užsakymą** dialogo langą.
1. Jūsų naujas pirkimo užsakymas yra atidarytas. **Pardavimo užsakymo eilutės** tinklelį pridėkite eilutę, kurioje yra šios vertės:

    - **Prekės numeris:** *M9200*
    - **Kiekis:** *40*
    - **Vienetas:** *ea*

1. Virš tinklelio esančiame meniu **Atsargos** pasirinkite **Rezervavimas**.
1. Veiksmų srityje **Rezervacijos partija** pasirinkite atverti **Rezervacija** puslapį.
1. Rezervuokite atsargas pardavimo eilutėje ir tada užverskite **Rezervacija** puslapį.
1. Pakartokite 1–4 veiksmus, kad pridėtumėte antrą pardavimo užsakymą tam pačiam klientui ir sandėliui.
1. Pridėkite dvi pardavimų eilutes, turinčias šias vertes. Pridėjus kiekvieną eilutę, rezervuokite atsargas kaip aprašyta 6-8 veiksmuose.

    - **1-a eilutė:** nustatykite lauką **Prekės numeris** į *M9200*, lauką **Kiekis** į *30* ir lauką **Vienetas** į *už vnt*.
    - **2-a eilutė:** nustatykite lauką **Prekės numeris** į *M9201*, lauką **Kiekis** į *20* ir lauką **Vienetas** į *už vnt*.

1. Pakartokite 1–4 veiksmus, kad pridėtumėte trečią pardavimo užsakymą tam pačiam klientui ir sandėliui.
1. Pridėkite dvi pardavimų eilutes, turinčias šias vertes. Pridėjus kiekvieną eilutę, rezervuokite atsargas kaip aprašyta 6-8 veiksmuose.

    - **1-a eilutė:** nustatykite lauką **Prekės numeris** į *M9201*, lauką **Kiekis** į *20* ir lauką **Vienetas** į *už vnt*.
    - **2-a eilutė:** nustatykite lauką **Prekės numeris** į *M9202*, lauką **Kiekis** į *60* ir lauką **Vienetas** į *už vnt*.

#### <a name="load-planning-workbench"></a>Krovinio planavimo darbo sritis

Krovinio planavimo darbo sritis naudos krovinio šablono ID, kad būtų galima kurti siuntas ir išleisti pardavimo užsakymo eilutes į sandėlį.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Krovinio planavimo darbo sritis**.
1. Lauke **Sandėlis** pasirinkite *51*.

    Dabar sukursite ką tik jūsų sukurtiems pardavimų užsakymams krovinį.

1. **Pardavimų eilutės** skirtuke, tinklelyje, pasirinkite naujų pardavimo užsakymų pardavimo eilutes.
1. Veiksmų srities **Tiekti ir pareikalauti** skirtuke **Pridėti** grupėje pasirinkite **Į naują krovinį**.
1. Dialogo lange **Krovinio šablono priskyrimas** **Krovinio šablono ID** lauke pasirinkite *20' konteineris*.
1. Pasirinkite **Gerai**.
1. **Kroviniai** dalyje **Krovinio planavimo darbo sritis** puslapyje, tinklelyje, suraskite naujai sukurtą sandėlio *51* krovinio ID. Slinkite į dešinę, kol pamatysite **Leisti krovinio išskaidymą siuntos patvirtinimo metu** stulpelį. Jūsų kroviniui pažymėkite žymės langelį.
1. Pasirinkite krovinį.
1. **Išleisti** meniu virš tinklelio pasirinkite **Išleisti į sandėlį**, kad sukurtumėte darbą.
1. Dialogo lange **Išleisti krovinį į sandėlį** patvirtinkite, kad **Įrašai, kuriuos reikia įtraukti** „FastTab” rodo krovinio ID.
1. Pasirinkite **Gerai**.

    Galite gauti „Apdorojimo operacija” pranešimą, kai sistema sukuria siuntas ir darbą.

1. **Kroviniai** dalyje **Krovinio planavimo darbo sritis** puslapyje dabar jūsų krovinio būsena turi būti *Bangos*. Pasirinkite krovinį, tada virš tinklelio esančiame meniu **Susijusi informacija** pasirinkite **Bangos išsami informacija**, kad peržiūrėtumėte sukurtus siuntų ID. Baigę uždarykite **Bangos** puslapį.
1. **Kroviniai** dalyje **Krovinio planavimo darbo sritis** pasirinkite krovinį, tada **Susijusi informacija** virš tinklelio esančiame meniu pasirinkite **Darbo išsami informacija**, kad peržiūrėtumėte ką tik sukurtą pardavimų užsakymų darbą.
1. Pasižymėkite sukurtų darbo ID. Gali tekti slinkti į dešinę, kad pamatytumėte pardavimo užsakymo numerį ir siuntos ID, susietus su darbo ID.

### <a name="step-2-set-up-the-execution-flow-for-mobile-devices"></a>2-as veiksmas: nustatykite mobiliųjų įrenginių vykdymo eigą

Mobiliojo įrenginio užduotyse reikės įvesti vartotojo informaciją, pvz., darbo ID arba numerio lentelės ID. Laukuose ši informacija paprastai teikiama sandėlio vartotojams brūkšninių kodų forma, kurie randami dokumentuose, pakuotėse ar išdėstyme. Norėdami atlikti scenarijų mobiliesiems įrenginiams skirtus veiksmus, įsitikinkite, kad nustatėte operacijų darbo ID ir operacijų prekės bei vietos numerio lentelės ID.

1. Prisijunkite prie mobiliojo įrenginio naudodami sandėlio *51* vartotojo ID ir slaptažodį sandėlio vartotojo ID ir slaptažodį.
1. Pasirinkite **Siunčiama**.
1. Pasirinkite **Pardavimų paėmimas**.
1. Turite galimybę įvesti darbo ID arba numerio lentelės ID. Įveskite pirmo pardavimo užsakymo darbo ID ir pasirinkite **Įvesti**.
1. **Viet** lauke įveskite vietą, kuri rodoma norint patvirtinti paėmimo vietą. Tada pasirinkite **Įvesti**.
1. **LP** lauke įveskite numerio lentelės ID. Numerio lentelės ID turi sutapti su prekės, sandėlio ir prekės, paimtos iš pasirinktos vietos, vietos ID. Baigę pasirinkite **Įveskite**.
1. **Prekė** lauke įveskite prekės numerį, kad patvirtintumėte prekės paėmimą ir įveskite **Įvesti**.
1. **Kiek.** lauke įveskite prekės kiekį, kad patvirtintumėte prekės paėmimą ir įveskite **Įvesti**.
1. **Tikslinė LP** lauke įveskite tikslinį numerio lentelės ID. Tikslinės numerio lentelės yra apibrėžtos vartotojo. Būtinai įveskite numerio lentelės ID, kurį atsimintumėte. Rekomenduojame naudoti dabartinę datą ir dviejų skaitmenų seką (YYMMDD\#\#) kaip formatą, pvz., *19112301*. Baigę pasirinkite **Įveskite**.
1. Peržiūrėkite rodomą informaciją. Ši informacija yra *Paimti* informacija, kuri dabar taps *Padėti* duomenimis padėjimo operacijai. Baigę pasirinkite **Įveskite**.

    - Gaunate **Pabaigtas darbas** pranešimą.

1. Pakartokite veiksmus nuo 4 iki 10, skirtus antrojo pardavimo užsakymo darbo ID.

Kitas veiksmas yra įkelti dvi paimtas numerio lenteles į sunkvežimį.

1. Prisijunkite prie mobiliojo įrenginio naudodami sandėlio *51* vartotojo ID ir slaptažodį sandėlio vartotojo ID ir slaptažodį.
1. Pasirinkite **Siunčiama**.
1. Pasirinkite **Pardavimų įkėlimas**.
1. Įveskite vartotojo nustatytą tikslinės numerio lentelės ID, kurį sukūrėte pirmam darbo ID ankstesniame procese. Tada pasirinkite **Įveskite**, kad tikslinės numerio lentelė būtų įvesta **ETAPAS** vietoje.
1. Dar kartą įveskite tikslinės numerio lentelės ID ir pasirinkite **Įvesti**, kad numerio lentelė būtų įvesta **ĮLANKOSDURYS** vietą.
1. Pakartokite 4–5 veiksmus, skirtus tikslinės numerio lentelės ID, kurį sukūrėte antrajam darbo ID.

Dabar du darbo ID bus uždaryti (įkelti).

### <a name="step-3-confirm-the-outbound-shipment"></a>3-ias veiksmas: patvirtinkite siunčiamą siuntą

Atlikdami šį veiksmą, patvirtinsite du pardavimo užsakymus ir pabaigtą krovinio darbą, kad būtų išsiųstos krovinio paimtos prekės sukurtas naujas nepaimtų prekių krovinis. Siunčiamos siuntos patvirtinimas turi būti atliktas **Įkelti išsamią informaciją** puslapyje.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Krovinio planavimo darbo sritis**.
1. **Kroviniai** dalyje, tinklelyje, pasirinkite savo sukurto krovinio ID eilutę.
1. Pasirinkite krovinio ID saitą, kad atidarytumėte **Krovinio išsami informacija** puslapį.
1. **Krovinio išsami informacija** puslapyje, esančiame Veiksmų srityje, **Išsiųsti ir gauti** skirtuke, **Patvirtinti** grupėje, pasirinkite **Siunčiama siunta**, kad būtų pradėtas patvirtinimas.
1. Dialogo lange **Siuntos patvirtinimas**, esančiame **Krovinio išskaidymo būdas siuntos patvirtinimo metu** lauke, pasirinkite *Išskaidyti kiekį naujame krovinyje*.
1. Pasirinkite **Gerai**.

    Galite gauti „Vykdymo operacija” pranešimą.

    Gaunate informacinius pranešimus, nurodančius, kad jūsų krovinio siunta buvo patvirtinta ir kad iš suskaidyto kiekio buvo sukurtas naujas krovinys.

Atnaujinkite **Krovinio planavimo darbo sritis** puslapį, kad pamatytumėte naujai sukurtą krovinį.

Taip pat galite patvirtinti, kad operacijų ryšiai atnaujinti šiais būdais:

- Likusios (neapdorotos) siuntos ir siuntos eilutės atnaujinamos naujais krovinio ID.
- Pardavimo užsakymas susietas su nauju ID.
- Pradiniame krovinyje nėra likusių krovinio eilučių.
- Likęs darbas atnaujintas nauju krovinio ID.
- Banga išlieka ta pati.
- Naujo krovinio būsena tinkamai atnaujinta. (Jei darbo būsena yra _Vykdoma_, krovinio būsena taip pat turi būti _Vykdoma_.)

## <a name="notes-and-tips"></a>Pastabos ir patarimai

- Taip pat galite įjungti **Leisti krovinio išskaidymą siuntos patvirtinimo metu** parametrą po krovinio sukūrimo, tuo tarpu kai **Krovinio šablonas** parametras yra išjungtas, bet prieš pradedant pakrovimą. Pereikite į pageidaujamą krovinį, tada antraštės rodinyje įjunkite parametrą.
- **Išskaidytas kiekis į naują krovinį** pasirinktis taip pat veikia, kai kai kurių likusių darbo antraščių būsena yra *vykdoma*. Todėl vis dar galite naudoti funkcijas, net jei darbuotojai jau vykdo paėmimo užsakymus.
- Jei pasirinksite **Atšaukti neįvykdytą kiekį**, kai yra likęs darbas, kurio būsena yra *Atviras* arba *Vykdomas*, gaunate tokį klaidos pranešimą: „Nepavyko atšaukti likusio krovinio kiekio. Yra krovinio darbas.“
- Jei pasirinksite **Atšaukti neįvykdytą kiekį**, kai nėra likusio darbo, bet yra neišleistų krovinio eilučių kroviniui, gausite tokį klaidos pranešimą: „Krovinio siuntos nepavyksta patvirtinti, nes prekės kiekis viršija procentinę dalį, kuri nurodyta pristatymo metu.“ Norėdami išvengti šios klaidos, galite nustatyti, kad **Pristatymo metu** neišleistos krovinio eilutės procentus į 100 procentų. Neišleistos eilutės nebus perkeltos į naują krovinį, bet dabartinis krovinys bus patvirtintas kaip pristatymo trūkumas. Tokiu atveju negalėsite iš naujo paleisti pradinio užsakymo. Todėl jums reikės kitaip išspręsti šią problemą.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]