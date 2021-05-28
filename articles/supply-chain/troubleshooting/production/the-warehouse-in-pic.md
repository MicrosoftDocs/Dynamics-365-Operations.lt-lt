---
title: Sandėlis išrinkimo dokumento žurnale nėra atnaujintas KS eilutėje.
description: Sandėlis išrinkimo dokumento žurnale nėra atnaujintas medžiagos važtaraštyje KS eilutėje.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5d24c0b8538f3894fd1d2a3edb3a6ed8633c9609
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026736"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>Sandėlis išrinkimo dokumento žurnale nėra atnaujintas KS eilutėje

KB numeris: 4614848

## <a name="symptoms"></a>Požymiai

Sandėlis išrinkimo dokumento žurnale nėra atnaujintas medžiagos važtaraštyje KS eilutėje.

## <a name="resolution"></a>Skiriamoji geba

Sistema veikia kaip sukurta. Jei sukuriama išrinkimo dokumento žurnalo eilutė su nuoroda (per partijos ID) į gamybos KS eilutę, gamybos KS eilutėje nurodytas sandėlis nebus atnaujinamas, jei sandėlio dimensija gamybos išrinkimo dokumento žurnalo eilutėje bus pakeista vėliau.
