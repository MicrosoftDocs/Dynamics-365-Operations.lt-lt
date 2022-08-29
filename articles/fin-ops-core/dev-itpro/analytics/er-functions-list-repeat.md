---
title: REPEAT ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudoti funkciją REPEAT Electronic Reporting (ER).
author: NickSelin
ms.date: 08/01/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-06-01
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: c56139a3c63b03f907b1dcbf4365990d2a13c35a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220726"
---
# <a name="repeat-er-function"></a>REPEAT ER funkcija

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Ši `REPEAT` funkcija sukuria įrašą, kuriame yra laukas, kurio vertė atitinka nurodytą įvestį. Tada grąžinamas naujas *įrašo* sąrašas, kuris kartojamas nurodytą kartų skaičių.

## <a name="syntax"></a>Sintaksė

```vb
REPEAT (item, number)
```

## <a name="arguments"></a>Argumentai

`item`: bet koks palaikomas [nesueitas ar](er-formula-supported-data-types-primitive.md) sudėtinis [duomenų](er-formula-supported-data-types-composite.md) tipas

Kartojimo vertė.

`number`: *Sveikasis*

Pakartotų skaičius.

## <a name="return-values"></a>Grįžimo vertės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="usage-notes"></a>Naudojimo pastabos

Grąžintų pasikartojančių įrašų sąrašas parodo šiuos laukus:

- Nurodyta vertė (`Item` laukas)
- Dabartinio įrašo indeksas (`Number` laukas)

> [!NOTE]
> Šiai funkcijai naudojamas vienas pagrįstas numeravimas, `Number` todėl **lauko vertė yra 1**, esanti pirmame gauto sąrašo įraše.

Šią funkciją [galite naudoti norėdami dauginti esamus duomenis, kad naudodami Regression komplektavimo automatizavimo įrankį (RSAT) būtų galima atlikti elektroninių ataskaitų (ER)](general-electronic-reporting.md)[sprendimų našumą ir tūrio bandymą](../perf-test/rsat/rsat-overview.md).

## <a name="example"></a>Pavyzdys

Norite generuoti dokumentą XML formatu, kuriame prieš prasidedant ER formato vykdymui dialogo lango duomenų įvedimo lauke turi būti tiek XML `Party` elementų, kiek nurodote.

Šioje iliustracijoje rodomas ER [formatas](er-overview-components.md#format-component). Šiuo formatu, pridedamas vienas `Party` XML elementas, kad būtų galima rodyti vienos šalies ypatybes.

<a href="./media/er-repeat-function-1.png"><img src="./media/er-repeat-function-1.png" alt="Format structure on the Format tab of the Format designer page." class="alignnone size-full" width="929" height="548" /></a>

Kitame pavyzdyje pateikti šie sukonfigūruoti duomenų šaltiniai:

- Duomenų `Party` šaltinis, nurodantis vieną šalį. Laukas `Party.Value` naudojamas norint rodyti vieną teksto vertę.
- Duomenų `NumberOfRepeats`[šaltinis](er-user-input-parameter-data-sources.md), naudojamas dialogo lange duomenų įvedimo laukui pasiūlyti apdorojimo laiku, kad būtų galima nurodyti šalių, kurios turėtų būti įvestos sugeneruotame dokumente, skaičių.
- Duomenų `Party2` šaltinis, kuris kartoti įrašą `Party`, kiek kartų nurodėte duomenų `NumberOfRepeats` šaltinyje.

<a href="./media/er-repeat-function-2.png"><img src="./media/er-repeat-function-2.png" alt="Configured data sources on the Mapping tab of the Format designer page." class="alignnone size-full" width="1044" height="411" /></a>

Kitas pavyzdys rodo redaguojamo ER formato duomenų susiejimus, kurie sukurti išeigai XML formatu generuoti. Ši išvestis pateikia atskiras šalis kaip išvardytas mazgus.

<a href="./media/er-repeat-function-3.png"><img src="./media/er-repeat-function-3.png" alt="Configured data bindings on the Mapping tab of the Format designer page." class="alignnone size-full" width="1051" height="417" /></a>

Toliau esanti iliustracija rodo rezultatą, kai paleistas sukurtas formatas ir nurodyta `NumberOfRepeats` duomenų šaltinio vertė **5**.

<a href="./media/er-repeat-function-4.png"><img src="./media/er-repeat-function-4.png" alt="Result of running the format on a new web browser tab." class="alignnone wp-image-290711 size-full" width="400" height="380" /></a>

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
