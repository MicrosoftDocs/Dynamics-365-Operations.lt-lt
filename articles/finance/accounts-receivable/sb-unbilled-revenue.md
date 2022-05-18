---
title: Neapmokėtos įplaukos
description: Šioje temoje paaiškinama, kaip nustatyti prekes ir sąskaitas, kad būtų galima naudoti neįrašytą įplaukų funkciją abonemento sąskaitose.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: a70786291822a85ec41c98ab8ce706f2ad79b08d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691251"
---
# <a name="unbilled-revenue"></a>Neapmokėtos įplaukos

Šioje temoje aprašoma negrąžintų įplaukų priemonė, kuri leidžia į balansą įtraukti visų atsiskaitymo grafikų sumas. Šios sumos yra įtraukiamos į negrąžintų įplaukų sąskaitą ir negrąžintą įplaukų korespondentinę sąskaitą, o sutarties sąskaitos išrašomos per įmokas.

## <a name="set-up-unbilled-revenue"></a>Nustatyti neišduotas įplaukas

Norėdami nustatyti neišduotas įplaukas, atlikite šiuos veiksmus.

- Periodinio **sutarties atsiskaitymo parametrų** puslapyje nustatykite laukus skyriuje **Neįrašyuotos** įplaukos.
- Neįskaitytų įplaukų priemonė gali būti naudojama prekėms, **kurių** prekės tipo laukas nustatytas kaip **standartinis**. Jį taip pat galima naudoti atidėjimo prekėms. Norėdami naudoti neišrašytas įplaukas su trumpalaikio funkcionalumo parinktimis, **nustatykite trumpalaikių pasirinkčių periodinės sutarties atsiskaitymo parametrų** puslapyje.

Norėdami nustatyti prekes, kad būtų galima naudoti neišduotas įplaukas, atlikite šiuos veiksmus.

1. Skirtuko Prekės **puslapyje Neįskaitytų** įplaukų **nustatymas** pasirinkite **Įtraukti**.
2. Naujoje eilutėje, prekės **kode**, pasirinkite prekės kodą.
3. **Lauke Prekės ryšys** pasirinkite prekės ryšį.
4. Norėdami pridėti daugiau eilučių, pakartokite šiuos veiksmus.
5. Pasirinkite **Įrašyti**.

Norėdami nustatyti prekes ir neišduotas įplaukų sąskaitas, atlikite šiuos veiksmus.

1. Skirtuko Sąskaitos **puslapyje Neįskaitytų** įplaukų **nustatymas** pasirinkite **Įtraukti**.
2. Naujoje eilutėje, prekės **kode**, pasirinkite prekės kodą.
3. **Lauke Prekės ryšys** pasirinkite prekės ryšį.
4. Pasirinkti sąskaitas, skirtas įplaukoms, kurių sf neišduotos, neišskaitytą nuolaidą ir nepastebamų įplaukų korespondentinę sąskaitą. Norėdami naudoti trumpalaikių sąskaitų apmokėjimą, **·** **·** **·** **turite nustatyti trumpalaikio neaprašyto metodo lauką kaip Periodinės sutarties atsiskaitymo parametrų puslapyje atlikti laikotarpiai arba Fiksuoti** metai.
5. Norėdami pridėti daugiau eilučių, pakartokite šiuos veiksmus.
6. Pasirinkite **Įrašyti**.

## <a name="use-unbilled-revenue"></a>Naudoti neišskaitytas įplaukas

1. Puslapyje Visi **atsiskaitymo grafikai sukurkite** atsiskaitymo grafiką.
2. Jei prekė dar nenustatyta naudoti neaprašytų įplaukų, **atsiskaitymo** grafiko eilutėje pažymėkite žymės langelį Neįrašomos įplaukos.
3. Nustatyti parinktį **Neįskaityto įplaukų** parinktis **Taip**. Tada peržiūrėkite ir redaguokite reikiamas ne vėliau kaip įplaukų, nuolaidų ir ne vėliau kaip korespondentinių sąskaitų sąskaitas.
4. Sąskaitų pateikimo grafike dalyje Neįrašytų **įplaukų apdorojimas** pasirinkite Sukurti žurnalo įrašą, **kad** sukurtumėte pradinį įplaukų, kurios nėra gautos, žurnalo įrašą. Šis veiksmas turi būti atliktas prieš išrašant atsiskaitymo grafiko SĄSKAITĄ faktūrą.
5. Sukūrę pradinį žurnalo įrašą, pasirinkite Generuoti SF **,** kad sukurtumėte pardavimo užsakymus ir registruokite sąskaitų pateikimo grafikų SF.
6. Kai SF užregistruojamos, galite peržiūrėti audito informaciją skirtuke **Atnaujinimai**, kurį rasite **visų atsiskaitymo grafikų puslapyje**.

