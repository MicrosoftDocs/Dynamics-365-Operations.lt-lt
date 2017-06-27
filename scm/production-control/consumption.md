---
title: "Medžiagų suvartojimo apskaičiavimas"
description: "Šiame straipsnyje pateikiama informacija apie įvairias parinktis, susijusias su medžiagų suvartojimo skaičiavimu."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1bd3168e80719c86e9a0541200fdb1608410c8f5
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="calculate-material-consumption"></a>Medžiagų suvartojimo apskaičiavimas

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikiama informacija apie įvairias parinktis, susijusias su medžiagų suvartojimo skaičiavimu. 

**Sąrankos** ir **Žingsnio vartojimo** skirtukuose **Linijos duomenys** „FastTab“ skirtuke **Medžiagų kiekių sąraše** yra šie variantai, susiję su medžiagų suvartojimo apskaičiavimais.

## <a name="variable-and-constant-consumption"></a>Kintamas ir pastovus vartojimas
Lauke **Vartojimas** galite pasirinkti, ar sąnaudos bus apskaičiuojamos kaip pastovus, ar kintamas kiekis. Pasirinkite **Pastovus**, jei gamybai reikalingas fiksuotas kiekis ar visa apimtis, nepriklausomai nuo pagaminamos produkcijos kiekio. Pasirinkite **Kintamas**, kuris yra numatytasis parametras, jei gatavoms prekėms reikalingas kiekis medžiagų yra proporcingas pagamintai produkcijai.

## <a name="calculating-consumption-from-a-formula"></a>Suvartojimo apskaičiavimas iš formulės
**Formulės** lauke galite nustatyti įvairias formules apskaičiuoti medžiagų sąnaudoms. Jei naudojate numatytąją vertę, **Standartinis**, vartojimas pagal formulę neskaičiuojamas. Kartu su laukais **Aukštis**, **Plotis**, **Gylis**, **Tankis**, ir **Nuolatinis** taikomos šios formulės:

-   Aukštis \* Konstanta
-   Aukštis \* Plotis \* Konstanta
-   Aukštis \* Plotis \* Gylis \* Konstanta
-   (Aukštis \* Plotis \* Gylis / Tankis) \* Konstanta

## <a name="rounding-up-and-multiples"></a>Suapvalina ir daugina
Taip pat **Apvalinimo** ir **Dauginimo** laukuose galite suapvalinti medžiagų sąnaudų vertę. Pavyzdžiui, galite suapvalinti vertę pagal padalinį, kuriame žaliava imama gamybai. **Suapvalinimo** lauke yra šie variantai: **Kiekis**, **Matavimas**, ir **Suvartojimas**.

### <a name="quantity"></a>Kiekis

Jei suapvalinimui pasirinksite **Kiekis**, tai kiekis bus konkretaus kiekio kartotinis. Pavyzdžiui, kai reikia sveikų skaičių, lauke **Kartotiniai** nurodykite **1**. Tada skaičiai apvalinami iki kiekio, kuris dalinasi iš 1.

### <a name="measurement"></a>Matavimo vienetas

Paprastai apvalinimui pasirenkamas **Matavimas**, kai žaliava tiekiama konkrečiais kiekiais. Pavyzdžiui, gatavam gaminiui reikia 2 metrų metalinio vamzdžio gabalo, o sandėlyje yra 4,5 metrų ilgio metaliniai vamzdžiai. Šiuo atveju galima naudoti **Matavimo** apvalinimo mechanizmą apskaičiuoti, kiek reikės metalinių vamzdžių pagaminti tam tikrą skaičių gatavų gaminių. Šiame pavyzdyje laukas **Formulė** yra nustatytas į **Aukštis \* Konstanta**. Laukas **Aukštis** yra nustatytas į **2**, siekiant nurodyti vamzdžio ilgį, reikalingą baigtai prekei. **Dauginimo** laukas yra nustatytas **4,5** nurodant, kad imamas 4,5 metrų ilgio vamzdis. Štai skaičiavimas:

1.  Kartotiniai, reikalingi 10 vienetų gatavų gaminių gamybai: 10 ÷ 2 = 5 vnt.
2.  Iš viso sąnaudos: 4,5 × 5 = 22,5 metrų metalinio vamzdžio

Laikoma, kad kiekvieniems penkiems gabalams sunaudojamo vamzdžio 0,5 metrų vamzdžio išmetama į metalo laužą.

### <a name="consumption"></a>Sunaudojimas

Paprastai kaip suapvalinimo mechanizmas pasirenkamas**Suvartojimas** kai žaliava konkretaus gaminio gamybai imama sveikais kiekiais. Pavyzdžiui, vienam gaminiui pagaminti sunaudojamos 2 kvortos dažų, o dažai yra 25 kvortų skardinėse. Šiuo atveju gali būti naudojamas **Suvartojimo** apvalinimo mechanizmas suapvalinti suvartojimą iki sveikų 25 kvortų skardinių skaičių. Štai kaip apskaičiuojamas dažų kiekis, kurio reikia pagaminti 180 vienetų gatavų gaminių:

1.  Reikalingi dažai, išskyrus atliekas: 180 × 2 = 360 kvortų
2.  Skardinių skaičius: 360 ÷ 25 = 14,4, kuris apvalinamas iki 15
3.  Reikalingi dažai su atliekomis: 15 × 25 = 375 kvortų

## <a name="step-consumption"></a>Pakopinis vartojimas
Vartojimas žingsniais naudojamas apskaičiuoti pastovų vartojimą kiekio intervalais. Pasirinkus **Vartojimą žingsniai**s **Formulės** srityje iš **Sąrankos** skirtuko, galite pridėti informaciją apie žingsnius **Vartojimo žingsniais** skirtuke. Fiksuotą suvartotą kiekį galima nustatyti intervalais pagal pagamintą kiekį. Pavyzdžiui, vartojimas žingsniais yra nustatytas taip, kaip parodyta toliau pateiktoje lentelėje.

| Serija Nuo | Kiekis |
|-------------|----------|
| 0,00        | 10.0000  |
| 100,00      | 20.0000  |
| 200,00      | 40.0000  |

Medžiagų kiekių suvestinėje (KS) nurodytas kiekis yra 1, o pagamintas kiekis yra 110. Suvartojimo formulė „Iš serijos“ (Kiekis) = Suvartojimas. Kadangi pagamintas kiekis yra 110, jis patenka į „Iš 100 serijos“. Todėl kiekis yra 20.




