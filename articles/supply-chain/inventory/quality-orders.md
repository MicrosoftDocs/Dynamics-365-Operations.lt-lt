---
title: Kokybės užsakymai
description: Šioje temoje aprašoma, kaip rankiniu būdu arba automatiškai kurti kokybės užsakymus, ir kaip su jais dirbti, norint atlikti tikrinimus ir įrašyti tikrinimo rezultatus programoje „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d06cd7766f4445a248e0394e75ae390314762cf211a2780da76b4f52aa5bccd4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739807"
---
# <a name="quality-orders"></a>Kokybės užsakymai

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip rankiniu būdu arba automatiškai kurti kokybės užsakymus, ir kaip su jais dirbti, norint atlikti tikrinimus ir įrašyti tikrinimo rezultatus programoje „Microsoft Dynamics 365 Supply Chain Management“.

## <a name="automatically-created-quality-orders"></a>Automatiškai kuriami kokybės užsakymai

Galite konfigūruoti sistemą taip, kad ji automatiškai kurs kokybės užsakymus pagal prekės pavyzdžių ėmimo taisykles. Daugiau informacijos ieškokite Kokybės [prekės bandymo valdymo tikrinimo](quality-item-sampling.md) priemonės.

## <a name="manually-create-quality-orders"></a><a name="manual-quality-orders"></a>Rankiniu būdu kurti kokybės užsakymus

Norėdami sukurti kokybės užsakymą rankiniu būdu, atlikite tolesnius veiksmus.

1. Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Kokybės užsakymai**.
1. Pasirinkite **Naujas**.
1. Dialogo lange **Kokybės užsakymai** lauke, **Nuorodos tipas** lauke, pasirinkite atsargų nuorodą, su ja bus susijęs jūsų kokybės užsakymas. Galimų pasirinkti nuorodų tipų aprašymo ieškokite toliau šioje temoje skyriuje [Kokybės užsakymo](#ref-types) nuorodos tipai.

    > [!NOTE]
    > Turi būti atsargų, susijusių su pasirinkta nuoroda. Jei nėra galimų nuorodos tipo, kiekio ir atsargų dimensijų derinio atsargų, gausite klaidos pranešimą.

1. Priklausomai nuo ankstesniame veiksme pasirinktos reikšmės, atlikite vieną iš **Nuorodos tipo** laukelių:

    - Jei pasirenkate **Atsargos**, tuomet jokia papildoma informacija yra nereikalaujama.
    - Jei pasirinkote **Pardavimas** ar **Pirkimas** , nurodykite šią informaciją:

        - **Sąskaitos pasirinkimas** – nurodyti kliento arba tiekėjo numerį.
        - **Nuorodos numeris** – nurodyti pardavimo užsakymo arba pirkimo užsakymo numerį.
        - **Nuoroda į partiją** – nurodyti konkrečią pardavimo užsakymo eilutę arba pirkimo užsakymo eilutę.

    - Jei pasirinkote **Gamyba**, **Sulaikymas** ar **Bendrų produktų gamyba**, laukelyje **Nuorodos numeris** gamybos užsakymo nuoroda, paketo numeris ar sulaikymo užsakymo numeris.
    - Jei pasirinkote **Maršruto operacija**, nurodykite šią informaciją:

        - **Nuorodos numeris** – nurodyti gamybos užsakymo arba paketo užsakymo numerį.
        - **Oper. Nr.** – nurodyti konkretaus maršruto operacijos numerį.
        - **Operacija** – nurodyti konkretaus maršruto operacijos numerį.
        - **Ištekliai** – nurodyti konkrečius išteklius, kurie turi būti naudojami maršruto operacijoje.

1. Lauke **Bandymo grupė** pasirinkite bandymo grupę, kurią reikia sukurti.
1. Lauke **Kiekis** įveskite prekių kiekį, kurį reikia patikrinti.
1. Skyriuje **Atsargų dimensijos** įveskite visas papildomas atsargų dimensijas, kurių reikia tai prekei.
1. Pasirinkite **Gerai**.

Kai kokybės užsakymas sukurtas, galite pradėti tikrinti atsargas ir įrašyti tikrinimo rezultatus. Daugiau informacijos apie tai, kaip įrašyti ir tikrinti tikrinimo rezultatus, [ieškokite prekių kokybės tikrinimas](tasks/inspect-quality-goods.md).

## <a name="quality-order-reference-types"></a><a name="ref-types"></a>Kokybės užsakymo nuorodų tipai

Kokybės užsakymai naudojami informacijai apie tikrinimus ir konkrečių atsargų jūsų sandėlyje tikrinimo rezultatus sekti. Kokybės užsakyme turi būti nuoroda, nurodanti tikrinamų atsargų šaltinį. Kokybės užsakymai gali būti susiję su šiais nuorodų tipais:

- **Atsargos** – šis nuorodos tipas nurodo, kad tikrinate turimų atsargų. Šio tipo patikrinimai paprastai yra atsitiktinai arba nesuplanuoti ir atliekami, kai sandėlio darbuotojas nustato problemą.
- **Pardavimas** – šis nuorodos tipas nurodo, kad tikrinate atsargas, susijusias su konkrečiu pardavimo užsakymu. Šio tipo patikrinimai paprastai yra susiję su kliento specifikacijomis arba analizės sertifikato (CoA), kuris turi būti pateiktas klientui kaip siuntos dalis, generavimą. (CoA kartais dar vadinamas atitikties sertifikatu \[Koc\].)
- **Pirkimas** – šis nuorodos tipas nurodo, kad tikrinate atsargas, susijusias su konkrečiu pirkimo užsakymu. Šio tipo patikrinimai dažnai naudojami gaunamiems prekėms tikrinti prieš jas pavarant į atsargas arba sunaudojamus gamybos procesuose.
- **Gamyba** – šis nuorodos tipas nurodo, kad tikrinate atsargas, susijusias su konkrečiu gamybos užsakymu. Šio tipo patikrinimai dažnai naudojami gautoms prekėms tikrinti prieš jas pavarant į atsargas arba sunaudojamus gamybos procesuose.
- **Sulaikymas** – šis nuorodos tipas nurodo, kad tikrinate atsargas, susijusias su konkrečiu karantino užsakymu. Sulaikymo užsakymai yra specialus užsakymo tipas, kuris seka atsargas išskirtinyje sandėlyje arba jūsų sandėlyje atskirtoje srityje. Šio tipo patikrinimai dažnai naudojami prekėms, kurias klientas grąžino arba kurios buvo sulaikytos, tikrinti ir atlikti tolesnę analizę. Sulaikymo užsakymus galima generuoti iš kokybės užsakymų. Jie taip pat gali būti sugeneruoti iš kitų šaltinių, tada kokybės užsakymai gali būti susiję su sulaikymo užsakymais.
- **Nukreipti veikimą** – šis nuorodos tipas nurodo, kad tikrinate atsargas, susijusias su konkrečiu nukreipimo žingsniu gamybos užsakymo. Šio tipo patikrinimai paprastai naudojami norint analizuoti produkto nebaigtą gamybą (NG) prieš pereiant prie kito gamybos proceso žingsnio.
- **Bendra gamyba** – šis nuorodos tipas nurodo, kad tikrinate atsargas, susijusias su konkrečiu bendros gamybos užsakymu. Šio tipo tikrinimai paprastai naudojami norint patikrinti paketinio užsakymo sudėtijus produktus prieš tai, kai sudėtiinis produktas įtraukiamas į atsargas.

## <a name="view-and-create-quality-orders-from-various-parts-of-the-system"></a>Peržiūrėti ir kurti kokybės užsakymus iš įvairių sistemos dalių

Kokybės užsakymus galima kurti rankiniu būdu. Jie taip pat gali būti sukurti automatiškai, remiantis jūsų apibrėžtais kokybės susiejimais. Daugiau informacijos apie tai, kaip sukurti ir valdyti automatinį kokybės užsakymų kūrimą, žr. [Kokybės susiejimus](quality-associations.md).

Kokybės užsakymo puslapį galite naudoti norėdami rankiniu būdu sukurti naują kokybės užsakymą arba peržiūrėti kokybės užsakymo, susijusio su kitu įrašu, būseną. Kokybės užsakymo puslapį galima pasiekti keliais būdais.

### <a name="from-the-quality-orders-page"></a>Iš kokybės užsakymų puslapio

Tam, kad rankiniu būdu kurtumėte prekybos užsakymus ir peržiūrėtumėte visus esančius užsakymus eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Kokybės užsakymai**. Likusiuose šios temos skyriuose pateikiama daugiau informacijos apie tai, kaip dirbti su **Kokybės užsakymų** puslapiu.

### <a name="from-sales-orders"></a>Iš prekybos užsakymų

Norėdami dirbti su kokybės užsakymais, susijusiais su jūsų prekybos užsakymais, eikite į **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai** ir tada atlikite šiuos veiksmus:

- Atidaryti pardavimo užsakymą arba pasirinkti jį tinklelyje. Tada, veiksmų juostoje, **Paimti ir supakuoti** skirtuke, **Kokybės valdymas** grupėje rinkitės **Kokybės užsakymai** tam, kad atvertumėte **Kokybės užsakymų** puslapį. Ten galite peržiūrėti, kurti arba atnaujinti su pardavimo užsakymu susijusius kokybės užsakymus.
- Atidarykite pardavimo užsakymą ir tada skirtuke **Antraštė** pasirinkite **Bendra** „FastTab“. Kokybės **užsakymo būsenos laukas** rodo bendrą visų kokybės užsakymų, susijusių su pardavimo užsakymu, būseną.
- Atidarykite pardavimo užsakymą ir tada skirtuke **Eilutė** pasirinkite **Prekybos užsakymo eilutės** Bendra. Kokybės **užsakymo būsenos** stulpelis rodo kiekvienos pardavimo užsakymo eilutės būseną.

### <a name="from-purchase-orders"></a>Iš pirkimo užsakymų

Norėdami dirbti su kokybės užsakymais, susijusiais su jūsų įsigijimo užsakymais, eikite į **Tiekimas ir šaltiniai \> Pirkimo užsakymai \> Visi pirkimo užsakymai** ir tada darykite šiuos veiksmus:

- Atidaryti pirkimo užsakymą arba pasirinkti jį tinklelyje. Tada, veiksmų juostoje **Gauti** skirtuke, **Kokybės valdymo** grupėje rinkitės **Kokybės užsakymai** tam, kad atvertumėte **Kokybės užsakymų** puslapį. Ten galite peržiūrėti, kurti arba atnaujinti su pirkimo užsakymu susijusius kokybės užsakymus.
- Atidarykite pirkimo užsakymą ir tada skirtuke **Antraštė** pasirinkite **Bendra** „FastTab“. Kokybės **užsakymo būsenos laukas** rodo bendrą visų kokybės užsakymų, susijusių su pirkimo užsakymu, būseną.
- Atidarykite pirkimo užsakymą ir tada skirtuke **Eilutė** pasirinkite **Pirkimo užsakymo eilutės** „FastTab“. Kokybės **užsakymo būsenos** stulpelis rodo kiekvienos pirkimo užsakymo eilutės būseną.

### <a name="from-production-orders"></a>Iš pirkimo užsakymų

Norėdami dirbti su kokybės užsakymais, susijusiais su jūsų gamybos užsakymais, eikite į **Gamybos kontrolė \> Gamybos užsakymai \> Visi gamybos užsakymai** ir tada atlikite šiuos veiksmus:

- Atidaryti gamybos užsakymą arba pasirinkti jį tinklelyje. Tada, veiksmų juostoje **Peržiūrėti** skirtuke, grupėje **Valdyti kokybę** rinktiės **Kokybės užsakymai** tam, kad atvertumėte **Kokybės užsakymų** puslapį. Ten galite peržiūrėti, kurti arba atnaujinti su pirkimo užsakymu susijusius gamybos užsakymus.
- Atidaryti gamybos užsakymą arba pasirinkti jį tinklelyje. Tada, veiksmų juostoje **Gamybos užsakymas** skirtuke **Gamybos informacija** grupėje rinkitės **Maršrutas** tam, kad atidarytumėte **Gamybos maršrutas** puslapį. Norėdami peržiūrėti kokybės užsakymus, susijusius su maršruto operacija, atlikite vieną iš šių veiksmų:

    - Tinklelyje pasirinkti tikslinio maršruto operaciją. Tada veiksmų srityje pasirinkite **Užklausas Kokybės \> užsakymai**.
    - Pasirinkite vertę lauke **Oper. Nr.** Tikslinio maršruto operacijos laukas, kuriame bus atidarytas **Gamybos** maršruto informacijos puslapis. „FastTab" **Bendri** kokybės užsakymo būsenos lauke rodoma kokybės **užsakymų**, susijusių su maršruto operacija, būsena.

- Atidaryti gamybos užsakymą ir pasirinkti **bendrąjį** „FastTab". Kokybės **užsakymo būsenos laukas rodo bendrą visų kokybės** užsakymų, susijusių su gamybos užsakymu, būseną.

### <a name="from-quarantine-orders"></a>Iš sulaikymo užsakymų

Norėdami dirbti su kokybės užsakymais, susijusiais su jūsų sulaikymo užsakymais, **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Sulaikymo užsakymai** ir tada atlikite šiuos veiksmus:

- Peržiūrėkite vertes **Kokybės užsakymo būsenos** stulpelyje. Tokiu būdu galite sužinoti bendrą visų kokybės užsakymų, susijusių su kiekvienu sulaikymo užsakymu tinklelyje, būseną.
- Pasirinkite sulaikymo užsakymą tinklelyje ir tada veiksmų juostoje rinkitės **Kokybės užsakymai** tam, kad peržiūrėtumėte, kurtumėte ir naujintumėte kokybės užsakymus, susijusius su sulaikymo užsakymu.

## <a name="advanced-actions-for-quality-orders"></a>Išplėstiniai kokybės užsakymų veiksmai

Kokybės užsakymams galite atlikti keletą veiksmų, norėdami valdyti būseną, generuoti dokumentus ir pateikti užklausą dėl papildomos informacijos.

### <a name="reopen-a-quality-order"></a>Atidaryti dar kartą kokybės užsakymą

Pagal numatytuosius nustatymus, po patikrinimo ir bandymų patvirtinimo nebegalima redaguoti ar atnaujinti kokybės užsakymo. Tačiau kai kuriais atvejais gali reikėti dar kartą atidaryti kokybės užsakymą jį baigus.

Norėdami iš naujo atverti kokybės užsakymą, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Kokybės užsakymai**.
1. Atidaryti patvirtintą kokybės užsakymą arba pasirinkti jį tinklelyje.
1. Veiksmų juostoje, pasirinkite **Atidaryti kokybės užsakymą iš naujo**.

### <a name="create-a-certificate-of-analysis-for-a-quality-order"></a>Kokybės užsakymo analizės sertifikato kūrimas

CoA yra ataskaita, kurią sugeneravo organizacijos kokybės užtikrinimo komanda. Ji patikrina, ar produktas atitinka konkrečius reikalavimus. Jūsų klientams arba reguliavimo institucijoms jūsų geopoliso vietoje gali reikėti CoAs. Jų gali reikėti atsižvelgiant į jūsų pramonės šaką ir produktų, kuriuos tvarkote, perkate, gaminate arba parduodate, tipą.

„Supply Chain Management“ leidžia sugeneruoti CoA iš kokybės užsakymo. Ataskaitoje bus įtraukti bet kurių kokybės užsakymo bandymų, kuriuose nustatyta **analizės sertifikato ataskaitos** parinktis *Taip,* rezultatai. Šią pasirinktį galima nustatyti pagal numatytuosius nustatymus, remiantis bandymu, kurį nurodote puslapyje **Testai**. Tačiau galite viršyti nustatymą konkretiems bandymams konkrečiam kokybės užsakymui.

Norėdami sukurti CoA kokybės užsakymą, atlikite tolesnius veiksmus.

1. Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Kokybės užsakymai**.
1. Pasirinkite kokybės užsakymą, kurio COA norite sukurti.
1. Veiksmų srityje pasirinkite **Analizės sertifikato \> užklausas**.
1. Puslapyje **Analizės sertifikatas** veiksmų juostoje rinkitės **Naujas**.
1. Nebūtina: lauke **Kontaktas** pasirinkite kontaktinį asmenį, kuriam turi būti adresuotas sertifikatas.
1. Veiksmų srityje pasirinkite **Spausdinimas**.
1. Analizės **Sertifikato dialogo** lange nurodykite, kaip ataskaita turėtų būti spausdinama. Tada pasirinkite **Gerai**, norėdami spausdinti ataskaitą spausdintuvu, ekrane, faile arba el. paštu.
1. Uždarykite puslapius.

### <a name="block-or-unblock-inventory-for-a-quality-order"></a>Blokuoti arba atblokuoti kokybės užsakymo atsargas

Kai kokybės užsakymas automatiškai generuojamas pagal kokybės susiejimą, kokybės susiejimui priskirtas prekės ėmimas gali būti konfigūruojamas taip, kad blokuoti visą tikrinamos nuorodos atsargų kiekį. Daugiau informacijos apie prekės mėginius, ieškokite Kokybės [prekės bandymo valdymo tikrinimo priemonės](quality-item-sampling.md).

Jei nenaudojate viso blokavimo arba jei kokybės užsakymą kuriate rankiniu būdu, sistema automatiškai sukuria prekės kiekio, kuris tikrinamas kokybės užsakyme, atsargų blokavimo įrašą. Įraše, kuris sukurtas **Atsargų blokavimo** puslapyje, atsargų **Blokavimo tipo laukas** nustatomas į *Kokybės užsakymą*.

Norėdami peržiūrėti ir redaguoti atsargų blokavimą kokybės užsakymui, kuris pasirinktas **Atsargų blokavimo** puslapyje, rinkitės **Užklausos \> Atsargų blokavimą** veiksmų juostoje. Norėdami gauti daugiau informacijos, žr. [inventoriaus blokavimas](inventory-blocking.md).

### <a name="inquire-about-the-details-of-a-quality-order"></a>Pateikti užklausą dėl kokybės užsakymo informacijos

Norėdami peržiūrėti daugiau informacijos apie kokybės užsakymą arba su juo susijusius, naudokite šiuos mygtukus **Kokybės užsakymų** puslapio veiksmų srityje:

- **Užklausos \> Darbo informacija** – atidaryti puslapį, kuriame galima peržiūrėti sandėlio darbą, susijusį su kokybės užsakymu.
- **Užklausos \> Neatitiktis** – atidarykite puslapį, kuriame galite peržiūrėti visas neatitiktis, susijusias su kokybės užsakymu.
- **Atsargos** – šio meniu komandos yra bendros visose atsargų operacijose. Galite naudoti juos peržiūrėti arba atnaujinti išsamią informaciją, pvz., operacijas, turimos atsargos, rezervavimas ir žymėjimas.

### <a name="create-cases-related-to-quality-orders"></a>Kurti atvejus, susijusius su kokybės užsakymais

Galite kurti atvejus, susijusius su kokybės užsakymais. Tokiu būdu galite sekti išsamią informaciją apie problemas ir dirbti su nutarimu. Tada galite naudoti atvejų valdymo darbo eigos priemones, kad per iš anksto nustatytą verslo procesą gautumėte papildomų patvirtinimų arba gautumėte daugiau informacijos apie tam tikrą problemą. Taip pat galite naudoti žinių straipsnių priemonę, kad sukurtumėte bendrųjų problemų nutarimų žinių bazę.

## <a name="case-management-examples-for-quality-management"></a>Atvejų valdymo pavyzdžiai, skirti kokybės valdymui

### <a name="example-1"></a>1 pavyzdys

Jūs dirbate gamybos įmonėje, kuri turi laikytis griežtų taisyklių, susijusių su reguliuojamųjų produktų, pvz., maisto, gamyba. Kokybės užsakymai naudojami išsamiai prekių kokybei gamybos procese įrašyti ir sekti. Jei tam tikrų kokybės užsakymo bandymų rezultatai nepavyksta, gali kilti įrangos problemų. Atvejai naudojami verslo procesui sekti ir išdavimui perskirti tinkamiems inžinieriams, kad būtų galima nustatyti šakninį priežastį. Kad verslo procesus būtų lengviau vykdyti, įmonė turi žinių apie bendrąsias problemas, susijusias su kokybės užsakymais ir įrangos klausimais.

### <a name="example-2"></a>2 pavyzdys

Jūs dirbate su paskirstymo įmone, kuri atųs produktus, kuriuos galima pritaikyti įvairioms šalims ir regionams. Kai kurie klientai turi griežtas specifikacijas, kurių reikia laikytis. Kitu atveju mokesčiai ir grąžinimai arba išlaidų grąžinimai gali būti patirtos. Naudokitės kokybės užsakymais norėdami sekti išsamią informaciją apie kiekvieną testą ir rezultatus, kurie atitinka kliento poreikius. Atvejai naudojami COA informacijai peržiūrėti ir patvirtinti prieš sugenerant dokumentą ir jį pridėjus prie kito siuntimo dokumento.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Kokybės valdymo procesai](quality-management-processes.md)
- [Kokybės testas](quality-tests.md)
- [Kokybės bandymo grupės](quality-test-groups.md)
- [Kokybės susiejimai](quality-associations.md)
- [Kokybės valdymo procesai](quality-management-processes.md)
- [Įjungti kiekio ir neatitikties valdymą](enable-quality-management.md)
- [Sandėlio procesų kokybės valdymas](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
