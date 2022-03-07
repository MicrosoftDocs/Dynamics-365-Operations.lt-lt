---
title: Keičiant būseną iš Paskelbta, kad baigta į Baigti įvyko klaida
description: Galite gauti klaidą keisdami gamybos užsakymo būseną iš Paskelbta baigta į Baigti. Šiame puslapyje paaiškinama, kodėl ir kaip sumažinti išdavimą.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 744637f5cccffe44b85f77c1a9df2034012fac40
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477098"
---
# <a name="error-when-changing-status-of-production-order-from-reported-as-finished-to-end"></a>Keičiant būseną iš Paskelbta gamyba, kad baigta į Baigti įvyko klaida

## <a name="symptoms"></a>Požymiai

Kai gamybos užsakymo būsena yra keičiama iš „Reported“ į baigtus kaip „End“, gaunu vieną iš tolesnių klaidos pranešimų:

> Naujinti konfliktą. Standartiniai kaštai neatitinka su finansine inventoriaus verte po naujinimo.

> Kritinė klaida įvyko funkcijoje InventCostMovement.checkVariance.

## <a name="cause"></a>Priežastis

Ši klaida atsitinka, nes pagrindiniai duomenys buvo pakeisti kito proceso. Procesas bandys naujinti duomenis iki penkių kartų. Jei konfliktas vis dar yra po penkių bandymų, gausite prieš tai aprašytą klaidos pranešimą.

## <a name="resolution"></a>Sprendimas

Toks veikimo būdas yra numatytas. Norėdami sustabdyti šią problemą, tęskite bendro kiekio darbą. Jis turėtų užbaigti vykdymą.

Jei bendro kiekio darbas nuolatos nepavyksta po jo naujinimo, patikrinkite, ar apvalinimo tikslumas buhalterinės klaidos nustatytajai valiutai atitinka apvalinimą taikomą vertės „InventSum“ lentelėje. Jei apvalinimo tikslumas buvo pakeistas į neatitinkančią vertę, turbūt turite atkeisti ją atgal į atitinkančią vertę. Ieškokite **ModifiedDateTime**. Šiuo atveju, vertė dažniausiai rodys, kad apvalinimo tikslumas neseniai buvo pakeistas.
