---
title: Darbo užsakymų telkiniai
description: Šioje temoje aprašoma, kaip modulyje Turto valdymas dirbti su darbo užsakymų telkiniais.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTablePoolPart, EntAssetWorkOrderPoolReferenceInfoPart, EntAssetWorkOrderPool, EntAssetWorkOrderPoolPreviewPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3e95a4fdfaf4817867f3d2df7774df6a27ee6599
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889510"
---
# <a name="work-order-pools"></a><span data-ttu-id="1ee3d-103">Darbo užsakymų telkiniai</span><span class="sxs-lookup"><span data-stu-id="1ee3d-103">Work order pools</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="1ee3d-104">Naudodami darbo užsakymų telkinius, galite grupuoti kažką bendra turinčius darbo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="1ee3d-105">Toliau pateikti keli objektų, kuriems galite sukurti darbo užsakymų telkinius, pavyzdžiai:</span><span class="sxs-lookup"><span data-stu-id="1ee3d-105">Here are some examples of things that you can create  work order pools for:</span></span>

- <span data-ttu-id="1ee3d-106">Darbo brigados, pavyzdžiui, A priežiūros brigada, B priežiūros brigada</span><span class="sxs-lookup"><span data-stu-id="1ee3d-106">Work crews, for example, Maintenance Crew A or Maintenance Crew B</span></span>  

- <span data-ttu-id="1ee3d-107">Profesiniai įgūdžiai, pavyzdžiui, elektrikai ar santechnikai</span><span class="sxs-lookup"><span data-stu-id="1ee3d-107">Professional skills, such as electricians or plumbers</span></span>  

- <span data-ttu-id="1ee3d-108">Fizinės vietos</span><span class="sxs-lookup"><span data-stu-id="1ee3d-108">Physical locations</span></span>  

- <span data-ttu-id="1ee3d-109">Grafikai, pavyzdžiui, savaičių ar kitų laikotarpių</span><span class="sxs-lookup"><span data-stu-id="1ee3d-109">Time schedules, such as weeks or other periods</span></span>  

<span data-ttu-id="1ee3d-110">Kai reikia, vieną darbo užsakymą galite naudoti keliuose darbo užsakymų telkiniuose.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-110">As you require, you can put one work order in multiple work order pools.</span></span>


## <a name="create-a-work-order-pool"></a><span data-ttu-id="1ee3d-111">Darbo užsakymų telkinio kūrimas</span><span class="sxs-lookup"><span data-stu-id="1ee3d-111">Create a work order pool</span></span>

<span data-ttu-id="1ee3d-112">Sąrašo puslapyje **Visi darbo užsakymų telkiniai** arba **Aktyvūs darbo užsakymų telkiniai** galite apžvelgti savo darbo užsakymų telkinius ir kurti naujus telkinius.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-112">On the **All work order pools** or **Active work order pools** list page, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="1ee3d-113">Pasirinkite **Turto valdymas** > **Bendra** > **Darbo užsakymų telkiniai** > **Visi darbo užsakymų telkiniai** arba **Aktyvūs darbo užsakymų telkiniai**.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-113">Select **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="1ee3d-114">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-114">Select **New**.</span></span>

3. <span data-ttu-id="1ee3d-115">Lauke **Telkinys** įveskite darbo užsakymų telkinio ID.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-115">In the **Pool** field, enter an ID for the work order pool.</span></span>

4. <span data-ttu-id="1ee3d-116">Lauke **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-116">the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="1ee3d-117">Nustatykite parinkties **Aktyvus** reikšmę **Taip**, jei norite nurodyti, kad darbo užsakymų telkinys yra aktyvus.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-117">Set the **Active** option to **Yes** to indicate that the work order pool is active.</span></span>

6. <span data-ttu-id="1ee3d-118">Nustatykite parinkties **Panaikinti darbo užsakymų ryšius** reikšmę **Taip**, jei darbo užsakymai turi būti automatiškai pašalinami iš darbo užsakymų telkinio.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-118">Set the **Delete work order relations** option to **Yes** if work orders should automatically be removed from the work order pool.</span></span>

7. <span data-ttu-id="1ee3d-119">Lauke **Naikinti ciklo būseną** pasirinkite darbo užsakymo ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-119">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="1ee3d-120">Pavyzdžiui, darbo užsakymo įvykdymo ciklo būseną galima nustatyti taip, kad būtų automatiškai panaikinami ryšiai su darbo užsakymų telkiniais.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-120">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

    <span data-ttu-id="1ee3d-121">Į darbo užsakymų telkinį darbo užsakymus galite pradėti įtraukti iš karto.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-121">You can start adding work orders to your work order pool right away.</span></span>

