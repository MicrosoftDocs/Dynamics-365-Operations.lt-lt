---
title: Kliento darbo eiga
description: Šioje temoje pateikiama informacijos apie kliento darbo eigą. Galite keisti konkrečius kliento laukus ir, naudodami šią darbo eigą, tuos keitimus siųsti tvirtinti, prieš juos įtraukiant prie kliento.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 8ff91a1df82d6195da266b97c347ef27afec662d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176029"
---
# <a name="customer-workflow"></a><span data-ttu-id="07b08-104">Kliento darbo eiga</span><span class="sxs-lookup"><span data-stu-id="07b08-104">Customer workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07b08-105">Į 8.0.4 versiją įtraukta klientų darbo eiga.</span><span class="sxs-lookup"><span data-stu-id="07b08-105">The customer workflow has been added to version 8.0.4.</span></span> <span data-ttu-id="07b08-106">Galite keisti konkrečius kliento laukus ir, naudodami šią darbo eigą, tuos keitimus siųsti tvirtinti, prieš juos įtraukiant prie kliento.</span><span class="sxs-lookup"><span data-stu-id="07b08-106">You can change specific fields for a customer and then send those changes for approval by using the workflow before they are added to the customer.</span></span>

## <a name="set-up-the-customer-workflow"></a><span data-ttu-id="07b08-107">Kliento darbo eigos nustatymas</span><span class="sxs-lookup"><span data-stu-id="07b08-107">Set up the customer workflow</span></span>

<span data-ttu-id="07b08-108">Kad galėtumėte naudoti kliento darbo eigos funkciją, turite ją įjungti.</span><span class="sxs-lookup"><span data-stu-id="07b08-108">Before you can use the customer workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="07b08-109">Eikite į **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="07b08-109">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="07b08-110">Norėdami įjungti šią funkciją, skirtuko **Bendra** „FastTab“ konteineryje **Klientų tvirtinimas** parinktį **Įjungti klientų tvirtinimus** nustatykite kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="07b08-110">On the **General** tab, on the **Customer approval** FastTab, set the **Enable customer approvals** option to **Yes** to enable the feature.</span></span>
3. <span data-ttu-id="07b08-111">Lauke **Duomenų objektų veikimo būdas** pasirinkite vieną iš tolesnių veikimo būdų, kurį turi naudoti duomenų objektai, kai importuojami duomenys.</span><span class="sxs-lookup"><span data-stu-id="07b08-111">In the **Data entity behavior** field, select the behavior that the data entities should use when data is imported:</span></span>

    - <span data-ttu-id="07b08-112">**Leisti keisti netvirtinant** – objektas kliento įrašą gali atnaujinti jo neapdorodamas darbo eigoje.</span><span class="sxs-lookup"><span data-stu-id="07b08-112">**Allow changes without approval** – An entity can update the customer record without processing it through the workflow.</span></span>
    - <span data-ttu-id="07b08-113">**Atmesti keitimus** – kliento įrašo keisti negalima.</span><span class="sxs-lookup"><span data-stu-id="07b08-113">**Reject changes** – Changes can't be made to the customer record.</span></span> <span data-ttu-id="07b08-114">Įjungtų darbo eigos laukų importuoti nepavyks.</span><span class="sxs-lookup"><span data-stu-id="07b08-114">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="07b08-115">**Kurti keitimo pasiūlymus** – bus pakeisti visi laukai, išskyrus įjungtus darbo eigos laukus.</span><span class="sxs-lookup"><span data-stu-id="07b08-115">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="07b08-116">Naujosios tų laukų reikšmės prie kliento bus įtrauktos kaip siūlomi keitimai, o darbo eiga bus pradėta automatiškai.</span><span class="sxs-lookup"><span data-stu-id="07b08-116">The new values for those fields will be added to the customer as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="07b08-117">Tada kliento laukų sąraše prie kiekvieno lauko, kurį reikia patvirtinti, kad būtų galima atlikti keitimus, pažymėkite žymės langelį **Įjungti**.</span><span class="sxs-lookup"><span data-stu-id="07b08-117">In the list of customer fields, select then **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="07b08-118">Eikite į **Gautinos sumos \> Sąranka \> Gautinų sumų darbo eigos**.</span><span class="sxs-lookup"><span data-stu-id="07b08-118">Go to **Accounts receivable \> Setup \> Accounts receivable workflows**.</span></span>
