---
title: Atsiskaitymo grafikų kūrimas
description: Šiame straipsnyje paaiškinama, kaip kurti, naikinti ir redaguoti atsiskaitymo grafikus.
author: JodiChristiansen
ms.date: 02/09/2022
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
ms.openlocfilehash: 1248799f92dc6cbce8528a53cc8a3012d2a67b3c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903398"
---
# <a name="create-billing-schedules"></a>Atsiskaitymo grafikų kūrimas

[!include [banner](../includes/banner.md)]

Atsiskaitymo grafiko **puslapyje** galite kurti, naikinti arba redaguoti atsiskaitymo grafikus. Taip pat galite peržiūrėti atsiskaitymo grafikų sąrašą. Kai kuriate atsiskaitymo grafiką, numatytosios jo vertės nustatomos pagal su juo susietą atsiskaitymo grupę. Papildoma informacija nustatoma periodinių sutarties **atsiskaitymo parametrų** puslapyje.

## <a name="create-a-billing-schedule"></a>Kurti atsiskaitymo grafiką

Norėdami kurti atsiskaitymo grafiką, atlikite šiuos veiksmus.

1. Atsiskaitymo grafiko **puslapyje** pasirinkite **Naujas**.
2. Dialogo lange **Kurti atsiskaitymo grafiką**, lauke **Atsiskaitymo grafiko grupė** pasirinkite atsiskaitymo grafiko grupę.
3. **Kliento sąskaitos lauke** pasirinkite kliento sąskaitą.
4. **Lauke Pradžios data** pasirinkite pradžios datą, tada laikotarpių **skaičiaus lauke** įveskite laikotarpių skaičių. Pabaigos **datos** laukas atnaujinamas pagal įvedamų laikotarpių skaičių. Jei atnaujinsite **lauką Atsiskaitymo pabaigos data**, laikotarpių **skaičius bus** atnaujintas į **0** (nulį).
5. Pasirinkite **Gerai**.
6. Atsiskaitymo grafiko **puslapio skirtuko** **Bendra lauke** **Aprašo įveskite atsiskaitymo grafiko aprašymą.**
7. Rodyklės **šablono** lauke, pasirinkite rodyklės šabloną rodyklės **atsiskaitymui**.

Tokie laukai kaip **SF kodas** **ir valiutos** kodas yra atnaujinami kliento informacija.

Atsižvelgiant **į pasirinktą** atsiskaitymo grafiko **grupę, automatiškai nustatomi atsiskaitymo dažnumo ir atsiskaitymo intervalo** laukai.

8. Norėdami sukurti atskiras SF, atskirai nustatykite **parinktį SF** kaip **Taip**.
9. Norėdami automatiškai atnaujinti sąskaitų pateikimo grafiką pasibaigus paskutiniam atsiskaitymo laikotarpiui, **·** **nustatykite parinktį Atnaujinti automatiškai į Taip**, tada nustatykite eilutes, **kad būtų galima įtraukti atnaujinimo lauką.**

Laukai **Parametrai** nustatomi automatiškai, remiantis periodinės sutarties atsiskaitymo parametrų **puslapio vertėmis**.

10. Norėdami sumažinti atsiskaitymo grafiko sumą, nustatykite dalinių laikotarpių **parinktį** **Taip**.
11. Norėdami sulygiuoti atsiskaitymo grafiko informacijos eilutes su mėnesio pabaiga, nustatykite parinktį Lygiuoti **kaip mėnesį** kaip **Taip**.
12. **Sutarties pradžios datos ir** **sutarties pabaigos datos** laukuose įveskite sutarties pradžios ir pabaigos datas. Šios datos tinka tik informacijai.

**Mokėjimo** lauke rodoma kliento mokėjimo informacija iš kliento. Kai eilutės elementas sulaikytas arba nutrauktas, mokėjimo informacijos pakeisti negalima.

> [!NOTE]
> Kai konsoliduojate SF pagal prekę, turi **sutapti** **mokėjimo** sąlygų, metodo **ir atsiskaitymo grafiko** laukų vertė. Kitu atveju SF negalima konsoliduoti.

