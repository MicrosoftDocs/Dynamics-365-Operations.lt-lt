---
title: STARTSWITH ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama funkcija STARTSWITH Electronic Reporting (ER).
author: NickSelin
ms.date: 02/11/2021
ms.prod: ''
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
ms.openlocfilehash: a9c22154484f9e98dbe101b5de0f539b2feb9865
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883733"
---
# <a name="startswith-er-function"></a>STARTSWITH ER funkcija

[!include [banner](../includes/banner.md)]

`STARTSWITH` funkcija nustato, ar nurodyta įvestis prasideda nurodytu tekstu. Gražinama *Loginė reikšmė* **TRUE** vertės, jeigu nurodyta įvestis prasideda nurodytu tekstu. Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.

## <a name="syntax"></a>Sintaksė

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a>Argumentai

`input`: *Eilutė*

Tinkamas *Eilutė* tipo arba eilutės konstantos duomenų šaltinio elemento maršrutas, kurio vertė gali prasidėti antru argumentu.

`start text`: *Eilutė*

Tinkamas *Eilutė* duomenų tipo arba eilutės konstantos duomenų šaltinio elemento maršrutas, kurio vertė gali prasidėti pirmo argumento pradžioje.

## <a name="return-values"></a>Grįžties vertės

*Bulio logika*

Gaunama *Bulio logikos* reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Šią funkciją galima naudoti nurodant [FILTER](er-functions-list-filter.md) funkcijos sąlygos išraišką, kai aktualus susiejimas sukonfigūruotas [„Regulatory Configuration Services”](../../../finance/localizations/rcs-globalization-feature.md), kad pasiektumėte [Microsoft Dataverse](/power-platform/admin/data-integrator). Priešingu atveju dizaino metu pateikiama išimtis. Gautame pranešime rekomenduojama naudoti [WHERE](er-functions-list-where.md) funkciją vietoje `FILTER` funkcijos.

## <a name="example-1"></a>1 pavyzdys

Išraiška `STARTSWITH ("abc", "d")` grąžina **FALSE**, o išraiška `STARTSWITH ("abc", "A")` grąžina **TRUE**.

## <a name="example-2"></a>2 pavyzdys

Išraiška `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` grąžina **TRUE**, jei vertė **Adresas** lauke **modelis** duomenų šaltinio prasideda **123 Coffee Street**. Kitu atveju ji grąžina **FALSE**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Loginės funkcijos](er-functions-category-logical.md)
