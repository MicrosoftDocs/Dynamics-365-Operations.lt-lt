---
title: Įsigijimo trikčių diagnostika ir šaltinio pasirinkimo darbo eigos
description: Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti dirbant su įsigijimo ir šaltinio pasirinkimo darbo eigomis.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cdedc45b8f057310801f134104156a732fb58d86
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434019"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a><span data-ttu-id="7fafd-103">Įsigijimo trikčių diagnostika ir šaltinio pasirinkimo darbo eigos</span><span class="sxs-lookup"><span data-stu-id="7fafd-103">Troubleshoot procurement and sourcing workflows</span></span>

<span data-ttu-id="7fafd-104">Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti dirbant su įsigijimo ir šaltinio pasirinkimo darbo eigomis.</span><span class="sxs-lookup"><span data-stu-id="7fafd-104">This topic describes how to fix issues that you might encounter while you work with procurement and sourcing workflows.</span></span>

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a><span data-ttu-id="7fafd-105">Klaida iš naujo pateikiant pirkimo užsakymą darbo eigai po pakeitimo: „Pirkimo užsakymo X pakeitimai yra leidžiami tik juodraštyje, kai suaktyvinamas keitimų valdymas”</span><span class="sxs-lookup"><span data-stu-id="7fafd-105">Error when re-submitting a purchase order to the workflow after a change: "Changes to purchase order X are allowed only in a Draft state when change management is activated"</span></span>

<span data-ttu-id="7fafd-106">Ši problema kyla tik tada, kai pirkimo užsakymo būsena buvo *Patvirtinta* dar prieš tai, kai pareikalavote pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="7fafd-106">This issue occurs only if the purchase order was in a *Confirmed* state before you requested changes.</span></span> <span data-ttu-id="7fafd-107">Jei pareikalaujate pakeitimų, kai pirkimo užsakymo būsena yra *Patvirtinta*, tada darbo eigą pavyks sėkmingai apdoroti.</span><span class="sxs-lookup"><span data-stu-id="7fafd-107">If you request changes while the purchase order is in an *Approved* state, the workflow can be processed successfully.</span></span>

### <a name="error-description"></a><span data-ttu-id="7fafd-108">Klaidos aprašas</span><span class="sxs-lookup"><span data-stu-id="7fafd-108">Error description</span></span>

<span data-ttu-id="7fafd-109">Ši klaida įvyksta darbo eigoje, kai pirkimo užsakymas iš naujo pateikiamas po jo pakeitimo:</span><span class="sxs-lookup"><span data-stu-id="7fafd-109">The following error occurs in the workflow when a purchase order is resubmitted after a change:</span></span>

> <span data-ttu-id="7fafd-110">Sustabdyta (klaida): X++ Išimtis: Pirkimo užsakymo PO0000569 pakeitimai leidžiami tik būsenos juodraštyje, kai įjungiamas keitimų valdymas</span><span class="sxs-lookup"><span data-stu-id="7fafd-110">Stopped (error): X++ Exception: Changes to purchase order PO0000569 are only allowed in state Draft when change management is activated at</span></span><br>
<span data-ttu-id="7fafd-111">SysWorkflowParticipantProvider-resolve</span><span class="sxs-lookup"><span data-stu-id="7fafd-111">SysWorkflowParticipantProvider-resolve</span></span><br>
<span data-ttu-id="7fafd-112">SysWorkflowParticipantProvider-resolveParticipants</span><span class="sxs-lookup"><span data-stu-id="7fafd-112">SysWorkflowParticipantProvider-resolveParticipants</span></span><br>
<span data-ttu-id="7fafd-113">SysWorkflowServiceProvider-resolveParticipant</span><span class="sxs-lookup"><span data-stu-id="7fafd-113">SysWorkflowServiceProvider-resolveParticipant</span></span><br>
<span data-ttu-id="7fafd-114">SysWorkflowQueue-resume</span><span class="sxs-lookup"><span data-stu-id="7fafd-114">SysWorkflowQueue-resume</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7fafd-115">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="7fafd-115">Issue resolution</span></span>

