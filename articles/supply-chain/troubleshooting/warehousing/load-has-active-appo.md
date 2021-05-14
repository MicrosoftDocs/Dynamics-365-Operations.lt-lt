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
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a><span data-ttu-id="d20ac-103">Negalite patvirtinti siuntos dėl kalendoriaus išdavimo</span><span class="sxs-lookup"><span data-stu-id="d20ac-103">You can't confirm a shipment because of an issue with the calendar</span></span>

<span data-ttu-id="d20ac-104">Klaidos kodas: TRX2716</span><span class="sxs-lookup"><span data-stu-id="d20ac-104">Error code: TRX2716</span></span>

## <a name="symptoms"></a><span data-ttu-id="d20ac-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="d20ac-105">Symptoms</span></span>

<span data-ttu-id="d20ac-106">Kai bandote patvirtinti siuntą, sistema rodo šį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="d20ac-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="d20ac-107">Esant kalendoriaus tipui %1 būtina užregistruoti ir išregistruoti paskyrą %2.</span><span class="sxs-lookup"><span data-stu-id="d20ac-107">The calendar type %1 requires the appointment %2 to be checked in and out.</span></span>

<span data-ttu-id="d20ac-108">Todėl negalite patvirtinti krovinio siuntimo.</span><span class="sxs-lookup"><span data-stu-id="d20ac-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="d20ac-109">Priežastis</span><span class="sxs-lookup"><span data-stu-id="d20ac-109">Cause</span></span>

<span data-ttu-id="d20ac-110">Yra aktyvių krovinio paskyrų.</span><span class="sxs-lookup"><span data-stu-id="d20ac-110">Active appointments for the load exist.</span></span> <span data-ttu-id="d20ac-111">Pvz., yra taisyklė, pagal kurią reikalaujama vairuotojo įregistravimo.</span><span class="sxs-lookup"><span data-stu-id="d20ac-111">For example, there is a rule that requires driver check-in.</span></span> <span data-ttu-id="d20ac-112">Todėl krovinio būsena šiuo metu yra, kai siuntos patvirtinimas nesėkmingas.</span><span class="sxs-lookup"><span data-stu-id="d20ac-112">Therefore, the load is currently in a state where shipment confirmation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="d20ac-113">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="d20ac-113">Resolution</span></span>

<span data-ttu-id="d20ac-114">Turite išnagrinėti ir išspręsti visas problemas, susijusias su aktyviomis paskyromis, kurios susijusios su kroviniu.</span><span class="sxs-lookup"><span data-stu-id="d20ac-114">You must investigate and fix any issues with the active appointments that are linked to the load.</span></span>

1. <span data-ttu-id="d20ac-115">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="d20ac-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="d20ac-116">Pasirinkite pakrovimą, kuriam siuntimo patvirtinti nepavyksta.</span><span class="sxs-lookup"><span data-stu-id="d20ac-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="d20ac-117">Veiksmų srityje, skirtuke **Transportavimas**, grupėje **Susitikimai**, pasirinkite **Susitikimo planavimas**.</span><span class="sxs-lookup"><span data-stu-id="d20ac-117">On the Action Pane, on the **Transportation** tab, in the **Appointments** group, select **Appointment scheduling**.</span></span>
1. <span data-ttu-id="d20ac-118">Atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="d20ac-118">Follow one of these steps:</span></span>

    - <span data-ttu-id="d20ac-119">Įsitikinkite, kad vairuotojo registravimas / išregistravimas baigtas paskyrai vykdyti.</span><span class="sxs-lookup"><span data-stu-id="d20ac-119">Make sure that driver check-in/check-out is completed for the appointment.</span></span>
    - <span data-ttu-id="d20ac-120">Užbaikite arba atšaukite paskyrą.</span><span class="sxs-lookup"><span data-stu-id="d20ac-120">Complete or cancel the appointment.</span></span>
    - <span data-ttu-id="d20ac-121">Išjunkite **reikiamą susijusios paskyros taisyklės parinktį Vairuotojo** registravimasis.</span><span class="sxs-lookup"><span data-stu-id="d20ac-121">Disable the **Driver check-in required** option for the related appointment rule.</span></span>
