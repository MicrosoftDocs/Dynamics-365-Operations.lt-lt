--- 
title: "Nustatyti pardavimo komisinių taisykles"
description: "Ši procedūra nurodo, kaip nustatyti ir įgalinti pardavimo komisinių skaičiavimą ir sekimą."
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8e7d2198b4976a6f60f05690d7b6f11f3da55e28
ms.openlocfilehash: 3d5c38b1f07803242350fe016b45c45d49c0b59b
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---
# <a name="set-up-sales-commission-rules"></a><span data-ttu-id="79aa4-103">Nustatyti pardavimo komisinių taisykles</span><span class="sxs-lookup"><span data-stu-id="79aa4-103">Set up sales commission rules</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79aa4-104">Ši procedūra nurodo, kaip nustatyti ir įgalinti pardavimo komisinių skaičiavimą ir sekimą.</span><span class="sxs-lookup"><span data-stu-id="79aa4-104">This procedure shows you how to set up and enable sales commission calculation and tracking.</span></span> <span data-ttu-id="79aa4-105">Procedūra nurodo, kaip sukurti klientų ir prekių komisinių grupes ir kaip susieti pasirinktą klientą ir produktą su atitinkamomis grupėmis.</span><span class="sxs-lookup"><span data-stu-id="79aa4-105">The procedure shows how to create both customer and item commission groups, and then how to link a selected customer and product to the respective groups.</span></span> <span data-ttu-id="79aa4-106">Tada tos grupės naudojamos nustatant komisinių skaičiavimą, kad būtų galima sukurti kliento, prekės ir pardavimo atstovų derinį, kuris turi atitikti pardavimo užsakyme nurodytą derinį, kad pardavėjai turėtų teisę į komisinius.</span><span class="sxs-lookup"><span data-stu-id="79aa4-106">Those groups are then used in the commission calculation setup to create a customer, item, and sales representatives combination that must be matched by the sales order to entitle the sales people to a commission.</span></span> <span data-ttu-id="79aa4-107">Nėra būtina sukurti klientų ir prekių komisinių grupes, nes komisiniai gali būti apskaičiuojami ir atskiram klientui ir / arba prekei.</span><span class="sxs-lookup"><span data-stu-id="79aa4-107">Creating customer and item commission groups are optional, as the calculation of commission can also be done for an individual customer and/or item.</span></span> <span data-ttu-id="79aa4-108">Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="79aa4-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-commission-groups-and-commission-rates"></a><span data-ttu-id="79aa4-109">Komisinių grupių ir komisinių tarifų nustatymas</span><span class="sxs-lookup"><span data-stu-id="79aa4-109">Set up commission groups and commission rates</span></span>
1. <span data-ttu-id="79aa4-110">Pasirinkite Pardavimai ir rinkodara > Komisiniai > Komisinius gaunančių klientų grupės.</span><span class="sxs-lookup"><span data-stu-id="79aa4-110">Go to Sales and marketing > Commissions > Customer groups for commission.</span></span>
2. <span data-ttu-id="79aa4-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="79aa4-111">Click New.</span></span>
3. <span data-ttu-id="79aa4-112">Lauke Grupė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="79aa4-112">In the Group field, type a value.</span></span>
4. <span data-ttu-id="79aa4-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="79aa4-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="79aa4-114">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="79aa4-114">Click Save.</span></span>
6. <span data-ttu-id="79aa4-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="79aa4-115">Close the page.</span></span>
7. <span data-ttu-id="79aa4-116">Pasirinkite Pardavimai ir rinkodara > Komisiniai > Prekių grupės.</span><span class="sxs-lookup"><span data-stu-id="79aa4-116">Go to Sales and marketing > Commissions > Item groups.</span></span>
8. <span data-ttu-id="79aa4-117">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="79aa4-117">Click New.</span></span>
9. <span data-ttu-id="79aa4-118">Lauke Grupė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="79aa4-118">In the Group field, type a value.</span></span>
10. <span data-ttu-id="79aa4-119">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="79aa4-119">In the Name field, type a value.</span></span>
11. <span data-ttu-id="79aa4-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="79aa4-120">Close the page.</span></span>
12. <span data-ttu-id="79aa4-121">Pasirinkite Pardavimai ir rinkodara > Komisiniai > Pardavimo grupės.</span><span class="sxs-lookup"><span data-stu-id="79aa4-121">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="79aa4-122">Komisinių pardavimo grupė nurodo pardavimo atstovo vaidmenis atliekančius darbuotojus, kuriems, kai su tam tikra pardavimo grupe susietas klientas nusiperka tam tikras prekes, gali būti paskirti komisiniai.</span><span class="sxs-lookup"><span data-stu-id="79aa4-122">A Commission sales group specifies the employees in sales representative roles who are eligible to receive a commission when a customer associated with the relevant sales group buys certain items.</span></span>  
    * <span data-ttu-id="79aa4-123">Demonstracinių duomenų įmonėje USMF yra pardavimo grupė, pavadinta "Pard. atst. JAV."</span><span class="sxs-lookup"><span data-stu-id="79aa4-123">In the USMF demo data company, there is a sales group called "Sales reps US."</span></span>  
