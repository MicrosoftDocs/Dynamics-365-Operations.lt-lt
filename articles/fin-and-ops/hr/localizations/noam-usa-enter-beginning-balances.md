---
title: "Algalapio pradžios balansų įvedimas"
description: "Temoje aprašomi pradžios balansų įvedimo veiksmai įvedant pajamų kodus, atskaitymus, išmokas ir mokesčius. Ši informacija yra naudinga partneriams perkeliant duomenis naujo algalapio diegimui iš kitos sistemos."
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 736eedf270ac08b0bdf9364821f8a7bae981ade9
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="55e6d-104">Algalapio pradžios balansų įvedimas</span><span class="sxs-lookup"><span data-stu-id="55e6d-104">Enter payroll beginning balances</span></span>

[!include[banner](../../includes/banner.md)]

<span data-ttu-id="55e6d-105">Temoje aprašomi pradžios balansų įvedimo veiksmai įvedant pajamų kodus, atskaitymus, išmokas ir mokesčius.</span><span class="sxs-lookup"><span data-stu-id="55e6d-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="55e6d-106">Ši informacija yra naudinga partneriams, kurie perkelia duomenis naujo algalapio diegimui iš kitos sistemos.</span><span class="sxs-lookup"><span data-stu-id="55e6d-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="55e6d-107">Kad pasiruoštume pradžios algalapių balansų įvedimui, patikriname šią informaciją:</span><span class="sxs-lookup"><span data-stu-id="55e6d-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

> * <span data-ttu-id="55e6d-108">Ar į sistemą įvesti ir pasiekiami darbuotojo įrašai</span><span class="sxs-lookup"><span data-stu-id="55e6d-108">Employee records are entered and available in the system</span></span>
> * <span data-ttu-id="55e6d-109">Darbuotojams nustatyti ir priskirti šie duomenys:</span><span class="sxs-lookup"><span data-stu-id="55e6d-109">The following data is set up and assigned to employees:</span></span>

> > * <span data-ttu-id="55e6d-110">Mokėjimo ciklai ir mokėjimo laikotarpiai</span><span class="sxs-lookup"><span data-stu-id="55e6d-110">Pay cycles and pay periods</span></span>
> > * <span data-ttu-id="55e6d-111">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="55e6d-111">Earning codes</span></span>
> > * <span data-ttu-id="55e6d-112">Mokesčiai</span><span class="sxs-lookup"><span data-stu-id="55e6d-112">Taxes</span></span>
> > * <span data-ttu-id="55e6d-113">Išmokos ir atskaitymai</span><span class="sxs-lookup"><span data-stu-id="55e6d-113">Benefits and deductions</span></span>

> * <span data-ttu-id="55e6d-114">Įmonė turėjo pasirinkti datą, nuo kurios galima nustatyti algalapio pradžios balansus.</span><span class="sxs-lookup"><span data-stu-id="55e6d-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>

