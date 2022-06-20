---
title: Atsiskaitymo grafikų funkcijos
description: Šiame straipsnyje paaiškinamos atsiskaitymo grafikų funkcijos, pvz., kainų metodai, perskyrimai ir nuolaidos, lygiavimo datos, paskaita, atvirkštinis atsiskaitymas ir išskaidytos prekių grupės.
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
ms.openlocfilehash: b6cfebc2bbfe06e118bfc96f9ae0df6323805e39
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853589"
---
# <a name="billing-schedule-features"></a>Atsiskaitymo grafikų funkcijos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinamos atsiskaitymo grafikų ir atsiskaitymo grafiko eilučių funkcijos. Aprašomi įvairūs kainodaros metodai, kaip naudoti perskyrimus ir nuolaidas, ir kaip atšaukti atsiskaitymo laikotarpį. Joje taip pat pateikiami ir paprastų skaičiavimų ir prekių grupių skaidymo pavyzdžiai.

## <a name="pricing-methods"></a>Kainodaros metodai

Prekės vieneto kainai apskaičiuoti galite naudoti vieną iš šių kainodaros metodų:

* Butas
* Standartinė
* Pakopa
* Fiksuota pakopa

### <a name="flat-pricing"></a>Buto kainodara

Kai naudojamas buto įkainojimo metodas, **atsiskaitymo** grafiko eilutės elemento vieneto kainą puslapyje Visi atsiskaitymo grafikai galima redaguoti pagal bet kokią norimą vertę. Kainos **vieneto** vertė visada yra **1**. Todėl prekės **Vieneto kaina** **ir Grynosios** sumos vertės yra vienodos.

### <a name="standard-pricing-without-a-trade-agreement"></a>Standartinė kainodara (be prekybos sutarties)

Kai standartinis kainodaros metodas naudojamas be prekybos sutarties, **·** **nustatote atsiskaitymo grafiko eilutės elemento vieneto kainą, pasirinkdami Produkto informacijos valdymas informacijos leidimo puslapyje.** Vieneto kaina rodoma skyriuje **Bazinė pardavimo** kaina. Jis skaičiuojamas kaip *Kainos*&divide;*kiekis.*

### <a name="standard-pricing-with-a-trade-agreement"></a>Standartinė kainodara (su prekybos sutartimi)

Toliau pateikti pavyzdžiai rodo standartinius kainos skaičiavimus, kai prekybos sutartis egzistuoja. Prekybos sutartis galite kurti išsamios informacijos **apie produktą puslapyje**.

Abiejuose pavyzdžiuose naudojama prekė su šiais kainos skliaustais.

| Kiekis iš | Kiekis į | U of M | Kaina | Kainos vienetas |
|---|---|---|---|---|
| 0 | 100 | Kiekvienas | 1.50 | 1 |
| 100 | 200 | Kiekvienas | 1.25 | 1 |
| 200 | 999999 | Kiekvienas | 1.00 | 1 |

**1 pavyzdys**

SF kiekis yra 250, ir naudojamas standartinis kainodaros metodas. Kadangi kiekis yra 200–999 999 kainų kiekio diapazone, vieneto kaina yra 1,00. 

Grynoji suma skaičiuojama taip:

*Grynoji* suma = (*kiekio*&times;*kaina*) &divide;*Kainos vienetas* = (250 &times; 1,00) &divide; 1 = 250

**2 pavyzdys**

SF kiekis yra 100, ir naudojamas standartinis kainodaros metodas. Kadangi SF kiekio diapazonas yra 0–100, vieneto kaina yra 1,50.

> [!NOTE]
> SF kiekio diapazonas yra 0–100, o ne 100–200 diapazone, nes, esant standartinio kiekio gretinimo veikimo būdą, kiekis atitinka, *jei* jis didesnis nei "nuo" *kiekis* ir mažesnis už kiekį "iki".

Grynoji suma skaičiuojama taip:

*Grynoji* suma = (100 &times; 1,50) &divide; 1 = 150

### <a name="tier-pricing"></a>Pakopų kainodara

Toliau pateiktame pavyzdyje prekė turi šiuos kainos skliaustus.

