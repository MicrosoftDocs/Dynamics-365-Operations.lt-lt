---
title: Nukopijavus aplinką trūksta produktų ir kategorijų
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai po svetainės kopijavimo iš vienos aplinkos į kitą arba toje pačioje aplinkoje trūksta produktų ir kategorijų.
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
ms.openlocfilehash: 813289db052323fd87cd5a65184d71a580f1a3e0df9ea7d50a752e26b3962d1c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763625"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>Nukopijavus aplinką trūksta produktų ir kategorijų

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai po svetainės kopijavimo iš vienos aplinkos į kitą arba toje pačioje aplinkoje trūksta produktų ir kategorijų.

## <a name="description"></a>Aprašymas

Kai svetainė nukopijuojama iš vienos aplinkos į kitą arba toje pačioje aplinkoje, svetainėje trūksta produktų ir kategorijų. Produktų ir kategorijų trūks el. prekybos parduotuvėje bei „Commerce“ svetainių daryklės skirtuke **Produktai**.

## <a name="resolution"></a>Sprendimas

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a>Susieti kanalo valdymo vieneto numerį su naujai nukopijuota svetaine „Commerce” svetainių daryklėje

Norėdami susieti kanalo valdymo vieneto numerį (OUN) su naujai nukopijuota svetaine „Commerce” svetainių daryklėje, atlikite šiuos veiksmus.

1. Pasirinkite naujai nukopijuotą svetainę.
1. Dalyje **Svetainės parametrai** pasirinkite **Kanalai**.
1. Šalia kanalo pavadinimo pasirinkite daugtaškį (**...**), tada pasirinkite **Keisti internetinės parduotuvės kanalą**.
1. Dialogo lange **Keisti internetinės parduotuvės kanalą** pasirinkite kanalą, kurį norite susieti su naujai nukopijuota svetaine, tada pasirinkite **Gerai**.
1. Pasirinkite **įrašyti ir publikuoti**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Susiekite „Dynamics 365 Commerce“ saitą su interneto kanalu](../associate-site-online-store.md)
