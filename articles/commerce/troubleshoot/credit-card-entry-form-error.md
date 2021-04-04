---
title: Kredito kortelės įrašo puslapyje rodoma klaida išregistravimo metu
description: Šioje temoje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai mokėjimo būdo skiltis neįkelta, ir rodomas klaidos pranešimas.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: f0751fc76e6eb4320f766886b4c1efcb1042e996
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585442"
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
