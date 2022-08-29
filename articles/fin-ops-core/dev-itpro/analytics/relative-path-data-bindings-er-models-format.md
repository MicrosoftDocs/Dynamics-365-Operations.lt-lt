---
title: Santykinio kelio naudojimas ER modelių ir formatų duomenų sąsajose
description: Naudodami elektroninių ataskaitų įrankį vartotojai nustatote elektroninio formato struktūras ir tada aprašote, kaip šias struktūras reikia pildyti.
author: kfend
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.search.form: ERSolutionTable, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
ms.openlocfilehash: 54fb7d488dff1ad36e2d44b8bb9e0fa3fce7ea1b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276569"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a>Santykinio kelio naudojimas ER modelių ir formatų duomenų sąsajose

[!include[banner](../includes/banner.md)]

Naudodami elektroninių ataskaitų (ER) įrankį vartotojai gali nustatyti elektroninio formato struktūras ir tada aprašyti, kaip šias struktūras reikia pildyti naudojant programoje esančius duomenis ir algoritmus. Daugiau informacijos žr. [Elektroninių ataskaitų (ER) konfigūracijų kūrimas](electronic-reporting-configuration.md). Norėdami nurodyti duomenų srautą finansų ir operacijų duomenims nuskaityti ir naudoti jį elektroniniam dokumentui generuoti, turite atlikti šiuos veiksmus:

- Susiekite sukonfigūruotus duomenų šaltinius su konkretaus domeno duomenų modelio elementais. Modelio struktūra ir pasirinkti duomenų šaltiniai gali būti sudėtingos hierarchinės struktūros dalys. Todėl galutinės sąsajos gali būti gana didelės ir jose gali būti daug skirtingų tipų elementų (pavyzdžiui, ryšių, lentelių ir metodų). Sąsajas gali tapti sunkiau skaityti ir gana sudėtinga peržiūrėti bei suprasti, ypač ne savininkams. 
- Susiekite duomenų modelio elementus su formato komponentais, kad apibrėžtumėte, kokie duomenų modelio duomenys bus automatiškai įvedami generuojant formato išvestis.

Siekiant patobulinti ER susiejimo kūrimo įrankių naudojimą buvo įdiegta [santykinio kelio](er-formula-language.md#relative-path) funkcija. Numatyta, kad susijusi maršruto pateikties parinktis įjungiama bet kuriam naujam programos egzemplioriui, kur įgalinta ER dizaino patirtis (Microsoft Dynamics 365 finansai, Microsoft reguliavimo konfigūravimo tarnyba). Įdiegėme santykinio kelio parametrą, kad vartotojai dirbdami su šia ER sąsajų pateiktimi galėtų naudoti visą kelią.

[![Vartotojo parametrai.](./media/relative-path-01.png)](./media/relative-path-01.png)

 
Įjungus santykinio kelio naudojimo parametrą, vienas simbolis @ pakeičia pirminio elemento kelią dabartinio modelio elemento sąsajoje. Visos sąsajos kelias tampa trumpesnis, todėl visą susiejimą galima aiškiau ir lengviau suprasti. Daugeliu atvejų norint peržiūrėti visas duomenų modelio sąsajas nereikia papildomai slinkti.

[![Modelių susiejimo kūrimo įrankis.](./media/relative-path-02.png)](./media/relative-path-02.png)
 
Pradėjus kurti naują ER išraišką reikia įvesti tik vieną simbolį, norint apibrėžti sąsają su pirminio elemento lauku.

[![Formulės konstruktorius.](./media/relative-path-03.png)](./media/relative-path-03.png)
 
Jei nusprendžiate pakeisti pirminio modelio elemento duomenų šaltinį, kuriam naudojamas absoliutusis kelias, turite rankiniu būdu iš naujo susieti šį modelio elementą, bei visus įdėtuosius elementus su nauju duomenų šaltiniu. Kai santykinio kelio naudojimo funkcija yra įjungta ir jūs pasirenkate naują duomenų šaltinį, kurį reikia susieti su pirminiu elementu, jums pasiūloma pasirinktis automatiškai vienu spustelėjimu iš naujo susieti visus įdėtuosius šio pirminio elemento elementus.

[![Pranešimas pakeisti esamą kelią.](./media/relative-path-04.png)](./media/relative-path-04.png)
 
Jei patvirtinsite įdėtųjų elementų sąsają, naujas pirminis elementas bus įtrauktas į visų įdėtųjų elementų, kuriuose yra esamas pirminis elementas, kelią.
Ši funkcija nepažeidžia ER sistemos suderinamumo su ankstesnėmis versijomis. Visos anksčiau sukurtos ER konfigūracijos veiks naudojant šią naują funkciją. Jums nereikės atnaujinti versijos arba konvertuoti.

> [!NOTE]
> Visi pakeitimai, įdiegti masiškai modifikuojant įdėtųjų elementų sąsajas modelių susiejimuose, įrašomi konfigūracijos pokytyje (pakeitimų sekimas). Tai leidžia klientams pritaikyti išvestinę modelio susiejimo versiją bet kokiai naujai jo pagrindinei versijai, modifikuotai naudojant šią naują funkciją.

## <a name="additional-resources"></a>Papildomi ištekliai

[ER formulės kalba](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

