---
title: ER SUMIF funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) SUMIF funkcija.
author: NickSelin
ms.date: 04/27/2020
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
ms.openlocfilehash: 8721e0115ab3c5ebe3071fe0b9ca5a80db766b0878d886b186f3f3d39f4a6397
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747622"
---
# <a name="sumif-er-function"></a>ER SUMIF funkcija

[!include [banner](../includes/banner.md)]

`SUMIF` funkcija pateikia tipo *Realusis skaičius* reikšmę, kuri nurodo reikšmių, kurias pateikė formato elementų susiejimai ir kurios buvo surinktos, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, sumą ir kuri tenkina nurodytą sąlygą. Sąlygą sudaro raktų intervalas ir rakto reikšmė.

## <a name="syntax"></a>Sintaksė

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a>Argumentai

`key name for summing`: *Eilutė*

Reikšmė, kurią pateikia reiškinys, sukonfigūruotas modulio Elektroninės ataskaitos (ER) formato komponento, kuriam sumavimo tikslais reikia naudoti susiejimo reikšmę, ypatybėje **Surinktų duomenų rakto pavadinimas**.

Ypatybę **Surinktų duomenų rakto reikšmė** galima sukonfigūruoti ER formato, esančio komponente **Common\\File**, kuriame įjungta parinktis **Rinkti išeigos informaciją**, komponentui **Seka** arba **XML elementas**.

## <a name="return-values"></a>Pateikiamos reikšmės

*Tikrasis*

Gaunama skaitinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Kai dabartinio komponento **Common\\File parinktis** **Rinkti išeigos informaciją** yra išjungta, ši funkcija pateikia **0** (nulio) reikšmę.

`condition range` argumente pakaitos simbolį **„\*“** galima naudoti norint vaizduoti kelis simbolius.

`condition value` argumente pakaitos simbolį **„\*“** galima naudoti norint vaizduoti kelis simbolius.

## <a name="example"></a>Pavyzdys

Norėdami apie tai, kaip naudoti šią funkciją, gauti daugiau informacijos, žr. užduočių vedlį [ER: duomenų formato išvesties duomenų naudojimas skaičiuojant ir sumuojant](tasks/er-format-counting-summing-1.md) (verslo proceso **Įsigyti / sukurti IT paslaugų ir sprendimų komponentų** dalis).

Daugiau informacijos ir funkcijos naudojimo pavyzdžių žr. [Sekos elementų ER formatais vykdymo atidėjimas](er-defer-sequence-element.md#Example) ir [XML elementų ER formatais vykdymo atidėjimas](er-defer-xml-element.md#Example).

## <a name="additional-resources"></a>Papildomi ištekliai

[Duomenų rinkinio funkcijos](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]