---
title: Kelių vieno modelio šaknies išvestinių susiejimų tvarkymas
description: Šioje temoje paaiškinama, kaip tvarkyti kelis išvestinius susiejimus, sukonfigūruotus vienai modelio šakniai.
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a774a0edf00a17be674b7a1bb07f6494e90554c3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743684"
---
# <a name="manage-several-derived-mappings-for-a-single-model-root"></a>Kelių vieno modelio šaknies išvestinių susiejimų tvarkymas

[!include [banner](../includes/banner.md)]

[Elektroninių ataskaitų (ER)](general-electronic-reporting.md) duomenų [modelio](general-electronic-reporting.md#data-model-and-model-mapping-components) komponentas yra naudojamas kiekviename sukonfigūruoto ER [formato](general-electronic-reporting.md#FormatComponentOutbound) komponente kaip datos šaltinis, skirtas išvesties dokumentų generavimui. Norėdami aprašyti vieną verslo domeną, sukonfigūruokite duomenų modelio komponentą, turintį daug šakninių apibrėžimų. 

Kiekvienas šakninis apibrėžimas leidžia pateikti to domeno duomenis geriausiai tinkančiu būdu konkretiems ataskaitų tikslams. Kiekvienam šakniniam apibrėžimui galite konfigūruoti ER [modelio susiejimo](general-electronic-reporting.md#data-model-and-model-mapping-components) komponentą kaip „Microsoft Dynamics 365 Finance” – konkretų jūsų duomenų modelio įvykdymą. Tokiu būdu aprašote, kaip jūsų duomenų modelis bus pildomas vykdymo metu.

ER modelio susiejimo komponentai gali būti ER duomenų modelio [konfigūracijose](general-electronic-reporting.md#Configuration) ir ER modelių susiejimo konfigūracijose. Vienoje ER konfigūracijoje gali būti daug susiejimo komponentų, iš kurių kiekvienas sukonfigūruotas vienam šakniniam apibrėžimui. Tačiau vienoje ER konfigūracijoje gali būti ir tik vienas susiejimo komponentas, sukonfigūruotas vienam šakniniam apibrėžimui.

Daugelis konfigūracijų teikėjų gali pasiūlyti ER modelio susiejimo konfigūracijas tam pačiam ER duomenų modeliui. Šiose modelio susiejimo konfigūracijose gali būti susiejimo komponentų skirtingiems šakniniams apibrėžimams. Galite naudoti modelio susiejimą vienam šakniniam apibrėžimui, kurį siūlo vienas [tiekėjas](general-electronic-reporting.md#Provider) ir naudoti modelio susiejimą kitam tiekėjo siūlomam šakniniam apibrėžimui.

Šiose temos procedūrose paaiškinama, kaip tvarkyti kelias ER duomenų modelio susiejimo konfigūracijas, kai jose yra skirtingų modelio susiejimo komponentų, sukonfigūruotų tam pačiam šakniniam apibrėžimui. 

Norėdami atlikti šio skyriaus procedūras, jums turi būti priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo.

Visos šios procedūros gali būti atliktos „USMF” įmonėje. Kodavimas nebūtinas.

## <a name="configure-the-er-framework"></a>ER sistemos konfigūracija

Kaip elektroninės ataskaitos kūrėjo vaidmenį turintis vartotojas, [sukonfigūruokite mažiausią rinkinį](er-quick-start2-customize-report.md#ConfigureFramework) iš ER parametrų prieš pradėdami naudoti ER sistemą generuoti verslo dokumentams.

## <a name="import-the-standard-er-format-configurations"></a>Standartinio ER formato konfigūracijų importavimas

Norėdami įtraukti standartines ER konfigūracijas į jūsų dabartinį „Finance” egzempliorių, turite jas importuoti iš ER saugyklos, sukonfigūruotos tam egzemplioriui. Atlikite skyriaus [ER konfigūracijų atsisiuntimas iš Konfigūracijos tarnybos visuotinės saugyklos](er-download-configurations-global-repo.md) veiksmus importuoti šioms ER formato konfigūracijoms:

- **Laisvos formos sąskaita faktūra („Excel“)**, 220.106 versija
- **Projekto sąskaita faktūra („Excel“)**, 226.27 versija

## <a name="review-the-imported-er-configurations"></a>Importuotų ER konfigūracijų peržiūra

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos** dalyje pasirinkite plytelę **Konfigūracijų ataskaitos**.
3. Puslapio **Konfigūracijos** konfigūracijos medžio kairėje pusėje išplėskite **Sąskaitos faktūros modelis**.

    ![Importuotų konfigūracijų peržiūra puslapyje Konfigūracijos](./media/er-multiple-model-mappings-image1.png)

4. Peržiūrėkite **Laisvos formos sąskaitos faktūros („Excel”)** formatą:

    1. Konfigūracijos medžio kairėje pusėje pasirinkite **Laisvos formos sąskaita faktūra („Excel”)**.
    2. Veiksmų srityje pasirinkite **Dizaino įrankis**.
    3. Iš puslapio **Formato dizaino įrankis** skirtuko **Susiejimas** duomenų šaltinių sąrašo pasirinkite **Modelis**.
    4. Pasirinkite **Peržiūrėti**.
    
       Dabartinis ER formatas yra sukonfigūruotas naudoti **Sąskaitos faktūros modelio** šakninį apibrėžimą **Kliento sąskaita faktūra**. Kai vykdomas šis formatas ir iškviečiamas **Modelio** duomenų šaltinis, šakniniam apibrėžimui **Kliento sąskaita faktūra** sukonfigūruotas susiejimo modelis yra naudojamas programai pasiekti ir duomenų modeliui užpildyti.

        ![Modelio duomenų šaltinio peržiūra puslapyje Formato dizaino įrankis](./media/er-multiple-model-mappings-image2.png)

    6. Uždarykite puslapį **Formato dizaino įrankis**.

5. Peržiūrėkite konfigūracijos **Sąskaitos faktūros susiejimo modelis** turinį:

    1. Konfigūracijos medžio kairiojoje srityje pasirinkite **Sąskaitos faktūros susiejimo modelis**.
    2. Veiksmų srityje pasirinkite **Dizaino įrankis**.
    3. Puslapyje **Duomenų šaltinio susiejimo modelis** atkreipkite dėmesį, kad dabartinėje ER modelio susiejimo konfigūracijoje yra keli susiejimo komponentai:

        + Modelio susiejimas **Kliento sąskaita faktūra** yra sukonfigūruotas **Sąskaitos faktūros modelio** šakniniam apibrėžimui **Kliento sąskaita faktūra**. Todėl, kai vykdomas **Laisvos formos sąskaitos faktūros („Excel”)** ER formatas, šios ER konfigūracijos susiejimo modelis **Kliento sąskaita faktūra** gali būti pasirenkamas programos duomenims pasiekti ir duomenų modeliui užpildyti.
        + Modelio susiejimas **Projekto sąskaita faktūra** yra sukonfigūruotas **Sąskaitos faktūros modelio** šakniniam apibrėžimui **Sąskaitos faktūros projektas**. Todėl, kai vykdomas **Projekto sąskaitos faktūros („Excel”)** ER formatas, šios ER konfigūracijos susiejimo modelis **Projekto sąskaita faktūra** gali būti pasirenkamas programos duomenims pasiekti ir duomenų modeliui užpildyti.

        ![Sąskaitos faktūros susiejimo modelis puslapyje Duomenų šaltinio susiejimo modelis](./media/er-multiple-model-mappings-image3.png)

    4. Uždarykite puslapį **Duomenų šaltinio susiejimo modelis**.
    5. „FastTab” skirtuke **Versijos** pasirinkite **Naikinti** panaikinti visoms šios ER konfigūracijos versijoms, naujesnėms už 240.175.

6. Peržiūrėkite konfigūracijos **Projekto sąskaitos faktūros susiejimo modelis (RDP)** turinį:

    1. Konfigūracijos medžio kairiojoje srityje pasirinkite **Projekto sąskaitos faktūros susiejimo modelis (RDP)**.
    2. Veiksmų srityje pasirinkite **Dizaino įrankis**.
    3. Puslapyje **Duomenų šaltinio susiejimo modelis** atkreipkite dėmesį, kad dabartinėje ER modelio susiejimo konfigūracijoje yra **Projekto sąskaitos faktūros** susiejimo modelis ir jis yra sukonfigūruotas **Sąskaitos faktūros modelio** šakniniam apibrėžimui **Projekto sąskaitos faktūra**. Kai vykdomas **Projekto sąskaitos faktūros („Excel”)** ER formatas, pasirinkite šios ER konfigūracijos susiejimo modelį **Projekto sąskaita faktūra** programos duomenims pasiekti ir duomenų modeliui užpildyti.

        ![Projekto sąskaitos faktūros susiejimo modelis puslapyje Duomenų šaltinio susiejimo modelis](./media/er-multiple-model-mappings-image4.png)

    4. Uždarykite puslapį **Duomenų šaltinio susiejimo modelis**.
    5. „FastTab” skirtuke **Versijos** pasirinkite **Naikinti** panaikinti visoms šios ER konfigūracijos versijoms, naujesnėms už 226.35.

## <a name="customize-the-imported-er-configurations"></a>Importuotų ER konfigūracijų tinkinimas

Šiame skyriuje paaiškinama, kaip [tinkinti](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration) „Microsoft” teikiamus susiejimų modelius. Pavyzdžiui, tinkinimo gali reikėti pasirinktinės logikos įgyvendinimui arba trūkstamų susiejimų įtraukimui.

### <a name="customize-the-invoice-model-mapping-configuration"></a>Sąskaitos faktūros modelio susiejimo konfigūracijos tinkinimas

1. Puslapio **Konfigūracijos** konfigūracijos medžio kairiojoje srityje pasirinkite **Sąskaitos faktūros susiejimo modelis**.
2. Veiksmų srityje pasirinkite **Kurti konfigūraciją**.
3. Išplečiamojo dialogo lango **Kurti konfigūraciją** lauke **Nauja** pasirinkite **Išvesti iš pavadinimo: Sąskaitos faktūros susiejimo modelis, „Microsoft”**.
4. Lauke **Pavadinimas** įveskite **Sąskaitos faktūros susiejimo modelis „Litware”**.
5. Pasirinkite **Kurti konfigūraciją**.
6. [Pažymėkite](er-quick-start2-customize-report.md#MarkFormatRunnable) išvestinio susiejimo [juodraščio](general-electronic-reporting.md#component-versioning) versiją kaip galimą naudoti vykdymo metu.

    1. Veiksmų srities skirtuko **Konfigūracijos** grupėje **Išplėstiniai parametrai** pasirinkite **Vartotojo parametrai**.
    2. **Vartotojo parametrai** dialogo lange nustatykite **Leisti parametrus** parinktį į **Taip** ir pasirinkite **Gerai**.
    3. Pasirinkite **Redaguoti** tam, kad pagal poreikį galėtumėte redaguoti puslapį.
    4. Šiuo metu iš konfigūracijos medžio pasirinktai konfigūracijai **Sąskaitos faktūros susiejimo modelis „Litware”** nustatykite parinktį **Vykdyti juodraštį** į **Taip**.

7. Veiksmų srityje pasirinkite **Dizaino įrankis** šios konfigūracijos susiejimo modelių peržiūrai.

    ![Sąskaitos faktūros susiejimų modelio peržiūra puslapyje Duomenų šaltinio susiejimo modelis](./media/er-multiple-model-mappings-image5.png)

    > [!TIP]
    > Dabar galite atidaryti bet kurį šios ER konfigūracijos susiejimo modelio komponentą dizaino įrankyje tam, kad konfigūruotumėte jūsų pasirinktinę logiką. Daugiau informacijos žiūrėkite [Susiejimo modelio konfigūracijos tinkinimas](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration).

8. Uždarykite puslapį **Duomenų šaltinio susiejimo modelis**.

Dabar turite **Sąskaitos faktūros susiejimo modelis** ir **Sąskaitos faktūros susiejimo modelis „Litware”** konfigūracijos, kurių kiekviena turi susiejimo modelį, sukonfigūruotą **Kliento sąskaitos faktūros** šakniniam apibrėžimui. Tiesiogiai priskirkite vieną iš susiejimo modelių kaip numatytąjį susiejimo modelį, naudojamą bet kurio iš ER formatų, pavyzdžiui, **Laisvos formos sąskaita faktūra („Excel”)** formato, kuriame yra modelio duomenų šaltinis su **Kliento sąskaita faktūra** šakniniu apibrėžimu. Kitu atveju, kai paleidžiate, redaguojate ar tvirtinate vieną iš ER formatų, pateikiama ši išimtis, informuojanti, kad joks numatytasis susiejimo modelis nebuvo priskirtas tiesiogiai:
 
> Yra daugiau nei vienas susiejimo modelis '\<model name\> (\<root descriptor\>)' duomenų modeliui konfigūracijose \<configuration names separated by commas\>. Nustatykite vieną iš konfigūracijų kaip numatytąją.

![Formato atidarymas jo redagavimui Konfigūracijos puslapyje](./media/er-multiple-model-mappings-image6.gif)

### <a name="customize-the-project-invoice-model-mapping-rdp-configuration"></a>Projekto sąskaitos faktūros modelio susiejimo (RDP) konfigūracijos tinkinimas

1. Puslapio **Konfigūracijos** konfigūracijos medžio kairiojoje srityje pasirinkite **Projekto sąskaitos faktūros susiejimo modelis (RDP)**.
2. Veiksmų srityje pasirinkite **Kurti konfigūraciją**.
3. Dialogo lango **Kurti konfigūraciją** lauke **Nauja** pasirinkite **Išvesti iš pavadinimo: Projekto sąskaitos faktūros susiejimo modelis (RDP), „Microsoft”**.
4. Lauke **Pavadinimas** įveskite **Projekto sąskaitos faktūros modelio susiejimas „Litware”**.
5. Pasirinkite **Kurti konfigūraciją**.
6. Šiuo metu iš konfigūracijos medžio pasirinktai konfigūracijai **Projekto sąskaitos faktūros susiejimo modelis „Litware”** nustatykite parinktį **Vykdyti juodraštį** į **Taip**.
7. Veiksmų srityje pasirinkite **Dizaino įrankis** šios konfigūracijos susiejimo modelių peržiūrai.

    ![Tinkintos Projekto sąskaitos faktūros susiejimų modelio peržiūra puslapyje Duomenų šaltinio susiejimo modelis](./media/er-multiple-model-mappings-image7.png)

8. Uždarykite puslapį **Duomenų šaltinio susiejimo modelis**.

Dabar turite **Sąskaitos faktūros susiejimo modelio**, **Projekto sąskaitos faktūros susiejimo modelio (RDP)** ir **Sąskaitos faktūros susiejimo modelio „Litware”** konfigūracijas. Kiekviena iš šių konfigūracijų turi susiejimo modelį, sukonfigūruotą **Projekto sąskaitos faktūros** šakniniam apibrėžimui. Tiesiogiai priskirkite vieną iš susiejimo modelių kaip numatytąjį susiejimo modelį, kuris yra naudojamas bet kurio ER formato. Pavyzdžiui, naudokite **Projekto sąskaitos faktūros („Excel”)** formatą, kuriame yra duomenų modelio šaltinis su **Projekto sąskaitos faktūros** šakniniu apibrėžimu. Kitu atveju, kai paleidžiate ar redaguojate vieną iš ER formatų, pateikiama išimtis, informuojanti, kad joks numatytasis susiejimo modelis nebuvo priskirtas tiesiogiai.

## <a name="select-the-derived-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Pasirinkite išvestinio sąskaitos faktūros susiejimo modelio „Litware” konfigūraciją kaip konfigūraciją, kurioje yra numatytieji susiejimo modeliai

1. Puslapio **Konfigūracijos** konfigūracijos medžio kairiojoje srityje pasirinkite **Sąskaitos faktūros susiejimo modelis „Litware”**.
2. Nustatykite parinktį **Numatytasis modelių susiejimui** į **Taip**.

    ![Susiejimo modelio nustatymas kaip numatytojo susiejimo modelio puslapyje Konfigūracijos](./media/er-multiple-model-mappings-image8.png)

    Dėl šio parametro naudojamas **Kliento sąskaitos faktūros kopija** susiejimo modelis, kai vykdote **Laisvos formos sąskaita faktūrą („Excel”)** arba kai ją redaguojate arba tvirtinate. Nėra paisoma susiejimo modelio **Kliento sąskaita faktūra** iš **Sąskaitos faktūros susiejimo modelio** konfigūracijos.

    Dabar galite atidaryti **Laisvos formos sąskaitos faktūros („Excel”)** formatą jo peržiūrai formatų dizaino įrankyje.

## <a name="select-the-derived-project-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Pasirinkite išvestinio Projekto sąskaitos faktūros susiejimo modelio „Litware” konfigūraciją kaip konfigūraciją, kurioje yra numatytieji susiejimo modeliai

1. Puslapio **Konfigūracijos** konfigūracijos medžio kairiojoje srityje pasirinkite **Projekto sąskaitos faktūros susiejimo modelis „Litware”**.
2. Nustatykite parinktį **Numatytasis modelių susiejimui** į **Taip**.

    Tokiu atveju, skirtingai nei ankstesniame skyriuje aprašytoje **Sąskaitos faktūros susiejimo modelio „Litware”** konfigūracijoje, negalite naudoti **Projekto sąskaitos faktūros kopijos** modelio susiejimo iš **Projekto sąskaitos faktūros susiejimo modelio „Litware”** konfigūracijos. Dvi konfigūracijos, kuriose yra modelio susiejimas šakniniam apibrėžimui **Projekto sąskaitos faktūros** šiuo metu yra pažymėtos kaip numatytoji konfigūracija. Todėl jų naudojimo prioritetas yra vienodas. Šios problemos sprendimui atlikite likusius šios procedūros veiksmus.

3. Konfigūracijos medžio kairiojoje srityje pasirinkite **Sąskaitos faktūros susiejimo modelis „Litware”**.
4. Veiksmų srityje pasirinkite **Dizaino įrankis**.
5. Puslapyje **Duomenų šaltinio susiejimo modelis** pasirinkite **Redaguoti** tam, kad galėtumėte redaguoti puslapį taip, kaip reikia.
6. Pasirinkite susiejimo modelį **Projekto sąskaitos faktūros kopija** ir tada jam parinkite **Yra panaikintas** žymės langelį.

    ![Susiejimo modelio nustatymas kaip praktiškai ištrinto puslapyje Duomenų šaltinio susiejimo modelis](./media/er-multiple-model-mappings-image9.png)

    Dėl šio parametro laikoma, kad **Sąskaitos faktūros susiejimo modelio „Litware”** konfigūracija neturi susiejimo modelio **Projekto sąskaitos faktūros** šakniniam apibrėžimui. Pagal numatytuosius nustatymus, pateiktas **Projekto sąskaitos faktūros kopijos** susiejimo modelis. Konfigūracija **Projekto sąskaitos faktūros susiejimo modelio „Litware”**, turinti modelio susiejimą, yra pažymėta kaip numatytoji konfigūracija. Kadangi ji pažymėta kaip numatytoji, jos prioritetas yra aukštesnis nei **Projekto sąskaitos faktūros** susiejimo modelio iš **Projekto sąskaitos faktūros susiejimo modelio (RDP)** konfigūracijos.

## <a name="other-considerations"></a>Kiti svarstymai

Susiejimo modelis **Projekto sąskaitos faktūros kopija** iš **Projekto sąskaitos faktūros susiejimo modelio „Litware”** konfigūracijos yra sukurtas naudoti **Atskaitos duomenų teikėjo** duomenų šaltinį. Duomenų šaltinis yra dalis *Objekto* tipo, nurodančio **„PsaProjInvoiceDP”** programos klasę. Ši klasė yra įdiegta kaip duomenų tiekėjas projekto sąskaitos faktūros „SQL Server Reporting Services“ (SSRS) ataskaitai Spausdinimo valdymo sistemoje. Pasirinkite šį duomenų šaltinį kaip ER [integravimo tašką](er-apis-app10-0-11.md#api-to-run-a-format-mapping-for-the-generation-of-outbound-documents). Į šį parametrą atsižvelgiama dabartiniame ER diegime Spausdinimo valdymo ataskaitoms. Norėdami gauti išsamesnės informacijos, peržiūrėkite programos klasės **„ERPrintMgmtDataProviderReport”** šaltinio kodą. Vykdymo metu priskiriamas **Atskaitos duomenų teikėjo** duomenų šaltinis, nes susiejimo modelio integravimo taškas verčia „Finance” teikti didesnį prioritetą šiam susiejimo komponentui nei **Projekto sąskaitos faktūros** susiejimo komponentui iš **Projekto sąskaitos faktūros modelio susiejimo (RDP)** konfigūracijos.

## <a name="see-also"></a>Taip pat žiūrėkite

- [Atskirų ER konfigūracijų ER modelio susiejimo valdymas](./tasks/er-manage-model-mapping-configurations-july-2017.md)
- [Nuo šalies konteksto priklausomo ER modelio susiejimų konfigūravimas](er-country-dependent-model-mapping.md)
- [Elektroninių ataskaitų sistemos API pakeitimai](er-apis-app10-0-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]