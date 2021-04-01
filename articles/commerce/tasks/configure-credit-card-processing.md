---
title: " Konfigūruoti kredito kortelės apdorojimą"
description: Ši procedūra padeda peržiūrėti mokėjimo paslaugų teikėjų sąrašą ir konfigūruoti gautinų sumų mokėjimo sąskaitą.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d365dfce8e8fbd332111d96eeb2a431151d7a342
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234226"
---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="7acfc-103"> Konfigūruoti kredito kortelės apdorojimą</span><span class="sxs-lookup"><span data-stu-id="7acfc-103">Configure credit card processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7acfc-104">Ši procedūra padeda peržiūrėti mokėjimo paslaugų teikėjų sąrašą ir konfigūruoti gautinų sumų mokėjimo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="7acfc-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="7acfc-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT, ir ji yra skirta administratoriams ir IT specialistams.</span><span class="sxs-lookup"><span data-stu-id="7acfc-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="7acfc-106">Mokėjimo paslaugų teikėjų sąrašo peržiūra</span><span class="sxs-lookup"><span data-stu-id="7acfc-106">View a list of payment providers</span></span>
1. <span data-ttu-id="7acfc-107">Pasirinkite Gautinos sumos > Mokėjimų sąranka > Mokėjimo tarnybos.</span><span class="sxs-lookup"><span data-stu-id="7acfc-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="7acfc-108">Spustelėkite Peržiūrėti galimus teikėjus.</span><span class="sxs-lookup"><span data-stu-id="7acfc-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="7acfc-109">Sukonfigūruoti mokėjimo sąskaitas</span><span class="sxs-lookup"><span data-stu-id="7acfc-109">Configure payment account</span></span>
1. <span data-ttu-id="7acfc-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="7acfc-110">Click New.</span></span>
2. <span data-ttu-id="7acfc-111">Lauke Mokėjimo tarnyba įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7acfc-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="7acfc-112">Lauke Mokėjimo jungtis pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="7acfc-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="7acfc-113">Perjunkite sekcijos Mokėjimo sąskaitos suma išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="7acfc-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="7acfc-114">Lauke Aplinka: įveskite „PROD“.</span><span class="sxs-lookup"><span data-stu-id="7acfc-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="7acfc-115">Spustelėkite Kredito kortelių tipai.</span><span class="sxs-lookup"><span data-stu-id="7acfc-115">Click Credit card types.</span></span>
7. <span data-ttu-id="7acfc-116">Lauke Mokėjimo žurnalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="7acfc-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="7acfc-117">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7acfc-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="7acfc-118">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="7acfc-118">Click Add.</span></span>
10. <span data-ttu-id="7acfc-119">Lauke Valiuta surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7acfc-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="7acfc-120">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="7acfc-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="7acfc-121">Lauke Mokėjimo žurnalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="7acfc-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="7acfc-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7acfc-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="7acfc-123">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="7acfc-123">Click Add.</span></span>
15. <span data-ttu-id="7acfc-124">Lauke Valiuta surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7acfc-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="7acfc-125">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="7acfc-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7acfc-126">Galite pakartotinai taikyti šiuos veiksmus visų kitų tipų kortelėms.</span><span class="sxs-lookup"><span data-stu-id="7acfc-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="7acfc-127">Lauke Mokėjimo žurnalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="7acfc-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="7acfc-128">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7acfc-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="7acfc-129">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="7acfc-129">Click Add.</span></span>
20. <span data-ttu-id="7acfc-130">Lauke Valiuta surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7acfc-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="7acfc-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="7acfc-131">Click Save.</span></span>
22. <span data-ttu-id="7acfc-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7acfc-132">Close the page.</span></span>
23. <span data-ttu-id="7acfc-133">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="7acfc-133">Click Validate.</span></span>
24. <span data-ttu-id="7acfc-134">Spustelėkite žymės langelį Numatytasis naujų kredito kortelių procesorius.</span><span class="sxs-lookup"><span data-stu-id="7acfc-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="7acfc-135">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="7acfc-135">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]