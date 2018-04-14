---
title: "Verslo poreikių ir darbo jėgos įgūdžių suderinimas"
description: "Galite sekti įgūdžius, kuriuos darbuotojai, pretendentai arba kontaktiniai asmenys turi arba turi turėti, kad efektyviai atliktų savo vaidmenis. Taip pat galite nurodyti įgūdžius, kurių reikia konkrečiam darbui."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3a5b9f98b371dbad9b6b0538e0d9975dc5ed701c
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="align-workforce-skills-with-business-needs"></a><span data-ttu-id="30f68-104">Verslo poreikių ir darbo jėgos įgūdžių suderinimas</span><span class="sxs-lookup"><span data-stu-id="30f68-104">Align workforce skills with business needs</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="30f68-105">Galite sekti įgūdžius, kuriuos darbuotojai, pretendentai arba kontaktiniai asmenys turi arba turi turėti, kad efektyviai atliktų savo vaidmenis.</span><span class="sxs-lookup"><span data-stu-id="30f68-105">You can track the skills that workers, applicants, or contact persons have, or should have, to fulfill their roles effectively.</span></span> <span data-ttu-id="30f68-106">Taip pat galite nurodyti įgūdžius, kurių reikia konkrečiam darbui.</span><span class="sxs-lookup"><span data-stu-id="30f68-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="30f68-107">Toliau pateikti įgūdžių, kuriuos galite sekti, pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="30f68-107">Examples of skills you can track include the following:</span></span>
-   <span data-ttu-id="30f68-108">Prižiūrėtojo – gebėjimas prižiūrėti kitų darbą.</span><span class="sxs-lookup"><span data-stu-id="30f68-108">Supervisory – Ability to supervise the work of others.</span></span>
-   <span data-ttu-id="30f68-109">Vadovo – gebėjimas vadovauti darbuotojams ir verslo domenams.</span><span class="sxs-lookup"><span data-stu-id="30f68-109">Leadership – Ability to lead employees and business domains.</span></span>
-   <span data-ttu-id="30f68-110">Planuotojo – gebėjimas žvelgti į priekį, formuluoti ir analizuoti planus.</span><span class="sxs-lookup"><span data-stu-id="30f68-110">Planning – Ability to look ahead, to form visions, and to see them through.</span></span>
-   <span data-ttu-id="30f68-111">HTML – gebėjimas rašyti HTML kodą.</span><span class="sxs-lookup"><span data-stu-id="30f68-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="30f68-112">Kad galėtumėte priskirti įgūdį asmeniui arba darbui, sukurti įgūdžių susiejimo iešką arba sukurti įgūdžių šabloną, turite įvesti informaciją apie įgūdžius puslapyje **Įgūdžiai**.</span><span class="sxs-lookup"><span data-stu-id="30f68-112">Before you can assign a skill to a person or a job, create a skill-mapping search, or create a skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="30f68-113">Kiekvieno įgūdžio atveju pasirinkite įgūdžio tipą ir vertinimo modelį.</span><span class="sxs-lookup"><span data-stu-id="30f68-113">For each skill, you can select a skill type and a rating model.</span></span>

## <a name="rating-models"></a><span data-ttu-id="30f68-114">Vertinimo modeliai</span><span class="sxs-lookup"><span data-stu-id="30f68-114">Rating models</span></span>
<span data-ttu-id="30f68-115">Vertinimo modelis padeda įvertinti asmens faktinį įgūdžių lygį, turimą pasiekti lygį arba įgūdžio, kurio reikia darbui, lygį.</span><span class="sxs-lookup"><span data-stu-id="30f68-115">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill that is required for a job.</span></span> <span data-ttu-id="30f68-116">Vertinimo modeliui galite sukurti iki 10 lygių.</span><span class="sxs-lookup"><span data-stu-id="30f68-116">You can enter up to 10 levels for a rating model.</span></span>  <span data-ttu-id="30f68-117">Kiekvienam vertinimo modelio lygiui priskiriamas koeficientas.</span><span class="sxs-lookup"><span data-stu-id="30f68-117">Each level in a rating model is assigned a factor.</span></span>  <span data-ttu-id="30f68-118">Koeficiento vertė bus naudojama įgūdžių vertinimui normalizuoti, kuris naudos skirtingus vertinimo modelius.</span><span class="sxs-lookup"><span data-stu-id="30f68-118">The factor value will be used to normalize the scores of skills that use different rating models.</span></span>  <span data-ttu-id="30f68-119">Koeficientas turi būti skaičius nuo 0 iki 9 ir kiekvienas lygis turi turėti unikalų koeficientą.</span><span class="sxs-lookup"><span data-stu-id="30f68-119">The factor must be a number between 0-9 and each level must have a unique factor.</span></span>  <span data-ttu-id="30f68-120">Didesnių koeficientų lygiai gali daryti didesnę įtaką vertinimo modeliui.</span><span class="sxs-lookup"><span data-stu-id="30f68-120">Levels with higher factor values carry more weight in a rating model.</span></span>

