---
title: GETLABELTEXT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama elektroninių ataskaitų teikimo (ER) funkcija GETLABELTEXT.
author: NickSelin
ms.date: 01/04/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 911567a94b80c2b762a37e83d37fc500132edb18
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075755"
---
# <a name="getlabeltext-er-function"></a>GETLABELTEXT ER funkcija

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

The`GETLABELTEXT` funkcija ieško konkrečios etiketės, kad grąžintų a *[Styga](er-formula-supported-data-types-primitive.md#string)* reikšmė, kuri reiškia nurodytos etiketės vertimą nurodyta kalba.

## <a name="syntax"></a>Sintaksė

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>Argumentai

### <a name="label-id"></a>Žymės kodas

`label id`:*Styga* arba *Etiketės ID*

Vieno iš šių etikečių tipų galiojantis ID:

- [Elektroninis ataskaitų teikimas (ER)](general-electronic-reporting.md) etiketė
- Microsoft Dynamics 365 Finance etiketė

#### <a name="usage-notes"></a>Naudojimo pastabos

Šis argumentas gali būti apibrėžtas tik kaip konstanta, naudojant vieną iš šių palaikomų šablonų:

- ER etiketėms:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- Finansų etiketės:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> Projektavimo metu ekrane rodomas patvirtinimo klaidos pranešimas **[Formulės dizaineris](er-advanced-formula-editor.md)** puslapį, jei naudojant pateiktą etiketės ID nepavyksta rasti etiketės.

### <a name="language"></a>Kalba

`language`: *Eilutė*

Eilutė, nurodanti kalbos kodą.

#### <a name="usage-notes"></a>Naudojimo pastabos

Šis argumentas gali būti apibrėžtas kaip teksto konstanta arba kaip duomenų šaltinio lauko, kuris grąžina a, kelias *Styga* vertė.

> [!NOTE]
> Projektavimo metu parodomas patvirtinimo klaidos pranešimas, jei naudojant pateiktą kalbos kodą nepavyksta rasti`language` argumentas, kai jis buvo apibrėžtas kaip teksto konstanta.
>
> Vykdymo metu vertimas`EN-US` Sistemos kalba grąžinama nurodytai etiketei, jei naudojant pateiktą kalbos kodą nerasta`language` argumentas.

## <a name="return-values"></a>Grįžimo vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="example-1-system-label"></a><a name=example-1></a> 1 pavyzdys: sistemos etiketė

Išraiškos`GETLABELTEXT (@"SYS70894", "en-us")` ir`GETLABELTEXT ("SYS70894", "en-us")` grąžinkite vertimą į anglų kalbą „Nieko spausdinti“.`@SYS70894` programos etiketė.

## <a name="example-2-er-label"></a><a name=example-2></a> 2 pavyzdys: ER etiketė

Pradedate redaguoti ER [konfigūracija](general-electronic-reporting.md#Configuration) tai buvo [išvestinė](er-quick-start2-customize-report.md#DeriveProvidedFormat) nuo **ISO20022 kredito pervedimas (DE)** konfigūraciją, įveskite naują duomenų šaltinį *[Apskaičiuotas laukas](er-calculated-field-ds-performance.md)* įveskite ir sukonfigūruokite išraišką`GETLABELTEXT(@"GER_LABEL:VendorName", "de")` šiam duomenų šaltiniui. Šiuo atveju vykdymo metu duomenų šaltinis pateikia vokišką vertimą „Kreditorenname“.`@GER_LABEL:VendorName` ER etiketė, kuri iš pradžių buvo sukonfigūruota bazėje **ISO20022 kredito pervedimas (DE)** ER konfigūracija.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)

[Daugiakalbių pranešimų Elektroninėse ataskaitose kūrimas](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
