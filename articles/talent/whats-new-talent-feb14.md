---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent“ (2019 m. vasario 14 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5f96dd60652705de820e0661d417dcaee8143561
ms.sourcegitcommit: 5384200c3e33510c5b3ac31f2b22443e1076251f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/14/2019
ms.locfileid: "390674"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a><span data-ttu-id="e4dfc-103">Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent“ (2019 m. vasario 14 d.)</span><span class="sxs-lookup"><span data-stu-id="e4dfc-103">What's new or changed in Dynamics 365 for Talent (February 14, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e4dfc-104">Šioje temoje aprašomos naujos ir pakeistos „Talent“ funkcijos.</span><span class="sxs-lookup"><span data-stu-id="e4dfc-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="e4dfc-105">„Attract“ pakeitimai</span><span class="sxs-lookup"><span data-stu-id="e4dfc-105">Changes in Attract</span></span>
<span data-ttu-id="e4dfc-106">Į šį leidimą įtraukta nedidelių pataisų.</span><span class="sxs-lookup"><span data-stu-id="e4dfc-106">There are minor bug fixes included with this release.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="e4dfc-107">Supažindinimo pakeitimai</span><span class="sxs-lookup"><span data-stu-id="e4dfc-107">Changes in Onboarding</span></span>
<span data-ttu-id="e4dfc-108">Į šį leidimą įtraukta nedidelių pataisų.</span><span class="sxs-lookup"><span data-stu-id="e4dfc-108">There are minor bug fixes included with this release.</span></span>
 
## <a name="changes-in-core-hr"></a><span data-ttu-id="e4dfc-109">„Core HR“ pakeitimai</span><span class="sxs-lookup"><span data-stu-id="e4dfc-109">Changes in Core HR</span></span> 
<span data-ttu-id="e4dfc-110">**8.1.2146 versija**</span><span class="sxs-lookup"><span data-stu-id="e4dfc-110">**Build 8.1.2146**</span></span>

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a><span data-ttu-id="e4dfc-111">Darbuotojo pastoviosios atlyginimo dalies objekto negalima eksportuoti į visus įrašus</span><span class="sxs-lookup"><span data-stu-id="e4dfc-111">Employee fixed compensation entity doesn't export all records</span></span>
<span data-ttu-id="e4dfc-112">Atlikus šį pakeitimą, objektas **Darbuotojo pastovioji atlyginimo dalis** galės eksportuoti visus įrašus.</span><span class="sxs-lookup"><span data-stu-id="e4dfc-112">With this change, the **Employee fixed compensation** entity will now export all records.</span></span> <span data-ttu-id="e4dfc-113">Objektą galima naudoti norint sukurti ir atnaujinti esamus darbuotojų pastoviųjų atlyginimo dalių įrašus.</span><span class="sxs-lookup"><span data-stu-id="e4dfc-113">The entity can be used to create and update existing fixed compensation records for employees.</span></span> 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a><span data-ttu-id="e4dfc-114">Įdarbinimo pabaigos data nustatoma neatsižvelgiant į darbuotojo pageidaujamos laiko juostos parametrus</span><span class="sxs-lookup"><span data-stu-id="e4dfc-114">Employment end date doesn't honor employee preferred time zone settings</span></span>
<span data-ttu-id="e4dfc-115">Įdarbinimo pabaigos datos dabar nustatomos atsižvelgiant į vartotojo pageidaujamą laiko juostą, kai įmonėje kuriamas arba baigiamas įdarbinimo procesas.</span><span class="sxs-lookup"><span data-stu-id="e4dfc-115">Employment end dates are now honoring the user-preferred time zone when creating or ending employment with a company.</span></span>
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a><span data-ttu-id="e4dfc-116">JK adresai „Analytics“ rodomi kaip Rytų Šveicarijos adresai</span><span class="sxs-lookup"><span data-stu-id="e4dfc-116">UK addresses display in Analytics as Eastern Switzerland addresses</span></span>
<span data-ttu-id="e4dfc-117">Šiame leidime atliktas pakeitimas, kuriuo ištaisyti adresų nesutapimai **personalo valdymo** ataskaitoje Darbuotojų skaičiaus pagal vietą.</span><span class="sxs-lookup"><span data-stu-id="e4dfc-117">In this release, a change has been made to correct misalignment in addresses in the **Personnel Management** "Headcount by location" report.</span></span>
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a><span data-ttu-id="e4dfc-118">Atleidimo kodas neužpildomas darbuotojo pareigų priskyrimo įraše, kai pareigų ėjimas nutraukiamas</span><span class="sxs-lookup"><span data-stu-id="e4dfc-118">Termination code is not populated on the worker position assignment record when ending the position</span></span>
<span data-ttu-id="e4dfc-119">Kai nutraukiamas darbuotojų pareigų priskyrimas, nustatomas numatytasis kodas Atleidimo priežastis.</span><span class="sxs-lookup"><span data-stu-id="e4dfc-119">A change has been made to default the "Termination reason" code when ending the employees position assignment.</span></span>

### <a name="new-entity-created-for-job-compensation-levels"></a><span data-ttu-id="e4dfc-120">Sukuriamas naujas objektas, skirtas užduoties kompensacijų lygiams</span><span class="sxs-lookup"><span data-stu-id="e4dfc-120">New entity created for job compensation levels</span></span>
<span data-ttu-id="e4dfc-121">Sukurtas naujas duomenų valdymo sistemos (DMF) objektas.</span><span class="sxs-lookup"><span data-stu-id="e4dfc-121">A new data management framework (DMF) entity was created.</span></span> <span data-ttu-id="e4dfc-122">Objektas suteikia galimybę kurti ir naujinti kiekvienos sistemoje nurodytos užduoties kompensacijų lygius, rinkos vertes ir apklausų informaciją.</span><span class="sxs-lookup"><span data-stu-id="e4dfc-122">The entity provides for creation and updates to compensation levels, market values, and survey information for each job defined in the system.</span></span>
