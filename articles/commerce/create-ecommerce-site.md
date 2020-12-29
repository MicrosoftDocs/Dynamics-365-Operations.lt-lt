---
title: Sukurkite e-komercijos saitą
description: Ši tema aprašo žingsnius ir informaciją, kurie yra būtini norint sukurti e-komercijos saitą „Dynamics 365 Commerce“ saito kūrimo įrankyje.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
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
ms.openlocfilehash: 7d552f29fd8f52b512a7c21b36b0a814cac50646
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517189"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="06a76-103">Sukurkite e-komercijos saitą</span><span class="sxs-lookup"><span data-stu-id="06a76-103">Create an e-commerce site</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="06a76-104">Ši tema aprašo žingsnius ir informaciją, kurie yra būtini norint sukurti e-komercijos saitą „Dynamics 365 Commerce“ saito kūrimo įrankyje.</span><span class="sxs-lookup"><span data-stu-id="06a76-104">This topic describes the steps and information required to create a new e-commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="06a76-105">Kai jūsų suteikiate licenciją „Dynamics 365 Commerce“ pajėgumams, sait kūrimo įrankis bus aprūpintas pradžios saitu, kurį galėsite naudoti pagal jūsų turimo saito pagrindus.</span><span class="sxs-lookup"><span data-stu-id="06a76-105">When you license the Dynamics 365 Commerce capabilities, site builder will be provisioned with a starter site that you can use as a basis for your own site.</span></span> <span data-ttu-id="06a76-106">Tačiau, jei norite pradėti nuo nulio, arba, jei norite sukurti antrą svetainę, turite sukurti naują svetainę svetainės kūrimo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="06a76-106">However, if you want to start from scratch or if you want to establish a second site, you will need to establish a new site in the site authoring environment.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="06a76-107">Svetainės nustatymas</span><span class="sxs-lookup"><span data-stu-id="06a76-107">Set up your site</span></span>

<span data-ttu-id="06a76-108">Norėdami nustatyti svetainę, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="06a76-108">To set up your site, do the following.</span></span>

