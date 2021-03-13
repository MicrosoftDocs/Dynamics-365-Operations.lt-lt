---
title: Gyvenimo įvykių apdorojimas
description: Programoje „Microsoft Dynamics 365 Human Resources“ darbuotojo ciklo metu kiekvienas darbuotojas gali susidurti su įvairiais gyvenimo įvykių pokyčiais.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42b7e2606bca4bb5eda1c9bfc7940f9067c4b943
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113521"
---
# <a name="process-life-events"></a><span data-ttu-id="8db48-103">Gyvenimo įvykių apdorojimas</span><span class="sxs-lookup"><span data-stu-id="8db48-103">Process life events</span></span>

<span data-ttu-id="8db48-104">Programoje „Microsoft Dynamics 365 Human Resources“ darbuotojo ciklo metu kiekvienas darbuotojas gali susidurti su įvairiais gyvenimo įvykių pokyčiais.</span><span class="sxs-lookup"><span data-stu-id="8db48-104">During the employee lifecycle in Microsoft Dynamics 365 Human Resources, each employee may encounter various life event changes.</span></span> <span data-ttu-id="8db48-105">Pavyzdžiui, santuoka, užimtumo pokytis arba priklausomojo / gavėjo pokytis.</span><span class="sxs-lookup"><span data-stu-id="8db48-105">For example, marriage, change in employment, or dependent/beneficiary change.</span></span> <span data-ttu-id="8db48-106">Norėdami naudoti gyvenimo įvykius, turite gyvenimo įvykius įgalinti išmokų parametrų formoje, nustatyti gyvenimo įvykių tipus ir nustatyti planų tipų gyvenimo įvykių parinktis.</span><span class="sxs-lookup"><span data-stu-id="8db48-106">To use life events, you must enable life events in the benefits parameters form, set up life event types, and set up life event options for plan types.</span></span>

<span data-ttu-id="8db48-107">Kad galėtumėte apdoroti gyvenimo įvykius, turite bent kartą jau būti paleidę atvirą registraciją per samdos laiko intervalą.</span><span class="sxs-lookup"><span data-stu-id="8db48-107">Before you can process life events, you must have already run open enrollment at least once during a hiring time frame.</span></span> <span data-ttu-id="8db48-108">Jungtinėse Valstijose atvira registracija paprastai vyksta kartą per metus.</span><span class="sxs-lookup"><span data-stu-id="8db48-108">In the United States, open enrollment is typically once per year.</span></span> <span data-ttu-id="8db48-109">Už Jungtinių Valstijų ribų atvira registracija gali būti vykdoma samdos metu.</span><span class="sxs-lookup"><span data-stu-id="8db48-109">Outside the United States, open enrollment may be run at the time of hire.</span></span> <span data-ttu-id="8db48-110">Darbininkui nereikia pasirinkti išmokos plano, kad būtų galima apdoroti gyvenimo įvykius, tačiau jie turi būti įtraukti į atviros registracijos apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="8db48-110">A worker does not need to select a benefit plan in order for life events to be processed, but they need to have been included in open enrollment processing.</span></span> 

<span data-ttu-id="8db48-111">Naudokite gyvenimo įvykių apdorojimą, kai yra darbininkų, kurių gyvenimo įvykiai įvyks ateityje.</span><span class="sxs-lookup"><span data-stu-id="8db48-111">Use life event processing when you have workers who have life events that take place on a future date.</span></span> <span data-ttu-id="8db48-112">Šiuo įvykiu apdorojami visi neapdoroti gyvenimo įvykiai (pvz., būsimi gyvenimo įvykiai arba įtraukti gyvenimo įvykiai, kurie nėra būdingi konkretiems darbininkams – vienas pavyzdžių yra nauja išmoka).</span><span class="sxs-lookup"><span data-stu-id="8db48-112">This event will process all life events that have not been processed (like future life events, or life events that have been added that are not specific to any one worker – one example is a new benefit).</span></span> <span data-ttu-id="8db48-113">Realiojo laiko gyvenimo įvykiai yra paslėpti.</span><span class="sxs-lookup"><span data-stu-id="8db48-113">Real-time life events are hidden.</span></span>

