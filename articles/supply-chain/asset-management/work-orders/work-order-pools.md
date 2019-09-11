---
title: Darbo užsakymų telkiniai
description: Šioje temoje aprašoma, kaip modulyje Turto valdymas dirbti su darbo užsakymų telkiniais.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875799"
---
# <a name="work-order-pools"></a><span data-ttu-id="c6f8c-103">Darbo užsakymų telkiniai</span><span class="sxs-lookup"><span data-stu-id="c6f8c-103">Work order pools</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="c6f8c-104">Naudodami darbo užsakymų telkinius, galite grupuoti kažką bendra turinčius darbo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="c6f8c-105">Pavyzdžiui, galite kurti darbo užsakymų telkinius, skirtus</span><span class="sxs-lookup"><span data-stu-id="c6f8c-105">For example, you can create work order pools for</span></span>

- <span data-ttu-id="c6f8c-106">darbo brigadoms, pavyzdžiui, A priežiūros brigadai, B priežiūros brigadai,</span><span class="sxs-lookup"><span data-stu-id="c6f8c-106">work crews, for example, Maintenance Crew A, Maintenance Crew B</span></span>  

- <span data-ttu-id="c6f8c-107">profesiniams įgūdžiams, pavyzdžiui, elektrikams ar santechnikams,</span><span class="sxs-lookup"><span data-stu-id="c6f8c-107">professional skills, for example, electricians or plumbers</span></span>  

- <span data-ttu-id="c6f8c-108">fizinėms vietoms,</span><span class="sxs-lookup"><span data-stu-id="c6f8c-108">physical locations</span></span>  

- <span data-ttu-id="c6f8c-109">laiko grafikams, pavyzdžiui, savaitėms ar kitiems laikotarpiams.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-109">time schedules, for example, weeks or other periods</span></span>  


<span data-ttu-id="c6f8c-110">Jei reikia, vieną darbo užsakymą galima įdėti į kelis darbo užsakymų telkinius.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-110">If required, one work order can be placed in many work order pools.</span></span>


## <a name="create-work-order-pool"></a><span data-ttu-id="c6f8c-111">Darbo užsakymų telkinio kūrimas</span><span class="sxs-lookup"><span data-stu-id="c6f8c-111">Create work order pool</span></span>

<span data-ttu-id="c6f8c-112">Dalyje **Visi darbo užsakymų telkiniai** arba **Aktyvūs darbo užsakymų telkiniai** galite apžvelgti savo darbo užsakymų telkinius ir kurti naujus telkinius.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-112">In **All work order pools** or **Active work order pools**, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="c6f8c-113">Spustelėkite **Turto valdymas** > **Bendra** > **Darbo užsakymų telkiniai** > **Visi darbo užsakymų telkiniai** arba **Aktyvūs darbo užsakymų telkiniai**.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-113">Click **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="c6f8c-114">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-114">Click **New**.</span></span>

3. <span data-ttu-id="c6f8c-115">Lauke **Telkinys** įterpkite darbo užsakymų telkinio ID, o lauke **Pavadinimas** – pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-115">Insert a work order pool ID in the **Pool** field and a name in the **Name** field.</span></span>

4. <span data-ttu-id="c6f8c-116">Perjungimo mygtuke **Aktyvus** pasirinkite Taip, jei norite nurodyti, kad darbo užsakymų telkinys yra aktyvus.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-116">Select "Yes" on the **Active** toggle button to indicate that the work order pool is active.</span></span>

5. <span data-ttu-id="c6f8c-117">Perjungimo mygtuke **Panaikinti darbo užsakymų ryšius** pasirinkite Taip, jei norite, kad darbo užsakymai būtų automatiškai pašalinami iš darbo užsakymų telkinio.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-117">Select "Yes" on the **Delete work order relations** toggle button if you want work orders to be automatically removed from the work order pool.</span></span>

