---
title: Nukopijavus aplinką trūksta produktų ir kategorijų
description: Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai po svetainės kopijavimo iš vienos aplinkos į kitą arba toje pačioje aplinkoje nėra produktų ir kategorijų.
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
ms.openlocfilehash: 0c094f6da7756d2a6a3b80ebdb211d7b78148813
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851110"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>Nukopijavus aplinką trūksta produktų ir kategorijų

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai po svetainės kopijavimo iš vienos aplinkos į kitą arba toje pačioje aplinkoje nėra produktų ir kategorijų.

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
