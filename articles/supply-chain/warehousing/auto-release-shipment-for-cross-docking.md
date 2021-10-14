---
title: Automatinis siuntos išleidimas skirstant prekes
description: Šioje temoje aprašoma prekių skirstymo strategija, leidžianti automatiškai išleisti poreikio užsakymą į sandėlį, kai pranešama, kad gamybos užsakymas pagal poreikio kiekį, yra baigtas, kad kiekis būtų perkeliamas tiesiai iš gamybos vietos į pakrovimo vietą.
author: Mirzaab
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 1315bda1fd284eb326d4f08bf36bfea59074fde3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577941"
---
# <a name="auto-release-shipment-for-cross-docking"></a>Automatinis siuntos išleidimas skirstant prekes

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma prekių skirstymo strategija, leidžianti automatiškai išleisti poreikio užsakymą į sandėlį, kai pranešama, kad gamybos užsakymas pagal poreikio kiekį, yra baigtas. Tokiu būdu, kiekis, kurio reikia norint įvykdyti poreikio užsakymą, perkeliamas tiesiai iš gamybos vietos į pakrovimo vietą.

Prekių skirstymas yra sandėlio apdorojimo srautas, kuriame kiekis, kurio reikia norint įvykdyti siuntimo užsakymą, yra nukreipiamas į užsakymo pakrovimo rampą arba pateikimo vietą iš vietos, kurioje užsakymas buvo gautas. (Gaunamas užsakymas gali būti pirkimo užsakymas, perkėlimo užsakymas arba gamybos užsakymas.) Kadangi Išplėstinė prekių skirstymo funkcija palaiko visus tiekimo ir poreikio užsakymus ir bei reikalauja, kad siuntimo poreikis būtų paskelbtas prieš identifikuojant prekių skirstymo galimybę, automatinio siuntos išleidimo funkcijai būdingos šios savybės:

- Kaip tiekimo užsakymus ji palaiko tik gamybos užsakymus, o kaip poreikio užsakymus – tik pardavimo užsakymus ir perkėlimo užsakymus.
- Prekių skirstymo operacija gali būti paleista, net jei poreikio užsakymas nebuvo paleistas į sandėlį prieš užregistruojant tiekimo kvitą (t. y. prieš tai, kai gamyba buvo paskelbta baigta).

Ši prekių skirstymo funkcija turi du pranašumus:

- Sandėlio operacijos gali praleisti gatavų prekių kiekio padėjimo į įprastą sandėlio saugojimo vietą žingsnį, jei šie kiekiai bus paimti iš naujo, kad būtų įvykdytas siunčiamas užsakymas. Vietoj to, kiekiai gali būti perkelti vienu metu, nuo išeigos vietos iki pakavimo / siuntimo vietos. Tokiu būdu funkcija padeda sutrumpinti atsargų tvarkymo laiką ir galiausiai leidžia sutaupyti laiko ir vietos sandėlio ceche.
- Sandėlio operacijos gali atidėti pardavimo užsakymų ir perkėlimo užsakymų skelbimą į sandėlį, kol bus pranešta, kad gatavų prekių, susijusių su gamybos užsakymu, gamyba yra baigta. Šis pranašumas gali būti ypač aktualus gamybos pagal užsakymą aplinkose, kuriose gamybos laikas yra ilgesnis nei gamybos laikas gamybos į atsargas aplinkose.

## <a name="prerequisites"></a>Būtinieji komponentai

| Būtinoji sąlyga | Aprašymas |
|---|---|
| Elementas | Prekė privalo turėti įgalintus sandėlio valdymo procesus.<p>**Pastaba:** Prekių, kurioms suaktyvinta esamo svorio funkcija, negalima įtraukti į prekių skirstymo procesus.</p> |
| Sandėlis | Sandėlis privalo turėti įgalintus sandėlio valdymo procesus. |
| Prekių skirstymo šablonai | Sandėliui turi būti nustatytas bent vienas prekių skirstymo šablonas, kuris naudoja poreikio skelbimo strategiją **Tiekimo kvite**. |
| Darbo klasė | Turi būti sukurtas prekių skirstymo darbo klasės ID, skirtas darbo užsakymo tipui **Prekių skirstymas**. |
| Darbo šablonai | Norint sukurti prekių skirstymo paėmimo ir padėjimo darbą, reikalingi darbo užsakymo tipo **Prekių skirstymas** darbo šablonai. |
| Vietos nurodymai | Norint nukreipti padėjimo darbą į vietas, kuriose bus pakuojami ir siunčiami pardavimo užsakymo kiekiai, reikalingi darbo užsakymo tipo **Prekių skirstymas** darbo užsakymo vietos nurodymai. |
| Poreikio užsakymo ir gamybos užsakymo žymėjimas | Sandėlio sistema gali suaktyvinti automatinį siuntimo užsakymo siuntimo paleidimą ir kaip baigtą veiksmą sukurti prekių skirstymo darbą iš išeigos vietos ataskaitoje, tik jei pardavimo užsakymai ir perkėlimo užsakymai yra rezervuoti ir pažymėti gamybos užsakymui. |

