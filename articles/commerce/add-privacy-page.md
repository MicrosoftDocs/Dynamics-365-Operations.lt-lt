---
title: Privatumo strategijos puslapio įtraukimas
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ į svetainę įtraukti privatumo strategijos puslapį.
author: v-chgri
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 07a806ac040df9dee284e2466629221fbc3403a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209280"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="eba58-103">Privatumo strategijos puslapio įtraukimas</span><span class="sxs-lookup"><span data-stu-id="eba58-103">Add a privacy policy page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="eba58-104">Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ į svetainę įtraukti privatumo strategijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="eba58-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="eba58-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="eba58-105">Overview</span></span>

<span data-ttu-id="eba58-106">Laikantis privatumo apsaugos taisyklių, taikomos organizacinės priemonės, kuriomis svetainių vartotojai informuojami apie tai, kaip renkami ir tvarkomi jų duomenys.</span><span class="sxs-lookup"><span data-stu-id="eba58-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="eba58-107">Tada vartotojai gali nuspręsti, kaip jų asmens duomenys turi būti tvarkomi, ir imtis atitinkamų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="eba58-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="eba58-108">„Microsoft“ privatumo nuostatų peržiūra programoje „Dynamics 365 Commerce“</span><span class="sxs-lookup"><span data-stu-id="eba58-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="eba58-109">Norėdami peržiūrėti „Microsoft“ privatumo nuostatas, kai esate prisijungę prie „Dynamics 365 Commerce“ kūrimo įrankių, pasirinkite viršutiniame dešiniajame kampe esantį mygtuką **Žinynas** (**?**), tada – **Privatumas ir slapukai**.</span><span class="sxs-lookup"><span data-stu-id="eba58-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="eba58-110">Atidaromas naujas skirtukas, kuriame yra saitas su [„Microsoft“ privatumo nuostatomis](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="eba58-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="eba58-111">Svetainės privatumo strategijos puslapio sukūrimas</span><span class="sxs-lookup"><span data-stu-id="eba58-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="eba58-112">Programoje „Dynamics 365 Commerce“ savo svetainės vartotojams prieigą prie privatumo strategijos galima suteikti keliais būdais.</span><span class="sxs-lookup"><span data-stu-id="eba58-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="eba58-113">Šiame skyriuje parodoma, kaip sukurti privatumo strategijos puslapį, o tada į jį nurodyti naudojant poraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="eba58-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="eba58-114">Toliau pateikiamos gairės yra pavyzdys, kuriuo parodoma, kaip sukurti bendrinį „Commerce“ svetainės privatumo strategijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="eba58-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="eba58-115">Jūsų pareiga yra sukurti ir įdiegti privatumo strategijos puslapio sprendimą, kuris geriausiai atitinka jūsų įmonės teisinius reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="eba58-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="eba58-116">Norėdami pradėti, kūrimo įrankiuose nueikite į svetainę, kuriai norite sukurti privatumo strategijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="eba58-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="eba58-117">Kurti šabloną</span><span class="sxs-lookup"><span data-stu-id="eba58-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="eba58-118">Jei šablonas, kurį galima naudoti privatumo strategijos puslapyje, jau sukurtas, pereikite į skyrių [Privatumo strategijos puslapio kūrimas](#build-a-privacy-policy-page).</span><span class="sxs-lookup"><span data-stu-id="eba58-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="eba58-119">Norėdami sukurti šabloną, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="eba58-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="eba58-120">Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte puslapio šabloną.</span><span class="sxs-lookup"><span data-stu-id="eba58-120">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="eba58-121">Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite **Reklaminės juostos šablonas** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="eba58-121">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="eba58-122">Šablone į reikiamas puslapio dalis įtraukite reikiamus modulius.</span><span class="sxs-lookup"><span data-stu-id="eba58-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="eba58-123">Norėdami gauti nurodymų, užveskite pelės žymiklį virš raudonų šauktukų.</span><span class="sxs-lookup"><span data-stu-id="eba58-123">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="eba58-124">(Pavyzdžiui, dalyje **HTML antraštė** gali reikėti modulio **Numatytasis išorinis scenarijus**.)</span><span class="sxs-lookup"><span data-stu-id="eba58-124">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="eba58-125">Srityje **Pagrindinė dalis** įtraukite modulį **Numatytasis puslapis**.</span><span class="sxs-lookup"><span data-stu-id="eba58-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="eba58-126">Modulio **Numatytasis puslapis** dalyje **Pagrindinis** įtraukite modulį **Raiškiojo turinio blokas**.</span><span class="sxs-lookup"><span data-stu-id="eba58-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="eba58-127">Modulyje **Raiškiojo turinio blokas** įtraukite modulį **Raiškiojo turinio bloko elementas**.</span><span class="sxs-lookup"><span data-stu-id="eba58-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="eba58-128">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="eba58-128">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="eba58-129">Privatumo strategijos puslapio kūrimas</span><span class="sxs-lookup"><span data-stu-id="eba58-129">Build a privacy policy page</span></span>

<span data-ttu-id="eba58-130">Norėdami sukurti privatumo strategijos puslapį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="eba58-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="eba58-131">Nueikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte puslapį.</span><span class="sxs-lookup"><span data-stu-id="eba58-131">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="eba58-132">Dialogo lange **Pasirinkti šabloną** pasirinkite privatumo strategijos puslapio šabloną.</span><span class="sxs-lookup"><span data-stu-id="eba58-132">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="eba58-133">Įveskite puslapio pavadinimą ir URL, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="eba58-133">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="eba58-134">Puslapio vietoje **Pagrindinis** įtraukite modulį **Raiškiojo turinio blokas**.</span><span class="sxs-lookup"><span data-stu-id="eba58-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="eba58-135">Modulyje **Raiškiojo turinio blokas** įtraukite modulį **Raiškiojo turinio bloko elementas**.</span><span class="sxs-lookup"><span data-stu-id="eba58-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="eba58-136">Modulio **Raiškiojo turinio blokas** ypatybių srityje pasirinkite **Įtraukti duomenų šaltinį**, tada – **Raiškiojo teksto turinys**.</span><span class="sxs-lookup"><span data-stu-id="eba58-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="eba58-137">Raiškiojo teksto rengyklėje įveskite privatumo strategijos puslapio turinį.</span><span class="sxs-lookup"><span data-stu-id="eba58-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="eba58-138">Jei reikia, raiškiojo teksto rengyklę išplėskite į viso ekrano režimą.</span><span class="sxs-lookup"><span data-stu-id="eba58-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="eba58-139">Baigę įvesti turinį, pasirinkite **Peržiūra**, kad puslapį galėtumėte peržiūrėti žiniatinklio naršyklėje.</span><span class="sxs-lookup"><span data-stu-id="eba58-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="eba58-140">Įtraukite likusius puslapio elementus ir modulių ypatybes.</span><span class="sxs-lookup"><span data-stu-id="eba58-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="eba58-141">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="eba58-141">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="eba58-142">Norėdami publikuoti privatumo strategijos puslapio URL, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="eba58-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="eba58-143">Nueikite į **URL adresai** ir pasirinkite privatumo strategijos puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="eba58-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="eba58-144">Pasirinkite **Publikuoti**, kad publikuotumėte pasirinktą URL.</span><span class="sxs-lookup"><span data-stu-id="eba58-144">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="eba58-145">Saito su privatumo strategijos puslapiu sukūrimas poraštėje</span><span class="sxs-lookup"><span data-stu-id="eba58-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="eba58-146">Saitą su privatumo strategijos puslapiu galite įtraukti į fragmentą.</span><span class="sxs-lookup"><span data-stu-id="eba58-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="eba58-147">Tokiu būdu saitą galite bendrinti ir atnaujinti keliuose svetainės puslapiuose, nurodydami fragmentą.</span><span class="sxs-lookup"><span data-stu-id="eba58-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="eba58-148">Šiame pavyzdyje parodoma, kaip saitą su privatumo strategijos puslapiu įtraukti į poraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="eba58-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="eba58-149">Norėdami į poraštės fragmentą įtraukti saitą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="eba58-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="eba58-150">Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas** tam, kad sukurtumėte puslapio fragmentą.</span><span class="sxs-lookup"><span data-stu-id="eba58-150">Go to **Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="eba58-151">Dialogo lange **Naujas fragmentas** pasirinkite **Poraštės** modulį.</span><span class="sxs-lookup"><span data-stu-id="eba58-151">In the **New fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="eba58-152">Dalyje **Fragmento pavadinimas** įveskite fragmento pavadinimą ir tuomet pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="eba58-152">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="eba58-153">Dalyje **Poraštės kategorija** įtraukite modulį **Poraštės elementas**.</span><span class="sxs-lookup"><span data-stu-id="eba58-153">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="eba58-154">Dešinėje esančioje ypatybių srityje pasirinkite **Saito tekstas**.</span><span class="sxs-lookup"><span data-stu-id="eba58-154">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="eba58-155">Dialogo lange **Saito tekstas** įveskite privatumo strategijos puslapio saito tekstą ir paskirtį, tada spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="eba58-155">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="eba58-156">Norėdami gauti privatumo strategijos puslapio URL, nueikite į **Puslapiai**, tada – į privatumo strategijos puslapį ir nukopijuokite URL iš ypatybių srities.</span><span class="sxs-lookup"><span data-stu-id="eba58-156">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="eba58-157">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="eba58-157">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="eba58-158">Peržiūrėkite fragmentą ir išbandykite saitą su privatumo strategijos puslapiu.</span><span class="sxs-lookup"><span data-stu-id="eba58-158">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="eba58-159">Dabar fragmentą galima nurodyti šablone kitiems svetainės puslapiams.</span><span class="sxs-lookup"><span data-stu-id="eba58-159">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="eba58-160">Kai šis fragmentas nurodomas šablono modulyje **Poraštė**, saito nuoroda bus rodoma visuose puslapiuose, kurie yra sukurti naudojant tą šabloną.</span><span class="sxs-lookup"><span data-stu-id="eba58-160">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eba58-161">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="eba58-161">Additional resources</span></span>

[<span data-ttu-id="eba58-162">Atitikties apžvalga</span><span class="sxs-lookup"><span data-stu-id="eba58-162">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="eba58-163">Pritaikymo neįgaliesiems funkcijos ir galimybės</span><span class="sxs-lookup"><span data-stu-id="eba58-163">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="eba58-164">Slapukų atitiktis</span><span class="sxs-lookup"><span data-stu-id="eba58-164">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="eba58-165">Su sekamais turinio pakeitimais susietų vartotojo ID keitimas</span><span class="sxs-lookup"><span data-stu-id="eba58-165">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]