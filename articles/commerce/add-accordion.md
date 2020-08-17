---
title: Akordeono modulis
description: Šioje temoje aprašomi akordeono moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1097289d339b84aa477752934afe8192e56c5ce5
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621089"
---
# <a name="accordion-module"></a><span data-ttu-id="4a2a6-103">Akordeono modulis</span><span class="sxs-lookup"><span data-stu-id="4a2a6-103">Accordion module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4a2a6-104">Šioje temoje aprašomi akordeono moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4a2a6-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="4a2a6-105">Overview</span></span>

<span data-ttu-id="4a2a6-106">Akordeono moduliai yra į talpyklas panašūs moduliai, kurie naudojami organizuojant informaciją arba modulius puslapyje ir kurie suteikia sutraukiamus stalčius primenančią funkciją.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-106">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="4a2a6-107">Akordeono modulis gali būti naudojamas bet kuriame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-107">An accordion module can be used on any page.</span></span>

<span data-ttu-id="4a2a6-108">Kiekviename akordeono modulyje galima įtraukti vieną ar daugiau akordeono elementų modulių.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-108">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="4a2a6-109">Kiekvienas akordeono elementų modulis vaizduoja sutraukiamą stalčių.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-109">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="4a2a6-110">Kiekviename akordeono elementų modulyje galima įtraukti vieną ar daugiau modulių.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-110">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="4a2a6-111">Modulių, kuriuos galima įtraukti į akordeono elementų modulį, tipų apribojimų nėra.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-111">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="4a2a6-112">Toliau pateiktame paveikslėlyje parodytas akordeono modulio, kuris naudojamas parduotuvės dažnai užduodamų klausimų (DUK) puslapyje esančiai informacijai tvarkyti, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-112">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![Akordeono modulio pavyzdys](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="4a2a6-114">Akordeono modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="4a2a6-114">Accordion module properties</span></span>

| <span data-ttu-id="4a2a6-115">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="4a2a6-115">Property name</span></span> | <span data-ttu-id="4a2a6-116">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="4a2a6-116">Values</span></span> | <span data-ttu-id="4a2a6-117">aprašymas</span><span class="sxs-lookup"><span data-stu-id="4a2a6-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="4a2a6-118">Antraštė</span><span class="sxs-lookup"><span data-stu-id="4a2a6-118">Heading</span></span> | <span data-ttu-id="4a2a6-119">Tekstas</span><span class="sxs-lookup"><span data-stu-id="4a2a6-119">Text</span></span> | <span data-ttu-id="4a2a6-120">Ši ypatybė nurodo pasirinktinę akordeono modulio teksto antraštę.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-120">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="4a2a6-121">Išplėsti viską</span><span class="sxs-lookup"><span data-stu-id="4a2a6-121">Expand All</span></span> | <span data-ttu-id="4a2a6-122">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="4a2a6-122">**True** or **False**</span></span> | <span data-ttu-id="4a2a6-123">Jei reikšmė nustatyta kaip **Teisinga**, išplėtimo / sutraukimo funkcija yra įjungta ir visi akordeono modulyje esantys elementai gali būti išplėsti ir sutraukti.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-123">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="4a2a6-124">Sąveikos stilius</span><span class="sxs-lookup"><span data-stu-id="4a2a6-124">Interaction Style</span></span> | <span data-ttu-id="4a2a6-125">**Nepriklausoma** arba **Išplėsti tik vieną elementą**</span><span class="sxs-lookup"><span data-stu-id="4a2a6-125">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="4a2a6-126">Ši ypatybė apibrėžia akordeono elementų sąveikos stilių.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-126">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="4a2a6-127">Jei vertė nustatyta kaip **Nepriklausoma**, kiekvieną akordeono elementą galima atskirai išplėsti arba sutraukti.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-127">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="4a2a6-128">Jei reikšmė nustatyta kaip **Išplėsti tik vieną elementą**, vienu metu galima išplėsti tik vieną elementą.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-128">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="4a2a6-129">Išplėtus elementus, anksčiau išplėsti elementai yra sutraukiami.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-129">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="4a2a6-130">Akordeono elementų modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="4a2a6-130">Accordion item module properties</span></span>

