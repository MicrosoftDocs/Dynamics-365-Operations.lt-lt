---
title: ER konfigūracijų kūrimas tam, kad sugeneruotuose failuose nebūtų rodomi KS simboliai
description: Šioje temoje paaiškinama, kaip konfigūruoti elektroninių ataskaitų (ER) formatą generuoti ataskaitoms, nerodančioms baitų eiliškumo žymos (KS) simbolių.
author: NickSelin
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9260db2edab75c9876ddf5af99bee4ff174c64e1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568978"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a>ER konfigūracijų kūrimas tam, kad sugeneruotuose failuose nebūtų rodomi KS simboliai

[!include [banner](../includes/banner.md)]

Galite sukurti [Elektroninių ataskaitų (ER)](general-electronic-reporting.md) [sprendimą](er-quick-start1-new-solution.md) siunčiamų dokumentų generavimui. Norint generuoti dokumentus kaip tekstinius arba XML failus, sprendimas turi apimti ER [konfigūraciją](general-electronic-reporting.md#Configuration) su ER [formato](general-electronic-reporting.md#FormatComponentOutbound) komponentu. Norint nurodyti [simbolio kodavimą](https://docs.microsoft.com/windows/win32/intl/character-sets), atitinkantį simbolių rinkinį sugeneruotuose failuose, ER formate turi būti **Bendra\\Failas** formato elementas. Norėdami konfigūruoti ER formato komponentą, atidarykite ER konfigūracijos [juodraščio](general-electronic-reporting.md#component-versioning) versiją ER formato dizaino įrankyje ir pridėkite **Bendra\\Failas** elementą. Lauke **Kodavimas** nurodykite siunčiamų failų, kurios generuojami vykdymo aplinkoje naudojant šį komponentą, kodavimą.

> [!NOTE]
> Jei formate yra neteisingas kodavimo pavadinimas, įrašant formato parametrų pakeitimus įvyksta klaida.

![Šakninio elemento pridėjimas Formato dizaino įrankio puslapyje](./media/er-suppress-bom-characters-image1.gif)

Jei kaip kodavimą nurodysite **„UTF-8”**, **„UTF-16”** arba **„UTF-32”**, parinktis **Nerodyti KS simbolių** taps galima. Nustatykite šią parinktį į **Taip** tam, kad [baitų eiliškumo žymos (KS) simboliai](https://docs.microsoft.com/globalization/encoding/byte-order-mark) būtų nerodomi siunčiamuose failuose, sugeneruotuose vykdymo aplinkoje, kai vykdomas redaguotinas ER formatas.

> [!NOTE]
> Jei paliksite lauką **Kodavimas** tuščią, bus naudojamas numatytasis **„UTF-8”** kodavimas.

![Parinkties Nerodyti KS simbolių nustatymas Formato dizaino įrankio puslapyje](./media/er-suppress-bom-characters-image2.gif)

Norėdami peržiūrėti funkciją vykdymo aplinkoje, atlikite atitinkamą procedūrą. Pavyzdžiui, atlikite temos [ER formato XML elementų vykdymo atidėjimas](er-defer-xml-element.md) veiksmus. Atlikę šios temos skyriaus [Suvestinės XML elemento vykdymo atidėjimas apskaičiuoto bendro skaičiaus panaudojimui](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) veiksmus, atlikite šiuos papildomus veiksmus.

1. UTF kodavimui nurodyti:

    1. Pasirinkite **Bendra\\Failas** tipo elementą **Ataskaita**.
    2. Lauke **Kodavimas** nurodykite **„UTF-8”** kodavimą.

2. XML failo su KS simboliais generavimui:

    1. Nustatykite parinktį **Nerodyti KS simbolių** į **Ne** tam, kad KS simboliai būtų įtraukti į sugeneruotus XML failus.
    2. Atlikite veiksmus, nurodytus temos [ER formato XML elementų vykdymo atidėjimas](er-defer-xml-element.md) skyriuje [Suvestinės XML elemento vykdymo atidėjimas apskaičiuoto bendro skaičiaus panaudojimui](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) ir įrašykite sugeneruotą failą kaip **„SampleXmlReport.xml”**.

3. XML failo be KS simbolių generavimui:

    1. Nustatykite parinktį **Nerodyti KS simbolių** į **Taip** tam, kad KS simboliai būtų nerodomi sugeneruotuose XML failuose.
    2. Atlikite veiksmus, nurodytus temos [ER formato XML elementų vykdymo atidėjimas](er-defer-xml-element.md) skyriuje [Suvestinės XML elemento vykdymo atidėjimas apskaičiuoto bendro skaičiaus panaudojimui](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) ir įrašykite sugeneruotą failą kaip **„SampleXmlReport (1).xml”**.

4. Failų lyginimo priemonėje palyginkite sugeneruotus failus.

    Pirmas skirtumas, kurį pastebėsite, yra failo antraštėje. Faile „SampleXmlReport.xml” yra KS simbolis, o faile „SampleXmlReport (1).xml” – nėra.

    ![Sugeneruotų failų palyginimas naudojant failų lyginimo priemonę](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a>Taip pat žiūrėkite

- [XML elementų ER formatais vykdymo atidėjimas](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]