<span data-ttu-id="8db48-114">Pavyzdžiui, jei šiandien vasario 1 d., o vasario 14 d. planuojama, kad darbininkas Joe Smith pakeis juridinius subjektus, jei vykdote gyvenimo įvykių apdorojimą vasario 15 d., sistema apdoroja visus įvykius iki vasario 15 d.</span><span class="sxs-lookup"><span data-stu-id="8db48-114">For example, if today is February 1, and on February 14 worker Joe Smith is scheduled to change legal entities, if you run life event processing for February 15, the system processes all events up until February 15.</span></span> 

1. <span data-ttu-id="8db48-115">Darbo srities **Išmokų valdymas** dalyje **Apdorojimas** pasirinkite **Gyvenimo įvykių apdorojimas**.</span><span class="sxs-lookup"><span data-stu-id="8db48-115">In the **Benefits management** workspace, under **Processing**, select **Life event processing**.</span></span>

2. <span data-ttu-id="8db48-116">Dialogo lange **Vykdyti gyvenimo įvykių apdorojimą** nurodykite šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="8db48-116">In the **Run life event process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="8db48-117">Laukas</span><span class="sxs-lookup"><span data-stu-id="8db48-117">Field</span></span> | <span data-ttu-id="8db48-118">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="8db48-118">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="8db48-119">**Registracijos laikotarpis**</span><span class="sxs-lookup"><span data-stu-id="8db48-119">**Enrollment period**</span></span> | <span data-ttu-id="8db48-120">Gyvenimo įvykių apdorojimo registracijos laikotarpis.</span><span class="sxs-lookup"><span data-stu-id="8db48-120">The enrollment period to process life events for.</span></span> |
   | <span data-ttu-id="8db48-121">**Juridinis subjektas**</span><span class="sxs-lookup"><span data-stu-id="8db48-121">**Legal entity**</span></span> | <span data-ttu-id="8db48-122">Gyvenimo įvykių apdorojimo juridinis subjektas.</span><span class="sxs-lookup"><span data-stu-id="8db48-122">The legal entity to process life events for.</span></span> |
   | <span data-ttu-id="8db48-123">**Gyvenimo įvykio data**</span><span class="sxs-lookup"><span data-stu-id="8db48-123">**Life event date**</span></span> | <span data-ttu-id="8db48-124">Sistema apdoroja visus įvykius registravimo laikotarpiu, kurie įvyksta iki šios datos.</span><span class="sxs-lookup"><span data-stu-id="8db48-124">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="8db48-125">**Darbininkas**</span><span class="sxs-lookup"><span data-stu-id="8db48-125">**Worker**</span></span> | <span data-ttu-id="8db48-126">Gyvenimo įvykių apdorojimo darbininkas.</span><span class="sxs-lookup"><span data-stu-id="8db48-126">The worker to process life events for.</span></span> <span data-ttu-id="8db48-127">Jei paliksite šį lauką tuščią, visųdarbininkų gyvenimo įvykiai bus apdorojami.</span><span class="sxs-lookup"><span data-stu-id="8db48-127">If you leave this field blank, life events will be processed for all workers.</span></span> |

3. <span data-ttu-id="8db48-128">Jei norite vykdyti procesą fone, pasirinkite **Vykdyti fone** ir atlikite šias užduotis:</span><span class="sxs-lookup"><span data-stu-id="8db48-128">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="8db48-129">Įveskite proceso informaciją.</span><span class="sxs-lookup"><span data-stu-id="8db48-129">Enter information for the process.</span></span>

   2. <span data-ttu-id="8db48-130">Norėdami nustatyti pasikartojančią užduotį, pasirinkite **Pasikartojimas**, įveskite pasikartojimo informaciją ir pažymėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="8db48-130">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="8db48-131">Norėdami nustatyti užduoties įspėjimą, pasirinkite **Įspėjimai**, pasirinkite gautinus įspėjimus, tada pažymėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="8db48-131">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="8db48-132">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="8db48-132">Select **OK**.</span></span> <span data-ttu-id="8db48-133">Procesas bus vykdomas naudojant jūsų nustatytus parametrus.</span><span class="sxs-lookup"><span data-stu-id="8db48-133">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="8db48-134">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="8db48-134">Select **OK**.</span></span>
