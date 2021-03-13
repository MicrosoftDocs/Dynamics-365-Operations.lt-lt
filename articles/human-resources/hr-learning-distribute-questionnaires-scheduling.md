---
title: Platinti klausimynus naudojant planavimą
description: Klausimyno planavimo funkcija suteikia galimybę planuoti ir platinti klausimynus keliems respondentams.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0cd101bfe88ae1acb051ba11a676da66ef6a3db6
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115467"
---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="9179b-103">Platinti klausimynus naudojant planavimą</span><span class="sxs-lookup"><span data-stu-id="9179b-103">Distribute questionnaires using scheduling</span></span>

<span data-ttu-id="9179b-104">Klausimyno planavimo funkcija suteikia galimybę planuoti ir platinti klausimynus keliems respondentams.</span><span class="sxs-lookup"><span data-stu-id="9179b-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="9179b-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="9179b-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="9179b-106">Klausimyno grafiko kūrimas</span><span class="sxs-lookup"><span data-stu-id="9179b-106">Create a questionnaire schedule</span></span>

1. <span data-ttu-id="9179b-107">Pasirinkite Klausimynas > Platinti > Klausimynų grafikai.</span><span class="sxs-lookup"><span data-stu-id="9179b-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>

2. <span data-ttu-id="9179b-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="9179b-108">Click New.</span></span>

3. <span data-ttu-id="9179b-109">Lauke Planavimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9179b-109">In the Scheduling field, type a value.</span></span>

4. <span data-ttu-id="9179b-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9179b-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="9179b-111">Nustatykite grafiką į Anoniminis, jei atsakymai turėtų būti registruojami be su jais susietų vardų.</span><span class="sxs-lookup"><span data-stu-id="9179b-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="9179b-112">Parinktį Leisti anoniminius rezultatus pirmiausia reikia nustatyti personalo parametruose.</span><span class="sxs-lookup"><span data-stu-id="9179b-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  

5. <span data-ttu-id="9179b-113">Lauke Tipas pasirinkite planavimo tipą.</span><span class="sxs-lookup"><span data-stu-id="9179b-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="9179b-114">Šiame pavyzdyje naudojame pasitenkinimo tipą.</span><span class="sxs-lookup"><span data-stu-id="9179b-114">In this example we will use the Satisfaction type.</span></span>

6. <span data-ttu-id="9179b-115">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="9179b-115">In the list, find and select the desired record.</span></span>

7. <span data-ttu-id="9179b-116">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="9179b-116">In the list, click the link in the selected row.</span></span>

8. <span data-ttu-id="9179b-117">Lauke Data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="9179b-117">In the Date field, enter a date.</span></span>

9. <span data-ttu-id="9179b-118">Išplėskite skyrių Darbuotojų savitarnos el. paštas.</span><span class="sxs-lookup"><span data-stu-id="9179b-118">Expand the Email for employee self service section.</span></span>

10. <span data-ttu-id="9179b-119">Lauke „Tema“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9179b-119">In the Subject field, type a value.</span></span>

    * <span data-ttu-id="9179b-120">Pavyzdys: galimas klausimynas</span><span class="sxs-lookup"><span data-stu-id="9179b-120">Example: Questionnaire available</span></span>  

11. <span data-ttu-id="9179b-121">Lauke Tekstas įveskite el. laiško tekstą.</span><span class="sxs-lookup"><span data-stu-id="9179b-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="9179b-122">Atkreipkite dėmesį, kad kintamasis gali būti naudojamas sistemos reikšmėms pakeisti.</span><span class="sxs-lookup"><span data-stu-id="9179b-122">Note, the variable can be used to substitue values in the system.</span></span>

    * <span data-ttu-id="9179b-123">Pavyzdys: Gerb. %P%, prisijunkite prie darbuotojų savitarnos, kad užpildytumėte klausimyną apie darbuotojų sveikatą.</span><span class="sxs-lookup"><span data-stu-id="9179b-123">Example: Dear %P%, Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="9179b-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="9179b-124">Contoso</span></span>  

12. <span data-ttu-id="9179b-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="9179b-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="9179b-126">Naudokite sąrankos informaciją klausimynui (-ams) parinkti ir teikti užklausas respondentams pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="9179b-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>

1. <span data-ttu-id="9179b-127">Spustelėkite Sąrankos informacija.</span><span class="sxs-lookup"><span data-stu-id="9179b-127">Click Setup details.</span></span>

2. <span data-ttu-id="9179b-128">Sąraše pasirinkite užklausą klausimyno respondentams sistemoje ieškoti.</span><span class="sxs-lookup"><span data-stu-id="9179b-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>

    * <span data-ttu-id="9179b-129">Pavyzdys: darbuotojai</span><span class="sxs-lookup"><span data-stu-id="9179b-129">Example: Workers</span></span>  

