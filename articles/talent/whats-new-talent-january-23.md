---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent – Core HR“ (2019 m. sausio 23 d.)
description: Šioje temoje aprašomos „Microsoft“ sistemos „Dynamics 365 Talent – Core HR“ naujos ir pakeistos funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
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
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 3c7a389ef4a651135836ce682d7cda95c536011a
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550210"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-23-2019"></a><span data-ttu-id="9345e-103">Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent – Core HR“ (2019 m. sausio 23 d.)</span><span class="sxs-lookup"><span data-stu-id="9345e-103">What's new or changed in Dynamics 365 Talent - Core HR (January 23, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9345e-104">**8.1.2121 versija**</span><span class="sxs-lookup"><span data-stu-id="9345e-104">**Build 8.1.2121**</span></span>

<span data-ttu-id="9345e-105">Šioje temoje aprašomos naujos ir pakeistos „Core HR“ funkcijos.</span><span class="sxs-lookup"><span data-stu-id="9345e-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="9345e-106">Pakeitimai</span><span class="sxs-lookup"><span data-stu-id="9345e-106">Changes</span></span>

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a><span data-ttu-id="9345e-107">Darbuotojo pastoviosios atlyginimo dalies importavimo funkcija neveikia kuriant naujus pastoviosios atlyginimo dalies įrašus</span><span class="sxs-lookup"><span data-stu-id="9345e-107">Import of employee fixed compensation not working when creating new fixed compensation records</span></span>
<span data-ttu-id="9345e-108">Pakeistas darbuotojo pastoviosios atlyginimo dalies objektas, kad kompensacijos lygis būtų nuskaitomas importuojant.</span><span class="sxs-lookup"><span data-stu-id="9345e-108">A change has been made to the employee fixed compensation entity to retrieve the compensation level upon import.</span></span> <span data-ttu-id="9345e-109">Prieš šį leidimą buvo rodomas pranešimas, nurodantis, koks lygis reikalingas.</span><span class="sxs-lookup"><span data-stu-id="9345e-109">Prior to this release, a message was displayed indicating that the level was required.</span></span>

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a><span data-ttu-id="9345e-110">Minimalaus balanso lauko pašalinimas iš atostogų užklausos dialogo lango</span><span class="sxs-lookup"><span data-stu-id="9345e-110">Remove the minimum balance field from the time off request dialog box</span></span>
<span data-ttu-id="9345e-111">Laukas **Minimalus balansas** pašalintas iš dialogo lango **Atostogų užklausa**.</span><span class="sxs-lookup"><span data-stu-id="9345e-111">The **Minimum balance** field has been removed from the **Time off request** dialog box.</span></span> <span data-ttu-id="9345e-112">Šis pakeitimas paveikia visas sritis, kuriose galima teikti atostogų užklausą.</span><span class="sxs-lookup"><span data-stu-id="9345e-112">This change affects all areas where time off can be requested.</span></span>

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a><span data-ttu-id="9345e-113">Kompensacijos lygio duomenų atnaujinimas nevykdomas visuose scenarijuose</span><span class="sxs-lookup"><span data-stu-id="9345e-113">Data upgrade for compensation levels not updating in all scenarios</span></span>
<span data-ttu-id="9345e-114">Atliktas pakeitimas siekiant atnaujinti kompensacijos lygį pastoviosios atlyginimo dalies planuose.</span><span class="sxs-lookup"><span data-stu-id="9345e-114">A change has been made to update the compensation level on fixed compensation plans.</span></span> <span data-ttu-id="9345e-115">Šis pakeitimas automatiškai užpildys pastoviosios atlyginimo dalies planų kompensacijos lygį užduotyse, kurios priskirtos darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="9345e-115">This change will populate the compensation level on fixed plans for the job assigned to the employee.</span></span>

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a><span data-ttu-id="9345e-116">Algalapio informacija puslapyje Pakeitimų valdymas galimas tik prisijungus sistemos administratoriaus teisėmis</span><span class="sxs-lookup"><span data-stu-id="9345e-116">Payroll information in the Manage changes page is only available when logged in as System Administrator</span></span>
<span data-ttu-id="9345e-117">Šis pakeitimas suteikia galimybę darbuotojams, kuriems priskirtas algalapio administratoriaus vaidmuo, pasiekti algalapio informaciją pareigų puslapyje pasirinkus **Pakeitimų laiko juosta > Valdyti pakeitimus**.</span><span class="sxs-lookup"><span data-stu-id="9345e-117">This change allows employees with the Payroll Administrator role access to the payroll information on the **Changes timeline > Manage changes** page for the position.</span></span>

### <a name="job-fields-default-to-positions"></a><span data-ttu-id="9345e-118">Pagal numatytuosius parametrus užduoties laukai nustatomi į pareigas</span><span class="sxs-lookup"><span data-stu-id="9345e-118">Job fields default to positions</span></span>
<span data-ttu-id="9345e-119">Keičiant užduotį pareigose, pagal numatytuosius parametrus užduoties laukai nustatomi į pareigas.</span><span class="sxs-lookup"><span data-stu-id="9345e-119">When changing the job on a position, job fields will default to the position.</span></span> <span data-ttu-id="9345e-120">Bus rodomas įspėjimo pranešimas, suteikiantis galimybę sutikti su numatytosiomis reikšmėmis arba palikti esamas tų laukų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="9345e-120">An alert message will appear giving an option to accept the default values or keep the existing values for those fields.</span></span>

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a><span data-ttu-id="9345e-121">Būsimų pasamdytų darbuotojų bandomasis laikotarpis ir kalendorius nerodomi.</span><span class="sxs-lookup"><span data-stu-id="9345e-121">Probation period and calendar are not displayed for future hired employees.</span></span>
<span data-ttu-id="9345e-122">Atlikus šį pakeitimą laukai **Bandomasis laikotarpis** ir **Kalendoriaus** buvo įtraukti į puslapį **Valdyti pakeitimus**, kad būtų galima įvesti buvusių ir būsimų darbuotojų duomenis.</span><span class="sxs-lookup"><span data-stu-id="9345e-122">With this change, **Probation period** and **Calendar** fields have been added to the **Manage changes** page to allow for data entry for future and past employees.</span></span>

### <a name="platform-update-23-for-finance-and-operations"></a><span data-ttu-id="9345e-123">„Finance and Operations“ platformos 23 naujinimas</span><span class="sxs-lookup"><span data-stu-id="9345e-123">Platform update 23 for Finance and Operations</span></span>
<span data-ttu-id="9345e-124">Nežymių klaidų pataisymai įtraukti kaip „Finance and Operations“ platformos 23 naujinimas.</span><span class="sxs-lookup"><span data-stu-id="9345e-124">Minor bug fixes have been included as part of Platform update 23 for Finance and Operations.</span></span> <span data-ttu-id="9345e-125">Daugiau informacijos žr. [Kas nauja arba pakeista „Dynamics 365 Finance and Operations“ 23 platformos naujinime (2019 m. sausio mėn.)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span><span class="sxs-lookup"><span data-stu-id="9345e-125">For more information, see [What's new or changed in Dynamics 365 Finance and Operations platform update 23 (January 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span></span> 
