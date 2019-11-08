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
ms.openlocfilehash: 3501cb49cbc8b3060da03b3d2e9badc949910a48
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652200"
---
# <a name="set-up-preferred-maintenance-workers"></a><span data-ttu-id="c22eb-103">Nustatyti pageidaujamus priežiūros darbuotojus</span><span class="sxs-lookup"><span data-stu-id="c22eb-103">Set up preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c22eb-104">Planuodami darbo užsakymus galite nustatyti priežiūros darbuotojų ar darbuotojų grupių pasirinkimo atlikti darbo užsakymą pirmumą.</span><span class="sxs-lookup"><span data-stu-id="c22eb-104">During work order scheduling, you can make a preference regarding which maintenance worker or worker group is allocated to complete the work order.</span></span> <span data-ttu-id="c22eb-105">Ši funkcija yra nebūtina, tačiau ji gali būti naudinga sprendžiant dėl labiausiai kvalifikuoto priežiūros darbuotojo užduočiai atlikti, atsižvelgiant į darbuotojo įgūdžius ir kompetencijas.</span><span class="sxs-lookup"><span data-stu-id="c22eb-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="c22eb-106">Tik tie priežiūros darbuotojai, kurie yra pasiekiami planuojamo užsakymo metu, pateks į grafiką.</span><span class="sxs-lookup"><span data-stu-id="c22eb-106">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="c22eb-107">Jei planuojant užsakymą pageidaujamo priežiūros darbuotojo sąranka atitiks darbo užsakymą, bet priežiūros darbuotojas paskirtas atlikti kitus darbus, darbo užsakymas bus paskirtas kitam pasiekiamam priežiūros darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="c22eb-107">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another available maintenance worker.</span></span>

