---
title: Negalima atšaukti vartotojui būsiančių darbų
description: Negalima atšaukti vartotojui būsiančių darbų
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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924406"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a>Negalima atšaukti vartotojui būsiančių darbų

Klaidos kodas: WAX708

## <a name="symptoms"></a>Požymiai

Sistema rodo tokį klaidos pranešimą:

> Negalima atšaukti vartotojui priskirto darbo.

## <a name="cause"></a>Priežastis

Darbą užrakina vartotojas ir jo atšaukti negalima. Norėdami tai patvirtinti, atidarykite darbo ID ir atidarykite **skirtuką** Bendra. Jei darbas užrakintas, darbo būsenos laukas bus nustatytas į Vykdoma, o laukas Užrakinta pagal **bus nustatytas** *kaip* **vartotojo** ID.

## <a name="resolution"></a>Skiriamoji geba

Norėdami atšaukti darbą atlikite šiuos žingsnius.

1. Eiti į **Sandėlio valdymo \> periodines užduotis \> Valyti darbą \> Atšaukti**.
1. Lauke **Darbo ID** nurodykite darbo, kurį norite atšaukti, ID.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Taip**, kad patvirtintumėte, kad norite atšaukti darbą.

Dėl platesnės informacijos, žr. [Darbo sandėlyje atšaukimas dėl išimčių tvarkymo](../../warehousing/cancel-warehouse-work.md).
