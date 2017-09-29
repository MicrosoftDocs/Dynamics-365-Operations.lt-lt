---
title: "Vėlesni čekiai"
description: "Šiame straipsnyje pateikta informacija apie vėlesnių čekių palaikymą programoje „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“. Vėlesni čekiai yra čekiai, išrašomi norint atlikti ir gauti mokėjimus ateityje. Todėl čekio negalima išgryninti iki nurodytos datos."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 45d28110ca93875eb534c69886ac2074ea4fe737
ms.openlocfilehash: 6a535b5f1192b7c27383cb8ece53f76a9c76f047
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2017

---

# <a name="postdated-checks"></a><span data-ttu-id="d9d85-105">Vėlesni čekiai</span><span class="sxs-lookup"><span data-stu-id="d9d85-105">Postdated checks</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d9d85-106">Šiame straipsnyje pateikta informacija apie vėlesnių čekių palaikymą programoje „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“.</span><span class="sxs-lookup"><span data-stu-id="d9d85-106">This article provides information about support for postdated checks in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="d9d85-107">Vėlesni čekiai yra čekiai, išrašomi norint atlikti ir gauti mokėjimus ateityje.</span><span class="sxs-lookup"><span data-stu-id="d9d85-107">Postdated checks are checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="d9d85-108">Todėl čekio negalima išgryninti iki nurodytos datos.</span><span class="sxs-lookup"><span data-stu-id="d9d85-108">Therefore, the check can't be cashed until the specified date.</span></span>

