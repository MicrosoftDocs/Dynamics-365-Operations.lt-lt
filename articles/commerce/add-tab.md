---
title: Skirtuko modulis
description: Šioje temoje aprašomi skirtuko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 8375c33bd6ffd3004cfc9d7b686d9a0edc77cdef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209232"
---
# <a name="tab-module"></a><span data-ttu-id="ede08-103">Skirtuko modulis</span><span class="sxs-lookup"><span data-stu-id="ede08-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ede08-104">Šioje temoje aprašomi skirtuko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="ede08-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ede08-105">Skirtuko moduliai yra talpyklas primenantys moduliai, naudojami siekiant surūšiuoti svetainės puslapyje esančią informaciją į skirtukus.</span><span class="sxs-lookup"><span data-stu-id="ede08-105">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="ede08-106">Jie gali būti naudojami bet kuriame puslapyje, kuriame informacija turi būti pateikta skirtukuose.</span><span class="sxs-lookup"><span data-stu-id="ede08-106">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="ede08-107">Kiekviename skirtuko modulyje galima įtraukti vieną ar daugiau skirtuko modulių.</span><span class="sxs-lookup"><span data-stu-id="ede08-107">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="ede08-108">Kiekvienas skirtuko elementų modulis yra vienas skirtukas. Į kiekvieną skirtuko elementų modulį galima įtraukti vieną arba daugiau modulių.</span><span class="sxs-lookup"><span data-stu-id="ede08-108">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="ede08-109">Modulių, kuriuos galima įtraukti į skirtuko elementų modulį, tipų apribojimų nėra.</span><span class="sxs-lookup"><span data-stu-id="ede08-109">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="ede08-110">Toliau pateiktame paveikslėlyje parodytas svetainės puslapyje esančio skirtuko modulio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="ede08-110">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="ede08-111">Šiame pavyzdyje pasirinktas skirtukas **Siuntimas**.</span><span class="sxs-lookup"><span data-stu-id="ede08-111">In this example, the **Shipping** tab selected.</span></span>

