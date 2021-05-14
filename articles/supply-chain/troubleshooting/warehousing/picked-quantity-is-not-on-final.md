---
title: Negalima patvirtinti siuntos, nes prekės nebuvo paimtos
description: Negalima patvirtinti siuntos, nes prekės nebuvo paimtos
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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938518"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>Negalima patvirtinti siuntos, nes prekės nebuvo paimtos

Klaidos kodas: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Požymiai

Kai bandote patvirtinti siuntą, sistema rodo šį klaidos pranešimą:

> Kai kurios prekės, kurias reikia pakrauti %1, dar nepaimtos ir neperkeltos į galutinę siuntimo vietą.

Todėl negalite patvirtinti krovinio siuntimo.

## <a name="cause"></a>Priežastis

Dabartinės krovinio arba siuntos būsenos patvirtinti negalima, nes gali būti viena iš šių sąlygų:

- Susijęs darbas dar neparinktas ir perkeltas į galutinę siuntimo vietą.
- Paimtas darbo kiekis neatitinka sukurto darbo kiekio krovinio eilutėje.

## <a name="resolution"></a>Skiriamoji geba

Tikrinti su kroviniu ar siunta susijusius pardavimo užsakymus arba perkėlimo užsakymus. Įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir kad kiekiai atitinka.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite pakrovimą, kuriam siuntimo patvirtinti nepavyksta.
1. „FastTab” **Krovinio eilutės** patikrinkite pakrovimo eilutę.
1. Pasižymėkite lauko Darbo **sukurtas kiekis** vertę.
1. Veiksmų srities skirtuko **Pakrovimas** grupėje **Susijusi informacija** pasirinkite **Darbas**.
1. Patikrinkite, ar darbas užbaigtas galutinėje siuntimo vietoje ir ar paimtas darbo kiekis atitinka krovinio eilutėje sukurtą darbo kiekį.
1. Pakartokite šią procedūrą visose krovinio eilutėse, norėdami įsitikinti, kad visi kriterijai yra įvykdyti.
