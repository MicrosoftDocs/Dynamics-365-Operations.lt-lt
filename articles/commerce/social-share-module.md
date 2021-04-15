---
title: „Social Share” modulis
description: Šioje temoje aprašomi „Social Share” moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: c34410a8c817de9fed350bf2cd2dd918a37c230f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795362"
---
# <a name="social-share-module"></a><span data-ttu-id="64e05-103">Bendrinimo socialiniuose tinkluose modulis</span><span class="sxs-lookup"><span data-stu-id="64e05-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="64e05-104">Šioje temoje aprašomi „Social Share” moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="64e05-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="64e05-105">„Social Share” moduliai leidžia vartotojams bendrinti „e-Commerce” svetainių puslapių URL socialiniuose tinkluose, pvz., „Facebook”, „Twitter”, „Pinterest” ir „LinkedIn”.</span><span class="sxs-lookup"><span data-stu-id="64e05-105">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="64e05-106">Svetainių puslapių URL taip pat galima bendrinti el. paštu.</span><span class="sxs-lookup"><span data-stu-id="64e05-106">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="64e05-107">„Social Share” moduliai dažniausiai naudojami produkto informacijos puslapiuose (PDP), siekiant padėti vartotojams bendrinti produkto informaciją.</span><span class="sxs-lookup"><span data-stu-id="64e05-107">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="64e05-108">Kiekvienas „Social Share” modulis yra „Social Share” elementų modulių konteineris.</span><span class="sxs-lookup"><span data-stu-id="64e05-108">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="64e05-109">Kiekvienas „Social Share” elemento modulis gali būti sukonfigūruotas taip, kad nukreiptų konkrečią socialinės medijos svetainę.</span><span class="sxs-lookup"><span data-stu-id="64e05-109">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="64e05-110">Integravimas su „Facebook”, „Twitter”, „Pinterest”, „LinkedIn” ir el. paštu palaikomas iš karto.</span><span class="sxs-lookup"><span data-stu-id="64e05-110">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="64e05-111">Kai svetainės vartotojas pasirenka socialinio tinklo simbolį, paleidžiamas HTML „iFrame“ atitinkamai socialinės medijos svetainei.</span><span class="sxs-lookup"><span data-stu-id="64e05-111">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="64e05-112">Naudodamas „iFrame” vartotojas gali prisijungti ir užregistruoti peržiūrėtą puslapio turinį.</span><span class="sxs-lookup"><span data-stu-id="64e05-112">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="64e05-113">Kiekviena socialinės medijos platforma gali sekti slapukus, todėl šis modulis reikalauja, kad svetainės vartotojai sutiktų su sutikimo naudoti slapukus pranešimu.</span><span class="sxs-lookup"><span data-stu-id="64e05-113">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="64e05-114">Jei nesutinkama naudoti slapukus, modulis bus paslėptas puslapyje.</span><span class="sxs-lookup"><span data-stu-id="64e05-114">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="64e05-115">Daugiau informacijos žr. [Slapukų atitiktis](cookie-compliance.md) .</span><span class="sxs-lookup"><span data-stu-id="64e05-115">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="64e05-116">Toliau pateiktoje iliustracijoje pabrėžiamas „Social Share” modulio, naudojamo produkto informacijos puslapyje, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="64e05-116">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![„Social Share” modulio pavyzdys](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="64e05-118">„Social Share” modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="64e05-118">Social share module properties</span></span>

