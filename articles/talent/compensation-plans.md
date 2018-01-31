---
title: "Kompensacijų planai"
description: "Kompensacijų ir išmokų vadovai gali naudoti Kompensavimo valdymą, skirtą prižiūrėti ir apdoroti organizacijos darbuotojų pastoviųjų ir kintamųjų atlyginimo dalių planus."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 4a25daf94499d12d720a494f3895726f5e7ebcdb
ms.contentlocale: lt-lt
ms.lasthandoff: 01/31/2018

---

# <a name="compensation-plans"></a><span data-ttu-id="1ba5d-103">Kompensacijų planai</span><span class="sxs-lookup"><span data-stu-id="1ba5d-103">Compensation plans</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="1ba5d-104">Kompensacijų ir išmokų vadovai gali naudoti Kompensavimo valdymą, skirtą prižiūrėti ir apdoroti organizacijos darbuotojų pastoviųjų ir kintamųjų atlyginimo dalių planus.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-104">Compensation and Benefits Managers can use Compensation management to maintain and process fixed and variable compensation plans for the organization's employees.</span></span>

### <a name="introduction"></a><span data-ttu-id="1ba5d-105">Įžanga</span><span class="sxs-lookup"><span data-stu-id="1ba5d-105">Introduction</span></span>

<span data-ttu-id="1ba5d-106">Kompensacijų valdymas naudojamas kontroliuoti pagrindinio užmokesčio ir premijų pristatymui.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-106">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="1ba5d-107">Darbuotojo fiksuotas pagrindinis užmokestis ir nuopelnų padidėjimai kontroliuojami naudojant pastoviosios kompensacijos dalies planus.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-107">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="1ba5d-108">Skatinamųjų išmokų, pvz., priedų, apdovanojimų už našumą, akcijų pasirinkimo sandorių, subsidijų bei vienkartinių premijų mokėjimas valdomas naudojant kintamosios kompensacijos dalies planus.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-108">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span> 

<span data-ttu-id="1ba5d-109">Darbuotojai gali būti registruojami vienam arba keliems abiejų tipų planams.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-109">Employees can be enrolled in one or more plans of both types.</span></span> <span data-ttu-id="1ba5d-110">Kad turėtų teisę registruotis kompensavimo planui, darbuotojas turi atitikti toliau nurodytus reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-110">An employee must meet the following requirements in order to be eligible for enrollment in a compensation plan:</span></span>
-   <span data-ttu-id="1ba5d-111">Darbuotojui turi būti priskirtos aktyvios pareigos.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-111">The employee must have an active position assignment.</span></span>
-   <span data-ttu-id="1ba5d-112">Darbuotojas turi atitikti kriterijus, kuriuos apibrėžia kompensavimo plano tinkamumo taisyklės.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-112">The employee must meet the criteria that are defined by eligibility rules for a compensation plan.</span></span>

