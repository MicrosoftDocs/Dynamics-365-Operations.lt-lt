---
title: Informacijos bendrinimas tarp didžiosios knygos atsiskaitymo ir metų pabaigos uždarymo
description: Šioje temoje pateikiama informacija apie patobulinimus, kurie veikia DK sudengimą ir DK metų pabaigos uždarymą.
author: kweekley
ms.date: 03/18/2022
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
ms.openlocfilehash: e18f77d73239de23000b5310d9342c6db95bc524
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462358"
---
# <a name="awareness-between-ledger-settlement-and-year-end-close"></a>Informacijos bendrinimas tarp didžiosios knygos atsiskaitymo ir metų pabaigos uždarymo

[!include [banner](../includes/banner.md)]


Microsoft versijoje Dynamics 365 Finance 10.0.25 funkcijų **valdymo** darbo srityje galima supratimą apie DK sudengimą ir **uždarymo metų pabaigoje** funkciją. Ši funkcija prideda du pirminius patobulinimus, daražiusį įtaką DK sudengimą ir DIDŽIOSIOS knygos metų pabaigos uždarymą.

DK metų pabaigos uždarymo metu sudengtos DK operacijos nebebus įtrauktos į kitų finansinių metų laikotarpio pradžios likutį. Šis patobulinimas užtikrina, kad į laikotarpio pradžios likutį įtraukiamos tik nesudengtos DK operacijos. Svarbu, kai vykdomas DK užsienio valiutos kurso pasikeitimas. Užsienio valiutos kurso pasikeitimas vykdomas tik toms DK operacijoms, kurių būsena **Nesudengta**. Tačiau prieš **pasibaigus DK sudengimo ir metų pabaigos uždarymo priemonės supratimui, pradžios likutis susumuotas ir susumuotais operacijas,** **·** **kurių būsena yra Sudengta, ir tas operacijas, kurių būsena Nesudengta,** o apibendrintos sumos būsena nustatyta kaip Nesudengta.**·**

Antrasis patobulinimas leidžia užregistruoti išsamių pradžios likučio operacijų DK metų pabaigos uždarymo metu. Jei metų **pabaigos uždarymo parinktis** **Išlaikyti informaciją nustatyta kaip Taip**, kiekvienai nesudengaiai DK operacijai bus sukurtas atskiras pradžios likutis. Šis parametras nustatomas kiekvienai pagrindinei sąskaitai DK sudengimo nustatyme. Išlaikydami išsamias pradžios likučio operacijas, labai pagerinate galimybę sudengti nesudengtas DK operacijas kitais finansiniais metais.

Siekiant palaikyti naujus patobulinimus, buvo atlikti DK sudengimo ir metų pabaigos uždarymo pakeitimai.

### <a name="changes-to-ledger-settlement"></a>DK sudengimo pakeitimai

- DK sudengimas turi būti atliktas per finansinius metus.
- Vienoje pagrindinėje sąskaitoje operacijoms turi būti atliktas DK sudengimas. Pagrindinė sąskaita dabar yra būtinas filtras DK sudengimo **puslapyje**.
- Negalima atlikti operacijų, užregistruotų uždarytuose finansiniuose metuose, DK sudengimo ir DK sudengimo atšaukimo (kitaip tariant, buvo vykdomas metų pabaigos uždarymas).

### <a name="changes-to-year-end-close"></a>Metų pabaigos uždarymo pakeitimai

- Jei kitų finansinių metų pradžios balanso operacijos buvo sudengtos, metų pabaigos uždarymo atšaukti negalima. Šis pakeitimas taikomas, kai metų pabaigos uždarymas atšaukiamos **arba** **kai** metų pabaigos uždarymas yra iš naujo pabaigęs ir DK parametruose nustatyta metų uždarymo parinktis Naikinti esamus metų pabaigos įrašus.
- Jei metų **pabaigos uždarymo** **parinktis Išlaikyti išsamią informaciją nustatyta kaip Taip** bet kuriai DK sudengimo balanso sąskaitai, bus sukurtos išsamesnės pradžios likučio operacijos tai pagrindinei sąskaitai.

