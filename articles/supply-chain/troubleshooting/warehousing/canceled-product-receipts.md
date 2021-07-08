---
title: Atšaukti produkto gavimo kvitai neatnaujina operacijos būsenos į Užregistruota
description: Atšaukus gaunamo krovinio produkto gavimo kvitus, sistema automatiškai atnaujina atsargų operacijos būseną iš Gauta į Užsakyta.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294135"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a><span data-ttu-id="dcd7f-103">Atšaukti produkto gavimo kvitai neatnaujina operacijos būsenos į Užregistruota</span><span class="sxs-lookup"><span data-stu-id="dcd7f-103">Canceled product receipts don't update transaction status to Registered</span></span>

## <a name="symptoms"></a><span data-ttu-id="dcd7f-104">Požymiai</span><span class="sxs-lookup"><span data-stu-id="dcd7f-104">Symptoms</span></span>

<span data-ttu-id="dcd7f-105">Įvykdžius **Atšaukti produkto gavimo kvitus** veiksmą gaunamam kroviniui, sistema automatiškai atnaujina atsargų operacijų būseną iš *Gauta* į *Užsakyta*.</span><span class="sxs-lookup"><span data-stu-id="dcd7f-105">After you run the **Cancel product receipts** action on an inbound load, the system automatically updates the status of inventory transactions from *Received* to *Ordered*.</span></span>

## <a name="resolution"></a><span data-ttu-id="dcd7f-106">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="dcd7f-106">Resolution</span></span>

<span data-ttu-id="dcd7f-107">Atšaukus siunčiamų krovinių važtaraščius, atsargų operacijų būsena lieka *Paimta*.</span><span class="sxs-lookup"><span data-stu-id="dcd7f-107">When packing slips are canceled for outbound loads, the status of inventory transactions remains *Picked*.</span></span> <span data-ttu-id="dcd7f-108">Tačiau kai atšaukiami gaunamo krovinio produktų gavimo kvitai, atsargų operacijų būsena neatkuriama į *Užregistruota*.</span><span class="sxs-lookup"><span data-stu-id="dcd7f-108">However, when product receipts from an inbound load are canceled, the status of inventory transactions isn't restored to *Registered*.</span></span> <span data-ttu-id="dcd7f-109">Todėl atšaukus produkto gavimo kvitą iš gaunamo krovinio, sandėlio darbuotojas turi iš naujo užregistruoti krovinių prekių kiekius.</span><span class="sxs-lookup"><span data-stu-id="dcd7f-109">Therefore, after a product receipt from an inbound load is canceled, the warehouse worker must re-register item quantities for the loads.</span></span>

<span data-ttu-id="dcd7f-110">Daugiau informacijos rasite [Registruoti gaunamo krovinio prekių kiekius](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span><span class="sxs-lookup"><span data-stu-id="dcd7f-110">For more information, see [Register item quantities that arrive on an inbound load](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span></span>
