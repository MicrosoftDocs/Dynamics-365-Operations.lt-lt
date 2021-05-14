---
title: Inžinerijos keitimo valdymo apžvalga
description: Ši tema pateikia inžinerijos keitimo valdymo apžvalgą, kuri padeda jums planuoti ir valdyti produkto versijas ir valdyti produkto gyvenimo ciklus bei inžinerijos pokyčius.
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d7c0839ffbea80904ca12d1cba7ba9880f721cdd
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947525"
---
# <a name="engineering-change-management-overview"></a><span data-ttu-id="e2675-103">Inžinerijos keitimo valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="e2675-103">Engineering change management overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a><span data-ttu-id="e2675-104">Funkcijos santrauka</span><span class="sxs-lookup"><span data-stu-id="e2675-104">Feature summary</span></span>

<span data-ttu-id="e2675-105">Šiandien gamintojams reikia stipraus produkto duomenų valdymo, versijos kontrolės ir inžinerijos keitimo valdymo siekiant sėkmės pasaulyje su nuolatos besitraukiančio gyvenimo ciklo produktais, padidinta kokybe ir patikimumo reikalavimais bei padidintu dėmesiu produkto saugai.</span><span class="sxs-lookup"><span data-stu-id="e2675-105">Today's manufacturers require strong product data management, version control, and engineering change management to succeed in a world of constantly shrinking product lifecycles, increased quality and reliability requirements, and an increased focus on product safety.</span></span>

<span data-ttu-id="e2675-106">Inžinerijos keitimo valdymas suteikia struktūrą ir discipliną produkto duomenų valdymo procesui ir suteikia produktams galimybę būti nustatytiems, išleistiems ir peržiūrėtiems valdymo būdu, kurį palaiko darbo eigos.</span><span class="sxs-lookup"><span data-stu-id="e2675-106">Engineering change management brings structure and discipline to the product data management process, and enables products to be defined, released, and revised in a controlled manner that is supported by workflows.</span></span><span data-ttu-id="e2675-107"> Per produkto versijas ir inžinerijos keitimo valdymą galite registruoti, įvertinti poveikį ir taikyti inžinerijos keitimus per visą produkto gyvavimo ciklą.</span><span class="sxs-lookup"><span data-stu-id="e2675-107"> Through product versions and engineering change management, you can document, assess the impact of, and apply engineering changes throughout the whole lifecycle of a product.</span></span>

<span data-ttu-id="e2675-108">Inžinerijos keitimo valdymo apžvalgą, kuri padeda jums planuoti ir valdyti produkto versijas ir valdyti produkto gyvenimo ciklus bei inžinerijos pokyčius.</span><span class="sxs-lookup"><span data-stu-id="e2675-108">Engineering change management helps you plan and manage product versioning, and manage product lifecycles and engineering changes.</span></span> <span data-ttu-id="e2675-109">Pateikiamas pagrindinių savybių sąrašas:</span><span class="sxs-lookup"><span data-stu-id="e2675-109">Here is a list of its main features:</span></span>

- <span data-ttu-id="e2675-110">Produkto versijos</span><span class="sxs-lookup"><span data-stu-id="e2675-110">Product versioning</span></span>
- <span data-ttu-id="e2675-111">Pagerintos produkto išleidimo funkcijos, kurios leidžia jums išlaikyti produkto pagrindinius duomenis viename juridiniame asmenyje (inžinerijos bendrovėje) ir publikuoti visiškai sukonfigūruotą išleistą produktą kitiems juridiniams asmenims.</span><span class="sxs-lookup"><span data-stu-id="e2675-111">Enhanced product release functionality that lets you maintain product master data in one legal entity (the engineering company) and publish the fully configured released product to other legal entities</span></span>
- <span data-ttu-id="e2675-112">Patvirtinimo taisyklės, kurioms reikalingas informacija yra įvedama prieš tai, kai įjungiama produkto versija (pasirengimo patikros)</span><span class="sxs-lookup"><span data-stu-id="e2675-112">Rules for validating that required information is entered before a product version is activated (readiness checks)</span></span>
- <span data-ttu-id="e2675-113">Pagerintas produkto gyvavimo ciklo valdymas per gerai išdirbtą valdymą, kai išleistas produktas gali būti naudojamas konkrečiuose verslo procesuose</span><span class="sxs-lookup"><span data-stu-id="e2675-113">Improved product lifecycle management through fine-grained control over when a released product can be used in specific business processes</span></span>
- <span data-ttu-id="e2675-114">Inžinerijos pokyčio reikalavimai palaikomi darbo eigų</span><span class="sxs-lookup"><span data-stu-id="e2675-114">Engineering change requests that are supported by workflows</span></span>
- <span data-ttu-id="e2675-115">Inžinerijos pokyčio užsakymai palaikomi darbo eigų</span><span class="sxs-lookup"><span data-stu-id="e2675-115">Engineering change orders that are supported by workflows</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

