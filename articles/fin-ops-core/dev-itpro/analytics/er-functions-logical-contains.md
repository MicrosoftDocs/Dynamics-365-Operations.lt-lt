---
title: „CONTAINS” ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip „CONTAINS” elektroninė ataskaita (ER) funkcija yra naudojama.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: c1d2d761a38d0edfb9abd439e0f710b336f54927
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745430"
---
# <a name="contains-er-function"></a>„CONTAINS” ER funkcija

[!include [banner](../includes/banner.md)]

`CONTAINS` funkcija nustato, ar nurodytoje įvestyje yra nurodytas tekstas. Gražinama *Loginė reikšmė* **TRUE** vertės, jeigu nurodytoje įvestyje yra nurodytas tekstas. Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.

## <a name="syntax"></a>Sintaksė

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a>Argumentai

`input`: *Eilutė*

Tinkamas *Eilutė* tipo arba eilutės konstantos duomenų šaltinio elemento maršrutas, kurio vertė gali talpinti antrą argumentą.

`search text`: *Eilutė*

Tinkamas *Eilutė* duomenų tipo arba eilutės konstantos duomenų šaltinio elemento maršrutas, kurio vertė gali būti talpinama pirmame argumente.

## <a name="return-values"></a>Grįžties vertės

*Bulio logika*

Gaunama *Bulio logikos* reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Šią funkciją galima naudoti nurodant [FILTER](er-functions-list-filter.md) funkcijos sąlygos išraišką, kai aktualus susiejimas sukonfigūruotas [„Regulatory Configuration Services”](../../../finance/localizations/rcs-globalization-feature.md), kad pasiektumėte [Microsoft Dataverse](../data-entities/data-integration-cds.md). Priešingu atveju dizaino metu pateikiama išimtis. Gautame pranešime rekomenduojama naudoti [WHERE](er-functions-list-where.md) funkciją vietoje `FILTER` funkcijos.

## <a name="example-1"></a>1 pavyzdys

Išraiška `CONTAINS ("abc", "d")` grąžina **FALSE**, o išraiška `CONTAINS ("abc", "C")` grąžina **TRUE**.

## <a name="example-2"></a>2 pavyzdys

Išraiška `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` grąžina **TRUE**, jei vertė **Adresas** lauke **modelis** duomenų šaltinio yra eilutė **DEU**. Kitu atveju ji grąžina **FALSE**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Loginės funkcijos](er-functions-category-logical.md)