13. <span data-ttu-id="79aa4-124">Veiksmų srityje spustelėkite Bendra.</span><span class="sxs-lookup"><span data-stu-id="79aa4-124">On the Action Pane, click General.</span></span>
14. <span data-ttu-id="79aa4-125">Spustelėkite Pardavimo atstovas.</span><span class="sxs-lookup"><span data-stu-id="79aa4-125">Click Sales rep.</span></span>
    * <span data-ttu-id="79aa4-126">Puslapyje Pardavimo atstovai rodomas įmonės pardavimo skyriuje dirbančių ir su specialia komisinių grupe susietų žmonių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="79aa4-126">The Sales rep. page displays a list of the company's sales people who are associated with a specific commission group.</span></span> <span data-ttu-id="79aa4-127">Tai pačiai grupei galite priskirti keletą pardavimo atstovų ir nurodyti jiems priklausančios komisinio mokesčio dalies procentinę reikšmę.</span><span class="sxs-lookup"><span data-stu-id="79aa4-127">You can assign multiple sales representatives to the same group and define their respective share of the total commission fee as a percentage value.</span></span> <span data-ttu-id="79aa4-128">Bendra komisinių dalis tarp visų darbuotojų neturi viršyti 100.</span><span class="sxs-lookup"><span data-stu-id="79aa4-128">The total commission share across all employees must not exceed 100.</span></span>  
15. <span data-ttu-id="79aa4-129">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="79aa4-129">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="79aa4-130">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="79aa4-130">Click Edit.</span></span>
17. <span data-ttu-id="79aa4-131">Nustatykite pasirinkties Komisinių dalis reikšmę „50“.</span><span class="sxs-lookup"><span data-stu-id="79aa4-131">Set Commission share to '50'.</span></span>
18. <span data-ttu-id="79aa4-132">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="79aa4-132">Click New.</span></span>
19. <span data-ttu-id="79aa4-133">Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="79aa4-133">In the Name field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="79aa4-134">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="79aa4-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="79aa4-135">Pavyzdžiui, filtruokite lauką Pavadinimas reikšme „Susan Burk‟.</span><span class="sxs-lookup"><span data-stu-id="79aa4-135">For example, filter on the Name field with a value of 'Susan Burk'.</span></span>
21. <span data-ttu-id="79aa4-136">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="79aa4-136">Click Select.</span></span>
22. <span data-ttu-id="79aa4-137">Nustatykite pasirinkties Komisinių dalis reikšmę „50“.</span><span class="sxs-lookup"><span data-stu-id="79aa4-137">Set Commission share to '50'.</span></span>
23. <span data-ttu-id="79aa4-138">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="79aa4-138">Click Save.</span></span>
24. <span data-ttu-id="79aa4-139">Pasirinkite Pardavimai ir rinkodara > Komisiniai > Komisinių skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="79aa4-139">Go to Sales and marketing > Commissions > Commission calculation.</span></span>
    * <span data-ttu-id="79aa4-140">Komisinių skaičiavimo puslapyje nurodote komisinių tarifą, kurį darbuotojas turėtų gauti už pardavimo operaciją, jei joje naudojamas iš anksto nustatytas kliento ir produkto derinys.</span><span class="sxs-lookup"><span data-stu-id="79aa4-140">In the Commission calculation page you define the commission rate that the employee is to receive for a sales transaction when it contains the pre-set combination of customer and product.</span></span> <span data-ttu-id="79aa4-141">Nustatydami komisinių tarifą turite nurodyti komisinių skaičiavimo pagrindą ir tai, ar prie jų turėtų būti priskaičiuojamos nuolaidos.</span><span class="sxs-lookup"><span data-stu-id="79aa4-141">As part of the commission rate setup, you must specify the commission calculation basis and whether it should include or exclude discounts.</span></span> <span data-ttu-id="79aa4-142">Taip pat galite įvesti galiojimo laikotarpį, kuriuo komisinių tarifas aktyvus.</span><span class="sxs-lookup"><span data-stu-id="79aa4-142">You can also enter a validity period for when the commission rate is active.</span></span>  
