---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. spalio 29 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 83b4734190163ebd2dc29096632642bd45c61e8f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773882"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a><span data-ttu-id="db554-103">Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. spalio 29 d.)</span><span class="sxs-lookup"><span data-stu-id="db554-103">What's new or changed in Dynamics 365 Talent (October 29, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="db554-104">Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 Talent“ funkcijos.</span><span class="sxs-lookup"><span data-stu-id="db554-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="db554-105">„Attract“ pakeitimai</span><span class="sxs-lookup"><span data-stu-id="db554-105">Changes in Attract</span></span>

<span data-ttu-id="db554-106">Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Attract“.</span><span class="sxs-lookup"><span data-stu-id="db554-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="db554-107">Supažindinimo pakeitimai</span><span class="sxs-lookup"><span data-stu-id="db554-107">Changes in Onboard</span></span>

<span data-ttu-id="db554-108">Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Onboard“.</span><span class="sxs-lookup"><span data-stu-id="db554-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="db554-109">„Core HR“ pakeitimai</span><span class="sxs-lookup"><span data-stu-id="db554-109">Changes in Core HR</span></span>

<span data-ttu-id="db554-110">Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2586 komponavimo versijai.</span><span class="sxs-lookup"><span data-stu-id="db554-110">Changes described in this section apply to build number 8.1.2586.</span></span> <span data-ttu-id="db554-111">Kai kurių antraščių skaičiai skliausteliuose nurodo palaikymo numerius „Microsoft Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="db554-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a><span data-ttu-id="db554-112">Šalių, kurios neturi vaidmenų, naikinimas turi būti numatytasis (371233)</span><span class="sxs-lookup"><span data-stu-id="db554-112">Delete parties with no roles should be on by default (371233)</span></span>

<span data-ttu-id="db554-113">Kai ruošiate naują aplinką „Talent“, parametras **Naikinti šalis, jei nėra vaidmenų** turi būti įjungtas pagal numatytuosius parametrus.</span><span class="sxs-lookup"><span data-stu-id="db554-113">When you provision a new environment in Talent, **Delete parties if no roles exist** is turned on by default.</span></span> <span data-ttu-id="db554-114">Kai naikinate darbuotoją, su darbuotoju susijusi šalis yra pašalinama, nebent įjungtas šis parametras.</span><span class="sxs-lookup"><span data-stu-id="db554-114">When you delete a worker, the party associated with the worker is not removed unless this setting is on.</span></span> <span data-ttu-id="db554-115">Šis keitimas apriboja pasikartojančius įrašus visuotinėje adresų knygelėje, kai reikia importuoti, keisti arba iš naujo importuoti darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="db554-115">This change limits duplicate records in the global address book when you need to import, change, or reimport workers.</span></span>

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a><span data-ttu-id="db554-116">Turi būti leidžiama naikinti juodraščius ir atšauktas atostogų užklausas „Common Data Service“ (376999)</span><span class="sxs-lookup"><span data-stu-id="db554-116">Draft and cancelled leave requests should be allowed to be deleted in Common Data Service (376999)</span></span>

<span data-ttu-id="db554-117">Atlikę šį keitimą, galite naikinti užklausas, kurių būsena „Common Data Service“ yra **Juodraštis** arba **Atšaukta** .</span><span class="sxs-lookup"><span data-stu-id="db554-117">With this change, you can now delete leave requests with a status of **Draft** or **Cancelled** in Common Data Service.</span></span>

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a><span data-ttu-id="db554-118">Papildomos sąrašo reikšmės pasirinktiniuose laukuose nėra atspindimos „Common Data Service“ spustelėjus Taikyti pasirinktinių laukų formoje (379599)</span><span class="sxs-lookup"><span data-stu-id="db554-118">Additional list values in custom fields aren't reflected in Common Data Service after clicking Apply on the Custom fields form (379599)</span></span>

