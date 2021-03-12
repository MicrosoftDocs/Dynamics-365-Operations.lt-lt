---
title: Pardavimo sutarčių vykdymas
description: Ši procedūra nurodo, kaip įvykdyti pardavimo sutartį, su ja susiejus pardavimo užsakymus.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines, SalesAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fca2f8777f5ce3b6a96be7fcab4f011aefd9d80b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991769"
---
# <a name="fulfill-sales-agreements"></a><span data-ttu-id="407d7-103">Pardavimo sutarčių vykdymas</span><span class="sxs-lookup"><span data-stu-id="407d7-103">Fulfill sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="407d7-104">Ši procedūra nurodo, kaip įvykdyti pardavimo sutartį, su ja susiejus pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="407d7-104">This procedure shows you how to fulfill a sales agreement by associating sales orders with it.</span></span> <span data-ttu-id="407d7-105">Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="407d7-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="407d7-106">Prieš paleisdami šį vadovą, įsitikinkite, kad turite galiojančią „Produkto vertės įsipareigojimas“ tipo pardavimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="407d7-106">Before starting this guide, make sure you have an effective sales agreement of type "Product value commitment".</span></span> <span data-ttu-id="407d7-107">Taip pat galite paleisti užduočių vadovą, pavadintą „Kurti pardavimo sutartis“.</span><span class="sxs-lookup"><span data-stu-id="407d7-107">Alternatively, you can run the task guide called "Create sales agreements".</span></span>  




## <a name="release-a-sales-order-from-the-agreement"></a><span data-ttu-id="407d7-108">Išleisti pardavimo užsakymą iš sutarties</span><span class="sxs-lookup"><span data-stu-id="407d7-108">Release a sales order from the agreement</span></span>
1. <span data-ttu-id="407d7-109">Eikite į Pardavimas ir rinkodara > Pardavimo sutartys > Pardavimo sutartys.</span><span class="sxs-lookup"><span data-stu-id="407d7-109">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="407d7-110">Sąraše atidarykite sutartį, pagal kurią norite išleisti užsakymą.</span><span class="sxs-lookup"><span data-stu-id="407d7-110">In the list, open the agreement against which you want to release the order.</span></span>
3. <span data-ttu-id="407d7-111">Srityje Veiksmas spustelėkite Pardavimo sutartis.</span><span class="sxs-lookup"><span data-stu-id="407d7-111">On the Action Pane, click Sales agreement.</span></span>
4. <span data-ttu-id="407d7-112">Spustelėkite išleidimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="407d7-112">Click Release order.</span></span>
    * <span data-ttu-id="407d7-113">Kaip nurodo tekstas puslapio Kurti paleidimo viršuje, informacija, reikalinga pardavimo užsakymo eilutėse skirsis atsižvelgiant į tai, ar sutartis yra pagrįsta kiekiu ar verte.</span><span class="sxs-lookup"><span data-stu-id="407d7-113">As the text on top of the  Create release order page points out, the details required for the sales order lines will differ depending on whether the agreement is quantity- or value-based.</span></span>  
    * <span data-ttu-id="407d7-114">Šiame vadove pateikiamos sutarties tipas „Produkto vertės įsipareigojimas“.</span><span class="sxs-lookup"><span data-stu-id="407d7-114">The agreement in this guide is of type "Product value commitment".</span></span> <span data-ttu-id="407d7-115">Todėl šio puslapio skyrius Eilutės yra tuščias.</span><span class="sxs-lookup"><span data-stu-id="407d7-115">This is why the Lines section of this page is blank.</span></span> <span data-ttu-id="407d7-116">Jei įsipareigojimas pagrįstas kiekiu, eilutės informacija nukopijuojama iš sutarties.</span><span class="sxs-lookup"><span data-stu-id="407d7-116">If the commitment was based on quantity, the line information would be copied from the agreement.</span></span>  