| Kiekis iš | Kiekis į | U of M | Kaina | Kainos vienetas |
|---|---|---|---|---|
| 0 | 100 | Kiekvienas | 1.50 | 10 |
| 100 | 200 | Kiekvienas | 1.25 | 10 |
| 200 | 999999 | Kiekvienas | 1.00 | 10 |

Jei SF kiekis yra 250, o naudojamas pakopos kainos metodas, prekių kainos skaičiuojamos tokiu būdu, remiantis kainų skliaustais:

- **Pirmosios 100 prekių:** 100 &times; 1,50 = 150,00
- **Antrosios 100 prekių:** 100 &times; 1,25 = 125,00
- **Likusios prekės:** 50 &times; 1,00 = 50,00

Grynoji suma skaičiuojama taip:

*Grynoji* suma = (150,00 &divide; 10) + (125,00 &divide; 10) + (50,00 &divide; 10) = 15,00 + 12,50 + 5,00 = 32,50

Apskaičiavus grynąją sumą, vieneto kaina apskaičiuojama dalijant grynąją sumą iš kiekio:

*Vieneto* kaina = 32,50 &divide; 250 = 0,13

### <a name="flat-tier-pricing"></a>Buto pakopos kainodara

Toliau pateiktame pavyzdyje prekė turi šiuos kainos skliaustus.

| Kiekis iš | Kiekis į | U of M | Fiksuotos pakopos suma | Kainos vienetas |
|---|---|---|---|---|
| 0 | 50 | Kiekvienas | 100.00 | 50 |
| 50 | 200 | Kiekvienas | 150.00 | 200 |

Toliau pateikiamoje lentelėje rodomos nupirktų kiekių SF ir vieneto kainos. Pirmiausia apskaičiuojama grynoji suma, tada skaičiuojama vieneto kaina.

| Sąskaita faktūra | Pirktas kiekis | Vnt. kaina | Grynoji suma |
|---|---|---|---|
| 1 | 25 | 2,00 &divide; 25 = 0,08 | 100 &divide; 50 = 2,00 |
| 2 | 20 | 2,00 &divide; 20 = 0,10 | 100 &divide; 50 = 2,00 |
| 3 | 50 | 2,00 &divide; 50 = 0,04 | 100 &divide; 50 = 2,00 |
| 4 | 60 | 0,75 &divide; 60 = 0,0125 = 0,01 | 150 &divide; 200 = 0,75 |

## <a name="escalations-and-discounts"></a>Perskyrimai ir nuolaidos

Perskyrimas *yra* kainos padidėjimas būsimam atsiskaitymo laikotarpiui, kuriam dar nesukurta SF. Nuolaida *yra* kainos sumažinimas būsimam atsiskaitymo laikotarpiui, kuriam dar nesukurta SF.

Abonemento sąskaitų išrašymo metu perskyrimų ir nuolaidų negalima taikyti atgaline data sąskaitų pateikimo grafikui. Pavyzdžiui, negalite taikyti perskyrimo trijų praeities mėnesių atsiskaitymo grafikui ir jį apdoroti. Kitaip tariant, negalima taikyti kainos padidėjimo, kuris įvyko prieš tris mėnesius.

Galite taikyti perskyrimą ar nuolaidą atsiskaitymo grafikui arba atsiskaitymo grafiko eilutei vienoje iš šių vietų:

- Visų **/ aktyvių atsiskaitymo grafikų** sąrašo puslapis
- Konkretus atsiskaitymo grafikas
- Konkreti atsiskaitymo grafiko eilutė

### <a name="apply-an-escalation-or-discount"></a>Taikyti perskyrimą arba nuolaidą

Norėdami taikyti perskyrimą arba nuolaidą atsiskaitymo grafikui, atlikite šiuos veiksmus.

