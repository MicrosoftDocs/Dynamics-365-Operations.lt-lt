---
title: Nustatykite produkto kiekio apribojimus B2B el. komercijos saitams
description: Šioje temoje aprašoma, kaip nustatyti produkto kiekio apribojimus verslo su verslu (B2B) el. komercijos saitams.
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
ms.openlocfilehash: 1208b968e476ccbc7a726facf1db896c7bf3c36f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211182"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a><span data-ttu-id="13552-103">Nustatykite produkto kiekio apribojimus B2B el. komercijos saitams</span><span class="sxs-lookup"><span data-stu-id="13552-103">Set product quantity limits for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="13552-104">Šioje temoje aprašoma, kaip nustatyti produkto kiekio apribojimus verslo su verslu (B2B) el. komercijos saitams.</span><span class="sxs-lookup"><span data-stu-id="13552-104">This topic describes how to set product quantity limits for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="13552-105">Didžioji dalis produktų turi matavimo vienetą, kuris nustato jų grupes.</span><span class="sxs-lookup"><span data-stu-id="13552-105">Most products have a unit of measure that defines their grouping.</span></span> <span data-ttu-id="13552-106">Grupavimas paveikia tai, kaip produktai gali būti parduoti.</span><span class="sxs-lookup"><span data-stu-id="13552-106">The grouping affects how the products can be sold.</span></span> <span data-ttu-id="13552-107">Kai kurie produktai gali turėti papildomą grupavimą kiekiams.</span><span class="sxs-lookup"><span data-stu-id="13552-107">Some products might have an additional grouping for quantities.</span></span> <span data-ttu-id="13552-108">Šis grupavimas nustato, ar produktai gali būti parduoti kaip atskiri vienetai ar kartu ir ar esama minimalaus ar maksimalaus kiekio apribojimo, kurio būtina laikytis.</span><span class="sxs-lookup"><span data-stu-id="13552-108">This grouping determines whether the products can be sold as individual units or multiples, and whether there is a minimum or maximum order quantity limit that must be followed.</span></span>

<span data-ttu-id="13552-109">Kiekio apribojimo funkcija užtikrina, kad minimalus, maksimalus, keletas ir standartinis kiekis, kuris yra konfigūruojamas „Microsoft Dynamics 365 Commerce“ (numatytuose užsakymo nustatymuose ar „Commerce“ vietos kūrimo saito nustatymuose) yra taikomas kliento užsakymams, kurie yra daromi el. komercijos saite.</span><span class="sxs-lookup"><span data-stu-id="13552-109">The quantity limiting feature ensures that the minimum, maximum, multiple, and standard quantities that are configured in Microsoft Dynamics 365 Commerce (in the default order settings or the Commerce site builder site settings) are applied to customer orders that are placed on an e-commerce site.</span></span> <span data-ttu-id="13552-110">Produkto kiekio apribojimai šiuo metu nėra palaikomi prekybos taške ir skambučių centruose.</span><span class="sxs-lookup"><span data-stu-id="13552-110">Product quantity limits aren't currently supported for the point of sale (POS) and call centers.</span></span>

<span data-ttu-id="13552-111">Daugelis mažmeninės veiklos prekybininkų suteikia galimybę klientų užsakymams (taip pat žinomiems kaip specialūs užsakymai) atitikti įvairius produktus ir įgyvendinti reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="13552-111">Many retailers provide the option of customer orders (also known as special orders) to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="13552-112">Toliau nurodomi įprasti scenarijai.</span><span class="sxs-lookup"><span data-stu-id="13552-112">Here are some typical scenarios:</span></span>

