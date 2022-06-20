---
title: Darbo su elektroninių SF priedu Meksikai pradžia
description: Šiame straipsnyje pateikiama informacija, kuri padės jums pradėti nuo Meksikai išrašytų elektroninių SF.
author: gionoder
ms.date: 12/01/2020
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
ms.openlocfilehash: 540b6e6f9b4b669957cc3310e473ad59b9210594
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855335"
---
# <a name="get-started-with-electronic-invoicing-for-mexico"></a>Darbo su elektroninių SF priedu Meksikai pradžia

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Meksikai skirtas elektroninių SF išrašymas šiuo metu gali nepatebėti visų funkcijų, kurios galimos "Comprobrašymą" fiskalinio skaitmeninio porų interneto (CFDI) dokumente, ir susijusio integravimo, Microsoft Dynamics kuris sukurtas į 365 finansus arba Dynamics 365 Supply Chain Management.

Šiame straipsnyje pateikiama informacija, kuri padės jums pradėti nuo Meksikai išrašytų elektroninių SF. Ji padės atlikti konfigūracijos veiksmus, priklausančius nuo šalies, „Regulatory Configuration Services” (RCS) ir „Finance”. Ji taip pat padeda jums atlikti veiksmus „Finance”, kurių reikia, kad CFDI SF būtų teikiamos naudojant paslaugą, ir paaiškina, kaip peržiūrėti apdorojimo rezultatus ir CFDI SF būsenas.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš atbaigdami šiame straipsnyje nurodytus veiksmus, [...](e-invoicing-get-started-service-administration.md)[turite atlikti veiksmus dalyje Darbo su elektroninių SF išrašymo tarnybos administravimu pradžia ir Darbo su elektroninių SF išrašymu pradžia](e-invoicing-get-started.md).

## <a name="set-up-the-cadena-xslt"></a>Nustatyti Cadena XSLT

Norėdami įtraukti Cadena XSLT schemą į CFDI apdorojimo globalizavimo funkciją, atlikite šiuos veiksmus.

