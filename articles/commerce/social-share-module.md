---
title: „Social Share” modulis
description: Šioje temoje aprašomi „Social Share” moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 82a8795360f453cdee19fa6e9e376a42e8276849
ms.sourcegitcommit: 69075e001d1fb4ef69282667052cd8d082273094
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022086"
---
# <a name="social-share-module"></a><span data-ttu-id="d8cf3-103">„Social Share” modulis</span><span class="sxs-lookup"><span data-stu-id="d8cf3-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d8cf3-104">Šioje temoje aprašomi „Social Share” moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d8cf3-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="d8cf3-105">Overview</span></span>

<span data-ttu-id="d8cf3-106">„Social Share” moduliai leidžia vartotojams bendrinti „e-Commerce” svetainių puslapių URL socialiniuose tinkluose, pvz., „Facebook”, „Twitter”, „Pinterest” ir „LinkedIn”.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-106">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="d8cf3-107">Svetainių puslapių URL taip pat galima bendrinti el. paštu.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-107">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="d8cf3-108">„Social Share” moduliai dažniausiai naudojami produkto informacijos puslapiuose (PDP), siekiant padėti vartotojams bendrinti produkto informaciją.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-108">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="d8cf3-109">Kiekvienas „Social Share” modulis yra „Social Share” elementų modulių konteineris.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-109">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="d8cf3-110">Kiekvienas „Social Share” elemento modulis gali būti sukonfigūruotas taip, kad nukreiptų konkrečią socialinės medijos svetainę.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-110">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="d8cf3-111">Integravimas su „Facebook”, „Twitter”, „Pinterest”, „LinkedIn” ir el. paštu palaikomas iš karto.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-111">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="d8cf3-112">Kai svetainės vartotojas pasirenka socialinio tinklo simbolį, paleidžiamas HTML „iFrame“ atitinkamai socialinės medijos svetainei.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-112">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="d8cf3-113">Naudodamas „iFrame” vartotojas gali prisijungti ir užregistruoti peržiūrėtą puslapio turinį.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-113">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="d8cf3-114">Kiekviena socialinės medijos platforma gali sekti slapukus, todėl šis modulis reikalauja, kad svetainės vartotojai sutiktų su sutikimo naudoti slapukus pranešimu.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-114">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="d8cf3-115">Jei nesutinkama naudoti slapukus, modulis bus paslėptas puslapyje.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-115">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="d8cf3-116">Daugiau informacijos žr. [Slapukų atitiktis](cookie-compliance.md) .</span><span class="sxs-lookup"><span data-stu-id="d8cf3-116">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="d8cf3-117">Toliau pateiktoje iliustracijoje pabrėžiamas „Social Share” modulio, naudojamo produkto informacijos puslapyje, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-117">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![„Social Share” modulio pavyzdys](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="d8cf3-119">„Social Share” modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="d8cf3-119">Social share module properties</span></span>

| <span data-ttu-id="d8cf3-120">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="d8cf3-120">Property name</span></span>             | <span data-ttu-id="d8cf3-121">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="d8cf3-121">Value</span></span>                 | <span data-ttu-id="d8cf3-122">aprašymas</span><span class="sxs-lookup"><span data-stu-id="d8cf3-122">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="d8cf3-123">Antraštė</span><span class="sxs-lookup"><span data-stu-id="d8cf3-123">Caption</span></span>                  | <span data-ttu-id="d8cf3-124">Tekstas</span><span class="sxs-lookup"><span data-stu-id="d8cf3-124">Text</span></span> | <span data-ttu-id="d8cf3-125">Ši ypatybė nurodo modulio antraštę.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-125">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="d8cf3-126">Padėtis</span><span class="sxs-lookup"><span data-stu-id="d8cf3-126">Orientation</span></span> | <span data-ttu-id="d8cf3-127">**Vertikali** ar **Horizontali**</span><span class="sxs-lookup"><span data-stu-id="d8cf3-127">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="d8cf3-128">Ši ypatybė apibrėžia socialinės medijos elementų maketo padėtį.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-128">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="d8cf3-129">„Social Share” elementų modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="d8cf3-129">Social share item module properties</span></span>
| <span data-ttu-id="d8cf3-130">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="d8cf3-130">Property name</span></span>             | <span data-ttu-id="d8cf3-131">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="d8cf3-131">Value</span></span>                 | <span data-ttu-id="d8cf3-132">aprašymas</span><span class="sxs-lookup"><span data-stu-id="d8cf3-132">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="d8cf3-133">Socialinė medija</span><span class="sxs-lookup"><span data-stu-id="d8cf3-133">Social media</span></span>              | <span data-ttu-id="d8cf3-134">**„Facebook”** , **„Twitter”** , **„Pinterest”** , **„LinkedIn”** , **„Mail“**</span><span class="sxs-lookup"><span data-stu-id="d8cf3-134">**Facebook** , **Twitter** , **Pinterest** , **LinkedIn** , **Mail**</span></span> | <span data-ttu-id="d8cf3-135">Išskleidžiamasis meniu, kuriame yra socialinės medijos platformų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-135">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="d8cf3-136">Piktograma</span><span class="sxs-lookup"><span data-stu-id="d8cf3-136">Icon</span></span> |<span data-ttu-id="d8cf3-137">Nuotrauka</span><span class="sxs-lookup"><span data-stu-id="d8cf3-137">Image</span></span>    | <span data-ttu-id="d8cf3-138">Tai bus atitinkamos socialinės medijos rodomas vaizdas.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-138">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="d8cf3-139">Geriausia būtų kiekvienos platformos vaizdo ieškoti socialinės medijos platformos SDK.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-139">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="d8cf3-140">„Social Share” modulio įtraukimas į pirkimo langelio modulį</span><span class="sxs-lookup"><span data-stu-id="d8cf3-140">Add a social share module to a buy box module</span></span>

