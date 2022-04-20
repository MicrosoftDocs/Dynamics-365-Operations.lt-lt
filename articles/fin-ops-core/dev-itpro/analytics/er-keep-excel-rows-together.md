---
title: ER formato kūrimas norint, kad eilutės išliktų tame pačiame „Excel“ puslapyje
description: Šioje temoje paaiškinama, kaip sukurti elektroninių ataskaitų (ER) formatą, pagal kurį eilutės bus išlaikomos tame pačiame Microsoft Excel puslapyje.
author: NickSelin
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-03-01
ms.dyn365.ops.version: Version 10.0.26
ms.openlocfilehash: 06782a4933fb5c3e86ad436b853f207fd3d5cddb
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612376"
---
# <a name="design-an-er-format-to-keep-rows-together-on-the-same-excel-page"></a>ER formato kūrimas norint, kad eilutės išliktų tame pačiame „Excel“ puslapyje

[!include [banner](../includes/banner.md)]


Šioje temoje paaiškinama, kaip sistemos administratoriaus arba elektroninio ataskaitų funkcinės [konsultanto](general-electronic-reporting.md) vaidmens vartotojas gali konfigūruoti elektroninės ataskaitos (ER) [formatą](er-overview-components.md#format-component) Microsoft Excel, kuris generuoja siunčiamus dokumentus ir valdo dokumentų puslapių temą, kad sukurtos eilutės būtų laikomos tame pačiame puslapyje.

Šiame pavyzdyje jūs pakeisite "Microsoft" pateiktą ER formatą, kuris naudojamas laisvos formos SF spausdinti Excel formatu. Jūsų pakeitimai leis jums valdyti sugeneruotos laisvos formos SF ataskaitos puslapių numeraciją, kad visos vienos SF eilutės būtų laikomos tame pačiame puslapyje, kai įmanoma.

Šios temos procedūros gali būti atliktos naudojant **„USMF”** įmonę. Kodavimas nebūtinas.

Šiame pavyzdyje jūs sukursite reikalingas [Litware](general-electronic-reporting.md#Configuration), Inc.**pavyzdžio įmonės ER** konfigūracijas. Įsitikinkite, kad **Litware, Inc.** (`http://www.litware.com`) PAVYZDŽIO įmonės konfigūracijos teikėjas yra įtrauktas į ER sistemos sąrašą ir kad jis pažymėtas kaip **Aktyvus**. Jei šio konfigūracijos teikėjo nėra arba **jei** jis nepažymėtas kaip Aktyvus, [atlikite konfigūracijos teikėjo kūrimo veiksmus ir pažymėkite jį kaip aktyvų](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="enter-a-new-free-text-invoice"></a>Įvesti naują laisvos formos SF

1. Norėdami įtraukti laisvos formos [SF, atlikite laisvos](../../../finance/accounts-receivable/create-free-text-invoice-new.md#create-a-free-text-invoice-1) formos SF kūrimo veiksmus.

    1. Prie SF pridėkite vieną eilutę.
    2. Pridėti penkias SF eilutės pastabas.

    ![SF eilutės pastabų peržiūra priedų puslapyje.](./media/er-keep-excel-rows-together-notes.png)

2. Norėdami sukurti penkias papildomas [SF eilutes,](../../../finance/accounts-receivable/create-free-text-invoice-new.md#copy-lines) kurios kopijuoja SF eilutę, pridėtą ankstesniame veiksme, atlikite veiksmus, aprašytus kopijavimo eilutėse.

    ![Peržiūrimos laisvos formos SF eilutės laisvos formos SF puslapyje.](./media/er-keep-excel-rows-together-invoice.png)

## <a name="configure-the-er-framework"></a>ER sistemos konfigūracija

Atlikite veiksmus, aprašytus skyriuje [Konfigūruoti ER sistemą](er-quick-start2-customize-report.md#ConfigureFramework), kad nustatytumėte minimalų ER parametrų rinkinį. Prieš pradėdami naudoti ER sistemą standartinio ER formato versijai kurti, turite užbaigti šį nustatymą.

## <a name="import-the-standard-er-format-configuration"></a>Standartinio ER formato konfigūracijos importavimas

Norėdami įtraukti standartines [ER konfigūracijas į dabartinį "Dynamics 365 Finance" egzempliorių, atlikite standartinės ER](er-quick-start2-customize-report.md#ImportERSolution1) formato konfigūracijos importavimo veiksmus. Pvz., importuokite **laisvos formos SF (Excel)** formato konfigūracijos 252.116 **versiją**. **Pagrindinė 252** pagrindinio SF modelio **konfigūracijos** versija automatiškai importuojama iš saugyklos kartu su reikalinga SF modelio **susiejimo** konfigūracija.

## <a name="set-up-print-management-to-use-the-standard-er-format"></a>Nustatyti spausdinimo valdymą standartiniam ER formatui naudoti

Vadovaukitės [nustatymo](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement1)**spausdinimo** valdymu, norėdami konfigūruoti gautinų sumų modulio spausdinimo valdymą taip, kad standartinis ER formatas būtų naudojamas spausdinant laisvos formos SF.

## <a name="configure-a-format-destination-for-the-standard-er-format"></a>Konfigūruokite standartinio ER formato formato paskirties vietą

Norėdami [sukonfigūruoti](er-quick-start1-new-solution.md#ConfigureDestination)[standartinio](er-destination-type-screen.md) ER formato ekrano paskirties vietą, kad sugeneruotos ataskaitos būtų konvertuojamos į PDF formatą ir būtų peržiūrimos naujoje naršyklės skirtuke, atlikite nurodytus veiksmus.

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a>Spausdinti laisvos formos sąskaitą faktūrą naudojant standartinį ER formatą

1. Norėdami naudoti standartinį [ER](er-embed-images-header-footer-excel-reports.md#ProcessInvoice1) formatą laisvos formos SF ataskaitai sugeneruoti Excel formatu, skirtai pridėtai SF, atlikite žingsnius spausdindami laisvos formos SF.
2. Atsisiųskite sugeneruotą "Excel" darbaknygę ir peržiūrėkite ją "Excel" kompiuterio programoje.

    Atkreipkite dėmesį, kad šešta SF eilutė prasideda pirmame ataskaitos puslapyje ir tęsia darbą antrame puslapyje. Paskutinė pastaba rodoma antrame puslapyje, o ne per daug, kad ji priklausytų šeštai SF eilutei. Todėl sf eilutės turinio viduryje puslapio lūžis palengvina šio dokumento skaityti.

    ![Excel darbalaukio programoje peržiūrima sugeneruotos laisvos formos SF puslapių numeracija.](./media/er-keep-excel-rows-together-invoice1.gif)

Likusios šios temos procedūros rodo, kaip galite derinti standartinį ER formatą, kad pagerinti SF ataskaitos peržvalgą ir perskaitytumą, tame pačiame puslapyje išlaikydami visą vienos SF eilutės turinį.

## <a name="create-a-custom-format"></a>Sukurkite pritaikytą formatą

Norėdami išvesti [formatą](er-embed-images-header-footer-excel-reports.md#DeriveProvidedFormat) iš importuoto ER **formato ir sukurti laisvos formos SF (Excel)** pasirinktinę ER konfigūraciją, kurią galima redaguoti ir modifikuoti, atlikite nurodytus veiksmus.

## <a name="edit-the-custom-format"></a>Pasirinktinio formato redagavimas

1. Norėdami atidaryti išvestinį [ER formatą, kad](er-embed-images-header-footer-excel-reports.md#ConfigureDerivedFormat) jį būtų galima redaguoti ER formato konstruktoriuje, atlikite nurodytus veiksmus.
2. Formato dizainerio **puslapio**, kuris yra kairiosios srities formato komponento medyje, **išplėskite Laisvos formos SF \>\> lapo SF** eilutės ir **pasirinkite InvoiceLines_Values** komponentą.
3. Skirtuke **Formatas** nustatykite pasirinktį **Išlaikyti eilutes kartu** kaip **Taip**.

    ![Redaguojamo ER formato parinkties Išlaikyti eilutes nustatymas kartu puslapyje Formatų konstruktorius.](./media/er-keep-excel-rows-together-format.png)

4. Pasirinkite **Išsaugoti** ir uždarykite puslapį.

## <a name="mark-the-custom-format-as-runnable"></a>Pažymėkite tinkintą formatą kaip leistiną

Atlikite nurodytus veiksmus, [kad pasirinktinį formatą](er-embed-images-header-footer-excel-reports.md#MarkFormatRunnable) būtų galima pažymėti kaip vykdyklė, kad modifikuota pasirinktinio ER formato versija būtų vykdoma.

## <a name="set-up-print-management-to-use-the-custom-er-format"></a>Nustatyti spausdinimo valdymą pasirinktiniam ER formatui naudoti

Vadovaukitės [nustatymo](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement2)**spausdinimo** valdymu, norėdami konfigūruoti gautinų sumų modulio spausdinimo valdymą taip, kad pasirinktinis ER formatas būtų naudojamas laisvos formos SF spausdinti.

## <a name="configure-a-format-destination-for-the-custom-er-format"></a>Konfigūruoti pasirinktinio ER formato formato paskirties vietą

Norėdami [sukonfigūruoti](er-quick-start1-new-solution.md#ConfigureDestination)**pasirinktinio** ER formato ekrano ER paskirties vietą, kad sugeneruotos ataskaitos būtų konvertuojamos į PDF formatą ir būtų peržiūrimos naujoje naršyklės skirtuke, atlikite nurodytus veiksmus.

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a>Spausdinti laisvos formos sąskaitą faktūrą naudojant tinkintą ER formatą

1. Norėdami naudoti pasirinktinį [ER formatą laisvos](er-embed-images-header-footer-excel-reports.md#ProcessInvoice2) formos SF ataskaitai sugeneruoti Excel formatu, skirtai pridėtai SF, atlikite veiksmus, nurodytus skyriuje Spausdinti laisvos formos SF.
2. Atsisiųskite sugeneruotą "Excel" darbaknygę ir peržiūrėkite ją "Excel" kompiuterio programoje.

    Atkreipkite dėmesį, kad šešta SF eilutė prasideda antrame puslapyje, o visos Excel eilutės, kuriose yra ši SF eilutė, rodomos kartu šiame puslapyje.

    ![Excel darbalaukio programoje peržiūrima atnaujinta sugeneruotos laisvos formos SF puslapių numeracija.](./media/er-keep-excel-rows-together-invoice2.gif)

## <a name="additional-resources"></a>Papildomi ištekliai

[Konfigūracijų kūrimas dokumentams „Excel“ formatu generuoti](er-fillable-excel.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
