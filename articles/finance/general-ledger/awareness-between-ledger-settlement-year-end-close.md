---
title: Informacijos bendrinimas tarp didžiosios knygos atsiskaitymo ir metų pabaigos uždarymo
description: Šioje temoje pateikiama informacija apie patobulinimus, turinčius įtakos Didžiosios knygos atsiskaitymams ir Didžiosios knygos metų pabaigos uždarymui.
author: kweekley
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: acfbcf1467363262769884063efbc1a6d6e21eb1
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075736"
---
# <a name="awareness-between-ledger-settlement-and-year-end-close"></a>Informacijos bendrinimas tarp didžiosios knygos atsiskaitymo ir metų pabaigos uždarymo

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

„Microsoft“.Dynamics 365 Finance versija 10.0.25, **Supratimas tarp atsiskaitymo knygoje ir uždarymo metų pabaigoje** funkcija pasiekiama **Funkcijų valdymas** darbo vieta. Ši funkcija prideda du pagrindinius patobulinimus, turinčius įtakos DK atsiskaitymui ir didžiosios knygos metų pabaigos uždarymui.

Didžiosios knygos metų pabaigos uždarymo metu apmokėtos knygos operacijos nebebus įtraukiamos į kitų fiskalinių metų pradinį balansą. Šis patobulinimas užtikrina, kad į pradinį balansą būtų įtrauktos tik neapmokėtos knygos operacijos. Tai svarbu, kai vykdomas didžiosios knygos užsienio valiutos perkainojimas. Užsienio valiutos perkainojimas vykdomas tik knygelės operacijoms, kurių būsena yra **Neišspręstas**. Tačiau prieš **Supratimas tarp atsiskaitymo knygoje ir uždarymo metų pabaigoje** funkcija buvo išleista, pradiniame balanse buvo apibendrinti abi operacijos, kurių būsena yra **Įsikūrė** ir tie, kurie turi statusą **Neišspręstas**, o apibendrintos sumos būsena nustatyta į **Neišspręstas**.

Antrasis patobulinimas leidžia paskelbti išsamias pradinio balanso operacijas didžiosios knygos metų pabaigos pabaigoje. Jei **Išsaugokite išsamią informaciją metų pabaigoje** parinktis nustatyta į **Taip**, kiekvienai neapmokėtai knygos operacijai bus sukurtas atskiras pradinis likutis. Šis nustatymas apibrėžiamas kiekvienai pagrindinei sąskaitai DK atsiskaitymų sąrankoje. Išsaugodami išsamias pradinio balanso operacijas, labai pagerinsite galimybę kitais finansiniais metais apmokėti neapmokėtas knygos operacijas.

Siekiant paremti naujus patobulinimus, buvo atlikti DK atsiskaitymo ir metų pabaigos uždarymo pakeitimai.

### <a name="changes-to-ledger-settlement"></a>Atsiskaitymų knygelės pakeitimai

- Didžiosios knygos atsiskaitymas turi būti atliktas per fiskalinius metus.
- Didžiosios knygos atsiskaitymas turi būti atliktas už operacijas vienoje pagrindinėje sąskaitoje. Dabar pagrindinė sąskaita yra būtinas filtras **Didžiosios knygos atsiskaitymas** puslapį.
- Didžiosios knygos atsiskaitymas ir DK atsiskaitymo atšaukimas negali būti atliekami operacijoms, kurios registruojamos per uždarus finansinius metus (kitaip tariant, buvo atliktas metų pabaigos uždarymas).

### <a name="changes-to-year-end-close"></a>Metų pabaigos uždarymo pakeitimai

- Metų pabaigos uždarymas negali būti atšauktas, jei kitais finansiniais metais buvo sumokėtos bet kokios pradinio balanso operacijos. Šis pakeitimas taikomas, kai metų pabaigos uždarymas atšaukiamas arba kai metų pabaigos uždarymas kartojamas ir **Iš naujo uždarydami metus ištrinkite esamus metų pabaigos įrašus** parinktis nustatyta į **Taip** Didžiosios knygos parametruose.
- Jei **Išsaugokite išsamią informaciją metų pabaigoje** parinktis nustatyta į **Taip** bet kuriai balansinei sąskaitai DK atsiskaityme bus sukurtos išsamesnės tos pagrindinės sąskaitos pradinio balanso operacijos.

