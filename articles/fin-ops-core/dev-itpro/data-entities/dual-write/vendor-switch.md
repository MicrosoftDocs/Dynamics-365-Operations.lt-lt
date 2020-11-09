---
title: Perjungti iš vieno tiekėjo dizaino į kitą
description: Šioje temoje aprašoma, kaip perjungti tiekėjo duomenų integravimą programose „Finance and Operations“ ir „Common Data Service“.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 0ecc401706911f8b92146b95bb6415185df8b451
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997557"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="c14a7-103">Perjungti iš vieno tiekėjo dizaino į kitą</span><span class="sxs-lookup"><span data-stu-id="c14a7-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="c14a7-104">Tiekėjo duomenų srautas</span><span class="sxs-lookup"><span data-stu-id="c14a7-104">Vendor data flow</span></span> 

<span data-ttu-id="c14a7-105">Jei nuspręsite naudoti objektą **Klientas** , kad galėtumėte išsaugoti tipo **Organizacija** tiekėjus, o objektą **Kontaktas** , kad galėtumėte išsaugoti tipo **Asmuo** tiekėjus, sukonfigūruokite toliau nurodytas darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="c14a7-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="c14a7-106">Priešingu atveju ši konfigūracija nebūtina.</span><span class="sxs-lookup"><span data-stu-id="c14a7-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="c14a7-107">Tipo Organizacija tiekėjams naudokite išplėstinį tiekėjo dizainą</span><span class="sxs-lookup"><span data-stu-id="c14a7-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="c14a7-108">**„Dynamics365FinanceExtended“** sprendimų pakete yra toliau nurodyti darbo eigos proceso šablonai.</span><span class="sxs-lookup"><span data-stu-id="c14a7-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="c14a7-109">Sukurkite darbo eigą kiekvienam šablonui.</span><span class="sxs-lookup"><span data-stu-id="c14a7-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="c14a7-110">Tiekėjų kūrimas objekte Klientai</span><span class="sxs-lookup"><span data-stu-id="c14a7-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="c14a7-111">Tiekėjų kūrimas objekte Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="c14a7-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="c14a7-112">Tiekėjų naujinimas objekte Klientai</span><span class="sxs-lookup"><span data-stu-id="c14a7-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="c14a7-113">Tiekėjų naujinimas objekte Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="c14a7-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="c14a7-114">Norėdami sukurti naujus darbo eigos procesus, naudojant darbo eigos proceso šablonus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c14a7-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="c14a7-115">Sukurkite darbo eigos procesą objektui **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų kūrimas objekte Klientai**.</span><span class="sxs-lookup"><span data-stu-id="c14a7-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="c14a7-116">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c14a7-116">Then select **OK**.</span></span> <span data-ttu-id="c14a7-117">Šia darbo eiga tvarkomas objekto **Klientas** tiekėjų kūrimo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="c14a7-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Tiekėjų kūrimas darbo eigos proceso objekte Klientas](media/create_process.png)

2. <span data-ttu-id="c14a7-119">Sukurkite darbo eigos procesą objektui **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų naujinimas objekte Klientai**.</span><span class="sxs-lookup"><span data-stu-id="c14a7-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="c14a7-120">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c14a7-120">Then select **OK**.</span></span> <span data-ttu-id="c14a7-121">Šia darbo eiga tvarkomas objekto **Klientas** tiekėjų naujinimo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="c14a7-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="c14a7-122">Sukurkite darbo eigos procesą objektui **Klientas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų kūrimas objekte Tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="c14a7-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="c14a7-123">Sukurkite darbo eigos procesą objektui **Klientas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų naujinimas objekte Tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="c14a7-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="c14a7-124">Priklausomai nuo poreikių, darbo eigas galite konfigūruoti kaip realaus laiko arba foninę darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="c14a7-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="c14a7-125">Norėdami sukonfigūruoti darbo eigą kaip foninę darbo eigą, pasirinkite **Konvertuoti į foninę darbo eigą**.</span><span class="sxs-lookup"><span data-stu-id="c14a7-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Mygtukas „Konvertuoti į foninę darbo eigą“](media/background_workflow.png)

6. <span data-ttu-id="c14a7-127">Aktyvinkite objektams **Klientas** ir **Tiekėjas** sukurtas darbo eigas, kad pradėtumėte naudoti objektą **Klientas** ir galėtumėte saugoti tipo **Organizacija** informaciją tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="c14a7-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="c14a7-128">Tipo Asmuo tiekėjams naudokite išplėstinį tiekėjo dizainą</span><span class="sxs-lookup"><span data-stu-id="c14a7-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="c14a7-129">**„Dynamics365FinanceExtended“** sprendimų pakete yra toliau nurodyti darbo eigos proceso šablonai.</span><span class="sxs-lookup"><span data-stu-id="c14a7-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="c14a7-130">Sukurkite darbo eigą kiekvienam šablonui.</span><span class="sxs-lookup"><span data-stu-id="c14a7-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="c14a7-131">Tiekėjų kūrimas tipo Asmuo objekte Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="c14a7-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="c14a7-132">Tiekėjų kūrimas tipo Asmuo objekte Kontaktai</span><span class="sxs-lookup"><span data-stu-id="c14a7-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="c14a7-133">Tiekėjų naujinimas tipo Asmuo objekte Kontaktai</span><span class="sxs-lookup"><span data-stu-id="c14a7-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="c14a7-134">Tiekėjų naujinimas tipo Asmuo objekte Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="c14a7-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="c14a7-135">Norėdami sukurti naujus darbo eigos procesus, naudojant darbo eigos proceso šablonus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c14a7-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="c14a7-136">Sukurkite darbo eigos procesą objektui **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų kūrimas tipo Asmuo objekte Kontaktai**.</span><span class="sxs-lookup"><span data-stu-id="c14a7-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="c14a7-137">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c14a7-137">Then select **OK**.</span></span> <span data-ttu-id="c14a7-138">Ši darbo eiga valdo objekto **Kontaktai** kūrimo scenarijų.</span><span class="sxs-lookup"><span data-stu-id="c14a7-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="c14a7-139">Sukurkite darbo eigos procesą objektui **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų naujinimas tipo Asmuo objekte Kontaktai**.</span><span class="sxs-lookup"><span data-stu-id="c14a7-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="c14a7-140">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c14a7-140">Then select **OK**.</span></span> <span data-ttu-id="c14a7-141">Ši darbo eiga valdo objekto **Kontaktai** naujinimo scenarijų.</span><span class="sxs-lookup"><span data-stu-id="c14a7-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="c14a7-142">Sukurkite darbo eigos procesą objektui **Kontaktas** ir pasirinkite šabloną **Tiekėjų kūrimas tipo Asmuo objekte Tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="c14a7-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="c14a7-143">Sukurkite darbo eigos procesą objektui **Kontaktas** ir pasirinkite šabloną **Tiekėjų naujinimas tipo Asmuo objekte Tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="c14a7-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="c14a7-144">Priklausomai nuo poreikių, darbo eigas galite konfigūruoti kaip realaus laiko arba foninę darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="c14a7-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="c14a7-145">Norėdami sukonfigūruoti darbo eigą kaip foninę darbo eigą, pasirinkite **Konvertuoti į foninę darbo eigą**.</span><span class="sxs-lookup"><span data-stu-id="c14a7-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="c14a7-146">Aktyvinkite objektams **Kontaktas** ir **Tiekėjas** sukurtas darbo eigas, kad pradėtumėte naudoti objektą **Kontaktas** ir galėtumėte saugoti tipo **Asmuo** informaciją tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="c14a7-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
