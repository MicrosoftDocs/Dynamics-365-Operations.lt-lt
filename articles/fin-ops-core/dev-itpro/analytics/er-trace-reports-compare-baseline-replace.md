---
title: Sugeneruotų ER ataskaitų rezultatų sekimo ir palyginimo su bazinėmis vertėmis patobulinimai
description: Šioje temoje aprašomi ER bazinio plano funkcijos 10.0.3 „Microsoft Dynamics 365 for Finance and Operations” versijoje (2019 m. birželio mėn) patobulinimai.
author: NickSelin
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 483d3ac7cd3192ffd4c785c4031a168af503f087
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743610"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a>Sugeneruotų ER ataskaitų rezultatų sekimo ir palyginimo su bazinėmis vertėmis patobulinimai

[!include[banner](../includes/banner.md)]

Šioje temoje aprašomas pirmasis patobulinimų, kurie atlikti kuriant elektroninių ataskaitų (ER) sistemą, rinkinys. Šie patobulinimai galimi „Microsoft Dynamics 365 for Finance and Operations“ 10.0.3 (2019 m. birželio mėn.) ir naujesnėse versijose.

## <a name="automate-the-setting-of-baseline-rules"></a>Automatizuokite pagrindinių taisyklių nustatymą

Temoje [Sugeneruotų ataskaitų rezultatų sekimas ir jų palyginimas su bazinėmis vertėmis](er-trace-reports-compare-baseline.md) paaiškinama, kaip konfigūruoti ER sistemą, siekiant surinkti informaciją apie ER formato vykdymą ir įvertinti šio vykdymo rezultatus. Šioje temoje pateiktame pavyzdyje parodyti veiksmai, kuriuos reikia atlikti.

Toliau pateikiami kai kurie veiksmai.

- Vykdykite ER formatą, kad būtų sugeneruotas siunčiamas failas, ir išsaugokite failą vietoje.
- Įtraukite vietoje saugomą failą kaip pagrindinės informacijos, kuri buvo pridėta prie ER formato, priedą.
- Konfigūruokite įtrauktos pagrindinės informacijos pagrindinę taisyklę. Ši konfigūracija apima toliau nurodytus veiksmus.

    - Nurodykite ER formato elementą, naudojamą siunčiamam failui generuoti.
    - Pasirinkite priedą, nurodantį sugeneruotą siunčiamą failą.

> [!NOTE]
> Šiuos veiksmus reikia atlikti patiems, net jei naujos ER galimybės leidžia juos atlikti automatiškai. Norėdami daugiau sužinoti apie šią funkciją, atlikite toliau pateiktą pavyzdį.

## <a name="example-automate-the-setting-of-baseline-rules"></a>Pavyzdys. Automatizuokite pagrindinių taisyklių nustatymą

Norėdami atlikti šiame pavyzdyje nurodytus veiksmus, pirmiausia turite atlikti veiksmus, aprašytus pavyzdyje, esančiame temos [Sugeneruotų ataskaitų rezultatų sekimas ir jų palyginimas su bazinėmis vertėmis](er-trace-reports-compare-baseline.md) skyriuje „Naujos pagrindinės informacijos įtraukimas pagal sukurtą ER formatą“.

### <a name="review-added-baseline"></a>Įtrauktos pagrindinės informacijos peržiūra

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Pasirinkite **Pagrindinė informacija**.

    > [!NOTE]
    > Veiksmų srities mygtukas **Pagrindinė informacija** yra tik tada, kai įjungtas šios įmonės ER vartotojo parametras **Vykdyti derinimo režimu**.

Įtraukta pasirinkto formato **Formatas, kuris turi mokytis ER pagrindinę informaciją** pagrindinė informacija, tačiau dar neįtrauktos šios pagrindinės informacijos pagrindinės taisyklės.

![Elektroninės ataskaitos formato bazinis puslapis, dar nėra taisyklių](media/GER-BaselineSample-AddBaseline2.PNG "Elektroninės ataskaitos (ER) formato bazinio puslapio ekrano kopija")

