---
title: " Nustatyti lojalumo programas"
description: Ši procedūra padeda nustatyti lojalumo programą su dviem lojalumo pakopomis.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
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
ms.openlocfilehash: b178f1c6a71b34b70db4dbcd1765117215a4d2a1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023408"
---
# <a name="define-loyalty-programs"></a><span data-ttu-id="087d8-103"> Nustatyti lojalumo programas</span><span class="sxs-lookup"><span data-stu-id="087d8-103">Define loyalty programs</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="087d8-104">Ši procedūra padeda nustatyti lojalumo programą su dviem lojalumo pakopomis.</span><span class="sxs-lookup"><span data-stu-id="087d8-104">This procedure shows how to set up a loyalty program with two loyalty tiers.</span></span> <span data-ttu-id="087d8-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="087d8-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="087d8-106">Eikite į Mažmeninė prekyba ir prekyba> ...</span><span class="sxs-lookup"><span data-stu-id="087d8-106">Go to Retail and Commerce > ..</span></span> <span data-ttu-id="087d8-107">> Lojalumo programos.</span><span class="sxs-lookup"><span data-stu-id="087d8-107">> Loyalty programs.</span></span>
2. <span data-ttu-id="087d8-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="087d8-108">Click New.</span></span>
3. <span data-ttu-id="087d8-109">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="087d8-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="087d8-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="087d8-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="087d8-111">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="087d8-111">Click Add line.</span></span>
6. <span data-ttu-id="087d8-112">Lauke Lygis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="087d8-112">In the Level field, enter a number.</span></span>
7. <span data-ttu-id="087d8-113">Lauke Pakopa įveskite lojalumo pakopos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="087d8-113">In the Tier field, enter a name for the loyalty tier.</span></span>
8. <span data-ttu-id="087d8-114">Lauke Aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="087d8-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="087d8-115">Lauke Datų intervalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="087d8-115">In the Date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="087d8-116">Šis datų intervalas turėtų apimti ateitį.</span><span class="sxs-lookup"><span data-stu-id="087d8-116">This date interval should extend into the future.</span></span> <span data-ttu-id="087d8-117">Pavyzdžiui, jei datų intervalas, pasirinktas aukso pakopai, yra vienerių metų laikotarpis, kiekvienas klientas, kuris patenka į aukso pakopą, gali gauti su ja susijusius atlygius vienerius metus.</span><span class="sxs-lookup"><span data-stu-id="087d8-117">For example, if the date interval that is selected for gold tier is a one-year period, any customer who qualifies for the gold tier can receive the rewards that are assigned to the gold tier for one year.</span></span> <span data-ttu-id="087d8-118">Jei klientui būnant aukso pakopoje ta pakopa jam priskiriama iš naujo, data, kada baigiasi pakopos galiojimas, pratęsiama dar metams, pradedant nuo tos dienos, kai pakopa buvo priskirta iš naujo.</span><span class="sxs-lookup"><span data-stu-id="087d8-118">If the customer re-qualifies for the gold tier while they are in the tier, the date that the tier expires is extended by another year from the date when they re-qualify.</span></span>  
10. <span data-ttu-id="087d8-119">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="087d8-119">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="087d8-120">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="087d8-120">Click Add line.</span></span>
12. <span data-ttu-id="087d8-121">Lauke Lygis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="087d8-121">In the Level field, enter a number.</span></span>
13. <span data-ttu-id="087d8-122">Lauke Pakopa įveskite lojalumo pakopos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="087d8-122">In the Tier field, enter a name for the loyalty tier.</span></span>
14. <span data-ttu-id="087d8-123">Lauke Aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="087d8-123">In the Description field, type a value.</span></span>
15. <span data-ttu-id="087d8-124">Lauke Datų intervalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="087d8-124">In the Date interval field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="087d8-125">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="087d8-125">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="087d8-126">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="087d8-126">Click Save.</span></span>
18. <span data-ttu-id="087d8-127">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="087d8-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="087d8-128">Pakopos taisyklės nurodo mažiausią atlygio taškų skaičių, kurį reikia surinkti per tam tikrą laikotarpį, norint pakopą priskirti.</span><span class="sxs-lookup"><span data-stu-id="087d8-128">Tier rules define the minimum number of a reward point needed to be earned during a time period to qualify for the tier.</span></span>  
19. <span data-ttu-id="087d8-129">Perjunkite sekcijos Pakopos taisyklės išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="087d8-129">Toggle the expansion of the Tier rules section.</span></span>
20. <span data-ttu-id="087d8-130">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="087d8-130">Click New.</span></span>
    * <span data-ttu-id="087d8-131">Vienai pakopai galite nustatyti daugiau nei vieną pakopos taisyklę.</span><span class="sxs-lookup"><span data-stu-id="087d8-131">You can have more than one tier rule per tier.</span></span> <span data-ttu-id="087d8-132">Pavyzdžiui, galite pasirinkti tris skirtingus kriterijus pakopai gauti: išleidžiant 500 JAV dolerių per mėnesį, išleidžiant 500 JAV dolerių per metus ir įvykdant 20 operacijų per metus.</span><span class="sxs-lookup"><span data-stu-id="087d8-132">For example, you could have three different criteria to earn a tier; by spending $500 in one month, by spending $1000 over one year, and by having 20 transactions in one year.</span></span> <span data-ttu-id="087d8-133">Norėdami tai padaryti, turėsite sukurti tris pakopos taisykles.</span><span class="sxs-lookup"><span data-stu-id="087d8-133">To do this, you would need to create three tier rules.</span></span>  
