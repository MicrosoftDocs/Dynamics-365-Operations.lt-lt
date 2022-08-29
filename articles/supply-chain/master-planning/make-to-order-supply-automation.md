---
title: Tiekimo automatizavimas pagal užsakymą
description: Šiame straipsnyje aprašoma, kaip nustatyti ir naudoti įvairius patobulinimus, kuriuos pridėjo gamybos pagal užsakymą tiekimo automatizavimo funkcija.
author: t-benebo
ms.date: 07/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-27
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9044acb472548a797ed387b08ca6892459785793
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220760"
---
# <a name="make-to-order-supply-automation"></a>Tiekimo automatizavimas pagal užsakymą

[!include [banner](../includes/banner.md)]

Gamybos *pagal užsakymą tiekimo automatizavimo funkcija "* Microsoft" prideda keletą patobulinimų Dynamics 365 Supply Chain Management. Šie patobulinimai įgalina atlikti šias užduotis:

- Peržiūrėkite išteklių pajėgumą vartotojo nustatytam laikotarpiui ir įgalinkite ilgalaikį pajėgumo įvertinimą.
- Pagerinti lankstumo, kontroliuojant kiekvieno bendrojo plano leistiną uždelsimo nuokrypį (neigiamas dienas).
- Išlaikyti produktus paskutinėms minutėms užsakymams ir optimizuoti esamo tiekimo naudojimą, iškvietimu iki vėliausio įmanomo tiekimo į poreikį, užuot naudojus pirmąjį galimą tiekimą.
- Patvirtavus komponento priskyrimą gamybos užsakymams išlaikyti kintamą, kad sistema galėtų optimizuoti paskutiniųjų minučių poreikio pokyčius. Kitaip tariant, ribokite žymėjimą vienu lygiu.
- Valdyti kiekvieno pardavimo užsakymo vykdymo strategiją. Numatytieji parametrai imami iš kliento nustatymo.
- Pagerinti vidinės įmonės informacijos srautą. Pirkimo užsakymai atnaujinami taip, kad juose būtų pristatymo būdo, pristatymo sąlygų ir išorinio prekės numerio laukai. Šis pakeitimas užtikrina, kad išsami poreikio informacija gali būti pateis į tiekimo įmonę.

Šiame straipsnyje aprašoma, kaip nustatyti ir naudoti kiekvieną patobulinimą.

> [!NOTE]
> Visi šiame straipsnyje aprašyti patobulinimai taikomi sistemoms, kurios naudoja integruotą bendrąjį planavimą. Planavimo optimizavimo papildinys, skirtas "Microsoft", taip pat palaiko šiuos du patobulinimus Dynamics 365 Supply Chain Management:
>
> - Atidėti bendrojo planų nuokrypio nuokrypį
> - Per bendrąjį planavimą naudojamos iškvietimo sekos valdymas

## <a name="turn-on-the-make-to-order-supply-automation-feature"></a>Įjungti gamybos pagal užsakymą tiekimo automatizavimo funkciją

Kad būtų galima naudoti šiame straipsnyje apibūdintą funkciją, turite įjungti ją savo sistemai. Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, kurioje priemonė pateikta tokiu būdu:

- **Modulis:** *bendrasis planavimas*
- **Funkcijos pavadinimas:** *gamybos pagal užsakymą tiekimo automatizavimas*

## <a name="set-the-number-of-days-to-show-on-capacity-load-page"></a>Nustatyti dienų, kurios bus rodomas pajėgumo apkrovos puslapyje, skaičių

Pajėgumo **puslapis** leidžia peržiūrėti išteklių galimų pajėgumų. Gamybos *pagal užsakymą tiekimo automatizavimo funkcija* pagerina pajėgumo **įkėlimo** puslapį, įtraukdama **dienų skaičių lauką**. Šį lauką galite naudoti norėdami apriboti dienų skaičių, kurį rodo **Peržiūros** tinklelis. Jūsų nustatyta vertė įrašoma į atmintį. Todėl jei paliksite puslapį ir grįšite vėliau, **Peržiūros** tinklelyje bus rodomas paskutinis nurodytas dienų skaičius.

Norėdami atidaryti puslapį **Pajėgumas**, kad būtų galima peržiūrėti turimus atskirų išteklių pajėgumus, atlikite šiuos veiksmus.

