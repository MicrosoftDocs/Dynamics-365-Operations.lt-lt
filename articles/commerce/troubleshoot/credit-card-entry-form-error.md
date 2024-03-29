---
title: Kredito kortelės įrašo puslapyje rodoma klaida išregistravimo metu
description: Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai mokėjimo būdo skyrius neįkeltas, ir rodomas klaidos pranešimas.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 25f0dde83efff7c1d9a2a456270f5d48047f44ba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269761"
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
