---
title: TABLENAME2ID ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama TABLENAME2ID elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: fe7ed336f2264e15e0a8a7305e1bcebb75b2cd07
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268063"
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

Šios funkcijos vykdymas gali turėti skirtingų rezultatų skirtinguose Microsoft Dynamics 365 finansų egzemplioriuose, net jei naudojamas tas pats įmonės pavadinimas.

## <a name="example"></a>Pavyzdys

`TABLENAME2ID ("Intrastat")` grąžina **1510**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kitos (konkrečios verslo srities) funkcijos](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
