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
ms.openlocfilehash: a1fac239524d4873a782e6a3d177a573a382d0f6
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552048"
---
# <a name="create-an-onboarding-template-by-using-dynamics-365-talent---onboard"></a><span data-ttu-id="7c7db-104">Supažindinimo šablono kūrimas, naudojant „Dynamics 365 Talent - Onboard”</span><span class="sxs-lookup"><span data-stu-id="7c7db-104">Create an onboarding template by using Dynamics 365 Talent - Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7c7db-105">„Microsoft Dynamics 365 Talent: Onboard” pateikia įvairius šablonus, kurie gali padėti jums sukurti supažindinimo vadovus kuo greičiau.</span><span class="sxs-lookup"><span data-stu-id="7c7db-105">Microsoft Dynamics 365 Talent: Onboard provides various templates that can help you create an onboarding guide as quickly as possible.</span></span> <span data-ttu-id="7c7db-106">Galite naudoti vieną ar daugiau iš šių šablonų arba galite sukurti savo šablonus.</span><span class="sxs-lookup"><span data-stu-id="7c7db-106">You can use one or more of these templates, or you can create your own templates.</span></span> <span data-ttu-id="7c7db-107">„Onboard” pateikia pavyzdinį tekstą, kurį galite naudoti kurdami savo šablonus.</span><span class="sxs-lookup"><span data-stu-id="7c7db-107">Onboard provides sample text that you can use when you create your own templates.</span></span> <span data-ttu-id="7c7db-108">Todėl procesas yra paprastas, net jei pradėsite nuo nulio.</span><span class="sxs-lookup"><span data-stu-id="7c7db-108">Therefore, the process is easy even if you start from scratch.</span></span>

## <a name="create-an-onboarding-template-from-an-existing-template"></a><span data-ttu-id="7c7db-109">Supažindinimo šablono kūrimas iš esamo šablono</span><span class="sxs-lookup"><span data-stu-id="7c7db-109">Create an onboarding template from an existing template</span></span>

1. <span data-ttu-id="7c7db-110">Kairiajame meniu pasirinkite **Šablonai**.</span><span class="sxs-lookup"><span data-stu-id="7c7db-110">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="7c7db-111">Dalyje **Populiarūs šablonai iš galerijos** arba **Mano šablonai** pasirinkite šabloną.</span><span class="sxs-lookup"><span data-stu-id="7c7db-111">Under **Popular templates from the gallery** or **My templates**, select a template.</span></span> <span data-ttu-id="7c7db-112">Norėdami peržiūrėti daugiau šablonų, pasirinkite **Daugiau šablonų galerijoje**.</span><span class="sxs-lookup"><span data-stu-id="7c7db-112">To view more templates, select **More in template gallery**.</span></span>
3. <span data-ttu-id="7c7db-113">Atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="7c7db-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="7c7db-114">Jei šablonas yra iš galerijos, pasirinkite **Įrašyti kaip mano šabloną**, įveskite naują šablono pavadinimą ir pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7c7db-114">If the template is from the gallery, select **Save as my template**, enter a new name for the template, and select **Save**.</span></span>
    - <span data-ttu-id="7c7db-115">Jei šablonas yra iš **Mano šablonai**, pasirinkite **Įrašyti kaip šabloną**, įveskite naują šablono pavadinimą ir pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7c7db-115">If the template is from **My templates**, select **Save as template**, enter a new name for the template, and select **Save**.</span></span>

    <span data-ttu-id="7c7db-116">[![Šablono kūrimas iš esamo šablono](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span><span class="sxs-lookup"><span data-stu-id="7c7db-116">[![Creating a template from an existing template](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span></span>

## <a name="create-a-new-onboarding-template"></a><span data-ttu-id="7c7db-117">Naujo supažindinimo šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="7c7db-117">Create a new onboarding template</span></span>

1. <span data-ttu-id="7c7db-118">Kairiajame meniu pasirinkite **Šablonai**.</span><span class="sxs-lookup"><span data-stu-id="7c7db-118">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="7c7db-119">Dalyje **Mano šablonai** pasirinkite plytelę **Įtraukti** (pliuso ženklas \[**+**\]).</span><span class="sxs-lookup"><span data-stu-id="7c7db-119">Under **My templates**, select the **Add** (plus sign \[**+**\]) tile.</span></span>

    <span data-ttu-id="7c7db-120">[![Naujo šablono kūrimas](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span><span class="sxs-lookup"><span data-stu-id="7c7db-120">[![Creating a new template](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span></span>

3. <span data-ttu-id="7c7db-121">Dialogo lange **Kurti vadovo šabloną** įveskite šablono pavadinimą, tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7c7db-121">In the **Create a guide template** dialog box, enter a name for the template, and then select **Save**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7c7db-122">Kiti veiksmai</span><span class="sxs-lookup"><span data-stu-id="7c7db-122">Next steps</span></span>

- [<span data-ttu-id="7c7db-123">Supažindinimo vadovų ir šablonų redagavimas</span><span class="sxs-lookup"><span data-stu-id="7c7db-123">Edit onboarding guides and templates</span></span>](./onboard-edit-guides-templates.md)
- [<span data-ttu-id="7c7db-124">Turinio bendrinimas su kitais bendraautoriais</span><span class="sxs-lookup"><span data-stu-id="7c7db-124">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="7c7db-125">Užduočių ir darbuotojų supažindinimo būsenos peržiūra</span><span class="sxs-lookup"><span data-stu-id="7c7db-125">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="7c7db-126">Samdos komandų kūrimas „Onboard”</span><span class="sxs-lookup"><span data-stu-id="7c7db-126">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="7c7db-127">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="7c7db-127">See also</span></span>

- [<span data-ttu-id="7c7db-128">Išbandykite arba įsigykite „Onboard” programėlę</span><span class="sxs-lookup"><span data-stu-id="7c7db-128">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="7c7db-129">Kas nauja</span><span class="sxs-lookup"><span data-stu-id="7c7db-129">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="7c7db-130">Leidimo pastabos</span><span class="sxs-lookup"><span data-stu-id="7c7db-130">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="7c7db-131">Palaikymo gavimas</span><span class="sxs-lookup"><span data-stu-id="7c7db-131">Get support</span></span>](./talent-support.md)