13. Skirtuke **Adresas** galite peržiūrėti ir atnaujinti laukus Pristatymo **adresas ir** Sąskaitą **pagal adresą**.
14. Skirtuke **Kontaktinė** informacija galite susieti galutinio vartotojo abonementą su atsiskaitymo grafiku.
15. Kontaktinės **informacijos laukuose** galite įvesti kontaktą, el. pašto adresą ir interneto adresą.
16. Norėdami sekti partnerio komisinių informaciją, nustatykite laukus **Partnerio** sąskaita **ir Partnerio komisinių koeficientas**. Šie laukai skirti tik informacijai.
17. Skirtuke **Bendra** galite peržiūrėti įvairias sumas, apskaičiuotas atsiskaitymo grafikui.
18. Skirtuke **Sulaikyta** galite peržiūrėti audito informaciją apie tai, kada atsiskaitymo grafikas buvo sulaikytas, kai sulaikymas buvo pašalintas.
19. Skirtuke **Nutraukimas** galite peržiūrėti atleidimo retrospektyvą, kuri buvo pritaikyta sąskaitų pateikimo grafikui arba iš jo pašalinta.
20. Pasirinkite **Įrašyti**.
21. Atsiskaitymo grafiko **eilutėse "** FastTab" pasirinkite **Įtraukti eilutę**.
22. **Lauke Prekės numeris** pasirinkite prekės numerį. Jei įtraukiama prekė yra pirminė įplaukų skaidymo prekė, eilutės automatiškai atnaujinamos naudojant antinamas prekes. Išskaidytoje įplaukoje galite redaguoti tik pirminę prekę. Tada visos antriniai prekės atitinkamai atnaujinamos.
23. **Lauke Prekės tipas** pasirinkite prekės tipą.
24. Atnaujinkite pradžios ir pabaigos datas.
25. Prieš sukurdami SF, galite pakeisti atsiskaitymo dažnumą atnaujindami lauką **Atsiskaitymo** dažnumas. Sukūrus pirmą atsiskaitymo grafiko SF, atsiskaitymo dažnumo keisti negalima.
26. **Lauke Vienetas** pasirinkite prekės matavimo vienetą.
27. **Lauke Kainos metodas** pasirinkite prekės kainodaros metodą.

Automatiškai **nustatomas** atsargų laukas Vieneto kaina. Tačiau jį galite atnaujinti, jei pakeičiate kainos metodą į **Butas**.

## <a name="remove-a-line-item"></a>Prekės eilutės pašalinimas

Norėdami pašalinti prekę iš atsiskaitymo grafiko, atlikite šiuos veiksmus.

1. Atsiskaitymo grafiko **puslapio** lauke Grafiko **numeris** pasirinkite norimą redaguoti atsiskaitymo grafiko numerį.
2. Atsiskaitymo grafiko **eilutėse** "FastTab" pasirinkite eilutę, norimą naikinti, tada pasirinkite **Pašalinti**.
3. Pasirinkite **Įrašyti**.

Likusioje šio straipsnio dalyje aprašomi veiksmai ir informacija, kurie galimi eilučių atsiskaitymo grafiko **eilutėse "** FastTab".

## <a name="billing-schedule-line-actions"></a>Atsiskaitymo grafiko eilutės veiksmai

Atsiskaitymo grafiko eilučių **"** FastTab" mygtukai leidžia taikyti veiksmus atskiroms eilutėms.

