---
title: STARTSWITH ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama funkcija STARTSWITH Electronic Reporting (ER).
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 010646d2ab96d9a326ffb01c369726790b6377a6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287225"
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