1. Atsisiųsti schemą iš [SAT svetainės](http://www.sat.gob.mx/sitio_internet/cfd/3/cadenaoriginal_3_3/cadenaoriginal_3_3.xslt).
2. Glaudinti schemą į pašto failą.
3. Įrašykite xslt failą į savo "Azure" saugyklos abonementą, nustatytą jūsų paslaugų aplinkoje, kad būtų galima naudoti naują konteinerį.

## <a name="rcs-setup"></a>RCS sąranka

RCS nustatymo metu galėsite atlikti toliau pateiktas užduotis.

1. Importuoti el. SF išrašymo funkciją, skirtą CFDI SF apdorojimui.
2. Peržiūrėti formato konfigūracijas, kurių reikia norint generuoti, pateikti ir gauti atsakymus apie CFDI SF ir pateikti bei gauti atsakymus apie atšaukimą.
3. Konfigūruoti įvykius, palaikančius CFDI SF pateikimo scenarijus.
4. Publikuoti el. SF išrašymo funkciją, skirtą CFDI SF.

> [!NOTE]
> „El. SF išrašymo funkcija” yra bendras išteklių, sukonfigūruotų ir publikuotų siekiant naudoti elektroninių SF išrašymo priedo serverį, pavadinimas. Šiuo atveju CFDI SF (MX) yra el. SF išrašymo funkcija, kurią nustatysite.

## <a name="import-the-e-invoicing-feature"></a>El. SF išrašymo funkcijos importavimas

1. Prisijunkite prie jūsų RCS abonemento.
2. Darbo srities **Globalizacijos funkcijos** dalyje **Funkcijos** pasirinkite plytelę **El. SF išrašymas**.
3. Puslapyje **El. SF išrašymo funkcijos** pasirinkite **Importuoti**, norėdami importuoti funkciją **CFDI SF (MX)** iš visuotinės saugyklos.

    > [!NOTE]
    > Jei sąraše nematote funkcijos, pasirinkite **Sinchronizuoti** ir pakartokite 3 veiksmą.

![CFDI SF (MX) funkcijos importavimas.](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

Kai importuojate funkciją **CFDI SF (MX)** iš visuotinės saugyklos, taip pat importuojami visi funkcijų parametrai, įskaitant konfigūracijas ir veiksmus.

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a>Naujos CFDI SF (MX) funkcijos versijos kūrimas

Galite sukurti naują versiją, jei, pavyzdžiui, reikia atnaujinti URL. Daugiau informacijos žr. [El. CFDI SF išrašymas](tasks/mx-00010-e-invoicing-cfdi.md).

- Puslapio **El. SF išrašymo funkcijos** skirtuke **Versijos** pasirinkite **Naujas**.

![Naujos elektroninių SF išrašymo funkcijos versijos įtraukimas.](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a>Konfigūracijos versijos naujinimas

1. Puslapio **El. SF išrašymo funkcijos** skirtuke **Konfigūracijos** pasirinkite **Įtraukti** arba **Naikinti**, norėdami valdyti konfigūracijos versijas (ER failo formato konfigūracijas).

    ![Elektroninių SF išrašymo funkcijos konfigūracijų valdymas.](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    Kai kuriate naują versiją, visos konfigūracijos perduodamos iš paskutinės publikuotos versijos. Norint apdoroti CFDI SF, būtinos toliau pateiktos konfigūracijos.

    - CFDI SF (BusinessDocumentService)
    - CFDI atsakymo pranešimo importavimas
    - CFDI klaidų žurnalo importavimas
    - CFDI atšaukimo užklausa (MX) (BusinessDocumentService)
    - CFDI SF (BusinessDocumentService)

2. Sąraše pasirinkite konfigūracijos versiją, tada pasirinkite **Redaguoti** arba **Peržiūrėti**, kad būtų atidarytas puslapis **Formato dizaino įrankis**, kuriame galite redaguoti arba peržiūrėti konfigūraciją.

    ![Puslapio Formato dizaino įrankis atidarymas.](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. Norėdami redaguoti ir peržiūrėti ER formato failo konfigūracijas, naudokite puslapį **Formato dizaino įrankis**. Daugiau informacijos žr. [Elektroninių dokumentų konfigūracijų kūrimas](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md).

    ![Formato dizaino įrankio puslapis.](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>El. SF išrašymo funkcijos nustatymų valdymas

- Puslapio **El. SF išrašymo funkcijos** skirtuke **Nustatymai** pasirinkite **Įtraukti**, **Naikinti** arba **Redaguoti**, norėdami valdyti el. SF išrašymo funkcijos nustatymus.

![Elektroninių SF išrašymo funkcijos nustatymų valdymas.](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

Norint pateikti CFDI SF autorizuoti (generuoti XML failą, pateikti XML failą ir apdoroti atsakymą), reikalingas **Pardavimo SF** funkcijos nustatymas.

Norint pateikti CFDI SF atšaukimą, reikalingi funkcijų **Atšaukimas** ir **Atšaukti** nustatymai.

### <a name="configure-the-sales-invoice-feature-setup"></a>Pardavimo SF funkcijos nustatymo konfigūravimas

1. Puslapio **El. SF išrašymo funkcijos** skirtuko **Nustatymai** stulpelyje **Funkcijos nustatymas** pasirinkite **Pardavimo SF**.
2. Pasirinkite **Redaguoti**, norėdami konfigūruoti veiksmus, taikymo taisykles ir kintamuosius.

    ![Elektroninių SF išrašymo funkcijos nustatymo redagavimas.](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. Puslapyje **Funkcijos versijos nustatymas** pasirinkite skirtuką **Veiksmai**, norėdami valdyti veiksmų sąrašą. Skirtukas Veiksmai nurodo operacijų, kurios turi būti vykdomos eilės tvarka siekiant visiškai įvykdyti įvykį, sąrašą.

    ![Skirtukas Veiksmai.](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | Veiksmo ID | Operacija                   | Veiksmo pavadinimas                                  | Veiksmo aprašas                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | 1         | Transformuoti dokumentą       | Generuoti CFDI el. SF be skaitmeninio parašo | Generuojama CFDI el. SF.                                |
    | 2         | Pasirašyti dokumentą            | Skaitmeninis parašas                                 | Pateikimo el. SF pasirašoma skaitmeniniu būdu.                |
    | 3         | Iškviesti Meksikos PAC tarnybą | Pateikti CFDI el. SF                        | „Windows” ryšio platformos (WCF) klientas pateikia CFDI el. SF. |
    | 4         | Apdoroti atsakymą         | Analizuoti žiniatinklio tarnybos atsakymą                 | Analizuojamas žiniatinklio tarnybos atsakymas ir grąžinamas klaidų žurnalas. |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a>Meksikos PAC žiniatinklio tarnybų URL nustatymas 

1. Puslapio **Funkcijos versijos nustatymas** skirtuko **Veiksmai** „FastTab” **Veiksmai** pasirinkite **Iškviesti Meksikos PAC tarnybą**.
2. „FastTab” **Parametrai** lauke **URL adresas** įveskite CFDI SF pateikimo žiniatinklio tarnybos URL.

> [!NOTE]
> Atlikite tuos pačius veiksmus, norėdami atnaujinti URL, skirtą funkcijų **Atšaukti** ir **Atšaukimo užklausa** nustatymų veiksmui **Iškviesti Meksikos PAC tarnybą**.

### <a name="set-up-the-path-for-the-cadena-xlst-schema"></a>Kada turi būti nustatytas Cadena XLST schemos maršrutas

1. Priemonės versijos **nustatymo puslapio** skirtuke **Kintamieji** **pasirinkite kintamojo pavadinimą DigitalSi skirtuke DigitalSi skirtukeXSLT**.
2. Reikšmės lauke **įveskite** : {containerUrl:"https://&lt; AccountStorageName&gt;.blob.core.windows.net/&lt; ContainerName&gt;","path":"&lt; RelativePath&gt;"}
   
    čia: \<RelativePath\> = aplanko\\ aplanko failo\\ vardas su dviem kairiosios brūkšnių, ContainerName turi nurodyti konteinerį, kuris naudojamas paslaugai.
   
    Kintamojo pavyzdys yra:
    
    {"kelias":"x xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx\\ dev\\ cadena_xslt","containerUrl":https://yyyyyyyyyy.blob.core.windows.net/containername}

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a>Juodraščio versijos priskyrimas el. SF išrašymo aplinkai

1. Puslapio **El. SF išrašymo funkcijos** skirtuke **Aplinkos** pasirinkite **Įjungti**.
2. Lauke **Aplinka** pasirinkite aplinką.
3. Lauke **Galioja nuo** pasirinkite datą, kada aplinka turėtų įsigalioti.
3. Pasirinkite **Įjungti**.

![Elektroninės SF išrašymo aplinkos įgalinimas.](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a>Versijos būsenos keitimas į Baigta

1. Puslapio **El. SF išrašymo funkcijos** skirtuke **Versijos** pasirinkite el. SF išrašymo funkcijos versiją, kurios būsena yra **Juodraštis**.
2. Pasirinkite **Keisti būseną \> Baigta**.

## <a name="change-the-version-status-to-published"></a>Versijos būsenos keitimas į Publikuota

- Puslapio **El. SF išrašymo funkcijos** skirtuke **Versijos** pasirinkite **Keisti būseną \> Publikuoti**.

## <a name="publish-the-e-invoicing-feature"></a>El. SF išrašymo funkcijos publikavimas

1. Puslapyje **El. SF išrašymo funkcijos** pasirinkite skirtuką **Versijos**, norėdami valdyti funkcijos **CFDI SF (MX)** būseną.
2. Pasirinkite **Keisti būseną**, norėdami pakeisti funkcijos būseną.

![Elektroninės SF išrašymo funkcijos būsenos keitimas.](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing--integration-in-finance"></a>Elektroninių SF išrašymo priedo integravimo nustatymas „Finance”

Norėdami nustatyti elektroninių SF išrašymo priedą „Finance”, atlikite toliau pateiktas užduotis.

1. Importuokite ER duomenų modelį, ER duomenų modelio susiejimą ir formatus, reikalingus CFDI SF.
2. Konfigūruokite atsakymų tipus CFDI SF atnaujinti. Šie atsakymų tipai naudojami įgaliotojo sertifikavimo teikėjo (PAC) serverio atsakymui.

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a>ER duomenų modelio, ER duomenų modelio susiejimo ir konteksto konfigūracijų, reikalingų CFDI SF, importavimas

1. Prisijunkite prie „Finance“.
2. Darbo srities **Elektroninės ataskaitos** dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **„Microsoft”**. Įsitikinkite, kad šis konfigūracijos teikėjas nustatytas kaip **Aktyvus**. Daugiau informacijos apie tai, kaip nustatyti teikėją į **Aktyvus**, žr. [Konfigūracijų teikėjų kūrimas ir jų pažymėjimas kaip aktyviais](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Pasirinkite **Saugyklos**.
4. Pasirinkite **Visuotiniai ištekliai \> Atidaryti**.
5. Importuokite **SF modelis**, **SF modelio susiejimas**, **CFDI SF formatas (MX)**, **CFDI SF atšaukimo užklausos formatas (MX)** ir **CFDI SF atšaukimo formatas (MX)**.

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a>CFDI SF apdorojimo funkcijos įjungimas

1. Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.
2. Skirtuke **Funkcijos** pažymėkite žymės langelį **Įjungti** eilutėse, skirtose funkcijos nuorodoms **MX-00010** ir **MX-00016**.

![CFDI SF apdorojimo funkcijų įjungimas.](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a>ER konfigūracijų importavimas ir CFDI SF naujinimo atsakymų tipų nustatymas

#### <a name="import-er-configurations"></a>Importuokite ER konfigūracijas

1. Darbo srities **Elektroninės ataskaitos** dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **„Microsoft”**.
3. Pasirinkite **Saugyklos**.
4. Pasirinkite **Visuotiniai ištekliai \> Atidaryti**.
5. Importuokite **Atsakymo pranešimo modelis**, **CFDI klaidų žurnalo importavimas (MX)** ir **CFDI atsakymo pranešimo importavimas (MX)**.

#### <a name="set-up-the-response-types"></a>Atsakymų tipų nustatymas

1. Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.
2. Skirtuke **Elektroninis dokumentas** pasirinkite **Įtraukti**.
3. Įveskite kliento SF žurnalą, tada lauke **Lentelės pavadinimas** pasirinkite projekto SF.
4. Nurodykite kiekvienos lentelės susijusį dokumento kontekstą.

    - Dalyje **Kliento SF žurnalas** įveskite **Kliento SF kontekstas**.
    - Dalyje **Projekto SF** įveskite **Projekto SF kontekstas**.

4. Pasirinkite **Atsakymų tipai**, norėdami sukonfigūruoti atsakymų tipus, kuriuos galima grąžinti iš elektroninių SF išrašymo priedo ir įtraukti į kliento SF žurnalą ar projekto SF.
5. Pasirinkite **Naujas**, tada lauke **Atsakymo tipas** pasirinkite **Atsakymas**.
6. Lauke **Pateikimo būsena** pasirinkite **Laukiama**.
7. Lauke **Modelio susiejimas** pasirinkite **Atsakymo pranešimo importavimo formatas – modelio susiejimas iš atsakymo pranešimo**.
8. Pasirinkite **Įrašyti**.
9. Pasirinkite **Naujas**, tada lauke **Atsakymo tipas** pasirinkite **Atsakymo duomenys**.
10. Lauke **Pateikimo būsena** pasirinkite **Laukiama**.
11. Lauke **Modelio susiejimas** pasirinkite **CFDI atsakymo duomenų importavimo formatas (informacija) – atsakymo duomenų importavimas**.
12. Pasirinkite **Įrašyti**.

## <a name="process-electronic-invoices-in-finance"></a>Elektroninių SF apdorojimas „Finance” 

CFDI SF apdorojimo metu „Finance” naudodami elektroninių SF išrašymo priedą galite atlikti toliau pateiktas užduotis:

- Pateikti CFDI SF.
- Peržiūrėti pateikimo vykdymo žurnalus.
- Pateikti CFDI SF atšaukimą.

### <a name="submit-cfdi-invoices"></a>CFDI SF pateikimas

Po to, kai įjungiate funkciją **Konfigūruojamas elektroninių SF išrašymo priedo integravimas**, proceso **Elektroninės SF eksportavimas / importavimas** (**Gautinos sumos \> SF \> El. SF**), skirto CFDI SF pateikti, nebegalima naudoti. Jis pakeičiamas nauju procesu pavadinimu **Pateikti elektroninius dokumentus**.

> [!NOTE]
> Prieš pradėdami naudoti naują procesą **Pateikti elektroninius dokumentus**, įsitikinkite, kad atliktas reikiamas Meksikos el. SF nustatymas. Daugiau informacijos žr. [CFDI 3.3 maketo versija](./latam-mex-cfdi-3-3.md).

1. Eikite į **Organizacijos administravimas \> Laikotarpio \> Elektroniniai dokumentai \> Pateikti elektroninius dokumentus**.
2. Pirmą kartą pateikę bet kokį dokumentą, visada nustatykite parinktį **Iš naujo pateikti dokumentus** į **Ne**. Jei turite iš naujo pateikti dokumentą naudodami paslaugą, nustatykite šią parinktį į **Taip**.
3. „FastTab” **Įtrauktini įrašai** pasirinkite **Filtruoti**, kad būtų atidarytas dialogo langas **Užklausa**, kuriame galite kurti užklausą, norėdami pasirinkti dokumentus pateikimui.

![CFDI dokumento pateikimas.](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> Pirmą kartą bandant pateikti dokumentą naudojant paslaugą, būsite paraginti patvirtinti ryšį su elektroninių SF išrašymo priedu. Pasirinkite **Spustelėkite čia, kad prisijungtumėte prie elektroninių dokumentų pateikimo paslaugos**.

### <a name="view-submission-logs"></a>Pateikimo žurnalų peržiūra

Galite peržiūrėti visų pateiktų dokumentų arba tik vieno pateikto dokumento pateikimo žurnalus.

#### <a name="view-all-submission-logs"></a>Visų pateikimo žurnalų peržiūra

Įjungus funkciją **Konfigūruojamas elektroninių SF išrašymo priedo integravimas**, galima naudoti naują puslapį, leidžiantį sekti dokumento pateikimo procesą. Galite naudoti šį puslapį norėdami peržiūrėti visų pateiktų dokumentų pateikimo žurnalus.

1. Eikite į **Organizacijos administravimas \> Laikotarpio \> Elektroniniai dokumentai \> Elektroninio dokumento pateikimo žurnalas**.
2. Lauke **Dokumento tipas** pasirinkite **Kliento SF žurnalas**, norėdami filtruoti pagal reikiamus elektroninius dokumentus.

    ![Dokumento tipo pasirinkimas norint peržiūrėti pateikimo žurnalus.](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. Norėdami peržiūrėti išsamią pateikimo vykdymo žurnalų informaciją, veiksmų srityje pasirinkite **Užklausos \> Pateikimo informacija**.

    ![Pateikimo žurnalo informacijos peržiūra.](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

Pateikimo žurnalų informacija suskirstyta į tris toliau pateiktus „FastTab”.

- **Apdorojimo veiksmai** – šis „FastTab” nurodo veiksmų, sukonfigūruotų funkcijos versijoje, nustatytoje RCS, vykdymo žurnalą. Stulpelyje **Būsena** nurodoma, ar veiksmas sėkmingai įvykdytas.
- **Veiksmų failai** – šis „FastTab” nurodo tarpinius failus, sugeneruotus veiksmų vykdymo metu. Galite pasirinkti **Peržiūrėti**, norėdami atsisiųsti failą ir jį peržiūrėti.
- **Apdorojimo veiksmų žurnalas** – šis „FastTab” nurodo ryšio tarp elektroninių SF išrašymo priedo ir tikslinės žiniatinklio tarnybos rezultatus. Taip pat rodoma, ką pateikė žiniatinklio tarnybos apdorojimas. Stulpelyje **Klaidos kodas** rodomas grąžinimo kodas, kurį pateikė autorizavimo žiniatinklio tarnyba.

Kai pateikta CFDI SF patvirtinama, jos būsena atnaujinama į **Patvirtinta**.

#### <a name="view-submission-logs-from-cfdi-invoices"></a>Pateikimo žurnalų peržiūra iš CFDI SF

Įjungę funkciją **Konfigūruojamas elektroninių SF išrašymo priedo integravimas**, taip pat galite peržiūrėti pateikimo žurnalus iš CFDI SF.

1. Eikite į **Gautinos sumos \> Užklausos ir ataskaitos \> CFDI (elektroninės SF)**.
2. Pasirinkite CFDI SF, kuri buvo pateikta po to, kai buvo įjungta funkcija **Konfigūruojamas elektroninių SF išrašymo priedo integravimas**.
3. Veiksmų srities skirtuke **Retrospektyva** pasirinkite **Elektroninio dokumento žurnalas**.

![Pateikimo žurnalų peržiūra iš CFDI SF.](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> Mygtukas **Retrospektyva** pasiekiamas CFDI SF, kurios buvo pateiktos prieš funkcijos **Konfigūruojamas elektroninių SF išrašymo priedo integravimas** įjungimą. Mygtukas **Retrospektyva** nėra pasiekiamas CFDI SF, pateiktoms po funkcijos **Konfigūruojamas elektroninių SF išrašymo priedo integravimas** įjungimo.

### <a name="submit-cancellation-of-cfdi-invoices"></a>CFDI SF atšaukimo pateikimas

Įjungus funkciją **Konfigūruojamas elektroninių SF išrašymo priedo integravimas**, nebegalima naudoti senojo CFDI SF atšaukimo proceso. Jis pakeičiamas nauju atšaukimo procesu, kuris įdėtas puslapyje **Elektroninių dokumentų pateikimo žurnalas**.

1. Eikite į **Gautinos sumos \> Užklausos ir ataskaitos \> CFDI (elektroninės SF)**.
2. Jei CFDI SF būsena yra **Patvirtinta**, pasirinkite **Funkcijos \> Atšaukti CFDI**.
3. Eikite į **Organizacijos administravimas \> Laikotarpio \> Elektroniniai dokumentai \> Elektroninio dokumento pateikimo žurnalas**.
4. Pasirinkite CFDI SF, tada pasirinkite **Funkcijos \> Siųsti susijusius pateikimus**.
5. Įveskite susijusio pateikimo aprašą ir pasirinkite **Gerai**.

#### <a name="view-cancellation-submission-logs"></a>Atšaukimo pateikimo žurnalų peržiūra

1. Eikite į **Organizacijos administravimas \> Laikotarpio \> Elektroniniai dokumentai \> Elektroninio dokumento pateikimo žurnalas**.
2. Lauke **Dokumento tipas** pasirinkite **Kliento SF žurnalas**, norėdami filtruoti tik pagal kliento SF žurnalo dokumentus.
3. Pasirinkite CFDI SF, tada veiksmų srityje pasirinkite **Užklausos \> Susijęs pateikimas**.

    Puslapyje **Susiję pateikimai** rodomi visi susiję pateikimai ir konkrečių CFDI SF pateikimo būsenos. Toliau pateiktoje iliustracijoje pirmoji eilutė nurodo pateikimą, kuris pateikė CFDI SF patvirtinimo užklausą. Antroji eilutė nurodo pateikimą, atšaukusį CFDI SF.

    ![Atšaukimo pateikimo žurnalų peržiūra.](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. Norėdami peržiūrėti išsamią pateikimo vykdymo žurnalų informaciją, veiksmų srityje pasirinkite **Užklausos \> Pateikimo informacija**.

    ![Atšaukimo pateikimo žurnalų informacijos peržiūra.](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a>Privatumo pranešimas
Norint įjungti funkciją **CFDI Meksikos elektroninė SF (MX)** gali prireikti siųsti ribotus duomenis, kurie apima įmonės mokesčių registravimo ID. Jie bus persiųsti mokesčių inspekcijos patvirtintoms trečiųjų šalių agentūroms, kad būtų galima siųsti elektronines SF šiai mokesčių inspekcijai iš anksto nustatytu formatu, reikalingu integravimui su vyriausybės žiniatinklio tarnyba. Administratorius gali įjungti ir išjungti funkciją **CFDI Meksikos elektroninė SF (MX)**, nuėjęs į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**. Skirtuke **Funkcijos** pasirinkite eilutes, kuriose yra funkcija **CFDI Meksikos elektroninė SF (MX)**, ir tinkamai pasirinkite. Duomenims, importuotiems iš šių išorinių sistemų į šią „Dynamics 365” internetinę paslaugą, taikomos [privatumo nuostatos](https://go.microsoft.com/fwlink/?LinkId=512132). Daugiau informacijos ieškokite skyriuose Privatumo pranešimas, esančiuose konkrečios šalies funkcijos dokumentacijoje.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių SF išrašymo priedo apžvalga](e-invoicing-service-overview.md)
- [Darbo su elektroninių SF priedu pradžia](e-invoicing-get-started.md)
- [Elektroninių SF nustatymas](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
