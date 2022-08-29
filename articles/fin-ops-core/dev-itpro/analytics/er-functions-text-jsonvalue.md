---
title: JSONVALUE ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama JSONVALUE elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 10/25/2021
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
ms.openlocfilehash: fba1141bce91fd7c9da3cd21aef13ce99329f379
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267970"
---
# <a name="jsonvalue-er-function"></a>JSONVALUE ER funkcija

[!include [banner](../includes/banner.md)]

`JSONVALUE` funkcija analizuojami duomenys „JavaScript Object Notation“ (JSON) formatu, kuris pasiekiamas nurodytu keliu bei norint išskleisti skaliarinę vertę, turinčią nurodytą ID. Tada grąžinama išskleista skaliarinė reikšmė kaip *Eilutės* reikšmė.

## <a name="syntax"></a>Sintaksė

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Argumentai

`input`: *Eilutė*

Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas, kuriame yra JSON duomenų.

`path`: *Eilutė*

Skaliarinės reikšmės JSON duomenų identifikatorius. Norėdami atskirti susijusių JSON mazgų pavadinimus, naudokite pasvirą brūkšnį (/). Naudoti laužtiniais (\[\]) skliaustais nurodymą, kad būtų nurodytas konkrečios vertės indeksas JSON masyve. Atkreipkite dėmesį, kad šiame indekse naudojamas nulinis numeravimas.

## <a name="return-values"></a>Grįžimo vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="example-1"></a>1 pavyzdys

Duomenų šaltinyje **JsonField** yra toliau nurodyti duomenys JSON formatu: **{„BuildNumber“:„7.3.1234.1“, „KeyThumbprint“:„7366E“}**. Tokiu atveju išraiška `JSONVALUE (JsonField, "BuildNumber")` grąžina šią *Eilutės* duomenų tipo reikšmę: **„7.3.1234.1“**.

## <a name="example-2"></a>2 pavyzdys

Įvedate tipo *Apskaičiuotas laukas* duomenų šaltinį **JsonField** ir jame yra reiškinys tolesnė išraiška: `"{""workers"": [ {""name"": ""Adam"", ""age"": 30, ""emails"": [""AdamS@Contoso.com"", ""AdamS@Hotmail.com"" ]}, { ""name"": ""John"", ""age"": 21, ""emails"": [""JohnS@Contoso.com"", ""JohnS@Aol.com""]}]}"`

Ši išraiška sukonfigūruota grąžinti [*eilutės*](er-formula-supported-data-types-primitive.md#string) vertę, kuri nurodo šiuos duomenis JSON formatu.

```json
{
    "workers": [
        {
            "name": "Adam",
            "age": 30,
            "emails": [ "AdamS@Contoso.com", "AdamS@Hotmail.com" ]
        },
        {
            "name": "John",
            "age": 21,
            "emails": [ "JohnS@Contoso.com", "JohnS@Aol.com" ]
        }
    ]
}
```

Tokiu atveju išraiška `JSONVALUE(json, "workers/[1]/emails/[0]")` grąžina šią *Eilutės* duomenų tipo reikšmę: `JohnS@Contoso.com`.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
