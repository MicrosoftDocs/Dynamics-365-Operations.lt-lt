---
title: Paskyros valdymo puslapiai ir moduliai
description: Šioje temoje aprašomi „Microsoft Dynamics 365 Commerce“ paskyros valdymo puslapiai ir moduliai.
author: v-chgri
manager: annbe
ms.date: 12/02/2019
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
ms.openlocfilehash: f9fc3731cd9d21294b0161e1d419f255096d7790
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885814"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="de46b-103">Paskyros valdymo puslapiai ir moduliai</span><span class="sxs-lookup"><span data-stu-id="de46b-103">Account management pages and modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="de46b-104">Šioje temoje aprašomi „Microsoft Dynamics 365 Commerce“ paskyros valdymo puslapiai ir moduliai.</span><span class="sxs-lookup"><span data-stu-id="de46b-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="de46b-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="de46b-105">Overview</span></span>

<span data-ttu-id="de46b-106">Paskyros valdomos keliuose „Dynamics 365 Commerce“ puslapiuose, kuriuose valdoma su vartotoju susijusi informacija.</span><span class="sxs-lookup"><span data-stu-id="de46b-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="de46b-107">Paskyros valdymo puslapiai apima paskyros valdymo nukreipimo puslapį, vartotojo profilio puslapį, vartotojo adresų puslapį, užsakymų retrospektyvos puslapį, išsamios užsakymų informacijos puslapį, lojalumo puslapį ir pageidavimų sąrašo puslapį.</span><span class="sxs-lookup"><span data-stu-id="de46b-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="de46b-108">Paskyros valdymo nukreipimo puslapis</span><span class="sxs-lookup"><span data-stu-id="de46b-108">Account management landing page</span></span>

