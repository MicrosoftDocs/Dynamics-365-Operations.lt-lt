---
title: Pritaikomų sandėlio lygio dimensijų rezervavimo strategija
description: Šioje temoje aprašoma atsargų rezervavimo strategija, kuria įmonės, prekiaujančios pagal paketą sekamais produktais ir vykdančios savo logistiką kaip palaikančias WMS operacijas, rezervuoja konkrečius kliento pardavimo užsakymų paketus, net jei rezervavimo hierarchija, kuri yra susieta su produktais, neleidžia rezervuoti tam tikrų paketų.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: eca0b61e1fa6760bfed1a9f9979deddccf6fb1a5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6343779"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a>Lanksti sandėlio dimensijų rezervavimo strategija

[!include [banner](../includes/banner.md)]

Kai *Paketas žemiau\[vietos\]* tipo atsargų rezervavimo hierarchija yra susieta su produktais, įmonėmis, parduodančiomis pagal paketą sekamus produktus ir valdo jų logistiką kaip operacijas, kurios yra įjungtos „ Microsoft Dynamics 365“ sandėlio valdymo sistemai (WMS), negalima rezervuoti tų produktų konkrečių paketų kliento pardavimo užsakymams.

Panašiu būdu, licencijos numeris gali būti rezervuojamas produktams prekybos užsakymuose, kai šie produktai yra susieti su nustatyta rezervacijos hierarchija.

Šis skyrius aprašo inventoriaus rezervacijos politiką, kuri leidžia šiems verslams rezervuoti konkrečius paketus arba licencijos numerius, net jei produktai yra susieti su *Paketo žemiau\[vietos\]* rezervavimo hierarchija.

## <a name="inventory-reservation-hierarchy"></a>Atsargų rezervavimo hierarchija

Šiame skyriuje apibendrinama esama atsargų rezervavimo hierarchija.

Atsargų rezervavimo hierarchija diktuoja tai, kad, kiek tai susiję su saugojimo dimensijomis, poreikio užsakyme yra privalomos vietos, sandėlio ir atsargų būsenos dimensijos. Kitaip tariant, privalomos dimensijos yra visos dimensijos, esančios aukščiau vietos dimensijos rezervavimo hierarchijoje, o sandėlio logika yra atsakinga už vietos priskyrimą pageidaujamam kiekiui ir vietos rezervavimą. Atliekant sąveiką tarp poreikio užsakymo ir sandėlio operacijų, tikimasi, kad poreikio užsakyme bus nurodyta iš kur užsakymas turi būti siunčiamas (tai yra, iš kokios vietos ir sandėlio). Tada sandėliui taikoma jo logika, kad būtų surastas reikiamas kiekis sandėlio patalpose.

Tačiau, siekiant atitikti verslo veiklos modelį, sekimo dimensijos (paketo ir serijos numeriai) yra lankstesnės. Atsargų rezervavimo hierarchijoje gali tilpti scenarijai, kuriuose taikomos šios sąlygos:

- Verslas priklauso nuo jo sandėlio operacijų, kuriomis valdomas kiekių, turinčių paketo ar serijos numerius *po to*, kai sandėliavimo saugykloje buvo surasti kiekiai, išrinkimas. Toks modelis dažnai vadinamas *Paketas žemiau\[vietos\]* arba *Serija žemiau\[vietos\]*. Jis paprastai naudojamas, kai produkto paketo ar serijos numerio identifikacija nėra svarbi klientams, kurie turi paklausą su parduodančiomis įmonėmis.
- Verslas priklauso nuo jo sandėlio operacijų, kuriomis valdomas kiekių, turinčių paketo ar serijos numerius *prieš* tai, kai sandėliavimo saugykloje buvo surasti kiekiai, išrinkimas. Jei paketo ar serijos numeriai yra reikalingi kaip kliento užsakymo specifikacijos dalis, jie įrašomi poreikio užsakyme ir sandėlio operacijoms, surandančioms kiekius sandėlyje, neleidžiama jų keisti. Toks modelis vadinamas *Paketas aukščiau\[vietos\]* arba *Serija aukščiau\[vietos\]*. Kadangi dimensijos aukščiau vietos yra konkretūs poreikio reikalavimai, kurie turi būti įvykdyti, sandėlio logika jų nepaskirstys. Šios dimensijos visada **privalo** būti nurodytos poreikio užsakyme arba susijusiose rezervacijose.

Šiuose scenarijuose problema yra ta, kad kiekvienam išleistam produktui gali būti priskirta tik viena atsargų rezervavimo hierarchija. Todėl, kad WMS galėtų dirbti su sekamomis prekėmis, po to, kai hierarchijos priskyrimas nustato, kada turi būti rezervuotas paketo ar serijos numeris (kai poreikio užsakymas jau užsakytas arba per sandėlio išrinkimo darbą), šis laikas negali būti pakeistas ad hoc pagrindu.

## <a name="flexible-reservation-for-batch-tracked-items"></a>Lankstus pagal paketą sekamų prekių rezervavimas

### <a name="business-scenario"></a>Verslo scenarijus

Šiame scenarijuje įmonė naudoja atsargų strategiją, kurioje pagamintos prekės sekamos pagal paketo numerius. Ši įmonė taip pat naudoja WMS darbo krūvį. Kadangi ši darbo krūvio logika yra tinkamai paruošta planuoti ir vykdyti sandėlio išrinkimo ir siuntimo operacijas, skirtas prekėms, kurioms įgalinti paketai, dauguma pagamintų prekių yra susietos su *Paketas žemiau\[vietos\]* atsargų rezervavimo hierarchija. Šio tipo veiklos sąrankos pranašumas yra tas, kad sprendimai (kurie iš esmės yra rezervavimo sprendimai) dėl to, kurie paketai turi būti paimti ir kur jie turi būti padėti sandėlyje, yra atidėti, kol bus pradėtos sandėlio išrinkimo operacijos. Jos neatliekamos, kai kliento užsakymas pateikiamas.

Nors *Paketas žemiau\[vietos\]* rezervavimo hierarchija puikiai tenkina įmonės veiklos tikslus, daugeliui įmonės nuolatinių klientų reikia to paties paketo, kurį jie anksčiau pirko, kai jie vėl užsisako produktų. Todėl įmonė ieško lankstumo taip, kad būtų tvarkomos paketo rezervavimo taisyklės, jog, atsižvelgiant į kliento norą įsigyti tą pačią prekę, galimi šie būdai:

- Paketo numerį galima įrašyti ir rezervuoti, kai užsakymą priima pardavimo apdorojimo priemonė, ir jo negalima keisti vykdant sandėlio operacijas ir (arba) kitus reikalavimus. Tai padeda užtikrinti, kad užsakytas paketo numeris yra siunčiamas klientui.
- Jei paketo numeris nėra svarbus klientui, sandėlio operacijomis galima nustatyti paketo numerį atliekant išrinkimo darbus, atlikus pardavimo užsakymų registravimą ir rezervavimą.

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a>Konkretaus paketo rezervavimo leidimas pardavimo užsakyme

Norint, kad prekių, susietų su *Paketas žemiau\[vietos\]* atsargų rezervavimo hierarchija, paketo rezervavimo veikimas būtų pageidaujamo dinamiškumo, atsargų valdytojai turi pasirinkti žymės langelį **Leisti rezervuoti pagal poreikio užsakymą**, skirtą **Paketo numerio** lygiui, esančiam puslapyje **Atsargų rezervavimo hierarchijos**.

![Atsargų rezervavimo hierarchijos dinamiškumo išplėtimas.](media/Flexible-inventory-reservation-hierarchy.png)

Pasirinkus **paketo numerio** lygį hierarchijoje, visos aukščiau nurodyto lygio dimensijos ir iki lygio **Vieta** bus pasirenkamos automatiškai. (Pagal numatytuosius parametrus visos dimensijos virš lygio **Vieta** yra iš anksto atrinktos). Šis veikimas atspindi logiką, kai visos dimensijos, esančios tarp paketo numerio ir vietos, taip pat automatiškai rezervuojamos, kai užsakymo eilutėje rezervuojamas konkretus paketo numeris.

> [!NOTE]
> Žymės langelis **Leisti rezervuoti užsakymą pagal poreikį** taikomas tik rezervavimo hierarchijos lygiui, kuris yra mažesnis nei sandėlio vietos dimensija.
>
> **Paketo numeris** ir **Licencijos numeris** yra tik lygiai hierarchijoje, kuri yra atvira lanksčiai rezervavimo politikai. Kitaip tariant, galite pasirinkite **Leisti rezervavimą pagal poreikio užsakymą** pažymimą laukelį **Vietos** ar **Serijinio numerio** lygyje.
>
> Jei jūsų rezervavimo hierarchijoje yra serijos numerio dimensija (kuri visada turi būti mažesnė už lygį **Paketo numeris**) ir, jei jau įjungėte paketo numerio paketui būdingą rezervavimą, sistema toliau tvarkys serijos numerio rezervavimo ir išrinkimo operacijas pagal taisykles, taikomas *Serija žemiau\[vietos\]*  rezervavimo strategijai.

Bet kuriuo metu galite leisti atlikti paketui būdingą rezervaciją *Paketas žemiau\[vietos\]* rezervavimo hierarchijai jūsų diegime. Šis keitimas neturės įtakos jokiems rezervavimams ir atidarytiems sandėlio darbams, kurie buvo sukurti prieš keičiant. Tačiau žymės langelio **Leisti rezervuoti užsakymą pagal poreikį** negalima išvalyti, jei problemų tipo **Rezervuotas užsakytas**, **Rezervuotas faktinis** ar **Užsakytas** atsargų operacijos yra vienai ar daugiau prekių, susijusių su ta rezervavimo hierarchija.

