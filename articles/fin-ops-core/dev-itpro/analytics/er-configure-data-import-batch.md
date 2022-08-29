---
title: Paketinis duomenų importavimas iš rankiniu būdu pasirinktų failų
description: Šiame straipsnyje paaiškinama, kaip importuoti duomenis iš rankiniu būdu pasirinktų failų paketiniu režimu.
author: kfend
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: Release 10.0.25
ms.custom: 220314
ms.assetid: ''
ms.search.form: ERSolutionTable, ERImportFormatSourceTable, ERWorkspace
ms.openlocfilehash: 21a2ab5f0eb07dda92baf9cc04ee36caeff8b4ec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288235"
---
# <a name="import-data-from-manually-selected-files-in-batch-mode"></a>Paketinis duomenų importavimas iš rankiniu būdu pasirinktų failų

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Norėdami duomenis importuoti iš [neautomatiniu būdu pasirinktų gaunamų failų paketiniu režimu, norėdami naudoti elektroninių ataskaitų (ER)](general-electronic-reporting.md) sistemą, sukonfigūruokite ER [formatą](er-overview-components.md#format-component), kuris palaiko importavimą. Tada vykdykite modelio [susiejimą](er-overview-components.md#model-mapping-component) su paskirties **vietos tipu**, kuris naudoja šį formatą kaip duomenų šaltinį. Norėdami importuoti duomenis, naršydami raskite norimą importuoti failą ir pasirinkite juos neautomatiniu būdu. 

Nauja ER galimybė, palaikanti duomenų importavimą paketiniu režimu įgalina šį procesą konfigūruoti kaip nenaudojamą. Norėdami importuoti duomenis, iš ER vartotojo sąsajos (UI) planuodami naują paketinę užduotį, galite naudoti ER konfigūracijas.

Šiame straipsnyje paaiškinama, kaip baigti duomenų importavimą iš rankiniu būdu pasirinkto failo paketiniu režimu. Pavyzdžiuose tiekėjo operacijos naudojamos kaip verslo duomenys. Šių pavyzdžių žingsnius galima atlikti **JAVMF įmonėje**. Kodavimas nebūtinas.

## <a name="prerequisites"></a>Būtinieji komponentai

Norėdami užbaigti pavyzdžius šiame straipsnyje, turite turėti šią prieigą:

- Vienas iš šių vaidmenų:

    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

- ER formatas ir modelio konfigūracijos, skirti 1099 mokėjimams

### <a name="create-the-required-er-configurations"></a>Kurti būtinas ER konfigūracijas

Norėdami sukurti būtinas ER konfigūracijas ir gauti kitas būtinąsias sąlygas, atlikite vieną iš šių veiksmų:

- Leiskite užduočių vedlius **ER importavimo duomenys iš „Microsoft Excel“ failas**, kurie yra **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų(10677)** verslo proceso dalis. Šios užduotys paaiškina, kaip kurti ir naudoti ER konfigūracijas, kurios interaktyviai importuoja tiekėjo operacijas iš Microsoft Excel failų. Daugiau informacijos žr. [„Excel“ formatu gaunamų dokumentų analizė](parse-incoming-documents-excel.md).
- Užbaikite pavyzdžių konfigūravimo [duomenų importavimą iš SharePoint](er-configure-data-import-sharepoint.md). Šiuose pavyzdžiuose paaiškinamas ER konfigūracijų kūrimo ir naudojimo procesas, kuris interaktyviai importuoja tiekėjo operacijas iš Excel failų, saugomų SharePoint aplanke.

### <a name="download-the-required-er-configurations"></a>Atsisiųsti reikiamas ER konfigūracijas

1. Atsisiųskite šias ER konfigūracijas ir įrašykite jas vietoje.

    | Turinio aprašas | Failas |
    |---------------------|------|
    | **1099 mokėjimų modelio** ER duomenų modelio konfigūravimas | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
    | **Tiekėjų operacijų (Excel) ER formato** konfigūracijai importuoti | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |

2. Naudokite pasirinktį [Įkelti iš XML failo](er-defer-sequence-element.md#import-the-sample-er-configurations) ER, norėdami importuoti atsisiųstas ER konfigūracijas į jūsų "Dynamics 365 Finance" egzempliorių šia tvarka:

    1. ER duomenų modelio konfigūracija
    2. ER formato konfigūracija

### <a name="download-the-required-excel-files"></a>Atsisiųsti reikiamus "Excel" failus

- Atsisiųskite toliau nurodytą duomenų rinkinio pavyzdį ir įrašykite jį vietoje.

    | Turinio aprašas | Failas |
    |---------------------|------|
    | **Gaunamas 1099import-data.xlsx** failas, kuriame yra importavimo duomenų pavyzdžiai | [1099import-data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

### <a name="review-the-prerequisites"></a>Peržiūrėkite būtinąsias sąlygas

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Konfigūracijos puslapyje **peržiūrėkite** paruoštą duomenų importavimo ER sprendimą paketiniu režimu.
3. Peržiūrėkite **formatų konfigūraciją Importuoti tiekėjų operacijas (Excel**).

    - Šios konfigūracijos formato komponentas sukurtas, norint išanalizuoti gaunamo Excel failą.
    - Šios konfigūracijos modelio susiejimo komponentas naudojamas norint užpildyti pagrindinį duomenų modelį naudojant iš išanalizuoto "Excel" failo duomenis.

    ![ER formato konfigūracija, skirta importuoti duomenis paketiniu režimu iš ER UI.](./media/er-configure-data-import-batch-configurations-1.png)

4. **Peržiūrėti 1099 mokėjimo modelio duomenų** modelio konfigūraciją.

    - Šios konfigūracijos modelio komponentas nurodo duomenų modelio struktūrą, naudojamą duomenims tarp paleisto ER komponentų perduoti.
    - Šios konfigūracijos modelio susiejimo komponentas naudojamas duomenims iš įvykdyto formato komponento gauti ir tada naujinti programos lenteles.

    ![ER duomenų modelio konfigūracija, skirta importuoti duomenis paketiniu režimu iš ER UI.](./media/er-configure-data-import-batch-configurations-2.png)

5. Programoje " **Excel" atidarykite failą 1099import-data.xlsx**.

    ![Pavyzdys "Excel" failas su duomenimis, kuriuos reikia importuoti paketiniu režimu.](./media/er-configure-data-import-batch-excel-content.png)

## <a name="enable-batch-data-import-for-er-from-the-ui"></a>Įgalinti ER paketinį duomenų importavimą iš UI

1. Eikite į **Sistemos administravimas** \> **Darbo sritys** \> **Funkcijų valdymas**.
2. Funkcijų valdymo **darbo srityje** pasirinkite neautomatiškai įkeltų **paketinių dokumentų importavimą į vykdyti ER** ir pasirinkite Įgalinti **dabar**.

## <a name="import-data-from-manually-selected-excel-files"></a>Importuoti duomenis iš rankiniu būdu pasirinktų Excel failų

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Konfigūracijos puslapyje **pasirinkite** **1099 mokėjimo modelio duomenų** modelio konfigūraciją.
3. Konfigūracijos komponentų "**FastTab**" pasirinkite **1099 rankinių operacijų importavimo** saitą.
4. Modelio ir **duomenų šaltinio susiejimo puslapyje** iš **anksto nepasirinktas 1099 rankinių** operacijų importavimo modelio susiejimas. Pasirinkite **Vykdyti**.
5. Skirtuke **Parametrai** pasirinkite **Naršyti**. Raskite ir pasirinkite **failą 1099import-data.xlsx**, tada pasirinkite **Gerai**.
6. Į lauką **Įveskite kvito ID**, įveskite **V-00001**.
7. Skirtuke **Vykdyti fone nustatykite** paketinio vykdymo **parinktį** **Taip**.

    Atkreipkite **dėmesį** **, kad užduoties aprašymo laukas nustatytas kaip Modelio susiejimo Vykdyti "Dėl 1099" neautomatinių operacijų importavimo, konfigūracija "1099 mokėjimo modelis"**. Ši vertė nurodo, kad pasirinkto modelio susiejimo vykdymas bus planuojamas kaip nauja paketinė užduotis.

    ![Nurodomas duomenų importavimo paketiniu režimu išsami informacija elektroninės ataskaitos parametrų dialogo lange.](./media/er-configure-data-import-batch-execution-parameters.png)

8. Pasirinkite **Gerai**. Pranešimas, praneša apie tai, kad suplanuota nauja paketinė užduotis.

    ![Pranešimas apie naują suplanuotą paketinę užduotį modelio ir duomenų šaltinio susiejimo puslapyje.](./media/er-configure-data-import-batch-scheduled-job-info.png)

## <a name="review-the-data-import-results-on-the-batch-job-page"></a>Duomenų importavimo rezultatų peržiūra paketinės užduoties puslapyje

1. Eikite į **Bendra** \> **Užklausos** \> **Paketinės užduotys** \> **Mano paketinės užduotys**.
2. Paketinės **užduoties** puslapyje filtruokite paketinių užduočių sąrašą, kad rastumėte suplanuotą paketą, tada pasirinkite jį.
3. Norėdami peržiūrėti užduoties **informaciją, pasirinkite užduoties ID** saitą.
4. Paketinių **užduočių "** FastTab" pasirinkite **Žurnalą**.

    ![Žurnalo mygtukas paketinės užduoties puslapyje.](./media/er-configure-data-import-batch-scheduled-job-record.png)

5. Peržiūrėkite vykdymo informaciją.

    ![Suplanuotos paketinės užduoties vykdymo žurnalas paketinės užduoties puslapyje.](./media/er-configure-data-import-batch-scheduled-job-log.png)

## <a name="change-the-data-import-parameters"></a>Keisti duomenų importavimo parametrus

Kai jūsų paketas suplanuotas ir dar nėra vykdomas, galite pakeisti suplanuoto duomenų importavimo parametrus.

1. Eikite į **Bendra** \> **Užklausos** \> **Paketinės užduotys** \> **Mano paketinės užduotys**.
2. Paketinės **užduoties** puslapyje filtruokite paketinių užduočių sąrašą, kad rastumėte suplanuotą paketą, tada pasirinkite jį.
3. Pasirinkti **Keisti būseną**.
4. Dialogo lange **Pasirinkti naują būseną** pasirinkite **Išskaita**, tada pasirinkite **Gerai**.
5. Norėdami pasiekti **užduoties informaciją, pasirinkite užduoties ID** saitą.
6. Paketinių **užduočių "** FastTab" pasirinkite **Parametrai**.
7. **Elektroninės ataskaitos parametrų dialogo** lange atlikite šiuos veiksmus:

    1. Norėdami **pasirinkti** alternatyvų duomenų importavimo failą, pasirinkite Naršyti.
    2. Pasirinkite **įvesti kvito ID**, kad būtų galima pakeisti tiekėjo operacijų importavimo kvito numerį.

        ![Pakeitus suplanuotos paketinės užduoties duomenų importavimo parametrus elektroninės ataskaitos parametrų dialogo lange.](./media/er-configure-data-import-batch-scheduled-job-parameters.png)

    3. Pasirinkite **Gerai**.

8. Įsitikinkite, kad paketas vis dar pažymėtas, tada dar kartą pasirinkite **Keisti būseną**.
9. Dialogo lange **Pasirinkti naują** būseną pasirinkite Laukiama **ir** pasirinkite **Gerai**.

## <a name="review-the-data-import-results-on-the-er-source-page"></a>Peržiūrėti duomenų importavimo rezultatus ER šaltinio puslapyje

1. Eikite į organizacijos **administravimo elektroninę** \> **ataskaitą –** \> **elektroninės ataskaitos šaltinis.**
2. Pasirinkite tiekėjo **operacijų (Excel)** importavimo įrašą, kuris buvo automatiškai sukurtas importuojant duomenis.

    ![Tiekėjo operacijų (Excel) konfigūracijos importavimo įrašas elektroninių ataskaitų šaltinio puslapyje.](./media/er-configure-data-import-batch-files-source-1.png)

3. Šaltiniams **pasirinkite Failų valstijos**.
4. Importavimo **formato** **"FastTabs" failuose ir šaltinio** žurnaluose peržiūrėkite išsamią importavimo informaciją.
5. **"FastTab"** Failuose pasirinkite įrašą. Atkreipkite dėmesį, kad importuotas failas yra pridėtas prie šio įrašo.

    ![Importuotas failas, pridėtas prie šaltinio puslapio įrašo Failų valstijos.](./media/er-configure-data-import-batch-files-source-2.png)

6. Pasirinkite **priedus, kad** peržiūrėtumėte importuotą failą.

    ![Importuotas failas dokumento peržiūros puslapyje.](./media/er-configure-data-import-batch-files-source-3.png)

    > [!TIP]
    > Kad būtų išsaugoti šie priedai, ER [...](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)**sistema** naudoja dokumento tipą, nustatytą dabartinei įmonei ER parametrų lauke Kita.

## <a name="review-the-data-import-results-on-the-vendor-settlement-for-1099s-page"></a>Peržiūrėti tiekėjo sudengimo 1099 puslapyje duomenų importavimo rezultatus

1. Pereikite į mokėtinų **sumų periodines** \> **užduotis** \> **Mokestis 1099** \> **tiekėjo sudengimas už 1099.**
2. Lauke Pradžios **data įveskite** **2017-12-31 (2017** m. gruodžio 31 d.).
3. Pasirinkite **rankiniu būdu 1099 operacijas**.

    ![Importuotos tiekėjo operacijos mokesčio 1099 operacijų puslapyje.](./media/er-configure-data-import-batch-imported-data.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
