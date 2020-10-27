---
title: Pirkimo užsakymų gaunamų krovinių sandėlio tvarkymas
description: Šioje temoje aprašomas pirkimo užsakymų gaunamų krovinių sandėlio tvarkymo procesas.
author: omulvad
manager: tfehr
ms.date: 03/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-21
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: f165a6187332a45e77c22de6eb10e227bc1c8f4c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985023"
---
# <a name="warehouse-handling-of-inbound-loads-for-purchase-orders"></a>Pirkimo užsakymų gaunamų krovinių sandėlio tvarkymas

Šioje temoje aprašomas pirkimo užsakymų gaunamų krovinių sandėlio tvarkymo procesas.

Kiekvienam gaunamam kroviniui jūsų sistemoje jau turėtų būti susijęs pardavimo užsakymas, joje taip pat gali būti susijusio krovinio specifikacija ir (arba) transportavimo planas. Norėdami gauti daugiau informacijos apie tai, kaip kurti ir valdyti gaunamus krovinius, žr. [Verslo procesai: gaunamų krovinių transportavimo planavimas](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/business-process-planning-transportation-for-inbound-loads).

## <a name="overview-how-inbound-loads-are-created-registered-and-received"></a>Apžvalga: kaip kurti, registruoti ir gauti gaunamus krovinius

Toliau pateiktame paveikslėlyje parodytas įprastas gaunamų krovinių, kurie atvykę į jūsų sandėlį turi pirkimo užsakymo kiekius, tvarkymo srautas.

![Gaunamų krovinių tvarkymo procesas](media/inbound-process.png "Gaunamų krovinių tvarkymo procesas")

1. **Tiekėjas patvirtina pirkimo užsakymą.**

    Procesas prasideda, kai pirkimo užsakymas įvedamas į sistemą ir tada pristatomas tiekėjui, kuris patvirtina užsakymą. Pirkimo užsakymas turi būti prieš jums sukuriant gaunamo krovinio įrašą. Tačiau gaunamą krovinį galite sukurti net tuo atveju, jei užsakymas nepatvirtintas. Daugiau informacijos žr. [Pirkimo užsakymų tvirtinimas](../procurement/purchase-order-approval-confirmation.md).

1. **Gaunamo krovinio įrašas sukuriamas, kad būtų galima planuoti atvykimą ir jo turinį.**

    Gaunamo krovinio įrašas rodo vieno ar kelių pirkimo užsakymų tiekėjo siuntą. Tikimasi, kad krovinys į sandėlį atvyks kaip vienas faktinis transportavimo vienetas (pvz., sunkvežimio krovinys). Gaunamo krovinio įrašas naudojamas planuojant ir leidžia logistikos koordinatoriui stebėti krovinio keliavimo iš tiekėjo eigą. Jis taip pat naudojamas užsakymo eilučių kiekiams registruoti ir eigai valdyti atliekant sandėlio operacijas, pvz., gavimo ir padėjimo. Krovinius galima kurti automatiškai arba rankiniu būdu, ir jie gali būti pagrįsti pirkimo užsakymu arba išankstiniu siuntimo pranešimu (ASN). Daugiau informacijos žr. [Gaunamo krovinio kūrimas arba modifikavimas](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/create-or-modify-an-inbound-load).

1. **Tiekėjas patvirtina krovinio išsiuntimą.**

    Tiekėjui išsiuntus krovinį, gaunančio sandėlio logistikos koordinatorius patvirtina krovinio siuntimą. Jeigu gaunančioji įmonė naudoja **transportavimo valdymo** modulį, gaunamų siuntų patvirtinimas suaktyvins kitus krovinio valdymo procesus, susietus su gaunamais kroviniais. Norėdami gauti daugiau informacijos, žr. [Krovinio siuntimo patvirtinimas](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/confirm-a-load-for-shipping).

