---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent Core HR“ (2018 m. lapkričio 27 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent Core HR“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
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
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 81ea0e4f4878d1967234c597504071ce464a22c5
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/19/2019
ms.locfileid: "857805"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-27-2018"></a><span data-ttu-id="0d9fe-103">Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent Core HR“ (2018 m. lapkričio 27 d.)</span><span class="sxs-lookup"><span data-stu-id="0d9fe-103">What's new or changed in Dynamics 365 for Talent Core HR (November 27, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0d9fe-104">**8.1.2064 versija**</span><span class="sxs-lookup"><span data-stu-id="0d9fe-104">**Build 8.1.2064**</span></span>

<span data-ttu-id="0d9fe-105">Šioje temoje aprašomos naujos ir pakeistos „Core HR“ funkcijos.</span><span class="sxs-lookup"><span data-stu-id="0d9fe-105">This topic describes features that are either new or changed in Core HR.</span></span>


## <a name="changes"></a><span data-ttu-id="0d9fe-106">Pakeitimai</span><span class="sxs-lookup"><span data-stu-id="0d9fe-106">Changes</span></span>

### <a name="unable-to-create-a-note-in-case-management"></a><span data-ttu-id="0d9fe-107">Nepavyksta sukurti pastabos sprendime Atvejų valdymas</span><span class="sxs-lookup"><span data-stu-id="0d9fe-107">Unable to create a note in Case Management</span></span>

<span data-ttu-id="0d9fe-108">Atliktas pakeitimas, susijęs su problema, kildavusia bandant redaguoti ar sukurti pastabą sprendimo Atvejų valdymas atvejo žurnale.</span><span class="sxs-lookup"><span data-stu-id="0d9fe-108">A change has been made for an issue when attempting to edit or create a note in the case log of Case Management.</span></span>

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a><span data-ttu-id="0d9fe-109">Klaidingai parašytas žodis kompensacijos darbo srityje pateikiamame kompensavimo skirtuke</span><span class="sxs-lookup"><span data-stu-id="0d9fe-109">Misspelled word on the analytics tab in the compensation workspace</span></span> 

<span data-ttu-id="0d9fe-110">Žodžių „Etninė kilmė“, esančių kompensacijos darbo srities kompensacijos analizės diagramoje rašyba pakeista į teisingą.</span><span class="sxs-lookup"><span data-stu-id="0d9fe-110">A change has been made to correct the spelling of 'Ethnic Origin' in the compensation analytics chart in the compensation workspace.</span></span>

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a><span data-ttu-id="0d9fe-111">Kai vartotojas nepriskirtas darbininkui, darbuotojų savitarnos darbo sritis nerodoma.</span><span class="sxs-lookup"><span data-stu-id="0d9fe-111">Employee self-service workspace not displaying when a user isn't assigned to a worker</span></span> 

<span data-ttu-id="0d9fe-112">Atliktas pakeitimas, susijęs su tuo, kai pirmame paleisties puslapyje vartotojas, kuris nėra priskirtas darbininkui, pasirinkdavo darbo sritį **Darbuotojų savitarna**.</span><span class="sxs-lookup"><span data-stu-id="0d9fe-112">A change has been made when the **Employee self-service** workspace is selected as the initial page on startup for a user who is not assigned to a worker.</span></span> <span data-ttu-id="0d9fe-113">Tokiu atveju bus rodoma numatytoji ataskaitų sritis.</span><span class="sxs-lookup"><span data-stu-id="0d9fe-113">In this situation, the default dashboard will be displayed.</span></span>

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a><span data-ttu-id="0d9fe-114">Su atostogomis ir neatvykimu susijusi klaida: objekto egzemplioriui nenustatyta objekto nuoroda.</span><span class="sxs-lookup"><span data-stu-id="0d9fe-114">Leave and Absence error: Object reference not set to an instance of an object</span></span>

<span data-ttu-id="0d9fe-115">Atlikta su atostogomis ir neatvykimu susijusių pakeitimų, siekiant ištaisyti šią klaidą, kai sąraše **Man priskirti darbo elementai** patvirtinami su atostogomis ir neatvykimu susiję įrašai.</span><span class="sxs-lookup"><span data-stu-id="0d9fe-115">Changes have been made to Leave and Absence to correct this error after approving leave and absence records in the **Work items assigned to me** list.</span></span>

### <a name="unable-to-recall-an-image-workflow"></a><span data-ttu-id="0d9fe-116">Nepavyksta atšaukti vaizdo darbo eigos</span><span class="sxs-lookup"><span data-stu-id="0d9fe-116">Unable to recall an image workflow</span></span>

<span data-ttu-id="0d9fe-117">Atšaukus vaizdo darbo eigą, ši eiga bus nustatyta kaip „Atšaukta“, o esamą užklausą bus galima panaikinti darbuotojų savitarnos darbo srityje.</span><span class="sxs-lookup"><span data-stu-id="0d9fe-117">After recalling an image workflow, the workflow will be set to "cancelled" and the existing request can be deleted in the employee self-service workspace.</span></span>

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a><span data-ttu-id="0d9fe-118">Po atleidimo keletą kartų rodomi pakartotinai pasamdyti darbuotojai arba rangovai.</span><span class="sxs-lookup"><span data-stu-id="0d9fe-118">Rehired employees or contractors show up multiple times after termination</span></span> 

<span data-ttu-id="0d9fe-119">Po šio atnaujinimo atleisti ir pakartotinai pasamdyti darbuotojai esamame sąraše bus rodomi tik kartą.</span><span class="sxs-lookup"><span data-stu-id="0d9fe-119">With this update, terminated employees that are rehired will only display one time in the exited list.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="0d9fe-120">Žinoma problema</span><span class="sxs-lookup"><span data-stu-id="0d9fe-120">Known issue</span></span>

- <span data-ttu-id="0d9fe-121">**Problema**: įtraukiant naują priedą į darbininko puslapį mygtukai **Naujas** ir **Redaguoti** yra papilkinti.</span><span class="sxs-lookup"><span data-stu-id="0d9fe-121">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="0d9fe-122">**Problemos sprendimas:** prieš atidarydami priedų puslapį įsitikinkite, kad „FactBoxes“ laukai puslapyje **Darbininkas** yra uždaryti.</span><span class="sxs-lookup"><span data-stu-id="0d9fe-122">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="0d9fe-123">Jei „FactBoxes“ laukai yra uždaryti, įkeliant puslapį **Darbininkas** priedų mygtukai bus įjungti.</span><span class="sxs-lookup"><span data-stu-id="0d9fe-123">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="0d9fe-124">(Ši problema bus pašalinta kitame platformos naujinime.)</span><span class="sxs-lookup"><span data-stu-id="0d9fe-124">(This issue will be fixed in the next platform update.)</span></span>
