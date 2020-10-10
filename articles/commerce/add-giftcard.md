---
title: Dovanų kortelės modulis
description: Šioje temoje aprašomi dovanų kortelių moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: fc47d590789c79c08af7555222aa7cc9409da23c
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817431"
---
# <a name="gift-card-module"></a><span data-ttu-id="10991-103">Dovanų kortelės modulis</span><span class="sxs-lookup"><span data-stu-id="10991-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="10991-104">Šioje temoje aprašomi dovanų kortelių moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="10991-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="10991-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="10991-105">Overview</span></span>

<span data-ttu-id="10991-106">Dovanų kortelių moduliai yra įprasta mokėjimo forma, naudojama „e-Commerce” operacijose, ir juos galima naudoti pirkimo užbaigimo moduliuose, kad dovanų kortelės būtų priimtos.</span><span class="sxs-lookup"><span data-stu-id="10991-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="10991-107">Dovanų kortelės modulis palaiko „Dynamics 365”, „SVS” ir „Givex” dovanų korteles.</span><span class="sxs-lookup"><span data-stu-id="10991-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="10991-108">„SVS” ir „Givex” dovanų kortelėmis apmokama naudojant „Adyen” mokėjimo paslaugų teikėją.</span><span class="sxs-lookup"><span data-stu-id="10991-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="10991-109">Daugiau informacijos apie išorinių dovanų kortelių, pvz., „SVS” ir „Givex”, palaikymą žr. [Išorinių dovanų kortelių palaikymas](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="10991-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="10991-110">„SVS” ir „Givex” dovanų kortelių panaudojimo pirkimo užbaigimo srauto metu palaikymas pasiekiamas „Dynamics 365 Commerce” 10.0.11 leidime.</span><span class="sxs-lookup"><span data-stu-id="10991-110">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="10991-111">Galimi du dovanų kortelių moduliai:</span><span class="sxs-lookup"><span data-stu-id="10991-111">There are two gift card modules available:</span></span>

- <span data-ttu-id="10991-112">**Dovanų kortelė** – šis modulis gali būti naudojamas pirkimo užbaigimo puslapyje, norint naudoti dovanų kortelę kaip mokėjimo priemonę.</span><span class="sxs-lookup"><span data-stu-id="10991-112">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="10991-113">**Dovanų kortelės balanso tikrinimas** – šis modulis gali būti naudojamas bet kuriame puslapyje, norint patikrinti dovanų kortelės balansą.</span><span class="sxs-lookup"><span data-stu-id="10991-113">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="10991-114">Šis modulis pasiekiamas 10.0.14 arba vėlesnio leidimo „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="10991-114">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="10991-115">Dovanų kortelės balanso tikrinimo modulio palaikymas pasiekiamas „Dynamics 365 Commerce” 10.0.14 leidime.</span><span class="sxs-lookup"><span data-stu-id="10991-115">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="10991-116">Toliau pateiktame paveikslėlyje parodytas pirkimo užbaigimo puslapyje esančio dovanų kortelės modulio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="10991-116">The following image shows an example of a gift card module on a checkout page.</span></span>

