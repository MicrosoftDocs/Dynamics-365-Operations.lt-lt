--- 
title: Gamybos eigos versijos galiojimo datos nustatymas
description: "Norėdami gamybos eigos versijos galiojimą ir apdorojimą nutraukti tam tikrą datą arba planuoti aktyvios versijos pakeitimą į naują versiją, turite nustatyti versijos galiojimo datą."
author: cvocph
manager: AnnBe
ms.date: 10/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6fabeb31720a60bf97d08dabf8ed87ac6af7cbf7
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="8ec9e-103">Gamybos eigos versijos galiojimo datos nustatymas</span><span class="sxs-lookup"><span data-stu-id="8ec9e-103">Define an expiry date for a production flow version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ec9e-104">Norėdami gamybos eigos versijos galiojimą ir apdorojimą nutraukti tam tikrą datą arba planuoti aktyvios versijos pakeitimą į naują versiją, turite nustatyti versijos galiojimo datą.</span><span class="sxs-lookup"><span data-stu-id="8ec9e-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="8ec9e-105">Šios versijos išjungti nebūtina.</span><span class="sxs-lookup"><span data-stu-id="8ec9e-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="8ec9e-106">Galiojimo datos nustatymas, kad būtų nutraukta gamybos eigos versija</span><span class="sxs-lookup"><span data-stu-id="8ec9e-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="8ec9e-107">Pasirinkite Gamybos kontrolė > Nustatymai > „Lean“ gamybos eiga > Gamybos eigos.</span><span class="sxs-lookup"><span data-stu-id="8ec9e-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="8ec9e-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="8ec9e-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8ec9e-109">Pasirinkite bet kokią gamybos eigą, kurios versija jau yra nustatyta.</span><span class="sxs-lookup"><span data-stu-id="8ec9e-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="8ec9e-110">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="8ec9e-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8ec9e-111">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="8ec9e-111">Click Edit.</span></span>
5. <span data-ttu-id="8ec9e-112">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="8ec9e-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="8ec9e-113">Lauke Galiojimo data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="8ec9e-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="8ec9e-114">Galiojimo datai pasibaigus, nauja versija nebus paleista arba įjungta.</span><span class="sxs-lookup"><span data-stu-id="8ec9e-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="8ec9e-115">Be to, nebebus galima kurti ar pradėti šios gamybos eigos užduočių.</span><span class="sxs-lookup"><span data-stu-id="8ec9e-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="8ec9e-116">Pasibaigus galiojimo datai, jūs vis tiek galėsite atlikti pradėtas užduotis.</span><span class="sxs-lookup"><span data-stu-id="8ec9e-116">You can still complete started jobs after the expiration date.</span></span>  


