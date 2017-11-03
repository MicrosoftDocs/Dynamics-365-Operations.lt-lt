---
title: "Rekomendacijų valdiklio įtraukimas į EKA įrenginio operacijų puslapį"
description: "Šioje temoje paaiškinama, kaip rekomendacijų valdiklį įtraukti į elektroninio kasos aparato (EKA) įrenginio operacijų ekraną naudojant ekrano maketo dizaino įrankį programoje „Microsoft Dynamics 365 for Retail“."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 47ad5dc8fd698f6f543c6a48e2c7eb01d4e148e6
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a><span data-ttu-id="902bc-103">Rekomendacijų valdiklio įtraukimas į EKA įrenginio operacijų puslapį</span><span class="sxs-lookup"><span data-stu-id="902bc-103">Add a recommendations control to the transaction page on a POS device</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="902bc-104">Šioje temoje paaiškinama, kaip rekomendacijų valdiklį įtraukti į elektroninio kasos aparato (EKA) įrenginio operacijų ekraną naudojant ekrano maketo dizaino įrankį programoje „Microsoft Dynamics 365 for Retail“.</span><span class="sxs-lookup"><span data-stu-id="902bc-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="902bc-105">Naudodami „Microsoft Dynamics 365 for Retail“ galite rodyti produktų rekomendacijas savo EKA įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="902bc-105">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="902bc-106">*Rekomendacijos* –tai prekės, kurios gali sudominti jūsų klientą atsižvelgiant į jo pirkimo istoriją, prekės, kurias klientas įtraukė į savo norų sąrašą, ir prekės, kurias kiti klientai įsigijo internetu ir įprastose parduotuvėse.</span><span class="sxs-lookup"><span data-stu-id="902bc-106">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="902bc-107">Norėdami rodyti produktų rekomendacijas, turite valdiklį įtraukti į operacijų ekraną naudodami ekrano maketo dizaino įrankį.</span><span class="sxs-lookup"><span data-stu-id="902bc-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="902bc-108">Atidarykite maketo dizaino įrankį</span><span class="sxs-lookup"><span data-stu-id="902bc-108">Open Layout designer</span></span>
1.  <span data-ttu-id="902bc-109">Pasirinkite **Mažmeninė prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA** &gt; **Ekrano maketai**.</span><span class="sxs-lookup"><span data-stu-id="902bc-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="902bc-110">Naudokite spartųjį filtrą, kad rastumėte ekraną, į kurį norite įtraukti valdiklį.</span><span class="sxs-lookup"><span data-stu-id="902bc-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="902bc-111">Pvz., filtruokite lauką **Ekrano maketo ID** naudodami reikšmę „F2CP16:9M“.</span><span class="sxs-lookup"><span data-stu-id="902bc-111">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="902bc-112">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="902bc-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="902bc-113">Pvz., pasirinkite „Pavadinimas: F2CP16:9M Ekrano maketo ID: F2CP16:9M“</span><span class="sxs-lookup"><span data-stu-id="902bc-113">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="902bc-114">Spustelėkite dalį **Maketo dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="902bc-114">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="902bc-115">Vykdykite paraginimo instrukcijas, kad paleistumėte maketo dizaino įrankį.</span><span class="sxs-lookup"><span data-stu-id="902bc-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="902bc-116">Kai būsite paraginti įvesti kredencialus, įveskite tuos pačius kredencialus, kuriuos naudojote paleisdami maketo dizaino įrankį iš puslapio **Ekrano maketai**.</span><span class="sxs-lookup"><span data-stu-id="902bc-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="902bc-117">Prisijungus bus parodytas puslapis, panašus į toliau pateiktą puslapį.</span><span class="sxs-lookup"><span data-stu-id="902bc-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="902bc-118">Maketas skirsis, atsižvelgiant į jūsų parduotuvėje atliktus tinkinimus.</span><span class="sxs-lookup"><span data-stu-id="902bc-118">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="902bc-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Pasirinkite rodymo parinktį</span><span class="sxs-lookup"><span data-stu-id="902bc-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="902bc-120">Galima pasirinkti iš dviejų konfigūracijų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="902bc-120">There are two configurations options available.</span></span> <span data-ttu-id="902bc-121">Pasirinkite geriausiai jūsų parduotuvei tinkančią parinktį ir vadovaukitės likusiomis instrukcijomis, kad baigtumėte valdiklio nustatymą.</span><span class="sxs-lookup"><span data-stu-id="902bc-121">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="902bc-122">Toliau nurodytos dvi parinktys.</span><span class="sxs-lookup"><span data-stu-id="902bc-122">The two options are:</span></span>
-   <span data-ttu-id="902bc-123">Rekomendacijos rodomos visada.</span><span class="sxs-lookup"><span data-stu-id="902bc-123">Recommendations are always visible.</span></span>
-   <span data-ttu-id="902bc-124">Skirtukas **Rekomendacijos** rodomos ekrano kairiojoje pusėje esančiame tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="902bc-124">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="902bc-125">Norėdami rekomendacijas rodyti visada, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="902bc-125">To make recommendations always visible</span></span>

