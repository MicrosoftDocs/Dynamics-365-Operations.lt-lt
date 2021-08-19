---
title: ER formato kūrimas, kad būtų galima sugeneruoti „Excel” formato ataskaitą su į puslapių antraštes ar poraštes įdėtais vaizdais
description: Šioje temoje paaiškinama, kaip naudoti elektronines ataskaitas (ER)) generuoti verslo dokumentams, kuriuose yra paveikslėlių ir figūrų, įdėtų į puslapių antraštes ar poraštes.
author: NickSelin
ms.date: 06/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 1115be8c33eeaf16c1a533e63b31d87b0fc5f68d6469ff075428f72ac146b2f4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746640"
---
# <a name="design-an-er-format-to-generate-a-report-in-excel-format-with-embedded-images-in-page-headers-or-footers"></a>ER formato kūrimas, kad būtų galima sugeneruoti „Excel” formato ataskaitą su į puslapių antraštes ar poraštes įdėtais vaizdais

[!include[banner](../includes/banner.md)]

Ši tema paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų funkcinio konsultanto vaidmens vartotojas gali atlikti šias užduotis:

- Konfigūruoti [Elektroninių ataskaitų (ER)](general-electronic-reporting.md) sistemos parametrus.
- Importuokite ER [konfigūracijas](general-electronic-reporting.md#Configuration), kurias [teikia](general-electronic-reporting.md#Provider) „Microsoft” ir, kurios naudojamos generuoti [laisvos formos sąskaitoms faktūroms](../../../finance/accounts-receivable/create-free-text-invoice-new.md), paremtoms [šablonu](er-fillable-excel.md#excel-file-component), pateiktu „Microsoft Excel” formatu.
- Sukurti standartinės „Microsoft” teikiamos ER formato konfigūracijos [pasirinktinę (išvestinę)](general-electronic-reporting.md#building-a-format-selecting-another-format-as-a-base-customization) versiją.
- Modifikuoti pasirinktinę ER formato konfigūraciją taip, kad ji sugeneruotų laisvos formos sąskaitos faktūros ataskaitą, kurios poraštėje būtų įmonės logotipo vaizdas.

Šios temos procedūros gali būti atliktos naudojant **„USMF”** įmonę. Kodavimas nebūtinas. Prieš pradėdami, atsisiųskite ir įrašykite toliau pateiktą failą.

| Aprašas        | Failo vardas |
|--------------------|-----------|
| Įmonės logotipo vaizdas | [Įmonės logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png) |

## <a name="content"></a>Turinys

- [Juridinio asmens konfigūravimas](#ConfigureLegalEntity)
- [ER sistemos konfigūracija](#ConfigureFramework)

    - [ER parametrų konfigūravimas](#ConfigureParameters)
    - [Aktyvuokite ER konfigūracijos tiekėją](#ActivateProvider)

        - [Peržiūrėkite ER konfigūracijos teikėjų sąrašą](#ReviewProvidersList)
        - [Pridėkite naują ER konfigūracijos tiekėją](#AddProvider)
        - [Aktyvuokite naują ER konfigūracijos tiekėją](#ActivateAddedProvider)

- [Importuokite standartinio ER formato konfigūracijas](#ImportERSolution1)

    - [Importuokite standartinio ER formato konfigūracijas](#ImportERFormat)
    - [Peržiūrėkite importuotas ER konfigūracijas](#ReviewImportedERSolution)

- [Spausdinti laisvos formos sąskaitą faktūrą naudojant standartinį ER formatą](#PrintInvoice1)

    - [Nustatyti spausdinimo valdymą](#ConfigurePrintManagement1)
    - [Spausdinti laisvos formos SF](#ProcessInvoice1)

- [Pritaikykite standartinį ER formatą](#CustomizeProvidedFormat)

    - [Sukurkite pritaikytą formatą](#DeriveProvidedFormat)
    - [Pasirinktinio formato redagavimas](#ConfigureDerivedFormat)
    - [Pažymėkite tinkintą formatą kaip leistiną](#MarkFormatRunnable)

- [Spausdinti laisvos formos sąskaitą faktūrą naudojant tinkintą ER formatą](#PrintInvoice2)

    - [Nustatyti spausdinimo valdymą](#ConfigurePrintManagement2)
    - [Spausdinti laisvos formos SF](#ProcessInvoice2)

- [Papildomi ištekliai](#References)

## <a name="configure-the-legal-entity"></a><a id="ConfigureLegalEntity"></a>Juridinio asmens konfigūravimas

1. Eikite į **Organizacijos administravimas** \> **Organizacijos** \> **Juridiniai subjektai**.
2. Puslapio **Juridiniai subjektai** „FastTab” **Įmonės logotipo vaizdo ataskaita** pasirinkite **Keisti**.
3. Dialogo lange **Pasirinkti vaizdo failą, kurį norite įkelti** pasirinkite **Naršyti** ir failą **„Company logo.png”**, kurį atsisiuntėte anksčiau.
4. Pasirinkite **Įrašyti** ir uždarykite puslapį **Juridiniai subjektai**.

![Įmonės logotipo vaizdas, pasirinktas Juridinių subjektų puslapyje.](./media/er-embed-images-header-footer-excel-reports-company-logo-image.png)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a>ER sistemos konfigūracija

Kaip elektroninių ataskaitų funkcinio konsultanto vartotojas, turite sukonfigūruoti minimalų ER parametrų rinkinį, kad galėtumėte naudoti ER sistemą standartinio ER formato pasirinktinės versijos kūrimui.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>ER parametrų konfigūravimas

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** pasirinkite **Elektroninių ataskaitų parametrai**.
3. **Elektroninių ataskaitų parametrai** puslapyje **Bendra** skirtuke nustatykite **Įjungti dizaino režimą** parinktį į **Taip**.
4. **Priedai** skirtuke nustatykite tolesnius parametrus:

    - **Konfigūracijos** lauke pasirinkite **Failas** tipą, skirtą **USMF** įmonei.
    - **Užduoties archyvas**, **Laikini**, **Bazinė linija** ir **Kiti** laukuose pasirinkite **Failas** tipą.

Norėdami sužinoti daugiau apie ER parametrus, žr. [ER sistemos konfigūracija](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>ER konfigūracijos tiekėjo aktyvavimas

Kiekviena pridėta ER konfigūracija pažymėta kaip priklausanti ER konfigūracijos teikėjui. ER konfigūracijos tiekėjas, kuris aktyvuojamas **Elektroninė ataskaita** darbo srityje naudojamas šiam tikslui. Todėl turite aktyvuoti ER konfigūracijos tiekėją **Elektroninė ataskaita** darbo srityje prieš pridėdami ar redaguodami ER konfigūracijas.

> [!NOTE]
> ER konfigūraciją gali redaguoti tik jos savininkas. Prieš redaguojant ER konfigūraciją atitinkamas ER konfigūracijos tiekėjas turi būti aktyvuotas **Elektroninė ataskaita** darbo srityje.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>ER konfigūracijos teikėjų sąrašo peržiūra

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** skyriuje pasirinkite **Konfigūracijos tiekėjai**.
3. **Konfigūracijos teikėjo lentelė** puslapyje kiekvienas teikėjo įrašas turi unikalų pavadinimą ir URL. Peržiūrėkite šio puslapio turinį. Jei įrašas, skirtas **Litware, Inc.** ( `https://www.litware.com`) jau yra, praleiskite sekančią procedūrą, [Pridėkite naują ER konfigūracijos teikėją](#AddProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Pridėkite naują ER konfigūracijos tiekėją

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** skyriuje pasirinkite **Konfigūracijos tiekėjai**.
3. **Konfigūracijos tiekėjai** puslapyje pasirinkite **Nauja**.
4. Lauke **Pavadinimas** įveskite **Litware, Inc.**
5. **Internetinis adresas** lauke įveskite `https://www.litware.com`.
6. Pasirinkite **Įrašyti**.

#### <a name="activate-the-new-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Aktyvuokite naują ER konfigūracijos tiekėją

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos teikėjai** dalyje pasirinkite **„Litware, Inc.”** plytelę ir pasirinkite **Nustatyti kaip aktyvų**.

Daugiau informacijos apie ER konfigūracijos tiekėjus žr. [Konfigūracijos teikėjų kūrimas pažymint juos kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Standartinio ER formato konfigūracijų importavimas

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat"></a>Standartinio ER konfigūracijų importavimas

Norėdami pridėti standartines ER konfigūracijas prie dabartinio „Dynamics 365 Finance” egzemplioriaus, importuokite jas iš ER [saugyklos](general-electronic-reporting.md#Repository), sukonfigūruotos tam programos egzemplioriui.

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapio **Konfigūracijos teikėjai** dalyje pasirinkite **„Microsoft”** plytelę, o tada pasirinkite **Saugyklos**, kad peržiūrėtumėte **„Microsoft”** tiekėjo saugyklų sąrašą.
3. Puslapyje **Konfigūracijų saugyklos** pasirinkite **Visuotinis** tipo saugyklą, paskui pasirinkite **Atidaryti**. Jei esate raginami autorizuoti, kad prisijungtumėte prie [„Regulatory Configuration Service”](../../../finance/localizations/rcs-overview.md), vadovaukitės autorizavimo instrukcijomis.
4. Puslapio **Konfigūracijos saugykla** kairiosios srities konfigūracijos medyje pasirinkite formato konfigūraciją **Laisvos formos tekstinė sąskaita faktūra („Excel”)**.
5. **Versijos** „FastTab” skirtuke pasirinkite pasirinktos ER formato konfigūracijos naujausią versiją (pavyzdžiui, **„240.112”**).
6. Pasirinkite **Importuoti**, kad pasirinktą versiją atsisiųstumėte iš Bendrosios saugyklos į dabartinę „Finance“ programą.

![Standartinių ER konfigūracijų importavimas puslapyje Konfigūracijos saugykla.](./media/er-embed-images-header-footer-excel-reports-import-solution.png)

> [!TIP]
> Jei kyla problemų prisijungiant prie [Bendrosios saugyklos ](er-download-configurations-global-repo.md), vietoj to galite [atsisiųsti konfigūracijas](download-electronic-reporting-configuration-lcs.md) iš „Microsoft Dynamics Lifecycle Services (LCS)”.

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>Importuotų ER konfigūracijų peržiūra

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos** dalyje pasirinkite plytelę **Konfigūracijų ataskaitos**.
3. Puslapio **Konfigūracijos** konfigūracijos medžio kairėje pusėje išplėskite **Sąskaitos faktūros modelis**.
4. Kartu su pasirinktu ER formatu **Laisvos formos sąskaita faktūra („Excel”)** buvo importuotos kitos būtinos ER konfigūracijos. Įsitikinkite, kad sekančios ER konfigūracijos yra prieinamos konfigūracijos medyje:

    - **Sąskaitos faktūros modelis** – šioje konfigūracijoje yra [duomenų modelio](general-electronic-reporting.md#data-model-and-model-mapping-components) ER komponentas, rodantis sąskaitos faktūros verslo domeno duomenų struktūrą.
    - **Sąskaitos faktūros modelio susiejimas** – šioje konfigūracijoje yra [modelio susiejimo ](general-electronic-reporting.md#data-model-and-model-mapping-components) ER komponentas, aprašantis, kaip duomenų modelis užpildomas programos duomenimis vykdymo metu.
    - **Laisvos formos sąskaita faktūra („Excel”)** – šioje konfigūracijoje yra [formato](general-electronic-reporting.md#FormatComponentOutbound) ir formato susiejimo ER komponentai. Formato komponentas nurodo ataskaitos maketą, paremtą „Excel” formato šablonu. Formato susiejimo komponentas apima modelio duomenų šaltinį ir nurodo, kaip šis duomenų šaltinis naudojamas ataskaitos maketui užpildyti vykdymo metu.

![Importuotos ER konfigūracijos puslapyje Konfigūracijos.](./media/er-embed-images-header-footer-excel-reports-imported-solution.png)

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a><a id="PrintInvoice1"></a>Spausdinti laisvos formos sąskaitą faktūrą naudojant standartinį ER formatą

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement1"></a>Nustatyti spausdinimo valdymą

1. Eikite į **Gautinos sumos** \> **Sąskaitos faktūros** \> **Visos laisvos formos SF**.
2. Puslapyje **Laisvos formos SF** pasirinkite **„FTI-00000002”** sąskaitą faktūrą, o tada veiksmų srities skirtuke **Sąskaita faktūra**, grupėje **Spausdinimo valdymas** pasirinkite **Spausdinimo valdymas**.
3. **Spausdinimo valdymo nustatymo** puslapio kairiniame medyje išplėskite **Modulis – gautinos sumos \> Dokumentai \> Laisvos formos sąskaita faktūra**, o tada pasirinkite **Pradinį \<Default\>** elementą.
4. Lauke **Ataskaitos formatas** pasirinkite **Laisvos formos sąskaita faktūra („Excel”)**.
5. Pasirinkite klavišą **„Esc”**, jei norite palikti **Spausdinimo valdymo nustatymo** puslapį ir grįžti į **Laisvos formos sąskaitos faktūros** puslapį.

![Laisvos formos sąskaitos faktūros standartiniu ER formatu spausdinimo valdymo parametrai Spausdinimo valdymo nustatymo puslapyje.](./media/er-embed-images-header-footer-excel-reports-print-management.png)

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice1"></a>Spausdinti laisvos formos SF

1. Puslapyje **Laisvos formos SF** įsitikinkite, kad **„FTI-00000002”** sąskaita faktūra vis dar pažymėta, o tada veiksmų srities skirtuke **Sąskaita faktūra**, grupėje **Dokumentas** pasirinkite **Spausdinimas** \> **Pasirinkta**.
2. Atsisiųskite sugeneruotą sąskaitą faktūrą „Excel” formatu ir atidarykite ją peržiūrai.
3. Atkreipkite dėmesį, kad pagal pateikto ER formato „Excel” šablono struktūrą sugeneruotos sąskaitos faktūros puslapio poraštėje yra informacija apie dabartinio puslapio numerį ir bendrą ataskaitos puslapių skaičių.

![Sugeneruota laisvos formos sąskaita faktūra.](./media/er-embed-images-header-footer-excel-reports-print-invoice1.gif)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Pritaikykite standartinį ER formatą

Pavyzdžiui, šiame skyriuje galite naudoti „Microsoft” teikiamas ER konfigūracijas, kad sugeneruotumėte laisvos formos sąskaitą faktūrą „Excel” formatu. Tačiau, norėdami sugeneruotų sąskaitų faktūrų puslapio poraštėje įtraukti įmonės logotipo vaizdą, turite pridėti tinkinimą.

Šiuo atveju, būdami „Litware, Inc.” atstovu turite sukurti (išvesti) naują ER formato konfigūraciją, pagrįstą „Microsoft” pateikta **Laisvos formos sąskaitos faktūros („Excel”)** konfigūracija.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Sukurkite pritaikytą formatą

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** kairiosios srities konfigūracijos medyje išplėskite **SF modelis**, o tada pasirinkite **Laisvos formos sąskaita faktūra („Excel”)**. „Litware, Inc.” naudos šio ER formato konfigūracijos importuotą versiją (pavyzdžiui, **„240.112”**) kaip pasirinktinės versijos pagrindą.
3. Pasirinkite **Kurti konfigūraciją**, kad atidarytumėte išplečiamąjį dialogo langą. naudokite šį dialogo langą, kad sukurtumėte naują pasirinktinio mokėjimo formato konfigūraciją.
4. **Nauja** lauko grupėje pasirinkite **Išvesti iš Pavadinimo: Laisvos formos sąskaita faktūra („Excel”), „Microsoft”** parinktį.
5. Lauke **Pavadinimas** įveskite **Tinkinta laisvos formos sąskaita faktūra („Excel”)**.
6. Pasirinkite **Kurti konfigūraciją**.

![Pasirinktinio mokėjimo formato konfigūracijos kūrimas išplečiamajame dialogo lange Kurti konfigūraciją.](./media/er-embed-images-header-footer-excel-reports-add-derived-format.png)

Sukuriama 240.112.1 versijos **Laisvos formos sąskaitos faktūros („Excel”) pasirinktinio** ER formato konfigūracija. Ši versija turi [būseną](general-electronic-reporting.md#component-versioning) **Juodraštis** ir ji gali būti redaguojama. Jūsų pritaikyto ER formato dabartinis turinys atitinka „Microsoft” pateikto formato turinį.

![Nauja ER formato konfigūracijos versija, sukurta Konfigūracijų puslapyje.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration1.png)

### <a name="edit-the-custom-format"></a><a id="ConfigureDerivedFormat"></a>Pasirinktinio formato redagavimas

Sukonfigūruokite pasirinktinį formatą taip, kad įmonės logotipo vaizdas būtų įtrauktas į poraštę kiekviename ataskaitos puslapyje.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** kairiosios srities konfigūracijos medyje išplėskite **Mokėjimo modelis**, o tada pasirinkite **Tinkinta laisvos formos sąskaita faktūra („Excel”)**.
3. **Versijos** „FastTab” skirtuke pasirinkite pasirinktos konfigūracijos **240.112.1** versiją.
4. Pasirinkite **Dizaino įrankis**.
5. **Formato kūrimo įrankis** puslapyje pasirinkite **Rodyti išsamią informaciją**, kad peržiūrėtumėte daugiau informacijos apie formatavimo elementus.
6. Išplėskite ir peržiūrėkite šiuos elementus:

    - **„Excel”** tipo **Laisvos formos sąskaitos faktūros** elementas. Šis elementas yra naudojamas sąskaitai faktūrai generuoti „Excel” darbaknygės formatu.
    - **Lapo** tipo **Laisvos formos sąskaitos faktūros\\ Sąskaitos faktūros** elementas. Šis elementas yra naudojamas sugeneruotos „Excel” darbaknygės darbalapiui generuoti.
    - **Poraštės** tipo **Laisvos formos sąskaitos faktūros \\ Sąskaitos faktūros \\ Poraštės** elementas. Šis elementas naudojamas sąskaitos faktūros poraštei užpildyti.

7. Pasirinkite **Laisvos formos sąskaitos faktūros \\ Sąskaitos faktūros \\ Poraštės** elementą.

    ![Poraštės elementas, esantis ER operacijų kūrimo įrankyje.](./media/er-embed-images-header-footer-excel-reports-derived-format0.png)

    > [!NOTE]
    > Kiekvienoje sugeneruotos sąskaitos faktūros puslapio poraštėje yra informacijos apie dabartinį puslapio numerį ir bendrą ataskaitos puslapių skaičių. Kaip matote, **Laisvos formos sąskaita faktūra \\ Sąskaita faktūra \\ Poraštė** elemente nėra antrinių elementų. Todėl naudojamas „Excel” šablonas yra konfigūruojamas rodyti puslapių kaitos informaciją kiekvienos ataskaitos poraštės centre.

8. Pasirinkite **Pridėti** ir pasirinkite **„Excel” \\ Vaizdas** pridedamo elemento formato tipą:

    1. Lauke **Lygiavimas** pasirinkite **Dešinė**.
    2. Lauke **Skalės aukštis** pasirinkite **Santykinis**.
    3. Lauke **Skalė procentais** įveskite **70**.
    4. Pasirinkite **Gerai**.

        > [!NOTE]
        > **„Excel” \\ Paveikslėlio** elementas yra naudojamas įmonės logotipo vaizdui pridėti ir lygiuoti dešinėje puslapio poraštės pusėje.

    ![Paveikslėlio elemento ypatybės dialogo lange Komponento ypatybės.](./media/er-embed-images-header-footer-excel-reports-derived-format1.png)

9. Kairiniame formato struktūros medyje pasirinkite ką tik pridėtą **Paveikslėlio** elementą, o tada skirtuke **Susiejimas** išplėskite duomenų šaltinio **modelį**.
10. Išplėskite **„model.Payment”** \> **„model.InvoiceBase” \> „model.InvoiceBase.CompanyInfo”**, o tada pasirinkite **„model.InvoiceBase.CompanyInfo.Logo”** duomenų šaltinio lauką. [Konteinerio](er-formula-supported-data-types-composite.md#container) tipo duomenų šaltinio parodo įmonės logotipo vaizdą kaip laikmenos turinį.
11. Pasirinkite **Susieti**. **Paveikslėlio** formato elementas dabar yra susietas su **„model.InvoiceBase.CompanyInfo.Logo”** duomenų šaltinio lauku. Todėl vykdymo metu įmonės logotipo vaizdas bus įdėtas į sugeneruotų sąskaitų faktūrų poraštes.

    ![Paveikslėlio formato elementas yra susietas su „model.InvoiceBase.CompanyInfo.Logo” duomenų šaltinio lauku ER operacijų kūrimo įrankyje.](./media/er-embed-images-header-footer-excel-reports-derived-format2.png)

12. Pasirinkite **Įrašyti** ir uždarykite **Dizaino įrankio** puslapį.

### <a name="mark-the-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Pažymėkite tinkintą formatą kaip leistiną

Kadangi pirmoji tinkinto formato versija, kurios būsena **Juodraštis**, buvo sukurta, formatą galite paleisti testavimui. Norėdami paleisti ataskaitą, apdorokite tiekėjo mokėjimą naudodami mokėjimo būdą, nurodantį jūsų pritaikytą ER formatą. Pagal numatytuosius nustatymus jums iškvietus ER formatą programoje tik būseną` **Baigta** ar **Bendrinta** turinčios versijos [bus svarstomos](general-electronic-reporting.md#component-versioning). Toks veikimas užtikrina, kad nebaigto dizaino ER formatai nebūtų naudojami. Tačiau, atliekant bandomuosius vykdymus, galite priversti programą naudoti ER formato **Juodraštis** būsenos versiją. Tokiu būdu galite koreguoti dabartinio formato versiją, jei reikia atlikti pakeitimus. Daugiau informacijos žr. [Taikomumas](electronic-reporting-destinations.md#applicability).

Norėdami naudoti ER formato juodraščio versiją, turite aiškiai pažymėti ER formatą.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
3. **Vartotojo parametrai** dialogo lange nustatykite **Leisti parametrus** parinktį į **Taip** ir pasirinkite **Gerai**.
4. Pasirinkite **Redaguoti**, kad šį puslapį būtų galima redaguoti, o tada konfigūracijos medžio kairinėje srityje pasirinkite **Tinkinta laisvos formos sąskaita faktūra („Excel”)**.
5. Nustatykite **Leist juodraštį** parinktį į **Taip**.

![Tinkinto formato žymėjimas kaip vykdytino konfigūracijų puslapyje.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration2.png)

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a><a id="PrintInvoice2"></a>Spausdinti laisvos formos sąskaitą faktūrą naudojant tinkintą ER formatą

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement2"></a>Nustatyti spausdinimo valdymą

1. Eikite į **Gautinos sumos** \> **Sąskaitos faktūros** \> **Visos laisvos formos SF**.
2. Puslapyje **Laisvos formos SF** pasirinkite **„FTI-00000002”** sąskaitą faktūrą, o tada veiksmų srities skirtuke **Sąskaita faktūra**, grupėje **Spausdinimo valdymas** pasirinkite **Spausdinimo valdymas**.
3. **Spausdinimo valdymo nustatymo** puslapio kairiniame medyje išplėskite **Modulis – gautinos sumos** \> **Dokumentai** \> **Laisvos formos sąskaita faktūra**, o tada pasirinkite **Pradinį** **\<Default\>** elementą.
4. Lauke **Ataskaitos formatas** pasirinkite **Tinkinta laisvos formos sąskaita faktūra („Excel”)**.
5. Pasirinkite klavišą **„Esc”**, jei norite palikti **Spausdinimo valdymo nustatymo** puslapį ir grįžti į **Laisvos formos sąskaitos faktūros** puslapį.

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice2"></a>Spausdinti laisvos formos SF

1. Puslapyje **Laisvos formos SF** įsitikinkite, kad **„FTI-00000002”** sąskaita faktūra vis dar pažymėta, o tada veiksmų srities skirtuke **Sąskaita faktūra**, grupėje **Dokumentas** pasirinkite **Spausdinimas** \> **Pasirinkta**.
2. Atsisiųskite sugeneruotą sąskaitą faktūrą „Excel” formatu ir atidarykite ją peržiūrai.
3. Atkreipkite dėmesį, kad pagal pasirinktinio ER formato struktūrą sugeneruotos sąskaitos faktūros puslapio poraštėje yra įmonės logotipo vaizdas ir informacija apie ataskaitos puslapių sąrašą.

![Sugeneruota laisvos formos sąskaita faktūra su įmonės logotipo vaizdu puslapio poraštėje.](./media/er-embed-images-header-footer-excel-reports-print-invoice2.gif)

## <a name="additional-resources"></a><a id="References"></a>Papildomi ištekliai

- [Konfigūracijų kūrimas dokumentams „Excel“ formatu generuoti](er-fillable-excel.md)
- [Vaizdų ir figūrų įterpimas generuojamuose dokumentuose naudojant ER](electronic-reporting-embed-images-shapes.md)