1. Pasirinkite atsiskaitymo grafiką arba atsiskaitymo grafiko eilutę.
2. Pasirinkite **perskyrimą ir** nuolaidą skirtuke **Perskyrimas** ir nuolaida arba sąskaitų pateikimo grafiko eilutėje.
3. Jei vartotojo kainos indeksas naudojamas perskyrimo ar nuolaidos skaičiavimui, pasirinkite vertę vartotojo kainos **indekso skaičiavimo lauke**.
4. Pasirinkite **Naujas,** jei norite įtraukti perskyrimo ar nuolaidos eilutę.
5. Nuolaidai pažymėkite žymės langelį **Nuolaida**. Norėdami perskirti, išvalykite **žymės** langelį Nuolaida.
6. Nustatykite laukus **Pradžios data** ir **Dažnis**.
7. Atidėjimo prekėms, kurios naudoja neaprašytų įplaukų funkciją, nustatykite **lauką Pabaigos** data.
8. Nustatykite **procentų**, **sumos** arba vartotojo kainų **indekso grafiko lauką**.
9. Nustatykite **pabaigos datos lauką**.
10. Pasirinkite **Gerai**.
11. Kiekvienai papildomai perskyrimo ar nuolaidos eilutei, kurios jums reikia, pakartokite 4–10 veiksmus.

### <a name="fields-on-the-billing-schedule-lines-page"></a>Laukai atsiskaitymo grafiko eilučių puslapyje

Atsiskaitymo **grafiko eilučių** puslapyje yra šie laukai.

| Laukas | Aprašymas |
|---|---|
| Prekės numeris | Atsiskaitymo grafiko eilutės prekės numeris. Šis laukas galimas tik kai puslapis atidaromas iš atsiskaitymo grafiko eilutės elemento. |
| Vartotojų kainų indekso apskaičiavimas | <p>Pasirinkite metodą, naudojamą skaičiuojant vartotojo kainų indekso perskyrimą:</p><ul><li>**Ankstesnis vartotojo kainos indeksas** – perskyrimo skaičiavimui naudoti ankstesnę vartotojo kainos indekso vertę.</li><li>**Pagrindinio vartotojo kainos indeksas** – perskyrimo skaičiavimui naudoti pagrindinio vartotojo kainos indekso vertę.</li></ul> |
| **Eilučių tinklelis** | |
| Nuolaida | <p>Nustatykite žymės langelį, jei norite nurodyti, ar sumos pakeitimas yra perskyrimo ar nuolaidos:</p><ul><li>**Pasirinkta** – pakeitimas taiko nuolaidą atsiskaitymo grafikui arba atsiskaitymo grafiko eilutei.</li><li>**Išvalyta** – pakeitimas taikomas perskyrimo atveju atsiskaitymo grafikui arba grafiko eilutei.</li></ul><p>Šio žymės langelio nustatymo negalima pakeisti prekėms, kurios naudoja sf išrašomos įplaukų funkciją. Be to, nuolaidos negali būti taikomos prekėms, kurios naudoja įplaukų skaidymo metodą.</p> |
| Pradžios data | Pasirinkti perskyrimo ar nuolaidos pradžios datą. |
| Dažnumas | Pasirinkite perskyrimo ar nuolaidos dažnumą: **Nėra**, Mėnesinis **·**, Ketvirtis **·**, **Pusiau kas metus** arba **Kasmet**. |
| Procentai | Nurodyti perskyrimo ar nuolaidos procentą. |
| Suma | Nurodyti perskyrimo ar nuolaidos sumą. |
| Vartotojų kainų indekso grafikas | Pasirinkti vartotojo kainų indekso grafiką, naudojamą skaičiavimams. |
| Pabaigos data | <p>Pasirinkti perskyrimo ar nuolaidos pabaigos datą.</p><p>**Pastaba:** šis laukas būtinas prekėms, kurios naudoja neaprašytų įplaukų funkciją.</p> |
| Atidėjimo grafiko numeris | <p>Atidėjimo grafiko numeris.</p><p>Šis laukas galimas tik kai puslapis atidaromas iš atsiskaitymo grafiko eilutės.</p> |
| Žurnalo numeris | <p>Žurnalo paketo numeris.</p><p>Šis laukas galimas tik kai puslapis atidaromas iš atsiskaitymo grafiko eilutės.</p> |
| Bendroji nuolaidos suma | <p>Nuolaidų sumos visoms tinklelio eilutėms.</p><p>Šis laukas galimas tik kai puslapis atidaromas iš atsiskaitymo grafiko eilutės.</p> |
| Dabartinė trumpalaikių įplaukų, kurios neišskaitomos, suma | <p>Dabartinė trumpalaikių įplaukų, kurios nėra gautos iš sąskaitos, suma.</p><p>Ši suma **rodoma**, kai periodinės sutarties atsiskaitymo parametrų puslapyje pasirinktas trumpalaikis atidėjimo metodas, **o eilutės elemento sąskaitos yra nustatytos sf įplaukų nustatymo** puslapyje.</p> |
| Dabartinė ilgalaikių įplaukų, kurios neišskaitomos, suma | <p>Dabartinė ilgalaikių įplaukų, kurios nėra gautos iš sąskaitos, suma.</p><p>Ši suma **rodoma**, kai periodinės sutarties atsiskaitymo parametrų puslapyje pasirinktas trumpalaikis atidėjimo metodas, **o eilutės elemento sąskaitos yra nustatytos sf įplaukų nustatymo** puslapyje.</p> |

