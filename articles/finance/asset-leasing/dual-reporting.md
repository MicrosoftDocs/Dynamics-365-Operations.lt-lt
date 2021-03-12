---
title: Dvigubos ataskaitos
description: Šioje temoje parodytas pavyzdys, rodantis, kaip galima įvykdyti tarptautinių finansinių ataskaitų standartų (IFRS) ataskaitų ir privalomųjų ataskaitų reikalavimus nuomojant turtą.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a7d9b3ea3d4f1d48b8a7326bd5a01d3119310c62
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003186"
---
# <a name="dual-reporting"></a><span data-ttu-id="643a9-103">Dvigubos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="643a9-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="643a9-104">Šioje temoje parodytas pavyzdys, rodantis, kaip galima įvykdyti tarptautinių finansinių ataskaitų standartų (IFRS) ataskaitų ir privalomųjų ataskaitų reikalavimus nuomojant turtą.</span><span class="sxs-lookup"><span data-stu-id="643a9-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="643a9-105">Reikia susipažinti su „Microsoft Dynamics 365 Finance“ registravimo sluoksniais, kad būtų lengviau suprasti pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="643a9-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="643a9-106">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="643a9-106">Example</span></span>

<span data-ttu-id="643a9-107">Toliau pateiktame pavyzdyje pateikiama nuomos sutartis pagal privalomųjų ataskaitų reikalavimus, naudojant ir grynaisiais pinigais paremtą metodą, ir IFRS ataskaitų metodus.</span><span class="sxs-lookup"><span data-stu-id="643a9-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="643a9-108">Įmonė turi sudaryti tris knygas, kad būtų atsižvelgta ir į Italijos įstatymų reikalavimus, ir į IFRS 16 reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="643a9-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="643a9-109">Vienos knygos reikia dėl IFRS 16, vienos – įstatymų reikalavimams, o dar vienos – tam, kad būtų automatiškai atšaukiami įstatyminiai registravimai.</span><span class="sxs-lookup"><span data-stu-id="643a9-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="643a9-110">Knygos nustatomos taip, kaip parodyta toliau esančiose lentelėse.</span><span class="sxs-lookup"><span data-stu-id="643a9-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="643a9-111">**IFRS 16 knyga**</span><span class="sxs-lookup"><span data-stu-id="643a9-111">**IFRS 16 book**</span></span>

<span data-ttu-id="643a9-112">IFRS 16 knyga nustatoma taip, kad atitiktų IFRS 16 apskaitos standartą.</span><span class="sxs-lookup"><span data-stu-id="643a9-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="643a9-113">Visi įrašai, užregistruoti šioje knygoje, bus registruojami pasirinktiniame sluoksnyje.</span><span class="sxs-lookup"><span data-stu-id="643a9-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="643a9-114">Pavadinimas / vardas ir (arba) pavardė</span><span class="sxs-lookup"><span data-stu-id="643a9-114">Name</span></span>                                    | <span data-ttu-id="643a9-115">aprašymas</span><span class="sxs-lookup"><span data-stu-id="643a9-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="643a9-116">Knygos tipas</span><span class="sxs-lookup"><span data-stu-id="643a9-116">Book type</span></span>                               | <span data-ttu-id="643a9-117">16-asis TFAS</span><span class="sxs-lookup"><span data-stu-id="643a9-117">IFRS 16</span></span>        |
| <span data-ttu-id="643a9-118">Knygos aprašymas</span><span class="sxs-lookup"><span data-stu-id="643a9-118">Book description</span></span>                        | <span data-ttu-id="643a9-119">16-asis TFAS</span><span class="sxs-lookup"><span data-stu-id="643a9-119">IFRS 16</span></span>        |
| <span data-ttu-id="643a9-120">Registravimo sluoksnis</span><span class="sxs-lookup"><span data-stu-id="643a9-120">Posting Layer</span></span>                           | <span data-ttu-id="643a9-121">1 pasirinktinis sluoksnis</span><span class="sxs-lookup"><span data-stu-id="643a9-121">Custom layer 1</span></span> |
| <span data-ttu-id="643a9-122">Nuomos tipas</span><span class="sxs-lookup"><span data-stu-id="643a9-122">Lease Type</span></span>                              | <span data-ttu-id="643a9-123">Finance</span><span class="sxs-lookup"><span data-stu-id="643a9-123">Finance</span></span>        |
| <span data-ttu-id="643a9-124">Apskaitos sistema</span><span class="sxs-lookup"><span data-stu-id="643a9-124">Accounting Framework</span></span>                    | <span data-ttu-id="643a9-125">16-asis TFAS</span><span class="sxs-lookup"><span data-stu-id="643a9-125">IFRS 16</span></span>        |
| <span data-ttu-id="643a9-126">Nuomos termino / naudingo naudojimo laiko nustatymas</span><span class="sxs-lookup"><span data-stu-id="643a9-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="643a9-127">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-127">0.00</span></span>           |
| <span data-ttu-id="643a9-128">Dabartinės vertės / turto tikrosios vertės nustatymas</span><span class="sxs-lookup"><span data-stu-id="643a9-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="643a9-129">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-129">0.00</span></span>           |
| <span data-ttu-id="643a9-130">Trumpojo laikotarpio ribinė reikšmė</span><span class="sxs-lookup"><span data-stu-id="643a9-130">Short-term threshold</span></span>                    | <span data-ttu-id="643a9-131">12</span><span class="sxs-lookup"><span data-stu-id="643a9-131">12</span></span>             |
| <span data-ttu-id="643a9-132">Mažos vertės ribinė reikšmė</span><span class="sxs-lookup"><span data-stu-id="643a9-132">Low Value Threshold</span></span>                     | <span data-ttu-id="643a9-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-133">5,000.00</span></span>       |
| <span data-ttu-id="643a9-134">Mokėti tiekėjui</span><span class="sxs-lookup"><span data-stu-id="643a9-134">Pay to Vendor</span></span>                           | <span data-ttu-id="643a9-135">nr.</span><span class="sxs-lookup"><span data-stu-id="643a9-135">No</span></span>             |

<span data-ttu-id="643a9-136">**Įstatyminė knyga**</span><span class="sxs-lookup"><span data-stu-id="643a9-136">**Statutory book**</span></span>

<span data-ttu-id="643a9-137">Įstatyminė knyga yra grynaisiais pinigais paremta knyga, kai įmonė apskaito nuomos išlaidas kaip grynaisiais pinigais kiekvieną mėnesį mokamą sumą.</span><span class="sxs-lookup"><span data-stu-id="643a9-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="643a9-138">Ši knyga nesukurs naudojimo teise valdomo turto arba nuomos įsipareigojimo.</span><span class="sxs-lookup"><span data-stu-id="643a9-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="643a9-139">Pavadinimas / vardas ir (arba) pavardė</span><span class="sxs-lookup"><span data-stu-id="643a9-139">Name</span></span>                                    | <span data-ttu-id="643a9-140">aprašymas</span><span class="sxs-lookup"><span data-stu-id="643a9-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="643a9-141">Knygos tipas</span><span class="sxs-lookup"><span data-stu-id="643a9-141">Book type</span></span>                               | <span data-ttu-id="643a9-142">Įstatyminė</span><span class="sxs-lookup"><span data-stu-id="643a9-142">Statutory</span></span>   |
| <span data-ttu-id="643a9-143">Knygos aprašymas</span><span class="sxs-lookup"><span data-stu-id="643a9-143">Book description</span></span>                        | <span data-ttu-id="643a9-144">Vietos GAAP</span><span class="sxs-lookup"><span data-stu-id="643a9-144">Local GAAP</span></span>  |
| <span data-ttu-id="643a9-145">Registravimo sluoksnis</span><span class="sxs-lookup"><span data-stu-id="643a9-145">Posting Layer</span></span>                           | <span data-ttu-id="643a9-146">Dabartiniai</span><span class="sxs-lookup"><span data-stu-id="643a9-146">Current</span></span>     |
| <span data-ttu-id="643a9-147">Nuomos tipas</span><span class="sxs-lookup"><span data-stu-id="643a9-147">Lease Type</span></span>                              | <span data-ttu-id="643a9-148">Automatinis</span><span class="sxs-lookup"><span data-stu-id="643a9-148">Automatic</span></span>   |
| <span data-ttu-id="643a9-149">Apskaitos sistema</span><span class="sxs-lookup"><span data-stu-id="643a9-149">Accounting Framework</span></span>                    | <span data-ttu-id="643a9-150">Grynųjų pinigų bazė</span><span class="sxs-lookup"><span data-stu-id="643a9-150">Cash basis</span></span>  |
| <span data-ttu-id="643a9-151">Nuomos termino / naudingo naudojimo laiko nustatymas</span><span class="sxs-lookup"><span data-stu-id="643a9-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="643a9-152">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-152">0.00</span></span>        |
| <span data-ttu-id="643a9-153">Dabartinės vertės / turto tikrosios vertės nustatymas</span><span class="sxs-lookup"><span data-stu-id="643a9-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="643a9-154">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-154">0.00</span></span>        |
| <span data-ttu-id="643a9-155">Trumpojo laikotarpio ribinė reikšmė</span><span class="sxs-lookup"><span data-stu-id="643a9-155">Short-term threshold</span></span>                    | <span data-ttu-id="643a9-156">0</span><span class="sxs-lookup"><span data-stu-id="643a9-156">0</span></span>           |
| <span data-ttu-id="643a9-157">Mažos vertės ribinė reikšmė</span><span class="sxs-lookup"><span data-stu-id="643a9-157">Low Value Threshold</span></span>                     | <span data-ttu-id="643a9-158">0</span><span class="sxs-lookup"><span data-stu-id="643a9-158">0</span></span>           |
| <span data-ttu-id="643a9-159">Mokėti tiekėjui</span><span class="sxs-lookup"><span data-stu-id="643a9-159">Pay to Vendor</span></span>                           | <span data-ttu-id="643a9-160">nr.</span><span class="sxs-lookup"><span data-stu-id="643a9-160">No</span></span>          |

