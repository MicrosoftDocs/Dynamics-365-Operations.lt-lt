---
title: Sąskaitos valdymo puslapiai ir moduliai
description: Šioje temoje aprašomi „Microsoft Dynamics 365 Commerce“ paskyros valdymo puslapiai ir moduliai.
author: v-chgri
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: df4959a61f1b2948c62a558523a848ff8b2fe0a8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796299"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="f1bb1-103">Sąskaitos valdymo puslapiai ir moduliai</span><span class="sxs-lookup"><span data-stu-id="f1bb1-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f1bb1-104">Šioje temoje aprašomi „Microsoft Dynamics 365 Commerce“ paskyros valdymo puslapiai ir moduliai.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f1bb1-105">Paskyros valdomos keliuose „Dynamics 365 Commerce“ puslapiuose, kuriuose valdoma su vartotoju susijusi informacija.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-105">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="f1bb1-106">Paskyros valdymo puslapiai apima paskyros valdymo nukreipimo puslapį, vartotojo profilio puslapį, vartotojo adresų puslapį, užsakymų retrospektyvos puslapį, išsamios užsakymų informacijos puslapį, lojalumo puslapį ir pageidavimų sąrašo puslapį.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-106">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="f1bb1-107">Paskyros valdymo nukreipimo puslapis</span><span class="sxs-lookup"><span data-stu-id="f1bb1-107">Account management landing page</span></span>

<span data-ttu-id="f1bb1-108">Paskyros valdymo nukreipimo puslapyje naudojami tolesni moduliai.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-108">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="f1bb1-109">**Konteineris** – visų paskyros valdymo nukreipimo puslapio modulius reikia patalpinti į konteinerį.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-109">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="f1bb1-110">**Paskyros pasisveikinimo plytelė** – naudojant šį modulį, paskyros valdymo puslapyje pateikiamas pasisveikinimo pranešimas.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-110">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="f1bb1-111">Jame yra antraštės ypatybių.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-111">It includes properties for the heading.</span></span>
- <span data-ttu-id="f1bb1-112">**Paskyros bendroji plytelė** – šis modulis gali būti naudojamas, norint teikti antraštes ir saitus į paskyrų valdymo puslapius, pavyzdžiui, puslapiai „Užsakymo istorija“ arba „Mano profilis“.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-112">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="f1bb1-113">Bendrosios plytelės modulį galima naudoti bet kurio puslapio plytelei konfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-113">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="f1bb1-114">„Fabrikam“ šis modulis naudojamas puslapių „Užsakymo istorija“ ir „Mano profilis“ saitams paskyros valdymo nukreipimo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-114">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="f1bb1-115">**Paskyros pageidavimų sąrašo plytelė** – naudojant šį modulį pateikiama kliento pageidavimų sąraše esančių prekių suvestinė.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-115">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="f1bb1-116">Pavyzdžiui, jame gali būti nurodyta „Pageidavimų sąraše turite 10 prekių.“</span><span class="sxs-lookup"><span data-stu-id="f1bb1-116">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="f1bb1-117">Jame pateikiamos antraštės ir „Peržiūrėti išsamią informaciją“ ypatybės.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-117">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="f1bb1-118">Saitą „Peržiūrėti išsamią informaciją“ reikia sukonfigūruoti taip, kad jis nukreiptų į pageidavimų sąrašo puslapį.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-118">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="f1bb1-119">**Paskyros adresų plytelė** – naudojant šį modulį pateikiama vartotojo adresų suvestinė.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-119">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="f1bb1-120">Pavyzdžiui, jame gali būti nurodyta „Į jūsų paskyrą įtraukti 2 adresai.“</span><span class="sxs-lookup"><span data-stu-id="f1bb1-120">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="f1bb1-121">Jame pateikiamos antraštės ir „Peržiūrėti išsamią informaciją“ ypatybės.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-121">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="f1bb1-122">Saitą „Peržiūrėti išsamią informaciją“ reikia sukonfigūruoti taip, kad jis nukreiptų į vartotojo adresų puslapį.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-122">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="f1bb1-123">**Paskyros lojalumo plytelė** – naudojant šį modulį rodoma informacija apie lojalumo programą ir pateikiamas saitas su šia informacija.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-123">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="f1bb1-124">Ši plytelė turi dvi būsenas: viena būsena nurodo saitus, skirtus prisijungti prie lojalumo programos, jeigu vartotojas dar nėra narys.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-124">This tile has two states: one state shows links to join a loyalty program if the user is not a member already.</span></span> <span data-ttu-id="f1bb1-125">Kita būsena rodo saitus, kad būtų galima peržiūrėti lojalumo informacijos puslapį, kai vartotojas jau yra narys.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-125">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="f1bb1-126">Ypatybėse yra antraštė, „Prisijungimo“ saitas ir „Peržiūrėti lojalumą“ saitas.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-126">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="f1bb1-127">Saitą „Peržiūrėti lojalumą“ reikia sukonfigūruoti taip, kad jis nukreiptų į lojalumo puslapį.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-127">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="f1bb1-128">Saitą „Prisijungti“ reikia sukonfigūruoti taip, kad jis nukreiptų į puslapį, kuriame vartotojai galėtų prisijungti prie lojalumo programos.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-128">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="f1bb1-129">Užsakymų retrospektyvos puslapis</span><span class="sxs-lookup"><span data-stu-id="f1bb1-129">Order history page</span></span>

