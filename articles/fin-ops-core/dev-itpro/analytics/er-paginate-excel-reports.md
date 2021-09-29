---
title: ER formato kūrimas sugeneruotų „Excel” dokumentų išdėstymui
description: Šioje temoje paaiškinama, kaip kurti Elektroninių ataskaitų (ER) formatą, kuris sunumeruoja sugeneruoto dokumento puslapius „Microsoft Excel”.
author: NickSelin
ms.date: 09/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: Version 10.0.22
ms.openlocfilehash: ce29225c4bce24adc2abefc3d3d6f20774852af4
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488344"
---
# <a name="design-an-er-format-to-paginate-generated-documents-in-excel"></a>ER formato kūrimas sugeneruotų „Excel” dokumentų išdėstymui

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip Sistemos administratoriaus arba Elektroninių ataskaitų funkcinio konsultanto vaidmenį turintis vartotojas gali konfigūruoti [Elektroninės ataskaitos (ER)](general-electronic-reporting.md) formatą, kad sugeneruoti siunčiamus dokumentus „Microsoft Excel” ir tvarkyti puslapių numeraciją.

Šiame pavyzdyje jūs modifikuosite „Microsoft” pateiktą ER formatą, kuris naudojamas valdiklio ataskaitai spausdinti, kai „Intrastat” deklaracija yra [generuojama](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md). Ši ataskaita leidžia jums stebėti paskelbtas „Intrastat” operacijas. Jūsų pakeitimai leis jums valdyti sugeneruotų kontrolės ataskaitų puslapių numeraciją.

Šios temos procedūros gali būti atliktos naudojant **„DEMF”** įmonę. Kodavimas nebūtinas. Prieš pradėdami, atsisiųskite ir įrašykite šiuos failus.

