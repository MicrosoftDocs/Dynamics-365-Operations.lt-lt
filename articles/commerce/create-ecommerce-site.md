---
title: El. prekybos svetainės kūrimas
description: Šioje temoje aprašomi veiksmai ir pateikiama informacija, reikalinga kuriant naują El. prekybos svetainę „Dynamics 365 Commerce“ svetainių daryklėje.
author: bicyclingfool
manager: AnnBe
ms.date: 01/23/2020
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
ms.openlocfilehash: 3d3d8a290f06d9734be21f2d59152acac6857506
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002018"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="6dab3-103">El. prekybos svetainės kūrimas</span><span class="sxs-lookup"><span data-stu-id="6dab3-103">Create an e-Commerce site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6dab3-104">Šioje temoje aprašomi veiksmai ir pateikiama informacija, reikalinga kuriant naują El. prekybos svetainę „Dynamics 365 Commerce“ svetainių daryklėje.</span><span class="sxs-lookup"><span data-stu-id="6dab3-104">This topic describes the steps and information required to create a new e-Commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="6dab3-105">Prieš kurdami savo El. prekybos svetainę, pirma turite sukurti naują svetainę svetainių daryklėje.</span><span class="sxs-lookup"><span data-stu-id="6dab3-105">Before you can start developing your e-Commerce site, you must first establish a new site in site builder.</span></span> 


<span data-ttu-id="6dab3-106">Norėdami pradėti kurti savo el. prekybos svetainę, pirmiausia turite sukurti naują svetainę svetainės kūrimo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="6dab3-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="6dab3-107">Kad galėtumėte kurti naują svetainę, programoje „Commerce“ reikia sukurti bent vieną internetinę parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="6dab3-107">Before you can create a new site, at least one online store must be created in Commerce.</span></span> 


## <a name="set-up-your-site"></a><span data-ttu-id="6dab3-108">Svetainės nustatymas</span><span class="sxs-lookup"><span data-stu-id="6dab3-108">Set up your site</span></span>

