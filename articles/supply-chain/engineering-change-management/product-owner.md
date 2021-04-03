---
title: Produktų savininkai
description: Šioje temoje pateikta informacija apie produkto savininkus. Produkto savininkas yra vartotojų grupė atsakinga už konkrečius produktus. Tik grupės nariai gali išleisti minėtus produktus. Produkto savininkas gali taip pat būti naudojamas patvirtinimo darbo eigoje.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: a1c3bc6f77fed83cfbbd502cdd469baa491fd81f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5266132"
---
# <a name="product-owners"></a><span data-ttu-id="8e368-106">Produktų savininkai</span><span class="sxs-lookup"><span data-stu-id="8e368-106">Product owners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e368-107">Produkto savininkas yra vartotojų grupė atsakinga už konkrečius produktus.</span><span class="sxs-lookup"><span data-stu-id="8e368-107">The product owner is a group of users who are responsible for specific products.</span></span> <span data-ttu-id="8e368-108">Kai produkto savininko grupė yra priskirta produktui, tik tos grupės nariai gali išleisti produktą.</span><span class="sxs-lookup"><span data-stu-id="8e368-108">When a product owner group is assigned to a product, only the members of that group can release the product.</span></span> <span data-ttu-id="8e368-109">Produkto savininkas gali taip pat būti naudojamas patvirtinimo darbo eigoje inžinerijos keitimo valdyme.</span><span class="sxs-lookup"><span data-stu-id="8e368-109">The product owner can also be used in the approval workflow in engineering change management.</span></span>

<span data-ttu-id="8e368-110">Produkto savininkai yra bendrieji nustatymai.</span><span class="sxs-lookup"><span data-stu-id="8e368-110">Product owners are global settings.</span></span> <span data-ttu-id="8e368-111">Dėl to, jie yra prieinami visiems juridiniams asmenims.</span><span class="sxs-lookup"><span data-stu-id="8e368-111">Therefore, they are available to all legal entities.</span></span>

## <a name="create-a-product-owner-group"></a><span data-ttu-id="8e368-112">Sukurkite produkto savininko grupę</span><span class="sxs-lookup"><span data-stu-id="8e368-112">Create a product owner group</span></span>

<span data-ttu-id="8e368-113">Norėdami sukurti produkto savininko grupę ir įtraukti į ją narius, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="8e368-113">To create a product owner group and add members to it, follow these steps.</span></span>

1. <span data-ttu-id="8e368-114">Eikite į **Inžinerijos keitimo valdymą \> Nustatymus \> Produkto savininkai**.</span><span class="sxs-lookup"><span data-stu-id="8e368-114">Go to **Engineering change management \> Setup \> Product owners**.</span></span>
2. <span data-ttu-id="8e368-115">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="8e368-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="8e368-116">Laukelyje **Produkto savininkas** įveskite grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="8e368-116">In the **Product owner** field, enter a name for the group.</span></span>
4. <span data-ttu-id="8e368-117">Laukelyje **Pavadinimas** įveskite grupės aprašą.</span><span class="sxs-lookup"><span data-stu-id="8e368-117">In the **Name** field, enter a description of the group.</span></span>
5. <span data-ttu-id="8e368-118">„FastTab“ **Nariai** įtraukite darbuotojus, kurie turi būti grupės nariai.</span><span class="sxs-lookup"><span data-stu-id="8e368-118">On the **Members** FastTab, add the workers who should be members of the group.</span></span>

## <a name="assign-a-product-owner-to-a-product"></a><span data-ttu-id="8e368-119">Priskirkite produkto savininką produktui</span><span class="sxs-lookup"><span data-stu-id="8e368-119">Assign a product owner to a product</span></span>

<span data-ttu-id="8e368-120">Siekiant priskirti produkto savininką produktui, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="8e368-120">To assign a product owner to a product, follow these steps.</span></span>

1. <span data-ttu-id="8e368-121">Atverkite **Produkto išsamios informacijos** puslapį atitinkamam produktui ar pagrindiniam produktui.</span><span class="sxs-lookup"><span data-stu-id="8e368-121">Open the **Product details** page for the relevant product or product master.</span></span>
1. <span data-ttu-id="8e368-122">„FastTab“ **Bendri** nustatykite **Produkto savininko** laukelį į atitinkamo produkto savininko grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="8e368-122">On the **General** FastTab, set the **Product owner** field to the name of the relevant product owner group.</span></span>

