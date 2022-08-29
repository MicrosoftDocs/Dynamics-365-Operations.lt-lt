---
title: Duomenų rinkimo kategorijos ER funkcijų sąrašas
description: Šiame straipsnyje pateikiama informacija apie duomenų rinkimo funkcijas, kurias palaiko elektroninės ataskaitos (ER).
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: e01bed49646ffe344004f9eb51e9013e1b4c5430
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286156"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a>Duomenų rinkimo kategorijos ER funkcijų sąrašas

[!include [banner](../includes/banner.md)]

Naudojant modulio Elektroninės ataskaitos (ER) duomenų rinkimo funkcijas, atliekamos vykdomo ER formato skaičiavimo ir sumavimo operacijos pagal išvesties, kuri jau sugeneruota **teksto** arba **XML** formatu, duomenis. Šis metodas naudojamas norint pagerinti vykdomo ER formato našumą, įvesti bendrąsias sumas generuojamuose dokumentuose ir kitais tikslais. Šiame straipsnyje pateikiama šių funkcijų suvestinė.

## <a name="list-of-supported-functions"></a>Palaikomų funkcijų sąrašas

| Funkcija | Aprašymas |
|----------|-------------|
| [CollectedList](er-functions-datacollection-collectedlist.md) | Ši funkcija pateikia tipo *Įrašų sąrašas* reikšmę, kurioje yra sąrašas reikšmių, kurias pateikė formato elementų ypatybė **Surinktų duomenų rakto reikšmė** ir kurios buvo surinktos, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokumentas, ir kuri tenkina nurodytas sąlygas. Kiekvieną sąlygą sudaro raktų intervalas ir rakto reikšmė. |
| [CountIF](er-functions-datacollection-countif.md) | Ši funkcija pateikia tipo *Sveikasis skaičius* reikšmę, kuri nurodo formato elementų, surinktų, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, skaičių ir kuri tenkina nurodytą sąlygą. Sąlygą sudaro raktų intervalas ir rakto reikšmė. |
| [CountIFs](er-functions-datacollection-countifs.md) | Ši funkcija pateikia tipo *Sveikasis skaičius* reikšmę, kuri nurodo formato elementų, surinktų, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, skaičių ir kuri tenkina nurodytas sąlygas. Kiekvieną sąlygą sudaro raktų intervalas ir rakto reikšmė. |
| [FormatElementName](er-functions-datacollection-formatelementname.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, nurodančią dabartinio ER formato elemento pavadinimą. |
| [SumIF](er-functions-datacollection-sumif.md) | Ši funkcija pateikia tipo *Realusis skaičius* reikšmę, kuri nurodo reikšmių, kurias pateikė formato elementų susiejimai ir kurios buvo surinktos, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, sumą ir kuri tenkina nurodytą sąlygą. Sąlygą sudaro raktų intervalas ir rakto reikšmė. |
| [SumIFs](er-functions-datacollection-sumifs.md) | Ši funkcija pateikia tipo *Realusis skaičius* reikšmę, kuri nurodo reikšmių, kurias pateikė formato elementų susiejimai ir kurios buvo surinktos, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, sumą ir kuri tenkina nurodytas sąlygas. Kiekvieną sąlygą sudaro raktų intervalas ir rakto reikšmė. |

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)

[Elektroninių ataskaitų formulių kalba](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