## <a name="example-cross-docking-flow"></a>Prekių skirstymo srauto pavyzdys

Įprastas prekių skirstymo srautas susideda iš šių pagrindinių žingsnių.

1. Pardavimo užsakymo priėmėjas sukuria pardavimo užsakymą, skirtą pagal užsakymą gaminamam produktui. Paprastai prašomas kiekis nėra turimas ir pirmiausia turi būti pagamintas.
2. Pardavimo užsakymo priėmėjas sukuria gamybos užsakymą tiesiogiai iš pardavimo užsakymo eilutės. Tokiu būdu, pardavimo užsakymo priėmėjas rezervuoja ir pažymi pardavimo užsakymo kiekį pagal gamybos užsakymo kiekį. 

    Arba gamybos planuotojas nurodo, kad patvirtinant suplanuotus užsakymus reikia atnaujinti žymėjimą.

3. Gamybos užsakymui atliekami šie veiksmai:

    1. Gamybos planuotojas įvertina ir paskelbia gamybos užsakymą. (Įvertinimas apima žaliavų rezervavimą, o išleidimas apima išleidimą į sandėlį.)
    2. Sandėlio darbuotojas pradeda ir baigia žaliavos paėmimą iš saugojimo vietos į gamybos įvesties vietą pagal gamybos paėmimo darbą.
    3. Cecho operatorius pradeda gamybos užsakymą.
    4. Atliekant paskutinį veiksmą, mašinos operatorius naudoja mobilųjį įrenginį, kad praneštų apie baigą gamybos užsakymą.

4. Sistema naudoja nustatymą, kad identifikuotų dviejų susietų užsakymų prekių skirstymo įvykį, o tada atlieka šias užduotis:

    1. Automatiškai išleidžia susijusį pardavimo užsakymą į sandėlį, kad sukurtų siuntą.
    2. Automatiškai sukuria prekių skirstymo darbą, kuriame yra instrukcijos paimti gatavas prekes iš išeigos vietos ir perkelti jas į pakrovimo vietą, kurią prekių skirstymo vietos nurodymai priskyrė pardavimo užsakymui.
    3. Ragina mašinos operatorių užbaigti prekių skirstymo darbą iš karto po to, kai pranešama, kad gamybos užsakymas yra baigtas.

5. Užbaigus prekių skirstymo darbą ir kai kiekiai yra pakrauti į transporto priemonę, sandėlio išsiutimo planuotojas patvirtina pardavimo siuntą.

## <a name="example-scenario"></a>Pavyzdinis scenarijus

Pagal šį scenarijų turite turėti įdiegtus demonstracinius duomenis ir naudoti **USMF** demonstracinių duomenų įmonę.

### <a name="set-up-cross-docking-that-uses-the-auto-release-shipment-feature"></a>Prekių skirstymo nustatymas, kuris naudoja automatinio siuntos išleidimo funkciją

#### <a name="cross-docking-template"></a>Prekių skirstymo šablonas

1. Eikit į **Sandėlio valdymas** \> **Sąranka** \> **Darbas** \> **Prekių skirstymo šablonai**.
2. Pasirinkite **Naujas**.
3. Lauke **Eilės numeris** įveskite **1**.
4. Lauke **Prekių skirstymo šablono ID** įveskite pavadinimą, pvz., **Xdock\_RAF**.
5. Lauke **Poreikio skelbimo strategija** pasirinkite **Tiekimo kvite**.
6. Lauke **Sandėlis** įveskite sandėlio, kuriame norite nustatyti prekių skirstymo procesą, numerį. Šiame pavyzdyje pasirinkite **51**.

    > [!NOTE]
    > Kai tik pasirinksite **Tiekimo kvite** kaip šablono poreikio skelbimo strategiją, visi kiti puslapio laukai taps nepasiekiami. Taip pat negalite nurodyti jokių tiekimo šaltinių. Taip nutinka, nes prekių skirstymas, kuris naudoja automatinio siuntos išleidimo funkciją, kaip tiekimo šaltinius palaiko tik gamybos užsakymus ir reikalauja, kad būtų pardavimo užsakymų ir gamybos užsakymų žymėjimas. Jei kaip poreikio skelbimo strategiją pasirinksite **Prieš tiekimo kvitą**, skirtukų **Planavimas** ir **Tiekimo šaltiniai** laukai bus pasiekiami ir juos bus galima redaguoti.