<span data-ttu-id="643a9-161">**Įstatyminė atšaukimo knyga**</span><span class="sxs-lookup"><span data-stu-id="643a9-161">**Statutory reversal book**</span></span>

<span data-ttu-id="643a9-162">Įstatyminė atšaukimo knyga nustatoma taip pat, kaip įstatyminė knyga.</span><span class="sxs-lookup"><span data-stu-id="643a9-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="643a9-163">Pavadinimas / vardas ir (arba) pavardė</span><span class="sxs-lookup"><span data-stu-id="643a9-163">Name</span></span>                                    | <span data-ttu-id="643a9-164">aprašymas</span><span class="sxs-lookup"><span data-stu-id="643a9-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="643a9-165">Knygos tipas</span><span class="sxs-lookup"><span data-stu-id="643a9-165">Book type</span></span>                               | <span data-ttu-id="643a9-166">Įstatyminė – atšaukimo</span><span class="sxs-lookup"><span data-stu-id="643a9-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="643a9-167">Knygos aprašymas</span><span class="sxs-lookup"><span data-stu-id="643a9-167">Book description</span></span>                        | <span data-ttu-id="643a9-168">Knyga, skirta įstatyminei knygai atšaukti</span><span class="sxs-lookup"><span data-stu-id="643a9-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="643a9-169">Registravimo sluoksnis</span><span class="sxs-lookup"><span data-stu-id="643a9-169">Posting Layer</span></span>                           | <span data-ttu-id="643a9-170">1 pasirinktinis sluoksnis</span><span class="sxs-lookup"><span data-stu-id="643a9-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="643a9-171">Nuomos tipas</span><span class="sxs-lookup"><span data-stu-id="643a9-171">Lease Type</span></span>                              | <span data-ttu-id="643a9-172">Automatinis</span><span class="sxs-lookup"><span data-stu-id="643a9-172">Automatic</span></span>                      |
| <span data-ttu-id="643a9-173">Apskaitos sistema</span><span class="sxs-lookup"><span data-stu-id="643a9-173">Accounting Framework</span></span>                    | <span data-ttu-id="643a9-174">Grynųjų pinigų bazė</span><span class="sxs-lookup"><span data-stu-id="643a9-174">Cash basis</span></span>                     |
| <span data-ttu-id="643a9-175">Nuomos termino / naudingo naudojimo laiko nustatymas</span><span class="sxs-lookup"><span data-stu-id="643a9-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="643a9-176">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-176">0.00</span></span>                           |
| <span data-ttu-id="643a9-177">Dabartinės vertės / turto tikrosios vertės nustatymas</span><span class="sxs-lookup"><span data-stu-id="643a9-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="643a9-178">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-178">0.00</span></span>                           |
| <span data-ttu-id="643a9-179">Trumpojo laikotarpio ribinė reikšmė</span><span class="sxs-lookup"><span data-stu-id="643a9-179">Short-term threshold</span></span>                    | <span data-ttu-id="643a9-180">0</span><span class="sxs-lookup"><span data-stu-id="643a9-180">0</span></span>                              |
| <span data-ttu-id="643a9-181">Mažos vertės ribinė reikšmė</span><span class="sxs-lookup"><span data-stu-id="643a9-181">Low Value Threshold</span></span>                     | <span data-ttu-id="643a9-182">0</span><span class="sxs-lookup"><span data-stu-id="643a9-182">0</span></span>                              |
| <span data-ttu-id="643a9-183">Mokėti tiekėjui</span><span class="sxs-lookup"><span data-stu-id="643a9-183">Pay to Vendor</span></span>                           | <span data-ttu-id="643a9-184">nr.</span><span class="sxs-lookup"><span data-stu-id="643a9-184">No</span></span>                             |

<span data-ttu-id="643a9-185">Šiam pavyzdžiui sukurta nuomos sutartis, kurios parametrai skirtukuose **Bendra** ir **Mokėjimo grafiko eilutės** nurodyti toliau.</span><span class="sxs-lookup"><span data-stu-id="643a9-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="643a9-186">**Skirtukas Bendra**</span><span class="sxs-lookup"><span data-stu-id="643a9-186">**General tab**</span></span>

| <span data-ttu-id="643a9-187">Laukas</span><span class="sxs-lookup"><span data-stu-id="643a9-187">Field</span></span>                      | <span data-ttu-id="643a9-188">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="643a9-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="643a9-189">Apskaičiuota skolinimosi palūkanų norma</span><span class="sxs-lookup"><span data-stu-id="643a9-189">Incremental borrowing rate</span></span> | <span data-ttu-id="643a9-190">5 %</span><span class="sxs-lookup"><span data-stu-id="643a9-190">5%</span></span>               |
| <span data-ttu-id="643a9-191">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="643a9-191">Commencement date</span></span>          | <span data-ttu-id="643a9-192">2020-01-01</span><span class="sxs-lookup"><span data-stu-id="643a9-192">1/1/2020</span></span>         |
| <span data-ttu-id="643a9-193">Nuomos grupė</span><span class="sxs-lookup"><span data-stu-id="643a9-193">Lease group</span></span>                | <span data-ttu-id="643a9-194">Pastatai</span><span class="sxs-lookup"><span data-stu-id="643a9-194">Buildings</span></span>        |
| <span data-ttu-id="643a9-195">Tiekėjas</span><span class="sxs-lookup"><span data-stu-id="643a9-195">Vendor</span></span>                     | <span data-ttu-id="643a9-196">1001</span><span class="sxs-lookup"><span data-stu-id="643a9-196">1001</span></span>             |
| <span data-ttu-id="643a9-197">Turto tikroji vertė</span><span class="sxs-lookup"><span data-stu-id="643a9-197">Fair value of the asset</span></span>    | <span data-ttu-id="643a9-198">245,000</span><span class="sxs-lookup"><span data-stu-id="643a9-198">245,000</span></span>          |
| <span data-ttu-id="643a9-199">Turto naudingo naudojimo laikas</span><span class="sxs-lookup"><span data-stu-id="643a9-199">Asset useful life</span></span>          | <span data-ttu-id="643a9-200">120</span><span class="sxs-lookup"><span data-stu-id="643a9-200">120</span></span>              |
| <span data-ttu-id="643a9-201">Anuiteto tipas</span><span class="sxs-lookup"><span data-stu-id="643a9-201">Annuity type</span></span>               | <span data-ttu-id="643a9-202">Įprastas anuitetas</span><span class="sxs-lookup"><span data-stu-id="643a9-202">Ordinary annuity</span></span> |
| <span data-ttu-id="643a9-203">Sujungimo intervalas</span><span class="sxs-lookup"><span data-stu-id="643a9-203">Compounding interval</span></span>       | <span data-ttu-id="643a9-204">Mėnesinis</span><span class="sxs-lookup"><span data-stu-id="643a9-204">Monthly</span></span>          |

