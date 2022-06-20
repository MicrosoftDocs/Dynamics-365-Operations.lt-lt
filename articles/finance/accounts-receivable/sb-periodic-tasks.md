---
title: Periodinės pasikartojančio sutarties atsiskaitymo užduotys
description: Šiame straipsnyje aprašomos periodinės užduotys, galimos periodiniame sutarties atsiskaitymo grafike.
author: JodiChristiansen
ms.date: 04/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: d834d1d7aa34448b4ef21606974538eb294b5d7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904794"
---
# <a name="periodic-tasks-in-recurring-contract-billing"></a>Periodinės pasikartojančio sutarties atsiskaitymo užduotys

Šiame straipsnyje aprašomos periodinės užduotys, galimos periodiniame sutarties atsiskaitymo grafike.

## <a name="generate-invoice"></a>Generuoti sąskaitą faktūrą

Norėdami kurti **masinį** periodinių SF iš informacijos, kurią nustatėte visuose sąskaitų apmokėjimo grafikuose ir Peržiūrėkite atsiskaitymo informacijos **puslapius** **·**, naudokite puslapį Generuoti SF. Kai sukuriama SF, pardavimo užsakymo apdorojimo eilutės prekės aprašymas atnaujinamas grafiko eilutės, kurios SF išrašyta, prekės aprašymu ir atsiskaitymo pradžios bei pabaigos datomis.

## <a name="generate-invoice-batch-processing"></a>Generuoti sąskaitų faktūrų paketo apdorojimą

Norėdami sukurti **pasikartojančias SF, naudodami** pasikartojantį paketinį apdorojimą, naudokite puslapį Generuoti SF paketinį apdorojimą. Galimi parametrai yra tokie patys, **kaip** ir parametrai, esantys puslapyje Generuoti SF, bet juos galima įrašyti paketiniu procesu, kurį galima vykdyti kelis kartus.

## <a name="price-update"></a>Kainos atnaujinimas

Norėdami vienu veiksmu atnaujinti kelių prekių kainas keliuose sąskaitų pateikimo grafikuose, naudokite kainos atnaujinimo priemonę. Kainas galima atnaujinti remiantis nurodyta procentine dalimi arba nurodyta suma. Eilučių sąraše rodomos tik dabartinės prekių vieneto kainos. Atnaujinus kainą, kainos nerodo.

Atkreipkite dėmesį į šiuos taškus apie kainos atnaujinimo priemonę:

- Jei tam tikrų metų pardavimo užsakymas jau sukurtas (t. y. prekėms išrašyta sąskaita), eilutės prekių kaina nėra paveikiama.
- Kainos atnaujinimo priemonę galima naudoti eilutės prekėms, kurių būsena yra **Aktyvus arba Sulaikyta** **.** Sulaikytų prekių planavimo parinktis **turi** būti nustatyta kaip Ne, **kai** sulaikymas buvo sulaikytas.
- Kainos atnaujinimo paslaugų programos negalima naudoti eilutės prekėms, kurios yra naudojimo prekės, kurios naudoja perskyrimą, rodyklės atsiskaitymą arba įplaukų skaidavimą.

### <a name="price-update-example"></a>Kainos atnaujinimo pavyzdys

Sukuriamas sąskaitų pateikimo grafikas ir pridedama atnaujinimo prekė. Vieneto kaina yra $750. Pirmieji prekės metai sumokami 2021 m. gruodžio 15 d. Sąskaitų pateikimo grafikas sukurtas laikotarpiui nuo 2022 m. sausio 1 d. iki gruodžio 31 d.

Atnaujinimo metu generuojant **SF** procesą sukuriamas 2022 m. pardavimo užsakymas. Kai veikia kainos atnaujinimo paslaugų programa, kaina atnaujinama iš failo $750 į $800.

