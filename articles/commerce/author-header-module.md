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
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885483"
---
# <a name="header-module"></a><span data-ttu-id="1efbe-103">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="1efbe-103">Header module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="1efbe-104">Šioje temoje aprašomi antraštės moduliai ir tai, kaip juos kurti programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="1efbe-104">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1efbe-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="1efbe-105">Overview</span></span>

<span data-ttu-id="1efbe-106">Antraštės modulis yra specialus konteineris, kuriame laikomi visi moduliai, kurie bus rodomi puslapio antraštėje.</span><span class="sxs-lookup"><span data-stu-id="1efbe-106">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="1efbe-107">Pavyzdžiui, jame gali būti svetainės logotipas, saitai su naršymo hierarchija, saitai su kitais svetainės puslapiais ir ieškos juosta.</span><span class="sxs-lookup"><span data-stu-id="1efbe-107">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="1efbe-108">Antraštės modulis automatiškai optimizuojamas įrenginiui, kuriame peržiūrima svetainė (t. y., stacionariam įrenginiui arba mobiliajam įrenginiui).</span><span class="sxs-lookup"><span data-stu-id="1efbe-108">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="1efbe-109">Pavyzdžiui, mobiliajame įrenginyje naršymo juosta sutraukiama į mygtuką **Meniu** (kuris kartais vadinamas *mėsainio stiliaus meniu*).</span><span class="sxs-lookup"><span data-stu-id="1efbe-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="1efbe-110">Antraštės ypatybės</span><span class="sxs-lookup"><span data-stu-id="1efbe-110">Properties of a header</span></span>

<span data-ttu-id="1efbe-111">Kaip ir bendrieji konteineriai, antraštės modulis palaiko **antraštės** ir **pločio** ypatybes.</span><span class="sxs-lookup"><span data-stu-id="1efbe-111">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="1efbe-112">Antraštės modulyje yra kelios vietos.</span><span class="sxs-lookup"><span data-stu-id="1efbe-112">A header module has multiple slots.</span></span> <span data-ttu-id="1efbe-113">Pavyzdžiui, yra vietos informaciniam pranešimui, naršymo meniu, logotipui, ieškos juostai, krepšelio piktogramai, pageidavimų sąrašo piktogramai ir paskyros informacijai.</span><span class="sxs-lookup"><span data-stu-id="1efbe-113">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="1efbe-114">Kiekviena vieta palaiko konkretų modulių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="1efbe-114">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="1efbe-115">Moduliai, esantys antraštės modulyje</span><span class="sxs-lookup"><span data-stu-id="1efbe-115">Modules that are available in a header module</span></span>