21. <span data-ttu-id="087d8-134">Lauke Atlygio taškas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="087d8-134">In the Reward point field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="087d8-135">Tai turėtų būti neišnaudojami atlygio už lojalumą taškai.</span><span class="sxs-lookup"><span data-stu-id="087d8-135">This should be a non-redeemable loyalty reward point.</span></span>  
22. <span data-ttu-id="087d8-136">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="087d8-136">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="087d8-137">Lauke Išduotų taškų minimumas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="087d8-137">In the Minimum issued points field, enter a number.</span></span>
    * <span data-ttu-id="087d8-138">Jei pakopa yra žemiausio lygio ir visi klientai gali ją gauti tiesiog dalyvaudami šioje programoje, įveskite „0“.</span><span class="sxs-lookup"><span data-stu-id="087d8-138">For the lowest level tier, if all customers qualify simply by participating in the program, enter '0'.</span></span>  
24. <span data-ttu-id="087d8-139">Lauke Vertinimo data spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="087d8-139">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="087d8-140">Šis datų intervalas turėtų apimti praeitį.</span><span class="sxs-lookup"><span data-stu-id="087d8-140">This date interval should extend into the past.</span></span> <span data-ttu-id="087d8-141">Tik šio datų intervalo metu gauti taškai bus įtraukiami skaičiuojant mažiausią išduotų taškų vertę.</span><span class="sxs-lookup"><span data-stu-id="087d8-141">Only points earned during this date interval will be counted towards reaching the minimum issued points value.</span></span>  
25. <span data-ttu-id="087d8-142">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="087d8-142">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="087d8-143">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="087d8-143">Click Save.</span></span>
27. <span data-ttu-id="087d8-144">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="087d8-144">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="087d8-145">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="087d8-145">Click New.</span></span>
29. <span data-ttu-id="087d8-146">Lauke Atlygio taškas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="087d8-146">In the Reward point field, click the drop-down button to open the lookup.</span></span>
30. <span data-ttu-id="087d8-147">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="087d8-147">In the list, click the link in the selected row.</span></span>
31. <span data-ttu-id="087d8-148">Lauke Išduotų taškų minimumas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="087d8-148">In the Minimum issued points field, enter a number.</span></span>
32. <span data-ttu-id="087d8-149">Lauke Vertinimo data spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="087d8-149">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="087d8-150">Šis datų intervalas turėtų apimti praeitį.</span><span class="sxs-lookup"><span data-stu-id="087d8-150">This date interval should extend into the past.</span></span>  
33. <span data-ttu-id="087d8-151">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="087d8-151">In the list, click the link in the selected row.</span></span>
34. <span data-ttu-id="087d8-152">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="087d8-152">Click Save.</span></span>
35. <span data-ttu-id="087d8-153">Spustelėkite Kainų grupės.</span><span class="sxs-lookup"><span data-stu-id="087d8-153">Click Price groups.</span></span>
    * <span data-ttu-id="087d8-154">Jei lojaliems klientams norite suteikti nuolaidas.</span><span class="sxs-lookup"><span data-stu-id="087d8-154">If you want to give loyalty customers discounts.</span></span> <span data-ttu-id="087d8-155">vieną arba daugiau kainų grupių turėsite priskirti lojalumo programai ir priskirti kainų grupes nuolaidoms.</span><span class="sxs-lookup"><span data-stu-id="087d8-155">you'll need to assign one or more price groups to the loyalty program and assign the price groups to discounts.</span></span> <span data-ttu-id="087d8-156">Rekomenduojama nenaudoti kainų grupių skirtingų tipų nuolaidų objektams.</span><span class="sxs-lookup"><span data-stu-id="087d8-156">It is a best practice to not mix price groups across different types of discounting entities.</span></span>  <span data-ttu-id="087d8-157">Pavyzdžiui, nenaudokite tos pačios kainų grupės lojalumo nuolaidai ir kanalo nuolaidai.</span><span class="sxs-lookup"><span data-stu-id="087d8-157">For example, don't use the same price group for a loyalty discount and a channel discount.</span></span>  
36. <span data-ttu-id="087d8-158">Lauke Kainų grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="087d8-158">In the Price group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="087d8-159">Puslapio viršuje esantis saitas Kainų grupės yra skirtas lojalumo programai.</span><span class="sxs-lookup"><span data-stu-id="087d8-159">The Price groups link at the top of the page is for the loyalty program.</span></span> <span data-ttu-id="087d8-160">„Fasttab“ Programos pakopos esantis saitas Kainų grupės yra skirtas tik konkrečiai lojalumo pakopai.</span><span class="sxs-lookup"><span data-stu-id="087d8-160">The Price groups link in the Program tiers fasttab is for a specific loyalty tier only.</span></span>  
37. <span data-ttu-id="087d8-161">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="087d8-161">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="087d8-162">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="087d8-162">Click Save.</span></span>
39. <span data-ttu-id="087d8-163">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="087d8-163">Close the page.</span></span>
40. <span data-ttu-id="087d8-164">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="087d8-164">Click Save.</span></span>