### <a name="milestone-billing"></a>Sąskaitų pateikimas dalimis

Rodyklės atsiskaitymas veikia su neišrašytomis įplaukomis šiomis sąlygomis:

- Jei rodyklės pirminė prekė nėra išrašyta (pažymėtas žymės langelis Nenurašytos įplaukos), o rodyklės antrinių elementų sąskaita išrašoma (**·** **išvalomas** žymės langelis Neišrašytos įplaukos), būtina nurodyti pirminės prekės pradžios ir pabaigos datas. Šios datos naudojamos norint sukurti pradinį žurnalo įrašą.
- Jei rodyklės pirminė prekė nėra išrašyta (išvalytas neužrašytų įplaukų žymės langelis), o rodyklės antrinių elementų SF išrašomos (**·** **pažymėtas** žymės langelis Neišrašytos įplaukos), turi būti nurodyta tik antrinių prekių, kurių pradinį žurnalo įrašą norite sukurti, pabaigos data.

Kiekvieną rodyklės po prekę galima apdoroti atskirai. Pabaigos datas galima nurodyti, kai esate pasiruošę kurti pradinį žurnalo įrašą.

> [!NOTE]
> Jei jau sukurtas rodyklės pirminės prekės ar antrinių prekių pradinis žurnalo įrašas arba sukurta SF, pradžios ir pabaigos datų redaguoti negalima.

### <a name="unbilled-revenue-with-straight-line-deferrals"></a>Neišrašytomos įplaukos su tiesiogiai atitinka atidėjimais

Norėdami naudoti neišrašytas įplaukas su tiesiogiai suplanuotais atidėjimo grafikais, atlikite šiuos veiksmus.

1. Puslapyje Visi **atsiskaitymo grafikai sukurkite** atsiskaitymo grafiką.
2. Įtraukite prekę į atsiskaitymo grafiko eilutes.
3. Pasirinkti **eilutės** atidėjimus.
4. Operacijos atidėjimo **puslapyje** atlikite šiuos veiksmus:

    1. Nustatykite atidėtą **pasirinktį** kaip **Taip**.
    2. Jei reikia, pakeiskite sąskaitas.
    3. Grafiko **skyriuje** pasirinkite Tiesiogiai tiesiogiai **ir** redaguokite kitas vertes, jei reikia.
    4. Pasirinkite **Gerai**.

5. Pasirinkite **neišskaitytas** eilutės įplaukas, tada atlikite šiuos veiksmus:

    1. Nustatyti parinktį **Neįskaityto įplaukų** parinktis **Taip**.
    2. Pasirinkite sąskaitas, kurios bus taikomos įplaukoms, nuolaidai ir įplaukų korespondentinė sąskaitai.

6. Atsiskaitymo grafike dalyje Neaprašytų **įplaukų apdorojimas** pasirinkite Kurti **žurnalo įrašą**. Arba, norėdami sukurti žurnalo **įrašą, naudokite neįskaitomos** įplaukų masinio apdorojimo puslapį.
7. Atidėjimo grafikas sukurtas. Galite peržiūrėti išsamią informaciją puslapyje **Visi atidėjimų grafikai**. Sukūrus atidėjimų grafiką, galima redaguoti įvairias atsiskaitymo grafiko eilutės elemento vertes. Pavyzdžiui, galite redaguoti vieneto kainą, kiekį arba datas.

### <a name="unbilled-revenue-with-event-based-deferrals"></a>Neišrašytos įplaukos su įvykiais pagrįstu atidėjimu

Norėdami naudoti neišrašytas įplaukas su atidėjimo pagal įvykį grafikais, atlikite šiuos veiksmus.

