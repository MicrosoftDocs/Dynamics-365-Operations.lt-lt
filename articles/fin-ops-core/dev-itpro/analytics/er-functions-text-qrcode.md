---
title: QRCODE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama QRCODE elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: bac0910d213ee05a2a7a7b218a6714d4f935be16
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916757"
---
# <a name="QRCODE">QRCODE ER funkcija</a>

[!include [banner](../includes/banner.md)]

`QRCODE` funkcija grąžina *konteinerio* reikšmę, kuri pateikia nurodytą eilutę dvejetainiu formatu kaip greito atsakymo kodo (QR kodą) atvaizdą.

## <a name="syntax"></a>Sintaksė

```
QRCODE (text)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

*Eilutės* reikšmė, nurodanti pradinį tekstą.

## <a name="return-values"></a>Grįžties vertės

*Konteineris*

Gautas dvejetainis srautas.

## <a name="example"></a>Pavyzdys

Galite sukonfigūruoti elektroninių ataskaitų (ER) formatą, kad sugeneruotumėte siunčiamą dokumentą „Microsoft Office“ formatu („Excel“ darbaknygės arba „Word“ dokumentai), naudodami iš anksto nustatytą šabloną. Šiame šablone gali būti **Paveikslėlio** objektas („Excel“ darbaknygė) arba **Paveikslėlio turinio valdiklis** („Word“ dokumentas) kaip QR kodo atvaizdo vietos rezervavimo ženklas. Jums reikia pridėti prie sukonfigūruoto ER formato **langelio** elementą, kuris bus naudojamas užpildyti šį vietos rezervavimo ženklą. Norėdami nurodyti, kokia informacija bus saugoma QR kodu, turite nustatyti šio **langelio** elemento susiejimą. Pavyzdžiui, galite sukonfigūruoti tokį susiejimą, kuriame yra ši išraiška:

```
QRCODE (model.ListOfShelfLabels.LabelText)`
```

Kai paleidžiate sukonfigūruotas ER formatą, **LabelText** lauko, priklausančio duomenų šaltiniui **model.ListOfShelfLabels**, teksto reikšmės bus naudojama generuoti QR kodo atvaizdą. Šis paveikslėlis pakeis QR kodo atvaizdo vietos rezervavimo ženklą dokumento šablone, naudodamas siuntimo dokumento generavimui. Kai nuskaitomas šis sugeneruoto dokumento vaizdas, jis grąžina tekstą, paimtą iš lauko **LabelText**, priklausančio duomenų šaltiniui **model.ListOfShelfLabels**. Daugiau informacijos žr. [Vaizdų ir figūrų įterpimas generuojamuose dokumentuose naudojant ER](electronic-reporting-embed-images-shapes.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)
