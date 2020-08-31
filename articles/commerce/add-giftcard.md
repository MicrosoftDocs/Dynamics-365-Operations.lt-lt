---
title: Dovanų kortelės modulis
description: Šioje temoje aprašomi dovanų kortelių moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 41f808d671bf5e7425390484ea30470e044899d8
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661247"
---
# <a name="gift-card-module"></a><span data-ttu-id="46f2d-103">Dovanų kortelės modulis</span><span class="sxs-lookup"><span data-stu-id="46f2d-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="46f2d-104">Šioje temoje aprašomi dovanų kortelių moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="46f2d-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="46f2d-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="46f2d-105">Overview</span></span>

<span data-ttu-id="46f2d-106">Dovanų kortelės yra įprasta mokėjimo forma, o dovanų kortelės modulį galima naudoti pirkimo užbaigimo modulyje, kad dovanų kortelės būtų priimtos.</span><span class="sxs-lookup"><span data-stu-id="46f2d-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="46f2d-107">Dovanų kortelės modulis palaiko „Dynamics 365”, „SVS” ir „Givex” dovanų korteles.</span><span class="sxs-lookup"><span data-stu-id="46f2d-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="46f2d-108">„SVS” ir „Givex” dovanų kortelėmis apmokama naudojant „Adyen” mokėjimo paslaugų teikėją.</span><span class="sxs-lookup"><span data-stu-id="46f2d-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="46f2d-109">Daugiau informacijos apie išorinių dovanų kortelių, pvz., „SVS” ir „Givex”, palaikymą žr. [Išorinių dovanų kortelių palaikymas](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="46f2d-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

<span data-ttu-id="46f2d-110">Toliau pateiktame paveikslėlyje parodytas pirkimo užbaigimo puslapyje esančio dovanų kortelės modulio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="46f2d-110">The following image shows an example of a gift card module on a checkout page.</span></span>

![Dovanų kortelės modulio pavyzdys](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="46f2d-112">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="46f2d-112">Module properties</span></span>

- <span data-ttu-id="46f2d-113">**Rodyti papildomus laukus** – ši ypatybė nurodo, kuriuos laukus reikia rodyti kartu su dovanų kortelės numeriu, kuris visada rodomas pagal numatytuosius nustatymus, naudojant dovanų korteles.</span><span class="sxs-lookup"><span data-stu-id="46f2d-113">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="46f2d-114">Pavyzdžiui, kai kurios dovanų kortelės palaiko asmeninio identifikacijos numerio (PIN) rodymą, o kitos palaiko PIN ir galiojimo datos rodymą.</span><span class="sxs-lookup"><span data-stu-id="46f2d-114">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="46f2d-115">Taip pat gali būti, kad ši ypatybė nustatyta į Nėra, tokiu atveju būtų rodomas tik dovanų kortelės numeris ir nebūtų jokių papildomų laukų.</span><span class="sxs-lookup"><span data-stu-id="46f2d-115">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="46f2d-116">Palaikomos reikšmės:</span><span class="sxs-lookup"><span data-stu-id="46f2d-116">Supported values:</span></span>
-   <span data-ttu-id="46f2d-117">PIN</span><span class="sxs-lookup"><span data-stu-id="46f2d-117">PIN</span></span>
-   <span data-ttu-id="46f2d-118">Galiojimo data</span><span class="sxs-lookup"><span data-stu-id="46f2d-118">Expiration date</span></span>
-   <span data-ttu-id="46f2d-119">PIN ir galiojimo data</span><span class="sxs-lookup"><span data-stu-id="46f2d-119">PIN and expiration date</span></span> 
-   <span data-ttu-id="46f2d-120">Jokia</span><span class="sxs-lookup"><span data-stu-id="46f2d-120">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="46f2d-121">Dovanų kortelių modulių svetainės parametrai</span><span class="sxs-lookup"><span data-stu-id="46f2d-121">Site settings for gift card modules</span></span>

<span data-ttu-id="46f2d-122">„Commerce“ svetainių rengyklės dalyje **Svetainės parametrai \> Plėtiniai** yra dovanų kortelės modulio parametras pavadinimu **Palaikomos dovanų kortelės tipas**.</span><span class="sxs-lookup"><span data-stu-id="46f2d-122">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="46f2d-123">Šis parametras palaiko tris toliau pateiktas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="46f2d-123">This setting supports three values:</span></span>
- <span data-ttu-id="46f2d-124">**„Dynamics 365” dovanų kortelė** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti tik „Dynamics 365” dovanų kortelėmis.</span><span class="sxs-lookup"><span data-stu-id="46f2d-124">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="46f2d-125">Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="46f2d-125">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="46f2d-126">**„SVS” ir „Givex” dovanų kortelės** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti tik „Givex” ir „SVS” dovanų kortelėmis.</span><span class="sxs-lookup"><span data-stu-id="46f2d-126">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="46f2d-127">Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems ir anoniminiams vartotojams.</span><span class="sxs-lookup"><span data-stu-id="46f2d-127">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="46f2d-128">**„Dynamics 365”, „SVS” ir „Givex” dovanų kortelės** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti „Dynamics 365”, „Givex” ir „SVS” dovanų kortelėmis.</span><span class="sxs-lookup"><span data-stu-id="46f2d-128">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="46f2d-129">Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="46f2d-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="46f2d-130">Dovanų kortelės modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="46f2d-130">Add a gift card module to a page</span></span>

<span data-ttu-id="46f2d-131">Instrukcijų, kaip įtraukti dovanų kortelės modulį į pirkimo užbaigimo puslapį ir nustatyti reikiamas ypatybes, žr. [Pirkimo užbaigimo modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="46f2d-131">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="46f2d-132">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="46f2d-132">Additional resources</span></span>

[<span data-ttu-id="46f2d-133">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="46f2d-133">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="46f2d-134">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="46f2d-134">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="46f2d-135">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="46f2d-135">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="46f2d-136">Mokėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="46f2d-136">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="46f2d-137">Pristatymo adreso modulis</span><span class="sxs-lookup"><span data-stu-id="46f2d-137">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="46f2d-138">Pristatymo parinkčių modulis</span><span class="sxs-lookup"><span data-stu-id="46f2d-138">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="46f2d-139">Išsamios užsakymo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="46f2d-139">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="46f2d-140">Išorinių dovanų kortelių palaikymas</span><span class="sxs-lookup"><span data-stu-id="46f2d-140">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