#### <a name="work-classes"></a>Darbo klasės

1. Eikite į **Sandėlio valdymas** \> **Sąranka** \> **Darbas** \> **Darbo klasės**.
2. Pasirinkite **Naujas**.
3. Lauke **Darbo klasės ID** įveskite pavadinimą, pvz., **CrossDock**.
4. Lauke **Darbo užsakymo tipas** pasirinkite **Prekių skirstymas**.

Norėdami apriboti vietų, kuriose galima dėti paskirstytas gatavas prekes, tipus, galite nurodyti vieną ar daugiau galiojančių vietos tipų.

#### <a name="work-templates"></a>Darbo šablonai

1. Eikite į **Sandėlio valdymas** \> **Sąranka** \> **Darbas** \> **Darbo šablonai**.
2. Lauke **Darbo užsakymo tipas** pasirinkite **Prekių skirstymas**.
3. Pasirinkite **Naujas**.
4. Lauke **Eilės numeris** įveskite **1**.
5. Lauke **Darbo šablonas** įveskite pavadinimą, pvz., **CrossDock\_51**.
6. Pasirinkite **Įrašyti**.
7. Dalyje **Darbo šablono informacija** pasirinkite **Naujas**.
8. Naujai eilutei lauke **Darbo tipas** pasirinkite **Paimti**. Lauke **Darbo klasės ID** pasirinkite **CrossDock**.
9. Pasirinkite **Naujas**.
10. Naujai eilutei lauke **Darbo tipas** pasirinkite **Dėti**. Lauke **Darbo klasės ID** pasirinkite **CrossDock**.

#### <a name="location-directives"></a>Vietos nurodymai

Tam, kad gatavų prekių kiekių judėjimas būtų nukreiptas į įprastą sandėliavimo vietą, standartiniam gatavų prekių atidėjimo procesui reikia vietos nurodymo **Dėti**. Taip pat turite nustatyti prekių skirstymo vietos nurodymą **Dėti**, kad darbui nurodytumėte, jog baigtas kiekis būtų dedamas nurodytoje pakrovimo vietoje, naudojamoje susijusio pardavimo užsakymo pateikimui.

Atliekant prekių skirstymą, kaip ir atidedant gatavas prekes, nereikia sukurti vietos nurodymo paėmimo darbo veiksmui, nes nurodyta išeigos vieta. Be to, tikimasi, kad ši išeigos vieta bus nustatyta kaip numatytoji išeigos vieta viename iš su ištekliais susijusių įrašų (t. y. išteklius, išteklių grupės sąryšis arba išteklių grupė) arba kaip numatytoji gamybos gatavų prekių vieta sandėliui.

1. Eikite į **Sandėlio valdymas** \> **Sąranka** \> **Vietos direktyvos**.
2. Lauke **Darbo užsakymo tipas** pasirinkite **Prekių skirstymas**.
3. Pasirinkite **Naujas**.
4. Lauke **Eilės numeris** įveskite **1**.
5. Lauke **Pavadinimas** įveskite pavadinimą, pvz., **Baydoor**.
6. Lauke **Darbo tipas** pasirinkite **Padėjimas**.
7. Lauke **Vieta** pasirinkite **5**.
8. Lauke **Sandėlis** pasirinkite **51**.
9. „FastTab“ **Eilutės** pasirinkite **Naujas**.
10. Lauke **Kiekis iki** įveskite didžiausią intervalo kiekį, pvz., **1000000**.
11. Pasirinkite **Įrašyti**.
12. „FastTab“ **Vietos nurodymų veiksmai** pasirinkite **Naujas**.
13. Lauke **Pavadinimas** įveskite pavadinimą, pvz., **Baydoor**.
14. Pasirinkite **Įrašyti**.
15. Norėdami apriboti padėjimo vietas vienai ar kelioms konkrečioms vietoms, galite naudoti standartinę užklausos priemonę. Pasirinkite **Redaguoti užklausą** ir pasirinkite **51** kaip lauko **Sandėlis**, esančio lentelėje **Vietos**, kriterijų.

### <a name="cross-dock-finished-goods-to-the-outbound-location"></a>Gatavų prekių skirstymas į pakrovimo vietą

Norėdami skirstyti gatavų prekių kiekį į susijusio pardavimo užsakymo pakrovimo vietą, atlikite šiuos veiksmus.