Pardavimo užsakymo ir 2022 m. atsiskaitymo grafiko keisti negalima, o vieneto kaina lieka $750, nes jau išrašytos 2022 m. sąskaitų pateikimo grafiko sąskaitos. 2023 atsiskaitymo grafiko eilutė ir eilutės informacija atnaujinta $800, nes 2023 m. sąskaitų pateikimo grafikas dar neišrašytas.

### <a name="update-prices--flat-pricing-method"></a>Naujinti kainas – buto įkainojimo metodas

Atnaujinę prekių, kurios naudoja buti įkainojimo metodą, kainas, galite nurodyti procentą ar sumą kainai padidinti.

Norėdami paleisti prekių, kurios naudoja paprastos kainodaros metodą, kainos atnaujinimo priemonę, atlikite šiuos veiksmus.

1. Kainos atnaujinimo **paslaugų programos** puslapyje pasirinkite butų kainodaros **metodą**.
2. **Lauke Padidinimo metodas** pasirinkite padidinimo metodą, kuris naudojamas prekių kainai atnaujinti.
3. Atsižvelgdami į pasirinktą padidinimo metodą lauke Procentai nurodykite procentą **arba** sumą lauke **Suma**.
4. Įrašuose **, į kuriuos reikia** įtraukti "FastTab", norėdami įtraukti **duomenų** filtrus, naudokite mygtuką Filtras.
5. Norėdami **peržiūrėti įrašų** diapazoną, pasirinkite Peržiūra.
6. Jei kurių nors eilučių apdoroti nenorite, pažymėkite jas ir pasirinkite **Šalinti**.
7. Pasirinkite **Gerai**.

### <a name="update-prices--standard-pricing-method"></a>Naujinti kainas – Standartinis kainodaros metodas

Jei prekės kaina įraše pakeista, ji gali būti atnaujinta visose atsiskaitymo grafiko eilutėse, jei prekė naudoja standartinį kainos metodą.

1. Kainos atnaujinimo **paslaugų programos** puslapyje pasirinkite standartinės **kainodaros** metodą.
2. Įrašuose **, į kuriuos reikia** įtraukti "FastTab", norėdami įtraukti **duomenų** filtrus, naudokite mygtuką Filtras.
3. Norėdami **peržiūrėti įrašų** diapazoną, pasirinkite Peržiūra.
4. Jei kurių nors eilučių apdoroti nenorite, pažymėkite jas ir pasirinkite **Šalinti**.
5. Pasirinkite **Gerai**.

## <a name="mass-hold-processing"></a>Masinis sulaikymo apdorojimas

Norėdami taikyti **hold hold parinktis** keliems sąskaitų pateikimo grafikams tuo pačiu metu, naudokite masinio sulaikymo puslapį.

Norėdami sulaikyti tik vieną atsiskaitymo grafiką arba vieną atsiskaitymo grafiko eilutę, atidarykite **puslapį** Visi atsiskaitymo grafikai ir pasirinkite Sulaikyti **vietą**. Norėdami pašalinti sulaikymas, naudokite puslapį **Šalinti sulaikymas**.

### <a name="put-billing-schedules-on-hold"></a>Sulaikyti atsiskaitymo grafikus

Norėdami sulaikyti kelis atsiskaitymo grafikus, atlikite šiuos veiksmus.

1. Masinio **sulaikymas** puslapyje nustatykite parinkties **Procesas lauką** Taikyti **sulaikymas**.
2. **Lauke Priežasties kodas** pasirinkite priežasties kodą.
3. Nustatykite grafiko **koregavimo pasirinktį**:

    - **Taip** – jei nustatote pasirinktį **kaip Taip**, lauke Sulaikyta data nurodykite **hold date**. Pašalintos visos atsiskaitymo grafiko eilutės po sulaikymo datos.
    - **Ne** – atsiskaitymo grafiko eilutės nėra pakeistos. Pakeičiama tik būsena. Jis atnaujintas į **Sulaikyta**.

