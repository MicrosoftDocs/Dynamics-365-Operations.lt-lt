---
title: Negalima pasirinkti atsargų būsenos pakeitimo kaip darbo tipo
description: Negalite sukurti atsargų būsenos darbo šablono eilutės, nes darbo tipą naudoja tik sistemos procesai. Pasirinkite kitą darbo tipą.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ad7f26f3235d15779583f9cdadeb4e6dca16242a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477126"
---
# <a name="cant-select-inventory-status-change-in-the-work-type-column"></a>Negalima pasirinkti atsargų būsenos pakeitimo kaip darbo stulpelio

## <a name="symptoms"></a>Požymiai

Konfigūruodami „Microsoft Dynamics 365 Supply Chain Management“ galite gauti tokį klaidos pranešimą:

> Negalite sukurti atsargų būsenos darbo šablono eilutės, nes darbo tipą negalioja tik sistemos procesai. Pasirinkite kitą darbo tipą.

## <a name="resolution"></a>Sprendimas

Toks veikimo būdas yra numatytas. *Inventoriaus būsenos keitimo* darbo tipas yra naudojamas sistemos procesų. Jo konfigūruoti negalima. Kadangi darbo tipų sąrašai yra fiksuoti kaip numeravimas, papildomi objektai negali būti filtruojami iš **Darbo tipo** iškrentančio meniu.
