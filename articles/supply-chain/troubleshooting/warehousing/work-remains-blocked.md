---
title: Darbo lieka užblokuotas
description: Darbo lieka užblokuotas
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924135"
---
# <a name="work-remains-blocked"></a>Darbo lieka užblokuotas

Klaidos kodas: WHSWorkBlockingExecutingWaveReason_ErrorMessage

## <a name="symptoms"></a>Požymiai

Sistema rodo tokį klaidos pranešimą:

> Darbas %1 lieka užblokuotas, nes susijusios bangos %2 būsena yra %3.

## <a name="cause"></a>Priežastis

Darbas šiuo metu apdorojamas bangoje ir jo negalima atblokuoti, kaip nurodyta vienoje iš šių sąlygų:

- Blokavimo priežasčių skirtuke vienos ar daugiau eilučių darbo blokavimo priežasties laukas **nustatytas** į **Apdorojama** *bangą*.
- Jums pasirinkus **Bangą** grupėje **Susijusi informacija** skirtuke **susijusi informacija** veiksmų juostoje, **Bangos būsenos** laukelis nustatytas *Apdorojimas*.

## <a name="resolution"></a>Skiriamoji geba

Veiksmų srities skirtuko **Susijusi informacija** grupėje **Susijusi informacija** pasirinkite **Banga**. Tada, **bangos** puslapyje veiksmų juostoje **Bangos** skirtuke, **Bangos** grupėje rinkitės **Išvalyti bangos duomenis**.

## <a name="workaround"></a>Apėjimo būdas

Jei ankstesni veiksmai neištaisė problemos, galite atšaukti darbą, atlikite šiuos veiksmus.

1. Eiti į **Sandėlio valdymo \> periodines užduotis \> Valyti darbą \> Atšaukti**.
1. Laukelyje **Darbo ID** nurodykite darbo ID, kurį norite atšaukti ir tai, kad dabar **Darbo būsenos** vertė *Atidaryta*, *Vykdoma*, *Atšaukta*, *Kombinuota* ar *Uždaryta*.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Taip**, kad patvirtintumėte, kad norite atšaukti darbą.

Dėl platesnės informacijos, žr. [Darbo sandėlyje atšaukimas dėl išimčių tvarkymo](../../warehousing/cancel-warehouse-work.md).
