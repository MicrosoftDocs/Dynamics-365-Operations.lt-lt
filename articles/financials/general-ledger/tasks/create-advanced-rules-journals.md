--- 
title: "Kurti papildomas žurnalų taisykles"
description: "Ši procedūra padeda sukurti išplėstines žurnalų taisykles."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1bb1663b0f5d7e6a550e1ffd2ee2edf3771a13b3
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="81a2d-103">Kurti papildomas žurnalų taisykles</span><span class="sxs-lookup"><span data-stu-id="81a2d-103">Create advanced rules for journals</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="81a2d-104">Ši procedūra padeda sukurti išplėstines žurnalų taisykles.</span><span class="sxs-lookup"><span data-stu-id="81a2d-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="81a2d-105">Ji apima žurnalo valdymo ir vartotojo registravimo apribojimų nustatymą.</span><span class="sxs-lookup"><span data-stu-id="81a2d-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="81a2d-106">Šioje procedūroje naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="81a2d-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="81a2d-107">Žurnalo valdymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="81a2d-107">Set up journal control</span></span>
1. <span data-ttu-id="81a2d-108">Pasirinkite Didžioji knyga > Žurnalo nustatymas > Žurnalo pavadinimai.</span><span class="sxs-lookup"><span data-stu-id="81a2d-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="81a2d-109">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="81a2d-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="81a2d-110">Spustelėkite Žurnalo valdymas.</span><span class="sxs-lookup"><span data-stu-id="81a2d-110">Click Journal control.</span></span>
4. <span data-ttu-id="81a2d-111">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="81a2d-111">Click Add.</span></span>
5. <span data-ttu-id="81a2d-112">Lauke Įmonės sąskaitos spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="81a2d-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="81a2d-113">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="81a2d-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="81a2d-114">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="81a2d-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="81a2d-115">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="81a2d-115">Click Add.</span></span>
9. <span data-ttu-id="81a2d-116">Lauke Sąskaitos struktūra spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="81a2d-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="81a2d-117">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="81a2d-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="81a2d-118">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="81a2d-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="81a2d-119">Lauke Segmentas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="81a2d-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="81a2d-120">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="81a2d-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="81a2d-121">Lauke Reikšmė nuo spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="81a2d-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="81a2d-122">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="81a2d-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="81a2d-123">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="81a2d-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="81a2d-124">Lauke Reikšmė iki spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="81a2d-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="81a2d-125">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="81a2d-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="81a2d-126">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="81a2d-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="81a2d-127">Registravimo apribojimų nustatymas</span><span class="sxs-lookup"><span data-stu-id="81a2d-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="81a2d-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="81a2d-128">Close the page.</span></span>
2. <span data-ttu-id="81a2d-129">Spustelėkite Registravimo apribojimai.</span><span class="sxs-lookup"><span data-stu-id="81a2d-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="81a2d-130">Dalyje Kaip norite nustatyti registravimo apribojimus pasirinkite Pagal vartotojo grupę.</span><span class="sxs-lookup"><span data-stu-id="81a2d-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="81a2d-131">Medyje patikrinkite „grupę, kuriai norite leisti registruoti šiam žurnalo pavadinimui.".</span><span class="sxs-lookup"><span data-stu-id="81a2d-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="81a2d-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="81a2d-132">Click OK.</span></span>