> * <span data-ttu-id="55e6d-115">Buvo surinkta informacija apie visas pajamas, išmokas / atskaitymus, išmokos įmokas, darbuotojo mokamus mokesčius ir darbdavio mokamus mokesčius bei sumas nuo metų pradžios iš senesnės versijos sistemos.</span><span class="sxs-lookup"><span data-stu-id="55e6d-115">Information were gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="55e6d-116">Planuodami įvesti pradžios balansus, apsvarstykite, kiek išsamūs duomenys turėtų būti.</span><span class="sxs-lookup"><span data-stu-id="55e6d-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="55e6d-117">Dauguma įmonių įveda vieną, konsoliduotą sumą nuo metų pradžios iki dabartinės datos.</span><span class="sxs-lookup"><span data-stu-id="55e6d-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="55e6d-118">Tačiau jei reikia išsamesnės informacijos, balansus galima įvesti nurodant ketvirčio pokyčius.</span><span class="sxs-lookup"><span data-stu-id="55e6d-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="55e6d-119">Pagal reikalingą informacijos detalumo lygį nustatoma, kiek mokėjimo išrašų reikės rankiniu būdu sukurti kiekvienam darbininkui.</span><span class="sxs-lookup"><span data-stu-id="55e6d-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="55e6d-120">Vienai sumai nuo metų pradžios iki dabartinės datos kiekvienam darbuotojui reikia rankiniu būdu sukurti tiktai vieną išrašą.</span><span class="sxs-lookup"><span data-stu-id="55e6d-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="55e6d-121">Kad tai atliktumėte, naudokite sumas nuo metų pradžios iki dabartinės datos, pateikiamas ankstesnės sistemos galutinio mokėjimo išraše, kaip naujoje algalapio sistemoje įvestą sumą.</span><span class="sxs-lookup"><span data-stu-id="55e6d-121">To do this use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="55e6d-122">Šiame pavyzdyje parodyta, kaip galite įvesti darbuotojo algalapio pradžios balansus, įskaitant pajamų kodus, išmokas / atskaitymus ir mokesčius.</span><span class="sxs-lookup"><span data-stu-id="55e6d-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="55e6d-123">Realioje situacijoje turėtumėte kiekvieno uždarbio kodo, išmokos atskaitymo, išmokos įmokos, darbuotojo mokamo mokesčio ir darbdavio mokamo mokesčio eilutės elementą su įvesta suma nuo metų pradžios iki dabartinės datos.</span><span class="sxs-lookup"><span data-stu-id="55e6d-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="55e6d-124">Naudodami šį kodų ir sumų sąrašą, atlikite veiksmus, skirtus rankiniu būdu sukurti pajamų ir mokėjimo išrašą su išjungta apskaita, kad algalapio tikslu galėtumėte perkelti pradžios balansus.</span><span class="sxs-lookup"><span data-stu-id="55e6d-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span>  <span data-ttu-id="55e6d-125">Apskaitą išjungti reikia todėl, kad šis pradžios balanso mokėjimo išrašas nebūtų užregistruotas didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="55e6d-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="55e6d-126">Tai buvo padaryta senesnės versijos sistemoje ir veiks naujojoje sistemoje, jums nustačius pradžios balansus didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="55e6d-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="55e6d-127">A.</span><span class="sxs-lookup"><span data-stu-id="55e6d-127">A.</span></span> <span data-ttu-id="55e6d-128">Kaip nustatyti pajamų kodus, kurie bus naudojami algalapių pradžios balansuose</span><span class="sxs-lookup"><span data-stu-id="55e6d-128">How to set up earnings codes to be used on payroll beginning balances</span></span>
<span data-ttu-id="55e6d-129">Įvedę algalapio pradžios balansus, įsitikinkite, kad pajamų kodai, kuriuos naudosite, sukonfigūruoti su įjungta parinktimi „Leisti redaguoti pajamų išrašo tarifus“.</span><span class="sxs-lookup"><span data-stu-id="55e6d-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="55e6d-130">Tai leis jums rankiniu būdu įvesti sumą iš senesnės versijos sistemos.</span><span class="sxs-lookup"><span data-stu-id="55e6d-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="55e6d-131">B.</span><span class="sxs-lookup"><span data-stu-id="55e6d-131">B.</span></span> <span data-ttu-id="55e6d-132">Pajamų išrašo kūrimas darbuotojui, turinčiam pradžios balansą</span><span class="sxs-lookup"><span data-stu-id="55e6d-132">Create earnings statement for an employee to have a beginning balance</span></span>
<span data-ttu-id="55e6d-133">Šis veiksmas rankiniu būdu sukuria paskutinio mokėjimo laikotarpio senesnės versijos sistemoje pajamų išrašą kiekvienam darbininkui, ir taip sukuriamos pajamų išrašo eilutės naujoje algalapio sistemoje.</span><span class="sxs-lookup"><span data-stu-id="55e6d-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="55e6d-134">Įveskite po vieną eilutę kiekvienam pajamų kodui, sumas nuo metų pradžios iki dabartinės datos ir valandas.</span><span class="sxs-lookup"><span data-stu-id="55e6d-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="55e6d-135">Toliau pateikiami pavyzdiniai veiksmai.</span><span class="sxs-lookup"><span data-stu-id="55e6d-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="55e6d-136">Atidarykite puslapį **Visi pajamų išrašai** ir spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="55e6d-136">Open the **All earnings statements** page and click **New**.</span></span>  

