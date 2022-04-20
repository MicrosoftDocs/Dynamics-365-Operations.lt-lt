---
title: Pardavimo atnaujinimo retrospektyvos valymo užduotis nesėkminga arba yra veikimo problemų
description: Pardavimo retrospektyvos valymo paketinė užduotis gali nepavykti arba gali užtrukti labai ilgai, jei yra didelis pardavimo atnaujinimo duomenų kiekis.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 124fb90ecafd4f4cccbd8a8bb443694c95365732
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570346"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Pardavimo atnaujinimo retrospektyvos valymo užduotis nesėkminga arba yra veikimo problemų

## <a name="symptoms"></a>Požymiai

**Pardavimo atnaujinimo retrospektyvos valymo** paketinė užduotis nepavyksta arba yra veikimo problemų.  

## <a name="cause"></a>Priežastis

Taip gali atsitikti, kai jūsų sistemoje yra daug pardavimo atnaujinimų, todėl gali atsirasti daug pardavimo atnaujinimo duomenų. Valymo užduotis bando išvalyti visus šiuos duomenis vienoje operacijoje. Todėl užduočiai atlikti gali reikėti daug laiko arba gali net nepavykti.

## <a name="resolution"></a>Sprendimas

**Pardavimo atnaujinimo retrospektyvos valymo** paketinės užduoties nauja versija prieinama iš Supply Chain Management versijos 10.0.19 ir naujesnės. Numatyta, kad ši funkcija nėra įjungta. Išsamesnės informacijos apie tai, kaip jis veikia ir kaip jį įgalinti funkcijų valdymas, žr [. Grafiko pardavimo retrospektyvos duomenų išvalymą](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

