---
title: GETENUMVALUEBYNAME ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama GETENUMVALUEBYNAME elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 4ded0c62b4556b21e731cd9b98db2863ec6ec442
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916849"
---
# <a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER funkcija</a>

[!include [banner](../includes/banner.md)]

`GETENUMVALUEBYNAME`funkcija ieško nurodytame išvardijimo duomenų šaltinyje konkrečios *Enum* reikšmės, naudodama išvardijimo pavadinimą, kuris nurodytas kaip *Eilutės* reikšmė. Jei *Enum* reikšmė randama, funkcija ją pateikia. Priešingu atveju funkcija grąžina **null** išvardijimo reikšmę.

## <a name="syntax"></a>Sintaksė

```
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Argumentai

`enumeration data source path`: *Išvardijimas*

Tinkamas vieno iš tolesnių išvardijimo tipų duomenų šaltinio maršrutas:

- Elektroninių ataskaitų (ER) modelių išvardijimas
- ER formatų išvardijimas
- „Microsoft Dynamics 365 Finance“ išvardijimas

`enumeration value text`: *Eilutė*

Eilutės reikšmė, nurodanti vienos išvardijimo reikšmės pavadinimą.

## <a name="return-values"></a>Grįžimo vertės

*Išvard.* leidžiama reikšmė NULL

Gaunama išvardijimo reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Nėra pateikiama jokia išimtis, jei reikšmė *Enum* nerasta naudojant išvardijimo reikšmę, nurodytą kaip *Eilutės* reikšmė.

## <a name="example"></a>Pavyzdys

Tolesnėje iliustracijoje duomenų modelyje įvestas išvardijimas **ReportDirection**. Atkreipkite dėmesį, kad išvardijimo reikšmėms nurodytos žymos.

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Tolesnėje iliustracijoje parodyta tolesnė išsami informacija.

- Duomenų šaltinis **$Direction** sukonfigūruotas ER ataskaitoje. Šis duomenų šaltinis yra sukonfigūruotas pagal modelių išvardijimą **ReportDirection**.
- Išraiška `$IsArrivals` sukurta naudoti modelių išvardijime veikiantį duomenų šaltinį **$Direction** kaip šios funkcijos parametrą.
- Šios lyginamosios išraiškos reikšmė yra **TEISINGA**.

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)
