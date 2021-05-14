---
title: Darbo atšaukti negalima dėl to, kad jis užblokuotas
description: Darbo atšaukti negalima dėl to, kad jis užblokuotas
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924284"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a>Darbo atšaukti negalima dėl to, kad jis užblokuotas

Klaidos kodas: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage

## <a name="symptoms"></a>Požymiai

Sistema rodo tokį klaidos pranešimą:

> Darbo %1atšaukti negalima, nes jį užblokavo priežasties %2 tipas. Darbas turi būti atblokuotas prieš jo atšaukimą.

## <a name="cause"></a>Priežastis

Darbą užblokuoja vartotojas ir jo atšaukti negalima.

Skirtuko **Bendra** puslapyje Darbas **nustatyta** **parinktis** Užblokuota kaip *Taip*. Šis parametras nurodo, kad darbas užblokuotas. Blokavimo **priežasčių** skirtukas rodo, kodėl darbas buvo užblokuotas.

## <a name="resolution"></a>Skiriamoji geba

Norėdami atblokuoti darbą, pasirinkite **blokavimo priežasčių** skirtuką ir atlikite vieną iš šių veiksmų:

- Jei **darbo blokavimo priežasties** laukelis yra nustatytas į *Neapibrėžta priežastis*: Veiksmų srities skirtuko **Darbas** skirtuke, **Darbas** grupėje rinkitės **Atblokuoti darbą**.
- Jei **Darbo blokavimo priežasties** laukelis yra nustatytas į *Apdorojimo banga*: Veiksmų juostoje **Susijusi informacija** skirtuke **Susijusi informacija** grupėje rinkitės **Banga**. Tada, **bangos** puslapyje veiksmų juostoje **Bangos** skirtuke, **Bangos** grupėje rinkitės **Išvalyti bangos duomenis**.

## <a name="workaround"></a>Apėjimo būdas

Jei ankstesni veiksmai neištaisė problemos, galite atšaukti darbą, atlikite šiuos veiksmus.

1. Eiti į **Sandėlio valdymo \> periodines užduotis \> Valyti darbą \> Atšaukti**.
1. Laukelyje **Darbo ID** nurodykite darbo ID, kurį norite atšaukti ir tai, kad dabar **Darbo būsenos** vertė *Atidaryta*, *Vykdoma*, *Atšaukta*, *Kombinuota* ar *Uždaryta*.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Taip**, kad patvirtintumėte, kad norite atšaukti darbą.

Dėl platesnės informacijos, žr. [Darbo sandėlyje atšaukimas dėl išimčių tvarkymo](../../warehousing/cancel-warehouse-work.md).