25. <span data-ttu-id="79aa4-143">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="79aa4-143">Click New.</span></span>
26. <span data-ttu-id="79aa4-144">Lauke Prekės kodas pasirinkite „Grupė‟.</span><span class="sxs-lookup"><span data-stu-id="79aa4-144">In the Item code field, select 'Group'.</span></span>
27. <span data-ttu-id="79aa4-145">Lauke „Prekės ryšys“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="79aa4-145">In the Item relation field, click the drop-down button to open the lookup.</span></span>
28. <span data-ttu-id="79aa4-146">Sąraše raskite ir pasirinkite anksčiau sukurtą grupę.</span><span class="sxs-lookup"><span data-stu-id="79aa4-146">In the list, find and select the group that you created earlier.</span></span>
29. <span data-ttu-id="79aa4-147">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="79aa4-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="79aa4-148">Lauke Kliento kodas pasirinkite „Grupė‟.</span><span class="sxs-lookup"><span data-stu-id="79aa4-148">In the Customer code field, select 'Group'.</span></span>
31. <span data-ttu-id="79aa4-149">Lauke Kliento ryšys spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="79aa4-149">In the Customer relation field, click the drop-down button to open the lookup.</span></span>
32. <span data-ttu-id="79aa4-150">Sąraše raskite ir pasirinkite anksčiau nustatytą grupę.</span><span class="sxs-lookup"><span data-stu-id="79aa4-150">In the list, select the group that you set up earlier.</span></span>
33. <span data-ttu-id="79aa4-151">Lauke Pard. atst. ryšys spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="79aa4-151">In the Sales rep. relation field, click the drop-down button to open the lookup.</span></span>
34. <span data-ttu-id="79aa4-152">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="79aa4-152">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="79aa4-153">Palikite parinktį „Prieš apskaičiuojant eilutės nuolaidą“.</span><span class="sxs-lookup"><span data-stu-id="79aa4-153">Keep the "Before line discount" option.</span></span>  
    * <span data-ttu-id="79aa4-154">Palikite parinktį „Įplaukos“ kaip komisinių vertės skaičiavimo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="79aa4-154">Keep the "Revenue" option as the basis for commission value calculation.</span></span>    
35. <span data-ttu-id="79aa4-155">Lauke Komisinių procentas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="79aa4-155">In the Commission percentage field, enter a number.</span></span>
36. <span data-ttu-id="79aa4-156">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="79aa4-156">Click Save.</span></span>

