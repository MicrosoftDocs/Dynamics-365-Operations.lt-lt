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
ms.openlocfilehash: 01e8aa5157d0ad1c01f996886e7845e49ab97603
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464723"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="4e86c-103">Samdymo užklausos pareigų būsena</span><span class="sxs-lookup"><span data-stu-id="4e86c-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4e86c-104">Šioje temoje aprašoma samdymo užklausos pareigų būsenos parinktis nustatyta „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="4e86c-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="4e86c-105">Fizinis pavadinimas: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="4e86c-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="4e86c-106">Toks numeravimas suteikia parinktį nustatytą visų pareigų būsenos vertėms samdymo užklausai Samdymo užklausos pareigų objekte.</span><span class="sxs-lookup"><span data-stu-id="4e86c-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="4e86c-107">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="4e86c-107">Value</span></span> | <span data-ttu-id="4e86c-108">Žyma: </span><span class="sxs-lookup"><span data-stu-id="4e86c-108">Label</span></span> | <span data-ttu-id="4e86c-109">aprašymas</span><span class="sxs-lookup"><span data-stu-id="4e86c-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4e86c-110">200000000</span><span class="sxs-lookup"><span data-stu-id="4e86c-110">200000000</span></span> | <span data-ttu-id="4e86c-111">Atviri</span><span class="sxs-lookup"><span data-stu-id="4e86c-111">Open</span></span> | <span data-ttu-id="4e86c-112">Pareigos samdymo užklausoje yra atviros samdymui.</span><span class="sxs-lookup"><span data-stu-id="4e86c-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="4e86c-113">Tai nerodo, kad šiuo metu nėra jokio aktyvaus pareigų priskyrimo pareigoms.</span><span class="sxs-lookup"><span data-stu-id="4e86c-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="4e86c-114">Samdymo metu pareigose gali būti darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="4e86c-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="4e86c-115">Tai rodo tik tai, kad pareigos yra prieinamos samdymui samdymo užklausos kontekste.</span><span class="sxs-lookup"><span data-stu-id="4e86c-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="4e86c-116">200000001</span><span class="sxs-lookup"><span data-stu-id="4e86c-116">200000001</span></span> | <span data-ttu-id="4e86c-117">Užpildyta</span><span class="sxs-lookup"><span data-stu-id="4e86c-117">Filled</span></span> | <span data-ttu-id="4e86c-118">Darbuotojas buvo atrinktas pareigų priskyrimui.</span><span class="sxs-lookup"><span data-stu-id="4e86c-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="4e86c-119">200000002</span><span class="sxs-lookup"><span data-stu-id="4e86c-119">200000002</span></span> | <span data-ttu-id="4e86c-120">Atšaukti</span><span class="sxs-lookup"><span data-stu-id="4e86c-120">Canceled</span></span> | <span data-ttu-id="4e86c-121">Samdymo užklausa šioms pareigoms buvo atšaukta.</span><span class="sxs-lookup"><span data-stu-id="4e86c-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="4e86c-122">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="4e86c-122">See also</span></span>

[<span data-ttu-id="4e86c-123">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="4e86c-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="4e86c-124">Pavyzdinė užklausa Samdymo prašymui</span><span class="sxs-lookup"><span data-stu-id="4e86c-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]