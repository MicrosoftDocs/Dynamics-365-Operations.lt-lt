---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. sausio 31 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
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
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fbbecd4e0f205c2f09ec30548756ff1a43872644
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899110"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a><span data-ttu-id="3a6b6-103">Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. sausio 31 d.)</span><span class="sxs-lookup"><span data-stu-id="3a6b6-103">What's new or changed in Dynamics 365 Talent (January 31, 2019)</span></span>

<span data-ttu-id="3a6b6-104">Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 Talent“ funkcijos.</span><span class="sxs-lookup"><span data-stu-id="3a6b6-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

<span data-ttu-id="3a6b6-105">**8.1.2128 versija**</span><span class="sxs-lookup"><span data-stu-id="3a6b6-105">**Build 8.1.2128**</span></span>

## <a name="core-hr-changes"></a><span data-ttu-id="3a6b6-106">„Core HR“ pakeitimai</span><span class="sxs-lookup"><span data-stu-id="3a6b6-106">Core HR Changes</span></span>

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a><span data-ttu-id="3a6b6-107">Nurodant atostogų laiką atostogaujančių žmonių kortelėje neatsižvelgiama į atostogų plano datas</span><span class="sxs-lookup"><span data-stu-id="3a6b6-107">Time off taken on leave people card doesn't consider leave plan dates</span></span>
<span data-ttu-id="3a6b6-108">Tiems, kurių atostogų planai nesudaromi pagal kalendorinius metus, kortelė **Užimta** dabar rodo užimtą laiką planu apibrėžtuose atostogų metuose.</span><span class="sxs-lookup"><span data-stu-id="3a6b6-108">For those that have leave plans that don’t run on a calendar year, the **Taken** card now displays time off that’s been taken in the plan-defined leave year.</span></span> <span data-ttu-id="3a6b6-109">Pavyzdžiui, jei organizacijos atostogų metai yra nuo birželio 1 d. iki gegužės 30 d. ir darbuotojas atostogavo 3 dienas gruodžio mėn., kortelė **Užimta** sausio 15 d. rodys 3 dienas.</span><span class="sxs-lookup"><span data-stu-id="3a6b6-109">For example, if an organization’s leave year is June 1 through May 30 and an employee has taken 3 days off in December, the **Taken** card on January 15, will display 3 days.</span></span> 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a><span data-ttu-id="3a6b6-110">Kaupimo sumos nesutampa su pakopos datos pagrindu</span><span class="sxs-lookup"><span data-stu-id="3a6b6-110">Accrual amounts not matching tier date basis</span></span>
<span data-ttu-id="3a6b6-111">Naujos parinktys įtrauktos į atostogų ir neatvykimo nustatymus (**personalo** parametrus), kad klientai galėtų nustatyti, kada darbuotojų aptarnavimo datų mėnesiai yra aktyvūs.</span><span class="sxs-lookup"><span data-stu-id="3a6b6-111">New options have been added to leave and absence (**Human resources** parameters) to enable customers to determine when employees’ months of service date are effective.</span></span> <span data-ttu-id="3a6b6-112">Kai kuriose organizacijose data yra mėnesio pabaiga, tačiau kitose tai gali būti kito mėnesio pradžia.</span><span class="sxs-lookup"><span data-stu-id="3a6b6-112">For some organizations, the date is the end of the month, but for others it may be the start of the next month.</span></span> <span data-ttu-id="3a6b6-113">Pvz., viena organizacija gali skirti atostogų laiką gruodžio 31 d., o kita gali skirti atostogų laiką sausio 1 d.</span><span class="sxs-lookup"><span data-stu-id="3a6b6-113">For example, one organization may award time off on December 31, while another may award time off on January 1.</span></span> <span data-ttu-id="3a6b6-114">Ši parinktis suteiks galimybę pasirinkti, kada skyrimas turėtų įvykti.</span><span class="sxs-lookup"><span data-stu-id="3a6b6-114">This option will allow you to choose when the award should occur.</span></span> 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a><span data-ttu-id="3a6b6-115">Darbuotojo samdos veiksmų būsena Darbo eiga baigta nesikeičia</span><span class="sxs-lookup"><span data-stu-id="3a6b6-115">Worker hire actions are stuck in "Workflow complete" state</span></span>
<span data-ttu-id="3a6b6-116">Atlikti keitimai siekiant ištaisyti problemą, dėl kurios kelios darbo eigos baigdavosi nustatant būseną Darbo eiga baigta.</span><span class="sxs-lookup"><span data-stu-id="3a6b6-116">Changes have been made to correct an issue where a small number of workflows finished with a "Workflow complete" status.</span></span> <span data-ttu-id="3a6b6-117">Naujos darbo eigos dabar turėtų būti perkeltos į būseną Užbaigta, kai darbo eiga baigiama.</span><span class="sxs-lookup"><span data-stu-id="3a6b6-117">New workflows should now move to a "Completed" state when the workflow finishes.</span></span> <span data-ttu-id="3a6b6-118">Visos darbo eigos, kurių darbo eigos būsena baigta, bus perkeltos į klaidos būseną, kad pagal poreikį būtų galima atnaujinti arba pašalinti.</span><span class="sxs-lookup"><span data-stu-id="3a6b6-118">Any workflows in a workflow completed status will be transitioned to an error status to allow for updating or removal if required.</span></span> 
