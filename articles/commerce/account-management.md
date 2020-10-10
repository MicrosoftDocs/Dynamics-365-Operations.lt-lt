---
title: Paskyros valdymo puslapiai ir moduliai
description: Šioje temoje aprašomi „Microsoft Dynamics 365 Commerce“ paskyros valdymo puslapiai ir moduliai.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0f963bcf65ae622522fe52fd59996c6ec0ecf17
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817163"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="fcfec-103">Paskyros valdymo puslapiai ir moduliai</span><span class="sxs-lookup"><span data-stu-id="fcfec-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fcfec-104">Šioje temoje aprašomi „Microsoft Dynamics 365 Commerce“ paskyros valdymo puslapiai ir moduliai.</span><span class="sxs-lookup"><span data-stu-id="fcfec-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fcfec-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="fcfec-105">Overview</span></span>

<span data-ttu-id="fcfec-106">Paskyros valdomos keliuose „Dynamics 365 Commerce“ puslapiuose, kuriuose valdoma su vartotoju susijusi informacija.</span><span class="sxs-lookup"><span data-stu-id="fcfec-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="fcfec-107">Paskyros valdymo puslapiai apima paskyros valdymo nukreipimo puslapį, vartotojo profilio puslapį, vartotojo adresų puslapį, užsakymų retrospektyvos puslapį, išsamios užsakymų informacijos puslapį, lojalumo puslapį ir pageidavimų sąrašo puslapį.</span><span class="sxs-lookup"><span data-stu-id="fcfec-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="fcfec-108">Paskyros valdymo nukreipimo puslapis</span><span class="sxs-lookup"><span data-stu-id="fcfec-108">Account management landing page</span></span>