4. Įrašuose **, į kuriuos reikia** įtraukti "FastTab", norėdami įtraukti **duomenų** filtrus, naudokite mygtuką Filtras.
5. Norėdami **peržiūrėti įrašų** diapazoną, pasirinkite Peržiūra.
6. Jei kurių nors eilučių apdoroti nenorite, pažymėkite jas ir pasirinkite **Šalinti**.
7. Pasirinkite **Gerai**.

Kai grįžtate į atsiskaitymo grafikų sąrašą, turėtumėte matyti, kad atsiskaitymo grafikų būsena buvo pakeista į **Sulaikyta**.

### <a name="remove-a-hold-from-several-billing-schedules"></a>Pašalinti sulaikymas iš kelių atsiskaitymo grafikų

1. Masinio **sulaikymas** puslapyje nustatykite parinkties **Procesas lauką** pašalinti **sulaikymas**.
2. **Lauke Priežasties kodas** įveskite priežasties kodą.
3. Lauke Pašalinti **datą** pasirinkite datą, kada turi būti pašalintas sulaikymas.
4. Jei reikia **, nustatykite laukus** Pakartotinio **gavimo data** ir Atidėjimo data. Atidėjimo data pridedama prie visų eilučių, kurios yra atidėtos.
5. Įrašuose **, į kuriuos reikia** įtraukti "FastTab", norėdami įtraukti **duomenų** filtrus, naudokite mygtuką Filtras.
6. Norėdami **peržiūrėti įrašų** diapazoną, pasirinkite Peržiūra.
7. Jei kurių nors eilučių apdoroti nenorite, pažymėkite jas ir pasirinkite **Šalinti**.
8. Pasirinkite **Gerai**.

> [!NOTE]
> Norėdami pašalinti sulaikymas, turite nustatyti reikšmę **Šalinti sulaikymo** vartotojų grupę, kuri yra periodinio **sutarties atsiskaitymo parametrų** puslapyje.

Pavyzdžiui, sąskaitos pateikimo eilutės pradžios data yra 2022 m. vasario 1 d., o pabaigos data – 2022 m. vasario 28 d. Atsiskaitymo suma yra $200. Lauke **Sulaikyta** data nustatyta 2022 m. vasario 10 d. Dėl to vasario laikotarpis yra koreguojamas, kad nebūtų galima įtraukti jokių datų po vasario 10 d. Naujas laikotarpis yra nuo vasario 1 d. iki vasario 9 d., o suma $64.29 (naudojant kasdienį pa bookingą). Visos sąskaitų siuntimo grafiko eilutės, rastos vasario 10 d. arba vėliau, pašalintos.

Jei procesas **Šalinti sulaikymo** procesas baigtas, **o** lauko Pašalinti datą reikšmė yra 2022 m. vasario 10 d., bus du atsiskaitymo laikotarpiai. Pirmasis atsiskaitymo laikotarpis yra nuo vasario 1 d. iki vasario 9 d., o suma $64.29. Antrasis atsiskaitymo laikotarpis yra nuo vasario 10 d. iki vasario 28 d., o suma $135.71.

## <a name="mass-termination-processing"></a>Masinis nutraukimo apdorojimas

Naudokite masinio **atleidimo puslapį** norėdami atleisti atsiskaitymo grafiko eilutes, kurios šiuo metu rodomos nurodant atleidimo datą.

Jei naudojate įplaukų ir išlaidų atidėjimus, atsiskaitymo grafikai, **·** **·** **kurių** lauke Atleidimo data nustatyta koreguoti grafiką, puslapyje Visi sąskaitų apmokėjimo grafikai gali būti grąžinami.

Atsiskaitymo grafikai, kurie naudoja kelių elementų paskirstymo (MEA) funkciją, nėra masinio **atleidimo** puslapyje. Jūs vis tiek galite atleisti atskirą atsiskaitymo grafiką naudodami atsiskaitymo grafiko atleidimo funkciją.

> [!NOTE]
> Nėra atsiskaitymo grafiko eilučių, kurios šiuo metu **įtrauktos** į sf generavimo paketą.

