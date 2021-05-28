---
title: Kredito kortelės įrašo puslapyje rodoma klaida išregistravimo metu
description: Šioje temoje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai mokėjimo būdo skiltis neįkelta, ir rodomas klaidos pranešimas.
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
ms.openlocfilehash: ea9105481e6c5812565f0d3604906c905bcb5443
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018511"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Kredito kortelės įrašo puslapyje rodoma klaida išregistravimo metu

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai **mokėjimo būdo** skiltis neįkelta, ir rodomas klaidos pranešimas.

## <a name="description"></a>aprašymas

Kai atidarote interneto parduotuvės mokėjimo puslapį, skiltis **Mokėjimo būdas** neįkeliama ir rodomas toks klaidos pranešimas: „Kažkas nutiko. Bandykite vėliau.“

![Mokėjimo modulio klaida](media/payment-module-error.jpg)

## <a name="resolution"></a>Skiriamoji geba

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Laukti, kol baigsis „Commerce Scale Unit“ talpyklos galiojimas

Mokėjimo paslaugos nustatymai interneto parduotuvės mokėjimo puslapyje talpinami „Commerce Scale Unit“ ir gali užtrukti iki 15 minučių, kol jie pasirodys el. komercijos svetainėje. Šie mokėjimo tarnybos nustatymai apima prekybininko paskyros ID, debesies API rakto ir įvairių konfigūravimo nustatymų, susijusių su mokėjimo būdu, pakeitimus.

## <a name="additional-resources"></a>Papildomi ištekliai

[Interneto kanalo nustatymas](../channel-setup-online.md)
