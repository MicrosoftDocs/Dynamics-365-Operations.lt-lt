---
title: E. prekybos svetainės kūrimas
description: Šioje temoje aprašomos užduotys, susijusios su naujos el. prekybos svetainės kūrimu programoje „Dynamics 365 Commerce“.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 54259d3f5dfd8c8e1ff2caaadfac497cc0e133e0
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945840"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="c3944-103">E. prekybos svetainės kūrimas</span><span class="sxs-lookup"><span data-stu-id="c3944-103">Create an e-Commerce site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c3944-104">Šioje temoje aprašomos užduotys, susijusios su naujos el. prekybos svetainės kūrimu programoje „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="c3944-104">This topic describes the tasks that are associated with the creation of a new e-Commerce site in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c3944-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="c3944-105">Overview</span></span>

<span data-ttu-id="c3944-106">Norėdami pradėti kurti savo el. prekybos svetainę, pirmiausia turite sukurti naują svetainę svetainės kūrimo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="c3944-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="c3944-107">Kad galėtumėte kurti naują svetainę, programoje „Dynamics 365 Retail“ reikia sukurti bent vieną internetinę parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="c3944-107">Before you can create a new site, at least one online store must be created in Dynamics 365 Retail.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="c3944-108">Svetainės nustatymas</span><span class="sxs-lookup"><span data-stu-id="c3944-108">Set up your site</span></span>

<span data-ttu-id="c3944-109">Norėdami nustatyti svetainę, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c3944-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="c3944-110">Sprendime „Microsoft Lifecycle Services“ (LCS) pasirinkite svetainės kūrimo aplinkos saitą.</span><span class="sxs-lookup"><span data-stu-id="c3944-110">In Microsoft Lifecycle Services (LCS), select the link for the site authoring environment.</span></span> 
1. <span data-ttu-id="c3944-111">Svetainės kūrimo aplinkos pagrindiniame puslapyje pasirinkite **Nauja svetainė**.</span><span class="sxs-lookup"><span data-stu-id="c3944-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="c3944-112">Dialogo lange **Nauja svetainė** nurodykite tolesnę informaciją.</span><span class="sxs-lookup"><span data-stu-id="c3944-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="c3944-113">Laukas</span><span class="sxs-lookup"><span data-stu-id="c3944-113">Field</span></span>                               | <span data-ttu-id="c3944-114">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="c3944-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="c3944-115">Svetainės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="c3944-115">Site name</span></span>                           | <span data-ttu-id="c3944-116">Įveskite rodomą svetainės pavadinimą, kuris turi būti naudojamas svetainės kūrimo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="c3944-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="c3944-117">Šis pavadinimas matomas tik kūrimo aplinkoje ir klientams rodomas nebus.</span><span class="sxs-lookup"><span data-stu-id="c3944-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="c3944-118">Svetainės administratoriaus saugos grupė</span><span class="sxs-lookup"><span data-stu-id="c3944-118">Site administrator's security group</span></span> | <span data-ttu-id="c3944-119">Nurodykite „Microsoft Azure Active Directory“ („Azure AD“) saugos grupę, valdančią vartotojus, kuriems šioje svetainėje priskirtas svetainės administratoriaus vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="c3944-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="c3944-120">Numatytasis kanalas (valdymo vieneto numeris)</span><span class="sxs-lookup"><span data-stu-id="c3944-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="c3944-121">Pasirinkite internetinę parduotuvę, kurios el. parduotuvė bus ši svetainė.</span><span class="sxs-lookup"><span data-stu-id="c3944-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="c3944-122">Jei norite, kad el. prekybos svetainė palaikytų kelias internetines parduotuves, po to, kai svetainė nustatoma, turite parduotuves susieti su savo svetaine dalyje **Svetainės parametrai**.</span><span class="sxs-lookup"><span data-stu-id="c3944-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="c3944-123">Numatytoji kalba</span><span class="sxs-lookup"><span data-stu-id="c3944-123">Default language</span></span>                            | <span data-ttu-id="c3944-124">Nurodykite numatytąją šios internetinės parduotuvės ir rinkos kalbą.</span><span class="sxs-lookup"><span data-stu-id="c3944-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="c3944-125">Internetinė parduotuvė gali palaikyti kelias kalbas.</span><span class="sxs-lookup"><span data-stu-id="c3944-125">An online store can support multiple languages.</span></span> <span data-ttu-id="c3944-126">Jei norite, kad ši arba kita internetinė parduotuvė palaikytų kelias kalbas, tai turite sukonfigūruoti dalyje **Svetainės parametrai**, kai svetainė nustatyta.</span><span class="sxs-lookup"><span data-stu-id="c3944-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="c3944-127">Domenas</span><span class="sxs-lookup"><span data-stu-id="c3944-127">Domain</span></span>                              | <span data-ttu-id="c3944-128">Pasirinkite domeno vardą, kuris bus šios internetinės parduotuvės domenas.</span><span class="sxs-lookup"><span data-stu-id="c3944-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="c3944-129">Jei sprendime LCS nekonfigūravote jokių domenų, šį lauką galite palikti tuščią.</span><span class="sxs-lookup"><span data-stu-id="c3944-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="c3944-130">Sukonfigūravę domeną sprendime LCS, jį turite įtraukti į internetinę parduotuvę dalyje **Svetainės parametrai**.</span><span class="sxs-lookup"><span data-stu-id="c3944-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="c3944-131">Maršrutas</span><span class="sxs-lookup"><span data-stu-id="c3944-131">Path</span></span>                              | <span data-ttu-id="c3944-132">Kai jūsų svetainė palaiko daugiau nei vieną tam tikro domeno vardo kalbą, naudodami kelio lauką sukurkite unikalų to domeno ir kalbos derinio svetainės URL.</span><span class="sxs-lookup"><span data-stu-id="c3944-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="c3944-133">Jei kalba, kurią nurodėte lauke **Numatytoji kalba**, yra vienintelė palaikoma šio domeno kalba arba toliau bus numatytoji kalba jums svetainę lokalizavus papildomomis kalbomis, rekomenduojame šį lauką palikti tuščią.</span><span class="sxs-lookup"><span data-stu-id="c3944-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="c3944-134">Sukūrę svetainę, patikrinti, ar ji susieta su internetine parduotuve, galite pasirinkdami skirtuką **Produktai**. Turėtumėte matyti produktų asortimentą, priskirtą internetinei parduotuvei.</span><span class="sxs-lookup"><span data-stu-id="c3944-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="c3944-135">Taip pat galite naudoti viršutinėje kairiojoje puslapio dalyje esantį išplečiamąjį meniu ir priskirtus produktus pasiekti pagal kategoriją.</span><span class="sxs-lookup"><span data-stu-id="c3944-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3944-136">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c3944-136">Additional resources</span></span>

[<span data-ttu-id="c3944-137">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="c3944-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="c3944-138">Naujos e. prekybos svetainės visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="c3944-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="c3944-139">Interneto svetainės susiejimas su kanalu</span><span class="sxs-lookup"><span data-stu-id="c3944-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="c3944-140">„Robots.txt” failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="c3944-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="c3944-141">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="c3944-141">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="c3944-142">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="c3944-142">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="c3944-143">Parduotuvės nustatymo pagal vietą įgalinimas</span><span class="sxs-lookup"><span data-stu-id="c3944-143">Enable location-based store detection</span></span>](enable-store-detection.md)
