---
title: Atleidimo nuo darbo būsena
description: Šioje temoje aprašoma atleidimo nuo darbo būsenos parinktį nustatytą „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: 8e91fbb420009d5131e2faa7dbea8a302a027e0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053856"
---
# <a name="job-exempt-status"></a><span data-ttu-id="1dc78-103">Atleidimo nuo darbo būsena</span><span class="sxs-lookup"><span data-stu-id="1dc78-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1dc78-104">Šioje temoje aprašoma atleidimo nuo darbo būsenos parinktį nustatytą „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="1dc78-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="1dc78-105">Fizinis pavadinimas: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="1dc78-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="1dc78-106">Numeravimo nurodo parinktį nustatytą FLSA atleidimo nuo darbo būsenos vertėms.</span><span class="sxs-lookup"><span data-stu-id="1dc78-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="1dc78-107">Jis patiektas esančiam cdm_jobexemptstatus parinkties rinkiniui.</span><span class="sxs-lookup"><span data-stu-id="1dc78-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="1dc78-108">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="1dc78-108">Value</span></span> | <span data-ttu-id="1dc78-109">Žyma</span><span class="sxs-lookup"><span data-stu-id="1dc78-109">Label</span></span> | <span data-ttu-id="1dc78-110">Aprašas</span><span class="sxs-lookup"><span data-stu-id="1dc78-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="1dc78-111">200000000</span><span class="sxs-lookup"><span data-stu-id="1dc78-111">200000000</span></span> | <span data-ttu-id="1dc78-112">Neapmokestinama</span><span class="sxs-lookup"><span data-stu-id="1dc78-112">Exempt</span></span> | <span data-ttu-id="1dc78-113">Nuo darbo atleidimo būsena paremta FLSA gairėmis.</span><span class="sxs-lookup"><span data-stu-id="1dc78-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="1dc78-114">200000001</span><span class="sxs-lookup"><span data-stu-id="1dc78-114">200000001</span></span> | <span data-ttu-id="1dc78-115">Neatleistas</span><span class="sxs-lookup"><span data-stu-id="1dc78-115">NonExempt</span></span> | <span data-ttu-id="1dc78-116">Darbas turi neatleidimo būseną paremtą FLSA gairėmis.</span><span class="sxs-lookup"><span data-stu-id="1dc78-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="1dc78-117">200000002</span><span class="sxs-lookup"><span data-stu-id="1dc78-117">200000002</span></span> | <span data-ttu-id="1dc78-118">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="1dc78-118">Does Not Apply</span></span> | <span data-ttu-id="1dc78-119">FLSA būsenos gairės netaikomos darbui.</span><span class="sxs-lookup"><span data-stu-id="1dc78-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="1dc78-120">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="1dc78-120">See also</span></span>

[<span data-ttu-id="1dc78-121">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="1dc78-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="1dc78-122">Pavyzdinė užklausa Samdymo prašymui</span><span class="sxs-lookup"><span data-stu-id="1dc78-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]