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
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a><span data-ttu-id="0cd03-103">Siuntos negalima patvirtinti dėl nebaigto arba trūkstamo darbo</span><span class="sxs-lookup"><span data-stu-id="0cd03-103">You can't confirm a shipment because of incomplete or missing work</span></span>

<span data-ttu-id="0cd03-104">Klaidos kodas: WAX515</span><span class="sxs-lookup"><span data-stu-id="0cd03-104">Error code: WAX515</span></span>

## <a name="symptoms"></a><span data-ttu-id="0cd03-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="0cd03-105">Symptoms</span></span>

<span data-ttu-id="0cd03-106">Kai bandote patvirtinti siuntą, sistema rodo šį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="0cd03-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="0cd03-107">Negalima patvirtinti krovinio %1 išsiuntimo, nes turi būti baigtas visas su kroviniu susijęs darbas.</span><span class="sxs-lookup"><span data-stu-id="0cd03-107">The shipment for load %1 could not be confirmed because all work for the load must be complete.</span></span>

<span data-ttu-id="0cd03-108">Todėl negalite patvirtinti krovinio siuntimo.</span><span class="sxs-lookup"><span data-stu-id="0cd03-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="0cd03-109">Priežastis</span><span class="sxs-lookup"><span data-stu-id="0cd03-109">Cause</span></span>

<span data-ttu-id="0cd03-110">Krovinio ar siuntimo būsena šiuo metu yra, kai siuntos patvirtinimas nesėkmingas.</span><span class="sxs-lookup"><span data-stu-id="0cd03-110">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="0cd03-111">Prieš patvirtindami siuntą turi būti bent tam tikras krovinio darbas ir viso darbo būsena turi būti  *Uždaryta* arba *Atšaukta*.</span><span class="sxs-lookup"><span data-stu-id="0cd03-111">Before you can confirm the shipment, at least some work must exist for the load, and all that work must have a status of *Closed* or *Canceled*.</span></span>

## <a name="resolution"></a><span data-ttu-id="0cd03-112">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="0cd03-112">Resolution</span></span>

<span data-ttu-id="0cd03-113">Patikrinkite krovinio arba siuntos susijusius pardavimo ar perkėlimo užsakymus ir įsitikinkite, ar visi susiję darbai buvo užbaigti ar atšaukti.</span><span class="sxs-lookup"><span data-stu-id="0cd03-113">Check the related sales orders or transfer orders for the load or shipment, and make sure that all the related work has been completed or canceled.</span></span>

<span data-ttu-id="0cd03-114">Su siuntomis ir kroviniais galite dirbti keliuose puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="0cd03-114">You can work with shipments and loads on several pages.</span></span> <span data-ttu-id="0cd03-115">Toliau pateikti poskyriai pateikia keletą pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="0cd03-115">The following subsections provide a few examples.</span></span>

### <a name="all-loads-page"></a><span data-ttu-id="0cd03-116">Visų krovinių puslapis</span><span class="sxs-lookup"><span data-stu-id="0cd03-116">All loads page</span></span>

1. <span data-ttu-id="0cd03-117">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="0cd03-117">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="0cd03-118">Pasirinkite pakrovimą, kuriam siuntimo patvirtinti nepavyksta.</span><span class="sxs-lookup"><span data-stu-id="0cd03-118">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="0cd03-119">Veiksmų srities skirtuko **Pakrovimas** grupėje **Susijusi informacija** pasirinkite **Darbas**.</span><span class="sxs-lookup"><span data-stu-id="0cd03-119">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="0cd03-120">Patikrinti kiekvieno darbo ID būseną.</span><span class="sxs-lookup"><span data-stu-id="0cd03-120">Inspect the status of each work ID.</span></span> <span data-ttu-id="0cd03-121">Kiekvieno darbo ID, kurio būsena nėra Uždaryta *arba* Atšaukta *sekimas*.</span><span class="sxs-lookup"><span data-stu-id="0cd03-121">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="0cd03-122">Kai kiekvieno darbo ID būsena yra Uždaryta *arba* *Atšaukta, bandykite* dar kartą patvirtinti siuntą.</span><span class="sxs-lookup"><span data-stu-id="0cd03-122">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-shipments-page"></a><span data-ttu-id="0cd03-123">Visų siuntimų puslapis</span><span class="sxs-lookup"><span data-stu-id="0cd03-123">All shipments page</span></span>

1. <span data-ttu-id="0cd03-124">Eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos**.</span><span class="sxs-lookup"><span data-stu-id="0cd03-124">Go to **Warehouse management \> Shipments\> All shipments**.</span></span>
1. <span data-ttu-id="0cd03-125">Pasirinkite siuntą, kurios patvirtinti negalima.</span><span class="sxs-lookup"><span data-stu-id="0cd03-125">Select the shipment that can't be confirmed.</span></span>
1. <span data-ttu-id="0cd03-126">Veiksmų srityje, skirtuke **Siuntimai**, grupėje **Darbas** pasirinkite **Darbo informacija**.</span><span class="sxs-lookup"><span data-stu-id="0cd03-126">On the Action Pane, on the **Shipments** tab, in the **Work** group, select **Work details**.</span></span>
1. <span data-ttu-id="0cd03-127">Patikrinti kiekvieno darbo ID būseną.</span><span class="sxs-lookup"><span data-stu-id="0cd03-127">Inspect the status of each work ID.</span></span> <span data-ttu-id="0cd03-128">Kiekvieno darbo ID, kurio būsena nėra Uždaryta *arba* Atšaukta *sekimas*.</span><span class="sxs-lookup"><span data-stu-id="0cd03-128">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="0cd03-129">Kai kiekvieno darbo ID būsena yra Uždaryta *arba* *Atšaukta, bandykite* dar kartą patvirtinti siuntą.</span><span class="sxs-lookup"><span data-stu-id="0cd03-129">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-work-page"></a><span data-ttu-id="0cd03-130">Visi darbo puslapiai</span><span class="sxs-lookup"><span data-stu-id="0cd03-130">All work page</span></span>

1. <span data-ttu-id="0cd03-131">Pasirinkite **Sandėlio valdymas \> Darbas \> Visi darbai**.</span><span class="sxs-lookup"><span data-stu-id="0cd03-131">Go to **Warehouse management \> Work\> All work**.</span></span>
1. <span data-ttu-id="0cd03-132">Pasirinkite užsakymo numerio darbą, pagal kurį siuntos patvirtinti negalima.</span><span class="sxs-lookup"><span data-stu-id="0cd03-132">Select the work for the order number that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="0cd03-133">Veiksmų srities skirtuko **Siuntimas** grupėje **Siuntimas** spustelėkite **Patvirtinti siuntimą**.</span><span class="sxs-lookup"><span data-stu-id="0cd03-133">On the Action Pane, on the **Shipment** tab, in the **Shipment** group, select **Confirm shipment**.</span></span>
1. <span data-ttu-id="0cd03-134">Patikrinti kiekvieno darbo ID būseną.</span><span class="sxs-lookup"><span data-stu-id="0cd03-134">Inspect the status of each work ID.</span></span> <span data-ttu-id="0cd03-135">Kiekvieno darbo ID, kurio būsena nėra Uždaryta *arba* Atšaukta *sekimas*.</span><span class="sxs-lookup"><span data-stu-id="0cd03-135">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="0cd03-136">Kai kiekvieno darbo ID būsena yra Uždaryta *arba* *Atšaukta, bandykite* dar kartą patvirtinti siuntą.</span><span class="sxs-lookup"><span data-stu-id="0cd03-136">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>