| <span data-ttu-id="4a2a6-131">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="4a2a6-131">Property name</span></span> | <span data-ttu-id="4a2a6-132">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="4a2a6-132">Values</span></span> | <span data-ttu-id="4a2a6-133">aprašymas</span><span class="sxs-lookup"><span data-stu-id="4a2a6-133">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="4a2a6-134">Kreipinys</span><span class="sxs-lookup"><span data-stu-id="4a2a6-134">Title</span></span> | <span data-ttu-id="4a2a6-135">Tekstas</span><span class="sxs-lookup"><span data-stu-id="4a2a6-135">Text</span></span> | <span data-ttu-id="4a2a6-136">Ši ypatybė nurodo akordeono elementų modulio pavadinimo tekstą.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-136">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="4a2a6-137">Pasirinkus pavadinimo sritį vartotojai gali išplėsti arba sutraukti sekciją.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-137">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="4a2a6-138">Išplėsti pagal numatytuosius parametrus</span><span class="sxs-lookup"><span data-stu-id="4a2a6-138">Expand by default</span></span> | <span data-ttu-id="4a2a6-139">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="4a2a6-139">**True** or **False**</span></span> | <span data-ttu-id="4a2a6-140">Jei vertė nustatyta kaip **Teisinga**, pagal numatytąsias nuostatas akordeono elementas išskleidžiamas, kai puslapis įkeliamas.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-140">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="4a2a6-141">Akordeono modulio įtraukimas į DUK puslapį</span><span class="sxs-lookup"><span data-stu-id="4a2a6-141">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="4a2a6-142">Norėdami į DUK puslapį įtraukti akordeono modulį ir nustatyti jo reikiamas ypatybes svetainių daryklėje, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-142">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="4a2a6-143">Eikite į **Puslapiai** ir naudokitės „Fabrikam“ rinkodaros šablonu (ar bet kokiu kitu šablonu be apribojimų), kad sukurtumėte naują puslapį su pavadinimu **Parduotuvės DUK**.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-143">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="4a2a6-144">**Numatytojo puslapio** vietoje **Pagrindinis** pasirinkite daugtaškį (**...**) ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-144">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4a2a6-145">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4a2a6-146">Vietoje **Konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-146">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4a2a6-147">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Akordeonas**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-147">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4a2a6-148">Akordeono modulio ypatybių srityje, šalia pieštuko simbolio, pasirinkite **Antraštė**.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-148">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="4a2a6-149">Dialogo lange **Antraštė**, dalyje **Antraštės tekstas**, įveskite **Dažnai užduodami klausimai**.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-149">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="4a2a6-150">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-150">Then select **OK**.</span></span>
1. <span data-ttu-id="4a2a6-151">Akordeono modulio ypatybių srityje pažymėkite žymės langelį **Rodyti „išplėsti viską“**, o tada laukelyje **Sąveikos stilius** pasirinkite **Nepriklausoma**.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-151">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="4a2a6-152">Vietoje **Akordeonas** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-152">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4a2a6-153">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Akordeono elementas**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-153">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4a2a6-154">Akordeono elementų modulio ypatybių srityje, dalyje **Pavadinimas**, įveskite pavadinimo tekstą (pavyzdžiui, **Kaip veikia grąžinimas?**).</span><span class="sxs-lookup"><span data-stu-id="4a2a6-154">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="4a2a6-155">Vietoje **Akordeono elementas** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-155">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4a2a6-156">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Teksto blokas**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-156">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4a2a6-157">Teksto bloko modulio ypatybių srityje įveskite teksto pastraipą (pvz., **Grąžinimai turi būti apdorojami skambučių centre. Dėl grąžinimo skambinkite 1-800-FABRIKAM. Gaminiams taikoma 30 dienų grąžinimo strategija. Dėl grąžinimo reikia kreiptis per šį laikotarpį.**).</span><span class="sxs-lookup"><span data-stu-id="4a2a6-157">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="4a2a6-158">Vietoje **Akordeonas** pridėkite dar kelis akordeono elementų modulius.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-158">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="4a2a6-159">Kiekviename akordeono elementų modulyje pridėkite tekstinio bloko modulį, kuriame yra turinio.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-159">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="4a2a6-160">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-160">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="4a2a6-161">Puslapyje bus rodomas akordeono modulis, kuriame yra jūsų įtrauktas turinys.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-161">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="4a2a6-162">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="4a2a6-162">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4a2a6-163">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="4a2a6-163">Additional resources</span></span>

[<span data-ttu-id="4a2a6-164">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="4a2a6-164">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4a2a6-165">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="4a2a6-165">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="4a2a6-166">Skirtuko modulis</span><span class="sxs-lookup"><span data-stu-id="4a2a6-166">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="4a2a6-167">Teksto bloko modulis</span><span class="sxs-lookup"><span data-stu-id="4a2a6-167">Text block module</span></span>](add-content-rich-block.md)
