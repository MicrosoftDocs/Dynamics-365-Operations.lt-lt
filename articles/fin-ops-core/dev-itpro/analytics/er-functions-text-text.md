---
title: TEXT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama TEXT elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 5da7375020be827f432ba97740da37abe48962fc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560066"
---
# <a name="text-er-function"></a>TEXT ER funkcija

[!include [banner](../includes/banner.md)]

`TEXT` funkcija grąžina nurodytą skaičių kaip *Eilutės* reikšmę, jį konvertavus į teksto eilutę, kuri formatuojama pagal dabartinio programos egzemplioriaus serverio lokalės parametrus.

## <a name="syntax"></a>Sintaksė

```vb
TEXT (number)
```

## <a name="arguments"></a>Argumentai

`number`: *Sveikasis* arba *Realusis*

Skaičius, kuris turi būti konvertuotas į teksto eilutę.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

*Realiojo skaičiaus* tipo reikšmių eilutės konvertavimas apribotas dviem skaičiais po kablelio.

## <a name="example"></a>Pavyzdys

Jei „Microsoft Dynamics 365 Finance“ egzemplioriaus serverio lokalė apibrėžta kaip **EN-US**, `TEXT (NOW ())` grąžina dabartinę Finansų seanso datą, pvz., 2015 m. gruodžio 17 d., kaip teksto eilutę **„2015-12-17 07:59:23“**. `TEXT (1/3)` grąžina **„0,33“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]