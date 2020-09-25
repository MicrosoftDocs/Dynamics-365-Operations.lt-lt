---
title: Projektų išteklių nustatymas
description: Šioje temoje pateikiama informacija apie projekto išteklių nustatymą arba prašymą.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760618"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="b4000-103">Projektų išteklių nustatymas</span><span class="sxs-lookup"><span data-stu-id="b4000-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4000-104">Turite nustatyti kalendorių ir jį susieti su darbuotoju.</span><span class="sxs-lookup"><span data-stu-id="b4000-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="b4000-105">Kalendorius naudojamas projektui planuoti ir projektui rezervuotų išteklių darbo laikui.</span><span class="sxs-lookup"><span data-stu-id="b4000-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="b4000-106">Nustatydami kalendorių ir optimizuodami išteklius projektų vadovai gali koreguoti išteklių paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="b4000-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="b4000-107">Atsižvelgiant į kalendoriaus grafiką, ištekliams gali būti taikomi apribojimai.</span><span class="sxs-lookup"><span data-stu-id="b4000-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="b4000-108">Puslapyje **Kalendoriai** galite nustatyti kalendorių.</span><span class="sxs-lookup"><span data-stu-id="b4000-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="b4000-109">Kai darbuotoją nustatote kaip projekto išteklių, galite pasirinkti iš įmonėje, kuriai nustatote išteklius, dirbančių darbuotojų.</span><span class="sxs-lookup"><span data-stu-id="b4000-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="b4000-110">Taip pat galite pasirinkti iš kitų savo organizacijos įmonių darbuotojų.</span><span class="sxs-lookup"><span data-stu-id="b4000-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="b4000-111">Šie darbuotojai vadinami vidiniais įmonės ištekliais.</span><span class="sxs-lookup"><span data-stu-id="b4000-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="b4000-112">Toliau nurodytose procedūrose paaiškinama, kaip savo įmonėje nustatyti darbuotoją kaip projekto išteklių ir kaip nustatyti vidinį įmonės projekto išteklių.</span><span class="sxs-lookup"><span data-stu-id="b4000-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="b4000-113">Darbuotojo nustatymas projekto ištekliumi</span><span class="sxs-lookup"><span data-stu-id="b4000-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="b4000-114">Puslapio **Darbuotojai** sąraše **Darbuotojai** pasirinkite darbuotoją, kurį pridedate kaip projekto išteklių, ir atidarykite darbuotojo įrašą.</span><span class="sxs-lookup"><span data-stu-id="b4000-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="b4000-115">Veiksmų srityje pasirinkite **Projektas** &gt; **Sąranka** &gt; **Projekto sąranka**.</span><span class="sxs-lookup"><span data-stu-id="b4000-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="b4000-116">Pasirinkite kalendorių ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b4000-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="b4000-117">Kaip išankstinio priskyrimo tipą taip pat galite nurodyti numatytuosius ištekliaus projektus.</span><span class="sxs-lookup"><span data-stu-id="b4000-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="b4000-118">Išankstiniai priskyrimai gali būti naudojami, kai išteklių vadovas ar projekto vadovas iš anksto žino, su kuriais projektais dirbs išteklius.</span><span class="sxs-lookup"><span data-stu-id="b4000-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="b4000-119">Išankstiniai priskyrimai taip pat gali būti paremti projekto rėmėjo ar kliento prašymu.</span><span class="sxs-lookup"><span data-stu-id="b4000-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="b4000-120">Norėdami iš anskto priskirti projektą, puslapyje **Priskirti projektus**, skirtuke **Projektai**, sąraše **Likę projektai** pasirinkite atitinkamą projektą.</span><span class="sxs-lookup"><span data-stu-id="b4000-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="b4000-121">Vidinių įmonės išteklių nustatymas</span><span class="sxs-lookup"><span data-stu-id="b4000-121">Set up an intercompany resource</span></span>

<span data-ttu-id="b4000-122">Kai nustatote darbuotoją kaip vidinį įmonės išteklių, turite užbaigti sąranką tiek skolinančioje įmonėje, tiek besiskolinančioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="b4000-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="b4000-123">Skolinančioje įmonėje</span><span class="sxs-lookup"><span data-stu-id="b4000-123">In the lending company</span></span>

