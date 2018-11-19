---
title: "Proceso šablono kūrimas sprendime „Attract“"
description: "Šioje temoje pateikiama informacija apie tai, kaip sukurti proceso šabloną sprendime „Attract“."
author: hasrivas
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 54c80f3d785ba7a7e0158c51201468f45796c193
ms.contentlocale: lt-lt
ms.lasthandoff: 10/22/2018

---

# <a name="create-a-process-template-in-attract"></a><span data-ttu-id="2d7e6-103">Proceso šablono kūrimas sprendime „Attract“</span><span class="sxs-lookup"><span data-stu-id="2d7e6-103">Create a process template in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2d7e6-104">*Samdos proceso šablone* pateikiamos visos veiklos, kurios turėtų būti įtrauktos samdymo į darbo vietą proceso metu.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-104">A *hiring process template* contains all the activities that should be included as part of the hiring process for a job.</span></span> <span data-ttu-id="2d7e6-105">Šioje temoje aprašomi proceso šablono, naudojamo „Microsoft Dynamics 365 for Talent: Attract“ elementai.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-105">This topic describes the elements of a process template in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="2d7e6-106">Taip pat paaiškinama, kaip sukurti šabloną.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-106">It also explains how to create a template.</span></span>

> [!NOTE]
> <span data-ttu-id="2d7e6-107">Šablonų kūrimas yra išsamios įdarbinimo informacijos priedo, skirto „Attract“ dalis.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-107">Template creation is part of the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="template-management"></a><span data-ttu-id="2d7e6-108">Šablonų valdymas</span><span class="sxs-lookup"><span data-stu-id="2d7e6-108">Template management</span></span>

<span data-ttu-id="2d7e6-109">Organizacijos gali nuspręsti, ar proceso šablonus sprendime „Attract“ gali kurti komandos nariai, ar tik administratoriai.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-109">Organizations can decide whether team members or only admins can create process templates in Attract.</span></span> <span data-ttu-id="2d7e6-110">Norėdami sukonfigūruoti šablonų valdymą, eikite į parinktį **Administravimo centras** \> **Šablonų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-110">To configure template management, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="2d7e6-111">Norėdami leisti komandos nariams kurti savo šablonus, įjunkite šablonų valdymą.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-111">To let team members create their own templates, turn on template management.</span></span> <span data-ttu-id="2d7e6-112">Jei šablonų valdymo neįjungsite, šablonus kurti galės tik administratoriai.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-112">If you don't turn on template management, only admins can create templates.</span></span>

## <a name="default-template"></a><span data-ttu-id="2d7e6-113">Numatytasis šablonas</span><span class="sxs-lookup"><span data-stu-id="2d7e6-113">Default template</span></span>

<span data-ttu-id="2d7e6-114">Numatytąjį šabloną nustatyti gali tik administratoriai.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-114">Only admins can set the default template.</span></span> <span data-ttu-id="2d7e6-115">Numatytasis šablonas naudojamas tada, jei sukūrus darbą nepasirenkamas šablonas.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-115">The default template is used if a template isn't selected when a job is created.</span></span> <span data-ttu-id="2d7e6-116">Norėdami nustatyti numatytąjį šabloną, eikite į parinktį **Administravimo centras** \> **Šablonų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-116">To set the default template, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="2d7e6-117">Šablono, kurį norite nustatyti numatytuoju, kortelėje pasirinkite elipsės mygtuką (**...**), tada pasirinkite **Nustatyti kaip numatytąjį**.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-117">On the card for the template that should be the default template, select the ellipsis button (**...**), and then select **Set as default**.</span></span>

## <a name="create-a-process-template"></a><span data-ttu-id="2d7e6-118">Proceso šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="2d7e6-118">Create a process template</span></span>

