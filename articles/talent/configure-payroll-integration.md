---
title: "Algalapio integravimo tarp „Talent“ ir „Dayforce“ konfigūravimas"
description: "Šioje temoje paaiškinama, kaip sukonfigūruoti integravimą tarp „Microsošt Dynamics 365 for Talent“ ir „Ceridian Dayforce“, kad galėtumėte apdoroti mokėjimo vykdymą."
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---

# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="a8a29-103">Algalapio integravimo tarp „Talent“ ir „Dayforce“ konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a8a29-104">Integravimas tarp „Microsoft Dynamics 365 for Talent“ ir „Ceridian Dayforce“ paremtas keliais konfigūravimo veiksmais, aprašytais šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="a8a29-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="a8a29-105">Prieš mokėjimo vykdymo apdorojimą turite sukonfigūruoti integravimą tiek „Talent“, tiek „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="a8a29-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="a8a29-106">Kai naudojate paslaugas, pvz., „Dayforce“ kad atliktumėte mokėjimų vykdymus, turite įjungti integravimą į „Talent“.</span><span class="sxs-lookup"><span data-stu-id="a8a29-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="a8a29-107">Integravimui reikalingi konkretūs duomenys iš „Talent“.</span><span class="sxs-lookup"><span data-stu-id="a8a29-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="a8a29-108">Todėl turite patvirtinti, kad duomenys, susieti su „Dayforce“, yra sukonfigūruojami „Talent“ taip, kad integravimas būtų palaikomas.</span><span class="sxs-lookup"><span data-stu-id="a8a29-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="a8a29-109">Integravimui naudojamos šios plačios duomenų kategorijos:</span><span class="sxs-lookup"><span data-stu-id="a8a29-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="a8a29-110">Personalo duomenys</span><span class="sxs-lookup"><span data-stu-id="a8a29-110">Human resources data</span></span>
- <span data-ttu-id="a8a29-111">Kompensacijos duomenys</span><span class="sxs-lookup"><span data-stu-id="a8a29-111">Compensation data</span></span>
- <span data-ttu-id="a8a29-112">Algalapio duomenys, pvz., mokėjimo ciklai, mokėjimo laikotarpiai ir pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="a8a29-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="a8a29-113">Darbininko duomenys</span><span class="sxs-lookup"><span data-stu-id="a8a29-113">Worker data</span></span>

<span data-ttu-id="a8a29-114">Šioje temoje aprašomi veiksmai, kuriuos reikia vykdyti norint įjungti integravimą.</span><span class="sxs-lookup"><span data-stu-id="a8a29-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="a8a29-115">Joje taip pat paaiškinami duomenų tipai ir išsami konfigūravimo informacija, reikalinga integravimui.</span><span class="sxs-lookup"><span data-stu-id="a8a29-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="a8a29-116">Integravimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-116">Enable the integration</span></span>

<span data-ttu-id="a8a29-117">Pirmiausia „Talent“ turite įjungti integravimą ir įvesti konfigūravimo informaciją, kad prisijungtumėte prie „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="a8a29-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="a8a29-118">Jei norite, kad sukuriama didžiosios knygos operacija būtų importuota į „Microsoft Dynamics 365 for Finance and Operations“, taip pat turite sukurti „Microsoft Azure“ saugyklos paskyrą ir įvesti „Azure Storage“ jungimosi eilutę į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="a8a29-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="a8a29-119">Norėdami įjungti integravimą į „Talent“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a8a29-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="a8a29-120">Puslapyje **Sistemos administravimas** pasirinkite **Integravimo konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="a8a29-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="a8a29-121">Įveskite saugų failų perdavimo protokolo (FTP) galinį punktą ir saugų FTP aplanko kelią.</span><span class="sxs-lookup"><span data-stu-id="a8a29-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="a8a29-122">Įveskite vardą ir slaptažodį to vartotojo, kuris turės prieigą prie saugaus FTP galinio punkto ir aplanko kelio.</span><span class="sxs-lookup"><span data-stu-id="a8a29-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="a8a29-123">Tinkamai išbandykite ryšį ir nustatykite parinktį **Įjungti algalapių integravimą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="a8a29-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="a8a29-124">Kai integravimas įjungiamas, sukuriamas duomenų eksportavimo paketas bei failai ir nustatomas dažnumas.</span><span class="sxs-lookup"><span data-stu-id="a8a29-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="a8a29-125">Galite pakeisti šį dažnumą pagal poreikį.</span><span class="sxs-lookup"><span data-stu-id="a8a29-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="a8a29-126">Daugiau informacijos apie „Azure“ saugyklos paskyras ir „Azure Storage“ jungimosi eilutes rasite šiose „Azure“ temose:</span><span class="sxs-lookup"><span data-stu-id="a8a29-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="a8a29-127">Apie „Azure“ saugyklos paskyras</span><span class="sxs-lookup"><span data-stu-id="a8a29-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="a8a29-128">„Azure Storage“ jungimosi eilučių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="a8a29-129">Jūsų duomenų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-129">Configure your data</span></span> 

<span data-ttu-id="a8a29-130">Kad apdorotumėte algalapį, turite sukonfigūruoti personalo duomenis „Talent“.</span><span class="sxs-lookup"><span data-stu-id="a8a29-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="a8a29-131">Turite nustatyti organizacijos duomenis, pvz., užduotis ir pareigas, taip pat išmokų ir kompensacijos informaciją.</span><span class="sxs-lookup"><span data-stu-id="a8a29-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="a8a29-132">Čia pateikiama įdarbinimo, mokėjimų ir atskaitymų informacija, būtina tam, kad būtų galima sugeneruoti darbuotojo mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="a8a29-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="a8a29-133">Personalo duomenys</span><span class="sxs-lookup"><span data-stu-id="a8a29-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="a8a29-134">Išmokos</span><span class="sxs-lookup"><span data-stu-id="a8a29-134">Benefits</span></span> 

<span data-ttu-id="a8a29-135">Personalas pateikia įrankius, kuriuos galima naudoti norint nustatyti ir tvarkyti organizacijos darbuotojams siūlomas arba apdorojamas išmokas, atskaitymus ir darbininkų kompensacijų planus.</span><span class="sxs-lookup"><span data-stu-id="a8a29-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="a8a29-136">Kurdami išmokas turėkite omenyje, kad toliau pateikiami duomenys ir konfigūracijos naudojami „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="a8a29-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="a8a29-137">Išmokų planai</span><span class="sxs-lookup"><span data-stu-id="a8a29-137">Benefit plans</span></span>