<span data-ttu-id="55e6d-137">Įveskite toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="55e6d-137">Enter the following:</span></span> 

| <span data-ttu-id="55e6d-138">Laukas</span><span class="sxs-lookup"><span data-stu-id="55e6d-138">Field</span></span>      | <span data-ttu-id="55e6d-139">Vertė</span><span class="sxs-lookup"><span data-stu-id="55e6d-139">Value</span></span>                 |
|------------|-----------------------|
| <span data-ttu-id="55e6d-140">Darbininkas</span><span class="sxs-lookup"><span data-stu-id="55e6d-140">Worker</span></span>     | <span data-ttu-id="55e6d-141">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="55e6d-141">Michael Redmond</span></span>       |
| <span data-ttu-id="55e6d-142">Mokėjimo ciklas</span><span class="sxs-lookup"><span data-stu-id="55e6d-142">Pay cycle</span></span>  | <span data-ttu-id="55e6d-143">sm</span><span class="sxs-lookup"><span data-stu-id="55e6d-143">sm</span></span>                    |
| <span data-ttu-id="55e6d-144">Mokėjimo laikotarpis</span><span class="sxs-lookup"><span data-stu-id="55e6d-144">Pay period</span></span> | <span data-ttu-id="55e6d-145">2017.06.16–2017.06.30</span><span class="sxs-lookup"><span data-stu-id="55e6d-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="55e6d-146">Skirtuke **Pajamų išrašo eilutė** įveskite toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="55e6d-146">In the **Earnings statement line** tab, enter the following:</span></span>

<span data-ttu-id="55e6d-147">1 eilutė: skirtukas **Pajamų išrašo eilutė**</span><span class="sxs-lookup"><span data-stu-id="55e6d-147">Line 1: **Earning statement line** tab</span></span>

| <span data-ttu-id="55e6d-148">Laukas</span><span class="sxs-lookup"><span data-stu-id="55e6d-148">Field</span></span>            | <span data-ttu-id="55e6d-149">Vertė</span><span class="sxs-lookup"><span data-stu-id="55e6d-149">Value</span></span>       |
|------------------|-------------|
| <span data-ttu-id="55e6d-150">Pajamų kodas</span><span class="sxs-lookup"><span data-stu-id="55e6d-150">Earnings code</span></span>    | <span data-ttu-id="55e6d-151">Reguliarus mokėjimas</span><span class="sxs-lookup"><span data-stu-id="55e6d-151">Regular pay</span></span> |
| <span data-ttu-id="55e6d-152">Kiekis</span><span class="sxs-lookup"><span data-stu-id="55e6d-152">Quantity</span></span>         | <span data-ttu-id="55e6d-153">1,00</span><span class="sxs-lookup"><span data-stu-id="55e6d-153">1.00</span></span>        |
| <span data-ttu-id="55e6d-154">Diapazonas</span><span class="sxs-lookup"><span data-stu-id="55e6d-154">Rage</span></span>             | <span data-ttu-id="55e6d-155">30 000</span><span class="sxs-lookup"><span data-stu-id="55e6d-155">30,000</span></span>      |
| <span data-ttu-id="55e6d-156">Skirtukas Eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="55e6d-156">Line details tab</span></span> |             |
| <span data-ttu-id="55e6d-157">Neautomatinis</span><span class="sxs-lookup"><span data-stu-id="55e6d-157">Manual</span></span>           | <span data-ttu-id="55e6d-158">(pažymėta)</span><span class="sxs-lookup"><span data-stu-id="55e6d-158">(marked)</span></span>    |