<span data-ttu-id="f1bb1-130">Užsakymų retrospektyvos puslapyje naudojant užsakymų retrospektyvos modulį rodomi visi vėliausi vartotojo pateikti užsakymai.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-130">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="f1bb1-131">Užsakymo informacijos puslapis</span><span class="sxs-lookup"><span data-stu-id="f1bb1-131">Order details page</span></span>

<span data-ttu-id="f1bb1-132">Išsamios užsakymų informacijos puslapyje pateikiama išsami informacija apie kiekvieną užsakymą, o jis pasiekiamas užsakymų retrospektyvos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-132">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="f1bb1-133">Jame naudojamas išsamios užsakymų informacijos modulis, kuriam išsamiai užsakymų informacijai gauti reikalingas pardavimo ID arba operacijos ID.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-133">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="my-profile-page"></a><span data-ttu-id="f1bb1-134">Mano profilio puslapis</span><span class="sxs-lookup"><span data-stu-id="f1bb1-134">My profile page</span></span>

<span data-ttu-id="f1bb1-135">Puslapyje Mano profilis rodoma vartotojo abonento profilio informacija naudojant abonento profilio modulį.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-135">The My profile page shows the user's account profile details using the account profile module.</span></span> <span data-ttu-id="f1bb1-136">Puslapyje rodomas el. pašto adresas, susietas su vartotojo abonentu ir nustatytomis jo nuostatomis.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-136">The page shows the email address associated with the user's account, as well as preferences set up for the account.</span></span> <span data-ttu-id="f1bb1-137">Jei bus nustatyti pasirinktiniai kliento atributai, jie taip pat bus rodomi skyriuje „Papildoma informacija”.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-137">If setting up custom customer attributes, an "Additional Information" section will also display those attributes.</span></span> <span data-ttu-id="f1bb1-138">Vartotojai gali redaguoti savo vardą, nuostatas arba papildomą informaciją (jei yra).</span><span class="sxs-lookup"><span data-stu-id="f1bb1-138">Users can edit their name, preferences, or additional information (if available).</span></span>

### <a name="user-address-page"></a><span data-ttu-id="f1bb1-139">Vartotojo adresų puslapis</span><span class="sxs-lookup"><span data-stu-id="f1bb1-139">User address page</span></span>

<span data-ttu-id="f1bb1-140">Vartotojo adresų puslapyje rodomas adresų, susietų su vartotojo paskyra, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-140">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="f1bb1-141">Vartotojas šiuos adresus pateikė užbaigdamas pirkimą arba įtraukė tiesiogiai šiame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-141">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="f1bb1-142">Puslapyje adresai įtraukiami ir redaguojami, pagrindinis adresas nustatomas, o esami adresai rodomi naudojant vartotojo adresų modulį.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-142">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="f1bb1-143">Pageidavimų sąrašo puslapis</span><span class="sxs-lookup"><span data-stu-id="f1bb1-143">Wish list page</span></span>

<span data-ttu-id="f1bb1-144">Pageidavimų sąrašo puslapyje rodomos prekės, įtrauktos į kliento pageidavimų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-144">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="f1bb1-145">Jame pageidavimų sąrašo prekės rodomos naudojant pageidavimų sąrašo modulį.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-145">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="f1bb1-146">Lojalumo puslapis</span><span class="sxs-lookup"><span data-stu-id="f1bb1-146">Loyalty page</span></span>

<span data-ttu-id="f1bb1-147">Lojalumo puslapyje klientai gali peržiūrėti savo lojalumo išsamią informaciją, jei jie jau yra lojalumo programos nariai.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-147">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="f1bb1-148">Jie taip pat gali peržiūrėti taškus, kuriuos uždirbo ir panaudojo atlikdami vėliausias operacijas.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-148">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="f1bb1-149">Puslapis naudoja lojalumo išsamios informacijos modulį, kad parodytų lojalumo išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-149">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="f1bb1-150">Norint prisijungti prie lojalumo programos, rinkodaros puslapį galima sukurti naudojant lojalumo prisijungimą ir lojalumo sąlygų modulius.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-150">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="f1bb1-151">Jei vartotojas nėra lojalumo programos narys, šie moduliai įgalins vartotoją prisijungti.</span><span class="sxs-lookup"><span data-stu-id="f1bb1-151">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1bb1-152">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f1bb1-152">Additional resources</span></span>

[<span data-ttu-id="f1bb1-153">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="f1bb1-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f1bb1-154">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="f1bb1-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f1bb1-155">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="f1bb1-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f1bb1-156">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="f1bb1-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f1bb1-157">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="f1bb1-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f1bb1-158">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="f1bb1-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f1bb1-159">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="f1bb1-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f1bb1-160">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="f1bb1-160">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]