---
title: "Tiekėjo darbo eiga"
description: "Keiskite tiekėjo informaciją ir naudokite darbo eigą, kad ją patvirtintumėte."
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Vendor
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: 950a1852acf9f3e4747ce2d55738c0eb3a646897
ms.contentlocale: lt-lt
ms.lasthandoff: 08/31/2018

---

# <a name="vendor-workflow"></a><span data-ttu-id="38f1f-103">Tiekėjo darbo eiga</span><span class="sxs-lookup"><span data-stu-id="38f1f-103">Vendor workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38f1f-104">Kai naudojama tiekėjo darbo eiga, konkrečių laukų pakeitimai siunčiami į darbo eigą patvirtinti prieš įtraukiant juos į tiekėją.</span><span class="sxs-lookup"><span data-stu-id="38f1f-104">When the vendor workflow is used, changes that are made to specific fields are sent to the workflow for approval before they are added to the vendor.</span></span>

## <a name="set-up-the-vendor-workflow"></a><span data-ttu-id="38f1f-105">Tiekėjo darbo eigos nustatymas</span><span class="sxs-lookup"><span data-stu-id="38f1f-105">Set up the vendor workflow</span></span>

<span data-ttu-id="38f1f-106">Norėdami naudoti darbo eigos funkciją, turite ją įjungti.</span><span class="sxs-lookup"><span data-stu-id="38f1f-106">Before you can use the workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="38f1f-107">Pasirinkite **Mokėtinos sumos \> Sąranka \> Mokėtinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="38f1f-107">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="38f1f-108">Skirtuko **General** „FastTab“ **Tiekėjo patvirtinimas** nustatykite parinktį **Įjungti tiekėjo patvirtinimą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="38f1f-108">On the **General** tab, on the **Vendor approval** FastTab, set the **Enable vendor approvals** option to **Yes**.</span></span>
3. <span data-ttu-id="38f1f-109">Lauke **Duomenų objekto veikimo būdas** pasirinkite veikimo būdą, kuris turi būti naudojamas importuojant duomenis.</span><span class="sxs-lookup"><span data-stu-id="38f1f-109">In the **Data entity behavior** field, select the behavior that should be used when data is imported:</span></span>

    - <span data-ttu-id="38f1f-110">**Leisti keisti be patvirtinimo** – duomenų objektas gali atnaujinti tiekėjo įrašą neapdorodamas jo darbo eigoje.</span><span class="sxs-lookup"><span data-stu-id="38f1f-110">**Allow changes without approval** – The data entity can update the vendor record without processing it through the workflow.</span></span>
    - <span data-ttu-id="38f1f-111">**Atmesti pakeitimus** – tiekėjo įrašo keisti negalima.</span><span class="sxs-lookup"><span data-stu-id="38f1f-111">**Reject changes** – Changes can't be made to the vendor record.</span></span> <span data-ttu-id="38f1f-112">Nepavyks importuoti laukų, kurių darbo eiga įjungta.</span><span class="sxs-lookup"><span data-stu-id="38f1f-112">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="38f1f-113">**Kurti pakeitimų pasiūlymus** – bus pakeisti visi laukai, išskyrus laukus, kurių darbo eiga įjungta.</span><span class="sxs-lookup"><span data-stu-id="38f1f-113">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="38f1f-114">Naujos tų laukų reikšmės bus įtrauktos į tiekėją kaip siūlomi pakeitimai, o darbo eiga bus paleista automatiškai.</span><span class="sxs-lookup"><span data-stu-id="38f1f-114">The new values for those fields will be added to the vendor as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="38f1f-115">Tiekėjo laukų sąraše pasirinkite žymės langelį **Įjungti**, pateiktą prie kiekvieno lauko, kuris turi būti patvirtintas prieš atliekant keitimus.</span><span class="sxs-lookup"><span data-stu-id="38f1f-115">In the list of vendor fields, select the **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="38f1f-116">Pasirinkite **Mokėtinos sumos \> Sąranka \> Mokėtinų sumų darbo eigos**.</span><span class="sxs-lookup"><span data-stu-id="38f1f-116">Go to **Accounts payable \> Setup \> Accounts payable workflows**.</span></span>
