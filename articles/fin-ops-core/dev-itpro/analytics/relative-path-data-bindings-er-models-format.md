---
title: Santykinio kelio naudojimas ER modelių ir formatų duomenų sąsajose
description: Naudodami elektroninių ataskaitų įrankį vartotojai nustatote elektroninio formato struktūras ir tada aprašote, kaip šias struktūras reikia pildyti.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 321a85c675439b91b99ec5988494d7514a5c53f4
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093142"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a>Santykinio kelio naudojimas ER modelių ir formatų duomenų sąsajose

[!include[banner](../includes/banner.md)]

Naudodami elektroninių ataskaitų (ER) įrankį vartotojai gali nustatyti elektroninio formato struktūras ir tada aprašyti, kaip šias struktūras reikia pildyti naudojant programoje esančius duomenis ir algoritmus. Daugiau informacijos žr. [Elektroninių ataskaitų (ER) konfigūracijų kūrimas](electronic-reporting-configuration.md). Norėdami nurodyti duomenų srautą, kuriuo bus gaunami „Finance and Operations“ duomenys, ir jį naudoti generuodami elektroninį dokumentą, turite atlikti toliau nurodytus veiksmus.

- Susiekite sukonfigūruotus duomenų šaltinius su konkretaus domeno [duomenų modelio](general-electronic-reporting.md#data-model-and-model-mapping-components) elementais. Modelio struktūra ir pasirinkti duomenų šaltiniai gali būti sudėtingos hierarchinės struktūros dalys. Todėl galutinės sąsajos gali būti gana didelės ir jose gali būti daug skirtingų tipų elementų (pavyzdžiui, ryšių, lentelių ir metodų). Sąsajas gali tapti sunkiau skaityti ir gana sudėtinga peržiūrėti bei suprasti, ypač ne savininkams. 
- Susiekite duomenų modelio elementus su [formato](general-electronic-reporting.md#FormatComponentOutbound) komponentais, kad apibrėžtumėte, kokie duomenų modelio duomenys bus automatiškai įvedami generuojant formato išvestis.

Siekiant patobulinti ER susiejimo kūrimo įrankių naudojimą buvo įdiegta [santykinio kelio](er-formula-language.md#relative-path) funkcija. Pagal numatytuosius parametrus visuose naujuose programos egzemplioriuose, kuriuose yra įgalintos ER kūrimo funkcijos („Microsoft“ „Dynamics 365 Finance“, „Microsoft Regulatory Configuration Service“), santykinio kelio rodymo parinktis yra įjungta. Įdiegėme santykinio kelio parametrą, kad vartotojai dirbdami su šia ER sąsajų pateiktimi galėtų naudoti visą kelią.

[![Vartotojo parametrai](./media/relative-path-01.png)](./media/relative-path-01.png)

 
Įjungus santykinio kelio naudojimo parametrą, vienas simbolis @ pakeičia pirminio elemento kelią dabartinio modelio elemento sąsajoje. Visos sąsajos kelias tampa trumpesnis, todėl visą susiejimą galima aiškiau ir lengviau suprasti. Daugeliu atvejų norint peržiūrėti visas duomenų modelio sąsajas nereikia papildomai slinkti.

[![Modelių susiejimo kūrimo įrankis](./media/relative-path-02.png)](./media/relative-path-02.png)
 
Pradėjus kurti naują ER išraišką reikia įvesti tik vieną simbolį, norint apibrėžti sąsają su pirminio elemento lauku.

[![Formulės konstruktorius](./media/relative-path-03.png)](./media/relative-path-03.png)
 
Jei nusprendžiate pakeisti pirminio modelio elemento duomenų šaltinį, kuriam naudojamas absoliutusis kelias, turite rankiniu būdu iš naujo susieti šį modelio elementą, bei visus įdėtuosius elementus su nauju duomenų šaltiniu. Kai santykinio kelio naudojimo funkcija yra įjungta ir jūs pasirenkate naują duomenų šaltinį, kurį reikia susieti su pirminiu elementu, jums pasiūloma pasirinktis automatiškai vienu spustelėjimu iš naujo susieti visus įdėtuosius šio pirminio elemento elementus.

[![Pranešimas pakeisti esamą kelią](./media/relative-path-04.png)](./media/relative-path-04.png)
 
Jei patvirtinsite įdėtųjų elementų sąsają, naujas pirminis elementas bus įtrauktas į visų įdėtųjų elementų, kuriuose yra esamas pirminis elementas, kelią.
Ši funkcija nepažeidžia ER sistemos suderinamumo su ankstesnėmis versijomis. Visos anksčiau sukurtos ER konfigūracijos veiks naudojant šią naują funkciją. Jums nereikės atnaujinti versijos arba konvertuoti.

> [!NOTE]
> Visi pakeitimai, įdiegti masiškai modifikuojant įdėtųjų elementų sąsajas modelių susiejimuose, įrašomi konfigūracijos pokytyje (pakeitimų sekimas). Tai leidžia klientams pritaikyti išvestinę modelio susiejimo versiją bet kokiai naujai jo pagrindinei versijai, modifikuotai naudojant šią naują funkciją.

## <a name="additional-resources"></a>Papildomi ištekliai

[ER formulės kalba](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]