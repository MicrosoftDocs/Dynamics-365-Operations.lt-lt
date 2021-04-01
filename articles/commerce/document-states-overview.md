---
title: Dokumentų būsenos ir vykdymo ciklas
description: Šioje temoje aptariamos įvairios „Microsoft Dynamics 365 Commerce“ puslapių elementų būsenos.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 457b1ac7afb8cad57399572acf429d208db917af
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230539"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="15778-103">Dokumentų būsenos ir vykdymo ciklas</span><span class="sxs-lookup"><span data-stu-id="15778-103">Document states and lifecycle</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="15778-104">Šioje temoje aptariamos įvairios „Microsoft Dynamics 365 Commerce“ puslapių elementų būsenos.</span><span class="sxs-lookup"><span data-stu-id="15778-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="15778-105">Dokumento būsenos aprašas</span><span class="sxs-lookup"><span data-stu-id="15778-105">Document state descriptions</span></span>

<span data-ttu-id="15778-106">Temoje [Puslapio elementai](page-elements-overview.md) pateikiama įvairių dokumentų tipų turinio valdymo sistemoje (TVS).</span><span class="sxs-lookup"><span data-stu-id="15778-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="15778-107">Šie dokumentų tipai gali turėti kelias būsenas kūrimo įrankyje.</span><span class="sxs-lookup"><span data-stu-id="15778-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="15778-108">Dokumentų būsenos padeda apsaugoti nuo duomenų nesuderinamumo ir įgalinti versijų valdymą.</span><span class="sxs-lookup"><span data-stu-id="15778-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="15778-109">Jomis galima nustatyti, kas gali keisti dokumentus, kada dokumentai gali būti keičiami ir kada keitimus gali peržiūrėti kiti asmenys.</span><span class="sxs-lookup"><span data-stu-id="15778-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="15778-110">Šioje lentelėje pateikiamos galimos „Commerce“ puslapio elementų dokumento būsenos.</span><span class="sxs-lookup"><span data-stu-id="15778-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="15778-111">Dokumento būsena</span><span class="sxs-lookup"><span data-stu-id="15778-111">Document state</span></span>      | <span data-ttu-id="15778-112">Svetainių daryklės veiksmai</span><span class="sxs-lookup"><span data-stu-id="15778-112">Site builder action</span></span>        | <span data-ttu-id="15778-113">aprašymas</span><span class="sxs-lookup"><span data-stu-id="15778-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="15778-114">Išregistruota</span><span class="sxs-lookup"><span data-stu-id="15778-114">Checked out</span></span>         | <span data-ttu-id="15778-115">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="15778-115">Select **Edit**.</span></span>           | <span data-ttu-id="15778-116">Taikomas dokumentas paimamas ir užrakinamas.</span><span class="sxs-lookup"><span data-stu-id="15778-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="15778-117">Kol dokumentas yra šioje būsenoje, jo negalima pakeisti kiti autentifikuoti sistemos vartotojai, o visi keitimai, kuriuos atliekate dokumente, matomi tik jums.</span><span class="sxs-lookup"><span data-stu-id="15778-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="15778-118">Įrašyta</span><span class="sxs-lookup"><span data-stu-id="15778-118">Saved</span></span>               | <span data-ttu-id="15778-119">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="15778-119">Select **Save**.</span></span>           | <span data-ttu-id="15778-120">Keitimai, atlikti išregistruotame dokumente, įrašomi į duomenų bazę, tačiau dokumentas dar nėra įrašomas ir atrakinamas ar publikuojamas.</span><span class="sxs-lookup"><span data-stu-id="15778-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="15778-121">Įrašyti keitimai nematomi kitiems autentifikuotiems sistemos vartotojams, kol autorius nepasirenka **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="15778-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing**.</span></span> <span data-ttu-id="15778-122">Jie nematomi išoriniams vartotojams, kol elementas nebus publikuotas.</span><span class="sxs-lookup"><span data-stu-id="15778-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="15778-123">Atmestas paėmimas ir užrakinimas</span><span class="sxs-lookup"><span data-stu-id="15778-123">Discarded check out</span></span> | <span data-ttu-id="15778-124">Pasirinkite **Atmesti pakeitimus**.</span><span class="sxs-lookup"><span data-stu-id="15778-124">Select **Discard edits**.</span></span>  | <span data-ttu-id="15778-125">Visi išregistruoto dokumento pakeitimai atmetami, o elementas grįžta į paskutinę įrašytą ir atrakintą versiją.</span><span class="sxs-lookup"><span data-stu-id="15778-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="15778-126">Įregistruota</span><span class="sxs-lookup"><span data-stu-id="15778-126">Checked in</span></span>          | <span data-ttu-id="15778-127">Pasirinkite **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="15778-127">Select **Finish editing**.</span></span> | <span data-ttu-id="15778-128">Redaguotas dokumentas yra įrašomas ir atrakinamas.</span><span class="sxs-lookup"><span data-stu-id="15778-128">The edited document is checked in.</span></span> <span data-ttu-id="15778-129">Visi pakeitimai yra matomi kitiems autentifikuotiems sistemos vartotojams ir tie vartotojai gali redaguoti dokumentą.</span><span class="sxs-lookup"><span data-stu-id="15778-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="15778-130">Kiekvienas įrašymas ir atrakinimas sukuria dokumento versijos įrašą elemento retrospektyvoje.</span><span class="sxs-lookup"><span data-stu-id="15778-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="15778-131">Publikuota</span><span class="sxs-lookup"><span data-stu-id="15778-131">Published</span></span>           | <span data-ttu-id="15778-132">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="15778-132">Select **Publish**.</span></span>        | <span data-ttu-id="15778-133">Dokumentas publikuojamas, o pakeitimai yra paskelbiami jūsų paleistoje svetainėje ir tampa aptinkami išoriniams vartotojams.</span><span class="sxs-lookup"><span data-stu-id="15778-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="15778-134">Elementai gali būti publikuojami tik tada, kai jie įrašyti ir atrakinti pasirinkus **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="15778-134">Items can be published only if they have first been checked in by selecting **Finish editing**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="15778-135">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="15778-135">Additional resources</span></span>

[<span data-ttu-id="15778-136">Turinio įtraukimo būdai</span><span class="sxs-lookup"><span data-stu-id="15778-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="15778-137">Puslapio modelio žodynas</span><span class="sxs-lookup"><span data-stu-id="15778-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="15778-138">Darbas su publikavimo grupėmis</span><span class="sxs-lookup"><span data-stu-id="15778-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="15778-139">Kelių kanalų bendrinimo funkcijos įjungimas ir naudojimas</span><span class="sxs-lookup"><span data-stu-id="15778-139">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="15778-140">Darbas su moduliais</span><span class="sxs-lookup"><span data-stu-id="15778-140">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="15778-141">Darbas su fragmentais</span><span class="sxs-lookup"><span data-stu-id="15778-141">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="15778-142">Šablonų ir maketų apžvalga</span><span class="sxs-lookup"><span data-stu-id="15778-142">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="15778-143">Svetainės naršymo tinkinimas</span><span class="sxs-lookup"><span data-stu-id="15778-143">Customize site navigation</span></span>](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]