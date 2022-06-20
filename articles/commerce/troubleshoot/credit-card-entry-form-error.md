---
title: Kredito kortelės įrašo puslapyje rodoma klaida išregistravimo metu
description: Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai mokėjimo būdo skyrius neįkeltas, ir rodomas klaidos pranešimas.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6d1f7ba2d1a63430431af94ed4bed3222c85f14d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910448"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Kredito kortelės įrašo puslapyje rodoma klaida išregistravimo metu

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai **mokėjimo būdo** skyrius neįkeltas, ir rodomas klaidos pranešimas.

## <a name="description"></a>aprašymas

Kai atidarote interneto parduotuvės mokėjimo puslapį, skiltis **Mokėjimo būdas** neįkeliama ir rodomas toks klaidos pranešimas: „Kažkas nutiko. Bandykite vėliau.“

![Mokėjimo modulio klaida.](media/payment-module-error.jpg)

## <a name="resolution"></a>Sprendimas

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Laukti, kol baigsis „Commerce Scale Unit“ talpyklos galiojimas

Mokėjimo paslaugos nustatymai interneto parduotuvės mokėjimo puslapyje talpinami „Commerce Scale Unit“ ir gali užtrukti iki 15 minučių, kol jie pasirodys el. komercijos svetainėje. Šie mokėjimo tarnybos nustatymai apima prekybininko paskyros ID, debesies API rakto ir įvairių konfigūravimo nustatymų, susijusių su mokėjimo būdu, pakeitimus.

## <a name="additional-resources"></a>Papildomi ištekliai

[Interneto kanalo nustatymas](../channel-setup-online.md)
