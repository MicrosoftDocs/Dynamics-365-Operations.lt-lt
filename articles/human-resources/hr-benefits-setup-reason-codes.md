---
title: Nustatyti priežasčių kodus
description: „Dynamics 365 Human Resources“ naudojami priežasčių kodus, siekiant paaiškinti, kodėl keičiasi darbuotojo išmokos.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae82c8312d344f5380adec8413766304681a0a05
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113537"
---
# <a name="set-up-reason-codes"></a><span data-ttu-id="1d677-103">Nustatyti priežasčių kodus</span><span class="sxs-lookup"><span data-stu-id="1d677-103">Set up reason codes</span></span>

<span data-ttu-id="1d677-104">„Dynamics 365 Human Resources“ naudojami priežasčių kodus, siekiant paaiškinti, kodėl keičiasi darbuotojo išmokos.</span><span class="sxs-lookup"><span data-stu-id="1d677-104">Dynamics 365 Human Resources uses reason codes to explain why an employee’s benefits are changing.</span></span>

> [!NOTE]
> <span data-ttu-id="1d677-105">Nuo 2021 m. sausio mėnesio priežasties kodai yra perkeliami į **Personalo valdymo** darbo sritį, o ne **Išmokų valdymo** darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="1d677-105">As of January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="1d677-106">Dėl daugiau informacijos, žr. [Rankiniu būdu perkelti priežasties kodus į personalo valdymą](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span><span class="sxs-lookup"><span data-stu-id="1d677-106">For more information, see [Manually migrate reason codes to Personnel management](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span></span>

## <a name="create-reason-codes"></a><span data-ttu-id="1d677-107">Priežasčių kodų kūrimas</span><span class="sxs-lookup"><span data-stu-id="1d677-107">Create reason codes</span></span>

1. <span data-ttu-id="1d677-108">Darbo srityje **Personalo valdymas** (ar **Išmokų valdymas** darbo srityje, jei jūsų priežasties kodai nebuvo perkelti), rinkitės **Nuorodos** ir tada rinkitės **Priežasties kodai**.</span><span class="sxs-lookup"><span data-stu-id="1d677-108">In the **Personnel management** workspace (or **Benefits management** workspace if your reason codes haven't yet migrated), select **Links**, and then select **Reason codes**.</span></span>

2. <span data-ttu-id="1d677-109">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1d677-109">Select **New**.</span></span>

3. <span data-ttu-id="1d677-110">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="1d677-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="1d677-111">Laukas</span><span class="sxs-lookup"><span data-stu-id="1d677-111">Field</span></span> | <span data-ttu-id="1d677-112">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="1d677-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1d677-113">**Tikslinės paskirties šifras**</span><span class="sxs-lookup"><span data-stu-id="1d677-113">**Reason code**</span></span> | <span data-ttu-id="1d677-114">Unikalus pavadinimas, skirtas nustatyti priežastį, dėl kurios darbuotojas galėtų keisti išmokų plano registraciją.</span><span class="sxs-lookup"><span data-stu-id="1d677-114">A unique name to identify the reason an employee would change a benefit plan enrollment.</span></span> |
   | <span data-ttu-id="1d677-115">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="1d677-115">**Description**</span></span> | <span data-ttu-id="1d677-116">Priežasties kodo aprašas.</span><span class="sxs-lookup"><span data-stu-id="1d677-116">A description of the reason code.</span></span> |

4. <span data-ttu-id="1d677-117">Skyriuje **Taikomi scenarijai**, nustatykite **Išmokų valdymas** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="1d677-117">Under **Applicable scenarios**, set **Benefits management** to **Yes**.</span></span> <span data-ttu-id="1d677-118">(Netaikoma, jei jūsų priežasties kodai dar nebuvo perkelti į **Personalo valdymo** dardbo sritį.)</span><span class="sxs-lookup"><span data-stu-id="1d677-118">(Not applicable if your reason codes haven't yet migrated to the **Personnel management** workspace.)</span></span>

5. <span data-ttu-id="1d677-119">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1d677-119">Select **Save**.</span></span>

## <a name="manually-migrate-reason-codes-to-personnel-management"></a><span data-ttu-id="1d677-120">Rankiniu būdu perkelti priežasties kodus į personalo valdymą</span><span class="sxs-lookup"><span data-stu-id="1d677-120">Manually migrate reason codes to Personnel management</span></span>

<span data-ttu-id="1d677-121">2021 m. sausio mėnesį priežasties kodai yra perkeliami į **Personalo valdymo** darbo sritį, o ne **Išmokų valdymo** darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="1d677-121">In January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="1d677-122">Didžio dalis kodo duomenų buvo automatiniu būdu perkelti į jūsų aplinką.</span><span class="sxs-lookup"><span data-stu-id="1d677-122">Most reason code data will automatically migrate in your environment.</span></span> <span data-ttu-id="1d677-123">Kai kurie priežasties kodo duomenys gali būti neperkelti.</span><span class="sxs-lookup"><span data-stu-id="1d677-123">Some reason code data might not migrate.</span></span> <span data-ttu-id="1d677-124">Pavyzdžiui, priežasties kodai dabar turi daugiausiai 15 ženklų, dėl to, visi ilgesni nei 15 ženklų priežasties kodai nebus automatiniu būdu perkelti.</span><span class="sxs-lookup"><span data-stu-id="1d677-124">For example, reason codes now have a 15-character maximum, so any reason codes longer than 15 characters won't migrate automatically.</span></span>

<span data-ttu-id="1d677-125">Matysite reklaminę juostą **Nuorodos** puslapyje **Išmokų valdymas** darbo srityje, kuri jus informuos apie perkelimą ir ar bet kurie priežasties kodai nepersikėlė.</span><span class="sxs-lookup"><span data-stu-id="1d677-125">You'll see a banner on the **Links** page of the **Benefits management** workspace informing you about the migration and whether any reason codes didn't migrate.</span></span>

1. <span data-ttu-id="1d677-126">Rinkitės **Priežasties kodai** dėl išsamios informacijos apie perkėlimo būseną.</span><span class="sxs-lookup"><span data-stu-id="1d677-126">Select **Reason codes** for details about migration status.</span></span>

   <span data-ttu-id="1d677-127">[![Priežasčių kodai](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span><span class="sxs-lookup"><span data-stu-id="1d677-127">[![Reason codes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span></span>

2. <span data-ttu-id="1d677-128">Rinkitės kodo priežastį, kuri nepersikėlė.</span><span class="sxs-lookup"><span data-stu-id="1d677-128">Select a reason code that failed to migrate.</span></span>

   <span data-ttu-id="1d677-129">[![Priežasties kodo perkėlimo būsena](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span><span class="sxs-lookup"><span data-stu-id="1d677-129">[![Reason code migration status](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span></span>

3. <span data-ttu-id="1d677-130">Rinkitės **Perkelti priežasties kodą**.</span><span class="sxs-lookup"><span data-stu-id="1d677-130">Select **Migrate reason code**.</span></span>

   <span data-ttu-id="1d677-131">[![Perkelti priežasties kodą](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span><span class="sxs-lookup"><span data-stu-id="1d677-131">[![Migrate reason code](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span></span>

4. <span data-ttu-id="1d677-132">Juostoje **išmokos priežasties kodo perkėlimas** turite dvi parinktis sudaryti žemėlapį personalo valdymo priežasties kodui:</span><span class="sxs-lookup"><span data-stu-id="1d677-132">In the **Benefit reason code migration** pane, you have two options for mapping to a Personnel management reason code:</span></span>

   - <span data-ttu-id="1d677-133">Norėdami naudoti esantį priežasties kodą personalo valdyme, rinkitės vieną iš esančių **Naudoti esantį priežasties kodą** iškrentančiame meniu.</span><span class="sxs-lookup"><span data-stu-id="1d677-133">To use an existing reason code in Personnel management, choose one from the **Use existing reason code** dropdown.</span></span>
     > [!NOTE]
     > <span data-ttu-id="1d677-134">Galtie naudoti tik esantį priežasties kodą personalo valdyme, jei kitas išmokų valdymo priežasties kodas dar nebuvo į jį perkeltas.</span><span class="sxs-lookup"><span data-stu-id="1d677-134">You can only use an existing reason code in Personnel management if another Benefits management reason code hasn't already migrated to it.</span></span>
   - <span data-ttu-id="1d677-135">Norėdami sukurti naują priežasties kodą personalo valdyme, įveskite naują **Naujas priežasties kodas** ir tada įveskite aprašą **Naujas aprašas**.</span><span class="sxs-lookup"><span data-stu-id="1d677-135">To create a new reason code in Personnel management, enter a new one in **New reason code**, and then enter a description in **New description**.</span></span>

   <span data-ttu-id="1d677-136">[![Padarykite žemėlapį personalo valdymo priežasties kodo](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span><span class="sxs-lookup"><span data-stu-id="1d677-136">[![Map to a Personnel management reason code](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span></span>

<span data-ttu-id="1d677-137">Po to, kai priežasties kodai perkeliami į personalo valdymą, parinktis jų naudojimui išmokų valdyme yra automatiškai nustatomas į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="1d677-137">After reason codes migrate to Personnel management, the option for using them in Benefits management is automatically set to **Yes**.</span></span>

<span data-ttu-id="1d677-138">[![Naudokite priežasties kodą išmokų valdyme](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span><span class="sxs-lookup"><span data-stu-id="1d677-138">[![Use reason code in Benefits management](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span></span>