---
title: Esamos veiklos įtraukimas į gamybos eigos versiją
description: Kurdami naujas gamybos eigų versijas, į naują versiją galite įtraukti senesnių versijų sukurtas veiklas.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 032855125ccd14fbdc1e1bdb735c92ce70853fb0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568389"
---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a><span data-ttu-id="07a84-103">Esamos veiklos įtraukimas į gamybos eigos versiją</span><span class="sxs-lookup"><span data-stu-id="07a84-103">Add an existing activity to a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="07a84-104">Kurdami naujas gamybos eigų versijas, į naują versiją galite įtraukti senesnių versijų sukurtas veiklas.</span><span class="sxs-lookup"><span data-stu-id="07a84-104">When creating new versions of production flows, you can choose to add activities created for the older versions, to the new version.</span></span> <span data-ttu-id="07a84-105">Šioje procedūroje parodoma, kaip kurti naują esamos gamybos eigos versiją nekopijuojant veiklų.</span><span class="sxs-lookup"><span data-stu-id="07a84-105">This procedure shows how a new version is created for an existing production flow, without copying the activities.</span></span> <span data-ttu-id="07a84-106">Atliekant kitą veiksmą, esama veikla yra įtraukiama į naują versiją.</span><span class="sxs-lookup"><span data-stu-id="07a84-106">In the next step, an existing activity is added to the new version.</span></span> 

<span data-ttu-id="07a84-107">Jei norite atlikti šią užduotį, turite sukurti gamybos eigos versiją ir veiklas.</span><span class="sxs-lookup"><span data-stu-id="07a84-107">This task requires production flow with version and activities already created.</span></span>


## <a name="create-a-new-production-flow-version"></a><span data-ttu-id="07a84-108">Kurti naują gamybos eigos versiją</span><span class="sxs-lookup"><span data-stu-id="07a84-108">Create a new production flow version</span></span>
1. <span data-ttu-id="07a84-109">Pasirinkite Gamybos kontrolė > Nustatymai > „Lean“ gamybos eiga > Gamybos eigos.</span><span class="sxs-lookup"><span data-stu-id="07a84-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="07a84-110">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="07a84-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="07a84-111">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="07a84-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="07a84-112">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="07a84-112">Click Edit.</span></span>
5. <span data-ttu-id="07a84-113">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="07a84-113">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="07a84-114">Lauke Galiojimo data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="07a84-114">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="07a84-115">Atkreipkite dėmesį, kad prieš kurdami naują gamybos eigos versiją, turite patikrinti aktyvios versijos galiojimo pabaigos datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="07a84-115">Note that before you create a new production flow version, make sure to check the expiration date and time of the active version.</span></span> <span data-ttu-id="07a84-116">Nauja versija bus sukurta su įsigaliojimo pradžios data, kuri sutampa su pasirinktos versijos galiojimo pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="07a84-116">The new version will be created with an effective start date, which connects to the expiry date of the selected version.</span></span>  
7. <span data-ttu-id="07a84-117">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="07a84-117">Click Add.</span></span>
8. <span data-ttu-id="07a84-118">Lauke Kopijuoti iš versijos pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="07a84-118">Select No in the Copy from version field.</span></span>
    * <span data-ttu-id="07a84-119">Pasirinkite Ne, kai norite pradėti naudodami tuščią versiją, t. y., jei dauguma nukopijuotos versijos veiklos turi būti pakeistos naujomis veiklomis..</span><span class="sxs-lookup"><span data-stu-id="07a84-119">Select No to start with an empty version if most of the activities of the copied version will be replaced by new activities.</span></span> <span data-ttu-id="07a84-120">Neautomatiniu būdu įtraukite nepakitusias veiklas į veiklos formos funkciją Įtraukti esamą.</span><span class="sxs-lookup"><span data-stu-id="07a84-120">Add the unchanged activities to the Add existing function in the activity form manually.</span></span>  
9. <span data-ttu-id="07a84-121">Lauke Dubliuoti „kanban“ taisykles pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="07a84-121">Select No in the Duplicate kanban rules field.</span></span>
    * <span data-ttu-id="07a84-122">Kai veiklos į naują versiją nekopijuojamos, naujos versijos kūrimo metu neįmanoma kopijuoti „kanban“ taisyklių.</span><span class="sxs-lookup"><span data-stu-id="07a84-122">When the activities are not copied to the new version, it is not possible to copy the kanban rules at the time of creation of the new version.</span></span>   <span data-ttu-id="07a84-123">Todėl vėliau reikia naudoti pakeitimo „kanban“ kūrimo funkciją „kanban“ taisyklės formoje, kad senos gamybos eigos versijos „kanban“ taisyklės būtų pakeistos naujos versijos veiklų „kanban“ taisyklėmis.</span><span class="sxs-lookup"><span data-stu-id="07a84-123">Instead you will use the create replacement kanban function later in the kanban rule form, to replace kanban rules of the old production flow version with kanban rules using the activities of the new version.</span></span>  
10. <span data-ttu-id="07a84-124">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="07a84-124">Click OK.</span></span>
11. <span data-ttu-id="07a84-125">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="07a84-125">In the list, find and select the desired record.</span></span>

## <a name="add-an-existing-activity"></a><span data-ttu-id="07a84-126">Esamos veiklos įtraukimas</span><span class="sxs-lookup"><span data-stu-id="07a84-126">Add an existing activity</span></span>
1. <span data-ttu-id="07a84-127">Spustelėkite Veiklos.</span><span class="sxs-lookup"><span data-stu-id="07a84-127">Click Activities.</span></span>
2. <span data-ttu-id="07a84-128">Spustelėdami Įtraukti esamą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="07a84-128">Click Add existing to open the drop dialog.</span></span>
    * <span data-ttu-id="07a84-129">Raskite ir pasirinkite esamą veiklą, kurią norite įtraukti į naują gamybos eigos versiją.</span><span class="sxs-lookup"><span data-stu-id="07a84-129">Find and select an existing activity to be added to the new production flow version.</span></span>  <span data-ttu-id="07a84-130">Atkreipkite dėmesį, kad sąraše rodomos šios gamybos eigos visų ankstesnių versijų sukurtos veiklos.</span><span class="sxs-lookup"><span data-stu-id="07a84-130">Note that the list shows all activities that have been created for this production flow for all previous versions of the flow.</span></span>  
3. <span data-ttu-id="07a84-131">Lauke Veikla įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="07a84-131">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="07a84-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="07a84-132">Click OK.</span></span>

