---
title: Kurti viešojo sektoriaus pradinį biudžetą ir tada atšaukti preliminaraus biudžeto įrašus
description: Kai sukuriate pradinio biudžeto įrašą ir naudojate biudžeto modelį ir dimensijų reikšmes, kuriuose yra preliminaraus biudžeto sumos, jas galima atšaukti.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32d89216d49a743729de8910f738276cbddcd8bb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446085"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="0a8ed-103">Kurti viešojo sektoriaus pradinį biudžetą ir tada atšaukti preliminaraus biudžeto įrašus</span><span class="sxs-lookup"><span data-stu-id="0a8ed-103">Create an original budget and then reverse preliminary budget entries in the public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a8ed-104">Kai sukuriate pradinio biudžeto įrašą ir naudojate biudžeto modelį ir dimensijų reikšmes, kuriuose yra preliminaraus biudžeto sumos, jas galima atšaukti.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="0a8ed-105">Ši procedūra buvo sukurta naudojant demonstracinės įmonės PSUS duomenis viešajame sektorių skaidinyje.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="0a8ed-106">Pasirinkite Biudžeto sudarymas > Biudžeto registro įrašai.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="0a8ed-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-107">Click New.</span></span>
3. <span data-ttu-id="0a8ed-108">Lauke Biudžeto modelis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0a8ed-109">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="0a8ed-110">Lauke Biudžeto kodas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0a8ed-111">Sąraše spustelėkite Pradinis biudžetas.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="0a8ed-112">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-112">Click Save.</span></span>
8. <span data-ttu-id="0a8ed-113">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-113">Click Add line.</span></span>
9. <span data-ttu-id="0a8ed-114">Pasirinktina: jei norite pakeisti antraštės datą, įveskite naują datą.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="0a8ed-115">Ši data lemia finansinį laikotarpį, kuriam bus įrašytas biudžetas.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="0a8ed-116">Lauke Sąskaitos struktūra spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="0a8ed-117">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="0a8ed-118">Lauke Dimensijų reikšmės nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="0a8ed-119">Lauke Suma įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="0a8ed-120">Lauke Valiuta spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="0a8ed-121">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="0a8ed-122">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-122">Click Save.</span></span>
17. <span data-ttu-id="0a8ed-123">Spustelėkite Atnaujinti biudžetų balansus.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="0a8ed-124">Pasirinktina: galite pasirinkti parinktį Atšaukti preliminarų biudžetą.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="0a8ed-125">Įsidėmėkite, kad galite atšaukti visus preliminaraus biudžeto įrašus arba tik jūsų nurodyto biudžeto kodo preliminaraus biudžeto įrašus.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="0a8ed-126">Norėdami pasirinkti konkrečias parinktis, puslapio viršuje spustelėkite piktogramą Atrakinti.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="0a8ed-127">Spustelėkite Naujinti.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-127">Click Update.</span></span>

