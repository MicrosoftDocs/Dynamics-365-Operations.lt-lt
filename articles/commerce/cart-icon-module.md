---
title: Krepšelio piktogramos modulis
description: Šioje temoje paaiškinamas krepšelio piktogramos modulis ir aprašoma, kaip pridėti jį prie svetainių puslapių, esančių „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6771a84118504cd5c8e44302380eb970e4658902
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411094"
---
# <a name="cart-icon-module"></a><span data-ttu-id="a19ac-103">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="a19ac-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a19ac-104">Šioje temoje paaiškinamas krepšelio piktogramos modulis ir aprašoma, kaip pridėti jį prie svetainių puslapių, esančių „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="a19ac-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a19ac-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="a19ac-105">Overview</span></span>

<span data-ttu-id="a19ac-106">Krepšelio piktogramos modulis nurodo krepšelį puslapio antraštės modulyje esantį krepšelį ir krepšelyje esančių prekių skaičių.</span><span class="sxs-lookup"><span data-stu-id="a19ac-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="a19ac-107">Krepšelio piktogramos modulis taip pat nurodo ir krepšelio suvestinę (dar vadinamą mažuoju krepšeliu), kai pelės žymiklis užvestas virš krepšelio piktogramos.</span><span class="sxs-lookup"><span data-stu-id="a19ac-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="a19ac-108">Mažasis krepšelis suteikia vartotojui krepšelyje esančių prekių suvestinę ir nereikia pereiti į krepšelio puslapį.</span><span class="sxs-lookup"><span data-stu-id="a19ac-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="a19ac-109">Be to, jis taip pat leidžia vartotojui tiesiogiai pereiti prie pirkimo užbaigimo puslapio, jei jis patenkintas suvestine.</span><span class="sxs-lookup"><span data-stu-id="a19ac-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="a19ac-110">Tai sumažina naršymo puslapių skaičių ir leidžia greičiau užbaigti pirkimą.</span><span class="sxs-lookup"><span data-stu-id="a19ac-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

<span data-ttu-id="a19ac-111">Toliau pateiktame vaizde parodytas krepšelio piktogramos modulio, kuris rodo mažąjį krepšelį „Fabrikam“ antraštėje, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="a19ac-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Krepšelio piktogramos modulio pavyzdys](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="a19ac-113">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="a19ac-113">Module properties</span></span>

- <span data-ttu-id="a19ac-114">**Rodyti mažąjį krepšelį** – kai ši ypatybė įjungta, leidžiamas krepšelio suvestinės (mažojo krepšelio) rodymas užvedus pelės žymiklį virš krepšelio piktogramos.</span><span class="sxs-lookup"><span data-stu-id="a19ac-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="a19ac-115">Ši funkcija palaikoma tik darbalaukio rodinio prievaduose.</span><span class="sxs-lookup"><span data-stu-id="a19ac-115">This functionality is only supported for desktop view ports.</span></span>


## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="a19ac-116">Krepšelio piktogramos modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="a19ac-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="a19ac-117">Norėdami įtraukti krepšelio piktogramos modulį, žr. [Antraštės modulis](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="a19ac-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="a19ac-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="a19ac-118">Additional resources</span></span>

[<span data-ttu-id="a19ac-119">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="a19ac-119">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="a19ac-120">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="a19ac-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a19ac-121">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="a19ac-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a19ac-122">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="a19ac-122">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="a19ac-123">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="a19ac-123">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="a19ac-124">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="a19ac-124">Footer module</span></span>](author-footer-module.md)
