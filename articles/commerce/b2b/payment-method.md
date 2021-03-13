---
title: Konfigūruoti kliento sąskaitos mokėjimo metodą B2B el. komercijos saitams
description: Ši tema aprašo, kaip konfigūruoti kliento sąskaitos mokėjimo metodą verslo su verslu (B2B) el. komercijos saitams.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 754e2f83d6c8ff5d3698d98062e54bba7ccd9836
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035941"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a><span data-ttu-id="cf48f-103">Konfigūruoti kliento sąskaitos mokėjimo metodą B2B el. komercijos saitams</span><span class="sxs-lookup"><span data-stu-id="cf48f-103">Configure the customer account payment method for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cf48f-104">Ši tema aprašo, kaip konfigūruoti kliento sąskaitos mokėjimo metodą verslo su verslu (B2B) el. komercijos saitams.</span><span class="sxs-lookup"><span data-stu-id="cf48f-104">This topic describes how to configure the customer account payment method for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="cf48f-105">Mažmeniniai prekybininkai gali priimti įvairius mokėjimo tipus vietoje produktų ir paslaugų, kuriuos jie parduoda el. komercijos kanale.</span><span class="sxs-lookup"><span data-stu-id="cf48f-105">Retailers can accept various types of payment in exchange for the products and services that they sell in an e-commerce channel.</span></span> <span data-ttu-id="cf48f-106">Visi mokėjimo tipai, kuriuos mažmenininkas priima, turi būti konfigūruojami „Microsoft Dynamics 365 Commerce“ nustatant sistemą.</span><span class="sxs-lookup"><span data-stu-id="cf48f-106">Each payment type that a retailer accepts must be configured in Microsoft Dynamics 365 Commerce when the system is set up.</span></span> <span data-ttu-id="cf48f-107">Kliento sąskaitos (ar „sąskaitoje“) mokėjimo metodas turi būti palaikomas B2B el. komercijos saituose.</span><span class="sxs-lookup"><span data-stu-id="cf48f-107">The customer account (or "on account") payment method must be supported on B2B e-commerce sites.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="cf48f-108">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="cf48f-108">Prerequisites</span></span>

1. <span data-ttu-id="cf48f-109">Įtraukite kliento sąskaitos mokėjimo metodą į „Commerce“ būstinę.</span><span class="sxs-lookup"><span data-stu-id="cf48f-109">Add the customer account payment method in Commerce headquarters.</span></span>
2. <span data-ttu-id="cf48f-110">Susiekite kliento sąskaitos mokėjimo metodą su el. komercijos kanalu.</span><span class="sxs-lookup"><span data-stu-id="cf48f-110">Associate the customer account payment method with the e-commerce channel.</span></span>
3. <span data-ttu-id="cf48f-111">Įsitikinkite, kad **Leisti sąskaitoje** yra įjungtas klientui **Mažmeninė prekybą ir komercija \> Klientai \> Visi klientai \> Numatyti mokėjimai** „Commerce“ būstinėje.</span><span class="sxs-lookup"><span data-stu-id="cf48f-111">Make sure that **Allow on account** is enabled for the customer at **Retail and Commerce \> Customers \> All customers \> Payment defaults** in Commerce headquarters.</span></span> <span data-ttu-id="cf48f-112">Taip pat, įsitikinkite, kad **Kredito limito** parametrai yra nustatyti tinkamai klientams **Mažmeninė prekyba ir komercija \> Klientai \> Visi klientai \> Kreditas ir kolekcijos** „Commerce“ būstinėje.</span><span class="sxs-lookup"><span data-stu-id="cf48f-112">Also make sure that **Credit limit** parameters are set appropriately for the customer at **Retail and Commerce \> Customers \> All customers \> Credit and Collections** in Commerce headquarters.</span></span> 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a><span data-ttu-id="cf48f-113">Įjunkite kliento sąskaitos mokėjimo metodą „Commerce“ vietos kūrimo įrankyje</span><span class="sxs-lookup"><span data-stu-id="cf48f-113">Enable the customer account payment method in Commerce site builder</span></span> 

<span data-ttu-id="cf48f-114">Norėdami įjungti kliento sąskaitos mokėjimo metodą „Commerce“ saito kūrimo įrankyje, vadovaukitės šiais žingsniais.</span><span class="sxs-lookup"><span data-stu-id="cf48f-114">To enable the customer account payment method in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="cf48f-115">Eikite į **Saito nustatymai \> Plėtiniai**.</span><span class="sxs-lookup"><span data-stu-id="cf48f-115">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="cf48f-116">Nustatykite **Įjungti kliento sąskaitos mokėjimus** ypatybę į **Įjungti B2B klientams**.</span><span class="sxs-lookup"><span data-stu-id="cf48f-116">Set the **Enable customer account payments** property to **Enabled for B2B customers**.</span></span> 
1. <span data-ttu-id="cf48f-117">Pasirinkite **Įrašyti ir publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="cf48f-117">Select **Save and Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="cf48f-118">Nauji saito nustatymai įsigalioja tik atnaujinus app.settings.json failą.</span><span class="sxs-lookup"><span data-stu-id="cf48f-118">The new site settings take effect only after the app.settings.json file is updated.</span></span> <span data-ttu-id="cf48f-119">Dėl daugiau informacijos, žr. [SDK ir modulio bibliotekos naujinimai](../e-commerce-extensibility/sdk-updates.md).</span><span class="sxs-lookup"><span data-stu-id="cf48f-119">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md).</span></span>

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a><span data-ttu-id="cf48f-120">Įjunkite kliento sąskaitos mokėjimo metodą išsiregistravimo puslapyje B2B el. komercijos saite</span><span class="sxs-lookup"><span data-stu-id="cf48f-120">Enable the customer account payment method on the checkout page for the B2B e-commerce site</span></span>

