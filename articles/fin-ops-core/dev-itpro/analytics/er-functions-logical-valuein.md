---
title: VALUEIN ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama VALUEIN elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 08/18/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f230b05cd88554d30106337ae3e3f684c958c76eaf8ad8eae0dceda53f0b6862
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729076"
---
# <a name="valuein-er-function"></a>VALUEIN ER funkcija

[!include [banner](../includes/banner.md)]

`VALUEIN` funkcija nustato, ar nurodyta įvestis atitinka bet kurią pateiktame sąraše nurodyto elemento reikšmę. Grąžinama *Bulio logikos* reikšmė **TEISINGA**, jei nurodyta įvestis sutampa su nurodytos išraiškos vykdymo rezultatu bent vienam nurodyto sąrašo įrašui. Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.

## <a name="syntax"></a>Sintaksė

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a>Argumentai

`input`: *Laukas*

Tinkamas *Įrašų sąrašo* tipo duomenų šaltinio elemento maršrutas. Šio elemento vertė bus sugretinta.

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

`list item expression`: *Bulio logika*

Tinkama sąlyginė išraiška nurodo išraišką, kuri nurodo vieną sugretinimui naudotiną konkretaus sąrašo lauką arba kurioje toks laukas yra.

## <a name="return-values"></a>Grįžties vertės

*Būlio logika*

Gaunama *Bulio logikos* reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Paprastai funkcija `VALUEIN` paverčiama sąlygų **OR** rinkiniu. Jei **ARBA** sąlygų sąrašas yra didelis, o maksimalus bendras SQL sakinio ilgis gali būti viršytas, apsvarstykite galimybę naudoti [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) funkciją.

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

Kai kuriais atvejais, ji gali būti paverčiama į duomenų bazės SQL sakinį naudojant `EXISTS JOIN` operatorių.

## <a name="example-1"></a>1 pavyzdys

Nustatote šį savo modelio susiejimo duomenų šaltinį **Sąrašas**, priklausantį tipui *Apskaičiuotasis laukas*. Šiame duomenų šaltinyje yra išraiška `SPLIT ("a,b,c", ",")`.

Kai duomenų šaltinis iškviečiamas, jei jis sukonfigūruotas kaip `VALUEIN ("B", List, List.Value)` išraiška, jis grąžinamas **TEISINGA**. Tokiu atveju funkcija `VALUEIN` paverčiama toliau nurodytu sąlygų rinkiniu: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, kai `("B" = "b")` lygu **TEISINGA**.

Kai duomenų šaltinis iškviečiamas, jei jis sukonfigūruotas kaip `VALUEIN ("B", List, LEFT(List.Value, 0))` išraiška, jis grąžinamas **KLAIDINGA**. Tokiu atveju `VALUEIN` funkcija paverčiama toliau nurodyta sąlyga: `("B" = "")` nelygu **TEISINGA**.

Viršutinė esant tokiai sąlygai įvesto teksto simbolių skaičiaus riba yra 32 768 simboliai. Todėl neturėtumėte kurti duomenų šaltinių, kuriuose vykdant galėtų būti viršijama ši riba. Tais atvejais, kai viršijama riba, programa sustabdoma ir pateikiama išimtis. Pavyzdžiui, ši situacija gali susiklostyti, jei duomenų šaltinis sukonfigūruojamas kaip `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, o sąrašuose **List1** ir **List2** yra didelis įrašų kiekis.

Kai kuriais atvejais funkcija `VALUEIN`, naudojantis operatoriumi `EXISTS JOIN`, paverčiama duomenų bazės išrašu. Tai įvyksta naudojantis funkcija  [`FILTER`](er-functions-list-filter.md) ir kai patenkinamos šios sąlygos:

- Funkcijos `VALUEIN`, kuria naudojantis pateikiamas įrašų sąrašas, duomenų šaltinio parinktis **ASK FOR QUERY** išjungta. Vykdant šį duomenų šaltinį nebus taikoma jokių papildomų sąlygų.
- Nesukonfigūruota jokių įdėtųjų funkcijos `VALUEIN`, kuria naudojantis pateikiamas įrašų sąrašas, duomenų šaltinio išraiškų.
- Funkcijos `VALUEIN` sąrašo elementas nurodo konkretaus duomenų šaltinio lauką, o ne jo išraišką ar metodą.

Apsvarstykite galimybę naudoti šią parinktį vietoj [`WHERE`](er-functions-list-where.md) funkcijos, aprašytos anksčiau šiame pavyzdyje.

## <a name="example-2"></a>2 pavyzdys

Apibrėžkite šiuos modelio susiejimo duomenų šaltinius:

- Duomenų šaltinis **In**, priklausantis tipui *Lentelės įrašai*. Šis duomenų šaltinis nurodo „Intrastat“ lentelę.
- Duomenų šaltinis **Port**, priklausantis tipui *Lentelės įrašai*. Šis duomenų šaltinis nurodo lentelę „IntrastatPort“.

Kai iškviečiamas duomenų šaltinis, kuris sukonfigūruotas kaip išraiška `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, sukuriamas SQL išrašas filtruotiems „Intrastat“ lentelės įrašams grąžinti.

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

Galutinis laukų **dataAreaId** SQL išrašas kuriamas naudojantis operatoriumi `IN`.

## <a name="example-3"></a>3 pavyzdys

Apibrėžkite šiuos modelio susiejimo duomenų šaltinius:

- Tipo *Apskaičiuotasis laukas* duomenų šaltinis **Le**. Šiame duomenų šaltinyje yra išraiška `SPLIT ("DEMF,GBSI,USMF", ",")`.
- Duomenų šaltinis **In**, priklausantis tipui *Lentelės įrašai*. Šis duomenų šaltinis nurodo lentelę „Intrastat“, o parinktis **Kryžminė įmonė** yra įjungta.

Kai iškviečiamas duomenų šaltinis, kuris sukonfigūruotas kaip išraiška `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, galutiniame SQL yra toliau nurodyta sąlyga.

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a>Papildomi ištekliai

[Loginės funkcijos](er-functions-category-logical.md)

[VALUEINLARGE funkcijos](er-functions-logical-valueinlarge.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]