<span data-ttu-id="55e6d-159">2 eilutė: skirtukas **Pajamų išrašo eilutė**</span><span class="sxs-lookup"><span data-stu-id="55e6d-159">Line 2: **Earning statement line** tab</span></span>

| <span data-ttu-id="55e6d-160">Laukas</span><span class="sxs-lookup"><span data-stu-id="55e6d-160">Field</span></span>            | <span data-ttu-id="55e6d-161">Vertė</span><span class="sxs-lookup"><span data-stu-id="55e6d-161">Value</span></span>    |
|------------------|----------|
| <span data-ttu-id="55e6d-162">Pajamų kodas</span><span class="sxs-lookup"><span data-stu-id="55e6d-162">Earnings code</span></span>    | <span data-ttu-id="55e6d-163">Premija</span><span class="sxs-lookup"><span data-stu-id="55e6d-163">Bonus</span></span>    |
| <span data-ttu-id="55e6d-164">Kiekis</span><span class="sxs-lookup"><span data-stu-id="55e6d-164">Quantity</span></span>         | <span data-ttu-id="55e6d-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="55e6d-165">1.0000</span></span>   |
| <span data-ttu-id="55e6d-166">Tarifas</span><span class="sxs-lookup"><span data-stu-id="55e6d-166">Rate</span></span>             | <span data-ttu-id="55e6d-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="55e6d-167">4250.00</span></span>  |
| <span data-ttu-id="55e6d-168">Skirtukas Eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="55e6d-168">Line details tab</span></span> |          |
| <span data-ttu-id="55e6d-169">Neautomatinis</span><span class="sxs-lookup"><span data-stu-id="55e6d-169">Manual</span></span>           | <span data-ttu-id="55e6d-170">(pažymėta)</span><span class="sxs-lookup"><span data-stu-id="55e6d-170">(marked)</span></span> |

<span data-ttu-id="55e6d-171">3 eilutė: skirtukas **Pajamų išrašo eilutė**</span><span class="sxs-lookup"><span data-stu-id="55e6d-171">Line 3: **Earning statement line** tab</span></span>

| <span data-ttu-id="55e6d-172">Laukas</span><span class="sxs-lookup"><span data-stu-id="55e6d-172">Field</span></span>           | <span data-ttu-id="55e6d-173">Vertė</span><span class="sxs-lookup"><span data-stu-id="55e6d-173">Value</span></span>      |
|-----------------|------------|
| <span data-ttu-id="55e6d-174">Pajamų kodas</span><span class="sxs-lookup"><span data-stu-id="55e6d-174">Earnings code</span></span>   | <span data-ttu-id="55e6d-175">Komisiniai</span><span class="sxs-lookup"><span data-stu-id="55e6d-175">Commission</span></span> |
| <span data-ttu-id="55e6d-176">Kiekis</span><span class="sxs-lookup"><span data-stu-id="55e6d-176">Quantity</span></span>        | <span data-ttu-id="55e6d-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="55e6d-177">1.0000</span></span>     |
| <span data-ttu-id="55e6d-178">Tarifas</span><span class="sxs-lookup"><span data-stu-id="55e6d-178">Rate</span></span>            | <span data-ttu-id="55e6d-179">!,299,00</span><span class="sxs-lookup"><span data-stu-id="55e6d-179">!,299.00</span></span>   |
| <span data-ttu-id="55e6d-180">Tarifas</span><span class="sxs-lookup"><span data-stu-id="55e6d-180">Rate</span></span>            | <span data-ttu-id="55e6d-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="55e6d-181">1,299.00</span></span>   |
| <span data-ttu-id="55e6d-182">Skirtukas Eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="55e6d-182">Line detail tab</span></span> |            |
| <span data-ttu-id="55e6d-183">Neautomatinis</span><span class="sxs-lookup"><span data-stu-id="55e6d-183">Manual</span></span>          | <span data-ttu-id="55e6d-184">(Pažymėta)</span><span class="sxs-lookup"><span data-stu-id="55e6d-184">(Marked)</span></span>   |