<span data-ttu-id="cf48f-121">Norėdami įjungti kliento sąskaitos mokėjimo metodą išsiregistravimo puslapyje B2B el. komercijos saite, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="cf48f-121">To enable the customer account payment method on the checkout page for the B2B e-commerce site, follow these steps.</span></span>

1. <span data-ttu-id="cf48f-122">„Commerce“ saito kūrimo įrankyje, suraskite ir redaguokite išsiregistravimo puslapį ar fragmentą, kuriame yra išsiregistravimo modulis B2B el. komercijos saite.</span><span class="sxs-lookup"><span data-stu-id="cf48f-122">In Commerce site builder, find and edit the checkout page or fragment that contains the checkout module for the B2B e-commerce site.</span></span>
1. <span data-ttu-id="cf48f-123">Vietoje **Išsiregistravimo sektoriaus konteineris** rinkitės **Įtraukti modulį** ir tuomet įtraukite **Kliento sąskaitos mokėjimas** modulį.</span><span class="sxs-lookup"><span data-stu-id="cf48f-123">In the **Checkout section container** slot, select **Add Module**, and then add a **Customer account payment** module.</span></span>
1. <span data-ttu-id="cf48f-124">Padėkite **Kliento sąskaitos mokėjimas** modulį pasirinkę daugtaškį (**...**) ir tuomet pasirinkę **Eiti aukštyn** ar **Eiti žemyn** kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="cf48f-124">Position the **Customer account payment** module by selecting the ellipsis (**...**), and then selecting **Move Up** or **Move Down** as required.</span></span>
1. <span data-ttu-id="cf48f-125">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="cf48f-125">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a><span data-ttu-id="cf48f-126">Patvirtinkite, kad kliento sąskaitos sumokėjimo metodas buvo įjungtas ir publikuotas</span><span class="sxs-lookup"><span data-stu-id="cf48f-126">Confirm that the customer account payment method has been enabled and published</span></span>

<span data-ttu-id="cf48f-127">Norėdami patvirtinti, kad kliento sąskaitos sumokėjimo metodas buvo įjungtas ir publikuotas, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cf48f-127">To confirm that the customer account payment method has been enabled, follow these steps.</span></span>

1. <span data-ttu-id="cf48f-128">Prisijunkite prie el. komercijos saito.</span><span class="sxs-lookup"><span data-stu-id="cf48f-128">Sign in to the e-commerce site.</span></span>
1. <span data-ttu-id="cf48f-129">Įtraukite prekę į vežimėlį.</span><span class="sxs-lookup"><span data-stu-id="cf48f-129">Add a product to the cart.</span></span>
1. <span data-ttu-id="cf48f-130">Eikite į išsiregistravimo puslapį.</span><span class="sxs-lookup"><span data-stu-id="cf48f-130">Go to the checkout page.</span></span> <span data-ttu-id="cf48f-131">Turėtumėte matyti naują **Kliento sąskaitos** mokėjimo metodą.</span><span class="sxs-lookup"><span data-stu-id="cf48f-131">You should see the new **Customer Account** payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf48f-132">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="cf48f-132">Additional resources</span></span>

[<span data-ttu-id="cf48f-133">Nustatykite B2B el. komercijos saitą</span><span class="sxs-lookup"><span data-stu-id="cf48f-133">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="cf48f-134">Kurkite organizacijos modeliavimo hierarchijas B2B organizacijoms</span><span class="sxs-lookup"><span data-stu-id="cf48f-134">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="cf48f-135">Valdykite verslo partnerio vartotojus B2B el. komercijos saituose</span><span class="sxs-lookup"><span data-stu-id="cf48f-135">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="cf48f-136">Nustatykite produkto kiekio apribojimus B2B el. komercijos saitams</span><span class="sxs-lookup"><span data-stu-id="cf48f-136">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

[<span data-ttu-id="cf48f-137">SDK ir Modulio biliotekos naujinimai</span><span class="sxs-lookup"><span data-stu-id="cf48f-137">SDK and Module library updates</span></span>](../e-commerce-extensibility/sdk-updates.md)
