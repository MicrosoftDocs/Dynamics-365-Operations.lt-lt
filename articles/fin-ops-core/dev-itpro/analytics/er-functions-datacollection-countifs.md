---
title: ER COUNTIFS funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) COUNTIFS funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: 5bc0beb20f600afdea2d58187dd2a9c26a775ec1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561332"
---
# <a name="countifs-er-function"></a>ER COUNTIFS funkcija

[!include [banner](../includes/banner.md)]

`COUNTIFS` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, kuri nurodo formato elementų, surinktų, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, skaičių ir kuri tenkina nurodytas sąlygas. Kiekvieną sąlygą sudaro raktų intervalas ir rakto reikšmė.

## <a name="syntax"></a>Sintaksė

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a>Argumentai

`condition 1 range`: *Eilutė*

Reikšmė, kurią pateika reiškinys, sukonfigūruotas modulio Elektroninės ataskaitos (ER) formato komponento ypatybėje **Surinktų duomenų rakto pavadinimas**. Šis argumentas yra privalomas.

`condition 1 value`: *Eilutė*

Reikšmė, kurią pateika reiškinys, sukonfigūruotas ER formato komponento ypatybėje **Surinktų duomenų rakto reikšmė**. Šis argumentas yra privalomas.

`condition N range`: *Eilutė*

Reikšmė, kurią pateika reiškinys, sukonfigūruotas ER formato komponento ypatybėje **Surinktų duomenų rakto pavadinimas**. Šie papildomi argumentai yra pasirinktiniai.

`condition N value`: *Eilutė*

Reikšmė, kurią pateika reiškinys, sukonfigūruotas ER formato komponento ypatybėje **Surinktų duomenų rakto reikšmė**. Šie papildomi argumentai yra pasirinktiniai.

## <a name="return-values"></a>Pateikiamos reikšmės

*Sveikasis skaičius*

Gaunama skaitinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Ypatybes **Surinktų duomenų rakto pavadinimas** ir **Surinktų duomenų rakto reikšmė** galima sukonfigūruoti ER formato, esančio komponente **Common\\File**, kuriame įjungta parinktis **Rinkti išeigos informaciją**, komponentui **Seka** arba **XML elementas**.

Kai dabartinio komponento **Common\\File parinktis** **Rinkti išeigos informaciją** yra išjungta, ši funkcija pateikia **0** (nulio) reikšmę.

`condition range` argumentuose pakaitos simbolį **„\*“** galima naudoti norint vaizduoti kelis simbolius.

`condition value` argumentuose pakaitos simbolį **„\*“** galima naudoti norint vaizduoti kelis simbolius.

## <a name="example"></a>Pavyzdys

Norėdami apie tai, kaip naudoti šią funkciją, gauti daugiau informacijos, žr. užduočių vedlį [ER: duomenų formato išvesties duomenų naudojimas skaičiuojant ir sumuojant](tasks/er-format-counting-summing-1.md) (verslo proceso **Įsigyti / sukurti IT paslaugų ir sprendimų komponentų** dalis).

## <a name="additional-resources"></a>Papildomi ištekliai

[Duomenų rinkinio funkcijos](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]