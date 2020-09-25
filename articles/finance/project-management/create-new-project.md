---
title: Kurti naują projektą
description: Šioje temoje pateikiama informacija apie tai, kaip kurti naują projektą.
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
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760613"
---
# <a name="create-a-new-project"></a><span data-ttu-id="bcfad-103">Kurti naują projektą</span><span class="sxs-lookup"><span data-stu-id="bcfad-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bcfad-104">Norėdami sukurti naują projektą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="bcfad-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="bcfad-105">Puslapyje **Projektų valdymas** pasirinkite **Naujas projektas** ir įveskite tolesnes reikšmes.</span><span class="sxs-lookup"><span data-stu-id="bcfad-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="bcfad-106">**Projekto tipas:** Laiko ir medžiagų.</span><span class="sxs-lookup"><span data-stu-id="bcfad-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="bcfad-107">**Projekto pavadinimas:** XYZ atnaujinimas, 2 etapas.</span><span class="sxs-lookup"><span data-stu-id="bcfad-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="bcfad-108">**Projekto grupė:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="bcfad-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="bcfad-109">**Projekto sutarties ID:** 00000002.</span><span class="sxs-lookup"><span data-stu-id="bcfad-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="bcfad-110">Pasirinkite **Kurti projektą**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="bcfad-111">Ištekliaus priskyrimas projektui</span><span class="sxs-lookup"><span data-stu-id="bcfad-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="bcfad-112">Puslapyje **Darbuotojai**, sąraše **Darbuotojai** pasirinkite darbuotojo, kurio kompetencijas nustatėte anksčiau, įrašą ir jį atidarykite.</span><span class="sxs-lookup"><span data-stu-id="bcfad-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="bcfad-113">Veiksmų srityje, skirtuke **Projektas**, grupėje **Nustatymas** pasirinkite **Priskirti projektus**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="bcfad-114">Puslapio **Išteklių tikrinimo projekto priskyrimai** skirtuko **Projektai** lauke **Įtraukti projektą į pasirinktus projektus** taikykite filtrą projektui **XYZ atnaujinimas, 2 etapas**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="bcfad-115">Srityje **Likę projektai** pasirinkite projektą ir, pasirinkdami rodyklės mygtuką, jį įtraukite į sritį **Pasirinkti projektai**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="bcfad-116">Taip pat galite pagal poreikį ištekliui priskirti kategorijų.</span><span class="sxs-lookup"><span data-stu-id="bcfad-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="bcfad-117">Kategorijos tipas gali būti **Išlaidos** arba **Įplaukos**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="bcfad-118">Kategorijos tipą nustato jūsų organizacija.</span><span class="sxs-lookup"><span data-stu-id="bcfad-118">The category type is determined by your organization.</span></span> <span data-ttu-id="bcfad-119">Jei ištekliui kategorijų nepriskirta, „Finance“ suranda numatytąją išlaidų ir įplaukų valandos kainų kategoriją.</span><span class="sxs-lookup"><span data-stu-id="bcfad-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="bcfad-120">Projekto išteklių ir vaidmenų charakteristikų nustatymas</span><span class="sxs-lookup"><span data-stu-id="bcfad-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="bcfad-121">Naudodamas projektų išteklių funkcijas projekto vadovas gali kurti reikiamus projekto vaidmenis.</span><span class="sxs-lookup"><span data-stu-id="bcfad-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="bcfad-122">Vaidmenys gali būti naudojami, jei rezervuojant išteklius vis dar nežinomi patvirtinti ištekliai.</span><span class="sxs-lookup"><span data-stu-id="bcfad-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="bcfad-123">Vaidmenis galima laikinai rezervuoti kaip planuotus išteklius, kad būtų galima vykdyti kitus projekto planavimo etapus.</span><span class="sxs-lookup"><span data-stu-id="bcfad-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="bcfad-124">[![Vaidmens pavyzdys](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="bcfad-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="bcfad-125">**Scenarijus:** „Contoso‟ buvo pasamdyta atlikti laiko ir medžiagų projektui su patvirtinta chartija.</span><span class="sxs-lookup"><span data-stu-id="bcfad-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="bcfad-126">Jaunesnysis projektų vadovas vis dar nustatinėja projekto sritį.</span><span class="sxs-lookup"><span data-stu-id="bcfad-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="bcfad-127">Išteklių vadovas šiuo metu identifikuoja konkrečius išteklius, kurie bus rezervuoti naujojo projekto darbui.</span><span class="sxs-lookup"><span data-stu-id="bcfad-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="bcfad-128">Dėl projekto svarbos projekto rėmėjas kaip vieno iš vaidmenų pageidavo vaidmens Vyresnysis projektų vadovas.</span><span class="sxs-lookup"><span data-stu-id="bcfad-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="bcfad-129">Išteklių vadovas turi gauti naująjį išteklių ir apibrėžti vaidmenį sistemoje – tam atvejui, jei, planuojant projektą, jaunesniajam projektų vadovui prireiktų informacijos apie išteklius.</span><span class="sxs-lookup"><span data-stu-id="bcfad-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="bcfad-130">Tolesniais veiksmais rodoma, kaip išteklių vadovas gali nustatyti Vyresniojo projektų vadovo vaidmenį ir susieti su juo išteklių charakteristikas.</span><span class="sxs-lookup"><span data-stu-id="bcfad-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="bcfad-131">Vėliau vaidmenį galima naudoti ieškant turimų išteklių, kurie atitinka reikiamas išteklių kompetencijas.</span><span class="sxs-lookup"><span data-stu-id="bcfad-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="bcfad-132">Puslapyje **Nustatyti vaidmenis** pasirinkite **Naujas** ir įveskite tolesnes reikšmes.</span><span class="sxs-lookup"><span data-stu-id="bcfad-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="bcfad-133">**Vaidmens ID:** Vyresnysis projektų vadovas.</span><span class="sxs-lookup"><span data-stu-id="bcfad-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="bcfad-134">**Aprašas:** Vyresnysis projektų vadovas.</span><span class="sxs-lookup"><span data-stu-id="bcfad-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="bcfad-135">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-135">Select **Create**.</span></span>
3. <span data-ttu-id="bcfad-136">Pasirinkite vaidmenį **Vyresnysis projektų vadovas**, tada – **Konfigūruoti charakteristikas**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="bcfad-137">Lauke **Charakteristikų tipas** pasirinkite **Įgūdis**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="bcfad-138">Lauke **Pasiekiamos charakteristikos** įveskite ieškotiną įgūdį.</span><span class="sxs-lookup"><span data-stu-id="bcfad-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="bcfad-139">Lauke **Charakteristikos tipas** pasirinkite **Sertifikatas**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="bcfad-140">Lauke **Pasiekiamos charakteristikos** įveskite ieškotino sertifikato tipą.</span><span class="sxs-lookup"><span data-stu-id="bcfad-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="bcfad-141">Projekto ištekliaus priskyrimas projektui</span><span class="sxs-lookup"><span data-stu-id="bcfad-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="bcfad-142">Puslapyje **Visi projektai** pasirinkite projektą **XYZ atnaujinimas, 2 etapas**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="bcfad-143">Skirtuke **Projekto komanda ir planavimas** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="bcfad-144">Lauke **Vaidmuo** pasirinkite **Komandos narys**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="bcfad-145">Pasirinkite **Rezervuoti kalendoriuje**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="bcfad-146">Puslapyje **Išteklių pasiekiamumas** pasirinkite **Rodinio parametrai**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="bcfad-147">Puslapyje **Koreguoti rodinio parametrus** įveskite tolesnes reikšmes.</span><span class="sxs-lookup"><span data-stu-id="bcfad-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="bcfad-148">**Datų intervalo rodinio formatas:** Diena.</span><span class="sxs-lookup"><span data-stu-id="bcfad-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="bcfad-149">**Rodyti užimtumo aprašus:** Taip.</span><span class="sxs-lookup"><span data-stu-id="bcfad-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="bcfad-150">**Rodyti likusį pajėgumą:** Taip.</span><span class="sxs-lookup"><span data-stu-id="bcfad-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="bcfad-151">Išteklių sąraše pasirinkite išteklių.</span><span class="sxs-lookup"><span data-stu-id="bcfad-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="bcfad-152">Pasirinkite **Tiksliai planuoti užimtumą** ir **Visas pajėgumas**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="bcfad-153">Ištekliaus priskyrimas numatytajam vaidmeniui</span><span class="sxs-lookup"><span data-stu-id="bcfad-153">Assign a resource to a default role</span></span>