> [!NOTE]
> Jei prekės esama rezervavimo hierarchija neleidžia užsakyti paketo specifikacijos, galite ją iš naujo priskirti rezervavimo hierarchijai, kuri leidžia paketo specifikaciją, jei hierarchijos lygio struktūra vienoda abiejose hierarchijose. Naudokite funkciją **Pakeisti prekių rezervavimo hierarchiją** atlikti priskyrimą iš naujo. Šis keitimas gali būti svarbus, jei norite, kad būtų išvengti dinamiško paketo rezervavimo pagal paketą sekamų prekių porinkiniui, ir norite jį leisti naudoti likusiame produkto portfelyje.

Neatsižvelgiant į tai, ar pasirinkote žymės langelį **Leisti rezervuoti pagal poreikio užsakymą**, jeigu nenorite rezervuoti konkretaus prekės paketo numerio užsakymo eilutėje, vis tiek bus taikoma numatytoji sandėlio operacijų logika, galiojanti *Paketas žemiau\[vietos\]* rezervavimo hierarchijoje.

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a>Kliento užsakymo konkretaus paketo numerio rezervavimas

Po to, kai pagal paketą sekamos prekės *Paketas žemiau\[vietos\]* atsargų rezervavimo hierarchija yra nustatyta taip, kad būtų leidžiama rezervuoti konkrečius paketo numerius pardavimo užsakymuose, pardavimo užsakymų procesoriai galėtų atlikti kliento užsakymus tai pačiai prekei vienu iš šių būdų, atsižvelgiant į kliento užklausą:

- **Įvesti užsakymo informaciją nenurodant paketo numerio** – šis metodas turėtų būti naudojamas, kai produkto paketo specifikacija nėra svarbi klientui. Visi esami procesai, susieti su šio tipo užsakymo tvarkymu, sistemoje lieka nekeisti. Vartotojui nereikia atlikti jokių papildomų veiksmų.
- **Įvesti užsakymo informaciją ir rezervuoti konkretų paketo numerį** – šis metodas turėtų būti naudojamas, kai klientas reikalauja konkretaus paketo. Paprastai klientai reikalauja konkretaus paketo, kai jie vėl užsako anksčiau įsigytus produktus. Šio tipo paketui būdingas rezervavimas nurodytas kaip *įvykdyto užsakymo rezervavimas*.

Šis taisyklių rinkinys galioja, kai apdorojami kiekiai, o paketo numeris yra vykdomas konkrečiam užsakymui:

- Tam, kad būtų galima rezervuoti konkretų prekės paketo numerį, esantį *Paketas žemiau\[vietos\]* rezervavimo strategijoje, sistema turi rezervuoti visas dimensijas naudojant vietą. Šiame intervale paprastai būna numerio lentelės dimensija.
- Vietos nurodymai nenaudojami, kai kuriami išrinkimo darbai, skirti pardavimo eilutei, kuriai naudojama įvykdyto užsakymo paketo rezervacija.
- Sandėlio darbo, skirto įvykdytų užsakymų paketams, apdorojimo metu, nei vartotojui, nei sistemai neleidžiama keisti paketo numerio. (Šis apdorojimas apima išimčių tvarkymą.)

Toliau pateiktame pavyzdyje parodytas visapusis srautas.

## <a name="example-scenario-batch-number-allocation"></a>Pavyzdinis scenarijus: Paketo numerio priskyrimas

Šiam pavyzdžiui turite įdiegti demonstracinius duomenis ir naudoti **USMF** demonstracinių duomenų įmonę.

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a>Atsargų rezervavimo hierarchijos nustatymas leisti paketui būdingą rezervaciją

1. Eiti į **Sandėlio valdymas** \> **Sąranka** \> **Atsargos \> Rezervavimo hierarchija**.
2. Pasirinkite **Naujas**.
3. Lauke **Pavadinimas** įveskite pavadinimą (pavyzdžiui, **BatchFlex**).
4. Lauke **Aprašas** įveskite aprašą (pvz., **Mažiau dinamiškas paketas**).
5. Lauke **Pasirinkta** pažymėkite **Serijos numeris** ir **Savininkas**, tada pasirinkite kairiosios rodyklės mygtuką, kad perkeltumėte juos į lauką **Pasiekiama**.
6. Pasirinkite **Gerai**.
7. Dimensijos lygio **Paketo numeris** eilutėje pažymėkite žymės langelį **Leisti rezervuoti užsakymą pagal poreikį**. Lygiai **Numerio lentelė** ir **Vieta** parenkami automatiškai, tad jūs negalite išvalyti jų žymės langelių.
8. Pasirinkite **Įrašyti**.

### <a name="create-a-new-released-product"></a>Kurti naują išleistą produktą

1. Nustatykite tris bendrųjų produkto duomenų parametrus naudodami šias vertes:

    - Lauke **Saugojimo dimensijų grupė** pasirinkite **Sand**.
    - Lauke **Saugojimo dimensijų grupė** pasirinkite **Pak. fakt**.
    - Lauke **Rezervavimo hierarchija** pasirinkite **BatchFlex**.

2. Sukurkite du paketo numerius, pvz., **B11** ir **B22**.
3. Įtraukite prekių kiekius į turimas atsargas, naudodami šias vertes.

    | Sandėlis | Paketo numeris | Vieta | Numerio lentelė | Kiekis |
    |-----------|--------------|----------|---------------|----------|
    | 24        | B11          | BULK-001 | Jokia          | 10       |
    | 24        | B11          | FL-001   | LP11          | 10       |
    | 24        | B22          | FL-002   | LP22          | 10       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a>Pardavimo užsakymo išsamios informacijos įvedimas

1. Eikite į **Pardavimas ir rinkodara** \> **Pardavimo užsakymai** \> **Visi pardavimo užsakymai**.
2. Pasirinkite **Naujas**.
3. Pardavimo užsakymo antraštėje, lauke **Kliento sąskaita** įveskite **JAV-003**.
4. Pridėkite naujos prekės eilutę ir kaip kiekį įveskite **10**. Įsitikinkite, kad laukas **Sandėlis** nustatytas į **24**.
5. „FastTab“ **Pardavimo užsakymo eilutės** pasirinkite **Atsargos**, tada grupėje **Tvarkyti** pasirinkite **Paketo rezervavimas**. Puslapyje **Paketo rezervavimas** rodomas paketų, kuriuos galima rezervuoti užsakymo eilutėje, sąrašas. Šiame pavyzdyje rodomas kiekis **20** paketo numeriui **B11** ir kiekis **10** paketo numeriui **B22**. Atkreipkite dėmesį, kad puslapio **Paketo rezervavimas** negalima pasiekti naudojant eilutę, jei tos eilutės prekė susieta su *Paketas žemiau\[vietos\]* rezervavimo hierarchija, nebent ji nustatyta taip, kad leistų atlikti paketui būdingą rezervavimą.

    > [!NOTE]
    > Norėdami rezervuoti konkretų pardavimo užsakymo paketą, turite naudoti puslapį **Paketo rezervavimas**.
    >
    > Jei paketo numerį įvesite tiesiai į pardavimo užsakymo eilutę, sistema veiks taip, lyg būtumėte įvedę konkrečią prekės, kuriai taikoma *Paketas žemiau\[vietos\]* rezervavimo strategija, paketo reikšmę. Įrašius eilutę, bus parodytas įspėjamasis pranešimas. Jei patvirtinate, kad paketo numeris turi būti nurodytas tiesiogiai užsakymo eilutėje, eilutė nebus apdorota naudojant įprastą sandėlio valdymo logiką.
    >
    > Jei rezervuosite kiekį iš puslapio **Rezervavimas**, nebus rezervuotas joks konkretus paketas, o eilutės sandėlio operacijų vykdymas vadovausis taisyklėmis, kurios taikomos *Paketas žemiau\[vietos\]* rezervavimo strategijoje.

    Apskritai, šis puslapis veikia ir sąveikauja taip pat, kaip ir su prekėmis, kurios turi susietą *Paketas aukščiau\[vietos\]* tipo rezervavimo hierarchiją. Tačiau taikomos šios išimtys:

    - „FastTab“**Paketo numeriai, įvykdyti šaltinio eilutei** nurodo paketo numerius, kurie rezervuoti užsakymo eilutei. Paketinės vertės tinklelyje bus rodomos viso užsakymo eilutės ciklo vykdymo metu, įskaitant sandėliavimo apdorojimo etapus. Priešingai, „FastTab“ **Peržiūra** įprastas užsakymo eilutės rezervavimas (t. y. rezervavimas, kuris atliekamas virš **vietos** lygio dimensijų) rodomas tinklelyje iki vietos, kai sukuriamas sandėlio darbas. Tada darbo objektas perima eilutės rezervavimą, o eilutės rezervavimas puslapyje nebebus rodomas. „FastTab“ **Paketo numeriai, vykdomi šaltinio eilutei** padeda užtikrinti, kad pardavimo užsakymo procesorius galėtų peržiūrėti paketo numerius, kurie buvo įvykdyti kliento užsakymui, bet kada ciklo metu iki sąskaitos faktūros išrašymo.
    - Be to, kad būtų galima rezervuoti tam tikrą paketą, vartotojas gali rankiniu būdu pasirinkti konkrečią paketo vietą ir numerio lentelę, užuot leidęs sistemai automatiškai jas parinkti. Ši charakteristika susijusi su įvykdyto užsakymo paketo rezervavimo mechanizmo dizaino įrankiu. Kaip jau minėta, kai paketo numeris rezervuojamas prekei, esančiai *Paketas žemiau\[vietos\]* rezervavimo strategijoje, sistema turi rezervuoti visas dimensijas naudojant vietą. Todėl sandėlio darbas bus atliekamas tose pačiose saugojimo dimensijose, kurias rezervavo vartotojai, dirbę su užsakymais, ir ne visada gali nurodyti prekių saugojimo vietą, kuri yra patogi arba netgi įmanoma,kalbant apie išrinkimo operacijas. Jei užsakymo vykdytojai žino apie sandėlio apribojimus, jie gali norėti neautomatiniu būdu pasirinkti konkrečias vietas ir numerio lenteles, kai jie rezervuoja paketą. Šiuo atveju vartotojas turi naudoti funkcijas **Rodyti dimensijas** puslapio antraštėje ir įtraukti vietą bei numerio lentelę į tinklelį, esantį „FastTab“ **Peržiūra**.

