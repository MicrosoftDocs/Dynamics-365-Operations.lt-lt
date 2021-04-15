---
title: Nustatyti priežasčių kodus
description: „Dynamics 365 Human Resources“ naudojami priežasčių kodus, siekiant paaiškinti, kodėl keičiasi darbuotojo išmokos.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ee74cb8b11c9b72940448077ee485ade4c0b7a39
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801052"
---
# <a name="set-up-reason-codes"></a><span data-ttu-id="4d437-103">Nustatyti priežasčių kodus</span><span class="sxs-lookup"><span data-stu-id="4d437-103">Set up reason codes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4d437-104">„Dynamics 365 Human Resources“ naudojami priežasčių kodus, siekiant paaiškinti, kodėl keičiasi darbuotojo išmokos.</span><span class="sxs-lookup"><span data-stu-id="4d437-104">Dynamics 365 Human Resources uses reason codes to explain why an employee’s benefits are changing.</span></span>

> [!NOTE]
> <span data-ttu-id="4d437-105">Nuo 2021 m. sausio mėnesio priežasties kodai yra perkeliami į **Personalo valdymo** darbo sritį, o ne **Išmokų valdymo** darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="4d437-105">As of January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="4d437-106">Dėl daugiau informacijos, žr. [Rankiniu būdu perkelti priežasties kodus į personalo valdymą](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span><span class="sxs-lookup"><span data-stu-id="4d437-106">For more information, see [Manually migrate reason codes to Personnel management](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span></span>

## <a name="create-reason-codes"></a><span data-ttu-id="4d437-107">Priežasčių kodų kūrimas</span><span class="sxs-lookup"><span data-stu-id="4d437-107">Create reason codes</span></span>

1. <span data-ttu-id="4d437-108">Darbo srityje **Personalo valdymas** (ar **Išmokų valdymas** darbo srityje, jei jūsų priežasties kodai nebuvo perkelti), rinkitės **Nuorodos** ir tada rinkitės **Priežasties kodai**.</span><span class="sxs-lookup"><span data-stu-id="4d437-108">In the **Personnel management** workspace (or **Benefits management** workspace if your reason codes haven't yet migrated), select **Links**, and then select **Reason codes**.</span></span>

2. <span data-ttu-id="4d437-109">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="4d437-109">Select **New**.</span></span>

3. <span data-ttu-id="4d437-110">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="4d437-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="4d437-111">Laukas</span><span class="sxs-lookup"><span data-stu-id="4d437-111">Field</span></span> | <span data-ttu-id="4d437-112">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="4d437-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="4d437-113">**Tikslinės paskirties šifras**</span><span class="sxs-lookup"><span data-stu-id="4d437-113">**Reason code**</span></span> | <span data-ttu-id="4d437-114">Unikalus pavadinimas, skirtas nustatyti priežastį, dėl kurios darbuotojas galėtų keisti išmokų plano registraciją.</span><span class="sxs-lookup"><span data-stu-id="4d437-114">A unique name to identify the reason an employee would change a benefit plan enrollment.</span></span> |
   | <span data-ttu-id="4d437-115">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="4d437-115">**Description**</span></span> | <span data-ttu-id="4d437-116">Priežasties kodo aprašas.</span><span class="sxs-lookup"><span data-stu-id="4d437-116">A description of the reason code.</span></span> |

4. <span data-ttu-id="4d437-117">Skyriuje **Taikomi scenarijai**, nustatykite **Išmokų valdymas** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="4d437-117">Under **Applicable scenarios**, set **Benefits management** to **Yes**.</span></span> <span data-ttu-id="4d437-118">(Netaikoma, jei jūsų priežasties kodai dar nebuvo perkelti į **Personalo valdymo** dardbo sritį.)</span><span class="sxs-lookup"><span data-stu-id="4d437-118">(Not applicable if your reason codes haven't yet migrated to the **Personnel management** workspace.)</span></span>

5. <span data-ttu-id="4d437-119">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4d437-119">Select **Save**.</span></span>

## <a name="manually-migrate-reason-codes-to-personnel-management"></a><span data-ttu-id="4d437-120">Rankiniu būdu perkelti priežasties kodus į personalo valdymą</span><span class="sxs-lookup"><span data-stu-id="4d437-120">Manually migrate reason codes to Personnel management</span></span>

<span data-ttu-id="4d437-121">2021 m. sausio mėnesį priežasties kodai yra perkeliami į **Personalo valdymo** darbo sritį, o ne **Išmokų valdymo** darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="4d437-121">In January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="4d437-122">Didžio dalis kodo duomenų buvo automatiniu būdu perkelti į jūsų aplinką.</span><span class="sxs-lookup"><span data-stu-id="4d437-122">Most reason code data will automatically migrate in your environment.</span></span> <span data-ttu-id="4d437-123">Kai kurie priežasties kodo duomenys gali būti neperkelti.</span><span class="sxs-lookup"><span data-stu-id="4d437-123">Some reason code data might not migrate.</span></span> <span data-ttu-id="4d437-124">Pavyzdžiui, priežasties kodai dabar turi daugiausiai 15 ženklų, dėl to, visi ilgesni nei 15 ženklų priežasties kodai nebus automatiniu būdu perkelti.</span><span class="sxs-lookup"><span data-stu-id="4d437-124">For example, reason codes now have a 15-character maximum, so any reason codes longer than 15 characters won't migrate automatically.</span></span>

<span data-ttu-id="4d437-125">Matysite reklaminę juostą **Nuorodos** puslapyje **Išmokų valdymas** darbo srityje, kuri jus informuos apie perkelimą ir ar bet kurie priežasties kodai nepersikėlė.</span><span class="sxs-lookup"><span data-stu-id="4d437-125">You'll see a banner on the **Links** page of the **Benefits management** workspace informing you about the migration and whether any reason codes didn't migrate.</span></span>

1. <span data-ttu-id="4d437-126">Rinkitės **Priežasties kodai** dėl išsamios informacijos apie perkėlimo būseną.</span><span class="sxs-lookup"><span data-stu-id="4d437-126">Select **Reason codes** for details about migration status.</span></span>

   <span data-ttu-id="4d437-127">[![Priežasčių kodai](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span><span class="sxs-lookup"><span data-stu-id="4d437-127">[![Reason codes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span></span>

2. <span data-ttu-id="4d437-128">Rinkitės kodo priežastį, kuri nepersikėlė.</span><span class="sxs-lookup"><span data-stu-id="4d437-128">Select a reason code that failed to migrate.</span></span>

   <span data-ttu-id="4d437-129">[![Priežasties kodo perkėlimo būsena](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span><span class="sxs-lookup"><span data-stu-id="4d437-129">[![Reason code migration status](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span></span>

3. <span data-ttu-id="4d437-130">Rinkitės **Perkelti priežasties kodą**.</span><span class="sxs-lookup"><span data-stu-id="4d437-130">Select **Migrate reason code**.</span></span>

   <span data-ttu-id="4d437-131">[![Perkelti priežasties kodą](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span><span class="sxs-lookup"><span data-stu-id="4d437-131">[![Migrate reason code](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span></span>

4. <span data-ttu-id="4d437-132">Juostoje **išmokos priežasties kodo perkėlimas** turite dvi parinktis sudaryti žemėlapį personalo valdymo priežasties kodui:</span><span class="sxs-lookup"><span data-stu-id="4d437-132">In the **Benefit reason code migration** pane, you have two options for mapping to a Personnel management reason code:</span></span>

   - <span data-ttu-id="4d437-133">Norėdami naudoti esantį priežasties kodą personalo valdyme, rinkitės vieną iš esančių **Naudoti esantį priežasties kodą** iškrentančiame meniu.</span><span class="sxs-lookup"><span data-stu-id="4d437-133">To use an existing reason code in Personnel management, choose one from the **Use existing reason code** dropdown.</span></span>
     > [!NOTE]
     > <span data-ttu-id="4d437-134">Galtie naudoti tik esantį priežasties kodą personalo valdyme, jei kitas išmokų valdymo priežasties kodas dar nebuvo į jį perkeltas.</span><span class="sxs-lookup"><span data-stu-id="4d437-134">You can only use an existing reason code in Personnel management if another Benefits management reason code hasn't already migrated to it.</span></span>
   - <span data-ttu-id="4d437-135">Norėdami sukurti naują priežasties kodą personalo valdyme, įveskite naują **Naujas priežasties kodas** ir tada įveskite aprašą **Naujas aprašas**.</span><span class="sxs-lookup"><span data-stu-id="4d437-135">To create a new reason code in Personnel management, enter a new one in **New reason code**, and then enter a description in **New description**.</span></span>

   <span data-ttu-id="4d437-136">[![Padarykite žemėlapį personalo valdymo priežasties kodo](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span><span class="sxs-lookup"><span data-stu-id="4d437-136">[![Map to a Personnel management reason code](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span></span>

<span data-ttu-id="4d437-137">Po to, kai priežasties kodai perkeliami į personalo valdymą, parinktis jų naudojimui išmokų valdyme yra automatiškai nustatomas į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="4d437-137">After reason codes migrate to Personnel management, the option for using them in Benefits management is automatically set to **Yes**.</span></span>

<span data-ttu-id="4d437-138">[![Naudokite priežasties kodą išmokų valdyme](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span><span class="sxs-lookup"><span data-stu-id="4d437-138">[![Use reason code in Benefits management](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]