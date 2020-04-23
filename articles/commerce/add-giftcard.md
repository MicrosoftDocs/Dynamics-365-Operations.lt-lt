---
title: Dovanų kortelės modulis
description: Šioje temoje aprašomi dovanų kortelių moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 70047376cec44523cc9cfe4df792bde23c776d8c
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261581"
---
# <a name="gift-card-module"></a><span data-ttu-id="7b1c4-103">Dovanų kortelės modulis</span><span class="sxs-lookup"><span data-stu-id="7b1c4-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7b1c4-104">Šioje temoje aprašomi dovanų kortelių moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7b1c4-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="7b1c4-105">Overview</span></span>

<span data-ttu-id="7b1c4-106">Dovanų kortelės yra įprasta mokėjimo forma, o dovanų kortelės modulį galima naudoti pirkimo užbaigimo modulyje, kad dovanų kortelės būtų priimtos.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="7b1c4-107">Dovanų kortelės modulis palaiko „Dynamics 365”, „SVS” ir „Givex” dovanų korteles.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="7b1c4-108">„SVS” ir „Givex” dovanų kortelėmis apmokama naudojant „Adyen” mokėjimo paslaugų teikėją.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="7b1c4-109">Daugiau informacijos apie išorinių dovanų kortelių, pvz., „SVS” ir „Givex”, palaikymą žr. [Išorinių dovanų kortelių palaikymas](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="7b1c4-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

## <a name="module-properties"></a><span data-ttu-id="7b1c4-110">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="7b1c4-110">Module properties</span></span>

- <span data-ttu-id="7b1c4-111">**Rodyti papildomus laukus** – ši ypatybė nurodo, kuriuos laukus reikia rodyti kartu su dovanų kortelės numeriu, kuris visada rodomas pagal numatytuosius nustatymus, naudojant dovanų korteles.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-111">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="7b1c4-112">Pavyzdžiui, kai kurios dovanų kortelės palaiko asmeninio identifikacijos numerio (PIN) rodymą, o kitos palaiko PIN ir galiojimo datos rodymą.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-112">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="7b1c4-113">Taip pat gali būti, kad ši ypatybė nustatyta į Nėra, tokiu atveju būtų rodomas tik dovanų kortelės numeris ir nebūtų jokių papildomų laukų.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-113">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="7b1c4-114">Palaikomos reikšmės:</span><span class="sxs-lookup"><span data-stu-id="7b1c4-114">Supported values:</span></span>
-   <span data-ttu-id="7b1c4-115">PIN</span><span class="sxs-lookup"><span data-stu-id="7b1c4-115">PIN</span></span>
-   <span data-ttu-id="7b1c4-116">Galiojimo data</span><span class="sxs-lookup"><span data-stu-id="7b1c4-116">Expiration date</span></span>
-   <span data-ttu-id="7b1c4-117">PIN ir galiojimo data</span><span class="sxs-lookup"><span data-stu-id="7b1c4-117">PIN and expiration date</span></span> 
-   <span data-ttu-id="7b1c4-118">Jokia</span><span class="sxs-lookup"><span data-stu-id="7b1c4-118">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="7b1c4-119">Dovanų kortelių modulių svetainės parametrai</span><span class="sxs-lookup"><span data-stu-id="7b1c4-119">Site settings for gift card modules</span></span>

<span data-ttu-id="7b1c4-120">„Commerce“ svetainių rengyklės dalyje **Svetainės parametrai \> Plėtiniai** yra dovanų kortelės modulio parametras pavadinimu **Palaikomos dovanų kortelės tipas**.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-120">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="7b1c4-121">Šis parametras palaiko tris toliau pateiktas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-121">This setting supports three values:</span></span>
- <span data-ttu-id="7b1c4-122">**„Dynamics 365” dovanų kortelė** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti tik „Dynamics 365” dovanų kortelėmis.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-122">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="7b1c4-123">Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-123">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="7b1c4-124">**„SVS” ir „Givex” dovanų kortelės** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti tik „Givex” ir „SVS” dovanų kortelėmis.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-124">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="7b1c4-125">Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems ir anoniminiams vartotojams.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-125">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="7b1c4-126">**„Dynamics 365”, „SVS” ir „Givex” dovanų kortelės** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti „Dynamics 365”, „Givex” ir „SVS” dovanų kortelėmis.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-126">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="7b1c4-127">Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-127">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="7b1c4-128">Dovanų kortelės modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="7b1c4-128">Add a gift card module to a page</span></span>

<span data-ttu-id="7b1c4-129">Instrukcijų, kaip įtraukti dovanų kortelės modulį į pirkimo užbaigimo puslapį ir nustatyti reikiamas ypatybes, žr. [Pirkimo užbaigimo modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="7b1c4-129">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b1c4-130">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7b1c4-130">Additional resources</span></span>

[<span data-ttu-id="7b1c4-131">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="7b1c4-131">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7b1c4-132">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="7b1c4-132">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7b1c4-133">Išorinių dovanų kortelių palaikymas</span><span class="sxs-lookup"><span data-stu-id="7b1c4-133">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