1. Eikite į **organizacijos administravimo \> išteklių \>**.
1. Pasirinkite išteklius, kurie bus tikrinami.
1. Veiksmų srities skirtuke Ištekliai **, grupėje** Rodinys **, pasirinkite** Pajėgumas **·**.
1. Norėdami apriboti **dienų skaičių,** kurį rodo Peržiūros tinklelis, naudokite dienų **skaičių**.

Norėdami atidaryti puslapį **Pajėgumas**, kad būtų galima peržiūrėti galimų išteklių grupės pajėgumą, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimas \> Resursai \> Resursų grupės**.
1. Pasirinkite išteklių grupę, kuri bus tikrinama.
1. Veiksmų srities skirtuko Išteklių grupė grupėje Rodinys pasirinkite **Pajėgumas** **·**.**·**
1. Norėdami apriboti **dienų skaičių,** kurį rodo Peržiūros tinklelis, naudokite dienų **skaičių**.

## <a name="apply-a-single-level-of-marking-when-you-firm-planned-orders"></a>Taikyti vieną žymėjimo lygį, kai galutinai planuojami užsakymai

*Ženklinimas* naudojamas susieti paklausą ir pasiūlą. Jis atspindi *fiksavimą*, kuris nurodo, kaip pagrindinis planavimas tikisi padengti paklausą. Tačiau žymėjimas yra nuolatinis, nei iškvietimas. Gamybos *pagal užsakymą tiekimo automatizavimo* funkcija suteikia galimybę apriboti atsargų žymėjimą iki vieno lygio, kai patvirtinti suplanuoti užsakymai. Kai tvirtinsite suplanuotą **užsakymą, dialogo** lange **Patvirtinti** įtrauksite šias naujas pasirinktis į lauką Atnaujinti žymėjimą:

- *Vieno lygio standartas* – naudojamas vieno lygio žymėjimas. Vieno lygio žymėjimas žymi tik pagrindinę prekę, o ne jos komplektavimo specifikacijos (KS) komponentus. Todėl patvirtię galite palikti gamybos užsakymų komponentų priskyrimus kintamus. Naudojant vieno lygio žymėjimą sistema gali optimizuoti, kad sistema gali atlikti paskutiniųjų minučių poreikio pokyčius. Standartiniu *vieno* lygio žymėjimu poreikio užsakymai žymimi pagal jų įvykdymo užsakymus, bet įvykdymo užsakymai nepažymėti, jei yra likęs kiekis.
- *Išplėstinis vieno* lygio – naudojamas vieno lygio žymėjimas. Išplėstinio *vieno* lygio žymėjimo metu poreikio užsakymai žymimi pagal jų įvykdymo užsakymus, o įvykdymo užsakymai visada žymimi, neatsižvelgiant į tai, ar liko kiekio.

Šios pasirinktys taip pat **galimos** **·** **lauke** Atnaujinti žymėjimą puslapio Standartinio atnaujinimo skirtuke Standartinis atnaujinimas, **kuriame nurodote numatytąjį dialogo lango Virtimas** pasirinkimą.

Norėdami gauti daugiau informacijos, žr. [atsargų žymėjimą naudodami planavimo optimizavimą](planning-optimization/marking.md).

## <a name="set-delay-tolerance-negative-days-at-the-master-plan-level"></a>Nustatyti nuokrypį dėl vėlavimo (neigiamos dienos) bendrojo plano lygiu

Gamybos *pagal užsakymą tiekimo automatizavimo* funkcija suteikia galimybę konfigūruoti leistiną uždelsimo nuokrypį (neigiamas dienas) bendrojo plano lygiu. Nustatymas taip pat galimas prekės padengimo ir padengimo grupės lygiuose. Jei neigiamos dienos priskiriamos daugiau nei viename lygyje, sistema taiko šią hierarchiją, kad nuspręstų, kurį parametrą naudoti:

- Jei neigiamų dienų yra sukonfigūruotos bendrojo plano **puslapyje**, šis parametras panaikina visus kitus neigiamus dienų nustatymus, kai planas paleidžiamas.
- Jei neigiamos dienos yra sukonfigūruotos prekių padengimo **puslapyje**, šis parametras panaikina padengimo grupės nustatymus.
- Neigiamos dienos, kurios sukonfigūruotos padengimo **grupių** puslapyje, taikomos tik tada, jei atitinkamos prekės arba bendrojo plano neigiamos dienos nebuvo sukonfigūruotos.

Norėdami nustatyti neigiamas bendrojo plano dienas, atlikite šiuos veiksmus.