> [!NOTE]
> <span data-ttu-id="55e6d-185">Norint įvesti kiekvieno darbininko algalapio pradžios balansus, labai svarbu kiekvienos pajamų išrašo eilutės skirtuko **Eilutės informacija** slankiklį **Neautomatiškai** nustatyti į parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="55e6d-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="55e6d-186">Srityje **Veiksmas** spustelėkite **Išleisti pajamų išrašą** JAV – FED – ER – FICA.</span><span class="sxs-lookup"><span data-stu-id="55e6d-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>

4. <span data-ttu-id="55e6d-187">Srityje **Veiksmas** spustelėkite **Mokėjimo išrašas**, kad atidarytumėte puslapį **Generuoti mokėjimo išrašus** ir nustatykite, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="55e6d-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

| <span data-ttu-id="55e6d-188">Laukas</span><span class="sxs-lookup"><span data-stu-id="55e6d-188">Field</span></span>              | <span data-ttu-id="55e6d-189">Vertė</span><span class="sxs-lookup"><span data-stu-id="55e6d-189">Value</span></span>     |
|--------------------|-----------|
| <span data-ttu-id="55e6d-190">Mokėjimo data</span><span class="sxs-lookup"><span data-stu-id="55e6d-190">Payment date</span></span>       | <span data-ttu-id="55e6d-191">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="55e6d-191">6/30/2017</span></span> |
| <span data-ttu-id="55e6d-192">Mokėjimo vykdymo tipas</span><span class="sxs-lookup"><span data-stu-id="55e6d-192">Payment run type</span></span>   | <span data-ttu-id="55e6d-193">Neautomatinis</span><span class="sxs-lookup"><span data-stu-id="55e6d-193">Manual</span></span>    |
| <span data-ttu-id="55e6d-194">Išjungti apskaitą</span><span class="sxs-lookup"><span data-stu-id="55e6d-194">Disable accounting</span></span> |   <span data-ttu-id="55e6d-195">Taip</span><span class="sxs-lookup"><span data-stu-id="55e6d-195">Yes</span></span>     |

> [!NOTE] 
> <span data-ttu-id="55e6d-196">Tai galima padaryti, tik kai nustatytas vykdymo tipas yra Rankiniu būdu ir kai vartotojas nori išjungti mokėjimo vykdymo apskaitą.</span><span class="sxs-lookup"><span data-stu-id="55e6d-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

<span data-ttu-id="55e6d-197">Spustelėkite **Gerai** ir uždarykite **sistemos pranešimą**.</span><span class="sxs-lookup"><span data-stu-id="55e6d-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="55e6d-198">Kodėl generuojant mokėjimo išrašus slankiklis turi būti nustatytas į parinktį Taip?</span><span class="sxs-lookup"><span data-stu-id="55e6d-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>
<span data-ttu-id="55e6d-199">Slankiklį nustačius į parinktį **Taip**, mokėjimo išrašo eilutės nėra paskirstomos didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="55e6d-199">Setting the slider to **Yes** prevents lines in the pay statement from being districuted to General ledger.</span></span> <span data-ttu-id="55e6d-200">DK sumos atnaujintos anksčiau, kai buvo įvesti sąskaitos balansai iš senesnės versijos sistemos.</span><span class="sxs-lookup"><span data-stu-id="55e6d-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="55e6d-201">Įvedus algalapio pradžios balansus galima generuoti ataskaitas, apimančias informaciją iš ankstesnių metų, taip pat ataskaitas išmokų ir mokesčių riboms nustatyti.</span><span class="sxs-lookup"><span data-stu-id="55e6d-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>   

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="55e6d-202">C.</span><span class="sxs-lookup"><span data-stu-id="55e6d-202">C.</span></span> <span data-ttu-id="55e6d-203">Darbuotojų mokėjimo išrašų kūrimas</span><span class="sxs-lookup"><span data-stu-id="55e6d-203">Create pay statements for employees</span></span>
<span data-ttu-id="55e6d-204">Sugeneravę mokėjimo išrašus, turinčius pradžios balansus, turite patikrinti, kad mokėjimo išrašuose tiksliai atsispindėtų algalapio duomenys.</span><span class="sxs-lookup"><span data-stu-id="55e6d-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="55e6d-205">Taip pat turite rankiniu būdu atnaujinti išmokų ir mokesčių informaciją, kad sutaptų su ankstesnės algalapio sistemos reikšmėmis.</span><span class="sxs-lookup"><span data-stu-id="55e6d-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="55e6d-206">Patikrinę, ar sumos iš ankstesnio algalapio sistemos sutampa su dabartinio mokėjimo išrašo sumomis, turite užbaigti mokėjimo išrašus.</span><span class="sxs-lookup"><span data-stu-id="55e6d-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="55e6d-207">Atidarykite puslapį **Visi mokėjimo išrašai**.</span><span class="sxs-lookup"><span data-stu-id="55e6d-207">Open the **All pay statements** page.</span></span>

