---
title: Atrankos dažnumas sukuriamas pagal
description: Šioje temoje aprašoma atrankos dažnumo sukūrimą pagal parinktį nustatytą „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: ae5ad3e556f40cedd385d8aadded9ef76447a98b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054097"
---
# <a name="screening-frequency-generate-from"></a><span data-ttu-id="96ec9-103">Atrankos dažnumas sukuriamas pagal</span><span class="sxs-lookup"><span data-stu-id="96ec9-103">Screening frequency generate from</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="96ec9-104">Šioje temoje aprašoma atrankos dažnumo sukūrimą pagal parinktį nustatytą „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="96ec9-104">This topic describes the Screening frequency generate from option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="96ec9-105">Fizinis pavadinimas: mshr_hcmfrequencygeneratefrom</span><span class="sxs-lookup"><span data-stu-id="96ec9-105">Physical name: mshr_hcmfrequencygeneratefrom</span></span>

<span data-ttu-id="96ec9-106">Toks numeravimas suteikia parinktį nustatytą būsenos vertėms siekiant nustatyti skaičiavimo pradžios datą kitai būtinai atrankai.</span><span class="sxs-lookup"><span data-stu-id="96ec9-106">This enumeration provides the option set of values for determining the start date of the calculation for the next required screening.</span></span>

| <span data-ttu-id="96ec9-107">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="96ec9-107">Value</span></span> | <span data-ttu-id="96ec9-108">Žyma</span><span class="sxs-lookup"><span data-stu-id="96ec9-108">Label</span></span> | <span data-ttu-id="96ec9-109">Aprašas</span><span class="sxs-lookup"><span data-stu-id="96ec9-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="96ec9-110">200000000 Nepasirinkta</span><span class="sxs-lookup"><span data-stu-id="96ec9-110">200000000 Not selected</span></span> | <span data-ttu-id="96ec9-111">Nebuvo parinkta jokios vertės.</span><span class="sxs-lookup"><span data-stu-id="96ec9-111">No value has been selected.</span></span> |
| <span data-ttu-id="96ec9-112">200000001 Duomenys užbaigti</span><span class="sxs-lookup"><span data-stu-id="96ec9-112">200000001 Date completed</span></span> | <span data-ttu-id="96ec9-113">Skaičiavimas atliekamas nuo paskutinės užbaigtos atrankos datos.</span><span class="sxs-lookup"><span data-stu-id="96ec9-113">Calculation is done from the last screening date completed.</span></span> |
| <span data-ttu-id="96ec9-114">200000002 Būtina data</span><span class="sxs-lookup"><span data-stu-id="96ec9-114">200000002 Date required</span></span> | <span data-ttu-id="96ec9-115">Skaičiavimas atliekamas nuo paskutinės būtinos atrankos datos.</span><span class="sxs-lookup"><span data-stu-id="96ec9-115">Calculation is done from the last screening date required.</span></span> |

## <a name="see-also"></a><span data-ttu-id="96ec9-116">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="96ec9-116">See also</span></span>

[<span data-ttu-id="96ec9-117">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="96ec9-117">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="96ec9-118">Samdomo pretendento pavyzdžio užklausa</span><span class="sxs-lookup"><span data-stu-id="96ec9-118">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]