| Mygtukas | Aprašymas |
|--------|-------------|
| Įtraukti eilutę | Įtraukite eilutę į atsiskaitymo grafiką. |
| Įtraukti iš elementų sąrašo | Įtraukite keletą prekių į atsiskaitymo grafiką, pasirinkdami juos sąraše. |
| Šalinti | <p>Pašalinti pasirinktą eilutę iš atsiskaitymo grafiko.</p><p>Prekėms, kurios yra įplaukų skaidymo dalis, galima pašalinti tik pirminę prekę. Visos susietos antriniai prekės automatiškai pašalinamos.</p> |
| Peržiūrėti išsamią atsiskaitymo informaciją | Peržiūrėkite išsamią atsiskaitymo informaciją. |
| Atleisti | <p>Atleisti pasirinktas eilutes. Šis mygtukas galimas tik tada, kai pasirinktų eilučių būsena yra **Aktyvi**.</p><p>Prekėms, kurios yra įplaukų skaidymo dalis, galima atleisti tik pirminę prekę.</p> |
| Pašalinti nutraukimą | <p>Pašalinti nutraukimą iš pasirinktų eilučių. Šis mygtukas galimas tik tada, kai pasirinktų eilučių būsena yra **Atleista**.</p><p>Prekių, kurios yra įplaukų skaidymo dalis, nutraukimą galite pašalinti tik iš pirminės prekės.</p> |
| Vietos sulaikymas | <p>Pasirinkite išsamią informaciją apie pasirinktos eilutės sulaikymas.</p><p>Prekėms, kurios yra įplaukų skaidymo dalis, galite sulaikyti tik pirminę prekę.</p> |
| Pašalinti sulaikymą | <p>Pašalinti sulaikymas iš pasirinktos eilutės.</p><p>Prekių, kurios yra įplaukų skaidymo dalis, sulaikymas galima pašalinti tik iš pirminės prekės.</p> |
| Perskyrimo ir nuolaida | Šis mygtukas negalimas prekėms, kurios yra įplaukų skaidymo dalis, išskyrus pirmines prekes, kurių įplaukų skaidymo metu naudojamas **nulinės sumos** paskirstymo metodas. |
| Atidėjimai | <p>Įvesti pasirinktos eilutės atidėjimo pasirinktis.</p><p>Šis mygtukas negalimas suskaidytoms pirminėms prekėms.</p> |
| Etapo paskirstymas | <p>Peržiūrėkite ir atnaujinkite pasirinktos eilutės rodyklės paskirstymo informaciją.</p><p>Šis mygtukas galimas tik tada, kai atsiskaitymo grafiko eilutės elementas yra rodyklės elementas.</p> |
| Palaikymas ir atnaujinimas | <p>Peržiūrėkite ir atnaujinkite pasirinktos eilutės palaikymo ir atnaujinimo informaciją.</p><p>Šis mygtukas galimas tik tada, kai atsiskaitymo grafiko eilutės elementas yra palaikymo arba atnaujinimo prekė.</p> |
| Rodyti dimensijas | Rodyti arba slėpti dimensijų stulpelius, kurie rodomi atsiskaitymo grafiko **eilučių tinklelyje**. |
| Apskaičiuoti vieneto kainą | <p>Apskaičiuokite prekės vieneto kainą, kad klientas galėtų mokėti sutarties sumą įmokas (pvz., kas dieną, kas mėnesį, ketvirtį, kas pusmetį arba kasmet). Galite pasirinkti sutarties kainą ir kainos dažnį.</p><p>Galite peržiūrėti pakeitimų žurnalo sekimą: seną sutarties kainą ir dažnį, naują sutarties kainą ir dažnį, pakeitimą atliekantį vartotoją, pakeitimo datą ir laiką.</p> |
| Derinimo data | <p>Nurodykite atnaujinimo prekių lygiavimo datą.</p><p>Jei prekių grupę pasirenkate **lauke Prekių** grupė, visos prekės naudoja sąskaitų pateikimo grafike esančio prekių grupės pirmojo elemento lygiavimo datą. Jei prekių **grupės laukas** yra tuščias, galite nurodyti lygiavimo datą, kuri bus naudojama visoms prekėms.</p><p>Šis mygtukas galimas tik tada, kai **laukas Atsiskaitymo** dažnumas nustatytas kaip **Metinis**.</p> |
| Neapmokėtos įplaukos | <p>Nustatyti prekę, kad būtų galima naudoti neap sf įplaukų funkciją. Tada galima nurodyti prekių įplaukas, kurių sf neišduotos, ir neįskaitytą nuolaidą.</p><p>Šis mygtukas galimas tik toms prekėms **, kurių prekės** tipo laukas nustatytas kaip **Standartinis**. Nėra esamų atsiskaitymo grafikų arba atsiskaitymo grafiko eilučių, kuriose SF jau sukurta.</p> |
| Įtraukti antrinę įplaukų dalį | <p>Pasirinkite iš antrinių prekių įtraukti į pardavimo užsakymą.</p><p>Šis mygtukas galimas tik su pirminiais elementais, išskaidytais iš įplaukų.</p> |
| Išankstinės kainos parinktys | Redaguokite prekės kainos pasirinktis. |