## <a name="proration-examples"></a>Paaikų pavyzdžiai

Pa bookingo skaičiavimai gali būti pagrįsti dienų skaičiumi arba mėnesių skaičiumi. Metodas, naudojamas skaičiuojant paskaitą, nustatytas periodinių sutarties **atsiskaitymo parametrų** puslapyje. Paskaitos metodas veikia tai, kaip apskaičiuojamos sumos atsiskaitymo grafikui šiose situacijose:

- Pradinis kūrimas
- Perskyrimo ar nuolaidos taikymas
- Atleidimas
- Išdėstymo arba šalinimo sulaikymas
- Palaikymo arba atnaujinimo pridėjimas

Šis pakartojimo metodas taip pat turi įtakos mėnesio pasikartojančių įplaukų (MRR) ataskaitos skaičiavimams.

### <a name="example-1"></a>1 pavyzdys

Metinė atsiskaitymo grafiko suma yra $5,000. Pradžios data yra 2019 m. rugpjūčio 12 d., o pabaigos data – 2019 m. gruodžio 22 d. Atsiskaitymo dažnumas yra metinis. Išskaičiuotos sumos yra apskaičiuojamos šiais būdais, atsižvelgiant į tai, ar naudojamas kasdienis, ar mėnesinis skaičiavimo metodas:

- **Kasdienis**

    - *Dienų skaičius Pabaigos* = *data* – *Pradžios data* + 1 = 133 dienos
    - *Metų dienų skaičius* = 2020 m. rugpjūčio 11 d. – 2019 m. rugpjūčio 12 d. + 1 = 366 dienos
    - *Pervertinta* suma = 5000 &times; (133 &divide; 366) = 1816,94

- **Mėnesinis**

    - *Pradžios mėnesio dalis* = (31 – 12 + 1) &divide; 31 = 20 &divide; 31
    - *Vidury mėnesiai* = 3
    - *Mėnesio pabaigos dalis* = 22 &divide; 31
    - Pervertinta suma = 5 000 &divide; 12 &times;\[(20 &divide; 31) + 3 + (22 &divide; 31)\] = 1814,52

### <a name="example-2"></a>2 pavyzdys

Metinė atsiskaitymo grafiko suma yra $12,000. Pradžios data yra 2019 m. rugpjūčio 1 d., o pabaigos data – 2019 m. gruodžio 31 d. Atsiskaitymo dažnumas yra metinis. Išskaičiuotos sumos yra apskaičiuojamos šiais būdais, atsižvelgiant į skaičiavimo metodą:

- **Kasdienis**

    - *Dienų skaičius Pabaigos* = *data* – *Pradžios data* + 1 = 153 dienos
    - *Metų dienų skaičius* = 2020 m. liepos 31 d. – 2019 m. rugpjūčio 1 d. + 1 = 366 dienos
    - *Pervertinta* suma = 12 000 &times; (153 &divide; 366) = 5016,39

- **Mėnesinis (visas mėnuo)**

    - *Mėnesių skaičius* = 5
    - *Iš viso mėnesių* = 12
    - *Pervertinta* suma = (12 000 &times; 5) &divide; 12 = 5 000

## <a name="reversing-a-period-billing"></a>Laikotarpio atsiskaitymo atšaukimas

Pavyzdžiui, atsiskaitymo grafikas turi tik vieną eilutę:

- Sąskaitas galima pateikti kas mėnesį 12 mėnesių nuo sausio iki gruodžio mėn.
- SF sukurtos visiems laikotarpiams iki balandžio pabaigos.

