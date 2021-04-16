---
title: Grąžintų prekių gavimo registravimas
description: Galite užregistruoti grąžintų prekių gavimą naudodami gavimų apžvalgos formą arba registracijos formą.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 96532173c003621271f768dcdc64d67b6948ab6c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836043"
---
# <a name="register-the-receipt-of-returned-items"></a><span data-ttu-id="c676e-103">Grąžintų prekių gavimo registravimas</span><span class="sxs-lookup"><span data-stu-id="c676e-103">Register the receipt of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c676e-104">Grąžintų prekių gavimą galima registruoti dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="c676e-104">There are two methods for registering the receipt of returned items.</span></span> <span data-ttu-id="c676e-105">Pirmasis būdas yra sandėlio gavimo procesas, kuris naudoja formą **Gavimų apžvalga**.</span><span class="sxs-lookup"><span data-stu-id="c676e-105">The first method is a warehouse receiving process that uses the **Arrival overview** form.</span></span> <span data-ttu-id="c676e-106">Antrasis naudoja formą **Registracija**.</span><span class="sxs-lookup"><span data-stu-id="c676e-106">The second uses the **Registration** form.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a><span data-ttu-id="c676e-107">Grąžintų prekių gavimo registravimas naudojant formą Gavimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="c676e-107">Register the receipt of returned items in the Arrival overview form</span></span>

<span data-ttu-id="c676e-108">Galite naudoti formą **Gavimų apžvalga**, jei norite identifikuoti grąžinimo siuntą pagal jos grąžinamų medžiagų autorizavimo (RMA) numerį.</span><span class="sxs-lookup"><span data-stu-id="c676e-108">You can use the **Arrival overview** form to identify a return shipment by its Return Material Authorization (RMA) number.</span></span> <span data-ttu-id="c676e-109">Jei žurnalo pavadinimas nurodytas skirtuke **Nustatymas** ir yra žurnalo eilutės, kurios atitinka eilutes, pažymėtas formoje **Gavimų apžvalga**, nauja žurnalo antraštė yra sukuriama spustelėjus **Pradėti gavimo žurnalą**.</span><span class="sxs-lookup"><span data-stu-id="c676e-109">If a journal name is defined on the **Setup** tab, and journal lines that correspond to the lines selected on the **Arrival overview** form exist, a new journal header is created when you click **Start arrival**.</span></span>

1.  <span data-ttu-id="c676e-110">Spustelėkite **Atsargų valdymas** \> **Laikotarpio** \> **Gavimų apžvalga**.</span><span class="sxs-lookup"><span data-stu-id="c676e-110">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="c676e-111">Lauke **Nustatymo pavadinimas** pasirinkite **Grąžinimo užsakymas**, tada spustelėkite **Naujinti**.</span><span class="sxs-lookup"><span data-stu-id="c676e-111">In the **Setup name** field, select **Return order**, and then click **Update**.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="c676e-112">Galite naudoti laukus <STRONG>Diapazonas</STRONG> norėdami susiaurinti paieškos rezultatus.</span><span class="sxs-lookup"><span data-stu-id="c676e-112">You can use the <STRONG>Range</STRONG> fields to narrow the search results.</span></span> <span data-ttu-id="c676e-113">Galite įrašyti ar pasirinkti RMA numerį lauke <STRONG>RMA numeris</STRONG>, jei norite tikslaus rezultato.</span><span class="sxs-lookup"><span data-stu-id="c676e-113">You can type or select the RMA number in the <STRONG>RMA number</STRONG> field for an exact result.</span></span> <span data-ttu-id="c676e-114">Norėdami apibrėžti ir įrašyti rinkinį filtrų, kurie nustatys, kurie įeinantys gavimai bus rodomi, spustelėkite skirtuką <STRONG>Nustatymas</STRONG>. Galimi filtrai yra tipai, sandėliai ir rampos.</span><span class="sxs-lookup"><span data-stu-id="c676e-114">To define and save a set of filters that will restrict which incoming arrivals are displayed, click the <STRONG>Setup</STRONG> tab. The available filters include types, warehouses, and docks.</span></span></P>

    

    > [!WARNING]
    > <P><span data-ttu-id="c676e-115">Grąžinimo užsakymų negalima maišyti su kitais gavimų tipais formoje <STRONG>Gavimų apžvalga</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="c676e-115">Return orders cannot be mixed with other arrival types in the <STRONG>Arrival overview</STRONG> form.</span></span> <span data-ttu-id="c676e-116">Todėl, nuoroda visada bus pardavimo užsakymas, bet pardavimo užsakymo ID nebus nurodyti žurnalo antraštėje.</span><span class="sxs-lookup"><span data-stu-id="c676e-116">Therefore, the reference will always be sales order, but no sales order ID will be specified on the journal header.</span></span></P>