## <a name="before-you-enable-the-feature"></a>Prieš įgalinant funkciją

Dėl funkcijų ir duomenų modelio pakeitimų svarbu, kad prieš įgalindami funkciją atsižveltumėte į šiuos dalykus:

- Visos operacijos, kurios buvo pažymėtos sudengti, bet nebuvo sudengtos, bus automatiškai atžymėtos, kai ši funkcija bus įjungta. Norėdami išvengti bet kokio darbo praradimo, sudengkite visas pažymėtas operacijas prieš įgalindami funkciją.
- Kai kurios organizacijos metų pabaigos uždarymą vykdo kelis kartus tais pačiais finansiniais metais. Neįjunkite funkcijos, jei metų pabaigos uždarymas jau buvo vykdomas vieną kartą ir bus vykdomas dar kartą tų pačių finansinių metų. Prieš apdorodami pirmąjį metų pabaigos uždarymą arba apdorodami finansinių metų praėjusių metų pabaigos uždarymą, turite įgalinti šią priemonę.

  Jei norite įgalinti funkciją, tačiau metų pabaigos uždarymas jau buvo paleistas vieną kartą, prieš įgalindami funkciją turite atšaukti metų pabaigos uždarymą.

- Kadangi finansinių metų sudengimas nebeį leidžiamas, rekomenduojame įgalinti priemonę prieš pradedant metų pabaigos uždarymo procesą. Tada, norėdami užtikrinti, kad kitų finansinių metų pradiniai balansai nebūtų paveikti ankstesnių kryžminių finansinių metų sudengimų, pradžios balanso operacija turėtų būti sudengta už uždaromi finansiniais metais.
- Kadangi pagrindinių sąskaitų sudengimas nebedingas, koreguokite savo sąskaitų planą arba procesus, norėdami užtikrinti, kad DK sudengimas galėtų būti atliktas toje pačioje pagrindinėje sąskaitoje.
- Funkcijos negalima įgalinti, jei naudojamas viešojo sektoriaus metų pabaigos uždarymo procesas.

## <a name="set-up-ledger-settlement"></a>NUSTATYTI DK sudengimą

Įgalinus funkciją ir prieš vykdant kitų metų pabaigos uždarymą, kiekviena organizacija turi nustatyti, ar per metų pabaigos uždarymą išlaikyti operacijos informaciją. Pasirinkimas neturi įtakos balanso registravimui iš ankstesnių metų pabaigos uždarymo procesų.

Parinktis **Išlaikyti išsamią informaciją metų pabaigos uždarymo** metu yra nustatyta kiekvienai pagrindinei sąskaitai DK sudengimo **nustatymo** puslapyje.

1.  Eikite **į LedgerLedger** > **setupGeneral** > **DK parametrus**.
2.  Skirtuke **DK sudengimas** pasirinkite DK sudengimo **sąskaitas**.

Arba

1.  Eikite į **LedgerPeriodic** > **tasksLedger** > **sudengimą**.
2.  Pasirinkti **DK sudengimo sąskaitas**.

Du stulpeliai įtraukti į DK sudengimų **puslapį**:
    
- **Pagrindinės sąskaitos tipas** – šis stulpelis skirtas tik informacijai. Jis rodo tipą, kuris priskirtas pagrindinei sąskaitai.
- **Uždaryti metų pabaigos informaciją – numatyta**, kad pasirinktis nustatyta kaip **Ne**. Jis gali būti nustatytas kaip **Taip** tik jei pagrindinės sąskaitos **tipo** stulpelyje nurodyta vertė **yra Balansas**, Turtas **arba** **Įsipareigojimas**. Kai parinktis nustatyta kaip **Ne**, pradžios likutis bus registruojamas suvestinėje, kaip įprasta metų pabaigos uždarymo metu. Jei nustatyta Taip, kiekvienos **DK** operacijos, kuri nėra sudengta pagrindinei sąskaitai, pradžios likučiai bus kuriami išsamiai.

