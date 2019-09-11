---
title: Suvartojimo registravimas
description: Šioje temoje aiškinama, kaip registruoti suvartojimą modulyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
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
ms.openlocfilehash: 7f785b0935b952d6de68fd120a3639077ad124bd
ms.sourcegitcommit: c0b581e4c647b6c47bc14d1d7bfe267832afecba
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/21/2019
ms.locfileid: "1913099"
---
# <a name="register-consumption"></a><span data-ttu-id="91c8e-103">Suvartojimo registravimas</span><span class="sxs-lookup"><span data-stu-id="91c8e-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="91c8e-104">Kai pagal darbo užsakymą atliekama priežiūros užduotis, kitas veiksmas – registruoti suvartojimą ir skelbti žurnalus.</span><span class="sxs-lookup"><span data-stu-id="91c8e-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="91c8e-105">Galite registruoti šiuos suvartojimo tipus: valandas, prekes ir išlaidas.</span><span class="sxs-lookup"><span data-stu-id="91c8e-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="91c8e-106">Skirtingi suvartojimo tipai registruojami ir skelbiami puslapyje **Darbo užsakymo žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="91c8e-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="91c8e-107">Modulio **Turto valdymas** žurnalo sąranka naudojama atskiriems valandų, prekių ir išlaidų žurnalams kurti ir skelbti modulyje **Projekto valdymas ir apskaita**.</span><span class="sxs-lookup"><span data-stu-id="91c8e-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="91c8e-108">Galbūt turėsite galimybę įtraukti arba pašalinti darbo užsakymo prognozės eilutes.</span><span class="sxs-lookup"><span data-stu-id="91c8e-108">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="91c8e-109">Darbo užsakymo ciklo būsenos sąranka, susijęs projekto tipas ir su projekto tipu susijusios etapo taisyklės nulemia tai, ar galite įtraukti arba redaguoti žurnalo eilutes.</span><span class="sxs-lookup"><span data-stu-id="91c8e-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="91c8e-110">Norėdami gauti daugiau informacijos apie darbo užsakymų ciklo būsenas ir susijusius projektų etapus žr. [Integravimas su projektų valdymu ir apskaita](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="91c8e-110">Read more about work order lifecycle states and related project stages in [Integration to project management and accounting](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="91c8e-111">Galima nustatyti, kad žurnalai būtų automatiškai skelbiami darbo užsakymo ciklo būsenoje.</span><span class="sxs-lookup"><span data-stu-id="91c8e-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="91c8e-112">Daugiau informacijos rasite [Darbo užsakymų ciklo būsenos](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="91c8e-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="91c8e-113">Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="91c8e-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="91c8e-114">Pasirinkite darbo užsakymą ir spustelėkite **Žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="91c8e-114">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="91c8e-115">Spustelėkite **Kopijuoti iš prognozės**, kad būtų perkeltos bet kokios prognozės eilutės, kurios gali būti sujungtos su darbo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="91c8e-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="91c8e-116">Galite pasirinkti, kuriuos suvartojimo tipus norite perkelti.</span><span class="sxs-lookup"><span data-stu-id="91c8e-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="91c8e-117">Jei reikia, atitinkamame „FastTab“ galite įtraukti daugiau suvartojimo eilučių spustelėję **Įtraukti eilutę** ir eilutėje įvedę duomenis.</span><span class="sxs-lookup"><span data-stu-id="91c8e-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="91c8e-118">Norėdami patikrinti žurnalo eilutes prieš paskelbiant, spustelėkite **Tikrinti žurnalus**.</span><span class="sxs-lookup"><span data-stu-id="91c8e-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="91c8e-119">Spustelėkite **Skelbti žurnalus**, kad skelbtumėte žurnalo eilutes.</span><span class="sxs-lookup"><span data-stu-id="91c8e-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="91c8e-120">Paskelbus suvartojimo žurnalus galite atnaujinti darbo užsakymo ciklo būseną, pavyzdžiui – „Pasibaigė“, kad būtų nurodyta, jog darbo užsakymas yra įvykdytas.</span><span class="sxs-lookup"><span data-stu-id="91c8e-120">After you've posted the consumption journals, you can update the work order lifecycle state, for example to "Ended", to indicate that the work order has been completed.</span></span>