3. <span data-ttu-id="9179b-130">Spustelėkite Peržiūrėti arba modifikuoti užklausą, norėdami pasirinkti konkrečius žmones arba koreguokite užklausą, kad rastumėte konkrečius kriterijus atitinkančių žmonių.</span><span class="sxs-lookup"><span data-stu-id="9179b-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>

    * <span data-ttu-id="9179b-131">Atkreipkite dėmesį, kad visi respondentai turi būti sistemos vartotojai.</span><span class="sxs-lookup"><span data-stu-id="9179b-131">Note that all respondents must also be users in the system.</span></span>  

4. <span data-ttu-id="9179b-132">Sąraše pažymėkite asmens eilutę.</span><span class="sxs-lookup"><span data-stu-id="9179b-132">In the list, mark the row for Person</span></span>

5. <span data-ttu-id="9179b-133">Lauke Kriterijai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9179b-133">In the Criteria field, enter or select a value.</span></span>

    * <span data-ttu-id="9179b-134">Pasirinkite Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="9179b-134">Select Julia Funderburk</span></span>  

6. <span data-ttu-id="9179b-135">Sąraše pasirinkite Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="9179b-135">In the list, select Julia Funderburk</span></span>

7. <span data-ttu-id="9179b-136">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9179b-136">Click OK.</span></span>

8. <span data-ttu-id="9179b-137">Spustelėkite skirtuką Klausimynai.</span><span class="sxs-lookup"><span data-stu-id="9179b-137">Click the Questionnaires tab.</span></span>

9. <span data-ttu-id="9179b-138">Medyje išplėskite dalį pasitenkinimo apklausos tipo klausimyno mazgas.</span><span class="sxs-lookup"><span data-stu-id="9179b-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>

10. <span data-ttu-id="9179b-139">Medyje pažymėkite Darbuotojų sveikatos įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="9179b-139">In the tree, check 'Workforce Health Assessment'.</span></span>

11. <span data-ttu-id="9179b-140">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9179b-140">Click OK.</span></span>

12. <span data-ttu-id="9179b-141">Spustelėkite Planuojamas atsakymų seansas.</span><span class="sxs-lookup"><span data-stu-id="9179b-141">Click Planned answer session.</span></span>

    * <span data-ttu-id="9179b-142">Atkreipkite dėmesį, kad funkcija Planuojamas atsakymų seansas sukuriama kiekvienam pažymėtam / užklaustam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="9179b-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  

13. <span data-ttu-id="9179b-143">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9179b-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="9179b-144">Pradėkite klausimyno grafiką, kad respondentai galėtų klausimyną užpildyti.</span><span class="sxs-lookup"><span data-stu-id="9179b-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>

1. <span data-ttu-id="9179b-145">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="9179b-145">Click Functions.</span></span>

2. <span data-ttu-id="9179b-146">Spustelėkite Pradėti.</span><span class="sxs-lookup"><span data-stu-id="9179b-146">Click Start.</span></span>

3. <span data-ttu-id="9179b-147">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9179b-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="9179b-148">Siųskite respondentams el. laišką, informuojantį apie galimą klausimyną.</span><span class="sxs-lookup"><span data-stu-id="9179b-148">Send the email to inform respondents of the available questionnaire.</span></span>

1. <span data-ttu-id="9179b-149">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="9179b-149">Click Functions.</span></span>

2. <span data-ttu-id="9179b-150">Spustelėkite Siųsti el. laišką.</span><span class="sxs-lookup"><span data-stu-id="9179b-150">Click Send email.</span></span>

3. <span data-ttu-id="9179b-151">Spustelėkite Atšaukti.</span><span class="sxs-lookup"><span data-stu-id="9179b-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="9179b-152">Naudokite funkciją Suplanuotas atsakymų seansas, norėdami stebėti, kas turi užpildyti klausimyną.</span><span class="sxs-lookup"><span data-stu-id="9179b-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>

1. <span data-ttu-id="9179b-153">Spustelėkite Planuojamas atsakymų seansas.</span><span class="sxs-lookup"><span data-stu-id="9179b-153">Click Planned answer session.</span></span>

    * <span data-ttu-id="9179b-154">Panaikinkite visus likusius suplanuotus atsakymų seansus, kai esate pasirengę baigti suplanuotą seansą.</span><span class="sxs-lookup"><span data-stu-id="9179b-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  

2. <span data-ttu-id="9179b-155">Spustelėkite Naikinti.</span><span class="sxs-lookup"><span data-stu-id="9179b-155">Click Delete.</span></span>

3. <span data-ttu-id="9179b-156">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="9179b-156">Click Yes.</span></span>

4. <span data-ttu-id="9179b-157">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9179b-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="9179b-158">Baikite grafiką, kai visi respondentai užpildė klausimyną ir (arba) panaikinti visi likę suplanuoti atsakymų seansai.</span><span class="sxs-lookup"><span data-stu-id="9179b-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>

1. <span data-ttu-id="9179b-159">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="9179b-159">Click Functions.</span></span>
2. <span data-ttu-id="9179b-160">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="9179b-160">Click End.</span></span>
3. <span data-ttu-id="9179b-161">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9179b-161">Click OK.</span></span>