6. Puslapyje **Paketo rezervavimas** pasirinkite paketo eilutę **B11** ir pažymėkite **Rezervuoti eilutę**. Nėra skirtosios logikos vietų ir numerio lentelių priskyrimo automatiniam rezervavimui. Kiekį galite įvesti rankiniu būdu į lauką **Rezervavimas**. Atkreipkite dėmesį, kad „FastTab“ **Paketo numeriai, įvykdyti šaltinio eilutei** paketas **B11** rodomas kaip **Įvykdyta**.

    ![Konkretaus paketo numerio vykdymas pardavimo užsakymo eilutei paketo rezervavimo puslapyje.](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > Pardavimo užsakymo eilutėje nurodytas kiekis gali būti rezervuojamas per kelis paketus. Taip pat galite to pačio paketo rezervavimą galima atlikti keliose vietose ir numerio lentelėse (jei yra įjungtos vietų numerio lentelės).
    >
    > Pardavimo užsakymo eilutėje esančio kiekio konkretaus paketo rezervavimas taip pat gali būti dalinis. Pavyzdžiui, visas 100 vienetų kiekis gali būti rezervuojamas tam, kad konkretus paketas būtų vykdomas 20 vnt., o 80 vienetų būtų rezervuota bet kurio turimo paketo vietoje ir sandėlio lygiuose. Šiuo atveju WMS atliks išrinkimų operacijas, naudodama dvi atskiras darbo eilutes.

7. Eikite į **Produkto informacijos valdymas** \> **Produktai** \> **Patvirtinti produktai**. Pažymėkite prekę ir pasirinkite **Tvarkyti atsargas** \> **Rodinys** \> **Operacijos**.

    ![Įvykdyto užsakymo rezervavimas kaip atsargų operacijų tipas.](media/Inventory-transactions-for-order-committed-reservation.png)

8. Peržiūrėkite prekės atsargų operacijas, susijusias su pardavimo užsakymo eilutės rezervavimu.

    - Operacija, kai laukas **Nuoroda** nustatytas kaip **Pardavimo užsakymas**, o laukas **Išduoti** yra nustatytas kaip **Rezervuota faktiškai** nurodo atsargų dimensijų, esančių virš lygio **Vieta**, užsakymo eilutės rezervavimą. Pagal prekės atsargų rezervavimo hierarchiją tos dimensijos yra vieta, sandėlis ir atsargų būsena.
    - Operacija, kai laukas **Nuoroda** nustatytas kaip **Įvykdyto užsakymo rezervavimas**, o laukas **Išduoti** yra nustatytas kaip **Rezervuota faktiškai** nurodo konkretaus paketo ir virš jo esančių visų atsargų dimensijų užsakymo eilutės rezervavimą. Pagal prekės atsargų rezervavimo hierarchiją tos dimensijos yra paketo numeris ir vieta. Šiame pavyzdyje vieta yra **Bulk-001**.

9. Pardavimo užsakymo antraštėje pasirinkite **Sandėlis** \> **Veiksmai** \> **Išleisti į sandėlį**. Užsakymo eilutė dabar yra banguota, ir sukuriami apkrovos ir darbai.

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a>Sandėlio darbo su įvykdyto užsakymo paketo numeriai peržiūra ir apdorojimas

1. „FastTab“ **Pardavimo užsakymo eilutės** pasirinkite **Sandėlis** \> **Darbo informacija**.

    Darbas, kuris tvarko paketo kiekio, kuris yra skirtas pardavimo užsakymo eilutei, išrinkimo operaciją, pasižymi šiomis savybėmis:

    - Kad sukurtų darbą, sistema naudoja darbo šablonus, o ne vietos nuorodas. Visi įprasti parametrai, apibrėžti darbo šablonams, pvz., maksimalus paėmimo eilučių skaičius arba konkretus matavimo vienetas, bus taikomi siekiant nustatyti, kada turi būti sukurtas naujas darbas. Tačiau į taisykles, kurios susietos su vietos nurodymais identifikuojant paėmimo vietas, nėra atsižvelgiama, nes įvykdyto užsakymo rezervavimu jau nurodoma visų atsargų dimensijos. Tose atsargų dimensijose yra dimensijų sandėlio sandėliavimo lygyje. Todėl darbas perima šias dimensijas ir nereikia vadovautis vietos nurodymais.
    - Paketo numeris nerodomas paėmimo eilutėje (kaip tai yra su darbo eilute, sukurta prekei, kuri yra susieta su *Paketas žemiau\[vietos\]* rezervavimo hierarchija). Vietoj to, paketo numeris „nuo“ ir visos kitos saugojimo dimensijos yra rodomi darbo eilutės darbo atsargų operacijoje, kuri nurodoma iš susietų atsargų operacijų.

        ![Sandėlio atsargų operacija darbui, kuris yra iš įvykdyto užsakymo rezervavimo.](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - Sukūrus darbą, prekės atsargų operacija, kai laukas **Nuoroda** nustatytas kaip **Įvykdyto užsakymo rezervavimas**, pašalinama. Atsargų operacija, kai laukas **Nuoroda** kaip **Darbas**, dabar turi faktinį rezervavimą visose kiekio atsargų dimensijose.

        Sandėlio operacijos gali tęsti darbo vykdymo tvarkymą įprastu būdu. Tačiau mobiliojo įrenginio instrukcijose bus nurodyta, kad darbuotojas galės pasirinkti konkretų paketo numerį. Sandėlio aplinkose, kuriose vietos yra kontroliuojamos pagal numerio lentelę, darbuotojui pasiekus vietą, saugančią tą patį paketą keliose numerio lentelėse, jis gali išsirinkti bet kurią numerio lentelę, kuri dar nerezervuota (pavyzdžiui, kitu įvykdyto užsakymo rezervavimu arba darbu, kilusiu iš šio tipo rezervavimo.)

        Jei paaiškėja, kad nepraktiška paimti iš vietos, nurodytos darbo eilutėje, sandėlio operatoriai gali naudoti vieną iš toliau nurodytų veiksmų, kad nukreiptų konkretaus paketo paėmimą iš patogesnės vietos:

        - Įprastas veiksmas **Nepaisyti vietos** mobiliajame įrenginyje (jei sandėlio darbuotojo parametras **Leisti nepaisyti paėmimo vietos** įjungtas)
        - Veiksmas **Keisti vietą** puslapyje **Darbų sąrašo informacija**. 

2. Mobiliajame įrenginyje baikite paėmimo ir dėjimo darbą.

    Kiekis **10**, skirtas paketo numeriui **B11**, dabar paimamas pardavimo užsakymo eilutei ir padedamas į vietą **Galinės durys**. Šiuo metu, jis paruoštas būti pakrautas į sunkvežimį ir išsiųstas kliento adresu.

## <a name="flexible-license-plate-reservation"></a>Lanksti licencijos numerio rezervacija

### <a name="business-scenario"></a>Verslo scenarijus

Šiame scenarijuje bendrovė naudoja sandėlio tvarkymą ir darbo apdorojimą bei tvarko krovimo planavimą individualių padėklų ar konteinerių lygmeniu, ne „Supply Chain Management“ prieš sukuriant darbą. Šie konteineriai yra rodomi licencijos numeriuose inventoriaus dimensijose. Dėl to, šiai prieigai specialūs licencijos numeriai turi būti paskirti iš anksto prie prekybos užsakymo linijų prieš paėmimo darbo pabaigą. Bendrovė ieško lankstumo taip, kad licencijos numerio rezervavimo taisyklės būtų sutvarkytos ir atsitiktų tokia įvykių seka:

- Licencijos numeris gali būti įrašytas ir rezervuotas, kai užsakymas yra paimtas prekybos apdorojimo ir jo paimti negali kiti poreikio prašytojai. Toks elgesys padeda užtikrinti, kad suplanuotas licencijos numeris yra išsiųstas klientui.
- Jei licencijos numeris dar nėra priskirtas prekybos užsakymo eilutei, sandėlio personalas gali pasirinkti licencijos numerį paėmimo darbo metu po prekybos užsakymo registravimo ir rezervacija yra baigta.

### <a name="turn-on-flexible-license-plate-reservation"></a>Įjungti lanksčią licencijos numerio rezervaciją

Prieš tai, kai galite naudoti lanksčią licencijos numerio rezervaciją, dvi funkcijos jūsų sistemoje turi būti įjungtos. Administratoriai gali naudoti [funkcijos valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus tam, kad patikrintų funkcijų būseną ir įjungtų jas, jei to reikia. Turite įjungti funkcijas šiame užsakyme:

1. **Funkcijos pavadinimas:** *Lanksti sandėlio dimensijų rezervavimo strategija*
1. **Funkcijos pavadinimas** *Su užsakymo susieto licencijos numerio lankstus rezervavimas*

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a>Rezervuoti specifinį licencijos numerį prekybos užsakyme

Tam, kad leistumėte licencijos numerio rezervavimą užsakyme, turite pasirinkti **Leisti rezervavimą pagal poreikio užsakymą** pažymimame laukelyje **Licencijos numerio** lygyje esančiame **Inventoriaus rezervavimo hierarchijos** puslapyje hierarchijai, kuri yra susieta su atitinkamu elementu.

![Inventoriaus rezervavimo hierarchijos puslapyje lanksčiai licencijos numerio rezervavimo hierarchijai.](media/Flexible-LP-reservation-hierarchy.png)

Galite įjungti licencijos numerio rezervaciją užsakyme bet kuriuo metu savo diegime. Šis pakeitimas nepakeis jokio rezervavimo ar neatidarys sandėlio užduotį, kuri buvo sukurta prieš atliekant pakeitimą. Nepaisant to, negalite pašalinti **Leisti rezervaciją pagal prašomą užsakymą** žymimo laukelio, jei vienam ar keliems susietiems su rezervacijos hierarchija elementams egzistuoja atviros išorės inventoriaus perlaidos *Užsakyme*, *Rezervuotame užsakyme* ar *Fiziškai rezervuotame*.

Net jei **Leisti rezervaciją pagal prašymo užsakymą** žymimas laukelis yra pasirinktas **Licencijos numerio** lygyje, dar galima *nerezervuoti* specialaus licencijos numerio užsakyme. Tokiu atveju, taikoma numatyta sandėlio operacijų logika, galiojanti rezervavimo hierarchijai.

Norėdami rezervuoti konkrečią numerio lentelę, turite naudoti [Atvirojo duomenų protokolo („OData”)](../../fin-ops-core/dev-itpro/data-entities/odata.md) procesą. Programoje šią rezervaciją galite atlikti tiesiai iš pardavimo užsakymo naudodami parinktį **Užsakymams ištikimos rezervacijos numerio lentelei** komandoje **Atidaryti „Excel” programoje**. „Excel“ priede atidarytuose objekto duomenyse turite įvesti toliau pateiktus su rezervacija susijusius duomenis ir tuomet pasirinkti **Viešinti** tam, kad siųstumėte duomenis atgal į „Supply Chain Management“:

- Nuoroda (Tik *Prekybos užsakymo* vertė yra palaikoma.)
- Prekybos numeris (Vertė gali būti išvesta iš vietos.)
- Partijos numeris
- Numerio lentelė
- Kiekis

Jei turite rezervuoti specialų licencijos numerį paketo sekamam elementui, naudokite **Paketo rezervavimo** puslapį, kaip aprašyta [Įvesti prekybos užsakymo informaciją](#sales-order-details) skyriuje.

Kai prekybos užsakymo eilutė naudoja su užsakymu susietą licencijos numerio rezervavimą apdorotą sandėlio operacijų, vietos nuorodos nėra naudojamos.

Jei sandėlio užduoties elementą sudaro eilutės, kurios atitinka visą padėklą ir turi su licencijos ženklu susijusius kiekius, galite optimizuoti paėmimo procesą naudodami mobilaus prietaiso meniu elementą, kuriame **Valdoma licencijos numeriu** parinktis nustatyta į *Taip*. Sandėlio darbuotojas gali tuomet nuskaityti licencijos numerį tam, kad pabaigtų paėmimą, o ne nuskaitytų elementus užduotyje po vieną.

![Mobiliojo įrenginio meniu elementas, kuriame tvarkymo pagal licencijos numerį parinktis yra nustatyta į Taip.](media/Handle-by-LP-menu-item.png)

Kadangi **Tvarkyti pagal licencijos numerį** funkcija nepalaiko darbo, kuris apima keletą padėklų, geriau turėti atskirą užduoties elementą skirtingiems licencijos numeriams. Šios prieigos naudojimui, įtraukite **Su užsakymu susijusio licencijos numerio ID** laukelį, kaip užduoties antraštės tarpą **Darbo šablono** puslapyje.

> [!NOTE]
> Pasirinkus su užsakymu susijusį darbo kūrimo procesą, paėmimo užduoties eilutėms bus priskirta „su užsakymu susijusių atsargų dimensijos“ reikšmė ir nebus galima tiesiogiai peržiūrėti licencijos numerio reikšmės. Konfigūruojant mobiliojo įrenginio menių elementą, palaikomas tik *Vartotojo nurodytas* procesas.

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a>Pavyzdinis scenarijus: Nustatyti ir apdoroti su užsakymo susieto licencijos numerio lankstus rezervavimą

Šis scenarijus parodo, kaip nustatyti ir apdoroti su užsakymo susieto licencijos numerio lankstus rezervavimą.

### <a name="make-demo-data-available"></a>Demonstracinių duomenų įgalinimas

Šis scenarijus aprašo vertes ir įrašus, kurie yra įtraukti į standartinius demonstracinius duomenis pateiktus „Supply Chain Management“. Jei norite dirbti su scenarijumi naudojant čia pateiktas vertes, įsitikinkite, kad dirbate su aplinka, kurioje įdiegti demonstraciniai duomenys. Taip pat, nustatykite teisinį subjektą į **USMF** prieš pradėdami.

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a>Sukurkite inventoriaus rezervavimo hierarchiją, kuri leidžia licencijos numerio rezervavimą

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Inventorius \> Hierarchijos rezervavimas**.
1. Pasirinkite **Naujas**.
1. **Pavadinimas** laukelyje, įveskite vertę (pavyzdžiui, *Lankstus LP*).
1. **Aprašas** laukelyje, įveskite vertę (pavyzdžiui, *Lankstus LP rezervavimas*).
1. **Pasirinkti** sąraše pasirinkite **Paketo numeris**, **Serijinis numeris** ir **Savininkas**.
1. Pasirinkite **Pašalinti** mygtuką ![rodyklė atgal.](media/backward-button.png) pasirinktų laukų perkėlimui į **Galimi** sąrašą.
1. Pasirinkite **Gerai**.
1. **Licencijos numeris** dimensijos lygio eilutėje, pasirinkite **Leisti rezervavimą pagal norimą užsakymą** pažymimą laukelį. **Vietos** lygis automatiškai pasirenkamas ir jūs negalite pašalinti žymimo laukelio.
1. Pasirinkite **Įrašyti**.

### <a name="create-two-released-products"></a>Sukurti du išleistus produktus

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. **Naujas išleistas produktas** teksto laukelyje, pasirinkite šias vertes:

    - **Produkto numeris:** *Elementas1*
    - **Elemento numeris:** *Elementas1*
    - **Prekių modelių grupė:** *FIFO*
    - **Prekių modelių grupė:** *Garso*
    - **Saugojimo dimensijos grupė:** *Sandėlis*
    - **Sekimo dimensijos grupė:** *Nėra*
    - **Rezervavimo hierarchija** *LankstusLP*

1. Pasirinkite **Gerai** tam, kad sukurtumėte produktą ir uždarytumėte teksto laukelį.
1. Atidaromas naujas produktas. **Sandėlio** „FastTab“, nustatykite **Vieneto sekos grupės ID** laukelį į *ea*.
1. Pakartokite ankstesnius žingsnius tam, kad sukurtumėte antrą produktą su tokiais pačiais parametrais, bet nustatykite **Produkto numerio** ir **Elemento numerio** laukelius į *Item2*.
1. Veiksmų juostoje, **Inventoriaus valdymas** skirtuke, **Peržiūros** grupėje pasirinkite **Turimas inventorius**. Tada pasirinkite **Kokybės tvarkymas**.
1. Tvarkykite turimą naujų elementų inventorių, kaip nurodyta tolesnėje lentelėje.

    | Produktas  | Sandėlis | Buvimo vieta | Numerio lentelė | Kiekis |
    |-------|-----------|----------|---------------|----------|
    | 1 elementas | 24        | FL-010   | LP01          | 10       |
    | 1 elementas | 24        | FL-011   | LP02          | 10       |
    | 2 elementas | 24        | FL-010   | LP01          | 5        |
    | 2 elementas | 24        | FL-011   | LP02          | 5        |

    > [!NOTE]
    > Privalote sukurti du licencijų numerius ir naudoti vietas, kurios leidžia maišytus elementus, tokius kaip *FL-010* ir *FL-011*.

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a>Sukurkite prekybos užsakymą ir rezervuokite specialų licencijos numerį

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Pasirinkite **Naujas**.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - **Kliento sąskaita:** *US-001*
    - **Sandėlis:** *24*

1. Pasirinkite **Gerai** tam, kad uždarytumėte **Sukurti prekybos užsakymą** teksto laukelį ir atidarytumėte naują prekybos užsakymą.
1. **Prekybos užsakymai** „FastTab“, įtraukite eilutę, kuri turi šiuos nustatymus:

    - **Elemento numeris:** *Elementas1*
    - **Kiekis:** *10*

1. Įtraukite antrą prekybos užsakymo eilutę, kuri turėtų šiuos parametrus:

    - **Elemento numeris:** *Elementas2*
    - **Kiekis:** *5*

1. Pasirinkite **Įrašyti**.
1. **Eilutės išsamios informacijos** „FastTab“, **Parametrų** skirtuke pažymėkite **Vietos ID** vertę kiekvienai eilutei. Šių verčių reikės specialių licencijų numerių rezervavimo metu.

    > [!NOTE]
    > Specialaus licencijos numerio rezervavimui, privalote naudoti **Su užsakymu susijusių rezervavimų licencijos numerio** duomenų objektą. Jei turite rezervuoti specialų licencijos numerį paketo sekamam elementui, naudokite **Paketo rezervavimo** puslapį, kaip aprašyta [Įvesti prekybos užsakymo informaciją](#sales-order-details) skyriuje.
    >
    > Jei įvedate licencijos ženklą tiesiai prekybos užsakymo eilutėje ir patvirtinate jį sistemoje, sandėlio valdymo apdorojimas nebebus naudojamas eilutėje.

1. Pasirinkite **Atidaryti „Microsoft Office“**, pasirinkite **Su užsakymu susijusios rezervacijos licencijos numeriui** ir atsisiųskite failą
1. Atidarykite atsisiųstą failą „Excel“ ir pasirinkite **Įjungti redagavimą** tam, kad įjungtumėte „Excel“ priedus vykdymui.
1. Jei „Excel“ papildinį paleisite pirmą kartą, pasirinkite **Pasitikėti šiuo papildiniu**.
1. Jei būsite paskatinti prisijungti, pasirinkite **Prisijungti** ir tuomet prisijunkite tais pačiais prisijungimo vardais, kuriuos naudojote prisijungti prie „Supply Chain Management“.
1. Elemento rezervavimui konkrečiame licencijos ženkle, „Excel“ prieduose pasirinkite **Naujas** tam, kad įtrauktumėte rezervacijos eilutę ir tuomet nustatykite šias vertes:

    - **Vietos ID:** Įveskite **Vietos ID** vertę, kurią rasite prekybos užsakymo eilutėje *Elementas 1*.
    - **Numerio lentelė:** *LP02*
    - **Atsargų kiekių rezervavimas:** *10*

1. Pasirinkite **Naujas** tam, kad įtrauktumėte rezervavimo eilutę ir tuomet nustatykite šias vertes:

    - **Vietos ID:** Įveskite **Vietos ID** vertę, kurią rasite prekybos užsakymo eilutėje *Elementas 2*.
    - **Numerio lentelė:** *LP02*
    - **Atsargų kiekių rezervavimas:** *5*

1. „Excel“ prieduose pasirinkite **Publikuoti** tam, kad siųstumėte duomenis atgal į „Supply Chain Management“.

    > [!NOTE]
    > Rezervavimo eilutė pasirodys sistemoje tik jei publikavimas bus baigtas be klaidų.

1. Eikite atgal į „Supply Chain Management“. 
1. Tam, kad peržiūrėtumėte elemento rezervavimą,**Prekybos užsakymo eilutės** „FastTab“, **Inventoriaus** meniu, pasirinkite **Palaikymas \> Rezervavimas**. Atkreipkite dėmesį, kad prekybos užsakymo eilutė *Elementui 1*, inventoriaus *10* yra rezervuota ir prekybos užsakymo eilutė *Elementui2*, *5* inventoriaus yra rezervuota.
1. Tam, kad peržiūrėtumėte inventoriaus perlaidas, kurios yra susijusios su prekybos užsakymo eilutės rezervavimu, **Prekybos užsakymo eilutės** „FastTab“, **Inventoriaus** meniu, pasirinkite **Peržiūra \> Perlaidos**. Atkreipkite dėmesį, kad esama dviejų perlaidų, kurios yra susijusios su rezervacija: viena, kai **Nuorodos** laukelis yra nustatytas į *Prekybos užsakymas* ir kita, kai **Nuorodos** laukelis yra nustatytas *Užsakymui įsipareigojusi rezervacija*.

    > [!NOTE]
    > Perlaida, kai **Nuorodos** laukelis yra nustatytas į *Prekybos užsakymą* rodo užsakymo eilutę rezervavimui inventoriaus dimensijoms, kurios prieš tai yra **Vietos** lygyje (saitas, sandėlis ir inventoriaus būsena). Perlaida, kai **Nuorodos** laukelis yra nustatytas į *Užsakymui įsipareigojusi rezervacija* rodo užsakymo eilutės rezervaciją konkrečiam licencijos numeriui ir vietai.

1. Tam, kad paleistumėte prekybos užsakymą, veiksmų juostoje **Sandėlis** skirtuke, **Veiksmų** grupėje, pasirinkite **Paleisti į sandėlį**.

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a>Peržiūrėti ir apdoroti sandėlio užduotį su užsakymui įsipareigojusiu priskirtu licencijos numeriu

1. **Prekybos užsakymo eilutės** „FastTab“,**Sandėlis** meniu, pasirinkite **Darbo informacija**.

    Kai rezervacija yra atlikta konkrečiam paketui, sistema nenaudoja vietos direktyvų, kai sukuria užduotį prekybos užsakymui, naudojančiam licencijos numerio rezervaciją. Kadangi užsakymui įsipareigojusi rezervacija nurodo visas inventoriaus dimensijas, įskaitant vietą, vietos direktyvos neturi būti naudojamos, nes tos inventoriaus dimensijos ką tik pateko į užduotį. Jos yra rodomos **Inventoriaus dimensijų suformavimas** skyriuje **Darbo inventoriaus perlaidos** puslapyje.

    > [!NOTE]
    > Po to, kai darbas yra sukurtas, elemento inventoriaus perlaida, kuroje **Nuorodos** laukelis yra nustatytas į *Užsakymui įsipareigojusi rezervacija* yra pašalinamas. Inventoriaus perlaida, kai **Nuorodos** laukelis yra nustatytas į *Darbą* dabar turi fizinį rezervavimą visoms inventoriaus kiekio dimensijoms.

1. Mobiliame prietaise, pabaikite paėmimo ir padėjimo užduotį naudodami meniu elementą, kuriame **Tvarkymas pagal licencijos numerį** laukelis yra pasirinktas.

    > [!NOTE]
    > **Tvarkyti pagal licencijos numerį** funkcija padeda jums apdoroti visą licencijos numerį. Jei turite apdoroti dalį licencijos numerio, negalite naudoti šios funkcijos.
    >
    > Rekomenduojame jums atskirti darbą sukurtą kiekvienam licencijos numeriui. Tam, kad pasiektumėte šį rezultatą, naudokite **Darbo antraštės pertraukas** funkciją **Darbo šablonai** puslapyje.

    Licencijos ženklas *LP02* dabar yra paimamas prekybos užsakymo eilutėms ir padedamas į *Baydoor* vietą. Šiuo metu, pasirengta pakrovimui ir išsiuntimui klientui.

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a>Sandėlio darbo išimčių tvarkymas su įvykdyto užsakymo paketo numeriais

Sandėlio darbas, skirtas paimti įvykdyto užsakymo paketo numerius, yra vykdomas su tuo pačiu standartiniu sandėlio išimties apdorojimu i veiksmais, kaip ir įprastas darbas. Paprastai atidarytą darbą arba darbo eilutę galima atšaukti, juos galima pertraukti, nes vartotojo vieta pilna, juos galima trumpai paimti, ir juos galima naujinti dėl perkėlimo. Taip pat gali būti sumažintas jau atlikto darbo paimtas kiekis, arba darbas gali būti atšauktas.

Ši pagrindinė taisyklė taikoma visiems šiems išimties tvarkymo veiksmams: klientui rezervuotas paketo numeris negali būti pakeistas kitu paketo numeriu, bet jo saugojimo dimensijos (vieta ir numerio lentelė) gali būti pakeistos arba vartotojui rankiniu būdu atnaujinant arba sistemai automatiškai atnaujinant. Automatinis naujinimas paremtas tuo pačiu atsitiktiniu sandėliavimo dimensijų priskyrimu, kuris taikomas, kai konkretus paketas buvo rezervuotas automatiškai, tačiau nenurodytos sandėliavimo dimensijos.

### <a name="example-scenario"></a>Pavyzdinis scenarijus

Šio scenarijaus pavyzdys yra atvejis, kai anksčiau baigtas darbas yra nepaimtas naudojant funkciją **Mažinti paimtą kiekį**. Šis pavyzdys apima tai, kad jūs jau pabaigėte žingsnius aprašytus [Pavyzdiniame scenarijuje: Paketo numerio priskyrimas](#Example-batch-allocation). Jis tęsiasi iš šio pavyzdžio.

1. Eikite į **Sandėlio valdymas** \> **Kroviniai** \> **Aktyvūs kroviniai**.
2. Pasirinkite krovinį, kuris buvo sukurtas siejant su pardavimo užsakymo siunta.
3. Iš „FastTab“ **Krovinio užsakymo eilutės** pasirinkite **Mažinti paimtą kiekį**.
4. Puslapyje **Mažinti paimtą kiekį** lauke **Perkelti į vietą** pasirinkite **FL-001**.
5. Lauke **Perkelti į numerio lentelę** pasirinkite **LP33**.
6. Tinklelyje į lauką **Atsargų kiekis, kurio paėmimo reikia atsisakyti** įveskite **10**.
7. Pasirinkite **Gerai**.

Čia pateikiami paėmimo atsisakymo veiksmo rezultatai:

- Anksčiau uždaryto darbo būsena nustatyta kaip **Atšaukta**.
- Tipo **Atsargų perkėlimas** naujas darbas sukuriamas nepaimtam kiekiui **10** paketo numeriui **B11**. Šis darbas vaizduoja perkėlimą iš vietos **Galinės durys** į numerio lentelę **LP33** vietoje **FL-001**. Būseną nustatyta kaip **Uždaryta**.
- Sistema iš naujo rezervuoja iš pradžių užsakytą paketo numerį ir priskiria vietos ir valstybinio numerio ID. (Šis procesas prilygsta nurodyto paketo numerio užsakymo eilutės funkcijai **Rezervuoti eilutę**). Todėl paketas **B11** rodomas, kaip įvykdytas „FastTab“ **Paketo numeriai, įvykdyti šaltinio eilutei**, puslapyje **Paketo rezervavimas** ir lauke **Rezervavimas** nurodytas kiekis **10**, skirto paketo numeriui **B11**. Be to, laukas **Vieta** nustatytas kaip **FL-001**, o laukas **Numerio lentelė** nustatytas kaip **LP11**. (Jei jų nematote, šiuos laukus galima įtraukti į tinklelį.)

Toliau esančiose lentelėse pateikiama apžvalga, nurodanti, kaip sistema apdoroja konkrečių sandėlio veiksmų įvykdyto užsakymo paketo rezervavimą. Norėdami suprasti lentelių turinį, Įsivaizduokite, kad kiekvienas sandėlio veiksmas yra vykdomas esamo sandėlio darbo, kilusio iš įvykdyto užsakymo paketo rezervavimo, kontekste, ar kiekvieno sandėlio veiksmo vykdymas turi įtakos to tipo darbui.

> [!NOTE]
> Šiose lentelėse stulpelyje „Paketo kiekis pasiekiamas“ rodoma, ar yra pasiekiamas paketo kiekis, be kiekio, kuris jau rezervuotas dabartiniam įvykdyto užsakymo rezervavimams, arba jau rezervuotas pagal sandėlio darbą, kuris gaunamas iš to tipo rezervavimų.

#### <a name="override-the-pick-location-on-the-open-work"></a>Paėmimo vietos perrašymas atidarytame darbe

<table>
<thead>
<tr>
<th>Pagrindinis sąrankos parametras</th>
<th>Paketo kiekis pasiekiamas</th>
<th>Pagrindiniai vartotojo veiksmai</th>
<th>Sandėlio darbas</th>
<th>Įvykdyto užsakymo paketo rezervavimas</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Parinktis <strong>Leisti keisti paėmimo vietą</strong> darbininkui yra įjungta.</td>
<td>Taip</td>
<td>
<ol>
<li>Pasirinkite <strong>Keisti vietą</strong> meniu elementą, esantį sandėlio programos mobiliųjų įrenginių programėlėje, kai pradedate paėmimo darbą.</li>
<li>Pasirinkite <strong>Siūlyti</strong>.</li>
<li>Patvirtinkite naują vietą, kuri siūloma pagal paketo kiekio pasiekiamumą.</li>
</ol>
</td>
<td>Dabartiniam darbui atsiranda šie veiksmai:
<ul>
<li>Vieta paėmimo eilutėje atnaujinama į naują vietą. (Jei vieta yra kontroliuojama pagal numerio lentelę, atsitiktinė numerio lentelė priskiriama darbo atsargų operacijai, o darbuotojas gali rinktis iš bet kurios turimos numerio lentelės, kurios kiekis yra pasiekiamas.)</li>
<li>Jei naujoje vietoje yra daugiau nei viena numerio lentelė, pradinė paėmimo eilutė padalijama į kelias eilutes, kad atitiktų kiekvieną numerio lentelę.</li>
</ul>
</td>
<td>Netaikoma</td>
</tr>
<tr>
<td>Ne</td>
<td>
<ol>
<li>Pasirinkite <strong>Keisti vietą</strong> meniu elementą, esantį sandėlio programos mobiliųjų įrenginių programėlėje, kai pradedate paėmimo darbą.</li>
<li>Įveskite vietą rankiniu būdu.</li>
</ol>
</td>
<td>Veiksmas <strong>Nepaisyti vietos</strong> nėra galimas. Jis nepavyksta ir rodoma klaida.</td>
<td>Netaikoma</td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a>Visas mygtukas – skaidykite darbo eilutę dėl perpildos vartotojo vietoje

<table>
<thead>
<tr>
<th>Pagrindinis sąrankos parametras</th>
<th>Paketo kiekis pasiekiamas</th>
<th>Pagrindiniai vartotojo veiksmai</th>
<th>Sandėlio darbas</th>
<th>Įvykdyto užsakymo paketo rezervavimas</th>
</tr>
</thead>
<tbody>
<tr>
<td>Parinktis <strong>Leisti skaidyti darbą</strong> įjungta mobiliojo įrenginio meniu elemente.</td>
<td>Netaikoma</td>
<td>
<ol>
<li>Pasirinkite <strong>Visas</strong> meniu elementą, esantį sandėlio valdymo mobiliųjų įrenginių programėlėje, kai apdorojate paėmimo darbą.</li>
<li>Lauke <strong>Paimtas kiekis</strong> įveskite reikiamo paėmimo dalinį kiekį, kad nurodytumėte visą pajėgumą.</li>
</ol>
</td>
<td>
<ul>
<li>Dabartiniame darbe kiekis atnaujinamas iki likusio kiekio, kuris turi būti paimtas.</li>
<li>Sukuriamas ir uždaromas naujas paimto kiekio darbas.</li>
</ul></td>
<td>Netaikoma</td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a>Baigto darbo paimto kiekio mažinimas (iš krovinio)

<table>
<thead>
<tr>
<th>Pagrindinis sąrankos parametras</th>
<th>Paketo kiekis pasiekiamas</th>
<th>Pagrindiniai vartotojo veiksmai</th>
<th>Sandėlio darbas</th>
<th>Įvykdyto užsakymo paketo rezervavimas</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Netaikoma</td>
<td>Taip</td>
<td>
<ol>
<li>Krovinio eilutėje atidarykite puslapį <strong>Sumažinti paimtą kiekį</strong>.</li>
<li>Įveskite visą kiekį, kad panaikintumėte paėmimą.</li>
<li>Pasirinkite „perkelti į“ vietą / numerio lentelę.</li>
</ol>
</td>
<td>
<ul> 
<li>Su krovinio eilute susietas darbas atšaukiamas.</li>
<li>Sukuriamas ir uždaromas naujas atsargų perkėlimo darbas.</li>
</ul>
</td>
<td>Kiekis dar kartą rezervuojamas tam pačiam paketui. Sistema atsitiktine tvarka priskiria vietą ir numerio lentelę (jei vieta yra kontroliuojama pagal numerio lentelę), kurioje yra kiekis yra pasiekiamas.</td>
</tr>
<tr>
<td>Ne</td>
<td>Peržiūrėkite ankstesnę eilutę.</td>
<td>Peržiūrėkite ankstesnę eilutę.</td>
<td>Kiekis yra dar kartą rezervuojamas tam pačiam paketui ir tai pačiai vietai bei numerio lentelei (jei vieta yra kontroliuojama pagal numerio lentelę), kurios buvo įvestos atšaukiant paėmimą.</td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a>Sandėlyje esančios prekės perkėlimas

> [!NOTE]
> Šis sandėlio veiksmas taikomas tik **Darbo kūrimo procesas** tipo perkėlimui, o neperkėlimui pagal šabloną.

<table>
<thead>
<tr>
<th>Pagrindinis sąrankos parametras</th>
<th>Paketo kiekis pasiekiamas</th>
<th>Pagrindiniai vartotojo veiksmai</th>
<th>Sandėlio darbas</th>
<th>Įvykdyto užsakymo paketo rezervavimas</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Parinktis <strong>Leisti perkelti atsargas su susijusiu darbu</strong> darbuotojui įjungiama.</td>
<td>Taip</td>
<td>
<ol>
<li>Pradėkite perkėlimą sandėlio valdymo mobiliųjų įrenginių programėlėje.</li>
<li>Įveskite „iš“ ir „į“ vietas.</li>
</ol></td>
<td>
<ul>
<li>Visuose esamuose darbuose, paveiktuose perkėlimo, paėmimo vieta atnaujinama į naują vietą „į“.</li>
<li>Sukuriamas ir uždaromas naujas atsargų perkėlimo darbas.</li>
</ul>
</td>
<td>Visi esami rezervavimai, kuriuos paveikė kiekio perkėlimas iš tam tikros vietos, yra rezervuojami iš naujo tam pačiam paketui. Sistema atsitiktine tvarka priskiria vietą ir numerio lentelę (jei vieta yra kontroliuojama pagal numerio lentelę), kurioje yra kiekis yra pasiekiamas.</td>
</tr>
<tr>
<td>Ne</td>
<td>Peržiūrėkite ankstesnę eilutę.</td>
<td>Peržiūrėkite ankstesnę eilutę.</td>
<td>Visi esami rezervavimai, kuriuos paveikė kiekio perkėlimas iš tam tikros vietos, yra rezervuojami iš naujo tam pačiam paketui ir naujai vietai „į“ bei numerio lentelei (jei vieta yra kontroliuojama pagal numerio lentelę).</td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a>Baigto darbo paimto kiekio atšaukimas (iš krovinio arba bangos)

<table>
<thead>
<tr>
<th>Pagrindinis sąrankos parametras</th>
<th>Paketo kiekis pasiekiamas</th>
<th>Pagrindiniai vartotojo veiksmai</th>
<th>Sandėlio darbas</th>
<th>Įvykdyto užsakymo paketo rezervavimas</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'>Netaikoma</td>
<td>Taip</td>
<td>
<ol>
<li>Atidarykite puslapį <strong>Atšaukti darbą</strong>.</li>
<li>Užklausos puslapyje pasirinkite parinktį <strong>Palikti prekes dabartinėje vietoje</strong>.</li>
</ol>
</td>
<td>Su kroviniu susietas visas darbas atšaukiamas.</td>
<td>Kiekis dar kartą rezervuojamas tam pačiam paketui. Sistema atsitiktine tvarka priskiria vietą ir numerio lentelę (jei vieta yra kontroliuojama pagal numerio lentelę), kurioje yra kiekis yra pasiekiamas.</td>
</tr>
<tr>
<td>Ne</td>
<td>Peržiūrėkite ankstesnę eilutę.</td>
<td>Peržiūrėkite ankstesnę eilutę.</td>
<td>Kiekis yra dar kartą rezervuojamas tam pačiam paketui ir vietai bei numerio lentelei, kai kiekis buvo paliktas atšaukiant.</td>
</tr>
<tr>
<td>Taip</td>
<td>
<ol>
<li>Atidarykite puslapį <strong>Atšaukti darbą</strong>.</li>
<li>Užklausos puslapyje pasirinkite parinktį <strong>Priskirti prekes šiai vietai</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Dabartinis darbas atšauktas.</li>
<li>Sukuriamas ir uždaromas naujas atsargų perkėlimo darbas.</li>
</ul>
</td>
<td>Kiekis dar kartą rezervuojamas tam pačiam paketui. Sistema atsitiktine tvarka priskiria vietą ir numerio lentelę (jei vieta yra kontroliuojama pagal numerio lentelę), kurioje yra kiekis yra pasiekiamas.</td>
</tr>
<tr>
<td>Ne</td>
<td>Peržiūrėkite ankstesnę eilutę.</td>
<td>Peržiūrėkite ankstesnę eilutę.</td>
<td>Kiekis yra dar kartą rezervuojamas tam pačiam paketui ir vietai bei numerio lentelei, kurioms kiekis buvo priskirtas atšaukiant.</td>
</tr>
<tr>
<td>Taip/ne</td>
<td>
<ol>
<li>Atidarykite puslapį <strong>Atšaukti darbą</strong>.</li>
<li>Užklausos puslapyje pasirinkite parinktį <strong>Perkelti elementus į šią vietą</strong>.</li>
</ol>
</td>
<td>Atšaukimas nėra palaikomas.</td>
<td>Netaikoma</td>
</tr>
<tr>
<td>Taip/ne</td>
<td>
<ol>
<li>Atidarykite puslapį <strong>Atšaukti darbą</strong>.</li>
<li>Užklausos puslapyje pasirinkite parinktį <strong>Perkelti prekes, atsižvelgiant į vietos nurodymus</strong>.</li>
</ol>
</td>
<td>Atšaukimas nėra palaikomas. </td>
<td>Netaikoma</td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a>Nevisiškai paimkite kiekį – užregistruokite kiekį, kuris fiziškai nerastas vietoje / numerio lentelėje, kol atliekate paėmimo darbą

<table>
<thead>
<tr>
<th>Pagrindinis sąrankos parametras</th>
<th>Paketo kiekis pasiekiamas</th>
<th>Pagrindiniai vartotojo veiksmai</th>
<th>Sandėlio darbas</th>
<th>Įvykdyto užsakymo paketo rezervavimas</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Tipo <strong>Nevisiškai paimta</strong> darbo išimtis nustatyta, kai <strong>Prekių perskirstymas</strong> = <strong>Nėra</strong>, <strong>Atsargų koregavimas</strong> = <strong>Taip</strong> ir <strong>Pašalinti rezervavimus</strong> = <strong>Ne</strong>.</td>
<td>Taip</td>
<td>
<ol>
<li>Pasirinkite <strong>Nevisiškai paimta</strong> meniu elementą, esantį sandėlio valdymo mobiliųjų įrenginių programėlėje, kai vykdote paėmimo darbą.</li>
<li>Lauke <strong>Paimti kiekį</strong> įveskite <strong>0</strong> (nulį).</li>
<li>Lauke <strong>Priežastis</strong> įveskite <strong>Perskirstymo nėra</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Dabartinis darbas uždaromas, o paimtas kiekis yra 0 (nulis).</li>
<li>Tipo <strong>Inventorizacija</strong> atsargų operacija ir <strong>Parduota</strong> išdavimo tipas, yra sukuriami, kad būtų galima nurodyti koregavimą.</li>
</ul>
</td>
<td>Kiekis dar kartą rezervuojamas tam pačiam paketui. Sistema atsitiktine tvarka priskiria vietą ir numerio lentelę (jei vieta yra kontroliuojama pagal numerio lentelę), kurioje yra kiekis yra pasiekiamas.</td>
</tr>
<tr>
<td>Ne</td>
<td>Peržiūrėkite ankstesnę eilutę.</td>
<td>
<ul>
<li>Trumpo paėmimo veiksmas nepavyksta ir rodoma klaida.</li>
<li>Dabartinis darbas tebeatidarytas.</li>
</ul>
</td>
<td>Netaikoma</td>
</tr>
<tr>
<td rowspan='2'>Tipo <strong>Nevisiškai paimta</strong> darbo išimtis nustatyta, kai <strong>Prekių perskirstymas</strong> = <strong>Nėra</strong>, <strong>Atsargų koregavimas</strong> = <strong>Taip</strong> ir <strong>Pašalinti rezervavimus</strong> = <strong>Taip</strong>.</td>
<td>Taip</td>
<td>
<ol>
<li>Pasirinkite <strong>Nevisiškai paimta</strong> meniu elementą, esantį sandėlio valdymo mobiliųjų įrenginių programėlėje, kai vykdote paėmimo darbą.</li>
<li>Lauke <strong>Paimti kiekį</strong> įveskite <strong>0</strong> (nulį).</li>
<li>Lauke <strong>Priežastis</strong> įveskite <strong>Perskirstymo nėra</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Dabartinis darbas uždaromas, o paimtas kiekis yra 0 (nulis).</li>
<li>Tipo <strong>Inventorizacija</strong> atsargų operacija ir <strong>Parduota</strong> išdavimo tipas, yra sukuriami, kad būtų galima nurodyti koregavimą.</li>
</ul>
</td>
<td>Visi esami rezervavimai, kuriuos paveikė kiekio koregavimas iš trumpo paėmimo vietos, yra rezervuojami iš naujo tam pačiam paketui. Sistema atsitiktine tvarka priskiria vietą ir numerio lentelę (jei vieta yra kontroliuojama pagal numerio lentelę), kurioje yra kiekis yra pasiekiamas.</td>
</tr>
<tr>
<td>Ne</td>
<td>Peržiūrėkite ankstesnę eilutę.</td>
<td>Peržiūrėkite ankstesnę eilutę.</td>
<td>Visi esami rezervavimai, kuriuos paveikė kiekio koregavimas iš trumpo paėmimo vietos, yra pašalinami.</td>
</tr>
<tr>
<td>Tipo <strong>Nevisiškai paimta</strong> darbo išimtis nustatyta, kai <strong>Prekių perskirstymas</strong> = <strong>Neautomatinis</strong>, <strong>Atsargų koregavimas</strong> = <strong>Taip</strong> ir <strong>Pašalinti rezervavimus</strong> = <strong>Ne / Taip</strong>. Be to, parinktis <strong>Leisti neautomatinį prekių perskirstymą</strong> darbuotojui yra įjungta.</td>
<td>Taip</td>
<td>
<ol>
<li>Pasirinkite <strong>Nevisiškai paimta</strong> meniu elementą, esantį sandėlio valdymo mobiliųjų įrenginių programėlėje, kai vykdote paėmimo darbą.</li>
<li>Lauke <strong>Trumpai paimti kiekį</strong> įveskite <strong>0</strong> (nulį).</li>
<li>Lauke <strong>Priežastis</strong> pasirinkite <strong>Trumpas paėmimas su neautomatiniu perskirstymu iš naujo</strong>.</li>
<li>Sąraše pasirinkite vietą / numerio lentelę.</li>
</ol>
</td>
<td>
<ul>
<li>Dabartiniam darbui atsiranda šie veiksmai:
<ul>
<li>Paėmimo eilutė uždaroma, o paimtas kiekis yra 0 (nulis).</li>
<li>Padėjimo eilutė atšaukiama.</li>
<li>Sukuriama nauja paėmimo eilutė. Ji naudoja vietą / numerio lentelę, kurią pasirinko vartotojas.</li>
<li>Sukuriama nauja padėjimo eilutė.</li>
</ul>
</li>
<li>Tipo <strong>Inventorizacija</strong> atsargų operacija ir <strong>Parduota</strong> išdavimo tipas, yra sukuriami, kad būtų galima nurodyti koregavimą.</li>
</ul>
</td>
<td>Netaikoma</td>
</tr>
<tr>
<td>Tipo <strong>Nevisiškai paimta</strong> darbo išimtis nustatyta, kai <strong>Prekių perskirstymas</strong> = <strong>Neautomatinis</strong>, <strong>Atsargų koregavimas</strong> = <strong>Taip</strong> ir <strong>Pašalinti rezervavimus</strong> = <strong>Ne</strong>. Be to, parinktis <strong>Leisti neautomatinį prekių perskirstymą</strong> darbuotojui yra įjungta.</td>
<td>Ne</td>
<td>
<ol>
<li>Pasirinkite <strong>Nevisiškai paimta</strong> meniu elementą, esantį sandėlio valdymo mobiliųjų įrenginių programėlėje, kai vykdote paėmimo darbą.</li>
<li>Lauke <strong>Trumpai paimti kiekį</strong> įveskite <strong>0</strong> (nulį).</li>
<li>Lauke <strong>Priežastis</strong> pasirinkite <strong>Trumpas paėmimas su neautomatiniu perskirstymu iš naujo</strong>.</li>
</ol>
</td>
<td>Trumpo paėmimo veiksmas nepavyksta ir rodoma klaida.</td>
<td>Netaikoma</td>
</tr>
<tr>
<td>Tipo <strong>Nevisiškai paimta</strong> darbo išimtis nustatyta, kai <strong>Prekių perskirstymas</strong> = <strong>Neautomatinis</strong>, <strong>Atsargų koregavimas</strong> = <strong>Taip</strong> ir <strong>Pašalinti rezervavimus</strong> = <strong>Taip</strong>. Be to, parinktis <strong>Leisti neautomatinį prekių perskirstymą</strong> darbuotojui yra įjungta.</td>
<td>Ne</td>
<td>
<ol>
<li>Pasirinkite <strong>Nevisiškai paimta</strong> meniu elementą, esantį sandėlio valdymo mobiliųjų įrenginių programėlėje, kai vykdote paėmimo darbą.</li>
<li>Lauke <strong>Trumpai paimti kiekį</strong> įveskite <strong>0</strong> (nulį).</li>
<li>Lauke <strong>Priežastis</strong> pasirinkite <strong>Trumpas paėmimas su neautomatiniu perskirstymu iš naujo</strong>.</li>
<li>Sąraše pasirinkite vietą / numerio lentelę.</li>
</ol>
</td>
<td>
<ul>
<li>Dabartiniam darbui atsiranda šie veiksmai:
<ul>
<li>Paėmimo eilutė uždaroma, o paimtas kiekis yra 0 (nulis).</li>
<li>Padėjimo eilutė atšaukiama.</li>
</ul>
</li>
<li>Tipo <strong>Inventorizacija</strong> atsargų operacija ir <strong>Parduota</strong> išdavimo tipas, yra sukuriami, kad būtų galima nurodyti koregavimą.</li>
</ul>
</td>
<td>Visi esami rezervavimai, kuriuos paveikė kiekio koregavimas, iš trumpo paėmimo vietos numerio lentelės yra pašalinami.</td>
</tr>
<tr>
<td>Tipo <strong>Nevisiškai paimta</strong> darbo išimtis nustatyta, kai <strong>Prekių perskirstymas</strong> = <strong>Automatinis</strong>, <strong>Atsargų koregavimas</strong> = <strong>Taip / Ne</strong> ir <strong>Pašalinti rezervavimus</strong> = <strong>Taip / Ne</strong>.</td>
<td>Netaikoma</td>
<td>
<ol>
<li>Pasirinkite <strong>Nevisiškai paimta</strong> meniu elementą, esantį sandėlio valdymo mobiliųjų įrenginių programėlėje, kai vykdote paėmimo darbą.</li>
<li>Lauke <strong>Trumpai paimti kiekį</strong> įveskite <strong>0</strong> (nulį).</li>
<li>Lauke <strong>Priežastis</strong> pasirinkite <strong>Trumpas paėmimas su automatiniu perskirstymu iš naujo</strong>.</li>
</ol>
</td>
<td>Trumpas paėmimas, kuris apima automatinį priskyrimą iš naujo, nepalaikomas.</td>
<td>Trumpas paėmimas, kuris apima automatinį priskyrimą iš naujo, nepalaikomas.</td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a>Keisti atsargų būseną

> [!NOTE]
> Šį sandėlio veiksmą galima vykdyti iš kelių įvesties vietų. Čia rodomas pavyzdys naudoja veiksmą **Atsargų būsenos keitimas** puslapyje **Turimos atsargos pagal vietą**.

<table>
<thead>
<tr>
<th>Pagrindinis sąrankos parametras</th>
<th>Paketo kiekis pasiekiamas</th>
<th>Pagrindiniai vartotojo veiksmai</th>
<th>Sandėlio darbas</th>
<th>Įvykdyto užsakymo paketo rezervavimas</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Skirtuke <strong>Sandėlis</strong>, įraše <strong>Sandėlis</strong>, laukas <strong>Pašalinti rezervavimus ir žymėjimus</strong> yra nustatytas kaip <strong>Rezervavimai</strong> arba <strong>Žymėjimai ir rezervacijos</strong>.</td>
<td>Taip</td>
<td>
<ol>
<li>Pasirinkti konkrečią vietą.</li>
<li>Pasirinkite eilutę, kurioje yra konkreti prekė, vieta ir numerio lentelė (jei vieta yra kontroliuojama pagal numerio lentelę).</li>
<li>Pasirinkite <strong>Atsargų būsenos keitimas</strong>.</li>
<li>Nustatyti lauką <strong>Atsargų būsena</strong> į <strong>Blokavimas</strong>.</li>
</ol>
</td>
<td>Atsargų būsenos keitimai neleidžiami kiekiams, kurie rezervuoti darbams.</td>
<td>
<ul>
<li>Kiekis dar kartą rezervuojamas tam pačiam paketui. Sistema atsitiktine tvarka priskiria vietą ir numerio lentelę (jei vieta yra kontroliuojama pagal numerio lentelę), kurioje yra kiekis yra pasiekiamas.</li>
<li>Yra sukuriamos dvi tipo <strong>Atsargų būsenos keitimas</strong> atsargų operacijos, kurios rodo atsargų būsenos dimensijos pokytį.</li>
<li>Tipo <strong>Atsargų blokavimas</strong> ir išleidimo tipo <strong>Rezervuota faktiškai</strong> atsargų operacija yra sukurta, kad būtų galima nurodyti užblokuoto kiekio rezervavimą.</li>
</ul>
</td>
</tr>
<tr>
<td>Ne</td>
<td>Peržiūrėkite ankstesnę eilutę.</td>
<td>Atsargų būsenos keitimai neleidžiami kiekiams, kurie rezervuoti darbams.</td>
<td>
<ul>
<li>Rezervavimas pašalinamas.</li>
<li>Yra sukuriamos dvi tipo <strong>Atsargų būsenos keitimas</strong> atsargų operacijos, kurios rodo atsargų būsenos dimensijos pokytį.</li>
<li>Tipo <strong>Atsargų blokavimas</strong> ir išleidimo tipo <strong>Rezervuota faktiškai</strong> atsargų operacija yra sukurta, kad būtų galima nurodyti užblokuoto kiekio rezervavimą.</li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'>Skirtuke <strong>Sandėlis</strong>, įraše <strong>Sandėlis</strong>, laukas <strong>Pašalinti rezervavimus ir žymėjimus</strong> yra nustatytas kaip <strong>Nėra</strong>.</td>
<td>Taip</td>
<td>
<ol>
<li>Pasirinkti konkrečią vietą.</li>
<li>Pasirinkite eilutę, kurioje yra konkreti prekė, vieta ir numerio lentelė (jei vieta yra kontroliuojama pagal numerio lentelę).</li>
<li>Pasirinkite <strong>Atsargų būsenos keitimas</strong>.</li>
<li>Nustatyti lauką <strong>Atsargų būsena</strong> į <strong>Blokavimas</strong>.</li>
</ol>
</td>
<td>Atsargų būsenos keitimai neleidžiami kiekiams, kurie rezervuoti darbams.</td>
<td>Kiekis dar kartą rezervuojamas tam pačiam paketui. Sistema atsitiktine tvarka priskiria vietą ir numerio lentelę (jei vieta yra kontroliuojama pagal numerio lentelę), kurioje yra kiekis yra pasiekiamas.</td>
</tr>
<tr>
<td>Ne</td>
<td>Peržiūrėkite ankstesnę eilutę.</td>
<td>Atsargų būsenos keitimai neleidžiami kiekiams, kurie rezervuoti darbams.</td>
<td>Atsargų būsenos keitimai neleidžiami.</td>
</tr>
</tbody>
</table>

## <a name="limitations"></a>Apribojimai

- Pritaikomų sandėlio lygio dimensijų rezervavimo funkcija nepalaiko šių funkcijų:

    - Esamo svorio valdymas
    - Faktinės neigiamos atsargos
    - Rezervavimas pagal užsakytą tiekimą
    - Perkėlimo užsakymai ir žaliavų paėmimas

- Konteinerių konsolidavimo taisyklė, taikoma pakuotei pagal nurodomąjį vienetą, turi trūkumų. Įvykdyto užsakymo rezervavimams rekomenduojame nenaudoti konteinerio kūrimo šablonų, kai laukas **Pakuoti pagal nurodomąjį vienetą** yra įjungtas. Dabartiniame kūrimo įrankyje vietos nurodymai nenaudojami, kai sukuriamas sandėlio darbas. Todėl per krovimo į konteinerius bangos veiksmą taikoma tik mažiausia vienetų sekų grupė (atsargų vienetas).

## <a name="see-also"></a>Taip pat žiūrėkite

- [Paketų numeriai Sandėlio valdyme](/dynamicsax-2012/appuser-itpro/batch-numbers-in-warehouse-management)
- [To paties pardavimo užsakymo paketo rezervavimas](../sales-marketing/reserve-same-batch-sales-order.md)
- [Seniausio paketo paėmimas mobiliajame įrenginyje](pick-oldest-batch.md)
- [Paketo ir numerio lentelės patvirtinimas](batch-and-license-plate-confirmation.md)
- [Rezervavimų, atliekamų valdant sandėlį, trikčių šalinimas](troubleshoot-warehouse-reservations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]