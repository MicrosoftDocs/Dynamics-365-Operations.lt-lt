---
title: Privatumo strategijos puslapio įtraukimas
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ į svetainę įtraukti privatumo strategijos puslapį.
author: v-chgri
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fd39ff5f8c5d97f2d524043b65627dc7e87fcf64
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946055"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="a4b47-103">Privatumo strategijos puslapio įtraukimas</span><span class="sxs-lookup"><span data-stu-id="a4b47-103">Add a privacy policy page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a4b47-104">Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ į svetainę įtraukti privatumo strategijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="a4b47-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a4b47-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="a4b47-105">Overview</span></span>

<span data-ttu-id="a4b47-106">Laikantis privatumo apsaugos taisyklių, taikomos organizacinės priemonės, kuriomis svetainių vartotojai informuojami apie tai, kaip renkami ir tvarkomi jų duomenys.</span><span class="sxs-lookup"><span data-stu-id="a4b47-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="a4b47-107">Tada vartotojai gali nuspręsti, kaip jų asmens duomenys turi būti tvarkomi, ir imtis atitinkamų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="a4b47-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="a4b47-108">„Microsoft“ privatumo nuostatų peržiūra programoje „Dynamics 365 Commerce“</span><span class="sxs-lookup"><span data-stu-id="a4b47-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="a4b47-109">Norėdami peržiūrėti „Microsoft“ privatumo nuostatas, kai esate prisijungę prie „Dynamics 365 Commerce“ kūrimo įrankių, pasirinkite viršutiniame dešiniajame kampe esantį mygtuką **Žinynas** (**?**), tada – **Privatumas ir slapukai**.</span><span class="sxs-lookup"><span data-stu-id="a4b47-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="a4b47-110">Atidaromas naujas skirtukas, kuriame yra saitas su [„Microsoft“ privatumo nuostatomis](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="a4b47-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="a4b47-111">Svetainės privatumo strategijos puslapio sukūrimas</span><span class="sxs-lookup"><span data-stu-id="a4b47-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="a4b47-112">Programoje „Dynamics 365 Commerce“ savo svetainės vartotojams prieigą prie privatumo strategijos galima suteikti keliais būdais.</span><span class="sxs-lookup"><span data-stu-id="a4b47-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="a4b47-113">Šiame skyriuje parodoma, kaip sukurti privatumo strategijos puslapį, o tada į jį nurodyti naudojant poraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="a4b47-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="a4b47-114">Toliau pateikiamos gairės yra pavyzdys, kuriuo parodoma, kaip sukurti bendrinį „Commerce“ svetainės privatumo strategijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="a4b47-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="a4b47-115">Jūsų pareiga yra sukurti ir įdiegti privatumo strategijos puslapio sprendimą, kuris geriausiai atitinka jūsų įmonės teisinius reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="a4b47-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="a4b47-116">Norėdami pradėti, kūrimo įrankiuose nueikite į svetainę, kuriai norite sukurti privatumo strategijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="a4b47-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="a4b47-117">Kurti šabloną</span><span class="sxs-lookup"><span data-stu-id="a4b47-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="a4b47-118">Jei šablonas, kurį galima naudoti privatumo strategijos puslapyje, jau sukurtas, pereikite į skyrių [Privatumo strategijos puslapio kūrimas](#build-a-privacy-policy-page).</span><span class="sxs-lookup"><span data-stu-id="a4b47-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="a4b47-119">Norėdami sukurti šabloną, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a4b47-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="a4b47-120">Nueikite į **Šablonai \> Naujas šablonas**.</span><span class="sxs-lookup"><span data-stu-id="a4b47-120">Go to **Templates \> New Template**.</span></span>
1. <span data-ttu-id="a4b47-121">Įveskite šablono pavadinimą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a4b47-121">Enter the template name, and then select **OK**.</span></span>
1. <span data-ttu-id="a4b47-122">Šablone į reikiamas puslapio dalis įtraukite reikiamus modulius.</span><span class="sxs-lookup"><span data-stu-id="a4b47-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="a4b47-123">Norėdami gauti nurodymų, užveskite pelės žymiklį virš raudonų šauktukų.</span><span class="sxs-lookup"><span data-stu-id="a4b47-123">For guidance, hover over the red exclamation marks.</span></span>

    <span data-ttu-id="a4b47-124">Pavyzdžiui, dalyje **HTML antraštė** gali reikėti modulio **Numatytasis išorinis scenarijus**.</span><span class="sxs-lookup"><span data-stu-id="a4b47-124">For example, the **HTML Head** slot might require a **Default External Script** module.</span></span>

1. <span data-ttu-id="a4b47-125">Srityje **Pagrindinė dalis** įtraukite modulį **Numatytasis puslapis**.</span><span class="sxs-lookup"><span data-stu-id="a4b47-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="a4b47-126">Modulio **Numatytasis puslapis** dalyje **Pagrindinis** įtraukite modulį **Raiškiojo turinio blokas**.</span><span class="sxs-lookup"><span data-stu-id="a4b47-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="a4b47-127">Modulyje **Raiškiojo turinio blokas** įtraukite modulį **Raiškiojo turinio bloko elementas**.</span><span class="sxs-lookup"><span data-stu-id="a4b47-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="a4b47-128">Šabloną įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="a4b47-128">Check the template in, and publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="a4b47-129">Privatumo strategijos puslapio kūrimas</span><span class="sxs-lookup"><span data-stu-id="a4b47-129">Build a privacy policy page</span></span>

<span data-ttu-id="a4b47-130">Norėdami sukurti privatumo strategijos puslapį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a4b47-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="a4b47-131">Nueikite į **Puslapiai \> Naujas puslapis**.</span><span class="sxs-lookup"><span data-stu-id="a4b47-131">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="a4b47-132">Pasirinkite privatumo strategijos puslapio šabloną.</span><span class="sxs-lookup"><span data-stu-id="a4b47-132">Select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="a4b47-133">Įveskite puslapio pavadinimą ir URL, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a4b47-133">Enter a page name and URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="a4b47-134">Puslapio vietoje **Pagrindinis** įtraukite modulį **Raiškiojo turinio blokas**.</span><span class="sxs-lookup"><span data-stu-id="a4b47-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="a4b47-135">Modulyje **Raiškiojo turinio blokas** įtraukite modulį **Raiškiojo turinio bloko elementas**.</span><span class="sxs-lookup"><span data-stu-id="a4b47-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="a4b47-136">Modulio **Raiškiojo turinio blokas** ypatybių srityje pasirinkite **Įtraukti duomenų šaltinį**, tada – **Raiškiojo teksto turinys**.</span><span class="sxs-lookup"><span data-stu-id="a4b47-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="a4b47-137">Raiškiojo teksto rengyklėje įveskite privatumo strategijos puslapio turinį.</span><span class="sxs-lookup"><span data-stu-id="a4b47-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="a4b47-138">Jei reikia, raiškiojo teksto rengyklę išplėskite į viso ekrano režimą.</span><span class="sxs-lookup"><span data-stu-id="a4b47-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="a4b47-139">Baigę įvesti turinį, pasirinkite **Peržiūra**, kad puslapį galėtumėte peržiūrėti žiniatinklio naršyklėje.</span><span class="sxs-lookup"><span data-stu-id="a4b47-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="a4b47-140">Įtraukite likusius puslapio elementus ir modulių ypatybes.</span><span class="sxs-lookup"><span data-stu-id="a4b47-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="a4b47-141">Privatumo strategijos puslapį įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="a4b47-141">Check the privacy policy page in, and publish it.</span></span>

<span data-ttu-id="a4b47-142">Norėdami publikuoti privatumo strategijos puslapio URL, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a4b47-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="a4b47-143">Nueikite į **URL adresai** ir pasirinkite privatumo strategijos puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="a4b47-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="a4b47-144">Pasirinktą URL publikuokite.</span><span class="sxs-lookup"><span data-stu-id="a4b47-144">Publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="a4b47-145">Saito su privatumo strategijos puslapiu sukūrimas poraštėje</span><span class="sxs-lookup"><span data-stu-id="a4b47-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="a4b47-146">Saitą su privatumo strategijos puslapiu galite įtraukti į fragmentą.</span><span class="sxs-lookup"><span data-stu-id="a4b47-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="a4b47-147">Tokiu būdu saitą galite bendrinti ir atnaujinti keliuose svetainės puslapiuose, nurodydami fragmentą.</span><span class="sxs-lookup"><span data-stu-id="a4b47-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="a4b47-148">Šiame pavyzdyje parodoma, kaip saitą su privatumo strategijos puslapiu įtraukti į poraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="a4b47-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="a4b47-149">Norėdami į poraštės fragmentą įtraukti saitą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a4b47-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="a4b47-150">Nueikite į **Puslapio fragmentai \> Naujas puslapio fragmentas**.</span><span class="sxs-lookup"><span data-stu-id="a4b47-150">Go to **Page Fragments \> New Page Fragment**.</span></span>
1. <span data-ttu-id="a4b47-151">Pasirinkite modulį **Poraštė**, tada lauke **Puslapio fragmento pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="a4b47-151">Select the **Footer** module, and then enter a name in the **Page Fragment Name** field.</span></span>
1. <span data-ttu-id="a4b47-152">Dalyje **Poraštės kategorija** įtraukite modulį **Poraštės elementas**.</span><span class="sxs-lookup"><span data-stu-id="a4b47-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="a4b47-153">Dešinėje esančioje ypatybių srityje pasirinkite **Saito tekstas**.</span><span class="sxs-lookup"><span data-stu-id="a4b47-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="a4b47-154">Dialogo lange **Saito tekstas** įveskite privatumo strategijos puslapio saito tekstą ir paskirtį, tada spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a4b47-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>

    <span data-ttu-id="a4b47-155">Norėdami gauti privatumo strategijos puslapio URL, nueikite į **Puslapiai**, tada – į privatumo strategijos puslapį ir nukopijuokite URL iš ypatybių srities.</span><span class="sxs-lookup"><span data-stu-id="a4b47-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>

1. <span data-ttu-id="a4b47-156">Fragmentą įrašykite, atrakinkite ir publikuokite.</span><span class="sxs-lookup"><span data-stu-id="a4b47-156">Save the fragment, check it in, and publish it.</span></span>
1. <span data-ttu-id="a4b47-157">Peržiūrėkite fragmentą ir išbandykite saitą su privatumo strategijos puslapiu.</span><span class="sxs-lookup"><span data-stu-id="a4b47-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="a4b47-158">Dabar fragmentą galima nurodyti šablone kitiems svetainės puslapiams.</span><span class="sxs-lookup"><span data-stu-id="a4b47-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="a4b47-159">Kai šis fragmentas nurodomas šablono modulyje **Poraštė**, saito nuoroda bus rodoma visuose puslapiuose, kurie yra sukurti naudojant tą šabloną.</span><span class="sxs-lookup"><span data-stu-id="a4b47-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a4b47-160">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="a4b47-160">Additional resources</span></span>

[<span data-ttu-id="a4b47-161">Atitikties apžvalga</span><span class="sxs-lookup"><span data-stu-id="a4b47-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="a4b47-162">Pritaikymo neįgaliesiems funkcijos ir galimybės</span><span class="sxs-lookup"><span data-stu-id="a4b47-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="a4b47-163">Slapukų atitiktis</span><span class="sxs-lookup"><span data-stu-id="a4b47-163">Cookie compliance</span></span>](cookie-compliance.md)
