---
title: SPLITLISTBYLIMIT ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama SPLITLISTBYLIMIT elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: d43ca9bd33cf21a0d72e407317088c9703bbf303
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271680"
---
# <a name="splitlistbylimit-er-function"></a>SPLITLISTBYLIMIT ER funkcija

[!include [banner](../includes/banner.md)]

`SPLITLISTBYLIMIT` funkcija išskaido nurodytą sąrašą į naują antrinių sąrašų (paketų) sąrašą. Kiekvieno paketo įrašų skaičius yra dinamiškai apskaičiuojamas. Tada funkcija grąžina rezultatą kaip naują *Įrašų sąrašo* reikšmę, kurią sudaro paketai.

## <a name="syntax"></a>Sintaksė

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

`limit value`: *Sveikasis* arba *Realusis*

Didžiausia ribos vertė, naudojama norint suskaidyti pradinį sąrašą į paketus.

`limit source`: *Laukas*

Tinkamas *sveikojo skaičiaus* arba *realiojo skaičiaus* tipo lauko maršrutas nurodytame sąraše. Šio lauko reikšmė apibrėžia veiksmą, kad bendroji suma padidinama.

## <a name="return-values"></a>Grįžties vertės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="usage-notes"></a>Naudojimo pastabos

Grąžintame paketų sąraše yra šių elementų:

- **Vertė**: *Sąrašas*

    Įrašų, priklausančių dabartiniam paketui, sąrašas.

- **BatchNumber**: *Sveikasis*

    Grąžinto sąrašo dabartinio paketo numeris.

Riba netaikoma vienam pradinio sąrašo elementui, jei ribos šaltinis viršija nustatytą ribą.

## <a name="example"></a>Pavyzdys

Tolesnėje iliustracijoje parodytas elektroninis ataskaitų (ER) formatas.

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

Tolesnėje iliustracijoje parodyti formatui naudojami duomenų šaltiniai.

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas formatas. Šiuo atveju išeiga yra standartinis prekių sąrašas.

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

Toliau pateiktose iliustracijose rodomas tas pats formatas, pakoreguotas norint pateikti prekių sąrašą paketais, jei viename pakete turi būti prekės, o bendrasis svoris negali viršyti ribos 9.

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas pakoreguotas formatas.

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> Riba nėra taikoma paskutinei pradinio sąrašo prekei, nes ribos šaltinio (**svorio**) reikšmė (**11**) viršija nustatytą ribą (**9**). Norėdami ignoruoti antrinius sąrašus generuojant ataskaitą, pagal poreikį naudokite funkciją `WHERE` arba atitinkamo formato elemento išraišką **Įjungta**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
