---
title: Samdymo užklausos pareigų būsena
description: Šioje temoje aprašoma samdymo užklausos pareigų būsenos parinktis nustatyta „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: 3f7bae64f58f0bdc1603b3c1b5493f1ebcfa8de9
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126055"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="4ff01-103">Samdymo užklausos pareigų būsena</span><span class="sxs-lookup"><span data-stu-id="4ff01-103">Recruiting request position status</span></span>

<span data-ttu-id="4ff01-104">Šioje temoje aprašoma samdymo užklausos pareigų būsenos parinktis nustatyta „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="4ff01-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="4ff01-105">Fizinis pavadinimas: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="4ff01-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="4ff01-106">Toks numeravimas suteikia parinktį nustatytą visų pareigų būsenos vertėms samdymo užklausai Samdymo užklausos pareigų objekte.</span><span class="sxs-lookup"><span data-stu-id="4ff01-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="4ff01-107">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="4ff01-107">Value</span></span> | <span data-ttu-id="4ff01-108">Žyma: </span><span class="sxs-lookup"><span data-stu-id="4ff01-108">Label</span></span> | <span data-ttu-id="4ff01-109">aprašymas</span><span class="sxs-lookup"><span data-stu-id="4ff01-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4ff01-110">200000000</span><span class="sxs-lookup"><span data-stu-id="4ff01-110">200000000</span></span> | <span data-ttu-id="4ff01-111">Atviri</span><span class="sxs-lookup"><span data-stu-id="4ff01-111">Open</span></span> | <span data-ttu-id="4ff01-112">Pareigos samdymo užklausoje yra atviros samdymui.</span><span class="sxs-lookup"><span data-stu-id="4ff01-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="4ff01-113">Tai nerodo, kad šiuo metu nėra jokio aktyvaus pareigų priskyrimo pareigoms.</span><span class="sxs-lookup"><span data-stu-id="4ff01-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="4ff01-114">Samdymo metu pareigose gali būti darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="4ff01-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="4ff01-115">Tai rodo tik tai, kad pareigos yra prieinamos samdymui samdymo užklausos kontekste.</span><span class="sxs-lookup"><span data-stu-id="4ff01-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="4ff01-116">200000001</span><span class="sxs-lookup"><span data-stu-id="4ff01-116">200000001</span></span> | <span data-ttu-id="4ff01-117">Užpildyta</span><span class="sxs-lookup"><span data-stu-id="4ff01-117">Filled</span></span> | <span data-ttu-id="4ff01-118">Darbuotojas buvo atrinktas pareigų priskyrimui.</span><span class="sxs-lookup"><span data-stu-id="4ff01-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="4ff01-119">200000002</span><span class="sxs-lookup"><span data-stu-id="4ff01-119">200000002</span></span> | <span data-ttu-id="4ff01-120">Atšaukti</span><span class="sxs-lookup"><span data-stu-id="4ff01-120">Canceled</span></span> | <span data-ttu-id="4ff01-121">Samdymo užklausa šioms pareigoms buvo atšaukta.</span><span class="sxs-lookup"><span data-stu-id="4ff01-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="4ff01-122">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="4ff01-122">See also</span></span>

[<span data-ttu-id="4ff01-123">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="4ff01-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="4ff01-124">Pavyzdinė užklausa Samdymo prašymui</span><span class="sxs-lookup"><span data-stu-id="4ff01-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