- <span data-ttu-id="13552-113">Klientas nori konkrečių variantų produktų, kurių daugelis turi būti parduodami kaip keli.</span><span class="sxs-lookup"><span data-stu-id="13552-113">A customer wants products of specific variants to be sold in multiples of a few.</span></span>
- <span data-ttu-id="13552-114">Klientas nori atsiimti produktus parduotuvėje arba vietoje, kuri nėra parduotuvė arba vieta, kurioje klientas tuos produktus nusipirko.</span><span class="sxs-lookup"><span data-stu-id="13552-114">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span> <span data-ttu-id="13552-115">Nepaisant to, pakavimo standartai parduotuvėms skiriasi nuo pakavimo standartų interneto prekybos platinimui.</span><span class="sxs-lookup"><span data-stu-id="13552-115">However, the packing standards for the stores differ from the packing standards for online sales distribution.</span></span>
- <span data-ttu-id="13552-116">Klientas nori pirkti limituoto leidimo produktą, kuris turėtų maksimalų kiekio apribojimą prekėms, kurias galima įsigyti.</span><span class="sxs-lookup"><span data-stu-id="13552-116">A customer wants to buy a limited-edition product that has a maximum quantity limit for items that can be purchased.</span></span>

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a><span data-ttu-id="13552-117">Įjunkite numatytą užsakymo nustatymų funkciją „Commerce“ būstinėje</span><span class="sxs-lookup"><span data-stu-id="13552-117">Turn on the default order settings feature in Commerce headquarters</span></span>

<span data-ttu-id="13552-118">Prieš tai, kai galite nustatyti produkto kiekio apribojimus, numatyta užsakymo nustatymų funkcija turi būti įjungta „Commerce“ būstinėje.</span><span class="sxs-lookup"><span data-stu-id="13552-118">Before you can set product quantity limits, the default order settings feature must be turned on in Commerce headquarters.</span></span>

<span data-ttu-id="13552-119">Norėdami įjungti numatytą užsakymo nustatymų funkciją, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="13552-119">To turn on the default order settings feature, follow these steps.</span></span>

1. <span data-ttu-id="13552-120">Eikite į **Sistemos administravimas \> Darbo sritys \> Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="13552-120">Go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="13552-121">Raskite ir pasirinkite **Palaikyti saitą ir numatytus užsakymo nustatymus tinkintame užsakyme** funkciją.</span><span class="sxs-lookup"><span data-stu-id="13552-121">Find and select the **Support the Site and Default order settings in the customer order** feature.</span></span>
1. <span data-ttu-id="13552-122">Dešiniosios juostos apačioje rinkitės **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="13552-122">At the bottom of the right pane, select **Enable now**.</span></span> 

## <a name="define-quantity-settings"></a><span data-ttu-id="13552-123">Nustatyktie kiekio nustatymus</span><span class="sxs-lookup"><span data-stu-id="13552-123">Define quantity settings</span></span> 

<span data-ttu-id="13552-124">Galite nustatyti kiekio nustatymus **Numatyti užsakymo nustatymai** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="13552-124">You can define the quantity settings on the **Default order settings** page.</span></span>

<span data-ttu-id="13552-125">Norėdami nustatyti kiekio nustatymus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="13552-125">To define the quantity settings, follow these steps.</span></span> 