## <a name="billing-schedule-line-details"></a>Atsiskaitymo grafiko eilutės informacija

Kai pasirenkate eilutę atsiskaitymo grafiko **eilutėse "** FastTab", galite peržiūrėti konkrečią tos eilutės informaciją. Išsami informacija yra padalinta į skirtingus skirtukus.

### <a name="general-tab"></a>Skirtukas Bendra

Toliau pateikiama informacija yra skirtuke **Bendra**.

| Laukas arba skyrius | Aprašymas |
|------------------|-------------|
| Naudojimas | <p>Šiame skyriuje pateikiama informacija apie prekių naudojimą. Jame yra šie laukai:</p><ul><li>**Naudojimo identifikatorius** – skaitiklio arba naudojimo prekės identifikatorius.</li><li>**Skaitymo pasirinktis** – naudojimo skaitymo pasirinktis: **skaitymas** arba **suvartojimas**.</li><li>**Įvertintas suvartojimas** – nurodyti įvertintą naudojimo prekės, kuri turi laikotarpių, kai SF nesukurta, suvartojimą. Informacijos puslapyje **Atsiskaitymo** informacija galite peržiūrėti įvertinto suvartojimo atsiskaitymo informacijos eilutes.</li></ul> |
| Išorinės nuorodos\* | Šiame skyriuje yra išorinių **ir** **eilučių numerių** laukai, kuriuose galite nurodyti išorinių nuorodų informaciją. |
| Rodyklė | <p>Šiame skyriuje pateikiama informacija apie rodyklės elementus. Joje yra laukas **Numatoma baigimo** data, kuris parodo prekės užbaigimo datą.</li></ul> |
| Tekstas | Eilutės komentaras. Tekstas išverstas į numatytąją kliento arba juridinio subjekto kalbą. |
| Prekių grupė | Eilutės prekės grupė. |
| Derinimo data | Atsiskaitymo grafiko lygiavimo data. |

\* Kai konsoliduojate SF pagal prekę puslapyje **Generuoti SF**, turi sutapti **išorinių** nuorodų laukai. Jei skiriasi net vienas simbolis, prekės sąskaitoje faktūroje nebus konsoliduotos. Išorinių nuorodų skyriaus bet kuris **laukas** nėra tikrinamas, o eilutės numerio **lauko** vertė turi būti teigiamas skaičius.

### <a name="address-tab"></a>Adreso skirtukas (pavadinimas)

Skirtuke Adresas galima rasti **šią** informaciją.

| Laukas | Aprašymas |
|-------|-------------|
| Pristatymo adresas | <p>Pasirinkti eilutės elemento pristatymo adresą. Numatytasis pristatymo adresas yra pagrindinis pristatymo adresas iš adreso **"** FastTab".</p><p>Kai keičiate adresą, galite pasirinkti šias adreso pasirinktis:</p><ul><li>**Adresai** – pasirinkti dabartinio kliento adresą.</li><li>**Naudojamas** – pasirinkite adresą, kuris šiuo metu naudojamas dabartiniam klientui.</li><li>**Kitas adresas** – pasirinkite bet kurio kliento įrašo adresą.</li></ul><p>Galima redaguoti tik prekių, kurios naudoja įplaukų skaidymo, pirminės prekės adresą. Antrinių prekių adresas sutampa su pagrindinio objekto adresu ir negali būti redaguojamas atskirai.</p> |
| Sąskaitos, į kurį reikia adrese, | <p>Pasirinkite eilutės elemento sąskaitos, į kurį reikia kreiptis, adresą. Numatytasis pristatymo adresas yra pagrindinis pristatymo adresas iš adreso **"** FastTab". Jei reikia, adresą galite keisti pagal galimų adresų tikslą:</p><ul><li>Jei nė vienas iš adresų neturi SF **paskirties**, numatytasis kliento adresas yra pagrindinis kliento adresas, nepaisant paskirties.</li><li>Jei vienas ar daugiau adresų turi SF **paskirtį**, numatytasis paskirties adresas yra paskutinis įvestas adresas.</li><li>Jei vienas ar **daugiau** adresų turi SF paskirtį, o vienas iš SF adresų nustatytas kaip pagrindinis adresas, numatytasis sąskaitos faktūros adresas yra adresas, **kuris** turi SF paskirtį ir yra nustatomas kaip pagrindinis adresas.</li><li>Galima redaguoti tik prekių, kurios naudoja įplaukų skaidymo, pirminės prekės adresą. Antrinių prekių adresas sutampa su pagrindinio objekto adresu ir negali būti redaguojamas atskirai.</li></ul> |

