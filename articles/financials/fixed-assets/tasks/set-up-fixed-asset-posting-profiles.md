--- 
title: "Ilgalaikio turto registravimo šablonų nustatymas"
description: "Šis užduočių vadovas nustatys ilgalaikio turto registravimo šablonus."
author: saraschi2
manager: AnnBe
ms.date: 02/24/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: dd4c2d67188b6c2c34f9046a6388de292d6c291e
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="d3d68-103">Ilgalaikio turto registravimo šablonų nustatymas</span><span class="sxs-lookup"><span data-stu-id="d3d68-103">Set up fixed asset posting profiles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d3d68-104">Šis užduočių vadovas nustatys ilgalaikio turto registravimo šablonus.</span><span class="sxs-lookup"><span data-stu-id="d3d68-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="d3d68-105">Jis naudoja vaidmenį Buhalteris ir USMF juridinio subjekto demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="d3d68-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="d3d68-106">Užduočių vadove pateikiami pagrindinio registravimo šablono pavyzdžiai, nors reikia sukurti jūsų konkretaus sąskaitų plano ir finansinių ataskaitų reikalavimų registravimo šablonus.</span><span class="sxs-lookup"><span data-stu-id="d3d68-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="d3d68-107">Pasirinkite Ilgalaikis turtas > Sąranka > Ilgalaikio turto registravimo šablonai.</span><span class="sxs-lookup"><span data-stu-id="d3d68-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="d3d68-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="d3d68-108">Click New.</span></span>
3. <span data-ttu-id="d3d68-109">Lauke Registravimo šablonas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="d3d68-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="d3d68-111">Turėsite sukurti kiekvieno ilgalaikio turto operacijos tipo, kurį naudosite dirbdami su ilgalaikiu turtu, registravimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="d3d68-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="d3d68-112">Šis užduočių vadovas pradės nuo įsigijimo operacijos tipo.</span><span class="sxs-lookup"><span data-stu-id="d3d68-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="d3d68-113">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-113">Click Add.</span></span>
6. <span data-ttu-id="d3d68-114">Lauke Knyga įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="d3d68-115">Laukas Grupavimai leidžia registravimo šabloną apibrėžti iki lentelės (kiekvienam ilgalaikiam turtui nustatyta po vieną sąskaitą) arba grupės (kiekvienai ilgalaikio turto grupei nustatyta po vieną sąskaitą).</span><span class="sxs-lookup"><span data-stu-id="d3d68-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="d3d68-116">Šiame užduočių vadove reikšmę paliksiu nustatytą į „Visi”, kad būtų taikoma visam ilgalaikiam turtui su nurodyta knyga.</span><span class="sxs-lookup"><span data-stu-id="d3d68-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="d3d68-117">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="d3d68-118">Lauke Įsigijimai galite įvesti korespondentinę sąskaitą arba jį palikti tuščią, kad būtų galima užpildyti atliekant konkrečią operaciją.</span><span class="sxs-lookup"><span data-stu-id="d3d68-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="d3d68-119">Lauke Operacijos tipas pasirinkite „Įsigijimo koregavimas‟.</span><span class="sxs-lookup"><span data-stu-id="d3d68-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="d3d68-120">Atlikdami įsigijimo koregavimo operacijas, naudojame tas pačias sąskaitas, kurios buvo naudojamos atliekant įsigijimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="d3d68-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="d3d68-121">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-121">Click Add.</span></span>
10. <span data-ttu-id="d3d68-122">Lauke Knyga įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="d3d68-123">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="d3d68-124">Lauke Įsigijimų koregavimai galite įvesti korespondentinę sąskaitą arba jį palikti tuščią, kad būtų galima užpildyti atliekant konkrečią operaciją.</span><span class="sxs-lookup"><span data-stu-id="d3d68-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="d3d68-125">Lauke Operacijos tipas pasirinkite „Nusidėvėjimas‟.</span><span class="sxs-lookup"><span data-stu-id="d3d68-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="d3d68-126">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-126">Click Add.</span></span>
14. <span data-ttu-id="d3d68-127">Lauke Knyga įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="d3d68-128">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="d3d68-129">Lauke Korespondentinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="d3d68-130">Lauke Operacijos tipas pasirinkite „Nusidėvėjimo koregavimas‟.</span><span class="sxs-lookup"><span data-stu-id="d3d68-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="d3d68-131">Atlikdami nusidėvėjimo koregavimo operacijas, naudojame tas pačias sąskaitas, kurios buvo naudojamos atliekant nusidėvėjimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="d3d68-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="d3d68-132">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-132">Click Add.</span></span>
19. <span data-ttu-id="d3d68-133">Lauke Knyga įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="d3d68-134">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="d3d68-135">Lauke Korespondentinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="d3d68-136">Lauke Operacijos tipas pasirinkite „Likvidavimas – pardavimas‟.</span><span class="sxs-lookup"><span data-stu-id="d3d68-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="d3d68-137">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-137">Click Add.</span></span>
24. <span data-ttu-id="d3d68-138">Lauke Knyga įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="d3d68-139">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="d3d68-140">Lauke Likvidavimai galite įvesti korespondentinę sąskaitą arba jį palikti tuščią, kad būtų galima užpildyti atliekant konkrečią operaciją.</span><span class="sxs-lookup"><span data-stu-id="d3d68-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="d3d68-141">Lauke Operacijos tipas pasirinkite „Likvidavimas – nurašymas‟.</span><span class="sxs-lookup"><span data-stu-id="d3d68-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="d3d68-142">Likvidavimui parduoti ir likvidavimui nurašyti naudosime tas pačias sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="d3d68-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="d3d68-143">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-143">Click Add.</span></span>
28. <span data-ttu-id="d3d68-144">Lauke Knyga įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="d3d68-145">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="d3d68-146">Lauke Likvidavimai galite įvesti korespondentinę sąskaitą arba jį palikti tuščią, kad būtų galima užpildyti atliekant konkrečią operaciją.</span><span class="sxs-lookup"><span data-stu-id="d3d68-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="d3d68-147">Išplėskite dalį Likvidavimas.</span><span class="sxs-lookup"><span data-stu-id="d3d68-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="d3d68-148">Turite nustatyti likvidavimo registravimo šablonus, skirtus tiek likvidavimui parduoti, tiek nurašyti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="d3d68-149">Prasidėsime nuo likvidavimo pardavimo operacijų.</span><span class="sxs-lookup"><span data-stu-id="d3d68-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="d3d68-150">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-150">Click Add.</span></span>
32. <span data-ttu-id="d3d68-151">Lauke Knyga įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="d3d68-152">Lauke Registruoti vertę pasirinkite „Įsigijimo vertė‟.</span><span class="sxs-lookup"><span data-stu-id="d3d68-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="d3d68-153">Įsigijimo reikšmė palies kiekvienų metų įsigijimo ir įsigijimo koregavimo reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="d3d68-154">Šių operacijų tipų sąskaitas taip pat galite apibrėžti atskirai.</span><span class="sxs-lookup"><span data-stu-id="d3d68-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="d3d68-155">Galite nustatyti, kad likvidavimo procesas naudotų skirtingas sąskaitas – tai priklausytų nuo to, ar likvidavimo rezultatas – pelnas, ar – nuostolis.</span><span class="sxs-lookup"><span data-stu-id="d3d68-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="d3d68-156">Pardavimo vertės tipą nustatysiu į „Visi‟, kad tos pačios sąskaitos būtų naudojamos visiems likvidavimų tipams.</span><span class="sxs-lookup"><span data-stu-id="d3d68-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="d3d68-157">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="d3d68-158">Lauke Korespondentinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="d3d68-159">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-159">Click Add.</span></span>
37. <span data-ttu-id="d3d68-160">Lauke Knyga įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="d3d68-161">Lauke Registruoti vertę pasirinkite „Nusidėvėjimas (ankstesniais metais)‟.</span><span class="sxs-lookup"><span data-stu-id="d3d68-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="d3d68-162">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="d3d68-163">Lauke Korespondentinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="d3d68-164">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-164">Click Add.</span></span>
41. <span data-ttu-id="d3d68-165">Lauke Knyga įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="d3d68-166">Lauke Registruoti vertę pasirinkite „Nusidėvėjimas (šiais metais)‟.</span><span class="sxs-lookup"><span data-stu-id="d3d68-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="d3d68-167">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="d3d68-168">Lauke Korespondentinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="d3d68-169">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-169">Click Add.</span></span>
46. <span data-ttu-id="d3d68-170">Lauke Knyga įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="d3d68-171">Lauke Registruoti vertę pasirinkite „Nusidėvėjimo koregavimai (ankstesniais metais)‟.</span><span class="sxs-lookup"><span data-stu-id="d3d68-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="d3d68-172">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="d3d68-173">Lauke Korespondentinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="d3d68-174">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-174">Click Add.</span></span>
51. <span data-ttu-id="d3d68-175">Lauke Knyga įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="d3d68-176">Lauke Registruoti vertę pasirinkite „Nusidėvėjimo koregavimai (šiais metais)‟.</span><span class="sxs-lookup"><span data-stu-id="d3d68-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="d3d68-177">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="d3d68-178">Lauke Korespondentinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="d3d68-179">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-179">Click Add.</span></span>
56. <span data-ttu-id="d3d68-180">Lauke Knyga įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="d3d68-181">Lauke Registruoti vertę pasirinkite „Balansinė vertė‟.</span><span class="sxs-lookup"><span data-stu-id="d3d68-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="d3d68-182">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="d3d68-183">Lauke Korespondentinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="d3d68-184">Lauke Pardavimas arba nurašymas pasirinkite „Nurašymas“.</span><span class="sxs-lookup"><span data-stu-id="d3d68-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="d3d68-185">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-185">Click Add.</span></span>
62. <span data-ttu-id="d3d68-186">Lauke Knyga įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="d3d68-187">Lauke Registruoti vertę pasirinkite „Įsigijimo vertė‟.</span><span class="sxs-lookup"><span data-stu-id="d3d68-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="d3d68-188">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="d3d68-189">Lauke Korespondentinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="d3d68-190">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-190">Click Add.</span></span>
67. <span data-ttu-id="d3d68-191">Lauke Knyga įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="d3d68-192">Lauke Registruoti vertę pasirinkite „Nusidėvėjimas (ankstesniais metais)‟.</span><span class="sxs-lookup"><span data-stu-id="d3d68-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="d3d68-193">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="d3d68-194">Lauke Korespondentinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="d3d68-195">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-195">Click Add.</span></span>
71. <span data-ttu-id="d3d68-196">Lauke Knyga įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="d3d68-197">Lauke Registruoti vertę pasirinkite „Nusidėvėjimas (šiais metais)‟.</span><span class="sxs-lookup"><span data-stu-id="d3d68-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="d3d68-198">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="d3d68-199">Lauke Korespondentinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="d3d68-200">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-200">Click Add.</span></span>
76. <span data-ttu-id="d3d68-201">Lauke Knyga įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="d3d68-202">Lauke Registruoti vertę pasirinkite „Nusidėvėjimo koregavimai (ankstesniais metais)‟.</span><span class="sxs-lookup"><span data-stu-id="d3d68-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="d3d68-203">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="d3d68-204">Lauke Korespondentinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="d3d68-205">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-205">Click Add.</span></span>
81. <span data-ttu-id="d3d68-206">Lauke Knyga įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="d3d68-207">Lauke Registruoti vertę pasirinkite „Nusidėvėjimo koregavimai (šiais metais)‟.</span><span class="sxs-lookup"><span data-stu-id="d3d68-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="d3d68-208">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="d3d68-209">Lauke Korespondentinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="d3d68-210">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d3d68-210">Click Add.</span></span>
86. <span data-ttu-id="d3d68-211">Lauke Knyga įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d3d68-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="d3d68-212">Lauke Registruoti vertę pasirinkite „Balansinė vertė‟.</span><span class="sxs-lookup"><span data-stu-id="d3d68-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="d3d68-213">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="d3d68-214">Lauke Korespondentinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d3d68-214">In the Offset account field, specify the desired values.</span></span>