3.  <span data-ttu-id="c676e-117">Tinklelyje **Gavimai** raskite eilutę, atitinkančią grąžinamą prekę ir tada pasirinkite žymės langelį, esantį stulpelyje **Pasirinkti įtraukti į gavimą**.</span><span class="sxs-lookup"><span data-stu-id="c676e-117">In the **Receipts** grid, locate the line that matches the item being returned, and then select the check box in the **Select for arrival** column.</span></span>

4.  <span data-ttu-id="c676e-118">Jei norite pašalinti tam tikras eilutes iš grąžinimo gavimo, pavyzdžiui, prekes iš pradinio užsakymo, kurios nebuvo įtrauktos į grąžinimo siuntą, išvalykite susijusius žymės langelius **Pasirinkti įtraukti į gavimą** lentelėje **Eilutės**, esančioje apatinėje formos dalyje.</span><span class="sxs-lookup"><span data-stu-id="c676e-118">To exclude certain lines from the return receipt, such as items from the original order that were not included in the return shipment, clear the associated **Select for arrival** check boxes in the **Lines** table in the lower part of the form.</span></span>

5.  <span data-ttu-id="c676e-119">Spustelėkite mygtuką **Pradėti gavimo žurnalą** norėdami sukurti gavimo žurnalą.</span><span class="sxs-lookup"><span data-stu-id="c676e-119">Click the **Start arrival** button to create an arrival journal.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="c676e-120">Galite pasirinkti kelis grąžinimo užsakymus ir juos visus įtraukti į vieną gavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="c676e-120">You can select multiple return orders and include them all in a single arrival process.</span></span> <span data-ttu-id="c676e-121">Kiekviena grąžinimo užsakymo eilutė bus nukopijuotą į atitinkamą prekių gavimo žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="c676e-121">Each return order line will be copied into a corresponding item arrival journal line.</span></span></P>

    

    > [!NOTE]
    > <P><span data-ttu-id="c676e-122">Taip pat galite rankiniu būdu sukurti gavimo žurnalą naudodami formą <STRONG>Prekių gavimo žurnalas</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="c676e-122">You can also manually create an arrival journal by using the <STRONG>Item arrival</STRONG> form.</span></span> 



6.  <span data-ttu-id="c676e-123">Spustelėkite **Atsargų valdymas** \> **Žurnalai** \> **Prekių gavimas** \> **Prekių gavimas**.</span><span class="sxs-lookup"><span data-stu-id="c676e-123">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>

7.  <span data-ttu-id="c676e-124">Pasirinkite gavimo žurnalą, kurį ką tik sukūrėte, ir tada spustelėkite **Eilutės**, kad atidarytumėte formą **Žurnalo eilutės, vietos**.</span><span class="sxs-lookup"><span data-stu-id="c676e-124">Select the arrival journal that you just created and then click **Lines** to open the **Journal lines, locations** form.</span></span>

8.  <span data-ttu-id="c676e-125">Skirtuke **Bendra** pakoreguokite skaičių lauke **Kiekis** (jei reikia), tada priskirkite perdavimo kodą lauke **Perdavimo kodas**.</span><span class="sxs-lookup"><span data-stu-id="c676e-125">On the **General** tab, adjust the number in the **Quantity** field, if it is required, and then assign a disposition code in the **Disposition code** field.</span></span>
    
    <span data-ttu-id="c676e-126">Taip pat galite pasirinkti ir žymės langelį **Sulaikymo valdymas**, kad grąžinamos prekės būtų siunčiamos naudojant tikrinimo procesą pagal sulaikymo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="c676e-126">Alternatively, you can select the **Quarantine management** check box to have the returned items sent through an inspection process in the context of a quarantine order.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="c676e-127">Jei siunčiate grąžinamas prekes per karantiną, jūs negalite nurodyti perdavimo kodo.</span><span class="sxs-lookup"><span data-stu-id="c676e-127">If you send the returned items through quarantine, you cannot specify a disposition code.</span></span></P>