### <a name="product-tab"></a>Skirtukas Produktas

Skirtuke Produktas galima rasti šią **informaciją**.

| Laukas arba skyrius | Aprašymas |
|------------------|-------------|
| Saugojimo dimensijos | <p>Šiame skyriuje rodoma prekės saugojimo informacija. Jame yra **serijos numerio** laukas, kuriame rodomas prekės serijos numeris.</p><p>Serijos numeris kopijuojamas iš pradinio pardavimo užsakymo vykstant palaikymo ir atnaujinimo procesui. Prekių, kurios naudoja įplaukų skaidymo naudojimą, pirminės prekės serijos numeris nukopijuojamas į visas ant jų naudojamas prekes. Serijos numeris kopijuojamas, kai parinktis **Kopijuoti serijos numerį** nustatyta kaip **Taip** periodinio **sutarties atsiskaitymo parametrų** puslapyje.</li></ul> |
| Produktų dimensijos | Prekės produkto informacija ir vertės atnaujinamos automatiškai, remiantis **varianto numerio** verte, pasirinkta atsiskaitymo grafiko eilutei. |

### <a name="account-tab"></a>Skirtukas Sąskaita

Skirtuke Sąskaita galima ši **informacija**.

| Laukas | Aprašymas |
|-------|-------------|
| Pagrindinė sąskaita | Pardavimo eilutėje sukurta pagrindinė sąskaita. Numatytoji vertė yra iš pardavimo užsakymo. Šis laukas gali būti tuščias. |
| Prekės finansinės dimensijos | <p>Numatytosios finansinės dimensijos reikšmės, pagrįstos kliento ir prekės įrašu.</p><p>Prekėms, kurios naudoja įplaukų skaidymas, antrinių prekių finansinės dimensijos vertes naudoja kliento ir prekių įrašų finansinės dimensijos vertės, kaip aprašyta anksčiau. Jei turite atnaujinti antrinių prekių finansinių dimensijų vertes, galite importuoti duomenų objektą.</p> |

### <a name="renewals-tab"></a>Skirtukas Atnaujinimai

Toliau pateikta informacija yra atnaujinimo **skirtuke**.

| Laukas | Aprašymas |
|-------|-------------|
| Atnaujinti automatiškai | <p>Vertė, nurodanti, ar atsiskaitymo grafiko eilutė automatiškai atnaujinama per kitą atsiskaitymo laikotarpį:</p><ul><li>**Taip** – kuriant SF automatiškai atnaujinama kito atsiskaitymo laikotarpio atsiskaitymo grafiko eilutė.</li><li>**Ne** – atsiskaitymo grafiko eilutė nėra automatiškai atnaujinama. Turite rankiniu būdu atnaujinti atsiskaitymo grafiką.</li></ul> |
| Eilutės, kurias reikia įtraukti vienam atnaujinimui | Eilučių, kurias reikia įtraukti į atsiskaitymo grafiko atnaujinimą, skaičius. |

Be to, skirtuke Atnaujinimai galima rasti šiuos **mygtukus**.

