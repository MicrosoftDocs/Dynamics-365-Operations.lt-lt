---
title: Dimensijos vieta negali būti tuščia, jei nustatytas serijos numeris
description: Jei gaunate šią klaidą, kai, sukūrus serijos prekės perkėlimo užsakymą, patvirtinate siuntą, numatytosios gavimo vietos laukas yra tuščias.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6f58c72438d5d1d93e59e46525debd65d44d9a76
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477128"
---
# <a name="error-when-confirming-shipment-after-creating-a-transfer-order-for-a-serial-item"></a>Kuriant serijos prekės perkėlimo užsakymą įvyko klaida patvirtinant siuntą

## <a name="symptoms"></a>Požymiai

Gausite tokį klaidos pranešimą, jei sukursite perdavimo užsakymą serijinei prekei naudodami sandėlį, kuris yra įjungtas papildomam sandėlio valdymui (WMS) ir tuomet pabaigę darbą, bandysite patvirtinti siuntimą.

> Dimensijos vieta negali būti tuščia, jei nustatytas dimensijos serijos numeris.

## <a name="cause"></a>Priežastis

Taip nutinka, nes **Numatytoji gavimo vieta** laukelis yra tuščias ir skirtas perdavimo sandėliui „iš“ sandėlio.

## <a name="resolution"></a>Sprendimas

Norėdami ištaisyti šią problemą, nurodykite nustatytąją gavimo vietą perdavimo sandėlyje. Įsitikinkite, kad šį vieta yra licencijos lentelės valdoma.