## <a name="year-end-close"></a>Metų pabaigos uždarymas

Kai metų pabaigos uždarymą **vykdote nueidami į General ledgerPeriod** > **closeYear** > **pabaigos** uždarymą, proceso metu sukuriami pagrindinių sąskaitų, nustatytų DK sudengti, pradiniai balansai. Pradžios likučiai kuriami suvestinėje arba išsamiai, atsižvelgiant į DK sudengimo nustatymą. Į procesą neįtrauktos sudengtos DK operacijos, neatsižvelgiant į tai, ar kiekvienos pagrindinės sąskaitos pradžios likutį registruojate suvestinėje, ar išsamiai.

Pvz., pagrindinėse sąskaitose registruojamos kelios operacijos130100 2021 finansiniais metais.

| Žurnalo numeris | Kvitas  | Data       | Tipas      | DK sąskaita | Abonemento pavadinimas        | Aprašymas       | Valiuta | Suma operacijos valiuta | Suma  | Suma, išreikšta ataskaitų valiuta |
|----------------|----------|------------|-----------|----------------|---------------------|-------------------|----------|--------------------------------|---------|------------------------------|
| 20853          | FTV-3000 | 12/3/2021  | Vykdymas | 130100-001-    | Gautinos sumos | Aptarnavimo mokestis       | USD      | 100                            | 100     | 100                          |
| 20855          | FTV-3004 | 12/5/2021  | Vykdymas | 130100-002-    | Gautinos sumos | Komunalinės paslaugos         | USD      | 175                            | 175     | 175                          |
| 20854          | CMV-4000 | 12/16/2021 | Vykdymas | 130100-001-    | Gautinos sumos | Grąžinimas            | USD      | -100                           | -100    | -100                         |
| 20851          | ARP-8000 | 12/20/2021 | Vykdymas | 130100-002-    | Gautinos sumos |                   | USD      | -0.88                          | -0.88   | -0.88                        |
| 20853          | ARPM0004 | 12/20/2021 | Vykdymas | 130100-002-    | Gautinos sumos |                   | EUR      | -127.11                        | -174.12 | -174.12                      |
| 20856          | CMV-4010 | 12/21/2021 | Vykdymas | 130100-002-    | Gautinos sumos | Kreditas sąskaitoje | USD      | -175                           | -175    | -175                         |
| 20857          | FTV-3011 | 12/28/2021 | Vykdymas | 130100-001-    | Gautinos sumos | Komunalinės paslaugos         | USD      | 400                            | 400     | 400                          |
| 20910          | FTV-3020 | 12/29/2021 | Vykdymas | 130100-002-    | Gautinos sumos | Aptarnavimas           | USD      | 300                            | 300     | 300                          |

Iš šių operacijų trys sudengimos DK sudengimo metu.

Išrašyta SF 175 JAV doleriams (175 USD). Šią SF apmokėjo mokėjimas eurais (EUR), o buvo taikoma mokėjimo nuolaida.

| Žurnalo numeris | Kvitas  | Data       | Tipas      | DK sąskaita | Abonemento pavadinimas        | Aprašymas | Valiuta | Suma operacijos valiuta | Suma  | Suma, išreikšta ataskaitų valiuta |
|----------------|----------|------------|-----------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20855          | FTV-3004 | 12/5/2021  | Vykdymas | 130100-002-    | Gautinos sumos | Komunalinės paslaugos   | USD      | 175                            | 175     | 175                          |
| 20851          | ARP-8000 | 12/20/2021 | Vykdymas | 130100-002-    | Gautinos sumos |             | USD      | -0.88                          | -0.88   | -0.88                        |
| 20853          | ARPM0004 | 12/20/2021 | Vykdymas | 130100-002-    | Gautinos sumos |             | EUR      | -127.11                        | -174.12 | -174.12                      |

Pagrindinės sąskaitos rezultatai 130100 priklauso nuo to, ar priemonė įgalinta prieš metų pabaigos uždarymą. Jei priemonė įgalinta, rezultatas taip pat priklauso nuo to, kaip nustatyta parinktis Išsaugoti išsamią informaciją metų pabaigos uždarymo metu.

