---
title: Atostogų užklausos darbo eigos kūrimas
description: Atostogų ir neatvykimų užklausų darbo eigos kūrimas, siekiant nuosekliai tvarkyti atostogų užklausas „Dynamics 365 Human Resources“.
author: andreabichsel
manager: AnnBe
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 209f0ec7236778cc0a828102e554b02206b45b73
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419658"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="df5b4-103">Atostogų užklausos darbo eigos kūrimas</span><span class="sxs-lookup"><span data-stu-id="df5b4-103">Create a leave request workflow</span></span>

<span data-ttu-id="df5b4-104">Galite sukurti darbo eigą „Dynamics 365 Human Resources“, kad galėtumėte nuosekliai tvarkyti atostogų ir neatvykimų užklausas.</span><span class="sxs-lookup"><span data-stu-id="df5b4-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="df5b4-105">**Atostogų ir neatvykimų** darbo eiga leidžia:</span><span class="sxs-lookup"><span data-stu-id="df5b4-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="df5b4-106">Nustatyti užduotis</span><span class="sxs-lookup"><span data-stu-id="df5b4-106">Define tasks</span></span>
- <span data-ttu-id="df5b4-107">Nustatyti, kas turi atlikti užduotis</span><span class="sxs-lookup"><span data-stu-id="df5b4-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="df5b4-108">Nurodyti, kas gali patvirtinti arba atmesti užklausas</span><span class="sxs-lookup"><span data-stu-id="df5b4-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="df5b4-109">Atostogų ir neatvykimų darbo eigos kūrimas</span><span class="sxs-lookup"><span data-stu-id="df5b4-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="df5b4-110">Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**.</span><span class="sxs-lookup"><span data-stu-id="df5b4-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="df5b4-111">Dalyje **Sąranka** pasirinkite **Žmogiškųjų išteklių darbo eigos**.</span><span class="sxs-lookup"><span data-stu-id="df5b4-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="df5b4-112">Pasirinkite **Nauja**, tada pasirinkite **Atostogų ir neatvykimų užklausa**.</span><span class="sxs-lookup"><span data-stu-id="df5b4-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="df5b4-113">Kai pasirodys pranešimo langelis **Atidaryti šį failą?**, pasirinkite **Atidaryti** ir prisijunkite, naudodami įmonės kredencialus.</span><span class="sxs-lookup"><span data-stu-id="df5b4-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="df5b4-114">Naudokite darbo eigos doroklį, kad sukurtumėte savo atostogų užklausų darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="df5b4-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="df5b4-115">Daugiau informacijos apie darbą su darbo eigomis žr. skyriuje [Darbo eigų apžvalgos kūrimas](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="df5b4-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="df5b4-116">Atostogų ir neatvykimų darbo eigos duomenų elementai</span><span class="sxs-lookup"><span data-stu-id="df5b4-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="df5b4-117">Galite naudoti tolesnius duomenų elementus, norėdami sukurti sąlyginius arba automatinius patvirtinimus atostogų ir neatvykimų užklausų darbo eigose.</span><span class="sxs-lookup"><span data-stu-id="df5b4-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="df5b4-118">**Suma**</span><span class="sxs-lookup"><span data-stu-id="df5b4-118">**Amount**</span></span>
- <span data-ttu-id="df5b4-119">**Komentuoti**</span><span class="sxs-lookup"><span data-stu-id="df5b4-119">**Comment**</span></span>
- <span data-ttu-id="df5b4-120">**Įmonė**</span><span class="sxs-lookup"><span data-stu-id="df5b4-120">**Company**</span></span>
- <span data-ttu-id="df5b4-121">**Sukūrė**</span><span class="sxs-lookup"><span data-stu-id="df5b4-121">**Created by**</span></span>
- <span data-ttu-id="df5b4-122">**Sukūrimo data ir laikas**</span><span class="sxs-lookup"><span data-stu-id="df5b4-122">**Created date and time**</span></span>
- <span data-ttu-id="df5b4-123">**Pabaigos data**</span><span class="sxs-lookup"><span data-stu-id="df5b4-123">**End date**</span></span>
- <span data-ttu-id="df5b4-124">**Atostogų tipas**</span><span class="sxs-lookup"><span data-stu-id="df5b4-124">**Leave type**</span></span>
- <span data-ttu-id="df5b4-125">**Modifikavo**</span><span class="sxs-lookup"><span data-stu-id="df5b4-125">**Modified by**</span></span>
- <span data-ttu-id="df5b4-126">**Pakeitimo data ir laikas**</span><span class="sxs-lookup"><span data-stu-id="df5b4-126">**Modified date and time**</span></span>
- <span data-ttu-id="df5b4-127">**Tikslinės paskirties šifras**</span><span class="sxs-lookup"><span data-stu-id="df5b4-127">**Reason code**</span></span>
- <span data-ttu-id="df5b4-128">**Užklausos ID**</span><span class="sxs-lookup"><span data-stu-id="df5b4-128">**Request ID**</span></span>
- <span data-ttu-id="df5b4-129">**Pradžios data**</span><span class="sxs-lookup"><span data-stu-id="df5b4-129">**Start date**</span></span>
- <span data-ttu-id="df5b4-130">**Būsena**</span><span class="sxs-lookup"><span data-stu-id="df5b4-130">**Status**</span></span> 
- <span data-ttu-id="df5b4-131">**Pateikimo data**</span><span class="sxs-lookup"><span data-stu-id="df5b4-131">**Submission date**</span></span>
- <span data-ttu-id="df5b4-132">**Pateikė**</span><span class="sxs-lookup"><span data-stu-id="df5b4-132">**Submitted by**</span></span>
- <span data-ttu-id="df5b4-133">**Pateikė personalas**</span><span class="sxs-lookup"><span data-stu-id="df5b4-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="df5b4-134">**Pateikė vadovas**</span><span class="sxs-lookup"><span data-stu-id="df5b4-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="df5b4-135">**Pateikė kito vardu**</span><span class="sxs-lookup"><span data-stu-id="df5b4-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="df5b4-136">**Darbininkas**</span><span class="sxs-lookup"><span data-stu-id="df5b4-136">**Worker**</span></span>
- <span data-ttu-id="df5b4-137">**Darbininko tipas**</span><span class="sxs-lookup"><span data-stu-id="df5b4-137">**Worker type**</span></span>

<span data-ttu-id="df5b4-138">Šie pavyzdžiai rodo, kaip galima sukurti skirtingus darbo eigos sąlygų tipus naudojant tolesnius duomenų elementus.</span><span class="sxs-lookup"><span data-stu-id="df5b4-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="df5b4-139">Sąlyginiame išraše naudokite **Priežasties kodas**, kad nukreiptumėte nedarbingumo atostogų užklausas su priežasties kodu **Operacija** personalui patvirtinti, o visus kitus priežasties kodus – vadovui.</span><span class="sxs-lookup"><span data-stu-id="df5b4-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="df5b4-140">Daugiau informacijos apie sąlyginius išrašus žr. [Sąlyginių darbo eigos sprendimų konfigūravimas](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span><span class="sxs-lookup"><span data-stu-id="df5b4-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="df5b4-141">Automatiniame veiksme naudokite **Pateikė personalas** ir **Pateikė vadovas**, norėdami automatiškai patvirtinti atostogų užklausas, kurias šie vaidmenys pateikia darbuotojų vardu.</span><span class="sxs-lookup"><span data-stu-id="df5b4-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="df5b4-142">Daugiau informacijos apie automatinius veiksmus žr. [Darbo eigos patvirtinimo procesų konfigūravimas](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="df5b4-142">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="df5b4-143">Sąlyginiame išraše arba automatiniame veiksme naudokite **Atostogų tipas**, norėdami valdyti, kaip darbo eiga nukreipia tam tikrų atostogų tipų užklausas.</span><span class="sxs-lookup"><span data-stu-id="df5b4-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="df5b4-144">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="df5b4-144">See also</span></span>

- [<span data-ttu-id="df5b4-145">Atostogų ir neatvykimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="df5b4-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
