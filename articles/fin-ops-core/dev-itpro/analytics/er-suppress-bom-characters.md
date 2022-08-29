---
title: ER konfigūracijų kūrimas tam, kad sugeneruotuose failuose nebūtų rodomi KS simboliai
description: Šiame straipsnyje paaiškinama, kaip konfigūruoti elektroninių ataskaitų (ER) formatą ataskaitoms, kurios sulaikyti pagal užsakymo žymę (KS), generuoti.
author: kfend
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: EROperationDesigner
ms.openlocfilehash: a2ea132b51f2f451fbe81a9c7869bea84bf4017a
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324026"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a>ER konfigūracijų kūrimas tam, kad sugeneruotuose failuose nebūtų rodomi KS simboliai

[!include [banner](../includes/banner.md)]

Galite sukurti [Elektroninių ataskaitų (ER)](general-electronic-reporting.md) [sprendimą](er-quick-start1-new-solution.md) siunčiamų dokumentų generavimui. Norint generuoti dokumentus kaip teksto arba XML failus, sprendimas turi apimti ER [konfigūraciją](general-electronic-reporting.md#Configuration), kurioje yra ER formato komponentas. Norint nurodyti [simbolio kodavimą](/windows/win32/intl/character-sets), atitinkantį simbolių rinkinį sugeneruotuose failuose, ER formate turi būti **Bendra\\Failas** formato elementas. Norėdami konfigūruoti ER formato komponentą, ER formato konstruktoriuje atidarykite ER konfigūracijos juodraščio versiją ir įtraukite bendrosios **rinkmenos\\** elementą. Lauke **Kodavimas** nurodykite siunčiamų failų, kurios generuojami vykdymo aplinkoje naudojant šį komponentą, kodavimą.

> [!NOTE]
> Jei formate yra neteisingas kodavimo pavadinimas, įrašant formato parametrų pakeitimus įvyksta klaida.

![Šakninio elemento pridėjimas Formato dizaino įrankio puslapyje.](./media/er-suppress-bom-characters-image1.gif)

Jei kaip kodavimą nurodysite **„UTF-8”**, **„UTF-16”** arba **„UTF-32”**, parinktis **Nerodyti KS simbolių** taps galima. Nustatykite šią parinktį į **Taip** tam, kad [baitų eiliškumo žymos (KS) simboliai](/globalization/encoding/byte-order-mark) būtų nerodomi siunčiamuose failuose, sugeneruotuose vykdymo aplinkoje, kai vykdomas redaguotinas ER formatas.

> [!NOTE]
> Jei paliksite lauką **Kodavimas** tuščią, bus naudojamas numatytasis **„UTF-8”** kodavimas.

![Parinkties Nerodyti KS simbolių nustatymas Formato dizaino įrankio puslapyje.](./media/er-suppress-bom-characters-image2.gif)

Norėdami peržiūrėti funkciją vykdymo aplinkoje, atlikite atitinkamą procedūrą. Pvz., atlikite veiksmus, nurodytą [XML elementų vykdymo atidėjime ER formatų straipsnyje](er-defer-xml-element.md). Atlikę formato modifikavimo veiksmus, [kad](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) skaičiavimas būtų paremtas sugeneruota to straipsnio išvesties sekcija, atlikite šiuos papildomus veiksmus.

1. UTF kodavimui nurodyti:

    1. Pasirinkite **Bendra\\Failas** tipo elementą **Ataskaita**.
    2. Lauke **Kodavimas** nurodykite **„UTF-8”** kodavimą.

2. XML failo su KS simboliais generavimui:

    1. Nustatykite parinktį **Nerodyti KS simbolių** į **Ne** tam, kad KS simboliai būtų įtraukti į sugeneruotus XML failus.
    2. Atlikite [veiksmus, nurodytus suvestinės XML](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used)[elemento vykdymo atidėjimas, kad apskaičiuota suma būtų naudojama XML elementų vykdymo atidėjimo ER](er-defer-xml-element.md) formatų straipsnyje skyriuje, ir įrašykite sugeneruotą failą kaip **SampleXmlReport.xml**.

3. XML failo be KS simbolių generavimui:

    1. Nustatykite parinktį **Nerodyti KS simbolių** į **Taip** tam, kad KS simboliai būtų nerodomi sugeneruotuose XML failuose.
    2. Atlikite [veiksmus, nurodytus suvestinės XML](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used)[elemento vykdymo atidėjimas, kad apskaičiuota suma būtų naudojama XML elementų vykdymo atidėjimo ER](er-defer-xml-element.md) formatų straipsnyje sekcijoje, **ir įrašykite sugeneruotą failą kaip SampleXmlReport (1).xml**.

4. Failų lyginimo priemonėje palyginkite sugeneruotus failus.

    Pirmas skirtumas, kurį pastebėsite, yra failo antraštėje. Faile „SampleXmlReport.xml” yra KS simbolis, o faile „SampleXmlReport (1).xml” – nėra.

    ![Sugeneruotų failų palyginimas naudojant failų lyginimo priemonę.](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a>Taip pat žiūrėkite

- [XML elementų ER formatais vykdymo atidėjimas](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
