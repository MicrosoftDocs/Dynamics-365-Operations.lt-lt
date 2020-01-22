---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent – Core HR“ (2018 m. lapkričio 15 d.)
description: Šioje temoje aprašomos „Microsoft“ sistemos „Dynamics 365 Talent – Core HR“ naujos ir pakeistos funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
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
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a7598db1dc4c11864cf5f5a73d00672ceb66e8c
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897471"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-15-2018"></a><span data-ttu-id="c7a4c-103">Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent – Core HR“ (2018 m. lapkričio 15 d.)</span><span class="sxs-lookup"><span data-stu-id="c7a4c-103">What's new or changed in Dynamics 365 Talent - Core HR (November 15, 2018)</span></span>

<span data-ttu-id="c7a4c-104">**8.1.2045 versija**</span><span class="sxs-lookup"><span data-stu-id="c7a4c-104">**Build 8.1.2045**</span></span>

<span data-ttu-id="c7a4c-105">Šioje temoje aprašomos naujos ir pakeistos „Core HR“ funkcijos.</span><span class="sxs-lookup"><span data-stu-id="c7a4c-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="other-changesfixes"></a><span data-ttu-id="c7a4c-106">Kiti pakeitimai / pataisos</span><span class="sxs-lookup"><span data-stu-id="c7a4c-106">Other changes/fixes</span></span>

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a><span data-ttu-id="c7a4c-107">Nepavyksta dabartinių darbuotojo pareigų pakeisti būsimas atviras pareigas</span><span class="sxs-lookup"><span data-stu-id="c7a4c-107">Unable to change employee´s current position to a future open position</span></span>

<span data-ttu-id="c7a4c-108">Atliktas pakeitimas, kad būtų galima perkelti pareigas, kai jos pasiekiamos tik ateityje.</span><span class="sxs-lookup"><span data-stu-id="c7a4c-108">A change has been made to enable position transfers when the position is only available in the future.</span></span> 

### <a name="position-does-not-display-when-creating-a-new-employee"></a><span data-ttu-id="c7a4c-109">Kuriant naują darbuotoją nerodomos pareigos</span><span class="sxs-lookup"><span data-stu-id="c7a4c-109">Position does not display when creating a new employee</span></span>

<span data-ttu-id="c7a4c-110">Atliktas pakeitimas, kad programoje „Talent“ samdant naujus darbuotojus būtų rodomos visos pasiekiamos pareigos, kurias galima priskirti.</span><span class="sxs-lookup"><span data-stu-id="c7a4c-110">A change has been made to display all open positions that are available for assignment when hiring new employees in Talent.</span></span> <span data-ttu-id="c7a4c-111">Tai taikoma retrospektyvinėms pareigoms arba tuo atveju, jei pareigų data yra būsima.</span><span class="sxs-lookup"><span data-stu-id="c7a4c-111">This includes historical positions or if the postitions have been future dated.</span></span> <span data-ttu-id="c7a4c-112">Dabar pareigos, priklausomai nuo įdarbinimo pradžios datos, bus rodomos teisingai.</span><span class="sxs-lookup"><span data-stu-id="c7a4c-112">Positions will now appear correctly based on the employment start date.</span></span> 

### <a name="termination-date-is-displaying-based-on-user-settings"></a><span data-ttu-id="c7a4c-113">Dabar atleidimo data rodoma remiantis vartotojo parametrais</span><span class="sxs-lookup"><span data-stu-id="c7a4c-113">Termination date is displaying based on user settings</span></span>

<span data-ttu-id="c7a4c-114">Atliktas buvusių darbuotojų sąrašo pakeitimas, kad peržiūrint atleidimo datą darbuotojai sąrašą galėtų pritaikyti pagal pageidaujamus laiko juostos poslinkius.</span><span class="sxs-lookup"><span data-stu-id="c7a4c-114">A change has been made to the past employees list to account for any time zone offsets for the employees preferred time zone when viewing the termination date.</span></span>

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a><span data-ttu-id="c7a4c-115">Man priskirti darbo elementai siejasi su neteisingai rodoma informacija</span><span class="sxs-lookup"><span data-stu-id="c7a4c-115">Work items assigned to me links not displaying the correct information</span></span>

<span data-ttu-id="c7a4c-116">Atlikus šį pakeitimą, naršant po išsamią atskirų darbo elementų, esančių sąraše, informaciją, bus rodoma teisinga pasirinkto elemento informacija.</span><span class="sxs-lookup"><span data-stu-id="c7a4c-116">With this change, navigation to the details of the individual work items in the list will display the correct information for the item selected.</span></span> <span data-ttu-id="c7a4c-117">Ši problema iškildavo tik taikant išplėstines saugos parinktis.</span><span class="sxs-lookup"><span data-stu-id="c7a4c-117">This issue only occurred with advanced security options.</span></span>


## <a name="known-issue"></a><span data-ttu-id="c7a4c-118">Žinoma problema</span><span class="sxs-lookup"><span data-stu-id="c7a4c-118">Known issue</span></span>

- <span data-ttu-id="c7a4c-119">**Problema**: įtraukiant naują priedą į darbininko puslapį mygtukai **Naujas** ir **Redaguoti** yra papilkinti.</span><span class="sxs-lookup"><span data-stu-id="c7a4c-119">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="c7a4c-120">**Problemos sprendimas:** prieš atidarydami priedų puslapį įsitikinkite, kad „FactBoxes“ laukai puslapyje **Darbininkas** yra uždaryti.</span><span class="sxs-lookup"><span data-stu-id="c7a4c-120">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="c7a4c-121">Jei „FactBoxes“ laukai yra uždaryti, įkeliant puslapį **Darbininkas** priedų mygtukai bus įjungti.</span><span class="sxs-lookup"><span data-stu-id="c7a4c-121">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="c7a4c-122">(Ši problema bus pašalinta kitame platformos naujinime.)</span><span class="sxs-lookup"><span data-stu-id="c7a4c-122">(This issue will be fixed in the next platform update.)</span></span>