5. <span data-ttu-id="407d7-117">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="407d7-117">Click Create.</span></span>
    * <span data-ttu-id="407d7-118">Pranešimas informuoja, kad pardavimo užsakymas sukurtas.</span><span class="sxs-lookup"><span data-stu-id="407d7-118">The message informs you that a sales order has been created.</span></span> <span data-ttu-id="407d7-119">Kadangi užsakyme eilučių nėra, turite įtraukti užsakymo eilučių informaciją, norėdami užbaigti išleidimo procesą.</span><span class="sxs-lookup"><span data-stu-id="407d7-119">Since the order does not contain any lines, you must add order line details to complete the release process.</span></span>   
6. <span data-ttu-id="407d7-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="407d7-120">Close the page.</span></span>
7. <span data-ttu-id="407d7-121">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="407d7-121">Close the page.</span></span>
8. <span data-ttu-id="407d7-122">Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="407d7-122">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
9. <span data-ttu-id="407d7-123">Sąraše raskite ir atidarykite užsakymą, kuris ankstesnėje užduotyje buvo sukurtas kaip užsakymo išleidimo rezultatas.</span><span class="sxs-lookup"><span data-stu-id="407d7-123">In the list, find and open the order that was created as the result of the order release in the previous task.</span></span>
10. <span data-ttu-id="407d7-124">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="407d7-124">Click Add line.</span></span>
11. <span data-ttu-id="407d7-125">Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="407d7-125">In the Item number field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="407d7-126">Lauke Prekės numeris, įveskite arba pasirinkite prekę, kuri nurodyta susijusioje pardavimo sutartyje.</span><span class="sxs-lookup"><span data-stu-id="407d7-126">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
13. <span data-ttu-id="407d7-127">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="407d7-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="407d7-128">Įsitikinkite, kad įvedate kiekį, su kuriuo grynoji suma bus mažesnė nei susijusios pardavimo sutarties vertė.</span><span class="sxs-lookup"><span data-stu-id="407d7-128">Make sure that you enter a quantity that brings the Net amount under the value of the associated sales agreement.</span></span>  
    * <span data-ttu-id="407d7-129">Atkreipkite dėmesį, kad dėl to, jog pardavimo užsakymas yra susietas su sutartimi, sutartas nuolaidos procentas taikomas užsakymo eilutei.</span><span class="sxs-lookup"><span data-stu-id="407d7-129">Notice that because the sales order is linked to the agreement, the negotiated discount percent is applied to the order line.</span></span>  
14. <span data-ttu-id="407d7-130">Spustelėkite eilutę „Atnaujinti“.</span><span class="sxs-lookup"><span data-stu-id="407d7-130">Click Update line.</span></span>
15. <span data-ttu-id="407d7-131">Spustelėkite „Pridėta“.</span><span class="sxs-lookup"><span data-stu-id="407d7-131">Click Attached.</span></span>
    * <span data-ttu-id="407d7-132">Puslapyje Pridėta sutartis rodomas ID ir sutarties, iš kurios eilutė išleista, sąlygos.</span><span class="sxs-lookup"><span data-stu-id="407d7-132">The Attached agreement page shows the ID and terms of the agreement from which the line is released.</span></span>  
16. <span data-ttu-id="407d7-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="407d7-133">Close the page.</span></span>
17. <span data-ttu-id="407d7-134">Veiksmų srityje spustelėkite Bendra.</span><span class="sxs-lookup"><span data-stu-id="407d7-134">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="407d7-135">Spustelėkite Pridėta pardavimo sutartis.</span><span class="sxs-lookup"><span data-stu-id="407d7-135">Click Attached sales agreement.</span></span>
19. <span data-ttu-id="407d7-136">Išplėskite skyrių Eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="407d7-136">Expand the Line details section.</span></span>
20. <span data-ttu-id="407d7-137">Spustelėkite skirtuką Įvykdymas.</span><span class="sxs-lookup"><span data-stu-id="407d7-137">Click the Fulfillment tab.</span></span>
    * <span data-ttu-id="407d7-138">Skirtuke Įvykdymas rodoma suvestinė visų pardavimo užsakymo eilučių, kurios susietos su šiuo įsipareigojimo, jų įvykdymo būsena ir suma arba kiekis, kuris dar nepaleistas.</span><span class="sxs-lookup"><span data-stu-id="407d7-138">The Fulfillment tab shows a summary of all the sales order lines that are associated with this commitment, and their fulfillment state, as well as the amount or quantity that has not yet been released.</span></span>   