<span data-ttu-id="643a9-205">**Skirtukas Mokėjimo grafiko eilutės**</span><span class="sxs-lookup"><span data-stu-id="643a9-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="643a9-206">Laukas</span><span class="sxs-lookup"><span data-stu-id="643a9-206">Field</span></span>             | <span data-ttu-id="643a9-207">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="643a9-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="643a9-208">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="643a9-208">Start date</span></span>        | <span data-ttu-id="643a9-209">2020-01-01</span><span class="sxs-lookup"><span data-stu-id="643a9-209">1/1/2020</span></span>   |
| <span data-ttu-id="643a9-210">Laikotarpio intervalas</span><span class="sxs-lookup"><span data-stu-id="643a9-210">Period interval</span></span>   | <span data-ttu-id="643a9-211">Mėnesiai</span><span class="sxs-lookup"><span data-stu-id="643a9-211">Months</span></span>     |
| <span data-ttu-id="643a9-212">Laikotarpiai</span><span class="sxs-lookup"><span data-stu-id="643a9-212">Periods</span></span>           | <span data-ttu-id="643a9-213">24</span><span class="sxs-lookup"><span data-stu-id="643a9-213">24</span></span>         |
| <span data-ttu-id="643a9-214">Pabaigos data</span><span class="sxs-lookup"><span data-stu-id="643a9-214">End date</span></span>          | <span data-ttu-id="643a9-215">2020-12-31</span><span class="sxs-lookup"><span data-stu-id="643a9-215">12/31/2020</span></span> |
| <span data-ttu-id="643a9-216">Mokėjimo dažnumas</span><span class="sxs-lookup"><span data-stu-id="643a9-216">Payment frequency</span></span> | <span data-ttu-id="643a9-217">Mėnesinis</span><span class="sxs-lookup"><span data-stu-id="643a9-217">Monthly</span></span>    |
| <span data-ttu-id="643a9-218">Mokėjimo suma</span><span class="sxs-lookup"><span data-stu-id="643a9-218">Payment amount</span></span>    | <span data-ttu-id="643a9-219">1000</span><span class="sxs-lookup"><span data-stu-id="643a9-219">1,000</span></span>      |

