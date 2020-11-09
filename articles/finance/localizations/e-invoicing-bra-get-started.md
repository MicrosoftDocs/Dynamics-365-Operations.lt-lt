---
title: Darbo su Brazilijos elektroninių SF išrašymo priedu pradžia
description: Šioje temoje pateikiama informacija, kuri padės jums pradėti naudotis Brazilijos elektroninių SF išrašymo priedu „Microsoft Dynamics 365 Finance” ir „Dynamics 365 Supply Chain Management”.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: fb3ec2d60875d7a0747d64b397aafaa0a3d26348
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039874"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>Darbo su Brazilijos elektroninių SF išrašymo priedu pradžia 

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> Brazilijos elektroninių SF išrašymo priedas šiuo metu nepalaiko visų funkcijų, pasiekiamų finansinio dokumento integravime, įtaisytame „Microsoft Dynamics 365 Finance” ir „Dynamics 365 Supply Chain Management”.

Šioje temoje pateikiama informacija, kuri padės jums pradėti naudotis Brazilijos elektroninių SF išrašymo priedu. Ji padės atlikti konfigūracijos veiksmus, priklausančius nuo šalies, programose „Regulatory Configuration Services” (RCS) ir „Finance” bei „Supply Chain Management”. Ji taip pat paaiškina, kaip pateikti NF-e finansinį dokumentą (elektroninio finansinio dokumento 55 modelis) naudojant paslaugą, ir kaip peržiūrėti apdorojimo rezultatus ir finansinių dokumentų būsenas.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš atlikdami šioje temoje nurodytus veiksmus, turite atlikti veiksmus, esančius [Darbo su elektroninių SF išrašymo priedu pradžia](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>RCS sąranka

RCS nustatymo metu galėsite atlikti toliau pateiktas užduotis.

1. Importuoti el. SF išrašymo funkciją, skirtą NF-e finansiniams dokumentams.
2. Peržiūrėti failų formatus, kurių reikia norint pateikti NF-e finansinius dokumentus autorizuoti.
3. Peržiūrėti failų formatus, kurių reikia norint prašyti atšaukti patvirtintą NF-e.
4. Konfigūruoti įvykį, kurio reikia norint pateikti NF-e finansinius dokumentus autorizuoti.
5. Konfigūruoti įvykį, kurio reikia norint prašyti atšaukti patvirtintą NF-e.
6. Priskirti el. SF išrašymo funkciją elektroninių SF išrašymo priedo aplinkai.
7. Publikuoti el. SF išrašymo funkciją.

> [!NOTE]
> „El. SF išrašymo funkcija” yra bendras išteklių, sukonfigūruotų ir publikuotų siekiant naudoti elektroninių SF išrašymo priedo serverį, pavadinimas. El. SF išrašymo funkcijos nustatymas be viso kito apima elektroninių ataskaitų (ER) konfigūracijos formatų naudojimą konfigūruojamiems eksportavimo ir importavimo failams kurti ir veiksmų bei veiksmų srautų naudojimą konfigūruojamų taisyklių kūrimui įgalinti, kad būtų galima siųsti užklausas, importuoti atsakymus ir analizuoti atsakymo turinį.

## <a name="import-the-e-invoicing-feature"></a>El. SF išrašymo funkcijos importavimas

1. Prisijunkite prie jūsų RCS abonemento
2. Darbo srities **Globalizacijos funkcijos** dalyje **Funkcijos** pasirinkite plytelę **El. SF išrašymas**.
3. Puslapyje **El. SF išrašymo funkcijos** pasirinkite **Importuoti** , norėdami importuoti NF-e finansinio dokumento el. SF išrašymo funkciją iš visuotinės saugyklos.

    ![Mygtukas Importuoti](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. Pasirinkite funkciją NF-e finansinis dokumentas ir pasirinkite **Importuoti**.

    ![NF-e funkcijos importavimas](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a>Naujos funkcijos NF-e finansinis dokumentas versijos kūrimas

- Puslapio **El. SF išrašymo funkcijos** skirtuke **Versijos** pasirinkite **Naujas**.

![Naujos el. SF išrašymo funkcijos versijos įtraukimas](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a>Konfigūracijos versijos naujinimas

1. Puslapio **El. SF išrašymo funkcijos** skirtuke **Konfigūracijos** pasirinkite **Įtraukti** arba **Naikinti** , norėdami valdyti konfigūracijos versijas (ER failo formato konfigūracijas).

    ![El. SF išrašymo funkcijos konfigūracijų valdymas](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - Kai kuriate naują funkcijos NF-e finansinis dokumentas versiją, visos konfigūracijos versijos (ER failų formatai) perduodamos iš naujausios versijos.
    - Norėdami pateikti NF-e finansinį dokumentą autorizavimui, būtinos toliau pateiktos konfigūracijos versijos.

        - NFe pateikimo eksportavimo formatas
        - NFe atsakymo pranešimo importavimas
        - NFe klaidų žurnalo importavimas

    - Norėdami pateikti NF-e atšaukimą, būtina toliau pateikta konfigūracijos versija.

        - NFe atšaukimo eksportavimo formatas

2. Sąraše pasirinkite konfigūracijos versiją, tada pasirinkite **Redaguoti** arba **Peržiūrėti** , kad būtų atidarytas puslapis **Formato dizaino įrankis** , kuriame galite redaguoti arba peržiūrėti konfigūraciją.

    ![Puslapio Formato dizaino įrankis atidarymas](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. Norėdami redaguoti arba peržiūrėti ER formato failo konfigūracijas, naudokite puslapį **Formato dizaino įrankis**. Daugiau informacijos žr. [Elektroninių dokumentų konfigūracijų kūrimas](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).

    ![Formato dizaino įrankio puslapis](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a>El. SF išrašymo funkcijos nustatymų valdymas

- Puslapio **El. SF išrašymo funkcijos** skirtuke **Nustatymai** pasirinkite **Įtraukti** arba **Naikinti** , norėdami valdyti el. SF išrašymo funkcijos nustatymus (t. y., NF-e įvykius).

![El. SF išrašymo funkcijos nustatymų valdymas](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

Kai sukuriate naują funkcijos NF-e finansinis dokumentas, kuri išvedama iš kitos el. SF išrašymo funkcijos, versiją, visi funkcijos nustatymai (NF-e įvykiai) perduodami iš naujausios versijos.

Norint pateikti NF-e finansinius dokumentus autorizuoti, reikalingas funkcijos **Pateikti** nustatymas.

Norint pateikti NF-e atšaukimą, reikalingas funkcijos **Atšaukimas** nustatymas.

#### <a name="configure-the-submit-feature-setup"></a>Funkcijos Pateikti nustatymo konfigūravimas

1. Puslapio **El. SF išrašymo funkcijos** skirtuko **Nustatymai** stulpelyje **Funkcijos nustatymas** pasirinkite **Pateikti**.
2. Pasirinkite **Redaguoti**.

    ![El. SF išrašymo funkcijos nustatymo redagavimas](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. Puslapyje **Funkcijos versijos nustatymas** pasirinkite skirtuką **Veiksmai** , norėdami valdyti veiksmų sąrašą.

    ![Skirtukas Veiksmai](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. Peržiūrėkite veiksmus, kurių reikia norint pateikti NF-e autorizuoti.

    | Veiksmo ID | Veiksmo pavadinimas                  | Veiksmo aprašas                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | 1         | Pakeisti dokumentą           | Sukurkite NF-e XML failą pateikimui.                          |
    | 2         | Pasirašyti dokumentą                | Pritaikykite skaitmeninį sertifikatą XML failui.                    |
    | 3         | Iškviesti Brazilijos SEFAZ tarnybą | Pateikite pasirašytą XML failą žiniatinklio tarnyboms autorizuoti. |
    | 4         | Apdoroti atsakymą             | Gaukite žiniatinklio tarnybos atsakymą.                                     |
    | 5         | Pakeisti dokumentą           | Analizuokite failo, kuris gaunamas kaip atsakymas, turinį.     |
    | 6         | Pakeisti dokumentą           | Sukurkite XML failą, norėdami pateikti užklausą dėl pateikimo būsenos.    |
    | 7         | Iškviesti Brazilijos SEFAZ tarnybą | Pateikite XML failą, pateikiantį užklausą dėl pateikimo būsenos.          |
    | 8         | Apdoroti atsakymą             | Gaukite žiniatinklio tarnybos atsakymą.                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>SEFAZ žiniatinklio tarnybų URL nustatymas 

1. Puslapio **Funkcijos versijos nustatymas** skirtuko **Veiksmai** „FastTab” **Veiksmai** pasirinkite **Iškviesti Brazilijos SEFAZ tarnybą** ( **3** veiksmo ID).
2. „FastTab” **Parametrai** lauke **URL adreso parametras** įveskite NF-e pateikimo SEFAZ žiniatinklio tarnybos URL.
3. „FastTab” **Veiksmai** pasirinkite **Iškviesti Brazilijos SEFAZ tarnybą** ( **7** veiksmo ID).
4. „FastTab” **Parametrai** lauke **URL adreso parametras** įveskite NF-e pateikimo SEFAZ žiniatinklio tarnybos URL.

#### <a name="configure-the-cancellation-feature-setup"></a>Funkcijos Atšaukimas nustatymo konfigūravimas

1. Puslapio **El. SF išrašymo funkcijos** skirtuko **Nustatymai** stulpelyje **Funkcijos nustatymas** pasirinkite **Atšaukimas**.
2. Pasirinkite **Redaguoti**.
3. Puslapyje **Funkcijos versijos nustatymas** pasirinkite skirtuką **Veiksmai** , norėdami valdyti veiksmų sąrašą.
4. Peržiūrėkite veiksmus, kurių reikia norint prašyti atšaukti patvirtintą NF-e.

    | Veiksmo ID | Veiksmo pavadinimas                  | Veiksmo aprašas                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | 1         | Pakeisti dokumentą           | Sukurkite NF-e atšaukimo XML failą pateikimui.            |
    | 2         | Pasirašyti dokumentą                | Pritaikykite skaitmeninį sertifikatą XML failui.                   |
    | 3         | Iškviesti Brazilijos SEFAZ tarnybą | Pateikite pasirašytą XML failą žiniatinklio tarnyboms atšaukti. |
    | 4         | Apdoroti atsakymą             | Gaukite žiniatinklio tarnybos atsakymą.                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>SEFAZ žiniatinklio tarnybų URL nustatymas

1. Puslapio **Funkcijos versijos nustatymas** skirtuko **Veiksmai** „FastTab” **Veiksmai** pasirinkite **Iškviesti Brazilijos SEFAZ tarnybą** ( **3** veiksmo ID).
2. „FastTab” **Parametrai** lauke **URL adreso parametras** įveskite patvirtintos NF-e atšaukimo SEFAZ žiniatinklio tarnybos URL.

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a>El. SF išrašymo aplinkos įgalinimas ir juodraščio versijos priskyrimas

1. Puslapio **El. SF išrašymo funkcijos** skirtuke **Aplinkos** pasirinkite **Įjungti**.
2. Lauke **Aplinka** pasirinkite aplinką.
3. Lauke **Galioja nuo** pasirinkite datą, kada aplinka turėtų įsigalioti.
4. Pasirinkite **Įjungti**.

![El. SF išrašymo aplinkos įgalinimas](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a>Būsenos keitimas į Baigta

1. Puslapio **El. SF išrašymo funkcijos** skirtuke **Versijos** pasirinkite el. SF išrašymo funkcijos versiją, kurios būsena yra **Juodraštis**.
2. Pasirinkite **Keisti būseną \> Baigta**.

### <a name="change-the-status-to-publish"></a>Būsenos keitimas į Publikuoti

1. Puslapio **El. SF išrašymo funkcijos** skirtuke **Versijos** pasirinkite el. SF išrašymo funkcijos versiją, kurios būsena yra **Baigta**.
2. Pasirinkite **Keisti būseną \> Publikuoti**.

![El. SF išrašymo funkcijos publikavimas](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Elektroninių SF išrašymo priedo integravimo nustatymas „Finance” arba „Supply Chain Management”

Nustatymo metu galėsite atlikti toliau pateiktas užduotis.

1. Įjungti Brazilijos „NF-e Federal” funkciją.
2. Importuoti konkretų ER duomenų modelį, duomenų modelio susiejimą ir formatus, reikalingus NF-e finansiniams dokumentams.
3. Importuoti ER konfigūraciją ir nustatyti atsakymų tipus, kurių reikia norint atnaujinti finansinio dokumento būseną po pateikimo proceso grąžinimo.

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a>Brazilijos „NF-e Federal” funkcijos įjungimas

1. Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.
2. Skirtuke **Funkcijos** pažymėkite žymės langelį **Įjungti** eilutėje, skirtoje funkcijos nuorodai **BR00053**.

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a>ER duomenų modelio susiejimo, skirto NF-e finansiniams dokumentams, importavimas

1. Prisijunkite prie „Finance“.
2. Darbo srities **Elektroninės ataskaitos** dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **„Microsoft”**. Įsitikinkite, kad šis konfigūracijos teikėjas nustatytas kaip **Aktyvus**. Daugiau informacijos apie tai, kaip nustatyti teikėją į **Aktyvus** , žr. [Konfigūracijų teikėjų kūrimas ir jų pažymėjimas kaip aktyviais](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Pasirinkite **Saugyklos**.
4. Pasirinkite **Visuotiniai ištekliai \> Atidaryti**.
5. Importuokite **finansinių dokumentų susiejimo** konfigūracijas.

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a>ER konfigūracijų importavimas ir finansinių dokumentų atsakymų tipų nustatymas

1. Darbo srities **Elektroninės ataskaitos** dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **„Microsoft”**.
2. Pasirinkite **Saugyklos**.
3. Pasirinkite **Visuotiniai ištekliai \> Atidaryti**.
4. Importuokite **NF-e klaidos žurnalo importavimas (BR)** , **NF-e atsakymo duomenų importavimo formatas (BR)** ir **NF-e atsakymo pranešimo importavimas (BR)**.
5. Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.
6. Skirtuke **Elektroninis dokumentas** pasirinkite **Įtraukti**.
6. Lauke **Lentelės pavadinimas** įveskite **Finansinio dokumento antraštė**.
7. Lauke **Dokumento kontekstas** pasirinkite **Kliento SF konteksto modelis – finansinio dokumento kontekstas**.
8. Pasirinkti **Atsakymų tipai**.
9. Pasirinkite **Naujas** , tada lauke **Atsakymo tipas** pasirinkite **Atsakymas**.
10. Lauke **Pateikimo būsena** pasirinkite **Laukiama**.
11. Lauke **Modelio susiejimas** pasirinkite **Atsakymo pranešimo importavimo formatas – modelio susiejimas iš atsakymo pranešimo**.
12. Pasirinkite **Įrašyti**.
13. Pasirinkite **Naujas** , tada lauke **Atsakymo tipas** įveskite **Atsakymo duomenys**.
14. Lauke **Pateikimo būsena** pasirinkite **Laukiama**.
15. Lauke **Modelio susiejimas** pasirinkite **NFe atsakymo duomenų importavimo formatas – atsakymo duomenų importavimas**.
16. Pasirinkite **Įrašyti**.

## <a name="electronic-invoice-processing"></a>El. SF apdorojimas

Apdorojimo „Finance” metu atliksite toliau pateiktas užduotis.

1. Pateikti finansinį dokumentą naudodami elektroninių SF išrašymo priedą.
2. Peržiūrėti pateikimo vykdymo žurnalus ir apdorojimo rezultatus.
3. Pateikti finansinio dokumento atšaukimą naudodami elektroninių SF išrašymo priedą.

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a>NF-e finansinių dokumentų pateikimas SEFAZ autorizavimui 

Po to, kai įjungiate funkciją **Konfigūruojamas elektroninių SF išrašymo priedo integravimas** , seno proceso, skirto NF-e finansiniams dokumentams pateikti autorizuoti ( **NF-e proceso eksportavimas / importavimas** ), nebegalima naudoti. Jis pakeičiamas nauju procesu pavadinimu **Pateikti elektroninius dokumentus**.

> [!NOTE]
> Prieš tęsdami įsitikinkite, kad turite vieną ar daugiau kliento 55 modelio finansinių dokumentų, kuriuos išdavė kliento finansinis padalinys. Šių finansinių dokumentų kryptis turi būti nustatyta į **Siunčiama** , o būsena turi būti **Sukurta**. Daugiau informacijos žr. [Kliento finansinio dokumento išdavimas (Brazilija)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).

1. Eikite į **Organizacijos administravimas \> Laikotarpio \> Elektroniniai dokumentai \> Pateikti elektroninius dokumentus**.
2. Pirmą kartą pateikę bet kokį dokumentą, visada nustatykite parinktį **Iš naujo pateikti dokumentus** į **Ne**. Jei turite iš naujo pateikti dokumentą naudodami paslaugą, nustatykite šią parinktį į **Taip**.
3. „FastTab” **Įtrauktini įrašai** pasirinkite **Filtruoti** , kad būtų atidarytas dialogo langas **Užklausa** , kuriame galite kurti užklausą, norėdami pasirinkti dokumentus pateikimui.
4. Skirtuke **Diapazonas** pasirinkite **Įtraukti**.
5. Lauke **Lentelė** pasirinkite **Finansinio dokumento antraštė**.
6. Lauke **Išvestinė lentelė** pasirinkite **Finansinio dokumento antraštė**.
6. Lauke **Laukas** pasirinkite **Numeris**.
7. Lauke **Kriterijai** įveskite finansinio dokumento, kuris turi būti pateiktas, numerį.
8. Pasirinkite **Gerai** , kad uždarytumėte dialogo langą **Užklausa**.
8. Pasirinkti **Gerai** , norėdami pateikti pasirinktus dokumentus.

> [!NOTE]
> Pirmą kartą bandant pateikti dokumentą naudojant paslaugą, būsite paraginti patvirtinti ryšį su elektroninių SF išrašymo priedu. Pasirinkite **Spustelėkite čia, kad prisijungtumėte prie elektroninių dokumentų pateikimo paslaugos**.

### <a name="view-all-submission-logs"></a>Visų pateikimo žurnalų peržiūra

Įjungus funkciją **Konfigūruojamas elektroninių SF išrašymo priedo integravimas** , galima naudoti naują puslapį, leidžiantį sekti dokumento pateikimo procesą. Galite naudoti šį puslapį norėdami peržiūrėti visų pateiktų dokumentų pateikimo žurnalus.

1. Eikite į **Organizacijos administravimas \> Laikotarpio \> Elektroniniai dokumentai \> Elektroninio dokumento pateikimo žurnalas**.
2. Lauke **Dokumento tipas** pasirinkite **Finansinio dokumento antraštė** , norėdami filtruoti tik pagal finansinius dokumentus.
3. Norėdami peržiūrėti išsamią pateikimo vykdymo žurnalų informaciją, veiksmų srityje pasirinkite **Užklausos \> Pateikimo informacija**.

![Pateikimo žurnalo informacijos peržiūra](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> Apdorojant NF-e finansinius dokumentus, stulpelyje **Klaidos kodas** rodomas grąžinimo kodas, kurį pateikė SEFAZ žiniatinklio tarnybos.

### <a name="view-submission-logs-through-the-fiscal-document-page"></a>Pateikimo žurnalų peržiūra naudojant finansinio dokumento puslapį

Įjungę funkciją **Konfigūruojamas elektroninių SF išrašymo priedo integravimas** , taip pat galite peržiūrėti pateikimo žurnalus naudodami finansinio dokumento puslapį.

1. Eikite į **Didžioji knyga \> Užklausos ir ataskaitos \> Finansiniai dokumentai \> Visi finansiniai dokumentai**.
2. Pasirinkite finansinį dokumentą, kuris buvo pateiktas anksčiau naudojant elektroninių SF išrašymo priedą.
3. Veiksmų srities skirtuke **„NF-e Federal”** pasirinkite **Elektroninio dokumento žurnalas**.

![Pateikimo žurnalų peržiūra iš finansinio dokumento puslapio](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a>Patvirtintų NF-e finansinių dokumentų pateikimas SEFAZ atšaukimui

Įjungus funkciją **Konfigūruojamas elektroninių SF išrašymo priedo integravimas** , nebegalima naudoti senojo NF-e finansinių dokumentų atšaukimo proceso. Jis pakeičiamas nauju atšaukimo procesu, kuris įdėtas puslapyje **Elektroninių dokumentų pateikimo žurnalas**.

> [!NOTE]
> Įsitikinkite, kad įvykdėte patvirtinto NF-e finansinio dokumento kliento finansinio dokumento atšaukimą. Daugiau informacijos žr. [Kliento finansinio dokumento atšaukimas (Brazilija)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).

1. Eikite į **Organizacijos administravimas \> Laikotarpio \> Elektroniniai dokumentai \> Elektroninio dokumento pateikimo žurnalas**.
2. Pasirinkite finansinį dokumentą, tada pasirinkite **Funkcijos \> Siųsti susijusius pateikimus**.
3. Įveskite susijusio pateikimo aprašą ir pasirinkite **Gerai**.

### <a name="view-cancellation-submission-logs"></a>Atšaukimo pateikimo žurnalų peržiūra

1. Eikite į **Organizacijos administravimas \> Laikotarpio \> Elektroniniai dokumentai \> Elektroninio dokumento pateikimo žurnalas**.
2. Lauke **Dokumento tipas** pasirinkite **Finansinio dokumento antraštė** , norėdami filtruoti tik pagal finansinius dokumentus.
3. Pasirinkite finansinį dokumentą, tada veiksmų srityje pasirinkite **Užklausos \> Susijęs pateikimas**.

    Susiję pateikimai yra pateikimai, kurie susiję su pagrindiniu pateikimu, atliktu pirmiausia. Pavyzdžiui, pateikimas, kuris įgalioja konkrečią NF-e, yra pagrindinis pateikimas. Pateikimas, kuris pateikia užklausą atšaukti tą pačią NF-e SEFAZ, yra susijęs pateikimas. Jis egzistuoja tik todėl, kad pateikia užklausą atšaukti užduotį, atliktą naudojant kitą pateikimą.

    Puslapyje **Susiję pateikimai** rodomi visi susiję pateikimai ir konkrečių finansinių dokumentų pateikimo būsenos. Toliau pateiktoje iliustracijoje pirmoji eilutė nurodo pateikimą, kuris pateikė finansinio dokumento patvirtinimo užklausą. Antroji eilutė nurodo pateikimą, atšaukusį finansinį dokumentą.

    ![Atšaukimo pateikimo žurnalų peržiūra](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. Norėdami peržiūrėti išsamią pateikimo vykdymo žurnalų informaciją, veiksmų srityje pasirinkite **Užklausos \> Pateikimo informacija**.

    ![Atšaukimo pateikimo žurnalų informacijos peržiūra](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a>Privatumo pranešimas
Įgalinant funkciją BR-00053 („NF-e Federal”) gali reikėti siųsti ribotus duomenis, įskaitant organizacijos mokesčių registracijos ID. Jie bus persiųsti mokesčių inspekcijos patvirtintoms trečiųjų šalių agentūroms, kad būtų galima siųsti elektronines SF šiai mokesčių inspekcijai iš anksto nustatytu formatu, reikalingu integravimui su vyriausybės žiniatinklio tarnyba. Administratorius gali įjungti ir išjungti funkciją BR-00053 („NF-e Federal”), nuėjęs į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**. Pasirinkite skirtuką **Funkcijos** , pasirinkite eilutę, kurioje yra funkcija BR-00053, tada atlikite reikiamą žymėjimą. Duomenims, importuotiems iš šių išorinių sistemų į šią „Dynamics 365” internetinę paslaugą, taikomos [privatumo nuostatos](https://go.microsoft.com/fwlink/?LinkId=512132). Daugiau informacijos ieškokite skyriuose Privatumo pranešimas, esančiuose konkrečios šalies funkcijos dokumentacijoje.


## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių SF išrašymo priedo apžvalga](e-invoicing-service-overview.md)
- [Darbo su elektroninių SF išrašymo priedu pradžia](e-invoicing-get-started.md)
- [Elektroninių SF išrašymo priedo nustatymas](e-invoicing-setup.md)
