---
title: Dovanų kortelės modulis
description: Šioje temoje aprašomi dovanų kortelių moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962768"
---
# <a name="gift-card-module"></a><span data-ttu-id="72cc1-103">Dovanų kortelės modulis</span><span class="sxs-lookup"><span data-stu-id="72cc1-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="72cc1-104">Šioje temoje aprašomi dovanų kortelių moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="72cc1-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="72cc1-105">Dovanų kortelių moduliai yra įprasta mokėjimo forma, naudojama „e-Commerce” operacijose, ir juos galima naudoti pirkimo užbaigimo moduliuose, kad dovanų kortelės būtų priimtos.</span><span class="sxs-lookup"><span data-stu-id="72cc1-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="72cc1-106">Dovanų kortelės modulis palaiko „Dynamics 365”, „SVS” ir „Givex” dovanų korteles.</span><span class="sxs-lookup"><span data-stu-id="72cc1-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="72cc1-107">„SVS” ir „Givex” dovanų kortelėmis apmokama naudojant „Adyen” mokėjimo paslaugų teikėją.</span><span class="sxs-lookup"><span data-stu-id="72cc1-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="72cc1-108">Daugiau informacijos apie išorinių dovanų kortelių, pvz., „SVS” ir „Givex”, palaikymą žr. [Išorinių dovanų kortelių palaikymas](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="72cc1-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="72cc1-109">„SVS” ir „Givex” dovanų kortelių panaudojimo pirkimo užbaigimo srauto metu palaikymas pasiekiamas „Dynamics 365 Commerce” 10.0.11 leidime.</span><span class="sxs-lookup"><span data-stu-id="72cc1-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="72cc1-110">Galimi du dovanų kortelių moduliai:</span><span class="sxs-lookup"><span data-stu-id="72cc1-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="72cc1-111">**Dovanų kortelė** – šis modulis gali būti naudojamas pirkimo užbaigimo puslapyje, norint naudoti dovanų kortelę kaip mokėjimo priemonę.</span><span class="sxs-lookup"><span data-stu-id="72cc1-111">**Gift card** – This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="72cc1-112">**Dovanų kortelės balanso tikrinimas** – šis modulis gali būti naudojamas bet kuriame puslapyje, norint patikrinti dovanų kortelės balansą.</span><span class="sxs-lookup"><span data-stu-id="72cc1-112">**Gift card balance check** – This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="72cc1-113">Šis modulis pasiekiamas 10.0.14 arba vėlesnio leidimo „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="72cc1-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="72cc1-114">Dovanų kortelės balanso tikrinimo modulio palaikymas pasiekiamas „Dynamics 365 Commerce” 10.0.14 leidime.</span><span class="sxs-lookup"><span data-stu-id="72cc1-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="72cc1-115">Toliau pateiktame paveikslėlyje parodytas pirkimo užbaigimo puslapyje esančio dovanų kortelės modulio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="72cc1-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Dovanų kortelės modulio pavyzdys](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="72cc1-117">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="72cc1-117">Module properties</span></span>

