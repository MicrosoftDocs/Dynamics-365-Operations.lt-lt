---
title: Nuo šalies konteksto priklausančio ER modelio susiejimų konfigūravimas
description: Šioje temoje aiškinama, kaip nustatyti ER modelio susiejimus, kad jie priklausytų nuo juridinio objekto, kuris valdo susiejimų naudojimą, šalies / regiono konteksto.
author: NickSelin
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.openlocfilehash: 5b26c605bd64b8d8e5a90f4389261e8e56825111
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605376"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a>Nuo šalies konteksto priklausančio ER modelio susiejimų konfigūravimas

[!include[banner](../includes/banner.md)]

Galite konfigūruoti elektroninių ataskaitų (ER) modelio susiejimus, kad jie naudotų bendrąjį ER duomenų modelį, bet būtų būdingi „Dynamics 365 Finance“. Šioje temoje aiškinama, kaip sukurti ER duomenų modelio ER modelio susiejimus, kad jų naudojimas atitiktų atitinkamus ER formatus, kuriuos naudoja įmonės pagal skirtingus šalies / regiono kontekstus.

## <a name="prerequisites"></a>Būtinieji komponentai

Norint įvykdyti šios temos pavyzdžių užduotis, reikia toliau nurodytų prieigų.

- Prieiga prie „Finance“ naudojant vieną iš tolesnių vaidmenų.
    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

- Prieiga prie „Regulatory Configuration Services“ (RCS) egzemplioriaus, kuris buvo pateiktas tam pačiam nuomotojui kaip „Finance“ dėl vieno iš šių vaidmenų:
    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

Norint atlikti kai kuriuos šios temos veiksmus, reikia įgyvendinti ER formatą. Kai kuriais atvejais ER formato įgyvendinimui turi įtakos įmonės, prie kurios šiuo metu esate prisijungę, šalies / regiono kontekstas. Galite paleisti ER formatą dabartiniame RCS egzemplioriuje, jei įmonė, kuriai reikia šalies / regiono konteksto, yra galima RCS. Kitu atveju, turite įkelti visą ER modelio susiejimo versiją ir ER formato konfigūracijas, kurios naudoja ER duomenų modelį jūsų „Finance“ egzemplioriuje, tada paleisti ER formatą „Finance“ egzemplioriuje. Informaciją, kaip importuoti konfigūracijas, kurios yra RCS, į „Finance“ egzempliorių, žr. [Konfigūracijų importavimas iš RCS](rcs-download-configurations.md).

## <a name="single-model-mapping-case"></a>Vieno modelio susiejimo atvejis