<span data-ttu-id="db554-119">Kai įtraukiate naujas sąrašo reikšmes į esamą pasirinktinį lauką, kuris jau sinchronizuotas su „Common Data Service“, jos bus pasiekiamos „Common Data Serivce“, kai keitimus pritaikysite formoje **Pasirinktiniai laukai**</span><span class="sxs-lookup"><span data-stu-id="db554-119">When you add new list values to an existing custom field that has already synchronized with Common Data Service, they're now available in Common Data Serivce after you apply your changes in the **Custom fields** form.</span></span>

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a><span data-ttu-id="db554-120">Taikykite kontrolinius sąrašus tarp juridinių subjektų, kai yra daugiau nei vienas įdarbinimas (371270)</span><span class="sxs-lookup"><span data-stu-id="db554-120">Apply onboarding checklists across legal entities when more than one employment exists (371270)</span></span>

<span data-ttu-id="db554-121">Šiose savaitės leidime galite taikyti kontrolinį sąrašą darbuotojams su daugiau nei vienu įdarbinimu eidami į **Darbuotojo forma > Kontroliniai sąrašai**.</span><span class="sxs-lookup"><span data-stu-id="db554-121">In this week's release, you can apply checklists to employees with more than one employment in **Worker form > Checklists**.</span></span>

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a><span data-ttu-id="db554-122">Išmokų atviros registracijos peržiūros funkcija pašalinta</span><span class="sxs-lookup"><span data-stu-id="db554-122">Benefits open enrollment preview feature has been removed</span></span>

<span data-ttu-id="db554-123">Kartu su mūsų pranešimu, paskelbtu tinklaraščio įraše [Strateginis investavimas į „Core HR“ veiklos efektyvumą](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence), „Microsoft“ pašalino išmokų atviros registracijos funkciją iš viešosios peržiūros.</span><span class="sxs-lookup"><span data-stu-id="db554-123">In conjunction with our announcement in the [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog post, Microsoft has removed the benefits open enrollment feature from public preview.</span></span> <span data-ttu-id="db554-124">Ateityje bus išleistos naujos funkcijos.</span><span class="sxs-lookup"><span data-stu-id="db554-124">New functionality will be released in the future.</span></span> <span data-ttu-id="db554-125">Gamybos išmokų atviros registracijos funkcijos naudojimas nepalaikomas.</span><span class="sxs-lookup"><span data-stu-id="db554-125">Production use of the benefits open enrollment feature isn't be supported.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="db554-126">Jau greitai</span><span class="sxs-lookup"><span data-stu-id="db554-126">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="db554-127">Veiklos efektyvumo vertinimų spausdinimas</span><span class="sxs-lookup"><span data-stu-id="db554-127">Print performance reviews</span></span>

<span data-ttu-id="db554-128">Žr. [Veiklos efektyvumo vertinimų spausdinimas](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) dirbant su „Dynamics 365“: 2019 leidimo 2 bangos planu.</span><span class="sxs-lookup"><span data-stu-id="db554-128">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="db554-129">Funkcijos valdymo darbo sritis</span><span class="sxs-lookup"><span data-stu-id="db554-129">Feature management workspace</span></span>

<span data-ttu-id="db554-130">Funkcijos įtraukiamos ir atnaujinamos kiekviename leidime.</span><span class="sxs-lookup"><span data-stu-id="db554-130">Features are added and updated in every release.</span></span> <span data-ttu-id="db554-131">Funkcijų valdymo patirtis suteikia darbo sritį, kurioje galite peržiūrėti kiekviename leidime pristatytų funkcijų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="db554-131">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="db554-132">Pagal numatytuosius nustatymus naujos funkcijos yra išjungtos.</span><span class="sxs-lookup"><span data-stu-id="db554-132">By default, new features are turned off.</span></span> <span data-ttu-id="db554-133">Galite naudoti darbo sritį, norėdami jas įjungti ir peržiūrėti jų dokumentaciją.</span><span class="sxs-lookup"><span data-stu-id="db554-133">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="db554-134">Norėdami daugiau sužinoti apie pakeitimus, pristatytus su funkcijų valdymu, žr. [Funkcijų valdymo apžvalga](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="db554-134">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
