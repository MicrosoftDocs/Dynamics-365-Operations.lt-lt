---
title: SPLITLIST ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama SPLITLIST elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 03/15/2021
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
ms.openlocfilehash: 38ac7e6c6bdf53705d1374c173422f7347253a5f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292533"
---
# <a name="splitlist-er-function"></a>SPLITLIST ER funkcija

[!include [banner](../includes/banner.md)]

`SPLITLIST` funkcija skaido nurodytą sąrašą į antrinius sąrašus (arba į paketus), iš kurių kiekviename būtų nurodytas įrašų skaičius. Tada grąžinamas rezultatas kaip nauja *Įrašų sąrašo* reikšmė, kurią sudaro paketai.

## <a name="syntax-1"></a>Sintaksė 1

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a>Sintaksė 2

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

`number`: *Sveikasis*

Didžiausias įrašų skaičius vienam paketui.

`on-demand reading flag`: *Bulio logika*

*Boolean* logikos reikšmė, nurodanti, ar subsaplankių elementai turi būti generuojami pagal poreikį.

## <a name="return-values"></a>Grįžties vertės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="usage-notes"></a>Naudojimo pastabos

Grąžintame paketų sąraše yra šių elementų:

 - **Vertė:** *Sąrašas*

    Įrašų, priklausančių dabartiniam paketui, sąrašas.

- **BatchNumber:** *Sveikasis*

    Grąžinto sąrašo dabartinio paketo numeris.

Kai nustatyta skaitymo pagal poreikį žymė Teisinga, paantraštiniai sąrašai generuojami pagal užklausą, kuri leidžia sumažinti atminties suvartojimą, bet gali padidinti našumą, jei elementai nenaudojami **nuosekliai**.

## <a name="example"></a>Pavyzdys

Tolesnėje iliustracijoje duomenų šaltinis **Eilutės** sukurtas kaip įrašų sąrašas, turintis tris įrašus. Šis sąrašas suskirstytas į paketus, iš kurių kiekviename yra iki dviejų įrašų.

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Tolesnėje iliustracijoje parodytas sukurtas formato maketas. Šiame formato makete sukuriami susiejimai su duomenų šaltiniu **Eilutės**, siekiant generuoti išeigą XML formatu. Ši išeiga pateikia atskirus kiekvieno paketo ir jame esančių įrašų mazgus.

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas sukurtas formatas.

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
