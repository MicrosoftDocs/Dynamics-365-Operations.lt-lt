---
title: Užbaigimo būsena
description: Šioje temoje aprašoma užbaigimo būsenos parinktį nustatytą „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: d8ea90785f303301a21a4ac799578b08cabd0e3d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468208"
---
# <a name="completion-status"></a><span data-ttu-id="877fb-103">Užbaigimo būsena</span><span class="sxs-lookup"><span data-stu-id="877fb-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="877fb-104">Šioje temoje aprašoma užbaigimo būsenos parinktį nustatytą „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="877fb-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="877fb-105">Fizinis pavadinimas: mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="877fb-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="877fb-106">Toks numeravimas suteikia parinktį nustatytą būsenos vertėms pretendento atrankai.</span><span class="sxs-lookup"><span data-stu-id="877fb-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="877fb-107">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="877fb-107">Value</span></span> | <span data-ttu-id="877fb-108">Žyma: </span><span class="sxs-lookup"><span data-stu-id="877fb-108">Label</span></span> | <span data-ttu-id="877fb-109">aprašymas</span><span class="sxs-lookup"><span data-stu-id="877fb-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="877fb-110">200000000</span><span class="sxs-lookup"><span data-stu-id="877fb-110">200000000</span></span> | <span data-ttu-id="877fb-111">Nebaigtas</span><span class="sxs-lookup"><span data-stu-id="877fb-111">Not Complete</span></span> | <span data-ttu-id="877fb-112">Pretendentas dar neužbaigė atrankos.</span><span class="sxs-lookup"><span data-stu-id="877fb-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="877fb-113">200000001</span><span class="sxs-lookup"><span data-stu-id="877fb-113">200000001</span></span> | <span data-ttu-id="877fb-114">Praleisti</span><span class="sxs-lookup"><span data-stu-id="877fb-114">Pass</span></span> | <span data-ttu-id="877fb-115">Pretendentas dar užbaigė atranką.</span><span class="sxs-lookup"><span data-stu-id="877fb-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="877fb-116">200000002</span><span class="sxs-lookup"><span data-stu-id="877fb-116">200000002</span></span> | <span data-ttu-id="877fb-117">Triktis</span><span class="sxs-lookup"><span data-stu-id="877fb-117">Fail</span></span> | <span data-ttu-id="877fb-118">Pretendentas nepavyko atranka.</span><span class="sxs-lookup"><span data-stu-id="877fb-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="877fb-119">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="877fb-119">See also</span></span>

[<span data-ttu-id="877fb-120">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="877fb-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="877fb-121">Samdomo pretendento pavyzdžio užklausa</span><span class="sxs-lookup"><span data-stu-id="877fb-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]