![Dovanų kortelės modulio pavyzdys](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="10991-118">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="10991-118">Module properties</span></span>

- <span data-ttu-id="10991-119">**Rodyti papildomus laukus** – ši ypatybė nurodo, kuriuos laukus reikia rodyti kartu su dovanų kortelės numeriu, kuris visada rodomas pagal numatytuosius nustatymus, naudojant dovanų korteles.</span><span class="sxs-lookup"><span data-stu-id="10991-119">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="10991-120">Pavyzdžiui, kai kurios dovanų kortelės palaiko asmeninio identifikacijos numerio (PIN) rodymą, o kitos palaiko PIN ir galiojimo datos rodymą.</span><span class="sxs-lookup"><span data-stu-id="10991-120">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="10991-121">Taip pat gali būti, kad ši ypatybė nustatyta į Nėra, tokiu atveju būtų rodomas tik dovanų kortelės numeris ir nebūtų jokių papildomų laukų.</span><span class="sxs-lookup"><span data-stu-id="10991-121">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="10991-122">Palaikomos reikšmės:</span><span class="sxs-lookup"><span data-stu-id="10991-122">Supported values:</span></span>
-   <span data-ttu-id="10991-123">PIN</span><span class="sxs-lookup"><span data-stu-id="10991-123">PIN</span></span>
-   <span data-ttu-id="10991-124">Galiojimo data</span><span class="sxs-lookup"><span data-stu-id="10991-124">Expiration date</span></span>
-   <span data-ttu-id="10991-125">PIN ir galiojimo data</span><span class="sxs-lookup"><span data-stu-id="10991-125">PIN and expiration date</span></span> 
-   <span data-ttu-id="10991-126">Jokia</span><span class="sxs-lookup"><span data-stu-id="10991-126">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="10991-127">Dovanų kortelių modulių svetainės parametrai</span><span class="sxs-lookup"><span data-stu-id="10991-127">Site settings for gift card modules</span></span>

<span data-ttu-id="10991-128">„Commerce“ svetainių rengyklės dalyje **Svetainės parametrai \> Plėtiniai** yra dovanų kortelės modulio parametras pavadinimu **Palaikomos dovanų kortelės tipas**.</span><span class="sxs-lookup"><span data-stu-id="10991-128">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="10991-129">Šis parametras palaiko tris toliau pateiktas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="10991-129">This setting supports three values:</span></span>
- <span data-ttu-id="10991-130">**„Dynamics 365” dovanų kortelė** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti tik „Dynamics 365” dovanų kortelėmis.</span><span class="sxs-lookup"><span data-stu-id="10991-130">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="10991-131">Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="10991-131">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="10991-132">**„SVS” ir „Givex” dovanų kortelės** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti tik „Givex” ir „SVS” dovanų kortelėmis.</span><span class="sxs-lookup"><span data-stu-id="10991-132">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="10991-133">Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems ir anoniminiams vartotojams.</span><span class="sxs-lookup"><span data-stu-id="10991-133">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="10991-134">**„Dynamics 365”, „SVS” ir „Givex” dovanų kortelės** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti „Dynamics 365”, „Givex” ir „SVS” dovanų kortelėmis.</span><span class="sxs-lookup"><span data-stu-id="10991-134">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="10991-135">Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="10991-135">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10991-136">Šie parametrai pasiekiami „Dynamics 365 Commerce” 10.0.11 leidime ir reikalingi tik tada, kai reikia „SVS” ar „Givex” dovanų kortelių palaikymo.</span><span class="sxs-lookup"><span data-stu-id="10991-136">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="10991-137">Jei atnaujinate iš senesnės „Dynamics 365 Commerce” versijos, turite rankiniu būdu atnaujinti failą appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="10991-137">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="10991-138">Instrukcijų, kaip atnaujinti failą appsettings.json, žr. [SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="10991-138">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="10991-139">Dovanų kortelės modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="10991-139">Add a gift card module to a page</span></span>

<span data-ttu-id="10991-140">Instrukcijų, kaip įtraukti dovanų kortelės modulį į pirkimo užbaigimo puslapį ir nustatyti reikiamas ypatybes, žr. [Pirkimo užbaigimo modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="10991-140">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="10991-141">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="10991-141">Additional resources</span></span>

[<span data-ttu-id="10991-142">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="10991-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="10991-143">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="10991-143">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="10991-144">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="10991-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="10991-145">Mokėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="10991-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="10991-146">Pristatymo adreso modulis</span><span class="sxs-lookup"><span data-stu-id="10991-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="10991-147">Pristatymo parinkčių modulis</span><span class="sxs-lookup"><span data-stu-id="10991-147">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="10991-148">Išsamios užsakymo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="10991-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="10991-149">Išorinių dovanų kortelių palaikymas</span><span class="sxs-lookup"><span data-stu-id="10991-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="10991-150">SDK ir modulių bibliotekos naujinimai</span><span class="sxs-lookup"><span data-stu-id="10991-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