1. <span data-ttu-id="06a76-109">Atidarykite svetainių daryklės aplinką.</span><span class="sxs-lookup"><span data-stu-id="06a76-109">Open the site builder environment.</span></span> <span data-ttu-id="06a76-110">„Microsoft Lifecycle Services“ (LCS) „Commerce“ aplinkos funkcijų puslapyje pateikiamas saitas į svetainių daryklę.</span><span class="sxs-lookup"><span data-stu-id="06a76-110">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="06a76-111">Svetainės kūrimo aplinkos pagrindiniame puslapyje pasirinkite **Nauja svetainė**.</span><span class="sxs-lookup"><span data-stu-id="06a76-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="06a76-112">Dialogo lange **Nauja svetainė** nurodykite tolesnę informaciją.</span><span class="sxs-lookup"><span data-stu-id="06a76-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="06a76-113">Laukas</span><span class="sxs-lookup"><span data-stu-id="06a76-113">Field</span></span>                               | <span data-ttu-id="06a76-114">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="06a76-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="06a76-115">Svetainės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="06a76-115">Site name</span></span>                           | <span data-ttu-id="06a76-116">Įveskite rodomą svetainės pavadinimą, kuris turi būti naudojamas svetainės kūrimo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="06a76-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="06a76-117">Šis pavadinimas matomas tik kūrimo aplinkoje ir klientams rodomas nebus.</span><span class="sxs-lookup"><span data-stu-id="06a76-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="06a76-118">Svetainės administratoriaus saugos grupė</span><span class="sxs-lookup"><span data-stu-id="06a76-118">Site administrator's security group</span></span> | <span data-ttu-id="06a76-119">Nurodykite „Microsoft Azure Active Directory“ („Azure AD“) saugos grupę, valdančią vartotojus, kuriems šioje svetainėje priskirtas svetainės administratoriaus vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="06a76-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="06a76-120">Numatytasis kanalas (valdymo vieneto numeris)</span><span class="sxs-lookup"><span data-stu-id="06a76-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="06a76-121">Pasirinkite internetinę parduotuvę, kurios el. parduotuvė bus ši svetainė.</span><span class="sxs-lookup"><span data-stu-id="06a76-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="06a76-122">Jei norite, kad jūsų e-komercijos saitas palaikytų keletą interneto parduotuvių, turite susieti parduotuves su jūsų saitu **Saito nustatymuose** nustačius saitą.</span><span class="sxs-lookup"><span data-stu-id="06a76-122">If you want your e-commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="06a76-123">Numatytoji kalba</span><span class="sxs-lookup"><span data-stu-id="06a76-123">Default language</span></span>                            | <span data-ttu-id="06a76-124">Nurodykite numatytąją šios internetinės parduotuvės ir rinkos kalbą.</span><span class="sxs-lookup"><span data-stu-id="06a76-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="06a76-125">Internetinė parduotuvė gali palaikyti kelias kalbas.</span><span class="sxs-lookup"><span data-stu-id="06a76-125">An online store can support multiple languages.</span></span> <span data-ttu-id="06a76-126">Jei norite, kad ši arba kita internetinė parduotuvė palaikytų kelias kalbas, tai turite sukonfigūruoti dalyje **Svetainės parametrai**, kai svetainė nustatyta.</span><span class="sxs-lookup"><span data-stu-id="06a76-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="06a76-127">Domenas</span><span class="sxs-lookup"><span data-stu-id="06a76-127">Domain</span></span>                              | <span data-ttu-id="06a76-128">Pasirinkite domeno vardą, kuris bus šios internetinės parduotuvės domenas.</span><span class="sxs-lookup"><span data-stu-id="06a76-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="06a76-129">Jei sprendime LCS nekonfigūravote jokių domenų, šį lauką galite palikti tuščią.</span><span class="sxs-lookup"><span data-stu-id="06a76-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="06a76-130">Sukonfigūravę domeną sprendime LCS, jį turite įtraukti į internetinę parduotuvę dalyje **Svetainės parametrai**.</span><span class="sxs-lookup"><span data-stu-id="06a76-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="06a76-131">Maršrutas</span><span class="sxs-lookup"><span data-stu-id="06a76-131">Path</span></span>                              | <span data-ttu-id="06a76-132">Kai jūsų svetainė palaiko daugiau nei vieną tam tikro domeno vardo kalbą, naudodami kelio lauką sukurkite unikalų to domeno ir kalbos derinio svetainės URL.</span><span class="sxs-lookup"><span data-stu-id="06a76-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="06a76-133">Jei kalba, kurią nurodėte lauke **Numatytoji kalba**, yra vienintelė palaikoma šio domeno kalba arba toliau bus numatytoji kalba jums svetainę lokalizavus papildomomis kalbomis, rekomenduojame šį lauką palikti tuščią.</span><span class="sxs-lookup"><span data-stu-id="06a76-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="06a76-134">Sukūrę svetainę, patikrinti, ar ji susieta su internetine parduotuve, galite pasirinkdami skirtuką **Produktai**. Turėtumėte matyti produktų asortimentą, priskirtą internetinei parduotuvei.</span><span class="sxs-lookup"><span data-stu-id="06a76-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="06a76-135">Taip pat galite naudoti viršutinėje kairiojoje puslapio dalyje esantį išplečiamąjį meniu ir priskirtus produktus pasiekti pagal kategoriją.</span><span class="sxs-lookup"><span data-stu-id="06a76-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06a76-136">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="06a76-136">Additional resources</span></span>

[<span data-ttu-id="06a76-137">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="06a76-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="06a76-138">Talpinkite naują e-komercijos nuomotoją</span><span class="sxs-lookup"><span data-stu-id="06a76-138">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="06a76-139">Susiekite „Dynamics 365 Commerce“ saitą su interneto kanalu</span><span class="sxs-lookup"><span data-stu-id="06a76-139">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="06a76-140">„robots.txt” failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="06a76-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="06a76-141">Masinis URL peradresavimų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="06a76-141">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="06a76-142">B2C nuomotojo nustatymas „Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="06a76-142">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="06a76-143">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="06a76-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="06a76-144">„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="06a76-144">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="06a76-145">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="06a76-145">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="06a76-146">Parduotuvės nustatymo pagal vietą įgalinimas</span><span class="sxs-lookup"><span data-stu-id="06a76-146">Enable location-based store detection</span></span>](enable-store-detection.md)
