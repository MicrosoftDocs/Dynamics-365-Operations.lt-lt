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
ms.openlocfilehash: 613eb2af626ca315a8bacb89fb348a5b14bd17b1717a90c99bcede66baef9040
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752392"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Kredito kortelės įrašo puslapyje rodoma klaida išregistravimo metu

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai **mokėjimo būdo** skiltis neįkelta, ir rodomas klaidos pranešimas.

## <a name="description"></a>aprašymas

Kai atidarote interneto parduotuvės mokėjimo puslapį, skiltis **Mokėjimo būdas** neįkeliama ir rodomas toks klaidos pranešimas: „Kažkas nutiko. Bandykite vėliau.“

![Mokėjimo modulio klaida.](media/payment-module-error.jpg)

## <a name="resolution"></a>Sprendimas

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Laukti, kol baigsis „Commerce Scale Unit“ talpyklos galiojimas

Mokėjimo paslaugos nustatymai interneto parduotuvės mokėjimo puslapyje talpinami „Commerce Scale Unit“ ir gali užtrukti iki 15 minučių, kol jie pasirodys el. komercijos svetainėje. Šie mokėjimo tarnybos nustatymai apima prekybininko paskyros ID, debesies API rakto ir įvairių konfigūravimo nustatymų, susijusių su mokėjimo būdu, pakeitimus.

## <a name="additional-resources"></a>Papildomi ištekliai

[Interneto kanalo nustatymas](../channel-setup-online.md)