8. <span data-ttu-id="1ee3d-122">„FastTab“ **Darbo užsakymai** pasirinkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-122">On the **Work orders** FastTab, select **Add line**.</span></span>

9. <span data-ttu-id="1ee3d-123">Lauke **Darbo užsakymas** pasirinkite darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-123">In the **Work order** field, select a work order.</span></span> <span data-ttu-id="1ee3d-124">Susiję laukai automatiškai atnaujinami.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-124">The related fields are automatically updated.</span></span>

10. <span data-ttu-id="1ee3d-125">Norėdami pridėti daugiau darbo užsakymų, pakartokite 8–9 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-125">Repeat steps 8 through 9 to add more work orders.</span></span>

11. <span data-ttu-id="1ee3d-126">Jei įtraukti darbo užsakymai turi būti atlikti tam tikrame užsakyme, lauke **Rūšiavimo tvarka** galite įvesti skaičius **1**, **2**, **3** ir t. t., kad nurodytumėte užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-126">If the work orders that you added should be done in a specific order, in the **Sort order** field, you can enter the numbers **1**, **2**, **3**, and so on, to specify that order.</span></span>

12. <span data-ttu-id="1ee3d-127">Norėdami peržiūrėti visų darbo užsakymų, įtrauktų į darbo užsakymų telkinį, sąrašą, veiksmų srityje, esančioje skirtuke **Darbo užsakymų telkinys**, grupėje **Peržiūrėti susijusių darbo užsakymų telkinį**, pasirinkite **Darbo užsakymai**, kad atidarytumėte sąrašo puslapį **Visi darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-127">To view a list of all the work orders that are included in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Work orders** to open the **All work orders** list page.</span></span>

13. <span data-ttu-id="1ee3d-128">Norėdami apskaičiuoti ir peržiūrėti priežiūros grafiko, nesuplanuotų darbo užsakymų ir suplanuotų darbo užsakymų pajėgumą, veiksmų srityje, esančioje skirtuke **Darbo užsakymų telkinys**, grupėje **Peržiūrėti susijusių darbo užsakymų telkinį**, pasirinkite **Pajėgumas**, kad atidarytumėte dialogo langą **Pajėgumo skaičiavimas**.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-128">To calculate and view capacity load for the maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Capacity load** to open the **Calculate capacity load** dialog.</span></span>

14. <span data-ttu-id="1ee3d-129">Norėdami apskaičiuoti ir peržiūrėti su priežiūros grafiku, nesuplanuotais darbo užsakymais ir suplanuotais darbo užsakymais susijusių elementų (atsarginių dalių ir kitų reikalingų elementų) prognozes, veiksmų srityje, esančioje skirtuke **Darbo užsakymų telkinys**, grupėje **Peržiūrėti susijusių darbo užsakymų telkinį**, pasirinkite **Elemento prognozė**, kad atidarytumėte dialogo langą **Apskaičiuoti elemento prognozę**.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-129">To calculate and view forecasts for items (spare parts and other required items) that are related to maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Item forecast** to open the **Calculate item forecast** dialog.</span></span>

15. <span data-ttu-id="1ee3d-130">Norėdami peržiūrėti pirkimo paraiškų, susijusių su darbo užsakymais, esančiais darbo užsakymų telkinyje, sąrašą, veiksmų srityje, esančioje skirtuke **Darbo užsakymų telkinys**, grupėje **Įsigijimas**, pasirinkite **Darbo užsakymo pirkimo paraiška**, kad atidarytumėte sąrašo puslapį **Darbo užsakymo pirkimo paraiška**.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-130">To view a list of purchase requisitions that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase requisition** to open the **Work order purchase requisition** list page.</span></span>

16. <span data-ttu-id="1ee3d-131">Norėdami peržiūrėti pirkimo užsakymų, susijusių su darbo užsakymais, esančiais darbo užsakymų telkinyje, sąrašą, veiksmų srityje, esančioje skirtuke **Darbo užsakymų telkinys**, grupėje **Įsigijimas**, pasirinkite **Darbo užsakymo pirkimas**, kad atidarytumėte sąrašo puslapį **Darbo užsakymo pirkimas**.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-131">To view a list of purchase orders that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase** to open the **Work order purchase** list page.</span></span>

>[!NOTE]
><span data-ttu-id="1ee3d-132">Kai tam tikras darbo užsakymų telkinys planuojant darbą nebėra aktualus, nustatykite telkinio parinkties **Aktyvus** reikšmę **Ne**, pasiekiamą puslapio **Darbo užsakymų telkinys** sąrašo rodinyje.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-132">When a work order pool is no longer relevant to your work planning, set the **Active** option for that pool to **No** in the list view of the **Work order pool** page.</span></span>

