---
title: Įgūdžių konfigūravimas
description: Galite sekti savo darbuotojo įgūdžius „Dynamics 365 Human Resources” platformoje. Taip pat galite nurodyti įgūdžius, kurių reikia konkrečiam darbui.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076564"
---
# <a name="configure-skills"></a><span data-ttu-id="38f4a-104">Įgūdžių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="38f4a-104">Configure skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="38f4a-105">Galite sekti savo darbuotojo įgūdžius „Dynamics 365 Human Resources” platformoje.</span><span class="sxs-lookup"><span data-stu-id="38f4a-105">You can track your worker's skills in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="38f4a-106">Taip pat galite nurodyti įgūdžius, kurių reikia konkrečiam darbui.</span><span class="sxs-lookup"><span data-stu-id="38f4a-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="38f4a-107">Įgūdžių, kuriuos galite sekti, pavyzdžiai:</span><span class="sxs-lookup"><span data-stu-id="38f4a-107">Examples of skills you can track include:</span></span>

- <span data-ttu-id="38f4a-108">Prižiūrėtojo – gebėjimas prižiūrėti kitų darbą.</span><span class="sxs-lookup"><span data-stu-id="38f4a-108">Supervisory – Ability to supervise the work of others.</span></span>
- <span data-ttu-id="38f4a-109">Vadovo – gebėjimas vadovauti darbuotojams ir verslo domenams.</span><span class="sxs-lookup"><span data-stu-id="38f4a-109">Leadership – Ability to lead employees and business domains.</span></span>
- <span data-ttu-id="38f4a-110">Planuotojo – gebėjimas žvelgti į priekį, formuluoti ir analizuoti planų vizijas.</span><span class="sxs-lookup"><span data-stu-id="38f4a-110">Planning – Ability to look ahead, to form vision statements, and to see them through.</span></span>
- <span data-ttu-id="38f4a-111">HTML – gebėjimas rašyti HTML kodą.</span><span class="sxs-lookup"><span data-stu-id="38f4a-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="38f4a-112">Jei dar nenustatėte įgūdžių tipų ir vertinimo modelių, turėsite juos įtraukti prieš kurdami įgūdžius.</span><span class="sxs-lookup"><span data-stu-id="38f4a-112">If you haven't already set up skill types and rating models, you'll need to add some before creating skills.</span></span>

<span data-ttu-id="38f4a-113">Šie žmonės gali įvesti darbuotojo įgūdžius:</span><span class="sxs-lookup"><span data-stu-id="38f4a-113">The following people can enter skills for a worker:</span></span>

- <span data-ttu-id="38f4a-114">Darbuotojai gali įvesti savo įgūdžius Darbuotojų savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="38f4a-114">Workers can enter skills for themselves in Employee self-service.</span></span> <span data-ttu-id="38f4a-115">Šiuos įgūdžius privalo patvirtinti vadovas.</span><span class="sxs-lookup"><span data-stu-id="38f4a-115">These skills require manager approval.</span></span>
- <span data-ttu-id="38f4a-116">Vadovai gali įvesti savo darbuotojų įgūdžius.</span><span class="sxs-lookup"><span data-stu-id="38f4a-116">Managers can enter skills for their workers.</span></span> <span data-ttu-id="38f4a-117">Galite sukurti darbo eigą, automatiškai patvirtinančią šiuos įgūdžius.</span><span class="sxs-lookup"><span data-stu-id="38f4a-117">You can create a workflow that auto-approves these skills.</span></span>

## <a name="create-a-skill-type"></a><span data-ttu-id="38f4a-118">Įgūdžių tipo kūrimas</span><span class="sxs-lookup"><span data-stu-id="38f4a-118">Create a skill type</span></span>

<span data-ttu-id="38f4a-119">Įgūdžių tipai yra kategorijos, kurioms priklauso atskiri įgūdžiai, pavyzdžiui, Administravimas arba Pardavimas.</span><span class="sxs-lookup"><span data-stu-id="38f4a-119">Skill types are categories that individual skills fall under, such as Administration or Sales.</span></span>

1. <span data-ttu-id="38f4a-120">Darbo srityje **Darbuotojo plėtra** pasirinkite **Saitai**.</span><span class="sxs-lookup"><span data-stu-id="38f4a-120">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="38f4a-121">Dalyje **Kompetencijos sąranka** pasirinkite **Įgūdžių tipai**.</span><span class="sxs-lookup"><span data-stu-id="38f4a-121">Under **Competency setup**, select **Skill types**.</span></span>

