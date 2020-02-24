---
title: Mažmeninės prekybos kanalų finansinių dimensijų kūrimas ir dimensijų reikšmių parduotuvėse konfigūravimas
description: Ši procedūra padeda kurti prekybos kanalo finansinę dimensiją su dimensijų reikšmėmis ir nurodo parduotuvių finansinių dimensijų reikšmių konfigūravimo veiksmus.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 79abb6875e2f5b101410ca004b525c4b881621a2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023419"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="03294-103">Mažmeninės prekybos kanalų finansinių dimensijų kūrimas ir dimensijų reikšmių parduotuvėse konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="03294-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="03294-104">Ši procedūra padeda kurti prekybos kanalo finansinę dimensiją su dimensijų reikšmėmis ir nurodo parduotuvių finansinių dimensijų reikšmių konfigūravimo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="03294-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="03294-105">Ši tema neapima kitų susijusių veiksmų, pavyzdžiui, dimensijų rinkinių ir sąskaitų struktūrų kūrimo.</span><span class="sxs-lookup"><span data-stu-id="03294-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="03294-106">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="03294-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="03294-107">Eikite į Didžioji knyga > Sąskaitų planas > Dimensijos > Finansinės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="03294-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="03294-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="03294-108">Click New.</span></span>
3. <span data-ttu-id="03294-109">Lauke Naudoti vertes iš pasirinkite „Prekybos kanalai“.</span><span class="sxs-lookup"><span data-stu-id="03294-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="03294-110">Lauke Dimensijos pavadinimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="03294-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="03294-111">Spustelėkite Aktyvinti.</span><span class="sxs-lookup"><span data-stu-id="03294-111">Click Activate.</span></span>
6. <span data-ttu-id="03294-112">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="03294-112">Click Close.</span></span>
7. <span data-ttu-id="03294-113">Spustelėkite Aktyvinti.</span><span class="sxs-lookup"><span data-stu-id="03294-113">Click Activate.</span></span>
8. <span data-ttu-id="03294-114">Spustelėkite Dimensijos reikšmės.</span><span class="sxs-lookup"><span data-stu-id="03294-114">Click Dimension values.</span></span>
9. <span data-ttu-id="03294-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="03294-115">Close the page.</span></span>
10. <span data-ttu-id="03294-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="03294-116">Click Save.</span></span>
11. <span data-ttu-id="03294-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="03294-117">Close the page.</span></span>
12. <span data-ttu-id="03294-118">Eikite į „Retail and Commerce“ > Kanalai > Parduotuvės > Visos parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="03294-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="03294-119">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="03294-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="03294-120">Perjunkite skyriaus „Finansinės dimensijos“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="03294-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="03294-121">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="03294-121">Click Edit.</span></span>
16. <span data-ttu-id="03294-122">Lauke Prekybos kanalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="03294-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="03294-123">Sąraše raskite ir pasirinkite naujinamos parduotuvės dimensijos reikšmę.</span><span class="sxs-lookup"><span data-stu-id="03294-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="03294-124">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="03294-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="03294-125">Lauke „CostCenter“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="03294-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="03294-126">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="03294-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="03294-127">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="03294-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="03294-128">Lauke Skyrius spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="03294-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="03294-129">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="03294-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="03294-130">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="03294-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="03294-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="03294-131">Click Save.</span></span>