Norite atšaukti balandžio atsiskaitymo laikotarpio SF.

Jei pardavimo SF dar nebuvo sukurta balandžio atsiskaitymo laikotarpiui, galite panaikinti pardavimo užsakymą. Šiuo atveju bus **pašalinta informacijos** būsena Išrašyta sąskaita. Tačiau, kadangi sukurta atsiskaitymo laikotarpio SF, **informacijos** būsenos Išrašyta sąskaita ištrinti negalima. Todėl, norėdami atšaukti sąskaitą balandžio mėnesį, turite sukurti eilutės korespondentinę kredito pažymą.

1. Puslapyje Visi **sąskaitų pateikimo grafikai** sukurkite tos pačios prekės grafiko eilutę.
2. **Pakeiskite prekės** kiekio vertę į neigiamą pradinį kiekį.
3. Nustatykite **atsiskaitymo dažnumo** lauką **kaip Vienkartinis**.
4. Atnaujinkite pradžios ir pabaigos datas, kad jos atitiktų atsiskaitymo informacijos eilutės, kurios kredito pažymą norite kurti, datas. Pavyzdžiui, nustatykite pradžios datą kaip 2019 m. balandžio 1 d., o pabaigos datą – 2019 m. balandžio 30 d.
5. Įrašykite pakeitimus.
6. Atidarykite **SF generavimo** puslapį ir sukurkite pardavimo užsakymą, kuriame yra nurodyto laikotarpio kredito pažyma.
7. Pasirinktinai: užregistruokite SF.

Kai peržiūrite atsiskaitymo grafiko eilutes, jūs atkreipkite dėmesį, kad nauja eilutė yra nuoroda į kredito pažymą. Pradinė eilutė vis tiek bus saitas į pradinę balandžio SF.

## <a name="split-item-group-examples"></a>Prekių grupių skirstyti pavyzdžius

Pavyzdžiui, yra šis nustatymas:

- Periodinio **sutarties atsiskaitymo parametrų puslapyje** pasirenkama **grupė** Skaidyti pagal prekę, o laukas **Unikalus grafiko tipas** nustatytas kaip **Klientas**.
- Sukurtos trys prekių grupės: PREFIX **,** DATAHUB **ir** SPP **.**
- Kliento US-001 turi keletą atsiskaitymo grafikų, kuriuose prekių grupė yra PREFIX ar DATAHUB.
- Kliento US-002 turi keletą atsiskaitymo grafikų, kuriuose prekių grupė yra PREFIX arba SPP.

| Atsiskaitymo grafiko numeris | Klientas | Prekių grupė |
|---|---|---|
| JŪSŲ 001 | US-001 | PRIEŠDĖLIS |
| JŪSŲ 002 | US-001 | DUOMENŲ BUTAS |
| JŪSŲSA003 | US-002 | PRIEŠDĖLIS |
| JŪSŲ, 004 | US-002 | SPP |

Klientas US-001 perka atnaujinimo prekę, kuri priklauso PREFIX prekių grupei. Ši operacija yra naujas pardavimo užsakymas.

| Pardavimo užsakymas # | Klientas | Pagrindinė prekė | Atnaujinimo elementas | Atnaujinimo prekių grupė | Atsiskaitymo grafiko numeris |
|---|---|---|---|---|---|
| SO0001 | US-001 | D0001 | D0002 | PRIEŠDĖLIS | JŪSŲ 001 |

Užregistrus pardavimo užsakymo SF, atnaujinimo prekė įtraukiama į esamą kliento sąskaitų pateikimo grafiką (=001). Šiame atsiskaitymo grafike naudojama PREFIX prekių grupė. Visos atnaujinimo prekės, priklausančios tai pačiai prekių grupei, yra patalpinos į tą patį sąskaitų pateikimo grafiką.

**Antraštė**
 
| Atsiskaitymo grafiko numeris | Klientas | Prekių grupė |
|---|---|---| 
| JŪSŲ 001 | US-001 | PRIEŠDĖLIS |

**Eilutė**

| Atsiskaitymo grafiko numeris | Klientas | Prekių grupė |
|---|---|---|
| JŪSŲ 001 | US-001 | D0002 |

