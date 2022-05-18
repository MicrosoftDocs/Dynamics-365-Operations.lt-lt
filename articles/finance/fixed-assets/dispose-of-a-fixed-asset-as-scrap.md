---
title: Nurašyto ilgalaikio turto likvidavimas
description: Temoje aprašomas procesas, kurio metu šalinamos nurašyto ilgalaikio turto, kuris buvo likviduotas, operacijos.
author: moaamer
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: c30837da84bff67bbab80ff5116135e2533a867d
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713084"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a>Nurašyto ilgalaikio turto likvidavimas

[!include [banner](../includes/banner.md)]

Temoje aprašomas procesas, kurio metu šalinamos nurašyto ilgalaikio turto, kuris buvo likviduotas, operacijos. Operacijų, kurias galima pašalinti, tipai apima turto įsigijimo ir sukaupto nusidėvėjimo operacijas bei kitas ilgalaikio turto operacijas. Šių operacijų panaikinimas paveikia balanso sąskaitas, pvz., įsigijimo koregavimą, nusidėvėjimo koregavimą, perkainojimą, vertės padidinimo ir vertės sumažinimo sąskaitas.

| Operacija                                         | Debetas (Dr.) | Kreditas (Kr.) |
|-----------------------------------------------------|-------------|--------------|
| Dr. sukauptas nusidėvėjimas                        | X           |              |
| Kr. ilgalaikio turto pelnas/nuostolis                          |             | X            |
| Dr. ilgalaikio turto pelnas/nuostolis                          | X           |              |
| Kr. ilgalaikio turto įsigijimo sąskaitos                 |             | X            |
| Dr. ilgalaikio turto pelnas/nuostolis (balansinė vertė \[NBV\]) | X           |              |
| Kr. ilgalaikio turto pelnas/nuostolis (NBV)                    |             | X            |

> [!NOTE]
> Rekomenduojame glaudžiai bendradarbiauti su savo įmonės vyriausiuoju finansininku (CFO) arba kontrolieriumi, kad būtų galima nustatyti teisingas sąskaitas, naudojamas kiekvienam operacijos tipui, taip pat įsitikinti, kad likvidavimo procesas ir generuojamos operacijos tinkamai naujina šias sąskaitas.

Prieš nurašyto ilgalaikio turto likvidavimą, turite sukurti DK sąskaitas, susietas su turto įsigijimo verte, šių metų nusidėvėjimą, praėjusių metų nusidėvėjimą ir turto NBV. Ilgalaikio turto operacijų tipai pateikiami puslapyje **Ilgalaikio turto registravimo šablonas**. Eikite į **Ilgalaikis turtas \> Sąranka \> Ilgalaikio turto registravimo šablonai**, o tada, „FastTab” konteineryje **Likvidavimas** lauke virš tinklelio pasirinkite **Nurašyta**. Toliau pateiktame paveikslėlyje parodytas ilgalaikio turto operacijų tipų sąrašas puslapyje **Ilgalaikio turto registravimo šablonai**.


[![Nurašyto turto likvidavimas, 1 iliustracija.](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)

Toliau pateiktame pavyzdyje ilgalaikis turtas buvo įsigytas 2018 m. sausio 1 d. ir jis bus nurašytas 2019 m. kovo 31 d.

- **Įsigijimo kaina:** 24 000,00 JAV doleriai (USD)
- **Dėvėjimo laikas:** dveji metai
- **Nusidėvėjimo metodas:** tiesiogiai proporcingas dėvėjimo laikas
- **Nusidėvėjimo suma:** 1 000,00 USD per mėnesį

Ilgalaikio turto NBV apskaičiuojama pagal toliau nurodytą formulę.

Balansinė vertė = įsigijimo kaina – nusidėvėjimas

Šiame pavyzdyje ilgalaikis turtas buvo įsigytas ir dėvėtas 15 mėnesių, nuo 2018 m. sausio mėn. iki 2019 m. kovo mėn. Todėl turto NBV yra 9 000,00 USD (24 000,00 USD – 15 000,00 USD).

[![Ilgalaikio turto nusidėvėjimo pavyzdžiai.](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)


Norėdami sukurti likvidavimo žurnalą, eikite į **Ilgalaikis turtas \> Žurnalo įrašai \> Ilgalaikio turto žurnalas**, tada veiksmų srityje pasirinkite **Eilutės**. Pasirinkite **Likvidavimas – nurašymas** ir pasirinkite ilgalaikio turto ID. Norėdami visiškai likviduoti turtą, neįveskite vertės į lauką **Debetas** arba į lauką **Kreditas** .

[![Ilgalaikio turto žurnalas.](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)

Nurašyto ilgalaikio turto likvidavimo operacija pakeičia ilgalaikio turto knygos laukų vertes toliau nurodytais būdais.

- Skyriuje **Balansas**, laukas **Būsena** atnaujinamas į **Nurašyta**.
- Skyriuje **Išdavimas**, laukas **Likvidavimo data** nustatomas į datą, kada turtas buvo nurašytas.

[![Ilgalaikio turto žurnalo informacija.](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)

Toliau pateiktame paveikslėlyje parodytas ilgalaikio turto balansas.

[![Ilgalaikio turto balansas.](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)

Toliau pateiktame paveikslėlyje parodytas užregistruotas kvitas.

[![Balansinė knygos vertė.](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
