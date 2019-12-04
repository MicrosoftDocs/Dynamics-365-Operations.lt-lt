---
title: Rekomendacijų valdiklio įtraukimas į EKA įrenginių operacijų ekraną
description: Šioje temoje paaiškinama, kaip rekomendacijų valdiklį įtraukti į elektroninio kasos aparato (EKA) įrenginio operacijų ekraną naudojant ekrano maketo dizaino įrankį programoje „Microsoft Dynamics 365 for Retail“.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e6f0b75c8d81a5ac6ec90020375aec39120d4406
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811221"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="3f3b2-103">Rekomendacijų valdiklio įtraukimas į EKA įrenginių operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="3f3b2-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="3f3b2-104">Šioje temoje paaiškinama, kaip rekomendacijų valdiklį įtraukti į elektroninio kasos aparato (EKA) įrenginio operacijų ekraną naudojant ekrano maketo dizaino įrankį programoje „Microsoft Dynamics 365 Retail“.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Retail.</span></span> <span data-ttu-id="3f3b2-105">Norėdami gauti daugiau informacijos apie produktų rekomendacijas, perskaitykite [EKA dokumentacijos produktų rekomendacijas.](product.md).</span><span class="sxs-lookup"><span data-stu-id="3f3b2-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="3f3b2-106">Naudodami „Microsoft Dynamics 365 Retail“ galite rodyti produktų rekomendacijas savo EKA įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-106">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 Retail.</span></span> <span data-ttu-id="3f3b2-107">Norėdami rodyti produktų rekomendacijas, turite valdiklį įtraukti į operacijų ekraną naudodami ekrano maketo dizaino įrankį.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="3f3b2-108">Atidarykite maketo dizaino įrankį</span><span class="sxs-lookup"><span data-stu-id="3f3b2-108">Open Layout designer</span></span>