1. Puslapyje Visi **atsiskaitymo grafikai sukurkite** atsiskaitymo grafiką.
2. Įtraukite prekę į atsiskaitymo grafiko eilutes.
3. Pasirinkti **eilutės** atidėjimus.
4. Operacijos atidėjimo **puslapyje** atlikite šiuos veiksmus:

    1. Nustatykite atidėtą **pasirinktį** kaip **Taip**.
    2. Jei reikia, pakeiskite sąskaitas.
    3. Grafiko **skyriuje** pasirinkite Pagal **įvykį**, Šabloną **,** Paskirstymo **tipą ir** Galiojimo **pabaigos sąskaitą**.
    4. Pasirinkite **Gerai**.

5. Pasirinkite **neišskaitytas** eilutės įplaukas, tada atlikite šiuos veiksmus:

    - Nustatyti parinktį **Neįskaityto įplaukų** parinktis **Taip**.
    - Pasirinkite sąskaitas, kurios bus taikomos įplaukoms, nuolaidai ir įplaukų korespondentinė sąskaitai.

6. Atsiskaitymo grafike dalyje Neaprašytų **įplaukų apdorojimas** pasirinkite Kurti **žurnalo įrašą**. Arba, norėdami sukurti žurnalo **įrašą, naudokite neįskaitomos** įplaukų masinio apdorojimo puslapį.
7. Atidėjimo grafikas sukurtas. Galite peržiūrėti išsamią informaciją puslapyje **Visi atidėjimų grafikai**. Sukūrus atidėjimų grafiką, galima redaguoti įvairias atsiskaitymo grafiko eilutės elemento vertes. Pavyzdžiui, galite redaguoti vieneto kainą, kiekį arba datas. Atidėjimo grafikas perskaičiuojamas pagal naujas vertes.

Paskirstymai perskaičiuojami pagal pasirinktą paskirstymo tipą (**Procentas**, **Baigimas procentais arba** Vienodos **sumos**). Kintamų **sumų** paskirstymo tipui paskirstymas perskaičiuojamas pagal įvykio pradinės vertės procento atitikmenį. Pavyzdžiui, pradinė vieneto kaina yra $100.00, o pradinės vertės procentas yra $55.00 (55 procentų). Jei vieneto kaina keičiama $200.00, kintamasis įvykio kiekis tampa $110.00 (vis dar 55 procentai).

> [!NOTE]
> Jei atidėjimo grafiko eilutės atpažintas, negalima redaguoti atsiskaitymo grafiko eilutės elemento. Norėdami redaguoti eilutės elementą, pirmiausia turite atšaukti atpažintas eilutes. Tada galima atnaujinti atsiskaitymo grafiko eilutę.

### <a name="unbilled-revenue-and-top-billing"></a>Neišrašytomos įplaukos ir viršutinės sąskaitos išrašymo data

Įvedamas trijų metų atsiskaitymo grafikas, o SF išrašoma kasmet per trijų metų laikotarpį. Visa sutarties suma įrašoma į neišrašytą įplaukų sąskaitą, iš kurios kuriamos metinės SF. Korespondentinė sąskaita yra įplaukų arba atidėtų įplaukų sąskaita.

Atkreipkite dėmesį, kad viršutinės sąskaitos išrašymas ir neįrašomos įplaukos veikia kartu, nes DK gali kilti suderinimo problemų. Pavyzdžiui, prekių grupės **nustatymo puslapyje** prekių grupė A **nustatoma** taip, kad viršutinių eilučių skaičius būtų nustatytas kaip **2**. **Atsiskaitymo grafikų puslapyje** yra trys elementai. Visos trys prekės priklauso prekių grupei A. Kai pradinis žurnalo įrašas sukuriamas įplaukų, kurių informacija nėra išsiųsta, visų trijų prekių suma apdorojama į neištaisytą sąskaitą. Sukūrus atsiskaitymo grafiko SF, įtraukiamos tik dviejų pagrindinių prekių sumos. Todėl SF suma nesutampa su suma, kuri buvo apdorota į neįrašytą įplaukų sąskaitą, o suderinimo problemos įvyksta DK.

Jei norite naudoti neišduotas įplaukas, **palikite** prekių grupės nustatymo puslapį tuščią arba nustatykite visas prekių grupes taip, **·** **kad viršutinių eilučių skaičius lauke būtų nustatytas kaip 0** (nulis). Jei norite naudoti viršutinį sąskaitų išrašymas, negalima atlikti jokių neužrašytų įplaukų veiksmų.

### <a name="examples"></a>Pavyzdžiai