<span data-ttu-id="d8cf3-141">Norėdami įtraukti „Social Share” modulį į pirkimo langelio modulį, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-141">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="d8cf3-142">„Fabrikam” svetainėje pasirinkite **Puslapiai** , tada – puslapį **DefaultPDP** , kad būtų atidarytas produkto informacijos puslapis.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-142">In the Fabrikam site, select **Pages** , and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="d8cf3-143">Vietoje **Pirkimo langelis (būtina)** pasirinkite daugtaškį ( **...** ), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-143">In the **Buybox (required)** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d8cf3-144">Dialogo lange **Įtraukti modulį** pasirinkite modulį **„Social Share”** , tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-144">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d8cf3-145">Vietoje **„Social Share”** pasirinkite daugtaškį ( **...** ), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-145">In the **Social Share** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d8cf3-146">Dialogo lange **Įtraukti modulį** pasirinkite modulį **SocialShare** , tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-146">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d8cf3-147">Modulio **SocialShare** ypatybių srities dalyje **Padėtis** pasirinkite **Horizontali**.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-147">In the properties pane of the **SocialShare** module, under **Orientation** , select **Horizontal**.</span></span> <span data-ttu-id="d8cf3-148">Jei reikia, įtraukite antraštę.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-148">Add a caption as needed.</span></span>
1. <span data-ttu-id="d8cf3-149">Vietoje **SocialShare** pasirinkite daugtaškį ( **...** ), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-149">In the **SocialShare** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d8cf3-150">Dialogo lange **Įtraukti modulį** pasirinkite modulį **SocialShareItem** , tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-150">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d8cf3-151">Modulio **SocialShareItem** ypatybių srities dalyje **Socialinė medija** pasirinkite **„Facebook”**.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-151">In the properties pane of the **SocialShareItem** module, under **Social Media** , select **Facebook**.</span></span>
1. <span data-ttu-id="d8cf3-152">Modulio **SocialShareItem** ypatybių srities dalyje **Piktograma** pasirinkite **+ Įtraukti vaizdą**.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-152">In the properties pane of the **SocialShareItem** module, under **Icon** , select **+ Add an image**.</span></span>
1. <span data-ttu-id="d8cf3-153">Dialogo lange **Medijos parinkiklis** pasirinkite „Facebook” logotipo vaizdą, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-153">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="d8cf3-154">Jei nėra „Facebook” logotipo vaizdo, pasirinkite **Įkelti naują medijos elementą** , kad įkeltumėte.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-154">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="d8cf3-155">Įtraukite ir konfigūruokite papildomus modulius **SocialShareItem** pagal poreikį.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-155">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="d8cf3-156">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-156">Select **Save** , and then select **Preview** to preview the page.</span></span> <span data-ttu-id="d8cf3-157">Puslapyje bus rodomas „Social Share” modulis.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-157">The page will show the social share module.</span></span>
1. <span data-ttu-id="d8cf3-158">Pasirinkite **Baigti redagavimą** , kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti** , kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="d8cf3-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d8cf3-159">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d8cf3-159">Additional resources</span></span>

[<span data-ttu-id="d8cf3-160">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="d8cf3-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d8cf3-161">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="d8cf3-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="d8cf3-162">Slapukų atitiktis</span><span class="sxs-lookup"><span data-stu-id="d8cf3-162">Cookie compliance</span></span>](cookie-compliance.md)
