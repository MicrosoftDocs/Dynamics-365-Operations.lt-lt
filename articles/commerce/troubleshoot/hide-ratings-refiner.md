---
title: Kai neįjungtas įvertinimų ir peržiūros sprendimas, ieškos rezultatuose ir kategorijų puslapiuose rodomi įvertinimų patikslinimai
description: Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kaip paslėpti įvertinimų tikslinimo priemonė paieškos rezultatuose ir kategorijų puslapiuose, kai vertinimo ir peržiūros sprendimas neįjungtas el. komercijos Microsoft Dynamics 365 Commerce svetainėje.
author: gvrmohanreddy
manager: annbe
ms.date: 09/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c35e176fc5673de194a81a3a4694a83f7bc9aa00
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885063"
---
# <a name="ratings-refiner-appears-on-search-results-and-category-pages-when-the-ratings-and-reviews-solution-isnt-enabled"></a>Kai neįjungtas įvertinimų ir peržiūros sprendimas, ieškos rezultatuose ir kategorijų puslapiuose rodomi įvertinimų patikslinimai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kaip paslėpti įvertinimų tikslinimo priemonė paieškos rezultatuose ir kategorijų puslapiuose, kai vertinimo ir peržiūros sprendimas neįjungtas el. komercijos Microsoft Dynamics 365 Commerce svetainėje.

## <a name="description"></a>Aprašas

Reitingų pagerintojas pasirodo paieškos rezultatuose ir kategorijos puslapiuose el. komercijos kanale, kuris nenaudoja reitingų ir rodinių sprendimo.

## <a name="resolution"></a>Sprendimas

### <a name="enable-the-hide-rating-setting-in-commerce-site-builder"></a>Įgalinti vertinimo slėpimo parametrą „Commerce" svetainės generatoriuje

Norėdami įgalinti parametrą **Slėpti įvertinimą** „Commerce" svetainės generatoriuje, kad įvertinimų patikslintojas būtų paslėptas ieškos rezultatuose ir kategorijos puslapiuose, atlikite šiuos veiksmus.

1. Eikite į **Saito nustatymai \> Plėtiniai**.
1. Dalyje **Vertinimai ir peržiūros** pažymėkite žymės langelį **Slėpt įvertinimą**.
1. Pasirinkite **įrašyti ir publikuoti**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Įvertinimų ir atsiliepimų apžvalga](../ratings-reviews-overview.md)

[Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite](../opt-in-ratings-reviews.md)
