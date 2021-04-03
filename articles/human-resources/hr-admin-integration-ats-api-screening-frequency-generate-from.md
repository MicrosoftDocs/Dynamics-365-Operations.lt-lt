---
title: Atrankos dažnumas sukuriamas pagal
description: Šioje temoje aprašoma atrankos dažnumo sukūrimą pagal parinktį nustatytą „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: 238cd5da750d815c904090cc9002e3d1a5d2bcc7
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464579"
---
# <a name="screening-frequency-generate-from"></a><span data-ttu-id="befff-103">Atrankos dažnumas sukuriamas pagal</span><span class="sxs-lookup"><span data-stu-id="befff-103">Screening frequency generate from</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="befff-104">Šioje temoje aprašoma atrankos dažnumo sukūrimą pagal parinktį nustatytą „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="befff-104">This topic describes the Screening frequency generate from option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="befff-105">Fizinis pavadinimas: mshr_hcmfrequencygeneratefrom</span><span class="sxs-lookup"><span data-stu-id="befff-105">Physical name: mshr_hcmfrequencygeneratefrom</span></span>

<span data-ttu-id="befff-106">Toks numeravimas suteikia parinktį nustatytą būsenos vertėms siekiant nustatyti skaičiavimo pradžios datą kitai būtinai atrankai.</span><span class="sxs-lookup"><span data-stu-id="befff-106">This enumeration provides the option set of values for determining the start date of the calculation for the next required screening.</span></span>

| <span data-ttu-id="befff-107">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="befff-107">Value</span></span> | <span data-ttu-id="befff-108">Žyma: </span><span class="sxs-lookup"><span data-stu-id="befff-108">Label</span></span> | <span data-ttu-id="befff-109">aprašymas</span><span class="sxs-lookup"><span data-stu-id="befff-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="befff-110">200000000 Nepasirinkta</span><span class="sxs-lookup"><span data-stu-id="befff-110">200000000 Not selected</span></span> | <span data-ttu-id="befff-111">Nebuvo parinkta jokios vertės.</span><span class="sxs-lookup"><span data-stu-id="befff-111">No value has been selected.</span></span> |
| <span data-ttu-id="befff-112">200000001 Duomenys užbaigti</span><span class="sxs-lookup"><span data-stu-id="befff-112">200000001 Date completed</span></span> | <span data-ttu-id="befff-113">Skaičiavimas atliekamas nuo paskutinės užbaigtos atrankos datos.</span><span class="sxs-lookup"><span data-stu-id="befff-113">Calculation is done from the last screening date completed.</span></span> |
| <span data-ttu-id="befff-114">200000002 Būtina data</span><span class="sxs-lookup"><span data-stu-id="befff-114">200000002 Date required</span></span> | <span data-ttu-id="befff-115">Skaičiavimas atliekamas nuo paskutinės būtinos atrankos datos.</span><span class="sxs-lookup"><span data-stu-id="befff-115">Calculation is done from the last screening date required.</span></span> |

## <a name="see-also"></a><span data-ttu-id="befff-116">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="befff-116">See also</span></span>

[<span data-ttu-id="befff-117">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="befff-117">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="befff-118">Samdomo pretendento pavyzdžio užklausa</span><span class="sxs-lookup"><span data-stu-id="befff-118">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]