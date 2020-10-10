---
title: Pardavimo užsakymų trikčių šalinimas
description: Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su pardavimo užsakymais.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage
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
ms.openlocfilehash: 6e51723915892f465ce09d09ee9ed622bab9451e
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889462"
---
# <a name="troubleshoot-sales-orders"></a><span data-ttu-id="2bf49-103">Pardavimo užsakymų trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="2bf49-103">Troubleshoot sales orders</span></span>

<span data-ttu-id="2bf49-104">Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su pardavimo užsakymais.</span><span class="sxs-lookup"><span data-stu-id="2bf49-104">This topic describes how to fix issues that you might encounter while you work with sales orders.</span></span>

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a><span data-ttu-id="2bf49-105">Mokesčių informacija nėra atnaujinama, jei pakeisiu vietą pardavimo užsakymo antraštėje.</span><span class="sxs-lookup"><span data-stu-id="2bf49-105">The tax information isn't updated if I change the location on a sales order header.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2bf49-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="2bf49-106">Issue description</span></span>

<span data-ttu-id="2bf49-107">Jei vieta, sandėlis arba pristatymo adresas pakeistas pardavimo užsakymo antraštėje arba eilutės lygiu, šiuo atveju mokesčių informacija nėra automatiškai atnaujinama eilutėse.</span><span class="sxs-lookup"><span data-stu-id="2bf49-107">If the site, warehouse, or delivery address is changed either on a sales order header or at the line level, the case tax information isn't automatically updated for the lines.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2bf49-108">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="2bf49-108">Issue resolution</span></span>

<span data-ttu-id="2bf49-109">Toks veikimo būdas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="2bf49-109">This behavior is by design.</span></span> <span data-ttu-id="2bf49-110">Problema kyla dėl to, kad pristatymo adresas, vieta ir sandėlis taip pat nėra automatiškai keičiami eilutės lygiu.</span><span class="sxs-lookup"><span data-stu-id="2bf49-110">The issue occurs because the delivery address, site, and warehouse aren't automatically changed at the line level either.</span></span> <span data-ttu-id="2bf49-111">Turite juos atnaujinti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="2bf49-111">You must update them manually.</span></span>

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a><span data-ttu-id="2bf49-112">Jei tam pačiam laikotarpiui ar persidengiantiems laikotarpiams yra dvi prekybos sutartys, visada pasirenkama ta pati sutarties eilutė.</span><span class="sxs-lookup"><span data-stu-id="2bf49-112">If there are two trade agreements for the same period or overlapping periods, the same agreement line is always selected.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2bf49-113">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="2bf49-113">Issue description</span></span>

<span data-ttu-id="2bf49-114">Jei tam pačiam laikotarpiui ar persidengiantiems laikotarpiams yra nustatytos dvi prekybos sutartys, atrodo, kad ta pati prekybos sutartis pasirenkama kiekvieną kartą, kai sukuriate pardavimo užsakymo eilutes, kuriose yra tos prekės.</span><span class="sxs-lookup"><span data-stu-id="2bf49-114">If two trade agreements are defined for the same period or overlapping periods, the same trade agreement seems to be selected every time when you create sales order lines that contain those items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2bf49-115">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="2bf49-115">Issue resolution</span></span>

