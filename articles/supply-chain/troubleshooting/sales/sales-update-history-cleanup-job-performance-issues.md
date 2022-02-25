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
ms.openlocfilehash: 371a8c7178cd7c5091d6dd9a91d0ee03b943a269
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103193"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Pardavimo atnaujinimo retrospektyvos valymo užduotis nesėkminga arba yra veikimo problemų

## <a name="symptoms"></a>Požymiai

**Pardavimo atnaujinimo retrospektyvos valymo** paketinė užduotis nepavyksta arba yra veikimo problemų.  

## <a name="cause"></a>Priežastis

Taip gali atsitikti, kai jūsų sistemoje yra daug pardavimo atnaujinimų, todėl gali atsirasti daug pardavimo atnaujinimo duomenų. Valymo užduotis bando išvalyti visus šiuos duomenis vienoje operacijoje. Todėl užduočiai atlikti gali reikėti daug laiko arba gali net nepavykti.

## <a name="resolution"></a>Sprendimas

**Pardavimo atnaujinimo retrospektyvos valymo** paketinės užduoties nauja versija prieinama iš Supply Chain Management versijos 10.0.19 ir naujesnės. Numatyta, kad ši funkcija nėra įjungta. Išsamesnės informacijos apie tai, kaip jis veikia ir kaip jį įgalinti funkcijų valdymas, žr. pardavimo [retrospektyvos valymo efektyvumo patobulinimus](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

