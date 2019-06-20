---
title: Rekomendacijų valdiklio įtraukimas į EKA įrenginių operacijų ekraną
description: Šioje temoje paaiškinama, kaip rekomendacijų valdiklį įtraukti į elektroninio kasos aparato (EKA) įrenginio operacijų ekraną naudojant ekrano maketo dizaino įrankį programoje „Microsoft Dynamics 365 for Retail“.
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
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
ms.openlocfilehash: f17da3db6fbc19548544a0c6c090a0b6db093673
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606854"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="dc15a-103">Rekomendacijų valdiklio įtraukimas į EKA įrenginių operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="dc15a-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="dc15a-104">Pašalinsime dabartinę produktų rekomendavimo paslaugos versiją ir šią funkciją pertvarkysime, suteikdami jai geresnį algoritmą ir naujesnes į mažmeninę prekybą orientuotas galimybes.</span><span class="sxs-lookup"><span data-stu-id="dc15a-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="dc15a-105">Daugiau informacijos žr. [Pašalintos arba nebenaudojamos funkcijos](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="dc15a-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span>

<span data-ttu-id="dc15a-106">Šioje temoje paaiškinama, kaip rekomendacijų valdiklį įtraukti į elektroninio kasos aparato (EKA) įrenginio operacijų ekraną naudojant ekrano maketo dizaino įrankį programoje „Microsoft Dynamics 365 for Retail“.</span><span class="sxs-lookup"><span data-stu-id="dc15a-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="dc15a-107">Naudodami „Microsoft Dynamics 365 for Retail“ galite rodyti produktų rekomendacijas savo EKA įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="dc15a-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="dc15a-108">*Rekomendacijos* –tai prekės, kurios gali sudominti jūsų klientą atsižvelgiant į jo pirkimo istoriją, prekės, kurias klientas įtraukė į savo norų sąrašą, ir prekės, kurias kiti klientai įsigijo internetu ir įprastose parduotuvėse.</span><span class="sxs-lookup"><span data-stu-id="dc15a-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="dc15a-109">Norėdami rodyti produktų rekomendacijas, turite valdiklį įtraukti į operacijų ekraną naudodami ekrano maketo dizaino įrankį.</span><span class="sxs-lookup"><span data-stu-id="dc15a-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="dc15a-110">Atidarykite maketo dizaino įrankį</span><span class="sxs-lookup"><span data-stu-id="dc15a-110">Open Layout designer</span></span>