<span data-ttu-id="d9d85-109">„Microsoft Dynamics 365 for Finance and Operations“ palaiko visą vėlesnių čekių valdymo ciklą ir Gautinose sumose, ir Mokėtinose sumose, kaip parodyta pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="d9d85-109">Microsoft Dynamics 365 for Finance and Operations supports the full management cycle for postdated checks in both Accounts receivable and Accounts payable, as shown in the following table.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9d85-110">Scenarijus</span><span class="sxs-lookup"><span data-stu-id="d9d85-110">Scenario</span></span></th>
<th><span data-ttu-id="d9d85-111">Išsami informacija</span><span class="sxs-lookup"><span data-stu-id="d9d85-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9d85-112">Vėlesnių čekių nustatymas</span><span class="sxs-lookup"><span data-stu-id="d9d85-112">Set up postdated checks</span></span></td>
<td><span data-ttu-id="d9d85-113">Turite nustatyti naują mokėjimo būdą ir nurodyti reguliarią mokėjimo procedūrą išrašytų čekių, gautų čekių ir išskaitomo mokesčio atsiskaitymo sąskaitoms.</span><span class="sxs-lookup"><span data-stu-id="d9d85-113">You must set up a new payment method, and specify the payment routine for clearing accounts for issued checks, received checks, and withholding tax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9d85-114">Vėlesnio tiekėjo čekio užregistravimas</span><span class="sxs-lookup"><span data-stu-id="d9d85-114">Register and post a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="d9d85-115">Registruokite vėlesnių čekių, išrašytų tiekėjui, išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="d9d85-115">Register the details of a postdated check that you issue to a vendor.</span></span> <span data-ttu-id="d9d85-116">Užregistravus mokėjimą tiekėjo įsipareigojimai pripažįstami, bet banko sąskaita nėra dar kredito sąskaita.</span><span class="sxs-lookup"><span data-stu-id="d9d85-116">When the payment is posted, the vendor liability is recognized, but the bank account isn’t yet credit.</span></span> <span data-ttu-id="d9d85-117">Vietoj to, šiuo tikslu naudojama atsiskaitymo sąskaita.</span><span class="sxs-lookup"><span data-stu-id="d9d85-117">Instead, a clearing account is used for this purpose.</span></span> </td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9d85-118">Registruoti kliento vėlesnį čekį</span><span class="sxs-lookup"><span data-stu-id="d9d85-118">Register and post a postdated check for a customer</span></span></td>
<td><span data-ttu-id="d9d85-119">Užregistruokite išsamią vėlesnio iš kliento gauto čekio informaciją.</span><span class="sxs-lookup"><span data-stu-id="d9d85-119">Register the details of a postdated check that you receive from a customer.</span></span> <span data-ttu-id="d9d85-120">Užregistravus mokėjimą kliento gaunama suma yra kreditas, bet banko sąskaita dar nėra debeto sąskaita.</span><span class="sxs-lookup"><span data-stu-id="d9d85-120">When the payment is posted, the customer receivable is credit, but the bank account isn’t yet debit.</span></span> <span data-ttu-id="d9d85-121">Vietoj to, šiuo tikslu naudojama atsiskaitymo sąskaita.</span><span class="sxs-lookup"><span data-stu-id="d9d85-121">Instead, a clearing account is used for this purpose.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9d85-122">Vėlesnio kliento arba tiekėjo čekio pakeitimo užregistravimas</span><span class="sxs-lookup"><span data-stu-id="d9d85-122">Register and post a replacement postdated check for a customer or a vendor</span></span></td>
<td>
<span data-ttu-id="d9d85-123">Jei pamesite arba sugadinsite pradinį čekį tiekėjui arba gautą iš kliento, galėsite išduoti pakeitimo vėlesnį čekį.</span><span class="sxs-lookup"><span data-stu-id="d9d85-123">If your original check to a vendor or from a customer is lost or damaged, you can issue a replacement postdated check.</span></span> <span data-ttu-id="d9d85-124">Kai užregistruosite išsamią čekio informaciją, pateikite nuorodą į pradinį čekį ir nurodykite, kad naujasis čekis yra pradinio čekio pakaitalas.</span><span class="sxs-lookup"><span data-stu-id="d9d85-124">When you register the check details, provide a reference to the original check, and indicate that the new check is a replacement for the original.</span></span> <span data-ttu-id="d9d85-125">Taip pat galite užregistruoti pakeitimo čekį.</span><span class="sxs-lookup"><span data-stu-id="d9d85-125">You can also post the replacement check.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9d85-126">Kliento vėlesnio čekio perkėlimas tiekėjui</span><span class="sxs-lookup"><span data-stu-id="d9d85-126">Transfer a customer postdated check to a vendor</span></span></td>
<td><span data-ttu-id="d9d85-127">Kai gaunate vėlesnį čekį iš kliento, galite perduoti čekį tiekėjui kaip mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="d9d85-127">When you receive a postdated check from a customer, you can transfer that check to a vendor as a payment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9d85-128">Vėlesnio kliento arba tiekėjo čekio sudengimas</span><span class="sxs-lookup"><span data-stu-id="d9d85-128">Settle a postdated check for a customer or a vendor</span></span></td>
<td><span data-ttu-id="d9d85-129">Sudenkite kliento arba tiekėjo vėlesnį čekį, užregistruotą tarpinėje sąskaitoje, kaip čekio terminas galiausiai sueis.</span><span class="sxs-lookup"><span data-stu-id="d9d85-129">Settle a postdated check that is posted to a bridging account for a customer or a vendor when the check finally matures.</span></span> <span data-ttu-id="d9d85-130">Sudengus čekį, banko sąskaita galiausiai yra debetas ar kreditas, pagal atsiskaitymo sąskaitą, kuri buvo naudota anksčiau.</span><span class="sxs-lookup"><span data-stu-id="d9d85-130">When the check is settled, the bank is finally debit or credit against the clearing account that was used earlier.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9d85-131">Vėlesnio tiekėjo čekio atšaukimas</span><span class="sxs-lookup"><span data-stu-id="d9d85-131">Cancel a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="d9d85-132">Šiais atvejais užregistruotą vėlesnį čekį galite atšaukti: – Bankas čekį grąžina.</span><span class="sxs-lookup"><span data-stu-id="d9d85-132">You can cancel a posted postdated check in these situations: - The check is returned by the bank.</span></span>
<span data-ttu-id="d9d85-133">- Čekis taikomas netinkamai sąskaitai faktūrai.</span><span class="sxs-lookup"><span data-stu-id="d9d85-133">- The check is applied to an incorrect invoice.</span></span>
<span data-ttu-id="d9d85-134">- Mokėjimas grynaisiais pinigais atliktas ne pagal čekį.</span><span class="sxs-lookup"><span data-stu-id="d9d85-134">- A cash payment is made against the check.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9d85-135">Vėlesnio čekio mokėjimo stabdymas</span><span class="sxs-lookup"><span data-stu-id="d9d85-135">Stop payment for a postdated check</span></span></td>
<td><span data-ttu-id="d9d85-136">Galite sustabdyti mokėjimą vėlesniame čekyje, kuris buvo išduotas tiekėjui dėl tokių priežasčių, kaip nepakankamos lėšos, sutarties su tiekėju sąlygų pakeitimai, tiekėjo prekių su defektais atsiuntimas arba prekių gražinimas tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="d9d85-136">You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor.</span></span> <span data-ttu-id="d9d85-137">Galite sustabdyti tik neapmokėtų čekių mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="d9d85-137">You can stop payment only on checks that haven’t cleared.</span></span></td>
</tr>
</tbody>
</table>



<span data-ttu-id="d9d85-138">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="d9d85-138">For more information, see the following topics:</span></span>

[<span data-ttu-id="d9d85-139">Vėlesnių čekių nustatymas</span><span class="sxs-lookup"><span data-stu-id="d9d85-139">Set up postdated checks</span></span>](tasks/set-up-postdated-checks.md)

[<span data-ttu-id="d9d85-140">Registruoti kliento vėlesnį čekį</span><span class="sxs-lookup"><span data-stu-id="d9d85-140">Register and post a postdated check for a customer</span></span>](tasks/register-post-postdated-check-customer.md)

[<span data-ttu-id="d9d85-141">Vėlesnio čekio iš kliento sudengimas</span><span class="sxs-lookup"><span data-stu-id="d9d85-141">Settle a postdated check from a customer</span></span>](tasks/settle-postdated-check-customer.md)

[<span data-ttu-id="d9d85-142">Registruoti tiekėjo vėlesnį čekį</span><span class="sxs-lookup"><span data-stu-id="d9d85-142">Register and post a postdated check for a vendor</span></span>](tasks/register-post-postdated-check-vendor.md) 

[<span data-ttu-id="d9d85-143">Vėlesnio tiekėjo čekio sudengimas</span><span class="sxs-lookup"><span data-stu-id="d9d85-143">Settle a postdated check for a vendor</span></span>](tasks/settle-postdated-check-vendor.md)



