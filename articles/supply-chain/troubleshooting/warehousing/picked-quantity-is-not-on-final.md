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
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="bd91b-103">Negalima patvirtinti siuntos, nes prekės nebuvo paimtos</span><span class="sxs-lookup"><span data-stu-id="bd91b-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="bd91b-104">Klaidos kodas: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="bd91b-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="bd91b-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="bd91b-105">Symptoms</span></span>

<span data-ttu-id="bd91b-106">Kai bandote patvirtinti siuntą, sistema rodo šį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="bd91b-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="bd91b-107">Kai kurios prekės, kurias reikia pakrauti %1, dar nepaimtos ir neperkeltos į galutinę siuntimo vietą.</span><span class="sxs-lookup"><span data-stu-id="bd91b-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="bd91b-108">Todėl negalite patvirtinti krovinio siuntimo.</span><span class="sxs-lookup"><span data-stu-id="bd91b-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="bd91b-109">Priežastis</span><span class="sxs-lookup"><span data-stu-id="bd91b-109">Cause</span></span>

<span data-ttu-id="bd91b-110">Dabartinės krovinio arba siuntos būsenos patvirtinti negalima, nes gali būti viena iš šių sąlygų:</span><span class="sxs-lookup"><span data-stu-id="bd91b-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="bd91b-111">Susijęs darbas dar neparinktas ir perkeltas į galutinę siuntimo vietą.</span><span class="sxs-lookup"><span data-stu-id="bd91b-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="bd91b-112">Paimtas darbo kiekis neatitinka sukurto darbo kiekio krovinio eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bd91b-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>

## <a name="resolution"></a><span data-ttu-id="bd91b-113">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="bd91b-113">Resolution</span></span>

<span data-ttu-id="bd91b-114">Tikrinti su kroviniu ar siunta susijusius pardavimo užsakymus arba perkėlimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="bd91b-114">Check the related sales orders or transfer orders for the load or shipment.</span></span> <span data-ttu-id="bd91b-115">Įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir kad kiekiai atitinka.</span><span class="sxs-lookup"><span data-stu-id="bd91b-115">Make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="bd91b-116">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="bd91b-116">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="bd91b-117">Pasirinkite pakrovimą, kuriam siuntimo patvirtinti nepavyksta.</span><span class="sxs-lookup"><span data-stu-id="bd91b-117">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="bd91b-118">„FastTab” **Krovinio eilutės** patikrinkite pakrovimo eilutę.</span><span class="sxs-lookup"><span data-stu-id="bd91b-118">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="bd91b-119">Pasižymėkite lauko Darbo **sukurtas kiekis** vertę.</span><span class="sxs-lookup"><span data-stu-id="bd91b-119">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="bd91b-120">Veiksmų srities skirtuko **Pakrovimas** grupėje **Susijusi informacija** pasirinkite **Darbas**.</span><span class="sxs-lookup"><span data-stu-id="bd91b-120">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="bd91b-121">Patikrinkite, ar darbas užbaigtas galutinėje siuntimo vietoje ir ar paimtas darbo kiekis atitinka krovinio eilutėje sukurtą darbo kiekį.</span><span class="sxs-lookup"><span data-stu-id="bd91b-121">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="bd91b-122">Pakartokite šią procedūrą visose krovinio eilutėse, norėdami įsitikinti, kad visi kriterijai yra įvykdyti.</span><span class="sxs-lookup"><span data-stu-id="bd91b-122">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>
