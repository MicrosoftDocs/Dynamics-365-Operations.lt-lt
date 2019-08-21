---
title: Būklės vertinimas
description: Šioje temoje paaiškinama, kaip modulyje Turto valdymas sukurti turto būklės vertinimo šabloną ir registraciją.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5294325f67f0484b39194b5bd9784a2e612001a4
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783452"
---
# <a name="condition-assessment"></a><span data-ttu-id="dd238-103">Būklės vertinimas</span><span class="sxs-lookup"><span data-stu-id="dd238-103">Condition assessment</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="dd238-104">Šioje temoje aiškinama, kaip modulyje Turto valdymas sukurti turto būklės vertinimo šabloną ir registraciją.</span><span class="sxs-lookup"><span data-stu-id="dd238-104">This topic explains how to create a condition assessment template and registration on an asset in Asset Management.</span></span> <span data-ttu-id="dd238-105">Būklės vertinimas atliekamas reguliariais intervalais, o pagrindinis tikslas – sukurti ir išlaikyti būklės duomenis apie turtą.</span><span class="sxs-lookup"><span data-stu-id="dd238-105">Condition assessment is performed at regular intervals, and the primary objective is to create and maintain condition data on assets.</span></span> <span data-ttu-id="dd238-106">Žvelgiant iš prevencinės priežiūros perspektyvos, svarbu stebėti svarbiausią informaciją, pvz., dabartinę būklę ir likusį eksploatavimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="dd238-106">Seen from a preventive maintenance perspective, it is important to monitor key information such as current condition, and remaining life span.</span></span> <span data-ttu-id="dd238-107">Be to, jei būklės vertinimą atliksite reguliariais intervalais, galėsite stebėti ir lyginti savo gamyklos mašinų būklę.</span><span class="sxs-lookup"><span data-stu-id="dd238-107">Furthermore, if you carry out condition assessment at regular intervals, you will be able to monitor and compare conditions on the machinery in your factory.</span></span>

<span data-ttu-id="dd238-108">Būklės vertinimas gali būti naudojamas daugumai įrangos būklių matuoti ir stebėti.</span><span class="sxs-lookup"><span data-stu-id="dd238-108">Condition assessment can be used to measure and monitor many conditions on your equipment.</span></span> <span data-ttu-id="dd238-109">Pavyzdys: galite matuoti mašinų vibracijas.</span><span class="sxs-lookup"><span data-stu-id="dd238-109">Example: You could measure vibrations on your machinery.</span></span> <span data-ttu-id="dd238-110">Užregistravę įvairių tipų įrangos vibracijos matavimus modulyje Turto valdymas, galite ieškoti naujausio užregistruoto vertinimo ir peržiūrėti vibracijos matavimus.</span><span class="sxs-lookup"><span data-stu-id="dd238-110">After you have registered vibration measurements in Asset Management on various types of equipment, you can search for the latest registered assessment and view vibration measurements.</span></span>

<span data-ttu-id="dd238-111">Sukuriamas turto būklės vertinimas.</span><span class="sxs-lookup"><span data-stu-id="dd238-111">Condition assessment is created on assets.</span></span> <span data-ttu-id="dd238-112">Prieš atlikdami būklės vertinimo procedūrą turite nustatyti turto tipo būklės vertinimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="dd238-112">You set up a condition assessment template on an asset type before you carry out the condition assessment procedure.</span></span> <span data-ttu-id="dd238-113">Būklės vertinimo šablonų naudojimo priežastis – išvengti būklės duomenų apie panašų turtą kitimo.</span><span class="sxs-lookup"><span data-stu-id="dd238-113">The reason for using templates for condition assessment is to avoid variation of condition data on similar assets.</span></span> <span data-ttu-id="dd238-114">Būklės vertinimo nustatymo ir naudojimo seka modulyje Turto valdymas: pirmiausia nustatykite reikiamus būklės vertinimo šablonus.</span><span class="sxs-lookup"><span data-stu-id="dd238-114">The sequence for setting up and using condition assessment in Asset Management is: First you set up the required condition assessment templates.</span></span> <span data-ttu-id="dd238-115">Tada susiekite šablonus su turto tipais formoje **Turto tipai**.</span><span class="sxs-lookup"><span data-stu-id="dd238-115">Next, you associate templates with asset types in the **Asset types** form.</span></span> <span data-ttu-id="dd238-116">Galiausiai, formoje **Turtas** galite kurti turto būklės vertinimo registracijas.</span><span class="sxs-lookup"><span data-stu-id="dd238-116">Finally, you can create condition assessment registrations on an asset in the **Asset** form.</span></span>

