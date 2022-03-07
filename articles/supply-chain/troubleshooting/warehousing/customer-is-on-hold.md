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
ms.openlocfilehash: 82b28e7cfd8c88e453cdd09398f5a92f605eab15a17d33defa0b9729a53c05b6
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012193"
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
