---
title: Nustatyti ir sukurti pretendentų atrankos priemones
description: Rasti kvalifikuotų kandidatų telkinį laisvoms vietoms užimti gali būti sunku, ypač, kai pareigoms reikalingas unikalus įgūdžių rinkinys.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmSkillMapping, HcmJobLookup, HcmSkillMappingLine, HcmPersonCertificate, CCHTMLPrintPreview
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4e7ed6feaa1b5b27fcfc0ec99a2d75415fe7d6a
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693069"
---
# <a name="identify-and-deploy-candidate-selection-tools"></a><span data-ttu-id="51803-103">Nustatyti ir sukurti pretendentų atrankos priemones</span><span class="sxs-lookup"><span data-stu-id="51803-103">Identify and deploy candidate selection tools</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="51803-104">Rasti kvalifikuotų kandidatų telkinį laisvoms vietoms užimti gali būti sunku, ypač, kai pareigoms reikalingas unikalus įgūdžių rinkinys.</span><span class="sxs-lookup"><span data-stu-id="51803-104">Finding a qualified pool of candidates to fill vacancies can be difficult, especially when a position requires a unique set of skills.</span></span>  <span data-ttu-id="51803-105">Tačiau gali būti, kad kandidatai su reikiamais įgūdžiais jau dirba jūsų organizacijoje.</span><span class="sxs-lookup"><span data-stu-id="51803-105">However, candidates with the skills you need might already be employed in your organization.</span></span> <span data-ttu-id="51803-106">Konkretaus įgūdžių rinkinio galite ieškoti tarp esamų darbuotojų arba naujų pretendentų.</span><span class="sxs-lookup"><span data-stu-id="51803-106">You can search for a specific skill set among existing employees, or new applicants.</span></span> <span data-ttu-id="51803-107">Tai darbdaviui leidžia greitai surinkti ir peržiūrėti pretendentus, kurie į laisvas pareigas kandidatuoja dabar arba kandidatavo anksčiau, arba surasti potencialių kandidatų iš esamo darbuotojų telkinio.</span><span class="sxs-lookup"><span data-stu-id="51803-107">This allows a recruiter to quickly gather and screen applicants who have applied for open position now or in the past, or to find potential candidates from their existing pool of employees.</span></span> <span data-ttu-id="51803-108">Naudodami šį užduočių įrašymą galite sužinoti, kaip įgūdžių išdėstymo funkcijos gali padėti rasti tinkamą asmenį laisvoms pareigoms užimti.</span><span class="sxs-lookup"><span data-stu-id="51803-108">Use this task recording to learn how the skill mapping functionality can help you find the right person for an open position.</span></span> <span data-ttu-id="51803-109">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="51803-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="51803-110">Pasirinkite Personalas > Kompetencijos > Įgūdžių analizė > Įgūdžių išdėstymo profiliai.</span><span class="sxs-lookup"><span data-stu-id="51803-110">Go to Human resources > Competencies > Skill analysis > Skill mapping profiles.</span></span>
2. <span data-ttu-id="51803-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="51803-111">Click New.</span></span>
3. <span data-ttu-id="51803-112">Lauke Įgūdžių išdėstymas įveskite įgūdžių išdėstymo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="51803-112">In the Skill mapping field, enter a name for your skill mapping.</span></span>  <span data-ttu-id="51803-113">Pavyzdys: buhalteris.</span><span class="sxs-lookup"><span data-stu-id="51803-113">Example: Accountant.</span></span>
4. <span data-ttu-id="51803-114">Lauke Aprašas įveskite įgūdžių išdėstymo aprašą.</span><span class="sxs-lookup"><span data-stu-id="51803-114">In the Description field, enter a description of the skill mapping..</span></span>
5. <span data-ttu-id="51803-115">Lauke Data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="51803-115">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="51803-116">Spustelėkite Nuskaityti šabloną.</span><span class="sxs-lookup"><span data-stu-id="51803-116">Click Retrieve profile.</span></span>
    * <span data-ttu-id="51803-117">Kaip ieškos pagrindą naudokite funkciją Nuskaityti šabloną ir iš pasirinkto asmens, užduoties ar kurso nuskaitykite sertifikatą, įgūdžius ir švietimo duomenis.</span><span class="sxs-lookup"><span data-stu-id="51803-117">Use Retrieve profile to pull in the Certificate, Skill, and Education data from a selected Person, Job or Course as the basis for your search.</span></span>   <span data-ttu-id="51803-118">Tada galite pridėti arba pašalinti kriterijų, nurodyti, ar kriterijai yra pasirinktiniai, ir rikiuoti kriterijų svarbą.</span><span class="sxs-lookup"><span data-stu-id="51803-118">You can then add or remove criteria, state if the criteria is optional and rank the importance of the criteria.</span></span>  
