---
title: Konkrečių įsigijimo kategorijų tiekėjų tvirtinimas
description: Šioje temoje aiškinama, kaip patvirtinti konkrečių įsigijimo kategorijų Dynamics 365 Supply Chain Management tiekėjus.
author: mkirknel
manager: AnnBe
ms.date: 07/30/2019
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
ms.openlocfilehash: e47124e22dd6c0e756bf42429327254f966b48a2
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018094"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="20b03-103">Konkrečių įsigijimo kategorijų tiekėjų tvirtinimas</span><span class="sxs-lookup"><span data-stu-id="20b03-103">Approve vendors for specific procurement categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="20b03-104">Šioje temoje aiškinama, kaip patvirtinti konkrečių įsigijimo kategorijų Dynamics 365 Supply Chain Management tiekėjus.</span><span class="sxs-lookup"><span data-stu-id="20b03-104">This topic explains how to approve vendors for specific procurement categories in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="20b03-105">Sukūrus pirkimo paraišką, gali reikėti pasirinkti patvirtintą arba pageidaujamą tiekėją, atsižvelgiant į tai, kaip nustatytos pirkimo strategijos.</span><span class="sxs-lookup"><span data-stu-id="20b03-105">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="20b03-106">Šioje procedūroje parodoma, kaip nurodyti, kad konkrečios įsigijimo kategorijos tiekėjas yra patvirtintas arba pageidaujamas.</span><span class="sxs-lookup"><span data-stu-id="20b03-106">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="20b03-107">Šią užduotį paprastai atlieka pirkimų profesionalai.</span><span class="sxs-lookup"><span data-stu-id="20b03-107">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="20b03-108">Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="20b03-108">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="20b03-109">Naršymo srityje eikite į **Moduliai > Įsigijimas ir išteklių paskirstymas > Tiekėjai > Visi tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="20b03-109">In the navigation pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="20b03-110">Pasirinkite tiekėją, kurį norite nustatyti kaip patvirtintą arba pageidaujamą kategorijos tiekėją.</span><span class="sxs-lookup"><span data-stu-id="20b03-110">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="20b03-111">Veiksmų srityje spustelėkite **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="20b03-111">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="20b03-112">Pažymėkite **Kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="20b03-112">Select **Categories**.</span></span>
5. <span data-ttu-id="20b03-113">Pažymėkite **Įtraukti kategoriją**.</span><span class="sxs-lookup"><span data-stu-id="20b03-113">Select **Add category**.</span></span>
6. <span data-ttu-id="20b03-114">Lauke **Kategorija** pažymėkite **BIURO IR STALO PRIEDAI (BIURO IR STALO PRIEDAI)**.</span><span class="sxs-lookup"><span data-stu-id="20b03-114">In the **Category** field, select **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span></span>
7. <span data-ttu-id="20b03-115">Lauke **Tiekėjų kategorijos būsena** pažymėkite **Pageidaujama**.</span><span class="sxs-lookup"><span data-stu-id="20b03-115">In the **Vendor category status** field, select **Preferred**.</span></span> <span data-ttu-id="20b03-116">Galima nurodyti daugiau nei vieną pageidaujamą kategorijos tiekėją.</span><span class="sxs-lookup"><span data-stu-id="20b03-116">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="20b03-117">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="20b03-117">Select **Save**.</span></span>
9. <span data-ttu-id="20b03-118">Naršymo srityje eikite į **Moduliai > Įsigijimas ir išteklių paskirstymas > Įsigijimo kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="20b03-118">In the navigation pane, go to **Modules > Procurement and sourcing > Procurement categories**.</span></span>
10. <span data-ttu-id="20b03-119">Medyje pažymėkite **KORP. ĮSIGIJIMO KATEGORIJOS\BIURO IR STALO PRIEDAI**.</span><span class="sxs-lookup"><span data-stu-id="20b03-119">In the tree, select **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span></span>
11. <span data-ttu-id="20b03-120">Išplėskite skyrių **Tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="20b03-120">Expand the **Vendors** section.</span></span> <span data-ttu-id="20b03-121">Patikrinkite, ar jūsų pasirinktas tiekėjas rodomas kaip pageidaujamas kategorijos Biuro ir stalo reikmenys tiekėjas.</span><span class="sxs-lookup"><span data-stu-id="20b03-121">Check if the vendor that you selected appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="20b03-122">Jei vykdote šią procedūrą kaip užduoties vadovą, gali reikėti pažymėti mygtuką **Atrakinti**, kad galėtumėte slinkti žemyn tiekėjų sąrašu.</span><span class="sxs-lookup"><span data-stu-id="20b03-122">If you’re running this procedure as a task guide, you may have to select the **Unlock** button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="20b03-123">Šiame puslapyje taip pat galima įtraukti pageidaujamų ir patvirtintų tiekėjų.</span><span class="sxs-lookup"><span data-stu-id="20b03-123">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="20b03-124">Medyje išplėskite **BIURO IR STALO PRIEDAI** ir pažymėkite **Žirklės**.</span><span class="sxs-lookup"><span data-stu-id="20b03-124">In the tree, expand **OFFICE AND DESK ACCESSORIES** and select **Scissors**.</span></span>
13. <span data-ttu-id="20b03-125">Lauke **Paveldimi tiekėjai iš pirminės kategorijos:** pažymėkite **Ne**.</span><span class="sxs-lookup"><span data-stu-id="20b03-125">Select **No** in the **Inherit vendors from parent category:** field.</span></span>
14. <span data-ttu-id="20b03-126">Lauke **Paveldimi tiekėjai iš pirminės kategorijos:** pažymėkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="20b03-126">Select **Yes** in the **Inherit vendors from parent category:** field.</span></span>