<span data-ttu-id="de46b-109">Paskyros valdymo nukreipimo puslapyje naudojami tolesni moduliai.</span><span class="sxs-lookup"><span data-stu-id="de46b-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="de46b-110">**Turinio išdėstymas** – šis modulis yra konteinerio modulis, kuriame laikomi visi paskyros valdymo nukreipimo puslapio moduliai.</span><span class="sxs-lookup"><span data-stu-id="de46b-110">**Content placement** – This module is a container module that holds all the modules on the account management landing page.</span></span>
- <span data-ttu-id="de46b-111">**Paskyros pasisveikinimo elementas** – naudojant šį modulį, paskyros valdymo puslapyje pateikiamas pasisveikinimo pranešimas.</span><span class="sxs-lookup"><span data-stu-id="de46b-111">**Account welcome item** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="de46b-112">Jame pateikiamos antraštės ir plytelių dydžio ypatybės.</span><span class="sxs-lookup"><span data-stu-id="de46b-112">It includes properties for the heading and the tile size.</span></span> <span data-ttu-id="de46b-113">Ypatybė **Plytelių dydis** apibrėžia turinio išdėstymo modulio plotį.</span><span class="sxs-lookup"><span data-stu-id="de46b-113">The **Tile size** property defines the width of the module in the content placement module.</span></span> <span data-ttu-id="de46b-114">Reikšmių intervalas yra nuo **1** iki **12** – **12** reiškia visą turinio išdėstymo konteinerio plotį.</span><span class="sxs-lookup"><span data-stu-id="de46b-114">Values range from **1** through **12**, where **12** represents the full width of the content placement container.</span></span>
- <span data-ttu-id="de46b-115">**Paskyros užsakymų pateikimo elementas** – naudojant šį modulį pateikiama vartotojo paskyros pateiktų užsakymų skaičiaus suvestinė.</span><span class="sxs-lookup"><span data-stu-id="de46b-115">**Account order placement item** – This module is used to provide a summary of the number of orders that have been placed by the user account.</span></span> <span data-ttu-id="de46b-116">Jame pateikiamos antraštės, plytelių dydžio ir saito „peržiūrėti išsamią informaciją“ ypatybės.</span><span class="sxs-lookup"><span data-stu-id="de46b-116">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="de46b-117">Saitą „peržiūrėti išsamią informaciją“ reikia sukonfigūruoti taip, kad jis nukreiptų į užsakymų retrospektyvos puslapį.</span><span class="sxs-lookup"><span data-stu-id="de46b-117">The "view details" link should be configured to redirect to the order history page.</span></span>
- <span data-ttu-id="de46b-118">**Paskyros profilio išdėstymo elementas** – naudojant šį modulį pateikiama vartotojo profilio suvestinė.</span><span class="sxs-lookup"><span data-stu-id="de46b-118">**Account profile placement item** – This module is used to provide a summary of the user profile.</span></span> <span data-ttu-id="de46b-119">Jame pateikiamos antraštės, plytelių dydžio ir saito „peržiūrėti išsamią informaciją“ ypatybės.</span><span class="sxs-lookup"><span data-stu-id="de46b-119">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="de46b-120">Saitą „peržiūrėti išsamią informaciją“ reikia sukonfigūruoti taip, kad jis nukreiptų į vartotojo profilio puslapį.</span><span class="sxs-lookup"><span data-stu-id="de46b-120">The "view details" link should be configured to redirect to the user profile page.</span></span>
- <span data-ttu-id="de46b-121">**Paskyros pageidavimų sąrašo elementas** – naudojant šį modulį pateikiama kliento pageidavimų sąraše esančių prekių suvestinė.</span><span class="sxs-lookup"><span data-stu-id="de46b-121">**Account wishlist item** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="de46b-122">Pavyzdžiui, jame gali būti nurodyta „Pageidavimų sąraše turite 10 prekių.“</span><span class="sxs-lookup"><span data-stu-id="de46b-122">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="de46b-123">Jame pateikiamos antraštės, plytelių dydžio ir saito „peržiūrėti išsamią informaciją“ ypatybės.</span><span class="sxs-lookup"><span data-stu-id="de46b-123">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="de46b-124">Saitą „peržiūrėti išsamią informaciją“ reikia sukonfigūruoti taip, kad jis nukreiptų į pageidavimų sąrašo puslapį.</span><span class="sxs-lookup"><span data-stu-id="de46b-124">The "view details" link should be configured to redirect to the wish list page.</span></span>
- <span data-ttu-id="de46b-125">**Paskyros adresų elementas** – naudojant šį modulį pateikiama vartotojo adresų suvestinė.</span><span class="sxs-lookup"><span data-stu-id="de46b-125">**Account address item** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="de46b-126">Pavyzdžiui, jame gali būti nurodyta „Į jūsų paskyrą įtraukti 2 adresai.“</span><span class="sxs-lookup"><span data-stu-id="de46b-126">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="de46b-127">Jame pateikiamos antraštės, plytelių dydžio ir saito „peržiūrėti išsamią informaciją“ ypatybės.</span><span class="sxs-lookup"><span data-stu-id="de46b-127">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="de46b-128">Saitą „peržiūrėti išsamią informaciją“ reikia sukonfigūruoti taip, kad jis nukreiptų į vartotojo adresų puslapį.</span><span class="sxs-lookup"><span data-stu-id="de46b-128">The "view details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="de46b-129">**Paskyros lojalumo elementas** – naudojant šį modulį rodoma informacija apie lojalumo programą ir pateikiamas saitas su šia informacija.</span><span class="sxs-lookup"><span data-stu-id="de46b-129">**Account loyalty item** – This module is used to show and link to loyalty program information.</span></span> <span data-ttu-id="de46b-130">Jame pateikiamos antraštės, plytelių dydžio, saito „peržiūrėti išsamią informaciją“ ir saito „tapkite nariu“ ypatybės.</span><span class="sxs-lookup"><span data-stu-id="de46b-130">It includes properties for the heading, the tile size, the "view details" link, and the "become a member" link.</span></span> <span data-ttu-id="de46b-131">Saitą „peržiūrėti išsamią informaciją“ reikia sukonfigūruoti taip, kad jis nukreiptų į lojalumo puslapį.</span><span class="sxs-lookup"><span data-stu-id="de46b-131">The "view details" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="de46b-132">Saitą „tapkite nariu“ reikia sukonfigūruoti taip, kad jis nukreiptų į puslapį, kuriame vartotojai galėtų prisijungti prie lojalumo programos.</span><span class="sxs-lookup"><span data-stu-id="de46b-132">The "become a member" link should be configured to redirect to a page where users can join the loyalty program.</span></span>

### <a name="order-history-page"></a><span data-ttu-id="de46b-133">Užsakymų retrospektyvos puslapis</span><span class="sxs-lookup"><span data-stu-id="de46b-133">Order history page</span></span>

