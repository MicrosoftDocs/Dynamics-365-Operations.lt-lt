---
title: Siuntos patvirtinti negalima, nes kiekis viršija pristatymo sumažinimo procentinę dalį
description: Siuntos patvirtinti negalima, nes kiekis viršija pristatymo sumažinimo procentinę dalį
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5339b9d800f7454e2a00c230a8d5deca3979c074
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938516"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a>Siuntos patvirtinti negalima, nes kiekis viršija pristatymo sumažinimo procentinę dalį

Klaidos kodas: WAX1687

## <a name="symptoms"></a>Požymiai

Kai bandote patvirtinti siuntą, sistema rodo šį klaidos pranešimą:

> Negalima patvirtinti krovinio išsiuntimo, nes prekių kiekis viršija pristatymo neviršijimo %1 procentą %2.

Todėl negalite patvirtinti krovinio siuntimo.

## <a name="cause"></a>Priežastis

Krovinio arba siuntos kiekis buvo paimtas tik iš dalies. Šiuo metu kiekis yra mažesnis nei paimtas kiekis procentais, kurie nepatenka į leidžiamą pristatymo pristatymo procentinę dalį.

## <a name="resolution"></a>Skiriamoji geba

Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:

- Nustatyti krovinio eilutės kiekį.
- Nustatykite pristatymo pateisavimo procentinę dalį.

### <a name="set-the-load-line-quantity"></a>Nustatyti krovinio eilutės kiekį

Norėdami nustatyti pakrovimo eilutės kiekį, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite pakrovimą, kuriam siuntimo patvirtinti nepavyksta.
1. Krovinio **eilučių** „FastTab" pasirinkite prekės, viršijančios pristatymo pateisavimo procentinę dalį, krovinio eilutę.
1. „FastTab” skirtuke **Eilutės išsami informacija** pasirinkite **Užsakymas** pridėti naujai eilutei.
1. Lauke Kiekis nustatykite vertę kaip paimtą kiekį (t. y. į darbo sukurto kiekio vertę), kad **būtų** galima patvirtinti **siuntą**.

### <a name="set-the-underdelivery-percentage"></a>Nustatykite pristatymo pateisavimo procentinę dalį

Norėdami nustatyti nepristatymo procentą, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite pakrovimą, kuriam siuntimo patvirtinti nepavyksta.
1. Krovinio **eilučių** „FastTab" pasirinkite prekės, viršijančios pristatymo pateisavimo procentinę dalį, krovinio eilutę.
1. „FastTab” skirtuke **Eilutės išsami informacija** pasirinkite **Bendri** pridėti naujai eilutei.
1. Lauke Pristatymo važtaraštis nustatykite didesnę procentinę vertę, kuri sutalpinti pagal krovinio kiekį paimtą kiekį, kad būtų galima **patvirtinti** siuntą.
