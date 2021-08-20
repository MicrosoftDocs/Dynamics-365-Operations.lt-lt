---
title: Neautomatinis nusidėvėjimas
description: Šiame straipsnyje apžvelgtas rankinis nusidėvėjimo metodas.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 444506bdbf33cb1bd05ae7b55f2059e0eb1ab5b136e8fb1adb6f9e5f53b7067c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743030"
---
# <a name="manual-depreciation"></a>Neautomatinis nusidėvėjimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje apžvelgtas rankinis nusidėvėjimo metodas.

Kai nustatote ilgalaikio turto nusidėvėjimo šabloną ir puslapio **Nusidėvėjimo profiliai** lauke **Metodas** pasirenkate **Rankinis**, ilgalaikio turto, priskirto nusidėvėjimo šablonui, nusidėvėjimas nustatomas pagal kiekviename kalendorinių metų intervale įvestą procentinį dydį. Intervalai, kurių procentinius dydžius nustatote, registruojami atsižvelgiant į reikšmę, kurią pasirenkate **Laikotarpio dažnio** lauke, esančiame „FastTab‟ **Bendra**, **Nusidėvėjimo profilių** puslapyje. Čia nurodytos reikšmės, kurias galite pasirinkti.

-   Kasmet
-   Mėnesinis
-   Kas ketvirtį
-   Kas pusę metų
-   Kasdien

Pasirinkę laikotarpio dažnį, spustelėkite **Rankiniu būdu sudaryti grafikai** ir nustatykite kiekvieno registravimo intervalo procentinius dydžius. Veikdami kartu, rankiniu būdu sudarytas grafikas ir registravimo intervalas apibrėžia nusidėvėjimo sumą, kaip parodyta vėliau šiame straipsnyje pateikiamuose pavyzdžiuose. Rankinis nusidėvėjimas visuomet skaičiuojamas kaip įsigijimo kainos procentinis dydis. Procentiniai dydžiai, kuriuos įvedate rankiniu būdu nustatomo nusidėvėjimo intervaluose, neprivalo sudaryti 100 procentų. Rankinis nusidėvėjimas yra lankstus nusidėvėjimo metodas, kuris dažnai naudojamas norint puslapyje **Knygos** nurodyti visiško nusidėvėjimo šabloną, pavyzdžiui, specialiais tikslais (pavyzdžiui, mokesčių) nustatyti neperiodinį nusidėvėjimą.

## <a name="examples"></a>Pavyzdžiai
Įsigijimo kaina: 11 000,00 Numatyta nurašymo vertė: 1 000,00 Toliau pateikiamoje lentelėje rodomi intervalai ir procentiniai dydžiai, kuriuos nustatote **Ilgalaikio turto nusidėvėjimo profilių grafikų** puslapyje.

| Intervalo numeris | Procentai |
|-----------------|------------|
| 1               | 10,00      |
| 2               | 50,00      |
| 3               | 8,00       |

Toliau pateikiamoje lentelėje rodoma, kaip skaičiuojamas kiekvieno intervalo nusidėvėjimas.

|  Intervalo numeris | Metinio nusidėvėjimo sumos skaičiavimas | Balansinė vertė intervalo pabaigoje |
|------------------|-----------------------------------------------|-------------------------------------------|
| 1                | (11 000 – 1 000) × 10 % = 1 000                | 10 000 (11 000 – 1 000)                   |
| 2                | (11 000 – 1 000) × 50 % = 5 000                | 5 000 (10 000 – 5 000)                    |
| 3                | (11 000 – 1 000) × 8 % = 800                   | 4 200 (5 000 – 800)                       |

Jeigu lauke **Laikotarpio dažnis** pasirenkate **Kas mėnesį**, nustatote 12 rankinių grafikų intervalų. Toliau pateikiamoje lentelėje rodomos pirmųjų dviejų intervalų nusidėvėjimo sumos.

| Intervalas | Nusidėvėjimo suma            |
|----------|--------------------------------|
| sausio  | (11 000 – 1 000) × 10 % = 1 000 |
| Vasaris | (11 000 – 1 000) × 50 % = 5 000 |

Jeigu *lauke <strong><em>Laikotarpio dažnis</em>*</strong> pasirenkate <strong>Kas pusmetį</strong>, nustatote du rankinių grafikų intervalus. Toliau pateikiamoje lentelėje rodomos tų dviejų intervalų nusidėvėjimo sumos.

| Intervalas    | Nusidėvėjimo suma            |
|-------------|--------------------------------|
| Birželio 30 d.     | (11 000 – 1 000) × 10 % = 1 000 |
| Gruodžio 31 d. | (11 000 – 1 000) × 50 % = 5 000 |

Bendra procentinių dydžių suma neturi būti 100. Tačiau, jei reikšmė lauke **Sukaupti procentai**, esančiame puslapyje **Ilgalaikio turto nusidėvėjimo profilių grafikų**, nėra **100**, gaunate pranešimą.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]