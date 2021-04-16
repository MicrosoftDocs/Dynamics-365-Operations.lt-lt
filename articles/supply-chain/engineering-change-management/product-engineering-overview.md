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
ms.openlocfilehash: 964db71efc9dc81d60199e37de8668de9d667496
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842086"
---
# <a name="engineering-change-management-overview"></a><span data-ttu-id="8185b-103">Inžinerijos keitimo valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="8185b-103">Engineering change management overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a><span data-ttu-id="8185b-104">Funkcijos santrauka</span><span class="sxs-lookup"><span data-stu-id="8185b-104">Feature summary</span></span>

<span data-ttu-id="8185b-105">Šiandien gamintojams reikia stipraus produkto duomenų valdymo, versijos kontrolės ir inžinerijos keitimo valdymo siekiant sėkmės pasaulyje su nuolatos besitraukiančio gyvenimo ciklo produktais, padidinta kokybe ir patikimumo reikalavimais bei padidintu dėmesiu produkto saugai.</span><span class="sxs-lookup"><span data-stu-id="8185b-105">Today's manufacturers require strong product data management, version control, and engineering change management to succeed in a world of constantly shrinking product lifecycles, increased quality and reliability requirements, and an increased focus on product safety.</span></span>

<span data-ttu-id="8185b-106">Inžinerijos keitimo valdymas suteikia struktūrą ir discipliną produkto duomenų valdymo procesui ir suteikia produktams galimybę būti nustatytiems, išleistiems ir peržiūrėtiems valdymo būdu, kurį palaiko darbo eigos.</span><span class="sxs-lookup"><span data-stu-id="8185b-106">Engineering change management brings structure and discipline to the product data management process, and enables products to be defined, released, and revised in a controlled manner that is supported by workflows.</span></span><span data-ttu-id="8185b-107"> Per produkto versijas ir inžinerijos keitimo valdymą galite registruoti, įvertinti poveikį ir taikyti inžinerijos keitimus per visą produkto gyvavimo ciklą.</span><span class="sxs-lookup"><span data-stu-id="8185b-107"> Through product versions and engineering change management, you can document, assess the impact of, and apply engineering changes throughout the whole lifecycle of a product.</span></span>

<span data-ttu-id="8185b-108">Inžinerijos keitimo valdymo apžvalgą, kuri padeda jums planuoti ir valdyti produkto versijas ir valdyti produkto gyvenimo ciklus bei inžinerijos pokyčius.</span><span class="sxs-lookup"><span data-stu-id="8185b-108">Engineering change management helps you plan and manage product versioning, and manage product lifecycles and engineering changes.</span></span> <span data-ttu-id="8185b-109">Pateikiamas pagrindinių savybių sąrašas:</span><span class="sxs-lookup"><span data-stu-id="8185b-109">Here is a list of its main features:</span></span>

- <span data-ttu-id="8185b-110">Produkto versijos</span><span class="sxs-lookup"><span data-stu-id="8185b-110">Product versioning</span></span>
- <span data-ttu-id="8185b-111">Pagerintos produkto išleidimo funkcijos, kurios leidžia jums išlaikyti produkto pagrindinius duomenis viename juridiniame asmenyje (inžinerijos bendrovėje) ir publikuoti visiškai sukonfigūruotą išleistą produktą kitiems juridiniams asmenims.</span><span class="sxs-lookup"><span data-stu-id="8185b-111">Enhanced product release functionality that lets you maintain product master data in one legal entity (the engineering company) and publish the fully configured released product to other legal entities</span></span>
- <span data-ttu-id="8185b-112">Patvirtinimo taisyklės, kurioms reikalingas informacija yra įvedama prieš tai, kai įjungiama produkto versija (pasirengimo patikros)</span><span class="sxs-lookup"><span data-stu-id="8185b-112">Rules for validating that required information is entered before a product version is activated (readiness checks)</span></span>
- <span data-ttu-id="8185b-113">Pagerintas produkto gyvavimo ciklo valdymas per gerai išdirbtą valdymą, kai išleistas produktas gali būti naudojamas konkrečiuose verslo procesuose</span><span class="sxs-lookup"><span data-stu-id="8185b-113">Improved product lifecycle management through fine-grained control over when a released product can be used in specific business processes</span></span>
- <span data-ttu-id="8185b-114">Inžinerijos pokyčio reikalavimai palaikomi darbo eigų</span><span class="sxs-lookup"><span data-stu-id="8185b-114">Engineering change requests that are supported by workflows</span></span>
- <span data-ttu-id="8185b-115">Inžinerijos pokyčio užsakymai palaikomi darbo eigų</span><span class="sxs-lookup"><span data-stu-id="8185b-115">Engineering change orders that are supported by workflows</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

