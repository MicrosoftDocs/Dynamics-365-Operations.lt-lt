---
title: Šiai vietai reikia nurodyti numerio lentelę
description: Jei gaunate šią klaidą, kai, sukūrus serijos prekės perkėlimo WMS įgalintą sandėlį, patvirtinate siuntą, numatytosios gavimo vietos laukas siekiant perkelti sandėlį.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2e562ad2b41dd149f215adc83bd2d54e55dccc05
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477059"
---
# <a name="license-plate-specification-error-when-confirming-shipment-for-a-transfer-order"></a>Numerio lentelės specifikacijos klaida patvirtinant perkėlimo užsakymo siuntą

## <a name="symptoms"></a>Požymiai

Gausite šį klaidos pranešimą, jei sukursite perdavimo užsakymą naudodami sandėlį, kuris yra įjungtas papildomam sandėlio valdymui (WMS) ir tuomet pabaigę darbą gausite tokį klaidos pranešimą:

> Šiai vietai reikia nurodyti numerio lentelę.

## <a name="cause"></a>Priežastis

Taip nutinka, nes **Numatytoji gavimo vieta** laukelis yra tuščias ir skirtas perdavimo sandėliui „iš“ sandėlio.

## <a name="resolution"></a>Sprendimas

Norėdami ištaisyti šią problemą, nurodykite nustatytąją gavimo vietą perdavimo sandėlyje. Įsitikinkite, kad šį vieta yra licencijos lentelės valdoma.
