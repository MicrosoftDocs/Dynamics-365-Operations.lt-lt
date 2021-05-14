---
title: Siuntos patvirtinti negalima, nes kiekis viršija pristatymo sumažinimo procentinę dalį
description: Siuntos patvirtinti negalima, nes kiekis viršija pristatymo sumažinimo procentinę dalį
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
ms.openlocfilehash: 5339b9d800f7454e2a00c230a8d5deca3979c074
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938516"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a><span data-ttu-id="4991c-103">Siuntos patvirtinti negalima, nes kiekis viršija pristatymo sumažinimo procentinę dalį</span><span class="sxs-lookup"><span data-stu-id="4991c-103">You can't confirm a shipment because the quantity exceeds the underdelivery percentage</span></span>

<span data-ttu-id="4991c-104">Klaidos kodas: WAX1687</span><span class="sxs-lookup"><span data-stu-id="4991c-104">Error code: WAX1687</span></span>

## <a name="symptoms"></a><span data-ttu-id="4991c-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="4991c-105">Symptoms</span></span>

<span data-ttu-id="4991c-106">Kai bandote patvirtinti siuntą, sistema rodo šį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="4991c-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="4991c-107">Negalima patvirtinti krovinio išsiuntimo, nes prekių kiekis viršija pristatymo neviršijimo %1 procentą %2.</span><span class="sxs-lookup"><span data-stu-id="4991c-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for underdelivery.</span></span>

<span data-ttu-id="4991c-108">Todėl negalite patvirtinti krovinio siuntimo.</span><span class="sxs-lookup"><span data-stu-id="4991c-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="4991c-109">Priežastis</span><span class="sxs-lookup"><span data-stu-id="4991c-109">Cause</span></span>

<span data-ttu-id="4991c-110">Krovinio arba siuntos kiekis buvo paimtas tik iš dalies.</span><span class="sxs-lookup"><span data-stu-id="4991c-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="4991c-111">Šiuo metu kiekis yra mažesnis nei paimtas kiekis procentais, kurie nepatenka į leidžiamą pristatymo pristatymo procentinę dalį.</span><span class="sxs-lookup"><span data-stu-id="4991c-111">The quantity is currently less than the picked quantity by a percentage that is outside the allowed underdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="4991c-112">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="4991c-112">Resolution</span></span>

<span data-ttu-id="4991c-113">Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:</span><span class="sxs-lookup"><span data-stu-id="4991c-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="4991c-114">Nustatyti krovinio eilutės kiekį.</span><span class="sxs-lookup"><span data-stu-id="4991c-114">Set the load line quantity.</span></span>
- <span data-ttu-id="4991c-115">Nustatykite pristatymo pateisavimo procentinę dalį.</span><span class="sxs-lookup"><span data-stu-id="4991c-115">Set the underdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="4991c-116">Nustatyti krovinio eilutės kiekį</span><span class="sxs-lookup"><span data-stu-id="4991c-116">Set the load line quantity</span></span>

<span data-ttu-id="4991c-117">Norėdami nustatyti pakrovimo eilutės kiekį, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4991c-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="4991c-118">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="4991c-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="4991c-119">Pasirinkite pakrovimą, kuriam siuntimo patvirtinti nepavyksta.</span><span class="sxs-lookup"><span data-stu-id="4991c-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="4991c-120">Krovinio **eilučių** „FastTab" pasirinkite prekės, viršijančios pristatymo pateisavimo procentinę dalį, krovinio eilutę.</span><span class="sxs-lookup"><span data-stu-id="4991c-120">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="4991c-121">„FastTab” skirtuke **Eilutės išsami informacija** pasirinkite **Užsakymas** pridėti naujai eilutei.</span><span class="sxs-lookup"><span data-stu-id="4991c-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="4991c-122">Lauke Kiekis nustatykite vertę kaip paimtą kiekį (t. y. į darbo sukurto kiekio vertę), kad **būtų** galima patvirtinti **siuntą**.</span><span class="sxs-lookup"><span data-stu-id="4991c-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-underdelivery-percentage"></a><span data-ttu-id="4991c-123">Nustatykite pristatymo pateisavimo procentinę dalį</span><span class="sxs-lookup"><span data-stu-id="4991c-123">Set the underdelivery percentage</span></span>

<span data-ttu-id="4991c-124">Norėdami nustatyti nepristatymo procentą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4991c-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="4991c-125">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="4991c-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="4991c-126">Pasirinkite pakrovimą, kuriam siuntimo patvirtinti nepavyksta.</span><span class="sxs-lookup"><span data-stu-id="4991c-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="4991c-127">Krovinio **eilučių** „FastTab" pasirinkite prekės, viršijančios pristatymo pateisavimo procentinę dalį, krovinio eilutę.</span><span class="sxs-lookup"><span data-stu-id="4991c-127">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="4991c-128">„FastTab” skirtuke **Eilutės išsami informacija** pasirinkite **Bendri** pridėti naujai eilutei.</span><span class="sxs-lookup"><span data-stu-id="4991c-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="4991c-129">Lauke Pristatymo važtaraštis nustatykite didesnę procentinę vertę, kuri sutalpinti pagal krovinio kiekį paimtą kiekį, kad būtų galima **patvirtinti** siuntą.</span><span class="sxs-lookup"><span data-stu-id="4991c-129">In the **Underdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