1. Eikite į **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**.
1. Sąrašo srityje pasirinkite bendrąjį planą arba kurkite naują.
1. Laiko ribose **dienomis "** FastTab" nustatykite parinktį **Neigiamos dienos** kaip *Taip*.
1. Artimiausiuose laukuose įveskite leidžiamų neigiamų dienų skaičių.

Daugiau informacijos apie neigiamų dienų naudojimą ieškokite sulaikyme leistinas [nuokrypis (neigiamos dienos).](planning-optimization/delay-tolerance.md)

## <a name="control-the-pegging-sequence-used-during-master-planning"></a>Valdyti iškvietimo seką, naudojamą bendrojo planavimo metu

Bendrasis planavimas naudoja iškvietimo *seką, kad* nustatytų, kuris tiekimas padengs kurį poreikį. Gamybos *pagal užsakymą tiekimo automatizavimo* funkcija įtraukia **naują parinktį Naudoti naujausią** galimą tiekimo parinktį, kuri leidžia jums labiau kontroliuoti iškvietimo seką. Nauja pasirinktis leidžia išlaikyti produktus, kuriuos galima naudoti paskutinėmis minutėmis, ir optimizuoti esamo tiekimo naudojimą, numesdami naujausią galimą tiekimą poreikiui, užuot naudojus pirmą galimą tiekimą.

Galite nustatyti iškvietimo seką pagrindiniame plane, prekės padengimo ar padengimo grupės lygyje. Jei iškvietimo seka nustatyta daugiau nei viename lygyje, sistema taiko šią hierarchiją, kad nuspręstų, kurį parametrą naudoti:

- Jei iškvietimo seka nustatyta bendrojo plano **puslapyje**, šis parametras panaikina visus kitus iškvietimo sekos parametrus, kai planas paleidžiamas.
- Jei prekių padengimo puslapyje nustatyta iškvietimo **seka, šis parametras** panaikina padengimo grupės nustatymus.
- Padengimo grupių puslapyje nustatyta **iškvietimo** seka taikoma tik tada, jei iškvietimo sekos parametrai nebuvo sukonfigūruoti pagal atitinkamą prekę arba bendrąjį planą.

Norėdami nustatyti iškvietimą padengimo grupės lygiu, atlikite šiuos veiksmus.

1. Pasirinkite **Bendrasis planavimas \> Sąranka \> Padengimas \> Padengimo grupės**.
1. Pasirinkite grupę sąrašo srityje arba kurkite naują.
1. Bendrajame **·** **·** **FastTab iškvietimo** **sekos** skyriuje Naudokite laukus Naudoti turimos atsargos ir Naudokite naujausius tiekimo laukus, norėdami konfigūruoti iškvietimo seką. Toliau šiame skyriuje pateikiamoje lentelėje rodoma, kaip šie nustatymai sujungiami, norint apibrėžti iškvietimo seką.

Norėdami nustatyti iškvietimą prekės padengimo lygyje, atlikite šiuos veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Tinklelyje pasirinkite produktą arba sukurkite naują.
1. Veiksmų srities skirtuke Planas **pasirinkite Prekės padengimas** **.**
1. Prekių **padengimo** puslapis pateikia eilutes, kurios leidžia nustatyti padengimo taisykles, taikomas prekei kiekviename sandėlyje. Pasirinkite esamą eilutę tinklelyje arba sukurkite naują.
1. Skirtuke **Bendra** pažymėkite žymės langelį **Perrašyti iškvietimo** seką.
1. Norėdami konfigūruoti **iškvietimo seką, naudokite** **laukus Naudoti turimas** atsargas ir Naudoti naujausius tiekimo laukus. Toliau šiame skyriuje pateikiamoje lentelėje rodoma, kaip šie nustatymai sujungiami, norint apibrėžti iškvietimo seką.

Norėdami nustatyti iškvietimą bendrojo plano lygiu, atlikite šiuos veiksmus.

1. Eikite į **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**.
1. Sąrašo srityje pasirinkite bendrąjį planą arba kurkite naują.
1. Bendrajame **FastTab** nustatykite iškvietimo **sekos perrašymo parinktį** *Taip*.
1. Norėdami konfigūruoti **iškvietimo seką, naudokite** **laukus Naudoti turimas** atsargas ir Naudoti naujausius tiekimo laukus. Toliau šiame skyriuje pateikiamoje lentelėje rodoma, kaip šie nustatymai sujungiami, norint apibrėžti iškvietimo seką.