Dabar US-001 klientas perka atnaujinimo prekę, kuri priklauso SPP prekių grupei. Ši operacija yra naujas pardavimo užsakymas.

| Pardavimo užsakymas # | Klientas | Pagrindinė prekė | Atnaujinimo elementas | Atnaujinimo prekių grupė | Atsiskaitymo grafiko numeris |
|---|---|---|---|---|---|
| SO0002 | US-001 | D0003 | D0004 | SPP | |

Šiuo metu kliento US-001 nėra sąskaitų pateikimo grafiko, kuriame naudojama SPP prekių grupė. Todėl sukuriamas naujas sąskaitų pateikimo grafikas.

**Antraštė**

| Atsiskaitymo grafiko numeris| Klientas | Prekių grupė |
|---|---|---|
| JŪSŲ 005 | US-001 | SPP |

**Eilutė**

| Atsiskaitymo grafiko numeris | Klientas | Prekių grupė |
|---|---|---|
| JŪSŲ 005 | US-001 | D0004 |

### <a name="multiple-billing-schedules-for-the-same-end-user-and-customer"></a>Keli to paties galutinio vartotojo ir kliento atsiskaitymo grafikai

Pavyzdžiui, yra šis nustatymas:

- Periodinio **sutarties atsiskaitymo parametrų puslapyje** pasirenkama **grupė** Skaidyti pagal prekę, o laukas **Unikalus grafiko tipas** nustatytas kaip **Galutinis vartotojas**.
- **Galutinių vartotojų puslapyje** nustatytas toks klientų ir galutinių vartotojų ryšys.

    | Kliento kodas | Galutinio vartotojo sąskaita |
    |---|---|
    | US-001 | US-221 |

Kliento ir galutinio vartotojo kombinacijai sukurti keli sąskaitų pateikimo grafikai. Kadangi **pasikartojančios sutarties atsiskaitymo** parametrų puslapyje **pasirinkta Skaidyti pagal prekių** grupę, galima sukurti keletą to paties kliento ir galutinio vartotojo ryšių atsiskaitymo grafikų.

| Atsiskaitymo grafiko numeris | Klientas | Galutinio vartotojo sąskaita | Antraštės prekių grupė |
|---|---|---|---|
| JŪSŲ 005 | US-001 | US-221 | GS1 |
| JŪSŲ 006 | US-001 | US-221 | GS2 |
| JŪSŲ 007 | US-001 | US-221 | GS3 |

Prekių nustatymo **puslapyje sukuriate** prekių ryšių palaikymą ir atnaujinimą.

| Prekės kodas | Prekės ryšys | Palaikymo elementas | Atnaujinimo elementas | Atnaujinimo prekių grupė |
|---|---|---|---|---|
| Lentelė | D001 | 27 PREKĖ | D007 | GS1 |
| Lentelė | D002 | 28 PREKĖ | D005 | GS2 |
| Lentelė | D003 | 29 PREKĖ | D006 | GS3 |

Dabar sukuriate pardavimo užsakymą klientui US-001. Šiame pardavimo užsakyme yra prekių iš **prekių nustatymo** puslapio. Kai sukuriate pardavimo užsakymą, atidarykite **palaikymo** ir atnaujinimo proceso puslapį ir **nustatykite** galutinio vartotojo sąskaitos lauką ir visą kitą reikiamą informaciją apie atnaujinimo prekę.

Kai sukuriama ir užregistruojama operacijos SF, sukuriami skirtingi kliento / galutinio vartotojo ir prekių grupės derinio sąskaitų pateikimo grafikai. Tam pačiam sąskaitų pateikimo grafikui galima priskirti daugiau nei vieną to paties pardavimo užsakymo eilutę.

| Pardavimo užsakymas # | Klientas | Galutinio vartotojo sąskaita | Pagrindinė prekė | Palaikymo elementas | Atnaujinimo elementas | Atsiskaitymo grafiko numeris |
|---|---|---|---|---|---|---|
| SO0001 | US-001 | US-221 | D001 | 27 PREKĖ | D007 | JŪSŲ 005 |
| SO0001 | US-001 | US-221 | D002 | 28 PREKĖ | D005 | JŪSŲ 006 |
| SO0001 | US-001 | US-221 | D003 | 29 PREKĖ | D006 | JŪSŲ 005 |