- <span data-ttu-id="72cc1-118">**Rodyti papildomus laukus** – ši ypatybė nurodo, kuriuos laukus reikia rodyti kartu su dovanų kortelės numeriu, kuris visada rodomas pagal numatytuosius nustatymus, naudojant dovanų korteles.</span><span class="sxs-lookup"><span data-stu-id="72cc1-118">**Show additional fields** – This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="72cc1-119">Pavyzdžiui, kai kurios dovanų kortelės palaiko asmeninio identifikacijos numerio (PIN) rodymą, o kitos palaiko PIN ir galiojimo datos rodymą.</span><span class="sxs-lookup"><span data-stu-id="72cc1-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="72cc1-120">Taip pat gali būti, kad ši ypatybė nustatyta į Nėra, tokiu atveju būtų rodomas tik dovanų kortelės numeris ir nebūtų jokių papildomų laukų.</span><span class="sxs-lookup"><span data-stu-id="72cc1-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="72cc1-121">Palaikomos reikšmės:</span><span class="sxs-lookup"><span data-stu-id="72cc1-121">Supported values:</span></span>
-   <span data-ttu-id="72cc1-122">PIN</span><span class="sxs-lookup"><span data-stu-id="72cc1-122">PIN</span></span>
-   <span data-ttu-id="72cc1-123">Galiojimo data</span><span class="sxs-lookup"><span data-stu-id="72cc1-123">Expiration date</span></span>
-   <span data-ttu-id="72cc1-124">PIN ir galiojimo data</span><span class="sxs-lookup"><span data-stu-id="72cc1-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="72cc1-125">Jokia</span><span class="sxs-lookup"><span data-stu-id="72cc1-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="72cc1-126">Dovanų kortelių modulių svetainės parametrai</span><span class="sxs-lookup"><span data-stu-id="72cc1-126">Site settings for gift card modules</span></span>

<span data-ttu-id="72cc1-127">„Commerce“ svetainių rengyklės dalyje **Svetainės parametrai \> Plėtiniai** yra dovanų kortelės modulio parametras pavadinimu **Palaikomos dovanų kortelės tipas**.</span><span class="sxs-lookup"><span data-stu-id="72cc1-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="72cc1-128">Šis parametras palaiko tris toliau pateiktas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="72cc1-128">This setting supports three values:</span></span>
- <span data-ttu-id="72cc1-129">**„Dynamics 365” dovanų kortelė** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti tik „Dynamics 365” dovanų kortelėmis.</span><span class="sxs-lookup"><span data-stu-id="72cc1-129">**Dynamics 365 gift card** – When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="72cc1-130">Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="72cc1-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="72cc1-131">**„SVS” ir „Givex” dovanų kortelės** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti tik „Givex” ir „SVS” dovanų kortelėmis.</span><span class="sxs-lookup"><span data-stu-id="72cc1-131">**SVS and Givex gift cards** – When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="72cc1-132">Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems ir anoniminiams vartotojams.</span><span class="sxs-lookup"><span data-stu-id="72cc1-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="72cc1-133">**„Dynamics 365”, „SVS” ir „Givex” dovanų kortelės** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti „Dynamics 365”, „Givex” ir „SVS” dovanų kortelėmis.</span><span class="sxs-lookup"><span data-stu-id="72cc1-133">**Dynamics 365, SVS, and Givex gift cards** – When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="72cc1-134">Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="72cc1-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="72cc1-135">Šie parametrai pasiekiami „Dynamics 365 Commerce” 10.0.11 leidime ir reikalingi tik tada, kai reikia „SVS” ar „Givex” dovanų kortelių palaikymo.</span><span class="sxs-lookup"><span data-stu-id="72cc1-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="72cc1-136">Jei atnaujinate iš senesnės „Dynamics 365 Commerce” versijos, turite rankiniu būdu atnaujinti failą appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="72cc1-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="72cc1-137">Instrukcijų, kaip atnaujinti failą appsettings.json, žr. [SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="72cc1-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a><span data-ttu-id="72cc1-138">Išplėsti vidines dovanų korteles, skirtas naudoti el. komercijos parduotuvėsfrontėse</span><span class="sxs-lookup"><span data-stu-id="72cc1-138">Extend internal gift cards for use in e-commerce storefronts</span></span>