## <a name="compensation-setup"></a><span data-ttu-id="1ba5d-113"> Kompensavimo sąranka</span><span class="sxs-lookup"><span data-stu-id="1ba5d-113">Compensation setup</span></span>
<span data-ttu-id="1ba5d-114">Toliau pateiktoje lentelėje išvardijami kompensavimo proceso komponentai, kurie gali būti itin svarbūs nustatant jūsų įmonės kompensavimo planus.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-114">The following table lists components of the compensation process that can be integral in setting up your company's compensation plans.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1ba5d-115">Komponentas</span><span class="sxs-lookup"><span data-stu-id="1ba5d-115">Component</span></span></th>
<th><span data-ttu-id="1ba5d-116">Daugiau informacijos...</span><span class="sxs-lookup"><span data-stu-id="1ba5d-116">More information…</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1ba5d-117">Pastoviosios atlyginimo dalies veiksmai</span><span class="sxs-lookup"><span data-stu-id="1ba5d-117">Fixed compensation actions</span></span></td>
<td><span data-ttu-id="1ba5d-118">Pastoviosios kompensavimo dalies veiksmais pasiekiama toliau nurodytų dviejų tikslų.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-118">Fixed compensation actions accomplish two purposes:</span></span>
<ul>
<li><span data-ttu-id="1ba5d-119">Veiksmai gali nurodyti, kokią informaciją reikia įrašyti, kai pasikeičia darbuotojo kompensavimas.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-119">Actions can specify the kind of information that must be recorded when an employee’s compensation changes.</span></span> <span data-ttu-id="1ba5d-120">Pavyzdžiui, galite reikalauti, kad būtų įrašoma pokyčio priežastis, pvz., paaukštinimas arba pažeminimas pareigose.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-120">For example, you can require that the reason a change, such as a promotion or a demotion be recorded.</span></span></li>
<li><span data-ttu-id="1ba5d-121">Veiksmai gali užtikrinti, kad, apdorojant pastoviosios kompensacijos dalies planus, būtų taikomas skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-121">Actions can ensure that a calculation is applied when fixed compensation plans are processed.</span></span>  <span data-ttu-id="1ba5d-122">Pvz., tipo Kapitalas veiksmai darbuotojų užmokestį palygins su darbuotojo lygio minimaliu atskaitos tašku ir užtikrins, kad darbuotojui būtų mokamas bent minimumas.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-122">For example, actions of type Equity will compare the employees pay to the minimum reference point for the level on the employee's and ensure the employee is getting paid at least the minimum.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ba5d-123">Lygiai</span><span class="sxs-lookup"><span data-stu-id="1ba5d-123">Levels</span></span></td>
<td><span data-ttu-id="1ba5d-124">Lygiai yra susieti su darbais ir visomis pareigomis, kurios yra susijusios su darbo nuoroda.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-124">Levels are associated with jobs and any positions that are related to a job reference.</span></span> <span data-ttu-id="1ba5d-125">Galite kurti šių trijų kompensavimo planų atskirus lygius: Kategorijų, Intervalų ir Pakopų.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-125">You can create discrete levels for the three types of compensation plans: Grade, Band, and Step.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ba5d-126">Diapazono realizavimo matrica</span><span class="sxs-lookup"><span data-stu-id="1ba5d-126">Range utilization matrix</span></span></td>
<td><span data-ttu-id="1ba5d-127">Diapazono realizavimo matrica padeda darbuotojus perkelti į jų darbų kontrolinį tašką.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-127">A range utilization matrix helps you transition employees to the control point for their jobs.</span></span> <span data-ttu-id="1ba5d-128">Taip pat galite naudoti diapazono realizavimą, norėdami valdyti mokėjimo koeficiento kapitalą įmonės viduje neatsižvelgiant į kiekvieno darbuotojo darbą ar visos įmonės darbą.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-128">You can also use range utilization to control pay rate equity in the company without regard to an individual employee's performance or the overall performance of the company.</span></span> <span data-ttu-id="1ba5d-129">Pavyzdžiui, darbuotojai, kuriems sumokama mažiau, nei numatyta pagal diapazoną, gauna didesnio procento padidinimą, nei tie darbuotojai, kuriems pagal diapazoną mokama daugiau.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-129">For example, employees who are paid lower in their range get higher percentage increases than employees who are paid higher in the range.</span></span> <span data-ttu-id="1ba5d-130">Tokiu būdu galite sistematiškai balansuoti kapitalo skirtumus.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-130">In this manner, you can systematically offset equity differences.</span></span> <span data-ttu-id="1ba5d-131">Diapazono realizavimas apskaičiuojamas taip: (Fiksuotas užmokesčio tarifas – Diapazono minimumas) ÷ (Diapazono maksimumas – Diapazono minimumas).</span><span class="sxs-lookup"><span data-stu-id="1ba5d-131">The range utilization is calculated as follows: (Fixed Pay Rate - Range Minimum) ÷ (Range Maximum - Range Minimum).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ba5d-132">Atskaitos taškų nustatymai</span><span class="sxs-lookup"><span data-stu-id="1ba5d-132">Reference point setups</span></span></td>
<td><span data-ttu-id="1ba5d-133">Atskaitos taškų sąranka apima atskaitos taškų, sudarančių intervalus mokėjimo koeficientų matricoje, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-133">A reference point setup includes a set of reference points that represent ranges in a matrix.</span></span> <span data-ttu-id="1ba5d-134">Kiekvieną diapazoną galima susieti su užmokesčio tarifu.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-134">Each range can be associated with a pay rate.</span></span> <span data-ttu-id="1ba5d-135">Pvz., kategorijų planų atskaitos taškai dažnai bus Minimumo, Vidurio ir Maksimumo.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-135">For example, grade plans will often have reference points of Minimum, Midpoint, and Maximum.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ba5d-136">Kompensavimo matrica</span><span class="sxs-lookup"><span data-stu-id="1ba5d-136">Compensation matrix</span></span></td>
<td><span data-ttu-id="1ba5d-137">Kompensavimo matrica yra atskaitos taškų ir lygių rinkinys, kurį naudojate kurdami kompensavimo struktūrą.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-137">A compensation matrix is the set of reference points and levels that you use to create a compensation structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ba5d-138">Kompensavimo struktūra</span><span class="sxs-lookup"><span data-stu-id="1ba5d-138">Compensation structure</span></span></td>
<td><span data-ttu-id="1ba5d-139">Kompensavimo struktūra yra kompensavimo matrica, kurioje užmokesčio tarifai susieti su kiekvieno lygio atskaitos taškais.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-139">A compensation structure is a compensation matrix that has pay rates associated with the reference points for each level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ba5d-140">Tinkamumo taisyklė</span><span class="sxs-lookup"><span data-stu-id="1ba5d-140">Eligibility rules</span></span></td>
<td><span data-ttu-id="1ba5d-141">Tinkamumo taisyklės naudojamos identifikuoti konkrečių darbų, darbų funkcijų, darbų tipų, skyrių, profesinių sąjungų ar kompensavimo regionų darbuotojams, kuriems taikomi konkretūs kompensavimo planai.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-141">Eligibility rules are used to identify employees in specific jobs, job functions, job types, departments, labor unions, or compensation regions that are covered by specific compensation plans.</span></span> <span data-ttu-id="1ba5d-142">Norėdami darbuotojus užregistruoti į planą, turite sukurti tiek kintamosios, tiek pastoviosios kompensavimo dalies planų tinkamumo taisykles.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-142">You must create eligibility rules for both variable and fixed compensation plans in order to enroll employees in the plan.</span></span> <span data-ttu-id="1ba5d-143">Kai nurodytos kompensavimo plano tinkamumo taisyklės, galite apibrėžti lygius, kurie turėtų būti taikomi darbams, kuriems taikomas planas.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-143">After eligibility rules are specified for a compensation plan, you can define the levels that should apply to the jobs that are covered by the plan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ba5d-144">Išmokų dažnumas</span><span class="sxs-lookup"><span data-stu-id="1ba5d-144">Pay frequencies</span></span></td>
<td><span data-ttu-id="1ba5d-145">Darbo užmokesčio dažniai yra naudojami apibrėžti laikotarpiui, kuriam nurodytas kompensavimas.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-145">Pay frequencies are used to define the time period for which the compensation is specified.</span></span>  <span data-ttu-id="1ba5d-146">Pvz., darbo užmokesčio dažnis padeda suprasti, ar kompensacijos suma nurodyta kaip metinis atlyginimas ar kaip valandinis darbo užmokesčio tarifas.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-146">For example, the pay frequency helps you understand if the compensation amount is specified as an annual salary versus an hourly pay rate.</span></span> <span data-ttu-id="1ba5d-147">Darbo užmokesčio dažniai taip pat naudojami nustatyti konvertavimo koeficientams, kuriais kompensavimo sumos iš mėnesinio, savaitinio, dvisavaitinio ir valandinio užmokesčio dažnių konvertuojamos į metinį užmokesčio dažnį.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-147">Pay frequencies are also used to set up conversion factors to convert compensation amounts from monthly, weekly, biweekly and hourly pay frequencies to an annual pay frequency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ba5d-148">Kompensacijos sritys</span><span class="sxs-lookup"><span data-stu-id="1ba5d-148">Compensation regions</span></span></td>
<td><span data-ttu-id="1ba5d-149">Kompensavimo regionai naudojami darbuotojo kompensacijai nurodyti pagal darbo vietą.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-149">Compensation regions are used to specify employee compensation based on the location of the workplace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ba5d-150">Kontrolinis taškas</span><span class="sxs-lookup"><span data-stu-id="1ba5d-150">Control point</span></span></td>
<td><span data-ttu-id="1ba5d-151">Kontrolinis taškas apibrėžia jūsų manymu idealų mokėjimo tarifą visiems darbuotojams atlyginimo lygyje.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-151">The control point defines what you consider to be the ideal pay rate for all employees at a compensation level.</span></span> <span data-ttu-id="1ba5d-152">Kategorijų plano struktūrų kontroliniai taškai paprastai yra diapazonų vidurio taškai.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-152">For grade plan structures, control points are typically the midpoint of the ranges.</span></span> <span data-ttu-id="1ba5d-153">Intervalų struktūrose kontroliniai taškai naudojami retai.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-153">Band structures rarely use control points.</span></span> <span data-ttu-id="1ba5d-154">Pastoviosios kompensacijos dalies kontrolinį tašką galite nurodyti Pastoviosios kompensacijos dalies planų formoje.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-154">You can specify the control point for a fixed compensation plan in the Fixed compensation plans form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ba5d-155">Užduoties funkcijos</span><span class="sxs-lookup"><span data-stu-id="1ba5d-155">Job functions</span></span></td>
<td><span data-ttu-id="1ba5d-156">Darbų funkcijos naudojamos norint kompensavimo planus klasifikuoti ir filtruoti tam tikriems darbams.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-156">Job functions are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ba5d-157">Užduočių tipai</span><span class="sxs-lookup"><span data-stu-id="1ba5d-157">Job types</span></span></td>
<td><span data-ttu-id="1ba5d-158">Darbų tipai naudojami norint kompensavimo planus klasifikuoti ir filtruoti tam tikriems darbams.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-158">Job types are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ba5d-159">Kintamosios atlyginimo dalies tipai</span><span class="sxs-lookup"><span data-stu-id="1ba5d-159">Variable compensation types</span></span></td>
<td><span data-ttu-id="1ba5d-160">Kintamosios kompensacijos dalies tipai, pvz., akcijų ar grynųjų pinigų premijos, yra nustatomos kintamosios kompensacijos dalies planuose.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-160">Variable compensation types, such as stock awards or cash award bonuses, are set up in variable compensation plans.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ba5d-161">Kompensavimo tinkleliai</span><span class="sxs-lookup"><span data-stu-id="1ba5d-161">Compensation grids</span></span></td>
<td><span data-ttu-id="1ba5d-162">Kompensavimo tinkleliuose yra kompensavimo struktūra.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-162">Compensation grids contain the compensation structure.</span></span>  <span data-ttu-id="1ba5d-163">Kompensavimo tinklelius gali naudoti vienas ar keli kompensavimo planai.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-163">Compensation grids can be used by one or more compensation plans.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ba5d-164">Veiklos efektyvumo planai</span><span class="sxs-lookup"><span data-stu-id="1ba5d-164">Performance plans</span></span></td>
<td><span data-ttu-id="1ba5d-165">Našumo planai naudojami našumui susieti su paskirstymo matrica, kad galėtumėte naudoti planą su mokėjimo už našumą strategija.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-165">Performance plans are used to associate performance with an allocation matrix, so that you can use the plan in a pay-for-performance strategy.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ba5d-166">Veiklos efektyvumo vertinimas</span><span class="sxs-lookup"><span data-stu-id="1ba5d-166">Performance ratings</span></span></td>
<td><span data-ttu-id="1ba5d-167">Našumo vertinimai naudojami našumo planuose premijos ar našumo apdovanojimui nustatyti.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-167">Performance ratings are used in performance plans to determine the amount of a merit award or performance award.</span></span></td>
</tr>
</tbody>
</table>