<span data-ttu-id="de46b-134">Užsakymų retrospektyvos puslapyje naudojant užsakymų retrospektyvos modulį rodomi visi vėliausi vartotojo pateikti užsakymai.</span><span class="sxs-lookup"><span data-stu-id="de46b-134">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="de46b-135">Užsakymo informacijos puslapis</span><span class="sxs-lookup"><span data-stu-id="de46b-135">Order details page</span></span>

<span data-ttu-id="de46b-136">Išsamios užsakymų informacijos puslapyje pateikiama išsami informacija apie kiekvieną užsakymą, o jis pasiekiamas užsakymų retrospektyvos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="de46b-136">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="de46b-137">Jame naudojamas išsamios užsakymų informacijos modulis, kuriam išsamiai užsakymų informacijai gauti reikalingas pardavimo ID arba operacijos ID.</span><span class="sxs-lookup"><span data-stu-id="de46b-137">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="de46b-138">Vartotojo profilio puslapis</span><span class="sxs-lookup"><span data-stu-id="de46b-138">User profile page</span></span>

<span data-ttu-id="de46b-139">Vartotojo profilio puslapyje rodoma išsami vartotojo paskyros informacija, pvz., vartotojo vardas ir el. pašto adresas.</span><span class="sxs-lookup"><span data-stu-id="de46b-139">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="de46b-140">Jame naudojamas vartotojo profilio modulis.</span><span class="sxs-lookup"><span data-stu-id="de46b-140">It uses the user profile module.</span></span> <span data-ttu-id="de46b-141">Nors el. pašto adreso pašalinti negalima, jį galima redaguoti.</span><span class="sxs-lookup"><span data-stu-id="de46b-141">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="de46b-142">Vartotojo profilio puslapyje taip pat rodomos vartotojo nuostatos, kurias naudodamas vartotojas gali sutikti arba atsisakyti naudoti tam tikras funkcijas, pvz., rekomendacijų sąrašų personalizavimo funkciją.</span><span class="sxs-lookup"><span data-stu-id="de46b-142">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="de46b-143">Vartotojo adresų puslapis</span><span class="sxs-lookup"><span data-stu-id="de46b-143">User address page</span></span>

<span data-ttu-id="de46b-144">Vartotojo adresų puslapyje rodomas adresų, susietų su vartotojo paskyra, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="de46b-144">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="de46b-145">Vartotojas šiuos adresus pateikė užbaigdamas pirkimą arba įtraukė tiesiogiai šiame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="de46b-145">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="de46b-146">Puslapyje adresai įtraukiami ir redaguojami, pagrindinis adresas nustatomas, o esami adresai rodomi naudojant vartotojo adresų modulį.</span><span class="sxs-lookup"><span data-stu-id="de46b-146">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="de46b-147">Pageidavimų sąrašo puslapis</span><span class="sxs-lookup"><span data-stu-id="de46b-147">Wish list page</span></span>

<span data-ttu-id="de46b-148">Pageidavimų sąrašo puslapyje rodomos prekės, įtrauktos į kliento pageidavimų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="de46b-148">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="de46b-149">Jame pageidavimų sąrašo prekės rodomos naudojant pageidavimų sąrašo modulį.</span><span class="sxs-lookup"><span data-stu-id="de46b-149">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="de46b-150">Lojalumo puslapis</span><span class="sxs-lookup"><span data-stu-id="de46b-150">Loyalty page</span></span>

<span data-ttu-id="de46b-151">Lojalumo puslapyje klientai gali prisijungti prie lojalumo programos arba, jei jie jau yra lojalumo programos nariai, peržiūrėti asmeninę išsamią programos informaciją.</span><span class="sxs-lookup"><span data-stu-id="de46b-151">The loyalty page lets customers join a loyalty program or, if they are already loyalty program members, view their program details.</span></span> <span data-ttu-id="de46b-152">Jie taip pat gali peržiūrėti taškus, kuriuos uždirbo ir panaudojo atlikdami vėliausias operacijas.</span><span class="sxs-lookup"><span data-stu-id="de46b-152">They can also view the points that they have earned and redeemed in recent transactions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="de46b-153">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="de46b-153">Additional resources</span></span>

[<span data-ttu-id="de46b-154">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="de46b-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="de46b-155">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="de46b-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="de46b-156">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="de46b-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="de46b-157">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="de46b-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="de46b-158">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="de46b-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="de46b-159">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="de46b-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="de46b-160">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="de46b-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="de46b-161">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="de46b-161">Footer module</span></span>](author-footer-module.md)