Šioje lentelėje parodyta, kaip sujungti **naudojimo turimos atsargos** **ir Naudoti** naujausius tiekimo parametrus, norint nustatyti iškvietimo seką.

| | Naudoti paskutinį tiekimą = Taip | Naudoti paskutinį tiekimą = Ne |
|---|---|---|
| **Naudoti turimos atsargos prieš visą** = *tiekimą* | <ol><li>Turimos atsargos</li><li>Esamas tiekimas, kuris gali atitikti poreikio datą</li><li>Esamas tiekimas, kuris negali atitikti poreikio datos, bet vis dar per neigiamas dienas</li><li>Sukurti naują tiekimą (suplanuotas užsakymas)</li></ol> | <ol><li>Turimos atsargos</li><li>Esamas tiekimas, kuris gali atitikti poreikio datą</li><li>Esamas tiekimas, kuris negali atitikti poreikio datos, bet vis dar per neigiamas dienas</li><li>Sukurti naują tiekimą (suplanuotas užsakymas)</li></ol> |
| **Naudoti turimos atsargos Po** = *viso tiekimo* | <ol><li>Esamas tiekimas, kuris gali atitikti poreikio datą</li><li>Turimos atsargos</li><li>Esamas tiekimas, kuris negali atitikti poreikio datos, bet vis dar per neigiamas dienas</li><li>Sukurti naują tiekimą (suplanuotas užsakymas)</li></ol> | <ol><li>Esamas tiekimas, kuris gali atitikti poreikio datą</li><li>Esamas tiekimas, kuris negali atitikti poreikio datos, bet vis dar per neigiamas dienas</li><li>Turimos atsargos</li><li>Sukurti naują tiekimą (suplanuotas užsakymas)</li></ol> |

## <a name="review-and-set-the-fulfillment-policy-that-applies-to-each-sales-order"></a>Peržiūrėti ir nustatyti įvykdymo strategiją, kuri taikoma kiekvienam pardavimo užsakymui

Įvykdymo strategijos kontroliuoja bendrosios užsakymo kainos ar kiekio, kuris turi būti faktiškai rezervuotas prieš išleidžiant pardavimo užsakymą į sandėlį, procentinę dalį. Galite nustatyti visuotinę numatytąją vykdymo strategiją ir nepaisyti jos konkretiems klientams, jei to reikia. Gamybos *pagal užsakymą tiekimo* automatizavimo funkcija suteikia galimybę peržiūrėti, kokia numatytoji strategija iš tikrųjų taikoma bet kokiai tvarkai ir, jei reikia, taikyti specialų užsakymo nepaisymus.

- Norėdami nustatyti numatytąją pardavimo užsakymų įvykdymo strategiją, eikite į gautinų **sumų \> nustatymo gautinų \> sumų parametrus**. Tada skirtuke **Sandėlio** valdymas **nustatykite pardavimo užsakymo** vykdymo strategijos lauką kaip strategijos, kurią norite naudoti, pavadinimą. 
- Norėdami nustatyti pardavimo užsakymų konkretaus kliento įvykdymo strategiją, eikite į Gautinų **sumų klientus \>\> Visi klientai**. Tada skirtuke **Sandėlis** nustatykite **įvykdymo** strategijos lauką kaip strategijos, kurią norite naudoti, pavadinimą.

Norėdami peržiūrėti numatytąją strategiją, kuri taikoma bet kokiai tvarkai ir taikomos konkrečiam užsakymui, atlikite šiuos veiksmus.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Atidarykite pardavimo užsakymą, kurį norite patikrinti arba redaguoti.
1. Pasirinkite antraštės **rodinį**.
1. Sandėlio **"** FastTab" peržiūrėkite ir redaguokite šiuos laukus, jei reikia:

    - **Užsakymo įvykdymo strategija** – pasirinkite įvykdymo strategiją, kuri bus naudojama pasirinktam užsakymui. Numatytosios strategijos bus nepaisoma. Norėdami naudoti numatytąją įvykdymo strategiją, kuri rodoma numatytojo **įvykdymo strategijos lauke**, palikite šį lauką tuščią.
    - **Numatytoji įvykdymo** strategija – šiame lauke rodoma numatytoji įvykdymo strategija, taikoma, jei **užsakymo vykdymo strategijos** laukas yra tuščias. Šis laukas skirtas tik skaityti. Jei jis tuščias, nebus nurodyta konkretaus kliento arba visuotinės numatytosios įvykdymo strategijos.

    Jei užsakymo **įvykdymo strategijos** laukas ir numatytosios **vykdymo strategijos** laukas yra tušti, įvykdymo strategija nėra taikoma. Tačiau gali būti taikomi kiti apribojimai ir gali reikalauti, kad prieš išduojant pardavimo užsakymą būtų įvykdytas rezervavimas ar kitos sąlygos.

