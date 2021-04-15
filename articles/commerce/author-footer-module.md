---
title: Poraštės modulis
description: Šioje temoje aprašomi poraštės moduliai ir tai, kaip juos kurti programoje „Dynamics 365 Commerce“.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d6e7b0ad4fe0723575a0ec55a9b02d110568db58
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797238"
---
# <a name="footer-module"></a><span data-ttu-id="f19a3-103">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="f19a3-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="f19a3-104">Šioje temoje aprašomi poraštės moduliai ir tai, kaip juos kurti programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="f19a3-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f19a3-105">Poraštės modulis yra specialus konteineris, kuriame laikomi moduliai, rodomi puslapio poraštėje.</span><span class="sxs-lookup"><span data-stu-id="f19a3-105">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="f19a3-106">Pavyzdžiui, jame gali būti saitų su įvairiais svetainės puslapiais, pvz., puslapiais **Susisiekite su mumis** ir **Parduotuvės strategijos**.</span><span class="sxs-lookup"><span data-stu-id="f19a3-106">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="f19a3-107">Toliau pateiktame paveikslėlyje parodytas svetainės puslapyje esančio poraštės modulio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="f19a3-107">The following image shows an example of a footer module on a site page.</span></span>

![Poraštės modulio pavyzdys](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="f19a3-109">Poraštės modulių ypatybės</span><span class="sxs-lookup"><span data-stu-id="f19a3-109">Footer module properties</span></span> 

<span data-ttu-id="f19a3-110">Kaip ir dauguma konteinerių, poraštės modulis palaiko antraštės ir pločio ypatybes.</span><span class="sxs-lookup"><span data-stu-id="f19a3-110">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="f19a3-111">Jis taip pat palaiko kelių poraštės kategorijos modulių įtraukimo galimybę.</span><span class="sxs-lookup"><span data-stu-id="f19a3-111">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="f19a3-112">Kiekvienas įtrauktas poraštės kategorijos modulis poraštės modulyje vaizduojamas kaip stulpelis.</span><span class="sxs-lookup"><span data-stu-id="f19a3-112">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="f19a3-113">Poraštės modulyje esantys moduliai</span><span class="sxs-lookup"><span data-stu-id="f19a3-113">Modules available in a footer module</span></span>

<span data-ttu-id="f19a3-114">**Poraštės elementai** – poraštės elementų modulyje gali būti antraštė, vaizdas ir saitas.</span><span class="sxs-lookup"><span data-stu-id="f19a3-114">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="f19a3-115">Antraštė gali būti naudojama atskirai arba kartu su vaizdu ir saitu.</span><span class="sxs-lookup"><span data-stu-id="f19a3-115">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="f19a3-116">Kiekvieną poraštės saitą galima sukonfigūruoti taip, kad jame būtų tik tekstas (pavyzdžiui, saitai „Susisiekite su mumis“ ir „Privatumas“), arba kad jame būtų ir tekstas, ir vaizdas (pavyzdžiui, socialinės medijos saitai).</span><span class="sxs-lookup"><span data-stu-id="f19a3-116">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="f19a3-117">**Grįžti į viršų** – grįžimo į viršų modulis suteikia saitą greitai pereiti į puslapio viršų.</span><span class="sxs-lookup"><span data-stu-id="f19a3-117">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="f19a3-118">Būtina paskirties vieta.</span><span class="sxs-lookup"><span data-stu-id="f19a3-118">A destination is required.</span></span> <span data-ttu-id="f19a3-119">Numatytoji paskirties vietos reikšmė yra \#, kuri vartotoją perkelia į puslapio viršų.</span><span class="sxs-lookup"><span data-stu-id="f19a3-119">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="f19a3-120">Kurti poraštės modulį</span><span class="sxs-lookup"><span data-stu-id="f19a3-120">Create a footer module</span></span>

1. <span data-ttu-id="f19a3-121">Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas** tam, kad sukurtumėte naują fragmentą.</span><span class="sxs-lookup"><span data-stu-id="f19a3-121">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="f19a3-122">Dialogo lange **Naujas fragmentas** pasirinkite **Konteinerio** modulį, įveskite fragmento pavadinimą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f19a3-122">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="f19a3-123">Vietoje **Numatytasis konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="f19a3-123">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f19a3-124">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Poraštės kategorija** ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f19a3-124">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f19a3-125">Vietoje **Poraštės kategorija** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="f19a3-125">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f19a3-126">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Poraštės elementas** ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f19a3-126">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f19a3-127">Pasirinkite vietą **Poraštės elementas**, tada dešinėje esančioje ypatybių srityje pagal poreikį sukonfigūruokite antraštę, saitą ir saito tekstą bei vaizdą.</span><span class="sxs-lookup"><span data-stu-id="f19a3-127">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="f19a3-128">Norėdami įtraukti daugiau poraštės elementų, kiekvienam elementui pakartokite 5–7 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f19a3-128">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="f19a3-129">Norėdami į poraštę įtraukti saitą „grįžti į viršų“, pasirinkite vietoje **Poraštės kategorija** esantį daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="f19a3-129">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="f19a3-130">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Atgal į pradžią** ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f19a3-130">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f19a3-131">Pasirinkite vietą **Atgal į pradžią**, tada dešinėje esančioje ypatybių srityje pagal poreikį sukonfigūruokite tekstą ir kitas modulio ypatybes.</span><span class="sxs-lookup"><span data-stu-id="f19a3-131">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="f19a3-132">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="f19a3-132">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="f19a3-133">Norėdami padėti užtikrinti, kad antraštė būtų rodoma kiekviename puslapyje, kiekviename sukurtame svetainės puslapio šablone atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f19a3-133">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="f19a3-134">Modulio **Numatytasis puslapis** vietoje **Poraštė** įtraukite jūsų sukurtą poraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="f19a3-134">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="f19a3-135">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="f19a3-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="f19a3-136">Fragmentą įtraukdami į puslapio šablonus padedate užtikrinti, kad poraštė bus vaizduojama kiekviename puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f19a3-136">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f19a3-137">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f19a3-137">Additional resources</span></span>

[<span data-ttu-id="f19a3-138">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="f19a3-138">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f19a3-139">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="f19a3-139">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f19a3-140">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="f19a3-140">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f19a3-141">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="f19a3-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f19a3-142">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="f19a3-142">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f19a3-143">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="f19a3-143">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f19a3-144">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="f19a3-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f19a3-145">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="f19a3-145">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]