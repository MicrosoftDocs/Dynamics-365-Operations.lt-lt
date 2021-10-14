---
title: Suplanuotas prekių skirstymas
description: Šioje temoje aprašoma Išplėstinis suplanuoto prekių skirstymas, kai atsargų kiekis, reikalingas užsakymui yra nukreipiamas tiesiai iš gavimo arba sukuriama į teisinga pakrovimo rampa arba išdėstymo sritis. Visos likusios atsargos iš gavimo šaltinių yra nukreipiamos į teisingą saugojimo vietą naudojant įprastą padėjimo procesą.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: c28639a4a575f5f356bf947ba8e0aee6bcd256b4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573038"
---
# <a name="planned-cross-docking"></a>Suplanuotas prekių skirstymas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas išplėstini suplanuotas prekių skirstymą. Išplėstinis suplanuoto prekių skirstymas yra sandėlio procesas, kai atsargų kiekis, reikalingas užsakymui yra nukreipiamas tiesiai iš gavimo arba sukuriama į teisinga pakrovimo rampa arba išdėstymo sritis. Visos likusios atsargos iš gavimo šaltinių yra nukreipiamos į teisingą saugojimo vietą naudojant įprastą padėjimo procesą.

Suplanuoto prekių skirstymo darbuotojai gali praleisti gaunamų atsargų padėjimus ir siunčiamų prekių paėmimus, jau pažymėti siunčiamam užsakymui. Todėl atsargų paėmimo kartai yra sumažinti, jei įmanoma. Taip pat dėl mažesnės sąveikos su sistema, laiko ir vietos taupymas sandėlio darbo aukšte yra padidinami.

Norėdami vykdyti prekių skirstymą, turite sukonfigūruoti naują prekių skirstymo šabloną, kuriame nurodytas tiekimo šaltinis ir kiti prekių skirstymo reikalavimų rinkiniai. Kadangi siuntimo užsakymas sukuriamas, eilutė turi būti pažymėta pagal gavimo užsakymą, kuriame yra ta prekė. Nurodymo kodą galite pasirinkti prekių skirstymo šablone, panašiai kaip nustatote papildymo ir pirkimo užsakymus.

Gaunamo užsakymo gavimo metu, prekių skirstymo nustatymas automatiškai identifikuoja prekių skirstymo poreikius ir sukuria reikiamo kiekio perkėlimo darbą, pagrįstą vietos nurodymo nustatymu.

> [!NOTE]
> Atsargų operacijos yra *ne* registruojamos atšaukus prekių skirstymo darbą, net jei šios galimybės nustatymas yra įjungtas sandėlio valdymo parametruose.

## <a name="turn-on-the-planned-cross-docking-features"></a>Įjungti suplanuoto prekių skirstymo funkcijas