### <a name="the-feature-isnt-enabled"></a>Ši funkcija neįgalinta
Metų pabaigos uždarymas sukuria tris pagrindinės sąskaitos pradžios likučio operacijas130100 2022 m. Operacijų suma apskaitos valiuta yra USD 525.

| Žurnalo numeris | Kvitas  | Data     | Tipas    | DK sąskaita | Abonemento pavadinimas        | Aprašymas | Valiuta | Suma operacijos valiuta | Suma  | Suma, išreikšta ataskaitų valiuta |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-002-    | Gautinos sumos |             | USD      | 299.12                         | 299.12  | 299.12                       |
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-001-    | Gautinos sumos |             | USD      | 400                            | 400     | 400                          |
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-002-    | Gautinos sumos |             | EUR      | -127.11                        | -174.12 | -174.12                      |

Nors mokėjimo operacija EUR -127,11 buvo sudengta DK, operacija vis dar nusiųsta kaip pradžios balansas.

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--no"></a>Priemonė įgalinta ir Išsaugoti informaciją metų pabaigos uždarymo metu = Ne

Metų pabaigos uždarymas sukuria dvi pagrindinės sąskaitos 2022 130100 balanso operacijas. Operacijų suma apskaitos valiuta vis dar USD 525, bet DK sudengtos operacijos į laikotarpio pradžios likutį neįtraukiamos. Bendra sąskaitos 130100-002 suma USD 125 vietoj USD 299.12, o 127,11 EUR / 174,12 USD operacijos nėra visiškai neįtrauktos.

| Žurnalo numeris | Kvitas  | Data     | Tipas    | DK sąskaita | Abonemento pavadinimas        | Aprašymas | Valiuta | Suma operacijos valiuta | Suma | Suma, išreikšta ataskaitų valiuta |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-002-    | Gautinos sumos |             | USD      | 125                            | 125    | 125                          |
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-001-    | Gautinos sumos |             | USD      | 400                            | 400    | 400                          |

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--yes"></a>Priemonė įgalinta ir Palikti informaciją metų pabaigos uždarymo metu = Taip

Uždaržius metus, 2022 m. sukuriamos penkios pagrindinės sąskaitos 130100 balanso operacijos. Sukuriama atskira pradžios likučio operacija kiekvienai iš penkių operacijų, kurios nebuvo sudengtos. Operacijų suma apskaitos valiuta vis dar USD 525.

| Žurnalo numeris | Kvitas  | Data     | Tipas    | DK sąskaita | Abonemento pavadinimas        | Aprašymas       | Valiuta | Suma operacijos valiuta | Suma | Suma, išreikšta ataskaitų valiuta |
|----------------|----------|----------|---------|----------------|---------------------|-------------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-001-    | Gautinos sumos | Aptarnavimo mokestis       | USD      | 100                            | 100    | 100                          |
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-001-    | Gautinos sumos | Grąžinimas            | USD      | -100                           | -100   | -100                         |
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-002-    | Gautinos sumos | Kreditas sąskaitoje | USD      | -175                           | -175   | -175                         |
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-001-    | Gautinos sumos | Komunalinės paslaugos         | USD      | 400                            | 400    | 400                          |
| 20910          | YEC_2021 | 2022-01-01 | Atidarantis | 130100-002-    | Gautinos sumos | Aptarnavimas           | USD      | 300                            | 300    | 300                          |

Kai saugoma išsami operacijų informacija, pradinės išsamios operacijos nepa paveikiamos. Jie lieka užregistruoti ir nesudengti finansiniais metais, kurie uždaromi. Šių operacijų kopija sukuriama pradžios likučiui. Toliau nurodytos pradinių operacijų vertės yra kopijuojamos į atidarymo balanso operacijas.