## <a name="specify-job-skills"></a><span data-ttu-id="30f68-121">Darbo įgūdžių nurodymas</span><span class="sxs-lookup"><span data-stu-id="30f68-121">Specify job skills</span></span>
<span data-ttu-id="30f68-122">Kai įvedate informaciją apie darbą, galite nurodyti įgūdžius, kuriuos asmuo turi turėti, kad galėtų atlikti darbą, reikalingą pagal pareigas.</span><span class="sxs-lookup"><span data-stu-id="30f68-122">When you enter information about a job, you can specify the skills that a person should have to perform the work required for the job.</span></span>  <span data-ttu-id="30f68-123">Be to, galite nurodyti norimą kiekvieno įgūdžio lygį ir įgūdžio svarbumo lygį.</span><span class="sxs-lookup"><span data-stu-id="30f68-123">In addition you can specify the desired level for each skill as well the level of importance of the skill.</span></span> <span data-ttu-id="30f68-124">Skirtingoms pareigoms gali būti reikalingas skirtingas to paties įgūdžio lygis.</span><span class="sxs-lookup"><span data-stu-id="30f68-124">Different jobs can require different levels of importance for the same skill.</span></span>

## <a name="enter-skills-for-workers-applicants-or-contacts"></a><span data-ttu-id="30f68-125">Darbuotojų, pretendentų arba kontaktų įgūdžių įvedimas</span><span class="sxs-lookup"><span data-stu-id="30f68-125">Enter skills for workers, applicants, or contacts</span></span>
<span data-ttu-id="30f68-126">Galite įvesti darbuotojų, pretendentų arba kontaktų tikslinius įgūdžius.</span><span class="sxs-lookup"><span data-stu-id="30f68-126">You can enter target skills or actual skills for workers, applicants, or contacts.</span></span> <span data-ttu-id="30f68-127">Tikslinis įgūdis yra įgūdis, kurį asmuo planuoja pasiekti.</span><span class="sxs-lookup"><span data-stu-id="30f68-127">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="30f68-128">Faktinis įgūdis yra įgūdis, kurį asmuo šiuo metu turi.</span><span class="sxs-lookup"><span data-stu-id="30f68-128">An actual skill is a skill that a person currently has.</span></span>

## <a name="skill-mapping-and-skill-mapping-profiles"></a><span data-ttu-id="30f68-129"> Įgūdžių išdėstymas ir įgūdžių išdėstymo šablonai</span><span class="sxs-lookup"><span data-stu-id="30f68-129">Skill mapping and Skill mapping profiles</span></span>
<span data-ttu-id="30f68-130">Galite kurti įgūdžių išdėstymo iešką, norėdami rasti darbuotoją, pretendentą arba kontaktinį asmenį, kurio kvalifikacija yra tinkama tam tikro tipo užduočiai atlikti.</span><span class="sxs-lookup"><span data-stu-id="30f68-130">You can create a skill-mapping search to find a worker, applicant, or contact person who is qualified to perform a specific type of task.</span></span> <span data-ttu-id="30f68-131">Įgūdžių išdėstymo ieškos mechanizmas tikrina visus įgūdžius, išsilavinimą, sertifikatus, atsakingas pareigas ir projekto patirtį ir pateikia rezultatus, kurie atitinka įvestus kriterijus.</span><span class="sxs-lookup"><span data-stu-id="30f68-131">Skill-mapping searches look across skills, education, certificates, positions of trust and project experience and return results that match the criteria entered.</span></span>  <span data-ttu-id="30f68-132">Pvz., gali būti naudinga žinoti, kurie jūsų organizacijos darbuotojai yra gavę CPA.</span><span class="sxs-lookup"><span data-stu-id="30f68-132">For example, it might be useful to know which workers in your organization earned their CPA.</span></span>

