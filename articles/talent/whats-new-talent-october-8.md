---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent – Core HR“ (2018 m. spalio 8 d.)
description: Šioje temoje aprašomos „Microsoft“ sistemos „Dynamics 365 Talent – Core HR“ naujos ir pakeistos funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 330ffebf73c8948a1bbab2ee57acba7b97a93b6f
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008878"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-8-2018"></a><span data-ttu-id="3e2b4-103">Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent – Core HR“ (2018 m. spalio 8 d.)</span><span class="sxs-lookup"><span data-stu-id="3e2b4-103">What's new or changed in Dynamics 365 Talent - Core HR (October 8, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3e2b4-104">**8.1.1050.0 versija**</span><span class="sxs-lookup"><span data-stu-id="3e2b4-104">**Build 8.1.1050.0**</span></span>

<span data-ttu-id="3e2b4-105">Šioje temoje aprašomos naujos ir pakeistos „Core HR“ funkcijos.</span><span class="sxs-lookup"><span data-stu-id="3e2b4-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a><span data-ttu-id="3e2b4-106">Atostogų pakopos pagrindui (atostogų valdymas) leidžiama naudoti kitas datas</span><span class="sxs-lookup"><span data-stu-id="3e2b4-106">Allow other dates to be used on leave tier basis (Leave Management)</span></span>

<span data-ttu-id="3e2b4-107">Skiriant darbuotojams atostogų premijas, premijų pakopos pagrindas nurodo, kiek ne darbo laiko darbuotojas sukaupia.</span><span class="sxs-lookup"><span data-stu-id="3e2b4-107">When awarding leave to employees, the award tier basis determines how much time off an employee accrues.</span></span> <span data-ttu-id="3e2b4-108">Dabar šios pakopos grindžiamos darbuotojo darbo pradžios data ir paaukštinimo data.</span><span class="sxs-lookup"><span data-stu-id="3e2b4-108">Currently, these tiers are based on employee start date and seniority date.</span></span> <span data-ttu-id="3e2b4-109">Taikydamos tam tikrus scenarijus organizacijos šias pakopas turi grįsti kitomis datomis, pvz., jubiliejaus data arba pradinio įdarbinimo data.</span><span class="sxs-lookup"><span data-stu-id="3e2b4-109">In some scenarios, organizations need these tiers to be based on other dates, like anniversary date or original hire date.</span></span> <span data-ttu-id="3e2b4-110">Šios datos jau yra naudojamos atostogų plane siekiant nustatyti, kada vykdomas kaupimas. Įtraukėme galimybę, kai darbuotojas yra užregistruotas plane, tas pačias datas panaudoti siekiant nustatyti sukauptą kiekį.</span><span class="sxs-lookup"><span data-stu-id="3e2b4-110">These dates are already used on the leave plan to determine when accruals happen, the ability for these same dates to be used when an employee is enrolled in a plan have been added to determine the accrual amount.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="3e2b4-111">Kiti pakeitimai</span><span class="sxs-lookup"><span data-stu-id="3e2b4-111">Other changes</span></span>
<span data-ttu-id="3e2b4-112">Šiame leidime pateikiamos įvairios pataisos.</span><span class="sxs-lookup"><span data-stu-id="3e2b4-112">Miscellanous fixes have been included in this release.</span></span>

## <a name="known-issue"></a><span data-ttu-id="3e2b4-113">Žinoma problema</span><span class="sxs-lookup"><span data-stu-id="3e2b4-113">Known issue</span></span>

<span data-ttu-id="3e2b4-114">**Problema:** pridedant naują priedą prie darbininko, mygtukai **Naujas** ir **Redaguoti** yra pateikiami pilka spalva. **Problemos sprendimas:** prieš atidarydami priedo puslapį įsitikinkite, kad „FactBoxes“ laukai puslapyje **Darbininkas** yra uždaryti.</span><span class="sxs-lookup"><span data-stu-id="3e2b4-114">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="3e2b4-115">Jei „FactBoxes“ laukai yra uždaryti, įkeliant puslapį **Darbininkas** priedų mygtukai bus įjungti.</span><span class="sxs-lookup"><span data-stu-id="3e2b4-115">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="3e2b4-116">(Ši problema bus pašalinta kitame platformos naujinime.)</span><span class="sxs-lookup"><span data-stu-id="3e2b4-116">(This issue will be fixed in the next platform update.)</span></span>