## <a name="process-events"></a><span data-ttu-id="1ba5d-168">Apdorojimo įvykiai</span><span class="sxs-lookup"><span data-stu-id="1ba5d-168">Process events</span></span>
<span data-ttu-id="1ba5d-169">Apdorojimo įvykis skaičiuoja tam tikro laikotarpio kompensavimo informaciją visiems darbuotojams, kurie yra įtraukti į vieną ar daugiau pastoviosios ar kintamosios atlyginimo dalies planų.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-169">A process event calculates compensation information for a specific period for all employees who are enrolled in one or more fixed or variable compensation plans.</span></span> <span data-ttu-id="1ba5d-170">Galite pakartotinai paleisti apdorojimo įvykį, jei norite patikrinti ar atnaujinti kompensacijų skaičiavimo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-170">You can run a process event repeatedly to test or update calculated compensation results.</span></span>

<a name="compensation-events"></a><span data-ttu-id="1ba5d-171">Kompensavimo įvykiai</span><span class="sxs-lookup"><span data-stu-id="1ba5d-171">Compensation events</span></span>
-------------------

<span data-ttu-id="1ba5d-172">Kiekvieną kartą vykdant apdorojimo įvykį, sukuriamas kompensavimo įvykis.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-172">Each time a process event is run, a compensation event is created.</span></span>  <span data-ttu-id="1ba5d-173">Kompensavimo įvykiuose yra kiekvieno darbuotojo, įtraukto į tą apdorojimo įvykį, kompensavimo proceso rezultatai.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-173">Compensation events contain the results of the compensation process for each employee included in that process event.</span></span>  <span data-ttu-id="1ba5d-174">Kai skaičiavimai yra teisingi, galite įkelti kompensavimo įvykį, kad atnaujintumėte darbuotojų, kuriuos paveikė apdorojimo įvykis, kompensacijų įrašus.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-174">When the calculations are correct, you can load the compensation event to update the compensation records for the employees who are affected by the process event.</span></span>

## <a name="recommendations"></a><span data-ttu-id="1ba5d-175"> Rekomendacijos</span><span class="sxs-lookup"><span data-stu-id="1ba5d-175">Recommendations</span></span>
<span data-ttu-id="1ba5d-176">Paleidę apdorojimo įvykį, pagal apskaičiuotas apdorojimo įvykio gaires galite rekomenduoti koreguoti darbuotojo nuopelnų padidėjimą ar premijos sumą.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-176">After you run a process event, you can recommend adjustments to an employee’s merit increase or award amount, based on the calculated guidelines of the process event.</span></span> <span data-ttu-id="1ba5d-177">Norėdami teikti rekomendacijas dėl darbuotojų, nustatydami kompensavimo planus arba apdorojimo įvykį turite įgalinti rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="1ba5d-177">To make recommendations for employees, you must enable recommendations when you set up compensation plans or when you set up the process event.</span></span>




