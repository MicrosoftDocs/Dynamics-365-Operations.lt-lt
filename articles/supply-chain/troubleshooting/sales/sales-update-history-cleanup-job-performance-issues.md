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
ms.openlocfilehash: c02273adf90afc67b7c0ae1b82c19d489bfbd3b1
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920079"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Pardavimo atnaujinimo retrospektyvos valymo užduotis nesėkminga arba yra veikimo problemų

## <a name="symptoms"></a>Požymiai

**Pardavimo atnaujinimo retrospektyvos valymo** paketinė užduotis nepavyksta arba yra veikimo problemų.  

## <a name="cause"></a>Priežastis

Taip gali atsitikti, kai jūsų sistemoje yra daug pardavimo atnaujinimų, todėl gali atsirasti daug pardavimo atnaujinimo duomenų. Valymo užduotis bando išvalyti visus šiuos duomenis vienoje operacijoje. Todėl užduočiai atlikti gali reikėti daug laiko arba gali net nepavykti.

## <a name="resolution"></a>Sprendimas

**Pardavimo atnaujinimo retrospektyvos valymo** paketinės užduoties nauja versija prieinama iš Supply Chain Management versijos 10.0.19 ir naujesnės. Pagal numatytuosius parametrus ši funkcija nėra įjungta. Išsamesnės informacijos apie tai, kaip jis veikia ir kaip jį įgalinti funkcijų valdymas, žr. [pardavimo retrospektyvos valymo efektyvumo patobulinimus](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