<span data-ttu-id="643a9-220">Norėdami apskaityti šią nuomą dviejose sistemose, naudokite dabartinį registravimo sluoksnį ir pasirinktinį registravimo sluoksnį.</span><span class="sxs-lookup"><span data-stu-id="643a9-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="643a9-221">Šioje lentelėje pateikiamas kiekvieno žurnalo įrašo, kurio reikia norint sąžiningai pateikti kiekvieno ataskaitų standarto finansinius duomenis, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="643a9-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="643a9-222">Po to pateikiamas išsamus kiekvieno žurnalo įrašo už pirmą nuomos mėnesį aprašas.</span><span class="sxs-lookup"><span data-stu-id="643a9-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="643a9-223">Sąskaitos numeris</span><span class="sxs-lookup"><span data-stu-id="643a9-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="643a9-224">aprašymas</span><span class="sxs-lookup"><span data-stu-id="643a9-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="643a9-225">Įstatyminė knyga (dabartinis sluoksnis)</span><span class="sxs-lookup"><span data-stu-id="643a9-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="643a9-226">Dabartinio sluoksnio bendroji suma</span><span class="sxs-lookup"><span data-stu-id="643a9-226">Current layer total</span></span></th>
<th><span data-ttu-id="643a9-227">Atšaukimo knyga (pasirinktinis sluoksnis)</span><span class="sxs-lookup"><span data-stu-id="643a9-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="643a9-228">IFRS 16 knyga (pasirinktinis sluoksnis)</span><span class="sxs-lookup"><span data-stu-id="643a9-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="643a9-229">Dabartinio sluoksnio ir pasirinktinio sluoksnio bendroji suma</span><span class="sxs-lookup"><span data-stu-id="643a9-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="643a9-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="643a9-230">JE-100</span></span></th>
<th><span data-ttu-id="643a9-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="643a9-231">JE-110</span></span></th>
<th><span data-ttu-id="643a9-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="643a9-232">JE-120</span></span></th>
<th><span data-ttu-id="643a9-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="643a9-233">JE-130</span></span></th>
<th><span data-ttu-id="643a9-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="643a9-234">JE-140</span></span></th>
<th><span data-ttu-id="643a9-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="643a9-235">JE-150</span></span></th>
<th><span data-ttu-id="643a9-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="643a9-236">JE-160</span></span></th>
<th><span data-ttu-id="643a9-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="643a9-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="643a9-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="643a9-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="643a9-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="643a9-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="643a9-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="643a9-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="643a9-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="643a9-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="643a9-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="643a9-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="643a9-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="643a9-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="643a9-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="643a9-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="643a9-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="643a9-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="643a9-246">1</span><span class="sxs-lookup"><span data-stu-id="643a9-246">1</span></span></td>
<td><span data-ttu-id="643a9-247">Nuomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="643a9-247">Lease expense</span></span></td>
<td><span data-ttu-id="643a9-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-249">1,000.00</span></span></td>
<td><span data-ttu-id="643a9-250">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-251">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-252">2</span><span class="sxs-lookup"><span data-stu-id="643a9-252">2</span></span></td>
<td><span data-ttu-id="643a9-253">Banko mokestis</span><span class="sxs-lookup"><span data-stu-id="643a9-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="643a9-254">3.00</span><span class="sxs-lookup"><span data-stu-id="643a9-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="643a9-255">3.00</span><span class="sxs-lookup"><span data-stu-id="643a9-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-256">3.00</span><span class="sxs-lookup"><span data-stu-id="643a9-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-257">3</span><span class="sxs-lookup"><span data-stu-id="643a9-257">3</span></span></td>
<td><span data-ttu-id="643a9-258">PVM išlaidos</span><span class="sxs-lookup"><span data-stu-id="643a9-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="643a9-259">5.00</span><span class="sxs-lookup"><span data-stu-id="643a9-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="643a9-260">5.00</span><span class="sxs-lookup"><span data-stu-id="643a9-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-261">5.00</span><span class="sxs-lookup"><span data-stu-id="643a9-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-262">4</span><span class="sxs-lookup"><span data-stu-id="643a9-262">4</span></span></td>
<td><span data-ttu-id="643a9-263">Tarpuskaitos sąskaita</span><span class="sxs-lookup"><span data-stu-id="643a9-263">Clearing account</span></span></td>
<td><span data-ttu-id="643a9-264">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-264">-1,000.00</span></span></td>
<td><span data-ttu-id="643a9-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="643a9-266">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-266">0.00</span></span></td>
<td><span data-ttu-id="643a9-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="643a9-268">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-269">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-270">5</span><span class="sxs-lookup"><span data-stu-id="643a9-270">5</span></span></td>
<td><span data-ttu-id="643a9-271">Mokėtinos sumos</span><span class="sxs-lookup"><span data-stu-id="643a9-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="643a9-272">–1 008,00</span><span class="sxs-lookup"><span data-stu-id="643a9-272">-1,008.00</span></span></td>
<td><span data-ttu-id="643a9-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="643a9-273">1,008.00</span></span></td>
<td><span data-ttu-id="643a9-274">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-275">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-276">6</span><span class="sxs-lookup"><span data-stu-id="643a9-276">6</span></span></td>
<td><span data-ttu-id="643a9-277">Naudojimo teise valdomas turtas</span><span class="sxs-lookup"><span data-stu-id="643a9-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-278">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="643a9-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="643a9-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="643a9-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-281">7</span><span class="sxs-lookup"><span data-stu-id="643a9-281">7</span></span></td>
<td><span data-ttu-id="643a9-282">Finansinės nuomos įsipareigojimas</span><span class="sxs-lookup"><span data-stu-id="643a9-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-283">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="643a9-284">–22 794,00</span><span class="sxs-lookup"><span data-stu-id="643a9-284">-22,794.00</span></span></td>
<td><span data-ttu-id="643a9-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-285">1,000.00</span></span></td>
<td><span data-ttu-id="643a9-286">–94,97</span><span class="sxs-lookup"><span data-stu-id="643a9-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="643a9-287">–21 888,87</span><span class="sxs-lookup"><span data-stu-id="643a9-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-288">8</span><span class="sxs-lookup"><span data-stu-id="643a9-288">8</span></span></td>
<td><span data-ttu-id="643a9-289">Palūkanų išlaidos</span><span class="sxs-lookup"><span data-stu-id="643a9-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-290">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-291">94.97</span><span class="sxs-lookup"><span data-stu-id="643a9-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="643a9-292">94.97</span><span class="sxs-lookup"><span data-stu-id="643a9-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-293">9</span><span class="sxs-lookup"><span data-stu-id="643a9-293">9</span></span></td>
<td><span data-ttu-id="643a9-294">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="643a9-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-295">–1 008,00</span><span class="sxs-lookup"><span data-stu-id="643a9-295">-1,008.00</span></span></td>
<td><span data-ttu-id="643a9-296">–1 008,00</span><span class="sxs-lookup"><span data-stu-id="643a9-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-297">–1 008,00</span><span class="sxs-lookup"><span data-stu-id="643a9-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-298">10</span><span class="sxs-lookup"><span data-stu-id="643a9-298">10</span></span></td>
<td><span data-ttu-id="643a9-299">Likvidavimo išlaidos</span><span class="sxs-lookup"><span data-stu-id="643a9-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-300">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-301">949.75</span><span class="sxs-lookup"><span data-stu-id="643a9-301">949.75</span></span></td>
<td><span data-ttu-id="643a9-302">949.75</span><span class="sxs-lookup"><span data-stu-id="643a9-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-303">11</span><span class="sxs-lookup"><span data-stu-id="643a9-303">11</span></span></td>
<td><span data-ttu-id="643a9-304">Sukauptas nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="643a9-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-305">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-306">–949,75</span><span class="sxs-lookup"><span data-stu-id="643a9-306">-949.75</span></span></td>
<td><span data-ttu-id="643a9-307">–949,75</span><span class="sxs-lookup"><span data-stu-id="643a9-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="643a9-308">Kaip nurodyta pirmiau pateiktoje lentelėje, reikia pateikti tris knygas, kad būtų galima deklaruoti ir įstatymines ataskaitas, ir IFRS ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="643a9-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="643a9-309">Įstatyminėje knygoje įrašomas nuomos mokestis pagal dabartinio sluoksnio grynaisiais pinigais paremtą apskaitą.</span><span class="sxs-lookup"><span data-stu-id="643a9-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="643a9-310">Įstatyminėje atšaukimo knygoje atšaukiami įstatyminio žurnalo įrašai.</span><span class="sxs-lookup"><span data-stu-id="643a9-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="643a9-311">IFRS 16 knygoje sukuriami žurnalo įrašai, kurie reikalingi pagal IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="643a9-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="643a9-312">Nuomą turite įvesti tik vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="643a9-312">You must enter a lease only one time.</span></span> <span data-ttu-id="643a9-313">Tada galite atidaryti puslapį **Knygos**, kad matytumėte visas su nuoma susijusias knygas.</span><span class="sxs-lookup"><span data-stu-id="643a9-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="643a9-314">Kai kuriate knygas, visos trys turi būti susietos su tuo pačiu nuomos įrašu.</span><span class="sxs-lookup"><span data-stu-id="643a9-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="643a9-315">Pirmajame žurnalo įraše įrašomos nuomos išlaidos pagal įstatyminę knygą.</span><span class="sxs-lookup"><span data-stu-id="643a9-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="643a9-316">Mokėjimus galite kurti kaip paketą arba pasirinkdami mokėjimo grafiką įstatyminėje knygoje.</span><span class="sxs-lookup"><span data-stu-id="643a9-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="643a9-317">Šiam pavyzdžiui sukurtas tolesnis įstatyminės knygos žurnalo įrašas iš mokėjimų grafiko.</span><span class="sxs-lookup"><span data-stu-id="643a9-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="643a9-318">Nuomos mokestis – 2020-01-31 – JE 100</span><span class="sxs-lookup"><span data-stu-id="643a9-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="643a9-319">Kodo tipas</span><span class="sxs-lookup"><span data-stu-id="643a9-319">Account type</span></span> | <span data-ttu-id="643a9-320">Sąskaitos numeris</span><span class="sxs-lookup"><span data-stu-id="643a9-320">Account number</span></span> | <span data-ttu-id="643a9-321">Sluoksnis</span><span class="sxs-lookup"><span data-stu-id="643a9-321">Layer</span></span>   | <span data-ttu-id="643a9-322">Sąskaitos aprašas</span><span class="sxs-lookup"><span data-stu-id="643a9-322">Account description</span></span> | <span data-ttu-id="643a9-323">Debetas</span><span class="sxs-lookup"><span data-stu-id="643a9-323">Debit</span></span>    | <span data-ttu-id="643a9-324">Kreditas</span><span class="sxs-lookup"><span data-stu-id="643a9-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="643a9-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="643a9-325">Ledger</span></span>       | <span data-ttu-id="643a9-326">1</span><span class="sxs-lookup"><span data-stu-id="643a9-326">1</span></span>              | <span data-ttu-id="643a9-327">Dabartiniai</span><span class="sxs-lookup"><span data-stu-id="643a9-327">Current</span></span> | <span data-ttu-id="643a9-328">Nuomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="643a9-328">Lease expense</span></span>       | <span data-ttu-id="643a9-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-329">1,000.00</span></span> |          |
| <span data-ttu-id="643a9-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="643a9-330">Ledger</span></span>       | <span data-ttu-id="643a9-331">4</span><span class="sxs-lookup"><span data-stu-id="643a9-331">4</span></span>              | <span data-ttu-id="643a9-332">Dabartiniai</span><span class="sxs-lookup"><span data-stu-id="643a9-332">Current</span></span> | <span data-ttu-id="643a9-333">Tarpuskaitos sąskaita</span><span class="sxs-lookup"><span data-stu-id="643a9-333">Clearing account</span></span>    |          | <span data-ttu-id="643a9-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-334">1,000.00</span></span> |

<span data-ttu-id="643a9-335">Mokėtinų sumų klerkas, naudodamas standartines „Dynamics 365“ funkcijas, sukuria sąskaitą faktūrą, skirtą sumokėti už nuomą nenaudojant turto nuomos funkcijos.</span><span class="sxs-lookup"><span data-stu-id="643a9-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="643a9-336">Tačiau, užuot kaip debeto sąskaitą pasirinkęs **Nuomos išlaidos**, mokėtinų sumų klerkas pasirenka tarpuskaitos sąskaitą, kad sugeneruotų tolesnį įrašą.</span><span class="sxs-lookup"><span data-stu-id="643a9-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="643a9-337">AP procesas – 2020-01-31 – JE 110</span><span class="sxs-lookup"><span data-stu-id="643a9-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="643a9-338">Kodo tipas</span><span class="sxs-lookup"><span data-stu-id="643a9-338">Account type</span></span> | <span data-ttu-id="643a9-339">Sąskaitos numeris</span><span class="sxs-lookup"><span data-stu-id="643a9-339">Account number</span></span> | <span data-ttu-id="643a9-340">Sluoksnis</span><span class="sxs-lookup"><span data-stu-id="643a9-340">Layer</span></span>   | <span data-ttu-id="643a9-341">Sąskaitos aprašas</span><span class="sxs-lookup"><span data-stu-id="643a9-341">Account description</span></span> | <span data-ttu-id="643a9-342">Debetas</span><span class="sxs-lookup"><span data-stu-id="643a9-342">Debit</span></span>    | <span data-ttu-id="643a9-343">Kreditas</span><span class="sxs-lookup"><span data-stu-id="643a9-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="643a9-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="643a9-344">Ledger</span></span>       | <span data-ttu-id="643a9-345">4</span><span class="sxs-lookup"><span data-stu-id="643a9-345">4</span></span>              | <span data-ttu-id="643a9-346">Dabartiniai</span><span class="sxs-lookup"><span data-stu-id="643a9-346">Current</span></span> | <span data-ttu-id="643a9-347">Tarpuskaitos sąskaita</span><span class="sxs-lookup"><span data-stu-id="643a9-347">Clearing account</span></span>    | <span data-ttu-id="643a9-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-348">1,000.00</span></span> |          |
| <span data-ttu-id="643a9-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="643a9-349">Ledger</span></span>       | <span data-ttu-id="643a9-350">2</span><span class="sxs-lookup"><span data-stu-id="643a9-350">2</span></span>              | <span data-ttu-id="643a9-351">Dabartiniai</span><span class="sxs-lookup"><span data-stu-id="643a9-351">Current</span></span> | <span data-ttu-id="643a9-352">Banko mokestis</span><span class="sxs-lookup"><span data-stu-id="643a9-352">Bank fee</span></span>            | <span data-ttu-id="643a9-353">3.00</span><span class="sxs-lookup"><span data-stu-id="643a9-353">3.00</span></span>     |          |
| <span data-ttu-id="643a9-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="643a9-354">Ledger</span></span>       | <span data-ttu-id="643a9-355">3</span><span class="sxs-lookup"><span data-stu-id="643a9-355">3</span></span>              | <span data-ttu-id="643a9-356">Dabartiniai</span><span class="sxs-lookup"><span data-stu-id="643a9-356">Current</span></span> | <span data-ttu-id="643a9-357">PVM išlaidos</span><span class="sxs-lookup"><span data-stu-id="643a9-357">VAT expense</span></span>         | <span data-ttu-id="643a9-358">5.00</span><span class="sxs-lookup"><span data-stu-id="643a9-358">5.00</span></span>     |          |
| <span data-ttu-id="643a9-359">Tiekėjas</span><span class="sxs-lookup"><span data-stu-id="643a9-359">Vendor</span></span>       | <span data-ttu-id="643a9-360">5</span><span class="sxs-lookup"><span data-stu-id="643a9-360">5</span></span>              | <span data-ttu-id="643a9-361">Dabartiniai</span><span class="sxs-lookup"><span data-stu-id="643a9-361">Current</span></span> | <span data-ttu-id="643a9-362">Mokėtinos sumos</span><span class="sxs-lookup"><span data-stu-id="643a9-362">Accounts payable</span></span>    |          | <span data-ttu-id="643a9-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="643a9-363">1,008.00</span></span> |

