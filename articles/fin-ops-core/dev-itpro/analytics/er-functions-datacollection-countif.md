---
title: ER COUNTIF funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) COUNTIF funkcija.
author: NickSelin
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: bebb3d3b810e68fa6a0d3f4deb92b750b7c9a9f3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755305"
---
# <a name="countif-er-function"></a>ER COUNTIF funkcija

[!include [banner](../includes/banner.md)]

`COUNTIF` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, kuri nurodo formato elementų, surinktų, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, skaičių ir kuri tenkina nurodytą sąlygą. Sąlygą sudaro raktų intervalas ir rakto reikšmė.

## <a name="syntax"></a>Sintaksė

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a>Argumentai

`condition range`: *Eilutė*

Reikšmė, kurią pateika reiškinys, sukonfigūruotas modulio Elektroninės ataskaitos (ER) formato komponento ypatybėje **Surinktų duomenų rakto pavadinimas**.

`condition value`: *Eilutė*

Reikšmė, kurią pateika reiškinys, sukonfigūruotas ER formato komponento ypatybėje **Surinktų duomenų rakto reikšmė**.

## <a name="return-values"></a>Pateikiamos reikšmės

*Sveikasis skaičius*

Gaunama skaitinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Ypatybes **Surinktų duomenų rakto pavadinimas** ir **Surinktų duomenų rakto reikšmė** galima sukonfigūruoti ER formato, esančio komponente **Common\\File**, kuriame įjungta parinktis **Rinkti išeigos informaciją**, komponentui **Seka** arba **XML elementas**.

Kai dabartinio komponento **Common\\File parinktis** **Rinkti išeigos informaciją** yra išjungta, ši funkcija pateikia **0** (nulio) reikšmę.

`condition range` argumente pakaitos simbolį **„\*“** galima naudoti norint vaizduoti kelis simbolius.

`condition value` argumente pakaitos simbolį **„\*“** galima naudoti norint vaizduoti kelis simbolius.

## <a name="example"></a>Pavyzdys

Norėdami apie tai, kaip naudoti šią funkciją, gauti daugiau informacijos, žr. užduočių vedlį [ER: duomenų formato išvesties duomenų naudojimas skaičiuojant ir sumuojant](tasks/er-format-counting-summing-1.md) (verslo proceso **Įsigyti / sukurti IT paslaugų ir sprendimų komponentų** dalis).

## <a name="additional-resources"></a>Papildomi ištekliai

[Duomenų rinkinio funkcijos](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]