## <a name="before-you-enable-the-feature"></a>Prieš įjungdami funkciją

Dėl funkcijų ir duomenų modelio pakeitimų, prieš įjungdami funkciją svarbu atsižvelgti į šiuos dalykus:

- Visos operacijos, kurios buvo pažymėtos atsiskaityti, bet nebuvo atsiskaitytos, bus automatiškai panaikintos, kai funkcija įjungta. Kad neprarastumėte darbo, sumokėkite visas pažymėtas operacijas prieš įjungdami funkciją.
- Kai kurios organizacijos vykdo metų pabaigos uždarymą kelis kartus tais pačiais fiskaliniais metais. Neįgalinkite funkcijos, jei metų pabaigos uždarymas jau buvo vieną kartą ir bus paleistas dar kartą tais pačiais finansiniais metais. Ši funkcija turi būti įjungta prieš apdorojant pirmąjį metų pabaigos uždarymą arba apdorojus paskutinį fiskalinių metų uždarymą.

  Jei norite įgalinti funkciją, bet metų pabaigos uždarymas jau buvo vieną kartą, turite pakeisti metų pabaigos uždarymą, kad galėtumėte įjungti funkciją.

- Kadangi atsiskaitymas per fiskalinius metus nebeleidžiamas, rekomenduojame įgalinti funkciją prieš pradedant uždarymo procesą metų pabaigoje. Tada siekiant užtikrinti, kad kitų fiskalinių metų pradžios likučiams įtakos nepadarytų ankstesni atsiskaitymai tarp fiskalinių metų, pradinio balanso sandoris turėtų būti apmokėtas už uždaromus finansinius metus.
- Kadangi atsiskaitymas tarp pagrindinių sąskaitų nebeleidžiamas, koreguokite sąskaitų planą arba procesus pagal poreikį, kad užtikrintumėte, jog atsiskaitymas knygoje gali būti atliekamas toje pačioje pagrindinėje sąskaitoje.
- Šios funkcijos įjungti negalima, jei naudojamas viešojo sektoriaus metų pabaigos uždarymo procesas.

## <a name="set-up-ledger-settlement"></a>Nustatyti DK atsiskaitymą

Kai įgalinate funkciją ir prieš paleidžiant kitą metų pabaigos uždarymą, kiekviena organizacija turi nuspręsti, ar išsaugos išsamią operacijos informaciją metų pabaigos uždarymo metu. Pasirinkimas neturi įtakos pradinio balanso įrašams iš ankstesnių metų pabaigos uždarymo procesų.

The **Išsaugokite išsamią informaciją metų pabaigoje** parinktis nustatyta kiekvienai pagrindinei paskyrai **Didžiosios knygos atsiskaitymų nustatymas** puslapį.

1.  Eiti į **Didžioji knyga** > **Didžiosios knygos nustatymas** > **Didžiosios knygos parametrai**.
2.  Ant **Didžiosios knygos atsiskaitymai** skirtuką, pasirinkite **Didžiosios knygos atsiskaitymo sąskaitos**.

Arba

1.  Eiti į **Didžioji knyga** > **Periodinės užduotys** > **Didžiosios knygos atsiskaitymai**.
2.  Pasirinkite **Didžiosios knygos atsiskaitymo sąskaitos**.

Prie jo buvo pridėti du stulpeliai **Didžiosios knygos atsiskaitymai** puslapis:
    
- **Pagrindinis sąskaitos tipas** – Šis stulpelis skirtas tik informaciniams tikslams. Tai rodo tipą, priskirtą pagrindinei paskyrai.
- **Išsaugokite išsamią informaciją metų pabaigoje** – Pagal numatytuosius nustatymus parinktis nustatyta į **Nr**. Jį galima nustatyti **Taip** tik jei reikšmė **Pagrindinis sąskaitos tipas** stulpelis yra **Balanso lapas**, **·**, arba **Atsakomybė**. Kai parinktis nustatyta į **Nr**, pradiniai likučiai bus paskelbti suvestinėje, kaip įprasta metų pabaigos uždarymo metu. Jei nustatyta **Taip**, pradiniai likučiai bus sukurti išsamiai kiekvienai knygos operacijai, kuri nėra apmokėta pagrindinėje sąskaitoje.