<span data-ttu-id="2d7e6-119">Proceso šablonus gali kurti administratoriai, darbdaviai ir samdos vadovai.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-119">Admins, recruiters, and hiring managers can create process templates.</span></span> <span data-ttu-id="2d7e6-120">Proceso šabloną sudaro *etapai* ir *veiklos*.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-120">A process template consists of *stages* and *activities*.</span></span> <span data-ttu-id="2d7e6-121">Etapuose sugrupuota viena arba kelios veiklos.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-121">Stages group together one or more activities.</span></span> <span data-ttu-id="2d7e6-122">Pagal numatytuosius parametrus, kiekviename proceso šablone pateikiamos potencialaus kliento, prašymo ir pasiūlymo veiklos.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-122">By default, every process template has Prospect, Application, and Offer activities.</span></span> <span data-ttu-id="2d7e6-123">Etapus, kuriuose yra šios veiklos, galima pervardyti.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-123">The stages that contain these activities can be renamed.</span></span> <span data-ttu-id="2d7e6-124">Daugiau etapų įtraukti galite pasirinkę **+ Naujas etapas**.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-124">You can add more stages by selecting **+ New Stage**.</span></span> <span data-ttu-id="2d7e6-125">Veiklas į etapą įtraukti galite nuvilkdami jas į atitinkamą etapą arba du kartus spustelėdami veiklas veiklų sąraše.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-125">You can activities to a stage either by dragging them to the appropriate stage or by double-clicking them in the activity list.</span></span>

> [!NOTE]
> <span data-ttu-id="2d7e6-126">Etapo pavadinimai kandidatams rodomi puslapyje **Prašymo būsena**.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-126">Stage names are visible to candidates on the **Application status** page.</span></span> <span data-ttu-id="2d7e6-127">Renkant pavadinimus etapams, reikėtų į šį faktą atsižvelgti.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-127">You should consider this fact when you choose names for stages.</span></span>

<span data-ttu-id="2d7e6-128">Norėdami sužinoti daugiau apie veiklas, žr. [Samdos proceso veiklos sprendime „Attract“](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="2d7e6-128">To learn more about activities, see [Hiring process activities in Attract](./activities-attract.md).</span></span>

<span data-ttu-id="2d7e6-129">Norėdami sukurti samdos proceso šabloną, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-129">Follow these steps to create a hiring process template.</span></span>

1. <span data-ttu-id="2d7e6-130">Eikite į parinktį **Šablonai**.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-130">Go to **Templates**.</span></span>
2. <span data-ttu-id="2d7e6-131">Pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-131">Select **New**.</span></span>
3. <span data-ttu-id="2d7e6-132">Lauke **šablono pavadinimas** įveskite šablono pavadinimą, tada pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-132">In the **Template name** field, enter a name for the template, and then select **Create**.</span></span>
4. <span data-ttu-id="2d7e6-133">Sąraše **Pasirinkite patvirtinimo procesą** pasirinkite **Numatytasis**, kad būtų reikalaujama patvirtinti darbą.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-133">In the **Choose the approval process** list, select **Default** to require approval for a job.</span></span>
5. <span data-ttu-id="2d7e6-134">Pasirinkite norėdami įgalinti arba išjungti potencialius klientus.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-134">Select to enable or disable prospects.</span></span>
6. <span data-ttu-id="2d7e6-135">Pasirenkama: įtraukite etapus arba juos pašalinkite.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-135">Optional: Add or remove stages.</span></span>

    - <span data-ttu-id="2d7e6-136">Norėdami įtraukti etapą, pasirinkite **+ Naujas etapas**.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-136">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="2d7e6-137">Norėdami pašalinti etapą, laikykite žymeklį virš etapo, tada pasirinkite pasirodantį šiukšliadėžės mygtuką.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-137">To remove a stage, hover the pointer over the stage, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="2d7e6-138">Potencialus kliento, prašymo ir pasiūlymo etapų pašalinti negalima, tačiau juos galima pervardyti.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-138">Prospect, Application, and Offer stages can't be removed, but they can be renamed.</span></span>

7. <span data-ttu-id="2d7e6-139">Pasirenkama: įtraukite veiklas arba jas pašalinkite.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-139">Optional: Add or remove activities.</span></span>

    - <span data-ttu-id="2d7e6-140">Norėdami įtraukti veiklą, vilkite ją iš dešinėje pateikto veiklų sąrašo į atitinkamo etapą.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-140">To add an activity, drag it from the activity list on the right to the appropriate stage.</span></span> <span data-ttu-id="2d7e6-141">Taip pat dukart spustelėkite veiklą ir pasirinkite, į kurį etapą norite ją įtraukti.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-141">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="2d7e6-142">Norėdami veiklą pašalinti, ją išplėskite, tada veiklos antraštėje pasirinkite šiukšliadėžės mygtuką.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-142">To remove an activity, expand it, and then select the trash can button on the activity header.</span></span>

8. <span data-ttu-id="2d7e6-143">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2d7e6-143">Select **Save**.</span></span>