<span data-ttu-id="8185b-116">Ankstesnis vaizdo įrašas ([Keitimo valdymo galimybės „Dynamics 365 Supply Chain Management“](https://youtu.be/N313FqvRuBc)) yra įtrauktos į [„Finance and Operations“ grojaraštį](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) prieinamą „YouTube“.</span><span class="sxs-lookup"><span data-stu-id="8185b-116">The preceding video ([Change management capabilities in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a><span data-ttu-id="8185b-117">Įjunkite jūsų sistemos inžinerinių pakeitimų valdymą ir versijos dimensijų funkcijas</span><span class="sxs-lookup"><span data-stu-id="8185b-117">Turn on the engineering change management and version dimension features for your system</span></span>

<span data-ttu-id="8185b-118">Prieš pradedami naudoti inžinerinių pakeitimų valdymą, turite įgalinti ir funkciją *Inžinerinių pakeitimų valdymas*, ir jos konfigūracijos raktą.</span><span class="sxs-lookup"><span data-stu-id="8185b-118">Before you can use engineering change management, you must enable both the *Engineering Change Management* feature and its configuration key.</span></span> <span data-ttu-id="8185b-119">Jei norite sekti operacijų produktų versijos dimensiją (pasirinktinai), turite įgalinti funkciją *Produkto versijos dimensija* ir jos konfigūracijos raktą.</span><span class="sxs-lookup"><span data-stu-id="8185b-119">If you also want to track the version dimension of products in transactions (optional), then you must also enable the *Product version dimension* feature and its configuration key.</span></span>

<span data-ttu-id="8185b-120">Pirmiausia įjunkite šias funkcijas atlikdami toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8185b-120">First, turn on the features by following these steps.</span></span>

1. <span data-ttu-id="8185b-121">Eikite į [Funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8185b-121">Go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
1. <span data-ttu-id="8185b-122">Tikrinkite naujinimus.</span><span class="sxs-lookup"><span data-stu-id="8185b-122">Check for updates.</span></span>
1. <span data-ttu-id="8185b-123">Įjunkite funkciją pavadinimu **Inžinerijos keitimo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="8185b-123">Turn on the feature that is named **Engineering Change Management**.</span></span>
1. <span data-ttu-id="8185b-124">Jei norite ją naudoti, įjunkite ir funkciją, kuri pavadinta **Produkto dimensijos versija**.</span><span class="sxs-lookup"><span data-stu-id="8185b-124">If you want to use it, then also turn on the feature that is named **Product dimension version**.</span></span>

<span data-ttu-id="8185b-125">Tada įjunkite konfigūracijos raktus atlikdami toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8185b-125">Next, turn on the configuration keys by following these steps.</span></span>

1. <span data-ttu-id="8185b-126">Įdėkite savo sistemą į priežiūros režimą kaip aprašyta [Priežiūros režime](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="8185b-126">Put your system into maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="8185b-127">Eikite į **Sistemos administravimas \> Sąranka \> Licencijos konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="8185b-127">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="8185b-128">Išplėskite mazgą **Prekyba**</span><span class="sxs-lookup"><span data-stu-id="8185b-128">Expand the **Trade** node</span></span>
1. <span data-ttu-id="8185b-129">Pažymėkite žymės langelį **Inžinerinių pakeitimų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="8185b-129">Select the **Engineering Change Management** check box.</span></span>
1. <span data-ttu-id="8185b-130">Jei norite jį naudoti, tada taip pat pažymėkite žymės langelį **Produkto dimensija – versija**.</span><span class="sxs-lookup"><span data-stu-id="8185b-130">If you want to use it, then also select the **Product dimension - Version** check box.</span></span>
1. <span data-ttu-id="8185b-131">Išjunkite priežiūros režimą kaip aprašyta [Priežiūros režime](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="8185b-131">Turn off maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
