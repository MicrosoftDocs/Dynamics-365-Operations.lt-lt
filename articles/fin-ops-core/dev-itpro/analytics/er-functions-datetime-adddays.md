---
title: ER ADDDAYS funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) ADDDAYS funkcija.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd1290538c506cd0db6eb21a304ff9812c808f17
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916458"
---
# <a name="ADDDAYS">ER ADDDAYS funkcija</a>

[!include [banner](../includes/banner.md)]

`ADDDAYS` funkcija apskaičiuoja *DateTime* reikšmę, kuri yra nurodytas dienų skaičius prieš nurodytą pradžios datą arba po jos.

## <a name="syntax"></a>Sintaksė

```
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
