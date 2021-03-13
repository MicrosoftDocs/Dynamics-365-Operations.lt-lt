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
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125959"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="83532-103">Samdymo užklausos būsena</span><span class="sxs-lookup"><span data-stu-id="83532-103">Recruiting request status</span></span>

<span data-ttu-id="83532-104">Šioje temoje aprašoma samdymo užklausos būsenos parinktis nustatyta „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="83532-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="83532-105">Fizinis pavadinimas: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="83532-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="83532-106">Toks numeravimas suteikia parinktį nustatytą samdymo užklausos verčių būsenai.</span><span class="sxs-lookup"><span data-stu-id="83532-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="83532-107">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="83532-107">Value</span></span> | <span data-ttu-id="83532-108">Žyma: </span><span class="sxs-lookup"><span data-stu-id="83532-108">Label</span></span> | <span data-ttu-id="83532-109">aprašymas</span><span class="sxs-lookup"><span data-stu-id="83532-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="83532-110">200000000</span><span class="sxs-lookup"><span data-stu-id="83532-110">200000000</span></span> | <span data-ttu-id="83532-111">Juodraštis</span><span class="sxs-lookup"><span data-stu-id="83532-111">Draft</span></span> | <span data-ttu-id="83532-112">Užklausa yra šablonas ir nėra parengta įjungtam samdymui.</span><span class="sxs-lookup"><span data-stu-id="83532-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="83532-113">200000001</span><span class="sxs-lookup"><span data-stu-id="83532-113">200000001</span></span> | <span data-ttu-id="83532-114">Peržiūrima</span><span class="sxs-lookup"><span data-stu-id="83532-114">In Review</span></span> | <span data-ttu-id="83532-115">Užklausa buvo pateikta ir yra nukreipta darbo eigos patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="83532-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="83532-116">Prieinama tik įjungus darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="83532-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="83532-117">200000002</span><span class="sxs-lookup"><span data-stu-id="83532-117">200000002</span></span> | <span data-ttu-id="83532-118">Laukia</span><span class="sxs-lookup"><span data-stu-id="83532-118">Pending</span></span> | <span data-ttu-id="83532-119">Užklausa laukia darbo eigos veiksmo.</span><span class="sxs-lookup"><span data-stu-id="83532-119">The request is pending workflow action.</span></span> <span data-ttu-id="83532-120">Prieinama tik įjungus darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="83532-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="83532-121">200000003</span><span class="sxs-lookup"><span data-stu-id="83532-121">200000003</span></span> | <span data-ttu-id="83532-122">Atšaukti</span><span class="sxs-lookup"><span data-stu-id="83532-122">Canceled</span></span> | <span data-ttu-id="83532-123">Užklausa atšaukta.</span><span class="sxs-lookup"><span data-stu-id="83532-123">The request has been canceled.</span></span> <span data-ttu-id="83532-124">Prieinama tik įjungus darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="83532-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="83532-125">200000004</span><span class="sxs-lookup"><span data-stu-id="83532-125">200000004</span></span> | <span data-ttu-id="83532-126">Uždrausta</span><span class="sxs-lookup"><span data-stu-id="83532-126">Denied</span></span> | <span data-ttu-id="83532-127">Užklausa buvo atmesta.</span><span class="sxs-lookup"><span data-stu-id="83532-127">The request has been denied.</span></span> <span data-ttu-id="83532-128">Prieinama tik įjungus darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="83532-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="83532-129">200000005</span><span class="sxs-lookup"><span data-stu-id="83532-129">200000005</span></span> | <span data-ttu-id="83532-130">Aktyvios</span><span class="sxs-lookup"><span data-stu-id="83532-130">Active</span></span> | <span data-ttu-id="83532-131">Bet kuri darbo eiga yra užbaigta ir patvirtinta, o užklausa parengta įjungtam samdmymui.</span><span class="sxs-lookup"><span data-stu-id="83532-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="83532-132">200000006</span><span class="sxs-lookup"><span data-stu-id="83532-132">200000006</span></span> | <span data-ttu-id="83532-133">Uždaryta</span><span class="sxs-lookup"><span data-stu-id="83532-133">Closed</span></span> | <span data-ttu-id="83532-134">Samdymo užklausa yra užverta.</span><span class="sxs-lookup"><span data-stu-id="83532-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="83532-135">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="83532-135">See also</span></span>

[<span data-ttu-id="83532-136">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="83532-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="83532-137">Pavyzdinė užklausa Samdymo prašymui</span><span class="sxs-lookup"><span data-stu-id="83532-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