Daugiau informacijos apie kiekvieną lauką ir procesą ieškokite Atleisti [atsiskaitymo grafikus](terminate-billing-schedule.md).

## <a name="mass-archive-process"></a>Masinis archyvavimo procesas

Naudokite masinio **archyvo puslapį** keliems sąskaitų pateikimo grafikams archyvuoti. Gali būti suarchyvuoti tik atleisti sąskaitų pateikimo grafikai.

Suarchyvus atsiskaitymo grafiką, įvyksta šie įvykiai:

- Būsena pakeista į **Archyvuota**.
- Atsiskaitymo grafikai yra visiškai užrakinti.
- Užklausos puslapiuose atsiskaitymo grafiko eilučių nebėra.

> [!NOTE]
> Atsiskaitymo grafiko archyvavimas yra nuolatinis veiksmas, jo negalima atšaukti.

Norėdami archyvuoti atsiskaitymo grafikus, atlikite šiuos veiksmus.

1. Masinio **archyvo** puslapio lauke **Atsiskaitymo pabaigos data** nurodykite atsiskaitymo pabaigos datą. Norėdami peržiūrėti visus nutrauktas atsiskaitymo grafikus, palikite šį lauką tuščią.
2. Įrašuose **, į kuriuos reikia** įtraukti "FastTab", **naudokite mygtuką** Filtras, kad apribokite rodomą įrašą.
3. Pasirinkite **Rodinio peržiūrą**.
4. Jei nenorite archyvuoti kai kurių įrašų, pažymėkite juos ir pasirinkite **Šalinti**.
5. Pasirinkite **Gerai,** kad būtų suarchyvuoti puslapio įrašai.

## <a name="mass-stubbing-process"></a>Masinis blokavimo procesas

Naudokite masinio **pasisiejikinimo** puslapį, kad visos pasirinktos atsiskaitymo grafiko eilutės būtų pažymėtos kaip išrašytos (suspūstos) arba nepažymėtos (atvirkštinėspūs). Dažniausiai užsispyrinėjamos arba atšaukiamos nebaigtos prekės importuotose atsiskaitymo grafiko eilutėse, kurios anksčiau buvo išrašytos kitoje sistemoje. Nebaigtos atsiskaitymo grafiko eilutės rodomos kaip nebaigtos ir kliento SF nesukuria.

### <a name="stub-records"></a>Suspūs įrašai

1. Masinio **suspūsčių** puslapio proceso pasirinkčių **lauke** pasirinkite **Nebaigta**.
2. **Galutinę datą nustatykite** galutinę datą, kad nurodykite eilutes, kurias norite taikyti procesui. Bus rodomi tik įrašai, kurių atsiskaitymo pradžios data yra nustatyta galutinę datą arba yra anksčiau.
3. Pasirinkite **Peržiūrėti, kad** būtų parodytos eilutės, kurias norite išspęsti.
4. Norėdami pašalinti eilutę iš proceso, pažymėkite ją, tada pasirinkite **Pašalinti**.
5. Pasirinkite Procesas **,** kad eilutės būtų susąsdinės.

### <a name="reverse-stub-records"></a>Atšauktisp. įrašus

1. Masinio **suspūsčių puslapio** lauke Proceso pasirinktys **pasirinkite** Atšaukti nebaigtą **sąslapį**.
2. **Galutinę datą nustatykite** galutinę datą, kad nurodykite eilutes, kurias norite taikyti procesui. Bus rodomi tik įrašai, kurių atsiskaitymo pradžios data yra nustatyta galutinę datą arba yra anksčiau.
3. Pasirinkite **Peržiūrėti, kad** būtų parodytos eilutės, kurias norite atšaukti suspėti.
4. Norėdami pašalinti eilutę iš proceso, pažymėkite ją, tada pasirinkite **Pašalinti**.
5. Pasirinkite Procesas **,** norėdami atšaukti eilutes suspūdimis.

## <a name="update-completion-date-process"></a>Atnaujinti užbaigimo datos procesą

