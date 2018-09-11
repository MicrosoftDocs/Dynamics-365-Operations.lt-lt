--- 
title: "Įvesti pretendento ir prašymo duomenis neautomatiškai"
description: "Ši procedūra nurodo, kaip rankiniu būdu tvarkyti informaciją apie pretendentus ir jų prašymus."
author: kherr75
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmApplicant, LogisticsContactInfoGrid, HRMApplication,  DirPartyTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 27f9c43f517e85a6196beed3165680cf5a6185ca
ms.contentlocale: lt-lt
ms.lasthandoff: 09/11/2018

---
# <a name="enter-applicant-and-application-data-manually"></a><span data-ttu-id="bbae4-103">Įvesti pretendento ir prašymo duomenis neautomatiškai</span><span class="sxs-lookup"><span data-stu-id="bbae4-103">Enter applicant and application data manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bbae4-104">Ši procedūra nurodo, kaip rankiniu būdu tvarkyti informaciją apie pretendentus ir jų prašymus.</span><span class="sxs-lookup"><span data-stu-id="bbae4-104">This procedure shows how to manually maintain information about applicants and their application.</span></span>   <span data-ttu-id="bbae4-105">Galite įvesti ir tvarkyti pretendentų asmeninę informaciją, pokalbių datas ir laikus, nuorodas, kompetencijas ir patogumų užklausas.</span><span class="sxs-lookup"><span data-stu-id="bbae4-105">You can enter and maintain personal information, interview dates and times, references, competencies, and accommodation requests for applicants.</span></span> <span data-ttu-id="bbae4-106">Taip pat galima atnaujinti pretendentų prašymų priimti į darbą būseną ir bendrauti su pretendentais laiškais arba el. laiškais.</span><span class="sxs-lookup"><span data-stu-id="bbae4-106">You can also update the status of applicants’ applications for employment and create letters or email messages to communicate with applicants.</span></span> <span data-ttu-id="bbae4-107">Kuriant pretendento įrašą, sukuriamas to pretendento asmens įrašas visuotinėje adresų knygelėje.</span><span class="sxs-lookup"><span data-stu-id="bbae4-107">When you create an applicant record, a person record for that applicant is created in the global address book.</span></span>       <span data-ttu-id="bbae4-108">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="bbae4-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-new-applicant-record"></a><span data-ttu-id="bbae4-109">Sukurti naują pretendento įrašą</span><span class="sxs-lookup"><span data-stu-id="bbae4-109">Create a new applicant record</span></span>
1. <span data-ttu-id="bbae4-110">Pasirinkite Personalas > Įdarbinimas > Pretendentai > Pretendentai.</span><span class="sxs-lookup"><span data-stu-id="bbae4-110">Go to Human resources > Recruitment > Applicants > Applicants.</span></span>
2. <span data-ttu-id="bbae4-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bbae4-111">Click New.</span></span>
3. <span data-ttu-id="bbae4-112">Lauke Vardas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bbae4-112">In the First name field, type a value.</span></span>
4. <span data-ttu-id="bbae4-113">Lauke Pavardė surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bbae4-113">In the Last name field, type a value.</span></span>
    * <span data-ttu-id="bbae4-114">Galite įvesti papildomą pretendento informaciją, jei tokia yra.</span><span class="sxs-lookup"><span data-stu-id="bbae4-114">You can enter additional applicant information if it's available.</span></span> <span data-ttu-id="bbae4-115">Pvz., informacija gali apimti pretendento aukščiausią laipsnį, dabartinio darbo pavadinimą arba ankstesnį darbdavį.</span><span class="sxs-lookup"><span data-stu-id="bbae4-115">For example, information can include the applicant's highest degree, current job title, or previous employer.</span></span>  
