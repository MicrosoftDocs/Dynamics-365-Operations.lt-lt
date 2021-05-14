---
title: Paskutinė uždaryto darbo eilutė turi būti padėta
description: Paskutinė uždaryto darbo eilutė turi būti padėta
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924380"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a>Paskutinė uždaryto darbo eilutė turi būti padėta

Klaidos kodas: WAX1285

## <a name="symptoms"></a>Požymiai

Sistema rodo tokį klaidos pranešimą:

> Paskutinė uždaryto darbo eilutė turi būti padėta.

## <a name="cause"></a>Priežastis

Dabartinės darbo būsenos atšaukti negalima.

Paskutinėje darbo eilutėje laukas Darbo būsena nustatytas kaip Uždaryta, **bet laukas** Darbo *tipas* nėra **nustatytas** kaip *Padėti*.

## <a name="resolution"></a>Skiriamoji geba

Norėdami atšaukti darbą atlikite šiuos žingsnius.

1. Eiti į **Sandėlio valdymo \> periodines užduotis \> Valyti darbą \> Atšaukti**.
1. Lauke **Darbo ID** nurodykite darbo, kurį norite atšaukti, ID.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Taip**, kad patvirtintumėte, kad norite atšaukti darbą.

Dėl platesnės informacijos, žr. [Darbo sandėlyje atšaukimas dėl išimčių tvarkymo](../../warehousing/cancel-warehouse-work.md).
