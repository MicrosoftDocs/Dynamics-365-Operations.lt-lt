---
title: Algalapio integravimo tarp „Talent“ ir „Dayforce“ konfigūravimas
description: Šioje temoje paaiškinama, kaip sukonfigūruoti integravimą tarp „Microsoft Dynamics 365 for Talent“ ir „Ceridian Dayforce“, kad galėtumėte apdoroti mokėjimo vykdymą.
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9a88bf61dbb12520b555ceb7363b1c646d95386e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518608"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="7683c-103">Algalapių integravimo tarp „Talent“ ir „Dayforce“ konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="7683c-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7683c-104">Integravimas tarp „Microsoft Dynamics 365 for Talent“ ir „Ceridian Dayforce“ paremtas keliais konfigūravimo veiksmais, aprašytais šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="7683c-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="7683c-105">Prieš mokėjimo vykdymo apdorojimą turite sukonfigūruoti integravimą tiek „Talent“, tiek „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="7683c-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="7683c-106">Kai naudojate paslaugas, pvz., „Dayforce“ kad atliktumėte mokėjimų vykdymus, turite įjungti integravimą į „Talent“.</span><span class="sxs-lookup"><span data-stu-id="7683c-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="7683c-107">Integravimui reikalingi konkretūs duomenys iš „Talent“.</span><span class="sxs-lookup"><span data-stu-id="7683c-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="7683c-108">Todėl turite patvirtinti, kad duomenys, susieti su „Dayforce“, yra sukonfigūruojami „Talent“ taip, kad integravimas būtų palaikomas.</span><span class="sxs-lookup"><span data-stu-id="7683c-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="7683c-109">Integravimui naudojamos šios plačios duomenų kategorijos:</span><span class="sxs-lookup"><span data-stu-id="7683c-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="7683c-110">Personalo duomenys</span><span class="sxs-lookup"><span data-stu-id="7683c-110">Human resources data</span></span>
- <span data-ttu-id="7683c-111">Kompensacijos duomenys</span><span class="sxs-lookup"><span data-stu-id="7683c-111">Compensation data</span></span>
- <span data-ttu-id="7683c-112">Algalapio duomenys, pvz., mokėjimo ciklai, mokėjimo laikotarpiai ir pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="7683c-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="7683c-113">Darbininko duomenys</span><span class="sxs-lookup"><span data-stu-id="7683c-113">Worker data</span></span>

<span data-ttu-id="7683c-114">Šioje temoje aprašomi veiksmai, kuriuos reikia vykdyti norint įjungti integravimą.</span><span class="sxs-lookup"><span data-stu-id="7683c-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="7683c-115">Joje taip pat paaiškinami duomenų tipai ir išsami konfigūravimo informacija, reikalinga integravimui.</span><span class="sxs-lookup"><span data-stu-id="7683c-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="7683c-116">Integravimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="7683c-116">Enable the integration</span></span>

<span data-ttu-id="7683c-117">Pirmiausia „Talent“ turite įjungti integravimą ir įvesti konfigūravimo informaciją, kad prisijungtumėte prie „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="7683c-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="7683c-118">Jei norite, kad sukuriama didžiosios knygos operacija būtų importuota į „Microsoft Dynamics 365 for Finance and Operations“, taip pat turite sukurti „Microsoft Azure“ saugyklos paskyrą ir įvesti „Azure Storage“ jungimosi eilutę į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="7683c-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="7683c-119">Norėdami įjungti integravimą į „Talent“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7683c-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="7683c-120">Puslapyje **Sistemos administravimas** pasirinkite **Integravimo konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="7683c-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="7683c-121">Įveskite saugų failų perdavimo protokolo (FTP) galinį punktą ir saugų FTP aplanko kelią.</span><span class="sxs-lookup"><span data-stu-id="7683c-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="7683c-122">Įveskite vardą ir slaptažodį to vartotojo, kuris turės prieigą prie saugaus FTP galinio punkto ir aplanko kelio.</span><span class="sxs-lookup"><span data-stu-id="7683c-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="7683c-123">Tinkamai išbandykite ryšį ir nustatykite parinktį **Įjungti algalapių integravimą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7683c-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="7683c-124">Kai integravimas įjungiamas, sukuriamas duomenų eksportavimo paketas bei failai ir nustatomas dažnumas.</span><span class="sxs-lookup"><span data-stu-id="7683c-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="7683c-125">Galite pakeisti šį dažnumą pagal poreikį.</span><span class="sxs-lookup"><span data-stu-id="7683c-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="7683c-126">Daugiau informacijos apie „Azure“ saugyklos paskyras ir „Azure Storage“ jungimosi eilutes rasite šiose „Azure“ temose:</span><span class="sxs-lookup"><span data-stu-id="7683c-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="7683c-127">Apie „Azure“ saugyklos paskyras</span><span class="sxs-lookup"><span data-stu-id="7683c-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="7683c-128">„Azure Storage“ jungimosi eilučių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="7683c-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="7683c-129">Jūsų duomenų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="7683c-129">Configure your data</span></span> 

<span data-ttu-id="7683c-130">Kad apdorotumėte algalapį, turite sukonfigūruoti personalo duomenis „Talent“.</span><span class="sxs-lookup"><span data-stu-id="7683c-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="7683c-131">Turite nustatyti organizacijos duomenis, pvz., užduotis ir pareigas, taip pat išmokų ir kompensacijos informaciją.</span><span class="sxs-lookup"><span data-stu-id="7683c-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="7683c-132">Čia pateikiama įdarbinimo, mokėjimų ir atskaitymų informacija, būtina tam, kad būtų galima sugeneruoti darbuotojo mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="7683c-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="7683c-133">Personalo duomenys</span><span class="sxs-lookup"><span data-stu-id="7683c-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="7683c-134">Išmokos</span><span class="sxs-lookup"><span data-stu-id="7683c-134">Benefits</span></span> 

<span data-ttu-id="7683c-135">Personalas pateikia įrankius, kuriuos galima naudoti norint nustatyti ir tvarkyti organizacijos darbuotojams siūlomas arba apdorojamas išmokas, atskaitymus ir darbininkų kompensacijų planus.</span><span class="sxs-lookup"><span data-stu-id="7683c-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="7683c-136">Kurdami išmokas turėkite omenyje, kad toliau pateikiami duomenys ir konfigūracijos naudojami „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="7683c-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="7683c-137">Išmokų planai</span><span class="sxs-lookup"><span data-stu-id="7683c-137">Benefit plans</span></span>