## <a name="set-the-delivery-mode-and-terms-on-individual-purchase-order-lines"></a>Atskirose pirkimo užsakymo eilutėse nustatyti pristatymo būdą ir sąlygas

Į visus pirkimo užsakymus **įtrauktos** pristatymo sąlygos **ir pristatymo būdo** parametrai užsakymo antraštėje. Gamybos *pagal užsakymą tiekimo automatizavimo funkcija* įtraukia šiuos parametrus į kiekvieną užsakymo eilutę. Todėl, jei reikia, galite nustatyti bet kurių **ar visų** **užsakymo** eilučių pristatymo sąlygų ir (arba) pristatymo būdo vertės nepaisymus. Eilutėms, kuriose nepaisymo nėra, naudojama antraštės vertė. Galite nurodyti, ar vieno ar abiejų užsakymo antraštės laukų vertės pakeitimas turėtų atnaujinti ir visas eilutes.

Norėdami nurodyti, kas turi būti daroma **eilutės** nustatymuose, jei vartotojas pakeičia pristatymo sąlygas ir (**arba**) pristatymo būdo vertę užsakymo antraštėje, atlikite šiuos veiksmus.

1. Eikite į **Įsigijimas ir šaltinio pasirinkimas \> Sąranka \> Įsigijimo ir šaltinio pasirinkimo parametrai**.
1. Skirtuke **Bendra**, numatytųjų verčių **ir parametrų** "FastTab", pasirinkite saitą **Naujinti užsakymo** eilutes.
1. Dialogo lango **Atnaujinti užsakymo** eilutes laukuose **Atnaujinamos pristatymo sąlygos** **ir Atnaujinti pristatymo būdą pasirinkite** vieną iš šių verčių:

    - *Niekada* – niekada ne naujinti užsakymo eilučių, kai užsakymo antraštėje pakeičiami nustatymai.
    - *Visada* – visada atnaujinti visas užsakymo eilutes, kai užsakymo antraštėje pakeičiami nustatymai.
    - *Paraginti* – jei vartotojas pakeičia vieną arba abu užsakymo antraštės nustatymus, atidarykite dialogo įrašykite, kuriame klausiama, ar vartotojas nori atnaujinti visas eilutes, kad jos atitiktų vieną ar abu parametrus.

Norėdami nustatyti pristatymo informaciją pirkimo užsakymo antraštėje, atlikite šiuos veiksmus.

1. Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Atidarykite pirkimo užsakymą, kurį norite redaguoti.
1. Pasirinkite antraštės **rodinį**.
1. Jei reikia **,** pristatymo "FastTab" **nustatykite pristatymo** būdo **ir pristatymo** sąlygų laukus.
1. Atsižvelgiant į parametrus įsigijimo ir **pirkimo** parametrų puslapyje, gali būti, kad jūsų paklaus, ar norite pritaikyti pakeitimus visoms užsakymo eilutėms.

Norėdami nustatyti pirkimo užsakymo eilutės pristatymo informacijos nepaisymus, atlikite šiuos veiksmus.

1. Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Atidarykite pirkimo užsakymą, kurį norite redaguoti.
1. Pasirinkite eilučių **rodinį**.
1. Pirkimo užsakymo **eilutėse** "FastTab" pasirinkite norimą redaguoti eilutę.
1. Eilutės informacijos **"** FastTab", skirtuke **Pristatymas**, nustatykite **laukus Pristatymo būdas ir** **Pristatymo** sąlygos. Išvalykite vieną arba abu laukus, kad antraštėje būtų naudojami gretinimo parametrai.

Vidinės įmonės užsakymų **kiekvienos** **pirkimo** užsakymo eilutės laukų Pristatymo būdas ir Pristatymo sąlygos vertės bus sinchronizuojamos tarp pirkimo užsakymo ir su juo susijusio pardavimo užsakymo.

## <a name="sync-external-item-ids-and-descriptions-for-intercompany-orders"></a>Sinchronizuoti vidinės įmonės užsakymų išorinius prekių PVM ir aprašus

