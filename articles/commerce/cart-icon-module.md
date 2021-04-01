---
title: Krepšelio piktogramos modulis
description: Šioje temoje paaiškinamas krepšelio piktogramos modulis ir aprašoma, kaip pridėti jį prie svetainių puslapių, esančių „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 43bc274548de016f24569001bac94aff324bea12
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213239"
---
# <a name="cart-icon-module"></a><span data-ttu-id="687c3-103">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="687c3-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="687c3-104">Šioje temoje paaiškinamas krepšelio piktogramos modulis ir aprašoma, kaip pridėti jį prie svetainių puslapių, esančių „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="687c3-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="687c3-105">Krepšelio piktogramos modulis nurodo krepšelį puslapio antraštės modulyje esantį krepšelį ir krepšelyje esančių prekių skaičių.</span><span class="sxs-lookup"><span data-stu-id="687c3-105">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="687c3-106">Krepšelio piktogramos modulis taip pat nurodo ir krepšelio suvestinę (dar vadinamą mažuoju krepšeliu), kai pelės žymiklis užvestas virš krepšelio piktogramos.</span><span class="sxs-lookup"><span data-stu-id="687c3-106">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="687c3-107">Mažasis krepšelis suteikia vartotojui krepšelyje esančių prekių suvestinę ir nereikia pereiti į krepšelio puslapį.</span><span class="sxs-lookup"><span data-stu-id="687c3-107">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="687c3-108">Be to, jis taip pat leidžia vartotojui tiesiogiai pereiti prie pirkimo užbaigimo puslapio, jei jis patenkintas suvestine.</span><span class="sxs-lookup"><span data-stu-id="687c3-108">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="687c3-109">Tai sumažina naršymo puslapių skaičių ir leidžia greičiau užbaigti pirkimą.</span><span class="sxs-lookup"><span data-stu-id="687c3-109">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="687c3-110">Krepšelio piktogramos modulio palaikymas pasiekiamas „Dynamics 365 Commerce” 10.0.11 leidime.</span><span class="sxs-lookup"><span data-stu-id="687c3-110">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="687c3-111">Toliau pateiktame vaizde parodytas krepšelio piktogramos modulio, kuris rodo mažąjį krepšelį „Fabrikam“ antraštėje, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="687c3-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Krepšelio piktogramos modulio pavyzdys](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="687c3-113">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="687c3-113">Module properties</span></span>

- <span data-ttu-id="687c3-114">**Rodyti mažąjį krepšelį** – kai ši ypatybė įjungta, leidžiamas krepšelio suvestinės (mažojo krepšelio) rodymas užvedus pelės žymiklį virš krepšelio piktogramos.</span><span class="sxs-lookup"><span data-stu-id="687c3-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="687c3-115">Ši funkcija palaikoma tik darbalaukio rodinio prievaduose.</span><span class="sxs-lookup"><span data-stu-id="687c3-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="687c3-116">Krepšelio piktogramos modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="687c3-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="687c3-117">Norėdami įtraukti krepšelio piktogramos modulį, žr. [Antraštės modulis](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="687c3-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="687c3-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="687c3-118">Additional resources</span></span>

[<span data-ttu-id="687c3-119">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="687c3-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="687c3-120">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="687c3-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="687c3-121">Mokėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="687c3-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="687c3-122">Siuntimo adreso modulis</span><span class="sxs-lookup"><span data-stu-id="687c3-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="687c3-123">Pristatymo parinkčių modulis</span><span class="sxs-lookup"><span data-stu-id="687c3-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="687c3-124">Paėmimo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="687c3-124">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="687c3-125">Išsamios užsakymo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="687c3-125">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="687c3-126">Dovanų kortelės modulis</span><span class="sxs-lookup"><span data-stu-id="687c3-126">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]