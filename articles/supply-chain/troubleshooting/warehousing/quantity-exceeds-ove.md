---
title: Siuntos patvirtinti negalima, nes kiekis viršija per didelio pristatymo procentinę dalį
description: Siuntos patvirtinti negalima, nes kiekis viršija per didelio pristatymo procentinę dalį
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
ms.openlocfilehash: c9b5ba8dedb927ee049d7e53e9a666902f563f49
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938521"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a>Siuntos patvirtinti negalima, nes kiekis viršija per didelio pristatymo procentinę dalį

Klaidos kodas: WAX1687

## <a name="symptoms"></a>Požymiai

Kai bandote patvirtinti siuntą, sistema rodo šį klaidos pranešimą:

> Negalima patvirtinti krovinio išsiuntimo, nes prekių kiekis viršija pristatymo viršijimo %1 procentą %2.

Todėl negalite patvirtinti krovinio siuntimo.

## <a name="cause"></a>Priežastis

Krovinio arba siuntos kiekis buvo paimtas tik iš dalies. Šiuo metu kiekis yra didesnis nei paimtas kiekis procentais, kurie nepatenka į viršijamo pristatymo pristatymo procentinę dalį.

## <a name="resolution"></a>Skiriamoji geba

Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:

- Nustatyti krovinio eilutės kiekį.
- Nustatykite pristatymo viršijamo procentinę dalį.

### <a name="set-the-load-line-quantity"></a>Nustatyti krovinio eilutės kiekį

Norėdami nustatyti pakrovimo eilutės kiekį, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite pakrovimą, kuriam siuntimo patvirtinti nepavyksta.
1. Krovinio **eilučių** „FastTab" pasirinkite prekės, viršijančios pristatymo viršijimo procentinę dalį, krovinio eilutę.
1. „FastTab” skirtuke **Eilutės išsami informacija** pasirinkite **Užsakymas** pridėti naujai eilutei.
1. Lauke Kiekis nustatykite vertę kaip paimtą kiekį (t. y. į darbo sukurto kiekio vertę), kad **būtų** galima patvirtinti **siuntą**.

### <a name="set-the-overdelivery-percentage"></a>Nustatykite pristatymo viršijimo procentinę dalį

Norėdami nustatyti nepristatymo procentą, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite pakrovimą, kuriam siuntimo patvirtinti nepavyksta.
1. Krovinio **eilučių** „FastTab" pasirinkite prekės, viršijančios pristatymo viršijimo procentinę dalį, krovinio eilutę.
1. „FastTab” skirtuke **Eilutės išsami informacija** pasirinkite **Bendri** pridėti naujai eilutei.
1. Lauke **Viršijimas** nustatykite didesnę procentinę vertę, kuri sutalpinti pagal krovinio kiekį paimtą kiekį, kad būtų galima patvirtinti siuntą tam, kad gabenimas būtų patvirtintas.
