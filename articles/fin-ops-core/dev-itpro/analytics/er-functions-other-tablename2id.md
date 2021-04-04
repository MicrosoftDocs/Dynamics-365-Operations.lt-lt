---
title: TABLENAME2ID ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama TABLENAME2ID elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 49370af4ebb7552dd3aff4512890fd93fa67c72d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563275"
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