Vidinės įmonės *užsakymuose "gamyba* pagal užsakymą" tiekimo automatizavimo funkcija įgalina išorinius prekių PVM ir tekstinius aprašymus pirkimo užsakymo eilutėse sinchronizuoti su susijusiomis vidinės įmonės pardavimo užsakymo eilutėmis, neatsižvelgiant į tai, ar pirkimo užsakymas skirtas tiesioginiam pristatymui. Priemonė taip pat suteikia galimybę vidinės įmonės pirkimo užsakyme nurodyti galutinę išorinio kliento sąskaitą. Tada sistema automatiškai rašys išorinius prekių ID ir tekstinius aprašymus iš išorinio kliento įrašo, o ne iš (vidinės) vidinės įmonės tiekėjo įrašo.

Norėdami nustatyti vidinės įmonės tiekėją sinchronizuoti išorinius prekių PVM ir prekių pavadinimus tarp vidinės įmonės pirkimo užsakymų ir susijusių vidinės įmonės pardavimo užsakymų, atlikite šiuos veiksmus.

1. Eikite į **Įsigijimas ir šaltinio pasirinkimas \> Tiekėjai \> Visi tiekėjai**.
1. Pasirinkti vidinės įmonės tiekėją, kurį norite nustatyti.
1. Veiksmų srities skirtuko Bendra **grupėje** **Nustatymas pasirinkite** Vidinė **įmonė**.
1. Vidinės įmonės **puslapio skirtuke** Pirkimo užsakymas skirtuko **Vidinės** įmonės pirkimo užsakymas -**\> Vidinės įmonės pardavimo užsakymas skyriuje pažymėkite žymės** langelį Išorinis prekės ID **ir** prekės pavadinimas.

Norėdami nurodyti vidinės įmonės pirkimo užsakymo galutinę išorinio kliento sąskaitą, atlikite šiuos veiksmus. Kliento **sąskaitos laukas** taikomas tik vidinės įmonės pirkimo užsakymams. Jį naudokite norėdami nurodyti kliento, kuris galiausiai gaus prekes, sąskaitos numerį. Kai šis laukas nustatytas, pirkimo užsakymo eilutės užuot vidinės įmonės tiekėjo, nurodyto pirkimo užsakyme, turės atlikti išorinius prekių aprašymus ir numerius iš nurodytos kliento sąskaitos. Jei kliento kodą pakeisite vėliau, išoriniai prekių aprašymai ir PVM bus atnaujinti, kad jie atitiktų naujos sąskaitos vertes. Kiekvienos eilutės išoriniai prekių aprašymai ir JŲ identifikavimo failai taip pat bus sinchronizuoti su atitinkančiu vidinės įmonės pardavimo užsakymu.

1. Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Atidarykite pirkimo užsakymą, kurį norite nustatyti, arba sukurkite naują.
1. Pasirinkite antraštės **rodinį**.
1. Nuorodos skyriuje **nustatykite** lauką **Kliento kodas** pagal atitinkamą išorinį kliento kodą.

Norėdami nurodyti išorinius prekės IDENTIFIKAVIMO ir tekstinius vidinės įmonės užsakymo eilutės aprašymus, atlikite šiuos veiksmus. Jūsų nustatytos vertės bus sinchronizuojamos su susijusios vidinės įmonės pardavimo užsakymo eilutėmis, nepaisant to, ar pirkimo užsakymas skirtas tiesioginiam pristatymui.

1. Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Atidarykite pirkimo užsakymą, kurį norite nustatyti, arba sukurkite naują.
1. Pasirinkite eilučių **rodinį**.
1. Pirkimo užsakymo **eilutėse** "FastTab" pasirinkite norimą redaguoti eilutę.
1. Eilutės **informacijos** "FastTab", **skirtuke** Bendra, **užsakymo** eilutės skyriaus lauke **Tekstas**, pateikite išorinį prekės, nurodytos pasirinktoje užsakymo eilutėje, aprašymą. Ši vertė bus sinchronizuojama su susijusia vidinės įmonės pardavimo užsakymo eilute.
1. **Nuorodos** skyriaus išoriniame **lauke** pateikite pasirinktos užsakymo eilutėje nurodytos prekės išorinio prekės ID. Ši vertė bus sinchronizuojama su susijusia vidinės įmonės pardavimo užsakymo eilute.

Daugiau informacijos ieškokite išorinio [kliento vidinės įmonės pardavimo užsakymo kūrimas ir SF](../sales-marketing/intercompany-sales-order-for-external-customer.md).