<span data-ttu-id="7fafd-116">Ši problema gali atsirasti dėl pirkimo užsakymo paskirstymų nenuoseklumo.</span><span class="sxs-lookup"><span data-stu-id="7fafd-116">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="7fafd-117">Norėdami atblokuoti šią problemą ir iš naujo nustatyti pirkimo užsakymą į būseną *Juodraštis*, eikite į **Įsigijimas ir šaltinio pasirinkimas \> Periodinės užduotys \> Valymas \> Pirkimo užsakymo paskirstymo nustatymas iš naujo**.</span><span class="sxs-lookup"><span data-stu-id="7fafd-117">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="7fafd-118">Norėdami gauti daugiau informacijos, peržiūrėkite šį tinklaraščio įrašą: [Pašalinti PO paskirstymo klaidas „Dynamics 365 Supply Chain Management”](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="7fafd-118">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

<span data-ttu-id="7fafd-119">Problema bus išspręsta naudojant [šį „Microsoft” žinių bazės (KB) straipsnį](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span><span class="sxs-lookup"><span data-stu-id="7fafd-119">The issue will be fixed through [this Microsoft Knowledge Base (KB) article](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="7fafd-120">Vienas ar daugiau apskaitos paskirstymų yra paskirstytas per daug arba per mažai.</span><span class="sxs-lookup"><span data-stu-id="7fafd-120">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

<span data-ttu-id="7fafd-121">Ši problema gali atsirasti dėl pirkimo užsakymo paskirstymų nenuoseklumo.</span><span class="sxs-lookup"><span data-stu-id="7fafd-121">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="7fafd-122">Norėdami atblokuoti šią problemą ir iš naujo nustatyti pirkimo užsakymą į būseną *Juodraštis*, eikite į **Įsigijimas ir šaltinio pasirinkimas \> Periodinės užduotys \> Valymas \> Pirkimo užsakymo paskirstymo nustatymas iš naujo**.</span><span class="sxs-lookup"><span data-stu-id="7fafd-122">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="7fafd-123">Norėdami gauti daugiau informacijos, peržiūrėkite šį tinklaraščio įrašą: [Pašalinti PO paskirstymo klaidas „Dynamics 365 Supply Chain Management”](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="7fafd-123">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a><span data-ttu-id="7fafd-124">Jei pristatymo likutis atšaukiamas pirkimo užsakyme, kur įjungtas keitimų valdymas, pirkimo užsakymo būsena yra patvirtinta.</span><span class="sxs-lookup"><span data-stu-id="7fafd-124">If a delivery remainder is canceled on a purchase order where change management is turned on, the purchase order goes to a Confirmed state.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7fafd-125">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="7fafd-125">Issue description</span></span>

<span data-ttu-id="7fafd-126">Jei vienintelis prašomas pirkimo užsakymo, kuriam taikomas keitimų valdymas, pakeitimas yra pristatymo likučio panaikinimas vienoje ar keliose eilutėse, pirkimo užsakymas bus priskirtas tiesiai į *Patvirtintą* būseną, kai jis bus patvirtintas, o žurnalas nebus sukurtas.</span><span class="sxs-lookup"><span data-stu-id="7fafd-126">For a purchase order that is subject to change management, if the only change that is requested is the cancellation of a delivery remainder on one or more of the lines, the purchase order will go directly to a *Confirmed* state when it's approved, and no journal will be created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7fafd-127">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="7fafd-127">Issue resolution</span></span>

<span data-ttu-id="7fafd-128">Pristatymo likučio atšaukimas nedaro poveikio patvirtinimo žurnalo turiniui.</span><span class="sxs-lookup"><span data-stu-id="7fafd-128">Cancellation of a delivery remainder doesn't affect the contents of the confirmation journal.</span></span> <span data-ttu-id="7fafd-129">Ši funkcija turėtų būti naudojama, kai eilutė buvo gauta iš dalies ir likučio kiekis turėtų būti atšauktas proceso etape po to, kai pirkimo užsakymas yra patvirtintas tiekėjo.</span><span class="sxs-lookup"><span data-stu-id="7fafd-129">This functionality should be used when the line has been partially received, and the remainder quality should be canceled in the process step after the purchase order has been confirmed with the vendor.</span></span>

<span data-ttu-id="7fafd-130">Jei tai turi atsispindėti pirkimo užsakymo patvirtinime, kiekis turi būti pakoreguotas pirkimo užsakymo eilutėje, kad būtų reikalingas patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="7fafd-130">If this should be reflected on the purchase order confirmation, the quantity should be adjusted on the purchase order line so that the confirmation will be required.</span></span> <span data-ttu-id="7fafd-131">Taip pat, jei eilutėje nieko negauta, kiekis gali būti pašalintas.</span><span class="sxs-lookup"><span data-stu-id="7fafd-131">Alternatively, if nothing has been received on the line, the quantity can be removed.</span></span> <span data-ttu-id="7fafd-132">Šiuo atveju reikės patvirtinti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="7fafd-132">In this case, reconfirmation will be required.</span></span>

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a><span data-ttu-id="7fafd-133">Atšaukti pirkimo užsakymai rodomi juodraštyje, esančiame pirkimo užsakymo paruošimo darbo srityje.</span><span class="sxs-lookup"><span data-stu-id="7fafd-133">Canceled purchase orders appear in the draft list in the Purchase order preparation workspace.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7fafd-134">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="7fafd-134">Issue description</span></span>

<span data-ttu-id="7fafd-135">Atšaukus pirkimo užsakymus, kurių būsena buvo *Patvirtinta*, atšaukti pirkimo užsakymai vis dar rodomi **Pirkimo užsakymo paruošimo** darbo srities pirkimo užsakymų juodraščių sąraše.</span><span class="sxs-lookup"><span data-stu-id="7fafd-135">After you cancel purchase orders that were in a *Confirmed* state, the canceled purchase orders still appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7fafd-136">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="7fafd-136">Issue resolution</span></span>

<span data-ttu-id="7fafd-137">Ši problema kyla tik pirkimo užsakymams, kuriems taikomas keitimų valdymas.</span><span class="sxs-lookup"><span data-stu-id="7fafd-137">This issue occurs only for purchase orders that are subject to change management.</span></span> <span data-ttu-id="7fafd-138">Tai įvyksta, nes atšaukimas laikomas pakeitimu, kuris turi būti patvirtintas.</span><span class="sxs-lookup"><span data-stu-id="7fafd-138">It occurs because the cancellation is considered a change that must be approved.</span></span> <span data-ttu-id="7fafd-139">Šį patvirtinimą sistema gali atlikti automatiškai.</span><span class="sxs-lookup"><span data-stu-id="7fafd-139">The approval can be done automatically by the system.</span></span> <span data-ttu-id="7fafd-140">Todėl reikalingas procesas pateikti atšauktą pirkimo užsakymą į patvirtinimo darbo eigą, kad jis galėtų patekti į *Patvirtintą* būseną.</span><span class="sxs-lookup"><span data-stu-id="7fafd-140">Therefore, the process is to submit the canceled purchase order to the approval workflow so that it can go to an *Approved* state.</span></span> <span data-ttu-id="7fafd-141">Tuo metu pirkimo užsakymas nebebus rodomas **Pirkimo užsakymo paruošimo** darbo srities pirkimo užsakymų juodraščių sąraše.</span><span class="sxs-lookup"><span data-stu-id="7fafd-141">At that point, the purchase order will no longer appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