<span data-ttu-id="c22eb-108">Kad galėtumėte nustatyti pageidaujamus priežiūros darbuotojus, pirmiausia turite nustatyti priežiūros darbuotojus ir darbuotojų grupes.</span><span class="sxs-lookup"><span data-stu-id="c22eb-108">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups.</span></span> <span data-ttu-id="c22eb-109">Norėdami sužinoti, kaip nustatyti priežiūros darbuotojus ir darbo grupes, žr. [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="c22eb-109">For a description about how to set up maintenance workers and worker groups, see to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="c22eb-110">Pageidaujamų priežiūros darbuotojų sąranka</span><span class="sxs-lookup"><span data-stu-id="c22eb-110">Set up preferred workers</span></span>

<span data-ttu-id="c22eb-111">Pageidaujamas priežiūros darbuotojas ar darbuotojų grupė gali būti susijusi konkrečiai su vienu ar daugiau toliau nurodytu aspektu.</span><span class="sxs-lookup"><span data-stu-id="c22eb-111">A preferred maintenance worker or worker group can be related to one or more of the following:</span></span>

- <span data-ttu-id="c22eb-112">prekyba</span><span class="sxs-lookup"><span data-stu-id="c22eb-112">trade</span></span>  
- <span data-ttu-id="c22eb-113">priežiūros užduoties tipo variantu</span><span class="sxs-lookup"><span data-stu-id="c22eb-113">maintenance job type variant</span></span>  
- <span data-ttu-id="c22eb-114">priežiūros užduoties tipu</span><span class="sxs-lookup"><span data-stu-id="c22eb-114">maintenance job type</span></span>  
- <span data-ttu-id="c22eb-115">priežiūros užduoties tipo kategorija</span><span class="sxs-lookup"><span data-stu-id="c22eb-115">maintenance job type category</span></span>  
- <span data-ttu-id="c22eb-116">turtas</span><span class="sxs-lookup"><span data-stu-id="c22eb-116">asset</span></span>  
- <span data-ttu-id="c22eb-117">turto tipu</span><span class="sxs-lookup"><span data-stu-id="c22eb-117">asset type</span></span>  

<span data-ttu-id="c22eb-118">Kuo daugiau atrankos kriterijų sukursite tam pačiam įrašui, tuo konkretesnė bus sąranka.</span><span class="sxs-lookup"><span data-stu-id="c22eb-118">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="c22eb-119">Spustelėkite **Turto valdymas** > **Sąranka** > **Darbuotojai** > **Pageidaujami priežiūros darbuotojai**.</span><span class="sxs-lookup"><span data-stu-id="c22eb-119">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="c22eb-120">Spustelėję **Naujas** sukurkite naują įrašą.</span><span class="sxs-lookup"><span data-stu-id="c22eb-120">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="c22eb-121">Pirmiausia sukurkite „numatytąjį” priežiūros darbuotoją ar darbuotojų grupę.</span><span class="sxs-lookup"><span data-stu-id="c22eb-121">Start by creating a "default" maintenance worker or worker group.</span></span> <span data-ttu-id="c22eb-122">Tokiu būdu jūs atrinksite tik naudodamiesi lauku **Pageidaujama priežiūros darbo grupė** arba lauku **Pageidaujamas priežiūros darbuotojas**.</span><span class="sxs-lookup"><span data-stu-id="c22eb-122">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="c22eb-123">Toliau ekrano kopijoje galite matyti pavyzdį pirmajame įraše, kuriame „Užklausos“ pasirinktos kaip **Pageidaujama priežiūros darbuotojų grupė**.</span><span class="sxs-lookup"><span data-stu-id="c22eb-123">In the screenshot below, you see an example in the first record in which "Requests" is selected as **Preferred maintenance worker group**.</span></span>

    [!NOTE] <span data-ttu-id="c22eb-124">Numatytoji konfigūracija bus naudojama darbo užsakymų planavimo metu, jei nebus rasta jokia kita, konkrečiau darbo užsakymo turinį atitinkanti kombinacija.</span><span class="sxs-lookup"><span data-stu-id="c22eb-124">The default setup will be used during work order scheduling if no other, more specific, combination matches the contents of the work order.</span></span>

4. <span data-ttu-id="c22eb-125">Kartokite 2 žingsnį, kad sukurtumėte naują įrašą.</span><span class="sxs-lookup"><span data-stu-id="c22eb-125">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="c22eb-126">Nustatykite reikiamus atrankos kriterijus priklausomai nuo išsamumo lygio pageidaujamam darbuotojui ar darbo grupei.</span><span class="sxs-lookup"><span data-stu-id="c22eb-126">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> 

    <span data-ttu-id="c22eb-127">*Pavyzdys:* toliau ekrano kopijoje, šeštame įraše, priežiūros darbuotojas Šonas Ričardsonas pasirenkamas kaip pageidaujamas darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="c22eb-127">*Example:* In the screenshot below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="c22eb-128">Jis bus automatiškai atrinktas planuojant darbo užsakymą, kuriame pateikiamas turtas CH-BP1-03-02, o priežiūros užduoties tipas – „Patalpų įvertinimas“, jei jis bus pasiekiamas grafike nustatytu laiku.</span><span class="sxs-lookup"><span data-stu-id="c22eb-128">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintenance job type "Facility assessment", if he is available at the scheduled time.</span></span>

    [!NOTE] <span data-ttu-id="c22eb-129">Įprastai, kai pageidaujamas priežiūros darbuotojas pasirenkamas sudarant darbo užsakymo grafiką, Turto valdyme peržiūrimi visi įrašai **Pageidaujami priežiūros darbuotojai** dėl galimų atitikimų, visada pirmiausiai atsižvelgiama į sudėtingiausią derinį.</span><span class="sxs-lookup"><span data-stu-id="c22eb-129">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="c22eb-130">Jei nerandama atitikimų, naudojami „numatytieji“ įrašai su atrankos kriterijais, nurodytais lauke **Pageidaujama priežiūros darbo grupė** ar lauke **Pageidaujamas priežiūros darbuotojas**.</span><span class="sxs-lookup"><span data-stu-id="c22eb-130">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>

![1 pav.](media/02-work-order-scheduling.png)

<span data-ttu-id="c22eb-132">Taip pat galite nustatyti *atsakingus* priežiūros darbuotojus, kurie gali būti atrinkti, kai sukuriama priežiūros užklausa arba darbo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="c22eb-132">You can also set up *responsible* maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="c22eb-133">Jeigu reikia, galite keisti atrankos kriterijus skiltyse **Visi darbo užsakymai** ir **Visos priežiūros užklausos**.</span><span class="sxs-lookup"><span data-stu-id="c22eb-133">You can edit the selection in **All work orders** and **All maintenance requests**, if required.</span></span> <span data-ttu-id="c22eb-134">Daugiau informacijos žr. [Atsakingi priežiūros darbuotojai](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="c22eb-134">For more information, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

<span data-ttu-id="c22eb-135">Kuriant darbo užsakymo grafiką skaičiuojami įvairūs įverčiai, siekiant nustatyti, kuriam darbuotojui turi būti paskirta atlikti užduotis, susijusias su darbo užsakymu (tokie įverčiai yra nustatomi nuorodoje **Turto valdymo parametrai** > **Darbo užsakymų planavimas**).</span><span class="sxs-lookup"><span data-stu-id="c22eb-135">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="c22eb-136">Jei du ar daugiau pageidaujami priežiūros darbuotojai ar atsakingi priežiūros darbuotojai įvertinami taip pat, planuojant darbo užsakymą, vienas darbuotojas yra pasirenkamas atsitiktine tvarka.</span><span class="sxs-lookup"><span data-stu-id="c22eb-136">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="c22eb-137">Kitaip, darbuotojas, surinkęs didžiausią įvertį, visada bus paskirtas atlikti darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="c22eb-137">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

