---
title: "Atšaukti gamybos užsakymo būseną"
description: "Šioje temoje aprašoma, kaip atšaukti gamybos užsakymo būseną."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmStatusDecrease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 10ce698ef07e9f290547b0eedd7c357f54852e76
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="reverse-the-production-order-status"></a><span data-ttu-id="1d927-103">Atšaukti gamybos užsakymo būseną</span><span class="sxs-lookup"><span data-stu-id="1d927-103">Reverse the production order status</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1d927-104">Šioje temoje aprašoma, kaip atšaukti gamybos užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="1d927-104">This topic describes how to reverse production order status.</span></span> 

<span data-ttu-id="1d927-105">Atšaukus gamybos užsakymo būseną, užsakymas ir visos operacijos, susijusios su maršrutais, grįš į ankstesnį gamybos ciklo etapą.</span><span class="sxs-lookup"><span data-stu-id="1d927-105">If you reverse the status of a production order, the order and all operations that are associated with the routes revert to a previous step in the production life cycle.</span></span> <span data-ttu-id="1d927-106">Pavyzdžiui, jei gamybos užsakymo būsena yra **Suplanuota**, o jūs pakeičiate ją atgal į **Sukurta**.</span><span class="sxs-lookup"><span data-stu-id="1d927-106">For example, a production order has a status of **Scheduled**, and you change the status back to **Created**.</span></span> <span data-ttu-id="1d927-107">Šiuo atveju sistema pirmiausia turi pakeisti būseną į **Įvertinta**, kuri eina prieš būseną **Suplanuota**.</span><span class="sxs-lookup"><span data-stu-id="1d927-107">In this case, the system must first change the status to **Estimated**, which is the status that immediately precedes **Scheduled**.</span></span> <span data-ttu-id="1d927-108">Tada būseną galima pakeisti į tą, kurios norite, pvz., **Sukurta**.</span><span class="sxs-lookup"><span data-stu-id="1d927-108">It can then change the status to the status that you want, **Created**.</span></span> <span data-ttu-id="1d927-109">**Pastaba.** Jei jūsų užsakymas pasiekė būseną **Paskelbti baigtu** vis tiek galite gražinti jį į ankstesnę būseną.</span><span class="sxs-lookup"><span data-stu-id="1d927-109">**Note:** If your order has reached the **Report as finished** status, you can still reverse it to an earlier status.</span></span> <span data-ttu-id="1d927-110">Tačiau norėdami atnaujinti užsakymo informaciją turite iš naujo paleisti įvertinimą ir operacijų planavimą, užduočių planavimą arba abiejų tipų planavimą.</span><span class="sxs-lookup"><span data-stu-id="1d927-110">However, you must re-run estimation and operations scheduling, job scheduling, or both types of scheduling, to update the information on the order.</span></span> <span data-ttu-id="1d927-111">Taip yra todėl, kad bet koks likusios prekės rezervavimo ir operacijų išteklių suvartojimas taip pat turi būti atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="1d927-111">This step is required, because any reservations of remaining item consumption and operations resource consumption must also be reset.</span></span> <span data-ttu-id="1d927-112">Toliau šiame straipsnyje aprašoma, kas rodoma, kai atšaukiate gamybos užsakymo būseną šiais būdais.</span><span class="sxs-lookup"><span data-stu-id="1d927-112">The rest of this article explains what occurs when you reverse the status of a production order in the following ways:</span></span>

-   <span data-ttu-id="1d927-113">Iš **Įvertinta** į **Sukurta**</span><span class="sxs-lookup"><span data-stu-id="1d927-113">From **Estimated** to **Created**</span></span>
-   <span data-ttu-id="1d927-114">Iš **Suplanuota** į **Įvertinta**</span><span class="sxs-lookup"><span data-stu-id="1d927-114">From **Scheduled** to **Estimated**</span></span>
-   <span data-ttu-id="1d927-115">Iš **Išleista** į **Suplanuota**</span><span class="sxs-lookup"><span data-stu-id="1d927-115">From **Released** to **Scheduled**</span></span>
-   <span data-ttu-id="1d927-116">Iš **Pradėta** į **Išleista**</span><span class="sxs-lookup"><span data-stu-id="1d927-116">From **Started** to **Released**</span></span>

## <a name="from-estimated-to-created"></a><span data-ttu-id="1d927-117">Iš Įvertinta į Sukurta</span><span class="sxs-lookup"><span data-stu-id="1d927-117">From Estimated to Created</span></span>
<span data-ttu-id="1d927-118">Grąžinus gamybos užsakymo būseną iš **Įvertinta** į **Sukurta**, į komplektavimo specifikaciją (KS) įtrauktų apskaičiuoto prekių suvartojimo duomenys bus pašalinti.</span><span class="sxs-lookup"><span data-stu-id="1d927-118">When you reverse the status of a production order from **Estimated** to **Created**, the item consumption that was calculated for the items in the bill of materials (BOM) is removed.</span></span> <span data-ttu-id="1d927-119">Atsargų operacijos gamybos eilutėje naikinamos ir gamybos KS eilučių laukas **Likučio būsena** nustatomas kaip **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="1d927-119">Inventory transactions on the production line are deleted, and the **Remain status** field on the production order's BOM lines is reset to **Ended**.</span></span> <span data-ttu-id="1d927-120">Pasirinkus parinktis **Išvestiniai pirkimai** ir **Išvestinė gamyba**, visi esami pirkimo arba gamybos užsakymai panaikinami.</span><span class="sxs-lookup"><span data-stu-id="1d927-120">When the **Derived purchases** and **Derived production** options are selected, any underlying purchase orders or production orders are deleted.</span></span> <span data-ttu-id="1d927-121">Jei įvertinote gamybos užsakymo išlaidas arba rankiniu būdu rezervavote prekes, kad jas būtų galima naudoti gamyboje, šios operacijos bus pašalintos.</span><span class="sxs-lookup"><span data-stu-id="1d927-121">If you estimated the costs of the production order, or if you manually reserved items so that they could be used in production, those transactions are removed.</span></span>