### <a name="make-a-new-baseline-rule"></a>Naujos pagrindinės taisyklės kūrimas

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Medyje išplėskite **Modelis, kuris turi mokytis ER pagrindinę informaciją**.
3. Medyje pasirinkite **Modelis, kuris turi mokytis ER pagrindinę informaciją\\Formatas, kuris turi mokytis ER pagrindinę informaciją**.
4. „FastTab“ **Versijos** pasirinkite **Vykdyti**.
5. Lauke **Įveskite ID** įveskite **1**.
6. Nustatykite parinkties **Kurti pagrindinės informacijos failus** reikšmę kaip **Taip**.
7. Pasirinkite **Gerai**.
8. Pasirinkite **Pagrindinė informacija**.

    ![Elektroninės ataskaitos formato bazinio puslapis, bazinės linijos pasirinktos](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Elektroninės ataskaitos (ER) formato bazinio puslapio ekrano kopija")

    Sugeneruotas siuntimo failas buvo automatiškai pridėtas prie vykdyto ER formato pagrindinės informacijos. Pagrindinė taisyklė buvo automatiškai įtraukta į šią pagrindinę informaciją; joje yra ir nuoroda į pridėtą failą.

9. Lauke **Pavadinimas** įveskite **1 pagrindinė informacija**.
10. Lauke **Failo vardo šablonas** įveskite **.xml**.
11. Pasirinkite **Įrašyti**.

### <a name="run-the-format"></a>Formato vykdymas

Dabar esate pasiruošę atlikti likusius veiksmus, nurodytus pavyzdyje, esančiame temoje [Sugeneruotų ataskaitų rezultatų sekimas ir jų palyginimas su bazinėmis vertėmis](er-trace-reports-compare-baseline.md), pradedant nuo skyriaus „Vykdyti sukurtą ER formatą ir peržiūrėti žurnalą, kad būtų išanalizuoti rezultatai“.

> [!NOTE]
> Kai panaikinate automatiškai įtrauktą pagrindinę taisyklę, esančią „FastTab“ **Pagrindinė informacija**, nurodytas priedas nėra automatiškai panaikinamas.

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Konfigūruokite pagrindinę informaciją, kad ji ignoruotų nuolat besikeičiančias ER išvesties dalis

Sukūrus ER formatą, kuriame yra informacijos, kuri keičiasi vykdant formatą, turi būti reikalaujama, kad, norint palyginti sugeneruotus rezultatus su bazinėmis vertėmis, reikia naudoti ER pagrindinės informacijos funkciją. Pavyzdžiui, informacija gali būti sugeneruoto dokumento vykdymo data ir laikas arba unikalusis identifikatorius skirtingais formatais (visuotinis unikalusis identifikatorius \[GUID\] ir t. t.). Naujosios ER galimybės leidžia sukonfigūruoti pagrindinę taisyklę, kad būtų nepaisoma ER formato besikeičiančių elementų, kai formatas yra vykdomas siekiant palyginti bazines vertes su formato vykdymo rezultatais. Norėdami daugiau sužinoti apie šią funkciją, atlikite toliau pateiktą pavyzdį.

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Pavyzdys. Konfigūruokite pagrindinę informaciją, kad ji ignoruotų nuolat besikeičiančias ER išvesties dalis

Norėdami atlikti šiame pavyzdyje nurodytus veiksmus, pirmiausia turite atlikti veiksmus, aprašytus pavyzdyje, esančiame temoje [Sugeneruotų ataskaitų rezultatų sekimas ir jų palyginimas su bazinėmis vertėmis](er-trace-reports-compare-baseline.md).

### <a name="modify-a-configured-er-format"></a>Sukonfigūruoto ER formato modifikavimas

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Medyje išplėskite **Modelis, kuris turi mokytis ER pagrindinę informaciją**.
3. Medyje pasirinkite **Modelis, kuris turi mokytis ER pagrindinę informaciją\\Formatas, kuris turi mokytis ER pagrindinę informaciją**.
4. Pasirinkite **Dizaino įrankis**.
5. Medyje pasirinkite **Išvestis\\Dokumentas**.
6. Pasirinkite **Įtraukti**.
7. Išplečiamojo dialogo lango medyje pasirinkite **XML\\Atributas**.
8. Lauke **Pavadinimas** įveskite **ProcessingDateTime**.
9. Pasirinkite **Gerai**.
10. Medžio skirtuke **Susiejimas** pasirinkite **Išvestis\\Dokumentas\\ProcessingDateTime**.
11. Pasirinkite **Redaguoti formulę**.
12. Lauke **Formulė** įveskite toliau nurodytą išraišką: **DATETIMEFORMAT(NOW(), "O")**.
13. Pasirinkite **Įrašyti**, tada pasirinkite **Testuoti**.
14. Norėdami dar kartą testuoti sukonfigūruotą išraišką pasirinkite **Testuoti**.

    ![Formulės dizaino įrankio puslapis](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Formulės kūrimo įrankio puslapio ekrano kopija")

    > [!NOTE]
    > Skirtuke **Testo vykdymo rezultatas** nurodoma, kad sukonfigūruota išraiška ją iškvietus pateikia kitą datos ir laiko vertę.

15. Uždarykite puslapį **Formulių kūrimo įrankis** ir pasirinkite **Įrašyti**.

    ![Formato dizaino įrankio puslapis](media/GER-BaselineSample-FormatMappingDesign2.PNG "Formato kūrimo įrankio puslapio ekrano kopija")

16. Uždarykite puslapį **Formato dizaino įrankis**.

### <a name="remove-an-existing-baseline-rule"></a>Esamos pagrindinės taisyklės šalinimas

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Pasirinkite **Pagrindinė informacija**.
3. Pagrindinės informacijos sąraše pasirinkite pagrindinę informaciją, kuri sukonfigūruota formatui **Formatas, kuris turi mokytis ER pagrindinę informaciją**.
4. Norėdami pašalinti anksčiau sukonfigūruotą pagrindinę taisyklę „FastTab“ **Pagrindinė informacija** pasirinkite **Naikinti**.

![Elektroninės ataskaitos formato bazinis puslapis, panaikinta](media/GER-BaselineSample-AddBaseline3.PNG "Elektroninės ataskaitos (ER) formato bazinio puslapio ekrano kopija")

### <a name="define-replacements-for-bindings-of-designed-er-format"></a>Apibrėžkite sukurto ER formato susiejimų keitimus

1. Puslapio **Konfigūracijos** „FastTab“ **Pakeitimai** pasirinkite **Pasirinkite komponentus**.
2. Formato komponentų medyje išplėskite **Išvestis**, išplėskite **Išvestis\\Dokumentas**, tada pažymėkite žymės langelį **Išvestis\\Dokumentas\\ProcessingDateTime**.
3. Pasirinkite **Gerai**.

![Elektroninės ataskaitos formato bazinis puslapis, komponentai](media/GER-BaselineSample-AddBaseline4.PNG "Elektroninės ataskaitos (ER) formato bazinio puslapio ekrano kopija")

Pasirinktas ER formato komponentas buvo įtrauktas į komponentų sąrašą „FastTab“ **Pakeitimai**. Kai pagrindinis ER formatas vykdomas derinimo režimu, kiekvieno komponento formato susiejimas bus pakeistas susiejiimu, kuris parodytas stulpelyje **Susiejimas**. Norėdami pakeisti numatytąjį susiejimą komponento, kuris yra nurodytas „FastTab“ **Pakeitimai**, pasirinkite **Redaguoti**.

### <a name="make-a-new-baseline-rule"></a>Naujos pagrindinės taisyklės kūrimas

Atlikite veiksmus, aprašytus anksčiau šios temos skyriuje „Pavyzdys. Automatizuokite pagrindinių taisyklių nustatymą“. Pranešimas įspėja, kad siunčiamas failas buvo sugeneruotas naudojant pagrindinės informacijos parametrus ir kad įvyko priverstinis formato susiejimų pakeitimas.

![Pranešimas konfigūracijų puslapyje](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Pranešimo konfigūracijų puslapyje ekrano kopija")

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a>Įspėjimų apie formato susiejimų pakeitimą slėpimas

Nustatydami tam tikrus ER parametrus, galite paslėpti pranešimus, įspėjančius apie formato susiejimų pakeitimą. Šis slėpimas gali būti naudingas, kai formato susiejimai pakeičiami režimu be priežiūros, naudojant „Regression Suite Automation Tool“. Šiuo atveju įspėjimas gali būti laikomas kaip vykdomo testavimo atvejo triktis.

1. Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos** pasirinkite **Vartotojo parametrai**.
2. Nustatykite parinkties **Slėpti pagrindinės informacijos įspėjimus** reikšmę kaip **Taip**, tada pasirinkite **Gerai**.

### <a name="review-the-generated-baseline-file"></a>Peržiūrėkite sugeneruotą pagrindinės informacijos failą

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Pasirinkite **Pagrindinė informacija**.
3. Pasirinkite **Priedai**.
    > [!NOTE]
    > Sugeneruotame faile yra vykdymo datos ir laiko tekstas (**#**) iš susiejimo, kuris buvo sukonfigūruotas įtrauktoje pagrindinėje taisyklėje, o ne iš formato susiejimo.
    
4. Uždarykite puslapį **Priedai**.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Vykdyti sukurtą ER formatą ir peržiūrėti žurnalą, kad būtų išanalizuoti rezultatai

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Medyje išplėskite **Modelis, kuris turi mokytis ER pagrindinę informaciją**.
3. Medyje pasirinkite **Modelis, kuris turi mokytis ER pagrindinę informaciją\\Formatas, kuris turi mokytis ER pagrindinę informaciją**.
4. „FastTab“ **Versijos** pasirinkite **Vykdyti**.
5. Lauke **Įveskite ID** įveskite **1**.
6. Pasirinkite **Gerai**.
7. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos derinimo žurnalai**.

Vykdymo žurnale yra informacijos apie sugeneruoto failo palyginimo su sukonfigūruota pagrindine informacija rezultatus. Žurnalas nurodo, kad sugeneruotas failas ir pagrindinė informacija yra vienodi, net jei vykdytame formate yra susiejimas, kad siunčiamame faile būtų galima įvesti nuolat besikeičiančias datos ir laiko vertes.

> [!NOTE]
> Nors siuntimo failas buvo sugeneruotas naudojant pagrindinės informacijos parametrus, kurie lėmė priverstinį formato susiejimų pakeitimą, negaunate įspėjimų apie pakeitimą.

## <a name="exchange-baseline-settings-between-environments"></a>Pagrindinės informacijos parametrų keitimas tarp aplinkų

### <a name="export-baseline-settings"></a>Pagrindinės informacijos parametrų eksportavimas

Naujos ER galimybės leidžia eksportuoti pasirinkto ER formato pagrindinės informacijos parametrus iš dabartinės aplinkos ir juos išsaugoti kaip XML failus. 

Norėdami eksportuoti pagrindinės informacijos parametrus puslapyje **Elektroninių ataskaitų formato pagrindinė informacija** pasirinkite **Eksportuoti**.

### <a name="import-baseline-settings"></a>Importuoti bazinius parametrus

Eksportuotus pagrindinės informacijos parametrus galima importuoti į kitą aplinką. Aplinka pirmiausia turi būti importuota kaip ER formatas. Tada galima importuoti pagrindinės informacijos parametrus.

Norėdami importuoti pagrindinės informacijos parametrus iš vietoje saugomo XML failo puslapyje **Elektroninių ataskaitų formato pagrindinė informacija** pasirinkite **Importuoti**, tada pasirinkite **Naršyti**, kad pasirinktumėte XML failą.

![Bazinių parametrų importavimo dialogo langas](media/GER-BaselineSample-ImportBaseline1.PNG "Bazinių parametrų importavimo dialogo lango ekrano kopija").

Norėdami importuoti pagrindinės informacijos parametrus iš XML failo, kuris saugomas „Microsoft SharePoint Server“ atsižvelgdami į dabartinius dokumentų valdymo parametrus ir pasirinktą dokumento tipą puslapyje **Elektroninių ataskaitų formato pagrindinė informacija** pasirinkite **Importuoti iš šaltinio**. Tada pasirinkti dokumento tipą ir XML failą. Būtinas dokumento tipas, kad būtų galima pasiekti „SharePoint“ aplanką, turi būti sukonfigūruotas iš anksto.

![Importavimo iš šaltinio dialogo langas](media/GER-BaselineSample-ImportBaseline2.PNG "Importavimo iš šaltinio dialogo lango ekrano kopija")

> [!NOTE]
> Galite naudoti užduočių įrašymo priemonę, kad įrašytumėte reikalingus dokumento tipo ir failo vardo pasirinkimo veiksmus dialogo lange **Importuoti iš šaltinio**. Tokiu būdu galite išlaikyti privalomus pagrindinės informacijos parametrus „SharePoint Server“, o tada juos automatiškai importuoti, leisdami užduoties įrašą, kai vykdote automatinius testus naudodami „Regression Suite Automation Tool“.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Sugeneruotų ataskaitų rezultatų sekimas ir jų palyginimas su bazinėmis vertėmis](er-trace-reports-compare-baseline.md)
- [Užduoties įrašymo ištekliai](../user-interface/task-recorder.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]