7. <span data-ttu-id="51803-119">Spustelėkite Užduotis.</span><span class="sxs-lookup"><span data-stu-id="51803-119">Click Job.</span></span>
8. <span data-ttu-id="51803-120">Lauke Užduotis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="51803-120">In the Job field, enter or select a value.</span></span>
9. <span data-ttu-id="51803-121">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="51803-121">Click OK.</span></span>
10. <span data-ttu-id="51803-122">Išplėskite FastTab“ Diapazonas ir įtraukite bet kokią papildomą informaciją, pvz., padalinį.</span><span class="sxs-lookup"><span data-stu-id="51803-122">Expand the Range FastTab, and add any additional information, such as department.</span></span>
11. <span data-ttu-id="51803-123">Išplėtę „FastTab“ Sertifikatai, galėsite peržiūrėti arba redaguoti sertifikatus.</span><span class="sxs-lookup"><span data-stu-id="51803-123">Expand the Certificates FastTab to view or edit the certificates.</span></span>
12. <span data-ttu-id="51803-124">Išplėtę „FastTab“ Įgūdžiai, galėsite peržiūrėti arba redaguoti įgūdžius.</span><span class="sxs-lookup"><span data-stu-id="51803-124">Expand the Skills FastTab to view or edit the skills.</span></span>
13. <span data-ttu-id="51803-125">Išplėtę „FastTab“ Išsilavinimas, galėsite peržiūrėti arba redaguoti išsilavinimo kriterijus.</span><span class="sxs-lookup"><span data-stu-id="51803-125">Expand the Education FastTab to view or edit the education criteria.</span></span>
14. <span data-ttu-id="51803-126">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="51803-126">Click Execute.</span></span>
15. <span data-ttu-id="51803-127">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="51803-127">Click OK.</span></span>
16. <span data-ttu-id="51803-128">Spustelėkite Rezultatas.</span><span class="sxs-lookup"><span data-stu-id="51803-128">Click Result.</span></span>
17. <span data-ttu-id="51803-129">Spustelėkite Rezultatas.</span><span class="sxs-lookup"><span data-stu-id="51803-129">Click Result.</span></span>
18. <span data-ttu-id="51803-130">Spustelėkite Atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="51803-130">Click Resume.</span></span>
19. <span data-ttu-id="51803-131">Spustelėkite Sertifikatai.</span><span class="sxs-lookup"><span data-stu-id="51803-131">Click Certificates.</span></span>
    * <span data-ttu-id="51803-132">Galite detalizuoti kiekvieną išvardytą asmenį ir peržiūrėti išsamią informaciją apie jų išsilavinimą, įgūdžius, profesinę patirtį.</span><span class="sxs-lookup"><span data-stu-id="51803-132">You can drill further into each person listed and see details regarding their education, skills, and professional experience.</span></span>  
20. <span data-ttu-id="51803-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="51803-133">Close the page.</span></span>
21. <span data-ttu-id="51803-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="51803-134">Close the page.</span></span>
22. <span data-ttu-id="51803-135">Dar kartą pasirinkite rezultatą.</span><span class="sxs-lookup"><span data-stu-id="51803-135">Select result again.</span></span>
23. <span data-ttu-id="51803-136">Spustelėkite Ataskaita.</span><span class="sxs-lookup"><span data-stu-id="51803-136">Click Report.</span></span>
    * <span data-ttu-id="51803-137">Ataskaitoje geriausi atitikmenys bus pateikiami jos viršuje.</span><span class="sxs-lookup"><span data-stu-id="51803-137">The report will list the best matches at the top of the report.</span></span>  <span data-ttu-id="51803-138">Galite matyti, kad yra pateiktas tarpo elementas.</span><span class="sxs-lookup"><span data-stu-id="51803-138">You can see that a gap element is listed.</span></span>  <span data-ttu-id="51803-139">Tai yra skirtumas tarp lygio, kuris buvo pateiktas įgūdžių išdėstyme, ir įgūdžių, priskirtų asmeniui, lygio.</span><span class="sxs-lookup"><span data-stu-id="51803-139">This is the difference between the level that was listed on the skill mapping, and the level of the skill that is assigned to the person.</span></span>  
24. <span data-ttu-id="51803-140">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="51803-140">Close the page.</span></span>
25. <span data-ttu-id="51803-141">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="51803-141">Click Save.</span></span>