1. <span data-ttu-id="3f3b2-109">Pasirinkite **Mažmeninė prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA** &gt; **Ekrano maketai**.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="3f3b2-110">Naudokite spartųjį filtrą, kad rastumėte ekraną, į kurį norite įtraukti valdiklį.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="3f3b2-111">Pvz., filtruokite lauką **Ekrano maketo ID** naudodami reikšmę **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="3f3b2-112">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="3f3b2-113">Pvz., pasirinkite **Pavadinimas: F2CP16:9M Ekrano maketo ID: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="3f3b2-114">Spustelėkite dalį **Maketo dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="3f3b2-115">Vykdykite paraginimo instrukcijas, kad paleistumėte maketo dizaino įrankį.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="3f3b2-116">Kai būsite paraginti įvesti kredencialus, įveskite tuos pačius kredencialus, kuriuos naudojote paleisdami maketo dizaino įrankį iš puslapio **Ekrano maketai**.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="3f3b2-117">Prisijungus bus parodytas puslapis, panašus į toliau pateiktą puslapį.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="3f3b2-118">Maketas skirsis, atsižvelgiant į jūsų parduotuvėje atliktus tinkinimus.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="3f3b2-119">[![Maketo dizaineris](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="3f3b2-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="3f3b2-120">Pasirinkite rodomą parinktį</span><span class="sxs-lookup"><span data-stu-id="3f3b2-120">Choose a display option</span></span>

<span data-ttu-id="3f3b2-121">Galima pasirinkti iš dviejų konfigūracijų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-121">There are two configurations options available.</span></span> <span data-ttu-id="3f3b2-122">Pasirinkite geriausiai jūsų parduotuvei tinkančią parinktį ir vadovaukitės likusiomis instrukcijomis, kad baigtumėte valdiklio nustatymą.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="3f3b2-123">Toliau nurodytos dvi parinktys.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-123">The two options are:</span></span>

- <span data-ttu-id="3f3b2-124">Rekomendacijos rodomos visada.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="3f3b2-125">Skirtukas **Rekomendacijos** rodomas ekrano kairiojoje pusėje esančiame tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="3f3b2-126">Nustatymas, kad rekomendacijos būtų visada matomos</span><span class="sxs-lookup"><span data-stu-id="3f3b2-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="3f3b2-127">Sumažinkite operacijų eilučių informacijos srities aukštį, kad ji būtų tokio paties aukščio kaip jos kairėje esanti kliento sritis.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="3f3b2-128">[![Sumažintas operacijų eilučių informacijos srities aukštis](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="3f3b2-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="3f3b2-129">Iš kairiojo meniu rekomendacijų valdiklį nuvilkite tarp operacijų eilučių informacijos srities ir mygtukyno į operacijų ekrano apatinėje dalyje, centre.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="3f3b2-130">Keiskite valdiklio dydį, kad jis tilptų toje erdvėje.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="3f3b2-131">[![Rekomendacijų valdiklis įtrauktas į maketą](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="3f3b2-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="3f3b2-132">Norėdami įrašyti ir uždaryti maketo dizaino įrankį, spustelėkite **X**.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="3f3b2-133">Programoje „Dynamics 365 for Retail“ atidarykite **Mažmeninė prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikai**.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-133">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="3f3b2-134">Išplečiamajame sąraše pasirinkite **1090 registrai**.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="3f3b2-135">Spustelėkite **Paleisti dabar**.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="3f3b2-136">Skirtuko Rekomendacijos įtraukimas į mygtukyną, esantį dešiniojoje ekrano pusėje</span><span class="sxs-lookup"><span data-stu-id="3f3b2-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="3f3b2-137">Dešiniuoju pelės klavišu spustelėkite tuščią erdvę po paskutiniuoju skirtuku mygtukyne, kuris yra kairiojoje puslapio pusėje.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="3f3b2-138">Spustelėkite **Pritaikyti**.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-138">Click **Customize**.</span></span>

    <span data-ttu-id="3f3b2-139">[![Tinkinimas – dialogo langas Skirtukų valdymas](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="3f3b2-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="3f3b2-140">Spustelėkite **Naujas skirtukas**.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-140">Click **New tab**.</span></span>
4. <span data-ttu-id="3f3b2-141">Raskite naują skirtuką, kurį ką tik įtraukėte.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-141">Find the new tab that you just added.</span></span> <span data-ttu-id="3f3b2-142">Gali reikėti slinkti žemyn.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="3f3b2-143">Išplečiamajame sąraše **Turinys** pasirinkite **Rekomenduojami produktai**.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="3f3b2-144">[![Parinkties Rekomenduojami produktai pasirinkimas lauke Turinys](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="3f3b2-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="3f3b2-145">Lauke **Žyma** įveskite rekomendacijų skirtuko pavadinimą. Pavyzdžiui, įveskite „Rekomenduojami produktai“.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="3f3b2-146">Lauke **Vaizdas** pasirinkite vaizdą, kuris bus rodomas skirtuke.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="3f3b2-147">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-147">Click **OK**.</span></span> <span data-ttu-id="3f3b2-148">Naujasis skirtukas atsiranda mygtukyne.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="3f3b2-149">Norėdami įrašyti ir uždaryti maketo dizaino įrankį, spustelėkite **X**.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="3f3b2-150">Programoje „Dynamics 365 for Retail“ atidarykite **Mažmeninė prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikai**.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-150">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="3f3b2-151">Išplečiamajame sąraše pasirinkite **1090 registrai**.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="3f3b2-152">Spustelėkite **Paleisti dabar**.</span><span class="sxs-lookup"><span data-stu-id="3f3b2-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3f3b2-153">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3f3b2-153">Additional resources</span></span>

[<span data-ttu-id="3f3b2-154">Produktų rekomendacijos EKA</span><span class="sxs-lookup"><span data-stu-id="3f3b2-154">Product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="3f3b2-155">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="3f3b2-155">Product recommendations overview</span></span>](../commerce/product-recommendations.md)
