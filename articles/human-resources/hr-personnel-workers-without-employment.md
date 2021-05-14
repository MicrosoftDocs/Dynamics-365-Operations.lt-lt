---
title: Neįdarbinti darbininkai
description: Darbuotojai, kurie neturi jokio būsimo, aktyvaus arba retrospektyvio įdarbinimo jūsų organizacijoje, rodomi darbuotojų formoje Be įdarbinimo.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1a137de25924f4c4ec6f6b1fe70f9d21af591c0
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924576"
---
# <a name="workers-without-employment"></a><span data-ttu-id="77a5b-103">Neįdarbinti darbininkai</span><span class="sxs-lookup"><span data-stu-id="77a5b-103">Workers without employment</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="77a5b-104">Darbuotojai, kurie neturi jokio būsimo, aktyvaus arba retrospektyvio įdarbinimo jūsų organizacijoje, rodomi **darbuotojų Be įdarbinimo**.</span><span class="sxs-lookup"><span data-stu-id="77a5b-104">Workers with no future, active, or historical employment with your organization appear in the **Workers without employment** form.</span></span> <span data-ttu-id="77a5b-105">Šios būsenos darbuotojai gali būti rodomi importuojant darbuotojus be įdarbinimo įrašų arba kai panaikinate darbuotojo įdarbinimas per **Darbuotojai > Įdarbinimo** retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="77a5b-105">Workers with this status can appear when you import workers without an employment record, or when you delete a worker's employment via **Workers > Employment history**.</span></span>

<span data-ttu-id="77a5b-106">Numatyta, kad **formoje Darbuotojai be įdarbinimo gali būti galimi šie** vaidmenys:</span><span class="sxs-lookup"><span data-stu-id="77a5b-106">By default, the **Workers without employment** form is available to the following roles:</span></span>

- <span data-ttu-id="77a5b-107">Žmogiškųjų išteklių asistentas</span><span class="sxs-lookup"><span data-stu-id="77a5b-107">Human Resources Assistant</span></span>
- <span data-ttu-id="77a5b-108">Žmogiškųjų išteklių vadovas</span><span class="sxs-lookup"><span data-stu-id="77a5b-108">Human Resources Manager</span></span>
- <span data-ttu-id="77a5b-109">Darbdavys</span><span class="sxs-lookup"><span data-stu-id="77a5b-109">Recruiter</span></span>
- <span data-ttu-id="77a5b-110">Kompensacijų ir priedų vadovas</span><span class="sxs-lookup"><span data-stu-id="77a5b-110">Comp and Benefits Manager</span></span>
- <span data-ttu-id="77a5b-111">Mokėjimo administratorius</span><span class="sxs-lookup"><span data-stu-id="77a5b-111">Payroll Administrator</span></span>
- <span data-ttu-id="77a5b-112">Mokėjimo vadovas</span><span class="sxs-lookup"><span data-stu-id="77a5b-112">Payroll Manager</span></span>
- <span data-ttu-id="77a5b-113">Mokymo vadovas</span><span class="sxs-lookup"><span data-stu-id="77a5b-113">Training Manager</span></span>

<span data-ttu-id="77a5b-114">Darbuotojų **sąraše be** įdarbinimo galite panaikinti nurodytus asmenis.</span><span class="sxs-lookup"><span data-stu-id="77a5b-114">In the **Workers without employment** list, you can delete the individuals listed.</span></span> <span data-ttu-id="77a5b-115">Numatyta, kad ši teisė suteikiama personalo asistento vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="77a5b-115">By default, this privilege is given to the Human Resources Assistant role.</span></span> <span data-ttu-id="77a5b-116">Šią teisę galite suteikti kitiems vaidmenims, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="77a5b-116">You can give this privilege to other roles with the following steps:</span></span>

1. <span data-ttu-id="77a5b-117">Pasirinkite **Sistemos administravimas**, tada pasirinkite skirtuką **Saugo konfigūravimas**.</span><span class="sxs-lookup"><span data-stu-id="77a5b-117">Select **System administration**, and then select **Security configuration**.</span></span>

2. <span data-ttu-id="77a5b-118">Skirtuke **Teisės** filtruokite sąrašą **Teisės**, kad būtų rodoma parinktis **Prižiūrėti darbininkus**.</span><span class="sxs-lookup"><span data-stu-id="77a5b-118">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>

   <span data-ttu-id="77a5b-119">[![Filtravimo privilegijų sąrašas](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span><span class="sxs-lookup"><span data-stu-id="77a5b-119">[![Filter Privileges list](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span></span>

3. <span data-ttu-id="77a5b-120">Stulpelyje **Nuorodos** pasirinkite **Rodyti meniu elementus**.</span><span class="sxs-lookup"><span data-stu-id="77a5b-120">In the **References** column, select **Display menu items**.</span></span>

4. <span data-ttu-id="77a5b-121">**Rodyti meniu elementus** pasirinkite **HcmWorkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="77a5b-121">In **Display menu items**, select **HcmWorkersWithoutEmployment**.</span></span>

   <span data-ttu-id="77a5b-122">[![Pasirinkti formą](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span><span class="sxs-lookup"><span data-stu-id="77a5b-122">[![Select form](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span></span>

5. <span data-ttu-id="77a5b-123">Nustatykite **Naikinti** teises į **Suteikti**.</span><span class="sxs-lookup"><span data-stu-id="77a5b-123">Set the **Delete** permission to **Grant**.</span></span>

6. <span data-ttu-id="77a5b-124">Pasirinkite skirtuką **Nepublikuoti objektai**.</span><span class="sxs-lookup"><span data-stu-id="77a5b-124">Select the **Unpublished objects** tab.</span></span>

7. <span data-ttu-id="77a5b-125">Pasirinkite **Publikuoti viską**.</span><span class="sxs-lookup"><span data-stu-id="77a5b-125">Select **Publish all**.</span></span>

   <span data-ttu-id="77a5b-126">[![Skelbti pakeitimus](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span><span class="sxs-lookup"><span data-stu-id="77a5b-126">[![Publish changes](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]