---
title: CASE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CASE elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 69b76a06bcd3ba002d9543447e60afa14d5a6ce6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687031"
---
# <a name="case-er-function"></a>CASE ER funkcija

[!include [banner](../includes/banner.md)]

`CASE` funkcija įvertina nurodytos išraiškos reikšmę pagal nurodytas alternatyvias parinktis ir grąžina pirmosios parinkties, kuri yra lygi nurodytos išraiškos vertei, rezultatą. Kitu atveju ji grąžina pasirenkamą numatytąjį rezultatą, jei numatytasis rezultatas yra nurodytas kaip paskutinis iškviestos funkcijos argumentas, prieš kurį nėra parinkties. Grąžinama reikšmė gali būti bet kurių palaikomo duomenų tipų reikšmė.

## <a name="syntax"></a>Sintaksė

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a>Argumentai

`expression`: *Primityvusis duomenų tipas* (Bulio logikos, skaitinis arba tekstinis)

Tinkama išraiška, grąžinanti primityviojo duomenų tipo reikšmę.

`option 1`: *Primityvusis duomenų tipas* (Bulio logikos, skaitinis arba tekstinis)

Tinkama išraiška, kuri grąžina to paties primityviojo duomenų tipo reikšmę kaip iškvietos `expression` funkcijos argumentą. Šis argumentas yra būtinas.

`result 1`: *Bet kuris iš palaikomų duomenų tipų*

Grąžintas rezultatas, atitinkantis ankstesnę parinktį. Šis argumentas yra būtinas.

`option N`: *Primityvusis duomenų tipas* (Bulio logikos, skaitinis arba tekstinis)

Tinkama išraiška, kuri grąžina to paties primityviojo duomenų tipo reikšmę kaip iškvietos `expression` funkcijos argumentą. Šis argumentas yra pasirinktinis.

`result N`: *Bet kuris iš palaikomų duomenų tipų*

Grąžintas rezultatas, atitinkantis ankstesnę parinktį. Šis argumentas yra pasirinktinis.

`default result`: *Bet kuris iš palaikomų duomenų tipų*

Rezultatas, kuris turėtų būti grąžintas, jei nėra atitikmens. Šis argumentas yra pasirinktinis.

## <a name="return-values"></a>Grįžties vertės

*Bet kuris iš palaikomų duomenų tipų*

Gauta bet kurio palaikomų duomenų tipo reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Vykdymo metu pateikiama išimtis, jei nėra atitikmens ir pasirinktinis numatytasis rezultatas nėra apibrėžtas.

Visi rezultatai ir turi būti nurodyti naudojant tą patį duomenų tipą. Jei sukonfigūruotų rezultatų duomenų tipai nesutampa, kūrimo metu pateikiama išimtis.

Jei pirmasis rezultatas ir *N*-tasis rezultatas yra duomenų tipo *Konteineris (įrašas)* arba *Įrašų sąrašas* reikšmės, rezultatai apima tik tuos laukus, kurie yra abiejose reikšmėse.

## <a name="example"></a>Pavyzdys

`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")`grąžina eilutę **„ŽIEMA“**, jei dabartinė programos seanso data yra nuo spalio iki gruodžio mėn. Kitu atveju pateikia tuščią eilutę.

## <a name="additional-resources"></a>Papildomi ištekliai

[Loginės funkcijos](er-functions-category-logical.md)
