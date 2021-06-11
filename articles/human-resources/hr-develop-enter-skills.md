---
title: Įgūdžių įvedimas
description: Darbuotojai ir vadovai gali įvesti įgūdžius „Dynamics 365 Human Resources” platformoje.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: b24d37292a2e9749fb2fde06b9f03fcd13db0bbe
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076606"
---
# <a name="enter-skills"></a><span data-ttu-id="32190-103">Įgūdžių įvedimas</span><span class="sxs-lookup"><span data-stu-id="32190-103">Enter skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="32190-104">Galite įvesti darbuotojų, pretendentų ar kontaktų tikslinius arba faktinius įgūdžius „Dynamics 365 Human Resources” platformoje.</span><span class="sxs-lookup"><span data-stu-id="32190-104">You can enter target skills or actual skills for workers, applicants, or contacts in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="32190-105">Tikslinis įgūdis yra įgūdis, kurį asmuo planuoja pasiekti.</span><span class="sxs-lookup"><span data-stu-id="32190-105">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="32190-106">Faktinis įgūdis yra įgūdis, kurį asmuo šiuo metu turi.</span><span class="sxs-lookup"><span data-stu-id="32190-106">An actual skill is a skill that a person currently has.</span></span>

## <a name="create-a-workflow-to-auto-approve-skills"></a><span data-ttu-id="32190-107">Darbo eigos kūrimas automatiniam įgūdžių patvirtinimui</span><span class="sxs-lookup"><span data-stu-id="32190-107">Create a workflow to auto-approve skills</span></span>

<span data-ttu-id="32190-108">Norėdami įvesti įgūdžius, kuriems nereikia patvirtinimo, turite sukurti darbo eigą, automatiškai patvirtinančią įgūdžius.</span><span class="sxs-lookup"><span data-stu-id="32190-108">To enter skills without requiring approval, you must create a workflow to auto-approve skills.</span></span>

> [!NOTE]
> <span data-ttu-id="32190-109">Darbuotojų įvestiems įgūdžiams visada reikalingas vadovo patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="32190-109">Skills entered by workers always require manager approval.</span></span> <span data-ttu-id="32190-110">Ši darbo eiga tik automatiškai patvirtina įgūdžius, kuriuos įvedė vadovai savo darbuotojų vardu.</span><span class="sxs-lookup"><span data-stu-id="32190-110">This workflow only auto-approves skills entered by managers on behalf of their workers.</span></span>

1. <span data-ttu-id="32190-111">Darbo erdvėje **Personalo valdymas** rinkitės **Nuorodos**.</span><span class="sxs-lookup"><span data-stu-id="32190-111">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="32190-112">Dalyje **Sąranka** pasirinkite **Personalo darbo eigos**.</span><span class="sxs-lookup"><span data-stu-id="32190-112">Under **Setup**, select **Human resources workflows**.</span></span>

3. <span data-ttu-id="32190-113">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="32190-113">Select **New**.</span></span>

