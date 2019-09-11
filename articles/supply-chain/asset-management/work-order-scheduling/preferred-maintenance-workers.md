---
title: Nustatyti pageidaujamus priežiūros darbuotojus
description: Šioje temoje aiškinama, kaip nustatyti pageidaujamus priežiūros darbuotojus skiltyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887416"
---
# <a name="preferred-maintenance-workers"></a><span data-ttu-id="6db6b-103">Pageidaujami priežiūros darbuotojai</span><span class="sxs-lookup"><span data-stu-id="6db6b-103">Preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="6db6b-104">Planuodami darbo užsakymus galite nustatyti priežiūros darbuotojų pasirinkimo atlikti darbo užsakymą pirmumą.</span><span class="sxs-lookup"><span data-stu-id="6db6b-104">You can make a preference regarding which maintenance workers are allocated to complete work orders during work order scheduling.</span></span> <span data-ttu-id="6db6b-105">Ši funkcija yra nebūtina, tačiau ji gali būti naudinga sprendžiant dėl labiausiai kvalifikuoto priežiūros darbuotojo užduočiai atlikti, atsižvelgiant į darbuotojo įgūdžius ir kompetencijas.</span><span class="sxs-lookup"><span data-stu-id="6db6b-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="6db6b-106">Taigi, planuojant darbo užsakymą sąranka **Pageidaujami priežiūros darbuotojai** yra naudojama sprendžiant dėl konkretaus priežiūros darbuotojo ar darbo grupės skyrimo atlikti darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="6db6b-106">Therefore, during work order scheduling, the setup in **Preferred maintenance workers** is used to determine if a specific maintenance worker or worker group should be scheduled for a work order.</span></span> <span data-ttu-id="6db6b-107">Tik tie priežiūros darbuotojai, kurie yra pasiekiami planuojamo užsakymo metu, pateks į grafiką.</span><span class="sxs-lookup"><span data-stu-id="6db6b-107">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="6db6b-108">Jei planuojant užsakymą pageidaujamo priežiūros darbuotojo sąranka atitiks darbo užsakymą, bet priežiūros darbuotojas paskirtas atlikti kitus darbus, darbo užsakymas bus paskirtas kitam pasiekiamam priežiūros darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="6db6b-108">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another, available, maintenance worker.</span></span>

<span data-ttu-id="6db6b-109">Prieš pradedant nustatyti pageidaujamus priežiūros darbuotojus, pirmiausia turite nustatyti priežiūros darbuotojus ir darbo grupes, kurios yra pasiekiamos atrankai.</span><span class="sxs-lookup"><span data-stu-id="6db6b-109">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups that should be available for selection.</span></span> <span data-ttu-id="6db6b-110">Norėdami sužinoti, kaip nustatyti priežiūros darbuotojus ir darbo grupes žr. aprašą [Priežiūros darbuotojai ir darbo grupės](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="6db6b-110">Refer to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md) for a description on how to set up maintenance workers and worker groups.</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="6db6b-111">Pageidaujamų priežiūros darbuotojų sąranka</span><span class="sxs-lookup"><span data-stu-id="6db6b-111">Set up preferred workers</span></span>

<span data-ttu-id="6db6b-112">Pageidaujamas priežiūros darbuotojas ar darbo grupė gali būti susijusi konkrečiai su</span><span class="sxs-lookup"><span data-stu-id="6db6b-112">A preferred maintenance worker or worker group can be related to a specific</span></span>

- <span data-ttu-id="6db6b-113">prekyba</span><span class="sxs-lookup"><span data-stu-id="6db6b-113">trade</span></span>  
- <span data-ttu-id="6db6b-114">priežiūros užduoties tipo variantu</span><span class="sxs-lookup"><span data-stu-id="6db6b-114">maintenance job type variant</span></span>  
- <span data-ttu-id="6db6b-115">priežiūros užduoties tipu</span><span class="sxs-lookup"><span data-stu-id="6db6b-115">maintenance job type</span></span>  
- <span data-ttu-id="6db6b-116">priežiūros užduoties tipo kategorija</span><span class="sxs-lookup"><span data-stu-id="6db6b-116">maintenance job type category</span></span>  
- <span data-ttu-id="6db6b-117">turtas</span><span class="sxs-lookup"><span data-stu-id="6db6b-117">asset</span></span>  
- <span data-ttu-id="6db6b-118">turto tipu</span><span class="sxs-lookup"><span data-stu-id="6db6b-118">asset type</span></span>  