Atlikite šios temos [1 priedas](#appendix1) nurodytus veiksmus, kad sukurtumėte būtinus ER komponentus. Dabar turite modelio susiejimo konfigūraciją **Susiejimas (bendrasis)**, kuriame yra **1 įvesties taškas** modelio susiejimo apibrėžimas.

![ER konfigūracijų puslapis, Formatas, skirtas susiejimų konfigūracijai sužinoti.](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a>Sukonfigūruoto formato paleidimas

1.  **Konfigūracijų puslapis**, esančio „FastTab“ **Versijos**, pasirinkite **Paleisti**.
2.  Pasirinkite **Gerai**.

Atkreipkite dėmesį, kad žiniatinklio naršyklė siūlo atsisiųsti tekstinį failą, kurį sugeneravo įvykdytas ER formatas. Kadangi šis formatas buvo sukurtas naudoti **1 įvesties taškas** apibrėžimą, o baziniam modeliui, kuriame yra susiejimas, skirtas šiam apibrėžimui, šiuo metu yra galimas tik vieno modelio susiejimas, įvykdytas ER formatas konfigūracijos **Susiejimas (bendrasis)** modelio susiejimą **Susiejimas (bendrasis)** naudojo kaip duomenų šaltinį. Todėl atsisiųstame faile yra tekstas **1 bendrasis funkcionalumas**.

## <a name="multiple-shared-model-mappings-case"></a>Kelių bendrinamų modelio susiejimų atvejis

Atlikite šios temos [2 priedas](#appendix2) nurodytus veiksmus, kad sukurtumėte būtinus ER komponentus. Dabar turite modelio susiejimo konfigūracijas **Susiejimas (bendrasis)** ir **Pasirinktinis susiejimas (bendrasis)**, kurių kiekvienoje yra modelio susiejimas, skirtas **1 įvesties taškas** apibrėžimui.

![ER konfigūracijos puslapis, Susiejimo bendroji pasirinktinė konfigūracija.](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a>Sukonfigūruoto formato paleidimas

1.  Puslapyje **Konfigūracijos** konfigūracijų medyje pasirinkite **Formatas, skirtas išmokti susiejimus**.
2.  „FastTab“ **Versijos** pasirinkite **Vykdyti**.
3.  Pasirinkite **Gerai**.

Atkreipkite dėmesį, kad pasirinktas ER formatas nepavyko. Klaidos pranešime nurodoma, kad modelis **Modelis, skirtas išmokti susiejimus** ir **1 įvesties taškas** apibrėžimas, esantys modelio susiejimo konfigūracijose **Susiejimas (bendrasis)** ir **Pasirinktinis susiejimas (bendrasis)**, turi daugiau nei vieną modelio susiejimą. Pranešime taip pat rekomenduojama vieną iš šių konfigūracijų pasirinkti kaip numatytąją konfigūraciją.

![ER konfigūracijos puslapis su klaidos pranešimu.](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a>Numatytosios susiejimo konfigūracijos apibrėžimas

Atlikite šiuos veiksmus, kad apibrėžtumėte modelio susiejimo konfigūraciją **Pasirinktinis (bendrasis) susiejimas** kaip numatytąją konfigūraciją, kad jos susiejimą galėtumėte naudoti kaip ER formato **Formatas, skirtas išmokti susiejimus** duomenų šaltinį.

1.  Puslapyje **Konfigūracijos** konfigūracijų medyje pasirinkite **Pasirinktinis susiejimas (bendrasis)**.
2.  Kaip reikalaujama, pasirinkite **Redaguoti**, kad galėtumėte redaguoti esamą puslapį.
3.  Nustatykite parinktį **Numatytasis modelių susiejimui** į **Taip**.
4.  Pasirinkite **Įrašyti**.

![ER konfigūracijų puslapis, Numatytas modelio susiejimas nustatytas į Taip.](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a>Sukonfigūruoto formato paleidimas

1.  Puslapyje **Konfigūracijos** konfigūracijų medyje pasirinkite **Formatas, skirtas išmokti susiejimus**.
2.  „FastTab“ **Versijos** pasirinkite **Vykdyti**.
3.  Pasirinkite **Gerai**.

Atkreipkite dėmesį, kad pasirinktas ER formatas pavyko. Žiniatinklio naršyklė siūlo atsisiųsti tekstinį failą, kurį sugeneravo įvykdytas ER formatas. Kadangi šis formatas sukonfigūruotas, kad būtų galima naudoti **1 įvesties taškas** apibrėžimą, o modelio **Pasirinktinis (bendrasis) susiejimas** susiejimo konfigūracija buvo pasirinkta kaip numatytoji konfigūracija, įvykdytas ER formatas naudojo konfigūracijos **Pasirinktinis (bendrasis) susiejimas** modelio **Susiejimas (bendrasis) kopija** konvertavimą kaip duomenų šaltinį. Todėl atsisiųstame faile yra **1 bendrosios funkcijos** tekstas.

> [!NOTE]
> Jei pakeisite įmonę, kurioje šiuo metu esate prisiregistravę, ir dar kartą paleisite šį ER formatą, sugeneruotame faile gausite tokį patį turinį, nes numatytoje ER modelio susiejimo konfigūracijoje nėra jokių įmonei priklausančių apribojimų.

## <a name="multiple-mixed-model-mappings-case"></a>Kelių mišrių modelio susiejimų atvejis

Atlikite veiksmus, nurodytus šios temos [3 priedas](#appendix3), kad sukurtumėte reikalingus ER komponentus. Dabar turite konfigūracijas **Susiejimas (bendrasis)**, **Pasirinktinis (bendrasis) susiejimas** ir **Modelio susiejimo susiejimas (ER)**, kuriose yra modelio susiejimas, skirtas **1 įvesties taškas** apibrėžimui.

Atkreipkite dėmesį, kad modelio susiejimo konfigūracijos **Susiejimas (FR)** 1 versija yra sukonfigūruota taip, kad ji būtų taikoma tik modelio **Modelis, skirtas sužinoti apie susiejimus**, kuris vykdomas „Finance“ įmonėse, kurioms būdingas Prancūzijos šalies / regiono kontekstas, ER formatams.

![ER konfigūracijos puslapis, Modelio susiejimo (FR) konfigūracija.](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a>Sukonfigūruoto formato paleidimas

1.  Pakeiskite įmonę į **FRSI**.
2.  Puslapyje **Konfigūracijos** konfigūracijų medyje pasirinkite **Formatas, skirtas išmokti susiejimus**.
3.  „FastTab“ **Versijos** pasirinkite **Vykdyti**.
4.  Pasirinkite **Gerai**.

Atkreipkite dėmesį, kad pasirinktas ER formatas pavyko. Interneto naršyklė siūlo atsisiųsti tekstinį failą, kurį sugeneravo įvykdytas ER formatas. Kadangi šis formatas sukonfigūruotas, kad būtų galima naudoti **1 įvesties taškas** apibrėžimą, o modelio **Pasirinktinis (bendrasis) susiejimas** susiejimo konfigūracija buvo pasirinkta kaip numatytoji konfigūracija, įvykdytas ER formatas naudojo konfigūracijos **Pasirinktinis (bendrasis) susiejimas** modelio **Susiejimas (bendrasis) kopija** konvertavimą kaip duomenų šaltinį. Todėl atsisiųstame faile yra **1 bendrosios funkcijos** tekstas.

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a>Prancūzijai būdingo susiejimo konfigūracijos nustatymas kaip numatytoji konfigūracija

Atlikite šiuos veiksmus, norėdami apibrėžti pasirinktinę modelio **Susiejimas (FR)** susiejimo konfigūraciją kaip numatytąją konfigūraciją. Atkreipkite dėmesį, kad šis susiejimas yra būdingas Prancūzijai ir jis bus laikomas numatytuoju susiejimu tarp visų modelio susiejimo konfigūracijų, kurios turi **FR** šalies kodą, nurodytą lauke **ISO šalių / regionų kodai**.

1.  Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite **Susiejimas (FR)**.
2.  Kaip reikalaujama, pasirinkite **Redaguoti**, kad galėtumėte redaguoti esamą puslapį.
3.  Nustatykite parinktį **Numatytasis modelių susiejimui** į **Taip**.
4.  Pasirinkite **Įrašyti**.

![ER konfigūracijų puslapis, Susiejimo (FR) konfigūracija, Numatytas modelio susiejimas nustatytas į Taip.](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a>Sukonfigūruoto formato paleidimas

1.  Puslapyje **Konfigūracijos** konfigūracijų medyje pasirinkite **Formatas, skirtas išmokti susiejimus**.
2.  „FastTab“ **Versijos** pasirinkite **Vykdyti**.
3.  Pasirinkite **Gerai**.

Atkreipkite dėmesį, kad pasirinktas ER formatas pavyko. Interneto naršyklė siūlo atsisiųsti tekstinį failą, kurį sugeneravo įvykdytas ER formatas. Kadangi šis formatas sukonfigūruotas, kad būtų galima naudoti **1 įvesties taškas** apibrėžimą, o modelio **Susiejimas (FR)** susiejimo konfigūracija buvo pasirinkta kaip numatytoji konfigūracija, įvykdytas ER formatas naudojo konfigūracijos **Susiejimas (FR)** modelio **Susiejimas (bendrasis) kopija** konvertavimą kaip duomenų šaltinį. Todėl atsisiųstame faile yra **1 FR funkcija** tekstas.

> [!NOTE]
> Jei pakeičiate įmonę, prie kurios šiuo metu esate prisijungę, ir dar kartą vykdote šį ER formatą, išvestis priklausys nuo pasirinktos įmonės šalies / regiono konteksto.

## <a name="other-model-mapping-cases"></a>Kiti modelio susiejimo atvejai

Kaip jau matėte, modelio susiejimo pasirinkimas, norint vykdyti ER formatą, veikia toliau nurodytu būdu.

- Modelio susiejimo aprašas, kurį naudoja ER formatas, yra nurodytas (šios temos **1 įvesties taškas** pavyzdžiuose).
- Visos susiejimo konfigūracijos, kuriose yra susiejimas su nurodytu aprašu ir kuris tenkina bet kurį sukonfigūruotą šalies / regiono konteksto apribojimą, gali potencialiai būti naudojamos norint vykdyti ER formatą (**Susiejimas (bendrasis)**, **Pasirinktinis susiejimas (bendrasis)** ir **Susiejimas (FR)** pavyzdžiai, pateikti šioje temoje).
- Bet kuris numatytasis susiejimas, kuris turi šalies / regiono konteksto apribojimą, turi aukščiausią pasirinkimo prioritetą (**Susiejimas (FR)** pavyzdžiai, pateikti šioje temoje).
- Bet kuris numatytasis susiejimas, kuris neturi šalies / regiono konteksto apribojimo, turi kitą aukščiausią pasirinkimo prioritetą (**Pasirinktinis susiejimas (bendrasis)** pavyzdžiai, pateikti šioje temoje).
- Bet kuris modelio susiejimas, kuri turi šalies / regiono konteksto apribojimus, turi aukštesnį pasirinkimo prioritetą, nei modelio susiejimas, kurie neturi šalies / regiono konteksto apribojimo.

Toliau pateiktoje lentelėje pateikiama informacija apie modelio susiejimo pasirinkimą visiems galimiems atvejams pagal modelio susiejimo parametrus, rezultatai.

- 1 stulpelyje nurodoma, ar pirmasis modelio susiejimas, kuris neturi šalies / regiono konteksto apribojimų (pavyzdžiui, bendrintas **Susiejimas (Bendrasis)** susiejimas) yra, ir jei yra, ar jo parinktis **Modelio susiejimo numatytasis parametras** nustatytas kaip **Taip**.
- 2 stulpelyje nurodoma, ar antrasis modelio susiejimas, kuris neturi šalies / regiono konteksto apribojimų (pavyzdžiui, bendrintas **Pasirinktinis susiejimas (Bendrasis)** susiejimas) yra, ir jei yra, ar jo parinktis **Modelio susiejimo numatytasis parametras** nustatytas kaip **Taip**.
- 3 stulpelyje nurodoma, ar pirmasis modelio susiejimas, kuris turi šalies / regiono A konteksto apribojimus (pavyzdžiui, Prancūzijai būdingas **Susiejimas (FR)** susiejimas) yra, ir jei yra, ar jo parinktis **Modelio susiejimo numatytasis parametras** nustatytas kaip **Taip**.
- 4 stulpelyje nurodoma, ar antrasis modelio susiejimas, kuris turi šalies / regiono A konteksto apribojimus, yra, ir jei yra, ar parinktis **Modelio susiejimo numatytasis parametras** nustatyta kaip **Taip**.
- 5 stulpelyje pateikiami modelio susiejimo pasirinkimo, norint vykdyti ER formatą valdant įmonei, kuriai būdingas šalies / regiono A kontekstas, rezultatas.
- 6 stulpelyje pateikiami modelio susiejimo pasirinkimo, norint vykdyti ER formatą valdant įmonei, kuriai būdingas šalies / regiono B kontekstas, rezultatas.

Lentelėje pliuso ženklas (+) nurodo, kad modelio susiejimo konfigūracija yra esamame „Microsoft Azure“ paslaugos, kuri naudojama norint vykdyti ER formatą („Finance“ arba RCS), egzemplioriuje.

| Saugykla | 1 modelio susiejimas be šalies/regiono konteksto (MM1) | 2 modelio susiejimas be šalies/regiono konteksto (MM2) | 1 modelio susiejimas su šalies/regiono A kontekstu (MM1A) | 2 modelio susiejimas su šalies/regiono A kontekstu (MM2A) | Vykdyti valdant įmonei, kuriai būdingas šalies / regiono A kontekstas | Vykdyti valdant įmonei, kuriai būdingas šalies / regiono B kontekstas |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     1   |     2   |    3    |    4    |           5               |            6               |
|     1   |         |         |         |         | Klaida (trūksta susiejimo)   | Klaida (trūksta susiejimo)    |
|     2   |     +   |         |         |         | MM1                       | MM1                        |
|     3   |     +   |     +   |         |         | Klaida (keli susiejimai) | Klaida (keli susiejimai)  |
|     4   |     +   |         |    +    |         | MM1A                      | MM1                        |
|     5   |     +   |         |    +    |    +    | Klaida (keli susiejimai) | MM1                        |
|     6   |     +   | numatytasis |    +    |    +    | MM2                       | MM2                        |
|     7   |     +   |         | numatytasis |         | MM1A                      | MM1                        |
|     8   |     +   |         | numatytasis |    +    | MM1A                      | MM1                        |
|     9   |     +   |         | numatytasis | numatytasis | Klaida (keli susiejimai) | MM1                        |
|    10   | numatytasis |         |         |         | MM1                       | MM1                        |
|    11   | numatytasis |    +    |         |         | MM1                       | MM1                        |
|    12   | numatytasis |         |    +    |         | MM1                       | MM1                        |
|    13   | numatytasis | numatytasis |         |         | Klaida (keli susiejimai) | Klaida (keli susiejimai)  |
|    14   | numatytasis |         | numatytasis |         | MM1A                      | MM1                        |
|    15   | numatytasis |         | numatytasis | numatytasis | MM1A                      | MM2A                       |
|    16   |         |         |    +    |    +    | MM1A                      | MM2A                       |
|    17   |         |         | numatytasis | numatytasis | MM1A                      | MM2A                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a>Sužinokite, koks susiejimas buvo naudojamas vykdant ER formatą

### <a name="configure-er-user-parameters"></a>ER naudotojo parametrų konfigūravimas

1.  Puslapio **Konfigūracijos** veiksmų srities skirtuke **KONFIGŪRACIJOS** pasirinkite **Vartotojo parametrai**.
2.  Nustatykite parinktį **Vykdyti derinimo režimu** kaip **Taip**.
4.  Pasirinkite **Gerai**.

### <a name="run-the-configured-format"></a>Sukonfigūruoto formato paleidimas

1.  Puslapyje **Konfigūracijos** konfigūracijų medyje pasirinkite **Formatas, skirtas išmokti susiejimus**.
2.  „FastTab“ **Versijos** pasirinkite **Vykdyti**.
3.  Pasirinkite **Gerai**.

### <a name="review-the-er-debug-log"></a>ER derinimų žurnalo peržiūra

1.  Naršymo srityje eikite į **Moduliai \> Organizacijos administravimas \> Elektroninė ataskaita \> Derinimų žurnalo konfigūracija**.
2.  Pasirinkite mygtuką **Iš naujo įkelti šį puslapį**.

![ER vykdymo žurnalų puslapis.](./media/RCS-Context-specific-mapping-DebugLog.PNG)

Atkreipkite dėmesį, kad naujas įrašas buvo įtrauktas į įvykdyto ER formato ER derinimų žurnalą. Kadangi šio įrašo laukas **Lygis** nustatytas kaip **Informacinis**, įrašas yra informacinis. Kadangi formato komponento laukas nustatytas kaip **Susiejimo konfigūracija**, įraše pateikiama informacija apie modelio susiejimą, kuris buvo naudojamas vykdant ER formatą **Formatas, skirtas sužinoti apie susiejimus** (pasirinktas lauke **Konfigūracijos pavadinimas**). Lauko **Sugeneruotas tekstas** kontekste pateikiama informacija apie tai, kad **Susiejimas (FR)** susiejimo komponentas, kuris yra konfigūracijoje **Susiejimas (FR)**, buvo naudotas vykdyti šią ataskaitą.

## <a name="appendix-1"></a><a name="appendix1"></a>1 priedas

### <a name="configure-a-sample-data-model"></a>Pavyzdžio duomenų modelio konfigūravimas

Prisijunkite prie savo RCS egzemplioriaus.

Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc.“ konfigūraciją. Norėdami atlikti šiuos veiksmus, pirmiausia RCS turite atlikti veiksmus, nurodytus [Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedūroje.

#### <a name="create-an-er-data-model-configuration"></a>ER duomenų modelio konfigūracijos kūrimas

1.  Numatytoje ataskaitų srityje pasirinkite **Elektroninės ataskaitos**.
2.  Pasirinkite plytelę **Ataskaitų konfigūracijos**.
3.  Puslapyje **Konfigūracijos** pasirinkite **Kurti konfigūraciją**.
4.  Išplečiamojo dialogo lango lauke **Pavadinimas** įveskite **Modelis, kuris skirtas sužinoti apie susiejimus**.
5.  Pasirinkite **Kurti konfigūraciją**.
6.  „FastTab“ pasirinkite **Konfigūracijos komponentai**.

Atkreipkite dėmesį, kad šios ER konfigūracijos 1 juodraščio versija parengta redaguoti. Šioje versijoje yra duomenų modelio komponentas.

#### <a name="design-a-sample-data-model"></a>Pavyzdžio duomenų modelio kūrimas

1.  Puslapyje **Konfigūracijos** pasirinkite **Dizaino įrankis**.
2.  Pasirinkite **Naujas**.
3.  Išplečiamojo dialogo lango lauke **Pavadinimas** įveskite **1 įvesties taškas**.
4.  Pasirinkite **Įtraukti**.
5.  Pasirinkite **Naujas**.
6.  Išplečiamojo dialogo lango lauke **Pavadinimas** įveskite **Funkcijos aprašas**.
7.  Pasirinkite **Įtraukti**.
8.  Pasirinkite **Naujas**.
9.  Išplečiamojo dialogo lango lauko grupėje **Naujas mazgas** pasirinkite **Modelio šaknis**.
10. Lauke **Pavadinimas** įveskite **2 įvesties taškas**.
11. Pasirinkite **2 įvesties taškas**.
12. Pasirinkite **Įtraukti**.
13. Pasirinkite **Naujas**.
14. Išplečiamojo dialogo lango lauke **Pavadinimas** įveskite **Funkcijos aprašas**.
15. Pasirinkite **Įtraukti**.

    ![ER duomenų modelio dizaino įrankio puslapis.](./media/RCS-Context-specific-mapping-Model.PNG)

16. Pasirinkite **Įrašyti**.
17. Uždarykite puslapį.

#### <a name="complete-the-modified-version-of-the-model-configuration"></a>Modelio konfigūracijos modifikuotos versijos užbaigimas

1.  Puslapio **Konfigūracijos** „FastTab“ **Versijos** pasirinkite **Keisti būseną**.

    > Pakeiskite sukurtos modelio konfigūracijos būseną iš **Juodraštis** į **Baigta**, kad ją būtų galima naudoti norint sukurti reikalingus modelio susiejimus ir formatus.

2.  Pasirinkite **Baigti**.
3.  Pasirinkite **Gerai**.

Atkreipkite dėmesį, kad sukurta konfigūracija įrašoma kaip 1 baigta versija.

### <a name="configure-a-sample-model-mapping"></a>Pavyzdžio modelio susiejimo konfigūravimas

#### <a name="create-an-er-model-mapping-configuration"></a>ER modelio susiejimo konfigūracijos kūrimas

1.  Puslapyje **Konfigūracijos** pasirinkite **Kurti konfigūraciją**.
2.  Išplečiamojo dialogo lango laukų grupėje **Naujas** pasirinkite parinktį **Modelio susiejimas, pagrįstas duomenų modeliu „Modelis, skirtas sužinoti apie susiejimus“**.
3.  Lauke **Pavadinimas** įveskite **Susiejimas (bendrasis)**.
4.  Lauke **Duomenų modelio aprašas** pasirinkite **1 įvesties taškas**.
5.  Pasirinkite **Kurti konfigūraciją**.

Atkreipkite dėmesį, kad šios ER konfigūracijos 1 juodraščio versija parengta redaguoti. Šioje versijoje yra modelio susiejimo komponentas.

#### <a name="design-a-sample-model-mapping"></a>Pavyzdžio modelio susiejimo kūrimas

1.  Puslapyje **Konfigūracijos** pasirinkite **Dizaino įrankis**.

    Atkreipkite dėmesį, kad **Į modelį** krypties tipo modelio susiejimas buvo automatiškai įtrauktas į šį komponentą ir yra skirtas **1 įvesties taškas** apibrėžimui.
    
2.  Pasirinkite **Dizaino įrankis**, kad pradėtumėte redaguoti įtrauktą modelio susiejimą.
3.  Skyriuje **Duomenų modelis** pasirinkite **Redaguoti**.
4.  Lauke **Formulė** įveskite **1 bendroji funkcija**.
5.  Pasirinkite **Įrašyti**.
6.  Uždarykite puslapį **Formulės konstruktorius**.

    ![ER modelio susiejimo dizainerio puslapis, 1 įvesties punkto aprašas.](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  Pasirinkite **Įrašyti**.
8.  Uždarykite puslapį **Modelio susiejimo dizaino įrankis**.
9.  Pasirinkite **Naujas**.
10. Lauke **Aprašas** pasirinkite **2 įvesties taškas**.
11. Lauke **Pavadinimas** įveskite **2 susiejimas (bendrasis)**.
12. Pasirinkite **Dizaino įrankis**.
13. Skyriuje **Duomenų modelis** pasirinkite **Redaguoti**.
14. Lauke **Formulė** įveskite **2 bendroji funkcija**.
15. Pasirinkite **Įrašyti**.
16. Uždarykite puslapį **Formulės konstruktorius**.

    ![ER modelio susiejimo dizainerio puslapis, 2 įvesties punkto aprašas.](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. Pasirinkite **Įrašyti**.
18. Uždarykite puslapį **Modelio susiejimo dizaino įrankis**.

    ![ER modelio susiejimo puslapis su įvesties punkto aprašais.](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. Uždarykite puslapį **Modelio susiejimai**.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Modelio susiejimo konfigūracijos modifikuotos versijos užbaigimas

1.  Puslapio **Konfigūracijos** „FastTab“ **Versijos** pasirinkite **Keisti būseną**.

    > Pakeiskite sukurtos modelio susiejimo konfigūracijos būseną iš **Juodraštis** į **Baigta**, kad ją galėtų naudoti ER formatai.

2.  Pasirinkite **Baigti**.
3.  Pasirinkite **Gerai**.

Atkreipkite dėmesį, kad sukurta konfigūracija įrašoma kaip 1 baigta versija.

### <a name="configure-a-sample-format"></a>Pavyzdinio formato konfigūravimas

#### <a name="create-an-er-format-configuration"></a>ER formato konfigūracijos kūrimas

1.  Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite elementą **Modelis, skirtas sužinoti apie susiejimus**.
2.  Pasirinkite **Kurti konfigūraciją**.
3.  Išplečiamojo dialogo lango laukų grupėje **Naujas** pasirinkite parinktį **Formatas pagal duomenų modelį „Modelis, skirtas sužinoti apie susiejimus“**.
4.  Lauke **Pavadinimas** įveskite **Formatas, skirtas sužinoti apie susiejimus**.
5.  Lauke **Duomenų modelio aprašas** pasirinkite **1 įvesties taškas**.
6.  Pasirinkite **Kurti konfigūraciją**.

Atkreipkite dėmesį, kad šios ER konfigūracijos 1 juodraščio versija parengta redaguoti. Šioje versijoje yra formato komponentas.

#### <a name="design-a-sample-format"></a>Pavyzdžio formato kūrimas

1.  Puslapyje **Konfigūracijos** pasirinkite **Dizaino įrankis**.
2.  Pasirinkite **Įtraukti šaknį**.
3.  Grupėje **Tekstas** pasirinkite elementą **Eilutė**.
4.  Pasirinkite **Gerai**.

#### <a name="bind-format-elements-to-a-data-source"></a>Formato elementų susiejimas su duomenų šaltiniu

1.  Puslapyje **Formato dizaino įrankis** skirtuke **Susiejimas** išplėskite modelio duomenų šaltinį.
2.  Pasirinkite lauką **Funkcijos aprašymas**.
3.  Pasirinkite **Susieti**.

    ![ER formato dizaino įrankio puslapis.](./media/RCS-Context-specific-mapping-Format.PNG)

4.  Pasirinkite **Įrašyti**.
5.  Uždarykite puslapį.

## <a name="appendix-2"></a><a name="appendix2"></a>2 priedas

### <a name="configure-a-sample-model-mapping-for-general-customization"></a>Pavyzdinio modelio susiejimo konfigūravimas bendrajam tinkinimui

Galite norėti tinkinti modelio susiejimą, kurį jums pateikė konfigūracijų teikėjas (partneris), tada naudoti tikintą versiją kaip ER formatų duomenų šaltinį. Tokiu atveju turite sukurti pasirinktinę ER modelio susiejimo konfigūraciją, kad būtų atlikti reikiami esamų modelio susiejimų pakeitimai. Šio priedo procedūroje kaip pavyzdys naudojamas **Susiejimas (bendrasis)** modelio susiejimas.

#### <a name="create-an-er-model-mapping-configuration"></a>ER modelio susiejimo konfigūracijos kūrimas

1.  Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite **Susiejimas (bendrasis)**.
2.  Pasirinkite **Kurti konfigūraciją**.
3.  Išplečiamajame dialogo lango lauko grupėje **Naujas** pasirinkite **Išvesti iš pavadinimo: susiejimas (bendrasis), „Litware, Inc“**.
4.  Lauke **Pavadinimas** įveskite **Pasirinktinis susiejimas (bendrasis)**.
5.  Pasirinkite **Kurti konfigūraciją**.

Atkreipkite dėmesį, kad šios ER konfigūracijos 1 juodraščio versija parengta redaguoti.

#### <a name="design-a-sample-model-mapping"></a>Pavyzdžio modelio susiejimo kūrimas

1.  Puslapyje **Konfigūracijos** pasirinkite **Dizaino įrankis**.

    > Atkreipkite dėmesį, kad pagrindinės konfigūracijos modelio susiejimai buvo automatiškai nukopijuoti į šią konfigūraciją.

2.  Pasirinkite **Susiejimo (bendrojo) kopija** susiejimą.
3.  Pasirinkite **Dizaino įrankis**.
4.  Skyriuje **Duomenų modelis** pasirinkite **Redaguoti**.
5.  Lauke **Formulė** įveskite **Pasirinktinė 1 bendroji funkcija**.
6.  Pasirinkite **Įrašyti**.
7.  Uždarykite puslapį.

    ![ER modelio susiejimo dizainerio puslapis, Bendrinio funkcionalumo 1 pasirinktinė formulė.](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  Pasirinkite **Įrašyti**.
9.  Uždarykite puslapį.
10. Pasirinkite **Susiejimo (bendrojo) 2 kopija** susiejimą.
11. Pasirinkite **Dizaino įrankis**.
12. Skyriuje **Duomenų modelis** pasirinkite **Redaguoti**.
13. Lauke **Formulė** įveskite **Pasirinktinė 2 bendroji funkcija**.
14. Pasirinkite **Įrašyti**.
15. Uždarykite puslapį.

    ![ER modelio susiejimo dizainerio puslapis, Bendrinio funkcionalumo 2 pasirinktinė formulė.](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. Pasirinkite **Įrašyti**.
17. Uždarykite puslapį.

    ![ER modelis duomenų šaltinio susiejimo puslapiui, skirtas (Bendram) kopijavimo susiejimui.](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. Uždarykite puslapį.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Modelio susiejimo konfigūracijos modifikuotos versijos užbaigimas

1.  Puslapio **Konfigūracijos** „FastTab“ **Versijos** pasirinkite **Keisti būseną**.

    > Pakeiskite sukurtos modelio susiejimo konfigūracijos būseną iš **Juodraštis** į **Baigta**, kad ją galėtų naudoti ER formatai.

2.  Pasirinkite **Baigti**.
3.  Pasirinkite **Gerai**.

Atkreipkite dėmesį, kad sukurta konfigūracija įrašoma kaip 1 baigta versija.

## <a name="appendix-3"></a><a name="appendix3"></a>3 priedas

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a>Pavyzdinio modelio susiejimo konfigūravimas tinkinimui pagal šalį / regioną

Kai kurių ER formatų duomenų paruošimui gali būti taikomi šaliai / regionui būdingi parametrai. Tokiu atveju galite valdyti atskirą ER modelio susiejimo konfigūraciją ir izoliuoti šios šalies / regiono reikalavimų, kuriuos reikia vykdyti iš bendrojo įgyvendinimo, įgyvendinimą. Šiame priede pateiktoje procedūroje kaip pavyzdys naudojamas **Formatas, skirtas sužinoti apie susiejimus** ER formatas ir Prancūzijai būdingi reikalavimai.

#### <a name="create-an-er-model-mapping-configuration"></a>ER modelio susiejimo konfigūracijos kūrimas

Visų pirmą, sukurkite naują ER modelio susiejimo konfigūraciją, kad įgyvendintumėte šaliai / regionui būdingus reikalavimus. Naudokite savo tinkavimo ER modelio susiejimo konfigūraciją kaip pagrindą.

1.  Puslapyje **Konfigūracijos** konfigūracijų medyje pasirinkite **Pasirinktinis susiejimas (bendrasis)**.
2.  Pasirinkite **Kurti konfigūraciją**.
3.  Išplečiamajame dialogo lango lauko grupėje **Naujas** pasirinkite **Išvesti iš pavadinimo: pasirinktinis susiejimas (bendrasis), „Litware, Inc“**.
4.  Lauke **Pavadinimas** įveskite **Susiejimas (FR)**.
5.  Pasirinkite **Kurti konfigūraciją**.

Atkreipkite dėmesį, kad šios ER konfigūracijos 1 juodraščio versija parengta redaguoti.

#### <a name="design-a-sample-model-mapping"></a>Pavyzdžio modelio susiejimo kūrimas

1.  Puslapyje **Konfigūracijos** pasirinkite **Dizaino įrankis**.

    > Atkreipkite dėmesį, kad pagrindinės konfigūracijos modelio susiejimai buvo automatiškai nukopijuoti į šią konfigūraciją.

2.  Pasirinkite **Susiejimo (bendrojo) kopijos kopija** susiejimą.
3.  Pavadinkite ją **Susiejimas (FR)**.
4.  Pasirinkite **Dizaino įrankis**.
5.  Skyriuje **Duomenų modelis** pasirinkite **Redaguoti**.
6.  Lauke **Formulė** įveskite **1 FR funkcija**.
7.  Pasirinkite **Įrašyti**.
8.  Uždarykite puslapį.

    ![ER modelio susiejimo dizainerio puslapis, FR funkcionalumo 1 formulė.](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  Pasirinkite **Įrašyti**.
10. Uždarykite puslapį.
11. Pasirinkite **2 susiejimo (bendrojo) kopijos kopija** susiejimą.
12. Pavadinkite ją **2 susiejimas (FR)**.
13. Pasirinkite **Dizaino įrankis**.
14. Skyriuje **Duomenų modelis** pasirinkite **Redaguoti**.
15. Lauke **Formulė** įveskite **2 FR funkcija**.
16. Pasirinkite **Įrašyti**.
17. Uždarykite puslapį.

    ![ER modelio susiejimo dizainerio puslapis, FR funkcionalumo 2 formulė.](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. Pasirinkite **Įrašyti**.
19. Uždarykite puslapį.

    ![Duomenų šaltinio susiejimo puslapio ER modelis.](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. Uždarykite puslapį.

#### <a name="specify-countryregion-context-restrictions-for-use"></a>Šalies / regiono konteksto naudojimo apribojimų nurodymas

1.  Puslapio **Konfigūracijos** „FastTab“ **ISO šalių / regionų kodai** pasirinkite **Naujas**.
2.  Lauke **ISO** pasirinkite **FR**.
3.  Pasirinkite **Įrašyti**.

Atkreipkite dėmesį, kad turite prisijungti prie konkrečios įmonės, esančios „Finance“, kad galėtumėte vykdyti ER formatą. Todėl ši įmonė gali būti laikoma šalimi, kuri valdo tiek ER formato vykdymą, tiek bazinio ER duomenų modelio tinkamo ER modelio susiejimo pasirinkimą. Pridėję **FR** šalies kodą, galite nurodyti, kad šis modelio pasirinkimas norint pasirinkti bazinio duomenų modelio ER formatą galimas tik tada, kai šį formato vykdymą valdo įmonė, kuriai būdingas Prancūzijos šalies / regiono kontekstas.

Galite pridėti kelis šalies/regiono kodus vienai ER modelio susiejimo konfigūracijos versijai. Tokiu būdu modelio susiejimai, esantys šio modelio susiejimo konfigūracijoje, gali būti naudojami ER formatui, kuris vykdomas valdant įmonėms, kurioms būdingas skirtingas šalies / regiono kontekstas.

Atkreipkite dėmes, kad šalies/regiono kodų sąrašas nurodytas kiekvienai ER modelio susiejimo konfigūracijos versijai ir gali skirtis priklausomai nuo versijos.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Modelio susiejimo konfigūracijos modifikuotos versijos užbaigimas

1.  Puslapio **Konfigūracijos** „FastTab“ **Versijos** pasirinkite **Keisti būseną**.

    > Pakeiskite sukurtos modelio susiejimo konfigūracijos būseną iš **Juodraštis** į **Baigta**, kad ją galėtų naudoti ER formatai.

2.  Pasirinkite **Baigti**.
3.  Pasirinkite **Gerai**.

Atkreipkite dėmesį, kad sukurta konfigūracija įrašoma kaip 1 baigta versija.

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)

[Atskirų ER konfigūracijų ER modelio susiejimo valdymas](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[Šalies / regiono konteksto taikymas](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a>Sukonfigūravau dvi bendrinamas ER modelio susiejimo konfigūracijas RCS ir pažymėjau vieną iš jų kaip numatytąją modelio susiejimo konfigūraciją. Sėkmingai įvykdžiau ER formatą, kuris buvo sukurtas tai pačiai bazinei ER duomenų modelio konfigūracijai, kad patikrinčiau modelio susiejimus. Tada importavau visą ER sprendimą (ER duomenų modelį, dvi ER modelio susiejimo konfigūracijas ir ER formato konfigūraciją) į „Finance“. Kodėl gaunu klaidos pranešimą, kai bandau vykdyti tokį patį ER formatą kaip „Finance“?
Numatytasis modelio susiejimo parametras priklauso nuo konkrečios aplinkos. Jis sukonfigūruotas RCS, bet neeksportuotas į “Finance“. Norėdami sėkmingai paleisti šį ER formatą, vieną iš ER modelio susiejimo konfigūracijų taip pat turite pažymėti kaip numatytąją modelio susiejimo konfigūraciją „Finance“.

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a>Sukonfigūravau vieną modelio susiejimą kaip bendrinamą modelio susiejimą ir užbaigiau jo juodraštinę versiją. Tada į tą patį duomenų modelį įtraukiau naują modelio susiejimo konfigūraciją ir sukonfigūravau kaip būdingą Prancūzijai. Kodėl yra pasirenkamas bendrinamas modelio susiejimas, kai vykdau ER formatą, nors šis formatas naudoja tinkamą šakninį apibrėžimą ir vykdymą kontroliuoja įmonė, kuriai būdingas Prancūzijos šalies / regiono kontekstas?
Įsitikinkite, kad bendrinamo modelio susiejimo konfigūracija nėra pažymėta kaip numatytoji modelio susiejimo konfigūracija. Kitu atveju, jos prioritetas bus aukštesnis pasirenkant susiejimą. Taip pat įsitikinkite, kad yra atsižvelgiama į Prancūzijai būdingo modelio susiejimo konfigūraciją, kai ER formato vykdymo metu pasirenkamas susiejimas. Er modelio konfigūraciją galima pasirinkti, jei patenkinama bent viena iš toliau nurodytų sąlygų.
- Bent viena ER modelio susijimo konfigūracijos versija turi būseną **Baigta** arba **Bendrinta**. Šiuo atveju, versija, kuri turi didžiausią versijos numerį, bus naudojama, kad būtų galima vykdyti ER formatą.
- Parinktis **Vykdyti juodraštį**, skirta ER modelio susiejimo konfigūracijai, yra įjungta. Šiuo atveju, versija, kuri turi būseną **Juodraštis**, bus naudojama, kad būtų galima vykdyti ER formatą.
> Parinktis **Vykdyti juodraštį** pasiekiama puslapyje **Konfigūracijos** kiekvienai ER modelio susiejimo konfigūracijai, kai įjungtas ER vartotojo parametras **Vykdyti parametrą**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