## <a name="year-end-close"></a>Metų pabaigos uždarymas

Kai paleidi metų pabaigą arti eidamas į **Didžioji knyga** > **Laikotarpis uždarytas** > **Metų pabaiga uždaryta**, procesas sukuria pagrindinių sąskaitų pradinius likučius, kurie yra apibrėžti DK atsiskaitymui. Pradiniai likučiai sukuriami suvestinėje arba išsamiai, atsižvelgiant į DK atsiskaitymo sąranką. Į procesą neįtraukiamos pagrindinės knygos operacijos, kurios yra apmokėtos, neatsižvelgiant į tai, ar kiekvienos pagrindinės sąskaitos pradinį likutį registruojate suvestinėje ar išsamiai.

Pavyzdžiui, kelios operacijos paskelbiamos pagrindinėje sąskaitoje 130100 2021 finansiniais metais.

| Žurnalo numeris | Kvitas  | Data       | Tipas      | DK sąskaita | Abonemento pavadinimas        | Aprašymas       | Valiuta | Suma operacijos valiuta | Suma  | Suma, išreikšta ataskaitų valiuta |
|----------------|----------|------------|-----------|----------------|---------------------|-------------------|----------|--------------------------------|---------|------------------------------|
| 20853          | FTV-3000 | 2021-12-03  | Vykdymas | 130100-001-    | Gautinos sumos | Aptarnavimo mokestis       | USD      | 100                            | 100     | 100                          |
| 20855          | FTV-3004 | 2021-12-05  | Vykdymas | 130100-002-    | Gautinos sumos | Komunalinės paslaugos         | USD      | 175                            | 175     | 175                          |
| 20854          | CMV-4000 | 2021-12-16 | Vykdymas | 130100-001-    | Gautinos sumos | Grąžinimas            | USD      | -100                           | -100    | -100                         |
| 20851          | ARP-8000 | 2021-12-20 | Vykdymas | 130100-002-    | Gautinos sumos |                   | USD      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 2021-12-20 | Vykdymas | 130100-002-    | Gautinos sumos |                   | EUR      | -127.11                        | -174.12 | -174.12                      |
| 20856          | CMV-4010 | 2021-12-21 | Vykdymas | 130100-002-    | Gautinos sumos | Kreditas sąskaitoje | USD      | -175                           | -175    | -175                         |
| 20857          | FTV-3011 | 2021-12-28 | Vykdymas | 130100-001-    | Gautinos sumos | Komunalinės paslaugos         | USD      | 400                            | 400     | 400                          |
| 20910          | FTV-3020 | 2021-12-29 | Vykdymas | 130100-002-    | Gautinos sumos | Paslauga           | USD      | 300                            | 300     | 300                          |

Iš šių operacijų trys yra atsiskaitoma DK atsiskaitymo metu.

Yra 175 USD (175 USD) sąskaita. Ši sąskaita buvo apmokėta atsiskaitant eurais (EUR), buvo pritaikyta grynųjų pinigų nuolaida.

| Žurnalo numeris | Kvitas  | Data       | Tipas      | DK sąskaita | Abonemento pavadinimas        | Aprašymas | Valiuta | Suma operacijos valiuta | Suma  | Suma, išreikšta ataskaitų valiuta |
|----------------|----------|------------|-----------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20855          | FTV-3004 | 2021-12-05  | Vykdymas | 130100-002-    | Gautinos sumos | Komunalinės paslaugos   | USD      | 175                            | 175     | 175                          |
| 20851          | ARP-8000 | 2021-12-20 | Vykdymas | 130100-002-    | Gautinos sumos |             | USD      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 2021-12-20 | Vykdymas | 130100-002-    | Gautinos sumos |             | EUR      | -127.11                        | -174.12 | -174.12                      |

Pagrindinės paskyros 130100 rezultatai priklauso nuo to, ar funkcija įjungta prieš uždarant metų pabaigą. Jei funkcija įjungta, rezultatas taip pat priklauso nuo parinkties Išsaugoti išsamią informaciją metų pabaigos uždarymo metu nustatymo.