Pagal versiją 10.0.27 įvedama nauja sąskaita, kai naudojamos neišskaitomos įplaukos. Kai užregistruojamas **pradinis žurnalo** įrašo kūrimo procesas, kreditas atliekamas naujai neišskaitomą įplaukų korespondentinę sąskaitą. Ši sąskaita naudojama vietoje įplaukų sąskaitos, kadangi ta pati vertė turi būti atšaukta išrašius sąskaitų faktūrų išrašymo sąskaitą faktūrą. Jeigu atsiranda valiutos kurso arba apvalinimo skirtumų, sumos, apskaičiuotos generuojant **SF procesą,** gali skirtis. Taip užtikrinama, kad grynoji sąskaitų suma yra 0 (nulis).

Šiame pavyzdyje parodyta, kaip naudoti neišrašytas įplaukas, kad būtų galima atpažinti visą balanso sutarties sumą kaip neišrašytas įplaukas. Kita įrašo pusė yra nepastebimos įplaukų korespondentinė sąskaita. Klientui išrašius SF, atšaukiamos neįrašytos įplaukos ir neįrašytų įplaukų korespondentinė sąskaita. Įplaukų pripažinimas bus arba SF išrašymo metu, arba pagal nustatytą atidėjimų pripažinimo grafiką.

#### <a name="assumptions"></a>Prielaidos

- Šių metų sausio 1 d. klientas pasirašo trijų metų sutartį dėl $390.
- Sutartį sudaro dvi dalys: licencijos ir priežiūros sutartis.
- Licencijos mokesčio pardavimo kaina yra $300, o klientui SF bus išrašyta $100 sutarties metų sausio 1 d. Pasirašant $300 licencijos mokestis bus laikomas įplaukomis.
- Priežiūros mokesčio pardavimo kaina yra $90, o klientui SF bus išrašyta $30 sutarties metų sausio 1 d. Mokėjimo $90 priežiūros mokestis bus atidėtas ir $2.50 mokestis bus atpažintas kiekvieną sutarties gyvavimo mėnesį.
- Klientui SF bus išrašyta $130 kiekvieno iš trijų sutarties metų pradžioje (sausio 1 d.).

#### <a name="steps"></a>Veiksmai

1. Nustatyti dvi išleistas prekes kaip neišduotas prekes. Norėdami nustatyti **prekes ir sąskaitas, kurių** įplaukos neišskaitomos, naudokite puslapį Neįskaitomos įplaukos.
2. Šiame pavyzdyje priežiūros mokestis atidedamas. Prekei reikia atidėjimo šablono, kuris nustatomas atidėjimų **šablonų** puslapyje. Šablono laikotarpio dažnumas **yra** Kas mėnesį, o atpažinimo laikotarpis – 36 mėnesių. Todėl mėnesio įplaukos yra $2.50.
3. Atidėtų **pagal numatytuosius nustatymus** prekių lauke **Priežiūros mokestis** nustatykite **atidėjimo prekę**. Dėl šio ir kito veiksmo priežiūros mokesčio prekė bus atidėta ją parduodant arba įtrauktą į atsiskaitymo grafiką.
4. Pasirinkite **atidėjimų numatytųjų nustatymų** \> **šabloną** ir pridėkite priežiūros mokesčio prekę ir tiesiogiai eilutėmis šabloną atlikdami 2 veiksmą. Priežiūros mokesčio prekė bus susieta su 36 mėnesių atidėjimo grafiku.
5. Kurti sąskaitų pateikimo grafiką, kuriame būtų dvi neaprašyto mokėjimo prekės. Sutarties atsiskaitymo grafikas nustatomas su šiais elementais.

    | Elementas | Pradžios data | Pabaigos data | Suma | Atsiskaitymo dažnumas | Atidėjimo prekė | Neapmokėtos įplaukos | Aprašymas |
    |---|---|---|---|---|---|---|---|
    | Licencija | Sausio 01 d., CIF | Gruodžio 31 d.RASTOS+2 d. | $100.00 | Kasmet | Ne | Taip | Klientui SF bus išrašoma $100.00 metu. Bendra $300.00 suma bus įrašyta iš anksto kaip balanso sąskaitos neįrašyta įplauka ir kaip pelno ir nuostolio įplaukos. Kiekviena SF sumažins neišrašytą sumą. |
    | Priežiūra | Sausio 01 d., CIF | Gruodžio 31 d.RASTOS+2 d. | $30.00 | Kasmet | Taip | Taip | Klientui SF bus išrašoma $30.00 metu. Bendroji $90.00 suma bus įrašyta iš anksto kaip neįrašomos įplaukos ir atidėtos įplaukos balanse. Kiekviena SF sumažins neišrašytą sumą. Atidėtos įplaukos bus atpažinsmos kas mėnesį per 36 mėnesius. |

