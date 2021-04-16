---
title: Sukurkite darbo eigą atostogų pirkimo ir pardavimo užklausai
description: Sukurkite darbo eigą atostogų pirkimo ir pardavimo užklausai, tam, kad galėtumėte nuosekliai tvarkyti atostogų pirkimo ir pardavimo užklausas Dynamics 365 Human Resources platformoje.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a0ddb3ea3aa7f1941ff486d7a3e1db5846fac3eb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790553"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="b1fc0-103">Sukurkite darbo eigą atostogų pirkimo ir pardavimo užklausai</span><span class="sxs-lookup"><span data-stu-id="b1fc0-103">Create a buy and sell leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b1fc0-104">Galite sukurti darbo eigą Dynamics 365 Human Resources platformoje, tam, kad nuosekliai tvarkytumėte savo atostogų pirkimo ir pardavimo užklausas.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="b1fc0-105">**Atostogų pirkimo ir pardavimo** darbo eiga jums leidžia:</span><span class="sxs-lookup"><span data-stu-id="b1fc0-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="b1fc0-106">Nustatyti užduotis</span><span class="sxs-lookup"><span data-stu-id="b1fc0-106">Define tasks</span></span>
- <span data-ttu-id="b1fc0-107">Nustatyti, kas turi atlikti užduotis</span><span class="sxs-lookup"><span data-stu-id="b1fc0-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="b1fc0-108">Nurodyti, kas gali patvirtinti arba atmesti užklausas</span><span class="sxs-lookup"><span data-stu-id="b1fc0-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="b1fc0-109">Sukurkite darbo eigą atostogų pirkimo ir pardavimo užklausai</span><span class="sxs-lookup"><span data-stu-id="b1fc0-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="b1fc0-110">Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="b1fc0-111">Dalyje **Sąranka** pasirinkite **Žmogiškųjų išteklių darbo eigos**.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="b1fc0-112">Pasirinkite **Naujas**, o tada pasirinkite **Atostogų pirkimo ir pardavimo užklausa**.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="b1fc0-113">Kai pasirodys pranešimo langelis **Atidaryti šį failą?**, pasirinkite **Atidaryti** ir prisijunkite, naudodami įmonės kredencialus.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="b1fc0-114">Naudokite darbo eigos doroklį, kad sukurtumėte savo atostogų užklausų darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="b1fc0-115">Daugiau informacijos apie darbą su darbo eigomis žr. skyriuje [Darbo eigų apžvalgos kūrimas](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="b1fc0-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="b1fc0-116">Atostogų ir neatvykimų darbo eigos duomenų elementai</span><span class="sxs-lookup"><span data-stu-id="b1fc0-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="b1fc0-117">Galite naudotis šiais informacijos elementais, kad sukurtumėte sąlyginius ir automatinius patvirtinimus atostogų pirkimo ir pardavimo užklausoms darbo eigose: </span><span class="sxs-lookup"><span data-stu-id="b1fc0-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="b1fc0-118">**Suma**</span><span class="sxs-lookup"><span data-stu-id="b1fc0-118">**Amount**</span></span>
- <span data-ttu-id="b1fc0-119">**Atostogų pirkimo ir pardavimo strategija**</span><span class="sxs-lookup"><span data-stu-id="b1fc0-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="b1fc0-120">**Įmonė**</span><span class="sxs-lookup"><span data-stu-id="b1fc0-120">**Company**</span></span>
- <span data-ttu-id="b1fc0-121">**Sukūrė**</span><span class="sxs-lookup"><span data-stu-id="b1fc0-121">**Created by**</span></span>
- <span data-ttu-id="b1fc0-122">**Sukūrimo data ir laikas**</span><span class="sxs-lookup"><span data-stu-id="b1fc0-122">**Created date and time**</span></span>
- <span data-ttu-id="b1fc0-123">**Pabaigos data**</span><span class="sxs-lookup"><span data-stu-id="b1fc0-123">**End date**</span></span>
- <span data-ttu-id="b1fc0-124">**Atostogų tipas**</span><span class="sxs-lookup"><span data-stu-id="b1fc0-124">**Leave type**</span></span>
- <span data-ttu-id="b1fc0-125">**Modifikavo**</span><span class="sxs-lookup"><span data-stu-id="b1fc0-125">**Modified by**</span></span>
- <span data-ttu-id="b1fc0-126">**Pakeitimo data ir laikas**</span><span class="sxs-lookup"><span data-stu-id="b1fc0-126">**Modified date and time**</span></span>
- <span data-ttu-id="b1fc0-127">**Užklausos ID**</span><span class="sxs-lookup"><span data-stu-id="b1fc0-127">**Request ID**</span></span>
- <span data-ttu-id="b1fc0-128">**Pradžios data**</span><span class="sxs-lookup"><span data-stu-id="b1fc0-128">**Start date**</span></span>
- <span data-ttu-id="b1fc0-129">**Būsena**</span><span class="sxs-lookup"><span data-stu-id="b1fc0-129">**Status**</span></span> 
- <span data-ttu-id="b1fc0-130">**Pateikimo data**</span><span class="sxs-lookup"><span data-stu-id="b1fc0-130">**Submission date**</span></span>
- <span data-ttu-id="b1fc0-131">**Pateikė**</span><span class="sxs-lookup"><span data-stu-id="b1fc0-131">**Submitted by**</span></span>
- <span data-ttu-id="b1fc0-132">**Pateikė personalas**</span><span class="sxs-lookup"><span data-stu-id="b1fc0-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="b1fc0-133">**Pateikė vadovas**</span><span class="sxs-lookup"><span data-stu-id="b1fc0-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="b1fc0-134">**Pateikė kito vardu**</span><span class="sxs-lookup"><span data-stu-id="b1fc0-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="b1fc0-135">**Darbuotojas**</span><span class="sxs-lookup"><span data-stu-id="b1fc0-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="b1fc0-136">Darbo eigos pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="b1fc0-136">Workflow examples</span></span>

<span data-ttu-id="b1fc0-137">Šie pavyzdžiai rodo, kaip galima sukurti skirtingus darbo eigos sąlygų tipus naudojant tolesnius duomenų elementus.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="b1fc0-138">Naudokite **Pateikė personalas** ir **Pateikė vadovas** automatiniame veiksme, tam, kad automatiškai būtų patvirtintos atostogų pirkimo ir pardavimo užklausos, ir kad šie vaidmenys būtų pateikti darbuotojų vardu.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="b1fc0-139">Daugiau informacijos apie automatinius veiksmus žr. [Darbo eigos patvirtinimo procesų konfigūravimas](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="b1fc0-139">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="b1fc0-140">Sąlyginiame išraše arba automatiniame veiksme naudokite **Atostogų tipas**, norėdami valdyti, kaip darbo eiga nukreipia tam tikrų atostogų tipų užklausas.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1fc0-141">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="b1fc0-141">See also</span></span>

[<span data-ttu-id="b1fc0-142">Atostogų ir neatvykimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="b1fc0-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="b1fc0-143">Atostogų pirkimo ir pardavimo strategijų valdymas</span><span class="sxs-lookup"><span data-stu-id="b1fc0-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]