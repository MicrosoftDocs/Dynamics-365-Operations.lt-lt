---
title: Banga negali būti išvalyta
description: Banga negali būti išvalyta
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924332"
---
# <a name="wave-isnt-eligible-for-cleanup"></a>Banga negali būti išvalyta

Klaidos kodas: WaveNotEligibleForCleanup

## <a name="symptoms"></a>Požymiai

Sistema rodo tokį klaidos pranešimą:

> Bangos %1 valyti negalima.

Bangos duomenų išvalyti negalima.  

## <a name="cause"></a>Priežastis

Banga šiuo metu apdorojama, kaip nurodyta vienoje iš šių sąlygų:

- **Bangos būsenos** laukelis nustatytas į *Vykdomas*.
- Jums pasirenkant **Paketo darbą** Bangos **grupėje** Bangos **skirtuke** veiksmų juostoje, **Statuso** laukelis nėra nustatytas į *Užbaigtas*, *Klaida* ar *Atšaukta*. Todėl paketinė užduotis šiuo metu vykdoma.

## <a name="resolution"></a>Skiriamoji geba

Veiksmų srities skirtuko Banga grupėje **Bangos** pasirinkite **Paketinė** užduotis ir **atlikite** vieną iš šių veiksmų:

- Jei **Būsenos** laukelis yra nustatytas į *Vykdomas*: veiksmų juostoje,**Paketo darbe** skirtuke rinkitės **Paketo darbo** grupę ir rinkitės **Peržiūrėti užduotis**. Galite stebėti eigą naujindami **Paketų užduotys** puslapį.
- Jei **Būsenos** laukelis nėra nustatytas į *Vykdomas*: veiksmų juostoje,**Paketo darbe** skirtuke rinkitės **Funkcijų darbo** grupę ir rinkitės **Keisti būseną**. Laukelyje **Rinktis naują būseną** rinkitės *Laukiama*. Tada pasirinkite **Gerai**.