<span data-ttu-id="72cc1-139">Pagal numatytuosius nustatymus vidinės dovanų kortelės nėra optimizuotos naudoti el. „Commerce Storefronts".</span><span class="sxs-lookup"><span data-stu-id="72cc1-139">By default, internal gift cards aren't optimized for use in e-commerce storefronts.</span></span> <span data-ttu-id="72cc1-140">Todėl prieš leisdami mokėjimui naudoti vidines dovanų korteles, turėtumėte jas konfigūruoti su plėtiniais, kurie padeda jas apsaugoti.</span><span class="sxs-lookup"><span data-stu-id="72cc1-140">Therefore, before you allow internal gift cards to be used for payment, you should configure them with extensions that help make them more secure.</span></span> <span data-ttu-id="72cc1-141">Štai dovanų kortelių sritys, kurias turėtumėte išplėsti prieš leisdami naudoti vidines dovanų korteles gamyboje:</span><span class="sxs-lookup"><span data-stu-id="72cc1-141">Here are the gift card areas that you should extend before you allow internal gift cards to be used in production:</span></span>

- <span data-ttu-id="72cc1-142">**Dovanų kortelės** numeris – numeracijos naudojamos vidinių dovanų kortelių dovanų kortelių numeriams generuoti.</span><span class="sxs-lookup"><span data-stu-id="72cc1-142">**Gift card number** – Number sequences are used to generate gift card numbers for internal gift cards.</span></span> <span data-ttu-id="72cc1-143">Kadangi skaičių sekas galima lengvai nuspėti, turite išplėsti dovanų kortelių numerių generavimą, kad išduotams dovanų kortelių numeriams būtų naudojamos atsitiktinės, kriptografijos saugos eilutės.</span><span class="sxs-lookup"><span data-stu-id="72cc1-143">Because number sequences can easily be predicted, you should extend the generation of gift card numbers so that random, cryptographically secure strings are used for the gift card numbers that are issued.</span></span>
- <span data-ttu-id="72cc1-144">**GetBalance** – **GetBalance** API naudojamas dovanų kortelių balansams ieškoti.</span><span class="sxs-lookup"><span data-stu-id="72cc1-144">**GetBalance** – The **GetBalance** API is used to look up gift card balances.</span></span> <span data-ttu-id="72cc1-145">Pagal numatytuosius nustatymus, ši API yra vieša.</span><span class="sxs-lookup"><span data-stu-id="72cc1-145">By default, this API public.</span></span> <span data-ttu-id="72cc1-146">Jei PIN nėra būtina ieškoti dovanų kortelių balansų, kyla pavojus, kad bruto force atakos galėtų naudoti GetBalance API, norint ieškoti dovanų kortelių numerių, kurie turi **balansus**.</span><span class="sxs-lookup"><span data-stu-id="72cc1-146">If a PIN isn't required to look up gift card balances, there is a risk that brute force attacks could use the **GetBalance** API to try to look up gift card numbers that have balances.</span></span> <span data-ttu-id="72cc1-147">Diegę vidinių dovanų kortelių IR API buferizavimo PIN reikalavimus, galite sumažinti riziką.</span><span class="sxs-lookup"><span data-stu-id="72cc1-147">By implementing both PIN requirements for internal gift cards and API throttling, you can help mitigate the risk.</span></span>
- <span data-ttu-id="72cc1-148">**PIN** – pagal numatytąjį nustatymą vidinės dovanų kortelės nepalaiko PIN.</span><span class="sxs-lookup"><span data-stu-id="72cc1-148">**PIN** – By default, internal gift cards don't support PINs.</span></span> <span data-ttu-id="72cc1-149">Turėtumėte išplėsti vidines dovanų korteles, kad likučiams ieškoti būtų reikalingas PIN.</span><span class="sxs-lookup"><span data-stu-id="72cc1-149">You should extend internal gift cards so that a PIN is required to look up balances.</span></span> <span data-ttu-id="72cc1-150">Šią funkciją taip pat galima naudoti dovanų kortelėms užrakinti po klaidingų bandymų įvesti PIN iš eilės.</span><span class="sxs-lookup"><span data-stu-id="72cc1-150">This functionality can also be used to lock gift cards after consecutive incorrect attempts to enter the PIN.</span></span>

