---
title: Tvirtinti konkrečių įsigijimo kategorijų tiekėjus
description: Sukūrus pirkimo paraišką, gali reikėti pasirinkti patvirtintą arba pageidaujamą tiekėją, atsižvelgiant į tai, kaip nustatytos pirkimo strategijos.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eec50e2e8f08fabb64f89c17159b97ba770026f8
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836343"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="d3ca7-103">Tvirtinti konkrečių įsigijimo kategorijų tiekėjus</span><span class="sxs-lookup"><span data-stu-id="d3ca7-103">Approve vendors for specific procurement categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d3ca7-104">Sukūrus pirkimo paraišką, gali reikėti pasirinkti patvirtintą arba pageidaujamą tiekėją, atsižvelgiant į tai, kaip nustatytos pirkimo strategijos.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-104">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="d3ca7-105">Šioje procedūroje parodoma, kaip nurodyti, kad konkrečios įsigijimo kategorijos tiekėjas yra patvirtintas arba pageidaujamas.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-105">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="d3ca7-106">Šią užduotį paprastai atlieka pirkimų profesionalai.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-106">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="d3ca7-107">Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-107">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="d3ca7-108">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Tiekėjai > Visi tiekėjai.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-108">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="d3ca7-109">Pasirinkite tiekėją, kurį norite nustatyti kaip patvirtintą arba pageidaujamą kategorijos tiekėją.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-109">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="d3ca7-110">Veiksmų srityje spustelėkite Bendra.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-110">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="d3ca7-111">Spustelėkite Kategorijos.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-111">Click Categories.</span></span>
5. <span data-ttu-id="d3ca7-112">Spustelėkite Įtraukti kategoriją.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-112">Click Add category.</span></span>
6. <span data-ttu-id="d3ca7-113">Lauke Kategorija pasirinkite BIURO IR STALO REIKMENYS (BIURO IR STALO REIKMENYS).</span><span class="sxs-lookup"><span data-stu-id="d3ca7-113">In the Category field, select OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES).</span></span>
7. <span data-ttu-id="d3ca7-114">Lauke Tiekėjo kategorijos būsena pasirinkite Pageidaujamas.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-114">In the Vendor category status field, select 'Preferred'.</span></span>
    * <span data-ttu-id="d3ca7-115">Galima nurodyti daugiau nei vieną pageidaujamą kategorijos tiekėją.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-115">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="d3ca7-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-116">Click Save.</span></span>
9. <span data-ttu-id="d3ca7-117">Eikite į Įsigijimas ir šaltinio pasirinkimas > Įsigijimo kategorijos.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-117">Go to Procurement and sourcing > Procurement categories.</span></span>
10. <span data-ttu-id="d3ca7-118">Medyje pasirinkite CORP ĮSIGIJIMO KATEGORIJOS \ BIURO IR STALO REIKMENYS.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-118">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES'.</span></span>
11. <span data-ttu-id="d3ca7-119">Išplėskite sekciją Tiekėjai.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-119">Expand the Vendors section.</span></span>
    * <span data-ttu-id="d3ca7-120">Patikrinkite, ar jūsų pasirinktas tiekėjas rodomas kaip pageidaujamas kategorijos Biuro ir stalo reikmenys tiekėjas.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-120">Check if the vendor that you selected  appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="d3ca7-121">Jei šią procedūrą vykdote kaip užduočių vedlį, jums gali reikėti spustelėti mygtuką Atrakinti, galėtumėte slinkti žemyn į tiekėjų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-121">If you’re running this procedure as a task guide, you may have to click the Unlock button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="d3ca7-122">Šiame puslapyje taip pat galima įtraukti pageidaujamų ir patvirtintų tiekėjų.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-122">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="d3ca7-123">Medyje išplėskite BIURO IR STALO REIKMENYS.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-123">In the tree, expand 'OFFICE AND DESK ACCESSORIES'.</span></span>
13. <span data-ttu-id="d3ca7-124">Medyje pasirinkite Žirklės.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-124">In the tree, select 'Scissors'.</span></span>
14. <span data-ttu-id="d3ca7-125">Lauke Perimti tiekėjus iš pirminės kategorijos pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-125">Select No in the Inherit vendors from parent category: field.</span></span>
15. <span data-ttu-id="d3ca7-126">Lauke Perimti tiekėjus iš pirminės kategorijos pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="d3ca7-126">Select Yes in the Inherit vendors from parent category: field.</span></span>

