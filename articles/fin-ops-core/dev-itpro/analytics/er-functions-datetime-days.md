---
title: ER DAYS funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DAYS funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 4f8c12a22f7654285d5598064473bf86689ed207
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916297"
---
# <a name="DAYS">DAYS ER funkcija</a>

[!include [banner](../includes/banner.md)]

`DAYS` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią dienų tarp pirmos nurodytos datos ir antros nurodytos datos skaičių.

## <a name="syntax"></a>Sintaksė

```
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a>Argumentai

`date 1`: *Data*

Datos reikšmė, nurodanti pradžios datą dienų skaičiui skaičiuoti.

`date 2`: *Data*

Datos reikšmė, nurodanti pabaigos datą dienų skaičiui skaičiuoti.

## <a name="return-values"></a>Pateikiamos reikšmės

*Sveikasis skaičius*

Gaunama skaitinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Kai pirmoji data yra vėlesnė nei antroji, `DAYS` funkcija pateikia teigiamą reikšmę, kai pirmoji data sutampa su antrąja, ji pateikia **0** (nulį), o, kai pirmoji data yra ankstesnė nei antroji data, ji pateikia neigiamą reikšmę.

## <a name="example"></a>Pavyzdys

`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` pateikia **–1**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Datos ir laiko funkcijos](er-functions-category-datetime.md)