## <a name="setting-up-commission-posting"></a><span data-ttu-id="79aa4-157">Komisinių registravimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="79aa4-157">Setting up commission posting</span></span>
1. <span data-ttu-id="79aa4-158">Pasirinkite Pardavimai ir rinkodara > Komisiniai > Komisinių registravimas.</span><span class="sxs-lookup"><span data-stu-id="79aa4-158">Go to Sales and marketing > Commissions > Commission posting.</span></span>
    * <span data-ttu-id="79aa4-159">Komisiniai mokesčiai mokami darbuotojams ir todėl turi būti nustatyti taip, kad būtų užtikrintas teisingas finansų registravimas atitinkamose DK sąskaitose.</span><span class="sxs-lookup"><span data-stu-id="79aa4-159">Commission fees are payable to the employees and must therefore be set up to ensure correct financial posting to the appropriate accounts in the General ledger.</span></span> <span data-ttu-id="79aa4-160">Tai atliekama puslapyje Komisinių registravimas.</span><span class="sxs-lookup"><span data-stu-id="79aa4-160">This is done in the Commission posting page.</span></span> <span data-ttu-id="79aa4-161">Peržiūrėkite dabartinei įmonei galimus taikyti nustatymus.</span><span class="sxs-lookup"><span data-stu-id="79aa4-161">Review the setup that is available for the current company.</span></span> <span data-ttu-id="79aa4-162">Paprastai komisinių sumos registruojamos paskirtoje išlaidų sąskaitoje ir koresponduojamos į paskirtą mokėtinos sumos sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="79aa4-162">Typically, the commission amounts are posted to a dedicated expense account and are offset to a dedicated payable account.</span></span> <span data-ttu-id="79aa4-163">Jei neturite nustatę komisinių registravimo taisyklių, sistema negalės išrašyti pardavimo užsakymo, kuriam gali būti paskaičiuoti komisiniai, sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="79aa4-163">If you don't have the commission posting rules set up, the system will fail to complete invoicing of a sales order which has eligible commissions.</span></span>  
2. <span data-ttu-id="79aa4-164">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="79aa4-164">Close the page.</span></span>

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a><span data-ttu-id="79aa4-165">Komisinių grupės priskyrimas klientui ir produktui</span><span class="sxs-lookup"><span data-stu-id="79aa4-165">Assign a commission group to a customer and a product</span></span>
1. <span data-ttu-id="79aa4-166">Pasirinkite Pardavimas ir rinkodara > Klientai > Visi klientai.</span><span class="sxs-lookup"><span data-stu-id="79aa4-166">Go to Sales and marketing > Customers > All customers.</span></span>
2. <span data-ttu-id="79aa4-167">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="79aa4-167">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="79aa4-168">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="79aa4-168">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="79aa4-169">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="79aa4-169">Click Edit.</span></span>
5. <span data-ttu-id="79aa4-170">Išplėskite skyrių Pardavimo užsakymo numatytieji nustatymai.</span><span class="sxs-lookup"><span data-stu-id="79aa4-170">Expand the Sales order defaults section.</span></span>
6. <span data-ttu-id="79aa4-171">Lauke Komisinių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="79aa4-171">In the Commission group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="79aa4-172">Sąraše pasirinkite anksčiau sukurtą grupę.</span><span class="sxs-lookup"><span data-stu-id="79aa4-172">In the list, select the group that you created earlier.</span></span>
8. <span data-ttu-id="79aa4-173">Lauke Pardavimo grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="79aa4-173">In the Sales group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="79aa4-174">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="79aa4-174">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="79aa4-175">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="79aa4-175">Click Save.</span></span>
11. <span data-ttu-id="79aa4-176">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="79aa4-176">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="79aa4-177">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="79aa4-177">Use the Quick Filter to find records.</span></span> <span data-ttu-id="79aa4-178">Pvz., filtruokite lauką Prekės numeris reikšme „T0020 “.</span><span class="sxs-lookup"><span data-stu-id="79aa4-178">For example, filter on the Item number field with a value of 'T0020 '.</span></span>
13. <span data-ttu-id="79aa4-179">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="79aa4-179">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="79aa4-180">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="79aa4-180">Click Edit.</span></span>
15. <span data-ttu-id="79aa4-181">Išplėskite skyrių Pardavimas.</span><span class="sxs-lookup"><span data-stu-id="79aa4-181">Expand the Sell section.</span></span>
16. <span data-ttu-id="79aa4-182">Lauke Komisinių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="79aa4-182">In the Commission group field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="79aa4-183">Sąraše pasirinkite anksčiau sukurtą komisinių grupę.</span><span class="sxs-lookup"><span data-stu-id="79aa4-183">In the list, select the commission group that you created earlier.</span></span>


