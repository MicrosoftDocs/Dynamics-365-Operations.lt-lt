---
title: Didelių dokumentų, sugeneruotų elektroninėse ataskaitose, glaudinimas
description: Šioje temoje paaiškinama, kaip glaudinti didelius dokumentus, sugeneruotus naudojant elektroninių ataskaitų (ER) formatą.
author: NickSelin
manager: kfend
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERFormatDestinationTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ef024185c4654804f6f260a43c1bf294b33c10e2
ms.sourcegitcommit: 6e290b0d3aeedd0e234ac4f1df92b1b9afd6fccc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829684"
---
# <a name="compress-large-documents-that-are-generated-in-electronic-reporting"></a>Didelių dokumentų, sugeneruotų elektroninėse ataskaitose, glaudinimas 

[!include [banner](../includes/banner.md)]

Galite naudoti [Elektroninę ataskaitų (ER) sistemą](general-electronic-reporting.md) norėdami sukonfigūruoti sprendimą, kuris iškviečia operacijų duomenis, kad būtų sugeneruotas siunčiamas dokumentas. Šis sugeneruotas dokumentas gali būti gana didelis. Kai šio tipo dokumentas sugeneruojamas, [Programos objektų serverio (AOS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/access-instances#location-of-packages-source-code-and-other-aos-configurations) atmintis naudojama jo laikymui. Tam tikru momentu dokumentas tada turi būti atsisiųstas iš jūsų „Microsoft Dynamics 365 Finance” programos. Šiuo metu didžiausias vieno dokumento, sugeneruoto ER, dydis ribojamas iki 2 gigabaitų (GB). Be to, „Finance” šiuo metu [riboja](https://fix.lcs.dynamics.com/Issue/Details?bugId=489291) atsisiųsto failo dydį iki 1 GB. Todėl turite sukonfigūruoti ER sprendimą, kuris sumažina tikimybę, kad šie apribojimai bus viršyti, o jūs gausite **Srautas tęsėsi per ilgai** arba **Srautas perkrautas arba nepakankamas aritmetinėje operacijoje** išimtį.

Kai konfigūruojate sprendimą, galite pakoreguoti savo ER formatą Operacijų dizaino įrankyje pridėdami **Aplanko** tipo šakninį elementą, kad suglaudintumėte turinį, kurį sugeneravo bet kuris jo įdėtųjų elementų. Glaudinimas vyksta „reikiamu laiku”, kad intensyviausias atminties naudojimas ir failo, kuris bus atsisiųstas, dydis galėtų būti sumažinti.

> [!NOTE]
> Failo glaudinimas sunaudoja papildomą CPU naudojimo procentą.

Norėdami sužinoti daugiau apie šį metodą, atlikite šioje temoje esantį pavyzdį.

## <a name="example-compress-an-outbound-document"></a>Pavyzdys: Siunčiamo dokumento glaudinimas

Šis pavyzdys parodo, kaip vartotojas, kuriam priskirtas **Sistemos administratoriaus** arba **Elektroninių ataskaitų funkcinio konsultanto** vaidmuo, gali sukonfigūruoti ER formatą sugeneruoto dokumento glaudinimui.

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš vykdydami šioje temoje esančias procedūras, turite atlikti toliau nurodytus veiksmus.

1. [Aktyvuoti konfigūracijos tiekėją](er-defer-xml-element.md#activate-a-configuration-provider).
2. [Importuoti pavyzdines ER konfigūracijas](er-defer-xml-element.md#import-the-sample-er-configurations).
3. [Peržiūrėti importuotą formatą](er-defer-xml-element.md#review-the-imported-format).

> [!NOTE]
> Šiuo metu formato struktūra prasideda nuo **Failo** tipo elemento **Ataskaita**, kuriame yra XML elementų. Todėl siunčiamas dokumentas bus sugeneruotas XML formatu ir nebus naudojamas joks glaudinimas.

### <a name="generate-an-er-format-to-get-an-uncompressed-document"></a>ER formato generavimas nesuglaudinto dokumento gavimui

1. [Vykdykite importuotą formatą](er-defer-xml-element.md#run-the-imported-format).
2. Atkreipkite dėmesį, kad sugeneruoto dokumento dydis XML formatu yra 3 kilobaitų (KB).

    ![Nesuglaudinto siunčiamo dokumento peržiūra](./media/er-compress-outbound-files1.png)

### <a name="modify-the-format-to-compress-the-generated-output"></a>Formato modifikavimas sugeneruotos išvesties glaudinimui

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapyje **Konfigūracijos** konfigūracijos medyje išplėskite **Modelis, norint sužinoti apie atidėtus elementus**.
3. Pasirinkite konfigūraciją **Formatavimas atidėtiems XML elementams rasti**.
4. Pasirinkite **Dizaino įrankis** formato struktūros modifikavimui.
5. Puslapio **Formato dizaino įrankis** skirtuke **Formatas** pasirinkite **Pridėti šaknį** šakninio formato elemento pridėjimui.
6. Dialogo lange **Pridėti** pasirinkite **Bendra\\Aplankas**.
7. Pasirinkite **Gerai** naujo šakninio elemento pridėjimo patvirtinimui.
8. Pasirinkite **Įrašyti**.

> [!NOTE]
> Formato struktūra prasideda nuo **Aplanko** tipo elemento. Šis elementas sugeneruos išvestį kaip suglaudintą (zip) failą. Kai dokumentas, kurį sugeneravo **Ataskaitos** elementas, yra siunčiamą zip failą, jo turinys bus glaudinamas, kad būtų sumažintas siunčiamo failo dydis.

### <a name="generate-an-er-format-to-get-a-compressed-document"></a>ER formato generavimas suglaudinto dokumento gavimui

1. Puslapyje **Formato dizaino įrankis** pasirinkite **Vykdyti**.
2. Atsisiųskite zip failą, kuris siūlomas žiniatinklio naršyklėje ir atidarę jį peržiūrėkite.
3. Atkreipkite dėmesį, kad sugeneruoto dokumento dydis ZIP formatu yra 1 KB.

    > [!NOTE] 
    > XML failo, kuris yra zip failas, glaudinimo koeficientas yra 87 procentai. Glaudinimo koeficientas priklauso nuo glaudinimų duomenų.

    ![Suglaudinto siunčiamo dokumento peržiūra](./media/er-compress-outbound-files2.png)

> [!NOTE]
> Jei ER [paskirties vieta](electronic-reporting-destinations.md) yra konfigūruojama formato elementui, kuris generuoja išvestį (šiame pavyzdyje – **Ataskaitos** elementas), išvesties glaudinimas bus apeinamas.

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų (ER) paskirties vietos](electronic-reporting-destinations.md)

[XML elementų ER formatais vykdymo atidėjimas](er-defer-xml-element.md)