<span data-ttu-id="bcfad-154">Norint padėti projektų ar išteklių vadovams, galima dar labiau detalizuoti projektui galimus rezervuoti išteklius.</span><span class="sxs-lookup"><span data-stu-id="bcfad-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="bcfad-155">Numatytąjį vaidmenį galima susieti su esamu ištekliumi arba naujai gautu ištekliumi.</span><span class="sxs-lookup"><span data-stu-id="bcfad-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="bcfad-156">Pavyzdžiui, kai Danielis buvo priimtas į darbą, jo patirtis ir įgūdžiai buvo tinkami verslo analitiko vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="bcfad-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="bcfad-157">Išteklių vadovas priskyrė šį vaidmenį kaip numatytąjį Danielio vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="bcfad-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="bcfad-158">Todėl išteklių vadovas Danielį pridėjo į verslo analitikų, kurie gali dirbti su projektais, telkinį.</span><span class="sxs-lookup"><span data-stu-id="bcfad-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="bcfad-159">Rezervuodami išteklius projektų vadovai gali filtruoti vaidmenų išteklius, kurie gali dirbti su projektais.</span><span class="sxs-lookup"><span data-stu-id="bcfad-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="bcfad-160">Kai panaudodami išteklius vadovai atlieka kelių kriterijų sprendimų analizę, šią informaciją jie gali naudoti kaip vieną iš kriterijų.</span><span class="sxs-lookup"><span data-stu-id="bcfad-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="bcfad-161">Jie taip pat gali į filtrą įtraukti kitų išteklių charakteristikų ir ieškoti išteklių, turinčių konkrečių įgūdžių, išsilavinimą ir patirties konkrečiam projektui atlikti.</span><span class="sxs-lookup"><span data-stu-id="bcfad-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="bcfad-162">**Scenarijus:** pradėtas patvirtintas projektas ir projekto planavimo etape kaip planuoti ištekliai buvo rezervuotas vyresniojo projekto vadovo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="bcfad-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="bcfad-163">Išteklių vadovas gavo išteklių užimti vyresniojo projekto vadovo vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="bcfad-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="bcfad-164">Puslapyje **Išteklių sąrašas** pasirinkite **Danielis Goldschmidtas**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="bcfad-165">Puslapyje **Ištekliaus vaidmuo** pasirinkite **Naujas** ir įveskite tolesnes reikšmes.</span><span class="sxs-lookup"><span data-stu-id="bcfad-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="bcfad-166">**Įsigalioja:** įveskite dabartinę datą.</span><span class="sxs-lookup"><span data-stu-id="bcfad-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="bcfad-167">**Galiojimo pabaiga:** įveskite **Niekada**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="bcfad-168">**Vaidmuo:** įveskite **Vyresnysis projektų vadovas**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="bcfad-169">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bcfad-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="bcfad-170">Skirtuke **Kompetencijos** pridėkite įgūdį **ProjektVald** ir sertifikatą **PMP**.</span><span class="sxs-lookup"><span data-stu-id="bcfad-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
