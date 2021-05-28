---
title: Dėl suderinimo priežasčių galite įtraukti tik pagrindinę sąskaitą kaip kredito sąskaitą
description: Kai transportavimo valdymo dalyje nustatote derinimo priežastį, galite įtraukti tik pagrindinę sąskaitą kaip kredito sąskaitą.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026731"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a>Dėl suderinimo priežasčių galite įtraukti tik pagrindinę sąskaitą kaip kredito sąskaitą

KB numeris: 4603538

## <a name="symptoms"></a>Požymiai

Kai transportavimo valdymo dalyje nustatote derinimo priežastį, galite įtraukti tik pagrindinę sąskaitą kaip kredito sąskaitą. Negalima įtraukti išlaidų centro ar kitos dimensijos kaip kredito sąskaitos. Tačiau debeto sąskaita leidžia pasirinkti kitas dimensijas.

## <a name="resolution"></a>Skiriamoji geba

Jei derinimas atliekamas ne mokėti tiekėjui, bet kredituoti konkrečią pagrindinę sąskaitą, sistema neleidžia pasirinkti kredito sąskaitos finansinės dimensijos, kai nustatote derinimo priežastį.

Jei sąskaitos struktūrai reikia konkrečios kredito pagrindinės sąskaitos finansinės dimensijos vertės, gauto tiekėjo žurnalo automatiškai registruoti negalima, nes trūksta finansinės dimensijos vertės. Todėl pirmiausia, naudodami SF žurnalo puslapį, turite nurodyti kredito **sąskaitą neautomatiniu** būdu.

Kadangi reikalinga kredito sąskaitos dimensijos vertė, tiekėjo SF žurnalo automatiškai registruoti negalima. Rankiniu būdu pridę dimensijos vertę prie kredito eilutės pagrindinės sąskaitos, ją turite užregistruoti neautomatiniu būdu.