9.  <span data-ttu-id="c676e-128">Spustelėkite mygtuką **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="c676e-128">Click the **Validate** button.</span></span>

10. <span data-ttu-id="c676e-129">Jei nėra klaidų tikrinimo procese, spustelėkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="c676e-129">If there are no errors in the validation process, click **Post**.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a><span data-ttu-id="c676e-130">Grąžintų prekių gavimo registravimas naudojant formą Registracija</span><span class="sxs-lookup"><span data-stu-id="c676e-130">Register the receipt of returned items in the Registration form</span></span>

<span data-ttu-id="c676e-131">Vietoje formos **Gavimų apžvalga**, galite naudoti formą **Registracija**, kad užregistruotumėte grąžinamų prekių gavimą.</span><span class="sxs-lookup"><span data-stu-id="c676e-131">As an alternative to using the **Arrival overview** form, you can use the **Registration** form to register the arrival of returned items.</span></span>

1.  <span data-ttu-id="c676e-132">Spustelėkite **Pardavimas ir rinkodara** \> **Bendra** \> **Grąžinimo užsakymai** \> **Visi grąžinimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="c676e-132">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span> <span data-ttu-id="c676e-133">Sukurkite naują grąžinimo užsakymą arba atidarykite grąžinimo užsakymą iš sąrašo.</span><span class="sxs-lookup"><span data-stu-id="c676e-133">Create a new return order or open the return order from the list.</span></span> <span data-ttu-id="c676e-134">„FastTab“ skirtuke **Eilutės** pasirinkite grąžinimo užsakymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="c676e-134">On the **Lines** FastTab, select the return order line.</span></span> <span data-ttu-id="c676e-135">Spustelėkite **Naujinti eilutę**, tada spustelėkite **Registracija**.</span><span class="sxs-lookup"><span data-stu-id="c676e-135">Click **Update line**, and then click **Registration**.</span></span>

2.  <span data-ttu-id="c676e-136">Priskirkite perdavimo kodą lauke **Perdavimo kodas**, tada spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c676e-136">Assign a disposition code in the **Disposition code** field, and then click **OK**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="c676e-137">Neįmanoma išsiųsti prekės patikrinti kaip sulaikymo užsakymo, naudojant formą <STRONG>Registracija</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="c676e-137">It is not possible to send the item for inspection as a quarantine order using the <STRONG>Registration</STRONG> form.</span></span></P>



3.  <span data-ttu-id="c676e-138">Tinklelyje **Operacijos** pasirinkite operaciją, kuri turi būti registruojama.</span><span class="sxs-lookup"><span data-stu-id="c676e-138">In the **Transactions** grid, select the transaction to be registered.</span></span>

4.  <span data-ttu-id="c676e-139">Tinklelyje **Registruoti dabar** spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="c676e-139">In the **Register now** grid, click **Add**.</span></span> <span data-ttu-id="c676e-140">Kartokite du ankstesnius veiksmus, kol visos grąžinamos prekės bus rodomos tinklelyje **Registruoti dabar**.</span><span class="sxs-lookup"><span data-stu-id="c676e-140">Repeat the previous two steps until all of the returned items appear in the **Register now** grid.</span></span>

5.  <span data-ttu-id="c676e-141">Spustelėkite **Registruoti viską**.</span><span class="sxs-lookup"><span data-stu-id="c676e-141">Click **Post all**.</span></span>

## <a name="see-also"></a><span data-ttu-id="c676e-142">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="c676e-142">See also</span></span>

<span data-ttu-id="c676e-143">[Gavimų peržiūra (forma)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="c676e-143">[Arrival overview (form)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]