<span data-ttu-id="6db6b-119">arba šių atrankos kriterijų deriniu.</span><span class="sxs-lookup"><span data-stu-id="6db6b-119">or a combination of those selections.</span></span> <span data-ttu-id="6db6b-120">Kuo daugiau atrankos kriterijų sukursite tam pačiam įrašui, tuo konkretesnė bus sąranka.</span><span class="sxs-lookup"><span data-stu-id="6db6b-120">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="6db6b-121">Spustelėkite **Turto valdymas** > **Sąranka** > **Darbuotojai** > **Pageidaujami priežiūros darbuotojai**.</span><span class="sxs-lookup"><span data-stu-id="6db6b-121">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="6db6b-122">Spustelėję **Naujas** sukurkite naują įrašą.</span><span class="sxs-lookup"><span data-stu-id="6db6b-122">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="6db6b-123">Pradėkite sukurdami „numatytąją“ priežiūros darbuotojų arba darbo grupių sąranką, kurios laukuose nėra nustatyti atrankos kriterijai, kaip nurodyta viršutiniame ženklelių sąraše.</span><span class="sxs-lookup"><span data-stu-id="6db6b-123">Start by creating a "default" maintenance worker or worker group setup that has no selections in the fields shown in the bullet list above.</span></span> <span data-ttu-id="6db6b-124">Tokiu būdu jūs atrinksite tik naudodamiesi lauku **Pageidaujama priežiūros darbo grupė** arba lauku **Pageidaujamas priežiūros darbuotojas**.</span><span class="sxs-lookup"><span data-stu-id="6db6b-124">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="6db6b-125">Toliau paveikslėlyje galite matyti pavyzdį pirmajame įraše, kuriame „Užklausos“ pasirinktos kaip pageidaujama priežiūros darbo grupė.</span><span class="sxs-lookup"><span data-stu-id="6db6b-125">In the figure below, you see an example in the first record in which "Requests" is selected as preferred maintenance worker group.</span></span>

>[!NOTE]
><span data-ttu-id="6db6b-126">Numatytoji sąranka bus naudojama planuojant darbo užsakymą tokiu atveju, kai skiriant darbo užsakymą jokia kita, išsamesnė, kombinacija neatitinka darbo užsakymo turinio.</span><span class="sxs-lookup"><span data-stu-id="6db6b-126">The default setup will be used during work order scheduling in case no other, more specific, combination matches the contents of the work order during work order scheduling.</span></span>

4. <span data-ttu-id="6db6b-127">Kartokite 2 žingsnį, kad sukurtumėte naują įrašą.</span><span class="sxs-lookup"><span data-stu-id="6db6b-127">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="6db6b-128">Nustatykite reikiamus atrankos kriterijus priklausomai nuo išsamumo lygio pageidaujamam darbuotojui ar darbo grupei.</span><span class="sxs-lookup"><span data-stu-id="6db6b-128">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> <span data-ttu-id="6db6b-129">*Pavyzdys:* toliau paveikslėlyje, šeštame įraše, priežiūros darbuotojas Šonas Ričardsonas pasirenkamas kaip pageidaujamas darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="6db6b-129">*Example:* In the figure below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="6db6b-130">Jis bus automatiškai atrinktas planuojant darbo užsakymą, kuriame pateikiamas turtas CH-BP1-03-02, o priežiūros užduoties tipas – „Patalpų įvertinimas“, jei jis bus pasiekiamas grafike nustatytu laiku.</span><span class="sxs-lookup"><span data-stu-id="6db6b-130">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintennace job type "Facility assessment", if he is available at the scheduled time.</span></span>

>[!NOTE]
><span data-ttu-id="6db6b-131">Įprastai, kai pageidaujamas priežiūros darbuotojas pasirenkamas sudarant darbo užsakymo grafiką, Turto valdyme peržiūrimi visi įrašai **Pageidaujami priežiūros darbuotojai** dėl galimų atitikimų, visada pirmiausiai atsižvelgiama į sudėtingiausią derinį.</span><span class="sxs-lookup"><span data-stu-id="6db6b-131">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="6db6b-132">Jei nerandama atitikimų, naudojami „numatytieji“ įrašai su atrankos kriterijais, nurodytais lauke **Pageidaujama priežiūros darbo grupė** ar lauke **Pageidaujamas priežiūros darbuotojas**.</span><span class="sxs-lookup"><span data-stu-id="6db6b-132">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>


![1 pav.](media/02-work-order-scheduling.png)

<span data-ttu-id="6db6b-134">Taip pat galite nustatyti atsakingus priežiūros darbuotojus, kurie gali būti atrinkti, kai sukuriama priežiūros užklausa arba darbo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="6db6b-134">You can also set up responsible maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="6db6b-135">Jeigu reikia, galite keisti atrankos kriterijus skiltyse **Visi darbo užsakymai** ir **Visos priežiūros užklausos**.</span><span class="sxs-lookup"><span data-stu-id="6db6b-135">In **All work orders** and **All maintenance requests**, you can edit the selection, if required.</span></span> <span data-ttu-id="6db6b-136">Daugiau informacijos žr. [Atsakingi priežiūros darbuotojai](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="6db6b-136">Refer to [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md) for more information.</span></span>

<span data-ttu-id="6db6b-137">Kuriant darbo užsakymo grafiką skaičiuojami įvairūs įverčiai, siekiant nustatyti, kuriam darbuotojui turi būti paskirta atlikti užduotis, susijusias su darbo užsakymu (tokie įverčiai yra nustatomi nuorodoje **Turto valdymo parametrai** > **Darbo užsakymų planavimas**).</span><span class="sxs-lookup"><span data-stu-id="6db6b-137">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="6db6b-138">Jei du ar daugiau pageidaujami priežiūros darbuotojai ar atsakingi priežiūros darbuotojai įvertinami taip pat, planuojant darbo užsakymą, vienas darbuotojas yra pasirenkamas atsitiktine tvarka.</span><span class="sxs-lookup"><span data-stu-id="6db6b-138">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="6db6b-139">Kitaip, darbuotojas, surinkęs didžiausią įvertį, visada bus paskirtas atlikti darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="6db6b-139">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

