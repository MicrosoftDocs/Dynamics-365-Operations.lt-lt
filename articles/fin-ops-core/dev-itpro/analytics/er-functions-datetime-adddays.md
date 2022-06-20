---
title: ER ADDDAYS funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama ADDDAYS Electronic Reporting (ER) funkcija.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: 7cf2031c042ae93512cc85afe6a1b51558f6c8f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858747"
---
# <a name="adddays-er-function"></a>ER ADDDAYS funkcija

[!include [banner](../includes/banner.md)]

`ADDDAYS` funkcija apskaičiuoja *DateTime* reikšmę, kuri yra nurodytas dienų skaičius prieš nurodytą pradžios datą arba po jos.

## <a name="syntax"></a>Sintaksė

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>Argumentai

`datetime`: *DateTime*

Datos / laiko reikšmė, nurodanti pradžios datą.

`days`: *Sveikasis skaičius*

Dienų prieš `datetime` arba po jos skaičius.

## <a name="return-values"></a>Pateikiamos reikšmės

*Data ir laikas*

Gauta datos / laiko reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Teigiama `days` reikšmė pateikia būsimą datą. Neigiama reikšmė pateikia praeities datą.

## <a name="example-1"></a>1 pavyzdys

`ADDDAYS (NOW(), 7)` nukelia datą ir laiką septyniomis dienomis į ateitį.

## <a name="example-2"></a>2 pavyzdys

`ADDDAYS (NOW(), -3)` nukelia datą ir laiką trimis dienomis į praeitį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Datos ir laiko funkcijos](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]