Naudokite puslapį **Atnaujinti užbaigimo datą**, norėdami atnaujinti konkrečių rodyklės elementų, esančių keliuose atsiskaitymo grafikuose arba vartotojams, užbaigimo datą. Taip pat galite atnaujinti rodyklės šablonų, kurie naudoja baigimo procento metodą, prekių baigimo **procentą**.

1. Puslapyje Atnaujinti **užbaigimo datą** eikite į Rodyklės **apdorojimą** ir pasirinkite Atnaujinti baigimo **procentą**.
2. **Lauke Procento** suma įveskite visą užbaigtą procentą.
3. Pasirinkite prekės numerį, susijusį su rodyklės šablonu.
4. Įrašuose **, į kuriuos įtraukiama "** FastTab", pasirinkite Filtras, norėdami kaip filtro kriterijų pasirinkti konkrečią galutinio vartotojo sąskaitą, **·** **·** **·** **atsiskaitymo** grafiko numerį arba prekių numerių vertę.
5. Pasirinkite **Gerai**, norėdami apdoroti keitimą. Kai apdorojimas baigtas, prie rodyklės paskirstymo pridedama nauja eilutė. Ši eilutė nurodo procentinę dalį, kuri buvo užbaigta rodyklės šablone.

## <a name="unbilled-revenue-mass-processing"></a>Neapmokėtų įplaukų masinis apdorojimas

Naudokite neįrašytą **įplaukų** masinio apdorojimo puslapį norėdami sukurti neįrašytą įplaukų žurnalo įrašą arba susumuoti žurnalo įrašą, kuriame pateikiama viena ar daugiau pasirinktų atsiskaitymo grafikų arba informacijos apie sąskaitas eilučių.

- **Kurti žurnalo įrašą** – kurti kelių atsiskaitymo grafiko eilučių neišrašytų įplaukų žurnalo įrašus. Naudokite mygtuką **Filtras** įrašuose **, kuriuos norite įtraukti į** "FastTab", kad pasirinktumėte sąraše rodomų įrašų diapazoną. Sąraše pateikiamos tik tos atsiskaitymo grafiko eilutės, kurių įplaukų žurnalo įrašai, kurių kvitai nebuvo sukurti. Sukuriami pradinio žurnalo įrašai. Taip pat kuriami atidėjimo prekių atidėjimo grafikai.
- **Užsirašyto** žurnalo įrašas – pažymėkite atsiskaitymo grafiko eilutes, kurių žurnalo įrašai dar nesurašti. Ši pasirinktis naudojama, jei neišduotas žurnalo įrašas jau užregistruotas kitoje sistemoje. Jis pažymi neįrašytą įplaukų žurnalą kaip nebaigtą ir DK neregistruona operacijos.
- **Atšaukti nebaigto žurnalo įrašą** – atšaukite apdorotus nebaigtų įrašų žurnalo įrašus. Jei apdorojant "Stub" žurnalo įrašą **buvo padaryta klaida**, **ši parinktis išvalys atsiskaitymo grafiko eilutės žymės langelį Stubbox**.
- **Užsiduotojo atsiskaitymo informacijos** eilutė – naudokite šį procesą, kai išorinės sistemos sąskaitos nebuvo apdorotos, o kai kurios atsiskaitymo informacijos eilutės jau buvo išrašytos. Šis procesas užtikrins, kad sąskaitose, kurių sąskaitos neįrašomos, bus rodoma teisinga suma.
- **Atšauktispę atsiskaitymo informacijos eilutę** – atšaukite visus nebaigtų **sąskaitų pateikimo informacijos eilutės** veiksmus.

Laukas **Žurnalo** pavadinimas naudojamas registruoti **žurnalo įrašą** Kurti DK.

> [!NOTE]
> Nebaigtas procesas neregistravimo sumų DK. Laukas **Žurnalo pavadinimas** negalimas visiems suspūstims ir atšaukti nebaigtus procesus.

