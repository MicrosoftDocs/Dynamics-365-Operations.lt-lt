---
title: Prekės RM rezervuoti negalima, kai išleistas gamybos užsakymas
description: 'Paleidžiant gamybos užsakymą gali būti rodoma klaida: „Prekės RM visiškai rezervuoti nepavyko.“ Užtikrinkite, kad yra visas kiekis, arba rezervuokite prekes rankiniu būdu.'
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 528895252d661bb012f49190c15853989833064d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477119"
---
# <a name="item-rm-cant-be-fully-reserved-when-a-production-order-is-released"></a>Prekės visiškai RM rezervuoti negalima, kai išleistas gamybos užsakymas

## <a name="symptoms"></a>Požymiai

Jei ne visos BOM eilutės prekės yra fiziškai prieinamos, kai gamybos užsakymas yra išleistas į sandėlį ir **Išleisti į sandėlį** politika yra nustatyta į *Būtina visa rezervacija* gamybos užsakyme, gausite tolesnį klaidos pranešimą:

> Prekė RM negali būti iki galo rezervuota. Įsitikinkite, kad visas kiekis yra prieinamas arba rezervuokite prekes rankiniu būdu, jei rezervacijos laukelis BOM eilutėje yra nustatytas į rankinį ar pradėtą. Nepavyko išleisti užsakymo į sandėlį, nes nepavyko rezervuoti kai kurių medžiagų.

## <a name="resolution"></a>Sprendimas

Šis elgesys yra suprojektuotas tokiu būdu ir veikia kaip tikėtasi. Ištaisykite šią problemą, vadovaukitės klaidos pranešime pateiktais nurodymais: „Įsitikinkite, kad yra visas kiekis, arba rezervuokite prekes rankiniu būdu, jei KS eilutės lauko Rezervavimas reikšmė nustatyta kaip Rankinis arba Pradėta."