<span data-ttu-id="8e368-123">Kol produkto savininkas yra priskirtas produktui, tik produkto savininko grupės nariai gali redaguoti **Produkto savininko** nustatymus.</span><span class="sxs-lookup"><span data-stu-id="8e368-123">While a product owner is assigned to a product, only the members of the product owner group can edit the **Product owner** setting.</span></span>

<span data-ttu-id="8e368-124">Produkto savininkas yra taip pat matomas **Išleistų produktų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="8e368-124">The product owner is also visible on the **Released products** page.</span></span>

## <a name="product-owners-and-product-releases"></a><span data-ttu-id="8e368-125">Produkto savininkai ir produkto leidimai</span><span class="sxs-lookup"><span data-stu-id="8e368-125">Product owners and product releases</span></span>

<span data-ttu-id="8e368-126">Tik vartotojai iš produkto produkto savininko grupės gali išleisti tą produktą.</span><span class="sxs-lookup"><span data-stu-id="8e368-126">Only users from a product's product owner group can release that product.</span></span> <span data-ttu-id="8e368-127">Nepaisant to, yra išimtis, kai produktas yra vaikiška prekė ir jos valdanti prekė yra išleidžiama valdančio savininko.</span><span class="sxs-lookup"><span data-stu-id="8e368-127">However, there is an exception when the product is a child item, and its parent is released by the parent's owner.</span></span> <span data-ttu-id="8e368-128">Kitaip tarian, jei produktas yra kito produkto BOM dalis, sistema netikrina kiekvienos prekės BOM produkto savininko.</span><span class="sxs-lookup"><span data-stu-id="8e368-128">In other words, if the product is part of the BOM of another product, the system doesn't check the product owner of each item in the BOM.</span></span> <span data-ttu-id="8e368-129">Ji tikrina tik valdančios prekės produkto savininką.</span><span class="sxs-lookup"><span data-stu-id="8e368-129">It checks only the product owner of the parent item.</span></span>

<span data-ttu-id="8e368-130">Pavyzdžiui, produktas X yra priskirtas *Kūrimo biurų* produkto savininko grupei.</span><span class="sxs-lookup"><span data-stu-id="8e368-130">For example, product X is assigned to the *Design cabinets* product owner group.</span></span> <span data-ttu-id="8e368-131">Produktas X taip pat yra BOM Y produkto dalis, kuris yra priskirtas *Projektavimo garsiakalbių* produkto savininko grupei.</span><span class="sxs-lookup"><span data-stu-id="8e368-131">Product X is also part of the BOM of product Y, which is assigned to the *Design Speakers* product owner group.</span></span> <span data-ttu-id="8e368-132">Jei naudotojas iš *Projektavimo garsiakalbių* produkto savininko grupės išleidžia Y produktą ir jo BOM, produktas X bus išleistas kartu su produktu Y.</span><span class="sxs-lookup"><span data-stu-id="8e368-132">If a user from the *Design Speakers* product owner group releases product Y and its BOM, product X will be released together with product Y.</span></span>

## <a name="product-owners-and-approvals"></a><span data-ttu-id="8e368-133">Produkto savininkai ir patvirtinimai</span><span class="sxs-lookup"><span data-stu-id="8e368-133">Product owners and approvals</span></span>

<span data-ttu-id="8e368-134">Kadangi produkto savininkai žino, ar konkretūs inžineriniai pakeitimai tiks jų produktams, dažnai apsimoka įtraukti juos kaip patvirtinimo proceso dalį inžinerijos keitimo valdyme.</span><span class="sxs-lookup"><span data-stu-id="8e368-134">Because product owners know whether specific engineering changes will benefit their products, it often makes sense to include them as part of the approval process in engineering change management.</span></span> <span data-ttu-id="8e368-135">Galite implementuoti šį požiūrį nustatydami produkto savininkus kaip pagrindinius tiekėjus darbo eigose, kurios naudojamos inžinerijos pokyčio valdymui.</span><span class="sxs-lookup"><span data-stu-id="8e368-135">You can implement this approach by setting up the product owners as participant providers in the workflows that are used for engineering change management.</span></span> <span data-ttu-id="8e368-136">Sistema tuomet priskirs patvirtinimo užduotis darbo eigose atsižvelgiant į produktus, kurie yra inžinerijos keitimo užklausose ir inžinerijos keitimo užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="8e368-136">The system will then assign approval tasks in the workflows, based on the products that are in engineering change requests and engineering change orders.</span></span> <span data-ttu-id="8e368-137">Dėl daugiau informacijos, žr. [Valdyti keitimus inžinerijos produktams](engineering-change-management.md).</span><span class="sxs-lookup"><span data-stu-id="8e368-137">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]