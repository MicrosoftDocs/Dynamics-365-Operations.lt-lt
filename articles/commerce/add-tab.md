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
ms.openlocfilehash: 42c3cd99897627dbcdbdec91cfdb03d5743f7388
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980187"
---
# <a name="tab-module"></a><span data-ttu-id="aa351-103">Skirtuko modulis</span><span class="sxs-lookup"><span data-stu-id="aa351-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aa351-104">Šioje temoje aprašomi skirtuko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="aa351-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="aa351-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="aa351-105">Overview</span></span>

<span data-ttu-id="aa351-106">Skirtuko moduliai yra talpyklas primenantys moduliai, naudojami siekiant surūšiuoti svetainės puslapyje esančią informaciją į skirtukus.</span><span class="sxs-lookup"><span data-stu-id="aa351-106">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="aa351-107">Jie gali būti naudojami bet kuriame puslapyje, kuriame informacija turi būti pateikta skirtukuose.</span><span class="sxs-lookup"><span data-stu-id="aa351-107">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="aa351-108">Kiekviename skirtuko modulyje galima įtraukti vieną ar daugiau skirtuko modulių.</span><span class="sxs-lookup"><span data-stu-id="aa351-108">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="aa351-109">Kiekvienas skirtuko elementų modulis yra vienas skirtukas. Į kiekvieną skirtuko elementų modulį galima įtraukti vieną arba daugiau modulių.</span><span class="sxs-lookup"><span data-stu-id="aa351-109">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="aa351-110">Modulių, kuriuos galima įtraukti į skirtuko elementų modulį, tipų apribojimų nėra.</span><span class="sxs-lookup"><span data-stu-id="aa351-110">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="aa351-111">Toliau pateiktame paveikslėlyje parodytas svetainės puslapyje esančio skirtuko modulio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="aa351-111">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="aa351-112">Šiame pavyzdyje pasirinktas skirtukas **Siuntimas**.</span><span class="sxs-lookup"><span data-stu-id="aa351-112">In this example, the **Shipping** tab selected.</span></span>