1. **Krovinys pristatomas į sandėlį, ir darbuotojai užregistruoja kiekius.**

    Kai į sandėlio priėmimo rampą atvyksta sunkvežimio krovinys, sandėlio darbuotojai užregistruoja krovinio kiekius. Kai naudojamas **sandėlio valdymo** modulis, darbuotojai atlieka registraciją naudodami mobiliuosius įrenginius. Norėdami gauti daugiau informacijos, žr. [Produkto gavimas pagal pirkimo užsakymus – registracija](../procurement/product-receipt-against-purchase-orders.md#registration) ir [Gaunamo krovinio prekių kiekių registravimas](#register-item-quantities-arriving).

1. **Užregistruoti krovinio kiekiai registruojami pagal pirkimo užsakymus.**

    Užregistravus gauto krovinio kiekius, šie produkto gavimo kiekiai turi būti užregistruoti įmonės atsargų didžiojoje knygoje, kad būtų įrašytas faktinis atsargų padidėjimas. Norėdami gauti daugiau informacijos, žr. [Produkto gavimas pagal pirkimo užsakymus – produkto gavimas](../procurement/product-receipt-against-purchase-orders.md#product-receipt) ir [Registruoti užregistruotus produkto kiekius pagal pirkimo užsakymus](#post-registered-quantities).

## <a name="register-item-quantities-that-arrive-on-an-inbound-load"></a><a name="register-item-quantities-arriving"></a>Užregistruokite prekių, atvykusių su gaunamu kroviniu, kiekius

„Microsoft Dynamics 365 Supply Chain Management“ palaiko kelis būdus, kuriais galima užregistruoti užsakytų produktų gavimą. Todėl galite konfigūruoti sistemą, kad ji atitiktų specifinius jūsų verslo poreikius. Šiame skyriuje aprašoma, kaip užregistruoti gaunamų prekių kiekius naudojant mobilųjį įrenginį, kai sistemoje įjungtas patobulinto sandėliavimo valdymo funkcija. Tačiau yra alternatyvus srautas, pagrįstas prekių gavimo žurnalo, o ne mobiliojo įrenginio naudojimu. Daugiau informacijos apie tokį srautą žr. [Prekių, kurioms įjungta patobulinto sandėliavimo funkcija, registravimas naudojant prekių gavimo žurnalą](tasks/register-items-advanced-warehousing.md).

Kai gaunamas krovinys pirmą kartą atvyksta į sandėlį, sandėlio darbuotojai turi užregistruoti siuntoje esančių prekių kiekius. Paprastai jie naudoja nešiojamus skaitytuvus. Šią darbo eigą galima naudoti tik tada, kai sistemoje yra toliau nurodyti elementai.

- **Gaunamo krovinio įrašas, apibrėžiantis prekių kiekius, kuriuos tikimasi gauti su siunta**

    Paprastai tiekėjas patvirtina gaunamo krovinio įrašą prieš siuntai atvykstant į sandėlį. Todėl krovinio būsena yra _Išsiųsta_. Tačiau sandėlio darbuotojai taip pat gali užregistruoti prekių kiekius tų krovinių, kurių būsena yra _Atvira_ arba _Gauta_.

- **Mobiliojo įrenginio meniu, sukonfigūruotas palaikyti krovinio gavimą**

    [Sandėliavimo programėlė](install-configure-warehousing-app.md), skirta mobiliesiems įrenginiams, palaiko šiuos darbo kūrimo procesus:

    - Krovinio prekės gavimas
    - Krovinio prekės gavimas ir atidėjimas
    - Mišrių numerių lentelių gavimas, kai mobiliojo įrenginio meniu elemento laukas **Šaltinio dokumento eilutės identifikavimo metodas** nustatytas kaip _Krovinio prekės gavimas_. Daugiau informacijos žr. [Mišrių numerio lentelių gavimas](mixed-license-plate-receiving.md).
    - Mišrių numerių lentelių gavimas ir padėjimas, kai mobiliojo įrenginio meniu elemento laukas **Šaltinio dokumento eilutės identifikavimo metodas** nustatytas kaip _Krovinio prekės gavimas_. Daugiau informacijos žr. [Mišrių numerio lentelių gavimas](mixed-license-plate-receiving.md).

    > [!NOTE]
    > Nepriklausomai nuo proceso sistema sugeneruos darbą paimti kiekius, užregistruotus priimančioje vietoje, ir padėti juos į įprastą saugojimo vietą. Kai naudojamas procesas _Krovinio prekės gavimas ir padėjimas_ arba _Mišrių numerio lentelių gavimas ir padėjimas_, krovinio kiekį užregistravusiam darbuotojui įrenginys taip pat paves atlikti padėjimo darbą, kuris yra registravimo užduoties dalis. Priešingai, procesų _Krovinio prekės gavimas_ ir _Mišrių numerio lentelių gavimas_ atveju, daroma prielaida, kad padėjimo darbas bus atliktas atskirai nuo registravimo užduoties.

- **Darbo šablonas, apibrėžiantis gaunamų krovinių paėmimo ir padėjimo darbus**

    Ši prekė susieta su ankstesnėmis prekėmis. Turite turėti bent vieną darbo šabloną, kurio darbo užsakymo tipas būtų _Pirkimo užsakymas_, ir jame turi būti paėmimo / padėjimo darbų tipų rinkinys.

Mobilusis įrenginys pateikia už gavimą atsakingam sandėlio klerkui nuorodas, padedančias atlikti krovinio kiekio registravimą. Šiame registravimo operacijų sraute turi būti mažiausiai tiek veiksmų, kuriuos reikia atlikti su kiekvieno krovinio ID, kiek nurodyta toliau.

1. Įveskite krovinio ID.
2. Įveskite gautos prekės numerį.
3. Įveskite kiekį pagal tą gautos prekės numerį.
4. Įveskite prekės pradinės vietos numerio lentelės numerį, jei sistema nėra nustatyta automatiškai sugeneruoti šį numerį.
5. Bakstelėkite **Gerai**.

Darbuotojui atlikus šiuos veiksmus, sistema atlieka toliau nurodytus atitinkamų objektų atnaujinimus su sąlyga, kad pirkimo užsakymo eilutės kiekis buvo gautas kaip vienas krovinys, ir visi krovinio kiekiai buvo užregistruoti.

| Objektas | Atnaujinimas | Banknotas |
|---|---|---|
| Apkrova | Krovinio eilutėje esantis laukas **Darbo sukurtas kiekis** atnaujintas, kad būtų rodomas užregistruotas kiekis. | Jei krovinys neturi siuntos patvirtinimo, lauko **Krovinio būsena** reikšmė lieka _Išsiųsta_ arba _Atvira_. Jei pradėta bent viena padėjimo darbo eilutė, ji pakeičiama į _Vykdoma_. |
| Pirkimo užsakymo, kuriame užregistruoti susiję krovinio kiekiai, atsargų operacija |<p>Atnaujinami toliau nurodyti laukai.</p><ul><li>Lauko <b>Gavimas</b> reikšmė nustatoma kaip <i>Užregistruota</i>.</li><li>Laukas <b>Vieta</b> atnaujinamas nurodant priėmimo rampos vietos kodą. (Šis kodas nurodomas lauke <b>Numatytoji gavimo vieta</b> kiekvienam sandėliui.)</li><li>Lukas <b>Numerio lentelės</b> atnaujinamas nurodant numerio lentelės numerį, kuris buvo įvestas arba sugeneruotas registravimo metu.</li><li>Laukas <b>Krovinio ID</b> atnaujinamas nurodant krovinio, kurio kiekis buvo užregistruotas, numerį. (Žr. pastabą.)</li></ul> | Galimybė susieti pirkimo užsakymo atsargų operaciją ir krovinio užregistruotus kiekius buvo pristatyta 10.0.9 versijoje kaip pasirenkama funkcija, kuri buvo pavadinta _Susieti pirkimo užsakymo atsargų operacijas su kroviniu_. Ši funkcija ypač naudinga operaciniams srautams, kai vienas nupirktų prekių užsakymas pristatomas kaip keli kroviniai arba kai viename krovinyje yra kelių pirkimo užsakymų kiekiai. |
| Sandėlio padėjimas | Darbas kuriamas remiantis darbo šablonu, kad būtų galima nurodyti darbuotojui perkelti užregistruotus kiekius iš gavimo vietos į įprastą saugojimo vietą. | Saugojimo vietos pasirinkimą kontroliuoja padėjimo vietos nurodymas. Jei neapibrėžtas joks vietos nurodymas, darbo padėjimo vieta yra tuščia. |

Atkreipkite dėmesį, kad sandėlio darbuotojai gali užregistruoti pirkimo užsakymo gavimą su vienu ar keliais susijusiais kroviniais nenaudodami proceso _Krovinio prekės gavimas_. Galimi šie metodai:

- **Mobiliajame įrenginyje:** naudokite procesus _Pirkimo užsakymo gavimo eilutė_ ir _Pirkimo užsakymo gavimo ir padėjimo eilutė_. (Jei pirkimo užsakymo eilutės kiekis susijęs su daugiau nei vienu kroviniu, darbuotojas negali naudoti proceso _Pirkimo užsakymo gavimo eilutė_. Vietoj to, darbuotojui bus pavesta naudoti įrenginio veiksmą, susietą su procesu _Krovinio prekės gavimas_.)
- **Kliento programoje:** naudokite prekių gavimo žurnalą.
- **Kliento programoje:** naudokite veiksmą **Registracija**, kurį galima pasiekti iš pirkimo užsakymo eilutės.

> [!NOTE]
> Jei pirkimo užsakymo gavimas užregistruojamas naudojant bet kurį iš anksčiau nurodytų metodų, ryšys tarp pirkimo užsakymo atsargų operacijos ir krovinio nesukuriamas, net kai įjungta funkcija _Susieti pirkimo užsakymo atsargų operacijas su kroviniu_. Viena šios taisyklės išimtis yra tada, kai naudojate parinktį **Pirkimo užsakymo gavimo eilutė**, ir tik vieno krovinio būsena užsakymo eilutėje yra ne _Gauta_.

### <a name="handle-discrepancies-during-registration-of-inbound-load-quantities"></a>Gaunamo krovinio kiekių registravimo metu atsiradusių nesutapimų tvarkymas

Sandėlių darbuotojai gali atlikti dalinio krovinio kiekio gavimo registravimą. Kiekvienas dalinis krovinio kiekio gavimas sukuria atskirą atsargų operaciją, kurios užregistruoto kiekio gavimo būsena yra _Užregistruota_, o partijos ID nurodo pradinės pirkimo užsakymo eilutės kilmę.

#### <a name="load-under-receiving"></a>Per mažo krovinio gavimas

Jei atvykus kroviniui prekių kiekis yra mažesnis nei nurodyta krovinio įraše, krovinius priimantis sandėlio personalas gali tiesiogiai kliento sistemoje patvirtinti šį neatitikimą sumažindamas krovinio eilutėje nurodytą kiekį, kad jis atitiktų faktinį pristatytą ir užregistruotą kiekį.

#### <a name="load-over-receiving"></a><a name="load-over-receiving"></a>Per didelio krovinio gavimas

Perviršis yra tada, kai krovinys atvyksta, o prekių kiekiai viršija numatytą krovinio eilutės kiekį. Krovinio registravimo metu galite kontroliuoti, ar priimti perviršį ir, jei perviršis priimamas, kokio dydžio jis gali būti.

Norėdami kontroliuoti, kas atsitinka, kaip sandėlio darbuotojas bando užregistruoti pristatymo perteklių, mobiliojo įrenginio meniu elementuose naudokite lauką **Per didelio krovinio gavimas**. Šis laukas pasiekiamas mobiliųjų įrenginių meniu elementuose, kurie naudoja toliau nurodytus darbo kūrimo procesų tipus.

- Krovinio prekės gavimas
- Krovinio prekės gavimas ir atidėjimas
- Mišrių numerių lentelių gavimas (kai lauko **Šaltinio dokumento eilutės identifikavimo metodas** reikšmė nustatyta kaip _Krovinio prekės gavimas_)
- Mišrių numerių lentelių gavimas ir padėjimas (kai lauko **Šaltinio dokumento eilutės identifikavimo metodas** reikšmė nustatyta kaip _Krovinio prekės gavimas_)

Toliau pateikiamoje lentelėje paaiškinamos laukui **Per didelio krovinio gavimas** galimos parinktys.

| Vertė | aprašymas |
|---|---|
| Leisti | Darbuotojai gali užregistruoti kiekių, viršijančių pasirinkto krovinio likusius neregistruotus kiekius, gavimą, tačiau tik tuo atveju, jei bendras užregistruotas kiekis neviršija pirkimo užsakymo eilutės, susietos su kroviniu, kiekio (po pristatymo pertekliaus procento pataisymo). |
| Blokuoti | <p>Darbuotojai negali užregistruoti kiekio gavimo, jei jis viršija likusį neužregistruotą pasirinkto krovinio kiekį (po pristatymo pertekliaus procento pataisymo). Darbuotojas, kuris bando užregistruoti gavimus, gaus klaidą ir negalės tęsti tol, kol jis ar ji neužregistruos kiekio, kuris lygus likusiam neužregistruotam krovinio kiekiui arba yra už jį mažesnis.</p><p>Pagal numatytuosius parametrus krovinio eilutės pristatymo pertekliaus procentinė vertė nukopijuojama iš susietos pirkimo užsakymo eilutės. Kai lauko <b>Per didelio krovinio gavimas</b> reikšmė nustatyta kaip <i>Blokuoti</i>, sistema naudoja pristatymo pertekliaus procentinę vertę, kad apskaičiuotų bendrą kiekį, kurį galima užregistruoti krovinio eilutei. Tačiau, jei reikia, ši vertė gali būti perrašyta atskiriems kroviniams. Šis veiksmas tampa aktualus gaunant srautus, kai keli arba visi pertekliniai kiekiai, sudarantys užsakymo eilutės pristatymo pertekliaus procentą, proporcingai paskirstomi keliems kroviniams. Toliau pateikiamas scenarijaus pavyzdys.</p><ul><li>Vienai pirkimo užsakymo eilutei priskirti keli kroviniai.</li><li>Pirkimo užsakymo eilutėje yra pristatymo pertekliaus procentinė dalis, kuri yra didesnė už 0 (nulį).</li><li>Jau buvo užregistruoti vieno ar daugiau krovinių kiekiai, neatsižvelgiant į pristatymo pertekliaus procentinę dalį.</li><li>Pristatymo pertekliaus kiekis atvyksta su paskutiniu kroviniu.</li></ul><p>Šiame scenarijuje paskutinio krovinio pertekliniam kiekiui užregistruoti mobilųjį įrenginį galima naudoti tik tuo atveju, jei sandėlio vadovas padidina atitinkamo krovinio eilutės pristatymo pertekliaus procentą iš numatytosios vertės į vertę, kuri yra pakankamai didelė, kad visą pristatymo perteklių būtų galima užregistruoti su paskutiniu kroviniu.</p> |
| Blokuoti tik uždariems kroviniams | Darbuotojai gali priimti didesnį atvirų krovinių krovinio eilutės kiekį, bet ne tų krovinių, kurių būsena yra _Gauta_. |

> [!NOTE]
> Numatytoji lauko **Per didelio krovinio gavimas** reikšmė yra _Leisti_. Naudojant šią reikšmę, veiksmas atitinka standartinį veiksmą, kuris buvo prieinamas prie pristatant funkciją _Krovinių kiekiai gauti per dideli_ 10.0.11 versijoje.

### <a name="put-away-the-registered-quantities"></a>Užregistruotų kiekių padėjimas

Mobiliajame įrenginyje užbaigus registraciją, veiksmas _Kiekio gavimo registracija_ atnaujina atsargų ir sandėlio įrašus, nurodydamas, kad kiekiai dabar yra priėmimo rampos vietoje ir juos galima rezervuoti. Tačiau įmonės sandėlio operacijoms paprastai reikia, kad kiekiai būtų perkelti iš priėmimo rampos į įprastą sandėlio saugyklą, kad galėtų vykti tolesni paėmimo procesai. Padėjimo nurodymai yra užfiksuojami padėjimo darbe, kuris automatiškai sugeneruojamas, kai gaunamas krovinys užregistruojamas kaip gautas.

Kai sandėlio darbuotojas užbaigia padėjimo darbą, sistema įrašo ir seka rezultatą atnaujindama kelis objektus, kaip apibendrinta toliau pateiktoje lentelėje.

| Objektas | Atnaujinimas | Banknotas |
|---|---|---|
| Apkrova | <p>Atnaujinami toliau nurodyti laukai.</p><ul><li>Lauko <b>Krovinio būsena</b> reikšmė keičiama į <i>Vykdoma</i>.</li><li>Lauko <b>Darbo būsena</b> reikšmė pakeičiama į <i>Atlikta 100,00 % darbo</i>.</li></ul> | Kai darbuotojas pradeda bent vienos padėjimo darbo eilutės padėjimo užduotį, lauko **Krovinio būsena** reikšmė pakeičiama į _Vykdoma_. |
| Darbo atsargų operacijos, su kuriomis susieti kiekiai buvo padėti | Atnaujinami laukai **Gavimas** ir **Vieta** bei kiti susiję laukai, kad atspindėtų perkėlimą iš gavimo vietos į saugojimo vietą. | Pirkimo užsakymo atsargų operacijos lauko **Gavimo būsena** reikšmė lieka _Užregistruota_. |
| Sandėlio padėjimas | Lauko **Darbo būsena** reikšmė pakeičiama į _Uždaryta_. | |

## <a name="post-registered-product-quantities-against-purchase-orders"></a><a name="post-registered-quantities"></a>Užregistruotų produktų kiekių registravimas pagal pirkimo užsakymus

Po to, kai gauti produktų kiekiai yra užregistruojami sistemoje, jie tampa prieinami rezervavimui ryšium su pardavimo ir kitomis siuntimo bei vidinėmis operacijomis. Tačiau sistema dar nenaujina atsargų (tarpinių) sąskaitų. Šis atnaujinimas gali įvykti tik tada, kai operacijų komanda užregistruoja užregistruotus produktų gavimus.

Norėdami atidaryti puslapį, kuriame galima užregistruoti produkto gavimą, operacijų komandos nariai gali atlikti bet kurį _vieną_ iš toliau nurodytų veiksmų.

- Atidarykite susijusį krovinio įrašą, tada pasirinkite veiksmą **Produkto gavimas**.
- Eikite į **Sandėlio valdymas \> Periodinės užduotys \> Atnaujinti produktų gavimus**, tada lauke **Krovinio ID** nurodykite norimą užregistruoti krovinį.
- Atidarykite susijusį pirkimo užsakymą, tada pasirinkite veiksmą **Produkto gavimas**.
- Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Produktų gavimas \> Produkto gavimo užduoties registravimas**.

Veiksmas **Produkto gavimas**, kurį galima rasti puslapyje **Krovinys** (ir atitinkamame atnaujinimo užduoties puslapyje – **Atnaujinti produktų gavimus**), gali atnaujinti produktų gavimo kiekius tik pirkimo užsakymo kiekiuose, kurių būsena yra _Užregistruota_. Tačiau veiksmas **Produkto gavimas**, kurį galima rasti puslapyje **Pirkimo užsakymas**, gali įtraukti abiejų apdorojimo būsenų kiekius (_Užsakyta_ ir _Užregistruota_). Jis taip pat gali valdyti produkto gavimo registravimo apimtį, panaudodamas tokius papildomus parametrus, kaip _Dabartinio gavimo kiekis_ ir _Užregistruotas kiekis ir paslaugos_.

Gali būti užregistruoti tik tų užsakymų produktų gavimai, kurių būsena yra _Patvirtinta_. Nepatvirtintų pirkimo užsakymų veiksmas **Produkto gavimas** bus rodomas kaip negalimas.

### <a name="post-registered-quantities-from-the-load-page"></a>Užregistruotų kiekių iš krovinio puslapio registravimas

Norint registruoti užregistruotus produktų kiekius iš puslapio **Krovinys**, turi būti įvykdytos toliau nurodytos būtinosios sąlygos.

- Krovinys turi turėti bent vieną kiekio vienetą, kurio būsena yra _Užregistruota_.
- Krovinio būsena turi būti _Išsiųsta_.
- Su kroviniu susieto pirkimo užsakymo būsena turi būti _Patvirtinta_.

> [!NOTE]
> Jei krovinio būsena nebuvo nustatyta kaip _Išsiųsta_, sistema automatiškai patvirtins krovinį prieš paleisdama produkto gavimo atnaujinimą. (Krovinio būsena yra nustatyta kaip _Išsiųsta_, kai vartotojas užregistruoja krovinio gaunamą siuntą.)

Norėdamas užregistruoti produktų gavimo registracijas, susietas su pasirinktu kroviniu, darbuotojas pasirenka veiksmą **Produkto gavimas** puslapyje **Krovinys**. Atidarytame puslapyje yra toliau nurodyta pagrindinė informacija.

- Lauke **Kiekis**, esančiame dalyje **Parametrai** skirtuke **Nustatymai**, rodomas _užregistruotas kiekis_. Kitų parinkčių čia nėra.
- „FastTab“ konteineryje **Apžvalga** esančiame tinklelyje pateikiami visi pirkimo užsakymai, kurie yra įtraukti į pasirinktą krovinį.
- „FastTab“ konteineryje **Eilutės** esančiame tinklelyje pateikiamos visos užsakymo eilutės, kurios turi registruotą kiekį.

> [!NOTE]
> Užsakymo eilučių, rodomų skirtuke **Eilutė**, kiekiai apskaičiuojami skirtingai, atsižvelgiant į tai, ar jūsų „Supply Chain Management“ versijoje pasiekiama ir įjungta funkcija _Leisti kelis vieno krovinio produktų gavimus_.
>
> | Versija | Skaičiavimas |
> |---|---|
> | Versijos iki 10.0.10 versijos ir naujesnės versijos, kuriose funkcija _Leisti kelis vieno krovinio produktų gavimus_ neįjungta | Eilutės kiekis yra visų užregistruotų _tos pirkimo užsakymo eilutės_ kiekių suma, neatsižvelgiant į tai, ar buvo atliktas kelių krovinių registravimas, registravimas atliktas nepriklausomai nuo krovinio, iš mobiliojo įrenginio ar iš kliento programos. |
> | 10.0.10 versija ir naujesnės versijos, kuriose funkcija _Leisti kelis vieno krovinio produktų gavimus_ įjungta | Eilutės kiekis yra visų _krovinio įrašo_, iš kurio buvo inicijuotas veiksmas **Produkto gavimo registravimas**, užregistruotų kiekių suma. |

Kai vartotojas pasirenka **Gerai**, kad patvirtintų produkto gavimo registravimą, sistema atlieka toliau nurodytus pagrindinius atitinkamų objektų atnaujinimus.

| Objektas | Atnaujinimas |
|---|---|
| Pirkimo užsakymo, kurio eilučių kiekiai įtraukti į registravimo aprėptį, atsargų operacija | <p>Atnaujinami toliau nurodyti laukai (tačiau atkreipkite dėmesį, kad yra ir daug kitų atnaujinimų).</p><ul><li>Lauko <b>Gavimas</b> reikšmė nustatoma kaip <i>Gauta</i>.</li><li>Laukas <b>Faktinė data</b> atnaujinamas nurodant registravimo datą.</li></ul> |
| Krovinys, iš kurio vartotojas užregistravo produkto gavimą | Krovinių naujinimai priklausys nuo naudojamos versijos ir lauko **Leisti kelis vieno krovinio produktų gavimus** nustatymo. Taisyklės aprašomos lentelėje, kuri pateikiama toliau šiame skyriuje. |

Laukas **Leisti kelis vieno krovinio produktų gavimus** leidžia įmonėms pasirinkti gaunamo krovinio gavimo strategiją. Priklausomai nuo to, kaip veikia operaciniai srautai, įmonės gali pasirinkti leisti arba neleisti atlikti kelių to paties krovinio produktų gavimų registravimų. Rekomenduojame, kad logistikos vadybininkas lauko **Leisti kelis vieno krovinio produktų gavimus** reikšmę nustatytų į vieną iš toliau nurodytų reikšmių.

- **Ne** – pasirinkite šią reikšmę, jei sandėlio priimantieji darbuotojai visada registruoja visus užsakymų kiekius, kurie pristatomi su kiekvienu kroviniu per nustatytą laiką. Jei kurie nors krovinio kiekiai nėra užregistruoti, sistema daro prielaidą, kad jie nebuvo pristatyti arba nebuvo krovinyje, todėl neturėtų būti laikomi krovinio dalimi. Iš krovinio vykdomas produkto gavimo registravimas naudojasi tokia pačia prielaida. Kartu su produkto gavimu ir visų užregistruotų kiekių atnaujinimu (jo pagrindinė funkcija), jis paskelbia, kai krovinys yra baigtas ir uždarytas papildomam apdorojimui. Tokiu atveju visi krovinio eilučių kiekiai automatiškai atnaujinami į užregistruotus kiekius, registruotų kiekių neturinčios krovinio eilutės panaikinamos, o krovinio būsena pakeičiama į _Gauta_.
- **Taip** – pasirinkite šią reikšmę, jei sandėlio priimantiems darbuotojams reikia daugiau laiko visiems gauto krovinio kiekiams užregistruoti, tačiau tuo tarpu turite užregistruoti jau užregistruotų gautų produktų kiekius. Šiuo atveju logistikos vadybininkas turės palikti krovinį atidarytą, net po to, kai bus atlikta produkto gavimo registravimo užduotis, kad likę krovinio kiekiai galėtų būti reguliariai registruojami ir produkto gavimas atnaujinamas didžiojoje knygoje.
- **Raginimas** – pasirinkite šią reikšmę, jei jūsų krovinio gavimo praktika yra mišri, ir kiekvieną kartą atliekant produkto gavimo registravimą reikia priimti sprendimą.

Toliau pateiktoje lentelėje apibendrinamas nustatymo **Leisti kelis vieno krovinio produktų gavimus** poveikis.

| Leisti kelis vieno krovinio produktų gavimus | Krovinio kiekis | Krovinio būsena | Banknotas |
|---|---|---|---|
| Kai šio lauko nėra (versijos iki 10.0.10) | <p>Krovinio kiekis nustatomas taip, kad jis būtų lygus užregistruotam kiekiui.</p><p>Jei krovinio kiekis atnaujinamas į 0 (nulį) (o tai reiškia, kad jokia registracija neatlikta), krovinio eilutė panaikinama.</p><p>Jei krovinio eilučių nėra, krovinys panaikinamas.</p> | _Gauta_ | Jei yra keli kroviniai užsakymo eilutės užregistruotam kiekiui, atnaujinama tik krovinio, iš kurio buvo užregistruotas gavimas, būsena į _Gauta_. |
| nr. | <p>Krovinio kiekis nustatomas taip, kad jis būtų lygus užregistruotam kiekiui, susijusiam su krovinio ID.</p><p>Jei atsargų operacijai neįrašomas joks krovinio ID, veiksmas atitinka veiksmą versijose iki 10.0.10.</p> | _Gauta_ | |
| Taip | Nėra naujinimų | _Gauta_, jei bendras užregistruotas krovinio kiekis yra lygus arba viršija krovinio kiekį | |
| Taip | Nėra naujinimų | _Išsiųsta_ arba _Vykdoma_, jei bendras užregistruotas krovinio kiekis yra mažesnis už krovinio kiekį | |

Po to, kai lauko **Krovinio būsena** reikšmė nustatoma kaip _Gauta_, tam kroviniui daugiau nebegalima atlikti produkto gavimo registravimų. Tačiau darbuotojas gali užregistruoti likusį užsakymo kiekį su gautu kroviniu, esant toliau nurodytoms sąlygoms. (Daugiau informacijos žr. ankstesniame šios temos skyriuje [Per didelio krovinio gavimas](#load-over-receiving).)

- „Supply Chain Management“ versija yra senesnė nei 10.0.11 versija.
- Funkcija _Krovinių kiekiai gauti per dideli_ yra įjungta, o mobiliojo įrenginio meniu elemento laukas **Krovinio eilutės kiekis pagal gavimą**, skirtas krovinio prekės gavimo veiksmui, nustatytas į _Leisti_.

Norėdamas užregistruoti papildomų užregistruotų krovinio kiekių produkto gavimą su kroviniu, kurio būsena yra _Gauta_, vartotojas turi atlikti registravimo veiksmą iš susieto pirkimo užsakymo.

### <a name="post-registered-quantities-from-the-purchase-order-page"></a>Užregistruotų kiekių iš pirkimo užsakymo puslapio registravimas

Norėdamas registruoti užregistruotus kiekius iš puslapio **Pirkimo užsakymas** puslapio, vartotojas prieš pasirinkdamas veiksmą **Produkto gavimas** užbaigia toliau nurodytas užduotis.

- Lauką **Kiekis**, esantį dalyje **Parametrai** skirtuke **Nustatymai**, nustatykite į _Užregistruotas kiekis_.
- Lauke **Produkto gavimas** įveskite į registravimą įtrauktų pirkimo užsakymų numerius.

> [!NOTE]
> Eilutės kiekis, kuris bus įtrauktas į registravimo apimtį, yra visų užregistruotų tos užsakymo eilutės kiekių suma, neatsižvelgiant į tai, ar buvo atliktas kelių krovinių kiekių registravimas, registravimas atliktas nepriklausomai nuo krovinio, iš mobiliojo įrenginio ar iš kliento programos. Ta pati taisyklė taikoma, kai produkto gavimo registravimas vykdomas iš krovinio, jei tai atliekama, kai lauko **Leisti kelis vieno krovinio produktų gavimus** nėra arba jis neįgalintas.

Kai vartotojas pasirenka **Gerai**, kad patvirtintų produkto gavimo registravimą, sistema atlieka toliau nurodytus pagrindinius atitinkamų objektų atnaujinimus.

| Objektas | Atnaujinimas |
|---|---|
| Pirkimo užsakymo, kurio eilučių kiekiai įtraukti į registravimo aprėptį, atsargų operacija | <p>Atnaujinami toliau nurodyti laukai (tačiau atkreipkite dėmesį, kad yra ir daug kitų atnaujinimų).</p><ul><li>Lauko <b>Gavimas</b> reikšmė nustatoma kaip <i>Gauta</i>.</li><li>Laukas <b>Faktinė data</b> atnaujinamas nurodant produkto gavimo registravimo veiksmo datą.</li></ul> |
| Apkrova | Krovinių atnaujinimai priklauso nuo to, ar laukas **Leisti kelis vieno krovinio produktų gavimus** yra pasiekiamas ir įgalintas. Taisyklės aprašomos kitoje lentelėje. |

Toliau pateiktoje lentelėje apibendrinamas nustatymo **Leisti kelis vieno krovinio produktų gavimus** poveikis.

| Leisti vieno krovinio kelis produkto gavimo kvitus | Krovinio kiekis | Krovinio būsena | Banknotas |
|---|---|---|---|
| Kai šis laukas yra išjungtas arba nepasiekiamas (versijose iki 10.0.10) | Nėra naujinimų | Jokie atnaujinimai neatlikti. (Būsena lieka _Atidaryta_, _Išsiųsta_ arba _Vykdoma_.) | Produkto gavimo registravimas inicijuojamas iš pirkimo užsakymo, todėl atnaujinimo logikoje nėra informacijos apie jo aprėptyje esančių užregistruotų kiekių ir krovinių, su kuriais buvo įrašyta registracija, ryšį. Todėl jis negali pasirinkti krovinio būsenos atnaujinimui. |
| Įgalintos | Nėra naujinimų | <p>Įvyksta vienas iš toliau nurodytų veiksmų.</p><ul><li>Būsena keičiama į <i>Gauta</i>, jei bendra pirkimo užsakymo atsargų operacijų gautų ir nupirktų kiekių suma yra didesnė už krovinio, su kuriuo jie susieti, kiekį arba yra jam lygi.</li><li>Būsena lieka <i>Atidaryta</i>, <i>Išsiųsta</i> arba <i>Vykdoma</i>, jei ankstesnė sąlyga neįvykdoma visoms krovinio eilutėms.</li></ul> | |

### <a name="select-the-appropriate-product-receipt-posting-option-for-your-logistics-operations"></a>Tinkamos produkto gavimo registravimo parinkties pasirinkimas logistikos operacijoms

Kaip buvo aprašyta ankščiau, sistema siūlo dvi produkto gavimo registravimo parinktis. Parinktis galima pasiekti šiose vietose:

- puslapyje **Krovinys** arba iš meniu **Sandėlio valdymas \> Periodinės užduotys** kaip atnaujinimo užduotį;
- puslapyje **Pirkimo užsakymas** arba iš meniu **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Produktų gavimas** kaip atnaujinimo užduotį.

Įmonėms, kurios naudoja krovinius savo gaunamų užsakymų transportavimui ir sandėlio tvarkymui planuoti bei valdyti, patariama naudoti šias funkcijas, kurios yra skirtos dirbti su kroviniais:

- veiksmus **Krovinio prekės gavimas** savo sandėlio mobiliuosiuose įrenginiuose, kurie skirti gautam produkto kiekiui pagal krovinį užregistruoti;
- veiksmus **Produkto gavimo registravimas**, kurie yra inicijuojami iš krovinio, siekiant atnaujinti atsargų didžiąją knygą.

> [!NOTE]
> Kitas kiekio registravimo ir produkto gavimo registravimo funkcijas galima naudoti atitinkamiems gavimo operaciniams procesams palaikyti. Tačiau jei naudosite jas pakaitomis su skirtosiomis į krovinį orientuotomis funkcijomis arba vietoj jų, galite pažeisti krovinio įrašų tikslumą, o dėl to gali sutrikti krovinių valdymo srautų sklandumas.

## <a name="example-scenarios"></a>Scenarijų pavyzdžiai

### <a name="prepare-your-system-to-run-the-sample-scenarios"></a>Parenkite sistemą, kad būtų galima vykdyti pavyzdinius scenarijus

Norėdami peržiūrėti šiame skyriuje aprašytus pavyzdinius scenarijus, pirmiausia turite įsitikinti, kad sistemoje yra įjungtos visos reikiamos funkcijos. Sistemoje taip pat turi būti reikiamų demonstracinių duomenų.

#### <a name="turn-on-the-required-features"></a>Reikiamų funkcijų įjungimas

Šiems scenarijams reikalinga funkcija _Keli produkto gavimo registravimai krovinyje_ ir jo būtinoji funkcija. Administratoriai gali įjungti šias funkcijas atlikdami toliau nurodytus veiksmus.

1. Atidarykite parinkties **Funkcijos valdymas** darbo sritį. (Norėdami gauti išsamią informaciją apie tai, kaip rasti ir naudoti šią darbo sritį, žr. [Funkcijų valdymo apžvalga](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)

1. Įjunkite funkciją _Susieti pirkimo užsakymo atsargų operacijas su kroviniu_, kuri pateikiama taip:

    - **Modulis:** _sandėlio valdymas_
    - **Funkcijos pavadinimas:** _Susieti pirkimo užsakymo atsargų operacijas su kroviniu_

1. Įjunkite funkciją _Keli produkto gavimo registravimai krovinyje_, kuri pateikiama taip:

    - **Modulis:** _sandėlio valdymas_
    - **Funkcijos pavadinimas:** _Keli produkto gavimo registravimai krovinyje_

#### <a name="enable-sample-data"></a>Duomenų pavyzdžių įgalinimas

Norėdami peržiūrėti šiuos scenarijus naudodami nurodytus įrašų ir reikšmių pavyzdžius, turite naudoti sistemą, kurioje įdiegti standartiniai demonstraciniai duomenys. Prieš pradėdami turite pasirinkti juridinį subjektą **USMF**.

#### <a name="add-a-menu-item-for-receiving-load-items-when-a-mobile-device-is-used"></a>Meniu elemento, skirto krovinio prekėms gauti, įtraukimas, kai naudojamas mobilusis įrenginys

Tam, kad sandėlio priimantys darbuotojai galėtų su kroviniu susijusioms gaunamoms atsargoms registruoti naudoti mobilųjį įrenginį, turite šiam tikslui sukurti mobiliojo įrenginio meniu elementą.

Šiame skyriuje sukusite mobiliojo įrenginio meniu elementą ir įtrauksite jį į esamą meniu. Sandėlio darbuotojas gali pasirinkti meniu elementą sandėliavimo programėlėje.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai** ir įsitikinkite, kad mobiliojo įrenginio meniu yra meniu elementas, kurio parametrai yra tokie:

    - **Režimas:** _Darbas_
    - **Darbo kūrimo procesas:** _Krovinio prekės gavimas_
    - **Generuoti numerio lentelę:** _Taip_

    Galite palikti visų parametrų numatytąsias reikšmes.

    ![Mobiliojo įrenginio meniu elementų parametrai](media/inbound-mobile-menu-items.png "Mobiliojo įrenginio meniu elementų parametrai")

    Daugiau informacijos apie tai, kaip nustatyti mobiliojo įrenginio meniu elementus žr. [Mobiliųjų įrenginių nustatymas darbui sandėlyje](configure-mobile-devices-warehouse.md).

2. Kai baigsite nustatyti menių elementą, eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai** ir įtraukite jį į savo mobiliųjų įrenginių meniu struktūrą.

### <a name="example-scenario-1-register-a-load-where-some-items-are-missing"></a>1 scenarijaus pavyzdys: krovinio, kuriame trūksta kai kurių prekių, registravimas

Šis scenarijus rodo, kaip registruoti gaunamo krovinio kiekius, kai yra ne visi numatyti kiekiai. Tada parodoma, kaip užregistruoti pirkimo užsakymo produkto gavimą.

#### <a name="create-a-load-to-plan-receipt-of-a-purchase-order"></a>Krovinio sukūrimas planuojant pirkimo užsakymo gavimą

Atlikdami šią procedūrą jūs neautomatiniu būdu sukursite pirkimo užsakymą ir susijusį krovinį. Tada atnaujinsite krovinį imituodami, kad jis buvo išsiųstas iš tiekėjo (kuris atnaujina krovinio būseną). Tada sandėlio planuotojai, norėdami rasti numatomus gaunamus krovinius, gali filtruoti krovinius pagal **krovinio būseną**.

1. Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Pasirinkite **Naujas**.
1. Dialogo lange **Kurti pirkimo užsakymą** lauko **Tiekėjo sąskaita** reikšmę nustatykite į _1001_.
1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą ir sukurtumėte pirkimo užsakymą.
1. Naujajame pirkimo užsakyme jau yra eilutė dalyje **Pirkimo užsakymo eilutės**. Nustatykite tokias šios eilutės reikšmes:

    - **Prekės numeris:** _A0001_
    - **Sandėlis:** _24_
    - **Kiekis:** _10_

1. Veiksmų srities skirtuke **Pirkimas** pasirinkite **Veiksmai \> Patvirtinti**. Užsakymo būsena dabar yra _Patvirtinta_.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Veiksmai \> Krovinio planavimo darbo sritis**.
1. Puslapio **Krovinio planavimo darbo sritis** veiksmų srities skirtuke **Pasiūla ir paklausa** pasirinkite **Įtraukti \> Į naują krovinį**.
1. Dialogo lange **Krovinio šablono priskyrimas** lauko **Krovinio šablono ID** reikšmę nustatykite į _20' konteineris_.
1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą ir grįžtumėte į darbo sritį.
1. Dalyje **Kroviniai** pasirinkite **Krovinio ID**, kad būtų atidarytas naujai sukurtas krovinys.
1. Peržiūrėkite krovinio antraštės ir eilutės informaciją ir atkreipkite dėmesį į toliau nurodytus punktus.

    - „FastTab“ konteineryje **Krovinys** lauko **Krovinio būsena** reikšmė nustatyta kaip _Atidaryta_.
    - Salyje **Krovinio eilutės** yra viena eilutė, kurioje lauko **Kiekis** reikšmė nustatyta kaip _10_, o lauko **Darbo sukurtas kiekis** reikšmė nustatyta kaip _0_ (nulis).

    ![Krovinio informacija](media/inbound-load-details.png "Krovinio informacija")

1. Veiksmų srities skirtuke **Siuntimas ir gavimas** pasirinkite **Patvirtinti \> Gaunama siunta**. Atkreipkite dėmesį, kad lauko **Krovinio būsena** reikšmė buvo pakeista į _Išsiųsta_.
1. Pasižymėkite **krovinio ID** reikšmę, kad galėtumėte ją panaudoti kitoje procedūroje.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-load"></a>Su kroviniu priimtų kiekių gavimo registravimas

Kai į sandėlio priėmimo rampą atvyksta krovinys, priimantis darbuotojas užregistruoja krovinio kiekius mobiliajame įrenginyje.

1. Norėdami prisijungti prie sandėlio 24, naudokitės mobiliuoju įrenginiu. (Standartiniuose demonstraciniuose duomenyse prisijunkite kaip vartotojo ID naudodami _24_, o kaip slaptažodį – _1_.)
1. Pasirinkite meniu elementą _Krovinio prekės gavimas_, kurį sukūrėte šiam scenarijui.
1. Norėdami įvesti šias reikšmės, vadovaukitės ekrane pateikiamomis duomenų įvedimo instrukcijomis. (Užsakymas gali skirtis priklausomai nuo naudojamo mobiliojo įrenginio arba emuliatoriaus.)

    - **Krovinys** – įveskite krovinio ID, kurį sukūrėte ankstesnėje procedūroje.
    - **Prekė** – įveskite _A0001_, kuri yra prekė, kurios tikimasi šiame krovinyje.
    - **Kiekis** – įveskite _9_ kaip faktinį kiekį, kuris yra krovinyje. Atkreipkite dėmesį, kad šis kiekis yra mažesnis nei numatytas.

1. Eikite toliau per darbo eigą, palikdami visus kitus laukus tuščius arba nustatydami jų numatytąsias reikšmes, kol jūsų įrenginys informuos, kad darbas baigtas.

Krovinio gavimo užduotis dabar baigta, o priimantis darbuotojas gali pereiti prie kitos savo užduoties. Tačiau sandėlio priimantis personalas galiausiai peržiūrės krovinio įrašą ir pamatys, kad gautas kiekis buvo mažesnis nei numatytas. Tada, naudodami žiniatinklio kliento programą jie atliks toliau nurodytą procedūrą.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Sąraše raskite ką tik gautą krovinį. (Jums gali tekti pažymėti žymės langelį **Rodyti uždarytą**, kad būtų įtraukti gaunami kroviniai, kurių krovinio būsena yra _Išsiųsta_.) Tada stulpelyje **Krovinio ID** pasirinkite saitą, kad būtų galima atidaryti krovinį.
1. Krovinio įraše atkreipkite dėmesį, kad lauko **Krovinio būsena** reikšmė lieka _Išsiųsta_, tačiau krovinio eilutėje esančio lauko **Darbo sukurtas kiekis** reikšmė pasikeitė į _9_.
1. Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Sąraše raskite ką tik gautą pirkimą, tada stulpelyje **Pirkimo užsakymas** pasirinkite saitą, kad būtų atidarytas užsakymas.
\
1. „FastTab“ konteineryje **Pirkimo užsakymo eilutės** pasirinkite **Atsargos \> Rodinys \> Operacijos**.
1. Peržiūrėkite dviejų pirkimo užsakymo operacijų informaciją. (Jums gali tekti individualizuoti puslapį **Atsargų operacijos**, kad tinklelyje pamatytumėte lauką **Krovinio ID**.) Turėtumėte matyti dvi operacijas.

    - Operacija, kurios gavimo būsena yra _Registruota_, rodo registravimo kiekį _9_, kuris buvo vykdomas pagal konkretų krovinį naudojant mobilųjį įrenginį. **Krovinio ID** susietas su svarstoma operacija.
    - Operacija, kurio gavimo būsena _Užsakyta_, atspindi likusį neregistruotą užsakymo eilutės kiekį _1_.

#### <a name="product-receiptpost-the-registered-load-quantities-against-purchase-orders"></a>Užregistruotų krovinio kiekių produktų gavimo registravimas pagal pirkimo užsakymus

Šioje procedūroje užregistruosite produkto gavimo atsargas, kurias registravote kroviniui. Todėl gautos atsargos ir su jomis susijusi savikaina bus įtraukta į įmonės didžiąją knygą.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Sąraše raskite gautą krovinį. (Jums gali tekti pažymėti žymės langelį **Rodyti uždarytą**, kad būtų įtraukti gaunami kroviniai, kurių krovinio būsena yra _Išsiųsta_.) Tada stulpelyje **Krovinio ID** pasirinkite saitą, kad būtų galima atidaryti krovinį.
1. Veiksmų srities skirtuke **Siuntimas ir gavimas** pasirinkite **Gauti \> Produkto gavimas**. Jei būsite paraginti patvirtinti veiksmą, pasirinkite **Taip**.
1. Dialogo lango **Produkto gavimo registravimas** „FastTab“ konteineryje **Eilutės** patikrinkite tinklelį. Turėtumėte matyti pirkimo užsakymo eilutę, kuriai buvo užregistruotas kiekis pagal pasirinktą krovinį.

    > [!NOTE]
    > Versijose, kur nėra funkcijos _Keli produkto gavimo registravimai krovinyje_ arba ji neįgalinta, numatytasis kiekis, rodomas tinklelyje **Krovinio eilutės**, bus bendras kiekis, užregistruotas visuose su pirkimo užsakymo eilute susietuose kroviniuose.

1. „FastTab“ konteinerio **Apžvalga** tinklelyje patikrinkite lauką **Produkto gavimas**. Atkreipkite dėmesį, kad jo nustatyta reikšmė yra numeris, rodantis pasirinkto krovinio ID.
1. Pasirinkite **Gerai**, kad užregistruotumėte produkto gavimą ir uždarytumėte dialogo langą **Produkto gavimo registravimas**.
1. Grįžote į krovinio informaciją. Atkreipkite dėmesį į toliau nurodytus punktus.

    - Lauko **Krovinio būsena** reikšmė dabar nustatyta kaip _Gauta_.
    - Krovinio eilutėje krovinio reikšmė **Kiekis** pasikeitė iš _10_ į _9_ vnt., kad atitiktų užregistruotą kiekį, tačiau lauko **Darbo sukurtas kiekis** reikšmė lieka _9_.

Jei pirkimo komanda nesitiki, kad tiekėjas pristatys likusį 1 užsakymo kiekį, ji galės uždaryti užsakymą, atnaujindama eilutės pristatymo likutį į _0_. Tačiau jei greitai nustatoma, kad trūkstama dalis atvyko su pradiniu kroviniu, sandėlio personalas gali atlikti vieną iš toliau nurodytų veiksmų.

- Užregistruokite kiekį su tuo pačiu kroviniu. Šiuo atveju lauko **Krovinio būsena** reikšmė bus iš naujo nustatyta kaip _Išsiųsta_, o lauko **Darbo sukurtas kiekis** reikšmė bus atnaujinta į _10_. Šis pasirinkimas galimas tik toliau nurodytais atvejais.

    - Funkcijos _Krovinių kiekiai gauti per dideli_ nėra arba ji neįgalinta.
    - Funkcija _Krovinių kiekiai gauti per dideli_ yra ir įgalinta, o lauko **Krovinio eilutės kiekis pagal gavimą** reikšmė nustatyta kaip _Leisti_.

- Pridėkite kiekį prie naujo arba esamo krovinio ir apdorokite jį įprastiniu būdu.
- Užregistruokite ir (arba) priimkite kiekį taip, kad nereikėtų tvarkyti krovinio.

### <a name="example-scenario-2-register-quantities-that-arrive-on-multiple-inbound-loads-where-some-items-are-missing"></a>2 scenarijaus pavyzdys: kiekių, atvykstančių su keliais gaunamais kroviniais, kuriuose trūksta kai kurių prekių, registravimas

Šiame scenarijuje gaunama siunta, susijusi su viena pirkimo užsakymo eilute, bus padalinta į du krovinius. Pavyzdžiui, pirkimo užsakymo eilutė gali būti padalinta į kelis krovinius dėl faktinio krovinio svorio ir (arba) tūrio apribojimų.

Šiame scenarijuje taip pat parodoma, kaip apdoroti kelis to pačio krovinio produktų gavimo registravimus. Užregistruosite kiekius, atvykusius su keliais gaunamais kroviniais, tačiau kiekiai nesutaps su numatomais kiekiais. Savikainos naujinimai, vykstantys registruojant produkto gavimą, bus atlikti kelis kartus tam pačiam kroviniui.

#### <a name="set-up-load-receiving-policies"></a>Krovinio gavimo strategijų nustatymas

Atlikdami šią procedūrą įgalinsite kelis produktų gavimo registravimus iš to paties krovinio.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.
1. Skirtuke **Kroviniai** nustatykite lauko **Leisti kelis vieno krovinio produktų gavimus** reikšmę _Taip_.

#### <a name="create-two-loads-to-plan-receipt-of-a-purchase-order"></a>Dviejų krovinių sukūrimas planuojant pirkimo užsakymo gavimą

Atlikdami šią procedūrą sukursite pirkimo užsakymą ir du krovinius. Tada neautomatiniu būdu atnaujinsite kiekvieną krovinį imituodami, kad jį išsiuntė tiekėjas (kuris atnaujina krovinio būseną). Tada sandėlio planuotojai, norėdami rasti numatomus gaunamus krovinius, gali filtruoti krovinius pagal **krovinio būseną**.

Taip pat sužinosite, kaip nustatyti pirkimo užsakymo eilutę, kad galėtumėte gauti kiekį, kuris yra 20 procentų didesnis nei nurodytas eilutės kiekis.

1. Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Pasirinkite **Naujas**.
1. „FastTab“ konteineryje **Tiekėjas** nustatykite lauko **Tiekėjo kodas** reikšmę kaip _1001_, tada pasirinkite **Gerai**.
1. Jūsų naujas pirkimo užsakymas atidaromas, ir tinklelyje **Pirkimo užsakymo eilutės** yra tuščia eilutė. Nustatykite tokias šios užsakymo eilutės reikšmes:

    - **Prekės numeris:** _A0001_
    - **Sandėlis:** _24_
    - **Kiekis:** _10_

1. „FastTab“ konteinerio **Eilutės informacija** skirtuke **Pristatymas** nustatykite lauko **Pristatymo perteklius** reikšmę kaip _20_.
1. Veiksmų srities skirtuke **Pirkimas** pasirinkite **Veiksmai \> Patvirtinti**. Užsakymo būsena dabar yra _Patvirtinta_.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Veiksmai \> Krovinio planavimo darbo sritis**.
1. Puslapio **Krovinio planavimo darbo sritis** veiksmų srities skirtuke **Pasiūla ir paklausa** pasirinkite **Įtraukti \> Į naują krovinį**.
1. Dialogo lange **Krovinio šablono priskyrimas** lauko **Krovinio šablono ID** reikšmę nustatykite į _20' konteineris_. Skirtuke **Informacija** pakeiskite lauko **Kiekis** reikšmę iš _10_ į _5_, kad iš dalies įtrauktumėte pirkimo užsakymo eilutės kiekį.
1. Norėdami pritaikyti nustatymus ir uždaryti dialogo langą, pasirinkite **Gerai**.
1. Norėdami sukurti antrą krovinį, pakartokite 8–10 veiksmus. Šį kartą lauko **Kiekis** reikšmė jau turėtų būti nustatyta kaip _5_.
1. Puslapio **Krovinio planavimo darbo sritis** tinklelyje **Kroviniai** pasirinkite lauko **Krovinio ID** reikšmę pirmam sukurtam kroviniui. Atidaromas puslapis **Krovinio informacija** ir rodomas pasirinktas krovinys. Atlikite šiuos veiksmus.

    1. Veiksmų srities skirtuke **Siuntimas ir gavimas** pasirinkite **Patvirtinti \> Gaunama siunta**.
    1. Atkreipkite dėmesį, kad lauko **Krovinio būsena** reikšmė buvo pakeista į _Išsiųsta_.
    1. Norėdami grįžti į puslapį **Krovinio planavimo darbo sritis** pasirinkite uždarymo mygtuką.

1. Pakartokite ankstesnį žingsnį antrajam sukurtam kroviniui.
1. Atkreipkite dėmesį į dvi lauko **Krovinio ID** reikšmes, kurios rodomos tinklelyje **Kroviniai**.

#### <a name="register-partial-receipt-of-the-quantities-that-arrived-on-the-first-load-and-post-the-registered-load-quantities"></a>Dalinio su pirmuoju kroviniu atvykusių kiekių gavimo užregistravimas ir užregistruotų krovinio kiekių registravimas

Kai į sandėlio priėmimo rampą atvyksta kroviniai, priimantis darbuotojas užregistruoja krovinio kiekius mobiliajame įrenginyje. Tada pagal krovinį užregistravus pirkimo užsakymo produkto gavimą, įmonės didžiojoje knygoje atnaujinama užregistruotų atsargų, kurios yra susietos su kroviniu, savikaina.

Ši procedūra rodo, kaip priimantis darbuotojas užregistruos krovinio kiekius mobiliajame įrenginyje.

1. Norėdami prisijungti prie sandėlio 24, naudokitės mobiliuoju įrenginiu. (Standartiniuose demonstraciniuose duomenyse prisijunkite kaip vartotojo ID naudodami _24_, o kaip slaptažodį – _1_.)
1. Pasirinkite meniu elementą _Krovinio prekės gavimas_, kurį sukūrėte šiam scenarijui.
1. Norėdami įvesti šias reikšmės, vadovaukitės ekrane pateikiamomis duomenų įvedimo instrukcijomis. (Užsakymas gali skirtis priklausomai nuo naudojamo mobiliojo įrenginio arba emuliatoriaus.)

    - **Krovinys** – įveskite pirmojo krovinio ID, kurį sukūrėte ankstesnėje procedūroje.
    - **Prekė** – įveskite _A0001_, kuri yra prekė, kurios tikimasi šiame krovinyje.
    - **Kiekis** – įveskite _3_. Atkreipkite dėmesį, kad šis kiekis yra mažesnis nei numatytas. Šiame scenarijuje įsivaizduokite, kad jūs, priimantis darbuotojas, neturite laiko užregistruoti visų šio krovinio kiekių. Vėliau šioje procedūroje užregistruosite likusius vienetus pakartodami šį veiksmą ir nustatydami lauko **Kiekis** reikšmę į _2_.

1. Eikite toliau per darbo eigą, palikdami visus kitus laukus tuščius arba nustatydami jų numatytąsias reikšmes, kol jūsų įrenginys informuos, kad darbas baigtas.
1. Žiniatinklio kliente eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Sąraše suraskite ką tik gautą krovinį ir pasirinkite **Krovinio ID** reikšmę, kad būtų galima atidaryti krovinį. Atkreipkite dėmesį, kad lauko **Krovinio būsena** reikšmė lieka _Išsiųsta_, tačiau krovinio eilutėje esančio lauko **Darbo sukurtas kiekis** reikšmė pasikeitė į _3_.
1. Veiksmų srities skirtuke **Siuntimas ir gavimas** pasirinkite **Gauti \> Produkto gavimas**. Jei būsite paraginti patvirtinti veiksmą, pasirinkite **Taip**.
1. Dialogo lange **Produkto gavimo registravimas** peržiūrėkite, bet nekeiskite rodomų reikšmių, ir tada pasirinkite **Gerai**.
1. Jūs esate grąžinami į savo pasirinkto krovinio puslapį **Krovinio informacija**. Atkreipkite dėmesį į toliau nurodytus punktus.

    - Lauko **Krovinio būsena** reikšmė lieka nustatyta kaip _Išsiųsta_.
    - Krovinio eilutėje lauko **Kiekis** reikšmė lieka _5_ vnt. (pradinis krovinio kiekis), o lauko **Darbo sukurtas kiekis** reikšmė lieka _3_.

1. Užbaikite likusio šio krovinio kiekio registravimą pakartodami šią procedūrą. Tačiau 3 veiksme lauko **Kiekis** reikšmę nustatykite į _2_.

Pirmojo krovinio gavimo užduotis dabar baigta. Buvo sukurti du produkto gavimo žurnalai, po vieną kiekvienam iš dviejų jūsų atliktų produkto gavimo atnaujinimų.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-second-load-and-account-for-the-overdelivered-quantity"></a>Užregistruokite kiekio, kuris buvo gautas su antruoju kroviniu, gavimą ir kiekio perviršio sąskaitą

Šiame scenarijuje priimantis darbuotojas užregistruos gautą kiekį, kuris viršija krovinio kiekį. Bus leidžiama priimti perviršį, nes sistema nustatyta taip, kad būtų leidžiamas pristatymo perteklius.

1. Norėdami prisijungti prie sandėlio 24, naudokitės mobiliuoju įrenginiu. (Standartiniuose demonstraciniuose duomenyse prisijunkite kaip vartotojo ID naudodami _24_, o kaip slaptažodį – _1_.)
1. Pasirinkite meniu elementą _Krovinio prekės gavimas_, kurį sukūrėte šiam scenarijui.
1. Norėdami įvesti šias reikšmės, vadovaukitės ekrane pateikiamomis duomenų įvedimo instrukcijomis. (Užsakymas gali skirtis priklausomai nuo naudojamo mobiliojo įrenginio arba emuliatoriaus.)

    - **Krovinys** – įveskite antrojo anksčiau sukurto krovinio ID.
    - **Prekė** – įveskite _A0001_, kuri yra prekė, kurios tikimasi šiame krovinyje.
    - **Kiekis** – įveskite reikšmę _7_, kuri reiškia likusį kiekį, kurį tiekėjas turi teisę pristatyti kaip bendro pirkimo užsakymo kiekio (12) dalį (kur 10 yra pradinis užsakymo kiekis, o 2 yra leidžiamas 20 procentų pristatymo pertekliaus kiekis). Atminkite, kad 5 vienetai jau buvo užregistruoti su pirmuoju kroviniu.

Antrojo krovinio kiekis dabar atnaujintas į 7, ir pagal šį kieki gali būti atnaujintas produkto gavimas.