1. <span data-ttu-id="b4000-124">Jei naudojate „Finance“, patikrinkite, ar pasirinkta skolinanti įmonė, o po to atlikite ankstesniame skyriuje nurodytą procedūrą „Darbuotojo nustatymas projekto ištekliumi“.</span><span class="sxs-lookup"><span data-stu-id="b4000-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="b4000-125">Puslapyje **Įmonės vidaus apskaita** pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b4000-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="b4000-126">Lauke **Juridinio subjekto ID** pasirinkite skolinančią įmonę.</span><span class="sxs-lookup"><span data-stu-id="b4000-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="b4000-127">Atitinkamai užpildykite likusius laukus ir pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b4000-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="b4000-128">Puslapyje **Perkėlimo kaina** pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b4000-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="b4000-129">Lauke **Besiskolinantis juridinis subjektas** pasirinkite atitinkamą įmonę.</span><span class="sxs-lookup"><span data-stu-id="b4000-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="b4000-130">Norėdami besiskolinančiai įmonei paskolinti tik tą išteklių, kurį sukūrėte šio skyriaus pradžioje, lauke **Išteklius** pasirinkite sukurto ištekliaus pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="b4000-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="b4000-131">Norėdami, kad besiskolinančiai įmonei būtų prieinami visi ištekliai, lauką **Išteklius** palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="b4000-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="b4000-132">Puslapio **Projektų valdymo ir apskaitos parametrai** skirtuke **Vidinė įmonė** parinktį **Įjungti vidinės įmonės išteklių planavimą ir tabelius** nustatykite kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="b4000-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="b4000-133">Besiskolinančioje įmonėje</span><span class="sxs-lookup"><span data-stu-id="b4000-133">In the borrowing company</span></span>

- <span data-ttu-id="b4000-134">Puslapyje **Išteklių sąrašas**, ieškos filtre įveskite sukurto skolinančiai įmonei skirto ištekliaus pavadinimą, kad patikrintumėte, ar pavadinimas įtrauktas į besiskolinančiai įmonei skirtą išteklių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="b4000-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="b4000-135">Projektų išteklių prašymas</span><span class="sxs-lookup"><span data-stu-id="b4000-135">Request project resources</span></span>
<span data-ttu-id="b4000-136">Projektų išteklių planavimo funkcija gali naudotis tik išteklių vadovai, norėdami platinti personalo išteklius įsipareigojimuose arba projektuose.</span><span class="sxs-lookup"><span data-stu-id="b4000-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="b4000-137">Norėdami įjungti šią funkciją, atlikite toliau nurodytas užduotis arba patvirtinkite, kad jos atliktos.</span><span class="sxs-lookup"><span data-stu-id="b4000-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="b4000-138">Nustatyti numeracijas.</span><span class="sxs-lookup"><span data-stu-id="b4000-138">Set up number sequences.</span></span>
- <span data-ttu-id="b4000-139">Nustatyti projektų valdymo ir apskaitos darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="b4000-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="b4000-140">Įjunkite išteklių užklausų darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="b4000-140">Enable resource request workflows.</span></span>

<span data-ttu-id="b4000-141">Atlikę pirmiau nurodytas užduotis, galite atlikti reikiamas kitas užduotis.</span><span class="sxs-lookup"><span data-stu-id="b4000-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="b4000-142">Sukurkite išteklių užklausą iš apytiksliai suplanuotų personalo išteklių.</span><span class="sxs-lookup"><span data-stu-id="b4000-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="b4000-143">Stebėti išteklių užklausas.</span><span class="sxs-lookup"><span data-stu-id="b4000-143">Monitor resource requests.</span></span>
- <span data-ttu-id="b4000-144">Vykdyti išteklių užklausas.</span><span class="sxs-lookup"><span data-stu-id="b4000-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="b4000-145">Pateikti personalo ištekliaus iš WBS užklausą.</span><span class="sxs-lookup"><span data-stu-id="b4000-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="b4000-146">Užregistruokite išteklius projektui nepateikdami personalo išteklių užklausos.</span><span class="sxs-lookup"><span data-stu-id="b4000-146">Book resources to a project without having a request for a staffed resource.</span></span>