1. <span data-ttu-id="dc15a-111">Pasirinkite **Mažmeninė prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA** &gt; **Ekrano maketai**.</span><span class="sxs-lookup"><span data-stu-id="dc15a-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="dc15a-112">Naudokite spartųjį filtrą, kad rastumėte ekraną, į kurį norite įtraukti valdiklį.</span><span class="sxs-lookup"><span data-stu-id="dc15a-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="dc15a-113">Pvz., filtruokite lauką **Ekrano maketo ID** naudodami reikšmę **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="dc15a-113">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="dc15a-114">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="dc15a-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="dc15a-115">Pvz., pasirinkite **Pavadinimas: F2CP16:9M Ekrano maketo ID: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="dc15a-115">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="dc15a-116">Spustelėkite dalį **Maketo dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="dc15a-116">Click **Layout designer**.</span></span>
5. <span data-ttu-id="dc15a-117">Vykdykite paraginimo instrukcijas, kad paleistumėte maketo dizaino įrankį.</span><span class="sxs-lookup"><span data-stu-id="dc15a-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="dc15a-118">Kai būsite paraginti įvesti kredencialus, įveskite tuos pačius kredencialus, kuriuos naudojote paleisdami maketo dizaino įrankį iš puslapio **Ekrano maketai**.</span><span class="sxs-lookup"><span data-stu-id="dc15a-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="dc15a-119">Prisijungus bus parodytas puslapis, panašus į toliau pateiktą puslapį.</span><span class="sxs-lookup"><span data-stu-id="dc15a-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="dc15a-120">Maketas skirsis, atsižvelgiant į jūsų parduotuvėje atliktus tinkinimus.</span><span class="sxs-lookup"><span data-stu-id="dc15a-120">The layout will be different depending on the customizations that were made for your store.</span></span>

    <span data-ttu-id="dc15a-121">[![Maketo dizaineris](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="dc15a-121">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="dc15a-122">Pasirinkite rodomą parinktį</span><span class="sxs-lookup"><span data-stu-id="dc15a-122">Choose a display option</span></span>

<span data-ttu-id="dc15a-123">Galima pasirinkti iš dviejų konfigūracijų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="dc15a-123">There are two configurations options available.</span></span> <span data-ttu-id="dc15a-124">Pasirinkite geriausiai jūsų parduotuvei tinkančią parinktį ir vadovaukitės likusiomis instrukcijomis, kad baigtumėte valdiklio nustatymą.</span><span class="sxs-lookup"><span data-stu-id="dc15a-124">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="dc15a-125">Toliau nurodytos dvi parinktys.</span><span class="sxs-lookup"><span data-stu-id="dc15a-125">The two options are:</span></span>

- <span data-ttu-id="dc15a-126">Rekomendacijos rodomos visada.</span><span class="sxs-lookup"><span data-stu-id="dc15a-126">Recommendations are always visible.</span></span>
- <span data-ttu-id="dc15a-127">Skirtukas **Rekomendacijos** rodomos ekrano kairiojoje pusėje esančiame tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="dc15a-127">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="dc15a-128">Nustatymas, kad rekomendacijos būtų visada matomos</span><span class="sxs-lookup"><span data-stu-id="dc15a-128">Make recommendations always visible</span></span>

1. <span data-ttu-id="dc15a-129">Sumažinkite operacijų eilučių informacijos srities aukštį, kad ji būtų tokio paties aukščio kaip jos kairėje esanti kliento sritis.</span><span class="sxs-lookup"><span data-stu-id="dc15a-129">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>

    <span data-ttu-id="dc15a-130">[![Sumažintas operacijų eilučių informacijos srities aukštis](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="dc15a-130">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="dc15a-131">Iš kairiojo meniu rekomendacijų valdiklį nuvilkite tarp operacijų eilučių informacijos srities ir mygtukyno į operacijų ekrano apatinėje dalyje, centre.</span><span class="sxs-lookup"><span data-stu-id="dc15a-131">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="dc15a-132">Keiskite valdiklio dydį, kad jis tilptų toje erdvėje.</span><span class="sxs-lookup"><span data-stu-id="dc15a-132">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="dc15a-133">[![Rekomendacijų valdiklis įtrauktas į maketą](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="dc15a-133">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>

3. <span data-ttu-id="dc15a-134">Norėdami įrašyti ir uždaryti maketo dizaino įrankį, spustelėkite **X**.</span><span class="sxs-lookup"><span data-stu-id="dc15a-134">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="dc15a-135">Programoje „Dynamics 365 for Retail“ atidarykite **Mažmeninė prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikai**.</span><span class="sxs-lookup"><span data-stu-id="dc15a-135">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="dc15a-136">Išplečiamajame sąraše pasirinkite  **1090 registrai**.</span><span class="sxs-lookup"><span data-stu-id="dc15a-136">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="dc15a-137">Spustelėkite **Paleisti dabar**.</span><span class="sxs-lookup"><span data-stu-id="dc15a-137">Click **Run now**.</span></span>

### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="dc15a-138">Skirtuko Rekomendacijos įtraukimas į mygtukyną, esantį dešiniojoje ekrano pusėje</span><span class="sxs-lookup"><span data-stu-id="dc15a-138">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="dc15a-139">Dešiniuoju pelės klavišu spustelėkite tuščią erdvę po paskutiniuoju skirtuku mygtukyne, kuris yra kairiojoje puslapio pusėje.</span><span class="sxs-lookup"><span data-stu-id="dc15a-139">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2. <span data-ttu-id="dc15a-140">Spustelėkite **Pritaikyti**.</span><span class="sxs-lookup"><span data-stu-id="dc15a-140">Click **Customize**.</span></span>

    <span data-ttu-id="dc15a-141">[![Tinkinimas – dialogo langas Skirtukų valdymas](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="dc15a-141">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="dc15a-142">Spustelėkite **Naujas skirtukas**.</span><span class="sxs-lookup"><span data-stu-id="dc15a-142">Click **New tab**.</span></span>
4. <span data-ttu-id="dc15a-143">Raskite naują skirtuką, kurį ką tik įtraukėte.</span><span class="sxs-lookup"><span data-stu-id="dc15a-143">Find the new tab that you just added.</span></span> <span data-ttu-id="dc15a-144">Gali reikėti slinkti žemyn.</span><span class="sxs-lookup"><span data-stu-id="dc15a-144">You may need to scroll down.</span></span>
5. <span data-ttu-id="dc15a-145">Išplečiamajame sąraše **Turinys** pasirinkite **Rekomenduojami produktai**.</span><span class="sxs-lookup"><span data-stu-id="dc15a-145">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="dc15a-146">[![Parinkties Rekomenduojami produktai pasirinkimas lauke Turinys](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="dc15a-146">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="dc15a-147">Lauke **Žyma** įveskite rekomendacijų skirtuko pavadinimą. Pavyzdžiui, įveskite „Rekomenduojami produktai“.</span><span class="sxs-lookup"><span data-stu-id="dc15a-147">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="dc15a-148">Lauke **Vaizdas** pasirinkite vaizdą, kuris bus rodomas skirtuke.</span><span class="sxs-lookup"><span data-stu-id="dc15a-148">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="dc15a-149">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="dc15a-149">Click **OK**.</span></span> <span data-ttu-id="dc15a-150">Naujasis skirtukas atsiranda mygtukyne.</span><span class="sxs-lookup"><span data-stu-id="dc15a-150">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="dc15a-151">Norėdami įrašyti ir uždaryti maketo dizaino įrankį, spustelėkite **X**.</span><span class="sxs-lookup"><span data-stu-id="dc15a-151">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="dc15a-152">Programoje „Dynamics 365 for Retail“ atidarykite **Mažmeninė prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikai**.</span><span class="sxs-lookup"><span data-stu-id="dc15a-152">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="dc15a-153">Išplečiamajame sąraše pasirinkite **1090 registrai**.</span><span class="sxs-lookup"><span data-stu-id="dc15a-153">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="dc15a-154">Spustelėkite **Paleisti dabar**.</span><span class="sxs-lookup"><span data-stu-id="dc15a-154">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dc15a-155">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="dc15a-155">Additional resources</span></span>

[<span data-ttu-id="dc15a-156">Personalizuotų produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="dc15a-156">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)