<span data-ttu-id="30f68-133">Naudodami įgūdžių išdėstymo šablonus galite rasti esamus darbuotojus arba kandidatus, kurių kvalifikacija tiesiogiai atitinka verslo poreikius.</span><span class="sxs-lookup"><span data-stu-id="30f68-133">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>  <span data-ttu-id="30f68-134">Pvz., galite sukurti atvirų jūsų organizacijos pareigų įgūdžių išdėstymo šabloną.</span><span class="sxs-lookup"><span data-stu-id="30f68-134">For example, you could create a skill-mapping profile for an open position in your organization.</span></span> <span data-ttu-id="30f68-135">Sukurdami tam tikros užduoties šabloną ir iš tos užduoties įgūdžius, išsilavinimą ir sertifikatus nukopijuodami į šabloną galite greitai ieškoti darbuotojų, pretendentų ir kontaktinių asmenų, kurie atitinka vieną arba daugiau šablone įvestų kriterijų, ir peržiūrėti kandidatų, kurių įgūdžiai labiausiai atitinka įgūdžių, reikalingų užduočiai atlikti, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="30f68-135">By creating a profile for a particular job and copying the skills, education and certificates from that job to the profile, you can quickly search workers, applicants and contact persons who match one or more of the criteria entered on the profile and view a list of the candidates whose skills most closely match the skills required for the job.</span></span>

> <span data-ttu-id="30f68-136">**Pastaba.** Tik darbuotojai, pretendentai ir kontaktiniai asmenys, kurie pasirinkti būti įtraukti į įgūdžių išdėstymo ieškas, gali būti rodomi įgūdžių ieškos rezultatų sąraše arba įtraukti į įgūdžių šabloną.</span><span class="sxs-lookup"><span data-stu-id="30f68-136">**Note** Only workers, applicants, and contact persons who are selected to be included in skill mapping searches can be displayed in a skill-mapping results list, or included in a skill profile.</span></span> <span data-ttu-id="30f68-137">Norėdami į įgūdžių išdėstymo ieškas įtraukti darbuotoją, pretendentą arba kontaktinį asmenį, toliau nurodytuose puslapiuose nustatykite parinktį **Įtraukti į įgūdžių išdėstymą** į Taip.</span><span class="sxs-lookup"><span data-stu-id="30f68-137">To include a worker, applicant, or contact person in skill mapping searches, set the **Include in skill mapping** selection to Yes in the following pages:</span></span>
> 
> + <span data-ttu-id="30f68-138">Darbuotojas</span><span class="sxs-lookup"><span data-stu-id="30f68-138">Worker</span></span>
> + <span data-ttu-id="30f68-139">Darbuotojas</span><span class="sxs-lookup"><span data-stu-id="30f68-139">Employee</span></span>
> + <span data-ttu-id="30f68-140">Pretendentas</span><span class="sxs-lookup"><span data-stu-id="30f68-140">Applicant</span></span>
> + <span data-ttu-id="30f68-141">Kontaktai</span><span class="sxs-lookup"><span data-stu-id="30f68-141">Contacts</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="30f68-142">Įgūdžių trūkumo analizė ir įgūdžių profilio analizė</span><span class="sxs-lookup"><span data-stu-id="30f68-142">Skill gap analysis and skill profile analysis</span></span>
<span data-ttu-id="30f68-143">Galite sukurti įgūdžių šablono analizę ir peržiūrėti darbuotojo, pretendento arba kontaktinio asmens kompetencijų sąrašą pagal konkrečią datą.</span><span class="sxs-lookup"><span data-stu-id="30f68-143">You can create a skill profile analysis to view a list of the competencies of a worker, applicant, or contact person as of a specific date.</span></span> <span data-ttu-id="30f68-144">Galite sukurti įgūdžių trūkumo analizę ir palyginti asmens įgūdžius su įgūdžiais, kurių reikia konkrečiam darbui.</span><span class="sxs-lookup"><span data-stu-id="30f68-144">You can create a skill gap analysis to compare a person’s skills and the skills that are required for a specific job.</span></span>  



<a name="see-also"></a><span data-ttu-id="30f68-145">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="30f68-145">See also</span></span>
--------

[<span data-ttu-id="30f68-146">Žmogiškieji ištekliai</span><span class="sxs-lookup"><span data-stu-id="30f68-146">Human resources</span></span>](index.md)