2. <span data-ttu-id="55e6d-208">Pažymėkite paskutinį sugeneruotą Michael Redmond mokėjimo išrašą</span><span class="sxs-lookup"><span data-stu-id="55e6d-208">Highlight the last generated pay statement for Michael Redmond</span></span>

3. <span data-ttu-id="55e6d-209">Spustelėkite **Redaguoti**, kad atidarytumėte puslapį **Mokėjimo išrašas**.</span><span class="sxs-lookup"><span data-stu-id="55e6d-209">Click **Edit** to open the **Pay statement** page.</span></span>

4. <span data-ttu-id="55e6d-210">Atidarykite skirtuką **Išmokų atskaitymai** ir įveskite toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="55e6d-210">Open the **Benefit deductions** tab and enter the following:</span></span>

| <span data-ttu-id="55e6d-211">Laukas</span><span class="sxs-lookup"><span data-stu-id="55e6d-211">Field</span></span>                           | <span data-ttu-id="55e6d-212">Vertė</span><span class="sxs-lookup"><span data-stu-id="55e6d-212">Value</span></span>            |
|---------------------------------|------------------|
| <span data-ttu-id="55e6d-213">Išmoka</span><span class="sxs-lookup"><span data-stu-id="55e6d-213">Benefit</span></span>                         | <span data-ttu-id="55e6d-214">Atskaitoma suma</span><span class="sxs-lookup"><span data-stu-id="55e6d-214">Deduction amount</span></span> |
| <span data-ttu-id="55e6d-215">401 000</span><span class="sxs-lookup"><span data-stu-id="55e6d-215">401K</span></span> | <span data-ttu-id="55e6d-216">Dalyvauja</span><span class="sxs-lookup"><span data-stu-id="55e6d-216">Participate</span></span>              | <span data-ttu-id="55e6d-217">3000.00</span><span class="sxs-lookup"><span data-stu-id="55e6d-217">3000.00</span></span>          |
| <span data-ttu-id="55e6d-218">Dantų gydymas</span><span class="sxs-lookup"><span data-stu-id="55e6d-218">Dental</span></span> | <span data-ttu-id="55e6d-219">SubSp</span><span class="sxs-lookup"><span data-stu-id="55e6d-219">SubSp</span></span>                  | <span data-ttu-id="55e6d-220">495,00</span><span class="sxs-lookup"><span data-stu-id="55e6d-220">495.00</span></span>           |
| <span data-ttu-id="55e6d-221">Išlaidos priklausomojo sveikatos priežiūrai</span><span class="sxs-lookup"><span data-stu-id="55e6d-221">Dep care spending</span></span> | <span data-ttu-id="55e6d-222">Dalyvauja</span><span class="sxs-lookup"><span data-stu-id="55e6d-222">Participate</span></span> | <span data-ttu-id="55e6d-223">2500.00</span><span class="sxs-lookup"><span data-stu-id="55e6d-223">2500.00</span></span>          |
| <span data-ttu-id="55e6d-224">Regėjimas</span><span class="sxs-lookup"><span data-stu-id="55e6d-224">Vision</span></span> | <span data-ttu-id="55e6d-225">SupSp</span><span class="sxs-lookup"><span data-stu-id="55e6d-225">SupSp</span></span>                  | <span data-ttu-id="55e6d-226">500,00</span><span class="sxs-lookup"><span data-stu-id="55e6d-226">500.00</span></span>           |

