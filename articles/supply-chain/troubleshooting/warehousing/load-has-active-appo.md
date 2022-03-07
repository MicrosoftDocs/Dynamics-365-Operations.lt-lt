---
title: Negalite patvirtinti siuntos dėl kalendoriaus išdavimo
description: Negalite patvirtinti siuntos dėl kalendoriaus išdavimo
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
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938520"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a>Negalite patvirtinti siuntos dėl kalendoriaus išdavimo

Klaidos kodas: TRX2716

## <a name="symptoms"></a>Požymiai

Kai bandote patvirtinti siuntą, sistema rodo šį klaidos pranešimą:

> Esant kalendoriaus tipui %1 būtina užregistruoti ir išregistruoti paskyrą %2.

Todėl negalite patvirtinti krovinio siuntimo.

## <a name="cause"></a>Priežastis

Yra aktyvių krovinio paskyrų. Pvz., yra taisyklė, pagal kurią reikalaujama vairuotojo įregistravimo. Todėl krovinio būsena šiuo metu yra, kai siuntos patvirtinimas nesėkmingas.

## <a name="resolution"></a>Skiriamoji geba

Turite išnagrinėti ir išspręsti visas problemas, susijusias su aktyviomis paskyromis, kurios susijusios su kroviniu.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite pakrovimą, kuriam siuntimo patvirtinti nepavyksta.
1. Veiksmų srityje, skirtuke **Transportavimas**, grupėje **Susitikimai**, pasirinkite **Susitikimo planavimas**.
1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Įsitikinkite, kad vairuotojo registravimas / išregistravimas baigtas paskyrai vykdyti.
    - Užbaikite arba atšaukite paskyrą.
    - Išjunkite **reikiamą susijusios paskyros taisyklės parinktį Vairuotojo** registravimasis.