![Skirtuko modulio pavyzdys](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="aa351-114">Skirtuko modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="aa351-114">Tab module properties</span></span>

| <span data-ttu-id="aa351-115">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="aa351-115">Property name</span></span> | <span data-ttu-id="aa351-116">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="aa351-116">Values</span></span> | <span data-ttu-id="aa351-117">aprašymas</span><span class="sxs-lookup"><span data-stu-id="aa351-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="aa351-118">Antraštė</span><span class="sxs-lookup"><span data-stu-id="aa351-118">Heading</span></span> | <span data-ttu-id="aa351-119">Tekstas</span><span class="sxs-lookup"><span data-stu-id="aa351-119">Text</span></span> | <span data-ttu-id="aa351-120">Ši ypatybė nurodo pasirinktinę skirtuko modulio teksto antraštę.</span><span class="sxs-lookup"><span data-stu-id="aa351-120">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="aa351-121">Aktyvaus skirtuko indeksas</span><span class="sxs-lookup"><span data-stu-id="aa351-121">Active Tab Index</span></span> | <span data-ttu-id="aa351-122">Skaičius</span><span class="sxs-lookup"><span data-stu-id="aa351-122">Number</span></span> | <span data-ttu-id="aa351-123">Ši ypatybė nurodo skirtuką, kuris pagal numatytuosius parametrus turi būti suaktyvintas, kai puslapis įkeliamas.</span><span class="sxs-lookup"><span data-stu-id="aa351-123">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="aa351-124">Jei nenurodyta jokia vertė, pagal numatytuosius parametrus suaktyvinamas pirmas skirtuko elementas.</span><span class="sxs-lookup"><span data-stu-id="aa351-124">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="aa351-125">Skirtuko elementų modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="aa351-125">Tab item module properties</span></span>

| <span data-ttu-id="aa351-126">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="aa351-126">Property name</span></span> | <span data-ttu-id="aa351-127">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="aa351-127">Values</span></span> | <span data-ttu-id="aa351-128">aprašymas</span><span class="sxs-lookup"><span data-stu-id="aa351-128">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="aa351-129">Kreipinys</span><span class="sxs-lookup"><span data-stu-id="aa351-129">Title</span></span> | <span data-ttu-id="aa351-130">Tekstas</span><span class="sxs-lookup"><span data-stu-id="aa351-130">Text</span></span> | <span data-ttu-id="aa351-131">Ši ypatybė nurodo skirtuko elementų modulio pavadinimo tekstą.</span><span class="sxs-lookup"><span data-stu-id="aa351-131">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="aa351-132">Skirtuko modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="aa351-132">Add a tab module to a page</span></span>

<span data-ttu-id="aa351-133">Norėdami į puslapį įtraukti skirtuko modulį ir nustatyti ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="aa351-133">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="aa351-134">Naudodami „Fabrikam“ rinkodaros šabloną (ar bet kokį kitą šabloną be apribojimų) sukurkite naują puslapį su pavadinimu **Parduotuvės strategijos puslapis**.</span><span class="sxs-lookup"><span data-stu-id="aa351-134">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="aa351-135">**Numatytojo puslapio** vietoje **Pagrindinis** pasirinkite daugtaškį (**...**) ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="aa351-135">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="aa351-136">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="aa351-136">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="aa351-137">Vietoje **Konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="aa351-137">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="aa351-138">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Skirtukas**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="aa351-138">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="aa351-139">Skirtuko modulio ypatybių srityje, šalia pieštuko simbolio, pasirinkite **Antraštė**.</span><span class="sxs-lookup"><span data-stu-id="aa351-139">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="aa351-140">Dialogo lange **Antraštė**, dalyje **Antraštės tekstas**, įveskite antraštės tekstą (pavyzdžiui, **Strategija**).</span><span class="sxs-lookup"><span data-stu-id="aa351-140">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="aa351-141">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="aa351-141">Then select **OK**.</span></span>
1. <span data-ttu-id="aa351-142">Vietoje **Skirtukas** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="aa351-142">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="aa351-143">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Skirtuko elementas**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="aa351-143">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="aa351-144">Skirtuko elementų modulio ypatybių srityje, dalyje **Pavadinimas**, įveskite pavadinimo tekstą (pavyzdžiui, **Pristatymas**).</span><span class="sxs-lookup"><span data-stu-id="aa351-144">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="aa351-145">Vietoje **Skirtuko elementas** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="aa351-145">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="aa351-146">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Teksto blokas**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="aa351-146">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="aa351-147">Teksto bloko modulio ypatybių srityje, dalyje **Raiškusis tekstas**, įveskite teksto pastraipą.</span><span class="sxs-lookup"><span data-stu-id="aa351-147">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="aa351-148">Vietoje **Skirtukas** įtraukite dar kelis skirtuko elementų modulius su pavadinimais.</span><span class="sxs-lookup"><span data-stu-id="aa351-148">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="aa351-149">Kiekviename skirtuko elementų modulyje pridėkite tekstinio bloko modulį, kuriame yra turinio.</span><span class="sxs-lookup"><span data-stu-id="aa351-149">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="aa351-150">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="aa351-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="aa351-151">Puslapyje bus rodomas skirtuko modulis, kuriame yra skirtuko elementų modulių su jūsų įtrauktu turiniu.</span><span class="sxs-lookup"><span data-stu-id="aa351-151">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="aa351-152">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="aa351-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aa351-153">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="aa351-153">Additional resources</span></span>

[<span data-ttu-id="aa351-154">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="aa351-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="aa351-155">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="aa351-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="aa351-156">Akordeono modulis</span><span class="sxs-lookup"><span data-stu-id="aa351-156">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="aa351-157">Teksto bloko modulis</span><span class="sxs-lookup"><span data-stu-id="aa351-157">Text block module</span></span>](add-content-rich-block.md)