5. <span data-ttu-id="55e6d-227">Skirtuke **Išmokų įmokos** įveskite toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="55e6d-227">In the **Benefit contributions** tab and enter the following:</span></span>

| <span data-ttu-id="55e6d-228">Laukas</span><span class="sxs-lookup"><span data-stu-id="55e6d-228">Field</span></span>              | <span data-ttu-id="55e6d-229">Vertė</span><span class="sxs-lookup"><span data-stu-id="55e6d-229">Value</span></span>               |
|--------------------|---------------------|
| <span data-ttu-id="55e6d-230">Išmoka</span><span class="sxs-lookup"><span data-stu-id="55e6d-230">Benefit</span></span>            | <span data-ttu-id="55e6d-231">Įnašo suma</span><span class="sxs-lookup"><span data-stu-id="55e6d-231">Contribution amount</span></span> |
| <span data-ttu-id="55e6d-232">401 000</span><span class="sxs-lookup"><span data-stu-id="55e6d-232">401K</span></span> | <span data-ttu-id="55e6d-233">Dalyvauja</span><span class="sxs-lookup"><span data-stu-id="55e6d-233">Participate</span></span> | <span data-ttu-id="55e6d-234">3000,00</span><span class="sxs-lookup"><span data-stu-id="55e6d-234">3000,00</span></span>             |
| <span data-ttu-id="55e6d-235">Dantų gydymas</span><span class="sxs-lookup"><span data-stu-id="55e6d-235">Dental</span></span> | <span data-ttu-id="55e6d-236">SubSp</span><span class="sxs-lookup"><span data-stu-id="55e6d-236">SubSp</span></span>     | <span data-ttu-id="55e6d-237">495,00</span><span class="sxs-lookup"><span data-stu-id="55e6d-237">495.00</span></span>              |
| <span data-ttu-id="55e6d-238">Regėjimas</span><span class="sxs-lookup"><span data-stu-id="55e6d-238">Vision</span></span> | <span data-ttu-id="55e6d-239">SubSp</span><span class="sxs-lookup"><span data-stu-id="55e6d-239">SubSp</span></span>     | <span data-ttu-id="55e6d-240">500,00</span><span class="sxs-lookup"><span data-stu-id="55e6d-240">500.00</span></span>              |

6. <span data-ttu-id="55e6d-241">Skirtuke **Mokesčių atskaitymai** įveskite toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="55e6d-241">In the **Tax deductions** tab, enter the following:</span></span>

| <span data-ttu-id="55e6d-242">Laukas</span><span class="sxs-lookup"><span data-stu-id="55e6d-242">Field</span></span>           | <span data-ttu-id="55e6d-243">Vertė</span><span class="sxs-lookup"><span data-stu-id="55e6d-243">Value</span></span>            |
|-----------------|------------------|
| <span data-ttu-id="55e6d-244">Mokesčio kodas</span><span class="sxs-lookup"><span data-stu-id="55e6d-244">Tax code</span></span>        | <span data-ttu-id="55e6d-245">Atskaitoma suma</span><span class="sxs-lookup"><span data-stu-id="55e6d-245">Deduction amount</span></span> |
| <span data-ttu-id="55e6d-246">JAV – FED – ER – FICA</span><span class="sxs-lookup"><span data-stu-id="55e6d-246">USA-FED-ER-FICA</span></span> | <span data-ttu-id="55e6d-247">1600.00</span><span class="sxs-lookup"><span data-stu-id="55e6d-247">1600.00</span></span>          |
| <span data-ttu-id="55e6d-248">JAV – FED – ER – MEDI</span><span class="sxs-lookup"><span data-stu-id="55e6d-248">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="55e6d-249">825.75</span><span class="sxs-lookup"><span data-stu-id="55e6d-249">825.75</span></span>           |