<span data-ttu-id="643a9-364">Kai išrašas išduodamas tiekėjui, vadovaukitės įprastu mokėjimo procesu.</span><span class="sxs-lookup"><span data-stu-id="643a9-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="643a9-365">Šio proceso metu sugeneruojamas tolesnis žurnalo įrašas.</span><span class="sxs-lookup"><span data-stu-id="643a9-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="643a9-366">Mokėjimas grynaisiais pinigais – 2020–01-31 JE 120</span><span class="sxs-lookup"><span data-stu-id="643a9-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="643a9-367">Kodo tipas</span><span class="sxs-lookup"><span data-stu-id="643a9-367">Account type</span></span> | <span data-ttu-id="643a9-368">Sąskaitos numeris</span><span class="sxs-lookup"><span data-stu-id="643a9-368">Account number</span></span> | <span data-ttu-id="643a9-369">Sluoksnis</span><span class="sxs-lookup"><span data-stu-id="643a9-369">Layer</span></span>   | <span data-ttu-id="643a9-370">Sąskaitos aprašas</span><span class="sxs-lookup"><span data-stu-id="643a9-370">Account description</span></span> | <span data-ttu-id="643a9-371">Debetas</span><span class="sxs-lookup"><span data-stu-id="643a9-371">Debit</span></span>    | <span data-ttu-id="643a9-372">Kreditas</span><span class="sxs-lookup"><span data-stu-id="643a9-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="643a9-373">Tiekėjas</span><span class="sxs-lookup"><span data-stu-id="643a9-373">Vendor</span></span>       | <span data-ttu-id="643a9-374">5</span><span class="sxs-lookup"><span data-stu-id="643a9-374">5</span></span>              | <span data-ttu-id="643a9-375">Dabartiniai</span><span class="sxs-lookup"><span data-stu-id="643a9-375">Current</span></span> | <span data-ttu-id="643a9-376">Mokėtinos sumos</span><span class="sxs-lookup"><span data-stu-id="643a9-376">Accounts Payable</span></span>    | <span data-ttu-id="643a9-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="643a9-377">1,008.00</span></span> |          |
| <span data-ttu-id="643a9-378">Bankas</span><span class="sxs-lookup"><span data-stu-id="643a9-378">Bank</span></span>         | <span data-ttu-id="643a9-379">9</span><span class="sxs-lookup"><span data-stu-id="643a9-379">9</span></span>              | <span data-ttu-id="643a9-380">Dabartiniai</span><span class="sxs-lookup"><span data-stu-id="643a9-380">Current</span></span> | <span data-ttu-id="643a9-381">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="643a9-381">Cash</span></span>                |          | <span data-ttu-id="643a9-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="643a9-382">1,008.00</span></span> |

