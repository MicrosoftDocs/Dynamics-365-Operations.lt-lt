---
title: Supažindinimo šablono kūrimas, naudojant „Dynamics 365 Talent - Onboard”
description: Šioje temoje paaiškinama, kaip „Microsoft Dynamics 365 Talent - Onboard” programėlėje sukurti supažindinimo vadovo šabloną, skirtą jūsų naujiems darbuotojams. Ši užduotis yra esminis pirmas žingsnis žmogiškojo kapitalo valdymo (HCM) nuo įdarbinimo iki atleidimo strategijoje.
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5c322a0dd9a3c61a2d333fdc716acde88a2165f0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462006"
---
# <a name="create-an-onboarding-template"></a><span data-ttu-id="4ad39-104">Supažindinimo šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="4ad39-104">Create an onboarding template</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4ad39-105">„Microsoft Dynamics 365 Talent: Onboard” pateikia įvairius šablonus, kurie gali padėti jums sukurti supažindinimo vadovus kuo greičiau.</span><span class="sxs-lookup"><span data-stu-id="4ad39-105">Microsoft Dynamics 365 Talent: Onboard provides various templates that can help you create an onboarding guide as quickly as possible.</span></span> <span data-ttu-id="4ad39-106">Galite naudoti vieną ar daugiau iš šių šablonų arba galite sukurti savo šablonus.</span><span class="sxs-lookup"><span data-stu-id="4ad39-106">You can use one or more of these templates, or you can create your own templates.</span></span> <span data-ttu-id="4ad39-107">„Onboard” pateikia pavyzdinį tekstą, kurį galite naudoti kurdami savo šablonus.</span><span class="sxs-lookup"><span data-stu-id="4ad39-107">Onboard provides sample text that you can use when you create your own templates.</span></span> <span data-ttu-id="4ad39-108">Todėl procesas yra paprastas, net jei pradėsite nuo nulio.</span><span class="sxs-lookup"><span data-stu-id="4ad39-108">Therefore, the process is easy even if you start from scratch.</span></span>

## <a name="create-an-onboarding-template-from-an-existing-template"></a><span data-ttu-id="4ad39-109">Supažindinimo šablono kūrimas iš esamo šablono</span><span class="sxs-lookup"><span data-stu-id="4ad39-109">Create an onboarding template from an existing template</span></span>

1. <span data-ttu-id="4ad39-110">Kairiajame meniu pasirinkite **Šablonai**.</span><span class="sxs-lookup"><span data-stu-id="4ad39-110">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="4ad39-111">Dalyje **Populiarūs šablonai iš galerijos** arba **Mano šablonai** pasirinkite šabloną.</span><span class="sxs-lookup"><span data-stu-id="4ad39-111">Under **Popular templates from the gallery** or **My templates**, select a template.</span></span> <span data-ttu-id="4ad39-112">Norėdami peržiūrėti daugiau šablonų, pasirinkite **Daugiau šablonų galerijoje**.</span><span class="sxs-lookup"><span data-stu-id="4ad39-112">To view more templates, select **More in template gallery**.</span></span>
3. <span data-ttu-id="4ad39-113">Atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="4ad39-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="4ad39-114">Jei šablonas yra iš galerijos, pasirinkite **Įrašyti kaip mano šabloną**, įveskite naują šablono pavadinimą ir pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4ad39-114">If the template is from the gallery, select **Save as my template**, enter a new name for the template, and select **Save**.</span></span>
    - <span data-ttu-id="4ad39-115">Jei šablonas yra iš **Mano šablonai**, pasirinkite **Įrašyti kaip šabloną**, įveskite naują šablono pavadinimą ir pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4ad39-115">If the template is from **My templates**, select **Save as template**, enter a new name for the template, and select **Save**.</span></span>

    <span data-ttu-id="4ad39-116">[![Šablono kūrimas iš esamo šablono](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span><span class="sxs-lookup"><span data-stu-id="4ad39-116">[![Creating a template from an existing template](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span></span>

## <a name="create-a-new-onboarding-template"></a><span data-ttu-id="4ad39-117">Naujo supažindinimo šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="4ad39-117">Create a new onboarding template</span></span>

1. <span data-ttu-id="4ad39-118">Kairiajame meniu pasirinkite **Šablonai**.</span><span class="sxs-lookup"><span data-stu-id="4ad39-118">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="4ad39-119">Dalyje **Mano šablonai** pasirinkite plytelę **Įtraukti** (pliuso ženklas \[**+**\]).</span><span class="sxs-lookup"><span data-stu-id="4ad39-119">Under **My templates**, select the **Add** (plus sign \[**+**\]) tile.</span></span>

    <span data-ttu-id="4ad39-120">[![Naujo šablono kūrimas](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span><span class="sxs-lookup"><span data-stu-id="4ad39-120">[![Creating a new template](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span></span>

3. <span data-ttu-id="4ad39-121">Dialogo lange **Kurti vadovo šabloną** įveskite šablono pavadinimą, tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4ad39-121">In the **Create a guide template** dialog box, enter a name for the template, and then select **Save**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="4ad39-122">Kiti veiksmai</span><span class="sxs-lookup"><span data-stu-id="4ad39-122">Next steps</span></span>

- [<span data-ttu-id="4ad39-123">Supažindinimo vadovų ir šablonų redagavimas</span><span class="sxs-lookup"><span data-stu-id="4ad39-123">Edit onboarding guides and templates</span></span>](./onboard-edit-guides-templates.md)
- [<span data-ttu-id="4ad39-124">Turinio bendrinimas su kitais bendraautoriais</span><span class="sxs-lookup"><span data-stu-id="4ad39-124">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="4ad39-125">Užduočių ir darbuotojų supažindinimo būsenos peržiūra</span><span class="sxs-lookup"><span data-stu-id="4ad39-125">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="4ad39-126">Samdos komandų kūrimas „Onboard”</span><span class="sxs-lookup"><span data-stu-id="4ad39-126">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="4ad39-127">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="4ad39-127">See also</span></span>

- [<span data-ttu-id="4ad39-128">Išbandykite arba įsigykite „Onboard” programėlę</span><span class="sxs-lookup"><span data-stu-id="4ad39-128">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="4ad39-129">Kas nauja arba pasikeitė „Dynamics 365 Talent“</span><span class="sxs-lookup"><span data-stu-id="4ad39-129">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="4ad39-130">Leidimo planai</span><span class="sxs-lookup"><span data-stu-id="4ad39-130">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="4ad39-131">Palaikymo dėl „Microsoft Dynamics 365 Talent“ gavimas</span><span class="sxs-lookup"><span data-stu-id="4ad39-131">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
