---
title: Skambučių centro kanalų kūrimas ir kanalo atributų nustatymas
description: Ši procedūra padeda kurti naują kanalą ir apibrėžti kanalo atributus.
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2f99029195a8b783f0d12990d4e8bab0bb348d7
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140963"
---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="2bd43-103">Skambučių centro kanalų kūrimas ir kanalo atributų nustatymas</span><span class="sxs-lookup"><span data-stu-id="2bd43-103">Create call center channels and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2bd43-104">Ši procedūra padeda kurti naują prekybos kanalą ir apibrėžti kanalo atributus.</span><span class="sxs-lookup"><span data-stu-id="2bd43-104">This procedure walks through creating a new commerce channel and defining channel attributes.</span></span> <span data-ttu-id="2bd43-105">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USRT.</span><span class="sxs-lookup"><span data-stu-id="2bd43-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="2bd43-106">Ši procedūra yra skirta prekybos IT vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="2bd43-106">This procedure is intended for the Commerce IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="2bd43-107">Kurkite naują saugyklą</span><span class="sxs-lookup"><span data-stu-id="2bd43-107">Create new store</span></span>
1. <span data-ttu-id="2bd43-108">Eikite į Visas darbo sritys > Kanalo diegimas.</span><span class="sxs-lookup"><span data-stu-id="2bd43-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="2bd43-109">Spustelėkite Naujas kanalas.</span><span class="sxs-lookup"><span data-stu-id="2bd43-109">Click New channel.</span></span>
3. <span data-ttu-id="2bd43-110">Spustelėkite Saugykla.</span><span class="sxs-lookup"><span data-stu-id="2bd43-110">Click Store.</span></span>
4. <span data-ttu-id="2bd43-111">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2bd43-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="2bd43-112">Lauke Saugyklos numeris įrašykite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2bd43-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="2bd43-113">Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="2bd43-114">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="2bd43-115">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2bd43-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="2bd43-116">Lauke Saugojimo laiko juosta pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="2bd43-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="2bd43-117">Lauke Kanalo profilis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="2bd43-118">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2bd43-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="2bd43-119">Lauke Kalba spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="2bd43-120">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="2bd43-121">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2bd43-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="2bd43-122">Lauke PVM grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="2bd43-123">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="2bd43-124">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2bd43-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="2bd43-125">Lauke Kliento adresų knygelė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2bd43-126">Pasirinkite adresų knygelę, naudojamą klientams susieti su šia saugykla.</span><span class="sxs-lookup"><span data-stu-id="2bd43-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="2bd43-127">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="2bd43-128">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2bd43-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="2bd43-129">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="2bd43-129">Click Select.</span></span>
22. <span data-ttu-id="2bd43-130">Lauke Darbuotojo adresų knygelė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2bd43-131">Pasirinkite adresų knygelę, naudojamą kasininkams susieti su šiuo kanalu.</span><span class="sxs-lookup"><span data-stu-id="2bd43-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="2bd43-132">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="2bd43-133">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2bd43-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="2bd43-134">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="2bd43-134">Click Select.</span></span>
26. <span data-ttu-id="2bd43-135">Lauke Numatytasis klientas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="2bd43-136">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2bd43-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="2bd43-137">Išplėskite arba sutraukite sekciją Ekrano išdėstymas.</span><span class="sxs-lookup"><span data-stu-id="2bd43-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="2bd43-138">Lauke Ekrano išdėstymo ID spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2bd43-139">Pasirinkite numatytąjį EKA ekrano maketą šiai parduotuvei.</span><span class="sxs-lookup"><span data-stu-id="2bd43-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="2bd43-140">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="2bd43-141">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2bd43-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="2bd43-142">Veiksmų srityje spustelėkite Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="2bd43-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="2bd43-143">Spustelėkite Kanalo atributai.</span><span class="sxs-lookup"><span data-stu-id="2bd43-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="2bd43-144">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="2bd43-144">Click New.</span></span>
35. <span data-ttu-id="2bd43-145">Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="2bd43-146">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="2bd43-147">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2bd43-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="2bd43-148">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="2bd43-148">Click Save.</span></span>
39. <span data-ttu-id="2bd43-149">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2bd43-149">Close the page.</span></span>
40. <span data-ttu-id="2bd43-150">Veiksmų srityje spustelėkite Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="2bd43-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="2bd43-151">Spustelėkite Mokėjimo būdai.</span><span class="sxs-lookup"><span data-stu-id="2bd43-151">Click Payment methods.</span></span>
42. <span data-ttu-id="2bd43-152">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="2bd43-152">Click New.</span></span>
43. <span data-ttu-id="2bd43-153">Lauke Mokėjimo būdas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="2bd43-154">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2bd43-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="2bd43-155">Išplėskite arba sutraukite sekciją Registravimas.</span><span class="sxs-lookup"><span data-stu-id="2bd43-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="2bd43-156">Lauke Sąskaitos numeris nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="2bd43-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="2bd43-157">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="2bd43-157">Click Save.</span></span>
48. <span data-ttu-id="2bd43-158">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2bd43-158">Close the page.</span></span>
49. <span data-ttu-id="2bd43-159">Veiksmų srityje spustelėkite Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="2bd43-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="2bd43-160">Spustelėkite Grynųjų pinigų deklaravimas.</span><span class="sxs-lookup"><span data-stu-id="2bd43-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="2bd43-161">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="2bd43-161">Click New.</span></span>
52. <span data-ttu-id="2bd43-162">Lauke Suma operacijos valiuta įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="2bd43-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="2bd43-163">Lauke Valiuta spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="2bd43-164">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="2bd43-165">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2bd43-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="2bd43-166">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="2bd43-166">Click Save.</span></span>
57. <span data-ttu-id="2bd43-167">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2bd43-167">Close the page.</span></span>
58. <span data-ttu-id="2bd43-168">Veiksmų srityje spustelėkite Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="2bd43-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="2bd43-169">Spustelėkite Saugyklos lokatorių grupės priskyrimas.</span><span class="sxs-lookup"><span data-stu-id="2bd43-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="2bd43-170">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="2bd43-170">Click New.</span></span>
61. <span data-ttu-id="2bd43-171">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="2bd43-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="2bd43-172">Lauke Lokatorių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="2bd43-173">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="2bd43-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="2bd43-174">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2bd43-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="2bd43-175">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="2bd43-175">Click Save.</span></span>
66. <span data-ttu-id="2bd43-176">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2bd43-176">Close the page.</span></span>

