---
title: Darbo su elektroninių SF priedu Italijai pradžia
description: Šiame straipsnyje pateikiama informacija, kuri padės jums pradėti nuo Italijos elektroninių SF išrašymo.
author: gionoder
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: a04866cef56aaa6f52a0177fae8c1e4f8fc6e70e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908988"
---
# <a name="get-started-with-electronic-invoicing-for-italy"></a>Darbo su elektroninių SF priedu Italijai pradžia

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> Italijos elektroninių SF išrašymas šiuo metu gali nepatebėti visų funkcijų, galimų elektroninėms Microsoft Dynamics SF 365 finansuose ir Dynamics 365 Supply Chain Management. 

Šiame straipsnyje pateikiama informacija, kuri padės jums pradėti nuo Italijos elektroninių SF išrašymo. Ji padės atlikti konfigūracijos veiksmus, priklausančius nuo šalies, „Regulatory Configuration Services” (RCS) ir „Finance”. Ji taip pat paaiškina, kaip pateikti elektronines SF, sugeneruotas Italijai būdingu formatu **„FatturaPA”**, naudojant paslaugą, ir kaip peržiūrėti apdorojimo rezultatus.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradėdami šiame straipsnyje nurodytus veiksmus, turite atlikti veiksmus dalyje Darbo su [elektroninių SF išrašymu pradžia](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>RCS sąranka

RCS nustatymo metu galėsite atlikti toliau pateiktas užduotis.

1. Importuoti el. SF išrašymo funkciją, skirtą kliento SF, kurių formatas **„FatturaPA”**, eksportavimui.
2. Peržiūrėti formato konfigūracijas, kurių reikia norint generuoti, pateikti ir gauti atsakymus apie elektronines SF.
3. Konfigūruoti įvykius, palaikančius elektroninių SF pateikimo scenarijus.
4. Publikuoti el. SF išrašymo funkciją.

> [!NOTE]
> „El. SF išrašymo funkcija” yra bendras išteklių, sukonfigūruotų ir publikuotų siekiant naudoti elektroninių SF išrašymo priedo serverį, pavadinimas. Šiuo atveju kliento elektroninių SF eksportavimas yra el. SF išrašymo funkcija, kurią nustatysite.

## <a name="import-the-e-invoicing-feature"></a>El. SF išrašymo funkcijos importavimas

1. Prisijunkite prie jūsų RCS abonemento.
2. Darbo srities **Globalizacijos funkcijos** dalyje **Funkcijos** pasirinkite plytelę **El. SF išrašymas**.
3. Puslapyje **El. SF išrašymo funkcijos** pasirinkite **Importuoti**, norėdami importuoti el. SF išrašymo funkciją iš visuotinės saugyklos.

    > [!NOTE]
    > Jei nematote pasiekiamų funkcijų sąrašo, pasirinkite **Sinchronizuoti**. 

4. Pasirinkite funkciją **El. SF eksportavimas (IT)** ir pasirinkite **Importuoti**.

![Funkcijos Elektroninių SF eksportavimas (IT) importavimas.](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

Kai importuojate funkciją **El. SF eksportavimas (IT)** iš visuotinės saugyklos, taip pat importuojami visi kituose skyriuose aprašyti parametrai.

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a>Naujos funkcijos El. SF eksportavimas (IT) versijos kūrimas

1. Puslapio **El. SF išrašymo funkcijos** skirtuke **Versijos** pasirinkite **Naujas**. 

    ![Naujos elektroninių SF išrašymo funkcijos versijos įtraukimas.](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    Taip pat sukonfigūruosite elektroninių ataskaitų (ER) formatus, susietus su el. SF išrašymo funkcija.

2. Skirtuke **Konfigūracijos** pasirinkite **Įtraukti**, norėdami valdyti konfigūracijos versijas.

    ![Elektroninės SF išrašymo funkcijos konfigūracijos versijų valdymas.](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    Šio etapo metu galite įtraukti ir konfigūruoti įvairių failų, kurie naudojami Italijos el. SF eksportuoti, ER formatus. Jei naudojate Italijos „FatturaPA” el. SF, naudokite toliau pateiktas standartines konfigūracijas arba faktines tinkintas konfigūracijas, kurias naudojate el. SF išrašymui.

    - Pardavimo SF (IT)
    - Projekto SF (IT)

    Kai kuriate el. SF išrašymo funkciją, išvestą iš kitos el. SF išrašymo funkcijos, visi ER formatai perduodami iš pradinės funkcijos.

3. Pasirinkite konkrečią ER formato failo konfigūraciją.
4. Norėdami atidaryti puslapį **Formato dizaino įrankis**, pasirinkite **Redaguoti** arba **Peržiūrėti**.

    ![Puslapio Formato dizaino įrankis atidarymas.](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. Norėdami redaguoti ir peržiūrėti ER formato failo konfigūracijas, naudokite puslapį **Formato dizaino įrankis**.

    ![Formato dizaino įrankio puslapis.](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>El. SF išrašymo funkcijos nustatymų valdymas

- Puslapio **El. SF išrašymo funkcijos** skirtuke **Nustatymai** pasirinkite **Įtraukti**, **Naikinti** arba **Redaguoti**, norėdami valdyti el. SF išrašymo funkcijos nustatymus.

![Elektroninių SF išrašymo funkcijos nustatymų valdymas.](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

Atlikdami šį veiksmą galite konfigūruoti įvykius, taikomus elektroninėms SF, įskaitant XML išvesties failų generavimą **„FatturaPA”** formatu ir pasirašymą skaitmeniniu būdu (jei reikia).

### <a name="configure-the-sales-invoice-feature-setup"></a>Pardavimo SF funkcijos nustatymo konfigūravimas

1. Puslapio **El. SF išrašymo funkcijos** skirtuko **Nustatymai** stulpelyje **Funkcijos nustatymas** pasirinkite **Pardavimo SF**.
2. Pasirinkite **Redaguoti**.
3. Puslapyje **Funkcijos versijos nustatymas** pasirinkite skirtuką **Veiksmai**, norėdami valdyti veiksmų sąrašą. Skirtukas Veiksmai nurodo operacijų, kurios turi būti vykdomos eilės tvarka siekiant visiškai įvykdyti įvykį, sąrašą.

    ![Skirtukas Veiksmai.](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | Veiksmo ID | Veiksmo pavadinimas        | Veiksmo aprašas                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | 1         | Transformuoti dokumentą | Kurkite el. SF XML failą **„FatturaPA”** formatu. |
    | 2         | Pasirašyti dokumentą      | Pritaikykite skaitmeninį parašą XML failui.             |

4. Norėdami peržiūrėti ir tvarkyti taikymo taisykles, pasirinkite skirtuką **Taikymo taisyklės**. Pritaikymo taisyklės nurodo kontekstą, kuriame bus vykdomas veiksmas.

    ![Skirtukas Taikymo taisyklės.](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. Pasirinkite skirtuką **Kintamieji**, norėdami peržiūrėti ir tvarkyti kintamuosius.

    ![Skirtukas Kintamieji.](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. Nustatykite viešuosius kintamuosius, reikalingus veiksmams vykdyti.

### <a name="configure-the-project-invoice-feature-setup"></a>Projekto SF funkcijos nustatymo konfigūravimas 

Veiksmai ir parametrai, reikalingi **Projekto SF** funkcijos nustatymui konfigūruoti, yra labai panašūs į **Pardavimo SF** funkcijos nustatymo veiksmus ir parametrus. Kai dirbate su projekto SF, peržiūrėkite pardavimo SF procedūras.

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a>El. SF išrašymo funkcijos priskyrimas aplinkai

1. Puslapio **El. SF išrašymo funkcijos** skirtuke **Aplinkos** pasirinkite **Įjungti**.
2. Lauke **Aplinka** pasirinkite aplinką.
3. Lauke **Galioja nuo** pasirinkite datą, kada aplinka turėtų įsigalioti.
4. Pasirinkite **Įjungti**. 

![Elektroninės SF išrašymo aplinkos įgalinimas.](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a>El. SF išrašymo funkcijos publikavimas

Galite publikuoti el. SF išrašymo funkciją pakeisdami versijos būseną į **Baigta** arba **Publikuota**.

### <a name="change-the-version-status-to-completed"></a>Versijos būsenos keitimas į Baigta

1. Puslapio **El. SF išrašymo funkcijos** skirtuke **Versijos** pasirinkite el. SF išrašymo funkcijos versiją, kurios būsena yra **Juodraštis**.
2. Pasirinkite **Keisti būseną \> Baigta**. 

### <a name="change-the-version-status-to-published"></a>Versijos būsenos keitimas į Publikuota 

1. Puslapio **El. SF išrašymo funkcijos** skirtuke **Versijos** pasirinkite el. SF išrašymo funkcijos versiją, kurios būsena yra **Baigta**.
2. Pasirinkite **Keisti būseną \> Publikuoti**.

![Elektroninės SF išrašymo funkcijos būsenos keitimas.](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-integration-in-finance"></a>Elektroninių SF išrašymo priedo integravimo nustatymas „Finance”

„Finance” nustatymo metu galėsite atlikti toliau pateiktas užduotis.

1. Importuokite ER duomenų modelį, ER duomenų modelio susiejimą ir konteksto konfigūracijas, skirtas „FatturaPA” el. SF.
2. Sukonfigūruokite sertifikatą, kurio reikia norint skaitmeniniu būdu pasirašyti Italijos el. SF.

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a>ER duomenų modelio, duomenų modelio susiejimo ir formatų importavimas

1. Darbo srityje **Elektroninės ataskaitos** įsitikinkite, kad **verslo dokumentų paslaugos** konfigūracijos teikėjas nustatytas į **Aktyvus**.
2. Pasirinkite **Saugyklos**.
3. Pasirinkite **Visuotiniai ištekliai \> Atidaryti**.
4. Importuokite **SF modelis**, **SF modelio susiejimas** ir **Kliento SF konteksto modelis**.

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a>Italijos kliento elektroninių SF eksportavimo funkcijos įjungimas

1. Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.
2. Skirtuke **Funkcijos** pažymėkite žymės langelį **Įjungta** eilutėje, skirtoje funkcijos nuorodai **IT00036**.

![Funkcijos „FatturaPA” įjungimas.](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a>Elektroninių dokumentų konfigūravimas

1. Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.
2. Skirtuke **Elektroninis dokumentas** pasirinkite **Įtraukti** ir įveskite lenteles, kurių reikia norint generuoti Italijos el. SF:

    - **Lentelės pavadinimas:** Kliento SF žurnalas
    - **Lentelės pavadinimas:** Projekto SF

3. Nurodykite kiekvienos lentelės susijusį dokumento kontekstą.

    - Dalyje **Kliento SF žurnalas** pasirinkite **Kliento SF kontekstas**.
    - Dalyje **Projekto SF** pasirinkite **Projekto SF kontekstas**.

![Atsakymų tipų nustatymas.](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a>El. SF apdorojimas

Apdorojimo „Finance” metu atliksite toliau pateiktas užduotis.

1. Italijos el. SF generavimas naudojant elektroninių SF išrašymo priedą
2. Vykdymo žurnalų ir apdorojimo rezultatų peržiūra

### <a name="generate-electronic-invoices"></a>Elektroninių SF generavimas

Įjungus funkciją **Konfigūruojamas elektroninių SF išrašymo priedo integravimas** ir suaktyvinus funkciją **IT00036**, nebegalima naudoti senojo „Finance” proceso, skirto Italijos el. SF generuoti. Jis pakeičiamas nauju procesu pavadinimu **Pateikti elektroninius dokumentus**.

Dokumentus galite pateikti neautomatiniu būdu, atsižvelgdami į el. SF dokumentų poreikį.

> [!NOTE]
> Prieš tęsdami įsitikinkite, kad nustatymas, reikalingas Italijos el. SF, buvo užbaigtas. Daugiau informacijos žr. [Kliento elektroninės SF](./emea-ita-e-invoices.md). Atkreipkite dėmesį, kad kai kurie šiame straipsnyje aprašyti nustatymo veiksmai gali būti negalimi dėl elektroninio SF išrašymo suaktyvinimo.

1. Eikite į **Organizacijos administravimas \> Laikotarpio \> Elektroniniai dokumentai \> Pateikti elektroninius dokumentus**.
2. Pirmą kartą pateikę bet kokį dokumentą, nustatykite parinktį **Iš naujo pateikti dokumentus** į **Ne**. Jei turite iš naujo pateikti dokumentą naudodami paslaugą, nustatykite šią parinktį į **Taip**.
3. „FastTab” **Įtrauktini įrašai** pasirinkite **Filtruoti**, kad būtų atidarytas dialogo langas **Užklausa**, kuriame galite kurti užklausą, norėdami pasirinkti dokumentus pateikimui.

![Dialogo langas Pateikti elektroninius dokumentus.](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a>Filtro užklausa

1. Dialogo lange **Užklausa** konfigūruokite pardavimo SF ir projekto SF filtravimo sąlygas arba palikite sąlygas tuščias, kad būtų įtrauktos visos nepateiktos SF.

    ![Pateikimo filtro kriterijų nustatymas.](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą **Užklausa**.
3. Pasirinkti **Gerai**, norėdami pateikti pasirinktus dokumentus.

> ![PASTABA] Pirmą kartą bandant pateikti dokumentą naudojant paslaugą, būsite paraginti patvirtinti ryšį su elektroninių SF išrašymo priedu. Pasirinkite **Spustelėkite čia, kad prisijungtumėte prie elektroninių dokumentų pateikimo paslaugos**.

#### <a name="view-submission-logs"></a>Pateikimo žurnalų peržiūra

Galite peržiūrėti visų pateiktų dokumentų pateikimo žurnalus.

1. Eikite į **Organizacijos administravimas \> Laikotarpio \> Elektroniniai dokumentai \> Elektroninio dokumento pateikimo žurnalas**.
2. Lauke **Dokumento tipas** pasirinkite **Kliento SF žurnalas** arba **Projekto SF**, norėdami filtruoti pagal reikiamus elektroninius dokumentus.

    ![Dokumento tipo pasirinkimas norint peržiūrėti pateikimo žurnalus.](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    Stulpelyje **Pateikimo būsena** rodoma reikšmė nurodo pateikimo proceso būseną. Ji nurodo, ar procesas buvo vykdomas kaip sukonfigūruotas ir ar reikia papildomų veiksmų.

3. Norėdami peržiūrėti išsamią pateikimo vykdymo žurnalų informaciją, veiksmų srityje pasirinkite **Užklausos \> Pateikimo informacija**.

    ![Pateikimo žurnalo informacijos peržiūra.](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. „FastTab” **Apdorojimo veiksmai** galite peržiūrėti veiksmų, sukonfigūruotų funkcijos versijoje, nustatytoje RCS, vykdymo žurnalą. Stulpelyje **Būsena** nurodoma, ar veiksmas sėkmingai įvykdytas.
5. „FastTab” **Veiksmų failai** galite peržiūrėti tarpinius failus, sugeneruotus veiksmų vykdymo metu. Galite pasirinkti **Peržiūrėti**, norėdami atsisiųsti išvesties XML failą **FatturaPA** formatu ir peržiūrėti jo turinį.

## <a name="related-topics"></a>Susijusios temos

- [Elektroninių SF išrašymo priedo apžvalga](e-invoicing-service-overview.md)
- [Darbo su elektroninių SF priedu pradžia](e-invoicing-get-started.md)
- [Elektroninių SF nustatymas](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
