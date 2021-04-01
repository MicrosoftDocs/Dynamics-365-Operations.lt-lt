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
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c024cc1b16ca60b2277eba2d7045020c2e67c3a0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206300"
---
# <a name="gift-card-module"></a><span data-ttu-id="7df4e-103">Dovanų kortelės modulis</span><span class="sxs-lookup"><span data-stu-id="7df4e-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7df4e-104">Šioje temoje aprašomi dovanų kortelių moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="7df4e-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7df4e-105">Dovanų kortelių moduliai yra įprasta mokėjimo forma, naudojama „e-Commerce” operacijose, ir juos galima naudoti pirkimo užbaigimo moduliuose, kad dovanų kortelės būtų priimtos.</span><span class="sxs-lookup"><span data-stu-id="7df4e-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="7df4e-106">Dovanų kortelės modulis palaiko „Dynamics 365”, „SVS” ir „Givex” dovanų korteles.</span><span class="sxs-lookup"><span data-stu-id="7df4e-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="7df4e-107">„SVS” ir „Givex” dovanų kortelėmis apmokama naudojant „Adyen” mokėjimo paslaugų teikėją.</span><span class="sxs-lookup"><span data-stu-id="7df4e-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="7df4e-108">Daugiau informacijos apie išorinių dovanų kortelių, pvz., „SVS” ir „Givex”, palaikymą žr. [Išorinių dovanų kortelių palaikymas](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="7df4e-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="7df4e-109">„SVS” ir „Givex” dovanų kortelių panaudojimo pirkimo užbaigimo srauto metu palaikymas pasiekiamas „Dynamics 365 Commerce” 10.0.11 leidime.</span><span class="sxs-lookup"><span data-stu-id="7df4e-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="7df4e-110">Galimi du dovanų kortelių moduliai:</span><span class="sxs-lookup"><span data-stu-id="7df4e-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="7df4e-111">**Dovanų kortelė** – šis modulis gali būti naudojamas pirkimo užbaigimo puslapyje, norint naudoti dovanų kortelę kaip mokėjimo priemonę.</span><span class="sxs-lookup"><span data-stu-id="7df4e-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="7df4e-112">**Dovanų kortelės balanso tikrinimas** – šis modulis gali būti naudojamas bet kuriame puslapyje, norint patikrinti dovanų kortelės balansą.</span><span class="sxs-lookup"><span data-stu-id="7df4e-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="7df4e-113">Šis modulis pasiekiamas 10.0.14 arba vėlesnio leidimo „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="7df4e-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="7df4e-114">Dovanų kortelės balanso tikrinimo modulio palaikymas pasiekiamas „Dynamics 365 Commerce” 10.0.14 leidime.</span><span class="sxs-lookup"><span data-stu-id="7df4e-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="7df4e-115">Toliau pateiktame paveikslėlyje parodytas pirkimo užbaigimo puslapyje esančio dovanų kortelės modulio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="7df4e-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Dovanų kortelės modulio pavyzdys](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="7df4e-117">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="7df4e-117">Module properties</span></span>

- <span data-ttu-id="7df4e-118">**Rodyti papildomus laukus** – ši ypatybė nurodo, kuriuos laukus reikia rodyti kartu su dovanų kortelės numeriu, kuris visada rodomas pagal numatytuosius nustatymus, naudojant dovanų korteles.</span><span class="sxs-lookup"><span data-stu-id="7df4e-118">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="7df4e-119">Pavyzdžiui, kai kurios dovanų kortelės palaiko asmeninio identifikacijos numerio (PIN) rodymą, o kitos palaiko PIN ir galiojimo datos rodymą.</span><span class="sxs-lookup"><span data-stu-id="7df4e-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="7df4e-120">Taip pat gali būti, kad ši ypatybė nustatyta į Nėra, tokiu atveju būtų rodomas tik dovanų kortelės numeris ir nebūtų jokių papildomų laukų.</span><span class="sxs-lookup"><span data-stu-id="7df4e-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="7df4e-121">Palaikomos reikšmės:</span><span class="sxs-lookup"><span data-stu-id="7df4e-121">Supported values:</span></span>
-   <span data-ttu-id="7df4e-122">PIN</span><span class="sxs-lookup"><span data-stu-id="7df4e-122">PIN</span></span>
-   <span data-ttu-id="7df4e-123">Galiojimo data</span><span class="sxs-lookup"><span data-stu-id="7df4e-123">Expiration date</span></span>
-   <span data-ttu-id="7df4e-124">PIN ir galiojimo data</span><span class="sxs-lookup"><span data-stu-id="7df4e-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="7df4e-125">Jokia</span><span class="sxs-lookup"><span data-stu-id="7df4e-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="7df4e-126">Dovanų kortelių modulių svetainės parametrai</span><span class="sxs-lookup"><span data-stu-id="7df4e-126">Site settings for gift card modules</span></span>

