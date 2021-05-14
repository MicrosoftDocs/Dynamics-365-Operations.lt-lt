---
title: Negalite patvirtinti siuntos, nes yra nulinis kiekis
description: Negalite patvirtinti siuntos, nes yra nulinis kiekis
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
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938517"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a><span data-ttu-id="b49cc-103">Negalite patvirtinti siuntos, nes yra nulinis kiekis</span><span class="sxs-lookup"><span data-stu-id="b49cc-103">You can't confirm a shipment because there is zero quantity</span></span>

<span data-ttu-id="b49cc-104">Klaidos kodas: LoadLineWarningUpdatedToZero</span><span class="sxs-lookup"><span data-stu-id="b49cc-104">Error code: LoadLineWarningUpdatedToZero</span></span>

## <a name="symptoms"></a><span data-ttu-id="b49cc-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="b49cc-105">Symptoms</span></span>

<span data-ttu-id="b49cc-106">Kai bandote patvirtinti siuntą, sistema rodo šį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="b49cc-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="b49cc-107">Prekės %1 ir siuntos %2 krovinio eilutė atnaujinta į nulinį kiekį dėl pristatymo trūkumo sąrankos, leidžiančios nesiųsti jokio šios prekės kiekio.</span><span class="sxs-lookup"><span data-stu-id="b49cc-107">Load line for item %1 and shipment %2 has been updated to have zero quantity due to underdelivery setup allowing not to ship any quantities for this item.</span></span>

<span data-ttu-id="b49cc-108">Todėl negalite patvirtinti krovinio siuntimo.</span><span class="sxs-lookup"><span data-stu-id="b49cc-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="b49cc-109">Priežastis</span><span class="sxs-lookup"><span data-stu-id="b49cc-109">Cause</span></span>

<span data-ttu-id="b49cc-110">Sistema įvertina, ar paimtas kiekis patenka į numatomus limitus, remdamasi paimtu kiekiu, krovinio eilutės kiekiu ir pristatymo pristatymo procentu.</span><span class="sxs-lookup"><span data-stu-id="b49cc-110">The system evaluates whether the picked quantity is within the expected limits, based on the picked quantity, load line quantity, and underdelivery percentage.</span></span> <span data-ttu-id="b49cc-111">Jei sistema nustato, kad krovinio eilutėje paimtas kiekis yra 0 (nulis), siuntos patvirtinti negalite.</span><span class="sxs-lookup"><span data-stu-id="b49cc-111">If the system finds that the picked quantity on the load line is 0 (zero), you can't confirm the shipment.</span></span> <span data-ttu-id="b49cc-112">Pavyzdžiui, šis išdavimas gali atsirasti, jei darbas buvo atšauktas, o pristatymo eilutėje pristatymo procentinė dalis yra 100 procentų.</span><span class="sxs-lookup"><span data-stu-id="b49cc-112">For example, this issue might occur if work has been canceled, and the underdelivery percentage on the load line is 100 percent.</span></span>

## <a name="resolution"></a><span data-ttu-id="b49cc-113">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="b49cc-113">Resolution</span></span>

<span data-ttu-id="b49cc-114">Patikrinkite krovinio eilutes, kad įsitikintumėte, jog pristatymo underdelive procentai ir kiekiai yra sulygiuoti su paimtu darbu.</span><span class="sxs-lookup"><span data-stu-id="b49cc-114">Check your load lines to make sure that the underdelivery percentage and quantities are aligned with the picked work.</span></span>

1. <span data-ttu-id="b49cc-115">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="b49cc-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="b49cc-116">Pasirinkite pakrovimą, kuriam siuntimo patvirtinti nepavyksta.</span><span class="sxs-lookup"><span data-stu-id="b49cc-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="b49cc-117">Krovinio **eilučių** „FastTab" pasirinkite prekės, viršijančios pristatymo pateisavimo procentinę dalį, krovinio eilutę.</span><span class="sxs-lookup"><span data-stu-id="b49cc-117">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="b49cc-118">Koreguokite lauko Pristatymo **Pristatymas ne iki galo** vertę arba **lauką** Kiekis.</span><span class="sxs-lookup"><span data-stu-id="b49cc-118">Adjust the value of the **Underdelivery** field or the **Quantity** field as required.</span></span>

> [!TIP]
> <span data-ttu-id="b49cc-119">Jei išdavimas vis tiek nėra fiksuotas, gali tekti atlikti daugiau susijusių pardavimo užsakymų arba perkėlimo užsakymų paėmimo darbų, kol turimas kiekis nesulygiuotas su kroviniu arba siunta.</span><span class="sxs-lookup"><span data-stu-id="b49cc-119">If the issue still isn't fixed, you might have to complete more picking work for the related sales orders or transfer orders until the available quantity is aligned with the load or shipment.</span></span>