### <a name="the-feature-isnt-enabled"></a>Funkcija neįjungta
Metų pabaigos uždarymas sukuria tris pagrindinės sąskaitos 130100 pradinio balanso operacijas 2022 m. Operacijų suma apskaitos valiuta yra USD 525.

| Žurnalo numeris | Kvitas  | Data     | Tipas    | DK sąskaita | Abonemento pavadinimas        | Aprašymas | Valiuta | Suma operacijos valiuta | Suma  | Suma, išreikšta ataskaitų valiuta |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-002-    | Gautinos sumos |             | USD      | 299.12                         | 299.12  | 299.12                       |
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-001-    | Gautinos sumos |             | USD      | 400                            | 400     | 400                          |
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-002-    | Gautinos sumos |             | EUR      | -127.11                        | -174.12 | -174.12                      |

Nors mokėjimo operacija už -127,11 EUR buvo apmokėta buhalterinėje knygoje, operacija vis tiek pateikiama kaip pradinis likutis.

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--no"></a>Funkcija įjungta ir Išsaugoti išsamią informaciją metų pabaigoje uždarant = Ne

Metų pabaigos uždarymas sukuria dvi pagrindinės sąskaitos 130100 pradinio balanso operacijas 2022 m. Operacijų suma apskaitos valiuta vis dar yra USD 525, tačiau knygoje apmokėtos operacijos neįtraukiamos į pradinį balansą. Bendra sąskaitos 130100-002- suma yra USD 125, o ne USD 299.12, o operacija už 127,11 EUR / 174,12 USD yra visiškai neįtraukta.

| Žurnalo numeris | Kvitas  | Data     | Tipas    | DK sąskaita | Abonemento pavadinimas        | Aprašymas | Valiuta | Suma operacijos valiuta | Suma | Suma, išreikšta ataskaitų valiuta |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-002-    | Gautinos sumos |             | USD      | 125                            | 125    | 125                          |
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-001-    | Gautinos sumos |             | USD      | 400                            | 400    | 400                          |

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--yes"></a>Funkcija įjungta ir Išsaugoti išsamią informaciją metų pabaigoje uždarant = Taip

Metų pabaigos uždarymas sukuria penkias pagrindinės sąskaitos 130100 pradinio balanso operacijas 2022 m. Kiekvienai iš penkių neapmokėtų operacijų sukuriama atskira pradinio balanso operacija. Operacijų suma apskaitos valiuta vis dar yra USD 525.

| Žurnalo numeris | Kvitas  | Data     | Tipas    | DK sąskaita | Abonemento pavadinimas        | Aprašymas       | Valiuta | Suma operacijos valiuta | Suma | Suma, išreikšta ataskaitų valiuta |
|----------------|----------|----------|---------|----------------|---------------------|-------------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-001-    | Gautinos sumos | Aptarnavimo mokestis       | USD      | 100                            | 100    | 100                          |
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-001-    | Gautinos sumos | Grąžinimas            | USD      | -100                           | -100   | -100                         |
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-002-    | Gautinos sumos | Kreditas sąskaitoje | USD      | -175                           | -175   | -175                         |
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-001-    | Gautinos sumos | Komunalinės paslaugos         | USD      | 400                            | 400    | 400                          |
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-002-    | Gautinos sumos | Paslauga           | USD      | 300                            | 300    | 300                          |

Kai išsaugoma išsami operacijos informacija, pradinės išsamios operacijos neturi įtakos. Jie lieka paskelbti ir nesutvarkyti finansiniais metais, kurie yra uždaromi. Šių operacijų kopija sukuriama pradiniam likučiui. Šios pradinių operacijų reikšmės nukopijuojamos į pradinio balanso operacijas.

- Didžiosios knygos sąskaita (pagrindinė sąskaita ir visi finansiniai aspektai)
- Sumos operacijos, apskaitos ir ataskaitų teikimo valiutomis
- Aprašymas
- Registravimo sluoksnis
- Registravimo tipas

   > [!NOTE]
   > Jokioms kitoms pradinio balanso operacijoms registravimo tipas nepriskirtas. Todėl registravimo tipą galima naudoti norint atskirti išsamiai perkeltas atidarymo operacijas.

