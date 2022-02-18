---
title: Importuokite duomenis iš rankiniu būdu pasirinktų failų paketiniu režimu
description: Šioje temoje paaiškinama, kaip importuoti duomenis iš rankiniu būdu pasirinktų failų paketiniu režimu.
author: NickSelin
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERImportFormatSourceTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: Release 10.0.25
ms.openlocfilehash: 8615b5a0623fd696c64f4ec03e481a2bcb16c0ac
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075754"
---
# <a name="import-data-from-manually-selected-files-in-batch-mode"></a>Importuokite duomenis iš rankiniu būdu pasirinktų failų paketiniu režimu

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Norėdami naudoti [Elektroninis ataskaitų teikimas (ER)](general-electronic-reporting.md) sistemą, norėdami importuoti duomenis iš rankiniu būdu pasirinktų gaunamų failų paketiniu režimu, sukonfigūruokite ER [formatu](er-overview-components.md#format-component) kuris palaiko importą. Tada paleiskite a [modelio kartografavimas](er-overview-components.md#model-mapping-component) iš **Į paskirties vietą** tipas, kuris naudoja tą formatą kaip duomenų šaltinį. Norėdami importuoti duomenis, suraskite failą, kurį norite importuoti, ir rankiniu būdu pasirinkite jį. 

Nauja ER galimybė, palaikanti duomenų importavimą paketiniu režimu, leidžia konfigūruoti šį procesą kaip be priežiūros. Duomenims importuoti galite naudoti ER konfigūracijas suplanuodami naują paketinę užduotį iš ER vartotojo sąsajos (UI).

Šioje temoje paaiškinama, kaip užbaigti duomenų importavimą iš rankiniu būdu pasirinkto failo paketiniu režimu. Pavyzdžiuose tiekėjo operacijos naudojamos kaip verslo duomenys. Šių pavyzdžių veiksmus galima atlikti **USMF** bendrovė. Kodavimas nebūtinas.

## <a name="prerequisites"></a>Būtinieji komponentai

Norint įvykdyti šios temos pavyzdžių užduotis, reikia toliau nurodytų prieigų.

- Vienas iš šių vaidmenų:

    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

- ER formato ir modelio konfigūracijos 1099 mokėjimams

### <a name="create-the-required-er-configurations"></a>Sukurkite reikiamas ER konfigūracijas

Norėdami sukurti reikiamas ER konfigūracijas ir gauti kitas būtinas sąlygas, atlikite vieną iš šių veiksmų:

- Leiskite užduočių vedlius **ER importavimo duomenys iš „Microsoft Excel“ failas**, kurie yra **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų(10677)** verslo proceso dalis. Šie užduočių vadovai paaiškina ER konfigūracijų, kurios interaktyviai importuoja tiekėjo operacijas iš Microsoft Excel failus. Daugiau informacijos žr. [„Excel“ formatu gaunamų dokumentų analizė](parse-incoming-documents-excel.md).
- Užpildykite pavyzdžius [Konfigūruoti duomenų importavimą iš SharePoint](er-configure-data-import-sharepoint.md). Šie pavyzdžiai paaiškina, kaip kurti ir naudoti ER konfigūracijas, kurios interaktyviai importuoja tiekėjo operacijas iš „Excel“ failų, saugomų SharePoint aplanką.

### <a name="download-the-required-er-configurations"></a>Atsisiųskite reikiamas ER konfigūracijas

1. Atsisiųskite šias ER konfigūracijas ir išsaugokite jas vietoje.

    | Turinio aprašas | Failas |
    |---------------------|------|
    | **1099 Mokėjimų modelis** ER duomenų modelio konfigūracija | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
    | **Pardavėjų operacijų importavimui (Excel)** ER formato konfigūracija | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |

2. Naudoti [Įkelti iš XML failo](er-defer-sequence-element.md#import-the-sample-er-configurations) ER parinktis, skirta importuoti atsisiųstas ER konfigūracijas į savo egzempliorių Dynamics 365 Finance tokia tvarka:

    1. ER duomenų modelio konfigūracija
    2. ER formato konfigūracija

### <a name="download-the-required-excel-files"></a>Atsisiųskite reikiamus Excel failus

- Atsisiųskite toliau pateiktą duomenų rinkinio pavyzdį ir išsaugokite jį vietoje.

    | Turinio aprašas | Failas |
    |---------------------|------|
    | Įeinantis **1099import-data.xlsx** failą, kuriame yra importuotinų duomenų pavyzdžiai | [1099import-data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

### <a name="review-the-prerequisites"></a>Peržiūrėkite būtinas sąlygas

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Ant **Konfigūracijos** puslapyje, peržiūrėkite parengtą ER sprendimą duomenų importavimui paketiniu režimu.
3. Peržiūrėkite **Pardavėjų operacijų importavimui (Excel)** formato konfigūracija.

    - Šios konfigūracijos formato komponentas skirtas analizuoti gaunamą Excel failą.
    - Šios konfigūracijos modelio susiejimo komponentas naudojamas baziniam duomenų modeliui užpildyti naudojant duomenis iš analizuojamo „Excel“ failo.

    ![ER formato konfigūracija, skirta duomenims paketiniu režimu importuoti iš ER vartotojo sąsajos.](./media/er-configure-data-import-batch-configurations-1.png)

4. Peržiūrėkite **1099 Mokėjimų modelis** duomenų modelio konfigūracija.

    - Šios konfigūracijos modelio komponentas atspindi duomenų modelio, kuris naudojamas duomenims perduoti tarp veikiančių ER komponentų, struktūrą.
    - Šios konfigūracijos modelio susiejimo komponentas naudojamas duomenims iš vykdomo formato komponento gauti ir tada atnaujinti taikomųjų programų lenteles.

    ![ER duomenų modelio konfigūracija, skirta duomenims importuoti paketiniu režimu iš ER vartotojo sąsajos.](./media/er-configure-data-import-batch-configurations-2.png)

5. Atidaryk **1099import-data.xlsx** failą „Excel“.

    ![Pavyzdinis Excel failas su duomenimis, skirtas importuoti paketiniu režimu.](./media/er-configure-data-import-batch-excel-content.png)

## <a name="enable-batch-data-import-for-er-from-the-ui"></a>Įgalinti paketinį ER duomenų importavimą iš vartotojo sąsajos

1. Eikite į **Sistemos administravimas** \> **Darbo sritys** \> **Funkcijų valdymas**.
2. Viduje konors **Funkcijų valdymas** darbo sritį, pasirinkite **Vykdykite ER importavimą rankiniu būdu įkeltų dokumentų paketu** funkcija, tada pasirinkite **Įgalinti dabar**.

## <a name="import-data-from-manually-selected-excel-files"></a>Importuokite duomenis iš rankiniu būdu pasirinktų Excel failų

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Ant **Konfigūracijos** puslapyje pasirinkite **1099 Mokėjimų modelis** duomenų modelio konfigūracija.
3. Ant **Konfigūracijos komponentai** FastTab, pasirinkite **1099 neautomatinių operacijų importui** nuoroda.
4. Ant **Modelio ir duomenų šaltinio atvaizdavimas** puslapis, **1099 neautomatinių operacijų importui** modelio atvaizdavimas yra iš anksto pasirinktas. Pasirinkite **Vykdyti**.
5. Ant **Parametrai** skirtuką, pasirinkite **Naršyti**. Raskite ir pasirinkite **1099import-data.xlsx** failą, tada pasirinkite **Gerai**.
6. Viduje konors **Įveskite kupono ID** lauką, įveskite **V-00001**.
7. Ant **Paleisti fone** skirtuką, nustatykite **Paketinis apdorojimas** galimybė į **Taip**.

    Atkreipkite dėmesį, kad **Užduoties aprašymas** laukas nustatytas į **Modelio susiejimo vykdymas „1099 neautomatinių operacijų importui“, konfigūracija „1099 mokėjimų modelis“**. Ši reikšmė rodo, kad pasirinkto modelio susiejimo vykdymas bus suplanuotas kaip nauja paketinė užduotis.

    ![Duomenų importavimo paketiniu režimu detalių nurodymas dialogo lange Elektroninės ataskaitos parametrai.](./media/er-configure-data-import-batch-execution-parameters.png)

8. Pasirinkite **Gerai**. Pranešimas praneša, kad suplanuota nauja paketinė užduotis.

    ![Pranešimas apie naują suplanuotą paketinę užduotį modelio duomenų šaltinio susiejimo puslapyje.](./media/er-configure-data-import-batch-scheduled-job-info.png)

## <a name="review-the-data-import-results-on-the-batch-job-page"></a>Peržiūrėkite duomenų importavimo rezultatus paketinio darbo puslapyje

1. Eikite į **Bendra** \> **Užklausos** \> **Paketinės užduotys** \> **Mano paketinės užduotys**.
2. Ant **Paketinis darbas** puslapyje, filtruokite paketinių užduočių sąrašą, kad rastumėte suplanuotą paketą, tada pasirinkite jį.
3. Pasirinkite **Darbo ID** nuoroda į darbo detales peržiūrėti.
4. Ant **Paketinės užduotys** FastTab, pasirinkite **Žurnalas**.

    ![Prisijungti mygtukas paketinio darbo puslapyje.](./media/er-configure-data-import-batch-scheduled-job-record.png)

5. Peržiūrėkite vykdymo detales.

    ![Suplanuotos paketinės užduoties vykdymo žurnalas Paketinės užduoties puslapyje.](./media/er-configure-data-import-batch-scheduled-job-log.png)

## <a name="change-the-data-import-parameters"></a>Pakeiskite duomenų importavimo parametrus

Kai paketas yra suplanuotas ir kol jis dar nebuvo paleistas, galite pakeisti suplanuoto duomenų importavimo parametrus.

1. Eikite į **Bendra** \> **Užklausos** \> **Paketinės užduotys** \> **Mano paketinės užduotys**.
2. Ant **Paketinis darbas** puslapyje, filtruokite paketinių užduočių sąrašą, kad rastumėte suplanuotą paketą, tada pasirinkite jį.
3. Pasirinkti **Keisti būseną**.
4. Viduje konors **Pasirinkite naują būseną** dialogo lange pasirinkite **Sulaikyti**, tada pasirinkite **Gerai**.
5. Pasirinkite **Darbo ID** nuoroda, kad pasiektumėte darbo informaciją.
6. Ant **Paketinės užduotys** FastTab, pasirinkite **Parametrai**.
7. Viduje konors **Elektroninės ataskaitos parametrai** dialogo lange, atlikite šiuos veiksmus:

    1. Pasirinkite **Naršyti** norėdami pasirinkti alternatyvų duomenų importavimo failą.
    2. Pasirinkite **Įveskite kupono ID** pakeisti tiekėjo operacijų importavimo kvito numerį.

        ![Suplanuotos paketinės užduoties duomenų importavimo parametrų keitimas dialogo lange Elektroninės ataskaitos parametrai.](./media/er-configure-data-import-batch-scheduled-job-parameters.png)

    3. Pasirinkite **Gerai**.

8. Įsitikinkite, kad partija vis dar pasirinkta, tada pasirinkite **Keisti būseną** vėl.
9. Viduje konors **Pasirinkite naują būseną** dialogo lange pasirinkite **Laukia**, tada pasirinkite **Gerai**.

## <a name="review-the-data-import-results-on-the-er-source-page"></a>Peržiūrėkite duomenų importavimo rezultatus ER šaltinio puslapyje

1. Eiti į **Organizacijos administravimas** \> **Elektroninis ataskaitų teikimas** \> **Elektroninių pranešimų šaltinis**.
2. Pasirinkite **Pardavėjų operacijų importavimui (Excel)** įrašas, kuris buvo automatiškai sukurtas importuojant duomenis.

    ![Elektroninių ataskaitų šaltinio puslapyje esančios konfigūracijos Tiekėjų operacijų importavimui (Excel) įrašas.](./media/er-configure-data-import-batch-files-source-1.png)

3. Pasirinkite **Šaltinių failų būsenos**.
4. Ant **Failai** ir **Importavimo formato šaltinio žurnalai** FastTabs, peržiūrėkite išsamią importavimo informaciją.
5. Ant **Failai** FastTab, pasirinkite įrašą. Atkreipkite dėmesį, kad importuotas failas pridedamas prie šio įrašo.

    ![Importuotas failas, pridėtas prie įrašo šaltinių puslapio Failo būsenose.](./media/er-configure-data-import-batch-files-source-2.png)

6. Pasirinkite **Priedai** norėdami peržiūrėti importuotą failą.

    ![Importuotas failas puslapyje Dokumento rodinys.](./media/er-configure-data-import-batch-files-source-3.png)

    > [!TIP]
    > Kad šie priedai būtų išsaugoti, ER sistema naudoja dokumento tipą, kuris yra [rinkinys](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) dabartinei įmonei **Kiti** ER parametrų lauką.

## <a name="review-the-data-import-results-on-the-vendor-settlement-for-1099s-page"></a>Peržiūrėkite duomenų importavimo rezultatus puslapyje Tiekėjo atsiskaitymas už 1099s

1. Eiti į **Mokėtinos sąskaitos** \> **Periodinės užduotys** \> **Mokestis 1099** \> **Pardavėjo atsiskaitymas už 1099s**.
2. Viduje konors **Nuo datos** lauką, įveskite **2017-12-31** (2017 m. gruodžio 31 d.).
3. Pasirinkite **Rankiniai 1099 sandoriai**.

    ![Importuotos tiekėjo operacijos puslapyje Mokesčių 1099 operacijos.](./media/er-configure-data-import-batch-imported-data.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
