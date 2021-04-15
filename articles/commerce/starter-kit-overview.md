---
title: Modulių bibliotekos peržiūra
description: Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ modulių bibliotekos apžvalga.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76fd75c2ed9a3ba4728129b77a43b50267be3bf3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795338"
---
# <a name="module-library-overview"></a><span data-ttu-id="f5bf1-103">Modulių bibliotekos peržiūra</span><span class="sxs-lookup"><span data-stu-id="f5bf1-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f5bf1-104">Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ modulių bibliotekos apžvalga.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

<span data-ttu-id="f5bf1-105">„Dynamics 365 Commerce“ modulių biblioteka – tai modulių, kuriuos galima naudoti el. prekybos svetainės kūrimui, rinkinys.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-105">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="f5bf1-106">Moduliuose yra ir vartotojo sąsajos (UI) aspektų, ir funkcinio veikimo aspektų.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-106">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="f5bf1-107">Modulių bibliotekos moduliams galima taikyti temas, kad būtų pakeistas šių modulių vaizdas.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-107">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="f5bf1-108">Temose naudojami pakopinio stiliaus aprašai (CSS).</span><span class="sxs-lookup"><span data-stu-id="f5bf1-108">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="f5bf1-109">Kartu su modulių biblioteka pateikiama išgalvotai el. prekybos svetainei „Fabrikam“ skirta tema, kurią galima naudoti kaip nuorodą.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-109">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="f5bf1-110">Modulių bibliotekos moduliai</span><span class="sxs-lookup"><span data-stu-id="f5bf1-110">Module library modules</span></span>

<span data-ttu-id="f5bf1-111">Modulių bibliotekoje pateikiami toliau nurodytų tipų moduliai.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-111">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="f5bf1-112">**Konteinerio modulis** – konteinerio modulis yra paprastas modulis, kuris kitų modulių atžvilgiu veikia kaip pagrindinis modulis.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-112">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="f5bf1-113">Šis modulis valdo jame esančių modulių maketą.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-113">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="f5bf1-114">**Rinkodaros moduliai** – rinkodaros moduliai apima pagrindinės turinio bloko, teksto bloko, vaizdo įrašų leistuvo ir karuselės modulius.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-114">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="f5bf1-115">Visus šiuos modulius galima naudoti turiniui parodyti.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-115">All these modules can be used to showcase content.</span></span> <span data-ttu-id="f5bf1-116">Šie moduliai grindžiami turinio valdymo sistemos (CMS) duomenimis ir jų galima įdėti bet kuriame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-116">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="f5bf1-117">**Antraštės ir poraštės moduliai** – antraštės ir poraštės moduliai rodomi visų svetainės puslapių antraštėse ir poraštėse.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-117">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="f5bf1-118">Naudojant ypatybes šiuos modulius galima konfigūruoti pagal poreikius.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-118">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="f5bf1-119">**Ieškos moduliai** – produktus galima atrasti naudojant ieškos modulį antraštėje.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-119">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="f5bf1-120">Ieškos rezultatai rodomi ieškos rezultatų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-120">Search results appear on the search results page.</span></span> <span data-ttu-id="f5bf1-121">Produktus taip pat galima atrasti kategorijos puslapiuose, kurie yra kiekvienos kategorijos, kuri palaikoma kanalo naršymo hierarchijoje, skirtieji puslapiai.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-121">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="f5bf1-122">Be to, norint toliau filtruoti ieškos rezultatus ieškos rezultatų ir kategorijos puslapiuose, galima naudoti tikslinimo modulius.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-122">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="f5bf1-123">**Išsamios produkto informacijos puslapio moduliai** – išsamios produkto informacijos puslapiuose produkto informacijai rodyti naudojami keli moduliai.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-123">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="f5bf1-124">Pirkimo langelio modulis leidžia klientams peržiūrėti produktus ir įtraukti juos į krepšelį.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-124">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="f5bf1-125">Kiti moduliai, pavyzdžiui, techninės specifikacijos moduliai, rodo išsamią produkto informaciją.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-125">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="f5bf1-126">Įvertinimų ir atsiliepimų modulis gali būti naudojamas atsiliepimams peržiūrėti ir teikti.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-126">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="f5bf1-127">**Pirkimo internetu ir atsiėmimo parduotuvėje modulis** – pirkimo internetu ir atsiėmimo parduotuvėje modulis integruotas su „Bing“ žemėlapiais.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-127">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="f5bf1-128">Jis gali būti naudojamas norint rasti netoliese esančias parduotuves, kuriose klientai gali atsiimti įsigytas prekes.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-128">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="f5bf1-129">**Pirkimo moduliai** – pirkimo moduliai apima krepšelio modulį, kuris gali būti naudojamas prekėms į krepšelį įtraukti.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-129">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="f5bf1-130">Pirkimo užbaigimo modulis fiksuoja siuntimo adresą, pristatymo parinktis ir dovanų kortelės, lojalumo programos ir kredito kortelės informaciją, kad būtų galima apdoroti užsakymą.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-130">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="f5bf1-131">Pateikus užsakymą užsakymo patvirtinimo modulis gali būti naudojamas išsamiai patvirtinimo informacijai rodyti.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-131">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="f5bf1-132">**Paskyros valdymo moduliai** – prisijungimo modulis leidžia klientams prisijungti prie esamos paskyros, o registracijos modulis leidžia sukurti naują paskyrą.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-132">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="f5bf1-133">Sukūrus paskyrą užsakymų retrospektyvos modulis gali būti naudojamas naujausiems užsakymams peržiūrėti, o išsamios užsakymo informacijos modulis gali būti naudojamas išsamiai užsakymo informacijai peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-133">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="f5bf1-134">**Rekomendacijų modulis** – rekomendacijos rodomos naudojant produktų išdėstymo modulį.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-134">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="f5bf1-135">Šis modulis palaiko algoritminius ir redakcinius sąrašus, kuriuos galima parodyti bet kuriame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f5bf1-135">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5bf1-136">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f5bf1-136">Additional resources</span></span>

[<span data-ttu-id="f5bf1-137">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="f5bf1-137">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f5bf1-138">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="f5bf1-138">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f5bf1-139">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="f5bf1-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f5bf1-140">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="f5bf1-140">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f5bf1-141">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="f5bf1-141">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f5bf1-142">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="f5bf1-142">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f5bf1-143">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="f5bf1-143">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]