| Mygtukas | Aprašymas |
|--------|-------------|
| Įplaukų, už kurias neišrašytos sąskaitos, žurnalo įrašo auditas | Peržiūrėti visus prekių, kurios naudoja sf įplaukų funkciją, pakeitimus. |
| Įtraukti atnaujinimo terminą | Įtraukite prekės atnaujinimo terminą. Naujo atnaujinimo termino pradžios data yra kita data, kuri yra po ankstesnio termino pabaigos datos. Galima **atnaujinti atnaujinimo pabaigos** datą, **atidėjimo** pradžios datą **,** atidėjimo **pabaigos** datą, **prekių** kiekį ir vieneto kainą. |
| Keisti atnaujinimo terminą | <p>Modifikuokite atnaujinimo terminą. Galite keisti pradinio laikotarpio atidėjimo pradžios ir pabaigos datas prieš sukurdami pradinį žurnalo įrašą. Vėlesnių sąlygų pradžios datos keisti negalima. Tai visada yra kita data po ankstesnės termino pabaigos.</p><p>Jei atnaujinimo terminas egzistuoja po termino, kurį modifikuojate, termino datų pakeisti negalima. Tokiu atveju gali būti atnaujinti tik **atnaujinamos** **prekės** kiekio ir vieneto kainos laukai.</p><p>Pvz., yra trys terminai. <ul><li>Pirmosios sąlygos pakeisti negalima, nes ji jau pradėta.</li><li>Antrą terminą galima keisti tik kiekį ir vieneto kainą.</li><li>Trečios sąlygos visos vertės, išskyrus pradžios datą, gali būti keičiamos. Be to, šablono **pasirinktis** Grafikas leidžia sukurti atidėjimo grafiką, pagrįstą nerašyto įplaukų elemento šablonu. Kai ši pasirinktis nustatyta į **Taip**, pasirinkite atidėjimo **šabloną** lauke Šablonas ir pakeiskite atidėjimo pradžios ir pabaigos datas, jei to reikalaujate. Vėlesniuose atnaujinimo sąlygose naudojamas tas pats atidėjimo šablonas. Tačiau atidėjimo šabloną galima keisti.</p></li></ul> |

### <a name="termination-tab"></a>Skirtukas Nutraukimas

Ši informacija prieinama skirtuke **Nutraukimas**.

| Laukas | Aprašymas |
|-------|-------------|
| Atleidimo data | Data, kai buvo nutraukta atsiskaitymo grafiko eilutė. Numatytoji vertė yra iš antraštės **lauko** Atleidimo data. Jei reikia, vertę galite pakeisti. |
| Nutraukimo tipas | Atleidimo tipas. Numatytoji vertė yra iš antraštės **lauko** Atleidimo tipas. |

### <a name="hold-tab"></a>Skirtukas Sulaikyti

Jei naudojami įplaukų ir išlaidų atidėjimai, skirtuke **Sulaikyta** rodoma atidėjimo data.

### <a name="escalation-and-discount-tab"></a>Perskyrimo ir nuolaidos skirtukas

Ši informacija yra perskyrimo ir **nuolaidos skirtuke**.

| Laukas | Aprašymas |
|-------|-------------|
| Perskyrimas | <p>Pasirinkite, ar leidžiami sąskaitų pateikimo grafiko eilutės perskyrimai. Sukūrus atsiskaitymo grafiko eilutę, taikoma bet kuri perskyrimo eilutė iš antraštės.</p><ul><li>**Taip** – perskyrimus galima taikyti eilutei. Kai ši parinktis pasirinkta, galite nustatyti sąskaitų pateikimo grafiko eilučių perskyrimą **perskyrimo ir nuolaidos** puslapyje.</li><li>**Ne** – perskyrimų negalima taikyti eilutei.</li></ul><p>Numatytasis parametras pagrįstas pasirinkta **atsiskaitymo grafiko** grupe.</p> |

### <a name="price-changes-tab"></a>Skirtukas Kainos keitimai

Eilučių, kurios pakeistos iš standartinės **kainos** į standartinės **kainos**, tinklelyje, skirtuke **Kainos keitimai**, yra šie stulpeliai:

- Keisti datą
- Pakeitė vartotojas
- Standartinė kaina
- Buto kaina
- Kainos atnaujinimas
