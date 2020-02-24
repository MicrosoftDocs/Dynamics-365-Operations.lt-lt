---
title: Registracijos tinkamumo apdorojimas
description: Šiame straipsnyje paaiškinama, kaip vykdyti registracijos tinkamumo apdorojimą.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0344c48460a7d1540481e09ba106526e119de72b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009885"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="85489-103">Registracijos tinkamumo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="85489-103">Process enrollment eligibility</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="85489-104">Šiame straipsnyje paaiškinama, kaip vykdyti registracijos tinkamumo apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="85489-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="85489-105">Darbo srities **Išmokų valdymas** dalyje **Apdorojimas** pasirinkite **Registracijos tinkamumo apdorojimas**.</span><span class="sxs-lookup"><span data-stu-id="85489-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="85489-106">Dialogo lange **Vykdyti registracijos išmokoms gauti tinkamumo apdorojimą** nurodykite šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="85489-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="85489-107">Laukas</span><span class="sxs-lookup"><span data-stu-id="85489-107">Field</span></span> | <span data-ttu-id="85489-108">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="85489-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="85489-109">Registracijos laikotarpis</span><span class="sxs-lookup"><span data-stu-id="85489-109">Enrollment period</span></span> | <span data-ttu-id="85489-110">Ragistracijos tinkamumo apdorojimo registracijos laikotarpis.</span><span class="sxs-lookup"><span data-stu-id="85489-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="85489-111">Juridinis subjektas</span><span class="sxs-lookup"><span data-stu-id="85489-111">Legal entity</span></span> | <span data-ttu-id="85489-112">Registracijos tinkamumo apdorojimo juridinis subjektas.</span><span class="sxs-lookup"><span data-stu-id="85489-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="85489-113">Darbininkas</span><span class="sxs-lookup"><span data-stu-id="85489-113">Worker</span></span> | <span data-ttu-id="85489-114">Registracijos tinkamumo apdorojimo darbininkas.</span><span class="sxs-lookup"><span data-stu-id="85489-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="85489-115">Jei paliksite šį lauką tuščią, visų darbuotojų registracijos tinkamumas bus apdorojamas.</span><span class="sxs-lookup"><span data-stu-id="85489-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="85489-116">Išmokų planas</span><span class="sxs-lookup"><span data-stu-id="85489-116">Benefit plan</span></span> | <span data-ttu-id="85489-117">Registracijos tinkamumo apdorojimo išmokų planas.</span><span class="sxs-lookup"><span data-stu-id="85489-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="85489-118">Jei norite vykdyti procesą fone, pasirinkite **Vykdyti fone** ir atlikite šias užduotis:</span><span class="sxs-lookup"><span data-stu-id="85489-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="85489-119">Įveskite proceso informaciją.</span><span class="sxs-lookup"><span data-stu-id="85489-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="85489-120">Norėdami nustatyti pasikartojančią užduotį, pasirinkite **Pasikartojimas**, įveskite pasikartojimo informaciją ir pažymėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="85489-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="85489-121">Norėdami nustatyti užduoties įspėjimą, pasirinkite **Įspėjimai**, pasirinkite gautinus įspėjimus, tada pažymėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="85489-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="85489-122">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="85489-122">Select **OK**.</span></span> <span data-ttu-id="85489-123">Procesas bus vykdomas naudojant jūsų nustatytus parametrus.</span><span class="sxs-lookup"><span data-stu-id="85489-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="85489-124">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="85489-124">Select **OK**.</span></span>