| Aprašas       | Failo vardas |
|-------------------|-----------| 
| Ataskaitos šablonas 1 | [„ERIntrastatReportDemo1.xlsx”](https://download.microsoft.com/download/7/2/a/72ae292a-8bb2-4b9d-8397-9764218f6fa8/ERIntrastatReportDemo1%20.xlsx) |
| Ataskaitos šablonas 2 | [„ERIntrastatReportDemo2.xlsx”](https://download.microsoft.com/download/7/d/1/7d15858d-6260-4afa-9dda-d8b955e59b1a/ERIntrastatReportDemo2.xlsx) |

## <a name="configure-the-er-framework"></a>ER sistemos konfigūracija

Atlikite veiksmus, aprašytus skyriuje [Konfigūruoti ER sistemą](er-quick-start2-customize-report.md#ConfigureFramework), kad nustatytumėte minimalų ER parametrų rinkinį. Prieš pradėdami naudoti ER sistemą standartinio ER formato versijai kurti, turite užbaigti šį nustatymą.

## <a name="import-the-standard-er-format-configuration"></a>Standartinio ER formato konfigūracijos importavimas

Atlikite veiksmus, aprašytus skyriuje [Importuoti standartinio ER formato konfigūracijas](er-quick-start2-customize-report.md#ImportERSolution1), kad įtrauktumėte standartines ER konfigūracijas į dabartinį „Dynamics 365 Finance” egzempliorių. Importuoti **1.9 leidimo** **„Intrastat” ataskaitos** formato konfigūracijos versiją. Pagrindinė 1 **„Intrastat” modelio** konfigūracijos versija yra automatiškai importuojama iš saugyklos.

## <a name="customize-the-standard-er-format"></a>Pritaikykite standartinį ER formatą

### <a name="create-the-custom-er-format"></a>Pasirinktinio ER formato kūrimas

Šiame scenarijuje jūs atstovaujate „Litware Inc.”, kuris šiuo metu pasirinktas kaip aktyvus ER konfigūracijos tiekėjas. Turite sukurti naują ER formato konfigūraciją naudodami **„Intrastat” ataskaitos** konfigūraciją kaip pagrindą.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** konfigūracijų medžio kairėje srityje išskleiskite **„Intrastat” modelis**, o tada pasirinkite **„Intrastat” ataskaita**. „Litware, Inc.” naudos ER formato konfigūracijos 1.9 versiją kaip pasirinktinės versijos pagrindą.
3. Pasirinkite **Kurti konfigūraciją**, kad atidarytumėte išplečiamąjį dialogo langą. Galite naudoti dialogo langą, kad sukurtumėte naują pasirinktinio mokėjimo formato konfigūraciją.
4. **Nauja** lauko grupėje pasirinkite **Išvesti iš Pavadinimo: „Intrastat” ataskaita, „Microsoft”**.
5. Lauke **Pavadinimas** įveskite **„Intrastat“ ataskaita „Litware”**.
6. Pasirinkite **Kurti konfigūraciją** naujo formato kūrimui.

Sukuriama **„Intrastat” ataskaitos „Litware”** ER formato konfigūracijos 1.9.1 versija. Ši versija turi [būseną](general-electronic-reporting.md#component-versioning) **Juodraštis** ir ji gali būti redaguojama. Jūsų pritaikyto ER formato dabartinis turinys atitinka „Microsoft” pateikto formato turinį.

### <a name="make-the-custom-format-runnable"></a>Padarykite tinkintą formatą kaip vykdytiną

Dabar, kai sukurta pirmoji jūsų pritaikyto formato versija, kurios būsena **Juodraštis**, formatą galite paleisti testavimui. Norėdami paleisti ataskaitą, apdorokite tiekėjo mokėjimą naudodami mokėjimo būdą, nurodantį jūsų pritaikytą ER formatą. Pagal numatytuosius nustatymus jums iškvietus ER formatą programoje tik būseną` **Baigta** ar **Bendrinta** turinčios versijos [bus svarstomos](general-electronic-reporting.md#component-versioning). Toks veikimas užtikrina, kad nebaigto dizaino ER formatai nebūtų naudojami. Tačiau, atliekant bandomuosius vykdymus, galite priversti programą naudoti ER formato **Juodraštis** būsenos versiją. Tokiu būdu galite koreguoti dabartinio formato versiją, jei reikia atlikti pakeitimus. Daugiau informacijos žr. [Taikomumas](electronic-reporting-destinations.md#applicability).

Norėdami naudoti ER formato juodraščio versiją, turite aiškiai pažymėti ER formatą.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
3. **Vartotojo parametrai** dialogo lange nustatykite **Leisti parametrus** parinktį į **Taip** ir pasirinkite **Gerai**.
4. Pasirinkite **Redaguoti**, kad pagal poreikį galėtumėte redaguoti esamą puslapį.
5. Konfigūracijos medžio kairiojoje srityje pasirinkite **„Intastat” ataskaita „Litware”**.
6. Nustatykite **Vykdyti juodraštį** parinktį į **Taip**, o tada pasirinkite **Įrašyti**.

    ![Paleiskite juodraštinę pasirinktį Konfigūracijų puslapyje.](./media/er-paginate-excel-reports-derived-format-configuration.png)

## <a name="set-up-foreign-trade-parameters-to-use-the-custom-er-format"></a>Užsienio prekybos parametrų nustatymas pasirinktinio ER formato naudojimui

Norėdami sukonfigūruoti užsienio prekybos parametrus, kad galėtumėte naudoti pasirinktinį formatą, atlikite šiuos veiksmus.

1. Pasirinkite **Mokesčiai** \> **Nustatymas** \> **Užsienio prekyba** \> **Užsienio prekybos parametrai**.
2. Puslapio **Užsienio prekybos parametrai** „FastTab“ **Elektroninės ataskaitos** lauke **Failo formato susiejimas** pasirinkite **„Intrastat” ataskaita „Litware”**.
3. **Ataskaitos formatų susiejimas** lauke pasirinkite **„Intrastat” ataskaita „Litware”**.
4. Pasirinkite **Įrašyti**.

## <a name="configure-the-custom-format-to-use-the-downloaded-report-template"></a>Konfigūruokite pasirinktinį formatą, kad būtų galima naudoti atsisiųstą ataskaitos šabloną

### <a name="review-the-first-downloaded-excel-template"></a>Peržiūrėkite pirmą atsisiųstą „Excel” šabloną

1. „Excel” darbalaukio programoje atidarykite **„ERIntrastatReportDemo1.xlsx”** šablono failą, kurį atsisiuntėte anksčiau.
2. Patikrinkite, ar šablone yra įvardyti diapazonai, skirti kurti ataskaitos antraštę, informaciją ir poraštės skyrius sugeneruotuose dokumentuose.

    ![„Excel” 1 šablono maketas darbalaukio programoje.](./media/er-paginate-excel-reports-template1.gif)

### <a name="replace-the-current-excel-template-in-the-custom-er-format"></a><a id="replace-template"></a>Pakeisti dabartinį Excel šabloną pasirinktiniu ER formatu

Turite įtraukti naują „Excel” šabloną į pasirinktinį ER formatą.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** kairiosios srities konfigūracijos medyje išplėskite **„Intrastat” modelis** \> **„Intrastat” ataskaita**, o tada pasirinkite **„Intrastat” ataskaitos „Litware”** konfigūraciją.
3. Pasirinkite **Dizaino įrankis**.
4. Puslapio **Formato kūrimo įrankis** veiksmų srityje pasirinkite **Rodyti išsamią informaciją**.
5. Įsitikinkite, kad pasirinktas **„Intrastat”: „Excel”** šakninis formato elementas, o tada veiksmų srities skirtuko **Importuoti** grupėje **Importuoti** pasirinkite **Naujinti iš „Excel”**.
6. Dialogo lange **Naujinti iš „Excel”** pasirinkite **Naujinti šabloną**.
7. Dialogo lange **Atidaryti** naršykite ir pasirinkite anksčiau atsisiųstą **„ERIntrastatReportDemo1.xlsx”** failą, o tada pasirinkite **Atidaryti**.
8. Pasirinkite **Gerai**.
9. Pasirinkite **Įrašyti**.

![Formato struktūra ER formatų rengyklėje pridėjus naują „Excel” šabloną.](./media/er-paginate-excel-reports-format1.png)

## <a name="change-the-data-binding-to-show-the-item-description-on-a-generated-report"></a>Duomenų susiejimo keitimas, kad sugeneruotoje ataskaitoje būtų rodomas prekės aprašymas

1. Puslapyje **Formato kūrimo įrankis** pasirinkite skirtuką **Susiejimas**.
2. Išplėskite **„Intrastat”** \> **Ataskaitos eilutės** ir pasirinkite **Prekės kodo** komponentą.
3. Pasirinkite **Redaguoti formulę**.
4. Pakeiskite susiejimo formulę iš `@.CommodityCode` į `CONCATENATE(@.CommodityCode, " ", @.ProductName)`.
5. Pasirinkite **Įrašyti**.

![Sukonfigūruotas susiejimas, kad būtų rodomas prekės aprašymas ER formaų rengyklėje.](./media/er-paginate-excel-reports-format1a.png)

## <a name="generate-an-intrastat-declaration-control-report"></a><a id="generate-intrastat-control-report"></a>Intrastat deklaracijos kontrolės ataskaitos generavimas

Visų pirma įsitikinkite, kad turite „Intrastat” operacijas atskaitoms **„Intrastat”** puslapyje.

![Operacijos „Intrastat” puslapyje.](./media/er-paginate-excel-reports-transactions1.gif)

Tada naudokite pasirinktinį ER formatą „Intrastat” deklaracijos valdiklio ataskaitai generuoti.

1. Eikite į **Mokesčiai** \> **Deklaracijos** \> **Užsienio prekyba** \> **„Intrastat”**.
2. Puslapyje **„Intrastat”**, esančiame Veiksmų srityje, pasirinkite **Išvestis** \> **Ataskaita**.
3. Dialogo lange **„Intrastat” ataskaita** atlikite šiuos veiksmus, jei norite vykdyti ataskaitą:

    1. Nustatykite laukus **Pradžios data** ir **Pabaigos data**, kad į ataskaitą būtų įtrauktos konkrečios „Intrastat” operacijos.
    2. Parinktį **Generuoti failą** nustatykite į **Ne**.
    3. Parinktį **Generuoti ataskaitą** nustatykite kaip **Taip**.
    4. Pasirinkite **Gerai**.

4. Atsisiųskite ir įrašykite sugeneruotą dokumentą.
5. Atidarykite dokumentą „Excel“ formatu ir peržiūrėkite jį.

    ![Sugeneruotas „Excel” dokumentas darbalaukio programoje.](./media/er-paginate-excel-reports-document1.png)

## <a name="configure-the-custom-format-to-paginate-generated-documents"></a>Konfigūruoti pasirinktinį formatą sugeneruotų dokumentų puslapių numeracijai

### <a name="review-the-second-downloaded-excel-template"></a>Peržiūrėkite antrą atsisiųstą „Excel” šabloną

1. „Excel” atidarykite **„ERIntrastatReportDemo2.xlsx”** šablono failą, kurį atsisiuntėte anksčiau.
2. Palyginkite šį šabloną su **„ERIntrastatReportDemo1.xlsx”** šablonu ir patikrinkite, ar jame yra keli nauji „Excel” pavadinimai, kad sukurtumėte ir užpildytumėte konkrečius puslapio skyrius sugeneruotuose dokumentuose:

    - Diapazonas **„ReportPageHeader”** yra įtrauktas puslapių antraščių kūrimui.
    - Diapazonas **„ReportPageFooter”** yra įtrauktas puslapių poraščių kūrimui.
    - Langelis **„ReportPageFooter”\_„PageLines”** yra sukonfigūruotas rodyti puslapio operacijų skaičių.
    - Langelis **„ReportPageFooter”\_„PageAmount”** yra sukonfigūruotas rodyti puslapio operacijų bendrą sumą.
    - Langelis **„ReportPageFooter”\_„PageWeight”** yra sukonfigūruotas rodyti puslapio operacijų bendrą svorį.
    - Langelis **„ReportPageFooter”\_„RunningCounterLines”** yra sukonfigūruotas rodyti operacijų veikiantį skaitiklį nuo ataskaitos pradžios iki dabartinio puslapio.
    - Langelis **„ReportPageFooter”\_„RunningTotalAmount”** yra sukonfigūruotas rodyti visų operacijų bendrą sumą nuo ataskaitos pradžios iki dabartinio puslapio.
    - Langelis **„ReportPageFooter”\_„RunningTotalWeight”** yra sukonfigūruotas rodyti visų operacijų bendrą svorį nuo ataskaitos pradžios iki dabartinio puslapio.

    ![„Excel” 2 šablono maketas darbalaukio programoje.](./media/er-paginate-excel-reports-template2a.gif)

    Šio šablono **„CommodityCode”** langelis yra sukonfigūruotas taip, kad langelio teksto eilutės būtų keliamos. Kadangi operacijos informacijos eilutė yra sukonfigūruota taip, kad ji automatiškai atitiktų eilutės aukštį, visos eilutės aukštis turi automatiškai pasikeisti, kai į naują eilutę keliamas **„CommodityCode”** langelio tekstas.

    ![„CommodityCode” langelis yra sukonfigūruotas taip, kad langelio teksto eilutės būtų keliamos.](./media/er-paginate-excel-reports-template2b.gif)

### <a name="repeat-the-replacement-of-the-current-excel-template-in-the-custom-er-format"></a>Pakartokite dabartinio „Excel” šablono pasirinktiniu ER formatu pakeitimą

1. Atlikite veiksmus, aprašytus šios temos [Pakeisti dabartinį „Excel” šabloną dabartiniu ER formatu](#replace-template) skyriuje. Tačiau 7 veiksme pasirinkite **„ERIntrastatReportDemo2.xlsx”** failą.
2. Puslapyje **Formato kūrimo įrankis** išplėskite **„Intrastat”**.
3. Pavadinkite [Diapazono](er-fillable-excel.md#range-component) formato komponentus, kurie buvo įtraukti į redaguotiną ER formatą, kad būtų sinchronizuota struktūra su pritaikyto „Excel” šablono struktūra:

    1. Pasirinkite **Diapazono** komponentą, susietą su „Excel” pavadinimu **„ReportPageHeader”**.
    2. Skirtuko **Formatas** lauke **Pavadinimas** įveskite **Ataskaitos puslapio antraštė**.
    3. Pasirinkite **Diapazono** komponentą, susietą su „Excel” pavadinimu **„ReportPageFooter”**.
    4. Skirtuko **Formatas** lauke **Pavadinimas** įveskite **Ataskaitos puslapio poraštė**.

4. Pasirinkite **Įrašyti**.

![Formato struktūra ER formatų rengyklėje pakeitus „Excel” šabloną.](./media/er-paginate-excel-reports-format2.png)

### <a name="change-the-format-structure-to-implement-document-pagination"></a>Formato struktūros keitimas, kad būtų galima įdiegti dokumento puslapių numeraciją

1. Puslapyje **Formatų rengyklė**, formatų medžių kairinėje srityje pasirinkite **„Intrastat”** šakninį komponentą.
2. Pasirinkite **Įtraukti**.
3. Dialogo lango **Įtraukti** pasirinkite [Puslapio](er-fillable-excel.md#page-component) komponentą **„Excel”** komponentų grupėje.
4. Dialogo lango **Komponento ypatybės** lauke **Pavadinimas** įveskite **Ataskaitos puslapis**. Tada pasirinkite **Gerai**.
5. Norėdami naudoti **Ataskaitos puslapio antraštės** komponentą kaip kiekvieno sugeneruoto puslapio antraštę, atlikite šiuos veiksmus:

    1. Pasirinkite **Ataskaitos puslapio antraštės** komponentą, o tada pasirinkite **Iškirpti**.
    2. Pasirinkite **Ataskaitos puslapio** komponentą, o tada pasirinkite **Įklijuoti**.
    3. Išplėskite **Ataskaitos puslapį**.
    4. Jei norite, kad **Puslapio** komponentas [atsižvelgtų](er-fillable-excel.md#page-component-structure) į šio diapazono puslapio antraštę, pasirinkite **Ataskaitos puslapio antraštė**, o tada **Formato** skirtuko lauke **Replikavimo kryptis** pasirinkite **Jokio replikavimo**.

6. Norėdami sunumeruoti sugeneruoto dokumento puslapius taip, kad būtų atsižvelgiama į ataskaitos eilučių turinį, atlikite šiuos veiksmus:

    1. Pasirinkite **Ataskaitos eilučių** komponentą, o tada pasirinkite **Iškirpti**.
    2. Pasirinkite **Ataskaitos puslapio** komponentą, o tada pasirinkite **Įklijuoti**.

7. Norėdami įtraukti ataskaitos poraštę po ataskaitos eilutėmis, bet prieš galutinę puslapio poraštę, atlikite šiuos veiksmus:

    1. Pasirinkite **Ataskaitos poraštės** komponentą, o tada pasirinkite **Iškirpti**.
    2. Pasirinkite **Ataskaitos puslapio** komponentą, o tada pasirinkite **Įklijuoti**.

8. Norėdami naudoti **Ataskaitos puslapio poraštės** komponentą kaip kiekvieno sugeneruoto puslapio poraštę, atlikite šiuos veiksmus:

    1. Pasirinkite **Ataskaitos puslapio poraštės** komponentą, o tada pasirinkite **Iškirpti**.
    2. Pasirinkite **Ataskaitos puslapio** komponentą, o tada pasirinkite **Įklijuoti**.
    3. Jei norite, kad **Puslapio** komponentas [atsižvelgtų](er-fillable-excel.md#page-component-structure) į šio diapazono puslapio poraštę, pasirinkite **Ataskaitos puslapio poraštė**, o tada **Formato** skirtuko lauke **Replikavimo kryptis** pasirinkite **Jokio replikavimo**.

![Formato struktūra ER formatų rengyklėje įvykdžius dokumentų puslapių numeraciją.](./media/er-paginate-excel-reports-format3.png)

### <a name="add-data-sources-to-calculate-page-footer-totals"></a>Duomenų šaltinių įtraukimas puslapio poraštės bendros sumos apskaičiavimui

Turite sukonfigūruoti naujus duomenų šaltinius, kad būtų galima apskaičiuoti puslapio sumą, vykdomą skaitiklį ir vykdomas bendras reikšmes, taip pat rodyti juos puslapio poraštės dalyje. Šiam tikslui rekomenduojame naudoti [Duomenų rinkinio](er-data-collection-data-sources.md) duomenų šaltinius.

1. Puslapyje **Formato kūrimo įrankis** pasirinkite skirtuką **Susiejimas**.
2. Dar kartą pasirinkite **Įtraukti šaknį** ir atlikite tolesnius veiksmus:

    1. Dialogo lango **Įtraukti duomenų šaltinį** skyriuje **Bendra** įveskite **Tuščias konteineris**.
    2. Dialogo lango **'Tuščio konteinerio šaltinio ypatybės** lauke **Pavadinimas** įveskite **Iš viso**.
    3. Pasirinkite **Gerai**.

3. Pasirinkite **Iš viso** duomenų šaltinį, pasirinkite **Įtraukti**, o tada atlikite šiuos veiksmus:

    1. Dialogo lango **Įtraukti duomenų šaltinį** skyriuje **Bendra** įveskite **Tuščias konteineris**.
    2. Dialogo lango **'Tuščio konteinerio šaltinio ypatybės** lauke **Pavadinimas** įveskite **Puslapis**.
    3. Pasirinkite **Gerai**.

4. Dar kartą pasirinkite **Įtraukti** ir atlikite tolesnius veiksmus.

    1. Dialogo lango **Įtraukti duomenų šaltinį** skyriuje **Bendra** įveskite **Tuščias konteineris**.
    2. Dialogo lango **'Tuščio konteinerio šaltinio ypatybės** lauke **Pavadinimas** įveskite **Vykdomas**.
    3. Pasirinkite **Gerai**.

5. Pasirinkite **„Total.Page”** duomenų šaltinį, pasirinkite **Įtraukti**, o tada atlikite šiuos veiksmus:

    1. Dialogo lango **Įtraukti duomenų šaltinį** skyriuje **Funkcijos** įveskite **Duomenų rinkinys**.
    2. Dialogo lango **'Duomenų rinkinio šaltinio ypatybės** lauke **Pavadinimas** įveskite **Suma**.
    3. Lauke **Elemento tipas** pasirinkite **Realusis skaičius**.
    4. Nustatykite **Rinkti visas vertes** parinktį į **Taip**.
    5. Pasirinkite **Gerai**.

6. Dar kartą pasirinkite **Įtraukti** ir atlikite tolesnius veiksmus.

    1. Dialogo lango **Įtraukti duomenų šaltinį** skyriuje **Funkcijos** įveskite **Duomenų rinkinys**.
    2. Dialogo lango **'Duomenų rinkinio šaltinio ypatybės** lauke **Pavadinimas** įveskite **Svoris**.
    3. Lauke **Elemento tipas** pasirinkite **Realusis skaičius**.
    4. Nustatykite **Rinkti visas vertes** parinktį į **Taip**.
    5. Pasirinkite **Gerai**.

7. Pasirinkite **„Total.Running”** duomenų šaltinį, pasirinkite **Įtraukti**, o tada atlikite šiuos veiksmus:

    1. Dialogo lango **Įtraukti duomenų šaltinį** skyriuje **Funkcijos** įveskite **Duomenų rinkinys**.
    2. Dialogo lango **'Duomenų rinkinio šaltinio ypatybės** lauke **Pavadinimas** įveskite **Suma**.
    3. Lauke **Elemento tipas** pasirinkite **Realusis skaičius**.
    4. Nustatykite **Rinkti visas vertes** lauką į **Taip**.
    5. Pasirinkite **Gerai**.

8. Dar kartą pasirinkite **Įtraukti** ir atlikite tolesnius veiksmus.

    1. Dialogo lango **Įtraukti duomenų šaltinį** skyriuje **Funkcijos** įveskite **Duomenų rinkinys**.
    2. Dialogo lango **'Duomenų rinkinio šaltinio ypatybės** lauke **Pavadinimas** įveskite **Svoris**.
    3. Lauke **Elemento tipas** pasirinkite **Realusis skaičius**.
    4. Nustatykite **Rinkti visas vertes** lauką į **Taip**.
    5. Pasirinkite **Gerai**.

9. Dar kartą pasirinkite **Įtraukti** ir atlikite tolesnius veiksmus.

    1. Dialogo lango **Įtraukti duomenų šaltinį** skyriuje **Funkcijos** įveskite **Duomenų rinkinys**.
    2. Dialogo lango **'Duomenų rinkinio šaltinio ypatybės** lauke **Pavadinimas** įveskite **Eilutės**.
    3. Lauke **Elemento tipas** pasirinkite **Sveikasis skaičius**.
    4. Nustatykite **Rinkti visas vertes** lauką į **Taip**.
    5. Pasirinkite **Gerai**.

10. Pasirinkite **Įrašyti**.

### <a name="add-data-sources-to-control-page-footer-visibility"></a>Duomenų šaltinių įtraukimas į valdiklio puslapio poraštės matomumą

Jei planuojate valdyti puslapio poraštės matomumą ir jūs neplanuojate įtraukti poraštės į galutinį puslapį, jeigu jame yra operacijų, sukonfigūruokite naują duomenų šaltinį, kad būtų galima apskaičiuoti reikiamą vykdomą skaitiklį.

1. Puslapyje **Formato kūrimo įrankis** pasirinkite skirtuką **Susiejimas**.
2. Pasirinkite **„Total.Running”** duomenų šaltinį ir **Įtraukti**.
3. Dialogo lango **Įtraukti duomenų šaltinį** skyriuje **Funkcijos** įveskite **Duomenų rinkinys**.
4. Dialogo lango **'Duomenų rinkinio šaltinio ypatybės** lauke **Pavadinimas** įveskite **Eilutės2**.
5. Lauke **Elemento tipas** pasirinkite **Sveikasis skaičius**.
6. Nustatykite **Rinkti visas vertes** parinktį į **Taip**.
7. Pasirinkite **Gerai**.
8. Pasirinkite **Įrašyti**.

![Įtraukti duomenų šaltiniai į ER formatų rengyklę.](./media/er-paginate-excel-reports-format4.png)

### <a name="configure-bindings-to-collect-total-values"></a>Konfigūruoti susiejimus bendrų reikšmių surinkimui

1. Formatų medžio **Formatų rengyklės** puslapyje išplėskite **Ataskaitos eilučių** komponentą ir pasirinkite įdėtąjį **SF vertės** komponentą.
2. Pasirinkite **Redaguoti formulę**.
3. Pakeiskite susiejimo formulę iš `NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", "")` į `Total.Page.Amount.Collect(NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", ""))`.

    > [!NOTE]
    > Kartu su kiekvienos iteruotos operacijos sumos verte „Excel”, šis susiejimas surinks vertę **„Total.Page.Amount”** duomenų šaltinio duomenų rinkinyje.

4. Pasirinkite įdėtąjį **Svorio** komponentą.
5. Pasirinkite **Redaguoti formulę**.
6. Pakeiskite susiejimo formulę iš `@.'$RoundedWeight'` į `Total.Page.Weight.Collect(@.'$RoundedWeight')`.

    > [!NOTE]
    > Kartu su kiekvienos iteruotos operacijos sumos svoriu „Excel”, šis susiejimas surinks vertę **„Total.Page.Weight”** duomenų šaltinio duomenų rinkinyje.

![Sukonfigūruoti susiejimai, skirti bendroms vertėms rinkti ER formatų rengyklėje.](./media/er-paginate-excel-reports-format5.png)

### <a name="configure-bindings-to-fill-in-page-footer-totals"></a>Susiejimų konfigūravimas siekiant užpildyti puslapio poraštės sumas

1. Formatų medžio puslapyje **Formatų kūrimo priemone** išplėskite **Ataskaitos puslapio poraštę**, pasirinkite įtaisytąjį **Diapazono** komponentą, kuris nurodo į **„ReportPageFooter”\_„PageAmount”** langelį, o tada atlikite šiuos veiksmus:

    1. Dešiniajame duomenų šaltinio medyje pasirinkite **„Total.Page.Amount.Sum()”** elementą.
    2. Pasirinkite **Susieti**.
    3. Pasirinkite **Redaguoti formulę**.
    4. Atnaujinkite formulę į `Total.Page.Amount.Sum(false)`.

    > [!NOTE]
    > Turite šios funkcijos argumentą nurodyti kaip **Klaidinga**, kad išsaugotumėte surinktus dabartinio puslapio duomenis, nes šie duomenys yra reikalingi apskaičiuoti bendrą eigos sumą, bendrą eilučių skaičių puslapiui ir eilučių eigos skaitiklį.

2. Formatų medyje pasirinkite įtaisytąjį **Diapazono** komponentą, kuris nurodo į „Excel” **„ReportPageFooter”\_„PageWeight”** langelį, o tada atlikite šiuos veiksmus:

    1. Dešiniajame duomenų šaltinio medyje pasirinkite **„Total.Page.Weight.Sum()”** elementą.
    2. Pasirinkite **Susieti**.
    3. Pasirinkite **Redaguoti formulę**.
    4. Atnaujinkite formulę į `Total.Page.Weight.Sum(false)`.

### <a name="configure-bindings-to-fill-in-page-running-totals"></a>Susiejimų konfigūravimas siekiant užpildyti puslapio eigos sumas

1. Formatų medžio puslapyje **Formatų kūrimo priemone** išplėskite **Ataskaitos puslapio poraštę**, pasirinkite įtaisytąjį **Diapazono** komponentą, kuris nurodo į **„ReportPageFooter”\_„RunningTotalAmount”** langelį, o tada atlikite šiuos veiksmus:

    1. Dešiniajame duomenų šaltinio medyje pasirinkite **„Total.Running.Amount.Collect()”** elementą.
    2. Pasirinkite **Susieti**.
    3. Pasirinkite **Redaguoti formulę**.
    4. Atnaujinkite formulę į `Total.Running.Amount.Sum(false)+Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))`.

    > [!NOTE]
    > Operandas `Total.Running.Amount.Sum(false)` grąžina anksčiau surinktą bendrą sumą. Operandas `Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))` grąžina bendrą dabartinio puslapio sumą. Turite nurodyti antrojo operando įdėtosios funkcijos argumentą kaip **Teisinga**, kad iš naujo nustatytumėte `Total.Page.Amount` duomenų rinkinį, kai tik ši reikšme yra pridedama bendrame `Total.Running.Amount` eigos rinkinyje. Nurodytas argumentas turi pradėti rinkti kito puslapio sumą nuo 0 (nulinės) vertės.
    >
    > Iškviečiama `Total.Running.Amount.Sum(false)` funkcija, jog būtų įvedama bendra eigos suma „Excel” langelyje **ReportPageFooter\_„RunningTotalAmount”** dabartiniame puslapyje.

2. Formatų medyje pasirinkite įtaisytąjį **Diapazono** komponentą, kuris nurodo į „Excel” **„ReportPageFooter”\_„RunningTotalWeight”** langelį, o tada atlikite šiuos veiksmus:

    1. Dešiniajame duomenų šaltinio medyje pasirinkite **„Total.Running.Weight.Collect()”** elementą.
    2. Pasirinkite **Susieti**.
    3. Pasirinkite **Redaguoti formulę**.
    4. Atnaujinkite formulę į `Total.Running.Weight.Sum(false)+Total.Running.Weight.Collect(Total.Page.Weight.Sum(true))`.

### <a name="configure-bindings-to-fill-in-the-page-running-counter"></a>Susiejimų konfigūravimas siekiant užpildyti puslapio eigos skaitiklį

1. Formatų medžio puslapyje **Formatų kūrimo priemone** išplėskite **Ataskaitos puslapio poraštę** ir pasirinkite įtaisytąjį **Diapazono** komponentą, kuris nurodo į **„ReportPageFooter”\_„RunningCounterLines”** langelį.
2. Pasirinkite **Redaguoti formulę**.
3. Įtraukite formulę `Total.Running.Lines.Collect(COUNT(Total.Page.Amount.Result))`.

    > [!NOTE]
    > Ši formulė grąžina visos ataskaitos surinktų sumos reikšmių skaičių. Šis skaičius yra lygus operacijų, kurios šiuo metu buvo iteruotos, skaičių. Tuo pat metu formulė surenka grąžintą reikšmę **„Total.Running.Lines”** rinkinyje.

### <a name="configure-bindings-to-fill-in-the-page-footer-counter"></a>Susiejimų konfigūravimas siekiant užpildyti puslapio poraštės skaitiklį

1. Formatų medžio puslapyje **Formatų kūrimo priemone** išplėskite **Ataskaitos puslapio poraštę** ir pasirinkite įtaisytąjį **Diapazono** komponentą, kuris nurodo į **„ReportPageFooter”\_„PageLines”** langelį.
2. Pasirinkite **Redaguoti formulę**.
3. Įtraukite formulę `COUNT(Total.Page.Amount.Result)-Total.Running.Lines.Sum(false)`.

    > [!NOTE]
    > Ši formulė dabartiniame puslapyje skaičiuoja operacijų skaičių kaip skirtumą tarp operacijų, kurios buvo surinktos **„Total.Page.Amount.Result”** visai ataskaitai, skaičiaus ir operacijų kurios buvo įrašytos šiame etape **„Total.Running.Lines.Sum”**, skaičiaus. Dėl to, kad dabartinio puslapio operacijų skaičius yra saugomas **„Total.Running.Lines”** komponento **Diapazonas**, kuris nurodo į „Excel” **„ReportPageFooter”\_„RunningCounterLines”** langelį, susiejime, dabartinio puslapio operacijų skaičius dar nėra įtrauktas. Todėl šis skirtumas yra lygus dabartinio puslapio operacijų skaičiui.

![Sukonfigūruoti susiejimai, skirti puslapio poraštės skaitikliui užpildyti ER formatų rengyklėje.](./media/er-paginate-excel-reports-format6.png)

### <a name="configure-component-visibility"></a>Komponento matomumo konfigūravimas

Jūs galite pakeisti puslapio antraštės ir poraštės matomumą konkrečiame sugeneruoto dokumento puslapyje, kad paslėptumėte šiuos elementus:

- Puslapio antraštę pirmajame puslapyje, nes ataskaitos antraštėje jau yra stulpelių pavadinimų
- Puslapio antraštė bet kuriame puslapyje, neturinčiame operacijų, kurios gali įvykti paskutiniame puslapyje
- Puslapio poraštė bet kuriame puslapyje, neturinčiame operacijų, kurios gali įvykti paskutiniame puslapyje

Norėdami pakeisti matomumą, atnaujinkite **Ataskaitos puslapio antraštės** ir **Ataskaitos puslapio poraštės** komponentų **Įgalinta** ypatybę.

1. Formatų medžio puslapyje **Formatų rengyklė** išplėskite **Ataskaitos puslapio** komponentą, pasirinkite įtaisytąjį **Ataskaitos puslapio antraštės** komponentą ir atlikite šiuos veiksmus:

    1. Pasirinkite **Redaguoti** laukui **Įgalinta**.
    2. Puslapio **Formulių dizaino įrankis** lauke **Formulė** įveskite šią išraišką:

        `AND(`<br>
        `COUNT(Total.Page.Amount.Result)<>0,`<br>
        `COUNT(Total.Page.Amount.Result)<>COUNT(model.CommodityRecord)`<br>
        `)`

2. Formatų medyje pasirinkite įdėtąjį **Ataskaitos puslapio poraštė** komponentą ir tada atlikite šiuos veiksmus:

    1. Pasirinkite **Redaguoti** laukui **Įgalinta**.
    2. Puslapio **Formulių dizaino įrankis** lauke **Formulė** įveskite šią išraišką:

        `(`<br>
        `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)+`<br>
        `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result))`<br>
        `)<>0`

    > [!NOTE]
    > Konstrukcija `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)` yra naudojama skaičiuoti dabartinio puslapio operacijų skaičiui. Konstrukcija `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result)` yra naudojama įtraukti dabartinio puslapio operacijų skaičiui į rinkinį ir tinkamai valdyti tolesnio puslapio poraštės matomumą.
    >
    > Rinkinys `Total.Running.Lines` negali būti pakartotinai panaudotas čia, nes pagrindinio komponento ypatybė **Įgalinta** yra apdorojama **po** to, kai apdorojami įtaisytųjų komponentų susiejimai. Kai **Įgalinta** ypatybė yra apdorojama, `Total.Running.Lines` rinkinys jau yra padidintas dabartinio puslapio operacijų skaičiumi.

3. Pasirinkite **Įrašyti**.

## <a name="generate-an-intrastat-declaration-control-report-updated"></a>„Intrastat” deklaracijos kontrolės ataskaitos generavimas (atnaujinta)

1. Įsitikinkite, kad turite 24 operacijas **„Intrastat”** puslapyje. Pakartokite veiksmus, aprašytus šios temos [„Intrastat” deklaracijos valdiklio ataskaitos generavimas](#generate-intrastat-control-report) skyriuje, kad sugeneruotumėte ir peržiūrėtumėte valdiklio ataskaitą.

    Visos operacijos yra pateikiamos pirmajame puslapyje. Bendra puslapių suma ir skaitikliai yra lygūs ataskaitos sumoms ir skaitikliams. Puslapio antraštės diapazonas yra paslėptas pirmajame puslapyje, nes ataskaitos antraštėje jau yra stulpelių pavadinimų. Puslapio antraštė ir poraštė yra paslėptos antrajame puslapyje, nes šiame puslapyje nėra operacijų.

    ![Sugeneruotas „Excel” dokumentas darbalaukio taikomojoje programoje.](./media/er-paginate-excel-reports-document2.gif)

2. Atnaujinkite dvi operacijas **„Intrastat”** puslapyje pakeisdami **Prekės numerio** kodą iš **„D00006”** į **„L0010”**. Atkreipkite dėmesį, kad naujos prekės produkto pavadinimas, **Aktyvi stereo ausinių pora**, yra ilgesnis nei pradinės prekės pavadinimas – **Standartinės ausinės**. Dėl šios situacijos teksto nukėlimas yra atitinkamame sugeneruoto dokumento langelyje. Dabar reikia atnaujinti dokumentų puslapių numeraciją ir su puslapiu susijusius sumavimą ir skaičiavimą. Pakartokite veiksmus, aprašytus [„Intrastat” deklaracijos valdiklio ataskaitos generavimas](#generate-intrastat-control-report) skyriuje, kad sugeneruotumėte ir peržiūrėtumėte valdiklio ataskaitą.

    Šiuo metu operacijos yra pateikiamos dviejuose puslapiuose, o bendrosios puslapių sumos ir skaitikliai apskaičiuojami teisingai. Puslapio antraštės diapazonas yra tinkamai paslėptas pirmajame puslapyje ir matomas antrajame puslapyje. Puslapio poraštė yra matoma abiejuose puslapiuose, nes juose yra operacijų.

    ![Atnaujintas sugeneruotas „Excel” dokumentas darbalaukio programoje.](./media/er-paginate-excel-reports-document3.gif)

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="is-there-any-way-to-recognize-when-the-final-page-is-processed-by-the-page-format-component"></a>Ar yra būdas atpažinti, kada galutinis puslapis yra apdorojamas pagal puslapio formato komponentą?

**Puslapio** komponentas [nerodo](er-fillable-excel.md#page-component-limitations) informacijos apie apdoroto puslapio skaičių ir bendro sugeneruoto dokumento puslapių skaičiaus. Neatsižvelgiant į tai, galite konfigūruoti ER [formules](er-formula-language.md), kad jos atpažintų galutinį puslapį. Toliau pateikiamas pavyzdys.

- Apskaičiuokite bendrą jau apdorotų operacijų skaičių naudodami **Ataskaitos puslapio** komponentą. Šį apskaičiavimą galite atlikti naudodami formulę `COUNT(Total.Page.Amount.Result)`. 
- Apskaičiuokite bendrą skaičių operacijų, kurias reikia apdoroti remiantis „`model.CommodityRecord`” susiejimu, sukonfigūruotu **Ataskaitos eilučių** komponentui. Galite atlikti šį skaičiavimą naudodami formulę `COUNT(model.CommodityRecord)`.
- Palyginkite du skaičius, kad atpažintumėte paskutinį puslapį. Kai abi vertės yra vienodos, sugeneruojamas paskutinis puslapis.

> [!NOTE]
> Rekomenduojame vadovautis šiuo principu tik tad, kai **Ataskaitos eilučių** komponento ypatybė **Įgalinta** neturi formulės, kuri gali grąžinti reikšmę [Klaidinga](er-formula-supported-data-types-primitive.md#boolean) vykdymo metu kai kuriems iteruotiems susieto [Įrašų sąrašo](er-formula-supported-data-types-composite.md#record-list) [įrašams](er-formula-supported-data-types-composite.md#record).

## <a name="additional-resources"></a>Papildomi ištekliai

- [Konfigūracijų kūrimas dokumentams „Excel“ formatu generuoti](er-fillable-excel.md)
- [DUOMENŲ RINKIMO duomenų šaltinių naudojimas elektroninių ataskaitų (ER) formatuose](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
