---
title: Brūkšninių kodų vaizdams generuoti brūkšninio kodo duomenų šaltinių naudojimas
description: Šioje temoje paaiškinama, kaip naudoti brūkšninio kodo duomenų šaltinius brūkšninio kodo vaizdams generuoti.
author: NickSelin
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.13
ms.openlocfilehash: bf71caf2ff14fb815999e63d6b7ee91afccbdd1b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563684"
---
# <a name="use-barcode-data-sources-to-generate-bar-code-images"></a>Brūkšninių kodų vaizdams generuoti brūkšninio kodo duomenų šaltinių naudojimas

[!include[banner](../includes/banner.md)]

Galite naudoti [Elektroninės ataskaitos (angl. ER)](general-electronic-reporting.md)sistemą, kad sukurtumėte [ER formato komponentus](general-electronic-reporting.md#FormatComponentOutbound), kuriuos galite paleisti jums reikalingų elektroninių ir spausdintinų siunčiamų dokumentų generavimui. Norėdami sugeneruoti siunčiamą dokumentą „Microsoft Office” formatu, turite nurodyti ataskaitos maketą, naudodami „Microsoft Excel” dokumentą arba „Microsoft Word” dokumentą kaip ataskaitos šabloną. [ER operacijų kūrėjas](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) suteikia galimybę pridėti „Excel” arba „Word” dokumentą kaip šabloną ER formatu. Toliau nurodyti pavadinti elementai pridėtame šablone yra susieti su sukonfigūruoto formato komponentų elementais:

- Turinio valdikliai „Word”
- Pavadinti lapai, diapazonai, langeliai, figūros ir vaizdai „Excel”

Šie pavadinti elementai naudojami kaip duomenų, įvestų į sugeneruotą dokumentą, kai vykdomas ER formatas, vietos rezervavimo ženklai. ER formato elementai yra susieti su duomenų šaltiniais. Šie duomenų šaltiniai nurodo duomenis, kurie bus įtraukti į sugeneruotus dokumentus apdorojimo metu. Daugiau informacijos žr. [Vaizdų ir figūrų įterpimas generuojamuose dokumentuose naudojant ER](electronic-reporting-embed-images-shapes.md).

ER dabar palaiko **Brūkšninis kodas** duomenų šaltinio tipą. Todėl dabar galite generuoti vaizdą, nurodantį nurodyto teksto brūkšninį kodą. Konfigūruodami ER formatą, galite nurodyti **Brūkšninis kodas** tipo duomenų šaltinius brūkšninio kodo vaizdams generuoti. Tada galite pridėti šiuos vaizdus į sugeneruotus verslo dokumentus, pvz., užsakymus, sąskaitas faktūras, važtaraščius ir kvitus. Taip pat galite pridėti juos prie įvairių rūšių etikečių, pvz., produktų ir lentynų etikečių, pakavimo ir gabenimo etikečių.

Šie vietos rezervavimo ženklai gali būti naudojami ataskaitų šablonuose, norint įvesti brūkšninių kodų vaizdus:

- [Paveikslėlio](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word)„Word” turinio valdiklis
- [Paveikslėlio ](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344) objektas „Excel”

Naudodami **Brūkšninis kodas** duomenų šaltinį, galite generuoti brūkšninius kodus šiais formatais:

- Vienos dimensijos brūkšniniai kodai:

    - Codabar
    - Code 39
    - Code 93
    - Code 128
    - EAN-8
    - EAN-13
    - ITF-14
    - „Intelligent Mail”
    - MSI
    - Plessey
    - PDF417
    - UPC-A
    - UPC-E

- Dviejų dimensijų brūkšniniai kodai:

    - Aztec
    - Duomenų matrica
    - QR kodas

Konfigūruodami **Brūkšninis kodas** duomenų šaltinį, galite nurodyti konkrečius vaizdų generavimo parametrus, kurie naudojami vaizdui generuoti:

- **Plotis** – nurodykite brūkšninio kodo plotį pikseliais. Vertė **0** (nulis) nurodo, kad naudojamas numatytasis plotis. Reikšmė skirtingiems formatams gali skirtis.
- **Aukštis** – nurodykite brūkšninio kodo aukštį pikseliais. Vertė **0** (nulis) nurodo, kad naudojamas numatytasis aukštis. Reikšmė skirtingiems formatams gali skirtis.
- **Paraštė** – nurodykite brūkšninio kodo maržos dydį pikseliais. Paraštė yra kiekvienos brūkšninio kodo pusės sritis, kuri turi būti švari (rami zona). Vertė **0** (nulis) nurodo, kad naudojama numatytoji paraštė. Reikšmė skirtingiems formatams gali skirtis.
- **Išeigos turinys** – nustatykite reikšmę į **Taip**, kad sugeneruotumėte brūkšninio kodo vaizdą, kuriame yra užkoduota informacija, kaip tekstas. Numatytoji reikšmė yra **Ne**.
- **Kodavimas** – nurodykite simbolių, užkoduotų sugeneruotame brūkšninio kodo vaizde, tipą. Pagal numatytuosius nustatymus, naudojamas **UTF-8** kodavimas.

> [!IMPORTANT]
> Kai pridedate naują **Brūkšninis kodas** duomenų šaltinį, turite jį įdėti į kitą prekę (konteinerį) kaip įdėtąjį elementą.
>
> Kai susiejate **Brūkšninis kodas** duomenų šaltinį su langelio elementu formate, o langelio elementas atspindi „Word” turinio valdiklį arba „Excel” paveikslėlį, duomenų šaltinis pateikiamas kaip siejanti funkcija, turinti vieną **Eilutė** tipo parametrą. Turite naudoti šį parametrą, kad nurodytumėte tekstą, kuris turi būti paverstas brūkšninio kodo vaizdu ir perskaitytas, kai nuskaitomas sugeneruotas brūkšninis kodas.

Norėdami sužinoti daugiau apie šią funkciją, atlikite šioje temoje esančius pavyzdžius.

## <a name="example-generate-a-payment-check-that-contains-a-bar-code-that-encodes-the-payable-amount"></a>Pavyzdys: sugeneruokite mokėjimo patikrinimą, kuriame yra brūkšninis kodas, kuris koduoja mokėtiną sumą

Šis pavyzdys parodo, kaip vartotojas, atliekantis **Sistemos administratorius** arba **Elektroninės ataskaitos funkcinis konsultantas** pareigas, gali konfigūruoti ER formatą, kuriame yra šablonas, naudojamas generuoti siunčiamą dokumentą „Excel” formatu, kuriame yra brūkšninis kodas. Čia pateikiama susijusių veiksmų apžvalga.

1. [Užpildyti būtinuosius komponentus](#ExamplePrerequisites).
2. [Aktyvuoti konfigūracijos tiekėją](#ExampleProvider).
3. [Importuokite tiekėjo ER sprendimą](#ExampleImportSolution).
4. [Sugeneruoti mokėjimo čekį](#ExampleGenerateCheque).
5. [Peržiūrėti sugeneruotą mokėjimo čekį](#ExampleReviewGeneratedCheque).
6. [Modifikuoti pateikto ER sprendimo formatą](#ExampleModifyFormat).

    1. [Taikyti naują čekio šabloną](#ExampleModifyFormatApplyTemplate).
    2. [Pridėti naują brūkšninio kodo duomenų šaltinį](#ExampleModifyFormatAddDataSource).
    3. [Susiekite naują formato elementą](#ExampleModifyFormatBindFormatElement).
    4. [Padaryti modifikuotą versiją prieinamą bandomiesiems vykdymams](#ExampleModifyFormatMakeVersionAvailable).

        1. [Baigti modifikuoto formato versiją](#CompleteToRun).
        2. [Padaryti juodraštinę versiją prieinamą naudojimui](#MarkToRun).

7. [Sugeneruoti mokėjimo čekį](#ExampleGenerateCheque2).
8. [Konvertuoti sugeneruotą čekį į PDF](#ExampleConvertToPDF).

Šiame pavyzdyje naudosite pateiktą ER sprendimą, sukonfigūruotą generuoti mokėjimo čekius. Šis sprendimas generuoja mokėjimo čekius, kai mokėtina suma įrašoma kaip skaičius ir kaip tekstas. Modifikuosite ER sprendimą, kad čekyje būtų pateiktas brūkšninis kodas, kuriame mokėtina suma yra užkoduota ir gali būti nuskaityta brūkšninio kodo skaitytuvu.

Šiuos veiksmus galite užbaigti įmonėje **USMF** programoje „Microsoft Dynamics 365 Finance“.

### <a name="complete-the-prerequisites"></a><a name="ExamplePrerequisites"></a>Būtinųjų komponentų pildymas

Norėdami atlikti šį pavyzdį, turite turėti prieigą prie įmonės USMF programoje „Finance“ ir vieną iš tolesnių vaidmenų.

- Elektroninės ataskaitos funkcijų konsultantas
- Sistemos administratorius

Jei dar nebaigėte pavyzdžio, pateikiamo [Įdėti vaizdai ir formos jūsų sugeneruotuose dokumentuose naudojant ER](electronic-reporting-embed-images-shapes.md) temoje, atsisiųskite šiuos ER sprendimo pavyzdžio konfigūravimus.

| Turinio aprašas         | Failo vardas                   |
|-----------------------------|-----------------------------|
| ER duomenų modelio konfigūracija | cheques.xml šablonas       |
| ER formato konfigūracija     | Čekių spausdinimas formatas.xml |

Be to, atsisiųskite nurodytą „Excel” failą, kuriame yra modifikuotas pateikto ER sprendimo šablonas.

| Turinio aprašas | Failo vardas                 |
|---------------------|---------------------------|
| Ataskaitos šablonas     | Čekio šablonas Excel.xlsx |

### <a name="activate-a-configuration-provider"></a><a name="ExampleProvider"></a>Konfigūracijų teikėjo aktyvinimas

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos tiekėjai** dalyje įsitikinkite, kad [konfigūracijos tiekėjas](general-electronic-reporting.md#Provider), nurodytas kaip **Litware, Inc.** įmonės pavyzdys, ir kad jis pažymėtas kaip aktyvus. Jeigu jis nenurodytas ar nepažymėtas kaip aktyvus, atlikite veiksmus temoje [Konfigūracijų teikėjo kūrimas ir jo aktyvios būsenos pažymėjimas](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![Įmonės pavyzdžio nustatymas į aktyvią būseną Lokalizavimo konfigūracijų puslapyje](./media/er-barcode-data-source-active-provider.png)

### <a name="import-the-provided-er-solution"></a><a name="ExampleImportSolution"></a>Importuokite pateiktą ER sprendimą

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos** dalyje pasirinkite plytelę **Konfigūracijų ataskaitos**.
3. Puslapyje **Konfigūracijos**, jei **Čekių šablonas** konfigūracija negalima konfigūracijos medyje, atlikite šiuos veiksmus, kad importuokite ER duomenų modelio konfigūraciją:

    1. Veiksmų srityje pasirinkite **Pakeisti** \> **Įkelti iš XML failo**.
    2. Dialogo lange pasirinkite **Naršyti**, suraskite ir pasirinkite failą **Šablonas cheques.xml**, tada pasirinkite **Gerai**.

4. Jei konfigūracijos medyje **Čekių spausdinimo formatas** konfigūracija negalima, atlikite šiuos veiksmus, kad importuotumėte ER formato konfigūraciją:

    1. Veiksmų srityje pasirinkite **Pakeisti** \> **Įkelti iš XML failo**.
    2. Dialogo lange pasirinkite **Naršyti**, suraskite ir pasirinkite failą **Kvitų spausdinimo format.xml**, tada pasirinkite **Gerai**.

5. Konfigūracijos medyje išplėskite **Čekių šablonas**.
6. Peržiūrėkite importuotų ER konfigūracijų sąrašą konfigūracijos medyje.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque"></a>Mokėjimo čekio generavimas

1. Eikite į **Grynųjų ir banko valdymas** \> **Banko sąskaitos** \> **Banko sąskaitos**.
2. **Banko sąskaitos** puslapyje pasirinkite **USMF OPER** paskyrą.
3. Banko sąskaitos informacijos puslapyje, veiksmų srityje, **Nustatyti** skirtuke, **Maketas** grupėje, pasirinkite **Čekis**.
4. **Čekio maketas** puslapyje pasirinkite **Redaguoti**.
5. **Bendra** „FastTab” skirtuke nustatykite parinktį **Bendrasis elektroninis eksportavimo formatas** į **Taip**.
6. **Eksportuoti formato konfigūraciją** lauke pasirinkite **Čekių spausdinimo formatas** jūsų anksčiau importuotą ER formatą.
7. Veiksmų srityje pasirinkite **Spausdinimo bandymas**.
8. Dialogo lange nustatykite **Perduodamo čekio formato** pasirinktį į **Taip**, tada pasirinkite **Gerai**.

    ![Čekio maketas – spausdinimo bandymo dialogo langas](./media/er-barcode-data-source-check-layout.png)

### <a name="review-the-generated-payment-check"></a><a name="ExampleReviewGeneratedCheque"></a>Sugeneruoto mokėjimo čekio peržiūra

- Atidaryti sugeneruotą tikrinimą programoje „Excel”.
2. Peržiūrėti sugeneruotą čekį.

    ![Sugeneruotas mokėjimo čekis „Excel”](./media/er-barcode-data-source-cheque1.png)

### <a name="modify-the-format-of-the-provided-er-solution"></a><a name="ExampleModifyFormat"></a>Pateikto ER sprendimo formato modifikavimas

#### <a name="apply-a-new-check-template"></a><a name="ExampleModifyFormatApplyTemplate"></a>Naujo čekio šablono taikymas

Galite naudoti „Excel” darbalaukio programą atidaryti jūsų anksčiau importuotą **Čekio šablonas Excel.xlsx** failą. Atkreipkite dėmesį, kad šis šablonas skiriasi nuo šablono, kurį naudojote sugeneruoti čekį pateiktame ER sprendime. Be to, jame yra **SumosBrūkšninisKodas** elementas, skirtas brūkšninio kodo vaizdui.

![SumosBrūkšninisKodas elementas „Excel” šablone](./media/er-barcode-data-source-cheque2.png)

Dabar turite modifikuoti ER sprendimą ir tada [iš naujo pritaikyti](modify-electronic-reporting-format-reapply-excel-template.md) modifikuotą šabloną.

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos** dalyje pasirinkite plytelę **Konfigūracijų ataskaitos**.
3. **Konfigūracijos** puslapyje, esančiame konfigūracijos medyje, išplėskite **Čekių modelis** ir pasirinkite **Čekių spausdinimo formatas**.
4. Veiksmų srityje pasirinkite **Dizaino įrankis**.
5. „ER Operations” kūrimo įrankyje pasirinkite **Susiejimas** skirtuką dešinėje puslapio pusėje, tada formato medžio srityje kairėje pasirinkite **Plėsti/sutraukti**.
6. Atkreipkite dėmesį, kad visi langelio formato elementai yra susieti su atitinkamais duomenų šaltiniais.

    ![Langelio formato elementų susiejimas su duomenų šaltiniais „ER Operations” kūrimo įrankyje](./media/er-barcode-data-source-cells-bound.png)

7. Pasirinkite **Formatuoti** skirtuką dešinėje puslapio pusėje.
8. Veiksmų srityje pasirinkite daugtaškį ( **...**) ir pasirinkite **Importuoti**.
9. **Importavimas** grupėje pasirinkite **Naujinti iš „Excel”** ir pasirinkite **Naujinti šabloną**.
10. Dialogo lange pereikite prie **Čekio šablono Excel.xlsx** failo, kuris įrašytas jūsų kompiuteryje, pasirinkite jį ir tada pasirinkite **Gerai**, kad patvirtintumėte taikyti pasirinktą šabloną.
11. Pasirinkite **Susiejimas** skirtuką dešinėje puslapio pusėje, tada formato medžio srityje kairėje pasirinkite **Plėsti/sutraukti**.
12. Atkreipkite dėmesį, kad **SumosBrūkšninisKodas** langelio elementas buvo pridėtas prie formato. Šis elementas yra susietas su **SumosBrūkšninisKodas** pridėtu į modifikuotą „Excel” šabloną elementu kaip vietos rezervavimo ženklas brūkšninio kodo vaizdui.

    ![SumosBrūkšninisKodas langelio elementas, pridėtas prie formato, esančio „ER Operations” kūrimo įrankyje](./media/er-barcode-data-source-cell-added.png)

#### <a name="add-a-new-barcode-data-source"></a><a name="ExampleModifyFormatAddDataSource"></a>Naujo brūkšninio kodo duomenų šaltinio pridėjimas

Tada turite pridėti naują **Brūkšninis kodas** tipo duomenų šaltinis.

1. „ER Operations” kūrimo įrankyje **Susiejimas** skirtuke, dešinėje puslapio pusėje, pasirinkite **spausdinti** duomenų šaltinį.
2. Pasirinkite **Pridėto**, tada **Funkcijos** grupėje pasirinkite **Brūkšninis kodas** duomenų šaltinio tipą.

    ![Brūkšninio kodo duomenų šaltinio tipo pasirinkimas](./media/er-barcode-data-source-add.png)

3. Dialogo lango lauke **Pavadinimas** įveskite **Brūkšninis kodas**.
4. **Brūkšninis formatas**, pasirinkite **Kodas 128**.
5. **Plotis** lauke įveskite **500**.
6. Pasirinkite **Gerai**.

    ![Duomenų bazės ypatybių dialogo langas](./media/er-barcode-data-source-add2.png)

#### <a name="bind-a-new-format-element"></a><a name="ExampleModifyFormatBindFormatElement"></a>Naujo formato elemento susiejimas

Tada turite susieti naujo formato elementą su ką tik pridėtu duomenų šaltiniu.

1. „ER Operations” kūrimo įrankyje **Susiejimas** skirtuke dešinėje puslapio pusėje, pasirinkite **spausdinti\\brūkšninį kodą** duomenų šaltinį.
2. Kairėje pusėje esančio medžio srityje pasirinkite **SumosBrūkšninisKodas** langelio elementą ir pasirinkite **Susieti**.
3. Veiksmų srityje pasirinkite **Rodyti išsamią informaciją**.
4. Atkreipkite dėmesį, kad, kadangi **Brūkšninis kodas** duomenų šaltinis atvaizduojamas kaip susietas su funkcija, kurioje yra vienas parametras, susieto formato elemento pavadinimas automatiškai paimtas kaip šio parametro argumentas.

    ![Išsami informacija apie brūkšninio kodo duomenų šaltinį „ER Operations” kūrimo įrankyje ](./media/er-barcode-data-source-bind1.png)

5. Norėdami koreguoti susiejimą, pasirinkite **Redaguoti formulę**.

    Nenorite, kad būtų grąžinamas langelio elemento pavadinimas. Todėl turite sukonfigūruoti išraišką, grąžinančią tekstą, kuriame nurodyta dabartinio čekio mokėtina suma. Todėl, kad pirminis **ČekioEilutės** diapazonas yra susietas su **čekių.šablonas** duomenų šaltiniu, dabartinio čekio mokėtina suma rodoma **čekių.šablonų.atributų.suma** lauke **Tikras** duomenų tipo.

6. Lauke **Formulė** įveskite **spausdinti.brūkšniniskodas(NUMERIOFORMATAS(@.atributai.suma,„F2”))**.
7. Pasirinkite **Įrašyti** ir uždarykite [ER Formulės kūrimo įrankį](general-electronic-reporting-formula-designer.md).
8. Atkreipkite dėmesį, kad susiejimas buvo pakoreguotas.

    ![Pakoreguotas susiejimas su „ER Operations” kūrimo įrankyje](./media/er-barcode-data-source-bind2.png)

9. Pasirinkite **Įrašyti** ir uždarykite „ER Operations” kūrimo įrankį.

#### <a name="make-the-modified-version-available-for-test-runs"></a><a name="ExampleModifyFormatMakeVersionAvailable"></a>Modifikuotos versijos prieinamumas bandomajam vykdymui

Pagal numatytuosius nustatymus vienintelės versijos, turinčios **Baigta** ir **Bendrinta** būsenas, yra naudojamos, kai paleidžiate ER formatą.

Jeigu baigiate savo keitimus, galite baigti savo darbą naudodami dabartinę juodraštinę versiją ir padaryti savo keitimus prieinamus naudoti. Norėdami gauti daugiau instrukcijų, žr. toliau einantį [Modifikuoto formato versijos pabaigimas](#CompleteToRun)skyrių.

Jei norite tęsti darbą su esama juodraščio versija, bet turite jį naudoti norėdami sugeneruoti čekius, turite aiškiai nurodyti, kad norite naudoti vykdymo formato juodraštinę versiją. Norėdami gauti daugiau instrukcijų, žr., [Juodraščio versijos naudojimui prieinamumas](#MarkToRun)skyrių.

##### <a name="complete-the-modified-format-version"></a><a name="CompleteToRun"></a>Modifikuoto formato versijos užbaigimas

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos** dalyje pasirinkite plytelę **Konfigūracijų ataskaitos**.
3. **Konfigūracijos** puslapyje, esančiame konfigūracijos medyje, išplėskite **Čekių modelis** ir pasirinkite **Čekių spausdinimo formatas**.
4. **Versijos** „FastTab“ pasirinkite įrašą, kurio būsena yra **Juodraštis**.
5. Pasirinkite **Pakeisti būseną** ir pasirinkite **Baigti**.
6. Dialogo lange pasirinkite **Gerai**.

Dabartinės versijos būsena pakeista iš **Juodraštis** į **Baigta** ir sukuriama nauja versija, kurios būsena **Juodraštis**. Galite naudoti šią naują juodraštinę versiją, kad pritaikytumėte papildomus keitimus.

##### <a name="make-the-draft-version-available-for-use"></a><a name="MarkToRun"></a>Juodraštinės versijos prieinamumas naudojimui

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos** dalyje pasirinkite plytelę **Konfigūracijų ataskaitos**.
3. Puslapyje **Konfigūracijos**, veiksmų srityje, **Konfigūracijos** skirtyje, grupėje **Išankstiniai parametrai** pasirinkite **Vartotojo parametrai**.
4. Dialogo lange nustatykite **Leisti parametrą** pasirinktis į **Taip**, tada pasirinkite **Gerai**.
5. Konfigūracijų medyje išplėskite **Čekių šablonas** ir pasirinkite **Čekių spausdinimo formatas**.
6. Nustatykite **Leist juodraštį** parinktį į **Taip**.
7. Pasirinkite **Įrašyti**.

Pasirinkto formato juodraštinė versija pažymėta kaip galima naudoti, kai paleidžiamas pasirinktas formatas.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque2"></a>Mokėjimo čekio generavimas

1. Eikite į **Grynųjų ir banko valdymas** \> **Banko sąskaitos** \> **Banko sąskaitos**.
2. **Banko sąskaitos** puslapyje pasirinkite **USMF OPER** paskyrą.
3. Banko sąskaitos informacijos puslapyje, veiksmų srityje, **Nustatyti** skirtuke, **Maketas** grupėje, pasirinkite **Čekis**.
4. Puslapyje **Čekio maketas**, esančiame Veiksmų srityje, pasirinkite **Spausdinimo bandymas**.
5. Dialogo lange nustatykite **Perduodamas čekio formatas** parinktį į **Taip**.
6. Pasirinkite **Gerai**.
7. Peržiūrėti sugeneruotą čekį. Atkreipkite dėmesį, kad brūkšninis kodas buvo sugeneruotas užkoduoti čekio mokėtiną sumą.

    ![Sugeneruotas mokėjimo čekis su brūkšninio kodu „Excel” programoje](./media/er-barcode-data-source-cheque3.png)

> [!IMPORTANT]
> Parodoma išimtis, jei **Brūkšninis kodas** duomenų šaltinio argumentas neatitinka atitinkamų reikalavimų, būdingų brūkšninio kodo formatui. Pavyzdžiui, kai **Brūkšninis kodas** duomenų šaltinis yra iškviečiamas sugeneruoti [EAN-8 ](https://wikipedia.org/wiki/EAN-8) pateikto teksto brūkšninį kodą, parodoma išimtis, jei tekstas viršija septynis simbolius.

### <a name="convert-the-generated-check-to-a-pdf"></a><a name="ExampleConvertToPDF"></a>Generuoto čekio konvertavimas į PDF

Kaip aprašyta [Spausdintinų FTI formų generavimas](er-generate-printable-fti-forms.md#finland) temoje, galite naudoti specialų šriftą brūkšniniams kodams sukurti sugeneruotame dokumente. Šiuo atveju papildomi sugeneruoto dokumento pakeitimai gali priklausyti nuo to šrifto prieinamumo pakeitimo aplinkoje. Pavyzdžiui, jei bandote konvertuoti dokumentą į PDF formatą arba peržiūrėti jį aplinkoje, kurioje trūksta šrifto, brūkšniniai kodai nebus atvaizduoti tinkamai.

Tačiau, kai naudojate **Brūkšninis kodas** duomenų šaltinį brūkšniniams kodams kurti, šių brūkšninių kodų atvaizdavimas nepriklauso nuo jokio šrifto. Todėl galite lengvai konvertuoti dokumentus, kuriuose yra brūkšniniai kodai, į PDF formatą. Toliau pateiktame paveikslėlyje rodoma sugeneruoto mokėjimo čekio, [konvertuoto](electronic-reporting-destinations.md#OutputConversionToPDF) į PDF, peržiūra, pagrįsta sukonfigūruoto ER[paskirties vietos](electronic-reporting-destinations.md) nustatymu.

![Mokėjimo čekio PDF peržiūra](./media/er-barcode-data-source-cheque4.png)

## <a name="limitations"></a>Apribojimai

> [!NOTE]
> Kai kurie sugeneruotų brūkšninių kodų tipai turi fiksuotas proporcijas. Toks veikimas yra reikšmingas, jei įjungėte **Įjungti EPPlus biblioteką Elektroninėje ataskaitų sistemoje** funkciją, kad galėtumėte dirbti su „Excel” dokumentais ER. Tokiu atveju vaizdas įvedamas į vietos rezervavimo ženklą, turintį fiksuotas proporcijas. Todėl, kai vietos rezervavimo ženklo dimensijos atitinka įvesto vaizdo koeficientą, tikro paveikslėlio dydis sugeneruotame dokumente gali būti keičiamas, kad būtų išlaikytos reikiamos proporcijos. Norėdami išvengti paveikslėlio dydžio keitimo, naudokite numatytų proporcijų vietos rezervavimo ženklą.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)
- [Elektroninių ataskaitų paskirties vietos](electronic-reporting-destinations.md)
- [Elektroninių ataskaitų formulių kalba](er-formula-language.md)
- [NUMERIOFORMATO funkcija](er-functions-text-numberformat.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]