![Skirtuko modulio pavyzdys](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="ede08-113">Skirtuko modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="ede08-113">Tab module properties</span></span>

| <span data-ttu-id="ede08-114">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="ede08-114">Property name</span></span> | <span data-ttu-id="ede08-115">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="ede08-115">Values</span></span> | <span data-ttu-id="ede08-116">aprašymas</span><span class="sxs-lookup"><span data-stu-id="ede08-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="ede08-117">Antraštė</span><span class="sxs-lookup"><span data-stu-id="ede08-117">Heading</span></span> | <span data-ttu-id="ede08-118">Tekstas</span><span class="sxs-lookup"><span data-stu-id="ede08-118">Text</span></span> | <span data-ttu-id="ede08-119">Ši ypatybė nurodo pasirinktinę skirtuko modulio teksto antraštę.</span><span class="sxs-lookup"><span data-stu-id="ede08-119">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="ede08-120">Aktyvaus skirtuko indeksas</span><span class="sxs-lookup"><span data-stu-id="ede08-120">Active Tab Index</span></span> | <span data-ttu-id="ede08-121">Skaičius</span><span class="sxs-lookup"><span data-stu-id="ede08-121">Number</span></span> | <span data-ttu-id="ede08-122">Ši ypatybė nurodo skirtuką, kuris pagal numatytuosius parametrus turi būti suaktyvintas, kai puslapis įkeliamas.</span><span class="sxs-lookup"><span data-stu-id="ede08-122">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="ede08-123">Jei nenurodyta jokia vertė, pagal numatytuosius parametrus suaktyvinamas pirmas skirtuko elementas.</span><span class="sxs-lookup"><span data-stu-id="ede08-123">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="ede08-124">Skirtuko elementų modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="ede08-124">Tab item module properties</span></span>

| <span data-ttu-id="ede08-125">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="ede08-125">Property name</span></span> | <span data-ttu-id="ede08-126">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="ede08-126">Values</span></span> | <span data-ttu-id="ede08-127">aprašymas</span><span class="sxs-lookup"><span data-stu-id="ede08-127">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="ede08-128">Kreipinys</span><span class="sxs-lookup"><span data-stu-id="ede08-128">Title</span></span> | <span data-ttu-id="ede08-129">Tekstas</span><span class="sxs-lookup"><span data-stu-id="ede08-129">Text</span></span> | <span data-ttu-id="ede08-130">Ši ypatybė nurodo skirtuko elementų modulio pavadinimo tekstą.</span><span class="sxs-lookup"><span data-stu-id="ede08-130">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="ede08-131">Skirtuko modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="ede08-131">Add a tab module to a page</span></span>

<span data-ttu-id="ede08-132">Norėdami į puslapį įtraukti skirtuko modulį ir nustatyti ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ede08-132">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="ede08-133">Naudodami „Fabrikam“ rinkodaros šabloną (ar bet kokį kitą šabloną be apribojimų) sukurkite naują puslapį su pavadinimu **Parduotuvės strategijos puslapis**.</span><span class="sxs-lookup"><span data-stu-id="ede08-133">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="ede08-134">**Numatytojo puslapio** vietoje **Pagrindinis** pasirinkite daugtaškį (**...**) ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="ede08-134">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="ede08-135">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ede08-135">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="ede08-136">Vietoje **Konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="ede08-136">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="ede08-137">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Skirtukas**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ede08-137">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="ede08-138">Skirtuko modulio ypatybių srityje, šalia pieštuko simbolio, pasirinkite **Antraštė**.</span><span class="sxs-lookup"><span data-stu-id="ede08-138">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="ede08-139">Dialogo lange **Antraštė**, dalyje **Antraštės tekstas**, įveskite antraštės tekstą (pavyzdžiui, **Strategija**).</span><span class="sxs-lookup"><span data-stu-id="ede08-139">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="ede08-140">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ede08-140">Then select **OK**.</span></span>
1. <span data-ttu-id="ede08-141">Vietoje **Skirtukas** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="ede08-141">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="ede08-142">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Skirtuko elementas**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ede08-142">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="ede08-143">Skirtuko elementų modulio ypatybių srityje, dalyje **Pavadinimas**, įveskite pavadinimo tekstą (pavyzdžiui, **Pristatymas**).</span><span class="sxs-lookup"><span data-stu-id="ede08-143">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="ede08-144">Vietoje **Skirtuko elementas** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="ede08-144">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="ede08-145">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Teksto blokas**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ede08-145">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="ede08-146">Teksto bloko modulio ypatybių srityje, dalyje **Raiškusis tekstas**, įveskite teksto pastraipą.</span><span class="sxs-lookup"><span data-stu-id="ede08-146">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="ede08-147">Vietoje **Skirtukas** įtraukite dar kelis skirtuko elementų modulius su pavadinimais.</span><span class="sxs-lookup"><span data-stu-id="ede08-147">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="ede08-148">Kiekviename skirtuko elementų modulyje pridėkite tekstinio bloko modulį, kuriame yra turinio.</span><span class="sxs-lookup"><span data-stu-id="ede08-148">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="ede08-149">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="ede08-149">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="ede08-150">Puslapyje bus rodomas skirtuko modulis, kuriame yra skirtuko elementų modulių su jūsų įtrauktu turiniu.</span><span class="sxs-lookup"><span data-stu-id="ede08-150">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="ede08-151">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="ede08-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ede08-152">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ede08-152">Additional resources</span></span>

[<span data-ttu-id="ede08-153">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="ede08-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ede08-154">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="ede08-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="ede08-155">Akordeono modulis</span><span class="sxs-lookup"><span data-stu-id="ede08-155">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="ede08-156">Teksto bloko modulis</span><span class="sxs-lookup"><span data-stu-id="ede08-156">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]