| <span data-ttu-id="64e05-119">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="64e05-119">Property name</span></span>             | <span data-ttu-id="64e05-120">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="64e05-120">Value</span></span>                 | <span data-ttu-id="64e05-121">aprašymas</span><span class="sxs-lookup"><span data-stu-id="64e05-121">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="64e05-122">Antraštė</span><span class="sxs-lookup"><span data-stu-id="64e05-122">Caption</span></span>                  | <span data-ttu-id="64e05-123">Tekstas</span><span class="sxs-lookup"><span data-stu-id="64e05-123">Text</span></span> | <span data-ttu-id="64e05-124">Ši ypatybė nurodo modulio antraštę.</span><span class="sxs-lookup"><span data-stu-id="64e05-124">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="64e05-125">Padėtis</span><span class="sxs-lookup"><span data-stu-id="64e05-125">Orientation</span></span> | <span data-ttu-id="64e05-126">**Vertikali** ar **Horizontali**</span><span class="sxs-lookup"><span data-stu-id="64e05-126">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="64e05-127">Ši ypatybė apibrėžia socialinės medijos elementų maketo padėtį.</span><span class="sxs-lookup"><span data-stu-id="64e05-127">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="64e05-128">„Social Share” elementų modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="64e05-128">Social share item module properties</span></span>
| <span data-ttu-id="64e05-129">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="64e05-129">Property name</span></span>             | <span data-ttu-id="64e05-130">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="64e05-130">Value</span></span>                 | <span data-ttu-id="64e05-131">aprašymas</span><span class="sxs-lookup"><span data-stu-id="64e05-131">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="64e05-132">Socialinė medija</span><span class="sxs-lookup"><span data-stu-id="64e05-132">Social media</span></span>              | <span data-ttu-id="64e05-133">**„Facebook”**, **„Twitter”**, **„Pinterest”**, **„LinkedIn”**, **„Mail“**</span><span class="sxs-lookup"><span data-stu-id="64e05-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="64e05-134">Išskleidžiamasis meniu, kuriame yra socialinės medijos platformų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="64e05-134">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="64e05-135">Piktograma</span><span class="sxs-lookup"><span data-stu-id="64e05-135">Icon</span></span> |<span data-ttu-id="64e05-136">Nuotrauka</span><span class="sxs-lookup"><span data-stu-id="64e05-136">Image</span></span>    | <span data-ttu-id="64e05-137">Tai bus atitinkamos socialinės medijos rodomas vaizdas.</span><span class="sxs-lookup"><span data-stu-id="64e05-137">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="64e05-138">Geriausia būtų kiekvienos platformos vaizdo ieškoti socialinės medijos platformos SDK.</span><span class="sxs-lookup"><span data-stu-id="64e05-138">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="64e05-139">„Social Share” modulio įtraukimas į pirkimo langelio modulį</span><span class="sxs-lookup"><span data-stu-id="64e05-139">Add a social share module to a buy box module</span></span>

<span data-ttu-id="64e05-140">Norėdami įtraukti „Social Share” modulį į pirkimo langelio modulį, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="64e05-140">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="64e05-141">„Fabrikam” svetainėje pasirinkite **Puslapiai**, tada – puslapį **DefaultPDP**, kad būtų atidarytas produkto informacijos puslapis.</span><span class="sxs-lookup"><span data-stu-id="64e05-141">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="64e05-142">Vietoje **Pirkimo langelis (būtina)** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="64e05-142">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="64e05-143">Dialogo lange **Įtraukti modulį** pasirinkite modulį **„Social Share”**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="64e05-143">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="64e05-144">Vietoje **„Social Share”** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="64e05-144">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="64e05-145">Dialogo lange **Įtraukti modulį** pasirinkite modulį **SocialShare**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="64e05-145">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="64e05-146">Modulio **SocialShare** ypatybių srities dalyje **Padėtis** pasirinkite **Horizontali**.</span><span class="sxs-lookup"><span data-stu-id="64e05-146">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="64e05-147">Jei reikia, įtraukite antraštę.</span><span class="sxs-lookup"><span data-stu-id="64e05-147">Add a caption as needed.</span></span>
1. <span data-ttu-id="64e05-148">Vietoje **SocialShare** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="64e05-148">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="64e05-149">Dialogo lange **Įtraukti modulį** pasirinkite modulį **SocialShareItem**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="64e05-149">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="64e05-150">Modulio **SocialShareItem** ypatybių srities dalyje **Socialinė medija** pasirinkite **„Facebook”**.</span><span class="sxs-lookup"><span data-stu-id="64e05-150">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="64e05-151">Modulio **SocialShareItem** ypatybių srities dalyje **Piktograma** pasirinkite **+ Įtraukti vaizdą**.</span><span class="sxs-lookup"><span data-stu-id="64e05-151">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="64e05-152">Dialogo lange **Medijos parinkiklis** pasirinkite „Facebook” logotipo vaizdą, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="64e05-152">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="64e05-153">Jei nėra „Facebook” logotipo vaizdo, pasirinkite **Įkelti naują medijos elementą**, kad įkeltumėte.</span><span class="sxs-lookup"><span data-stu-id="64e05-153">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="64e05-154">Įtraukite ir konfigūruokite papildomus modulius **SocialShareItem** pagal poreikį.</span><span class="sxs-lookup"><span data-stu-id="64e05-154">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="64e05-155">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="64e05-155">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="64e05-156">Puslapyje bus rodomas „Social Share” modulis.</span><span class="sxs-lookup"><span data-stu-id="64e05-156">The page will show the social share module.</span></span>
1. <span data-ttu-id="64e05-157">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="64e05-157">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64e05-158">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="64e05-158">Additional resources</span></span>

[<span data-ttu-id="64e05-159">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="64e05-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="64e05-160">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="64e05-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="64e05-161">Slapukų atitiktis</span><span class="sxs-lookup"><span data-stu-id="64e05-161">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]