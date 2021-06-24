---
title: Siuntos negalima patvirtinti dėl nebaigto arba trūkstamo darbo
description: Siuntos negalima patvirtinti dėl nebaigto arba trūkstamo darbo
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: beef0909d41e69f3e7bcc1021527be35b7e6fd44
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123848"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a>Siuntos negalima patvirtinti dėl nebaigto arba trūkstamo darbo

Klaidos kodas: WAX515

## <a name="symptoms"></a>Požymiai

Kai bandote patvirtinti siuntą, sistema rodo šį klaidos pranešimą:

> Negalima patvirtinti krovinio %1 išsiuntimo, nes turi būti baigtas visas su kroviniu susijęs darbas.

Todėl negalite patvirtinti krovinio siuntimo.

## <a name="cause"></a>Priežastis

Krovinio ar siuntimo būsena šiuo metu yra, kai siuntos patvirtinimas nesėkmingas. Prieš patvirtindami siuntą turi būti bent tam tikras krovinio darbas ir viso darbo būsena turi būti  *Uždaryta* arba *Atšaukta*.

## <a name="resolution"></a>Skiriamoji geba

Patikrinkite krovinio arba siuntos susijusius pardavimo ar perkėlimo užsakymus ir įsitikinkite, ar visi susiję darbai buvo užbaigti ar atšaukti.

Su siuntomis ir kroviniais galite dirbti keliuose puslapiuose. Toliau pateikti poskyriai pateikia keletą pavyzdžių.

### <a name="all-loads-page"></a>Visų krovinių puslapis

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite pakrovimą, kuriam siuntimo patvirtinti nepavyksta.
1. Veiksmų srities skirtuko **Pakrovimas** grupėje **Susijusi informacija** pasirinkite **Darbas**.
1. Patikrinti kiekvieno darbo ID būseną. Kiekvieno darbo ID, kurio būsena nėra Uždaryta *arba* Atšaukta *sekimas*.
1. Kai kiekvieno darbo ID būsena yra Uždaryta *arba* *Atšaukta, bandykite* dar kartą patvirtinti siuntą.

### <a name="all-shipments-page"></a>Visų siuntimų puslapis

1. Eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos**.
1. Pasirinkite siuntą, kurios patvirtinti negalima.
1. Veiksmų srityje, skirtuke **Siuntimai**, grupėje **Darbas** pasirinkite **Darbo informacija**.
1. Patikrinti kiekvieno darbo ID būseną. Kiekvieno darbo ID, kurio būsena nėra Uždaryta *arba* Atšaukta *sekimas*.
1. Kai kiekvieno darbo ID būsena yra Uždaryta *arba* *Atšaukta, bandykite* dar kartą patvirtinti siuntą.

### <a name="all-work-page"></a>Visi darbo puslapiai

1. Pasirinkite **Sandėlio valdymas \> Darbas \> Visi darbai**.
1. Pasirinkite užsakymo numerio darbą, pagal kurį siuntos patvirtinti negalima.
1. Veiksmų srities skirtuko **Siuntimas** grupėje **Siuntimas** spustelėkite **Patvirtinti siuntimą**.
1. Patikrinti kiekvieno darbo ID būseną. Kiekvieno darbo ID, kurio būsena nėra Uždaryta *arba* Atšaukta *sekimas*.
1. Kai kiekvieno darbo ID būsena yra Uždaryta *arba* *Atšaukta, bandykite* dar kartą patvirtinti siuntą.
