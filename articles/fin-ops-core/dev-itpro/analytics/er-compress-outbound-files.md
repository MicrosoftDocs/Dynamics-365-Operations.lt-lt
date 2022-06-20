---
title: Didelių dokumentų, sugeneruotų elektroninėse ataskaitose, glaudinimas
description: Šiame straipsnyje paaiškinama, kaip glaudinti didelius dokumentus, sugeneruotus elektroninės ataskaitos (ER) formatu.
author: NickSelin
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERFormatDestinationTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 9a4995879717e715f8ebadb6a80e00949df7545c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864813"
---
# <a name="compress-large-documents-that-are-generated-in-electronic-reporting"></a>Didelių dokumentų, sugeneruotų elektroninėse ataskaitose, glaudinimas 

[!include [banner](../includes/banner.md)]

Galite naudoti [Elektroninę ataskaitų (ER) sistemą](general-electronic-reporting.md) norėdami sukonfigūruoti sprendimą, kuris iškviečia operacijų duomenis, kad būtų sugeneruotas siunčiamas dokumentas. Šis sugeneruotas dokumentas gali būti gana didelis. Kai šio tipo dokumentas sugeneruojamas, [Programos objektų serverio (AOS)](../dev-tools/access-instances.md#location-of-packages-source-code-and-other-aos-configurations) atmintis naudojama jo laikymui. Tuomet dokumentą reikia atsisiųsti iš programos " Microsoft Dynamics 365" finansai. Šiuo metu didžiausias vieno dokumento, sugeneruoto ER, dydis ribojamas iki 2 gigabaitų (GB). Be to, „Finance” šiuo metu [riboja](https://fix.lcs.dynamics.com/Issue/Details?kb=4569432&bugId=453907&dbType=3) atsisiųsto failo dydį iki 1 GB. Todėl turite sukonfigūruoti ER sprendimą, kuris sumažina tikimybę, kad šie apribojimai bus viršyti, o jūs gausite **Srautas tęsėsi per ilgai** arba **Srautas perkrautas arba nepakankamas aritmetinėje operacijoje** išimtį.

Kai konfigūruojate sprendimą, galite pakoreguoti savo ER formatą Operacijų dizaino įrankyje pridėdami **Aplanko** tipo šakninį elementą, kad suglaudintumėte turinį, kurį sugeneravo bet kuris jo įdėtųjų elementų. Glaudinimas vyksta „reikiamu laiku”, kad intensyviausias atminties naudojimas ir failo, kuris bus atsisiųstas, dydis galėtų būti sumažinti.

> [!NOTE]
> Failo glaudinimas sunaudoja papildomą CPU naudojimo procentą.

Norėdami gauti daugiau informacijos apie šį būdą, šiame straipsnyje užpildykite pavyzdį.

## <a name="example-compress-an-outbound-document"></a>Pavyzdys: Siunčiamo dokumento glaudinimas

Šis pavyzdys parodo, kaip vartotojas, kuriam priskirtas vaidmuo **Sistemos administratorius** arba **Elektroninių ataskaitų funkcinis konsultantas**, gali sukonfigūruoti ER formatą sugeneruoto dokumento glaudinimui.

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš pabaigdami šiame straipsnyje nurodytas procedūras, turite atlikti šiuos veiksmus.

1. [Aktyvuoti konfigūracijos tiekėją](er-defer-xml-element.md#activate-a-configuration-provider).
2. [Importuoti pavyzdines ER konfigūracijas](er-defer-xml-element.md#import-the-sample-er-configurations).
3. [Peržiūrėti importuotą formatą](er-defer-xml-element.md#review-the-imported-format).

> [!NOTE]
> Šiuo metu formato struktūra prasideda nuo **Failo** tipo elemento **Ataskaita**, kuriame yra XML elementų. Todėl siunčiamas dokumentas bus sugeneruotas XML formatu ir nebus naudojamas joks glaudinimas.

### <a name="generate-an-er-format-to-get-an-uncompressed-document"></a>ER formato generavimas nesuglaudinto dokumento gavimui

1. [Vykdykite importuotą formatą](er-defer-xml-element.md#run-the-imported-format).
2. Atkreipkite dėmesį, kad sugeneruoto dokumento dydis XML formatu yra 3 kilobaitų (KB).

    ![Nesuglaudinto siunčiamo dokumento peržiūra.](./media/er-compress-outbound-files1.png)

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

    ![Suglaudinto siunčiamo dokumento peržiūra.](./media/er-compress-outbound-files2.png)

> [!NOTE]
> Jei ER [paskirties vieta](electronic-reporting-destinations.md) yra konfigūruojama formato elementui, kuris generuoja išvestį (šiame pavyzdyje – **Ataskaitos** elementas), išvesties glaudinimas bus apeinamas.

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų (ER) paskirties vietos](electronic-reporting-destinations.md)

[XML elementų ER formatais vykdymo atidėjimas](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]