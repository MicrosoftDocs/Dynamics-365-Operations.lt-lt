---
title: Samdymo užklausos būsena
description: Šioje temoje aprašoma samdymo užklausos būsenos parinktis nustatyta „Dynamics 365 Human Resources“.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3b05cc531a84144708ff52913927bbd04574a3b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059189"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="bf538-103">Samdymo užklausos būsena</span><span class="sxs-lookup"><span data-stu-id="bf538-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bf538-104">Šioje temoje aprašoma samdymo užklausos būsenos parinktis nustatyta „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="bf538-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="bf538-105">Fizinis pavadinimas: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="bf538-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="bf538-106">Toks numeravimas suteikia parinktį nustatytą samdymo užklausos verčių būsenai.</span><span class="sxs-lookup"><span data-stu-id="bf538-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="bf538-107">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="bf538-107">Value</span></span> | <span data-ttu-id="bf538-108">Žyma</span><span class="sxs-lookup"><span data-stu-id="bf538-108">Label</span></span> | <span data-ttu-id="bf538-109">Aprašas</span><span class="sxs-lookup"><span data-stu-id="bf538-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="bf538-110">200000000</span><span class="sxs-lookup"><span data-stu-id="bf538-110">200000000</span></span> | <span data-ttu-id="bf538-111">Juodraštis</span><span class="sxs-lookup"><span data-stu-id="bf538-111">Draft</span></span> | <span data-ttu-id="bf538-112">Užklausa yra šablonas ir nėra parengta įjungtam samdymui.</span><span class="sxs-lookup"><span data-stu-id="bf538-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="bf538-113">200000001</span><span class="sxs-lookup"><span data-stu-id="bf538-113">200000001</span></span> | <span data-ttu-id="bf538-114">Peržiūrima</span><span class="sxs-lookup"><span data-stu-id="bf538-114">In Review</span></span> | <span data-ttu-id="bf538-115">Užklausa buvo pateikta ir yra nukreipta darbo eigos patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="bf538-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="bf538-116">Prieinama tik įjungus darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="bf538-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="bf538-117">200000002</span><span class="sxs-lookup"><span data-stu-id="bf538-117">200000002</span></span> | <span data-ttu-id="bf538-118">Laukia</span><span class="sxs-lookup"><span data-stu-id="bf538-118">Pending</span></span> | <span data-ttu-id="bf538-119">Užklausa laukia darbo eigos veiksmo.</span><span class="sxs-lookup"><span data-stu-id="bf538-119">The request is pending workflow action.</span></span> <span data-ttu-id="bf538-120">Prieinama tik įjungus darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="bf538-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="bf538-121">200000003</span><span class="sxs-lookup"><span data-stu-id="bf538-121">200000003</span></span> | <span data-ttu-id="bf538-122">Atšaukti</span><span class="sxs-lookup"><span data-stu-id="bf538-122">Canceled</span></span> | <span data-ttu-id="bf538-123">Užklausa atšaukta.</span><span class="sxs-lookup"><span data-stu-id="bf538-123">The request has been canceled.</span></span> <span data-ttu-id="bf538-124">Prieinama tik įjungus darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="bf538-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="bf538-125">200000004</span><span class="sxs-lookup"><span data-stu-id="bf538-125">200000004</span></span> | <span data-ttu-id="bf538-126">Uždrausta</span><span class="sxs-lookup"><span data-stu-id="bf538-126">Denied</span></span> | <span data-ttu-id="bf538-127">Užklausa buvo atmesta.</span><span class="sxs-lookup"><span data-stu-id="bf538-127">The request has been denied.</span></span> <span data-ttu-id="bf538-128">Prieinama tik įjungus darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="bf538-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="bf538-129">200000005</span><span class="sxs-lookup"><span data-stu-id="bf538-129">200000005</span></span> | <span data-ttu-id="bf538-130">Aktyvios</span><span class="sxs-lookup"><span data-stu-id="bf538-130">Active</span></span> | <span data-ttu-id="bf538-131">Bet kuri darbo eiga yra užbaigta ir patvirtinta, o užklausa parengta įjungtam samdmymui.</span><span class="sxs-lookup"><span data-stu-id="bf538-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="bf538-132">200000006</span><span class="sxs-lookup"><span data-stu-id="bf538-132">200000006</span></span> | <span data-ttu-id="bf538-133">Uždaryta</span><span class="sxs-lookup"><span data-stu-id="bf538-133">Closed</span></span> | <span data-ttu-id="bf538-134">Samdymo užklausa yra užverta.</span><span class="sxs-lookup"><span data-stu-id="bf538-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="bf538-135">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="bf538-135">See also</span></span>

[<span data-ttu-id="bf538-136">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="bf538-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="bf538-137">Pavyzdinė užklausa Samdymo prašymui</span><span class="sxs-lookup"><span data-stu-id="bf538-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]