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
ms.openlocfilehash: c4ba48c5b6e3476c203eed2fddf053ce8af873dd6a7665df54560c8894f8c2d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750887"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a>Dėl suderinimo priežasčių galite įtraukti tik pagrindinę sąskaitą kaip kredito sąskaitą

KB numeris: 4603538

## <a name="symptoms"></a>Požymiai

Kai transportavimo valdymo dalyje nustatote derinimo priežastį, galite įtraukti tik pagrindinę sąskaitą kaip kredito sąskaitą. Negalima įtraukti išlaidų centro ar kitos dimensijos kaip kredito sąskaitos. Tačiau debeto sąskaita leidžia pasirinkti kitas dimensijas.

## <a name="resolution"></a>Skiriamoji geba

Jei derinimas atliekamas ne mokėti tiekėjui, bet kredituoti konkrečią pagrindinę sąskaitą, sistema neleidžia pasirinkti kredito sąskaitos finansinės dimensijos, kai nustatote derinimo priežastį.

Jei sąskaitos struktūrai reikia konkrečios kredito pagrindinės sąskaitos finansinės dimensijos vertės, gauto tiekėjo žurnalo automatiškai registruoti negalima, nes trūksta finansinės dimensijos vertės. Todėl pirmiausia, naudodami SF žurnalo puslapį, turite nurodyti kredito **sąskaitą neautomatiniu** būdu.

Kadangi reikalinga kredito sąskaitos dimensijos vertė, tiekėjo SF žurnalo automatiškai registruoti negalima. Rankiniu būdu pridę dimensijos vertę prie kredito eilutės pagrindinės sąskaitos, ją turite užregistruoti neautomatiniu būdu.