<span data-ttu-id="6dab3-109">Norėdami nustatyti svetainę, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6dab3-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="6dab3-110">Atidarykite svetainių daryklės aplinką.</span><span class="sxs-lookup"><span data-stu-id="6dab3-110">Open the site builder environment.</span></span> <span data-ttu-id="6dab3-111">„Microsoft Lifecycle Services“ (LCS) „Commerce“ aplinkos funkcijų puslapyje pateikiamas saitas į svetainių daryklę.</span><span class="sxs-lookup"><span data-stu-id="6dab3-111">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="6dab3-112">Svetainės kūrimo aplinkos pagrindiniame puslapyje pasirinkite **Nauja svetainė**.</span><span class="sxs-lookup"><span data-stu-id="6dab3-112">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="6dab3-113">Dialogo lange **Nauja svetainė** nurodykite tolesnę informaciją.</span><span class="sxs-lookup"><span data-stu-id="6dab3-113">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="6dab3-114">Laukas</span><span class="sxs-lookup"><span data-stu-id="6dab3-114">Field</span></span>                               | <span data-ttu-id="6dab3-115">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="6dab3-115">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="6dab3-116">Svetainės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="6dab3-116">Site name</span></span>                           | <span data-ttu-id="6dab3-117">Įveskite rodomą svetainės pavadinimą, kuris turi būti naudojamas svetainės kūrimo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="6dab3-117">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="6dab3-118">Šis pavadinimas matomas tik kūrimo aplinkoje ir klientams rodomas nebus.</span><span class="sxs-lookup"><span data-stu-id="6dab3-118">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="6dab3-119">Svetainės administratoriaus saugos grupė</span><span class="sxs-lookup"><span data-stu-id="6dab3-119">Site administrator's security group</span></span> | <span data-ttu-id="6dab3-120">Nurodykite „Microsoft Azure Active Directory“ („Azure AD“) saugos grupę, valdančią vartotojus, kuriems šioje svetainėje priskirtas svetainės administratoriaus vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="6dab3-120">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="6dab3-121">Numatytasis kanalas (valdymo vieneto numeris)</span><span class="sxs-lookup"><span data-stu-id="6dab3-121">Default channel (operating unit number)</span></span> | <span data-ttu-id="6dab3-122">Pasirinkite internetinę parduotuvę, kurios el. parduotuvė bus ši svetainė.</span><span class="sxs-lookup"><span data-stu-id="6dab3-122">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="6dab3-123">Jei norite, kad el. prekybos svetainė palaikytų kelias internetines parduotuves, po to, kai svetainė nustatoma, turite parduotuves susieti su savo svetaine dalyje **Svetainės parametrai**.</span><span class="sxs-lookup"><span data-stu-id="6dab3-123">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="6dab3-124">Numatytoji kalba</span><span class="sxs-lookup"><span data-stu-id="6dab3-124">Default language</span></span>                            | <span data-ttu-id="6dab3-125">Nurodykite numatytąją šios internetinės parduotuvės ir rinkos kalbą.</span><span class="sxs-lookup"><span data-stu-id="6dab3-125">Specify the default language for this online store and market.</span></span> <span data-ttu-id="6dab3-126">Internetinė parduotuvė gali palaikyti kelias kalbas.</span><span class="sxs-lookup"><span data-stu-id="6dab3-126">An online store can support multiple languages.</span></span> <span data-ttu-id="6dab3-127">Jei norite, kad ši arba kita internetinė parduotuvė palaikytų kelias kalbas, tai turite sukonfigūruoti dalyje **Svetainės parametrai**, kai svetainė nustatyta.</span><span class="sxs-lookup"><span data-stu-id="6dab3-127">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="6dab3-128">Domenas</span><span class="sxs-lookup"><span data-stu-id="6dab3-128">Domain</span></span>                              | <span data-ttu-id="6dab3-129">Pasirinkite domeno vardą, kuris bus šios internetinės parduotuvės domenas.</span><span class="sxs-lookup"><span data-stu-id="6dab3-129">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="6dab3-130">Jei sprendime LCS nekonfigūravote jokių domenų, šį lauką galite palikti tuščią.</span><span class="sxs-lookup"><span data-stu-id="6dab3-130">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="6dab3-131">Sukonfigūravę domeną sprendime LCS, jį turite įtraukti į internetinę parduotuvę dalyje **Svetainės parametrai**.</span><span class="sxs-lookup"><span data-stu-id="6dab3-131">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="6dab3-132">Maršrutas</span><span class="sxs-lookup"><span data-stu-id="6dab3-132">Path</span></span>                              | <span data-ttu-id="6dab3-133">Kai jūsų svetainė palaiko daugiau nei vieną tam tikro domeno vardo kalbą, naudodami kelio lauką sukurkite unikalų to domeno ir kalbos derinio svetainės URL.</span><span class="sxs-lookup"><span data-stu-id="6dab3-133">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="6dab3-134">Jei kalba, kurią nurodėte lauke **Numatytoji kalba**, yra vienintelė palaikoma šio domeno kalba arba toliau bus numatytoji kalba jums svetainę lokalizavus papildomomis kalbomis, rekomenduojame šį lauką palikti tuščią.</span><span class="sxs-lookup"><span data-stu-id="6dab3-134">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="6dab3-135">Sukūrę svetainę, patikrinti, ar ji susieta su internetine parduotuve, galite pasirinkdami skirtuką **Produktai**. Turėtumėte matyti produktų asortimentą, priskirtą internetinei parduotuvei.</span><span class="sxs-lookup"><span data-stu-id="6dab3-135">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="6dab3-136">Taip pat galite naudoti viršutinėje kairiojoje puslapio dalyje esantį išplečiamąjį meniu ir priskirtus produktus pasiekti pagal kategoriją.</span><span class="sxs-lookup"><span data-stu-id="6dab3-136">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6dab3-137">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="6dab3-137">Additional resources</span></span>

[<span data-ttu-id="6dab3-138">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="6dab3-138">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="6dab3-139">Naujos e. prekybos svetainės visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="6dab3-139">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="6dab3-140">Interneto svetainės susiejimas su kanalu</span><span class="sxs-lookup"><span data-stu-id="6dab3-140">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="6dab3-141">„Robots.txt” failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="6dab3-141">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="6dab3-142">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="6dab3-142">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="6dab3-143">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="6dab3-143">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="6dab3-144">Parduotuvės nustatymo pagal vietą įgalinimas</span><span class="sxs-lookup"><span data-stu-id="6dab3-144">Enable location-based store detection</span></span>](enable-store-detection.md)
