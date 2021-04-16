---
title: Perjungti iš vieno tiekėjo dizaino į kitą
description: Šioje temoje aprašoma, kaip perjungti tiekėjo duomenų integravimą programose „Finance and Operations“ ir „Dataverse“.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5a18fed2eac4c120dca20a1d7797d047639275b9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750599"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="38115-103">Perjungimas iš vieno tiekėjo dizaino į kitą</span><span class="sxs-lookup"><span data-stu-id="38115-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="38115-104">Tiekėjo duomenų srautas</span><span class="sxs-lookup"><span data-stu-id="38115-104">Vendor data flow</span></span> 

<span data-ttu-id="38115-105">Jei nuspręsite naudoti **Paskyra** lentelę, kad galėtumėte išsaugoti tipo **Organizacija** tiekėjus, o lentelę **Kontaktai**, kad galėtumėte išsaugoti tipo **Asmuo** tiekėjus, sukonfigūruokite toliau nurodytas darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="38115-105">If you choose to use the **Account** table to store vendors of the **Organization** type and the **Contact** table to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="38115-106">Priešingu atveju ši konfigūracija nebūtina.</span><span class="sxs-lookup"><span data-stu-id="38115-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="38115-107">Tipo Organizacija tiekėjams naudokite išplėstinį tiekėjo dizainą</span><span class="sxs-lookup"><span data-stu-id="38115-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="38115-108">**„Dynamics365FinanceExtended“** sprendimų pakete yra toliau nurodyti darbo eigos proceso šablonai.</span><span class="sxs-lookup"><span data-stu-id="38115-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="38115-109">Sukurkite darbo eigą kiekvienam šablonui.</span><span class="sxs-lookup"><span data-stu-id="38115-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="38115-110">Tiekėjų kūrimas lentelėje Klientai</span><span class="sxs-lookup"><span data-stu-id="38115-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="38115-111">Tiekėjų kūrimas lentelėje Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="38115-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="38115-112">Tiekėjų naujinimas lentelėje Klientai</span><span class="sxs-lookup"><span data-stu-id="38115-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="38115-113">Tiekėjų naujinimas lentelėje Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="38115-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="38115-114">Norėdami sukurti naujus darbo eigos procesus, naudojant darbo eigos proceso šablonus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="38115-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="38115-115">Sukurkite darbo eigos procesą lentelei **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų kūrimas lentelėje Paskyros**.</span><span class="sxs-lookup"><span data-stu-id="38115-115">Create a workflow process for the **Vendor** table, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="38115-116">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="38115-116">Then select **OK**.</span></span> <span data-ttu-id="38115-117">Šioje darbo eigoje tvarkomas lentelės **Paskyra** tiekėjų kūrimo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="38115-117">This workflow handles the vendor creation scenario for the **Account** table.</span></span>

    ![Tiekėjų kūrimas darbo eigos proceso lentelėje Klientai](media/create_process.png)

2. <span data-ttu-id="38115-119">Sukurkite darbo eigos procesą lentelei **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Atnaujinti tiekėjus lentelėje Paskyros**.</span><span class="sxs-lookup"><span data-stu-id="38115-119">Create a workflow process for the **Vendor** table, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="38115-120">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="38115-120">Then select **OK**.</span></span> <span data-ttu-id="38115-121">Šioje darbo eigoje tvarkomas lentelės **Paskyra** tiekėjų naujinimo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="38115-121">This workflow handles the vendor update scenario for the **Account** table.</span></span>
3. <span data-ttu-id="38115-122">Sukurkite darbo eigos procesą lentelei **Paskyra** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų kūrimas lentelėje Tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="38115-122">Create a workflow process for the **Account** table, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="38115-123">Sukurkite darbo eigos procesą lentelei **Paskyra** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų atnaujinimas lentelėje Tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="38115-123">Create a workflow process for the **Account** table, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="38115-124">Priklausomai nuo poreikių, darbo eigas galite konfigūruoti kaip realaus laiko arba foninę darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="38115-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="38115-125">Norėdami sukonfigūruoti darbo eigą kaip foninę darbo eigą, pasirinkite **Konvertuoti į foninę darbo eigą**.</span><span class="sxs-lookup"><span data-stu-id="38115-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Mygtukas „Konvertuoti į foninę darbo eigą“](media/background_workflow.png)