### <a name="unbilled-revenue-stub-example"></a>Nebaigtų įplaukų nebaigtos veiklos pavyzdys

Nustatytas vienerių metų sąskaitų pateikimo grafikas nuo 2021 m. spalio mėn. iki 2022 m. rugsėjo mėn. Neišsiųstos įplaukos jau apdorotos išorinėje sistemoje. Devynių atsiskaitymo grafiko mėnesių sąskaita jau išrašyta. Kiekvieno atsiskaitymo laikotarpio suma yra $250. Metų pradžioje bendra suma, užregistruota įplaukoms, kurių sf neišskaitomos, $3,000. Po devynių $2,250 sąskaitos jau išrašytos, o $750 įplaukų likutis.

Norėdami nustatyti atsiskaitymo grafiką, kuriame lieka tik trijų mėnesių vertė nesurašytų įplaukų, atlikite šiuos veiksmus.

1. Informacijos apie **sąskaitas** puslapyje sukurkite laikotarpio nuo 2021 m. spalio mėn. iki 2022 m. rugsėjo mėn., prekės numerio S0001 ir mėnesio $250 grafiką.
2. Sąskaitų **pateikimo grafikui pasirinkite** Kurti žurnalo įrašą. Sf $3,000 užregistruota įplaukoms, kurių sf nėra.
3. Pasirinkite **Nebaigtos sąskaitos informacijos eilutę** ir nurodykite operacijos datą 2022 m. birželio mėn. (devyni mėnesiai). Atsiskaitymo grafiko eilutės nebus rodomos peržiūroje. Paveiktos eilutės pagrįstos operacijos data.
4. Pasirinkite **Gerai**.

Pirmi devyni mėnesiai, kurių sąskaitos išrašytos, yra nebaigti.

[![Peržiūrėkite atsiskaitymo informacijos eilučių nebaigtą informaciją.](./media/01_View-billing-detail-stub.png)](./media/01_View-billing-detail-stub.png)

Sf $3,000 atšaukiama iš ne sf įplaukų, o $750 įplaukų, kurios lieka neužregistruotos, sf suma. Norėdami peržiūrėti nepatikrintų įplaukų registravimus, **·** **išsamios** eilutės informacijos puslapio skirtuke Atnaujinimai pasirinkite neįskaitytą įplaukų žurnalo įrašo auditą.

[![Neišskaitytų įplaukų žurnalo įrašo auditas.](./media/02_Unbilled-rev-journal-audit.png)](./media/02_Unbilled-rev-journal-audit.png)

> [!NOTE]
> Galima sukurti ne anksčiau pateiktą įplaukų žurnalo įrašą bet kuriam atnaujinimo laikotarpiui, nes išrašytos visų ankstesnio laikotarpio sąskaitų pateikimo informacijos eilučių sąskaitos. Pavyzdžiui, atsiskaitymo grafiko eilutės atsiskaitymo dažnumas yra kas mėnesį 12 mėnesių laikotarpis, nuo 2021 m. sausio iki gruodžio mėn. Eilutėje yra trys terminai: pradinis terminas, antras terminas (nuo 2022 m. sausio iki gruodžio) ir trečias terminas (nuo 2023 m. sausio iki gruodžio). Po to, kai SF sukuriama visoms informacijos apie sąskaitas eilutėms nuo pradinių 2021 m. 12 mėnesių, vėliau galima sukurti nepatirtų įplaukų žurnalo įrašą.
>
> Atidėjimo prekėms, kurios naudoja neaprašytų įplaukų funkciją, apdorojama atsiskaitymo eilutė ir nuolaidos eilutės. Šioms prekėms kuriamas neįrašyto įplaukų žurnalo įrašas ir atsiskaitymo eilutės atidėjimo grafikas bei nuolaidos eilutė.
>
> Žurnalo įrašai, kurie sukurti ne atidėjimo prekėms ir atidėjimo prekėms registruoti kreditą skirtingose įplaukų sąskaitose.