<span data-ttu-id="643a9-383">Šiuo metu esate visiškai apskaitę šią nuomą pagal privalomuosius ataskaitų reikalavimus ir galite generuoti bandomąjį balansą naudodami dabartinį sluoksnį.</span><span class="sxs-lookup"><span data-stu-id="643a9-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="643a9-384">Sistema pateikia bandomąjį balansą su tolesniais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="643a9-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="643a9-385">Sąskaitos numeris</span><span class="sxs-lookup"><span data-stu-id="643a9-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="643a9-386">aprašymas</span><span class="sxs-lookup"><span data-stu-id="643a9-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="643a9-387">Įstatyminė knyga (dabartinis sluoksnis)</span><span class="sxs-lookup"><span data-stu-id="643a9-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="643a9-388">Dabartinio sluoksnio bendroji suma</span><span class="sxs-lookup"><span data-stu-id="643a9-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="643a9-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="643a9-389">JE-100</span></span></th>
<th><span data-ttu-id="643a9-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="643a9-390">JE-110</span></span></th>
<th><span data-ttu-id="643a9-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="643a9-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="643a9-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="643a9-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="643a9-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="643a9-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="643a9-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="643a9-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="643a9-395">1</span><span class="sxs-lookup"><span data-stu-id="643a9-395">1</span></span></td>
<td><span data-ttu-id="643a9-396">Nuomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="643a9-396">Lease expense</span></span></td>
<td><span data-ttu-id="643a9-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-399">2</span><span class="sxs-lookup"><span data-stu-id="643a9-399">2</span></span></td>
<td><span data-ttu-id="643a9-400">Banko mokestis</span><span class="sxs-lookup"><span data-stu-id="643a9-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="643a9-401">3.00</span><span class="sxs-lookup"><span data-stu-id="643a9-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="643a9-402">3.00</span><span class="sxs-lookup"><span data-stu-id="643a9-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-403">3</span><span class="sxs-lookup"><span data-stu-id="643a9-403">3</span></span></td>
<td><span data-ttu-id="643a9-404">PVM išlaidos</span><span class="sxs-lookup"><span data-stu-id="643a9-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="643a9-405">5.00</span><span class="sxs-lookup"><span data-stu-id="643a9-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="643a9-406">5.00</span><span class="sxs-lookup"><span data-stu-id="643a9-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-407">4</span><span class="sxs-lookup"><span data-stu-id="643a9-407">4</span></span></td>
<td><span data-ttu-id="643a9-408">Tarpuskaitos sąskaita</span><span class="sxs-lookup"><span data-stu-id="643a9-408">Clearing account</span></span></td>
<td><span data-ttu-id="643a9-409">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-409">-1,000.00</span></span></td>
<td><span data-ttu-id="643a9-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="643a9-411">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-412">5</span><span class="sxs-lookup"><span data-stu-id="643a9-412">5</span></span></td>
<td><span data-ttu-id="643a9-413">Mokėtinos sumos</span><span class="sxs-lookup"><span data-stu-id="643a9-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="643a9-414">–1 008,00</span><span class="sxs-lookup"><span data-stu-id="643a9-414">-1,008.00</span></span></td>
<td><span data-ttu-id="643a9-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="643a9-415">1,008.00</span></span></td>
<td><span data-ttu-id="643a9-416">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-417">6</span><span class="sxs-lookup"><span data-stu-id="643a9-417">6</span></span></td>
<td><span data-ttu-id="643a9-418">Naudojimo teise valdomas turtas</span><span class="sxs-lookup"><span data-stu-id="643a9-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-419">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-420">7</span><span class="sxs-lookup"><span data-stu-id="643a9-420">7</span></span></td>
<td><span data-ttu-id="643a9-421">Finansinės nuomos įsipareigojimas</span><span class="sxs-lookup"><span data-stu-id="643a9-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-422">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-423">8</span><span class="sxs-lookup"><span data-stu-id="643a9-423">8</span></span></td>
<td><span data-ttu-id="643a9-424">Palūkanų išlaidos</span><span class="sxs-lookup"><span data-stu-id="643a9-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-425">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-426">9</span><span class="sxs-lookup"><span data-stu-id="643a9-426">9</span></span></td>
<td><span data-ttu-id="643a9-427">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="643a9-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-428">–1 008,00</span><span class="sxs-lookup"><span data-stu-id="643a9-428">-1,008.00</span></span></td>
<td><span data-ttu-id="643a9-429">–1 008,00</span><span class="sxs-lookup"><span data-stu-id="643a9-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-430">10</span><span class="sxs-lookup"><span data-stu-id="643a9-430">10</span></span></td>
<td><span data-ttu-id="643a9-431">Likvidavimo išlaidos</span><span class="sxs-lookup"><span data-stu-id="643a9-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-432">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="643a9-433">11</span><span class="sxs-lookup"><span data-stu-id="643a9-433">11</span></span></td>
<td><span data-ttu-id="643a9-434">Sukauptas nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="643a9-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="643a9-435">0,00</span><span class="sxs-lookup"><span data-stu-id="643a9-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="643a9-436">Jei norite naudoti IFRS 16 skaičius ir vykdyti tą patį bandomąjį balansą, įstatyminio apskaitos žurnalo įrašai turi būti atšaukti, o IFRS 16 žurnalo įrašai – registruojami.</span><span class="sxs-lookup"><span data-stu-id="643a9-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="643a9-437">Kad galėtumėte atšaukti įstatyminio žurnalo įrašus, šiame pavyzdyje yra pateikta įstatyminė atšaukimo knyga, kurios nustatymai tokie patys, kaip įstatyminės knygos, tačiau priešingas registravimo šablonas.</span><span class="sxs-lookup"><span data-stu-id="643a9-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="643a9-438">Pavyzdžiui, įstatyminėje knygoje *debetuojama* nuomos išlaidų sąskaita, tačiau atšaukimo knygoje ši sąskaita bus *kredituojama*.</span><span class="sxs-lookup"><span data-stu-id="643a9-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="643a9-439">Šiuos ryšius lengva apibrėžti turto nuomos registravimo sąskaitose, esančiose puslapyje **Turto nuomos parametrai** (**Turto nuoma \> Sąranka \> Turto nuomos parametrai**).</span><span class="sxs-lookup"><span data-stu-id="643a9-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="643a9-440">Kai tas pats procesas, kuris buvo naudojamas įstatyminei knygai, naudojamas atšaukimo knygai, sukuriamas tolesnis žurnalo įrašas.</span><span class="sxs-lookup"><span data-stu-id="643a9-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="643a9-441">Skirtumas yra tas, kad atšaukimo knygoje rezervuojami atšaukiami įrašai iš įstatyminės knygos.</span><span class="sxs-lookup"><span data-stu-id="643a9-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="643a9-442">Atšaukiami įrašai taip pat sukuriami pasirinktiniame sluoksnyje.</span><span class="sxs-lookup"><span data-stu-id="643a9-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="643a9-443">Kai bandomasis balansas vykdomas dabartiniame sluoksnyje, atšaukiami žurnalo įrašai neįtraukiami.</span><span class="sxs-lookup"><span data-stu-id="643a9-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="643a9-444">Nuomos mokestis – 2020-01-31 – JE 130</span><span class="sxs-lookup"><span data-stu-id="643a9-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="643a9-445">Kodo tipas</span><span class="sxs-lookup"><span data-stu-id="643a9-445">Account type</span></span> | <span data-ttu-id="643a9-446">Sąskaitos numeris</span><span class="sxs-lookup"><span data-stu-id="643a9-446">Account number</span></span> | <span data-ttu-id="643a9-447">Sluoksnis</span><span class="sxs-lookup"><span data-stu-id="643a9-447">Layer</span></span>  | <span data-ttu-id="643a9-448">Sąskaitos aprašas</span><span class="sxs-lookup"><span data-stu-id="643a9-448">Account description</span></span> | <span data-ttu-id="643a9-449">Debetas</span><span class="sxs-lookup"><span data-stu-id="643a9-449">Debit</span></span>    | <span data-ttu-id="643a9-450">Kreditas</span><span class="sxs-lookup"><span data-stu-id="643a9-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="643a9-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="643a9-451">Ledger</span></span>       | <span data-ttu-id="643a9-452">4</span><span class="sxs-lookup"><span data-stu-id="643a9-452">4</span></span>              | <span data-ttu-id="643a9-453">Pasirinktinis</span><span class="sxs-lookup"><span data-stu-id="643a9-453">Custom</span></span> | <span data-ttu-id="643a9-454">Tarpuskaitos sąskaita</span><span class="sxs-lookup"><span data-stu-id="643a9-454">Clearing account</span></span>    | <span data-ttu-id="643a9-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-455">1,000.00</span></span> |          |
| <span data-ttu-id="643a9-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="643a9-456">Ledger</span></span>       | <span data-ttu-id="643a9-457">1</span><span class="sxs-lookup"><span data-stu-id="643a9-457">1</span></span>              | <span data-ttu-id="643a9-458">Pasirinktinis</span><span class="sxs-lookup"><span data-stu-id="643a9-458">Custom</span></span> | <span data-ttu-id="643a9-459">Nuomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="643a9-459">Lease expense</span></span>       |          | <span data-ttu-id="643a9-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-460">1,000.00</span></span> |

<span data-ttu-id="643a9-461">Kai jau pašalinsite įstatyminio žurnalo įrašus, užsakysite visus žurnalo įrašus, kurių IFRS 16 knygoje reikalaujama pagal IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="643a9-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="643a9-462">Šie įrašai apima pradinį naudojimo teise valdomo turto ir įsipareigojimo pripažinimą bei palūkanų ir nusidėvėjimo įrašą.</span><span class="sxs-lookup"><span data-stu-id="643a9-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="643a9-463">Pradinis pripažinimas – 2020-01-01 – JE 140</span><span class="sxs-lookup"><span data-stu-id="643a9-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="643a9-464">Kodo tipas</span><span class="sxs-lookup"><span data-stu-id="643a9-464">Account type</span></span> | <span data-ttu-id="643a9-465">Sąskaitos numeris</span><span class="sxs-lookup"><span data-stu-id="643a9-465">Account number</span></span> | <span data-ttu-id="643a9-466">Sluoksnis</span><span class="sxs-lookup"><span data-stu-id="643a9-466">Layer</span></span>  | <span data-ttu-id="643a9-467">Sąskaitos aprašas</span><span class="sxs-lookup"><span data-stu-id="643a9-467">Account description</span></span>      | <span data-ttu-id="643a9-468">Debetas</span><span class="sxs-lookup"><span data-stu-id="643a9-468">Debit</span></span>     | <span data-ttu-id="643a9-469">Kreditas</span><span class="sxs-lookup"><span data-stu-id="643a9-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="643a9-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="643a9-470">Ledger</span></span>       | <span data-ttu-id="643a9-471">6</span><span class="sxs-lookup"><span data-stu-id="643a9-471">6</span></span>              | <span data-ttu-id="643a9-472">Pasirinktinis</span><span class="sxs-lookup"><span data-stu-id="643a9-472">Custom</span></span> | <span data-ttu-id="643a9-473">Naudojimo teise valdomas turtas</span><span class="sxs-lookup"><span data-stu-id="643a9-473">ROU Asset</span></span>                | <span data-ttu-id="643a9-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="643a9-474">22,793.90</span></span> |           |
| <span data-ttu-id="643a9-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="643a9-475">Ledger</span></span>       | <span data-ttu-id="643a9-476">7</span><span class="sxs-lookup"><span data-stu-id="643a9-476">7</span></span>              | <span data-ttu-id="643a9-477">Pasirinktinis</span><span class="sxs-lookup"><span data-stu-id="643a9-477">Custom</span></span> | <span data-ttu-id="643a9-478">Finansinės nuomos įsipareigojimas</span><span class="sxs-lookup"><span data-stu-id="643a9-478">Finance lease obligation</span></span> |           | <span data-ttu-id="643a9-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="643a9-479">22,793.90</span></span> |