6. Puslapyje Visi **sąskaitų pateikimo grafikai** naudokite įrašų procesą Kurti **žurnalą,** kad balanso sutarties vertė būtų registruojama kaip neplanuotos įplaukos.

Sukuriami du žurnalo įrašai: po vieną kiekvienai atsiskaitymo grafiko eilutei.

| Neapmokėtų įplaukų sąskaita | Įplaukų, kuriems neišrašyta sąskaita, korespondentinė sąskaita | Debeto suma | Kredito suma |
|---|---|---|---|
| Neapmokėtų įplaukų sąskaita | | $300.00 | |
| | Įplaukų, kuriems neišrašyta sąskaita, korespondentinė sąskaita | | $300.00 |

| Neapmokėtų įplaukų sąskaita | Atidėtos įplaukos | Debeto suma | Kredito suma |
|---|---|---|---|
| Neapmokėtų įplaukų sąskaita | | $90.00 | |
| |Atidėtos priežiūros įplaukos | | $90.00 |

Pirmas žurnalo įrašas užregistruojamas neįskaitomose įplaukų korespondentinės sąskaitose, o antrasis registruojamas atidėtų įplaukų sąskaitoje. Jei atsiskaitymo eilutėje yra ir neįrašytoms įplaukoms, ir atidėtoms įplaukoms, naudojama atidėtų įplaukų sąskaita, o ne ne neišsiųstų įplaukų korespondentinė sąskaita. Sutartyje reikalaujama, kad kliento SF būtų sukurta kasmet pradžioje. Norėdami sukurti **SF,** naudokite procesą Generuoti SF. Sukūrus SF, sukuriami šie žurnalo įrašai.

| Pagrindinė sąskaita | Neapmokėtų įplaukų sąskaita | Debeto suma | Kredito suma |
|---|---|---|---|
| Nepatebimos įplaukų korespondentinė sąskaita | | $100.00 | |
| | Neapmokėtų įplaukų sąskaita | | $100.00 |
| Gautinos sumos | | $100.00 | |
| | Įplaukų sąsk. | | $100.00 |

| Pagrindinė sąskaita | Neapmokėtų įplaukų sąskaita | Debeto suma | Kredito suma |
|---|---|---|---|
| Atidėtų priežiūros įplaukų sąskaita | | $30.00 | |
| | Neapmokėtų įplaukų sąskaita | | $30.00 |
| Gautinos sumos | | $30.00 | |
| | Atidėtų priežiūros įplaukų sąskaita | | $30.00 |

Šis tas pats žurnalo įrašas bus sukurtas SF, kurios užregistruotos kitų dviejų metų pradžioje. Atidėtų įplaukų sąskaitos grynoji suma bus 0 (nulis), nes nėra apvalinimo arba valiutos kurso skirtumų. Atidėtos įplaukos turi būti atšauktos tiksliai taip, kaip buvo kredituotos proceso Kurti **žurnalą metu**. Kadangi įplaukos vis dar atidėtos ir bus atpažinos vėliau, atidėtų įplaukų sąskaitos kreditas atsiranda dar kartą.

Paskutiniame veiksme atpažinimo žurnalo įrašas sukuriamas kiekvieną mėnesį, kad būtų atpažinti atidėtos priežiūros mokesčio įplaukos. Žurnalo įrašą galima sukurti naudojant atpažinimo **apdorojimo** puslapį. Kitu atveju, jį galima sukurti atidėjimo **grafiko** puslapiuose pasirinkus **Atpažinti** eilutes.

| Atidėtųjų įplaukų sąskaita | Įplaukų sąsk. | Debeto suma | Kredito suma |
|---|---|---|---|
| Atidėtos priežiūros įplaukos | | $2.50 | |
| | Priežiūros įplaukos | | $2.50 |

Šis žurnalo įrašas bus sukurtas kiekvieną kartą, kai bus vykdomas šio atidėto elemento atpažinimo procesas (iš viso 36 kartus).

#### <a name="short-term-fixed-year"></a>Trumpalaikis: fiksuoti metai

