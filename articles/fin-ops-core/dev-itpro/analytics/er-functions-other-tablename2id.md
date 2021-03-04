---
title: TABLENAME2ID ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama TABLENAME2ID elektroninių ataskaitų (ER) funkcija.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a68a8e1f4afa378ab446eae12bc90cdb3aba8b19
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681163"
---
# <a name="tablename2id-er-function"></a>TABLENAME2ID ER funkcija

[!include [banner](../includes/banner.md)]

`TABLENAME2ID` funkcija grąžina nurodyto lentelės pavadinimo lentelės ID skaitinį vaizdavimą kaip *sveikojo skaičiaus* reikšmę.

## <a name="syntax"></a>Sintaksė

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

Tekstinė reikšmė, nurodanti tinkamą lentelės pavadinimą.

## <a name="return-values"></a>Grįžties vertės

*Sveikasis skaičius*

Gaunama skaitinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Šios funkcijos atlikimas gali lemti skirtingus rezultatus skirtinguose „Microsoft Dynamics 365 Finance“ egzemplioriuose, net jei naudojamas tos pačios įmonės pavadinimas.

## <a name="example"></a>Pavyzdys

`TABLENAME2ID ("Intrastat")` grąžina **1510**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kitos (konkrečios verslo srities) funkcijos](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]