<span data-ttu-id="643a9-480">Nuomos mokestis registruojamas taip, kaip kiti nuomos mokesčiai.</span><span class="sxs-lookup"><span data-stu-id="643a9-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="643a9-481">Tarpuskaitos sąskaitos naudojimo priežastis – užtikrinti, kad grynieji pinigai būtų kredituoti tik vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="643a9-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="643a9-482">Nuomos mokestis – 2020-01-31 – JE 150</span><span class="sxs-lookup"><span data-stu-id="643a9-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="643a9-483">Kodo tipas</span><span class="sxs-lookup"><span data-stu-id="643a9-483">Account type</span></span> | <span data-ttu-id="643a9-484">Sąskaitos numeris</span><span class="sxs-lookup"><span data-stu-id="643a9-484">Account number</span></span> | <span data-ttu-id="643a9-485">Sluoksnis</span><span class="sxs-lookup"><span data-stu-id="643a9-485">Layer</span></span>  | <span data-ttu-id="643a9-486">Sąskaitos aprašas</span><span class="sxs-lookup"><span data-stu-id="643a9-486">Account description</span></span>      | <span data-ttu-id="643a9-487">Debetas</span><span class="sxs-lookup"><span data-stu-id="643a9-487">Debit</span></span>    | <span data-ttu-id="643a9-488">Kreditas</span><span class="sxs-lookup"><span data-stu-id="643a9-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="643a9-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="643a9-489">Ledger</span></span>       | <span data-ttu-id="643a9-490">7</span><span class="sxs-lookup"><span data-stu-id="643a9-490">7</span></span>              | <span data-ttu-id="643a9-491">Pasirinktinis</span><span class="sxs-lookup"><span data-stu-id="643a9-491">Custom</span></span> | <span data-ttu-id="643a9-492">Finansinės nuomos įsipareigojimas</span><span class="sxs-lookup"><span data-stu-id="643a9-492">Finance lease obligation</span></span> | <span data-ttu-id="643a9-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-493">1,000.00</span></span> |          |
| <span data-ttu-id="643a9-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="643a9-494">Ledger</span></span>       | <span data-ttu-id="643a9-495">4</span><span class="sxs-lookup"><span data-stu-id="643a9-495">4</span></span>              | <span data-ttu-id="643a9-496">Pasirinktinis</span><span class="sxs-lookup"><span data-stu-id="643a9-496">Custom</span></span> | <span data-ttu-id="643a9-497">Tarpuskaitos sąskaita</span><span class="sxs-lookup"><span data-stu-id="643a9-497">Clearing account</span></span>         |          | <span data-ttu-id="643a9-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="643a9-498">1,000.00</span></span> |

<span data-ttu-id="643a9-499">Palūkanų sąnaudų žurnalo įrašas generuojamas iš įsipareigojimo amortizacijos grafiko.</span><span class="sxs-lookup"><span data-stu-id="643a9-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="643a9-500">Palūkanų sąnaudos – 2020-01-31 – JE 160</span><span class="sxs-lookup"><span data-stu-id="643a9-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="643a9-501">Kodo tipas</span><span class="sxs-lookup"><span data-stu-id="643a9-501">Account type</span></span> | <span data-ttu-id="643a9-502">Sąskaitos numeris</span><span class="sxs-lookup"><span data-stu-id="643a9-502">Account number</span></span> | <span data-ttu-id="643a9-503">Sluoksnis</span><span class="sxs-lookup"><span data-stu-id="643a9-503">Layer</span></span>  | <span data-ttu-id="643a9-504">Sąskaitos aprašas</span><span class="sxs-lookup"><span data-stu-id="643a9-504">Account description</span></span>      | <span data-ttu-id="643a9-505">Debetas</span><span class="sxs-lookup"><span data-stu-id="643a9-505">Debit</span></span> | <span data-ttu-id="643a9-506">Kreditas</span><span class="sxs-lookup"><span data-stu-id="643a9-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="643a9-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="643a9-507">Ledger</span></span>       | <span data-ttu-id="643a9-508">8</span><span class="sxs-lookup"><span data-stu-id="643a9-508">8</span></span>              | <span data-ttu-id="643a9-509">Pasirinktinis</span><span class="sxs-lookup"><span data-stu-id="643a9-509">Custom</span></span> | <span data-ttu-id="643a9-510">Palūkanų išlaidos</span><span class="sxs-lookup"><span data-stu-id="643a9-510">Interest expense</span></span>         | <span data-ttu-id="643a9-511">94.97</span><span class="sxs-lookup"><span data-stu-id="643a9-511">94.97</span></span> |        |
| <span data-ttu-id="643a9-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="643a9-512">Ledger</span></span>       | <span data-ttu-id="643a9-513">7</span><span class="sxs-lookup"><span data-stu-id="643a9-513">7</span></span>              | <span data-ttu-id="643a9-514">Pasirinktinis</span><span class="sxs-lookup"><span data-stu-id="643a9-514">Custom</span></span> | <span data-ttu-id="643a9-515">Finansinės nuomos įsipareigojimas</span><span class="sxs-lookup"><span data-stu-id="643a9-515">Finance lease obligation</span></span> |       | <span data-ttu-id="643a9-516">94.97</span><span class="sxs-lookup"><span data-stu-id="643a9-516">94.97</span></span>  |

<span data-ttu-id="643a9-517">Nusidėvėjimo išlaidų žurnalo įrašas generuojamas iš turto nusidėvėjimo grafiko.</span><span class="sxs-lookup"><span data-stu-id="643a9-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="643a9-518">Nusidėvėjimo išlaidos – 2020-01-31 – JE 170</span><span class="sxs-lookup"><span data-stu-id="643a9-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="643a9-519">Kodo tipas</span><span class="sxs-lookup"><span data-stu-id="643a9-519">Account type</span></span> | <span data-ttu-id="643a9-520">Sąskaitos numeris</span><span class="sxs-lookup"><span data-stu-id="643a9-520">Account number</span></span> | <span data-ttu-id="643a9-521">Sluoksnis</span><span class="sxs-lookup"><span data-stu-id="643a9-521">Layer</span></span>  | <span data-ttu-id="643a9-522">Sąskaitos aprašas</span><span class="sxs-lookup"><span data-stu-id="643a9-522">Account description</span></span>      | <span data-ttu-id="643a9-523">Debetas</span><span class="sxs-lookup"><span data-stu-id="643a9-523">Debit</span></span>  | <span data-ttu-id="643a9-524">Kreditas</span><span class="sxs-lookup"><span data-stu-id="643a9-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="643a9-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="643a9-525">Ledger</span></span>       | <span data-ttu-id="643a9-526">10</span><span class="sxs-lookup"><span data-stu-id="643a9-526">10</span></span>             | <span data-ttu-id="643a9-527">Pasirinktinis</span><span class="sxs-lookup"><span data-stu-id="643a9-527">Custom</span></span> | <span data-ttu-id="643a9-528">Likvidavimo išlaidos</span><span class="sxs-lookup"><span data-stu-id="643a9-528">Depreciation expense</span></span>     | <span data-ttu-id="643a9-529">949.75</span><span class="sxs-lookup"><span data-stu-id="643a9-529">949.75</span></span> |        |
| <span data-ttu-id="643a9-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="643a9-530">Ledger</span></span>       | <span data-ttu-id="643a9-531">11</span><span class="sxs-lookup"><span data-stu-id="643a9-531">11</span></span>             | <span data-ttu-id="643a9-532">Pasirinktinis</span><span class="sxs-lookup"><span data-stu-id="643a9-532">Custom</span></span> | <span data-ttu-id="643a9-533">Sukauptas nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="643a9-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="643a9-534">949.75</span><span class="sxs-lookup"><span data-stu-id="643a9-534">949.75</span></span> |