3. <span data-ttu-id="38f4a-122">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="38f4a-122">Select **New**.</span></span>

4. <span data-ttu-id="38f4a-123">Užpildykite toliau nurodytus laukus:</span><span class="sxs-lookup"><span data-stu-id="38f4a-123">Complete the following fields:</span></span>

   - <span data-ttu-id="38f4a-124">**Įgūdžių tipas**: Įveskite įgūdžių tipo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="38f4a-124">**Skill type**: Enter a name for the skill type.</span></span>
   - <span data-ttu-id="38f4a-125">**Aprašas**: Įveskite įgūdžių tipo aprašą.</span><span class="sxs-lookup"><span data-stu-id="38f4a-125">**Description**: Enter a description for the skill type.</span></span>

5. <span data-ttu-id="38f4a-126">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="38f4a-126">Select **Save**.</span></span>

## <a name="create-a-rating-model"></a><span data-ttu-id="38f4a-127">Vertinimo modelio kūrimas</span><span class="sxs-lookup"><span data-stu-id="38f4a-127">Create a rating model</span></span>

<span data-ttu-id="38f4a-128">Vertinimo modelis padeda įvertinti asmens faktinį įgūdžių lygį, turimą pasiekti lygį arba darbui reikalingo įgūdžio lygį.</span><span class="sxs-lookup"><span data-stu-id="38f4a-128">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill required for a job.</span></span> <span data-ttu-id="38f4a-129">Kiekvienam vertinimo modelio lygiui priskiriamas koeficientas.</span><span class="sxs-lookup"><span data-stu-id="38f4a-129">Each level in a rating model is assigned a factor.</span></span>

1. <span data-ttu-id="38f4a-130">Darbo srityje **Darbuotojo plėtra** pasirinkite **Saitai**.</span><span class="sxs-lookup"><span data-stu-id="38f4a-130">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="38f4a-131">Dalyje **Kompetencijos sąranka** pasirinkite **Vertinimo modeliai**.</span><span class="sxs-lookup"><span data-stu-id="38f4a-131">Under **Competency setup**, select **Rating models**.</span></span>

3. <span data-ttu-id="38f4a-132">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="38f4a-132">Select **New**.</span></span>

4. <span data-ttu-id="38f4a-133">Užpildykite toliau nurodytus laukus:</span><span class="sxs-lookup"><span data-stu-id="38f4a-133">Complete the following fields:</span></span>

   - <span data-ttu-id="38f4a-134">**Vertinimas**: Įveskite vertinimo modelio pavadinimą, pavyzdžiui, **Įgūdžiai**.</span><span class="sxs-lookup"><span data-stu-id="38f4a-134">**Rating**: Enter a name for the rating model, such as **Skills**.</span></span>
   - <span data-ttu-id="38f4a-135">**Aprašas**: Įveskite vertinimo modelio aprašą, pavyzdžiui, **Įgūdžių vertinimai**.</span><span class="sxs-lookup"><span data-stu-id="38f4a-135">**Description**: Enter a description for the rating model, such as **Skill ratings**.</span></span>