<span data-ttu-id="1efbe-116">Antraštės modulyje galima naudoti tolesnius modulius.</span><span class="sxs-lookup"><span data-stu-id="1efbe-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="1efbe-117">**Naršymo meniu** – naršymo meniu vaizduojama kanalo naršymo hierarchija ir kiti statiniai naršymo saitai.</span><span class="sxs-lookup"><span data-stu-id="1efbe-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="1efbe-118">Kanalo naršymo hierarchiją galima konfigūruoti programoje „Dynamics 365 Retail“.</span><span class="sxs-lookup"><span data-stu-id="1efbe-118">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="1efbe-119">Sukonfigūruoti elementai tada rodomi kaip antraštės naršymo elementai.</span><span class="sxs-lookup"><span data-stu-id="1efbe-119">Configured items then appear as header navigation.</span></span> <span data-ttu-id="1efbe-120">Be to, galima sukonfigūruoti statinius naršymo saitus ir pateikti santykinius saitus su kitais el. prekybos svetainės puslapiais.</span><span class="sxs-lookup"><span data-stu-id="1efbe-120">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="1efbe-121">Pačią antraštę galima lygiuoti kairėje, dešinėje arba centre.</span><span class="sxs-lookup"><span data-stu-id="1efbe-121">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="1efbe-122">**Krepšelio piktograma** – krepšelio piktograma yra speciali piktograma, vaizduojanti krepšelį.</span><span class="sxs-lookup"><span data-stu-id="1efbe-122">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="1efbe-123">Ji rodoma antraštėje ir nurodo krepšelyje esančių prekių skaičių.</span><span class="sxs-lookup"><span data-stu-id="1efbe-123">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="1efbe-124">Prie krepšelio piktogramos turėtų būti saitas su krepšelio puslapiu, kad naudodami piktogramą klientai galėtų būti nukreipiami į krepšelio puslapį.</span><span class="sxs-lookup"><span data-stu-id="1efbe-124">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="1efbe-125">**Pageidavimų sąrašo piktograma** – pageidavimų sąrašo piktograma rodoma antraštėje ir nurodo prekių, įtrauktų į kliento pageidavimų sąrašą, skaičių.</span><span class="sxs-lookup"><span data-stu-id="1efbe-125">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="1efbe-126">Prie šios piktogramos turėtų būti saitas su pageidavimų sąrašo puslapiu, kad naudodami piktogramą klientai galėtų būti nukreipiami į pageidavimų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="1efbe-126">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="1efbe-127">**Prisijungimo modulis** – antraštėje rodomas prisijungimo modulis.</span><span class="sxs-lookup"><span data-stu-id="1efbe-127">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="1efbe-128">Jį naudodami klientai gali prisijungti prie savo paskyros arba registruotis paskyrai.</span><span class="sxs-lookup"><span data-stu-id="1efbe-128">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="1efbe-129">Jei klientas jau prisijungęs, modulį galima sukonfigūruoti taip, kad jame būtų rodomi saitai su paskyros puslapiu, užsakymų retrospektyvos puslapiu ar kitu puslapiu.</span><span class="sxs-lookup"><span data-stu-id="1efbe-129">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="1efbe-130">**Logotipo modulis** – šiame modulyje rodomas logotipas, vaizduojantis pardavėją ir prekės ženklą.</span><span class="sxs-lookup"><span data-stu-id="1efbe-130">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="1efbe-131">Tai yra vaizdas su saitu.</span><span class="sxs-lookup"><span data-stu-id="1efbe-131">It's an image that has a link.</span></span> <span data-ttu-id="1efbe-132">Saitas paprastai sukonfigūruotas taip, kad nukreiptų į pagrindinį puslapį, todėl klientai gali greitai grįžti į pagrindinį puslapį iš bet kurio svetainės puslapio.</span><span class="sxs-lookup"><span data-stu-id="1efbe-132">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="1efbe-133">**Įspėjimas** – antraštėje rodomas įspėjimas, kurį naudojant rodomas įdėtasis pranešimas, taikomas visiems svetainės puslapiams.</span><span class="sxs-lookup"><span data-stu-id="1efbe-133">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="1efbe-134">Pavyzdžiui, įspėjime gali būti rodomas pranešimas, pvz., „Metinis išpardavimas baigiasi už 2 dienų“.</span><span class="sxs-lookup"><span data-stu-id="1efbe-134">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="1efbe-135">**Ieškos juosta** – ieškos juostoje vartotojai gali įvesti ieškos terminus, kad galėtų ieškoti produktų.</span><span class="sxs-lookup"><span data-stu-id="1efbe-135">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="1efbe-136">Modulyje reikia sukonfigūruoti ieškos rezultatų puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="1efbe-136">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="1efbe-137">Galima sukonfigūruoti užklausos eilutės parametrą (numatytoji reikšmė yra **q**).</span><span class="sxs-lookup"><span data-stu-id="1efbe-137">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="1efbe-138">Ieškos juostoje yra automatinio siūlymo vieta, kurioje reikia įtraukti automatinio siūlymo modulį.</span><span class="sxs-lookup"><span data-stu-id="1efbe-138">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="1efbe-139">**Automatinis siūlymas** – automatinio siūlymo modulyje rodomi automatiškai pasiūlyti rezultatai.</span><span class="sxs-lookup"><span data-stu-id="1efbe-139">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="1efbe-140">Šie rezultatai gali būti raktažodžiai, produktai ar kategorijos, kur randamas ieškos terminas.</span><span class="sxs-lookup"><span data-stu-id="1efbe-140">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="1efbe-141">Kurti antraštės modulį</span><span class="sxs-lookup"><span data-stu-id="1efbe-141">Create a header module</span></span>

<span data-ttu-id="1efbe-142">Norėdami sukurti antraštės modulį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1efbe-142">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="1efbe-143">Sukurkite puslapio fragmentą, kuriame yra antraštės modulis.</span><span class="sxs-lookup"><span data-stu-id="1efbe-143">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="1efbe-144">Į antraštės modulio vietas įtraukite modulių.</span><span class="sxs-lookup"><span data-stu-id="1efbe-144">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="1efbe-145">Atnaujinkite kiekvieno modulio parametrus.</span><span class="sxs-lookup"><span data-stu-id="1efbe-145">Update the settings for each module.</span></span>
1. <span data-ttu-id="1efbe-146">Puslapio fragmentą įrašykite.</span><span class="sxs-lookup"><span data-stu-id="1efbe-146">Save the page fragment.</span></span> 
1. <span data-ttu-id="1efbe-147">Puslapį įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="1efbe-147">Check in the page, and publish it.</span></span>

<span data-ttu-id="1efbe-148">Norėdami padėti užtikrinti, kad antraštė būtų rodoma kiekviename puslapyje, kiekviename sukurtame svetainės puslapio šablone atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1efbe-148">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="1efbe-149">Numatytajame puslapyje į pagrindinės vietos antraštę įtraukite puslapio fragmentą, kuriame yra antraštės modulis.</span><span class="sxs-lookup"><span data-stu-id="1efbe-149">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="1efbe-150">Šabloną įrašykite.</span><span class="sxs-lookup"><span data-stu-id="1efbe-150">Save the template.</span></span> 
1. <span data-ttu-id="1efbe-151">Šabloną įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="1efbe-151">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1efbe-152">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1efbe-152">Additional resources</span></span>

[<span data-ttu-id="1efbe-153">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="1efbe-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1efbe-154">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="1efbe-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="1efbe-155">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="1efbe-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="1efbe-156">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="1efbe-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1efbe-157">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="1efbe-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="1efbe-158">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="1efbe-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="1efbe-159">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="1efbe-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="1efbe-160">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="1efbe-160">Footer module</span></span>](author-footer-module.md)