Kai kurie laukai iš pradinių operacijų turi būti pakeisti pradinio balanso išsamiose operacijose. Pradinio balanso operacijų data visada yra pirmoji kitų finansinių metų diena. Žurnalo numeris turi pasikeisti, o kvito numeris pasikeis į vertę, kuri buvo įvesta metų pabaigos uždarymo dialogo lange.

Informaciją apie pradinius sandorius galite rasti adresu **Didžiosios knygos atsiskaitymas** puslapį. Kiekviena išsami pradinio balanso operacija rodo **Pradinė sandorio data** stulpelyje tinklelyje. Šis stulpelis gali padėti suderinti operacijas naujais finansiniais metais. Galite pasirinkti **Žiūrėti originalų kuponą** grįžkite į visą originalų kuponą.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Sudengti operacijas
Norėdami sudengti DK operacijas, atlikite toliau nurodytus veiksmus.

1. Eiti į **Didžioji knyga** > **Periodinės užduotys** > **Didžiosios knygos atsiskaitymai**.
2.  Nustatykite filtrus puslapio viršuje.

    1. Pasirinkite datos diapazoną. Arba pasirinkite datos intervalo kodą, kad automatiškai užpildytumėte dienų seką.

       - Dienų seka negali viršyti fiskalinių metų. Jei dienų seka kerta fiskalinius metus, pasirinkus operacijos nebus rodomos **Rodyti operacijas**.
       - Jei dienų seka yra atvirais finansiniais metais, sandoriai gali būti apmokėti ir atsiskaitymas gali būti atšauktas. Jei dienų seka yra uždarais fiskaliniais metais arba metų pabaigos uždarymas baigtas, operacijos rodomos, tačiau jų negalima apmokėti arba neapmokėti. Galite panaikinti operacijų žymėjimą tik uždarais finansiniais metais. Jei dienų seka yra uždarais fiskaliniais metais, **Pažymėti pasirinktą**, **už pažymėtas operacijas**, ir **Atvirkščiai pažymėti sandoriai** mygtukai nepasiekiami.

    2. Pasirinkite pagrindinę sąskaitą, kurioje bus rodomos operacijos. Šis laukas yra būtinas. Peržvalga rodo tik pagrindines paskyras, kurios yra pasirinktos **Didžiosios knygos atsiskaitymas** puslapis įmonės sąskaitų planui.
    3. Pasirinkite paskelbimo sluoksnį. Negalite apmokėti operacijų, kurios yra skirtinguose registravimo sluoksniuose.
    4. Norėdami rodyti pagrindinę sąskaitą ir dimensijas atskiruose stulpeliuose, pasirinkite finansinių dimensijų rinkinį.

3.  Pasirinkite **Rodyti operacijas** kad būtų rodomos visos operacijos, atitinkančios jūsų nustatytus filtrus. Pakeitus bet kurį filtrą arba dimensijų rinkinius, būtina dar kartą pasirinkti **Rodyti operacijas**.
4.  Pasirinkite eilutes atsiskaitymui. Vertė **Pasirinkta suma** puslapio viršuje esantis laukas didėja arba mažėja, kad atspindėtų bendrą sumą pasirinktose eilutėse.
5.  Kai baigsite pasirinkti operacijas, pasirinkite **Pažymėti pasirinktą**. Kiekvienai pasirinktai operacijai rodoma varnelė **Pažymėtas** stulpelyje. Be to, vertė **Pažymėta suma** virš tinklelio esantis laukas didėja arba mažėja, kad atspindėtų bendrą sumą pažymėtose eilutėse.
6.  Kai reikšmė **Pažymėta suma** laukas yra **0** (nulis), pasirinkite **Atsiskaityti už pažymėtas operacijas**.

    - Dalinis atsiskaitymas neleidžiamas. Pavyzdžiui, negalite apmokėti $100 debeto operacijos $90 kredito operacija. Likusi $10 kredito operacija taip pat turi būti pažymėta, kad būtų įtraukta į atsiskaitymą.
    - Įveskite atsiskaitymo datą. Data turi būti paskutinė operacijų, kurios yra pažymėtos atsiskaityti, data arba vėlesnė.

