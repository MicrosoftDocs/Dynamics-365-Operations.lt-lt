---
title: Atleidimo nuo darbo būsena
description: Šioje temoje aprašoma atleidimo nuo darbo būsenos parinktį nustatytą „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: 1f211002468384227acb2343ed6cbc6ae2a215d1
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464457"
---
# <a name="job-exempt-status"></a><span data-ttu-id="a436f-103">Atleidimo nuo darbo būsena</span><span class="sxs-lookup"><span data-stu-id="a436f-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a436f-104">Šioje temoje aprašoma atleidimo nuo darbo būsenos parinktį nustatytą „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="a436f-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="a436f-105">Fizinis pavadinimas: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="a436f-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="a436f-106">Numeravimo nurodo parinktį nustatytą FLSA atleidimo nuo darbo būsenos vertėms.</span><span class="sxs-lookup"><span data-stu-id="a436f-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="a436f-107">Jis patiektas esančiam cdm_jobexemptstatus parinkties rinkiniui.</span><span class="sxs-lookup"><span data-stu-id="a436f-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="a436f-108">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="a436f-108">Value</span></span> | <span data-ttu-id="a436f-109">Žyma: </span><span class="sxs-lookup"><span data-stu-id="a436f-109">Label</span></span> | <span data-ttu-id="a436f-110">aprašymas</span><span class="sxs-lookup"><span data-stu-id="a436f-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a436f-111">200000000</span><span class="sxs-lookup"><span data-stu-id="a436f-111">200000000</span></span> | <span data-ttu-id="a436f-112">Neapmokestinama</span><span class="sxs-lookup"><span data-stu-id="a436f-112">Exempt</span></span> | <span data-ttu-id="a436f-113">Nuo darbo atleidimo būsena paremta FLSA gairėmis.</span><span class="sxs-lookup"><span data-stu-id="a436f-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="a436f-114">200000001</span><span class="sxs-lookup"><span data-stu-id="a436f-114">200000001</span></span> | <span data-ttu-id="a436f-115">Neatleistas</span><span class="sxs-lookup"><span data-stu-id="a436f-115">NonExempt</span></span> | <span data-ttu-id="a436f-116">Darbas turi neatleidimo būseną paremtą FLSA gairėmis.</span><span class="sxs-lookup"><span data-stu-id="a436f-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="a436f-117">200000002</span><span class="sxs-lookup"><span data-stu-id="a436f-117">200000002</span></span> | <span data-ttu-id="a436f-118">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="a436f-118">Does Not Apply</span></span> | <span data-ttu-id="a436f-119">FLSA būsenos gairės netaikomos darbui.</span><span class="sxs-lookup"><span data-stu-id="a436f-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="a436f-120">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="a436f-120">See also</span></span>

[<span data-ttu-id="a436f-121">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="a436f-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="a436f-122">Pavyzdinė užklausa Samdymo prašymui</span><span class="sxs-lookup"><span data-stu-id="a436f-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]