<span data-ttu-id="1ee3d-133">Norėdami pašalinti visas darbuotojo užsakymo eilutes, nustatykite parinkties **Panaikinti darbo užsakymų ryšius** reikšmę **Taip**.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-133">To delete all worker order lines, set the **Delete work order relations** option to **Yes**.</span></span> <span data-ttu-id="1ee3d-134">Ši parinktis naudinga, jei, pavyzdžiui, norite sukurti tuščią telkinį, kurį vėliau galėsite naudoti kitiems darbo užsakymams.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-134">This option is useful if, for example, you want to create an empty pool that you can use later for other work orders.</span></span> <span data-ttu-id="1ee3d-135">Kai esate pasiruošę naudodami darbo užsakymų telkinį vėliau kurti naujus darbo užsakymų ryšius, nepamirškite nustatyti parinkties **Panaikinti darbo užsakymų ryšius** reikšmės **Ne**.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-135">When you're ready to use the work order pool to create new work order relations later, remember to set the **Delete work order relations** option to **No**.</span></span>

<span data-ttu-id="1ee3d-136">Toliau pateiktame paveikslėlyje parodytas sąrašo puslapio **Darbo užsakymų telkinys** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-136">The illustration below shows an example of the **Work order pool** list page.</span></span>

![1 pav.](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a><span data-ttu-id="1ee3d-138">Darbo užsakymo įtraukimas į darbo užsakymų telkinį</span><span class="sxs-lookup"><span data-stu-id="1ee3d-138">Add a work order to a work order pool</span></span>

<span data-ttu-id="1ee3d-139">Kaip aprašyta ankstesniame skyriuje, kurdami darbo užsakymų telkinį, į jį galite įtraukti darbo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-139">As described in the previous section, you can add work orders to a work order pool when you create that pool.</span></span> <span data-ttu-id="1ee3d-140">Darbo užsakymus į darbo užsakymų kaupinį taip pat galite įtraukti sąrašo puslapyje **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-140">You can also add work orders to a work order pool on the **All work orders** or **Active work orders** list page.</span></span>

1. <span data-ttu-id="1ee3d-141">Pasirinkite darbo užsakymą, o tada veiksmų srityje, skirtuke **Darbo užsakymas**, grupėje **Tvarkyti**, pasirinkite **Darbo užsakymų telkinys**.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-141">Select the work order, and then, on the Action Pane, on the **Work order** tab, in the **Maintain** group, select **Work order pool**.</span></span>

2. <span data-ttu-id="1ee3d-142">Sąraše pasirinkite darbo užsakymą ir spustelėkite **Darbo užsakymų telkinys**.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-142">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="1ee3d-143">Dialogo lango **Tvarkyti darbo užsakymų telkinį** lauke **Įtraukti / šalinti** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-143">In the **Maintain work order pool** dialog, in the **Add/remove** field, select **Add**.</span></span>

4. <span data-ttu-id="1ee3d-144">Lauke **Telkinys** pasirinkite darbo užsakymų telkinį.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-144">In the **Pool** field, select the work order pool.</span></span>

5. <span data-ttu-id="1ee3d-145">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-145">Select **OK**.</span></span>

6. <span data-ttu-id="1ee3d-146">Norėdami pridėti darbo užsakymą, kurį įtraukėte konkrečiame užsakyme, pire darbo užsakymų telkinio, sąrašo puslapyje **Visi darbo užsakymų telkiniai** arba **Aktyvūs darbo užsakymų telkiniai** pasirinkite telkinį ir pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-146">To put the work order that you added in a specific order in the work order pool, on the **All work order pools** or **Active work order pools** list page, select the pool, and then select **Edit**.</span></span> <span data-ttu-id="1ee3d-147">Tada puslapyje **Darbo užsakymų telkinys**, „FastTab“ **Darbo užsakymai**, naudokite lauką **Rūšiavimo tvarka**, kad nustatytumėte į telkinį įtrauktų darbo užsakymų rūšiavimo tvarką.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-147">Then, on the **Work order pool** page, on the **Work orders** FastTab, use the **Sort order** field to adjust the sort order of the work orders that are included in pool.</span></span>

<span data-ttu-id="1ee3d-148">Norėdami pašalinti pasirinktą darbo užsakymą iš darbo užsakymų telkinio, pakartokite šiuos veiksmus, tačiau atlikdami 3 veiksmą pasirinkite **Šalinti**.</span><span class="sxs-lookup"><span data-stu-id="1ee3d-148">To remove a work order from a work order pool, repeat these steps, but select **Remove** in step 3.</span></span>