4. <span data-ttu-id="32190-114">Srityje **Kurti darbo eigą** pasirinkite **Darbuotojo įgūdžiai**.</span><span class="sxs-lookup"><span data-stu-id="32190-114">In the **Create workflow** pane, select **Worker skills**.</span></span>

   <span data-ttu-id="32190-115">[![Pasirinkite darbuotojo įgūdžių darbo eigą](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span><span class="sxs-lookup"><span data-stu-id="32190-115">[![Select Worker skills workflow](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span></span>

5. <span data-ttu-id="32190-116">Dialogo lange **Atidaryti šį failą?** pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="32190-116">In the **Open this file?** dialogue, select **Open**.</span></span> <span data-ttu-id="32190-117">Paraginti įveskite savo kredencialus.</span><span class="sxs-lookup"><span data-stu-id="32190-117">When prompted, enter your credentials.</span></span>

6. <span data-ttu-id="32190-118">Darbo eigos rengyklėje pasirinkite darbo eigos elementą **Patvirtinti įgūdžius** ir nuvilkite jį į drobę.</span><span class="sxs-lookup"><span data-stu-id="32190-118">In the workflow editor, select the **Approve skills** workflow element and drag it onto the canvas.</span></span>

   <span data-ttu-id="32190-119">[![Darbo eigos elemento Patvirtinti įgūdžius pasirinkimas](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span><span class="sxs-lookup"><span data-stu-id="32190-119">[![Select Approve skills workflow element](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span></span>

7. <span data-ttu-id="32190-120">Sujunkite elementą **Pradėti** su **Patvirtinti įgūdžius 1** elementu, o tada sujunkite **Patvirtinti įgūdžius 1** elementą su **Baigti** elementu.</span><span class="sxs-lookup"><span data-stu-id="32190-120">Connect the **Start** element to the **Approve skills 1** element, and then connect the **Approve skills 1** element to the **End** element.</span></span> <span data-ttu-id="32190-121">Jums gali tekti slinkti žemyn, kad pamatytumėte elementą **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="32190-121">You might need to scroll down to see the **End** element.</span></span> <span data-ttu-id="32190-122">Galite nuvilkti jį arčiau kitų elementų.</span><span class="sxs-lookup"><span data-stu-id="32190-122">You can drag it closer to the other elements.</span></span>

   <span data-ttu-id="32190-123">[![Sujunkite darbo eigos elementus](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span><span class="sxs-lookup"><span data-stu-id="32190-123">[![Connect workflow elements](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span></span>

8. <span data-ttu-id="32190-124">Du kartus spustelėkite darbo eigos elementą **Patvirtinti įgūdžius 1**, o tada dešiniuoju pelės mygtuku spustelėkite **1 veiksmo** elementą.</span><span class="sxs-lookup"><span data-stu-id="32190-124">Double-click the **Approve skills 1** workflow element, and then right-click the **Step 1** element.</span></span> <span data-ttu-id="32190-125">Dešiniuoju pelės mygtuku spustelėkite **1 veiksmo** elementą, o tada pasirinkite **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="32190-125">Right-click the **Step 1** element, and then select **Properties**.</span></span>

9. <span data-ttu-id="32190-126">Lange **Ypatybės** pasirinkite **Sąlyga** kairiojoje naršymo srityje.</span><span class="sxs-lookup"><span data-stu-id="32190-126">In the **Properties** window, select **Condition** on the left-hand nav bar.</span></span>

10. <span data-ttu-id="32190-127">Pasirinkite **Vykdyti šį veiksmą tik tada, kai įvykdytos nurodytos sąlygos**.</span><span class="sxs-lookup"><span data-stu-id="32190-127">Select **Run this step only when the following condition is met**.</span></span>

11. <span data-ttu-id="32190-128">Pasirinkite **Įtraukti sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="32190-128">Select **Add condition**.</span></span> <span data-ttu-id="32190-129">Po **Kur** pasirinkite **Darbuotojo savitarnos įgūdžiai**, o tada – **Darbuotojo savitarnos įgūdžiai. Asmuo**.</span><span class="sxs-lookup"><span data-stu-id="32190-129">After **Where**, select **Employee self service skills**, and then select **Employee self service skills.Person**.</span></span> <span data-ttu-id="32190-130">Po **yra** pasirinkite **laukas**, o tada – **Vartotojo ir asmens ryšys.Asmuo**.</span><span class="sxs-lookup"><span data-stu-id="32190-130">After **is**, select **field**, and then select **User to person relationship.Person**.</span></span>

    <span data-ttu-id="32190-131">[![Sąlygos nurodymas](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span><span class="sxs-lookup"><span data-stu-id="32190-131">[![Specify condition](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span></span>

12. <span data-ttu-id="32190-132">Pasirinkite **Priskyrimas** kairiojoje naršymo juostoje.</span><span class="sxs-lookup"><span data-stu-id="32190-132">Select **Assignment** on the left-hand nav bar.</span></span>

13. <span data-ttu-id="32190-133">Skirtuke **Priskyrimo tipas** pasirinkite **Hierarchija**.</span><span class="sxs-lookup"><span data-stu-id="32190-133">On the **Assignment type** tab, select **Hierarchy**.</span></span>

14. <span data-ttu-id="32190-134">Skirtuko **Hierarchijos pasirinkimas** lauke **Hierarchijos tipas:** pasirinkite **Valdymo hierarchija**.</span><span class="sxs-lookup"><span data-stu-id="32190-134">On the **Hierarchy selection** tab, in the **Hierarchy type:** field, select **Managerial hierarchy**.</span></span>

    <span data-ttu-id="32190-135">[![Valdymo hierarchijos nurodymas](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span><span class="sxs-lookup"><span data-stu-id="32190-135">[![Specify managerial hierarchy](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span></span>

15. <span data-ttu-id="32190-136">Pasirinkite **Uždaryti** ir **Darbo eiga** naršymo kelyje, o tada – **Įrašyti ir uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="32190-136">Select **Close**, select **Workflow** in the canvas breadcrumb, and then select **Save and close**.</span></span>

<span data-ttu-id="32190-137">Daugiau informacijos apie darbo eigų kūrimą rasite [Darbo eigos sistemos apžvalga](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="32190-137">For more information about creating workflows, see [Workflow system overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="enter-skills-for-a-worker"></a><span data-ttu-id="32190-138">Darbuotojo įgūdžių įvedimas</span><span class="sxs-lookup"><span data-stu-id="32190-138">Enter skills for a worker</span></span>

1. <span data-ttu-id="32190-139">Pasirinkite darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="32190-139">Select a worker.</span></span>

2. <span data-ttu-id="32190-140">**Darbuotojo** puslapio veiksmų juostoje pasirinkite **Asmuo**, o tada – **Įgūdžiai**.</span><span class="sxs-lookup"><span data-stu-id="32190-140">In the action bar of the **Worker** page, select **Person**, and then select **Skills**.</span></span>

3. <span data-ttu-id="32190-141">Puslapyje **Įgūdžiai** užpildykite šiuos laukus kiekvienam įgūdžiui:</span><span class="sxs-lookup"><span data-stu-id="32190-141">On the **Skills** page, complete the following fields for each skill:</span></span>

   - <span data-ttu-id="32190-142">**Įgūdis**: Pasirinkite įgūdį.</span><span class="sxs-lookup"><span data-stu-id="32190-142">**Skill**: Select a skill.</span></span>
   - <span data-ttu-id="32190-143">**Lygio tipas**: Pasirinkite **Faktinis** jau turimam darbuotojo įgūdžiui arba **Tikslinis** – įgūdžiui, kurį darbuotojas siekią įgyti.</span><span class="sxs-lookup"><span data-stu-id="32190-143">**Level type**: Select **Actual** for a skill the worker already has, or select **Target** for a skill the worker is working toward.</span></span>
   - <span data-ttu-id="32190-144">**Lygis**: Pasirinkite darbuotojo įgūdžio lygį.</span><span class="sxs-lookup"><span data-stu-id="32190-144">**Level**: Select a level for the worker's skill.</span></span>
   - <span data-ttu-id="32190-145">**Lygio data**: Kalendoriaus įrankyje pasirinkite datą.</span><span class="sxs-lookup"><span data-stu-id="32190-145">**Level date**: Select a date in the calendar tool.</span></span>
   - <span data-ttu-id="32190-146">**Egzaminuotojas**: Jei reikia, iš sąrašo pasirinkite egzaminuotoją.</span><span class="sxs-lookup"><span data-stu-id="32190-146">**Examiner**: If appropriate, select an examiner from the list.</span></span> <span data-ttu-id="32190-147">Galite filtruoti savo iešką.</span><span class="sxs-lookup"><span data-stu-id="32190-147">You can filter your search.</span></span>
   - <span data-ttu-id="32190-148">**Darbo patirties metai**: Įveskite darbo patirties metus.</span><span class="sxs-lookup"><span data-stu-id="32190-148">**Years of experience**: Enter years of experience.</span></span>
   - <span data-ttu-id="32190-149">**Patvirtinta**: Jei įgūdis yra patvirtintas, pažymėkite šį lauką.</span><span class="sxs-lookup"><span data-stu-id="32190-149">**Verified**: If the skill is verified, check the box.</span></span>
   - <span data-ttu-id="32190-150">**Patvirtino**: Įveskite patvirtinusio asmens vardą.</span><span class="sxs-lookup"><span data-stu-id="32190-150">**Verified by**: Enter the name of the verifier.</span></span>

4. <span data-ttu-id="32190-151">Įvedę įgūdžius, pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="32190-151">When you're done entering skills, select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="32190-152">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="32190-152">See also</span></span>

[<span data-ttu-id="32190-153">Įgūdžių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="32190-153">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="32190-154">Įgūdžių susiejimas</span><span class="sxs-lookup"><span data-stu-id="32190-154">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]