<span data-ttu-id="2bf49-116">Jei nurodytą datą yra daugiau nei viena prekybos sutartis, visada pasirenkama prekybos sutartis, turinti žemiausią kainą.</span><span class="sxs-lookup"><span data-stu-id="2bf49-116">If there is more than one trade agreement for a given date, the trade agreement that has the lowest price is always selected.</span></span> <span data-ttu-id="2bf49-117">Norėdami gauti daugiau informacijos, atsisiųskite šią techninę dokumentaciją: [Prekybos sutartys „Microsoft Dynamics AX” 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span><span class="sxs-lookup"><span data-stu-id="2bf49-117">For more information, download the following white paper: [Trade agreements in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span></span>

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a><span data-ttu-id="2bf49-118">Ar galiu susieti pirkimo užsakymą su pardavimo užsakymu, siekiant įvykdyti paklausą?</span><span class="sxs-lookup"><span data-stu-id="2bf49-118">Can I link a purchase order to a sales order to fulfill demand?</span></span>

<span data-ttu-id="2bf49-119">Galite sukurti pirkimo užsakymą naudojant pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="2bf49-119">You can create a purchase order from a sales order.</span></span> <span data-ttu-id="2bf49-120">Norėdami gauti daugiau informacijos, žr. [Pirkimo užsakymo kūrimas naudojant pardavimo užsakymą](tasks/create-purchase-order-sales-order.md).</span><span class="sxs-lookup"><span data-stu-id="2bf49-120">For more information, see [Create a purchase order from a sales order](tasks/create-purchase-order-sales-order.md).</span></span>

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a><span data-ttu-id="2bf49-121">Negaliu atšaukti arba panaikinti grąžinimo užsakymą arba pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="2bf49-121">I can't cancel or delete a return order or a sales order.</span></span>

<span data-ttu-id="2bf49-122">Galite atšaukti tik pardavimo užsakymus ir grąžinimo užsakymus, kurie yra būsenoje *Sukurta*.</span><span class="sxs-lookup"><span data-stu-id="2bf49-122">You can cancel only sales orders and return orders that are in a *Created* state.</span></span> <span data-ttu-id="2bf49-123">Norėdami gauti daugiau informacijos, žr. [Grąžinimo užsakymo atšaukimas](../service-management/cancel-return-order.md).</span><span class="sxs-lookup"><span data-stu-id="2bf49-123">For more information, see [Cancel a return order](../service-management/cancel-return-order.md).</span></span>

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a><span data-ttu-id="2bf49-124">Bandant atšaukti pardavimo užsakymą, gaunu „Rezervacijų šalinti negalima, nes sukurtas šiomis rezervacijomis grindžiamas darbas” klaidos pranešimą.</span><span class="sxs-lookup"><span data-stu-id="2bf49-124">When I try to cancel a sales order, I receive a "Reservations cannot be removed because there is work created which relies on the reservations" error.</span></span>

<span data-ttu-id="2bf49-125">Jei darbas susietas su pardavimo užsakymu, negalite atšaukti pardavimo užsakymo, kol darbas nebus atšauktas.</span><span class="sxs-lookup"><span data-stu-id="2bf49-125">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="2bf49-126">Šis reikalavimas taikomas, net jei darbas, susietas su pardavimo užsakymu, yra uždarytas.</span><span class="sxs-lookup"><span data-stu-id="2bf49-126">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

<span data-ttu-id="2bf49-127">Norėdami ištaisyti šią problemą, vykdykite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="2bf49-127">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="2bf49-128">Atšaukite darbą ir grąžinkite atsargas į norimą vietą.</span><span class="sxs-lookup"><span data-stu-id="2bf49-128">Cancel the work, and put inventory back into the desired location.</span></span> <span data-ttu-id="2bf49-129">Eikite prie atitinkamo pardavimo užsakymo krovinio ir pasirinkite arba **Sumažinti paimtą kiekį** krovinio eilutėje, arba **Atšaukti darbą** veiksmų srityje.</span><span class="sxs-lookup"><span data-stu-id="2bf49-129">Go to the relevant load of the sales order, and select either **Reduce picked quantity** on the load line or **Reverse work** on the Action Pane.</span></span>

    <span data-ttu-id="2bf49-130">Dabar darbo būsena yra *Atšaukta*, o naujas atsargų perkėlimo darbas automatiškai sukuriamas ir apdorojamas, siekiant sugrąžinti atsargas į vietą, kuri buvo aprašyta atšaukimo metu.</span><span class="sxs-lookup"><span data-stu-id="2bf49-130">The work now has a status of *Canceled*, and new inventory movement work is automatically created and processed to put inventory back into the location that was described at the time of reversal.</span></span>

2. <span data-ttu-id="2bf49-131">Panaikinkite krovinį.</span><span class="sxs-lookup"><span data-stu-id="2bf49-131">Delete the load.</span></span> <span data-ttu-id="2bf49-132">Siunta taip pat panaikinama.</span><span class="sxs-lookup"><span data-stu-id="2bf49-132">The shipment is also deleted.</span></span>
3. <span data-ttu-id="2bf49-133">Dabar turėtumėte galėti nueiti į pardavimo užsakymą ir jį atšaukti.</span><span class="sxs-lookup"><span data-stu-id="2bf49-133">You should now be able to go to the sales order and cancel it.</span></span>

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a><span data-ttu-id="2bf49-134">Negaliu atšaukti vidinės įmonės pirkimo užsakymo, susieto su pardavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="2bf49-134">I can't cancel an intercompany purchase order that is linked to a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2bf49-135">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="2bf49-135">Issue description</span></span>

<span data-ttu-id="2bf49-136">Jei mėginsite atšaukti vidinės įmonės pirkimo užsakymą, susietą su pardavimo užsakymu, galite gauti tokį klaidos pranešimą: „Kiekio sumažinti negalima, nes pasikeis likusio atnaujinto kiekio ženklas.”</span><span class="sxs-lookup"><span data-stu-id="2bf49-136">If you try to cancel an intercompany purchase order that is linked to a sales order, you might receive the following error message: "Quantity cannot be reduced because the remaining update quantity changes sign."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2bf49-137">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="2bf49-137">Issue resolution</span></span>

<span data-ttu-id="2bf49-138">Ši problema buvo išspręsta „Microsoft Dynamics 365 Supply Chain Management” versijoje 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="2bf49-138">This issue was fixed in Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span></span> <span data-ttu-id="2bf49-139">Šioje versijoje ir vėlesnėse versijose dabar galite atšaukti vidinės įmonės pirkimo užsakymą, kuris yra susijęs su pardavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="2bf49-139">In that version and later versions, you can now cancel an intercompany purchase order that is linked to a sales order.</span></span>

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a><span data-ttu-id="2bf49-140">Ar galiu atkurti panaikintą pardavimo užsakymą, kurio SF jau išrašyta?</span><span class="sxs-lookup"><span data-stu-id="2bf49-140">Can I restore an invoiced sales order that was deleted?</span></span>

### <a name="issue-description"></a><span data-ttu-id="2bf49-141">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="2bf49-141">Issue description</span></span>

<span data-ttu-id="2bf49-142">Pardavimo užsakymas, kurio SF jau išrašyta, buvo panaikintas per klaidą ir Jūs norite jį atkurti arba peržiūrėti jo informaciją.</span><span class="sxs-lookup"><span data-stu-id="2bf49-142">An invoiced sales order was deleted by mistake, and you want to restore it or view its details.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2bf49-143">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="2bf49-143">Issue resolution</span></span>

<span data-ttu-id="2bf49-144">Jeigu panaikintam pardavimo užsakymui jau išrašyta SF, eikite į **Kliento sąskaita \> Operacijos \> Originalus dokumentas \> Rodinio informacija**.</span><span class="sxs-lookup"><span data-stu-id="2bf49-144">If the deleted sales order has already been invoiced, go to **Customer account \> Transactions \> Original document \> View details**.</span></span> <span data-ttu-id="2bf49-145">Suraskite ieškomą SF ir pasirinkite ją, kad peržiūrėtumėte išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="2bf49-145">Find the invoice that you're looking for, and select it to view its details.</span></span> <span data-ttu-id="2bf49-146">Ši informacija apima pardavimo užsakymo nuorodą.</span><span class="sxs-lookup"><span data-stu-id="2bf49-146">These details include the sales order reference.</span></span> <span data-ttu-id="2bf49-147">Taip pat turėtumėte turėti prieigą prie pardavimo užsakymo informacijos tame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="2bf49-147">You should also be able to access the sales order details from that page.</span></span>

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a><span data-ttu-id="2bf49-148">Pardavimo užsakymo antraštės galutinis terminas nerastas „SalesOrderHeaderV2Entity” duomenų objekte.</span><span class="sxs-lookup"><span data-stu-id="2bf49-148">The deadline of a sales order header can't be found in the SalesOrderHeaderV2Entity data entity.</span></span>

<span data-ttu-id="2bf49-149">*SalesOrderHeaderV2Entity* objektui galutinio termino lauko nėra.</span><span class="sxs-lookup"><span data-stu-id="2bf49-149">The deadline field doesn't exist on the *SalesOrderHeaderV2Entity* entity.</span></span>

## <a name="i-must-delete-orphaned-sales-order-records"></a><span data-ttu-id="2bf49-150">Privalau panaikinti pavienius pardavimo užsakymų įrašus.</span><span class="sxs-lookup"><span data-stu-id="2bf49-150">I must delete orphaned sales order records.</span></span>

<span data-ttu-id="2bf49-151">Norėdami išvalyti pavienius pardavimo užsakymų įrašus, vykdykite *Pardavimo užsakymo panaikinimas* periodinę užduotį, apsilankę vienoje iš šių vietų:</span><span class="sxs-lookup"><span data-stu-id="2bf49-151">To clean up orphaned sales order records, run the *Sales order deletion* periodic job by going to either of the following places:</span></span>

- <span data-ttu-id="2bf49-152">Pardavimas ir rinkodara \> Periodinės užduotys \> Valymas \> Naikinti pardavimo užsakymus</span><span class="sxs-lookup"><span data-stu-id="2bf49-152">Sales and marketing \> Periodic tasks \> Clean up \> Delete sales orders</span></span>
- <span data-ttu-id="2bf49-153">Mažmeninė prekyba ir prekyba \> IT mažmeninė prekyba ir prekyba \> Valymas \> Naikinti pardavimo užsakymus</span><span class="sxs-lookup"><span data-stu-id="2bf49-153">Retail and commerce \> Retail and commerce IT \> Clean up \> Delete sales orders</span></span>

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a><span data-ttu-id="2bf49-154">Ar yra būdas apskaičiuoti jau užregistruotų SF komisinius?</span><span class="sxs-lookup"><span data-stu-id="2bf49-154">Is there a way to calculate commissions on invoices that have already been posted?</span></span>

<span data-ttu-id="2bf49-155">„Supply Chain Management“ šiuo metu nepalaiko užregistruotų SF komisinių skaičiavimo.</span><span class="sxs-lookup"><span data-stu-id="2bf49-155">Supply Chain Management doesn't currently support the calculation of commissions for posted invoices.</span></span>

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a><span data-ttu-id="2bf49-156">Vidinės įmonės procese nepalaikomas paketo elementas.</span><span class="sxs-lookup"><span data-stu-id="2bf49-156">A bundle item isn't supported in an intercompany process.</span></span>

<span data-ttu-id="2bf49-157">Paketo elementas negalimas pirkimo užsakyme, nes, jei patikrinsite pardavimo užsakymo eilutes, skirtas paketo elementui, pastebėsite, kad kiekis yra *0* (nulis), o būsena *Atšaukta*.</span><span class="sxs-lookup"><span data-stu-id="2bf49-157">The bundle item isn't available for the purchase order because, if you examine the sales order lines for the bundle item, you will notice that the quantity is *0* (zero) and the status is *Cancelled*.</span></span> <span data-ttu-id="2bf49-158">Toks veikimo būdas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="2bf49-158">This behavior is by design.</span></span> <span data-ttu-id="2bf49-159">Pardavimo užsakymas perka tik paketo elemento komponentus.</span><span class="sxs-lookup"><span data-stu-id="2bf49-159">The sales order buys only the components of the bundle item.</span></span> <span data-ttu-id="2bf49-160">Jis neperka pačio paketo elemento.</span><span class="sxs-lookup"><span data-stu-id="2bf49-160">It doesn't buy the bundle item itself.</span></span>

<span data-ttu-id="2bf49-161">Jei turite pirkti paketą, apsvarstykite, ar turite pažymėti jį kaip paketo elementą, nes ši funkcija iš tikrųjų skirta įplaukų pripažinimo scenarijams.</span><span class="sxs-lookup"><span data-stu-id="2bf49-161">If you must buy a bundle, consider whether you have to mark it as bundle item, because this functionality is actually designed for revenue recognition scenarios.</span></span> <span data-ttu-id="2bf49-162">Daugiau informacijos apie paketo elementus žr. [Paketai](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span><span class="sxs-lookup"><span data-stu-id="2bf49-162">For more information about bundle items, see [Bundles](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span></span>
