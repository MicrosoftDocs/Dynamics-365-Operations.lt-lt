---
title: Poraštės modulis
description: Šioje temoje aprašomi poraštės moduliai ir tai, kaip juos kurti programoje „Dynamics 365 Commerce“.
author: anupamar
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 51f8d26d6223dcd1f6961058cd9d772a67c69670
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269641"
---
# <a name="footer-module"></a><span data-ttu-id="b1a4f-103">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="b1a4f-103">Footer module</span></span>  


[!include [banner](includes/banner.md)]

<span data-ttu-id="b1a4f-104">Šioje temoje aprašomi poraštės moduliai ir tai, kaip juos kurti programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b1a4f-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="b1a4f-105">Overview</span></span>

<span data-ttu-id="b1a4f-106">Poraštės modulis yra specialus konteineris, kuriame laikomi moduliai, rodomi puslapio poraštėje.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="b1a4f-107">Pavyzdžiui, jame gali būti saitų su įvairiais svetainės puslapiais, pvz., puslapiais **Susisiekite su mumis** ir **Parduotuvės strategijos**.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

## <a name="footer-module-properties"></a><span data-ttu-id="b1a4f-108">Poraštės modulių ypatybės</span><span class="sxs-lookup"><span data-stu-id="b1a4f-108">Footer module properties</span></span> 

<span data-ttu-id="b1a4f-109">Kaip ir dauguma konteinerių, poraštės modulis palaiko antraštės ir pločio ypatybes.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-109">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="b1a4f-110">Jis taip pat palaiko kelių poraštės kategorijos modulių įtraukimo galimybę.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-110">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="b1a4f-111">Kiekvienas įtrauktas poraštės kategorijos modulis poraštės modulyje vaizduojamas kaip stulpelis.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-111">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="b1a4f-112">Poraštės modulyje esantys moduliai</span><span class="sxs-lookup"><span data-stu-id="b1a4f-112">Modules available in a footer module</span></span>

<span data-ttu-id="b1a4f-113">**Poraštės elementai** – poraštės elementų modulyje gali būti antraštė, vaizdas ir saitas.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-113">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="b1a4f-114">Antraštė gali būti naudojama atskirai arba kartu su vaizdu ir saitu.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-114">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="b1a4f-115">Kiekvieną poraštės saitą galima sukonfigūruoti taip, kad jame būtų tik tekstas (pavyzdžiui, saitai „Susisiekite su mumis“ ir „Privatumas“), arba kad jame būtų ir tekstas, ir vaizdas (pavyzdžiui, socialinės medijos saitai).</span><span class="sxs-lookup"><span data-stu-id="b1a4f-115">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="b1a4f-116">**Grįžti į viršų** – grįžimo į viršų modulis suteikia saitą greitai pereiti į puslapio viršų.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-116">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="b1a4f-117">Būtina paskirties vieta.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-117">A destination is required.</span></span> <span data-ttu-id="b1a4f-118">Numatytoji paskirties vietos reikšmė yra #, kuri vartotoją perkelia į puslapio viršų.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-118">The default destination value is #, which takes the user to the top of the page.</span></span>

## <a name="author-a-footer-module"></a><span data-ttu-id="b1a4f-119">Poraštės modulio kūrimas</span><span class="sxs-lookup"><span data-stu-id="b1a4f-119">Author a footer module</span></span>

1. <span data-ttu-id="b1a4f-120">Naršymo srityje pasirinkite **Fragmentai** ir **Naujas puslapio fragmentas**.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-120">In the navigation pane, select **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="b1a4f-121">Dialogo lange **Naujas puslapio fragmentas** pasirinkite poraštės modulį, įveskite puslapio fragmento pavadinimą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-121">In the **New Page Fragment** dialog box, select the footer module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b1a4f-122">Kairėje esančiame struktūros medyje pasirinkite prie poraštės modulio esantį daugtaškio mygtuką (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-122">In the outline tree on the left, select the ellipsis button (**...**) for the footer module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="b1a4f-123">Dialogo lange **Modulio įtraukimas** pasirinkite poraštės kategorijos modulį ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-123">In the **Add Module** dialog box, select the footer category module, and then select **OK**.</span></span>
1. <span data-ttu-id="b1a4f-124">Struktūros medyje pasirinkite prie poraštės kategorijos modulio esantį daugtaškio mygtuką, tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-124">In the outline tree, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="b1a4f-125">Dialogo lange **Modulio įtraukimas** pasirinkite poraštės elemento modulį ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-125">In the **Add Module** dialog box, select the footer item module, and then select **OK**.</span></span>
1. <span data-ttu-id="b1a4f-126">Struktūros medyje pasirinkite poraštės elemento modulį.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-126">In the outline tree, select the footer item module.</span></span> <span data-ttu-id="b1a4f-127">Tada dešinėje esančioje ypatybių srityje pagal poreikį sukonfigūruokite antraštę, saitą ir saito tekstą bei vaizdą.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-127">Then, in the properties pane on the right, configure the heading, link and link text, and image as you require.</span></span>
1. <span data-ttu-id="b1a4f-128">Norėdami įtraukti daugiau poraštės elementų, pakartokite 5–7 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-128">To add more footer items, repeat steps 5 through 7.</span></span>
1. <span data-ttu-id="b1a4f-129">Norėdami į poraštę įtraukti saitą „grįžti į viršų“, pasirinkite prie poraštės kategorijos modulio esantį daugtaškio mygtuką, tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-129">To add a "back to top" link to your footer, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="b1a4f-130">Dialogo lange **Modulio įtraukimas** pasirinkite grįžimo į viršų modulį ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-130">In the **Add Module** dialog box, select the back to top module, and then select **OK**.</span></span>
1. <span data-ttu-id="b1a4f-131">Struktūros medyje pasirinkite grįžimo į viršų modulį.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-131">In the outline tree, select the back to top module.</span></span> <span data-ttu-id="b1a4f-132">Tada dešinėje esančioje ypatybių srityje pagal poreikį sukonfigūruokite grįžimo į viršų modulį.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-132">Then, in the properties pane on the right, configure the back to top module as you require.</span></span>
1. <span data-ttu-id="b1a4f-133">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapio fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-133">Select **Save**, select **Finish editing** to check in the page fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="b1a4f-134">Kiekviename sukurtame svetainės puslapio šablone atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-134">On every page template that has been created for the site, follow these steps.</span></span>

1. <span data-ttu-id="b1a4f-135">Numatytojo puslapio vietos **Pagrindinis** poraštės modulyje įtraukite sukurtą poraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-135">In the **Main** slot of the default page, in the footer module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="b1a4f-136">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-136">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="b1a4f-137">Puslapio fragmentą įtraukdami į puslapio šablonus, padedate užtikrinti, kad poraštė bus vaizduojama kiekviename puslapyje.</span><span class="sxs-lookup"><span data-stu-id="b1a4f-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1a4f-138">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b1a4f-138">Additional resources</span></span>

[<span data-ttu-id="b1a4f-139">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="b1a4f-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b1a4f-140">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="b1a4f-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b1a4f-141">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="b1a4f-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b1a4f-142">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="b1a4f-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b1a4f-143">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="b1a4f-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b1a4f-144">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="b1a4f-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b1a4f-145">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="b1a4f-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="b1a4f-146">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="b1a4f-146">Footer module</span></span>](author-footer-module.md)