Galite naudoti **neišrašytas** **įplaukas kartu su trumpalaikiu funkcionalumu, nustatydami neaprašytą lauką periodinės sutarties atsiskaitymo parametrų** puslapyje. Toliau pateikiamas pavyzdys rodo skaičiavimus, kurie atliekami, kai fiksuotos įplaukos naudojamos kartu **su** fiksuotų metų trumpalaikiu nenuskaityto nusidėvėjimo metodu.

Sukuriamas atsiskaitymo grafikas, kuriame yra šie kriterijai:

- **Pradžios data:** 2020 m. birželio 1 d.
- **Pabaigos data:** 2021 m. gruodžio 31 d.
- **Vieneto kaina:** $100
- **Dažnis: kas** mėnesį

Puslapyje Visi **atsiskaitymo grafikai** pradinį žurnalo įrašą sukuria procesas Kurti **žurnalą**. Dabartinės trumpalaikio ir ilgalaikės sumos skaičiuojamos taip:

- **Trumpalaikių įplaukų, kurios neišskaitomos, suma:** $700
- **Dabartinė ilgalaikių įplaukų, kurios neišskaitomos, suma:** $1,200

SF sukuriama atsiskaitymo laikotarpiui nuo 2020 m. birželio 1 d. iki 2020 m. lapkričio 30 d. Dabartinės trumpalaikio ir ilgalaikės sumos skaičiuojamos taip:

- **Trumpalaikių įplaukų, kurios neišskaitomos, suma:** $100
- **Dabartinė ilgalaikių įplaukų, kurios neišskaitomos, suma:** $1,200

SF sukuriama atsiskaitymo laikotarpiui nuo 2020 m. gruodžio 1 d. iki 2020 m. gruodžio 31 d. Dabartinės trumpalaikio ir ilgalaikės sumos skaičiuojamos taip:

- **Trumpalaikių įplaukų, kurios neišskaitomos, suma:** $1,200
- **Dabartinė ilgalaikių įplaukų, kurios neišskaitomos, suma:** $0

#### <a name="short-term-rolling-periods"></a>Trumpalaikis: slenksties laikotarpiai

Galite naudoti neišrašytas įplaukas **kartu su trumpalaikiu funkcionalumu, nustatydami trumpalaikio neaprašyto metodo periodinės sutarties atsiskaitymo parametrų** puslapyje. Toliau pateikiamas pavyzdys rodo skaičiavimus, kurie **atliekami**, kai neįskaitomos įplaukos naudojamos kartu su trumpalaikiu nenuskaityto ataskaitinio laikotarpio metodu.

Sukuriamas atsiskaitymo grafikas, kuriame yra šie kriterijai:

- **Pradžios data:** 2020 m. birželio 1 d.
- **Pabaigos data:** 2021 m. gruodžio 31 d.
- **Vieneto kaina:** $100
- **Dažnis: kas** mėnesį

Puslapyje Visi **atsiskaitymo grafikai** pradinį žurnalo įrašą sukuria procesas Kurti **žurnalą**. Dabartinės trumpalaikio ir ilgalaikės sumos skaičiuojamos taip:

- **Trumpalaikių įplaukų, kurios neišskaitomos, suma:** $1,200
- **Dabartinė ilgalaikių įplaukų, kurios neišskaitomos, suma:** $700

SF sukuriama atsiskaitymo laikotarpiui nuo 2020 m. birželio 1 d. iki 2020 m. lapkričio 30 d. Dabartinės trumpalaikio ir ilgalaikės sumos skaičiuojamos taip:

- **Trumpalaikių įplaukų, kurios neišskaitomos, suma:** $1,200
- **Dabartinė ilgalaikių įplaukų, kurios neišskaitomos, suma:** $100

SF sukuriama atsiskaitymo laikotarpiui nuo 2020 m. gruodžio 1 d. iki 2020 m. gruodžio 31 d. Dabartinės trumpalaikio ir ilgalaikės sumos skaičiuojamos taip:

- **Trumpalaikių įplaukų, kurios neišskaitomos, suma:** $1,200
- **Dabartinė ilgalaikių įplaukų, kurios neišskaitomos, suma:** $0

### <a name="items-with-revenue-allocation"></a>Prekės su įplaukų paskirstymu

Dvi prekės, kurių atsiskaitymo dažnumas skiriasi, yra įtraukiami į atsiskaitymo grafiką. Ir naudoti neįrašomas įplaukas, ir yra atidėtos prekės.