- DK sąskaita (pagrindinė sąskaita ir visos finansinės dimensijos)
- Operacijų, apskaitos ir ataskaitų valiutų sumos
- Aprašymas
- Registravimo sluoksnis
- Registravimo tipas

   > [!NOTE]
   > Jokiai kitai balanso operacijai nepriskirtas registravimo tipas. Todėl registravimo tipą galima naudoti išsamiai pavestims atidarymo operacijoms atskirti.

Kai kurie pradinių operacijų laukai turi pakeisti pradinio balanso išsamiose operacijose. Balanso operacijų pradžios data visada yra pirmoji kitų finansinių metų diena. Žurnalo numeris turi pasikeisti, o kvito numeris pasikeičia į vertę, kuri buvo įvesta metų pabaigos uždarymo dialogo lange.

Informaciją iš pradinių operacijų galima rasti DK sudengimo **puslapyje**. Kiekviena išsami pradžios likučio operacija tinklelyje **rodo stulpelį** Pradinės operacijos data. Šis stulpelis gali padėti suderinti operacijas naujais finansiniais metais. Galite pasirinkti Peržiūrėti pradinį **kvitą, norėdami** detalizuoti atgal prie viso pradinio kvito.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Sudengti operacijas
Norėdami sudengti DK operacijas, atlikite toliau nurodytus veiksmus.

1. Eikite į **LedgerPeriodic** > **tasksLedger** > **sudengimą**.
2.  Puslapio viršuje nustatykite filtrus.

    1. Pasirinkite datos diapazoną. Arba galite pasirinkti datos intervalo kodą, kad datų diapazonas būtų automatiškai užpildomas.

       - Datų diapazonas negali būti kryžminis finansinių metų. Jei datų diapazonas peržengia finansinius metus, pasirinkus Rodyti operacijas nebus **rodomos jokios operacijos**.
       - Jei datų diapazonas yra atvirus finansinius metus, operacijas galima sudengti ir sudengimas gali būti atšauktas. Jei datų diapazonas yra uždarytuose finansiniuose metuose arba jei metų pabaigos uždarymas baigtas, operacijos rodomos, tačiau jų negalima sudengti arba nesudengti. Galite atžymėti tik uždarytų finansinių metų operacijas. Jei datų diapazonas yra uždarytuose finansiniuose metuose, **žymėti pasirinktus** metus, **·** **sudengti pažymėtas operacijas ir atšaukti pažymėtų** operacijų mygtukus naudoti negalima.

    2. Pasirinkti pagrindinę sąskaitą, kurios operacijas rodyti. Šis laukas yra būtinas. Peržvalga rodo tik įmonės sąskaitų **plano DK** sudengimo puslapyje pasirinktas pagrindines sąskaitas.
    3. Pasirinkti registravimo sluoksnį. Negalima sudengti operacijų, kurios yra skirtinguose registravimo sluoksniuose.
    4. Norėdami pagrindinę sąskaitą ir dimensijas rodyti atskiruose stulpeliuose, pasirinkite finansinių dimensijų rinkinį.

3.  Pasirinkite **Rodyti operacijas**, kad būtų rodomos visos operacijos, kurios atitinka jūsų nustatytus filtrus. Pakeitus bet kurį filtrą arba dimensijų rinkinius, būtina dar kartą pasirinkti **Rodyti operacijas**.
4.  Pasirinkti eilutes sudengti. Puslapio viršuje esanti **lauko Pasirinkta** suma vertė didėja arba mažina, kad atspindėtų bendrą sumą pasirinktose eilutėse.
5.  Baigę pasirinkti operacijas, pasirinkite Žymėti **pasirinktą**. Kiekvienai pažymėtai operacijai stulpelyje Pažymėta rodoma **varnelė**. Be to, reikšmė lauke Pažymėta **suma virš** tinklelio didėja arba mažėja, kad atspindėtų bendrą sumą pažymėtose eilutėse.
6.  Kai pažymėto sumos lauko **vertė yra** **0 (nulis**), pasirinkite Sudengti **pažymėtas operacijas**.

    - Dalinis sudengimas neleidžiamas. Pavyzdžiui, negalima sudengti sf $100 operacijos pagal $90 operaciją. Likusi kredito $10 taip pat turi būti pažymėta įtraukti į sudengimą.
    - Įvesti sudengimo datą. Data turi sudengti pažymėtų operacijų vėliausią datą arba po jos.