## <a name="enable-gift-card-payments-for-guest-checkout"></a><span data-ttu-id="72cc1-151">Įgalinti mokėjimus dovanų kortele išsiregistrregistrus</span><span class="sxs-lookup"><span data-stu-id="72cc1-151">Enable gift card payments for guest checkout</span></span>

<span data-ttu-id="72cc1-152">Numatyta, kad mokėjimai dovanų kortele neįgalinti svečiui (anoniminiam) išregistravimas.</span><span class="sxs-lookup"><span data-stu-id="72cc1-152">By default, gift card payments aren't enabled for guest (anonymous) checkout.</span></span> <span data-ttu-id="72cc1-153">Norėdami įjungti juos, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="72cc1-153">To enable them, follow these steps.</span></span>

1. <span data-ttu-id="72cc1-154">„Commerce“ štabe eikite į **Mažmeninė prekyba ir komercija \> Kanalo sąranka \> POS nustatymai \> POS \> POS operacijos**.</span><span class="sxs-lookup"><span data-stu-id="72cc1-154">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS Operations**.</span></span>
1. <span data-ttu-id="72cc1-155">Pasirinkite ir sulaikykite (arba spustelėkite dešiniuoju pelės mygtuku) tinklelio antraštę, tada pasirinkite Įterpti **stulpelius**.</span><span class="sxs-lookup"><span data-stu-id="72cc1-155">Select and hold (or right-click) the header of the grid, and then select **Insert columns**.</span></span>
1. <span data-ttu-id="72cc1-156">**Įterpimo** stulpelių dialogo lange pažymėkite žymės **langelį AllowAnonymousAccess**.</span><span class="sxs-lookup"><span data-stu-id="72cc1-156">In the **Insert columns** dialog box, select the **AllowAnonymousAccess** check box.</span></span>
1. <span data-ttu-id="72cc1-157">Pasirinkite **Naujinti**.</span><span class="sxs-lookup"><span data-stu-id="72cc1-157">Select **Update**.</span></span>
1. <span data-ttu-id="72cc1-158">**520** operacijų (dovanų kortelės likutis) ir **214** atveju **nustatykite AllowAnonymousAccess** vertę  **kaip** 1.</span><span class="sxs-lookup"><span data-stu-id="72cc1-158">For operations **520** (Gift card balance) and **214**, set the **AllowAnonymousAccess** value to **1**.</span></span>
1. <span data-ttu-id="72cc1-159">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="72cc1-159">Select **Save**.</span></span>
1. <span data-ttu-id="72cc1-160">Naudodami **1090** paskirstymo grafiką sinchronizuokite kanalo duomenų bazės pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="72cc1-160">Run the **1090** scheduler job to sync changes to the channel database.</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="72cc1-161">Dovanų kortelės modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="72cc1-161">Add a gift card module to a page</span></span>

<span data-ttu-id="72cc1-162">Instrukcijų, kaip įtraukti dovanų kortelės modulį į pirkimo užbaigimo puslapį ir nustatyti reikiamas ypatybes, žr. [Pirkimo užbaigimo modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="72cc1-162">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72cc1-163">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="72cc1-163">Additional resources</span></span>

[<span data-ttu-id="72cc1-164">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="72cc1-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="72cc1-165">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="72cc1-165">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="72cc1-166">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="72cc1-166">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="72cc1-167">Mokėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="72cc1-167">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="72cc1-168">Siuntimo adreso modulis</span><span class="sxs-lookup"><span data-stu-id="72cc1-168">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="72cc1-169">Pristatymo parinkčių modulis</span><span class="sxs-lookup"><span data-stu-id="72cc1-169">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="72cc1-170">Paėmimo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="72cc1-170">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="72cc1-171">Išsamios užsakymo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="72cc1-171">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="72cc1-172">Išorinių dovanų kortelių palaikymas</span><span class="sxs-lookup"><span data-stu-id="72cc1-172">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="72cc1-173">SDK ir modulių bibliotekos naujinimai</span><span class="sxs-lookup"><span data-stu-id="72cc1-173">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
