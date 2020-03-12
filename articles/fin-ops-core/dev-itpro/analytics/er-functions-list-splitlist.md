---
title: SPLITLIST ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama SPLITLIST elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56ef02e3ea0ca2207ccdc79468a9ea4c1fbe8f95
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041888"
---
# <a name="SPLITLIST">SPLITLIST ER funkcija</a>

[!include [banner](../includes/banner.md)]

`SPLITLIST` funkcija skaido nurodytą sąrašą į antrinius sąrašus (arba į paketus), iš kurių kiekviename būtų nurodytas įrašų skaičius. Tada grąžinamas rezultatas kaip nauja *Įrašų sąrašo* reikšmė, kurią sudaro paketai.

## <a name="syntax"></a>Sintaksė

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

`number`: *Sveikasis*

Didžiausias įrašų skaičius vienam paketui.

## <a name="return-values"></a>Grįžimo vertės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="usage-notes"></a>Naudojimo pastabos

Grąžintame paketų sąraše yra šių elementų:

 - **Vertė:** *Sąrašas*

    Įrašų, priklausančių dabartiniam paketui, sąrašas.

- **BatchNumber:** *Sveikasis*

    Grąžinto sąrašo dabartinio paketo numeris.

## <a name="example"></a>Pavyzdys

Tolesnėje iliustracijoje duomenų šaltinis **Eilutės** sukurtas kaip įrašų sąrašas, turintis tris įrašus. Šis sąrašas suskirstytas į paketus, iš kurių kiekviename yra iki dviejų įrašų.

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Tolesnėje iliustracijoje parodytas sukurtas formato maketas. Šiame formato makete sukuriami susiejimai su duomenų šaltiniu **Eilutės**, siekiant generuoti išeigą XML formatu. Ši išeiga pateikia atskirus kiekvieno paketo ir jame esančių įrašų mazgus.

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas sukurtas formatas.

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)
