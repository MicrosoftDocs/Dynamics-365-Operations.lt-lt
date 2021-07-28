---
title: ER konfigūracijų su „Excel” šablonais, skirtų ataskaitų „Word” formatu generavimui, pakartotinis naudojimas
description: Šioje temoje aprašoma, kaip ataskaitai formatai, skirti generuoti ataskaitoms kaip „Excel” darbaknygėms, gali būti konfigūruojami ataskaitų kaip „Word” dokumentų konfigūravimui.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d152449b55ab111cf5bac363b38d32c3658a56e3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359416"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a>ER konfigūracijų su „Excel” šablonais, skirtų ataskaitų „Word” formatu generavimui, pakartotinis naudojimas

[!include [banner](../../includes/banner.md)]

Norėdami generuoti ataskaitas kaip „Microsoft Word” dokumentus, galite [konfigūruoti](../er-design-configuration-word.md) naują [Elektroninių ataskaitų (ER)](../general-electronic-reporting.md) [formatą](../general-electronic-reporting.md#FormatComponentOutbound). Arba galite pakartotinai naudoti ER formatą, kuris iš pradžių buvo sukurtas generuoti ataskaitoms kaip „Excel” darbaknygėms. Šiuo atveju turite pakeisti „Excel” šabloną į „Word” šabloną.

Tolesnės procedūros rodo, kaip vartotojas sistemos administratoriaus vaidmenyje arba elektroninės ataskaitos kūrėjo vaidmenyje gali konfigūruoti ER formatą, skirtą generuoti ataskaitoms kaip „Word” failams, pakartotinai naudodamas ER formatą, kuris buvo sukurtas generuoti ataskaitoms kaip „Excel” failams.

Šias procedūras galima užbaigti GBSI įmonėje.

## <a name="prerequisites"></a>Būtinieji komponentai

Norėdami užbaigti šias procedūras, pirmiausia turite atlikti užduočių vedlyje [Konfigūracijos, skirtos ataskaitoms „OPENXML” formatu generuoti, kūrimas](er-design-reports-openxml-2016-11.md) nurodytus veiksmus.

Taip pat turite atsisiųsti ir įrašyti vietoje šiuos šablonus ataskaitos pavyzdžiui:

- [Mokėjimo ataskaitos šablonas (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [Susietas mokėjimo ataskaitos šablonas („SampleVendPaymDocReportBounded.docx”)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

Šios procedūros skirtos funkcijai, kuri buvo įtraukta į 1611 „Dynamics 365 for Operations” versiją (2016 m. lapkričio mėn).

## <a name="select-the-existing-er-report-configuration"></a>Pasirinkite esamą ER ataskaitos konfigūraciją

1. „Dynamics 365 Finance” eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. Įsitikinkite, kad konfigūracijos teikėjas **„Litware, Inc.“** yra pasirinktas kaip **Aktyvus**. Jeigu nėra, atlikite veiksmus, nurodytus [Kurkite konfigūracijos teikėjus ir pažymėkite juos kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md) užduočių vedlyje.
3. Pasirinkite **Ataskaitų konfigūracijos**. Pakartotinai naudosite esamą ER konfigūraciją, kuri iš buvo sukurta ataskaitos išvesčiai „OPENXML” formatu generuoti.
4. Puslapio **Konfigūracijos** konfigūracijų medžio kairėje srityje išskleiskite **Mokėjimo modelis**, o tada pasirinkite **Pavyzdinė darbalapio ataskaita**.

    > [!NOTE]
    > Pasirinktos ER formato konfigūracijos šablono versiją galima redaguoti **Versijos** „FastTab” skirtuke.

5. Pasirinkite **Dizaino įrankis**.
6. Puslapyje **Formato dizaino įrankis** atkreipkite dėmesį, kad šakninio formato elemento pavadinimas nurodo, kad šiuo metu naudojamas „Excel” šablonas.

![Esamos konfigūracijos pasirinkimas.](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a>Peržiūrėkite atsisiųstą „Word” šabloną

1. „Word” darbalaukio programoje atidarykite **„SampleVendPaymDocReport.docx”** šablono failą, kurį atsisiuntėte anksčiau.
2. Patvirtinkite, kad šiame šablone yra tik dokumento maketas, kurį norite sugeneruoti kaip ER išvestį.

![„Word” šablono maketas darbalaukio programoje.](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a>Pakeiskite „Excel” šabloną į „Word” šabloną ir įtraukite pasirinktinę XML dalį

Šiuo metu „Excel” dokumentas naudojamas kaip šablonas OPENXML formato išvesčiai generuoti. Šį šabloną pakeisite į „Word” šablono failą „SampleVendPaymDocReport.docx”, kurį atsisiuntėte anksčiau. Taip pat išplėsite „Word“ šabloną įtraukdami pasirinktinę XML dalį.

1. „Finance” puslapio **Formato dizaino įrankis** skirtuke **Formatas** pasirinkite **Priedai**.
2. Puslapyje **Priedai** pasirinkite **Naikinti** esamo „Excel” šablono pašalinimui. Pasirinkite **Taip** pakeitimo patvirtinimui.
3. Pasirinkite **Naujas** \> **Failas**.

    > [!NOTE]
    > Turite pasirinkti dokumento tipą, kuris buvo [sukonfigūruotas](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) naudojant ER parametrus, kad išsaugotumėte ER formato šablonus.

4. Pasirinkite **Naršyti**, o tada pereikite ir pasirinkite **„SampleVendPaymDocReport.docx”** failą, kurį atsisiuntėte anksčiau.
5. Pasirinkite **Gerai**.
6. Uždarykite puslapį **Priedai**.
7. Puslapio **Formato dizaino įrankis** lauke **Šablonas** įveskite arba pasirinkite **„SampleVendPaymDocReport.docx”** failą naudoti „Word” šablonui, vietoj anksčiau naudoto „Excel” šablono.
8. Pasirinkite **Įrašyti**.

    Be to, kad išsaugomi konfigūracijos pakeitimai, veiksmas **Įrašyti** atnaujinamą pridėtą „Word” šabloną. Sukurto formato hierarchinė struktūra įtraukiama į pridėtą „Word” dokumentą kaip nauja pasirinktinė XML dalis, pavadinta **Ataskaita**. Pridėtame „Word” šablone yra dokumento maketas, kuris bus sugeneruotas kaip ER išvestis, ir duomenų struktūra, kurią apdorojimo metu ER įves į šį šabloną.

9. Atkreipkite dėmesį, kad šakninio formato elemento pavadinimas nurodo, kad šiuo metu naudojamas „Word” šablonas.

    ![„Excel” šablono pakeitimas „Word” šablonu ir pasirinktinės XML dalies įtraukimas.](../media/er-design-configuration-word-2016-11-image03.gif)

10. Skirtuke **Formatas** pasirinkite **Priedai.**

Dabar galite susieti pasirinktinės XML dalies **Ataskaita** elementus su „Word“ dokumento turinio valdikliais.

Jei esate susipažinę su „Word“ dokumentų kaip formų, turinčių [turinio valdiklius](/office/client-developer/word/content-controls-in-word), susietus su [pasirinktinių XML dalių](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) elementais, kūrimo procesu, atlikite visus tolesnės procedūros veiksmus, kad sukurtumėte tokį dokumentą. Daugiau informacijos žiūrėkite [Formų, kurias vartotojai užbaigia ar spausdina programoje „Word“, kūrimas](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b). Kitu atveju praleiskite tolesnę procedūrą.

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a>Gaukite „Word” dokumentą su pasirinktine XML dalimi ir atlikite duomenų susiejimą

1. „Finance” puslapyje **Priedai** pasirinkite **Atidaryti** šablono atsisiuntimui iš „Finance” ir jo saugojimui vietoje kaip „Word” dokumento.
3. „Word” darbalaukio programoje atidarykite ką tik atsisiųstą dokumentą.
4. Skirtuke **Kūrėjas** pasirinkite **XML susiejimo sritis**.

    > [!NOTE]
    > Jei juostelėje nerodomas **Programuotojo** skirtukas, tinkinkite juostelę jam įtraukti.

5. Srities **XML susiejimas** lauke **Pasirinktinė XML dalis** pasirinkite **Ataskaitos** pasirinktinę XML dalį.
6. Susiekite pasirinktos **Ataskaitos** pasirinktinės XML dalies elementus ir „Word“ dokumento turinio valdiklius.
7. Įrašykite vietoje atnaujintą „Word” dokumentą kaip **„SampleVendPaymDocReportBounded.docx”**.

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Peržiūrėti „Word“ šabloną, kuriame pasirinktinė XML dalis yra susieta su turinio valdikliais

1. „Word” darbalaukio programoje atidarykite **„SampleVendPaymDocReportBounded.docx”** šablono failą.
2. Patvirtinkite, kad šiame šablone yra dokumento maketas, kurį norite sugeneruoti kaip ER išvestį. Turinio valdikliai, kurie yra naudojami kaip vietos rezervavimo ženklai duomenims, ER įvedamiems į šį šabloną vykdymo metu, yra paremti susiejimais, sukonfigūruotais tarp **Ataskaitos** pasirinktinės XML dalies elementų ir „Word” dokumento turinio valdiklių.

![„Word” šablono peržiūra darbalaukio programoje.](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Įkelkite „Word“ šabloną, kuriame pasirinktinė XML dalis yra susieta su turinio valdikliais

1. „Finance” puslapyje **Priedai** pasirinkite **Naikinti** „Word” šabloną, kuriame nėra susiejimų tarp **Ataskaitos** pasirinktinės XML dalies ir turinio valdiklių. Pasirinkite **Taip** pakeitimo patvirtinimui.
2. Pasirinkite **Nauja** \> **Failas** pridėti naujam šablonui, kuriame yra susiejimai tarp **Ataskaitos** pasirinktinės XML dalies elementų ir turinio valdiklių.

    > [!NOTE]
    > Turite pasirinkti dokumento tipą, kuris buvo [sukonfigūruotas](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) naudojant ER parametrus, kad išsaugotumėte ER formato šablonus.

3. Pasirinkite **Naršyti**, o tada naršykite ir pasirinkite **„SampleVendPaymDocReportBounded.docx”** failą, kurį atsisiuntėte ar paruošėte atlikdami procedūrą, aprašytą [Gaukite „Word” su pasirinktine XML dalimi duomenų susiejimui](#get-word-doc) skyriuje.
4. Pasirinkite **Gerai**.
5. Uždarykite puslapį **Priedai**.
6. Puslapio **Formato dizaino įrankis** lauke **Šablonas** pasirinkite ką tik atsisiųstą dokumentą.
7. Pasirinkite **Įrašyti**.
8. Uždarykite puslapį **Formato dizaino įrankis**.

## <a name="mark-the-configured-format-as-runnable"></a>Pažymėkite sukonfigūruotą formatą kaip vykdytiną

Norėdami paleisti redaguojamo formato juodraščio versiją, turite ją padaryti [vykdytina](../er-quick-start2-customize-report.md#MarkFormatRunnable).

1. „Finance” puslapio **Konfigūracijos** veiksmų srities skirtuko **Konfigūracijos** grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
2. **Vartotojo parametrai** dialogo lange nustatykite **Leisti parametrus** parinktį į **Taip** ir pasirinkite **Gerai**.
3. Pasirinkite **Redaguoti**, kad pagal poreikį galėtumėte redaguoti esamą puslapį.
4. Šiuo metu pasirinktai **Pavyzdinio darbalapio ataskaitos** konfigūracijai nustatykite parinktį **Vykdyti juodraštį** į **Taip**.
5. Pasirinkite **Įrašyti**.

## <a name="run-the-format-to-create-output-in-word-format"></a>Vykdykite formatą išvesties „Word” formatu sukūrimui

1. „Finance” eikite į **Mokėtinos sumos** \> **Mokėjimai** \> **Mokėjimų žurnalas**.
2. Anksčiau įvestame mokėjimo žurnale pasirinkite **Eilutės**.
3. Puslapyje **Tiekėjo mokėjimai** pasirinkite visas tinklelio eilutes.
4. Pasirinkite **Mokėjimo būsena** \> **Nėra**.

    ![Apdorotini mokėjimai puslapyje Tiekėjo mokėjimai.](../media/er-design-configuration-word-2016-11-image05.png)

5. Veiksmų srityje pasirinkite **Generuoti mokėjimus**.
6. Atsiradusiame dialogo lange atlikite toliau nurodytus veiksmus:

    1. Lauke **Mokėjimo būdas** pasirinkite **Elektroninis**.
    2. Lauke **Banko sąskaita** įveskite **GBSI OPER**.
    3. Pasirinkite **Gerai**.

7. Dialogo lange **Elektroninių ataskaitų parametrai** pasirinkite **Gerai**.
8. Sugeneruota išvestis pateikiama „Word” formatu kartu su informacija apie apdorotus mokėjimus. Analizuokite sugeneruotą išvestį.

    ![Sugeneruota išvestis „Word” formatu.](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a>Papildomi ištekliai

- [Ataskaitų generavimo „Word“ formatu naujos ER konfigūracijos kūrimas](../er-design-configuration-word.md)
- [Vaizdų ir figūrų įterpimas generuojamuose dokumentuose naudojant ER](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