6. <span data-ttu-id="c6f8c-118">Lauke **Naikinti ciklo būseną** pasirinkite darbo užsakymo ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-118">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="c6f8c-119">Pavyzdžiui, darbo užsakymo įvykdymo ciklo būseną galima nustatyti taip, kad būtų automatiškai panaikinami ryšiai su darbo užsakymų telkiniais.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-119">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

7. <span data-ttu-id="c6f8c-120">Į darbo užsakymų telkinį darbo užsakymus galite pradėti įtraukti iš karto.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-120">You can start adding work orders to your work order pool right away.</span></span> <span data-ttu-id="c6f8c-121">„FastTab“ konteineryje **Darbo užsakymai** spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-121">On the **Work orders** FastTab, click **Add line**.</span></span>

8. <span data-ttu-id="c6f8c-122">Lauke **Darbo užsakymas** pasirinkite darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-122">Select a work order in the **Work order** field.</span></span> <span data-ttu-id="c6f8c-123">Susiję laukai automatiškai atnaujinami.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-123">The related fields are automatically updated.</span></span>

9. <span data-ttu-id="c6f8c-124">Jei norite įtraukti daugiau darbo užsakymų, pakartokite 7–8 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-124">Repeat steps 7-8 if you want to add more work orders.</span></span>

10. <span data-ttu-id="c6f8c-125">Lauke **Rikiavimo tvarka** galite nurodyti, ar darbo užsakymus reikia vykdyti tam tikra tvarka.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-125">In the **Sort order** field, you can indicate if the work orders should be carried out in a certain order.</span></span> <span data-ttu-id="c6f8c-126">Įterpdami skaičius 1, 2, 3 ir t. t., galite nurodyti konkrečią pasirinktų darbo užsakymų seką.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-126">Insert numbers 1, 2, 3, and so on to indicate a specific sequence for the selected work orders.</span></span>

11. <span data-ttu-id="c6f8c-127">Spustelėję mygtuką **Darbo užsakymai**, matysite visų į darbo užsakymų telkinį įtrauktų darbo užsakymų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-127">Click the **Work orders** button to see a list of all the work orders included in the work order pool.</span></span>

12. <span data-ttu-id="c6f8c-128">Spustelėję mygtuką **Pajėgumas**, atidarysite sritį **Pajėgumas** ir galėsite skaičiuoti bei peržiūrėti priežiūros grafiko, nesuplanuotų darbo užsakymų ir suplanuotų darbo užsakymų pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-128">Click the **Capacity load** button to open **Capacity load** to calculate and view capacity load for maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

13. <span data-ttu-id="c6f8c-129">Spustelėję mygtuką **Prekių prognozė**, atidarysite sritį **Prekių prognozė** ir galėsite skaičiuoti bei peržiūrėti prekių (atsarginių dalių ir kitų reikiamų prekių), susijusių su priežiūros grafiku, nesuplanuotais darbo užsakymais ir suplanuotais darbo užsakymais, prognozes.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-129">Click the **Item forecast** button to open **Item forecast** to calculate and view forecasts for items (spare parts and other required items) related to maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

14. <span data-ttu-id="c6f8c-130">Spustelėję mygtuką **Darbo užsakymo pirkimo paraiška**, atidarysite sąrašą **Darbo užsakymo pirkimo paraiška** ir matysite pirkimo paraiškų, susijusių su darbo užsakymų telkinyje esančiais darbo užsakymais, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-130">Click the **Work order purchase requisition** button to open the **Work order purchase requisition** list to see a list of purchase requisitions related to the work orders in the work order pool.</span></span>

15. <span data-ttu-id="c6f8c-131">Spustelėję mygtuką **Darbo užsakymų pirkimas**, atidarysite sąrašą **Darbo užsakymų pirkimas** ir matysite pirkimo užsakymų, susijusių su darbo užsakymų telkinyje esančiais darbo užsakymais, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-131">Click the **Work order purchase** button to open the **Work order purchase** list to see a list of purchase orders related to the work orders in the work order pool.</span></span>