1.  <span data-ttu-id="902bc-126">Sumažinkite operacijų eilučių informacijos srities aukštį, kad ji būtų tokio paties aukščio kaip jos kairėje esanti kliento sritis.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="902bc-126">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="902bc-127">Iš kairiojo meniu rekomendacijų valdiklį nuvilkite tarp operacijų eilučių informacijos srities ir mygtukyno į operacijų ekrano apatinėje dalyje, centre.</span><span class="sxs-lookup"><span data-stu-id="902bc-127">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="902bc-128">Keiskite valdiklio dydį, kad jis tilptų toje erdvėje.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="902bc-128">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="902bc-129">Norėdami įrašyti ir uždaryti maketo dizaino įrankį, spustelėkite **X**.</span><span class="sxs-lookup"><span data-stu-id="902bc-129">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="902bc-130">Programoje „Dynamics 365 for Retail“ atidarykite **Mažmeninė prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikai**.</span><span class="sxs-lookup"><span data-stu-id="902bc-130">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="902bc-131">Išplečiamajame sąraše pasirinkite **1090 registrai**.</span><span class="sxs-lookup"><span data-stu-id="902bc-131">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="902bc-132">Spustelėkite **Paleisti dabar**.</span><span class="sxs-lookup"><span data-stu-id="902bc-132">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="902bc-133">Norėdami skirtuką Rekomendacijos įtraukti į ekrano kairiojoje pusėje esantį mygtukyną, atlikite tolesnius veiksmus</span><span class="sxs-lookup"><span data-stu-id="902bc-133">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="902bc-134">Dešiniuoju pelės klavišu spustelėkite tuščią erdvę po paskutiniuoju skirtuku mygtukyne, kuris yra kairiojoje puslapio pusėje.</span><span class="sxs-lookup"><span data-stu-id="902bc-134">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="902bc-135">Spustelėkite **Tinkinti**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="902bc-135">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="902bc-136">Spustelėkite **Naujas skirtukas**.</span><span class="sxs-lookup"><span data-stu-id="902bc-136">Click **New tab**.</span></span>
4.  <span data-ttu-id="902bc-137">Raskite naują skirtuką, kurį ką tik įtraukėte.</span><span class="sxs-lookup"><span data-stu-id="902bc-137">Find the new tab that you just added.</span></span> <span data-ttu-id="902bc-138">Gali reikėti slinkti žemyn.</span><span class="sxs-lookup"><span data-stu-id="902bc-138">You may need to scroll down.</span></span>
5.  <span data-ttu-id="902bc-139">Išplečiamajame sąraše **Turinys** pasirinkite **Rekomenduojami produktai**.</span><span class="sxs-lookup"><span data-stu-id="902bc-139">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="902bc-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="902bc-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="902bc-141">Lauke **Žyma** įveskite rekomendacijų skirtuko pavadinimą. Pavyzdžiui, įveskite „Rekomenduojami produktai“.</span><span class="sxs-lookup"><span data-stu-id="902bc-141">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="902bc-142">Lauke **Vaizdas** pasirinkite vaizdą, kuris bus rodomas skirtuke.</span><span class="sxs-lookup"><span data-stu-id="902bc-142">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="902bc-143">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="902bc-143">Click **OK**.</span></span> <span data-ttu-id="902bc-144">Naujasis skirtukas atsiranda mygtukyne.</span><span class="sxs-lookup"><span data-stu-id="902bc-144">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="902bc-145">Norėdami įrašyti ir uždaryti maketo dizaino įrankį, spustelėkite **X**.</span><span class="sxs-lookup"><span data-stu-id="902bc-145">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="902bc-146">Programoje „Dynamics 365 for Retail“ atidarykite **Mažmeninė prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikai**.</span><span class="sxs-lookup"><span data-stu-id="902bc-146">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="902bc-147">Išplečiamajame sąraše pasirinkite **1090 registrai**.</span><span class="sxs-lookup"><span data-stu-id="902bc-147">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="902bc-148">Spustelėkite **Paleisti dabar**.</span><span class="sxs-lookup"><span data-stu-id="902bc-148">Click **Run now**.</span></span>


<a name="see-also"></a><span data-ttu-id="902bc-149">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="902bc-149">See also</span></span>
--------

[<span data-ttu-id="902bc-150">Pritaikytų produkto rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="902bc-150">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