## <a name="from-scheduled-to-estimated"></a><span data-ttu-id="1d927-122">Iš Suplanuota į Įvertinta</span><span class="sxs-lookup"><span data-stu-id="1d927-122">From Scheduled to Estimated</span></span>
<span data-ttu-id="1d927-123">Grąžinus gamybos užsakymo būseną iš **Suplanuota** į **Įvertinta**, suplanuotos pradžios ir pabaigos datos ir laikai bus pašalinti.</span><span class="sxs-lookup"><span data-stu-id="1d927-123">When you reverse the status of a production order from **Scheduled** to **Estimated**, the scheduled start and end dates and times are removed.</span></span> <span data-ttu-id="1d927-124">Planavimo metu įvykdytas pajėgumo rezervavimas yra pašalinamas, o užduotys, sukurtos užduočių planavimo metu, yra naikinamos.</span><span class="sxs-lookup"><span data-stu-id="1d927-124">Capacity reservations that were made during scheduling are removed, and jobs that were created during job scheduling are deleted.</span></span> <span data-ttu-id="1d927-125">Visa informacija apie operacijų planavimą ir užduočių planavimą, įrašoma puslapyje **Gamybos užsakymo informacija**, bus atnaujinta.</span><span class="sxs-lookup"><span data-stu-id="1d927-125">All information that is recorded about operation scheduling and job scheduling on the **Production order details** page is reset.</span></span>

## <a name="from-released-to-scheduled"></a><span data-ttu-id="1d927-126">Iš Išleista į Suplanuota</span><span class="sxs-lookup"><span data-stu-id="1d927-126">From Released to Scheduled</span></span>
<span data-ttu-id="1d927-127">Grąžinus gamybos užsakymo būseną iš **Išleista** į **Suplanuota**, pasikeis tik būsenos lauke rodoma būsena.</span><span class="sxs-lookup"><span data-stu-id="1d927-127">When you reverse the status of a production order from **Released** to **Scheduled**, the only change that occurs is the value in the status field.</span></span>

## <a name="from-started-to-released"></a><span data-ttu-id="1d927-128">Iš Pradėta į Išleista</span><span class="sxs-lookup"><span data-stu-id="1d927-128">From Started to Released</span></span>
<span data-ttu-id="1d927-129">Grąžinus gamybos užsakymo būseną iš **Pradėta** į **Išleista**, visos prekės, kurios buvo paskelbtos baigtomis, bus grąžintos.</span><span class="sxs-lookup"><span data-stu-id="1d927-129">When you reverse the status of a production order from **Started** to **Released**, all items that were reported as finished are reverted.</span></span> <span data-ttu-id="1d927-130">Jei medžiagos buvo surinktos arba jei gautos ir siunčiamos siuntos buvo gaminamos, šie parametrai atšaukiami.</span><span class="sxs-lookup"><span data-stu-id="1d927-130">If material has been picked, or if inbound and outbound deliveries have been made to production, those settings are reversed.</span></span> <span data-ttu-id="1d927-131">Gamybos užsakymo KS eilučių lauko **Likučio būsena** vertė pasikeičia iš **Baigta** į **Medžiagų suvartojimas**.</span><span class="sxs-lookup"><span data-stu-id="1d927-131">The **Remain status** field on the production order’s BOM lines is changed from **Ended** to **Material consumption**.</span></span> <span data-ttu-id="1d927-132">Jei buvo užregistruotas laikas arba gamybos maršruto operacijai nustatytas kiekis buvo paskelbtas baigtu, šie parametrai bus atšaukti.</span><span class="sxs-lookup"><span data-stu-id="1d927-132">If time has been registered, or if quantities have been reported as finished for the operations in the production route, those settings are reversed.</span></span> <span data-ttu-id="1d927-133">Gamybos maršruto lauke **Likučio būsena** pasikeičia iš **Baigta** į **Maršruto suvartojimas**.</span><span class="sxs-lookup"><span data-stu-id="1d927-133">The **Remain status** field is changed from **Ended** to **Route consumption** in the production route.</span></span> <span data-ttu-id="1d927-134">Atšaukiami visų prekių, kurios užregistruotos kaip apdorojamos arba kurių gamyba nebaigta, parametrai.</span><span class="sxs-lookup"><span data-stu-id="1d927-134">The settings for all items that are posted as in process or work in process are reversed.</span></span> <span data-ttu-id="1d927-135">**Gamybos užsakymo informacijos** puslapio laukai, kuriuose nurodomas pradėtas gaminti arba paskelbtas baigtu kiekis, nustatomi iš naujo.</span><span class="sxs-lookup"><span data-stu-id="1d927-135">On the **Production order details** page, fields that show a quantity that was started or reported as finished are reset.</span></span> <span data-ttu-id="1d927-136">Šių operacijų datos taip pat nustatomos iš naujo.</span><span class="sxs-lookup"><span data-stu-id="1d927-136">The dates for those transactions are also reset.</span></span>