- <span data-ttu-id="7683c-138">Planas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-138">Plan (required)</span></span>
- <span data-ttu-id="7683c-139">Tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-139">Type (required)</span></span>
- <span data-ttu-id="7683c-140">Poveikis algalapiui (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-140">Payroll impact (required)</span></span>
- <span data-ttu-id="7683c-141">Susigrąžinti skolas</span><span class="sxs-lookup"><span data-stu-id="7683c-141">Recover arrears</span></span>
- <span data-ttu-id="7683c-142">Atskaitymo metodas</span><span class="sxs-lookup"><span data-stu-id="7683c-142">Deduction method</span></span>
- <span data-ttu-id="7683c-143">Atskaitymo pirmumas</span><span class="sxs-lookup"><span data-stu-id="7683c-143">Deduction priority</span></span>
- <span data-ttu-id="7683c-144">Apribojimo laikotarpis</span><span class="sxs-lookup"><span data-stu-id="7683c-144">Limit period</span></span>
- <span data-ttu-id="7683c-145">Limito suma</span><span class="sxs-lookup"><span data-stu-id="7683c-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="7683c-146">Išmokos</span><span class="sxs-lookup"><span data-stu-id="7683c-146">Benefits</span></span>

- <span data-ttu-id="7683c-147">Planas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-147">Plan (required)</span></span>
- <span data-ttu-id="7683c-148">Tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-148">Type (required)</span></span>
- <span data-ttu-id="7683c-149">Parinktis (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-149">Option (required)</span></span>
- <span data-ttu-id="7683c-150">Išmokos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-150">Benefit ID (required)</span></span>
- <span data-ttu-id="7683c-151">Dažnumas</span><span class="sxs-lookup"><span data-stu-id="7683c-151">Frequency</span></span>
- <span data-ttu-id="7683c-152">Pagrindas</span><span class="sxs-lookup"><span data-stu-id="7683c-152">Basis</span></span>
- <span data-ttu-id="7683c-153">Suma arba tarifas</span><span class="sxs-lookup"><span data-stu-id="7683c-153">Amount or rate</span></span>
- <span data-ttu-id="7683c-154">Pajamų kodas</span><span class="sxs-lookup"><span data-stu-id="7683c-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="7683c-155">Palaikomi dažnumai</span><span class="sxs-lookup"><span data-stu-id="7683c-155">Supported frequencies</span></span> 

- <span data-ttu-id="7683c-156">Savaitinis</span><span class="sxs-lookup"><span data-stu-id="7683c-156">Weekly</span></span>
- <span data-ttu-id="7683c-157">Už dvi savaites</span><span class="sxs-lookup"><span data-stu-id="7683c-157">Bi-weekly</span></span>
- <span data-ttu-id="7683c-158">Kas pusę mėnesio</span><span class="sxs-lookup"><span data-stu-id="7683c-158">Semi-monthly</span></span>
- <span data-ttu-id="7683c-159">Mėnesinis</span><span class="sxs-lookup"><span data-stu-id="7683c-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="7683c-160">Palaikomos bazės</span><span class="sxs-lookup"><span data-stu-id="7683c-160">Supported bases</span></span> 

- <span data-ttu-id="7683c-161">Fiksuota suma</span><span class="sxs-lookup"><span data-stu-id="7683c-161">Fixed amount</span></span>
- <span data-ttu-id="7683c-162">Pajamų procentinė dalis</span><span class="sxs-lookup"><span data-stu-id="7683c-162">Percent of earnings</span></span>
- <span data-ttu-id="7683c-163">Produktyvios valandos</span><span class="sxs-lookup"><span data-stu-id="7683c-163">Productive hours</span></span>

<span data-ttu-id="7683c-164">„Dayforce“ sukuria šiuos atskaitymus pagal poveikį atlyginimui, šis poveikis apibrėžiamas išmokų plane.</span><span class="sxs-lookup"><span data-stu-id="7683c-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="7683c-165">Pasirinkimas „Talent“</span><span class="sxs-lookup"><span data-stu-id="7683c-165">Selection in Talent</span></span>        | <span data-ttu-id="7683c-166">Rezultatas „Dayforce“</span><span class="sxs-lookup"><span data-stu-id="7683c-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="7683c-167">None</span><span class="sxs-lookup"><span data-stu-id="7683c-167">None</span></span>                       | <span data-ttu-id="7683c-168">Nesukuriama jokio atskaitymo.</span><span class="sxs-lookup"><span data-stu-id="7683c-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="7683c-169">Tik atskaitymas</span><span class="sxs-lookup"><span data-stu-id="7683c-169">Deduction only</span></span>             | <span data-ttu-id="7683c-170">Sukuriamas darbuotojo atskaitymas.</span><span class="sxs-lookup"><span data-stu-id="7683c-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="7683c-171">Tik įnašas</span><span class="sxs-lookup"><span data-stu-id="7683c-171">Contribution only</span></span>          | <span data-ttu-id="7683c-172">Sukuriamas darbdavio atskaitymas.</span><span class="sxs-lookup"><span data-stu-id="7683c-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="7683c-173">Atskaitymas ir įnašas</span><span class="sxs-lookup"><span data-stu-id="7683c-173">Deduction and contribution</span></span> | <span data-ttu-id="7683c-174">Sukuriami darbuotojo ir darbdavio atskaitymai.</span><span class="sxs-lookup"><span data-stu-id="7683c-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="7683c-175">Daugiau informacijos apie tai, kaip nustatyti ir tvarkyti išlaidų programą, rasite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="7683c-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="7683c-176">Pristatyti darbuotojų išmokų programą</span><span class="sxs-lookup"><span data-stu-id="7683c-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="7683c-177">Kurti naują išmoką</span><span class="sxs-lookup"><span data-stu-id="7683c-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="7683c-178">Apibrėžti išmokų tinkamumo taisykles ir strategijas</span><span class="sxs-lookup"><span data-stu-id="7683c-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="7683c-179">Užregistruoti ir pašalinti išmokas darbuotojams</span><span class="sxs-lookup"><span data-stu-id="7683c-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="7683c-180">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="7683c-180">Compensation</span></span> 

<span data-ttu-id="7683c-181">Kompensacijų valdymas naudojamas kontroliuoti pagrindinio užmokesčio ir premijų pristatymui.</span><span class="sxs-lookup"><span data-stu-id="7683c-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="7683c-182">Darbuotojo fiksuotas pagrindinis užmokestis ir nuopelnų padidėjimai kontroliuojami naudojant pastoviosios kompensacijos dalies planus.</span><span class="sxs-lookup"><span data-stu-id="7683c-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="7683c-183">Skatinamųjų išmokų, pvz., priedų, apdovanojimų už našumą, akcijų pasirinkimo sandorių, subsidijų bei vienkartinių premijų mokėjimas valdomas naudojant kintamosios kompensacijos dalies planus.</span><span class="sxs-lookup"><span data-stu-id="7683c-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="7683c-184">„Dayforce“ naudojama kompensacijos informacija, kad būtų apskaičiuotas darbuotojo valandinis ar metinis tarifas.</span><span class="sxs-lookup"><span data-stu-id="7683c-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="7683c-185">Būtini pastoviosios atlyginimo dalies planai ir užmokesčio tarifo konvertavimas.</span><span class="sxs-lookup"><span data-stu-id="7683c-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="7683c-186">Darbuotojai turi būti susieti su pastoviosios atlyginimo dalies planu.</span><span class="sxs-lookup"><span data-stu-id="7683c-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="7683c-187">Daugiau informacijos apie kompensacijų planus rasite šios temose:</span><span class="sxs-lookup"><span data-stu-id="7683c-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="7683c-188">Pastoviosios atlyginimo dalies planų kūrimas</span><span class="sxs-lookup"><span data-stu-id="7683c-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="7683c-189">Kintamosios atlyginimo dalies planų kūrimas</span><span class="sxs-lookup"><span data-stu-id="7683c-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="7683c-190">Kurti atlyginimų / kompensavimo struktūrą ir planus</span><span class="sxs-lookup"><span data-stu-id="7683c-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="7683c-191">Kompensavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="7683c-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="7683c-192">Kompensavimo proceso nustatymas ir rezultatų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="7683c-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="7683c-193">Darbuotojo įtraukimas į fiksuoto atlyginimo dalies planą</span><span class="sxs-lookup"><span data-stu-id="7683c-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="7683c-194">Darbuotojo įtraukimas į kintamosios atlyginimo dalies planą</span><span class="sxs-lookup"><span data-stu-id="7683c-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="7683c-195">Darbai</span><span class="sxs-lookup"><span data-stu-id="7683c-195">Jobs</span></span> 

<span data-ttu-id="7683c-196">Užduotis yra užduočių ir pareigų, kurias asmeniui reikia įvykdyti, rinkinys.</span><span class="sxs-lookup"><span data-stu-id="7683c-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="7683c-197">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="7683c-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="7683c-198">Užduoties komponentų nustatymas</span><span class="sxs-lookup"><span data-stu-id="7683c-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="7683c-199">Apibrėžti naujas užduotis</span><span class="sxs-lookup"><span data-stu-id="7683c-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="7683c-200">Pareigybės</span><span class="sxs-lookup"><span data-stu-id="7683c-200">Positions</span></span>

<span data-ttu-id="7683c-201">Pareigos yra atskiros užduoties egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="7683c-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="7683c-202">Pavyzdžiui, pareigos „Pardavimo vadybininkas (rytų regionas)“ yra vienos iš pareigų, susietų su užduotimi „Pardavimo vadovas“.</span><span class="sxs-lookup"><span data-stu-id="7683c-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="7683c-203">Pareigos egzistuoja padalinyje.</span><span class="sxs-lookup"><span data-stu-id="7683c-203">A position exists in a department.</span></span> <span data-ttu-id="7683c-204">Su kiekvienomis pareigomis galima susieti tik vieną darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="7683c-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="7683c-205">Nustatydami pareigas, atkreipkite dėmesį į šiuos duomenis ir konfigūravimą:</span><span class="sxs-lookup"><span data-stu-id="7683c-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="7683c-206">Pareigos (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-206">Position (required)</span></span>
- <span data-ttu-id="7683c-207">Aprašas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-207">Description (required)</span></span>
- <span data-ttu-id="7683c-208">Užduotis (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-208">Job (required)</span></span>
- <span data-ttu-id="7683c-209">Padalinys (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-209">Department (required)</span></span>
- <span data-ttu-id="7683c-210">Pareigų tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-210">Position type (required)</span></span>
- <span data-ttu-id="7683c-211">Viso etato ekvivalentas</span><span class="sxs-lookup"><span data-stu-id="7683c-211">Full-time equivalent</span></span>
- <span data-ttu-id="7683c-212">Įprastos darbo valandos per metus (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="7683c-213">Apmokama juridinio subjekto (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="7683c-214">Mokėjimo ciklas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-214">Pay cycle (required)</span></span>
- <span data-ttu-id="7683c-215">Numatytosios finansinės dimensijos – išlaidų centras (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="7683c-216">Darbininko priskyrimas – darbininkas, priskyrimo pradžia, priskyrimo pabaiga, priežasties kodas</span><span class="sxs-lookup"><span data-stu-id="7683c-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="7683c-217">Jei tame pačiame padalinyje su tuo pačiu darbu susiejamos kelios pareigos, „Dayforce“ jos yra konsoliduojamos į vienas pareigas.</span><span class="sxs-lookup"><span data-stu-id="7683c-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="7683c-218">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="7683c-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="7683c-219">Darbo jėgos organizavimas naudojant padalinius, darbo vietas ir pareigas</span><span class="sxs-lookup"><span data-stu-id="7683c-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="7683c-220">Pareigų nustatymas</span><span class="sxs-lookup"><span data-stu-id="7683c-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="7683c-221">Padaliniai</span><span class="sxs-lookup"><span data-stu-id="7683c-221">Departments</span></span>

<span data-ttu-id="7683c-222">Padalinys yra valdymo vienetas, nurodantis organizacijos kategoriją arba funkcinę sritį.</span><span class="sxs-lookup"><span data-stu-id="7683c-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="7683c-223">Padalinys yra atsakingas už tam tikrą organizacijos sritį, pvz., pardavimą, apskaitą arba personalą.</span><span class="sxs-lookup"><span data-stu-id="7683c-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="7683c-224">Padalinius galite naudoti norėdami pranešti apie funkcines sritis.</span><span class="sxs-lookup"><span data-stu-id="7683c-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="7683c-225">Padaliniai gali turėti pelno ir nuostolio atsakomybę.</span><span class="sxs-lookup"><span data-stu-id="7683c-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="7683c-226">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="7683c-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="7683c-227">Padalinio kūrimas ir priskyrimas padalinių hierarchijai</span><span class="sxs-lookup"><span data-stu-id="7683c-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="7683c-228">Apibrėžti naujus padalinius</span><span class="sxs-lookup"><span data-stu-id="7683c-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="7683c-229">Mokėjimo ciklai ir mokėjimo laikotarpiai</span><span class="sxs-lookup"><span data-stu-id="7683c-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="7683c-230">Mokėjimo ciklas lemia algalapio pateikimo dažnumą ir konkrečias dienas, kuriomis sumokama darbininkams.</span><span class="sxs-lookup"><span data-stu-id="7683c-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="7683c-231">Pavyzdžiui, mokėjimo ciklas gali būti mėnesinis ir darbuotojams gali būti sumokėta paskutinę mėnesio dieną.</span><span class="sxs-lookup"><span data-stu-id="7683c-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="7683c-232">Mokėjimo ciklas taip pat gali būti savaitinis, o darbuotojams gali būti sumokama kitą antradienį po mokėjimo laikotarpio pabaigos.</span><span class="sxs-lookup"><span data-stu-id="7683c-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="7683c-233">Mokėjimo ciklai priskiriami pareigoms tam, kad būtų galima valdyti, kada sumokama tas pareigas einantiems darbininkams.</span><span class="sxs-lookup"><span data-stu-id="7683c-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="7683c-234">Sukūrę mokėjimo ciklus, galite generuoti kiekvieno ciklo mokėjimo laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="7683c-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="7683c-235">Į kiekvieną mokėjimo laikotarpį įeina numatytoji mokėjimo data, paremta jūsų pateikta informacija.</span><span class="sxs-lookup"><span data-stu-id="7683c-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="7683c-236">Tačiau galite pakeisti numatytąją mokėjimo datą mokėjimo laikotarpyje, kad leistumėte išimtis, pvz., tuo atveju, jei mokėjimo data sutampa su švente.</span><span class="sxs-lookup"><span data-stu-id="7683c-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="7683c-237">„Dayforce“ naudojama ši informacija:</span><span class="sxs-lookup"><span data-stu-id="7683c-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="7683c-238">Mokėjimo ciklas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-238">Pay cycle (required)</span></span>
- <span data-ttu-id="7683c-239">Mokėjimo ciklo dažnumas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="7683c-240">Laikotarpio pradžios data (būtina pirmajam mokėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="7683c-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="7683c-241">Numatytoji mokėjimo data (būtina pirmajam mokėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="7683c-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="7683c-242">Ši informacija yra integruota į „Dayforce“ kaip mokėjimo grupės ir skiriasi priklausomai nuo šalies ar regiono kiekvienam mokėjimo ciklui.</span><span class="sxs-lookup"><span data-stu-id="7683c-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="7683c-243">Prieš integravimą reikia sugeneruoti bent vieną mokėjimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="7683c-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="7683c-244">„Dayforce“ sugeneruoja mokėjimo grupių kalendorius ir mokėjimo datas pagal pirmojo laikotarpio pradžios datą ir numatytojo mokėjimo datą, nustatytą „Talent“.</span><span class="sxs-lookup"><span data-stu-id="7683c-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="7683c-245">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="7683c-245">Earning codes</span></span>

<span data-ttu-id="7683c-246">Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas.</span><span class="sxs-lookup"><span data-stu-id="7683c-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="7683c-247">Kodams būdingi įvairūs parametrai, susiję su pajamomis, pvz., apskaitos taisyklės, mokesčių įstatymai, ataskaitų kūrimo reikalavimai ir bendrųjų sumų pajėgumas.</span><span class="sxs-lookup"><span data-stu-id="7683c-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="7683c-248">„Dayforce“ naudojama ši informacija:</span><span class="sxs-lookup"><span data-stu-id="7683c-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="7683c-249">Pajamų kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-249">Earning Code (required)</span></span>
- <span data-ttu-id="7683c-250">aprašymas</span><span class="sxs-lookup"><span data-stu-id="7683c-250">Description</span></span>
- <span data-ttu-id="7683c-251">Matavimo vienetas</span><span class="sxs-lookup"><span data-stu-id="7683c-251">Unit of measure</span></span>
- <span data-ttu-id="7683c-252">Produktyvus</span><span class="sxs-lookup"><span data-stu-id="7683c-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="7683c-253">Darbininko duomenys</span><span class="sxs-lookup"><span data-stu-id="7683c-253">Worker data</span></span>

<span data-ttu-id="7683c-254">Įrašai apie jūsų turimus darbininkų tipus yra svarbūs jūsų personalo ir algalapių sistemoms.</span><span class="sxs-lookup"><span data-stu-id="7683c-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="7683c-255">Informacija, kurią įvedate, gali būti naudojama darbininkų ir asmeninei informacijai sekti.</span><span class="sxs-lookup"><span data-stu-id="7683c-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="7683c-256">Galite tvarkyti šią darbininkų informaciją:</span><span class="sxs-lookup"><span data-stu-id="7683c-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="7683c-257">**Pagrindinė** – tvarkykite pagrindinę darbininko informaciją, pvz., kontaktinę informaciją, demografinę informaciją, identifikacijos informaciją, šeimos informaciją, santykį su karine tarnyba, informaciją apie gyvenimą ne tėvynėje ir asmeninius kontaktus bei kontaktinius asmenis nelaimės atveju.</span><span class="sxs-lookup"><span data-stu-id="7683c-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="7683c-258">**Įdarbinimas** – tvarkykite informaciją apie darbininko įdarbinimą, pvz., priklausymą įmonei ar organizacijai, priskyrimą pareigoms, pradžios ir pabaigos datas, tinkamumą dirbti, darbo režimą, pensiją, atostogas ir informaciją apie perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="7683c-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="7683c-259">**Atostogos ir nebuvimas** – tvarkykite informaciją apie darbininko nebuvimą, pvz., darbo kalendorius, nebuvimo operacijas ir nebuvimo nustatymą.</span><span class="sxs-lookup"><span data-stu-id="7683c-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="7683c-260">**Kompensacija ir algalapis** – tvarkykite informaciją apie darbininko kompensacijos planus ir algalapio informaciją, pvz., plano registraciją, apdovanojimus, našumą, komisinius, mokesčių informaciją, išėjimą į pensiją ir atskaitymus iš atlyginimų.</span><span class="sxs-lookup"><span data-stu-id="7683c-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="7683c-261">Įvesdami darbininko informaciją turėkite omenyje, kad toliau pateikiami duomenys ir konfigūracijos naudojami „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="7683c-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="7683c-262">Bendroji informacija</span><span class="sxs-lookup"><span data-stu-id="7683c-262">General information</span></span>

- <span data-ttu-id="7683c-263">Darbuotojo numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-263">Personnel number (required)</span></span>
- <span data-ttu-id="7683c-264">Vardas (būtinas)</span><span class="sxs-lookup"><span data-stu-id="7683c-264">First name (required)</span></span>
- <span data-ttu-id="7683c-265">Pavardė (būtinai)</span><span class="sxs-lookup"><span data-stu-id="7683c-265">Last name (required)</span></span>
- <span data-ttu-id="7683c-266">Antras vardas</span><span class="sxs-lookup"><span data-stu-id="7683c-266">Middle name</span></span>
- <span data-ttu-id="7683c-267">Paaukštinimo data</span><span class="sxs-lookup"><span data-stu-id="7683c-267">Seniority date</span></span>
- <span data-ttu-id="7683c-268">Žinoma kaip</span><span class="sxs-lookup"><span data-stu-id="7683c-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="7683c-269">Asmeninė informacija</span><span class="sxs-lookup"><span data-stu-id="7683c-269">Personal information</span></span>

- <span data-ttu-id="7683c-270">Šeiminė padėtis (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-270">Marital status (required)</span></span>
- <span data-ttu-id="7683c-271">Gimimo data (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-271">Birth date (required)</span></span>
- <span data-ttu-id="7683c-272">Lytis (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-272">Gender (required)</span></span>
- <span data-ttu-id="7683c-273">Asmuo su negalia</span><span class="sxs-lookup"><span data-stu-id="7683c-273">Person with disabilities</span></span>
- <span data-ttu-id="7683c-274">Pilietybės šalies regionas (tik Meksikai)</span><span class="sxs-lookup"><span data-stu-id="7683c-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="7683c-275">Adresas</span><span class="sxs-lookup"><span data-stu-id="7683c-275">Address information</span></span>

- <span data-ttu-id="7683c-276">Pagrindinis (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-276">Primary (required)</span></span>
- <span data-ttu-id="7683c-277">Šalis / regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-277">Country/region (required)</span></span>
- <span data-ttu-id="7683c-278">Pašto kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-278">Postal code (required)</span></span>
- <span data-ttu-id="7683c-279">Gatvės numeris (būtina) (tik Meksikai)</span><span class="sxs-lookup"><span data-stu-id="7683c-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="7683c-280">Pastatų kompleksas (tik Meksikai)</span><span class="sxs-lookup"><span data-stu-id="7683c-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="7683c-281">Miestas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-281">City (required)</span></span>
- <span data-ttu-id="7683c-282">Valstija (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-282">State (required)</span></span>
- <span data-ttu-id="7683c-283">Apygarda (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="7683c-284">Kontaktinė informacija</span><span class="sxs-lookup"><span data-stu-id="7683c-284">Contact information</span></span> 

- <span data-ttu-id="7683c-285">Pirminis (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-285">Primary (required)</span></span>
- <span data-ttu-id="7683c-286">Kontakto numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-286">Contact number (required)</span></span>
- <span data-ttu-id="7683c-287">Išplėtimas</span><span class="sxs-lookup"><span data-stu-id="7683c-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="7683c-288">Algalapio informacija ir pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="7683c-288">Payroll information and earning codes</span></span>

<span data-ttu-id="7683c-289">Darbuotojams gali būti priskirtos tam tikros pajamos, išmokamos tam tikru dažnumu, darbuotojai gali turėti pageidaujamą mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="7683c-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="7683c-290">Toliau pateikiami laukeliai naudojami „Dayforce“, kad būtų užtikrinta, jog naudojamos tos parinktys ir nustatymai.</span><span class="sxs-lookup"><span data-stu-id="7683c-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="7683c-291">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="7683c-291">Earning codes</span></span>

- <span data-ttu-id="7683c-292">Pareigos (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-292">Position (required)</span></span>
- <span data-ttu-id="7683c-293">Pajamų kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-293">Earning Code (required)</span></span>
- <span data-ttu-id="7683c-294">Dažnumas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-294">Frequency (required)</span></span>
- <span data-ttu-id="7683c-295">Suma (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="7683c-296">Algalapių informacija</span><span class="sxs-lookup"><span data-stu-id="7683c-296">Payroll information</span></span>

- <span data-ttu-id="7683c-297">Mokėjimo būdas</span><span class="sxs-lookup"><span data-stu-id="7683c-297">Payment Method</span></span>
- <span data-ttu-id="7683c-298">Ekonominė sritis (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-298">Economic Region (required)</span></span>
- <span data-ttu-id="7683c-299">Darbuotojų išmokų ID</span><span class="sxs-lookup"><span data-stu-id="7683c-299">Employee Benefits ID</span></span>
- <span data-ttu-id="7683c-300">Asmens kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-300">National ID Number (required)</span></span>
- <span data-ttu-id="7683c-301">Karo tarnybos numeris</span><span class="sxs-lookup"><span data-stu-id="7683c-301">Military Service Number</span></span>
- <span data-ttu-id="7683c-302">Pamainos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-302">Shift ID (required)</span></span>
- <span data-ttu-id="7683c-303">Mokesčių numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-303">Tax Number (required)</span></span>
- <span data-ttu-id="7683c-304">Sąjungos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-304">Union ID (required)</span></span>
- <span data-ttu-id="7683c-305">Darbo dienos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-305">Work Day ID (required)</span></span>
- <span data-ttu-id="7683c-306">Darbo leidimo numeris</span><span class="sxs-lookup"><span data-stu-id="7683c-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="7683c-307">Meksikoje palaikomi šie mokėjimo būdai – **Grynieji**, **Čekis** (įmonės fizinis čekis) ir **Elektroninis mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="7683c-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="7683c-308">Jei konkretus mokėjimo būdas nenurodytas, kaip numatytasis būdas naudojamas **Čekis**.</span><span class="sxs-lookup"><span data-stu-id="7683c-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="7683c-309">Įdarbinimo informacija</span><span class="sxs-lookup"><span data-stu-id="7683c-309">Employment details</span></span>

<span data-ttu-id="7683c-310">Detali įdarbinimo retrospektyva naudojama kaip pagrindinis informacijos šaltinis, kuriuo remiantis „Dayforce“ gaunamos darbuotojo samdos, atleidimo ir pakartotinės samdos būsenos.</span><span class="sxs-lookup"><span data-stu-id="7683c-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="7683c-311">„Dayforce“ palaiko tik vieną įdarbinimo įrašą vienu metu.</span><span class="sxs-lookup"><span data-stu-id="7683c-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="7683c-312">Įdarbinimo pradžios data (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-312">Employment start date (required)</span></span>
- <span data-ttu-id="7683c-313">Įdarbinimo pabaigos data</span><span class="sxs-lookup"><span data-stu-id="7683c-313">Employment end date</span></span>
- <span data-ttu-id="7683c-314">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="7683c-314">Start date</span></span>
- <span data-ttu-id="7683c-315">Patikslinta darbo pradžios data</span><span class="sxs-lookup"><span data-stu-id="7683c-315">Adjusted start date</span></span>
- <span data-ttu-id="7683c-316">Atleidimo data (būtina po atleidimo)</span><span class="sxs-lookup"><span data-stu-id="7683c-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="7683c-317">Atleidimo priežastis (būtina po atleidimo)</span><span class="sxs-lookup"><span data-stu-id="7683c-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="7683c-318">Darbuotojo pagrindinės datos gaunamos naudojant toliau pateikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="7683c-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="7683c-319">„Talent“</span><span class="sxs-lookup"><span data-stu-id="7683c-319">Talent</span></span>                | <span data-ttu-id="7683c-320">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="7683c-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7683c-321">Naujausia samdos data</span><span class="sxs-lookup"><span data-stu-id="7683c-321">Most recent hire date</span></span> | <span data-ttu-id="7683c-322">Dabartinio nenutraukto įdarbinimo retrospektyvos įrašo įdarbinimo pradžia</span><span class="sxs-lookup"><span data-stu-id="7683c-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="7683c-323">Atleidimo data</span><span class="sxs-lookup"><span data-stu-id="7683c-323">Termination date</span></span>      | <span data-ttu-id="7683c-324">Dabartinio nenutraukto įdarbinimo retrospektyvos įrašo atleidimo data</span><span class="sxs-lookup"><span data-stu-id="7683c-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="7683c-325">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="7683c-325">Start date</span></span>            | <span data-ttu-id="7683c-326">Dabartinio neaktyvios įdarbinimo retrospektyvos įrašo koreguota pradžios data, pradžios data ar įdarbinimo pradžia</span><span class="sxs-lookup"><span data-stu-id="7683c-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="7683c-327">Pradinio įdarbinimo data</span><span class="sxs-lookup"><span data-stu-id="7683c-327">Original hire date</span></span>    | <span data-ttu-id="7683c-328">Anksčiausio įdarbinimo retrospektyvos įrašo įdarbinimo pradžia</span><span class="sxs-lookup"><span data-stu-id="7683c-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="7683c-329">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="7683c-329">Compensation</span></span>

<span data-ttu-id="7683c-330">Pastoviosios atlyginimo dalies planas turi būti susietas su kiekvieno darbuotojo pagrindinėmis pareigomis įdarbinimo laikotarpio metu.</span><span class="sxs-lookup"><span data-stu-id="7683c-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="7683c-331">Šis laikotarpis prasideda nuo tos datos, kai darbuotojas pasamdomas (ar įdarbinimo pradžios datos), ir tęsiasi iki atleidimo.</span><span class="sxs-lookup"><span data-stu-id="7683c-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="7683c-332">Įsigaliojimo data (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-332">Effective Date (required)</span></span>
- <span data-ttu-id="7683c-333">Galiojimo pabaigos data</span><span class="sxs-lookup"><span data-stu-id="7683c-333">Expiration date</span></span>
- <span data-ttu-id="7683c-334">Užmokesčio tarifas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-334">Pay Rate (required)</span></span>
- <span data-ttu-id="7683c-335">Užmokesčio tarifo konvertavimas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="7683c-336">Metinis atitikmuo (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="7683c-337">Valandinis atitikmuo (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="7683c-338">Jei pagal valandas apmokamas darbuotojas eina kelias pareigas, pagrindinių pareigų pastovioji atlyginimo dalis importuojama į „Dayforce“ kaip darbuotojo lygmens bazinis tarifas / alga.</span><span class="sxs-lookup"><span data-stu-id="7683c-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="7683c-339">Nepagrindinių pareigų valandinis tarifas išsaugomas atitinkamose pareigose „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="7683c-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="7683c-340">Jei etatinis darbuotojas eina kelias pareigas, iš visų aktyvių pareigų išvedamas suvestinis valandinis tarifas bei metinė alga ir jie naudojami kaip darbuotojo lygmens bazinis tarifas / alga.</span><span class="sxs-lookup"><span data-stu-id="7683c-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="7683c-341">Identifikavimo numeriai</span><span class="sxs-lookup"><span data-stu-id="7683c-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="7683c-342">Socialinio draudimo identifikatorius</span><span class="sxs-lookup"><span data-stu-id="7683c-342">Social Security identifier</span></span> 

<span data-ttu-id="7683c-343">Kiekvienas darbuotojas turi turėti vieną pirminį identifikatorių.</span><span class="sxs-lookup"><span data-stu-id="7683c-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="7683c-344">Šis identifikatorius turi būti **SSN** identifikacijos tipo.</span><span class="sxs-lookup"><span data-stu-id="7683c-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="7683c-345">„Dayforce“ jis automatiškai išvedamas kaip darbuotojo socialinio draudimo identifikatorius, kuris yra būtinas samdai.</span><span class="sxs-lookup"><span data-stu-id="7683c-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="7683c-346">Pirminis (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-346">Primary (required)</span></span>
- <span data-ttu-id="7683c-347">Identifikacijos tipas = "SSN"</span><span class="sxs-lookup"><span data-stu-id="7683c-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="7683c-348">Išdavimo data</span><span class="sxs-lookup"><span data-stu-id="7683c-348">Issued Date</span></span>
- <span data-ttu-id="7683c-349">Galiojimo data</span><span class="sxs-lookup"><span data-stu-id="7683c-349">Expiration Date</span></span>

<span data-ttu-id="7683c-350">Darbuotojai gali deklaruoti kelis **SSN** identifikacijos tipo identifikacijos numerius.</span><span class="sxs-lookup"><span data-stu-id="7683c-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="7683c-351">Tačiau tik įrašas, pažymėtas kaip **Pirminis**, yra integruojamas į „Dayforce“, nepriklausomai nuo to, ar numeris yra aktyvus ar negaliojantis.</span><span class="sxs-lookup"><span data-stu-id="7683c-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="7683c-352">Banko sąskaitos ir išmokos</span><span class="sxs-lookup"><span data-stu-id="7683c-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="7683c-353">Jei darbuotojas pasirinko, kad pinigai jam būtų pervesti pavedimu į jo banko sąskaitą, būtina įvesti galiojančią banko sąskaitos informaciją.</span><span class="sxs-lookup"><span data-stu-id="7683c-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="7683c-354">„Talent“</span><span class="sxs-lookup"><span data-stu-id="7683c-354">Talent</span></span>                         | <span data-ttu-id="7683c-355">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="7683c-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7683c-356">Banko sąskaitos numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="7683c-357">SWIFT kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-357">SWIFT code (required)</span></span>          | <span data-ttu-id="7683c-358">**Banko ID** laukelis naudojamas, apdorojant algalapį Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="7683c-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="7683c-359">Filialo numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="7683c-360">Banko sąskaitos tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-360">Bank account type (required)</span></span>   | <span data-ttu-id="7683c-361">**Sąskaitos tipo** laukelis naudojamas apdorojant algalapį Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="7683c-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="7683c-362">Į palaikomas vertes įeina **Tikrinimas** ir **Algalapis**.</span><span class="sxs-lookup"><span data-stu-id="7683c-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="7683c-363">Darbuotojai, pasirinkę apmokėjimą pavedimu į banko sąskaitą, turi pateikti nuorodą į likučio sąskaitą, esančią juridiniame subjekte, kurio pirminis adresas yra Meksikoje ir kuris yra susietas su galiojančia banko sąskaita Meksikos banke.</span><span class="sxs-lookup"><span data-stu-id="7683c-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="7683c-364">Visos kitos nelikutinės sąskaitos yra ignoruojamos.</span><span class="sxs-lookup"><span data-stu-id="7683c-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="7683c-365">Adresas</span><span class="sxs-lookup"><span data-stu-id="7683c-365">Address information</span></span>

<span data-ttu-id="7683c-366">Kiekvienas darbuotojas turi turėti vieną pirminę vietą.</span><span class="sxs-lookup"><span data-stu-id="7683c-366">Every employee must have one primary location.</span></span> <span data-ttu-id="7683c-367">„Dayforce“ ši vieta naudojama darbuotojo pagrindinei gyvenamajai vietai nustatyti mokesčių tikslais.</span><span class="sxs-lookup"><span data-stu-id="7683c-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="7683c-368">Pirminis (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-368">Primary (required)</span></span>
- <span data-ttu-id="7683c-369">Šalis / regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-369">Country/region (required)</span></span>
- <span data-ttu-id="7683c-370">Pašto kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="7683c-371">Gatvė (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-371">Street (required)</span></span>
- <span data-ttu-id="7683c-372">Gatvės numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-372">Street Number (required)</span></span>
- <span data-ttu-id="7683c-373">Pastatų kompleksas</span><span class="sxs-lookup"><span data-stu-id="7683c-373">Building Complement</span></span>
- <span data-ttu-id="7683c-374">Miestas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-374">City (required)</span></span>
- <span data-ttu-id="7683c-375">Valstija (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-375">State (required)</span></span>
- <span data-ttu-id="7683c-376">Apygarda (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="7683c-377">Duomenų konfigūravimas norint generuoti algalapius JAV ir Kanadoje</span><span class="sxs-lookup"><span data-stu-id="7683c-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="7683c-378">Jei generuojate užmokesčius darbuotojams JAV ir Kanadoje, reikia sukonfigūruoti šiuos elementus:</span><span class="sxs-lookup"><span data-stu-id="7683c-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="7683c-379">Su pareigomis būtina nurodyti padalinius.</span><span class="sxs-lookup"><span data-stu-id="7683c-379">Departments are required on positions.</span></span>
- <span data-ttu-id="7683c-380">Išlaidų centrai turi būti nustatyti kaip finansinės dimensijos ir būti pirmas elementas numatytoje finansinės dimensijos eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7683c-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="7683c-381">Galite sukonfigūruoti „Talent“, kad prie pareigų būtų nurodytas padalinys.</span><span class="sxs-lookup"><span data-stu-id="7683c-381">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="7683c-382">Norėdami tai atlikti, eikite į **Bendrinamos personalo pareigos > Pareigos > Prie pareigų reikalauti padalinių**.</span><span class="sxs-lookup"><span data-stu-id="7683c-382">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="7683c-383">Rekomenduojame integruojant šį parametrą taikyti.</span><span class="sxs-lookup"><span data-stu-id="7683c-383">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="7683c-384">Pareigų rūšys</span><span class="sxs-lookup"><span data-stu-id="7683c-384">Job types</span></span>

<span data-ttu-id="7683c-385">Užduočių tipai naudojami sugrupuoti panašioms užduotims į kategorijas.</span><span class="sxs-lookup"><span data-stu-id="7683c-385">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="7683c-386">Užduočių tipai būtini tam, kad algalapiai būtų apdoroti JAV ir Kanadoje.</span><span class="sxs-lookup"><span data-stu-id="7683c-386">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="7683c-387">Kai kurie užduočių tipų pavyzdžiai: visa darbo diena ar ne visa darbo diena arba atlyginimas ir valandinis užmokestis.</span><span class="sxs-lookup"><span data-stu-id="7683c-387">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="7683c-388">Užduočių tipai yra susieti su „Dayforce“ kaip mokėjimo tipai, nurodantys, ar darbuotojas gauna valandinį ar fiksuotą užmokestį.</span><span class="sxs-lookup"><span data-stu-id="7683c-388">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="7683c-389">Šie užduočių tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="7683c-389">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="7683c-390">Darbo vietos tipas</span><span class="sxs-lookup"><span data-stu-id="7683c-390">Job type</span></span>   | <span data-ttu-id="7683c-391">aprašymas</span><span class="sxs-lookup"><span data-stu-id="7683c-391">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="7683c-392">Valandinis</span><span class="sxs-lookup"><span data-stu-id="7683c-392">Hourly</span></span>     | <span data-ttu-id="7683c-393">Valandinis</span><span class="sxs-lookup"><span data-stu-id="7683c-393">Hourly</span></span>      |
| <span data-ttu-id="7683c-394">Fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="7683c-394">Salaried</span></span>   | <span data-ttu-id="7683c-395">Fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="7683c-395">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="7683c-396">Pareigų tipai</span><span class="sxs-lookup"><span data-stu-id="7683c-396">Position types</span></span> 

<span data-ttu-id="7683c-397">Pareigų tipus naudojate tam, kad apibrėžtumėte, ar pareigoms skirta visa darbo diena, ne visa darbo diena ar kad esama dar kito varianto.</span><span class="sxs-lookup"><span data-stu-id="7683c-397">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="7683c-398">Pareigų tipai yra susieti su „Dayforce“ kaip mokėjimo klasės, nurodančios, ar darbuotojas dirba visą ar ne visą darbo dieną.</span><span class="sxs-lookup"><span data-stu-id="7683c-398">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="7683c-399">Šie pareigų tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="7683c-399">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="7683c-400">Pareigų tipas</span><span class="sxs-lookup"><span data-stu-id="7683c-400">Position type</span></span>   | <span data-ttu-id="7683c-401">aprašymas</span><span class="sxs-lookup"><span data-stu-id="7683c-401">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="7683c-402">Visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="7683c-402">Full-time</span></span>       | <span data-ttu-id="7683c-403">Darbuotojas, dirbantis visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="7683c-403">Full time employee</span></span> |
| <span data-ttu-id="7683c-404">Ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="7683c-404">Part-time</span></span>       | <span data-ttu-id="7683c-405">Darbuotojas, dirbantis ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="7683c-405">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="7683c-406">Priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="7683c-406">Reason codes</span></span>

<span data-ttu-id="7683c-407">Priežasčių kodai pateikia informaciją apie darbuotojo būseną.</span><span class="sxs-lookup"><span data-stu-id="7683c-407">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="7683c-408">Priežasčių kodai yra susieti su „Dayforce“ kaip būsenos priežastys, nurodančios darbuotojo pareigų ar įdarbinimo būsenos pokyčių priežastį.</span><span class="sxs-lookup"><span data-stu-id="7683c-408">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="7683c-409">Šie priežasčių kodai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="7683c-409">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="7683c-410">Tikslinės paskirties šifras</span><span class="sxs-lookup"><span data-stu-id="7683c-410">Reason code</span></span>    | <span data-ttu-id="7683c-411">aprašymas</span><span class="sxs-lookup"><span data-stu-id="7683c-411">Description</span></span>      | <span data-ttu-id="7683c-412">Taikomi scenarijai</span><span class="sxs-lookup"><span data-stu-id="7683c-412">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="7683c-413">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="7683c-413">RESIGNATION</span></span>    | <span data-ttu-id="7683c-414">Atsistatydinimas</span><span class="sxs-lookup"><span data-stu-id="7683c-414">Resignation</span></span>      | <span data-ttu-id="7683c-415">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="7683c-415">Terminate worker</span></span>     |
| <span data-ttu-id="7683c-416">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="7683c-416">TERMINATION</span></span>    | <span data-ttu-id="7683c-417">Atleidimas</span><span class="sxs-lookup"><span data-stu-id="7683c-417">Termination</span></span>      | <span data-ttu-id="7683c-418">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="7683c-418">Terminate worker</span></span>     |
| <span data-ttu-id="7683c-419">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="7683c-419">RETIREMENT</span></span>     | <span data-ttu-id="7683c-420">Išėjimas į pensiją</span><span class="sxs-lookup"><span data-stu-id="7683c-420">Retirement</span></span>       | <span data-ttu-id="7683c-421">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="7683c-421">Terminate worker</span></span>     |
| <span data-ttu-id="7683c-422">KITA</span><span class="sxs-lookup"><span data-stu-id="7683c-422">OTHER</span></span>          | <span data-ttu-id="7683c-423">Kitos priežastys</span><span class="sxs-lookup"><span data-stu-id="7683c-423">Other Reasons</span></span>    | <span data-ttu-id="7683c-424">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="7683c-424">Terminate worker</span></span>     |
| <span data-ttu-id="7683c-425">DEATH</span><span class="sxs-lookup"><span data-stu-id="7683c-425">DEATH</span></span>          | <span data-ttu-id="7683c-426">Mirtis</span><span class="sxs-lookup"><span data-stu-id="7683c-426">Death</span></span>            | <span data-ttu-id="7683c-427">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="7683c-427">Terminate worker</span></span>     |
| <span data-ttu-id="7683c-428">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="7683c-428">LEAVEOFABSENCE</span></span> | <span data-ttu-id="7683c-429">Laisvadienis</span><span class="sxs-lookup"><span data-stu-id="7683c-429">Leave of Absence</span></span> | <span data-ttu-id="7683c-430">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="7683c-430">Terminate worker</span></span>     |
| <span data-ttu-id="7683c-431">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="7683c-431">CONTRACTEND</span></span>    | <span data-ttu-id="7683c-432">Sutarties pabaiga</span><span class="sxs-lookup"><span data-stu-id="7683c-432">End of Contract</span></span>  | <span data-ttu-id="7683c-433">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="7683c-433">Terminate worker</span></span>     |
| <span data-ttu-id="7683c-434">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="7683c-434">SALARYCHANGE</span></span>   | <span data-ttu-id="7683c-435">Atlyginimo pasikeitimas</span><span class="sxs-lookup"><span data-stu-id="7683c-435">Change of Salary</span></span> | <span data-ttu-id="7683c-436">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="7683c-436">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="7683c-437">Šeiminė padėtis</span><span class="sxs-lookup"><span data-stu-id="7683c-437">Marital status</span></span>

<span data-ttu-id="7683c-438">Šeiminės padėties vertės yra susietos su „Dayforce“ ir išverčiamos, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="7683c-438">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="7683c-439">Toliau pateikiamoje lentelėje parodoma, kaip šeiminės padėties vertės yra susietos su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="7683c-439">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="7683c-440">„Talent“</span><span class="sxs-lookup"><span data-stu-id="7683c-440">Talent</span></span>                 | <span data-ttu-id="7683c-441">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="7683c-441">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="7683c-442">Vedęs / ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="7683c-442">Married</span></span>                | <span data-ttu-id="7683c-443">Vedęs / ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="7683c-443">Married</span></span>              |
| <span data-ttu-id="7683c-444">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="7683c-444">Single</span></span>                 | <span data-ttu-id="7683c-445">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="7683c-445">Single</span></span>               |
| <span data-ttu-id="7683c-446">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="7683c-446">Widowed</span></span>                | <span data-ttu-id="7683c-447">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="7683c-447">Widowed</span></span>              |
| <span data-ttu-id="7683c-448">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="7683c-448">Divorced</span></span>               | <span data-ttu-id="7683c-449">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="7683c-449">Divorced</span></span>             |
| <span data-ttu-id="7683c-450">Registruota partnerystė</span><span class="sxs-lookup"><span data-stu-id="7683c-450">Registered Partnership</span></span> | <span data-ttu-id="7683c-451">Civilinė partnerystė</span><span class="sxs-lookup"><span data-stu-id="7683c-451">Domestic Partnership</span></span> |
| <span data-ttu-id="7683c-452">None</span><span class="sxs-lookup"><span data-stu-id="7683c-452">None</span></span>                   | <span data-ttu-id="7683c-453">None</span><span class="sxs-lookup"><span data-stu-id="7683c-453">None</span></span>                 |
| <span data-ttu-id="7683c-454">Sugyventiniai</span><span class="sxs-lookup"><span data-stu-id="7683c-454">Cohabiting</span></span>             | <span data-ttu-id="7683c-455">Sugyventiniai</span><span class="sxs-lookup"><span data-stu-id="7683c-455">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="7683c-456">Giminė</span><span class="sxs-lookup"><span data-stu-id="7683c-456">Gender</span></span>

<span data-ttu-id="7683c-457">Paskirtoji lytis yra susieta su „Dayforce“ ir išverčiama, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="7683c-457">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="7683c-458">Toliau pateikiamoje lentelėje parodoma, kaip paskirtoji lytis yra susieta su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="7683c-458">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="7683c-459">„Talent“</span><span class="sxs-lookup"><span data-stu-id="7683c-459">Talent</span></span>       | <span data-ttu-id="7683c-460">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="7683c-460">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="7683c-461">Vyras</span><span class="sxs-lookup"><span data-stu-id="7683c-461">Male</span></span>         | <span data-ttu-id="7683c-462">Vyras</span><span class="sxs-lookup"><span data-stu-id="7683c-462">Male</span></span>            |
| <span data-ttu-id="7683c-463">Moteris</span><span class="sxs-lookup"><span data-stu-id="7683c-463">Female</span></span>       | <span data-ttu-id="7683c-464">Moteris</span><span class="sxs-lookup"><span data-stu-id="7683c-464">Female</span></span>          |
| <span data-ttu-id="7683c-465">Konkrečiai nenurodyta</span><span class="sxs-lookup"><span data-stu-id="7683c-465">Non-specific</span></span> | <span data-ttu-id="7683c-466">*Nepalaikoma*</span><span class="sxs-lookup"><span data-stu-id="7683c-466">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="7683c-467">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="7683c-467">Earning codes</span></span>

<span data-ttu-id="7683c-468">Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas.</span><span class="sxs-lookup"><span data-stu-id="7683c-468">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="7683c-469">Kodai apibrėžia kelis parametrus, susijusius su pajamomis, pvz., apskaitos taisykles, mokesčių įstatymus, ataskaitų kūrimo reikalavimus ir bendrųjų sumų pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="7683c-469">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="7683c-470">Jei naudojamas nepalaikomas dažnumas, skaičiavimams naudojamas iš anksto numatytasis dažnumas **Kiekvienas mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="7683c-470">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="7683c-471">Palaikomi dažnumai</span><span class="sxs-lookup"><span data-stu-id="7683c-471">Supported frequencies</span></span>

- <span data-ttu-id="7683c-472">Visos</span><span class="sxs-lookup"><span data-stu-id="7683c-472">All</span></span>
- <span data-ttu-id="7683c-473">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="7683c-473">EVERYPAY</span></span>
- <span data-ttu-id="7683c-474">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="7683c-474">EACHPAYPERIOD</span></span>
- <span data-ttu-id="7683c-475">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="7683c-475">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="7683c-476">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="7683c-476">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="7683c-477">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-477">1OFMTH</span></span>
- <span data-ttu-id="7683c-478">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-478">LASTOFMTH</span></span>
- <span data-ttu-id="7683c-479">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-479">2OFMTH</span></span>
- <span data-ttu-id="7683c-480">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-480">3OFMTH</span></span>
- <span data-ttu-id="7683c-481">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-481">4OFMTH</span></span>
- <span data-ttu-id="7683c-482">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-482">5OFMTH</span></span>
- <span data-ttu-id="7683c-483">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-483">1N2OFMTH</span></span>
- <span data-ttu-id="7683c-484">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-484">3N4OFMTH</span></span>
- <span data-ttu-id="7683c-485">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-485">1N3OFMTH</span></span>
- <span data-ttu-id="7683c-486">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-486">1N4OFMTH</span></span>
- <span data-ttu-id="7683c-487">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-487">2N3OFMTH</span></span>
- <span data-ttu-id="7683c-488">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-488">2N4OFMTH</span></span>
- <span data-ttu-id="7683c-489">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-489">1N2N3OFMTH</span></span>
- <span data-ttu-id="7683c-490">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-490">1N2N4OFMTH</span></span>
- <span data-ttu-id="7683c-491">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-491">1N3N4OFMTH</span></span>
- <span data-ttu-id="7683c-492">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-492">2N3N4OFMTH</span></span>
- <span data-ttu-id="7683c-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="7683c-494">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="7683c-494">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="7683c-495">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="7683c-495">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="7683c-496">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="7683c-496">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="7683c-497">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="7683c-497">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="7683c-498">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="7683c-498">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="7683c-499">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="7683c-499">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="7683c-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="7683c-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="7683c-501">Adresai</span><span class="sxs-lookup"><span data-stu-id="7683c-501">Addresses</span></span>

<span data-ttu-id="7683c-502">Konkrečios šalies ar regiono, valstijos ir apygardos (savivaldybės) kodų identifikacijai reikalingi tam tikri formatai, kuriuos gali atpažinti „Dayforce“ ir šalyje / regione veikiantys teikėjai.</span><span class="sxs-lookup"><span data-stu-id="7683c-502">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="7683c-503">Nors miestų formatas yra kintamas, kiekvienas miestas turi būti susietas su valstija.</span><span class="sxs-lookup"><span data-stu-id="7683c-503">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="7683c-504">„Talent“</span><span class="sxs-lookup"><span data-stu-id="7683c-504">Talent</span></span>          | <span data-ttu-id="7683c-505">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="7683c-505">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="7683c-506">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="7683c-506">Country/Region</span></span>  | <span data-ttu-id="7683c-507">Šalies kodas</span><span class="sxs-lookup"><span data-stu-id="7683c-507">Country Code</span></span>          |
| <span data-ttu-id="7683c-508">Pašto kodas</span><span class="sxs-lookup"><span data-stu-id="7683c-508">Zip/Postal Code</span></span> | <span data-ttu-id="7683c-509">Pašto indeksas</span><span class="sxs-lookup"><span data-stu-id="7683c-509">Postal Code</span></span>           |
| <span data-ttu-id="7683c-510">Apskritis</span><span class="sxs-lookup"><span data-stu-id="7683c-510">State</span></span>           | <span data-ttu-id="7683c-511">Valstijos kodas</span><span class="sxs-lookup"><span data-stu-id="7683c-511">State Code</span></span>            |
| <span data-ttu-id="7683c-512">Miestas</span><span class="sxs-lookup"><span data-stu-id="7683c-512">City</span></span>            | <span data-ttu-id="7683c-513">Miestas</span><span class="sxs-lookup"><span data-stu-id="7683c-513">City</span></span>                  |
| <span data-ttu-id="7683c-514">Apygarda</span><span class="sxs-lookup"><span data-stu-id="7683c-514">County</span></span>          | <span data-ttu-id="7683c-515">Apygarda (savivaldybė)</span><span class="sxs-lookup"><span data-stu-id="7683c-515">County (Municipality)</span></span> |
| <span data-ttu-id="7683c-516">Gatvė</span><span class="sxs-lookup"><span data-stu-id="7683c-516">Street</span></span>          | <span data-ttu-id="7683c-517">1 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="7683c-517">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="7683c-518">Mokesčių regionai</span><span class="sxs-lookup"><span data-stu-id="7683c-518">Tax regions</span></span>

<span data-ttu-id="7683c-519">Mokesčių regionai naudojami apibrėžti tinkamam mokesčiui, kuris turėtų būti taikomas generuojant algalapį.</span><span class="sxs-lookup"><span data-stu-id="7683c-519">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="7683c-520">Mokesčių regionai yra susieti su „Dayforce“ vietų adresais.</span><span class="sxs-lookup"><span data-stu-id="7683c-520">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="7683c-521">Numatytasis mokesčių regionas turi būti susietas su darbininko aktyviomis pareigomis.</span><span class="sxs-lookup"><span data-stu-id="7683c-521">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="7683c-522">Mokesčių regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-522">Tax region (required)</span></span>
- <span data-ttu-id="7683c-523">Šalis / regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-523">Country/Region (required)</span></span>
- <span data-ttu-id="7683c-524">Valstija (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-524">State (required)</span></span>
- <span data-ttu-id="7683c-525">Apygarda</span><span class="sxs-lookup"><span data-stu-id="7683c-525">County</span></span> 
- <span data-ttu-id="7683c-526">Miestas (būtina)</span><span class="sxs-lookup"><span data-stu-id="7683c-526">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="7683c-527">Duomenų konfigūravimas sugeneruoti algalapiui Meksikoje</span><span class="sxs-lookup"><span data-stu-id="7683c-527">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="7683c-528">Jei generuojate mokėjimus darbuotojams Meksikoje, reikia sukonfigūruoti šiuos elementus:</span><span class="sxs-lookup"><span data-stu-id="7683c-528">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="7683c-529">Su pareigomis būtina nurodyti padalinius.</span><span class="sxs-lookup"><span data-stu-id="7683c-529">Departments are required on positions.</span></span>
- <span data-ttu-id="7683c-530">Išlaidų centrai turi būti nustatyti kaip finansinės dimensijos ir būti pirmas elementas numatytoje finansinės dimensijos eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7683c-530">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="7683c-531">Užduočių tipai</span><span class="sxs-lookup"><span data-stu-id="7683c-531">Job types</span></span>

<span data-ttu-id="7683c-532">Užduočių tipai naudojami sugrupuoti panašioms užduotims į kategorijas.</span><span class="sxs-lookup"><span data-stu-id="7683c-532">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="7683c-533">Užduočių tipai yra būtini, kad algalapis būtų apdorotas Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="7683c-533">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="7683c-534">Kai kurie užduočių tipų pavyzdžiai: visa darbo diena ar ne visa darbo diena arba atlyginimas ir valandinis užmokestis.</span><span class="sxs-lookup"><span data-stu-id="7683c-534">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="7683c-535">Užduočių tipai yra susieti su „Dayforce“ kaip mokėjimo tipai, nurodantys, ar darbuotojas gauna valandinį ar fiksuotą užmokestį.</span><span class="sxs-lookup"><span data-stu-id="7683c-535">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="7683c-536">Šie užduočių tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="7683c-536">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="7683c-537">Darbo vietos tipas</span><span class="sxs-lookup"><span data-stu-id="7683c-537">Job type</span></span>   | <span data-ttu-id="7683c-538">aprašymas</span><span class="sxs-lookup"><span data-stu-id="7683c-538">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="7683c-539">Valandinis</span><span class="sxs-lookup"><span data-stu-id="7683c-539">Hourly</span></span>     | <span data-ttu-id="7683c-540">MX valandinis</span><span class="sxs-lookup"><span data-stu-id="7683c-540">MX Hourly</span></span>   |
| <span data-ttu-id="7683c-541">Fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="7683c-541">Salaried</span></span>   | <span data-ttu-id="7683c-542">MX fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="7683c-542">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="7683c-543">Pareigų tipai</span><span class="sxs-lookup"><span data-stu-id="7683c-543">Position types</span></span> 

<span data-ttu-id="7683c-544">Pareigų tipus naudojate tam, kad apibrėžtumėte, ar pareigoms skirta visa darbo diena, ne visa darbo diena ar kad esama dar kito varianto.</span><span class="sxs-lookup"><span data-stu-id="7683c-544">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="7683c-545">Pareigų tipai yra susieti su „Dayforce“ kaip mokėjimo klasės, nurodančios, ar darbuotojas dirba visą ar ne visą darbo dieną.</span><span class="sxs-lookup"><span data-stu-id="7683c-545">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="7683c-546">Šie pareigų tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="7683c-546">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="7683c-547">Pareigų tipas</span><span class="sxs-lookup"><span data-stu-id="7683c-547">Position type</span></span>   | <span data-ttu-id="7683c-548">aprašymas</span><span class="sxs-lookup"><span data-stu-id="7683c-548">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="7683c-549">Visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="7683c-549">Full-time</span></span>       | <span data-ttu-id="7683c-550">Darbuotojas, dirbantis visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="7683c-550">Full time employee</span></span> |
| <span data-ttu-id="7683c-551">Ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="7683c-551">Part-time</span></span>       | <span data-ttu-id="7683c-552">Darbuotojas, dirbantis ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="7683c-552">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="7683c-553">Priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="7683c-553">Reason codes</span></span>

<span data-ttu-id="7683c-554">Priežasčių kodai pateikia informaciją apie darbuotojo būseną.</span><span class="sxs-lookup"><span data-stu-id="7683c-554">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="7683c-555">Priežasčių kodai yra susieti su „Dayforce“ kaip būsenos priežastys, nurodančios darbuotojo pareigų ar įdarbinimo būsenos pokyčių priežastį.</span><span class="sxs-lookup"><span data-stu-id="7683c-555">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="7683c-556">Šie priežasčių kodai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="7683c-556">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="7683c-557">Tikslinės paskirties šifras</span><span class="sxs-lookup"><span data-stu-id="7683c-557">Reason code</span></span>            | <span data-ttu-id="7683c-558">aprašymas</span><span class="sxs-lookup"><span data-stu-id="7683c-558">Description</span></span>                    | <span data-ttu-id="7683c-559">Taikomi scenarijai</span><span class="sxs-lookup"><span data-stu-id="7683c-559">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="7683c-560">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="7683c-560">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="7683c-561">Išvykimas prieš pirmą algalapį</span><span class="sxs-lookup"><span data-stu-id="7683c-561">Departure before first payroll</span></span> | <span data-ttu-id="7683c-562">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="7683c-562">Terminate worker</span></span>     |
| <span data-ttu-id="7683c-563">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="7683c-563">RESIGNATION</span></span>            | <span data-ttu-id="7683c-564">Atsistatydinimas</span><span class="sxs-lookup"><span data-stu-id="7683c-564">Resignation</span></span>                    | <span data-ttu-id="7683c-565">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="7683c-565">Terminate worker</span></span>     |
| <span data-ttu-id="7683c-566">PENSION</span><span class="sxs-lookup"><span data-stu-id="7683c-566">PENSION</span></span>                | <span data-ttu-id="7683c-567">Pensija</span><span class="sxs-lookup"><span data-stu-id="7683c-567">Pension</span></span>                        | <span data-ttu-id="7683c-568">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="7683c-568">Terminate worker</span></span>     |
| <span data-ttu-id="7683c-569">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="7683c-569">TERMINATION</span></span>            | <span data-ttu-id="7683c-570">Atleidimas</span><span class="sxs-lookup"><span data-stu-id="7683c-570">Termination</span></span>                    | <span data-ttu-id="7683c-571">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="7683c-571">Terminate worker</span></span>     |
| <span data-ttu-id="7683c-572">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="7683c-572">RETIREMENT</span></span>             | <span data-ttu-id="7683c-573">Išėjimas į pensiją</span><span class="sxs-lookup"><span data-stu-id="7683c-573">Retirement</span></span>                     | <span data-ttu-id="7683c-574">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="7683c-574">Terminate worker</span></span>     |
| <span data-ttu-id="7683c-575">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="7683c-575">ABSENTEE</span></span>               | <span data-ttu-id="7683c-576">Nesantysis</span><span class="sxs-lookup"><span data-stu-id="7683c-576">Absentee</span></span>                       | <span data-ttu-id="7683c-577">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="7683c-577">Terminate worker</span></span>     |
| <span data-ttu-id="7683c-578">KITA</span><span class="sxs-lookup"><span data-stu-id="7683c-578">OTHER</span></span>                  | <span data-ttu-id="7683c-579">Kitos priežastys</span><span class="sxs-lookup"><span data-stu-id="7683c-579">Other Reasons</span></span>                  | <span data-ttu-id="7683c-580">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="7683c-580">Terminate worker</span></span>     |
| <span data-ttu-id="7683c-581">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="7683c-581">CLOSURE</span></span>                | <span data-ttu-id="7683c-582">Įmonės uždarymas</span><span class="sxs-lookup"><span data-stu-id="7683c-582">Business Closure</span></span>               | <span data-ttu-id="7683c-583">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="7683c-583">Terminate worker</span></span>     |
| <span data-ttu-id="7683c-584">DEATH</span><span class="sxs-lookup"><span data-stu-id="7683c-584">DEATH</span></span>                  | <span data-ttu-id="7683c-585">Mirtis</span><span class="sxs-lookup"><span data-stu-id="7683c-585">Death</span></span>                          | <span data-ttu-id="7683c-586">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="7683c-586">Terminate worker</span></span>     |
| <span data-ttu-id="7683c-587">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="7683c-587">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="7683c-588">Laisvadienis</span><span class="sxs-lookup"><span data-stu-id="7683c-588">Leave of Absence</span></span>               | <span data-ttu-id="7683c-589">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="7683c-589">Terminate worker</span></span>     |
| <span data-ttu-id="7683c-590">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="7683c-590">CONTRACTEND</span></span>            | <span data-ttu-id="7683c-591">Sutarties pabaiga</span><span class="sxs-lookup"><span data-stu-id="7683c-591">End of Contract</span></span>                | <span data-ttu-id="7683c-592">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="7683c-592">Terminate worker</span></span>     |
| <span data-ttu-id="7683c-593">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="7683c-593">SALARYCHANGE</span></span>           | <span data-ttu-id="7683c-594">Atlyginimo keitimas</span><span class="sxs-lookup"><span data-stu-id="7683c-594">Change of Salary</span></span>               | <span data-ttu-id="7683c-595">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="7683c-595">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="7683c-596">Įdarbinimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="7683c-596">Terms of employment</span></span>

<span data-ttu-id="7683c-597">Įdarbinimo sąlygos naudojamos įdarbinimo sąlygų kategorijoms kurti.</span><span class="sxs-lookup"><span data-stu-id="7683c-597">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="7683c-598">Sąlygos yra susietos su „Dayforce“ kaip įdarbinimo indikatorių vertės.</span><span class="sxs-lookup"><span data-stu-id="7683c-598">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="7683c-599">Šios įdarbinimo sąlygos ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="7683c-599">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="7683c-600">Įdarbinimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="7683c-600">Terms of employment</span></span>   | <span data-ttu-id="7683c-601">aprašymas</span><span class="sxs-lookup"><span data-stu-id="7683c-601">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="7683c-602">Reguliarus</span><span class="sxs-lookup"><span data-stu-id="7683c-602">Regular</span></span>               | <span data-ttu-id="7683c-603">Reguliarus</span><span class="sxs-lookup"><span data-stu-id="7683c-603">Regular</span></span>     |
| <span data-ttu-id="7683c-604">Tiesioginis</span><span class="sxs-lookup"><span data-stu-id="7683c-604">Direct</span></span>                | <span data-ttu-id="7683c-605">Tiesioginis</span><span class="sxs-lookup"><span data-stu-id="7683c-605">Direct</span></span>      |
| <span data-ttu-id="7683c-606">Stažuotė</span><span class="sxs-lookup"><span data-stu-id="7683c-606">Internship</span></span>            | <span data-ttu-id="7683c-607">Stažuotė</span><span class="sxs-lookup"><span data-stu-id="7683c-607">Internship</span></span>  |
| <span data-ttu-id="7683c-608">Nuolatinis</span><span class="sxs-lookup"><span data-stu-id="7683c-608">Permanent</span></span>             | <span data-ttu-id="7683c-609">Nuolatinis</span><span class="sxs-lookup"><span data-stu-id="7683c-609">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="7683c-610">Šeiminė padėtis</span><span class="sxs-lookup"><span data-stu-id="7683c-610">Marital status</span></span>

<span data-ttu-id="7683c-611">Šeiminės padėties vertės yra susietos su „Dayforce“ ir išverčiamos, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="7683c-611">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="7683c-612">Toliau pateikiamoje lentelėje parodoma, kaip šeiminės padėties vertės yra susietos su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="7683c-612">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="7683c-613">„Talent“</span><span class="sxs-lookup"><span data-stu-id="7683c-613">Talent</span></span>                 | <span data-ttu-id="7683c-614">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="7683c-614">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="7683c-615">Vedęs / ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="7683c-615">Married</span></span>                | <span data-ttu-id="7683c-616">Vedęs / ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="7683c-616">Married</span></span>                   |
| <span data-ttu-id="7683c-617">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="7683c-617">Single</span></span>                 | <span data-ttu-id="7683c-618">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="7683c-618">Single</span></span>                    |
| <span data-ttu-id="7683c-619">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="7683c-619">Widowed</span></span>                | <span data-ttu-id="7683c-620">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="7683c-620">Widowed</span></span>                   |
| <span data-ttu-id="7683c-621">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="7683c-621">Divorced</span></span>               | <span data-ttu-id="7683c-622">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="7683c-622">Divorced</span></span>                  |
| <span data-ttu-id="7683c-623">Registruota partnerystė</span><span class="sxs-lookup"><span data-stu-id="7683c-623">Registered Partnership</span></span> | <span data-ttu-id="7683c-624">Civilinė partnerystė</span><span class="sxs-lookup"><span data-stu-id="7683c-624">Domestic Partnership</span></span>      |
| <span data-ttu-id="7683c-625">None</span><span class="sxs-lookup"><span data-stu-id="7683c-625">None</span></span>                   | <span data-ttu-id="7683c-626">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="7683c-626">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="7683c-627">Sugyventiniai</span><span class="sxs-lookup"><span data-stu-id="7683c-627">Cohabiting</span></span>             | <span data-ttu-id="7683c-628">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="7683c-628">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="7683c-629">Giminė</span><span class="sxs-lookup"><span data-stu-id="7683c-629">Gender</span></span>

<span data-ttu-id="7683c-630">Paskirtoji lytis yra susieta su „Dayforce“ ir išverčiama, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="7683c-630">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="7683c-631">Toliau pateikiamoje lentelėje parodoma, kaip paskirtoji lytis yra susieta su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="7683c-631">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="7683c-632">„Talent“</span><span class="sxs-lookup"><span data-stu-id="7683c-632">Talent</span></span>       | <span data-ttu-id="7683c-633">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="7683c-633">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="7683c-634">Vyras</span><span class="sxs-lookup"><span data-stu-id="7683c-634">Male</span></span>         | <span data-ttu-id="7683c-635">Vyras</span><span class="sxs-lookup"><span data-stu-id="7683c-635">Male</span></span>                      |
| <span data-ttu-id="7683c-636">Moteris</span><span class="sxs-lookup"><span data-stu-id="7683c-636">Female</span></span>       | <span data-ttu-id="7683c-637">Moteris</span><span class="sxs-lookup"><span data-stu-id="7683c-637">Female</span></span>                    |
| <span data-ttu-id="7683c-638">Konkrečiai nenurodyta</span><span class="sxs-lookup"><span data-stu-id="7683c-638">Non-specific</span></span> | <span data-ttu-id="7683c-639">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="7683c-639">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="7683c-640">Mokėjimo būdas</span><span class="sxs-lookup"><span data-stu-id="7683c-640">Payment method</span></span>

<span data-ttu-id="7683c-641">Mokėjimo būdai leidžia darbuotojui ir įmonei apibrėžti darbuotojų apmokėjimą.</span><span class="sxs-lookup"><span data-stu-id="7683c-641">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="7683c-642">Mokėjimo būdai yra susieti su „Dayforce“ ir išverčiami, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="7683c-642">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="7683c-643">Toliau pateikiamoje lentelėje parodoma, kaip mokėjimo būdai yra susieti su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="7683c-643">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="7683c-644">„Talent“</span><span class="sxs-lookup"><span data-stu-id="7683c-644">Talent</span></span>             | <span data-ttu-id="7683c-645">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="7683c-645">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="7683c-646">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="7683c-646">Cash</span></span>               | <span data-ttu-id="7683c-647">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="7683c-647">Cash</span></span>                      |
| <span data-ttu-id="7683c-648">Elektroninis mokėjimas</span><span class="sxs-lookup"><span data-stu-id="7683c-648">Electronic Payment</span></span> | <span data-ttu-id="7683c-649">Perkėlimas</span><span class="sxs-lookup"><span data-stu-id="7683c-649">Transfer</span></span>                  |
| <span data-ttu-id="7683c-650">Tikrinti</span><span class="sxs-lookup"><span data-stu-id="7683c-650">Check</span></span>              | <span data-ttu-id="7683c-651">Čekis</span><span class="sxs-lookup"><span data-stu-id="7683c-651">Cheque</span></span>                    |
| <span data-ttu-id="7683c-652">Banko čekis</span><span class="sxs-lookup"><span data-stu-id="7683c-652">Bank Draft</span></span>         | <span data-ttu-id="7683c-653">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="7683c-653">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="7683c-654">Kiti</span><span class="sxs-lookup"><span data-stu-id="7683c-654">Other</span></span>              | <span data-ttu-id="7683c-655">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="7683c-655">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="7683c-656">Banko sąskaitos tipas</span><span class="sxs-lookup"><span data-stu-id="7683c-656">Bank account type</span></span>

<span data-ttu-id="7683c-657">Banko sąskaitų tipai naudojami elektroniniams mokėjimams į darbuotojų sąskaitas vykdyti.</span><span class="sxs-lookup"><span data-stu-id="7683c-657">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="7683c-658">Banko sąskaitų tipai yra susieti su „Dayforce“ kaip pavedimų sąskaitos informacija.</span><span class="sxs-lookup"><span data-stu-id="7683c-658">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="7683c-659">Banko sąskaitų tipai yra išverčiami, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="7683c-659">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="7683c-660">„Talent“</span><span class="sxs-lookup"><span data-stu-id="7683c-660">Talent</span></span>            | <span data-ttu-id="7683c-661">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="7683c-661">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="7683c-662">Čekių sąskaita</span><span class="sxs-lookup"><span data-stu-id="7683c-662">Checking Account</span></span>  | <span data-ttu-id="7683c-663">Čekių sąskaita</span><span class="sxs-lookup"><span data-stu-id="7683c-663">CheckingAccount</span></span>           |
| <span data-ttu-id="7683c-664">Algalapių sąskaita</span><span class="sxs-lookup"><span data-stu-id="7683c-664">Payroll Account</span></span>   | <span data-ttu-id="7683c-665">Algalapių sąskaita</span><span class="sxs-lookup"><span data-stu-id="7683c-665">PayrollAccount</span></span>            |
| <span data-ttu-id="7683c-666">Taupomoji sąskaita</span><span class="sxs-lookup"><span data-stu-id="7683c-666">Savings Account</span></span>   | <span data-ttu-id="7683c-667">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="7683c-667">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="7683c-668">„BankGirot“ sąskaita</span><span class="sxs-lookup"><span data-stu-id="7683c-668">BankGirot account</span></span> | <span data-ttu-id="7683c-669">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="7683c-669">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="7683c-670">„PlusGirot“ sąskaita</span><span class="sxs-lookup"><span data-stu-id="7683c-670">PlusGirot account</span></span> | <span data-ttu-id="7683c-671">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="7683c-671">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="7683c-672">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="7683c-672">Earning codes</span></span>

<span data-ttu-id="7683c-673">Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas.</span><span class="sxs-lookup"><span data-stu-id="7683c-673">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="7683c-674">Kodai apibrėžia kelis parametrus, susijusius su pajamomis, pvz., apskaitos taisykles, mokesčių įstatymus, ataskaitų kūrimo reikalavimus ir bendrųjų sumų pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="7683c-674">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="7683c-675">Jei naudojamas nepalaikomas dažnumas, skaičiavimams naudojamas iš anksto numatytasis dažnumas **Kiekvienas mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="7683c-675">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="7683c-676">Palaikomi dažnumai</span><span class="sxs-lookup"><span data-stu-id="7683c-676">Supported frequencies</span></span>

- <span data-ttu-id="7683c-677">Visos</span><span class="sxs-lookup"><span data-stu-id="7683c-677">All</span></span>
- <span data-ttu-id="7683c-678">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="7683c-678">EVERYPAY</span></span>
- <span data-ttu-id="7683c-679">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="7683c-679">EACHPAYPERIOD</span></span>
- <span data-ttu-id="7683c-680">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="7683c-680">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="7683c-681">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="7683c-681">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="7683c-682">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-682">1OFMTH</span></span>
- <span data-ttu-id="7683c-683">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-683">LASTOFMTH</span></span>
- <span data-ttu-id="7683c-684">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-684">2OFMTH</span></span>
- <span data-ttu-id="7683c-685">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-685">3OFMTH</span></span>
- <span data-ttu-id="7683c-686">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-686">4OFMTH</span></span>
- <span data-ttu-id="7683c-687">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-687">5OFMTH</span></span>
- <span data-ttu-id="7683c-688">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-688">1N2OFMTH</span></span>
- <span data-ttu-id="7683c-689">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-689">3N4OFMTH</span></span>
- <span data-ttu-id="7683c-690">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-690">1N3OFMTH</span></span>
- <span data-ttu-id="7683c-691">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-691">1N4OFMTH</span></span>
- <span data-ttu-id="7683c-692">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-692">2N3OFMTH</span></span>
- <span data-ttu-id="7683c-693">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-693">2N4OFMTH</span></span>
- <span data-ttu-id="7683c-694">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-694">1N2N3OFMTH</span></span>
- <span data-ttu-id="7683c-695">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-695">1N2N4OFMTH</span></span>
- <span data-ttu-id="7683c-696">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-696">1N3N4OFMTH</span></span>
- <span data-ttu-id="7683c-697">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-697">2N3N4OFMTH</span></span>
- <span data-ttu-id="7683c-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="7683c-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="7683c-699">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="7683c-699">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="7683c-700">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="7683c-700">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="7683c-701">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="7683c-701">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="7683c-702">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="7683c-702">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="7683c-703">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="7683c-703">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="7683c-704">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="7683c-704">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="7683c-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="7683c-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="7683c-706">Adresai</span><span class="sxs-lookup"><span data-stu-id="7683c-706">Addresses</span></span>

<span data-ttu-id="7683c-707">Konkrečios šalies ar regiono, valstijos ir apygardos (savivaldybės) kodų identifikacijai reikalingi tam tikri formatai, kuriuos gali atpažinti „Dayforce“ ir šalyje / regione veikiantys teikėjai.</span><span class="sxs-lookup"><span data-stu-id="7683c-707">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="7683c-708">Nors miestų formatas yra kintamas, kiekvienas miestas turi būti susietas su valstija.</span><span class="sxs-lookup"><span data-stu-id="7683c-708">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="7683c-709">„Talent“</span><span class="sxs-lookup"><span data-stu-id="7683c-709">Talent</span></span>              | <span data-ttu-id="7683c-710">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="7683c-710">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="7683c-711">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="7683c-711">Country/Region</span></span>      | <span data-ttu-id="7683c-712">Šalies kodas</span><span class="sxs-lookup"><span data-stu-id="7683c-712">Country Code</span></span>          |
| <span data-ttu-id="7683c-713">Pašto kodas</span><span class="sxs-lookup"><span data-stu-id="7683c-713">Zip/Postal Code</span></span>     | <span data-ttu-id="7683c-714">Pašto indeksas</span><span class="sxs-lookup"><span data-stu-id="7683c-714">Postal Code</span></span>           |
| <span data-ttu-id="7683c-715">Apskritis</span><span class="sxs-lookup"><span data-stu-id="7683c-715">State</span></span>               | <span data-ttu-id="7683c-716">Valstijos kodas</span><span class="sxs-lookup"><span data-stu-id="7683c-716">State Code</span></span>            |
| <span data-ttu-id="7683c-717">Miestas</span><span class="sxs-lookup"><span data-stu-id="7683c-717">City</span></span>                | <span data-ttu-id="7683c-718">Miestas</span><span class="sxs-lookup"><span data-stu-id="7683c-718">City</span></span>                  |
| <span data-ttu-id="7683c-719">Apygarda</span><span class="sxs-lookup"><span data-stu-id="7683c-719">County</span></span>              | <span data-ttu-id="7683c-720">Apygarda (savivaldybė)</span><span class="sxs-lookup"><span data-stu-id="7683c-720">County (Municipality)</span></span> |
| <span data-ttu-id="7683c-721">Gatvė</span><span class="sxs-lookup"><span data-stu-id="7683c-721">Street</span></span>              | <span data-ttu-id="7683c-722">1 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="7683c-722">Address Line 1</span></span>        |
| <span data-ttu-id="7683c-723">Gatvė, namo nr.</span><span class="sxs-lookup"><span data-stu-id="7683c-723">Street Number</span></span>       | <span data-ttu-id="7683c-724">2 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="7683c-724">Address Line 2</span></span>        |
| <span data-ttu-id="7683c-725">Pastatų kompleksas</span><span class="sxs-lookup"><span data-stu-id="7683c-725">Building Complement</span></span> | <span data-ttu-id="7683c-726">5 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="7683c-726">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="7683c-727">Paso numeris</span><span class="sxs-lookup"><span data-stu-id="7683c-727">Passport number</span></span>

<span data-ttu-id="7683c-728">Darbuotojai gali paskelbti paso informaciją.</span><span class="sxs-lookup"><span data-stu-id="7683c-728">Employees can declare passport information.</span></span> <span data-ttu-id="7683c-729">Ši informacija yra **Paso** identifikacijos tipo pobūdžio ir yra integruota į „Dayforce“ kaip dalis darbuotojo informacijos, susijusios su Meksika.</span><span class="sxs-lookup"><span data-stu-id="7683c-729">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="7683c-730">Identifikacijos tipas = "Pasas"</span><span class="sxs-lookup"><span data-stu-id="7683c-730">Identification Type = "Passport"</span></span>
- <span data-ttu-id="7683c-731">Išdavimo data</span><span class="sxs-lookup"><span data-stu-id="7683c-731">Issued Date</span></span>
- <span data-ttu-id="7683c-732">Galiojimo data</span><span class="sxs-lookup"><span data-stu-id="7683c-732">Expiration Date</span></span>

<span data-ttu-id="7683c-733">Darbuotojai gali paskelbti kelis **Paso** identifikacijos tipo identifikacijos numerius.</span><span class="sxs-lookup"><span data-stu-id="7683c-733">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="7683c-734">Tačiau į „Dayforce“ integruojamas tik dabartinis aktyvus paso įrašas.</span><span class="sxs-lookup"><span data-stu-id="7683c-734">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="7683c-735">Jei nebegalioja visi paso įrašai, į „Dayforce“ integruojamas pasas, kuris buvo išduotas vėliausiai.</span><span class="sxs-lookup"><span data-stu-id="7683c-735">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
