---
title: ER ORDERBY funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) ORDERBY funkcija.
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
ms.openlocfilehash: a6aed53dcad6d402fc2ca61ae0687016cdb3af5b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916205"
---
# <a name="ORDERBY">ER ORDERBY funkcija</a>

[!include [banner](../includes/banner.md)]

`ORDERBY` funkcija nurodytą sąrašą pateikia kaip tipo *Įrašų sąrašas* reikšmę, jį surikiavus pagal nurodytus argumentus. Šiuos argumentus galima apibrėžti kaip išraiškas.

## <a name="syntax"></a>Sintaksė

```
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

`expression 1`: *Laukas*

Tinkamas duomenų šaltinio lauko kelias, kurį nurodo iškviestos funkcijos `list` argumentas. Nurodytas laukas turi būti primityviojo duomenų tipo. Šis argumentas yra būtinas.

`expression N`: *Laukas*

Tinkamas duomenų šaltinio lauko kelias, kurį nurodo iškviestos funkcijos `list` argumentas. Nurodytas laukas turi būti primityviojo duomenų tipo. Šie papildomi argumentai yra pasirinktiniai.

## <a name="return-values"></a>Pateikiamos reikšmės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="example-1"></a>1 pavyzdys

Jei įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("C|B|A", "|")`, reiškinys `FIRST( ORDERBY( DS, DS. Value)).Value` pateikia teksto reikšmę **„A“**.

## <a name="example-2"></a>2 pavyzdys

Jei **Tiekėjas** sukonfigūruotas kaip modulio Elektroninės ataskaitos (ER) duomenų šaltinis, nurodantis lentelę VendTable, reiškinys `ORDERBY (Vendors, Vendors.'name()')` pateikia tiekėjų sąrašą, surikiuotą pagal pavadinimą didėjančia tvarka.

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)