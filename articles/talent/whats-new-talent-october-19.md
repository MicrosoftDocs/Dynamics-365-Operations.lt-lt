---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent – Core HR“ (2018 m. spalio 16 d.)
description: Šioje temoje aprašomos „Microsoft“ sistemos „Dynamics 365 Talent – Core HR“ naujos ir pakeistos funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
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
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d5f2aea5fcc81d0b4c1d8a392a3e56c888440a94
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897401"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-16-2018"></a><span data-ttu-id="443cb-103">Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent – Core HR“ (2018 m. spalio 16 d.)</span><span class="sxs-lookup"><span data-stu-id="443cb-103">What's new or changed in Dynamics 365 Talent - Core HR (October 16, 2018)</span></span>

<span data-ttu-id="443cb-104">**8.1.1067 versija**</span><span class="sxs-lookup"><span data-stu-id="443cb-104">**Build 8.1.1067**</span></span>

<span data-ttu-id="443cb-105">Šioje temoje aprašomos naujos ir pakeistos „Core HR“ funkcijos.</span><span class="sxs-lookup"><span data-stu-id="443cb-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-managers-to-update-time-off-requests"></a><span data-ttu-id="443cb-106">Leisti vadovams atnaujinti prašymus išleisti iš darbo</span><span class="sxs-lookup"><span data-stu-id="443cb-106">Allow managers to update time off requests</span></span>

<span data-ttu-id="443cb-107">Darbo eigoje patvirtinus darbuotų prašymus išleisti iš darbo, juos gali reikėti atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="443cb-107">Employee time off requests may need to be updated after they are approved through the workflow.</span></span> <span data-ttu-id="443cb-108">Daugeliu atvejų šiuos atnaujinimus darbuotojo vardu atlieka vadovas.</span><span class="sxs-lookup"><span data-stu-id="443cb-108">In many cases, the manager makes these updates on the employee’s behalf.</span></span> <span data-ttu-id="443cb-109">Ši nauja funkcija suteikia vadovams galimybę darbuotojų vardu atnaujinti ne darbo laiką arba atšaukti prašymus išleisti iš darbo.</span><span class="sxs-lookup"><span data-stu-id="443cb-109">This new feature provides the ability for managers to update time off or cancel time off requests on behalf of their employees.</span></span> <span data-ttu-id="443cb-110">Ši galimybė kontroliuojama parametru **Darbas kito asmens vardu**, kurį galima nustatyti puslapyje **Personalo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="443cb-110">This capability is controlled by the **Work on behalf** parameter that can be set on the **Human Resource Parameters** page.</span></span> 
 
## <a name="allow-hr-to-update-time-off-requests"></a><span data-ttu-id="443cb-111">Leisti personalo skyriui atnaujinti prašymus išleisti iš darbo</span><span class="sxs-lookup"><span data-stu-id="443cb-111">Allow HR to update time off requests</span></span>

<span data-ttu-id="443cb-112">Panašiai kaip ir naudojant anksčiau minėtą funkciją, darbo eigoje patvirtinus darbuotojų prašymus išleisti iš darbo, juos gali reikėti atnaujinti personalo skyriaus darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="443cb-112">Similar to the feature above, employee time off requests may need to be updated by HR after they have been previously approved through the workflow.</span></span> <span data-ttu-id="443cb-113">Ši funkcija suteikia galimybę personalo skyriaus vartotojams atnaujinti prašymus išleisti iš darbo.</span><span class="sxs-lookup"><span data-stu-id="443cb-113">This feature provides the ability for HR users to update time off requests.</span></span> <span data-ttu-id="443cb-114">Šią galimybę galima įjungti darbo srityje **Žmonės** ir puslapyje **Darbininkas** naudojantis nauja parinktimi **Rodyti ne darbo laiką**.</span><span class="sxs-lookup"><span data-stu-id="443cb-114">The capability is enabled in the **People** workspace and on the **Worker** page, using a new option called **View time off**.</span></span> <span data-ttu-id="443cb-115">Šiuose puslapiuose personalo skyriaus vartotojai gali peržiūrėti prašymus ir atnaujinti ne darbo laiko operacijas panašiai, kaip šiuos veiksmus gali atlikti vadovai.</span><span class="sxs-lookup"><span data-stu-id="443cb-115">On those pages, HR users can view requests and update time off transactions, similar to how managers can perform these actions.</span></span>