5. <span data-ttu-id="bbae4-116">Perjunkite skyriaus „Kontaktinė informacija“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="bbae4-116">Toggle the expansion of the Contact information section.</span></span>
6. <span data-ttu-id="bbae4-117">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="bbae4-117">Click Add.</span></span>
7. <span data-ttu-id="bbae4-118">Lauke „Aprašas“ įveskite „Kontaktinis el. paštas“.</span><span class="sxs-lookup"><span data-stu-id="bbae4-118">In the Description field, type 'Communications email'.</span></span>
8. <span data-ttu-id="bbae4-119">Lauke „Tipas“ pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="bbae4-119">In the Type field, select an option.</span></span>
9. <span data-ttu-id="bbae4-120">Lauke „Kontaktinis numeris / adresas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bbae4-120">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="bbae4-121">Šis el. pašto adresas bus naudojamas susirašinėti su pretendentu el. laiškais.</span><span class="sxs-lookup"><span data-stu-id="bbae4-121">This email address will be used to generate email communication with the applicant.</span></span>  
10. <span data-ttu-id="bbae4-122">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="bbae4-122">Click Add.</span></span>
11. <span data-ttu-id="bbae4-123">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bbae4-123">In the Description field, type a value.</span></span>
12. <span data-ttu-id="bbae4-124">Lauke „Kontaktinis numeris / adresas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bbae4-124">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="bbae4-125">Pretendento asmeninė informacija.</span><span class="sxs-lookup"><span data-stu-id="bbae4-125">Applicant personal information.</span></span>  
    * <span data-ttu-id="bbae4-126">Jei reikia, galite įvesti papildomą pretendento asmeninę informaciją.</span><span class="sxs-lookup"><span data-stu-id="bbae4-126">You can enter additional personal information for the applicant, if needed.</span></span> <span data-ttu-id="bbae4-127">Pvz., tai gali būti gimimo data, etninė kilmė, lytis ar šeimyninė padėtis.</span><span class="sxs-lookup"><span data-stu-id="bbae4-127">For example, this can include birth date, ethnic origin, gender, or marital status.</span></span>  
13. <span data-ttu-id="bbae4-128">Veiksmų srityje spustelėkite „Kompetencijos“.</span><span class="sxs-lookup"><span data-stu-id="bbae4-128">On the Action Pane, click Competencies.</span></span>
    * <span data-ttu-id="bbae4-129">Galite įvesti pretendento kompetencijos profilį, įskaitant jo įgūdžius, profesinę patirtį, išsilavinimą, bandymus arba sertifikatus.</span><span class="sxs-lookup"><span data-stu-id="bbae4-129">You can enter the applicant's competency profile, including their skills, professional experiences, education, tests, or certificates.</span></span>  
    * <span data-ttu-id="bbae4-130">Šią informaciją galima panaudoti susiejant pretendento įgūdžius su įgūdžiais, susietais su jūsų įmonės duomenyse apibrėžtomis užduotimis.</span><span class="sxs-lookup"><span data-stu-id="bbae4-130">This information can be used to map the applicant's skills to the skills associated with the jobs defined in your company's data.</span></span>   

## <a name="create-an-application-for-the-applicant"></a><span data-ttu-id="bbae4-131">Sukurti pretendento prašymą</span><span class="sxs-lookup"><span data-stu-id="bbae4-131">Create an application for the applicant</span></span>
1. <span data-ttu-id="bbae4-132">Spustelėkite „Prašymai“.</span><span class="sxs-lookup"><span data-stu-id="bbae4-132">Click Applications.</span></span>
2. <span data-ttu-id="bbae4-133">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bbae4-133">Click New.</span></span>
3. <span data-ttu-id="bbae4-134">Lauke „Įdarbinimo projektas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bbae4-134">In the Recruitment project field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bbae4-135">Pasirinkus įdarbinimo projektą, pretendentas bus susietas su konkrečia į tą įdarbinimo projektą įtraukta siūloma darbo vieta.</span><span class="sxs-lookup"><span data-stu-id="bbae4-135">By selecting a recruitment project, the applicant will be associated with a specific opening included in that recruitment project.</span></span>  
4. <span data-ttu-id="bbae4-136">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bbae4-136">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="bbae4-137">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bbae4-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="bbae4-138">Pagal numatytuosius nustatymus, užduotis ir padalinys priklauso nuo pasirinkto įdarbinimo projekto.</span><span class="sxs-lookup"><span data-stu-id="bbae4-138">By default, the job and department are based on the selected recruitment project.</span></span>  
6. <span data-ttu-id="bbae4-139">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bbae4-139">Click Save.</span></span>
    * <span data-ttu-id="bbae4-140">Įrašę paraišką, galite prie jos pridėti dokumentus, apimančius pretendento patirtį, premijas ir motyvacinį laišką.</span><span class="sxs-lookup"><span data-stu-id="bbae4-140">After saving the application, you can attach documents to it, including the applicant's experience, awards, and cover letter.</span></span>  