5. <span data-ttu-id="38f4a-136">Dalyje **Lygiai** pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="38f4a-136">In the **Levels** section, select **New**.</span></span> <span data-ttu-id="38f4a-137">Kiekvienam lygiui, kurį norite pridėti, užpildykite šiuos laukus:</span><span class="sxs-lookup"><span data-stu-id="38f4a-137">For each level you want to add, complete the following fields:</span></span>

   - <span data-ttu-id="38f4a-138">**Lygis**: Įveskite lygio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="38f4a-138">**Level**: Enter a name for the level.</span></span>
   - <span data-ttu-id="38f4a-139">**Aprašas**: Įveskite lygio aprašą.</span><span class="sxs-lookup"><span data-stu-id="38f4a-139">**Description**: Enter a description for the level.</span></span>
   - <span data-ttu-id="38f4a-140">**Koeficientas**: Įveskite koeficiento vertę nuo 0 iki 9.</span><span class="sxs-lookup"><span data-stu-id="38f4a-140">**Factor**: Enter a factor value from 0-9.</span></span> <span data-ttu-id="38f4a-141">Koeficientai padeda normalizuoti skirtingus vertinimo modelius naudojančių įgūdžių rezultatus.</span><span class="sxs-lookup"><span data-stu-id="38f4a-141">Factors help normalize the scores of skills that use different rating models.</span></span> <span data-ttu-id="38f4a-142">Kiekvienas lygis privalo turėti unikalų koeficientą.</span><span class="sxs-lookup"><span data-stu-id="38f4a-142">Each level must have a unique factor.</span></span> <span data-ttu-id="38f4a-143">Didesnių koeficientų lygiai gali daryti didesnę įtaką vertinimo modeliui.</span><span class="sxs-lookup"><span data-stu-id="38f4a-143">Levels with higher factor values carry more weight in a rating model.</span></span>

   <span data-ttu-id="38f4a-144">Tęskite lygių pridėjimą, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="38f4a-144">Continue adding levels as necessary.</span></span> <span data-ttu-id="38f4a-145">Kiekvienam vertinimo modeliui galite įvesti iki 10 lygių.</span><span class="sxs-lookup"><span data-stu-id="38f4a-145">You can enter up to 10 levels for each rating model.</span></span>

6. <span data-ttu-id="38f4a-146">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="38f4a-146">Select **Save**.</span></span>

## <a name="create-a-skill"></a><span data-ttu-id="38f4a-147">Įgūdžio kūrimas</span><span class="sxs-lookup"><span data-stu-id="38f4a-147">Create a skill</span></span>

<span data-ttu-id="38f4a-148">Kad galėtumėte priskirti įgūdį, sukurti įgūdžių susiejimo iešką ar įgūdžių profilį, turite įvesti informaciją apie įgūdžius puslapyje **Įgūdžiai**.</span><span class="sxs-lookup"><span data-stu-id="38f4a-148">Before you can assign a skill, or create a skill-mapping search or skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="38f4a-149">Kiekvieno įgūdžio atveju pasirinkite įgūdžio tipą ir vertinimo modelį.</span><span class="sxs-lookup"><span data-stu-id="38f4a-149">For each skill, you can select a skill type and a rating model.</span></span>

1. <span data-ttu-id="38f4a-150">Darbo srityje **Darbuotojo plėtra** pasirinkite **Saitai**.</span><span class="sxs-lookup"><span data-stu-id="38f4a-150">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="38f4a-151">Dalyje **Kompetencijos sąranka** pasirinkite **Įgūdžiai**.</span><span class="sxs-lookup"><span data-stu-id="38f4a-151">Under **Competency setup**, select **Skills**.</span></span>

3. <span data-ttu-id="38f4a-152">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="38f4a-152">Select **New**.</span></span>

4. <span data-ttu-id="38f4a-153">Užpildykite toliau nurodytus laukus:</span><span class="sxs-lookup"><span data-stu-id="38f4a-153">Complete the following fields:</span></span>

   - <span data-ttu-id="38f4a-154">**Įgūdis**: Įveskite įgūdžio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="38f4a-154">**Skill**: Enter a name for the skill.</span></span>
   - <span data-ttu-id="38f4a-155">**Aprašas**: Įveskite įgūdžio aprašą.</span><span class="sxs-lookup"><span data-stu-id="38f4a-155">**Description**: Enter a description for the skill.</span></span>
   - <span data-ttu-id="38f4a-156">**Vertinimas**: Pasirinkite vertinimo modelį, kurį norite naudoti šiam įgūdžiui.</span><span class="sxs-lookup"><span data-stu-id="38f4a-156">**Rating**: Select the rating model you want to use for this skill.</span></span>
   - <span data-ttu-id="38f4a-157">**Įgūdžių tipas**: Pasirinkite iš įgūdžių tipų sąrašo.</span><span class="sxs-lookup"><span data-stu-id="38f4a-157">**Skill type**: Select from the list of skill types.</span></span>

5. <span data-ttu-id="38f4a-158">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="38f4a-158">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="38f4a-159">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="38f4a-159">See also</span></span>

[<span data-ttu-id="38f4a-160">Įgūdžių įvedimas</span><span class="sxs-lookup"><span data-stu-id="38f4a-160">Enter skills</span></span>](hr-develop-enter-skills.md)<br>
[<span data-ttu-id="38f4a-161">Įgūdžių susiejimas</span><span class="sxs-lookup"><span data-stu-id="38f4a-161">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]