6. <span data-ttu-id="38f1f-117">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="38f1f-117">Select **New**.</span></span>
7. <span data-ttu-id="38f1f-118">Pasirinkite **Tiekėjo siūlomų pakeitimų darbo eiga**.</span><span class="sxs-lookup"><span data-stu-id="38f1f-118">Select **Proposed vendor changes workflow**.</span></span> 
8. <span data-ttu-id="38f1f-119">Nustatykite darbo eigą, kad ji atitiktų jūsų patvirtinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="38f1f-119">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="38f1f-120">Darbo eigos patvirtinimo elementas **Darbo eigos patvirtinimas dėl tiekėjo siūlomo pakeitimo** pritaikys pakeitimus tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="38f1f-120">The **Workflow approval for proposed vendor change** workflow approval element will apply the changes to the vendor.</span></span>

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="38f1f-121">Tiekėjo informacijos keitimas ir pakeitimų pateikimas į darbo eigą</span><span class="sxs-lookup"><span data-stu-id="38f1f-121">Change vendor information and submit the changes to the workflow</span></span>

<span data-ttu-id="38f1f-122">Pakeitus lauką, kurio darbo eiga įjungta, rodomas puslapis **Siūlomi pakeitimai**.</span><span class="sxs-lookup"><span data-stu-id="38f1f-122">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="38f1f-123">Šiame puslapyje rodoma pradinė lauko reikšmė ir nauja įvesta reikšmė.</span><span class="sxs-lookup"><span data-stu-id="38f1f-123">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="38f1f-124">Nustatoma pradinė pakeisto lauko reikšmė.</span><span class="sxs-lookup"><span data-stu-id="38f1f-124">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="38f1f-125">Būsenos pranešimas taip pat nurodo, kad pakeitimai nebuvo pateikti.</span><span class="sxs-lookup"><span data-stu-id="38f1f-125">A status message also informs you that your changes haven't been submitted.</span></span> 

<span data-ttu-id="38f1f-126">Kiekvieną kartą pakeitus lauką, kurio darbo eiga įjungta, tas laukas įtraukiamas į sąrašą puslapyje **Siūlomi pakeitimai**.</span><span class="sxs-lookup"><span data-stu-id="38f1f-126">Every time that you change a field that is enabled for the workflow, that field is added to the list on the **Proposed changes** page.</span></span> <span data-ttu-id="38f1f-127">Norėdami atmesti siūlomą lauko reikšmę, naudokite mygtuką **Atmesti**, pateiktą šalia lauko sąraše.</span><span class="sxs-lookup"><span data-stu-id="38f1f-127">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="38f1f-128">Norėdami atmesti visus keitimus, naudokite mygtuką **Atmesti visus keitimus** puslapio apačioje.</span><span class="sxs-lookup"><span data-stu-id="38f1f-128">To discard all changes, use the **Discard all changes** button at the bottom of the page.</span></span> <span data-ttu-id="38f1f-129">Pasirinkite **Gerai** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="38f1f-129">Select **OK** to close the page.</span></span>

<span data-ttu-id="38f1f-130">Kai pateikiamas bent vienas siūlomas pakeitimas, veiksmų srityje rodomi du papildomi skirtukai: **Siūlomi pakeitimai** ir **Darbo eigos**.</span><span class="sxs-lookup"><span data-stu-id="38f1f-130">After you have at least one proposed change, two additional tabs appear on the action pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="38f1f-131">Pasirinkite **Siūlomi pakeitimai**, kad atidarytumėte puslapį **Siūlomi pakeitimai** ir peržiūrėtumėte savo pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="38f1f-131">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="38f1f-132">Pasirinkite **Darbo eiga \> Pateikti**, kad pateiktumėte pakeitimus į darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="38f1f-132">Select **Workflow \> Submit to submit the changes to workflow**.</span></span>

    <span data-ttu-id="38f1f-133">Puslapio būsena pakeičiama į **Pakeitimai laukia patvirtinimo**.</span><span class="sxs-lookup"><span data-stu-id="38f1f-133">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="38f1f-134">Darbo eiga seka standartinį darbo eigos procesą „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="38f1f-134">The workflow follows the standard workflow process in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="38f1f-135">Tvirtintojas nukreipiamas į puslapį **Tiekėjas**, kuriame jis gali peržiūrėti pakeitimus puslapyje **Siūlomi pakeitimai**, pasirinkti **Darbo eiga \> Patvirtinti** ir patvirtinti darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="38f1f-135">The approver is directed to the **Vendor** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="38f1f-136">Viską patvirtinus, laukai atnaujinami reikšmėmis, kurias pasiūlėte.</span><span class="sxs-lookup"><span data-stu-id="38f1f-136">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