1. <span data-ttu-id="13552-126">Eikite į porduktą **Mažmeninė prekyba ir komercija\> Produktai ir kategorijos \> Išleisti produktai pagal kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="13552-126">Go to Product **Retail and Commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="13552-127">Rinkitės išleistą produktą.</span><span class="sxs-lookup"><span data-stu-id="13552-127">Select a released product.</span></span>
1. <span data-ttu-id="13552-128">Veiksmų juostoje **Valdyti inventorių** skirtuke, **Užsakymo nustatymai** grupėje, rinkitės **Numatyto užsakymo nustatymai**.</span><span class="sxs-lookup"><span data-stu-id="13552-128">On the Action Pane, on the **Manage inventory** tab, in the **Order settings** group, select **Default order settings**.</span></span> 
1. <span data-ttu-id="13552-129">Puslapyje **Numatyto užsakymo nustatymai**, „FastTabe“ **Prekybos užsakymas** skyriuje **Prekybos kiekis**, nustatykite produkto pardavimo kiekius:</span><span class="sxs-lookup"><span data-stu-id="13552-129">On the **Default order settings** page, on the **Sales order** FastTab, in the **Sales quantity** section, set the product sales quantities:</span></span>

    - <span data-ttu-id="13552-130">**Keli** – Kiekis, kurį produktas gali būti paverstas į kelis.</span><span class="sxs-lookup"><span data-stu-id="13552-130">**Multiple** – The quantity that the product can be bought in multiples of.</span></span>
    - <span data-ttu-id="13552-131">**Minimalus užsakymo kiekis** – Minimalus produktų skaičius, kuris turi būti įsigytas.</span><span class="sxs-lookup"><span data-stu-id="13552-131">**Minimum Order Quantity** – The minimum number of products that must be purchased.</span></span>
    - <span data-ttu-id="13552-132">**Maksimalus užsakymo kiekis** – Maksimalus produktų skaičius, kurį galima įsigyti.</span><span class="sxs-lookup"><span data-stu-id="13552-132">**Maximum Order Quantity** – The maximum number of products that can be purchased.</span></span>
    - <span data-ttu-id="13552-133">**Standartinis užsakymo kiekis** – Numatytas kiekis, kuris yra automatiškai įvedamas, kai produktas yra pasirinktas.</span><span class="sxs-lookup"><span data-stu-id="13552-133">**Standard Order Quantity** – The default quantity that is automatically entered when the product is selected.</span></span>

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a><span data-ttu-id="13552-134">Įjunkite B2B užsakymo kiekių apribojimų funkciją „Commerce“ saito kūrimo įrankyje</span><span class="sxs-lookup"><span data-stu-id="13552-134">Turn on the B2B order quantity limits feature in Commerce site builder</span></span>

<span data-ttu-id="13552-135">Norėdami įjungti B2B užsakymo kiekių apribojimų funkciją „Commerce“ saito kūrimo įrankyje, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="13552-135">To turn on the B2B order quantity limits feature in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="13552-136">Eikite į **Saito nustatymai \> Plėtiniai**</span><span class="sxs-lookup"><span data-stu-id="13552-136">Go to **Site settings \> Extensions**</span></span>
1. <span data-ttu-id="13552-137">Skyriuje **Įjungti užsakymo kiekio apribojimus**, rinkitės **Įjungti B2B klientams** iškrentančiame meniu.</span><span class="sxs-lookup"><span data-stu-id="13552-137">Under **Enable Order Quantity Limits**, select **Enabled for B2B customers** in the drop-down menu.</span></span> 

> [!NOTE] 
> <span data-ttu-id="13552-138">Naujinti saito kūrimo įrankio nustatymai įsigalioja po to, kai app.settings.json failas buvo atnaujintas.</span><span class="sxs-lookup"><span data-stu-id="13552-138">Updated site builder settings take effect only after the app.settings.json file has been updated.</span></span> <span data-ttu-id="13552-139">Dėl daugiau informacijos, žr. [SDK ir modulio bibliotekos naujinimai](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="13552-139">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13552-140">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="13552-140">Additional resources</span></span>

[<span data-ttu-id="13552-141">Nustatykite B2B el. komercijos saitą</span><span class="sxs-lookup"><span data-stu-id="13552-141">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="13552-142">Kurkite organizacijos modeliavimo hierarchijas B2B organizacijoms</span><span class="sxs-lookup"><span data-stu-id="13552-142">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="13552-143">Verslo partnerio vartotojų valdymas B2B el. prekybos svetainėse</span><span class="sxs-lookup"><span data-stu-id="13552-143">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="13552-144">Konfigūruoti kliento sąskaitos mokėjimo metodą B2B el. komercijos saitams</span><span class="sxs-lookup"><span data-stu-id="13552-144">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]