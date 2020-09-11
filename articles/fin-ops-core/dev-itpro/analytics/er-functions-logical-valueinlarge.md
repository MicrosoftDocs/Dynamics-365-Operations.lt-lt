---
title: VALUEINLARGE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama VALUEINLARGE elektroninės ataskaitos (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 4630ec20e7cbca97c5e43093e6a888a5e09f41a3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705148"
---
# <a name="valueinlarge-er-function"></a>VALUEINLARGE ER funkcija

[!include [banner](../includes/banner.md)]

`VALUEINLARGE` funkcija nustato, ar nurodyta *Int64* arba *Sveikojo skaičiaus* tipo įvestis atitinka bet kurią pateiktame sąraše nurodytos prekės reikšmę. Ši funkcija grąžina *Bulio logikos* reikšmę **TEISINGA**, jei nurodyta įvestis sutampa su nurodyto reiškinio vykdymo rezultatu bent vienam pateikto sąrašo įrašui. Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**. Norėdami suprasti skirtumą su `VALUEIN` funkcija, žr. [Usage note](#usage_note) skyrių, esantį vėliau šioje temoje.

## <a name="syntax"></a>Sintaksė

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a>Argumentai

`input`: *Laukas*

Tinkamas *Įrašų sąrašo* tipo duomenų šaltinio elemento maršrutas. Šio elemento vertė bus sugretinta.

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

`list item expression`: *Išraiška*

Tinkama sąlyginė išraiška nurodo išraišką, kuri nurodo vieną sugretinimui naudotiną konkretaus sąrašo lauką arba kurioje toks laukas yra.

## <a name="return-values"></a>Grįžties vertės

*Bulio logika*

Gaunama *Bulio logikos* reikšmė.

## <a name=""></a><a name="usage_note">Naudojimo pastabos</a>

Kai nurodyta įvestis atitinka *Int64* arba *Sveikojo skaičiaus* tipo duomenų šaltinio prekę ir kalbą, kuri gali būti konvertuojama į tiesioginį SQL sakinį, pateiktas sąrašas konvertuojamas į laikinąją SQL lentelę, o gretinimas yra atliekamas duomenų bazėje vykdant vieną `EXISTS JOIN` užklausą. Kitu atveju ši funkcija veikia kaip [`VALUEIN`](er-functions-logical-valuein.md) funkcija.

Kai nurodyta įvestis atitinka duomenų šaltinio prekę, kuri sukurta ne kaip *Int64* ir *Sveikojo skaičiaus* tipo prekė, kūrimo laiku įvyksta klaida, informuojanti, kad `VALUEINLARGE` funkcija netaikoma sukonfigūruotai ER išraiškai.

Kai vykdoma funkcijos `VALUEINLARGE` išraiška ir šioje vykdymo apimtyje naudojama daugiau nei viena laikina lentelė, įvyksta vykdymo klaida.

## <a name="example"></a>Pavyzdys

Apibrėžkite šiuos modelio susiejimo duomenų šaltinius:

- Duomenų šaltinis**In**, priklausantis tipui *Lentelės įrašai*.
    - Šis duomenų šaltinis nurodo **Intrastat** lentelę.
    - **Visos įmonės** pasirinktis nustatoma kaip **Ne**.
- *Apskaičiuotojo lauko* tipo duomenų šaltinis **InMemory**.
    - Šiame duomenų šaltinyje yra išraiška `WHERE (In, In.Port <> "")`.
- *Apskaičiuotojo lauko* tipo duomenų šaltinis **InFiltered**.
    - Šiame duomenų šaltinyje yra išraiška `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.

Kai duomenų šaltinis **InFiltered** traktuojamas įmonės **DEMF** kontekste, programos duomenų bazėje sukuriama nauja laikina lentelė, į kurią įterpiamas įrašo identifikacijos kodų atminties sąrašas ir sugeneruojamas šis SQL sakinys, kad būtų grąžinti filtruoti **Intrastat** lentelės įrašai.

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a>Papildomi ištekliai

[Loginės funkcijos](er-functions-category-logical.md)

[VALUEIN funkcijos](er-functions-logical-valuein.md)
