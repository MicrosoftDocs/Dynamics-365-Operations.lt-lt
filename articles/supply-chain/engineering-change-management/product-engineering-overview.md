---
title: Inžinerijos keitimo valdymo apžvalga
description: Ši tema pateikia inžinerijos keitimo valdymo apžvalgą, kuri padeda jums planuoti ir valdyti produkto versijas ir valdyti produkto gyvenimo ciklus bei inžinerijos pokyčius.
author: t-benebo
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: f1aa04b472eaef7ed398f08a05d46bac2d589561
ms.sourcegitcommit: 9f32389715b226c11e74c53547527e0a8b51e300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514355"
---
# <a name="engineering-change-management-overview"></a><span data-ttu-id="fd394-103">Inžinerijos keitimo valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="fd394-103">Engineering change management overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a><span data-ttu-id="fd394-104">Funkcijos santrauka</span><span class="sxs-lookup"><span data-stu-id="fd394-104">Feature summary</span></span>

<span data-ttu-id="fd394-105">Šiandien gamintojams reikia stipraus produkto duomenų valdymo, versijos kontrolės ir inžinerijos keitimo valdymo siekiant sėkmės pasaulyje su nuolatos besitraukiančio gyvenimo ciklo produktais, padidinta kokybe ir patikimumo reikalavimais bei padidintu dėmesiu produkto saugai.</span><span class="sxs-lookup"><span data-stu-id="fd394-105">Today's manufacturers require strong product data management, version control, and engineering change management to succeed in a world of constantly shrinking product lifecycles, increased quality and reliability requirements, and an increased focus on product safety.</span></span>

<span data-ttu-id="fd394-106">Inžinerijos keitimo valdymas suteikia struktūrą ir discipliną produkto duomenų valdymo procesui ir suteikia produktams galimybę būti nustatytiems, išleistiems ir peržiūrėtiems valdymo būdu, kurį palaiko darbo eigos.</span><span class="sxs-lookup"><span data-stu-id="fd394-106">Engineering change management brings structure and discipline to the product data management process, and enables products to be defined, released, and revised in a controlled manner that is supported by workflows.</span></span><span data-ttu-id="fd394-107">Per produkto versijas ir inžinerijos keitimo valdymą galite registruoti, įvertinti poveikį ir taikyti inžinerijos keitimus per visą produkto gyvavimo ciklą.</span><span class="sxs-lookup"><span data-stu-id="fd394-107"> Through product versions and engineering change management, you can document, assess the impact of, and apply engineering changes throughout the whole lifecycle of a product.</span></span>

<span data-ttu-id="fd394-108">Inžinerijos keitimo valdymo apžvalgą, kuri padeda jums planuoti ir valdyti produkto versijas ir valdyti produkto gyvenimo ciklus bei inžinerijos pokyčius.</span><span class="sxs-lookup"><span data-stu-id="fd394-108">Engineering change management helps you plan and manage product versioning, and manage product lifecycles and engineering changes.</span></span> <span data-ttu-id="fd394-109">Pateikiamas pagrindinių savybių sąrašas:</span><span class="sxs-lookup"><span data-stu-id="fd394-109">Here is a list of its main features:</span></span>

- <span data-ttu-id="fd394-110">Produkto versijos</span><span class="sxs-lookup"><span data-stu-id="fd394-110">Product versioning</span></span>
- <span data-ttu-id="fd394-111">Pagerintos produkto išleidimo funkcijos, kuriso leidžia jums išlaikyti produkto pagrindinius duomenis viename juridiniame asmenyje (inžinerijso bendrovėje) ir publikuoti visiškai sukonfigūruotą išleistą produktą kitiems juridiniams asmenims.</span><span class="sxs-lookup"><span data-stu-id="fd394-111">Enhanced product release functionality that lets you maintain product master data in one legal entity (the engineering company) and publish the fully configured released product to other legal entities</span></span>
- <span data-ttu-id="fd394-112">Patvirtinimo taisyklės, kurioms reikalingas informacija yra įvedama prieš tai, kai įjungiama produkto versija (pasirengimo patikros)</span><span class="sxs-lookup"><span data-stu-id="fd394-112">Rules for validating that required information is entered before a product version is activated (readiness checks)</span></span>
- <span data-ttu-id="fd394-113">Pagerintas produkto gyvavimo ciklo valdymas per gerai išdirbtą valdymą, kai išleistas produktas gali būti naudojamas konkrečiuose verslo procesuose</span><span class="sxs-lookup"><span data-stu-id="fd394-113">Improved product lifecycle management through fine-grained control over when a released product can be used in specific business processes</span></span>
- <span data-ttu-id="fd394-114">Inžinerijos pokyčio reikalavimai palaikomi darbo eigų</span><span class="sxs-lookup"><span data-stu-id="fd394-114">Engineering change requests that are supported by workflows</span></span>
- <span data-ttu-id="fd394-115">Inžinerijos pokyčio užsakymai palaikomi darbo eigų</span><span class="sxs-lookup"><span data-stu-id="fd394-115">Engineering change orders that are supported by workflows</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

<span data-ttu-id="fd394-116">Ankstesnis vaizdo įrašas ([Keitimo valdymo galimybės „Dynamics 365 Supply Chain Management“](https://youtu.be/N313FqvRuBc)) yra įtrauktos į [„Finance and Operations“ grojaraštį](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) prieinamą „YouTube“.</span><span class="sxs-lookup"><span data-stu-id="fd394-116">The preceding video ([Change management capabilities in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="turn-on-engineering-change-management-for-your-system"></a><span data-ttu-id="fd394-117">Įjunkite inžinerijos keitimo valdymą savo sistemai</span><span class="sxs-lookup"><span data-stu-id="fd394-117">Turn on engineering change management for your system</span></span>

<span data-ttu-id="fd394-118">Pirmiausia įjunkite inžinerijos keitimo valdymą šiais žingsniais.</span><span class="sxs-lookup"><span data-stu-id="fd394-118">First, turn on engineering change management by following these steps.</span></span>

1. <span data-ttu-id="fd394-119">Eikite į [Funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fd394-119">Go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
1. <span data-ttu-id="fd394-120">Tikrinkite naujinimus.</span><span class="sxs-lookup"><span data-stu-id="fd394-120">Check for updates.</span></span>
1. <span data-ttu-id="fd394-121">Įjunkite funkciją pavadinimu **Inžinerijos keitimo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="fd394-121">Turn on the feature that is named **Engineering Change Management**.</span></span>

<span data-ttu-id="fd394-122">Po to įjunkite **Inžinerijos keitimo valdymo** konfigūravimo mygtuką šiais žingsniais.</span><span class="sxs-lookup"><span data-stu-id="fd394-122">Next, turn on the **Engineering Change Management** configuration key by following these steps.</span></span>

1. <span data-ttu-id="fd394-123">Įdėkite savo sistemą į priežiūros režimą kaip aprašyta [Priežiūros režime](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="fd394-123">Put your system into maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="fd394-124">Eikite į **Sistemos administravimas \> Sąranka \> Licencijos konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="fd394-124">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="fd394-125">Išplėskite **Prekybos** mazgą ir pasirinkite **Inžinerijos keitimo valdymo** žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="fd394-125">Expand the **Trade** node, and select the **Engineering Change Management** check box.</span></span>
1. <span data-ttu-id="fd394-126">Išjunkite priežiūros režimą kaip aprašyta [Priežiūros režime](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="fd394-126">Turn off maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
