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
ms.openlocfilehash: 1d7b0140d0c2724234a549ca4dfb23109012654abe0e60fcea1f98e8f17c153a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748696"
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