6. <span data-ttu-id="38115-127">Aktyvinkite lentelėms **Paskyra** ir **Tiekėjas** sukurtas darbo eigas, kad pradėtumėte naudoti lentelę **Paskyra** ir galėtumėte saugoti tipo **Organizacija** informaciją tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="38115-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** table to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="38115-128">Tipo Asmuo tiekėjams naudokite išplėstinį tiekėjo dizainą</span><span class="sxs-lookup"><span data-stu-id="38115-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="38115-129">**„Dynamics365FinanceExtended“** sprendimų pakete yra toliau nurodyti darbo eigos proceso šablonai.</span><span class="sxs-lookup"><span data-stu-id="38115-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="38115-130">Sukurkite darbo eigą kiekvienam šablonui.</span><span class="sxs-lookup"><span data-stu-id="38115-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="38115-131">Tiekėjų kūrimas tipo Asmuo lentelėje Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="38115-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="38115-132">Tiekėjų kūrimas tipo Asmuo lentelėje Kontaktai</span><span class="sxs-lookup"><span data-stu-id="38115-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="38115-133">Tiekėjų naujinimas tipo Asmuo lentelėje Kontaktai</span><span class="sxs-lookup"><span data-stu-id="38115-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="38115-134">Tiekėjų naujinimas tipo Asmuo lentelėje Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="38115-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="38115-135">Norėdami sukurti naujus darbo eigos procesus, naudojant darbo eigos proceso šablonus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="38115-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="38115-136">Sukurkite darbo eigos procesą lentelei **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų kūrimas tipo Asmuo lentelėje Kontaktai**.</span><span class="sxs-lookup"><span data-stu-id="38115-136">Create a workflow process for the **Vendor** table, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="38115-137">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="38115-137">Then select **OK**.</span></span> <span data-ttu-id="38115-138">Ši darbo eiga tvarko lentelės **Kontaktai** tiekėjų kūrimo scenarijų.</span><span class="sxs-lookup"><span data-stu-id="38115-138">This workflow handles the vendor creation scenario for the **Contact** table.</span></span>
2. <span data-ttu-id="38115-139">Sukurkite darbo eigos procesą lentelei **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų atnaujinimas tipo Asmuo lentelėje Kontaktai**.</span><span class="sxs-lookup"><span data-stu-id="38115-139">Create a workflow process for the **Vendor** table, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="38115-140">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="38115-140">Then select **OK**.</span></span> <span data-ttu-id="38115-141">Ši darbo eiga tvarko lentelės **Kontaktai** teikėjų atnaujinimo scenarijų.</span><span class="sxs-lookup"><span data-stu-id="38115-141">This workflow handles the vendor update scenario for the **Contact** table.</span></span>
3. <span data-ttu-id="38115-142">Sukurkite darbo eigos procesą lentelei **Kontaktai** ir pasirinkite šabloną **Tiekėjų kūrimas tipo Asmuo lentelėje Tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="38115-142">Create a workflow process for the **Contact** table, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="38115-143">Sukurkite darbo eigos procesą lentelei **Kontaktai** ir pasirinkite šabloną **Tiekėjų atnaujinimas tipo Asmuo lentelėje Tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="38115-143">Create a workflow process for the **Contact** table, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="38115-144">Priklausomai nuo poreikių, darbo eigas galite konfigūruoti kaip realaus laiko arba foninę darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="38115-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="38115-145">Norėdami sukonfigūruoti darbo eigą kaip foninę darbo eigą, pasirinkite **Konvertuoti į foninę darbo eigą**.</span><span class="sxs-lookup"><span data-stu-id="38115-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="38115-146">Aktyvinkite lentelėms **Kontaktai** ir **Tiekėjas** sukurtas darbo eigas, kad pradėtumėte naudoti lentelę **Kontaktai** ir galėtumėte saugoti tipo **Asmuo** informaciją tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="38115-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** table to store information for vendors of the **Person** type.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]