Pažymėtų operacijų būsena atnaujinama į **Sudengta**.

> [!IMPORTANT]
> Visos operacijos, kurias pažymėjote atsiskaityti už aktyvų juridinį asmenį ir pasirinktą pagrindinę sąskaitą, bus apmokėtos. Operacijos neturi būti rodomos puslapyje. Jie bus išspręsti, net jei jie bus paslėpti dėl filtro.

Kai kurie procesai, pvz., operacijos atšaukimas, automatiškai apmoka DK operacijas. Pavyzdžiui, mokėjimas ir sąskaita faktūra apmokami kaip gautinos sumos, o atsiskaitymas sukuria realų pelną / nuostolį. Apmokėjus mokėjimą ir sąskaitą faktūrą, neapmokamos jokios pagrindinės knygos operacijos, pvz., gautinų sumų knygos sąskaitos operacijos. Tačiau jei mokėjimas ir sąskaita yra neapmokėti gautinų sumų sąraše, atšaukus gautinų sumų apmokėjimą, pirminis ir atbulinis apskaitos įrašai bus apmokėti didžiojoje knygoje. Kai **Supratimas tarp atsiskaitymo knygoje ir uždarymo metų pabaigoje** funkcija įjungta, DK atsiskaitymas už atšaukimą neįvyksta automatiškai, jei atšaukimo data yra kitais fiskaliniais metais.

## <a name="use-excel-for-ledger-settlement"></a>Atsiskaitymams naudokite Excel

Sandoriai, kurie rodomi **Didžiosios knygos atsiskaitymas** puslapį galima eksportuoti į Excel. Programoje Excel galite toliau filtruoti operacijas, kad nustatytumėte, kurias operacijas pažymėti atsiskaitymui.
Abu DK atsiskaitymo objektai eksportuoja Didžiosios knygos operacijas tik į pagrindinę sąskaitą, kuri pasirinkta **Didžiosios knygos atsiskaitymas** puslapį. Nors uždarytų fiskalinių metų operacijos vis tiek gali būti pažymėtos arba nepažymėtos naudojant „Excel“, jos negali būti apmokėtos. Be to, tais finansiniais metais apmokėtos operacijos negali būti atšauktos.

## <a name="make-transactions-easier-to-find"></a>Lengvesnė operacijų paieška

The **Didžiosios knygos atsiskaitymai** puslapyje yra galimybių, kurios palengvina atsiskaitymui reikalingų operacijų peržiūrą.

• Naudoti **Pažymėtas** filtras, kad filtruotumėte operacijas pagal tai, ar **Pažymėtas** pažymėtas jų žymimasis langelis.
• Naudoti **Būsena** filtrą, kad filtruotumėte operacijas pagal jų būseną.
• Pasirinkite **Rūšiuoti pagal absoliučią sumą** rūšiuoti sumas pagal absoliučią vertę. Tokiu būdu galite sugrupuoti debetus ir kreditus, kurių suma yra tokia pati.

## <a name="reverse-a-settlement"></a>Sudengimo atšaukimas

Galite atšaukti per klaida atliktą sudengimą.

1.  Atlikite 1–3 veiksmus [Atlikti sandorius](#settle-transactions) skyriuje, kad būtų rodomos jus dominančios operacijos.
2.  Filtre **Būsena** pasirinkite **Sudengta**.
3.  Pasirinkite eilutes, kurias norite pakeisti.
4.  Pasirinkite **Atvirkščiai pažymėti sandoriai**. Visų operacijų, turinčių tą patį atsiskaitymo ID, būsena atnaujinama į **Neišspręstas**.

> [!IMPORTANT]
> Visos operacijos, turinčios tą patį atsiskaitymo ID, bus anuliuotos, net jei jos nepažymėtos. Pavyzdžiui, buvo pažymėtos ir sutvarkytos keturios eilutės. Visos keturios eilutės turi tą patį atsiskaitymo ID. Jei pažymėsite vieną iš šių keturių eilučių ir pasirinksite **Atvirkščiai pažymėti sandoriai**, visos keturios eilutės bus apverstos.