- **Prekės numeris 1000: "** Surface Pro 128GB"

    - **Atsiskaitymo dažnumas: vieną** kartą
    - **Vieneto kaina:** $1,500
    - **Atskira pardavimo kaina:** $1,600
    - **Sutarties įplaukos:** $1,465.26

- **Prekės numeris S0021:** draudimas, parduodamas kartu su prekės numeriu 1000

    - **Atsiskaitymo dažnumas:** kas mėnesį 12 mėnesių
    - **Vieneto kaina:** $20 per mėnesį
    - **Atskira pardavimo kaina:** $25
    - **Sutarties įplaukos:** $264.74

Kadangi abi prekės naudoja neišrašytas įplaukas ir įplaukų paskirstymą, bendra sutarties suma atnaujinimo eilutėje yra 0 (nulis). Sutarties **įplaukų** stulpelis pridedamas ir rodo sutarties įplaukų sumą.

Šioje lentelėje rodomas pradinis prekių ir SF žurnalo įrašas.

| Neapmokėtų įplaukų sąskaita | Atidėtųjų įplaukų sąskaita | Debeto suma | Kredito suma |
|---|---|---|---|
| **Prekės 1000 žurnalo įrašas** | | | |
| Debeto neįrašytų įplaukų sąskaita (401250) | | $1,465.26 | |
| | Atidėtų kredito įplaukų sąskaita (250600) | | $1,465.26 |
| **Prekės 0021 žurnalo įrašas** | | | |
| Debeto neįrašytų įplaukų sąskaita (401250) | | $274.74 | |
| | Atidėtų kredito įplaukų sąskaita (250600) | | $274.74 |
| **PVM sąskaita faktūra** | | | |
| | Kredito nepateisytų įplaukų sąskaita | | $1,465.26 |
| | Kredito nepateisytų įplaukų sąskaita | | $274.74 |
| Debeto AR sąskaita (130100) | | $1,488.16 | |

#### <a name="changes-to-the-billing-schedule-line-billing-detail-line-or-revenue-allocation"></a>Atsiskaitymo grafiko eilutės, atsiskaitymo informacijos eilutės arba įplaukų paskirstymo pakeitimai

Pakeitus vieneto kainą arba kiekį, reikia atnaujinti kiekvienos prekės, kuri yra įplaukų paskirstymo dalis, sutarties įplaukų sumą. Todėl žurnalo įrašas perskaičiuojamas.

Pavyzdžiui, prekės 1000 vieneto kaina pakeičiama iš $1,500 į $1,600. Šiuo atveju sutarties įplaukų suma automatiškai perskaičiuojama kaip $1,549.47. Prekės S0021 sutarties įplaukos perskaičiuotos kaip $290.53.

Kai pakeistas patvirtinamas ir fiksuotas, abiejų prekių pradinio žurnalo įrašai atšaukiami ir sukuriami nauji žurnalo įrašai:

- **Prekė 1000:** pradinis pardavimo žurnalo įrašas $1,465.26 atšauktas. Sukuriamas naujas žurnalo $1,549.47 įrašas.
- **Prekė S0021:** pradinis pardavimo žurnalo įrašas $274.74 atšauktas. Sukuriamas naujas žurnalo įrašas$290.53 žurnalo įrašas.

#### <a name="termination"></a>Atleidimas

Prekės S0021 pradžios data yra 2020 m. sausio mėn., o pabaigos data – 2020 m. gruodžio mėn., bet yra nutraukta 2020 m. birželio mėn. Būtina perskaičiuoti sutarties įplaukų sumą abiems prekėms:

- **1000 prekė:** sutarties įplaukos perskaičiuotos kaip $1,567.67.
- **Prekė S0021:** sutarties įplaukos perskaičiuotos kaip $124.00.

Koregavimo žurnalo įrašas sukuriamas eilutei, kuri yra nutraukta. Eilutės, priklausančios tam pačiam kelių elementų išdėstymo (MEA) numeriui, žurnalo įrašas atšaukiatas ir sukuriamas naujas žurnalo įrašas:

- **Prekė 1000:** pradinis pardavimo žurnalo įrašas $1,465.26 atšauktas. Sukuriamas darbo $1,549.47 koregavimo žurnalo įrašas.
- **Prekė S0021:** pradinis pardavimo žurnalo įrašas $274.74 atšauktas. Sukuriamas naujas žurnalo $124.00 įrašas.
