---
title: GETLABELTEXT ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama GETLABELTEXT Electronic reporting (ER) funkcija.
author: kfend
ms.date: 03/18/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: dad87548518b77f2def1cf2383a21607f45170e1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285946"
---
# <a name="getlabeltext-er-function"></a>GETLABELTEXT ER funkcija

[!include [banner](../includes/banner.md)]

Funkcija `GETLABELTEXT` ieško konkrečios žymės, kad būtų grąžinama eilutės *[...](er-formula-supported-data-types-primitive.md#string)* vertė, nurodanti nurodytos žymės konvertavimą į nurodytą kalbą.

## <a name="syntax"></a>Sintaksė

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>Argumentai

### <a name="label-id"></a>Žymės kodas

`label id`: *eilutės* arba *žymės id*

Tinkamas vieno iš šių žymės tipų ID:

- [Elektroninių ataskaitų (ER)](general-electronic-reporting.md) žymė
- Microsoft Dynamics 365 finansų žyma

#### <a name="usage-notes"></a>Naudojimo pastabos

Šis argumentas gali būti apibrėžiamas tik kaip konstanta, naudojant vieną iš šių palaikomų šablonų:

- ER žymėse:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- Finansų žymų:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> Dizaino metu, formulės konstruktoriaus puslapyje rodomas **[...](er-advanced-formula-editor.md)** tikrinimo klaidos pranešimas, jei naudojant pateiktą žymės ID žymės nerasta jokios žymės.

### <a name="language"></a>Kalba

`language`: *Eilutė*

Eilutė, nurodanti kalbos kodą.

#### <a name="usage-notes"></a>Naudojimo pastabos

Šis argumentas gali būti apibrėžiamas kaip teksto konstanta arba kaip duomenų šaltinio lauko, kuris grąžina eilutės vertę *, maršrutas*.

> [!NOTE]
> Dizaino metu rodomas tikrinimo klaidos pranešimas `language`, jei jokio kalbos kodo negalima rasti naudojant pateiktą argumentą, kai jis apibrėžiamas kaip teksto konstanta.
>
> Vykdyklės metu sistemos kalbos vertimas `EN-US` grąžinamas pagal nurodytą žymę, jei kalbos kodas nerastas naudojant pateiktą argumentą `language`.

## <a name="return-values"></a>Grįžimo vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="example-1-system-label"></a><a name=example-1></a> 1 pavyzdys: Sistemos žyma

Išraiškos ir `GETLABELTEXT (@"SYS70894", "en-us")` programos `GETLABELTEXT ("SYS70894", "en-us")` žymės angliškas vertimas "Nėra ko spausdinti `@SYS70894` ".

## <a name="example-2-er-label"></a><a name=example-2></a> 2 pavyzdys: ER žymė

Pradedama redaguoti [ER](general-electronic-reporting.md#Configuration)[...](er-quick-start2-customize-report.md#DeriveProvidedFormat)**konfigūraciją, išvestą iš ISO20022 kredito perkėlimo (DE)** konfigūracijos, *[...](er-calculated-field-ds-performance.md)*`GETLABELTEXT(@"GER_LABEL:VendorName", "de")` įvesti naują apskaičiuoto lauko tipo duomenų šaltinį ir konfigūruoti šio duomenų šaltinio išraišką. Šiuo atveju apdorojimo metu duomenų šaltinis grąžina Vokietijos vertimą "Kreditorenname" `@GER_LABEL:VendorName` ER **žymai, kuri buvo iš pradžių sukonfigūruota bazinėje ISO20022 kredito pervedimo (DE)** ER konfigūracijoje.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)

[Daugiakalbių pranešimų Elektroninėse ataskaitose kūrimas](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
