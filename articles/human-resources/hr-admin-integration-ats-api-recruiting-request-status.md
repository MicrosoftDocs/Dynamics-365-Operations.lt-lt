---
title: Samdymo užklausos būsena
description: Šioje temoje aprašoma samdymo užklausos būsenos parinktis nustatyta „Dynamics 365 Human Resources“.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0032e6bfdbfd2792dafda8bf24a1b0cbc551740d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464651"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="45807-103">Samdymo užklausos būsena</span><span class="sxs-lookup"><span data-stu-id="45807-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="45807-104">Šioje temoje aprašoma samdymo užklausos būsenos parinktis nustatyta „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="45807-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="45807-105">Fizinis pavadinimas: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="45807-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="45807-106">Toks numeravimas suteikia parinktį nustatytą samdymo užklausos verčių būsenai.</span><span class="sxs-lookup"><span data-stu-id="45807-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="45807-107">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="45807-107">Value</span></span> | <span data-ttu-id="45807-108">Žyma: </span><span class="sxs-lookup"><span data-stu-id="45807-108">Label</span></span> | <span data-ttu-id="45807-109">aprašymas</span><span class="sxs-lookup"><span data-stu-id="45807-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="45807-110">200000000</span><span class="sxs-lookup"><span data-stu-id="45807-110">200000000</span></span> | <span data-ttu-id="45807-111">Juodraštis</span><span class="sxs-lookup"><span data-stu-id="45807-111">Draft</span></span> | <span data-ttu-id="45807-112">Užklausa yra šablonas ir nėra parengta įjungtam samdymui.</span><span class="sxs-lookup"><span data-stu-id="45807-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="45807-113">200000001</span><span class="sxs-lookup"><span data-stu-id="45807-113">200000001</span></span> | <span data-ttu-id="45807-114">Peržiūrima</span><span class="sxs-lookup"><span data-stu-id="45807-114">In Review</span></span> | <span data-ttu-id="45807-115">Užklausa buvo pateikta ir yra nukreipta darbo eigos patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="45807-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="45807-116">Prieinama tik įjungus darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="45807-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="45807-117">200000002</span><span class="sxs-lookup"><span data-stu-id="45807-117">200000002</span></span> | <span data-ttu-id="45807-118">Laukia</span><span class="sxs-lookup"><span data-stu-id="45807-118">Pending</span></span> | <span data-ttu-id="45807-119">Užklausa laukia darbo eigos veiksmo.</span><span class="sxs-lookup"><span data-stu-id="45807-119">The request is pending workflow action.</span></span> <span data-ttu-id="45807-120">Prieinama tik įjungus darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="45807-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="45807-121">200000003</span><span class="sxs-lookup"><span data-stu-id="45807-121">200000003</span></span> | <span data-ttu-id="45807-122">Atšaukti</span><span class="sxs-lookup"><span data-stu-id="45807-122">Canceled</span></span> | <span data-ttu-id="45807-123">Užklausa atšaukta.</span><span class="sxs-lookup"><span data-stu-id="45807-123">The request has been canceled.</span></span> <span data-ttu-id="45807-124">Prieinama tik įjungus darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="45807-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="45807-125">200000004</span><span class="sxs-lookup"><span data-stu-id="45807-125">200000004</span></span> | <span data-ttu-id="45807-126">Uždrausta</span><span class="sxs-lookup"><span data-stu-id="45807-126">Denied</span></span> | <span data-ttu-id="45807-127">Užklausa buvo atmesta.</span><span class="sxs-lookup"><span data-stu-id="45807-127">The request has been denied.</span></span> <span data-ttu-id="45807-128">Prieinama tik įjungus darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="45807-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="45807-129">200000005</span><span class="sxs-lookup"><span data-stu-id="45807-129">200000005</span></span> | <span data-ttu-id="45807-130">Aktyvios</span><span class="sxs-lookup"><span data-stu-id="45807-130">Active</span></span> | <span data-ttu-id="45807-131">Bet kuri darbo eiga yra užbaigta ir patvirtinta, o užklausa parengta įjungtam samdmymui.</span><span class="sxs-lookup"><span data-stu-id="45807-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="45807-132">200000006</span><span class="sxs-lookup"><span data-stu-id="45807-132">200000006</span></span> | <span data-ttu-id="45807-133">Uždaryta</span><span class="sxs-lookup"><span data-stu-id="45807-133">Closed</span></span> | <span data-ttu-id="45807-134">Samdymo užklausa yra užverta.</span><span class="sxs-lookup"><span data-stu-id="45807-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="45807-135">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="45807-135">See also</span></span>

[<span data-ttu-id="45807-136">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="45807-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="45807-137">Pavyzdinė užklausa Samdymo prašymui</span><span class="sxs-lookup"><span data-stu-id="45807-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]