<span data-ttu-id="fcfec-109">Paskyros valdymo nukreipimo puslapyje naudojami tolesni moduliai.</span><span class="sxs-lookup"><span data-stu-id="fcfec-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="fcfec-110">**Konteineris** – visų paskyros valdymo nukreipimo puslapio modulius reikia patalpinti į konteinerį.</span><span class="sxs-lookup"><span data-stu-id="fcfec-110">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="fcfec-111">**Paskyros pasisveikinimo plytelė** – naudojant šį modulį, paskyros valdymo puslapyje pateikiamas pasisveikinimo pranešimas.</span><span class="sxs-lookup"><span data-stu-id="fcfec-111">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="fcfec-112">Jame yra antraštės ypatybių.</span><span class="sxs-lookup"><span data-stu-id="fcfec-112">It includes properties for the heading.</span></span>
- <span data-ttu-id="fcfec-113">**Paskyros bendroji plytelė** – šis modulis gali būti naudojamas, norint teikti antraštes ir saitus į paskyrų valdymo puslapius, pavyzdžiui, puslapiai „Užsakymo istorija“ arba „Mano profilis“.</span><span class="sxs-lookup"><span data-stu-id="fcfec-113">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="fcfec-114">Bendrosios plytelės modulį galima naudoti bet kurio puslapio plytelei konfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="fcfec-114">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="fcfec-115">„Fabrikam“ šis modulis naudojamas puslapių „Užsakymo istorija“ ir „Mano profilis“ saitams paskyros valdymo nukreipimo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="fcfec-115">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="fcfec-116">**Paskyros pageidavimų sąrašo plytelė** – naudojant šį modulį pateikiama kliento pageidavimų sąraše esančių prekių suvestinė.</span><span class="sxs-lookup"><span data-stu-id="fcfec-116">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="fcfec-117">Pavyzdžiui, jame gali būti nurodyta „Pageidavimų sąraše turite 10 prekių.“</span><span class="sxs-lookup"><span data-stu-id="fcfec-117">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="fcfec-118">Jame pateikiamos antraštės ir „Peržiūrėti išsamią informaciją“ ypatybės.</span><span class="sxs-lookup"><span data-stu-id="fcfec-118">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="fcfec-119">Saitą „Peržiūrėti išsamią informaciją“ reikia sukonfigūruoti taip, kad jis nukreiptų į pageidavimų sąrašo puslapį.</span><span class="sxs-lookup"><span data-stu-id="fcfec-119">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="fcfec-120">**Paskyros adresų plytelė** – naudojant šį modulį pateikiama vartotojo adresų suvestinė.</span><span class="sxs-lookup"><span data-stu-id="fcfec-120">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="fcfec-121">Pavyzdžiui, jame gali būti nurodyta „Į jūsų paskyrą įtraukti 2 adresai.“</span><span class="sxs-lookup"><span data-stu-id="fcfec-121">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="fcfec-122">Jame pateikiamos antraštės ir „Peržiūrėti išsamią informaciją“ ypatybės.</span><span class="sxs-lookup"><span data-stu-id="fcfec-122">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="fcfec-123">Saitą „Peržiūrėti išsamią informaciją“ reikia sukonfigūruoti taip, kad jis nukreiptų į vartotojo adresų puslapį.</span><span class="sxs-lookup"><span data-stu-id="fcfec-123">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="fcfec-124">**Paskyros lojalumo plytelė** – naudojant šį modulį rodoma informacija apie lojalumo programą ir pateikiamas saitas su šia informacija.</span><span class="sxs-lookup"><span data-stu-id="fcfec-124">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="fcfec-125">Ši plytelė turi dvi būsenas: viena būsena nurodo saitus, skirtus prisijungti prie lojalumo programos, jei vartotojas dar nėra narys.</span><span class="sxs-lookup"><span data-stu-id="fcfec-125">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="fcfec-126">Kita būsena rodo saitus, kad būtų galima peržiūrėti lojalumo informacijos puslapį, kai vartotojas jau yra narys.</span><span class="sxs-lookup"><span data-stu-id="fcfec-126">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="fcfec-127">Ypatybėse yra antraštė, „Prisijungimo“ saitas ir „Peržiūrėti lojalumą“ saitas.</span><span class="sxs-lookup"><span data-stu-id="fcfec-127">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="fcfec-128">Saitą „Peržiūrėti lojalumą“ reikia sukonfigūruoti taip, kad jis nukreiptų į lojalumo puslapį.</span><span class="sxs-lookup"><span data-stu-id="fcfec-128">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="fcfec-129">Saitą „Prisijungti“ reikia sukonfigūruoti taip, kad jis nukreiptų į puslapį, kuriame vartotojai galėtų prisijungti prie lojalumo programos.</span><span class="sxs-lookup"><span data-stu-id="fcfec-129">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="fcfec-130">Užsakymų retrospektyvos puslapis</span><span class="sxs-lookup"><span data-stu-id="fcfec-130">Order history page</span></span>

<span data-ttu-id="fcfec-131">Užsakymų retrospektyvos puslapyje naudojant užsakymų retrospektyvos modulį rodomi visi vėliausi vartotojo pateikti užsakymai.</span><span class="sxs-lookup"><span data-stu-id="fcfec-131">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="fcfec-132">Užsakymo informacijos puslapis</span><span class="sxs-lookup"><span data-stu-id="fcfec-132">Order details page</span></span>

<span data-ttu-id="fcfec-133">Išsamios užsakymų informacijos puslapyje pateikiama išsami informacija apie kiekvieną užsakymą, o jis pasiekiamas užsakymų retrospektyvos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="fcfec-133">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="fcfec-134">Jame naudojamas išsamios užsakymų informacijos modulis, kuriam išsamiai užsakymų informacijai gauti reikalingas pardavimo ID arba operacijos ID.</span><span class="sxs-lookup"><span data-stu-id="fcfec-134">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="fcfec-135">Vartotojo profilio puslapis</span><span class="sxs-lookup"><span data-stu-id="fcfec-135">User profile page</span></span>