Jei jūsų sistemoje dar nėra funkcijų, aprašytų šioje temoje, eikite į [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ir toliau pateikiama tvarka įjunkite šias funkcijas:

1. *Suplanuotas prekių skirstymas*
1. *Prekių skirstymo šablonai su vietovės nurodymais*
    > [!NOTE]
    > Ši funkcija įgalina prekių skirstymo šablone nurodyti lauką **Nurodymo kodas**, panašiai kaip nustatote papildymo šablonus. Šios funkcijos įgalinimas neleidžia jums įtraukti nurodymo kodo į prekių skirstymo šablono eilutes, paskutinei *Įdėti* eilutei. Taip užtikrinama, kad prieš atsižvelgiant į darbo šablonus, galutinė įdėjimo vieta gali būti nustatyta darbo kūrimo metu.

## <a name="setup"></a>Sąranka

### <a name="regenerate-load-posting-methods"></a>Pakartotinai generuoti krovinio registravimo metodus

Suplanuotas prekių skirstymas yra įgyvendinamas kaip krovinio registravimo metodas. Įjungę funkciją, turite pakartotinai generuoti metodus.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Krovinio registravimo metodai**.
1. Veiksmų srityje spustelėkite **Pakartotinai generuoti metodus**.

    Baigus pakartotinį generavimą , turėtumėte matyti metodą, kurio **Metodo pavadinimas** yra *Planuoti prekių skirstymą*.

1. Uždarykite puslapį.

### <a name="create-a-cross-docking-template"></a>Sukurkite prekių skirstymo šabloną

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Darbas \> Prekių skirstymo šablonai**.
1. Veiksmų srityje pasirinkite **Nauja** šablonui sukurti.
1. Antraštėje nustatykite šias vertes:

    - **Seka:** *1*

        Šis laukas nurodo tvarką, kuria yra vertinami šablonai.

    - **Prekių skirstymo šablono ID:** *51*
    - **Aprašas:** *Sandėlis 51*
    - **Paklausos išleidimo strategija:** *Prieš tiekimo kvitą*
    - **Sandėlis:** *51*

1. „FastTab“ nustatymas **Planavimas** kontroliuoja, kaip veikia šablonas. Nustatykite toliau nurodytas reikšmes.

    - **Paklausos reikalavimai:** *Nėra*

        Šiame lauke apibrėžiami atsargų paklausos reikalavimai. Jei paklausa turi būti susieta su tiekimu prieš išleidimą, pasirinkite *Žymėjimas*. Jei paklausa turi būti užsakymas, rezervuotas pagal tiekimą prieš išleidžiant, pasirinkite *Užsakymo rezervavimas*.

    - **Vietos tipas:** *Siuntimo vietos*

        Šiame lauke nurodoma, ar prekių skirstymas turi naudoti surinkimo/krovinio vietas iš siuntimo, ar reikia naudoti vietos nurodymus, kad būtų galima rasti surinkimo/krovinio vietas.

    - **Darbo šablonas** – Palikite šį lauką tuščią.

        Šiame lauke apibrėžiamas darbo šablonas, kurį reikia naudoti, kai sukuriamas prekių skirstymo darbas.

    - **Iš naujo patikrinti tiekimo kvitą:** *Ne*

        Ši pasirinktis nurodo, ar turi būti iš naujo patikrinta pasiūla gavimo metu. Jei ši pasirinktis nustatyta kaip *Taip,* tikrinamas ir maksimalus laiko langą, ir galiojimo dienų intervalas.

    - **Nurodymo kodas:** Palikite šį lauką tuščią

        Šią parinktį įgalina funkcija *Prekių skirstymo šablonai su vietos nurodymais*. Sistema naudoja vietos nurodymus, kad padėtų nustatyti geriausią vietą, į kurią bus perkeliamos prekių skirstymo atsargos. Galite ją nustatyti, priskirdami nurodymo kodą kiekvienam susijusiam prekių skirstymo šablonui. Jei nurodymo kodas yra nustatytas, sistema ieškos vietos nurodymų pagal nurodymo kodą, kai darbas bus sugeneruotas. Tokiu būdu galite apriboti vietos nurodymus, naudojamus konkrečiam prekių skirstymo šablonui.

    - **Patikrinti laiko langą:** *Taip*

        Ši pasirinktis nurodo, ar maksimalaus laiko langas turi būti įvertintas, kai pasirinktas tiekimo šaltinis. Jei ši pasirinktis nustatyta kaip *Taip*, laukai, susiję su maksimalaus ir minimalaus laiko langais, bus prieinami.

    - **Maksimalus laiko langais:** *5*

        Šis laukas apibrėžia maksimalų leidžiamą laikotarpį tarp tiekiamų prekių atvykimo ir reikiamų prekių išvykimo.

    - **Maksimalaus laiko lango vienetas:** *Dienos*
    - **Minimalus laiko langas:** *0*

        Šis laukas apibrėžia minimalų leidžiamą laikotarpį tarp tiekiamų prekių atvykimo ir reikiamų prekių išvykimo.

    - **Minimalaus laiko lango vienetas:** *Dienos*
    - **Galiojimo dienų diapazonas:** *0*

        *„Pirmas baigia galioti, pirmas išeina“ (FEFO) kriterijus:* Šis laukas apibrėžia maksimalų galiojimo datos pirmojo termino pabaigos skaičių tarp paketo, kuris yra sandėlyje ir šiuo metu gaunamo paketo.

1. „FastTab“ skirtuke **Tiekimo šaltiniai** turite nurodyti tiekimo tipus, kurie galioja šiam šablonui. Pasirinkite **Nauja** ir tada nustatykite šias reikšmes:

    - **SEekos numeris:** *1*
    - **Tiekimo šaltinis:** *Pirkimo užsakymas*

> [!NOTE]
> Galite nustatyti užklausą, norėdami kontroliuoti, kada konkretus prekių skirstymo šablonas naudojamas. Prekių skirstymo šablonų užklausa turi tik *InventTable* (prekių) lentelę ir vidinę sujungtą *WHSInventTable* (WHS prekių) lentelę. Jei į užklausą norite įtraukti kitas lenteles, galite jas sujungti tik naudodami *esamos jungtys* arba *nesamos jungtys*. Kai filtruojate sujungtas lenteles, kiekvienam prijungtos lentelės įrašui nuskaitomas kiekvienos prijungtos lentelės įrašas. Jei yra sujungimo tipas yra *esamos jungtys*, ieška baigiasi po to, kai buvo rastas pirmas sugretinimas. Pavyzdžiui, jei prijungiate pardavimo užsakymo eilučių lentelę prie prekių lentelės, sistema patikrina ir grąžina prekes, kurių bent viena pardavimo užsakymo eilutė turi nustatytą sąlygą. Iš esmės, duomenys surenkami iš pirminės (prekių) lentelės, o ne iš antrinės (pardavimo užsakymo eilutės) lentelės. Todėl šiame langelyje negalima filtruoti pagal šaltinio dokumentus, pvz., pardavimo užsakymo eilutes arba klientus.

### <a name="create-a-work-class"></a>Darbo klasės kūrimas

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Darbas \> Darbo klasės**.
1. Veiksmų srityje pasirinkite **Nauja** darbo klasės krovinio grupės sukūrimui.
1. Nustatykite toliau nurodytas reikšmes.

    - **Darbo klasės ID:** *Prekių skirstymas*
    - **Aprašas:** *Prekių skirstymas*
    - **Darbo užsakymo tipas** *Prekių skirstymas*

### <a name="create-a-work-template"></a>Darbo šablono kūrimas

1. Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.
1. Lauką **Darbo užsakymo tipas** nustatykite į *Prekių skirstymas*.
1. Veiksmų srityje pasirinkite **Nauja,** kad pridėtumėte eilutę į **Peržiūros** skirtuką.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Sekos numeris:** *1*
    - **Darbo šablonas** *51 Prekių skirstymas*
    - **Darbo šablono aprašas** *51 Prekių skirstymas*

1. Pasirinkite **Įrašyti,** kad būtų galima naudoti **Darbo šablono išsami informacija** „FastTab“ skirtuką.
1. „FastTab” skirtuke **Išsami darbo šablono informacija** pasirinkite **Nauja** norėdami sukurti naują tinklelio eilutę.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Darbo tipas:** *Paėmimas*
    - **Darbo klasės ID:** *Prekių skirstymas*

1. Pasirinkite **Nauja** kitai eilutei įtraukti ir nustatykite šias reikšmes:

    - **Darbo tipas:** *Padėjimas*
    - **Darbo klasės ID:** *Prekių skirstymas*

1. Pasirinkite **Įrašyti** ir patvirtinkite, kad pasirinktas žymės langelis **Galiojantis** žymės langelis *51 prekių skirstymo* šablonui.
1. Pasirinktinai: pasirinkite **Redaguoti užklausą**, jei norite nustatyti kriterijus, pagal kuriuos būtų kontroliuojama, kada ir kur naudojamas darbo šablonas.

    Galite nustatyti užklausą, norėdami kontroliuoti, kada konkretus darbo šablonas naudojamas. Pavyzdžiui, galite nurodyti, kad šablonas gali būti naudojamas tik tam tikroje vietoje. Jei norite, kad prekių skirstymo darbo šablonas būtų taikomas tam tikroje vietoje, turite filtruoti **Pradžios vieta** laukelį , o ne **Vieta** laukelį, nes gaunamų užklausų proceso darbo kūrimas (pirkimas, prekių skirstymas ir papildymas) pradedamas nuo padėjimo eilutės. Kai sukuriamas darbas, vietos įvertinimas nustato **Vietos** laukelį kaip padėjimo vietą. Tačiau paėmimo vieta saugoma **Pradžios vietos** laukelyje.

> [!NOTE]
> Darbo klasės ir darbų tipų *Paėmimas* ir *Padėjimas* ID turi sutapti.

### <a name="create-location-directives"></a>Vietos nurodymo kūrimas

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.
1. Kairinės srities lauką **Darbo užsakymo tipas** nustatykite į *Prekių skirstymas*.
1. Veiksmų srityje pasirinkite **Nauja** ir tada nustatykite šias reikšmes:

    - **SEekos numeris:** *1*
    - **Pavadinimas:** *51 prekių skirstymas*
    - **Darbo tipas:** *Padėjimas*
    - **Vieta:** *5*
    - **Sandėlis:** *51*

1. Pasirinkite **Įrašyti,** kad būtų galima naudoti **Eilutės** „FastTab“ skirtuką.
1. „FastTab“ skirtuke **Eilutės** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Pradinis kiekis:** *1*
    - **Galutinis kiekis:** *1000000*

1. Pasirinkite **Įrašyti,** kad būtų galima naudoti **Vietos nurodymų veiksmų** „FastTab“ skirtuką.
1. „FastTab“ skirtuke **Vietos nurodymo veiksmai** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Pavadinimas:** *Baydoor*
    - **Fiksuotos vietos naudojimas:** *Fiksuotos ir nefiksuotos vietos*

1. Pasirinkite **Įrašyti,** jei norite, kad atsirastų **Redaguoti užklausą** mygtukas **Vietos nurodymo veiksmų** įrankių juostoje.
1. Norėdami atidaryti užklausų rengyklę, pasirinkite **Redaguoti užklausą**.
1. Skirtuke **Diapazonas** įsitikinkite, kad sukonfigūruotos šios dvi eilutės:

    - Eilutė 1:

        - **Lentelė:** *Vietos*
        - **Išvestinė lentelė:** *Vietos*
        - **Laukas:** *Sandėlis*
        - **Kriterijai:** *51*

    - Eilutė 2:

        - **Lentelė:** *Vietos*
        - **Išvestinė lentelė:** *Vietos*
        - **Laukas:** *Vieta*
        - **Kriterijai:** *Baydoor*

1. Pasirinkite **Gerai** ir uždarykite užklausos rengyklę.

### <a name="create-a-mobile-device-menu-item"></a>Mobiliojo įrenginio meniu elemento kūrimas

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Kairiojoje srityje esančiame meniu elementų sąraše pasirinkite **Pirkimo padėjimas**.
1. Pasirinkite **Redaguoti**.
1. „FastTab“ skirtuke **Darbo klasės** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Darbo klasės ID:** *Prekių skirstymas*
    - **Darbo užsakymo tipas** *Prekių skirstymas*

1. Pasirinkite **Įrašyti**.

## <a name="scenario"></a>Scenarijus

### <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas

Norėdami sukurti pirkimo užsakymą kaip tiekimo šaltinį, atlikite šiuos veiksmus.

1. Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Dialogo lange **Sukurti pirkimo užsakymą** nustatykite šias vertes:

    - **Tiekėjo paskyra:** *104*
    - **Sandėlis:** *51*

1. Pasirinkite **Gerai** ir pasižymėkite užsakymo numerį.
1. Nauja eilutė pridedama į „FastTab” skirtuką **Pirkimo užsakymo eilutės**. Šioje eilutėje nustatykite šias reikšmes:

    - **Prekės numeris:** *A0001*
    - **Kiekis:** *5*

### <a name="create-a-sales-order"></a>Kurti pardavimo užsakymą

Norėdami sukurti pardavimo užsakymą kaip paklausos tiekimo šaltinį, atlikite šiuos veiksmus.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - **Kliento sąskaita:** *US-002*
    - **Sandėlis:** *51*

1. Pasirinkite **Gerai**.
1. Nauja eilutė pridedama į „FastTab” skirtuką **Pardavimo užsakymo eilutės**. Šioje eilutėje nustatykite šias reikšmes:

    - **Prekės numeris:** *A0001*
    - **Kiekis:** *3*

### <a name="create-planned-cross-docking"></a>Suplanuoto prekių skirstymo sukūrimas

Atlikite šiuos veiksmus, norėdami sukurti suplanuotą prekių skirstymo iš pardavimo užsakymo.

1. Puslapyje **Pardavimo užsakymo išsami informacija** Jūsų sukurtam pardavimo užsakymui veiksmų srities **Sandėlio** skirtuko grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.

    Išleidimo į sandėlio veiksmas sukuria pardavimo užsakymo siuntos ir krovinio eilutę pardavimo užsakymas ir bando paskirstyti atsargas.
    
    Jūs gausite informacinį pranešimą. Taip pat gausite tokį įspėjamąjį pranešimą: „Bangai XXXX nebuvo sukurtas joks darbas“. Dėl išsamesnės informacijos žr. darbo kūrimo retrospektyvos žurnale.“ Taip nutinka, nes sandėlyje nėra atsargų.

1. „FastTab“ skirtuke **Pardavimo užsakymo eilutės** meniu **Sandėlis** pasirinkite **Išsami siuntimo informacija**.

    Pasirodys puslapis **Išsami siuntimo informacija** ir parodys pardavimo užsakymui sukurtą darbą.

1. „FastTab“ skirtuke **Krovinio eilutės** atkreipkite dėmesį, kad **Suplanuoto prekių skirstymo kiekio** laukas nustatytas kaip *3*. Kadangi sandėlyje nėra pasiekiamų atsargų, bet tinkamas tiekimo šaltinis bus gautas per laiko langą, nurodytą prekių skirstymo šablone, kuriame buvo sukurtas prekių skirstymo kiekis.
1. „FastTab“ skirtuke **Krovinio eilutės** pasirinkite **Suplanuotas prekių skirstymas** peržiūrėti išsamią sukurto prekių skirstymo informaciją.

## <a name="process-the-cross-docking"></a>Prekių skirstymo apdorojimas

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a>Pirkimo užsakymas „Warehousing“ programėlėje

Sistema gaus 5 kiekį iš pirkimo užsakymo į gavimo vietą ir sukurs du darbo vienetus.

Pirmoji sukurta darbo ID yra **Darbo užsakymo tipo** *Prekių skirstymo* reikšmė, susieta su pardavimo užsakymu. Ji turi 3 kiekį ir yra nukreipta į galutinę siuntimo vietą, kad ją būtų galima išsiųsti nedelsiant.

Antroji sukurta darbo ID yra **Darbo užsakymo tipo** *Pirkimo užsakymas* reikšmė, susieta su pirkimo užsakymu. Jos likęs kiekis yra 2, jis nebuvo perkrautas ir nukreiptas į padėjimo į saugyklą.

1. Prisijunkite kaip mobiliojo įrenginio vartotojas sandėlyje *51*.
1. Eikite į **Gavimas \> Pirkimo gavimą**.
1. Lauke **PU numeris** įveskite savo pirkimo užsakymo numerį.
1. Lauke **Kiekis** įveskite *5*.
1. Pasirinkite **Gerai**.
1. Kitame puslapyje nustatykite lauką **Prekė** į *A0001*.
1. Pasirinkite **Gerai**.
1. Kitame puslapyje patvirtinkite **PU numerio**, **Prekės** ir **Kiekio** reikšmes pasirinkdami **Gerai**.

    Gaunate Pabaigtas darbas pranešimą.

1. Pasirinkti **Atšaukti** norėdami atsijungti.

### <a name="put-away-to-cross-docking-and-bulk"></a>Atsargų padėjimas prekių skirstyme ir krovinyje

Šiuo metu abejos darbo ID turi vienodas tikslines numerio lentelės. Norėdami atlikti kitus veiksmus, turite gauti darbo ID ir tikslinės numerio lentelės ID. Tai galite sužinoti iš išsamios pirkimo ir pardavimo užsakymų eilučių darbo informacijos. Taip pat galite pereiti prie **Sandėlio valdymas \> Darbas \> Išsami darbo informacija** ir filtruoti darbą, kurio **Sandėlio** reikšmė yra *51*.

1. Mobiliajame įrenginyje eikite į **Gavimas \> Pirkimo padėjimas** ir įveskite tikslinę darbo numerio lentelę.
1. Lauke **ID** įveskite tikslinės numerio lentelės ID iš darbo informacijos.

    Prekių skirstymo paėmimo puslapyje pateikiama paėmimo vieta (*RECV*), tikslinė numerio lentelė (*numerio lentelė*), prekė (*A0001*) ir kiekis (*3*).

1. Pasirinkite **Gerai**.
1. Lauke **Tikslinė LP** įveskite tikslinės numerio lentelės ID, kuri turi būti įtraukta (perskirstyta) į siuntimo vietą. Galite pasirinkti bet kurį savo pasirinktą numerio lentelės ID.
1. Pasirinkite **Gerai**.
1. Kito puslapio lauke **ID** įveskite tikslinės numerio lentelės ID.
1. Pasirinkite **Gerai**.
1. Patvirtinkite paėmimo darbą, kad būtų galima paimti likusį 2 kiekį ir pasirinkite **Gerai**.
1. Kitame puslapyje pasirinkite **Atlikta** užbaigti paėmimo procesą ir pradėti padėjimo procesą.

    Mobiliųjų įrenginių programėlė pateikia Jums vietą ir numerio lentelę, į kurias galima įtraukti prekę.

1. Patvirtinkite krovinio **Padėjimo** saugyklą pasirinkdami **Gerai**.
1. Kitame puslapyje patvirtinkite prekių skirstymo **Padėjimą** pasirinkdami **Gerai**.

    Gaunate Pabaigtas darbas pranešimą.

1. Pasirinkti **Atšaukti** norėdami atsijungti.

Toliau pateiktoje iliustracijoje rodoma, kaip atliktas prekių skirstymas gali atrodyti „Microsoft Dynamics 365 Supply Chain Management“.

![Atliktas prekių skirstymas.](media/PlannedCrossDockingWork.png "Atliktas prekių skirstymas")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