1. Eikite į **Pardavimas ir rinkodara** \> **Pardavimo užsakymai** \> **Visi pardavimo užsakymai**.
2. Pasirinkite **Naujas**.
3. Pardavimo užsakymo antraštėje pasirinkite kliento sąskaitą **US-001** ir prekių skirstymui nustatytą sandėlį, kuris naudoja automatinio siuntos išleidimo funkciją.
4. Pridėkite gatavos prekės eilutę ir kaip kiekį įveskite **10**.
5. Dalyje **Pardavimo užsakymo eilutės** pasirinkite **Produktas ir tiekimas** \> **Gamybos užsakymas**.
6. Dialogo lange **Kurti gamybos užsakymą** peržiūrėkite numatytąsias vertes ir pasirinkite **Kurti**. Sukuriamas naujas gamybos užsakymas, susijęs su pardavimo užsakymu (t. y., jis rezervuotas ir pažymėtas).
7. Pasirinktinai: pakeiskite lauko **Kiekis** vertę taip, kad ji būtų didesnė už vertę, reikalingą pardavimo užsakymui įvykdyti. Kai gamybos kiekis skelbiamas baigtu, sistema, atsižvelgdama į įprastą gatavų prekių atidėjimo procedūrą, sukurs prekių skirstymo darbą pažymėtam kiekiui ir likusio kiekio atidėjimo darbui.

    Kaip minėta anksčiau, tarp pardavimo užsakymo ir gamybos užsakymo turi būti žymėjimas. Kitu atveju prekių skirstymas neveiks. Žymėjimą galima sukurti keliais būdais:

    - Sistema žymėjimą gali sukurti automatiškai šiais atvejais:

        - Gamybos užsakymas sukuriamas rankiniu būdu tiesiogiai iš pardavimo užsakymo eilutės (žr. 6 veiksmą).
        - Patvirtinami suplanuoti gamybos užsakymai, o nustatyta lauko **Atnaujinti žymėjimą** reikšmė yra **Standartinis**.

    - Vartotojas gali rankiniu būdu sukurti žymėjimą atidarydamas puslapį **Žymėjimas** iš poreikio užsakymo eilutės.

    > [!NOTE]
    > Žymėjimo negalima rankiniu būdu sukurti prekėms, kurios yra nustatytos kaip atsargų modelius naudoti standartinį ir svertinį vidurkį.

8. Puslapio **Gamybos užsakymas** veiksmų srityje, skirtuke **Gamybos užsakymas**, grupėje **Procesas**, pasirinkite **Įvertinti**, o tada pasirinkite **Gerai**. Užsakymas įvertintas, o žaliavų kiekis rezervuotas gamybai.
9. Veiksmų srityje, esančioje skirtuke **Gamybos užsakymas**, grupėje **Procesas**, pasirinkite **Išleisti**, o tada pasirinkite **Gerai**. Žaliavoms sukuriamas paėmimo darbas.
10. Atidarykite ir peržiūrėkite darbą. Veiksmų srityje, skirtuke **Sandėlis**, grupėje **Bendra** pasirinkite **Darbo informacija**. Pasižymėkite darbo ID.
11. Prisijunkite prie sandėlio mobiliųjų įrenginių programėlės darbo pradžiai sandėlyje Nr. 51.
12. Eikite į **Gamyba** \> **Gaminių paėmimas**.
13. Įveskite darbo ID, kad pradėtumėte ir užbaigtumėte žaliavų paėmimą. 

    Po to, kai pranešama apie baigtą darbą, žaliavų kiekis yra gamybos įvesties vietoje (USMF demonstraciniuose duomenyse – **005**) ir gali prasidėti gamybos užsakymo vykdymas.

14. Puslapio **Gamybos užsakymas** veiksmų srityje, skirtuke **Gamybos užsakymas**, grupėje **Procesas**, pasirinkite **Pradėti**, o tada pasirinkite **Gerai**.
15. Programoje eikite į **Gamyba** \> **RAF ir atidėjimas**.
16. Lauke **Produkto ID** įveskite gamybos užsakymo numerį ir kitą privalomą informaciją, tada pasirinkite **Gerai**.

Atkreipkite dėmesį į vykstančius įvykius:

- Suaktyvinamas susijusio pardavimo užsakymo išleidimas į sandėlį.
- Remiantis išleidimu, sukuriama siunta ir prekių skirstymas. Šis darbas nurodo sandėlio operatoriui paimti kiekius, kurie reikalingi pardavimo užsakymo eilutei įvykdyti, ir perkelti juos į pakrovimo vietą, nurodytą prekių skirstymo vietos nurodyme.
- Jei gamybos užsakymo kiekis yra didesnis nei kiekis, kurio reikia pardavimo užsakymui, sukuriamas įprastas atidėjimo darbas. Šis darbas nurodo sandėlio operatoriui paimti gatavų prekių kiekį, kuris lieka po prekių skirstymo ir perkelti jį į įprastą sandėliavimo vietą, atsižvelgiant į vietos nurodymą.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]