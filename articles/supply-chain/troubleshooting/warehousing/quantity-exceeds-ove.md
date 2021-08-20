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
ms.openlocfilehash: b25050572662afebbeaa39fa5a96e70cef618ac671dceba189fab1315480ede2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755160"
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