Pažymėtų operacijų būsena atnaujinama į **Sudengta**.

> [!IMPORTANT]
> Visos operacijos, kurias pažymėjote sudengti aktyviam juridiniam subjektui ir pasirinkta pagrindinė sąskaita bus sudengtos. Operacijos neturi būti rodomos puslapyje. Jos bus sudengtos, net jei jos paslėptos dėl filtro.

Kai kurie procesai, pvz., operacijos atšaukimas, automatiškai sudengias DK operacijas. Pavyzdžiui, mokėjimas ir SF sudengiuojami gautinose sumose, o sudengimas generuoja įvykdytą pelną / nuostolį. Mokėjimo ir SF sudengimas nesudengia jokių DK operacijų, pvz., gautinų sumų DK sąskaitos operacijų. Tačiau jei mokėjimas ir SF nesudengti gautinose sumose, atšaukus apskaitos įrašą, kuris buvo užregistruotas atšaukiant gautinų sumų sudengimą, pradiniai ir atšaukimo apskaitos įrašai bus sudengti DK. Įgalinus **DK sudengimo** ir metų pabaigos uždarymo priemonės supratimą, atšaukimų DK sudengimas automatiškai neišsijungia, jei atšaukimo data yra kitų finansinių metų.

## <a name="use-excel-for-ledger-settlement"></a>Naudoti "Excel" DK sudengti

DK sudengimo puslapyje **rodomos operacijos** gali būti eksportuojamos į Excel. Programoje "Excel" galite toliau filtruoti operacijas, kad nustatytumėte, kurias operacijas reikia pažymėti sudengti.
Abu DK sudengimo objektai eksportuos tik pagrindinės sąskaitos, pasirinktos DK sudengimo **puslapyje, DK operacijas**. Nors uždarytų finansinių metų operacijos vis tiek gali būti pažymėtos ar atžymėtos naudojant Excel, jos negali būti sudengtos. Be to, negalima atšaukti sudengtos šių finansinių metų operacijos.

## <a name="make-transactions-easier-to-find"></a>Lengvesnė operacijų paieška

DK **sudengimų** puslapyje yra galimybių, kurios padeda lengviau peržiūrėti operacijas, reikalingas sudengti.

• Naudokite pažymėtą **filtrą** operacijoms filtruoti, atsižvelgiant į **tai, ar** pažymėtas jų žymės langelis.
• Naudokite būsenos **filtrą** operacijoms filtruoti pagal jų būseną.
• Norėdami surūšiuoti **sumas pagal absoliučią** vertę, pasirinkite Rūšiuoti pagal absoliučią sumą. Tokiu būdu galite grupuoti debetus ir kreditus, kurių suma ta pati.

## <a name="reverse-a-settlement"></a>Sudengimo atšaukimas

Galite atšaukti per klaida atliktą sudengimą.

1.  Norėdami parodyti jus dominaas operacijas, atlikite 1–3 [veiksmus](#settle-transactions), skyriuje Sudengti operacijas.
2.  Filtre **Būsena** pasirinkite **Sudengta**.
3.  Pasirinkti atšaukimo eilutes.
4.  Pasirinkti Atšaukti **pažymėtas operacijas**. Visų operacijų, kurių sudengimo ID toks pats, būsena atnaujinama į **Nesudengta**.

> [!IMPORTANT]
> Visos operacijos, kurios turi tą patį sudengimo ID, bus atšauktos, net jei jos nepažymėtos. Pavyzdžiui, keturios eilutės pažymėtos ir sudengtos. Visos keturios eilutės turi tą patį sudengimo ID. Jei vieną iš tų keturių eilučių pažymėsite ir pasirinksite **Atšaukti pažymėtas operacijas**, visos keturios eilutės bus atšauktos.






