---
title: Rekomendacijų įtraukimas į operacijų ekraną
description: Šioje temoje paaiškinama, kaip rekomendacijų valdiklį įtraukti į elektroninio kasos aparato (EKA) įrenginio operacijų ekraną naudojant ekrano maketo dizaino įrankį programoje „Microsoft Dynamics 365 Commerce“.
author: bebeale
manager: AnnBe
ms.date: 05/26/20
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
ms.openlocfilehash: 77870cd19ebf15a72f323f116579f7769a766995
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404238"
---
# <a name="add-recommendations-to-the-transaction-screen"></a><span data-ttu-id="92e25-103">Rekomendacijų įtraukimas į operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="92e25-103">Add recommendations to the transaction screen</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="92e25-104">Šioje temoje paaiškinama, kaip rekomendacijų valdiklį įtraukti į elektroninio kasos aparato (EKA) įrenginio operacijų ekraną naudojant ekrano maketo dizaino įrankį programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="92e25-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="92e25-105">Norėdami gauti daugiau informacijos apie produktų rekomendacijas, perskaitykite [EKA dokumentacijos produktų rekomendacijas.](product.md).</span><span class="sxs-lookup"><span data-stu-id="92e25-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="92e25-106">Naudodami „Commerce“ galite rodyti produktų rekomendacijas savo EKA įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="92e25-106">You can display product recommendations on your POS device when you use Commerce.</span></span> <span data-ttu-id="92e25-107">Norėdami rodyti produktų rekomendacijas, turite valdiklį įtraukti į operacijų ekraną naudodami ekrano maketo dizaino įrankį.</span><span class="sxs-lookup"><span data-stu-id="92e25-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="92e25-108">Atidarykite maketo dizaino įrankį</span><span class="sxs-lookup"><span data-stu-id="92e25-108">Open Layout designer</span></span>

1. <span data-ttu-id="92e25-109">Pasirinkite **Mažmeninė prekyba ir prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA** &gt; **Ekrano maketai**.</span><span class="sxs-lookup"><span data-stu-id="92e25-109">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="92e25-110">Naudokite spartųjį filtrą, kad rastumėte ekraną, į kurį norite įtraukti valdiklį.</span><span class="sxs-lookup"><span data-stu-id="92e25-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="92e25-111">Pvz., filtruokite lauką **Ekrano maketo ID** naudodami reikšmę **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="92e25-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="92e25-112">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="92e25-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="92e25-113">Pvz., pasirinkite **Pavadinimas: F2CP16:9M Ekrano maketo ID: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="92e25-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="92e25-114">Spustelėkite dalį **Maketo dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="92e25-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="92e25-115">Vykdykite paraginimo instrukcijas, kad paleistumėte maketo dizaino įrankį.</span><span class="sxs-lookup"><span data-stu-id="92e25-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="92e25-116">Kai būsite paraginti įvesti kredencialus, įveskite tuos pačius kredencialus, kuriuos naudojote paleisdami maketo dizaino įrankį iš puslapio **Ekrano maketai**.</span><span class="sxs-lookup"><span data-stu-id="92e25-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="92e25-117">Prisijungus bus parodytas puslapis, panašus į toliau pateiktą puslapį.</span><span class="sxs-lookup"><span data-stu-id="92e25-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="92e25-118">Maketas skirsis, atsižvelgiant į jūsų parduotuvėje atliktus tinkinimus.</span><span class="sxs-lookup"><span data-stu-id="92e25-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="92e25-119">[![Maketo dizaineris](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="92e25-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="92e25-120">Pasirinkite rodomą parinktį</span><span class="sxs-lookup"><span data-stu-id="92e25-120">Choose a display option</span></span>

<span data-ttu-id="92e25-121">Galima pasirinkti iš dviejų konfigūracijų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="92e25-121">There are two configurations options available.</span></span> <span data-ttu-id="92e25-122">Pasirinkite geriausiai jūsų parduotuvei tinkančią parinktį ir vadovaukitės likusiomis instrukcijomis, kad baigtumėte valdiklio nustatymą.</span><span class="sxs-lookup"><span data-stu-id="92e25-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="92e25-123">Toliau nurodytos dvi parinktys.</span><span class="sxs-lookup"><span data-stu-id="92e25-123">The two options are:</span></span>

