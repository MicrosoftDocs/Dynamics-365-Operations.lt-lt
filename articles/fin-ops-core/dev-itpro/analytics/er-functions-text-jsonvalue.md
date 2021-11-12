---
title: JSONVALUE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama JSONVALUE elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 10/25/2021
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
ms.openlocfilehash: ff33098e5be4dd9748d01d45b596360617305724
ms.sourcegitcommit: f8b597b09157d934b62bd5fb9a4d05b8f82b5a0e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/26/2021
ms.locfileid: "7700068"
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