- <span data-ttu-id="a8a29-138">Planas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-138">Plan (required)</span></span>
- <span data-ttu-id="a8a29-139">Tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-139">Type (required)</span></span>
- <span data-ttu-id="a8a29-140">Poveikis algalapiui (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-140">Payroll impact (required)</span></span>
- <span data-ttu-id="a8a29-141">Susigrąžinti skolas</span><span class="sxs-lookup"><span data-stu-id="a8a29-141">Recover arrears</span></span>
- <span data-ttu-id="a8a29-142">Atskaitymo metodas</span><span class="sxs-lookup"><span data-stu-id="a8a29-142">Deduction method</span></span>
- <span data-ttu-id="a8a29-143">Atskaitymo pirmumas</span><span class="sxs-lookup"><span data-stu-id="a8a29-143">Deduction priority</span></span>
- <span data-ttu-id="a8a29-144">Apribojimo laikotarpis</span><span class="sxs-lookup"><span data-stu-id="a8a29-144">Limit period</span></span>
- <span data-ttu-id="a8a29-145">Limito suma</span><span class="sxs-lookup"><span data-stu-id="a8a29-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="a8a29-146">Išmokos</span><span class="sxs-lookup"><span data-stu-id="a8a29-146">Benefits</span></span>

- <span data-ttu-id="a8a29-147">Planas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-147">Plan (required)</span></span>
- <span data-ttu-id="a8a29-148">Tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-148">Type (required)</span></span>
- <span data-ttu-id="a8a29-149">Parinktis (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-149">Option (required)</span></span>
- <span data-ttu-id="a8a29-150">Išmokos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-150">Benefit ID (required)</span></span>
- <span data-ttu-id="a8a29-151">Dažnumas</span><span class="sxs-lookup"><span data-stu-id="a8a29-151">Frequency</span></span>
- <span data-ttu-id="a8a29-152">Pagrindas</span><span class="sxs-lookup"><span data-stu-id="a8a29-152">Basis</span></span>
- <span data-ttu-id="a8a29-153">Suma arba tarifas</span><span class="sxs-lookup"><span data-stu-id="a8a29-153">Amount or rate</span></span>
- <span data-ttu-id="a8a29-154">Pajamų kodas</span><span class="sxs-lookup"><span data-stu-id="a8a29-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="a8a29-155">Palaikomi dažnumai</span><span class="sxs-lookup"><span data-stu-id="a8a29-155">Supported frequencies</span></span> 

- <span data-ttu-id="a8a29-156">Savaitinis</span><span class="sxs-lookup"><span data-stu-id="a8a29-156">Weekly</span></span>
- <span data-ttu-id="a8a29-157">Už dvi savaites</span><span class="sxs-lookup"><span data-stu-id="a8a29-157">Bi-weekly</span></span>
- <span data-ttu-id="a8a29-158">Kas pusę mėnesio</span><span class="sxs-lookup"><span data-stu-id="a8a29-158">Semi-monthly</span></span>
- <span data-ttu-id="a8a29-159">Mėnesinis</span><span class="sxs-lookup"><span data-stu-id="a8a29-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="a8a29-160">Palaikomos bazės</span><span class="sxs-lookup"><span data-stu-id="a8a29-160">Supported bases</span></span> 

- <span data-ttu-id="a8a29-161">Fiksuota suma</span><span class="sxs-lookup"><span data-stu-id="a8a29-161">Fixed amount</span></span>
- <span data-ttu-id="a8a29-162">Pajamų procentinė dalis</span><span class="sxs-lookup"><span data-stu-id="a8a29-162">Percent of earnings</span></span>
- <span data-ttu-id="a8a29-163">Produktyvios valandos</span><span class="sxs-lookup"><span data-stu-id="a8a29-163">Productive hours</span></span>

<span data-ttu-id="a8a29-164">„Dayforce“ sukuria šiuos atskaitymus pagal poveikį atlyginimui, šis poveikis apibrėžiamas išmokų plane.</span><span class="sxs-lookup"><span data-stu-id="a8a29-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="a8a29-165">Pasirinkimas „Talent“</span><span class="sxs-lookup"><span data-stu-id="a8a29-165">Selection in Talent</span></span>        | <span data-ttu-id="a8a29-166">Rezultatas „Dayforce“</span><span class="sxs-lookup"><span data-stu-id="a8a29-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="a8a29-167">None</span><span class="sxs-lookup"><span data-stu-id="a8a29-167">None</span></span>                       | <span data-ttu-id="a8a29-168">Nesukuriama jokio atskaitymo.</span><span class="sxs-lookup"><span data-stu-id="a8a29-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="a8a29-169">Tik atskaitymas</span><span class="sxs-lookup"><span data-stu-id="a8a29-169">Deduction only</span></span>             | <span data-ttu-id="a8a29-170">Sukuriamas darbuotojo atskaitymas.</span><span class="sxs-lookup"><span data-stu-id="a8a29-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="a8a29-171">Tik įnašas</span><span class="sxs-lookup"><span data-stu-id="a8a29-171">Contribution only</span></span>          | <span data-ttu-id="a8a29-172">Sukuriamas darbdavio atskaitymas.</span><span class="sxs-lookup"><span data-stu-id="a8a29-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="a8a29-173">Atskaitymas ir įnašas</span><span class="sxs-lookup"><span data-stu-id="a8a29-173">Deduction and contribution</span></span> | <span data-ttu-id="a8a29-174">Sukuriami darbuotojo ir darbdavio atskaitymai.</span><span class="sxs-lookup"><span data-stu-id="a8a29-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="a8a29-175">Daugiau informacijos apie tai, kaip nustatyti ir tvarkyti išlaidų programą, rasite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="a8a29-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="a8a29-176">Pristatyti darbuotojų išmokų programą</span><span class="sxs-lookup"><span data-stu-id="a8a29-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="a8a29-177">Kurti naują išmoką</span><span class="sxs-lookup"><span data-stu-id="a8a29-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="a8a29-178">Apibrėžti išmokų tinkamumo taisykles ir strategijas</span><span class="sxs-lookup"><span data-stu-id="a8a29-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="a8a29-179">Užregistruoti ir pašalinti išmokas darbuotojams</span><span class="sxs-lookup"><span data-stu-id="a8a29-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="a8a29-180">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="a8a29-180">Compensation</span></span> 

<span data-ttu-id="a8a29-181">Kompensacijų valdymas naudojamas kontroliuoti pagrindinio užmokesčio ir premijų pristatymui.</span><span class="sxs-lookup"><span data-stu-id="a8a29-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="a8a29-182">Darbuotojo fiksuotas pagrindinis užmokestis ir nuopelnų padidėjimai kontroliuojami naudojant pastoviosios kompensacijos dalies planus.</span><span class="sxs-lookup"><span data-stu-id="a8a29-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="a8a29-183">Skatinamųjų išmokų, pvz., priedų, apdovanojimų už našumą, akcijų pasirinkimo sandorių, subsidijų bei vienkartinių premijų mokėjimas valdomas naudojant kintamosios kompensacijos dalies planus.</span><span class="sxs-lookup"><span data-stu-id="a8a29-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="a8a29-184">„Dayforce“ naudojama kompensacijos informacija, kad būtų apskaičiuotas darbuotojo valandinis ar metinis tarifas.</span><span class="sxs-lookup"><span data-stu-id="a8a29-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="a8a29-185">Būtini pastoviosios atlyginimo dalies planai ir užmokesčio tarifo konvertavimas.</span><span class="sxs-lookup"><span data-stu-id="a8a29-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="a8a29-186">Darbuotojai turi būti susieti su pastoviosios atlyginimo dalies planu.</span><span class="sxs-lookup"><span data-stu-id="a8a29-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="a8a29-187">Daugiau informacijos apie kompensacijų planus rasite šios temose:</span><span class="sxs-lookup"><span data-stu-id="a8a29-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="a8a29-188">Pastoviosios atlyginimo dalies planų kūrimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="a8a29-189">Kintamosios atlyginimo dalies planų kūrimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="a8a29-190">Kurti atlyginimų / kompensavimo struktūrą ir planus</span><span class="sxs-lookup"><span data-stu-id="a8a29-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="a8a29-191">Kompensavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="a8a29-192">Kompensavimo proceso nustatymas ir rezultatų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="a8a29-193">Darbuotojo įtraukimas į fiksuoto atlyginimo dalies planą</span><span class="sxs-lookup"><span data-stu-id="a8a29-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="a8a29-194">Darbuotojo įtraukimas į kintamosios atlyginimo dalies planą</span><span class="sxs-lookup"><span data-stu-id="a8a29-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="a8a29-195">Darbai</span><span class="sxs-lookup"><span data-stu-id="a8a29-195">Jobs</span></span> 

<span data-ttu-id="a8a29-196">Užduotis yra užduočių ir pareigų, kurias asmeniui reikia įvykdyti, rinkinys.</span><span class="sxs-lookup"><span data-stu-id="a8a29-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="a8a29-197">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="a8a29-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="a8a29-198">Užduoties komponentų nustatymas</span><span class="sxs-lookup"><span data-stu-id="a8a29-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="a8a29-199">Apibrėžti naujas užduotis</span><span class="sxs-lookup"><span data-stu-id="a8a29-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="a8a29-200">Pareigybės</span><span class="sxs-lookup"><span data-stu-id="a8a29-200">Positions</span></span>

<span data-ttu-id="a8a29-201">Pareigos yra atskiros užduoties egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="a8a29-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="a8a29-202">Pavyzdžiui, pareigos „Pardavimo vadybininkas (rytų regionas)“ yra vienos iš pareigų, susietų su užduotimi „Pardavimo vadovas“.</span><span class="sxs-lookup"><span data-stu-id="a8a29-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="a8a29-203">Pareigos egzistuoja padalinyje.</span><span class="sxs-lookup"><span data-stu-id="a8a29-203">A position exists in a department.</span></span> <span data-ttu-id="a8a29-204">Su kiekvienomis pareigomis galima susieti tik vieną darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="a8a29-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="a8a29-205">Nustatydami pareigas, atkreipkite dėmesį į šiuos duomenis ir konfigūravimą:</span><span class="sxs-lookup"><span data-stu-id="a8a29-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="a8a29-206">Pareigos (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-206">Position (required)</span></span>
- <span data-ttu-id="a8a29-207">Aprašas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-207">Description (required)</span></span>
- <span data-ttu-id="a8a29-208">Užduotis (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-208">Job (required)</span></span>
- <span data-ttu-id="a8a29-209">Padalinys (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-209">Department (required)</span></span>
- <span data-ttu-id="a8a29-210">Pareigų tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-210">Position type (required)</span></span>
- <span data-ttu-id="a8a29-211">Viso etato ekvivalentas</span><span class="sxs-lookup"><span data-stu-id="a8a29-211">Full-time equivalent</span></span>
- <span data-ttu-id="a8a29-212">Įprastos darbo valandos per metus (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="a8a29-213">Apmokama juridinio subjekto (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="a8a29-214">Mokėjimo ciklas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-214">Pay cycle (required)</span></span>
- <span data-ttu-id="a8a29-215">Numatytosios finansinės dimensijos – išlaidų centras (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="a8a29-216">Darbininko priskyrimas – darbininkas, priskyrimo pradžia, priskyrimo pabaiga, priežasties kodas</span><span class="sxs-lookup"><span data-stu-id="a8a29-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="a8a29-217">Jei tame pačiame padalinyje su tuo pačiu darbu susiejamos kelios pareigos, „Dayforce“ jos yra konsoliduojamos į vienas pareigas.</span><span class="sxs-lookup"><span data-stu-id="a8a29-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="a8a29-218">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="a8a29-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="a8a29-219">Darbo jėgos organizavimas naudojant padalinius, darbo vietas ir pareigas</span><span class="sxs-lookup"><span data-stu-id="a8a29-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="a8a29-220">Pareigų nustatymas</span><span class="sxs-lookup"><span data-stu-id="a8a29-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="a8a29-221">Padaliniai</span><span class="sxs-lookup"><span data-stu-id="a8a29-221">Departments</span></span>

<span data-ttu-id="a8a29-222">Padalinys yra valdymo vienetas, nurodantis organizacijos kategoriją arba funkcinę sritį.</span><span class="sxs-lookup"><span data-stu-id="a8a29-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="a8a29-223">Padalinys yra atsakingas už tam tikrą organizacijos sritį, pvz., pardavimą, apskaitą arba personalą.</span><span class="sxs-lookup"><span data-stu-id="a8a29-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="a8a29-224">Padalinius galite naudoti norėdami pranešti apie funkcines sritis.</span><span class="sxs-lookup"><span data-stu-id="a8a29-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="a8a29-225">Padaliniai gali turėti pelno ir nuostolio atsakomybę.</span><span class="sxs-lookup"><span data-stu-id="a8a29-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="a8a29-226">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="a8a29-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="a8a29-227">Padalinio kūrimas ir priskyrimas padalinių hierarchijai</span><span class="sxs-lookup"><span data-stu-id="a8a29-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="a8a29-228">Apibrėžti naujus padalinius</span><span class="sxs-lookup"><span data-stu-id="a8a29-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="a8a29-229">Mokėjimo ciklai ir mokėjimo laikotarpiai</span><span class="sxs-lookup"><span data-stu-id="a8a29-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="a8a29-230">Mokėjimo ciklas lemia algalapio pateikimo dažnumą ir konkrečias dienas, kuriomis sumokama darbininkams.</span><span class="sxs-lookup"><span data-stu-id="a8a29-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="a8a29-231">Pavyzdžiui, mokėjimo ciklas gali būti mėnesinis ir darbuotojams gali būti sumokėta paskutinę mėnesio dieną.</span><span class="sxs-lookup"><span data-stu-id="a8a29-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="a8a29-232">Mokėjimo ciklas taip pat gali būti savaitinis, o darbuotojams gali būti sumokama kitą antradienį po mokėjimo laikotarpio pabaigos.</span><span class="sxs-lookup"><span data-stu-id="a8a29-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="a8a29-233">Mokėjimo ciklai priskiriami pareigoms tam, kad būtų galima valdyti, kada sumokama tas pareigas einantiems darbininkams.</span><span class="sxs-lookup"><span data-stu-id="a8a29-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="a8a29-234">Sukūrę mokėjimo ciklus, galite generuoti kiekvieno ciklo mokėjimo laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="a8a29-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="a8a29-235">Į kiekvieną mokėjimo laikotarpį įeina numatytoji mokėjimo data, paremta jūsų pateikta informacija.</span><span class="sxs-lookup"><span data-stu-id="a8a29-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="a8a29-236">Tačiau galite pakeisti numatytąją mokėjimo datą mokėjimo laikotarpyje, kad leistumėte išimtis, pvz., tuo atveju, jei mokėjimo data sutampa su švente.</span><span class="sxs-lookup"><span data-stu-id="a8a29-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="a8a29-237">„Dayforce“ naudojama ši informacija:</span><span class="sxs-lookup"><span data-stu-id="a8a29-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="a8a29-238">Mokėjimo ciklas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-238">Pay cycle (required)</span></span>
- <span data-ttu-id="a8a29-239">Mokėjimo ciklo dažnumas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="a8a29-240">Laikotarpio pradžios data (būtina pirmajam mokėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="a8a29-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="a8a29-241">Numatytoji mokėjimo data (būtina pirmajam mokėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="a8a29-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="a8a29-242">Ši informacija yra integruota į „Dayforce“ kaip mokėjimo grupės ir skiriasi priklausomai nuo šalies ar regiono kiekvienam mokėjimo ciklui.</span><span class="sxs-lookup"><span data-stu-id="a8a29-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="a8a29-243">Prieš integravimą reikia sugeneruoti bent vieną mokėjimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="a8a29-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="a8a29-244">„Dayforce“ sugeneruoja mokėjimo grupių kalendorius ir mokėjimo datas pagal pirmojo laikotarpio pradžios datą ir numatytojo mokėjimo datą, nustatytą „Talent“.</span><span class="sxs-lookup"><span data-stu-id="a8a29-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="a8a29-245">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="a8a29-245">Earning codes</span></span>

<span data-ttu-id="a8a29-246">Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas.</span><span class="sxs-lookup"><span data-stu-id="a8a29-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="a8a29-247">Kodams būdingi įvairūs parametrai, susiję su pajamomis, pvz., apskaitos taisyklės, mokesčių įstatymai, ataskaitų kūrimo reikalavimai ir bendrųjų sumų pajėgumas.</span><span class="sxs-lookup"><span data-stu-id="a8a29-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="a8a29-248">„Dayforce“ naudojama ši informacija:</span><span class="sxs-lookup"><span data-stu-id="a8a29-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="a8a29-249">Pajamų kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-249">Earning Code (required)</span></span>
- <span data-ttu-id="a8a29-250">aprašymas</span><span class="sxs-lookup"><span data-stu-id="a8a29-250">Description</span></span>
- <span data-ttu-id="a8a29-251">Matavimo vienetas</span><span class="sxs-lookup"><span data-stu-id="a8a29-251">Unit of measure</span></span>
- <span data-ttu-id="a8a29-252">Produktyvus</span><span class="sxs-lookup"><span data-stu-id="a8a29-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="a8a29-253">Darbininko duomenys</span><span class="sxs-lookup"><span data-stu-id="a8a29-253">Worker data</span></span>

<span data-ttu-id="a8a29-254">Įrašai apie jūsų turimus darbininkų tipus yra svarbūs jūsų personalo ir algalapių sistemoms.</span><span class="sxs-lookup"><span data-stu-id="a8a29-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="a8a29-255">Informacija, kurią įvedate, gali būti naudojama darbininkų ir asmeninei informacijai sekti.</span><span class="sxs-lookup"><span data-stu-id="a8a29-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="a8a29-256">Galite tvarkyti šią darbininkų informaciją:</span><span class="sxs-lookup"><span data-stu-id="a8a29-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="a8a29-257">**Pagrindinė** – tvarkykite pagrindinę darbininko informaciją, pvz., kontaktinę informaciją, demografinę informaciją, identifikacijos informaciją, šeimos informaciją, santykį su karine tarnyba, informaciją apie gyvenimą ne tėvynėje ir asmeninius kontaktus bei kontaktinius asmenis nelaimės atveju.</span><span class="sxs-lookup"><span data-stu-id="a8a29-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="a8a29-258">**Įdarbinimas** – tvarkykite informaciją apie darbininko įdarbinimą, pvz., priklausymą įmonei ar organizacijai, priskyrimą pareigoms, pradžios ir pabaigos datas, tinkamumą dirbti, darbo režimą, pensiją, atostogas ir informaciją apie perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="a8a29-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="a8a29-259">**Atostogos ir nebuvimas** – tvarkykite informaciją apie darbininko nebuvimą, pvz., darbo kalendorius, nebuvimo operacijas ir nebuvimo nustatymą.</span><span class="sxs-lookup"><span data-stu-id="a8a29-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="a8a29-260">**Kompensacija ir algalapis** – tvarkykite informaciją apie darbininko kompensacijos planus ir algalapio informaciją, pvz., plano registraciją, apdovanojimus, našumą, komisinius, mokesčių informaciją, išėjimą į pensiją ir atskaitymus iš atlyginimų.</span><span class="sxs-lookup"><span data-stu-id="a8a29-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="a8a29-261">Įvesdami darbininko informaciją turėkite omenyje, kad toliau pateikiami duomenys ir konfigūracijos naudojami „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="a8a29-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="a8a29-262">Bendroji informacija</span><span class="sxs-lookup"><span data-stu-id="a8a29-262">General information</span></span>

- <span data-ttu-id="a8a29-263">Darbuotojo numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-263">Personnel number (required)</span></span>
- <span data-ttu-id="a8a29-264">Vardas (būtinas)</span><span class="sxs-lookup"><span data-stu-id="a8a29-264">First name (required)</span></span>
- <span data-ttu-id="a8a29-265">Pavardė (būtinai)</span><span class="sxs-lookup"><span data-stu-id="a8a29-265">Last name (required)</span></span>
- <span data-ttu-id="a8a29-266">Antras vardas</span><span class="sxs-lookup"><span data-stu-id="a8a29-266">Middle name</span></span>
- <span data-ttu-id="a8a29-267">Paaukštinimo data</span><span class="sxs-lookup"><span data-stu-id="a8a29-267">Seniority date</span></span>
- <span data-ttu-id="a8a29-268">Žinoma kaip</span><span class="sxs-lookup"><span data-stu-id="a8a29-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="a8a29-269">Asmeninė informacija</span><span class="sxs-lookup"><span data-stu-id="a8a29-269">Personal information</span></span>

- <span data-ttu-id="a8a29-270">Šeiminė padėtis (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-270">Marital status (required)</span></span>
- <span data-ttu-id="a8a29-271">Gimimo data (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-271">Birth date (required)</span></span>
- <span data-ttu-id="a8a29-272">Lytis (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-272">Gender (required)</span></span>
- <span data-ttu-id="a8a29-273">Asmuo su negalia</span><span class="sxs-lookup"><span data-stu-id="a8a29-273">Person with disabilities</span></span>
- <span data-ttu-id="a8a29-274">Pilietybės šalies regionas (tik Meksikai)</span><span class="sxs-lookup"><span data-stu-id="a8a29-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="a8a29-275">Adresas</span><span class="sxs-lookup"><span data-stu-id="a8a29-275">Address information</span></span>

- <span data-ttu-id="a8a29-276">Pagrindinis (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-276">Primary (required)</span></span>
- <span data-ttu-id="a8a29-277">Šalis / regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-277">Country/region (required)</span></span>
- <span data-ttu-id="a8a29-278">Pašto kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-278">Postal code (required)</span></span>
- <span data-ttu-id="a8a29-279">Gatvės numeris (būtina) (tik Meksikai)</span><span class="sxs-lookup"><span data-stu-id="a8a29-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="a8a29-280">Pastatų kompleksas (tik Meksikai)</span><span class="sxs-lookup"><span data-stu-id="a8a29-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="a8a29-281">Miestas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-281">City (required)</span></span>
- <span data-ttu-id="a8a29-282">Valstija (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-282">State (required)</span></span>
- <span data-ttu-id="a8a29-283">Apygarda (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="a8a29-284">Kontaktinė informacija</span><span class="sxs-lookup"><span data-stu-id="a8a29-284">Contact information</span></span> 

- <span data-ttu-id="a8a29-285">Pirminis (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-285">Primary (required)</span></span>
- <span data-ttu-id="a8a29-286">Kontakto numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-286">Contact number (required)</span></span>
- <span data-ttu-id="a8a29-287">Išplėtimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="a8a29-288">Algalapio informacija ir pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="a8a29-288">Payroll information and earning codes</span></span>

<span data-ttu-id="a8a29-289">Darbuotojams gali būti priskirtos tam tikros pajamos, išmokamos tam tikru dažnumu, darbuotojai gali turėti pageidaujamą mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="a8a29-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="a8a29-290">Toliau pateikiami laukeliai naudojami „Dayforce“, kad būtų užtikrinta, jog naudojamos tos parinktys ir nustatymai.</span><span class="sxs-lookup"><span data-stu-id="a8a29-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="a8a29-291">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="a8a29-291">Earning codes</span></span>

- <span data-ttu-id="a8a29-292">Pareigos (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-292">Position (required)</span></span>
- <span data-ttu-id="a8a29-293">Pajamų kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-293">Earning Code (required)</span></span>
- <span data-ttu-id="a8a29-294">Dažnumas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-294">Frequency (required)</span></span>
- <span data-ttu-id="a8a29-295">Suma (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="a8a29-296">Algalapių informacija</span><span class="sxs-lookup"><span data-stu-id="a8a29-296">Payroll information</span></span>

- <span data-ttu-id="a8a29-297">Mokėjimo būdas</span><span class="sxs-lookup"><span data-stu-id="a8a29-297">Payment Method</span></span>
- <span data-ttu-id="a8a29-298">Ekonominė sritis (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-298">Economic Region (required)</span></span>
- <span data-ttu-id="a8a29-299">Darbuotojų išmokų ID</span><span class="sxs-lookup"><span data-stu-id="a8a29-299">Employee Benefits ID</span></span>
- <span data-ttu-id="a8a29-300">Asmens kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-300">National ID Number (required)</span></span>
- <span data-ttu-id="a8a29-301">Karo tarnybos numeris</span><span class="sxs-lookup"><span data-stu-id="a8a29-301">Military Service Number</span></span>
- <span data-ttu-id="a8a29-302">Pamainos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-302">Shift ID (required)</span></span>
- <span data-ttu-id="a8a29-303">Mokesčių numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-303">Tax Number (required)</span></span>
- <span data-ttu-id="a8a29-304">Sąjungos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-304">Union ID (required)</span></span>
- <span data-ttu-id="a8a29-305">Darbo dienos ID (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-305">Work Day ID (required)</span></span>
- <span data-ttu-id="a8a29-306">Darbo leidimo numeris</span><span class="sxs-lookup"><span data-stu-id="a8a29-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="a8a29-307">Meksikoje palaikomi šie mokėjimo būdai – **Grynieji**, **Čekis** (įmonės fizinis čekis) ir **Elektroninis mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="a8a29-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="a8a29-308">Jei konkretus mokėjimo būdas nenurodytas, kaip numatytasis būdas naudojamas **Čekis**.</span><span class="sxs-lookup"><span data-stu-id="a8a29-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="a8a29-309">Įdarbinimo informacija</span><span class="sxs-lookup"><span data-stu-id="a8a29-309">Employment details</span></span>

<span data-ttu-id="a8a29-310">Detali įdarbinimo retrospektyva naudojama kaip pagrindinis informacijos šaltinis, kuriuo remiantis „Dayforce“ gaunamos darbuotojo samdos, atleidimo ir pakartotinės samdos būsenos.</span><span class="sxs-lookup"><span data-stu-id="a8a29-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="a8a29-311">„Dayforce“ palaiko tik vieną įdarbinimo įrašą vienu metu.</span><span class="sxs-lookup"><span data-stu-id="a8a29-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="a8a29-312">Įdarbinimo pradžios data (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-312">Employment start date (required)</span></span>
- <span data-ttu-id="a8a29-313">Įdarbinimo pabaigos data</span><span class="sxs-lookup"><span data-stu-id="a8a29-313">Employment end date</span></span>
- <span data-ttu-id="a8a29-314">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="a8a29-314">Start date</span></span>
- <span data-ttu-id="a8a29-315">Patikslinta darbo pradžios data</span><span class="sxs-lookup"><span data-stu-id="a8a29-315">Adjusted start date</span></span>
- <span data-ttu-id="a8a29-316">Atleidimo data (būtina po atleidimo)</span><span class="sxs-lookup"><span data-stu-id="a8a29-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="a8a29-317">Atleidimo priežastis (būtina po atleidimo)</span><span class="sxs-lookup"><span data-stu-id="a8a29-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="a8a29-318">Darbuotojo pagrindinės datos gaunamos naudojant toliau pateikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="a8a29-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="a8a29-319">„Talent“</span><span class="sxs-lookup"><span data-stu-id="a8a29-319">Talent</span></span>                | <span data-ttu-id="a8a29-320">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="a8a29-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8a29-321">Naujausia samdos data</span><span class="sxs-lookup"><span data-stu-id="a8a29-321">Most recent hire date</span></span> | <span data-ttu-id="a8a29-322">Dabartinio nenutraukto įdarbinimo retrospektyvos įrašo įdarbinimo pradžia</span><span class="sxs-lookup"><span data-stu-id="a8a29-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="a8a29-323">Atleidimo data</span><span class="sxs-lookup"><span data-stu-id="a8a29-323">Termination date</span></span>      | <span data-ttu-id="a8a29-324">Dabartinio nenutraukto įdarbinimo retrospektyvos įrašo atleidimo data</span><span class="sxs-lookup"><span data-stu-id="a8a29-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="a8a29-325">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="a8a29-325">Start date</span></span>            | <span data-ttu-id="a8a29-326">Dabartinio neaktyvios įdarbinimo retrospektyvos įrašo koreguota pradžios data, pradžios data ar įdarbinimo pradžia</span><span class="sxs-lookup"><span data-stu-id="a8a29-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="a8a29-327">Pradinio įdarbinimo data</span><span class="sxs-lookup"><span data-stu-id="a8a29-327">Original hire date</span></span>    | <span data-ttu-id="a8a29-328">Anksčiausio įdarbinimo retrospektyvos įrašo įdarbinimo pradžia</span><span class="sxs-lookup"><span data-stu-id="a8a29-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="a8a29-329">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="a8a29-329">Compensation</span></span>

<span data-ttu-id="a8a29-330">Pastoviosios atlyginimo dalies planas turi būti susietas su kiekvieno darbuotojo pagrindinėmis pareigomis įdarbinimo laikotarpio metu.</span><span class="sxs-lookup"><span data-stu-id="a8a29-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="a8a29-331">Šis laikotarpis prasideda nuo tos datos, kai darbuotojas pasamdomas (ar įdarbinimo pradžios datos), ir tęsiasi iki atleidimo.</span><span class="sxs-lookup"><span data-stu-id="a8a29-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="a8a29-332">Įsigaliojimo data (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-332">Effective Date (required)</span></span>
- <span data-ttu-id="a8a29-333">Galiojimo pabaigos data</span><span class="sxs-lookup"><span data-stu-id="a8a29-333">Expiration date</span></span>
- <span data-ttu-id="a8a29-334">Užmokesčio tarifas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-334">Pay Rate (required)</span></span>
- <span data-ttu-id="a8a29-335">Užmokesčio tarifo konvertavimas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="a8a29-336">Metinis atitikmuo (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="a8a29-337">Valandinis atitikmuo (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="a8a29-338">Jei pagal valandas apmokamas darbuotojas eina kelias pareigas, pagrindinių pareigų pastovioji atlyginimo dalis importuojama į „Dayforce“ kaip darbuotojo lygmens bazinis tarifas / alga.</span><span class="sxs-lookup"><span data-stu-id="a8a29-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="a8a29-339">Nepagrindinių pareigų valandinis tarifas išsaugomas atitinkamose pareigose „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="a8a29-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="a8a29-340">Jei etatinis darbuotojas eina kelias pareigas, iš visų aktyvių pareigų išvedamas suvestinis valandinis tarifas bei metinė alga ir jie naudojami kaip darbuotojo lygmens bazinis tarifas / alga.</span><span class="sxs-lookup"><span data-stu-id="a8a29-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="a8a29-341">Identifikavimo numeriai</span><span class="sxs-lookup"><span data-stu-id="a8a29-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="a8a29-342">Socialinio draudimo identifikatorius</span><span class="sxs-lookup"><span data-stu-id="a8a29-342">Social Security identifier</span></span> 

<span data-ttu-id="a8a29-343">Kiekvienas darbuotojas turi turėti vieną pirminį identifikatorių.</span><span class="sxs-lookup"><span data-stu-id="a8a29-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="a8a29-344">Šis identifikatorius turi būti **SSN** identifikacijos tipo.</span><span class="sxs-lookup"><span data-stu-id="a8a29-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="a8a29-345">„Dayforce“ jis automatiškai išvedamas kaip darbuotojo socialinio draudimo identifikatorius, kuris yra būtinas samdai.</span><span class="sxs-lookup"><span data-stu-id="a8a29-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="a8a29-346">Pirminis (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-346">Primary (required)</span></span>
- <span data-ttu-id="a8a29-347">Identifikacijos tipas = "SSN"</span><span class="sxs-lookup"><span data-stu-id="a8a29-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="a8a29-348">Išdavimo data</span><span class="sxs-lookup"><span data-stu-id="a8a29-348">Issued Date</span></span>
- <span data-ttu-id="a8a29-349">Galiojimo data</span><span class="sxs-lookup"><span data-stu-id="a8a29-349">Expiration Date</span></span>

<span data-ttu-id="a8a29-350">Darbuotojai gali deklaruoti kelis **SSN** identifikacijos tipo identifikacijos numerius.</span><span class="sxs-lookup"><span data-stu-id="a8a29-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="a8a29-351">Tačiau tik įrašas, pažymėtas kaip **Pirminis**, yra integruojamas į „Dayforce“, nepriklausomai nuo to, ar numeris yra aktyvus ar negaliojantis.</span><span class="sxs-lookup"><span data-stu-id="a8a29-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="a8a29-352">Banko sąskaitos ir išmokos</span><span class="sxs-lookup"><span data-stu-id="a8a29-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="a8a29-353">Jei darbuotojas pasirinko, kad pinigai jam būtų pervesti pavedimu į jo banko sąskaitą, būtina įvesti galiojančią banko sąskaitos informaciją.</span><span class="sxs-lookup"><span data-stu-id="a8a29-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="a8a29-354">„Talent“</span><span class="sxs-lookup"><span data-stu-id="a8a29-354">Talent</span></span>                         | <span data-ttu-id="a8a29-355">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="a8a29-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8a29-356">Banko sąskaitos numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="a8a29-357">SWIFT kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-357">SWIFT code (required)</span></span>          | <span data-ttu-id="a8a29-358">**Banko ID** laukelis naudojamas, apdorojant algalapį Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="a8a29-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="a8a29-359">Filialo numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="a8a29-360">Banko sąskaitos tipas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-360">Bank account type (required)</span></span>   | <span data-ttu-id="a8a29-361">**Sąskaitos tipo** laukelis naudojamas apdorojant algalapį Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="a8a29-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="a8a29-362">Į palaikomas vertes įeina **Tikrinimas** ir **Algalapis**.</span><span class="sxs-lookup"><span data-stu-id="a8a29-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="a8a29-363">Darbuotojai, pasirinkę apmokėjimą pavedimu į banko sąskaitą, turi pateikti nuorodą į likučio sąskaitą, esančią juridiniame subjekte, kurio pirminis adresas yra Meksikoje ir kuris yra susietas su galiojančia banko sąskaita Meksikos banke.</span><span class="sxs-lookup"><span data-stu-id="a8a29-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="a8a29-364">Visos kitos nelikutinės sąskaitos yra ignoruojamos.</span><span class="sxs-lookup"><span data-stu-id="a8a29-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="a8a29-365">Adresas</span><span class="sxs-lookup"><span data-stu-id="a8a29-365">Address information</span></span>

<span data-ttu-id="a8a29-366">Kiekvienas darbuotojas turi turėti vieną pirminę vietą.</span><span class="sxs-lookup"><span data-stu-id="a8a29-366">Every employee must have one primary location.</span></span> <span data-ttu-id="a8a29-367">„Dayforce“ ši vieta naudojama darbuotojo pagrindinei gyvenamajai vietai nustatyti mokesčių tikslais.</span><span class="sxs-lookup"><span data-stu-id="a8a29-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="a8a29-368">Pirminis (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-368">Primary (required)</span></span>
- <span data-ttu-id="a8a29-369">Šalis / regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-369">Country/region (required)</span></span>
- <span data-ttu-id="a8a29-370">Pašto kodas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="a8a29-371">Gatvė (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-371">Street (required)</span></span>
- <span data-ttu-id="a8a29-372">Gatvės numeris (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-372">Street Number (required)</span></span>
- <span data-ttu-id="a8a29-373">Pastatų kompleksas</span><span class="sxs-lookup"><span data-stu-id="a8a29-373">Building Complement</span></span>
- <span data-ttu-id="a8a29-374">Miestas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-374">City (required)</span></span>
- <span data-ttu-id="a8a29-375">Valstija (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-375">State (required)</span></span>
- <span data-ttu-id="a8a29-376">Apygarda (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="a8a29-377">Duomenų konfigūravimas norint generuoti algalapius JAV ir Kanadoje</span><span class="sxs-lookup"><span data-stu-id="a8a29-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="a8a29-378">Jei generuojate užmokesčius darbuotojams JAV ir Kanadoje, reikia sukonfigūruoti šiuos elementus:</span><span class="sxs-lookup"><span data-stu-id="a8a29-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="a8a29-379">Su pareigomis būtina nurodyti padalinius.</span><span class="sxs-lookup"><span data-stu-id="a8a29-379">Departments are required on positions.</span></span>
- <span data-ttu-id="a8a29-380">Išlaidų centrai turi būti nustatyti kaip finansinės dimensijos ir būti pirmas elementas numatytoje finansinės dimensijos eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a8a29-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="a8a29-381">Užduočių tipai</span><span class="sxs-lookup"><span data-stu-id="a8a29-381">Job types</span></span>

<span data-ttu-id="a8a29-382">Užduočių tipai naudojami sugrupuoti panašioms užduotims į kategorijas.</span><span class="sxs-lookup"><span data-stu-id="a8a29-382">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="a8a29-383">Užduočių tipai būtini tam, kad algalapiai būtų apdoroti JAV ir Kanadoje.</span><span class="sxs-lookup"><span data-stu-id="a8a29-383">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="a8a29-384">Kai kurie užduočių tipų pavyzdžiai: visa darbo diena ar ne visa darbo diena arba atlyginimas ir valandinis užmokestis.</span><span class="sxs-lookup"><span data-stu-id="a8a29-384">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="a8a29-385">Užduočių tipai yra susieti su „Dayforce“ kaip mokėjimo tipai, nurodantys, ar darbuotojas gauna valandinį ar fiksuotą užmokestį.</span><span class="sxs-lookup"><span data-stu-id="a8a29-385">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="a8a29-386">Šie užduočių tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="a8a29-386">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="a8a29-387">Darbo vietos tipas</span><span class="sxs-lookup"><span data-stu-id="a8a29-387">Job type</span></span>   | <span data-ttu-id="a8a29-388">aprašymas</span><span class="sxs-lookup"><span data-stu-id="a8a29-388">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="a8a29-389">Valandinis</span><span class="sxs-lookup"><span data-stu-id="a8a29-389">Hourly</span></span>     | <span data-ttu-id="a8a29-390">Valandinis</span><span class="sxs-lookup"><span data-stu-id="a8a29-390">Hourly</span></span>      |
| <span data-ttu-id="a8a29-391">Fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-391">Salaried</span></span>   | <span data-ttu-id="a8a29-392">Fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-392">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="a8a29-393">Pareigų tipai</span><span class="sxs-lookup"><span data-stu-id="a8a29-393">Position types</span></span> 

<span data-ttu-id="a8a29-394">Pareigų tipus naudojate tam, kad apibrėžtumėte, ar pareigoms skirta visa darbo diena, ne visa darbo diena ar kad esama dar kito varianto.</span><span class="sxs-lookup"><span data-stu-id="a8a29-394">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="a8a29-395">Pareigų tipai yra susieti su „Dayforce“ kaip mokėjimo klasės, nurodančios, ar darbuotojas dirba visą ar ne visą darbo dieną.</span><span class="sxs-lookup"><span data-stu-id="a8a29-395">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="a8a29-396">Šie pareigų tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="a8a29-396">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="a8a29-397">Pareigų tipas</span><span class="sxs-lookup"><span data-stu-id="a8a29-397">Position type</span></span>   | <span data-ttu-id="a8a29-398">aprašymas</span><span class="sxs-lookup"><span data-stu-id="a8a29-398">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="a8a29-399">Visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="a8a29-399">Full-time</span></span>       | <span data-ttu-id="a8a29-400">Darbuotojas, dirbantis visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="a8a29-400">Full time employee</span></span> |
| <span data-ttu-id="a8a29-401">Ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="a8a29-401">Part-time</span></span>       | <span data-ttu-id="a8a29-402">Darbuotojas, dirbantis ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="a8a29-402">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="a8a29-403">Priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="a8a29-403">Reason codes</span></span>

<span data-ttu-id="a8a29-404">Priežasčių kodai pateikia informaciją apie darbuotojo būseną.</span><span class="sxs-lookup"><span data-stu-id="a8a29-404">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="a8a29-405">Priežasčių kodai yra susieti su „Dayforce“ kaip būsenos priežastys, nurodančios darbuotojo pareigų ar įdarbinimo būsenos pokyčių priežastį.</span><span class="sxs-lookup"><span data-stu-id="a8a29-405">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="a8a29-406">Šie priežasčių kodai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="a8a29-406">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="a8a29-407">Tikslinės paskirties šifras</span><span class="sxs-lookup"><span data-stu-id="a8a29-407">Reason code</span></span>    | <span data-ttu-id="a8a29-408">aprašymas</span><span class="sxs-lookup"><span data-stu-id="a8a29-408">Description</span></span>      | <span data-ttu-id="a8a29-409">Taikomi scenarijai</span><span class="sxs-lookup"><span data-stu-id="a8a29-409">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="a8a29-410">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="a8a29-410">RESIGNATION</span></span>    | <span data-ttu-id="a8a29-411">Atsistatydinimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-411">Resignation</span></span>      | <span data-ttu-id="a8a29-412">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="a8a29-412">Terminate worker</span></span>     |
| <span data-ttu-id="a8a29-413">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="a8a29-413">TERMINATION</span></span>    | <span data-ttu-id="a8a29-414">Atleidimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-414">Termination</span></span>      | <span data-ttu-id="a8a29-415">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="a8a29-415">Terminate worker</span></span>     |
| <span data-ttu-id="a8a29-416">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="a8a29-416">RETIREMENT</span></span>     | <span data-ttu-id="a8a29-417">Išėjimas į pensiją</span><span class="sxs-lookup"><span data-stu-id="a8a29-417">Retirement</span></span>       | <span data-ttu-id="a8a29-418">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="a8a29-418">Terminate worker</span></span>     |
| <span data-ttu-id="a8a29-419">KITA</span><span class="sxs-lookup"><span data-stu-id="a8a29-419">OTHER</span></span>          | <span data-ttu-id="a8a29-420">Kitos priežastys</span><span class="sxs-lookup"><span data-stu-id="a8a29-420">Other Reasons</span></span>    | <span data-ttu-id="a8a29-421">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="a8a29-421">Terminate worker</span></span>     |
| <span data-ttu-id="a8a29-422">DEATH</span><span class="sxs-lookup"><span data-stu-id="a8a29-422">DEATH</span></span>          | <span data-ttu-id="a8a29-423">Mirtis</span><span class="sxs-lookup"><span data-stu-id="a8a29-423">Death</span></span>            | <span data-ttu-id="a8a29-424">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="a8a29-424">Terminate worker</span></span>     |
| <span data-ttu-id="a8a29-425">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="a8a29-425">LEAVEOFABSENCE</span></span> | <span data-ttu-id="a8a29-426">Laisvadienis</span><span class="sxs-lookup"><span data-stu-id="a8a29-426">Leave of Absence</span></span> | <span data-ttu-id="a8a29-427">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="a8a29-427">Terminate worker</span></span>     |
| <span data-ttu-id="a8a29-428">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="a8a29-428">CONTRACTEND</span></span>    | <span data-ttu-id="a8a29-429">Sutarties pabaiga</span><span class="sxs-lookup"><span data-stu-id="a8a29-429">End of Contract</span></span>  | <span data-ttu-id="a8a29-430">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="a8a29-430">Terminate worker</span></span>     |
| <span data-ttu-id="a8a29-431">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="a8a29-431">SALARYCHANGE</span></span>   | <span data-ttu-id="a8a29-432">Atlyginimo pasikeitimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-432">Change of Salary</span></span> | <span data-ttu-id="a8a29-433">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="a8a29-433">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="a8a29-434">Šeiminė padėtis</span><span class="sxs-lookup"><span data-stu-id="a8a29-434">Marital status</span></span>

<span data-ttu-id="a8a29-435">Šeiminės padėties vertės yra susietos su „Dayforce“ ir išverčiamos, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="a8a29-435">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="a8a29-436">Toliau pateikiamoje lentelėje parodoma, kaip šeiminės padėties vertės yra susietos su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="a8a29-436">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="a8a29-437">„Talent“</span><span class="sxs-lookup"><span data-stu-id="a8a29-437">Talent</span></span>                 | <span data-ttu-id="a8a29-438">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="a8a29-438">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="a8a29-439">Vedęs / ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="a8a29-439">Married</span></span>                | <span data-ttu-id="a8a29-440">Vedęs / ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="a8a29-440">Married</span></span>              |
| <span data-ttu-id="a8a29-441">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="a8a29-441">Single</span></span>                 | <span data-ttu-id="a8a29-442">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="a8a29-442">Single</span></span>               |
| <span data-ttu-id="a8a29-443">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="a8a29-443">Widowed</span></span>                | <span data-ttu-id="a8a29-444">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="a8a29-444">Widowed</span></span>              |
| <span data-ttu-id="a8a29-445">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="a8a29-445">Divorced</span></span>               | <span data-ttu-id="a8a29-446">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="a8a29-446">Divorced</span></span>             |
| <span data-ttu-id="a8a29-447">Registruota partnerystė</span><span class="sxs-lookup"><span data-stu-id="a8a29-447">Registered Partnership</span></span> | <span data-ttu-id="a8a29-448">Civilinė partnerystė</span><span class="sxs-lookup"><span data-stu-id="a8a29-448">Domestic Partnership</span></span> |
| <span data-ttu-id="a8a29-449">None</span><span class="sxs-lookup"><span data-stu-id="a8a29-449">None</span></span>                   | <span data-ttu-id="a8a29-450">None</span><span class="sxs-lookup"><span data-stu-id="a8a29-450">None</span></span>                 |
| <span data-ttu-id="a8a29-451">Sugyventiniai</span><span class="sxs-lookup"><span data-stu-id="a8a29-451">Cohabiting</span></span>             | <span data-ttu-id="a8a29-452">Sugyventiniai</span><span class="sxs-lookup"><span data-stu-id="a8a29-452">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="a8a29-453">Giminė</span><span class="sxs-lookup"><span data-stu-id="a8a29-453">Gender</span></span>

<span data-ttu-id="a8a29-454">Paskirtoji lytis yra susieta su „Dayforce“ ir išverčiama, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="a8a29-454">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="a8a29-455">Toliau pateikiamoje lentelėje parodoma, kaip paskirtoji lytis yra susieta su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="a8a29-455">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="a8a29-456">„Talent“</span><span class="sxs-lookup"><span data-stu-id="a8a29-456">Talent</span></span>       | <span data-ttu-id="a8a29-457">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="a8a29-457">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="a8a29-458">Vyras</span><span class="sxs-lookup"><span data-stu-id="a8a29-458">Male</span></span>         | <span data-ttu-id="a8a29-459">Vyras</span><span class="sxs-lookup"><span data-stu-id="a8a29-459">Male</span></span>            |
| <span data-ttu-id="a8a29-460">Moteris</span><span class="sxs-lookup"><span data-stu-id="a8a29-460">Female</span></span>       | <span data-ttu-id="a8a29-461">Moteris</span><span class="sxs-lookup"><span data-stu-id="a8a29-461">Female</span></span>          |
| <span data-ttu-id="a8a29-462">Konkrečiai nenurodyta</span><span class="sxs-lookup"><span data-stu-id="a8a29-462">Non-specific</span></span> | <span data-ttu-id="a8a29-463">*Nepalaikoma*</span><span class="sxs-lookup"><span data-stu-id="a8a29-463">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="a8a29-464">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="a8a29-464">Earning codes</span></span>

<span data-ttu-id="a8a29-465">Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas.</span><span class="sxs-lookup"><span data-stu-id="a8a29-465">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="a8a29-466">Kodai apibrėžia kelis parametrus, susijusius su pajamomis, pvz., apskaitos taisykles, mokesčių įstatymus, ataskaitų kūrimo reikalavimus ir bendrųjų sumų pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="a8a29-466">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="a8a29-467">Jei naudojamas nepalaikomas dažnumas, skaičiavimams naudojamas iš anksto numatytasis dažnumas **Kiekvienas mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="a8a29-467">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="a8a29-468">Palaikomi dažnumai</span><span class="sxs-lookup"><span data-stu-id="a8a29-468">Supported frequencies</span></span>

- <span data-ttu-id="a8a29-469">Visos</span><span class="sxs-lookup"><span data-stu-id="a8a29-469">All</span></span>
- <span data-ttu-id="a8a29-470">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="a8a29-470">EVERYPAY</span></span>
- <span data-ttu-id="a8a29-471">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="a8a29-471">EACHPAYPERIOD</span></span>
- <span data-ttu-id="a8a29-472">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="a8a29-472">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="a8a29-473">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="a8a29-473">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="a8a29-474">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-474">1OFMTH</span></span>
- <span data-ttu-id="a8a29-475">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-475">LASTOFMTH</span></span>
- <span data-ttu-id="a8a29-476">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-476">2OFMTH</span></span>
- <span data-ttu-id="a8a29-477">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-477">3OFMTH</span></span>
- <span data-ttu-id="a8a29-478">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-478">4OFMTH</span></span>
- <span data-ttu-id="a8a29-479">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-479">5OFMTH</span></span>
- <span data-ttu-id="a8a29-480">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-480">1N2OFMTH</span></span>
- <span data-ttu-id="a8a29-481">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-481">3N4OFMTH</span></span>
- <span data-ttu-id="a8a29-482">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-482">1N3OFMTH</span></span>
- <span data-ttu-id="a8a29-483">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-483">1N4OFMTH</span></span>
- <span data-ttu-id="a8a29-484">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-484">2N3OFMTH</span></span>
- <span data-ttu-id="a8a29-485">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-485">2N4OFMTH</span></span>
- <span data-ttu-id="a8a29-486">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-486">1N2N3OFMTH</span></span>
- <span data-ttu-id="a8a29-487">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-487">1N2N4OFMTH</span></span>
- <span data-ttu-id="a8a29-488">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-488">1N3N4OFMTH</span></span>
- <span data-ttu-id="a8a29-489">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-489">2N3N4OFMTH</span></span>
- <span data-ttu-id="a8a29-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="a8a29-491">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="a8a29-491">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="a8a29-492">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="a8a29-492">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="a8a29-493">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="a8a29-493">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="a8a29-494">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="a8a29-494">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="a8a29-495">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="a8a29-495">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="a8a29-496">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="a8a29-496">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="a8a29-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="a8a29-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="a8a29-498">Adresai</span><span class="sxs-lookup"><span data-stu-id="a8a29-498">Addresses</span></span>

<span data-ttu-id="a8a29-499">Konkrečios šalies ar regiono, valstijos ir apygardos (savivaldybės) kodų identifikacijai reikalingi tam tikri formatai, kuriuos gali atpažinti „Dayforce“ ir šalyje / regione veikiantys teikėjai.</span><span class="sxs-lookup"><span data-stu-id="a8a29-499">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="a8a29-500">Nors miestų formatas yra kintamas, kiekvienas miestas turi būti susietas su valstija.</span><span class="sxs-lookup"><span data-stu-id="a8a29-500">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="a8a29-501">„Talent“</span><span class="sxs-lookup"><span data-stu-id="a8a29-501">Talent</span></span>          | <span data-ttu-id="a8a29-502">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="a8a29-502">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="a8a29-503">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="a8a29-503">Country/Region</span></span>  | <span data-ttu-id="a8a29-504">Šalies kodas</span><span class="sxs-lookup"><span data-stu-id="a8a29-504">Country Code</span></span>          |
| <span data-ttu-id="a8a29-505">Pašto kodas</span><span class="sxs-lookup"><span data-stu-id="a8a29-505">Zip/Postal Code</span></span> | <span data-ttu-id="a8a29-506">Pašto indeksas</span><span class="sxs-lookup"><span data-stu-id="a8a29-506">Postal Code</span></span>           |
| <span data-ttu-id="a8a29-507">Apskritis</span><span class="sxs-lookup"><span data-stu-id="a8a29-507">State</span></span>           | <span data-ttu-id="a8a29-508">Valstijos kodas</span><span class="sxs-lookup"><span data-stu-id="a8a29-508">State Code</span></span>            |
| <span data-ttu-id="a8a29-509">Miestas</span><span class="sxs-lookup"><span data-stu-id="a8a29-509">City</span></span>            | <span data-ttu-id="a8a29-510">Miestas</span><span class="sxs-lookup"><span data-stu-id="a8a29-510">City</span></span>                  |
| <span data-ttu-id="a8a29-511">Apygarda</span><span class="sxs-lookup"><span data-stu-id="a8a29-511">County</span></span>          | <span data-ttu-id="a8a29-512">Apygarda (savivaldybė)</span><span class="sxs-lookup"><span data-stu-id="a8a29-512">County (Municipality)</span></span> |
| <span data-ttu-id="a8a29-513">Gatvė</span><span class="sxs-lookup"><span data-stu-id="a8a29-513">Street</span></span>          | <span data-ttu-id="a8a29-514">1 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="a8a29-514">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="a8a29-515">Mokesčių regionai</span><span class="sxs-lookup"><span data-stu-id="a8a29-515">Tax regions</span></span>

<span data-ttu-id="a8a29-516">Mokesčių regionai naudojami apibrėžti tinkamam mokesčiui, kuris turėtų būti taikomas generuojant algalapį.</span><span class="sxs-lookup"><span data-stu-id="a8a29-516">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="a8a29-517">Mokesčių regionai yra susieti su „Dayforce“ vietų adresais.</span><span class="sxs-lookup"><span data-stu-id="a8a29-517">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="a8a29-518">Numatytasis mokesčių regionas turi būti susietas su darbininko aktyviomis pareigomis.</span><span class="sxs-lookup"><span data-stu-id="a8a29-518">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="a8a29-519">Mokesčių regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-519">Tax region (required)</span></span>
- <span data-ttu-id="a8a29-520">Šalis / regionas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-520">Country/Region (required)</span></span>
- <span data-ttu-id="a8a29-521">Valstija (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-521">State (required)</span></span>
- <span data-ttu-id="a8a29-522">Apygarda</span><span class="sxs-lookup"><span data-stu-id="a8a29-522">County</span></span> 
- <span data-ttu-id="a8a29-523">Miestas (būtina)</span><span class="sxs-lookup"><span data-stu-id="a8a29-523">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="a8a29-524">Duomenų konfigūravimas sugeneruoti algalapiui Meksikoje</span><span class="sxs-lookup"><span data-stu-id="a8a29-524">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="a8a29-525">Jei generuojate mokėjimus darbuotojams Meksikoje, reikia sukonfigūruoti šiuos elementus:</span><span class="sxs-lookup"><span data-stu-id="a8a29-525">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="a8a29-526">Su pareigomis būtina nurodyti padalinius.</span><span class="sxs-lookup"><span data-stu-id="a8a29-526">Departments are required on positions.</span></span>
- <span data-ttu-id="a8a29-527">Išlaidų centrai turi būti nustatyti kaip finansinės dimensijos ir būti pirmas elementas numatytoje finansinės dimensijos eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a8a29-527">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="a8a29-528">Užduočių tipai</span><span class="sxs-lookup"><span data-stu-id="a8a29-528">Job types</span></span>

<span data-ttu-id="a8a29-529">Užduočių tipai naudojami sugrupuoti panašioms užduotims į kategorijas.</span><span class="sxs-lookup"><span data-stu-id="a8a29-529">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="a8a29-530">Užduočių tipai yra būtini, kad algalapis būtų apdorotas Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="a8a29-530">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="a8a29-531">Kai kurie užduočių tipų pavyzdžiai: visa darbo diena ar ne visa darbo diena arba atlyginimas ir valandinis užmokestis.</span><span class="sxs-lookup"><span data-stu-id="a8a29-531">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="a8a29-532">Užduočių tipai yra susieti su „Dayforce“ kaip mokėjimo tipai, nurodantys, ar darbuotojas gauna valandinį ar fiksuotą užmokestį.</span><span class="sxs-lookup"><span data-stu-id="a8a29-532">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="a8a29-533">Šie užduočių tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="a8a29-533">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="a8a29-534">Darbo vietos tipas</span><span class="sxs-lookup"><span data-stu-id="a8a29-534">Job type</span></span>   | <span data-ttu-id="a8a29-535">aprašymas</span><span class="sxs-lookup"><span data-stu-id="a8a29-535">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="a8a29-536">Valandinis</span><span class="sxs-lookup"><span data-stu-id="a8a29-536">Hourly</span></span>     | <span data-ttu-id="a8a29-537">MX valandinis</span><span class="sxs-lookup"><span data-stu-id="a8a29-537">MX Hourly</span></span>   |
| <span data-ttu-id="a8a29-538">Fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-538">Salaried</span></span>   | <span data-ttu-id="a8a29-539">MX fiksuotas atlyginimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-539">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="a8a29-540">Pareigų tipai</span><span class="sxs-lookup"><span data-stu-id="a8a29-540">Position types</span></span> 

<span data-ttu-id="a8a29-541">Pareigų tipus naudojate tam, kad apibrėžtumėte, ar pareigoms skirta visa darbo diena, ne visa darbo diena ar kad esama dar kito varianto.</span><span class="sxs-lookup"><span data-stu-id="a8a29-541">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="a8a29-542">Pareigų tipai yra susieti su „Dayforce“ kaip mokėjimo klasės, nurodančios, ar darbuotojas dirba visą ar ne visą darbo dieną.</span><span class="sxs-lookup"><span data-stu-id="a8a29-542">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="a8a29-543">Šie pareigų tipai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="a8a29-543">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="a8a29-544">Pareigų tipas</span><span class="sxs-lookup"><span data-stu-id="a8a29-544">Position type</span></span>   | <span data-ttu-id="a8a29-545">aprašymas</span><span class="sxs-lookup"><span data-stu-id="a8a29-545">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="a8a29-546">Visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="a8a29-546">Full-time</span></span>       | <span data-ttu-id="a8a29-547">Darbuotojas, dirbantis visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="a8a29-547">Full time employee</span></span> |
| <span data-ttu-id="a8a29-548">Ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="a8a29-548">Part-time</span></span>       | <span data-ttu-id="a8a29-549">Darbuotojas, dirbantis ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="a8a29-549">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="a8a29-550">Priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="a8a29-550">Reason codes</span></span>

<span data-ttu-id="a8a29-551">Priežasčių kodai pateikia informaciją apie darbuotojo būseną.</span><span class="sxs-lookup"><span data-stu-id="a8a29-551">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="a8a29-552">Priežasčių kodai yra susieti su „Dayforce“ kaip būsenos priežastys, nurodančios darbuotojo pareigų ar įdarbinimo būsenos pokyčių priežastį.</span><span class="sxs-lookup"><span data-stu-id="a8a29-552">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="a8a29-553">Šie priežasčių kodai ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="a8a29-553">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="a8a29-554">Tikslinės paskirties šifras</span><span class="sxs-lookup"><span data-stu-id="a8a29-554">Reason code</span></span>            | <span data-ttu-id="a8a29-555">aprašymas</span><span class="sxs-lookup"><span data-stu-id="a8a29-555">Description</span></span>                    | <span data-ttu-id="a8a29-556">Taikomi scenarijai</span><span class="sxs-lookup"><span data-stu-id="a8a29-556">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="a8a29-557">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="a8a29-557">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="a8a29-558">Išvykimas prieš pirmą algalapį</span><span class="sxs-lookup"><span data-stu-id="a8a29-558">Departure before first payroll</span></span> | <span data-ttu-id="a8a29-559">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="a8a29-559">Terminate worker</span></span>     |
| <span data-ttu-id="a8a29-560">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="a8a29-560">RESIGNATION</span></span>            | <span data-ttu-id="a8a29-561">Atsistatydinimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-561">Resignation</span></span>                    | <span data-ttu-id="a8a29-562">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="a8a29-562">Terminate worker</span></span>     |
| <span data-ttu-id="a8a29-563">PENSION</span><span class="sxs-lookup"><span data-stu-id="a8a29-563">PENSION</span></span>                | <span data-ttu-id="a8a29-564">Pensija</span><span class="sxs-lookup"><span data-stu-id="a8a29-564">Pension</span></span>                        | <span data-ttu-id="a8a29-565">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="a8a29-565">Terminate worker</span></span>     |
| <span data-ttu-id="a8a29-566">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="a8a29-566">TERMINATION</span></span>            | <span data-ttu-id="a8a29-567">Atleidimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-567">Termination</span></span>                    | <span data-ttu-id="a8a29-568">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="a8a29-568">Terminate worker</span></span>     |
| <span data-ttu-id="a8a29-569">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="a8a29-569">RETIREMENT</span></span>             | <span data-ttu-id="a8a29-570">Išėjimas į pensiją</span><span class="sxs-lookup"><span data-stu-id="a8a29-570">Retirement</span></span>                     | <span data-ttu-id="a8a29-571">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="a8a29-571">Terminate worker</span></span>     |
| <span data-ttu-id="a8a29-572">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="a8a29-572">ABSENTEE</span></span>               | <span data-ttu-id="a8a29-573">Nesantysis</span><span class="sxs-lookup"><span data-stu-id="a8a29-573">Absentee</span></span>                       | <span data-ttu-id="a8a29-574">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="a8a29-574">Terminate worker</span></span>     |
| <span data-ttu-id="a8a29-575">KITA</span><span class="sxs-lookup"><span data-stu-id="a8a29-575">OTHER</span></span>                  | <span data-ttu-id="a8a29-576">Kitos priežastys</span><span class="sxs-lookup"><span data-stu-id="a8a29-576">Other Reasons</span></span>                  | <span data-ttu-id="a8a29-577">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="a8a29-577">Terminate worker</span></span>     |
| <span data-ttu-id="a8a29-578">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="a8a29-578">CLOSURE</span></span>                | <span data-ttu-id="a8a29-579">Įmonės uždarymas</span><span class="sxs-lookup"><span data-stu-id="a8a29-579">Business Closure</span></span>               | <span data-ttu-id="a8a29-580">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="a8a29-580">Terminate worker</span></span>     |
| <span data-ttu-id="a8a29-581">DEATH</span><span class="sxs-lookup"><span data-stu-id="a8a29-581">DEATH</span></span>                  | <span data-ttu-id="a8a29-582">Mirtis</span><span class="sxs-lookup"><span data-stu-id="a8a29-582">Death</span></span>                          | <span data-ttu-id="a8a29-583">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="a8a29-583">Terminate worker</span></span>     |
| <span data-ttu-id="a8a29-584">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="a8a29-584">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="a8a29-585">Laisvadienis</span><span class="sxs-lookup"><span data-stu-id="a8a29-585">Leave of Absence</span></span>               | <span data-ttu-id="a8a29-586">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="a8a29-586">Terminate worker</span></span>     |
| <span data-ttu-id="a8a29-587">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="a8a29-587">CONTRACTEND</span></span>            | <span data-ttu-id="a8a29-588">Sutarties pabaiga</span><span class="sxs-lookup"><span data-stu-id="a8a29-588">End of Contract</span></span>                | <span data-ttu-id="a8a29-589">Atleisti darbininką</span><span class="sxs-lookup"><span data-stu-id="a8a29-589">Terminate worker</span></span>     |
| <span data-ttu-id="a8a29-590">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="a8a29-590">SALARYCHANGE</span></span>           | <span data-ttu-id="a8a29-591">Atlyginimo keitimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-591">Change of Salary</span></span>               | <span data-ttu-id="a8a29-592">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="a8a29-592">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="a8a29-593">Įdarbinimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="a8a29-593">Terms of employment</span></span>

<span data-ttu-id="a8a29-594">Įdarbinimo sąlygos naudojamos įdarbinimo sąlygų kategorijoms kurti.</span><span class="sxs-lookup"><span data-stu-id="a8a29-594">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="a8a29-595">Sąlygos yra susietos su „Dayforce“ kaip įdarbinimo indikatorių vertės.</span><span class="sxs-lookup"><span data-stu-id="a8a29-595">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="a8a29-596">Šios įdarbinimo sąlygos ir aprašai yra būtini.</span><span class="sxs-lookup"><span data-stu-id="a8a29-596">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="a8a29-597">Įdarbinimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="a8a29-597">Terms of employment</span></span>   | <span data-ttu-id="a8a29-598">aprašymas</span><span class="sxs-lookup"><span data-stu-id="a8a29-598">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="a8a29-599">Reguliarus</span><span class="sxs-lookup"><span data-stu-id="a8a29-599">Regular</span></span>               | <span data-ttu-id="a8a29-600">Reguliarus</span><span class="sxs-lookup"><span data-stu-id="a8a29-600">Regular</span></span>     |
| <span data-ttu-id="a8a29-601">Tiesioginis</span><span class="sxs-lookup"><span data-stu-id="a8a29-601">Direct</span></span>                | <span data-ttu-id="a8a29-602">Tiesioginis</span><span class="sxs-lookup"><span data-stu-id="a8a29-602">Direct</span></span>      |
| <span data-ttu-id="a8a29-603">Stažuotė</span><span class="sxs-lookup"><span data-stu-id="a8a29-603">Internship</span></span>            | <span data-ttu-id="a8a29-604">Stažuotė</span><span class="sxs-lookup"><span data-stu-id="a8a29-604">Internship</span></span>  |
| <span data-ttu-id="a8a29-605">Nuolatinis</span><span class="sxs-lookup"><span data-stu-id="a8a29-605">Permanent</span></span>             | <span data-ttu-id="a8a29-606">Nuolatinis</span><span class="sxs-lookup"><span data-stu-id="a8a29-606">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="a8a29-607">Šeiminė padėtis</span><span class="sxs-lookup"><span data-stu-id="a8a29-607">Marital status</span></span>

<span data-ttu-id="a8a29-608">Šeiminės padėties vertės yra susietos su „Dayforce“ ir išverčiamos, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="a8a29-608">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="a8a29-609">Toliau pateikiamoje lentelėje parodoma, kaip šeiminės padėties vertės yra susietos su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="a8a29-609">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="a8a29-610">„Talent“</span><span class="sxs-lookup"><span data-stu-id="a8a29-610">Talent</span></span>                 | <span data-ttu-id="a8a29-611">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="a8a29-611">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="a8a29-612">Vedęs / ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="a8a29-612">Married</span></span>                | <span data-ttu-id="a8a29-613">Vedęs / ištekėjusi</span><span class="sxs-lookup"><span data-stu-id="a8a29-613">Married</span></span>                   |
| <span data-ttu-id="a8a29-614">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="a8a29-614">Single</span></span>                 | <span data-ttu-id="a8a29-615">Nevedęs / neištekėjusi</span><span class="sxs-lookup"><span data-stu-id="a8a29-615">Single</span></span>                    |
| <span data-ttu-id="a8a29-616">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="a8a29-616">Widowed</span></span>                | <span data-ttu-id="a8a29-617">Našlys (-ė)</span><span class="sxs-lookup"><span data-stu-id="a8a29-617">Widowed</span></span>                   |
| <span data-ttu-id="a8a29-618">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="a8a29-618">Divorced</span></span>               | <span data-ttu-id="a8a29-619">Išsiskyręs (-usi)</span><span class="sxs-lookup"><span data-stu-id="a8a29-619">Divorced</span></span>                  |
| <span data-ttu-id="a8a29-620">Registruota partnerystė</span><span class="sxs-lookup"><span data-stu-id="a8a29-620">Registered Partnership</span></span> | <span data-ttu-id="a8a29-621">Civilinė partnerystė</span><span class="sxs-lookup"><span data-stu-id="a8a29-621">Domestic Partnership</span></span>      |
| <span data-ttu-id="a8a29-622">None</span><span class="sxs-lookup"><span data-stu-id="a8a29-622">None</span></span>                   | <span data-ttu-id="a8a29-623">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="a8a29-623">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="a8a29-624">Sugyventiniai</span><span class="sxs-lookup"><span data-stu-id="a8a29-624">Cohabiting</span></span>             | <span data-ttu-id="a8a29-625">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="a8a29-625">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="a8a29-626">Giminė</span><span class="sxs-lookup"><span data-stu-id="a8a29-626">Gender</span></span>

<span data-ttu-id="a8a29-627">Paskirtoji lytis yra susieta su „Dayforce“ ir išverčiama, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="a8a29-627">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="a8a29-628">Toliau pateikiamoje lentelėje parodoma, kaip paskirtoji lytis yra susieta su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="a8a29-628">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="a8a29-629">„Talent“</span><span class="sxs-lookup"><span data-stu-id="a8a29-629">Talent</span></span>       | <span data-ttu-id="a8a29-630">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="a8a29-630">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="a8a29-631">Vyras</span><span class="sxs-lookup"><span data-stu-id="a8a29-631">Male</span></span>         | <span data-ttu-id="a8a29-632">Vyras</span><span class="sxs-lookup"><span data-stu-id="a8a29-632">Male</span></span>                      |
| <span data-ttu-id="a8a29-633">Moteris</span><span class="sxs-lookup"><span data-stu-id="a8a29-633">Female</span></span>       | <span data-ttu-id="a8a29-634">Moteris</span><span class="sxs-lookup"><span data-stu-id="a8a29-634">Female</span></span>                    |
| <span data-ttu-id="a8a29-635">Konkrečiai nenurodyta</span><span class="sxs-lookup"><span data-stu-id="a8a29-635">Non-specific</span></span> | <span data-ttu-id="a8a29-636">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="a8a29-636">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="a8a29-637">Mokėjimo būdas</span><span class="sxs-lookup"><span data-stu-id="a8a29-637">Payment method</span></span>

<span data-ttu-id="a8a29-638">Mokėjimo būdai leidžia darbuotojui ir įmonei apibrėžti darbuotojų apmokėjimą.</span><span class="sxs-lookup"><span data-stu-id="a8a29-638">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="a8a29-639">Mokėjimo būdai yra susieti su „Dayforce“ ir išverčiami, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="a8a29-639">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="a8a29-640">Toliau pateikiamoje lentelėje parodoma, kaip mokėjimo būdai yra susieti su „Dayforce“.</span><span class="sxs-lookup"><span data-stu-id="a8a29-640">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="a8a29-641">„Talent“</span><span class="sxs-lookup"><span data-stu-id="a8a29-641">Talent</span></span>             | <span data-ttu-id="a8a29-642">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="a8a29-642">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="a8a29-643">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="a8a29-643">Cash</span></span>               | <span data-ttu-id="a8a29-644">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="a8a29-644">Cash</span></span>                      |
| <span data-ttu-id="a8a29-645">Elektroninis mokėjimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-645">Electronic Payment</span></span> | <span data-ttu-id="a8a29-646">Perkėlimas</span><span class="sxs-lookup"><span data-stu-id="a8a29-646">Transfer</span></span>                  |
| <span data-ttu-id="a8a29-647">Tikrinti</span><span class="sxs-lookup"><span data-stu-id="a8a29-647">Check</span></span>              | <span data-ttu-id="a8a29-648">Čekis</span><span class="sxs-lookup"><span data-stu-id="a8a29-648">Cheque</span></span>                    |
| <span data-ttu-id="a8a29-649">Banko čekis</span><span class="sxs-lookup"><span data-stu-id="a8a29-649">Bank Draft</span></span>         | <span data-ttu-id="a8a29-650">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="a8a29-650">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="a8a29-651">Kiti</span><span class="sxs-lookup"><span data-stu-id="a8a29-651">Other</span></span>              | <span data-ttu-id="a8a29-652">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="a8a29-652">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="a8a29-653">Banko sąskaitos tipas</span><span class="sxs-lookup"><span data-stu-id="a8a29-653">Bank account type</span></span>

<span data-ttu-id="a8a29-654">Banko sąskaitų tipai naudojami elektroniniams mokėjimams į darbuotojų sąskaitas vykdyti.</span><span class="sxs-lookup"><span data-stu-id="a8a29-654">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="a8a29-655">Banko sąskaitų tipai yra susieti su „Dayforce“ kaip pavedimų sąskaitos informacija.</span><span class="sxs-lookup"><span data-stu-id="a8a29-655">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="a8a29-656">Banko sąskaitų tipai yra išverčiami, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.</span><span class="sxs-lookup"><span data-stu-id="a8a29-656">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="a8a29-657">„Talent“</span><span class="sxs-lookup"><span data-stu-id="a8a29-657">Talent</span></span>            | <span data-ttu-id="a8a29-658">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="a8a29-658">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="a8a29-659">Čekių sąskaita</span><span class="sxs-lookup"><span data-stu-id="a8a29-659">Checking Account</span></span>  | <span data-ttu-id="a8a29-660">Čekių sąskaita</span><span class="sxs-lookup"><span data-stu-id="a8a29-660">CheckingAccount</span></span>           |
| <span data-ttu-id="a8a29-661">Algalapių sąskaita</span><span class="sxs-lookup"><span data-stu-id="a8a29-661">Payroll Account</span></span>   | <span data-ttu-id="a8a29-662">Algalapių sąskaita</span><span class="sxs-lookup"><span data-stu-id="a8a29-662">PayrollAccount</span></span>            |
| <span data-ttu-id="a8a29-663">Taupomoji sąskaita</span><span class="sxs-lookup"><span data-stu-id="a8a29-663">Savings Account</span></span>   | <span data-ttu-id="a8a29-664">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="a8a29-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="a8a29-665">„BankGirot“ sąskaita</span><span class="sxs-lookup"><span data-stu-id="a8a29-665">BankGirot account</span></span> | <span data-ttu-id="a8a29-666">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="a8a29-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="a8a29-667">„PlusGirot“ sąskaita</span><span class="sxs-lookup"><span data-stu-id="a8a29-667">PlusGirot account</span></span> | <span data-ttu-id="a8a29-668">*Nepalaikoma Meksikoje*</span><span class="sxs-lookup"><span data-stu-id="a8a29-668">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="a8a29-669">Pajamų kodai</span><span class="sxs-lookup"><span data-stu-id="a8a29-669">Earning codes</span></span>

<span data-ttu-id="a8a29-670">Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas.</span><span class="sxs-lookup"><span data-stu-id="a8a29-670">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="a8a29-671">Kodai apibrėžia kelis parametrus, susijusius su pajamomis, pvz., apskaitos taisykles, mokesčių įstatymus, ataskaitų kūrimo reikalavimus ir bendrųjų sumų pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="a8a29-671">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="a8a29-672">Jei naudojamas nepalaikomas dažnumas, skaičiavimams naudojamas iš anksto numatytasis dažnumas **Kiekvienas mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="a8a29-672">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="a8a29-673">Palaikomi dažnumai</span><span class="sxs-lookup"><span data-stu-id="a8a29-673">Supported frequencies</span></span>

- <span data-ttu-id="a8a29-674">Visos</span><span class="sxs-lookup"><span data-stu-id="a8a29-674">All</span></span>
- <span data-ttu-id="a8a29-675">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="a8a29-675">EVERYPAY</span></span>
- <span data-ttu-id="a8a29-676">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="a8a29-676">EACHPAYPERIOD</span></span>
- <span data-ttu-id="a8a29-677">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="a8a29-677">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="a8a29-678">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="a8a29-678">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="a8a29-679">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-679">1OFMTH</span></span>
- <span data-ttu-id="a8a29-680">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-680">LASTOFMTH</span></span>
- <span data-ttu-id="a8a29-681">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-681">2OFMTH</span></span>
- <span data-ttu-id="a8a29-682">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-682">3OFMTH</span></span>
- <span data-ttu-id="a8a29-683">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-683">4OFMTH</span></span>
- <span data-ttu-id="a8a29-684">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-684">5OFMTH</span></span>
- <span data-ttu-id="a8a29-685">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-685">1N2OFMTH</span></span>
- <span data-ttu-id="a8a29-686">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-686">3N4OFMTH</span></span>
- <span data-ttu-id="a8a29-687">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-687">1N3OFMTH</span></span>
- <span data-ttu-id="a8a29-688">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-688">1N4OFMTH</span></span>
- <span data-ttu-id="a8a29-689">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-689">2N3OFMTH</span></span>
- <span data-ttu-id="a8a29-690">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-690">2N4OFMTH</span></span>
- <span data-ttu-id="a8a29-691">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-691">1N2N3OFMTH</span></span>
- <span data-ttu-id="a8a29-692">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-692">1N2N4OFMTH</span></span>
- <span data-ttu-id="a8a29-693">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-693">1N3N4OFMTH</span></span>
- <span data-ttu-id="a8a29-694">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-694">2N3N4OFMTH</span></span>
- <span data-ttu-id="a8a29-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a8a29-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="a8a29-696">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="a8a29-696">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="a8a29-697">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="a8a29-697">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="a8a29-698">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="a8a29-698">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="a8a29-699">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="a8a29-699">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="a8a29-700">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="a8a29-700">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="a8a29-701">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="a8a29-701">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="a8a29-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="a8a29-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="a8a29-703">Adresai</span><span class="sxs-lookup"><span data-stu-id="a8a29-703">Addresses</span></span>

<span data-ttu-id="a8a29-704">Konkrečios šalies ar regiono, valstijos ir apygardos (savivaldybės) kodų identifikacijai reikalingi tam tikri formatai, kuriuos gali atpažinti „Dayforce“ ir šalyje / regione veikiantys teikėjai.</span><span class="sxs-lookup"><span data-stu-id="a8a29-704">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="a8a29-705">Nors miestų formatas yra kintamas, kiekvienas miestas turi būti susietas su valstija.</span><span class="sxs-lookup"><span data-stu-id="a8a29-705">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="a8a29-706">„Talent“</span><span class="sxs-lookup"><span data-stu-id="a8a29-706">Talent</span></span>              | <span data-ttu-id="a8a29-707">„Dayforce“</span><span class="sxs-lookup"><span data-stu-id="a8a29-707">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="a8a29-708">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="a8a29-708">Country/Region</span></span>      | <span data-ttu-id="a8a29-709">Šalies kodas</span><span class="sxs-lookup"><span data-stu-id="a8a29-709">Country Code</span></span>          |
| <span data-ttu-id="a8a29-710">Pašto kodas</span><span class="sxs-lookup"><span data-stu-id="a8a29-710">Zip/Postal Code</span></span>     | <span data-ttu-id="a8a29-711">Pašto indeksas</span><span class="sxs-lookup"><span data-stu-id="a8a29-711">Postal Code</span></span>           |
| <span data-ttu-id="a8a29-712">Apskritis</span><span class="sxs-lookup"><span data-stu-id="a8a29-712">State</span></span>               | <span data-ttu-id="a8a29-713">Valstijos kodas</span><span class="sxs-lookup"><span data-stu-id="a8a29-713">State Code</span></span>            |
| <span data-ttu-id="a8a29-714">Miestas</span><span class="sxs-lookup"><span data-stu-id="a8a29-714">City</span></span>                | <span data-ttu-id="a8a29-715">Miestas</span><span class="sxs-lookup"><span data-stu-id="a8a29-715">City</span></span>                  |
| <span data-ttu-id="a8a29-716">Apygarda</span><span class="sxs-lookup"><span data-stu-id="a8a29-716">County</span></span>              | <span data-ttu-id="a8a29-717">Apygarda (savivaldybė)</span><span class="sxs-lookup"><span data-stu-id="a8a29-717">County (Municipality)</span></span> |
| <span data-ttu-id="a8a29-718">Gatvė</span><span class="sxs-lookup"><span data-stu-id="a8a29-718">Street</span></span>              | <span data-ttu-id="a8a29-719">1 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="a8a29-719">Address Line 1</span></span>        |
| <span data-ttu-id="a8a29-720">Gatvė, namo nr.</span><span class="sxs-lookup"><span data-stu-id="a8a29-720">Street Number</span></span>       | <span data-ttu-id="a8a29-721">2 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="a8a29-721">Address Line 2</span></span>        |
| <span data-ttu-id="a8a29-722">Pastatų kompleksas</span><span class="sxs-lookup"><span data-stu-id="a8a29-722">Building Complement</span></span> | <span data-ttu-id="a8a29-723">5 adreso eilutė</span><span class="sxs-lookup"><span data-stu-id="a8a29-723">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="a8a29-724">Paso numeris</span><span class="sxs-lookup"><span data-stu-id="a8a29-724">Passport number</span></span>

<span data-ttu-id="a8a29-725">Darbuotojai gali paskelbti paso informaciją.</span><span class="sxs-lookup"><span data-stu-id="a8a29-725">Employees can declare passport information.</span></span> <span data-ttu-id="a8a29-726">Ši informacija yra **Paso** identifikacijos tipo pobūdžio ir yra integruota į „Dayforce“ kaip dalis darbuotojo informacijos, susijusios su Meksika.</span><span class="sxs-lookup"><span data-stu-id="a8a29-726">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="a8a29-727">Identifikacijos tipas = "Pasas"</span><span class="sxs-lookup"><span data-stu-id="a8a29-727">Identification Type = "Passport"</span></span>
- <span data-ttu-id="a8a29-728">Išdavimo data</span><span class="sxs-lookup"><span data-stu-id="a8a29-728">Issued Date</span></span>
- <span data-ttu-id="a8a29-729">Galiojimo data</span><span class="sxs-lookup"><span data-stu-id="a8a29-729">Expiration Date</span></span>

<span data-ttu-id="a8a29-730">Darbuotojai gali paskelbti kelis **Paso** identifikacijos tipo identifikacijos numerius.</span><span class="sxs-lookup"><span data-stu-id="a8a29-730">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="a8a29-731">Tačiau į „Dayforce“ integruojamas tik dabartinis aktyvus paso įrašas.</span><span class="sxs-lookup"><span data-stu-id="a8a29-731">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="a8a29-732">Jei nebegalioja visi paso įrašai, į „Dayforce“ integruojamas pasas, kuris buvo išduotas vėliausiai.</span><span class="sxs-lookup"><span data-stu-id="a8a29-732">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