- <span data-ttu-id="91c8e-121">Puslapio **Darbo užsakymo žurnalai** viršuje pateiktame lauke **Rodyti** pasirinkite, kurias žurnalo eilutes norite matyti: visas, nepaskelbtas ar paskelbtas.</span><span class="sxs-lookup"><span data-stu-id="91c8e-121">In the **Show** field placed at the top of the **Work order journals** page, select which journal lines you want to see: All, Not posted, or Posted.</span></span> <span data-ttu-id="91c8e-122">Jei žurnalas paskelbtas, žymės langelyje **Paskelbta** yra varnelė.</span><span class="sxs-lookup"><span data-stu-id="91c8e-122">Posted journals have a check mark in the **Posted** check box.</span></span>  
- <span data-ttu-id="91c8e-123">Kai darbo užsakymo žurnale sukuriamos prekės eilutės, su preke susijusios produkto dimensijos ir sekimo dimensijos automatiškai perkeliamos į žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="91c8e-123">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="91c8e-124">Toliau pateiktoje ekrano kopijoje matomas darbo užsakymo valandų ir prekių registracijų **darbo užsakymo žurnaluose** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="91c8e-124">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![1 pav.](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="91c8e-126">Darbo užsakymų su keliomis darbo užsakymo užduotimis valandų padalijimas</span><span class="sxs-lookup"><span data-stu-id="91c8e-126">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="91c8e-127">Jei darbo užsakyme yra kelios darbo užsakymo užduotys, darbo valandas galite registruoti naudodami funkciją **Padalyti valandas**, t. y., viena valandos registracijos eilutė gali būti vienodai padalyta kiekvienai darbo užsakymo užduočiai.</span><span class="sxs-lookup"><span data-stu-id="91c8e-127">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="91c8e-128">Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="91c8e-128">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="91c8e-129">Pasirinkite darbo užsakymą ir spustelėkite **Žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="91c8e-129">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="91c8e-130">Pasirinkite valandų registracijos eilutę, kurią norite padalyti, ir spustelėkite **Padalyti valandas**.</span><span class="sxs-lookup"><span data-stu-id="91c8e-130">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="91c8e-131">Dialogo lango **Padalyti valandas darbo užsakymo priežiūros užduotims** lauke **Darbuotojas** automatiškai rodomas prisijungusio darbuotojo vardas.</span><span class="sxs-lookup"><span data-stu-id="91c8e-131">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="91c8e-132">Jei reikia, galite pasirinkti kitą darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="91c8e-132">If required, you can select another worker.</span></span>

5. <span data-ttu-id="91c8e-133">Lauke **Kategorija** pasirinkite valandų registravimo kategoriją.</span><span class="sxs-lookup"><span data-stu-id="91c8e-133">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="91c8e-134">Lauke **Valandos** įrašykite darbo valandų, kurias norite padalyti, skaičių.</span><span class="sxs-lookup"><span data-stu-id="91c8e-134">Insert number of work hours to be split in the **Hours** field.</span></span>

![2 paveikslėlis](media/02-consumption.png)

7. <span data-ttu-id="91c8e-136">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="91c8e-136">Click **OK**.</span></span>

<span data-ttu-id="91c8e-137">*Pavyzdys:* Toliau pateiktoje ekrano kopijoje matomos darbo užsakymo, kuriame yra trys darbo užsakymo užduotys, žurnalo eilutės.</span><span class="sxs-lookup"><span data-stu-id="91c8e-137">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="91c8e-138">Pirmoji eilutė, kurioje yra trys valandos, buvo padalyta, ir kiekvienoje darbo užsakymo užduotyje užregistruojama viena darbo valanda.</span><span class="sxs-lookup"><span data-stu-id="91c8e-138">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="91c8e-139">Sukūrus tris valandų registracijos eilutes galite nuspręsti, ką daryti su pradine valandų registracijos eilute (pirmoji eilutė pavyzdyje).</span><span class="sxs-lookup"><span data-stu-id="91c8e-139">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="91c8e-140">Galite ją palikti arba ištrinti.</span><span class="sxs-lookup"><span data-stu-id="91c8e-140">You can keep it as is or delete it.</span></span> 

![3 paveikslėlis](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="91c8e-142">Suvartojimo registracijų finansinės dimensijos</span><span class="sxs-lookup"><span data-stu-id="91c8e-142">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="91c8e-143">Registruojant suvartojimą į registracijas konkrečia seka įtraukiamos finansinės dimensijos, susijusios su skirtingais registravimo tipais.</span><span class="sxs-lookup"><span data-stu-id="91c8e-143">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

<span data-ttu-id="91c8e-144">*Valandų ir išlaidų registracijos:* jei yra, pirmiausia įtraukiamos žurnalo antraštės finansinės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="91c8e-144">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="91c8e-145">Tada įtraukiamos susijusio darbo užsakymo projekto finansinės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="91c8e-145">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="91c8e-146">Galiausiai įtraukiamos išteklių (darbuotojo) finansinės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="91c8e-146">Finally, financial dimensions from the resource (worker) are added.</span></span>

<span data-ttu-id="91c8e-147">*Prekių registracijos:* jei yra, pirmiausia įtraukiamos žurnalo antraštės finansinės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="91c8e-147">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="91c8e-148">Tada įtraukiamos susijusio darbo užsakymo projekto finansinės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="91c8e-148">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="91c8e-149">Tada įtraukiamos vietos finansinės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="91c8e-149">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="91c8e-150">Galiausiai įtraukiamos prekės finansinės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="91c8e-150">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="91c8e-151">Visuose trijuose registracijų tipuose patikrinamas finansinių dimensijų derinys, o netinkami deriniai uždengiami.</span><span class="sxs-lookup"><span data-stu-id="91c8e-151">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="91c8e-152">Tai – „Dynamics 365 for Finance and Operations“ standartinė sąranka.</span><span class="sxs-lookup"><span data-stu-id="91c8e-152">This is standard setup in Dynamics 365 for Finance and Operations.</span></span>