6. <span data-ttu-id="07b08-119">Pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="07b08-119">Select **New**.</span></span>
7. <span data-ttu-id="07b08-120">Pasirinkite **Siūlomų kliento keitimų darbo eiga**.</span><span class="sxs-lookup"><span data-stu-id="07b08-120">Select **Proposed customer change workflow**.</span></span> 
8. <span data-ttu-id="07b08-121">Darbo eigą nustatykite taip, kad ji atitiktų jūsų tvirtinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="07b08-121">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="07b08-122">Darbo eigos **Siūlomo kliento keitimo darbo eigos tvirtinimas** tvirtinimo elementas keitimus pritaikys klientui.</span><span class="sxs-lookup"><span data-stu-id="07b08-122">The **Workflow approval for proposed customer change** workflow approval element will apply the changes to the customer.</span></span>

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="07b08-123">Kliento informacijos keitimas ir keitimų teikimas į darbo eigą</span><span class="sxs-lookup"><span data-stu-id="07b08-123">Change customer information and submit the changes to the workflow</span></span>

<span data-ttu-id="07b08-124">Kai keičiate įjungtą darbo eigos lauką, pasirodo puslapis **Siūlomi keitimai**.</span><span class="sxs-lookup"><span data-stu-id="07b08-124">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="07b08-125">Šiame puslapyje rodoma pradinė lauko reikšmė ir jūsų įvesta nauja reikšmė.</span><span class="sxs-lookup"><span data-stu-id="07b08-125">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="07b08-126">Jūsų pakeistame lauke grąžinama pradinė jo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="07b08-126">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="07b08-127">Puslapyje būsenos pranešimas jums praneša, kad jūsų keitimai nepateikti.</span><span class="sxs-lookup"><span data-stu-id="07b08-127">A status message on the page informs you that your changes haven't been submitted.</span></span>

<span data-ttu-id="07b08-128">Jums kaskart keičiant įjungtą darbo eigos lauką, jis įtraukiamas į siūlomų keitimų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="07b08-128">Every time that you change a field that is enabled for the workflow, that field is added to the list of proposed changes.</span></span> <span data-ttu-id="07b08-129">Norėdami atmesti siūlomą lauko reikšmę, naudokite prie sąraše esančio lauko esantį mygtuką **Atmesti**.</span><span class="sxs-lookup"><span data-stu-id="07b08-129">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="07b08-130">Norėdami atmesti visus keitimus, naudokite puslapio apačioje esantį mygtuką **Atmesti visus keitimus**.</span><span class="sxs-lookup"><span data-stu-id="07b08-130">To discard all changes, use the **Discard all change** button at the bottom of the page.</span></span> <span data-ttu-id="07b08-131">Norėdami uždaryti puslapį, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="07b08-131">Select **OK** to close the page.</span></span>

<span data-ttu-id="07b08-132">Kai turite bent vieną siūlomą keitimą, veiksmų srityje atsiranda du papildomi meniu: **Siūlomi keitimai** ir **Darbo eiga**.</span><span class="sxs-lookup"><span data-stu-id="07b08-132">After you have at least one proposed change, two additional menus appear on the Action Pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="07b08-133">Pasirinkdami **Siūlomi keitimai**, galite atidaryti puslapį **Siūlomi keitimai** ir peržiūrėti savo keitimus.</span><span class="sxs-lookup"><span data-stu-id="07b08-133">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="07b08-134">Pasirinkite **Darbo eiga \> Pateikti**, kad keitimus pateiktumėte į darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="07b08-134">Select **Workflow \> Submit** to submit the changes to the workflow.</span></span>

    <span data-ttu-id="07b08-135">Puslapio būsena pakeičiama į **Patvirtinimo laukiantys keitimai**.</span><span class="sxs-lookup"><span data-stu-id="07b08-135">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="07b08-136">Ši darbo eiga vykdoma pagal standartinį programos darbo eigų procesą.</span><span class="sxs-lookup"><span data-stu-id="07b08-136">The workflow follows the standard workflow process in the application.</span></span> <span data-ttu-id="07b08-137">Tvirtintojas nukreipiamas į puslapį **Klientas**, kurio puslapyje **Siūlomi keitimai** jis gali peržiūrėti keitimus ir, pasirinkdamas **Darbo eiga \> Patvirtinti**, patvirtinti darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="07b08-137">The approver is directed to the **Customer** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="07b08-138">Viską patvirtinus, laukai yra atnaujinami jūsų pasiūlytomis reikšmėmis.</span><span class="sxs-lookup"><span data-stu-id="07b08-138">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