<span data-ttu-id="643a9-535">Kai bus sukurti ir užregistruoti visi šie žurnalo įrašai, matysite tolesnes „1 pasirinktinio sluoksnio“ reikšmes.</span><span class="sxs-lookup"><span data-stu-id="643a9-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="643a9-536">Atkreipkite dėmesį, kad į paskutinį stulpelį įtrauktas banko mokestis, pridėtinės vertės mokesčio (PVM) išlaidos ir grynųjų pinigų sumažinimas iš ankstesnio sluoksnio, tačiau jis neapima privalomųjų ataskaitų žurnalo įrašų.</span><span class="sxs-lookup"><span data-stu-id="643a9-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="643a9-537">Todėl galite išnaudoti dvigubų ataskaitų galimybes.</span><span class="sxs-lookup"><span data-stu-id="643a9-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="643a9-538">Dabar įmonė tiesiog turi vykdyti bandomąjį balansą ir sujungti dabartinį sluoksnį su standartiniu sluoksniu, kad sukurtų IFRS bandomąjį balansą.</span><span class="sxs-lookup"><span data-stu-id="643a9-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="643a9-539">Sąskaitos Nr.</span><span class="sxs-lookup"><span data-stu-id="643a9-539">Account No</span></span> | <span data-ttu-id="643a9-540">aprašymas</span><span class="sxs-lookup"><span data-stu-id="643a9-540">Description</span></span>              | <span data-ttu-id="643a9-541">Įstatyminė knyga\-Dabartinis sluoksnis\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="643a9-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="643a9-542">Įstatyminė knyga\-Dabartinis sluoksnis\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="643a9-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="643a9-543">Įstatyminė knyga\-Dabartinis sluoksnis\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="643a9-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="643a9-544">Dabartinis sluoksnis \- Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="643a9-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="643a9-545">Atšaukimo knyga\-Pasirinktinis sluoksnis\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="643a9-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="643a9-546">IFRS 16 knyga\-Pasirinktinis sluoksnis\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="643a9-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="643a9-547">IFRS 16 knyga\-Pasirinktinis sluoksnis\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="643a9-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="643a9-548">IFRS 16 knyga\-Pasirinktinis sluoksnis\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="643a9-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="643a9-549">IFRS 16 knyga\-Pasirinktinis sluoksnis\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="643a9-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="643a9-550">Pasirinktinis sluoksnis \+ Dabartinis sluoksnis \- Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="643a9-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="643a9-551">1</span><span class="sxs-lookup"><span data-stu-id="643a9-551">1</span></span>          | <span data-ttu-id="643a9-552">Nuomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="643a9-552">Lease expense</span></span>            | <span data-ttu-id="643a9-553">1,000 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="643a9-554">1,000 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-554">1,000\.00</span></span>               |   | <span data-ttu-id="643a9-555">–1 000</span><span class="sxs-lookup"><span data-stu-id="643a9-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="643a9-556">0 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-556">0\.00</span></span>                                   |
| <span data-ttu-id="643a9-557">2</span><span class="sxs-lookup"><span data-stu-id="643a9-557">2</span></span>          | <span data-ttu-id="643a9-558">Banko mokestis</span><span class="sxs-lookup"><span data-stu-id="643a9-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="643a9-559">3 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="643a9-560">3 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="643a9-561">3 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-561">3\.00</span></span>                                   |
| <span data-ttu-id="643a9-562">3</span><span class="sxs-lookup"><span data-stu-id="643a9-562">3</span></span>          | <span data-ttu-id="643a9-563">PVM išlaidos</span><span class="sxs-lookup"><span data-stu-id="643a9-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="643a9-564">5 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="643a9-565">5 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="643a9-566">5 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-566">5\.00</span></span>                                   |
| <span data-ttu-id="643a9-567">4</span><span class="sxs-lookup"><span data-stu-id="643a9-567">4</span></span>          | <span data-ttu-id="643a9-568">Tarpuskaitos sąskaita</span><span class="sxs-lookup"><span data-stu-id="643a9-568">Clearing account</span></span>         | <span data-ttu-id="643a9-569">–1 000,00</span><span class="sxs-lookup"><span data-stu-id="643a9-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="643a9-570">1,000 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="643a9-571">0 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-571">0\.00</span></span>                   |   | <span data-ttu-id="643a9-572">1000</span><span class="sxs-lookup"><span data-stu-id="643a9-572">1,000</span></span>                                           |                                                | <span data-ttu-id="643a9-573">–1 000</span><span class="sxs-lookup"><span data-stu-id="643a9-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="643a9-574">0 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-574">0\.00</span></span>                                   |
| <span data-ttu-id="643a9-575">5</span><span class="sxs-lookup"><span data-stu-id="643a9-575">5</span></span>          | <span data-ttu-id="643a9-576">Mokėtinos sumos</span><span class="sxs-lookup"><span data-stu-id="643a9-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="643a9-577">–1 008,00</span><span class="sxs-lookup"><span data-stu-id="643a9-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="643a9-578">1,008 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-578">1,008\.00</span></span>                                         | <span data-ttu-id="643a9-579">0 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="643a9-580">0 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-580">0\.00</span></span>                                   |
| <span data-ttu-id="643a9-581">6</span><span class="sxs-lookup"><span data-stu-id="643a9-581">6</span></span>          | <span data-ttu-id="643a9-582">Naudojimo teise valdomas turtas</span><span class="sxs-lookup"><span data-stu-id="643a9-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="643a9-583">0 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="643a9-584">22,794</span><span class="sxs-lookup"><span data-stu-id="643a9-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="643a9-585">22,793 \. 90</span><span class="sxs-lookup"><span data-stu-id="643a9-585">22,793\.90</span></span>                              |
| <span data-ttu-id="643a9-586">7</span><span class="sxs-lookup"><span data-stu-id="643a9-586">7</span></span>          | <span data-ttu-id="643a9-587">Finansinės nuomos įsipareigojimas</span><span class="sxs-lookup"><span data-stu-id="643a9-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="643a9-588">0 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="643a9-589">–22 794</span><span class="sxs-lookup"><span data-stu-id="643a9-589">\-22,794</span></span>                                       | <span data-ttu-id="643a9-590">1000</span><span class="sxs-lookup"><span data-stu-id="643a9-590">1,000</span></span>                                          | <span data-ttu-id="643a9-591">–94,97</span><span class="sxs-lookup"><span data-stu-id="643a9-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="643a9-592">–21 888,87</span><span class="sxs-lookup"><span data-stu-id="643a9-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="643a9-593">8</span><span class="sxs-lookup"><span data-stu-id="643a9-593">8</span></span>          | <span data-ttu-id="643a9-594">Palūkanų išlaidos</span><span class="sxs-lookup"><span data-stu-id="643a9-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="643a9-595">0 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="643a9-596">94 \. 97</span><span class="sxs-lookup"><span data-stu-id="643a9-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="643a9-597">94 \. 97</span><span class="sxs-lookup"><span data-stu-id="643a9-597">94\.97</span></span>                                  |
| <span data-ttu-id="643a9-598">9</span><span class="sxs-lookup"><span data-stu-id="643a9-598">9</span></span>          | <span data-ttu-id="643a9-599">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="643a9-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="643a9-600">–1 008,00</span><span class="sxs-lookup"><span data-stu-id="643a9-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="643a9-601">–1 008,00</span><span class="sxs-lookup"><span data-stu-id="643a9-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="643a9-602">–1 008,00</span><span class="sxs-lookup"><span data-stu-id="643a9-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="643a9-603">10</span><span class="sxs-lookup"><span data-stu-id="643a9-603">10</span></span>         | <span data-ttu-id="643a9-604">Likvidavimo išlaidos</span><span class="sxs-lookup"><span data-stu-id="643a9-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="643a9-605">0 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="643a9-606">949 \. 75</span><span class="sxs-lookup"><span data-stu-id="643a9-606">949\.75</span></span>                                        | <span data-ttu-id="643a9-607">949 \. 75</span><span class="sxs-lookup"><span data-stu-id="643a9-607">949\.75</span></span>                                 |
| <span data-ttu-id="643a9-608">11</span><span class="sxs-lookup"><span data-stu-id="643a9-608">11</span></span>         | <span data-ttu-id="643a9-609">Sukauptas nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="643a9-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="643a9-610">0 \. 00</span><span class="sxs-lookup"><span data-stu-id="643a9-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="643a9-611">–949,75</span><span class="sxs-lookup"><span data-stu-id="643a9-611">\-949\.75</span></span>                                      | <span data-ttu-id="643a9-612">–949,75</span><span class="sxs-lookup"><span data-stu-id="643a9-612">\-949\.75</span></span>                               |