## <a name="create-a-condition-assessment-template"></a><span data-ttu-id="dd238-117">Būklės vertinimo šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="dd238-117">Create a condition assessment template</span></span>

1. <span data-ttu-id="dd238-118">Pasirinkite **Turto valdymas** > **Sąranka** > **Turto tipai** > **Būklės vertinimas**.</span><span class="sxs-lookup"><span data-stu-id="dd238-118">Select **Asset management** > **Setup** > **Asset types** > **Condition assessment**.</span></span>
2. <span data-ttu-id="dd238-119">Pasirinkite **Naujas**, kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="dd238-119">Select **New** to create a new template.</span></span>
3. <span data-ttu-id="dd238-120">Lauke **Šablonas** įveskite ir šablono ID.</span><span class="sxs-lookup"><span data-stu-id="dd238-120">Insert and ID for the template in the **Template** field.</span></span>
4. <span data-ttu-id="dd238-121">Lauke **Pavadinimas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="dd238-121">Insert a name for the template in the **Name** field.</span></span>
5. <span data-ttu-id="dd238-122">„FastTab“ skirtuke **Būklės vertinimo eilutės** pridėkite eilutes, reikalingas būklės vertinimui, įskaitant tinkamo būklės tipo ir matavimo vieneto pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="dd238-122">On the **Condition assessment lines** FastFab, add the lines required for the condition assessment, including selection of the appropriate condition type and measurement unit.</span></span>
6. <span data-ttu-id="dd238-123">„FastTab“ skirtuke **Turto tipai** pridėkite turto tipus, kurie turėtų naudoti būklės vertinimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="dd238-123">On the **Asset types** FastTab, add the asset types that should use the condition assessment template.</span></span>
7. <span data-ttu-id="dd238-124">Grupės **Išsami informacija**, esančios ekrano viršuje, laukuose **Eilutės** ir **Turto tipai** pamatysite vertinimo eilučių ir turto tipų, susijusių su pasirinktu būklės vertinimo šablonu, skaičių.</span><span class="sxs-lookup"><span data-stu-id="dd238-124">In the **Lines** and **Asset types** fields in the **Details** group at the top of the screen, you will see the number of assessment lines and asset types related to the selected condition assessment template.</span></span>


## <a name="create-condition-assessment-registration-on-an-asset"></a><span data-ttu-id="dd238-125">Turto būklės vertinimo registracijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="dd238-125">Create condition assessment registration on an asset</span></span>

