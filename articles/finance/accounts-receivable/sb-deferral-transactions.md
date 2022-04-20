---
title: Atidėjimo operacijos abonemento sąskaitose
description: Šioje temoje aprašomos įvairios operacijos, kurias galima naudoti atidėjimo operacijose kaip įplaukų ir išlaidų atidėjimų dalis abonemento sąskaitose.
author: JodiChristiansen
ms.date: 11/04/2021
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
ms.openlocfilehash: f66c538afc732caf3faed3cfea6c695ff7f16273
ms.sourcegitcommit: d0e99545d722c924db57ae2bd06f72154a1f1f97
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/08/2022
ms.locfileid: "8557976"
---
# <a name="deferral-default-transactions"></a>Atidėjimo numatytosios operacijos

Šioje temoje aprašomos operacijos, kurios leidžia naudoti įplaukų ir išlaidų atidėjimus. Atidėjimo grafikai visada yra pagrįsti grindžiamą dokumentu arba atsiskaitymo grafiku ir nuo jo priklauso. Atidėjimo grafikai kuriami pagal numatytuosius nustatymus ir jų negalima įvesti arba kurti atskirai.

## <a name="sales-order-transaction-deferral"></a>Pardavimo užsakymo operacijos atidėjimas

Norėdami įvesti **arba redaguoti** pardavimo **užsakymo eilutės atidėjimo** parametrus naudokite atidėjimus arba kurti kredito pažymą.

> [!NOTE]
> Kai pardavimo užsakymas **sukurtas** **iš atsiskaitymo grafiko,** visos vertės, esantys puslapyje Atidėjimai arba Kurti kredito pažymą, yra tik skaitomi, o atidėjimo parametrų redaguoti negalima. Norėdami redaguoti vertes, naudokite puslapį Modifikuoti **grafiką**.

### <a name="edit-deferral-options"></a>Redaguoti atidėjimo parinktis

Norėdami redaguoti eilutės atidėjimo pasirinktis, atlikite šiuos veiksmus.

1. Sukurkite pardavimo užsakymo operaciją.
2. Pasirinkite eilutę, tada pasirinkite **Atidėjimai**.
3. Operacijos atidėjimo **puslapyje** atidėta pasirinktis **turi** būti nustatyta kaip **Taip**. Redaguokite kitus laukus, jei reikia.
4. Norėdami peržiūrėti atidėjimo grafiką, pasirinkite **Peržiūrėti**.
5. Jei atlikote kokius nors operacijos atidėjimo pakeitimus, pasirinkite Gerai **ir** grįžkite į operacijos puslapį.
6. Užfiksuokite ir užregistruokite operaciją.

Užregistrę operaciją, atidarykite visų **atidėjimų grafikų puslapį** ir peržiūrėkite atidėjimo grafiką.

### <a name="create-a-credit-note"></a>Kredito pažymos kūrimas

Norėdami sukurti kredito pažymą atlikite nurodytus veiksmus.

1. Sukurkite pardavimo užsakymo operaciją.
2. **Pardavimo užsakymo eilučių** skyriuje pasirinkite prekę, kurios kredito pažymą norite sukurti.
3. Pasirinkite **Pardavimo užsakymo eilutė** \> **Nauja**, tada pasirinkite Kredito **pažyma.**
4. Pasirinkti **atidėjimus**.
5. Pardavimo užsakymo **operacijos atidėjimo puslapyje** nustatykite prekės esamo **grafiko** koregavimo pasirinktį **Taip**.
6. Koreguotame **grafiko** lauke pasirinkite atidėjimų grafiką, kurį norite taikyti kredito pažymai.
7. Atnaujinkite **laukus Perskaičiuoti datą ir** **Pabaigos data kaip** jums reikia.
8. Pasirinkite **Gerai**.
9. Baigti pardavimo užsakymo operacijos registravimą.

