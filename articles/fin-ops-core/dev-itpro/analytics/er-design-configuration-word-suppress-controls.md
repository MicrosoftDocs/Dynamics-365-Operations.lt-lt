---
title: Nerodomo „Word” turinio valdikliai sugeneruotose ataskaitose
description: Šioje temoje paaiškinama, kaip konfigūruoti elektroninės ataskaitos (ER) formatą ataskaitoms generuoti, pavyzdžiui, failams „Microsoft Word”, kuriuose turinio valdikliai nerodomi.
author: NickSelin
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: e6ab75c970c6c14d4977b6c739ba46e33f4962e9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348049"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a>Nerodomo „Word” turinio valdikliai sugeneruotose ataskaitose

[!include [banner](../includes/banner.md)]

Norėdami generuoti ataskaitas „Microsoft Word” kaip dokumentus, turite sukurti ataskaitų šabloną kaip „Word” dokumentą. Šiame šablone turi būti „Word” duomenų valdikliai, kaip vietos rezervavimo ženklai duomenims, kurie turi būti užpildyti apdorojimo metu. Norėdami naudoti „Word” dokumentą, sukurtą kaip šabloną jūsų ataskaitoms, galite [sukonfigūruoti](er-design-configuration-word.md) naują [elektroninės ataskaitos (ER)](general-electronic-reporting.md) [sprendimą](er-quick-start1-new-solution.md). Šis sprendimas turi apimti ER [konfigūraciją,](general-electronic-reporting.md#Configuration) kurioje yra ER [formato](general-electronic-reporting.md#FormatComponentOutbound) komponentas. Šis ER formatas turi būti sukonfigūruotas naudoti skirtą šabloną ataskaitai kurti.

Versijoje 10.0.6 ir vėlesnėse „Dynamics 365 Finance” versijose galite konfigūruoti formules savo ER formatu, kad sugeneruotuose dokumentuose nerodomi kai kuriuos „Word” turinio valdiklius.

Toliau paaiškinama, kaip vartotojas, kuris priskirtas sistemos administratoriui arba elektroninio ataskaitų funkcinio konsultanto vaidmeniui, gali konfigūruoti ER formatą, kuris generuoja ataskaitas kaip „Word” failus ir nerodo kai kuriuos sugeneruotų ataskaitų, kurios sukonfigūruotos naudojant „Word” šabloną, turinio valdiklius.

Šie žingsniai gali būti užbaigti GBSI bendrovėje.

## <a name="prerequisites"></a>Būtinieji komponentai

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti šių užduočių vadovuose nurodytus veiksmus:

- [Konfigūracijos, skirtos ataskaitoms OPENXML formatu generuoti, kūrimas](./tasks/er-design-reports-openxml-2016-11.md)
- [Pakartotinai naudokite ER konfigūracijas su „Excel“ šablonais, kad sugeneruotumėte ataskaitas „Word“ formatu](./tasks/er-design-configuration-word-2016-11.md)

Kai atliksite šių užduočių vedlių veiksmus, šie elementai bus paruošti:

- **Darbalapio ataskaitos pavyzdys** ER formatas, sukonfigūruotas generuoti dokumentą „Word” formatu
- [Juodraštis](general-electronic-reporting.md#component-versioning) ataskaitos **Darbalapio ataskaitos pavyzdys** versijos, pažymėtas kaip **Vykdytinas**
- **Elektroninis** mokėjimo būdas, sukonfigūruotas naudoti **Darbalapio ataskaitos pavyzdys** ER formatu tiekėjo mokėjimui apdoroti

Taip pat turite atsisiųsti ir įrašyti šį ataskaitos pavyzdžio šabloną:

- [Susietas mokėjimo ataskaitos šablonas Nr. 2 (SampleVendPaymDocReportBounded2.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a>Peržiūrėkite atsisiųstą „Word” šabloną

1. „Word” darbalaukio programoje atidarykite **SampleVendPaymDocReportBounded2.docx** šablono failą, kurį atsisiuntėte anksčiau.
2. Patikrinkite, ar šablono faile yra suvestinės skyrius, kuriame rodomos kiekvieno valiutos kodo, kurį atitiko apdoroti mokėjimai, bendros mokėjimo sumos.

    - Suvestinės dalis yra atskiroje „Word” dokumento lentelėje.
    - Pirmoje šios lentelės eilutėje lentelės stulpelių antraštės yra sekcijos antraštė.
    - Antroje šios lentelės eilutėje kaip išsami informacija apie sekciją yra pasikartojantis turinio valdiklis.
    - Šis turinio valdiklis yra susietas su **SuvestinėsEilutės** lauko **Ataskaita** tinkintos XML dalies.
    - Pagal šį susiejimą turinio valdiklis yra susietas su **SuvestinėsEilutės** redaguotino ER formato elementu.

    > [!NOTE]
    > Pasikartojantis turinio valdiklis žymimas **SuvestinėsEilutės** raktu, atitinkančiu pasirinktinės susietos XML dalies lauką.

    ![„Word” šablono maketas.](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a>Pasirinkite esamą ER ataskaitos konfigūraciją

Toliau nurodytus veiksmus atlikite iš naujo naudodami esamą ER konfigūraciją, kurią konfigūravote, kai įbaigsite anksčiau paminėtuose užduočių vadovuose nurodytus veiksmus.

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. Pasirinkite **Ataskaitų konfigūracijos**.
3. Puslapyje **Konfigūracijos** konfigūracijų medžio kairinėje srityje išskleiskite **Mokėjimo modelis**, o tada pasirinkite **Darbalapio ataskaitos pavyzdys**.
4. Pasirinkite **Kūrimo įrankis**, kad galėtumėte redaguoti pasirinkto ER formato juodraščio versiją.

## <a name="replace-the-current-template-with-the-new-template"></a>Pakeiskite esamą šabloną nauju šablonu

Šiuo metu SampleVendPaymDocReportBounded.docx failas naudojamas kaip šablonas „Word” formato išvesčiai generuoti. Atlikdami kitus veiksmus, pakeisite šį „Word” šabloną nauju „Word” šablonu, SampleVendPaymDocReportBounded2.docx, kurį atsisiuntėte anksčiau.

1. Puslapyje **Formato kūrimo įrankis** pasirinkite **Priedai**.
2. Puslapyje **Priedai** pasirinkite **Naikinti**, kad pašalintumėte esamą „Excel” šabloną.
3. Norėdami patvirtinti sunaikinimo operaciją, pasirinkite **Taip**.
4. Pasirinkite **Naujas** \> **Failas**.
5. Pasirinkite **Naršyti**, o tada pereikite ir pasirinkite **SampleVendPaymDocReportBounded2.docx** failą, kurį atsisiuntėte anksčiau.
6. Pasirinkite **Gerai**.
7. Uždarykite puslapį **Priedai**.
8. **Formato kūrimo įrankis** puslapyje, **Šablonas** lauke įveskite arba pasirinkite **SampleVendPaymDocReportBounded2.docx** failą.

## <a name="run-the-format-to-create-word-output"></a>Paleiskite formatą, kad sukurtumėte „Word“ išvestį

1. Eikite į **Mokėtinos sąskaitos** \> **Mokėjimai** \> **Mokėjimų žurnalas**.
2. Puslapyje **Tiekėjų mokėjimai**, **Sąrašas** skirtuke pasirinkite visus mokėjimus.
3. Pasirinkite **Mokėjimo būsena** \> **Nėra**.
4. Pasirinkite **Generuoti mokėjimus**.
5. Lauke **Mokėjimo būdas** pasirinkite **Elektroninis**.
6. Lauke **Banko sąskaita** įveskite **GBSI OPER**.
7. Pasirinkite **Gerai**.
8. **Elektroninės ataskaitos parametrai** dialogo lange pasirinkite **Gerai** ir išanalizuokite sugeneruotą išeigą.

    ![Apdorotini mokėjimai puslapyje Tiekėjo mokėjimai.](./media/er-design-configuration-word-suppress-controls-image2.gif)

    Išvestis pateikiama „Word” formatu ir joje yra suvestinės dalis.

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a>Konfigūruokite redaguojamą formatą, kad suvestinės skyrius būtų nerodomas

Jei norite nerodyti suvestinės skyriaus sugeneruotame dokumente, remiantis vartotojo, kuris paleidžia šį ER formatą, užklausa, turite modifikuoti redaguojamą ER formatą.

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos** ir atidarykite ER formato juodraščio versiją, kad jį suredaguotumėte.
2. Pasirinkite **Ataskaitų konfigūracijos**. 
3. **Konfigūracijos** puslapyje, konfigūracijų medyje, išplėskite **Mokėjimo modelis** \> **Darbalapio ataskaitos pavyzdys**.
4. Pasirinkite **Dizaino įrankis**.
5. **Formato kūrimo įrankis** puslapyje išplėskite **„Word”** ir pasirinkite **SuvestinėsEilutės**.
6. **Susiejimas** skirtuke, pridėkite duomenų šaltinį, kad paklaustumėte vartotojo, ar apdorojimo metu nerodyti suvestinės sekcijos:

    1. Pasirinkite **Įtraukti šaknį**.
    2. **Pridėti duomenų šaltinį** dialogo lange pasirinkite **Bendras / Vartotojo įvesties parametras**, kad atidarytumėte **Vartotojo įvesties parametro duomenų šaltinio ypatybės** dialogo langą.
    3. Lauke **Pavadinimas** įveskite **uipNerodyti**.
    4. Lauke **Žyma** įveskite **Nerodyti suvestinės sekcijos**.
    5. Lauke **Operacijų duomenų tipo pavadinimas** lauke pasirinkite arba įveskite **NeTaip**.
    6. Pasirinkite **Gerai**.

7. Pridėkite naują duomenų šaltinį **NeTaip** programos išvardijimo tipo:

    1. Pasirinkite **Įtraukti šaknį**.
    2. **Pridėti duomenų šaltinį** dialogo lange pasirinkite **Dynamics 365 for Operations\Išvardijimas**, kad atidarytumėte **„Išvardijimo” duomenų šaltinio ypatybės** dialogo langą.
    3. Lauke **Pavadinimas** įveskite **enumNeTaip**.
    4. Lauke **Žyma** įveskite **Nerodyti parinkčių**.
    5. Lauke **Operacijų duomenų tipo pavadinimas** lauke pasirinkite arba įveskite **NeTaip**.
    6. Pasirinkite **Gerai**.

8. Pasirinktam **SuvestinėsEilutės** formato elementui, sukonfigūruokite formulę, nurodančią, kada „Word” turinio valdiklis, susietas su pasirinktu formato elementu, turi būti nerodomas:

    1. **Susiejimas** skirtuke, **Pašalinta** dalyje, pasirinkite **Redaguoti**, kad atidarytumėte **[Formulės kūrimo įrankio](general-electronic-reporting-formula-designer.md)** puslapį.
    2. **Formulė** lauke įveskite formulę `uipSuppress = enumNoYes.Yes`.
    3. Pasirinkite **Įrašyti** ir uždarykite puslapį **Formulių dizaino įrankis**.

        > [!NOTE]
        > Ši formulė bus taikoma sugeneruotame dokumente, **kai bus paleisti visi kiti formato elementai**. Norėdami taikyti šią formulę, sugeneruotame dokumente randamas „Word” turinio valdiklis, žymimas kaip formato elementas, kurį sukonfigūravo formulė (šiuo atveju **SuvestinėsEilutės**). Tada šis turinio valdiklis yra visiškai pašalintas kartu su „Word” lentelės eilute, kurioje jis yra. Suvestinės skyriaus informacijos eilutė pašalinama iš sugeneruoto dokumento.
        >
        > Kūrimo metu galite konfigūruoti formato elementą **Pašalinta**, tačiau nei vienas jūsų naudojamas turinio valdiklis „Word” šablone neturi žymos, atitinkančios formato elemento pavadinimą, pagal kurį **Pašalinta** ypatybė yra sukonfigūruota. Kai tikrinate formatą kūrimo metu, gaunate [perspėjimą](er-components-inspections.md#i14) apie šį nesutapimą.
        >
        > Apdorojimo metu pateikiama išimtis, jei nėra „Word” šablono, kurį naudojate, turinio valdiklio žymės, kuri atitinka formato elemento, kurio sukonfigūruota ypatybė **Pašalinta** pavadinimą.

    4. Skirtuko **Susiejimas**, **Pašalinta** dalyje, nustatykite **Su tėviniu** parinktį į **Taip**.

        > [!NOTE]
        > Turite nustatyti parinktį į **Taip**, kad pašalintumėte visą „Word” lentelę kaip eilutės pirminį objektą, kuriame yra suvestinės skyriaus informacija. Jei nustatote šią parinktį į **Ne**, skyriaus antraštės eilutė lieka sugeneruotame dokumente.

9. Pasirinkite **Įrašyti** tam, kad išsaugotumėte pakeitimus redaguotiname formate.

    ![Sugeneruota išvestis „Word” formatu.](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a>Paleiskite pakeistą formatą, kad sukurtumėte „Word“ išvestį

1. Eikite į **Mokėtinos sąskaitos** \> **Mokėjimai** \> **Mokėjimų žurnalas**.
2. Pasirinkite jūsų sukurtą mokėjimo žurnalą, tada pasirinkite **Eilutės**.
3. Puslapyje **Tiekėjo mokėjimai** pasirinkite visas eilutes, tada pasirinkite **Mokėjimo būsena**\> **Nėra**.
4. Pasirinkite **Generuoti mokėjimus**.
5. Lauke **Mokėjimo būdas** pasirinkite **Elektroninis**.
6. Lauke **Banko sąskaita** įveskite **GBSI OPER**.
7. Pasirinkite **Gerai**.
8. **Elektroninės ataskaitos parametrai** dialogo lange, lauke **Nerodyti suvestinės skyriaus** lauke, pasirinkite **Taip**.
9. Pasirinkite **Gerai** ir analizuokite sugeneruotą išvestį.

    ![Sugeneruota išvestis „Word” formatu.](./media/er-design-configuration-word-suppress-controls-image4.gif)

    Atkreipkite dėmesį, kad išvestyje nėra suvestinės skyriaus, nes jis nerodomas.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Konfigūracijos, skirtos ataskaitoms OPENXML formatu generuoti, kūrimas](./tasks/er-design-reports-openxml-2016-11.md)
- [Ataskaitų generavimo „Word“ formatu naujos ER konfigūracijos kūrimas](er-design-configuration-word.md)
- [Pakartotinai naudokite ER konfigūracijas su „Excel“ šablonais, kad sugeneruotumėte ataskaitas „Word“ formatu](./tasks/er-design-configuration-word-2016-11.md)
- [Sukonfigūruoto ER komponento patikrinimas, kad nekiltų vykdymo problemų](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]