21. <span data-ttu-id="407d7-139">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="407d7-139">Close the page.</span></span>
22. <span data-ttu-id="407d7-140">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="407d7-140">Close the page.</span></span>
23. <span data-ttu-id="407d7-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="407d7-141">Close the page.</span></span>

## <a name="apply-sales-agreement-in-the-order-process"></a><span data-ttu-id="407d7-142">Taikyti pardavimo sutartį užsakymo procese</span><span class="sxs-lookup"><span data-stu-id="407d7-142">Apply sales agreement in the order process</span></span>
1. <span data-ttu-id="407d7-143">Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="407d7-143">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="407d7-144">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="407d7-144">Click New.</span></span>
3. <span data-ttu-id="407d7-145">Lauke Kliento sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="407d7-145">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="407d7-146">Sąraše raskite ir pasirinkite klientą, nurodyta pardavimo sutartyje.</span><span class="sxs-lookup"><span data-stu-id="407d7-146">In the list, find and select the customer specified on the sales agreement.</span></span>
5. <span data-ttu-id="407d7-147">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="407d7-147">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="407d7-148">Išplėskite skyrių Bendra.</span><span class="sxs-lookup"><span data-stu-id="407d7-148">Expand the General section.</span></span>
7. <span data-ttu-id="407d7-149">Lauke Pardavimo sutarties ID spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="407d7-149">In the Sales agreement ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="407d7-150">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="407d7-150">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="407d7-151">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="407d7-151">Click Yes.</span></span>
10. <span data-ttu-id="407d7-152">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="407d7-152">Click OK.</span></span>
11. <span data-ttu-id="407d7-153">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="407d7-153">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="407d7-154">Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="407d7-154">In the Item number field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="407d7-155">Lauke Prekės numeris, įveskite arba pasirinkite prekę, kuri nurodyta susijusioje pardavimo sutartyje.</span><span class="sxs-lookup"><span data-stu-id="407d7-155">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
14. <span data-ttu-id="407d7-156">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="407d7-156">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="407d7-157">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="407d7-157">Click Save.</span></span>
16. <span data-ttu-id="407d7-158">Veiksmų srityje spustelėkite Paimti ir pakuoti.</span><span class="sxs-lookup"><span data-stu-id="407d7-158">On the Action Pane, click Pick and pack.</span></span>
17. <span data-ttu-id="407d7-159">Spustelėkite Registruoti važtaraštį.</span><span class="sxs-lookup"><span data-stu-id="407d7-159">Click Post packing slip.</span></span>
18. <span data-ttu-id="407d7-160">Išplėskite skyrių Parametrai.</span><span class="sxs-lookup"><span data-stu-id="407d7-160">Expand the Parameters section.</span></span>
19. <span data-ttu-id="407d7-161">Lauke Registravimas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="407d7-161">Select Yes in the Posting field.</span></span>
20. <span data-ttu-id="407d7-162">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="407d7-162">Click OK.</span></span>
21. <span data-ttu-id="407d7-163">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="407d7-163">Click OK.</span></span>
22. <span data-ttu-id="407d7-164">Veiksmų srityje spustelėkite Bendra.</span><span class="sxs-lookup"><span data-stu-id="407d7-164">On the Action Pane, click General.</span></span>
23. <span data-ttu-id="407d7-165">Spustelėkite Pridėta pardavimo sutartis.</span><span class="sxs-lookup"><span data-stu-id="407d7-165">Click Attached sales agreement.</span></span>
24. <span data-ttu-id="407d7-166">Spustelėkite skirtuką Įvykdymas.</span><span class="sxs-lookup"><span data-stu-id="407d7-166">Click the Fulfillment tab.</span></span>

