---
title: NUMERALSTOTEXT ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama NUMERALSTOTEXT elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 172693583699edfad7deeb16f8fc081abb6119d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287995"
---
# <a name="numeralstotext-er-function"></a>NUMERALSTOTEXT ER funkcija

[!include [banner](../includes/banner.md)]

`NUMERALSTOTEXT`f unkcija grąžina nurodytą skaičių kaip *Eilutės* reikšmę po to, kai ji buvo nurodyta žodžiais (t. y. konvertuota į teksto eilutes) pasirinkta kalba.

## <a name="syntax"></a>Sintaksė

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a>Argumentai

`number`: *Sveikasis* arba *Realusis*

Skaitinė reikšmė, nurodanti skaičių, kuris turi būti nurodytas žodžiais.

`language`: *Eilutė*

*Eilutės* reikšmė, nurodanti kalbos kodą.

`currency`: *Eilutė*

*Eilutės* reikšmė, nurodanti valiutos kodą.

`print currency name flag`: *Bulio logika*

*Bulio logikos* reikšmė, nurodanti, ar į nurodytų žodžiais skaičių tekstą reikia įtraukti naują valiutos pavadinimą.

`decimal points`: *Sveikasis*

*Sveikojo skaičiaus* reikšmė, nurodanti skaičių po kablelio, kurį nurodytų žodžiais skaičių tekstas turėtų pateikti.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Kalbos kodas nėra būtinas. Jei nurodomas kaip tuščia eilutė, naudojamas vykdomo konteksto kalbos kodas. Numatytasis kalbos kodas yra **EN-US**. Vykdomo konteksto kalbos kodas apibrėžiamas veikiančios elektroninių ataskaitų (ER) formato elemente **Aplankas** arba **Failas**.

Valiutos kodas nėra būtinas. Jei nurodomas kaip tuščia eilutė, naudojama vykdomo konteksto įmonės valiuta.

> [!NOTE] 
> Argumentai `print currency name flag`ir `decimal points` analizuojami tik šiais kalbos kodais : **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, ir **RU**. Be to, argumentas `print currency name flag` analizuojamas tik įmonėms, kurių šalies arba regiono kontekste palaikomas valiutos pavadinimų linksniavimas.

## <a name="example-1"></a>1 pavyzdys

`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` grąžina **„One Thousand Two Hundred Thirty Four and 56“**.

## <a name="example-2"></a>2 pavyzdys

`NUMERALSTOTEXT (120, "PL", "", false, 0)` grąžina **„sto dwadzieścia“**. 

## <a name="example-3"></a>3 pavyzdys

`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` grąžina **„сто двадцать евро 21 евроцент“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
