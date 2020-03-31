---
title: Naujo dokumento vartotojo sąsaja funkcijoje Verslo dokumentų valdymas
description: Šioje temoje pateikiama informacija apie tai, kaip naudoti naujo dokumento vartotojo sąsają (UI) elektroninių ataskaitų (ER) sistemos funkcijoje Verslo dokumentų valdymas.
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4acde9703c721ab7c20d1603299a10dda91b23c4
ms.sourcegitcommit: b8f8ccab2cd9d848e5ecd71caaf0a63237e2236b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2020
ms.locfileid: "2957068"
---
# <a name="new-document-user-interface-in-business-document-management"></a><span data-ttu-id="b9941-103">Naujo dokumento vartotojo sąsaja funkcijoje Verslo dokumentų valdymas</span><span class="sxs-lookup"><span data-stu-id="b9941-103">New document user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9941-104">Verslo dokumentų valdymas leidžia verslo vartotojams redaguoti verslo dokumentų šablonus naudojant „Microsoft Office 365“ paslaugą arba atitinkamą „Microsoft Office“ darbalaukio programą.</span><span class="sxs-lookup"><span data-stu-id="b9941-104">Business document management lets business users edit business document templates by using a Microsoft Office 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="b9941-105">Redagavimas gali būti dizaino keitimai arba nauji diegimai arba vartotojai gali įtraukti vietos rezervavimo ženklų, kad galėtų įtraukti papildomų duomenų, nekeisdami šaltinio kodo.</span><span class="sxs-lookup"><span data-stu-id="b9941-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="b9941-106">Norėdami gauti daugiau informacijos apie tai, kaip naudotis funkcija Verslo dokumentų valdymas, žr. [Funkcijos Verslo dokumentų valdymas apžvalga](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="b9941-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="b9941-107">Naujo dokumento vartotojo sąsaja (UI) yra aiškesnė ir patogesnė naudoti.</span><span class="sxs-lookup"><span data-stu-id="b9941-107">The new document user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="b9941-108">Srityje **Verslo dokumentas** rodomi tik tie šablonai, kurie yra pasiekiami dabartiniam tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="b9941-108">The **Business document** area shows only the templates that are available for the current provider.</span></span>

<span data-ttu-id="b9941-109">Paspaudę mygtuką **Naujas dokumentas**, vartotojai gali kurti ir redaguoti šabloną elektroninių ataskaitų (ER) formato konfigūracijoje, kurią pateikia kitas teikėjas.</span><span class="sxs-lookup"><span data-stu-id="b9941-109">The **New document** button lets users create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="b9941-110">Šioje temoje pateikiamame pavyzdyje teikėjas yra „Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="b9941-110">In the example in this topic, the provider is Microsoft.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="b9941-111">Naujo dokumento vartotojo sąsajos įjungimas funkcijoje Verslo dokumentų valdymas</span><span class="sxs-lookup"><span data-stu-id="b9941-111">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="b9941-112">Norėdami pradėti naudoti naujo dokumento vartotojo sąsają funkcijoje Verslo dokumentų valdymas, turite įjungti funkciją **Į „Office“ panaši vartotojo sąsaja funkcijoje Verslo dokumentų valdymas** darbo srityje **Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="b9941-112">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="b9941-113">Atlikite tolesnius veiksmus, norėdami įjungti šią funkciją visiems juridiniams subjektams.</span><span class="sxs-lookup"><span data-stu-id="b9941-113">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="b9941-114">Darbo srityje **Funkcijų valdymas** skirtuke **Nauja** sąraše pasirinkite funkciją **Į „Office“ panaši vartotojo sąsaja funkcijoje Verslo dokumentų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="b9941-114">In the **Feature management** workspace, on the **New** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="b9941-115">Pasirinkite **Įjungti dabar**, kad įjungtumėte pasirinktą funkciją.</span><span class="sxs-lookup"><span data-stu-id="b9941-115">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="b9941-116">Norėdami pasiekti naują funkciją, atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b9941-116">Refresh the page to access the new feature.</span></span>

### <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="b9941-117">Šablonų, priklausančių kitiems teikėjams, redagavimas</span><span class="sxs-lookup"><span data-stu-id="b9941-117">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="b9941-118">Darbo srityje **Verslo dokumentų valdymas** pasirinkite **Naujas dokumentas**.</span><span class="sxs-lookup"><span data-stu-id="b9941-118">In the **Business document management** workspace, select **New document**.</span></span>

    ![Darbo sritis Verslo dokumentų valdymas](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="b9941-120">Dialogo lange pasirinkite dokumentą, kurį norite naudoti kaip šabloną, tada pasirinkite **Kurti dokumentą**.</span><span class="sxs-lookup"><span data-stu-id="b9941-120">In the dialog box, select the document to use as a template, and then select **Create document**.</span></span>

    ![Verslo dokumentų dialogo langas](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="b9941-122">Naujo dialogo lango lauke **Pavadinimas** pakeiskite pavadinimą į norimą pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="b9941-122">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="b9941-123">Pavadinimo tekstas naudojamas automatiškai sukurtai naujai ER formato konfigūracijai pavadinti.</span><span class="sxs-lookup"><span data-stu-id="b9941-123">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="b9941-124">Šios konfigūracijos (**Kliento laisvos formos sąskaitos-faktūros ataskaitos (GER) kopija**) juodraščio versijoje bus suredaguotas šablonas ir ji bus naudojama vykdant šį ER formatą, skirtą dabartiniam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="b9941-124">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="b9941-125">Originalus šablonas iš pagrindinio ER formato konfigūracijos bus naudojamas visiems kitiems vartotojams skirtam ER formatui vykdyti.</span><span class="sxs-lookup"><span data-stu-id="b9941-125">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="b9941-126">Lauke **Pavadinimas** pakeiskite redaguojamo šablono, kuris bus automatiškai sukurtas, pirmo pataisymo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="b9941-126">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="b9941-127">Lauke **Komentaras** atnaujinkite redaguojamo šablono, kuris bus automatiškai sukurtas, pataisymo pastabas.</span><span class="sxs-lookup"><span data-stu-id="b9941-127">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="b9941-128">Pasirinkite **Gerai**, kad patvirtintumėte redagavimo proceso pradžią.</span><span class="sxs-lookup"><span data-stu-id="b9941-128">Select **OK** to confirm the start of the editing process.</span></span>

    ![Dokumento kūrimo dialogo langas](./media/BDM_overview_new_template3.png)

<span data-ttu-id="b9941-130">Paspaudus mygtuką **Naujas dokumentas**, sukuriamas ir redaguojamas šablonas ER formato konfigūracijoje, kurią pateikia kitas teikėjas.</span><span class="sxs-lookup"><span data-stu-id="b9941-130">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="b9941-131">Šiame pavyzdyje teikėjas yra „Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="b9941-131">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="b9941-132">Pasirinkę **Naujas dokumentas**, peržiūrėsite visus šablonus, priklausančius dabartiniam ir kitiems teikėjams.</span><span class="sxs-lookup"><span data-stu-id="b9941-132">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="b9941-133">Pasirinktas šablonas atidaromas ir jį galima redaguoti.</span><span class="sxs-lookup"><span data-stu-id="b9941-133">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="b9941-134">Redaguotas šablonas bus išsaugotas naujoje automatiškai sugeneruotoje ER formato konfigūracijoje.</span><span class="sxs-lookup"><span data-stu-id="b9941-134">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

<span data-ttu-id="b9941-135">Daugiau informacijos žr. [Verslo dokumentų valdymo apžvalga](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="b9941-135">For more information, see [Business document management overview](er-business-document-management.md).</span></span>