---
title: Registruojant tiekėjo SF įvyko išimtis
description: "\"Išimtį pateikė invocation paskirties vieta\" išimtis įvyksta registruojant tiekėjo SF."
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ecc63cb7d0d2392105d8e4290f8e837945ae0781
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477088"
---
# <a name="an-exception-occurs-during-vendor-invoice-posting"></a>Registruojant tiekėjo SF įvyko išimtis


## <a name="symptoms"></a>Požymiai

Registruodami tiekėjo SF gaunate šią išimtį:

> Išimtį pateikė iškavimo tikslas

## <a name="cause"></a>Priežastis

Ši problema gali atsirasti dėl pirkimo užsakymo paskirstymų nenuoseklumo.

## <a name="resolution"></a>Sprendimas

Norėdami atblokuoti šią problemą ir iš naujo nustatyti pirkimo užsakymą į būseną *Juodraštis*, eikite į **Įsigijimas ir šaltinio pasirinkimas \> Periodinės užduotys \> Valymas \> Pirkimo užsakymo paskirstymo nustatymas iš naujo**. Norėdami gauti daugiau informacijos, peržiūrėkite šį tinklaraščio įrašą: [Pašalinti PO paskirstymo klaidas „Dynamics 365 Supply Chain Management”](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).
