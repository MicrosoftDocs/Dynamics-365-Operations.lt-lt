---
title: Dokumentų būsenos ir vykdymo ciklas
description: Šioje temoje aptariamos įvairios „Microsoft Dynamics 365 Commerce“ puslapių elementų būsenos.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b4f1c462f734b2d58843308f0f877fe18a4d9af7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002986"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="2dbbb-103">Dokumentų būsenos ir vykdymo ciklas</span><span class="sxs-lookup"><span data-stu-id="2dbbb-103">Document states and lifecycle</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2dbbb-104">Šioje temoje aptariamos įvairios „Microsoft Dynamics 365 Commerce“ puslapių elementų būsenos.</span><span class="sxs-lookup"><span data-stu-id="2dbbb-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="2dbbb-105">Dokumento būsenos aprašas</span><span class="sxs-lookup"><span data-stu-id="2dbbb-105">Document state descriptions</span></span>

<span data-ttu-id="2dbbb-106">Temoje [Puslapio elementai](page-elements-overview.md) pateikiama įvairių dokumentų tipų turinio valdymo sistemoje (TVS).</span><span class="sxs-lookup"><span data-stu-id="2dbbb-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="2dbbb-107">Šie dokumentų tipai gali turėti kelias būsenas kūrimo įrankyje.</span><span class="sxs-lookup"><span data-stu-id="2dbbb-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="2dbbb-108">Dokumentų būsenos padeda apsaugoti nuo duomenų nesuderinamumo ir įgalinti versijų valdymą.</span><span class="sxs-lookup"><span data-stu-id="2dbbb-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="2dbbb-109">Jomis galima nustatyti, kas gali keisti dokumentus, kada dokumentai gali būti keičiami ir kada keitimus gali peržiūrėti kiti asmenys.</span><span class="sxs-lookup"><span data-stu-id="2dbbb-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="2dbbb-110">Šioje lentelėje pateikiamos galimos „Commerce“ puslapio elementų dokumento būsenos.</span><span class="sxs-lookup"><span data-stu-id="2dbbb-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="2dbbb-111">Dokumento būsena</span><span class="sxs-lookup"><span data-stu-id="2dbbb-111">Document state</span></span> | <span data-ttu-id="2dbbb-112">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="2dbbb-112">Description</span></span> |
|---|---|
| <span data-ttu-id="2dbbb-113">Paimta ir užrakinta</span><span class="sxs-lookup"><span data-stu-id="2dbbb-113">Checked out</span></span> | <span data-ttu-id="2dbbb-114">Jums paėmus ir užrakinus TVS elementą, jo negali redaguoti jokie kiti autentifikuoti sistemos vartotojai.</span><span class="sxs-lookup"><span data-stu-id="2dbbb-114">When a CMS item is checked out to you, it can't be edited by any other authenticated system users.</span></span> <span data-ttu-id="2dbbb-115">Visi keitimai, kuriuos atliekate elementui, matomi tik jums.</span><span class="sxs-lookup"><span data-stu-id="2dbbb-115">Any changes that you make to the item are visible only to you.</span></span> |
| <span data-ttu-id="2dbbb-116">Įrašyta ir atrakinta</span><span class="sxs-lookup"><span data-stu-id="2dbbb-116">Checked in</span></span> | <span data-ttu-id="2dbbb-117">Kai TVS elementas įrašytas ir atrakintas, visi keitimai yra matomi kitiems autentifikuotiems sistemos vartotojams, ir tie vartotojai gali tik tada paimti ir užrakinti elementą bei jį redaguoti.</span><span class="sxs-lookup"><span data-stu-id="2dbbb-117">When a CMS item is checked in, all changes are visible to other authenticated system users, and those users can then check out the item and edit it.</span></span> <span data-ttu-id="2dbbb-118">Kiekvienas įrašymas ir atrakinimas sukuria dokumento versijos įrašą elemento retrospektyvoje.</span><span class="sxs-lookup"><span data-stu-id="2dbbb-118">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="2dbbb-119">Publikuota</span><span class="sxs-lookup"><span data-stu-id="2dbbb-119">Published</span></span> | <span data-ttu-id="2dbbb-120">Kai TVS elementas yra publikuotas, jis yra priverstinai teikiamas į jūsų tiesioginę svetainę ir tampa aptinkamas internete neautentifikuotų Išorinių vartotojų.</span><span class="sxs-lookup"><span data-stu-id="2dbbb-120">When a CMS item is published, it's pushed to your live site and becomes discoverable on the internet by non-authenticated external users.</span></span> <span data-ttu-id="2dbbb-121">Elementai gali būti publikuojami tik tada, kai jie įrašyti ir atrakinti.</span><span class="sxs-lookup"><span data-stu-id="2dbbb-121">Items can be published only if they have been checked in.</span></span> |
| <span data-ttu-id="2dbbb-122">Įrašyta</span><span class="sxs-lookup"><span data-stu-id="2dbbb-122">Saved</span></span> | <span data-ttu-id="2dbbb-123">Keitimai, kurie buvo atlikti su paimtu ir užrakintu TVS elementu, gali būti įrašyti į TVS, prieš elementą įrašant ir atrakinant ar publikuojant.</span><span class="sxs-lookup"><span data-stu-id="2dbbb-123">Changes that have been made to a checked-out CMS item can be saved to the CMS before the item is checked in or published.</span></span> <span data-ttu-id="2dbbb-124">Šie įrašyti keitimai nematomi kitiems autentifikuotiems sistemos vartotojams, kol elementas nebus įrašytas ir atrakintas.</span><span class="sxs-lookup"><span data-stu-id="2dbbb-124">These saved changes aren't visible to other authenticated system users until the item is checked in.</span></span> <span data-ttu-id="2dbbb-125">Jie nematomi išoriniams vartotojams, kol elementas nebus publikuotas.</span><span class="sxs-lookup"><span data-stu-id="2dbbb-125">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="2dbbb-126">Atmestas paėmimas ir užrakinimas</span><span class="sxs-lookup"><span data-stu-id="2dbbb-126">Discarded check out</span></span> | <span data-ttu-id="2dbbb-127">Kai paimtas ir užrakintas TVS elementas atmetamas, visi įrašyti keitimai panaikinami, o elementas grįžta į vėliausiai įrašytą ir atrakintą versiją.</span><span class="sxs-lookup"><span data-stu-id="2dbbb-127">When a checked-out CMS item is discarded, all saved changes are deleted, and the item reverts to the version that was most recently checked in.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="2dbbb-128">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="2dbbb-128">Additional resources</span></span>

[<span data-ttu-id="2dbbb-129">Turinio įtraukimo būdai</span><span class="sxs-lookup"><span data-stu-id="2dbbb-129">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="2dbbb-130">Puslapio modelio žodynas</span><span class="sxs-lookup"><span data-stu-id="2dbbb-130">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="2dbbb-131">Darbas su publikavimo grupėmis</span><span class="sxs-lookup"><span data-stu-id="2dbbb-131">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="2dbbb-132">Darbas su moduliais</span><span class="sxs-lookup"><span data-stu-id="2dbbb-132">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="2dbbb-133">Darbas su fragmentais</span><span class="sxs-lookup"><span data-stu-id="2dbbb-133">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="2dbbb-134">Šablonų ir maketų apžvalga</span><span class="sxs-lookup"><span data-stu-id="2dbbb-134">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="2dbbb-135">Svetainės naršymo tinkinimas</span><span class="sxs-lookup"><span data-stu-id="2dbbb-135">Customize site navigation</span></span>](customize-site-navigation.md)