<span data-ttu-id="e2675-116">Ankstesnis vaizdo įrašas ([Keitimo valdymo galimybės „Dynamics 365 Supply Chain Management“](https://youtu.be/N313FqvRuBc)) yra įtrauktos į [„Finance and Operations“ grojaraštį](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) prieinamą „YouTube“.</span><span class="sxs-lookup"><span data-stu-id="e2675-116">The preceding video ([Change management capabilities in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a><span data-ttu-id="e2675-117">Įjunkite jūsų sistemos inžinerinių pakeitimų valdymą ir versijos dimensijų funkcijas</span><span class="sxs-lookup"><span data-stu-id="e2675-117">Turn on the engineering change management and version dimension features for your system</span></span>

<span data-ttu-id="e2675-118">Prieš pradedami naudoti inžinerinių pakeitimų valdymą, turite įgalinti ir funkciją *Inžinerinių pakeitimų valdymas*, ir jos konfigūracijos raktą.</span><span class="sxs-lookup"><span data-stu-id="e2675-118">Before you can use engineering change management, you must enable both the *Engineering Change Management* feature and its configuration key.</span></span> <span data-ttu-id="e2675-119">Jei norite sekti operacijų produktų versijos dimensiją (pasirinktinai), turite įgalinti funkciją *Produkto versijos dimensija* ir jos konfigūracijos raktą.</span><span class="sxs-lookup"><span data-stu-id="e2675-119">If you also want to track the version dimension of products in transactions (optional), then you must also enable the *Product version dimension* feature and its configuration key.</span></span>

<span data-ttu-id="e2675-120">Pirmiausia įjunkite šias funkcijas atlikdami toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e2675-120">First, turn on the features by following these steps.</span></span>

1. <span data-ttu-id="e2675-121">Eikite į darbo [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) srityje.</span><span class="sxs-lookup"><span data-stu-id="e2675-121">Go to the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace.</span></span>
1. <span data-ttu-id="e2675-122">Tikrinkite naujinimus.</span><span class="sxs-lookup"><span data-stu-id="e2675-122">Check for updates.</span></span>
1. <span data-ttu-id="e2675-123">Įjunkite funkciją pavadinimu **Inžinerijos keitimo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="e2675-123">Turn on the feature that is named **Engineering Change Management**.</span></span>
1. <span data-ttu-id="e2675-124">Jei norite ją naudoti, įjunkite ir funkciją, kuri pavadinta **Produkto dimensijos versija**.</span><span class="sxs-lookup"><span data-stu-id="e2675-124">If you want to use it, then also turn on the feature that is named **Product dimension version**.</span></span>

<span data-ttu-id="e2675-125">Tada įjunkite konfigūracijos raktus atlikdami toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e2675-125">Next, turn on the configuration keys by following these steps.</span></span>

1. <span data-ttu-id="e2675-126">Įdėkite savo sistemą į priežiūros režimą kaip aprašyta [Priežiūros režime](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="e2675-126">Put your system into maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="e2675-127">Eikite į **Sistemos administravimas \> Sąranka \> Licencijos konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="e2675-127">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="e2675-128">Išplėskite mazgą **Prekyba**.</span><span class="sxs-lookup"><span data-stu-id="e2675-128">Expand the **Trade** node.</span></span>
1. <span data-ttu-id="e2675-129">Įgalinkite pagrindinės priemonės konfigūracijos raktą pažymėdami žymės **langelį Inžinerijos** keitimo valdymas.</span><span class="sxs-lookup"><span data-stu-id="e2675-129">Enable the configuration key for the main feature by selecting the **Engineering Change Management** check box.</span></span> <span data-ttu-id="e2675-130">(Nebūtina išplėsti mazgo, nebent jūs taip pat norite išjungti vieną ar abi jo anttrines funkcijas.)</span><span class="sxs-lookup"><span data-stu-id="e2675-130">(It isn't necessary to expand the node unless you also want to disable one or both of its sub-features.)</span></span>
1. <span data-ttu-id="e2675-131">Jei norite taip pat naudoti versijos matmenis, tada taip pat pažymėkite žymės langelį **Produkto dimensija – versija**.</span><span class="sxs-lookup"><span data-stu-id="e2675-131">If you also want to use the version dimension, then select the **Product dimension - Version** check box.</span></span> <span data-ttu-id="e2675-132">(Šis žymės langelis yra žemyn sąraše, o ne įdėtas po **„Engineering Change Management“** mazgas.)</span><span class="sxs-lookup"><span data-stu-id="e2675-132">(This check box is further down the list, not nested under the **Engineering Change Management** node.)</span></span>
1. <span data-ttu-id="e2675-133">Išjunkite priežiūros režimą kaip aprašyta [Priežiūros režime](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="e2675-133">Turn off maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2675-134">Nuo 2022 m. balandžio mėn. „Engineering Change Management“ ir produkto dimensijos licencijos raktai – versija bus įgalinta pagal numatytuosius nustatymus visoms naujiems **diegimams, tačiau prireikus vis tiek galėsite** jas **išjungti**.</span><span class="sxs-lookup"><span data-stu-id="e2675-134">Starting in April 2022, the license keys for both **Engineering Change Management** and **Product dimension - Version** will be enabled by default for all new installations, but you will still be able to disable them if needed.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