7. <span data-ttu-id="55e6d-250">Skirtuke **Mokesčių įmokos** įveskite toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="55e6d-250">In the **Tax contributions** tab enter the following:</span></span>

8. <span data-ttu-id="55e6d-251">Spustelėkite **Skaičiuoti**.</span><span class="sxs-lookup"><span data-stu-id="55e6d-251">Click **Calculate**.</span></span>
> [!IMPORTANT] 
> <span data-ttu-id="55e6d-252">Patikrinkite bendrąsias mokėjimo išrašo sumas, kad jos atitiktų darbininko sumas nuo metų pradžios iki dabartinės datos iš senesnės versijos sistemos.</span><span class="sxs-lookup"><span data-stu-id="55e6d-252">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="55e6d-253">Galbūt prieš pereidami prie kito veiksmo norėsite stabtelėti ir atlikti bendrą visų mokėjimo išrašų patikrinimą.</span><span class="sxs-lookup"><span data-stu-id="55e6d-253">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="55e6d-254">Patikrinę, peržiūrėkite visus mokėjimo išrašus ir juos užbaikite.</span><span class="sxs-lookup"><span data-stu-id="55e6d-254">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="55e6d-255">Tą patį procesą prireikus galima atlikti ketvirčio pokyčių atžvilgiu visiems ankstesniems kiekvienų metų ketvirčiams.</span><span class="sxs-lookup"><span data-stu-id="55e6d-255">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="55e6d-256">Šito reikia tik tada, jei klientui reikia peržiūrėti duomenis pagal ketvirtį negrįžtant prie ankstesnės versijos sistemos.</span><span class="sxs-lookup"><span data-stu-id="55e6d-256">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="55e6d-257">Jei suklysite įvesdami pradžios balansus darbuotojui</span><span class="sxs-lookup"><span data-stu-id="55e6d-257">If you make a mistake Entering Beginning Balances for an Employee</span></span>
<span data-ttu-id="55e6d-258">Galima atšaukti ir iš naujo įvesti operacijas.</span><span class="sxs-lookup"><span data-stu-id="55e6d-258">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="55e6d-259">Norėdami atšaukti operaciją, turite atlikti toliau nurodytus veiksmus puslapyje **Visi mokėjimo išrašai**.</span><span class="sxs-lookup"><span data-stu-id="55e6d-259">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="55e6d-260">Spustelėkite **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="55e6d-260">Click **Reverse**.</span></span>

2. <span data-ttu-id="55e6d-261">Spustelėkite **Taip**, kai rodomas šis pranešimas: „Atšaukus šį mokėjimo išrašą, norint jį patikslinti, bus sukurtas atšaukimo mokėjimo išrašas</span><span class="sxs-lookup"><span data-stu-id="55e6d-261">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="55e6d-262">Nei vieno iš šių mokėjimo išrašų redaguoti negalima.</span><span class="sxs-lookup"><span data-stu-id="55e6d-262">Neither pay statement can be edited.</span></span> <span data-ttu-id="55e6d-263">Ar norite atšaukti šį mokėjimo išrašą?“</span><span class="sxs-lookup"><span data-stu-id="55e6d-263">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="55e6d-264">rodomas.</span><span class="sxs-lookup"><span data-stu-id="55e6d-264">displays.</span></span> 

<span data-ttu-id="55e6d-265">Atšaukus mokėjimo išrašą galima generuoti naują darbuotojo mokėjimo išrašą iš anksčiau sukurto pajamų išrašo.</span><span class="sxs-lookup"><span data-stu-id="55e6d-265">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="55e6d-266">Prieš generuojant naują mokėjimo išrašą būtinai ištaisyti neteisingas pajamų išrašo eilutes, o tada generuoti naują mokėjimo išrašą su teisingomis sumomis.</span><span class="sxs-lookup"><span data-stu-id="55e6d-266">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 