- <span data-ttu-id="92e25-124">Rekomendacijos rodomos visada.</span><span class="sxs-lookup"><span data-stu-id="92e25-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="92e25-125">Skirtukas **Rekomendacijos** rodomas ekrano kairiojoje pusėje esančiame tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="92e25-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="92e25-126">Nustatymas, kad rekomendacijos būtų visada matomos</span><span class="sxs-lookup"><span data-stu-id="92e25-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="92e25-127">Sumažinkite operacijų eilučių informacijos srities aukštį, kad ji būtų tokio paties aukščio kaip jos kairėje esanti kliento sritis.</span><span class="sxs-lookup"><span data-stu-id="92e25-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="92e25-128">[![Sumažintas operacijų eilučių informacijos srities aukštis](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="92e25-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="92e25-129">Iš kairiojo meniu rekomendacijų valdiklį nuvilkite tarp operacijų eilučių informacijos srities ir mygtukyno į operacijų ekrano apatinėje dalyje, centre.</span><span class="sxs-lookup"><span data-stu-id="92e25-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="92e25-130">Keiskite valdiklio dydį, kad jis tilptų toje erdvėje.</span><span class="sxs-lookup"><span data-stu-id="92e25-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="92e25-131">[![Rekomendacijų valdiklis įtrauktas į maketą](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="92e25-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="92e25-132">Norėdami įrašyti ir uždaryti maketo dizaino įrankį, spustelėkite **X**.</span><span class="sxs-lookup"><span data-stu-id="92e25-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="92e25-133">„Commerce“ eikite į **Mažmeninė prekyba ir prekyba** &gt; **Mažmeninės prekybos ir prekybos IT** &gt; **Paskirstymo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="92e25-133">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="92e25-134">Išplečiamajame sąraše pasirinkite **1090 registrai**.</span><span class="sxs-lookup"><span data-stu-id="92e25-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="92e25-135">Spustelėkite **Paleisti dabar**.</span><span class="sxs-lookup"><span data-stu-id="92e25-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="92e25-136">Skirtuko Rekomendacijos įtraukimas į mygtukyną, esantį dešiniojoje ekrano pusėje</span><span class="sxs-lookup"><span data-stu-id="92e25-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="92e25-137">Dešiniuoju pelės klavišu spustelėkite tuščią erdvę po paskutiniuoju skirtuku mygtukyne, kuris yra kairiojoje puslapio pusėje.</span><span class="sxs-lookup"><span data-stu-id="92e25-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="92e25-138">Spustelėkite **Pritaikyti**.</span><span class="sxs-lookup"><span data-stu-id="92e25-138">Click **Customize**.</span></span>

    <span data-ttu-id="92e25-139">[![Tinkinimas – dialogo langas Skirtukų valdymas](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="92e25-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="92e25-140">Spustelėkite **Naujas skirtukas**.</span><span class="sxs-lookup"><span data-stu-id="92e25-140">Click **New tab**.</span></span>
4. <span data-ttu-id="92e25-141">Raskite naują skirtuką, kurį ką tik įtraukėte.</span><span class="sxs-lookup"><span data-stu-id="92e25-141">Find the new tab that you just added.</span></span> <span data-ttu-id="92e25-142">Gali reikėti slinkti žemyn.</span><span class="sxs-lookup"><span data-stu-id="92e25-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="92e25-143">Išplečiamajame sąraše **Turinys** pasirinkite **Rekomenduojami produktai**.</span><span class="sxs-lookup"><span data-stu-id="92e25-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="92e25-144">[![Parinkties Rekomenduojami produktai pasirinkimas lauke Turinys](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="92e25-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="92e25-145">Lauke **Žyma** įveskite rekomendacijų skirtuko pavadinimą. Pavyzdžiui, įveskite „Rekomenduojami produktai“.</span><span class="sxs-lookup"><span data-stu-id="92e25-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="92e25-146">Lauke **Vaizdas** pasirinkite vaizdą, kuris bus rodomas skirtuke.</span><span class="sxs-lookup"><span data-stu-id="92e25-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="92e25-147">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="92e25-147">Click **OK**.</span></span> <span data-ttu-id="92e25-148">Naujasis skirtukas atsiranda mygtukyne.</span><span class="sxs-lookup"><span data-stu-id="92e25-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="92e25-149">Norėdami įrašyti ir uždaryti maketo dizaino įrankį, spustelėkite **X**.</span><span class="sxs-lookup"><span data-stu-id="92e25-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="92e25-150">„Commerce“ eikite į **Mažmeninė prekyba ir prekyba** &gt; **Mažmeninės prekybos ir prekybos IT** &gt; **Paskirstymo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="92e25-150">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="92e25-151">Išplečiamajame sąraše pasirinkite **1090 registrai**.</span><span class="sxs-lookup"><span data-stu-id="92e25-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="92e25-152">Spustelėkite **Paleisti dabar**.</span><span class="sxs-lookup"><span data-stu-id="92e25-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92e25-153">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="92e25-153">Additional resources</span></span>

[<span data-ttu-id="92e25-154">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="92e25-154">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="92e25-155">„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="92e25-155">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="92e25-156">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="92e25-156">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="92e25-157">Personalizuotų rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="92e25-157">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="92e25-158">Personalizuotų rekomendacijų atsisakymas</span><span class="sxs-lookup"><span data-stu-id="92e25-158">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="92e25-159">Produktų rekomendacijų įtraukimas į EKA</span><span class="sxs-lookup"><span data-stu-id="92e25-159">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="92e25-160">AI-ML rekomendacijų rezultatų koregavimas</span><span class="sxs-lookup"><span data-stu-id="92e25-160">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="92e25-161">Kuruojamų rekomendacijų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="92e25-161">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="92e25-162">Rekomendacijų su demonstraciniais duomenimis kūrimas</span><span class="sxs-lookup"><span data-stu-id="92e25-162">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="92e25-163">DUK apie produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="92e25-163">Product recommendations FAQ</span></span>](faq-recommendations.md)
