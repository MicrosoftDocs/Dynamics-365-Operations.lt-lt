---
title: Poraštės modulis
description: Šioje temoje aprašomi poraštės moduliai ir tai, kaip juos kurti programoje „Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 42a71ea9498461febca80952acc3158517918332
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2020
ms.locfileid: "3816966"
---
# <a name="footer-module"></a><span data-ttu-id="9b97c-103">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="9b97c-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="9b97c-104">Šioje temoje aprašomi poraštės moduliai ir tai, kaip juos kurti programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="9b97c-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9b97c-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="9b97c-105">Overview</span></span>

<span data-ttu-id="9b97c-106">Poraštės modulis yra specialus konteineris, kuriame laikomi moduliai, rodomi puslapio poraštėje.</span><span class="sxs-lookup"><span data-stu-id="9b97c-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="9b97c-107">Pavyzdžiui, jame gali būti saitų su įvairiais svetainės puslapiais, pvz., puslapiais **Susisiekite su mumis** ir **Parduotuvės strategijos**.</span><span class="sxs-lookup"><span data-stu-id="9b97c-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="9b97c-108">Toliau pateiktame paveikslėlyje parodytas svetainės puslapyje esančio poraštės modulio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="9b97c-108">The following image shows an example of a footer module on a site page.</span></span>

![Poraštės modulio pavyzdys](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="9b97c-110">Poraštės modulių ypatybės</span><span class="sxs-lookup"><span data-stu-id="9b97c-110">Footer module properties</span></span> 

<span data-ttu-id="9b97c-111">Kaip ir dauguma konteinerių, poraštės modulis palaiko antraštės ir pločio ypatybes.</span><span class="sxs-lookup"><span data-stu-id="9b97c-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="9b97c-112">Jis taip pat palaiko kelių poraštės kategorijos modulių įtraukimo galimybę.</span><span class="sxs-lookup"><span data-stu-id="9b97c-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="9b97c-113">Kiekvienas įtrauktas poraštės kategorijos modulis poraštės modulyje vaizduojamas kaip stulpelis.</span><span class="sxs-lookup"><span data-stu-id="9b97c-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="9b97c-114">Poraštės modulyje esantys moduliai</span><span class="sxs-lookup"><span data-stu-id="9b97c-114">Modules available in a footer module</span></span>

<span data-ttu-id="9b97c-115">**Poraštės elementai** – poraštės elementų modulyje gali būti antraštė, vaizdas ir saitas.</span><span class="sxs-lookup"><span data-stu-id="9b97c-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="9b97c-116">Antraštė gali būti naudojama atskirai arba kartu su vaizdu ir saitu.</span><span class="sxs-lookup"><span data-stu-id="9b97c-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="9b97c-117">Kiekvieną poraštės saitą galima sukonfigūruoti taip, kad jame būtų tik tekstas (pavyzdžiui, saitai „Susisiekite su mumis“ ir „Privatumas“), arba kad jame būtų ir tekstas, ir vaizdas (pavyzdžiui, socialinės medijos saitai).</span><span class="sxs-lookup"><span data-stu-id="9b97c-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="9b97c-118">**Grįžti į viršų** – grįžimo į viršų modulis suteikia saitą greitai pereiti į puslapio viršų.</span><span class="sxs-lookup"><span data-stu-id="9b97c-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="9b97c-119">Būtina paskirties vieta.</span><span class="sxs-lookup"><span data-stu-id="9b97c-119">A destination is required.</span></span> <span data-ttu-id="9b97c-120">Numatytoji paskirties vietos reikšmė yra \#, kuri vartotoją perkelia į puslapio viršų.</span><span class="sxs-lookup"><span data-stu-id="9b97c-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="9b97c-121">Kurti poraštės modulį</span><span class="sxs-lookup"><span data-stu-id="9b97c-121">Create a footer module</span></span>

1. <span data-ttu-id="9b97c-122">Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas** tam, kad sukurtumėte naują fragmentą.</span><span class="sxs-lookup"><span data-stu-id="9b97c-122">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="9b97c-123">Dialogo lange **Naujas fragmentas** pasirinkite **Konteinerio** modulį, įveskite fragmento pavadinimą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9b97c-123">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="9b97c-124">Vietoje **Numatytasis konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="9b97c-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9b97c-125">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Poraštės kategorija** ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9b97c-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9b97c-126">Vietoje **Poraštės kategorija** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="9b97c-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9b97c-127">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Poraštės elementas** ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9b97c-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9b97c-128">Pasirinkite vietą **Poraštės elementas**, tada dešinėje esančioje ypatybių srityje pagal poreikį sukonfigūruokite antraštę, saitą ir saito tekstą bei vaizdą.</span><span class="sxs-lookup"><span data-stu-id="9b97c-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="9b97c-129">Norėdami įtraukti daugiau poraštės elementų, kiekvienam elementui pakartokite 5–7 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9b97c-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="9b97c-130">Norėdami į poraštę įtraukti saitą „grįžti į viršų“, pasirinkite vietoje **Poraštės kategorija** esantį daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="9b97c-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="9b97c-131">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Atgal į pradžią** ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9b97c-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9b97c-132">Pasirinkite vietą **Atgal į pradžią**, tada dešinėje esančioje ypatybių srityje pagal poreikį sukonfigūruokite tekstą ir kitas modulio ypatybes.</span><span class="sxs-lookup"><span data-stu-id="9b97c-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="9b97c-133">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="9b97c-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="9b97c-134">Norėdami padėti užtikrinti, kad antraštė būtų rodoma kiekviename puslapyje, kiekviename sukurtame svetainės puslapio šablone atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9b97c-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="9b97c-135">Modulio **Numatytasis puslapis** vietoje **Poraštė** įtraukite jūsų sukurtą poraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="9b97c-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="9b97c-136">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="9b97c-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="9b97c-137">Fragmentą įtraukdami į puslapio šablonus padedate užtikrinti, kad poraštė bus vaizduojama kiekviename puslapyje.</span><span class="sxs-lookup"><span data-stu-id="9b97c-137">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b97c-138">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9b97c-138">Additional resources</span></span>

[<span data-ttu-id="9b97c-139">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="9b97c-139">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9b97c-140">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="9b97c-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="9b97c-141">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="9b97c-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="9b97c-142">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="9b97c-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="9b97c-143">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="9b97c-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="9b97c-144">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="9b97c-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="9b97c-145">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="9b97c-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="9b97c-146">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="9b97c-146">Footer module</span></span>](author-footer-module.md)
