---
title: ER FORMATELEMENTNAME funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) FORMATELEMENTNAME funkcija.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 72977edfbe06e0d68d9226c9c25fa0633e7951d22438e053ae2a7cf4ef9a5848
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764494"
---
# <a name="formatelementname-er-function"></a>ER FORMATELEMENTNAME funkcija

[!include [banner](../includes/banner.md)]

`FORMATELEMENTNAME` funkcija pateikia tipo *Eilutė* reikšmę, nurodančią modulio Elektroninės ataskaitos (ER) dabartinio formato elemento pavadinimą.

## <a name="syntax"></a>Sintaksė

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a>Pateikiamos reikšmės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Šią funkciją galima iškviesti ER reiškiniuose, kurie buvo sukonfigūruoti ER grupės **Tekstas** formato komponento, esančio komponente **Common\\File**, kuriame įjungta parinktis **Rinkti išeigos informaciją**, ypatybėms **Surinktų duomenų rakto pavadinimas** ir **Surinktų duomenų rakto reikšmė**.

## <a name="example"></a>Pavyzdys

Norėdami apie tai, kaip naudoti šią funkciją, gauti daugiau informacijos, žr. užduočių vedlį [ER: duomenų formato išvesties duomenų naudojimas skaičiuojant ir sumuojant](tasks/er-format-counting-summing-1.md) (verslo proceso **Įsigyti / sukurti IT paslaugų ir sprendimų komponentų** dalis).

## <a name="additional-resources"></a>Papildomi ištekliai

[Duomenų rinkinio funkcijos](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]