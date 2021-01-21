---
title: Kliento portalo įdiegimas, nustatymas ir atnaujinimas
description: Šioje temoje pateikiama licencijavimo informacija ir kliento portalo nustatymo instrukcijos.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 0343100362c4d7bc3e09334fb7890919bdb84941
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435613"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="12cda-103">Kliento portalo įdiegimas, nustatymas ir atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="12cda-103">Install, set up, and update the Customer portal</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="12cda-104">Licencijavimo reikalavimai</span><span class="sxs-lookup"><span data-stu-id="12cda-104">Licensing requirements</span></span>

<span data-ttu-id="12cda-105">Norėdami naudoti kliento portalą, turite turėti toliau išvardytas licencijas.</span><span class="sxs-lookup"><span data-stu-id="12cda-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="12cda-106">**„Power Apps“ portalai** – ši licencija reikalinga kliento portalo prieglobai.</span><span class="sxs-lookup"><span data-stu-id="12cda-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="12cda-107">Portalai licencijuojami remiantis naudojimu.</span><span class="sxs-lookup"><span data-stu-id="12cda-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="12cda-108">Norėdami gauti daugiau informacijos, žr. [„Power Apps“ portalų licencijavimo reikalavimus](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span><span class="sxs-lookup"><span data-stu-id="12cda-108">For more information, see the [Power Apps portals licensing requirements](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="12cda-109">**Dvigubas rašymas** – turite turėti būtinas licencijas, kad galėtumėte įjungti dvigubo rašymo funkciją „Supply Chain Management“ objektams.</span><span class="sxs-lookup"><span data-stu-id="12cda-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management entities.</span></span> <span data-ttu-id="12cda-110">Prireikus daugiau informacijos, žr. [dvigubo rašymo sistemos reikalavimai](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span><span class="sxs-lookup"><span data-stu-id="12cda-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="12cda-111">Priklausomybė nuo dvigubo rašymo ir „Power Apps“ portalų</span><span class="sxs-lookup"><span data-stu-id="12cda-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="12cda-112">Kliento portalas yra priklausomas nuo „Power Apps“ portalų ir dvigubo rašymo, kaip parodyta tolesnėje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="12cda-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

<span data-ttu-id="12cda-113">![Kliento portalo priklausomybės](media/customer-portal-elements.png "Kliento portalo priklausomybes")</span><span class="sxs-lookup"><span data-stu-id="12cda-113">![Customer portal dependencies](media/customer-portal-elements.png "Customer portal dependencies")</span></span>

<span data-ttu-id="12cda-114">Skirtingai nei kitos „Supply Chain Management“ funkcijos, kliento portalo šablonas yra „Power Apps“ portaluose.</span><span class="sxs-lookup"><span data-stu-id="12cda-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="12cda-115">Todėl klientų portalą riboja „Power Apps“ portalų teikiamos funkcijos bei galimybės ir dvigubą rašymą naudojantys objektai.</span><span class="sxs-lookup"><span data-stu-id="12cda-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the entities in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a><span data-ttu-id="12cda-116">Reikalingi nustatymo veiksmai, norint įjungti kliento portalą</span><span class="sxs-lookup"><span data-stu-id="12cda-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="12cda-117">Įsitikinę, kad turite reikiamas licencijas, galite nustatyti dvigubo rašymo funkciją, kaip nurodyta [dvigubo rašymo pradinio sinchronizavimo instrukcijose](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="12cda-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span></span>

<span data-ttu-id="12cda-118">Būtinai įjunkite toliau išvardytus susiejimus su objektais dvigubo rašymo funkcijoje.</span><span class="sxs-lookup"><span data-stu-id="12cda-118">Be sure to enable the following entity mappings in dual-write:</span></span>

- <span data-ttu-id="12cda-119">Pardavimo užsakymo antraštė</span><span class="sxs-lookup"><span data-stu-id="12cda-119">Sales Order Header</span></span>
- <span data-ttu-id="12cda-120">Pardavimo užsakymo informacija</span><span class="sxs-lookup"><span data-stu-id="12cda-120">Sales Order Details</span></span>
- <span data-ttu-id="12cda-121">Sąskaitos</span><span class="sxs-lookup"><span data-stu-id="12cda-121">Accounts</span></span>
- <span data-ttu-id="12cda-122">Kontaktai</span><span class="sxs-lookup"><span data-stu-id="12cda-122">Contacts</span></span>
- <span data-ttu-id="12cda-123">Produktai</span><span class="sxs-lookup"><span data-stu-id="12cda-123">Products</span></span>

<span data-ttu-id="12cda-124">Atlikę šį nustatymą, galite paruošti kliento portalo šabloną.</span><span class="sxs-lookup"><span data-stu-id="12cda-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="12cda-125">Kliento portalo rengimas</span><span class="sxs-lookup"><span data-stu-id="12cda-125">Provision the Customer portal</span></span>

<span data-ttu-id="12cda-126">Prieš pradėdami įsitikinkite, kad jau atlikote [reikiamus nustatymo veiksmus](#required-setup).</span><span class="sxs-lookup"><span data-stu-id="12cda-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="12cda-127">Tada atlikite toliau pateiktus veiksmus, kad parengtumėte kliento portalą.</span><span class="sxs-lookup"><span data-stu-id="12cda-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="12cda-128">Eikite į [make.powerapps.com](https://make.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="12cda-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="12cda-129">Įsitikinkite, kad naudojate aplinką, kurioje įjungėte dvigubo rašymo funkciją.</span><span class="sxs-lookup"><span data-stu-id="12cda-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="12cda-130">Skirtuke **Kurti** slinkite iki **Pradėti nuo šablono** dalies ir pasirinkite šabloną, pavadintą **Kliento portalas**.</span><span class="sxs-lookup"><span data-stu-id="12cda-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Customer Portal**.</span></span>
4. <span data-ttu-id="12cda-131">Vadovaukitės ekrane pateikiamais nurodymais.</span><span class="sxs-lookup"><span data-stu-id="12cda-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="12cda-132">Užbaigus parengimą, kliento portalą galima pasiekti puslapyje **Pagrindinis**, dalyje **Jūsų programos**.</span><span class="sxs-lookup"><span data-stu-id="12cda-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="12cda-133">Jei dvigubo rašymo sprendimas neįdiegtas aplinkoje, su kuria dirbate, jums bus parodytas klaidos pranešimas ir kliento portalas nebus parengtas.</span><span class="sxs-lookup"><span data-stu-id="12cda-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="12cda-134">Kliento portalo atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="12cda-134">Update the Customer portal</span></span>

<span data-ttu-id="12cda-135">Vėliau į kliento portalą galima įtraukti daugiau funkcijų.</span><span class="sxs-lookup"><span data-stu-id="12cda-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="12cda-136">Bet kokie pakeitimai, kuriuos „Microsoft“ atlieka pagrindiniams komponentams, bus automatiškai rodomi jūsų aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="12cda-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="12cda-137">Tačiau svetainėje, kuri parengta jūsų aplinkoje, konfigūravimo duomenų pakeitimai nebus automatiškai rodomi.</span><span class="sxs-lookup"><span data-stu-id="12cda-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="12cda-138">Jums reikės rankiniu būdu pritaikyti šiuos pakeitimus – gauti kodą iš naujo šablono ir sujungti jį su parengta svetaine.</span><span class="sxs-lookup"><span data-stu-id="12cda-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12cda-139">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="12cda-139">Additional resources</span></span>

<span data-ttu-id="12cda-140">Norėdami sužinoti, kaip nustatyti ir tinkinti kliento portalą, pirmiausia peržiūrėkite toliau pateiktą pagrindinių technologijų dokumentaciją.</span><span class="sxs-lookup"><span data-stu-id="12cda-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="12cda-141">„Power Apps“ portalų dokumentacija</span><span class="sxs-lookup"><span data-stu-id="12cda-141">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="12cda-142">Dvigubo rašymo dokumentacija</span><span class="sxs-lookup"><span data-stu-id="12cda-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="12cda-143">Norėdami veiksmingai tvarkyti savo portalus, turite suprasti „Power Apps“ portalus ir „Common Data Service“ ciklą.</span><span class="sxs-lookup"><span data-stu-id="12cda-143">To effectively manage your portals, you must understand the Power Apps portals and Common Data Service lifecycle.</span></span> <span data-ttu-id="12cda-144">Daugiau informacijos ieškokite šiuose ištekliuose:</span><span class="sxs-lookup"><span data-stu-id="12cda-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="12cda-145">Apie portalo ciklą</span><span class="sxs-lookup"><span data-stu-id="12cda-145">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="12cda-146">Portalo naujovinimas</span><span class="sxs-lookup"><span data-stu-id="12cda-146">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="12cda-147">Portalo konfigūracijos perkėlimas</span><span class="sxs-lookup"><span data-stu-id="12cda-147">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="12cda-148">Sprendimo ciklo valdymas – „Dynamics 365 for Customer Engagement“ programos</span><span class="sxs-lookup"><span data-stu-id="12cda-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)