### <a name="purchase-orders-and-purchase-invoices"></a>Pirkimo užsakymai ir pirkimo SF

Jei norite naudoti atidėjimo funkciją pirkimo užsakymui, pirmiausia sugeneruokite SF. Tada norėdami redaguoti **arba pridėti atidėjimo prekes** naudokite laukiančių tiekėjo SF puslapį. Negalite tiesiogiai redaguoti ar pridėti atidėjimų prie pirkimo užsakymo.

1. Norėdami įvesti **tiekėjo SF, naudokite laukiančių** tiekėjo SF puslapį.

    Kai įvedate eilutę, automatiškai nustatomas jūsų pasirenkatos prekės ar įsigijimo kategorijos atidėjimas. Šis atidėjimas pagrįstas atidėjimo numatytųjų **parametrų puslapyje.** Atidėjimus galima redaguoti arba pridėti paskirstymo lygyje.

3. Pirkimo eilutėje pasirinkite Finansai **paskirstyti \> sumas**.
4. Kiekvienai paskirstymo sumai pasirinkite **Atidėjimai**. Užregistrus SF, sukuriamas kiekvieno paskirstymo, kuriam nustatytas atidėjimas, atidėjimo grafikas.

### <a name="tax"></a>Mokesčiai

Kai kuriais atvejais mokesčių suma gali būti visiškai arba iš dalies nesugrąžinama. Jei atidėjimo eilutės mokesčio suma yra nesugrąžintina suma, nesugrąžinama mokesčio suma registruojant SF įtraukiama į atidėjimo grafiko sumą.

### <a name="variance"></a>Nukrypimas

Jei tiekėjo SF eilutės suma skiriasi nuo pirkimo užsakymo eilutės sumos, sukuriami nuokrypių paskirstymai. Jei eilutė atidėta, šių paskirstymų DK sąskaita yra nustatyta atidėjimo sąskaitai, o sumos yra įtraukiamos į atidėjimo grafiko sumą registruojant SF. Šie paskirstymai vadinami **kainų nuokrypiu** ir **išlaidų nuokrypiu**.

### <a name="general-journals-and-invoice-journals"></a>Bendrieji žurnalai ir SF žurnalai

Norėdami įvesti **žurnalo** kvito eilutės atidėjimų parametrus, naudokite atidėjimų puslapį. Taip pat galite peržiūrėti tiesiogiai suplanuotų atidėjimų atidėjimų grafiką. Kai įvedate eilutę, atidėjimas automatiškai nustatomas remiantis **atidėjimo sąskaitų nustatymu atidėjimo numatytųjų nustatymų** puslapyje. Galite neautomatiniu būdu pakeisti kiekvienos eilutės atidėjimo pasirinktis. Užregistrus žurnalo kvitą, sukuriamas atidėjimo grafikas.

#### <a name="post-and-transfer"></a>Registruoti ir perkelti

Norėdami užregistruoti žurnalo kvitą, naudokite komandą **Registruoti ir** perkelti. Atidėjimo pasirinktys bus po eilutės, su kurią taikomas kvitas. Kvitams, kurių klaidų nėra, atidėjimo grafikas sukuriamas, jei jis atidėtas. Kvitui, kuriame yra klaida ir kuris yra perkeliamas, visos atidėjimo pasirinktys taip pat perkeliamos su juo.

#### <a name="tax"></a>Mokesčiai

Kai kuriais atvejais mokesčių suma gali būti visiškai arba iš dalies nesugrąžinama. Jei atidėjimo eilutės mokesčio suma yra nesugrąžintina suma, nesugrąžinama mokesčio suma registruojant SF įtraukiama į atidėjimo grafiko sumą.

## <a name="free-text-invoice-transaction-deferral"></a>Laisvos formos SF operacijos atidėjimas

Norėdami įvesti **laisvos formos** SF eilutės paskirstymo atidėjimo parametrus naudokite atidėjimų puslapį. Kai įvedamas paskirstymas, atidėjimas automatiškai nustatomas remiantis atidėjimo numatytųjų **parametrų puslapyje**.

