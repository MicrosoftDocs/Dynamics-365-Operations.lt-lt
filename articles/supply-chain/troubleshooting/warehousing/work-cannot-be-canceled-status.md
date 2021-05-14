---
title: Darbo atšaukti negalima dėl jo būsenos
description: Darbo atšaukti negalima dėl jo būsenos
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924260"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a>Darbo atšaukti negalima dėl jo būsenos

Klaidos kodas: WAX2190

## <a name="symptoms"></a>Požymiai

Sistema rodo tokį klaidos pranešimą:

> Darbo %1 atšaukti negalite, nes jo būsena %2.

## <a name="cause"></a>Priežastis

Dabartinės darbo būsenos atšaukti negalima.

Darbo antraštėje arba darbo eilutėse nėra numatomos **darbo būsenos** vertės. Darbo **antraštės laukas Darbo būsena nėra nustatytas** *kaip* Atidaryta arba *Vykdoma*.

## <a name="resolution"></a>Skiriamoji geba

Norėdami atšaukti darbą atlikite šiuos žingsnius.

1. Eiti į **Sandėlio valdymo \> periodines užduotis \> Valyti darbą \> Atšaukti**.
1. Lauke **Darbo ID** nurodykite darbo, kurį norite atšaukti, ID.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Taip**, kad patvirtintumėte, kad norite atšaukti darbą.

Dėl platesnės informacijos, žr. [Darbo sandėlyje atšaukimas dėl išimčių tvarkymo](../../warehousing/cancel-warehouse-work.md).
