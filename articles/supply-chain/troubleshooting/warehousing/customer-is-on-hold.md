---
title: Negalite patvirtinti siuntos, nes klientas yra sulaikytas
description: Negalite patvirtinti siuntos, nes klientas yra sulaikytas.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 801778fc8f04b106bf168a3dcd5a89767a837740
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344269"
---
# <a name="you-cant-confirm-a-shipment-because-the-customer-is-on-hold"></a>Negalite patvirtinti siuntos, nes klientas yra sulaikytas

Klaidos kodas: WAX:CustomerOnHoldShipmentCannotBeConfirmed

## <a name="symptoms"></a>Požymiai

Kai bandote patvirtinti siuntą, sistema rodo šį klaidos pranešimą:

> Siuntos %1 patvirtinti negalima, nes klientas yra sulaikytas %2.

Todėl negalite patvirtinti krovinio siuntimo.

## <a name="cause"></a>Priežastis

Kliento krovinio arba siuntos paskyra yra sulaikyta. Todėl kliento būsena neleidžia patvirtinti siuntimo.

## <a name="resolution"></a>Sprendimas

Norėdami atblokuoti kliento kodą, naudokite nurodytą procedūrą.

1. Eikite į **Gautinos sumos \> Klientai \> Visi klientai**.
1. Atidarykite kliento sąskaitą, kurios siuntos patvirtinti negalima.
1. FastTab **Kreditas ir rinkiniai** nustatykite **SF išrašymo ir pristatymo sulaikymo** lauką į *Ne*.
1. Pakartokite šią procedūrą visiems užblokuotiems krovinio klientams.