>[!NOTE]
><span data-ttu-id="c6f8c-132">Kai tam tikras darbo užsakymų telkinys planuojant darbą nebėra aktualus, sąrašo rodinyje **Darbo užsakymų telkinys** esantį to telkinio žymės langelį **Aktyvus** nustatykite kaip Ne.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-132">When a work order pool is no longer relevant for your work planning, set the **Active** check box for that pool to "No" in the **Work order pool** list view.</span></span>

<span data-ttu-id="c6f8c-133">Jei norite panaikinti visas darbo užsakymų eilutes, pavyzdžiui, norėdami sukurti tuščią telkinį, kurį vėliau galėtumėte naudoti su kitais darbo užsakymais, pažymėkite žymės langelį **Panaikinti darbo užsakymų ryšius**.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-133">Select the **Delete work order relations** check box if you want to delete all work order lines, for example to create an empty pool that you can later use for other work orders.</span></span> <span data-ttu-id="c6f8c-134">Jei, naudodami darbo užsakymų telkinį, vėliau norite kurti naujus darbo užsakymų ryšius, nepamirškite žymės langelio **Panaikinti darbo užsakymų ryšius** išvalyti.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-134">Remember to clear the **Delete work order relations** check box if you want to use the work order pool to create new work order relations later.</span></span>


![1 pav.](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a><span data-ttu-id="c6f8c-136">Darbo užsakymo įtraukimas į darbo užsakymų telkinį</span><span class="sxs-lookup"><span data-stu-id="c6f8c-136">Add work order to a work order pool</span></span>

<span data-ttu-id="c6f8c-137">Kaip aprašyta pirmesniame skyriuje, kurdami darbo užsakymų telkinį, į jį galite įtraukti darbo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-137">As described in the section above, you can add work orders to a work order pool when you create the pool.</span></span> <span data-ttu-id="c6f8c-138">Į darbo užsakymų telkinį darbo užsakymą taip pat galite įtraukti iš sąrašo **Visi darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-138">You can also add a work order to a work order pool from one of the **All work orders** list.</span></span>

1. <span data-ttu-id="c6f8c-139">Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-139">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="c6f8c-140">Sąraše pasirinkite darbo užsakymą ir spustelėkite **Darbo užsakymų telkinys**.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-140">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="c6f8c-141">Lauke **Įtraukti / šalinti** pasirinkite Įtraukti.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-141">Select "Add" in the **Add/remove** field.</span></span>

4. <span data-ttu-id="c6f8c-142">Lauke **Telkinys** pasirinkite darbo užsakymų telkinį.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-142">Select the work order pool in the **Pool** field.</span></span>

5. <span data-ttu-id="c6f8c-143">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-143">Click **OK**.</span></span>

6. <span data-ttu-id="c6f8c-144">Jei, į darbo užsakymų telkinį įtraukę darbo užsakymą, jį norite padėti į konkrečią telkinio seką: atidarykite vieną darbo užsakymų telkinių sąrašo puslapių, pasirinkite telkinį ir spustelėkite **Redaguoti** bei formos **Darbo užsakymų telkinys** „FastTab“ konteinerio **Darbo užsakymai** lauke **Rikiavimo tvarka** koreguokite į telkinį įtrauktų darbo užsakymų rikiavimo tvarką.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-144">After you have added a work order to a work order pool, if you want to place the work order in a specific sequence in the pool: Open one of the work order pools list pages, select the pool and click **Edit**, and adjust the sort order of the work orders included in pool in the **Work order pool** form > **Work orders** FastTab > **Sort order** field.</span></span>

<span data-ttu-id="c6f8c-145">Jei pasirinktą darbo užsakymą norite pašalinti iš darbo užsakymų telkinio, atlikdami 3 veiksmą pasirinkite Šalinti.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-145">If you want to remove the selected work order from a work order pool, select "Remove" in step 3.</span></span>

