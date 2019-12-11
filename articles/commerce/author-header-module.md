---
title: Antraštės modulis
description: Šioje temoje aprašomi antraštės moduliai ir tai, kaip juos kurti programoje „Microsoft Dynamics 365 Commerce“.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697280"
---
# <a name="header-module"></a><span data-ttu-id="f25b8-103">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="f25b8-103">Header module</span></span>

<span data-ttu-id="f25b8-104">[!include [banner](includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span><span class="sxs-lookup"><span data-stu-id="f25b8-104">[!include [banner]includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span></span>

<span data-ttu-id="f25b8-105">Šioje temoje aprašomi antraštės moduliai ir tai, kaip juos kurti programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="f25b8-105">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f25b8-106">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="f25b8-106">Overview</span></span>

<span data-ttu-id="f25b8-107">Antraštės modulis yra specialus konteineris, kuriame laikomi visi moduliai, kurie bus rodomi puslapio antraštėje.</span><span class="sxs-lookup"><span data-stu-id="f25b8-107">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="f25b8-108">Pavyzdžiui, jame gali būti svetainės logotipas, saitai su naršymo hierarchija, saitai su kitais svetainės puslapiais ir ieškos juosta.</span><span class="sxs-lookup"><span data-stu-id="f25b8-108">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="f25b8-109">Antraštės modulis automatiškai optimizuojamas įrenginiui, kuriame peržiūrima svetainė (t. y., stacionariam įrenginiui arba mobiliajam įrenginiui).</span><span class="sxs-lookup"><span data-stu-id="f25b8-109">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="f25b8-110">Pavyzdžiui, mobiliajame įrenginyje naršymo juosta sutraukiama į mygtuką **Meniu** (kuris kartais vadinamas *mėsainio stiliaus meniu*).</span><span class="sxs-lookup"><span data-stu-id="f25b8-110">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="f25b8-111">Antraštės ypatybės</span><span class="sxs-lookup"><span data-stu-id="f25b8-111">Properties of a header</span></span>

<span data-ttu-id="f25b8-112">Kaip ir bendrieji konteineriai, antraštės modulis palaiko **antraštės** ir **pločio** ypatybes.</span><span class="sxs-lookup"><span data-stu-id="f25b8-112">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="f25b8-113">Antraštės modulyje yra kelios vietos.</span><span class="sxs-lookup"><span data-stu-id="f25b8-113">A header module has multiple slots.</span></span> <span data-ttu-id="f25b8-114">Pavyzdžiui, yra vietos informaciniam pranešimui, naršymo meniu, logotipui, ieškos juostai, krepšelio piktogramai, pageidavimų sąrašo piktogramai ir paskyros informacijai.</span><span class="sxs-lookup"><span data-stu-id="f25b8-114">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="f25b8-115">Kiekviena vieta palaiko konkretų modulių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="f25b8-115">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="f25b8-116">Moduliai, esantys antraštės modulyje</span><span class="sxs-lookup"><span data-stu-id="f25b8-116">Modules that are available in a header module</span></span>

<span data-ttu-id="f25b8-117">Antraštės modulyje galima naudoti tolesnius modulius.</span><span class="sxs-lookup"><span data-stu-id="f25b8-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="f25b8-118">**Naršymo meniu** – naršymo meniu vaizduojama kanalo naršymo hierarchija ir kiti statiniai naršymo saitai.</span><span class="sxs-lookup"><span data-stu-id="f25b8-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="f25b8-119">Kanalo naršymo hierarchiją galima konfigūruoti programoje „Dynamics 365 Retail“.</span><span class="sxs-lookup"><span data-stu-id="f25b8-119">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="f25b8-120">Sukonfigūruoti elementai tada rodomi kaip antraštės naršymo elementai.</span><span class="sxs-lookup"><span data-stu-id="f25b8-120">Configured items then appear as header navigation.</span></span> <span data-ttu-id="f25b8-121">Be to, galima sukonfigūruoti statinius naršymo saitus ir pateikti santykinius saitus su kitais el. prekybos svetainės puslapiais.</span><span class="sxs-lookup"><span data-stu-id="f25b8-121">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="f25b8-122">Pačią antraštę galima lygiuoti kairėje, dešinėje arba centre.</span><span class="sxs-lookup"><span data-stu-id="f25b8-122">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="f25b8-123">**Krepšelio piktograma** – krepšelio piktograma yra speciali piktograma, vaizduojanti krepšelį.</span><span class="sxs-lookup"><span data-stu-id="f25b8-123">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="f25b8-124">Ji rodoma antraštėje ir nurodo krepšelyje esančių prekių skaičių.</span><span class="sxs-lookup"><span data-stu-id="f25b8-124">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="f25b8-125">Prie krepšelio piktogramos turėtų būti saitas su krepšelio puslapiu, kad naudodami piktogramą klientai galėtų būti nukreipiami į krepšelio puslapį.</span><span class="sxs-lookup"><span data-stu-id="f25b8-125">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="f25b8-126">**Pageidavimų sąrašo piktograma** – pageidavimų sąrašo piktograma rodoma antraštėje ir nurodo prekių, įtrauktų į kliento pageidavimų sąrašą, skaičių.</span><span class="sxs-lookup"><span data-stu-id="f25b8-126">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="f25b8-127">Prie šios piktogramos turėtų būti saitas su pageidavimų sąrašo puslapiu, kad naudodami piktogramą klientai galėtų būti nukreipiami į pageidavimų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="f25b8-127">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="f25b8-128">**Prisijungimo modulis** – antraštėje rodomas prisijungimo modulis.</span><span class="sxs-lookup"><span data-stu-id="f25b8-128">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="f25b8-129">Jį naudodami klientai gali prisijungti prie savo paskyros arba registruotis paskyrai.</span><span class="sxs-lookup"><span data-stu-id="f25b8-129">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="f25b8-130">Jei klientas jau prisijungęs, modulį galima sukonfigūruoti taip, kad jame būtų rodomi saitai su paskyros puslapiu, užsakymų retrospektyvos puslapiu ar kitu puslapiu.</span><span class="sxs-lookup"><span data-stu-id="f25b8-130">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="f25b8-131">**Logotipo modulis** – šiame modulyje rodomas logotipas, vaizduojantis pardavėją ir prekės ženklą.</span><span class="sxs-lookup"><span data-stu-id="f25b8-131">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="f25b8-132">Tai yra vaizdas su saitu.</span><span class="sxs-lookup"><span data-stu-id="f25b8-132">It's an image that has a link.</span></span> <span data-ttu-id="f25b8-133">Saitas paprastai sukonfigūruotas taip, kad nukreiptų į pagrindinį puslapį, todėl klientai gali greitai grįžti į pagrindinį puslapį iš bet kurio svetainės puslapio.</span><span class="sxs-lookup"><span data-stu-id="f25b8-133">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="f25b8-134">**Įspėjimas** – antraštėje rodomas įspėjimas, kurį naudojant rodomas įdėtasis pranešimas, taikomas visiems svetainės puslapiams.</span><span class="sxs-lookup"><span data-stu-id="f25b8-134">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="f25b8-135">Pavyzdžiui, įspėjime gali būti rodomas pranešimas, pvz., „Metinis išpardavimas baigiasi už 2 dienų“.</span><span class="sxs-lookup"><span data-stu-id="f25b8-135">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="f25b8-136">**Ieškos juosta** – ieškos juostoje vartotojai gali įvesti ieškos terminus, kad galėtų ieškoti produktų.</span><span class="sxs-lookup"><span data-stu-id="f25b8-136">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="f25b8-137">Modulyje reikia sukonfigūruoti ieškos rezultatų puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="f25b8-137">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="f25b8-138">Galima sukonfigūruoti užklausos eilutės parametrą (numatytoji reikšmė yra **q**).</span><span class="sxs-lookup"><span data-stu-id="f25b8-138">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="f25b8-139">Ieškos juostoje yra automatinio siūlymo vieta, kurioje reikia įtraukti automatinio siūlymo modulį.</span><span class="sxs-lookup"><span data-stu-id="f25b8-139">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="f25b8-140">**Automatinis siūlymas** – automatinio siūlymo modulyje rodomi automatiškai pasiūlyti rezultatai.</span><span class="sxs-lookup"><span data-stu-id="f25b8-140">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="f25b8-141">Šie rezultatai gali būti raktažodžiai, produktai ar kategorijos, kur randamas ieškos terminas.</span><span class="sxs-lookup"><span data-stu-id="f25b8-141">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="f25b8-142">Kurti antraštės modulį</span><span class="sxs-lookup"><span data-stu-id="f25b8-142">Create a header module</span></span>

<span data-ttu-id="f25b8-143">Norėdami sukurti antraštės modulį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f25b8-143">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="f25b8-144">Sukurkite puslapio fragmentą, kuriame yra antraštės modulis.</span><span class="sxs-lookup"><span data-stu-id="f25b8-144">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="f25b8-145">Į antraštės modulio vietas įtraukite modulių.</span><span class="sxs-lookup"><span data-stu-id="f25b8-145">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="f25b8-146">Atnaujinkite kiekvieno modulio parametrus.</span><span class="sxs-lookup"><span data-stu-id="f25b8-146">Update the settings for each module.</span></span>
1. <span data-ttu-id="f25b8-147">Puslapio fragmentą įrašykite.</span><span class="sxs-lookup"><span data-stu-id="f25b8-147">Save the page fragment.</span></span> 
1. <span data-ttu-id="f25b8-148">Puslapį įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="f25b8-148">Check in the page, and publish it.</span></span>

<span data-ttu-id="f25b8-149">Norėdami padėti užtikrinti, kad antraštė būtų rodoma kiekviename puslapyje, kiekviename sukurtame svetainės puslapio šablone atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f25b8-149">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="f25b8-150">Numatytajame puslapyje į pagrindinės vietos antraštę įtraukite puslapio fragmentą, kuriame yra antraštės modulis.</span><span class="sxs-lookup"><span data-stu-id="f25b8-150">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="f25b8-151">Šabloną įrašykite.</span><span class="sxs-lookup"><span data-stu-id="f25b8-151">Save the template.</span></span> 
1. <span data-ttu-id="f25b8-152">Šabloną įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="f25b8-152">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f25b8-153">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f25b8-153">Additional resources</span></span>

[<span data-ttu-id="f25b8-154">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="f25b8-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f25b8-155">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="f25b8-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f25b8-156">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="f25b8-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f25b8-157">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="f25b8-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f25b8-158">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="f25b8-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f25b8-159">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="f25b8-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f25b8-160">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="f25b8-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f25b8-161">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="f25b8-161">Footer module</span></span>](author-footer-module.md)