## <a name="fields"></a>Laukai

Operacijos **atidėjimo** puslapyje yra šie laukai.

| Laukas | Aprašymas |
|-------|-------------|
| Atidėta | <p>Nurodykite, ar eilutė yra atidėjimas:</p><ul><li>**Taip** – eilutė yra atidėjimas.</li><li>**Ne** – eilutė nėra atidėjimas.</li></ul><p>Kai ši pasirinktis nustatyta **kaip Taip**, **negalima naudoti** esamos grafiko parinkties Koreguoti esamą. Prekėms ir mokesčiams, kurie jau nustatyti kaip atidėti, ši pasirinktis nustatyta kaip **Taip**. Prekėms ir mokesčiams, kurie pagal numatytuosius nustatymus nėra nustatyti kaip atidėti, nustatykite šią pasirinktį kaip **Taip**.</p> |
| Koreguoti esamą grafiką | <p>Nurodyti, ar eilutė yra esamo atidėjimo grafiko koregavimas:</p><ul><li>**Taip** – nauja pardavimo eilutė yra esamo atidėjimo grafiko koregavimas. Tokiu atveju koreguotos grafiko lauke galite pasirinkti atidėjimo **grafiką**.</li><li>**Ne** – nauja pardavimo eilutė nėra esamo atidėjimo grafiko koregavimas.</li></ul><p>Kai ši pasirinktis nustatyta **į Taip**, **pasirinktis** Atidėta yra negalima.</p> |
| Pakoreguotas grafikas | <p>Pasirinkti atidėjimo grafiką, kurį koreguoja eilutė. Tada visos puslapio vertės atnaujinamos verčių iš atidėjimo grafiko verčių. Šių verčių redaguoti negalima.</p><p>Šis laukas galimas tik tada, kai nustatyta **parinktis Koreguoti** esamą grafiką kaip **Taip**.</p> |
| Perskaičiavimo data | <p>Nurodykite laikotarpio, pagal kurį norite perskaičiuoti likusią sumą, pradžios datą. Numatytoji data yra kito neatpažįsto laikotarpio data.</p><p>Šis laukas galimas tik tada, kai nustatyta **parinktis Koreguoti** esamą grafiką kaip **Taip**.</p> |
| Pabaigos data | <p>Atsižvelgiant į atidėjimo tipą, pabaigos data gali būti arba negali būti atnaujinta:</p><ul><li>Nurodykite naują tiesiogiai suplanuoto atidėjimo pabaigos datą. Esama atidėjimo grafiko pabaigos data yra numatytoji vertė.</li><li>Įvykio pagrįstame atidėjime nurodykite kredito įvykio eilutės pabaigos datą. Ši data gali būti neįpildyta.</li></ul><p>Šis laukas galimas tik tada, kai nustatyta **parinktis Koreguoti** esamą grafiką kaip **Taip**.</p> |
| Atsiskaitymo grafiko numeris | <p>Atsiskaitymo grafiko numeris.</p><p>Šis laukas galimas tik periodinių sutarties atsiskaitymo grafikų atveju.</p> |
| Atidėjimo koregavimo būdas | <p>Atidėto koregavimo metodas. Vertė atitinka pasikartojančios sutarties atsiskaitymo **grafiko** masinio atleidimo apdorojimo puslapio vertę.</p><p>Šis laukas galimas tik periodinių sutarties atsiskaitymo grafikų atveju.</p> |
| **Sąskaitos – Įplaukos** | |
| Atidėjimo sąskaita | <p>Atidėjimo sąskaita, kuri yra registravimo sąskaita, rodoma pardavimo **užsakymo** puslapyje.</p><p>Jei eilutė nėra atidėta, šis laukas yra tuščias. Šiuo atveju registravimo sąskaita yra numatytoji įplaukų sąskaita.</p> |
| Pripažinimo sąskaita | <p>Nurodykite sąskaitą, kuri naudojama atpažintą atidėjimą. Ši sąskaita turi skirtis nuo atidėjimo sąskaitos.</p><p>Kai pasirinktis **Atidėta** iš pradžių **nustatyta kaip Taip**, dimensijos vertės, naudojamos atidėjimo sąskaitoje, nukopijuojamos į atpažinimo sąskaitą. Jei atidėjimo sąskaitos dimensijos nėra atpažinimo sąskaitai, jos nepaisoma.</p> |
| Pradinio pripažinimo sąskaita | <p>Pasirinkti sąskaitą pradiniam įplaukų atpažinimui. Numatytoji vertė yra iš atidėjimų **numatytųjų reikšmių** puslapio.</p><p>Šis laukas galimas tik tada, kai **lauko Atidėjimo registravimo** **·** **būdas puslapio Įplaukos ir išlaidų atidėjimai parametrai nustatyta kaip Pelnas ir nuostoliai.**</p> |
| Pripažinimo korespondentinė sąskaita | <p>Pasirinkite korespondentinės įplaukų pripažinimo sąskaitą. Numatytoji vertė yra iš atidėjimų **numatytųjų reikšmių** puslapio.</p><p>Šis laukas galimas tik tada, kai **lauko Atidėjimo registravimo** **·** **būdas puslapio Įplaukos ir išlaidų atidėjimai parametrai nustatyta kaip Pelnas ir nuostoliai.**</p> |
| **Sąskaitos - Nuolaida** | Šis skyrius rodomas tik atidėtų prekių atveju. Jis paslėptas atidėtų mokesčių mokėjimo metu. |
| Atidėjimo sąskaita | <p>Nurodyti nuolaidos atidėjimo sąskaitos numerį. Numatytoji vertė yra iš atidėjimų **numatytųjų reikšmių** puslapio.</p><p>Šis laukas **galimas** **·** **tik** tada, kai nuolaidos atidėjimo pasirinkties laukas nustatytas į Atskirti nuolaidos grafiką įplaukų ir išlaidų atidėjimų parametrų puslapyje, o eilutei taikoma nuolaida.</p> |
| Pripažinimo sąskaita | <p>Nurodyti nuolaidos atpažinimo sąskaitos numerį. Numatytoji vertė yra iš atidėjimų **numatytųjų reikšmių** puslapio.</p><p>Šis laukas **galimas** **·** **tik** tada, kai nuolaidos atidėjimo pasirinkties laukas nustatytas į Atskirti nuolaidos grafiką įplaukų ir išlaidų atidėjimų parametrų puslapyje, o eilutei taikoma nuolaida.</p> |
| Pradinio pripažinimo sąskaita | <p>Pasirinkti pradinio nuolaidos atpažinimo sąskaitą. Numatytoji vertė yra iš atidėjimų **numatytųjų reikšmių** puslapio.</p><p>Šis laukas galimas tik tada **, kai lauko Atidėjimo** **·** **registravimo būdas puslapyje Įplaukos ir išlaidų atidėjimų parametrai nustatyta kaip Pelnas ir nuostolis**, o eilutei taikoma nuolaida.</p> |
| Pripažinimo korespondentinė sąskaita | <p>Pasirinkite korespondentinės įplaukų pripažinimo sąskaitą. Numatytoji vertė yra iš atidėjimų **numatytųjų reikšmių** puslapio.</p><p>Šis laukas galimas tik tada **, kai lauko Atidėjimo** **·** **registravimo būdas puslapyje Įplaukos ir išlaidų atidėjimų parametrai nustatyta kaip Pelnas ir nuostolis**, o eilutei taikoma nuolaida.</p> |
| **Sąskaitos – Suvartojimas** | Šis skyrius rodomas tik atidėtų prekių atveju. Jis paslėptas atidėtų mokesčių mokėjimo metu. |
| Atidėjimo sąskaita | <p>Nurodyti suvartojimo atidėjimo sąskaitos numerį.</p><p>Standartinių produktų sukurti du atidėjimo grafikai:</p><ul><li>**Standartinis pardavimas** – įplaukų grafikas, kuriame yra kredito balansas. Šiuo atveju pasirinkite suvartojimo atidėjimo sąskaitą.</li><li>**Suvartojimas** – suvartojimas (parduotų prekių savikainos \[PPS\]) išlaidų grafikas, kuriame yra debeto balansas. Šiuo atveju pasirinkite suvartojimo atpažinimo sąskaitą.</li></ul><p>Užregistrus SF, suvartojimo suma registruojama nurodytame suvartojimo atidėjimo sąskaitoje. Šie laukai aptarnavimo prekėms negalimi.</p> |
| Pripažinimo sąskaita | Nurodyti suvartojimo atpažinimo sąskaitos numerį. |
| Pradinio pripažinimo sąskaita | <p>Nurodyti pirminės suvartojimo atpažinimo sumos sąskaitą. Numatytoji vertė yra iš atidėjimų **numatytųjų reikšmių** puslapio.</p><p>Šis laukas galimas tik tada, kai **lauko Atidėjimo registravimo** **·** **būdas puslapio Įplaukos ir išlaidų atidėjimai parametrai nustatyta kaip Pelnas ir nuostoliai.**</p> |
| Pripažinimo korespondentinė sąskaita | <p>Nurodyti sąskaitą suvartojimui pripažinti korespondentinę sumą. Numatytoji vertė yra iš atidėjimų **numatytųjų reikšmių** puslapio.</p><p>Šis laukas galimas tik tada, kai **lauko Atidėjimo registravimo** **·** **būdas puslapio Įplaukos ir išlaidų atidėjimai parametrai nustatyta kaip Pelnas ir nuostoliai.**</p> |
| **Planuoti** | |
| Grafiko tipas | <p>Pasirinkti atidėjimų grafiko tipą: tiesiogiai **eilutė** (numatytoji) arba **pagrįstas įvykiu**.</p><p>Pasirinktys, rodomos puslapyje, yra pagrįstos jūsų pasirinktu atidėjimo grafiko tipu.</p><p>Jei numatytasis šablonas nustatytas **operacijos eilutės atidėjimo** numatytųjų parametrų puslapyje, atidėjimo grafiko tipas remiasi pasirinkto šablono tipu.</p> |
| **Grafikas – tiesiogiai suplanuota** | |
| Konsoliduoti ankstesnius laikotarpius | <p>Nurodykite, ar norite konsoliduoti ankstesnių laikotarpių atidėjimo grafiko eilutes:</p><ul><li>**Taip** – konsoliduoti ankstesnių laikotarpių atidėjimo grafiko eilutes.</li><li>**Ne** – ne konsoliduokite ankstesnių laikotarpių atidėjimo grafiko eilučių.</li></ul><p>Numatytoji vertė yra iš parametrų **puslapio Įplaukos ir išlaidų atidėjimai**.</p> |
| Vieno laikotarpio lygu | <p>Nurodykite, ar dienų skaičius kiekviename laiko periode yra lygus ar skiriasi pagal laikotarpį:</p><ul><li>**Taip** – kiekvienas laikotarpis turi tokį patį dienų skaičių.</li><li>**Ne** – laikotarpių skaičius vienodas.</li></ul><p>Kai ši pasirinktis nustatyta **kaip Ne**, skaičiuojant kiekvieno atidėjimo grafiko laikotarpio sumą atsižvelgiama į laikotarpio dienų skaičių.</p><p>Numatytoji vertė yra iš parametrų **puslapio Įplaukos ir išlaidų atidėjimai**.</p> |
| Grafikas iš šablono | <p>Nurodykite, ar atidėjimo grafikas sukurtas pagal šabloną, ar pabaigos datą:</p><ul><li>**Taip** – atidėjimo grafikas sukurtas pagal šabloną.</li><li>**Ne** – atidėjimo grafikas sukurtas pagal pabaigos datą.</li></ul> |
| Šablonas | Pasirinkite atidėjimo šabloną. |
| Nepaisymo pradžios data | <p>Nurodykite, ar norite nepaisyti pradžios datos:</p><ul><li>**Taip** – nepaisyti pradžios datos su data, kurią įvedate lauke **Pradžios** data.</li><li>**Ne** – pradžios data yra numatytoji **atidėjimo** pradžios datos taisyklė, taikoma SF datai, nurodytai registravimo **SF** puslapyje. Šią taisyklę galima nustatyti puslapyje **Įplaukų ir išlaidų atidėjimai**.</li></ul> |
| Atidėjimo pradžios data | Nurodyti atidėjimo pradžios datą. Operacijos data yra numatytoji vertė. |
| Atidėjimo pabaigos data | <p>Atidėjimo pabaigos data.</p><p>Ši data automatiškai apskaičiuojama remiantis atidėjimo šablonu. Jei šablonas neparinktas, datą turite įvesti rankiniu būdu.</p> |
| **Grafikas – pagrįstas įvykiu** | |
| Šablonas | <p>Pasirinkite įvykio šabloną. Šis laukas nėra būtinas.</p><p>Jei pasirenkate šabloną, šablono vertės perrašo visas įvykiais pagrįstus duomenis ir įvykio eilutes.</p> |
| Paskirstymo tipas | <p>Pasirinkite įvykio eilučių paskirstymo tipą:</p><ul><li>**Kintamos** sumos – kiekvienoje eilutėje įvedama konkreti paskirstymo suma.</li><li>**Vienodos** sumos – suma vienodai paskirstoma kiekvienoje eilutėje.</li><li>**Procentas** – suma paskirstoma remiantis procentine verte, kuri įvedama kiekvienai eilutei.</li><li>**Baigimo procentas** – kiekvienai eilutei įvedama kaupiamoji užbaigimo vertė.</li><p>**Kintamas** kiekis – kiekvienai eilutei įvedamas konkretus paskirstymo kiekis.</li></ul><p>**Pastaba.** Jei norite pasirinkti baigimo **procentą**, datos turi būti didėjančia tvarka.</p> |
| **Sukurti atskirus įvykius vienam vienetui** | |
| Aprašymas | <p>Nurodykite, ar norite atskirti įvykius pagal vienetus:</p><ul><li>**Taip** – atskirkite įvykio eilutes, kad kiekvienam kiekiui būtų viena eilutė.<p>Pavyzdžiui, yra trys įvykio eilutės, o SF – keturi. Šiuo atveju gautame atidėjimo grafike yra 12 eilučių.</p></li><li>**Ne** – neatskirkite įvykio eilučių.</li></ul> |
| Galiojimo pabaigos sąskaita | <p>Pasirinkite sąskaitą, kuri naudojama atpažintoms eilutėms, kurių galiojimo laikas pasibaigęs. Galite pasirinkti sąskaitą sukūrę atidėjimų grafiką.</p><p>Jei yra nustatyta įvykio galiojimo data, atpažinimo proceso metu atpažinimo suma eina į galiojimo pabaigos sąskaitą, o ne į atpažinimo sąskaitą.</p> |
| **Grafikas – įvykiais grindžiamos eilutės** | |
| Aprašymas | Įvykio aprašymas. |
| Atidėjimo pabaigos data | <p>Pasirinkite įvykio pabaigos datą.</p><p>**Pastaba:** jei pasirinksite pabaigos datą, galiojimo **datos laukas** bus išvalytas. Pabaigos ir galiojimo datų naudoti negalima.</p> |
| Galiojimo data | <p>Pasirinkite įvykio galiojimo datą.</p><p>**Pastaba:** jei pasirinksite pabaigos datą, galiojimo **datos laukas** bus išvalytas. Pabaigos ir galiojimo datų naudoti negalima.</p> |
| Kiekis | <p>Nurodyti paskirstymo kiekį. Numatytoji visų eilučių vertė yra **0** (nulis). Jei atnaujinsite kiekį, bendras visų eilučių kiekis turi būti lygus pardavimo užsakymo eilutės prekės kiekiui arba mažesnis.</p><p>Šis laukas galimas tik tada, kai **paskirstymo tipo** lauke nustatyta Kintamas kiekis.**·**</p><p>Jei pardavimo užsakymo eilutės prekės kiekis pakeičiamas taip, kad jis mažesnis už pradinį kiekį, ir sukuriama SF, sukuriama mažiau įvykio eilučių. Bendras paskirstytas kiekis neviršija kiekio, nurodyto sukurtame pardavimo užsakyme arba sąskaitų pateikimo grafike.</p> |
| Paskirstymo procentas | <p>Nurodyti paskirstymo procentinę dalį. Jei nustatytas **lauko Paskirstymo** tipas procentas arba **Baigimo** **procentas**, galite neautomatiniu būdu įvesti procentą. Kitu atveju jis apskaičiuojamas automatiškai.</p><p>Jei lauke **Paskirstymo tipas** nustatyta procentinė **išraiška**, bendroji procentų suma turi būti lygi 100.</p> |
| Suma | <p>Nurodyti paskirstymo sumą. Jei paskirstymo **tipo laukas** nustatytas kaip Kintamos **sumos arba** **Baigimo procentas**, sumą galite įvesti rankiniu būdu.</p><p>Jei lauke **Paskirstymo tipas** nustatyta baigimo **procentinė išraiška**, o sumą įvedate čia, **automatiškai apskaičiuojama** baigimo procento lauko vertė.</p><p>Dėl apvalinimo apskaičiuota suma gali ne tiksliai atitikti tai, kas įvesta neautomatiniu būdu. Jei jums reikia tikslaus kiekio, nustatykite paskirstymo **tipo lauką** kintamos **sumos**.</p> |
| Užbaigimo procentinė dalis | <p>Nurodyti baigimo procentus. Vertė turi būti nuo 0 (nulio) iki 100.</p><p>Šis laukas galimas tik tada, kai **paskirstymo** tipo lauke nustatyta baigimo **procentinė išraiška**.</p> |
| Užbaigimo suma | <p>Apskaičiuota visų atidėjimo grafiko eilučių suma.</p><p>Jei nustatytas **baigimo** procento paskirstymo **tipo laukas**, sumą galite įvesti rankiniu būdu. Šiuo atveju, baigimo procento **lauko** vertė apskaičiuojama pagal jūsų įveda sumą.</p><p>Dėl apvalinimo apskaičiuota suma gali ne tiksliai atitikti tai, kas įvesta neautomatiniu būdu.</p><p>Šis laukas galimas tik tada, kai **paskirstymo** tipo lauke nustatyta baigimo **procentinė išraiška**.</p> |
| Atpažinti paštu | <p>Nurodyti, ar eilutė automatiškai atpažįstama iš karto, kai tik užregistruojama operacija:</p><ul><li>**Pasirinkta** – eilutė automatiškai atpažįstama iš karto, kai tik operacija užregistruojama.</li><li>**Išvalyta** – eilutė neatpažįstama iš karto, kai tik operacija užregistruojama.</li></ul> |
| Pripažinimo sąskaita | <p>Nurodyti įvykio atpažinimo sąskaitą, jei sąskaita skiriasi nuo sąskaitos, naudojamos visam atidėjimo grafikui.</p><p>Šį lauką galite naudoti kartu su pasirinktimi **Atpažinti ir registruoti**.</p> |
