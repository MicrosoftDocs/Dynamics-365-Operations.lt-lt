--- 
title: " Apibrėžti skambučių centro kanalą ir kanalo atributus"
description: "Ši procedūra padeda kurti naują mažmenos kanalą ir apibrėžti kanalo atributus."
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 1418f04d8fb4d05756ac7a5f4b92a1950037be1d
ms.contentlocale: lt-lt
ms.lasthandoff: 02/07/2018

---
# <a name="define-call-center-channel-and-channel-attributes"></a><span data-ttu-id="bba7b-103"> Apibrėžti skambučių centro kanalą ir kanalo atributus</span><span class="sxs-lookup"><span data-stu-id="bba7b-103">Define call center channel and channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="bba7b-104">Ši procedūra padeda kurti naują mažmenos kanalą ir apibrėžti kanalo atributus.</span><span class="sxs-lookup"><span data-stu-id="bba7b-104">This procedure walks through creating a new retail channel and defining channel attributes.</span></span> <span data-ttu-id="bba7b-105">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USRT.</span><span class="sxs-lookup"><span data-stu-id="bba7b-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="bba7b-106">Ši procedūra yra skirta mažmenos IT vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="bba7b-106">This procedure is intended for the Retail IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="bba7b-107">Kurkite naują saugyklą</span><span class="sxs-lookup"><span data-stu-id="bba7b-107">Create new store</span></span>
1. <span data-ttu-id="bba7b-108">Eikite į Visas darbo sritys > Kanalo diegimas.</span><span class="sxs-lookup"><span data-stu-id="bba7b-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="bba7b-109">Spustelėkite Naujas kanalas.</span><span class="sxs-lookup"><span data-stu-id="bba7b-109">Click New channel.</span></span>
3. <span data-ttu-id="bba7b-110">Spustelėkite Saugykla.</span><span class="sxs-lookup"><span data-stu-id="bba7b-110">Click Store.</span></span>
4. <span data-ttu-id="bba7b-111">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bba7b-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="bba7b-112">Lauke Saugyklos numeris įrašykite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bba7b-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="bba7b-113">Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="bba7b-114">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="bba7b-115">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bba7b-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="bba7b-116">Lauke Saugojimo laiko juosta pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="bba7b-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="bba7b-117">Lauke Kanalo profilis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="bba7b-118">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bba7b-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="bba7b-119">Lauke Kalba spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="bba7b-120">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="bba7b-121">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bba7b-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="bba7b-122">Lauke PVM grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="bba7b-123">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="bba7b-124">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bba7b-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="bba7b-125">Lauke Kliento adresų knygelė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bba7b-126">Pasirinkite adresų knygelę, naudojamą klientams susieti su šia saugykla.</span><span class="sxs-lookup"><span data-stu-id="bba7b-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="bba7b-127">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="bba7b-128">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bba7b-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="bba7b-129">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="bba7b-129">Click Select.</span></span>
22. <span data-ttu-id="bba7b-130">Lauke Darbuotojo adresų knygelė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bba7b-131">Pasirinkite adresų knygelę, naudojamą kasininkams susieti su šiuo kanalu.</span><span class="sxs-lookup"><span data-stu-id="bba7b-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="bba7b-132">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="bba7b-133">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bba7b-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="bba7b-134">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="bba7b-134">Click Select.</span></span>
26. <span data-ttu-id="bba7b-135">Lauke Numatytasis klientas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="bba7b-136">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bba7b-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="bba7b-137">Išplėskite arba sutraukite sekciją Ekrano išdėstymas.</span><span class="sxs-lookup"><span data-stu-id="bba7b-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="bba7b-138">Lauke Ekrano išdėstymo ID spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bba7b-139">Pasirinkite numatytąjį EKA ekrano maketą šiai parduotuvei.</span><span class="sxs-lookup"><span data-stu-id="bba7b-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="bba7b-140">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="bba7b-141">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bba7b-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="bba7b-142">Veiksmų srityje spustelėkite Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="bba7b-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="bba7b-143">Spustelėkite Kanalo atributai.</span><span class="sxs-lookup"><span data-stu-id="bba7b-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="bba7b-144">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bba7b-144">Click New.</span></span>
35. <span data-ttu-id="bba7b-145">Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="bba7b-146">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="bba7b-147">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bba7b-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="bba7b-148">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bba7b-148">Click Save.</span></span>
39. <span data-ttu-id="bba7b-149">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bba7b-149">Close the page.</span></span>
40. <span data-ttu-id="bba7b-150">Veiksmų srityje spustelėkite Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="bba7b-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="bba7b-151">Spustelėkite Mokėjimo būdai.</span><span class="sxs-lookup"><span data-stu-id="bba7b-151">Click Payment methods.</span></span>
42. <span data-ttu-id="bba7b-152">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bba7b-152">Click New.</span></span>
43. <span data-ttu-id="bba7b-153">Lauke Mokėjimo būdas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="bba7b-154">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bba7b-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="bba7b-155">Išplėskite arba sutraukite sekciją Registravimas.</span><span class="sxs-lookup"><span data-stu-id="bba7b-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="bba7b-156">Lauke Sąskaitos numeris nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="bba7b-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="bba7b-157">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bba7b-157">Click Save.</span></span>
48. <span data-ttu-id="bba7b-158">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bba7b-158">Close the page.</span></span>
49. <span data-ttu-id="bba7b-159">Veiksmų srityje spustelėkite Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="bba7b-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="bba7b-160">Spustelėkite Grynųjų pinigų deklaravimas.</span><span class="sxs-lookup"><span data-stu-id="bba7b-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="bba7b-161">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bba7b-161">Click New.</span></span>
52. <span data-ttu-id="bba7b-162">Lauke Suma operacijos valiuta įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="bba7b-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="bba7b-163">Lauke Valiuta spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="bba7b-164">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="bba7b-165">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bba7b-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="bba7b-166">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bba7b-166">Click Save.</span></span>
57. <span data-ttu-id="bba7b-167">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bba7b-167">Close the page.</span></span>
58. <span data-ttu-id="bba7b-168">Veiksmų srityje spustelėkite Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="bba7b-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="bba7b-169">Spustelėkite Saugyklos lokatorių grupės priskyrimas.</span><span class="sxs-lookup"><span data-stu-id="bba7b-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="bba7b-170">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bba7b-170">Click New.</span></span>
61. <span data-ttu-id="bba7b-171">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bba7b-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="bba7b-172">Lauke Lokatorių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="bba7b-173">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bba7b-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="bba7b-174">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bba7b-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="bba7b-175">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bba7b-175">Click Save.</span></span>
66. <span data-ttu-id="bba7b-176">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bba7b-176">Close the page.</span></span>