<span data-ttu-id="443cb-116">Prieigą prie šios funkcijos kontroliuoja ši saugos pareiga:</span><span class="sxs-lookup"><span data-stu-id="443cb-116">The security duty that controls access to this functionality is:</span></span>
- <span data-ttu-id="443cb-117">Pareiga: prižiūrėti darbininkų atostogų ir neatvykimų procesus</span><span class="sxs-lookup"><span data-stu-id="443cb-117">Duty: Maintain worker-specific leave and absence processes.</span></span>
- <span data-ttu-id="443cb-118">Teisė: tvarkyti visų darbininkų atostogų ir leidimo neatvykti prašymus</span><span class="sxs-lookup"><span data-stu-id="443cb-118">Privilege: Maintain leave and absence requests for all workers.</span></span>

## <a name="other-changes"></a><span data-ttu-id="443cb-119">Kiti pakeitimai</span><span class="sxs-lookup"><span data-stu-id="443cb-119">Other changes</span></span>
<span data-ttu-id="443cb-120">Šiame leidime atlikti toliau nurodyti naujinimai.</span><span class="sxs-lookup"><span data-stu-id="443cb-120">The following updates have been made in this release:</span></span>
- <span data-ttu-id="443cb-121">Pakeisti darbininkų samdymo veiksmai, kad jie daugiau „nebestrigtų“ būsenoje **Darbo eiga baigta**.</span><span class="sxs-lookup"><span data-stu-id="443cb-121">Changes to worker hire actions so that they are no longer "stuck" in **Workflow complete** state.</span></span>
- <span data-ttu-id="443cb-122">Dabar įdarbinimo įrašą galima sukurti be įdarbinimo pradžios datos.</span><span class="sxs-lookup"><span data-stu-id="443cb-122">Employment record can now be created without an employment start date.</span></span>
- <span data-ttu-id="443cb-123">Dabar darbuotojų savitarnoje rodomai „Dynamics 365 Talent“ kursų registravimo datai taikomas šios datos laiko juostos poslinkis.</span><span class="sxs-lookup"><span data-stu-id="443cb-123">The Dynamics 365 Talent registration date for a course shown in Employee self-service now applies the time zone offset to the date.</span></span>
- <span data-ttu-id="443cb-124">„Excel“ failų negalima importuoti kelis kartus be klaidų naudojant parinktį **Darbuotojo objektas**.</span><span class="sxs-lookup"><span data-stu-id="443cb-124">Excel files can be imported multiple times without any errors using **Employee Entity**.</span></span>

## <a name="known-issue"></a><span data-ttu-id="443cb-125">Žinoma problema</span><span class="sxs-lookup"><span data-stu-id="443cb-125">Known issue</span></span>

- <span data-ttu-id="443cb-126">**Problema**: įtraukiant naują priedą į darbininko puslapį mygtukai **Naujas** ir **Redaguoti** yra papilkinti.</span><span class="sxs-lookup"><span data-stu-id="443cb-126">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="443cb-127">**Problemos sprendimas:** prieš atidarydami priedų puslapį įsitikinkite, kad „FactBoxes“ laukai puslapyje **Darbininkas** yra uždaryti.</span><span class="sxs-lookup"><span data-stu-id="443cb-127">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="443cb-128">Jei „FactBoxes“ laukai yra uždaryti, įkeliant puslapį **Darbininkas** priedų mygtukai bus įjungti.</span><span class="sxs-lookup"><span data-stu-id="443cb-128">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="443cb-129">(Ši problema bus pašalinta kitame platformos naujinime.)</span><span class="sxs-lookup"><span data-stu-id="443cb-129">(This issue will be fixed in the next platform update.)</span></span>