1. <span data-ttu-id="dd238-126">Pasirinkite **Turto valdymas** > **Bendra** > **Turtas** > **Visas turtas**.</span><span class="sxs-lookup"><span data-stu-id="dd238-126">Select **Asset management** > **Common** > **Assets** > **All Assets**.</span></span>
2. <span data-ttu-id="dd238-127">Sąraše pasirinkite turtą, kurio būklės vertinimo registraciją norite sukurti.</span><span class="sxs-lookup"><span data-stu-id="dd238-127">In the list, select the asset for which you want to create a condition assessment registration.</span></span>
3. <span data-ttu-id="dd238-128">Skirtuke **Bendra** spustelėkite **Būklės vertinimas**.</span><span class="sxs-lookup"><span data-stu-id="dd238-128">On the **General** tab, click **Condition assessment**.</span></span>
4. <span data-ttu-id="dd238-129">Spustelėję **Nauja** sukurkite naują registraciją.</span><span class="sxs-lookup"><span data-stu-id="dd238-129">Click **New** to make a new registration.</span></span>
5. <span data-ttu-id="dd238-130">Lauke **Data** pasirinkite būklės vertinimo datą.</span><span class="sxs-lookup"><span data-stu-id="dd238-130">Select the date for the condition assessment in the **Date** field.</span></span>
6. <span data-ttu-id="dd238-131">Lauke **Darbuotojas** pasirinkite darbuotojo, kuris atliko vertinimo registraciją, vardą ir pavardę.</span><span class="sxs-lookup"><span data-stu-id="dd238-131">Select the name of the worker who carried out the assessment registration in the **Worker** field.</span></span>
7. <span data-ttu-id="dd238-132">Lauke **Eilutės** pamatysite vertinimo eilučių, nustatytų atliekant būklės vertinimą, skaičių.</span><span class="sxs-lookup"><span data-stu-id="dd238-132">In the **Lines** field, you see the number of assessment lines set up on the condition assessment.</span></span>
8. <span data-ttu-id="dd238-133">Lauke **Šablonas** pasirinkite būklės vertinimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="dd238-133">Select a template for the condition assessment in the **Template** field.</span></span> <span data-ttu-id="dd238-134">Šablono pavadinimas automatiškai įterpiamas į lauką **Pavadinimas**, o susijusios registracijos eilutės – į „FastTab“ skirtuką **Būklės vertinimo eilutės**.</span><span class="sxs-lookup"><span data-stu-id="dd238-134">The name of the template is automatically inserted in the **Name** field, and the related registration lines are inserted on the **Condition assessment lines** FastTab.</span></span>
9. <span data-ttu-id="dd238-135">„FastTab“ skirtuke **Pastabos** galite įterpti pastabų, susijusių su pasirinktu būklės vertinimu.</span><span class="sxs-lookup"><span data-stu-id="dd238-135">You can insert notes relating to the selected condition assessment on the **Notes** FastTab.</span></span>
10. <span data-ttu-id="dd238-136">Lauke **Reikšmė** prie kiekvienos būklės vertinimo eilutės įterpkite matavimo duomenis.</span><span class="sxs-lookup"><span data-stu-id="dd238-136">For each condition assessment line, insert measurement data in the **Value** field.</span></span>
11. <span data-ttu-id="dd238-137">Lauke **Būklės vertinimo eilutės** „FastTab“ > **Komentarai** prie pasirinktos registracijos eilutės galite įterpti komentarą.</span><span class="sxs-lookup"><span data-stu-id="dd238-137">You can insert a comment relating to the selected registration line on the **Condition assessment lines** FastTab > **Comments** field.</span></span> <span data-ttu-id="dd238-138">Jei prie eilutės pridedate komentarą, automatiškai parenkamas žymės langelis **Komentaras**.</span><span class="sxs-lookup"><span data-stu-id="dd238-138">If you add a comment on a line, the **Comment** check box is automatically selected.</span></span>

<span data-ttu-id="dd238-139">Atlikę turto būklės vertinimo registraciją, galite atsispausdinti būklės vertinimo ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="dd238-139">After you have made a condition assessment registration on an asset, you can print a condition assessment report.</span></span>

>[!NOTE]
><span data-ttu-id="dd238-140">Taip pat galite užregistruoti darbo užsakymo būklės vertinimą (mygtukas **Turto valdymas** > **Bendra** > **Darbo užsakymai** > **Visi darbo užsakymai** > **Būklės vertinimas**).</span><span class="sxs-lookup"><span data-stu-id="dd238-140">You can also register condition assessment on a work order (**Asset management** > **Common** > **Work orders** > **All Work orders** > **Condition assessment** button.)</span></span>
