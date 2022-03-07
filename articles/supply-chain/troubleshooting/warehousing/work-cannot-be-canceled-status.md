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
ms.openlocfilehash: f983501b490c5516525b4d5904603ed62e8799f9e6124e5672b36a12804ecb0a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755983"
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