<span data-ttu-id="7df4e-127">„Commerce“ svetainių rengyklės dalyje **Svetainės parametrai \> Plėtiniai** yra dovanų kortelės modulio parametras pavadinimu **Palaikomos dovanų kortelės tipas**.</span><span class="sxs-lookup"><span data-stu-id="7df4e-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="7df4e-128">Šis parametras palaiko tris toliau pateiktas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="7df4e-128">This setting supports three values:</span></span>
- <span data-ttu-id="7df4e-129">**„Dynamics 365” dovanų kortelė** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti tik „Dynamics 365” dovanų kortelėmis.</span><span class="sxs-lookup"><span data-stu-id="7df4e-129">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="7df4e-130">Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="7df4e-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="7df4e-131">**„SVS” ir „Givex” dovanų kortelės** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti tik „Givex” ir „SVS” dovanų kortelėmis.</span><span class="sxs-lookup"><span data-stu-id="7df4e-131">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="7df4e-132">Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems ir anoniminiams vartotojams.</span><span class="sxs-lookup"><span data-stu-id="7df4e-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="7df4e-133">**„Dynamics 365”, „SVS” ir „Givex” dovanų kortelės** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti „Dynamics 365”, „Givex” ir „SVS” dovanų kortelėmis.</span><span class="sxs-lookup"><span data-stu-id="7df4e-133">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="7df4e-134">Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="7df4e-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7df4e-135">Šie parametrai pasiekiami „Dynamics 365 Commerce” 10.0.11 leidime ir reikalingi tik tada, kai reikia „SVS” ar „Givex” dovanų kortelių palaikymo.</span><span class="sxs-lookup"><span data-stu-id="7df4e-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="7df4e-136">Jei atnaujinate iš senesnės „Dynamics 365 Commerce” versijos, turite rankiniu būdu atnaujinti failą appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="7df4e-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="7df4e-137">Instrukcijų, kaip atnaujinti failą appsettings.json, žr. [SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="7df4e-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="7df4e-138">Dovanų kortelės modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="7df4e-138">Add a gift card module to a page</span></span>

<span data-ttu-id="7df4e-139">Instrukcijų, kaip įtraukti dovanų kortelės modulį į pirkimo užbaigimo puslapį ir nustatyti reikiamas ypatybes, žr. [Pirkimo užbaigimo modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="7df4e-139">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7df4e-140">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7df4e-140">Additional resources</span></span>

[<span data-ttu-id="7df4e-141">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="7df4e-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="7df4e-142">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="7df4e-142">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="7df4e-143">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="7df4e-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7df4e-144">Mokėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="7df4e-144">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="7df4e-145">Siuntimo adreso modulis</span><span class="sxs-lookup"><span data-stu-id="7df4e-145">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="7df4e-146">Pristatymo parinkčių modulis</span><span class="sxs-lookup"><span data-stu-id="7df4e-146">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="7df4e-147">Paėmimo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="7df4e-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="7df4e-148">Išsamios užsakymo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="7df4e-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7df4e-149">Išorinių dovanų kortelių palaikymas</span><span class="sxs-lookup"><span data-stu-id="7df4e-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="7df4e-150">SDK ir modulių bibliotekos naujinimai</span><span class="sxs-lookup"><span data-stu-id="7df4e-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]