<span data-ttu-id="fcfec-136">Vartotojo profilio puslapyje rodoma išsami vartotojo paskyros informacija, pvz., vartotojo vardas ir el. pašto adresas.</span><span class="sxs-lookup"><span data-stu-id="fcfec-136">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="fcfec-137">Jis naudoja vartotojo profilio išsamią informaciją ir vartotojo profilio redagavimo modulius.</span><span class="sxs-lookup"><span data-stu-id="fcfec-137">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="fcfec-138">Nors el. pašto adreso pašalinti negalima, jį galima redaguoti.</span><span class="sxs-lookup"><span data-stu-id="fcfec-138">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="fcfec-139">Vartotojo profilio puslapyje taip pat rodomos vartotojo nuostatos, kurias naudodamas vartotojas gali sutikti arba atsisakyti naudoti tam tikras funkcijas, pvz., rekomendacijų sąrašų personalizavimo funkciją.</span><span class="sxs-lookup"><span data-stu-id="fcfec-139">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="fcfec-140">Vartotojo adresų puslapis</span><span class="sxs-lookup"><span data-stu-id="fcfec-140">User address page</span></span>

<span data-ttu-id="fcfec-141">Vartotojo adresų puslapyje rodomas adresų, susietų su vartotojo paskyra, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="fcfec-141">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="fcfec-142">Vartotojas šiuos adresus pateikė užbaigdamas pirkimą arba įtraukė tiesiogiai šiame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="fcfec-142">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="fcfec-143">Puslapyje adresai įtraukiami ir redaguojami, pagrindinis adresas nustatomas, o esami adresai rodomi naudojant vartotojo adresų modulį.</span><span class="sxs-lookup"><span data-stu-id="fcfec-143">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="fcfec-144">Pageidavimų sąrašo puslapis</span><span class="sxs-lookup"><span data-stu-id="fcfec-144">Wish list page</span></span>

<span data-ttu-id="fcfec-145">Pageidavimų sąrašo puslapyje rodomos prekės, įtrauktos į kliento pageidavimų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="fcfec-145">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="fcfec-146">Jame pageidavimų sąrašo prekės rodomos naudojant pageidavimų sąrašo modulį.</span><span class="sxs-lookup"><span data-stu-id="fcfec-146">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="fcfec-147">Lojalumo puslapis</span><span class="sxs-lookup"><span data-stu-id="fcfec-147">Loyalty page</span></span>

<span data-ttu-id="fcfec-148">Lojalumo puslapyje klientai gali peržiūrėti savo lojalumo išsamią informaciją, jei jie jau yra lojalumo programos nariai.</span><span class="sxs-lookup"><span data-stu-id="fcfec-148">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="fcfec-149">Jie taip pat gali peržiūrėti taškus, kuriuos uždirbo ir panaudojo atlikdami vėliausias operacijas.</span><span class="sxs-lookup"><span data-stu-id="fcfec-149">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="fcfec-150">Puslapis naudoja lojalumo išsamios informacijos modulį, kad parodytų lojalumo išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="fcfec-150">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="fcfec-151">Norint prisijungti prie lojalumo programos, rinkodaros puslapį galima sukurti naudojant lojalumo prisijungimą ir lojalumo sąlygų modulius.</span><span class="sxs-lookup"><span data-stu-id="fcfec-151">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="fcfec-152">Jei vartotojas nėra lojalumo programos narys, šie moduliai įgalins vartotoją prisijungti.</span><span class="sxs-lookup"><span data-stu-id="fcfec-152">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fcfec-153">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="fcfec-153">Additional resources</span></span>

[<span data-ttu-id="fcfec-154">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="fcfec-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fcfec-155">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="fcfec-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="fcfec-156">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="fcfec-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="fcfec-157">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="fcfec-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="fcfec-158">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="fcfec-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fcfec-159">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="fcfec-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="fcfec-160">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="fcfec-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="fcfec-161">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="fcfec-161">Footer module</span></span>](author-footer-module.md)
