---
title: Nusidėvėjimo faktorius
description: Šiame straipsnyje apžvelgiamas nusidėvėjimo pagal koeficientą metodas.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbac1d84654673b3746887d943c0ecb530be4ae3
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713168"
---
# <a name="factor-depreciation"></a>Nusidėvėjimo faktorius

[!include [banner](../includes/banner.md)]

Šiame straipsnyje apžvelgiamas nusidėvėjimo pagal koeficientą metodas.

Koeficientai yra turto nusidėvėjimo procentai. Kai nustatote ilgalaikio turto nusidėvėjimo profilį ir puslapio **Nusidėvėjimo šablonai** lauke **Metodas** pasirenkate vertę  **Koeficientas**, galite nustatyti progresyvinį, regresyvinį arba tiesiogiai proporcingą nusidėvėjimą.

-   Pasirinkus progresyvinį nusidėvėjimą, nusidėvėjimo suma didės kiekvieną nusidėvėjimo laikotarpį.
-   Pasirinkus regresyvinį nusidėvėjimą, laikotarpio nusidėvėjimo suma mažės laikui bėgant.
-   Pasirinkus tiesiogiai proporcingą nusidėvėjimą, kiekvieną laikotarpį nusidėvėjimas bus toks pat.

Toliau pateiktos taisyklės ir pavyzdžiai nurodo, kaip nustatyti kiekvieno nusidėvėjimo tipo koeficientus. 

> [!NOTE] 
> Kai lauke **Metodas** pasirinksite **Koeficientas**, bus rodomi laukai **Koeficientas** ir **Intervalas**.

## <a name="progressive-depreciation"></a>Progresyvinis nusidėvėjimas
Lauko **Koeficientas** vertė – daugiau negu **50**.

### <a name="example"></a>Pavyzdys

Įsigijimo kaina yra 100 000, koeficientas yra 70, dėvėjimo laikas yra 10 metų, o nusidėvėjimas pradėtas sausio 1 d. Rodomos tik pirmųjų šešių dėvėjimo metų nusidėvėjimo ir balansinės vertės sumos.

| Metai | Laikotarpis      | Nusidėvėjimo suma | Balansinės vertės suma |
|------|-------------|---------------------|-----------------------|
| 1    | Gruodžio 31 d. | 307,69              | 99 692,31             |
| 2    | Gruodžio 31 d. | 1447,21            | 98 245,10             |
| 3    | Gruodžio 31 d. | 3104,50            | 95 140,60             |
| 4    | Gruodžio 31 d. | 5150,21            | 89 990,39             |
| 5    | Gruodžio 31 d. | 7522,95            | 82 467,44             |
| 6    | Gruodžio 31 d. | 10 184,06           | 72 283,38             |

## <a name="digressive-depreciation"></a>Regresyvinis nusidėvėjimas
Lauko **Koeficientas** vertė – mažiau negu **50**.

### <a name="example"></a>Pavyzdys

Įsigijimo kaina yra 100 000, koeficientas yra 20, dėvėjimo laikas yra 10 metų, o nusidėvėjimas pradėtas sausio 1 d. Rodomos tik pirmųjų šešių dėvėjimo metų nusidėvėjimo ir balansinės vertės sumos.

| Metai | Laikotarpis      | Nusidėvėjimo suma | Balansinės vertės suma |
|------|-------------|---------------------|-----------------------|
| 1    | Gruodžio 31 d. | 56 080,43           | 43 919,57             |
| 2    | Gruodžio 31 d. | 10 665,70           | 33 253,87             |
| 3    | Gruodžio 31 d. | 7156,22            | 26 097,65             |
| 4    | Gruodžio 31 d. | 5538,06            | 20 559,59             |
| 5    | Gruodžio 31 d. | 4579,89            | 15 979,70             |
| 6    | Gruodžio 31 d. | 3937,36            | 12 042,34             |

## <a name="straight-line-depreciation"></a>Tiesiogiai proporcingas nusidėvėjimas
Lauko **Koeficientas** vertė lygi **50**. Šiuo atveju kiekvieno laikotarpio nusidėvėjimas vienodas, reikia atsižvelgti į kituose laukuose nurodytas, kaip aprašyta straipsnyje [Tiesiogiai proporcingas nusidėvėjimas](straight-line-service-life-depreciation.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
