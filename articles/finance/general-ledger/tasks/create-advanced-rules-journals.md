---
title: Kurti papildomas žurnalų taisykles
description: Ši procedūra padeda sukurti išplėstines žurnalų taisykles.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e61ed731c4040e7351e20421f6cf217ae9a4641d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222364"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="3ef42-103">Kurti papildomas žurnalų taisykles</span><span class="sxs-lookup"><span data-stu-id="3ef42-103">Create advanced rules for journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3ef42-104">Ši procedūra padeda sukurti išplėstines žurnalų taisykles.</span><span class="sxs-lookup"><span data-stu-id="3ef42-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="3ef42-105">Ji apima žurnalo valdymo ir vartotojo registravimo apribojimų nustatymą.</span><span class="sxs-lookup"><span data-stu-id="3ef42-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="3ef42-106">Šioje procedūroje naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="3ef42-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="3ef42-107">Žurnalo valdymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="3ef42-107">Set up journal control</span></span>
1. <span data-ttu-id="3ef42-108">**Naršymo sritis** eikite į **Moduliai > Bendroji didžioji knyga > Žurnalo sąranka > Žurnalų pavadinimai**.</span><span class="sxs-lookup"><span data-stu-id="3ef42-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="3ef42-109">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3ef42-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3ef42-110">**Veiksmų srityje** spustelėkite **Žurnalo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="3ef42-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="3ef42-111">„fastTab“ **Kurie sąskaitų tipai gali būti registruojami** spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="3ef42-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="3ef42-112">Lauke **Įmonės sąskaitos** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3ef42-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="3ef42-113">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3ef42-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="3ef42-114">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3ef42-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="3ef42-115">„fastTab“ **Kurios segmentų reikšmės tinka šiam žurnalui** spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="3ef42-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="3ef42-116">Lauke **Sąskaitos struktūra** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3ef42-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="3ef42-117">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3ef42-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="3ef42-118">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3ef42-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="3ef42-119">Lauke **Segmentas** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3ef42-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="3ef42-120">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3ef42-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="3ef42-121">Lauke **Nuo reikšmės** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3ef42-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="3ef42-122">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3ef42-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="3ef42-123">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3ef42-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="3ef42-124">Lauke **Iki reikšmės** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3ef42-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="3ef42-125">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3ef42-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="3ef42-126">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3ef42-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="3ef42-127">Registravimo apribojimų nustatymas</span><span class="sxs-lookup"><span data-stu-id="3ef42-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="3ef42-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3ef42-128">Close the page.</span></span>
2. <span data-ttu-id="3ef42-129">Spustelėkite **Registravimo apribojimai**.</span><span class="sxs-lookup"><span data-stu-id="3ef42-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="3ef42-130">Lauke **Kaip norite nustatyti registravimo apribojimus** pažymėkite Pagal vartotojų grupę.</span><span class="sxs-lookup"><span data-stu-id="3ef42-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="3ef42-131">Medyje patikrinkite „grupę, kuriai norite leisti registruoti šiam žurnalo pavadinimui.".</span><span class="sxs-lookup"><span data-stu-id="3ef42-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="3ef42-132">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3ef42-132">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]